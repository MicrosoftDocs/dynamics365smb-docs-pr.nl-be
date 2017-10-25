---
title: Expediteurs instellen| Microsoft Docs
description: U kunt een code instellen voor al uw expediteurs en gegevens over hen opgeven.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 84a5d9eb8757dc82834c17327ffbb510cd15fa1a
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-shipping-agents"></a><span data-ttu-id="82ba8-103">Procedure: expediteurs instellen</span><span class="sxs-lookup"><span data-stu-id="82ba8-103">How to: Set Up Shipping Agents</span></span>
<span data-ttu-id="82ba8-104">U kunt een code instellen voor al uw expediteurs en gegevens over hen opgeven.</span><span class="sxs-lookup"><span data-stu-id="82ba8-104">You can set up a code for each of your shipping agents and enter information about them.</span></span>  

<span data-ttu-id="82ba8-105">Als u een Internet-adres opgeeft voor een expediteur die services biedt waarmee zendingen via het Internet kunnen worden getraceerd, kunt u de functie voor het automatisch traceren van zendingen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="82ba8-105">If you enter an Internet address for the shipping agent, and the agent provides package tracking services on the Internet, you can use the automatic package tracking feature.</span></span> <span data-ttu-id="82ba8-106">Zie [Procedure: zendingen traceren](sales-how-track-packages.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="82ba8-106">For more information, see [How to: Track Packages](sales-how-track-packages.md).</span></span>

<span data-ttu-id="82ba8-107">Wanneer u expediteurs instelt op uw verkooporders, kunt u ook opgeven welke services elke expediteur aanbiedt.</span><span class="sxs-lookup"><span data-stu-id="82ba8-107">When you set up shipping agents on your sales orders, you can also specify the services that each shipping agent offers.</span></span>  
<span data-ttu-id="82ba8-108">Voor elke expediteur kunt u een onbeperkt aantal services inclusief bijbehorende verzendtijd opgeven.</span><span class="sxs-lookup"><span data-stu-id="82ba8-108">For each shipping agent, you can set up an unlimited number of services, and you can specify a shipping time for each service.</span></span>  

<span data-ttu-id="82ba8-109">Wanneer u een expediteurservice hebt toegewezen aan een verkooporderregel, wordt de verzendtijd van de service opgenomen op de berekening van de ordertoezegging voor die regel.</span><span class="sxs-lookup"><span data-stu-id="82ba8-109">When you have assigned a shipping agent service to a sales order line, the shipping time of the service will be included in the order promising calculation, for that line.</span></span> <span data-ttu-id="82ba8-110">Zie voor meer informatie [Procedure: ordertoezeggingsdatums berekenen](sales-how-to-calculate-order-promising-dates.md).</span><span class="sxs-lookup"><span data-stu-id="82ba8-110">For more information, see [How to: Calculate Order Promising Dates](sales-how-to-calculate-order-promising-dates.md).</span></span>

## <a name="to-set-up-a-shipping-agent"></a><span data-ttu-id="82ba8-111">Een expediteur instellen</span><span class="sxs-lookup"><span data-stu-id="82ba8-111">To set up a shipping agent</span></span>  
1.  <span data-ttu-id="82ba8-112">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Expediteurs** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="82ba8-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Shipping Agents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="82ba8-113">Vul de velden in.</span><span class="sxs-lookup"><span data-stu-id="82ba8-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="82ba8-114">.</span><span class="sxs-lookup"><span data-stu-id="82ba8-114">.</span></span>  
3.  <span data-ttu-id="82ba8-115">Kies de actie **Expediteurservices**.</span><span class="sxs-lookup"><span data-stu-id="82ba8-115">Choose the **Shipping Agent Services** action.</span></span>
4. <span data-ttu-id="82ba8-116">Vul de velden in **Expediteurservices** naar wens in.</span><span class="sxs-lookup"><span data-stu-id="82ba8-116">In the **Shipping Agent Services**, fill in the fields as necessary.</span></span>

> [!NOTE]  
>  <span data-ttu-id="82ba8-117">Als u de expediteur op de orderregel verwijdert, wordt ook de code voor de expediteurservice verwijderd.</span><span class="sxs-lookup"><span data-stu-id="82ba8-117">If you delete the shipping agent on the order line, the shipping agent service code is also deleted.</span></span> <span data-ttu-id="82ba8-118">Vervolgens wordt de inhoud van de velden die gedeeltelijk op de expediteurservice zijn gebaseerd opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="82ba8-118">The contents of fields that were based in part on the shipping agent service are recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="82ba8-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="82ba8-119">See Also</span></span>
<span data-ttu-id="82ba8-120">[Procedure: zendingen traceren](sales-how-track-packages.md)  </span><span class="sxs-lookup"><span data-stu-id="82ba8-120">[How to: Track Packages](sales-how-track-packages.md)  </span></span>  
[<span data-ttu-id="82ba8-121">Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="82ba8-121">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="82ba8-122">Voorraad</span><span class="sxs-lookup"><span data-stu-id="82ba8-122">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="82ba8-123">[Magazijnbeheer instellen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="82ba8-123">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="82ba8-124">[Assemblagebeheer](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="82ba8-124">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="82ba8-125">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="82ba8-125">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="82ba8-126">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="82ba8-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

