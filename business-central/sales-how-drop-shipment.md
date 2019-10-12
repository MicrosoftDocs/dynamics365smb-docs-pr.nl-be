---
title: Een verkooporder koppelen aan een inkooporder voor een directe verzending | Microsoft Docs
description: Hierin wordt beschreven hoe u een verkooporder kunt maken die is gekoppeld aan een inkooporder om verzending direct van de leverancier naar de klant mogelijk te maken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 01799b1881fbcdc6285e84f86f9db88a8c4196a7
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312232"
---
# <a name="make-drop-shipments"></a><span data-ttu-id="f16f1-103">Doorverzendingen uitvoeren</span><span class="sxs-lookup"><span data-stu-id="f16f1-103">Make Drop Shipments</span></span>
<span data-ttu-id="f16f1-104">Een doorverzending is de directe verzending van artikelen van een van uw leveranciers naar een van uw klanten.</span><span class="sxs-lookup"><span data-stu-id="f16f1-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="f16f1-105">Wanneer een verkooporder gemarkeerd is voor doorverzending en u een inkooporder maakt met de klant in het veld **Verzenden naar**, **Klantadres**, kunt u de twee documenten koppelen en zo de leverancier instrueren om rechtstreeks naar de klant te verzenden.</span><span class="sxs-lookup"><span data-stu-id="f16f1-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Ship-to** field, **Customer Address**, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="f16f1-106">Een verkooporder voor doorverzending maken</span><span class="sxs-lookup"><span data-stu-id="f16f1-106">To create a sales order for drop shipment</span></span>
<span data-ttu-id="f16f1-107">Ter voorbereiding op een doorverzending maakt u een verkooporder voor een artikel zoals u dat normaal doet, maar u moet wel op de verkoopregel aangeven dat voor de verkoop doorverzending vereist is.</span><span class="sxs-lookup"><span data-stu-id="f16f1-107">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="f16f1-108">Maak een verkooporder voor een artikel.</span><span class="sxs-lookup"><span data-stu-id="f16f1-108">Create a sales order for an item.</span></span> <span data-ttu-id="f16f1-109">Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16f1-109">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="f16f1-110">Op de verkooporderregel voor de doorverzending schakelt u het selectievakje **Doorverzending** in.</span><span class="sxs-lookup"><span data-stu-id="f16f1-110">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="f16f1-111">Gebruik de functie **Kolommen kiezen** als het veld niet zichtbaar is.</span><span class="sxs-lookup"><span data-stu-id="f16f1-111">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="f16f1-112">Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f16f1-112">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="f16f1-113">De inkooporder voor doorverzendingen maken</span><span class="sxs-lookup"><span data-stu-id="f16f1-113">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="f16f1-114">Ter voorbereiding op een doorverzending van het artikel dat u wilt verkopen, maakt u een inkooporder zoals u dat normaal doet, maar u moet op de inkooporder wel aangeven dat het artikel naar de klant moet worden verzonden en niet naar uzelf.</span><span class="sxs-lookup"><span data-stu-id="f16f1-114">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="f16f1-115">Inkooporder maken.</span><span class="sxs-lookup"><span data-stu-id="f16f1-115">Create a purchase order.</span></span> <span data-ttu-id="f16f1-116">Vul geen velden op de regels in.</span><span class="sxs-lookup"><span data-stu-id="f16f1-116">Do not fill any fields on the lines.</span></span> <span data-ttu-id="f16f1-117">Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="f16f1-117">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="f16f1-118">Selecteer in het veld **Verzenden naar**, **Klantadres**.</span><span class="sxs-lookup"><span data-stu-id="f16f1-118">In the **Ship-to** field, select **Customer Address**.</span></span>
3. <span data-ttu-id="f16f1-119">Selecteer in het veld **Klant** de klant aan wie u verkoopt.</span><span class="sxs-lookup"><span data-stu-id="f16f1-119">In the **Customer** field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="f16f1-120">Kies de actie **Doorverzendingen** en kies vervolgens de actie **Verkooporder ophalen**.</span><span class="sxs-lookup"><span data-stu-id="f16f1-120">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="f16f1-121">Selecteer op de pagina **Verkoopoverzicht** de verkooporder die u hebt voorbereid in [Een verkooporder voor doorverzending maken](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span><span class="sxs-lookup"><span data-stu-id="f16f1-121">On the **Sales List** page, select the sales order that you prepared in [To create a sales order for drop shipment](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).</span></span>
5. <span data-ttu-id="f16f1-122">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="f16f1-122">Choose the **OK** button.</span></span>

<span data-ttu-id="f16f1-123">De regelgegevens van de verkooporder worden ingevoegd op de inkooporderregel(s).</span><span class="sxs-lookup"><span data-stu-id="f16f1-123">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="f16f1-124">U kunt de leverancier nu opdragen om de artikelen naar de klant te verzenden, bijvoorbeeld door de inkooporder als een PDF via e-mail te verzenden.</span><span class="sxs-lookup"><span data-stu-id="f16f1-124">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="f16f1-125">De gekoppelde inkooporder weergeven op basis van de verkooporder</span><span class="sxs-lookup"><span data-stu-id="f16f1-125">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="f16f1-126">Selecteer de verkooporderregel van de doorverzending, kies de actie **Order**, kies de actie **Doorverzending** en kies vervolgens de actie **Inkooporder**.</span><span class="sxs-lookup"><span data-stu-id="f16f1-126">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="f16f1-127">Een doorverzending boeken</span><span class="sxs-lookup"><span data-stu-id="f16f1-127">To post a drop shipment</span></span>
<span data-ttu-id="f16f1-128">Nadat de leverancier de artikelen heeft verzonden, kunt u de verkooporder boeken als verzonden.</span><span class="sxs-lookup"><span data-stu-id="f16f1-128">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="f16f1-129">U kunt de inkooporder ook boeken, maar alleen met de optie **Ontvangen**, totdat de verkooporder is gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="f16f1-129">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="f16f1-130">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="f16f1-130">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="f16f1-131">Open de verkooporder die u hebt gemaakt in [Een verkooporder voor een doorverzending maken]().</span><span class="sxs-lookup"><span data-stu-id="f16f1-131">Open the sales order that you created in [To create a sales order for drop shipment]().</span></span>
3. <span data-ttu-id="f16f1-132">Geef in het veld **Te verzenden aantal** op hoeveel van de orderhoeveelheid moet worden verzonden, de volledige of gedeeltelijke orderhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="f16f1-132">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="f16f1-133">Kies de actie **Boeken** of **Boeken en verzenden**.</span><span class="sxs-lookup"><span data-stu-id="f16f1-133">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="f16f1-134">Kies vervolgens **de optie Verzenden** om later te factureren of de optie **Verzenden en factureren** om meteen te factureren.</span><span class="sxs-lookup"><span data-stu-id="f16f1-134">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="f16f1-135">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f16f1-135">See Also</span></span>
[<span data-ttu-id="f16f1-136">Speciale orders maken:</span><span class="sxs-lookup"><span data-stu-id="f16f1-136">Create Special Orders</span></span>](sales-how-to-create-special-orders.md)  
[<span data-ttu-id="f16f1-137">Artikelen kopen voor een verkoop</span><span class="sxs-lookup"><span data-stu-id="f16f1-137">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="f16f1-138">Producten verkopen</span><span class="sxs-lookup"><span data-stu-id="f16f1-138">Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="f16f1-139">Inkopen vastleggen</span><span class="sxs-lookup"><span data-stu-id="f16f1-139">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="f16f1-140">Verkoop</span><span class="sxs-lookup"><span data-stu-id="f16f1-140">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="f16f1-141">Voorraad</span><span class="sxs-lookup"><span data-stu-id="f16f1-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="f16f1-142">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f16f1-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
