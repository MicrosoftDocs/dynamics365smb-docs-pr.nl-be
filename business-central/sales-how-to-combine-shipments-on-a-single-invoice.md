---
title: 'Procedure: Verzendingen combineren op één factuur | Microsoft Docs'
description: Als u meerdere verzendingen tegelijkertijd wilt factureren, kunt u de functie Verzamelfacturering gebruiken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2936e819ba50adde6df021cc0dc2694367c29fc9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5778509"
---
# <a name="combine-shipments-on-a-single-invoice"></a><span data-ttu-id="c9fd7-103">Verzendingen combineren op één factuur</span><span class="sxs-lookup"><span data-stu-id="c9fd7-103">Combine Shipments on a Single Invoice</span></span>
<span data-ttu-id="c9fd7-104">Als u meerdere verzendingen tegelijkertijd wilt factureren, kunt u de functie Verzamelfacturering gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-104">If you want to invoice more than one shipment at a time, you can use the combined shipments feature.</span></span>  

<span data-ttu-id="c9fd7-105">Voordat u een verzamelfactuur kunt maken, moet u meerdere verkoopverzendingen voor dezelfde klant in dezelfde valuta boeken.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-105">Before you can create a combined shipment, more than one sales shipment for the same customer in the same currency must be posted.</span></span> <span data-ttu-id="c9fd7-106">U moet dus twee of meer verkooporders hebben gemaakt en deze als verzonden maar niet als gefactureerd boeken.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-106">In other words, you must have create two or more sales orders and post them as shipped, but not invoiced.</span></span> 

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="c9fd7-107">Verzendingen handmatig op één factuur combineren</span><span class="sxs-lookup"><span data-stu-id="c9fd7-107">To manually combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="c9fd7-108">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopfacturen** in en kies de gerelateerde koppeling</span><span class="sxs-lookup"><span data-stu-id="c9fd7-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c9fd7-109">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-109">Choose the **New** action.</span></span> <span data-ttu-id="c9fd7-110">Zie [Verkopen factureren](sales-how-invoice-sales.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-110">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>
3. <span data-ttu-id="c9fd7-111">Voer in het veld **Orderklantnr.**</span><span class="sxs-lookup"><span data-stu-id="c9fd7-111">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="c9fd7-112">de klant in die de factuur voor de verzonden artikelen zal ontvangen.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-112">field, enter the customer who will receive the invoice for the shipped items.</span></span>  
4. <span data-ttu-id="c9fd7-113">Selecteer op het sneltabblad **Regels** de actie **Verzendregels ophalen**.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-113">On the **Lines** FastTab, choose the **Get Shipment Lines** action.</span></span>  
5. <span data-ttu-id="c9fd7-114">Selecteer de verzendregels die u wilt opnemen in de factuur:</span><span class="sxs-lookup"><span data-stu-id="c9fd7-114">Select the shipment line that you want to include in the invoice:</span></span>  

    - <span data-ttu-id="c9fd7-115">Als u alle regels wilt invoegen, selecteert u alle regels en klikt u op **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-115">To insert all lines, select all lines and choose the **OK** button.</span></span>  
    - <span data-ttu-id="c9fd7-116">Als u specifieke regels wilt invoegen, selecteert u deze regels en klikt u op **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-116">To insert specific lines, select the lines and choose the **OK** button.</span></span> <span data-ttu-id="c9fd7-117">Gebruik de Ctrl-toets om meerdere niet-aaneengesloten regels te selecteren.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-117">You can use the Ctrl key to select multiple nonsequential lines.</span></span>  

    <span data-ttu-id="c9fd7-118">Als u de verkeerde verzendregel hebt geselecteerd of als u opnieuw wilt beginnen, kunt u de regels op de factuur verwijderen en de functie **Verzendregels ophalen** opnieuw uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-118">If an incorrect shipment line was selected or you want to start over, you can simply delete the lines on the invoice and re-run the **Get Shipment Lines** function.</span></span>  
