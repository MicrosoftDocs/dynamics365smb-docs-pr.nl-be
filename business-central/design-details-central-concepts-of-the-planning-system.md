---
title: 'Ontwerpdetails: Centrale begrippen van het planningssysteem | Microsoft Docs'
description: De planningsfuncties bevinden zich in een batchverwerking waarmee eerst de relevante artikelen en periode voor de planning worden geselecteerd en vervolgens mogelijke acties voor de gebruiker worden voorgesteld op basis van de vraag-aanbodsituatie en de planningsparameters van de artikelen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 6cfe028d21086269f1492aefde31fe6b659d06b4
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788133"
---
# <a name="design-details-central-concepts-of-the-planning-system"></a>Ontwerpdetails: Centrale begrippen van het planningssysteem
De planningsfuncties bevinden zich in een batchverwerking die eerst de relevante artikelen en periode selecteert voor de planning. Vervolgens roept de batchverwerking op basis van de low-levelcode van elk artikel (stuklijstpositie) een codeunit aan, die een voorzieningenplan berekent door combinaties van voorziening en vraag in overeenstemming te brengen en mogelijke acties voor de gebruiker voor te stellen. De voorgestelde acties worden als regels weergegeven in het planningsvoorstel of inkoopvoorstel.  

![Inhoud van de pagina Planningwerkblad](media/NAV_APP_supply_planning_1_planning_worksheet.png "Inhoud van de pagina Planningwerkblad")  

De planner van het bedrijf, bijvoorbeeld een inkoper of productieplanner, wordt naar verwachting de gebruiker van het planningssysteem. Het planningssysteem ondersteunt de gebruiker door de uitgebreide maar redelijk eenvoudige berekeningen van een planning uit te voeren. De gebruiker kan zich vervolgens richten op het oplossen van complexere problemen, zoals wanneer zaken afwijken van normaal.  

Het planningssysteem wordt gestuurd door de verwachte en werkelijke vraag van klanten, zoals prognoses en verkooporders. Het uitvoeren van de planningsberekening leidt ertoe dat de toepassing specifieke acties voor de gebruiker voorstelt die ondernomen dienen te worden met betrekking tot mogelijke voorzieningen door leveranciers, assemblage- of productieafdelingen of transfers vanuit andere magazijnen. Deze voorgestelde acties kunnen het maken van nieuwe voorzieningenorders zijn, zoals inkoop- of productieorders. Als er al voorzieningenorders zijn, kunnen de voorgestelde acties bestaan uit het vergroten of versnellen van de orders om te voorzien in veranderingen in de vraag.  

Een ander doel van het planningssysteem is ervoor te zorgen dat de voorraad niet onnodig toeneemt. Als de vraag afneemt, zal het planningssysteem voorstellen dat de gebruiker bestaande voorzieningenorders uitstelt, in omvang verkleint of annuleert.  

MRP en MPS, Mutatieplan berekenen en Regeneratief plan berekenen zijn allemaal functies binnen één codeunit die de planninglogica bevat. De berekening van het voorzieningenplan betreft echter verschillende subsystemen.  

Het planningssysteem bevat geen speciale logica voor capaciteitsniveaus of nauwkeurige planning. Dergelijke planningsactiviteiten worden daarom uitgevoerd als een afzonderlijke discipline. Het ontbreken van directe integratie tussen de twee gebieden betekent ook dat aanzienlijke wijzigingen in capaciteit of het schema vereisen dat de planning opnieuw wordt uitgevoerd.  

## <a name="planning-parameters"></a>Planningsparameters  
Planningsparameters die de gebruiker instelt voor een artikel of een groep artikelen, bepalen welke acties het planningssysteem voorstelt in de verschillende situaties. De planningsparameters worden gedefinieerd op elke artikelkaart om te bepalen wanneer, hoeveel en hoe er wordt aangevuld.  

Planningsparameters kunnen ook voor elke combinatie van artikel, vestiging en variant worden gedefinieerd door een SKU voor elke benodigde combinatie in te stellen en vervolgens afzonderlijke parameters op te geven.  

Zie [Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md) en [Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md) voor meer informatie.  

## <a name="planning-starting-date"></a>Begindatum planning  
Ter voorkoming van een voorzieningenplan dat openstaande orders in het verleden bevat en het voorstellen van potentieel onmogelijke acties behandelt het planningssysteem alle datums voor de begindatum van de planning als een vaste zone waar de volgende speciale regel geldt:  

Alle vraag en aanbod vóór de begindatum van de planningsperiode wordt beschouwd als deel van de voorraad of wordt verzonden.  

Met andere woorden, er wordt vanuit gegaan dat de planning voor het verleden is uitgevoerd op basis van de opgegeven planning  

