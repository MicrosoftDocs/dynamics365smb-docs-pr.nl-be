---
title: Picken en verzenden in standaardmagazijnconfiguraties | Microsoft Docs
description: In Business Central kunnen uitgaande processen voor picken en verzending op vier manieren worden uitgevoerd met verschillende functionaliteiten afhankelijk van het complexiteitsniveau van het magazijn.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2020
ms.author: sgroespe
ms.openlocfilehash: 475f32dbaf9b4b80a61e1cad542fbf6db79cb029
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528322"
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a><span data-ttu-id="8d3a7-103">Procedure: picken en verzenden in standaardmagazijnconfiguraties</span><span class="sxs-lookup"><span data-stu-id="8d3a7-103">Walkthrough: Picking and Shipping in Basic Warehouse Configurations</span></span>

[!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]

<span data-ttu-id="8d3a7-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)] kunnen uitgaande processen voor picken en verzending op vier manieren worden uitgevoerd met verschillende functionaliteiten afhankelijk van het complexiteitsniveau van het magazijn.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the outbound processes for picking and shipping can be performed in four ways using different functionalities depending on the warehouse complexity level.</span></span>  

|<span data-ttu-id="8d3a7-105">Methode</span><span class="sxs-lookup"><span data-stu-id="8d3a7-105">Method</span></span>|<span data-ttu-id="8d3a7-106">Inkomend proces</span><span class="sxs-lookup"><span data-stu-id="8d3a7-106">Inbound process</span></span>|<span data-ttu-id="8d3a7-107">Opslaglocaties</span><span class="sxs-lookup"><span data-stu-id="8d3a7-107">Bins</span></span>|<span data-ttu-id="8d3a7-108">Magazijnpicks</span><span class="sxs-lookup"><span data-stu-id="8d3a7-108">Picks</span></span>|<span data-ttu-id="8d3a7-109">Verzendingen</span><span class="sxs-lookup"><span data-stu-id="8d3a7-109">Shipments</span></span>|<span data-ttu-id="8d3a7-110">Complexiteitsniveau (zie [Ontwerpdetails: Magazijninstelling](design-details-warehouse-setup.md))</span><span class="sxs-lookup"><span data-stu-id="8d3a7-110">Complexity level (See [Design Details: Warehouse Setup](design-details-warehouse-setup.md))</span></span>|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|<span data-ttu-id="8d3a7-111">A</span><span class="sxs-lookup"><span data-stu-id="8d3a7-111">A</span></span>|<span data-ttu-id="8d3a7-112">Picken en verzending van de orderregel boeken</span><span class="sxs-lookup"><span data-stu-id="8d3a7-112">Post pick and shipment from the order line</span></span>|<span data-ttu-id="8d3a7-113">X</span><span class="sxs-lookup"><span data-stu-id="8d3a7-113">X</span></span>|||<span data-ttu-id="8d3a7-114">2</span><span class="sxs-lookup"><span data-stu-id="8d3a7-114">2</span></span>|  
|<span data-ttu-id="8d3a7-115">B</span><span class="sxs-lookup"><span data-stu-id="8d3a7-115">B</span></span>|<span data-ttu-id="8d3a7-116">Picken en verzending van een voorraadpickdocument boeken</span><span class="sxs-lookup"><span data-stu-id="8d3a7-116">Post pick and shipment from an inventory pick document</span></span>||<span data-ttu-id="8d3a7-117">X</span><span class="sxs-lookup"><span data-stu-id="8d3a7-117">X</span></span>||<span data-ttu-id="8d3a7-118">3</span><span class="sxs-lookup"><span data-stu-id="8d3a7-118">3</span></span>|  
|<span data-ttu-id="8d3a7-119">L</span><span class="sxs-lookup"><span data-stu-id="8d3a7-119">C</span></span>|<span data-ttu-id="8d3a7-120">Picken en verzending van een magazijnverzendingdocument boeken</span><span class="sxs-lookup"><span data-stu-id="8d3a7-120">Post pick and shipment from a warehouse shipment document</span></span>|||<span data-ttu-id="8d3a7-121">X</span><span class="sxs-lookup"><span data-stu-id="8d3a7-121">X</span></span>|<span data-ttu-id="8d3a7-122">5-4-6</span><span class="sxs-lookup"><span data-stu-id="8d3a7-122">4/5/6</span></span>|  
|<span data-ttu-id="8d3a7-123">D</span><span class="sxs-lookup"><span data-stu-id="8d3a7-123">D</span></span>|<span data-ttu-id="8d3a7-124">Picken van een magazijnpickdocument en verzending van een magazijnverzendingdocument boeken</span><span class="sxs-lookup"><span data-stu-id="8d3a7-124">Post pick from a warehouse pick document and post shipment from a warehouse shipment document</span></span>||<span data-ttu-id="8d3a7-125">X</span><span class="sxs-lookup"><span data-stu-id="8d3a7-125">X</span></span>|<span data-ttu-id="8d3a7-126">X</span><span class="sxs-lookup"><span data-stu-id="8d3a7-126">X</span></span>|<span data-ttu-id="8d3a7-127">5-4-6</span><span class="sxs-lookup"><span data-stu-id="8d3a7-127">4/5/6</span></span>|  

