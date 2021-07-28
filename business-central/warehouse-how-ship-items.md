---
title: Artikelen verzenden
description: In dit onderwerp wordt beschreven hoe u artikelen vanuit uw magazijn verzendt, afhankelijk van uw magazijnconfiguratie voor verzendingsverwerking.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 60274947bb0f38ed6e116767ac5c74357482298c
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435946"
---
# <a name="ship-items"></a>Artikelen verzenden

Wanneer u artikelen verzendt vanuit een magazijn waarvoor magazijnverzendingsverwerking niet is ingesteld, registreert u de verzending in het gerelateerde bedrijfsdocument, zoals een verkooporder, serviceorder, inkoopretourorder of uitgaande transferorder.

Als u artikelen verzendt vanuit een magazijn dat is ingesteld voor magazijnverzendingsverwerking, kunt u artikelen alleen verzenden op basis van brondocumenten die door andere afdelingen zijn vrijgegeven voor magazijnactiviteiten.

> [!NOTE]
> Als u in uw magazijn met cross-docking en opslaglocaties werkt, kunt u voor elke regel u zien hoeveel artikelen in de cross-dockopslaglocaties zijn geplaatst. Deze aantallen worden automatisch berekend wanneer de velden op de verzending worden bijgewerkt. Als dit de artikelen voor de voorbereide verzending zijn, kunt u een pick maken voor alle regels en de verzendingen vervolgens voltooien. Zie [Artikelen cross-docken](warehouse-how-to-cross-dock-items.md) voor meer informatie.

## <a name="to-ship-items-with-a-sales-order"></a>Artikelen verzenden met een verkooporder

Hieronder wordt beschreven hoe u artikelen verzendt vanuit een verkooporder. De stappen zijn vergelijkbaar voor inkoopretourorders, serviceorders en uitgaande transferorders.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.
2. Open een bestaande verkooporder of maak een nieuwe. Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie.
3. Voer in het veld **Te verzenden aantal** het aantal in dat u hebt verzonden.

    De waarde in het veld **Verzonden aantal** wordt dienovereenkomstig bijgewerkt. Als het een gedeeltelijke verzending is, is de waarde lager dan de waarde in het veld **Aantal**.
4. Kies de actie **Boeken**.

> [!NOTE]
> Als uw organisatie geen verkooporders gebruikt, dan, wanneer u de verkoopfactuur boekt, gaat [!INCLUDE [prod_short](includes/prod_short.md)] ervan uit dat u de volledige hoeveelheid heeft verzonden. Als dit in tegenspraak is met hoe uw organisatie werkt, raden we u aan verkooporders te gebruiken en zendingen te registreren zoals uitgelegd in dit artikel.

## <a name="to-ship-items-with-a-warehouse-shipment"></a>Artikelen verzenden met een magazijnverzending

Eerst maakt u een verzendingsdocument op basis van een bedrijfsbrondocument. Vervolgens pickt u de opgegeven artikelen voor de verzending.

### <a name="to-create-a-warehouse-shipment"></a>Een magazijnverzending maken

Gewoonlijk maakt de werknemer die verantwoordelijk voor verzendingen is, een magazijnverzending. De volgende procedure beschrijft hoe u de zending handmatig kunt maken in de standaardversie van [!INCLUDE[prod_short](includes/prod_short.md)], maar uw organisatie heeft mogelijk een geautomatiseerd deel van het proces, zoals het gebruik van draagbare of gemonteerde scanners die worden ondersteund door externe providers.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Magazijnverzendingen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  

    Vul de velden op het sneltabblad **Algemeen** in. Bij het ophalen van brondocumentregels worden bepaalde gegevens automatisch naar elke regel gekopieerd.  

    Voor magazijnconfiguraties met gestuurde opslag en pick: als de vestiging een standaardzone en -opslaglocatie voor verzendingen heeft, worden de velden **Zone** en **Opslaglocatie** automatisch ingevuld. U kunt deze waarden desgewenst wijzigen.  

    > [!NOTE]  
    > Als u artikelen wilt verzenden met andere magazijnklassen dan de magazijnklasse van de opslaglocatie in het veld **Opslaglocatie** in de documentkop, moet u de inhoud van het veld **Opslaglocatie** in de kop verwijderen voordat u de brondocumentregels voor de artikelen ophaalt.  
