---
title: 'Ontwerpdetails: Vraag en aanbod afstemmen | Microsoft Docs'
description: De kern van het planningssysteem omvat het afstemmen van vraag en voorziening via het voorstellen van gebruikeracties om de voorzieningenorders te wijzigen als er geen evenwicht is. Dit vindt plaats per combinatie van variant en vestiging.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: 13ab8097b9c6d75f838a58c347af31d560fa9374
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "914855"
---
# <a name="design-details-balancing-supply-with-demand"></a>Ontwerpdetails: Vraag en aanbod afstemmen
De kern van het planningssysteem omvat het afstemmen van vraag en voorziening via het voorstellen van gebruikeracties om de voorzieningenorders te wijzigen als er geen evenwicht is. Dit vindt plaats per combinatie van variant en vestiging.  

Stel dat elk voorraadprofiel een reeks vraaggebeurtenissen bevat (gesorteerd op datum en prioriteit) en een bijbehorende reeks voorzieninggebeurtenissen. Elke gebeurtenis verwijst terug naar de bronsoort en de identificatie. De regels voor compensatie van het artikel zijn eenvoudig. Vier gevallen van overeenkomende vraag en aanbod kunnen op een bepaald moment in het proces optreden:  

1. Er bestaat geen vraag of voorziening voor het artikel => de planning is voltooid (of moet niet beginnen.)  
2. Vraag bestaat maar er is geen voorziening => voorziening moet worden voorgesteld.  
3. Er is aanbod maar er is geen vraag naar => aanbod moet worden geannuleerd.  
4. Zowel vraag als voorziening bestaan => vragen moeten worden gesteld en beantwoord voordat er kan worden gezorgd dat aan de vraag wordt voldaan en de voorziening toereikend is.  

     Als de timing van het aanbod niet geschikt is, kan het aanbod wellicht als volgt opnieuw worden gepland:  

    1.  Als het aanbod eerder wordt geplaatst dan de vraag, kan het aanbod mogelijk opnieuw uit worden gepland, zodat de voorraad zo klein mogelijk is.  
    2.  Als het aanbod later dan de vraag is geplaatst, kan het aanbod mogelijk opnieuw worden ingepland. Anders stelt het systeem nieuw aanbod voor.  
    3.  Als het aanbod op de datum voldoet aan de vraag, kan het planningssysteem doorgaan met te analyseren of het aantal van het aanbod aan de vraag kan voldoen.  

     Als de timing eenmaal duidelijk is, kan het juiste, te leveren aantal als volgt worden berekend:  

    1.  Als het aanbodaantal kleiner is dan de vraag, is het mogelijk dat het aanbodaantal kan worden vergroot (of niet, indien beperkt door een beleid voor maximaal aantal).  
    2.  Als het aanbodaantal groter is dan de vraag, is het mogelijk dat het aanbodaantal kan worden verminderd (of niet, indien beperkt door een beleid voor minimaal aantal).  

     Op dit punt bestaat een van de volgende twee situaties:  

    1.  De huidige vraag kan worden verwerkt. In dat geval kan het worden afgesloten en kan de planning voor de volgende vraag beginnen.  
    2.  De voorziening heeft het maximum bereikt, waardoor een deel van het vraagaantal niet gedekt is. In dit geval kan het planningssysteem de huidige voorraad sluiten en doorgaan naar de volgende.  

 De procedure begint overnieuw met de volgende vraag en de huidige voorziening of andersom. De huidige voorzieningen kunnen mogelijk deze volgende vraag ook verwerken, of de huidige vraag is nog niet volledig verwerkt.  

## <a name="rules-concerning-actions-for-supply-events"></a>Regels betreffende acties voor voorzieningsgebeurtenissen  
Wanneer het planningssysteem een verticale berekening uitvoert waarin de voorziening moet voldoen aan de vraag, wordt de vraag als een gegeven feit genomen. Dit wil zeggen dat de vraag buiten de invloed van het planningssysteem ligt. De aanbodzijde kan echter worden beheerd. Het planningssysteem stelt daarom voor om nieuwe voorzieningsorders te maken, bestaande orders opnieuw te plannen, en/of het orderaantal te wijzigen. Als een bestaande voorzieningenorder overbodig wordt, stelt het planningssysteem voor dat de gebruiker deze annuleert.  

Als de gebruiker een bestaande voorzieningenorder wil uitsluiten van de planningsuggesties, kan hij stellen dat deze geen planningsflexibiliteit heeft (Planningsflexibiliteit = Geen). Overtollige voorzieningen van die order worden dan gebruikt om de vraag te verwerken, maar er wordt geen actie voorgesteld.  

In het algemeen heeft elk aanbod een planningsflexibiliteit die wordt beperkt door de voorwaarden van elk van de voorgestelde acties.  

