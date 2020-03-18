---
title: 'Ontwerpdetails: Vraag en aanbod afstemmen | Microsoft Docs'
description: Om te begrijpen hoe het planningssysteem werkt, is het noodzakelijk om de prioriteitsdoelen van het planningssysteem te begrijpen. De belangrijkste hiervan zijn om te zorgen dat aan eventuele vraag wordt voldaan door voldoende aanbod en dat elk aanbod een doel dient.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 54e7aabe2989033a33373b960633b1c8f8e38eab
ms.sourcegitcommit: d0dc5e5c46b932899e2a9c7183959d0ff37738d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076424"
---
# <a name="design-details-balancing-demand-and-supply"></a>Ontwerpdetails: Vraag en aanbod afstemmen
Om te begrijpen hoe het planningssysteem werkt, is het noodzakelijk om de prioriteitsdoelen van het planningssysteem te begrijpen. De belangrijkste hiervan zijn om te zorgen dat:  

- Aan eventuele vraag wordt voldaan door voldoende aanbod.  
- Elk aanbod dient een doel.  

 Over het algemeen worden deze doelstellingen bereikt door aanbod met vraag af te stemmen.  

## <a name="demand-and-supply"></a>Vraag en voorzieningen
 Vraag is de verzamelterm voor elk soort brutovraag, zoals een verkooporder en materiaalbehoefte van een productieorder. Bovendien staat de toepassing meer technische soorten vraag toe, zoals negatieve voorraad en inkoopretouren  

  Voorziening is de algemene term voor elke soort positief of inkomend aantal, zoals voorraad, inkopen, assemblage, productie of inkomende transfers. Een verkoopretour kan bovendien ook voorziening vertegenwoordigen.  

  Om de vele bronnen van vraag en voorzieningen te sorteren, ordent het planningssysteem deze op twee tijdpaden die voorraadprofielen worden genoemd. Eén profiel bevat vraaggebeurtenissen en het andere bevat de corresponderende voorzieninggebeurtenissen. Elke gebeurtenis vertegenwoordigt een entiteit uit het ordernetwerk, bijvoorbeeld een verkooporderregel, een artikelpost of een productieorderregel.  

  Wanneer voorraadprofielen worden geladen, worden de verschillende vraag-voorzieningcombinaties vereffend om een voorzieningenplan uit te voeren dat aan de genoemde doelstellingen voldoet.  

  Planningsparameters en voorraadniveaus zijn respectievelijk andere soorten vraag en aanbod, die geïntegreerde afstemming ondergaan om voorraadartikelen aan te vullen. Zie voor meer informatie [Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md).

## <a name="the-concept-of-balancing-in-brief"></a>Het concept sluitend maken in het kort
  Vraag is afkomstig van klanten van een bedrijf. Voorziening is wat het bedrijf kan maken of verwijderen om te zorgen voor balans. Het planningssysteem begint met de onafhankelijke vraag en werkt vervolgens achterwaarts naar de voorziening.  

   De voorraadprofielen worden gebruikt om gegevens te bevatten over de vraag en voorzieningen, aantallen en tijd. Deze profielen vormen in principe de twee zijden van de vereffeningsschaal.  

   Het doel van het planningsmechanisme is om vraag en voorziening van een artikel op elkaar af te stemmen om te zorgen dat de voorziening voldoet aan de vraag op een haalbare manier zoals wordt bepaald door de planningsparameters en -regels.  

   ![Overzicht van vraag- en aanbodafstemming](media/nav_app_supply_planning_2_balancing.png "Overzicht van vraag- en aanbodafstemming")

## <a name="dealing-with-orders-before-the-planning-starting-date"></a>Werken met orders voor de geplande begindatum
Om te voorkomen dat een voorzieningenplan onmogelijke en daarom nutteloze voorstellen toont, beschouwt het planningssysteem de periode tot de begindatum van de planning als een vaste zone waarvoor niets wordt gepland. De volgende regel geldt voor de vaste zone:  

