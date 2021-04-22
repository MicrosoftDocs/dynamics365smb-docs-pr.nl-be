---
title: Picken volgens FEFO inschakelen | Microsoft Docs
description: Eerste-verlopen-First-Out (FEFO) is een sorteringsmethode die ervoor zorgt dat de oudste artikelen, die met de vroegste vervaldata, eerst worden gepickt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3a47c9daeeab036055a0644e1b389735f7440106
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784079"
---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="5e363-103">Artikelen picken volgens FEFO inschakelen</span><span class="sxs-lookup"><span data-stu-id="5e363-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="5e363-104">First-Expired-First-Out (FEFO) is een sorteringsmethode die ervoor zorgt dat de oudste artikelen, die met de vroegste vervaldata, eerst worden gepickt.</span><span class="sxs-lookup"><span data-stu-id="5e363-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="5e363-105">Deze functie werkt alleen wanneer aan de volgende criteria wordt voldaan:</span><span class="sxs-lookup"><span data-stu-id="5e363-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="5e363-106">Het artikel moet een serie-/partijnummer hebben.</span><span class="sxs-lookup"><span data-stu-id="5e363-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="5e363-107">Op de tracking-code van het artikel moet het veld **Magazijnserienr.-tracering** of **Magazijnlottracering** worden geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="5e363-107">On the item’s item tracking code setup, the **SN Warehouse Tracking** field or the **Lot Warehouse Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="5e363-108">Het artikel moet met een verloopdatum naar de voorraad worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="5e363-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="5e363-109">Op de locatie moeten de schakelaars **Pick vereist**, **Picken volgens FEFO** en **Opslaglocatie verplicht** zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="5e363-109">On the location, the **Require Pick**, **Pick According to FEFO**, and **Bin Mandatory** toggles must be turned on.</span></span>  

 <span data-ttu-id="5e363-110">Wanneer aan alle criteria wordt voldaan, worden artikelen met serie- of partijnummers die moeten worden gepickt, gesorteerd met de oudste eerst bij alle picks en verplaatsingen, behalve artikelen waarvoor specifieke tracering van Serienr. of partijnummer plaatsvindt.</span><span class="sxs-lookup"><span data-stu-id="5e363-110">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
> <span data-ttu-id="5e363-111">Indien voor sommige artikelen met serie- of partijnummers specifieke tracering plaatsvindt, wordt dit eerst nageleefd en worden daarna de overige, niet-specifieke, serie- en partijnummers gerangschikt volgens FEFO.</span><span class="sxs-lookup"><span data-stu-id="5e363-111">If some serial or lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>
<br /><br />
<span data-ttu-id="5e363-112">Als twee artikelen met serie- of lotnummer dezelfde vervaldatum hebben, wordt het artikel met het laagste lot- of serienummer geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="5e363-112">If two serial or lot-numbered items have the same expiration date, then the application selects the item with the lowest serial or lot number.</span></span>
<br /><br />
<span data-ttu-id="5e363-113">Tijdens het picken van artikelen met een serie- of lotnummer op locaties die zijn ingesteld op gestuurde opslag en pick, worden alleen aantallen in locaties van het type *Pick* gepickt volgens FEFO.</span><span class="sxs-lookup"><span data-stu-id="5e363-113">When picking serial or lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
<br /><br />
<span data-ttu-id="5e363-114">Als u verplaatsingen volgens FEFO mogelijk wilt maken, laat u het veld **Van opslaglocatie** leeg op de pagina **Voorraadverplaatsing** of **Verplaatsingsvoorstel**.</span><span class="sxs-lookup"><span data-stu-id="5e363-114">To enable movements according to FEFO, leave the **From Bin** field empty on the **Inventory Movement** page or the **Movement Worksheet** pages.</span></span>  
<br /><br />
<span data-ttu-id="5e363-115">Als het veld **Strikte verloopdatumboeking** is geselecteerd op de kaart met de **Artikeltraceringscode**, worden alleen artikelen die niet zijn verlopen, in de pick opgenomen en worden de regels gesorteerd volgens het FEFO-principe.</span><span class="sxs-lookup"><span data-stu-id="5e363-115">If the **Strict Expiration Posting** field is selected on the **Item Tracking Code Card**, only items that are not expired will be included in the pick, and the lines are sorted according to the FEFO principle.</span></span>

## <a name="see-also"></a><span data-ttu-id="5e363-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5e363-116">See Also</span></span>  
<span data-ttu-id="5e363-117">[artikelen picken](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="5e363-117">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="5e363-118">[Picken van artikelen voor magazijnverzending](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="5e363-118">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="5e363-119">[Artikelen picken met een voorraadpick](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="5e363-119">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="5e363-120">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="5e363-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="5e363-121">Voorraad</span><span class="sxs-lookup"><span data-stu-id="5e363-121">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="5e363-122">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5e363-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]