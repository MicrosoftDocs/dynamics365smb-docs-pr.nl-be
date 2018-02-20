---
title: Codes voor standaardservices instellen | Microsoft Docs
description: Leer hoe u codes instelt voor serviceactiviteiten die u vaak uitvoert.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2d617fa06ea18d6e74f473600020f14d8f286d98
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---

# <a name="set-up-standard-service-codes"></a><span data-ttu-id="6ee78-103">Standaardservicecodes instellen</span><span class="sxs-lookup"><span data-stu-id="6ee78-103">Set Up Standard Service Codes</span></span>
<span data-ttu-id="6ee78-104">Bij het uitvoeren van de services moeten vaak servicedocumenten worden opgesteld waarbij de serviceregels vergelijkbare informatie bevatten.</span><span class="sxs-lookup"><span data-stu-id="6ee78-104">When you perform typical service, you often have to create service documents that use service lines that contain similar information.</span></span> <span data-ttu-id="6ee78-105">Om het gemakkelijk te maken om deze regels te maken, kunt u standaardservicecodes met een vooraf gedefinieerde reeks serviceregels instellen.</span><span class="sxs-lookup"><span data-stu-id="6ee78-105">To make it easy to create these lines, you can set up standard service codes that have a predefined set of service lines.</span></span> <span data-ttu-id="6ee78-106">Wanneer u de code voor een servicedocument kiest, worden de regels automatisch ingevuld.</span><span class="sxs-lookup"><span data-stu-id="6ee78-106">When you choose the code on a service document, the lines are entered automatically.</span></span> <span data-ttu-id="6ee78-107">U kunt elk gewenst aantal standaardservicecodes instellen en aan elke code kan een onbeperkt aantal serviceregels van verschillende soorten, inclusief artikel, resource, kosten of standaardtekst, worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="6ee78-107">You can set up any number of standard service codes, and each code can have an unlimited number of service lines of different types, including item, resource, cost, or standrd text linked to it.</span></span> <span data-ttu-id="6ee78-108">U kunt serviceregels van elke standaardservicecode maken op de kaart **Standaardservicecode**.</span><span class="sxs-lookup"><span data-stu-id="6ee78-108">You create service lines of each standard serice code on the **Standard Service Code** card.</span></span> <span data-ttu-id="6ee78-109">Vervolgens kunt u standaardservicecodes toewijzen aan serviceartikelgroepen op de pagina **Std. serviceartikelgroepcodes**.</span><span class="sxs-lookup"><span data-stu-id="6ee78-109">You then assign standard service codes to service item groups on the **Standard Serv. Item Gr. Codes** page.</span></span> <span data-ttu-id="6ee78-110">Later, wanneer u een servicedocument opstelt, kunt u de actie **Standaardservicecodes ophalen** gebruiken om serviceregels toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="6ee78-110">Later, when you create a service document, you can use the **Get Standard Service Codes** action to add service lines.</span></span>  
  
> [!Tip]
>  <span data-ttu-id="6ee78-111">U kunt hetzelfde concept gebruiken om regels in verkoop- en inkoopdocumenten te maken.</span><span class="sxs-lookup"><span data-stu-id="6ee78-111">You can use the same concept to create lines on sales and purchase documents.</span></span> <span data-ttu-id="6ee78-112">Zie voor meer informatie [Periodieke verkoop- en inkoopregels maken](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="6ee78-112">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>    
  
## <a name="to-set-up-a-standard-service-code"></a><span data-ttu-id="6ee78-113">Standaardservicecodes instellen</span><span class="sxs-lookup"><span data-stu-id="6ee78-113">To set up a standard service code</span></span>    
1. <span data-ttu-id="6ee78-114">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Standaardservicecodes** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="6ee78-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Standard Service Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6ee78-115">Vul de velden in.</span><span class="sxs-lookup"><span data-stu-id="6ee78-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="6ee78-116">Vul de serviceregels in die zijn gekoppeld aan deze servicecode.</span><span class="sxs-lookup"><span data-stu-id="6ee78-116">Fill in the service lines linked to this service code.</span></span>  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a><span data-ttu-id="6ee78-117">Een standaardservicecode toewijzen aan een serviceartikelgroep</span><span class="sxs-lookup"><span data-stu-id="6ee78-117">To assign a standard service code to a service item group</span></span>
1. <span data-ttu-id="6ee78-118">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Serviceartikelgroepen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="6ee78-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6ee78-119">Vul de velden in.</span><span class="sxs-lookup"><span data-stu-id="6ee78-119">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="6ee78-120">Vul de serviceregels in die zijn gekoppeld aan deze servicecode.</span><span class="sxs-lookup"><span data-stu-id="6ee78-120">Fill in the service lines linked to this service code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6ee78-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6ee78-121">See Also</span></span>
[<span data-ttu-id="6ee78-122">CRM - Service</span><span class="sxs-lookup"><span data-stu-id="6ee78-122">Service Management</span></span>](service-service.md)
