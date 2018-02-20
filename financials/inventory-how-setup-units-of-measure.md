---
title: Artikeleenheden instellen | Microsoft Docs
description: U kunt meerdere maateenheden voor een artikel instellen zodat u maateenheden kunt toewijzen aan het artikel.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 01/12/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f6fad390b5b8d209212f20cfca5dfdd5fafd11cc
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-item-units-of-measure"></a>Artikeleenheden instellen
U kunt meerdere eenheden voor een artikel instellen zodat u eenheden kunt toewijzen aan het artikel voor de volgende doeleinden:

- Wijs een basiseenheid op de artikelkaart van het artikel toe om te bepalen hoe het wordt opgeslagen in voorraad en om als conversiebasis te dienen voor alternatieve eenheden.
- Wijs alternatieve eenheden aan inkoop-, productie- of verkoopdocumenten toe om op te geven hoeveel eenheden van de basiseenheid u tegelijk verwerkt in die processen. U kunt het artikel bijvoorbeeld kopen op pallets en alleen afzonderlijke delen in de productie gebruiken.

Als een artikel in één eenheid in voorraad is, maar in een andere eenheid wordt geproduceerd, kan een productieorder worden gemaakt die gebruikmaakt van een productiebatcheenheid voor het berekenen van het juiste aantal onderdelen tijdens de batchverwerking **Productieorder vernieuwen**. Een voorbeeld van een berekening van een productiebatcheenheid is wanneer een geproduceerd artikel als stukgoed in voorraad is maar in tonnen gewicht wordt geproduceerd. Zie voor meer informatie [Werken met productiebatcheenheden](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).

## <a name="to-set-up-a-unit-of-measure"></a>Een eenheid instellen
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikelen** in en klik vervolgens op de gerelateerde koppeling.
2. Open de artikelkaart waarvoor u alternatieve eenheden wilt instellen.
3. Kies de actie **Eenheden**. Het venster **Artikeleenheden** wordt geopend.
4. Als het veld **Basiseenheid** op de artikelkaart is ingevuld, is die eenheid al ingesteld.
5. Kies de actie **Nieuw**. Een nieuwe lege regel wordt ingevoegd.
6. Voer in het veld **Code** de naam van de eenheid in. Of kies het veld waaruit u de eenheidscodes in de database wilt selecteren.
7. Voer in het veld **Aantal per eenheid** in hoeveel eenheden van de basismaateenheid de nieuwe maateenheid bevat.
8. Herhaal stap 5 t/m 7 om alle alternatieve eenheden in te stellen die u in verschillende processen voor dit artikel wilt gebruiken.

U kunt nu afwisselende eenheden gebruiken op inkoop-, productie- en verkoopdocumenten. Zie voor meer informatie Standaardeenheidscodes invoeren voor inkoop- en verkooptransacties of De productiebatcheenheid gebruiken.

## <a name="to-set-up-unit-of-measure-translations"></a>Eenheidsvertalingen instellen
Wanneer u artikelen aan buitenlandse klanten verkoopt, wilt u de eenheid mogelijk opgeven in de taal van de klant. Als u dit wilt doen, moet u de benodigde eenheidsvertalingen instellen.

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Zoeken naar pagina of rapport"), voer **Eenheden** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer de code waarvoor u vertalingen wilt instellen en kies de actie **Vertalingen**.
3. Selecteer in het veld **Taal** de pijl-omlaag voor een overzicht van de beschikbare taalcodes. Selecteer de taalcode waarvoor u een vertaling wilt invoeren en kies de knop OK om de code naar het veld te kopiëren.
4. Voer de gewenste tekst in het veld **Omschrijving** in.
5. Herhaal stap 2 tot en met 4 voor de maateenheidscodes en de talen waarvoor u vertalingen wilt invoeren.

## <a name="to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions"></a>Standaardeenheidscodes invoeren voor verkoop- en inkooptransacties
Als u doorgaans in andere eenheden dan de basiseenheid inkoopt of verkoopt, kunt u verschillende eenheden opgeven voor inkopen en verkopen. U moet hiervoor de eenheden instellen in het venster **Artikeleenheden**.

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikelen** in en klik vervolgens op de gerelateerde koppeling.
2. Open de desbetreffende artikelkaart waarvoor u een standaardeenheidscode voor verkopen of inkopen wilt opgeven.
3. Open voor verkopen op het sneltabblad **Factureren** in het veld **Verkoopeenheid** het venster **Artikeleenheden**.
4. Open voor inkopen op het sneltabblad **Aanvulling** in het veld **Ink.-eenheid** het venster **Artikeleenheden**.
5. Selecteer de code die u als standaardeenheid voor respectievelijk verkopen of inkopen wilt instellen en kies de knop **OK**.

## <a name="see-also"></a>Zie ook
[Werken met productiebatcheenheden](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[Voorraad beheren](inventory-manage-inventory.md)  
[Inkopen beheren](purchasing-manage-purchasing.md)  
[Verkopen beheren](sales-manage-sales.md)    
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