<span data-ttu-id="8d3a7-128">Zie voor meer informatie [Ontwerpdetails: Uitgaande magazijnstroom](design-details-outbound-warehouse-flow.md).</span><span class="sxs-lookup"><span data-stu-id="8d3a7-128">For more information, see [Design Details: Outbound Warehouse Flow](design-details-outbound-warehouse-flow.md).</span></span>  

<span data-ttu-id="8d3a7-129">De volgende procedure geeft methode B in de vorige tabel weer.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-129">The following walkthrough demonstrates method B in the previous table.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="8d3a7-130">Informatie over deze procedure</span><span class="sxs-lookup"><span data-stu-id="8d3a7-130">About This Walkthrough</span></span>

<span data-ttu-id="8d3a7-131">In standaardmagazijnconfiguraties waarbij voor uw vestiging wel een pickverwerking vereist is, maar geen verzendingsverwerking, gebruikt u de pagina **Voorraadpick** om pick- en verzendingsinformatie voor de uitgaande brondocumenten te verzamelen en boeken.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-131">In basic warehouse configurations where your location is set up to require pick processing but not ship processing, you use the **Inventory Pick** page to record and post pick and ship information for your outbound source documents.</span></span> <span data-ttu-id="8d3a7-132">Het uitgaand brondocument kan een verkooporder zijn, maar ook een inkoopretourorder, een uitgaande transferorder of een productieorder met daarop de materiaalbehoefte.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-132">The outbound source document can be a sales order, purchase return order, outbound transfer order, or a production order with component need.</span></span>  

<span data-ttu-id="8d3a7-133">In deze procedure worden de volgende taken gedemonstreerd:</span><span class="sxs-lookup"><span data-stu-id="8d3a7-133">This walkthrough demonstrates the following tasks:</span></span>  

- <span data-ttu-id="8d3a7-134">Locatie ZILVER instellen voor voorraadpicks.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-134">Setting up SILVER location for inventory picks.</span></span>  
- <span data-ttu-id="8d3a7-135">Maak een verkooporder voor klant 10000 voor 30 luidsprekers.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-135">Creating a sales order for customer 10000 for 30 loudspeakers.</span></span>  
- <span data-ttu-id="8d3a7-136">De verkooporder vrijgeven voor magazijnverwerking.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-136">Releasing the sales order for warehouse handling.</span></span>  
- <span data-ttu-id="8d3a7-137">Een voorraadpick maken op basis van een vrijgegeven brondocument.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-137">Creating an inventory pick based on a released source document.</span></span>  
- <span data-ttu-id="8d3a7-138">De magazijnverplaatsing van het magazijn vastleggen en tegelijkertijd de verkoopverzending voor de bronverkooporder boeken.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-138">Registering the warehouse movement from the warehouse and at the same time posting the sales shipment for the source sales order.</span></span>  

## <a name="roles"></a><span data-ttu-id="8d3a7-139">Rollen</span><span class="sxs-lookup"><span data-stu-id="8d3a7-139">Roles</span></span>

