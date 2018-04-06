---
title: Magazijnactiviteiten | Microsoft Docs
description: Nadat goederen zijn ontvangen en voordat goederen worden verzonden, vindt een aantal interne magazijnactiviteiten plaats om een effectieve doorloop in het magazijn te waarborgen en om bedrijfsvoorraden te organiseren en bij te houden.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 604f7e55067efaebed412683ed51ce8717562688
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="warehouse-management"></a><span data-ttu-id="7fbba-103">Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="7fbba-103">Warehouse Management</span></span>
<span data-ttu-id="7fbba-104">Nadat goederen zijn ontvangen en voordat goederen worden verzonden, vindt een aantal interne magazijnactiviteiten plaats om een effectieve doorloop in het magazijn te waarborgen en om bedrijfsvoorraden te organiseren en bij te houden.</span><span class="sxs-lookup"><span data-stu-id="7fbba-104">After goods are received and before goods are shipped, a series of internal warehouse activities take place to ensure an effective flow through the warehouse and to organize and maintain company inventories.</span></span>

<span data-ttu-id="7fbba-105">Gebruikelijke magazijnactiviteiten zijn onder andere het in opslag brengen van artikelen, artikelen binnen of tussen magazijnen verplaatsen en artikelen picken voor assemblage, productie of verzending.</span><span class="sxs-lookup"><span data-stu-id="7fbba-105">Typical warehouse activities include putting items away, moving items inside or between warehouses, and picking items for assembly, production, or shipment.</span></span> <span data-ttu-id="7fbba-106">Het assembleren van artikelen voor verkoop of voorraad kan ook als magazijnactiviteit worden beschouwd, maar dit wordt al ergens anders besproken.</span><span class="sxs-lookup"><span data-stu-id="7fbba-106">Assembling items for sale or inventory may also be considered warehouse activities, but these are covered elsewhere.</span></span> <span data-ttu-id="7fbba-107">Zie voor meer informatie [Assemblagebeheer](assembly-assemble-items.md).</span><span class="sxs-lookup"><span data-stu-id="7fbba-107">For more information, see [Assembly Management](assembly-assemble-items.md).</span></span>  

<span data-ttu-id="7fbba-108">In grote magazijnen kunnen deze verschillende afhandelingstaken door verschillende afdelingen worden uitgevoerd en kan de integratie worden beheerd door een gestuurde werkstroom.</span><span class="sxs-lookup"><span data-stu-id="7fbba-108">In large warehouses, these different handling tasks can be separated by departments and the integration managed by a directed workflow.</span></span> <span data-ttu-id="7fbba-109">In eenvoudigere installaties is de stroom minder geformaliseerd en worden de magazijnactiviteiten uitgevoerd met zogeheten voorraadopslag en voorraadpicks.</span><span class="sxs-lookup"><span data-stu-id="7fbba-109">In simpler installations, the flow is less formalized and the warehouse activities are performed with so-called inventory put-aways and inventory picks.</span></span> <span data-ttu-id="7fbba-110">Zie [Ontwerpdetails: Magazijnoverzicht](design-details-warehouse-overview.md) voor meer informatie over standaard- en geavanceerde magazijnconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="7fbba-110">For more information about basic versus advanced warehouse configurations, see [Design Details: Warehouse Overview](design-details-warehouse-overview.md).</span></span>

<span data-ttu-id="7fbba-111">Voordat u magazijnactiviteiten kunt uitvoeren, moet u het systeem instellen voor de relevante complexiteit van magazijnverwerking.</span><span class="sxs-lookup"><span data-stu-id="7fbba-111">Before you can perform warehouse activities, you must set the system up for the relevant complexity of warehouse processing.</span></span> <span data-ttu-id="7fbba-112">Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="7fbba-112">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

 <span data-ttu-id="7fbba-113">In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.</span><span class="sxs-lookup"><span data-stu-id="7fbba-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="7fbba-114">**Als u dit wilt doen**</span><span class="sxs-lookup"><span data-stu-id="7fbba-114">**To**</span></span>|<span data-ttu-id="7fbba-115">**Zie**</span><span class="sxs-lookup"><span data-stu-id="7fbba-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="7fbba-116">De ontvangst van artikelen in magazijnvestigingen registreren, alleen met een inkooporder, in eenvoudige vestigingsconfiguraties, of met een magazijnontvangst, in het geval van semi- of volledig geautomatiseerde magazijnverwerking in de vestiging.</span><span class="sxs-lookup"><span data-stu-id="7fbba-116">Record the receipt of items at warehouse locations, either with a purchase order only, in simple location setups, or with a warehouse receipt, in case of semi or fully automated warehouse processing at the location.</span></span>|[<span data-ttu-id="7fbba-117">Artikelen ontvangen</span><span class="sxs-lookup"><span data-stu-id="7fbba-117">Receive Items</span></span>](warehouse-how-receive-items.md)|
