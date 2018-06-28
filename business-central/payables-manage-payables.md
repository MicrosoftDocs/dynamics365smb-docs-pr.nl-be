---
title: Overzicht van taken om crediteuren te beheren | Microsoft Docs
description: Schetst taken om crediteuren te beheren, bijvoorbeeld crediteuren betalen of uitgaande betalingen vereffenen met posten om facturen of creditnota's te sluiten.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/28/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 730596534df93b7aa16f7975b5c5b1307a7f571a
ms.contentlocale: nl-be
ms.lasthandoff: 06/28/2018

---
# <a name="managing-payables"></a><span data-ttu-id="1847a-103">Betalingsverplichtingen beheren</span><span class="sxs-lookup"><span data-stu-id="1847a-103">Managing Payables</span></span>
<span data-ttu-id="1847a-104">Een belangrijk deel van het beheer van uw betalingsverplichtingen is het betalen van uw leveranciers of het vergoeden van kosten die uw werknemers maken.</span><span class="sxs-lookup"><span data-stu-id="1847a-104">A big part of managing accounts payable is paying your vendors, or reimbursing your employees for expenses.</span></span> <span data-ttu-id="1847a-105">U kunt functies gebruiken om in het venster **Betalingsdagboek** automatisch betalingsregels toe te voegen voor inkoopfacturen die betaald moeten worden.</span><span class="sxs-lookup"><span data-stu-id="1847a-105">You can use functions to add payments lines for purchase invoices that are due in the **Payment Journal** window.</span></span> <span data-ttu-id="1847a-106">Als u banktransacties naar uw bank wilt verzenden, kunt u meerdere betalingsdagboekregels naar een bestand exporteren, dat u vervolgens naar uw bank uploadt.</span><span class="sxs-lookup"><span data-stu-id="1847a-106">To send transactions to your bank, you can export multiple payment journal lines to a file, and then upload the file to your bank.</span></span> <span data-ttu-id="1847a-107">U kunt ook betalingen per cheque doen, inclusief deze verzenden als elektronische betalingen.</span><span class="sxs-lookup"><span data-stu-id="1847a-107">You can also make payments by check, including transmitting checks as electronic payments.</span></span>

<span data-ttu-id="1847a-108">Een andere veel voorkomende taak is uitgaande betalingen met de relateerde leveranciers- of werknemersposten te vereffenen om daarmee de gerelateerde inkoopfacturen, inkoopcreditnota's of onkostendeclaraties te sluiten als zijnde betaald.</span><span class="sxs-lookup"><span data-stu-id="1847a-108">Another typical task is to apply outgoing payments to their related vendor or employee ledger entries in order to close purchase invoices, purchase credit memos, or employee accounts as paid.</span></span> <span data-ttu-id="1847a-109">U kunt dit werk in het venster **Betalingsreconciliatiedagboek** doen door een bankafschriftbestand te importeren om de betalingen te registreren.</span><span class="sxs-lookup"><span data-stu-id="1847a-109">You can do this in the **Payment Reconciliation Journal** window by importing a bank statement file to register the payments.</span></span> <span data-ttu-id="1847a-110">De betalingen worden vereffend met openstaande leveranciers-, klanten- of werknemersposten, door de betalingtekst te vergelijken met de informatie in de posten.</span><span class="sxs-lookup"><span data-stu-id="1847a-110">The payments are applied to open vendor, customer, or employee ledger entries by matching payment text and entry information.</span></span> <span data-ttu-id="1847a-111">Er zijn verschillende manieren om de overeenkomsten te controleren en te wijzigen voordat u het dagboek boekt.</span><span class="sxs-lookup"><span data-stu-id="1847a-111">There are various ways to review and change the matches before you post the journal.</span></span> <span data-ttu-id="1847a-112">U kunt ervoor kiezen om openstaande bankrekeningposten met betrekking tot de vereffende posten te sluiten wanneer u het dagboek boekt.</span><span class="sxs-lookup"><span data-stu-id="1847a-112">You can choose to close any open bank account ledger entries related to the applied ledger entries when you post the journal.</span></span> <span data-ttu-id="1847a-113">De bankrekening wordt automatisch gereconcilieerd wanneer alle betalingen worden vereffend.</span><span class="sxs-lookup"><span data-stu-id="1847a-113">The bank account is automatically reconciled when all payments are applied.</span></span>

