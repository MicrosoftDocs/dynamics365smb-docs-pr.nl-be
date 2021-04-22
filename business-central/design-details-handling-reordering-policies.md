---
title: 'Ontwerpdetails: Bestelbeleid verwerken | Microsoft Docs'
description: Overzicht van taken voor het definiëren van een bestelbeleid in voorraadplanning.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5dc916bcba012476e9365c8d5c8e97d413b4cdd5
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784629"
---
# <a name="design-details-handling-reordering-policies"></a>Ontwerpdetails: Bestelbeleid verwerken
Om een artikel deel te laten nemen aan voorraadplanning, moet een bestelbeleid worden gedefinieerd. Er zijn vier soorten bestelbeleid:  

* Vast bestelaantal  
* Maximum aantal  
* Order  
* Lot-for-Lot  

Beleid voor vast bestelaantal en maximum aantal heeft betrekking op voorraadplanning. Hoewel voorraadplanning technisch eenvoudiger is dan de vereffeningsprocedure, moet dit beleid naast elkaar bestaan met stapsgewijze vereffening van voorziening en ordertracering. Er gelden strikte regels voor de verwerking van het bestelbeleid om de integratie tussen deze twee te beheren en om zichtbaarheid te bieden in de betrokken planningslogica.  

## <a name="the-role-of-the-reorder-point"></a>De rol van het bestelpunt
Naast de algemene afstemming van vraag en aanbod, moet het planningssysteem ook voorraadniveaus voor de betrokken artikelen controleren om rekening te houden met gedefinieerd bestelbeleid.  

Een bestelpunt vertegenwoordigt vraag tijdens doorlooptijd. Wanneer de geplande voorraad onder het voorraadniveau komt dat door het bestelpunt is gedefinieerd, is het tijd om het bestelaantal te verhogen. Ondertussen wordt verwacht dat de voorraad afneemt en mogelijk nul wordt (of het veiligheidsvoorraadniveau bereikt), totdat de aanvulling plaatsvindt.  

Het planningssysteem zal een voorwaarts geplande voorzieningenorder voorstellen op het moment dat de verwachte voorraad onder het bestelpunt komt.  

Het bestelpunt geeft een bepaald voorraadniveau aan. Voorraadniveaus kunnen tijdens het tijdsinterval echter aanzienlijk schommelen en daarom moet het planningssysteem constant de geplande beschikbare voorraad controleren.

## <a name="monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Het verwachte voorraadniveau en het bestelpunt controleren
Voorraad is een soort aanbod, maar voor voorraadplanning maakt het planningssysteem onderscheid tussen twee voorraadniveaus:  

* Geplande voorraad  
* Geplande beschikbare voorraad  

### <a name="projected-inventory"></a>Geschatte inventaris  
In eerste instantie is verwachte voorraad het aantal van de brutovoorraad, inclusief aanbod en vraag in het verleden, ook indien niet geboekt, wanneer het planningsproces wordt gestart. In de toekomst wordt dit een schommelend gepland voorraadniveau dat wordt onderhouden door bruto aantallen van toekomstige vraag en aanbod omdat deze worden geïntroduceerd op het tijdpad (gereserveerd of op een andere manier toegewezen).  

De geplande voorraad wordt gebruikt door het planningssysteem om het bestelpunt te controleren en het bestelaantal te bepalen wanneer het bestelbeleid Maximum aantal wordt gebruikt.  

### <a name="projected-available-inventory"></a>Geplande beschikbare voorraad  
De geplande beschikbare voorraad is het deel van de geplande voorraad dat op een bepaald moment beschikbaar is om aan de vraag te voldoen. De geplande beschikbare voorraad wordt gebruikt door de planningsengine voor het controleren van de veiligheidsvoorraad.  

De geplande beschikbare voorraad wordt gebruikt door het planningssysteem om de veiligheidsvoorraad te controleren, aangezien de veiligheidsvoorraad altijd beschikbaar moet zijn om te voldoen aan onverwachte vraag.  

