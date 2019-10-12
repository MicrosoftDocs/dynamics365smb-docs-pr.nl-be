---
title: 'Procedure: Verzendingen combineren op één factuur | Microsoft Docs'
description: Als u meerdere verzendingen tegelijkertijd wilt factureren, kunt u de functie Verzamelfacturering gebruiken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6a9f4d6ee49b8958b3dcc33697db5ce0d77ae2c8
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312040"
---
# <a name="combine-shipments-on-a-single-invoice"></a><span data-ttu-id="c01b5-103">Verzendingen combineren op één factuur</span><span class="sxs-lookup"><span data-stu-id="c01b5-103">Combine Shipments on a Single Invoice</span></span>
<span data-ttu-id="c01b5-104">Als u meerdere verzendingen tegelijkertijd wilt factureren, kunt u de functie Verzamelfacturering gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c01b5-104">If you want to invoice more than one shipment at a time, you can use the combined shipments feature.</span></span>  

 <span data-ttu-id="c01b5-105">Voordat u een verzamelfactuur kunt maken, moet u meerdere verkoopverzendingen voor dezelfde klant in dezelfde valuta boeken.</span><span class="sxs-lookup"><span data-stu-id="c01b5-105">Before you can create a combined shipment, more than one sales shipment for the same customer in the same currency must be posted.</span></span> <span data-ttu-id="c01b5-106">U moet dus twee of meer verkooporders invullen en deze als verzonden maar niet als gefactureerd boeken.</span><span class="sxs-lookup"><span data-stu-id="c01b5-106">In other words, you must have filled in two or more sales orders and posted them as shipped, but not invoiced.</span></span> <span data-ttu-id="c01b5-107">Om verzendingen te combineren moet het selectievakje **Verzendingen combineren** zijn ingeschakeld op het sneltabblad **Verzending** van de **klantenkaart**.</span><span class="sxs-lookup"><span data-stu-id="c01b5-107">To combine shipments, the **Combine Shipments** check box must be selected on the **Shipping** FastTab of the **Customer** card.</span></span>  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="c01b5-108">Verzendingen handmatig op één factuur combineren</span><span class="sxs-lookup"><span data-stu-id="c01b5-108">To manually combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="c01b5-109">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="c01b5-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c01b5-110">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c01b5-110">Choose the **New** action.</span></span> <span data-ttu-id="c01b5-111">Zie [Verkopen factureren](sales-how-invoice-sales.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="c01b5-111">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>
3. <span data-ttu-id="c01b5-112">Voer in het veld **Orderklantnr.**</span><span class="sxs-lookup"><span data-stu-id="c01b5-112">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="c01b5-113">de klant in die de factuur voor de verzonden artikelen zal ontvangen.</span><span class="sxs-lookup"><span data-stu-id="c01b5-113">field, enter the customer who will receive the invoice for the shipped items.</span></span>  
4. <span data-ttu-id="c01b5-114">Selecteer op het sneltabblad **Regels** de actie **Verzendregels ophalen**.</span><span class="sxs-lookup"><span data-stu-id="c01b5-114">On the **Lines** FastTab, choose the **Get Shipment Lines** action.</span></span>  
5. <span data-ttu-id="c01b5-115">Selecteer de verzendregels die u wilt opnemen in de factuur:</span><span class="sxs-lookup"><span data-stu-id="c01b5-115">Select the shipment line that you want to include in the invoice:</span></span>  

    - <span data-ttu-id="c01b5-116">Als u alle regels wilt invoegen, selecteert u alle regels en klikt u op **OK**.</span><span class="sxs-lookup"><span data-stu-id="c01b5-116">To insert all lines, select all lines and choose the **OK** button.</span></span>  
    - <span data-ttu-id="c01b5-117">Als u specifieke regels wilt invoegen, selecteert u deze regels en klikt u op **OK**.</span><span class="sxs-lookup"><span data-stu-id="c01b5-117">To insert specific lines, select the lines and choose the **OK** button.</span></span> <span data-ttu-id="c01b5-118">Gebruik de Ctrl-toets om meerdere niet-aaneengesloten regels te selecteren.</span><span class="sxs-lookup"><span data-stu-id="c01b5-118">You can use the Ctrl key to select multiple nonsequential lines.</span></span>  

    <span data-ttu-id="c01b5-119">Als u de verkeerde verzendregel hebt geselecteerd of als u opnieuw wilt beginnen, kunt u de regels op de factuur verwijderen en de functie **Verzendregels ophalen** opnieuw uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="c01b5-119">If an incorrect shipment line was selected or you want to start over, you can simply delete the lines on the invoice and re-run the **Get Shipment Lines** function.</span></span>  