Alle vraag en aanbod vóór de begindatum van de planningsperiode wordt beschouwd als deel van de voorraad of wordt verzonden.  

Het planningssysteem zal, met enkele uitzonderingen, geen wijzigingen in voorzieningenorders in de vaste zone voorstellen en er worden voor die periode geen ordertraceringskoppelingen gemaakt of onderhouden.  

De uitzonderingen op deze regel zijn als volgt:  

   * Als de verwachte beschikbare voorraad, inclusief totale vraag en aanbod in de vaste zone, lager is dan nul.  
   * Als serie-/lotnummers vereist zijn op de geantidateerde order(s).  
   * Als de aanbod/vraag-combinatie is gekoppeld door een order-aan-order beleid.  

Als de eerste beschikbare voorraad onder nul is, wordt er op de dag vóór de planningsperiode door het planningssysteem een noodvoorzieningenorder voorgesteld voor het ontbrekende aantal. Dus is de voorspelde en beschikbare voorraad altijd minstens nul wanneer het plannen voor de toekomstige periode begint. De planningsregel voor deze voorzieningenorder geeft een waarschuwingspictogram Noodgeval weer en er worden extra gegevens getoond bij het opzoeken.  

### <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a>Serie-/lotnummers en order-naar-order koppelingen zijn vrijgesteld van de vaste zone  
   Als serie-/lotnummers vereist zijn of als een order-naar-order koppeling bestaat, zal het planningssysteem de vaste zone negeren en zulke aantallen opnemen die geantidateerd zijn vanaf de begindatum, en mogelijk corrigerende acties voorstellen als vraag en aanbod niet zijn gesynchroniseerd. De bedrijfsreden voor dit principe is dat dergelijke specifieke vraag-voorzieningcombinaties moeten overeenkomen om te zorgen dat aan deze specifieke vraag wordt voldaan.

## <a name="loading-the-inventory-profiles"></a>De voorraadprofielen laden
Om de vele bronnen van vraag en voorzieningen te sorteren, ordent het planningssysteem deze op twee tijdpaden die voorraadprofielen worden genoemd.  

