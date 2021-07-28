---
title: Artikelen categoriseren| Microsoft Docs
description: Om u te helpen zoeken naar artikelen kunt u artikelkenmerken toewijzen en artikelen categoriseren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: category, search, attribute, facet
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b831443bd9e068b4c20f583cc8e0e7132d75ac5e
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6441155"
---
# <a name="categorize-items"></a>Artikelen categoriseren

Om een overzicht van uw artikelen bij te houden en u te helpen artikelen te sorteren en zoeken, is het handig om uw artikelen in artikelcategorieën te organiseren.

Als u artikelen op basis van kenmerken wilt zoeken, kunt u artikelkenmerken aan artikelen en ook aan artikelcategorieën toewijzen. Zie [Werken met artikelkenmerken](inventory-how-work-item-attributes.md) voor meer informatie.
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4j4mo?rel=0]

## <a name="to-create-an-item-category"></a>Een artikelcategorie maken
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelcategorieën** in en kies vervolgens de gerelateerde koppeling.
2. Kies op de pagina **Artikelcategorieën** de actie **Nieuw**.
3. Vul indien nodig de velden op de pagina **Artikelcategoriekaart** op het sneltabblad **Algemeen** in: [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Geef op het sneltabblad **Kenmerken** alle artikelkenmerken voor de artikelcategorie op. Zie voor meer informatie [Artikelkenmerken aan artikelcategorieën toewijzen](inventory-how-work-item-attributes.md#to-assign-item-attributes-to-item-categories).

> [!NOTE]  
> Als de artikelcategorie een bovenliggende artikelcategorie heeft, zoals aangegeven door het veld **Bovenliggende categorie**, worden alle artikelkenmerken die aan die bovenliggende artikelcategorie zijn toegewezen, vooraf ingevuld op het sneltabblad **Kenmerken**.

> [!NOTE]  
> Opmerking: artikelkenmerken die u aan een artikelcategorie toewijst, worden automatisch toegepast op het artikel waaraan de artikelcategorie is toegewezen.

Als u van gedachten verandert over een artikelcategorie, kunt u deze verwijderen. Als deze echter al aan een artikel is toegewezen, moet u die toewijzing verwijderen voordat u de artikelcategorie kunt verwijderen.

## <a name="to-assign-an-item-category-to-an-item"></a>Een artikelcategorie aan een artikel toewijzen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Open de kaart voor het artikel dat u aan een artikelcategorie wilt toewijzen.
3. Kies in het veld **Artikelcategoriecode** de zoekknop en selecteer een bestaande artikelcategorie. U kunt ook de actie **Nieuw** kiezen om eerst een nieuwe artikelcategorie te maken, zoals is uitgelegd in het gedeelte [Een artikelcategorie maken](inventory-how-categorize-items.md#to-create-an-item-category).

## <a name="categories-attributes-and-variants"></a>Categorieën, kenmerken en varianten

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a>Zie ook

[Werken met artikelkenmerken](inventory-how-work-item-attributes.md)  
[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]