---
title: Een boeking ongedaan maken door een tegenboeking te boeken| Microsoft Docs
description: Als u een foutieve boeking in het dagboek hebt gemaakt, kunt u vervolgens de functie Transactie tegenboeken gebruiken om de boeking ongedaan te maken met de juiste audittrail.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: f2767fca96e1f3689fc4806d878381d02622f261
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243745"
---
# <a name="reverse-postings"></a><span data-ttu-id="1e523-103">Boekingen tegenboeken</span><span class="sxs-lookup"><span data-stu-id="1e523-103">Reverse Postings</span></span>
<span data-ttu-id="1e523-104">Om een foutieve dagboekpost ongedaan te maken, selecteert en maakt u een tegenboeking (posten die identiek zijn aan de oorspronkelijke post, maar met een tegenovergesteld teken in het bedragveld) met hetzelfde documentnummer en dezelfde boekingsdatum als de originele post.</span><span class="sxs-lookup"><span data-stu-id="1e523-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="1e523-105">Nadat een post is tegengeboekt, moet u de juiste post maken.</span><span class="sxs-lookup"><span data-stu-id="1e523-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="1e523-106">U kunt alleen posten tegenboeken die zijn geboekt vanaf een algemene dagboekregel.</span><span class="sxs-lookup"><span data-stu-id="1e523-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="1e523-107">Een post kan slechts één keer worden tegengeboekt.</span><span class="sxs-lookup"><span data-stu-id="1e523-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="1e523-108">Voor meer informatie over het boeken vanuit een dagboek zie [Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md)</span><span class="sxs-lookup"><span data-stu-id="1e523-108">For more information about posting from a general journal, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>

<span data-ttu-id="1e523-109">Als u een onjuist negatief aantal hebt geboekt, dat wil zeggen, als u een inkooporder hebt gemaakt met bijvoorbeeld het verkeerde aantal artikelen en deze order hebt geboekt als ontvangen (maar niet gefactureerd), kunt u de boeking ongedaan maken.</span><span class="sxs-lookup"><span data-stu-id="1e523-109">If you have made an incorrect negative quantity posting, such as a purchase order with the wrong number of items and posted it as received but not invoiced, then you can undo the posting.</span></span>

<span data-ttu-id="1e523-110">Als u een onjuist positief aantal hebt geboekt, dat wil zeggen, als u een inkoopretourorder hebt gemaakt met bijvoorbeeld het verkeerde aantal artikelen en deze order hebt geboekt als verzonden (maar niet gefactureerd), kunt u de boeking ongedaan maken.</span><span class="sxs-lookup"><span data-stu-id="1e523-110">If you have made an incorrect positive quantity posting, such as a purchase return order with the wrong number of items and posted it as shipped but not invoiced, then you can undo the posting.</span></span>   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="1e523-111">De dagboekboeking van een grootboekpost tegenboeken</span><span class="sxs-lookup"><span data-stu-id="1e523-111">To reverse the journal posting of a general ledger entry</span></span>
<span data-ttu-id="1e523-112">U kunt posten vanuit alle **Posten**-pagina's tegenboeken.</span><span class="sxs-lookup"><span data-stu-id="1e523-112">You can reverse entries from all **Ledger Entries** pages.</span></span> <span data-ttu-id="1e523-113">De volgende procedure is gebaseerd op de pagina **Grootboekposten**.</span><span class="sxs-lookup"><span data-stu-id="1e523-113">The following procedure is based on the **General Ledger Entries** page.</span></span>
1. <span data-ttu-id="1e523-114">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Grootboekposten** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="1e523-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="1e523-115">Selecteer de post die u wilt tegenboeken en kies vervolgens de actie **Transactie tegenboeken**.</span><span class="sxs-lookup"><span data-stu-id="1e523-115">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="1e523-116">Het moet afkomstig zijn uit een dagboekboeking.</span><span class="sxs-lookup"><span data-stu-id="1e523-116">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="1e523-117">Selecteer op de pagina **Transactieposten tegenboeken** de relevante post en kies de actie **Tegenboeken**.</span><span class="sxs-lookup"><span data-stu-id="1e523-117">On the **Reverse Transaction Entries** page, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="1e523-118">Kies de knop **Ja** in het bevestigingsbericht.</span><span class="sxs-lookup"><span data-stu-id="1e523-118">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a><span data-ttu-id="1e523-119">Een aantalsboeking ongedaan maken op een geboekte inkoopontvangst</span><span class="sxs-lookup"><span data-stu-id="1e523-119">To undo a quantity posting on a posted purchase receipt</span></span>  

