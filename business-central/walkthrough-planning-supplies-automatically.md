---
title: Procedure - Goederen automatisch plannen
description: Deze procedure laat zien hoe u het leveringsplanningssysteem kunt gebruiken om automatisch inkoop- en productieorders voor verschillende verkooporders te plannen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: bholtorf
---
# <a name="walkthrough-planning-supplies-automatically"></a>Procedure: Goederen automatisch plannen

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Termen zoals 'planningsvoorstel uitvoeren' en 'MRP uitvoeren' verwijzen naar het berekenen van het hoofdproductieschema en de benodigde materialen op basis van de werkelijke en de geprognosticeerde behoefte.  

-   MPS is de berekening van een hoofdproductieschema op basis van de werkelijke vraag en de vraagprognose. De MPS-berekening wordt gebruikt voor eindartikelen met een voorspelling of een verkooporderregel. Deze artikelen worden "MPS-artikelen" genoemd en worden dynamisch geïdentificeerd wanneer de berekening start.  
-   MRP is de berekening van het benodigde materiaal op basis van de werkelijke vraag naar materiaal en de vraagprognose op materiaalniveau. MRP wordt alleen berekend voor artikelen die geen MPS-artikelen zijn. Het uiteindelijke doel van MRP is om in tijd gefaseerde formele plannen te leveren, per artikel, om het juiste artikel op de juiste tijd te kunnen leveren, op de juiste plaats en in de juiste aantallen.  

 De planningsalgoritmen die worden gebruikt voor MPS en MRP zijn identiek. De planningsalgoritmen maken gebruik van netting, hergebruik van bestaande voorraadorders, en actieberichten. Er wordt door het planningssysteem gekeken naar wat er nodig is of zal zijn (behoefte) en wat er beschikbaar is of verwacht wordt (voorziening). Als deze hoeveelheden tegen elkaar zijn weggestreept, worden actieberichten weergegeven in het planningsvoorstel. Actieberichten zijn suggesties voor het maken van een nieuwe voorraadorder, het wijzigen van een voorraadorder (hoeveelheid of datum), of het annuleren van een bestaande voorraadorder. Voorraadorders kunnen productieorders, inkooporders of transferorders zijn. Zie voor meer informatie [Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md).  

 Het planningsresultaat wordt deels berekend op basis van de vraag-aanbodsets in de database en deels op basis van de SKU-kaarten of artikelkaarten, productiestuklijsten en bewerkingsplannen.  

## <a name="about-this-walkthrough"></a>Informatie over deze procedure
 In dit overzicht ziet u hoe u het voorraadplanningsysteem kunt gebruiken om automatisch alle inkoop- en productieorders te plannen die nodig zijn om 15 toerfietsen te produceren die worden gevraagd volgens verschillende verkooporders. Voor een duidelijk en realistisch overzicht wordt het aantal planningsregels beperkt door alle andere vraag/aanbod-sets in het demobedrijf CRONUS International Ltd. uit te filteren behalve de verkoopvraag op de vestiging OOST.  

 In deze procedure worden de volgende taken beschreven:  

-   De verkooporder maken en een volledig voorraadplan berekenen.  
-   Planningsparameters en ordertraceringsposten achter de planningsregels weergeven.  
-   Automatisch de voorgestelde voorraadorders maken.  
-   Nieuwe verkoopvraag maken en dienovereenkomstig plannen.  

## <a name="roles"></a>Rollen

-   Productieplanner  
-   Inkoper  

## <a name="prerequisites"></a>Vereisten
 U moet het volgende doen om deze procedure uit te voeren:  

-   Het voorbeeldbedrijf CRONUS International Ltd.  
-   Voor het wijzigen van diverse ingestelde waarden door de stappen in het gedeelte 'Voorbeeldgegevens voorbereiden', verderop in dit overzicht te volgen.  

