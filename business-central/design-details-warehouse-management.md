---
title: 'Ontwerpdetails: Magazijnbeheer | Microsoft Docs'
description: Dit onderwerp bevat een overzicht van het ontwerp, de concepten en principes achter de magazijnbeheerfuncties in Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 87b3717a8f45444bc43da445d359ed6d79b40372
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786449"
---
# <a name="design-details-warehouse-management"></a><span data-ttu-id="7bc4c-103">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="7bc4c-103">Design Details: Warehouse Management</span></span>
<span data-ttu-id="7bc4c-104">Deze documentatie bevat een overzicht van de concepten en principes die worden gehanteerd in de magazijnbeheerfuncties in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="7bc4c-104">This documentation gives an overview of the concepts and principles that are used in the Warehouse Management features in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="7bc4c-105">Er wordt uitgelegd wat het ontwerp is achter centrale magazijnfuncties en hoe deze functies worden geïntegreerd met andere leveringsketenfuncties.</span><span class="sxs-lookup"><span data-stu-id="7bc4c-105">It explains the design behind central warehouse features and how warehousing integrates with other supply chain features.</span></span>  

<span data-ttu-id="7bc4c-106">Om onderscheid te kunnen maken tussen de verschillende complexiteitsniveaus van magazijnfuncties, wordt deze documentatie verdeeld in twee algemene groepen, standaard- en geavanceerde magazijnconfiguraties, aangeduid met sectietitels.</span><span class="sxs-lookup"><span data-stu-id="7bc4c-106">To differentiate the different complexity levels of the warehousing, this documentation is divided into two general groups, Basic and Advanced warehouse configurations, indicated by section titles.</span></span> <span data-ttu-id="7bc4c-107">Dit eenvoudig onderscheid omvat verschillende complexiteitniveaus zoals gedefinieerd door productgranules en vestigingsinstellingen.</span><span class="sxs-lookup"><span data-stu-id="7bc4c-107">This simple differentiation covers different complexity levels as defined by product granules and location setup.</span></span> <span data-ttu-id="7bc4c-108">Zie voor meer informatie [Ontwerpdetails: Magazijninstelling](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="7bc4c-108">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="7bc4c-109">In dit gedeelte</span><span class="sxs-lookup"><span data-stu-id="7bc4c-109">In This Section</span></span>  
[<span data-ttu-id="7bc4c-110">Ontwerpdetails: Magazijnoverzicht</span><span class="sxs-lookup"><span data-stu-id="7bc4c-110">Design Details: Warehouse Overview</span></span>](design-details-warehouse-overview.md)  
[<span data-ttu-id="7bc4c-111">Ontwerpdetails: Magazijninstelling</span><span class="sxs-lookup"><span data-stu-id="7bc4c-111">Design Details: Warehouse Setup</span></span>](design-details-warehouse-setup.md)  
[<span data-ttu-id="7bc4c-112">Ontwerpdetails: Inkomende magazijnstroom</span><span class="sxs-lookup"><span data-stu-id="7bc4c-112">Design Details: Inbound Warehouse Flow</span></span>](design-details-inbound-warehouse-flow.md)  
[<span data-ttu-id="7bc4c-113">Ontwerpdetails: Inkomende magazijnstromen</span><span class="sxs-lookup"><span data-stu-id="7bc4c-113">Design Details: Internal Warehouse Flows</span></span>](design-details-internal-warehouse-flows.md)  
[<span data-ttu-id="7bc4c-114">Ontwerpdetails: Beschikbaarheid in het magazijn</span><span class="sxs-lookup"><span data-stu-id="7bc4c-114">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="7bc4c-115">Ontwerpdetails: Uitgaande magazijnstroom</span><span class="sxs-lookup"><span data-stu-id="7bc4c-115">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="7bc4c-116">Ontwerpdetails: Integratie met voorraad</span><span class="sxs-lookup"><span data-stu-id="7bc4c-116">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]