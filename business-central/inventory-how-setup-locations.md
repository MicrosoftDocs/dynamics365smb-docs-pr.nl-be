---
title: Een vestigingskaart instellen en transferroutes definiëren
description: U maakt een vestigingskaart voor elke plaats waar u voorraadartikelen opslaat, bijvoorbeeld een magazijn of een distributiecentrum, en u stelt routes in om artikelen tussen vestigingen over te brengen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/01/2021
ms.author: edupont
ms.openlocfilehash: 0319f0c64dd46610aa82705257091bd9478ac14f
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184336"
---
# <a name="set-up-locations"></a><span data-ttu-id="fe039-103">Vestigingen instellen</span><span class="sxs-lookup"><span data-stu-id="fe039-103">Set Up Locations</span></span>

<span data-ttu-id="fe039-104">Als u artikelen op meer dan één plaats of magazijn koopt, opslaat of verkoopt, moet u elke vestiging instellen met een vestigingskaart en transferroutes definiëren.</span><span class="sxs-lookup"><span data-stu-id="fe039-104">If you buy, store, or sell items at more than one place or warehouse, you must set up each location with a location card and define transfer routes.</span></span> <span data-ttu-id="fe039-105">[!INCLUDE [prod_short](includes/prod_short.md)] gebruikt vestigingen om de voorraad bij te houden in zowel eenvoudigere gevallen als de meer complexe magazijnprocessen.</span><span class="sxs-lookup"><span data-stu-id="fe039-105">[!INCLUDE [prod_short](includes/prod_short.md)] uses locations to help keep track of inventory in both simpler cases and the more complex warehouse processes.</span></span>