## <a name="story"></a>Scenario
 De klant, Cannon Group PLC, bestelt vijf toerfietsen voor verzending op 5 februari 2021.  

 Eduardo, de productieplanner, voert de routinevoorraadplanning uit voor de eerste week van februari 2021. Eduardo filtert op hun eigen vestiging, OOST, en voert een planningsinterval in van de werkdatum (23 januari 2021) tot 7 februari 2021 alvorens een voorlopig voorraadplan te berekenen.  

 De enige vraag voor die week is voor de verkooporder van de Cannon Group. Eduardo ziet dat geen van de planningsregels een waarschuwing bevat en gaat voorraadorders maken zonder wijzigingen voor de voorgestelde planningsregels.  

 De volgende dag, nog voordat een van de voorlopige voorraadorders is gestart of geboekt, krijgt Eduardo bericht dat een andere klant tien toerfietsen heeft besteld voor verzending op 12 februari 2021. Daarom berekent Eduardo het voorraadplan opnieuw om het aan te passen aan de gewijzigde vraag. De herberekening leidt tot een mutatieplan met een voorstel om zowel de tijd als de hoeveelheid van een aantal voorraadorders te wijzigen die tijdens de eerste run zijn gemaakt.  

 Tijdens de diverse stappen van de planning zoekt Eduardo de betreffende orders op en gebruikt de functie Ordertracering om te zien welke vraag door welk aanbod wordt gedekt.  

## <a name="preparing-sample-data"></a>Voorbeeldgegevens voorbereiden
 Maak SKU's (StockKeeping Units) voor de toerfiets en een selectie van de samenstellende onderdelen, artikelnummers 1001 tot en met 1300. Sommige onderdelen worden uitgesloten om de procedures te vereenvoudigen. Pas de planningsparameters van de geselecteerde materialen aan voor een meer transparant planningsresultaat.  

### <a name="to-create-stockkeeping-units"></a>SKU's maken

1.  Open de artikelkaart voor artikel 1001, Toerfiets.  
2.  Kies de actie **SKU maken**.  
3.  Laat op de pagina **SKU maken** alle opties en filters ongewijzigd en klik op de knop **OK**.  
4.  Herhaal stap 1 tot en met 3 voor alle artikelen in het getallenbereik tussen 1100 en 1300.  

### <a name="to-change-selected-planning-parameters"></a>Geselecteerde planningsparameters wijzigen

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **SKU's** in en kies vervolgens de gerelateerde koppeling.  
2.  Open de SKU-kaart van OOST voor artikel 1100, Voorwiel.  
3.  Vul de velden op het sneltabblad **Gepland** in, zoals in de volgende tabel is beschreven.  

    |Bestelbeleid|Veiligheidsvoorraad|Lotaccumulatieperiode|Herplanningsperiode|  
    |-------------------------------------------|-----------------------------------------------|-------------------------------------------------|---------------------------------------------|  
    |Lot-for-Lot|Leeg|2W|2W|  

4.  Herhaal stap 2 en 3 voor alle SKU´s in het getallenbereik tussen 1100 en 1300.  

 Hiermee is de voorbereiding van voorbeeldgegevens voor het overzicht voltooid.  

## <a name="creating-a-regenerative-supply-plan"></a>Een regeneratief voorraadplan maken
 In reactie op een nieuwe verkooporder voor vijf toerfietsen, start Ricardo het planningsproces door filters, opties, planningsinterval in te stellen en alle andere vraag, behalve die uit de eerste week van februari op de vestiging OOST, uit te sluiten. Ricardo begint met de berekening van een MPS (hoofdproductieschema) en berekent vervolgens een volledig voorraadplan voor alle vraag op lager niveau (MRP).  

### <a name="to-create-the-sales-order"></a>De verkooporder maken

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Nieuw**.  
3.  Vul op de pagina **Verkooporder** de velden in, zoals is beschreven in de volgende tabel.  

    |Naam van orderklant|Verzenddatum|Artikelnr.|Locatie|Aantal|  
    |----------------------------|-------------------|--------------|--------------|--------------|  
    |Van Terp Kantoorinrichting|05-02-2014|1001|OOST|5|  

4.  Accepteer de beschikbaarheidswaarschuwing en kies de knop **Ja** om het nieuwe gevraagde aantal vast te leggen.  

