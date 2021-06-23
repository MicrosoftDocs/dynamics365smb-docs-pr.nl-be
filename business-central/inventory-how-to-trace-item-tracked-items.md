---
title: Artikelen met artikeltracering traceren
description: U kunt zien waar een artikel met artikeltracering is gebruikt, inclusief hoe en wanneer dit is ontvangen of geproduceerd, overgebracht, verkocht, verbruikt of geretourneerd. U kunt tevens alle huidige exemplaren van een bepaald serie- of lotnummer in de database vinden. Dit doet u met behulp van de functies Artikeltracering en Posten zoeken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: bbfe0237beb58f22d3be7bc388d7b2726f05d4ba
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214765"
---
# <a name="trace-item-tracked-items"></a><span data-ttu-id="56db9-105">Artikelen met artikeltracering traceren</span><span class="sxs-lookup"><span data-stu-id="56db9-105">Trace Item-Tracked Items</span></span>
<span data-ttu-id="56db9-106">U kunt zien waar een artikel met artikeltracering is gebruikt, inclusief hoe en wanneer dit is ontvangen of geproduceerd, overgebracht, verkocht, verbruikt of geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="56db9-106">You can see where an item-tracked item was used, including how and when it was received or produced, transferred, sold, consumed, or returned.</span></span> <span data-ttu-id="56db9-107">U kunt tevens alle huidige exemplaren van een bepaald serie- of lotnummer in de database vinden.</span><span class="sxs-lookup"><span data-stu-id="56db9-107">You can also find all current instances of a specific serial or lot number in the database.</span></span> <span data-ttu-id="56db9-108">Dit doet u met behulp van de functies Artikeltracering en [Posten zoeken](ui-find-entries.md).</span><span class="sxs-lookup"><span data-stu-id="56db9-108">You do this by using the Item Tracing and the [Find Entries](ui-find-entries.md) features.</span></span>  

<span data-ttu-id="56db9-109">Deze functies zijn vooral handig tijdens het uitvoeren van kwaliteitscontroles wanneer u wilt weten welke klanten producten met een bepaald lotnummer hebben ontvangen of wanneer u wilt weten uit welk lot een defect onderdeel afkomstig is.</span><span class="sxs-lookup"><span data-stu-id="56db9-109">These features can be particularly useful in quality control when you need to find out which customers received products with a particular lot number or when you need to find out which lot a defective component came from.</span></span>  

 <span data-ttu-id="56db9-110">Op de pagina **Artikeltracering** kunt u voorwaarts en achterwaarts traceren in een reeks van geboekte voorraadtransacties voor het serie- of lotnummer.</span><span class="sxs-lookup"><span data-stu-id="56db9-110">On the **Item Tracing** page, you can trace forwards and backwards in a sequence of posted inventory transactions for the serial or lot number.</span></span>  

 <span data-ttu-id="56db9-111">Op de pagina **Posten zoeken** kunt u niet de reeks transacties bekijken, maar wel alle records van het serie- of lotnummer, zowel geboekte posten als open records.</span><span class="sxs-lookup"><span data-stu-id="56db9-111">On the **Find Entries** page, you cannot see the sequence of transactions, but you can see all records of the serial or lot number, both posted entries and open records.</span></span>  

 <span data-ttu-id="56db9-112">De twee functies kunnen in combinatie worden gebruikt door een getraceerd serie- of lotnummer over te brengen naar de pagina **Posten zoeken** om een volledig traceerscenario te voltooien.</span><span class="sxs-lookup"><span data-stu-id="56db9-112">The two features can be used in combination by transferring a traced serial or lot number to the **Find Entries** page to finish a complete trace scenario.</span></span> <!-- For more information, see [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).   -->

## <a name="to-trace-item-tracked-items"></a><span data-ttu-id="56db9-113">Artikelen met artikeltracering traceren</span><span class="sxs-lookup"><span data-stu-id="56db9-113">To trace item-tracked items</span></span>  

