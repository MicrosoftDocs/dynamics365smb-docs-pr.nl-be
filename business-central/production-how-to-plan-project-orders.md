---
title: Projectorders plannen | Microsoft Docs
description: Deze planningstaak wordt gestart vanaf een verkooporder en gebruikt het venster **Verkooporderplanning**. Wanneer u eenmaal een projectproductieorder hebt gemaakt, kunt u deze verder plannen in het venster **Orderplanning**.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 08cd8c323e8f5221bd6915618582441a739e77c8
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="plan-project-orders"></a><span data-ttu-id="28187-104">Projectorders plannen</span><span class="sxs-lookup"><span data-stu-id="28187-104">Plan Project Orders</span></span>
<span data-ttu-id="28187-105">Deze planningstaak wordt gestart vanaf een verkooporder en gebruikt het venster **Verkooporderplanning**.</span><span class="sxs-lookup"><span data-stu-id="28187-105">This planning task starts from a sales order and uses the **Sales Order Planning** window.</span></span> <span data-ttu-id="28187-106">Wanneer u eenmaal een projectproductieorder hebt gemaakt, kunt u deze verder plannen in het venster **Orderplanning**.</span><span class="sxs-lookup"><span data-stu-id="28187-106">Once you have created a project production order, you can plan it further by using the **Order Planning** window.</span></span>  

## <a name="to-create-a-project-production-order"></a><span data-ttu-id="28187-107">Een projectproductieorder maken</span><span class="sxs-lookup"><span data-stu-id="28187-107">To create a project production order</span></span>  

1.  <span data-ttu-id="28187-108">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="28187-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="28187-109">Selecteer de verkooporder die het productieproject vertegenwoordigt en kies de actie **Planning**.</span><span class="sxs-lookup"><span data-stu-id="28187-109">Select the sales order that represents the production project, and then choose the **Planning** action.</span></span>  
4.  <span data-ttu-id="28187-110">Kies in het venster **Verkooporderplanning** de actie **Prod.-order maken**.</span><span class="sxs-lookup"><span data-stu-id="28187-110">In the **Sales Order Planning** window, choose  the **Create Prod. Order** action.</span></span>  
5.  <span data-ttu-id="28187-111">Selecteer in het venster **Prod.order voor verkooporder maken** de optie **Projectorder** in het veld **Ordersoort**.</span><span class="sxs-lookup"><span data-stu-id="28187-111">In the **Create Order from Sales** window, in the **Order Type** field, select **Project Order**.</span></span>  
6.  <span data-ttu-id="28187-112">Kies de knop **Ja**.</span><span class="sxs-lookup"><span data-stu-id="28187-112">Choose the **Yes** button.</span></span>  
7.  <span data-ttu-id="28187-113">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Productieorders** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="28187-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Production Orders**, and then choose the related link.</span></span>
8. <span data-ttu-id="28187-114">Open de zojuist gemaakte productieorder.</span><span class="sxs-lookup"><span data-stu-id="28187-114">Open the production order just created.</span></span>  

    <span data-ttu-id="28187-115">Het veld **Bronsoort** van de productieorder bevat **Verkoopkop** en de order heeft meerdere regels (één voor elk verkoopregelartikel dat moet worden geproduceerd).</span><span class="sxs-lookup"><span data-stu-id="28187-115">Notice that the **Source Type** field of the production order contains **Sales Header** and the order has multiple lines, one for each sales line item that must be produced.</span></span>  
9. <span data-ttu-id="28187-116">Kies de actie **Planning**.</span><span class="sxs-lookup"><span data-stu-id="28187-116">Choose the **Planning** action.</span></span>
10. <span data-ttu-id="28187-117">In het venster **Orderplanning** kiest u de actie **Vernieuwen** om nieuwe vraag te berekenen.</span><span class="sxs-lookup"><span data-stu-id="28187-117">In the **Order Planning** window, choose the **Refresh** action to calculate new demand.</span></span>  

<span data-ttu-id="28187-118">De orderkopregel voor de projectorder wordt weergegeven met daaronder alle uitgevouwen regels met vraag waaraan niet is voldaan.</span><span class="sxs-lookup"><span data-stu-id="28187-118">The order header line for the project order is displayed with all unfulfilled demand lines expanded under it.</span></span> <span data-ttu-id="28187-119">Hoewel de productieorder regels bevat voor verschillende geproduceerde artikelen, wordt de totale vraag voor alle productieorderregels onder één orderkopregel in het venster **Orderplanning** vermeld, samen met de oorspronkelijke klantnaam.</span><span class="sxs-lookup"><span data-stu-id="28187-119">Although the production order contains lines for several produced items, the total demand for all production order lines is listed under one order header line in the **Order Planning** window, and the original customer name is displayed.</span></span> <span data-ttu-id="28187-120">U kunt nu doorgaan met de planning van regels zoals beschreven in [Nieuwe vraag order voor order plannen](production-how-to-plan-for-new-demand.md).</span><span class="sxs-lookup"><span data-stu-id="28187-120">You can now proceed to plan for the demand as described in [Plan for New Demand Order by Order](production-how-to-plan-for-new-demand.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="28187-121">Vraagregels in de projectproductieorder die een **Prod.-order** hebben in het veld **Aanvullingsmethode**, vertegenwoordigen onderliggende productieorders.</span><span class="sxs-lookup"><span data-stu-id="28187-121">Demand lines in the project production order that have **Prod. Order** in their **Replenishment System** field represent underlying production orders.</span></span> <span data-ttu-id="28187-122">Nadat u deze productieorders hebt gemaakt, moet u opnieuw een plan berekenen in het venster **Orderplanning** om de eventuele niet-afgehandelde vraag naar deze materialen te bepalen.</span><span class="sxs-lookup"><span data-stu-id="28187-122">After you have generated these production orders, you must again calculate a plan in the **Order Planning** window to identify any unfulfilled component demand for them.</span></span> <span data-ttu-id="28187-123">In dat geval worden deze als vraagregels onder een normale productieorderkopregel weergegeven, wat betekent dat de projectrelatie niet langer zichtbaar is in het venster.</span><span class="sxs-lookup"><span data-stu-id="28187-123">In that case, they are displayed as demand lines under a normal production order header line, meaning, the project relation is no longer visible in the window.</span></span> <span data-ttu-id="28187-124">Wanneer u echter ordertracering gebruikt, kunt u vooruit- en terugkijken naar alle orders voor voorzieningen die onder de oorspronkelijke verkooporder zijn gemaakt</span><span class="sxs-lookup"><span data-stu-id="28187-124">However, if you are using the Order Tracking feature, then you can look back and forth to all supply orders made under the original sales order.</span></span>  

## <a name="see-also"></a><span data-ttu-id="28187-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="28187-125">See Also</span></span>
<span data-ttu-id="28187-126">[Gepland](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="28187-126">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="28187-127">Productie instellen</span><span class="sxs-lookup"><span data-stu-id="28187-127">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="28187-128">[Productie](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="28187-128">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="28187-129">Voorraad</span><span class="sxs-lookup"><span data-stu-id="28187-129">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="28187-130">Inkoop</span><span class="sxs-lookup"><span data-stu-id="28187-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="28187-131">[Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="28187-131">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="28187-132">Aanbevolen procedures instellen: voorraadplanning</span><span class="sxs-lookup"><span data-stu-id="28187-132">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="28187-133">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="28187-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

