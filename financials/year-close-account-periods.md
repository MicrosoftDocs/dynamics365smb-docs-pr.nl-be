---
title: 'Procedure: Boekingsperioden afsluiten | Microsoft Docs'
description: Hierin wordt uitgelegd hoe u boekingsperioden afsluit.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 69bea225084f239523c4ed67471b52ad91e914d9
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-close-accounting-periods"></a>Procedure: boekhoudperioden afsluiten
Wanneer een boekjaar is afgelopen, moet u de hierin opgenomen perioden afsluiten.

## <a name="to-close-accounting-periods"></a>Boekhoudperioden afsluiten
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Boekingsperioden** in en kies vervolgens de gerelateerde koppeling.
2. Kies in het venster **Boekingsperioden** de actie **Jaar afsluiten**.

    Als er meerdere boekjaren zijn geopend, wordt het vroegste boekjaar automatisch geselecteerd om te worden afgesloten. Er verschijnt een bericht waarin wordt aangegeven welk jaar wordt afgesloten en welke gevolgen dit heeft.
3. Kies de knop **Ja** om het jaar af te sluiten.

Het boekjaar is nu afgesloten en de selectievakjes **Afgesloten** en **Geblokkeerd** zijn ingeschakeld voor alle perioden van het jaar. U kunt het boekjaar niet meer openen en de selectievakjes **Afgesloten** en **Geblokkeerd** niet uitschakelen.

**Opmerking**: u kunt een boekjaar niet afsluiten voordat u een nieuw boekjaar hebt gemaakt. Wanneer een boekjaar is afgesloten, kunt u de begindatum van het volgende boekjaar niet meer wijzigen.

Zelfs als een boekjaar is afgesloten, kunt u er nog steeds grootboekposten voor boeken. Als u dit doet, worden de posten gemarkeerd als zijnde geboekt naar een afgesloten boekjaar en wordt het veld **Naboeking** geselecteerd.

Nadat een boekjaar is afgesloten, moet u de resultaten- of winst- en verliesrekeningen afsluiten en de jaarresultaten naar een balansrekening overbrengen. U kunt deze procedure herhalen telkens wanneer u boekt naar een afgesloten boekjaar.

## <a name="see-also"></a>Zie ook
[Boeken afsluiten](year-close-books.md)  
[Procedure: de jaareinde-ultimopost boeken](year-how-post-year-end-close-entry.md)  
[Procedure: Nieuw boekjaar openen](finance-how-open-new-fiscal-year.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

