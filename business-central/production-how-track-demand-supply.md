---
title: Relatie tussen vraag en aanbod bijhouden | Microsoft Docs
description: Vanuit elk document voor aanbod of vraag in het zogenaamde ordernetwerk kunt u de ordervraag (getraceerd aantal), prognose , raamverkooporder of planningsparameter (niet-getraceerd aantal) traceren die een planningregel heeft doen stijgen.
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
ms.openlocfilehash: 2300cc6e3f4c429cd73a17939420a44b846a3b13
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="track-relations-between-demand-and-supply"></a><span data-ttu-id="a8a12-103">Relaties tussen vraag en aanbod bijhouden</span><span class="sxs-lookup"><span data-stu-id="a8a12-103">Track Relations Between Demand and Supply</span></span>
<span data-ttu-id="a8a12-104">Vanuit elk document voor aanbod of vraag in het zogenaamde ordernetwerk kunt u de ordervraag (getraceerd aantal), prognose , raamverkooporder of planningsparameter (niet-getraceerd aantal) traceren die een planningregel heeft doen stijgen.</span><span class="sxs-lookup"><span data-stu-id="a8a12-104">From any supply or demand document in the so-called order network, you can track the order demand (tracked quantity), forecast, blanket sales order, or planning parameter (untracked quantity) that has given rise to the planning line in question.</span></span>

<span data-ttu-id="a8a12-105">De planningsvoorstellen bevatten ook ondersteunende planninginformatie over entiteiten die geen orders zijn om de planner te helpen een optimaal leveringsplan op te stellen.</span><span class="sxs-lookup"><span data-stu-id="a8a12-105">The planning worksheets also offers supporting planning information about non-order entities to help the planner obtain an optimal supply plan.</span></span> <span data-ttu-id="a8a12-106">Zie de sectie Niet-getraceerde planningselementen voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="a8a12-106">For more information, see the "Untracked Planning Elements" section.</span></span>

## <a name="to-track-linked-items"></a><span data-ttu-id="a8a12-107">Gekoppelde artikelen traceren</span><span class="sxs-lookup"><span data-stu-id="a8a12-107">To track linked items</span></span>
<span data-ttu-id="a8a12-108">Met behulp van ordertracering kunt u nagaan hoe verkooporders, productieorders en inkooporders aan de productieorder zijn gekoppeld via de plannings- en reserveringssystemen.</span><span class="sxs-lookup"><span data-stu-id="a8a12-108">Order tracking shows how sales orders, production orders, and purchase orders are related to the manufacturing order through the planning and reservation systems.</span></span>

<span data-ttu-id="a8a12-109">Hieronder wordt beschreven hoe u gekoppelde artikelen in een vast geplande productieorder traceert.</span><span class="sxs-lookup"><span data-stu-id="a8a12-109">The following describes how to track linked items on a firm planned production order.</span></span> <span data-ttu-id="a8a12-110">De stappen voor alle andere soorten orders en vanuit planningsvoorstelregels zijn vergelijkbaar.</span><span class="sxs-lookup"><span data-stu-id="a8a12-110">The steps are similar for all other order types, and from planning worksheet lines.</span></span>

1. <span data-ttu-id="a8a12-111">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vast geplande productieorder** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="a8a12-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Order**, and then choose the related link.</span></span>
2. <span data-ttu-id="a8a12-112">Open de betreffende vast geplande productieorder in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a8a12-112">Open the relevant firm planned production order from the list.</span></span>
3. <span data-ttu-id="a8a12-113">Op het sneltabblad **Regels** kiest u de actie **Functies** en vervolgens **Ordertracering**.</span><span class="sxs-lookup"><span data-stu-id="a8a12-113">On the **Lines** FastTab, choose the **Functions** action, and then choose the **Order Tracking** action.</span></span>

<span data-ttu-id="a8a12-114">Op de regels in het venster **Ordertracering** worden de documenten weergegeven die zijn gekoppeld aan de huidige productieorderregel.</span><span class="sxs-lookup"><span data-stu-id="a8a12-114">The lines in the **Order Tracking** display the documents that are related to the current production order line.</span></span>

## <a name="untracked-planning-elements"></a><span data-ttu-id="a8a12-115">Niet-getraceerde planningselementen</span><span class="sxs-lookup"><span data-stu-id="a8a12-115">Untracked Planning Elements</span></span>
<span data-ttu-id="a8a12-116">Het venster **Niet-getraceerde planningselementen** wordt geopend wanneer u het veld **Niet-getraceerd aantal** in het venster **Orderplanning** kiest.</span><span class="sxs-lookup"><span data-stu-id="a8a12-116">The **Untracked Planning Elements** window opens when you choose the **Untracked Qty.** field in the **order Planning** window.</span></span> <span data-ttu-id="a8a12-117">Dit dient twee doelen:</span><span class="sxs-lookup"><span data-stu-id="a8a12-117">It serves two purposes:</span></span>