### <a name="time-buckets"></a>Tijdsintervallen  
Een strakke controle over de verwachte voorraad hebben, is van cruciaal belang om te detecteren wanneer het bestelpunt wordt bereikt of overschreden en om het juiste orderaantal te berekenen wanneer het bestelbeleid Maximum aantal wordt gebruikt.  

Zoals eerder gezegd, wordt het verwachte voorraadniveau berekend aan het begin van de planningsperiode. Het een brutoniveau is dat geen rekening houdt met reserveringen en soortgelijke toewijzingen. Om dit voorraadniveau te controleren tijdens de planningsreeks, controleert het systeem de samengevoegde wijzigingen gedurende een periode, een tijdsinterval. Het systeem zorgt dat het tijdsinterval ten minste één dag is, aangezien dit de nauwkeurigste tijdseenheid is voor een vraag- of voorzieningsgebeurtenis.  

### <a name="determining-the-projected-inventory-level"></a>Het verwachte voorraadniveau bepalen  
In de volgende reeks wordt beschreven hoe het voorspelde voorraadniveau wordt bepaald:  

* Wanneer een voorzieningsgebeurtenis, zoals een inkooporder, totaal is gepland, wordt hiermee de geplande voorraad verhoogd op de vervaldatum.  
* Wanneer aan een vraaggebeurtenis volledig is voldaan, wordt de geplande voorraad niet direct verminderd. In plaats hiervan wordt een afnameaanmaning geboekt. Dat is een interne record die de datum en het aantal bevat van de bijdrage aan de verwachte voorraad.  
* Wanneer een volgende voorzieningsgebeurtenis wordt gepland en op het tijdpad wordt geplaatst, worden de geboekte afnameaanmaningen een voor een onderzocht tot aan de geplande datum van de voorziening tijdens het bijwerken van de geplande voorraad. Tijdens dit proces kan het bestelpuntniveau van de interne toenameherinnering worden bereikt of overschreden.  
* Als een nieuwe voorzieningenorder wordt geïntroduceerd, controleert het systeem of het vóór de huidige voorziening wordt ingevoerd. Als dat zo is, wordt de nieuwe voorziening de huidige voorziening en begint de vereffeningsprocedure opnieuw.  

Hierna wordt een grafische illustratie van dit principe getoond:  

![Het verwachte voorraadniveau bepalen](media/nav_app_supply_planning_2_projected_inventory.png "Het verwachte voorraadniveau bepalen")  

1. Voorziening **Sa** van 4 (vast) sluit vraag **Da** van -3 af.  
2. CloseDemand: Maak een afnameaanmaning van -3 (niet weergegeven).  
3. Voorziening **Sa** is afgesloten met een overschot van 1 (er bestaat geen vraag meer).  

     Hiermee wordt het geplande voorraadniveau verhoogd naar +4, terwijl de geplande **beschikbare** voorraad -1 wordt.  

4. De volgende voorziening **Sb** van 2 (een andere order) is al ingesteld op de tijdlijn.  
5. Er wordt gecontroleerd of er afnameaanmaningen zijn voorafgaand aan **Sb** (die zijn er niet, dus er wordt geen actie ondernomen.)  
6. Het systeem sluit voorziening **Sb** (er bestaat geen vraag meer) door A: het te verlagen tot 0 (annuleren), of B: het te laten zoals het is.  

     Hiermee wordt het voorspelde voorraadniveau verhoogd (A: +0 => +4 of B: +2 = +6).  

7. Er wordt een laatste controle gedaan: zijn er eventuele afnameaanmaningen? Ja, er is één op de datum van **Da**.  
8. Het systeem voegt de afnameherinnering -3 toe aan het verwachte voorraadniveau, hetzij A: +4 -3 = 1 of B: +6 -3 = +3.  
9. In het geval van A maakt het systeem een voorwaarts geplande order die begint op de datum **Da**.  

     In het geval van B, wordt het bestelpunt bereikt en wordt een nieuwe order gemaakt.

