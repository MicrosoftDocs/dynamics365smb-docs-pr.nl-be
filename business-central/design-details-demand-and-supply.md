---
title: 'Ontwerpdetails: Vraag en aanbod | Microsoft Docs'
description: Vraag is de verzamelterm voor elk soort brutovraag, zoals een verkooporder en materiaalbehoefte van een productieorder. Bovendien staat de toepassing meer technische soorten vraag toe, zoals negatieve voorraad en inkoopretouren
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: 8ef7211aa812b1faf784ecf36f1873a6e2dcc6fc
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303648"
---
# <a name="design-details-demand-and-supply"></a><span data-ttu-id="62637-104">Ontwerpdetails: Vraag en aanbod</span><span class="sxs-lookup"><span data-stu-id="62637-104">Design Details: Demand and Supply</span></span>
<span data-ttu-id="62637-105">Vraag is de verzamelterm voor elk soort brutovraag, zoals een verkooporder en materiaalbehoefte van een productieorder.</span><span class="sxs-lookup"><span data-stu-id="62637-105">Demand is the common term used for any kind of gross demand, such as a sales order and component need from a production order.</span></span> <span data-ttu-id="62637-106">Bovendien staat de toepassing meer technische soorten vraag toe, zoals negatieve voorraad en inkoopretouren</span><span class="sxs-lookup"><span data-stu-id="62637-106">In addition, application allows more technical types of demand, such as negative inventory and purchase returns.</span></span>  

 <span data-ttu-id="62637-107">Voorziening is de algemene term voor elke soort positief of inkomend aantal, zoals voorraad, inkopen, assemblage, productie of inkomende transfers.</span><span class="sxs-lookup"><span data-stu-id="62637-107">Supply is the common term used for any kind of positive or inbound quantity, such as inventory, purchases, assembly, production, or inbound transfers.</span></span> <span data-ttu-id="62637-108">Een verkoopretour kan bovendien ook voorziening vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="62637-108">In addition, a sales return may also represent supply.</span></span>  

 <span data-ttu-id="62637-109">Om de vele bronnen van vraag en voorzieningen te sorteren, ordent het planningssysteem deze op twee tijdpaden die voorraadprofielen worden genoemd.</span><span class="sxs-lookup"><span data-stu-id="62637-109">To sort out the many sources of demand and supply, the planning system organizes them on two time lines called inventory profiles.</span></span> <span data-ttu-id="62637-110">Eén profiel bevat vraaggebeurtenissen en het andere bevat de corresponderende voorzieninggebeurtenissen.</span><span class="sxs-lookup"><span data-stu-id="62637-110">One profile holds demand events, and the other holds the corresponding supply events.</span></span> <span data-ttu-id="62637-111">Elke gebeurtenis vertegenwoordigt een entiteit uit het ordernetwerk, bijvoorbeeld een verkooporderregel, een artikelpost of een productieorderregel.</span><span class="sxs-lookup"><span data-stu-id="62637-111">Each event represents one order network entity, such as a sales order line, an item ledger entry, or a production order line.</span></span>  

 <span data-ttu-id="62637-112">Wanneer voorraadprofielen worden geladen, worden de verschillende vraag-voorzieningcombinaties vereffend om een voorzieningenplan uit te voeren dat aan de genoemde doelstellingen voldoet.</span><span class="sxs-lookup"><span data-stu-id="62637-112">When inventory profiles are loaded, the different demand-supply sets are balanced to output a supply plan that fulfills the listed goals.</span></span>  

 <span data-ttu-id="62637-113">Planningsparameters en voorraadniveaus zijn respectievelijk andere soorten vraag en aanbod, die geïntegreerde afstemming ondergaan om voorraadartikelen aan te vullen.</span><span class="sxs-lookup"><span data-stu-id="62637-113">Planning parameters and inventory levels are other types of demand and supply respectively, which undergo integrated balancing to replenish stock items.</span></span> <span data-ttu-id="62637-114">Zie voor meer informatie [Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md).</span><span class="sxs-lookup"><span data-stu-id="62637-114">For more information, see [Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="62637-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="62637-115">See Also</span></span>  
 <span data-ttu-id="62637-116">[Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="62637-116">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="62637-117">[Ontwerpdetails: Centrale begrippen van het planningssysteem](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="62637-117">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 [<span data-ttu-id="62637-118">Ontwerpdetails: Voorraadplanning</span><span class="sxs-lookup"><span data-stu-id="62637-118">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
