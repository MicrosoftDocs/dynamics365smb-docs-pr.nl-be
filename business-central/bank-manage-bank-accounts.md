---
title: Bankrekeningen beheren| Microsoft Docs
description: U moet regelmatig bankposten reconciliëren met de gerelateerde banktransacties in uw bankrekeningen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c36e906c87cb17acb85d8cde32fdc51ee501469d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5381743"
---
# <a name="reconciling-bank-accounts"></a><span data-ttu-id="d42be-103">Bankrekeningen reconciliëren</span><span class="sxs-lookup"><span data-stu-id="d42be-103">Reconciling Bank Accounts</span></span>

<span data-ttu-id="d42be-104">Voor al uw bankrekeningen moet op gezette tijden een bankafstemming worden uitgevoerd om ervoor te zorgen dat de kasgegevens van het bedrijf correct zijn.</span><span class="sxs-lookup"><span data-stu-id="d42be-104">A bank reconciliation should be completed at regular intervals for all your bank accounts to ensure that the company's cash records are correct.</span></span> <span data-ttu-id="d42be-105">U doet dit door boekingen op uw interne bankrekeningen te vergelijken en af te stemmen met banktransacties bij uw bank en vervolgens de saldi op uw interne bankrekeningen te boeken om totalen beschikbaar te stellen voor financiële managers.</span><span class="sxs-lookup"><span data-stu-id="d42be-105">You do this by comparing and matching entries in your internal bank accounts with bank transactions at your bank, and then posting the balances to your internal bank accounts to make totals available to finance managers.</span></span> <span data-ttu-id="d42be-106">Bankafstemming is ook een praktische manier om ontbrekende betalingen en boekhoudfouten te ontdekken en op te lossen.</span><span class="sxs-lookup"><span data-stu-id="d42be-106">Bank reconciliation is also a practical way to discover and resolve missing payments and bookkeeping errors.</span></span>

<span data-ttu-id="d42be-107">U kunt de taak uitvoeren op de pagina **Bankreconciliatie**, waar u bankafschriftregels in het linkerdeelvenster afstemt met uw interne bankposten in het rechterdeelvenster.</span><span class="sxs-lookup"><span data-stu-id="d42be-107">You can perform the task on the **Bank Acc. Reconciliation** page where you match (reconcile) bank statement lines in the left-hand pane with your internal bank account ledger entries in the right-hand pane.</span></span> <span data-ttu-id="d42be-108">U kunt deze taak ook uitvoeren op de pagina **Betalingsreconciliatiedagboek** als onderdeel van de verwerking van betalingen op een bankafschrift.</span><span class="sxs-lookup"><span data-stu-id="d42be-108">Alternatively, you can perform this task on the **Payment Reconciliation Journal** page as part of processing the payments that are represented on a bank statement.</span></span> <span data-ttu-id="d42be-109">Op beide pagina's kunt u de bankafschriftinformatie invullen door een bestand of een feed te importeren en kunt u automatische afstemmingsvoorstellen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="d42be-109">On both pages, you can fill in the bank statement information by importing a file or feed and you can use automatic matching suggestions.</span></span>

> [!NOTE]  
> <span data-ttu-id="d42be-110">In de Noord-Amerikaanse versies kunt u bankreconciliatie ook uitvoeren op de pagina **Werkblad bankreconciliatie**, dat geschikter is voor cheques en borgsommen, maar geen importeren van bankafschriftbestanden biedt.</span><span class="sxs-lookup"><span data-stu-id="d42be-110">In the North American versions, you can also perform bank reconciliation on the **Bank Rec. Worksheet** page, which is better suited for checks and deposits but does not offer import of bank statement files.</span></span> <span data-ttu-id="d42be-111">Als u deze pagina wilt gebruiken in plaats van de pagina **Bankreconciliatie**, schakelt u het veld **Bankreconciliatie met automatische afstemming** uit op de pagina **Boekhoudinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="d42be-111">To use this page instead of the **Bank Acc. Reconciliation** page, deselect the **Bank Recon. with Auto. Match** field on the **General Ledger Setup** page.</span></span> <span data-ttu-id="d42be-112">Zie voor meer informatie [Bankrekeningen reconciliëren](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) onder Lokale functionaliteit voor de Verenigde Staten.</span><span class="sxs-lookup"><span data-stu-id="d42be-112">For more information, see [Reconcile Bank Accounts](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) under United States Local Functionality.</span></span>