1.  <span data-ttu-id="1e523-120">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Geboekte inkoopontvangsten** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="1e523-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Receipts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1e523-121">Open de geboekte ontvangst die u ongedaan wilt maken.</span><span class="sxs-lookup"><span data-stu-id="1e523-121">Open the posted receipt that you want to undo.</span></span>  
3.  <span data-ttu-id="1e523-122">Selecteer de regel(s) die u ongedaan wilt maken.</span><span class="sxs-lookup"><span data-stu-id="1e523-122">Select the line or lines that you want to undo.</span></span>  
4.  <span data-ttu-id="1e523-123">Kies de actie **Ontvangst ongedaan maken**.</span><span class="sxs-lookup"><span data-stu-id="1e523-123">Choose **Undo Receipt** action.</span></span>

    <span data-ttu-id="1e523-124">Er wordt een correctieregel ingevoegd onder de geselecteerde ontvangstregel.</span><span class="sxs-lookup"><span data-stu-id="1e523-124">A corrective line is inserted under the selected receipt line.</span></span>  

    <span data-ttu-id="1e523-125">Als de hoeveelheid in een magazijnontvangst is ontvangen, wordt een correctieregel ingevoegd in de geboekte magazijnontvangst.</span><span class="sxs-lookup"><span data-stu-id="1e523-125">If the quantity was received in a warehouse receipt, then a corrective line is inserted in the posted warehouse receipt.</span></span>  

    <span data-ttu-id="1e523-126">De velden **Ontvangen aantal** en **Niet geboekt aantal** op de bijbehorende inkooporder worden ingesteld op nul.</span><span class="sxs-lookup"><span data-stu-id="1e523-126">The **Quantity Received** and **Qty. Rcd. Not Invoiced** fields on the related purchase order are set to zero.</span></span>

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a><span data-ttu-id="1e523-127">Een aantalboeking ongedaan maken en opnieuw uitvoeren voor een geboekte retourzending</span><span class="sxs-lookup"><span data-stu-id="1e523-127">To undo and then redo a quantity posting on a posted return shipment</span></span>

1.  <span data-ttu-id="1e523-128">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Geboekte retourverzendingen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="1e523-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Return Shipments**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1e523-129">Open de geboekte retourzending die u ongedaan wilt maken.</span><span class="sxs-lookup"><span data-stu-id="1e523-129">Open the posted return shipment that you want to undo.</span></span>
3. <span data-ttu-id="1e523-130">Selecteer de regel(s) die u ongedaan wilt maken.</span><span class="sxs-lookup"><span data-stu-id="1e523-130">Select the line or lines you want to undo.</span></span>  

4.  <span data-ttu-id="1e523-131">Kies de actie **Retourverzending ongedaan maken**.</span><span class="sxs-lookup"><span data-stu-id="1e523-131">Choose the **Undo Return Shipment** action.</span></span>  

    <span data-ttu-id="1e523-132">In het geboekte document wordt een gecorrigeerde regel ingevoegd. Op de retourorder worden de velden **Retouraantal verzonden** en **Retourverzending niet gefact.** ingesteld op nul.</span><span class="sxs-lookup"><span data-stu-id="1e523-132">A corrective line is inserted in the posted document, and the **Return Qty. Shipped** and **Return Shpd. Not Invd.** fields on the return order are set to zero.</span></span>  

    <span data-ttu-id="1e523-133">Ga nu terug naar de inkoopretourorder om opnieuw te boeken.</span><span class="sxs-lookup"><span data-stu-id="1e523-133">Now go back to the purchase return order to redo the posting.</span></span>  

