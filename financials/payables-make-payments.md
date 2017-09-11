---
title: Overzicht van taken om betalingen aan leveranciers te beheren | Microsoft Docs
description: Schetst taken om betalingen aan leveranciers en schuldeisers te beheren, bijvoorbeeld het boeken van betalingsregels en het ophalen van een overzicht van het verschuldigde saldo.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d0b9020596484a8910db2f5720adfe159ad96fe7
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---
# <a name="make-payments"></a><span data-ttu-id="a46ae-103">Betalingen doen</span><span class="sxs-lookup"><span data-stu-id="a46ae-103">Make Payments</span></span>
<span data-ttu-id="a46ae-104">Als u betalingen aan leveranciers betaalt, boekt u de relateerde betalingsregels in het venster **Betalingsdagboek**.</span><span class="sxs-lookup"><span data-stu-id="a46ae-104">When you make payments to vendors, you post the related payment lines in the **Payment Journal** window.</span></span> <span data-ttu-id="a46ae-105">U kunt de functie **Leveranciersbetalingen voorstellen** gebruiken om betalingen te vinden die moeten worden voldaan.</span><span class="sxs-lookup"><span data-stu-id="a46ae-105">You can use the **Suggest Vendor Payments** function to find payments that are due.</span></span> <span data-ttu-id="a46ae-106">U kunt ook het rapport **Leverancier - Open posten** gebruiken om een overzicht te krijgen van betalingen die moeten worden voldaan.</span><span class="sxs-lookup"><span data-stu-id="a46ae-106">You can also use the **Vendor - Summary Aging** report to get an overview of due payments.</span></span>

<span data-ttu-id="a46ae-107">Vanuit het betalingsdagboek kunt u automatische cheques afdrukken of vastleggen wanneer cheques worden uitgeschreven.</span><span class="sxs-lookup"><span data-stu-id="a46ae-107">From the payment journal, you can print computer checks or record when checks are written.</span></span> <span data-ttu-id="a46ae-108">Wanneer **Automatische cheque** is geselecteerd in het veld **Betalingssoort**, moeten de cheques worden afgedrukt voordat de dagboekregels kunnen worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="a46ae-108">If you select **Computer Check** in the **Bank Payment Type** field, then any lines representing checks must be printed before the payment journal can be posted.</span></span>

<span data-ttu-id="a46ae-109">Wanneer de betalingen worden geboekt, kunt u deze exporteren naar een bankbestand om ze te uploaden naar uw bank voor verwerking.</span><span class="sxs-lookup"><span data-stu-id="a46ae-109">When the payments are posted, you can export them to a bank file for upload to your bank for processing.</span></span>

<span data-ttu-id="a46ae-110">Nadat de betalingen in uw bank worden gemaakt, moet u deze met de relateerde openstaande leveranciersposten vereffenen.</span><span class="sxs-lookup"><span data-stu-id="a46ae-110">After the payments are made at your bank, you must apply them to their related open vendor ledger entries.</span></span> <span data-ttu-id="a46ae-111">U kunt dit handmatig doen of door een bankafschriftbestand te importeren en de betalingen automatisch te vereffenen.</span><span class="sxs-lookup"><span data-stu-id="a46ae-111">You can do this manually or by importing a bank statement file and applying the payments automatically.</span></span> <span data-ttu-id="a46ae-112">Zie voor meer informatie [Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="a46ae-112">For more information, see [Apply Payments Automatically and Reconcile Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span>

<span data-ttu-id="a46ae-113">In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.</span><span class="sxs-lookup"><span data-stu-id="a46ae-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="a46ae-114">Als u dit wilt doen</span><span class="sxs-lookup"><span data-stu-id="a46ae-114">To</span></span> | <span data-ttu-id="a46ae-115">Zie</span><span class="sxs-lookup"><span data-stu-id="a46ae-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="a46ae-116">Gebruik een functie om leveranciersbetalingen voor te stellen volgens geselecteerde criteria, zoals kortingsgeschiktheid, vervaldatum en uw liquiditeit.</span><span class="sxs-lookup"><span data-stu-id="a46ae-116">Use a function to suggest vendor payments according to selected criteria, such as due date, discount eligibility, and your liquidity.</span></span> |[<span data-ttu-id="a46ae-117">Procedure: Leveranciersbetalingen voorstellen</span><span class="sxs-lookup"><span data-stu-id="a46ae-117">How to: Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md) |
| <span data-ttu-id="a46ae-118">Cheques uitgeven voor betalingen, als afdrukken of computercheques.</span><span class="sxs-lookup"><span data-stu-id="a46ae-118">Issue checks for payments, either as print-outs or as computer checks.</span></span> <span data-ttu-id="a46ae-119">Cheques nietig verklaren voor of na het boeken.</span><span class="sxs-lookup"><span data-stu-id="a46ae-119">Void checks before or after posting.</span></span> |[<span data-ttu-id="a46ae-120">Procedure: Werken met cheques</span><span class="sxs-lookup"><span data-stu-id="a46ae-120">How to: Work with Checks</span></span>](payables-how-work-checks.md) |
| <span data-ttu-id="a46ae-121">Om ervoor te zorgen dat uw bank alleen gevalideerde cheques en bedragen vrijgeeft, kunt u deze verzenden in een bestand dat gegevens over de leverancier, cheque en betaling bevat.</span><span class="sxs-lookup"><span data-stu-id="a46ae-121">Make sure that your bank only clears validated checks and amounts by sending them a file that contains vendor, check, and payment information.</span></span> |[<span data-ttu-id="a46ae-122">Procedure: Een Positive Pay-bestand exporteren</span><span class="sxs-lookup"><span data-stu-id="a46ae-122">How to: Export a Positive Pay file</span></span>](finance-how-positive-pay.md) |
|<span data-ttu-id="a46ae-123">Exporteer betalingen vanuit het venster **Betalingsdagboek** naar een bankbestand dat u uploadt naar uw bank voor verwerking, inclusief EFT (electronic funds transfer) in Noord-Amerika.</span><span class="sxs-lookup"><span data-stu-id="a46ae-123">Export payments from the **Payment Journal** window to a bank file that you upload to your bank for processing, including EFT (electronic funds transfer) in North America.</span></span> |[<span data-ttu-id="a46ae-124">Procedure: Betalingen naar een bankbestand exporteren</span><span class="sxs-lookup"><span data-stu-id="a46ae-124">How to: Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  

## <a name="see-also"></a><span data-ttu-id="a46ae-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a46ae-125">See Also</span></span>
[<span data-ttu-id="a46ae-126">Betalingsverplichtingen beheren</span><span class="sxs-lookup"><span data-stu-id="a46ae-126">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="a46ae-127">Inkoop</span><span class="sxs-lookup"><span data-stu-id="a46ae-127">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="a46ae-128">Tegoeden beheren</span><span class="sxs-lookup"><span data-stu-id="a46ae-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="a46ae-129">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a46ae-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

