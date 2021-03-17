---
title: Codes voor audittrails instellen | Microsoft Docs
description: Lees meer over de taken om broncodes en redencodes in te stellen die u kunt gebruiken om audittrails bij te houden.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accounting, auditing, bookkeeping
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9dab74a6a8debd20de781890c3b391457c6034e3
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386911"
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails"></a><span data-ttu-id="b9f62-103">Broncodes en redencodes instellen voor audittrails</span><span class="sxs-lookup"><span data-stu-id="b9f62-103">Setting Up Source Codes and Reason Codes for Audit Trails</span></span>

<span data-ttu-id="b9f62-104">Aan alle geboekte posten wordt automatisch een broncode toegewezen zodat transacties tot aan hun herkomst kunnen worden getraceerd.</span><span class="sxs-lookup"><span data-stu-id="b9f62-104">All posted entries are automatically assigned a source code so that transactions can be traced to their origin.</span></span> <span data-ttu-id="b9f62-105">Als u aan posten een aanvullende broncode wilt toewijzen, kunt u redencodes gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b9f62-105">If you want to give entries a supplementary source code, you can use reason codes.</span></span> <span data-ttu-id="b9f62-106">Met redencodes wordt aangegeven waarom een post is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b9f62-106">Reason codes are used to indicate why an entry was created.</span></span> <span data-ttu-id="b9f62-107">Wanneer u redencodes instelt, kunt u deze toewijzen aan volledige dagboeksjablonen en -batches en aan afzonderlijke dagboekregels en -documenten.</span><span class="sxs-lookup"><span data-stu-id="b9f62-107">When you set up reason codes, you can assign them to entire journal templates and journal batches, and you can assign them to individual journal lines and documents.</span></span>  

<span data-ttu-id="b9f62-108">Gebruik voor zowel broncodes als redencodes codes die gemakkelijk te onthouden en beschrijvend zijn.</span><span class="sxs-lookup"><span data-stu-id="b9f62-108">For both source codes and reason codes, use codes that are easy to remember and descriptive.</span></span> <span data-ttu-id="b9f62-109">De code moet uniek zijn en u kunt zoveel codes instellen als u maar wilt.</span><span class="sxs-lookup"><span data-stu-id="b9f62-109">The code must be unique, and you can set up as many codes as you like.</span></span>

## <a name="define-source-codes"></a><span data-ttu-id="b9f62-110">Broncodes definiëren</span><span class="sxs-lookup"><span data-stu-id="b9f62-110">Define source codes</span></span>

<span data-ttu-id="b9f62-111">In bepaalde gevallen wilt u nagaan hoe een bepaalde post ontstaan is, bijvoorbeeld of de post afkomstig is van de boeking van een dagboek of een inkoopfactuur.</span><span class="sxs-lookup"><span data-stu-id="b9f62-111">Sometimes, you want see how a particular entry arose, such as whether it came from posting a general journal or a purchase invoice.</span></span> <span data-ttu-id="b9f62-112">Met een broncode wordt de herkomst van een post aangeduid.</span><span class="sxs-lookup"><span data-stu-id="b9f62-112">A source code indicates where an entry was created.</span></span> <span data-ttu-id="b9f62-113">Posten worden gemaakt wanneer u dagboeken en facturen boekt en bepaalde batchverwerkingen uitvoert.</span><span class="sxs-lookup"><span data-stu-id="b9f62-113">Entries are created when journals and invoices are posted and when certain batch jobs are executed.</span></span> <span data-ttu-id="b9f62-114">Elke boekingssoort heeft een bepaalde broncode, die wordt toegewezen wanneer afzonderlijke posten worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b9f62-114">Each posting type has a specific source code that is assigned when individual entries are created.</span></span>  

