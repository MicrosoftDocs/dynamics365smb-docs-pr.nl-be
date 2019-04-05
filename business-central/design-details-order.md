---
title: 'Ontwerpdetails: Order | Microsoft Docs'
description: In dit onderwerp vindt u informatie over order-naar-order-koppelingen in een omgeving waarin op order wordt geproduceerd.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, order
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 4152dfb744215034383239ea98847fbf7b5751e9
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816461"
---
# <a name="design-details-order"></a><span data-ttu-id="79758-103">Ontwerpdetails: Order</span><span class="sxs-lookup"><span data-stu-id="79758-103">Design Details: Order</span></span>
<span data-ttu-id="79758-104">In een op-order-produceren omgeving wordt een artikel ingekocht of geproduceerd om uitsluitend aan een specifieke vraag te voldoen.</span><span class="sxs-lookup"><span data-stu-id="79758-104">In a make-to-order environment, an item is purchased or produced to exclusively cover a specific demand.</span></span> <span data-ttu-id="79758-105">Meestal heeft dit betrekking op A-producten en de motivatie om het bestelbeleid Order te kiezen, kan zijn dat de vraag niet frequent is, dat de doorlooptijd onbeduidend is of dat de vereiste kenmerken verschillen.</span><span class="sxs-lookup"><span data-stu-id="79758-105">Typically it relates to A-items, and the motivation for choosing the order reordering policy can be that the demand is infrequent, the lead-time is insignificant, or the required attributes vary.</span></span>  

<span data-ttu-id="79758-106">Het programma maakt een order-naar-order-koppeling die fungeert als voorlopige verbinding tussen de voorziening, een voorzieningenorder of voorraad, en de vraag waaraan het zal voldoen.</span><span class="sxs-lookup"><span data-stu-id="79758-106">The program creates an order-to-order link, which acts as a preliminary connection between the supply, a supply order or inventory, and the demand that it is going to fulfill.</span></span>  

<span data-ttu-id="79758-107">Afgezien van het gebruik van het bestelbeleid kan de order-aan-order koppeling tijdens planning op de volgende manieren worden toegepast:</span><span class="sxs-lookup"><span data-stu-id="79758-107">Apart from using the Order policy, the order-to-order link can be applied during planning in the following ways:</span></span>  

* <span data-ttu-id="79758-108">Wanneer het productiebeleid Op order produceren wordt gebruikt om productieorders met meerdere niveaus of projecttype te maken (waarbij benodigde onderdelen op dezelfde productieorder worden geproduceerd).</span><span class="sxs-lookup"><span data-stu-id="79758-108">When using the Make-to-Order manufacturing policy to create multi-level or project type production orders (producing needed components on the same production order).</span></span>  
* <span data-ttu-id="79758-109">Wanneer de functie Verkooporderplanning wordt gebruikt om een productieorder te maken van een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="79758-109">When using the Sales Order Planning feature to create a production order from a sales order.</span></span>  

<span data-ttu-id="79758-110">Zelfs als een productiebedrijf zichzelf beschouwt als een op-order-produceren omgeving, kan het het best zijn een lot-voor-lot bestelbeleid te gebruiken als de artikelen standaard zijn, zonder variatie in kenmerken.</span><span class="sxs-lookup"><span data-stu-id="79758-110">Even if a manufacturing company considers itself as a make-to-order environment, it might be best to use a Lot-for-Lot reordering policy if the items are pure standard without variation in attributes.</span></span> <span data-ttu-id="79758-111">Hierdoor gebruikt het systeem niet-geplande voorraad en worden verkooporders alleen gecumuleerd met dezelfde verzenddatum of binnen een bepaalde periode.</span><span class="sxs-lookup"><span data-stu-id="79758-111">As a result, the system will use unplanned inventory and only accumulates sales orders with the same shipment date or within a defined time bucket.</span></span>  

## <a name="order-to-order-links-and-past-due-dates"></a><span data-ttu-id="79758-112">Order-naar-order koppelingen en overschreden vervaldatums</span><span class="sxs-lookup"><span data-stu-id="79758-112">Order-to-Order Links and Past Due Dates</span></span>  
<span data-ttu-id="79758-113">In tegenstelling tot de meeste combinaties van voorziening en vraag, worden gekoppelde orders met vervaldatums voor de begindatum van de planning, volledig door het systeem gepland.</span><span class="sxs-lookup"><span data-stu-id="79758-113">Unlike most supply-demand sets, linked orders with due dates before the planning starting date are fully planned for by the system.</span></span> <span data-ttu-id="79758-114">De bedrijfsreden voor deze uitzondering is dat specifieke vraag-voorzieningcombinaties moeten worden gesynchroniseerd tot aan uitvoering.</span><span class="sxs-lookup"><span data-stu-id="79758-114">The business reason for this exception is that specific demand-supply sets must be synchronized through to execution.</span></span> <span data-ttu-id="79758-115">Zie voor meer informatie over de bevroren zone die de meeste vraag/voorziening toepast [Ontwerpdetails: Werken met orders voor de geplande begindatum](design-details-dealing-with-orders-before-the-planning-starting-date.md).</span><span class="sxs-lookup"><span data-stu-id="79758-115">For more information about the frozen zone that applies to most demand-supply types, see [Design Details: Dealing with Orders Before the Planning Starting Date](design-details-dealing-with-orders-before-the-planning-starting-date.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="79758-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="79758-116">See Also</span></span>  
<span data-ttu-id="79758-117">[Ontwerpdetails: Bestelbeleid](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="79758-117">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="79758-118">[Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="79758-118">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="79758-119">[Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="79758-119">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="79758-120">Ontwerpdetails: Voorraadplanning</span><span class="sxs-lookup"><span data-stu-id="79758-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
