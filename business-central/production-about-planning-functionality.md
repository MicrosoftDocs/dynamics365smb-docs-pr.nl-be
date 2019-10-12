---
title: Informatie over het plannen van functionaliteit | Microsoft Docs
description: Het planningssysteem houdt rekening met alle gegevens over vraag en voorzieningen, berekent het nettoresultaat, en doet suggesties voor het in overeenstemming brengen van de voorzieningen en de vraag.
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
ms.openlocfilehash: 27a2a105cbb6a8a449de44c564dc448ec6136d61
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2313480"
---
# <a name="about-planning-functionality"></a><span data-ttu-id="ff23c-103">Informatie over het plannen van functionaliteit</span><span class="sxs-lookup"><span data-stu-id="ff23c-103">About Planning Functionality</span></span>
<span data-ttu-id="ff23c-104">Het planningssysteem houdt rekening met alle gegevens over vraag en aanbod, berekent het nettoresultaat en doet suggesties voor het in overeenstemming brengen van aanbod en vraag.</span><span class="sxs-lookup"><span data-stu-id="ff23c-104">The planning system takes all demand and supply data into account, nets the results, and creates suggestions for balancing the supply to meet the demand.</span></span>  

<span data-ttu-id="ff23c-105">Zie [Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md) voor gedetailleerde informatie.</span><span class="sxs-lookup"><span data-stu-id="ff23c-105">For detailed information, see [Design Details: Supply Planning](design-details-supply-planning.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="ff23c-106">Voor alle velden die in dit onderwerp worden genoemd, kunt u de knopinfo lezen om de functie te begrijpen.</span><span class="sxs-lookup"><span data-stu-id="ff23c-106">For all the fields that are mentioned in this topic, read the tooltip to understand their function.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a><span data-ttu-id="ff23c-107">Vraag en voorzieningen</span><span class="sxs-lookup"><span data-stu-id="ff23c-107">Demand and Supply</span></span>  
<span data-ttu-id="ff23c-108">Planning bestaat uit twee elementen: vraag en voorzieningen.</span><span class="sxs-lookup"><span data-stu-id="ff23c-108">Planning has two elements: demand and supply.</span></span> <span data-ttu-id="ff23c-109">Deze moeten in evenwicht worden gehouden, zodat op tijd en op een kosteneffectieve wijze aan de vraag wordt voldaan.</span><span class="sxs-lookup"><span data-stu-id="ff23c-109">These must be held in balance to ensure that the demand is met in a timely and cost-efficient manner.</span></span>  

- <span data-ttu-id="ff23c-110">Vraag is een gebruikelijke term voor elke soort brutobehoefte, zoals een verkooporder, serviceorder, materiaalbehoefte vanuit een assemblage- of productieorder, transfer uit, raamcontract of prognose.</span><span class="sxs-lookup"><span data-stu-id="ff23c-110">Demand is the common term used for any kind of gross requirement such as a sales order, service order, component need from assembly or production orders, outbound transfer, blanket order or forecast.</span></span> <span data-ttu-id="ff23c-111">Daarnaast voorziet de toepassing in enkele andere technische soorten vraag, zoals een negatieve productie- of inkooporder, negatieve voorraad en inkoopretour.</span><span class="sxs-lookup"><span data-stu-id="ff23c-111">In addition to these, application allows some other technical types of demand - such as a negative production or purchase order, negative inventory, and purchase return.</span></span>  
- <span data-ttu-id="ff23c-112">Voorzieningen is een gebruikelijke term voor elke soort aanvulling, zoals voorraad, een inkoop-, assemblage- of productieorder, of transfer in.</span><span class="sxs-lookup"><span data-stu-id="ff23c-112">Supply is the common word used for any kind of replenishment such as inventory, a purchase order, assembly order, production order, or inbound transfer.</span></span> <span data-ttu-id="ff23c-113">Ter vergelijking kunnen er ook een negatieve verkoop- of serviceorder, negatieve materiaalbehoefte of verkoopretour zijn, die alle op de een of andere wijze ook voorzieningen weergeven.</span><span class="sxs-lookup"><span data-stu-id="ff23c-113">Correspondingly, there can be a negative sales or service order, negative component need or sales return – all of which in some way also represent supply.</span></span>  

<span data-ttu-id="ff23c-114">Een ander doel van het planningssysteem is ervoor te zorgen dat de voorraad niet onnodig toeneemt.</span><span class="sxs-lookup"><span data-stu-id="ff23c-114">Another goal of the planning system is to ensure that the inventory does not grow unnecessarily.</span></span> <span data-ttu-id="ff23c-115">In het geval van een afnemende vraag zal het planningssysteem voorstellen om bestaande aanvullingsorders uit te stellen, in omvang te verkleinen of te annuleren.</span><span class="sxs-lookup"><span data-stu-id="ff23c-115">In the case of decreasing demand, the planning system will suggest that you postpone, decrease in quantity, or cancel existing replenishment orders.</span></span>  

## <a name="planning-calculation"></a><span data-ttu-id="ff23c-116">Planningsberekening</span><span class="sxs-lookup"><span data-stu-id="ff23c-116">Planning Calculation</span></span>  
<span data-ttu-id="ff23c-117">Het planningssysteem wordt gestuurd door de verwachte en werkelijke vraag van klanten, alsmede de parameters van de voorraadinkoopvoorstellen.</span><span class="sxs-lookup"><span data-stu-id="ff23c-117">The planning system is driven by anticipated and actual customer demand, as well as inventory reordering parameters.</span></span> <span data-ttu-id="ff23c-118">Het uitvoeren van de planningsberekening leidt ertoe dat de toepassing specifieke acties (planningsboodschappen) voorstelt die genomen dienen te worden met betrekking tot mogelijke aanvullingen door leveranciers, transfers tussen magazijnen of productie.</span><span class="sxs-lookup"><span data-stu-id="ff23c-118">Running the planning calculation will result in application suggesting specific actions (Action Messages) to take concerning possible replenishment from vendors, transfers between warehouses, or production.</span></span> <span data-ttu-id="ff23c-119">Als er al aanvullingsorders zijn, kunnen de voorgestelde acties bestaan uit het vergroten of versnellen van de orders om te voorzien in veranderingen in de vraag.</span><span class="sxs-lookup"><span data-stu-id="ff23c-119">If replenishment orders already exist, the suggested actions could be to increase or expedite the orders to meet the changes in demand.</span></span>  

<span data-ttu-id="ff23c-120">De basis van de planningsroutine is gelegen in de bruto-naar-netto-berekening.</span><span class="sxs-lookup"><span data-stu-id="ff23c-120">The basis of the planning routine is in the gross-to-net calculation.</span></span> <span data-ttu-id="ff23c-121">De nettobehoeften sturen de geplande ordervrijgaven, die worden gepland op basis van de bewerkingsplaninformatie (geproduceerde artikelen) of de artikeldoorlooptijd (ingekochte artikelen).</span><span class="sxs-lookup"><span data-stu-id="ff23c-121">Net requirements drive planned order releases, which are scheduled based on the routing information (manufactured items) or the item card lead time (purchased items).</span></span> <span data-ttu-id="ff23c-122">De aantallen van geplande ordervrijgaven zijn gebaseerd op de planningsberekening en worden beïnvloed door de parameters die zijn ingesteld op de afzonderlijke artikelkaarten.</span><span class="sxs-lookup"><span data-stu-id="ff23c-122">Planned order release quantities are based on the planning calculation, and are affected by the parameters set on the individual item cards.</span></span>  

## <a name="planning-with-manual-transfer-orders"></a><span data-ttu-id="ff23c-123">Planning met handmatige transferorders</span><span class="sxs-lookup"><span data-stu-id="ff23c-123">Planning with Manual Transfer Orders</span></span>
<span data-ttu-id="ff23c-124">In het veld **Aanvullingsmethode** op een SKU-kaart kunt u zien dat het planningssysteem zo kan worden ingesteld dat er transferorders worden gemaakt om voorraad en vraag op alle vestigingen in balans te brengen.</span><span class="sxs-lookup"><span data-stu-id="ff23c-124">As you can see from the **Replenishment System** field on a SKU card, the planning system can be set up to create transfer orders to balance supply and demand across locations.</span></span>  

<span data-ttu-id="ff23c-125">Naast dergelijke automatische transferorders, moet u mogelijk zo nu en dan voorraadhoeveelheden naar een andere vestiging verplaatsen, ongeacht de bestaande vraag.</span><span class="sxs-lookup"><span data-stu-id="ff23c-125">In addition to such automatic transfer orders, you may sometimes need to perform a general move of inventory quantities to another location, irrespective of existing demand.</span></span> <span data-ttu-id="ff23c-126">U kunt voor dit doel handmatig een transferorder maken voor de hoeveelheid die moet worden verplaatst.</span><span class="sxs-lookup"><span data-stu-id="ff23c-126">For this purpose you would manually create a transfer order for the quantity to move.</span></span> <span data-ttu-id="ff23c-127">U kunt ervoor zorgen dat het planningssysteem deze handmatige transferorder niet wijzigt door het veld **Planningsflexibiliteit** op de transferregel(s) in te stellen op Geen.</span><span class="sxs-lookup"><span data-stu-id="ff23c-127">To ensure that the planning system does not try to manipulate this manual transfer order, you must set the **Planning Flexibility** on the transfer line(s) to None.</span></span>  

<span data-ttu-id="ff23c-128">Daar staat tegenover dat u het veld **Planningsflexibiliteit** moet instellen op de standaardwaarde Ongelimiteerd als u wilt dat het planningssysteem de hoeveelheden van de transferorder en de datums wel wijzigt op basis van de bestaande vraag.</span><span class="sxs-lookup"><span data-stu-id="ff23c-128">Contrarily, if you do want the planning system to adjust the transfer order quantities and dates to existing demand, you must set the **Planning Flexibility** field to the default value, Unlimited.</span></span>

## <a name="planning-parameters"></a><span data-ttu-id="ff23c-129">Planningsparameters</span><span class="sxs-lookup"><span data-stu-id="ff23c-129">Planning Parameters</span></span>  
<span data-ttu-id="ff23c-130">De planningsparameters bepalen wanneer, hoeveel en hoe er wordt aangevuld op basis van de verschillende instellingen op de artikelkaart (SKU) en de productie-instellingen.</span><span class="sxs-lookup"><span data-stu-id="ff23c-130">The planning parameters control when, how much, and how to replenish based on the various settings on the item card (or stockkeeping unit - SKU), and the manufacturing setup.</span></span>  

<span data-ttu-id="ff23c-131">De volgende planningsparameters bestaan op de artikel-/SKU-kaart:</span><span class="sxs-lookup"><span data-stu-id="ff23c-131">The following planning parameters exist on the item or SKU card:</span></span>  

-   <span data-ttu-id="ff23c-132">Dempingsperiode</span><span class="sxs-lookup"><span data-stu-id="ff23c-132">Dampener Period</span></span>  
-   <span data-ttu-id="ff23c-133">Dempingsaantal</span><span class="sxs-lookup"><span data-stu-id="ff23c-133">Dampener Quantity</span></span>  
-   <span data-ttu-id="ff23c-134">Bestelbeleid</span><span class="sxs-lookup"><span data-stu-id="ff23c-134">Reordering Policy</span></span>  
-   <span data-ttu-id="ff23c-135">Bestelpunt</span><span class="sxs-lookup"><span data-stu-id="ff23c-135">Reorder Point</span></span>
-   <span data-ttu-id="ff23c-136">Maximale voorraad</span><span class="sxs-lookup"><span data-stu-id="ff23c-136">Maximum Inventory</span></span>  
-   <span data-ttu-id="ff23c-137">Overflowniveau</span><span class="sxs-lookup"><span data-stu-id="ff23c-137">Overflow Level</span></span>  
-   <span data-ttu-id="ff23c-138">Tijdsinterval</span><span class="sxs-lookup"><span data-stu-id="ff23c-138">Time Bucket</span></span>  
-   <span data-ttu-id="ff23c-139">Lotaccumulatieperiode</span><span class="sxs-lookup"><span data-stu-id="ff23c-139">Lot Accumulation Period</span></span>  
-   <span data-ttu-id="ff23c-140">Herplanningsperiode</span><span class="sxs-lookup"><span data-stu-id="ff23c-140">Rescheduling Period</span></span>  
-   <span data-ttu-id="ff23c-141">Bestelaantal</span><span class="sxs-lookup"><span data-stu-id="ff23c-141">Reorder Quantity</span></span>  
-   <span data-ttu-id="ff23c-142">Veiligheidstijd</span><span class="sxs-lookup"><span data-stu-id="ff23c-142">Safety Lead Time</span></span>  
-   <span data-ttu-id="ff23c-143">Veiligheidsvoorraad</span><span class="sxs-lookup"><span data-stu-id="ff23c-143">Safety Stock Quantity</span></span>  
-   <span data-ttu-id="ff23c-144">Assemblagebeleid</span><span class="sxs-lookup"><span data-stu-id="ff23c-144">Assembly Policy</span></span>  
-   <span data-ttu-id="ff23c-145">Productiebeleid</span><span class="sxs-lookup"><span data-stu-id="ff23c-145">Manufacturing Policy</span></span>  

<span data-ttu-id="ff23c-146">De volgende orderwijzigingen bestaan op de artikel-/SKU-kaart:</span><span class="sxs-lookup"><span data-stu-id="ff23c-146">The following order modifiers exist on the item or SKU card:</span></span>  

-   <span data-ttu-id="ff23c-147">Min. bestelaantal</span><span class="sxs-lookup"><span data-stu-id="ff23c-147">Minimum Order Quantity</span></span>  
-   <span data-ttu-id="ff23c-148">Max. bestelaantal</span><span class="sxs-lookup"><span data-stu-id="ff23c-148">Maximum Order Quantity</span></span>  
-   <span data-ttu-id="ff23c-149">Vaste lotgrootte</span><span class="sxs-lookup"><span data-stu-id="ff23c-149">Order Multiple</span></span>  

<span data-ttu-id="ff23c-150">Algemene velden voor planningsinstellingen op de pagina **Productie-instellingen** zijn onder andere:</span><span class="sxs-lookup"><span data-stu-id="ff23c-150">Global planning setup fields on the **Manufacturing Setup** page include:</span></span>  

-   <span data-ttu-id="ff23c-151">Dynamische low-levelcode</span><span class="sxs-lookup"><span data-stu-id="ff23c-151">Dynamic Low-Level Code</span></span>  
-   <span data-ttu-id="ff23c-152">Huidige vraagprognose</span><span class="sxs-lookup"><span data-stu-id="ff23c-152">Current Demand Forecast</span></span>  
-   <span data-ttu-id="ff23c-153">Prognose op vestigingen gebruiken</span><span class="sxs-lookup"><span data-stu-id="ff23c-153">Use Forecast on Locations</span></span>  
-   <span data-ttu-id="ff23c-154">Std. veiligheidstijd</span><span class="sxs-lookup"><span data-stu-id="ff23c-154">Default Safety Lead Time</span></span>  
-   <span data-ttu-id="ff23c-155">Blanco-overflowniveau</span><span class="sxs-lookup"><span data-stu-id="ff23c-155">Blank Overflow Level</span></span>  
-   <span data-ttu-id="ff23c-156">Gecombineerd MPS/MRP berek.</span><span class="sxs-lookup"><span data-stu-id="ff23c-156">Combined MPS/MRP Calculation</span></span>   
-   <span data-ttu-id="ff23c-157">Onderdelen op vestiging</span><span class="sxs-lookup"><span data-stu-id="ff23c-157">Components at Location</span></span>  
-   <span data-ttu-id="ff23c-158">Standaard dempingsperiode</span><span class="sxs-lookup"><span data-stu-id="ff23c-158">Default Dampener Period</span></span>  
-   <span data-ttu-id="ff23c-159">Demping standaardhoeveelheid</span><span class="sxs-lookup"><span data-stu-id="ff23c-159">Default Dampener Quantity</span></span>  

<span data-ttu-id="ff23c-160">Zie [Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ff23c-160">For more information, see [Design Details: Planning Parameters](design-details-planning-parameters.md)</span></span>  

## <a name="other-important-planning-fields"></a><span data-ttu-id="ff23c-161">Andere belangrijke planningsvelden</span><span class="sxs-lookup"><span data-stu-id="ff23c-161">Other Important Planning Fields</span></span>
### <a name="planning-flexibility"></a><span data-ttu-id="ff23c-162">Planningsflexibiliteit</span><span class="sxs-lookup"><span data-stu-id="ff23c-162">Planning Flexibility</span></span>
<span data-ttu-id="ff23c-163">Voor de meeste aanvulorders, bijvoorbeeld productieorders, kunt u **Ongelimiteerd** of **Geen** instellen voor het veld **Planningsflexibiliteit** op de regels.</span><span class="sxs-lookup"><span data-stu-id="ff23c-163">On most supply orders, such as production orders, you can select **Unlimited** or **None** in the **Planning Flexibility** field on the lines.</span></span>

<span data-ttu-id="ff23c-164">Zo geeft u op of het planningssysteem bij de berekening van planningsboodschappen rekening houdt met het aanbod op de productieorderregel.</span><span class="sxs-lookup"><span data-stu-id="ff23c-164">This specifies whether the supply represented by the production order line is considered by the planning system when calculating action messages.</span></span>
<span data-ttu-id="ff23c-165">Als het veld de optie **Ongelimiteerd** bevat, wordt de regel opgenomen in de berekening van planningsboodschappen.</span><span class="sxs-lookup"><span data-stu-id="ff23c-165">If the field contains **Unlimited**, then the planning system includes the line when calculating action messages.</span></span> <span data-ttu-id="ff23c-166">Als het veld de optie **Geen** bevat, is de regel vast en onveranderbaar, en wordt deze regel niet door het planningssysteem meegenomen bij de berekening van planningsboodschappen.</span><span class="sxs-lookup"><span data-stu-id="ff23c-166">If the field contains **None**, then the line is firm and unchangeable, and the planning system does not include the line when calculating action messages.</span></span>

### <a name="warning"></a><span data-ttu-id="ff23c-167">Waarschuwing</span><span class="sxs-lookup"><span data-stu-id="ff23c-167">Warning</span></span>
<span data-ttu-id="ff23c-168">Het informatieveld **Waarschuwing** op de pagina **Planningsvoorstel** biedt u informatie over elke planningsregel die voor een uitzonderlijke situatie met tekst is gemaakt. De gebruiker kan er dan voor kiezen om aanvullende informatie te lezen.</span><span class="sxs-lookup"><span data-stu-id="ff23c-168">The **Warning** information field on the **Planning Worksheet** page informs you of any planning line created for an unusual situation with a text, which the user can choose to read additional information.</span></span> <span data-ttu-id="ff23c-169">De volgende waarschuwingstypen zijn mogelijk:</span><span class="sxs-lookup"><span data-stu-id="ff23c-169">The following warning types exist:</span></span>

- <span data-ttu-id="ff23c-170">Noodgeval</span><span class="sxs-lookup"><span data-stu-id="ff23c-170">Emergency</span></span>
- <span data-ttu-id="ff23c-171">Uitzondering</span><span class="sxs-lookup"><span data-stu-id="ff23c-171">Exception</span></span>
- <span data-ttu-id="ff23c-172">Opmerking</span><span class="sxs-lookup"><span data-stu-id="ff23c-172">Attention</span></span>
- <span data-ttu-id="ff23c-173">Noodgeval</span><span class="sxs-lookup"><span data-stu-id="ff23c-173">Emergency</span></span>

<span data-ttu-id="ff23c-174">De waarschuwing Noodgeval wordt in twee gevallen weergegeven:</span><span class="sxs-lookup"><span data-stu-id="ff23c-174">The emergency warning is displayed in two situations:</span></span>

- <span data-ttu-id="ff23c-175">De voorraad is negatief op de geplande begindatum.</span><span class="sxs-lookup"><span data-stu-id="ff23c-175">The inventory is negative on the planning starting date.</span></span>
- <span data-ttu-id="ff23c-176">Er bestaan geantedateerde voorziening- of vraaggebeurtenissen.</span><span class="sxs-lookup"><span data-stu-id="ff23c-176">Back-dated supply or demand events exist.</span></span>

<span data-ttu-id="ff23c-177">Als de voorraad van een artikel negatief is op de geplande begindatum, wordt er door het planningssysteem een noodorder voor een voorziening voorgesteld die wordt aangevoerd op de geplande begindatum.</span><span class="sxs-lookup"><span data-stu-id="ff23c-177">If an item’s inventory is negative on the planning starting date, the planning system suggests an emergency supply order for the negative quantity to arrive on the planning starting date.</span></span> <span data-ttu-id="ff23c-178">De waarschuwing vermeldt de begindatum en de hoeveelheid van de order voor een noodvoorziening.</span><span class="sxs-lookup"><span data-stu-id="ff23c-178">The warning text states the starting date and the quantity of the emergency order.</span></span>

<span data-ttu-id="ff23c-179">Alle documentregels met vervaldatums voor de geplande begindatum worden samengevoegd tot één noodorder voor een voorziening voor het artikel die wordt aangevoerd op de geplande startdatum.</span><span class="sxs-lookup"><span data-stu-id="ff23c-179">Any document lines with due dates before the planning starting date are consolidated into one emergency supply order for the item to arrive on the planning starting date.</span></span>

### <a name="exception"></a><span data-ttu-id="ff23c-180">Uitzondering</span><span class="sxs-lookup"><span data-stu-id="ff23c-180">Exception</span></span>
<span data-ttu-id="ff23c-181">De uitzonderingswaarschuwing wordt weergegeven als de verwachte beschikbare voorraad onder de veiligheidsvoorraad daalt.</span><span class="sxs-lookup"><span data-stu-id="ff23c-181">The exception warning is displayed if the projected available inventory drops below the safety stock quantity.</span></span>

<span data-ttu-id="ff23c-182">Het planningssysteem stelt een order voor een voorziening voor om aan de vraag op de vervaldatum te kunnen voldoen.</span><span class="sxs-lookup"><span data-stu-id="ff23c-182">The planning system will suggest a supply order to meet the demand on its due date.</span></span> <span data-ttu-id="ff23c-183">De waarschuwing vermeldt de veiligheidsvoorraad van het artikel en de datum waarop de voorraad daaronder daalt.</span><span class="sxs-lookup"><span data-stu-id="ff23c-183">The warning text states the item’s safety stock quantity and the date on which it is violated.</span></span>

<span data-ttu-id="ff23c-184">Als de beschikbare voorraad kleiner is dan de veiligheidsvoorraad, wordt dit als een uitzondering beschouwd omdat dit normaliter niet gebeurt als het bestelpunt op de juiste manier is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="ff23c-184">Violating the safety stock level is considered an exception because it should not occur if the reorder point has been set correctly.</span></span>

> [!NOTE]
> <span data-ttu-id="ff23c-185">Voorzieningen op planningsregels met uitzonderingswaarschuwingen worden gewoonlijk niet gewijzigd volgens planningsparameters.</span><span class="sxs-lookup"><span data-stu-id="ff23c-185">Supply on planning lines with Exception warnings is normally not modified according to planning parameters.</span></span> <span data-ttu-id="ff23c-186">In plaats daarvan stelt het planningssysteem alleen een voorziening ter dekking van de hoeveelheid van de exacte vraag voor.</span><span class="sxs-lookup"><span data-stu-id="ff23c-186">Instead, the planning system only suggests a supply to cover the exact demand quantity.</span></span> <span data-ttu-id="ff23c-187">U kunt echter de uitvoering van de planning zo instellen dat bepaalde planningsparameters voor planningsregels met bepaalde waarschuwingen worden gerespecteerd.</span><span class="sxs-lookup"><span data-stu-id="ff23c-187">However, you can set the planning run up to respect certain planning parameters for planning lines with certain warnings.</span></span> <span data-ttu-id="ff23c-188">Zie Planningsparameters voor uitzonderingswaarschuwingen respecteren in Plan berekenen - Planningsvoorstel</span><span class="sxs-lookup"><span data-stu-id="ff23c-188">For more information, see “Respect Planning Parameters for Exception Warnings” in Calculate Plan - Plan.</span></span> <span data-ttu-id="ff23c-189">voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ff23c-189">Wksh.</span></span>

### <a name="attention"></a><span data-ttu-id="ff23c-190">Opmerking</span><span class="sxs-lookup"><span data-stu-id="ff23c-190">Attention</span></span>
<span data-ttu-id="ff23c-191">De waarschuwing Attentie wordt in twee gevallen weergegeven:</span><span class="sxs-lookup"><span data-stu-id="ff23c-191">The attention warning is displayed in two situations:</span></span>

- <span data-ttu-id="ff23c-192">De geplande begindatum is eerder dan de werkdatum.</span><span class="sxs-lookup"><span data-stu-id="ff23c-192">The planning starting date is earlier than the work date.</span></span>
- <span data-ttu-id="ff23c-193">Op de planningsregel wordt voorgesteld een vrijgegeven inkoop- of productieorder te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="ff23c-193">The planning line suggests to change a released purchase or production order.</span></span>

> [!NOTE]
> <span data-ttu-id="ff23c-194">bij het plannen van regels met waarschuwingen wordt het veld **Planningsboodschap accepteren** niet geselecteerd, omdat de planner naar verwachting de regels verder gaat bekijken voordat de planning wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ff23c-194">In planning lines with warnings, the **Accept Action Message** field is not selected, because the planner is expected to further investigate these lines before carrying out the plan.</span></span>

## <a name="see-also"></a><span data-ttu-id="ff23c-195">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ff23c-195">See Also</span></span>  
[<span data-ttu-id="ff23c-196">Ontwerpdetails: Voorzieningsplanning</span><span class="sxs-lookup"><span data-stu-id="ff23c-196">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)  
<span data-ttu-id="ff23c-197">[Gepland](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="ff23c-197">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="ff23c-198">Productie instellen</span><span class="sxs-lookup"><span data-stu-id="ff23c-198">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="ff23c-199">[Productie](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="ff23c-199">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="ff23c-200">Voorraad</span><span class="sxs-lookup"><span data-stu-id="ff23c-200">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="ff23c-201">Inkoop</span><span class="sxs-lookup"><span data-stu-id="ff23c-201">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="ff23c-202">Aanbevolen procedures instellen: voorraadplanning</span><span class="sxs-lookup"><span data-stu-id="ff23c-202">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="ff23c-203">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ff23c-203">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
