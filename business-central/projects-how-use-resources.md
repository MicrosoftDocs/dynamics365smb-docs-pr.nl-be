---
title: Resourcegebruik en prijzen vastleggen en aanpassen| Microsoft Docs
description: Beschrijft hoe u het resourcegebruik of -verbruik kunt vastleggen dat is gekoppeld aan een project, om kosten, prijzen en werksoorten bij te houden en te beheren.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 777de65d2cda454491b6c3ea82ebb99d4839dce4
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5780394"
---
# <a name="use-resources-for-jobs"></a><span data-ttu-id="055e8-103">Resources gebruiken voor projecten</span><span class="sxs-lookup"><span data-stu-id="055e8-103">Use Resources for Jobs</span></span>
<span data-ttu-id="055e8-104">U legt het gebruik van resources vast in het projectdagboek om kosten, prijzen en de werksoorten bij te houden die zijn gekoppeld aan projecten.</span><span class="sxs-lookup"><span data-stu-id="055e8-104">You record the usage of resources in the job journal to keep track of costs, prices, and the work types that are linked to jobs.</span></span> <span data-ttu-id="055e8-105">Zie voor meer informatie [Gebruik vastleggen voor projecten](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="055e8-105">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

> [!NOTE]
> <span data-ttu-id="055e8-106">U kunt ook externe resources aanschaffen, bijvoorbeeld om een leverancier te factureren voor het geleverde werk.</span><span class="sxs-lookup"><span data-stu-id="055e8-106">You can also purchase external resources, for example, to invoice a vendor for work delivered.</span></span> <span data-ttu-id="055e8-107">Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="055e8-107">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

<span data-ttu-id="055e8-108">U kunt ook het verbruik van een resource boeken in een resourcedagboek.</span><span class="sxs-lookup"><span data-stu-id="055e8-108">You can also post the usage of a resource in a resource journal.</span></span> <span data-ttu-id="055e8-109">Posten die in een resourcedagboek zijn geboekt, werken niet door in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="055e8-109">Entries posted in a resource journal have no effect on the general ledger.</span></span>

## <a name="to-assign-resources-to-jobs"></a><span data-ttu-id="055e8-110">Resources toewijzen aan projecten</span><span class="sxs-lookup"><span data-stu-id="055e8-110">To assign resources to jobs</span></span>
<span data-ttu-id="055e8-111">U wijst resources aan projecten toe door projectplanningsregels voor het project te maken.</span><span class="sxs-lookup"><span data-stu-id="055e8-111">You assign resources to jobs by creating job planning lines for the job.</span></span> <span data-ttu-id="055e8-112">Zie voor meer informatie [Projecten maken](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="055e8-112">For more information, see [Create Jobs](projects-how-create-jobs.md).</span></span>

## <a name="to-record-resource-usage-for-a-job"></a><span data-ttu-id="055e8-113">Resourceverbruik voor een project vastleggen</span><span class="sxs-lookup"><span data-stu-id="055e8-113">To record resource usage for a job</span></span>
1. <span data-ttu-id="055e8-114">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projectdagboeken** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="055e8-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="055e8-115">Open een relevante projectdagboekbatch en vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="055e8-115">Open a relevant job journal batch, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="055e8-116">Wanneer het dagboek compleet is, kiest u de actie **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="055e8-116">When the journal is complete, choose the **Post** action.</span></span>

## <a name="to-adjust-resource-prices"></a><span data-ttu-id="055e8-117">Resourceprijzen aanpassen</span><span class="sxs-lookup"><span data-stu-id="055e8-117">To adjust resource prices</span></span>
<span data-ttu-id="055e8-118">Als u kost- of verkoopprijzen wilt wijzigen voor een groot aantal resources, kunt u een batchverwerking gebruiken.</span><span class="sxs-lookup"><span data-stu-id="055e8-118">If you want to change costs or prices for a large number of resources, you can use a batch job.</span></span>  

1. <span data-ttu-id="055e8-119">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Resourceprijzen herwaarderen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="055e8-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Adjust Resource Costs/Prices**, and then choose the related link.</span></span>
2. <span data-ttu-id="055e8-120">Vul de overige velden op een regel desgewenst in en kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="055e8-120">Fill in the fields on a line as necessary, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="055e8-121">Met deze batchverwerking worden geen alternatieve kosten of prijzen voor resources gemaakt of aangepast.</span><span class="sxs-lookup"><span data-stu-id="055e8-121">This batch job does not create or adjust alternate costs or prices for resources.</span></span> <span data-ttu-id="055e8-122">Dit verandert alleen de inhoud van het veld op de resourcekaart voor het veld **Aan te passen prijs** dat u hebt geselecteerd in de batchtaak.</span><span class="sxs-lookup"><span data-stu-id="055e8-122">It only changes the contents of the field on the resource card for the **Adjust Field** field that you selected in the batch job.</span></span> <span data-ttu-id="055e8-123">De aanpassing werkt onmiddellijk door voor de resources. Controleer daarom uw herwaarderingsfactoren zorgvuldig voordat u de batchverwerking uitvoert.</span><span class="sxs-lookup"><span data-stu-id="055e8-123">The adjustment will take effect immediately for resources, so check your adjustment factors before you run the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-existing-alternate-prices"></a><span data-ttu-id="055e8-124">Suggesties voor wijzigingen van resourceprijzen krijgen op basis van bestaande alternatieve prijzen</span><span class="sxs-lookup"><span data-stu-id="055e8-124">To get resource price change suggestions based on existing alternate prices</span></span>
<span data-ttu-id="055e8-125">Als u al alternatieve resourceprijzen hebt ingesteld voor bepaalde resources, kunt u een batchverwerking gebruiken om meerdere alternatieve resourceprijzen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="055e8-125">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="055e8-126">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Resourceprijswijzigingen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="055e8-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="055e8-127">Kies de actie **Res.prijsvoorstellen (Prijs)** en vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="055e8-127">Choose the **Suggest Res. Price Chg. (Price)** action, and then fill in the fields as necessary.</span></span>
3. <span data-ttu-id="055e8-128">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="055e8-128">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="055e8-129">Nadat de batchverwerking is voltooid, bevat de pagina **Resourceprijswijzigingen** de resultaten van de batchverwerking.</span><span class="sxs-lookup"><span data-stu-id="055e8-129">When the batch job is finished, the **Resource Price Changes** page shows the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-standard-prices"></a><span data-ttu-id="055e8-130">Resourceprijsvoorstellen ophalen op basis van standaardverkoopprijzen</span><span class="sxs-lookup"><span data-stu-id="055e8-130">To get resource price change suggestions based on standard prices</span></span>
<span data-ttu-id="055e8-131">Als u meerdere alternatieve resourceprijzen wilt instellen op basis van de standaardverkoopprijzen op de resourcekaarten, kunt u een batchverwerking gebruiken.</span><span class="sxs-lookup"><span data-stu-id="055e8-131">If you want to set up multiple alternate resource prices based on the standard prices on the resource cards, you can use a batch job.</span></span>  

1. <span data-ttu-id="055e8-132">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Resourceprijswijzigingen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="055e8-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Price Changes**, and then choose the related link.</span></span>
2. <span data-ttu-id="055e8-133">Kies de actie **Res.prijsvoorstellen (Res.)** en vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="055e8-133">Choose the **Suggest Res. Price Chg. (Res.)** action, and then fill in the fields as necessary.</span></span>  
3. <span data-ttu-id="055e8-134">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="055e8-134">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="055e8-135">Nadat de batchverwerking is voltooid, opent u de pagina **Resourceprijswijzigingen** om de resultaten van de batchverwerking te bekijken.</span><span class="sxs-lookup"><span data-stu-id="055e8-135">When the batch job is finished, open the **Resource Price Changes** page to see the results of the batch job.</span></span>

## <a name="to-get-resource-price-change-suggestions-based-on-alternate-prices"></a><span data-ttu-id="055e8-136">Suggesties voor wijzigingen van resourceprijzen krijgen op basis van alternatieve prijzen</span><span class="sxs-lookup"><span data-stu-id="055e8-136">To get resource price change suggestions based on alternate prices</span></span>
<span data-ttu-id="055e8-137">Als u al alternatieve resourceprijzen hebt ingesteld voor bepaalde resources, kunt u een batchverwerking gebruiken om meerdere alternatieve resourceprijzen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="055e8-137">If you have already set up alternate resource price for some resources, you can use a batch job to set up multiple alternate resource prices.</span></span>

1. <span data-ttu-id="055e8-138">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Res.prijsvoorstellen (Prijs)** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="055e8-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Suggest Res. Price Chg. (Price)**, and then choose the related link.</span></span>  
2. <span data-ttu-id="055e8-139">Vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="055e8-139">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="055e8-140">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="055e8-140">Choose the **OK** button.</span></span>  
4. <span data-ttu-id="055e8-141">Nadat de batchverwerking is voltooid, opent u de pagina **Resourceprijswijzigingen** om de resultaten van de batchverwerking te bekijken.</span><span class="sxs-lookup"><span data-stu-id="055e8-141">When the batch job is finished, open the **Resource Price Changes** page to see the results of the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="055e8-142">Zie ook</span><span class="sxs-lookup"><span data-stu-id="055e8-142">See Also</span></span>
[<span data-ttu-id="055e8-143">Projectbeheer</span><span class="sxs-lookup"><span data-stu-id="055e8-143">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="055e8-144">Financiën</span><span class="sxs-lookup"><span data-stu-id="055e8-144">Finance</span></span>](finance.md)  
<span data-ttu-id="055e8-145">[Inkoop](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="055e8-145">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="055e8-146">[Verkoop](sales-manage-sales.md)   </span><span class="sxs-lookup"><span data-stu-id="055e8-146">[Sales](sales-manage-sales.md)   </span></span>  
<span data-ttu-id="055e8-147">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="055e8-147">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]