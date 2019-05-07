---
title: 'Ontwerpdetails: Bestelbeleid | Microsoft Docs'
description: In dit onderwerp wordt een overzicht van het beleid voor artikelaanvulling gegeven.
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
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 1212c6f2f7e9da03a15c7fb39496d85869ef3e73
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "912324"
---
# <a name="design-details-reordering-policies"></a>Ontwerpdetails: Bestelbeleid
Met het bestelbeleid wordt bepaald hoeveel wordt besteld wanneer het artikel moet worden aangevuld. Er zijn vier verschillende soorten bestelbeleid.  

## <a name="fixed-reorder-qty"></a>Vast bestelaantal
Het beleid Vast bestelaantal is gerelateerd aan de voorraadplanning van typische C-producten (lage voorraadkosten, laag verouderingsrisico en/of veel artikelen). Dit beleid wordt gewoonlijk gebruikt in relatie met een bestelpunt met de verwachte vraag tijdens de doorlooptijd van het artikel.  

### <a name="calculated-per-time-bucket"></a>Berekend per tijdsinterval  
 Als het planningssysteem ontdekt dat het bestelpunt in een bepaald tijdsinterval (bestelfrequentie) is bereikt of overschreden - boven of op het bestelpunt aan het begin van de periode en onder of op het bestelpunt aan het einde van de periode - wordt voorgesteld een nieuwe voorzieningenorder voor het opgegeven bestelaantal te maken en deze voorwaarts te plannen vanaf de eerste datum na het einde van het tijdsinterval.  

 Door bestelpunten in combinatie met tijdsintervallen te gebruiken, wordt het aantal voorzieningsvoorstellen verminderd. Dit geeft een handmatig proces aan van het frequent door het magazijn lopen om de werkelijke inhoud in de verschillende opslaglocaties te controleren.  

### <a name="creates-only-necessary-supply"></a>Maakt alleen benodigde voorzieningen  
 Voordat een nieuwe voorzieningenorder wordt voorgesteld om aan een bestelpunt te voldoen, controleert het planningssysteem of al voorziening is besteld voor ontvangst binnen de doorlooptijd van het artikel. Als een bestaande voorzieningenorder het probleem oplost door de geplande voorraad binnen de looptijd op of boven het bestelpunt te brengen, stelt het systeem geen nieuwe voorzieningenorder voor.  

 Orders voor voorzieningen die specifiek zijn gemaakt om te voldoen aan een bestelpunt, worden uitgesloten van de normale afstemming van voorzieningen en kunnen op geen enkele manier achteraf worden gewijzigd. Dus als een artikel dat het bestelpunt gebruikt, moet worden uitgefaseerd (niet aangevuld), is het raadzaam openstaande orders voor voorzieningen handmatig te controleren of het bestelbeleid te wijzigen in lot-voor-lot, waarbij het systeem overbodige voorzieningen reduceert of annuleert.  

### <a name="combines-with-order-modifiers"></a>Combineert met orderaanpassingsfuncties  
 De ordervelden Min. bestelaantal, Max. bestelaantal en Vaste lotgrootte zouden geen grote rol moeten afspelen wanneer het beleid voor vaste bestelaantallen wordt gebruikt. Het planningssysteem houdt echter toch rekening met deze wijzigingsfactoren en verlaagt het aantal tot het opgegeven maximum orderaantal (en maakt twee of meer voorzieningen om het totale orderaantal te bereiken), verhoogt de order tot het opgegeven maximum aantal of rondt het orderaantal af op een opgegeven orderveelvoud.  

### <a name="combines-with-calendars"></a>Combineert met agenda's  
 Voordat het planningssysteem een nieuwe voorzieningenorder voorstelt, wordt gecontroleerd of de order is gepland voor een niet-werkdag, volgens agenda's die zijn gedefinieerd in het veld **Basisagendacode** op de pagina's **Bedrijfsgegevens** en **Vestiging**.  

 Als de verwachte datum een vrije dag is, verplaatst het planningssysteem de order voorwaarts naar de dichtstbijzijnde werkdatum. Dit kan resulteren in een order die voldoet een bestelpunt maar aan een bepaalde vraag niet voldoet. Voor dergelijke vraag in onbalans maakt het systeem een extra voorziening.  

