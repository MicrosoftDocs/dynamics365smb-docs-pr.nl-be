---
title: Picken volgens FEFO inschakelen | Microsoft Docs
description: Eerste-verlopen-First-Out (FEFO) is een sorteringsmethode die ervoor zorgt dat de oudste artikelen, die met de vroegste vervaldata, eerst worden gepickt.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 7e494ebc118b7c75ab565ae57259030987bbeee7
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="b885b-103">Artikelen picken volgens FEFO inschakelen</span><span class="sxs-lookup"><span data-stu-id="b885b-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="b885b-104">First-Expired-First-Out (FEFO) is een sorteringsmethode die ervoor zorgt dat de oudste artikelen, die met de vroegste vervaldata, eerst worden gepickt.</span><span class="sxs-lookup"><span data-stu-id="b885b-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="b885b-105">Deze functie werkt alleen wanneer aan de volgende criteria wordt voldaan:</span><span class="sxs-lookup"><span data-stu-id="b885b-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="b885b-106">Het artikel moet een serie-/partijnummer hebben.</span><span class="sxs-lookup"><span data-stu-id="b885b-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="b885b-107">Op de tracking-code van het artikel moet het veld **Serienr. specifieke magazijn tracering** of **Partij-specifieke magazijn tracering** worden geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="b885b-107">On the item’s item tracking code setup, the **SN-Specific Warehouse Tracking** field or the **Lot-Specific Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="b885b-108">Het artikel moet met een verloopdatum naar de voorraad worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="b885b-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="b885b-109">Op de vestigingskaart moet het selectievakje **Picken vereisen** zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="b885b-109">On the location card, the **Require Pick** check box must be selected.</span></span>  
-   <span data-ttu-id="b885b-110">Op de vestigingskaart moet het selectievakje **Picken volgens FEFO** zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="b885b-110">On the location card, the **Pick According to FEFO** check box must be selected.</span></span>  
-   <span data-ttu-id="b885b-111">Op de vestigingskaart moet het selectievakje **Opslaglocatie verplicht** zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="b885b-111">On the location card, the **Bin Mandatory** check box must be selected.</span></span>  

 <span data-ttu-id="b885b-112">Wanneer aan alle criteria wordt voldaan, worden artikelen met serie- of partijnummers die moeten worden gepickt, gesorteerd met de oudste eerst bij alle picks en verplaatsingen, behalve artikelen waarvoor specifieke tracering van Serienr. of partijnummer plaatsvindt.</span><span class="sxs-lookup"><span data-stu-id="b885b-112">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
> <span data-ttu-id="b885b-113">Indien voor sommige artikelen met serie- of partijnummers specifieke tracering plaatsvindt, wordt dit eerst nageleefd en worden daarna de overige, niet-specifieke, serie- en partijnummers gerangschikt volgens FEFO.</span><span class="sxs-lookup"><span data-stu-id="b885b-113">If some serial/lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>
<br /><br />
<span data-ttu-id="b885b-114">Als twee artikelen met serie- of lotnummer dezelfde vervaldatum hebben, wordt het artikel met het laagste lot- of serienummer geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="b885b-114">If two serial/lot-numbered items have the same expiration date, then the program selects the item with the lowest serial or lot number.</span></span>
<br /><br />
<span data-ttu-id="b885b-115">Tijdens het picken van artikelen met een serie-/lotnummer op locaties die zijn ingesteld op gestuurde opslag en pick, worden alleen aantallen in locaties van het type *Pick* gepicked volgens FEFO.</span><span class="sxs-lookup"><span data-stu-id="b885b-115">When picking serial/lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
<br /><br />
<span data-ttu-id="b885b-116">U kunt verplaatsingen volgens FEFO mogelijk maken, hetzij in het venster **Voorraadverplaatsing** of **Werkblad verplaatsing**, door het veld **Uit opslaglocatie** leeg te maken.</span><span class="sxs-lookup"><span data-stu-id="b885b-116">To enable movements according to FEFO, either in the **Inventory Movement** window or the **Movement Worksheet** window, you must leave the **From Bin** field empty.</span></span>  
<br /><br />
<span data-ttu-id="b885b-117">Als het veld **Strikte vervaldatumboeking** is ingeschakeld, worden alleen artikelen die niet zijn verlopen, opgenomen in de pick.</span><span class="sxs-lookup"><span data-stu-id="b885b-117">If the **Strict Expiration Posting** field is selected, then only items that are not expired will be included in the pick.</span></span> <span data-ttu-id="b885b-118">Dit geldt ook als u niet picken volgens FEFO gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b885b-118">This applies even if you are not using Pick according to FEFO.</span></span>

## <a name="see-also"></a><span data-ttu-id="b885b-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b885b-119">See Also</span></span>  
<span data-ttu-id="b885b-120">[artikelen picken](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="b885b-120">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="b885b-121">[Picken van artikelen voor magazijnverzending](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="b885b-121">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="b885b-122">[Artikelen picken met een voorraadpick](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="b885b-122">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="b885b-123">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="b885b-123">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="b885b-124">Voorraad</span><span class="sxs-lookup"><span data-stu-id="b885b-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="b885b-125">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b885b-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

