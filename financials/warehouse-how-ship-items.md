---
title: Artikelen verzenden | Microsoft Docs
description: "Afhankelijk van de magazijnconfiguratie, kunt u de verzending direct registreren in het gerelateerde uitgaande bedrijfsdocument, zoals een verkooporder, of magazijnverzendingsdocumenten gebruiken die deel uitmaken van een werkstroom en met verschillende magazijnactiviteiten zijn geïntegreerd."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 223eed1ca4e362b8209373fac71d20ab88b2aaff
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="ship-items"></a>Artikelen verzenden
Wanneer u artikelen verzendt vanuit een magazijn waarvoor magazijnverzendingsverwerking niet is ingesteld, registreert u de verzending in het gerelateerde bedrijfsdocument, zoals een verkooporder, serviceorder, inkoopretourorder of uitgaande transferorder.

Als u artikelen verzendt vanuit een magazijn met magazijnverzendingsverwerking, kunt u artikelen alleen verzenden op basis van brondocumenten die door andere afdelingen zijn vrijgegeven voor magazijnactiviteiten.

> [!NOTE]
> Als u in uw magazijn met cross-docking en opslaglocaties werkt, kunt u voor elke regel u zien hoeveel artikelen in de cross-dockopslaglocaties zijn geplaatst. Deze aantallen worden automatisch berekend wanneer de velden op de verzending worden bijgewerkt. Als dit de artikelen voor de voorbereide verzending zijn, kunt u een pick maken voor alle regels en de verzendingen vervolgens voltooien. Zie [Artikelen cross-docken](warehouse-how-to-cross-dock-items.md) voor meer informatie.

## <a name="to-ship-items-with-a-sales-order"></a>Artikelen verzenden met een verkooporder
Hieronder wordt beschreven hoe u artikelen ontvangt met een inkooporder. De stappen zijn vergelijkbaar voor inkoopretourorders, serviceorders en uitgaande transferorders.  
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verkooporders** in en klik vervolgens op de gerelateerde koppeling.
2. Open een bestaande verkooporder of maak een nieuwe. Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie.
3. Voer in het veld **Te verzenden aantal** het aantal in dat u hebt ontvangen.

    De waarde in het veld **Verzonden aantal** wordt dienovereenkomstig bijgewerkt. Als het een gedeeltelijke verzending is, is de waarde lager dan de waarde in het veld **Aantal**.
4. Kies de actie **Boeken**.

## <a name="to-ship-items-with-a-warehouse-shipment"></a>Artikelen verzenden met een magazijnverzending
Eerst maakt u een verzendingsdocument op basis van een bedrijfsbrondocument. Vervolgens pickt u de opgegeven artikelen voor de verzending.

### <a name="to-create-a-warehouse-shipment"></a>Een magazijnverzending maken
Gewoonlijk maakt de werknemer die verantwoordelijk voor verzendingen is een magazijnverzending.
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Magazijnverzendingen** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies de actie **Nieuw**.  

    Vul de velden op het sneltabblad **Algemeen** in. Bij het ophalen van brondocumentregels worden bepaalde gegevens automatisch naar elke regel gekopieerd.  

    Voor magazijnconfiguraties met gestuurde opslag en pick: als de vestiging een standaardzone en -opslaglocatie voor verzendingen heeft, worden de velden **Zone** en **Opslaglocatie** automatisch ingevuld. U kunt deze waarden desgewenst wijzigen.  

    > [!NOTE]  
    >  Als u artikelen wilt verzenden met andere magazijnklassen dan de magazijnklasse van de opslaglocatie in het veld **Opslaglocatie** in de documentkop, moet u de inhoud van het veld **Opslaglocatie** in de kop verwijderen voordat u de brondocumentregels voor de artikelen ophaalt.  
