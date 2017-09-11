---
title: Artikelen overbrengen tussen magazijnvestigingen| Microsoft Docs
description: Beschrijft hoe u voorraad verplaatst van de ene plaats of magazijn naar een andere, met het herindelingsdagboek of met transferorders.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d54b75240cb0a2dddcfabc488a18e0bf9635f82c
ms.contentlocale: nl-be
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-transfer-inventory-between-locations"></a><span data-ttu-id="2172d-103">Procedure: Voorraad overbrengen tussen vestigingen</span><span class="sxs-lookup"><span data-stu-id="2172d-103">How to: Transfer Inventory Between Locations</span></span>
<span data-ttu-id="2172d-104">U kunt voorraadartikelen tussen vestigingen overbrengen door transferorders te maken.</span><span class="sxs-lookup"><span data-stu-id="2172d-104">You can transfer inventory items between locations by creating transfer orders.</span></span> <span data-ttu-id="2172d-105">U kunt ook het artikelherindelingsdagboek gebruiken.</span><span class="sxs-lookup"><span data-stu-id="2172d-105">Alternatively, you can use the item reclassification journal.</span></span>

<span data-ttu-id="2172d-106">Met transferorders verzendt u de uitgaande transfer vanuit de ene vestiging en ontvangt u de inkomende transfer op de andere vestiging.</span><span class="sxs-lookup"><span data-stu-id="2172d-106">With transfer orders, you ship the outbound transfer from one location and receive the inbound transfer at the other location.</span></span> <span data-ttu-id="2172d-107">U kunt zo de desbetreffende magazijnactiviteiten beheren en u krijgt meer zekerheid dat voorraadaantallen correct worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="2172d-107">This allows you to manage the involved warehouse activities and provides more certainty that inventory quantities are updated correctly.</span></span>

<span data-ttu-id="2172d-108">Met het herindelingsdagboek hoeft u alleen de velden **Vestigingscode** en **Nieuwe vestigingscode** in te vullen.</span><span class="sxs-lookup"><span data-stu-id="2172d-108">With the reclassification journal, you simply fill in the **Location Code** and the **New Location Code** fields.</span></span> <span data-ttu-id="2172d-109">Als u het dagboek boekt, worden de artikelposten aangepast op de betreffende vestigingen.</span><span class="sxs-lookup"><span data-stu-id="2172d-109">When you post the journal, the item ledger entries are adjusted at the locations in question.</span></span> <span data-ttu-id="2172d-110">Met deze methode worden magazijnactiviteiten niet beheerd.</span><span class="sxs-lookup"><span data-stu-id="2172d-110">With this method, warehouse activities are not managed.</span></span>

> [!NOTE]  
>   <span data-ttu-id="2172d-111">Als u artikelen in uw voorraad hebt geregistreerd zonder vestigingscode, bijvoorbeeld van een tijdstip waarop u slechts één magazijn had, kunt u deze artikelen niet overbrengen met transferorders.</span><span class="sxs-lookup"><span data-stu-id="2172d-111">If you have items recorded in your inventory without a location code, for example from a time when you only had one warehouse, then you cannot transfer those items using transfer orders.</span></span> <span data-ttu-id="2172d-112">In plaats hiervan moet u het herindelingsdagboek gebruiken om de artikelen van een lege vestigingscode opnieuw in te delen voor een werkelijke vestigingscode.</span><span class="sxs-lookup"><span data-stu-id="2172d-112">Instead, you must use the reclassification journal to reclassify the items from a blank location code to an actual location code.</span></span>  <span data-ttu-id="2172d-113">Zie stap 3 in het gedeelte "Artikelen overbrengen met het artikelherindelingsdagboek" voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="2172d-113">For more information, see step 3 in the "To transfer items with the item reclassification journal" section.</span></span>

