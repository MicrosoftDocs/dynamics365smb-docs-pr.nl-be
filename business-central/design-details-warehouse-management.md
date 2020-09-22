---
title: 'Ontwerpdetails: Magazijnbeheer | Microsoft Docs'
description: Dit onderwerp bevat een overzicht van het ontwerp, de concepten en principes achter de magazijnbeheerfuncties in Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 25e492318d7581780fd9fe9038531e1ba1c24282
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787196"
---
# <a name="design-details-warehouse-management"></a><span data-ttu-id="4f49b-103">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="4f49b-103">Design Details: Warehouse Management</span></span>
<span data-ttu-id="4f49b-104">Deze documentatie bevat een overzicht van de concepten en principes die worden gehanteerd in de magazijnbeheerfuncties in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4f49b-104">This documentation gives an overview of the concepts and principles that are used in the Warehouse Management features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="4f49b-105">Er wordt uitgelegd wat het ontwerp is achter centrale magazijnfuncties en hoe deze functies worden geïntegreerd met andere leveringsketenfuncties.</span><span class="sxs-lookup"><span data-stu-id="4f49b-105">It explains the design behind central warehouse features and how warehousing integrates with other supply chain features.</span></span>  

<span data-ttu-id="4f49b-106">Om onderscheid te kunnen maken tussen de verschillende complexiteitsniveaus van magazijnfuncties, wordt deze documentatie verdeeld in twee algemene groepen, standaard- en geavanceerde magazijnconfiguraties, aangeduid met sectietitels.</span><span class="sxs-lookup"><span data-stu-id="4f49b-106">To differentiate the different complexity levels of the warehousing, this documentation is divided into two general groups, Basic and Advanced warehouse configurations, indicated by section titles.</span></span> <span data-ttu-id="4f49b-107">Dit eenvoudig onderscheid omvat verschillende complexiteitniveaus zoals gedefinieerd door productgranules en vestigingsinstellingen.</span><span class="sxs-lookup"><span data-stu-id="4f49b-107">This simple differentiation covers different complexity levels as defined by product granules and location setup.</span></span> <span data-ttu-id="4f49b-108">Zie voor meer informatie [Ontwerpdetails: Magazijninstelling](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="4f49b-108">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="4f49b-109">In dit gedeelte</span><span class="sxs-lookup"><span data-stu-id="4f49b-109">In This Section</span></span>  
[<span data-ttu-id="4f49b-110">Ontwerpdetails: Magazijnoverzicht</span><span class="sxs-lookup"><span data-stu-id="4f49b-110">Design Details: Warehouse Overview</span></span>](design-details-warehouse-overview.md)  
[<span data-ttu-id="4f49b-111">Ontwerpdetails: Magazijninstelling</span><span class="sxs-lookup"><span data-stu-id="4f49b-111">Design Details: Warehouse Setup</span></span>](design-details-warehouse-setup.md)  
[<span data-ttu-id="4f49b-112">Ontwerpdetails: Inkomende magazijnstroom</span><span class="sxs-lookup"><span data-stu-id="4f49b-112">Design Details: Inbound Warehouse Flow</span></span>](design-details-inbound-warehouse-flow.md)  
[<span data-ttu-id="4f49b-113">Ontwerpdetails: Inkomende magazijnstromen</span><span class="sxs-lookup"><span data-stu-id="4f49b-113">Design Details: Internal Warehouse Flows</span></span>](design-details-internal-warehouse-flows.md)  
[<span data-ttu-id="4f49b-114">Ontwerpdetails: Beschikbaarheid in het magazijn</span><span class="sxs-lookup"><span data-stu-id="4f49b-114">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="4f49b-115">Ontwerpdetails: Uitgaande magazijnstroom</span><span class="sxs-lookup"><span data-stu-id="4f49b-115">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="4f49b-116">Ontwerpdetails: Integratie met voorraad</span><span class="sxs-lookup"><span data-stu-id="4f49b-116">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)
