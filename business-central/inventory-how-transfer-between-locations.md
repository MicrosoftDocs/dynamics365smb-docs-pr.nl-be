---
title: Artikelen overbrengen tussen magazijnvestigingen| Microsoft Docs
description: Beschrijft hoe u voorraad verplaatst van de ene plaats of magazijn naar een andere, met het herindelingsdagboek of met transferorders.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: move, warehouse
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f406a44a3d786c06ea1ac1e61d5b51bb97b67f12
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746153"
---
# <a name="transfer-inventory-between-locations"></a><span data-ttu-id="f65e3-103">Voorraad overbrengen tussen vestigingen</span><span class="sxs-lookup"><span data-stu-id="f65e3-103">Transfer Inventory Between Locations</span></span>
<span data-ttu-id="f65e3-104">U kunt voorraadartikelen tussen vestigingen overbrengen door transferorders te maken.</span><span class="sxs-lookup"><span data-stu-id="f65e3-104">You can transfer inventory items between locations by creating transfer orders.</span></span> <span data-ttu-id="f65e3-105">U kunt ook het artikelherindelingsdagboek gebruiken.</span><span class="sxs-lookup"><span data-stu-id="f65e3-105">Alternatively, you can use the item reclassification journal.</span></span>

<span data-ttu-id="f65e3-106">Met transferorders verzendt u de uitgaande transfer vanuit de ene vestiging en ontvangt u de inkomende transfer op de andere vestiging.</span><span class="sxs-lookup"><span data-stu-id="f65e3-106">With transfer orders, you ship the outbound transfer from one location and receive the inbound transfer at the other location.</span></span> <span data-ttu-id="f65e3-107">U kunt zo de desbetreffende magazijnactiviteiten beheren en u krijgt meer zekerheid dat voorraadaantallen correct worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="f65e3-107">This allows you to manage the involved warehouse activities and provides more certainty that inventory quantities are updated correctly.</span></span>

<span data-ttu-id="f65e3-108">Met het herindelingsdagboek hoeft u alleen de velden **Vestigingscode** en **Nieuwe vestigingscode** in te vullen.</span><span class="sxs-lookup"><span data-stu-id="f65e3-108">With the reclassification journal, you simply fill in the **Location Code** and the **New Location Code** fields.</span></span> <span data-ttu-id="f65e3-109">Als u het dagboek boekt, worden de artikelposten aangepast op de betreffende vestigingen.</span><span class="sxs-lookup"><span data-stu-id="f65e3-109">When you post the journal, the item ledger entries are adjusted at the locations in question.</span></span> <span data-ttu-id="f65e3-110">Met deze methode worden magazijnactiviteiten niet beheerd.</span><span class="sxs-lookup"><span data-stu-id="f65e3-110">With this method, warehouse activities are not managed.</span></span>

