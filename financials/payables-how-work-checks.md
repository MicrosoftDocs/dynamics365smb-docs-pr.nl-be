---
title: Cheques afgeven, afdrukken, annuleren, en nietig verklaren| Microsoft Docs
description: Beschrijft hoe u cheques afgeeft met het betalingsdagboek, cheques afdrukt, en chequeposten nietig verklaart of weergeeft in Financials.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 0875164a3afee7a835346a8d4b9323dda9ebf080
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-with-checks"></a><span data-ttu-id="1a82d-103">Procedure: Werken met cheques</span><span class="sxs-lookup"><span data-stu-id="1a82d-103">How to: Work With Checks</span></span>
<span data-ttu-id="1a82d-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)] kunt u elektronische en handmatige cheques verzenden.</span><span class="sxs-lookup"><span data-stu-id="1a82d-104">You can issue electronic and manual checks in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="1a82d-105">Bij beide methoden wordt het betalingsdagboek gebruikt om cheques te verzenden naar leveranciers.</span><span class="sxs-lookup"><span data-stu-id="1a82d-105">Both methods use the payment journal to issue checks to vendors.</span></span> <span data-ttu-id="1a82d-106">Daarnaast kunt u cheques nietig verklaren en chequeposten weergeven.</span><span class="sxs-lookup"><span data-stu-id="1a82d-106">You can also void checks and view check ledger entries.</span></span>

<span data-ttu-id="1a82d-107">Bij het proces voor het uitgeven van cheques worden betalingen voorgesteld, worden posten gemaakt en worden de computercheques afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="1a82d-107">The process of issuing checks suggests payments, creates ledger entries, and prints the computer checks.</span></span>

> [!NOTE]  
>   <span data-ttu-id="1a82d-108">Om ervoor te zorgen dat uw bank alleen gevalideerde cheques en bedragen vrijgeeft, kunt u deze verzenden in een bestand dat gegevens over de leverancier, cheque en betaling bevat.</span><span class="sxs-lookup"><span data-stu-id="1a82d-108">To make sure that your bank only clears validated checks and amounts, you can send them a file that contains vendor, check, and payment information.</span></span> <span data-ttu-id="1a82d-109">Zie voor meer informatie [Procedure: Een Positive Pay-bestand exporteren](finance-how-positive-pay.md).</span><span class="sxs-lookup"><span data-stu-id="1a82d-109">For more information, see [How to: Export a Positive Pay file](finance-how-positive-pay.md).</span></span>

<span data-ttu-id="1a82d-110">De printer moet correct zijn ingesteld op het afdrukken van chequeformulieren en u moet bepalen welke indeling wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1a82d-110">Your printer must be correctly set up with the check forms, and you must define which check layout to use.</span></span> <span data-ttu-id="1a82d-111">Zie voor meer informatie [Procedure: Cheque-indelingen definiëren](finance-how-define-check-layouts.md)</span><span class="sxs-lookup"><span data-stu-id="1a82d-111">For more information, see [How to: Define Check Layouts](finance-how-define-check-layouts.md)</span></span>

## <a name="to-issue-checks"></a><span data-ttu-id="1a82d-112">Cheques uitgeven</span><span class="sxs-lookup"><span data-stu-id="1a82d-112">To issue checks</span></span>
1. <span data-ttu-id="1a82d-113">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsdagboeken** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="1a82d-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="1a82d-114">Vul het dagboek met relevante betalingen, bijvoorbeeld met behulp van de functie Leveranciersbetalingen voorstellen.</span><span class="sxs-lookup"><span data-stu-id="1a82d-114">Fill in the journal with relevant payments, for example by using the Suggest Vendor Payments function.</span></span> <span data-ttu-id="1a82d-115">Zie voor meer informatie [Procedure: Leveranciersbetalingen voorstellen](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="1a82d-115">For more information, see [How to: Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>
3. <span data-ttu-id="1a82d-116">Selecteer een van de volgende opties in het veld **Betalingssoort** op dagboekregels voor betalingen die u wilt doen met cheques:</span><span class="sxs-lookup"><span data-stu-id="1a82d-116">In the **Bank Payment Type** field on journal lines for payment that you want to make with checks, select one of the following options:</span></span>

   * <span data-ttu-id="1a82d-117">**Automatische cheque**: selecteer deze optie als u een cheque wilt afdrukken voor het bedrag op de betalingsdagboekregel.</span><span class="sxs-lookup"><span data-stu-id="1a82d-117">**Computer Check**: Select this option if you want to print a check for the amount on the payment journal line.</span></span> <span data-ttu-id="1a82d-118">U moet de cheques afdrukken voordat u de dagboekregels kunt boeken.</span><span class="sxs-lookup"><span data-stu-id="1a82d-118">You must print the checks before you can post the journal lines.</span></span> <span data-ttu-id="1a82d-119">U kunt **Automatische cheque** alleen selecteren als het **Tegenrekeningsoort** of het **Rekeningsoort** **Bankrekening** is.</span><span class="sxs-lookup"><span data-stu-id="1a82d-119">You can only select **Computer Check** if the **Bal. Account Type** or the **Account Type** is **Bank Account**.</span></span>
   * <span data-ttu-id="1a82d-120">**Handmatige cheque**: selecteer deze optie als u handmatig een cheque hebt gemaakt en er een bijbehorende chequepost moet worden gemaakt voor dit bedrag.</span><span class="sxs-lookup"><span data-stu-id="1a82d-120">**Manual Check**: Select this option if you have created a check manually and want to create a corresponding check ledger entry for this amount.</span></span> <span data-ttu-id="1a82d-121">Met deze optie kunt u geen cheques afdrukken vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="1a82d-121">By using this option, you cannot print checks from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="1a82d-122">U kunt **Handmatige cheque** alleen selecteren als het **Tegenrekeningsoort** of het **Rekeningsoort** **Bankrekening** is.</span><span class="sxs-lookup"><span data-stu-id="1a82d-122">You can only select **Manual Check** if the **Bal. Account Type** or the **Account Type** is **Bank Account**.</span></span>

     > [!NOTE]  
