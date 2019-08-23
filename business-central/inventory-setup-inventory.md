---
title: Voorraad instellen| Microsoft Docs
description: Beschrijft hoe u uw voorraad en voorraadprocessen instelt, inclusief transferroutes en locaties, zoals magazijnen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 06/20/2019
ms.author: SorenGP
ms.openlocfilehash: 53214df635c637e265c6d302498beee08e9b806c
ms.sourcegitcommit: acbbe80503e61296310ea7f787a9d7f4bc6dccd7
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 08/12/2019
ms.locfileid: "1870535"
---
# <a name="setting-up-inventory"></a><span data-ttu-id="f9801-103">Voorraad instellen</span><span class="sxs-lookup"><span data-stu-id="f9801-103">Setting Up Inventory</span></span>
<span data-ttu-id="f9801-104">Voordat u magazijnactiviteiten en voorraadwaardering kunt beheren, moet u de regels en waarden configureren die het voorraadbeleid van het bedrijf definiëren.</span><span class="sxs-lookup"><span data-stu-id="f9801-104">Before you can manage warehouse activities and inventory costing, you must configure the rules and values that define the company's inventory policies.</span></span>

<span data-ttu-id="f9801-105">U kunt betere klantenservice bieden en uw leveringsketen optimaliseren door uw voorraad op verschillende adressen te organiseren.</span><span class="sxs-lookup"><span data-stu-id="f9801-105">You can provide better customer service and optimize your supply chain by organizing your inventory at different addresses.</span></span> <span data-ttu-id="f9801-106">U kunt vervolgens artikelen op verschillende vestigingen kopen, opslaan of verkopen en voorraad overbrengen tussen vestigingen.</span><span class="sxs-lookup"><span data-stu-id="f9801-106">You can then buy, store, or sell items at different locations and transfer inventory between them.</span></span>