De normale soorten vraag en voorziening met vervaldatums op of na de begindatum van de planning worden in elk voorraadprofiel geladen. Na het laden worden de verschillende soorten vraag en voorziening gesorteerd op basis van algemene prioriteiten, zoals vervaldatum, low-levelcodes, vestiging en variant. Daarnaast worden orderprioriteiten toegepast op de verschillende soorten om ervoor te zorgen dat aan de belangrijkste vraag het eerst wordt voldaan. Zie [Orders in prioriteitsvolgorde plaatsen](design-details-balancing-demand-and-supply.md#prioritizing-orders) voor meer informatie.  

Zoals eerder gezegd, kan vraag ook negatief zijn. Dit betekent dat het moet worden verwerkt als voorraad. In tegenstelling tot de normale soorten voorziening wordt negatieve vraag echter gezien als vaste voorziening. Het planningssysteem kan hier rekening mee houden, maar er worden geen wijzigingen voorgesteld.  

Over het algemeen beschouwt het planningssysteem alle voorzieningenorders na de begindatum van de planning als vatbaar voor wijziging om aan vraag te voldoen. Zodra echter een aantal vanuit een voorzieningenorder is geboekt, kan deze niet meer in het planningssysteem worden gewijzigd. De volgende verschillende orders kunnen niet opnieuw worden gepland:  

- Vrijgegeven productieorders waarbij het verbruik of de output is geboekt.  
- Assemblageorders waarbij het verbruik of de output is geboekt.  
- Transferorders waarop verzending is geboekt.  
- Inkooporders waarop ontvangst is geboekt.  

Afgezien van het laden van typen vraag en aanbod, worden bepaalde soorten geladen met het oog op speciale regels en afhankelijkheden die worden beschreven in het volgende.  

### <a name="item-dimensions-are-separated"></a>Artikeldimensies worden gescheiden  
Het voorzieningenplan moet worden berekend per combinatie van artikeldimensies, zoals variant en vestiging. Er is echter geen reden om elke theoretische combinatie te berekenen. Alleen combinaties met vraag en/of aanbod moeten worden berekend.  

Het planningssysteem bepaalt dit via het voorraadprofiel. Wanneer een nieuwe combinatie wordt gevonden, wordt een interne besturingsrecord gemaakt die de werkelijke combinatiegegevens bevat. De SKU wordt automatisch ingevoerd als besturingsrecord of buitenste lus. Daarom worden de juiste planningsparameters op basis van een combinatie van variant en vestiging ingesteld en kan de toepassing doorgaan naar de binnenlus.  

> [!NOTE]  
>  De gebruiker hoeft geen SKU-record in te voeren tijdens het invoeren van vraag en/of voorziening voor een bepaalde combinatie van variant en vestiging. Wanneer er geen SKU bestaat voor een bepaalde combinatie, maakt de toepassing daarom een eigen tijdelijke SKU op basis van de artikelkaartgegevens. Als Vestiging verplicht op Ja is ingesteld op de pagina Voorraadinstellingen, moet een SKU worden gemaakt of moet Onderdelen op vestiging worden ingesteld op Ja. Zie [Ontwerpdetails: Vraag op lege vestiging](design-details-demand-at-blank-location.md) voor meer informatie.  

### <a name="seriallot-numbers-are-loaded-by-specification-level"></a>Serie-/lotnummers worden geladen op specificatieniveau  
Kenmerken in de vorm van serie-/lotnummers worden in de voorraadprofielen geladen met de vraag en het aanbod waaraan ze zijn toegewezen.  

Vraag- en voorzieningskenmerken worden gerangschikt op orderprioriteit en op het niveau van specificatie. Omdat serie-/lotnummers het specificatieniveau aangeven, wordt bij een specifiekere vraag, zoals een lotnummer dat specifiek is geselecteerd voor een verkoopregel, een overeenkomst gezocht vóór minder specifieke vraag, bijvoorbeeld een verkoop vanuit een willekeurig geselecteerd lotnummer.  

> [!NOTE]  
>  Er zijn geen speciale prioriteitsregels voor vraag en voorzieningen met serie-/lotnummers, behalve het specificatieniveau dat wordt gedefinieerd door de combinatie van serie- en lotnummer en de instelling voor artikeltracering van de betreffende artikelen.  

Tijdens het sluitend maken beschouwt het planningssysteem voorzieningen met serie-/lotnummers als inflexibel en wordt niet geprobeerd om dergelijke voorzieningenorders te verhogen of opnieuw te plannen (tenzij ze worden gebruikt in een order-naar-order relatie). Zie Order-naar-order koppelingen worden nooit verbroken). Dit beschermt de voorziening van het ontvangen van meerdere, mogelijk strijdige planningsboodschappen wanneer een voorziening variërende kenmerken heeft, zoals een verzameling verschillende serienummers.  

Een andere reden dat voorziening met serienummers/lotnummers inflexibel is, is dat serienummers/lotnummers over het algemeen zo laat in het proces worden toegewezen dat het verwarrend zou zijn als er wijzigingen werden voorgesteld.  

Het vereffenen van serie-/lotnummers heeft geen betrekking op de [vaste zone](design-details-dealing-with-orders-before-the-planning-starting-date.md). Als de vraag en het aanbod niet zijn gesynchroniseerd, zal het planningssysteem wijzigingen of nieuwe orders voorstellen, ongeacht de geplande begindatum.  

### <a name="order-to-order-links-are-never-broken"></a>Order-naar-order koppelingen worden nooit verbroken  
Bij het plannen van een order-naar-order-artikel moet de gekoppelde voorziening alleen worden gebruikt voor de vraag waarvoor het oorspronkelijk is bedoeld. De gekoppelde vraag moet niet door een willekeurige andere voorziening worden verwerkt, zelfs wanneer het in de huidige situatie beschikbaar is wat betreft tijd en aantal. Een assemblageorder die is gekoppeld aan een verkooporder in een op-order-assembleren scenario, kan bijvoorbeeld niet worden gebruikt om aan andere vraag te voldoen.  

