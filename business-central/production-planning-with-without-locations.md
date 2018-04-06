---
title: Planning met of zonder vestigingen | Microsoft Docs
description: Het is belangrijk dat u planningen met of zonder vestigingscodes op vraagregels begrijpt.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a2043b50e9f398839034c87e8f0fb42f68d8c036
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="planning-with-or-without-locations"></a><span data-ttu-id="f810b-103">Planning met of zonder vestigingen</span><span class="sxs-lookup"><span data-stu-id="f810b-103">Planning With or Without Locations</span></span>
<span data-ttu-id="f810b-104">Ten aanzien van de planning met of zonder vestigingscodes op vraagregels, werkt het planningssysteem eenvoudig en duidelijk wanneer:</span><span class="sxs-lookup"><span data-stu-id="f810b-104">Concerning planning with or without location codes on demand lines, the planning system operates in a straight forward way when:</span></span>  

-   <span data-ttu-id="f810b-105">vraagregels altijd vestigingscodes bevatten en het systeem SKU's gebruikt, inclusief de relevante vestigingsinstellingen.</span><span class="sxs-lookup"><span data-stu-id="f810b-105">demand lines always carry location codes and the system fully uses stockkeeping units, including the relevant location setup.</span></span>  
-   <span data-ttu-id="f810b-106">vraagregels nooit vestigingscodes bevatten en het systeem geen SKU's of andere vestigingsinstellingen gebruikt (zie het laatste scenario hieronder).</span><span class="sxs-lookup"><span data-stu-id="f810b-106">demand lines never carry location codes and the system does not use SKUs or any location setup (see last scenario below).</span></span>  

<span data-ttu-id="f810b-107">Als vraagregels echter de ene keer wel vestigingscodes bevatten en de andere keer niet, volgt het planningssysteem bepaalde regels, afhankelijk van de instellingen.</span><span class="sxs-lookup"><span data-stu-id="f810b-107">However, if demand lines sometimes have location codes and other times do not, the planning system will follow certain rules depending on setup.</span></span>  

## <a name="demand-at-location"></a><span data-ttu-id="f810b-108">Vraag op vestiging</span><span class="sxs-lookup"><span data-stu-id="f810b-108">Demand at Location</span></span>  
<span data-ttu-id="f810b-109">Wanneer het planningssysteem ontdekt dat er op een bepaalde vestiging vraag is (een regel met een vestigingscode), reageert het systeem op verschillende manieren, afhankelijk van drie essentiële instellingen.</span><span class="sxs-lookup"><span data-stu-id="f810b-109">When the planning system detects demand at a location (a line with a location code), it will behave in different ways depending on 3 critical setup values.</span></span>  

<span data-ttu-id="f810b-110">Tijdens de uitvoering van een planning controleert het systeem een voor een de waarden van de drie instellingen en plant aan de hand van die waarden:</span><span class="sxs-lookup"><span data-stu-id="f810b-110">During a planning run, the system checks for the 3 setup values in sequence and plans accordingly:</span></span>  

1.  <span data-ttu-id="f810b-111">Is het selectievakje **Vestiging verplicht** ingeschakeld?</span><span class="sxs-lookup"><span data-stu-id="f810b-111">Is there a check mark in the **Location Mandatory** field?</span></span>  

    <span data-ttu-id="f810b-112">Als dit het geval is dan:</span><span class="sxs-lookup"><span data-stu-id="f810b-112">If yes, then:</span></span>  

2.  <span data-ttu-id="f810b-113">Bestaat de SKU voor het artikel?</span><span class="sxs-lookup"><span data-stu-id="f810b-113">Does SKU exist for the item?</span></span>  

    <span data-ttu-id="f810b-114">Als dit het geval is dan:</span><span class="sxs-lookup"><span data-stu-id="f810b-114">If yes, then:</span></span>  

    <span data-ttu-id="f810b-115">Het artikel is gepland aan de hand van de planningsparameters op de SKU-kaart.</span><span class="sxs-lookup"><span data-stu-id="f810b-115">The item is planned according to planning parameters on the SKU card.</span></span>  

    <span data-ttu-id="f810b-116">Als dit niet het geval is dan:</span><span class="sxs-lookup"><span data-stu-id="f810b-116">If no, then:</span></span>  

