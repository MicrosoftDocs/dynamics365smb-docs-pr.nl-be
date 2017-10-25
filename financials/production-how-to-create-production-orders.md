---
title: Productieorderkoppen maken | Microsoft Docs
description: U kunt een productieorder handmatig maken. De eerste stap is het maken van een productieorderkop.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0c792dbb7d7261e8f8b89ca4f3d39d875142c4eb
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-production-order-headers"></a><span data-ttu-id="64c5a-103">Procedure: productieorderkoppen maken</span><span class="sxs-lookup"><span data-stu-id="64c5a-103">How to: Create Production Order Headers</span></span>
<span data-ttu-id="64c5a-104">U kunt een productieorder handmatig maken. De eerste stap is het maken van een productieorderkop.</span><span class="sxs-lookup"><span data-stu-id="64c5a-104">You can create a production order manually, and the first step is to create a production order header.</span></span>

<span data-ttu-id="64c5a-105">Productieorders worden meestal automatisch op basis van een planningsfunctie gemaakt om te voldoen aan een bekende vraag.</span><span class="sxs-lookup"><span data-stu-id="64c5a-105">Production orders are typically created automatically by a planning function to fulfill a known demand.</span></span> <span data-ttu-id="64c5a-106">Zie [Planning](production-planning.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="64c5a-106">For more information, see [Planning](production-planning.md).</span></span>   

<span data-ttu-id="64c5a-107">In de volgende procedure wordt een vast geplande productieorder gemaakt.</span><span class="sxs-lookup"><span data-stu-id="64c5a-107">In the following procedure, a firm planned production order is created.</span></span> <span data-ttu-id="64c5a-108">U kunt ook productieorders maken met een andere status.</span><span class="sxs-lookup"><span data-stu-id="64c5a-108">You can also create production orders with a different status.</span></span>  

## <a name="to-create-a-production-order-header"></a><span data-ttu-id="64c5a-109">Productieorderkoppen maken</span><span class="sxs-lookup"><span data-stu-id="64c5a-109">To create a production order header</span></span>  
1.  <span data-ttu-id="64c5a-110">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Vast geplande productieorders** in en klik op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="64c5a-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="64c5a-111">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="64c5a-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="64c5a-112">Selecteer in het veld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="64c5a-112">In the **No.**</span></span> <span data-ttu-id="64c5a-113">het volgende nummer uit de reeks in.</span><span class="sxs-lookup"><span data-stu-id="64c5a-113">field, insert the next number in the series.</span></span>  
4.  <span data-ttu-id="64c5a-114">Selecteer in het veld **Bronsoort** de bron van de productieorder.</span><span class="sxs-lookup"><span data-stu-id="64c5a-114">In the **Source Type** field, select the source of the production order.</span></span>

    <span data-ttu-id="64c5a-115">Hier kunt u opgeven of er voor een familie van artikelen moet worden geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="64c5a-115">Here you can select to produce for a family of items.</span></span> <span data-ttu-id="64c5a-116">Zie [Procedure: Werken met productfamilies](production-how-work-family.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="64c5a-116">For more information, see [How to: Work With Production Families](production-how-work-family.md).</span></span>
5.  <span data-ttu-id="64c5a-117">Selecteer in het veld **Bronnr.** het artikelnummer, de productfamilie of de verkoopkop waarvoor de productieorder moet worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="64c5a-117">In the **Source No.** field, select the item number, family, or sales header for which the production order is to be generated.</span></span>  
6.  <span data-ttu-id="64c5a-118">Vul de velden **Aantal** en **Vervaldatum** in op basis van de specificaties.</span><span class="sxs-lookup"><span data-stu-id="64c5a-118">Fill in the **Quantity** and **Due Date** fields according to your specifications.</span></span>  

<span data-ttu-id="64c5a-119">Wanneer productievereisten veranderen, bijvoorbeeld onderdelen of bewerkingen, kunt u de productieorder snel herplannen.</span><span class="sxs-lookup"><span data-stu-id="64c5a-119">When production requirements change, such as components or operations, you can quickly replan the production order.</span></span> <span data-ttu-id="64c5a-120">Zie [Procedure: Productieorders direct opnieuw plannen of vernieuwen](production-how-to-replan-refresh-production-orders.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="64c5a-120">For more information, see [How to: Replan or Refresh Production Orders Directly](production-how-to-replan-refresh-production-orders.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="64c5a-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="64c5a-121">See Also</span></span>  
<span data-ttu-id="64c5a-122">[Productie](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="64c5a-122">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="64c5a-123">Productie instellen</span><span class="sxs-lookup"><span data-stu-id="64c5a-123">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="64c5a-124">[Gepland](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="64c5a-124">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="64c5a-125">Voorraad</span><span class="sxs-lookup"><span data-stu-id="64c5a-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="64c5a-126">Inkoop</span><span class="sxs-lookup"><span data-stu-id="64c5a-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="64c5a-127">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="64c5a-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

