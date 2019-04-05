---
title: Een kostensoortschema instellen | Microsoft Docs
description: Kostensoortschema's lijken op rekeningschema's in het grootboek.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger, accounts
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 2846967648f5c0e0b6015c7990a941642fc27323
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "817037"
---
# <a name="set-up-cost-types"></a><span data-ttu-id="87f0e-103">Kostensoorten instellen</span><span class="sxs-lookup"><span data-stu-id="87f0e-103">Set Up Cost Types</span></span>
<span data-ttu-id="87f0e-104">Een kostensoortschema lijkt op het rekeningschema in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="87f0e-104">The chart of cost types is similar to the chart of accounts in the general ledger.</span></span> <span data-ttu-id="87f0e-105">U kunt het kostensoortschema op de volgende manieren instellen:</span><span class="sxs-lookup"><span data-stu-id="87f0e-105">You can set up the chart of cost types in the following ways:</span></span>  

-   <span data-ttu-id="87f0e-106">Geef het kostensoortschema een structuur die vergelijkbaar is met de resultatenrekeningen in het grootboekrekeningschema.</span><span class="sxs-lookup"><span data-stu-id="87f0e-106">Structure the chart of cost types similar to the income statement accounts in the general ledger chart of accounts.</span></span> <span data-ttu-id="87f0e-107">Vervolgens kunt u het grootboekrekeningschema overbrengen naar het kostensoortschema.</span><span class="sxs-lookup"><span data-stu-id="87f0e-107">Then, you can transfer the general ledger chart of accounts to the chart of cost types.</span></span> <span data-ttu-id="87f0e-108">U kunt elke gewenste aanpassing na de overdracht aanbrengen.</span><span class="sxs-lookup"><span data-stu-id="87f0e-108">You can make any necessary adjustments after the transfer.</span></span>  
-   <span data-ttu-id="87f0e-109">Maak nieuwe kostensoortschema's of voeg nieuwe kostensoorten toe aan bestaande kostensoortschema's.</span><span class="sxs-lookup"><span data-stu-id="87f0e-109">Create new chart of cost types or add new cost types to existing chart of cost types.</span></span> <span data-ttu-id="87f0e-110">U moet elke nieuwe kostensoort afzonderlijk maken.</span><span class="sxs-lookup"><span data-stu-id="87f0e-110">You must create each new cost type individually.</span></span>  

## <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types"></a><span data-ttu-id="87f0e-111">Het grootboekrekeningschema overbrengen naar het kostensoortschema</span><span class="sxs-lookup"><span data-stu-id="87f0e-111">To transfer the general ledger chart of accounts to the chart of cost types</span></span>  
1.  <span data-ttu-id="87f0e-112">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Kostensoortschema** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="87f0e-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="87f0e-113">Kies de actie **Kostensoorten ophalen uit rekeningschema**.</span><span class="sxs-lookup"><span data-stu-id="87f0e-113">Choose the **Get Cost Types from Chart of Accounts** action.</span></span> <span data-ttu-id="87f0e-114">Kies in dialoogvenster de knop **Ja** om de overdracht te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="87f0e-114">In the dialog box, choose the **Yes** button to confirm the transfer.</span></span> <span data-ttu-id="87f0e-115">De functie maakt gebruik van het rekeningschema om een kostensoortschema te maken.</span><span class="sxs-lookup"><span data-stu-id="87f0e-115">The function uses the chart of accounts to create a chart of cost types.</span></span>  

    <span data-ttu-id="87f0e-116">Het kostensoortschema bevat nu alle resultatenrekeningen in het grootboek inclusief koppen en subtotalen.</span><span class="sxs-lookup"><span data-stu-id="87f0e-116">The chart of cost types now contain all income statement accounts in the general ledger and include headings and subtotals.</span></span> <span data-ttu-id="87f0e-117">U kunt het kostensoortschema zo nodig wijzigen.</span><span class="sxs-lookup"><span data-stu-id="87f0e-117">You can change the chart of cost types, as necessary.</span></span> <span data-ttu-id="87f0e-118">U kunt bijvoorbeeld dubbele kostensoorten verwijderen.</span><span class="sxs-lookup"><span data-stu-id="87f0e-118">For example, you can delete duplicate existing cost types.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="87f0e-119">De functie **Kostensoorten registreren in rekeningschema** werkt de relatie tussen het rekeningschema en het kostensoortschema bij.</span><span class="sxs-lookup"><span data-stu-id="87f0e-119">The **Register Cost Types in Chart of Accounts** function updates the relationship between the chart of accounts and the chart of cost types.</span></span> <span data-ttu-id="87f0e-120">Het veld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="87f0e-120">The **No.**</span></span> <span data-ttu-id="87f0e-121">wordt ingevuld en gecontroleerd om ervoor te zorgen dat iedere grootboekrekening slechts aan één kostensoort is gerelateerd.</span><span class="sxs-lookup"><span data-stu-id="87f0e-121">field is filled and verified to make sure that each general ledger account is related to only one cost type.</span></span> <span data-ttu-id="87f0e-122">De functie wordt automatisch uitgevoerd voordat deze van grootboekposten naar kostprijsboekhouding wordt overgebracht.</span><span class="sxs-lookup"><span data-stu-id="87f0e-122">The function runs automatically before transferring general ledger entries to cost accounting.</span></span>  