<span data-ttu-id="b9f62-115">Bij het boeken van dagboeken, orders, facturen of creditnota's en bij het uitvoeren van de verschillende batchverwerkingen worden posten in de financiële overzichten gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b9f62-115">Posting journals, orders, invoices, or credit memos, and running various batch jobs, creates entries in the financial statements.</span></span> <span data-ttu-id="b9f62-116">Het venster **Broncode-instelling** bevat meerdere sneltabbladen, één voor elk toepassingsgebied.</span><span class="sxs-lookup"><span data-stu-id="b9f62-116">The **Source Code Setup** page contains several FastTabs, one for each application area.</span></span> <span data-ttu-id="b9f62-117">Elk sneltabblad bevat de broncode die van toepassing is op dat toepassingsgebied.</span><span class="sxs-lookup"><span data-stu-id="b9f62-117">Each FastTab contains the source codes that are applicable for that application area.</span></span>

<span data-ttu-id="b9f62-118">Wanneer u een batchverwerking boekt of uitvoert, wordt de juiste broncode automatisch aan de post gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="b9f62-118">When you post or run a batch job, the correct source code is automatically attached to the entry.</span></span> <span data-ttu-id="b9f62-119">Als u bijvoorbeeld boekt vanuit het financieel dagboek, wordt de post gecodeerd als *FINDAGB*.</span><span class="sxs-lookup"><span data-stu-id="b9f62-119">For example, when you post from the general journal, the entry is coded as *GENJNL*.</span></span> <span data-ttu-id="b9f62-120">Vervolgens kunt u de pagina **Grootboekposten** filteren om te laten zien welke boekingen bijvoorbeeld vanuit het dagboek of uit verkoopdocumenten zijn geboekt</span><span class="sxs-lookup"><span data-stu-id="b9f62-120">You can then filter the **General Ledger Entries** page to show which entries were posted from the general journal or from sales documents, for example</span></span>

### <a name="to-define-source-codes"></a><span data-ttu-id="b9f62-121">Broncodes definiëren</span><span class="sxs-lookup"><span data-stu-id="b9f62-121">To define source codes</span></span>

1. <span data-ttu-id="b9f62-122">Kies het pictogram ![Pagina of rapport zoeken](media/ui-search/search_small.png "Pictogram Pagina of rapport zoeken"), voer **Broncode-instelling** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="b9f62-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Source Code Setup**, and then choose the related link.</span></span>  

2. <span data-ttu-id="b9f62-123">Geef in het venster **Broncode-instelling** voor elk boekingstype en elke batchtaak de relevante broncode op.</span><span class="sxs-lookup"><span data-stu-id="b9f62-123">In the **Source Code Setup** window, for each each posting type and batch job, specify the relevant source code.</span></span>  

<span data-ttu-id="b9f62-124">U kunt de inhoud van een veld later wijzigen en die wijziging heeft dan invloed op toekomstige berichten.</span><span class="sxs-lookup"><span data-stu-id="b9f62-124">You can change the contents of a field later, and that change will then impact future postings.</span></span>

## <a name="change-source-codes"></a><span data-ttu-id="b9f62-125">Broncodes wijzigen</span><span class="sxs-lookup"><span data-stu-id="b9f62-125">Change source codes</span></span>

<span data-ttu-id="b9f62-126">U wilt wellicht een broncode wijzigen.</span><span class="sxs-lookup"><span data-stu-id="b9f62-126">You may want to change a source code.</span></span> <span data-ttu-id="b9f62-127">U wilt bijvoorbeeld de broncode *DAGBOEK* wijzigen in *DAGB*.</span><span class="sxs-lookup"><span data-stu-id="b9f62-127">For example, you want to change the source code *GENJNL* to *GNJ*.</span></span>

### <a name="to-change-source-codes"></a><span data-ttu-id="b9f62-128">Broncodes wijzigen</span><span class="sxs-lookup"><span data-stu-id="b9f62-128">To change source codes</span></span>

1. <span data-ttu-id="b9f62-129">Kies het pictogram ![Pagina of rapport zoeken](media/ui-search/search_small.png "Pictogram Pagina of rapport zoeken"), voer **Broncodes** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="b9f62-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Source Codes**, and then choose the related link.</span></span>

