---
title: Picken en verzenden in standaardmagazijnconfiguraties
description: In Business Central kunnen uitgaande processen voor picken en verzending op vier manieren worden uitgevoerd met verschillende functionaliteiten afhankelijk van het complexiteitsniveau van het magazijn.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: e1763e6288c8b8218955049ba7ef4c461ee5164e
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214665"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a><span data-ttu-id="7fee0-103">Procedure: picken en verzenden in standaardmagazijnconfiguraties</span><span class="sxs-lookup"><span data-stu-id="7fee0-103">Walkthrough: Picking and Shipping in Basic Warehouse Configurations</span></span>

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)] -->

<span data-ttu-id="7fee0-104">In [!INCLUDE[prod_short](includes/prod_short.md)] kunnen uitgaande processen voor picken en verzending op vier manieren worden uitgevoerd met verschillende functionaliteiten afhankelijk van het complexiteitsniveau van het magazijn.</span><span class="sxs-lookup"><span data-stu-id="7fee0-104">In [!INCLUDE[prod_short](includes/prod_short.md)], the outbound processes for picking and shipping can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="7fee0-105">Methode</span><span class="sxs-lookup"><span data-stu-id="7fee0-105">Method</span></span>|<span data-ttu-id="7fee0-106">Inkomend proces</span><span class="sxs-lookup"><span data-stu-id="7fee0-106">Inbound process</span></span>|<span data-ttu-id="7fee0-107">Opslaglocaties</span><span class="sxs-lookup"><span data-stu-id="7fee0-107">Bins</span></span>|<span data-ttu-id="7fee0-108">Magazijnpicks</span><span class="sxs-lookup"><span data-stu-id="7fee0-108">Picks</span></span>|<span data-ttu-id="7fee0-109">Verzendingen</span><span class="sxs-lookup"><span data-stu-id="7fee0-109">Shipments</span></span>|<span data-ttu-id="7fee0-110">Complexiteitsniveau (zie [Ontwerpdetails: Magazijninstelling](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="7fee0-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="7fee0-111">A</span><span class="sxs-lookup"><span data-stu-id="7fee0-111">A</span></span>|<span data-ttu-id="7fee0-112">Picken en verzending van de orderregel boeken</span><span class="sxs-lookup"><span data-stu-id="7fee0-112">Post pick and shipment from the order line</span></span>|<span data-ttu-id="7fee0-113">X</span><span class="sxs-lookup"><span data-stu-id="7fee0-113">X</span></span>|||<span data-ttu-id="7fee0-114">2</span><span class="sxs-lookup"><span data-stu-id="7fee0-114">2</span></span>|  
|<span data-ttu-id="7fee0-115">B</span><span class="sxs-lookup"><span data-stu-id="7fee0-115">B</span></span>|<span data-ttu-id="7fee0-116">Picken en verzending van een voorraadpickdocument boeken</span><span class="sxs-lookup"><span data-stu-id="7fee0-116">Post pick and shipment from an inventory pick document</span></span>||<span data-ttu-id="7fee0-117">X</span><span class="sxs-lookup"><span data-stu-id="7fee0-117">X</span></span>||<span data-ttu-id="7fee0-118">3</span><span class="sxs-lookup"><span data-stu-id="7fee0-118">3</span></span>|  
|<span data-ttu-id="7fee0-119">L</span><span class="sxs-lookup"><span data-stu-id="7fee0-119">C</span></span>|<span data-ttu-id="7fee0-120">Picken en verzending van een magazijnverzendingdocument boeken</span><span class="sxs-lookup"><span data-stu-id="7fee0-120">Post pick and shipment from a warehouse shipment document</span></span>|||<span data-ttu-id="7fee0-121">X</span><span class="sxs-lookup"><span data-stu-id="7fee0-121">X</span></span>|<span data-ttu-id="7fee0-122">5-4-6</span><span class="sxs-lookup"><span data-stu-id="7fee0-122">4/5/6</span></span>|  
|<span data-ttu-id="7fee0-123">D</span><span class="sxs-lookup"><span data-stu-id="7fee0-123">D</span></span>|<span data-ttu-id="7fee0-124">Picken van een magazijnpickdocument en verzending van een magazijnverzendingdocument boeken</span><span class="sxs-lookup"><span data-stu-id="7fee0-124">Post pick from a warehouse pick document and post shipment from a warehouse shipment document</span></span>||<span data-ttu-id="7fee0-125">X</span><span class="sxs-lookup"><span data-stu-id="7fee0-125">X</span></span>|<span data-ttu-id="7fee0-126">X</span><span class="sxs-lookup"><span data-stu-id="7fee0-126">X</span></span>|<span data-ttu-id="7fee0-127">5-4-6</span><span class="sxs-lookup"><span data-stu-id="7fee0-127">4/5/6</span></span>|  

<span data-ttu-id="7fee0-128">Zie voor meer informatie [Ontwerpdetails: Uitgaande magazijnstroom](design-details-outbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="7fee0-128">For more information, see [Design Details: Outbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="7fee0-129">De volgende procedure geeft methode B in de vorige tabel weer.</span><span class="sxs-lookup"><span data-stu-id="7fee0-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="7fee0-130">Informatie over deze procedure</span><span class="sxs-lookup"><span data-stu-id="7fee0-130">About This Walkthrough</span></span>

<span data-ttu-id="7fee0-131">In standaardmagazijnconfiguraties waarbij voor uw vestiging wel een pickverwerking vereist is, maar geen verzendingsverwerking, gebruikt u de pagina **Voorraadpick** om pick- en verzendingsinformatie voor de uitgaande brondocumenten te verzamelen en boeken.</span><span class="sxs-lookup"><span data-stu-id="7fee0-131">In basic warehouse configurations where your location is set up to require pick processing but not ship processing, you use the **Inventory Pick** page to record and post pick and ship information for your outbound source documents.</span></span> <span data-ttu-id="7fee0-132">Het uitgaand brondocument kan een verkooporder zijn, maar ook een inkoopretourorder, een uitgaande transferorder of een productieorder met daarop de materiaalbehoefte.</span><span class="sxs-lookup"><span data-stu-id="7fee0-132">The outbound source document can be a sales order, purchase return order, outbound transfer order, or a production order with component need.</span></span>  

<span data-ttu-id="7fee0-133">In deze procedure worden de volgende taken gedemonstreerd:</span><span class="sxs-lookup"><span data-stu-id="7fee0-133">This walkthrough demonstrates the following tasks:</span></span>  

- <span data-ttu-id="7fee0-134">Locatie ZUID instellen voor voorraadpicks.</span><span class="sxs-lookup"><span data-stu-id="7fee0-134">Setting up SOUTH location for inventory picks.</span></span>  
- <span data-ttu-id="7fee0-135">Maak een verkooporder voor klant 10000 voor 30 lampen.</span><span class="sxs-lookup"><span data-stu-id="7fee0-135">Creating a sales order for customer 10000 for 30 Amsterdam Lamps.</span></span>  
- <span data-ttu-id="7fee0-136">De verkooporder vrijgeven voor magazijnverwerking.</span><span class="sxs-lookup"><span data-stu-id="7fee0-136">Releasing the sales order for warehouse handling.</span></span>  
- <span data-ttu-id="7fee0-137">Een voorraadpick maken op basis van een vrijgegeven brondocument.</span><span class="sxs-lookup"><span data-stu-id="7fee0-137">Creating an inventory pick based on a released source document.</span></span>  
- <span data-ttu-id="7fee0-138">De magazijnverplaatsing van het magazijn vastleggen en tegelijkertijd de verkoopverzending voor de bronverkooporder boeken.</span><span class="sxs-lookup"><span data-stu-id="7fee0-138">Registering the warehouse movement from the warehouse and at the same time posting the sales shipment for the source sales order.</span></span>  

## <a name="roles"></a><span data-ttu-id="7fee0-139">Rollen</span><span class="sxs-lookup"><span data-stu-id="7fee0-139">Roles</span></span>

<span data-ttu-id="7fee0-140">In dit overzicht worden taken gedemonstreerd voor de volgende gebruikersrollen:</span><span class="sxs-lookup"><span data-stu-id="7fee0-140">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

- <span data-ttu-id="7fee0-141">Magazijnbeheerder</span><span class="sxs-lookup"><span data-stu-id="7fee0-141">Warehouse Manager</span></span>  
- <span data-ttu-id="7fee0-142">Orderverwerker</span><span class="sxs-lookup"><span data-stu-id="7fee0-142">Order Processor</span></span>  
- <span data-ttu-id="7fee0-143">Magazijnmedewerker</span><span class="sxs-lookup"><span data-stu-id="7fee0-143">Warehouse Worker</span></span>  

<!-- ## Prerequisites

To complete this walkthrough, you will need:  

- For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS installed.
 -->

## <a name="story"></a><span data-ttu-id="7fee0-144">Scenario</span><span class="sxs-lookup"><span data-stu-id="7fee0-144">Story</span></span>

<span data-ttu-id="7fee0-145">Ellen, de magazijnmanager bij CRONUS, stelt magazijn ZUID in voor basispickverwerking waarbij magazijnmedewerkers uitgaande orders afzonderlijk verwerken.</span><span class="sxs-lookup"><span data-stu-id="7fee0-145">Ellen, the warehouse manager at CRONUS, sets up SOUTH warehouse for basic pick handling where warehouse workers process outbound orders individually.</span></span> <span data-ttu-id="7fee0-146">De orderverwerker Suzanne maakt een verkooporder voor 30 eenheden van het artikel 1928-S om aan klant 10000 vanuit het magazijn ZUID te worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="7fee0-146">Susan, the order processor, creates a sales order for 30 units of item 1928-S to be shipped to customer 10000 from the SOUTH Warehouse.</span></span> <span data-ttu-id="7fee0-147">De magazijnmedewerker John zorgt ervoor dat de verzending wordt voorbereid en aan de klant geleverd.</span><span class="sxs-lookup"><span data-stu-id="7fee0-147">John, the warehouse worker must make sure that the shipment is prepared and delivered to the customer.</span></span> <span data-ttu-id="7fee0-148">John beheert alle betrokken taken op de pagina **Voorraadpick**, die automatisch verwijst naar de opslaglocaties waar 1928-S is opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="7fee0-148">John manages all involved tasks on the **Inventory Pick** page, which automatically points to the bins where 1928-S is stored.</span></span>

[!INCLUDE[set_up_location.md](includes/set_up_location.md)]

### <a name="setting-up-the-bin-codes"></a><span data-ttu-id="7fee0-149">De opslaglocatiecodes instellen</span><span class="sxs-lookup"><span data-stu-id="7fee0-149">Setting Up the Bin Codes</span></span>
<span data-ttu-id="7fee0-150">Nadat u de locatie hebt ingesteld, moet u twee opslaglocaties toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7fee0-150">Once you have the location set up, you must add two bins.</span></span>

#### <a name="to-setup-the-bin-codes"></a><span data-ttu-id="7fee0-151">De opslaglocatiecodes instellen</span><span class="sxs-lookup"><span data-stu-id="7fee0-151">To setup the bin codes</span></span>

1. <span data-ttu-id="7fee0-152">Selecteer de acties **Opslaglocaties**.</span><span class="sxs-lookup"><span data-stu-id="7fee0-152">Select the **Bins** action.</span></span>
2. <span data-ttu-id="7fee0-153">Maak twee opslaglocaties met de codes *S-01-0001* en *S-01-0002*.</span><span class="sxs-lookup"><span data-stu-id="7fee0-153">Create two bins, with the codes *S-01-0001* and *S-01-0002*.</span></span>

### <a name="making-yourself-a-warehouse-employee-at-location-south"></a><span data-ttu-id="7fee0-154">Uzelf magazijnmedewerker maken op locatie ZUID</span><span class="sxs-lookup"><span data-stu-id="7fee0-154">Making Yourself a Warehouse Employee at Location SOUTH</span></span>

<span data-ttu-id="7fee0-155">Om van deze functionaliteit gebruik te kunnen maken, moet u zichzelf als magazijnmedewerker toevoegen aan de locatie.</span><span class="sxs-lookup"><span data-stu-id="7fee0-155">In order to use this functionality, you must add yourself to the location as a warehouse worker.</span></span> 

#### <a name="to-make-yourself-a-warehouse-employee"></a><span data-ttu-id="7fee0-156">Uzelf magazijnmedewerker maken</span><span class="sxs-lookup"><span data-stu-id="7fee0-156">To make yourself a warehouse employee</span></span>

  1. <span data-ttu-id="7fee0-157">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnmedewerkers** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="7fee0-157">Choose the ![Lightbulb that opens the Tell Me feature first](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="7fee0-158">Kies het veld **Gebruikers-ID** en selecteer uw eigen gebruikersaccount op de pagina **Magazijnmedewerkers**.</span><span class="sxs-lookup"><span data-stu-id="7fee0-158">Choose the **User ID** field, and select your own user account on the **Warehouse Employees** page.</span></span>
  3. <span data-ttu-id="7fee0-159">Kies ZUID in het veld **Vestiging**.</span><span class="sxs-lookup"><span data-stu-id="7fee0-159">In the **Location Code** field, choose SOUTH.</span></span>  
  4. <span data-ttu-id="7fee0-160">Selecteer het veld **Standaard** en selecteer vervolgens de knop **Ja**.</span><span class="sxs-lookup"><span data-stu-id="7fee0-160">Select the **Default** field, and then select the **Yes** button.</span></span>  

### <a name="making-item-1928-s-available"></a><span data-ttu-id="7fee0-161">Artikel 1928-S beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="7fee0-161">Making Item 1928-S Available</span></span>

<span data-ttu-id="7fee0-162">Als u artikel 1928-S op locatie ZUID beschikbaar wilt maken, volgt u deze stappen:</span><span class="sxs-lookup"><span data-stu-id="7fee0-162">To make item 1928-S available at the SOUTH location follow these steps:</span></span>  

  1. <span data-ttu-id="7fee0-163">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikeldagboeken** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="7fee0-163">Choose the ![Lightbulb that opens the Tell Me feature second](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Journals**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="7fee0-164">Open het standaarddagboek en maak twee artikeldagboekregels met de volgende informatie over de werkdatum (23 januari).</span><span class="sxs-lookup"><span data-stu-id="7fee0-164">Open the default journal, and then create two item journal lines with the following information about the work date (January 23).</span></span>  

        |<span data-ttu-id="7fee0-165">Boekingssoort</span><span class="sxs-lookup"><span data-stu-id="7fee0-165">Entry Type</span></span>|<span data-ttu-id="7fee0-166">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="7fee0-166">Item Number</span></span>|<span data-ttu-id="7fee0-167">Vestiging</span><span class="sxs-lookup"><span data-stu-id="7fee0-167">Location Code</span></span>|<span data-ttu-id="7fee0-168">Opslaglocatie</span><span class="sxs-lookup"><span data-stu-id="7fee0-168">Bin Code</span></span>|<span data-ttu-id="7fee0-169">Aantal</span><span class="sxs-lookup"><span data-stu-id="7fee0-169">Quantity</span></span>|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |<span data-ttu-id="7fee0-170">Pos. correctie</span><span class="sxs-lookup"><span data-stu-id="7fee0-170">Positive Adjmt.</span></span>|<span data-ttu-id="7fee0-171">1928-S</span><span class="sxs-lookup"><span data-stu-id="7fee0-171">1928-S</span></span>|<span data-ttu-id="7fee0-172">ZUID</span><span class="sxs-lookup"><span data-stu-id="7fee0-172">SOUTH</span></span>|<span data-ttu-id="7fee0-173">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="7fee0-173">S-01-0001</span></span>|<span data-ttu-id="7fee0-174">20</span><span class="sxs-lookup"><span data-stu-id="7fee0-174">20</span></span>|  
        |<span data-ttu-id="7fee0-175">Pos. correctie</span><span class="sxs-lookup"><span data-stu-id="7fee0-175">Positive Adjmt.</span></span>|<span data-ttu-id="7fee0-176">1928-S</span><span class="sxs-lookup"><span data-stu-id="7fee0-176">1928-S</span></span>|<span data-ttu-id="7fee0-177">ZUID</span><span class="sxs-lookup"><span data-stu-id="7fee0-177">SOUTH</span></span>|<span data-ttu-id="7fee0-178">S-01-0002</span><span class="sxs-lookup"><span data-stu-id="7fee0-178">S-01-0002</span></span>|<span data-ttu-id="7fee0-179">20</span><span class="sxs-lookup"><span data-stu-id="7fee0-179">20</span></span>|  

        <span data-ttu-id="7fee0-180">Standaard is het veld **Opslaglocatie** op de verkoopregels verborgen, dus u moet het weergeven.</span><span class="sxs-lookup"><span data-stu-id="7fee0-180">By default, the **Bin Code** field on the sales lines are hidden, so you must display it.</span></span> <span data-ttu-id="7fee0-181">Hiervoor moet u de pagina personaliseren.</span><span class="sxs-lookup"><span data-stu-id="7fee0-181">To do this you need to personalize the page.</span></span> <span data-ttu-id="7fee0-182">Zie voor meer informatie [Een pagina personaliseren via de banner Personaliseren](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).</span><span class="sxs-lookup"><span data-stu-id="7fee0-182">For more information, see [To start personalizing a page through the Personalizing banner](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).</span></span>

  3. <span data-ttu-id="7fee0-183">Kies **Acties**, vervolgens **Boeking** en kies vervolgens **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="7fee0-183">Choose **Actions**, then **Posting**, and then choose **Post**.</span></span>  
  4. <span data-ttu-id="7fee0-184">Selecteer de knop **Ja**.</span><span class="sxs-lookup"><span data-stu-id="7fee0-184">Select the **Yes** button.</span></span>  

## <a name="creating-the-sales-order"></a><span data-ttu-id="7fee0-185">De verkooporder maken</span><span class="sxs-lookup"><span data-stu-id="7fee0-185">Creating the Sales Order</span></span>

<span data-ttu-id="7fee0-186">Verkooporders zijn de meest gebruikte soort uitgaand brondocument.</span><span class="sxs-lookup"><span data-stu-id="7fee0-186">Sales orders are the most common type of outbound source document.</span></span>  

### <a name="to-create-the-sales-order"></a><span data-ttu-id="7fee0-187">De verkooporder maken</span><span class="sxs-lookup"><span data-stu-id="7fee0-187">To create the sales order</span></span>

1. <span data-ttu-id="7fee0-188">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="7fee0-188">Choose the ![Lightbulb that opens the Tell Me feature third](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7fee0-189">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="7fee0-189">Choose the **New** action.</span></span>  
3. <span data-ttu-id="7fee0-190">Maak een verkooporder voor klant 10000 op 23 januari (werkdatum) met de volgende verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="7fee0-190">Create a sales order for customer 10000 on the work date (January 23) with the following sales order line.</span></span>  

    |<span data-ttu-id="7fee0-191">Artikel</span><span class="sxs-lookup"><span data-stu-id="7fee0-191">Item</span></span>|<span data-ttu-id="7fee0-192">Vestiging</span><span class="sxs-lookup"><span data-stu-id="7fee0-192">Location Code</span></span>|<span data-ttu-id="7fee0-193">Aantal</span><span class="sxs-lookup"><span data-stu-id="7fee0-193">Quantity</span></span>|  
    |----|-------------|--------|  
    |<span data-ttu-id="7fee0-194">1928-S</span><span class="sxs-lookup"><span data-stu-id="7fee0-194">1928-S</span></span>|<span data-ttu-id="7fee0-195">ZUID</span><span class="sxs-lookup"><span data-stu-id="7fee0-195">SOUTH</span></span>|<span data-ttu-id="7fee0-196">30</span><span class="sxs-lookup"><span data-stu-id="7fee0-196">30</span></span>|  

     <span data-ttu-id="7fee0-197">Ga door om het magazijn te informeren dat de verkooporder klaar is voor magazijnverwerking.</span><span class="sxs-lookup"><span data-stu-id="7fee0-197">Proceed to notify the warehouse that the sales order is ready for warehouse handling.</span></span>  

4. <span data-ttu-id="7fee0-198">Kies de actie **Vrijgeven**.</span><span class="sxs-lookup"><span data-stu-id="7fee0-198">Choose the **Release** action.</span></span>  

    <span data-ttu-id="7fee0-199">John gaat door met het picken en verzenden van de verkochte artikelen.</span><span class="sxs-lookup"><span data-stu-id="7fee0-199">John proceeds to pick and ship the sold items.</span></span>  

## <a name="picking-and-shipping-items"></a><span data-ttu-id="7fee0-200">Artikelen picken en verzenden</span><span class="sxs-lookup"><span data-stu-id="7fee0-200">Picking and Shipping Items</span></span>

<span data-ttu-id="7fee0-201">Op de pagina **Voorraadpick** kunt u alle uitgaande magazijnactiviteiten voor een bepaald brondocument, zoals een verkooporder, beheren.</span><span class="sxs-lookup"><span data-stu-id="7fee0-201">On the **Inventory Pick** page, you can manage all outbound warehouse activities for a specific source document, such as a sales order.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a><span data-ttu-id="7fee0-202">U kunt als volgt artikels picken en verzenden</span><span class="sxs-lookup"><span data-stu-id="7fee0-202">To pick and ship items</span></span>

1. <span data-ttu-id="7fee0-203">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraadpicks** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="7fee0-203">Choose the ![Lightbulb that opens the Tell Me feature fourth](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Picks**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7fee0-204">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="7fee0-204">Choose the **New** action.</span></span>  

    <span data-ttu-id="7fee0-205">Zorg ervoor dat het veld **Nee.**</span><span class="sxs-lookup"><span data-stu-id="7fee0-205">Make sure that the **No.**</span></span> <span data-ttu-id="7fee0-206">op het sneltabblad **Algemeen** is ingevuld.</span><span class="sxs-lookup"><span data-stu-id="7fee0-206">field on the **General** FastTab is filled in.</span></span>
3. <span data-ttu-id="7fee0-207">Selecteer het veld **Brondocument** en selecteer vervolgens **Verkooporder**.</span><span class="sxs-lookup"><span data-stu-id="7fee0-207">Select the **Source Document** field, and then select **Sales Order**.</span></span>  
4. <span data-ttu-id="7fee0-208">Selecteer het veld **Bronnr.**, selecteer de regel voor de verkoop aan klant 10000, en kies vervolgens de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fee0-208">Select the **Source No.** field, select the line for the sale to customer 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="7fee0-209">U kunt ook de actie **Brondocument ophalen** kiezen en de verkooporder kiezen.</span><span class="sxs-lookup"><span data-stu-id="7fee0-209">Alternatively, choose the **Get Source Document** action, and then select the sales order.</span></span>  
5. <span data-ttu-id="7fee0-210">Kies de actie **Te verwerken aantal autom. invullen**.</span><span class="sxs-lookup"><span data-stu-id="7fee0-210">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="7fee0-211">Of voer in het veld **Te verwerken aantal** respectievelijk 10 en 20 in op de twee voorraadpickregels.</span><span class="sxs-lookup"><span data-stu-id="7fee0-211">Alternatively, in the **Qty. to Handle** field, enter 10 and 20 respectively on the two inventory pick lines.</span></span>  
6. <span data-ttu-id="7fee0-212">Kies de actie **Boeken**, selecteer **Verzenden** en kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fee0-212">Choose the **Post** action, select **Ship**, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="7fee0-213">Nu zijn de 30 lampen geregistreerd als gepickt uit de opslaglocaties S-01-0001 en S-01-0002, en een negatieve artikelpost is gemaakt om de geboekte verkoopverzending te weerspiegelen.</span><span class="sxs-lookup"><span data-stu-id="7fee0-213">The 30 Amsterdam Lamps are now registered as picked from bins S-01-0001 and S-01-0002, and a negative item ledger entry is created reflecting the posted sales shipment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7fee0-214">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7fee0-214">See Also</span></span>

[<span data-ttu-id="7fee0-215">Artikelen picken met een voorraadpick</span><span class="sxs-lookup"><span data-stu-id="7fee0-215">Pick Items with Inventory Picks</span></span>](warehouse-how-to-pick-items-with-inventory-picks.md)  
[<span data-ttu-id="7fee0-216">Picken van artikelen voor magazijnverzending</span><span class="sxs-lookup"><span data-stu-id="7fee0-216">Pick Items for Warehouse Shipment</span></span>](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[<span data-ttu-id="7fee0-217">Standaardmagazijnen met bewerkingsgebieden instellen</span><span class="sxs-lookup"><span data-stu-id="7fee0-217">Set Up Basic Warehouses with Operations Areas</span></span>](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[<span data-ttu-id="7fee0-218">Onderdelen verplaatsen naar een bewerkingsgebied in standaardmagazijnconfiguraties</span><span class="sxs-lookup"><span data-stu-id="7fee0-218">Move Components to an Operation Area in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[<span data-ttu-id="7fee0-219">Picken voor productie of assemblage</span><span class="sxs-lookup"><span data-stu-id="7fee0-219">Pick for Production or Assembly</span></span>](warehouse-how-to-pick-for-production.md)  
[<span data-ttu-id="7fee0-220">Artikelen ad hoc verplaatsen in standaardmagazijnconfiguraties</span><span class="sxs-lookup"><span data-stu-id="7fee0-220">Move Items Ad Hoc in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[<span data-ttu-id="7fee0-221">Ontwerpdetails: Uitgaande magazijnstroom</span><span class="sxs-lookup"><span data-stu-id="7fee0-221">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="7fee0-222">Procedures voor bedrijfsprocessen</span><span class="sxs-lookup"><span data-stu-id="7fee0-222">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
<span data-ttu-id="7fee0-223">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7fee0-223">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]