3.  <span data-ttu-id="f810b-117">Bevat het veld **Onderdelen op vestiging** de vereiste vestigingscode?</span><span class="sxs-lookup"><span data-stu-id="f810b-117">Does the **Components at Location** field contain the demanded location code?</span></span>  

    <span data-ttu-id="f810b-118">Als dit het geval is dan:</span><span class="sxs-lookup"><span data-stu-id="f810b-118">If yes, then:</span></span>  

    <span data-ttu-id="f810b-119">Het artikel is gepland aan de hand van de planningsparameters op de artikelkaart.</span><span class="sxs-lookup"><span data-stu-id="f810b-119">The item is planned according to planning parameters on the item card.</span></span>  

    <span data-ttu-id="f810b-120">Als dit niet het geval is dan:</span><span class="sxs-lookup"><span data-stu-id="f810b-120">If no, then:</span></span>  

    <span data-ttu-id="f810b-121">Het artikel is gepland aan de hand van: Bestelbeleid =  *Lot-for-Lot*, Inclusief voorraad =  *Ja*, alle andere planningsparameters = Leeg.</span><span class="sxs-lookup"><span data-stu-id="f810b-121">The item is planned according to: Reordering Policy =  *Lot-for-Lot*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span> <span data-ttu-id="f810b-122">(Artikelen die gebruikmaken van het bestelbeleid  *Order* blijven zowel  *Order* als de andere instellingen gebruiken.)</span><span class="sxs-lookup"><span data-stu-id="f810b-122">(Items using reordering policy  *Order* remain using  *Order* as well as the other settings.)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f810b-123">Dit minimale alternatief dekt alleen de exacte vraag.</span><span class="sxs-lookup"><span data-stu-id="f810b-123">This minimal alternative only covers the exact demand.</span></span> <span data-ttu-id="f810b-124">Alle gedefinieerde planningsparameters worden genegeerd.</span><span class="sxs-lookup"><span data-stu-id="f810b-124">Any planning parameters defined are ignored.</span></span>  

<span data-ttu-id="f810b-125">Zie de variaties in de onderstaande scenario's.</span><span class="sxs-lookup"><span data-stu-id="f810b-125">See variations in the scenarios below.</span></span>  

## <a name="demand-at-blank-location"></a><span data-ttu-id="f810b-126">Vraag op 'lege vestiging'</span><span class="sxs-lookup"><span data-stu-id="f810b-126">Demand at "Blank Location"</span></span>  
<span data-ttu-id="f810b-127">Zelfs als het selectievakje **Vestiging verplicht** ingeschakeld is, kan het systeem vraagregels zonder een vestigingscode maken, ook wel *LEGE* vestigingen genoemd.</span><span class="sxs-lookup"><span data-stu-id="f810b-127">Even if the **Location Mandatory** check box is selected, the system will allow demand lines to be created without a location code – also referred to as *BLANK* location.</span></span> <span data-ttu-id="f810b-128">Dit is een afwijking voor het systeem omdat verschillende instellingswaarden zijn afgestemd op gebruik van vestigingen (zie boven). De planningsengine maakt hierdoor geen planningsregel voor een dergelijke vraagregel.</span><span class="sxs-lookup"><span data-stu-id="f810b-128">This is a deviation for the system because it has various setup values tuned to dealing with locations (see above) and as a result, the planning engine will not create a planning line for such a demand line.</span></span> <span data-ttu-id="f810b-129">Als het veld **Vestiging verplicht** niet ingeschakeld is, maar een van de instellingswaarden voor vestigingen bestaat, wordt er ook uitgegaan van een afwijking en reageert het planningssysteem met het 'minimale alternatief' als uitvoer:</span><span class="sxs-lookup"><span data-stu-id="f810b-129">If the **Location Mandatory** field is not selected but any of the location setup values exist, then that is also considered a deviation and the planning system will react by outputting the "minimal alternative":</span></span>   
<span data-ttu-id="f810b-130">Het artikel wordt gepland volgens: Bestelbeleid =  *Lot-for-Lot* ( *Order* blijft *Order)*, Inclusief voorraad =  *Ja*, alle andere planningsparameters = Leeg.</span><span class="sxs-lookup"><span data-stu-id="f810b-130">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains *Order)*, Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

