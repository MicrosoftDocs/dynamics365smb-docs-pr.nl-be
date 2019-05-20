---
title: Crediteuren beheren| Microsoft Docs
description: Overzicht van hoe u crediteuren (AP) beheert, inclusief leveranciersbetalingen, crediteuren, schuld en verschuldigd saldo.
services: project-madeira
documentationcenter: ''
author: bholtorf
manager: edupont
editor: ''
ms.service: dynamics365-business-central
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 04/01/2019
ms.author: bholtorf
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: f7556b204403f0abdb6361a0e1650b90e58810e1
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1238889"
---
# <a name="managing-payables"></a><span data-ttu-id="249b3-103">Betalingsverplichtingen beheren</span><span class="sxs-lookup"><span data-stu-id="249b3-103">Managing Payables</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="249b3-104">heeft alles wat u nodig hebt om uw betalingsverplichtingen efficiënt te beheren.</span><span class="sxs-lookup"><span data-stu-id="249b3-104">has what you need to effectively manage accounts payable.</span></span>  

## <a name="payments"></a><span data-ttu-id="249b3-105">Betalingen</span><span class="sxs-lookup"><span data-stu-id="249b3-105">Payments</span></span>
<span data-ttu-id="249b3-106">U kunt eenvoudig betalingen prioriteit geven, rekening houden met boetes voor late betalingen en kortingen voor tijdige betalingen verwerken.</span><span class="sxs-lookup"><span data-stu-id="249b3-106">It's easy to prioritize payments, account for penalties for overdue payments, and handle discounts for early payments.</span></span>

<span data-ttu-id="249b3-107">U kunt betalingen registreren in een diversendagboek en vervolgens cheques afdrukken voordat het betalingsdagboek wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="249b3-107">You can record payments in a general journal, and then print checks before posting the payment journal.</span></span>

<span data-ttu-id="249b3-108">U kunt betalingen vereffenen om facturen te sluiten wanneer u de betaling boekt of nadat u de betaling hebt geboekt.</span><span class="sxs-lookup"><span data-stu-id="249b3-108">You can apply payments to close invoices when you post the payment, or after you post the payment.</span></span> <span data-ttu-id="249b3-109">Met het veld **Vereffeningsmethode** dat is opgegeven voor de leverancier (op de **Leverancierskaart**), wordt bepaald of u de betaling handmatig of automatisch vereffend.</span><span class="sxs-lookup"><span data-stu-id="249b3-109">The **Application Method** specified for the vendor (on the **Vendor Card**) determines whether you apply the payment manually, or automatically.</span></span> <span data-ttu-id="249b3-110">U kunt transacties altijd handmatig vereffenen.</span><span class="sxs-lookup"><span data-stu-id="249b3-110">You can always apply transactions manually.</span></span> <span data-ttu-id="249b3-111">Als de vereffeningsmethode voor de leverancier echter is ingesteld op **Toepassen op oudste** en u geen document opgeeft waarmee de betaling wordt vereffend, wordt de betaling vereffend met de oudste open post van de leverancier.</span><span class="sxs-lookup"><span data-stu-id="249b3-111">However, if the application method for the vendor is **Apply to Oldest**, and you do not specify a document to apply the payment to, the payment is applied to the oldest open entry for the vendor.</span></span>

## <a name="suggest-vendor-payments"></a><span data-ttu-id="249b3-112">Leveranciersbetalingen voorstellen</span><span class="sxs-lookup"><span data-stu-id="249b3-112">Suggest Vendor Payments</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="249b3-113">heeft een functie die voorstellen kan doen voor betalingen aan leveranciers. Zo krijgt u bijvoorbeeld een bericht als de vervaldatum voor een betaling nadert of als voor een betaling een korting mogelijk is.</span><span class="sxs-lookup"><span data-stu-id="249b3-113">can suggest various payments to vendors, such as payments that will be due soon, or payments where a discount is available.</span></span> <span data-ttu-id="249b3-114">In het betalingsvoorstel kan een bedrag worden meegenomen dat u opgeeft als beschikbaar kapitaal, en geschiktheid voor contantkortingen.</span><span class="sxs-lookup"><span data-stu-id="249b3-114">The payment suggestion can consider an amount that you specify as available funds for payment, and eligibility for payment discounts.</span></span>

## <a name="issue-checks"></a><span data-ttu-id="249b3-115">Cheques uitgeven</span><span class="sxs-lookup"><span data-stu-id="249b3-115">Issue Checks</span></span>
<span data-ttu-id="249b3-116">Met [!INCLUDE[d365fin](includes/d365fin_md.md)] kunt u cheques elektronisch en handmatig uitgeven aan leveranciers.</span><span class="sxs-lookup"><span data-stu-id="249b3-116">[!INCLUDE[d365fin](includes/d365fin_md.md)] lets you issue checks to vendors manually and electronically.</span></span> <span data-ttu-id="249b3-117">Dit doet u beide op de pagina **Betalingsdagboeken**, waarin u cheques ook ongeldig kunt maken en chequeposten kunt bekijken.</span><span class="sxs-lookup"><span data-stu-id="249b3-117">You do both on the **Payment Journals** page, where you can also void checks and view check ledger entries.</span></span>

