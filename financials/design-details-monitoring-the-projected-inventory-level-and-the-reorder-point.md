---
title: 'Ontwerpdetails: Het verwachte voorraadniveau en het bestelpunt controleren | Microsoft Docs'
description: Leer hoe met voorraadplanning onderscheid wordt gemaakt tussen verwachte voorraad en verwachte beschikbare voorraadniveaus.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, inventory, planning
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a0e64d96389739c67a9e9f548958fac12e3aca2a
ms.contentlocale: nl-be
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-monitoring-the-projected-inventory-level-and-the-reorder-point"></a><span data-ttu-id="c8837-103">Ontwerpdetails: Het verwachte voorraadniveau en het bestelpunt controleren</span><span class="sxs-lookup"><span data-stu-id="c8837-103">Design Details: Monitoring the Projected Inventory Level and the Reorder Point</span></span>
<span data-ttu-id="c8837-104">Voorraad is een soort aanbod, maar voor voorraadplanning maakt het planningssysteem onderscheid tussen twee voorraadniveaus:</span><span class="sxs-lookup"><span data-stu-id="c8837-104">Inventory is a type of supply, but for inventory planning, the planning system distinguishes between two inventory levels:</span></span>  

* <span data-ttu-id="c8837-105">Geplande voorraad</span><span class="sxs-lookup"><span data-stu-id="c8837-105">Projected inventory</span></span>  
* <span data-ttu-id="c8837-106">Geplande beschikbare voorraad</span><span class="sxs-lookup"><span data-stu-id="c8837-106">Projected available inventory</span></span>  

## <a name="projected-inventory"></a><span data-ttu-id="c8837-107">Geschatte inventaris</span><span class="sxs-lookup"><span data-stu-id="c8837-107">Projected Inventory</span></span>  
<span data-ttu-id="c8837-108">In eerste instantie is verwachte voorraad het aantal van de brutovoorraad, inclusief aanbod en vraag in het verleden, ook indien niet geboekt, wanneer het planningsproces wordt gestart.</span><span class="sxs-lookup"><span data-stu-id="c8837-108">Initially, projected inventory is the quantity of gross inventory, including supply and demand in the past even if not posted, when starting the planning process.</span></span> <span data-ttu-id="c8837-109">In de toekomst wordt dit een schommelend gepland voorraadniveau dat wordt onderhouden door bruto aantallen van toekomstige vraag en aanbod omdat deze worden geïntroduceerd op het tijdpad (gereserveerd of op een andere manier toegewezen).</span><span class="sxs-lookup"><span data-stu-id="c8837-109">In the future, this becomes a moving projected inventory level that is maintained by gross quantities from future supply and demand because those are introduced along the time line (whether reserved or in other ways allocated).</span></span>  

<span data-ttu-id="c8837-110">De geplande voorraad wordt gebruikt door het planningssysteem om het bestelpunt te controleren en het bestelaantal te bepalen wanneer het bestelbeleid Maximum aantal wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c8837-110">The projected inventory is used by the planning system to monitor the reorder point and to determine the reorder quantity when using the Maximum Qty. reordering policy.</span></span>  

## <a name="projected-available-inventory"></a><span data-ttu-id="c8837-111">Geplande beschikbare voorraad</span><span class="sxs-lookup"><span data-stu-id="c8837-111">Projected Available Inventory</span></span>  
<span data-ttu-id="c8837-112">De geplande beschikbare voorraad is het deel van de geplande voorraad dat op een bepaald moment beschikbaar is om aan de vraag te voldoen.</span><span class="sxs-lookup"><span data-stu-id="c8837-112">The projected available inventory is the part of the projected inventory that at a given point in time is available to fulfill demand.</span></span> <span data-ttu-id="c8837-113">De geplande beschikbare voorraad wordt gebruikt door de planningsengine voor het controleren van de veiligheidsvoorraad.</span><span class="sxs-lookup"><span data-stu-id="c8837-113">The projected available inventory is used by the planning engine when monitoring the safety stock level.</span></span>  

<span data-ttu-id="c8837-114">De geplande beschikbare voorraad wordt gebruikt door het planningssysteem om de veiligheidsvoorraad te controleren, aangezien de veiligheidsvoorraad altijd beschikbaar moet zijn om te voldoen aan onverwachte vraag.</span><span class="sxs-lookup"><span data-stu-id="c8837-114">The projected available inventory is used by the planning system to monitor the safety stock level, since the safety stock must always be available to serve unexpected demand.</span></span>  

## <a name="time-buckets"></a><span data-ttu-id="c8837-115">Tijdsintervallen</span><span class="sxs-lookup"><span data-stu-id="c8837-115">Time Buckets</span></span>  
<span data-ttu-id="c8837-116">Een strakke controle over de verwachte voorraad hebben, is van cruciaal belang om te detecteren wanneer het bestelpunt wordt bereikt of overschreden en om het juiste orderaantal te berekenen wanneer het bestelbeleid Maximum aantal wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c8837-116">Having a tight control of the projected inventory is crucial to detect when the reorder point is reached or crossed and to calculate the right order quantity when using the Maximum Qty. reordering policy.</span></span>  