### <a name="should-not-be-used-with-forecast"></a>Moet niet worden gebruikt met prognose  
 Omdat de verwachte vraag al is uitgedrukt in het bestelpuntniveau, is het niet nodig een prognose in de planning van een artikel op te nemen met behulp van een bestelpunt. Als het belangrijk is dat de planning op een prognose wordt gebaseerd, gebruikt u het lot-voor-lot beleid.  

### <a name="must-not-be-used-with-reservations"></a>Mag niet met reserveringen worden gebruikt  
 Als de gebruiker een aantal heeft gereserveerd, bijvoorbeeld een aantal in voorraad, voor een of andere toekomstige vraag, wordt de basis van de planning verstoord. Zelfs als de geplande voorraad met betrekking tot het bestelpunt aanvaardbaar is, zijn de hoeveelheden mogelijk niet beschikbaar. Het systeem probeert dit mogelijk te compenseren door uitzonderingsorders aan te maken. Het wordt echter aangeraden het veld Reserveren in te stellen op Nooit voor artikelen die worden gepland met behulp van een bestelpunt.

## <a name="maximum-qty"></a>Maximum aantal
Het beleid Maximum aantal is een manier om voorraad bij te houden met behulp van een bestelpunt.  

Alles over het beleid voor een vast bestelaantal geldt ook voor dit beleid. Het enige verschil is de hoeveelheid van de voorgestelde voorziening. Wanneer het beleid voor maximaal aantal wordt gebruikt, wordt het bestelaantal dynamisch bepaald op basis van het geplande voorraadniveau en verschilt daarom gewoonlijk per order.  

### <a name="calculated-per-time-bucket"></a>Berekend per tijdsinterval  
Het bestelaantal wordt bepaald op het moment (het einde van het tijdsinterval) dat het planningssysteem detecteert dat het bestelpunt is overschreden. Op dit moment meet het systeem het verschil tussen het huidige geplande voorraadniveau en de opgegeven maximale voorraad. Dit vormt het aantal dat opnieuw moet worden besteld. Het systeem controleert vervolgens of de voorziening al elders is besteld voor ontvangst binnen de doorlooptijd. Als dit het geval is, wordt het aantal van de nieuwe voorzieningenorder verminderd met de reeds bestelde aantallen.  

Het systeem zorgt dat de geplande voorraad ten minste het bestelpuntniveau bereikt, voor het geval dat de gebruiker is vergeten een maximaal voorraadaantal op te geven.  

### <a name="combines-with-order-modifiers"></a>Combineert met orderaanpassingsfuncties  
Afhankelijk van de instellingen kan het het beste zijn om het maximale aantal-beleid te combineren met orderwijzigingen om een minimaal orderaantal te garanderen of af te ronden op een geheel aantal inkoopeenheden, of te splitsen in meerdere lots zoals bepaald door het maximale orderaantal.  

### <a name="combines-with-calendars"></a>Combineert met agenda's  
Voordat het planningssysteem een nieuwe voorzieningenorder voorstelt, wordt gecontroleerd of de order is gepland voor een niet-werkdag, volgens agenda's die zijn gedefinieerd in het veld **Basisagendacode** op de pagina's **Bedrijfsgegevens** en **Vestiging**.  

Als de verwachte datum een vrije dag is, verplaatst het planningssysteem de order voorwaarts naar de dichtstbijzijnde werkdatum. Dit kan resulteren in een order die voldoet een bestelpunt maar aan een bepaalde vraag niet voldoet. Voor dergelijke vraag in onbalans maakt het systeem een extra voorziening.

## <a name="order"></a>Volgorde
In een op-order-produceren omgeving wordt een artikel ingekocht of geproduceerd om uitsluitend aan een specifieke vraag te voldoen. Meestal heeft dit betrekking op A-producten en de motivatie om het bestelbeleid Order te kiezen, kan zijn dat de vraag niet frequent is, dat de doorlooptijd onbeduidend is of dat de vereiste kenmerken verschillen.  

