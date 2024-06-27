---
title: 'Ontwerpdetails: Bestelbeleid verwerken'
description: Dit artikel geeft een overzicht van het bestelbeleid dat u kunt gebruiken bij leveringsplanning.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 06/12/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Ontwerpdetails: Bestelbeleid verwerken

Om een artikel op te nemen in de leveringsplanning moet u een bestelbeleid voor het artikel specificeren op de pagina **Artikel**. De volgende soorten bestelbeleid zijn beschikbaar:  

* Vast bestelaantal  
* Maximum aantal  
* Volgorde  
* Lot-for-Lot  

Het beleid **Vast bestelaantal** en het beleid **Maximum aantal** hebben betrekking op voorraadplanning. Dit beleid bestaat naast het stapsgewijze afstemmen van aanbod en ordertracering.  

## De rol van het bestelpunt

Een bestelpunt vertegenwoordigt vraag tijdens doorlooptijd. Wanneer wordt voorspeld dat voorraad onder het niveau komt dat door het bestelpunt is gedefinieerd, is het tijd om meer te bestellen. De voorraad zal geleidelijk afnemen totdat de aanvulling arriveert. Het kan nul of het niveau van de veiligheidsvoorraad bereiken. Het planningssysteem zal een voorwaarts geplande voorzieningenorder voorstellen op het moment dat de verwachte voorraad onder het bestelpunt komt.  

Voorraadniveaus kunnen aanzienlijk veranderen gedurende het tijdsinterval. Daarom monitort het planningssysteem voortdurend de beschikbare voorraad.

## Het verwachte voorraadniveau en het bestelpunt controleren

Voorraad is een soort aanbod, maar voor voorraadplanning maakt het planningssysteem onderscheid tussen twee voorraadniveaus:  

* Geplande voorraad  
* Geplande beschikbare voorraad  

### Geplande voorraad  

Aan het begin van het planningsproces is de verwachte voorraad de brutohoeveelheid voorraad. De brutohoeveelheid omvat geboekte en niet-geboekte vraag en aanbod in het verleden. Deze hoeveelheid wordt een gepland voorraadniveau dat brutohoeveelheden van toekomstige vraag en aanbod behouden. Toekomstige vraag en aanbod worden geïntroduceerd langs de tijdlijn, gereserveerd of op andere manieren toegewezen.  

De geplande voorraad wordt gebruikt door het planningssysteem om het bestelpunt te controleren en het bestelaantal te bepalen met het bestelbeleid **Maximum aantal**.  

### Geplande beschikbare voorraad  

De geplande beschikbare voorraad is de voorraad die op een bepaald moment beschikbaar is om aan de vraag te voldoen. De geplande beschikbare voorraad wordt gebruikt voor het controleren van de veiligheidsvoorraad. Veiligheidsvoorraad moet altijd beschikbaar zijn voor onverwachte vraag.  

### Tijdsintervallen  

Geplande voorraad is belangrijk om te detecteren wanneer het bestelpunt wordt bereikt of overschreden en om het juiste orderaantal te berekenen wanneer het bestelbeleid **Maximum aantal** wordt gebruikt.  

