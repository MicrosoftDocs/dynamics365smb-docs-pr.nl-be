---
title: Serviceorderstatus en herstelstatus
description: Tussen het veld Status op de pagina Serviceorder en de herstelstatus van het serviceartikel, weergegeven in het veld Herstelstatuscode op de pagina Serviceorder, bestaat een bepaalde relatie in de module CRM - Service. Met de serviceorderstatus wordt de herstelstatus van de serviceartikelen in de serviceorder aangegeven.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/15/2020
ms.author: edupont
ms.openlocfilehash: 9bbe3a4263250a7d06bfffa2019114eba72a31ca
ms.sourcegitcommit: 2d2dfb6c3eca1322835f0167dc7dab614346972e
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/19/2020
ms.locfileid: "4038631"
---
# <a name="service-order-status-and-repair-status"></a><span data-ttu-id="26201-104">Serviceorderstatus en herstelstatus</span><span class="sxs-lookup"><span data-stu-id="26201-104">Service Order Status and Repair Status</span></span>

<span data-ttu-id="26201-105">Tussen het veld **Status** op de pagina **Serviceorder** en de herstelstatus van het serviceartikel, weergegeven in het veld **Herstelstatuscode** op de pagina **Serviceorder**, bestaat een bepaalde relatie in de module CRM - Service.</span><span class="sxs-lookup"><span data-stu-id="26201-105">The **Status** field on the **Service Order** page and the service item repair status, which is represented by the **Repair Status Code** field on the **Service Order** page have a certain relationship in Service Management.</span></span> <span data-ttu-id="26201-106">Met de serviceorderstatus wordt de herstelstatus van de serviceartikelen in de serviceorder aangegeven.</span><span class="sxs-lookup"><span data-stu-id="26201-106">The service order status reflects the repair status of all the service items in the service order.</span></span>  

> [!NOTE]  
> <span data-ttu-id="26201-107">Deze twee statusvelden zijn niet gerelateerd aan het veld **Vrijgavestatus** op de serviceorderkop, dat bepaalt hoe serviceartikelen in het magazijn worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="26201-107">These two status field are not related to the **Release Status** field on the service order header, which determines how the warehouse handles service items.</span></span>  

<span data-ttu-id="26201-108">Telkens wanneer de herstelstatus van een serviceartikel wordt gewijzigd in een serviceorder, wordt de orderstatus bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="26201-108">Each time the repair status of a service item is changed in a service order, the status of the order is updated.</span></span> <span data-ttu-id="26201-109">Als de algemene herstelstatus van de afzonderlijke serviceartikelen moet worden aangegeven, moet u het volgende opgeven:</span><span class="sxs-lookup"><span data-stu-id="26201-109">To display the status that reflects the overall repair status of the individual service items, you must specify the following:</span></span>  

* <span data-ttu-id="26201-110">De serviceorderstatus die aan elke herstelstatus is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="26201-110">The service order status that each repair status is linked to.</span></span>  
* <span data-ttu-id="26201-111">Het prioriteitsniveau van elke optie voor serviceorderstatus.</span><span class="sxs-lookup"><span data-stu-id="26201-111">The level of priority of each service order status option.</span></span>  

<span data-ttu-id="26201-112">Wanneer u een serviceofferte omzet in een serviceorder, wordt de herstelstatus van elk serviceartikel in de order gewijzigd in **Eerste** en de serviceorderstatus in **In behandeling**.</span><span class="sxs-lookup"><span data-stu-id="26201-112">When you convert a service quote to a service order, the repair status of each service item is changed in the order to **Initial** and the service order status is changed to **Pending**.</span></span>  

