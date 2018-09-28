---
title: 'Ontwerpdetails: Voorraadwaardering | Microsoft Docs'
description: Deze documentatie biedt gedetailleerde technische inzichten in de concepten en principes die worden gebruikt binnen de functies voor voorraadwaardering in Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 04f41fa7b075692fef8243e24cff1ef3a5ebaf65
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="0be1b-103">Ontwerpdetails: Voorraadwaardering</span><span class="sxs-lookup"><span data-stu-id="0be1b-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="0be1b-104">Deze documentatie biedt gedetailleerde technische inzichten in de concepten en principes die worden gebruikt binnen de functies voor voorraadwaardering in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="0be1b-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="0be1b-105">Voorraadwaardering, ook wel kostenbeheer genoemd, heeft betrekking op het vastleggen en rapporteren van operationele bedrijfskosten.</span><span class="sxs-lookup"><span data-stu-id="0be1b-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="0be1b-106">In dit gedeelte</span><span class="sxs-lookup"><span data-stu-id="0be1b-106">In This Section</span></span>  
[<span data-ttu-id="0be1b-107">Ontwerpdetails: Waarderingsmethoden</span><span class="sxs-lookup"><span data-stu-id="0be1b-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="0be1b-108">Ontwerpdetails: Artikelvereffening</span><span class="sxs-lookup"><span data-stu-id="0be1b-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="0be1b-109">Ontwerpdetails: bekend probleem met artikelvereffening</span><span class="sxs-lookup"><span data-stu-id="0be1b-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="0be1b-110">Ontwerpdetails: Kostenwaardering</span><span class="sxs-lookup"><span data-stu-id="0be1b-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="0be1b-111">Ontwerpdetails: Boekingsdatum op herwaarderingswaardepost</span><span class="sxs-lookup"><span data-stu-id="0be1b-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="0be1b-112">Ontwerpdetails: Verwachte kostenboeking</span><span class="sxs-lookup"><span data-stu-id="0be1b-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="0be1b-113">Ontwerpdetails: Gemiddelde kostprijs</span><span class="sxs-lookup"><span data-stu-id="0be1b-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="0be1b-114">Ontwerpdetails: Verschil</span><span class="sxs-lookup"><span data-stu-id="0be1b-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="0be1b-115">Ontwerpdetails: Afronding</span><span class="sxs-lookup"><span data-stu-id="0be1b-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="0be1b-116">Ontwerpdetails: Kostenonderdelen</span><span class="sxs-lookup"><span data-stu-id="0be1b-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="0be1b-117">Ontwerpdetails: Voorraadperioden</span><span class="sxs-lookup"><span data-stu-id="0be1b-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="0be1b-118">Ontwerpdetails: Voorraadboeking</span><span class="sxs-lookup"><span data-stu-id="0be1b-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="0be1b-119">Ontwerpdetails: Productieorderboeking</span><span class="sxs-lookup"><span data-stu-id="0be1b-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="0be1b-120">Ontwerpdetails: Assemblageorderboeking</span><span class="sxs-lookup"><span data-stu-id="0be1b-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="0be1b-121">Ontwerpdetails: Reconciliatie met het grootboek</span><span class="sxs-lookup"><span data-stu-id="0be1b-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="0be1b-122">Ontwerpdetails: Rekeningen in het grootboek</span><span class="sxs-lookup"><span data-stu-id="0be1b-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="0be1b-123">Ontwerpdetails: Herwaardering</span><span class="sxs-lookup"><span data-stu-id="0be1b-123">Design Details: Revaluation</span></span>](design-details-revaluation.md)

