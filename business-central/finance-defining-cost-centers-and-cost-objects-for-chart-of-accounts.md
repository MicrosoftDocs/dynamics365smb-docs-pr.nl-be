---
title: "Kostenplaatsen en kostenobjecten voor rekeningschema's definiëren | Microsoft Docs"
description: In het grootboek kunt u de inkomsten- en onkostenposten automatisch overbrengen naar de kostprijsboekhouding, hetzij voor elke grootboekboeking of met behulp van een batchtaak. Wanneer u de overdracht uitvoert, worden alleen de posten overgebracht die al zijn gekoppeld aan een kostenplaats of een kostenobject. Om tot een zinvolle overdracht te komen, moet u ervoor zorgen dat kostenplaatsen en de kostenobjecten juist zijn gedefinieerd.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8bbfcad34b0b717d961ccd2ebe3eb095aaef1335
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a><span data-ttu-id="0f1c3-105">Kostenplaatsen en kostenobjecten voor rekeningschema's definiëren</span><span class="sxs-lookup"><span data-stu-id="0f1c3-105">Defining Cost Centers and Cost Objects for Chart of Accounts</span></span>
<span data-ttu-id="0f1c3-106">In het grootboek kunt u de inkomsten- en onkostenposten automatisch overbrengen naar de kostprijsboekhouding, hetzij voor elke grootboekboeking of met behulp van een batchtaak.</span><span class="sxs-lookup"><span data-stu-id="0f1c3-106">You can automatically transfer the expense and income entries from the general ledger to cost accounting either for each general ledger posting or with a batch job.</span></span> <span data-ttu-id="0f1c3-107">Wanneer u de overdracht uitvoert, worden door [!INCLUDE[d365fin](includes/d365fin_md.md)] alleen de posten overgebracht die al zijn gekoppeld aan een kostenplaats of een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="0f1c3-107">When you do the transfer, [!INCLUDE[d365fin](includes/d365fin_md.md)] only transfers the entries that are already linked to a cost center or a cost object.</span></span> <span data-ttu-id="0f1c3-108">Om tot een zinvolle overdracht te komen, moet u ervoor zorgen dat kostenplaatsen en de kostenobjecten juist zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="0f1c3-108">To establish a meaningful transfer, you must ensure that the cost centers and cost objects are correctly defined.</span></span>  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a><span data-ttu-id="0f1c3-109">Standaarddimensiewaarden definiëren voor grootboekrekeningen</span><span class="sxs-lookup"><span data-stu-id="0f1c3-109">Defining Default Dimension Values for General Ledger Accounts</span></span>  
<span data-ttu-id="0f1c3-110">Voor elke grootboekrekening definieert u standaarddimensiewaarden in de tabel **Standaarddimensie**.</span><span class="sxs-lookup"><span data-stu-id="0f1c3-110">For each general ledger account, you can define default dimension values in the **Default Dimension** table.</span></span> <span data-ttu-id="0f1c3-111">In het volgende voorbeeld ziet u hoe u kunt definiëren dat er altijd een AFDELING als kostenplaats, maar nooit een PROJECT als kostenobject moet voorkomen bij het boeken naar een grootboekrekening.</span><span class="sxs-lookup"><span data-stu-id="0f1c3-111">The following example shows how to define that there should always be a DEPARTMENT cost center, but never be a PROJECT cost object when posting to a general ledger account.</span></span>  