## <a name="the-role-of-the-time-bucket"></a>De rol van het tijdsinterval
Het doel van het tijdsinterval is vraaggebeurtenissen binnen het tijdskader te verzamelen om een gezamenlijke voorzieningenorder te maken.  

Voor bestelbeleid dat een bestelpunt gebruikt, kunt u een tijdsinterval opgeven. Dit zorgt ervoor dat de vraag in dezelfde periode wordt opgeteld voordat wordt gecontroleerd wat het effect op de geplande voorraad is en of het bestelpunt is verstreken. Als het bestelpunt is overschreden, wordt een nieuwe voorzieningenorder voorwaarts gepland vanaf het einde van de periode die wordt gedefinieerd door het tijdsinterval. De tijdsintervallen beginnen op de begindatum van de planning.  

Het tijdsinterval geeft het handmatige proces aan om het voorraadniveau op frequente basis te controleren in plaats van voor elke transactie. De gebruiker moet de frequentie (het tijdsinterval) definiëren. De gebruiker verzamelt bijvoorbeeld alle artikelbehoeften van één leverancier om een wekelijkse order te plaatsen.  

![Voorbeeld van tijdsinterval in planning](media/nav_app_supply_planning_2_reorder_cycle.png "Voorbeeld van tijdsinterval in planning")  

Het tijdsinterval wordt doorgaans gebruikt om een watervaleffect te voorkomen. Een vereffende rij van vraag en aanbod waarbij bijvoorbeeld een vroege vraag wordt geannuleerd of een nieuwe wordt gemaakt. Het resultaat is dat elke voorzieningenorder (behalve de laatste) opnieuw wordt gepland.

## <a name="staying-under-the-overflow-level"></a>Onder het overflowniveau blijven
Wanneer de beleidsopties Maximum aantal en Vast bestelaantal worden gebruikt, richt het planningssysteem zich alleen op de geplande voorraad in het betreffende tijdsinterval. Dit betekent dat het planningssysteem overbodige voorziening kan voorstellen wanneer negatieve vraag- of positieve voorzieningswijzigingen buiten het betreffende tijdsinterval plaatsvinden. Als om deze reden een overbodige voorziening wordt voorgesteld, berekent het planningssysteem tot welk aantal de voorziening moet worden teruggebracht (of verwijderd) om de overbodige voorziening te voorkomen. Dit aantal wordt het overflowniveau genoemd. De overflow wordt gecommuniceerd als een planningsregel met een actie **Aantal wijzigen (afname)** of **Annuleren** en het volgende waarschuwingsbericht:  

*Let op: De geplande voorraad [xx] is groter dan het overflowniveau [xx] op de Vervaldatum [xx].*  

![Overflowniveau van voorraad](media/supplyplanning_2_overflow1_new.png "Overflowniveau van voorraad")  

###  <a name="calculating-the-overflow-level"></a>Het overflowniveau berekenen  
Het overflowniveau wordt op verschillende manieren berekend, afhankelijk van de planningsinstelling.  

#### <a name="maximum-qty-reordering-policy"></a>Bestelbeleid Maximum aantal  
Overflowniveau = Maximale voorraad  

> [!NOTE]  
>  Als een minimaal orderaantal bestaat, wordt het als volgt toegevoegd: overflowniveau = maximale voorraad + minimaal orderaantal.  

#### <a name="fixed-reorder-qty-reordering-policy"></a>Bestelbeleid voor vast bestelaantal  
Overflowniveau = Bestelaantal + bestelpunt  

> [!NOTE]  
>  Als het minimale bestelaantal hoger is dan het bestelpunt, wordt dit als volgt vervangen: overflowniveau = bestelaantal + minimum bestelaantal.  