## <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-page"></a><span data-ttu-id="87f0e-123">Nieuwe kostensoorten instellen op de pagina Kostensoortschema</span><span class="sxs-lookup"><span data-stu-id="87f0e-123">To set up new cost types in the Chart of Cost Types page</span></span>  
1.  <span data-ttu-id="87f0e-124">Open de pagina **Kostensoortschema** in de bewerkmodus.</span><span class="sxs-lookup"><span data-stu-id="87f0e-124">Open the **Chart of Cost Types** page in edit mode.</span></span>  
2.  <span data-ttu-id="87f0e-125">Vul de velden indien nodig in zoals beschreven.</span><span class="sxs-lookup"><span data-stu-id="87f0e-125">Fill in the fields as described as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  <span data-ttu-id="87f0e-126">U kunt kostensoorten instellen en onderhouden op de pagina **Kostensoortkaart** of op de pagina **Kostensoortschema**.</span><span class="sxs-lookup"><span data-stu-id="87f0e-126">You can set up and maintain cost types in either the **Cost Type Card** page or on the **Chart of Cost Types** page.</span></span> <span data-ttu-id="87f0e-127">In deze procedure stelt u kostensoorten op de pagina **Kostensoortschema** in.</span><span class="sxs-lookup"><span data-stu-id="87f0e-127">In this procedure, you set up cost types on the **Chart of Cost Types** page.</span></span>

3.  <span data-ttu-id="87f0e-128">Nadat u alle kostensoorten hebt gemaakt, kiest u de actie **Kostensoorten inspringen**.</span><span class="sxs-lookup"><span data-stu-id="87f0e-128">After you have created all cost types, choose the **Indent Cost Types** action.</span></span> <span data-ttu-id="87f0e-129">Kies in het dialoogvenster de knop **Ja**.</span><span class="sxs-lookup"><span data-stu-id="87f0e-129">In the dialog box, choose the **Yes** button.</span></span>  
4.  <span data-ttu-id="87f0e-130">Koppel het nieuwe kostensoort aan de corresponderende grootboekrekening.</span><span class="sxs-lookup"><span data-stu-id="87f0e-130">Link the new cost type to the corresponding general ledger account.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="87f0e-131">Als u definities hebt ingevoerd in de **Samentelling**-velden voor het regelsoort **Eindtotaal** voordat u de functie **Kostensoorten inspringen** uitvoert, moet u de definities opnieuw invoeren omdat de functie de waarden in alle velden **Eindtotaal** overschrijft.</span><span class="sxs-lookup"><span data-stu-id="87f0e-131">If you have entered definitions in the **Totaling** fields for the line type of **End-Total** before you run the **Indent Cost Types** function, then you must enter the definitions again because the function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="to-update-cost-types"></a><span data-ttu-id="87f0e-132">Kostensoorten bijwerken</span><span class="sxs-lookup"><span data-stu-id="87f0e-132">To update cost types</span></span>  
1.  <span data-ttu-id="87f0e-133">Op de pagina **Instelling kostprijsboekhouding** selecteert u of het kostensoortschema automatisch wilt laten bijwerken als het rekeningschema wordt gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="87f0e-133">On the **Cost Accounting Setup** page, select if you want the chart of cost types to be automatically updated when the chart of accounts is changed.</span></span>  
2.  <span data-ttu-id="87f0e-134">In het veld **Grootboekrekening afstemmen** kunt u kiezen uit de volgende opties.</span><span class="sxs-lookup"><span data-stu-id="87f0e-134">In the **Align G/L Account** field, you can choose from the following options.</span></span>  

- <span data-ttu-id="87f0e-135">in **Geen uitlijning** - er wordt geen overeenkomstige wijziging in het kostensoortschema doorgevoerd als u het rekeningschema wijzigt.</span><span class="sxs-lookup"><span data-stu-id="87f0e-135">**No Alignment** - There is no corresponding change in the chart of cost types when you change the chart of accounts.</span></span>  
- <span data-ttu-id="87f0e-136">**Geen uitlijning** - er wordt een overeenkomstige wijziging doorgevoerd in het kostensoortschema als u het rekeningschema wijzigt.</span><span class="sxs-lookup"><span data-stu-id="87f0e-136">**Automatic** - A corresponding change is made in the chart of cost types when you change the chart of accounts.</span></span>  
- <span data-ttu-id="87f0e-137">**Vragen** - wanneer u een wijziging aanbrengt in het rekeningschema krijgt u een bericht waarin u wordt gevraagd of u de overeenkomstige wijziging in het kostensoortschema wilt maken.</span><span class="sxs-lookup"><span data-stu-id="87f0e-137">**Prompt** - A message is displayed asking if you want to make a corresponding change in the chart of cost types when you change the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="87f0e-138">Zie ook</span><span class="sxs-lookup"><span data-stu-id="87f0e-138">See Also</span></span>  
[<span data-ttu-id="87f0e-139">Kosten verantwoorden</span><span class="sxs-lookup"><span data-stu-id="87f0e-139">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="87f0e-140">[Kostenplaatsen en kostenobjecten voor rekeningschema's definiëren](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="87f0e-140">[Defining Cost Centers and Cost Objects for Chart of Accounts](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span></span>  
<span data-ttu-id="87f0e-141">[Saldi tussen kostensoort, kostenplaats en kostenobject](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span><span class="sxs-lookup"><span data-stu-id="87f0e-141">[Balances Between Cost Type, Cost Center, and Cost Object](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span></span>  
<span data-ttu-id="87f0e-142">[Kostenboekhouding instellen](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="87f0e-142">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="87f0e-143">[Terminologie in kostprijsboekhouding](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="87f0e-143">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="87f0e-144">Kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="87f0e-144">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="87f0e-145">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="87f0e-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