2. <span data-ttu-id="b9f62-130">Selecteer op de regel met de te wijzigen code de code in het veld **Code**.</span><span class="sxs-lookup"><span data-stu-id="b9f62-130">On the line with the code to be changed, select the code in the **Code** field.</span></span>

3. <span data-ttu-id="b9f62-131">Voer de nieuwe code in en kies vervolgens de knop **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b9f62-131">Enter the new code, and then choose the **Yes** button.</span></span> <span data-ttu-id="b9f62-132">U kunt de inhoud van het veld **Omschrijving** ook wijzigen.</span><span class="sxs-lookup"><span data-stu-id="b9f62-132">You can also change the contents of the **Description** field.</span></span>

<span data-ttu-id="b9f62-133">De nieuwe posten die worden geboekt uit het dagboek, hebben de nieuwe broncode.</span><span class="sxs-lookup"><span data-stu-id="b9f62-133">All new entries that are posted from the general journal will have the new source code.</span></span>

## <a name="define-reason-codes"></a><span data-ttu-id="b9f62-134">Redencodes definiëren</span><span class="sxs-lookup"><span data-stu-id="b9f62-134">Define reason codes</span></span>

<span data-ttu-id="b9f62-135">Redencodes vullen de broncodes aan en worden gebruikt om aan te geven waarom een post is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b9f62-135">Reason codes supplement the source codes and are used to indicate why an entry was created.</span></span> <span data-ttu-id="b9f62-136">U kunt redencodes toewijzen aan afzonderlijke posten en u kunt permanente codes toewijzen aan bepaalde dagboeksjablonen en -batches.</span><span class="sxs-lookup"><span data-stu-id="b9f62-136">You can assign reason codes on individual entries, and you can assign permanent codes to specific journal templates and journal batches.</span></span> <span data-ttu-id="b9f62-137">Wanneer een redencode aan een dagboekregel of een verkoop- of inkoopkop is gekoppeld, worden alle posten met de redencode gemarkeerd wanneer deze worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="b9f62-137">When a reason code is linked to a journal line or a sales or purchase header, all entries are marked with the reason code when they are posted.</span></span>  

### <a name="to-set-up-reason-codes"></a><span data-ttu-id="b9f62-138">Redencodes instellen</span><span class="sxs-lookup"><span data-stu-id="b9f62-138">To set up reason codes</span></span>

1. <span data-ttu-id="b9f62-139">Kies het pictogram ![Pagina of rapport zoeken](media/ui-search/search_small.png "Pictogram Pagina of rapport zoeken"), voer **Redencodes** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="b9f62-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon")  icon, enter **Reason Codes**, and then choose the related link.</span></span>

2. <span data-ttu-id="b9f62-140">Voer in het venster **Redencodes** de eerste code in het veld **Code** in.</span><span class="sxs-lookup"><span data-stu-id="b9f62-140">In the **Reason Codes** window, enter the first code in the **Code** field.</span></span> <span data-ttu-id="b9f62-141">Typ een uitleg in het veld **Omschrijving**.</span><span class="sxs-lookup"><span data-stu-id="b9f62-141">In the **Description** field, enter an explanatory text.</span></span>

<span data-ttu-id="b9f62-142">Herhaal de procedure voor elke code die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b9f62-142">Repeat the procedure for each code you want to use.</span></span> <span data-ttu-id="b9f62-143">U kunt een onbeperkt aantal codes instellen.</span><span class="sxs-lookup"><span data-stu-id="b9f62-143">You can set up any number of codes.</span></span>

<span data-ttu-id="b9f62-144">De volgende procedure beschrijft hoe u een redencode aan een dagboeksjabloon kunt toevoegen, maar vergelijkbare stappen zijn van toepassing op het toevoegen van een redencode aan een dagboekregel of dagboekbatch.</span><span class="sxs-lookup"><span data-stu-id="b9f62-144">The following procedure describes how to add a reason code to a journal template, but similar steps apply to adding a reason code to a journal line or journal batch.</span></span>  

### <a name="to-assign-reason-codes-to-journal-templates"></a><span data-ttu-id="b9f62-145">Redencodes toewijzen aan dagboeksjablonen</span><span class="sxs-lookup"><span data-stu-id="b9f62-145">To assign reason codes to journal templates</span></span>

