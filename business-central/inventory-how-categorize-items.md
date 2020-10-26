---
title: Artikelen categoriseren| Microsoft Docs
description: Om u te helpen zoeken naar artikelen kunt u artikelkenmerken toewijzen en artikelen categoriseren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a5698746fe52ff7ff6ca38e1207f09ded0742c96
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914125"
---
# <a name="categorize-items"></a><span data-ttu-id="54094-103">Artikelen categoriseren</span><span class="sxs-lookup"><span data-stu-id="54094-103">Categorize Items</span></span>

<span data-ttu-id="54094-104">Om een overzicht van uw artikelen bij te houden en u te helpen artikelen te sorteren en zoeken, is het handig om uw artikelen in artikelcategorieën te organiseren.</span><span class="sxs-lookup"><span data-stu-id="54094-104">To maintain an overview of your items and to help you sort and find items, it is useful to organize your items in item categories.</span></span>

<span data-ttu-id="54094-105">Als u artikelen op basis van kenmerken wilt zoeken, kunt u artikelkenmerken aan artikelen en ook aan artikelcategorieën toewijzen.</span><span class="sxs-lookup"><span data-stu-id="54094-105">To find items by characteristics, you can assign item attributes to items and also to item categories.</span></span> <span data-ttu-id="54094-106">Zie [Werken met artikelkenmerken](inventory-how-work-item-attributes.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="54094-106">For more information, see [Work with Item Attributes](inventory-how-work-item-attributes.md).</span></span>
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category"></a><span data-ttu-id="54094-107">Een artikelcategorie maken</span><span class="sxs-lookup"><span data-stu-id="54094-107">To create an item category</span></span>
1. <span data-ttu-id="54094-108">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelcategorieën** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="54094-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Item Categories** , and then choose the related link.</span></span>
2. <span data-ttu-id="54094-109">Kies op de pagina **Artikelcategorieën** de actie **Nieuw** .</span><span class="sxs-lookup"><span data-stu-id="54094-109">On the **Item Categories** page, choose the **New** action.</span></span>
3. <span data-ttu-id="54094-110">Vul indien nodig de velden op de pagina **Artikelcategoriekaart** op het sneltabblad **Algemeen** in:</span><span class="sxs-lookup"><span data-stu-id="54094-110">On the **Item Category Card** page, on the **General** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="54094-111">Geef op het sneltabblad **Kenmerken** alle artikelkenmerken voor de artikelcategorie op.</span><span class="sxs-lookup"><span data-stu-id="54094-111">On the **Attributes** FastTab, specify any item attributes for the item category.</span></span> <span data-ttu-id="54094-112">Zie voor meer informatie [Artikelkenmerken aan artikelcategorieën toewijzen](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span><span class="sxs-lookup"><span data-stu-id="54094-112">For more information, see [To assign item attributes to item categories](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).</span></span>

> [!NOTE]  
> <span data-ttu-id="54094-113">Als de artikelcategorie een bovenliggende artikelcategorie heeft, zoals aangegeven door het veld **Bovenliggende categorie** , worden alle artikelkenmerken die aan die bovenliggende artikelcategorie zijn toegewezen, vooraf ingevuld op het sneltabblad **Kenmerken** .</span><span class="sxs-lookup"><span data-stu-id="54094-113">If the item category has a parent item category, as indicated by the **Parent Category** field, then any item attributes that are assigned to that parent item category are prefilled on the **Attributes** FastTab.</span></span>

> [!NOTE]  
> <span data-ttu-id="54094-114">Opmerking: artikelkenmerken die u aan een artikelcategorie toewijst, worden automatisch toegepast op het artikel waaraan de artikelcategorie is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="54094-114">Item attributes that you assign to an item category will automatically apply to the item that the item category is assigned to.</span></span>

<span data-ttu-id="54094-115">Als u van gedachten verandert over een artikelcategorie, kunt u deze verwijderen.</span><span class="sxs-lookup"><span data-stu-id="54094-115">If you change your mind about an item category, you can delete it.</span></span> <span data-ttu-id="54094-116">Als deze echter al aan een artikel is toegewezen, moet u die toewijzing verwijderen voordat u de artikelcategorie kunt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="54094-116">However, if it has already been assigned to an item, you must remove that assignment before you can delete the item category.</span></span>

## <a name="to-assign-an-item-category-to-an-item"></a><span data-ttu-id="54094-117">Een artikelcategorie aan een artikel toewijzen</span><span class="sxs-lookup"><span data-stu-id="54094-117">To assign an item category to an item</span></span>

1. <span data-ttu-id="54094-118">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="54094-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items** , and then choose the related link.</span></span>
2. <span data-ttu-id="54094-119">Open de kaart voor het artikel dat u aan een artikelcategorie wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="54094-119">Open the card for the item that you want to assign to an item category.</span></span>
3. <span data-ttu-id="54094-120">Kies in het veld **Artikelcategoriecode** de zoekknop en selecteer een bestaande artikelcategorie.</span><span class="sxs-lookup"><span data-stu-id="54094-120">Choose the lookup button in the **Item Category Code** field and select an existing item category.</span></span> <span data-ttu-id="54094-121">U kunt ook de actie **Nieuw** kiezen om eerst een nieuwe artikelcategorie te maken, zoals is uitgelegd in het gedeelte [Een artikelcategorie maken](inventory-how-categorize-items.md#to-create-an-item-category).</span><span class="sxs-lookup"><span data-stu-id="54094-121">Alternatively, choose the **New** action to first create a new item category as explained in [To create an item category](inventory-how-categorize-items.md#to-create-an-item-category).</span></span>

## <a name="categories-attributes-and-variants"></a><span data-ttu-id="54094-122">Categorieën, kenmerken en varianten</span><span class="sxs-lookup"><span data-stu-id="54094-122">Categories, attributes, and variants</span></span>

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a><span data-ttu-id="54094-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="54094-123">See Also</span></span>

[<span data-ttu-id="54094-124">Werken met artikelkenmerken</span><span class="sxs-lookup"><span data-stu-id="54094-124">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)  
[<span data-ttu-id="54094-125">Nieuwe artikelen registreren</span><span class="sxs-lookup"><span data-stu-id="54094-125">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="54094-126">Voorraad</span><span class="sxs-lookup"><span data-stu-id="54094-126">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="54094-127">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="54094-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
