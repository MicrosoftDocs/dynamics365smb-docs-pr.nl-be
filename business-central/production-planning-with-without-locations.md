---
title: Planning met of zonder vestigingen
description: In dit onderwerp leert u over productie en fabricage, inclusief leveringsplanning, in Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/16/2021
ms.author: edupont
ms.openlocfilehash: fa1b63bb94152c130077907dbe2d4e0d08281f40
ms.sourcegitcommit: acc1871afa889cb699e65b1b318028c05f8e6444
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/16/2021
ms.locfileid: "6636003"
---
# <a name="planning-with-or-without-locations"></a>Planning met of zonder vestigingen
Ten aanzien van de planning met of zonder vestigingscodes op vraagregels, werkt het planningssysteem eenvoudig en duidelijk wanneer:  

-   vraagregels altijd vestigingscodes bevatten en het systeem SKU's gebruikt, inclusief de relevante vestigingsinstellingen.  
-   vraagregels nooit vestigingscodes bevatten en het systeem geen SKU's of andere vestigingsinstellingen gebruikt (zie het laatste scenario hieronder).  

Als vraagregels echter de ene keer wel vestigingscodes bevatten en de andere keer niet, volgt het planningssysteem bepaalde regels, afhankelijk van de instellingen.  

> [!TIP]
> Als u vaak voor vraag bij verschillende vestigingen moet plannen, wordt de functie voor SKU's aanbevolen.

## <a name="demand-at-location"></a>Vraag op vestiging  

Wanneer het planningssysteem ontdekt dat er op een bepaalde vestiging vraag is (een regel met een vestigingscode), reageert het systeem op verschillende manieren, afhankelijk van drie essentiële instellingen.  

Tijdens de uitvoering van een planning controleert het systeem een voor een de waarden van de drie instellingen en plant aan de hand van die waarden:  

1. Staat er een vinkje in het veld **Vestiging verplicht** op de pagina **Voorraadinstellingen**?  

    Als dit het geval is dan:  

2. Bestaat de SKU voor het artikel?  

    Als dit het geval is dan:  

    Het artikel is gepland aan de hand van de planningsparameters op de SKU-kaart.  

    Als dit niet het geval is dan:  

3. Bevat het veld **Onderdelen op vestiging** op de pagina **Productie-instellingen** de gevraagde vestgingscode?  

    Als dit het geval is dan:  

    Het artikel is gepland aan de hand van de planningsparameters op de artikelkaart.  

    Als dit niet het geval is dan:  

    Het artikel is gepland aan de hand van: Bestelbeleid =  *Lot-for-Lot*, Inclusief voorraad =  *Ja*, alle andere planningsparameters = Leeg. (Artikelen die gebruikmaken van het bestelbeleid  *Order* blijven zowel  *Order* als de andere instellingen gebruiken.)  

> [!NOTE]  
> Dit minimale alternatief dekt alleen de exacte vraag. Alle gedefinieerde planningsparameters worden genegeerd.  

Zie de variaties in de onderstaande scenario's.  

> [!TIP]
> Het veld **Vestiging verplicht** op de pagina **Voorraadinstellingen** en het veld **Onderdelen op vestiging** op de pagina Productie-instellingen zijn erg belangrijk om te bepalen hoe het planningssysteem vraagregels met/zonder vestigingscodes verwerkt.
>
> Voor productievraag die wordt aangeschaft (wanneer de planningsengine alleen wordt gebruikt voor inkoopplanning en niet voor productieplanning), gebruikt [!INCLUDE [prod_short](includes/prod_short.md)] voor onderdelen de vestiging die is opgegeven op de productieorder. Door dit veld in te vullen kunt u echter de onderdelen naar een andere vestiging leiden.
>
> U kunt dit ook voor een specifieke SKU definiëren door de code van een andere vestiging in het veld **Onderdelen op vestiging** op de SKU-kaart te selecteren. Let echter op dat dit nauwelijks zinvol is aangezien de planningslogica vervormd kan zijn wanneer u plant voor de SKU-component.

Een ander belangrijk veld is het veld **Max. bestelaantal** op de **artikel** kaart. Het specificeert een maximaal toegestane hoeveelheid voor een artikelordervoorstel en wordt gebruikt als het artikel wordt geleverd in een vaste transporteenheid, zoals een container, die u bijvoorbeeld volledig wilt benutten. Als het programma de noodzaak voor aanvulling heeft vastgesteld en de lotgrootte heeft aangepast volgens het opgegeven bestelbeleid, wordt het aantal, indien nodig, verlaagd om te voldoen aan het maximale bestelaantal dat u voor het artikel definieert. Bij eventuele aanvullende behoeften worden er nieuwe orders berekend om eraan te voldoen. Dit veld wordt meestal gebruikt met een productiebeleid voor op voorraad produceren.  

