---
title: 'Ontwerpdetails: Vraag en aanbod afstemmen'
description: In dit artikel wordt beschreven hoe u doelen kunt prioriteren door vraag en aanbod in evenwicht te brengen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/15/2022
ms.custom: bap-template
---
# <a name="design-details-balancing-supply-and-demand" />Ontwerpdetails: Vraag en aanbod afstemmen

Om te begrijpen hoe het planningssysteem werkt, is het belangrijk om de geprioriteerde doelen te begrijpen:  

* Aan eventuele vraag wordt voldaan door voldoende aanbod.  
* Elk aanbod dient een doel.  

Over het algemeen worden deze doelstellingen bereikt door aanbod met vraag af te stemmen.  

## <a name="supply-and-demand" />Vraag en aanbod

De term *aanbod* verwijst naar elke vorm van positieve of inkomende hoeveelheid, zoals:

* Voorraad
* Inkopen
* Assemblage
* Productie
* Inkomende transfers
* Verkoopretouren  

De term *vraag* verwijst naar elke vorm van brutovraag, zoals:

* Een artikel voor een verkooporder
* Een materiaal voor een productieorder

Met [!INCLUDE [prod_short](includes/prod_short.md)] kunt u bovendien meer technische soorten vraag gebruiken, zoals negatieve voorraad en inkoopretouren.

Om de vele bronnen van vraag en aanbod te sorteren, ordent het planningssysteem deze op twee tijdpaden die voorraadprofielen worden genoemd. Eén profiel is voor vraaggebeurtenissen en het andere is voor de corresponderende aanbodgebeurtenissen. Elke aanbodgebeurtenis vertegenwoordigt één entiteit in een order, zoals:

* Een verkooporderregel
* Een artikelpost
* Een productieorderregel

Wanneer voorraadprofielen worden geladen, worden de vraag/aanbod-combinaties afgestemd om een aanbodplan te maken dat aan de genoemde doelstellingen voldoet.

Voorraadniveaus en planningsparameters zijn andere typen vraag en aanbod. Deze typen ondergaan een geïntegreerde afstemming om voorraadartikelen aan te vullen. Zie voor meer informatie [Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md).

## <a name="the-concept-of-balancing-in-brief" />Het concept van afstemmen in het kort

Vraag komt van uw klanten. Aanbod is wat u kunt maken en verwijderen om te zorgen voor balans. Het planningssysteem begint met de vraag en werkt vervolgens achterwaarts naar het aanbod.  

Voorraadprofielen worden gebruikt om gegevens te bevatten over vraag en aanbod, hoeveelheden en tijd. Deze profielen vormen in principe de twee zijden van de balansschaal.  

Het doel van planning is om vraag en aanbod van een artikel op elkaar af te stemmen om te zorgen dat het aanbod voldoet aan de vraag zoals wordt bepaald door de planningsparameters en -regels.  

:::image type="content" source="media/nav_app_supply_planning_2_balancing.png" alt-text="Overzicht van vraag- en aanbodafstemming.":::

## <a name="process-orders-before-the-planning-start-date" />Orders verwerken vóór de startdatum van de planning

Om te voorkomen dat een aanbodplan onredelijke suggesties doet, plant het planningssysteem niets in de periode voor de startdatum van de planning. De volgende regel geldt voor die periode:

* Alle vraag en aanbod vóór de begindatum van de planningsperiode wordt beschouwd als deel van de voorraad of wordt verzonden.  

Op enkele uitzonderingen na zal het planningssysteem geen wijzigingen voorstellen voor aanvulorders in de periode of koppelingen voor ordertracering voor die periode maken. Dit zijn uitzonderingen op deze regel:  

* De voorraad die wordt verwacht beschikbaar te zijn, inclusief totale vraag en aanbod in de periode, is kleiner dan nul.  
* Geantidateerde orders vereisen serie- of lotnummers.  
* De vraag/aanbod-combinatie wordt gekoppeld door een order-naar-order beleid. 

