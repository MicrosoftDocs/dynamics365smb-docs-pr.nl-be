---
title: Bankrekeningen beheren| Microsoft Docs
description: "U moet regelmatig bankposten reconciliëren met de gerelateerde banktransacties in uw bankrekeningen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f3733c3ec0048171294aae51dcfac0c2ecdc9e72
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="managing-bank-accounts"></a><span data-ttu-id="66c70-103">Bankrekeningen beheren</span><span class="sxs-lookup"><span data-stu-id="66c70-103">Managing Bank Accounts</span></span>
<span data-ttu-id="66c70-104">U moet met vaste intervallen uw bankposten reconciliëren in [!INCLUDE[d365fin](includes/d365fin_md.md)] met de gerelateerde banktransacties in bankrekeningen bij uw bank, en vervolgens het saldo boeken naar uw bankrekening.</span><span class="sxs-lookup"><span data-stu-id="66c70-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="66c70-105">U kunt deze taak uitvoeren als onderdeel van de verwerking van betalingen op een bankafschrift in het **Betalingsreconciliatiedagboek**.</span><span class="sxs-lookup"><span data-stu-id="66c70-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="66c70-106">U kunt de taak ook apart van de betalingsverwerking uitvoeren in het venster **Bankreconciliatie**, waar u bankafschriftregels in het linkerdeelvenster reconcilieert met uw interne bankposten in het rechterdeelvenster.</span><span class="sxs-lookup"><span data-stu-id="66c70-106">Alternatively, you can perform the task separately from payment processing, in the **Bank Acc. Reconciliation** window where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="66c70-107">In beide vensters kunt u de bankafschriftinformatie invullen door een bestand of een feed te importeren en kunt u automatische afstemmingsvoorstellen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="66c70-107">In both windows, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="66c70-108">In Noord-Amerikaanse versies kunt u bankreconciliatie ook uitvoeren in het venster **Werkblad bankreconciliatie**, dat geschikter is voor cheques en borgsommen, maar geen importeren van bankafschriftbestanden biedt.</span><span class="sxs-lookup"><span data-stu-id="66c70-108">In North American versions, you can also perform bank reconciliation in the **Bank Rec. Worksheet** window, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="66c70-109">Als u dit venster wilt gebruiken in plaats van het venster **Bankreconciliatie**, schakelt u het veld **Bankreconciliatie met automatische afstemming** uit in het venster **Boekhoudinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="66c70-109">To use this window instead of the **Bank Acc. Reconciliation** window, deselect the **Bank Recon. with Auto. Match** field in the **General Ledger Setup** window.</span></span> <span data-ttu-id="66c70-110">Zie voor meer informatie het gedeelte "Bankrekeningen reconciliëren" onder Lokale functionaliteit voor de Verenigde Staten.</span><span class="sxs-lookup"><span data-stu-id="66c70-110">For more information, see the "Reconcile Bank Accounts" section under United States Local Functionality.</span></span>

<span data-ttu-id="66c70-111">Soms moet u bedragen overboeken tussen bankrekeningen in [!INCLUDE[d365fin](includes/d365fin_md.md)] om transfers bij uw bank weer te geven.</span><span class="sxs-lookup"><span data-stu-id="66c70-111">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="66c70-112">U voert deze taak in het venster **Dagboek** op verschillende manieren uit, afhankelijk van de valuta van de gelden.</span><span class="sxs-lookup"><span data-stu-id="66c70-112">You perform this task in the **General Journal** window, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="66c70-113">Voordat u bankrekeningen kunt beheren, moet u elke bankrekening als bankrekeningkaart instellen.</span><span class="sxs-lookup"><span data-stu-id="66c70-113">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="66c70-114">Daarnaast moet u elektronische services instellen die u kunt gebruiken voor de import van bankafschriften en de export van het betalingsbestand.</span><span class="sxs-lookup"><span data-stu-id="66c70-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="66c70-115">Zie voor meer informatie [Bankrekeningen instellen](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="66c70-115">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="66c70-116">In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.</span><span class="sxs-lookup"><span data-stu-id="66c70-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="66c70-117">Als u dit wilt doen</span><span class="sxs-lookup"><span data-stu-id="66c70-117">To</span></span> | <span data-ttu-id="66c70-118">Zie</span><span class="sxs-lookup"><span data-stu-id="66c70-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="66c70-119">Bankrekeningen reconciliëren met betrekking tot betalingsverwerking in het venster **Betalingsreconciliatiedagboek**.</span><span class="sxs-lookup"><span data-stu-id="66c70-119">Reconcile bank accounts in connection with payment processing in the **Payment Reconciliation Journal** window.</span></span> |[<span data-ttu-id="66c70-120">Betalingen automatisch vereffenen en bankrekeningen reconciliëren</span><span class="sxs-lookup"><span data-stu-id="66c70-120">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="66c70-121">Bankrekeningen reconciliëren, inclusief chequeposten als afzonderlijke taak in het venster **Bankreconciliatie**.</span><span class="sxs-lookup"><span data-stu-id="66c70-121">Reconcile bank accounts, including check ledger entries, as a separate task in the **Bank Acc. Reconciliation** window.</span></span> |[<span data-ttu-id="66c70-122">Bankrekeningen apart reconciliëren</span><span class="sxs-lookup"><span data-stu-id="66c70-122">Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="66c70-123">Transacties boeken tussen bankrekeningen in dezelfde valuta of in verschillende valuta's.</span><span class="sxs-lookup"><span data-stu-id="66c70-123">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="66c70-124">Bankfondsen overboeken</span><span class="sxs-lookup"><span data-stu-id="66c70-124">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="66c70-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="66c70-125">See Also</span></span>
[<span data-ttu-id="66c70-126">Bankieren instellen</span><span class="sxs-lookup"><span data-stu-id="66c70-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="66c70-127">Tegoeden beheren</span><span class="sxs-lookup"><span data-stu-id="66c70-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="66c70-128">[Betalingsverplichtingen beheren](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="66c70-128">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="66c70-129">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="66c70-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="66c70-130">Algemene bedrijfsfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="66c70-130">General Business Functionality</span></span>](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

