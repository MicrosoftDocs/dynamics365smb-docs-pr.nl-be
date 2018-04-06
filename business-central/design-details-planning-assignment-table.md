---
title: 'Ontwerpdetails: Tabel Planningstoewijzing | Microsoft Docs'
description: Dit onderwerp biedt inzicht in wat er gebeurt wanneer u wijzigt hoe u plant voor een artikel.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3e412c6fe82b3ee5640329c523b19d68f849f93a
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-planning-assignment-table"></a><span data-ttu-id="facda-103">Ontwerpdetails: Tabel Planningstoewijzing</span><span class="sxs-lookup"><span data-stu-id="facda-103">Design Details: Planning Assignment Table</span></span>
<span data-ttu-id="facda-104">Alle artikelen moeten worden gepland, maar er is geen reden om een planning voor een artikel te berekenen tenzij er een verandering in het vraag- of aanbodpatroon is opgetreden sinds er voor het laatst een planning is berekend.</span><span class="sxs-lookup"><span data-stu-id="facda-104">All items should be planned for, however, there is no reason to calculate a plan for an item unless there has been a change in the demand or supply pattern since the last time a plan was calculated.</span></span>  
  
<span data-ttu-id="facda-105">Als de gebruiker een nieuwe verkooporder heeft ingevoerd of een bestaande heeft gewijzigd, is er reden om de planning opnieuw te berekenen.</span><span class="sxs-lookup"><span data-stu-id="facda-105">If the user has entered a new sales order or changed an existing one, there is reason to recalculate the plan.</span></span> <span data-ttu-id="facda-106">Andere redenen omvatten een wijziging in de voorspelde of gewenste veiligheidsvoorraad.</span><span class="sxs-lookup"><span data-stu-id="facda-106">Other reasons include a change in forecast or the desired safety stock quantity.</span></span> <span data-ttu-id="facda-107">Het wijzigen van een stuklijst door een materiaal toe te voegen of te verwijderen duidt waarschijnlijk op een wijziging, maar alleen voor het onderdeelartikel.</span><span class="sxs-lookup"><span data-stu-id="facda-107">Changing a bill of material by adding or removing a component would most likely indicate a change, but for the component item only.</span></span>  
  
<span data-ttu-id="facda-108">Voor meerdere vestigingen vindt de toewijzing plaats op het niveau van de combinatie artikel per vestiging.</span><span class="sxs-lookup"><span data-stu-id="facda-108">For multiple locations, the assignment takes place at the level of item per location combination.</span></span> <span data-ttu-id="facda-109">Wanneer bijvoorbeeld een verkooporder op slechts één vestiging is gemaakt, wordt het artikel in die specifieke vestiging voor planning toegewezen.</span><span class="sxs-lookup"><span data-stu-id="facda-109">If, for example, a sales order has been created at only one location, the program will assign the item at that specific location for planning.</span></span>  
  
<span data-ttu-id="facda-110">De reden voor het selecteren van artikelen voor planning heeft te maken met systeemprestaties.</span><span class="sxs-lookup"><span data-stu-id="facda-110">The reason for selecting items for planning is a matter of system performance.</span></span> <span data-ttu-id="facda-111">Als er geen verschil is opgetreden in het vraag/aanbod-patroon van een artikel, zal het planningssysteem geen uit te voeren acties voorstellen.</span><span class="sxs-lookup"><span data-stu-id="facda-111">If no change in an item’s demand-supply pattern has occurred, the planning system will not suggest any actions to be taken.</span></span> <span data-ttu-id="facda-112">Zonder de planningstoewijzing moet het systeem de berekeningen voor alle artikelen uitvoeren om te weten waarvoor moet worden gepland, en dat zou de systeembronnen uitputten.</span><span class="sxs-lookup"><span data-stu-id="facda-112">Without the planning assignment, the system would have to perform the calculations for all items in order to find out what to plan for, and that would drain system resources.</span></span>  
  
