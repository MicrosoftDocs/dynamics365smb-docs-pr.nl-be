---
title: 'Ontwerpdetails: Vraag en aanbod | Microsoft Docs'
description: In dit onderwerp worden de concepten van vraag beschreven, de verzamelterm voor elk soort brutovraag, zoals een verkooporder en materiaalbehoefte van een productieorder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: f808865bd4fc2113dd5c04071f7ba2e8793fe3af
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185576"
---
# <a name="design-details-demand-at-blank-location"></a><span data-ttu-id="9f828-103">Ontwerpdetails: Vraag op lege vestiging</span><span class="sxs-lookup"><span data-stu-id="9f828-103">Design Details: Demand at Blank Location</span></span>
<span data-ttu-id="9f828-104">Wanneer een gebruiker een vraaggebeurtenis maakt, zoals een verkooporderregel, kan de gebruiker soms een vestigingscode toevoegen, maar soms ook niet. In dat geval wordt een lege vestiging gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9f828-104">When a user creates a demand event, such as a sales order line, the program allows the user to sometimes specify a location code and other times not, that is, use blank location.</span></span>

<span data-ttu-id="9f828-105">Voor vraag met of zonder vestigingscodes werkt het planningssysteem eenvoudig en duidelijk wanneer:</span><span class="sxs-lookup"><span data-stu-id="9f828-105">For demand with or without location codes, the planning system operates in a straight forward way when:</span></span>

- <span data-ttu-id="9f828-106">Vraagregels altijd vestigingscodes bevatten en het systeem SKU's gebruikt, inclusief de relevante vestigingsinstellingen.</span><span class="sxs-lookup"><span data-stu-id="9f828-106">Demand lines always carry location codes and the system fully uses SKUs, including the relevant location setup.</span></span>
- <span data-ttu-id="9f828-107">Vraagregels bevatten nooit vestigingscodes en het systeem gebruikt geen SKU's of andere vestigingsinstellingen (zie het laatste scenario in het volgende gedeelte).</span><span class="sxs-lookup"><span data-stu-id="9f828-107">Demand lines never carry location codes, and the system does not use SKUs or any location setup (see the last scenario in the following section).</span></span>

<span data-ttu-id="9f828-108">Als vraaggebeurtenissen echter de ene keer wel vestigingscodes bevatten en de andere keer niet, volgt het planningssysteem bepaalde regels, afhankelijk van de instellingen.</span><span class="sxs-lookup"><span data-stu-id="9f828-108">However, if demand events sometimes have location codes and other times do not, the planning system will follow certain rules depending on setup.</span></span>

## <a name="demand-at-location"></a><span data-ttu-id="9f828-109">Vraag op vestiging</span><span class="sxs-lookup"><span data-stu-id="9f828-109">Demand at Location</span></span>
<span data-ttu-id="9f828-110">Wanneer het planningssysteem ontdekt dat er op een bepaalde vestiging vraag is, reageert het systeem op verschillende manieren, afhankelijk van drie essentiële instellingen.</span><span class="sxs-lookup"><span data-stu-id="9f828-110">When the planning system detects demand at a location, it will behave in different ways depending on three critical setup values.</span></span> <span data-ttu-id="9f828-111">Tijdens de uitvoering van een planning controleert het systeem een voor een de waarden van de drie instellingen en plant aan de hand van die waarden.</span><span class="sxs-lookup"><span data-stu-id="9f828-111">During a planning run, the system checks for three setup values in sequence and plans accordingly.</span></span>

1. <span data-ttu-id="9f828-112">Is het selectievakje **Vestiging verplicht** ingeschakeld?</span><span class="sxs-lookup"><span data-stu-id="9f828-112">Is there a check mark in the **Location Mandatory** field?</span></span>

    <span data-ttu-id="9f828-113">Als dit het geval is dan:</span><span class="sxs-lookup"><span data-stu-id="9f828-113">If yes, then:</span></span>

