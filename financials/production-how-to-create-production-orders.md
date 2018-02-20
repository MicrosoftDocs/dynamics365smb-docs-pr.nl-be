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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 3ffbe781830a492256be864bace38bbef3050596
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="create-production-order-headers"></a><span data-ttu-id="9488a-103">Productieorderkoppen maken</span><span class="sxs-lookup"><span data-stu-id="9488a-103">Create Production Order Headers</span></span>
<span data-ttu-id="9488a-104">U kunt een productieorder handmatig maken. De eerste stap is het maken van een productieorderkop.</span><span class="sxs-lookup"><span data-stu-id="9488a-104">You can create a production order manually, and the first step is to create a production order header.</span></span>

<span data-ttu-id="9488a-105">Productieorders worden meestal automatisch op basis van een planningsfunctie gemaakt om te voldoen aan een bekende vraag.</span><span class="sxs-lookup"><span data-stu-id="9488a-105">Production orders are typically created automatically by a planning function to fulfill a known demand.</span></span> <span data-ttu-id="9488a-106">Zie [Planning](production-planning.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="9488a-106">For more information, see [Planning](production-planning.md).</span></span>   

<span data-ttu-id="9488a-107">In de volgende procedure wordt een vast geplande productieorder gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9488a-107">In the following procedure, a firm planned production order is created.</span></span> <span data-ttu-id="9488a-108">U kunt ook productieorders maken met een andere status.</span><span class="sxs-lookup"><span data-stu-id="9488a-108">You can also create production orders with a different status.</span></span>  

## <a name="to-create-a-production-order-header"></a><span data-ttu-id="9488a-109">Productieorderkoppen maken</span><span class="sxs-lookup"><span data-stu-id="9488a-109">To create a production order header</span></span>  
1.  <span data-ttu-id="9488a-110">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Vast geplande productieorders** in en klik op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="9488a-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9488a-111">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="9488a-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="9488a-112">Selecteer in het veld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="9488a-112">In the **No.**</span></span> <span data-ttu-id="9488a-113">het volgende nummer uit de reeks in.</span><span class="sxs-lookup"><span data-stu-id="9488a-113">field, insert the next number in the series.</span></span>  
4.  <span data-ttu-id="9488a-114">Selecteer in het veld **Bronsoort** de bron van de productieorder.</span><span class="sxs-lookup"><span data-stu-id="9488a-114">In the **Source Type** field, select the source of the production order.</span></span>

    <span data-ttu-id="9488a-115">Hier kunt u opgeven of er voor een familie van artikelen moet worden geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="9488a-115">Here you can select to produce for a family of items.</span></span> <span data-ttu-id="9488a-116">Zie [Werken met productfamilies](production-how-work-family.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="9488a-116">For more information, see [Work With Production Families](production-how-work-family.md).</span></span>
5.  <span data-ttu-id="9488a-117">Selecteer in het veld **Bronnr.** het artikelnummer, de productfamilie of de verkoopkop waarvoor de productieorder moet worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="9488a-117">In the **Source No.** field, select the item number, family, or sales header for which the production order is to be generated.</span></span>  
6.  <span data-ttu-id="9488a-118">Vul de velden **Aantal** en **Vervaldatum** in op basis van de specificaties.</span><span class="sxs-lookup"><span data-stu-id="9488a-118">Fill in the **Quantity** and **Due Date** fields according to your specifications.</span></span>  

<span data-ttu-id="9488a-119">Wanneer productievereisten veranderen, bijvoorbeeld onderdelen of bewerkingen, kunt u de productieorder snel herplannen.</span><span class="sxs-lookup"><span data-stu-id="9488a-119">When production requirements change, such as components or operations, you can quickly replan the production order.</span></span> <span data-ttu-id="9488a-120">Zie [Productieorders direct opnieuw plannen of vernieuwen](production-how-to-replan-refresh-production-orders.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="9488a-120">For more information, see [Replan or Refresh Production Orders Directly](production-how-to-replan-refresh-production-orders.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="9488a-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9488a-121">See Also</span></span>  
<span data-ttu-id="9488a-122">[Productie](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="9488a-122">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="9488a-123">Productie instellen</span><span class="sxs-lookup"><span data-stu-id="9488a-123">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="9488a-124">[Gepland](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="9488a-124">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="9488a-125">Voorraad</span><span class="sxs-lookup"><span data-stu-id="9488a-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="9488a-126">Inkoop</span><span class="sxs-lookup"><span data-stu-id="9488a-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="9488a-127">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9488a-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