Zie [Werken met orders vóór de geplande begindatum](design-details-balancing-demand-and-supply.md#dealing-with-orders-before-the-planning-starting-date) voor meer informatie.  

## <a name="dynamic-order-tracking-pegging"></a>Dynamische ordertracering (tracering van de behoefte)  
Dynamische ordertracering met het gelijktijdig maken van planningsboodschappen in het planningsvoorstel maakt geen deel uit van het voorzieningsplanningssysteem in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Deze functie koppelt, in realtime, de vraag en de aantallen die ze kunnen verwerken, wanneer een nieuwe vraag of voorziening wordt gemaakt of gewijzigd.  

Als de gebruiker bijvoorbeeld een verkooporder invoert of wijzigt, zoekt het dynamisch ordertraceringssysteem direct geschikt aanbod om aan de vraag te voldoen. Dit kan uit voorraad zijn of van een verwachte order voor voorzieningen (zoals een inkooporder of productieorder). Wanneer een voorzieningsbron wordt gevonden, wordt een koppeling tussen de vraag en de voorziening gemaakt en weergegeven op alleen-weergavepagina's die toegankelijk zijn via de betreffende documentregels. Wanneer geen passende voorziening kan worden gevonden, maakt het dynamische ordertraceringssysteem planningsboodschappen in het planningsvoorstel met voorstellen voor het voorzieningenplan die de dynamische vereffening aangeven. Het dynamische ordertraceringssysteem biedt een zeer elementair planningssysteem dat nuttig kan zijn voor de planner en voor andere rollen in de interne leveringsketen.  

Dynamische ordertracering kan worden beschouwd als een tool die de gebruiker helpt beoordelen of suggesties voor voorzieningenorders moeten worden geaccepteerd. Van de aanbodzijde kan een gebruiker zien welke vraag tot het aanbod heeft geleid en van de vraagzijde welk aanbod aan de vraag moet voldoen.  

![Voorbeeld van dynamische ordertracering](media/NAV_APP_supply_planning_1_dynamic_order_tracking.png "Voorbeeld van dynamische ordertracering")  

Zie voor meer informatie [Reservering, ordertracering en planningsboodschappen](design-details-reservation-order-tracking-and-action-messaging.md).  

In bedrijven met een lage artikelstroom en minder geavanceerde productstructuren kan het goed zijn de dynamische ordertracering te gebruiken als de belangrijkste manier om voorraad te plannen. In drukkere omgevingen moet het planningssysteem echter altijd worden gebruikt om te zorgen voor een evenwichtig leveringsplan.  

### <a name="dynamic-order-tracking-versus-the-planning-system"></a>Dynamische ordertracering tegenover het planningssysteem  
Op het eerste gezicht kan het moeilijk zijn onderscheid te maken tussen het planningssysteem en dynamische ordertracering. Beide functies geven output in het planningsvoorstel weer door acties voor te stellen die de planner moet uitvoeren. De manier waarop deze output wordt geproduceerd verschilt echter.  

Het planningssysteem verwerkt het volledige vraag-voorzieningpatroon van een bepaald artikel op alle niveaus van de stuklijsthiërarchie op de tijdlijn, terwijl bij dynamische ordertracering alleen de situatie wordt afgehandeld van de order waardoor deze is geactiveerd. Bij het vereffenen van vraag en voorziening maakt het planningssysteem koppelingen in een door de gebruiker geactiveerde batchmodus, terwijl met dynamische ordertracering de koppelingen automatisch en tussendoor worden gemaakt, telkens wanneer de gebruiker een vraag of voorziening in de toepassing invoert, bijvoorbeeld een inkooporder of verkooporder.  

Tijdens dynamische ordertracering worden koppelingen gecreëerd tussen vraag en aanbod wanneer gegevens worden ingevoerd op een first-come/first-served basis. Dit kan leiden tot enige verstoring van prioriteiten. Een verkooporder die eerst is ingevoerd, met een vervaldatum van volgende maand, kan bijvoorbeeld zijn gekoppeld aan het aanbod in voorraad, terwijl de volgende verkooporder die morgen vervalt, ertoe kan leiden dat een planningsboodschap een nieuwe inkooporder maakt om deze te dekken, zoals hieronder geïllustreerd.  

![Voorbeeld van ordertracering in leveringsplanning 1](media/NAV_APP_supply_planning_1_dynamic_order_tracking_graph.png "Voorbeeld van ordertracering in leveringsplanning 1")  

Het planningssysteem werkt echter met alle vraag en aanbod voor een bepaald artikel, in volgorde van prioriteit op basis van vervaldatums en ordersoorten, dat wil zeggen op basis van eerst nodig eerst bediend. Het verwijdert alle ordertraceringskoppelingen die dynamisch zijn gemaakt en maakt ze opnieuw op basis van de prioriteit van de vervaldatum. Wanneer het planningssysteem is uitgevoerd, zijn alle verstoringen van het evenwicht tussen vraag en voorziening opgelost, zoals hieronder wordt aangegeven voor dezelfde gegevens.  

![Voorbeeld van ordertracering in leveringsplanning 2](media/NAV_APP_supply_planning_1_planning_graph.png "Voorbeeld van ordertracering in leveringsplanning 2")  

Na de planning blijven geen planningsboodschappen achter in de tabel Planningsboodschappost, omdat ze door de voorgestelde acties in het planningsvoorstel zijn vervangen.  

Zie Ordertraceringskoppelingen tijdens planning in [Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md#balancing-supply-with-demand) voor meer informatie.  

## <a name="sequence-and-priority-in-planning"></a>Volgorde en prioriteit in planning  
Bij het vaststellen van een plan is de volgorde van de berekeningen belangrijk om de taak binnen een redelijke tijd te voltooien. Bovendien speelt de prioriteitsvolgorde van vereisten en resources een belangrijke rol in het behalen van de beste resultaten.  

Het planningssysteem in [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt gestuurd door de vraag. Artikelen op hoog niveau moeten worden gepland vóór artikelen op laag niveau, omdat de planning voor artikelen op hoog niveau aanvullende vraag kan genereren voor de artikelen op het lagere niveau. Dit betekent bijvoorbeeld dat detailhandelvestigingen moeten worden gepland voordat distributiecentra worden gepland, omdat het plan voor een detailhandelvestiging extra vraag voor het distributiecentrum kan inhouden. Op een gedetailleerd afstemmingsniveau betekent dit ook dat een verkooporder niet tot een nieuwe voorzieningenorder moet leiden als een reeds bestaande voorzieningenorder aan de verkooporder kan voldoen. Zo moet een voorziening met een specifiek lotnummer ook niet worden toegewezen om aan algemene vraag te voldoen als er andere vraag bestaat die deze specifieke lot vereist.  

### <a name="item-priority--low-level-code"></a>Prioriteit/low-levelcode artikel  
In een productieomgeving leidt de vraag naar een voltooid, verkoopbaar artikel tot afgeleide vraag naar onderdelen die het voltooide artikel vormen. De stuklijststructuur bepaalt de onderdeelstructuur en kan verschillende niveaus half afgewerkte artikelen verwerken. Een artikel op één niveau plannen leidt tot afgeleide vraag voor onderdelen op het volgende niveau, enzovoort. Uiteindelijk leidt dit tot afgeleide vraag naar ingekochte artikelen. Daarom plant het planningssysteem voor artikelen in de volgorde van hun rangorde in de totale stuklijsthiërarchie, te beginnen met verkoopbare voltooide artikelen op het hoogste niveau, en dan omlaag door de productstructuur naar de artikelen van het lagere niveau (op basis van de low-levelcode).  

![Planning voor stuklijsten](media/NAV_APP_supply_planning_1_BOM_planning.png "Planning voor stuklijsten")  

De cijfers laten zien in welke volgorde voorstellen worden gemaakt voor voorzieningenorders op het hoogste niveau en, ervan uitgaande dat de gebruiker deze voorstellen accepteert, ook voor de artikelen op een lager niveau.  

Zie [Voorraadprofielen laden](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles) voor meer informatie over overwegingen voor productie.  

### <a name="locations--transfer-level-priority"></a>Prioriteit op niveau van vestigingen/transfers  
Bedrijven die in meerdere vestigingen actief zijn, moeten mogelijk voor elke vestiging afzonderlijk plannen. Het veiligheidsvoorraadniveau van een artikel en het bestelbeleid ervan kunnen bijvoorbeeld van vestiging tot vestiging verschillen In dit geval moeten per artikel en ook per vestiging de planningsparameters worden opgegeven.  

Dit wordt ondersteund met het gebruik van SKU's, waar individuele planningsparameters kunnen worden opgegeven op SKU-niveau. Een SKU kan worden gezien als een artikel op een bepaalde locatie. Als de gebruiker geen SKU voor die vestiging heeft opgegeven, worden standaard de parameters gebruikt die op de artikelkaart zijn ingesteld. De toepassing berekent alleen een planning voor actieve vestigingen, wat betekent dat er een bestaande vraag of voorziening is voor het betreffende artikel.  

In principe kan elk artikel op elke locatie worden afgehandeld, maar de benadering door de toepassing van het vestigingsconcept is tamelijk strikt. Een verkooporder op de ene vestiging kan bijvoorbeeld niet worden vervuld door beschikbare voorraad op een andere vestiging. Het aantal op voorraad moet eerst worden overgebracht naar de vestiging die op de verkooporder is opgegeven.  

![Planning van voorraadhoudende eenheden](media/NAV_APP_supply_planning_1_SKU_planning.png "Planning van voorraadhoudende eenheden")  

Zie [Ontwerpdetails: Transfers in planning](design-details-transfers-in-planning.md) voor meer informatie.  

### <a name="order-priority"></a>Orderprioriteit  
Binnen een bepaalde SKU staat de verzochte of beschikbare datum voor de hoogste prioriteit; de vraag van vandaag moet worden verwerkt vóór de vraag van de eerstvolgende dagen. Afgezien van dit soort prioriteit worden de verschillende soorten vraag en aanbod gesorteerd op basis van bedrijfsbelang om te beslissen aan welke vraag moet worden voldaan voordat aan andere vraag kan worden voldaan. Voor de aanbodzijde geeft de orderprioriteit aan welke voorzieningenbron moet worden toegepast voordat andere voorzieningenbronnen worden toegepast.  

Zie [Orders in prioriteitsvolgorde plaatsen](design-details-balancing-demand-and-supply.md#prioritizing-orders) voor meer informatie.  

## <a name="demand-forecasts-and-blanket-orders"></a>Vraagprognoses en raamcontracten  
Prognoses en raamcontracten vertegenwoordigen beide verwachte vraag. Het raamcontract omvat de bedoelde inkoop van een klant over een bepaalde periode en is bedoeld om de onzekerheid van de algemene prognose te verminderen. Het raamcontract is een klantspecifieke prognose in aanvulling op de niet-opgegeven prognose zoals hieronder beschreven.  

![Planning met prognoses](media/NAV_APP_supply_planning_1_forecast_and_blanket.png "Planning met prognoses")  

Zie voor meer informatie het gedeelte 'Prognosevraag wordt verlaagd door verkooporders' in [Voorraadprofielen laden](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).  

## <a name="planning-assignment"></a>Planningsopdracht  
Alle artikelen moeten worden gepland, maar er is geen reden om een planning voor een artikel te berekenen tenzij er een verandering in het vraag- of aanbodpatroon is opgetreden sinds er voor het laatst een planning is berekend.  

Als de gebruiker een nieuwe verkooporder heeft ingevoerd of een bestaande heeft gewijzigd, is er reden om de planning opnieuw te berekenen. Andere redenen omvatten een wijziging in de voorspelde of gewenste veiligheidsvoorraad. Het wijzigen van een stuklijst door een materiaal toe te voegen of te verwijderen duidt waarschijnlijk op een wijziging, maar alleen voor het onderdeelartikel.  

Het planningssysteem bewaakt dergelijke gebeurtenissen en wijst de benodigde artikelen toe aan de planning.  

Voor meerdere vestigingen vindt de toewijzing plaats op het niveau van de combinatie artikel per vestiging. Wanneer bijvoorbeeld een verkooporder op slechts één vestiging is gemaakt, wordt het artikel in die specifieke vestiging voor planning toegewezen.  

De reden voor het selecteren van artikelen voor planning heeft te maken met systeemprestaties. Als er geen verschil is opgetreden in het vraag/aanbod-patroon van een artikel, zal het planningssysteem geen uit te voeren acties voorstellen. Zonder de planningstoewijzing moet het systeem de berekeningen voor alle artikelen uitvoeren om te weten waarvoor moet worden gepland, en dat zou de systeembronnen uitputten.  

U vindt een volledige lijst met redenen voor het toewijzen van een artikel voor de planning in [Ontwerpdetails: Tabel Planningstoewijzing](design-details-planning-assignment-table.md).  

De planningsopties in [!INCLUDE[d365fin](includes/d365fin_md.md)] zijn:  

-   Regeneratief plan berekenen - berekent alle geselecteerde artikelen, of het nodig is of niet.  
-   Mutatieplan berekenen - berekent alleen de geselecteerde artikelen die een wijziging hebben ondergaan in het vraag/aanbod-patroon en daarom zijn toegewezen voor planning.  

Een aantal gebruikers is van mening dat de mutatieplanning tussendoor moet worden uitgevoerd, bijvoorbeeld wanneer verkooporders worden ingevoerd. Dit kan echter verwarrend zijn omdat dynamische ordertracering en planningsboodschappen ook ad hoc worden berekend. Bovendien biedt [!INCLUDE[d365fin](includes/d365fin_md.md)] real-time ATP-besturing, waardoor pop-upwaarschuwingen worden weergegeven wanneer verkooporders worden ingevoerd als niet aan de vraag kan worden voldaan onder het huidige leveringsplan.  

Naast deze overwegingen plant het planningssysteem alleen artikelen die de gebruiker heeft voorbereid met de juiste planningsparameters. Anders wordt ervan uitgegaan dat de gebruiker de artikelen handmatig of semiautomatisch plant met de functie Orderplanning.  

Zie voor meer informatie over de automatische planningsprocedures [Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md).  

## <a name="item-dimensions"></a>Artikeldimensies  
Vraag en voorziening kunnen variantcodes en vestigingscodes hebben die moeten worden gerespecteerd wanneer het planningssysteem vraag en aanbod afstemt.  

Het systeem behandelt variant- en vestigingscodes als artikeldimensies op een verkooporderregel, voorraadpost, enzovoort. Er wordt een planning berekend voor elke combinatie van variant en locatie, alsof de combinatie een apart artikelnummer is.  

In plaats van een theoretische combinatie van vestiging en variant te berekenen, berekent de toepassing alleen de combinaties die werkelijk voorkomen in de database.  

Zie [Ontwerpdetails: Vraag op lege vestiging](design-details-balancing-demand-and-supply.md) voor meer informatie over de manier waarop het planningssysteem omgaat met vestigingscodes in vraag.  

## <a name="item-attributes"></a>Artikelkenmerken  
Afgezien van algemene artikeldimensies, zoals artikelnummer, variant, vestiging en soort order, kan elke vraag- en aanbodgebeurtenis extra specificaties hebben in de vorm van serie-/lotnummers. Het planningssysteem plant deze kenmerken op bepaalde manieren, afhankelijk van het specificatieniveau.  

Een order-aan-order koppeling tussen vraag en aanbod is een ander soort kenmerk dat van invloed is op het planningssysteem.  

### <a name="specific-attributes"></a>Specifieke kenmerken  
Bepaalde kenmerken van vraag zijn specifiek en moeten precies overeenkomen met bijbehorende voorzieningen. Er zijn de volgende twee specifieke kenmerken:  

-   Vereiste serie-/lotnummers die bepaalde vereffening vereisen (het selectievakje **Specifieke serienr.-tracering** of **Specifieke lottracering** is ingeschakeld op de pagina **Artikeltraceringscode** voor de artikeltraceringscode die door het artikel wordt gebruikt).  
-   Koppelingen naar voorzieningenorders die handmatig of automatisch worden gemaakt voor bepaalde vraag (order-naar-order koppelingen).  

Voor deze kenmerken past het planningssysteem de volgende regels toe:  

-   Aan vraag met bepaalde kenmerken kan alleen worden voldaan door aanbod met overeenkomende kenmerken.  
-   Voorzieningen met specifieke kenmerken kunnen ook voldoen aan vraag waarvoor niet specifiek om deze kenmerken wordt gevraagd.  

Als aan vraag naar specifieke kenmerken niet kan worden voldaan door voorraad of verwachte voorzieningen, stelt het planningssysteem een nieuwe voorzieningenorder voor om aan deze specifieke vraag te voldoen, ongeacht planningsparameters.  

### <a name="non-specific-attributes"></a>Niet-specifieke kenmerken  
Artikelen met een serie-/lotnummer zonder specifieke artikeltraceringinstellingen kunnen serie-/lotnummers bevatten die niet op exacte hetzelfde serie-/partijnummer hoeven te worden toegepast, maar op elk willekeurig serie-/partijnummer kunnen worden toegepast. Dit geeft het planningssysteem meer vrijheid om bijvoorbeeld een vraag met een serienummer af te stemmen op een voorziening met een serienummer, doorgaans in de voorraad.  

Vraag-aanbod met serie-/lotnummers, specifiek of niet-specifiek, wordt gezien als hoge prioriteit en is daarom vrijgesteld van de vaste zone, wat betekent dat het onderdeel is van planning zelfs als het vervalt vóór de geplande begindatum.  

Zie voor meer informatie het gedeelte 'Serie-/lotnummers worden geladen per specificatieniveau' in [Voorraadprofielen laden](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles).  

Voor meer informatie over hoe het planningssysteem kenmerken afstemt raadpleegt u [Serie-/lotnummers en order-naar-order koppelingen zijn vrijgesteld van de vaste zone](design-details-balancing-demand-and-supply.md#seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone).  

## <a name="order-to-order-links"></a>Order-naar-order koppelingen  
Order-naar-order aanschaffing betekent dat een artikel wordt ingekocht, geassembleerd of geproduceerd om exclusief aan een specifieke vraag te voldoen. Meestal heeft dit betrekking op A-producten en de motivatie om dit beleid te kiezen, kan zijn dat de vraag niet frequent is, dat de doorlooptijd onbeduidend is of dat de vereiste kenmerken verschillen.  

Een ander speciaal geval waarin order-aan-order koppelingen worden gebruikt is wanneer een assemblageorder aan een verkooporder wordt gekoppeld in een assembleren-op-order scenario.  

Order-naar-order koppelingen worden op vier manieren toegepast tussen vraag en aanbod:  

-   Wanneer het geplande artikel het bestelbeleid Order gebruikt.  
-   Wanneer het productiebeleid Op order produceren wordt gebruikt om productieorders met meerdere niveaus of projecttype te maken (waarbij benodigde onderdelen op dezelfde productieorder worden geproduceerd).  
-   Bij het maken van productieorders voor verkooporders met de functie Verkooporderplanning.  
-   Bij het assembleren van een artikel op een verkooporder. (Het assemblagebeleid is ingesteld op Op order assembleren.  

In deze gevallen zal het planningssysteem alleen voorstellen het vereiste aantal te bestellen. Zodra de inkoop-, productie- of assemblageorder is gemaakt, blijft deze gekoppeld worden aan de corresponderende vraag. Wanneer de tijd of het aantal van een verkooporder verandert, stelt het planningssysteem voor dat de bijbehorende voorzieningenorder dienovereenkomstig wordt gewijzigd.  

Wanneer order-naar-order koppelingen bestaan, betrekt het planningssysteem geen gekoppelde voorziening of voorraad in de vereffeningsprocedure. Het is aan de gebruiker om te evalueren of de gekoppelde voorziening moet worden gebruikt om aan andere of nieuwe vraag te voldoen en, in dat geval, de voorzieningenorder te verwijderen of de gekoppelde voorziening handmatig te reserveren.  

Reserveringen en ordertraceringskoppelingen worden onderbroken als een situatie onmogelijk wordt, zoals het verplaatsen van de vraag naar een datum die eerder is dan de voorziening. De order-naar-order koppeling wordt echter aangepast aan eventuele wijzigingen in de vraag of het aanbod en daarom wordt de koppeling nooit verbroken.  

## <a name="reservations"></a>Reserveringen  
Het planningssysteem houdt in de berekening geen rekening met gereserveerde aantallen. Als bijvoorbeeld een verkooporder totaal of deels is gereserveerd tegen het aantal in voorraad, kan het gereserveerde aantal in voorraad niet worden gebruikt om aan andere vraag te voldoen. Het planningssysteem houdt in de berekening geen rekening met deze vraag-voorzieningcombinatie.  

Het planningssysteem neemt echter toch gereserveerde aantallen op in het verwachte voorraadprofiel omdat met alle aantallen rekening moet worden gehouden wanneer wordt bepaald wanneer het bestelpunt is gepasseerd en hoeveel moet worden besteld om het maximale voorraadniveau te bereiken en niet te overschrijden. Dus leiden overbodige reserveringen tot verhoogde risico's dat voorraadniveaus laag worden omdat de planninglogica gereserveerde aantallen niet detecteert.  

De volgende illustratie geeft aan hoe reserveringen het meest haalbare plan kunnen belemmeren.  

![Planning met reserveringen](media/NAV_APP_supply_planning_1_reservations.png "Planning met reserveringen")  

Zie voor meer informatie [Reservering, ordertracering en planningsboodschappen](design-details-reservation-order-tracking-and-action-messaging.md).  

## <a name="warnings"></a>Waarschuwingen  
De eerste kolom in het planningsvoorstel is voor de waarschuwingsvelden. Voor elke planningsregel die is gemaakt voor een uitzonderlijke situatie wordt een waarschuwingspictogram weergegeven in dit veld, waarop de gebruiker kan klikken voor meer informatie.  

Voorraad op planningsregels met waarschuwingen wordt gewoonlijk niet gewijzigd volgens planningsparameters. In plaats daarvan stelt het planningssysteem alleen een voorziening ter dekking van de hoeveelheid van de exacte vraag voor. Het systeem kan echter zo worden ingesteld dat bepaalde planningsparameters voor planningsregels met bepaalde waarschuwingen worden gerespecteerd. Zie de omschrijving van deze opties voor respectievelijk de batchverwerking **Plan berekenen - Planningsvoorstel** en de batchverwerking **Plan berekenen - Ink.-voorstel** voor meer informatie.  

De waarschuwingsgegevens worden op de pagina **Niet-getraceerde planningselementen** weergegeven, die ook wordt gebruikt om ordertraceringskoppelingen te tonen aan niet-order systeementiteiten. De volgende waarschuwingstypen zijn mogelijk:  

-   Noodgeval  
-   Uitzondering  
-   Opmerking  

![Waarschuwingen in het planningswerkblad](media/NAV_APP_supply_planning_1_warnings.png "Waarschuwingen in het planningswerkblad")  

### <a name="emergency"></a>Noodgeval  
De waarschuwing Noodgeval wordt in twee gevallen weergegeven:  

-   Wanneer de voorraad negatief is op de geplande begindatum.  
-   Wanneer er geantedateerde voorziening- of vraaggebeurtenissen bestaan.  

Als de voorraad van een artikel negatief is op de geplande begindatum, wordt er door het planningssysteem een noodorder voor een voorziening voorgesteld die wordt aangevoerd op de geplande begindatum. De waarschuwing vermeldt de begindatum en de hoeveelheid van de order voor een noodvoorziening. Zie voor meer informatie [Verwachte negatieve voorraad verwerken](design-details-handling-reordering-policies.md#handling-projected-negative-inventory).  

Alle documentregels met vervaldatums voor de geplande begindatum worden samengevoegd tot één noodorder voor een voorziening voor het artikel die wordt aangevoerd op de geplande startdatum.  

### <a name="exception"></a>Uitzondering  
De uitzonderingswaarschuwing wordt weergegeven als de verwachte beschikbare voorraad onder de veiligheidsvoorraad daalt. Het planningssysteem stelt een order voor een voorziening voor om aan de vraag op de vervaldatum te kunnen voldoen. De waarschuwing vermeldt de veiligheidsvoorraad van het artikel en de datum waarop de voorraad daaronder daalt.  

Als de beschikbare voorraad kleiner is dan de veiligheidsvoorraad, wordt dit als een uitzondering beschouwd omdat dit normaliter niet gebeurt als het bestelpunt op de juiste manier is ingesteld. Zie voor meer informatie [De rol van het bestelpunt](design-details-handling-reordering-policies.md#the-role-of-the-reorder-point).  

In het algemeen zorgen uitzonderlijke ordervoorstellen ervoor dat de verwachte beschikbare voorraad nooit lager is dan de veiligheidsvoorraad. Dit betekent dat het voorgestelde aantal voldoende is om de veiligheidsvoorraad te dekken, zonder dat planningsparameters moeten worden overwogen. In sommige scenario's komen orderwijzigingen echter in aanmerking.  

> [!NOTE]  
>  Het planningssysteem kan de veiligheidsvoorraad opzettelijk hebben verbruikt en vult deze vervolgens direct aan. Zie [Veiligheidsvoorraad kan wordt verbruikt](design-details-balancing-demand-and-supply.md#loading-the-inventory-profiles) voor meer informatie.

### <a name="attention"></a>Opmerking  
De attentiewaarschuwing wordt in drie gevallen weergegeven:  

-   De geplande begindatum is eerder dan de werkdatum.  
-   Op de planningsregel wordt voorgesteld een vrijgegeven inkoop- of productieorder te wijzigen.  
-   De verwachte voorraad is groter dan het overflowniveau op de vervaldatum. Zie voor meer informatie [Onder het overflowniveau blijven](design-details-handling-reordering-policies.md#staying-under-the-overflow-level).  

> [!NOTE]  
>  bij het plannen van regels met waarschuwingen wordt het veld **Planningsboodschap accepteren** niet geselecteerd, omdat de planner naar verwachting de regels verder gaat bekijken voordat de planning wordt uitgevoerd.  

## <a name="error-logs"></a>Foutenlogboeken  
Op de aanvraagpagina Planning berekenen kan de gebruiker het veld **Stoppen en eerste fout tonen** selecteren om de planning te laten stoppen wanneer de eerste fout wordt geconstateerd. Tegelijkertijd wordt een boodschap weergegeven met informatie over de fout. Als er sprake is van een fout, worden alleen de planningsregels die zijn gemaakt voordat de fout werd geconstateerd, in het planningsvoorstel weergegeven.  

Als het veld niet is geselecteerd, wordt de batchverwerking Planning berekenen voortgezet totdat deze is voltooid. Fouten onderbreken de batchverwerking niet. Als er een of meer fouten zijn, wordt na afloop een bericht weergegeven waarin staat hoeveel artikelen dit betreft aan de hand van fouten. Vervolgens wordt de pagina **Planningfoutenlogboek** geopend met meer informatie over de fout en koppelingen naar de betreffende documenten of instellingskaart(en).  

![Foutmeldingen in het planningswerkblad](media/NAV_APP_supply_planning_1_error_log.png "Foutmeldingen in het planningswerkblad")  

## <a name="planning-flexibility"></a>Planningsflexibiliteit  
Het is niet altijd praktisch om een bestaande voorzieningenorder te plannen, bijvoorbeeld wanneer de productie is gestart of wanneer op een bepaalde dag aanvullend personeel wordt ingehuurd om het werk te doen. Om aan te geven of een bestaande order kan worden gewijzigd door het planningssysteem, hebben alle voorzieningenorderregels een veld Planningsflexibiliteit met twee opties: Onbeperkt of Geen. Als het veld is ingesteld op Geen, wordt niet geprobeerd de voorzieningenorderregel te wijzigen.  

Het veld kan handmatig worden ingesteld door de gebruiker, maar in sommige gevallen wordt het automatisch ingesteld door het systeem. Het feit dat de planningsflexibiliteit handmatig kan worden ingesteld door de gebruiker is belangrijk omdat hierdoor het gebruik van de functie eenvoudig kan worden aangepast aan verschillende werkstromen en bedrijfsgevallen.  

Zie [Ontwerpdetails: Transfers in planning](design-details-transfers-in-planning.md) voor meer informatie over het gebruik van dit veld.  

## <a name="order-planning"></a>Orderplanning  
De planningfunctie voor algemene voorzieningen wordt weergegeven op de pagina **Orderplanning** en is bedoeld voor handmatige besluitvorming. Deze houdt geen rekening met planningsparameters en wordt daarom niet verder besproken in dit document. Voor meer informatie over de orderplanningsfunctie raadpleegt u de Help in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>  Het is niet raadzaam Orderplanning te gebruiken als het bedrijf al gebruikmaakt van plannings- of inkoopvoorstellen. Orders voor voorzieningen die zijn gemaakt via de pagina **Orderplanning** kunnen worden gewijzigd of verwijderd tijdens de automatisch uitgevoerde planningen. Dat komt doordat voor de geautomatiseerde planning planningsparameters worden gebruikt en deze niet in aanmerking kunnen worden genomen door gebruikers die handmatig plannen op de pagina Orderplanning.  

##  <a name="finite-loading"></a>Eindige bezettingsplanning  
[!INCLUDE[d365fin](includes/d365fin_md.md)] is een standaard ERP-systeem, geen verzend- of werkvloercontrolesysteem. Het systeem plant een uitvoerbaar gebruik van resources door een ruw schema te leveren, maar het maakt en onderhoudt niet automatisch gedetailleerde schema's op basis van prioriteiten of optimalisatieregels.  

Het bedoelde gebruik van de functie Capaciteitsbegrensde resource is 1): overbelasting uit specifieke resources te voorkomen, en 2): ervoor te zorgen dat alle capaciteit toegewezen is als dit de omlooptijd van een productieorder kan verhogen. De functie omvat geen voorzieningen of opties om bewerkingen te prioriteren of te optimaliseren, zoals mag worden verwacht in een systeem voor verzending. De functie kan echter ruwe capaciteitsinformatie leveren die nuttig is om knelpunten te vinden en overbelasting van resources te voorkomen.  

Bij het plannen met capaciteitsbegrensde resources zorgt het systeem dat er geen resources boven de gedefinieerde capaciteit (kritieke werklastpercentage) worden geladen. Dit gebeurt door elke bewerking toe te wijzen aan de dichtstbijzijnde beschikbare periode. Als de periode niet groot genoeg is om de hele bewerking uit te voeren, wordt de bewerking in twee of meer delen gesplitst in de dichtstbijgelegen perioden.  

> [!NOTE]  
>  In het geval van gesplitste bewerkingen wordt de insteltijd slechts eenmaal toegewezen omdat ervan wordt uitgegaan dat enige handmatige aanpassing wordt uitgevoerd om de planning te optimaliseren.  

De dempingstijd kan bij resources worden opgeteld om splitsen van bewerkingen te minimaliseren. Hiermee kan het systeem de werklast op de laatst mogelijke dag plannen door het kritieke werklastpercentage iets te overschrijden als dit het aantal bewerkingen kan verminderen die worden gesplitst.  

Hiermee wordt het overzicht afgesloten van centrale concepten die betrekking hebben op de planning van voorzieningen in [!INCLUDE[d365fin](includes/d365fin_md.md)]. In de volgende secties worden deze concepten verder geanalyseerd en in de context geplaatst van de kernplanningsprocedures, het afstemmen van vraag en voorziening, en het gebruik van bestelbeleid.  

## <a name="see-also"></a>Zie ook  
[Ontwerpdetails: Transfers in planning](design-details-transfers-in-planning.md)   
[Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md)   
[Ontwerpdetails: Tabel Planningstoewijzing](design-details-planning-assignment-table.md)   
[Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md)   
[Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md)
