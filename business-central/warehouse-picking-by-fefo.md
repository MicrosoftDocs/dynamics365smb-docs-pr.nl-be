---
title: Picken volgens FEFO inschakelen | Microsoft Docs
description: Eerste-verlopen-First-Out (FEFO) is een sorteringsmethode die ervoor zorgt dat de oudste artikelen, die met de vroegste vervaldata, eerst worden gepickt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 74068ac6041cd318271ecf0272a8ad9b1a2f507c
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2876476"
---
# <a name="enable-picking-items-by-fefo"></a><span data-ttu-id="de49a-103">Artikelen picken volgens FEFO inschakelen</span><span class="sxs-lookup"><span data-stu-id="de49a-103">Enable Picking Items by FEFO</span></span>
<span data-ttu-id="de49a-104">First-Expired-First-Out (FEFO) is een sorteringsmethode die ervoor zorgt dat de oudste artikelen, die met de vroegste vervaldata, eerst worden gepickt.</span><span class="sxs-lookup"><span data-stu-id="de49a-104">First-Expired-First-Out (FEFO) is a sorting method that ensures that the oldest items, those with the earliest expiration dates, are picked first.</span></span>  

 <span data-ttu-id="de49a-105">Deze functie werkt alleen wanneer aan de volgende criteria wordt voldaan:</span><span class="sxs-lookup"><span data-stu-id="de49a-105">This functionality only works when the following criteria are met:</span></span>  

-   <span data-ttu-id="de49a-106">Het artikel moet een serie-/partijnummer hebben.</span><span class="sxs-lookup"><span data-stu-id="de49a-106">The item must have a serial/lot number.</span></span>  
-   <span data-ttu-id="de49a-107">In de instelling van de trackingcode van het artikel moet het veld **Specifieke serienr.-tracering** of **Specifieke lottracering** worden geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="de49a-107">On the item’s item tracking code setup, the **SN Specific Tracking** field or the **Lot Specific Tracking** field must be selected.</span></span>  
-   <span data-ttu-id="de49a-108">Het artikel moet met een verloopdatum naar de voorraad worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="de49a-108">The item must be posted to inventory with an expiration date.</span></span>  
-   <span data-ttu-id="de49a-109">Op de vestigingskaart moet het selectievakje **Picken vereisen** zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="de49a-109">On the location card, the **Require Pick** check box must be selected.</span></span>  
-   <span data-ttu-id="de49a-110">Op de vestigingskaart moet het selectievakje **Picken volgens FEFO** zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="de49a-110">On the location card, the **Pick According to FEFO** check box must be selected.</span></span>  
-   <span data-ttu-id="de49a-111">Op de vestigingskaart moet het selectievakje **Opslaglocatie verplicht** zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="de49a-111">On the location card, the **Bin Mandatory** check box must be selected.</span></span>  

 <span data-ttu-id="de49a-112">Wanneer aan alle criteria wordt voldaan, worden artikelen met serie- of partijnummers die moeten worden gepickt, gesorteerd met de oudste eerst bij alle picks en verplaatsingen, behalve artikelen waarvoor specifieke tracering van Serienr. of partijnummer plaatsvindt.</span><span class="sxs-lookup"><span data-stu-id="de49a-112">When all the criteria are met, then serial/lot-numbered items to be picked are sorted with the oldest first in all picks and movements, except for items that use SN-specific or lot-specific tracking.</span></span>  

> [!NOTE]  
> <span data-ttu-id="de49a-113">Indien voor sommige artikelen met serie- of partijnummers specifieke tracering plaatsvindt, wordt dit eerst nageleefd en worden daarna de overige, niet-specifieke, serie- en partijnummers gerangschikt volgens FEFO.</span><span class="sxs-lookup"><span data-stu-id="de49a-113">If some serial/lot-numbered items use specific tracking, then those are respected first and under them, the remaining, non-specific, serial/lot numbers are listed according to FEFO.</span></span>
<br /><br />
<span data-ttu-id="de49a-114">Als twee artikelen met serie- of lotnummer dezelfde vervaldatum hebben, wordt het artikel met het laagste lot- of serienummer geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="de49a-114">If two serial/lot-numbered items have the same expiration date, then application selects the item with the lowest serial or lot number.</span></span>
<br /><br />
<span data-ttu-id="de49a-115">Tijdens het picken van artikelen met een serie-/lotnummer op locaties die zijn ingesteld op gestuurde opslag en pick, worden alleen aantallen in locaties van het type *Pick* gepicked volgens FEFO.</span><span class="sxs-lookup"><span data-stu-id="de49a-115">When picking serial/lot-numbered items in locations set up for directed put-away and pick, only quantities on bins of type *Pick* are picked according to FEFO.</span></span>  
<br /><br />
<span data-ttu-id="de49a-116">U kunt verplaatsingen volgens FEFO mogelijk maken, hetzij op de pagina **Voorraadverplaatsing** of **Verplaatsingsvoorstel**, door het veld **Uit opslaglocatie** leeg te maken.</span><span class="sxs-lookup"><span data-stu-id="de49a-116">To enable movements according to FEFO, either on the **Inventory Movement** page or the **Movement Worksheet** page, you must leave the **From Bin** field empty.</span></span>  
<br /><br />
<span data-ttu-id="de49a-117">Als het veld **Strikte vervaldatumboeking** is ingeschakeld, worden alleen artikelen die niet zijn verlopen, opgenomen in de pick.</span><span class="sxs-lookup"><span data-stu-id="de49a-117">If the **Strict Expiration Posting** field is selected, then only items that are not expired will be included in the pick.</span></span> <span data-ttu-id="de49a-118">Dit geldt ook als u niet picken volgens FEFO gebruikt.</span><span class="sxs-lookup"><span data-stu-id="de49a-118">This applies even if you are not using Pick according to FEFO.</span></span>

## <a name="see-also"></a><span data-ttu-id="de49a-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="de49a-119">See Also</span></span>  
<span data-ttu-id="de49a-120">[artikelen picken](warehouse-pick-items.md) </span><span class="sxs-lookup"><span data-stu-id="de49a-120">[Picking Items](warehouse-pick-items.md) </span></span>  
<span data-ttu-id="de49a-121">[Picken van artikelen voor magazijnverzending](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="de49a-121">[Pick Items for Warehouse Shipment](warehouse-how-to-pick-items-for-warehouse-shipment.md) </span></span>  
<span data-ttu-id="de49a-122">[Artikelen picken met een voorraadpick](warehouse-how-to-pick-items-with-inventory-picks.md) </span><span class="sxs-lookup"><span data-stu-id="de49a-122">[Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md) </span></span>  
[<span data-ttu-id="de49a-123">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="de49a-123">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
[<span data-ttu-id="de49a-124">Voorraad</span><span class="sxs-lookup"><span data-stu-id="de49a-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="de49a-125">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="de49a-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
