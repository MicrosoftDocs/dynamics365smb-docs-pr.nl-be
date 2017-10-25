---
title: "Procedure: Verzendingen combineren op één factuur | Microsoft Docs"
description: Als u meerdere verzendingen tegelijkertijd wilt factureren, kunt u de functie Verzamelfacturering gebruiken.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: e6be50119da5c617ce6dbf603903266f9ced821e
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="a6de8-103">Procedure: verzendingen combineren op één factuur</span><span class="sxs-lookup"><span data-stu-id="a6de8-103">How to: Combine Shipments on a Single Invoice</span></span>
<span data-ttu-id="a6de8-104">Als u meerdere verzendingen tegelijkertijd wilt factureren, kunt u de functie Verzamelfacturering gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a6de8-104">If you want to invoice more than one shipment at a time, you can use the combined shipments feature.</span></span>  

 <span data-ttu-id="a6de8-105">Voordat u een verzamelfactuur kunt maken, moet u meerdere verkoopverzendingen voor dezelfde klant in dezelfde valuta boeken.</span><span class="sxs-lookup"><span data-stu-id="a6de8-105">Before you can create a combined shipment, more than one sales shipment for the same customer in the same currency must be posted.</span></span> <span data-ttu-id="a6de8-106">U moet dus twee of meer verkooporders invullen en deze als verzonden maar niet als gefactureerd boeken.</span><span class="sxs-lookup"><span data-stu-id="a6de8-106">In other words, you must have filled in two or more sales orders and posted them as shipped, but not invoiced.</span></span> <span data-ttu-id="a6de8-107">Om verzendingen te combineren moet het selectievakje **Verzendingen combineren** zijn ingeschakeld op het sneltabblad **Verzending** van de **klantenkaart**.</span><span class="sxs-lookup"><span data-stu-id="a6de8-107">To combine shipments, the **Combine Shipments** check box must be selected on the **Shipping** FastTab of the **Customer** card.</span></span>  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="a6de8-108">Verzendingen handmatig op één factuur combineren</span><span class="sxs-lookup"><span data-stu-id="a6de8-108">To manually combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="a6de8-109">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verkoopfacturen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="a6de8-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="a6de8-110">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="a6de8-110">Choose the **New** action.</span></span> <span data-ttu-id="a6de8-111">Zie [Procedure: Verkopen factureren](sales-how-invoice-sales.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="a6de8-111">For more information, see [How to: Invoice Sales](sales-how-invoice-sales.md).</span></span>
3. <span data-ttu-id="a6de8-112">Selecteer in het veld **Orderklantnr.**</span><span class="sxs-lookup"><span data-stu-id="a6de8-112">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="a6de8-113">de klant in die de factuur voor de verzonden artikelen zal ontvangen.</span><span class="sxs-lookup"><span data-stu-id="a6de8-113">field, enter the customer who will receive the invoice for the shipped items.</span></span>  
4. <span data-ttu-id="a6de8-114">Selecteer op het sneltabblad **Regels** de actie **Verzendregels ophalen**.</span><span class="sxs-lookup"><span data-stu-id="a6de8-114">On the **Lines** FastTab, choose the **Get Shipment Lines** action.</span></span>  
5. <span data-ttu-id="a6de8-115">Selecteer de verzendregels die u wilt opnemen in de factuur:</span><span class="sxs-lookup"><span data-stu-id="a6de8-115">Select the shipment line that you want to include in the invoice:</span></span>  

    - <span data-ttu-id="a6de8-116">Als u alle regels wilt invoegen, selecteert u alle regels en klikt u op **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6de8-116">To insert all lines, select all lines and choose the **OK** button.</span></span>  
    - <span data-ttu-id="a6de8-117">Als u specifieke regels wilt invoegen, selecteert u deze regels en klikt u op **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6de8-117">To insert specific lines, select the lines and choose the **OK** button.</span></span> <span data-ttu-id="a6de8-118">Gebruik de Ctrl-toets om meerdere niet-aaneengesloten regels te selecteren.</span><span class="sxs-lookup"><span data-stu-id="a6de8-118">You can use the Ctrl key to select multiple nonsequential lines.</span></span>  

    <span data-ttu-id="a6de8-119">Als u de verkeerde verzendregel hebt geselecteerd of als u opnieuw wilt beginnen, kunt u de regels op de factuur verwijderen en de functie **Verzendregels ophalen** opnieuw uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="a6de8-119">If an incorrect shipment line was selected or you want to start over, you can simply delete the lines on the invoice and re-run the **Get Shipment Lines** function.</span></span>  
