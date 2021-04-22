---
title: Bedrijfsgerelateerde onkosten vastleggen en terugbetalen | Microsoft Docs
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
ms.openlocfilehash: edef774738233890af240b20622cc40585d79116
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783834"
---
# <a name="record-and-reimburse-employees-expenses"></a><span data-ttu-id="ed39b-103">Kosten van werknemers registreren en terugbetalen</span><span class="sxs-lookup"><span data-stu-id="ed39b-103">Record and Reimburse Employees' Expenses</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="ed39b-104">ondersteunt transacties voor een werknemer op dezelfde manier als voor leveranciers.</span><span class="sxs-lookup"><span data-stu-id="ed39b-104">supports transactions for employee in a similar way as for vendors.</span></span> <span data-ttu-id="ed39b-105">Daarom zijn er werknemersboekingsgroepen om te zorgen dat werknemersposten worden geboekt naar de relevante rekeningen in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="ed39b-105">Accordingly, employee posting groups exist to make sure that employee ledger entries are posted to the relevant accounts in the general ledger.</span></span>

> [!NOTE]  
> <span data-ttu-id="ed39b-106">Werknemerstransacties kunnen alleen in de lokale valuta worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="ed39b-106">Employee transactions can be posted in the local currency only.</span></span> <span data-ttu-id="ed39b-107">Terugbetalingen aan werknemers ondersteunen geen kortingen en betalingstoleranties.</span><span class="sxs-lookup"><span data-stu-id="ed39b-107">Reimbursement payments to employees do not support discounts and payment tolerances.</span></span>

<span data-ttu-id="ed39b-108">Als medewerkers hun eigen geld uitgeven tijdens zakelijke activiteiten, kunt u de kosten boeken naar de rekening van de werknemer.</span><span class="sxs-lookup"><span data-stu-id="ed39b-108">If employees spend their own money during business activities, you can post the expense to the employee's account.</span></span> <span data-ttu-id="ed39b-109">Vervolgens kunt u de werknemer terugbetalen door een betaling te doen naar de bankrekening van de werknemer, net zoals u leveranciers betaalt.</span><span class="sxs-lookup"><span data-stu-id="ed39b-109">Then you can reimburse the employee by making a payment to the employee's bank account, similarly to how you pay vendors.</span></span>  

> [!TIP]
> <span data-ttu-id="ed39b-110">In dit artikel wordt uitgelegd hoe u de kosten in de boeken registreert en hoe u de werknemer vergoedt.</span><span class="sxs-lookup"><span data-stu-id="ed39b-110">This article explains how to record the expense in the books and how to reimburse the employee.</span></span> <span data-ttu-id="ed39b-111">Uw organisatie heeft mogelijk een portal of app waar medewerkers hun onkostendeclaraties kunnen indienen.</span><span class="sxs-lookup"><span data-stu-id="ed39b-111">Your organization may have a portal or app where employees can submit their expense reports.</span></span>

## <a name="to-record-an-employees-expense"></a><span data-ttu-id="ed39b-112">Onkosten van een werknemer registreren</span><span class="sxs-lookup"><span data-stu-id="ed39b-112">To record an employee's expense</span></span>
<span data-ttu-id="ed39b-113">U boekt onkosten van een werknemer op de pagina **Diversendagboek**.</span><span class="sxs-lookup"><span data-stu-id="ed39b-113">You post employees' expenses on the **General Journal** page.</span></span>
1. <span data-ttu-id="ed39b-114">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële dagboeken** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="ed39b-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="ed39b-115">Open de relevante dagboekbatch.</span><span class="sxs-lookup"><span data-stu-id="ed39b-115">Open the relevant general journal batch.</span></span> <span data-ttu-id="ed39b-116">Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ed39b-116">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="ed39b-117">Vul op een nieuwe dagboekregel de velden indien nodig in.</span><span class="sxs-lookup"><span data-stu-id="ed39b-117">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="ed39b-118">Herhaal stap 3 voor alle kosten die de werknemer heeft betaald.</span><span class="sxs-lookup"><span data-stu-id="ed39b-118">Repeat step 3 for all the expenses that the employee has incurred.</span></span>

    > [!TIP]  
    > <span data-ttu-id="ed39b-119">Als u meerdere onkostenregels boven één tegenrekeningsregel wilt invoeren voor de bankrekening van de werknemer, selecteert u het selectievakje **Salderingsbedrag voorstellen** op de regel voor uw batch op de pagina **Fin. dagboekbatches**.</span><span class="sxs-lookup"><span data-stu-id="ed39b-119">If you want to enter multiple expense lines above one balance-account line for the employee's bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="ed39b-120">Vervolgens wordt het veld **Bedrag** op de tegenrekeningsregel automatisch ingevuld met de waarde die nodig is om de onkosten in balans te brengen.</span><span class="sxs-lookup"><span data-stu-id="ed39b-120">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the expenses.</span></span>
