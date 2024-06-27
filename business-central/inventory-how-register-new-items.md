---
title: Artikelkaarten maken voor goederen of services
description: U maakt artikelkaarten voor services die u als uren verkoopt en voor fysieke producten. Voorbeelden zijn componenten en eindproducten die u vanuit uw voorraad verkoopt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Nieuwe artikelen registreren

Artikelen zijn de goederen of diensten die u koopt, opslaat, verkoopt, levert en waarvoor u verantwoording aflegt. Gebruik de pagina **Artikelkaart** om informatie te registreren over de volgende soorten items:

* **Voorraad** geeft aan dat het artikel een fysieke eenheid is die u beheert en bijhoudt in de voorraad.
* **Niet-voorraad** zijn fysieke eenheden die u niet beheert of bijhoudt in de inventaris.
* **Service**artikelen zijn een arbeidstijdeenheid, die doorgaans wordt gebruikt in servicemanagement.

Ga voor meer informatie over deze typen artikelen naar [Over artikeltypen](inventory-about-item-types.md).

> [!TIP]
> Er zijn ook catalogusartikelen, die vergelijkbaar zijn met artikelen die niet op voorraad zijn, omdat het artikelen zijn die u aan klanten aanbiedt, maar die u pas beheert als u ze verkoopt. Ga voor meer informatie naar [Werken met catalogusartikelen](inventory-how-work-nonstock-items.md).  

## Primaire en alternatieve leveranciers

Als u hetzelfde artikel inkoopt bij meerdere leveranciers, kunt u die leveranciers aan de artikelkaart koppelen. Gebruik de actie **Leveranc.** op de pagina **Artikelkaart** om de pagina **Artikel-/leverancierscatalogus** te openen. Op de pagina worden de leveranciers weergegeven waarbij u het artikel koopt, zodat u eenvoudig een alternatieve leverancier kunt maken of selecteren wanneer u een inkooporder maakt.

## Artikelsjablonen gebruiken