<span data-ttu-id="f9801-107">Als u uw voorraad hebt ingesteld, kunt u verschillende voorraadprocessen met betrekking tot artikeltransacties beheren.</span><span class="sxs-lookup"><span data-stu-id="f9801-107">When you have set up your inventory, you can manage various processes related to item transactions.</span></span> <span data-ttu-id="f9801-108">Zie voor meer informatie [Voorraad beheren](inventory-manage-inventory.md) en [Magazijnbeheer](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="f9801-108">For more information, see [Manage Inventory](inventory-manage-inventory.md) and [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

| <span data-ttu-id="f9801-109">Aan</span><span class="sxs-lookup"><span data-stu-id="f9801-109">To</span></span> | <span data-ttu-id="f9801-110">Zie</span><span class="sxs-lookup"><span data-stu-id="f9801-110">See</span></span> |
| --- | --- |
| <span data-ttu-id="f9801-111">Definieer de algemene voorraadinstellingen, zoals nummerreeksen en hoe u vestigingen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f9801-111">Define the general inventory setup, such as number series and how to use locations.</span></span> |[<span data-ttu-id="f9801-112">Algemene voorraadgegevens instellen</span><span class="sxs-lookup"><span data-stu-id="f9801-112">Set Up General Inventory Information</span></span>](inventory-how-setup-general.md) |
|<span data-ttu-id="f9801-113">Een efficiënt distributiemodel configureren met een combinatie van verschillende locaties en divisies die aan zakelijke partners of medewerkers zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="f9801-113">Configure an efficient distribution model with a combination of different locations and responsibility centers assigned to business partners or employees.</span></span>|[<span data-ttu-id="f9801-114">Werken met divisies</span><span class="sxs-lookup"><span data-stu-id="f9801-114">Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|
| <span data-ttu-id="f9801-115">Orden uw voorraad op verschillende locaties, inclusief transferroutes.</span><span class="sxs-lookup"><span data-stu-id="f9801-115">Organize your inventory at multiple locations, including transfer routes.</span></span> |[<span data-ttu-id="f9801-116">Vestigingen instellen</span><span class="sxs-lookup"><span data-stu-id="f9801-116">Set Up Locations</span></span>](inventory-how-register-new-items.md) |
| <span data-ttu-id="f9801-117">Maak artikelkaarten voor voorraad-, niet-voorraad- of serviceartikelen waarin u handelt.</span><span class="sxs-lookup"><span data-stu-id="f9801-117">Create item cards for inventory, non-inventory, or service items that you trade in.</span></span> |[<span data-ttu-id="f9801-118">Nieuwe artikelen registreren</span><span class="sxs-lookup"><span data-stu-id="f9801-118">Register New Items</span></span>](inventory-how-register-new-items.md) |
|<span data-ttu-id="f9801-119">Gebruik de functie **Item kopiëren** om snel een nieuwe artikelkaart te maken op basis van een bestaande.</span><span class="sxs-lookup"><span data-stu-id="f9801-119">Use the **Copy Item** function to quickly create a new item card based on an existing one.</span></span>|[<span data-ttu-id="f9801-120">Bestaande items kopiëren om nieuwe items te maken</span><span class="sxs-lookup"><span data-stu-id="f9801-120">Copy Existing Items to Create New Items</span></span>](inventory-how-copy-items.md)|
|<span data-ttu-id="f9801-121">Leer hoe u het veld **Soort** op artikelkaarten invult volgens het bedrijfsdoel.</span><span class="sxs-lookup"><span data-stu-id="f9801-121">Learn how to fill in the **Type** field on item cards according to the business purpose.</span></span>|[<span data-ttu-id="f9801-122">Over artikeltypen</span><span class="sxs-lookup"><span data-stu-id="f9801-122">About Item Types</span></span>](inventory-about-item-types.md)|
|<span data-ttu-id="f9801-123">Stel meerdere eenheden in voor een artikel die u kunt gebruiken als alternatieve maateenheden, bijvoorbeeld in verkoop-, inkoop- of productietransacties.</span><span class="sxs-lookup"><span data-stu-id="f9801-123">Set up multiple units of measure for an item that you can use as alternate UOMs, for example on sales, purchasing, or production transactions.</span></span>|[<span data-ttu-id="f9801-124">Artikeleenheden instellen</span><span class="sxs-lookup"><span data-stu-id="f9801-124">Set Up Item Units of Measure</span></span>](inventory-how-setup-units-of-measure.md)|
|<span data-ttu-id="f9801-125">Als aanvulling op vestigingskaarten kunt u gegevens opnemen over de artikelen in een bepaalde vestiging of een bepaalde variant.</span><span class="sxs-lookup"><span data-stu-id="f9801-125">As a supplement to item cards, record information about your items in a specific location or of a specific variant.</span></span>|[<span data-ttu-id="f9801-126">SKU's instellen</span><span class="sxs-lookup"><span data-stu-id="f9801-126">Set Up Stockkeeping Units</span></span>](inventory-how-to-set-up-stockkeeping-units.md)|
| <span data-ttu-id="f9801-127">Artikelen toewijzen aan categorieën en er kenmerken aan toewijzen om u en klanten te helpen artikelen te vinden.</span><span class="sxs-lookup"><span data-stu-id="f9801-127">Assign items to categories and give them attributes to help you and customers find items.</span></span> |[<span data-ttu-id="f9801-128">Artikelen categoriseren</span><span class="sxs-lookup"><span data-stu-id="f9801-128">Categorize Items</span></span>](inventory-how-categorize-items.md) |
|<span data-ttu-id="f9801-129">Importeer meerdere artikelafbeeldingen in één keer uit een zip-bestand waarin de bestanden zijn genoemd naar artikelnummers.</span><span class="sxs-lookup"><span data-stu-id="f9801-129">Import multiple item pictures in one go from a zip file where the files are named according to item numbers.</span></span>|[<span data-ttu-id="f9801-130">Meerdere artikelafbeeldingen importeren</span><span class="sxs-lookup"><span data-stu-id="f9801-130">Import Multiple Item Pictures</span></span>](inventory-how-import-item-pictures.md)|

## <a name="see-also"></a><span data-ttu-id="f9801-131">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f9801-131">See Also</span></span>
[<span data-ttu-id="f9801-132">Voorraad beheren</span><span class="sxs-lookup"><span data-stu-id="f9801-132">Managing Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="f9801-133">Inkopen beheren</span><span class="sxs-lookup"><span data-stu-id="f9801-133">Managing Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="f9801-134">[Verkopen beheren](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="f9801-134">[Managing Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="f9801-135">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f9801-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="f9801-136">Algemene bedrijfsfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="f9801-136">General Business Functionality</span></span>](ui-across-business-areas.md)