> [!NOTE]
> <span data-ttu-id="26201-113">Voordat u serviceorders kunt maken, moet u reparatiestatussen en servicestatusprioriteiten instellen.</span><span class="sxs-lookup"><span data-stu-id="26201-113">Before you can create service orders, you must set up repair statuses and service status priorities.</span></span> <span data-ttu-id="26201-114">Zie voor meer informatie [Statussen instellen voor serviceorders en reparaties](service-order-repair-status.md).</span><span class="sxs-lookup"><span data-stu-id="26201-114">For more information, see [Set Up Statuses for Service Orders and Repairs](service-order-repair-status.md).</span></span>

## <a name="specifying-service-order-status-for-repair-status"></a><span data-ttu-id="26201-115">Serviceorderstatus opgeven voor herstelstatus</span><span class="sxs-lookup"><span data-stu-id="26201-115">Specifying Service Order Status for Repair Status</span></span>

<span data-ttu-id="26201-116">Elke herstelstatus is gekoppeld aan een bepaalde serviceorderstatus.</span><span class="sxs-lookup"><span data-stu-id="26201-116">Each repair status is linked to a particular service order status.</span></span> <span data-ttu-id="26201-117">De opties voor de serviceorderstatus zijn als volgt:</span><span class="sxs-lookup"><span data-stu-id="26201-117">The options for the service order status are as follows:</span></span>

* <span data-ttu-id="26201-118">**In behandeling**</span><span class="sxs-lookup"><span data-stu-id="26201-118">**Pending**</span></span>
* <span data-ttu-id="26201-119">**In verwerking**</span><span class="sxs-lookup"><span data-stu-id="26201-119">**In Process**</span></span>
* <span data-ttu-id="26201-120">**Afwachten**</span><span class="sxs-lookup"><span data-stu-id="26201-120">**On Hold**</span></span>
* <span data-ttu-id="26201-121">**Gereedgemeld**</span><span class="sxs-lookup"><span data-stu-id="26201-121">**Finished**</span></span>

<span data-ttu-id="26201-122">De opties voor de reparatiestatus zijn als volgt:</span><span class="sxs-lookup"><span data-stu-id="26201-122">The repair status options are as follows:</span></span>

* <span data-ttu-id="26201-123">**Eerste**</span><span class="sxs-lookup"><span data-stu-id="26201-123">**Initial**</span></span>
* <span data-ttu-id="26201-124">**In verwerking**</span><span class="sxs-lookup"><span data-stu-id="26201-124">**In Process**</span></span>
* <span data-ttu-id="26201-125">**Toegewezen**</span><span class="sxs-lookup"><span data-stu-id="26201-125">**Referred**</span></span>
* <span data-ttu-id="26201-126">**Deels service verleend**</span><span class="sxs-lookup"><span data-stu-id="26201-126">**Partly Serviced**</span></span>
* <span data-ttu-id="26201-127">**Offerte gereed**</span><span class="sxs-lookup"><span data-stu-id="26201-127">**Quote Finished**</span></span>
* <span data-ttu-id="26201-128">**Wachten op klant**</span><span class="sxs-lookup"><span data-stu-id="26201-128">**Waiting for Customer**</span></span>
* <span data-ttu-id="26201-129">**Reserveonderdeel besteld**</span><span class="sxs-lookup"><span data-stu-id="26201-129">**Spare Part Ordered**</span></span>
* <span data-ttu-id="26201-130">**Reserveonderdeel ontvangen**</span><span class="sxs-lookup"><span data-stu-id="26201-130">**Spare Part Received**</span></span>
* <span data-ttu-id="26201-131">**Gereedgemeld**</span><span class="sxs-lookup"><span data-stu-id="26201-131">**Finished**</span></span>  

### <a name="pending"></a><span data-ttu-id="26201-132">In behandeling</span><span class="sxs-lookup"><span data-stu-id="26201-132">Pending</span></span>

