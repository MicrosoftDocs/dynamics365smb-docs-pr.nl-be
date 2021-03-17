---
title: Overzicht van taken om kosten en inkomsten toe te wijzen | Microsoft Docs
description: Beschrijft de taken om een post in een dagboek te verdelen over verschillende rekeningen wanneer u het dagboek boekt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c455d0ba2fb6bc06b5815331ca028c43f03b2ebf
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5376899"
---
# <a name="allocate-costs-and-income"></a><span data-ttu-id="7566d-103">Kosten en inkomsten toewijzen</span><span class="sxs-lookup"><span data-stu-id="7566d-103">Allocate Costs and Income</span></span>
<span data-ttu-id="7566d-104">U kunt een post in een dagboek verdelen over verschillende rekeningen wanneer u het dagboek boekt.</span><span class="sxs-lookup"><span data-stu-id="7566d-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="7566d-105">De verdeling kan plaatsvinden op basis van drie verschillende methoden.</span><span class="sxs-lookup"><span data-stu-id="7566d-105">The allocation can be made by three different methods:</span></span>

* <span data-ttu-id="7566d-106">Aantal</span><span class="sxs-lookup"><span data-stu-id="7566d-106">Quantity</span></span>
* <span data-ttu-id="7566d-107">Percentage (%)</span><span class="sxs-lookup"><span data-stu-id="7566d-107">Percentage (%)</span></span>
* <span data-ttu-id="7566d-108">Bedrag</span><span class="sxs-lookup"><span data-stu-id="7566d-108">Amount</span></span>

<span data-ttu-id="7566d-109">De toewijzingsfuncties kunnen worden gebruikt met periodieke dagboeken en in VA-dagboeken.</span><span class="sxs-lookup"><span data-stu-id="7566d-109">The allocation features can be used with recurring general journals and in fixed assets journals.</span></span>
<!--You can also distribute the cost or revenue of a line to an intercompany partner when you post a sales or purchase document. When you post the document, a line will be posted in your general journal, and a corresponding line will be created in the intercompany outbox.-->

