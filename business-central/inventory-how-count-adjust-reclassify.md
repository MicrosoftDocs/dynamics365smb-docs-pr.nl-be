---
title: 'Voorraad tellen, aanpassen en herindelen'
description: Leer hoe u fysiek kunt tellen en aanpassingen en herindelingen kunt maken.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 05/24/2024
ms.custom: bap-template
---
# <a name="count-adjust-and-reclassify-inventory-using-journals"></a>Voorraad tellen, corrigeren en herindelen met dagboeken

Tel fysiek alle artikelen in uw voorraad om ervoor te zorgen dat uw hoeveelheden correct zijn. Sommige bedrijven doen een jaarlijkse fysieke telling, en andere tellen vaker alle of slechts enkele items. Nadat u artikelen hebt geteld, gebruikt u dagboeken om de werkelijke hoeveelheden naar het grootboek te boeken. Bijvoorbeeld wanneer u de voorraad aan het einde van een periode waardeert.

Gebruik cyclustellingen om sommige items vaker te tellen dan andere, misschien vanwege hun waarde. Voor cyclustellingen wijst u speciale telperioden aan de artikelen toe. Lees meer op [Cyclustelling uitvoeren](inventory-how-count-adjust-reclassify.md#to-do-cycle-counting).

Om hoeveelheden aan te passen na een fysieke telling of andere doeleinden, gebruikt u een artikeldagboek om de inventarisatieposten te wijzigen zonder transacties te boeken. U kunt de hoeveelheid ook aanpassen voor één artikel op een artikelkaart.

Als u kenmerken van artikelposten wilt wijzigen, gebruikt u een artikelherindelingsdagboek. Typische kenmerken voor herindelen zijn onder meer dimensies en verkoopcampagnecodes. Herindelingsdagboeken kunnen ook worden gebruikt voor overboekingen door opslaglocatie- en vestigingscodes te herindelen. Speciale stappen zijn van toepassing wanneer u serie- of lotnummers en hun vervaldatums wilt herindelen. Zie voor meer informatie [Werken met serie- en lotnummers](inventory-how-work-item-tracking.md).

> [!NOTE]
> In processen met meerdere stappen worden artikelen in opslaglocaties geregistreerd als magazijnposten, niet als artikelposten. Daarom voert u tellingen, aanpassingen en herindelingen uit in magazijndagboeken die opslaglocaties ondersteunen. Vervolgens synchroniseert u de nieuwe of gewijzigde magazijnposten met de gerelateerde artikelposten om de wijzigingen in voorraadaantallen en waarden weer te geven.

[!INCLUDE [edit-in-excel](includes/edit-in-excel.md)]

## <a name="to-count-physical-inventory"></a>Fysieke voorraad tellen

Als u wilt controleren of de geregistreerde hoeveelheid hetzelfde is als de fysieke hoeveelheid in voorraad, telt u uw fysieke voorraad. Dat wil zeggen, tel de daadwerkelijke artikelen die beschikbaar zijn. Doorgaans vinden tellingen plaats aan het einde van een boekjaar, maar sommige bedrijven tellen artikelen vaker. Als er verschillen zijn, boekt u de werkelijke hoeveelheden naar de artikelrekeningen voordat u de voorraadwaardering uitvoert.

> [!NOTE]
> In deze procedure wordt beschreven hoe u een inventarisatie uitvoert met een dagboek op de pagina **Inventarisatiedagboek**. U kunt documenten gebruiken op de pagina's **Inventarisatieorder** en **Inventarisatieregistratie**. Deze documenten bieden meer controle en ondersteuning bij het verdelen van het telwerk over meerdere medewerkers. Meer informatie op [Voorraad tellen met documenten](inventory-how-count-inventory-with-documents.md).<br /><br />
> De op documenten gebaseerde functionaliteit kan niet worden gebruikt om artikelen te tellen in opslaglocaties of magazijnposten.

Het telproces omvat ook de volgende taken:

- De verwachte voorraad berekenen.
- Druk het rapport af dat u voor de telling wilt gebruiken.
- Invoeren en boeken van de werkelijke hoeveelheden.

Afhankelijk van de magazijninstellingen kunt u de inventarisatie op een van de volgende manieren uitvoeren. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).  

