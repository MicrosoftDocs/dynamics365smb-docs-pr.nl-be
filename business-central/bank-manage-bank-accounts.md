---
title: Bankrekeningen beheren| Microsoft Docs
description: U moet regelmatig bankposten reconciliëren met de gerelateerde banktransacties in uw bankrekeningen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 62b2bf8987146a69d17bd343f88d31d60a205ffb
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816758"
---
# <a name="managing-bank-accounts"></a><span data-ttu-id="87533-103">Bankrekeningen beheren</span><span class="sxs-lookup"><span data-stu-id="87533-103">Managing Bank Accounts</span></span>
<span data-ttu-id="87533-104">U moet met vaste intervallen uw bankposten reconciliëren in [!INCLUDE[d365fin](includes/d365fin_md.md)] met de gerelateerde banktransacties in bankrekeningen bij uw bank, en vervolgens het saldo boeken naar uw bankrekening.</span><span class="sxs-lookup"><span data-stu-id="87533-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="87533-105">U kunt deze taak uitvoeren als onderdeel van de verwerking van betalingen op een bankafschrift in het **Betalingsreconciliatiedagboek**.</span><span class="sxs-lookup"><span data-stu-id="87533-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="87533-106">U kunt de taak ook apart van de betalingsverwerking uitvoeren op de pagina **Bankreconciliatie**, waar u bankafschriftregels in het linkerdeelvenster reconcilieert met uw interne bankposten in het rechterdeelvenster.</span><span class="sxs-lookup"><span data-stu-id="87533-106">Alternatively, you can perform the task separately from payment processing, on the **Bank Acc. Reconciliation** page where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="87533-107">Op beide pagina's kunt u de bankafschriftinformatie invullen door een bestand of een feed te importeren en kunt u automatische afstemmingsvoorstellen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="87533-107">In both pages, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="87533-108">In Noord-Amerikaanse versies kunt u bankreconciliatie ook uitvoeren op de pagina **Werkblad bankreconciliatie**, dat geschikter is voor cheques en borgsommen, maar geen importeren van bankafschriftbestanden biedt.</span><span class="sxs-lookup"><span data-stu-id="87533-108">In North American versions, you can also perform bank reconciliation on the **Bank Rec. Worksheet** page, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="87533-109">Als u deze pagina wilt gebruiken in plaats van de pagina **Bankreconciliatie**, schakelt u het veld **Bankreconciliatie met automatische afstemming** uit op de pagina **Boekhoudinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="87533-109">To use this page instead of the **Bank Acc. Reconciliation** page, deselect the **Bank Recon. with Auto. Match** field on the **General Ledger Setup** page.</span></span> <span data-ttu-id="87533-110">Zie voor meer informatie het gedeelte "Bankrekeningen reconciliëren" onder Lokale functionaliteit voor de Verenigde Staten.</span><span class="sxs-lookup"><span data-stu-id="87533-110">For more information, see the "Reconcile Bank Accounts" section under United States Local Functionality.</span></span>

<span data-ttu-id="87533-111">Soms moet u bedragen overboeken tussen bankrekeningen in [!INCLUDE[d365fin](includes/d365fin_md.md)] om transfers bij uw bank weer te geven.</span><span class="sxs-lookup"><span data-stu-id="87533-111">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="87533-112">U voert deze taak op de pagina **Dagboek** op verschillende manieren uit, afhankelijk van de valuta van de gelden.</span><span class="sxs-lookup"><span data-stu-id="87533-112">You perform this task on the **General Journal** page, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="87533-113">Voordat u bankrekeningen kunt beheren, moet u elke bankrekening als bankrekeningkaart instellen.</span><span class="sxs-lookup"><span data-stu-id="87533-113">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="87533-114">Daarnaast moet u elektronische services instellen die u kunt gebruiken voor de import van bankafschriften en de export van het betalingsbestand.</span><span class="sxs-lookup"><span data-stu-id="87533-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="87533-115">Zie voor meer informatie [Bankrekeningen instellen](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="87533-115">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="87533-116">In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.</span><span class="sxs-lookup"><span data-stu-id="87533-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="87533-117">Als u dit wilt doen</span><span class="sxs-lookup"><span data-stu-id="87533-117">To</span></span> | <span data-ttu-id="87533-118">Zie</span><span class="sxs-lookup"><span data-stu-id="87533-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="87533-119">Bankrekeningen reconciliëren met betrekking tot betalingsverwerking op de pagina **Betalingsreconciliatiedagboek**.</span><span class="sxs-lookup"><span data-stu-id="87533-119">Reconcile bank accounts in connection with payment processing on the **Payment Reconciliation Journal** page.</span></span> |[<span data-ttu-id="87533-120">Betalingen automatisch vereffenen en bankrekeningen reconciliëren</span><span class="sxs-lookup"><span data-stu-id="87533-120">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="87533-121">Bankrekeningen reconciliëren, inclusief chequeposten als afzonderlijke taak op de pagina **Bankreconciliatie**.</span><span class="sxs-lookup"><span data-stu-id="87533-121">Reconcile bank accounts, including check ledger entries, as a separate task on the **Bank Acc. Reconciliation** page.</span></span> |[<span data-ttu-id="87533-122">Bankrekeningen apart reconciliëren</span><span class="sxs-lookup"><span data-stu-id="87533-122">Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="87533-123">Transacties boeken tussen bankrekeningen in dezelfde valuta of in verschillende valuta's.</span><span class="sxs-lookup"><span data-stu-id="87533-123">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="87533-124">Bankfondsen overboeken</span><span class="sxs-lookup"><span data-stu-id="87533-124">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="87533-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="87533-125">See Also</span></span>
[<span data-ttu-id="87533-126">Bankieren instellen</span><span class="sxs-lookup"><span data-stu-id="87533-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="87533-127">Tegoeden beheren</span><span class="sxs-lookup"><span data-stu-id="87533-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="87533-128">[Betalingsverplichtingen beheren](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="87533-128">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="87533-129">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="87533-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="87533-130">Algemene bedrijfsfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="87533-130">General Business Functionality</span></span>](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 
