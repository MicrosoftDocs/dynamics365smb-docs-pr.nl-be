---
title: Boekingsperioden afsluiten voor een boekjaar
description: In dit artikel wordt beschreven hoe u de boekhoudperioden afsluit die deel uitmaken van het boekjaar voor jaarafsluiting.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
ms.search.form: '100,'
ms.date: 05/07/2024
ms.service: dynamics-365-business-central
---
# <a name="close-accounting-periods"></a>Boekhoudperioden afsluiten

Wanneer een boekjaar is afgelopen, moet u de hierin opgenomen perioden afsluiten.

## <a name="to-close-accounting-periods"></a>Boekhoudperioden afsluiten

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Boekhoudperioden afsluiten** in en kies vervolgens de gerelateerde koppeling.
2. Kies op de pagina **Boekingsperioden** de actie **Jaar afsluiten**.

    Als er meerdere boekjaren zijn geopend, wordt het vroegste boekjaar automatisch geselecteerd om te worden afgesloten. Een bericht geeft aan welk jaar wordt afgesloten en welke gevolgen dit heeft.
3. Kies de knop **Ja** om het jaar af te sluiten.

Het boekjaar is nu afgesloten en de selectievakjes **Afgesloten** en **Geblokkeerd** zijn ingeschakeld voor alle perioden van het jaar. U kunt het boekjaar niet meer openen en de selectievakjes **Afgesloten** en **Geblokkeerd** niet uitschakelen.

> [!NOTE]  
> U kunt een boekjaar niet afsluiten voordat u een nieuw boekjaar hebt gemaakt. Nadat een boekjaar is afgesloten, kunt u de begindatum van het volgende boekjaar niet meer wijzigen.

Zelfs als een boekjaar is afgesloten, kunt u er nog steeds grootboekposten naar boeken. Als u dit doet, worden de posten gemarkeerd als zijnde geboekt naar een afgesloten boekjaar en wordt het veld **Naboeking** geselecteerd.

Nadat een boekjaar is afgesloten, moet u de resultaten- of winst- en verliesrekeningen afsluiten en de jaarresultaten naar een balansrekening overbrengen. U kunt deze procedure herhalen telkens wanneer u boekt naar een afgesloten boekjaar.

## <a name="see-also"></a>Zie ook

[Boeken afsluiten](year-close-books.md)  
[De jaareinde-ultimopost boeken](year-how-post-year-end-close-entry.md)  
[Werken met boekingsperioden en fiscale jaren](finance-accounting-periods-and-fiscal-years.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