<span data-ttu-id="8d3a7-140">In dit overzicht worden taken gedemonstreerd voor de volgende gebruikersrollen:</span><span class="sxs-lookup"><span data-stu-id="8d3a7-140">This walkthrough demonstrates tasks that are performed by the following user roles:</span></span>  

- <span data-ttu-id="8d3a7-141">Magazijnbeheerder</span><span class="sxs-lookup"><span data-stu-id="8d3a7-141">Warehouse Manager</span></span>  
- <span data-ttu-id="8d3a7-142">Orderverwerker</span><span class="sxs-lookup"><span data-stu-id="8d3a7-142">Order Processor</span></span>  
- <span data-ttu-id="8d3a7-143">Magazijnmedewerker</span><span class="sxs-lookup"><span data-stu-id="8d3a7-143">Warehouse Worker</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="8d3a7-144">Vereisten</span><span class="sxs-lookup"><span data-stu-id="8d3a7-144">Prerequisites</span></span>

<span data-ttu-id="8d3a7-145">U moet het volgende doen om deze procedure uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="8d3a7-145">To complete this walkthrough, you will need:</span></span>  

- <span data-ttu-id="8d3a7-146">Voor [!INCLUDE[prodshort](includes/prodshort.md)] online, een bedrijf gebaseerd op de optie **Geavanceerde evaluatie - volledige voorbeeldgegevens** in een sandboxomgeving.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-146">For [!INCLUDE[prodshort](includes/prodshort.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment.</span></span> <span data-ttu-id="8d3a7-147">Voor [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, CRONUS International Ltd. geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-147">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, CRONUS International Ltd. installed.</span></span>  
- <span data-ttu-id="8d3a7-148">Maak van uzelf een magazijnwerknemer bij de vestiging ZILVER door de volgende stappen uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="8d3a7-148">To make yourself a warehouse employee at the location SILVER by following these steps:</span></span>  

  1. <span data-ttu-id="8d3a7-149">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnmedewerkers** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-149">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="8d3a7-150">Kies het veld **Gebruikers-ID** en selecteer uw eigen gebruikersaccount op de pagina **Gebruikers**.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-150">Choose the **User ID** field, and select your own user account on the **Users** page.</span></span>  
  3. <span data-ttu-id="8d3a7-151">Voer ZILVER in het veld **Vestiging** in.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-151">In the **Location Code** field, enter SILVER.</span></span>  
  4. <span data-ttu-id="8d3a7-152">Selecteer het veld **Standaard**.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-152">Select the **Default** field.</span></span>  

