---
title: Picken voor interne bewerkingen in geavanceerde magazijnconfiguraties
description: 'Als uw locaties picking en verzending gebruiken, pickt u componenten voor assemblage- en taakactiviteiten op de pagina Magazijnpick.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/02/2022
ms.author: bholtorf
---
# Picken voor productie, assemblage of taken in geavanceerde magazijnconfiguraties

Hoe u materialen voor productie, projecten of assemblageorders verzamelt, is afhankelijk van de vestigingsinstellingen van uw magazijn. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).

Zet in een geavanceerde magazijnconfiguratie voor de uitgaande stroom (pick) de schakelaars **Pick vereisen** en **Verzenden vereisen** aan op de pagina **Locatiekaart** voor de locatie.

Als voor de locatie magazijnpickverwerking en magazijnverzendingsverwerking is vereist, gebruikt u magazijnpickdocumenten om de pickinformatie te beheren voordat u het gebruik of verbruik van materialen boekt.  

Vervolgens kunt u een compleet nieuw magazijnpickdocument maken. Picks maken deel uit van een werkstroom waarbij een persoon die een order verwerkt ze op een push-manier maakt, of de magazijnmedewerker maakt ze op een pull-manier:

- Op een push-manier, waarbij u de actie **Pick maken** gebruikt op de pagina **Productieorder**, **Assemblageorder**, **Projectkaart**. Selecteer de te picken regels en bereidt de picks voor door bijvoorbeeld op te geven uit welke opslaglocaties moet worden gepickt en in welke moet worden opgeslagen en hoeveel eenheden moeten worden verwerkt. Opslaglocaties kunnen vooraf worden gedefinieerd voor de magazijnlocatie of resource.
- Op een pull-manier, waarbij u **Productieorder**, **Assemblageorder**, **Projectkaart** naar het magazijn vrijgeeft om de artikelen beschikbaar te maken voor picken. Daarna kunnen magazijnmedewerkers op de pagina **Pickvoorstel** de actie **Magazijndocumenten ophalen** om hun toegewezen picks te krijgen.

Om materialen voor brondocumenten op een pull-manier te verzamelen of te verplaatsen, moet u het brondocument vrijgeven om het klaar te maken voor picking. Voor interne doeleinden kunnen brondocumenten op de volgende manieren vrijgegeven worden.  

|Brondocument|Vrijgavemethode|  
|---------------------|--------------------|  
|Productieorder|Wijzig de orderstatus in Vrijgegeven of maak direct een vrijgegeven productieorder.|  
|Assemblageorder|Status wijzigen in Vrijgegeven.|
|Projecten | Wijzig de status in Open of maak direct een project met de status Open.|  

## Productie

Gebruik **Magazijnpick**-documenten om productiematerialen in de stroom naar productie te picken.

Voor een locatie die opslaglocaties gebruikt om artikelen te verplaatsen naar grijpvoorraadlocaties, kunt u de volgende methoden gebruiken:

* Voor een locatie die gestuurde opslag en pick gebruikt, volgt u de stappen in het artikel [Artikelen verplaatsen in geavanceerde magazijnconfiguraties](warehouse-how-to-move-items-in-advanced-warehousing.md) .
* Voor andere locaties volgt u de stappen in het artikel [Artikelen ongepland verplaatsen in standaardmagazijnconfiguraties](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

## Assemblage  

Gebruik **Magazijnpick**-documenten om assemblagematerialen naar het assemblagegebied te verplaatsen.

[!INCLUDE [prod_short](includes/prod_short.md)] ondersteunt assemblagestromen van het type op voorraad assembleren en op order assembleren. Ga voor meer informatie over assembleren voor order in de uitgaande magazijnstroom naar [Artikelen voor assembleren voor order in magazijnverzendingen](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

## Projectbeheer  

Gebruik **Magazijnpick**-documenten om projectmaterialen in de stroom naar projectbeheer te picken.

> [!NOTE]
> De mogelijkheid om componenten voor taakplanningsregels te picken is toegevoegd aan [!INCLUDE[d365fin](includes/d365fin_md.md)] in 2022 releasewave 2. Om de mogelijkheid te gebruiken, moet een beheerder **Functie-update: Voorraad- en magazijnpicks vanuit projecten inschakelen** inschakelen op de pagina **Functiebeheer**.
>
> Projecten bieden geen ondersteuning voor geavanceerde configuraties waarbij de schakelaar **Gericht picken en opslaan** is ingeschakeld.

## Bulksgewijs pickdocumenten maken met het pickvoorstel

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Pickvoorstel** in en kies vervolgens de gerelateerde koppeling.  

2. Kies de actie **Magazijndocumenten ophalen**.  

    De lijst toont de vrijgegeven productie, projecten, assemblageorders die zijn doorgestuurd naar de pickfunctie. De orders omvatten de orders waarvoor al pickinstructies zijn gemaakt. De lijst bevat geen documenten met pickregels die volledig zijn gepickt en geregistreerd.  
3. Selecteer de orders waarvoor u een pick wilt voorbereiden.

    > [!NOTE]  
    > Als u een document selecteert dat al instructies heeft voor alle regels, [!INCLUDE [prod_short](includes/prod_short.md)] geeft dit aan dat er niets te behandelen is. Om de al gemaakte pickinstructies voor het magazijn te combineren tot één efficiënte pickinstructie, verwijdert u eerst de afzonderlijke magazijnpicks.

4. Vul het veld **Sorteringsmethode** in om de regels op de gewenste wijze te sorteren.  

    > [!NOTE]  
    > De manier waarop de regels in het werkblad worden gesorteerd, wordt niet automatisch doorgevoerd in de pickinstructie. Er zijn echter dezelfde sorteerhulpmiddelen beschikbaar, samen met opslaglocatievolgorde. U kunt de volgorde van de regels die u in het voorstel plant gemakkelijk opnieuw bepalen wanneer u de pickinstructies maakt of door te sorteren in de pickinstructies.

5. Vul het veld **Te verwerken aantal** in. Kies de actie **Te verwerken aantal autom. invullen** of vul de velden handmatig in.  

    De pagina toont de beschikbare hoeveelheden in cross-dockopslaglocaties, wat handig is voor het plannen van werktoewijzingen in cross-docksituaties. [!INCLUDE[prod_short](includes/prod_short.md)] stelt altijd eerst een pick uit een cross-dockopslaglocatie voor.

6. U kunt de regels zo nodig handmatig bewerken. U kunt ook bepaalde regels verwijderen om de pick nog efficiënter te maken. Als er bijvoorbeeld meerdere regels zijn met artikelen in cross-dockopslaglocaties, kunt u een pick maken voor alle regels. De cross-dockartikelen worden dan gepickt, samen met de andere artikelen in het brondocument, en in de cross-docklocaties komt ruimte vrij voor andere binnenkomende artikelen.

    > [!NOTE]  
    >  De regels worden alleen uit het voorstel verwijderd, niet uit de pickselectielijst.  

7. Kies de actie **Pick maken**. De pagina **Pick maken** wordt geopend, waar u meer informatie aan de pick kunt toevoegen.  

    Geef op hoe pickregels moten worden gesorteerd in de pickdocumenten door een van de volgende opties te selecteren.  

    |Optie|Omschrijving|
    |-|-|
    |Per magazijn Document|Maakt afzonderlijke pickdocumenten voor regels van het werkblad met hetzelfde magazijn-brondocument.|
    |Per klant/leverancier/vestiging|Maakt afzonderlijke pickdocumenten voor elke klant (projecten)|
    |Per artikel|Maakt afzonderlijke pickdocumenten voor elk artikel in het pickvoorstel.|
    |Per Van zone|Maakt afzonderlijke pickdocumenten voor elke zone waar u de artikelen uit haalt.|
    |Per opslaglocatie|Maakt afzonderlijke pickdocumenten voor elke opslaglocatie waar u de artikelen uit haalt.|
    |Per vervaldatum|Maakt afzonderlijke pickdocumenten voor brondocumenten die dezelfde vervaldatum hebben.|

    Geef op hoe de pickdocumenten moeten worden gemaakt door een selectie te maken uit de volgende opties.  

    |Optie|Omschrijving|
    |-|-|
    |Max. Nee Pickregels|Maakt pickdocumenten die niet meer dan het opgegeven aantal regels in een document hebben.|
    |Max. Nee pickbrondocumenten.|Maakt pickdocumenten die niet meer dan het opgegeven aantal brondocumenten hebben.|
    |Toegewezen gebruikers-id|Maakt pickdocumenten alleen voor voorstelregels die zijn toegewezen aan de geselecteerde magazijnmedewerker.|
    |Sorteringsmethode voor pickregels|Selecteer uit de beschikbare opties om regels te sorteren in het gemaakte pickdocument.|
    |Breakbulkfilter plaatsen|Verbergt tussenliggende bulksplitsing pickregels wanneer een grotere eenheid wordt omgezet in een kleinere eenheid en volledig wordt gepickt.|
    |Te verwerken aantal niet opvullen|Laat het veld **Te verwerken aantal** leeg op de gemaakte pickregels.|
    |Pick afdrukken|Drukt de pickdocumenten af wanneer ze worden gemaakt. U kunt ook afdrukken vanuit de gemaakte pickdocumenten.|

8. Kies de knop **Ok**.  

## Artikelen picken voor een productieorder, assemblageorder, project

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Picks** in en kies vervolgens de gerelateerde koppeling.  

    Als u een bepaalde pick wilt bewerken, selecteert u het pickformulier in het overzicht. U kunt het overzicht ook filteren op picks die aan u zijn toegewezen. De pickkaart openen.  
2. Als het veld **Toegewezen gebruikers-id** leeg is, voert u uw id in om uzelf te identificeren indien nodig.  
3. Pick de artikelen.  

    Als het magazijn opslaglocaties gebruikt, worden de standaard opslaglocaties voor de artikelen voorgesteld om de artikelen uit te halen. De instructies bevatten minstens twee afzonderlijke regels voor de acties Nemen en Plaatsen.  

    Bedrijfsruimten zoals productiewerkplaatsen hebben mogelijk een standaardbak voor de componenten die ze nodig hebben. Als dit het geval is, wordt de standaardmagazijncode toegevoegd aan het magazijnpickdocument om aan te geven waar de artikelen moeten worden geplaatst. Zie voor meer informatie de knopinfo voor het veld **Code verbruikslocatie**, **Opslaglocatie Naar-assemblage** of **Naar - Opslaglocatiecode van project**.

    Indien voor het magazijn gestuurde opslag en pick is ingesteld, wordt de opslaglocatievolgorde gebruikt voor het berekenen van de beste opslaglocaties waaruit gepickt kan worden. Die opslaglocaties worden voorgesteld op de pickregels. De instructies bevatten minstens twee afzonderlijke regels voor de acties Nemen en Plaatsen.  

    * De eerste regel met **Nemen** in het veld **Actiesoort** geeft aan waar de artikelen zich in het pickgebied bevinden. Als u een groot aantal artikelen via één verzendregel verzendt, moeten de artikelen mogelijk in verschillende opslaglocaties worden gepickt en wordt er een Nemen-regel voor elke opslaglocatie weergegeven.
    * De volgende regel met **Plaatsen** in het veld **Actiesoort** geeft aan waar u de artikelen in het magazijn moet plaatsen. U kunt de zone en de opslaglocatie op deze regel niet wijzigen.

    > [!NOTE]
    > Als het nodig is de artikelen voor een regel in meerdere opslaglocaties te picken of te plaatsen, bijvoorbeeld omdat de aangewezen opslaglocatie vol is, gebruikt u de actie **Regel splitsen** op het sneltabblad **Regels**. De actie maakt een regel voor de resterende te verwerken hoeveelheid.

4. Als u de pick hebt uitgevoerd en de artikelen op de productie-, assemblage- of projectlocatie of de opslaglocatie hebt geplaatst, kiest u de actie **Pick registreren**.  

    U kunt de artikelen nu naar het betreffende gebied brengen en het gebruik of verbruik van de gepickte materialen boeken door het verbruiksdagboek, de assemblageorder of het projectdagboek te boeken. De volgende artikelen bieden meer informatie:

    * [Verbruik en output registreren voor één vrijgegeven productieorderregel](production-how-to-register-consumption-and-output.md)
    * [Artikelen samenstellen](assembly-how-to-assemble-items.md)
    * [Verbruik of gebruik voor projecten registreren](projects-how-record-job-usage.md)

## Materialen afboeken voor productie in een geavanceerde magazijnconfiguratie

Afboekingsmethoden hebben invloed op de stroom van materialen in productie. Zie voor meer informatie [Materialen afboeken op basis van de output van een bewerking](production-how-to-flush-components-according-to-operation-output.md). Afhankelijk van de geselecteerde afboekingsmethode kunt u op de volgende manieren materialen picken voor productie:

* Gebruik een **Magazijnpick**-document om de pick vast te leggen voor artikelen die de afboekingsmethode **Handmatig** gebruiken. U dient het verbruik apart te registreren. Zie voor meer informatie [Productieverbruik in batches boeken](production-how-to-post-consumption.md).
* Gebruik een **Magazijnpick**-document om de pick vast te leggen voor artikelen die de afboekingsmethode **Picken + voorwaarts**, **Picken + achterwaarts** gebruiken. Het verbruik van de materialen gebeurt automatisch wanneer u de status van de productieorder wijzigt of door een bewerking te starten of te beëindigen. Alle vereiste materialen moeten beschikbaar zijn. Anders wordt afgeboekte verbruiksboeking voor dat materiaal gestopt.
* Gebruik een **Magazijnverplaatsing**-document zonder een verwijzing naar een brondocument of andere manieren om de verplaatsing vast te leggen van materialen die gebruikmaken van de afboekingsmethode **Voorwaarts** of **Achterwaarts**. Het verbruik van de materialen gebeurt automatisch wanneer u de status van de productieorder wijzigt of een bewerking start of beëindigt. Alle vereiste materialen moeten beschikbaar zijn. Anders wordt het boeken van afgeboekte verbruiksboeking voor dat materiaal gestopt. Zie voor meer informatie [Artikelen verplaatsten](warehouse-move-items.md).

### Voorbeeld

U hebt een productieorder voor 15 STUKS van artikel SP-SCM1004. Sommige artikelen op de materialenlijst moeten handmatig worden afgeboekt in een verbruiksdagboek. Andere artikelen kunnen automatisch worden gepickt en afgeboekt met behulp van de afboekingsmethode **Picken + Achterwaarts**.  

In de volgende stappen worden de acties beschreven die verschillende gebruikers uitvoeren en de gerelateerde reactie:  

1. De winkelsupervisor geeft de productieorder vrij. Artikelen met de afboekingsmethode **Voorwaarts** zonder routeringskoppeling worden afgetrokken van de grijpvoorraadlocatie.  
2. De winkelsupervisor kiest de actie **Magazijnpick maken** op de productieorder. Er wordt een magazijnpickdocument gemaakt voor artikelen met de afboekingsmethoden **Handmatig**, **Pick + Achterwaarts** en **Pick + Voorwaarts**. Deze artikelen worden in de verbruikslocatie geplaatst.  
3. De magazijnmanager wijst de picks toe aan een magazijnmedewerker.  
4. De magazijnmedewerker pickt de artikelen uit de desbetreffende opslaglocaties en plaatst ze in de verbruikslocatie of in de opslaglocatie die is opgegeven in de magazijnpick. De opslaglocatie kan de opslaglocatie van een afdeling of bewerkingsplaats zijn.
5. De magazijnmedewerker registreert de pick. Het aantal wordt overgebracht van de opslaglocatie naar de verbruiksopslaglocatie. Het veld **Gepickt aantal** op de onderdelenlijst voor alle gepickte artikelen wordt bijgewerkt.

    > [!NOTE]  
    >  Alleen het gepickte aantal kan worden verbruikt.  
6. De machineoperator informeert de productieplanner dat de eindproducten gereed zijn.
7. De winkelsupervisor gebruikt het verbruiksdagboek of productiedagboek om het verbruik van materialen te boeken die de afboekingsmethode **Handmatig** gebruiken.
8. De winkelsupervisor gebruikt het outputdagboek of productiedagboek om de output te boeken. Het aantal materialen dat de afboekingsmethode **Picken + Voorwaarts** of **Picken + Achterwaarts** met routeringskoppelingen gebruikt, wordt afgetrokken van de Verbruikslocatie.
9. De productieplanner wijzigt de status van de productieorder in **Gereedgemeld**. Het aantal materialen dat gebruikmaakt van de afboekingsmethode **Achterwaarts**, wordt afgetrokken van de grijpvoorraadlocatie en het aantal materialen dat gebruikmaakt van de afboekingsmethode **Picken + Achterwaarts** zonder routeringskoppeling wordt afgetrokken van de verbruikslocatie.  

De volgende illustratie geeft aan wanneer het veld **Opslaglocatie** in de materialenlijst wordt gevuld volgens de instelling van uw vestiging of bewerkingsplaats/afdeling.  

:::image type="content" source="media/binflow.png" alt-text="Overzicht van wanneer en hoe het veld Opslaglocatie wordt ingevuld.":::

## Zie ook

[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Assemblage](assembly-assemble-items.md)  
[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