#### <a name="order-multiple"></a>Vaste lotgrootte  
Als een vaste lotgrootte bestaat, wordt het overflowniveau voor zowel het bestelbeleid Maximum aantal als Vast bestelaantal aangepast.  

###  <a name="creating-the-planning-line-with-overflow-warning"></a>De planningsregel met overflowwaarschuwing maken  
Als door een bestaande voorraad de geplande voorziening groter is dan het overflowniveau aan het einde van het tijdsinterval, wordt een planningsregel gemaakt. Om te waarschuwen voor de mogelijke overbodige voorziening, bevat de planningsregel een waarschuwing, is het veld **Planningsboodschap accepteren** niet geselecteerd en is de planningsboodschap Annuleren of Aantal wijzigen.  

#### <a name="calculating-the-planning-line-quantity"></a>Het planningsregelaantal berekenen  
Planningsregelaantal = Voorzieningaantal - (Geplande voorraad - Overflowniveau)  

> [!NOTE]  
>  Net als alle waarschuwingsregels worden eventuele maximale/minimale orderaantallen of vaste ordergrootte genegeerd.  

#### <a name="defining-the-action-message-type"></a>De soort planningsboodschap definiëren  

-   Als het planningsregelaantal groter is dan 0, is de planningsboodschap Aantal wijzigen.  
-   Als het planningsregelaantal gelijk is aan of kleiner is dan 0, is de planningsboodschap Annuleren  

#### <a name="composing-the-warning-message"></a>Het waarschuwingsbericht opstellen  
In het geval van overflow wordt op de pagina **Niet-getraceerde planningselementen** een waarschuwing weergegeven met de volgende informatie:  

-   Het geplande voorraadniveau dat de waarschuwing heeft geactiveerd  
-   Het berekenende overflowniveau  
-   De vervaldatum van de voorzieningsgebeurtenis.  

Voorbeeld: “De verwachte voorraad 120 is hoger dan het overflowniveau 60 op 28-01-11“  

### <a name="scenario"></a>Scenario  
In dit scenario verandert een klant een verkooporder van 70 in 40 stuks tussen twee planningen. De overflowfunctie wordt geactiveerd om de inkoop te beperken die werd voorgesteld voor het oorspronkelijke verkoopaantal.  

#### <a name="item-setup"></a>Artikelinstellingen  

|Bestelbeleid|Maximum aantal|  
|-----------------------|------------------|  
|Max. bestelaantal|100|  
|Bestelpunt|50|  
|Voorraad|80|  

#### <a name="situation-before-sales-decrease"></a>Situatie voor verkoopafname  

|Gebeurtenis|Aantal wijzigen|Geschatte inventaris|  
|-----------|-----------------|-------------------------|  
|Dag één|Geen|80|  
|Verkoop|-70|10|  
|Einde van periode|Geen|10|  
|Nieuwe inkooporder voorstellen|+90|100|  

#### <a name="situation-after-sales-ddecrease"></a>Situatie na verkoopafname  

|Wijziging|Aantal wijzigen|Geschatte inventaris|  
|------------|-----------------|-------------------------|  
|Dag één|Geen|80|  
|Verkoop|-40|40|  
|Inkoop|+90|130|  
|Einde van periode|Geen|130|  
|Voorstellen om inkoop te verminderen<br /><br /> van 90 naar 60|-30|100|  

#### <a name="resulting-planning-lines"></a>Resulterende planningsregels  
 Er wordt één planningsregel (waarschuwing) gemaakt om de inkoop met 30 te reduceren, van 90 tot 60, om de geplande voorraad op 100 te houden, op basis van het overflowniveau.  

![Plannen volgens overloopniveau](media/nav_app_supply_planning_2_overflow2.png "Plannen volgens overloopniveau")  

> [!NOTE]  
>  Zonder de overflowfunctie wordt er geen waarschuwing gemaakt als het geplande voorraadniveau boven de maximale voorraad is. Dit kan een overbodige voorziening van 30 genereren.