- <span data-ttu-id="8d3a7-153">Maak artikel LS-81 beschikbaar op locatie ZILVER door deze stappen te volgen:</span><span class="sxs-lookup"><span data-stu-id="8d3a7-153">Make item LS-81 available at SILVER location by following these steps:</span></span>  

  1. <span data-ttu-id="8d3a7-154">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikeldagboeken** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-154">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Journals**, and then choose the related link.</span></span>  
  2. <span data-ttu-id="8d3a7-155">Open het standaarddagboek en maak twee artikeldagboekregels met de volgende informatie over de werkdatum (23 januari).</span><span class="sxs-lookup"><span data-stu-id="8d3a7-155">Open the default journal, and then create two item journal lines with the following information about the work date (January 23).</span></span>  

        |<span data-ttu-id="8d3a7-156">Boekingssoort</span><span class="sxs-lookup"><span data-stu-id="8d3a7-156">Entry Type</span></span>|<span data-ttu-id="8d3a7-157">Artikelnummer</span><span class="sxs-lookup"><span data-stu-id="8d3a7-157">Item Number</span></span>|<span data-ttu-id="8d3a7-158">Vestiging</span><span class="sxs-lookup"><span data-stu-id="8d3a7-158">Location Code</span></span>|<span data-ttu-id="8d3a7-159">Opslaglocatie</span><span class="sxs-lookup"><span data-stu-id="8d3a7-159">Bin Code</span></span>|<span data-ttu-id="8d3a7-160">Aantal</span><span class="sxs-lookup"><span data-stu-id="8d3a7-160">Quantity</span></span>|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |<span data-ttu-id="8d3a7-161">Pos. correctie</span><span class="sxs-lookup"><span data-stu-id="8d3a7-161">Positive Adjmt.</span></span>|<span data-ttu-id="8d3a7-162">LS-81</span><span class="sxs-lookup"><span data-stu-id="8d3a7-162">LS-81</span></span>|<span data-ttu-id="8d3a7-163">ZILVER</span><span class="sxs-lookup"><span data-stu-id="8d3a7-163">SILVER</span></span>|<span data-ttu-id="8d3a7-164">S-01-0001</span><span class="sxs-lookup"><span data-stu-id="8d3a7-164">S-01-0001</span></span>|<span data-ttu-id="8d3a7-165">20</span><span class="sxs-lookup"><span data-stu-id="8d3a7-165">20</span></span>|  
        |<span data-ttu-id="8d3a7-166">Pos. correctie</span><span class="sxs-lookup"><span data-stu-id="8d3a7-166">Positive Adjmt.</span></span>|<span data-ttu-id="8d3a7-167">LS-81</span><span class="sxs-lookup"><span data-stu-id="8d3a7-167">LS-81</span></span>|<span data-ttu-id="8d3a7-168">ZILVER</span><span class="sxs-lookup"><span data-stu-id="8d3a7-168">SILVER</span></span>|<span data-ttu-id="8d3a7-169">S-01-0002</span><span class="sxs-lookup"><span data-stu-id="8d3a7-169">S-01-0002</span></span>|<span data-ttu-id="8d3a7-170">20</span><span class="sxs-lookup"><span data-stu-id="8d3a7-170">20</span></span>|  

  3. <span data-ttu-id="8d3a7-171">Kies de actie **Boeken** en selecteer de knop **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-171">Choose the **Post** action, and then select the **Yes** button.</span></span>  

## <a name="story"></a><span data-ttu-id="8d3a7-172">Scenario</span><span class="sxs-lookup"><span data-stu-id="8d3a7-172">Story</span></span>

<span data-ttu-id="8d3a7-173">Ellen, de magazijnmanager bij CRONUS, stelt magazijn ZILVER in voor basispickverwerking waarbij magazijnmedewerkers uitgaande orders afzonderlijk verwerken.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-173">Ellen, the warehouse manager at CRONUS, sets up SILVER warehouse for basic pick handling where warehouse workers process outbound orders individually.</span></span> <span data-ttu-id="8d3a7-174">De orderverwerker Suzanne maakt een verkooporder voor 30 eenheden van het artikel LS-81 om aan klant 10000 vanuit het ZILVER Magazijn te worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-174">Susan, the order processor, creates a sales order for 30 units of item LS-81 to be shipped to customer 10000 from the SILVER Warehouse.</span></span> <span data-ttu-id="8d3a7-175">De magazijnmedewerker John zorgt ervoor dat de verzending wordt voorbereid en aan de klant geleverd.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-175">John, the warehouse worker must make sure that the shipment is prepared and delivered to the customer.</span></span> <span data-ttu-id="8d3a7-176">John beheert alle betrokken taken op de pagina **Voorraadpick**, dat automatisch wijst naar de opslaglocaties waar LS-81 is opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-176">John manages all involved tasks on the **Inventory Pick** page, which automatically points to the bins where LS-81 is stored.</span></span>  

## <a name="setting-up-the-location"></a><span data-ttu-id="8d3a7-177">De locatie instellen</span><span class="sxs-lookup"><span data-stu-id="8d3a7-177">Setting Up the Location</span></span>

<span data-ttu-id="8d3a7-178">De instellingen van de pagina **Vestiging** definiëren de magazijnstromen van het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-178">The setup of the **Location Card** page defines the company’s warehouse flows.</span></span>  

### <a name="to-set-up-the-location"></a><span data-ttu-id="8d3a7-179">De vestiging instellen</span><span class="sxs-lookup"><span data-stu-id="8d3a7-179">To set up the location</span></span>