<span data-ttu-id="fe039-106">U kunt vervolgens documentregels voor een bepaalde vestiging maken, beschikbaarheid per locatie weergeven en voorraad tussen locaties overbrengen.</span><span class="sxs-lookup"><span data-stu-id="fe039-106">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="fe039-107">Zie [Voorraad beheren](inventory-manage-inventory.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="fe039-107">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a><span data-ttu-id="fe039-108">Vestigingskaarten</span><span class="sxs-lookup"><span data-stu-id="fe039-108">Location cards</span></span>

<span data-ttu-id="fe039-109">Op de vestigingskaart staat informatie over een vestiging, zoals een magazijn of distributiecentrum.</span><span class="sxs-lookup"><span data-stu-id="fe039-109">The location card specifies information about a location, such as a warehouse or distribution center.</span></span> <span data-ttu-id="fe039-110">U wijst aan elke vestiging een naam toe en een code die de vestiging vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="fe039-110">You give each location a name and a code that represents the location.</span></span> <span data-ttu-id="fe039-111">U kunt de vestigingscode in andere delen van het programma invoeren om transacties voor een bepaalde vestiging vast te leggen.</span><span class="sxs-lookup"><span data-stu-id="fe039-111">You can then enter the location code in other parts of the program when you want to record transactions for a given location.</span></span>  

<span data-ttu-id="fe039-112">U kunt informatie invoeren over opslaglocaties en magazijnbeleid voor elke vestiging.</span><span class="sxs-lookup"><span data-stu-id="fe039-112">You can enter information about bins and warehouse policies for each location.</span></span> <span data-ttu-id="fe039-113">Op basis van het geselecteerde magazijnbeleid gebruikt u de opties op het sneltabblad **Opslaglocaties** om de opslaglocaties te definiëren die als standaardopslaglocaties worden gebruikt wanneer u transacties uitvoert.</span><span class="sxs-lookup"><span data-stu-id="fe039-113">Based on the warehouse policies you select, you can use the options on the **Bins** FastTab to define the bins that will be used as default bins when you are performing transactions.</span></span> <span data-ttu-id="fe039-114">Als u gestuurde opslag en pick gebruikt, gebruikt u de meeste opties op het sneltabblad **Opslaglocatiebeleid** om te definiëren hoe u de verschillende magazijnfuncties wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="fe039-114">If you are using directed put-away and pick, you use most of the options on the **Bin Policies** FastTab to define how you would like to use the various advanced warehousing features.</span></span>  

<span data-ttu-id="fe039-115">Sommige optievelden zijn niet beschikbaar en uitgeschakeld door andere instellingen op de pagina **Vestigingskaart** om niet-ondersteunde combinaties te beperken.</span><span class="sxs-lookup"><span data-stu-id="fe039-115">Some option fields are grayed and disabled by other settings in the **Location Card** page to restrict unsupported setup combinations.</span></span>  

<span data-ttu-id="fe039-116">Kies de actie **Zones** of **Opslaglocaties** voor informatie over zones en opslaglocaties die zijn gedefinieerd voor de vestiging.</span><span class="sxs-lookup"><span data-stu-id="fe039-116">Choose the **Zones** or **Bins** action to view information about zones and bins that may be defined for the location.</span></span>

### <a name="to-create-a-location-card"></a><span data-ttu-id="fe039-117">Een vestigingskaart maken</span><span class="sxs-lookup"><span data-stu-id="fe039-117">To create a location card</span></span>

1. <span data-ttu-id="fe039-118">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vestigingen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="fe039-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="fe039-119">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="fe039-119">Choose the **New** action.</span></span>
3. <span data-ttu-id="fe039-120">Vul indien nodig de velden op de pagina **Vestiging** in.</span><span class="sxs-lookup"><span data-stu-id="fe039-120">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="fe039-121">Herhaal stap 2 en 3 voor elke locatie waar u voorraad wilt houden.</span><span class="sxs-lookup"><span data-stu-id="fe039-121">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="fe039-122">Veel velden op de vestigingskaart verwijzen naar de verwerking van artikelen in inkomende en uitgaande magazijnprocessen.</span><span class="sxs-lookup"><span data-stu-id="fe039-122">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="fe039-123">De velden zijn niet relevant voor bedrijven die de meer complexe magazijnfunctionaliteit niet nodig hebben.</span><span class="sxs-lookup"><span data-stu-id="fe039-123">The fields are not relevant for companies that do not require the more complex warehouse functionality.</span></span> <span data-ttu-id="fe039-124">Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="fe039-124">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

<span data-ttu-id="fe039-125">U kunt de configuratie van een vestiging later wijzigen, maar u kunt de instellingen van vestigingen met artikelposten niet bewerken.</span><span class="sxs-lookup"><span data-stu-id="fe039-125">You can change the configuration of a location later, but you cannot edit the setup of locations that have item ledger entries.</span></span>  

<span data-ttu-id="fe039-126">Als u meerdere vestigingen heeft, kunt u vervolgens transferroutes tussen vestigingen definiëren.</span><span class="sxs-lookup"><span data-stu-id="fe039-126">Next, if you have multiple locations, you can define transfer routes between locations.</span></span>  

### <a name="to-create-a-transfer-route"></a><span data-ttu-id="fe039-127">Een transferroute maken</span><span class="sxs-lookup"><span data-stu-id="fe039-127">To create a transfer route</span></span>

1. <span data-ttu-id="fe039-128">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Transferroutes** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="fe039-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="fe039-129">U kunt ook vanuit elke **Vestiging**-pagina de actie **Transferroutes** kiezen.</span><span class="sxs-lookup"><span data-stu-id="fe039-129">Alternatively, from any **Location Card** page, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="fe039-130">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="fe039-130">Choose the **New** action.</span></span>
4. <span data-ttu-id="fe039-131">Vul indien nodig de velden op de pagina **Vestiging** in.</span><span class="sxs-lookup"><span data-stu-id="fe039-131">On the **Location Card** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="fe039-132">U kunt nu voorraadartikelen tussen twee vestigingen overbrengen.</span><span class="sxs-lookup"><span data-stu-id="fe039-132">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="fe039-133">Zie voor meer informatie [Voorraad overbrengen tussen vestigingen](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="fe039-133">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="bins"></a><span data-ttu-id="fe039-134">Opslaglocaties</span><span class="sxs-lookup"><span data-stu-id="fe039-134">Bins</span></span>

<span data-ttu-id="fe039-135">Opslaglocaties vertegenwoordigen de standaard magazijnstructuur en worden gebruikt voor het doen van voorstellen over de plaatsing van artikelen.</span><span class="sxs-lookup"><span data-stu-id="fe039-135">Bins represent the basic warehouse structure and are used to make suggestions about the placement of items.</span></span> <span data-ttu-id="fe039-136">Wanneer u uw opslaglocaties hebt gemaakt, kunt u de inhoud die u in de afzonderlijke opslaglocaties wilt plaatsen precies definiëren. De opslaglocatie kan echter ook functioneren als een vrije opslaglocatie zonder opgegeven inhoud.</span><span class="sxs-lookup"><span data-stu-id="fe039-136">When you have created your bins, you can define precisely the contents that you want to place in each bin, or the bin can function as a floating bin without specified contents.</span></span> <span data-ttu-id="fe039-137">Opslaglocaties worden voornamelijk gebruikt in basis- en geavanceerde magazijnactiviteiten.</span><span class="sxs-lookup"><span data-stu-id="fe039-137">Bins are predominantly used in basic and advance warehouse operations.</span></span> <span data-ttu-id="fe039-138">Als u voorraad op een eenvoudigere manier beheert, heeft u waarschijnlijk geen opslaglocaties nodig.</span><span class="sxs-lookup"><span data-stu-id="fe039-138">If you manage inventory in a more simple setup, you probably do not need bins.</span></span>

<span data-ttu-id="fe039-139">Om de opslaglocatiefunctionaliteit op een vestiging te gebruiken, activeert u eerst de functionaliteit op de **vestigingskaart** door het veld **Opslaglocatie verplicht** op het sneltabblad **Magazijn** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="fe039-139">To use the bin functionality at a location, you first activate the functionality on the **Location** card by selecting the **Bins Mandatory** field on the **Warehouse** FastTab.</span></span> <span data-ttu-id="fe039-140">U ontwerpt vervolgens de artikelstroom op de locatie door de opslaglocatiecodes op te geven in de instellingsvelden voor de verschillende stromen.</span><span class="sxs-lookup"><span data-stu-id="fe039-140">Then you design the item flow at the location by specifying bin codes in setup fields that represent the different flows.</span></span>

> [!NOTE]
> <span data-ttu-id="fe039-141">Voordat u opslaglocatiecodes op de vestigingskaart kunt opgeven, moeten de opslaglocatiecodes worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fe039-141">Before you can specify bin codes on the location card, the bin codes must be created.</span></span>

<span data-ttu-id="fe039-142">Zie [Opslaglocaties maken](warehouse-how-to-create-individual-bins.md) en [Opslaglocatiesoorten instellen](warehouse-how-to-set-up-bin-types.md).</span><span class="sxs-lookup"><span data-stu-id="fe039-142">For more information, see [Create Bins](warehouse-how-to-create-individual-bins.md) and [Set Up Bin Types](warehouse-how-to-set-up-bin-types.md).</span></span>  

## <a name="zones"></a><span data-ttu-id="fe039-143">Zones</span><span class="sxs-lookup"><span data-stu-id="fe039-143">Zones</span></span>

<span data-ttu-id="fe039-144">Als u uw opslaglocaties onder zones wilt structureren, kunt u dat doen op de pagina **Zones**.</span><span class="sxs-lookup"><span data-stu-id="fe039-144">If you want to structure your bins under zones, you can do that in the **Zones** page.</span></span>

<span data-ttu-id="fe039-145">[!INCLUDE [prod_short](includes/prod_short.md)] kopieert de velden die u voor een bepaalde zone instelt, naar de opslaglocaties erin.</span><span class="sxs-lookup"><span data-stu-id="fe039-145">[!INCLUDE [prod_short](includes/prod_short.md)] copies the fields that you set for any particular zone to the bins within it.</span></span> <span data-ttu-id="fe039-146">Op deze manier kunt u een zone toewijzen aan een opslaglocatie of een opslaglocatiesjabloon (filter voor het maken van opslaglocaties), worden diverse andere velden automatisch ingevuld.</span><span class="sxs-lookup"><span data-stu-id="fe039-146">This way, you can assign a zone to a bin or a bin template (bin creation filter), and several other fields are then filled in automatically.</span></span>

<span data-ttu-id="fe039-147">U kunt echter ook slechts één zone instellen en uw magazijn indelen op basis van alleen de opslaglocaties.</span><span class="sxs-lookup"><span data-stu-id="fe039-147">However, you can choose to set up just one zone and to organize your warehouse according to bins alone.</span></span> <span data-ttu-id="fe039-148">Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="fe039-148">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="fe039-149">Zie ook</span><span class="sxs-lookup"><span data-stu-id="fe039-149">See Also</span></span>

[<span data-ttu-id="fe039-150">Voorraad beheren</span><span class="sxs-lookup"><span data-stu-id="fe039-150">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="fe039-151">Voorraad overbrengen tussen vestigingen</span><span class="sxs-lookup"><span data-stu-id="fe039-151">Transfer Inventory Between Locations</span></span>](inventory-how-transfer-between-locations.md)  
[<span data-ttu-id="fe039-152">Opslaglocaties maken</span><span class="sxs-lookup"><span data-stu-id="fe039-152">Create Bins</span></span>](warehouse-how-to-create-individual-bins.md)  
[<span data-ttu-id="fe039-153">Opslaglocatiesoorten instellen</span><span class="sxs-lookup"><span data-stu-id="fe039-153">Set Up Bin Types</span></span>](warehouse-how-to-set-up-bin-types.md)  
[<span data-ttu-id="fe039-154">Magazijnbeheer instellen</span><span class="sxs-lookup"><span data-stu-id="fe039-154">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
<span data-ttu-id="fe039-155">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fe039-155">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="fe039-156">Wijzigen welke functies worden weergegeven</span><span class="sxs-lookup"><span data-stu-id="fe039-156">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="fe039-157">Algemene bedrijfsfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="fe039-157">General Business Functionality</span></span>](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]