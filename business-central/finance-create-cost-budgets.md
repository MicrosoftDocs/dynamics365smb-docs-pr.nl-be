---
title: Kostenbudgetten maken | Microsoft Docs
description: In dit onderwerp wordt aangegeven waar u kostenbudgetten kunt maken en analyseren.
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
ms.openlocfilehash: a107203cf81b149b920944db1fabace6e434221a
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="creating-cost-budgets"></a><span data-ttu-id="5a0d4-103">Kostenbudgetten maken</span><span class="sxs-lookup"><span data-stu-id="5a0d4-103">Creating Cost Budgets</span></span>
<span data-ttu-id="5a0d4-104">Budgettering in kostprijsboekhouding lijkt op budgettering in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="5a0d4-104">Budgeting in cost accounting resembles budgeting in the general ledger.</span></span> <span data-ttu-id="5a0d4-105">Een kostenbudget wordt gemaakt op basis van kostensoorten zoals een budget voor het grootboek wordt gemaakt op basis van grootboekrekeningen.</span><span class="sxs-lookup"><span data-stu-id="5a0d4-105">A cost budget is created based on cost types just as a budget for the general ledger is created based on general ledger accounts.</span></span>  

<span data-ttu-id="5a0d4-106">Een kostenbudget wordt gemaakt voor een bepaalde periode, bijvoorbeeld een boekjaar.</span><span class="sxs-lookup"><span data-stu-id="5a0d4-106">A cost budget is created for a certain period of time, for example, a fiscal year.</span></span> <span data-ttu-id="5a0d4-107">U kunt zoveel kostenbudgetten instellen als u nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="5a0d4-107">You can create as many cost budgets as needed.</span></span> <span data-ttu-id="5a0d4-108">U kunt een nieuw kostenbudget handmatig maken, door een kostenbudget te importeren of door een bestaand kostenbudget als basisbudget te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="5a0d4-108">You can create a new cost budget manually, or by importing a cost budget, or by copying an existing cost budget as the budget base.</span></span> <span data-ttu-id="5a0d4-109">Zie [Grootboekbudgetten maken](finance-how-create-budgets.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="5a0d4-109">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

<span data-ttu-id="5a0d4-110">U gebruikt de volgende vensters om kostenbudgetten te maken en te analyseren.</span><span class="sxs-lookup"><span data-stu-id="5a0d4-110">You use the following windows to create and analyze cost budgets.</span></span> <span data-ttu-id="5a0d4-111">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen") om een venster te vinden en lees vervolgens de knopinfo voor elk venster.</span><span class="sxs-lookup"><span data-stu-id="5a0d4-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon to find a window, and then read the tooltip for each.</span></span>

|<span data-ttu-id="5a0d4-112">Aan</span><span class="sxs-lookup"><span data-stu-id="5a0d4-112">To</span></span>|<span data-ttu-id="5a0d4-113">Zie</span><span class="sxs-lookup"><span data-stu-id="5a0d4-113">See</span></span>|  
|--------|---------|  
|<span data-ttu-id="5a0d4-114">Budgetten overboeken vanuit het grootboek</span><span class="sxs-lookup"><span data-stu-id="5a0d4-114">Transfer budgets from the general ledger.</span></span>|<span data-ttu-id="5a0d4-115">Batchverwerking **Budget kopiëren naar kostprijsboekhouding**</span><span class="sxs-lookup"><span data-stu-id="5a0d4-115">**Copy G-L Budget to Cost Acctg.** batch job</span></span>|  
|<span data-ttu-id="5a0d4-116">Kostenbegrotingen kopiëren.</span><span class="sxs-lookup"><span data-stu-id="5a0d4-116">Copy cost budgets.</span></span>|<span data-ttu-id="5a0d4-117">Batchverwerking **Kostenbudget kopiëren**</span><span class="sxs-lookup"><span data-stu-id="5a0d4-117">**Copy Cost Budget** batch job</span></span>|  
|<span data-ttu-id="5a0d4-118">Begrotingen toewijzen.</span><span class="sxs-lookup"><span data-stu-id="5a0d4-118">Allocate budgets.</span></span>|<span data-ttu-id="5a0d4-119">Venster **Kostenverdeling**</span><span class="sxs-lookup"><span data-stu-id="5a0d4-119">**Cost Allocation** window</span></span>|  
|<span data-ttu-id="5a0d4-120">Zie de kostenbudgetregisters en de kostenbudgetposten.</span><span class="sxs-lookup"><span data-stu-id="5a0d4-120">See cost budget registers and cost budget entries.</span></span>|<span data-ttu-id="5a0d4-121">Venster **Kostenbudgetregisters**</span><span class="sxs-lookup"><span data-stu-id="5a0d4-121">**Cost Budget Registers** window</span></span>|  
|<span data-ttu-id="5a0d4-122">Vergelijkingen tussen kostenbudgetten afdrukken met behulp van diverse rapporten.</span><span class="sxs-lookup"><span data-stu-id="5a0d4-122">Print cost budget comparisons using various reports.</span></span>|<span data-ttu-id="5a0d4-123">Rapport **Saldo/Budget kostprijsboekhouding**</span><span class="sxs-lookup"><span data-stu-id="5a0d4-123">**Cost Acctg. Balance-Budget** report</span></span><br /><br /> <span data-ttu-id="5a0d4-124">Rapport **Rekeningoverzicht/Budget kostprijsboekhouding**</span><span class="sxs-lookup"><span data-stu-id="5a0d4-124">**Cost Acctg. Statement-Budget** report</span></span><br /><br /> <span data-ttu-id="5a0d4-125">Rapport **Kostenbudget per kostenplaats**</span><span class="sxs-lookup"><span data-stu-id="5a0d4-125">**Cost Budget by Cost Center** report</span></span><br /><br /> <span data-ttu-id="5a0d4-126">Rapport **Kostenbudget per kostenobject**</span><span class="sxs-lookup"><span data-stu-id="5a0d4-126">**Cost Budget by Cost Object** report</span></span>|  

## <a name="see-also"></a><span data-ttu-id="5a0d4-127">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5a0d4-127">See Also</span></span>  
[<span data-ttu-id="5a0d4-128">Kosten verantwoorden</span><span class="sxs-lookup"><span data-stu-id="5a0d4-128">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
[<span data-ttu-id="5a0d4-129">Grootboekbudgetten maken</span><span class="sxs-lookup"><span data-stu-id="5a0d4-129">Create G/L Budgets</span></span>](finance-how-create-budgets.md)  
<span data-ttu-id="5a0d4-130">[Terminologie in kostprijsboekhouding](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="5a0d4-130">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="5a0d4-131">Kosten definiëren en toewijzen</span><span class="sxs-lookup"><span data-stu-id="5a0d4-131">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)  
<span data-ttu-id="5a0d4-132">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5a0d4-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

