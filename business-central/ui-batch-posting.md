---
title: Hoe u meerdere documenten tegelijkertijd boekt | Microsoft Docs
description: In plaats van afzonderlijke documenten een voor een te boeken kunt u meerdere niet-geboekte documenten in een lijst selecteren voor batchboeking, hetzij voor onmiddellijke boeking, hetzij gepland voor bijvoorbeeld het einde van de dag.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1fd25f8b07a359414f62ef4757162f8a73889c27
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912733"
---
# <a name="post-multiple-documents-at-the-same-time"></a><span data-ttu-id="e573a-103">Meerdere documenten tegelijkertijd boeken</span><span class="sxs-lookup"><span data-stu-id="e573a-103">Post Multiple Documents at the Same Time</span></span>

<span data-ttu-id="e573a-104">In plaats van afzonderlijke documenten een voor een te boeken kunt u meerdere niet-geboekte documenten in een lijst selecteren voor directe batchboeking of voor batchboeking volgens een planning, bijvoorbeeld aan het einde van de dag.</span><span class="sxs-lookup"><span data-stu-id="e573a-104">Instead of posting individual documents one by one, you can select multiple non-posted documents in a list for immediate posting or for batch posting according to a schedule, such as at the end of the day.</span></span> <span data-ttu-id="e573a-105">Dit kan handig zijn als alleen een supervisor documenten kan boeken die door andere gebruikers zijn gemaakt of om problemen met de systeemprestaties te voorkomen door boeking tijdens werkuren.</span><span class="sxs-lookup"><span data-stu-id="e573a-105">This may be useful if only a supervisor can post documents created by other users or to avoid system performance issues from posting during work hours.</span></span>

## <a name="to-post-multiple-purchase-orders-immediately"></a><span data-ttu-id="e573a-106">Meerdere inkooporders onmiddellijk boeken</span><span class="sxs-lookup"><span data-stu-id="e573a-106">To post multiple purchase orders immediately</span></span>

<span data-ttu-id="e573a-107">In de volgende procedure wordt uitgelegd hoe u meerdere inkooporders onmiddellijk kunt boeken.</span><span class="sxs-lookup"><span data-stu-id="e573a-107">The following procedure explains how to post multiple purchase orders immediately.</span></span> <span data-ttu-id="e573a-108">De stappen zijn vergelijkbaar voor alle inkoop- en verkoopdocumenten.</span><span class="sxs-lookup"><span data-stu-id="e573a-108">The steps are similar for all purchase and sales documents.</span></span>

1. <span data-ttu-id="e573a-109">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="e573a-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders** , and then choose the related link.</span></span>
2. <span data-ttu-id="e573a-110">Ga op de pagina **Inkooporders** door met het selecteren van alle te boeken orders:</span><span class="sxs-lookup"><span data-stu-id="e573a-110">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="e573a-111">Voer in het veld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="e573a-111">In the **No.**</span></span> <span data-ttu-id="e573a-112">de drie verticale stippen om het contextmenu te openen en kies vervolgens de actie **Meer selecteren** .</span><span class="sxs-lookup"><span data-stu-id="e573a-112">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="e573a-113">Schakel het selectievakje in voor alle regels die orders vertegenwoordigen die u tegelijkertijd wilt boeken.</span><span class="sxs-lookup"><span data-stu-id="e573a-113">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="e573a-114">Kies de actie **Boeken** en kies vervolgens weer de actie **Boeken** .</span><span class="sxs-lookup"><span data-stu-id="e573a-114">Choose the **Posting** action, and then choose the **Post** action.</span></span>
6. <span data-ttu-id="e573a-115">Kies de knop **Ja** in het bevestigingsbericht.</span><span class="sxs-lookup"><span data-stu-id="e573a-115">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-batch-post-multiple-purchase-orders"></a><span data-ttu-id="e573a-116">Meerdere inkooporders in een batch boeken</span><span class="sxs-lookup"><span data-stu-id="e573a-116">To batch post multiple purchase orders</span></span>

<span data-ttu-id="e573a-117">In de volgende procedure wordt uitgelegd hoe u inkooporders in een batch boekt.</span><span class="sxs-lookup"><span data-stu-id="e573a-117">The following procedure explains how to batch post purchase orders.</span></span> <span data-ttu-id="e573a-118">De stappen zijn vergelijkbaar voor alle inkoop- en verkoopdocumenten waarbij de actie **Batchboeken** beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="e573a-118">The steps are similar for all purchase and sales documents where the **Batch Post** action is available.</span></span>