2. <span data-ttu-id="9f828-114">Bestaat de SKU voor het artikel?</span><span class="sxs-lookup"><span data-stu-id="9f828-114">Does SKU exist for the item?</span></span>

    <span data-ttu-id="9f828-115">Als dit het geval is dan:</span><span class="sxs-lookup"><span data-stu-id="9f828-115">If yes, then:</span></span>

    <span data-ttu-id="9f828-116">Het artikel is gepland aan de hand van de planningsparameters op de SKU-kaart.</span><span class="sxs-lookup"><span data-stu-id="9f828-116">The item is planned according to planning parameters on the SKU card.</span></span>

    <span data-ttu-id="9f828-117">Als dit niet het geval is dan:</span><span class="sxs-lookup"><span data-stu-id="9f828-117">If no, then:</span></span>

3. <span data-ttu-id="9f828-118">Bevat het veld Onderdelen op vestiging de vereiste vestigingscode?</span><span class="sxs-lookup"><span data-stu-id="9f828-118">Does the Components at Location field contain the demanded location code?</span></span>

  <span data-ttu-id="9f828-119">Als dit het geval is dan:</span><span class="sxs-lookup"><span data-stu-id="9f828-119">If yes, then:</span></span>

  <span data-ttu-id="9f828-120">Het artikel is gepland aan de hand van de planningsparameters op de artikelkaart.</span><span class="sxs-lookup"><span data-stu-id="9f828-120">The item is planned according to planning parameters on the item card.</span></span>

  <span data-ttu-id="9f828-121">Als dit niet het geval is dan:</span><span class="sxs-lookup"><span data-stu-id="9f828-121">If no, then:</span></span>

  <span data-ttu-id="9f828-122">Het artikel wordt gepland aan de hand van: Bestelbeleid = Lot-voor-lot, Inclusief voorraad = Ja, alle andere planningsparameters = Leeg, artikelen die gebruikmaken van bestelbeleid = Order blijven zowel Order als de andere instellingen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="9f828-122">The item is planned according to: Reordering Policy = Lot-for-Lot, Include Inventory = Yes, all other planning parameters = Empty, items using Reordering Policy = Order will remain using Order along with the other settings.</span></span>

> [!NOTE]
> <span data-ttu-id="9f828-123">De uitzonderlijke planningsinstelling die wordt uitgevoerd als laatste reactie in stap 3 hierboven, wordt in het volgende "minimaal alternatief" genoemd.</span><span class="sxs-lookup"><span data-stu-id="9f828-123">The exceptional planning setup that is output as the last reaction in step 3 above is referred to in the following as the “minimal alternative”.</span></span> <span data-ttu-id="9f828-124">Deze planningsinstellingen dekken alleen de exacte vraag en alle andere planningsparameters worden genegeerd.</span><span class="sxs-lookup"><span data-stu-id="9f828-124">This planning setup only covers the exact demand, and all other planning parameters are ignored.</span></span>

<span data-ttu-id="9f828-125">Voor informatie over variaties van deze planningslogica raadpleegt u het gedeelte Scenario's hieronder.</span><span class="sxs-lookup"><span data-stu-id="9f828-125">For information about variations of this planning logic, see the Scenarios section below.</span></span>

## <a name="demand-at-blank-location"></a><span data-ttu-id="9f828-126">Vraag op lege vestiging</span><span class="sxs-lookup"><span data-stu-id="9f828-126">Demand at Blank Location</span></span>
<span data-ttu-id="9f828-127">Zelfs als het veld **Vestiging verplicht** is geselecteerd, kan het programma vraagregels zonder een vestigingscode maken, ook wel lege vestiging genoemd.</span><span class="sxs-lookup"><span data-stu-id="9f828-127">Even if the **Location Mandatory** field is selected, the program will allow demand lines to be created without a location code, also referred to as blank location.</span></span> <span data-ttu-id="9f828-128">Dit is een afwijking voor het systeem omdat verschillende instellingswaarden zijn afgestemd op gebruik van vestigingen (zie boven). De planningsengine maakt hierdoor geen planningsregel voor een dergelijke vraagregel.</span><span class="sxs-lookup"><span data-stu-id="9f828-128">This is a deviation for the system because it has various setup values tuned to dealing with locations (see above) and as a result, the planning engine will not create a planning line for such a demand line.</span></span>