1. <span data-ttu-id="b9f62-146">Kies het pictogram ![Pagina of rapport zoeken](media/ui-search/search_small.png "Pictogram Pagina of rapport zoeken"), voer **Fin. dagboeksjablonen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="b9f62-146">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon")  icon, enter **General Journal Templates**, and then choose the related link.</span></span>

2. <span data-ttu-id="b9f62-147">Geef in het veld **Redencode** op de regel met de geselecteerde dagboeksjabloon de relevante code op.</span><span class="sxs-lookup"><span data-stu-id="b9f62-147">On the line with the selected journal template, in the **Reason Code** field, specify the relevant code.</span></span>

3. <span data-ttu-id="b9f62-148">Sluit de dagboeksjabloon.</span><span class="sxs-lookup"><span data-stu-id="b9f62-148">Close the journal template.</span></span>

<span data-ttu-id="b9f62-149">De geselecteerde redencode wordt gekopieerd naar nieuwe dagboekbatches die met deze dagboeksjabloon worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b9f62-149">The selected reason code will be copied to new journal batches created under this journal template.</span></span> <span data-ttu-id="b9f62-150">Op dezelfde manier kunt u redencodes toewijzen aan dagboeksjablonen in andere toepassingsgebieden.</span><span class="sxs-lookup"><span data-stu-id="b9f62-150">You assign reason codes to journal templates in the other application areas in the same way.</span></span>

### <a name="to-use-reason-codes-on-sales-and-purchase-documents"></a><span data-ttu-id="b9f62-151">Redencodes gebruiken voor verkoop- en inkoopdocumenten</span><span class="sxs-lookup"><span data-stu-id="b9f62-151">To use reason codes on sales and purchase documents</span></span>

1. <span data-ttu-id="b9f62-152">Open het betreffende verkoop- of inkoopdocument.</span><span class="sxs-lookup"><span data-stu-id="b9f62-152">Open the relevant sales or purchase document.</span></span>

2. <span data-ttu-id="b9f62-153">Voer de code in het veld **Redencode** op de verkoop- of inkoopkop in.</span><span class="sxs-lookup"><span data-stu-id="b9f62-153">On the sales or purchase header, enter the code in the **Reason Code** field.</span></span>

<span data-ttu-id="b9f62-154">Wanneer de factuur wordt geboekt, wordt de redencode gekopieerd naar elke grootboek-, klant- en leverancierspost.</span><span class="sxs-lookup"><span data-stu-id="b9f62-154">When the invoice is posted, the reason code is copied to each general ledger, customer, and vendor entry.</span></span> <span data-ttu-id="b9f62-155">U kunt geen andere redencodes toewijzen aan afzonderlijke inkoop- en verkoopregels, omdat alle regels als één post zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="b9f62-155">You cannot assign different reason codes to the individual purchase and sales lines because all lines are posted as one entry.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="b9f62-156">Zie Gerelateerde training op [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="b9f62-156">See Related Training at [Microsoft Learn](/learn/paths/set-up-financial-management-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="b9f62-157">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b9f62-157">See Also</span></span>

[<span data-ttu-id="b9f62-158">Financiën</span><span class="sxs-lookup"><span data-stu-id="b9f62-158">Finance</span></span>](finance.md)  
[<span data-ttu-id="b9f62-159">Bankrekeningen reconciliëren</span><span class="sxs-lookup"><span data-stu-id="b9f62-159">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="b9f62-160">Werken met dimensies</span><span class="sxs-lookup"><span data-stu-id="b9f62-160">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="b9f62-161">Bedrijfsgegevens importeren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="b9f62-161">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="b9f62-162">Cashflow in uw bedrijf analyseren</span><span class="sxs-lookup"><span data-stu-id="b9f62-162">Analyzing Cash Flow in Your Company</span></span>](finance-analyze-cash-flow.md)  
<span data-ttu-id="b9f62-163">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b9f62-163">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]