## <a name="handling-projected-negative-inventory"></a>Voorspelde negatieve voorraad afhandelen
Het bestelpunt drukt de verwachte vraag uit tijdens de doorlooptijd van het artikel. Wanneer het bestelpunt is verstreken, is het tijd om meer te bestellen. Maar de geplande voorraad moet groot genoeg zijn om de vraag te dekken totdat de nieuwe order wordt ontvangen. In de tussentijd moet de veiligheidsvoorraad zorgen voor schommelingen in de vraag tot aan een bepaald serviceniveau.  

 Dus beschouwt het planningssysteem het als een noodgeval als aan toekomstige vraag niet kan worden voldaan vanuit de voorspelde voorraad, of anders uitgedrukt, als de voorspelde voorraad negatief wordt. Het systeem verwerkt dergelijke uitzonderingen door een nieuwe voorzieningenorder voor te stellen om te voldoen aan het deel van de vraag waaraan de voorraad of andere voorzieningen niet kunnen voldoen. Voor de ordergrootte van de nieuwe voorzieningenorder wordt geen rekening gehouden met de maximale voorraad of het bestelaantal. Dit geldt ook voor de ordervelden Min. bestelaantal, Max. bestelaantal en Vaste lotgrootte. In plaats hiervan is dit het exacte tekort.  

 De planningsregel voor dit soort voorzieningenorder geeft een waarschuwingspictogram Noodgeval weer en er worden extra gegevens getoond bij het opzoeken om de gebruiker te informeren over de situatie.  

 In de volgende illustratie staat aanbod D voor een noodorder om een correctie uit te voeren voor negatieve voorraad.  

 ![Suggestie voor noodplanning om negatieve inventaris te voorkomen](media/nav_app_supply_planning_2_negative_inventory.png "Suggestie voor noodplanning om negatieve inventaris te voorkomen")  

1.  Voorziening **A**, de oorspronkelijk geplande voorraad, is onder het bestelpunt.  
2.  Er is een nieuwe voorwaarts-geplande voorziening gemaakt (**C**).  

     (Aantal = Maximale voorraad – Gepland voorraadniveau)  
3.  Voorziening **A** wordt afgesloten door vraag **B**, die niet volledig is verwerkt.  

     (Vraag **B** zou kunnen proberen Aanbod C in te plannen, maar dat gebeurt niet op basis van het tijdsintervalconcept.)  
4.  Er wordt nieuw aanbod (**D**) gemaakt om te voldoen aan het resterende aantal van de vraag **B**.  
5.  Vraag **B** wordt gesloten (waarbij een aanmaning voor de geplande voorraad wordt gemaakt).  
6.  De nieuwe voorziening **D** is afgesloten.  
7.  Geplande voorraad wordt gecontroleerd; bestelpunt is niet overschreden.  
8.  Voorziening **C** is afgesloten (er bestaat geen vraag meer).  
9. Laatste controle: Er bestaan geen openstaande voorraadniveauaanmaningen.  

> [!NOTE]  
>  Stap 4 geeft aan hoe het systeem in eerdere versies dan Microsoft Dynamics NAV 2009 SP1 reageert.  

Hiermee wordt de omschrijving afgerond van centrale principes met betrekking tot voorraadplanning op basis van bestelbeleid. In het volgende gedeelte worden de kenmerken van de vier ondersteunde soorten bestelbeleid beschreven.

## <a name="reordering-policies"></a>Bestelbeleid
Met het bestelbeleid wordt bepaald hoeveel wordt besteld wanneer het artikel moet worden aangevuld. Er zijn vier verschillende soorten bestelbeleid.  

### <a name="fixed-reorder-qty"></a>Vast bestelaantal
Het beleid Vast bestelaantal is gerelateerd aan de voorraadplanning van typische C-producten (lage voorraadkosten, laag verouderingsrisico en/of veel artikelen). Dit beleid wordt gewoonlijk gebruikt in relatie met een bestelpunt met de verwachte vraag tijdens de doorlooptijd van het artikel.  

