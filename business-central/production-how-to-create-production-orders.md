---
title: Productieorderkoppen maken | Microsoft Docs
description: U kunt een productieorder handmatig maken. De eerste stap is het maken van een productieorderkop.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 70a6f2e583e5ba78eecae0a25d6533d8265414ca
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1253321"
---
# <a name="create-production-order-headers"></a><span data-ttu-id="8c82c-103">Productieorderkoppen maken</span><span class="sxs-lookup"><span data-stu-id="8c82c-103">Create Production Order Headers</span></span>
<span data-ttu-id="8c82c-104">U kunt een productieorder handmatig maken. De eerste stap is het maken van een productieorderkop.</span><span class="sxs-lookup"><span data-stu-id="8c82c-104">You can create a production order manually, and the first step is to create a production order header.</span></span>

<span data-ttu-id="8c82c-105">Productieorders worden meestal automatisch op basis van een planningsfunctie gemaakt om te voldoen aan een bekende vraag.</span><span class="sxs-lookup"><span data-stu-id="8c82c-105">Production orders are typically created automatically by a planning function to fulfill a known demand.</span></span> <span data-ttu-id="8c82c-106">Zie [Planning](production-planning.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8c82c-106">For more information, see [Planning](production-planning.md).</span></span>   

<span data-ttu-id="8c82c-107">In de volgende procedure wordt een vast geplande productieorder gemaakt.</span><span class="sxs-lookup"><span data-stu-id="8c82c-107">In the following procedure, a firm planned production order is created.</span></span> <span data-ttu-id="8c82c-108">U kunt ook productieorders maken met een andere status.</span><span class="sxs-lookup"><span data-stu-id="8c82c-108">You can also create production orders with a different status.</span></span>  

## <a name="to-create-a-production-order-header"></a><span data-ttu-id="8c82c-109">Productieorderkoppen maken</span><span class="sxs-lookup"><span data-stu-id="8c82c-109">To create a production order header</span></span>  
1.  <span data-ttu-id="8c82c-110">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vast geplande productieorders** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="8c82c-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="8c82c-111">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="8c82c-111">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="8c82c-112">Selecteer in het veld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="8c82c-112">In the **No.**</span></span> <span data-ttu-id="8c82c-113">het volgende nummer uit de reeks in.</span><span class="sxs-lookup"><span data-stu-id="8c82c-113">field, insert the next number in the series.</span></span>  
4.  <span data-ttu-id="8c82c-114">Selecteer in het veld **Bronsoort** de bron van de productieorder.</span><span class="sxs-lookup"><span data-stu-id="8c82c-114">In the **Source Type** field, select the source of the production order.</span></span>

    <span data-ttu-id="8c82c-115">Hier kunt u opgeven of er voor een familie van artikelen moet worden geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="8c82c-115">Here you can select to produce for a family of items.</span></span> <span data-ttu-id="8c82c-116">Zie [Werken met productfamilies](production-how-work-family.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8c82c-116">For more information, see [Work With Production Families](production-how-work-family.md).</span></span>
5.  <span data-ttu-id="8c82c-117">Selecteer in het veld **Bronnr.** het artikelnummer, de productfamilie of de verkoopkop waarvoor de productieorder moet worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="8c82c-117">In the **Source No.** field, select the item number, family, or sales header for which the production order is to be generated.</span></span>  
6.  <span data-ttu-id="8c82c-118">Vul de velden **Aantal** en **Vervaldatum** in op basis van de specificaties.</span><span class="sxs-lookup"><span data-stu-id="8c82c-118">Fill in the **Quantity** and **Due Date** fields according to your specifications.</span></span>  

<span data-ttu-id="8c82c-119">Wanneer productievereisten veranderen, bijvoorbeeld onderdelen of bewerkingen, kunt u de productieorder snel herplannen.</span><span class="sxs-lookup"><span data-stu-id="8c82c-119">When production requirements change, such as components or operations, you can quickly replan the production order.</span></span> <span data-ttu-id="8c82c-120">Zie [Productieorders direct opnieuw plannen of vernieuwen](production-how-to-replan-refresh-production-orders.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8c82c-120">For more information, see [Replan or Refresh Production Orders Directly](production-how-to-replan-refresh-production-orders.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="8c82c-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8c82c-121">See Also</span></span>  
<span data-ttu-id="8c82c-122">[Productie](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="8c82c-122">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="8c82c-123">Productie instellen</span><span class="sxs-lookup"><span data-stu-id="8c82c-123">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="8c82c-124">[Gepland](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="8c82c-124">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="8c82c-125">Voorraad</span><span class="sxs-lookup"><span data-stu-id="8c82c-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="8c82c-126">Inkoop</span><span class="sxs-lookup"><span data-stu-id="8c82c-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="8c82c-127">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8c82c-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
