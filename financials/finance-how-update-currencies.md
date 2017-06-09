---
title: 'Procedure: Valutawisselkoersen bijwerken | Microsoft Docs'
description: Werken met meerdere valuta&quot;s
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, Yahoo
ms.date: 03/24/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: b261da0f233ce78a9f14c2979c876be401ffedef
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-update-currency-exchange-rates"></a>Procedure: Valutawisselkoersen bijwerken
U moet een code instellen voor elke gebruikte valuta als u in andere valuta's dan uw lokale valuta inkoopt of verkoopt, in een andere valuta tegoeden of schulden hebt of grootboektransacties in verschillende valuta's vastlegt.  

**Opmerking**: voor deze functionaliteit is vereist dat uw ervaring is ingesteld op **Pakket**. Zie [Uw ervaring in [!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen](ui-experiences.md) voor meer informatie.

U kunt een externe service gebruiken om valutawisselkoersen actueel te houden. De Yahoo Currency Exchange Rates-service is vooraf geïnstalleerd en kan worden ingeschakeld.

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Een wisselkoersservice instellen
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Valutawisselkoersservices** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul in het venster **Valutawisselkoersservice** indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Kies het selectievakje **Ingeschakeld** om de service in te schakelen.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Valutawisselkoersen bijwerken met een service
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Valuta´s** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Wisselkoersen bijwerken**.

De waarde in het veld **Wisselkoers** in het venster **Valuta´s** wordt bijgewerkt met de laatste wisselkoers.

## <a name="see-also"></a>Zie ook
[Afsluitingsjaren en -perioden](year-close-years-periods.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

