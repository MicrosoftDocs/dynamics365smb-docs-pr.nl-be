---
title: Ontvangst combineren | Microsoft Docs
description: Als u meer dan één inkoopontvangst tegelijk wilt factureren, kunt u de functie Ontvangsten combineren gebruiken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/02/2020
ms.author: edupont
ms.openlocfilehash: 70433ce496c79edcd053ae345b3b0559cf60b744
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782911"
---
# <a name="combine-receipts-on-a-single-invoice"></a><span data-ttu-id="94faf-103">Ontvangsten combineren op één factuur</span><span class="sxs-lookup"><span data-stu-id="94faf-103">Combine Receipts on a Single Invoice</span></span>

<span data-ttu-id="94faf-104">Als u meer dan één inkoopontvangst tegelijk wilt factureren, kunt u de functie **Ontvangsten combineren** gebruiken.</span><span class="sxs-lookup"><span data-stu-id="94faf-104">If you want to invoice more than one purchase receipt at a time, you can use the **Combine Receipts** function.</span></span>  

<span data-ttu-id="94faf-105">Een gecombineerde inkoopontvangst kan pas worden gemaakt wanneer meer inkoopontvangsten van dezelfde leverancier in dezelfde valuta zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="94faf-105">Before you can create a combined purchase receipt, more than one receipt from the same vendor in the same currency must be posted.</span></span> <span data-ttu-id="94faf-106">U moet dus twee of meer inkooporders hebben ingevuld en deze hebben geboekt als ontvangen, maar niet als gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="94faf-106">In other words, you must have filled in two or more purchase orders and posted them as received, but not invoiced.</span></span>  

<span data-ttu-id="94faf-107">Wanneer inkoopontvangsten zijn gecombineerd op een factuur en zijn geboekt, wordt een geboekte inkoopfactuur gemaakt voor de gefactureerde regels.</span><span class="sxs-lookup"><span data-stu-id="94faf-107">When purchase receipts are combined on an invoice and posted, then a posted purchase invoice is created for the invoiced lines.</span></span> <span data-ttu-id="94faf-108">Het veld **Gefactureerd aantal** op de oorspronkelijke inkooporder of het oorspronkelijke inkoopraamcontract wordt bijgewerkt op basis van het gefactureerde aantal.</span><span class="sxs-lookup"><span data-stu-id="94faf-108">The **Quantity Invoiced** field on the originating purchase order, or blanket purchase order, is updated based on the invoiced quantity.</span></span> <span data-ttu-id="94faf-109">Dit oorspronkelijke inkoopdocument wordt echter niet verwijderd, zelfs als dit volledig is ontvangen en gefactureerd en daarom moet u het inkoopdocument zelf verwijderen.</span><span class="sxs-lookup"><span data-stu-id="94faf-109">However, this original purchase document is not deleted, even if it has been fully received and invoiced, and you must therefore delete the purchase document.</span></span>  

> [!NOTE]
> <span data-ttu-id="94faf-110">De resulterende inkoopfactuur kan later niet worden gecorrigeerd of geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="94faf-110">The resulting purchase invoice cannot later be corrected or canceled.</span></span> <span data-ttu-id="94faf-111">Als u een inkoopfactuur wilt wijzigen die op deze manier is gemaakt, moet u inkoopcreditnota's gebruiken.</span><span class="sxs-lookup"><span data-stu-id="94faf-111">If you want to modify a purchase invoice that is created in this way, you must use purchase credit memos.</span></span> <span data-ttu-id="94faf-112">Zie voor meer informatie [Onbetaalde inkoopfacturen corrigeren of annuleren](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="94faf-112">For more information, see [Correct or Cancel Unpaid Purchase Invoices](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).</span></span>

## <a name="to-combine-receipts"></a><span data-ttu-id="94faf-113">Ontvangsten combineren</span><span class="sxs-lookup"><span data-stu-id="94faf-113">To combine receipts</span></span>

1. <span data-ttu-id="94faf-114">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopfacturen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="94faf-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="94faf-115">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="94faf-115">Choose the **New** action.</span></span> <span data-ttu-id="94faf-116">Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="94faf-116">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>  
3. <span data-ttu-id="94faf-117">Op het sneltabblad **Regels** selecteert u de actie **Ontvangstregels ophalen**.</span><span class="sxs-lookup"><span data-stu-id="94faf-117">On the **Lines** FastTab, choose the **Get Receipt Lines** action.</span></span>  
4. <span data-ttu-id="94faf-118">Selecteer meerdere ontvangstregels die u wilt opnemen in de factuur.</span><span class="sxs-lookup"><span data-stu-id="94faf-118">Select multiple receipt lines that you want to include in the invoice.</span></span>  

    <span data-ttu-id="94faf-119">Als een onjuiste ontvangstregel is geselecteerd of als u opnieuw wilt beginnen, kunt u de regels op de inkoopfactuur gewoon verwijderen en vervolgens de functie **Ontvangstregels ophalen** opnieuw gebruiken.</span><span class="sxs-lookup"><span data-stu-id="94faf-119">If an incorrect receipt line was selected or you want to start over, you can just delete the lines on the purchase invoice and then use the **Get Receipt Lines** function again.</span></span>  
5. <span data-ttu-id="94faf-120">Kies de actie **Boeken** om de factuur te boeken.</span><span class="sxs-lookup"><span data-stu-id="94faf-120">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting"></a><span data-ttu-id="94faf-121">Open inkooporders verwijderen na gecombineerde ontvangstboeking</span><span class="sxs-lookup"><span data-stu-id="94faf-121">To remove open purchase orders after combined receipt posting</span></span>

1. <span data-ttu-id="94faf-122">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gefactureerde inkooporders verwijderen** in en selecteer de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="94faf-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Purchase Orders**, and select the related link.</span></span>  
2. <span data-ttu-id="94faf-123">Vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="94faf-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="94faf-124">.</span><span class="sxs-lookup"><span data-stu-id="94faf-124">.</span></span>
3. <span data-ttu-id="94faf-125">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="94faf-125">Choose the **OK** button.</span></span>  

<span data-ttu-id="94faf-126">U kunt de afzonderlijke orders ook handmatig verwijderen.</span><span class="sxs-lookup"><span data-stu-id="94faf-126">Alternatively, delete the individual orders manually.</span></span>

<span data-ttu-id="94faf-127">Herhaal stap 1 t/m 3 voor alle andere betrokken documenten, zoals inkoopraamcontracten.</span><span class="sxs-lookup"><span data-stu-id="94faf-127">Repeat steps 1 through 3 for any other affected documents, such as blanket purchase orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="94faf-128">Zie ook</span><span class="sxs-lookup"><span data-stu-id="94faf-128">See Also</span></span>

[<span data-ttu-id="94faf-129">Inkoop</span><span class="sxs-lookup"><span data-stu-id="94faf-129">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="94faf-130">Niet-betaalde inkoopfacturen corrigeren of annuleren</span><span class="sxs-lookup"><span data-stu-id="94faf-130">Correct or Cancel Unpaid Purchase Invoices</span></span>](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
<span data-ttu-id="94faf-131">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="94faf-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
