---
title: 'Ontwerpdetails: Voorraadwaardering | Microsoft Docs'
description: Deze documentatie biedt gedetailleerde technische inzichten in de concepten en principes die worden gebruikt binnen de functies voor voorraadwaardering in Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 8bfcf2b10d9b302c9a65b7cf27c7fb336be68617
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215990"
---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="9ceca-103">Ontwerpdetails: Voorraadwaardering</span><span class="sxs-lookup"><span data-stu-id="9ceca-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="9ceca-104">Deze documentatie biedt gedetailleerde technische inzichten in de concepten en principes die worden gebruikt binnen de functies voor voorraadwaardering in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="9ceca-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

<span data-ttu-id="9ceca-105">Voorraadwaardering, ook wel kostenbeheer genoemd, heeft betrekking op het vastleggen en rapporteren van operationele bedrijfskosten.</span><span class="sxs-lookup"><span data-stu-id="9ceca-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="9ceca-106">In dit gedeelte</span><span class="sxs-lookup"><span data-stu-id="9ceca-106">In This Section</span></span>  
[<span data-ttu-id="9ceca-107">Ontwerpdetails: Waarderingsmethoden</span><span class="sxs-lookup"><span data-stu-id="9ceca-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="9ceca-108">Ontwerpdetails: Artikelvereffening</span><span class="sxs-lookup"><span data-stu-id="9ceca-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="9ceca-109">Ontwerpdetails: bekend probleem met artikelvereffening</span><span class="sxs-lookup"><span data-stu-id="9ceca-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="9ceca-110">Ontwerpdetails: Kostenwaardering</span><span class="sxs-lookup"><span data-stu-id="9ceca-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="9ceca-111">Ontwerpdetails: Boekingsdatum op herwaarderingswaardepost</span><span class="sxs-lookup"><span data-stu-id="9ceca-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="9ceca-112">Ontwerpdetails: Verwachte kostenboeking</span><span class="sxs-lookup"><span data-stu-id="9ceca-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="9ceca-113">Ontwerpdetails: Gemiddelde kostprijs</span><span class="sxs-lookup"><span data-stu-id="9ceca-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="9ceca-114">Ontwerpdetails: Verschil</span><span class="sxs-lookup"><span data-stu-id="9ceca-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="9ceca-115">Ontwerpdetails: Afronding</span><span class="sxs-lookup"><span data-stu-id="9ceca-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="9ceca-116">Ontwerpdetails: Kostenonderdelen</span><span class="sxs-lookup"><span data-stu-id="9ceca-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="9ceca-117">Ontwerpdetails: Voorraadperioden</span><span class="sxs-lookup"><span data-stu-id="9ceca-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="9ceca-118">Ontwerpdetails: Voorraadboeking</span><span class="sxs-lookup"><span data-stu-id="9ceca-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="9ceca-119">Ontwerpdetails: Productieorderboeking</span><span class="sxs-lookup"><span data-stu-id="9ceca-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="9ceca-120">Ontwerpdetails: Assemblageorderboeking</span><span class="sxs-lookup"><span data-stu-id="9ceca-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="9ceca-121">Ontwerpdetails: Reconciliatie met het grootboek</span><span class="sxs-lookup"><span data-stu-id="9ceca-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="9ceca-122">Ontwerpdetails: Rekeningen in het grootboek</span><span class="sxs-lookup"><span data-stu-id="9ceca-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="9ceca-123">Ontwerpdetails: Voorraadwaardering</span><span class="sxs-lookup"><span data-stu-id="9ceca-123">Design Details: Inventory Valuation</span></span>](design-details-inventory-valuation.md)  
[<span data-ttu-id="9ceca-124">Ontwerpdetails: Herwaardering</span><span class="sxs-lookup"><span data-stu-id="9ceca-124">Design Details: Revaluation</span></span>](design-details-revaluation.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]