|<span data-ttu-id="7fbba-118">De opslag- en pickprocessen omzeilen om een artikel van de ontvangst direct naar de productie of verzending door te sturen.</span><span class="sxs-lookup"><span data-stu-id="7fbba-118">Bypass the put-away and pick processes to expedite an item straight from receiving or production to shipping.</span></span>|[<span data-ttu-id="7fbba-119">Artikelen cross-docken</span><span class="sxs-lookup"><span data-stu-id="7fbba-119">Cross-Dock Items</span></span>](warehouse-how-to-cross-dock-items.md)|    
|<span data-ttu-id="7fbba-120">Artikelen opslaan die uit aankopen, verkoopretouren, transport of productieoutput zijn ontvangen, volgens het geconfigureerde magazijnproces.</span><span class="sxs-lookup"><span data-stu-id="7fbba-120">Put away items received from purchases, sales returns, transfers, or production output according to the configured warehouse process.</span></span>|[<span data-ttu-id="7fbba-121">Artikelen opslaan</span><span class="sxs-lookup"><span data-stu-id="7fbba-121">Putting Items Away</span></span>](warehouse-put-away-items.md)|
|<span data-ttu-id="7fbba-122">Artikelen verplaatsen tussen opslaglocaties in het magazijn.</span><span class="sxs-lookup"><span data-stu-id="7fbba-122">Move items between bins in the warehouse.</span></span>|[<span data-ttu-id="7fbba-123">Artikelen verplaatsen</span><span class="sxs-lookup"><span data-stu-id="7fbba-123">Moving Items</span></span>](warehouse-move-items.md)|
|<span data-ttu-id="7fbba-124">Artikelen picken die moeten worden verzonden, getransporteerd of gebruikt in assemblage of productie, volgens het geconfigureerde magazijnproces.</span><span class="sxs-lookup"><span data-stu-id="7fbba-124">Pick items to be shipped, transferred, or consumed in assembly or production, according to the configured warehouse process.</span></span>|[<span data-ttu-id="7fbba-125">Artikelen picken</span><span class="sxs-lookup"><span data-stu-id="7fbba-125">Picking Items</span></span>](warehouse-pick-items.md)|
|<span data-ttu-id="7fbba-126">De verzending van artikelen van magazijnvestigingen registreren, alleen met een verkooporder, in eenvoudige vestigingsconfiguraties, of met een magazijnverzending, in het geval van semi- of volledig geautomatiseerde magazijnprocessen in de vestiging.</span><span class="sxs-lookup"><span data-stu-id="7fbba-126">Record the shipment of items from warehouse locations, either with a sales order only, in simple location setups, or with a warehouse shipment, in case of semi or fully automated warehouse processes at the location.</span></span>|[<span data-ttu-id="7fbba-127">Artikelen verzenden</span><span class="sxs-lookup"><span data-stu-id="7fbba-127">Ship Items</span></span>](warehouse-how-ship-items.md)|  

## <a name="see-also"></a><span data-ttu-id="7fbba-128">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7fbba-128">See Also</span></span>  
[<span data-ttu-id="7fbba-129">Voorraad</span><span class="sxs-lookup"><span data-stu-id="7fbba-129">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="7fbba-130">[Magazijnbeheer instellen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="7fbba-130">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="7fbba-131">[Assemblagebeheer](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="7fbba-131">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="7fbba-132">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="7fbba-132">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="7fbba-133">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7fbba-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