5. <span data-ttu-id="ed39b-121">Kies de actie **Boeken** om de kosten op de rekening van de werknemer te registreren.</span><span class="sxs-lookup"><span data-stu-id="ed39b-121">Choose the **Post** action to record the expenses on the employee's account.</span></span>

## <a name="to-reimburse-an-employee"></a><span data-ttu-id="ed39b-122">Een werknemer terugbetalen</span><span class="sxs-lookup"><span data-stu-id="ed39b-122">To reimburse an employee</span></span>
<span data-ttu-id="ed39b-123">U betaalt werknemers terug door betalingen te boeken naar hun bankrekening op de pagina **Betalingsdagboek**.</span><span class="sxs-lookup"><span data-stu-id="ed39b-123">You reimburse employees by posting payments to their bank account on the **Payment Journal** page.</span></span>
1. <span data-ttu-id="ed39b-124">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsdagboeken** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="ed39b-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="ed39b-125">Open de relevante betalingsdagboekbatch.</span><span class="sxs-lookup"><span data-stu-id="ed39b-125">Open the relevant payment journal batch.</span></span> <span data-ttu-id="ed39b-126">Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ed39b-126">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="ed39b-127">Vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="ed39b-127">Fill in the fields as necessary.</span></span> <span data-ttu-id="ed39b-128">Zie voor meer informatie [Betalingen doen](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="ed39b-128">For more information, see [Making Payments](payables-make-payments.md).</span></span>
4. <span data-ttu-id="ed39b-129">Of kies de actie **Werknemersbetalingen voorstellen** om automatisch dagboekregels in te voegen voor werknemersterugbetalingen die in behandeling zijn.</span><span class="sxs-lookup"><span data-stu-id="ed39b-129">Alternatively, choose the **Suggest Employee Payment** action to automatically insert journal lines for pending employee reimbursements.</span></span>
5. <span data-ttu-id="ed39b-130">Kies de actie **Boeken** om de terugbetaling te registreren.</span><span class="sxs-lookup"><span data-stu-id="ed39b-130">Choose the **Post** action to register the reimbursement.</span></span>  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a><span data-ttu-id="ed39b-131">Terugbetalingen reconciliëren met werknemersposten</span><span class="sxs-lookup"><span data-stu-id="ed39b-131">To reconcile reimbursements with employee ledger entries</span></span>
<span data-ttu-id="ed39b-132">U vereffent werknemersbetalingen met de gerelateerde open werknemersposten op dezelfde manier als u dat doet voor leveranciersbetalingen, bijvoorbeeld op de pagina **Betalingsreconciliatiedagboek**, op basis van de gerelateerde bankafschriftposten.</span><span class="sxs-lookup"><span data-stu-id="ed39b-132">You apply employee payments to their related open employee ledger entries in the same way as you do for vendor payments, for example on the **Payment Reconciliation Journal** page, based on the related bank statement entries.</span></span> <span data-ttu-id="ed39b-133">Zie voor meer informatie [Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="ed39b-133">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span> <span data-ttu-id="ed39b-134">U kunt ook handmatig vereffenen op de pagina **Werknemerposten**.</span><span class="sxs-lookup"><span data-stu-id="ed39b-134">Alternatively, you can apply manually on the **Employee Ledger Entries** page.</span></span> <span data-ttu-id="ed39b-135">Zie voor meer informatie het gerelateerde [Leveranciersbetalingen reconciliëren met het betalingsdagboek of vanuit leveranciersposten](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="ed39b-135">For more information, see the related [Reconcile Vendor Payments with the Payment Journal or from Vendor Ledger Entries](payables-how-apply-purchase-transactions-manually.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="ed39b-136">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ed39b-136">See Also</span></span>
[<span data-ttu-id="ed39b-137">Transacties direct naar het grootboek boeken</span><span class="sxs-lookup"><span data-stu-id="ed39b-137">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="ed39b-138">Werken met diversendagboeken</span><span class="sxs-lookup"><span data-stu-id="ed39b-138">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="ed39b-139">Journaalboekingen tegenboeken en ontvangsten/zendingen ongedaan maken</span><span class="sxs-lookup"><span data-stu-id="ed39b-139">Reverse Journal Postings and Undo Receipts/Shipments</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="ed39b-140">Financiën</span><span class="sxs-lookup"><span data-stu-id="ed39b-140">Finance</span></span>](finance.md)  
<span data-ttu-id="ed39b-141">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ed39b-141">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]