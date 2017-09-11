---
title: Overzicht van taken om kosten en inkomsten toe te wijzen | Microsoft Docs
description: Beschrijft de taken om een post in een dagboek te verdelen over verschillende rekeningen wanneer u het dagboek boekt.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/07/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 1620e69ce8018256780dcba108c31312c02166cb
ms.contentlocale: nl-be
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-allocate-costs-and-income"></a><span data-ttu-id="df7ce-103">Procedure: Kosten en inkomsten toewijzen</span><span class="sxs-lookup"><span data-stu-id="df7ce-103">How to: Allocate Costs and Income</span></span>
<span data-ttu-id="df7ce-104">U kunt een post in een dagboek verdelen over verschillende rekeningen wanneer u het dagboek boekt.</span><span class="sxs-lookup"><span data-stu-id="df7ce-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="df7ce-105">De verdeling kan plaatsvinden op basis van drie verschillende methoden.</span><span class="sxs-lookup"><span data-stu-id="df7ce-105">The allocation can be made by three different methods:</span></span>

* <span data-ttu-id="df7ce-106">Aantal</span><span class="sxs-lookup"><span data-stu-id="df7ce-106">Quantity</span></span>
* <span data-ttu-id="df7ce-107">Percentage (%)</span><span class="sxs-lookup"><span data-stu-id="df7ce-107">Percentage (%)</span></span>
* <span data-ttu-id="df7ce-108">Bedrag</span><span class="sxs-lookup"><span data-stu-id="df7ce-108">Amount</span></span>

<span data-ttu-id="df7ce-109">De toewijzingsfuncties kunnen worden gebruikt met periodieke dagboeken en in VA-dagboeken.</span><span class="sxs-lookup"><span data-stu-id="df7ce-109">The allocation features can be used with recurring general journals and in fixed assets journals.</span></span>
<!--You can also distribute the cost or revenue of a line to an intercompany partner when you post a sales or purchase document. When you post the document, a line will be posted in your general journal, and a corresponding line will be created in the intercompany outbox.-->

