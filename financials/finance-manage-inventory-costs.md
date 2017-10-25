---
title: Voorraadkosten beheren | Microsoft Docs
description: Kostenbeheer heeft betrekking op het vastleggen en rapporteren van operationele bedrijfskosten. Dit omvat de rapportage van productie- en voorraadkosten (dus de waarde van artikelen).
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 8da779426dfd06519507796c995adcedcd40ac81
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="managing-inventory-costs"></a><span data-ttu-id="2bd44-104">Voorraadkosten beheren</span><span class="sxs-lookup"><span data-stu-id="2bd44-104">Managing Inventory Costs</span></span>
<span data-ttu-id="2bd44-105">Kostenbeheer heeft betrekking op het vastleggen en rapporteren van operationele bedrijfskosten.</span><span class="sxs-lookup"><span data-stu-id="2bd44-105">Cost management, also referred to as “costing”, is concerned with recording and reporting business operating costs.</span></span> <span data-ttu-id="2bd44-106">Dit omvat de rapportage van productie- en voorraadkosten (dus de waarde van artikelen).</span><span class="sxs-lookup"><span data-stu-id="2bd44-106">It includes the reporting of manufacturing costs and inventory costs, that is, the value of items.</span></span>   

<span data-ttu-id="2bd44-107">U dient de volgende centrale principes te begrijpen: met waarderingsmethoden wordt gedefinieerd hoe artikelen worden gewaardeerd wanneer ze de voorraad verlaten, met een herwaardering van kosten worden de kosten bijgewerkt van goederen die worden verkocht met gerelateerde inkoopkosten die na de verkoop zijn geboekt en de voorraadwaarden moeten regelmatig worden geboekt naar speciale grootboekrekeningen.</span><span class="sxs-lookup"><span data-stu-id="2bd44-107">Central principles to understand are that costing methods define how items are valued when they leave inventory, that cost adjustment updates the cost of goods sold with related purchase costs posted after the sale, and that inventory values must be posted to dedicated G/L accounts at regular intervals.</span></span>