<span data-ttu-id="7566d-110">In de volgende procedures wordt beschreven hoe voorbereidingen moeten worden getroffen om kosten in een periodiek dagboek te verdelen door verdeelsleutels te definiëren.</span><span class="sxs-lookup"><span data-stu-id="7566d-110">The following procedures describe how to prepare to allocate costs in a recurring general journal by defining allocation keys.</span></span> <span data-ttu-id="7566d-111">Wanneer verdeelsleutels worden gedefinieerd, voltooit en boekt u het dagboek zoals elk ander periodiek dagboek.</span><span class="sxs-lookup"><span data-stu-id="7566d-111">When allocation keys are defined, you complete and post the journal like any other recurring general journal.</span></span> <span data-ttu-id="7566d-112">Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7566d-112">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="7566d-113">Verdeelsleutels instellen</span><span class="sxs-lookup"><span data-stu-id="7566d-113">To set up allocation keys</span></span>
<span data-ttu-id="7566d-114">U kunt een post in een periodiek dagboek verdelen over verschillende rekeningen wanneer u het dagboek boekt.</span><span class="sxs-lookup"><span data-stu-id="7566d-114">You can allocate an entry in a recurring general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="7566d-115">De verdeling kan plaatsvinden op basis van aantal, percentage of bedrag.</span><span class="sxs-lookup"><span data-stu-id="7566d-115">The allocation can be made by quantity, percentage, or amount.</span></span>
1. <span data-ttu-id="7566d-116">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Periodiek dagboek** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="7566d-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="7566d-117">Kies het veld **Batchnaam** om de pagina **Fin. dagboekbatches** te openen.</span><span class="sxs-lookup"><span data-stu-id="7566d-117">Choose the **Batch Name** field to open the **General Journal Batches** page.</span></span>
3. <span data-ttu-id="7566d-118">U kunt verdeelsleutels in een bestaande batch in de lijst wijzigen of u kunt een nieuwe batch met verdeelsleutels maken.</span><span class="sxs-lookup"><span data-stu-id="7566d-118">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="7566d-119">Als u een nieuwe batch wilt maken, kiest u de actie **Nieuw** en gaat u naar de volgende stap.</span><span class="sxs-lookup"><span data-stu-id="7566d-119">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="7566d-120">Als u de verdeelsleutels van een bestaand dagboek wilt wijzigen, selecteert u het dagboek en gaat u naar stap 7.</span><span class="sxs-lookup"><span data-stu-id="7566d-120">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="7566d-121">Voer in het veld **Naam** een naam voor de batch in, bijvoorbeeld Schoonmaak.</span><span class="sxs-lookup"><span data-stu-id="7566d-121">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="7566d-122">Voer in het veld **Omschrijving** een omschrijving in, bijvoorbeeld Dagboek schoonmaakkosten.</span><span class="sxs-lookup"><span data-stu-id="7566d-122">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="7566d-123">Wanneer u klaar bent, sluit u de pagina.</span><span class="sxs-lookup"><span data-stu-id="7566d-123">When you are done, close the page.</span></span> <span data-ttu-id="7566d-124">Er wordt een nieuw, leeg periodiek dagboek geopend.</span><span class="sxs-lookup"><span data-stu-id="7566d-124">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="7566d-125">Vul de velden op de regel in.</span><span class="sxs-lookup"><span data-stu-id="7566d-125">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="7566d-126">Kies de actie **Verdeelsleutels**.</span><span class="sxs-lookup"><span data-stu-id="7566d-126">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="7566d-127">Voeg voor elke verdeelsleutel een regel toe.</span><span class="sxs-lookup"><span data-stu-id="7566d-127">Add a line for each allocation.</span></span> <span data-ttu-id="7566d-128">U moet ofwel het veld **Verdeelsleutel %**, of **Verdeelsleutelaantal**, of **Bedrag** invullen.</span><span class="sxs-lookup"><span data-stu-id="7566d-128">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="7566d-129">U moet ook het veld **Rekeningnr.** invullen. Als u de transactie wilt toewijzen aan verschillende globale dimensies, moet u ook de globale dimensievelden invullen.</span><span class="sxs-lookup"><span data-stu-id="7566d-129">You must also fill in the **Account No.** field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="7566d-130">Als u een percentage op de regel invoert, wordt het bedrag in het veld **Bedrag** automatisch berekend.</span><span class="sxs-lookup"><span data-stu-id="7566d-130">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="7566d-131">Deze bedragen hebben het tegengestelde teken van het totale bedrag in het veld **Bedrag** in het periodieke dagboek.</span><span class="sxs-lookup"><span data-stu-id="7566d-131">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="7566d-132">Kies **OK** na het invoeren van de verdeelsleutelregels om terug te keren naar de pagina **Periodiek dagboek**.</span><span class="sxs-lookup"><span data-stu-id="7566d-132">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** page.</span></span> <span data-ttu-id="7566d-133">Het veld **Verdeeld bedrag (LV)** wordt ingevuld en de inhoud komt overeen met het veld **Bedrag**.</span><span class="sxs-lookup"><span data-stu-id="7566d-133">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="7566d-134">Boek het dagboek.</span><span class="sxs-lookup"><span data-stu-id="7566d-134">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="7566d-135">Een reeds ingestelde verdeelsleutel wijzigen</span><span class="sxs-lookup"><span data-stu-id="7566d-135">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="7566d-136">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Periodiek dagboek** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="7566d-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="7566d-137">Selecteer op de pagina **Periodiek dagboek** het dagboek met de verdeling.</span><span class="sxs-lookup"><span data-stu-id="7566d-137">On the **Recurring General Journal** page, select the journal with the allocation.</span></span>
3. <span data-ttu-id="7566d-138">Kies de regel met de verdeelsleutel en kies vervolgens **Verdeelsleutels**.</span><span class="sxs-lookup"><span data-stu-id="7566d-138">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="7566d-139">Pas de relevante velden aan en kies vervolgens de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="7566d-139">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="7566d-140">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7566d-140">See Also</span></span>
[<span data-ttu-id="7566d-141">Afsluitingsjaren en -perioden</span><span class="sxs-lookup"><span data-stu-id="7566d-141">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="7566d-142">[Werken met diversendagboeken](ui-work-general-journals.md)  </span><span class="sxs-lookup"><span data-stu-id="7566d-142">[Working with General Journals](ui-work-general-journals.md)  </span></span>  
<span data-ttu-id="7566d-143">[Documenten en dagboeken boeken](ui-post-documents-journals.md)  </span><span class="sxs-lookup"><span data-stu-id="7566d-143">[Posting Documents and Journals](ui-post-documents-journals.md)  </span></span>  
<span data-ttu-id="7566d-144">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7566d-144">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]