Het programma maakt een order-naar-order-koppeling die fungeert als voorlopige verbinding tussen de voorziening, een voorzieningenorder of voorraad, en de vraag waaraan het zal voldoen.  

Afgezien van het gebruik van het bestelbeleid kan de order-aan-order koppeling tijdens planning op de volgende manieren worden toegepast:  

* Wanneer het productiebeleid Op order produceren wordt gebruikt om productieorders met meerdere niveaus of projecttype te maken (waarbij benodigde onderdelen op dezelfde productieorder worden geproduceerd).  
* Wanneer de functie Verkooporderplanning wordt gebruikt om een productieorder te maken van een verkooporder.  

Zelfs als een productiebedrijf zichzelf beschouwt als een op-order-produceren omgeving, kan het het best zijn een lot-voor-lot bestelbeleid te gebruiken als de artikelen standaard zijn, zonder variatie in kenmerken. Hierdoor gebruikt het systeem niet-geplande voorraad en worden verkooporders alleen gecumuleerd met dezelfde verzenddatum of binnen een bepaalde periode.  

### <a name="order-to-order-links-and-past-due-dates"></a>Order-naar-order koppelingen en overschreden vervaldatums  
In tegenstelling tot de meeste combinaties van voorziening en vraag, worden gekoppelde orders met vervaldatums voor de begindatum van de planning, volledig door het systeem gepland. De bedrijfsreden voor deze uitzondering is dat specifieke vraag-voorzieningcombinaties moeten worden gesynchroniseerd tot aan uitvoering. Zie voor meer informatie over de bevroren zone die de meeste vraag/voorziening toepast [Ontwerpdetails: Werken met orders voor de geplande begindatum](design-details-dealing-with-orders-before-the-planning-starting-date.md).

## <a name="lot-for-lot"></a>Lot-for-Lot
Het lot-for-lot-beleid is het meest flexibel omdat het systeem alleen reageert op werkelijke vraag, én rekening houdt met verwachte vraag uit prognoses en raamcontracten en vervolgens het orderaantal op basis van de vraag vereffent. Het lot-for-lot-beleid is bedoeld voor A- en B-artikelen waar voorraad kan worden geaccepteerd maar vermeden moet worden.  

In sommige opzichten lijkt het lot-voor-lot beleid op het orderbeleid, maar het hanteert een algemene aanpak van artikelen; het kan aantallen in voorraad accepteren en het bundelt vraag en corresponderend aanbod in tijdsintervallen die door de gebruiker worden gedefinieerd.  

Het tijdsinterval wordt gedefinieerd in het veld **Tijdsinterval**. Er wordt gewerkt met een minimumtijdsinterval van één dag, aangezien dit de kleinste tijdseenheid voor vraag- en voorzieningsgebeurtenissen in het systeem is (hoewel in de praktijk de tijdseenheid voor productieorders en materiaalbehoeften zelfs seconden kan zijn).  

Met het tijdsinterval worden ook limieten ingesteld wanneer een bestaande voorzieningenorder opnieuw moet worden gepland om te voldoen aan een bepaalde vraag. Als het aanbod binnen het tijdsinterval ligt, wordt het opnieuw in of uit gepland om aan de vraag te voldoen. Als de voorziening eerder ligt, ontstaat onnodige opeenhoping van voorraad en moet worden geannuleerd. Als het later ligt, wordt in plaats daarvan een nieuwe order gemaakt.  

Met dit beleid is het ook mogelijk om een veiligheidsvoorraad te definiëren om mogelijke schommelingen in voorzieningen op te vangen of te voldoen aan plotselinge vraag.  

Omdat het aantal van de voorzieningenorder op de werkelijke vraag is gebaseerd, kan het zinnig zijn de orderwijzigingen te gebruiken: rond het orderaantal naar boven af om aan een opgegeven orderveelvoud (of inkoopeenheid) te voldoen, vergroot de order tot een opgegeven minimaal orderaantal of verlaag het aantal tot het opgegeven maximale aantal (en maak zo twee of meer voorzieningen om het totaal benodigde aantal te bereiken).

## <a name="see-also"></a>Zie ook  
[Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md)   
[Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md)   
[Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)
