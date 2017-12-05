---
title: 'Ontwerpdetails: Vraag en aanbod afsluiten | Microsoft Docs'
description: Wanneer de vereffeningsprocedures voor voorzieningen zijn uitgevoerd, zijn er drie mogelijke eindsituaties.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: f682e2fdaa5be20ae8e6f3ff6ee2ff4769b48545
ms.contentlocale: nl-be
ms.lasthandoff: 11/10/2017

---
# <a name="design-details-closing-demand-and-supply"></a><span data-ttu-id="b2b3f-103">Ontwerpdetails: Vraag en aanbod afsluiten</span><span class="sxs-lookup"><span data-stu-id="b2b3f-103">Design Details: Closing Demand and Supply</span></span>
<span data-ttu-id="b2b3f-104">Wanneer de vereffeningsprocedures voor voorzieningen zijn uitgevoerd, zijn er drie mogelijke eindsituaties:</span><span class="sxs-lookup"><span data-stu-id="b2b3f-104">When the supply balancing procedures have been performed, there are three possible end situations:</span></span>  

-   <span data-ttu-id="b2b3f-105">Er is voldaan aan het benodigde aantal en de datum van de vraaggebeurtenissen en de planning hiervoor kan worden afgesloten.</span><span class="sxs-lookup"><span data-stu-id="b2b3f-105">The required quantity and date of the demand events have been met and the planning for them can be closed.</span></span> <span data-ttu-id="b2b3f-106">De voorzieningsgebeurtenis is nog open en kan de volgende vraag verwerken, zodat de vereffeningsprocedure overnieuw kan starten met de huidige voorzieningsgebeurtenis en de volgende vraag.</span><span class="sxs-lookup"><span data-stu-id="b2b3f-106">The supply event is still open and may be able to cover the next demand, so the balancing procedure can start over with the current supply event and the next demand.</span></span>  

-   <span data-ttu-id="b2b3f-107">De voorzieningenorder kan niet worden aangepast om alle vraag te verwerken.</span><span class="sxs-lookup"><span data-stu-id="b2b3f-107">The supply order cannot be modified to cover all of the demand.</span></span> <span data-ttu-id="b2b3f-108">De vraaggebeurtenis is nog open, met een niet-gedekt aantal dat mogelijk kan worden gedekt door de volgende voorzieningsgebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="b2b3f-108">The demand event is still open, with some uncovered quantity that may be covered by the next supply event.</span></span> <span data-ttu-id="b2b3f-109">De huidige voorzieningsgebeurtenis wordt dus afgesloten, zodat de vereffeningsprocedure opnieuw kan starten met de huidige vraag en de volgende voorzieningsgebeurtenis.</span><span class="sxs-lookup"><span data-stu-id="b2b3f-109">Thus the current supply event is closed, so the balancing act can start over with the current demand and the next supply event.</span></span>  

-   <span data-ttu-id="b2b3f-110">Alle vraag is gedekt; er is geen verdere vraag (of er is helemaal geen vraag geweest).</span><span class="sxs-lookup"><span data-stu-id="b2b3f-110">All of the demand has been covered; there is no subsequent demand (or there has been no demand at all).</span></span> <span data-ttu-id="b2b3f-111">Als er eventuele surplusvoorziening is, kan deze worden verlaagd (of geannuleerd) en vervolgens gesloten.</span><span class="sxs-lookup"><span data-stu-id="b2b3f-111">If there is any surplus supply, it may be decreased (or canceled) and then closed.</span></span> <span data-ttu-id="b2b3f-112">Het is mogelijk dat er verder in de keten aanvullende voorzieninggebeurtenissen zijn en die moeten ook worden geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="b2b3f-112">It is possible that additional supply events exist further along in the chain, and they should also be canceled.</span></span>  

 <span data-ttu-id="b2b3f-113">Als laatste maakt het planningssysteem een ordertraceringskoppeling tussen de voorziening en de vraag.</span><span class="sxs-lookup"><span data-stu-id="b2b3f-113">Last, the planning system will create an order tracking link between the supply and the demand.</span></span>  