<span data-ttu-id="f810b-131">Zie de variaties in de onderstaande configuratiescenario's.</span><span class="sxs-lookup"><span data-stu-id="f810b-131">See variations in the setup scenarios below.</span></span>  

### <a name="setup-1"></a><span data-ttu-id="f810b-132">Instelling 1:</span><span class="sxs-lookup"><span data-stu-id="f810b-132">Setup 1:</span></span>  

-   <span data-ttu-id="f810b-133">Vestiging verplicht = *Ja*</span><span class="sxs-lookup"><span data-stu-id="f810b-133">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="f810b-134">SKU is ingesteld voor  *ROOD*</span><span class="sxs-lookup"><span data-stu-id="f810b-134">SKU is set up for  *RED*</span></span>  
-   <span data-ttu-id="f810b-135">Onderdeel op vestiging =  *BLAUW*</span><span class="sxs-lookup"><span data-stu-id="f810b-135">Component at Location =  *BLUE*</span></span>  

#### <a name="case-11-demand-is-at--red-location"></a><span data-ttu-id="f810b-136">Case 1.1: vraag is op  *RODE* vestiging</span><span class="sxs-lookup"><span data-stu-id="f810b-136">Case 1.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="f810b-137">Het artikel is gepland volgens planningsparameters op de SKU-kaart (inclusief mogelijke transfer).</span><span class="sxs-lookup"><span data-stu-id="f810b-137">The item is planned according to planning parameters on the SKU card (including possible transfer).</span></span>  

#### <a name="case-12-demand-is-at--blue-location"></a><span data-ttu-id="f810b-138">Case 1.2: vraag is op *BLAUWE* vestiging</span><span class="sxs-lookup"><span data-stu-id="f810b-138">Case 1.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="f810b-139">Het artikel is gepland aan de hand van de planningsparameters op de artikelkaart.</span><span class="sxs-lookup"><span data-stu-id="f810b-139">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-13-demand-is-at--green-location"></a><span data-ttu-id="f810b-140">Case 1.3: vraag is op  *GROENE* vestiging</span><span class="sxs-lookup"><span data-stu-id="f810b-140">Case 1.3: Demand is at  *GREEN* location</span></span>  

<span data-ttu-id="f810b-141">Het artikel is gepland volgens: Bestelbeleid =  *Lot-for-Lot* ( *Order* blijft  *Order*), Inclusief voorraad =  *Ja*, alle andere planningsparameters = Leeg.</span><span class="sxs-lookup"><span data-stu-id="f810b-141">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-14-demand-is-at--blank-location"></a><span data-ttu-id="f810b-142">Case 1.4: vraag is op *LEGE* vestiging</span><span class="sxs-lookup"><span data-stu-id="f810b-142">Case 1.4: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="f810b-143">Het artikel is niet gepland omdat er geen vestiging is gedefinieerd op de vraagregel.</span><span class="sxs-lookup"><span data-stu-id="f810b-143">The item is not planned because no location is defined on the demand line.</span></span>  

### <a name="setup-2"></a><span data-ttu-id="f810b-144">Instelling 2:</span><span class="sxs-lookup"><span data-stu-id="f810b-144">Setup 2:</span></span>  

