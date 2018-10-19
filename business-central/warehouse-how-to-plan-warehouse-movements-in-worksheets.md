---
title: Plannen van magazijnverplaatsingen in werkbladen | Microsoft Docs
description: Met de functie voor de opslaglocatieaanvulling kunt u verplaatsingen plannen in het voorstel. U kunt de regels die u wilt instellen als verplaatsingsinstructies echter ook handmatig plannen.
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
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: d66ad263235d7f123f731263b0f13a009a1e20fd
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="plan-warehouse-movements-in-worksheets"></a><span data-ttu-id="ab6f3-103">Plannen van magazijnverplaatsingen in werkbladen</span><span class="sxs-lookup"><span data-stu-id="ab6f3-103">Plan Warehouse Movements in Worksheets</span></span>
<span data-ttu-id="ab6f3-104">Met de functie voor de opslaglocatieaanvulling kunt u verplaatsingen plannen in het voorstel. U kunt de regels die u wilt instellen als verplaatsingsinstructies echter ook handmatig plannen.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-104">Plan movements in the worksheet using a bin replenishment function or manually planning the lines that you want to create as movement instructions.</span></span>  

## <a name="to-calculate-a-replenishment-movement"></a><span data-ttu-id="ab6f3-105">U kunt als volgt aanvullingsverplaatsingen berekenen</span><span class="sxs-lookup"><span data-stu-id="ab6f3-105">To calculate a replenishment movement</span></span>  
<span data-ttu-id="ab6f3-106">Naarmate meer artikelen worden verzonden naar klanten, bevatten de opslaglocaties met de hoogste classificatie steeds minder artikelen.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-106">As the warehouse ships items out to customers, the bins with the highest bin rankings contain fewer and fewer items.</span></span> <span data-ttu-id="ab6f3-107">Als u deze opslaglocaties met de hoogste classificatie wilt vullen, voert u de functie **Opslagloc.-aanvulling berekenen** uit in het venster **Verplaatsingsvoorstel**</span><span class="sxs-lookup"><span data-stu-id="ab6f3-107">To fill up these high-ranking pick bins with items from other bins, run the **Calculate Bin Replenishment** function in the **Movement Worksheet** window</span></span>