### <a name="to-create-a-regenerative-plan-to-fulfill-demand-at-location-east"></a>Een regeneratief plan maken om aan de vraag op de vestiging OOST te voldoen

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Planningsvoorstel** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Regeneratief plan berekenen**.  
3.  Vul op de pagina **Plan berekenen - Planningsvoorstel** de velden in zoals beschreven in de volgende tabel.  

    |Planning berekenen|Begindatum|Einddatum|Resultaten weergeven:|Totalen beperken tot|  
    |--------------------|-------------------|-----------------|-------------------|---------------------|  
    |**MPS** = Ja<br /><br /> **MRP** = Nee|23-01-2021<br /><br /> (werkdatum)|07-02-2021|1001..1300|Vestigingsfilter = OOST|  

4.  Kies **OK** om de planning te starten.  

     Er wordt één planningsregel gemaakt met het voorstel dat er een geplande productieorder wordt uitgegeven voor de productie van de tien toerfietsen, artikel 1001, vóór 5 februari 2021, de verzenddatum van de verkooporder.  

     Controleer vervolgens of deze planningsregel gaat over de Cannon Group-verkooporder met de functie **Ordertracering**, die vraag en gepland aanbod dynamisch koppelt.  

5.  Selecteer de nieuwe planningsregel en kies de actie **Ordertracering**.  
6.  Kies op de pagina **Ordertracering** de actie **Weergeven**.  

     De verkooporder voor de verzending van vijf toerfietsen naar klantnummer 10000, op 05-02-2021, wordt weergegeven.  

7.  Sluit de pagina's **Verkooporder** en **Ordertracering**.  

### <a name="to-calculate-mrp-to-include-underlying-component-needs"></a>MRP berekenen om onderliggende materiaalbehoeften op te nemen

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Planningsvoorstel** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Regeneratief plan berekenen**.  
3.  Vul op de pagina **Plan berekenen - Planningsvoorstel** de velden in zoals beschreven in de volgende tabel.  

    |Berekenen|Begindatum|Einddatum|Resultaten weergeven:|Totalen beperken tot:|  
    |---------------|-------------------|-----------------|-------------------|----------------------|  
    |**MPS** = Ja<br /><br /> **MRP** = Ja|23-01-2021|07-02-2021|1001..1300|Vestigingsfilter = OOST|  

4.  Kies de knop **OK** om de planning te starten.  

     Er worden in totaal 14 planningsregels gemaakt met een voorstel voor voorraadorders voor alle vraag in verband met de verkooporder voor toerfietsen op de vestiging OOST.  

## <a name="analyze-the-planning-result"></a>Het planningsresultaat analyseren
 Voor het analyseren van de voorgestelde aantallen vouwt Eduardo de geselecteerde planningsregels uit om ordertraceringsposten en planningsparameters te zien.  

 Noteer op de pagina **Planningsvoorstel** in de kolom **Vervaldatum** dat de levering van de voorgestelde orders achterwaarts is gepland vanaf de vervaldatum van de verkooporder, 05-02-2021. De tijdlijn begint op de bovenste planningsregel met de productieorder voor het produceren van de voltooide toerfietsen. De tijdlijn eindigt op de onderste planningsregel met de inkooporder voor een van de artikelen op het laagste niveau, 1255, Socket (achter), met 01-30-2021 als vervaldatum. Evenals de planningsregel voor artikel 1251, Draagas achterwiel, staat deze regel voor een inkooporder voor materialen met een deadline op de begindatum van het bijbehorende geproduceerde hoofdartikel, subassemblageartikel 1250, dat een deadline heeft van 03-02-2014. In het voorstel ziet u dat alle onderliggende artikelen moeten worden voldaan op de begindatum van de bovenliggende artikelen.  

 In de planningsregel voor artikel 1300, kettingmontage, worden tien stuks voorgesteld. Dit wijkt van de vijf stuks af die we verwachten nodig te hebben om de verkooporder te voldoen. Ga door om de ordertraceringsposten weer te geven.  

### <a name="to-view-order-tracking-entries-for-item-1300"></a>Ordertraceringposten voor artikel 1300 weergeven