<span data-ttu-id="9f828-129">Als het veld **Vestiging verplicht** niet is geselecteerd maar een van de vestigingsinstellingwaarden bestaat, wordt dit ook beschouwd als een afwijking, en wordt door het planningssysteem gereageerd met het "minimale alternatief": het artikel wordt gepland volgens: bestelbeleid = lot-voor-lot (order blijft order), inclusief voorraad = Ja, alle andere planningsparameters = Leeg.</span><span class="sxs-lookup"><span data-stu-id="9f828-129">If the **Location Mandatory** field is not selected but any of the location setup values exist, it is also considered a deviation, and the planning system will react by using the “minimal alternative”: The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

## <a name="scenarios"></a><span data-ttu-id="9f828-130">Scenario's</span><span class="sxs-lookup"><span data-stu-id="9f828-130">Scenarios</span></span>
<span data-ttu-id="9f828-131">In de volgende scenario's worden varianten van de vraag op een lege vestiging omschreven en hoe het planningssysteem wordt ingesteld op het "minimale alternatief".</span><span class="sxs-lookup"><span data-stu-id="9f828-131">The following scenarios describe variations of demand at blank location and how the planning system resolves to the “minimal alternative.”</span></span>

### <a name="setup-1"></a><span data-ttu-id="9f828-132">Instelling 1:</span><span class="sxs-lookup"><span data-stu-id="9f828-132">Setup 1:</span></span>
<span data-ttu-id="9f828-133">Vestiging verplicht = Ja</span><span class="sxs-lookup"><span data-stu-id="9f828-133">Location Mandatory = Yes</span></span>

<span data-ttu-id="9f828-134">SKU is ingesteld voor ROOD</span><span class="sxs-lookup"><span data-stu-id="9f828-134">SKU is set up for RED</span></span>

<span data-ttu-id="9f828-135">Onderdelen op vestiging = BLAUW</span><span class="sxs-lookup"><span data-stu-id="9f828-135">Components at Location = BLUE</span></span>

#### <a name="case-11-demand-is-at-red-location"></a><span data-ttu-id="9f828-136">Case 1.1: vraag is op RODE vestiging</span><span class="sxs-lookup"><span data-stu-id="9f828-136">Case 1.1: Demand is at RED location</span></span>
<span data-ttu-id="9f828-137">Het artikel is gepland aan de hand van de planningsparameters op de SKU-kaart.</span><span class="sxs-lookup"><span data-stu-id="9f828-137">The item is planned according to planning parameters on the SKU card.</span></span>

#### <a name="case-12-demand-is-at-blue-location"></a><span data-ttu-id="9f828-138">Case 1.2: vraag is op BLAUWE vestiging</span><span class="sxs-lookup"><span data-stu-id="9f828-138">Case 1.2: Demand is at BLUE location</span></span>
<span data-ttu-id="9f828-139">Het artikel is gepland volgens: Bestelbeleid = Lot-voor-lot ( Order blijft Order), Inclusief voorraad = Ja, alle andere planningsparameters = Leeg.</span><span class="sxs-lookup"><span data-stu-id="9f828-139">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-13-demand-is-at-green-location"></a><span data-ttu-id="9f828-140">Case 1.3: vraag is op GROENE vestiging</span><span class="sxs-lookup"><span data-stu-id="9f828-140">Case 1.3: Demand is at GREEN location</span></span>
<span data-ttu-id="9f828-141">Het artikel is gepland volgens: Bestelbeleid = Lot-voor-lot ( Order blijft Order), Inclusief voorraad = Ja, alle andere planningsparameters = Leeg.</span><span class="sxs-lookup"><span data-stu-id="9f828-141">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-14-demand-is-at-blank-location"></a><span data-ttu-id="9f828-142">Case 1.4: vraag is op LEGE vestiging</span><span class="sxs-lookup"><span data-stu-id="9f828-142">Case 1.4: Demand is at BLANK location</span></span>
<span data-ttu-id="9f828-143">Het artikel is niet gepland omdat er geen vestiging is gedefinieerd op de vraagregel.</span><span class="sxs-lookup"><span data-stu-id="9f828-143">The item is not planned because no location is defined on the demand line.</span></span>

