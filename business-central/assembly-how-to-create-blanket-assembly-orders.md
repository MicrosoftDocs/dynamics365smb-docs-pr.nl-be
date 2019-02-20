---
title: Afroepassemblyorders maken | Microsoft Docs
description: Als het veld **Aanvullingsmethode** op de artikelkaart **Assemblage** bevat, is de standaardbevoorradingsmethode van het artikel het assembleren van gedefinieerde onderdelen en mogelijk door een gedefinieerde bron.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 12/20/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 5801fcc1284edfe1b8578518c084455c336d5a40
ms.openlocfilehash: 8796ccf6ce73ded327fad35573a2268e249fb7a7
ms.contentlocale: nl-be
ms.lasthandoff: 12/27/2018

---
# <a name="create-blanket-assembly-orders"></a><span data-ttu-id="6ae26-103">Afroepassemblyorders maken</span><span class="sxs-lookup"><span data-stu-id="6ae26-103">Create Blanket Assembly Orders</span></span>
<span data-ttu-id="6ae26-104">U kunt assemblagebeheer gebruiken om een assemblageartikel op verzoek van een klant aan te passen tijdens het verkoopproces.</span><span class="sxs-lookup"><span data-stu-id="6ae26-104">You can use assembly management to customize an assembly item to a customer’s request during the sales process.</span></span> <span data-ttu-id="6ae26-105">Zie voor meer informatie [Op order geassembleerde artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="6ae26-105">For more information, see [Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>  

 <span data-ttu-id="6ae26-106">Net zoals bij andere artikelen, kunt u ook verkoopraamcontracten maken voor aangepaste assemblageartikelen alvorens u periodiek de werkelijke verkooporders maakt volgens de raamcontractovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="6ae26-106">As with any other type of item, you can also create blanket sales orders for customized assembly items before periodically making the actual sales orders according to the blanket order agreement.</span></span> <span data-ttu-id="6ae26-107">Dit proces omvat verschillende extra stappen wanneer u het vergelijkt met het maken van een normaal raamcontract, en gebruikt assemblageraamcontracten, een variatie van een gekoppelde assemblageorder.</span><span class="sxs-lookup"><span data-stu-id="6ae26-107">This process involves several extra steps when you compare it to creating a regular blanket sales order, and it uses a variation of a linked assembly order, which is a blanket assembly order.</span></span>

> [!NOTE]  
>  <span data-ttu-id="6ae26-108">Net als alle raamcontracten zijn hoeveelheden op assemblageraamcontracten alleen prognoses en niet operationeel totdat ze worden geconverteerd naar werkelijke assemblage orders.</span><span class="sxs-lookup"><span data-stu-id="6ae26-108">Like all blanket orders, quantities on assembly blanket orders are only forecasts and are not operational until they are converted to actual assembly orders.</span></span> <span data-ttu-id="6ae26-109">Orderfunctionaliteit, zoals beschikbaarheidsberekening, reservering en artikeltracering is dan ook niet actief op assemblageraamcontracten.</span><span class="sxs-lookup"><span data-stu-id="6ae26-109">Therefore, order functionality, such as availability calculation, reservation, and item tracking, is not active on blanket assembly orders.</span></span>  

## <a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a><span data-ttu-id="6ae26-110">Een afroepassemblyorder maken voor een voor-order-assembleren-artikel</span><span class="sxs-lookup"><span data-stu-id="6ae26-110">To create a blanket assembly order for an assemble\-to\-order item</span></span>  
1. <span data-ttu-id="6ae26-111">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopraamcontracten** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="6ae26-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Blanket Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="6ae26-112">Maak een nieuw verkoopraamcontract met één regel voor een assemblageartikel.</span><span class="sxs-lookup"><span data-stu-id="6ae26-112">Create a new blanket sales order with one line for an assembly item.</span></span> <span data-ttu-id="6ae26-113">Zie [Verkoopraamcontracten maken](sales-how-to-create-blanket-sales-orders.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="6ae26-113">For more information, see [Create Blanket Sales Orders](sales-how-to-create-blanket-sales-orders.md).</span></span>  
3. <span data-ttu-id="6ae26-114">Voer het volledige aantal in het veld **Aant. op order assembleren** in op de afroepassemblageorderregel.</span><span class="sxs-lookup"><span data-stu-id="6ae26-114">In the **Qty. to Assemble to Order** field on the blanket assembly order line, enter the full quantity.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="6ae26-115">Maak geen raamcontractovereenkomsten voor een gedeeltelijke hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="6ae26-115">You should not create blanket order agreements for a partial quantity.</span></span> <span data-ttu-id="6ae26-116">Daarom moet u dezelfde hoeveelheid invoeren die u hebt ingevoerd in het veld **Hoeveelheid** op de verkoopraamcontractregel.</span><span class="sxs-lookup"><span data-stu-id="6ae26-116">Therefore, you must enter the same quantity that you entered in the **Quantity** field on the blanket sales order line.</span></span>  

4. <span data-ttu-id="6ae26-117">Kies de actie **Op order assembleren** en kies vervolgens de actie **Op orderregels assembleren**.</span><span class="sxs-lookup"><span data-stu-id="6ae26-117">Choose the **Assemble to Order** action, and then choose the **Assemble-to-Order Lines** action.</span></span> <span data-ttu-id="6ae26-118">Of kies het veld **Aant. op order assembleren** op de regel.</span><span class="sxs-lookup"><span data-stu-id="6ae26-118">Alternatively, choose the **Qty. to Assemble to Order)** field on the line.</span></span>  
5. <span data-ttu-id="6ae26-119">Bekijk of wijzig de assemblageorderregels volgens de raamcontractovereenkomst die u met de klant hebt gemaakt op de pagina **Op orderregels assembleren**.</span><span class="sxs-lookup"><span data-stu-id="6ae26-119">On the **Assemble-to-Order Lines** page, review or modify the assembly order lines according to the blanket order agreement that you have made with the customer.</span></span> <span data-ttu-id="6ae26-120">Als u meer informatie wilt, kiest u de actie **Document weergeven** om de volledige afroepassemblyorder te openen.</span><span class="sxs-lookup"><span data-stu-id="6ae26-120">If you want to view more information, choose the **Show Document** action to open the complete blanket assembly order.</span></span> <span data-ttu-id="6ae26-121">U kunt de inhoud van de meeste velden niet wijzigen en u kunt niet boeken.</span><span class="sxs-lookup"><span data-stu-id="6ae26-121">You cannot change the contents of most fields, and you cannot post.</span></span>  
6. <span data-ttu-id="6ae26-122">Wanneer u de assemblageorderregels hebt bijgewerkt volgens de raamcontractovereenkomst, sluit u de pagina **Op orderregels assembleren** om terug te keren naar de pagina **Verkoopraamcontract**.</span><span class="sxs-lookup"><span data-stu-id="6ae26-122">When you have adjusted the assembly order lines according to the blanket order agreement, close the **Assemble-to-Order Lines** page to return to the **Blanket Sales Order** page.</span></span>  
7. <span data-ttu-id="6ae26-123">Wanneer de klant vraagt om een verkooporder op basis van het overeengekomen verkoopraamcontract te maken, maakt u een verkooporder voor het overeengekomen assemblageartikel of de artikelen.</span><span class="sxs-lookup"><span data-stu-id="6ae26-123">When the customer requests to create a sales order based on the agreed blanket sales order, create a sales order for the agreed assembly item or items.</span></span> <span data-ttu-id="6ae26-124">Zie [Verkoopraamcontracten maken](sales-how-to-create-blanket-sales-orders.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="6ae26-124">For more information, see [Create Blanket Sales Orders](sales-how-to-create-blanket-sales-orders.md).</span></span>

<span data-ttu-id="6ae26-125">Het gekoppelde assemblageraamcontract en eventuele aanpassingen zijn gekoppeld aan die nieuwe verkooporder, als voorbereiding op de assemblage van het artikel of de artikelen die verkocht worden.</span><span class="sxs-lookup"><span data-stu-id="6ae26-125">The linked blanket assembly order and any customizations are linked to that new sales order to prepare for assembly of the item or items to be sold.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6ae26-126">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6ae26-126">See Also</span></span>
[<span data-ttu-id="6ae26-127">Verkoopraamcontracten maken</span><span class="sxs-lookup"><span data-stu-id="6ae26-127">Create Blanket Sales Orders</span></span>](sales-how-to-create-blanket-sales-orders.md)  
[<span data-ttu-id="6ae26-128">Assemblagebeheer</span><span class="sxs-lookup"><span data-stu-id="6ae26-128">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="6ae26-129">Werken met stuklijsten</span><span class="sxs-lookup"><span data-stu-id="6ae26-129">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="6ae26-130">Voorraad</span><span class="sxs-lookup"><span data-stu-id="6ae26-130">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="6ae26-131">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="6ae26-131">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="6ae26-132">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6ae26-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