-   <span data-ttu-id="f810b-145">Vestiging verplicht = *Ja*</span><span class="sxs-lookup"><span data-stu-id="f810b-145">Location Mandatory = *Yes*</span></span>  
-   <span data-ttu-id="f810b-146">Er bestaat geen SKU</span><span class="sxs-lookup"><span data-stu-id="f810b-146">No SKU exists</span></span>  
-   <span data-ttu-id="f810b-147">Onderdeel op vestiging =  *BLAUW*</span><span class="sxs-lookup"><span data-stu-id="f810b-147">Component at Location =  *BLUE*</span></span>  

#### <a name="case-21-demand-is-at--red-location"></a><span data-ttu-id="f810b-148">Case 2.1: vraag is op  *RODE* vestiging</span><span class="sxs-lookup"><span data-stu-id="f810b-148">Case 2.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="f810b-149">Het artikel is gepland volgens: Bestelbeleid =  *Lot-for-Lot* ( *Order* blijft  *Order*), Inclusief voorraad =  *Ja*, alle andere planningsparameters = Leeg.</span><span class="sxs-lookup"><span data-stu-id="f810b-149">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-22-demand-is-at--blue-location"></a><span data-ttu-id="f810b-150">Case 2.2: vraag is op *BLAUWE* vestiging</span><span class="sxs-lookup"><span data-stu-id="f810b-150">Case 2.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="f810b-151">Het artikel is gepland aan de hand van de planningsparameters op de artikelkaart.</span><span class="sxs-lookup"><span data-stu-id="f810b-151">The item is planned according to planning parameters on the item card.</span></span>  

### <a name="setup-3"></a><span data-ttu-id="f810b-152">Instelling 3:</span><span class="sxs-lookup"><span data-stu-id="f810b-152">Setup 3:</span></span>  

-   <span data-ttu-id="f810b-153">Vestiging verplicht = *Nee*</span><span class="sxs-lookup"><span data-stu-id="f810b-153">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="f810b-154">Er bestaat geen SKU</span><span class="sxs-lookup"><span data-stu-id="f810b-154">No SKU exists</span></span>  
-   <span data-ttu-id="f810b-155">Onderdeel op vestiging =  *BLAUW*</span><span class="sxs-lookup"><span data-stu-id="f810b-155">Component at Location =  *BLUE*</span></span>  

#### <a name="case-31-demand-is-at--red-location"></a><span data-ttu-id="f810b-156">Case 3.1: vraag is op  *RODE* vestiging</span><span class="sxs-lookup"><span data-stu-id="f810b-156">Case 3.1: Demand is at  *RED* location</span></span>  

<span data-ttu-id="f810b-157">Het artikel is gepland volgens: Bestelbeleid =  *Lot-for-Lot* ( *Order* blijft  *Order*), Inclusief voorraad =  *Ja*, alle andere planningsparameters = Leeg.</span><span class="sxs-lookup"><span data-stu-id="f810b-157">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-32-demand-is-at--blue-location"></a><span data-ttu-id="f810b-158">Case 3.2: vraag is op *BLAUWE* vestiging</span><span class="sxs-lookup"><span data-stu-id="f810b-158">Case 3.2: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="f810b-159">Het artikel is gepland aan de hand van de planningsparameters op de artikelkaart.</span><span class="sxs-lookup"><span data-stu-id="f810b-159">The item is planned according to planning parameters on the item card.</span></span>  

#### <a name="case-33-demand-is-at--blank-location"></a><span data-ttu-id="f810b-160">Case 3.3: Vraag is op  *LEGE* vestiging</span><span class="sxs-lookup"><span data-stu-id="f810b-160">Case 3.3: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="f810b-161">Het artikel is gepland volgens: Bestelbeleid =  *Lot-for-Lot* ( *Order* blijft  *Order*), Inclusief voorraad =  *Ja*, alle andere planningsparameters = Leeg.</span><span class="sxs-lookup"><span data-stu-id="f810b-161">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

