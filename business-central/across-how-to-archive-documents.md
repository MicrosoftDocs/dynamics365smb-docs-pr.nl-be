---
title: Verkoop- en inkoopdocumenten archiveren | Microsoft Docs
description: U kunt verkoop- en inkooporders, offertes, raamcontracten, retourorders en raamcontracten archiveren en u kunt het gearchiveerde document gebruiken om het document waaruit het is gearchiveerd, opnieuw te maken.
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
ms.openlocfilehash: 6b1b23c062fdb1c4558a292c7aa454ae24ff3c71
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="archive-documents"></a><span data-ttu-id="56ef9-103">Documenten archiveren</span><span class="sxs-lookup"><span data-stu-id="56ef9-103">Archive Documents</span></span>
<span data-ttu-id="56ef9-104">U kunt verkoop- en inkooporders, offertes, raamcontracten, retourorders en raamcontracten archiveren en u kunt het gearchiveerde document gebruiken om het document waaruit het is gearchiveerd, opnieuw te maken.</span><span class="sxs-lookup"><span data-stu-id="56ef9-104">You can archive sales and purchase orders, quotes, return orders, and blanket orders, and you can use the archived document to recreate the document that it was archived from.</span></span>

## <a name="to-set-up-automatic-document-archiving"></a><span data-ttu-id="56ef9-105">Automatische documentarchivering instellen</span><span class="sxs-lookup"><span data-stu-id="56ef9-105">To set up automatic document archiving</span></span>  
<span data-ttu-id="56ef9-106">U kunt automatische archivering van verkoop- en inkooporders, offertes, raamcontracten en retourorders instellen voordat u documenten verwijdert.</span><span class="sxs-lookup"><span data-stu-id="56ef9-106">You can set up automatic archiving of sales and purchase orders, quotes, blanket orders, and return orders, before you delete documents.</span></span>

<span data-ttu-id="56ef9-107">In de volgende procedure wordt beschreven hoe u automatische archivering van verkoopdocumenten instelt.</span><span class="sxs-lookup"><span data-stu-id="56ef9-107">The following procedure describes how to set up automatic archiving of sales documents.</span></span> <span data-ttu-id="56ef9-108">De stappen zijn vergelijkbaar voor inkoopdocumenten.</span><span class="sxs-lookup"><span data-stu-id="56ef9-108">The steps are similar for purchase documents.</span></span>
1.  <span data-ttu-id="56ef9-109">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instellingen van verkoop en tegoeden** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="56ef9-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales & Receivables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="56ef9-110">Vul in het venster **Instellingen van verkoop en tegoeden** de velden als volgt in:</span><span class="sxs-lookup"><span data-stu-id="56ef9-110">In the **Sales & Receivables Setup** window, fill in the fields as follows.</span></span>

|<span data-ttu-id="56ef9-111">Veld</span><span class="sxs-lookup"><span data-stu-id="56ef9-111">Field</span></span>|<span data-ttu-id="56ef9-112">Description</span><span class="sxs-lookup"><span data-stu-id="56ef9-112">Description</span></span>|
|-----|-----------|
|<span data-ttu-id="56ef9-113">**Verkoopoffertes archiveren**</span><span class="sxs-lookup"><span data-stu-id="56ef9-113">**Archiving Sales Quotes**</span></span>|<span data-ttu-id="56ef9-114">**Nooit** om verkoopoffertes nooit te archiveren wanneer deze worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="56ef9-114">**Never** to never archive sales quotes when they are deleted.</span></span> <span data-ttu-id="56ef9-115">**Vraag** om de gebruiker te laten kiezen of verkoopoffertes moeten worden gearchiveerd wanneer ze worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="56ef9-115">**Question** to prompt the user to choose whether to archive sales quotes when they are deleted.</span></span> <span data-ttu-id="56ef9-116">**Altijd** om verkoopoffertes automatisch te archiveren wanneer deze worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="56ef9-116">**Always** to archive sales quotes automatically when they are deleted.</span></span>|
|<span data-ttu-id="56ef9-117">**Raamcontractorders archiveren**</span><span class="sxs-lookup"><span data-stu-id="56ef9-117">**Archiving Blanket Sales Orders**</span></span>|<span data-ttu-id="56ef9-118">Selecteer dit om raamcontactorders steeds automatisch te archiveren wanneer ze worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="56ef9-118">Select to archive blanket sales orders automatically each time they are deleted.</span></span>|
|<span data-ttu-id="56ef9-119">**Orders en retourorders archiveren**</span><span class="sxs-lookup"><span data-stu-id="56ef9-119">**Arch. Orders and Ret. Orders**</span></span>|<span data-ttu-id="56ef9-120">Selecteer dit om steeds automatisch verkooporders te archiveren wanneer ze worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="56ef9-120">Select to automatically archive sales orders each time they are deleted.</span></span>|

