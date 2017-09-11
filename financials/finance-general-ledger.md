---
title: Leren over grootboek en COA| Microsoft Docs
description: "Beschrijft het grootboek, het rekeningschema en rekeningcategorieën."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 06becfd7e54803fea925e8364719576bef0a8bab
ms.contentlocale: nl-be
ms.lasthandoff: 09/11/2017

---
# <a name="understanding-the-general-ledger-and-the-coa"></a><span data-ttu-id="9429c-103">Het grootboek en COA begrijpen</span><span class="sxs-lookup"><span data-stu-id="9429c-103">Understanding the General Ledger and the COA</span></span>
<span data-ttu-id="9429c-104">In het grootboek worden uw financiële gegevens opgeslagen en het rekeningschema bevat de rekeningen waarnaar alle grootboekposten worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="9429c-104">The general ledger stores your financial data, and the chart of accounts shows the accounts that all general ledger entries are posted to.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="9429c-105"> bevat een standaardrekeningschema dat gereed is voor ondersteuning van uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="9429c-105"> includes a standard chart of accounts that is ready to support your business.</span></span>

## <a name="general-ledger-setup-and-general-posting-setup"></a><span data-ttu-id="9429c-106">Grootboekinstellingen en algemene boekingsinstellingen</span><span class="sxs-lookup"><span data-stu-id="9429c-106">General Ledger Setup and General Posting Setup</span></span>
<span data-ttu-id="9429c-107">De instelling van het grootboek bevindt zich in de kern van financiële processen omdat hiermee wordt bepaald hoe u gegevens boekt.</span><span class="sxs-lookup"><span data-stu-id="9429c-107">The setup of the general ledger is at the core of financial processes because it defines how you post data.</span></span>  

<span data-ttu-id="9429c-108">In het venster **Grootboekinstellingen** geeft u op hoe bepaalde boekhoudkwesties in uw bedrijf worden afgehandeld, zoals:</span><span class="sxs-lookup"><span data-stu-id="9429c-108">In the **General Ledger Setup** window, you specify how to handle certain accounting issues in your company, such as:</span></span>  

* <span data-ttu-id="9429c-109">Factuurafrondingsdetails</span><span class="sxs-lookup"><span data-stu-id="9429c-109">Invoice rounding details</span></span>  
* <span data-ttu-id="9429c-110">Adresindelingen</span><span class="sxs-lookup"><span data-stu-id="9429c-110">Address formats</span></span>  
* <span data-ttu-id="9429c-111">Financiële rapportage</span><span class="sxs-lookup"><span data-stu-id="9429c-111">Financial reporting</span></span>  