<span data-ttu-id="facda-113">De tabel **Planningsopdracht** bewaakt vraag- en aanbodgebeurtenissen en wijst de benodigde artikelen toe aan de planning.</span><span class="sxs-lookup"><span data-stu-id="facda-113">The **Planning Assignment** table monitors demand and supply events and assigns the appropriate items for planning.</span></span> <span data-ttu-id="facda-114">De volgende gebeurtenissen worden gecontroleerd:</span><span class="sxs-lookup"><span data-stu-id="facda-114">The following events are monitored:</span></span>  
  
* <span data-ttu-id="facda-115">Een nieuwe verkooporder, prognose, onderdeel, inkooporder, productieorder, assemblageorder of transferorder.</span><span class="sxs-lookup"><span data-stu-id="facda-115">A new sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="facda-116">Wijziging van een artikel, aantal, locatie, variant of datum in een verkooporder, prognose, onderdeel, inkooporder, productieorder, assemblageorder of transferorder.</span><span class="sxs-lookup"><span data-stu-id="facda-116">Change of item, quantity, location, variant, or date on a sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="facda-117">Annulering van een verkooporder, prognose, onderdeel, inkooporder, productieorder, assemblageorder of transferorder.</span><span class="sxs-lookup"><span data-stu-id="facda-117">Cancellation of a sales order, forecast, component, purchase order, production order, assembly order, or transfer order.</span></span>  
* <span data-ttu-id="facda-118">Verbruik van andere dan geplande artikelen.</span><span class="sxs-lookup"><span data-stu-id="facda-118">Consumption of items other than planned.</span></span>  
* <span data-ttu-id="facda-119">Output van andere dan geplande artikelen.</span><span class="sxs-lookup"><span data-stu-id="facda-119">Output of items other than planned.</span></span>  
* <span data-ttu-id="facda-120">Niet-geplande wijzigingen in voorraad.</span><span class="sxs-lookup"><span data-stu-id="facda-120">Unplanned changes in inventory.</span></span>  
  
<span data-ttu-id="facda-121">Voor deze directe aanbod-vraag verplaatsingen onderhoudt het ordertracerings- en planningsboodschapsysteem de tabel Planningstoewijzing en geeft het een planningsreden als een planningsboodschap.</span><span class="sxs-lookup"><span data-stu-id="facda-121">For these direct supply-demand displacements, the order tracking and action messaging system maintains the Planning Assignment table and states a planning reason as an action message.</span></span>  
  
<span data-ttu-id="facda-122">De volgende wijzigingen in stamgegevens kunnen ook een verstoord evenwicht in de planning veroorzaken:</span><span class="sxs-lookup"><span data-stu-id="facda-122">The following changes in master data can also cause a planning imbalance:</span></span>  
  
* <span data-ttu-id="facda-123">Wijziging van status in Gecertificeerd in de productiestuklijstkop (voor alle artikelen die de kop gebruiken).</span><span class="sxs-lookup"><span data-stu-id="facda-123">Change of status to Certified in the production BOM header (for all items using that header).</span></span>  
* <span data-ttu-id="facda-124">Verwijderde regel (onderliggend artikel).</span><span class="sxs-lookup"><span data-stu-id="facda-124">Deleted line (child item).</span></span>  
* <span data-ttu-id="facda-125">Wijziging van status in Gecertificeerd in de bewerkingsplankop (voor alle artikelen die het bewerkingsplan gebruiken).</span><span class="sxs-lookup"><span data-stu-id="facda-125">Change of status to Certified in the routing header (for all items using that routing).</span></span>  
* <span data-ttu-id="facda-126">Wijzigingen in de volgende artikelkaartvelden.</span><span class="sxs-lookup"><span data-stu-id="facda-126">Changes in the following item card fields.</span></span>  
* <span data-ttu-id="facda-127">Veiligheidsvoorraad of veiligheidstijd.</span><span class="sxs-lookup"><span data-stu-id="facda-127">Safety Stock Quantity or Safety Lead Time.</span></span>  
* <span data-ttu-id="facda-128">Levertermijn.</span><span class="sxs-lookup"><span data-stu-id="facda-128">Lead Time Calculation.</span></span>  
* <span data-ttu-id="facda-129">Bestelpunt.</span><span class="sxs-lookup"><span data-stu-id="facda-129">Reorder Point.</span></span>  
* <span data-ttu-id="facda-130">Productiestuklijstnr. (en alle onderliggende elementen van oude stuklijstverwijzing).</span><span class="sxs-lookup"><span data-stu-id="facda-130">Production BOM No. (and all children of old BOM reference).</span></span>  
* <span data-ttu-id="facda-131">Bew.-plannr.</span><span class="sxs-lookup"><span data-stu-id="facda-131">Routing No.</span></span>  
* <span data-ttu-id="facda-132">Bestelbeleid.</span><span class="sxs-lookup"><span data-stu-id="facda-132">Reordering Policy.</span></span>  
  
