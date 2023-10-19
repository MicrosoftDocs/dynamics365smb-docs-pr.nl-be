---
title: Productvarianten beheren
description: 'Leer hoe u producten die bijna identiek zijn maar in kleur, maat of materiaal variëren, als artikelvarianten kunt vastleggen.'
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: 'item, variant, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 09/26/2022
ms.author: bholtorf
---
# <a name="manage-product-variants"></a>Productvarianten beheren

Artikelvarianten zijn een geweldige manier om uw lijst met producten onder controle te houden. Bijvoorbeeld als u over een groot aantal artikelen beschikt die bijna identiek zijn alleen van kleur verschillen. U kunt elke variant als een afzonderlijk artikel definiëren. Maar u kiest ervoor om één artikel in te stellen en de verschillende kleuren op te geven als varianten van het artikel.  

> [!TIP]
> Zie [Procedure: varianten](contoso-coffee/manufacturing/variants.md) voor de demogegevens van Contoso Coffee voor een praktische inleiding tot het gebruik van varianten in de productie.  

## <a name="add-variants-to-an-item"></a>Varianten aan een artikel toevoegen

Als uw organisatie heeft besloten varianten te gebruiken, is het eenvoudig genoeg om varianten voor een artikel te definiëren.  

### <a name="to-add-variants"></a>Varianten toevoegen

1. Open [de pagina **Artikeloverzicht**](https://businesscentral.dynamics.com/?page=31) en open het relevante artikel.  
2. Kies op de kaart **Artikel** de actie **Artikel** en kies vervolgens de actie **Varianten**.  
3. Vermeld de varianten op de pagina **Artikelvarianten**.  

Wanneer u vervolgens een verkoopdocument maakt en het artikel toevoegt, kunt u de variant van het artikel specificeren in het veld **Variantcode**. Hetzelfde geldt voor inkoopdocumenten.  

## <a name="item-availability-by-variant"></a>Artikelbeschikbaarheid per variant

[!INCLUDE [inventory_variant-availability](includes/inventory_variant-availability.md)]

## <a name="require-use-of-variants"></a>Gebruik van varianten vereisen

Vanaf releasewave 2 van 2022 kunnen beheerders eisen dat gebruikers de variant opgeven in documenten en dagboeken voor artikelen met varianten. U kunt de mogelijkheid activeren door naar de pagina **Voorraadinstellingen** te navigeren en vervolgens het veld **Variant verplicht indien aanwezig** te selecteren. U kunt deze algemene instelling overschrijven voor specifieke artikelen.  

Op artikelkaarten heeft het veld **Variant verplicht indien aanwezig** de volgende opties:

|Veldwaarde |Omschrijving|
|---------|----|
|Standaard| De instelling van **Voorraadinstellingen** is van toepassing op dit artikel.|
|Nr.| Gebruikers hoeven geen variant voor dit artikel op te geven.|
|Ja| Als het artikel een of meer varianten heeft, moeten gebruikers de relevante variant opgeven. Als ze dat niet doen, kunnen ze de transactie niet boeken.|

> [!NOTE]
> Deze instellingen zijn niet van invloed op artikelen die geen varianten hebben.

Als de mogelijkheid is ingeschakeld, kunnen gebruikers geen invoer plaatsen als de variant niet is opgegeven.

## <a name="categories-attributes-and-variants"></a>Categorieën, kenmerken en varianten

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="see-also"></a>Zie ook

[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Algemene voorraadgegevens instellen](inventory-how-setup-general.md)  
[Procedure: varianten](contoso-coffee/manufacturing/variants.md)  