3.  Kies de actie **Brondocumenten ophalen**. Het venster **Brondocumenten** verschijnt.

    U kunt vanuit een nieuwe of geopende magazijnverzending het venster **Filters om brondoc. op te halen** gebruiken voor het ophalen van de vrijgegeven brondocumentregels die bepalen welke artikelen moeten worden verzonden.

    1. Kies de actie **Filters om brondoc. op te halen gebruiken**.  
    2. U stelt een nieuw filter in door een omschrijvende code in te voeren in het veld **Code** en vervolgens de actie **Wijzigen** te kiezen.  
    3. Definieer het soort brondocumentregels dat u wilt ophalen door de relevante filtervelden in te vullen.  
    4. Kies de actie **Uitvoeren**.  

    Alle vrijgegeven brondocumentregels die voldoen aan de filtercriteria worden nu ingevoegd in het venster **Mag. -verzending** van waaruit u de filterfunctie hebt geactiveerd.  

    De filtercombinaties die u definieert, worden opgeslagen in het venster **Filters om brondoc. op te halen** tot de volgende keer dat u deze nodig hebt. U kunt een onbeperkt aantal filtercombinaties maken. U kunt de criteria op elk moment wijzigen door de actie **Wijzigen** te kiezen.

4.  Selecteer de brondocumenten waarvoor u artikelen wilt verzenden en klik op **OK**.  

De regels van de brondocumenten verschijnen in het venster **Mag. -verzending**. Het veld **Te verzenden aantal** is ingevuld met de openstaande hoeveelheid voor elke regel, maar u kunt het aantal wijzigen indien nodig. Als u de inhoud van het veld **Opslaglocatie** op het sneltabblad **Algemeen** verwijdert voordat u de regels ophaalt, moet u op elke verzendregel een opslaglocatie invullen.  

> [!NOTE]  
>  U kunt niet meer artikelen verzenden dan het aantal in het veld **Openstaand aantal** op de brondocumentregel. Als u meer artikelen wilt verzenden, haalt u een ander brondocument op dat een regel voor het item bevat. U gebruikt de filterfunctie om brondocumenten met het artikel op te halen.  

Als u alle regels voor de verzending hebt, kunt u het proces starten dat deze doorstuurt naar het magazijnpersoneel om te picken.

### <a name="to-pick-and-ship"></a>U kunt als volgt een verzending picken en verzenden
Doorgaans wordt een nieuw pickdocument gemaakt of een bestaand pickdocument geopend door een magazijnmedewerker die verantwoordelijk is voor pickactiviteiten.
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Magazijnverzendingen** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer de magazijnverzending waarvoor u wilt picken en kies de actie **Pick maken**.
3. Vul de velden in het venster in en klik vervolgens op de knop **OK**. Het opgegeven magazijnpickdocument wordt gemaakt.

    U kunt ook een bestaande magazijnpick openen.
4. Klik op het pictogram ![pictogram Zoeken naar pagina of rapport](media/ui-search/search_small.png "Zoeken naar pagina of rapport"), voer **Magazijnpicks** in en klik vervolgens op de gerelateerde koppeling. Selecteer de magazijnpick waaraan u wilt werken.

    Als het magazijn met opslaglocaties werkt, zijn de pickregels omgezet in Nemen- en Plaatsen-regels.

    U kunt deze regels sorteren, een werknemer aan de pick toewijzen, een breakbulkfilter instellen als u met gestuurde opslag en pick werkt en de pickinstructies afdrukken.

5. Voer de pick uit en plaats de artikelen in de opgegeven opslaglocatie voor verzending of in de verzendruimte als u niet met opslaglocaties werkt.
6. Kies de actie **Pick registreren**.

    De velden **Te verzenden aantal** en **Documentstatus** op de kop van het verzenddocument worden bijgewerkt. De gepickte artikelen zijn niet meer beschikbaar voor een andere verzending of voor interne bewerkingen.
7. Druk de verzenddocumenten af, bereid de zending voor en boek de zending.

Zie [Artikelen picken voor magazijnverzending](warehouse-how-to-pick-items-for-warehouse-shipment.md) voor meer informatie over het picken voor magazijnverzendingen.

U kunt in het pickvoorstel verschillende pickinstructies combineren tot één instructie (voor verschillende verzendingen) en zo de artikelen in het magazijn nog efficiënter picken. Zie [Picks plannen in voorstellen](warehouse-how-to-plan-picks-in-worksheets.md) voor meer informatie.

> [!NOTE]
> Als u de ontvangst van bepaalde artikelen in het magazijn afwacht en met cross-docken werkt, berekent [!INCLUDE[d365fin](includes/d365fin_md.md)] voor elke verzend- of pickvoorstelregel het aantal van het artikel in de cross-dockopslaglocatie. Dit veld wordt bijgewerkt telkens wanneer u het verzenddocument of het voorstel opent of sluit. Zie [Artikelen cross-docken](warehouse-how-to-cross-dock-items.md) voor meer informatie.

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