<span data-ttu-id="df7ce-110">In de volgende procedures wordt beschreven hoe voorbereidingen moeten worden getroffen om kosten in een periodiek dagboek te verdelen door verdeelsleutels te definiëren.</span><span class="sxs-lookup"><span data-stu-id="df7ce-110">The following procedures describe how to prepare to allocate costs in a recurring general journal by defining allocation keys.</span></span> <span data-ttu-id="df7ce-111">Wanneer verdeelsleutels worden gedefinieerd, voltooit en boekt u het dagboek zoals elk ander periodiek dagboek.</span><span class="sxs-lookup"><span data-stu-id="df7ce-111">When allocation keys are defined, you complete and post the journal like any other recurring general journal.</span></span> <span data-ttu-id="df7ce-112">Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="df7ce-112">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="df7ce-113">Verdeelsleutels instellen</span><span class="sxs-lookup"><span data-stu-id="df7ce-113">To set up allocation keys</span></span>
<span data-ttu-id="df7ce-114">U kunt een post in een periodiek dagboek verdelen over verschillende rekeningen wanneer u het dagboek boekt.</span><span class="sxs-lookup"><span data-stu-id="df7ce-114">You can allocate an entry in a recurring general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="df7ce-115">De verdeling kan plaatsvinden op basis van aantal, percentage of bedrag.</span><span class="sxs-lookup"><span data-stu-id="df7ce-115">The allocation can be made by quantity, percentage, or amount.</span></span>
1. <span data-ttu-id="df7ce-116">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Periodiek dagboek** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="df7ce-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="df7ce-117">Kies het veld **Batchnaam** om het venster **Fin. dagboekbatches** te openen.</span><span class="sxs-lookup"><span data-stu-id="df7ce-117">Choose the **Batch Name** field to open the **General Journal Batches** window.</span></span>
3. <span data-ttu-id="df7ce-118">U kunt verdeelsleutels in een bestaande batch in de lijst wijzigen of u kunt een nieuwe batch met verdeelsleutels maken.</span><span class="sxs-lookup"><span data-stu-id="df7ce-118">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="df7ce-119">Als u een nieuwe batch wilt maken, kiest u de actie **Nieuw** en gaat u naar de volgende stap.</span><span class="sxs-lookup"><span data-stu-id="df7ce-119">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="df7ce-120">Als u de verdeelsleutels van een bestaand dagboek wilt wijzigen, selecteert u het dagboek en gaat u naar stap 7.</span><span class="sxs-lookup"><span data-stu-id="df7ce-120">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="df7ce-121">Voer in het veld **Naam** een naam voor de batch in, bijvoorbeeld Schoonmaak.</span><span class="sxs-lookup"><span data-stu-id="df7ce-121">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="df7ce-122">Voer in het veld **Omschrijving** een omschrijving in, bijvoorbeeld Dagboek schoonmaakkosten.</span><span class="sxs-lookup"><span data-stu-id="df7ce-122">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="df7ce-123">Wanneer u klaar bent, sluit u het venster.</span><span class="sxs-lookup"><span data-stu-id="df7ce-123">When you are done, close the window.</span></span> <span data-ttu-id="df7ce-124">Er wordt een nieuw, leeg periodiek dagboek geopend.</span><span class="sxs-lookup"><span data-stu-id="df7ce-124">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="df7ce-125">Vul de velden op de regel in.</span><span class="sxs-lookup"><span data-stu-id="df7ce-125">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="df7ce-126">Kies de actie **Verdeelsleutels**.</span><span class="sxs-lookup"><span data-stu-id="df7ce-126">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="df7ce-127">Voeg voor elke verdeelsleutel een regel toe.</span><span class="sxs-lookup"><span data-stu-id="df7ce-127">Add a line for each allocation.</span></span> <span data-ttu-id="df7ce-128">U moet ofwel het veld **Verdeelsleutel %**, of **Verdeelsleutelaantal**, of **Bedrag** invullen.</span><span class="sxs-lookup"><span data-stu-id="df7ce-128">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="df7ce-129">U moet ook het veld **Rekeningnr.** invullen</span><span class="sxs-lookup"><span data-stu-id="df7ce-129">You must also fill in the **Account No.**</span></span> <span data-ttu-id="df7ce-130">en, als u de transactie verdeelt over globale dimensies, ook de globale dimensievelden.</span><span class="sxs-lookup"><span data-stu-id="df7ce-130">field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="df7ce-131">Als u een percentage op de regel invoert, wordt het bedrag in het veld **Bedrag** automatisch berekend.</span><span class="sxs-lookup"><span data-stu-id="df7ce-131">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="df7ce-132">Deze bedragen hebben het tegengestelde teken van het totale bedrag in het veld **Bedrag** in het periodieke dagboek.</span><span class="sxs-lookup"><span data-stu-id="df7ce-132">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="df7ce-133">Kies **OK** na het invoeren van de verdeelsleutelregels om terug te keren naar het venster **Periodiek dagboek**.</span><span class="sxs-lookup"><span data-stu-id="df7ce-133">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** window.</span></span> <span data-ttu-id="df7ce-134">Het veld **Verdeeld bedrag (LV)** wordt ingevuld en de inhoud komt overeen met het veld **Bedrag**.</span><span class="sxs-lookup"><span data-stu-id="df7ce-134">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="df7ce-135">Boek het dagboek.</span><span class="sxs-lookup"><span data-stu-id="df7ce-135">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="df7ce-136">Een reeds ingestelde verdeelsleutel wijzigen</span><span class="sxs-lookup"><span data-stu-id="df7ce-136">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="df7ce-137">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Periodiek dagboek** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="df7ce-137">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="df7ce-138">Selecteer in het venster **Periodiek dagboek** het dagboek met de verdeling.</span><span class="sxs-lookup"><span data-stu-id="df7ce-138">In the **Recurring General Journal** window, select the journal with the allocation.</span></span>
3. <span data-ttu-id="df7ce-139">Kies de regel met de verdeelsleutel en kies vervolgens **Verdeelsleutels**.</span><span class="sxs-lookup"><span data-stu-id="df7ce-139">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="df7ce-140">Pas de relevante velden aan en kies vervolgens de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="df7ce-140">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="df7ce-141">Zie ook</span><span class="sxs-lookup"><span data-stu-id="df7ce-141">See Also</span></span>
[<span data-ttu-id="df7ce-142">Afsluitingsjaren en -perioden</span><span class="sxs-lookup"><span data-stu-id="df7ce-142">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="df7ce-143">[Werken met diversendagboeken](ui-work-general-journals.md)  </span><span class="sxs-lookup"><span data-stu-id="df7ce-143">[Working with General Journals](ui-work-general-journals.md)  </span></span>  
<span data-ttu-id="df7ce-144">[Documenten en dagboeken boeken](ui-post-documents-journals.md)  </span><span class="sxs-lookup"><span data-stu-id="df7ce-144">[Posting Documents and Journals](ui-post-documents-journals.md)  </span></span>  
<span data-ttu-id="df7ce-145">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="df7ce-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

