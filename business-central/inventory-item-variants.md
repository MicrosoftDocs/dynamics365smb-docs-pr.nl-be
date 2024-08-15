---
title: Productvarianten beheren
description: 'Leer hoe u producten die bijna identiek zijn maar in kleur, maat of materiaal variëren, als artikelvarianten kunt vastleggen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item, variant, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---

# <a name="manage-product-variants"></a>Productvarianten beheren

Artikelvarianten zijn een geweldige manier om uw lijst met producten onder controle te houden. Bijvoorbeeld als u over een groot aantal artikelen beschikt die bijna identiek zijn alleen van kleur verschillen. U kunt elke variant als een afzonderlijk artikel definiëren. Maar u kunt er ook voor kiezen één artikel in te stellen en de verschillende kleuren op te geven als varianten van het artikel.  

> [!TIP]
> Zie [Procedure: varianten](contoso-coffee/manufacturing/variants.md) voor de demogegevens van Contoso Coffee voor een praktische inleiding tot het gebruik van varianten in de productie.  

## <a name="add-variants-to-an-item"></a>Varianten aan een artikel toevoegen

Het is eenvoudig genoeg om varianten voor een artikel te definiëren.  

### <a name="to-add-variants"></a>Varianten toevoegen

1. Open [de pagina **Artikeloverzicht**](https://businesscentral.dynamics.com/?page=31) en open het relevante artikel.  
2. Kies bij  **Item** kaart de actie  **Gerelateerde**, kies vervolgens  **Item** en kies tot slot de actie  **Varianten** .  
3. Geef op de pagina  **Artikelvarianten** de varianten weer.  

Wanneer u vervolgens een verkoopdocument maakt en het artikel toevoegt, kunt u de variant van het artikel opgeven in het veld Variant **Code** . Hetzelfde geldt voor inkoopdocumenten.  

## <a name="item-availability-by-variant"></a>Artikelbeschikbaarheid per variant

[!INCLUDE [inventory_variant-availability](includes/inventory_variant-availability.md)]

## <a name="require-use-of-variants"></a>Gebruik van varianten vereisen

Vanaf releasewave 2 van 2022 kunnen beheerders eisen dat gebruikers de variant opgeven in documenten en dagboeken voor artikelen met varianten. Als u de mogelijkheid wilt activeren, gaat u naar de pagina **Voorraadinstellingen** en selecteert u het veld **Variant verplicht indien aanwezig**. U kunt deze algemene instelling overschrijven voor specifieke artikelen.  

Op artikelkaarten heeft het veld **Variant verplicht indien aanwezig** de volgende opties:

|Veldwaarde |Beschrijving|
|---------|----|
|Standaard (Nee)| De instelling van **Voorraadinstellingen** is van toepassing op dit artikel.|
|Nr.| Gebruikers hoeven geen variant voor dit artikel op te geven.|
|Ja| Als het artikel een of meer varianten heeft, moeten gebruikers de relevante variant opgeven. Als ze dat niet doen, kunnen ze de transactie niet boeken.|

> [!NOTE]
> Deze instellingen zijn niet van invloed op artikelen die geen varianten hebben.

Als de mogelijkheid is ingeschakeld, kunt u geen post boeken als de variant niet is opgegeven.

## <a name="categories-attributes-and-variants"></a>Categorieën, kenmerken en varianten

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a>Zie ook

[Registreer nieuwe items](inventory-how-register-new-items.md)    
[Algemene inventarisinformatie instellen](inventory-how-setup-general.md)    
[Procedure: varianten](contoso-coffee/manufacturing/variants.md)    
