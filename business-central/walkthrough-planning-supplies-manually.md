---
title: 'Procedure: Leveringen handmatig plannen | Microsoft Docs'
description: In het volgende overzicht ziet u het proces voor het plannen van voorraadorders om aan nieuwe vraag te voldoen. U kunt voorraadplanning starten met vaste tussenpozen, bijvoorbeeld elke ochtend of elke maandag, of wanneer u bericht krijgt van verkoop of productie, afhankelijk van het type vraag.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: f8c20f51997ca2ec056423b9089b645e5a258235
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1248974"
---
# <a name="walkthrough-planning-supplies-manually"></a><span data-ttu-id="70194-104">Procedure: Leveringen handmatig plannen</span><span class="sxs-lookup"><span data-stu-id="70194-104">Walkthrough: Planning Supplies Manually</span></span>

<span data-ttu-id="70194-105">**Opmerking**: deze procedure moet op een demonstratiebedrijf worden uitgevoerd met de optie **Volledige evaluatie - volledige voorbeeldgegevens**, dat in de sandboxomgeving beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="70194-105">**Note**: This walkthrough must be performed on a demonstration company with the **Full Evaluation - Complete Sample Data** option, which is available in the Sandbox environment.</span></span> <span data-ttu-id="70194-106">Zie [Een sandboxomgeving maken](across-how-create-sandbox-environment.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="70194-106">For more information, see [Creating a Sandbox Environment](across-how-create-sandbox-environment.md).</span></span>

<span data-ttu-id="70194-107">In het volgende overzicht ziet u het proces voor het plannen van voorraadorders om aan nieuwe vraag te voldoen.</span><span class="sxs-lookup"><span data-stu-id="70194-107">This walkthrough demonstrates the process of planning supply orders to fulfill new demand.</span></span> <span data-ttu-id="70194-108">U kunt voorraadplanning starten met vaste tussenpozen, bijvoorbeeld elke ochtend of elke maandag, of wanneer u bericht krijgt van verkoop of productie, afhankelijk van het type vraag.</span><span class="sxs-lookup"><span data-stu-id="70194-108">You can initiate supply planning at fixed intervals, for example, every morning or every Monday, or when you are notified by sales or production, depending on the type of demand.</span></span> <span data-ttu-id="70194-109">In dit scenario gebruikt u de pagina **Orderplanning**, een eenvoudig voorraadplanningshulpmiddel op basis van handmatige besluitvorming in plaats van automatische planning op basis van parameters.</span><span class="sxs-lookup"><span data-stu-id="70194-109">In this walkthrough you will use the **Order Planning** page, a simple supply planning tool that is based on manual decision-making instead of parameter-based automatic planning.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="70194-110">Informatie over deze procedure</span><span class="sxs-lookup"><span data-stu-id="70194-110">About This Walkthrough</span></span>  
 <span data-ttu-id="70194-111">In deze procedure worden de volgende taken beschreven:</span><span class="sxs-lookup"><span data-stu-id="70194-111">This walkthrough illustrates the following tasks:</span></span>  

-   <span data-ttu-id="70194-112">Een inkooporder plannen voor het fabriceren van onderdelen.</span><span class="sxs-lookup"><span data-stu-id="70194-112">Planning a purchase order for manufacturing components.</span></span>  
-   <span data-ttu-id="70194-113">Een transferorder plannen om aan de verkoopvraag te voldoen.</span><span class="sxs-lookup"><span data-stu-id="70194-113">Planning a transfer order to fulfill sales demand.</span></span>  
-   <span data-ttu-id="70194-114">Een productieorder plannen voor een artikel met meerdere niveaus.</span><span class="sxs-lookup"><span data-stu-id="70194-114">Planning a production order for a multilevel item.</span></span>  

## <a name="roles"></a><span data-ttu-id="70194-115">Rollen</span><span class="sxs-lookup"><span data-stu-id="70194-115">Roles</span></span>  
 <span data-ttu-id="70194-116">In deze procedure worden taken gedemonstreerd voor de volgende gebruikersrollen:</span><span class="sxs-lookup"><span data-stu-id="70194-116">This walkthrough demonstrates tasks performed by the following user roles:</span></span>  

-   <span data-ttu-id="70194-117">Productieplanner</span><span class="sxs-lookup"><span data-stu-id="70194-117">Production Planner</span></span>  
-   <span data-ttu-id="70194-118">Inkoper</span><span class="sxs-lookup"><span data-stu-id="70194-118">Purchasing Agent</span></span>  
-   <span data-ttu-id="70194-119">Verkooporderverwerker</span><span class="sxs-lookup"><span data-stu-id="70194-119">Sales Order Processor</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="70194-120">Vereisten</span><span class="sxs-lookup"><span data-stu-id="70194-120">Prerequisites</span></span>  
 <span data-ttu-id="70194-121">Voordat u met dit scenario begint, moet u de [!INCLUDE[d365fin](includes/d365fin_md.md)] installeren.</span><span class="sxs-lookup"><span data-stu-id="70194-121">Before you begin this walkthrough, you must install the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="70194-122">Breng de volgende wijzigingen aan in de database:</span><span class="sxs-lookup"><span data-stu-id="70194-122">The following modifications must be made to the database:</span></span>  

-   <span data-ttu-id="70194-123">Verwijder alle bestaande verkooporders voor fietsen.</span><span class="sxs-lookup"><span data-stu-id="70194-123">Delete all existing sales orders for bicycles.</span></span>  
-   <span data-ttu-id="70194-124">Maak één verkooporder voor 10 fietsen op de locatie BLAUW.</span><span class="sxs-lookup"><span data-stu-id="70194-124">Create one sales order for 10 bicycles at BLUE location.</span></span>  
-   <span data-ttu-id="70194-125">Verwijder alle geplande en vast geplande productieorders.</span><span class="sxs-lookup"><span data-stu-id="70194-125">Delete all planned and firm planned production orders.</span></span> <span data-ttu-id="70194-126">Verwijder geen gestarte orders met posten die al zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="70194-126">Do not delete started orders with entries that are already posted.</span></span>  

 <span data-ttu-id="70194-127">Gebruik als algemene regel de voorgestelde gegevens uit deze procedure aangezien deze gegevens de benodigde records bevatten.</span><span class="sxs-lookup"><span data-stu-id="70194-127">As a rule, use the suggested data in this walkthrough because this data has the necessary records.</span></span>  

## <a name="story"></a><span data-ttu-id="70194-128">Scenario</span><span class="sxs-lookup"><span data-stu-id="70194-128">Story</span></span>  
 <span data-ttu-id="70194-129">Eduardo, de productieplanner van een klein productiebedrijf is bezig met het plannen van de productie en inkooporders om te voldoen aan de nieuwe verkoopvraag.</span><span class="sxs-lookup"><span data-stu-id="70194-129">Eduardo, the Production Planner of a small manufacturing company, is about to plan production and purchase orders to fulfill new sales demand.</span></span>  

 <span data-ttu-id="70194-130">Aangezien de producten uit slechts enkele stuklijstniveaus bestaan en de orderstroom tamelijk gering is, gebruikt Eduardo de pagina **Orderplanning** om de orders voor voorzieningen handmatig te maken, met één productniveau tegelijk.</span><span class="sxs-lookup"><span data-stu-id="70194-130">Because the products have few BOM levels and the flow of orders is relatively low, Eduardo uses the **Order Planning** page to manually create supply orders, one product level at a time.</span></span>  

 <span data-ttu-id="70194-131">In een meer complexe productieomgeving wordt het planningsvoorstel gebruikt om de voorraad te plannen op basis van artikelparameters als herplanningsperiode, veiligheidstijd, bestelpunt en batchberekeningen van de geconsolideerde aanvraag van alle productniveaus.</span><span class="sxs-lookup"><span data-stu-id="70194-131">In a more complex manufacturing environment, the planning worksheet is used to plan supply based on item parameters such as rescheduling period, safety lead time, reorder point, and batch calculations of consolidated demand from all product levels.</span></span>  

## <a name="setting-up-the-sample-data"></a><span data-ttu-id="70194-132">Voorbeeldgegevens instellen</span><span class="sxs-lookup"><span data-stu-id="70194-132">Setting Up the Sample Data</span></span>  
 <span data-ttu-id="70194-133">In het standaarddemobedrijf CRONUS is momenteel sprake van een grote hoeveelheid niet-geplande vraag.</span><span class="sxs-lookup"><span data-stu-id="70194-133">The standard CRONUS demonstration company currently has lots of unplanned demand.</span></span> <span data-ttu-id="70194-134">Tijdens de verschillende planningstaken in deze procedure moet u afwijken van de realistische bedrijfswerkstroom door de vraag met vervaldatums in de nabije toekomst te negeren en in plaats daarvan de vraag te gebruiken met latere vervaldatums.</span><span class="sxs-lookup"><span data-stu-id="70194-134">During the different planning tasks in this walkthrough, you will have to deviate from the realistic business flow by ignoring demand with close due dates and instead use demand with later due dates.</span></span>  

## <a name="using-the-order-planning-page"></a><span data-ttu-id="70194-135">De pagina Orderplanning gebruiken</span><span class="sxs-lookup"><span data-stu-id="70194-135">Using the Order Planning Page</span></span>  

<!--
The **Order Planning** page can be accessed from several different locations on the **Departments** menu in the navigation pane:  

-   Manufacturing, Planning  
-   Sales & Marketing, Order Processing  
-   Purchase, Planning  
-   In addition, you can open this page for a specific production order by choosing **Planning** on the **Navigate** tab in the **Order** group.

-->  

### <a name="to-use-the-order-planning-page"></a><span data-ttu-id="70194-136">De pagina Orderplanning gebruiken</span><span class="sxs-lookup"><span data-stu-id="70194-136">To use the Order Planning page</span></span>  

1.  <span data-ttu-id="70194-137">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Orderplanning** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="70194-137">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Order Planning**, and then choose the related link.</span></span>  

     <span data-ttu-id="70194-138">Als de pagina **Orderplanning** voor het eerst wordt geopend, moet er een planning worden berekend om de nieuwe vraag weer te geven sinds deze voor het laatst is berekend.</span><span class="sxs-lookup"><span data-stu-id="70194-138">When the **Order Planning** page first opens, a plan must be calculated to show the new demand since it was last calculated.</span></span>  

2.  <span data-ttu-id="70194-139">Kies de actie **Plan berekenen**.</span><span class="sxs-lookup"><span data-stu-id="70194-139">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="70194-140">Het planningssysteem analyseert de nieuwe vraag die is geïntroduceerd, zoals nieuwe of gewijzigde verkoop- of productieorders.</span><span class="sxs-lookup"><span data-stu-id="70194-140">The planning system analyzes any new demand that has been introduced, such as new sales, changed sales, or production orders.</span></span>  

     <span data-ttu-id="70194-141">Op basis van de totale beschikbaarheid wordt de benodigde hoeveelheid voor elke vraagregel berekend.</span><span class="sxs-lookup"><span data-stu-id="70194-141">Based on total availability, the quantity needed for each demand line is calculated.</span></span> <span data-ttu-id="70194-142">Deze berekening wordt per order uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="70194-142">This calculation is performed order-by-order.</span></span> <span data-ttu-id="70194-143">Dit betekent dat de order met de vraagregel met de vroegste verval- of verzenddatum eerst wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="70194-143">This means that the order which includes the demand line with the earliest due date or shipment date will be calculated first.</span></span> <span data-ttu-id="70194-144">Vervolgens worden aanvullende vraagregels in dezelfde volgorde berekend, ongeacht de vervaldatum of de verzenddatum.</span><span class="sxs-lookup"><span data-stu-id="70194-144">After that, additional demand lines will be calculated in the same order, regardless of the due date or shipment date.</span></span>  

3.  <span data-ttu-id="70194-145">De pagina **Orderplanning** moet zijn gemaximaliseerd en de afmetingen van de kolomvelden moeten zo zijn ingesteld dat alle standaardveldnamen zichtbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="70194-145">Be sure that the **Order Planning** page is maximized and that column fields are resized to show all the default field names.</span></span>  

     <span data-ttu-id="70194-146">Wanneer de berekening is voltooid, worden in de pagina alle niet-afgehandelde vraagregels weergegeven als samengevouwen orderkopregels gesorteerd op de vroegste vraagdatum.</span><span class="sxs-lookup"><span data-stu-id="70194-146">When the calculation is completed, the page displays all unfulfilled demand as collapsed order header lines sorted by earliest demand date.</span></span>  

     <span data-ttu-id="70194-147">U ziet dat CRONUS diverse orders heeft met niet-afgehandelde vraag.</span><span class="sxs-lookup"><span data-stu-id="70194-147">Notice that CRONUS has several orders with unfulfilled demand.</span></span> <span data-ttu-id="70194-148">Elke vette planningsregel geeft een order weer, verkoop of productie, met inbegrip van ten minste één orderregel met onvoldoende beschikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="70194-148">Each bold planning line represents an order, sales order, or production order, including at least one order line with insufficient availability.</span></span>  

4.  <span data-ttu-id="70194-149">Selecteer in het veld **Vraag weergeven als** het filter **Alle vraag**.</span><span class="sxs-lookup"><span data-stu-id="70194-149">In the **Show Demand As** field, select the **All Demand** filter.</span></span>  

     <span data-ttu-id="70194-150">In het veld **Soort vraag** kunt u kiezen welke soorten orders u wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="70194-150">With the **Demand Type** field, you can choose which order types that you want to display.</span></span>  

     <span data-ttu-id="70194-151">Orders zonder beschikbaarheidsproblemen worden niet weergegeven.</span><span class="sxs-lookup"><span data-stu-id="70194-151">Orders that do not have availability problems are not shown.</span></span> <span data-ttu-id="70194-152">Als er geen orders bestaan wanneer een planning wordt berekend, verschijnt een bericht en worden er geen planningsregels weergegeven.</span><span class="sxs-lookup"><span data-stu-id="70194-152">If no orders exist when a plan is calculated, a message will display and no planning lines will appear.</span></span>  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a><span data-ttu-id="70194-153">Een inkooporder plannen om te voldoen aan de vraag naar onderdelen</span><span class="sxs-lookup"><span data-stu-id="70194-153">Planning a Purchase Order to Fulfill Component Demand</span></span>  
 <span data-ttu-id="70194-154">In deze procedure maakt u een inkooporder voor de benodigde productieonderdelen.</span><span class="sxs-lookup"><span data-stu-id="70194-154">In this procedure, you create a purchase order for needed manufacturing components.</span></span>  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a><span data-ttu-id="70194-155">Een inkooporder plannen om te voldoen aan de onderdelenbehoefte voor de productie</span><span class="sxs-lookup"><span data-stu-id="70194-155">To plan a purchase order to fulfill component need in production</span></span>  

1.  <span data-ttu-id="70194-156">Vouw de eerste regel uit (klik op het symbool +).</span><span class="sxs-lookup"><span data-stu-id="70194-156">Expand the first line (choose the + symbol).</span></span>  
2.  <span data-ttu-id="70194-157">Kies de eerste vraagregel met, artikel, **LSU-15** en kies de actie **Document weergeven**.</span><span class="sxs-lookup"><span data-stu-id="70194-157">Choose the first demand line, with item **LSU-15**, and then choose the **Show Document** action.</span></span>  
3.  <span data-ttu-id="70194-158">Sluit de geopende productieorder om terug te keren naar de pagina **Orderplanning**.</span><span class="sxs-lookup"><span data-stu-id="70194-158">Close the opened production order to return to the **Order Planning** page.</span></span>  
4.  <span data-ttu-id="70194-159">Selecteer **Inkoop** in het veld **Aanvullingsmethode**.</span><span class="sxs-lookup"><span data-stu-id="70194-159">In the **Replenishment System** field, select **Purchase**.</span></span>  

     <span data-ttu-id="70194-160">De standaardwaarde komt van de artikelkaart (of SKU-kaart), maar u kunt dit wijzigen in een van de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="70194-160">The default value is from the item card, or SKU card, but you can change it to one of the following options:</span></span>  

    -   <span data-ttu-id="70194-161">**Inkoop** – een inkooporder maken.</span><span class="sxs-lookup"><span data-stu-id="70194-161">**Purchase** – To create a purchase order.</span></span>  
    -   <span data-ttu-id="70194-162">**Transfer** – een transferorder maken.</span><span class="sxs-lookup"><span data-stu-id="70194-162">**Transfer** – To create a transfer order.</span></span>  
    -   <span data-ttu-id="70194-163">**Prod.-order** – een productieorder maken.</span><span class="sxs-lookup"><span data-stu-id="70194-163">**Prod. Order** – To create a production order.</span></span>  

5.  <span data-ttu-id="70194-164">Selecteer in het veld **Aanleveren van** een van de volgende opties op basis van de geselecteerde aanvullingsmethode:</span><span class="sxs-lookup"><span data-stu-id="70194-164">In the **Supply From** field, select one of the following options according to the selected replenishment system:</span></span>  

    -   <span data-ttu-id="70194-165">**Leverancier** – Voor inkoop</span><span class="sxs-lookup"><span data-stu-id="70194-165">**Vendor** – For purchases</span></span>  
    -   <span data-ttu-id="70194-166">**Locatie** – voor transfers</span><span class="sxs-lookup"><span data-stu-id="70194-166">**Location** – For transfers</span></span>  

     <span data-ttu-id="70194-167">Als het veld niet is ingevuld, verschijnt er een foutbericht wanneer u voorraadorders probeert te maken.</span><span class="sxs-lookup"><span data-stu-id="70194-167">If the field is not filled in, an error message will display when you try to create the supply orders.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="70194-168">Als voor de onderdelen een standaardleveranciernummer is ingesteld op de artikelkaarten, zijn de regels vooraf ingevuld.</span><span class="sxs-lookup"><span data-stu-id="70194-168">If the components have a default vendor number set up on the item cards, the lines will be preset.</span></span>  

6.  <span data-ttu-id="70194-169">Kies het veld **Aanleveren van**.</span><span class="sxs-lookup"><span data-stu-id="70194-169">Choose the **Supply From**  field.</span></span>  
7.  <span data-ttu-id="70194-170">Kies op de pagina **Artikelleveranciers** de actie **Nieuw** en selecteer leverancier **30000**.</span><span class="sxs-lookup"><span data-stu-id="70194-170">On the **Item Vendor Catalogue** page, choose the **New** action, and then select vendor **30000**.</span></span>  
8.  <span data-ttu-id="70194-171">Kies de knop **OK** om terug te gaan naar de pagina **Orderplanning**.</span><span class="sxs-lookup"><span data-stu-id="70194-171">Choose the **OK** button to return to the **Order Planning** page.</span></span>  
9. <span data-ttu-id="70194-172">Kopieer leveranciernummer **30000** naar de overige regels voor luidsprekeronderdelen in deze productieorder.</span><span class="sxs-lookup"><span data-stu-id="70194-172">Copy vendor **30000** to the other lines for loudspeaker components on this production order.</span></span>  

     <span data-ttu-id="70194-173">U kunt nu een inkooporder gaan maken.</span><span class="sxs-lookup"><span data-stu-id="70194-173">You are now ready to create a purchase order.</span></span>  

10. <span data-ttu-id="70194-174">Kies de actie **Orders maken**.</span><span class="sxs-lookup"><span data-stu-id="70194-174">Choose the **Make Orders** action.</span></span> <span data-ttu-id="70194-175">De pagina **Orders voor voorzieningen maken** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="70194-175">The **Make Supply Orders** page opens.</span></span>  
11. <span data-ttu-id="70194-176">Kies op het sneltabblad **Orderplanning** in het veld **Orders maken voor** de optie **Actieve order**.</span><span class="sxs-lookup"><span data-stu-id="70194-176">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **Active Order** option.</span></span>  
12. <span data-ttu-id="70194-177">Kies op het sneltabblad **Opties** in het veld **Inkooporder maken** de optie **Inkooporders maken**.</span><span class="sxs-lookup"><span data-stu-id="70194-177">On the **Options** FastTab, in the **Create Purchase Order** field, choose the **Make Purch. Order** option.</span></span>  
13. <span data-ttu-id="70194-178">Klik op **OK** om inkooporders te maken voor alle onderdelen van de order.</span><span class="sxs-lookup"><span data-stu-id="70194-178">Choose the **OK** button to create purchase orders for all the components of the order.</span></span>  

     <span data-ttu-id="70194-179">De inkooporders worden gemaakt en opgeslagen als de laatste orders in de lijst met inkooporders.</span><span class="sxs-lookup"><span data-stu-id="70194-179">The purchase orders are now created and saved as the last orders in the list of purchase orders.</span></span>  

## <a name="planning-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="70194-180">Een transferorder plannen om aan de verkoopvraag te voldoen</span><span class="sxs-lookup"><span data-stu-id="70194-180">Planning a Transfer Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="70194-181">In deze procedure gaat u plannen voor de vraag van een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="70194-181">In this procedure, you will plan for demand from a sales order.</span></span> <span data-ttu-id="70194-182">Vraagregels geven de verkoopregels aan en niet de onderdeelregels, zoals bij de productievraag.</span><span class="sxs-lookup"><span data-stu-id="70194-182">Demand lines represent sales lines and not component lines, as in production demand.</span></span>  

### <a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a><span data-ttu-id="70194-183">Een transferorder plannen om aan de verkoopvraag te voldoen</span><span class="sxs-lookup"><span data-stu-id="70194-183">To plan a transfer order to fulfill sales demand</span></span>  

1.  <span data-ttu-id="70194-184">Verplaats de aanwijzer naar de planningsregel voor ordernummer **2008**.</span><span class="sxs-lookup"><span data-stu-id="70194-184">Move the pointer to the planning line for order **2008**.</span></span>  
2.  <span data-ttu-id="70194-185">Vouw de regel uit en verplaats de aanwijzer naar de vraagregel.</span><span class="sxs-lookup"><span data-stu-id="70194-185">Expand the line and move the pointer to the demand line.</span></span>  

     <span data-ttu-id="70194-186">Verkooporder **2008 betreft** tien luidsprekers van het type **LS-120** die zijn besteld door John Haddock Insurance Co.</span><span class="sxs-lookup"><span data-stu-id="70194-186">Sales order **2008** is for ten loudspeakers, item **LS-120**, ordered by John Haddock Insurance Co.</span></span>  

     <span data-ttu-id="70194-187">Voor het artikel is het aanvulsysteem geselecteerd en de standaardleverancier wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="70194-187">The item’s defined replenishment system and default vendor will display.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="70194-188">Onder aan de pagina staan vier informatievelden.</span><span class="sxs-lookup"><span data-stu-id="70194-188">At the bottom of the page, there are four information fields.</span></span> <span data-ttu-id="70194-189">In het veld **Vroegste beschikbaarheidsdatum** zijn de tien stuks die nodig zijn, beschikbaar via een inkomende voorraadorder, maar pas negen dagen na de huidige vervaldatum.</span><span class="sxs-lookup"><span data-stu-id="70194-189">In the **Earliest Date Available** field, the ten pieces that are needed will be available, on an inbound supply order, nine days later than the current due date.</span></span> <span data-ttu-id="70194-190">Als dat te laat is voor de klant, bevat het veld **Beschikbaar voor transfer** 13 stuks van het artikel op een andere locatie.</span><span class="sxs-lookup"><span data-stu-id="70194-190">If this is too late for the customer, the **Available for Transfer** field shows 13 pieces of the item at another location.</span></span> <span data-ttu-id="70194-191">U gaat voor deze voorraad een planning maken.</span><span class="sxs-lookup"><span data-stu-id="70194-191">You will want to plan for this stock.</span></span>  

3.  <span data-ttu-id="70194-192">Kies het veld **Beschikbaar voor transfer** om de pagina **Alternatieve voorziening ophalen** te openen.</span><span class="sxs-lookup"><span data-stu-id="70194-192">Choose the **Available for Transfer** field to open the **Get Alternative Supply** page.</span></span>  
4.  <span data-ttu-id="70194-193">Klik op **OK** om de tien beschikbare artikelen te boeken.</span><span class="sxs-lookup"><span data-stu-id="70194-193">Choose the **OK** button to book the ten items that are available.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="70194-194">Op de vraagregel wordt de voorgestelde inkoop vervangen door een transfer van de locatie GROEN.</span><span class="sxs-lookup"><span data-stu-id="70194-194">In the demand line, the suggested purchase has been exchanged with a transfer from GREEN location.</span></span> <span data-ttu-id="70194-195">Met de functie **Orders maken** maakt u een transferorder van GROEN naar de gewenste locatie.</span><span class="sxs-lookup"><span data-stu-id="70194-195">The **Make Orders** function creates a transfer order from GREEN to the demanded location.</span></span> <span data-ttu-id="70194-196">Het veld **Vervangingsartikel** werkt op dezelfde manier.</span><span class="sxs-lookup"><span data-stu-id="70194-196">The **Substitutes Exists** field works in the same way.</span></span>  

5.  <span data-ttu-id="70194-197">Kies de actie **Orders maken**.</span><span class="sxs-lookup"><span data-stu-id="70194-197">Choose the **Make Orders** action.</span></span> <span data-ttu-id="70194-198">De pagina **Orders voor voorzieningen maken** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="70194-198">The **Make Supply Orders** page opens.</span></span>  
6.  <span data-ttu-id="70194-199">Kies op het sneltabblad **Orderplanning** in het veld **Orders maken voor** de optie **Actieve order**.</span><span class="sxs-lookup"><span data-stu-id="70194-199">On the **Order Planning** FastTab, in the **Make Orders for** field, choose the **The Active Order** option.</span></span>  
7.  <span data-ttu-id="70194-200">Selecteer op het sneltabblad **Opties** in het veld **Transferorder maken** de optie **Transferorders maken**.</span><span class="sxs-lookup"><span data-stu-id="70194-200">On the **Options** FastTab, in the **Create Transfer Order** field, select the **Make Trans. Orders** option.</span></span>  
8.  <span data-ttu-id="70194-201">Klik op **OK** om de transferorder te maken om te voldoen aan de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="70194-201">Choose the **OK** button to create the transfer order to supply the sales order.</span></span>  

     <span data-ttu-id="70194-202">De transferorder is nu gemaakt en in de lijst opgeslagen als de laatste order in de lijst met open transferorders.</span><span class="sxs-lookup"><span data-stu-id="70194-202">The transfer order is now created and saved in the list as the last order in the list of open transfer orders.</span></span>  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a><span data-ttu-id="70194-203">Een productieorder met meerdere niveaus plannen om aan de verkoopvraag te voldoen</span><span class="sxs-lookup"><span data-stu-id="70194-203">Planning a Multilevel Production Order to Fulfill Sales Demand</span></span>  
 <span data-ttu-id="70194-204">In deze procedure gaat u plannen om aan de verkoopvraag te voldoen voor een geproduceerd artikel met meerdere productniveaus, waarbij de productievraag voor alle niveaus samenhangt.</span><span class="sxs-lookup"><span data-stu-id="70194-204">In this procedure, you will plan to fulfill sales demand for a produced item with multiple product levels, each creating dependent production demand.</span></span>  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a><span data-ttu-id="70194-205">Een productie met meerdere niveaus plannen om aan de verkoopvraag te voldoen</span><span class="sxs-lookup"><span data-stu-id="70194-205">To plan multilevel production to fulfill sales demand</span></span>  

1.  <span data-ttu-id="70194-206">Selecteer de planningsregel met de verkoopvraag voor ordernummer **1001** (gemaakt bij de vereiste gegevens).</span><span class="sxs-lookup"><span data-stu-id="70194-206">Select the planning line with sales demand for order **1001**, created earlier as prerequisite data.</span></span>  

     <span data-ttu-id="70194-207">Deze vraag is een verkoopregel maar voor het artikel is het aanvulsysteem **Prod.-order** gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="70194-207">This demand is a sales line, but the item has a defined replenishment system of **Prod. Order**.</span></span> <span data-ttu-id="70194-208">Voeg een tweede bel toe aan de onderdelenlijst voor elke fiets.</span><span class="sxs-lookup"><span data-stu-id="70194-208">Proceed to add an extra bell to the component need of each bicycle.</span></span>  

2.  <span data-ttu-id="70194-209">Kies de actie **Materialen** om de pagina **Planningsmaterialen** te openen.</span><span class="sxs-lookup"><span data-stu-id="70194-209">Choose the **Components** action to open the **Planning Components** page.</span></span>  
3.  <span data-ttu-id="70194-210">Wijzig in de regel voor de fietsbel het veld **Aantal per** van **1** in **2**.</span><span class="sxs-lookup"><span data-stu-id="70194-210">On the line with the Bell item, change the **Quantity per** field from **1** to **2**.</span></span>  
4.  <span data-ttu-id="70194-211">Bekijk op de pagina **Orderplanning** de planningsalternatieven.</span><span class="sxs-lookup"><span data-stu-id="70194-211">On the **Order Planning** page, consider your planning alternatives.</span></span> <span data-ttu-id="70194-212">In dit geval zijn er geen alternatieve leveringsmethoden, geen transfer, geen vervangend artikel en geen latere levering.</span><span class="sxs-lookup"><span data-stu-id="70194-212">In this case, you have no alternative means of supply, no transfer, substitute, or later delivery.</span></span> <span data-ttu-id="70194-213">U moet de voorgestelde voorzieningsorder, een productieorder, maken.</span><span class="sxs-lookup"><span data-stu-id="70194-213">You must create the suggested supply order, a production order.</span></span>  
5.  <span data-ttu-id="70194-214">Kies de actie **Orders maken** om de productieorder te maken.</span><span class="sxs-lookup"><span data-stu-id="70194-214">Choose the **Make Orders** action to create the production order.</span></span>  

     <span data-ttu-id="70194-215">U ziet dat op de pagina **Orderplanning** de planningsregel voor verkooporder **1001** niet meer bestaat en dat aan de eerste verkoopvraag is voldaan.</span><span class="sxs-lookup"><span data-stu-id="70194-215">On the **Order Planning** page, notice that the planning line for sales order **1001** no longer exists and that the initial sales demand has been covered.</span></span>  

6.  <span data-ttu-id="70194-216">Sluit de pagina **Orderplanning**.</span><span class="sxs-lookup"><span data-stu-id="70194-216">Close the **Order Planning** page.</span></span>  

     <span data-ttu-id="70194-217">U zou nu in deze weergave kunnen blijven om alle planningstaken te voltooien.</span><span class="sxs-lookup"><span data-stu-id="70194-217">Now, you could choose to stay in this view and complete all the planning tasks.</span></span> <span data-ttu-id="70194-218">In plaats daarvan neemt u nu de rol van de productieplanner op en gaat u naar de zojuist gemaakte productieorder om de pagina **Orderplanning** te openen.</span><span class="sxs-lookup"><span data-stu-id="70194-218">Instead, you will now take on the Production Planner role by going to the production order that you just created and access the **Order Planning** page.</span></span>  

 <span data-ttu-id="70194-219">Als productieplanner moet u nu een specifieke productieorder plannen.</span><span class="sxs-lookup"><span data-stu-id="70194-219">As a production planner you now must plan a specific production order.</span></span>  

### <a name="to-plan-a-specific-production-order"></a><span data-ttu-id="70194-220">Een specifieke productieorder plannen</span><span class="sxs-lookup"><span data-stu-id="70194-220">To plan a specific production order</span></span>  

1.  <span data-ttu-id="70194-221">Open de productieorder **101001** (voor tien fietsen) die u hebt gemaakt met de functie **Orders maken**.</span><span class="sxs-lookup"><span data-stu-id="70194-221">Open the production order **101001**, for ten bicycles, that you just created by using the **Make Orders** function.</span></span>  
2.  <span data-ttu-id="70194-222">Open de pagina **Prod.-ordermaterialen** om te controleren of de extra bel wordt weergegeven op de productieorder.</span><span class="sxs-lookup"><span data-stu-id="70194-222">Open the **Prod. Order Components** page to check that the extra bell is reflected on the production order.</span></span>  
3.  <span data-ttu-id="70194-223">Kies de actie **Planning**.</span><span class="sxs-lookup"><span data-stu-id="70194-223">Choose the **Planning** action.</span></span>  

     <span data-ttu-id="70194-224">De pagina **Orderplanning** wordt geopend in een weergave die altijd wordt gefilterd op de specifieke productievraag.</span><span class="sxs-lookup"><span data-stu-id="70194-224">The **Order Planning** page opens in a view that is always filtered on the specific production demand.</span></span> <span data-ttu-id="70194-225">De verkoopvraag wordt niet weergegeven.</span><span class="sxs-lookup"><span data-stu-id="70194-225">Sales demand is not displayed.</span></span> <span data-ttu-id="70194-226">U moet eerst een planning berekenen voordat een nieuwe vraag wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="70194-226">You must calculate a plan before you can see any additional demand.</span></span>  

4.  <span data-ttu-id="70194-227">Kies de actie **Plan berekenen**.</span><span class="sxs-lookup"><span data-stu-id="70194-227">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="70194-228">U ziet dat er vier nieuwe productieorders verschijnen voor de niet-geplande productievraag op basis van order **101001.**</span><span class="sxs-lookup"><span data-stu-id="70194-228">Notice that four new production orders appear as unplanned production demand derived from order **101001**.</span></span> <span data-ttu-id="70194-229">De nieuwe regels geven de nieuwe productievraag weer voor de subassemblages die moeten worden gemaakt om de order te produceren.</span><span class="sxs-lookup"><span data-stu-id="70194-229">The new lines represent new production demand from the subassemblies that must be created to produce the order.</span></span>  

5.  <span data-ttu-id="70194-230">Kies de actie **Alles uitvouwen** om een overzicht te krijgen van de volledige productievraag voor de productieorders.</span><span class="sxs-lookup"><span data-stu-id="70194-230">Choose the **Expand All** action to get an overview of all the production demand for the production orders.</span></span>  

     <span data-ttu-id="70194-231">Als u aanvullende informatie over de vraagregels wilt verstrekken, kunt u de velden **Aantal vraag** en **Beschikbaar aantal vraag** toevoegen aan uw weergave.</span><span class="sxs-lookup"><span data-stu-id="70194-231">To provide additional information about the demand lines, you may want to add the **Demand Quantity** and **Demand Qty. Available** fields to your view.</span></span>  

     <span data-ttu-id="70194-232">U moet nu tien stuks van elk onderdeel leveren.</span><span class="sxs-lookup"><span data-stu-id="70194-232">Now you must supply ten of each component.</span></span>  

     <span data-ttu-id="70194-233">Houd er rekening mee dat vier van de vraagregels aanvullingsmethode Prod.-order hebben.</span><span class="sxs-lookup"><span data-stu-id="70194-233">Note that four of the demand lines have replenishment system Prod. Order.</span></span> <span data-ttu-id="70194-234">Deze vier halffabrikaten vertegenwoordigen het tweede productniveau van de fiets.</span><span class="sxs-lookup"><span data-stu-id="70194-234">These four subassemblies represent the second product level of the bicycle.</span></span>  

     <span data-ttu-id="70194-235">De standaardinstellingen voor aanvulling zijn al ingevuld en u kunt de orders gaan maken.</span><span class="sxs-lookup"><span data-stu-id="70194-235">The default replenishment settings are already filled in and you can proceed to make orders.</span></span>  

6.  <span data-ttu-id="70194-236">Kies de actie **Orders maken**.</span><span class="sxs-lookup"><span data-stu-id="70194-236">Choose the **Make Orders** action.</span></span>  

     <span data-ttu-id="70194-237">Lees, voordat u de knop **OK** kiest, de tekst op het sneltabblad **Orderplanning**.</span><span class="sxs-lookup"><span data-stu-id="70194-237">Before you choose the **OK** button, notice the text on the **Order Planning** FastTab.</span></span> <span data-ttu-id="70194-238">Deze tekst is belangrijk omdat u weet dat de productstructuur van de fiets een aantal geproduceerde onderdelen (subassemblages) bevat die in de vraag worden opgenomen wanneer u deze productieorder maakt.</span><span class="sxs-lookup"><span data-stu-id="70194-238">This text is important because you know that the bicycle has several produced components, subassemblies, in its product structure that might be in demand when you create this production order.</span></span>  

7.  <span data-ttu-id="70194-239">Kies op de pagina **Orders voor voorzieningen maken** in het veld **Orders maken voor** de optie **Alle regels** en kies vervolgens de knop **OK** om productieorders te maken voor het tweede productniveau van de order.</span><span class="sxs-lookup"><span data-stu-id="70194-239">On the **Make Supply Order** page, in the **Make Orders for** field, choose the **All Lines** option, and then choose the **OK** button to create production orders for the second product level of the order.</span></span>  

     <span data-ttu-id="70194-240">U ziet dat de hoogste productievraag voor productieorder 101001 niet meer bestaat.</span><span class="sxs-lookup"><span data-stu-id="70194-240">Note that the top-level production demand for production order 101001 no longer exists.</span></span> <span data-ttu-id="70194-241">Dat betekent dat de aanvankelijke productievraag voor subassemblages nu is ingepland.</span><span class="sxs-lookup"><span data-stu-id="70194-241">This means that the initial production demand for subassemblies has been planned for.</span></span>  

     <span data-ttu-id="70194-242">Bereken op de pagina **Orderplanning** nogmaals de planning om de fietsstructuur te plannen.</span><span class="sxs-lookup"><span data-stu-id="70194-242">On the **Order Planning** page, you calculate a plan again in order to plan the bicycle structure.</span></span>  

8.  <span data-ttu-id="70194-243">Kies de actie **Planning berekenen** om de planning opnieuw te berekenen volgens de instructies uit de Help-tekst.</span><span class="sxs-lookup"><span data-stu-id="70194-243">Choose the **Calculate Plan** action to recalculate the plan as instructed by the embedded Help text.</span></span>  

     <span data-ttu-id="70194-244">De twee nieuwe regels geven de aanvullende productievraag aan die is afgeleid van de subassemblages die in de vorige stappen zijn gepland.</span><span class="sxs-lookup"><span data-stu-id="70194-244">The two new lines represent additional production demand derived from the subassemblies planned in the previous steps.</span></span> <span data-ttu-id="70194-245">Er wordt aangegeven dat u twee productieorders maakt voor de wielnaven, een voor 10 voornaven en een voor 10 achternaven.</span><span class="sxs-lookup"><span data-stu-id="70194-245">It is suggested that you make two production orders to supply the wheel hubs, one for 10 front hubs and one for 10 back hubs.</span></span>  

9. <span data-ttu-id="70194-246">Kies de actie **Alles uitvouwen** om een overzicht te krijgen van de twee productieorders.</span><span class="sxs-lookup"><span data-stu-id="70194-246">Choose the **Expand All** action to get an overview of all the demand for the two production orders.</span></span>  

     <span data-ttu-id="70194-247">Het voorgestelde voorzieningsplan geeft aan dat er in totaal vier inkooporders worden gemaakt voor de onderdelen.</span><span class="sxs-lookup"><span data-stu-id="70194-247">The suggested supply plan indicates that a total of four purchase orders will be created for the components.</span></span> <span data-ttu-id="70194-248">U besluit de voorgestelde orders te maken.</span><span class="sxs-lookup"><span data-stu-id="70194-248">You decide to make the proposed orders.</span></span>  

10. <span data-ttu-id="70194-249">Kies de actie **Orders maken**.</span><span class="sxs-lookup"><span data-stu-id="70194-249">Choose the **Make Orders** action.</span></span>  
11. <span data-ttu-id="70194-250">Selecteer in het veld **Orders maken voor** de optie **Alle regels** en kies vervolgens de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="70194-250">In the **Make Orders for** field, select the **All Lines** option, and then choose the **OK** button.</span></span> <span data-ttu-id="70194-251">Controleer of er een aanvullende vraag bestaat voor de productie van het hoofdartikel, de fiets (verkocht op verkooporder 1001).</span><span class="sxs-lookup"><span data-stu-id="70194-251">Check if additional demand exists for the production of the parent item, the bicycle, which is being sold on sales order 1001.</span></span>  
12. <span data-ttu-id="70194-252">Kies de actie **Plan berekenen**.</span><span class="sxs-lookup"><span data-stu-id="70194-252">Choose the **Calculate Plan** action.</span></span>  

     <span data-ttu-id="70194-253">Het bericht geeft aan dat nu in alle vereiste artikelen is voorzien.</span><span class="sxs-lookup"><span data-stu-id="70194-253">The message indicates that all required items are now supplied.</span></span> <span data-ttu-id="70194-254">Controleer de vast gepland productieorders die worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="70194-254">Verify the firm planned production orders that are created.</span></span>  

13. <span data-ttu-id="70194-255">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vast geplande productieorders** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="70194-255">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  

     <span data-ttu-id="70194-256">Bekijk op de pagina **Vast geplande productieorders** hoe de begin- en eindtijden van afzonderlijke orders nu zijn gepland volgens de productstructuur.</span><span class="sxs-lookup"><span data-stu-id="70194-256">On the **Firm Planned Prod. Orders** page review how start times and end times of individual orders are scheduled according to the product structure.</span></span> <span data-ttu-id="70194-257">De onderdelen op het laagste niveau worden het eerst geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="70194-257">The lowest-level components are produced first.</span></span> <span data-ttu-id="70194-258">Daarom moet u orders met meerdere niveaus plannen zoals is gedemonstreerd in deze planningswerkstroom.</span><span class="sxs-lookup"><span data-stu-id="70194-258">Therefore, you must plan multilevel orders as demonstrated in this planning workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="70194-259">Zie ook</span><span class="sxs-lookup"><span data-stu-id="70194-259">See Also</span></span>  
 <span data-ttu-id="70194-260">[Procedures voor bedrijfsprocessen](walkthrough-business-process-walkthroughs.md) </span><span class="sxs-lookup"><span data-stu-id="70194-260">[Business Process Walkthroughs](walkthrough-business-process-walkthroughs.md) </span></span>  
 [<span data-ttu-id="70194-261">Procedure: Goederen automatisch plannen</span><span class="sxs-lookup"><span data-stu-id="70194-261">Walkthrough: Planning Supplies Automatically</span></span>](walkthrough-planning-supplies-automatically.md)
