---
title: Artikelkenmerken instellen en toewijzen aan artikelen| Microsoft Docs
description: "Beschrijft hoe u kenmerkwaarden instelt die bijvoorbeeld kunnen worden gebruikt als zoekwoorden, en deze toewijst aan artikelen en artikelcategorieën."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: categories, search words, facets
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2b29fed7bf976c896b3d663f526d9c3a96200100
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-item-attributes"></a>Werken met artikelkenmerken
Wanneer klanten informeren naar een artikel, via correspondentie of via een geïntegreerde webwinkel, kunnen ze ernaar vragen of zoeken op basis van kenmerken, zoals hoogte en model. Als u deze klantenservice wilt bieden, kunt u artikelkenmerkwaarden van verschillende typen aan uw artikelen toewijzen, die vervolgens kunnen worden gebruikt bij het zoeken naar artikelen.

U kunt ook artikelkenmerken aan artikelcategorieën toewijzen, die vervolgens worden toegepast op de artikelen die de artikelcategorieën gebruiken. Zie [Artikelen categoriseren](inventory-how-categorize-items.md) voor meer informatie.

> [!Tip]  
> Als u afbeeldingen aan artikelen koppelt, kan de extensie Afbeeldingsanalyse kenmerken in de afbeelding detecteren en de kenmerken voorstellen, zodat u kunt besluiten of u deze toewijst. De extensie is klaar. U hoeft deze alleen in te schakelen. Zie voor meer informatie [De extensie Afbeeldingsanalyse voor Microsoft Finance and Operations, Business edition](ui-extensions-image-analyzer.md).

## <a name="to-create-item-attributes"></a>Artikelkenmerken maken
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikelkenmerken** in en klik vervolgens op de gerelateerde koppeling.
2. Kies in het venster **Artikelkenmerken** de actie **Nieuw**.
3. Vul in het venster **Artikelkenmerk** indien nodig de velden in. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Als u **Optie** selecteert in het veld **Soort**, kunt u de actie **Artikelkenmerkwaarden** kiezen om waarden voor het artikelkenmerk te maken. Zie het gedeelte "Waarden voor artikelkenmerken van het soort Optie maken" voor meer informatie.  

## <a name="to-create-values-for-item-attributes-of-type-option"></a>Waarden voor artikelkenmerken van het soort Optie maken
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikelkenmerken** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer in het venster **Artikelkenmerken** een artikelkenmerk van het soort **Optie** waarvoor u waarden wilt maken, en kies vervolgens de actie **Artikelkenmerkwaarden**.
3. Vul in het venster **Artikelkenmerkwaarden** indien nodig de velden in. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-item-attributes-to-items"></a>Artikelkenmerken aan artikelen toewijzen
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikelen** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer in het venster **Artikelen** het artikel waaraan u kenmerkwaarden wilt toewijzen, en kies vervolgens de actie **Kenmerken**.
3. Kies in het venster **Artikelkenmerkwaarden** de actie **Nieuw**.
4. Kies de zoekknop in het veld **Kenmerk** en selecteer een bestaand artikelkenmerk. U kunt ook de actie **Nieuw** kiezen om eerst een nieuw artikelkenmerk te maken, zoals is uitgelegd in het gedeelte "Artikelkenmerken maken".
5. Voer in het veld **Waarde** de artikelkenmerkwaarde in, zoals "2010" voor het kenmerk **Modeljaar**.
6. Kies voor artikelkenmerken van het soort **Optie** de zoekknop in het veld **Waarde** en selecteer een artikelkenmerkwaarde. U kunt ook de actie **Nieuw** kiezen om eerst een nieuwe artikelkenmerkwaarde te maken, zoals is uitgelegd in het gedeelte "Waarden voor artikelkenmerken van het soort Optie maken".
7. Herhaal stap 4 tot en met 6 voor alle artikelkenmerken die u wilt toewijzen aan het artikel.

## <a name="to-assign-item-attributes-to-item-categories"></a>Artikelkenmerken aan artikelcategorieën toewijzen
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikelcategorieën** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer in het venster **Artikelcategorieën** de artikelcategorie waaraan u artikelkenmerken wilt toewijzen en kies vervolgens de actie **Bewerken**.
3. Kies in het venster **Artikelcategoriekaart** op het sneltabblad **Kenmerken** de actie **Nieuw**.
4. Kies de zoekknop in het veld **Kenmerk** en selecteer een bestaand artikelkenmerk. U kunt ook de actie **Nieuw** kiezen om eerst een nieuw artikelkenmerk te maken, zoals is uitgelegd in het gedeelte "Artikelkenmerken maken".
5. Kies in het veld **Standaardwaarde** de zoekknop en selecteer een artikelkenmerkwaarde.
6. Herhaal stap 4 en 5 voor alle artikelkenmerken die u wilt toewijzen aan de artikelcategorie.

> [!NOTE]  
>   Artikelkenmerken voor bovenliggende artikelcategorieën worden doorgegeven aan onderliggende artikelcategorieën. Dit wordt aangegeven door het veld **Overgenomen van** op het sneltabblad **Kenmerken**. Zie [Artikelen categoriseren](inventory-how-categorize-items.md) voor meer informatie.

## <a name="to-filter-by-item-attributes"></a>Filteren op artikelkenmerken
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikelen** in en klik vervolgens op de gerelateerde koppeling.
2. Kies in het venster **Artikelen** de actie **Filteren op kenmerken**.
3. Kies in het venster **Filteren op kenmerken** de opzoekknop in het veld **Kenmerk** en selecteer een bestaand artikelkenmerk.
4. Kies in het veld **Waarde** de zoekknop en selecteer een kenmerkwaarde om artikelen op te filteren.

    > [!NOTE]  
   >   U kunt alleen rechtstreeks waarden selecteren voor artikelkenmerken die vaste waarden hebben, zoals Kleur. Voor artikelkenmerken die variabele waarden hebben, zoals Breedte, moet u de artikelkenmerkwaarde opgeven door eerst een voorwaarde te selecteren. Zie stap 5.
5. Kies in het veld **Waarde** voor een variabel artikelkenmerk de zoekknop.
6. Kies in het venster **Filterwaarde opgeven**, in het veld **Voorwaarde** de vervolgkeuzepijl en selecteer een voorwaarde.
7. Voer in het veld **Waarde** een kenmerkwaarde in om artikelen op te filteren.

    **Voorbeeld:** als u wilt filteren op artikelen waarvan de materiaalomschrijving begint met "blauw", vult u de velden als volgt in: veld **Kenmerk**: Materiaalomschrijving, veld **Voorwaarde**: Begint met, veld **Waarde**: blauw.
8. Kies de knop **Ok**.   

De artikelen in de **Artikelen**-vensters worden gefilterd door de opgegeven artikelkenmerkwaarden.

## <a name="see-also"></a>Zie ook
[Artikelen categoriseren](inventory-how-categorize-items.md)    
[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