<span data-ttu-id="c8837-117">Zoals eerder gezegd, wordt het verwachte voorraadniveau berekend aan het begin van de planningsperiode.</span><span class="sxs-lookup"><span data-stu-id="c8837-117">As stated earlier, the projected inventory level is calculated at the start of the planning period.</span></span> <span data-ttu-id="c8837-118">Het een brutoniveau is dat geen rekening houdt met reserveringen en soortgelijke toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="c8837-118">It is a gross level that does not consider reservations and similar allocations.</span></span> <span data-ttu-id="c8837-119">Om dit voorraadniveau te controleren tijdens de planningsreeks, controleert het systeem de samengevoegde wijzigingen gedurende een periode, een tijdsinterval.</span><span class="sxs-lookup"><span data-stu-id="c8837-119">To monitor this inventory level during the planning sequence, the system monitors the aggregated changes over a period of time, a time bucket.</span></span> <span data-ttu-id="c8837-120">Het systeem zorgt dat het tijdsinterval ten minste één dag is, aangezien dit de nauwkeurigste tijdseenheid is voor een vraag- of voorzieningsgebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="c8837-120">The system ensures that the time bucket is at least one day since it is the most precise unit of time for a demand or supply event.</span></span>  

## <a name="determining-the-projected-inventory-level"></a><span data-ttu-id="c8837-121">Het verwachte voorraadniveau bepalen</span><span class="sxs-lookup"><span data-stu-id="c8837-121">Determining the Projected Inventory Level</span></span>  
<span data-ttu-id="c8837-122">In de volgende reeks wordt beschreven hoe het voorspelde voorraadniveau wordt bepaald:</span><span class="sxs-lookup"><span data-stu-id="c8837-122">The following sequence describes how the projected inventory level is determined:</span></span>  

* <span data-ttu-id="c8837-123">Wanneer een voorzieningsgebeurtenis, zoals een inkooporder, totaal is gepland, wordt hiermee de geplande voorraad verhoogd op de vervaldatum.</span><span class="sxs-lookup"><span data-stu-id="c8837-123">When a supply event, such as a purchase order has been totally planned, it will increase the projected inventory on its due date.</span></span>  
* <span data-ttu-id="c8837-124">Wanneer aan een vraaggebeurtenis volledig is voldaan, wordt de geplande voorraad niet direct verminderd.</span><span class="sxs-lookup"><span data-stu-id="c8837-124">When a demand event has been fully satisfied, it will not decrease the projected inventory right away.</span></span> <span data-ttu-id="c8837-125">In plaats hiervan wordt een afnameaanmaning geboekt. Dat is een interne record die de datum en het aantal bevat van de bijdrage aan de verwachte voorraad.</span><span class="sxs-lookup"><span data-stu-id="c8837-125">Instead, it posts a decrease reminder, which is an internal record that holds the date and quantity of the contribution to the projected inventory.</span></span>  
* <span data-ttu-id="c8837-126">Wanneer een volgende voorzieningsgebeurtenis wordt gepland en op het tijdpad wordt geplaatst, worden de geboekte afnameaanmaningen een voor een onderzocht tot aan de geplande datum van de voorziening tijdens het bijwerken van de geplande voorraad.</span><span class="sxs-lookup"><span data-stu-id="c8837-126">When a subsequent supply event is planned and placed on the time line, the posted decrease reminders are investigated one by one up until the planned date of the supply while updating the projected inventory.</span></span> <span data-ttu-id="c8837-127">Tijdens dit proces kan het bestelpuntniveau van de interne toenameherinnering worden bereikt of overschreden.</span><span class="sxs-lookup"><span data-stu-id="c8837-127">During this process, the reorder point level of the internal increase reminder may be reached or crossed.</span></span>  
* <span data-ttu-id="c8837-128">Als een nieuwe voorzieningenorder wordt geïntroduceerd, controleert het systeem of het vóór de huidige voorziening wordt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="c8837-128">If a new supply order is introduced, the system checks if it is entered before the current supply.</span></span> <span data-ttu-id="c8837-129">Als dat zo is, wordt de nieuwe voorziening de huidige voorziening en begint de vereffeningsprocedure opnieuw.</span><span class="sxs-lookup"><span data-stu-id="c8837-129">If it is, the new supply becomes current supply and the balancing procedure starts over.</span></span>  

<span data-ttu-id="c8837-130">Hierna wordt een grafische illustratie van dit principe getoond:</span><span class="sxs-lookup"><span data-stu-id="c8837-130">The following shows a graphical illustration of this principle:</span></span>  

