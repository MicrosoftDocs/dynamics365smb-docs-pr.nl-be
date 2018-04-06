---
title: Resourcegebruik en prijzen vastleggen en aanpassen| Microsoft Docs
description: Beschrijft hoe u het resourcegebruik of -verbruik kunt vastleggen dat is gekoppeld aan een project, om kosten, prijzen en werksoorten bij te houden en te beheren.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f86fed1b300df98ef120e2f91fdd0785670d04f1
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="use-resources-for-jobs"></a><span data-ttu-id="27560-103">Resources gebruiken voor projecten</span><span class="sxs-lookup"><span data-stu-id="27560-103">Use Resources for Jobs</span></span>
<span data-ttu-id="27560-104">U legt het gebruik van resources vast in het projectdagboek om kosten, prijzen en de werksoorten bij te houden die zijn gekoppeld aan projecten.</span><span class="sxs-lookup"><span data-stu-id="27560-104">You record the usage of resources in the job journal to keep track of costs, prices, and the work types that are linked to jobs.</span></span> <span data-ttu-id="27560-105">Zie voor meer informatie [Gebruik vastleggen voor projecten](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="27560-105">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

<span data-ttu-id="27560-106">U kunt ook het verbruik van een resource boeken in een resourcedagboek.</span><span class="sxs-lookup"><span data-stu-id="27560-106">You can also post the usage of a resource in a resource journal.</span></span> <span data-ttu-id="27560-107">Posten die in een resourcedagboek zijn geboekt, werken niet door in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="27560-107">Entries posted in a resource journal have no effect on the general ledger.</span></span>

## <a name="to-assign-resources-to-jobs"></a><span data-ttu-id="27560-108">Resources toewijzen aan projecten</span><span class="sxs-lookup"><span data-stu-id="27560-108">To assign resources to jobs</span></span>
<span data-ttu-id="27560-109">U wijst resources aan projecten toe door projectplanningsregels voor het project te maken.</span><span class="sxs-lookup"><span data-stu-id="27560-109">You assign resources to jobs by creating job planning lines for the job.</span></span> <span data-ttu-id="27560-110">Zie voor meer informatie [Projecten maken](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="27560-110">For more information, see [Create Jobs](projects-how-create-jobs.md).</span></span>

## <a name="to-record-resource-usage-for-a-job"></a><span data-ttu-id="27560-111">Resourceverbruik voor een project vastleggen</span><span class="sxs-lookup"><span data-stu-id="27560-111">To record resource usage for a job</span></span>
1. <span data-ttu-id="27560-112">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projectdagboeken** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="27560-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="27560-113">Open een relevante projectdagboekbatch en vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="27560-113">Open a relevant job journal batch, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="27560-114">Wanneer het dagboek compleet is, kiest u de actie **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="27560-114">When the journal is complete, choose the **Post** action.</span></span>

## <a name="to-adjust-resource-prices"></a><span data-ttu-id="27560-115">Resourceprijzen aanpassen</span><span class="sxs-lookup"><span data-stu-id="27560-115">To adjust resource prices</span></span>
<span data-ttu-id="27560-116">Als u kost- of verkoopprijzen wilt wijzigen voor een groot aantal resources, kunt u een batchverwerking gebruiken.</span><span class="sxs-lookup"><span data-stu-id="27560-116">If you want to change costs or prices for a large number of resources, you can use a batch job.</span></span>  

1. <span data-ttu-id="27560-117">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Resourceprijzen herwaarderen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="27560-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Adjust Resource Costs/Prices**, and then choose the related link.</span></span>
2. <span data-ttu-id="27560-118">Vul de overige velden op een regel desgewenst in en kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="27560-118">Fill in the fields on a line as necessary, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="27560-119">Met deze batchverwerking worden geen alternatieve kosten of prijzen voor resources gemaakt of aangepast.</span><span class="sxs-lookup"><span data-stu-id="27560-119">This batch job does not create or adjust alternate costs or prices for resources.</span></span> <span data-ttu-id="27560-120">Dit verandert alleen de inhoud van het veld op de resourcekaart voor het veld **Aan te passen prijs** dat u hebt geselecteerd in de batchtaak.</span><span class="sxs-lookup"><span data-stu-id="27560-120">It only changes the contents of the field on the resource card for the **Adjust Field** field that you selected in the batch job.</span></span> <span data-ttu-id="27560-121">De aanpassing werkt onmiddellijk door voor de resources. Controleer daarom uw herwaarderingsfactoren zorgvuldig voordat u de batchverwerking uitvoert.</span><span class="sxs-lookup"><span data-stu-id="27560-121">The adjustment will take effect immediately for resources, so check your adjustment factors before you run the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a><span data-ttu-id="27560-122">Suggesties voor wijzigingen van resourceprijzen krijgen op basis van bestaande alternatieve prijzen</span><span class="sxs-lookup"><span data-stu-id="27560-122">To get resource price change suggestions based on existing alternate prices</span></span>
<span data-ttu-id="27560-123">Als u al alternatieve resourceprijzen hebt ingesteld voor bepaalde resources, kunt u een batchverwerking gebruiken om meerdere alternatieve resourceprijzen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="27560-123">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="27560-124">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png ""pictogram Zoeken naar pagina of rapport"), voer **Resourceprijswijzigingen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="27560-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="27560-125">Kies de actie **Res.prijsvoorstellen (Prijs)** en vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="27560-125">Choose the **Suggest Res. Price Chg. (Price)** action, and then fill in the fields as necessary.</span></span>
3. <span data-ttu-id="27560-126">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="27560-126">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="27560-127">Nadat de batchverwerking is voltooid, bevat het venster **Resourceprijswijzigingen** de resultaten van de batchverwerking.</span><span class="sxs-lookup"><span data-stu-id="27560-127">When the batch job is finished, the **Resource Price Changes** window shows the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a><span data-ttu-id="27560-128">Resourceprijsvoorstellen ophalen op basis van standaardverkoopprijzen</span><span class="sxs-lookup"><span data-stu-id="27560-128">To get resource price change suggestions based on standard prices</span></span>
<span data-ttu-id="27560-129">Als u meerdere alternatieve resourceprijzen wilt instellen op basis van de standaardverkoopprijzen op de resourcekaarten, kunt u een batchverwerking gebruiken.</span><span class="sxs-lookup"><span data-stu-id="27560-129">If you want to set up multiple alternate resource prices based on the standard prices on the resource cards, you can use a batch job.</span></span>  

1. <span data-ttu-id="27560-130">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png ""pictogram Zoeken naar pagina of rapport"), voer **Resourceprijswijzigingen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="27560-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="27560-131">Kies de actie **Res.prijsvoorstellen (Res.)** en vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="27560-131">Choose the **Suggest Res. Price Chg. (Res.)** action, and then fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="27560-132">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="27560-132">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="27560-133">Nadat de batchverwerking is voltooid, opent u het venster **Resourceprijswijzigingen** om de resultaten van de batchverwerking te bekijken.</span><span class="sxs-lookup"><span data-stu-id="27560-133">When the batch job is finished, open the **Resource Price Changes** window to see the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a><span data-ttu-id="27560-134">Suggesties voor wijzigingen van resourceprijzen krijgen op basis van alternatieve prijzen</span><span class="sxs-lookup"><span data-stu-id="27560-134">To get resource price change suggestions based on alternate prices</span></span>
<span data-ttu-id="27560-135">Als u al alternatieve resourceprijzen hebt ingesteld voor bepaalde resources, kunt u een batchverwerking gebruiken om meerdere alternatieve resourceprijzen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="27560-135">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="27560-136">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png ""pictogram Zoeken naar pagina of rapport"), voer **Resourceprijswijziging voorstellen (Prijs)** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="27560-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Suggest Res. Price Chg. (Price)**, and then choose the related link.</span></span>  
2. <span data-ttu-id="27560-137">Vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="27560-137">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="27560-138">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="27560-138">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="27560-139">Nadat de batchverwerking is voltooid, opent u het venster **Resourceprijswijzigingen** om de resultaten van de batchverwerking te bekijken.</span><span class="sxs-lookup"><span data-stu-id="27560-139">When the batch job is finished, open the **Resource Price Changes** window to see the results of the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="27560-140">Zie ook</span><span class="sxs-lookup"><span data-stu-id="27560-140">See Also</span></span>
[<span data-ttu-id="27560-141">Projectbeheer</span><span class="sxs-lookup"><span data-stu-id="27560-141">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="27560-142">Financiën</span><span class="sxs-lookup"><span data-stu-id="27560-142">Finance</span></span>](finance.md)  
<span data-ttu-id="27560-143">[Inkoop](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="27560-143">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="27560-144">[Verkoop](sales-manage-sales.md)   </span><span class="sxs-lookup"><span data-stu-id="27560-144">[Sales](sales-manage-sales.md)   </span></span>  
<span data-ttu-id="27560-145">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="27560-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