## <a name="export-payments-to-a-bank-file"></a><span data-ttu-id="249b3-118">Betalingen naar een bankbestand exporteren</span><span class="sxs-lookup"><span data-stu-id="249b3-118">Export Payments to a Bank File</span></span>
<span data-ttu-id="249b3-119">Wanneer u klaar bent om een leverancier te betalen, kunt u met behulp van de pagina **Betalingsdagboek** een bestand met de betalingsgegevens exporteren van de dagboekregels.</span><span class="sxs-lookup"><span data-stu-id="249b3-119">When you are ready to pay a vendor, from the **Payment Journal** page you can export a file with the payment information from the journal lines.</span></span> <span data-ttu-id="249b3-120">Vervolgens kunt u het bestand uploaden naar uw elektronische bank voor verwerking van de overboekingen.</span><span class="sxs-lookup"><span data-stu-id="249b3-120">You can then upload the file to your electronic bank to process the money transfers.</span></span>

<span data-ttu-id="249b3-121">Als u geen betalingsdagboekregel voor een geëxporteerde betaling wilt boeken, bijvoorbeeld omdat u op bevestiging wacht dat de transactie door de bank is verwerkt, kunt u de dagboekregel gewoon verwijderen.</span><span class="sxs-lookup"><span data-stu-id="249b3-121">If you do not want to post a payment journal line for an exported payment, for example because you are waiting for the bank to confirm the transaction, just delete the journal line.</span></span> <span data-ttu-id="249b3-122">Wanneer u later een betalingsdagboekregel maakt om het restbedrag op de factuur te betalen, bevat het veld **Totaal geëxporteerd bedrag** het gedeelte van het betalingsbedrag dat al is geëxporteerd.</span><span class="sxs-lookup"><span data-stu-id="249b3-122">Later, when you create a payment journal line to pay the remaining amount on the invoice, the **Total Exported Amount** field shows how much of the payment amount has already been exported.</span></span> <span data-ttu-id="249b3-123">U kunt ook gedetailleerde gegevens vinden over het geëxporteerde totaal door de knop **Krediettransferregisterposten** te kiezen.</span><span class="sxs-lookup"><span data-stu-id="249b3-123">Also, you can find detailed information about the exported total by choosing the **Credit Transfer Reg. Entries** button.</span></span>

<span data-ttu-id="249b3-124">Als u wacht met het boeken van betalingen totdat uw bank bevestigt dat transacties zijn verwerkt, kunt u op twee manieren voorkomen dat betalingen voor open documenten per ongeluk opnieuw worden geëxporteerd:</span><span class="sxs-lookup"><span data-stu-id="249b3-124">If you wait to post payments until after your bank confirms that it has processed transactions, there are two ways to avoid accidentally re-exporting payments for open documents:</span></span>  

* <span data-ttu-id="249b3-125">U kunt in een betalingsdagboek met voorgestelde betalingsregels sorteren op de kolom **Naar betalingsbestand geëxporteerd** of **Totaal geëxporteerd bedrag** en vervolgens betalingsvoorstellen verwijderen voor openstaande facturen waarvoor al betalingen zijn verricht en waarvoor u geen betalingen meer wilt verrichten.</span><span class="sxs-lookup"><span data-stu-id="249b3-125">In a payment journal with suggested payment lines, sort on either the **Exported to Payment File** or **Total Exported Amount** columns, and then delete payment suggestions for open invoices for which payments have already been made and you do not want to make payments for.</span></span>

    <span data-ttu-id="249b3-126">**Opmerking**: u moet deze kolommen mogelijk aan de lijst toevoegen.</span><span class="sxs-lookup"><span data-stu-id="249b3-126">**Note** You might have to add these columns to the list.</span></span> <span data-ttu-id="249b3-127">Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="249b3-127">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  
* <span data-ttu-id="249b3-128">Zo kunt u ook in de batchverwerking **Leveranciersbetalingen voorstellen**, waarmee u opgeeft welke betalingen in het betalingsdagboek moeten worden opgenomen, opgeven dat dagboekregels voor betalingen die al zijn geëxporteerd, niet moeten worden ingevoegd door het selectievakje **Geëxporteerde betalingen overslaan** te kiezen.</span><span class="sxs-lookup"><span data-stu-id="249b3-128">Alternatively, on the **Suggest Vendor Payments** batch job, where you specify the payments to include in the payment journal, you can specify not to insert journal lines for payments that have already been exported by choosing the **Skip Exported Payments** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="249b3-129">Zie ook</span><span class="sxs-lookup"><span data-stu-id="249b3-129">See Also</span></span>
[<span data-ttu-id="249b3-130">Betalingsmethoden</span><span class="sxs-lookup"><span data-stu-id="249b3-130">Payment Methods</span></span>](finance-payment-methods.md)  
[<span data-ttu-id="249b3-131">Financiën</span><span class="sxs-lookup"><span data-stu-id="249b3-131">Finance</span></span>](finance.md)  
<span data-ttu-id="249b3-132">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="249b3-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