<span data-ttu-id="1847a-114">U kunt ook uitgaande betalingen handmatig vereffenen in het venster **Betalingsdagboek** of vanuit de gerelateerde leveranciers- of werknemersposten.</span><span class="sxs-lookup"><span data-stu-id="1847a-114">Alternatively, you can apply outgoing payments manually in the **Payment Journal** window or from the related vendor or employee ledger entries.</span></span>

<span data-ttu-id="1847a-115">In de volgende tabel wordt een reeks taken beschreven binnen crediteuren, met koppelingen naar de beschrijvende onderwerpen.</span><span class="sxs-lookup"><span data-stu-id="1847a-115">The following table describes a sequence of tasks within accounts payable, with links to the topics that describe them.</span></span>

| <span data-ttu-id="1847a-116">Als u dit wilt doen</span><span class="sxs-lookup"><span data-stu-id="1847a-116">To</span></span> | <span data-ttu-id="1847a-117">Zie</span><span class="sxs-lookup"><span data-stu-id="1847a-117">See</span></span> |
| --- | --- |
| <span data-ttu-id="1847a-118">Genereer verschuldigde leveranciersbetalingen of werknemersvergoedingen, bereid betalingen via cheques voor en exporteer betalingen naar een bankbestand tijdens het boeken.</span><span class="sxs-lookup"><span data-stu-id="1847a-118">Generate due vendor payments or employee reimbursements, prepare check payments, and export payments to a bank file when posting.</span></span> |[<span data-ttu-id="1847a-119">Betalingen uitvoeren</span><span class="sxs-lookup"><span data-stu-id="1847a-119">Making Payments</span></span>](payables-make-payments.md) |
| <span data-ttu-id="1847a-120">Vereffen leveranciersbetalingen automatisch met niet-betaalde inkoopfacturen door een bankafschriftbestand te importeren.</span><span class="sxs-lookup"><span data-stu-id="1847a-120">Apply vendor payments automatically to unpaid purchase invoices by importing a bank statement file.</span></span> |[<span data-ttu-id="1847a-121">Betalingen automatisch vereffenen en bankrekeningen reconciliëren</span><span class="sxs-lookup"><span data-stu-id="1847a-121">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="1847a-122">Vereffen leveranciersbetalingen handmatig met niet-betaalde inkoopfacturen.</span><span class="sxs-lookup"><span data-stu-id="1847a-122">Apply vendor payments to unpaid purchase invoices manually.</span></span> |[<span data-ttu-id="1847a-123">Leveranciersbetalingen handmatig reconciliëren</span><span class="sxs-lookup"><span data-stu-id="1847a-123">Reconcile Vendor Payments Manually</span></span>](payables-how-apply-purchase-transactions-manually.md) |
|<span data-ttu-id="1847a-124">Zorg voor correcte voorraadwaardering door artikelkosten toe te voegen, zoals vracht, fysieke verwerking, verzekering en transport, die u maakt wanneer u inkoopt.</span><span class="sxs-lookup"><span data-stu-id="1847a-124">Ensure correct inventory valuation by assigning added item costs, such as freight, physical handling, insurance, and transportation that you incur when purchasing.</span></span>|[<span data-ttu-id="1847a-125">Artikeltoeslagen gebruiken om extra handelskosten te verantwoorden</span><span class="sxs-lookup"><span data-stu-id="1847a-125">Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)|

## <a name="see-also"></a><span data-ttu-id="1847a-126">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1847a-126">See Also</span></span>
[<span data-ttu-id="1847a-127">Inkoop</span><span class="sxs-lookup"><span data-stu-id="1847a-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="1847a-128">Tegoeden beheren</span><span class="sxs-lookup"><span data-stu-id="1847a-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="1847a-129">Artikeltoeslagen gebruiken om extra handelskosten te verantwoorden</span><span class="sxs-lookup"><span data-stu-id="1847a-129">Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)  
[<span data-ttu-id="1847a-130">Algemene bedrijfsfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="1847a-130">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="1847a-131">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1847a-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

