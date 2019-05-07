---
title: 'Ontwerpdetails: Verwachte negatieve voorraad verwerken | Microsoft Docs'
description: Het bestelpunt drukt de verwachte vraag uit tijdens de doorlooptijd van het artikel. Wanneer het bestelpunt is verstreken, is het tijd om meer te bestellen. Maar de geplande voorraad moet groot genoeg zijn om de vraag te dekken totdat de nieuwe order wordt ontvangen. In de tussentijd moet de veiligheidsvoorraad zorgen voor schommelingen in de vraag tot aan een bepaald serviceniveau.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: a0ecfe62e70c434ecfd6d698424e20119be13554
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "918875"
---
# <a name="design-details-handling-projected-negative-inventory"></a><span data-ttu-id="e50ba-106">Ontwerpdetails: Verwachte negatieve voorraad verwerken</span><span class="sxs-lookup"><span data-stu-id="e50ba-106">Design Details: Handling Projected Negative Inventory</span></span>
<span data-ttu-id="e50ba-107">Het bestelpunt drukt de verwachte vraag uit tijdens de doorlooptijd van het artikel.</span><span class="sxs-lookup"><span data-stu-id="e50ba-107">The reorder point expresses the anticipated demand during the lead time of the item.</span></span> <span data-ttu-id="e50ba-108">Wanneer het bestelpunt is verstreken, is het tijd om meer te bestellen.</span><span class="sxs-lookup"><span data-stu-id="e50ba-108">When the reorder point is passed, it is time to order more.</span></span> <span data-ttu-id="e50ba-109">Maar de geplande voorraad moet groot genoeg zijn om de vraag te dekken totdat de nieuwe order wordt ontvangen.</span><span class="sxs-lookup"><span data-stu-id="e50ba-109">But the projected inventory must be large enough to cover the demand until the new order is received.</span></span> <span data-ttu-id="e50ba-110">In de tussentijd moet de veiligheidsvoorraad zorgen voor schommelingen in de vraag tot aan een bepaald serviceniveau.</span><span class="sxs-lookup"><span data-stu-id="e50ba-110">Meanwhile, the safety stock should take care of fluctuations in demand up to a targeted service level.</span></span>  

 <span data-ttu-id="e50ba-111">Dus beschouwt het planningssysteem het als een noodgeval als aan toekomstige vraag niet kan worden voldaan vanuit de voorspelde voorraad, of anders uitgedrukt, als de voorspelde voorraad negatief wordt.</span><span class="sxs-lookup"><span data-stu-id="e50ba-111">Consequently, the planning system considers it an emergency if a future demand cannot be served from the projected inventory, or expressed in another way, that the projected inventory goes negative.</span></span> <span data-ttu-id="e50ba-112">Het systeem verwerkt dergelijke uitzonderingen door een nieuwe voorzieningenorder voor te stellen om te voldoen aan het deel van de vraag waaraan de voorraad of andere voorzieningen niet kunnen voldoen.</span><span class="sxs-lookup"><span data-stu-id="e50ba-112">The system deals with such an exception by suggesting a new supply order to meet the part of the demand that cannot be met by inventory or other supply.</span></span> <span data-ttu-id="e50ba-113">Voor de ordergrootte van de nieuwe voorzieningenorder wordt geen rekening gehouden met de maximale voorraad of het bestelaantal. Dit geldt ook voor de ordervelden Min. bestelaantal, Max. bestelaantal en Vaste lotgrootte.</span><span class="sxs-lookup"><span data-stu-id="e50ba-113">The order size of the new supply order will not take the maximum inventory or the reorder quantity into consideration, nor will it take into consideration the order modifiers Maximum Order Quantity, Minimum Order Quantity, and Order Multiple.</span></span> <span data-ttu-id="e50ba-114">In plaats hiervan is dit het exacte tekort.</span><span class="sxs-lookup"><span data-stu-id="e50ba-114">Instead, it will reflect the exact deficiency.</span></span>  

 <span data-ttu-id="e50ba-115">De planningsregel voor dit soort voorzieningenorder geeft een waarschuwingspictogram Noodgeval weer en er worden extra gegevens getoond bij het opzoeken om de gebruiker te informeren over de situatie.</span><span class="sxs-lookup"><span data-stu-id="e50ba-115">The planning line for this type of supply order will display an Emergency warning icon, and additional information will be provided upon lookup to inform the user of the situation.</span></span>  

 <span data-ttu-id="e50ba-116">In de volgende illustratie staat aanbod D voor een noodorder om een correctie uit te voeren voor negatieve voorraad.</span><span class="sxs-lookup"><span data-stu-id="e50ba-116">In the following illustration, supply D represents an emergency order to adjust for negative inventory.</span></span>  

 <span data-ttu-id="e50ba-117">![Suggestie van noodplanning om negatieve voorraad te voorkomen](media/nav_app_supply_planning_2_negative_inventory.png "Suggestie van noodplanning om negatieve voorraad te voorkomen")</span><span class="sxs-lookup"><span data-stu-id="e50ba-117">![Emergency planning suggestion to avoid negative inventory](media/nav_app_supply_planning_2_negative_inventory.png "Emergency planning suggestion to avoid negative inventory")</span></span>  

