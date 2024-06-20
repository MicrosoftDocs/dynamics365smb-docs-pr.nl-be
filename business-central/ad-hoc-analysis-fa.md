---
title: Adhoc-analyse van vaste-activagegevens
description: Leer hoe u de gegevensanalysemodus gebruikt om gegevens te analyseren van vaste activa.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '5604, 20'
ms.date: 05/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analysis-of-fixed-assets-data"></a>Adhoc-analyse van vaste-activagegevens

In dit artikel leert u hoe u de functie **Gegevensanalyse** gebruikt om vaste-activagegevens te analyseren direct vanaf lijstpagina's en query's. U hoeft geen rapport uit te voeren of over te stappen naar een andere toepassing, zoals Excel. De functie biedt een interactieve en veelzijdige manier om gegevens te berekenen, samen te vatten en te onderzoeken. In plaats van rapporten uit te voeren met opties en filters, kunt u meerdere tabbladen toevoegen die verschillende taken of weergaven van de gegevens vertegenwoordigen. Enkele voorbeelden zijn 'Totale activa', 'Afschrijvingen in de loop van de tijd' of welke andere weergave dan ook die u maar kunt bedenken. Voor meer informatie over het gebruik van de functie **Gegevensanalyse** gaat u naar [Lijst- en querygegevens analyseren met de analysemodus](analysis-mode.md).

Gebruik de volgende lijstpagina's om te beginnen met ad-hocanalyse van vaste-activaprocessen:

- [VA-posten](https://businesscentral.dynamics.com/?page=5604)
- [Grootboekposten](https://businesscentral.dynamics.com/?page=20)

## <a name="fixed-assets-ad-hoc-analysis-scenarios"></a>Scenario's voor adhoc-analyse van vaste-activa

Gebruik de functie **Gegevensanalyse** voor snelle feitencontrole en ad-hocanalyse:

- Als u geen rapport wilt uitvoeren.
- Als er geen rapport voor uw specifieke behoefte bestaat.
- Als u snel wilt herhalen om een goed overzicht te krijgen van een deel van uw bedrijf.

In de volgende secties vindt u voorbeelden van vaste-activascenario's in [!INCLUDE [prod_short](includes/prod_short.md)].

| Vlak | Actie | Deze pagina openen in de analysemodus | Deze velden gebruiken |
| ---- | ----- | ------------------------------- |------------------- |
| [Vaste activa (huidige waarde)](#example-fixed-assets-current-value) | Volg activawaarde, zowel voor alle activa als voor één enkel activum. | [VA-posten](https://businesscentral.dynamics.com/?page=5604) | **Afschrijvingsboek**, **VA-nr.**, **VA-boekingsdatum**, **VA-boekingssoort** en **Bedrag** |
| [De waarde van activa verandert in de loop van de tijd](#example-asset-value-changes-over-time) | Wijzigingen in de waarde van activa bijhouden in de loop van de tijd. | [VA-posten](https://businesscentral.dynamics.com/?page=5604) | Kies de velden **VA-boekingssoort**, **VA-boekingsdatum** en **Bedrag** |
|[Afschrijvingen op vaste activa in de loop van de tijd](#example-fixed-asset-depreciations-over-time) | Volg afschrijvingen in de loop van de tijd, zowel voor alle activa als voor één enkel activum. | [VA-posten](https://businesscentral.dynamics.com/?page=5604) | **Afschrijvingsboek**, **VA-nr.**, **VA-boekingsjaar**, **VA-boekingsmaand**, en **Bedrag** en **VA-boekingssoort** |

### <a name="example-fixed-assets-current-value"></a>Voorbeeld: vaste activa (huidige waarde)

Volg deze stappen om de waarde van een of meer vaste activa bij te houden:

1. Open de lijst [VA-posten](https://businesscentral.dynamics.com/?page=5604) en kies :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus openen."::: om de analysemodus in te schakelen.
1. Ga naar het menu **Kolommen** en verwijder alle kolommen (selecteer het vakje naast het veld **Zoeken**, rechts).
1. Sleep de velden **Afschrijvingsboek** en **VA-nr.** naar het gebied **Rijgroepen**.
1. Kies de velden **VA-boekingsdatum** en **VA-boekingssoort**.
1. Sleep het veld **Bedrag** naar het gebied **Waarden**.
1. Hernoem uw analysetabblad naar **Activaoverzicht - waarde** of iets dat deze analyse voor u beschrijft.

De volgende afbeelding toont het resultaat van deze stappen.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png" alt-text="Voorbeeld van hoe u gegevensanalyse uitvoert op de pagina VA-posten om de waarde van een activum te bekijken." lightbox="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png":::

### <a name="example-asset-value-changes-over-time"></a>Voorbeeld wijzigingen in de waarde van activa in de loop van de tijd

Volg deze stappen om veranderingen in de waarde van activa in de loop van de tijd bij te houden:

1. Open de lijst [VA-posten](https://businesscentral.dynamics.com/?page=5604) en kies :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus openen."::: om de analysemodus in te schakelen.
1. Ga naar het menu **Kolommen** en verwijder alle kolommen (selecteer het vakje naast het veld **Zoeken**, rechts).
1. Schakel de schakelaar **Draaimodus** in (bevindt zich boven het veld **Zoeken**, rechts).
1. Sleep het veld **VA-boekingssoort** naar het gebied **Rijgroepen**.
1. Sleep de velden **VA-boekingsjaar** en **VA-boekingsmaand** naar het gebied **Kolomlabels**.
1. Sleep het veld **Bedrag** naar het gebied **Waarden**.
1. Hernoem uw analysetabblad naar **De waarde van activa verandert in de loop van de tijd** of iets dat deze analyse voor u beschrijft.

De volgende afbeelding toont het resultaat van deze stappen.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-changes-over-time.png" alt-text="Voorbeeld van hoe u gegevensanalyse uitvoert op de pagina VA-posten om wijzigingen van activawaarden in de loop van de tijd te bekijken." lightbox="media/data-analysis-fa-ledger-entries-asset-changes-over-time.png":::

### <a name="example-fixed-asset-depreciations-over-time"></a>Voorbeeld: afschrijvingen op vaste activa in de loop van de tijd

Volg deze stappen om de afschrijving van een of meer vaste activa bij te houden:

1. Open de lijst [VA-posten](https://businesscentral.dynamics.com/?page=5604) en kies :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus openen."::: om de analysemodus in te schakelen.
1. Ga naar het menu **Kolommen** en verwijder alle kolommen (selecteer het vakje naast het veld **Zoeken**, rechts).
1. Schakel de schakelaar **Draaimodus** in (bevindt zich boven het veld **Zoeken**, rechts).
1. Sleep de velden **Afschrijvingsboek** en **VA-nr.** naar het gebied **Rijgroepen**.
1. Sleep de velden **VA-boekingsjaar** en **VA-boekingsmaand** naar het gebied **Kolomlabels**.
1. Sleep het veld **Bedrag** naar het gebied **Waarden**.
1. Kies in het veld **VA-boekingssoort** **Afschrijving**.
1. Hernoem uw analysetabblad naar **Afschrijvingen in de loop van de tijd** of iets dat deze analyse voor u beschrijft.

De volgende afbeelding toont het resultaat van deze stappen.

:::image type="content" source="media/data-analysis-fa-ledger-entries-depreciation-by-asset.png" alt-text="Voorbeeld van hoe u gegevensanalyse uitvoert op de pagina VA-posten om afschrijving in de loop van de tijd te bekijken." lightbox="media/data-analysis-fa-ledger-entries-depreciation-by-asset.png":::

## <a name="data-foundation-for-ad-hoc-analysis-on-fixed-assets"></a>Gegevensbasis voor ad-hocanalyse van vaste activa

Wanneer u vaste activa boekt, [!INCLUDE [prod_short](includes/prod_short.md)] worden er posten gemaakt in de tabel **VA-post**. Daarom wordt een ad-hocanalyse van vaste activa doorgaans uitgevoerd op de pagina [VA-posten](https://businesscentral.dynamics.com/?page=5604).

## <a name="contributors"></a>Bijdragers

*Microsoft handhaaft dit artikel. Delen van de voorbeelden zijn oorspronkelijk geschreven door de volgende bijdrager.*

* [Aldona Stec](https://www.linkedin.com/in/aldona-stec-25283bb1) | [!INCLUDE[prod_short](includes/prod_short.md)] Consulent

## <a name="see-also"></a>Zie ook

[Lijst- en querygegevens analyseren met de analysemodus](analysis-mode.md)  
[Overzicht van analyses van vaste activa](fa-analytics-overview.md)  
[Overzicht van analyses, bedrijfsinformatie en rapportage](reports-bi-reporting.md)  
[Overzicht van vaste activa](fa-manage.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
