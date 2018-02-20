---
title: 'Ontwerpdetails: Bestelbeleid verwerken | Microsoft Docs'
description: "Overzicht van taken voor het definiëren van een bestelbeleid in voorraadplanning."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 2a6658508f8e12a11989d54da6d6c8e3a36631cc
ms.contentlocale: nl-be
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-handling-reordering-policies"></a><span data-ttu-id="60e10-103">Ontwerpdetails: Bestelbeleid verwerken</span><span class="sxs-lookup"><span data-stu-id="60e10-103">Design Details: Handling Reordering Policies</span></span>
<span data-ttu-id="60e10-104">Om een artikel deel te laten nemen aan voorraadplanning, moet een bestelbeleid worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="60e10-104">For an item to participate in supply planning, a reorder policy must be defined.</span></span> <span data-ttu-id="60e10-105">Er zijn vier soorten bestelbeleid:</span><span class="sxs-lookup"><span data-stu-id="60e10-105">The following four reordering policies exist:</span></span>  
  
* <span data-ttu-id="60e10-106">Vast bestelaantal</span><span class="sxs-lookup"><span data-stu-id="60e10-106">Fixed Reorder Qty.</span></span>  
* <span data-ttu-id="60e10-107">Maximum aantal</span><span class="sxs-lookup"><span data-stu-id="60e10-107">Maximum Qty.</span></span>  
* <span data-ttu-id="60e10-108">Order</span><span class="sxs-lookup"><span data-stu-id="60e10-108">Order</span></span>  
* <span data-ttu-id="60e10-109">Lot-for-Lot</span><span class="sxs-lookup"><span data-stu-id="60e10-109">Lot-for-Lot</span></span>  
  
<span data-ttu-id="60e10-110">Beleid voor vast bestelaantal en maximum aantal heeft betrekking op voorraadplanning.</span><span class="sxs-lookup"><span data-stu-id="60e10-110">Fixed Reorder Qty. and Maximum Qty. policies relate to inventory planning.</span></span> <span data-ttu-id="60e10-111">Hoewel voorraadplanning technisch eenvoudiger is dan de vereffeningsprocedure, moet dit beleid naast elkaar bestaan met stapsgewijze vereffening van voorziening en ordertracering.</span><span class="sxs-lookup"><span data-stu-id="60e10-111">Although inventory planning is technically simpler than the balancing procedure, these policies must coexist with the step-by-step balancing of supply and order tracking.</span></span> <span data-ttu-id="60e10-112">Er gelden strikte regels voor de verwerking van het bestelbeleid om de integratie tussen deze twee te beheren en om zichtbaarheid te bieden in de betrokken planningslogica.</span><span class="sxs-lookup"><span data-stu-id="60e10-112">To control the integration between the two, and to provide visibility into the involved planning logic, strict principles govern how reordering policies are handled.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="60e10-113">In dit gedeelte</span><span class="sxs-lookup"><span data-stu-id="60e10-113">In This Section</span></span>  
[<span data-ttu-id="60e10-114">Ontwerpdetails: De rol van het bestelpunt</span><span class="sxs-lookup"><span data-stu-id="60e10-114">Design Details: The Role of the Reorder Point</span></span>](design-details-the-role-of-the-reorder-point.md)  
[<span data-ttu-id="60e10-115">Ontwerpdetails: Het verwachte voorraadniveau en het bestelpunt controleren</span><span class="sxs-lookup"><span data-stu-id="60e10-115">Design Details: Monitoring the Projected Inventory Level and the Reorder Point</span></span>](design-details-monitoring-the-projected-inventory-level-and-the-reorder-point.md)  
[<span data-ttu-id="60e10-116">Ontwerpdetails: De rol van het tijdsinterval</span><span class="sxs-lookup"><span data-stu-id="60e10-116">Design Details: The Role of the Time Bucket</span></span>](design-details-the-role-of-the-time-bucket.md)  
[<span data-ttu-id="60e10-117">Ontwerpdetails: Onder het overflowniveau blijven</span><span class="sxs-lookup"><span data-stu-id="60e10-117">Design Details: Staying under the Overflow Level</span></span>](design-details-staying-under-the-overflow-level.md)  
[<span data-ttu-id="60e10-118">Ontwerpdetails: Verwachte negatieve voorraad verwerken</span><span class="sxs-lookup"><span data-stu-id="60e10-118">Design Details: Handling Projected Negative Inventory</span></span>](design-details-handling-projected-negative-inventory.md)  
[<span data-ttu-id="60e10-119">Ontwerpdetails: Bestelbeleid</span><span class="sxs-lookup"><span data-stu-id="60e10-119">Design Details: Reordering Policies</span></span>](design-details-reordering-policies.md)  
  
## <a name="see-also"></a><span data-ttu-id="60e10-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="60e10-120">See Also</span></span>  
<span data-ttu-id="60e10-121">[Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="60e10-121">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="60e10-122">[Ontwerpdetails: Tabel Planningstoewijzing](design-details-planning-assignment-table.md) </span><span class="sxs-lookup"><span data-stu-id="60e10-122">[Design Details: Planning Assignment Table](design-details-planning-assignment-table.md) </span></span>  
<span data-ttu-id="60e10-123">[Ontwerpdetails: Centrale begrippen van het planningssysteem](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="60e10-123">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
<span data-ttu-id="60e10-124">[Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="60e10-124">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
[<span data-ttu-id="60e10-125">Ontwerpdetails: Voorraadplanning</span><span class="sxs-lookup"><span data-stu-id="60e10-125">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