Order-naar-order vraag en aanbod moeten precies afgestemd zijn. Het planningssysteem waarborgt de voorziening onder alle omstandigheden, zonder rekening te houden met parameters voor ordergrootte, velden en aantallen in de voorraad (buiten de aantallen die betrekking hebben op de gekoppelde orders). Om dezelfde reden stelt het systeem voor overschotaanbod te verlagen als de gekoppelde vraag wordt verlaagd.  

Deze vereffening heeft ook invloed op de timing. Er wordt geen rekening gehouden met de beperkte horizon die wordt opgegeven door het tijdsinterval; de voorziening wordt opnieuw gepland als het tijdschema van de vraag wordt gewijzigd. Er wordt echter rekening gehouden met de dempingstijd en het wordt voorkomen dat order-naar-order voorzieningen worden uitgepland, behalve de interne voorzieningen van een productieorder met meerdere niveaus (projectorder).  

> [!NOTE]  
>  Serie-/lotnummers kunnen ook worden opgegeven op order-op-order vraag. In dat geval wordt het aanbod niet standaard beschouwd als inflexibel, wat normaal wel het geval is met serie-/lotnummers. In dit geval brengt het systeem een verhoging of verlaging aan afhankelijk van wijzigingen in de vraag. Als één vraag bovendien variërende serie-/lotnummers heeft, zoals meerdere lotnummers, wordt per lot één voorraadorder voorgesteld.  

> [!NOTE]  
>  Prognoses moeten niet leiden tot het maken van voorzieningenorders die zijn gebonden door een order-op-order koppeling. Als de prognose wordt gebruikt, moet deze alleen worden gebruikt als generator van afhankelijke vraag in een productieomgeving.  

### <a name="component-need-is-loaded-according-to-production-order-changes"></a>Materiaalbehoefte wordt geladen op basis van wijzigingen in productieorders  
Bij de verwerking van productieorders moet het planningssysteem de benodigde materialen controleren voordat ze in het vraagprofiel worden geladen. Materiaalregels die voortvloeien uit een gewijzigde productieorder vervangen regels uit de oorspronkelijke order. Hierdoor wordt gezorgd dat het planningssysteem bepaalt dat planningsregels voor materiaalbehoefte nooit worden gedupliceerd.  

###  <a name="BKMK_SafetyStockMayBeConsumed"></a> Veiligheidsvoorraad kan worden verbruikt  
De veiligheidsvoorraad is hoofdzakelijk een vraagsoort en wordt daarom in het voorraadprofiel geladen op de begindatum van de planning.  

De veiligheidsvoorraad is een voorraadhoeveelheid die opzij is gezet om onzekerheden in de vraag te compenseren tijdens de aanvullingslevertermijn. Deze voorraad kan echter worden verbruikt als deze moet worden gebruikt om aan vraag te voldoen. In dat geval zorgt het planningssysteem ervoor dat de veiligheidsvoorraad snel wordt aangevuld, door een voorzieningenorder voor te stellen om het verbruikte deel van de veiligheidsvoorraad aan te vullen op de datum waarop het is verbruikt. Deze planningsregel zal een pictogram van een uitzonderingswaarschuwing bevatten, zodat de planner weet dat de veiligheidsvoorraad gedeeltelijk of volledig is verbruikt door een uitzonderingsorder voor het ontbrekende aantal.  

### <a name="forecast-demand-is-reduced-by-sales-orders"></a>Prognosevraag wordt verlaagd door verkooporders  
De vraagprognose drukt de verwachte toekomstige vraag uit. Wanneer werkelijke vraag wordt ingevoerd, meestal als verkooporders voor geproduceerde artikelen, wordt de prognose verbruikt.  

