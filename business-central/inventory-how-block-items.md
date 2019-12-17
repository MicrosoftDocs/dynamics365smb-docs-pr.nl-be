---
title: Artikelen blokkeren vanuit Verkoop of Inkoop
description: In Business Central kan een artikel worden gemarkeerd als geblokkeerd voor verkoop, geblokkeerd voor inkoop of geblokkeerd voor alle doeleinden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 12/04/2019
ms.author: sgroespe
ms.openlocfilehash: 0218cf1b4982b9e8c5b5c2817590bc5ebd8f1941
ms.sourcegitcommit: b6e506a45a1cd632294bafa1c959746cc3a144f6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896073"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="c5d7d-103">Artikelen blokkeren vanuit Verkoop of Inkoop</span><span class="sxs-lookup"><span data-stu-id="c5d7d-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="c5d7d-104">U kunt voorkomen dat een artikel wordt ingevoerd op verkoop- of inkoopregels en u kunt voorkomen dat het wordt geboekt in een transactie.</span><span class="sxs-lookup"><span data-stu-id="c5d7d-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="c5d7d-105">De volgende tabel laat zien wat er gebeurt wanneer artikelen worden geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="c5d7d-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="c5d7d-106">Optie</span><span class="sxs-lookup"><span data-stu-id="c5d7d-106">Option</span></span>|<span data-ttu-id="c5d7d-107">Description</span><span class="sxs-lookup"><span data-stu-id="c5d7d-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="c5d7d-108">**Verkoop geblokkeerd**</span><span class="sxs-lookup"><span data-stu-id="c5d7d-108">**Sales Blocked**</span></span>|<span data-ttu-id="c5d7d-109">U kunt het artikel niet invoeren in een verkoopdocument of een verkoopartikeldagboek.</span><span class="sxs-lookup"><span data-stu-id="c5d7d-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="c5d7d-110">**Inkoop geblokkeerd**</span><span class="sxs-lookup"><span data-stu-id="c5d7d-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="c5d7d-111">U kunt het artikel niet invoeren in een inkoopdocument, in een inkoopartikeldagboek of in planningsprocessen voor inkoop.</span><span class="sxs-lookup"><span data-stu-id="c5d7d-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="c5d7d-112">**Geblokkeerd**</span><span class="sxs-lookup"><span data-stu-id="c5d7d-112">**Blocked**</span></span>|<span data-ttu-id="c5d7d-113">U kunt het artikel niet voor een artikeltransactie gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c5d7d-113">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="c5d7d-114">Geblokkeerde artikelen kunnen worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="c5d7d-114">Blocked items can be returned.</span></span> <span data-ttu-id="c5d7d-115">Dit betekent dat geen van de bovenstaande instellingen van toepassing zijn als het artikel wordt gebruikt in retourorders en creditnota's.</span><span class="sxs-lookup"><span data-stu-id="c5d7d-115">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="c5d7d-116">Wanneer u de functie **Document kopiëren** gebruikt om nieuwe documenten te maken op basis van bestaande documenten, ontvangt u een bericht als er items op de brondocumentregels zijn geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="c5d7d-116">When you use the **Copy Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="c5d7d-117">De geblokkeerde documentregels worden uitgesloten van het nieuwe document en een bericht toont een overzicht van alle documentregels die in het brondocument zijn geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="c5d7d-117">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="c5d7d-118">Voorkomen dat een artikel wordt ingevoerd op verkoopregels</span><span class="sxs-lookup"><span data-stu-id="c5d7d-118">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="c5d7d-119">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="c5d7d-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c5d7d-120">Selecteer het artikel dat u wilt blokkeren en schakel vervolgens het selectievakje **Verkoop geblokkeerd** in.</span><span class="sxs-lookup"><span data-stu-id="c5d7d-120">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="c5d7d-121">Wanneer u probeert het artikel in te voeren in een verkoopdocument of -dagboekregel, wordt nu een foutbericht weergegeven dat aangeeft dat het artikel is geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="c5d7d-121">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="c5d7d-122">Voorkomen dat een artikel wordt ingevoerd op inkoopregels</span><span class="sxs-lookup"><span data-stu-id="c5d7d-122">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="c5d7d-123">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="c5d7d-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c5d7d-124">Selecteer het artikel dat u wilt blokkeren en schakel vervolgens het selectievakje **Inkoop geblokkeerd** in.</span><span class="sxs-lookup"><span data-stu-id="c5d7d-124">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="c5d7d-125">Wanneer u probeert het artikel in te voeren in een inkoopdocument of -dagboekregel, wordt nu een foutbericht weergegeven dat aangeeft dat het artikel is geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="c5d7d-125">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="c5d7d-126">Voorkomen dat een artikel wordt geboekt</span><span class="sxs-lookup"><span data-stu-id="c5d7d-126">To block an item from being posted</span></span>
1. <span data-ttu-id="c5d7d-127">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="c5d7d-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="c5d7d-128">Selecteer het artikel dat u wilt blokkeren en schakel vervolgens het selectievakje **Geblokkeerd** in.</span><span class="sxs-lookup"><span data-stu-id="c5d7d-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="c5d7d-129">Wanneer u probeert een transactie van welke aard dan ook te boeken voor het artikel, krijgt u nu een foutbericht dat het artikel is geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="c5d7d-129">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5d7d-130">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c5d7d-130">See Also</span></span>  
[<span data-ttu-id="c5d7d-131">Nieuwe artikelen registreren</span><span class="sxs-lookup"><span data-stu-id="c5d7d-131">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="c5d7d-132">Voorraad</span><span class="sxs-lookup"><span data-stu-id="c5d7d-132">Inventory</span></span>](inventory-manage-inventory.md)  