7. <span data-ttu-id="c01b5-120">Kies de actie **Boeken** om de factuur te boeken.</span><span class="sxs-lookup"><span data-stu-id="c01b5-120">To post the invoice, choose the **Post** action.</span></span>  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a><span data-ttu-id="c01b5-121">Verzendingen automatisch op één factuur combineren</span><span class="sxs-lookup"><span data-stu-id="c01b5-121">To automatically combine shipments on a single invoice</span></span>  
1. <span data-ttu-id="c01b5-122">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verzendingen combineren** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="c01b5-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Combine Shipments**, and then choose the related link.</span></span> <span data-ttu-id="c01b5-123">De opvraagpagina voor de batchverwerking wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="c01b5-123">The batch job request page opens.</span></span>  
2. <span data-ttu-id="c01b5-124">Vul de benodigde velden in.</span><span class="sxs-lookup"><span data-stu-id="c01b5-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="c01b5-125">Schakel het selectievakje **Facturen boeken** in.</span><span class="sxs-lookup"><span data-stu-id="c01b5-125">Select the **Post Invoices** check box.</span></span>  
4.  <span data-ttu-id="c01b5-126">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="c01b5-126">Choose the **OK** button.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c01b5-127">U moet de facturen handmatig boeken als het selectievakje **Facturen boeken** niet was ingeschakeld bij de batchverwerking.</span><span class="sxs-lookup"><span data-stu-id="c01b5-127">You will need to manually post the invoices if the **Post Invoices** check box was not selected on the batch job.</span></span>  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a><span data-ttu-id="c01b5-128">Openstaande verkooporders verwijderen na boeking van een verzamelfactuur</span><span class="sxs-lookup"><span data-stu-id="c01b5-128">To remove open sales orders after combined shipment posting</span></span> 
<span data-ttu-id="c01b5-129">Als verzendingen worden gecombineerd op een factuur en worden geboekt, wordt er een geboekte verkoopfactuur gemaakt voor de gefactureerde regel.</span><span class="sxs-lookup"><span data-stu-id="c01b5-129">When shipments are combined on an invoice and posted, a posted sales invoice is created for the invoiced lines.</span></span> <span data-ttu-id="c01b5-130">Het veld **Verzonden aantal** op het oorspronkelijke verkoopraamcontract of de oorspronkelijke verkooporder wordt bijgewerkt op basis van het gefactureerde aantal.</span><span class="sxs-lookup"><span data-stu-id="c01b5-130">The **Quantity Invoiced** field on the originating blanket sales order or sales order is updated based on the invoiced quantity.</span></span>  

<span data-ttu-id="c01b5-131">Als u op deze manier verzendingen factureert, blijven de orders van waaruit de verzending zijn geboekt bestaan, ook als ze volledig zijn verzonden en gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="c01b5-131">When you invoice shipments in this way, the orders from which the shipments were posted still exist, even if they have been fully shipped and invoiced.</span></span>   

1. <span data-ttu-id="c01b5-132">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gefactureerde verkooporders verwijderen** in en selecteer vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="c01b5-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Invoiced Sales Orders**, and then select the link.</span></span>  
2. <span data-ttu-id="c01b5-133">Geef in het filterveld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="c01b5-133">Specify in the **No.**</span></span> <span data-ttu-id="c01b5-134">op welke verkooporders moeten worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="c01b5-134">filter field which sales orders to delete.</span></span>  
3. <span data-ttu-id="c01b5-135">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="c01b5-135">Choose the **OK** button.</span></span>  

<span data-ttu-id="c01b5-136">U kunt afzonderlijke verkooporders ook handmatig verwijderen.</span><span class="sxs-lookup"><span data-stu-id="c01b5-136">Alternatively, delete individual sales orders manually.</span></span>  

<span data-ttu-id="c01b5-137">Herhaal stap 1 t/m 3 voor alle andere betrokken documenten, zoals verkoopraamcontracten.</span><span class="sxs-lookup"><span data-stu-id="c01b5-137">Repeat steps 1 through 3 for any other affected documents, such as blanket sales orders.</span></span>

## <a name="see-also"></a><span data-ttu-id="c01b5-138">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c01b5-138">See Also</span></span>  
[<span data-ttu-id="c01b5-139">Verkoop</span><span class="sxs-lookup"><span data-stu-id="c01b5-139">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="c01b5-140">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c01b5-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