>   <span data-ttu-id="1a82d-123">U moet computercheques afdrukken voordat u de gerelateerde dagboekregels boekt.</span><span class="sxs-lookup"><span data-stu-id="1a82d-123">You must print computer checks before you post the related journal lines.</span></span>
4. <span data-ttu-id="1a82d-124">In het geval van automatische cheques kiest u **Cheque afdrukken**.</span><span class="sxs-lookup"><span data-stu-id="1a82d-124">In case of computer checks, choose **Print Check**.</span></span>
5. <span data-ttu-id="1a82d-125">Vul indien nodig de velden in het venster **Cheque** in.</span><span class="sxs-lookup"><span data-stu-id="1a82d-125">In the **Check** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. <span data-ttu-id="1a82d-126">Klik op **Afdrukken**.</span><span class="sxs-lookup"><span data-stu-id="1a82d-126">Choose the **Print** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="1a82d-127">Als u cheques in meerdere valuta's van verschillende bankrekeningen wilt afdrukken, moet u de batchverwerking **Cheque afdrukken** voor elke valuta afzonderlijk uitvoeren en de juiste bankrekening opgeven.</span><span class="sxs-lookup"><span data-stu-id="1a82d-127">If you want to print checks in more than one currency from different bank accounts, you must run the **Print Check** batch job separately for each currency and specify the appropriate bank account.</span></span>

## <a name="to-cancel-printed-checks-that-are-not-posted"></a><span data-ttu-id="1a82d-128">Afgedrukte cheques annuleren die niet zijn geboekt</span><span class="sxs-lookup"><span data-stu-id="1a82d-128">To cancel printed checks that are not posted</span></span>
<span data-ttu-id="1a82d-129">U kunt niet-geboekte cheques annuleren nadat ze zijn afgedrukt door de actie **Ongeldige cheque** in het venster **Betalingsdagboek** te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="1a82d-129">You can cancel non-posted checks after they have been printed by using the **Void Check** action in the **Payment Journal** window.</span></span>

1. <span data-ttu-id="1a82d-130">Kies in het venster **Betalingsdagboek** de actie **Ongeldige cheque** en kies vervolgens welke cheques u wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="1a82d-130">In the **Payment Journal** window, choose the **Void Check**, and then choose which checks to cancel.</span></span>

## <a name="to-void-checks"></a><span data-ttu-id="1a82d-131">Cheques nietig verklaren</span><span class="sxs-lookup"><span data-stu-id="1a82d-131">To void checks</span></span>
<span data-ttu-id="1a82d-132">Wanneer chequebetaling is geboekt, kunt u cheques alleen annuleren (nietig verklaren) vanuit de resulterende bankposten.</span><span class="sxs-lookup"><span data-stu-id="1a82d-132">When check payment have been posted, you can only cancel (void) checks from the resulting bank ledger entries.</span></span>

1. <span data-ttu-id="1a82d-133">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bankrekeningen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="1a82d-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="1a82d-134">Selecteer de betreffende bankrekening, kies de actie **Bewerken** en kies vervolgens de actie **Chequeposten**.</span><span class="sxs-lookup"><span data-stu-id="1a82d-134">Select the relevant bank account, choose the **Edit** action, and then choose the **Check Ledger Entries** action.</span></span>
3. <span data-ttu-id="1a82d-135">Kies in het venster **Chequeposten** de actie **Ongeldige cheque**.</span><span class="sxs-lookup"><span data-stu-id="1a82d-135">In the **Check Ledger Entries** window, choose the **Void Check** action.</span></span>
4. <span data-ttu-id="1a82d-136">Schakel het selectievakje **Cheque alleen nietig verklaren** in.</span><span class="sxs-lookup"><span data-stu-id="1a82d-136">Select the **Void Check Only** check box.</span></span>
5. <span data-ttu-id="1a82d-137">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="1a82d-137">Choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a82d-138">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1a82d-138">See Also</span></span>
[<span data-ttu-id="1a82d-139">Betalingsverplichtingen beheren</span><span class="sxs-lookup"><span data-stu-id="1a82d-139">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="1a82d-140">Bankieren instellen</span><span class="sxs-lookup"><span data-stu-id="1a82d-140">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="1a82d-141">Procedure: Een Positive Pay-bestand exporteren</span><span class="sxs-lookup"><span data-stu-id="1a82d-141">How to: Export a Positive Pay file</span></span>](finance-how-positive-pay.md)  
<span data-ttu-id="1a82d-142">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1a82d-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

