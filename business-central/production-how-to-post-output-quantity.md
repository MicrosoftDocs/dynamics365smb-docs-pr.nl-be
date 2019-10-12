---
title: Productie-output en bewerkingstijd in batches boeken | Microsoft Docs
description: Het outputaantal geeft het gereedgemelde aantal van onderhanden werk aan.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: cc4acf5fbaf10df3b833e310a83854e52b0d2b73
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313264"
---
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="86338-103">Output en bewerkingstijden in batches boeken</span><span class="sxs-lookup"><span data-stu-id="86338-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="86338-104">Het outputaantal geeft het gereedgemelde aantal van onderhanden werk aan.</span><span class="sxs-lookup"><span data-stu-id="86338-104">The output quantity represents the work progress in the form of the finished quantity.</span></span>  

> [!NOTE]
> <span data-ttu-id="86338-105">Alleen wanneer u het outputaantal bij de laatste bewerking boekt, wordt de voorraad automatisch bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="86338-105">Only when you post output quantity on the last operation, the inventory is updated automatically.</span></span>  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a><span data-ttu-id="86338-106">Outputaantallen voor een of meer productieorderregels boeken</span><span class="sxs-lookup"><span data-stu-id="86338-106">To post output quantities for one or more production order lines</span></span>
1. <span data-ttu-id="86338-107">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Outputdagboek** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="86338-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="86338-108">Voer in de velden informatie over de productieorder en output in.</span><span class="sxs-lookup"><span data-stu-id="86338-108">Fill in the fields with the production order data and the output data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="86338-109">Als de bewerking is voltooid, selecteert u het veld **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="86338-109">If the operation has been completed, select the **Finished** field.</span></span>  

    <span data-ttu-id="86338-110">Als het magazijn waar de artikelen worden opgeslagen opslaglocaties gebruikt, maar geen pickverwerking vereist, kunt u  een opslaglocatie toewijzen aan de dagboekregel om aan te geven waar de artikelen in het magazijn moeten worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="86338-110">If the warehouse location where the items should be put away uses bins but does not require put-away processing,  assign a bin code to the journal line to specify where the items should be placed in the warehouse.</span></span> <span data-ttu-id="86338-111">Zie [Productie- of assemblageoutput opslaan](warehouse-how-to-put-away-production-output.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="86338-111">For more information, see [Put Away Production or Assembly Output](warehouse-how-to-put-away-production-output.md).</span></span>  

4. <span data-ttu-id="86338-112">Kies de actie **Boeken** om de bewerkingen te boeken.</span><span class="sxs-lookup"><span data-stu-id="86338-112">Choose the **Post** acto post the operations.</span></span> <span data-ttu-id="86338-113">Het outputaantal wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="86338-113">The output quantity will be posted.</span></span> <span data-ttu-id="86338-114">Het artikel is nu beschikbaar voor verzending.</span><span class="sxs-lookup"><span data-stu-id="86338-114">The item is now available for shipping.</span></span>  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="86338-115">Bewerkingstijd boeken voor een of meerdere productieorderregels</span><span class="sxs-lookup"><span data-stu-id="86338-115">To post run times for one or more production order lines</span></span>
<span data-ttu-id="86338-116">De bewerkingstijd geeft de benodigde werktijd voor onderhanden werk aan.</span><span class="sxs-lookup"><span data-stu-id="86338-116">The run time represents work progress in the form of the necessary working time.</span></span>    

1.  <span data-ttu-id="86338-117">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Outputdagboek** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="86338-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="86338-118">Voer in de velden informatie over de productieorder en output in.</span><span class="sxs-lookup"><span data-stu-id="86338-118">Fill in the fields with the production order data and the output data.</span></span>  
3.  <span data-ttu-id="86338-119">Als de bewerking is voltooid, selecteert u het veld **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="86338-119">If the operation is completed, select the **Finished** field.</span></span>  
4. <span data-ttu-id="86338-120">Kies de actie **Boeken** om de bestede tijd per bewerking te boeken.</span><span class="sxs-lookup"><span data-stu-id="86338-120">Choose the **Post** action to post the time spent per operation.</span></span> <span data-ttu-id="86338-121">Capaciteitsposten worden bijgewerkt voor de gebruikte afdelingen of bewerkingsplaatsen.</span><span class="sxs-lookup"><span data-stu-id="86338-121">Capacity ledger entries are updated for the used work or machine centers.</span></span>

## <a name="see-also"></a><span data-ttu-id="86338-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="86338-122">See Also</span></span>  
<span data-ttu-id="86338-123">[Productie](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="86338-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="86338-124">Productie instellen</span><span class="sxs-lookup"><span data-stu-id="86338-124">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="86338-125">[Gepland](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="86338-125">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="86338-126">Voorraad</span><span class="sxs-lookup"><span data-stu-id="86338-126">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="86338-127">Inkoop</span><span class="sxs-lookup"><span data-stu-id="86338-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="86338-128">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="86338-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
