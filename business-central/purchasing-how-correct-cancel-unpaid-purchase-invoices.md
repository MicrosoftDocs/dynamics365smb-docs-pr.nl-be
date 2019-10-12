---
title: Niet-betaalde inkoopfacturen wijzigen of annuleren | Microsoft Docs
description: Verklaart hoe u een geboekte inkoopfactuur corrigeert, annuleert of ongedaan maakt, en hoe u automatisch een inkoopcreditnota gemaakt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 52d2b578d4703d4df38c9431f4554855fd146d87
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312568"
---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a><span data-ttu-id="d2edc-103">Niet-betaalde inkoopfacturen corrigeren of annuleren</span><span class="sxs-lookup"><span data-stu-id="d2edc-103">Correct or Cancel Unpaid Purchase Invoices</span></span>
<span data-ttu-id="d2edc-104">U kunt een geboekte inkoopfactuur corrigeren of annuleren.</span><span class="sxs-lookup"><span data-stu-id="d2edc-104">You can correct or cancel a posted purchase invoice.</span></span> <span data-ttu-id="d2edc-105">Dit is handig als u een typefout wilt corrigeren of als u de aankoop in het begin van het orderproces wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="d2edc-105">This is useful if you want to correct a typing mistake, or if you want to change the purchase early in the order process.</span></span>