1. <span data-ttu-id="a8a12-118">De tabel bevat informatie over ongetraceerde hoeveelheden die worden weergegeven wanneer de gebruiker opzoekt in het venster Ordertracering om de ongetraceerde aantallen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="a8a12-118">To hold information about untracked quantities displayed when the user looks up from the Order Tracking window to see untracked quantities.</span></span>
2. <span data-ttu-id="a8a12-119">De tabel bevat waarschuwingsberichten die worden weergegeven wanneer de gebruiker op het pictogram **Waarschuwing** in het venster **Planningsvoorstel** klikt.</span><span class="sxs-lookup"><span data-stu-id="a8a12-119">To hold warning messages displayed when the user chooses the **Warning** icon in the **Planning Worksheet** window.</span></span>

<span data-ttu-id="a8a12-120">Het venster bevat posten die een verklaring kunnen geven voor niet-getraceerde overschotaantallen in het ordertraceringsnetwerk.</span><span class="sxs-lookup"><span data-stu-id="a8a12-120">The window contains entries which account for an untracked surplus quantity in order tracking network.</span></span> <span data-ttu-id="a8a12-121">Deze posten worden gegenereerd tijdens het planningsproces en verklaren waar het niet-getraceerde overschotaantal in de ordertraceringsregels vandaan kwam.</span><span class="sxs-lookup"><span data-stu-id="a8a12-121">These entries are generated during the planning run and explain where the untracked surplus quantity in the order tracking lines came from.</span></span> <span data-ttu-id="a8a12-122">Dit niet-getraceerde overschot kan afkomstig zijn uit:</span><span class="sxs-lookup"><span data-stu-id="a8a12-122">This untracked surplus can come from:</span></span>

- <span data-ttu-id="a8a12-123">Productieprognose</span><span class="sxs-lookup"><span data-stu-id="a8a12-123">Production forecast</span></span>
- <span data-ttu-id="a8a12-124">Raamcontractenorders</span><span class="sxs-lookup"><span data-stu-id="a8a12-124">Blanket orders</span></span>
- <span data-ttu-id="a8a12-125">Veiligheidsvoorraad</span><span class="sxs-lookup"><span data-stu-id="a8a12-125">Safety stock quantity</span></span>
- <span data-ttu-id="a8a12-126">Bestelpunt</span><span class="sxs-lookup"><span data-stu-id="a8a12-126">Reorder point</span></span>
- <span data-ttu-id="a8a12-127">Maximale voorraad</span><span class="sxs-lookup"><span data-stu-id="a8a12-127">Maximum inventory</span></span>
- <span data-ttu-id="a8a12-128">Bestelaantal</span><span class="sxs-lookup"><span data-stu-id="a8a12-128">Reorder quantity</span></span>
- <span data-ttu-id="a8a12-129">Max. bestelaantal</span><span class="sxs-lookup"><span data-stu-id="a8a12-129">Maximum order quantity</span></span>
- <span data-ttu-id="a8a12-130">Min. bestelaantal</span><span class="sxs-lookup"><span data-stu-id="a8a12-130">Minimum order quantity</span></span>
- <span data-ttu-id="a8a12-131">Vaste lotgrootte</span><span class="sxs-lookup"><span data-stu-id="a8a12-131">Order multiple</span></span>
- <span data-ttu-id="a8a12-132">Demping (% van lotgrootte)</span><span class="sxs-lookup"><span data-stu-id="a8a12-132">Dampener (% of lot size)</span></span>

## <a name="see-also"></a><span data-ttu-id="a8a12-133">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a8a12-133">See Also</span></span>  
<span data-ttu-id="a8a12-134">[Gepland](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="a8a12-134">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="a8a12-135">Productie instellen</span><span class="sxs-lookup"><span data-stu-id="a8a12-135">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="a8a12-136">[Productie](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="a8a12-136">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="a8a12-137">Voorraad</span><span class="sxs-lookup"><span data-stu-id="a8a12-137">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="a8a12-138">Inkoop</span><span class="sxs-lookup"><span data-stu-id="a8a12-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="a8a12-139">Ontwerpdetails: Reservering, tracering en planningsboodschappen</span><span class="sxs-lookup"><span data-stu-id="a8a12-139">Design Details: Reservation, Tracking, and Action Messaging</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
<span data-ttu-id="a8a12-140">[Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="a8a12-140">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="a8a12-141">Aanbevolen procedures instellen: voorraadplanning</span><span class="sxs-lookup"><span data-stu-id="a8a12-141">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="a8a12-142">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a8a12-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

