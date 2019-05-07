---
title: Kostenplaatsen en kostenobjecten voor rekeningschema's definiëren | Microsoft Docs
description: In het grootboek kunt u de inkomsten- en onkostenposten automatisch overbrengen naar de kostprijsboekhouding, hetzij voor elke grootboekboeking of met behulp van een batchtaak. Wanneer u de overdracht uitvoert, worden alleen de posten overgebracht die al zijn gekoppeld aan een kostenplaats of een kostenobject. Om tot een zinvolle overdracht te komen, moet u ervoor zorgen dat kostenplaatsen en de kostenobjecten juist zijn gedefinieerd.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 00c0ac4a37476c2ab21ddc850e80e7abeb5eda18
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "923334"
---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a><span data-ttu-id="61624-105">Kostenplaatsen en kostenobjecten voor rekeningschema's definiëren</span><span class="sxs-lookup"><span data-stu-id="61624-105">Defining Cost Centers and Cost Objects for Chart of Accounts</span></span>
<span data-ttu-id="61624-106">In het grootboek kunt u de inkomsten- en onkostenposten automatisch overbrengen naar de kostprijsboekhouding, hetzij voor elke grootboekboeking of met behulp van een batchtaak.</span><span class="sxs-lookup"><span data-stu-id="61624-106">You can automatically transfer the expense and income entries from the general ledger to cost accounting either for each general ledger posting or with a batch job.</span></span> <span data-ttu-id="61624-107">Wanneer u de overdracht uitvoert, worden door [!INCLUDE[d365fin](includes/d365fin_md.md)] alleen de posten overgebracht die al zijn gekoppeld aan een kostenplaats of een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="61624-107">When you do the transfer, [!INCLUDE[d365fin](includes/d365fin_md.md)] only transfers the entries that are already linked to a cost center or a cost object.</span></span> <span data-ttu-id="61624-108">Om tot een zinvolle overdracht te komen, moet u ervoor zorgen dat kostenplaatsen en de kostenobjecten juist zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="61624-108">To establish a meaningful transfer, you must ensure that the cost centers and cost objects are correctly defined.</span></span>  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a><span data-ttu-id="61624-109">Standaarddimensiewaarden definiëren voor grootboekrekeningen</span><span class="sxs-lookup"><span data-stu-id="61624-109">Defining Default Dimension Values for General Ledger Accounts</span></span>  
<span data-ttu-id="61624-110">Voor elke grootboekrekening definieert u standaarddimensiewaarden in de tabel **Standaarddimensie**.</span><span class="sxs-lookup"><span data-stu-id="61624-110">For each general ledger account, you can define default dimension values in the **Default Dimension** table.</span></span> <span data-ttu-id="61624-111">In het volgende voorbeeld ziet u hoe u kunt definiëren dat er altijd een AFDELING als kostenplaats, maar nooit een PROJECT als kostenobject moet voorkomen bij het boeken naar een grootboekrekening.</span><span class="sxs-lookup"><span data-stu-id="61624-111">The following example shows how to define that there should always be a DEPARTMENT cost center, but never be a PROJECT cost object when posting to a general ledger account.</span></span>  

|<span data-ttu-id="61624-112">**Dimensiecode**</span><span class="sxs-lookup"><span data-stu-id="61624-112">**Dimension Code**</span></span>|<span data-ttu-id="61624-113">**Waardeboeking**</span><span class="sxs-lookup"><span data-stu-id="61624-113">**Value Posting**</span></span>|  
|------------------------------------------|-----------------------------------------|  
|<span data-ttu-id="61624-114">Kostenplaats</span><span class="sxs-lookup"><span data-stu-id="61624-114">Department</span></span>|<span data-ttu-id="61624-115">Verplicht</span><span class="sxs-lookup"><span data-stu-id="61624-115">Code Mandatory</span></span>|  
|<span data-ttu-id="61624-116">Kostendrager</span><span class="sxs-lookup"><span data-stu-id="61624-116">Project</span></span>|<span data-ttu-id="61624-117">Geen</span><span class="sxs-lookup"><span data-stu-id="61624-117">No Code</span></span>|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a><span data-ttu-id="61624-118">Dimensiewaarden voor overheadkosten en directe kosten definiëren</span><span class="sxs-lookup"><span data-stu-id="61624-118">Defining Dimension Values for Overhead Costs and Direct Costs</span></span>  
 <span data-ttu-id="61624-119">Overheadkosten kunt u overbrengen naar een kostenplaats en directe kosten naar een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="61624-119">You can transfer overhead costs to a cost center and direct costs to a cost object.</span></span> <span data-ttu-id="61624-120">In de volgende tabel ziet u de optimale combinatie van instelwaarden voor dimensies.</span><span class="sxs-lookup"><span data-stu-id="61624-120">The following table shows the optimal combination of the dimension setup values.</span></span>  

|<span data-ttu-id="61624-121">Overbrengen naar</span><span class="sxs-lookup"><span data-stu-id="61624-121">Transfer To</span></span>|<span data-ttu-id="61624-122">Kostenplaatsboeking</span><span class="sxs-lookup"><span data-stu-id="61624-122">Cost Center Posting</span></span>|<span data-ttu-id="61624-123">Kostenobjectboeking</span><span class="sxs-lookup"><span data-stu-id="61624-123">Cost Object Posting</span></span>|  
|-----------------|-------------------------|-------------------------|  
|<span data-ttu-id="61624-124">Kostenplaats</span><span class="sxs-lookup"><span data-stu-id="61624-124">Cost Center</span></span>|<span data-ttu-id="61624-125">Verplicht</span><span class="sxs-lookup"><span data-stu-id="61624-125">Code Mandatory</span></span>|<span data-ttu-id="61624-126">Geen</span><span class="sxs-lookup"><span data-stu-id="61624-126">No Code</span></span>|  
|<span data-ttu-id="61624-127">Kostenobject</span><span class="sxs-lookup"><span data-stu-id="61624-127">Cost Object</span></span>|<span data-ttu-id="61624-128">Geen</span><span class="sxs-lookup"><span data-stu-id="61624-128">No Code</span></span>|<span data-ttu-id="61624-129">Verplicht</span><span class="sxs-lookup"><span data-stu-id="61624-129">Code Mandatory</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="61624-130">Zorg ervoor dat de vooraf gedefinieerde kostenplaats en het vooraf gedefinieerde kostenobject die u in het grootboek hebt ingesteld, automatisch naar de kostprijsboekhouding worden overgedragen, door het selectievakje **GB-boekingen controleren** op de pagina Instelling kostprijsboekhouding te selecteren.</span><span class="sxs-lookup"><span data-stu-id="61624-130">To make sure that the predefined cost center and cost object that you set up in the general ledger are automatically carried over to cost accounting, select the **Check G/L Postings** check box in the Cost Accounting Setup page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="61624-131">Zie ook</span><span class="sxs-lookup"><span data-stu-id="61624-131">See Also</span></span>  
[<span data-ttu-id="61624-132">Kosten verantwoorden</span><span class="sxs-lookup"><span data-stu-id="61624-132">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
[<span data-ttu-id="61624-133">Kostenboekhouding instellen</span><span class="sxs-lookup"><span data-stu-id="61624-133">Setting Up Cost Accounting</span></span>](finance-set-up-cost-accounting.md)  
<span data-ttu-id="61624-134">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="61624-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