<span data-ttu-id="26201-133">Met de serviceorderstatus **In behandeling** wordt aangegeven dat de service op elk moment kan worden begonnen of hervat.</span><span class="sxs-lookup"><span data-stu-id="26201-133">The service order status **Pending** indicates that the service can start or continue at any time.</span></span> <span data-ttu-id="26201-134">De herstelstatusopties **Eerste**, **Toegewezen**, **Deels service verleend** en **Reserveonderdeel ontvangen** kunnen daarom worden gekoppeld aan deze serviceorderstatus.</span><span class="sxs-lookup"><span data-stu-id="26201-134">Therefore, the repair status options of **Initial**, **Referred**, **Partly Serviced**, and **Spare Part Received** can be linked to this service order status.</span></span>  

### <a name="in-process"></a><span data-ttu-id="26201-135">In verwerking</span><span class="sxs-lookup"><span data-stu-id="26201-135">In Process</span></span>

<span data-ttu-id="26201-136">Met de serviceorderstatus **In verwerking** wordt aangegeven dat de service wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="26201-136">The service order status **In Process** indicates that the service is in process.</span></span> <span data-ttu-id="26201-137">De herstelstatusopties **In verwerking** en **Reserveonderdeel besteld** kunnen daarom worden gekoppeld aan deze serviceorderstatus.</span><span class="sxs-lookup"><span data-stu-id="26201-137">Therefore, the repair status options **In Process** and **Spare Part Ordered** can both be linked to this service order status.</span></span> <span data-ttu-id="26201-138">Als u de status **Reserveonderdeel besteld** koppelt aan de serviceorderstatus **In verwerking**, moet u ook de status **Reserveonderdeel ontvangen** koppelen aan deze serviceorderstatus.</span><span class="sxs-lookup"><span data-stu-id="26201-138">If you link the **Spare Part Ordered** status to an **In Process** service order status, you must also link the **Spare Part Received** status to this service order status.</span></span>  

### <a name="on-hold"></a><span data-ttu-id="26201-139">Wachten</span><span class="sxs-lookup"><span data-stu-id="26201-139">On Hold</span></span>

<span data-ttu-id="26201-140">Met de serviceorderstatus **Afwachten** wordt aangegeven dat de service tijdelijk is stilgelegd, omdat u op een antwoord van de klant of op reserveonderdelen wacht voordat de service kan worden begonnen.</span><span class="sxs-lookup"><span data-stu-id="26201-140">The service order status **On Hold** indicates that the service is temporarily on hold because you are waiting for a customer response or spare parts before the service can start.</span></span> <span data-ttu-id="26201-141">De herstelstatusopties **Offerte gereed**, **Reserveonderdeel besteld** en **Wachten op klant** kunnen daarom worden gekoppeld aan deze serviceorderstatus.</span><span class="sxs-lookup"><span data-stu-id="26201-141">Therefore, the repair status options of **Quote Finished**, **Spare Part Ordered**, and **Waiting for Customer** can be linked to this service order status.</span></span>  

### <a name="finished"></a><span data-ttu-id="26201-142">Gereedgemeld</span><span class="sxs-lookup"><span data-stu-id="26201-142">Finished</span></span>

<span data-ttu-id="26201-143">Met de serviceorderstatus **Gereedgemeld** wordt aangegeven dat de service is voltooid.</span><span class="sxs-lookup"><span data-stu-id="26201-143">The service order status **Finished** indicates that the service has been completed.</span></span> <span data-ttu-id="26201-144">De herstelstatus **Gereedgemeld** is daarom gekoppeld aan deze status.</span><span class="sxs-lookup"><span data-stu-id="26201-144">Therefore, the **Finished** repair status is linked to this status.</span></span>  

## <a name="assigning-priority-to-service-order-status"></a><span data-ttu-id="26201-145">Prioriteit toewijzen aan serviceorderstatus</span><span class="sxs-lookup"><span data-stu-id="26201-145">Assigning Priority to Service Order Status</span></span>

