---
title: Budgetten maken| Microsoft Docs
description: "Beschrijft hoe u budgetten maakt om verschillende financiële activiteiten te prognosticeren en dimensies toewijst voor bedrijfsinformatiedoeleinden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: cda69d70ece090a149a13e5e1f4ed02fa70c49f7
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create--budgets"></a><span data-ttu-id="20da8-103">Procedure: budgetten maken</span><span class="sxs-lookup"><span data-stu-id="20da8-103">How to: Create  Budgets</span></span>
<span data-ttu-id="20da8-104">U kunt budgetten met aparte namen maken als u meerdere budgetten wilt gebruiken voor dezelfde perioden.</span><span class="sxs-lookup"><span data-stu-id="20da8-104">You can have multiple budgets for identical time periods by creating budgets with separate names.</span></span> <span data-ttu-id="20da8-105">Eerst stelt u de begrotingsnaam in en voert u de begrotingscijfers in.</span><span class="sxs-lookup"><span data-stu-id="20da8-105">First, you set up the budget name and enter the budget figures.</span></span> <span data-ttu-id="20da8-106">De begrotingsnaam wordt vervolgens opgenomen op alle begrotingsposten die u maakt.</span><span class="sxs-lookup"><span data-stu-id="20da8-106">The budget name is then included on all the budget entries you create.</span></span>  

 <span data-ttu-id="20da8-107">Wanneer u een budget maakt, kunt u vier dimensies voor elk budget opgeven.</span><span class="sxs-lookup"><span data-stu-id="20da8-107">When you create a budget, you can define four dimensions for each budget.</span></span> <span data-ttu-id="20da8-108">Deze budgetspecifieke dimensies worden budgetdimensies genoemd.</span><span class="sxs-lookup"><span data-stu-id="20da8-108">These budget-specific dimensions are called budget dimensions.</span></span> <span data-ttu-id="20da8-109">U selecteert de budgetdimensies voor elk budget uit de ingestelde dimensies.</span><span class="sxs-lookup"><span data-stu-id="20da8-109">You select the budget dimensions for each budget from among the dimensions you have already set up.</span></span> <span data-ttu-id="20da8-110">Met budgetdimensies kunnen budgetfilters worden ingesteld en dimensiegegevens aan budgetposten worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="20da8-110">Budget dimensions can be used to set filters on a budget and to add dimension information to budget entries.</span></span> <span data-ttu-id="20da8-111">Zie voor meer informatie [Werken met dimensies](finance-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="20da8-111">For more information, see [Working with Dimensions](finance-dimensions.md).</span></span>

 <span data-ttu-id="20da8-112">Budgetten spelen een belangrijke rol in bedrijfsinformatie, zoals in financiële overzichten gebaseerd op rapportageschema's die budgetposten bevatten, of wanneer gebudgetteerde en werkelijke bedragen in het rekeningschema worden geanalyseerd.</span><span class="sxs-lookup"><span data-stu-id="20da8-112">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="20da8-113">Zie voor meer informatie [Bedrijfsinformatie](bi.md).</span><span class="sxs-lookup"><span data-stu-id="20da8-113">For more information, see [Business Intelligence](bi.md).</span></span>

 <span data-ttu-id="20da8-114">Budgetten spelen een belangrijke rol in bedrijfsinformatie, zoals in financiële overzichten gebaseerd op rapportageschema's die budgetposten bevatten, of wanneer gebudgetteerde en werkelijke bedragen in het rekeningschema worden geanalyseerd.</span><span class="sxs-lookup"><span data-stu-id="20da8-114">Budgets play an important role in business intelligence, such as in financial statement based on account schedules that include budget entries or when analyzing budgeted versus actual amounts in the chart of accounts.</span></span> <span data-ttu-id="20da8-115">Zie voor meer informatie [Bedrijfsinformatie](bi.md).</span><span class="sxs-lookup"><span data-stu-id="20da8-115">For more information, see [Business Intelligence](bi.md).</span></span>

<span data-ttu-id="20da8-116">In kostenadministratie werkt u met kostenbudgetten op een soortgelijke manier.</span><span class="sxs-lookup"><span data-stu-id="20da8-116">In cost accounting, you work with cost budgets in a similar way.</span></span> <span data-ttu-id="20da8-117">Zie [Procedure: Kostenbudgetten maken](finance-create-cost-budgets.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="20da8-117">For more information, see [Creating Cost Budgets](finance-create-cost-budgets.md).</span></span>    

 > [!NOTE]  
>   <span data-ttu-id="20da8-118">Deze functionaliteit vereist dat uw ervaring is ingesteld op **Suite**.</span><span class="sxs-lookup"><span data-stu-id="20da8-118">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="20da8-119">Zie voor meer informatie [Uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-ervaring aanpassen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="20da8-119">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>  

### <a name="to-create-a-new-budget"></a><span data-ttu-id="20da8-120">Een nieuw budget maken</span><span class="sxs-lookup"><span data-stu-id="20da8-120">To create a new budget</span></span>  

1. <span data-ttu-id="20da8-121">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Grootboekbudgetten** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="20da8-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **G/L Budgets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="20da8-122">Kies de actie **Lijst bewerken** en vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="20da8-122">Choose the **Edit List** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="20da8-123">Kies de actie **Budget bewerken**.</span><span class="sxs-lookup"><span data-stu-id="20da8-123">Choose the **Edit Budget** action.</span></span>
4. <span data-ttu-id="20da8-124">Vul boven in het venster **Budget** de benodigde velden in om te definiëren wat wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="20da8-124">At the top of the **Budget** window, fill in the fields as necessary to define what is displayed.</span></span>  

    <span data-ttu-id="20da8-125">Alleen posten met de budgetnaam die u hebt ingevoerd in het veld **Budgetnaam** worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="20da8-125">Only entries that contain the budget name that you entered in the **budget Name** field are shown.</span></span> <span data-ttu-id="20da8-126">Aangezien de begrotingsnaam net is gemaakt, zijn er geen posten die overeenkomen met het filter.</span><span class="sxs-lookup"><span data-stu-id="20da8-126">Because the budget name has just been created, there are no entries that match the filter.</span></span> <span data-ttu-id="20da8-127">Daarom is het venster leeg.</span><span class="sxs-lookup"><span data-stu-id="20da8-127">Therefore, the window is empty.</span></span>  
5. <span data-ttu-id="20da8-128">Voer een bedrag in door op de betreffende cel in de matrix te klikken.</span><span class="sxs-lookup"><span data-stu-id="20da8-128">To enter an amount, choose the relevant cell in the matrix.</span></span> <span data-ttu-id="20da8-129">Het venster **Grootboekbudgetposten** verschijnt.</span><span class="sxs-lookup"><span data-stu-id="20da8-129">The **G/L Budget Entries** window opens.</span></span>  
6. <span data-ttu-id="20da8-130">Maak een nieuwe regel en vul het veld **Bedrag** in.</span><span class="sxs-lookup"><span data-stu-id="20da8-130">Create a new line and fill in the **Amount** field.</span></span> <span data-ttu-id="20da8-131">Sluit het venster **Grootboekbudgetposten**.</span><span class="sxs-lookup"><span data-stu-id="20da8-131">Close the **G/L Budget Entries** window.</span></span>  
7. <span data-ttu-id="20da8-132">Herhaal stap 5 tot en met 6 totdat u alle budgetbedragen hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="20da8-132">Repeat steps 5 and 6 until you have entered all of the budget amounts.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="20da8-133">Op het sneltabblad **Filters** kunt u de budgetinformatie filteren op budgetdimensies die u hebt ingesteld onder de budgetnaam.</span><span class="sxs-lookup"><span data-stu-id="20da8-133">On the **Filters** FastTab, you can filter the budget information by budget dimensions you have set up under the budget name.</span></span>   

## <a name="see-also"></a><span data-ttu-id="20da8-134">Zie ook</span><span class="sxs-lookup"><span data-stu-id="20da8-134">See Also</span></span>
[<span data-ttu-id="20da8-135">Financiën</span><span class="sxs-lookup"><span data-stu-id="20da8-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="20da8-136">Bedrijfsinformatie</span><span class="sxs-lookup"><span data-stu-id="20da8-136">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="20da8-137">Financiën instellen</span><span class="sxs-lookup"><span data-stu-id="20da8-137">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="20da8-138">Het grootboek en het rekeningschema</span><span class="sxs-lookup"><span data-stu-id="20da8-138">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="20da8-139">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="20da8-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