Als de eerste beschikbare voorraad onder nul is, wordt er op de dag vóór de planningsperiode door het planningssysteem een noodvoorzieningenorder voorgesteld voor het ontbrekende aantal. Dus is de voorspelde en beschikbare voorraad altijd minstens nul wanneer het plannen voor de toekomstige periode begint. De planningsregel voor deze aanvulorder geeft een noodgevalpictogram weer en extra gegevens.

### <a name="serial-and-lot-numbers-and-order-to-order-links-are-exempt-from-the-previous-period" />Serie-/lotnummers en order-naar-order koppelingen zijn vrijgesteld van de vorige periode

Als serie- of lotnummers vereist zijn of als er een order-naar-order-koppeling bestaat, negeert het planningssysteem de regel over de vorige periode. De systeem neemt geantidateerde hoeveelheden op vanaf de startdatum en kan corrigerende acties voorstellen als vraag en aanbod niet gesynchroniseerd zijn. Deze vraag/aanbodcombinaties moeten overeenkomen om ervoor te zorgen dat aan een specifieke vraag wordt voldaan.

## <a name="load-inventory-profiles" />Voorraadprofielen laden

Om de vele bronnen van vraag en aanbod te sorteren, ordent het planningssysteem deze op twee tijdpaden die voorraadprofielen worden genoemd.  

Vraag en aanbod met vervaldatums op of na de begindatum van de planning worden in elk voorraadprofiel geladen. Bij het laden worden de soorten vraag en aanbod gesorteerd volgens algemene prioriteiten, zoals:

* Vervaldatum
* Low-levelcodes
* Locatie
* Variant