1.  <span data-ttu-id="56db9-114">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikeltracering** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="56db9-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Tracing**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="56db9-115">In de filtervelden boven aan de pagina geeft u de specifieke artikelnummers op of een filter voor de artikelnummers die u wilt traceren.</span><span class="sxs-lookup"><span data-stu-id="56db9-115">In the filter fields at the top of the page, enter the specific item numbers or a filter on the item numbers that you would like to trace.</span></span>  
3.  <span data-ttu-id="56db9-116">Selecteer in het veld **Onderdelen weergeven** of u ook wilt zien waar de onderdelen voor de artikelen vandaan komen.</span><span class="sxs-lookup"><span data-stu-id="56db9-116">In the **Show Components** field, select whether you would like to also see where the components for the items came from.</span></span> <span data-ttu-id="56db9-117">U beschikt over de volgende opties in dit veld.</span><span class="sxs-lookup"><span data-stu-id="56db9-117">Your options in this field are as follows.</span></span>  

    |<span data-ttu-id="56db9-118">Veld</span><span class="sxs-lookup"><span data-stu-id="56db9-118">Field</span></span>|<span data-ttu-id="56db9-119">Description</span><span class="sxs-lookup"><span data-stu-id="56db9-119">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="56db9-120">**Nee**</span><span class="sxs-lookup"><span data-stu-id="56db9-120">**No**</span></span>|<span data-ttu-id="56db9-121">Selecteer deze optie als u geen onderdelen wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="56db9-121">Select this option if you do not want to see any components.</span></span>|  
    |<span data-ttu-id="56db9-122">**Met artikeltracering**:</span><span class="sxs-lookup"><span data-stu-id="56db9-122">**Item-tracked Only**</span></span>|<span data-ttu-id="56db9-123">Selecteer deze optie als u alleen onderdelen met lot- of serienummers wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="56db9-123">Select this option if you want to see only components that have lot or serial numbers.</span></span>|  
    |<span data-ttu-id="56db9-124">**Alle**</span><span class="sxs-lookup"><span data-stu-id="56db9-124">**All**</span></span>|<span data-ttu-id="56db9-125">Selecteer deze optie als u alle onderdelen wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="56db9-125">Select this option if you want to see all components.</span></span>|  

4.  <span data-ttu-id="56db9-126">Selecteer in het veld **Traceringsmethode** de methode waarmee u het artikel wilt traceren.</span><span class="sxs-lookup"><span data-stu-id="56db9-126">In the **Trace Method** field, select the method you would like to use for tracing the item.</span></span> <span data-ttu-id="56db9-127">De volgende opties zijn beschikbaar</span><span class="sxs-lookup"><span data-stu-id="56db9-127">The options are as follows</span></span>  

    |<span data-ttu-id="56db9-128">Veld</span><span class="sxs-lookup"><span data-stu-id="56db9-128">Field</span></span>|<span data-ttu-id="56db9-129">Description</span><span class="sxs-lookup"><span data-stu-id="56db9-129">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="56db9-130">**Gebruik->Oorsprong**</span><span class="sxs-lookup"><span data-stu-id="56db9-130">**Usage->Origin**</span></span>|<span data-ttu-id="56db9-131">Met deze methode wordt het artikel getraceerd vanaf waar het is gebruikt tot waar het vandaan kwam.</span><span class="sxs-lookup"><span data-stu-id="56db9-131">This method traces the item starting from where it was used to where it came from.</span></span> <span data-ttu-id="56db9-132">Als een geproduceerd artikel bijvoorbeeld is verkocht aan een klant, ziet u dat op de pagina **Artikeltracering**, waarbij de verkoopverzendingsregel eerst wordt weergegeven. U kunt deze regel uitbreiden om de afkomst van de productieorder te zien.</span><span class="sxs-lookup"><span data-stu-id="56db9-132">For instance, if a manufactured item was sold to a customer, the **Item Tracing** page shows this with the sales shipment line first, which you can then expand to see from which production order it came.</span></span>|  
    |<span data-ttu-id="56db9-133">**Oorsprong->Gebruik**</span><span class="sxs-lookup"><span data-stu-id="56db9-133">**Origin->Usage**</span></span>|<span data-ttu-id="56db9-134">Met deze methode wordt het item getraceerd vanaf waar het in de voorraad is opgenomen tot waar het is gebruikt.</span><span class="sxs-lookup"><span data-stu-id="56db9-134">This method traces the item starting from where it came into inventory to where it was used.</span></span> <span data-ttu-id="56db9-135">Als een geproduceerd artikel bijvoorbeeld aan een klant is verkocht, ziet u dit op de pagina **Artikeltracering** waarbij de voltooide productieorder eerst wordt weergegeven. U kunt deze order uitbreiden om de verkoopverzendingsregels waarin het artikel wordt gebruikt weer te geven.</span><span class="sxs-lookup"><span data-stu-id="56db9-135">For instance, if a manufactured item was sold to a customer, the **Item Tracing** page shows this with the finished production order first, which you can then expand to see sale shipment lines where the item was used.</span></span>|  