De prognose zelf wordt niet verminderd door verkooporders; deze blijft gelijk. De prognoseaantallen die in de planningsberekening worden gebruikt, worden echter verlaagd (met de verkooporderaantallen) voordat het eventuele resterende aantal in het vraagvoorraadprofiel wordt opgenomen. Wanneer het planningssysteem de werkelijke verkoop in een periode onderzoekt, worden zowel openstaande verkooporders als artikelposten uit verzonden verkoop meegenomen, tenzij ze zijn afgeleid van een raamcontract.  

Een gebruiker is vereist om een geldige prognoseperiode te definiëren. De datum van het prognoseaantal definieert het begin van de periode, en de datum op de volgende prognose bepaalt het einde van de periode.  

De prognose voor perioden vóór de planningsperiode wordt niet gebruikt, ongeacht of het is verbruikt of niet. Het eerste belangrijke prognosecijfer is de datum van of de dichtstbijzijnde datum vóór de begindatum van de planning.  

De prognose kan gelden voor onafhankelijke vraag, zoals verkooporders, of afhankelijke vraag, zoals productieorderonderdelen (moduleprognose). Een artikel kan beide soorten prognoses hebben. Tijdens planning vindt het verbruik afzonderlijk plaats, eerst voor onafhankelijke vraag en dan voor afhankelijke vraag.  

### <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Raamcontractvraag wordt verlaagd door verkooporders  
Prognoses worden aangevuld door het verkoopraamcontract, als manier om toekomstige vraag van een specifieke klant op te geven. Net als bij de (niet gespecificeerde) prognose moeten werkelijke verkopen de verwachte vraag verbruiken en moet het resterende aantal in het vraagvoorraadprofiel worden opgenomen. Door het verbruik wordt het raamcontract niet werkelijk verlaagd.  

De planningsberekening houdt rekening met open verkooporders die zijn gekoppeld aan de specifieke raamcontractregel, maar er wordt geen rekening gehouden met een geldige tijdsperiode. Er wordt ook geen rekening gehouden met geboekte orders, aangezien de boekingsprocedure het openstaande raamcontractaantal al heeft verlaagd.

## <a name="prioritizing-orders"></a>Orders in prioriteitsvolgorde plaatsen
Binnen een bepaalde SKU staat de verzochte of beschikbare datum voor de hoogste prioriteit; de vraag van vandaag moet worden verwerkt vóór de vraag van volgende week. Naast deze algemene prioriteit zal het planningssysteem ook voorstellen aan welk soort vraag moet worden voldaan voordat aan andere vraag wordt voldaan. Zo wordt ook voorgesteld welke voorzieningenbron moet worden toegepast voordat andere voorzieningenbronnen worden toegepast. Dit gebeurt op basis van orderprioriteiten.  

Geladen vraag en aanbod dragen bij aan een profiel voor de voorspelde voorraad op basis van de volgende prioriteiten:  

### <a name="priorities-on-the-demand-side"></a>Prioriteiten aan de vraagkant  
1. Al verzonden: Artikelpost  
2. Inkoopretourorder  
3. Verkooporder  
4. Onderhoudsorder  
5. Behoefte aan productieonderdelen  
6. Assemblageorderregel  
7. Uitgaande transferorder  
8. Raamcontract (dat niet al is verbruikt door verwante verkooporders)  
9. Prognose (die niet al is verbruikt door andere verkooporders)  

> [!NOTE]  
>  Inkoopretouren zijn meestal niet betrokken bij voorraadplanning; ze moeten altijd worden gereserveerd vanuit de lot die geretourneerd zal worden. Indien niet gereserveerd, spelen inkoopretouren een rol in de beschikbaarheid en hebben ze een hoge prioriteit om te voorkomen dat het planningssysteem een voorzieningenorder voorstelt, puur met het oog op een inkoopretour.  

