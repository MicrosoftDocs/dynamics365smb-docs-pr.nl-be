---
title: Een verkooporder koppelen aan een inkooporder voor een directe verzending | Microsoft Docs
description: Hierin wordt beschreven hoe u een verkooporder kunt maken die is gekoppeld aan een inkooporder om verzending direct van de leverancier naar de klant mogelijk te maken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c6b84d3622b4261c1f88880ba1257bf00f83e346
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748455"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="0b059-103">Doorverzendingen uitvoeren</span><span class="sxs-lookup"><span data-stu-id="0b059-103">Make Drop Shipments</span></span>

<span data-ttu-id="0b059-104">Een doorverzending is de directe verzending van artikelen van een van uw leveranciers naar een van uw klanten.</span><span class="sxs-lookup"><span data-stu-id="0b059-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="0b059-105">Wanneer een verkooporder gemarkeerd is voor doorverzending en u een inkooporder maakt met de klant in het veld **Verzenden naar**, **Klantadres**, kunt u de twee documenten koppelen en zo de leverancier instrueren om rechtstreeks naar de klant te verzenden.</span><span class="sxs-lookup"><span data-stu-id="0b059-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Ship-to** field, **Customer Address**, you can link the two documents to instruct the vendor to ship directly to the customer.</span></span>
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="0b059-106">Een verkooporder voor doorverzending maken</span><span class="sxs-lookup"><span data-stu-id="0b059-106">To create a sales order for drop shipment</span></span>

<span data-ttu-id="0b059-107">Ter voorbereiding op een doorverzending maakt u een verkooporder voor een artikel en geeft u op de verkoopregel aan dat voor de verkoop doorverzending vereist is.</span><span class="sxs-lookup"><span data-stu-id="0b059-107">To prepare a drop shipment, you create a sales order for an item and indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="0b059-108">Maak een verkooporder voor een artikel.</span><span class="sxs-lookup"><span data-stu-id="0b059-108">Create a sales order for an item.</span></span> <span data-ttu-id="0b059-109">Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="0b059-109">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="0b059-110">Op de verkooporderregel voor de doorverzending schakelt u het selectievakje **Doorverzending** in.</span><span class="sxs-lookup"><span data-stu-id="0b059-110">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="0b059-111">Gebruik de functie **Kolommen kiezen** als het veld niet zichtbaar is.</span><span class="sxs-lookup"><span data-stu-id="0b059-111">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="0b059-112">Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="0b059-112">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="0b059-113">De inkooporder voor doorverzendingen maken</span><span class="sxs-lookup"><span data-stu-id="0b059-113">To create the purchase order for drop shipment</span></span>