5.  <span data-ttu-id="1e523-134">Let op de pagina **Geboekte retourverzending** op het nummer in het **Retourordernr.**</span><span class="sxs-lookup"><span data-stu-id="1e523-134">On the **Posted Return Shipment** page, take a note of the number in the **Return Order No.**</span></span> <span data-ttu-id="1e523-135">toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="1e523-135">field.</span></span>  
6.  <span data-ttu-id="1e523-136">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopretourorders** in en selecteer vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="1e523-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Return Orders**, and then select the related link.</span></span>  
7.  <span data-ttu-id="1e523-137">Open de retourorder en kies de actie **Opnieuw openen**.</span><span class="sxs-lookup"><span data-stu-id="1e523-137">Open the return order in question, and then choose the **Reopen** action.</span></span>  
8.  <span data-ttu-id="1e523-138">Corrigeer de post in het veld **Aantal** en boek de inkoopretourorder opnieuw.</span><span class="sxs-lookup"><span data-stu-id="1e523-138">Correct the entry in the **Quantity** field and post the purchase return order again.</span></span>  

## <a name="to-post-a-negative-entry"></a><span data-ttu-id="1e523-139">Een negatieve post boeken</span><span class="sxs-lookup"><span data-stu-id="1e523-139">To post a negative entry</span></span>  
<span data-ttu-id="1e523-140">U kunt het veld **Storno** gebruiken om een negatief debetbedrag in plaats van een creditbedrag te boeken, of om een negatief creditbedrag in plaats van een debetbedrag op een rekening te boeken.</span><span class="sxs-lookup"><span data-stu-id="1e523-140">You can use the **Correction** field to post a negative debit instead of a credit, or to post a negative credit instead of a debit on an account.</span></span> <span data-ttu-id="1e523-141">Om aan juridische vereisten te voldoen is dit veld standaard zichtbaar in alle dagboeken.</span><span class="sxs-lookup"><span data-stu-id="1e523-141">To meet legal requirements, this field is visible by default in all journals.</span></span> <span data-ttu-id="1e523-142">De velden **Debetbedrag** en **Creditbedrag** bevatten beide zowel de oorspronkelijke post als de gecorrigeerde post.</span><span class="sxs-lookup"><span data-stu-id="1e523-142">The **Debit Amount** and **Credit Amount** fields include both the original entry, and the corrected entry.</span></span> <span data-ttu-id="1e523-143">Deze velden hebben geen invloed op het rekeningsaldo.</span><span class="sxs-lookup"><span data-stu-id="1e523-143">These fields have no effect on the account balance.</span></span>  

1.  <span data-ttu-id="1e523-144">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële dagboeken** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="1e523-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link</span></span>  
2.  <span data-ttu-id="1e523-145">Selecteer in het veld **Batchnaam** de juiste batchnaam.</span><span class="sxs-lookup"><span data-stu-id="1e523-145">In the **Batch Name** field, select the required batch name.</span></span>  
3.  <span data-ttu-id="1e523-146">Voer informatie in de relevante velden in.</span><span class="sxs-lookup"><span data-stu-id="1e523-146">Enter information into the relevant fields.</span></span>  
4.  <span data-ttu-id="1e523-147">Selecteer op de dagboekregel die u wilt activeren voor negatieve posten het selectievakje **Storno**.</span><span class="sxs-lookup"><span data-stu-id="1e523-147">In the journal line that you want to activate for negative entries, select the **Correction** check box.</span></span>  
5.  <span data-ttu-id="1e523-148">Als u naar het dagboek wilt boeken, kiest u de actie **Boeken** en kiest u vervolgens de knop **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1e523-148">To post the journal, choose the **Post** action, and then choose the **Yes** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e523-149">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1e523-149">See Also</span></span>
[<span data-ttu-id="1e523-150">Transacties direct naar het grootboek boeken</span><span class="sxs-lookup"><span data-stu-id="1e523-150">Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="1e523-151">Werken met diversendagboeken</span><span class="sxs-lookup"><span data-stu-id="1e523-151">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="1e523-152">Financiën</span><span class="sxs-lookup"><span data-stu-id="1e523-152">Finance</span></span>](finance.md)  
<span data-ttu-id="1e523-153">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1e523-153">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