Orderprioriteiten worden op de verschillende typen toegepast om de belangrijkste vraag het eerst af te handelen. Zie voor meer informatie [Orders prioriteit geven](design-details-balancing-demand-and-supply.md#prioritize-orders).  

Vraag kan ook negatief zijn. Behandel negatieve vraag als aanbod. In tegenstelling tot normaal aanbod wordt negatieve vraag echter beschouwd als vast aanbod. Het planningssysteem kan hier rekening mee houden, maar er worden geen wijzigingen in voorgesteld.  

Over het algemeen beschouwt het planningssysteem alle voorzieningenorders na de begindatum van de planning als vatbaar voor wijziging om aan vraag te voldoen. Nadat een hoeveelheid is geboekt vanuit een aanvulorder, kan deze echter niet meer door het planningssysteem worden gewijzigd. De volgende orders kunnen niet opnieuw worden gepland:  

* Vrijgegeven productieorders waarbij het verbruik of de output is geboekt.  
* Assemblageorders waarbij het verbruik of de output is geboekt.  
* Transferorders waarop verzending is geboekt.  
* Inkooporders waarop ontvangst is geboekt.  

Afgezien van het laden van de typen vraag en aanbod worden bepaalde typen geladen met het oog op speciale regels en afhankelijkheden. In de volgende secties in dit artikel worden deze regels en afhankelijkheden beschreven.  

### <a name="item-dimensions-are-separated" />Artikeldimensies worden gescheiden

Het aanbodplan moet worden berekend per combinatie van artikeldimensies, zoals variant en vestiging. Alleen de combinaties met vraag en/of aanbod moeten worden berekend.  

Het planningssysteem zoekt naar combinaties in het voorraadprofiel. Wanneer een nieuwe combinatie wordt gevonden, wordt een interne besturingsrecord gemaakt die de informatie over de combinatie bevat. De SKU wordt dan ingevoerd als besturingsrecord of buitenste lus. Daarom worden de planningsparameters op basis van een combinatie van variant en vestiging ingesteld en kan het systeem doorgaan naar de binnenlus. 

> [!NOTE]  
> U hoeft geen SKU-record in te voeren tijdens het invoeren van vraag en/of aanbod voor een bepaalde combinatie van variant en vestiging. Wanneer er geen SKU bestaat voor een bepaalde combinatie, maakt [!INCLUDE [prod_short](includes/prod_short.md)] daarom een tijdelijke SKU op basis van het artikel. Als de schakelaar **Vestiging verplicht** is ingeschakeld op de **pagina Voorraadinstellingen**, moet u een SKU maken of de schakelaar **Onderdelen op vestiging** inschakelen. Zie voor meer informatie [Planning met of zonder vestigingen](production-planning-with-without-locations.md).  

### <a name="serial-and-lot-numbers-are-loaded-by-specification-level" />Serie- en lotnummers worden geladen op specificatieniveau

Serie- en lotnummers worden in de voorraadprofielen geladen met de vraag en het aanbod waaraan ze zijn toegewezen.  

Vraag- en aanbodkenmerken worden gerangschikt op orderprioriteit en op het niveau van specificatie. Omdat serie- en lotnummerovereenkomsten het specificatieniveau weerspiegelen, zal een meer specifieke vraag eerder overeenkomen dan een minder specifieke vraag. Een specifieke vraag kan bijvoorbeeld een lotnummer zijn dat is opgegeven voor een verkoopregel. Een minder specifieke vraag kan een verkoop van een willekeurig lotnummer zijn.

> [!NOTE]  
> De enige speciale prioriteitsregels voor vraag en aanbod met serie- en lotnummers, zijn het specificatieniveau dat wordt gedefinieerd door de combinaties ervan en de instelling van artikeltracering voor de artikelen.  

Tijdens het afstemmen beschouwt het planningssysteem aanbod met serie- en lotnummers als inflexibel. Het systeem zal dergelijke aanvulorders niet vergroten of opnieuw plannen. De enige uitzondering hierop is als ze worden gebruikt in een order-naar-order-relatie. Zie voor meer informatie [Order-naar-order koppelingen worden nooit verbroken](#order-to-order-links-are-never-broken). Deze uitzondering beschermt het aanbod tegen het ontvangen van verschillende, mogelijk conflicterende, actieberichten wanneer het verschillende kenmerken heeft. Er kunnen bijvoorbeeld verschillende kenmerken zijn wanneer het aanbod een verzameling verschillende serienummers heeft.  

Een andere reden waarom aanbod met serie- en lotnummers inflexibel is, is dat serie- en lotnummers vaak laat in het proces worden toegekend. Het kan verwarrend zijn als er op dat moment wijzigingen worden voorgesteld.  

Het afstemmen van serie- en lotnummers respecteert niet de regel om niets te plannen vóór de startdatum van de planning. Als vraag en aanbod niet zijn gesynchroniseerd, zal het planningssysteem wijzigingen of nieuwe orders voorstellen, ongeacht de geplande begindatum.  

### <a name="order-to-order-links-are-never-broken" />Order-naar-order koppelingen worden nooit verbroken

Bij het plannen van een order-naar-order-artikel moet het gekoppelde aanbod alleen worden gebruikt voor waarvoor het oorspronkelijk is bedoeld. De gekoppelde vraag moet niet door een willekeurig ander aanbod worden gedekt, zelfs wanneer het aanbod beschikbaar is wat betreft tijd en aantal. Een assemblageorder die is gekoppeld aan een verkooporder in een op-order-assembleren scenario, kunt u bijvoorbeeld niet gebruiken om aan andere vraag te voldoen.  

Order-naar-order vraag en aanbod moeten precies afgestemd zijn. Het planningssysteem waarborgt het aanbod zonder rekening te houden met parameters voor ordergrootte, wijzigingen en aantallen in voorraad (buiten de aantallen die betrekking hebben op de gekoppelde orders). Om dezelfde reden stelt het systeem voor overschotaanbod te verlagen als de gekoppelde vraag wordt verlaagd.  

Deze vereffening heeft ook invloed op de timing. Er wordt geen rekening gehouden met de beperkte horizon die wordt opgegeven door het tijdsinterval; de voorziening wordt opnieuw gepland als het tijdschema van de vraag wordt gewijzigd. Er wordt echter rekening gehouden met de dempingstijd en het wordt voorkomen dat order-naar-order voorzieningen worden uitgepland, behalve de interne voorzieningen van een productieorder met meerdere niveaus (projectorder).  

> [!NOTE]  
> Serie- en lotnummers kunnen ook worden opgegeven voor order-op-order vraag. In dat geval is het aanbod niet inflexibel, wat normaal wel het geval is met serie- en lotnummers. In dit geval brengt het systeem een verhoging of verlaging aan, afhankelijk van wijzigingen in de vraag. Als één vraag bovendien variërende serie- en lotnummers heeft, zoals meerdere lotnummers, wordt voor elke lot één voorraadorder voorgesteld.  

> [!NOTE]  
> Prognoses moeten niet leiden tot het maken van voorzieningenorders die zijn gebonden door een order-op-order koppeling. Als de prognose wordt gebruikt, moet deze alleen worden gebruikt als generator van afhankelijke vraag in een productieomgeving.

### <a name="component-need-is-loaded-according-to-production-order-changes" />Materiaalbehoefte wordt geladen op basis van wijzigingen in productieorders

Bij de verwerking van productieorders moet het planningssysteem de benodigde materialen controleren voordat ze in het vraagprofiel worden geladen. Materiaalregels die voortvloeien uit een gewijzigde productieorder vervangen de regels uit de oorspronkelijke order. De wijziging zorgt ervoor dat het planningssysteem geen dubbele planningsregels maakt voor een materiaalbehoefte.  

### <a name="consume-safety-stock" />Veiligheidsvoorraad verbruiken

Veiligheidsvoorraad is vraag die in het voorraadprofiel wordt geladen op de begindatum van de planning.  

Veiligheidsvoorraad is een voorraadhoeveelheid die opzij is gezet om onzekerheden in de vraag te compenseren tijdens aanvulling. Het kan echter worden verbruikt om aan een vraag te voldoen. In dat geval zorgt het planningssysteem ervoor dat de veiligheidsvoorraad snel aangevuld wordt. Het systeem stelt een aanvulorder voor om de veiligheidsvoorraad aan te vullen op de datum waarop deze wordt verbruikt. De planningsregel zal een pictogram van een uitzonderingswaarschuwing bevatten, zodat de planner weet dat de veiligheidsvoorraad gedeeltelijk of volledig is verbruikt door een uitzonderingsorder voor het ontbrekende aantal.  

### <a name="forecast-demand-is-reduced-by-sales-orders" />Prognosevraag wordt verlaagd door verkooporders

Vraagprognoses drukken verwachte toekomstige vraag uit. Wanneer werkelijke vraag wordt ingevoerd, meestal als verkooporders voor geproduceerde artikelen, wordt de prognose verbruikt.

De prognose zelf wordt niet verlaagd door verkooporders. De prognosehoeveelheden die in de planningsberekening worden gebruikt, worden echter verlaagd met de verkooporderaantallen voordat de eventuele resterende hoeveelheid in het vraagprofiel wordt opgenomen. Voor verkopen gedurende een periode omvat de planning zowel openstaande verkooporders als artikelposten van verzonden verkopen. De uitzondering op deze regel is wanneer ze afkomstig zijn van een raamcontract.  

U moet een geldige prognoseperiode definiëren. De datum van het prognoseaantal definieert het begin van de periode, en de datum op de volgende prognose bepaalt het einde van de periode.  

De prognose voor perioden vóór de planningsperiode wordt niet gebruikt, ongeacht of het is verbruikt of niet. Het eerste belangrijke prognosecijfer is de begindatum van de planning of de datum die daar het dichtst bij ligt.  

De prognose kan voor verschillende soorten vraag zijn:

* Onafhankelijke vraag, zoals verkooporders
* Afhankelijke vraag, zoals productieordermateriaal

Een artikel kan beide soorten prognoses hebben. Tijdens planning vindt het verbruik afzonderlijk plaats, eerst voor onafhankelijke vraag en dan voor afhankelijke vraag.  

### <a name="blanket-order-demand-is-reduced-by-sales-orders" />Raamcontractvraag wordt verlaagd door verkooporders

Prognoses worden aangevuld door verkoopraamcontracten, als manier om toekomstige vraag van een specifieke klant op te geven. Net als bij de (niet gespecificeerde) prognose moeten werkelijke verkopen de verwachte vraag verbruiken en moet het resterende aantal in het vraagvoorraadprofiel worden opgenomen. Verbruik vermindert de hoeveelheid van raamcontracten niet.

De planningsberekening houdt rekening met open verkooporders die zijn gekoppeld aan de specifieke raamcontractregel, maar niet met een geldige tijdsperiode. Er wordt ook geen rekening gehouden met geboekte orders, aangezien de boekingsprocedure het openstaande raamcontractaantal al heeft verlaagd.

## <a name="prioritize-orders" />Orders in prioriteitsvolgorde plaatsen

Binnen een bepaalde SKU vertegenwoordigt de gevraagde of beschikbare datum de hoogste prioriteit. De vraag van vandaag moet worden afgehandeld vóór de vraag van volgende week. Maar naast deze algemene prioriteit zal het planningssysteem de volgende suggesties doen op basis van volgordeprioriteiten:

* Aan welk type vraag u als eerste moet voldoen.
* Welke aanbodbron moet worden toegepast voordat andere aanbodbronnen worden toegepast.  

Geladen vraag en aanbod dragen bij aan een profiel voor voorspelde voorraad op basis van de volgende prioriteiten.  

### <a name="priorities-on-the-demand-side" />Prioriteiten aan de vraagkant

1. Al verzonden: Artikelpost  
2. Inkoopretourorder  
3. Verkooporder  
4. Serviceorder  
5. Behoefte aan productiemateriaal  
6. Assemblageorderregel  
7. Uitgaande transferorder  
8. Raamcontract (dat niet al is verbruikt door verwante verkooporders)  
9. Prognose (die niet al is verbruikt door andere verkooporders)  

> [!NOTE]  
> Inkoopretouren zijn meestal niet betrokken bij voorraadplanning; ze moeten altijd worden gereserveerd vanuit de lot die geretourneerd zal worden. Indien niet gereserveerd, spelen inkoopretouren een rol in de beschikbaarheid en hebben ze een hoge prioriteit om te voorkomen dat het planningssysteem een aanvulorder voorstelt, puur met het oog op een inkoopretour.  

### <a name="priorities-on-the-supply-side" />Prioriteiten aan de aanbodkant

1. Al in voorraad: Artikelpost (Planningsflexibiliteit = geen)  
2. Verkoopretourorder (Planningsflexibiliteit = Geen)  
3. Inkomende transferorder  
4. Productieorder  
5. Assemblageorder  
6. Inkooporder  

### <a name="priority-related-to-the-state-of-supply-and-demand" />Prioriteit met betrekking tot de status van vraag en aanbod

Naast de prioriteiten vanuit het type vraag en aanbod zijn er nog andere zaken die van invloed zijn op de planningsflexibiliteit. Bijvoorbeeld magazijnactiviteiten en de status van de volgende orders:

* Verkopen
* Inkoop
* Transfer
* Assemblage
* Productie

De status van deze orders heeft de volgende effecten: 

1. Gedeeltelijk verwerkt (Planningsflexibiliteit = Geen)  
2. Al in verwerking in het magazijn (Planningsflexibiliteit = geen)  
3. Vrijgegeven - alle ordersoorten (Planningsflexibiliteit = Onbeperkt)  
4. Vaste geplande productieorder (Planningsflexibiliteit = Onbeperkt)  
5. Gepland/open - alle ordersoorten (Planningsflexibiliteit = Onbeperkt)

## <a name="balancing-supply-with-demand" />Aanbod afstemmen op vraag

Het planningssysteem brengt vraag en aanbod in evenwicht door acties voor te stellen om aanvulorders te herzien die niet in evenwicht zijn. Deze afstemming gebeurt voor elke combinatie van variant en locatie.  

Stel u voor dat elk voorraadprofiel twee reeksen bevat:

* Een reeks vraaggebeurtenissen, gesorteerd op datum en prioriteit
* Een overeenkomstige reeks aanbodgebeurtenissen

Elke gebeurtenis verwijst naar de bronsoort en de identificatie. De regels voor afstemming van het artikel zijn eenvoudig. Vraag en aanbod afstemmen kan als volgt op een bepaald moment in het proces optreden:  

1. Er bestaat geen vraag of voorziening voor het artikel => de planning is voltooid (of moet niet beginnen.)  
2. Vraag bestaat maar er is geen aanbod => aanbod moet worden voorgesteld.  
3. Er is aanbod maar er is geen vraag naar => aanbod moet worden geannuleerd.  
4. Zowel vraag als aanbod bestaan => er moeten vragen worden gesteld en beantwoord voordat [!INCLUDE [prod_short](includes/prod_short.md)] kan zorgen dat het aanbod aan de vraag kan voldoen.

    Als de timing van het aanbod niet geschikt is, kan het aanbod wellicht als volgt opnieuw worden gepland:  

    1. Als het aanbod eerder wordt geplaatst dan de vraag, kan het aanbod mogelijk opnieuw worden gepland, zodat de voorraad zo klein mogelijk is.  
    2. Als het aanbod later dan de vraag is geplaatst, kan het aanbod mogelijk voorwaarts worden gepland. Anders stelt het systeem nieuw aanbod voor.  
    3. Als het aanbod op de datum voldoet aan de vraag, kan het planningssysteem doorgaan met te analyseren of de hoeveelheid van het aanbod aan de vraag kan voldoen.  

    Als de timing eenmaal duidelijk is, kan de aan te bieden hoeveelheid als volgt worden berekend:  

    1. Als de aanbodhoeveelheid kleiner is dan de vraag, kan de aanbodhoeveelheid worden vergroot (of niet, als u een beleid voor maximale hoeveelheid hebt).  
    2. Als de aanbodhoeveelheid groter is dan de vraag, kan de aanbodhoeveelheid worden verkleind (of niet, als u een beleid voor minimale hoeveelheid hebt).  

    Op dit punt bestaat een van de volgende twee situaties:  

    1. De huidige vraag kan worden verwerkt. In dat geval kan het worden afgesloten en kan de planning voor de volgende vraag beginnen.  
    2. De voorziening heeft het maximum bereikt, waardoor een deel van het vraagaantal niet gedekt is. In dit geval kan het planningssysteem de huidige voorraad sluiten en doorgaan naar de volgende.  

 De procedure begint opnieuw met de volgende vraag en het huidige aanbod of andersom. De huidige voorzieningen kunnen mogelijk deze volgende vraag ook verwerken, of de huidige vraag is nog niet volledig verwerkt.  

### <a name="rules-for-actions-for-supply-events" />Regels voor acties voor aanbodgebeurtenissen

Voor verticale berekeningen waarbij het aanbod aan de vraag moet voldoen, wordt de vraag als een gegeven beschouwd. Het valt buiten de controle van het planningssysteem. Het planningssysteem kan echter de aanbodzijde beheren en zal de volgende suggesties doen:

* Nieuwe aanvulorders maken
* Bestaande orders opnieuw plannen of de hoeveelheden ervan wijzigen
* Aanvulorders annuleren die niet langer nodig zijn  

Als u een aanvulorder wil uitsluiten van de planningsuggesties, kunt u stellen dat deze geen planningsflexibiliteit heeft (Planningsflexibiliteit = Geen). Overtollige voorzieningen van die order worden dan gebruikt om de vraag te verwerken, maar er wordt geen actie voorgesteld. 

In het algemeen heeft elk aanbod een planningsflexibiliteit die wordt beperkt door de voorwaarden van elk van de voorgestelde acties.  

* **Opnieuw uitplannen**: de datum van een bestaande voorzieningenorder kan worden uitgepland om te voldoen aan de vervaldatum van de vraag tenzij:

  * De order vertegenwoordigt voorraad (altijd op dag nul).  
  * De order een order-naar-order koppeling met andere vraag heeft.  
  * Het ligt buiten het bereik om opnieuw te plannen in het tijdsinterval.
  * Er is een aanbod dichterbij dat kan worden gebruikt.  
  * Van de andere kant kan de gebruiker besluiten niet te herplannen omdat:
  * De aanvulorder is gekoppeld aan een andere vraag op een eerdere datum.  
  * De benodigde herplanning is zo minimaal dat deze verwaarloosbaar is.  

* **Opnieuw inplannen**: de datum van een bestaande aanvulorder kan worden gepland, behalve in de volgende omstandigheden:

  * De order is direct aan andere vraag gekoppeld.  
  * Het ligt buiten het bereik om opnieuw te plannen zoals gedefinieerd in het tijdsinterval.

> [!NOTE]  
> Wanneer u een artikel via een bestelpunt plant, kunt u de aanvulorder opnieuw plannen. Dit komt vaak voor bij voorwaarts geplande aanvulorders die worden geactiveerd door een bestelpunt.

* **Aantal verhogen**: Het aantal van een bestaande voorzieningenorder kan worden verhoogd om aan de vraag te voldoen, tenzij de voorzieningenorder rechtstreeks aan een vraag is gekoppeld door een order-op-order koppeling.  

> [!NOTE]  
> Hoewel u de aanvulorder kunt vergroten, kan de vergroting beperkt worden door een gedefinieerde maximale orderhoeveelheid.  

* **Aantal verlagen**: Een bestaande voorzieningenorder met een surplus vergeleken met bestaande vraag kan worden verminderd om aan de vraag te voldoen.  

> [!NOTE]  
> Hoewel de hoeveelheid kan worden verlaagd, kan er toch nog overschot zijn in vergelijking met de vraag wegens een gedefinieerde minimale orderhoeveelheid of orderveelvoud. 

* **Annuleren**: als een speciaal geval van de aantal verlagende actie kan de aanvulorder worden geannuleerd als deze tot nul is verlaagd. 
* **Nieuw**: als er nog geen aanvulorders bestaan en er geen bestaande order kan worden gewijzigd om op de gevraagde vervaldatum te voldoen aan de benodigde hoeveelheid, wordt een nieuwe aanvulorder voorgesteld.  

### <a name="determine-the-supply-quantity" />De aanbodhoeveelheid bepalen

U definieert de planningsparameters die de voorgestelde hoeveelheid van elke aanvulorder bepalen.  

Wanneer met het planningssysteem het aantal van een nieuwe aanvulorder of de wijziging van de hoeveelheid voor een bestaande order wordt berekend, kan de voorgestelde hoeveelheid verschillen van de werkelijke vraag.  

Als een maximale voorraad of vaste orderhoeveelheden worden geselecteerd, kan de voorgestelde hoeveelheid worden verhoogd om te voldoen aan die vaste hoeveelheid of de maximale voorraad. Als een bestelbeleid een bestelpunt gebruikt, kan het aantal worden verhoogd om ten minste te voldoen aan het bestelpunt. 

De voorgestelde hoeveelheid kan worden gewijzigd in deze volgorde:  

1. Tot aan de maximale orderhoeveelheid.  
2. Tot aan het minimale bestelaantal.  
3. Tot aan het dichtstbijzijnde ordermeervoud.

### <a name="order-tracking-links-during-planning" />Ordertraceringskoppelingen tijdens planning

Voor het volgen van orders tijdens planning herschikt het planningssysteem de koppelingen voor het volgen van orders voor de combinaties van artikelen, varianten en vestigingen. Het systeem herschikt de traceringskoppelingen om de volgende redenen:

* Om de suggesties voor het dekken van alle vraag te verifiëren en ervoor te zorgen dat alle aanvulorders nodig zijn.  
* De koppelingen voor het volgen van orders moeten regelmatig opnieuw worden afgestemd.  

Na verloop van tijd raken de koppelingen voor het volgen van orders uit balans. De koppelingen raken uit balans omdat het netwerk voor het volgen van orders pas wordt herschikt als een vraag- of aanbodgebeurtenis is gesloten.

Voordat aanbod op vraag wordt afgestemd, worden alle bestaande ordertraceringskoppelingen verwijderd. Tijdens de afstemmingsprocedure, wanneer een vraag- of aanbodgebeurtenis wordt gesloten, worden nieuwe ordertraceringskoppelingen gemaakt tussen de vraag en het aanbod.  

> [!NOTE]  
> Zelfs als het artikel niet is ingesteld voor dynamische ordertracering, maakt het planningssysteem afgestemde ordertraceringskoppelingen.

## <a name="close-balanced-supply-and-demand" />Afgestemde vraag en aanbod sluiten

Het afstemmen van aanbod heeft drie mogelijke uitkomsten:

* Er is voldaan aan de benodigde hoeveelheid en datum van de vraaggebeurtenissen en de planning hiervoor kan worden afgesloten. De aanbodgebeurtenis blijft open en kan mogelijk aan de volgende vraag voldoen. Doordat de aanbodgebeurtenis open wordt gehouden, kan de afstemmingsprocedure opnieuw beginnen met de huidige aanbodgebeurtenis en de volgende vraag.  
* De aanvulorder kan niet worden aangepast om aan alle vraag te voldoen. De vraaggebeurtenis is nog open, met een niet-gedekt aantal dat mogelijk kan worden gedekt door de volgende aanbodgebeurtenis. De huidige aanbodgebeurtenis wordt daarom afgesloten en de afstemmingsprocedure kan opnieuw beginnen met de huidige vraag en de volgende aanbodgebeurtenis.  
* Alle vraag is gedekt en er is geen volgende vraag (of er was helemaal geen vraag). Surplusaanbod kan deze worden verkleind (of geannuleerd) en vervolgens gesloten. Alle andere aanbodgebeurtenissen moeten ook worden geannuleerd.  

Als laatste maakt het planningssysteem een ordertraceringskoppeling tussen het aanbod en de vraag.  

### <a name="create-the-planning-line-suggested-action" />De planningsregel maken (voorgestelde actie)

Als een actie **Nieuw**, **Aantal wijzigen**, **Herplannen**, **Herplannen en aantal wijzigen** of **Annuleren** wordt voorgesteld om de aanvulorder te herzien, maakt het planningssysteem een planningsregel in het planningsvoorstel. Voor ordertracering wordt de planningsregel niet alleen gemaakt wanneer de aanbodgebeurtenis wordt gesloten, maar ook als de vraaggebeurtenis wordt gesloten. Dit geldt ook al is de aanbodgebeurtenis nog open en kan deze worden gewijzigd wanneer de volgende vraaggebeurtenis wordt verwerkt. De planningsregel kan weer worden gewijzigd wanneer deze wordt gemaakt.

Om de belasting van de database bij het afhandelen van productieorders te verminderen, kan de planningsregel op drie niveaus worden beheerd:

* Maak alleen de planningsregel met de huidige vervaldatum en aantal maar zonder het bewerkingsplan en materialen.  
* Bewerkingsplan opnemen: het geplande bewerkingsplan omvat berekening van begin- en einddatums en -tijden. Bewerkingsplan opnemen is veeleisend voor wat betreft databasetoegang. Voor het bepalen van de eind- en vervaldatums kan het noodzakelijk zijn om het bewerkingsplan te berekenen, zelfs als de aanbodgebeurtenis niet is afgesloten. Bijvoorbeeld als u voorwaartse planning doet.  
* Ontwikkeling stuklijst opnemen: dit kan gebeuren vlak voordat de aanbodgebeurtenis wordt gesloten.

## <a name="see-also" />Zie ook

[Ontwerpdetails: Centrale begrippen van het planningssysteem](design-details-central-concepts-of-the-planning-system.md)  
[Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md)  
[Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
