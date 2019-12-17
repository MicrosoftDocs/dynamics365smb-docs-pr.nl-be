---
title: Codes voor standaardservices instellen | Microsoft Docs
description: Leer hoe u codes instelt voor serviceactiviteiten die u vaak uitvoert.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 766af833ddef09b72a520e97d47a32fb7b77fd86
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877435"
---
# <a name="set-up-standard-service-codes"></a><span data-ttu-id="b1a4e-103">Standaardservicecodes instellen</span><span class="sxs-lookup"><span data-stu-id="b1a4e-103">Set Up Standard Service Codes</span></span>
<span data-ttu-id="b1a4e-104">Bij het uitvoeren van de services moeten vaak servicedocumenten worden opgesteld waarbij de serviceregels vergelijkbare informatie bevatten.</span><span class="sxs-lookup"><span data-stu-id="b1a4e-104">When you perform typical service, you often have to create service documents that use service lines that contain similar information.</span></span> <span data-ttu-id="b1a4e-105">Om het gemakkelijk te maken om deze regels te maken, kunt u standaardservicecodes met een vooraf gedefinieerde reeks serviceregels instellen.</span><span class="sxs-lookup"><span data-stu-id="b1a4e-105">To make it easy to create these lines, you can set up standard service codes that have a predefined set of service lines.</span></span> <span data-ttu-id="b1a4e-106">Wanneer u de code voor een servicedocument kiest, worden de regels automatisch ingevuld.</span><span class="sxs-lookup"><span data-stu-id="b1a4e-106">When you choose the code on a service document, the lines are entered automatically.</span></span> <span data-ttu-id="b1a4e-107">U kunt elk gewenst aantal standaardservicecodes instellen en aan elke code kan een onbeperkt aantal serviceregels van verschillende soorten, inclusief artikel, resource, kosten of standaardtekst, worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="b1a4e-107">You can set up any number of standard service codes, and each code can have an unlimited number of service lines of different types, including item, resource, cost, or standrd text linked to it.</span></span> <span data-ttu-id="b1a4e-108">U kunt serviceregels van elke standaardservicecode maken op de kaart **Standaardservicecode**.</span><span class="sxs-lookup"><span data-stu-id="b1a4e-108">You create service lines of each standard serice code on the **Standard Service Code** card.</span></span> <span data-ttu-id="b1a4e-109">Vervolgens kunt u standaardservicecodes toewijzen aan serviceartikelgroepen op de pagina **Std. serviceartikelgroepcodes**.</span><span class="sxs-lookup"><span data-stu-id="b1a4e-109">You then assign standard service codes to service item groups on the **Standard Serv. Item Gr. Codes** page.</span></span> <span data-ttu-id="b1a4e-110">Later, wanneer u een servicedocument opstelt, kunt u de actie **Standaardservicecodes ophalen** gebruiken om serviceregels toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b1a4e-110">Later, when you create a service document, you can use the **Get Standard Service Codes** action to add service lines.</span></span>  
  
> [!Tip]
>  <span data-ttu-id="b1a4e-111">U kunt hetzelfde concept gebruiken om regels in verkoop- en inkoopdocumenten te maken.</span><span class="sxs-lookup"><span data-stu-id="b1a4e-111">You can use the same concept to create lines on sales and purchase documents.</span></span> <span data-ttu-id="b1a4e-112">Zie voor meer informatie [Periodieke verkoop- en inkoopregels maken](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="b1a4e-112">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>    
  
## <a name="to-set-up-a-standard-service-code"></a><span data-ttu-id="b1a4e-113">Standaardservicecodes instellen</span><span class="sxs-lookup"><span data-stu-id="b1a4e-113">To set up a standard service code</span></span>    
1. <span data-ttu-id="b1a4e-114">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Standaardservicecodes** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="b1a4e-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Service Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b1a4e-115">Vul de velden in.</span><span class="sxs-lookup"><span data-stu-id="b1a4e-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="b1a4e-116">Vul de serviceregels in die zijn gekoppeld aan deze servicecode.</span><span class="sxs-lookup"><span data-stu-id="b1a4e-116">Fill in the service lines linked to this service code.</span></span>  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a><span data-ttu-id="b1a4e-117">Een standaardservicecode toewijzen aan een serviceartikelgroep</span><span class="sxs-lookup"><span data-stu-id="b1a4e-117">To assign a standard service code to a service item group</span></span>
1. <span data-ttu-id="b1a4e-118">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Serviceartikelgroepen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="b1a4e-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b1a4e-119">Vul de velden in.</span><span class="sxs-lookup"><span data-stu-id="b1a4e-119">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="b1a4e-120">Vul de serviceregels in die zijn gekoppeld aan deze servicecode.</span><span class="sxs-lookup"><span data-stu-id="b1a4e-120">Fill in the service lines linked to this service code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b1a4e-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b1a4e-121">See Also</span></span>
[<span data-ttu-id="b1a4e-122">Servicebeheer</span><span class="sxs-lookup"><span data-stu-id="b1a4e-122">Service Management</span></span>](service-service.md)