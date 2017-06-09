---
title: 'Procedure: Leveranciers in een prioriteitsvolgorde plaatsen | Microsoft Docs'
description: 'Procedure: leveranciers in een prioriteitsvolgorde plaatsen'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ae80ae9ecc15838b59999ded775c7fa0063c8a54
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-prioritize-vendors"></a>Procedure: leveranciers in een prioriteitsvolgorde plaatsen
[!INCLUDE[d365fin](includes/d365fin_md.md)] heeft een functie die voorstellen kan doen voor betalingen aan leveranciers, bijvoorbeeld bij betalingen die binnenkort moeten worden betaald, of als voor een betaling een korting mogelijk is. Zie voor meer informatie [Procedure: Leveranciersbetalingen voorstellen](payables-how-suggest-vendor-payments.md).

Eerst moet u aan uw leveranciers eerst een prioriteit toewijzen door nummers aan hen toe te wijzen.

## <a name="to-prioritize-vendors"></a>Leveranciers in een prioriteitsvolgorde plaatsen
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Leveranciers** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de relevante leverancier en kies **Bewerken**.
3. Voer in het veld **Prioriteit** een nummer in.

In [!INCLUDE[d365fin](includes/d365fin_md.md)] heeft het laagste nummer, 0 uitgezonderd, de hoogste prioriteit. Als u bijvoorbeeld de nummers 1, 2 en 3 toewijst, heeft nummer 1 de hoogste prioriteit.

Als u geen prioriteitsnummer wilt toekennen aan een leverancier, laat u het veld **Prioriteit** leeg. Die leverancier wordt onder alle leveranciers met prioriteitsnummers geplaatst wanneer u betalingsvoorstellen in het programma inschakelt. U kunt zo veel prioriteitsniveaus invoeren als er nodig zijn.

## <a name="see-also"></a>Zie ook
[Inkoop instellen](purchasing-setup-purchasing.md)  
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