- Als uw vestiging geen gestuurde opslag en pick gebruikt, gebruikt u de pagina **Inventarisatiedagboek**. De procedure is vergelijkbaar met fysieke inventarisatie zonder cyclustelling.  
- Als uw vestiging wel gestuurde opslag en pick gebruikt, gebruikt u de pagina **Magazijninventarisatiedagboek**. Gebruik vervolgens de pagina **Artikeldagboeken** om de actie **Magazijnherwaardering berekenen** uit te voeren. <!--We should say what to do on each of these pages.-->

### <a name="to-calculate-expected-inventory-in-basic-warehouse-configurations"></a>Verwachte voorraad in standaardmagazijnconfiguraties berekenen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), pictogram, voer **Inventarisatiedagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie  **Inventaris berekenen** uit  **Voorbereiden**.
3. Specificeer op de pagina **Voorraad berekenen** de voorwaarden die moeten worden gebruikt om de dagboekregels te maken, zoals of artikelen die niet op voorraad zijn al dan niet moeten worden opgenomen.
4. Stel alleen filters in als u de voorraad voor bepaalde artikelen, opslaglocaties, vestigingen of dimensies wilt berekenen.
5. Kies de knop **Ok**.

> [!NOTE]  
> Artikelposten worden verwerkt volgens de informatie die u hebt opgegeven en de regels in het inventarisatiedagboek worden gemaakt. U ziet dat het veld **Aantal (inventaris)** hetzelfde aantal heeft als het veld **Aantal (Berekend)**. U hoeft het getelde aantal niet in te voeren voor artikelen waar deze waarden overeenkomen. Als de getelde hoeveelheid echter afwijkt, voer dan de getelde hoeveelheid in.

### <a name="to-print-the-report-to-be-used-when-counting"></a>Het rapport afdrukken dat bij het tellen moet worden gebruikt

1. Kies op de pagina **Fysieke inventarislogboeken**  met de berekende verwachte inventaris de actie **Afdrukken** in **Start**.
2. Geef op de pagina **Fysieke inventarislijst**  aan of het rapport de berekende hoeveelheid en inventarisartikelen op serie- en lotnummers moet weergeven.
3. Stel filters in als u het rapport alleen wilt afdrukken voor bepaalde artikelen, opslaglocaties, vestigingen of dimensies.
4. Kies **Afdrukken**.

Magazijnmedewerkers kunnen nu de voorraad tellen en eventuele afwijkingen in het afgedrukte rapport vastleggen.

> [!NOTE]
> Het kan enkele dagen duren voordat afgedrukte rapporten terugkomen voor definitieve verwerking en boeking. Wanneer u de werkelijk getelde voorraad opgeeft en boekt, past het systeem de voorraad aan om het verschil weer te geven tussen de verwachte en de werkelijk getelde voorraad. U moet de oorspronkelijk berekende journaalregels behouden en de verwachte voorraad niet herberekenen, omdat de verwachte voorraad kan veranderen en tot onjuiste voorraadniveaus kan leiden. Als u meerdere rapporten moet uitgeven, bijvoorbeeld voor verschillende locaties of een groep items, moet u afzonderlijke dagboekbatches maken en bewaren.

### <a name="to-enter-and-post-the-actual-counted-inventory-in-basic-warehouse-configurations"></a>De werkelijk getelde voorraad in standaardmagazijnconfiguraties invoeren en boeken

1. Voer op elke regel op de pagina **Fysieke inventarisjournalen** waar de werkelijke voorraad, zoals bepaald door de fysieke telling, afwijkt van de berekende hoeveelheid, de werkelijke voorraad in het veld **Aantal (fysieke inventaris)** in.
  
  > [!NOTE]  
  > Als de verschillen in de telling worden veroorzaakt door artikelen die met onjuiste vestigingen zijn geboekt, moet u de verschillen niet invoeren in het inventarisatiedagboek. Gebruik in plaats daarvan een herindelingsdagboek of een transferorder om items om te leiden naar de juiste vestigingen. 

2. Om de berekende hoeveelheden om te zetten in de daadwerkelijk getelde hoeveelheden, kiest u de actie  **Post** in  **Home**.

    Bij boeken worden artikelposten en inventarisatieposten gemaakt. Open de pagina Artikelkaart voor het artikel om de inventarisatieposten te bekijken.

3. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
4. Om de telling te verifiëren, opent u de pagina **Artikel kaart** voor het artikel en kiest u de actie **Phys. Inventory Ledger Posten** van **Artikel**
1. .

### <a name="to-calculate-the-expected-inventory-in-advanced-warehouse-configurations"></a>De verwachte voorraad in geavanceerde magazijnconfiguraties berekenen

Synchroniseer artikelboek en magazijn <!--warehouse what?--> voordat u de fysieke voorraad telt. Anders boekt u naar het inventarisatiedagboek en het artikelgrootboek de inventarisatieresultaten in combinatie met andere magazijncorrecties voor de artikelen. Zie voor meer informatie [Hoeveelheden synchroniseren in het artikelboek en magazijn](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") pictogram, voer **Magazijninventarisatiedagboek** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Voorraad berekenen** om de pagina **Magazijn - Voorraad berekenen** te openen.  
3. Stel de gewenste filters in om het aantal artikelen dat wordt geteld in het dagboek op te geven en klik vervolgens op **OK**.

   [!INCLUDE [prod_short](includes/prod_short.md)] maakt een regel voor elke opslaglocatie die voldoet aan de filtercriteria. U kunt regels verwijderen, maar als u het resultaat wilt boeken als inventarisatie, moet u alle opslaglocaties opnemen in de artikeltelling.  

   Als u alleen een artikel in sommige opslaglocaties telt maar niet in andere, kunt u verschillen invoeren en deze later op de pagina **Artikeldagboek** boeken met de actie **Magazijnherwaardering berekenen**.  

### <a name="to-enter-and-post-the-actual-counted-inventory-in-advanced-warehouse-configurations"></a>De werkelijk getelde voorraad in geavanceerde magazijnconfiguraties invoeren en boeken

1. Voer op de pagina **Magazijninventarisatiedagboek** de werkelijke hoeveelheden in het veld **Aantal (inventaris)** in.  

    > [!NOTE]  
    > Het veld **Aantal (berekend)** wordt ingevuld op basis van opslaglocatierecords. Dit aantal wordt gekopieerd naar het veld **Aantal (Fysiek)** op elke regel. Als de hoeveelheden in deze velden niet overeenkomen, vul dan de werkelijke hoeveelheid in.  

2. Wanneer u alle werkelijke aantallen hebt ingevoerd, kiest u de actie **Registreren**.  

    Wanneer u het dagboek registreert, maakt [!INCLUDE [prod_short](includes/prod_short.md)] twee magazijnposten in het magazijnregister voor elke getelde en geregistreerde regel:  

    - Als de berekende aantallen niet overeenkomen met de werkelijke aantallen, wordt een negatief of positief aantal geregistreerd voor de opslaglocatie. Vervolgens wordt een tegengesteld aantal geboekt naar de correctieopslaglocatie van de vestiging.  
    - Als het berekende aantal wel overeenkomt met het getelde aantal, registreert [!INCLUDE [prod_short](includes/prod_short.md)] **0** voor zowel de opslaglocatie als de correctieopslaglocatie. 

Wanneer u inventarisatie registreert, boekt u niet naar het artikel, de inventarisatie of de waardeboeken. De records zijn echter beschikbaar voor reconciliatie wanneer dat nodig is. Om de hoeveelheden nauwkeurig te houden, boekt u, nadat u de artikelen in alle opslaglocaties hebt geteld, de resultaten.<!--physical inventory journal--> Zie voor meer informatie [Hoeveelheden synchroniseren in het artikelboek en magazijn](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

## <a name="to-do-cycle-counting"></a>Cyclustelling uitvoeren

U kunt artikelen zo vaak tellen als u wilt. Bijvoorbeeld omdat ze waardevoller zijn of topverkopers. Geef de telfrequentie op door speciale telperioden aan de artikelen toe te wijzen.

Afhankelijk van de magazijninstellingen kunt u cyclustelling op een van de volgende manieren uitvoeren. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).  

- Als uw vestiging geen gestuurde opslag en picks gebruikt, gebruikt u de pagina **Inventarisatiedagboek**. De stappen zijn vergelijkbaar met fysieke inventarisatie zonder cyclustelling.  
- Als uw vestiging wel gestuurde opslag en pick gebruikt, gebruikt u de pagina **Magazijninventarisatiedagboek**. Gebruik vervolgens de pagina **Artikeldagboeken** om de actie **Magazijnherwaardering berekenen** uit te voeren. <!--we should say what to do on each of these pages-->  

### <a name="to-set-up-counting-periods"></a>U kunt als volgt tellingsperioden instellen

Een inventarisatie wordt gewoonlijk periodiek uitgevoerd, bijvoorbeeld maandelijks, per kwartaal of jaarlijks. U kunt de inventarisatieperioden instellen die u wilt gebruiken en wijst er vervolgens één toe aan elk artikel. Gebruik daarna de actie **Tellingsperiode berekenen** op de pagina **Inventarisatiedagboek** om automatisch regels voor de artikelen te maken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") pictogram, voer **Voorraadtellingsperioden** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-assign-a-counting-period-to-an-item"></a>Een tellingsperiode toewijzen aan een artikel

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer het artikel waaraan u een tellingsperiode wilt toewijzen.  
3. Selecteer in het veld **Code van inventarisatieperiode** de gewenste tellingsperiode.  

> [!NOTE]
> Als u de telperiode wijzigt, wordt er een bericht weergegeven met informatie over de resultaten van de wijziging. Kies **Ja** om de code te wijzigen en de eerste tellingsperiode voor het artikel te berekenen. De volgende keer dat u een tellingsperiode in het magazijninventarisatiedagboek berekent, wordt het item als een regel op de pagina **Inventarisatieartikelselectie** weergegeven. U kunt het artikel dan periodiek tellen.

### <a name="to-start-a-count-based-on-counting-periods-in-basic-warehouse-configurations"></a>Een telling starten op basis van tellingsperioden in standaardmagazijnconfiguraties

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") pictogram, voer **Inventarisatiedagboek** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Tellingsperiode berekenen**.

    De pagina **Inventarisatieartikelselectie** toont artikelen die moeten worden geteld op basis van hun tellingsperioden.
3. Tel de fysieke voorraad. Meer informatie op [Fysieke voorraad tellen](inventory-how-count-adjust-reclassify.md#to-count-physical-inventory).

### <a name="to-start-a-count-based-on-counting-periods-in-advanced-warehouse-configurations"></a>Een telling starten op basis van tellingsperioden in geavanceerde magazijnconfiguraties

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") pictogram, voer **Magazijninventarisatiedagboek** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Tellingsperiode berekenen**.

    De pagina **Inventarisatieartikelselectie** toont artikelen die moeten worden geteld op basis van hun tellingsperioden.
3. Tel de fysieke voorraad. Meer informatie op [Fysieke voorraad tellen](inventory-how-count-adjust-reclassify.md#to-count-physical-inventory).  

   > [!NOTE]  
   > Tel het artikel in alle opslaglocaties die het bevatten. Als u opslaglocatieregels verwijdert die zijn opgehaald voor telling op de pagina **Magazijninventarisatie**, is de telling onjuist wanneer u deze boekt in het fysieke voorraadjournaal.  

## <a name="to-adjust-the-quantity-of-one-item"></a>De hoeveelheid van één artikel aanpassen

Nadat u een fysieke telling van een artikel hebt uitgevoerd, gebruikt u de actie **Voorraad corrigeren** om het werkelijke voorraadaantal vast te leggen.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het artikel waarvoor u voorraad wilt aanpassen, en kies vervolgens de actie **Voorraad wijzigen**.
3. Voer in het veld **Nieuwe voorraad** voor de vestiging het resultaat van de telling in.
4. Kies de knop **Ok**.

<!-- I don't see a "Quantity on Hand" field on the Item Card page. Should this point to the options for viewing availability?

The item’s inventory is adjusted. The new quantity is shown in the **Quantity on Hand** field on the **Item Card** page.-->

U kunt ook de actie **Voorraad corrigeren** gebruiken als eenvoudige manier om gekochte artikelen aan voorraad toe te voegen als u geen inkoopfacturen of orders gebruikt om uw inkopen te registreren. Meer informatie op [Inkopen vastleggen](purchasing-how-record-purchases.md).

> [!NOTE]  
> Nadat u de voorraad hebt gecorrigeerd, werkt u de huidige waarde bij. Zie [Voorraad herwaarderen](inventory-how-revalue-inventory.md) voor meer informatie.

### <a name="to-adjust-the-quantities-of-multiple-items-in-basic-warehouse-configurations"></a>De hoeveelheden van meerdere artikelen in standaardmagazijnconfiguraties corrigeren

Op de pagina  **Artikeldagboeken** kunt u artikeltransacties rechtstreeks naar de voorraad Aanpassen boeken voor aankopen, verkopen en positieve of negatieve wijzigingen, zonder dat u documenten hoeft te gebruiken.

Als u het artikeldagboek vaak gebruikt om dezelfde of vergelijkbare dagboekregels te boeken, bijvoorbeeld voor materiaalverbruik, kunt u de pagina **Standaardartikeldagboek** gebruiken om deze terugkerende taak gemakkelijker te maken. Zie [Werken met standaarddagboeken](ui-work-general-journals.md#work-with-standard-journals) voor meer informatie.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikeldagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Kies de actie **Boeken** om de hoeveelheden te corrigeren.

### <a name="to-adjust-bin-quantities-in-advanced-warehouse-configurations"></a>Opslaglocatieaantallen in geavanceerde magazijnconfiguraties aanpassen

Als uw vestiging gestuurde opslag en picks gebruikt, gebruikt u de pagina **Magazijnartikeldagboek** om ongeplande positieve en negatieve hoeveelheidswijzigingen te boeken. Bijvoorbeeld voor artikelen die als vermist zijn opgegeven en onverwachts verschijnen, of voor verliezen als gevolg van breuk.  

Magazijnartikeldagboeken bieden u meer aanpassingsniveaus om uw hoeveelheden nauwkeuriger te maken. Het magazijn weet hoeveel artikelen er voorhanden zijn en waar ze zijn opgeslagen, maar elke aanpassing wordt niet in het artikelboek geboekt. Bijschrijvingen of afschrijvingen worden gedaan naar de echte opslaglocatie met de hoeveelheidsaanpassing. Er wordt een tegenboeking gemaakt in een correctieopslaglocatie. De correctieopslaglocatie is een virtuele opslaglocatie zonder echte artikelen. U geeft de virtuele opslaglocatie op in het veld **Opslaglocatiecode voorraadherwaardering** op **Vestigingskaart**-pagina's.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), en voer **Magazijnartikeldagboek** in. Kies vervolgens de gerelateerde koppeling.  
2. Vul de informatie op de kop in.  
3. Kies in het veld **Artikelnummer** op de regel het artikel.  
4. Voer de opslaglocatie in waar u de extra artikelen wilt opslaan of waar de artikelen verloren zijn gegaan.  
5. Als u extra artikelen aantreft, voert u een positief aantal in het veld **Aantal** in. Bij ontbrekende artikelen voert u een negatieve waarde in.  
6. Kies de actie **Registreren**.

## <a name="to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries"></a>De aangepaste magazijnposten synchroniseren met de gerelateerde artikelposten

Boek de correctieopslaglocatierecords in het artikelboek voor de gedefinieerde perioden. Sommige bedrijven boeken dagelijkse aanpassingen in het artikelboek, terwijl andere minder vaak afstemmen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikeldagboek** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de velden op de dagboekregels in.  
3. Kies de actie **Magazijnherwaardering berekenen** en voeg filters toe op de pagina **Magazijnherwaardering berekenen**. Herwaarderingen worden alleen berekend voor de posten in de correctieopslaglocatie die aan de filtervereisten voldoen.  
4. Vul op het sneltabblad **Opties** het veld **Documentnr.** in met een nummer. Het nummer wordt weergegeven op de artikeldagboekregels.
5. Klik op **OK**. De positieve en negatieve correcties worden opgeteld voor elk artikel en er worden regels gemaakt in het artikeldagboek.  
6. Boek de dagboekregels om de verschillen in aantal in te voeren op de artikelposten. De hoeveelheden in de opslaglocaties en het artikelboek komen nu overeen.  

## <a name="see-also"></a>Zie ook

[Voorraad tellen met documenten](inventory-how-count-inventory-with-documents.md)  
[Voorraad](inventory-manage-inventory.md)  
[Overzicht van magazijnbeheer](design-details-warehouse-management.md)  
[Verkoop](sales-manage-sales.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
