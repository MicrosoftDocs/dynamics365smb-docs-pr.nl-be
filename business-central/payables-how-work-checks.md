---
title: Cheques afgeven, afdrukken, annuleren, en nietig verklaren| Microsoft Docs
description: Beschrijft hoe u cheques afgeeft met het betalingsdagboek, cheques afdrukt, en chequeposten nietig verklaart of weergeeft in Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 04/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: db28ad9a4adb45514b1d1287d269d8daefe64865
ms.openlocfilehash: 39b48fbd34b29db56b39712fbd2cbf5dc91fefc6
ms.contentlocale: nl-be
ms.lasthandoff: 04/26/2018

---
# <a name="make-check-payments"></a><span data-ttu-id="40441-103">Chequebetalingen doen</span><span class="sxs-lookup"><span data-stu-id="40441-103">Make Check Payments</span></span>
<span data-ttu-id="40441-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)] kunt u elektronische en handmatige cheques verzenden.</span><span class="sxs-lookup"><span data-stu-id="40441-104">You can issue electronic and manual checks in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="40441-105">Bij beide methoden wordt het betalingsdagboek gebruikt om cheques te verzenden naar leveranciers.</span><span class="sxs-lookup"><span data-stu-id="40441-105">Both methods use the payment journal to issue checks to vendors.</span></span> <span data-ttu-id="40441-106">Daarnaast kunt u cheques nietig verklaren en chequeposten weergeven.</span><span class="sxs-lookup"><span data-stu-id="40441-106">You can also void checks and view check ledger entries.</span></span>

<span data-ttu-id="40441-107">In de volgende procedure wordt beschreven hoe u een leverancier betaalt met een computercheque door de betaling te vereffenen met de relevante leveranciersfactuur, de cheque af te drukken en vervolgens de betaling te boeken als betaald.</span><span class="sxs-lookup"><span data-stu-id="40441-107">The following procedure shows how to pay a vendor with a computer checks by applying the payment to the relevant vendor invoice, printing the check, and then posting the payment as paid.</span></span> <span data-ttu-id="40441-108">Dit leidt tot positieve leveranciersposten die worden vereffend met negatieve bankposten en fysieke cheques voor verwerking in de bank.</span><span class="sxs-lookup"><span data-stu-id="40441-108">This results in positive vendor ledger entries, applied to negative bank ledger entries, and physical checks for processing in the bank.</span></span>

<span data-ttu-id="40441-109">U kunt met twee soorten cheques betalen.</span><span class="sxs-lookup"><span data-stu-id="40441-109">You can pay with two types of checks.</span></span> <span data-ttu-id="40441-110">Voor beide soorten moet het veld **Tegenrekeningtype** of **Rekeningsoort** **Bankrekening** bevatten.</span><span class="sxs-lookup"><span data-stu-id="40441-110">For both types, the **Bal. Account Type** or the **Account Type** field must contain **Bank Account**.</span></span>

- <span data-ttu-id="40441-111">**Automatische cheque**: selecteer deze optie als u een cheque wilt afdrukken voor het bedrag op de betalingsdagboekregel.</span><span class="sxs-lookup"><span data-stu-id="40441-111">**Computer Check**: Select this option if you want to print a check for the amount on the payment journal line.</span></span> <span data-ttu-id="40441-112">U moet de cheques afdrukken voordat u de dagboekregels kunt boeken.</span><span class="sxs-lookup"><span data-stu-id="40441-112">You must print the checks before you can post the journal lines.</span></span> <span data-ttu-id="40441-113">U kunt **Automatische cheque** alleen selecteren als</span><span class="sxs-lookup"><span data-stu-id="40441-113">You can only select **Computer Check** if</span></span>
- <span data-ttu-id="40441-114">**Handmatige cheque**: selecteer deze optie als u handmatig een cheque hebt gemaakt en er een bijbehorende chequepost moet worden gemaakt voor dit bedrag.</span><span class="sxs-lookup"><span data-stu-id="40441-114">**Manual Check**: Select this option if you have created a check manually and want to create a corresponding check ledger entry for this amount.</span></span> <span data-ttu-id="40441-115">Met deze optie kunt u de cheque niet afdrukken.</span><span class="sxs-lookup"><span data-stu-id="40441-115">By using this option, you cannot print the check.</span></span>