<span data-ttu-id="9429c-112">In het venster **Boekingsgroepinstelling** geeft u op dezelfde manier op hoe u combinaties van algemene bedrijfsgroepen en algemene productboekingsgroepen wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="9429c-112">Similarly, in the **General Posting Setup** window, you specify how you want to set up combinations of general business and general product posting groups.</span></span> <span data-ttu-id="9429c-113">Met boekingsgroepen worden entiteiten zoals klanten, leveranciers, artikelen, resources en verkoop- en inkoopdocumenten aan grootboekrekeningen gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="9429c-113">Posting groups map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> <span data-ttu-id="9429c-114">U vult een regel in voor elke combinatie van bedrijfs- en productboekingsgroep.</span><span class="sxs-lookup"><span data-stu-id="9429c-114">You fill in a line for each combination of business posting group and product posting group.</span></span> <span data-ttu-id="9429c-115">Zie [Boekingsgroepinstellingen](finance-posting-groups.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="9429c-115">For more information, see [Posting Group Setups](finance-posting-groups.md)</span></span>  

## <a name="the-chart-of-accounts"></a><span data-ttu-id="9429c-116">het rekeningschema</span><span class="sxs-lookup"><span data-stu-id="9429c-116">The Chart of Accounts</span></span>
<span data-ttu-id="9429c-117">In het rekeningschema worden alle grootboekrekeningen weergegeven.</span><span class="sxs-lookup"><span data-stu-id="9429c-117">The chart of accounts shows all general ledger accounts.</span></span> <span data-ttu-id="9429c-118">In het rekeningschema kunt u onder andere het volgende doen:</span><span class="sxs-lookup"><span data-stu-id="9429c-118">From the chart of accounts, you can do things like:</span></span>  

* <span data-ttu-id="9429c-119">Rapporten weergeven waarin grootboekposten en saldi worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="9429c-119">View reports that show general ledger entries and balances.</span></span>  
* <span data-ttu-id="9429c-120">Sluit uw resultatenrekening.</span><span class="sxs-lookup"><span data-stu-id="9429c-120">Close your income statement.</span></span>  
* <span data-ttu-id="9429c-121">Open de grootboekrekeningkaart om instellingen toe te voegen of te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="9429c-121">Open the G/L account card to add or change settings.</span></span>  
* <span data-ttu-id="9429c-122">Bekijk een lijst met boekingsgroepen waarmee naar die rekening wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="9429c-122">See a list of posting groups that post to that account.</span></span>  

<span data-ttu-id="9429c-123">U kunt grootboekrekeningen toevoegen, wijzigen of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="9429c-123">You can add, change, or delete general ledger accounts.</span></span> <span data-ttu-id="9429c-124">Om verschillen te voorkomen, kunt u echter geen grootboekrekening verwijderen als deze gegevens worden gebruikt in het rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="9429c-124">However, to prevent discrepancies, you can't delete a general ledger account if it's data is used in the chart of accounts.</span></span>  

## <a name="account-categories"></a><span data-ttu-id="9429c-125">Rekeningcategorieën</span><span class="sxs-lookup"><span data-stu-id="9429c-125">Account Categories</span></span>
<span data-ttu-id="9429c-126">U kunt de structuur van uw financiële overzichten personaliseren door grootboekrekeningen toe te wijzen aan rekeningcategorieën.</span><span class="sxs-lookup"><span data-stu-id="9429c-126">You can personalize the structure of your financial statements by mapping general ledger accounts to account categories.</span></span>  

<span data-ttu-id="9429c-127">Het venster **GB-rekeningcategorieën** toont uw categorieën en subcategorieën en de grootboekrekeningen die eraan zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="9429c-127">The **G/L Account Categories** window shows your categories and subcategories, and the G/L accounts that are assigned to them.</span></span> <span data-ttu-id="9429c-128">U kunt nieuwe subcategorieën maken en die categorieën toewijzen aan bestaande rekeningen.</span><span class="sxs-lookup"><span data-stu-id="9429c-128">You can create new subcategories and assign those categories to existing accounts.</span></span>  

<span data-ttu-id="9429c-129">U maakt een categoriegroep door andere subcategorieën onder een regel te laten inspringen in het venster **GB-rekeningcategorieën**.</span><span class="sxs-lookup"><span data-stu-id="9429c-129">You create a category group by indenting other subcategories under a line in the **G/L Account Categories** window.</span></span> <span data-ttu-id="9429c-130">Zo wordt het gemakkelijk voor u om een overzicht te krijgen, omdat elke groepering een totaalsaldo weergeeft.</span><span class="sxs-lookup"><span data-stu-id="9429c-130">This makes it easy for you to get an overview, because each grouping shows a total balance.</span></span> <span data-ttu-id="9429c-131">U kunt bijvoorbeeld subcategorieën maken voor verschillende soorten activa en vervolgens categoriegroepen maken voor vaste activa versus huidige activa.</span><span class="sxs-lookup"><span data-stu-id="9429c-131">For example, you can create subcategories for different types of assets, and then create category groups for fixed assets versus current assets.</span></span>  

<span data-ttu-id="9429c-132">U kunt opgeven of de rekeningen in elke subcategorie moeten worden opgenomen in bepaalde soorten rapporten.</span><span class="sxs-lookup"><span data-stu-id="9429c-132">You can specify whether the accounts in each subcategory must be included in specific types of reports.</span></span> <span data-ttu-id="9429c-133">De rekeningcategorieën helpen de indeling te definiëren van uw financiële overzichten.</span><span class="sxs-lookup"><span data-stu-id="9429c-133">The account categories help define the layout of your financial statements.</span></span>  

<span data-ttu-id="9429c-134">Het standaardsaldo-overzicht heeft bijvoorbeeld één subcategorie voor Kas onder Huidige activa.</span><span class="sxs-lookup"><span data-stu-id="9429c-134">For example, the default balance statement has a subcategory for Cash under Current Assets.</span></span> <span data-ttu-id="9429c-135">Als u wilt dat kleine kas en de betaalrekening worden meegenomen in het saldo-overzicht, kunt u het volgende doen:</span><span class="sxs-lookup"><span data-stu-id="9429c-135">If you want the balance statement consider petty cash and checking, you can:</span></span>  

1. <span data-ttu-id="9429c-136">Voeg twee nieuwe subcategorieën toe.</span><span class="sxs-lookup"><span data-stu-id="9429c-136">Add two new subcategories.</span></span> <span data-ttu-id="9429c-137">Een voor kleine kas en een voor uw betaalrekening.</span><span class="sxs-lookup"><span data-stu-id="9429c-137">One for petty cash, and one for your checking account.</span></span>  
2. <span data-ttu-id="9429c-138">Geef de extra rapportdefinitie **Kasrekeningen** voor deze subcategorieën op.</span><span class="sxs-lookup"><span data-stu-id="9429c-138">Specify the additional report definition **Cash Accounts** for these subcategories.</span></span>  
3. <span data-ttu-id="9429c-139">Laat ze inspringen onder de subcategorie **Kas**.</span><span class="sxs-lookup"><span data-stu-id="9429c-139">Indent them under the **Cash** subcategory.</span></span>  

<span data-ttu-id="9429c-140">De volgende keer dat u rapportageschema's genereert, bevat uw saldo-overzicht een totaalsaldo voor kas en twee regels met saldi voor kleine kas en de betaalrekening.</span><span class="sxs-lookup"><span data-stu-id="9429c-140">The next time you generate account schedules your balance statement will show a total balance for cash and two lines with balances for petty cash and the checking account.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9429c-141">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9429c-141">See Also</span></span>
[<span data-ttu-id="9429c-142">Financiën</span><span class="sxs-lookup"><span data-stu-id="9429c-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="9429c-143">De rekeningschema's instellen of wijzigen</span><span class="sxs-lookup"><span data-stu-id="9429c-143">Setting Up or Changing the Chart of Accounts</span></span>](finance-setup-chart-accounts.md)  
[<span data-ttu-id="9429c-144">Bedrijfsinformatie</span><span class="sxs-lookup"><span data-stu-id="9429c-144">Business Intelligence</span></span>](bi.md)  

