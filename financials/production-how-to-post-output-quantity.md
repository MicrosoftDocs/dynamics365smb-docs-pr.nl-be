---
title: Productie-output en bewerkingstijd in batches boeken | Microsoft Docs
description: Het outputaantal geeft het gereedgemelde aantal van onderhanden werk aan.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: e885149e28c2e09dc244bc5c0a431e7b2fe047a5
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="batch-post-output-and-run-times"></a>Output en bewerkingstijden in batches boeken
Het outputaantal geeft het gereedgemelde aantal van onderhanden werk aan.  

> [!NOTE]
> Alleen wanneer u het outputaantal bij de laatste bewerking boekt, wordt de voorraad automatisch bijgewerkt.  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a>Outputaantallen voor een of meer productieorderregels boeken
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Outputdagboek** in en klik vervolgens op de gerelateerde koppeling.  
2. Voer in de velden informatie over de productieorder en output in. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Als de bewerking is voltooid, selecteert u het veld **Voltooid**.  

    Als het magazijn waar de artikelen worden opgeslagen opslaglocaties gebruikt, maar geen pickverwerking vereist, kunt u  een opslaglocatie toewijzen aan de dagboekregel om aan te geven waar de artikelen in het magazijn moeten worden geplaatst. Zie [Productie- of assemblageoutput opslaan](warehouse-how-to-put-away-production-output.md) voor meer informatie.  

4. Kies de actie **Boeken** om de bewerkingen te boeken. Het outputaantal wordt geboekt. Het artikel is nu beschikbaar voor verzending.  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a>Bewerkingstijd boeken voor een of meerdere productieorderregels
De bewerkingstijd geeft de benodigde werktijd voor onderhanden werk aan.    

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Outputdagboek** in en klik vervolgens op de gerelateerde koppeling.  
2. Voer in de velden informatie over de productieorder en output in.  
3.  Als de bewerking is voltooid, selecteert u het veld **Voltooid**.  
4. Kies de actie **Boeken** om de bestede tijd per bewerking te boeken. Capaciteitsposten worden bijgewerkt voor de gebruikte afdelingen of bewerkingsplaatsen.

## <a name="see-also"></a>Zie ook  
[Productie](production-manage-manufacturing.md)    
[Productie instellen](production-configure-production-processes.md)  
[Gepland](production-planning.md)      
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