1.  <span data-ttu-id="e50ba-118">Voorziening **A**, de oorspronkelijk geplande voorraad, is onder het bestelpunt.</span><span class="sxs-lookup"><span data-stu-id="e50ba-118">Supply **A**, initial projected inventory, is below reorder point.</span></span>  
2.  <span data-ttu-id="e50ba-119">Er is een nieuwe voorwaarts-geplande voorziening gemaakt (**C**).</span><span class="sxs-lookup"><span data-stu-id="e50ba-119">A new forward-scheduled supply is created (**C**).</span></span>  

     <span data-ttu-id="e50ba-120">(Aantal = Maximale voorraad – Gepland voorraadniveau)</span><span class="sxs-lookup"><span data-stu-id="e50ba-120">(Quantity = Maximum Inventory – Projected Inventory Level)</span></span>  
3.  <span data-ttu-id="e50ba-121">Voorziening **A** wordt afgesloten door vraag **B**, die niet volledig is verwerkt.</span><span class="sxs-lookup"><span data-stu-id="e50ba-121">Supply **A** is closed by demand **B**, which is not fully covered.</span></span>  

     <span data-ttu-id="e50ba-122">(Vraag **B** zou kunnen proberen Aanbod C in te plannen, maar dat gebeurt niet op basis van het tijdsintervalconcept.)</span><span class="sxs-lookup"><span data-stu-id="e50ba-122">(Demand **B** could try to schedule Supply C in but that will not happen according to the time-bucket concept.)</span></span>  
4.  <span data-ttu-id="e50ba-123">Er wordt nieuw aanbod (**D**) gemaakt om te voldoen aan het resterende aantal van de vraag **B**.</span><span class="sxs-lookup"><span data-stu-id="e50ba-123">New supply (**D**) is created to cover the remaining quantity on Demand **B**.</span></span>  
5.  <span data-ttu-id="e50ba-124">Vraag **B** wordt gesloten (waarbij een aanmaning voor de geplande voorraad wordt gemaakt).</span><span class="sxs-lookup"><span data-stu-id="e50ba-124">Demand **B** is closed (creating a reminder to the projected inventory).</span></span>  
6.  <span data-ttu-id="e50ba-125">De nieuwe voorziening **D** is afgesloten.</span><span class="sxs-lookup"><span data-stu-id="e50ba-125">The new supply **D** is closed.</span></span>  
7.  <span data-ttu-id="e50ba-126">Geplande voorraad wordt gecontroleerd; bestelpunt is niet overschreden.</span><span class="sxs-lookup"><span data-stu-id="e50ba-126">Projected Inventory is checked; reorder point has not been crossed.</span></span>  
8.  <span data-ttu-id="e50ba-127">Voorziening **C** is afgesloten (er bestaat geen vraag meer).</span><span class="sxs-lookup"><span data-stu-id="e50ba-127">Supply **C** is closed (no more demand exists).</span></span>  
9. <span data-ttu-id="e50ba-128">Laatste controle: Er bestaan geen openstaande voorraadniveauaanmaningen.</span><span class="sxs-lookup"><span data-stu-id="e50ba-128">Final check: No outstanding inventory level reminders exist.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="e50ba-129">Stap 4 geeft aan hoe het systeem in eerdere versies dan Microsoft Dynamics NAV 2009 SP1 reageert.</span><span class="sxs-lookup"><span data-stu-id="e50ba-129">Step 4 reflects how the system reacts in versions earlier than Microsoft Dynamics NAV 2009 SP1.</span></span>  

 <span data-ttu-id="e50ba-130">Hiermee wordt de omschrijving afgerond van centrale principes met betrekking tot voorraadplanning op basis van bestelbeleid.</span><span class="sxs-lookup"><span data-stu-id="e50ba-130">This concludes the description of central principles relating to inventory planning based on reordering policies.</span></span> <span data-ttu-id="e50ba-131">In het volgende gedeelte worden de kenmerken van de vier ondersteunde soorten bestelbeleid beschreven.</span><span class="sxs-lookup"><span data-stu-id="e50ba-131">The following section describes the characteristics of the four supported reordering policies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e50ba-132">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e50ba-132">See Also</span></span>  
 <span data-ttu-id="e50ba-133">[Ontwerpdetails: Bestelbeleid](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="e50ba-133">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
 <span data-ttu-id="e50ba-134">[Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="e50ba-134">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
 <span data-ttu-id="e50ba-135">[Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="e50ba-135">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
 [<span data-ttu-id="e50ba-136">Ontwerpdetails: Voorraadplanning</span><span class="sxs-lookup"><span data-stu-id="e50ba-136">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
