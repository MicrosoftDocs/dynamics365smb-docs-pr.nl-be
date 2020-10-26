---
title: Artikelen blokkeren vanuit Verkoop of Inkoop
description: U kunt voorkomen dat een artikel bijvoorbeeld wordt gebruikt in verkoop- of inkoopdocumenten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f958600a47daa12a665975d6c41e214fca7cf5ad
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914110"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="358f5-103">Artikelen blokkeren vanuit Verkoop of Inkoop</span><span class="sxs-lookup"><span data-stu-id="358f5-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="358f5-104">U kunt voorkomen dat een artikel wordt ingevoerd op regels in verkoop- of inkoopdocumenten en u kunt voorkomen dat het wordt geboekt in een transactie.</span><span class="sxs-lookup"><span data-stu-id="358f5-104">You can block an item from being entered on lines in sales or purchase documents, and you can block it from being posted in any transaction.</span></span> <span data-ttu-id="358f5-105">Dit is bijvoorbeeld handig wanneer een artikel een bekend defect heeft.</span><span class="sxs-lookup"><span data-stu-id="358f5-105">For example, this is useful when an item has a known defect.</span></span> <span data-ttu-id="358f5-106">Als iemand een geblokkeerd item kiest voor een verkoop- of aankoopdocument, zal een bericht hen laten weten dat het artikel is geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="358f5-106">If someone chooses a blocked item on a sales or purchase document a message will inform them that the item is blocked.</span></span>

<span data-ttu-id="358f5-107">De volgende tabel laat zien wat er gebeurt wanneer artikelen worden geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="358f5-107">The following table describes what occurs when items are blocked.</span></span>  

|<span data-ttu-id="358f5-108">Optie</span><span class="sxs-lookup"><span data-stu-id="358f5-108">Option</span></span>|<span data-ttu-id="358f5-109">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="358f5-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="358f5-110">**Verkoop geblokkeerd**</span><span class="sxs-lookup"><span data-stu-id="358f5-110">**Sales Blocked**</span></span>|<span data-ttu-id="358f5-111">U kunt het artikel niet invoeren in een verkoopdocument of een verkoopartikeldagboek.</span><span class="sxs-lookup"><span data-stu-id="358f5-111">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="358f5-112">**Inkoop geblokkeerd**</span><span class="sxs-lookup"><span data-stu-id="358f5-112">**Purchasing Blocked**</span></span>|<span data-ttu-id="358f5-113">U kunt het artikel niet invoeren in een inkoopdocument, in een inkoopartikeldagboek of in planningsprocessen voor inkoop.</span><span class="sxs-lookup"><span data-stu-id="358f5-113">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="358f5-114">**Geblokkeerd**</span><span class="sxs-lookup"><span data-stu-id="358f5-114">**Blocked**</span></span>|<span data-ttu-id="358f5-115">U kunt het artikel niet voor een artikeltransactie gebruiken.</span><span class="sxs-lookup"><span data-stu-id="358f5-115">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="358f5-116">Geblokkeerde artikelen kunnen worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="358f5-116">Blocked items can be returned.</span></span> <span data-ttu-id="358f5-117">Dit betekent dat geen van de bovenstaande instellingen van toepassing zijn als het artikel wordt gebruikt in retourorders en creditnota's.</span><span class="sxs-lookup"><span data-stu-id="358f5-117">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

<span data-ttu-id="358f5-118">Wanneer u de functie **Kopiëren uit document** gebruikt om nieuwe documenten te maken op basis van bestaande documenten, ontvangt u een bericht als er items op de brondocumentregels zijn geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="358f5-118">When you use the **Copy from Document** function to create new documents based on existing documents, you are notified if any items on the source document lines are blocked.</span></span> <span data-ttu-id="358f5-119">De geblokkeerde documentregels worden uitgesloten van het nieuwe document en een bericht toont een overzicht van alle documentregels die in het brondocument zijn geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="358f5-119">The blocked document lines are excluded from the new document, and a notification shows an overview of all document lines that are blocked in the source document.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="358f5-120">Voorkomen dat een artikel wordt ingevoerd op verkoopregels</span><span class="sxs-lookup"><span data-stu-id="358f5-120">To block an item from being entered on sales lines</span></span>  
1.  <span data-ttu-id="358f5-121">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="358f5-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items** , and then choose the related link.</span></span>  
2.  <span data-ttu-id="358f5-122">Selecteer het artikel dat u wilt blokkeren en schakel vervolgens het selectievakje **Verkoop geblokkeerd** in.</span><span class="sxs-lookup"><span data-stu-id="358f5-122">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="358f5-123">Voorkomen dat een artikel wordt ingevoerd op inkoopregels</span><span class="sxs-lookup"><span data-stu-id="358f5-123">To block an item from being entered on purchase lines</span></span>  
1.  <span data-ttu-id="358f5-124">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="358f5-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items** , and then choose the related link.</span></span>  
2.  <span data-ttu-id="358f5-125">Selecteer het artikel dat u wilt blokkeren en schakel vervolgens het selectievakje **Inkoop geblokkeerd** in.</span><span class="sxs-lookup"><span data-stu-id="358f5-125">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="358f5-126">Voorkomen dat een artikel wordt geboekt</span><span class="sxs-lookup"><span data-stu-id="358f5-126">To block an item from being posted</span></span>
1. <span data-ttu-id="358f5-127">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="358f5-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items** , and then choose the related link.</span></span>
2. <span data-ttu-id="358f5-128">Selecteer het artikel dat u wilt blokkeren en schakel vervolgens het selectievakje **Geblokkeerd** in.</span><span class="sxs-lookup"><span data-stu-id="358f5-128">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

## <a name="see-also"></a><span data-ttu-id="358f5-129">Zie ook</span><span class="sxs-lookup"><span data-stu-id="358f5-129">See Also</span></span>  
[<span data-ttu-id="358f5-130">Nieuwe artikelen registreren</span><span class="sxs-lookup"><span data-stu-id="358f5-130">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="358f5-131">Voorraad</span><span class="sxs-lookup"><span data-stu-id="358f5-131">Inventory</span></span>](inventory-manage-inventory.md)  