## <a name="to-archive-a-sales-order"></a><span data-ttu-id="56ef9-121">Een verkooporder archiveren</span><span class="sxs-lookup"><span data-stu-id="56ef9-121">To archive a sales order</span></span>
<span data-ttu-id="56ef9-122">In de volgende procedure wordt beschreven hoe u een verkooporder archiveert.</span><span class="sxs-lookup"><span data-stu-id="56ef9-122">The following procedure describes how to archive a sales order.</span></span> <span data-ttu-id="56ef9-123">De stappen zijn vergelijkbaar voor alle orders, raamcontracten, retourorders en offertes.</span><span class="sxs-lookup"><span data-stu-id="56ef9-123">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="56ef9-124">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="56ef9-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="56ef9-125">Open een verkooporder die u wilt archiveren.</span><span class="sxs-lookup"><span data-stu-id="56ef9-125">Open a sales order that you want to archive.</span></span>  
3.  <span data-ttu-id="56ef9-126">Kies de actie **Document archiveren**.</span><span class="sxs-lookup"><span data-stu-id="56ef9-126">Choose the **Archive Document** action.</span></span>

<span data-ttu-id="56ef9-127">De verkooporder wordt gearchiveerd.</span><span class="sxs-lookup"><span data-stu-id="56ef9-127">The sales order is archived.</span></span> <span data-ttu-id="56ef9-128">U kunt deze bekijken in het venster **Gearchiveerde verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="56ef9-128">You can view it in the **Archived Sales orders** window.</span></span> <span data-ttu-id="56ef9-129">Van hieruit kunt u deze ook gebruiken om de verkooporder waaruit deze is gearchiveerd, opnieuw te maken.</span><span class="sxs-lookup"><span data-stu-id="56ef9-129">From here, you can also use it to recreate the sales order that it was archived from.</span></span>

## <a name="to-recreate-a-sales-order-from-the-archive"></a><span data-ttu-id="56ef9-130">Een verkooporder maken vanuit het archief</span><span class="sxs-lookup"><span data-stu-id="56ef9-130">To recreate a sales order from the archive</span></span>
<span data-ttu-id="56ef9-131">In de volgende procedure wordt beschreven hoe u een verkooporder opnieuw maakt.</span><span class="sxs-lookup"><span data-stu-id="56ef9-131">The following procedure describes how to recreate a sales order.</span></span> <span data-ttu-id="56ef9-132">De stappen zijn vergelijkbaar voor alle orders, raamcontracten, retourorders en offertes.</span><span class="sxs-lookup"><span data-stu-id="56ef9-132">The steps are similar for all orders, blanket orders, return orders, and quotes.</span></span>

1.  <span data-ttu-id="56ef9-133">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gearchiveerde verkooporders** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="56ef9-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Archived Sales Orders**, and then choose the related link.</span></span>
2.  <span data-ttu-id="56ef9-134">Selecteer de gearchiveerde verkooporder die u opnieuw wilt maken en kies vervolgens de actie **Herstellen**.</span><span class="sxs-lookup"><span data-stu-id="56ef9-134">Select the archived sales order that you want to recreate, and then choose the **Restore** action.</span></span>  

<span data-ttu-id="56ef9-135">De verkooporder wordt gemaakt en toegevoegd aan het venster **Verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="56ef9-135">The sales order is created and added to the **Sales Orders** window.</span></span>

## <a name="to-delete-archived-sales-orders"></a><span data-ttu-id="56ef9-136">Gearchiveerde verkooporders verwijderen</span><span class="sxs-lookup"><span data-stu-id="56ef9-136">To delete archived sales orders</span></span>
<span data-ttu-id="56ef9-137">In de volgende procedure wordt beschreven hoe gearchiveerde verkooporders verwijdert.</span><span class="sxs-lookup"><span data-stu-id="56ef9-137">The following procedure describes how to delete archived sales orders.</span></span> <span data-ttu-id="56ef9-138">De stappen lijken op andere gearchiveerde inkoop- en verkoopdocumenten.</span><span class="sxs-lookup"><span data-stu-id="56ef9-138">The steps are similar for other archived sales and purchase documents.</span></span>

1.  <span data-ttu-id="56ef9-139">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gearch. verk.-orderversies verwijderen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="56ef9-139">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Archived Sales Order Versions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="56ef9-140">Selecteer in het venster **Gearch. verk.-orderversies verwijderen** de gewenste filters.</span><span class="sxs-lookup"><span data-stu-id="56ef9-140">In the **Delete Archived Sales Order Versions** window, select the appropriate filters.</span></span>  
3.  <span data-ttu-id="56ef9-141">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="56ef9-141">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="56ef9-142">Zie ook</span><span class="sxs-lookup"><span data-stu-id="56ef9-142">See Also</span></span>
[<span data-ttu-id="56ef9-143">Documentregels traceren</span><span class="sxs-lookup"><span data-stu-id="56ef9-143">Track Document Lines</span></span>](across-how-to-track-document-lines.md)  
[<span data-ttu-id="56ef9-144">Verkoop</span><span class="sxs-lookup"><span data-stu-id="56ef9-144">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="56ef9-145">Algemene bedrijfsfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="56ef9-145">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="56ef9-146">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="56ef9-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