#### <a name="calculated-per-time-bucket"></a>Berekend per tijdsinterval  
Als het planningssysteem ontdekt dat het bestelpunt in een bepaald tijdsinterval (bestelfrequentie) is bereikt of overschreden - boven of op het bestelpunt aan het begin van de periode en onder of op het bestelpunt aan het einde van de periode - wordt voorgesteld een nieuwe voorzieningenorder voor het opgegeven bestelaantal te maken en deze voorwaarts te plannen vanaf de eerste datum na het einde van het tijdsinterval.  

Door bestelpunten in combinatie met tijdsintervallen te gebruiken, wordt het aantal voorzieningsvoorstellen verminderd. Dit geeft een handmatig proces aan van het frequent door het magazijn lopen om de werkelijke inhoud in de verschillende opslaglocaties te controleren.  

#### <a name="creates-only-necessary-supply"></a>Maakt alleen benodigde voorzieningen  
Voordat een nieuwe voorzieningenorder wordt voorgesteld om aan een bestelpunt te voldoen, controleert het planningssysteem of al voorziening is besteld voor ontvangst binnen de doorlooptijd van het artikel. Als een bestaande voorzieningenorder het probleem oplost door de geplande voorraad binnen de looptijd op of boven het bestelpunt te brengen, stelt het systeem geen nieuwe voorzieningenorder voor.  

Orders voor voorzieningen die specifiek zijn gemaakt om te voldoen aan een bestelpunt, worden uitgesloten van de normale afstemming van voorzieningen en kunnen op geen enkele manier achteraf worden gewijzigd. Dus als een artikel dat het bestelpunt gebruikt, moet worden uitgefaseerd (niet aangevuld), is het raadzaam openstaande orders voor voorzieningen handmatig te controleren of het bestelbeleid te wijzigen in lot-voor-lot, waarbij het systeem overbodige voorzieningen reduceert of annuleert.  

#### <a name="combines-with-order-modifiers"></a>Combineert met orderaanpassingsfuncties  
De ordervelden Min. bestelaantal, Max. bestelaantal en Vaste lotgrootte zouden geen grote rol moeten afspelen wanneer het beleid voor vaste bestelaantallen wordt gebruikt. Het planningssysteem houdt echter toch rekening met deze wijzigingsfactoren en verlaagt het aantal tot het opgegeven maximum orderaantal (en maakt twee of meer voorzieningen om het totale orderaantal te bereiken), verhoogt de order tot het opgegeven maximum aantal of rondt het orderaantal af op een opgegeven orderveelvoud.  

#### <a name="combines-with-calendars"></a>Combineert met agenda's  
Voordat het planningssysteem een nieuwe voorzieningenorder voorstelt, wordt gecontroleerd of de order is gepland voor een niet-werkdag, volgens agenda's die zijn gedefinieerd in het veld **Basisagendacode** op de pagina's **Bedrijfsgegevens** en **Vestiging**.  

Als de verwachte datum een vrije dag is, verplaatst het planningssysteem de order voorwaarts naar de dichtstbijzijnde werkdatum. Dit kan resulteren in een order die voldoet een bestelpunt maar aan een bepaalde vraag niet voldoet. Voor dergelijke vraag in onbalans maakt het systeem een extra voorziening.  

#### <a name="should-not-be-used-with-forecast"></a>Moet niet worden gebruikt met prognose  
Omdat de verwachte vraag al is uitgedrukt in het bestelpuntniveau, is het niet nodig een prognose in de planning van een artikel op te nemen met behulp van een bestelpunt. Als het belangrijk is dat de planning op een prognose wordt gebaseerd, gebruikt u het lot-voor-lot beleid.  

