---
title: Adhoc-analyse van voorraadgegevens
description: Leer hoe u de gegevensanalysemodus gebruikt om voorraadgegevens te analyseren.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/03/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analysis-of-inventory-data"></a>Adhoc-analyse van voorraadgegevens

In dit artikel leert u hoe u de functie **Gegevensanalyse** gebruikt om voorraadgegevens te analyseren direct vanaf lijstpagina's en query's. U hoeft geen rapport uit te voeren of over te stappen naar een andere toepassing, zoals Excel. De functie biedt een interactieve en veelzijdige manier om gegevens te berekenen, samen te vatten en te onderzoeken. In plaats van rapporten uit te voeren met opties en filters, kunt u meerdere tabbladen toevoegen die verschillende taken of weergaven van de gegevens vertegenwoordigen. Enkele voorbeelden zijn 'verlopende voorraad' of 'topverkopers', of elke andere weergave die u maar kunt bedenken. Voor meer informatie over het gebruik van de functie **Gegevensanalyse** gaat u naar [Lijst- en querygegevens analyseren met de analysemodus](analysis-mode.md).

Gebruik de volgende lijstpagina's voor ad-hocanalyse van voorraadprocessen:

- [Artikelposten](https://businesscentral.dynamics.com/?page=38)

## <a name="inventory-ad-hoc-analysis-scenarios"></a>Ad-hocanalysescenario's voor voorraad

Gebruik de functie **Gegevensanalyse** voor snelle feitencontrole en ad-hocanalyse:

- Als u geen rapport wilt uitvoeren.
- Als er geen rapport voor uw specifieke behoefte bestaat.
- Als u snel wilt herhalen om een goed overzicht te krijgen van een deel van uw bedrijf.

In de volgende secties vindt u voorbeelden van voorraadscenario's in [!INCLUDE [prod_short](includes/prod_short.md)].

| Vlak | Actie | Deze pagina openen in de analysemodus | Deze velden gebruiken |
| ---- | ----- | ------------------------------- |------------------- |
| [Voorhanden voorraad](#example-inventory-on-hand) | Krijg een overzicht van artikelen die beschikbaar zijn in uw voorraad. | [Artikelposten](https://businesscentral.dynamics.com/?page=38) | **Artikelnr.**, **Resterend aantal** |
|[Voorbeeld: verlopende of oude voorraad volgen](#example-track-expiring-or-old-stock) | Krijg een overzicht van artikelen in uw voorraad die al langere tijd op voorraad zijn en niet goed verkopen. | [Artikelposten](https://businesscentral.dynamics.com/?page=38) | **Boekingsdatum (jaar)**, **Boekingsdatum (maand)**, **Artikelnr.**, **Boekingsdatum**, **Boekingssoort**, **Hoeveelheid** en **Resterend aantal**. |
| [Geretourneerde artikelen op retourreden](#example-returned-items-by-return-reason) | Krijg een overzicht van goederen die klanten retourneren, gecategoriseerd op retourreden. Gebruik dit voor analyse voor kwaliteitscontrole. | [Artikelposten](https://businesscentral.dynamics.com/?page=38) | **Retourreden**, **Boekingsdatum (maand)**, **Hoeveelheid**, **Kostenbedrag**, **Boekingsdatum**, **Documentsoort**, **Artikelnr.** en **Documentnr.** |
| Voorraaddoorvoer | Krijg een overzicht van aankopen en verkopen in uw voorraad per maand of kwartaal. | [Artikelposten](https://businesscentral.dynamics.com/?page=38) | **Boekingsdatum (jaar)**, **Boekingsdatum (maand)**, **Artikelnr.**, **Aantal**, **Verkoopbedrag**, **Kostenbedrag (werkelijk)** en **Boekingsdatum (maand)** |
| [Voorraadverplaatsingen] | Krijg een overzicht van hoe goederen in uw voorraad zich tussen vestigingen verplaatsen. | [Artikelposten](https://businesscentral.dynamics.com/?page=38) | **Vestigingscode**, **Aantal**, **Boekingsdatum**, **Artikelnr.** |

## <a name="example-inventory-on-hand"></a>Voorbeeld: voorhanden voorraad

Volg deze stappen om artikelen in uw voorraad die op voorraad zijn te analyseren:

1. Open de lijst [Klantenposten](https://businesscentral.dynamics.com/?page=38) en kies :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus openen."::: om de analysemodus in te schakelen.
1. Ga naar het menu **Kolommen** en verwijder alle kolommen (selecteer het vakje naast het veld **Zoeken**).
1. Sleep het veld **Artikelnr.** naar het gebied **Rijgroepen**. Sleep de velden in die volgorde.
1. Sleep het veld **Resterend aantal** naar het gebied **Waarden**.
1. Stel een **Niet gelijk**-filter op **0** op **Resterend aantal**. Als u geen negatieve voorraadniveaus toestaat, stelt u een **Groter dan**-filter in op **0**.
1. Voeg optioneel andere velden toe aan de analyse en draai eventueel op vestiging of andere velden.
1. Hernoem uw analysetabblad naar **Voorhanden voorraad** of iets dat deze analyse voor u beschrijft.

De volgende afbeelding toont het resultaat van deze stappen.

:::image type="content" source="media/data-analysis-inventory-on-hand.png" alt-text="Voorbeeld van hoe u een analyse van beschikbare voorraadgegevens uitvoert." lightbox="media/data-analysis-inventory-on-hand.png":::

## <a name="example-track-expiring-or-old-stock"></a>Voorbeeld: verlopende of oude voorraad volgen

Als u artikelen in uw voorraad wilt analyseren die al langere tijd op voorraad zijn en niet goed verkopen, voert u deze stappen uit:

1. Open de lijst [Klantenposten](https://businesscentral.dynamics.com/?page=38) en kies :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus openen."::: om de analysemodus in te schakelen.
1. Ga naar het menu **Kolommen** en verwijder alle kolommen (selecteer het vakje naast het veld **Zoeken**, rechts).
1. Sleep de velden **Boekingsdatum (jaar)**, **Boekingsdatum (maand)** en **Artikelnr.** naar het gebied **Rijgroepen**. Sleep de velden in die volgorde.
1. Kies in het gebied **Kolommen** de velden **Boekingsdatum**, **Boekingssoort**, **Hoeveelheid** en **Resterend aantal**.
1. Stel een **Kleiner dan**-filter in op **Boekingsdatum** om te definiëren wat u bedoelt met 'oud'.
1. Hernoem uw analysetabblad naar **Oude voorraad** of iets dat deze analyse voor u beschrijft.

De volgende afbeelding toont het resultaat van deze stappen.

:::image type="content" source="media/data-analysis-inventory-dead-stock.png" alt-text="Voorbeeld van hoe u gegevensanalyse van dode voorraad uitvoert op de pagina Artikelposten." lightbox="media/data-analysis-inventory-dead-stock.png":::

## <a name="example-returned-items-by-return-reason"></a>Voorbeeld: geretourneerde artikelen op retourreden

Volg deze stappen om geretourneerde artikelen te analyseren, gesorteerd op de redenen voor hun retourzending:

1. Open de lijst [Artikelposten](https://businesscentral.dynamics.com/?page=38).
1. Voeg het veld **Retourreden** toe door de pagina te personaliseren. Kies in het menu **Instellingen** **Personaliseren**.
1. Verlaat de personalisatiemodus.
1. Kies :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus openen."::: om de analysemodus in te schakelen.
1. Ga naar het menu **Kolommen** en verwijder alle kolommen (selecteer het vakje naast het veld **Zoeken**, rechts).
1. Sleep de velden **Retourreden** en **Boekingsdatum (maand)** naar het gebied **Rijgroepen**. Sleep de velden in die volgorde.
1. Sleep de velden **Hoeveelheid** en **Kostenbedrag** naar het gebied **Waarden**.
1. Voeg eventueel andere velden toe die u in de analyse wilt opnemen en schakel deze in het gebied **Kolommen** in. U kunt bijvoorbeeld de velden **Boekingsdatum**, **Documentsoort**, **Artikelnr.** en **Documentnr.** toevoegen.
1. Hernoem uw analysetabblad naar **Geretourneerde artikelen op retourreden** of iets dat deze analyse voor u beschrijft.  

## <a name="example-inventory-throughput"></a>Voorbeeld: voorraaddoorvoer

1. Open de lijst [Klantenposten](https://businesscentral.dynamics.com/?page=38) en kies :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus openen."::: om de analysemodus in te schakelen.
1. Ga naar het menu **Kolommen** en verwijder alle kolommen (selecteer het vakje naast het veld **Zoeken**, rechts).
1. Schakel de schakelaar **Draaimodus** in (bevindt zich boven het veld **Zoeken**, rechts).
1. Sleep de velden **Boekingsdatum (jaar)**, **Boekingsdatum (maand)** en **Artikelnr.** naar het gebied **Rijgroepen**.
1. Sleep de velden **Hoeveelheid**, **Verkoopbedrag** en **Kostenbedrag (werkelijk)** naar het gebied **Waarden**.
1. Sleep het veld **Boekingsdatum (maand)** naar het gebied **Kolomgroepen**.
1. Hernoem uw analysetabblad naar **Voorraaddoorvoer per maand** of iets dat deze analyse voor u beschrijft.  

## <a name="inventory-movements"></a>Voorraadverplaatsingen

Volg deze stappen om voorraadverplaatsingen tussen vestigingen bij te houden:

1. Open de lijst [Klantenposten](https://businesscentral.dynamics.com/?page=38) en kies :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus openen."::: om de analysemodus in te schakelen.
1. Ga naar het menu **Kolommen** en verwijder alle kolommen (selecteer het vakje naast het veld **Zoeken**, rechts).
1. Sleep het veld **Vestigingscode** naar het gebied **Rijgroepen**.
1. Sleep het veld **Aantal** naar het gebied **Waarden**.
1. Voeg eventueel andere velden toe die u in de analyse wilt opnemen en schakel deze in het gebied **Kolommen** in. U kunt bijvoorbeeld het veld **Artikelnr.** toevoegen.
1. Hernoem uw analysetabblad naar **Voorraadverplaatsingen** of iets dat deze analyse voor u beschrijft.  

   > [!TIP]
   > Als u het veld Boekingsdatum toevoegt, kunt u ook verplaatsingen in de loop van de tijd volgen.

## <a name="data-foundation-for-ad-hoc-analysis-on-inventory"></a>Gegevensbasis voor ad-hocanalyse van voorraad

Wanneer u een verkooporder boekt, werkt [!INCLUDE [prod_short](includes/prod_short.md)] de rekening van de klant, het grootboek en de artikelposten bij.

- Voor elke verkooporderregel wordt een artikelpost gemaakt in de tabel **Artikelpost** (als de verkoopregels artikelnummers bevatten). Daarnaast worden verkooporders altijd geregistreerd in de tabellen **Verkoopverzendkop** en **Verkoopfactuurkop**. Ga voor meer informatie over direct verkopen naar [Verkopen boeken](ui-post-sales.md).

Wanneer u een inkoopdocument boekt, werkt [!INCLUDE [prod_short](includes/prod_short.md)] de rekening van de leverancier, het grootboek, de artikelposten en de resourceposten bij.

- Voor elke inkoopregel worden, indien van toepassing, posten gemaakt in de tabel **Artikelpost** (als de inkoopregel van het type Artikel is). Daarnaast worden inkoopdocumenten altijd vastgelegd in de tabellen **Inkoopontvangst** en **Inkoopfactuur**. Ga voor meer informatie naar [Inkopen boeken](purchasing-how-record-purchases.md#posting-purchases).

## <a name="see-also"></a>Zie ook

[Lijst- en querygegevens analyseren met de analysemodus](analysis-mode.md)  
[Overzicht van voorraadanalyse](inventory-analytics-overview.md)  
[Overzicht van analyses, bedrijfsinformatie en rapportage](reports-bi-reporting.md)  
[Overzicht van voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