1.  <span data-ttu-id="ab6f3-108">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verplaatsingsvoorstel** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ab6f3-109">Kies de actie **Opslaglocatieaanvulling berekenen**.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-109">Choose the **Calculate Bin Replenishment** action.</span></span>  

    [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="ab6f3-110">maakt regels die precies aangeven hoe u artikelen moet verplaatsen van laag- naar hooggeclassificeerde opslaglocaties.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-110">creates lines that indicate precisely how you should move items from the low-ranking bins to the higher-ranking bins.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="ab6f3-111">Een verplaatsing volgens FEFO wordt voorgesteld wanneer u de functie **Verplaatsing maken** activeert indien voor een artikel aan de de volgende voorwaarden wordt voldaan:</span><span class="sxs-lookup"><span data-stu-id="ab6f3-111">A movement is suggested according to FEFO when you activate the **Create Movement** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="ab6f3-112">Het artikel heeft een vervaldatum.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-112">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="ab6f3-113">Op de vestigingskaart is het selectievakje **Picken volgens FEFO** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-113">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="ab6f3-114">Het selectievakje op de vestigingskaart **Opslaglocatie verplicht** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-114">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="ab6f3-115">De velden **Van zone** en **Van opslaglocatie** zijn leeg.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-115">The **From Zone** and **From Bin** fields are blank.</span></span>  

    <span data-ttu-id="ab6f3-116">Zie voor meer informatie [Picken op basis van FEFO](warehouse-picking-by-fefo.md).</span><span class="sxs-lookup"><span data-stu-id="ab6f3-116">For more information, see [Picking by FEFO](warehouse-picking-by-fefo.md).</span></span>  

3.  <span data-ttu-id="ab6f3-117">Bekijk en wijzig de regels indien nodig. U kunt ook regels verwijderen als er onvoldoende tijd is om alle regels uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-117">Look through the lines and change them if necessary, or delete some of them if there is not enough time to perform them all.</span></span>  
4.  <span data-ttu-id="ab6f3-118">Kies de actie **Verplaatsing maken** om een instructie te maken voor de medewerkers in het magazijn.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-118">Choose the **Create Movement** action to make a warehouse instruction for action by warehouse employees.</span></span>  

## <a name="to-move-the-entire-contents-of-one-or-more-bins-by-using-the-get-bin-content-function"></a><span data-ttu-id="ab6f3-119">U kunt de volledige inhoud van een of meer opslaglocaties verplaatsen met de functie Opslaglocatie-inhoud ophalen</span><span class="sxs-lookup"><span data-stu-id="ab6f3-119">To move the entire contents of one or more bins by using the Get Bin Content function</span></span>  
<span data-ttu-id="ab6f3-120">Met het verplaatsingsvoorstel kunt u ook andere verplaatsingen van magazijnartikelen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-120">You can also use the movement worksheet to plan other movement of inventory within the warehouse.</span></span> <span data-ttu-id="ab6f3-121">Als u bijvoorbeeld artikelen in een opslaglocatie wilt plaatsen voor kwaliteitscontrole, kunt u deze actie met het voorstel plannen en vervolgens een verplaatsing maken met instructies voor een werknemer.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-121">For example, when you want to place items in a bin for quality control, you can use the movement worksheet to plan this action and then create a movement to make instructions for an employee.</span></span>  

1.  <span data-ttu-id="ab6f3-122">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verplaatsingsvoorstel** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ab6f3-123">Kies de actie **Opslaglocatie-inhoud ophalen**.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-123">Choose the **Get Bin Content** action.</span></span> <span data-ttu-id="ab6f3-124">Gebruik het aanvraagvenster om te filteren op de opslaglocaties en artikelen die op de verplaatsingsvoorstelregels moeten verschijnen.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-124">Use the request window to filter which bins and items you want to appear on the movement worksheet lines.</span></span>  
3.  <span data-ttu-id="ab6f3-125">Vul de relevante velden in het aanvraagvenster voor de batchverwerking in.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-125">Fill in the relevant fields in the batch job request window.</span></span> <span data-ttu-id="ab6f3-126">Als u bijvoorbeeld de opslaglocatie-inhoud van alle opslaglocaties in een bepaalde zone van de vestiging wilt weergeven, vult u het veld **Zone** in.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-126">For example, if you want to see the bin content of all the bins in a certain zone at the location, fill in the **Zone Code** field.</span></span> <span data-ttu-id="ab6f3-127">Als u regels wilt ophalen voor elke opslaglocatie met een bepaald artikel, vult u het veld **Artikelnr.** in.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-127">If you want to retrieve lines for each bin that contains a particular item, fill in the **Item No.** field.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="ab6f3-128">U kunt artikelen niet handmatig van of naar een opslaglocatie van het soort Ontvangen verplaatsen, omdat artikelen in een dergelijke opslaglocatie moeten worden geregistreerd als opgeslagen voordat ze deel uitmaken van de beschikbare voorraad.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-128">You cannot manually move items in or out of a bin of bin type RECEIVE, because items that are in a RECEIVE-type bin must be registered as being put away before they are part of available inventory.</span></span>  

4.  <span data-ttu-id="ab6f3-129">Als u een groot aantal regels ophaalt, klikt u op **Sorteren** om een sortering te selecteren voor de regels in het voorstel. Klik vervolgens op **OK**.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-129">If you are retrieving many lines, choose **Sort** to select a sorting method to determine the order the lines will appear in the worksheet, and then choose the **OK** button.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="ab6f3-130">Verplaatsingsregels worden opgehaald volgens FEFO wanneer u de functie **Opslaglocatie-inhoud ophalen** activeert indien voor een artikel aan de volgende voorwaarden wordt voldaan:</span><span class="sxs-lookup"><span data-stu-id="ab6f3-130">Movement lines are retrieved according to FEFO when you activate the **Get Bin Content** function if the following conditions are met for an item:</span></span>  
    >   
    >  -   <span data-ttu-id="ab6f3-131">Het artikel heeft een vervaldatum.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-131">The item has an expiration date.</span></span>  
    > -   <span data-ttu-id="ab6f3-132">Op de vestigingskaart is het selectievakje **Picken volgens FEFO** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-132">The **Pick According to FEFO** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="ab6f3-133">Het selectievakje op de vestigingskaart **Opslaglocatie verplicht** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-133">The **Bin Mandatory** check box on the location card is selected.</span></span>  
    > -   <span data-ttu-id="ab6f3-134">De velden **Van zone** en **Van opslaglocatie** zijn leeg.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-134">The **From Zone** and **From Bin** fields are blank.</span></span>  

5.  <span data-ttu-id="ab6f3-135">Maak de gewenste wijzigingen in een aantal van de opgehaalde regels.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-135">Complete some of the retrieved lines to reflect the changes you want to make.</span></span> <span data-ttu-id="ab6f3-136">U moet voor elk te verplaatsen artikel de velden **Artikelnr.**, **Van opslaglocatie**, **Naar opslaglocatie** en **Aantal** invullen.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-136">For each item that you want to move, you must fill in the **Item No.**, **From Bin Code**, **To Bin Code**, and **Quantity** fields.</span></span>  
6.  <span data-ttu-id="ab6f3-137">Verwijder de onvolledige regels waaruit u de informatie hebt overgenomen.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-137">Delete the incomplete lines that you used for information.</span></span>  
7.  <span data-ttu-id="ab6f3-138">Wanneer u in de verplaatsingsvoorstelregels precies hebt aangegeven hoe de verplaatsing moet worden uitgevoerd door de magazijnmedewerker, kiest u de actie **Verplaatsing maken** om de instructies voor de werknemer te maken.</span><span class="sxs-lookup"><span data-stu-id="ab6f3-138">Once the movement worksheet lines accurately reflect how the movement action should be carried out by the warehouse employee, choose the **Create Movement** action to create the instructions for the employee.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ab6f3-139">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ab6f3-139">See Also</span></span>  
[<span data-ttu-id="ab6f3-140">Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="ab6f3-140">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="ab6f3-141">Voorraad</span><span class="sxs-lookup"><span data-stu-id="ab6f3-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="ab6f3-142">[Magazijnbeheer instellen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="ab6f3-142">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="ab6f3-143">[Assemblagebeheer](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="ab6f3-143">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="ab6f3-144">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="ab6f3-144">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="ab6f3-145">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ab6f3-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