1. <span data-ttu-id="8d3a7-180">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vestigingen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-180">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Locations**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8d3a7-181">Open de vestigingskaart ZILVER.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-181">Open the SILVER location card.</span></span>  
3. <span data-ttu-id="8d3a7-182">Schakel op het sneltabblad **Magazijn** het selectievakje **Pick vereist** in.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-182">On the **Warehouse** FastTab, choose the **Require Pick** check box.</span></span>  

## <a name="creating-the-sales-order"></a><span data-ttu-id="8d3a7-183">De verkooporder maken</span><span class="sxs-lookup"><span data-stu-id="8d3a7-183">Creating the Sales Order</span></span>

<span data-ttu-id="8d3a7-184">Verkooporders zijn de meest gebruikte soort uitgaand brondocument.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-184">Sales orders are the most common type of outbound source document.</span></span>  

### <a name="to-create-the-sales-order"></a><span data-ttu-id="8d3a7-185">De verkooporder maken</span><span class="sxs-lookup"><span data-stu-id="8d3a7-185">To create the sales order</span></span>

1. <span data-ttu-id="8d3a7-186">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-186">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8d3a7-187">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-187">Choose the **New** action.</span></span>  
3. <span data-ttu-id="8d3a7-188">Maak een verkooporder voor klant 10000 op 23 januari (werkdatum) met de volgende verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-188">Create a sales order for customer 10000 on the work date (January 23) with the following sales order line.</span></span>  

    |<span data-ttu-id="8d3a7-189">Artikel</span><span class="sxs-lookup"><span data-stu-id="8d3a7-189">Item</span></span>|<span data-ttu-id="8d3a7-190">Vestiging</span><span class="sxs-lookup"><span data-stu-id="8d3a7-190">Location Code</span></span>|<span data-ttu-id="8d3a7-191">Aantal</span><span class="sxs-lookup"><span data-stu-id="8d3a7-191">Quantity</span></span>|  
    |----|-------------|--------|  
    |<span data-ttu-id="8d3a7-192">LS_81</span><span class="sxs-lookup"><span data-stu-id="8d3a7-192">LS_81</span></span>|<span data-ttu-id="8d3a7-193">ZILVER</span><span class="sxs-lookup"><span data-stu-id="8d3a7-193">SILVER</span></span>|<span data-ttu-id="8d3a7-194">30</span><span class="sxs-lookup"><span data-stu-id="8d3a7-194">30</span></span>|  

     <span data-ttu-id="8d3a7-195">Ga door om het magazijn te informeren dat de verkooporder klaar is voor magazijnverwerking.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-195">Proceed to notify the warehouse that the sales order is ready for warehouse handling.</span></span>  

4. <span data-ttu-id="8d3a7-196">Kies de actie **Vrijgeven**.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-196">Choose the **Release** action.</span></span>  

    <span data-ttu-id="8d3a7-197">John gaat door met het picken en verzenden van de verkochte artikelen.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-197">John proceeds to pick and ship the sold items.</span></span>  

## <a name="picking-and-shipping-items"></a><span data-ttu-id="8d3a7-198">Artikelen picken en verzenden</span><span class="sxs-lookup"><span data-stu-id="8d3a7-198">Picking and Shipping Items</span></span>

<span data-ttu-id="8d3a7-199">Op de pagina **Voorraadpick** kunt u alle uitgaande magazijnactiviteiten voor een bepaald brondocument, zoals een verkooporder, beheren.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-199">On the **Inventory Pick** page, you can manage all outbound warehouse activities for a specific source document, such as a sales order.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a><span data-ttu-id="8d3a7-200">U kunt als volgt artikels picken en verzenden</span><span class="sxs-lookup"><span data-stu-id="8d3a7-200">To pick and ship items</span></span>

1. <span data-ttu-id="8d3a7-201">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraadpicks** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-201">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Picks**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8d3a7-202">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-202">Choose the **New** action.</span></span>  

    <span data-ttu-id="8d3a7-203">Zorg ervoor dat het veld **Nee.**</span><span class="sxs-lookup"><span data-stu-id="8d3a7-203">Make sure that the **No.**</span></span> <span data-ttu-id="8d3a7-204">op het sneltabblad **Algemeen** is ingevuld.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-204">field on the **General** FastTab is filled in.</span></span>