Het geplande voorraadniveau wordt berekend aan het begin van de planningsperiode. Het een brutoniveau is dat geen rekening houdt met reserveringen en andere toewijzingen. Om dit voorraadniveau te controleren tijdens de planningsreeks, controleert het planningssysteem de samengevoegde wijzigingen gedurende een periode. Die periode wordt een *tijdsinterval* genoemd. Ga voor meer informatie over tijdsintervallen naar [De rol van het tijdsinterval](#the-role-of-the-time-bucket). Het planningssysteem zorgt ervoor dat het tijdsinterval minimaal één dag is. Eén dag is de minimale tijdseenheid voor vraag- of aanbodgebeurtenissen.  

### Het geplande voorraadniveau bepalen  

In de volgende reeks wordt beschreven hoe het voorspelde voorraadniveau wordt bepaald:  

* Wanneer een aanbodgebeurtenis, zoals een inkooporder, totaal is gepland, wordt hiermee de geplande voorraad verhoogd op de vervaldatum van de gebeurtenis.  
* Wanneer aan een vraaggebeurtenis volledig is voldaan, wordt de geplande voorraad niet direct verminderd. In plaats hiervan wordt een afnameherinnering geboekt. Dat is een interne record die de datum en het aantal bevat van de toevoeging aan de geplande voorraad.  
* Wanneer een latere aanbodgebeurtenis wordt gepland en aan de tijdlijn wordt toegevoegd, onderzoekt het systeem geboekte afnameherinneringen een voor een tot de geplande datum van het aanbod. Tijdens dit proces kan het bestelpuntniveau van de interne toenameherinnering worden bereikt of overschreden.  
* Als een nieuwe aanvulorder wordt geïntroduceerd, controleert het systeem of deze vóór het huidige aanbod wordt ingevoerd. Als dat zo is, wordt het nieuwe aanbod het huidige aanbod en begint de afstemmingsprocedure opnieuw.  

De volgende afbeelding toont dit principe.  

![Het verwachte voorraadniveau bepalen.](media/nav_app_supply_planning_2_projected_inventory.png "Het verwachte voorraadniveau bepalen")  

1. Voorziening **Sa** van 4 (vast) sluit vraag **Da** van -3 af.  
2. CloseDemand: Maak een afnameaanmaning van -3 (niet weergegeven).  
3. Aanbod **Sa** is afgesloten met een overschot van 1 (er is niet meer vraag).  

     Hiermee wordt het geplande voorraadniveau verhoogd naar +4, terwijl de geplande **beschikbare** voorraad -1 wordt.  

4. Het volgende aanbod **Sb** van 2 (een andere order) is al ingesteld op de tijdlijn.  
5. Het planningssysteem controleert op een afnameherinnering vóór **Sb** (in dit voorbeeld is die er niet, dus wordt er geen actie ondernomen).  
6. Het systeem sluit aanbod **Sb** (er bestaat geen vraag meer) door A het te verlagen tot 0 (annuleren) of B het te laten zoals het is.  

     Hiermee wordt het voorspelde voorraadniveau verhoogd (A: +0 => +4 or B: +2 = +6).  

7. Het planningssysteem doet een laatste controle. Is er een afnameherinnering? Ja, er is er één op de datum van **Da**.  
8. Het planningssysteem voegt de afnameherinnering -3 toe aan het verwachte voorraadniveau, hetzij A: +4 -3 = 1 of B: +6 -3 = +3.  
9. In het geval van A maakt het systeem een voorwaarts geplande order die begint op de datum **Da**. In het geval van B wordt het bestelpunt bereikt en wordt een nieuwe order gemaakt.

## De rol van het tijdsinterval

Het doel van het tijdsinterval is vraaggebeurtenissen binnen een periode te verzamelen om een gezamenlijke aanvulorder te maken.  

Voor bestelbeleid dat een bestelpunt gebruikt, kunt u een tijdsinterval opgeven. Tijdsintervallen helpen ervoor te zorgen dat de vraag binnen dezelfde tijdsperiode wordt gecumuleerd. Het systeem controleert vervolgens het effect op de geplande voorraad en of het bestelpunt is gepasseerd.

Als u bestelpunt overschrijdt, wordt een nieuwe aanbodorder voorwaarts gepland vanaf het einde van het tijdsinterval. Tijdsintervallen beginnen op de begindatum van de planning.  

Het tijdsinterval geeft het handmatige proces aan om het voorraadniveau op frequente basis te controleren in plaats van voor elke transactie. U definieert de frequentie (het tijdsinterval). U verzamelt bijvoorbeeld alle artikelbehoeften van een leverancier om een wekelijkse order te plaatsen.  

![Voorbeeld van tijdsinterval in planning.](media/nav_app_supply_planning_2_reorder_cycle.png "Voorbeeld van tijdsinterval in planning")  

Tijdsintervallen worden doorgaans gebruikt om een watervaleffect te voorkomen. Een vereffende rij van vraag en aanbod waarbij bijvoorbeeld een vroege vraag wordt geannuleerd of een nieuwe wordt gemaakt. Het resultaat is dat elke voorzieningenorder (behalve de laatste) opnieuw wordt gepland.

## Onder het overflowniveau blijven

Wanneer de beleidsopties **Maximum aantal** en **Vast bestelaantal** worden gebruikt, richt het planningssysteem zich alleen op de geplande voorraad in het betreffende tijdsinterval. Het kan extra aanbod voorstellen wanneer negatieve vraag of positieve veranderingen in het aanbod plaatsvinden buiten het tijdsinterval. Voor extra aanbod berekent het planningssysteem de hoeveelheid waarmee u het aanbod dient te verminderen. Dit aantal wordt het overflowniveau genoemd. De overflow is beschikbaar als een planningsregel met een actie **Aantal wijzigen (afname)** of **Annuleren** en het volgende waarschuwingsbericht:  

* Let op: De geplande voorraad [xx] is groter dan het overflowniveau [xx] op de Vervaldatum [xx].*  

![Overflowniveau van voorraad.](media/supplyplanning_2_overflow1_new.png "Overflowniveau van voorraad")  

### Het overflowniveau berekenen  

Het overflowniveau wordt op verschillende manieren berekend, afhankelijk van het bestelbeleid.  

#### Maximum aantal

Overflowniveau = maximale voorraad  

> [!NOTE]  
> Als u een minimale bestelhoeveelheid hanteert, wordt deze als volgt toegevoegd:
>
> overflowniveau = maximale voorraad + minimale bestelhoeveelheid.  

#### Vast bestelaantal  

overflowniveau = bestelaantal + bestelpunt  

> [!NOTE]  
> Als de minimale orderbestelhoeveelheid groter is dan het bestelpunt, wordt deze als volgt vervangen:
>
> overloopniveau = bestelhoeveelheid + minimale orderhoeveelheid  

#### Vaste lotgrootte  

Als een ordermeervoud bestaat, wordt het overflowniveau aangepast voor zowel het bestelbeleid Maximum aantal als Vast bestelaantal.  

### De planningsregel met een overflowwaarschuwing maken  

Er wordt een planningsregel gemaakt wanneer door een aanbod de geplande voorraad groter is dan het overflowniveau aan het einde van het tijdsinterval. Om te waarschuwen voor het extra aanbod bevat de planningsregel een waarschuwingsbericht, is het veld **Planningsboodschap accepteren** niet geselecteerd en is de planningsboodschap **Annuleren** of **Aantal wijzigen**.  

#### Het planningsregelaantal berekenen  

De hoeveelheid op een planningsregel wordt als volgt berekend:

planningsregelaantal = huidig aanbodaantal - (geplande voorraad - overflowniveau)  

> [!NOTE]  
> Net als bij alle waarschuwingsregels worden het maximale en het minimale orderaantal en het orderveelvoud genegeerd.  

#### Het type planningsboodschap definiëren  

* Als het planningsregelaantal groter is dan 0, is de planningsboodschap **Aantal wijzigen**.  
* Als het planningsregelaantal gelijk is aan of kleiner is dan 0, is de planningsboodschap **Annuleren**  

#### Het waarschuwingsbericht opstellen  

In het geval van overflow wordt op de pagina **Niet-getraceerde planningselementen** een waarschuwing weergegeven met de volgende informatie:  

* Het geplande voorraadniveau dat de waarschuwing heeft geactiveerd  
* Het berekenende overflowniveau  
* De vervaldatum van de aanbodgebeurtenis  

Voorbeeld: “De verwachte voorraad 120 is hoger dan het overflowniveau 60 op 01-28-23“  

### Voorbeeld van een scenario  

In dit scenario verandert een klant een verkooporder van 70 in 40 stuks tussen twee planningen. De overflowfunctie reduceert de inkoop die werd voorgesteld voor het oorspronkelijke verkoopaantal.  

#### Artikelinstellingen  

|Bestelbeleid|Maximum aantal|  
|-----------------------|------------------|  
|Maximaal bestelaantal|100|  
|Bestelpunt|50|  
|Voorraad|80|  

#### Situatie voor een verkoopafname  

|Evenement|Aantal wijzigen|Geschatte inventaris|  
|-----------|-----------------|-------------------------|  
|Dag één|Geen|80|  
|Verkoop|-70|10|  
|Einde van periode|Geen|10|  
|Nieuwe inkooporder voorstellen|+90|100|  

#### Situatie na verkoopafname  

|Wijzigen|Aantal wijzigen|Geschatte inventaris|  
|------------|-----------------|-------------------------|  
|Dag één|Geen|80|  
|Verkoop|-40|40|  
|Inkoop|+90|130|  
|Einde van periode|Geen|130|  
|Voorstellen om inkoop te verminderen<br><br> van 90 naar 60|-30|100|  

#### Resulterende planningsregels  

Het systeem maakt een waarschuwingsplanningsregel om de inkoop met 30 te reduceren, van 90 tot 60, om de geplande voorraad op 100 te houden, op basis van het overflowniveau.  

![Plannen volgens overloopniveau.](media/nav_app_supply_planning_2_overflow2.png "Plannen volgens overloopniveau")  

> [!NOTE]  
> Zonder de overflowfunctie wordt er geen waarschuwing gemaakt als het geplande voorraadniveau boven het maximum ligt, wat een extra aanbod van 30 zou kunnen veroorzaken.

## Voorspelde negatieve voorraad afhandelen

Het bestelpunt drukt de verwachte vraag uit tijdens de doorlooptijd van het artikel. De geplande voorraad moet groot genoeg zijn om de vraag te dekken totdat de nieuwe order wordt ontvangen. In de tussentijd moet de veiligheidsvoorraad zorgen voor schommelingen in de vraag tot aan een bepaald serviceniveau.  

Het planningssysteem beschouwt het als een noodgeval als een toekomstige vraag niet kan worden bediend vanuit de geplande voorraad. Of, op een andere manier uitgedrukt, dat de geplande voorraad negatief wordt. Het systeem stelt voor dat u een nieuwe aanvulorder maakt om het onvervulde deel van de vraag te dekken. De grootte van de nieuwe aanvulorder houdt geen rekening met de maximale voorraad of de bestelhoeveelheid, noch met de volgende ordermodificaties:

* Max. bestelaantal
* Min. bestelaantal
* Vaste lotgrootte 

In plaats hiervan is dit het exacte tekort.  

De planningsregel voor deze aanvulorder geeft een waarschuwingspictogram **Noodgeval** weer met extra gegevens over de situatie.  

In de volgende afbeelding staat aanbod D voor een noodorder om een correctie uit te voeren voor negatieve voorraad.  

![Suggestie voor noodplanning om negatieve inventaris te voorkomen.](media/nav_app_supply_planning_2_negative_inventory.png "Suggestie voor noodplanning om negatieve inventaris te voorkomen")  

1. Aanbod **A**, de oorspronkelijk geplande voorraad, is onder het bestelpunt.  
2. Er is een nieuwe voorwaarts-geplande voorziening gemaakt (**C**).  

     (aantal = maximale voorraad – gepland voorraadniveau)  
3. Aanbod **A** wordt afgesloten door vraag **B**, die niet volledig is verwerkt.  

     (Vraag **B** zou kunnen proberen Aanbod C in te plannen, maar het tijdsinterval voorkomt dat.)  
4. Er wordt nieuw aanbod (**D**) gemaakt om te voldoen aan het resterende aantal van de vraag **B**.  
5. Vraag **B** wordt gesloten (waarbij een aanmaning voor de geplande voorraad wordt gemaakt).  
6. De nieuwe voorziening **D** is afgesloten.  
7. Geplande voorraad wordt gecontroleerd. Het bestelpunt is niet overschreden.  
8. Voorziening **C** is afgesloten (er bestaat geen vraag meer).  
9. Laatste controle. Er bestaan geen openstaande voorraadniveau-aanmaningen.  

In het volgende gedeelte worden de kenmerken van de vier ondersteunde soorten bestelbeleid beschreven.

## Bestelbeleid

Met het bestelbeleid wordt bepaald hoeveel wordt besteld wanneer het artikel moet worden aangevuld. Er zijn vier verschillende soorten bestelbeleid.  

### Vast bestelaantal

Het beleid Vast bestelaantal wordt doorgaans gebruikt voor voorraadplanning voor artikelen met de volgende kenmerken:

* Lage voorraadkosten
* Laag risico op veroudering
* Klein aantal artikelen

Dit beleid wordt gewoonlijk gebruikt met een bestelpunt dat de verwachte vraag weerspiegelt tijdens de doorlooptijd van het artikel.  

#### Berekend per tijdsinterval  

Als u het bestelpunt in een tijdsinterval (bestelcyclus) bereikt of passeert, stelt het systeem twee acties voor:

* Een nieuwe aanvulorder voor de bestelhoeveelheid maken
* De order vooruit plannen vanaf de eerste datum na het einde van het tijdsinterval  

Het bestelpunt met tijdsinterval vermindert het aantal aanbodvoorstellen. Het weerspiegelt een proces van handmatig controleren op de werkelijke inhoud van bakken in uw magazijn.  

#### Maakt alleen benodigd aanbod  

Voordat het een nieuwe aanvulorder voorstelt om aan een bestelpunt te voldoen, controleert het planningssysteem op het volgende aanbod:

* Of er al aanbod is besteld
* Of u verwacht het aanbod binnen de doorlooptijd van het artikel te ontvangen

Het systeem stelt geen nieuwe aanvulorder voor als een aanbod de verwachte voorraad binnen de doorlooptijd naar het bestelpunt brengt.  

Aanvulorders die specifiek zijn gemaakt om te voldoen aan een bestelpunt, worden uitgesloten van de aanbodafstemming en worden niet gewijzigd. Als u een artikel met een bestelpunt wilt uitfaseren, controleert u uw uitstaande aanvulorders handmatig of wijzigt u het bestelbeleid in **Lot-voor-Lot**. Het systeem vermindert of annuleert extra aanbod.  

#### Combineert met ordermodificaties  

De ordermodificaties Min. bestelaantal, Max. bestelaantal en Vaste lotgrootte zouden geen grote rol moeten afspelen wanneer u het beleid Vast bestelaantal gebruikt. Het planningssysteem houdt er echter rekening mee:

* Verlaag de hoeveelheid tot de opgegeven maximale bestelhoeveelheid (en maak twee of meer aanbodhoeveelheden om de totale bestelhoeveelheid te bereiken)
* Verhoog de order tot de opgegeven minimale bestelhoeveelheid
* Rond de orderhoeveelheid naar boven af om aan een opgegeven orderveelvoud te voldoen  

#### Combineert met agenda's  

Voordat een nieuwe aanvulorder wordt voorgesteld om aan een bestelpunt te voldoen, controleert het planningssysteem of de order is gepland voor een niet-werkdag. Het gebruikt de agenda's die u opgeeft in het veld **Basisagendacode** op de pagina's **Bedrijfsgegevens** en **Vestiging**.  

Als de geplande datum een vrije dag is, verplaatst het planningssysteem de order voorwaarts naar de dichtstbijzijnde werkdag. De datum verplaatsen kan resulteren in een order die voldoet een bestelpunt maar aan een bepaalde vraag niet voldoet. Voor dergelijke vraag in onbalans maakt het systeem een extra voorziening.  

#### Moet niet worden gebruikt met prognoses  

Omdat de verwachte vraag al is uitgedrukt in het bestelpuntniveau, is het niet nodig een prognose in de planning op te nemen. Als het belangrijk is dat de planning op een prognose wordt gebaseerd, gebruikt u het beleid **Lot-voor-lot**.  

#### Moet niet met reserveringen worden gebruikt  

Als u een aantal hebt gereserveerd, bijvoorbeeld een aantal in voorraad, voor een toekomstige vraag, wordt de basis van de planning mogelijk verstoord. Zelfs als de geplande voorraad met betrekking tot het bestelpunt aanvaardbaar is, zijn de hoeveelheden mogelijk niet beschikbaar. Het systeem kan proberen dit te compenseren door uitzonderingsorders te maken. We raden echter aan om het veld **Reserveren** in te stellen op **Nooit** voor artikelen die zijn gepland met behulp van een bestelpunt.

### Maximum aantal

Het beleid Maximum aantal is een manier om voorraad bij te houden met behulp van een bestelpunt.  

Alles over het beleid voor een vast bestelaantal geldt ook voor dit beleid. Het enige verschil is de hoeveelheid van de voorgestelde voorziening. Wanneer u het beleid voor maximaal aantal gebruikt, wordt het bestelaantal dynamisch bepaald op basis van het geplande voorraadniveau. Daarom verschilt het meestal van order tot order.  

#### Berekenen per tijdsinterval

Wanneer u het bestelpunt bereikt of overschrijdt, bepaalt het systeem de bestelhoeveelheid aan het einde van een tijdsinterval. Het meet de kloof tussen het huidige geplande voorraadniveau en de opgegeven maximale voorraad om de te bestellen hoeveelheid te bepalen. Het systeem controleert vervolgens:

* Of er al aanbod is besteld
* Of u verwacht het aanbod binnen de doorlooptijd van het artikel te ontvangen

Als dit het geval is, verlaagt het systeem de hoeveelheid van de nieuwe aanvulorder met de reeds bestelde hoeveelheden.  

Als u geen maximale voorraadhoeveelheid opgeeft, zorgt het planningssysteem ervoor dat de geplande voorraad de bestelhoeveelheid bereikt.

#### Combineren met ordermodificaties

Afhankelijk van uw instelling is het misschien het beste om het beleid voor maximale hoeveelheid te combineren met ordermodificaties:

* Zorgen voor een minimaal orderaantal
* Rond de hoeveelheid af op een geheel aantal inkoopmaateenheden
* Verdeel de hoeveelheid in partijen zoals gedefinieerd door de maximale orderhoeveelheid  

### Combineren met agenda's

Voordat een nieuwe aanvulorder wordt voorgesteld om aan een bestelpunt te voldoen, controleert het planningssysteem of de order is gepland voor een niet-werkdag. Het gebruikt de agenda's die u opgeeft in het veld **Basisagendacode** op de pagina's **Bedrijfsgegevens** en **Vestiging**.  

Als de geplande datum een vrije dag is, verplaatst het planningssysteem de order voorwaarts naar de dichtstbijzijnde werkdag. De datum verplaatsen kan resulteren in een order die voldoet een bestelpunt maar aan een bepaalde vraag niet voldoet. Voor dergelijke vraag in onbalans maakt het systeem een extra voorziening.

### Volgorde

In een op-order-produceren omgeving wordt een artikel ingekocht of geproduceerd om aan een specifieke vraag te voldoen. Het bestelbeleid Order wordt doorgaans gebruikt voor artikelen met de volgende kenmerken

* Vraag is niet frequent
* De doorlooptijd is onbeduidend
* Vereiste kenmerken variëren  

[!INCLUDE [prod_short](includes/prod_short.md)] maakt een order-naar-order-koppeling die fungeert als voorlopige verbinding tussen het aanbod (een aanvulorder of voorraad) en de vraag. U kunt de order-naar-order koppeling tijdens de planning op de volgende manieren toepassen:  

* Wanneer u het productiebeleid Op order produceren gebruikt om productieorders met meerdere niveaus of projecttypen te maken (waarbij benodigde materiaal op dezelfde productieorder worden geproduceerd)  
* Wanneer u verkooporderplanning gebruikt om een productieorder te maken van een verkooporder  

> [!TIP]
> Als artikelkenmerken niet variëren, is het misschien het beste om een lot-voor-lot-bestelbeleid te gebruiken. Hierdoor gebruikt het systeem niet-geplande voorraad en worden verkooporders alleen gecumuleerd met dezelfde verzenddatum of binnen een bepaalde periode.  

#### Order-naar-order koppelingen en overschreden vervaldatums

In tegenstelling tot de meeste combinaties van voorziening en vraag, worden gekoppelde orders met vervaldatums voor de begindatum van de planning, volledig door het systeem gepland. De reden voor deze uitzondering is dat specifieke vraag-voorzieningcombinaties moeten worden gesynchroniseerd. Zie voor meer informatie over de vaste zone die voor de meeste vraag/aanbodtypen geldt, [Orders verwerken vóór de startdatum van de planning](design-details-balancing-demand-and-supply.md#process-orders-before-the-planning-start-date).

### Lot-for-Lot

Het beleid Lot-voor-lot is het meest flexibel omdat het systeem alleen reageert op de daadwerkelijke vraag. Het handelt op de verwachte vraag van prognose- en raamcontracten en regelt vervolgens de orderhoeveelheid op basis van de vraag. Het lot-voor-lot beleid is bedoeld voor artikelen waar voorraad kan worden geaccepteerd maar vermeden moet worden.  

In sommige opzichten is het Lot-for-Lot-beleid vergelijkbaar met het bestelbeleid. Het kan hoeveelheden in voorraad accepteren en het bundelt vraag en aanbod in de tijdsintervallen die u definieert.

U specificeert het tijdsinterval in het veld **Tijdsinterval** op de pagina **Artikel**. De minimale grootte van een tijdsinterval is één dag, omdat dat de kleinste tijdseenheid is voor vraag- en aanbodgebeurtenissen in [!INCLUDE [prod_short](includes/prod_short.md)].  

Met het tijdsinterval worden ook limieten ingesteld wanneer u een aanbodorder opnieuw moet plannen om te voldoen aan een bepaalde vraag. Aanbod binnen het tijdsinterval wordt opnieuw in of uit gepland om aan de vraag te voldoen. Eerder aanbod zorgt voor extra voorraad en u moet deze annuleren. Voor levering die later is, maakt u een nieuwe aanbodorder.  

Met dit beleid kunt u een veiligheidsvoorraad opgeven om veranderingen in het aanbod op te vangen of om aan een plotselinge vraag te voldoen. Het lot-voor-lot-beleid kan ook een dempingsperiode en dempingshoeveelheid omvatten om de orderplanning te verminderen.  

Samen met het veld **Herplanningsperiode** draagt het veld **Lotaccumulatieperiode** bij aan de definitie van de bestelcyclus. Vanaf de datum van de eerste vraag worden alle aanvragen in de volgende lotaccumulatieperiode gecumuleerd tot één aanvulorder op de datum van de eerste vraag. Vraag buiten de lotaccumulatieperiode wordt niet gedekt door de aanvulorder.

Omdat de aanvulorderhoeveelheid is gebaseerd op de werkelijke vraag, kan het zinvol zijn om ordermodificaties te gebruiken:

* Rond de bestelhoeveelheid naar boven af om te voldoen aan een orderveelvoud (of maateenheid)
* Verhoog de order tot een opgegeven minimale orderhoeveelheid
* Verlaag de hoeveelheid tot de opgegeven maximale hoeveelheid (en maak dus twee of meer aanbodhoeveelheden om de totale benodigde hoeveelheid te bereiken)

## Zie ook  

[Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md)  
[Ontwerpdetails: Tabel Planningstoewijzing](design-details-planning-assignment-table.md)  
[Ontwerpdetails: Centrale begrippen van het planningssysteem](design-details-central-concepts-of-the-planning-system.md)  
[Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md)  
[Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
