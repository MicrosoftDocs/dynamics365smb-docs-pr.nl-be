---
title: Voorraad instellen| Microsoft Docs
description: Beschrijft hoe u uw voorraad en voorraadprocessen instelt, inclusief transferroutes en locaties, zoals magazijnen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 01/12/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 62eee7532e457721430cb31519b5acb23e95bfcb
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-inventory"></a><span data-ttu-id="3f49a-103">Voorraad instellen</span><span class="sxs-lookup"><span data-stu-id="3f49a-103">Setting Up Inventory</span></span>
<span data-ttu-id="3f49a-104">Voordat u magazijnactiviteiten en voorraadwaardering kunt beheren, moet u de regels en waarden configureren die het voorraadbeleid van het bedrijf definiëren.</span><span class="sxs-lookup"><span data-stu-id="3f49a-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="3f49a-105">U kunt betere klantenservice bieden en uw leveringsketen optimaliseren door uw voorraad op verschillende adressen te organiseren.</span><span class="sxs-lookup"><span data-stu-id="3f49a-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="3f49a-106">U kunt vervolgens artikelen op verschillende vestigingen kopen, opslaan of verkopen en voorraad overbrengen tussen vestigingen.</span><span class="sxs-lookup"><span data-stu-id="3f49a-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="3f49a-107">Als u uw voorraad hebt ingesteld, kunt u verschillende voorraadprocessen met betrekking tot artikeltransacties beheren.</span><span class="sxs-lookup"><span data-stu-id="3f49a-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="3f49a-108">Zie voor meer informatie [Voorraad beheren](inventory-manage-inventory.md) en [Magazijnbeheer](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="3f49a-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="3f49a-109">Aan</span><span class="sxs-lookup"><span data-stu-id="3f49a-109">To</span></span> | <span data-ttu-id="3f49a-110">Zie</span><span class="sxs-lookup"><span data-stu-id="3f49a-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="3f49a-111">Definieer de algemene voorraadinstellingen, zoals nummerreeksen en hoe u vestigingen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="3f49a-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="3f49a-112">Algemene voorraadgegevens instellen</span><span class="sxs-lookup"><span data-stu-id="3f49a-112">Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="3f49a-113">Een efficiënt distributiemodel configureren met een combinatie van verschillende locaties en divisies die aan zakelijke partners of medewerkers zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="3f49a-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="3f49a-114">Werken met divisies</span><span class="sxs-lookup"><span data-stu-id="3f49a-114">Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="3f49a-115">Orden uw voorraad op verschillende locaties, inclusief transferroutes.</span><span class="sxs-lookup"><span data-stu-id="3f49a-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="3f49a-116">Vestigingen instellen</span><span class="sxs-lookup"><span data-stu-id="3f49a-116">Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="3f49a-117">Maak artikelkaarten voor voorraadartikelen waarin u handelt.</span><span class="sxs-lookup"><span data-stu-id="3f49a-117">Create item cards for inventory items that you trade in.</span></span> |[<span data-ttu-id="3f49a-118">Nieuwe artikelen registreren</span><span class="sxs-lookup"><span data-stu-id="3f49a-118">Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="3f49a-119">Stel meerdere eenheden in voor een artikel die u kunt gebruiken als alternatieve maateenheden, bijvoorbeeld in verkoop-, inkoop- of productietransacties.</span><span class="sxs-lookup"><span data-stu-id="3f49a-119">Set up multiple units of measure for an item that you can use as alternate UOMs, for example on sales, purchasing, or production transactions.</span></span>|[<span data-ttu-id="3f49a-120">Artikeleenheden instellen</span><span class="sxs-lookup"><span data-stu-id="3f49a-120">Set Up Item Units of Measure</span></span>](inventory-how-setup-units-of-measure.md)|
|<span data-ttu-id="3f49a-121">Als aanvulling op vestigingskaarten kunt u gegevens opnemen over de artikelen in een bepaalde vestiging of een bepaalde variant.</span><span class="sxs-lookup"><span data-stu-id="3f49a-121">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="3f49a-122">SKU's instellen</span><span class="sxs-lookup"><span data-stu-id="3f49a-122">Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="3f49a-123">Artikelen toewijzen aan categorieën en er kenmerken aan toewijzen om u en klanten te helpen artikelen te vinden.</span><span class="sxs-lookup"><span data-stu-id="3f49a-123">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="3f49a-124">Artikelen categoriseren</span><span class="sxs-lookup"><span data-stu-id="3f49a-124">Categorize Items</span></span>](inventory-how-categorize-items.md) |

## <a name="see-also"></a><span data-ttu-id="3f49a-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3f49a-125">See Also</span></span>
[<span data-ttu-id="3f49a-126">Voorraad beheren</span><span class="sxs-lookup"><span data-stu-id="3f49a-126">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="3f49a-127">Inkopen beheren</span><span class="sxs-lookup"><span data-stu-id="3f49a-127">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="3f49a-128">[Verkopen beheren](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="3f49a-128">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="3f49a-129">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3f49a-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="3f49a-130">Algemene bedrijfsfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="3f49a-130">General Business Functionality</span></span>](ui-across-business-areas.md)