Als u de instellingen voor verschillende soorten artikelen opnieuw wilt gebruiken wanneer u nieuwe artikelen maakt, kunt u artikelen opslaan als artikelsjablonen. Artikelsjablonen helpen het proces van het toevoegen van nieuwe artikelen te versnellen en de consistentie in uw artikelgegevens te vergroten. Wanneer u een nieuw artikel registreert, verschijnt er een pagina waarop u een sjabloon kunt kiezen. Nadat u een sjabloon heeft gekozen, worden de instellingen ervan voor u ingevuld op het artikel dat u maakt. Als u slechts één artikelsjabloon hebt, gebruiken nieuwe artikelen altijd deze sjabloon. Ga naar voor meer informatie over het instellen van een artikelsjabloon naar [Een artikelkaart opslaan als artikelsjabloon](#save-an-item-card-as-an-item-template).

## Artikelen opnemen in stuklijsten

U kunt hiërarchieën structureren die een hoofdartikel hebben met onderliggende componentartikelen in assemblage- en productiestuklijsten (BOM). Ga voor meer informatie over stuklijsten naar [Werken met stuklijsten](inventory-how-work-BOMs.md).

## Een nieuwe artikelkaart maken

De volgende video toont hoe u een artikel instelt op de pagina Artikelkaart. U kunt echter ook nieuwe artikelen maken door bestaande te kopiëren. Ga voor meer informatie naar [Bestaande artikelen kopiëren om nieuwe artikelen te maken](inventory-how-copy-items.md).  

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

[!INCLUDE[create_new_item](includes/create_new_item.md)]

> [!NOTE]
> In het veld **Waarderingsmethode** bepaalt u hoe de eenheidskostprijs van het artikel wordt berekend door de veronderstellingen die worden gemaakt over de stroom van artikelen in het bedrijf. Afhankelijk van het type item zijn vijf waarderingsmethoden beschikbaar. Ga voor meer informatie over kosten naar [Ontwerpdetails: kostenberekeningsmethoden](design-details-costing-methods.md).
>
> Als u **Gemiddeld** selecteert, worden de eenheidskosten van een artikel berekend als de gemiddelde eenheidskosten op een bepaald moment na een aanschaf. Voorraad wordt gewaardeerd met de aanname dat alle voorraad tegelijkertijd wordt verkocht. Met deze instelling kunt u het veld **Kostprijs** kiezen en zo op de pagina **Overzicht gemiddelde-kostenberekening** de transacties bekijken die zijn gebruikt om de gemiddelde kostprijs te berekenen.

U kunt speciale prijzen of kortingen gebruiken die u of uw leverancier voor het artikel toekent op basis van bepaalde criteria. Criteria zijn bijvoorbeeld de klant, de minimale bestelhoeveelheid of de einddatum. U stelt speciale prijzen in door de actie **Speciale prijzen instellen** of **Speciale kortingen instellen** te kiezen. Elke rij op de pagina **Verkoopprijzen** vertegenwoordigt bijvoorbeeld een speciale prijs. Elke kolom vertegenwoordigt een criterium dat moet gelden om een klant de speciale prijs te geven die u invoert in het veld **Eenheidsprijs** op de pagina **Verkoopprijzen**. Zie voor meer informatie over prijzen [Afspraken over prijzen, kortingen en betalingen van verkopen vastleggen](sales-how-record-sales-price-discount-payment-agreements.md) of [Speciale inkoopprijzen en kortingen registreren](purchasing-how-record-purchase-price-discount-payment-agreements.md).

### Een artikelkaart als artikelsjabloon opslaan

1. Kies op de pagina **Artikelkaart** de actie **Opslaan als sjabloon**. De pagina **Artikelsjabloon** toont de artikelkaart als sjabloon.
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> U kunt dimensies voor artikelen ook hergebruiken. Als u sjablonen wilt hergebruiken, kiest u de actie **Dimensies**. De pagina **Dimensiesjablonen** geeft alle dimensiecodes weer die voor het artikel zijn ingesteld. Bewerk of voeg dimensies toe die van toepassing zijn op nieuwe artikelen die u op basis van de sjabloon maakt.

De artikelsjabloon wordt toegevoegd aan de lijst met artikelsjablonen, zodat u deze kunt gebruiken om nieuwe artikelkaarten te maken.

### Artikelen gebruikt in productieorders

Als u artikelen wilt registreren die in productieorders worden gebruikt, geeft u het aanvulsysteem op als *Prod.-order* op het sneltabblad **Aanvulling**. Zie voor meer informatie [Over productieorders](production-about-production-orders.md).  

## Meerdere leveranciers voor een artikel instellen

Als u hetzelfde artikel bij meerdere leveranciers inkoopt, moet u informatie over elk van deze leveranciers invoeren, bijvoorbeeld informatie over prijzen, levertermijn, kortingen, enzovoort.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer het betreffende artikel en kies vervolgens de actie **Bewerken**.  
3. Kies de actie **Leveranciers**.  
4. Klik op het veld **Leveranciersnr.** en selecteer vervolgens de leverancier waarvoor u het artikel wilt instellen.  
5. Het invullen van de overige velden is optioneel.  
6. Herhaal stap 2 t/m 5 voor elke leverancier waarbij u het artikel wilt kunnen inkopen.

Deze leveranciers worden vervolgens weergegeven op de pagina **Artikelleveranciers**, die u opent vanuit de artikelkaart, zodat u gemakkelijk een alternatieve leverancier kunt selecteren.

## Artikelvervangingen instellen

U kunt artikelen instellen om vervangingen te hebben, zoals andere artikelen die kunnen worden gebruikt in plaats van het oorspronkelijke artikel.

### Een artikelvervanging maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.  
2. Zoek het relevante artikel en kies vervolgens **Artikelnr.** om de artikelkaart te openen.  
3. Kies de actie **Verwant**, kies dan **Artikel** en vervolgens **Vervangingen** om de pagina **Artikelvervangingspost** te openen.  
4. Kies het veld **Vervangingsartikelnr.** en selecteer vervolgens het vervangingsartikel uit de lijst.
5. Vul indien nodig andere velden op de pagina in of wijzig deze.

Wanneer het gevraagde aantal artikelen de hoeveelheid die in voorraad beschikbaar is overschrijdt, wordt een bericht weergegeven dat er vervangende artikelen bestaan.

> [!NOTE]  
> Houd er rekening mee dat artikelvervangingen er niet automatisch toe leiden dat een artikel wordt vervangen door een ander artikel, bijvoorbeeld bij het maken van een verkooporder of in een stuklijst. In plaats daarvan wordt u erop gewezen dat er een vervanging voor u beschikbaar is.

## Categorieën, kenmerken en varianten

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

Zie [Productvarianten beheren](inventory-item-variants.md) voor meer informatie over varianten.  

## Artikelkaarten verwijderen

Als u een transactie voor een artikel boekt, kunt u de kaart niet verwijderen omdat de grootboekposten mogelijk nodig zijn voor voorraadwaardering of controle. Als u artikelkaarten met grootboekposten wilt verwijderen, neemt u contact op met de Microsoft-partner om dat via code te doen.  

## Voorraad beheren in magazijnen

Wanneer u een nieuw artikel registreert, ziet u velden die betrekking hebben op magazijnbeheer, met name op het sneltabblad **Magazijn**. Als uw organisatie geen gebruik maakt van de magazijnbeheermogelijkheden in [!INCLUDE [prod_short](includes/prod_short.md)], kunt u die velden negeren.  

Als uw organisatie later magazijnbeheer instelt, raden we u aan ervoor te zorgen dat elk bestaand artikel de juiste informatie in de verschillende velden bevat. Op deze manier kunnen de magazijnprocessen verlopen zoals verwacht. De informatie kan velden bevatten zoals **Magazijnklassecode** of **Opslagsjabloon**. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).  

## Planning

Wanneer uw bedrijf de leveringsplanningsprocessen gebruikt in [!INCLUDE [prod_short](includes/prod_short.md)], moet u de relevante velden invullen op het sneltabblad **Planning**. Voor een inleiding tot het planningsgebied zie [Ontwerpdetails: centrale concepten van het planningssysteem](design-details-central-concepts-of-the-planning-system.md).  

Voor voorbeelden van hoe u de velden op het sneltabblad **Planning** gebruikt zie [Best practices instellen: planningsparameters](setup-best-practices-planning-parameters.md).  

## Zie ook

[Voorraad](inventory-manage-inventory.md)  
[Maateenheden instellen](inventory-how-setup-units-of-measure.md)  
[Productvarianten beheren](inventory-item-variants.md)  
[Intrastat-rapportage instellen](finance-how-setup-report-intrastat.md#other-intrastat-configurations)  
[Voorraadkosten reconciliëren met het grootboek](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Nummerreeksen maken](ui-create-number-series.md)  
[Boekingsgroepen instellen](finance-posting-groups.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Informatie over het plannen van functionaliteit](production-about-planning-functionality.md)  
[Aanbevolen procedures instellen: Planningparameters](setup-best-practices-planning-parameters.md)  
[Aanbevolen procedures instellen: voorraadplanning](setup-best-practices-supply-planning.md)  
[Ontwerpdetails: Centrale begrippen van het planningssysteem](design-details-central-concepts-of-the-planning-system.md)  
[Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md)  
[Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