<span data-ttu-id="2172d-114">Als u artikelen wilt overbrengen, moeten locaties en transferroutes zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="2172d-114">To transfer items, locations and transfer routes must be set up.</span></span> <span data-ttu-id="2172d-115">Zie voor meer informatie [Procedure: Vestigingen instellen](inventory-how-setup-locations.md).</span><span class="sxs-lookup"><span data-stu-id="2172d-115">For more information, see [How to: Set Up Locations](inventory-how-setup-locations.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="2172d-116">Deze functionaliteit vereist dat uw ervaring is ingesteld op **Pakket**.</span><span class="sxs-lookup"><span data-stu-id="2172d-116">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="2172d-117">Zie voor meer informatie [Uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-ervaring aanpassen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="2172d-117">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-transfer-items-with-a-transfer-order"></a><span data-ttu-id="2172d-118">Artikelen overbrengen met een transferorder</span><span class="sxs-lookup"><span data-stu-id="2172d-118">To transfer items with a transfer order</span></span>
1. <span data-ttu-id="2172d-119">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Transferorders** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="2172d-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="2172d-120">Vul in het venster **Transferorder** indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="2172d-120">In the **Transfer Order** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
>   <span data-ttu-id="2172d-121">Als u de velden **Transitcode**, **Expediteur** en **Servicecode expediteur** hebt ingevuld in het venster **Transferroutegegevens**</span><span class="sxs-lookup"><span data-stu-id="2172d-121">If you have filled in the **In-Transit Code**, **Shipping Agent Code**, and **Shipping Agent Service** fields in the **Trans. Route Spec.**</span></span> <span data-ttu-id="2172d-122">toen u de transferroute instelde, worden de corresponderende velden op de transferorder automatisch ingevuld.</span><span class="sxs-lookup"><span data-stu-id="2172d-122">window when you set up the transfer route, then the corresponding fields on the transfer order are filled in automatically.</span></span>

    <span data-ttu-id="2172d-123">Wanneer u het veld **Servicecode expediteur** invult, wordt de ontvangstdatum in de ontvangstvestiging berekend door de verzendtijd van de expediteurservice op te tellen bij de verzenddatum.</span><span class="sxs-lookup"><span data-stu-id="2172d-123">When you fill in the **Shipping Agent Service** field, the receipt date at the transfer-to location is calculated by adding the shipping time of the shipping agent service to the shipment date.</span></span>

    <span data-ttu-id="2172d-124">Als magazijnmedewerker op de aflevervestiging gaat u verder om de artikelen te verzenden.</span><span class="sxs-lookup"><span data-stu-id="2172d-124">As a warehouse worker at the transfer-from location, proceed to ship the items.</span></span>
3. <span data-ttu-id="2172d-125">Kies de actie **Boeken**, kies de optie **Verzenden** en kies vervolgens de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="2172d-125">Choose the **Post** action, choose the **Ship** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="2172d-126">De artikelen zijn nu in transit tussen de opgegeven vestigingen volgens de opgegeven transferroute.</span><span class="sxs-lookup"><span data-stu-id="2172d-126">The items are now in transit between the specified locations, according to the specifies transfer route.</span></span>

    <span data-ttu-id="2172d-127">Als magazijnmedewerker op de aflevervestiging gaat u verder om de artikelen te ontvangen.</span><span class="sxs-lookup"><span data-stu-id="2172d-127">As a warehouse worker at the transfer-from location, proceed to receive the items.</span></span>
4. <span data-ttu-id="2172d-128">Kies de actie **Boeken**, kies de optie **Ontvangen** en kies vervolgens de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="2172d-128">Choose the **Post** action, choose the **Receive** option, and then choose the **OK** button.</span></span>

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a><span data-ttu-id="2172d-129">Artikelen overbrengen met het artikelherindelingsdagboek</span><span class="sxs-lookup"><span data-stu-id="2172d-129">To transfer items with the item reclassification journal</span></span>
1. <span data-ttu-id="2172d-130">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikelherindelingsdagboeken** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="2172d-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Reclass. Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="2172d-131">Vul in het venster **Artikelherindelingsdagboeken** indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="2172d-131">In the **Item Reclass. Journal** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="2172d-132">Voer in het veld **Vestiging** de vestiging in waar de artikelen momenteel zijn opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="2172d-132">In the **Location Code** field, enter the location where the items are currently stored.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="2172d-133">Als u artikelen wilt overbrengen die geen vestigingscode hebben, laat u het veld **Vestiging** leeg.</span><span class="sxs-lookup"><span data-stu-id="2172d-133">To transfer items that have no location code, leave the **Location Code** field blank.</span></span>
4. <span data-ttu-id="2172d-134">Voer in het veld **Nieuwe vestiging** de vestiging in waarnaar u de artikelen wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="2172d-134">In the **New Location Code** field, enter the location that you want to transfer the items to.</span></span>
5. <span data-ttu-id="2172d-135">Kies de actie **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="2172d-135">Choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="2172d-136">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2172d-136">See Also</span></span>
[<span data-ttu-id="2172d-137">Voorraad beheren</span><span class="sxs-lookup"><span data-stu-id="2172d-137">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="2172d-138">Procedure: Vestigingen instellen</span><span class="sxs-lookup"><span data-stu-id="2172d-138">How to: Set Up Locations</span></span>](inventory-how-setup-locations.md)  
[<span data-ttu-id="2172d-139">Toeleveringsketen</span><span class="sxs-lookup"><span data-stu-id="2172d-139">Supply Chain</span></span>](madeira-supply-chain.md)  
<span data-ttu-id="2172d-140">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2172d-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="2172d-141">[Uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-ervaring aanpassen](ui-experiences.md)</span><span class="sxs-lookup"><span data-stu-id="2172d-141">[Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md)</span></span>  
[<span data-ttu-id="2172d-142">Algemene bedrijfsfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="2172d-142">General Business Functionality</span></span>](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
