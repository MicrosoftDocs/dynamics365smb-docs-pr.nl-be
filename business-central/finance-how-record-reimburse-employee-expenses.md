---
title: Bedrijfsgerelateerde onkosten vastleggen en terugbetalen | Microsoft Docs
description: Boek onkosten van werknemers met het dagboek naar de rekening van de werknemer en boek later een betaling naar de bankrekening van de werknemer om bedrijfgerelateerde onkosten terug te betalen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 660cb4d9f2238bffeb1c7eaf49d5d70dbb654f45
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "934044"
---
# <a name="record-and-reimburse-employees-expenses"></a><span data-ttu-id="21c90-103">Kosten van werknemers registreren en terugbetalen</span><span class="sxs-lookup"><span data-stu-id="21c90-103">Record and Reimburse Employees' Expenses</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="21c90-104">ondersteunt transacties voor een werknemer op dezelfde manier als voor leveranciers.</span><span class="sxs-lookup"><span data-stu-id="21c90-104">supports transactions for employee in a similar way as for vendors.</span></span> <span data-ttu-id="21c90-105">Daarom zijn er werknemersboekingsgroepen om te zorgen dat werknemersposten worden geboekt naar de relevante rekeningen in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="21c90-105">Accordingly, employee posting groups exist to make sure that employee ledger entries are posted to the relevant accounts in the general ledger.</span></span>

> [!NOTE]  
> <span data-ttu-id="21c90-106">Werknemerstransacties kunnen alleen in de lokale valuta worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="21c90-106">Employee transactions can be posted in the local currency only.</span></span> <span data-ttu-id="21c90-107">Terugbetalingen aan werknemers ondersteunen geen kortingen en betalingstoleranties.</span><span class="sxs-lookup"><span data-stu-id="21c90-107">Reimbursement payments to employees do not support discounts and payment tolerances.</span></span>

<span data-ttu-id="21c90-108">Als medewerkers hun eigen geld uitgeven tijdens zakelijke activiteiten, kunt u de kosten boeken naar de rekening van de werknemer.</span><span class="sxs-lookup"><span data-stu-id="21c90-108">If employees spend their own money during business activities, you can post the expense to the employee's account.</span></span> <span data-ttu-id="21c90-109">Vervolgens kunt u de werknemer terugbetalen door een betaling te doen naar de bankrekening van de werknemer, net zoals u leveranciers betaalt.</span><span class="sxs-lookup"><span data-stu-id="21c90-109">Then you can reimburse the employee by making a payment to the employee's bank account, similarly to how you pay vendors.</span></span>

## <a name="to-record-an-employees-expense"></a><span data-ttu-id="21c90-110">Onkosten van een werknemer registreren</span><span class="sxs-lookup"><span data-stu-id="21c90-110">To record an employee's expense</span></span>
<span data-ttu-id="21c90-111">U boekt onkosten van een werknemer op de pagina **Diversendagboek**.</span><span class="sxs-lookup"><span data-stu-id="21c90-111">You post employees' expenses on the **General Journal** page.</span></span>
1. <span data-ttu-id="21c90-112">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële dagboeken** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="21c90-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="21c90-113">Open de relevante dagboekbatch.</span><span class="sxs-lookup"><span data-stu-id="21c90-113">Open the relevant general journal batch.</span></span> <span data-ttu-id="21c90-114">Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="21c90-114">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="21c90-115">Vul op een nieuwe dagboekregel de velden indien nodig in.</span><span class="sxs-lookup"><span data-stu-id="21c90-115">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="21c90-116">Herhaal stap 3 voor alle kosten die de werknemer heeft betaald.</span><span class="sxs-lookup"><span data-stu-id="21c90-116">Repeat step 3 for all the expenses that the employee has incurred.</span></span>

    > [!TIP]  
    > <span data-ttu-id="21c90-117">Als u meerdere onkostenregels boven één tegenrekeningsregel wilt invoeren voor de bankrekening van de werknemer, selecteert u het selectievakje **Salderingsbedrag voorstellen** op de regel voor uw batch op de pagina **Fin. dagboekbatches**.</span><span class="sxs-lookup"><span data-stu-id="21c90-117">If you want to enter multiple expense lines above one balance-account line for the employee's bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="21c90-118">Vervolgens wordt het veld **Bedrag** op de tegenrekeningsregel automatisch ingevuld met de waarde die nodig is om de onkosten in balans te brengen.</span><span class="sxs-lookup"><span data-stu-id="21c90-118">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the expenses.</span></span>
