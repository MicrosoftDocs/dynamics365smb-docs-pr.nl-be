---
title: Verbruik in batches boeken
description: Als de afboekingsmethode **Handmatig** is, moet u de materialen handmatig boeken met behulp van een verbruiksdagboek.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 66a19b624c74ec844806c27c490c300746b46704
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787914"
---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="95fc9-103">Productieverbruik in batches boeken</span><span class="sxs-lookup"><span data-stu-id="95fc9-103">Batch Post Production Consumption</span></span>

<span data-ttu-id="95fc9-104">Als de afboekingsmethode **Handmatig** is, moet u de materialen handmatig boeken met behulp van een verbruiksdagboek.</span><span class="sxs-lookup"><span data-stu-id="95fc9-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>  

>[!NOTE]
> <span data-ttu-id="95fc9-105">Als u het selectievakje **Pick vereist** op de vestigingskaart hebt ingeschakeld om aan te geven dat de vestiging voorraadpickverwerking vereist, hoeft u deze batchverwerking niet uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="95fc9-105">If you have placed a check mark in the **Require Pick** field on the location card to indicate that the location requires inventory pick processing, then you do not need to use this batch job.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="95fc9-106">handelt het verbruik dan af wanneer u de voorraadpick boekt.</span><span class="sxs-lookup"><span data-stu-id="95fc9-106">will handle consumption when you post the inventory pick.</span></span> <span data-ttu-id="95fc9-107">Zie [Picken voor productie of assemblage](warehouse-how-to-pick-for-production.md#to-pick-components-in-basic-warehouse-configurations) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="95fc9-107">For more information, see [Pick for Production or Assembly](warehouse-how-to-pick-for-production.md#to-pick-components-in-basic-warehouse-configurations).</span></span> 

<span data-ttu-id="95fc9-108">U kunt [!INCLUDE[prod_short](includes/prod_short.md)] ook zo instellen materialen automatisch worden geboekt (*afgeboekt*) als u productieorders start of voltooit.</span><span class="sxs-lookup"><span data-stu-id="95fc9-108">You can also set up [!INCLUDE[prod_short](includes/prod_short.md)] to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="95fc9-109">Zie voor meer informatie [Afboeking van materialen op basis van de uitvoer van een bewerking inschakelen](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="95fc9-109">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="95fc9-110">Verbruik boeken voor een of meer productieorderregels</span><span class="sxs-lookup"><span data-stu-id="95fc9-110">To post consumption for one or more production order lines</span></span>

1.  <span data-ttu-id="95fc9-111">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verbruiksdagboek** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="95fc9-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="95fc9-112">Voer in de velden informatie over de productieorder en verbruik in.</span><span class="sxs-lookup"><span data-stu-id="95fc9-112">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="95fc9-113">Gebruik de actie **Verbruik berekenen** om journaalregels vanuit productieorders te genereren gebaseerd op de werkelijke output (het aantal gereedgemelde goederen dat u hebt gemeld) of de verwachte output (het aantal gereedgemelde goederen dat u verwacht te produceren).</span><span class="sxs-lookup"><span data-stu-id="95fc9-113">Use the **Calc. Consumption** action to generate journal lines from production orders based on the actual output (the quantity of finished goods that you have reported) or on the expected output (the quantity of finished goods that you expect to produce).</span></span>

    > [!NOTE]
    > <span data-ttu-id="95fc9-114">Als u de vestigingskaart zo hebt geconfigureerd dat magazijnpickverwerking vereist is, kunnen alleen hoeveelheden die al via een magazijnactiviteit zijn gepickt, worden ingevoerd in het veld **Aantal** op de pagina **Verbruiksdagboek**, niet een berekende hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="95fc9-114">If you configured the location card to require warehouse pick processing, then only quantities that are already picked through a warehouse activity can be entered in the **Quantity** field in the **Consumption Journal** page, not any calculated quantity.</span></span> <span data-ttu-id="95fc9-115">Zie voor meer informatie [Picken voor productie of assemblage in geavanceerde magazijnconfiguraties](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)</span><span class="sxs-lookup"><span data-stu-id="95fc9-115">For more information, see [Pick for Production or Assembly in Advanced Warehouse Configurations](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)</span></span>

3.  <span data-ttu-id="95fc9-116">Kies de actie **Boeken** om het verbruik te boeken.</span><span class="sxs-lookup"><span data-stu-id="95fc9-116">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="95fc9-117">De gerelateerde voorraden worden verminderd.</span><span class="sxs-lookup"><span data-stu-id="95fc9-117">The related inventories are reduced.</span></span>



## <a name="see-also"></a><span data-ttu-id="95fc9-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="95fc9-118">See Also</span></span>

<span data-ttu-id="95fc9-119">[Productie](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="95fc9-119">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="95fc9-120">Productie instellen</span><span class="sxs-lookup"><span data-stu-id="95fc9-120">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="95fc9-121">[Gepland](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="95fc9-121">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="95fc9-122">Voorraad</span><span class="sxs-lookup"><span data-stu-id="95fc9-122">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="95fc9-123">Inkoop</span><span class="sxs-lookup"><span data-stu-id="95fc9-123">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="95fc9-124">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="95fc9-124">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
