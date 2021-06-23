---
title: Bedrijfsgerelateerde onkosten van werknemers vastleggen en terugbetalen
description: Boek onkosten van werknemers met het dagboek naar de rekening van de werknemer en boek later een betaling naar de bankrekening van de werknemer om bedrijfgerelateerde onkosten terug te betalen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: dd4ce755e3414f19ae501c1d437f3e1d78d565a1
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184411"
---
# <a name="record-and-reimburse-employees-expenses"></a><span data-ttu-id="82404-103">Kosten van werknemers registreren en terugbetalen</span><span class="sxs-lookup"><span data-stu-id="82404-103">Record and Reimburse Employees' Expenses</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="82404-104">ondersteunt transacties voor werknemers op dezelfde manier als voor leveranciers.</span><span class="sxs-lookup"><span data-stu-id="82404-104">supports transactions for employees in a similar way as for vendors.</span></span> <span data-ttu-id="82404-105">Daarom zijn er werknemersboekingsgroepen om te zorgen dat werknemersposten worden geboekt naar de relevante rekeningen in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="82404-105">Accordingly, employee posting groups exist to make sure that employee ledger entries are posted to the relevant accounts in the general ledger.</span></span>

> [!NOTE]  
> <span data-ttu-id="82404-106">Werknemerstransacties kunnen alleen in de lokale valuta worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="82404-106">Employee transactions can be posted in the local currency only.</span></span> <span data-ttu-id="82404-107">Terugbetalingen aan werknemers ondersteunen geen kortingen en betalingstoleranties.</span><span class="sxs-lookup"><span data-stu-id="82404-107">Reimbursement payments to employees do not support discounts and payment tolerances.</span></span>

<span data-ttu-id="82404-108">Als medewerkers hun eigen geld uitgeven tijdens zakelijke activiteiten, kunt u de kosten boeken naar de rekening van de werknemer.</span><span class="sxs-lookup"><span data-stu-id="82404-108">If employees spend their own money during business activities, you can post the expense to the employee's account.</span></span> <span data-ttu-id="82404-109">Vervolgens kunt u de werknemer terugbetalen door een betaling te doen naar de bankrekening van de werknemer, net zoals u leveranciers betaalt.</span><span class="sxs-lookup"><span data-stu-id="82404-109">Then you can reimburse the employee by making a payment to the employee's bank account, similarly to how you pay vendors.</span></span>  

> [!TIP]
> <span data-ttu-id="82404-110">In dit artikel wordt uitgelegd hoe u de kosten in de boeken registreert en hoe u de werknemer vergoedt.</span><span class="sxs-lookup"><span data-stu-id="82404-110">This article explains how to record the expense in the books and how to reimburse the employee.</span></span> <span data-ttu-id="82404-111">Uw organisatie heeft mogelijk een portal of app waar medewerkers hun onkostendeclaraties kunnen indienen.</span><span class="sxs-lookup"><span data-stu-id="82404-111">Your organization may have a portal or app where employees can submit their expense reports.</span></span>

<span data-ttu-id="82404-112">[!INCLUDE [prod_short](includes/prod_short.md)] is flexibel genoeg voor veel verschillende praktijken.</span><span class="sxs-lookup"><span data-stu-id="82404-112">[!INCLUDE [prod_short](includes/prod_short.md)] is flexible enough to suit many different practices.</span></span> <span data-ttu-id="82404-113">De exacte rekeningnummers die moeten worden gebruikt, zijn afhankelijk van de configuratie en processen van uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="82404-113">The exact account numbers to use depends on your organization's configuration and processes.</span></span>  

## <a name="to-record-an-employees-expense"></a><span data-ttu-id="82404-114">Onkosten van een werknemer registreren</span><span class="sxs-lookup"><span data-stu-id="82404-114">To record an employee's expense</span></span>

<span data-ttu-id="82404-115">U boekt onkosten van een werknemer op de pagina **Diversendagboek**.</span><span class="sxs-lookup"><span data-stu-id="82404-115">You post employees' expenses on the **General Journal** page.</span></span>

1. <span data-ttu-id="82404-116">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële dagboeken** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="82404-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="82404-117">Open de relevante dagboekbatch.</span><span class="sxs-lookup"><span data-stu-id="82404-117">Open the relevant general journal batch.</span></span> <span data-ttu-id="82404-118">Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="82404-118">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="82404-119">Vul op een nieuwe dagboekregel de velden indien nodig in.</span><span class="sxs-lookup"><span data-stu-id="82404-119">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="82404-120">Herhaal stap 3 voor alle kosten die de werknemer heeft betaald.</span><span class="sxs-lookup"><span data-stu-id="82404-120">Repeat step 3 for all the expenses that the employee has incurred.</span></span>

    > [!TIP]  
    > <span data-ttu-id="82404-121">Als u meerdere onkostenregels boven één tegenrekeningsregel wilt invoeren voor de bankrekening van de werknemer, selecteert u het selectievakje **Salderingsbedrag voorstellen** op de regel voor uw batch op de pagina **Fin. dagboekbatches**.</span><span class="sxs-lookup"><span data-stu-id="82404-121">If you want to enter multiple expense lines above one balance-account line for the employee's bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="82404-122">Vervolgens wordt het veld **Bedrag** op de tegenrekeningsregel automatisch ingevuld met de waarde die nodig is om de onkosten in balans te brengen.</span><span class="sxs-lookup"><span data-stu-id="82404-122">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the expenses.</span></span>
