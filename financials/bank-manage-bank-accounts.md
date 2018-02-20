---
title: Bankrekeningen beheren| Microsoft Docs
description: "U moet regelmatig bankposten in Financials reconciliëren met de gerelateerde banktransacties in uw bankrekeningen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 20ff1bad076bff8ce07716cfffc2fa5e05605bb2
ms.contentlocale: nl-be
ms.lasthandoff: 02/02/2018

---
# <a name="managing-bank-accounts"></a><span data-ttu-id="b4902-103">Bankrekeningen beheren</span><span class="sxs-lookup"><span data-stu-id="b4902-103">Managing Bank Accounts</span></span>
<span data-ttu-id="b4902-104">U moet met vaste intervallen uw bankposten reconciliëren in [!INCLUDE[d365fin](includes/d365fin_md.md)] met de gerelateerde banktransacties in bankrekeningen bij uw bank, en vervolgens het saldo boeken naar uw bankrekening.</span><span class="sxs-lookup"><span data-stu-id="b4902-104">At regular intervals, you must reconcile your bank ledger entries in [!INCLUDE[d365fin](includes/d365fin_md.md)] with the related bank transactions in bank accounts at your bank, and then post the balance to your bank account.</span></span> <span data-ttu-id="b4902-105">U kunt deze taak uitvoeren als onderdeel van de verwerking van betalingen op een bankafschrift in het **Betalingsreconciliatiedagboek**.</span><span class="sxs-lookup"><span data-stu-id="b4902-105">You can perform this task either as part of processing the payments represented on a bank statement in the **Payment Reconciliation Journal**.</span></span> <span data-ttu-id="b4902-106">U kunt de taak ook apart van betalingsverwerking uitvoeren in het venster **Bankreconciliatie**, dat chequeposten ondersteunt.</span><span class="sxs-lookup"><span data-stu-id="b4902-106">Alternatively, you can perform the task separately from payment processing, in the **Bank Acc. Reconciliation** window, which supports check ledger entries.</span></span> <span data-ttu-id="b4902-107">In beide gevallen vult u de vensters in door het bankafschrift te importeren in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="b4902-107">In both cases, you fill in the windows by importing the bank statement into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

<span data-ttu-id="b4902-108">Soms moet u bedragen overboeken tussen bankrekeningen in [!INCLUDE[d365fin](includes/d365fin_md.md)] om transfers bij uw bank weer te geven.</span><span class="sxs-lookup"><span data-stu-id="b4902-108">Sometimes, you need to transfer amounts between bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect transfers at your bank.</span></span> <span data-ttu-id="b4902-109">U voert deze taak in het venster **Dagboek** op verschillende manieren uit, afhankelijk van de valuta van de gelden.</span><span class="sxs-lookup"><span data-stu-id="b4902-109">You perform this task in the **General Journal** window, in different ways depending on the currency of the funds.</span></span>

<span data-ttu-id="b4902-110">Voordat u bankrekeningen kunt beheren, moet u elke bankrekening als bankrekeningkaart instellen.</span><span class="sxs-lookup"><span data-stu-id="b4902-110">Before you can manage bank accounts, you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="b4902-111">Daarnaast moet u elektronische services instellen die u kunt gebruiken voor de import van bankafschriften en de export van het betalingsbestand.</span><span class="sxs-lookup"><span data-stu-id="b4902-111">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="b4902-112">Zie voor meer informatie [Bankrekeningen instellen](bank-setup-banking.md).</span><span class="sxs-lookup"><span data-stu-id="b4902-112">For more information, see [Set Up Bank Accounts](bank-setup-banking.md).</span></span>

<span data-ttu-id="b4902-113">In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.</span><span class="sxs-lookup"><span data-stu-id="b4902-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="b4902-114">Als u dit wilt doen</span><span class="sxs-lookup"><span data-stu-id="b4902-114">To</span></span> | <span data-ttu-id="b4902-115">Zie</span><span class="sxs-lookup"><span data-stu-id="b4902-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="b4902-116">Bankrekeningen reconciliëren met betrekking tot betalingsverwerking in het venster **Betalingsreconciliatiedagboek**.</span><span class="sxs-lookup"><span data-stu-id="b4902-116">Reconcile bank accounts in connection with payment processing in the **Payment Reconciliation Journal** window.</span></span> |[<span data-ttu-id="b4902-117">Betalingen automatisch vereffenen en bankrekeningen reconciliëren</span><span class="sxs-lookup"><span data-stu-id="b4902-117">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="b4902-118">Bankrekeningen reconciliëren, inclusief chequeposten als afzonderlijke taak in het venster **Bankreconciliatie**.</span><span class="sxs-lookup"><span data-stu-id="b4902-118">Reconcile bank accounts, including check ledger entries, as a separate task in the **Bank Acc. Reconciliation** window.</span></span> |[<span data-ttu-id="b4902-119">Bankrekeningen apart reconciliëren</span><span class="sxs-lookup"><span data-stu-id="b4902-119">Reconcile Bank Accounts Separately</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="b4902-120">Transacties boeken tussen bankrekeningen in dezelfde valuta of in verschillende valuta's.</span><span class="sxs-lookup"><span data-stu-id="b4902-120">Post transfers between bank accounts in the same currency or in different currencies.</span></span> |[<span data-ttu-id="b4902-121">Bankfondsen overboeken</span><span class="sxs-lookup"><span data-stu-id="b4902-121">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a><span data-ttu-id="b4902-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b4902-122">See Also</span></span>
[<span data-ttu-id="b4902-123">Bankieren instellen</span><span class="sxs-lookup"><span data-stu-id="b4902-123">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="b4902-124">Tegoeden beheren</span><span class="sxs-lookup"><span data-stu-id="b4902-124">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="b4902-125">[Betalingsverplichtingen beheren](payables-manage-payables.md)  </span><span class="sxs-lookup"><span data-stu-id="b4902-125">[Managing Payables](payables-manage-payables.md)  </span></span>  
<span data-ttu-id="b4902-126">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b4902-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="b4902-127">Algemene bedrijfsfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="b4902-127">General Business Functionality</span></span>](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

