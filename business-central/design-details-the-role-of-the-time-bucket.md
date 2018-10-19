---
title: 'Ontwerpdetails: De rol van het tijdsinterval | Microsoft Docs'
description: Het doel van het tijdsinterval is vraaggebeurtenissen binnen het tijdvenster te verzamelen om een gezamenlijke voorzieningenorder te maken.
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
ms.openlocfilehash: c258c13a08e9556caddf55a0d14962ad85cd8ca7
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-the-role-of-the-time-bucket"></a><span data-ttu-id="fd655-103">Ontwerpdetails: De rol van het tijdsinterval</span><span class="sxs-lookup"><span data-stu-id="fd655-103">Design Details: The Role of the Time Bucket</span></span>
<span data-ttu-id="fd655-104">Het doel van het tijdsinterval is vraaggebeurtenissen binnen het tijdvenster te verzamelen om een gezamenlijke voorzieningenorder te maken.</span><span class="sxs-lookup"><span data-stu-id="fd655-104">The purpose of the time bucket is to collect demand events within the time window in order to make a joint supply order.</span></span>  

 <span data-ttu-id="fd655-105">Voor bestelbeleid dat een bestelpunt gebruikt, kunt u een tijdsinterval opgeven.</span><span class="sxs-lookup"><span data-stu-id="fd655-105">For reordering policies that use a reorder point, you can define a time bucket.</span></span> <span data-ttu-id="fd655-106">Dit zorgt ervoor dat de vraag in dezelfde periode wordt opgeteld voordat wordt gecontroleerd wat het effect op de geplande voorraad is en of het bestelpunt is verstreken.</span><span class="sxs-lookup"><span data-stu-id="fd655-106">This ensures that demand within the same time period is accumulated before checking the impact on the projected inventory and whether the reorder point has been passed.</span></span> <span data-ttu-id="fd655-107">Als het bestelpunt is overschreden, wordt een nieuwe voorzieningenorder voorwaarts gepland vanaf het einde van de periode die wordt gedefinieerd door het tijdsinterval.</span><span class="sxs-lookup"><span data-stu-id="fd655-107">If the reorder point is passed, a new supply order is scheduled forward from the end of the period defined by the time bucket.</span></span> <span data-ttu-id="fd655-108">De tijdsintervallen beginnen op de begindatum van de planning.</span><span class="sxs-lookup"><span data-stu-id="fd655-108">The time buckets begin on the planning starting date.</span></span>  

 <span data-ttu-id="fd655-109">Het tijdsinterval geeft het handmatige proces aan om het voorraadniveau op frequente basis te controleren in plaats van voor elke transactie.</span><span class="sxs-lookup"><span data-stu-id="fd655-109">The time-bucketed concept reflects the manual process of checking the inventory level on a frequent basis rather than for each transaction.</span></span> <span data-ttu-id="fd655-110">De gebruiker moet de frequentie (het tijdsinterval) definiëren.</span><span class="sxs-lookup"><span data-stu-id="fd655-110">The user needs to define the frequency (the time bucket).</span></span> <span data-ttu-id="fd655-111">De gebruiker verzamelt bijvoorbeeld alle artikelbehoeften van één leverancier om een wekelijkse order te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="fd655-111">For example, the user gathers all item needs from one vendor to place a weekly order.</span></span>  

 <span data-ttu-id="fd655-112">![Voorbeeld van tijdverzameling bij planning](media/nav_app_supply_planning_2_reorder_cycle.png "Voorbeeld van tijdverzameling bij planning")</span><span class="sxs-lookup"><span data-stu-id="fd655-112">![Example of time bucket in planning](media/nav_app_supply_planning_2_reorder_cycle.png "Example of time bucket in planning")</span></span>  

 <span data-ttu-id="fd655-113">Het tijdsinterval wordt doorgaans gebruikt om een watervaleffect te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="fd655-113">The time bucket is generally used to avoid a cascade effect.</span></span> <span data-ttu-id="fd655-114">Een vereffende rij van vraag en aanbod waarbij bijvoorbeeld een vroege vraag wordt geannuleerd of een nieuwe wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fd655-114">For example, a balanced row of demand and supply where an early demand is canceled, or a new one is created.</span></span> <span data-ttu-id="fd655-115">Het resultaat is dat elke voorzieningenorder (behalve de laatste) opnieuw wordt gepland.</span><span class="sxs-lookup"><span data-stu-id="fd655-115">The result would be that every supply order (except the last one) is rescheduled.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fd655-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="fd655-116">See Also</span></span>  
 <span data-ttu-id="fd655-117">[Ontwerpdetails: Bestelbeleid](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="fd655-117">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="fd655-118">[Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="fd655-118">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="fd655-119">[Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="fd655-119">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="fd655-120">Ontwerpdetails: Voorraadplanning</span><span class="sxs-lookup"><span data-stu-id="fd655-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