### <a name="priorities-on-the-supply-side"></a>Prioriteiten aan de aanbodkant  
1. Al in voorraad: Artikelpost (Planningsflexibiliteit = geen)  
2. Verkoopretourorder (Planningsflexibiliteit = Geen)  
3. Inkomende transferorder  
4. Productieorder  
5. Assemblageorder  
6. Inkooporder  

### <a name="priority-related-to-the-state-of-demand-and-supply"></a>Prioriteit met betrekking tot de status van vraag en aanbod  
Afgezien van prioriteiten als gevolg van het soort vraag en aanbod geeft de huidige status van de orders in het uitvoeringsproces ook een prioriteit aan. Magazijnactiviteiten hebben bijvoorbeeld invloed en er wordt rekening gehouden met de status van verkoop-, inkoop-, transfer-, assemblage- en productieorders:  

1. Gedeeltelijk verwerkt (Planningsflexibiliteit = Geen)  
2. Al in verwerking in het magazijn (Planningsflexibiliteit = geen)  
3. Vrijgegeven - alle ordersoorten (Planningsflexibiliteit = Onbeperkt)  
4. Vaste geplande productieorder (Planningsflexibiliteit = Onbeperkt)  
5. Gepland/open - alle ordersoorten (Planningsflexibiliteit = Onbeperkt)

## <a name="balancing-supply-with-demand"></a>Aanbod afstemmen op vraag
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

### <a name="rules-concerning-actions-for-supply-events"></a>Regels betreffende acties voor voorzieningsgebeurtenissen  
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

### <a name="determining-the-supply-quantity"></a>Het voorzieningsaantal bepalen  
Planningsparameters die worden gedefinieerd door de gebruiker, bepalen het voorgestelde aantal van elke voorzieningenorder.  

Wanneer met het planningssysteem het aantal van een nieuwe voorzieningenorder of een wijziging van het aantal voor een bestaande voorzieningenorder wordt berekend, kan het voorgestelde aantal verschillen van wat daadwerkelijk wordt gevraagd.  

Als een maximale voorraad of een vast orderaantal is geselecteerd, kan het voorgestelde aantal worden verhoogd om te voldoen aan dat vaste aantal of de maximale voorraad. Als een bestelbeleid een bestelpunt gebruikt, kan het aantal worden verhoogd om ten minste te voldoen aan het bestelpunt.  

 Het voorgestelde aantal kan worden gewijzigd in deze volgorde:  

1. Tot aan het (eventuele) maximale bestelaantal.  
2. Tot aan het minimale bestelaantal.  
3. Tot aan het dichtstbijzijnde ordermeervoud. (In het geval van foutieve instellingen kan dit het maximale orderaantal overschrijden.)  

### <a name="order-tracking-links-during-planning"></a>Ordertraceringskoppelingen tijdens een planning  
Voor wat betreft ordertracering tijdens planning is het belangrijk te vermelden dat het planningssysteem de dynamisch gemaakte ordertraceringskoppelingen herschikt voor de combinaties van artikel/variant/vestiging.  

Hiervoor zijn twee redenen:  

-   Het planningssysteem moet de voorstellen kunnen rechtvaardigen: dat alle vraag is verwerkt en dat er geen overbodige voorzieningenorders zijn.  
-   Dynamisch gemaakte ordertraceringskoppelingen moeten regelmatig worden afgestemd.  

Na verloop van tijd raken dynamische ordertraceringskoppelingen in onbalans aangezien het hele ordertraceringsnetwerk pas wordt herschikt als een vraag- of aanbodgebeurtenis werkelijk wordt afgesloten.  

Voordat voorzieningen op vraag in overeenstemming worden gebracht, worden alle bestaande ordertraceringskoppelingen verwijderd. Vervolgens wordt tijdens de vereffeningsprocedure, wanneer een vraag- of voorzieningsgebeurtenis wordt afgesloten, de nieuwe ordertraceringskoppelingen tot stand gebracht tussen vraag en voorziening.  