7. <span data-ttu-id="a6de8-120">Kies de actie **Boeken** om de factuur te boeken.</span><span class="sxs-lookup"><span data-stu-id="a6de8-120">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="a6de8-121">Verzendingen automatisch op één factuur combineren</span><span class="sxs-lookup"><span data-stu-id="a6de8-121">To automatically combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="a6de8-122">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verzamelfacturering** in en klik vervolgens o de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="a6de8-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Combine Shipments**, and then choose the related link.</span></span> <span data-ttu-id="a6de8-123">Het opvraagvenster voor de batchverwerking wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="a6de8-123">The batch job request window opens.</span></span>  
2. <span data-ttu-id="a6de8-124">Vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="a6de8-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="a6de8-125">Schakel het selectievakje **Facturen boeken** in.</span><span class="sxs-lookup"><span data-stu-id="a6de8-125">Select the **Post Invoices** check box.</span></span>  
4.  <span data-ttu-id="a6de8-126">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6de8-126">Choose the **OK** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a6de8-127">U moet de facturen handmatig boeken als het selectievakje **Facturen boeken** niet was ingeschakeld bij de batchverwerking.</span><span class="sxs-lookup"><span data-stu-id="a6de8-127">You will need to manually post the invoices if the **Post Invoices** check box was not selected on the batch job.</span></span>  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a><span data-ttu-id="a6de8-128">Openstaande verkooporders verwijderen na boeking van een verzamelfactuur</span><span class="sxs-lookup"><span data-stu-id="a6de8-128">To remove open sales orders after combined shipment posting</span></span> 
<span data-ttu-id="a6de8-129">Als verzendingen worden gecombineerd op een factuur en worden geboekt, wordt er een geboekte verkoopfactuur gemaakt voor de gefactureerde regel.</span><span class="sxs-lookup"><span data-stu-id="a6de8-129">When shipments are combined on an invoice and posted, a posted sales invoice is created for the invoiced lines.</span></span> <span data-ttu-id="a6de8-130">Het veld **Verzonden aantal** op het oorspronkelijke verkoopraamcontract of de oorspronkelijke verkooporder wordt bijgewerkt op basis van het gefactureerde aantal.</span><span class="sxs-lookup"><span data-stu-id="a6de8-130">The **Quantity Invoiced** field on the originating blanket sales order or sales order is updated based on the invoiced quantity.</span></span>  

<span data-ttu-id="a6de8-131">Als u op deze manier verzendingen factureert, blijven de orders van waaruit de verzending zijn geboekt bestaan, ook als ze volledig zijn verzonden en gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="a6de8-131">When you invoice shipments in this way, the orders from which the shipments were posted still exist, even if they have been fully shipped and invoiced.</span></span>   

1. <span data-ttu-id="a6de8-132">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Gefact. verk.-orders verwijderen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="a6de8-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Invoiced Sales Orders**, and then select the link.</span></span>  
2. <span data-ttu-id="a6de8-133">Geef in het filterveld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="a6de8-133">Specify in the **No.**</span></span> <span data-ttu-id="a6de8-134">op welke verkooporders moeten worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="a6de8-134">filter field which sales orders to delete.</span></span>  
3. <span data-ttu-id="a6de8-135">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="a6de8-135">Choose the **OK** button.</span></span>  

<span data-ttu-id="a6de8-136">U kunt afzonderlijke verkooporders ook handmatig verwijderen.</span><span class="sxs-lookup"><span data-stu-id="a6de8-136">Alternatively, delete individual sales orders manually.</span></span>  

<span data-ttu-id="a6de8-137">Herhaal stap 1 t/m 3 voor alle andere betrokken documenten, zoals verkoopraamcontracten.</span><span class="sxs-lookup"><span data-stu-id="a6de8-137">Repeat steps 1 through 3 for any other affected documents, such as blanket sales orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6de8-138">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a6de8-138">See Also</span></span>  
[<span data-ttu-id="a6de8-139">Verkoop</span><span class="sxs-lookup"><span data-stu-id="a6de8-139">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="a6de8-140">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a6de8-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

