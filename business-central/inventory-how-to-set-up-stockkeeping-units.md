---
title: SKU's instellen | Microsoft Docs
description: In SKU's kunt u gegevens opnemen over de artikelen voor een bepaalde vestiging of een bepaalde variantcode.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: c94a02cdbd658efcf96c5cff443ebfe03cb3feef
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3785908"
---
# <a name="set-up-stockkeeping-units"></a><span data-ttu-id="0c9d6-103">SKU's instellen</span><span class="sxs-lookup"><span data-stu-id="0c9d6-103">Set Up Stockkeeping Units</span></span>
<span data-ttu-id="0c9d6-104">In SKU's kunt u gegevens opnemen over de artikelen voor een bepaalde vestiging of een bepaalde variantcode.</span><span class="sxs-lookup"><span data-stu-id="0c9d6-104">You can use stockkeeping units to record information about your items for a specific location or a specific variant code.</span></span>  

 <span data-ttu-id="0c9d6-105">SKU's zijn een aanvulling op de artikelkaarten.</span><span class="sxs-lookup"><span data-stu-id="0c9d6-105">Stockkeeping units are a supplement to item cards.</span></span> <span data-ttu-id="0c9d6-106">Ze vervangen ze niet, hoewel ze wel zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="0c9d6-106">They do not replace them, although they are related to them.</span></span> <span data-ttu-id="0c9d6-107">Met SKU's kunt u voor een bepaald artikel onderscheid maken tussen gegevens betreffende een bepaalde vestiging (bijvoorbeeld een magazijn of distributiecentrum) of een bepaalde variant (bijvoorbeeld verschillende opslaglocatienummers of aanvullingsgegevens).</span><span class="sxs-lookup"><span data-stu-id="0c9d6-107">Stockkeeping units allow you to differentiate information about an item for a specific location, such as a warehouse or distribution center, or a specific variant, such as different shelf numbers and different replenishment information, for the same item.</span></span>  

## <a name="to-set-up-a-stockkeeping-unit"></a><span data-ttu-id="0c9d6-108">SKU's instellen</span><span class="sxs-lookup"><span data-stu-id="0c9d6-108">To set up a stockkeeping unit</span></span>  

1.  <span data-ttu-id="0c9d6-109">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **SKU's** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="0c9d6-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Stockkeeping Units**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0c9d6-110">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="0c9d6-110">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="0c9d6-111">Vul de velden op de kaart in.</span><span class="sxs-lookup"><span data-stu-id="0c9d6-111">Fill in the fields on the card.</span></span> <span data-ttu-id="0c9d6-112">De volgende velden zijn vereist: **Artikelnr.**, **Vestigingscode** en/of **variantcode**.</span><span class="sxs-lookup"><span data-stu-id="0c9d6-112">The following fields are required: **Item No.**, **Location Code**, and/or **Variant Code**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

<span data-ttu-id="0c9d6-113">Als u de eerste SKU voor een artikel hebt ingesteld, wordt het selectievakje **SKU bestaat** op de kaart **Artikel** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="0c9d6-113">When you have set up the first stockkeeping unit for an item, the **Stockkeeping Unit Exists** check box on the **Item** card is selected.</span></span>  

<span data-ttu-id="0c9d6-114">Als u meerdere SKU's voor een artikel wilt maken, kunt u de batchverwerking **SKU maken** gebruiken.</span><span class="sxs-lookup"><span data-stu-id="0c9d6-114">To create several stockkeeping units for an item, use the **Create Stockkeeping Unit** batch job.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0c9d6-115">De gegevens op de **SKU**-kaart hebben voorrang op de gegevens op de **artikelkaart**.</span><span class="sxs-lookup"><span data-stu-id="0c9d6-115">The information on the **Stockkeeping Unit** card has priority over the **Item** card.</span></span>

> [!Warning]
> <span data-ttu-id="0c9d6-116">Wanneer de SKU wordt geleverd via productie, wordt het veld **Vaste verrekenprijs** niet gebruikt bij de facturering en de berekening van de werkelijke kosten van een geproduceerd artikel.</span><span class="sxs-lookup"><span data-stu-id="0c9d6-116">If the SKU is supplied through production, then the **Standard Cost** field is not used when invoicing and adjusting the actual cost of the produced item.</span></span> <span data-ttu-id="0c9d6-117">In plaats daarvan wordt het veld **Vaste verrekenprijs** van de onderliggende artikelkaart gebruikt en worden eventuele afwijkingen berekend tegen het kostenaandeel van dat artikel.</span><span class="sxs-lookup"><span data-stu-id="0c9d6-117">Instead, the **Standard Cost** field on the underlying item card is used, and any variances are calculated against the cost shares of that item.</span></span><br /><br />
> <span data-ttu-id="0c9d6-118">Omdat productiestuklijsten en routering niet kunnen worden toegewezen aan SKU´s, zijn de berekening van kosten per eenheid en de bijbehorende berekening van het kostenaandeel ook niet beschikbaar voor SKU's.</span><span class="sxs-lookup"><span data-stu-id="0c9d6-118">Because production BOMs and routing cannot be assigned to SKUs, then the unit cost roll-up and the related calculation of cost shares are also not available on SKUs.</span></span> <span data-ttu-id="0c9d6-119">Zie [Vaste verrekenprijs berekenen](finance-about-calculating-standard-cost.md) voor nadere informatie</span><span class="sxs-lookup"><span data-stu-id="0c9d6-119">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="0c9d6-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0c9d6-120">See Also</span></span>  
[<span data-ttu-id="0c9d6-121">Nieuwe artikelen registreren</span><span class="sxs-lookup"><span data-stu-id="0c9d6-121">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="0c9d6-122">Magazijnbeheer instellen</span><span class="sxs-lookup"><span data-stu-id="0c9d6-122">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="0c9d6-123">Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="0c9d6-123">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="0c9d6-124">Voorraad</span><span class="sxs-lookup"><span data-stu-id="0c9d6-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="0c9d6-125">[Assemblagebeheer](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="0c9d6-125">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="0c9d6-126">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="0c9d6-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="0c9d6-127">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0c9d6-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
