---
title: 'Ontwerpdetails: Voorraadwaardering | Microsoft Docs'
description: Deze documentatie biedt gedetailleerde technische inzichten in de concepten en principes die worden gebruikt binnen de functies voor voorraadwaardering in Finance and Operations, Business edition.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 11/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 2ee8988a89e4bd01683a6945e66e08ab9608af2e
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="6a618-103">Ontwerpdetails: Voorraadwaardering</span><span class="sxs-lookup"><span data-stu-id="6a618-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="6a618-104">Deze documentatie biedt gedetailleerde technische inzichten in de concepten en principes die worden gebruikt binnen de functies voor voorraadwaardering in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6a618-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="6a618-105">Voorraadwaardering, ook wel kostenbeheer genoemd, heeft betrekking op het vastleggen en rapporteren van operationele bedrijfskosten.</span><span class="sxs-lookup"><span data-stu-id="6a618-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="6a618-106">In dit gedeelte</span><span class="sxs-lookup"><span data-stu-id="6a618-106">In This Section</span></span>  
[<span data-ttu-id="6a618-107">Ontwerpdetails: Waarderingsmethoden</span><span class="sxs-lookup"><span data-stu-id="6a618-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="6a618-108">Ontwerpdetails: Artikelvereffening</span><span class="sxs-lookup"><span data-stu-id="6a618-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="6a618-109">Ontwerpdetails: bekend probleem met artikelvereffening</span><span class="sxs-lookup"><span data-stu-id="6a618-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="6a618-110">Ontwerpdetails: Kostenwaardering</span><span class="sxs-lookup"><span data-stu-id="6a618-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="6a618-111">Ontwerpdetails: Boekingsdatum op herwaarderingswaardepost</span><span class="sxs-lookup"><span data-stu-id="6a618-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="6a618-112">Ontwerpdetails: Verwachte kostenboeking</span><span class="sxs-lookup"><span data-stu-id="6a618-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="6a618-113">Ontwerpdetails: Gemiddelde kostprijs</span><span class="sxs-lookup"><span data-stu-id="6a618-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="6a618-114">Ontwerpdetails: Verschil</span><span class="sxs-lookup"><span data-stu-id="6a618-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="6a618-115">Ontwerpdetails: Afronding</span><span class="sxs-lookup"><span data-stu-id="6a618-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="6a618-116">Ontwerpdetails: Kostenonderdelen</span><span class="sxs-lookup"><span data-stu-id="6a618-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="6a618-117">Ontwerpdetails: Voorraadperioden</span><span class="sxs-lookup"><span data-stu-id="6a618-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="6a618-118">Ontwerpdetails: Voorraadboeking</span><span class="sxs-lookup"><span data-stu-id="6a618-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="6a618-119">Ontwerpdetails: Productieorderboeking</span><span class="sxs-lookup"><span data-stu-id="6a618-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="6a618-120">Ontwerpdetails: Assemblageorderboeking</span><span class="sxs-lookup"><span data-stu-id="6a618-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="6a618-121">Ontwerpdetails: Reconciliatie met het grootboek</span><span class="sxs-lookup"><span data-stu-id="6a618-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="6a618-122">Ontwerpdetails: Rekeningen in het grootboek</span><span class="sxs-lookup"><span data-stu-id="6a618-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="6a618-123">Ontwerpdetails: Herwaardering</span><span class="sxs-lookup"><span data-stu-id="6a618-123">Design Details: Revaluation</span></span>](design-details-revaluation.md)