> [!NOTE]  
>  Zelfs als het artikel niet is ingesteld voor dynamische ordertracering, maakt het planningssysteem afgestemde ordertraceringskoppelingen, zoals hierboven uitgelegd.
## <a name="closing-demand-and-supply"></a>Vraag en aanbod afsluiten
Wanneer de vereffeningsprocedures voor voorzieningen zijn uitgevoerd, zijn er drie mogelijke eindsituaties:  

* Er is voldaan aan het benodigde aantal en de datum van de vraaggebeurtenissen en de planning hiervoor kan worden afgesloten. De voorzieningsgebeurtenis is nog open en kan de volgende vraag verwerken, zodat de vereffeningsprocedure overnieuw kan starten met de huidige voorzieningsgebeurtenis en de volgende vraag.  
* De voorzieningenorder kan niet worden aangepast om alle vraag te verwerken. De vraaggebeurtenis is nog open, met een niet-gedekt aantal dat mogelijk kan worden gedekt door de volgende voorzieningsgebeurtenis. De huidige voorzieningsgebeurtenis wordt dus afgesloten, zodat de vereffeningsprocedure opnieuw kan starten met de huidige vraag en de volgende voorzieningsgebeurtenis.  
* Alle vraag is gedekt; er is geen verdere vraag (of er is helemaal geen vraag geweest). Als er eventuele surplusvoorziening is, kan deze worden verlaagd (of geannuleerd) en vervolgens gesloten. Het is mogelijk dat er verder in de keten aanvullende voorzieninggebeurtenissen zijn en die moeten ook worden geannuleerd.  

Als laatste maakt het planningssysteem een ordertraceringskoppeling tussen de voorziening en de vraag.  

### <a name="creating-the-planning-line-suggested-action"></a>De planningsregel (voorgestelde actie) maken  
Als een actie - Nieuw, Aantal wijzigen, Herplannen, Herplannen en aantal wijzigen of Annuleren- wordt voorgesteld om de voorzieningenorder te herzien, maakt het planningssysteem een planningsregel in het planningsvoorstel. Vanwege ordertracering wordt de planningsregel niet alleen gemaakt wanneer de voorzieningsgebeurtenis wordt afgesloten, maar ook als de vraaggebeurtenis wordt afgesloten, zelfs als de voorzieningsgebeurtenis nog openstaat en nog kan veranderen als de volgende vraaggebeurtenis wordt verwerkt. Dit betekent dat nadat de planningsregel is gemaakt, deze weer kan worden gewijzigd.  

Om databasetoegang te beperken bij het verwerken van productieorders, kan de planningsregel worden onderhouden op drie niveaus terwijl wordt geprobeerd het minst veeleisende onderhoudsniveau uit te voeren:  

* Maak alleen de planningsregel met de huidige vervaldatum en aantal maar zonder het bewerkingsplan en materialen.  
* Bewerkingsplan opnemen: het geplande bewerkingsplan wordt opgesteld inclusief de berekening van begin- en einddatums en -tijden. Dit is vereist voor wat betreft de databasetoegang. Voor het bepalen van de eind- en vervaldatums kan het noodzakelijk zijn om dit te berekenen, zelfs als de voorzieningsgebeurtenis niet is afgesloten (in het geval van voorwaartse planning).  
* Ontwikkeling stuklijst opnemen: dit kan wachten tot vlak voordat de voorzieningsgebeurtenis wordt gesloten.  

Hiermee worden de omschrijvingen afgerond van hoe vraag en voorzieningen worden geladen, prioriteit krijgen en worden vereffend door het planningssysteem. Bij integratie met deze voorraadplanningactiviteit moet het systeem ervoor zorgen dat het vereiste voorraadniveau van elk gepland artikel wordt onderhouden op basis van het bestelbeleid.

## <a name="see-also"></a>Zie ook  
 [Ontwerpdetails: Centrale begrippen van het planningssysteem](design-details-central-concepts-of-the-planning-system.md)   
 [Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md)   
 [Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)
