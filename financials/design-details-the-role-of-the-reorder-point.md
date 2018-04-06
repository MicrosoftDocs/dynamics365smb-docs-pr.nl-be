---
title: 'Ontwerpdetails: De rol van het bestelpunt | Microsoft Docs'
description: In dit onderwerp wordt het belang van het instellen van een bestelpunt aangegeven, zodat u weet wanneer u meer voorraad moet bestellen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5b5e3cec4bc5af8188470ea1d711422c0130677e
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-the-role-of-the-reorder-point"></a><span data-ttu-id="a6abb-103">Ontwerpdetails: De rol van het bestelpunt</span><span class="sxs-lookup"><span data-stu-id="a6abb-103">Design Details: The Role of the Reorder Point</span></span>
<span data-ttu-id="a6abb-104">Naast de algemene afstemming van vraag en aanbod, moet het planningssysteem ook voorraadniveaus voor de betrokken artikelen controleren om rekening te houden met gedefinieerd bestelbeleid.</span><span class="sxs-lookup"><span data-stu-id="a6abb-104">In addition to the general balancing of supply and demand, the planning system must also monitor inventory levels for the affected items to respect the defined reordering policies.</span></span>  
  
<span data-ttu-id="a6abb-105">Een bestelpunt vertegenwoordigt vraag tijdens doorlooptijd.</span><span class="sxs-lookup"><span data-stu-id="a6abb-105">A reorder point represents demand during lead time.</span></span> <span data-ttu-id="a6abb-106">Wanneer de geplande voorraad onder het voorraadniveau komt dat door het bestelpunt is gedefinieerd, is het tijd om het bestelaantal te verhogen.</span><span class="sxs-lookup"><span data-stu-id="a6abb-106">When the projected inventory passes below the inventory level defined by the reorder point, it is time to order more quantity.</span></span> <span data-ttu-id="a6abb-107">Ondertussen wordt verwacht dat de voorraad afneemt en mogelijk nul wordt (of het veiligheidsvoorraadniveau bereikt), totdat de aanvulling plaatsvindt.</span><span class="sxs-lookup"><span data-stu-id="a6abb-107">Meanwhile, the inventory is expected to decrease gradually and possibly reach zero (or the safety stock level), until the replenishment arrives.</span></span>  
  
<span data-ttu-id="a6abb-108">Het planningssysteem zal een voorwaarts geplande voorzieningenorder voorstellen op het moment dat de verwachte voorraad onder het bestelpunt komt.</span><span class="sxs-lookup"><span data-stu-id="a6abb-108">Accordingly, the planning system will suggest a forward-scheduled supply order at the point when the projected inventory passes below the reorder point.</span></span>  
  
<span data-ttu-id="a6abb-109">Het bestelpunt geeft een bepaald voorraadniveau aan.</span><span class="sxs-lookup"><span data-stu-id="a6abb-109">The reorder point reflects a certain inventory level.</span></span> <span data-ttu-id="a6abb-110">Voorraadniveaus kunnen tijdens het tijdsinterval echter aanzienlijk schommelen en daarom moet het planningssysteem constant de geplande beschikbare voorraad controleren.</span><span class="sxs-lookup"><span data-stu-id="a6abb-110">However, inventory levels can move significantly during the time bucket and, therefore, the planning system must constantly monitor the projected available inventory.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a6abb-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a6abb-111">See Also</span></span>  
<span data-ttu-id="a6abb-112">[Ontwerpdetails: Bestelbeleid](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="a6abb-112">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="a6abb-113">[Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="a6abb-113">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="a6abb-114">[Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="a6abb-114">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="a6abb-115">Ontwerpdetails: Voorraadplanning</span><span class="sxs-lookup"><span data-stu-id="a6abb-115">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
