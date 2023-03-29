---
title: 'Ontwerpdetails: Centrale begrippen van het planningssysteem'
description: De planningsfunctie stelt mogelijke acties voor die de gebruiker kan ondernemen op basis van de vraag/aanbod-situatie en de planningsparameters van de artikelen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
---
# Ontwerpdetails: Centrale begrippen van het planningssysteem

De planningsfuncties bevinden zich in een batchverwerking die eerst de relevante artikelen en periode selecteert voor de planning. Vervolgens roept de batchverwerking, op basis van de low-levelcode (stuklijstpositie) van elk artikel, een code-eenheid aan die een aanbodplan berekent. De code-eenheid stemt vraag/aanbod-combinaties af en stelt acties voor die de gebruiker kan ondernemen. De voorgestelde acties worden als regels weergegeven in het planningsvoorstel of inkoopvoorstel.  

![Inhoud van de pagina Planningsvoorstellen.](media/design_details_central_concepts_of_the_planning_system_planning_worksheets.png "Inhoud van de pagina Planningsvoorstellen")  

De planner van een bedrijf, bijvoorbeeld een inkoper of productieplanner, wordt naar verwachting de gebruiker van het planningssysteem. Het planningssysteem ondersteunt de gebruiker door de uitgebreide maar redelijk eenvoudige berekeningen van een planning uit te voeren. De gebruiker kan zich vervolgens richten op het oplossen van complexere problemen, zoals wanneer zaken afwijken van normaal.  

Het planningssysteem wordt gestuurd door de verwachte en werkelijke vraag van klanten, zoals prognoses en verkooporders. Planningsberekeningen suggereren acties die u kunt ondernemen met betrekking tot aanbod van leveranciers, assemblage of productie, of transfers vanuit andere magazijnen. Een voorbeeld van een voorgestelde actie is het maken van nieuwe aanbodorders, zoals inkoop- of productieorders. Als er al aanbodorders zijn, kunnen de voorgestelde acties bestaan uit het vergroten of versnellen van orders om te voorzien in veranderingen in de vraag.  

Een ander doel van het planningssysteem is ervoor te zorgen dat de voorraad niet onnodig toeneemt. Als de vraag afneemt, zal het planningssysteem voorstellen dat de gebruiker bestaande aanvulorders uitstelt, in omvang verkleint of annuleert.  

Een code-eenheid bevat de planningslogica en de volgende functies:

* MRP en MPS
* Mutatieplan berekenen
* Regeneratief plan berekenen

De berekening van het aanbodplan betreft echter verschillende subsystemen.  

Het planningssysteem bevat geen speciale logica voor capaciteitsniveaus of nauwkeurige planning. Dit soort planningswerk wordt afzonderlijk gedaan. Het ontbreken van directe integratie tussen de twee gebieden betekent ook dat aanzienlijke wijzigingen in capaciteit of de planning vereisen dat u de planning opnieuw uitvoert.  

## Planningsparameters

De planningsparameters die u instelt voor een artikel of een groep artikelen, bepalen welke acties het planningssysteem voorstelt in verschillende situaties. Definieer planningsparameters voor elk artikel om te bepalen wanneer, hoeveel en hoe er wordt aangevuld.  

U kunt ook planningsparameters definiëren voor elke combinatie van artikel, vestiging en variant door een SKU voor elke benodigde combinatie in te stellen en vervolgens afzonderlijke parameters op te geven. Zie voor meer informatie [Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md) en [Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md).  

## Begindatum planning

Het planningssysteem helpt u te voorkomen dat u in het verleden openstaande orders hebt en voorgestelde acties hebt die niet mogelijk zijn. Planning behandelt alle datums vóór de startdatum als een bevroren zone. De volgende regel geldt voor de vaste zone:  