1.  Selecteer de planningsregel voor artikel 1300 en kies de actie **Ordertracering**.  

     De twee regels op de pagina **Ordertracering** laten zien dat er vijf stuks worden getraceerd vanaf de planningsregel (eerste ordertraceringsregel) tot aan verkooporder 1001 (tweede traceringsregel). De laatste vijf stuks die in de planning worden voorgesteld, houden geen verband met documentregels, maar met een planningsparameter, een prognosepost of een raamcontractpost. Dergelijke niet-getraceerde aantallen worden opgeteld in het veld **Niet getraceerd aantal** in de koptekst van de pagina **Ordertracering**.  

2.  Selecteer het veld **Niet getraceerd aantal**.  

     Op de pagina **Niet-getraceerd planningselementen** ziet u dat artikel 1300 gebruikmaakt van een planningsparameter, Min. bestelaantal, met de waarde 10,00. Daarom is de planningsregel voor tien stuks in totaal, waarvan er slechts vijf worden getraceerd naar een vraag. De laatste vijf stuks zijn een niet-getraceerd aantal om aan de planningsparameter te voldoen. Ga verder met het bekijken van de planningsparameter.  

### <a name="to-check-the-planning-parameter"></a>De planningsparameter controleren

1.  Op de pagina **Niet-getraceerde planningselementen** selecteert u de ordertraceringsregel van artikel 1300.  
2.  Kies het veld **Artikelnr.** en kies vervolgens de actie **Geavanceerd**.  
3.  Kies op de pagina **Artikeloverzicht** de actie **SKU's**.  
4.  Open op de pagina **SKU-overzicht** de SKU-kaart van OOST.  
5.  Op het sneltabblad **Planning** ziet u dat het veld **Min. bestelaantal** de waarde 10 bevat.  
6.  Sluit alle pagina's behalve **Planningsvoorstel**.  

### <a name="to-view-more-order-tracking-entries"></a>Meer ordertraceringsposten weergeven

1.  Selecteer de planningsregel voor artikel 1110 Velg en kies de actie **Ordertracering**.  

     De pagina **Ordertracering** geeft aan dat vijf velgen per productieorder nodig zijn voor respectievelijk voor- en achterwielen.  

     Dezelfde ordertracering geldt voor de planningsregels voor de artikelen 1120, 1160 en 1170. Voor artikel 1120 is het veld **Aantal per** op de productiestuklijst van elk wielartikel ingesteld op 50 stuks, wat een totaal van 100 oplevert.  

     De planningsregel voor artikel 1150 voor zes stuks lijkt onregelmatig. Ga door om te analyseren.  

2.  Selecteer de planningsregel voor artikel 1150 en kies de actie **Ordertracering**.  

     De pagina **Ordertracering** toont dat vijf eenheden worden getraceerd naar het voorwiel, en één eenheid niet is getraceerd. Ga door het niet-getraceerde aantal weer te geven.  

3.  Selecteer het veld **Niet getraceerd aantal**.  

     Op de pagina **Niet-getraceerde planningselementen** blijkt dat artikel 1150 een planningsparameter Vaste lotgrootte gebruikt met de waarde 2.00. Dit geeft aan dat het artikel moet worden besteld in aantallen die deelbaar zijn door 2. Het getal dat het dichtst bij 5 ligt en dat deelbaar is door 2, is 6.  

     Dezelfde ordertracering geldt voor planningsregels voor voornaafonderdelen, artikelen 1151 en 1155, behalve dat elke behoefte wordt vermenigvuldigd met het uitvalpercentage dat is ingesteld voor artikel 1150 in het veld **Uitvalpercentage** op de artikelkaart.  

 Hiermee is de analyse van het oorspronkelijke voorraadplan voltooid. Het selectievakje **Planningsboodschap accepteren** is ingeschakeld in alle planningsregels, wat aangeeft dat ze gereed zijn om te worden geconverteerd naar voorzieningenorders.  

## <a name="carrying-out-action-messages"></a>Planningsboodschappen uitvoeren
 Vervolgens converteert Eduardo de voorgestelde planningsregels naar voorraadorders met de functie **Planningsboodschap uitvoeren**.  

### <a name="to-automatically-create-the-suggested-supply-orders"></a>Automatisch de voorgestelde voorraadorders maken

