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
redirect_url: finance-set-up-cost-accounting
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: b3ca863a9f4969046695e0cec16fedf6f5ac7aec
ms.contentlocale: nl-be
ms.lasthandoff: 11/22/2018

---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a><span data-ttu-id="a0871-105">Kostenplaatsen en kostenobjecten voor rekeningschema's definiëren</span><span class="sxs-lookup"><span data-stu-id="a0871-105">Defining Cost Centers and Cost Objects for Chart of Accounts</span></span>
<span data-ttu-id="a0871-106">In het grootboek kunt u de inkomsten- en onkostenposten automatisch overbrengen naar de kostprijsboekhouding, hetzij voor elke grootboekboeking of met behulp van een batchtaak.</span><span class="sxs-lookup"><span data-stu-id="a0871-106">You can automatically transfer the expense and income entries from the general ledger to cost accounting either for each general ledger posting or with a batch job.</span></span> <span data-ttu-id="a0871-107">Wanneer u de overdracht uitvoert, worden door [!INCLUDE[d365fin](includes/d365fin_md.md)] alleen de posten overgebracht die al zijn gekoppeld aan een kostenplaats of een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="a0871-107">When you do the transfer, [!INCLUDE[d365fin](includes/d365fin_md.md)] only transfers the entries that are already linked to a cost center or a cost object.</span></span> <span data-ttu-id="a0871-108">Om tot een zinvolle overdracht te komen, moet u ervoor zorgen dat kostenplaatsen en de kostenobjecten juist zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="a0871-108">To establish a meaningful transfer, you must ensure that the cost centers and cost objects are correctly defined.</span></span>  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a><span data-ttu-id="a0871-109">Standaarddimensiewaarden definiëren voor grootboekrekeningen</span><span class="sxs-lookup"><span data-stu-id="a0871-109">Defining Default Dimension Values for General Ledger Accounts</span></span>  
<span data-ttu-id="a0871-110">Voor elke grootboekrekening definieert u standaarddimensiewaarden in de tabel **Standaarddimensie**.</span><span class="sxs-lookup"><span data-stu-id="a0871-110">For each general ledger account, you can define default dimension values in the **Default Dimension** table.</span></span> <span data-ttu-id="a0871-111">In het volgende voorbeeld ziet u hoe u kunt definiëren dat er altijd een AFDELING als kostenplaats, maar nooit een PROJECT als kostenobject moet voorkomen bij het boeken naar een grootboekrekening.</span><span class="sxs-lookup"><span data-stu-id="a0871-111">The following example shows how to define that there should always be a DEPARTMENT cost center, but never be a PROJECT cost object when posting to a general ledger account.</span></span>  

|<span data-ttu-id="a0871-112">**Dimensiecode**</span><span class="sxs-lookup"><span data-stu-id="a0871-112">**Dimension Code**</span></span>|<span data-ttu-id="a0871-113">**Waardeboeking**</span><span class="sxs-lookup"><span data-stu-id="a0871-113">**Value Posting**</span></span>|  
|------------------------------------------|-----------------------------------------|  
|<span data-ttu-id="a0871-114">Kostenplaats</span><span class="sxs-lookup"><span data-stu-id="a0871-114">Department</span></span>|<span data-ttu-id="a0871-115">Verplicht</span><span class="sxs-lookup"><span data-stu-id="a0871-115">Code Mandatory</span></span>|  
|<span data-ttu-id="a0871-116">Kostendrager</span><span class="sxs-lookup"><span data-stu-id="a0871-116">Project</span></span>|<span data-ttu-id="a0871-117">Geen</span><span class="sxs-lookup"><span data-stu-id="a0871-117">No Code</span></span>|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a><span data-ttu-id="a0871-118">Dimensiewaarden voor overheadkosten en directe kosten definiëren</span><span class="sxs-lookup"><span data-stu-id="a0871-118">Defining Dimension Values for Overhead Costs and Direct Costs</span></span>  
 <span data-ttu-id="a0871-119">Overheadkosten kunt u overbrengen naar een kostenplaats en directe kosten naar een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="a0871-119">You can transfer overhead costs to a cost center and direct costs to a cost object.</span></span> <span data-ttu-id="a0871-120">In de volgende tabel ziet u de optimale combinatie van instelwaarden voor dimensies.</span><span class="sxs-lookup"><span data-stu-id="a0871-120">The following table shows the optimal combination of the dimension setup values.</span></span>  

|<span data-ttu-id="a0871-121">Overbrengen naar</span><span class="sxs-lookup"><span data-stu-id="a0871-121">Transfer To</span></span>|<span data-ttu-id="a0871-122">Kostenplaatsboeking</span><span class="sxs-lookup"><span data-stu-id="a0871-122">Cost Center Posting</span></span>|<span data-ttu-id="a0871-123">Kostenobjectboeking</span><span class="sxs-lookup"><span data-stu-id="a0871-123">Cost Object Posting</span></span>|  
|-----------------|-------------------------|-------------------------|  
|<span data-ttu-id="a0871-124">Kostenplaats</span><span class="sxs-lookup"><span data-stu-id="a0871-124">Cost Center</span></span>|<span data-ttu-id="a0871-125">Verplicht</span><span class="sxs-lookup"><span data-stu-id="a0871-125">Code Mandatory</span></span>|<span data-ttu-id="a0871-126">Geen</span><span class="sxs-lookup"><span data-stu-id="a0871-126">No Code</span></span>|  
|<span data-ttu-id="a0871-127">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="a0871-127">Cost Object</span></span>|<span data-ttu-id="a0871-128">Geen</span><span class="sxs-lookup"><span data-stu-id="a0871-128">No Code</span></span>|<span data-ttu-id="a0871-129">Verplicht</span><span class="sxs-lookup"><span data-stu-id="a0871-129">Code Mandatory</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="a0871-130">Zorg ervoor dat de vooraf gedefinieerde kostenplaats en het vooraf gedefinieerde kostenobject die u in het grootboek hebt ingesteld, automatisch naar de kostprijsboekhouding worden overgedragen, door het selectievakje **GB-boekingen controleren** op de pagina Instelling kostprijsboekhouding te selecteren.</span><span class="sxs-lookup"><span data-stu-id="a0871-130">To make sure that the predefined cost center and cost object that you set up in the general ledger are automatically carried over to cost accounting, select the **Check G/L Postings** check box in the Cost Accounting Setup page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a0871-131">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a0871-131">See Also</span></span>  
[<span data-ttu-id="a0871-132">Kosten verantwoorden</span><span class="sxs-lookup"><span data-stu-id="a0871-132">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
[<span data-ttu-id="a0871-133">Kostenboekhouding instellen</span><span class="sxs-lookup"><span data-stu-id="a0871-133">Setting Up Cost Accounting</span></span>](finance-set-up-cost-accounting.md)  
<span data-ttu-id="a0871-134">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a0871-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

