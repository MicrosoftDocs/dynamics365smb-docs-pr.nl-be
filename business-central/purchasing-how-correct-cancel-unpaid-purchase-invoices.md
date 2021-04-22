---
title: Niet-betaalde inkoopfacturen wijzigen of annuleren | Microsoft Docs
description: Verklaart hoe u een geboekte inkoopfactuur corrigeert, annuleert of ongedaan maakt, en hoe u automatisch een inkoopcreditnota gemaakt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b2e2e64cd3845f20e9c3e0fea5c114ebcd08491d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5780244"
---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a><span data-ttu-id="c5070-103">Niet-betaalde inkoopfacturen corrigeren of annuleren</span><span class="sxs-lookup"><span data-stu-id="c5070-103">Correct or Cancel Unpaid Purchase Invoices</span></span>

<span data-ttu-id="c5070-104">U kunt een geboekte inkoopfactuur corrigeren of annuleren.</span><span class="sxs-lookup"><span data-stu-id="c5070-104">You can correct or cancel a posted purchase invoice.</span></span> <span data-ttu-id="c5070-105">Dit is handig als u een typefout wilt corrigeren of als u de aankoop in het begin van het orderproces wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c5070-105">This is useful if you want to correct a typing mistake, or if you want to change the purchase early in the order process.</span></span>

<span data-ttu-id="c5070-106">Als u al hebt betaald voor producten op de geboekte inkoopfactuur, kunt u deze niet corrigeren of annuleren vanuit de geboekte inkoopfactuur zelf.</span><span class="sxs-lookup"><span data-stu-id="c5070-106">If you have already paid for products on the posted purchase invoice, you cannot correct or cancel it from the posted purchase invoice itself.</span></span> <span data-ttu-id="c5070-107">In plaats hiervan moet u handmatig een inkoopcreditnota maken om de aankoop tegen te boeken, optioneel aangestuurd met een inkoopretourorder.</span><span class="sxs-lookup"><span data-stu-id="c5070-107">Instead, you must manually create a purchase credit memo to reverse the purchase, optionally managed with a purchase return order.</span></span> <span data-ttu-id="c5070-108">Hetzelfde geldt als u een geboekte inkoopfactuur wilt wijzigen die is gebaseerd op gecombineerde inkoopontvangsten.</span><span class="sxs-lookup"><span data-stu-id="c5070-108">The same applies if you want to modify a posted purchase invoice that was based on combined purchase receipts.</span></span> <span data-ttu-id="c5070-109">Zie voor meer informatie [Inkoopretouren of annuleringen verwerken](purchasing-how-process-purchase-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="c5070-109">For more information, see [Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md).</span></span>

<span data-ttu-id="c5070-110">Op de pagina **Geboekte inkoopfacturen** kunt u de knop **Corrigeren** of de knop **Annuleren** kiezen.</span><span class="sxs-lookup"><span data-stu-id="c5070-110">On the **Posted Purchase Invoice** page, you can choose the **Correct** button or the **Cancel** button.</span></span> <span data-ttu-id="c5070-111">Wanneer u een geboekte inkoopfactuur wijzigt of annuleert, wordt de corrigerende inkoopcreditnota toegepast op alle algemene grootboekposten en inventarisatieposten die werden gemaakt toen de aanvankelijke inkoopfactuur werd geboekt.</span><span class="sxs-lookup"><span data-stu-id="c5070-111">When you correct or cancel a posted purchase invoice, the corrective purchase credit memo is applied to all general ledger and inventory ledger entries that were created when the initial purchase invoice was posted.</span></span> <span data-ttu-id="c5070-112">Hiermee voert u een tegenboeking uit van de geboekte inkoopfactuur in uw financiële records en laat u de gecorrigeerde inkoopcreditnota staan voor uw auditcontrole.</span><span class="sxs-lookup"><span data-stu-id="c5070-112">This reverses the posted purchase invoice in your financial records and leaves the corrective posted purchase credit memo for your audit trail.</span></span> <span data-ttu-id="c5070-113">Hieronder wordt het gebruik van **Corrigeren** en **Annuleren** beschreven.</span><span class="sxs-lookup"><span data-stu-id="c5070-113">In the following the use of **Correct** and **Cancel** is described.</span></span>
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE4dhoc?rel=0]