1.  Schakel het selectievakje **Planningsboodschap accepteren** in op alle planningsregels met een waarschuwing van het soort Uitzondering.  
2.  Kies de actie **Planningsboodschap uitvoeren**.  
3.  Vul op de pagina **Planningsboodschap uitvoeren - Plan.** de velden in, zoals is beschreven in de volgende tabel.  

    |Productieorder|Inkooporder|Transferorder|  
    |----------------------|--------------------|--------------------|  
    |Vast gepland|Inkooporders maken|Transferorders maken|  

4.  Klik op **OK** om automatisch alle voorgestelde voorraadorders te maken.  
5.  Sluit de lege pagina **Planningsvoorstel**.  

 Hiermee is de oorspronkelijke berekening, de analyse en het maken van een voorraadplan voor de vraag op de vestiging OOST in de eerste week van februari voltooid. In het volgende gedeelte bestelt een andere klant tien toerfietsen en moet Eduardo opnieuw plannen.  

## <a name="creating-a-net-change-plan"></a>Een mutatieplan maken
 De volgende dag, voordat er voorraadorders zijn gestart of geboekt, arriveert een nieuwe verkooporder van Libros S.A. voor tien toerfietsen die moeten worden verzonden op 12 februari 2021. Eduardo krijgt bericht van de nieuwe vraag en plant opnieuw om het huidige voorzieningsplan aan te passen. Eduardo gebruikt de functie Mutatieplan berekenen om alleen de wijzigingen te berekenen die zijn aangebracht in vraag of aanbod sinds de laatste planningsrun. Bovendien breidt Eduardo de planningsperiode uit naar 14 februari 2021 om de nieuwe verkoopvraag op 12 februari 2014 mee te nemen.  

 In het planningsysteem wordt de beste manier berekend om te voldoen aan de vraag naar deze twee identieke producten, zoals het samenvoegen van bepaalde inkoop- en productieorders, het opnieuw plannen van andere orders en het zo nodig maken van nieuwe orders.  

### <a name="to-create-the-new-sales-demand-and-replan-accordingly"></a>De nieuwe verkoopvraag maken en dienovereenkomstig opnieuw plannen

1.  Kies de actie **Nieuw**.  
2.  Vul op de pagina **Verkooporder** de velden in, zoals is beschreven in de volgende tabel.  

    |Naam van orderklant|Verzenddatum|Artikelnr.|Locatie|Aantal|  
    |----------------------------|-------------------|--------------|--------------|--------------|  
    |Libros S.A.|12-02-2021|1001|OOST|10|  

3.  Accepteer de beschikbaarheidswaarschuwing en klik op **Ja** om het gevraagde aantal vast te leggen.  
4.  Plan vervolgens opnieuw voor aanpassing van het huidige voorraadplan.  
5.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Planningsvoorstel** in en kies vervolgens de gerelateerde koppeling.  
6.  Kies de actie **Mutatieplan berekenen**.  
7.  Vul op de pagina **Plan berekenen - Planningsvoorstel** de velden in zoals beschreven in de volgende tabel.  

    |Planning berekenen|Begindatum|Einddatum|Resultaten weergeven:|Totalen beperken tot|  
    |--------------------|-------------------|-----------------|-------------------|---------------------|  
    |**MPS** = Ja<br /><br /> **MRP** = Ja|23-01-2021|14-02-2021|1001..1300|Vestigingsfilter = OOST|  

