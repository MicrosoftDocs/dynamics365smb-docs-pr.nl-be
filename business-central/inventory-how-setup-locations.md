---
title: "Een vestigingskaart instellen en transferroutes definiëren| Microsoft Docs"
description: U maakt een vestigingskaart voor elke plaats waar u voorraadartikelen opslaat, bijvoorbeeld een magazijn of een distributiecentrum, en u stelt routes in om artikelen tussen vestigingen over te brengen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 01/25/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: 45943ef97eee9d6bf24fd679e5dbbab96f5177f8
ms.contentlocale: nl-be
ms.lasthandoff: 04/18/2018

---
# <a name="set-up-locations"></a><span data-ttu-id="78741-103">Vestigingen instellen</span><span class="sxs-lookup"><span data-stu-id="78741-103">Set Up Locations</span></span>
<span data-ttu-id="78741-104">Als u artikelen op meer dan één plaats of magazijn koopt, opslaat of verkoopt, moet u elke vestiging instellen met een vestigingskaart en transferroutes definiëren.</span><span class="sxs-lookup"><span data-stu-id="78741-104">If you buy, store, or sell items at more than one place or warehouse, you must set each location up with a location card and define transfer routes.</span></span>

<span data-ttu-id="78741-105">U kunt vervolgens documentregels voor een bepaalde vestiging maken, beschikbaarheid per locatie weergeven en voorraad tussen locaties overbrengen.</span><span class="sxs-lookup"><span data-stu-id="78741-105">You can then create document lines for a specific location, view availability by location, and transfer inventory between locations.</span></span> <span data-ttu-id="78741-106">Zie [Voorraad beheren](inventory-manage-inventory.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="78741-106">For more information, see [Manage Inventory](inventory-manage-inventory.md).</span></span>

## <a name="to-create-a-location-card"></a><span data-ttu-id="78741-107">Een vestigingskaart maken</span><span class="sxs-lookup"><span data-stu-id="78741-107">To create a location card</span></span>
1. <span data-ttu-id="78741-108">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Vestigingen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="78741-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>
2. <span data-ttu-id="78741-109">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="78741-109">Choose the **New** action.</span></span>
3. <span data-ttu-id="78741-110">Vul indien nodig de velden in het venster **Vestigingskaart** in.</span><span class="sxs-lookup"><span data-stu-id="78741-110">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="78741-111">Herhaal stap 2 en 3 voor elke locatie waar u voorraad wilt houden.</span><span class="sxs-lookup"><span data-stu-id="78741-111">Repeat steps 2 and 3 for every location where you want to keep inventory.</span></span>

> [!NOTE]  
> <span data-ttu-id="78741-112">Veel velden op de vestigingskaart verwijzen naar de verwerking van artikelen in inkomende en uitgaande magazijnprocessen.</span><span class="sxs-lookup"><span data-stu-id="78741-112">Many fields on the location card refer to the handling of items in inbound and outbound warehouse processes.</span></span> <span data-ttu-id="78741-113">Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="78741-113">For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).</span></span>

## <a name="to-create-a-transfer-route"></a><span data-ttu-id="78741-114">Een transferroute maken</span><span class="sxs-lookup"><span data-stu-id="78741-114">To create a transfer route</span></span>
1. <span data-ttu-id="78741-115">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Transferroutes** in en klik op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="78741-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer Routes**, and then choose the related link.</span></span>
2. <span data-ttu-id="78741-116">U kunt ook vanuit elk **Vestiging**-venster de actie **Transferroutes** kiezen.</span><span class="sxs-lookup"><span data-stu-id="78741-116">Alternatively, from any **Location Card** window, choose the **Transfer Routes** action.</span></span>
3. <span data-ttu-id="78741-117">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="78741-117">Choose the **New** action.</span></span>
4. <span data-ttu-id="78741-118">Vul indien nodig de velden in het venster **Vestigingskaart** in.</span><span class="sxs-lookup"><span data-stu-id="78741-118">In the **Location Card** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="78741-119">U kunt nu voorraadartikelen tussen twee vestigingen overbrengen.</span><span class="sxs-lookup"><span data-stu-id="78741-119">You can now transfer inventory items between two locations.</span></span> <span data-ttu-id="78741-120">Zie voor meer informatie [Voorraad overbrengen tussen vestigingen](inventory-how-transfer-between-locations.md).</span><span class="sxs-lookup"><span data-stu-id="78741-120">For more information, see [Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md).</span></span>    

## <a name="see-also"></a><span data-ttu-id="78741-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="78741-121">See Also</span></span>
[<span data-ttu-id="78741-122">Voorraad beheren</span><span class="sxs-lookup"><span data-stu-id="78741-122">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="78741-123">[Voorraad overbrengen tussen vestigingen](inventory-how-transfer-between-locations.md)  </span><span class="sxs-lookup"><span data-stu-id="78741-123">[Transfer Inventory Between Locations](inventory-how-transfer-between-locations.md)  </span></span>  
<span data-ttu-id="78741-124">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="78741-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="78741-125">Wijzigen welke functies worden weergegeven</span><span class="sxs-lookup"><span data-stu-id="78741-125">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="78741-126">Algemene bedrijfsfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="78741-126">General Business Functionality</span></span>](ui-across-business-areas.md)

