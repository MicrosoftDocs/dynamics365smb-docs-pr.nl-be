---
title: Productieorders maken op basis van verkooporders
description: U kunt productieorders maken op basis van verkooporders.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/28/2021
ms.author: edupont
ms.openlocfilehash: 438f4d4e1833ba607ceedb9f5d9450c0a4dbb680
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115248"
---
# <a name="create-production-orders-from-sales-orders"></a><span data-ttu-id="72cec-103">Productieorders maken op basis van verkooporders</span><span class="sxs-lookup"><span data-stu-id="72cec-103">Create Production Orders from Sales Orders</span></span>
<span data-ttu-id="72cec-104">U kunt direct op basis van verkooporders productieorders maken voor geproduceerde artikelen.</span><span class="sxs-lookup"><span data-stu-id="72cec-104">You can create production orders for produced items directly from sales orders.</span></span>  

## <a name="to-create-a-production-order-from-a-sales-order"></a><span data-ttu-id="72cec-105">Een productieorder maken op basis van een verkooporder</span><span class="sxs-lookup"><span data-stu-id="72cec-105">To create a production order from a sales order</span></span>  

1.  <span data-ttu-id="72cec-106">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="72cec-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="72cec-107">Selecteer de verkooporder die u wilt omzetten in een productieorder.</span><span class="sxs-lookup"><span data-stu-id="72cec-107">Select the sales order you want to create a production order for.</span></span>  
3.  <span data-ttu-id="72cec-108">Kies de actie **Planning**.</span><span class="sxs-lookup"><span data-stu-id="72cec-108">Choose the **Planning** action.</span></span> <span data-ttu-id="72cec-109">Op de pagina **Verkooporderplanning** kunt u de beschikbaarheid van het verkooporderartikel weergeven.</span><span class="sxs-lookup"><span data-stu-id="72cec-109">On the **Sales Order Planning** page, you can view the availability of the sales order item.</span></span>  
4.  <span data-ttu-id="72cec-110">Kies de actie **Prod.-order maken**.</span><span class="sxs-lookup"><span data-stu-id="72cec-110">Choose the **Create Prod. Order** action.</span></span>  
5.  <span data-ttu-id="72cec-111">Selecteer de status en het ordersoort.</span><span class="sxs-lookup"><span data-stu-id="72cec-111">Select the status and order type.</span></span>  
6.  <span data-ttu-id="72cec-112">Kies de knop **Ja** om een of meer productieorders te maken voor de regels die **Prod.order** in het veld **Aanvullingsmethode** hebben.</span><span class="sxs-lookup"><span data-stu-id="72cec-112">Choose the **Yes** button to create one or more production orders for the lines that have **Prod. Order** in their **Replenishment System** field.</span></span>


> [!NOTE]  
> <span data-ttu-id="72cec-113">Vraagregels in de gemaakte productieorder die **Prod.-order** hebben in het veld **Aanvullingsmethode**, vertegenwoordigen onderliggende productieorders.</span><span class="sxs-lookup"><span data-stu-id="72cec-113">Demand lines in the created production order that have **Prod. Order** in their **Replenishment System** field represent underlying production orders.</span></span> <span data-ttu-id="72cec-114">Nadat u deze productieorders hebt gemaakt, moet u er onvervulde componentvraag voor bepalen met de pagina **Orderplanning** of de functie **Opnieuw plannen** vanuit gemaakte orders.</span><span class="sxs-lookup"><span data-stu-id="72cec-114">After you have generated these production orders, remember to identify any unfulfilled component demand for them using the **Order Planning** page or the **Replan** function from created orders.</span></span> 

## <a name="order-type"></a><span data-ttu-id="72cec-115">Ordersoort</span><span class="sxs-lookup"><span data-stu-id="72cec-115">Order type</span></span>  
<span data-ttu-id="72cec-116">U kunt kiezen uit twee manieren om de productieorders te maken, zoals beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="72cec-116">You can choose between two ways to create the production orders as outlined in the following table.</span></span>

|<span data-ttu-id="72cec-117">Optie</span><span class="sxs-lookup"><span data-stu-id="72cec-117">Option</span></span>|<span data-ttu-id="72cec-118">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="72cec-118">Description</span></span>|
|------|-----------|
|<span data-ttu-id="72cec-119">Artikelorder</span><span class="sxs-lookup"><span data-stu-id="72cec-119">Item Order</span></span>|<span data-ttu-id="72cec-120">Eén productieorder wordt gemaakt voor elke benodigde productieorder die wordt vertegenwoordigd door een regel in het venster **Verkooporderplanning**.</span><span class="sxs-lookup"><span data-stu-id="72cec-120">One production order is created for each needed production order that is represented by a line in the **Sales Order Planning** window.</span></span>|
|<span data-ttu-id="72cec-121">Projectorder</span><span class="sxs-lookup"><span data-stu-id="72cec-121">Project Order</span></span>|<span data-ttu-id="72cec-122">Eén productieorder wordt gemaakt voor alle benodigde productieorders die worden vertegenwoordigd door regels in het venster **Verkooporderplanning**.</span><span class="sxs-lookup"><span data-stu-id="72cec-122">One production order is created for all needed production orders order that are represented by lines in the **Sales Order Planning** window.</span></span> |

<span data-ttu-id="72cec-123">Wanneer u projectorders gebruikt, bevat het veld **Bronsoort** van de productieorder **Verkoopkop** en heeft de order heeft meerdere regels (één voor elk verkoopregelartikel dat moet worden geproduceerd).</span><span class="sxs-lookup"><span data-stu-id="72cec-123">When you use project orders, the **Source Type** field of the production order contains **Sales Header** and the order has multiple lines, one for each sales line item that must be produced.</span></span>  


## <a name="see-also"></a><span data-ttu-id="72cec-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="72cec-124">See Also</span></span>  
[<span data-ttu-id="72cec-125">Productie instellen</span><span class="sxs-lookup"><span data-stu-id="72cec-125">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="72cec-126">[Productie](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="72cec-126">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="72cec-127">Voorraad</span><span class="sxs-lookup"><span data-stu-id="72cec-127">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="72cec-128">Inkoop</span><span class="sxs-lookup"><span data-stu-id="72cec-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="72cec-129">[Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="72cec-129">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="72cec-130">Aanbevolen procedures instellen: voorraadplanning</span><span class="sxs-lookup"><span data-stu-id="72cec-130">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="72cec-131">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="72cec-131">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