<span data-ttu-id="c8837-131">![](media/nav_app_supply_planning_2_projected_inventory.png "NAV_APP_supply_planning_2_projected_inventory")</span><span class="sxs-lookup"><span data-stu-id="c8837-131">![](media/nav_app_supply_planning_2_projected_inventory.png "NAV_APP_supply_planning_2_projected_inventory")</span></span>  

1. <span data-ttu-id="c8837-132">Voorziening **Sa** van 4 (vast) sluit vraag **Da** van -3 af.</span><span class="sxs-lookup"><span data-stu-id="c8837-132">Supply **Sa** of 4 (fixed) closes Demand **Da** of -3.</span></span>  
2. <span data-ttu-id="c8837-133">CloseDemand: Maak een afnameaanmaning van -3 (niet weergegeven).</span><span class="sxs-lookup"><span data-stu-id="c8837-133">CloseDemand: Create a decrease reminder of -3 (not shown).</span></span>  
3. <span data-ttu-id="c8837-134">Voorziening **Sa** is afgesloten met een overschot van 1 (er bestaat geen vraag meer).</span><span class="sxs-lookup"><span data-stu-id="c8837-134">Supply **Sa** is closed with a surplus of 1 (no more demand exists).</span></span>  

     <span data-ttu-id="c8837-135">Hiermee wordt het geplande voorraadniveau verhoogd naar +4, terwijl de geplande **beschikbare** voorraad -1 wordt.</span><span class="sxs-lookup"><span data-stu-id="c8837-135">This increases the projected inventory level to +4, while the projected **available** inventory becomes -1.</span></span>  

4. <span data-ttu-id="c8837-136">De volgende voorziening **Sb** van 2 (een andere order) is al ingesteld op de tijdlijn.</span><span class="sxs-lookup"><span data-stu-id="c8837-136">The next supply **Sb** of 2 (another order) has already been placed on the timeline.</span></span>  
5. <span data-ttu-id="c8837-137">Er wordt gecontroleerd of er afnameaanmaningen zijn voorafgaand aan **Sb** (die zijn er niet, dus er wordt geen actie ondernomen.)</span><span class="sxs-lookup"><span data-stu-id="c8837-137">System checks if there is any decrease reminder preceding **Sb** (there is not, so no action is taken).</span></span>  
6. <span data-ttu-id="c8837-138">Het systeem sluit voorziening **Sb** (er bestaat geen vraag meer) door A: het te verlagen tot 0 (annuleren), of B: het te laten zoals het is.</span><span class="sxs-lookup"><span data-stu-id="c8837-138">System closes supply **Sb** (no more demand exists)—either A: by reducing it to 0 (cancel) or B: by leaving as is.</span></span>  

     <span data-ttu-id="c8837-139">Hiermee wordt het voorspelde voorraadniveau verhoogd (A: +0 => +4 of B: +2 = +6).</span><span class="sxs-lookup"><span data-stu-id="c8837-139">This increases the projected inventory level (A: +0 => +4 or B: +2 = +6).</span></span>  

7. <span data-ttu-id="c8837-140">Er wordt een laatste controle gedaan: zijn er eventuele afnameaanmaningen?</span><span class="sxs-lookup"><span data-stu-id="c8837-140">System makes a final check: Is there any decrease reminder?</span></span> <span data-ttu-id="c8837-141">Ja, er is één op de datum van **Da**.</span><span class="sxs-lookup"><span data-stu-id="c8837-141">Yes, there is one on the date of **Da**.</span></span>  
8. <span data-ttu-id="c8837-142">Het systeem voegt de afnameherinnering -3 toe aan het verwachte voorraadniveau, hetzij A: +4 -3 = 1 of B: +6 -3 = +3.</span><span class="sxs-lookup"><span data-stu-id="c8837-142">System adds the decrease reminder of -3 reminder to the projected inventory level, either A: +4 -3 = 1 or B: +6 -3 = +3.</span></span>  
9. <span data-ttu-id="c8837-143">In het geval van A maakt het systeem een voorwaarts geplande order die begint op de datum **Da**.</span><span class="sxs-lookup"><span data-stu-id="c8837-143">In case of A, the system creates a forward-scheduled order starting on date **Da**.</span></span>  

     <span data-ttu-id="c8837-144">In het geval van B, wordt het bestelpunt bereikt en wordt een nieuwe order gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c8837-144">In case of B, the reorder point is reached and a new order is created.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c8837-145">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c8837-145">See Also</span></span>  
<span data-ttu-id="c8837-146">[Ontwerpdetails: Bestelbeleid](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="c8837-146">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="c8837-147">[Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="c8837-147">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="c8837-148">[Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="c8837-148">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="c8837-149">Ontwerpdetails: Voorraadplanning</span><span class="sxs-lookup"><span data-stu-id="c8837-149">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