3. Kies de actie **Brondocumenten ophalen**. De pagina **Brondocumenten** verschijnt.

    U kunt vanuit een nieuwe of geopende magazijnverzending de pagina **Filters om brondoc. op te halen** gebruiken voor het ophalen van de vrijgegeven brondocumentregels die bepalen welke artikelen moeten worden verzonden.

    1. Kies de actie **Filters om brondoc. op te halen gebruiken**.  
    2. U stelt een nieuw filter in door een omschrijvende code in te voeren in het veld **Code** en vervolgens de actie **Wijzigen** te kiezen.  
    3. Definieer het soort brondocumentregels dat u wilt ophalen door de relevante filtervelden in te vullen.  
    4. Kies de actie **Uitvoeren**.  

    Alle vrijgegeven brondocumentregels die voldoen aan de filtercriteria worden nu ingevoegd op de pagina **Mag. -verzending** van waaruit u de filterfunctie hebt geactiveerd.  

    De filtercombinaties die u definieert, worden opgeslagen op de pagina **Filters om brondoc. op te halen** tot de volgende keer dat u deze nodig hebt. U kunt een onbeperkt aantal filtercombinaties maken. U kunt de criteria op elk moment wijzigen door de actie **Wijzigen** te kiezen.

4. Selecteer de brondocumenten waarvoor u artikelen wilt verzenden en klik op **OK**.  

De regels van de brondocumenten verschijnen op de pagina **Mag. -verzending**. Het veld **Te verzenden aantal** is ingevuld met de openstaande hoeveelheid voor elke regel, maar u kunt het aantal wijzigen indien nodig. Als u de inhoud van het veld **Opslaglocatie** op het sneltabblad **Algemeen** verwijdert voordat u de regels ophaalt, moet u op elke verzendregel een opslaglocatie invullen.  

> [!NOTE]  
> U kunt niet meer artikelen verzenden dan het aantal in het veld **Openstaand aantal** op de brondocumentregel. Als u meer artikelen wilt verzenden, haalt u een ander brondocument op dat een regel voor het item bevat. U gebruikt de filterfunctie om brondocumenten met het artikel op te halen.  

Als u alle regels voor de verzending hebt, kunt u het proces starten dat deze doorstuurt naar het magazijnpersoneel om te picken.

### <a name="to-pick-and-ship"></a>U kunt als volgt een verzending picken en verzenden

Doorgaans wordt een nieuw pickdocument gemaakt of een bestaand pickdocument geopend door een magazijnmedewerker die verantwoordelijk is voor pickactiviteiten.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnverzendingen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de magazijnverzending waarvoor u wilt picken en kies de actie **Pick maken**.
3. Vul de velden op de pagina in en klik vervolgens op de knop **OK**. Het opgegeven magazijnpickdocument wordt gemaakt.

    U kunt ook een bestaande magazijnpick openen.
4. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Picks** in en kies vervolgens de gerelateerde koppeling. Selecteer de magazijnpick waaraan u wilt werken.

    Als het magazijn met opslaglocaties werkt, zijn de pickregels omgezet in Nemen- en Plaatsen-regels.

    U kunt deze regels sorteren, een werknemer aan de pick toewijzen, een breakbulkfilter instellen als u met gestuurde opslag en pick werkt en de pickinstructies afdrukken.

5. Voer de pick uit en plaats de artikelen in de opgegeven opslaglocatie voor verzending of in de verzendruimte als u niet met opslaglocaties werkt.
6. Kies de actie **Pick registreren**.

    De velden **Te verzenden aantal** en **Documentstatus** op de kop van het verzenddocument worden bijgewerkt. De gepickte artikelen zijn niet meer beschikbaar voor een andere verzending of voor interne bewerkingen.
7. Druk de verzenddocumenten af, bereid de zending voor en boek de zending.

Zie [Artikelen picken voor magazijnverzending](warehouse-how-to-pick-items-for-warehouse-shipment.md) voor meer informatie over het picken voor magazijnverzendingen.

U kunt in het pickvoorstel verschillende pickinstructies combineren tot één instructie (voor verschillende verzendingen) en zo de artikelen in het magazijn nog efficiënter picken. Zie [Picks plannen in voorstellen](warehouse-how-to-plan-picks-in-worksheets.md) voor meer informatie.

> [!NOTE]
> Als u de ontvangst van bepaalde artikelen in het magazijn afwacht en met cross-docken werkt, berekent [!INCLUDE[prod_short](includes/prod_short.md)] voor elke verzend- of pickvoorstelregel het aantal van het artikel in de cross-dockopslaglocatie. Dit veld wordt bijgewerkt telkens wanneer u het verzenddocument of het voorstel opent of sluit. Zie [Artikelen cross-docken](warehouse-how-to-cross-dock-items.md) voor meer informatie.

## <a name="see-also"></a>Zie ook

[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Assemblagebeheer](assembly-assemble-items.md)  
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]