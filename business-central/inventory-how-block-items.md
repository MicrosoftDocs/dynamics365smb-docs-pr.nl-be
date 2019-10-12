---
title: Artikelen blokkeren vanuit Verkoop of Inkoop
description: In Business Central kan een artikel worden gemarkeerd als geblokkeerd voor verkoop, geblokkeerd voor inkoop of geblokkeerd voor alle doeleinden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 87cfa1830e461eac2a03a10e917712dba56eaf98
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308632"
---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="ee24b-103">Artikelen blokkeren vanuit Verkoop of Inkoop</span><span class="sxs-lookup"><span data-stu-id="ee24b-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="ee24b-104">U kunt voorkomen dat een artikel wordt ingevoerd op verkoop- of inkoopregels en u kunt voorkomen dat het wordt geboekt in een transactie.</span><span class="sxs-lookup"><span data-stu-id="ee24b-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="ee24b-105">De volgende tabel laat zien wat er gebeurt wanneer artikelen worden geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="ee24b-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="ee24b-106">Optie</span><span class="sxs-lookup"><span data-stu-id="ee24b-106">Option</span></span>|<span data-ttu-id="ee24b-107">Description</span><span class="sxs-lookup"><span data-stu-id="ee24b-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="ee24b-108">**Verkoop geblokkeerd**</span><span class="sxs-lookup"><span data-stu-id="ee24b-108">**Sales Blocked**</span></span>|<span data-ttu-id="ee24b-109">U kunt het artikel niet invoeren in een verkoopdocument of een verkoopartikeldagboek.</span><span class="sxs-lookup"><span data-stu-id="ee24b-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="ee24b-110">**Inkoop geblokkeerd**</span><span class="sxs-lookup"><span data-stu-id="ee24b-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="ee24b-111">U kunt het artikel niet invoeren in een inkoopdocument, in een inkoopartikeldagboek of in planningsprocessen voor inkoop.</span><span class="sxs-lookup"><span data-stu-id="ee24b-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="ee24b-112">**Geblokkeerd**</span><span class="sxs-lookup"><span data-stu-id="ee24b-112">**Blocked**</span></span>|<span data-ttu-id="ee24b-113">U kunt het artikel niet voor een artikeltransactie gebruiken.</span><span class="sxs-lookup"><span data-stu-id="ee24b-113">You cannot use the item for any item transaction.</span></span>|  

> [!NOTE]
> <span data-ttu-id="ee24b-114">Geblokkeerde artikelen kunnen worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="ee24b-114">Blocked items can be returned.</span></span> <span data-ttu-id="ee24b-115">Dit betekent dat geen van de bovenstaande instellingen van toepassing zijn als het artikel wordt gebruikt in retourorders en creditnota's.</span><span class="sxs-lookup"><span data-stu-id="ee24b-115">This means that none of the above settings apply when the item is used on return orders and credit memos.</span></span>

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="ee24b-116">Voorkomen dat een artikel wordt ingevoerd op verkoopregels</span><span class="sxs-lookup"><span data-stu-id="ee24b-116">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="ee24b-117">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="ee24b-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ee24b-118">Selecteer het artikel dat u wilt blokkeren en schakel vervolgens het selectievakje **Verkoop geblokkeerd** in.</span><span class="sxs-lookup"><span data-stu-id="ee24b-118">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="ee24b-119">Wanneer u probeert het artikel in te voeren in een verkoopdocument of -dagboekregel, wordt nu een foutbericht weergegeven dat aangeeft dat het artikel is geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="ee24b-119">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="ee24b-120">Voorkomen dat een artikel wordt ingevoerd op inkoopregels</span><span class="sxs-lookup"><span data-stu-id="ee24b-120">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="ee24b-121">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="ee24b-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ee24b-122">Selecteer het artikel dat u wilt blokkeren en schakel vervolgens het selectievakje **Inkoop geblokkeerd** in.</span><span class="sxs-lookup"><span data-stu-id="ee24b-122">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="ee24b-123">Wanneer u probeert het artikel in te voeren in een inkoopdocument of -dagboekregel, wordt nu een foutbericht weergegeven dat aangeeft dat het artikel is geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="ee24b-123">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="ee24b-124">Voorkomen dat een artikel wordt geboekt</span><span class="sxs-lookup"><span data-stu-id="ee24b-124">To block an item from being posted</span></span>
1. <span data-ttu-id="ee24b-125">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="ee24b-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="ee24b-126">Selecteer het artikel dat u wilt blokkeren en schakel vervolgens het selectievakje **Geblokkeerd** in.</span><span class="sxs-lookup"><span data-stu-id="ee24b-126">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="ee24b-127">Wanneer u probeert een transactie van welke aard dan ook te boeken voor het artikel, krijgt u nu een foutbericht dat het artikel is geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="ee24b-127">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee24b-128">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ee24b-128">See Also</span></span>  
[<span data-ttu-id="ee24b-129">Nieuwe artikelen registreren</span><span class="sxs-lookup"><span data-stu-id="ee24b-129">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="ee24b-130">Voorraad</span><span class="sxs-lookup"><span data-stu-id="ee24b-130">Inventory</span></span>](inventory-manage-inventory.md)  
