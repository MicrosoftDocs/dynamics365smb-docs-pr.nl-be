---
title: Optionele activiteiten voor het afsluiten van periodes | Microsoft Docs
description: Dit onderwerp schetst de optionele processen en activiteiten voor het sluiten van boekingsperioden in Finance and Operations, Business edition.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, aging, creditor payments, vendor payments
ms.date: 06/19/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 344e294083813d41b415ad07e6e8acdd3fe5047b
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="overview-of-tasks-to-close-accounting-periods"></a><span data-ttu-id="67963-103">Overzicht van taken voor het sluiten van boekingsperioden</span><span class="sxs-lookup"><span data-stu-id="67963-103">Overview of Tasks to Close Accounting Periods</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="67963-104"> dwingt u niet om perioden te sluiten, maar er zijn veel activiteiten voor periode-einden (maandeinden) die u kunt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="67963-104"> does not force you to close periods, however, there are many period-end (month-end) activities that you can do.</span></span> <span data-ttu-id="67963-105">In dit onderwerp vindt u een overzicht van optionele processen en activiteiten voor het afsluiten van perioden.</span><span class="sxs-lookup"><span data-stu-id="67963-105">This topic provides an overview of optional processes and activities for closing periods.</span></span>  

## <a name="general-ledger"></a><span data-ttu-id="67963-106">Grootboek</span><span class="sxs-lookup"><span data-stu-id="67963-106">General Ledger</span></span>
* <span data-ttu-id="67963-107">Geef de boekingsperioden voor het gehele systeem of een specifieke gebruiker op.</span><span class="sxs-lookup"><span data-stu-id="67963-107">Specify system-wide and user-specific posting periods.</span></span>  

    <span data-ttu-id="67963-108">Hiermee worden de datums opgegeven waartussen u boekingen wilt toestaan.</span><span class="sxs-lookup"><span data-stu-id="67963-108">This specifies the dates between which you allow posting.</span></span> <span data-ttu-id="67963-109">Afhankelijk van uw zakelijke processen wilt u het boeken mogelijk toestaan aan het begin of juist aan het einde van de periode.</span><span class="sxs-lookup"><span data-stu-id="67963-109">Depending on your business, you may want to allow posting at the start of the period, or toward the end.</span></span> <span data-ttu-id="67963-110">Zie [Boekingsperioden opgeven](finance-how-specify-posting-periods.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="67963-110">For more information, see [Specify Posting Periods](finance-how-specify-posting-periods.md).</span></span>  
* <span data-ttu-id="67963-111">Voer alle noodzakelijke grootboekherwaarderingen uit.</span><span class="sxs-lookup"><span data-stu-id="67963-111">Make all necessary G/L adjustments.</span></span>  
* <span data-ttu-id="67963-112">Wijzig en boek periodieke dagboeken.</span><span class="sxs-lookup"><span data-stu-id="67963-112">Update and post Recurring Journals.</span></span>  
  <!--* Process Consolidations-->
* <span data-ttu-id="67963-113">Voer rapportageschema's als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="67963-113">Run account schedules as follows:</span></span>  
  * <span data-ttu-id="67963-114">Open het venster **Rapportageschema** en kies de actie **Afdrukken**.</span><span class="sxs-lookup"><span data-stu-id="67963-114">Open the **Account Schedule** window, and then choose the **Print** action.</span></span>  

## <a name="sales-and-receivables"></a><span data-ttu-id="67963-115">Verkopen en tegoeden</span><span class="sxs-lookup"><span data-stu-id="67963-115">Sales and Receivables</span></span>
* <span data-ttu-id="67963-116">Boek alle verkooporders, facturen, creditnota's en retourorders.</span><span class="sxs-lookup"><span data-stu-id="67963-116">Post all sales orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="67963-117">Boek alle ontvangstendagboeken.</span><span class="sxs-lookup"><span data-stu-id="67963-117">Post all cash receipt journals.</span></span>  
* <span data-ttu-id="67963-118">Wijzig en boek periodieke dagboeken die zijn gerelateerd aan Verkoop.</span><span class="sxs-lookup"><span data-stu-id="67963-118">Update and post recurring journals that are related to sales and receivables.</span></span>  
* <span data-ttu-id="67963-119">Reconcilieer klanten met het grootboek.</span><span class="sxs-lookup"><span data-stu-id="67963-119">Reconcile accounts receivable to the general ledger.</span></span>  
* <span data-ttu-id="67963-120">Voer de batchverwerking **Gefactureerde verkooporders verwijderen** uit.</span><span class="sxs-lookup"><span data-stu-id="67963-120">Run the **Delete Invoiced Sales Orders** batch job.</span></span>  

## <a name="purchases-and-payables"></a><span data-ttu-id="67963-121">Inkopen en schulden</span><span class="sxs-lookup"><span data-stu-id="67963-121">Purchases and Payables</span></span>
* <span data-ttu-id="67963-122">Boek alle inkooporders, facturen, creditnota's en retourorders.</span><span class="sxs-lookup"><span data-stu-id="67963-122">Post all purchase orders, invoices, credit memos, and return orders.</span></span>  
* <span data-ttu-id="67963-123">Boek alle betalingsdagboeken.</span><span class="sxs-lookup"><span data-stu-id="67963-123">Post all payment journals.</span></span>  
* <span data-ttu-id="67963-124">Wijzig en boek periodieke dagboeken die zijn gerelateerd aan Inkoop.</span><span class="sxs-lookup"><span data-stu-id="67963-124">Update and post recurring journals that are related to purchases & payables.</span></span>  
* <span data-ttu-id="67963-125">Voer het rapport **Vervallen betalingen** uit en reconcilieer leveranciers met het grootboek.</span><span class="sxs-lookup"><span data-stu-id="67963-125">Run the **Aged Accounts Payable** report and reconcile accounts payable to the general ledger.</span></span>  
* <span data-ttu-id="67963-126">Voer de batchverwerking **Gefactureerde inkooporders verwijderen** uit.</span><span class="sxs-lookup"><span data-stu-id="67963-126">Run the **Delete Invoiced Purchase Orders** batch job.</span></span>  

<span data-ttu-id="67963-127">Vast activum</span><span class="sxs-lookup"><span data-stu-id="67963-127">Fixed Assets</span></span>
* <span data-ttu-id="67963-128">Boek alle onderhoudskosten via de VA-dagboeken of Facturen.</span><span class="sxs-lookup"><span data-stu-id="67963-128">Post all maintenance costs have been posted through the fixed asset journals or invoices.</span></span>
* <span data-ttu-id="67963-129">Boek herwaarderingen.</span><span class="sxs-lookup"><span data-stu-id="67963-129">Post adjustments.</span></span>
* <span data-ttu-id="67963-130">Boek waardevermeerdering.</span><span class="sxs-lookup"><span data-stu-id="67963-130">Post appreciation.</span></span>
* <span data-ttu-id="67963-131">Boek afschrijving.</span><span class="sxs-lookup"><span data-stu-id="67963-131">Post depreciation.</span></span>
* <span data-ttu-id="67963-132">Wijzig en boek het periodiek VA-dagboek.</span><span class="sxs-lookup"><span data-stu-id="67963-132">Update and post the recurring fixed asset journal.</span></span>

<span data-ttu-id="67963-133">Intercomp</span><span class="sxs-lookup"><span data-stu-id="67963-133">Intercompany</span></span>
* <span data-ttu-id="67963-134">IC-transacties verwerken</span><span class="sxs-lookup"><span data-stu-id="67963-134">Process Intercompany Transactions</span></span>

## <a name="calculate-and-process-sales-tax"></a><span data-ttu-id="67963-135">Btw berekenen en verwerken</span><span class="sxs-lookup"><span data-stu-id="67963-135">Calculate and Process Sales Tax</span></span>
* <span data-ttu-id="67963-136">Vul belastingaangiften in.</span><span class="sxs-lookup"><span data-stu-id="67963-136">Complete Tax Statements.</span></span>  

## <a name="see-also"></a><span data-ttu-id="67963-137">Zie ook</span><span class="sxs-lookup"><span data-stu-id="67963-137">See Also</span></span>
[<span data-ttu-id="67963-138">Afsluitingsjaren en -perioden</span><span class="sxs-lookup"><span data-stu-id="67963-138">Closing Years and Periods</span></span>](year-close-years-periods.md)  
[<span data-ttu-id="67963-139">Boeken afsluiten</span><span class="sxs-lookup"><span data-stu-id="67963-139">Closing Books</span></span>](year-close-books.md)  
<span data-ttu-id="67963-140">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="67963-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

