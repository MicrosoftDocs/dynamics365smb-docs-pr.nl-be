---
title: Kostenbudgetten maken | Microsoft Docs
description: In dit onderwerp wordt aangegeven waar u kostenbudgetten kunt maken en analyseren.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 4c50c2b6a81eccfe07d41c2527547b7694aca4e7
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816279"
---
# <a name="creating-cost-budgets"></a><span data-ttu-id="0a38d-103">Kostenbudgetten maken</span><span class="sxs-lookup"><span data-stu-id="0a38d-103">Creating Cost Budgets</span></span>
<span data-ttu-id="0a38d-104">Budgettering in kostprijsboekhouding lijkt op budgettering in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="0a38d-104">Budgeting in cost accounting resembles budgeting in the general ledger.</span></span> <span data-ttu-id="0a38d-105">Een kostenbudget wordt gemaakt op basis van kostensoorten zoals een budget voor het grootboek wordt gemaakt op basis van grootboekrekeningen.</span><span class="sxs-lookup"><span data-stu-id="0a38d-105">A cost budget is created based on cost types just as a budget for the general ledger is created based on general ledger accounts.</span></span>  

<span data-ttu-id="0a38d-106">Een kostenbudget wordt gemaakt voor een bepaalde periode, bijvoorbeeld een boekjaar.</span><span class="sxs-lookup"><span data-stu-id="0a38d-106">A cost budget is created for a certain period of time, for example, a fiscal year.</span></span> <span data-ttu-id="0a38d-107">U kunt zoveel kostenbudgetten instellen als u nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="0a38d-107">You can create as many cost budgets as needed.</span></span> <span data-ttu-id="0a38d-108">U kunt een nieuw kostenbudget handmatig maken, door een kostenbudget te importeren of door een bestaand kostenbudget als basisbudget te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="0a38d-108">You can create a new cost budget manually, or by importing a cost budget, or by copying an existing cost budget as the budget base.</span></span> <span data-ttu-id="0a38d-109">Zie [Grootboekbudgetten maken](finance-how-create-budgets.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="0a38d-109">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

<span data-ttu-id="0a38d-110">U gebruikt de volgende pagina's om kostenbudgetten te maken en te analyseren.</span><span class="sxs-lookup"><span data-stu-id="0a38d-110">You use the following pages to create and analyze cost budgets.</span></span> <span data-ttu-id="0a38d-111">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen") om een pagina te vinden en lees vervolgens de knopinfo voor elke pagina.</span><span class="sxs-lookup"><span data-stu-id="0a38d-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon to find a page, and then read the tooltip for each.</span></span>

|<span data-ttu-id="0a38d-112">Aan</span><span class="sxs-lookup"><span data-stu-id="0a38d-112">To</span></span>|<span data-ttu-id="0a38d-113">Zie</span><span class="sxs-lookup"><span data-stu-id="0a38d-113">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="0a38d-114">Budgetten overboeken vanuit het grootboek</span><span class="sxs-lookup"><span data-stu-id="0a38d-114">Transfer budgets from the general ledger.</span></span>|<span data-ttu-id="0a38d-115">Batchverwerking **Budget kopiëren naar kostprijsboekhouding**</span><span class="sxs-lookup"><span data-stu-id="0a38d-115">**Copy G-L Budget to Cost Acctg.** batch job</span></span>|  
|<span data-ttu-id="0a38d-116">Kostenbegrotingen kopiëren.</span><span class="sxs-lookup"><span data-stu-id="0a38d-116">Copy cost budgets.</span></span>|<span data-ttu-id="0a38d-117">Batchverwerking **Kostenbudget kopiëren**</span><span class="sxs-lookup"><span data-stu-id="0a38d-117">**Copy Cost Budget** batch job</span></span>|  
|<span data-ttu-id="0a38d-118">Begrotingen toewijzen.</span><span class="sxs-lookup"><span data-stu-id="0a38d-118">Allocate budgets.</span></span>|<span data-ttu-id="0a38d-119">Pagina **Kostenverdeling**</span><span class="sxs-lookup"><span data-stu-id="0a38d-119">**Cost Allocation** page</span></span>|  
|<span data-ttu-id="0a38d-120">Zie de kostenbudgetregisters en de kostenbudgetposten.</span><span class="sxs-lookup"><span data-stu-id="0a38d-120">See cost budget registers and cost budget entries.</span></span>|<span data-ttu-id="0a38d-121">Pagina **Kostenbudgetregisters**</span><span class="sxs-lookup"><span data-stu-id="0a38d-121">**Cost Budget Registers** page</span></span>|  
|<span data-ttu-id="0a38d-122">Vergelijkingen tussen kostenbudgetten afdrukken met behulp van diverse rapporten.</span><span class="sxs-lookup"><span data-stu-id="0a38d-122">Print cost budget comparisons using various reports.</span></span>|<span data-ttu-id="0a38d-123">Rapport **Saldo/Budget kostprijsboekhouding**</span><span class="sxs-lookup"><span data-stu-id="0a38d-123">**Cost Acctg. Balance-Budget** report</span></span><br /><br /> <span data-ttu-id="0a38d-124">Rapport **Rekeningoverzicht/Budget kostprijsboekhouding**</span><span class="sxs-lookup"><span data-stu-id="0a38d-124">**Cost Acctg. Statement-Budget** report</span></span><br /><br /> <span data-ttu-id="0a38d-125">Rapport **Kostenbudget per kostenplaats**</span><span class="sxs-lookup"><span data-stu-id="0a38d-125">**Cost Budget by Cost Center** report</span></span><br /><br /> <span data-ttu-id="0a38d-126">Rapport **Kostenbudget per kostenobject**</span><span class="sxs-lookup"><span data-stu-id="0a38d-126">**Cost Budget by Cost Object** report</span></span>|  

## <a name="see-also"></a><span data-ttu-id="0a38d-127">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0a38d-127">See Also</span></span>  
[<span data-ttu-id="0a38d-128">Kosten verantwoorden</span><span class="sxs-lookup"><span data-stu-id="0a38d-128">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
[<span data-ttu-id="0a38d-129">Grootboekbudgetten maken</span><span class="sxs-lookup"><span data-stu-id="0a38d-129">Create G/L Budgets</span></span>](finance-how-create-budgets.md)  
<span data-ttu-id="0a38d-130">[Terminologie in kostprijsboekhouding](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="0a38d-130">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="0a38d-131">Kosten definiëren en toewijzen</span><span class="sxs-lookup"><span data-stu-id="0a38d-131">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)  
<span data-ttu-id="0a38d-132">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0a38d-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