7. <span data-ttu-id="c9fd7-119">Kies de actie **Boeken** om de factuur te boeken.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-119">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="c9fd7-120">Verzendingen automatisch op één factuur combineren</span><span class="sxs-lookup"><span data-stu-id="c9fd7-120">To automatically combine shipments on a single invoice</span></span>  
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="c9fd7-121">selecteert alleen verkooporders waar **Verzendingen combineren** is gekozen.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-121">will select only sales orders where **Combine Shipments** is chosen.</span></span> 

1. <span data-ttu-id="c9fd7-122">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verzendingen combineren** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Combine Shipments**, and then choose the related link.</span></span> <span data-ttu-id="c9fd7-123">De opvraagpagina voor de batchverwerking wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-123">The batch job request page opens.</span></span>  
2. <span data-ttu-id="c9fd7-124">Vul de vereiste velden in.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="c9fd7-125">Kies het selectievakje **Facturen boeken**.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-125">Choose the **Post Invoices** check box.</span></span>  
4. <span data-ttu-id="c9fd7-126">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-126">Choose the **OK** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c9fd7-127">U moet de facturen handmatig boeken als het selectievakje **Facturen boeken** niet was ingeschakeld bij de batchverwerking.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-127">You will need to manually post the invoices if the **Post Invoices** check box was not selected on the batch job.</span></span>  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a><span data-ttu-id="c9fd7-128">Openstaande verkooporders verwijderen na boeking van een verzamelfactuur</span><span class="sxs-lookup"><span data-stu-id="c9fd7-128">To remove open sales orders after combined shipment posting</span></span> 
<span data-ttu-id="c9fd7-129">Als verzendingen worden gecombineerd op een factuur en worden geboekt, wordt er een geboekte verkoopfactuur gemaakt voor de gefactureerde regel.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-129">When shipments are combined on an invoice and posted, a posted sales invoice is created for the invoiced lines.</span></span> <span data-ttu-id="c9fd7-130">Het veld **Verzonden aantal** op het oorspronkelijke verkoopraamcontract of de oorspronkelijke verkooporder wordt bijgewerkt op basis van het gefactureerde aantal.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-130">The **Quantity Invoiced** field on the originating blanket sales order or sales order is updated based on the invoiced quantity.</span></span>  

<span data-ttu-id="c9fd7-131">Als u op deze manier verzendingen factureert, blijven de orders van waaruit de verzending zijn geboekt bestaan, ook als ze volledig zijn verzonden en gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-131">When you invoice shipments in this way, the orders from which the shipments were posted still exist, even if they have been fully shipped and invoiced.</span></span>   

1. <span data-ttu-id="c9fd7-132">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gefactureerde verkooporders verwijderen** in en selecteer de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Sales Orders**, and then select the link.</span></span>  
2. <span data-ttu-id="c9fd7-133">Geef in het filterveld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="c9fd7-133">Specify in the **No.**</span></span> <span data-ttu-id="c9fd7-134">op welke verkooporders moeten worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-134">filter field which sales orders to delete.</span></span>  
3. <span data-ttu-id="c9fd7-135">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-135">Choose the **OK** button.</span></span>  

<span data-ttu-id="c9fd7-136">U kunt afzonderlijke verkooporders ook handmatig verwijderen.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-136">Alternatively, delete individual sales orders manually.</span></span>  

<span data-ttu-id="c9fd7-137">Herhaal stap 1 t/m 3 voor alle andere betrokken documenten, zoals verkoopraamcontracten.</span><span class="sxs-lookup"><span data-stu-id="c9fd7-137">Repeat steps 1 through 3 for any other affected documents, such as blanket sales orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="c9fd7-138">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c9fd7-138">See Also</span></span>  
[<span data-ttu-id="c9fd7-139">Verkoop</span><span class="sxs-lookup"><span data-stu-id="c9fd7-139">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="c9fd7-140">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c9fd7-140">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]