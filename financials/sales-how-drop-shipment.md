---
title: Een verkooporder maken die is gekoppeld aan een inkooporder voor een directe verzending | Microsoft Docs
description: Hierin wordt beschreven hoe u een verkooporder kunt maken die is gekoppeld aan een inkooporder om verzending direct van de leverancier naar de klant mogelijk te maken.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 990867cb428f860b1001177738d1a027f72485bc
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-make-drop-shipments"></a><span data-ttu-id="c07aa-103">Procedure: Doorverzendingen maken</span><span class="sxs-lookup"><span data-stu-id="c07aa-103">How to: Make Drop Shipments</span></span>
<span data-ttu-id="c07aa-104">Een doorverzending is de directe verzending van artikelen van een van uw leveranciers naar een van uw klanten.</span><span class="sxs-lookup"><span data-stu-id="c07aa-104">A drop shipment is the shipment of items from one of your vendors directly to one of your customers.</span></span>

<span data-ttu-id="c07aa-105">Wanneer een verkooporder voor doorverzending is gemarkeerd en u maakt een inkooporder waarin de klant in het veld **Orderklantnr.**</span><span class="sxs-lookup"><span data-stu-id="c07aa-105">When a sales order is marked for drop shipment, and you create a purchase order specifying the customer in the **Sell-to Customer No.**</span></span> <span data-ttu-id="c07aa-106">is opgegeven, kunt u de twee documenten koppelen en daarbij de leverancier opdragen om direct naar de klant te verzenden.</span><span class="sxs-lookup"><span data-stu-id="c07aa-106">field, you can link the two documents and thereby instruct the vendor to ship directly to the customer.</span></span>

## <a name="to-create-a-sales-order-for-drop-shipment"></a><span data-ttu-id="c07aa-107">Een verkooporder voor doorverzending maken</span><span class="sxs-lookup"><span data-stu-id="c07aa-107">To create a sales order for drop shipment</span></span>
<span data-ttu-id="c07aa-108">Ter voorbereiding op een doorverzending maakt u een verkooporder voor een artikel zoals u dat normaal doet, maar u moet wel op de verkoopregel aangeven dat voor de verkoop doorverzending vereist is.</span><span class="sxs-lookup"><span data-stu-id="c07aa-108">To prepare a drop shipment, you create a sales order for an item as normal, except you must indicate on the sales line that the sale requires drop shipment.</span></span>