#### <a name="must-not-be-used-with-reservations"></a>Mag niet met reserveringen worden gebruikt  
Als de gebruiker een aantal heeft gereserveerd, bijvoorbeeld een aantal in voorraad, voor een of andere toekomstige vraag, wordt de basis van de planning verstoord. Zelfs als de geplande voorraad met betrekking tot het bestelpunt aanvaardbaar is, zijn de hoeveelheden mogelijk niet beschikbaar. Het systeem probeert dit mogelijk te compenseren door uitzonderingsorders aan te maken. Het wordt echter aangeraden het veld Reserveren in te stellen op Nooit voor artikelen die worden gepland met behulp van een bestelpunt.

### <a name="maximum-qty"></a>Maximum aantal
Het beleid Maximum aantal is een manier om voorraad bij te houden met behulp van een bestelpunt.  

Alles over het beleid voor een vast bestelaantal geldt ook voor dit beleid. Het enige verschil is de hoeveelheid van de voorgestelde voorziening. Wanneer het beleid voor maximaal aantal wordt gebruikt, wordt het bestelaantal dynamisch bepaald op basis van het geplande voorraadniveau en verschilt daarom gewoonlijk per order.  

#### <a name="calculated-per-time-bucket"></a>Berekend per tijdsinterval  
Het bestelaantal wordt bepaald op het moment (het einde van het tijdsinterval) dat het planningssysteem detecteert dat het bestelpunt is overschreden. Op dit moment meet het systeem het verschil tussen het huidige geplande voorraadniveau en de opgegeven maximale voorraad. Dit vormt het aantal dat opnieuw moet worden besteld. Het systeem controleert vervolgens of de voorziening al elders is besteld voor ontvangst binnen de doorlooptijd. Als dit het geval is, wordt het aantal van de nieuwe voorzieningenorder verminderd met de reeds bestelde aantallen.  

Het systeem zorgt dat de geplande voorraad ten minste het bestelpuntniveau bereikt, voor het geval dat de gebruiker is vergeten een maximaal voorraadaantal op te geven.  

#### <a name="combines-with-order-modifiers"></a>Combineert met orderaanpassingsfuncties  
Afhankelijk van de instellingen kan het het beste zijn om het maximale aantal-beleid te combineren met orderwijzigingen om een minimaal orderaantal te garanderen of af te ronden op een geheel aantal inkoopeenheden, of te splitsen in meerdere lots zoals bepaald door het maximale orderaantal.  

### <a name="combines-with-calendars"></a>Combineert met agenda's  
Voordat het planningssysteem een nieuwe voorzieningenorder voorstelt, wordt gecontroleerd of de order is gepland voor een niet-werkdag, volgens agenda's die zijn gedefinieerd in het veld **Basisagendacode** op de pagina's **Bedrijfsgegevens** en **Vestiging**.  

Als de verwachte datum een vrije dag is, verplaatst het planningssysteem de order voorwaarts naar de dichtstbijzijnde werkdatum. Dit kan resulteren in een order die voldoet een bestelpunt maar aan een bepaalde vraag niet voldoet. Voor dergelijke vraag in onbalans maakt het systeem een extra voorziening.

### <a name="order"></a>Volgorde
In een op-order-produceren omgeving wordt een artikel ingekocht of geproduceerd om uitsluitend aan een specifieke vraag te voldoen. Meestal heeft dit betrekking op A-producten en de motivatie om het bestelbeleid Order te kiezen, kan zijn dat de vraag niet frequent is, dat de doorlooptijd onbeduidend is of dat de vereiste kenmerken verschillen.  

De toepassing maakt een order-naar-order-koppeling die fungeert als voorlopige verbinding tussen de voorziening, een voorzieningenorder of voorraad, en de vraag waaraan het zal voldoen.  

Afgezien van het gebruik van het bestelbeleid kan de order-aan-order koppeling tijdens planning op de volgende manieren worden toegepast:  

* Wanneer het productiebeleid Op order produceren wordt gebruikt om productieorders met meerdere niveaus of projecttype te maken (waarbij benodigde onderdelen op dezelfde productieorder worden geproduceerd).  
* Wanneer de functie Verkooporderplanning wordt gebruikt om een productieorder te maken van een verkooporder.  