## <a name="creating-the-planning-line-suggested-action"></a><span data-ttu-id="b2b3f-114">De planningsregel (voorgestelde actie) maken</span><span class="sxs-lookup"><span data-stu-id="b2b3f-114">Creating the Planning Line (Suggested Action)</span></span>  
 <span data-ttu-id="b2b3f-115">Als een actie - Nieuw, Aantal wijzigen, Herplannen, Herplannen en aantal wijzigen of Annuleren- wordt voorgesteld om de voorzieningenorder te herzien, maakt het planningssysteem een planningsregel in het planningsvoorstel.</span><span class="sxs-lookup"><span data-stu-id="b2b3f-115">If any action – New, Change Quantity, Reschedule, Reschedule and Change Quantity, or Cancel – is suggested to revise the supply order, the planning system creates a planning line in the planning worksheet.</span></span> <span data-ttu-id="b2b3f-116">Vanwege ordertracering wordt de planningsregel niet alleen gemaakt wanneer de voorzieningsgebeurtenis wordt afgesloten, maar ook als de vraaggebeurtenis wordt afgesloten, zelfs als de voorzieningsgebeurtenis nog openstaat en nog kan veranderen als de volgende vraaggebeurtenis wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="b2b3f-116">Due to order tracking, the planning line is created not only when the supply event is closed, but also if the demand event is closed, even though the supply event is still open and may be subject to additional changes when the next demand event is processed.</span></span> <span data-ttu-id="b2b3f-117">Dit betekent dat nadat de planningsregel is gemaakt, deze weer kan worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="b2b3f-117">This means that when first created, the planning line may be changed again.</span></span>  

 <span data-ttu-id="b2b3f-118">Om databasetoegang te beperken bij het verwerken van productieorders, kan de planningsregel worden onderhouden op drie niveaus terwijl wordt geprobeerd het minst veeleisende onderhoudsniveau uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="b2b3f-118">To minimize database access when handling production orders, the planning line can be maintained in three levels, while aiming to perform the least demanding maintenance level:</span></span>  

-   <span data-ttu-id="b2b3f-119">Maak alleen de planningsregel met de huidige vervaldatum en aantal maar zonder het bewerkingsplan en materialen.</span><span class="sxs-lookup"><span data-stu-id="b2b3f-119">Create only the planning line with the current due date and quantity but without the routing and components.</span></span>  

-   <span data-ttu-id="b2b3f-120">Bewerkingsplan opnemen: het geplande bewerkingsplan wordt opgesteld inclusief de berekening van begin- en einddatums en -tijden.</span><span class="sxs-lookup"><span data-stu-id="b2b3f-120">Include routing: the planned routing is laid out including calculation of starting and ending dates and times.</span></span> <span data-ttu-id="b2b3f-121">Dit is vereist voor wat betreft de databasetoegang.</span><span class="sxs-lookup"><span data-stu-id="b2b3f-121">This is demanding in terms of database accesses.</span></span> <span data-ttu-id="b2b3f-122">Voor het bepalen van de eind- en vervaldatums kan het noodzakelijk zijn om dit te berekenen, zelfs als de voorzieningsgebeurtenis niet is afgesloten (in het geval van voorwaartse planning).</span><span class="sxs-lookup"><span data-stu-id="b2b3f-122">To determine the ending and due dates, it may be necessary to calculate this even if the supply event has not been closed (in the case of forward scheduling).</span></span>  

-   <span data-ttu-id="b2b3f-123">Ontwikkeling stuklijst opnemen: dit kan wachten tot vlak voordat de voorzieningsgebeurtenis wordt gesloten.</span><span class="sxs-lookup"><span data-stu-id="b2b3f-123">Include BOM explosion: this can wait until just before the supply event is closed.</span></span>  

 <span data-ttu-id="b2b3f-124">Hiermee worden de omschrijvingen afgerond van hoe vraag en voorzieningen worden geladen, prioriteit krijgen en worden vereffend door het planningssysteem.</span><span class="sxs-lookup"><span data-stu-id="b2b3f-124">This concludes the descriptions of how demand and supply is loaded, prioritized, and balanced by the planning system.</span></span> <span data-ttu-id="b2b3f-125">Bij integratie met deze voorraadplanningactiviteit moet het systeem ervoor zorgen dat het vereiste voorraadniveau van elk gepland artikel wordt onderhouden op basis van het bestelbeleid.</span><span class="sxs-lookup"><span data-stu-id="b2b3f-125">In integration with this supply planning activity, the system must ensure that the required inventory level of each planned item is maintained according to its reordering policies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b2b3f-126">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b2b3f-126">See Also</span></span>  
 <span data-ttu-id="b2b3f-127">[Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="b2b3f-127">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
 <span data-ttu-id="b2b3f-128">[Ontwerpdetails: Centrale begrippen van het planningssysteem](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="b2b3f-128">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
 [<span data-ttu-id="b2b3f-129">Ontwerpdetails: Voorraadplanning</span><span class="sxs-lookup"><span data-stu-id="b2b3f-129">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)