## <a name="to-correct-a-posted-purchase-invoice"></a><span data-ttu-id="c5070-114">Een geboekte inkoopfactuur corrigeren</span><span class="sxs-lookup"><span data-stu-id="c5070-114">To correct a posted purchase invoice</span></span>
1. <span data-ttu-id="c5070-115">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Geboekte inkoopfacturen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="c5070-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c5070-116">Selecteer de geboekte inkoopfactuur die u wilt corrigeren.</span><span class="sxs-lookup"><span data-stu-id="c5070-116">Select the posted purchase invoice that you want to correct.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="c5070-117">Als het selectievakje **Geannuleerd** is geselecteerd, kunt u de geboekte inkoopfactuur niet corrigeren omdat deze al is gecorrigeerd of geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="c5070-117">If the **Canceled** check box is selected, then you cannot correct the posted purchase invoice because it has already been corrected or canceled.</span></span>
3. <span data-ttu-id="c5070-118">Kies op de pagina **Geboekte inkoopfactuur** **Corrigeren**.</span><span class="sxs-lookup"><span data-stu-id="c5070-118">On the **Posted Purchase Invoice** page, choose **Correct**.</span></span>

    <span data-ttu-id="c5070-119">Een nieuwe inkoopfactuur met dezelfde gegevens wordt gemaakt waar u de correctie kunt maken.</span><span class="sxs-lookup"><span data-stu-id="c5070-119">A new purchase invoice with the same information is created where you can make the correction.</span></span> <span data-ttu-id="c5070-120">Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="c5070-120">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span> <span data-ttu-id="c5070-121">Het veld **Geannuleerd** op de eerste geboekte inkoopfactuur is gewijzigd in **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c5070-121">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>

    <span data-ttu-id="c5070-122">Een inkoopcreditnota wordt automatisch gemaakt en geboekt om de oorspronkelijke geboekte inkoopfactuur nietig te verklaren.</span><span class="sxs-lookup"><span data-stu-id="c5070-122">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span>
4. <span data-ttu-id="c5070-123">Kies **Corrigerende creditnota tonen** om de geboekte inkoopcreditnota weer te geven die de in eerste instantie geboekte inkoopfactuur nietig verklaart.</span><span class="sxs-lookup"><span data-stu-id="c5070-123">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="to-cancel-a-posted-purchase-invoice"></a><span data-ttu-id="c5070-124">Een geboekte inkoopfactuur annuleren</span><span class="sxs-lookup"><span data-stu-id="c5070-124">To cancel a posted purchase invoice</span></span>
1. <span data-ttu-id="c5070-125">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Geboekte inkoopfacturen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="c5070-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c5070-126">Selecteer de geboekte inkoopfactuur die u wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="c5070-126">Select the posted purchase invoice that you want to cancel.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="c5070-127">Als het selectievakje **Geannuleerd** is geselecteerd, kunt u de geboekte inkoopfactuur niet annuleren omdat deze al is geannuleerd of gecorrigeerd.</span><span class="sxs-lookup"><span data-stu-id="c5070-127">If the **Canceled** check box is selected, then you cannot cancel the posted purchase invoice because it has already been canceled or corrected.</span></span>
3. <span data-ttu-id="c5070-128">Kies op de pagina **Geboekte inkoopfactuur** **Annuleren**.</span><span class="sxs-lookup"><span data-stu-id="c5070-128">On the **Posted Purchase Invoice** page, choose **Cancel**.</span></span>

    <span data-ttu-id="c5070-129">Een inkoopcreditnota wordt automatisch gemaakt en geboekt om de oorspronkelijke geboekte inkoopfactuur nietig te verklaren.</span><span class="sxs-lookup"><span data-stu-id="c5070-129">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span> <span data-ttu-id="c5070-130">Het veld **Geannuleerd** op de eerste geboekte inkoopfactuur is gewijzigd in **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c5070-130">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>
4. <span data-ttu-id="c5070-131">Kies **Corrigerende creditnota tonen** om de geboekte inkoopcreditnota weer te geven die de in eerste instantie geboekte inkoopfactuur nietig verklaart.</span><span class="sxs-lookup"><span data-stu-id="c5070-131">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

### <a name="partial-invoice-posting-also-supported"></a><span data-ttu-id="c5070-132">Gedeeltelijke factuurboeking wordt ook ondersteund</span><span class="sxs-lookup"><span data-stu-id="c5070-132">Partial Invoice Posting also Supported</span></span>
<span data-ttu-id="c5070-133">Als de annulering betrekking heeft op een gedeeltelijke factuurboeking, wordt de oorspronkelijke inkooporderregel bijgewerkt om de geannuleerde gefactureerde hoeveelheid weer te geven.</span><span class="sxs-lookup"><span data-stu-id="c5070-133">If the cancellation is related to a partial invoice posting, then the originating purchase order line is updated to reflect the canceled invoiced quantity.</span></span> <span data-ttu-id="c5070-134">De velden **Te factureren aantal** en **Aantal gefactureerd** op de gerelateerde inkooporderregel worden opnieuw ingesteld op de waarden vóór de gedeeltelijke boeking.</span><span class="sxs-lookup"><span data-stu-id="c5070-134">The **Qty. to Invoice** and **Qty. Invoiced** fields on the related purchase order line are reset to the values before the partial posting.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5070-135">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c5070-135">See Also</span></span>
[<span data-ttu-id="c5070-136">Inkoop</span><span class="sxs-lookup"><span data-stu-id="c5070-136">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="c5070-137">Inkopen vastleggen</span><span class="sxs-lookup"><span data-stu-id="c5070-137">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="c5070-138">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c5070-138">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]