5. <span data-ttu-id="82404-123">Kies de actie **Boeken** om de kosten op de rekening van de werknemer te registreren.</span><span class="sxs-lookup"><span data-stu-id="82404-123">Choose the **Post** action to record the expenses on the employee's account.</span></span>

## <a name="to-reimburse-an-employee"></a><span data-ttu-id="82404-124">Een werknemer terugbetalen</span><span class="sxs-lookup"><span data-stu-id="82404-124">To reimburse an employee</span></span>

<span data-ttu-id="82404-125">U betaalt werknemers terug door betalingen te boeken naar hun bankrekening op de pagina **Betalingsdagboek**.</span><span class="sxs-lookup"><span data-stu-id="82404-125">You reimburse employees by posting payments to their bank account on the **Payment Journal** page.</span></span>  

1. <span data-ttu-id="82404-126">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsdagboeken** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="82404-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="82404-127">Open de relevante betalingsdagboekbatch.</span><span class="sxs-lookup"><span data-stu-id="82404-127">Open the relevant payment journal batch.</span></span> <span data-ttu-id="82404-128">Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="82404-128">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="82404-129">Vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="82404-129">Fill in the fields as necessary.</span></span> <span data-ttu-id="82404-130">Zie voor meer informatie [Betalingen doen](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="82404-130">For more information, see [Making Payments](payables-make-payments.md).</span></span>
4. <span data-ttu-id="82404-131">Of kies de actie **Werknemersbetalingen voorstellen** om automatisch dagboekregels in te voegen voor werknemersterugbetalingen die in behandeling zijn.</span><span class="sxs-lookup"><span data-stu-id="82404-131">Alternatively, choose the **Suggest Employee Payment** action to automatically insert journal lines for pending employee reimbursements.</span></span>
5. <span data-ttu-id="82404-132">Kies de actie **Boeken** om de terugbetaling te registreren.</span><span class="sxs-lookup"><span data-stu-id="82404-132">Choose the **Post** action to register the reimbursement.</span></span>  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a><span data-ttu-id="82404-133">Terugbetalingen reconciliëren met werknemersposten</span><span class="sxs-lookup"><span data-stu-id="82404-133">To reconcile reimbursements with employee ledger entries</span></span>

<span data-ttu-id="82404-134">U vereffent werknemersbetalingen met de gerelateerde open werknemersposten op dezelfde manier als u dat doet voor leveranciersbetalingen, bijvoorbeeld op de pagina **Betalingsreconciliatiedagboek**, op basis van de gerelateerde bankafschriftposten.</span><span class="sxs-lookup"><span data-stu-id="82404-134">You apply employee payments to their related open employee ledger entries in the same way as you do for vendor payments, for example on the **Payment Reconciliation Journal** page, based on the related bank statement entries.</span></span> <span data-ttu-id="82404-135">Zie voor meer informatie [Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="82404-135">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span> <span data-ttu-id="82404-136">U kunt ook handmatig vereffenen op de pagina **Werknemerposten**.</span><span class="sxs-lookup"><span data-stu-id="82404-136">Alternatively, you can apply manually on the **Employee Ledger Entries** page.</span></span> <span data-ttu-id="82404-137">Zie voor meer informatie het gerelateerde [Leveranciersbetalingen reconciliëren met het betalingsdagboek of vanuit leveranciersposten](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="82404-137">For more information, see the related [Reconcile Vendor Payments with the Payment Journal or from Vendor Ledger Entries](payables-how-apply-purchase-transactions-manually.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="82404-138">Zie ook</span><span class="sxs-lookup"><span data-stu-id="82404-138">See Also</span></span>

[<span data-ttu-id="82404-139">Transacties direct naar het grootboek boeken</span><span class="sxs-lookup"><span data-stu-id="82404-139">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="82404-140">Werken met diversendagboeken</span><span class="sxs-lookup"><span data-stu-id="82404-140">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="82404-141">Journaalboekingen tegenboeken en ontvangsten/zendingen ongedaan maken</span><span class="sxs-lookup"><span data-stu-id="82404-141">Reverse Journal Postings and Undo Receipts/Shipments</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="82404-142">Financiën</span><span class="sxs-lookup"><span data-stu-id="82404-142">Finance</span></span>](finance.md)  
<span data-ttu-id="82404-143">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="82404-143">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]