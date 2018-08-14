---
title: Artikelen blokkeren vanuit Verkoop of Inkoop
description: In Business Central kan een artikel worden gemarkeerd als geblokkeerd voor verkoop, geblokkeerd voor inkoop of geblokkeerd voor alle doeleinden.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/23/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: c6f10f8252c00bf0a599f9fa794ee36c41ce92be
ms.openlocfilehash: 2f8be478dda62fef2cb34397de488f45d4fcfc0c
ms.contentlocale: nl-be
ms.lasthandoff: 07/31/2018

---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="27e8c-103">Artikelen blokkeren vanuit Verkoop of Inkoop</span><span class="sxs-lookup"><span data-stu-id="27e8c-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="27e8c-104">U kunt voorkomen dat een artikel wordt ingevoerd op verkoop- of inkoopregels en u kunt voorkomen dat het wordt geboekt in een transactie.</span><span class="sxs-lookup"><span data-stu-id="27e8c-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="27e8c-105">De volgende tabel laat zien wat er gebeurt wanneer artikelen worden geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="27e8c-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="27e8c-106">Optie</span><span class="sxs-lookup"><span data-stu-id="27e8c-106">Option</span></span>|<span data-ttu-id="27e8c-107">Description</span><span class="sxs-lookup"><span data-stu-id="27e8c-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="27e8c-108">**Verkoop geblokkeerd**</span><span class="sxs-lookup"><span data-stu-id="27e8c-108">**Sales Blocked**</span></span>|<span data-ttu-id="27e8c-109">U kunt het artikel niet invoeren in een verkoopdocument of een verkoopartikeldagboek.</span><span class="sxs-lookup"><span data-stu-id="27e8c-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="27e8c-110">**Inkoop geblokkeerd**</span><span class="sxs-lookup"><span data-stu-id="27e8c-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="27e8c-111">U kunt het artikel niet invoeren in een inkoopdocument, in een inkoopartikeldagboek of in planningsprocessen voor inkoop.</span><span class="sxs-lookup"><span data-stu-id="27e8c-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="27e8c-112">**Geblokkeerd**</span><span class="sxs-lookup"><span data-stu-id="27e8c-112">**Blocked**</span></span>|<span data-ttu-id="27e8c-113">U kunt het artikel niet voor een artikeltransactie gebruiken.</span><span class="sxs-lookup"><span data-stu-id="27e8c-113">You cannot use the item for any item transaction.</span></span> <span data-ttu-id="27e8c-114">Voor meer informatie over het blokkeren van een artikel voor alle doeleinden raadpleegt u Artikelkaart.</span><span class="sxs-lookup"><span data-stu-id="27e8c-114">For more information about blocking an item for all purposes, see Item Card.</span></span>|  

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="27e8c-115">Voorkomen dat een artikel wordt ingevoerd op verkoopregels</span><span class="sxs-lookup"><span data-stu-id="27e8c-115">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="27e8c-116">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikelen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="27e8c-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="27e8c-117">Selecteer het artikel dat u wilt blokkeren en schakel vervolgens het selectievakje **Verkoop geblokkeerd** in.</span><span class="sxs-lookup"><span data-stu-id="27e8c-117">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="27e8c-118">Wanneer u probeert het artikel in te voeren in een verkoopdocument of -dagboekregel, wordt nu een foutbericht weergegeven dat aangeeft dat het artikel is geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="27e8c-118">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="27e8c-119">Voorkomen dat een artikel wordt ingevoerd op inkoopregels</span><span class="sxs-lookup"><span data-stu-id="27e8c-119">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="27e8c-120">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikelen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="27e8c-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="27e8c-121">Selecteer het artikel dat u wilt blokkeren en schakel vervolgens het selectievakje **Inkoop geblokkeerd** in.</span><span class="sxs-lookup"><span data-stu-id="27e8c-121">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="27e8c-122">Wanneer u probeert het artikel in te voeren in een inkoopdocument of -dagboekregel, wordt nu een foutbericht weergegeven dat aangeeft dat het artikel is geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="27e8c-122">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="27e8c-123">Voorkomen dat een artikel wordt geboekt</span><span class="sxs-lookup"><span data-stu-id="27e8c-123">To block an item from being posted</span></span>
1. <span data-ttu-id="27e8c-124">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikelen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="27e8c-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="27e8c-125">Selecteer het artikel dat u wilt blokkeren en schakel vervolgens het selectievakje **Geblokkeerd** in.</span><span class="sxs-lookup"><span data-stu-id="27e8c-125">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="27e8c-126">Wanneer u probeert een transactie van welke aard dan ook te boeken voor het artikel, krijgt u nu een foutbericht dat het artikel is geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="27e8c-126">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="27e8c-127">Zie ook</span><span class="sxs-lookup"><span data-stu-id="27e8c-127">See Also</span></span>  
[<span data-ttu-id="27e8c-128">Nieuwe artikelen registreren</span><span class="sxs-lookup"><span data-stu-id="27e8c-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="27e8c-129">Voorraad</span><span class="sxs-lookup"><span data-stu-id="27e8c-129">Inventory</span></span>](inventory-manage-inventory.md)  

