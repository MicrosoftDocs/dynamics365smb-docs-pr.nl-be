---
title: 'Ontwerpdetails: Bestelbeleid verwerken | Microsoft Docs'
description: "Overzicht van taken voor het definiëren van een bestelbeleid in voorraadplanning."
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
ms.openlocfilehash: e06d91bc1c293e7015af0fe21d918361f322c10d
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-handling-reordering-policies"></a><span data-ttu-id="e5560-103">Ontwerpdetails: Bestelbeleid verwerken</span><span class="sxs-lookup"><span data-stu-id="e5560-103">Design Details: Handling Reordering Policies</span></span>
<span data-ttu-id="e5560-104">Om een artikel deel te laten nemen aan voorraadplanning, moet een bestelbeleid worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="e5560-104">For an item to participate in supply planning, a reorder policy must be defined.</span></span> <span data-ttu-id="e5560-105">Er zijn vier soorten bestelbeleid:</span><span class="sxs-lookup"><span data-stu-id="e5560-105">The following four reordering policies exist:</span></span>  
  
* <span data-ttu-id="e5560-106">Vast bestelaantal</span><span class="sxs-lookup"><span data-stu-id="e5560-106">Fixed Reorder Qty.</span></span>  
* <span data-ttu-id="e5560-107">Maximum aantal</span><span class="sxs-lookup"><span data-stu-id="e5560-107">Maximum Qty.</span></span>  
* <span data-ttu-id="e5560-108">Order</span><span class="sxs-lookup"><span data-stu-id="e5560-108">Order</span></span>  
* <span data-ttu-id="e5560-109">Lot-for-Lot</span><span class="sxs-lookup"><span data-stu-id="e5560-109">Lot-for-Lot</span></span>  
  
<span data-ttu-id="e5560-110">Beleid voor vast bestelaantal en maximum aantal heeft betrekking op voorraadplanning.</span><span class="sxs-lookup"><span data-stu-id="e5560-110">Fixed Reorder Qty. and Maximum Qty. policies relate to inventory planning.</span></span> <span data-ttu-id="e5560-111">Hoewel voorraadplanning technisch eenvoudiger is dan de vereffeningsprocedure, moet dit beleid naast elkaar bestaan met stapsgewijze vereffening van voorziening en ordertracering.</span><span class="sxs-lookup"><span data-stu-id="e5560-111">Although inventory planning is technically simpler than the balancing procedure, these policies must coexist with the step-by-step balancing of supply and order tracking.</span></span> <span data-ttu-id="e5560-112">Er gelden strikte regels voor de verwerking van het bestelbeleid om de integratie tussen deze twee te beheren en om zichtbaarheid te bieden in de betrokken planningslogica.</span><span class="sxs-lookup"><span data-stu-id="e5560-112">To control the integration between the two, and to provide visibility into the involved planning logic, strict principles govern how reordering policies are handled.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="e5560-113">In dit gedeelte</span><span class="sxs-lookup"><span data-stu-id="e5560-113">In This Section</span></span>  
[<span data-ttu-id="e5560-114">Ontwerpdetails: De rol van het bestelpunt</span><span class="sxs-lookup"><span data-stu-id="e5560-114">Design Details: The Role of the Reorder Point</span></span>](design-details-the-role-of-the-reorder-point.md)  
[<span data-ttu-id="e5560-115">Ontwerpdetails: Het verwachte voorraadniveau en het bestelpunt controleren</span><span class="sxs-lookup"><span data-stu-id="e5560-115">Design Details: Monitoring the Projected Inventory Level and the Reorder Point</span></span>](design-details-monitoring-the-projected-inventory-level-and-the-reorder-point.md)  
[<span data-ttu-id="e5560-116">Ontwerpdetails: De rol van het tijdsinterval</span><span class="sxs-lookup"><span data-stu-id="e5560-116">Design Details: The Role of the Time Bucket</span></span>](design-details-the-role-of-the-time-bucket.md)  
[<span data-ttu-id="e5560-117">Ontwerpdetails: Onder het overflowniveau blijven</span><span class="sxs-lookup"><span data-stu-id="e5560-117">Design Details: Staying under the Overflow Level</span></span>](design-details-staying-under-the-overflow-level.md)  
[<span data-ttu-id="e5560-118">Ontwerpdetails: Verwachte negatieve voorraad verwerken</span><span class="sxs-lookup"><span data-stu-id="e5560-118">Design Details: Handling Projected Negative Inventory</span></span>](design-details-handling-projected-negative-inventory.md)  
[<span data-ttu-id="e5560-119">Ontwerpdetails: Bestelbeleid</span><span class="sxs-lookup"><span data-stu-id="e5560-119">Design Details: Reordering Policies</span></span>](design-details-reordering-policies.md)  
  
## <a name="see-also"></a><span data-ttu-id="e5560-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e5560-120">See Also</span></span>  
<span data-ttu-id="e5560-121">[Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="e5560-121">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="e5560-122">[Ontwerpdetails: Tabel Planningstoewijzing](design-details-planning-assignment-table.md) </span><span class="sxs-lookup"><span data-stu-id="e5560-122">[Design Details: Planning Assignment Table](design-details-planning-assignment-table.md) </span></span>  
<span data-ttu-id="e5560-123">[Ontwerpdetails: Centrale begrippen van het planningssysteem](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="e5560-123">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
<span data-ttu-id="e5560-124">[Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="e5560-124">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
[<span data-ttu-id="e5560-125">Ontwerpdetails: Voorraadplanning</span><span class="sxs-lookup"><span data-stu-id="e5560-125">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