## <a name="demand-at-blank-location"></a>Vraag op 'lege vestiging'  
Zelfs als het selectievakje **Vestiging verplicht** ingeschakeld is, kan het systeem vraagregels zonder een vestigingscode maken, ook wel *LEGE* vestigingen genoemd. Dit is een afwijking voor het systeem omdat verschillende instellingswaarden zijn afgestemd op gebruik van vestigingen (zie boven). De planningsengine maakt hierdoor geen planningsregel voor een dergelijke vraagregel. Als het veld **Vestiging verplicht** niet ingeschakeld is, maar een van de instellingswaarden voor vestigingen bestaat, wordt er ook uitgegaan van een afwijking en reageert het planningssysteem met het 'minimale alternatief' als uitvoer:   
Het artikel wordt gepland volgens: Bestelbeleid =  *Lot-for-Lot* ( *Order* blijft *Order)*, Inclusief voorraad =  *Ja*, alle andere planningsparameters = Leeg.  

Zie de variaties in de onderstaande configuratiescenario's.  

### <a name="setup-1"></a>Instelling 1:  

-   Vestiging verplicht = *Ja*  
-   SKU is ingesteld voor  *ROOD*  
-   Onderdeel op vestiging =  *BLAUW*  

#### <a name="case-11-demand-is-at--red-location"></a>Case 1.1: vraag is op  *RODE* vestiging  

Het artikel is gepland volgens planningsparameters op de SKU-kaart (inclusief mogelijke transfer).  

#### <a name="case-12-demand-is-at--blue-location"></a>Case 1.2: vraag is op *BLAUWE* vestiging  

Het artikel is gepland aan de hand van de planningsparameters op de artikelkaart.  

#### <a name="case-13-demand-is-at--green-location"></a>Case 1.3: vraag is op  *GROENE* vestiging  

Het artikel is gepland volgens: Bestelbeleid =  *Lot-for-Lot* ( *Order* blijft  *Order*), Inclusief voorraad =  *Ja*, alle andere planningsparameters = Leeg.  

#### <a name="case-14-demand-is-at--blank-location"></a>Case 1.4: vraag is op *LEGE* vestiging  

Het artikel is niet gepland omdat er geen vestiging is gedefinieerd op de vraagregel.  

### <a name="setup-2"></a>Instelling 2:  

-   Vestiging verplicht = *Ja*  
-   Er bestaat geen SKU  
-   Onderdeel op vestiging =  *BLAUW*  

#### <a name="case-21-demand-is-at--red-location"></a>Case 2.1: vraag is op  *RODE* vestiging  

Het artikel is gepland volgens: Bestelbeleid =  *Lot-for-Lot* ( *Order* blijft  *Order*), Inclusief voorraad =  *Ja*, alle andere planningsparameters = Leeg.  

#### <a name="case-22-demand-is-at--blue-location"></a>Case 2.2: vraag is op *BLAUWE* vestiging  

Het artikel is gepland aan de hand van de planningsparameters op de artikelkaart.  

### <a name="setup-3"></a>Instelling 3:  

-   Vestiging verplicht = *Nee*  
-   Er bestaat geen SKU  
-   Onderdeel op vestiging =  *BLAUW*  

#### <a name="case-31-demand-is-at--red-location"></a>Case 3.1: vraag is op  *RODE* vestiging  

Het artikel is gepland volgens: Bestelbeleid =  *Lot-for-Lot* ( *Order* blijft  *Order*), Inclusief voorraad =  *Ja*, alle andere planningsparameters = Leeg.  

#### <a name="case-32-demand-is-at--blue-location"></a>Case 3.2: vraag is op *BLAUWE* vestiging  

Het artikel is gepland aan de hand van de planningsparameters op de artikelkaart.  

#### <a name="case-33-demand-is-at--blank-location"></a>Case 3.3: Vraag is op  *LEGE* vestiging  

Het artikel is gepland volgens: Bestelbeleid =  *Lot-for-Lot* ( *Order* blijft  *Order*), Inclusief voorraad =  *Ja*, alle andere planningsparameters = Leeg.  

### <a name="setup-4"></a>Instelling 4:  

-   Vestiging verplicht = *Nee*  
-   Er bestaat geen SKU  
-   Onderdeel op vestiging =  *LEEG*  

#### <a name="case-41-demand-is-at--blue-location"></a>Case 4.1: vraag is op  *BLAUWE* vestiging  

Het artikel is gepland volgens: Bestelbeleid =  *Lot-for-Lot* ( *Order* blijft  *Order*), Inclusief voorraad =  *Ja*, alle andere planningsparameters = Leeg.  

#### <a name="case-42-demand-is-at--blank-location"></a>Case 4.2: Vraag is op  *LEGE* vestiging  

Het artikel is gepland aan de hand van de planningsparameters op de artikelkaart.  

Zoals u in het laatste scenario kunt zien, kunt u alleen een correct resultaat krijgen voor een vraagregel zonder vestigingscode door alle instellingswaarden uit te schakelen die naar vestigingen verwijzen. Zo krijgt u ook alleen stabiele planningsresultaten voor vraag op vestigingen als u SKU's gebruikt.  

Als u vaak vraag op vestigingen plant, raden we daarom aan dat u de SKU-functionaliteit gebruikt.  

## <a name="see-also"></a>Zie ook

[Gepland](production-planning.md)  
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)  
[Voorraad](inventory-manage-inventory.md)  
[SKU's instellen](inventory-how-to-set-up-stockkeeping-units.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)  
[Aanbevolen procedures instellen: voorraadplanning](setup-best-practices-supply-planning.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]