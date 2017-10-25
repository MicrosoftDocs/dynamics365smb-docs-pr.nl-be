---
title: Werkelijk versus budget analyseren| Microsoft Docs
description: Beschrijft hoe u werkelijke bedragen analyseert in vergelijking met budgetbedragen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 06/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 126c8da9b9ef80e954510fa8e5089906d7dd6f01
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-analyze-actual-amounts-versus-budgeted-amounts"></a><span data-ttu-id="5daf2-103">Procedure: Werkelijke bedragen analyseren in vergelijking met budgetbedragen.</span><span class="sxs-lookup"><span data-stu-id="5daf2-103">How to: Analyze Actual Amounts Versus Budgeted Amounts</span></span>
<span data-ttu-id="5daf2-104">Als onderdeel van het verzamelen, analyseren en delen van uw bedrijfsgegevens bekijkt u werkelijke bedragen in vergelijking met gebudgetteerde bedragen voor alle rekeningen en voor meerdere perioden.</span><span class="sxs-lookup"><span data-stu-id="5daf2-104">As a part of gathering, analyzing, and sharing your company data, you view actual amounts compared to budgeted amounts for all accounts and for several periods.</span></span>

<span data-ttu-id="5daf2-105">Als u gebudgetteerde bedragen wilt analyseren, moet u eerst budgetten maken.</span><span class="sxs-lookup"><span data-stu-id="5daf2-105">To analyze budgeted amounts, you must first create budgets.</span></span> <span data-ttu-id="5daf2-106">Zie [Procedure: Budgetten maken](finance-how-create-budgets.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="5daf2-106">For more information, see [How to: Create Budgets](finance-how-create-budgets.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="5daf2-107">Deze functionaliteit vereist dat uw ervaring is ingesteld op **Suite**.</span><span class="sxs-lookup"><span data-stu-id="5daf2-107">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="5daf2-108">Zie voor meer informatie [Uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-ervaring aanpassen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="5daf2-108">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-view-a-budget"></a><span data-ttu-id="5daf2-109">Een begroting bekijken</span><span class="sxs-lookup"><span data-stu-id="5daf2-109">To view a budget</span></span>
<span data-ttu-id="5daf2-110">In een begroting met dimensies kunt u de posten filteren en zo bepaalde begrotingen bekijken.</span><span class="sxs-lookup"><span data-stu-id="5daf2-110">In a budget with dimensions, you can filter the entries and see specific budgets.</span></span>

1. <span data-ttu-id="5daf2-111">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Grootboekbudgetten** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="5daf2-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **G/L Budgets**, and then choose the related link.</span></span>
2. <span data-ttu-id="5daf2-112">Open het budget dat u wilt weergeven in het venster **Grootboekbudgetten**.</span><span class="sxs-lookup"><span data-stu-id="5daf2-112">In the **G/L Budgets** window, open the budget that you want to view.</span></span>  
3. <span data-ttu-id="5daf2-113">Vul boven in het venster de benodigde velden in om te definiëren wat wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="5daf2-113">At the top of the window, fill in the fields as necessary to define what is shown.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="5daf2-114">Als u **Periode** hebt geselecteerd in het veld **Als regels weergeven** of **Als kolommen weergeven**, moet u het veld **Weergeven per** invullen.</span><span class="sxs-lookup"><span data-stu-id="5daf2-114">If you have selected **Period** in either the **Show as Lines** or the **Show as Columns** field, then you must fill in the **View by** field.</span></span> <span data-ttu-id="5daf2-115">Als u **Periode** niet hebt geselecteerd in het veld **Als regels weergeven** of **Als kolommen weergeven** voert u de juiste periode in het veld **Datumfilter** in.</span><span class="sxs-lookup"><span data-stu-id="5daf2-115">If you have not selected **Period** in either the **Show as Lines** or **Show as Columns** field, then enter the appropriate period in **Date Filter** field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="5daf2-116">Alleen posten uit de grootboekbegroting met de filtercodes die u op het sneltabblad **Filters** hebt ingevoerd, worden in de berekening opgenomen.</span><span class="sxs-lookup"><span data-stu-id="5daf2-116">Only entries from the general ledger budget with the filter codes that you enter on the **Filters** FastTab are included in the calculation.</span></span> <span data-ttu-id="5daf2-117">Budgetposten met andere filtercodes of zonder filtercodes worden niet opgenomen.</span><span class="sxs-lookup"><span data-stu-id="5daf2-117">Budget entries with other filter codes or without any filter codes are not included.</span></span> <span data-ttu-id="5daf2-118">Zolang het filter in het venster is ingesteld, worden in het budget alleen de budgetposten met deze filtercodes weergegeven.</span><span class="sxs-lookup"><span data-stu-id="5daf2-118">As long as the filter remains on the window, the budget only displays the budget entries with these filter codes.</span></span>  

> [!TIP]  
>   <span data-ttu-id="5daf2-119">Als u de begroting wilt aanpassen, kunt u de begrotingsposten aanpassen.</span><span class="sxs-lookup"><span data-stu-id="5daf2-119">If you want to modify the budget, you can modify the budget entries.</span></span> <span data-ttu-id="5daf2-120">Kies een bedrag om de onderliggende grootboekbudgetposten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="5daf2-120">Choose an amount to view the underlying general ledger budget entries.</span></span>

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a><span data-ttu-id="5daf2-121">Werkelijke en gebudgetteerde bedragen bekijken voor de rekeningen</span><span class="sxs-lookup"><span data-stu-id="5daf2-121">To view actual and budgeted amounts for all accounts</span></span>  
<span data-ttu-id="5daf2-122">U kunt grootboekbudgetten bekijken en ze vergelijken met werkelijke cijfers in verschillende onderdelen van [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5daf2-122">You can view general ledger budgets and compare them with actual figures in several areas of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

1. <span data-ttu-id="5daf2-123">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rekeningschema** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="5daf2-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="5daf2-124">Kies in het venster **Rekeningschema** de actie **Saldo/Budget (Grootboek)**.</span><span class="sxs-lookup"><span data-stu-id="5daf2-124">In the **Chart of Accounts** window, choose the **G/L Balance/Budget** action.</span></span>
3. <span data-ttu-id="5daf2-125">Vul boven in het venster de benodigde velden in om te definiëren wat wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="5daf2-125">At the top of the window, fill in the fields as necessary to define what is shown.</span></span>  
4. <span data-ttu-id="5daf2-126">Als u een specificatie wilt bekijken die deel uitmaakt van een weergegeven bedrag, moet u het veld kiezen.</span><span class="sxs-lookup"><span data-stu-id="5daf2-126">To see a specification that makes up the amount shown, choose the field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="5daf2-127">De filters die u instelt op de vensterkop, worden toegepast op grootboekposten en budgetposten.</span><span class="sxs-lookup"><span data-stu-id="5daf2-127">The filters you set in the window header will be applied to general ledger entries and also budget entries.</span></span>

<span data-ttu-id="5daf2-128">Het rekeningschema wordt weergegeven in de kolommen aan de linkerzijde.</span><span class="sxs-lookup"><span data-stu-id="5daf2-128">The leftmost columns contain the chart of accounts.</span></span> <span data-ttu-id="5daf2-129">In de eerste vier van de vijf kolommen aan de rechterzijde worden de werkelijke en gebudgetteerde debet- en creditbedragen voor elke rekening weergegeven.</span><span class="sxs-lookup"><span data-stu-id="5daf2-129">Of the five columns on the rightmost side, the first four columns show actual and budgeted debit and credit amounts for each account.</span></span> <span data-ttu-id="5daf2-130">De vijfde kolom geeft de verhouding weer tussen de werkelijke en gebudgetteerde bedragen op de grootboekrekening.</span><span class="sxs-lookup"><span data-stu-id="5daf2-130">The fifth column shows the proportional relationship between the actual and the budgeted amounts on the general ledger account.</span></span>  

> [!TIP]  
>   <span data-ttu-id="5daf2-131">Met het veld **Weergeven per** in het venster **Saldo/Budget (Grootboek)** kunt u de periodelenge selecteren.</span><span class="sxs-lookup"><span data-stu-id="5daf2-131">Use the **View by** field in the **G/L Balance/Budget** window to select the period length.</span></span> <span data-ttu-id="5daf2-132">Gebruik het veld **Weergeven als** om te selecteren hoe bedragen worden berekend, **Mutatie** of **Saldo t/m datum**.</span><span class="sxs-lookup"><span data-stu-id="5daf2-132">Use the **View as** field to select the way the amounts will be calculated, **Net Change** or **Balance at Date**.</span></span> <span data-ttu-id="5daf2-133">Kies de actie **Vorige periode** of **Volgende periode** om de periode te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="5daf2-133">Choose the **Previous Period** or **Next Period** action to change the period.</span></span>  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a><span data-ttu-id="5daf2-134">Werkelijke en gebudgetteerde bedragen bekijken voor verschillende perioden</span><span class="sxs-lookup"><span data-stu-id="5daf2-134">To view actual and budgeted amounts for several periods</span></span>  
<span data-ttu-id="5daf2-135">In plaats van de werkelijke en de gebudgetteerde bedragen in een bepaalde periode te bekijken voor alle rekeningen, kunt u een aantal perioden voor een afzonderlijke rekening bekijken.</span><span class="sxs-lookup"><span data-stu-id="5daf2-135">Instead of viewing the actual and budgeted amounts for all accounts within a single period, you can view a number of periods for a single account.</span></span>  

1. <span data-ttu-id="5daf2-136">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rekeningschema** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="5daf2-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="5daf2-137">Selecteer in het venster **Rekeningschema** de betreffende grootboekrekening en kies de actie **Rekeningsaldo/Budget**.</span><span class="sxs-lookup"><span data-stu-id="5daf2-137">In the **Chart of Accounts** window, select the relevant general ledger account, and then choose the **G/L Account Balance/Budget** action.</span></span>  
3. <span data-ttu-id="5daf2-138">Vul boven in het venster de benodigde velden in om te definiëren wat wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="5daf2-138">At the top of the window, fill in the fields as necessary to define what is shown.</span></span>   
4. <span data-ttu-id="5daf2-139">Als u een specificatie voor een weergegeven bedrag wilt bekijken, moet u het veld kiezen.</span><span class="sxs-lookup"><span data-stu-id="5daf2-139">To see a specification of an amount shown, choose the field.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5daf2-140">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5daf2-140">See Also</span></span>
<span data-ttu-id="5daf2-141">[Bedrijfsinformatie](bi.md)
[Procedure: Werken met rapportageschema's](bi-how-work-account-schedule.md)</span><span class="sxs-lookup"><span data-stu-id="5daf2-141">[Business Intelligence](bi.md)
[How to: Work with Account Schedules](bi-how-work-account-schedule.md)</span></span>  
[<span data-ttu-id="5daf2-142">Financiën</span><span class="sxs-lookup"><span data-stu-id="5daf2-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="5daf2-143">Financiën instellen</span><span class="sxs-lookup"><span data-stu-id="5daf2-143">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="5daf2-144">Het grootboek en het rekeningschema</span><span class="sxs-lookup"><span data-stu-id="5daf2-144">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="5daf2-145">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5daf2-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

