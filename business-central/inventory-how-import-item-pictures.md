---
title: Veel artikelafbeeldingen uit een ZIP-bestand importeren | Microsoft Docs
description: U kunt meerdere artikelafbeeldingen in één keer importeren. Geef uw afbeeldingsbestanden namen die corresponderen met uw artikelnummers, comprimeer ze in een zip-bestand en gebruik vervolgens de pagina Artikelafbeeldingen importeren om te bepalen welke artikelafbeeldingen worden geïmporteerd.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product, image
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4da0f30f47827515f8591802ce2ca49c245009ab
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922906"
---
# <a name="import-multiple-item-pictures"></a>Meerdere artikelafbeeldingen importeren
U kunt meerdere artikelafbeeldingen in één keer importeren. Geef uw afbeeldingsbestanden namen die corresponderen met uw artikelnummers, comprimeer ze in een zip-bestand en gebruik vervolgens de pagina **Artikelafbeeldingen importeren** om te bepalen welke artikelafbeeldingen worden geïmporteerd.

Alle algemene bestandsindelingen worden ondersteund.

## <a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a>Afbeeldingsbestanden noemen naar de artikelnamen en het ZIP-bestand voorbereiden
1. Benoem elk bestand op de locatie waar uw artikelafbeeldingen zijn opgeslagen volgens het nummer van het gerelateerde artikel. Voorbeeld:

    |Artikelnr.|Bestandsnaam|
    |-|-|
    |1000|1000.bmp|
    |1001|1001.bmp|
    |1002|1002.bmp|

2. Verzamel alle bestanden in een ZIP-bestand. Selecteer bijvoorbeeld in Windows Verkenner de bestanden, en kies **Verzenden naar** , **Gecomprimeerde (gezipte) map** .     

## <a name="to-import-item-pictures"></a>Artikelafbeeldingen importeren
1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraad instellen** in en kies de desbetreffende koppeling.
2. Kies de actie **Artikelafbeeldingen importeren** .
3. Selecteer in het veld **Een ZIP-bestand selecteren** de relevante ZIP-map en kies de knop **Openen** .

    Er wordt een regel voor elk artikel en afbeelding gemaakt op de pagina **Artikelafbeeldingen importeren** .

    > [!NOTE]
    > Voor artikelkaarten die al een afbeelding hebben, wordt het selectievakje **Afbeelding bestaat al** geselecteerd. Als u geen bestaande afbeeldingen wilt vervangen, schakelt u het selectievakje **Afbeeldingen vervangen** uit. Als u geen afzonderlijke bestaande afbeeldingen wilt vervangen, verwijdert u de desbetreffende regels.

3. Kies de actie **Afbeeldingen importeren** .

Het veld **Status importeren** wordt bijgewerkt om aan te geven of de afbeeldingsimport is voltooid of overgeslagen.       

## <a name="see-also"></a>Zie ook
[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Nummerreeksen maken](ui-create-number-series.md)  
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