### <a name="setup-2"></a><span data-ttu-id="9f828-144">Instelling 2:</span><span class="sxs-lookup"><span data-stu-id="9f828-144">Setup 2:</span></span>
<span data-ttu-id="9f828-145">Vestiging verplicht = Ja</span><span class="sxs-lookup"><span data-stu-id="9f828-145">Location Mandatory = Yes</span></span>

<span data-ttu-id="9f828-146">Er bestaat geen SKU</span><span class="sxs-lookup"><span data-stu-id="9f828-146">No SKU exists</span></span>

<span data-ttu-id="9f828-147">Onderdelen op vestiging = BLAUW</span><span class="sxs-lookup"><span data-stu-id="9f828-147">Components at Location = BLUE</span></span>

#### <a name="case-21-demand-is-at-red-location"></a><span data-ttu-id="9f828-148">Case 2.1: vraag is op RODE vestiging</span><span class="sxs-lookup"><span data-stu-id="9f828-148">Case 2.1: Demand is at RED location</span></span>
<span data-ttu-id="9f828-149">Het artikel is gepland volgens: Bestelbeleid = Lot-voor-lot ( Order blijft Order), Inclusief voorraad = Ja, alle andere planningsparameters = Leeg.</span><span class="sxs-lookup"><span data-stu-id="9f828-149">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-22-demand-is-at-blue-location"></a><span data-ttu-id="9f828-150">Case 2.2: vraag is op BLAUWE vestiging</span><span class="sxs-lookup"><span data-stu-id="9f828-150">Case 2.2: Demand is at BLUE location</span></span>
<span data-ttu-id="9f828-151">Het artikel is gepland aan de hand van de planningsparameters op de artikelkaart.</span><span class="sxs-lookup"><span data-stu-id="9f828-151">The item is planned according to planning parameters on the item card.</span></span>

### <a name="setup-3"></a><span data-ttu-id="9f828-152">Instelling 3:</span><span class="sxs-lookup"><span data-stu-id="9f828-152">Setup 3:</span></span>
<span data-ttu-id="9f828-153">Vestiging verplicht = Nee</span><span class="sxs-lookup"><span data-stu-id="9f828-153">Location Mandatory = No</span></span>

<span data-ttu-id="9f828-154">Er bestaat geen SKU</span><span class="sxs-lookup"><span data-stu-id="9f828-154">No SKU exists</span></span>

<span data-ttu-id="9f828-155">Onderdelen op vestiging = BLAUW</span><span class="sxs-lookup"><span data-stu-id="9f828-155">Components at Location = BLUE</span></span>

#### <a name="case-31-demand-is-at-red-location"></a><span data-ttu-id="9f828-156">Case 3.1: vraag is op RODE vestiging</span><span class="sxs-lookup"><span data-stu-id="9f828-156">Case 3.1: Demand is at RED location</span></span>
<span data-ttu-id="9f828-157">Het artikel is gepland volgens: Bestelbeleid = Lot-voor-lot ( Order blijft Order), Inclusief voorraad = Ja, alle andere planningsparameters = Leeg.</span><span class="sxs-lookup"><span data-stu-id="9f828-157">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-32-demand-is-at-blue-location"></a><span data-ttu-id="9f828-158">Case 3.2: vraag is op BLAUWE vestiging</span><span class="sxs-lookup"><span data-stu-id="9f828-158">Case 3.2: Demand is at BLUE location</span></span>
<span data-ttu-id="9f828-159">Het artikel is gepland aan de hand van de planningsparameters op de artikelkaart.</span><span class="sxs-lookup"><span data-stu-id="9f828-159">The item is planned according to planning parameters on the item card.</span></span>

#### <a name="case-33-demand-is-at-blank-location"></a><span data-ttu-id="9f828-160">Case 3.3: vraag is op LEGE vestiging</span><span class="sxs-lookup"><span data-stu-id="9f828-160">Case 3.3: Demand is at BLANK location</span></span>
<span data-ttu-id="9f828-161">Het artikel is gepland volgens: Bestelbeleid = Lot-voor-lot ( Order blijft Order), Inclusief voorraad = Ja, alle andere planningsparameters = Leeg.</span><span class="sxs-lookup"><span data-stu-id="9f828-161">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

