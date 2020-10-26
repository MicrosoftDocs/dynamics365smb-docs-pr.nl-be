---
title: Werkelijk versus budget analyseren| Microsoft Docs
description: Beschrijft hoe u werkelijke bedragen analyseert in vergelijking met budgetbedragen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 587e41ebb4e700b376e555e761a4aa221b49b6c0
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917663"
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a><span data-ttu-id="92fa9-103">Werkelijke bedragen analyseren in vergelijking met budgetbedragen</span><span class="sxs-lookup"><span data-stu-id="92fa9-103">Analyze Actual Amounts Versus Budgeted Amounts</span></span>
<span data-ttu-id="92fa9-104">Als onderdeel van het verzamelen, analyseren en delen van uw bedrijfsgegevens bekijkt u werkelijke bedragen in vergelijking met gebudgetteerde bedragen voor alle rekeningen en voor meerdere perioden.</span><span class="sxs-lookup"><span data-stu-id="92fa9-104">As a part of gathering, analyzing, and sharing your company data, you view actual amounts compared to budgeted amounts for all accounts and for several periods.</span></span>

<span data-ttu-id="92fa9-105">Als u gebudgetteerde bedragen wilt analyseren, moet u eerst grootboekbudgetten maken.</span><span class="sxs-lookup"><span data-stu-id="92fa9-105">To analyze budgeted amounts, you must first create G(L budgets.</span></span> <span data-ttu-id="92fa9-106">Zie [Grootboekbudgetten maken](finance-how-create-budgets.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="92fa9-106">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="to-view-a-gl-budget"></a><span data-ttu-id="92fa9-107">Grootboekbudget bekijken</span><span class="sxs-lookup"><span data-stu-id="92fa9-107">To view a G/L budget</span></span>
<span data-ttu-id="92fa9-108">In een begroting met dimensies kunt u de posten filteren en zo bepaalde begrotingen bekijken.</span><span class="sxs-lookup"><span data-stu-id="92fa9-108">In a budget with dimensions, you can filter the entries and see specific budgets.</span></span>

1. <span data-ttu-id="92fa9-109">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Grootboekbudgetten** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="92fa9-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **G/L Budgets** , and then choose the related link.</span></span>
2. <span data-ttu-id="92fa9-110">Open het budget dat u wilt weergeven op de pagina **Grootboekbudgetten** .</span><span class="sxs-lookup"><span data-stu-id="92fa9-110">On the **G/L Budgets** page, open the budget that you want to view.</span></span>  
3. <span data-ttu-id="92fa9-111">Vul boven aan de pagina de benodigde velden in om te definiëren wat wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="92fa9-111">At the top of the page, fill in the fields as necessary to define what is shown.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="92fa9-112">Als u **Periode** hebt geselecteerd in het veld **Als regels weergeven** of **Als kolommen weergeven** , moet u het veld **Weergeven per** invullen.</span><span class="sxs-lookup"><span data-stu-id="92fa9-112">If you have selected **Period** in either the **Show as Lines** or the **Show as Columns** field, then you must fill in the **View by** field.</span></span> <span data-ttu-id="92fa9-113">Als u **Periode** niet hebt geselecteerd in het veld **Als regels weergeven** of **Als kolommen weergeven** voert u de juiste periode in het veld **Datumfilter** in.</span><span class="sxs-lookup"><span data-stu-id="92fa9-113">If you have not selected **Period** in either the **Show as Lines** or **Show as Columns** field, then enter the appropriate period in **Date Filter** field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="92fa9-114">Alleen posten uit de grootboekbegroting met de filtercodes die u op het sneltabblad **Filters** hebt ingevoerd, worden in de berekening opgenomen.</span><span class="sxs-lookup"><span data-stu-id="92fa9-114">Only entries from the general ledger budget with the filter codes that you enter on the **Filters** FastTab are included in the calculation.</span></span> <span data-ttu-id="92fa9-115">Budgetposten met andere filtercodes of zonder filtercodes worden niet opgenomen.</span><span class="sxs-lookup"><span data-stu-id="92fa9-115">Budget entries with other filter codes or without any filter codes are not included.</span></span> <span data-ttu-id="92fa9-116">Zolang het filter op de pagina is ingesteld, worden in het budget alleen de budgetposten met deze filtercodes weergegeven.</span><span class="sxs-lookup"><span data-stu-id="92fa9-116">As long as the filter remains on the page, the budget only displays the budget entries with these filter codes.</span></span>  

> [!TIP]  
>   <span data-ttu-id="92fa9-117">Als u de begroting wilt aanpassen, kunt u de begrotingsposten aanpassen.</span><span class="sxs-lookup"><span data-stu-id="92fa9-117">If you want to modify the budget, you can modify the budget entries.</span></span> <span data-ttu-id="92fa9-118">Kies een bedrag om de onderliggende grootboekbudgetposten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="92fa9-118">Choose an amount to view the underlying general ledger budget entries.</span></span>

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a><span data-ttu-id="92fa9-119">Werkelijke en gebudgetteerde bedragen bekijken voor de rekeningen</span><span class="sxs-lookup"><span data-stu-id="92fa9-119">To view actual and budgeted amounts for all accounts</span></span>  
<span data-ttu-id="92fa9-120">U kunt grootboekbudgetten bekijken en ze vergelijken met werkelijke cijfers in verschillende onderdelen van [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="92fa9-120">You can view general ledger budgets and compare them with actual figures in several areas of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

1. <span data-ttu-id="92fa9-121">Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="92fa9-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts** , and then choose the related link.</span></span>  
2. <span data-ttu-id="92fa9-122">Kies op de pagina **Rekeningschema** de actie **Saldo/Budget (Grootboek)** .</span><span class="sxs-lookup"><span data-stu-id="92fa9-122">On the **Chart of Accounts** page, choose the **G/L Balance/Budget** action.</span></span>
3. <span data-ttu-id="92fa9-123">Vul boven aan de pagina de benodigde velden in om te definiëren wat wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="92fa9-123">At the top of the page, fill in the fields as necessary to define what is shown.</span></span>  
4. <span data-ttu-id="92fa9-124">Als u een specificatie wilt bekijken die deel uitmaakt van een weergegeven bedrag, moet u het veld kiezen.</span><span class="sxs-lookup"><span data-stu-id="92fa9-124">To see a specification that makes up the amount shown, choose the field.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="92fa9-125">De filters die u instelt in de paginakop, worden toegepast op grootboekposten en budgetposten.</span><span class="sxs-lookup"><span data-stu-id="92fa9-125">The filters you set on the page header will be applied to general ledger entries and also budget entries.</span></span>

<span data-ttu-id="92fa9-126">Het rekeningschema wordt weergegeven in de kolommen aan de linkerzijde.</span><span class="sxs-lookup"><span data-stu-id="92fa9-126">The leftmost columns contain the chart of accounts.</span></span> <span data-ttu-id="92fa9-127">In de eerste vier van de vijf kolommen aan de rechterzijde worden de werkelijke en gebudgetteerde debet- en creditbedragen voor elke rekening weergegeven.</span><span class="sxs-lookup"><span data-stu-id="92fa9-127">Of the five columns on the rightmost side, the first four columns show actual and budgeted debit and credit amounts for each account.</span></span> <span data-ttu-id="92fa9-128">De vijfde kolom geeft de verhouding weer tussen de werkelijke en gebudgetteerde bedragen op de grootboekrekening.</span><span class="sxs-lookup"><span data-stu-id="92fa9-128">The fifth column shows the proportional relationship between the actual and the budgeted amounts on the general ledger account.</span></span>  

> [!TIP]  
>   <span data-ttu-id="92fa9-129">Met het veld **Weergeven per** op de pagina **Saldo/Budget (Grootboek)** kunt u de periodelengte selecteren.</span><span class="sxs-lookup"><span data-stu-id="92fa9-129">Use the **View by** field on the **G/L Balance/Budget** page to select the period length.</span></span> <span data-ttu-id="92fa9-130">Gebruik het veld **Weergeven als** om te selecteren hoe bedragen worden berekend, **Mutatie** of **Saldo t/m datum** .</span><span class="sxs-lookup"><span data-stu-id="92fa9-130">Use the **View as** field to select the way the amounts will be calculated, **Net Change** or **Balance at Date** .</span></span> <span data-ttu-id="92fa9-131">Kies de actie **Vorige periode** of **Volgende periode** om de periode te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="92fa9-131">Choose the **Previous Period** or **Next Period** action to change the period.</span></span>  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a><span data-ttu-id="92fa9-132">Werkelijke en gebudgetteerde bedragen bekijken voor verschillende perioden</span><span class="sxs-lookup"><span data-stu-id="92fa9-132">To view actual and budgeted amounts for several periods</span></span>  
<span data-ttu-id="92fa9-133">In plaats van de werkelijke en de gebudgetteerde bedragen in een bepaalde periode te bekijken voor alle rekeningen, kunt u een aantal perioden voor een afzonderlijke rekening bekijken.</span><span class="sxs-lookup"><span data-stu-id="92fa9-133">Instead of viewing the actual and budgeted amounts for all accounts within a single period, you can view a number of periods for a single account.</span></span>  

1. <span data-ttu-id="92fa9-134">Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="92fa9-134">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts** , and then choose the related link.</span></span>  
2. <span data-ttu-id="92fa9-135">Selecteer op de pagina **Rekeningschema** de betreffende grootboekrekening en kies de actie **Rekeningsaldo/Budget** .</span><span class="sxs-lookup"><span data-stu-id="92fa9-135">On the **Chart of Accounts** page, select the relevant general ledger account, and then choose the **G/L Account Balance/Budget** action.</span></span>  
3. <span data-ttu-id="92fa9-136">Vul boven aan de pagina de benodigde velden in om te definiëren wat wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="92fa9-136">At the top of the page, fill in the fields as necessary to define what is shown.</span></span>   
4. <span data-ttu-id="92fa9-137">Als u een specificatie voor een weergegeven bedrag wilt bekijken, moet u het veld kiezen.</span><span class="sxs-lookup"><span data-stu-id="92fa9-137">To see a specification of an amount shown, choose the field.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="92fa9-138">Zie Gerelateerde training op [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="92fa9-138">See Related Training at [Microsoft Learn](/learn/modules/budgets-exchange-rates-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="92fa9-139">Zie ook</span><span class="sxs-lookup"><span data-stu-id="92fa9-139">See Also</span></span>
[<span data-ttu-id="92fa9-140">Bedrijfsinformatie</span><span class="sxs-lookup"><span data-stu-id="92fa9-140">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="92fa9-141">Werken met rekeningschema's</span><span class="sxs-lookup"><span data-stu-id="92fa9-141">Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
[<span data-ttu-id="92fa9-142">Financiën</span><span class="sxs-lookup"><span data-stu-id="92fa9-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="92fa9-143">Financiën instellen</span><span class="sxs-lookup"><span data-stu-id="92fa9-143">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="92fa9-144">Het grootboek en het rekeningschema</span><span class="sxs-lookup"><span data-stu-id="92fa9-144">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="92fa9-145">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="92fa9-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