> [!NOTE]
> <span data-ttu-id="e573a-119">Het batchboeken van documenten gebeurt op de achtergrond.</span><span class="sxs-lookup"><span data-stu-id="e573a-119">Batch posting of documents happens in the background.</span></span> <span data-ttu-id="e573a-120">[!INCLUDE [prodshort](includes/prodshort.md)] online bevat standaardtaken voor boeken op de achtergrond en boeken in batches.</span><span class="sxs-lookup"><span data-stu-id="e573a-120">[!INCLUDE [prodshort](includes/prodshort.md)] online includes default jobs for background posting and batch posting.</span></span> <span data-ttu-id="e573a-121">Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="e573a-121">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

1. <span data-ttu-id="e573a-122">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="e573a-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders** , and then choose the related link.</span></span>  
2. <span data-ttu-id="e573a-123">Ga op de pagina **Inkooporders** door met het selecteren van alle te boeken orders:</span><span class="sxs-lookup"><span data-stu-id="e573a-123">On the **Purchase Orders** page, proceed to select all orders to be posted:</span></span>
3. <span data-ttu-id="e573a-124">Voer in het veld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="e573a-124">In the **No.**</span></span> <span data-ttu-id="e573a-125">de drie verticale stippen om het contextmenu te openen en kies vervolgens de actie **Meer selecteren** .</span><span class="sxs-lookup"><span data-stu-id="e573a-125">field, choose the three vertical dots to open the context menu, and then choose the **Select More** action.</span></span>
4. <span data-ttu-id="e573a-126">Schakel het selectievakje in voor alle regels die orders vertegenwoordigen die u tegelijkertijd wilt boeken.</span><span class="sxs-lookup"><span data-stu-id="e573a-126">Select the check box for all the lines representing orders that you want to post at the same time.</span></span>
5. <span data-ttu-id="e573a-127">Kies de actie **Boeken** en kies vervolgens de actie **Batchboeken** .</span><span class="sxs-lookup"><span data-stu-id="e573a-127">Choose the **Posting** action, and then choose the **Post Batch** action.</span></span>
6. <span data-ttu-id="e573a-128">Vul desgewenst de velden op de pagina **Batchboeken inkooporders** in.</span><span class="sxs-lookup"><span data-stu-id="e573a-128">On the **Batch Post Purchase Order** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. <span data-ttu-id="e573a-129">Kies de knop **Ok** .</span><span class="sxs-lookup"><span data-stu-id="e573a-129">Choose the **OK** button.</span></span>
8. <span data-ttu-id="e573a-130">Als u mogelijke problemen wilt zien die zijn opgetreden tijdens het batchboeken van documenten, opent u de pagina **Foutberichtregister** .</span><span class="sxs-lookup"><span data-stu-id="e573a-130">To view potential issues that occurred during batch posting of documents, open the **Error Message Register** page.</span></span>

<span data-ttu-id="e573a-131">De inkooporders worden nu toegevoegd aan een speciale taakwachtrijpost, die bepaalt wanneer de documenten worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="e573a-131">The purchase orders will now be added to a dedicated job queue entry, which defines when the documents are posted.</span></span> <span data-ttu-id="e573a-132">Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="e573a-132">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

<span data-ttu-id="e573a-133">Als u **PDF** selecteert in het veld **Soort rapportuitvoer** , zijn succesvol geboekte inkooporders beschikbaar in het onderdeel **Rapportinbox** in uw rolcentrum.</span><span class="sxs-lookup"><span data-stu-id="e573a-133">If you select **PDF** in the **Report Output Type** field, successfully posted purchase orders will be available in the **Report Inbox** part on your Role Center.</span></span>

## <a name="see-also"></a><span data-ttu-id="e573a-134">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e573a-134">See Also</span></span>

[<span data-ttu-id="e573a-135">Documenten en dagboeken boeken</span><span class="sxs-lookup"><span data-stu-id="e573a-135">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
[<span data-ttu-id="e573a-136">Taakwachtrijen gebruiken om taken te plannen</span><span class="sxs-lookup"><span data-stu-id="e573a-136">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
[<span data-ttu-id="e573a-137">Geboekte documenten bewerken</span><span class="sxs-lookup"><span data-stu-id="e573a-137">Edit Posted Documents</span></span>](across-edit-posted-document.md)  
[<span data-ttu-id="e573a-138">Niet-betaalde inkoopfacturen corrigeren of annuleren</span><span class="sxs-lookup"><span data-stu-id="e573a-138">Correct or Cancel Unpaid Purchase Invoices</span></span>](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[<span data-ttu-id="e573a-139">Pagina's en informatie zoeken met Vertel me</span><span class="sxs-lookup"><span data-stu-id="e573a-139">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="e573a-140">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e573a-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