* Alle vraag en aanbod vóór de begindatum van de planningsperiode wordt beschouwd als deel van de voorraad of als verzonden. Met andere woorden, er wordt vanuit gegaan dat de planning voor het verleden wordt uitgevoerd op basis van de opgegeven planning Zie voor meer informatie [Orders verwerken vóór de startdatum van de planning](design-details-balancing-demand-and-supply.md#process-orders-before-the-planning-start-date).  

## Dynamische ordertracering (tracering van de behoefte)

Dynamische ordertracering en het gelijktijdig maken van planningsboodschappen in het planningsvoorstel maakt geen deel uit van het aanbodplanningssysteem. Wanneer vraag of aanbod wordt gemaakt of gewijzigd, worden met dynamische ordertracering de vraag en de aantallen gekoppeld om die in real-time te dekken.  

Als u bijvoorbeeld een verkooporder invoert of wijzigt, zoekt het dynamisch ordertraceringssysteem direct aanbod om aan de vraag te voldoen. Het aanbod kan uit voorraad zijn of uit een verwachte aanbodorder (zoals een inkooporder of productieorder). Wanneer het een aanbodbron vindt, koppelt [!INCLUDE [prod_short](includes/prod_short.md)] de vraag en het aanbod. U opent de koppeling op alleen-lezen pagina's vanuit de documentregels. Wanneer geen aanbod kan worden gevonden, maakt het dynamische ordertraceringssysteem planningsboodschappen in het planningsvoorstel met aanbodplanvoorstellen.  

Dynamische ordertracering helpt u te beoordelen of u suggesties voor aanvulorders accepteert. Aan de aanbodzijde toont het de vraag die het aanbod heeft gecreëerd. Aan de vraagzijde identificeert het het aanbod dat door de vraag moet worden gedekt.  

:::image type="content" source="media/nav_app_supply_planning_1_dynamic_order_tracking.png" alt-text="Voorbeeld van dynamische ordertracering.":::

Zie voor meer informatie [Ontwerpdetails: Reservering, ordertracering en planningsboodschappen](design-details-reservation-order-tracking-and-action-messaging.md)  

In bedrijven met een lage artikelstroom en minder geavanceerde productstructuren kan het goed zijn dynamische ordertracering te gebruiken voor aanbodplanning. In drukkere omgevingen moet het planningssysteem echter worden gebruikt om te zorgen voor een evenwichtig aanbodplan.  

### Dynamische ordertracering tegenover het planningssysteem

Het kan moeilijk zijn onderscheid te maken tussen het planningssysteem en dynamische ordertracering. Beide functies geven output in het planningsvoorstel weer door acties voor te stellen die de planner moet uitvoeren. De manier waarop deze output wordt geproduceerd verschilt echter.  

Het planningssysteem behandelt het volledige vraag- en aanbodpatroon van een artikel. Het houdt rekening met alle niveaus van de stuklijsthiërarchie langs de tijdlijn. Dynamische ordertracering richt zich alleen op de situatie van de order die deze heeft geactiveerd. Bij het afstemmen van vraag en aanbod maakt het planningssysteem koppelingen in een door de gebruiker geactiveerde batchmodus. Dynamische ordertracering maakt de koppelingen automatisch wanneer u een vraag of een aanbod invoert. Bijvoorbeeld wanneer u een verkoop- of inkooporder maakt.  

Tijdens dynamische ordertracering worden koppelingen gecreëerd tussen vraag en aanbod op basis van wie het eerst komt, het eerst maalt. Dit kan leiden tot verstoring van prioriteiten. Een als eerste ingevoerde verkooporder met een vervaldatum volgende maand kan bijvoorbeeld worden gekoppeld aan het aanbod in voorraad. De volgende verkooporder die morgen vervalt, kan een planningsboodschap veroorzaken om een nieuwe inkooporder te maken om deze te dekken. De volgende afbeelding toont dit scenario.  

:::image type="content" source="media/nav_app_supply_planning_1_dynamic_order_tracking_graph.png" alt-text="Voorbeeld van ordertracering in leveringsplanning 1.":::

Het planningssysteem behandelt vraag en aanbod voor artikelen in een geprioriteerde volgorde. De order wordt geprioriteerd op basis van vervaldatums en ordertypes. Dat wil zeggen: wie het eerst nodig heeft, het eerst maalt. Het verwijdert alle ordertraceringskoppelingen die dynamisch zijn gemaakt en maakt ze opnieuw op basis van de prioriteit van de vervaldatum. Wanneer het planningssysteem is uitgevoerd, zijn alle verstoringen van het evenwicht tussen vraag en voorziening opgelost, zoals hieronder wordt aangegeven voor dezelfde gegevens.

:::image type="content" source="media/nav_app_supply_planning_1_planning_graph.png" alt-text="Voorbeeld van ordertracering in leveringsplanning 2.":::  

Nadat u de planning hebt uitgevoerd, bevat de tabel Planningsboodschappost geen planningsboodschappen. Die berichten worden vervangen door de acties die worden voorgesteld in het planningswerkblad. Zie voor meer informatie [Ordertraceringskoppelingen tijdens een planning](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-are-loaded-by-specification-level).  

## Volgorde en prioriteit in planning

De volgorde van berekeningen in uw plan is belangrijk om de taak binnen een redelijke tijd te voltooien. De prioriteit van vereisten en resources speelt ook een belangrijke rol in het behalen van de beste resultaten.  

Het planningssysteem wordt gestuurd door vraag. Artikelen op hoog niveau moeten vóór artikelen op laag niveau worden gepland, omdat deze mogelijk vraag naar artikelen op lager niveau genereren. Plan bijvoorbeeld winkellocaties vóór distributiecentra, omdat de winkellocatie mogelijk vraag vanuit het distributiecentrum omvat. Als een vrijgegeven aanvulorder op een gedetailleerd afstemmingsniveau een verkooporder kan dekken, zou het systeem geen nieuwe aanvulorder moeten maken. Een aanbod met een specifiek lotnummer moet ook niet worden toegewezen om aan algemene vraag te voldoen als er andere vraag bestaat die deze specifieke lot vereist.  

### Prioriteit/low-levelcode artikel

In een productieomgeving leidt de vraag naar een voltooid, verkoopbaar artikel tot afgeleide vraag naar onderdelen die het voltooide artikel vormen. De stuklijststructuur bepaalt de onderdeelstructuur en kan verschillende niveaus half afgewerkte artikelen verwerken. Een artikel op één niveau plannen leidt tot afgeleide vraag naar materiaal op het volgende niveau. Uiteindelijk leidt deze hiërarchie tot afgeleide vraag naar ingekochte artikelen. Het planningssysteem plant voor artikelen in volgorde van rangschikking in de totale stuklijsthiërarchie. Het systeem begint met voltooide verkoopbare artikelen op het hoogste niveau en gaat omlaag in de productstructuur naar de artikelen op lager niveau (volgens de low-levelcode).  

De volgende afbeelding toont de volgorde waarin [!INCLUDE [prod_short](includes/prod_short.md)] aanvulorders op het hoogste niveau voorstelt. Het gaat ervan uit dat de suggesties zijn geaccepteerd en toont ook artikelen op een lager niveau.

:::image type="content" source="media/nav_app_supply_planning_1_bom_planning.png" alt-text="Planning voor stuklijsten.":::

Zie voor meer informatie over productieoverwegingen [Voorraadprofielen laden](design-details-balancing-demand-and-supply.md#load-inventory-profiles).  

#### Prestaties optimaliseren voor berekeningen op laag niveau

Codeberekeningen op laag niveau kunnen de systeemprestaties beïnvloeden. Om de impact te verminderen kunt u **Dynamische codeberekening op laag niveau** uitschakelen op de pagina **Productie-instellingen**. Als u dat doet, zal [!INCLUDE[prod_short](includes/prod_short.md)] voorstellen dat u een terugkerend taakwachtrij-item maakt dat dagelijks low-level codes bijwerkt. U kunt ervoor zorgen dat de taak buiten werktijd wordt uitgevoerd door een starttijd op te geven in het veld **Vroegste begindatum/-tijd**.

U kunt codeberekeningen op laag niveau versnellen door **Berekening van low-levelcode optimaliseren** in te schakelen op de pagina **Productie-instellingen**.

> [!IMPORTANT]
> Als u ervoor kiest om de prestaties te optimaliseren, zal [!INCLUDE[prod_short](includes/prod_short.md)] nieuwe berekeningsmethoden gebruiken om low-levelcodes te bepalen. Als u een extensie hebt die afhankelijk is van de gebeurtenissen die door de oude berekeningen worden gebruikt, werkt de extensie mogelijk niet meer.

### Prioriteit op niveau van vestigingen/transfers

Bedrijven die in meerdere vestigingen actief zijn, moeten mogelijk voor elke vestiging afzonderlijk plannen. Het veiligheidsvoorraadniveau van een artikel en het bestelbeleid ervan kunnen bijvoorbeeld van vestiging tot vestiging verschillen U dient de planningsparameters per artikel en vestiging op te geven.  

U kunt SKU's gebruiken om individuele planningsparameters op te geven. Een SKU kan worden gezien als een artikel op een bepaalde locatie. Als u geen SKU voor die vestiging hebt gedefinieerd, gebruikt [!INCLUDE [prod_short](includes/prod_short.md)] de parameters die op de artikelkaart zijn ingesteld. [!INCLUDE [prod_short](includes/prod_short.md)] berekent alleen een plan voor actieve locaties, waar vraag of aanbod is voor een bepaald artikel.  

Elk artikel kan op elke vestiging worden afgehandeld, maar [!INCLUDE [prod_short](includes/prod_short.md)] heeft een strikte benadering van het concept van vestigingen. Een verkooporder voor een artikel op de ene vestiging kan bijvoorbeeld niet worden afgehandeld door voorraad op een andere vestiging. Het aantal op voorraad moet eerst worden overgebracht naar de vestiging die op de verkooporder is opgegeven.

:::image type="content" source="media/nav_app_supply_planning_1_sku_planning.png" alt-text="Planning van SKU's.":::

Zie voor meer informatie [Ontwerpdetails - Transfers in planning](design-details-transfers-in-planning.md)  

### Orderprioriteit

Binnen een bepaalde SKU staat de verzochte of beschikbare datum voor de hoogste prioriteit; de vraag van vandaag moet worden verwerkt vóór de vraag van de eerstvolgende dagen. Afgezien van dit type prioriteit worden de verschillende soorten vraag en aanbod gesorteerd op basis van bedrijfsbelang om te beslissen aan welke vraag eerst moet worden voldaan. Aan de aanbodzijde bepaalt de orderprioriteit welke aanbodbron als eerste wordt toegepast. Zie voor meer informatie [Orders prioriteit geven](design-details-balancing-demand-and-supply.md#prioritize-orders).  

## Vraagprognoses en raamcontracten

Prognoses en raamcontracten vertegenwoordigen beide verwachte vraag. Het raamcontract omvat de bedoelde inkoop van een klant over een bepaalde periode en is bedoeld om de onzekerheid van de algemene prognose te verminderen. Het raamcontract is een klantspecifieke prognose in aanvulling op de ongespecificeerde prognose beschreven in de volgende afbeelding.  

:::image type="content" source="media/nav_app_supply_planning_1_forecast_and_blanket.png" alt-text="Planning met prognoses.":::

Zie voor meer informatie [Prognosevraag wordt verlaagd door verkooporders](design-details-balancing-demand-and-supply.md#forecast-demand-is-reduced-by-sales-orders).  

## Planningsopdracht

Alle artikelen moeten opnieuw worden gepland voor wanneer het vraag- of aanbodpatroon is gewijzigd sinds de laatste keer dat een plan werd berekend. Als u bijvoorbeeld een nieuwe verkooporder invoert of een bestaande wijzigt, berekent u het plan opnieuw. Andere redenen om opnieuw te plannen omvatten een wijziging in de voorspelde hoeveelheid of de hoeveelheid van de veiligheidsvoorraad. Het wijzigen van een stuklijst door een materiaal toe te voegen of te verwijderen duidt waarschijnlijk op een wijziging, maar alleen voor het materiaalartikel.  

Het planningssysteem bewaakt dergelijke gebeurtenissen en wijst de benodigde artikelen toe aan de planning.  

Voor meerdere vestigingen vindt de toewijzing plaats op het artikelniveau per vestigingscombinatie. Wanneer bijvoorbeeld een verkooporder op slechts één vestiging is gemaakt, wijst [!INCLUDE [prod_short](includes/prod_short.md)] het artikel in die specifieke vestiging voor planning toe.  

De reden voor het selecteren van artikelen voor planning heeft te maken met systeemprestaties. Als er geen verschil is opgetreden in het vraag/aanbod-patroon van een artikel, zal het planningssysteem geen uit te voeren acties voorstellen. Zonder de planningstoewijzing moet het systeem de berekeningen voor alle artikelen uitvoeren om te weten waarvoor moet worden gepland. Ga voor meer informatie over de redenen om artikelen toe te wijzen voor planning naar [Ontwerpdetails: Tabel Planningstoewijzing](design-details-planning-assignment-table.md).  

Hieronder worden de beschikbare planningsopties beschreven.  

* **Regeneratief plan berekenen**: berekent alle geselecteerde artikelen, of het nodig is of niet.  
* **Mutatieplan berekenen**: berekent alleen de artikelen die een wijziging hebben ondergaan in het vraag/aanbod-patroon en daarom zijn toegewezen voor planning.  

Sommige gebruikers zijn van mening dat de mutatieplanning ad hoc moet worden uitgevoerd, bijvoorbeeld wanneer verkooporders worden ingevoerd. Dit kan echter verwarrend zijn omdat dynamische ordertracering en planningsboodschappen ook ad hoc worden berekend. [!INCLUDE[prod_short](includes/prod_short.md)] biedt real-time ATP-controle. Het geeft pop-upwaarschuwingen wanneer u verkooporders invoert en het huidige aanbodplan niet aan de vraag kan voldoen.  

Het planningssysteem plant alleen de artikelen die u hebt voorbereid met de juiste planningsparameters. Anders wordt ervan uitgegaan dat u de artikelen handmatig of semiautomatisch plant met de functie Orderplanning. Zie voor meer informatie over de automatische planningsprocedures [Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md).  

## Artikeldimensies

Vraag en voorziening kunnen variantcodes en vestigingscodes hebben die moeten worden gerespecteerd wanneer het planningssysteem vraag en aanbod afstemt.  

[!INCLUDE [prod_short](includes/prod_short.md)] behandelt variant- en vestigingscodes als artikeldimensies op een verkooporderregel, in een voorraadpost, enzovoort. Er wordt een planning berekend voor elke combinatie van variant en locatie, alsof de combinatie een apart artikelnummer is.  

In plaats van theoretische combinaties van vestiging en variant te berekenen, berekent [!INCLUDE [prod_short](includes/prod_short.md)] alleen de combinaties die werkelijk voorkomen in de database. Zie [Ontwerpdetails: Vraag op lege vestiging](design-details-balancing-demand-and-supply.md) voor meer informatie over de manier waarop het planningssysteem omgaat met vestigingscodes bij vraag.  

## Artikelkenmerken

Artikelen hebben vaak algemene kenmerken, zoals een artikelnummer, variantcode, vestigingscode en ordertype. Elke vraag- en aanbodgebeurtenis kan echter andere specificaties hebben, zoals serie- of lotnummers. Het planningssysteem plant deze kenmerken op bepaalde manieren, afhankelijk van het specificatieniveau.  

Een order-aan-order koppeling tussen vraag en aanbod is een ander soort kenmerk dat van invloed is op het planningssysteem. Zie voor meer informatie [Oder-naar-order koppelingen](#order-to-order-links).

### Specifieke kenmerken

Sommige vraagkenmerken zijn specifiek en een aanbod moet daar exact op aansluiten.

* Serie- of lotnummers die specifieke vereffening vereisen (Deze kenmerken zijn vereist als u **Specifieke serienr.-tracering** of **Specifieke lottracering** inschakelt op de pagina **Artikeltraceringscode** voor de artikeltraceringscode die door het artikel wordt gebruikt).  
* Koppelingen naar voorzieningenorders die handmatig of automatisch worden gemaakt voor bepaalde vraag (order-naar-order koppelingen).  

Het planningssysteem past de volgende regels toe op deze kenmerken:  

* Aan vraag met bepaalde kenmerken kan alleen worden voldaan door aanbod met overeenkomende kenmerken.  
* Aanbod met specifieke kenmerken kan ook voldoen aan vraag die niet specifiek deze kenmerken vereist.  

Als voorraad of voorspeld aanbod niet aan een vraag naar specifieke kenmerken kan voldoen, stelt het planningssysteem een nieuwe aanbodorder voor zonder rekening te houden met planningsparameters.  

### Niet-specifieke kenmerken

Artikelen met serie- of lotnummers zonder specifieke instelling voor artikeltracering kunnen niet-specifieke serie- of lotnummers hebben. Dit soort nummers kan op elk serie- of lotnummer worden toegepast. Het planningssysteem heeft meer vrijheid om bijvoorbeeld een vraag met serienummers af te stemmen op een aanbod met serienummers, doorgaans in voorraad.  

Vraag-aanbod met serie- of lotnummers, specifiek of niet-specifiek, heeft hoge prioriteit en is vrijgesteld van de bevroren zone. Ze maken deel uit van de planning, zelfs als de vervaldatum ervan vóór de startdatum van de planning ligt. Zie voor meer informatie [Serie-/lotnummers worden geladen per specificatieniveau](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-are-loaded-by-specification-level).

Zie voor meer informatie over hoe het planningssysteem kenmerken afstemt [Serie-/lotnummers en order-naar-order koppelingen zijn vrijgesteld van de vorige periode](design-details-balancing-demand-and-supply.md#serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period).  

## Order-naar-order koppelingen

Order-naar-order betekent dat u een artikel koopt, assembleert of produceert voor een specifieke vraag. Er zijn verschillende redenen om voor dit beleid te kiezen:

* De vraag is zeldzaam.
* De doorlooptijd is onbeduidend.
* De vereiste kenmerken variëren.  

Een ander speciaal geval waarin order-naar-order koppelingen worden gebruikt is wanneer een assemblageorder aan een verkooporder wordt gekoppeld in een assembleren-op-order scenario.  

Order-naar-order koppelingen worden op vier manieren toegepast tussen vraag en aanbod:  

* Wanneer het geplande artikel het bestelbeleid **Order** gebruikt  
* Wanneer u het productiebeleid Op order produceren wordt gebruikt om productieorders met meerdere niveaus of projecttypen te maken (waarbij benodigde materiaal voor dezelfde productieorder worden geproduceerd)  
* Wanneer u productieorders maakt voor verkooporders met de functie Verkooporderplanning  
* Wanneer u een artikel assembleert voor een verkooporder (**Assemblagebeleid** is ingesteld op **Op order assembleren**)  

Het planningssysteem stelt voor alleen het vereiste aantal te bestellen. De inkoop-, productie- of assemblageorder blijft aansluiten bij de vraag. Wanneer de tijd of het aantal van een verkooporder bijvoorbeeld verandert, stelt het planningssysteem voor dat u de aanvulorder daaraan aanpast.  

Wanneer order-naar-order koppelingen bestaan, betrekt het planningssysteem geen gekoppeld aanbod of gekoppelde voorraad bij de afstemmingsprocedure. Planners kunnen beslissen of ze het gekoppelde aanbod of een nieuwe vraag gebruiken. In het laatste geval kunnen ze de aanvulorder verwijderen of het gekoppelde aanbod handmatig reserveren.  

Reserveringen en ordertraceringskoppelingen worden verbroken als een situatie onmogelijk wordt. Bijvoorbeeld bij het verplaatsen van de vraag naar een datum die eerder ligt dan het aanbod. Order-naar-order-koppelingen passen zich aan veranderingen in de vraag of het aanbod aan en worden nooit verbroken.  

## Reserveringen

Het planningssysteem houdt in berekeningen geen rekening met gereserveerde aantallen. Als een hoeveelheid voor een verkooporder bijvoorbeeld geheel of gedeeltelijk is gereserveerd, kunt u de hoeveelheid niet gebruiken om aan andere vraag te voldoen.

Het planningssysteem houdt in het voorspelde voorraadprofiel rekening met gereserveerde aantallen. Het moet alle hoeveelheden in overweging nemen om te bepalen wanneer het bestelpunt is gepasseerd en hoeveel er opnieuw moeten worden besteld om het maximale voorraadniveau te bereiken. Overbodige reserveringen kunnen het risico vergroten dat voorraadniveaus laag worden omdat de planningslogica gereserveerde aantallen niet detecteert.  

De volgende afbeelding laat zien hoe reserveringen de planning kunnen belemmeren.  

:::image type="content" source="media/nav_app_supply_planning_1_reservations.png" alt-text="Planning met reserveringen.":::

Zie voor meer informatie [Ontwerpdetails: Reservering, ordertracering en planningsboodschappen](design-details-reservation-order-tracking-and-action-messaging.md)  

## Waarschuwingen

De eerste kolom in het planningsvoorstel is voor de waarschuwingsvelden. Er wordt een waarschuwingspictogram weergegeven wanneer u een planningsregel maakt voor een ongebruikelijke situatie.  

Aanbod op planningsregels met waarschuwingen wordt gewoonlijk niet gewijzigd volgens planningsparameters. In plaats daarvan stelt het planningssysteem alleen een aanbod ter dekking van de exacte hoeveelheid van de vraag voor. Het systeem kan echter zo worden ingesteld dat bepaalde planningsparameters voor planningsregels met bepaalde waarschuwingen worden gerespecteerd. De waarschuwingsgegevens worden op de pagina **Niet-getraceerde planningselementen** weergegeven, die ook ordertraceringskoppelingen toont met niet-order netwerkentiteiten. Er zijn drie soorten waarschuwingen:  

* Noodgeval  
* Uitzondering  
* Opmerking  

:::image type="content" source="media/nav_app_supply_planning_1_warnings.png" alt-text="Waarschuwingen in het planningswerkblad.":::

### Noodgeval

De noodgevalwaarschuwing wordt in twee gevallen weergegeven:  

* Wanneer de voorraad negatief is op de begindatum van de planning  
* Wanneer er geantedateerde aanbod- of vraaggebeurtenissen bestaan  

Als de voorraad van een artikel negatief is op de geplande begindatum, wordt er door het planningssysteem een noodorder voor een voorziening voorgesteld die wordt aangevoerd op de geplande begindatum. De waarschuwing vermeldt de begindatum en de hoeveelheid van de order voor een noodvoorziening. Zie voor meer informatie [Ontwerpdetails: Verwachte negatieve voorraad verwerken](design-details-handling-reordering-policies.md#handling-projected-negative-inventory).  

Documentregels met een vervaldatum vóór de begindatum van de planning worden geconsolideerd in een noodleveringsorder. De order is gepland om te arriveren op de startdatum van de planning.  

### Uitzondering

De uitzonderingswaarschuwing wordt weergegeven als de verwachte beschikbare voorraad onder de veiligheidsvoorraad daalt. Het planningssysteem stelt een order voor een voorziening voor om aan de vraag op de vervaldatum te kunnen voldoen. De waarschuwing vermeldt de veiligheidsvoorraad van het artikel en de datum waarop de voorraad daaronder daalt.  

Het overtreden van de veiligheidsvoorraad is een uitzondering. Dit zou niet moeten gebeuren als het bestelpunt correct is ingesteld. Zie voor meer informatie [De rol van het bestelpunt](design-details-handling-reordering-policies.md#the-role-of-the-reorder-point).  

Uitzonderlijke ordervoorstellen helpen ervoor zorgen dat de verwachte beschikbare voorraad nooit lager is dan de veiligheidsvoorraad. Het voorgestelde aantal is voldoende om de veiligheidsvoorraad te dekken, zonder dat planningsparameters moeten worden overwogen. In sommige scenario's komen orderwijzigingen echter in aanmerking.  

> [!NOTE]  
> Het planningssysteem kan de veiligheidsvoorraad opzettelijk hebben verbruikt en vult deze vervolgens direct aan. Zie voor meer informatie [Veiligheidsvoorraad verbruiken](design-details-balancing-demand-and-supply.md#consume-safety-stock).

### Opmerking

De attentiewaarschuwing wordt in drie gevallen weergegeven:  

* De geplande begindatum is eerder dan de werkdatum.  
* Op de planningsregel wordt voorgesteld een vrijgegeven inkoop- of productieorder te wijzigen.  
* De verwachte voorraad is groter dan het overflowniveau op de vervaldatum. Zie voor meer informatie [Onder het overflowniveau blijven](design-details-handling-reordering-policies.md#stay-below-the-overflow-level).  

> [!NOTE]  
> Bij planningsregels met waarschuwingen wordt het veld **Planningsboodschap accepteren** niet geselecteerd, omdat de planner naar verwachting de regels verder gaat bekijken voordat de planning wordt uitgevoerd.  

## Foutlogboeken

Op de aanvraagpagina **Planning berekenen** kan de gebruiker het veld **Stoppen en eerste fout tonen** selecteren om de planning te laten stoppen wanneer de eerste fout wordt geconstateerd. Er wordt een bericht weergegeven met informatie over de fout. Als er sprake is van een fout, toont het planningsvoorstel alleen de planningsregels die met succes zijn gemaakt voordat de fout optrad.  

Als het veld niet is geselecteerd, wordt de batchverwerking **Planning berekenen** voortgezet totdat deze is voltooid. Fouten onderbreken de batchverwerking niet. Als er fouten zijn, wordt in een bericht aangegeven om hoeveel artikelen het gaat. Vervolgens wordt de pagina **Planningfoutenlogboek** geopend met meer informatie over de fout en koppelingen naar de betreffende documenten of instellingen.  

:::image type="content" source="media/nav_app_supply_planning_1_error_log.png" alt-text="Foutmeldingen in het planningswerkblad.":::

## Planningsflexibiliteit

Het is niet altijd praktisch om een bestaande aanvulorder te plannen. Bijvoorbeeld wanneer de productie is gestart of u op een bepaalde dag extra mensen inhuurt om de klus te klaren. Om aan te geven of een bestaande order kan worden gewijzigd door het planningssysteem, hebben alle aanvulorderregels een veld **Planningsflexibiliteit** met twee opties: **Onbeperkt** of **Geen**. Als het veld is ingesteld op **Geen**, wordt niet geprobeerd de aanvulorderregel te wijzigen.  

U kunt handmatig een optie in het veld kiezen, maar in sommige gevallen wordt het automatisch ingesteld door [!INCLUDE [prod_short](includes/prod_short.md)]. Het feit dat u de planningsflexibiliteit handmatig kunt instellen is belangrijk omdat hierdoor het gebruik van de functie eenvoudig kan worden aangepast aan verschillende werkstromen en bedrijfsgevallen. Zie voor meer informatie over hoe dit veld wordt gebruikt [Ontwerpdetails: Transfers in planning](design-details-transfers-in-planning.md).  

## Orderplanning

De planningfunctie voor algemene voorzieningen wordt weergegeven op de pagina **Orderplanning** en is bedoeld voor handmatige besluitvorming. Deze houdt geen rekening met planningsparameters en wordt daarom niet verder besproken in dit artikel. Zie voor meer informatie [Nieuwe vraag order voor order plannen](production-how-to-plan-for-new-demand.md).  

> [!NOTE]  
> Het is niet raadzaam orderplanning te gebruiken als uw bedrijf al gebruikmaakt van plannings- of inkoopvoorstellen. Orders voor voorzieningen die zijn gemaakt via de pagina **Orderplanning** kunnen worden gewijzigd of verwijderd tijdens de automatisch uitgevoerde planningen. Deze wijzigingen treden op doordat de geautomatiseerde planning planningsparameters gebruikt waar u mogelijk geen rekening hebt gehouden toen u het plan handmatig maakte op de pagina Orderplanning.  

## Beperkte werklast

[!INCLUDE[prod_short](includes/prod_short.md)] biedt een ruwe planning om een redelijk gebruik van middelen te plannen. Het maakt en onderhoudt niet automatisch gedetailleerde planningen op basis van prioriteiten of optimalisatieregels.  

Het beoogde gebruik van de resourcefunctie met beperkte capaciteit is als volgt:

* Om overbelasting van bronnen te voorkomen
* Om ervoor te zorgen dat capaciteit niet niet-toegewezen blijft als dit de doorlooptijd van een productieorder zou kunnen verkorten

Bij het plannen met capaciteitsbegrensde resources zorgt [!INCLUDE [prod_short](includes/prod_short.md)] dat er geen resources boven hun capaciteit (kritieke belasting) worden geladen. Elke bewerking wordt toegewezen aan de dichtstbijzijnde beschikbare periode. Als de periode niet groot genoeg is om de hele bewerking uit te voeren, wordt de bewerking in twee of meer delen gesplitst in de dichtstbijgelegen beschikbare perioden.  

> [!NOTE]  
> In het geval van gesplitste bewerkingen wordt de insteltijd slechts eenmaal toegewezen omdat ervan wordt uitgegaan dat enige handmatige aanpassing wordt uitgevoerd om de planning te optimaliseren.  

U kunt dempingstijd toevoegen aan resources om splitsen van bewerkingen te minimaliseren. Door dempingstijd kan [!INCLUDE [prod_short](includes/prod_short.md)] de belasting plannen op de laatst mogelijke dag door het kritieke belastingpercentage iets te overschrijden.  

## Zie ook

[Ontwerpdetails: Transfers in planning](design-details-transfers-in-planning.md)  
[Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md)  
[Ontwerpdetails: Tabel Planningstoewijzing](design-details-planning-assignment-table.md)  
[Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md)  
[Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
