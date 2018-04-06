---
title: SKU's instellen | Microsoft Docs
description: In SKU's kunt u gegevens opnemen over de artikelen voor een bepaalde vestiging of een bepaalde variantcode.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4870e82d4390e0a96a137579d035fee0e54b19eb
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-stockkeeping-units"></a><span data-ttu-id="b20df-103">SKU's instellen</span><span class="sxs-lookup"><span data-stu-id="b20df-103">Set Up Stockkeeping Units</span></span>
<span data-ttu-id="b20df-104">In SKU's kunt u gegevens opnemen over de artikelen voor een bepaalde vestiging of een bepaalde variantcode.</span><span class="sxs-lookup"><span data-stu-id="b20df-104">You can use stockkeeping units to record information about your items for a specific location or a specific variant code.</span></span>  

 <span data-ttu-id="b20df-105">SKU's zijn een aanvulling op de artikelkaarten.</span><span class="sxs-lookup"><span data-stu-id="b20df-105">Stockkeeping units are a supplement to item cards.</span></span> <span data-ttu-id="b20df-106">Ze vervangen ze niet, hoewel ze wel zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="b20df-106">They do not replace them, although they are related to them.</span></span> <span data-ttu-id="b20df-107">Met SKU's kunt u voor een bepaald artikel onderscheid maken tussen gegevens betreffende een bepaalde vestiging (bijvoorbeeld een magazijn of distributiecentrum) of een bepaalde variant (bijvoorbeeld verschillende opslaglocatienummers of aanvullingsgegevens).</span><span class="sxs-lookup"><span data-stu-id="b20df-107">Stockkeeping units allow you to differentiate information about an item for a specific location, such as a warehouse or distribution center, or a specific variant, such as different shelf numbers and different replenishment information, for the same item.</span></span>  

## <a name="to-set-up-a-stockkeeping-unit"></a><span data-ttu-id="b20df-108">SKU's instellen</span><span class="sxs-lookup"><span data-stu-id="b20df-108">To set up a stockkeeping unit</span></span>  

1.  <span data-ttu-id="b20df-109">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Zoeken naar pagina of rapport"), voer **SKU's** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="b20df-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Stockkeeping Units**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b20df-110">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="b20df-110">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="b20df-111">Vul de velden op de kaart in.</span><span class="sxs-lookup"><span data-stu-id="b20df-111">Fill in the fields on the card.</span></span> <span data-ttu-id="b20df-112">De volgende velden zijn vereist: **Artikelnr.**, **Vestigingscode** en/of **variantcode**.</span><span class="sxs-lookup"><span data-stu-id="b20df-112">The following fields are required: **Item No.**, **Location Code**, and/or **Variant Code**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

<span data-ttu-id="b20df-113">Als u de eerste SKU voor een artikel hebt ingesteld, wordt het selectievakje **SKU bestaat** op de kaart **Artikel** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="b20df-113">When you have set up the first stockkeeping unit for an item, the **Stockkeeping Unit Exists** check box on the **Item** card is selected.</span></span>  

<span data-ttu-id="b20df-114">Als u meerdere SKU's voor een artikel wilt maken, kunt u de batchverwerking **SKU maken** gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b20df-114">To create several stockkeeping units for an item, use the **Create Stockkeeping Unit** batch job.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b20df-115">De gegevens op de **SKU**-kaart hebben voorrang op de gegevens op de **artikelkaart**.</span><span class="sxs-lookup"><span data-stu-id="b20df-115">The information on the **Stockkeeping Unit** card has priority over the **Item** card.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b20df-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b20df-116">See Also</span></span>  
[<span data-ttu-id="b20df-117">Nieuwe artikelen registreren</span><span class="sxs-lookup"><span data-stu-id="b20df-117">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="b20df-118">Magazijnbeheer instellen</span><span class="sxs-lookup"><span data-stu-id="b20df-118">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="b20df-119">Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="b20df-119">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="b20df-120">Voorraad</span><span class="sxs-lookup"><span data-stu-id="b20df-120">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="b20df-121">[Assemblagebeheer](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="b20df-121">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="b20df-122">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="b20df-122">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="b20df-123">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b20df-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

