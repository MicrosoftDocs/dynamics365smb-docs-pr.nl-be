---
title: 'Ontwerpdetails: Voorraadwaardering | Microsoft Docs'
description: Deze documentatie biedt gedetailleerde technische inzichten in de concepten en principes die worden gebruikt binnen de functies voor voorraadwaardering in Dynamics 365.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: ef098c17ab54d45eec380548f70042a436c95128
ms.contentlocale: nl-be
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="f5cbc-103">Ontwerpdetails: Voorraadwaardering</span><span class="sxs-lookup"><span data-stu-id="f5cbc-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="f5cbc-104">Deze documentatie biedt gedetailleerde technische inzichten in de concepten en principes die worden gebruikt binnen de functies voor voorraadwaardering in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f5cbc-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="f5cbc-105">Voorraadwaardering, ook wel kostenbeheer genoemd, heeft betrekking op het vastleggen en rapporteren van operationele bedrijfskosten.</span><span class="sxs-lookup"><span data-stu-id="f5cbc-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="f5cbc-106">In dit gedeelte</span><span class="sxs-lookup"><span data-stu-id="f5cbc-106">In This Section</span></span>  
[<span data-ttu-id="f5cbc-107">Ontwerpdetails: Waarderingsmethoden</span><span class="sxs-lookup"><span data-stu-id="f5cbc-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="f5cbc-108">Ontwerpdetails: Artikelvereffening</span><span class="sxs-lookup"><span data-stu-id="f5cbc-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="f5cbc-109">Ontwerpdetails: Kostenwaardering</span><span class="sxs-lookup"><span data-stu-id="f5cbc-109">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="f5cbc-110">Ontwerpdetails: Verwachte kostenboeking</span><span class="sxs-lookup"><span data-stu-id="f5cbc-110">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="f5cbc-111">Ontwerpdetails: Gemiddelde kostprijs</span><span class="sxs-lookup"><span data-stu-id="f5cbc-111">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="f5cbc-112">Ontwerpdetails: Verschil</span><span class="sxs-lookup"><span data-stu-id="f5cbc-112">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="f5cbc-113">Ontwerpdetails: Afronding</span><span class="sxs-lookup"><span data-stu-id="f5cbc-113">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="f5cbc-114">Ontwerpdetails: Kostenonderdelen</span><span class="sxs-lookup"><span data-stu-id="f5cbc-114">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="f5cbc-115">Ontwerpdetails: Voorraadperioden</span><span class="sxs-lookup"><span data-stu-id="f5cbc-115">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="f5cbc-116">Ontwerpdetails: Voorraadboeking</span><span class="sxs-lookup"><span data-stu-id="f5cbc-116">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="f5cbc-117">Ontwerpdetails: Productieorderboeking</span><span class="sxs-lookup"><span data-stu-id="f5cbc-117">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="f5cbc-118">Ontwerpdetails: Assemblageorderboeking</span><span class="sxs-lookup"><span data-stu-id="f5cbc-118">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="f5cbc-119">Ontwerpdetails: Reconciliatie met het grootboek</span><span class="sxs-lookup"><span data-stu-id="f5cbc-119">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="f5cbc-120">Ontwerpdetails: Rekeningen in het grootboek</span><span class="sxs-lookup"><span data-stu-id="f5cbc-120">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="f5cbc-121">Ontwerpdetails: Herwaardering</span><span class="sxs-lookup"><span data-stu-id="f5cbc-121">Design Details: Revaluation</span></span>](design-details-revaluation.md)