5. <span data-ttu-id="21c90-119">Kies de actie **Boeken** om de kosten op de rekening van de werknemer te registreren.</span><span class="sxs-lookup"><span data-stu-id="21c90-119">Choose the **Post** action to record the expenses on the employee's account.</span></span>

## <a name="to-reimburse-an-employee"></a><span data-ttu-id="21c90-120">Een werknemer terugbetalen</span><span class="sxs-lookup"><span data-stu-id="21c90-120">To reimburse an employee</span></span>
<span data-ttu-id="21c90-121">U betaalt werknemers terug door betalingen te boeken naar hun bankrekening op de pagina **Betalingsdagboek**.</span><span class="sxs-lookup"><span data-stu-id="21c90-121">You reimburse employees by posting payments to their bank account on the **Payment Journal** page.</span></span>
1. <span data-ttu-id="21c90-122">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsdagboeken** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="21c90-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="21c90-123">Open de relevante betalingsdagboekbatch.</span><span class="sxs-lookup"><span data-stu-id="21c90-123">Open the relevant payment journal batch.</span></span> <span data-ttu-id="21c90-124">Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="21c90-124">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="21c90-125">Vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="21c90-125">Fill in the fields as necessary.</span></span> <span data-ttu-id="21c90-126">Zie voor meer informatie [Betalingen doen](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="21c90-126">For more information, see [Making Payments](payables-make-payments.md).</span></span>
4. <span data-ttu-id="21c90-127">Of kies de actie **Werknemersbetalingen voorstellen** om automatisch dagboekregels in te voegen voor werknemersterugbetalingen die in behandeling zijn.</span><span class="sxs-lookup"><span data-stu-id="21c90-127">Alternatively, choose the **Suggest Employee Payment** action to automatically insert journal lines for pending employee reimbursements.</span></span>
5. <span data-ttu-id="21c90-128">Kies de actie **Boeken** om de terugbetaling te registreren.</span><span class="sxs-lookup"><span data-stu-id="21c90-128">Choose the **Post** action to register the reimbursement.</span></span>  

## <a name="to-reconcile-reimbursements-with-employee-ledger-entries"></a><span data-ttu-id="21c90-129">Terugbetalingen reconciliëren met werknemersposten</span><span class="sxs-lookup"><span data-stu-id="21c90-129">To reconcile reimbursements with employee ledger entries</span></span>
<span data-ttu-id="21c90-130">U vereffent werknemersbetalingen met de gerelateerde open werknemersposten op dezelfde manier als u dat doet voor leveranciersbetalingen, bijvoorbeeld op de pagina **Betalingsreconciliatiedagboek**, op basis van de gerelateerde bankafschriftposten.</span><span class="sxs-lookup"><span data-stu-id="21c90-130">You apply employee payments to their related open employee ledger entries in the same way as you do for vendor payments, for example on the **Payment Reconciliation Journal** page, based on the related bank statement entries.</span></span> <span data-ttu-id="21c90-131">Zie voor meer informatie [Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="21c90-131">For more information, see [Applying Payments Automatically and Reconciling Bank Accounts](receivables-apply-payments-auto-reconcile-bank-accounts.md).</span></span> <span data-ttu-id="21c90-132">U kunt ook handmatig vereffenen op de pagina **Werknemerposten**.</span><span class="sxs-lookup"><span data-stu-id="21c90-132">Alternatively, you can apply manually on the **Employee Ledger Entries** page.</span></span> <span data-ttu-id="21c90-133">Zie voor meer informatie het gerelateerde [Leveranciersbetalingen reconciliëren met het betalingsdagboek of vanuit leveranciersposten](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="21c90-133">For more information, see the related [Reconcile Vendor Payments with the Payment Journal or from Vendor Ledger Entries](payables-how-apply-purchase-transactions-manually.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="21c90-134">Zie ook</span><span class="sxs-lookup"><span data-stu-id="21c90-134">See Also</span></span>
[<span data-ttu-id="21c90-135">Transacties direct naar het grootboek boeken</span><span class="sxs-lookup"><span data-stu-id="21c90-135">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="21c90-136">Werken met diversendagboeken</span><span class="sxs-lookup"><span data-stu-id="21c90-136">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="21c90-137">Boekingen tegenboeken</span><span class="sxs-lookup"><span data-stu-id="21c90-137">Reverse Postings</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="21c90-138">Financiën</span><span class="sxs-lookup"><span data-stu-id="21c90-138">Finance</span></span>](finance.md)  
<span data-ttu-id="21c90-139">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="21c90-139">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