<span data-ttu-id="0b059-114">Om een doorverzending voor te bereiden geeft u op de inkooporder aan dat deze naar uw klant moet worden verzonden, niet naar uzelf.</span><span class="sxs-lookup"><span data-stu-id="0b059-114">To prepare a drop shipment, you indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="0b059-115">Inkooporder maken.</span><span class="sxs-lookup"><span data-stu-id="0b059-115">Create a purchase order.</span></span> <span data-ttu-id="0b059-116">Vul geen velden op de regels in.</span><span class="sxs-lookup"><span data-stu-id="0b059-116">Do not fill any fields on the lines.</span></span> <span data-ttu-id="0b059-117">Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="0b059-117">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="0b059-118">Selecteer in het veld **Verzenden naar**, **Klantadres**.</span><span class="sxs-lookup"><span data-stu-id="0b059-118">In the **Ship-to** field, select **Customer Address**.</span></span>
3. <span data-ttu-id="0b059-119">Selecteer in het veld **Klant** de klant aan wie u verkoopt.</span><span class="sxs-lookup"><span data-stu-id="0b059-119">In the **Customer** field, select the customer that you are selling to.</span></span>
4. <span data-ttu-id="0b059-120">Kies de actie **Doorverzendingen** en kies vervolgens de actie **Verkooporder ophalen**.</span><span class="sxs-lookup"><span data-stu-id="0b059-120">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
5. <span data-ttu-id="0b059-121">Selecteer op de pagina **Verkoopoverzicht** de verkooporder die u hebt voorbereid in [Een verkooporder voor doorverzending maken](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="0b059-121">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
6. <span data-ttu-id="0b059-122">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b059-122">Choose the **OK** button.</span></span>

<span data-ttu-id="0b059-123">De regelgegevens van de verkooporder worden ingevoegd op de inkooporderregel(s).</span><span class="sxs-lookup"><span data-stu-id="0b059-123">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="0b059-124">U kunt de leverancier nu opdragen om de artikelen naar de klant te verzenden, bijvoorbeeld door de inkooporder als een PDF via e-mail te verzenden.</span><span class="sxs-lookup"><span data-stu-id="0b059-124">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a><span data-ttu-id="0b059-125">Meerdere inkooporders voor doorverzendingen maken</span><span class="sxs-lookup"><span data-stu-id="0b059-125">To create multiple purchase orders for drop shipments</span></span>

<span data-ttu-id="0b059-126">U kunt ook het inkoopvoorstel gebruiken om de inkooporder voor de leverancier te maken.</span><span class="sxs-lookup"><span data-stu-id="0b059-126">You can also use the requisition worksheet to create the purchase order for the vendor.</span></span> <span data-ttu-id="0b059-127">Het voordeel van het gebruik van het inkoopvoorstel is dat het inkooporders kan maken voor alle openstaande doorverzendingen, zodat u ze niet allemaal afzonderlijk hoeft te maken.</span><span class="sxs-lookup"><span data-stu-id="0b059-127">The advantage of using the requisition worksheet is that it can create purchase orders for all outstanding drop shipments, so you don't have to create each one individually.</span></span>

1. <span data-ttu-id="0b059-128">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopvoorstellen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="0b059-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Requistion Worksheets**, and then choose the related link.</span></span>
2. <span data-ttu-id="0b059-129">Kies de actie **Doorverzendingen** en kies vervolgens de actie **Verkooporder ophalen**.</span><span class="sxs-lookup"><span data-stu-id="0b059-129">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
3. <span data-ttu-id="0b059-130">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="0b059-130">Choose the **OK** button.</span></span>
4. <span data-ttu-id="0b059-131">Bekijk de inkooporderregels en selecteer in het veld **Leveranciersnr.** de leverancier die de benodigde goederen levert.</span><span class="sxs-lookup"><span data-stu-id="0b059-131">Review the purchase order lines, and in the **Vendor No.** field, select vendor that supplies required goods.</span></span> 
5. <span data-ttu-id="0b059-132">Kies de actie **Planningsboodschap uitvoeren** om beoordeelde regels om te zetten in een inkooporder.</span><span class="sxs-lookup"><span data-stu-id="0b059-132">Choose the **Carry Out Action Message** action to convert reviewed lines to a purchase order.</span></span>

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="0b059-133">De gekoppelde inkooporder weergeven op basis van de verkooporder</span><span class="sxs-lookup"><span data-stu-id="0b059-133">To view the linked purchase order from the sales order</span></span>

* <span data-ttu-id="0b059-134">Selecteer de verkooporderregel van de doorverzending, kies de actie **Order**, kies de actie **Doorverzending** en kies vervolgens de actie **Inkooporder**.</span><span class="sxs-lookup"><span data-stu-id="0b059-134">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="0b059-135">Een doorverzending boeken</span><span class="sxs-lookup"><span data-stu-id="0b059-135">To post a drop shipment</span></span>

<span data-ttu-id="0b059-136">Nadat de leverancier de artikelen heeft verzonden, kunt u de verkooporder boeken als verzonden.</span><span class="sxs-lookup"><span data-stu-id="0b059-136">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="0b059-137">U kunt de inkooporder ook boeken, maar alleen met de optie **Ontvangen**, totdat de verkooporder is gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="0b059-137">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="0b059-138">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="0b059-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="0b059-139">Open de verkooporder die u hebt gemaakt in [Een verkooporder voor een doorverzending maken](#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="0b059-139">Open the sales order that you created in [To create a sales order for drop shipment](#to-create-a-sales-order-for-drop-shipment).</span></span>
3. <span data-ttu-id="0b059-140">Geef in het veld **Te verzenden aantal** op hoeveel van de orderhoeveelheid moet worden verzonden, de volledige of gedeeltelijke orderhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="0b059-140">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="0b059-141">Kies de actie **Boeken** of **Boeken en verzenden**.</span><span class="sxs-lookup"><span data-stu-id="0b059-141">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="0b059-142">Kies vervolgens **de optie Verzenden** om later te factureren of de optie **Verzenden en factureren** om meteen te factureren.</span><span class="sxs-lookup"><span data-stu-id="0b059-142">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="0b059-143">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0b059-143">See Also</span></span>

[<span data-ttu-id="0b059-144">Speciale orders maken:</span><span class="sxs-lookup"><span data-stu-id="0b059-144">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="0b059-145">Artikelen kopen voor een verkoop</span><span class="sxs-lookup"><span data-stu-id="0b059-145">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="0b059-146">Producten verkopen</span><span class="sxs-lookup"><span data-stu-id="0b059-146">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="0b059-147">Inkopen vastleggen</span><span class="sxs-lookup"><span data-stu-id="0b059-147">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="0b059-148">Verkoop</span><span class="sxs-lookup"><span data-stu-id="0b059-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="0b059-149">Voorraad</span><span class="sxs-lookup"><span data-stu-id="0b059-149">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="0b059-150">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0b059-150">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
