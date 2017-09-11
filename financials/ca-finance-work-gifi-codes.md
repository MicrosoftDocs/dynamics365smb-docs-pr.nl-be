---
title: GIFI-codes in Canada | Microsoft Docs
Description: In Canada kunt u instellen GIGI-codes (General Index of Financial Information) instellen en deze toewijzen aan boekingsgroepen
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d5211f5c8265e572ff1d1a809b1046ce89f8c1e6
ms.contentlocale: nl-be
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-work-with-gifi-codes-in-canada"></a><span data-ttu-id="63238-103">Procedure: Met GIFI-codes werken in Canada</span><span class="sxs-lookup"><span data-stu-id="63238-103">How to: Work With GIFI Codes in Canada</span></span>
<span data-ttu-id="63238-104">Fiscale gegevens kunnen grootboekrekeningen, rapporten, resultatenrekeningen, balansen en afschriften van ingehouden winst omvatten.</span><span class="sxs-lookup"><span data-stu-id="63238-104">Fiscal information can include general ledger accounts, reports, income statements, balance sheets, and statements of retained earnings.</span></span> <span data-ttu-id="63238-105">Fiscale gegevens worden ingedeeld met behulp van codes.</span><span class="sxs-lookup"><span data-stu-id="63238-105">Fiscal information is classified using codes.</span></span> <span data-ttu-id="63238-106">Het gebruik van codes kan de overheid helpen informatie te verwerken, elektronische aangifte voor te bereiden en elektronische belastinggegevens te valideren.</span><span class="sxs-lookup"><span data-stu-id="63238-106">The use of codes helps the government to process information, prepare for electronic filing, and validate tax information electronically.</span></span> <span data-ttu-id="63238-107">Het gebruik van statistische codes helpt statistische organisaties ook efficiënter werken, aangezien de financiële gegevens beter beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="63238-107">The use of codes also helps statistical organizations to work more efficiently, as financial information is more readily available.</span></span> <span data-ttu-id="63238-108">Zie voor meer informatie de [website van de Canada Revenue Agency](http://www.cra-arc.gc.ca/).</span><span class="sxs-lookup"><span data-stu-id="63238-108">For more information, see the [Canada Revenue Agency website](http://www.cra-arc.gc.ca/).</span></span>

<span data-ttu-id="63238-109">Het Canada Revenue Agency gebruikt GIFI-codes (General Index of Financial Information) om financiële en belastinggegevens elektronisch te verzamelen, valideren en verwerken.</span><span class="sxs-lookup"><span data-stu-id="63238-109">The Canada Revenue Agency uses General Index of Financial Information (GIFI) codes to collect, validate, and process financial and tax information electronically.</span></span> <span data-ttu-id="63238-110">Het is het beste GIFI-codes alleen toe te wijzen aan boekingsrekeningen, zodat alle totalisering wordt uitgevoerd door uw belastingvoorbereidingssoftware.</span><span class="sxs-lookup"><span data-stu-id="63238-110">It is a best practice to assign GIFI codes only to posting accounts, so that all totaling is done by your tax preparation software.</span></span>

<span data-ttu-id="63238-111">Wanneer een rekening aan een GIFI-code is gekoppeld, wordt deze onder die code aan het Revenue Agency aangegeven.</span><span class="sxs-lookup"><span data-stu-id="63238-111">When an account is associated with a GIFI code, it is reported to the revenue agency under that code.</span></span> <span data-ttu-id="63238-112">Meerdere rekeningen kunnen alle dezelfde GIFI-code hebben, maar elke rekening kan slechts één GIFI-code hebben.</span><span class="sxs-lookup"><span data-stu-id="63238-112">Multiple accounts can all have the same GIFI code, but each account can have only one GIFI code.</span></span>

<span data-ttu-id="63238-113">U kunt saldo-informatie exporteren per GIFI-code en het geëxporteerde bestand in Excel opslaan, wat handig is om informatie over te brengen naar uw belastingvoorbereidingssoftware.</span><span class="sxs-lookup"><span data-stu-id="63238-113">You can export balance information by GIFI code and save the exported file in Excel, which is useful for transferring information to your tax preparation software.</span></span>

## <a name="to-set-up-gifi-codes"></a><span data-ttu-id="63238-114">GIFI-codes instellen</span><span class="sxs-lookup"><span data-stu-id="63238-114">To set up GIFI codes</span></span>
<span data-ttu-id="63238-115">In Dynamics NAV moet u GIFI-codes instellen voor grootboekrekeningen, rapporten, balansen, rapporten, inkomstenoverzichten en afschriften van ingehouden winsten.</span><span class="sxs-lookup"><span data-stu-id="63238-115">In Dynamics NAV, you must set up GIFI codes for general ledger accounts, reports, balance sheets, income sheets, and statements of retained earnings.</span></span>

1. <span data-ttu-id="63238-116">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **GIGI-codes** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="63238-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **GIFI Codes**, and then choose the related link.</span></span>
2. <span data-ttu-id="63238-117">Kies in het venster **GIFI-codes** de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="63238-117">In the **GIFI Codes** window, choose the **New** action.</span></span>
3. <span data-ttu-id="63238-118">Stel GIFI-codes in door velden in te vullen.</span><span class="sxs-lookup"><span data-stu-id="63238-118">Set up GIFI codes by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-associate-gifi-codes-with-gl-accounts"></a><span data-ttu-id="63238-119">GIFI-codes koppelen aan grootboekrekeningen</span><span class="sxs-lookup"><span data-stu-id="63238-119">To associate GIFI codes with G/L accounts</span></span>
<span data-ttu-id="63238-120">Als u financiële gegevens wilt aangeven per GIFI-code, moet elke GIFI-code aan de juiste rekeningen worden gekoppeld in het rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="63238-120">To report financial information by GIFI code, each GIFI code must be associated with the appropriate accounts in the chart of accounts.</span></span>

1. <span data-ttu-id="63238-121">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rekeningschema** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="63238-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="63238-122">Selecteer een relevante grootboekrekening en kies vervolgens de actie **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="63238-122">Select a relevant general ledger account, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="63238-123">Selecteer op het sneltabblad **Kostprijsboekhouding** in het veld **GIFI-code** een geschikte GIFI-code.</span><span class="sxs-lookup"><span data-stu-id="63238-123">On the **Cost Accounting** FastTab, in the **GIFI Code** field, select an appropriate GIFI code.</span></span>

## <a name="to-view-account-balances-using-the-gifi-code-report"></a><span data-ttu-id="63238-124">Rekeningsaldi weergeven met behulp van het rapport GIFI-code</span><span class="sxs-lookup"><span data-stu-id="63238-124">To view account balances using the GIFI code report</span></span>
<span data-ttu-id="63238-125">U kunt uw rekeningsaldi per GIFI-code controleren met het rapport **Rekeningsaldi per GIFI-code**.</span><span class="sxs-lookup"><span data-stu-id="63238-125">You can review your account balances by GIFI code by using the **Account Balances by GIFI Code** report.</span></span>

1. <span data-ttu-id="63238-126">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rekeningsaldi per GIFI-code** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="63238-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Balances by GIFI Code**, and then choose the related link.</span></span>
2. <span data-ttu-id="63238-127">Opgeven wat in de lijst moeten worden opgenomen door de velden te vullen.</span><span class="sxs-lookup"><span data-stu-id="63238-127">Specify what to include in the report by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="63238-128">Kies de knop **Afdrukken** of **Voorbeeld**.</span><span class="sxs-lookup"><span data-stu-id="63238-128">Choose the **Print** or the **Preview** button.</span></span>

## <a name="to-export-balance-information-using-gifi-codes"></a><span data-ttu-id="63238-129">Saldo-informatie exporteren met GIFI-codes</span><span class="sxs-lookup"><span data-stu-id="63238-129">To export balance information using GIFI codes</span></span>
<span data-ttu-id="63238-130">U kunt saldo-informatie exporteren met GIFI-codes en het geëxporteerde bestand opslaan in Excel.</span><span class="sxs-lookup"><span data-stu-id="63238-130">You can export balance information using GIFI codes and save the exported file in Excel.</span></span> <span data-ttu-id="63238-131">U kunt het bestand wijzigen, opslaan of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="63238-131">You can modify, save, or delete the file.</span></span> <span data-ttu-id="63238-132">U kunt het bestand gebruiken om gegevens over te brengen naar uw belastingvoorbereidingssoftware.</span><span class="sxs-lookup"><span data-stu-id="63238-132">You can use the file to transfer information to your tax preparation software.</span></span>

1. <span data-ttu-id="63238-133">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **GIFI-gegevens exporteren naar Excel** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="63238-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Export GIFI Info. to Excel**, and then choose the related link.</span></span>
2. <span data-ttu-id="63238-134">Geef op wat naar Excel moet worden geëxporteerd door de velden in te vullen.</span><span class="sxs-lookup"><span data-stu-id="63238-134">Specify what to export to Excel by filling the fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="63238-135">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="63238-135">Choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="63238-136">Het Excel-bestand heeft de volgende kenmerken:</span><span class="sxs-lookup"><span data-stu-id="63238-136">The Excel file has the following characteristics:</span></span>

* <span data-ttu-id="63238-137">Het saldo wordt afgerond naar het dichtstbijzijnde percentage, maar de celwaarde behoudt hetzelfde percentage als in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="63238-137">The balance is rounded to the nearest percentage, but the cell value maintains the same percentage as it does in the general ledger.</span></span>
* <span data-ttu-id="63238-138">Negatieve getallen worden weergegeven als positieve getallen tussen haakjes.</span><span class="sxs-lookup"><span data-stu-id="63238-138">Negative numbers are represented as positive number in brackets.</span></span> <span data-ttu-id="63238-139">-123 wordt dus weergegeven als (123).</span><span class="sxs-lookup"><span data-stu-id="63238-139">Accordingly, -123 is represented as (123).</span></span>

## <a name="see-also"></a><span data-ttu-id="63238-140">Zie ook</span><span class="sxs-lookup"><span data-stu-id="63238-140">See Also</span></span>
<span data-ttu-id="63238-141">[Financiën](finance.md) </span><span class="sxs-lookup"><span data-stu-id="63238-141">[Finance](finance.md) </span></span>  
[<span data-ttu-id="63238-142">Financiën instellen</span><span class="sxs-lookup"><span data-stu-id="63238-142">Setting Up Finance</span></span>](finance-setup-finance.md)