|<span data-ttu-id="0f1c3-112">**Dimensiecode**</span><span class="sxs-lookup"><span data-stu-id="0f1c3-112">**Dimension Code**</span></span>|<span data-ttu-id="0f1c3-113">**Waardeboeking**</span><span class="sxs-lookup"><span data-stu-id="0f1c3-113">**Value Posting**</span></span>|  
|------------------------------------------|-----------------------------------------|  
|<span data-ttu-id="0f1c3-114">Kostenplaats</span><span class="sxs-lookup"><span data-stu-id="0f1c3-114">Department</span></span>|<span data-ttu-id="0f1c3-115">Verplicht</span><span class="sxs-lookup"><span data-stu-id="0f1c3-115">Code Mandatory</span></span>|  
|<span data-ttu-id="0f1c3-116">Kostendrager</span><span class="sxs-lookup"><span data-stu-id="0f1c3-116">Project</span></span>|<span data-ttu-id="0f1c3-117">Geen</span><span class="sxs-lookup"><span data-stu-id="0f1c3-117">No Code</span></span>|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a><span data-ttu-id="0f1c3-118">Dimensiewaarden voor overheadkosten en directe kosten definiëren</span><span class="sxs-lookup"><span data-stu-id="0f1c3-118">Defining Dimension Values for Overhead Costs and Direct Costs</span></span>  
 <span data-ttu-id="0f1c3-119">Overheadkosten kunt u overbrengen naar een kostenplaats en directe kosten naar een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="0f1c3-119">You can transfer overhead costs to a cost center and direct costs to a cost object.</span></span> <span data-ttu-id="0f1c3-120">In de volgende tabel ziet u de optimale combinatie van instelwaarden voor dimensies.</span><span class="sxs-lookup"><span data-stu-id="0f1c3-120">The following table shows the optimal combination of the dimension setup values.</span></span>  

|<span data-ttu-id="0f1c3-121">Overbrengen naar</span><span class="sxs-lookup"><span data-stu-id="0f1c3-121">Transfer To</span></span>|<span data-ttu-id="0f1c3-122">Kostenplaatsboeking</span><span class="sxs-lookup"><span data-stu-id="0f1c3-122">Cost Center Posting</span></span>|<span data-ttu-id="0f1c3-123">Kostenobjectboeking</span><span class="sxs-lookup"><span data-stu-id="0f1c3-123">Cost Object Posting</span></span>|  
|-----------------|-------------------------|-------------------------|  
|<span data-ttu-id="0f1c3-124">Kostenplaats</span><span class="sxs-lookup"><span data-stu-id="0f1c3-124">Cost Center</span></span>|<span data-ttu-id="0f1c3-125">Verplicht</span><span class="sxs-lookup"><span data-stu-id="0f1c3-125">Code Mandatory</span></span>|<span data-ttu-id="0f1c3-126">Geen</span><span class="sxs-lookup"><span data-stu-id="0f1c3-126">No Code</span></span>|  
|<span data-ttu-id="0f1c3-127">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="0f1c3-127">Cost Object</span></span>|<span data-ttu-id="0f1c3-128">Geen</span><span class="sxs-lookup"><span data-stu-id="0f1c3-128">No Code</span></span>|<span data-ttu-id="0f1c3-129">Verplicht</span><span class="sxs-lookup"><span data-stu-id="0f1c3-129">Code Mandatory</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="0f1c3-130">Zorg ervoor dat de vooraf gedefinieerde kostenplaats en het vooraf gedefinieerde kostenobject die u in het grootboek hebt ingesteld, automatisch naar de kostprijsboekhouding worden overgedragen, door het selectievakje **GB-boekingen controleren** in het venster Instelling kostprijsboekhouding te selecteren.</span><span class="sxs-lookup"><span data-stu-id="0f1c3-130">To make sure that the predefined cost center and cost object that you set up in the general ledger are automatically carried over to cost accounting, select the **Check G/L Postings** check box in the Cost Accounting Setup window.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0f1c3-131">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0f1c3-131">See Also</span></span>  
[<span data-ttu-id="0f1c3-132">Kosten verantwoorden</span><span class="sxs-lookup"><span data-stu-id="0f1c3-132">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="0f1c3-133">[Kostenplaatsen instellen](finance-how-to-set-up-cost-centers.md) </span><span class="sxs-lookup"><span data-stu-id="0f1c3-133">[Set Up Cost Centers](finance-how-to-set-up-cost-centers.md) </span></span>  
[<span data-ttu-id="0f1c3-134">Kostenobjecten instellen</span><span class="sxs-lookup"><span data-stu-id="0f1c3-134">Set Up Cost Objects</span></span>](finance-how-to-set-up-cost-objects.md)  
<span data-ttu-id="0f1c3-135">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0f1c3-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