8.  Kies de knop **OK** om de planning te starten.  

 In totaal zijn er 14 planningsregels gemaakt. In de eerste planningsregel ziet u dat in het veld **Planningsboodschap** de tekst **Nieuw** wordt weergegeven, in het veld **Aantal** 10 staat en in het veld **Vervaldatum** 12 februari 2021 staat. Deze nieuwe regel voor het bovenliggende artikel, 1001, toerfiets, is gemaakt omdat het artikel gebruikmaakt van een bestelbeleid volgens **Order**, wat betekent dat deze moet worden geleverd in een één-op-één-relatie met de vraag, de verkooporder van tien stuks.  

 De volgende twee planningsregels zijn de productieorders voor de wielen van de toerfiets. Elke bestaande order van vijf, in het veld **Oorspr. aantal**, wordt verhoogd tot 15 in het veld **Aantal**. Beide productieorders hebben ongewijzigde vervaldatums, zoals aangegeven in het veld **Planningsboodschap** dat **Aantal wijzigen** bevat. Dit is ook het geval voor de planningsregel voor artikel 1300, behalve dat diens lotgrootte van 10,00 de getraceerde vraag voor 15 stuks afrondt naar 20.  

 Alle andere planningsregels hebben een planningsboodschap met **Herplannen en aantal wijzigen**. Dit betekent dat, los van een verhoging in aantal, de vervaldatums worden verplaatst conform het voorraadplan om het extra aantal op te nemen in de beschikbare productietijd (capaciteit). Ingekochte materialen worden opnieuw gepland en verhoogd om voor de productieorders te leveren. Ga door om de nieuwe planning te analyseren.  

## <a name="analyze-the-changed-planning-result"></a>Het gewijzigde planningsresultaat analyseren
 Omdat alle lot-voor-lot-geplande artikelen in het filter, 1100 tot 1300, een herplanningsperiode van twee weken hebben, worden de bestaande leveringsorders allemaal gewijzigd om aan de nieuwe vraag te voldoen, die binnen de opgegeven twee weken plaatsvindt.  

 Verschillende planningsregels worden eenvoudig vermenigvuldigd met drie om 15 toerfietsen te bieden in plaats van 5, en de vervaldatums worden terug in de tijd verplaatst om de verhoogde aantallen te bieden op de verzenddatum van de verkooporder aan de Cannon Group. Voor deze planningregels kunnen alle aantallen worden getraceerd. De resterende planningsregels worden verhoogd met tien stuks bovenop en daarnaast worden de vervaldatums verplaatst. Voor deze planningregels is een deel van de aantallen niet-getraceerd als gevolg van verschillende planningsparameters. Ga door om enkele van deze ordertraceringsposten weer te geven.  

### <a name="to-view-order-tracking-entries-for-item-1250"></a>Ordertraceringposten voor artikel 1250 weergeven

1.  Selecteer de planningsregel voor artikel 1250 en kies de actie **Ordertracering**.  

     De zeven regels op de pagina **Ordertracering** geven weer dat vijf en tien stuks worden getraceerd van het achterwiel naar de toerfietsen op de twee respectievelijke verkooporders.  

     De laatste vijf stuks zijn niet-getraceerd. Ga door om te analyseren.  

2.  Selecteer het veld **Niet getraceerd aantal**.  

     Op de pagina **Niet-getraceerd planningselementen** ziet u dat artikel 1250 gebruikmaakt van een planningsparameter Vaste lotgrootte, met de waarde 10,00. Daarom bevat de planningsregel de waarde 20, om de werkelijke behoefte naar boven af te ronden op het eerstvolgende getal dat deelbaar is door 10. De laatste vijf stuks zijn een niet-getraceerd aantal om aan de planningsparameter te voldoen.  

3.  Sluit alle pagina's behalve **Planningsvoorstel**.  

### <a name="to-view-an-existing-order"></a>Een bestaande order bekijken

1.  Selecteer in de planningsregel voor artikel 1250 het veld **Referentieordernummer**. toe te wijzen.  
2.  Op de pagina **Vast geplande productieorder** voor de achternaaf. De bestaande order voor tien stuks die u in de eerste planning hebt gemaakt, opent.  
3.  Sluit de vast geplande productieorder.  

 Hiermee is het overzicht voltooid van de manier waarop het planningsysteem wordt gebruikt om automatisch de vraag te detecteren, de juiste voorraadorders te berekenen overeenkomstig de vraag en de planningsparameters, en vervolgens automatisch verschillende soorten voorraadorders te maken met de juiste datums en aantallen.  

## <a name="see-also"></a>Zie ook
 [Procedures voor bedrijfsprocessen](walkthrough-business-process-walkthroughs.md)   
<!--  [Walkthrough: Planning Supplies Manually](walkthrough-planning-supplies-manually.md)    -->
 [Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