<span data-ttu-id="d42be-113">Voordat u uw bankrekeningen kunt beheren in [!INCLUDE[prod_short](includes/prod_short.md)], moet u elke bankrekening als bankrekeningkaart instellen.</span><span class="sxs-lookup"><span data-stu-id="d42be-113">Before you can manage your bank accounts within [!INCLUDE[prod_short](includes/prod_short.md)], you must set each bank account up as a bank account card.</span></span> <span data-ttu-id="d42be-114">Daarnaast moet u elektronische services instellen die u kunt gebruiken voor de import van bankafschriften en de export van het betalingsbestand.</span><span class="sxs-lookup"><span data-stu-id="d42be-114">In addition, you must set up electronic services that you may use for bank statement import and payment file export.</span></span> <span data-ttu-id="d42be-115">Zie [Bankieren instellen](bank-setup-banking.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d42be-115">For more information, see [Setting Up Banking](bank-setup-banking.md).</span></span>

<span data-ttu-id="d42be-116">De volgende tabel beschrijft een reeks taken, met koppelingen naar de onderwerpen waarin deze worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="d42be-116">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

| <span data-ttu-id="d42be-117">Als u dit wilt doen:</span><span class="sxs-lookup"><span data-stu-id="d42be-117">To</span></span> | <span data-ttu-id="d42be-118">Zie</span><span class="sxs-lookup"><span data-stu-id="d42be-118">See</span></span> |
| --- | --- |
| <span data-ttu-id="d42be-119">Bankrekeningen reconciliëren als afzonderlijke taak op de pagina **Bankreconciliatie**.</span><span class="sxs-lookup"><span data-stu-id="d42be-119">Reconcile bank accounts as a separate task on the **Bank Acc. Reconciliation** page.</span></span> |[<span data-ttu-id="d42be-120">Bankrekeningen afstemmen</span><span class="sxs-lookup"><span data-stu-id="d42be-120">Reconcile Bank Accounts</span></span>](bank-how-reconcile-bank-accounts-separately.md) |
| <span data-ttu-id="d42be-121">Bankrekeningen reconciliëren met betrekking tot betalingsverwerking op de pagina **Betalingsreconciliatiedagboek**.</span><span class="sxs-lookup"><span data-stu-id="d42be-121">Reconcile bank accounts in connection with payment processing on the **Payment Reconciliation Journal** page.</span></span> |[<span data-ttu-id="d42be-122">Betalingen automatisch vereffenen en bankrekeningen reconciliëren</span><span class="sxs-lookup"><span data-stu-id="d42be-122">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

> [!TIP]
> <span data-ttu-id="d42be-123">Gebruik bankreconciliatie om te controleren of uw boeken up-to-date zijn en boek de reconciliatie pas als u er tevreden mee bent.</span><span class="sxs-lookup"><span data-stu-id="d42be-123">Use bank reconciliation to help verify that your books are up-to-date, and do not post the reconciliation until you are satisfied with the reconciliation.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="d42be-124">Zie Gerelateerde training op [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="d42be-124">See Related Training at [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="d42be-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d42be-125">See Also</span></span>

[<span data-ttu-id="d42be-126">Bankieren instellen</span><span class="sxs-lookup"><span data-stu-id="d42be-126">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="d42be-127">Bankrekeningen afstemmen</span><span class="sxs-lookup"><span data-stu-id="d42be-127">Reconcile Bank Accounts</span></span>](bank-how-reconcile-bank-accounts-separately.md)  
[<span data-ttu-id="d42be-128">Betalingen automatisch vereffenen en bankrekeningen reconciliëren</span><span class="sxs-lookup"><span data-stu-id="d42be-128">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[<span data-ttu-id="d42be-129">Bankfondsen overboeken</span><span class="sxs-lookup"><span data-stu-id="d42be-129">Transfer Bank Funds</span></span>](bank-how-transfer-bank-funds.md)  
[<span data-ttu-id="d42be-130">Tegoeden beheren</span><span class="sxs-lookup"><span data-stu-id="d42be-130">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="d42be-131">Betalingsverplichtingen beheren</span><span class="sxs-lookup"><span data-stu-id="d42be-131">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="d42be-132">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d42be-132">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="d42be-133">Algemene bedrijfsfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="d42be-133">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]