3. <span data-ttu-id="8d3a7-205">Selecteer het veld **Brondocument** en selecteer vervolgens **Verkooporder**.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-205">Select the **Source Document** field, and then select **Sales Order**.</span></span>  
4. <span data-ttu-id="8d3a7-206">Selecteer het veld **Bronnr.**, selecteer de regel voor de verkoop aan klant 10000, en kies vervolgens de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-206">Select the **Source No.** field, select the line for the sale to customer 10000, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="8d3a7-207">U kunt ook de actie **Brondocument ophalen** kiezen en de verkooporder kiezen.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-207">Alternatively, choose the **Get Source Document** action, and then select the sales order.</span></span>  
5. <span data-ttu-id="8d3a7-208">Kies de actie **Te verwerken aantal autom. invullen**.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-208">Choose the **Autofill Qty. to Handle** action.</span></span>  

    <span data-ttu-id="8d3a7-209">Of voer in het veld **Te verwerken aantal** respectievelijk 10 en 20 in op de twee voorraadpickregels.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-209">Alternatively, in the **Qty. to Handle** field, enter 10 and 20 respectively on the two inventory pick lines.</span></span>  
6. <span data-ttu-id="8d3a7-210">Kies de actie **Boeken**, selecteer **Verzenden** en kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-210">Choose the **Post** action, select **Ship**, and then choose the **OK** button.</span></span>  

    <span data-ttu-id="8d3a7-211">Nu zijn de 30 luidsprekers geregistreerd als gepickt uit de opslaglocaties S-01-0001 en S-01-0002, en een negatieve artikelpost is gemaakt om de geboekte verkoopverzending te weerspiegelen.</span><span class="sxs-lookup"><span data-stu-id="8d3a7-211">The 30 loudspeakers are now registered as picked from bins S-01-0001 and S-01-0002, and a negative item ledger entry is created reflecting the posted sales shipment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8d3a7-212">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8d3a7-212">See Also</span></span>

[<span data-ttu-id="8d3a7-213">Artikelen picken met een voorraadpick</span><span class="sxs-lookup"><span data-stu-id="8d3a7-213">Pick Items with Inventory Picks</span></span>](warehouse-how-to-pick-items-with-inventory-picks.md)  
[<span data-ttu-id="8d3a7-214">Picken van artikelen voor magazijnverzending</span><span class="sxs-lookup"><span data-stu-id="8d3a7-214">Pick Items for Warehouse Shipment</span></span>](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[<span data-ttu-id="8d3a7-215">Standaardmagazijnen met bewerkingsgebieden instellen</span><span class="sxs-lookup"><span data-stu-id="8d3a7-215">Set Up Basic Warehouses with Operations Areas</span></span>](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[<span data-ttu-id="8d3a7-216">Onderdelen verplaatsen naar een bewerkingsgebied in standaardmagazijnconfiguraties</span><span class="sxs-lookup"><span data-stu-id="8d3a7-216">Move Components to an Operation Area in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  
[<span data-ttu-id="8d3a7-217">Picken voor productie of assemblage</span><span class="sxs-lookup"><span data-stu-id="8d3a7-217">Pick for Production or Assembly</span></span>](warehouse-how-to-pick-for-production.md)  
[<span data-ttu-id="8d3a7-218">Artikelen ad hoc verplaatsen in standaardmagazijnconfiguraties</span><span class="sxs-lookup"><span data-stu-id="8d3a7-218">Move Items Ad Hoc in Basic Warehouse Configurations</span></span>](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[<span data-ttu-id="8d3a7-219">Ontwerpdetails: Uitgaande magazijnstroom</span><span class="sxs-lookup"><span data-stu-id="8d3a7-219">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="8d3a7-220">Procedures voor bedrijfsprocessen</span><span class="sxs-lookup"><span data-stu-id="8d3a7-220">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
<span data-ttu-id="8d3a7-221">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8d3a7-221">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