-   **Opnieuw uitplannen**: de datum van een bestaande voorzieningenorder kan worden uitgepland om te voldoen aan de vervaldatum van de vraag tenzij:  

    -   De order vertegenwoordigt voorraad (altijd op dag nul).  
    -   De order een order-naar-order koppeling met andere vraag heeft.  
    -   De order ligt buiten de herplanningspagina die door het tijdsinterval wordt gedefinieerd.  
    -   Er is een voorziening dichterbij die kan worden gebruikt.  
    -   Van de andere kant kan de gebruiker besluiten niet te herplannen omdat:  
    -   De voorzieningenorder is al gekoppeld aan een andere vraag op een eerdere datum.  
    -   De benodigde herplanning is zo minimaal dat de gebruiker het verwaarloosbaar vindt.  

-   **Opnieuw inplannen**: de datum van een bestaande voorzieningenorder kan worden ingepland, behalve in de volgende omstandigheden:  

    -   De order is direct aan andere vraag gekoppeld.  
    -   De order ligt buiten de herplanningspagina die door het tijdsinterval wordt gedefinieerd.  

> [!NOTE]  
>  Bij het plannen van een artikel via een bestelpunt kan de voorzieningenorder altijd worden ingepland, indien noodzakelijk. Dit is gebruikelijk bij voorwaarts-geplande voorzieningenorders die worden geactiveerd door een bestelpunt.  

-   **Aantal verhogen**: Het aantal van een bestaande voorzieningenorder kan worden verhoogd om aan de vraag te voldoen, tenzij de voorzieningenorder rechtstreeks aan een vraag is gekoppeld door een order-op-order koppeling.  

> [!NOTE]  
>  Hoewel het mogelijk is om de order voor voorzieningen te verhogen, kan het vanwege een gedefinieerd maximaal orderaantal beperkt zijn.  

-   **Aantal verlagen**: Een bestaande voorzieningenorder met een surplus vergeleken met bestaande vraag kan worden verminderd om aan de vraag te voldoen.  

> [!NOTE]  
>  Hoewel het aantal kan worden verlaagd, kan er toch nog overschot zijn in vergelijking met de vraag wegens een gedefinieerd minimaal orderaantal of orderveelvoud.  

-   **Annuleren**: Als een speciaal incident van de aantal verlagende actie kan de voorzieningenorder worden geannuleerd als deze tot nul is verlaagd.  
-   **Nieuw**: Als er nog geen voorzieningenorder bestaat en er geen bestaande order kan worden gewijzigd om op de gevraagde vervaldatum te voldoen aan het benodigde aantal, wordt een nieuwe voorzieningenorder voorgesteld.  

## <a name="determining-the-supply-quantity"></a>Het voorzieningsaantal bepalen  
Planningsparameters die worden gedefinieerd door de gebruiker, bepalen het voorgestelde aantal van elke voorzieningenorder.  

Wanneer met het planningssysteem het aantal van een nieuwe voorzieningenorder of een wijziging van het aantal voor een bestaande voorzieningenorder wordt berekend, kan het voorgestelde aantal verschillen van wat daadwerkelijk wordt gevraagd.  

Als een maximale voorraad of een vast orderaantal is geselecteerd, kan het voorgestelde aantal worden verhoogd om te voldoen aan dat vaste aantal of de maximale voorraad. Als een bestelbeleid een bestelpunt gebruikt, kan het aantal worden verhoogd om ten minste te voldoen aan het bestelpunt.  

 Het voorgestelde aantal kan worden gewijzigd in deze volgorde:  

1. Tot aan het (eventuele) maximale bestelaantal.  
2. Tot aan het minimale bestelaantal.  
3. Tot aan het dichtstbijzijnde ordermeervoud. (In het geval van foutieve instellingen kan dit het maximale orderaantal overschrijden.)  

## <a name="order-tracking-links-during-planning"></a>Ordertraceringskoppelingen tijdens een planning  
Voor wat betreft ordertracering tijdens planning is het belangrijk te vermelden dat het planningssysteem de dynamisch gemaakte ordertraceringskoppelingen herschikt voor de combinaties van artikel/variant/vestiging.  

Hiervoor zijn twee redenen:  

-   Het planningssysteem moet de voorstellen kunnen rechtvaardigen: dat alle vraag is verwerkt en dat er geen overbodige voorzieningenorders zijn.  
-   Dynamisch gemaakte ordertraceringskoppelingen moeten regelmatig worden afgestemd.  

Na verloop van tijd raken dynamische ordertraceringskoppelingen in onbalans aangezien het hele ordertraceringsnetwerk pas wordt herschikt als een vraag- of aanbodgebeurtenis werkelijk wordt afgesloten.  

Voordat voorzieningen op vraag in overeenstemming worden gebracht, worden alle bestaande ordertraceringskoppelingen verwijderd. Vervolgens wordt tijdens de vereffeningsprocedure, wanneer een vraag- of voorzieningsgebeurtenis wordt afgesloten, de nieuwe ordertraceringskoppelingen tot stand gebracht tussen vraag en voorziening.  

> [!NOTE]  
>  Zelfs als het artikel niet is ingesteld voor dynamische ordertracering, maakt het planningssysteem afgestemde ordertraceringskoppelingen, zoals hierboven uitgelegd.  

## <a name="see-also"></a>Zie ook  
[Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md)   
[Ontwerpdetails: Centrale begrippen van het planningssysteem](design-details-central-concepts-of-the-planning-system.md)   
[Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)