### <a name="setup-4"></a><span data-ttu-id="f810b-162">Instelling 4:</span><span class="sxs-lookup"><span data-stu-id="f810b-162">Setup 4:</span></span>  

-   <span data-ttu-id="f810b-163">Vestiging verplicht = *Nee*</span><span class="sxs-lookup"><span data-stu-id="f810b-163">Location Mandatory = *No*</span></span>  
-   <span data-ttu-id="f810b-164">Er bestaat geen SKU</span><span class="sxs-lookup"><span data-stu-id="f810b-164">No SKU exists</span></span>  
-   <span data-ttu-id="f810b-165">Onderdeel op vestiging =  *LEEG*</span><span class="sxs-lookup"><span data-stu-id="f810b-165">Component at Location =  *BLANK*</span></span>  

#### <a name="case-41-demand-is-at--blue-location"></a><span data-ttu-id="f810b-166">Case 4.1: vraag is op  *BLAUWE* vestiging</span><span class="sxs-lookup"><span data-stu-id="f810b-166">Case 4.1: Demand is at  *BLUE* location</span></span>  

<span data-ttu-id="f810b-167">Het artikel is gepland volgens: Bestelbeleid =  *Lot-for-Lot* ( *Order* blijft  *Order*), Inclusief voorraad =  *Ja*, alle andere planningsparameters = Leeg.</span><span class="sxs-lookup"><span data-stu-id="f810b-167">The item is planned according to: Reordering Policy =  *Lot-for-Lot* ( *Order* remains  *Order*), Include Inventory =  *Yes*, all other planning parameters = Empty.</span></span>  

#### <a name="case-42-demand-is-at--blank-location"></a><span data-ttu-id="f810b-168">Case 4.2: Vraag is op  *LEGE* vestiging</span><span class="sxs-lookup"><span data-stu-id="f810b-168">Case 4.2: Demand is at  *BLANK* location</span></span>  

<span data-ttu-id="f810b-169">Het artikel is gepland aan de hand van de planningsparameters op de artikelkaart.</span><span class="sxs-lookup"><span data-stu-id="f810b-169">The item is planned according to planning parameters on the item card.</span></span>  

<span data-ttu-id="f810b-170">Zoals u in het laatste scenario kunt zien, kunt u alleen een correct resultaat krijgen voor een vraagregel zonder vestigingscode door alle instellingswaarden uit te schakelen die naar vestigingen verwijzen.</span><span class="sxs-lookup"><span data-stu-id="f810b-170">As you can see from the last scenario, the only way to get a correct result for a demand line without a location code is to disable all setup values relating to locations.</span></span> <span data-ttu-id="f810b-171">Zo krijgt u ook alleen stabiele planningsresultaten voor vraag op vestigingen als u SKU's gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f810b-171">Similarly, the only way to get stable planning results for demand at locations is to use stockkeeping units.</span></span>  

<span data-ttu-id="f810b-172">Als u dus vaak plant voor vraag op vestigingen, wordt u sterk aangeraden de functie voor SKU's te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="f810b-172">Therefore, if you often plan for demand at locations, it is strongly advised to use the Stockkeeping Units feature.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f810b-173">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f810b-173">See Also</span></span>
<span data-ttu-id="f810b-174">[Gepland](production-planning.md)  </span><span class="sxs-lookup"><span data-stu-id="f810b-174">[Planning](production-planning.md)  </span></span>  
[<span data-ttu-id="f810b-175">Productie instellen</span><span class="sxs-lookup"><span data-stu-id="f810b-175">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="f810b-176">[Productie](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="f810b-176">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="f810b-177">Voorraad</span><span class="sxs-lookup"><span data-stu-id="f810b-177">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="f810b-178">Inkoop</span><span class="sxs-lookup"><span data-stu-id="f810b-178">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="f810b-179">[Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="f810b-179">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="f810b-180">Aanbevolen procedures instellen: voorraadplanning</span><span class="sxs-lookup"><span data-stu-id="f810b-180">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="f810b-181">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f810b-181">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

