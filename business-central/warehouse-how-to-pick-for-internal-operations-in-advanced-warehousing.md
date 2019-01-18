---
title: Picken voor interne bewerkingen in geavanceerde magazijnconfiguraties | Microsoft Docs
description: In geavanceerde magazijnconfiguraties waarbij de locatie is ingesteld voor het gebruik van picken en verzending, kunt u componenten voor productie- en assemblageactiviteiten kiezen via de pagina **Magazijnpick**.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 7e4a489b49c5a97cd0df077544a51c6ba73a4a85
ms.contentlocale: nl-be
ms.lasthandoff: 11/26/2018

---
# <a name="pick-for-assembly-or-production-in-advanced-warehouse-configurations"></a><span data-ttu-id="20222-103">Picken voor assemblage of productie in geavanceerde magazijnconfiguraties</span><span class="sxs-lookup"><span data-stu-id="20222-103">Pick for Assembly or Production in Advanced Warehouse Configurations</span></span>
<span data-ttu-id="20222-104">In geavanceerde magazijnconfiguraties waarbij de locatie is ingesteld voor het gebruik van picken en verzending, kunt u componenten voor productie- en assemblageactiviteiten kiezen via de pagina **Magazijnpick**.</span><span class="sxs-lookup"><span data-stu-id="20222-104">In advanced warehouse configurations where the location is set up to use picking as well as shipping, you can pick components for production and assembly activities with the **Warehouse Pick** page.</span></span>  