<span data-ttu-id="26201-146">Wanneer een herstelstatus van een serviceartikel wordt gewijzigd, worden de opties voor serviceorderstatus geïdentificeerd die zijn gekoppeld aan de verschillende herstelstatusopties van de serviceartikelen in de order.</span><span class="sxs-lookup"><span data-stu-id="26201-146">When a repair status of a service item is changed, the service order status options linked to the different repair status options of all the service items in the order are identified.</span></span> <span data-ttu-id="26201-147">Als de serviceartikelen zijn gekoppeld aan twee of meer opties voor serviceorderstatus, wordt de serviceorderstatusoptie met de hoogste prioriteit geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="26201-147">If the service items are linked to two or more service order status options, the service order status option with the highest priority is selected.</span></span>  

<span data-ttu-id="26201-148">U moet bepalen welke serviceorderstatus de belangrijkste gegevens over de status van de serviceorder bevat en aan deze status de hoogste prioriteit toewijzen, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="26201-148">You must decide which service order status contains the most important information about the status of the service order and assign that status the highest priority, and so on.</span></span>  

<span data-ttu-id="26201-149">Als u vervolgens een nieuwe serviceorder maakt en er serviceartikelen aan toevoegt, wordt het veld **Prioriteit** in de serviceorderkop bijgewerkt op basis van de prioriteiten van de serviceartikelen.</span><span class="sxs-lookup"><span data-stu-id="26201-149">Then, when you create a new service order and you add service items to it, the **Priority** field on the service order header is updated based on the priorities on the service items.</span></span>  

### <a name="example"></a><span data-ttu-id="26201-150">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="26201-150">Example</span></span>

<span data-ttu-id="26201-151">Hier volgt een typisch voorbeeld van een toewijzing van prioriteitsniveau:</span><span class="sxs-lookup"><span data-stu-id="26201-151">A typical priority level assignment could be as follows:</span></span>  

* <span data-ttu-id="26201-152">In verwerking: Hoog</span><span class="sxs-lookup"><span data-stu-id="26201-152">In Process - High</span></span>  
* <span data-ttu-id="26201-153">In behandeling: Relatief hoog</span><span class="sxs-lookup"><span data-stu-id="26201-153">Pending - Medium high</span></span>  
* <span data-ttu-id="26201-154">Afwachten: Relatief laag</span><span class="sxs-lookup"><span data-stu-id="26201-154">On Hold - Medium low</span></span>  
* <span data-ttu-id="26201-155">Gereedgemeld: Laag</span><span class="sxs-lookup"><span data-stu-id="26201-155">Finished - Low</span></span>  

<span data-ttu-id="26201-156">Als één serviceartikel bijvoorbeeld de herstelstatus **Eerste** heeft, gekoppeld aan de serviceorderstatus **In behandeling**, een ander serviceartikel de herstelstatus **In verwerking** heeft, gekoppeld aan de serviceorderstatus **In verwerking**, en een derde serviceartikel de herstelstatus **Reserveonderdeel besteld**, gekoppeld aan de serviceorderstatus **Afwachten**, dan is de uiteindelijke serviceorderstatus **In verwerking**, omdat deze de hoogste prioriteit heeft.</span><span class="sxs-lookup"><span data-stu-id="26201-156">For example, if one service item has the repair status **Initial**, linked to the service order status **Pending**, another has the repair status **In Process**, linked to the service order status **In Process**, and a third has the repair status **Spare Part Ordered**, linked to the service order status **On Hold**, the resulting service order status will be **In Process** because this has the highest priority.</span></span>  

## <a name="see-also"></a><span data-ttu-id="26201-157">Zie ook</span><span class="sxs-lookup"><span data-stu-id="26201-157">See Also</span></span>

[<span data-ttu-id="26201-158">Statussen instellen voor serviceorders en reparaties</span><span class="sxs-lookup"><span data-stu-id="26201-158">Set Up Statuses for Service Orders and Repairs</span></span>](service-order-repair-status.md)  
[<span data-ttu-id="26201-159">CRM - Service instellen</span><span class="sxs-lookup"><span data-stu-id="26201-159">Setting Up Service Management</span></span>](service-setup-service.md)  
