---
title: Picken van artikelen voor magazijnverzending
description: Ontdek hoe u magazijnpickdocumenten kunt gebruiken om pickinformatie te maken en te verwerken voordat u een magazijnverzending boekt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 09/11/2023
ms.custom: bap-template
ms.search.forms: '7335, 7339, 7345,'
---
# <a name="pick-items-for-warehouse-shipment"></a>Picken van artikelen voor magazijnverzending

In [!INCLUDE[prod_short](includes/prod_short.md)] gebeurt het ontvangen en opslaan op een van de volgende vier manieren, zoals beschreven in de volgende tabel.

|Methode|Uitgaand proces|Pick vereist|Verzending vereist|Complexiteitsniveau (meer informatie op [Overzicht van magazijnbeheer](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Picken en verzending vanaf de orderregel boeken|||Geen specifieke magazijnactiviteit.|  
|B|Picken en verzending vanuit een voorraadpickdocument boeken|Ingeschakeld||Basis: Order voor order|  
|H|Picken en verzending vanuit een magazijnverzendingdocument boeken||Ingeschakeld|Basis: Geconsolideerde boeking voor ontvangen/verzenden voor meerdere orders.|  
|D|Picken vanuit een magazijnpickdocument boeken en verzending vanuit een magazijnverzendingdocument boeken|Ingeschakeld|Ingeschakeld|Geavanceerd|  

Zie voor meer informatie [Uitgaande magazijnstroom](design-details-outbound-warehouse-flow.md).

Dit artikel verwijst naar methode D in de tabel. Zie voor meer informatie over het verzenden van artikelen [Artikelen verzenden](warehouse-how-ship-items.md).

Als voor een vestiging zowel magazijnpickverwerking als magazijnverzendingsverwerking is vereist, gebruikt u magazijnpickdocumenten om de pickinformatie te beheren voordat u de magazijnverzending boekt.  

Vervolgens kunt u een compleet nieuw magazijnpickdocument maken. Picks maken deel uit van een werkstroom waarbij de persoon die een order verwerkt ze op een push-manier maakt, of de magazijnmedewerker maakt ze op een pull-manier:

- Op een push-manier, waarbij u de actie **Pick maken** gebruikt op de pagina **Magazijnverzending**. Selecteer de te picken regels en bereidt de picks voor door bijvoorbeeld op te geven uit welke opslaglocaties moet worden gepickt en in welke moet worden opgeslagen en hoeveel eenheden moeten worden verwerkt. Opslaglocaties kunnen vooraf worden gedefinieerd voor de magazijnlocatie of resource.
- Op een pull-manier, waarbij u de actie **Vrijgeven** op de pagina **Magazijnverzending** gebruikt om de artikelen beschikbaar te maken voor picking. Daarna kunnen magazijnmedewerkers op de pagina **Pickvoorstel** de actie **Magazijndocumenten ophalen** om hun toegewezen picks te krijgen.

> [!NOTE]  
> Het picken voor magazijnverzending van artikelen die worden samengesteld voor een verkooporder volgt dezelfde stappen als gewone magazijnpicks voor verzending, zoals beschreven in dit artikel. Het aantal pickregels voor het te verzenden aantal is mogelijk echter veel-op-één omdat u de materialen pickt, niet het geassembleerde artikel.  
>
> Magazijnpickregels worden gemaakt voor de waarde in het veld **Resterend aantal** op de regels van de assemblageorder die is gekoppeld aan de verkooporderregel die wordt verzonden. Alle onderdelen worden in één actie gepickt. Zie voor meer informatie [Op-order-assembleren-artikelen in magazijnverzendingen afhandelen](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).  
>  
> Zie [Picken voor productie, assemblage of projecten in geavanceerde magazijnconfiguraties](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md) voor meer informatie over het picken van materialen voor assemblageorders, met inbegrip van situaties waar de assemblage niet voor een verkoopverzending is.  

## <a name="check-whether-items-are-available-for-picking"></a>Controleer of artikelen beschikbaar zijn om te picken

[!INCLUDE [inventory-availability-overview](includes/inventory-availability-overview.md)]

## <a name="to-create-pick-documents-in-bulk-with-the-pick-worksheet"></a>Bulksgewijs pickdocumenten maken met het pickvoorstel

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Pickvoorstel** in en kies vervolgens de gerelateerde koppeling.  

2. Kies de actie **Magazijndocumenten ophalen**.  

    De lijst bevat alle zendingen die zijn vrijgegeven voor picken, inclusief de zendingen waarvoor al pickinstructies zijn gemaakt. De lijst bevat geen documenten met pickregels die volledig zijn gepickt en geregistreerd.  
3. Selecteer de verzendingen waarvoor u een pick wilt voorbereiden.

    > [!NOTE]  
    >  Als u een verzendingsdocument of interne-pickdocument selecteert waarvoor u al instructies hebt gemaakt voor alle regels, krijgt u een bericht dat meldt dat er 'niets is om af te handelen.' Als de pickinstructies voor het magazijn al zijn gemaakt maar u ze wilt combineren tot één efficiënte pickinstructie, moet u eerst de afzonderlijke magazijnpicks verwijderen.

4. Vul het veld **Sorteermethode** in om de regels te sorteren.  

    > [!NOTE]  
    >  De manier waarop de regels in het werkblad worden gesorteerd, wordt niet automatisch doorgevoerd in de pickinstructie. Er zijn echter dezelfde mogelijkheden voor sorteren en opslaglocatievolgorde. U kunt de volgorde van de regels die u in het voorstel plant gemakkelijk opnieuw bepalen wanneer u de pickinstructies maakt of door te sorteren in de pickinstructies.

5. Vul het veld **Te verwerken aantal** handmatig in of gebruik hiervoor de actie **Te verwerken aantal autom. invullen**.  

    De pagina toont de beschikbare hoeveelheden in cross-dockopslaglocaties. Deze informatie is handig voor het plannen van werktoewijzingen in cross-docksituaties. [!INCLUDE[prod_short](includes/prod_short.md)] stelt altijd eerst een pick uit een cross-dockopslaglocatie voor.
6. U kunt de regels zo nodig bewerken. U kunt ook regels verwijderen om de pick nog efficiënter te maken. Als er bijvoorbeeld meerdere regels zijn met artikelen in cross-dockopslaglocaties, kunt u een pick maken voor alle regels. De cross-dockartikelen worden dan verzonden, samen met de andere artikelen in de verzending, en in de cross-docklocaties komt ruimte vrij voor andere binnenkomende artikelen.  

    > [!NOTE]  
    >  Als u regels verwijdert, worden ze alleen uit het voorstel verwijderd. Ze worden niet verwijderd uit het pickselectieoverzicht.  

7. Kies de actie **Pick maken**. De pagina **Pick maken** wordt geopend, waar u meer informatie aan de pick kunt toevoegen. Geef op hoe pickregels moten worden gesorteerd in de pickdocumenten door een van de volgende opties te selecteren.  

    |Optie|Omschrijving|
    |-|-|
    |Per magazijn Document|Maakt afzonderlijke pickdocumenten voor regels van het werkblad met hetzelfde magazijn-brondocument.|
    |Per klant/leverancier/vestiging|Maak afzonderlijke pickdocumenten voor elke klant (verkooporders), leverancier (inkoopretourorders) en vestiging (transferorders).|
    |Per artikel|Maak afzonderlijke pickdocumenten voor elk artikel in het pickvoorstel.|
    |Per Van zone|Maak afzonderlijke pickdocumenten voor elke zone waar u artikelen uit haalt.|
    |Per opslaglocatie|Maak afzonderlijke pickdocumenten voor elke opslaglocatie waar u artikelen uit haalt.|
    |Per vervaldatum|Maak afzonderlijke pickdocumenten voor brondocumenten die dezelfde vervaldatum hebben.|

    Geef op hoe de pickdocumenten worden gemaakt door een selectie te maken uit de volgende opties.

    |Optie|Omschrijving|
    |-|-|
    |Max. Nee Pickregels|Maakt pickdocumenten die niet meer dan het opgegeven aantal regels in een document hebben.|
    |Max. Nee pickbrondocumenten.|Maakt pickdocumenten die ieder niet meer dan het opgegeven aantal brondocumenten hebben.|
    |Toegewezen gebruikers-id|Maakt pickdocumenten alleen voor voorstelregels die zijn toegewezen aan de geselecteerde magazijnmedewerker.|
    |Sorteringsmethode voor pickregels|Selecteer uit de beschikbare opties om regels te sorteren in het gemaakte pickdocument.|
    |Breakbulkfilter plaatsen|Verbergt tussenliggende bulksplitsing pickregels wanneer een grotere eenheid wordt omgezet in een kleinere eenheid en volledig wordt gepickt.|
    |Te verwerken aantal niet opvullen|Laat het veld Te verwerken aantal in de gemaakte pickregels leeg.|
    |Pick afdrukken|Drukt de pickdocumenten af wanneer ze worden gemaakt. U kunt ook afdrukken vanuit de gemaakte pickdocumenten.|

8. Klik op **OK**. [!INCLUDE [prod_short](includes/prod_short.md)] maakt de keuze op basis van uw selecties.  

## <a name="to-pick-items-for-a-warehouse-shipment"></a>Picken van artikelen voor een magazijnverzending

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnpicks** in en kies vervolgens de gerelateerde koppeling.  

    Als u een bepaalde pick wilt bewerken, selecteert u het pickformulier of het overzicht. U kunt het overzicht ook filteren op picks die speciaal aan u zijn toegewezen. De pickkaart openen.  
2. Als het veld **Toegewezen gebruikers-id** leeg is, voert u uw id in om uzelf te identificeren indien nodig.  
3. Pick de artikelen.  

    Als het magazijn opslaglocaties gebruikt, worden de standaard opslaglocaties voor de artikelen voorgesteld om de artikelen uit te halen. De instructies bevatten minstens twee afzonderlijke regels voor de acties Nemen en Plaatsen.  

    Indien voor het magazijn gestuurde opslag en pick is ingesteld, wordt opslaglocatievolgorde gebruikt voor het berekenen van de beste opslaglocaties waaruit gepickt kan worden. Die opslaglocaties worden voorgesteld op de pickregels. De instructies bevatten minstens twee afzonderlijke regels voor de acties Nemen en Plaatsen.  

    * De eerste regel met **Nemen** in het veld **Actiesoort** geeft aan waar de artikelen zich in het pickgebied bevinden. Als u een groot aantal artikelen via één verzendregel verzendt, moeten de artikelen mogelijk in verschillende opslaglocaties worden gepickt en wordt er een Nemen-regel voor elke opslaglocatie weergegeven.
    * De volgende regel met **Plaatsen** in het veld **Actiesoort** geeft aan waar u de artikelen in het magazijn moet plaatsen. U kunt de zone en de opslaglocatie op deze regel niet wijzigen.

    > [!NOTE]
    > Als het nodig is de artikelen voor een regel in meerdere opslaglocaties te picken of te plaatsen, bijvoorbeeld omdat de aangewezen opslaglocatie vol is, gebruikt u de actie **Regel splitsen** op het sneltabblad **Regels**. De actie maakt een regel voor de resterende te verwerken hoeveelheid.

4. Nadat u de pick hebt uitgevoerd en de artikelen op de verzendlocatie hebt geplaatst, kiest u de actie **Pick registreren**.  

U kunt nu de artikelen naar de afdeling voor verzending overbrengen en de verzending boeken, inclusief het gerelateerde brondocument, op de pagina **Mag. -verzending**. Zie voor meer informatie [Artikelen verzenden](warehouse-how-ship-items.md).

## <a name="see-also"></a>Zie ook

- [Overzicht van magazijnbeheer](design-details-warehouse-management.md)
- [Voorraad beheren](inventory-manage-inventory.md)  
- [Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
- [Assemblage](assembly-assemble-items.md)    
- [Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