<span data-ttu-id="2bd44-108">In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.</span><span class="sxs-lookup"><span data-stu-id="2bd44-108">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="2bd44-109">**Als u dit wilt doen**</span><span class="sxs-lookup"><span data-stu-id="2bd44-109">**To**</span></span>|<span data-ttu-id="2bd44-110">**Zie**</span><span class="sxs-lookup"><span data-stu-id="2bd44-110">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="2bd44-111">Lees conceptuele informatie voor het begrip van de principes en definities die functionaliteit voor voorraadwaarderingsboekhouding in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] beheren.</span><span class="sxs-lookup"><span data-stu-id="2bd44-111">Read various conceptual information to understand the principles and definitions that govern the inventory costing accounting functionality in [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)].</span></span>|[<span data-ttu-id="2bd44-112">Over voorraadwaardering</span><span class="sxs-lookup"><span data-stu-id="2bd44-112">About Inventory Costing</span></span>](finance-learn-about-costing.md)|  
|<span data-ttu-id="2bd44-113">Stel voorraadperioden, waarderingsmethoden en afrondingsmethoden in.</span><span class="sxs-lookup"><span data-stu-id="2bd44-113">Set up inventory periods, costing methods, and rounding methods.</span></span>|[<span data-ttu-id="2bd44-114">Voorraadwaardering en kostprijsberekening instellen</span><span class="sxs-lookup"><span data-stu-id="2bd44-114">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)|
|<span data-ttu-id="2bd44-115">Vermeerder of verminder de waarde van een of meer artikelen in voorraad door de huidige, berekende waarde ervan te boeken.</span><span class="sxs-lookup"><span data-stu-id="2bd44-115">Appreciate or depreciate the value of one or more items in inventory by posting their current, calculated value.</span></span>|[<span data-ttu-id="2bd44-116">Procedure: Voorraad herwaarderen</span><span class="sxs-lookup"><span data-stu-id="2bd44-116">How to: Revalue Inventory</span></span>](inventory-how-revalue-inventory.md)|
|<span data-ttu-id="2bd44-117">Herwaardeer artikelkosten, automatisch of handmatig, om kostenwijzigingen door te sturen van inkomende posten naar de gerelateerde uitgaande posten.</span><span class="sxs-lookup"><span data-stu-id="2bd44-117">Adjust item costs, either automatically or manually, to forward cost changes from inbound entries to their related outbound entries.</span></span>|[<span data-ttu-id="2bd44-118">Procedure: Artikelkosten herwaarderen</span><span class="sxs-lookup"><span data-stu-id="2bd44-118">How to: Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|
|<span data-ttu-id="2bd44-119">Speciale waarderingsfuncties gebruiken voor dagelijkse artikeltransacties in de artikelbewerkingen.</span><span class="sxs-lookup"><span data-stu-id="2bd44-119">Use special costing functions for every-day item transactions in the item operations.</span></span>|[<span data-ttu-id="2bd44-120">Voorraad- en productiekosten verwerken</span><span class="sxs-lookup"><span data-stu-id="2bd44-120">Handling Inventory and Manufacturing Costs</span></span>](finance-handle-inventory-and-manufacturing-costs.md)|  
|<span data-ttu-id="2bd44-121">U moet regelmatig de vaste verrekenprijzen van onderdelen bijwerken in assemblage- of productiestuklijsten en de nieuwe kosten tot aan het hoofdartikel berekenen.</span><span class="sxs-lookup"><span data-stu-id="2bd44-121">Periodically update the standard costs of components, in assembly or production BOMs, and roll the new costs up to the parent item.</span></span>|[<span data-ttu-id="2bd44-122">Procedure: vaste verrekenprijzen aanpassen</span><span class="sxs-lookup"><span data-stu-id="2bd44-122">How to: Update Standard Costs</span></span>](finance-how-to-update-standard-costs.md)|
|<span data-ttu-id="2bd44-123">Controle- en rapportagetaken uit te voeren voor een periode-einde, zoals het berekenen van de voorraadwaarde en het boeken van kosten in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="2bd44-123">Perform period-end control and reporting tasks, such calculate the value of inventory and post costs to the general ledger.</span></span>|[<span data-ttu-id="2bd44-124">Kosten rapporteren en afstemmen met het grootboek</span><span class="sxs-lookup"><span data-stu-id="2bd44-124">Reporting Costs and Reconciling with the General Ledger</span></span>](finance-report-costs-and-reconcile-with-the-general-ledger.md)|  
|<span data-ttu-id="2bd44-125">Meer informatie over alle mechanisme in het kostprijsberekeningsysteem.</span><span class="sxs-lookup"><span data-stu-id="2bd44-125">Learn about all mechanisms in the costing system.</span></span>|[<span data-ttu-id="2bd44-126">Ontwerpdetails: Voorraadwaardering</span><span class="sxs-lookup"><span data-stu-id="2bd44-126">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)|  

## <a name="see-also"></a><span data-ttu-id="2bd44-127">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2bd44-127">See Also</span></span>  
 [<span data-ttu-id="2bd44-128">Financiën</span><span class="sxs-lookup"><span data-stu-id="2bd44-128">Finance</span></span>](finance.md)  
 <span data-ttu-id="2bd44-129">[Voorraad](inventory-manage-inventory.md) </span><span class="sxs-lookup"><span data-stu-id="2bd44-129">[Inventory](inventory-manage-inventory.md) </span></span>  
 <span data-ttu-id="2bd44-130">[Verkoop](sales-manage-sales.md) </span><span class="sxs-lookup"><span data-stu-id="2bd44-130">[Sales](sales-manage-sales.md) </span></span>  
 [<span data-ttu-id="2bd44-131">Inkoop</span><span class="sxs-lookup"><span data-stu-id="2bd44-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="2bd44-132">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2bd44-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

