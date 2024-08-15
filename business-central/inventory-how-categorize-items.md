---
title: Artikelen in categorieën indelen
description: Om u te helpen zoeken naar artikelen kunt u artikelkenmerken toewijzen en artikelen categoriseren.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'category, search, attribute, facet'
ms.search.form: '5730, 5733, 5401'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
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
4. Geef op het sneltabblad **Kenmerken** alle artikelkenmerken voor de artikelcategorie op. Zie voor meer informatie [Artikelkenmerken aan artikelcategorieën toewijzen](inventory-how-work-item-attributes.md#assign-item-attributes-to-item-categories).

> [!NOTE]  
> Als de artikelcategorie een bovenliggende artikelcategorie heeft, zoals aangegeven door het veld **Bovenliggende categorie**, worden alle artikelkenmerken die aan die bovenliggende artikelcategorie zijn toegewezen, vooraf ingevuld op het sneltabblad **Kenmerken**.

> [!NOTE]  
> Opmerking: artikelkenmerken die u aan een artikelcategorie toewijst, worden automatisch toegepast op het artikel waaraan de artikelcategorie is toegewezen.

Als u van gedachten verandert over een artikelcategorie, kunt u deze verwijderen. Als de categorie echter aan een artikel is toegewezen, moet u die toewijzing vooraf verwijderen.

## <a name="to-assign-an-item-category-to-an-item"></a>Een artikelcategorie aan een artikel toewijzen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Open de kaart voor het artikel dat u aan een artikelcategorie wilt toewijzen.
3. Kies in het veld **Artikelcategoriecode** de zoekknop en selecteer een bestaande artikelcategorie. U kunt ook de actie **Nieuw** kiezen om eerst een nieuwe artikelcategorie te maken, zoals is uitgelegd in het gedeelte [Een artikelcategorie maken](inventory-how-categorize-items.md#to-create-an-item-category).

## <a name="categories-attributes-and-variants"></a>Categorieën, kenmerken en varianten

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a>Zie ook

[Werken met itemkenmerken](inventory-how-work-item-attributes.md)    
[productvarianten beheren](inventory-item-variants.md)    
[Registreer nieuwe items](inventory-how-register-new-items.md)    
[Voorraad](inventory-manage-inventory.md)    
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