### <a name="setup-4"></a><span data-ttu-id="9f828-162">Instelling 4:</span><span class="sxs-lookup"><span data-stu-id="9f828-162">Setup 4:</span></span>
<span data-ttu-id="9f828-163">Vestiging verplicht = Nee</span><span class="sxs-lookup"><span data-stu-id="9f828-163">Location Mandatory = No</span></span>

<span data-ttu-id="9f828-164">Er bestaat geen SKU</span><span class="sxs-lookup"><span data-stu-id="9f828-164">No SKU exists</span></span>

<span data-ttu-id="9f828-165">Onderdelen op vestiging = LEEG</span><span class="sxs-lookup"><span data-stu-id="9f828-165">Components at Location = BLANK</span></span>

#### <a name="case-41-demand-is-at-blue-location"></a><span data-ttu-id="9f828-166">Case 4.1: vraag is op BLAUWE vestiging</span><span class="sxs-lookup"><span data-stu-id="9f828-166">Case 4.1: Demand is at BLUE location</span></span>
<span data-ttu-id="9f828-167">Het artikel is gepland volgens: Bestelbeleid = Lot-voor-lot ( Order blijft Order), Inclusief voorraad = Ja, alle andere planningsparameters = Leeg.</span><span class="sxs-lookup"><span data-stu-id="9f828-167">The item is planned according to: Reordering Policy = Lot-for-Lot (Order remains Order), Include Inventory = Yes, all other planning parameters = Empty.</span></span>

#### <a name="case-42-demand-is-at-blank-location"></a><span data-ttu-id="9f828-168">Case 4.2: vraag is op LEGE vestiging</span><span class="sxs-lookup"><span data-stu-id="9f828-168">Case 4.2: Demand is at BLANK location</span></span>
<span data-ttu-id="9f828-169">Het artikel is gepland aan de hand van de planningsparameters op de artikelkaart.</span><span class="sxs-lookup"><span data-stu-id="9f828-169">The item is planned according to planning parameters on the item card.</span></span>

<span data-ttu-id="9f828-170">Zoals in het laatste scenario wordt getoond, kunt u alleen een correct resultaat krijgen voor een vraagregel zonder vestigingscode door alle instellingswaarden uit te schakelen die naar vestigingen verwijzen.</span><span class="sxs-lookup"><span data-stu-id="9f828-170">As illustrated in the last scenario, the only way to get a correct result for a demand line without a location code is to disable all setup values relating to locations.</span></span> <span data-ttu-id="9f828-171">Zo krijgt u ook alleen stabiele planningsresultaten voor vraag op vestigingen als u SKU's gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9f828-171">Similarly, the only way to get stable planning results for demand at locations is to use SKUs.</span></span> <span data-ttu-id="9f828-172">Als bedrijven dus vaak plannen voor vraag op vestigingen, wordt hun sterk aangeraden de granule voor SKU's te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="9f828-172">Therefore, if companies often plan for demand at locations, they are strongly advised to use the Stockkeeping Units granule.</span></span>

## <a name="see-also"></a><span data-ttu-id="9f828-173">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9f828-173">See Also</span></span>  
<span data-ttu-id="9f828-174">[Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md) </span><span class="sxs-lookup"><span data-stu-id="9f828-174">[Design Details: Balancing Demand and Supply](design-details-balancing-demand-and-supply.md) </span></span>  
<span data-ttu-id="9f828-175">[Ontwerpdetails: Centrale begrippen van het planningssysteem](design-details-central-concepts-of-the-planning-system.md) </span><span class="sxs-lookup"><span data-stu-id="9f828-175">[Design Details: Central Concepts of the Planning System](design-details-central-concepts-of-the-planning-system.md) </span></span>  
[<span data-ttu-id="9f828-176">Ontwerpdetails: Voorraadplanning</span><span class="sxs-lookup"><span data-stu-id="9f828-176">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