> [!NOTE]  
> <span data-ttu-id="40441-116">Om ervoor te zorgen dat uw bank alleen gevalideerde cheques en bedragen vrijgeeft, kunt u deze verzenden in een bestand dat gegevens over de leverancier, cheque en betaling bevat.</span><span class="sxs-lookup"><span data-stu-id="40441-116">To make sure that your bank only clears validated checks and amounts, you can send them a file that contains vendor, check, and payment information.</span></span> <span data-ttu-id="40441-117">Zie voor meer informatie [Een Positive Pay-bestand exporteren](finance-how-positive-pay.md).</span><span class="sxs-lookup"><span data-stu-id="40441-117">For more information, see [Export a Positive Pay file](finance-how-positive-pay.md).</span></span>

<span data-ttu-id="40441-118">De printer moet correct zijn ingesteld op het afdrukken van chequeformulieren en u moet bepalen welke indeling wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="40441-118">Your printer must be correctly set up with the check forms, and you must define which check layout to use.</span></span> <span data-ttu-id="40441-119">Zie voor meer informatie [Cheque-indelingen definiëren](finance-how-define-check-layouts.md)</span><span class="sxs-lookup"><span data-stu-id="40441-119">For more information, see [Define Check Layouts](finance-how-define-check-layouts.md)</span></span>

## <a name="to-pay-a-vendor-invoice-with-a-computer-check"></a><span data-ttu-id="40441-120">Een leverancier betalen met een automatische cheque</span><span class="sxs-lookup"><span data-stu-id="40441-120">To pay a vendor invoice with a computer check</span></span>
<span data-ttu-id="40441-121">Hierna wordt beschreven hoe u een leverancier per cheque betaalt.</span><span class="sxs-lookup"><span data-stu-id="40441-121">The following describes how to pay a vendor by check.</span></span> <span data-ttu-id="40441-122">De stappen zijn vergelijkbaar met het terugbetalen van een klant per cheque.</span><span class="sxs-lookup"><span data-stu-id="40441-122">The steps are similar to refund a customer by check.</span></span>

1. <span data-ttu-id="40441-123">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsdagboeken** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="40441-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="40441-124">Vul de betalingsdagboekregels in.</span><span class="sxs-lookup"><span data-stu-id="40441-124">Fill in the payment journal lines.</span></span> <span data-ttu-id="40441-125">Zie voor meer informatie [Betalingen en terugbetalingen vastleggen](payables-how-post-payments-refunds.md).</span><span class="sxs-lookup"><span data-stu-id="40441-125">For more information, see [Record Payments and Refunds](payables-how-post-payments-refunds.md).</span></span>
3. <span data-ttu-id="40441-126">Selecteer **Cheque** in het veld **Betalingswijze**.</span><span class="sxs-lookup"><span data-stu-id="40441-126">In the **Payment Method Code** field, select **Check**.</span></span>
4. <span data-ttu-id="40441-127">Selecteer **Automatische cheque** in het veld **Betalingssoort**.</span><span class="sxs-lookup"><span data-stu-id="40441-127">In the **Bank Payment Type** field, select **Computer Check**.</span></span>
5. <span data-ttu-id="40441-128">Kies de actie **Cheque afdrukken**.</span><span class="sxs-lookup"><span data-stu-id="40441-128">Choose the **Print Check** action.</span></span>
6. <span data-ttu-id="40441-129">Vul indien nodig de velden in het venster **Cheque** in.</span><span class="sxs-lookup"><span data-stu-id="40441-129">In the **Check** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. <span data-ttu-id="40441-130">Kies de knop **Verzenden naar**, selecteer de optie **PDF-document**, en kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="40441-130">Choose the **Send to** button, select the **PDF Document** option, and then choose the **OK** button.</span></span>

    <span data-ttu-id="40441-131">De fysieke cheques kunnen nu naar de bank worden gebracht voor verwerking.</span><span class="sxs-lookup"><span data-stu-id="40441-131">The physical checks can now be brought to the bank for processing.</span></span> <span data-ttu-id="40441-132">Boek de betaling zoals vereffend met de leverancier en daarmee betaald in het systeem.</span><span class="sxs-lookup"><span data-stu-id="40441-132">Proceed to post the payment as applied to the vendor and thereby paid in the system.</span></span>
8. <span data-ttu-id="40441-133">Kies de actie **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="40441-133">Choose the **Post** action.</span></span>

<span data-ttu-id="40441-134">Er worden volledig vereffende leveranciersposten en bankposten gemaakt.</span><span class="sxs-lookup"><span data-stu-id="40441-134">Fully applied vendor ledger entries and bank ledger entries are created.</span></span>

> [!NOTE]  
> <span data-ttu-id="40441-135">Als u cheques in meerdere valuta's van verschillende bankrekeningen wilt afdrukken en betalen, moet u de batchverwerking **Cheque afdrukken** voor elke valuta afzonderlijk uitvoeren en de juiste bankrekening opgeven.</span><span class="sxs-lookup"><span data-stu-id="40441-135">If you want to print and pay checks in more than one currency from different bank accounts, you must run the **Print Check** batch job separately for each currency and specify the appropriate bank account.</span></span>