<span data-ttu-id="facda-133">In deze gevallen onderhoudt een nieuwe functie, Beheer planningstoewijzing, de tabel en wordt als planningsreden Mutatie vermeld.</span><span class="sxs-lookup"><span data-stu-id="facda-133">In these cases, a new function, Planning Assignment Management, maintains the table and states the planning reason as Net Change.</span></span>  
  
<span data-ttu-id="facda-134">De volgende wijzigingen hebben geen planningsopdracht als gevolg:</span><span class="sxs-lookup"><span data-stu-id="facda-134">The following changes do not cause a planning assignment:</span></span>  
  
* <span data-ttu-id="facda-135">Agenda's</span><span class="sxs-lookup"><span data-stu-id="facda-135">Calendars</span></span>  
* <span data-ttu-id="facda-136">Overige planningsparameters op de artikelkaart</span><span class="sxs-lookup"><span data-stu-id="facda-136">Other planning parameters on the item card</span></span>  
  
<span data-ttu-id="facda-137">Bij het berekenen van een MPS of MRP gelden de volgende beperkingen:</span><span class="sxs-lookup"><span data-stu-id="facda-137">When calculating an MPS or an MRP, the following restrictions apply:</span></span>  
  
* <span data-ttu-id="facda-138">MPS: Het planningssysteem controleert of het artikel een productieprognose of een verkooporder heeft.</span><span class="sxs-lookup"><span data-stu-id="facda-138">MPS: The planning system checks that the item carries a production forecast or a sales order.</span></span> <span data-ttu-id="facda-139">Zo niet, dan wordt het artikel niet opgenomen in de planning.</span><span class="sxs-lookup"><span data-stu-id="facda-139">If not, the item is not included in the plan.</span></span>  
* <span data-ttu-id="facda-140">MRP: Wanneer het planningssysteem ontdekt dat het artikel wordt aangevuld door een MPS-planningsregel of een MPS-voorzieningenorder, wordt het artikel uit de planning gelaten.</span><span class="sxs-lookup"><span data-stu-id="facda-140">MRP: If the planning system detects that the item is being replenished by an MPS planning line or MPS supply order, the item will be left out of the planning.</span></span> <span data-ttu-id="facda-141">Vraag van relevante onderdelen wordt echter opgenomen.</span><span class="sxs-lookup"><span data-stu-id="facda-141">However, any demand from relevant components is included.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="facda-142">Zie ook</span><span class="sxs-lookup"><span data-stu-id="facda-142">See Also</span></span>  
<span data-ttu-id="facda-143">[Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="facda-143">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="facda-144">[Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="facda-144">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
<span data-ttu-id="facda-145">[Ontwerpdetails: Transfers in planning](design-details-transfers-in-planning.md) </span><span class="sxs-lookup"><span data-stu-id="facda-145">[Design Details: Transfers in Planning](design-details-transfers-in-planning.md) </span></span>  
[<span data-ttu-id="facda-146">Ontwerpdetails: Planningsparameters</span><span class="sxs-lookup"><span data-stu-id="facda-146">Design Details: Planning Parameters</span></span>](design-details-planning-parameters.md)  