5.  <span data-ttu-id="56db9-136">Kies de actie **Traceren** om de tracering uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="56db9-136">Choose the **Trace** action to run the trace.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="56db9-137">Als u dezelfde partij via meer transacties hebt ontvangen, worden op de pagina **Artikeltracering** mogelijk niet alle transacties weergegeven.</span><span class="sxs-lookup"><span data-stu-id="56db9-137">If you have received the same lot on more transactions, then the **Item Tracing** page may not show all transactions.</span></span> <span data-ttu-id="56db9-138">Alleen vereffende transacties worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="56db9-138">Only applied transactions are shown.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="56db9-139">Als al extra transactiegeschiedenis onder een artikeltraceringsregel is getraceerd door een andere bovenliggende regel, wordt het selectievakje **Al getraceerd** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="56db9-139">If additional transaction history under an item tracing line has already been traced by another line above it, then the **Already Traced** check box is selected.</span></span> <span data-ttu-id="56db9-140">Voor een eenvoudiger weergave worden dergelijke onderliggende regels niet weergegeven.</span><span class="sxs-lookup"><span data-stu-id="56db9-140">To provide a simpler view, such underlying lines are not shown.</span></span>  
>   
>  <span data-ttu-id="56db9-141">Als u de artikeltraceringsregels wilt zoeken waarin de transactiegeschiedenis al is getraceerd, kiest u de knop **Ga naar Reeds getraceerd**.</span><span class="sxs-lookup"><span data-stu-id="56db9-141">To find the item tracing lines where the transaction history has already been traced, choose the **Go to Already Traced** button.</span></span> <span data-ttu-id="56db9-142">De desbetreffende artikeltraceringsregel is geselecteerd en alle onderliggende regels zijn uitgevouwen.</span><span class="sxs-lookup"><span data-stu-id="56db9-142">The item tracing line in question is selected, and all underlying lines are expanded.</span></span>  

## <a name="to-find-item-tracked-items-with-find-entries"></a><span data-ttu-id="56db9-143">Artikelen met artikeltracering zoeken met Posten zoeken</span><span class="sxs-lookup"><span data-stu-id="56db9-143">To find item-tracked items with Find Entries</span></span>  

1. <span data-ttu-id="56db9-144">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Posten zoeken** in en selecteer de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="56db9-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then select the related link.</span></span>  
2. <span data-ttu-id="56db9-145">Kies **Acties** > **Zoeken op** > **Zoeken op artikelverwijzing**.</span><span class="sxs-lookup"><span data-stu-id="56db9-145">Choose **Actions** > **Find by** > **Find by Item Reference**.</span></span>
3. <span data-ttu-id="56db9-146">Voer in de velden **Serienr.** en **Lotnr.** de artikeltraceringsnummers in die u wilt traceren.</span><span class="sxs-lookup"><span data-stu-id="56db9-146">In the **Serial No.** and **Lot No.** fields, enter the item tracking numbers that you want to trace.</span></span>  
4. <span data-ttu-id="56db9-147">Kies de actie **Zoeken** om alle exemplaren van het serie- of lotnummer in de database te zoeken.</span><span class="sxs-lookup"><span data-stu-id="56db9-147">Choose the **Find** action to find all instances of the serial or lot number in the database.</span></span>  

## <a name="see-also"></a><span data-ttu-id="56db9-148">Zie ook</span><span class="sxs-lookup"><span data-stu-id="56db9-148">See Also</span></span>

[<span data-ttu-id="56db9-149">Voorraad</span><span class="sxs-lookup"><span data-stu-id="56db9-149">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="56db9-150">Werken met serie-, lot- en pakketnummers</span><span class="sxs-lookup"><span data-stu-id="56db9-150">Work with Serial, Lot, and Package Numbers</span></span>](inventory-how-work-item-tracking.md)  
[<span data-ttu-id="56db9-151">Ontwerpdetails: Artikeltracering</span><span class="sxs-lookup"><span data-stu-id="56db9-151">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)  
[<span data-ttu-id="56db9-152">Ontwerpdetails: Artikeltracering en reserveringen</span><span class="sxs-lookup"><span data-stu-id="56db9-152">Design Details - Item Tracking and Reservations</span></span>](design-details-item-tracking-and-reservations.md)  
[<span data-ttu-id="56db9-153">Artikelen reserveren</span><span class="sxs-lookup"><span data-stu-id="56db9-153">Reserve Items</span></span>](inventory-how-to-reserve-items.md)  
<span data-ttu-id="56db9-154">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="56db9-154">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
<!-- [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md)   -->
[<span data-ttu-id="56db9-155">Posten zoeken</span><span class="sxs-lookup"><span data-stu-id="56db9-155">Find Entries</span></span>](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]