<span data-ttu-id="d2edc-106">Als u al hebt betaald voor producten op de geboekte inkoopfactuur, kunt u deze niet corrigeren of annuleren vanuit de geboekte inkoopfactuur zelf.</span><span class="sxs-lookup"><span data-stu-id="d2edc-106">If you have already paid for products on the posted purchase invoice, you cannot correct or cancel it from the posted purchase invoice itself.</span></span> <span data-ttu-id="d2edc-107">In plaats hiervan moet u handmatig een inkoopcreditnota maken om de aankoop tegen te boeken, optioneel aangestuurd met een inkoopretourorder.</span><span class="sxs-lookup"><span data-stu-id="d2edc-107">Instead, you must manually create a purchase credit memo to reverse the purchase, optionally managed with a purchase return order.</span></span> <span data-ttu-id="d2edc-108">Zie voor meer informatie [Inkoopretouren of annuleringen verwerken](purchasing-how-process-purchase-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="d2edc-108">For more information, see [Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md).</span></span>

<span data-ttu-id="d2edc-109">Op de pagina **Geboekte inkoopfacturen** kunt u de knop **Corrigeren** of de knop **Annuleren** kiezen.</span><span class="sxs-lookup"><span data-stu-id="d2edc-109">On the **Posted Purchase Invoice** page, you can choose the **Correct** button or the **Cancel** button.</span></span> <span data-ttu-id="d2edc-110">Wanneer u een geboekte inkoopfactuur wijzigt of annuleert, wordt de corrigerende inkoopcreditnota toegepast op alle algemene grootboekposten en inventarisatieposten die werden gemaakt toen de aanvankelijke inkoopfactuur werd geboekt.</span><span class="sxs-lookup"><span data-stu-id="d2edc-110">When you correct or cancel a posted purchase invoice, the corrective purchase credit memo is applied to all general ledger and inventory ledger entries that were created when the initial purchase invoice was posted.</span></span> <span data-ttu-id="d2edc-111">Hiermee voert u een tegenboeking uit van de geboekte inkoopfactuur in uw financiële records en laat u de gecorrigeerde inkoopcreditnota staan voor uw auditcontrole.</span><span class="sxs-lookup"><span data-stu-id="d2edc-111">This reverses the posted purchase invoice in your financial records and leaves the corrective posted purchase credit memo for your audit trail.</span></span> <span data-ttu-id="d2edc-112">Hieronder wordt het gebruik van **Corrigeren** en **Annuleren** beschreven.</span><span class="sxs-lookup"><span data-stu-id="d2edc-112">In the following the use of **Correct** and **Cancel** is described.</span></span>

## <a name="to-correct-a-posted-purchase-invoice"></a><span data-ttu-id="d2edc-113">Een geboekte inkoopfactuur corrigeren</span><span class="sxs-lookup"><span data-stu-id="d2edc-113">To correct a posted purchase invoice</span></span>
1. <span data-ttu-id="d2edc-114">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Geboekte inkoopfacturen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="d2edc-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d2edc-115">Selecteer de geboekte inkoopfactuur die u wilt corrigeren.</span><span class="sxs-lookup"><span data-stu-id="d2edc-115">Select the posted purchase invoice that you want to correct.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="d2edc-116">Als het selectievakje **Geannuleerd** is geselecteerd, kunt u de geboekte inkoopfactuur niet corrigeren omdat deze al is gecorrigeerd of geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="d2edc-116">If the **Canceled** check box is selected, then you cannot correct the posted purchase invoice because it has already been corrected or canceled.</span></span>
3. <span data-ttu-id="d2edc-117">Kies op de pagina **Geboekte inkoopfactuur** **Corrigeren**.</span><span class="sxs-lookup"><span data-stu-id="d2edc-117">On the **Posted Purchase Invoice** page, choose **Correct**.</span></span>

    <span data-ttu-id="d2edc-118">Een nieuwe inkoopfactuur met dezelfde gegevens wordt gemaakt waar u de correctie kunt maken.</span><span class="sxs-lookup"><span data-stu-id="d2edc-118">A new purchase invoice with the same information is created where you can make the correction.</span></span> <span data-ttu-id="d2edc-119">Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="d2edc-119">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span> <span data-ttu-id="d2edc-120">Het veld **Geannuleerd** op de eerste geboekte inkoopfactuur is gewijzigd in **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d2edc-120">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>

    <span data-ttu-id="d2edc-121">Een inkoopcreditnota wordt automatisch gemaakt en geboekt om de oorspronkelijke geboekte inkoopfactuur nietig te verklaren.</span><span class="sxs-lookup"><span data-stu-id="d2edc-121">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span>
4. <span data-ttu-id="d2edc-122">Kies **Corrigerende creditnota tonen** om de geboekte inkoopcreditnota weer te geven die de in eerste instantie geboekte inkoopfactuur nietig verklaart.</span><span class="sxs-lookup"><span data-stu-id="d2edc-122">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="to-cancel-a-posted-purchase-invoice"></a><span data-ttu-id="d2edc-123">Een geboekte inkoopfactuur annuleren</span><span class="sxs-lookup"><span data-stu-id="d2edc-123">To cancel a posted purchase invoice</span></span>
1. <span data-ttu-id="d2edc-124">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Geboekte inkoopfacturen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="d2edc-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d2edc-125">Selecteer de geboekte inkoopfactuur die u wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="d2edc-125">Select the posted purchase invoice that you want to cancel.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="d2edc-126">Als het selectievakje **Geannuleerd** is geselecteerd, kunt u de geboekte inkoopfactuur niet annuleren omdat deze al is geannuleerd of gecorrigeerd.</span><span class="sxs-lookup"><span data-stu-id="d2edc-126">If the **Canceled** check box is selected, then you cannot cancel the posted purchase invoice because it has already been canceled or corrected.</span></span>
3. <span data-ttu-id="d2edc-127">Kies op de pagina **Geboekte inkoopfactuur** **Annuleren**.</span><span class="sxs-lookup"><span data-stu-id="d2edc-127">On the **Posted Purchase Invoice** page, choose **Cancel**.</span></span>

    <span data-ttu-id="d2edc-128">Een inkoopcreditnota wordt automatisch gemaakt en geboekt om de oorspronkelijke geboekte inkoopfactuur nietig te verklaren.</span><span class="sxs-lookup"><span data-stu-id="d2edc-128">A purchase credit memo is automatically created and posted to void the initial posted purchase invoice.</span></span> <span data-ttu-id="d2edc-129">Het veld **Geannuleerd** op de eerste geboekte inkoopfactuur is gewijzigd in **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d2edc-129">The **Canceled** field on the initial posted purchase invoice is changed to **Yes**.</span></span>
4. <span data-ttu-id="d2edc-130">Kies **Corrigerende creditnota tonen** om de geboekte inkoopcreditnota weer te geven die de in eerste instantie geboekte inkoopfactuur nietig verklaart.</span><span class="sxs-lookup"><span data-stu-id="d2edc-130">Choose **Show Corrective Credit Memo** to view the posted purchase credit memo that voids the initial posted purchase invoice.</span></span>

## <a name="see-also"></a><span data-ttu-id="d2edc-131">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d2edc-131">See Also</span></span>
[<span data-ttu-id="d2edc-132">Inkoop</span><span class="sxs-lookup"><span data-stu-id="d2edc-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="d2edc-133">Inkopen vastleggen</span><span class="sxs-lookup"><span data-stu-id="d2edc-133">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="d2edc-134">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d2edc-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