> [!NOTE]  
>   <span data-ttu-id="f65e3-111">Als u artikelen in uw voorraad hebt geregistreerd zonder vestigingscode, bijvoorbeeld van een tijdstip waarop u slechts één magazijn had, kunt u deze artikelen niet overbrengen met transferorders.</span><span class="sxs-lookup"><span data-stu-id="f65e3-111">If you have items recorded in your inventory without a location code, for example from a time when you only had one warehouse, then you cannot transfer those items using transfer orders.</span></span> <span data-ttu-id="f65e3-112">In plaats hiervan moet u het herindelingsdagboek gebruiken om de artikelen van een lege vestigingscode opnieuw in te delen voor een werkelijke vestigingscode.</span><span class="sxs-lookup"><span data-stu-id="f65e3-112">Instead, you must use the reclassification journal to reclassify the items from a blank location code to an actual location code.</span></span>  <span data-ttu-id="f65e3-113">Zie stap 3 in [Artikelen overbrengen met het artikelherindelingsdagboek](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f65e3-113">For more information, see step 3 in [To transfer items with the item reclassification journal](inventory-how-transfer-between-locations.md#to-transfer-items-with-the-item-reclassification-journal).</span></span>

<span data-ttu-id="f65e3-114">Als u artikelen wilt overbrengen, moeten locaties en transferroutes zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="f65e3-114">To transfer items, locations and transfer routes must be set up.</span></span> <span data-ttu-id="f65e3-115">Zie [Vestigingen instellen](inventory-how-setup-locations.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f65e3-115">For more information, see [Set Up Locations](inventory-how-setup-locations.md).</span></span>

## <a name="to-transfer-items-with-a-transfer-order"></a><span data-ttu-id="f65e3-116">Artikelen overbrengen met een transferorder</span><span class="sxs-lookup"><span data-stu-id="f65e3-116">To transfer items with a transfer order</span></span>
1. <span data-ttu-id="f65e3-117">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Transferorders** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="f65e3-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="f65e3-118">Vul in de koptekst van de pagina **Transferorder** de velden in zoals nodig.</span><span class="sxs-lookup"><span data-stu-id="f65e3-118">On the header of the **Transfer Order** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   <span data-ttu-id="f65e3-119">Als u tijdens het instellen van de transferroute tussen deze vestigingen de velden **Transitcode**, **Expediteur** en **Expediteurservice** op de pagina **Transferroutegegevens** hebt ingevuld, worden de bijbehorende velden op de transferorder automatisch ingevuld.</span><span class="sxs-lookup"><span data-stu-id="f65e3-119">If you have filled in the **In-Transit Code**, **Shipping Agent Code**, and **Shipping Agent Service** fields on the **Trans. Route Spec.** page when you set up the transfer route, then the corresponding fields on the transfer order are filled in automatically.</span></span>

    <span data-ttu-id="f65e3-120">Wanneer u het veld **Servicecode expediteur** invult, wordt de ontvangstdatum in de ontvangstvestiging berekend door de verzendtijd van de expediteurservice op te tellen bij de verzenddatum.</span><span class="sxs-lookup"><span data-stu-id="f65e3-120">When you fill in the **Shipping Agent Service** field, the receipt date at the transfer-to location is calculated by adding the shipping time of the shipping agent service to the shipment date.</span></span>

3. <span data-ttu-id="f65e3-121">Om de regels in te vullen, voert u ze handmatig in of kiest u een van de volgende opties onder de actie **Functies**:</span><span class="sxs-lookup"><span data-stu-id="f65e3-121">To fill in the lines, either enter them manually or choose one of the following options on the under the **Functions** action:</span></span>
    - <span data-ttu-id="f65e3-122">Kies de actie **Opslaglocatie-inhoud ophalen** om bestaande artikelen uit een specifieke opslaglocatie te selecteren.</span><span class="sxs-lookup"><span data-stu-id="f65e3-122">Choose the **Get Bin Content** action to select existing items from a specific bin at the location.</span></span>
    - <span data-ttu-id="f65e3-123">Kies de actie **Ontvangstregels ophalen** om artikelen te selecteren die net zijn aangekomen op de aflevervestiging.</span><span class="sxs-lookup"><span data-stu-id="f65e3-123">Choose the **Get Receipt Lines** to select items that have just arrived at the transfer-from location.</span></span>   

    <span data-ttu-id="f65e3-124">Als magazijnmedewerker op de aflevervestiging gaat u verder om de artikelen te verzenden.</span><span class="sxs-lookup"><span data-stu-id="f65e3-124">As a warehouse worker at the transfer-from location, proceed to ship the items.</span></span>
4. <span data-ttu-id="f65e3-125">Kies de actie **Boeken**, kies de optie **Verzenden** en kies vervolgens de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="f65e3-125">Choose the **Post** action, choose the **Ship** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="f65e3-126">De artikelen zijn nu in transit tussen de opgegeven vestigingen volgens de opgegeven transferroute.</span><span class="sxs-lookup"><span data-stu-id="f65e3-126">The items are now in transit between the specified locations, according to the specifies transfer route.</span></span>

    <span data-ttu-id="f65e3-127">Als magazijnmedewerker op de aflevervestiging gaat u verder om de artikelen te ontvangen.</span><span class="sxs-lookup"><span data-stu-id="f65e3-127">As a warehouse worker at the transfer-from location, proceed to receive the items.</span></span> <span data-ttu-id="f65e3-128">De tranferorderregels zijn dezelfde als bij verzending en kunnen niet worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="f65e3-128">The transfer order lines are the same as when shipped and cannot be edited.</span></span>
5. <span data-ttu-id="f65e3-129">Kies de actie **Boeken**, kies de optie **Ontvangen** en kies vervolgens de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="f65e3-129">Choose the **Post** action, choose the **Receive** option, and then choose the **OK** button.</span></span>

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a><span data-ttu-id="f65e3-130">Artikelen overbrengen met het artikelherindelingsdagboek</span><span class="sxs-lookup"><span data-stu-id="f65e3-130">To transfer items with the item reclassification journal</span></span>
1. <span data-ttu-id="f65e3-131">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelherindelingsdagboeken** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="f65e3-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Reclass. Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="f65e3-132">Vul op de pagina **Artikelherindelingsdagboeken** indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="f65e3-132">On the **Item Reclass. Journal** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="f65e3-133">Voer in het veld **Vestiging** de vestiging in waar de artikelen momenteel zijn opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="f65e3-133">In the **Location Code** field, enter the location where the items are currently stored.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="f65e3-134">Als u artikelen wilt overbrengen die geen vestigingscode hebben, laat u het veld **Vestiging** leeg.</span><span class="sxs-lookup"><span data-stu-id="f65e3-134">To transfer items that have no location code, leave the **Location Code** field blank.</span></span>
4. <span data-ttu-id="f65e3-135">Voer in het veld **Nieuwe vestiging** de vestiging in waarnaar u de artikelen wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="f65e3-135">In the **New Location Code** field, enter the location that you want to transfer the items to.</span></span>
5. <span data-ttu-id="f65e3-136">Kies de actie **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="f65e3-136">Choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="f65e3-137">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f65e3-137">See Also</span></span>
[<span data-ttu-id="f65e3-138">Voorraad beheren</span><span class="sxs-lookup"><span data-stu-id="f65e3-138">Manage Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="f65e3-139">Vestigingen instellen</span><span class="sxs-lookup"><span data-stu-id="f65e3-139">Set Up Locations</span></span>](inventory-how-setup-locations.md)  
<span data-ttu-id="f65e3-140">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f65e3-140">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="f65e3-141">Wijzigen welke functies worden weergegeven</span><span class="sxs-lookup"><span data-stu-id="f65e3-141">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="f65e3-142">Algemene bedrijfsfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="f65e3-142">General Business Functionality</span></span>](ui-across-business-areas.md)