<span data-ttu-id="20222-105">U kunt tevens de pagina **Verplaatsingsvoorstel** gebruiken voor ad hoc verplaatsing van artikelen tussen opslaglocaties, dat wil zeggen, zonder verwijzing naar een brondocument.</span><span class="sxs-lookup"><span data-stu-id="20222-105">Alternatively, you can use the **Movement Worksheet** page to move items between bins ad hoc, meaning without reference to a source document.</span></span> <span data-ttu-id="20222-106">Zie [Artikelen verplaatsen in geavanceerde magazijnconfiguraties](warehouse-how-to-move-items-in-advanced-warehousing.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="20222-106">For more information, see [Move Items in advanced warehouse configurations](warehouse-how-to-move-items-in-advanced-warehousing.md).</span></span>  

<span data-ttu-id="20222-107">Zie [Onderdelen verplaatsen naar een bewerkingsgebied in standaardmagazijnconfiguraties](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md) voor informatie over het picken van artikelen voor interne bewerkingen in standaardmagazijnvestigingen die alleen zijn ingesteld voor picken.</span><span class="sxs-lookup"><span data-stu-id="20222-107">For information about picking items for internal operations in basic warehouse locations that are set up for picking only, see [Move Components to an Operation Area in Basic Warehouse Configurations](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).</span></span>  

<span data-ttu-id="20222-108">Een magazijn-pickdocument kan niet van het begin af gemaakt worden, omdat een pick-activiteit altijd onderdeel is van een werkstroom, zowel bij een pull- als bij een push-scenario.</span><span class="sxs-lookup"><span data-stu-id="20222-108">You cannot create a warehouse pick document from scratch because a pick activity is always part of a workflow, either in a pull or a push scenario.</span></span>  

<span data-ttu-id="20222-109">Bij een push-scenario kan een magazijn-pickdocument gemaakt worden door **Mag. Pick maken** in het brondocument te selecteren, zoals een vrijgegeven assemblageorder of een verzending uit het magazijn.</span><span class="sxs-lookup"><span data-stu-id="20222-109">You can create the warehouse pick document in a push fashion by selecting **Create Whse. Pick** on the source document, such as a released assembly order or warehouse shipment.</span></span> <span data-ttu-id="20222-110">Zie voor meer informatie [Artikelen picken met een magazijnpick](warehouse-how-to-pick-items-for-warehouse-shipment.md).</span><span class="sxs-lookup"><span data-stu-id="20222-110">For more information, see [Pick Items with Warehouse Picks](warehouse-how-to-pick-items-for-warehouse-shipment.md).</span></span>  

<span data-ttu-id="20222-111">Tevens kunt u bij een pull-scenario een magazijnpickdocument maken door de pagina **Pickvoorstel** te gebruiken om pickverzoeken, voor zowel verzending als voor interne doeleinden, vast te stellen en vervolgens de benodigde magazijnpickdocumenten te maken.</span><span class="sxs-lookup"><span data-stu-id="20222-111">Alternatively, you can create the warehouse pick document in a pull fashion by using the **Pick Worksheet** page to detect pick requests, both for shipment and internal operations, and then create the required warehouse pick documents.</span></span>  

<span data-ttu-id="20222-112">De volgende procedure beschrijft een pull-scenario, waarbij u onderdelen voor een vrijgegeven productieorder pickt met behulp van de pagina **Werkblad Pick**.</span><span class="sxs-lookup"><span data-stu-id="20222-112">The following procedure explains a pull scenario where you pick components for a released production order through the **Pick Worksheet** page.</span></span> <span data-ttu-id="20222-113">De procedure geldt ook voor een assemblageorder.</span><span class="sxs-lookup"><span data-stu-id="20222-113">The procedure also applies for an assembly order.</span></span>  

<span data-ttu-id="20222-114">Als u een pick-verzoek wilt maken, bij zowel een pull- als een push-scenario, moeten de betreffende brondocumenten vrijgegeven worden.</span><span class="sxs-lookup"><span data-stu-id="20222-114">To create pick requests, both for pull and for push scenarios, the source documents in question must be released.</span></span> <span data-ttu-id="20222-115">Voor interne doeleinden kunnen brondocumenten op de volgende manieren vrijgegeven worden.</span><span class="sxs-lookup"><span data-stu-id="20222-115">Release source documents for internal operations in the following ways.</span></span>  

|<span data-ttu-id="20222-116">Brondocument</span><span class="sxs-lookup"><span data-stu-id="20222-116">Source Document</span></span>|<span data-ttu-id="20222-117">Vrijgavemethode</span><span class="sxs-lookup"><span data-stu-id="20222-117">Release Method</span></span>|  
|---------------------|--------------------|  
|<span data-ttu-id="20222-118">Productieorder</span><span class="sxs-lookup"><span data-stu-id="20222-118">Production Order</span></span>|<span data-ttu-id="20222-119">Wijzig de ordersoort in vrijgegeven productieorder.</span><span class="sxs-lookup"><span data-stu-id="20222-119">Change order type to released production order.</span></span>|  
|<span data-ttu-id="20222-120">Assemblageorder</span><span class="sxs-lookup"><span data-stu-id="20222-120">Assembly Order</span></span>|<span data-ttu-id="20222-121">Status wijzigen in Vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="20222-121">Change status to Released.</span></span>|  

## <a name="to-pick-components-using-the-pick-worksheet"></a><span data-ttu-id="20222-122">Onderdelen picken op basis van het pickvoorstel</span><span class="sxs-lookup"><span data-stu-id="20222-122">To pick components using the pick worksheet</span></span>  
1.  <span data-ttu-id="20222-123">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Pickvoorstel** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="20222-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Pick Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="20222-124">Kies de actie **Magazijndocumenten ophalen** en selecteer vervolgens de onderdeelregels van de vrijgegeven productieorder.</span><span class="sxs-lookup"><span data-stu-id="20222-124">Choose the **Get Warehouse Documents** action, and then select the component lines from the released production order.</span></span>  
3.  <span data-ttu-id="20222-125">Inspecteer en sorteer de regels om een efficiënte pickronde samen te stellen en combineer ze eventueel met andere voorstelregels zodat de werknemer zo min mogelijk tijd nodig heeft.</span><span class="sxs-lookup"><span data-stu-id="20222-125">Inspect the lines, sort them to ensure an efficient picking round, and combine them with other worksheet lines if necessary to make best use of employee time.</span></span>  
4.  <span data-ttu-id="20222-126">Kies de actie **Pick maken**.</span><span class="sxs-lookup"><span data-stu-id="20222-126">Choose the **Create Pick** action.</span></span>  
5.  <span data-ttu-id="20222-127">Bepaal hoe de magazijn-pickdocumenten gemaakt moeten worden en hoe de pickregels gesorteerd moeten worden door de velden op de pagina **Pick maken** in te vullen.</span><span class="sxs-lookup"><span data-stu-id="20222-127">Define how to create the warehouse pick documents and how to sort pick lines by filling fields on the **Create Pick** page.</span></span>  
6.  <span data-ttu-id="20222-128">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="20222-128">Choose the **OK** button.</span></span> <span data-ttu-id="20222-129">Magazijn-pickdocumenten worden gemaakt met een pickregel voor ieder onderdeel dat voor de interne activiteit benodigd is.</span><span class="sxs-lookup"><span data-stu-id="20222-129">Warehouse pick documents are created with pick lines for each component that is required in the internal operation.</span></span>  

<span data-ttu-id="20222-130">Indien het gebied voor interne activiteit, zoals een productie-shopfloor, een standaardopslaglocatie heeft voor het plaatsen van onderdelen die voor de activiteit benodigd zijn, wordt de code van deze opslaglocatie ingevoerd in de Plaatsen-regels in het magazijnpickdocument, zodat de magazijnmedewerkers weten waar de artikelen geplaatst moeten worden.</span><span class="sxs-lookup"><span data-stu-id="20222-130">If the internal operation area, such as a production shop floor, is set up with a default bin for placement of components to be used in the operation, then that bin code is inserted in the Place lines on the warehouse pick document to instruct warehouse workers where to place the items.</span></span> <span data-ttu-id="20222-131">Zie voor meer informatie het veld **Code verbruikslocatie** of **Opslaglocatie Naar-assemblage**.</span><span class="sxs-lookup"><span data-stu-id="20222-131">For more information, see the **To-Production Bin Code** or the **To-Assembly Bin Code** field.</span></span>

## <a name="filling-the-consumption-bin"></a><span data-ttu-id="20222-132">De verbruiksopslaglocatie vullen</span><span class="sxs-lookup"><span data-stu-id="20222-132">Filling the Consumption Bin</span></span>
<span data-ttu-id="20222-133">In dit stroomdiagram wordt weergegeven hoe het veld **Opslaglocatie** op de productieordercomponentregels wordt ingevuld op basis van uw locatie-instellingen.</span><span class="sxs-lookup"><span data-stu-id="20222-133">This flow chart shows how the **Bin Code** field on production order component lines is filled according to your location setup.</span></span>

<span data-ttu-id="20222-134">![Diagram van opslaglocatiestroom](media/binflow.png "Opslaglocatiestroom")</span><span class="sxs-lookup"><span data-stu-id="20222-134">![Bin flow chart](media/binflow.png "BinFlow")</span></span>  

## <a name="see-also"></a><span data-ttu-id="20222-135">Zie ook</span><span class="sxs-lookup"><span data-stu-id="20222-135">See Also</span></span>
[<span data-ttu-id="20222-136">Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="20222-136">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="20222-137">Voorraad</span><span class="sxs-lookup"><span data-stu-id="20222-137">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="20222-138">[Magazijnbeheer instellen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="20222-138">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="20222-139">[Assemblagebeheer](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="20222-139">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="20222-140">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="20222-140">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="20222-141">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="20222-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

