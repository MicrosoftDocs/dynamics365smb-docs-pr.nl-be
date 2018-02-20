---
title: Grootboekbudgetten maken | Microsoft Docs
description: "Hier wordt beschreven hoe u grootboekbudgetten maakt om verschillende financiële activiteiten te prognosticeren en dimensies toewijst voor bedrijfsinformatiedoeleinden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f6969d05cfde9ba7ce5767a961d4af1c7b3bd983
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="create-gl-budgets"></a><span data-ttu-id="0ea24-103">Grootboekbudgetten maken</span><span class="sxs-lookup"><span data-stu-id="0ea24-103">Create G/L Budgets</span></span>
<span data-ttu-id="0ea24-104">U kunt budgetten met aparte namen maken als u meerdere budgetten wilt gebruiken voor dezelfde perioden.</span><span class="sxs-lookup"><span data-stu-id="0ea24-104">You can have multiple budgets for identical time periods by creating budgets with separate names.</span></span> <span data-ttu-id="0ea24-105">Eerst stelt u de begrotingsnaam in en voert u de begrotingscijfers in.</span><span class="sxs-lookup"><span data-stu-id="0ea24-105">First, you set up the budget name and enter the budget figures.</span></span> <span data-ttu-id="0ea24-106">De begrotingsnaam wordt vervolgens opgenomen op alle begrotingsposten die u maakt.</span><span class="sxs-lookup"><span data-stu-id="0ea24-106">The budget name is then included on all the budget entries you create.</span></span>  

 <span data-ttu-id="0ea24-107">Wanneer u een budget maakt, kunt u vier dimensies voor elk budget opgeven.</span><span class="sxs-lookup"><span data-stu-id="0ea24-107">When you create a budget, you can define four dimensions for each budget.</span></span> <span data-ttu-id="0ea24-108">Deze budgetspecifieke dimensies worden budgetdimensies genoemd.</span><span class="sxs-lookup"><span data-stu-id="0ea24-108">These budget-specific dimensions are called budget dimensions.</span></span> <span data-ttu-id="0ea24-109">U selecteert de budgetdimensies voor elk budget uit de ingestelde dimensies.</span><span class="sxs-lookup"><span data-stu-id="0ea24-109">You select the budget dimensions for each budget from among the dimensions you have already set up.</span></span> <span data-ttu-id="0ea24-110">Met budgetdimensies kunnen budgetfilters worden ingesteld en dimensiegegevens aan budgetposten worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="0ea24-110">Budget dimensions can be used to set filters on a budget and to add dimension information to budget entries.</span></span> <span data-ttu-id="0ea24-111">Zie voor meer informatie [Werken met dimensies](finance-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="0ea24-111">For more information, see [Working with Dimensions](finance-dimensions.md).</span></span>

 <span data-ttu-id="0ea24-112">Budgetten spelen een belangrijke rol in bedrijfsinformatie, zoals in financiële overzichten gebaseerd op rapportageschema's die budgetposten bevatten, of wanneer gebudgetteerde en werkelijke bedragen in het rekeningschema worden geanalyseerd.</span><span class="sxs-lookup"><span data-stu-id="0ea24-112">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="0ea24-113">Zie voor meer informatie [Bedrijfsinformatie](bi.md).</span><span class="sxs-lookup"><span data-stu-id="0ea24-113">For more information, see [Business Intelligence](bi.md).</span></span>

 <span data-ttu-id="0ea24-114">Budgetten spelen een belangrijke rol in bedrijfsinformatie, zoals in financiële overzichten gebaseerd op rapportageschema's die budgetposten bevatten, of wanneer gebudgetteerde en werkelijke bedragen in het rekeningschema worden geanalyseerd.</span><span class="sxs-lookup"><span data-stu-id="0ea24-114">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="0ea24-115">Zie voor meer informatie [Bedrijfsinformatie](bi.md).</span><span class="sxs-lookup"><span data-stu-id="0ea24-115">For more information, see [Business Intelligence](bi.md).</span></span>

<span data-ttu-id="0ea24-116">In kostenadministratie werkt u met kostenbudgetten op een soortgelijke manier.</span><span class="sxs-lookup"><span data-stu-id="0ea24-116">In cost accounting, you work with cost budgets in a similar way.</span></span> <span data-ttu-id="0ea24-117">Zie [Procedure: Kostenbudgetten maken](finance-create-cost-budgets.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="0ea24-117">For more information, see [Creating Cost Budgets](finance-create-cost-budgets.md).</span></span>    

## <a name="to-create-a-new-gl-budget"></a><span data-ttu-id="0ea24-118">Een nieuw grootboekbudget maken</span><span class="sxs-lookup"><span data-stu-id="0ea24-118">To create a new G/L budget</span></span>  
1. <span data-ttu-id="0ea24-119">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Grootboekbudgetten** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="0ea24-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **G/L Budgets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0ea24-120">Kies de actie **Lijst bewerken** en vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="0ea24-120">Choose the **Edit List** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="0ea24-121">Kies de actie **Budget bewerken**.</span><span class="sxs-lookup"><span data-stu-id="0ea24-121">Choose the **Edit Budget** action.</span></span>
4. <span data-ttu-id="0ea24-122">Vul boven in het venster **Budget** de benodigde velden in om te definiëren wat wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0ea24-122">At the top of the **Budget** window, fill in the fields as necessary to define what is displayed.</span></span>  

    <span data-ttu-id="0ea24-123">Alleen posten met de budgetnaam die u hebt ingevoerd in het veld **Budgetnaam** worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0ea24-123">Only entries that contain the budget name that you entered in the **budget Name** field are shown.</span></span> <span data-ttu-id="0ea24-124">Aangezien de begrotingsnaam net is gemaakt, zijn er geen posten die overeenkomen met het filter.</span><span class="sxs-lookup"><span data-stu-id="0ea24-124">Because the budget name has just been created, there are no entries that match the filter.</span></span> <span data-ttu-id="0ea24-125">Daarom is het venster leeg.</span><span class="sxs-lookup"><span data-stu-id="0ea24-125">Therefore, the window is empty.</span></span>  
5. <span data-ttu-id="0ea24-126">Voer een bedrag in door op de betreffende cel in de matrix te klikken.</span><span class="sxs-lookup"><span data-stu-id="0ea24-126">To enter an amount, choose the relevant cell in the matrix.</span></span> <span data-ttu-id="0ea24-127">Het venster **Grootboekbudgetposten** verschijnt.</span><span class="sxs-lookup"><span data-stu-id="0ea24-127">The **G/L Budget Entries** window opens.</span></span>  
6. <span data-ttu-id="0ea24-128">Maak een nieuwe regel en vul het veld **Bedrag** in.</span><span class="sxs-lookup"><span data-stu-id="0ea24-128">Create a new line and fill in the **Amount** field.</span></span> <span data-ttu-id="0ea24-129">Sluit het venster **Grootboekbudgetposten**.</span><span class="sxs-lookup"><span data-stu-id="0ea24-129">Close the **G/L Budget Entries** window.</span></span>  
7. <span data-ttu-id="0ea24-130">Herhaal stap 5 tot en met 6 totdat u alle budgetbedragen hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="0ea24-130">Repeat steps 5 and 6 until you have entered all of the budget amounts.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0ea24-131">Op het sneltabblad **Filters** kunt u de budgetinformatie filteren op budgetdimensies die u hebt ingesteld onder de budgetnaam.</span><span class="sxs-lookup"><span data-stu-id="0ea24-131">On the **Filters** FastTab, you can filter the budget information by budget dimensions you have set up under the budget name.</span></span>   

## <a name="see-also"></a><span data-ttu-id="0ea24-132">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0ea24-132">See Also</span></span>
[<span data-ttu-id="0ea24-133">Financiën</span><span class="sxs-lookup"><span data-stu-id="0ea24-133">Finance</span></span>](finance.md)  
[<span data-ttu-id="0ea24-134">Bedrijfsinformatie</span><span class="sxs-lookup"><span data-stu-id="0ea24-134">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="0ea24-135">Financiën instellen</span><span class="sxs-lookup"><span data-stu-id="0ea24-135">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="0ea24-136">Het grootboek en het rekeningschema</span><span class="sxs-lookup"><span data-stu-id="0ea24-136">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="0ea24-137">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0ea24-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