Zelfs als een productiebedrijf zichzelf beschouwt als een op-order-produceren omgeving, kan het het best zijn een lot-voor-lot bestelbeleid te gebruiken als de artikelen standaard zijn, zonder variatie in kenmerken. Hierdoor gebruikt het systeem niet-geplande voorraad en worden verkooporders alleen gecumuleerd met dezelfde verzenddatum of binnen een bepaalde periode.  

#### <a name="order-to-order-links-and-past-due-dates"></a>Order-naar-order koppelingen en overschreden vervaldatums  
In tegenstelling tot de meeste combinaties van voorziening en vraag, worden gekoppelde orders met vervaldatums voor de begindatum van de planning, volledig door het systeem gepland. De bedrijfsreden voor deze uitzondering is dat specifieke vraag-voorzieningcombinaties moeten worden gesynchroniseerd tot aan uitvoering. Zie voor meer informatie over de vaste zone die voor de meeste vraag/aanbodstypen geldt, [Werken met orders vóór de geplande begindatum](design-details-balancing-demand-and-supply.md#dealing-with-orders-before-the-planning-starting-date).

### <a name="lot-for-lot"></a>Lot-for-Lot
Het lot-for-lot-beleid is het meest flexibel omdat het systeem alleen reageert op werkelijke vraag, én rekening houdt met verwachte vraag uit prognoses en raamcontracten en vervolgens het orderaantal op basis van de vraag vereffent. Het lot-for-lot-beleid is bedoeld voor A- en B-artikelen waar voorraad kan worden geaccepteerd maar vermeden moet worden.  

In sommige opzichten lijkt het lot-voor-lot beleid op het orderbeleid, maar het hanteert een algemene aanpak van artikelen; het kan aantallen in voorraad accepteren en het bundelt vraag en corresponderend aanbod in tijdsintervallen die door de gebruiker worden gedefinieerd.  

Het tijdsinterval wordt gedefinieerd in het veld **Tijdsinterval**. Er wordt gewerkt met een minimumtijdsinterval van één dag, aangezien dit de kleinste tijdseenheid voor vraag- en voorzieningsgebeurtenissen in het systeem is (hoewel in de praktijk de tijdseenheid voor productieorders en materiaalbehoeften zelfs seconden kan zijn).  

Met het tijdsinterval worden ook limieten ingesteld wanneer een bestaande voorzieningenorder opnieuw moet worden gepland om te voldoen aan een bepaalde vraag. Als het aanbod binnen het tijdsinterval ligt, wordt het opnieuw in of uit gepland om aan de vraag te voldoen. Als de voorziening eerder ligt, ontstaat onnodige opeenhoping van voorraad en moet worden geannuleerd. Als het later ligt, wordt in plaats daarvan een nieuwe order gemaakt.  

Met dit beleid is het ook mogelijk om een veiligheidsvoorraad te definiëren om mogelijke schommelingen in voorzieningen op te vangen of te voldoen aan plotselinge vraag.  

Omdat het aantal van de voorzieningenorder op de werkelijke vraag is gebaseerd, kan het zinnig zijn de orderwijzigingen te gebruiken: rond het orderaantal naar boven af om aan een opgegeven orderveelvoud (of inkoopeenheid) te voldoen, vergroot de order tot een opgegeven minimaal orderaantal of verlaag het aantal tot het opgegeven maximale aantal (en maak zo twee of meer voorzieningen om het totaal benodigde aantal te bereiken).

## <a name="see-also"></a>Zie ook  
[Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md)   
[Ontwerpdetails: Tabel Planningstoewijzing](design-details-planning-assignment-table.md)   
[Ontwerpdetails: Centrale begrippen van het planningssysteem](design-details-central-concepts-of-the-planning-system.md)   
[Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md)   
[Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]