1. <span data-ttu-id="c07aa-109">Maak een verkooporder voor een artikel.</span><span class="sxs-lookup"><span data-stu-id="c07aa-109">Create a sales order for an item.</span></span> <span data-ttu-id="c07aa-110">Zie [Procedure: Producten verkopen](sales-how-sell-products.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="c07aa-110">For more information, see [How to: Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="c07aa-111">Op de verkooporderregel voor de doorverzending schakelt u het selectievakje **Doorverzending** in.</span><span class="sxs-lookup"><span data-stu-id="c07aa-111">On the sales order line for the drop shipment, select the **Drop Shipment** check box.</span></span> <span data-ttu-id="c07aa-112">Gebruik de functie **Kolommen kiezen** als het veld niet zichtbaar is.</span><span class="sxs-lookup"><span data-stu-id="c07aa-112">Use the **Choose Columns** function if the field is not visible.</span></span> <span data-ttu-id="c07aa-113">Zie [Persoonlijke gebruikersinstellingen](ui-user-personalization.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="c07aa-113">For more information, see [User Personalization](ui-user-personalization.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="c07aa-114">Deze functionaliteit vereist dat uw ervaring is ingesteld op **Suite**.</span><span class="sxs-lookup"><span data-stu-id="c07aa-114">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="c07aa-115">Zie voor meer informatie [Uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-ervaring aanpassen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="c07aa-115">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-create-the-purchase-order-for-drop-shipment"></a><span data-ttu-id="c07aa-116">De inkooporder voor doorverzendingen maken</span><span class="sxs-lookup"><span data-stu-id="c07aa-116">To create the purchase order for drop shipment</span></span>
<span data-ttu-id="c07aa-117">Ter voorbereiding op een doorverzending van het artikel dat u wilt verkopen, maakt u een inkooporder zoals u dat normaal doet, maar u moet op de inkooporder wel aangeven dat het artikel naar de klant moet worden verzonden en niet naar uzelf.</span><span class="sxs-lookup"><span data-stu-id="c07aa-117">To prepare a drop shipment for the item to be sold, you create a purchase order as normal, except you must indicate on the purchase order that it must be shipped to your customer, not to yourself.</span></span>

1. <span data-ttu-id="c07aa-118">Inkooporder maken.</span><span class="sxs-lookup"><span data-stu-id="c07aa-118">Create a purchase order.</span></span> <span data-ttu-id="c07aa-119">Vul geen velden op de regels in.</span><span class="sxs-lookup"><span data-stu-id="c07aa-119">Do not fill any fields on the lines.</span></span> <span data-ttu-id="c07aa-120">Zie voor meer informatie [Procedure: Inkopen vastleggen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="c07aa-120">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>
2. <span data-ttu-id="c07aa-121">Selecteer in het veld **Orderklantnr.**</span><span class="sxs-lookup"><span data-stu-id="c07aa-121">In the **Sell-to Customer No.**</span></span> <span data-ttu-id="c07aa-122">de klant aan wie u verkoopt.</span><span class="sxs-lookup"><span data-stu-id="c07aa-122">field, select the customer that you are selling to.</span></span>
3. <span data-ttu-id="c07aa-123">Kies de actie **Doorverzendingen** en kies vervolgens de actie **Verkooporder ophalen**.</span><span class="sxs-lookup"><span data-stu-id="c07aa-123">Choose the **Drop Shipments** action, and then choose the **Get Sales Order** action.</span></span>
4. <span data-ttu-id="c07aa-124">Selecteer in het venster **Verkoopoverzicht** de verkooporder die u hebt voorbereid in de sectie "Een verkooporder voor doorverzending maken".</span><span class="sxs-lookup"><span data-stu-id="c07aa-124">In the **Sales List** window, select the sales order that you prepared in the "To create a sales order for drop shipment" section.</span></span>
5. <span data-ttu-id="c07aa-125">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="c07aa-125">Choose the **OK** button.</span></span>

<span data-ttu-id="c07aa-126">De regelgegevens van de verkooporder worden ingevoegd op de inkooporderregel(s).</span><span class="sxs-lookup"><span data-stu-id="c07aa-126">The line information from the sales order is inserted on the purchase order line(s).</span></span>

<span data-ttu-id="c07aa-127">U kunt de leverancier nu opdragen om de artikelen naar de klant te verzenden, bijvoorbeeld door de inkooporder als een PDF via e-mail te verzenden.</span><span class="sxs-lookup"><span data-stu-id="c07aa-127">You can now instruct the vendor to ship the items to your customer, for example, by mailing the purchase order as a PDF.</span></span>     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a><span data-ttu-id="c07aa-128">De gekoppelde inkooporder weergeven op basis van de verkooporder</span><span class="sxs-lookup"><span data-stu-id="c07aa-128">To view the linked purchase order from the sales order</span></span>
* <span data-ttu-id="c07aa-129">Selecteer de verkooporderregel van de doorverzending, kies de actie **Order**, kies de actie **Doorverzending** en kies vervolgens de actie **Inkooporder**.</span><span class="sxs-lookup"><span data-stu-id="c07aa-129">Select the drop-shipment sales order line, choose the **Order** action, choose the **Drop Shipment** action, and then choose the **Purchase Order** action.</span></span>

## <a name="to-post-a-drop-shipment"></a><span data-ttu-id="c07aa-130">Een doorverzending boeken</span><span class="sxs-lookup"><span data-stu-id="c07aa-130">To post a drop shipment</span></span>
<span data-ttu-id="c07aa-131">Nadat de leverancier de artikelen heeft verzonden, kunt u de verkooporder boeken als verzonden.</span><span class="sxs-lookup"><span data-stu-id="c07aa-131">After the vendor ships the items, you can post the sales order as shipped.</span></span> <span data-ttu-id="c07aa-132">U kunt de inkooporder ook boeken, maar alleen met de optie **Ontvangen**, totdat de verkooporder is gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="c07aa-132">You can also post the purchase order, but only with the **Receive** option until the sales order has been invoiced.</span></span>

1. <span data-ttu-id="c07aa-133">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verkooporders** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="c07aa-133">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="c07aa-134">Open de verkooporder die u hebt gemaakt in de sectie "Een verkooporder voor een doorverzending maken".</span><span class="sxs-lookup"><span data-stu-id="c07aa-134">Open the sales order that you created in the "To create a sales order for a drop shipment" section.</span></span>
3. <span data-ttu-id="c07aa-135">Geef in het veld **Te verzenden aantal** op hoeveel van de orderhoeveelheid moet worden verzonden, de volledige of gedeeltelijke orderhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="c07aa-135">In the **Qty. to Ship** field, specify how many of the order quantity to ship, the full or a partial order quantity.</span></span>
4. <span data-ttu-id="c07aa-136">Kies de actie **Boeken** of **Boeken en verzenden**.</span><span class="sxs-lookup"><span data-stu-id="c07aa-136">Choose the **Post** or **Post and Send** action.</span></span>
5. <span data-ttu-id="c07aa-137">Kies vervolgens **de optie Verzenden** om later te factureren of de optie **Verzenden en factureren** om meteen te factureren.</span><span class="sxs-lookup"><span data-stu-id="c07aa-137">Choose either the **Ship** option to invoice later, or the **Ship and Invoice** option to invoice immediately.</span></span>

## <a name="see-also"></a><span data-ttu-id="c07aa-138">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c07aa-138">See Also</span></span>
<span data-ttu-id="c07aa-139">[Procedure: Speciale orders maken](sales-how-to-create-special-orders.md)|</span><span class="sxs-lookup"><span data-stu-id="c07aa-139">[How to: Create Special Orders](sales-how-to-create-special-orders.md)|</span></span>  
[<span data-ttu-id="c07aa-140">Procedure: Producten verkopen</span><span class="sxs-lookup"><span data-stu-id="c07aa-140">How to: Sell Products</span></span>](sales-how-sell-products.md)  
[<span data-ttu-id="c07aa-141">Procedure: Inkopen vastleggen</span><span class="sxs-lookup"><span data-stu-id="c07aa-141">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)  
[<span data-ttu-id="c07aa-142">Verkoop</span><span class="sxs-lookup"><span data-stu-id="c07aa-142">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="c07aa-143">Voorraad</span><span class="sxs-lookup"><span data-stu-id="c07aa-143">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="c07aa-144">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c07aa-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