## <a name="to-cancel-printed-checks-that-are-not-posted"></a><span data-ttu-id="40441-136">Afgedrukte cheques annuleren die niet zijn geboekt</span><span class="sxs-lookup"><span data-stu-id="40441-136">To cancel printed checks that are not posted</span></span>
<span data-ttu-id="40441-137">U kunt niet-geboekte cheques annuleren nadat ze zijn afgedrukt door de actie **Ongeldige cheque** in het venster **Betalingsdagboek** te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="40441-137">You can cancel non-posted checks after they have been printed by using the **Void Check** action in the **Payment Journal** window.</span></span>

1. <span data-ttu-id="40441-138">Kies in het venster **Betalingsdagboek** de actie **Ongeldige cheque** en kies vervolgens welke cheques u wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="40441-138">In the **Payment Journal** window, choose the **Void Check**, and then choose which checks to cancel.</span></span>

## <a name="to-void-checks"></a><span data-ttu-id="40441-139">Cheques nietig verklaren</span><span class="sxs-lookup"><span data-stu-id="40441-139">To void checks</span></span>
<span data-ttu-id="40441-140">Wanneer chequebetaling is geboekt, kunt u cheques alleen annuleren (nietig verklaren) vanuit de resulterende bankposten.</span><span class="sxs-lookup"><span data-stu-id="40441-140">When check payment have been posted, you can only cancel (void) checks from the resulting bank ledger entries.</span></span>

1. <span data-ttu-id="40441-141">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bankrekeningen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="40441-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="40441-142">Selecteer de betreffende bankrekening, kies de actie **Bewerken** en kies vervolgens de actie **Chequeposten**.</span><span class="sxs-lookup"><span data-stu-id="40441-142">Select the relevant bank account, choose the **Edit** action, and then choose the **Check Ledger Entries** action.</span></span>
3. <span data-ttu-id="40441-143">Kies in het venster **Chequeposten** de actie **Ongeldige cheque**.</span><span class="sxs-lookup"><span data-stu-id="40441-143">In the **Check Ledger Entries** window, choose the **Void Check** action.</span></span>
4. <span data-ttu-id="40441-144">Schakel het selectievakje **Cheque alleen nietig verklaren** in.</span><span class="sxs-lookup"><span data-stu-id="40441-144">Select the **Void Check Only** check box.</span></span>
5. <span data-ttu-id="40441-145">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="40441-145">Choose the **OK** button.</span></span>

## <a name="to-view-a-summary-of-posted-checks"></a><span data-ttu-id="40441-146">Een overzicht weergeven van geboekte cheques</span><span class="sxs-lookup"><span data-stu-id="40441-146">To view a summary of posted checks</span></span>
<span data-ttu-id="40441-147">Als u geboekte cheques wilt controleren, bijvoorbeeld om meerdere cheques te verifiëren die aan één leverancier zijn betaald, kunt u het rapport **Bank - Cheques Detail** gebruiken.</span><span class="sxs-lookup"><span data-stu-id="40441-147">If you want to review posted checks, for example to verify multiple checks paid to one vendor, you can use the **Bank Account - Check Details** report.</span></span>
1. <span data-ttu-id="40441-148">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bank - Cheques Detail** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="40441-148">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Account - Check Details**, and then choose the related link.</span></span>
2. <span data-ttu-id="40441-149">Stel filters als relevant in en kies de knop **Voorbeeld**.</span><span class="sxs-lookup"><span data-stu-id="40441-149">Set filters as relevant, and then choose the **Preview** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="40441-150">Zie ook</span><span class="sxs-lookup"><span data-stu-id="40441-150">See Also</span></span>
[<span data-ttu-id="40441-151">Betalingen uitvoeren</span><span class="sxs-lookup"><span data-stu-id="40441-151">Making Payments</span></span>](payables-make-payments.md)  
[<span data-ttu-id="40441-152">Betalingsverplichtingen beheren</span><span class="sxs-lookup"><span data-stu-id="40441-152">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="40441-153">Bankieren instellen</span><span class="sxs-lookup"><span data-stu-id="40441-153">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="40441-154">Een Positive Pay-bestand exporteren</span><span class="sxs-lookup"><span data-stu-id="40441-154">Export a Positive Pay file</span></span>](finance-how-positive-pay.md)  
<span data-ttu-id="40441-155">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="40441-155">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

