---
title: Adhoc-analyse van financiële gegevens
description: Leer hoe u de gegevensanalysemodus gebruikt om financiële gegevens te analyseren.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analysis-of-finance-data"></a>Adhoc-analyse van financiële gegevens

In dit artikel leert u hoe u de functie **Gegevensanalyse** gebruikt om financiële gegevens te analyseren direct vanaf lijstpagina's en query's. U hoeft geen rapport uit te voeren of over te stappen naar een andere toepassing, zoals Excel. De functie biedt een interactieve en veelzijdige manier om gegevens te berekenen, samen te vatten en te onderzoeken. In plaats van rapporten uit te voeren met opties en filters, kunt u meerdere tabbladen toevoegen die verschillende taken of weergaven van de gegevens vertegenwoordigen. Enkele voorbeelden zijn 'Totale activa in de loop van de tijd', 'Debiteuren', 'Crediteuren' of welke andere weergave dan ook die u maar kunt bedenken. Voor meer informatie over het gebruik van de functie **Gegevensanalyse** gaat u naar [Lijst- en querygegevens analyseren met de analysemodus](analysis-mode.md).

Gebruik de volgende lijstpagina's om te beginnen met ad-hocanalyse van financiële processen:

- [Grootboekposten](https://businesscentral.dynamics.com/?page=20)
- [Klantenposten](https://businesscentral.dynamics.com/?page=25)
- [Leveranciersposten](https://businesscentral.dynamics.com/?page=29)

## <a name="ad-hoc-analysis-scenarios-in-finance"></a>Ad-hocanalysescenario's in de financiële wereld

Gebruik de functie **Gegevensanalyse** voor snelle feitencontrole en ad-hocanalyse:

- Als u geen rapport wilt uitvoeren.
- Als er geen rapport voor uw specifieke behoefte bestaat.
- Als u snel wilt herhalen om een goed overzicht te krijgen van een deel van uw bedrijf.

In de volgende secties vindt u voorbeelden van financiële scenario's in [!INCLUDE [prod_short](includes/prod_short.md)].

| Vlak | Actie | Deze pagina openen in de analysemodus | Deze velden gebruiken |
| ---- | ----- | ------------------------------- |------------------- |
|[Voorbeeld: Financiën (debiteuren)](#example-finance-accounts-receivable) | Bekijk bijvoorbeeld wat uw klanten u verschuldigd zijn, uitgesplitst in tijdsintervallen voor wanneer bedragen moeten worden betaald. | [Klantenposten](https://businesscentral.dynamics.com/?page=25) | **Klantnaam**, **Deadline** en **Resterend bedrag** |
| [Financiën (crediteuren)](#example-finance-accounts-payable) | Bekijk wat u uw leveranciers verschuldigd bent, uitgesplitst in tijdsintervallen voor wanneer bedragen moeten worden betaald. | [Leveranciersposten](https://businesscentral.dynamics.com/?page=29) | **Leveranciersnaam**, **Documentsoort**, **Documentnr.**, **Vervaldatum (jaar)**, **Vervaldatum (maand)** en **Resterend bedrag**. |
| [Financiën (verkoopfacturen per grootboekrekening)](#example-finance-sales-invoices-by-gl-account) | Bekijk vanuit het rekeningschema hoe uw verkoopfacturen over de grootboekrekeningen worden verdeeld, bijvoorbeeld opgesplitst in tijdsintervallen voor het moment waarop bedragen zijn geboekt. | [Grootboekposten](https://businesscentral.dynamics.com/?page=20) | **Naam grootboekrekening**, **Broncode**, **Naam grootboekrekening**,  **G/L-rekeningnr.**, **Debetbedrag**, **Creditbedrag**, **Postdatum Jaar**, **Postdatum Kwartaal** en **Posting Datum Maand** |
| [Financiën (Resultatenrekening)](#example-finance-income-statement) | Bekijk uw inkomsten over de inkomstenrekeningen uit het rekeningschema, bijvoorbeeld opgesplitst in tijdsintervallen voor wanneer bedragen zijn geboekt. | [Grootboekposten](https://businesscentral.dynamics.com/?page=20) | **Grootboekrekeningnr.**, **Boekingsdatum** en **Bedrag**. |
| [Financiën (totale activa)](#example-finance-total-assets) | Bekijk uw activa over de activarekeningen uit het rekeningschema, bijvoorbeeld opgesplitst in tijdsintervallen voor wanneer bedragen zijn geboekt. | [Grootboekposten](https://businesscentral.dynamics.com/?page=20) | **Grootboekrekeningnr.**, **Boekingsdatum** en **Bedrag**. |

### <a name="example-finance-accounts-receivable"></a>Voorbeeld: Financiën (debiteuren)

Als u wilt zien wat uw klanten u verschuldigd zijn, wellicht uitgesplitst in tijdsintervallen voor wanneer bedragen moeten worden betaald, doet u het volgende:

1. Open de lijst [Klantenposten](https://businesscentral.dynamics.com/?page=25) en kies :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus openen"::: om de analysemodus in te schakelen.
1. Ga naar het menu **Kolommen** en verwijder alle kolommen (selecteer het vakje naast het veld *Zoeken*, rechts).
1. Schakel de schakelaar **Draai*modus** in (bevindt zich boven het veld **Zoeken**, rechts).
1. Sleep het veld **Klantnaam** naar het gebied **Rijgroepen** en sleep **Resterend bedrag** naar het gebied **Waarden**.
1. Sleep het veld **Vervaldatum (maand)** naar het gebied **Kolomlabels**.
1. Als u de analyse wilt uitvoeren voor een bepaald jaar of kwartaal, past u een filter toe in het menu **Analysefilters** (aan de rechterkant onder het menu **Kolommen**).
1. Hernoem uw analysetabblad naar **Oudere accounts per maand** of iets dat deze analyse beschrijft.

### <a name="example-finance-accounts-payable"></a>Voorbeeld: Financiën (Schulden)

Als u wilt zien wat u uw leveranciers verschuldigd bent, wellicht uitgesplitst in tijdsintervallen voor wanneer bedragen moeten worden betaald, doet u het volgende:

1. Open de lijstpagina [Leveranciersposten](https://businesscentral.dynamics.com/?page=29) en kies :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus openen":::. om de analysemodus in te schakelen.
1. Ga naar het menu **Kolommen** en verwijder alle kolommen (selecteer het vakje naast het veld **Zoeken**).
1. Schakel de schakelaar **Draaimodus** in (bevindt zich boven het veld **Zoeken**, rechts).
1. Sleep de velden **Leveranciersnaam**, **Documentsoort** en **Documentnummer** naar het gebied **Rijgroepen** en sleep vervolgens het veld **Resterend bedrag** naar het gebied **Waarden**.
1. Sleep de velden **Vervaldatum (jaar)** en **Vervaldatum (maand)** naar het gebied **Kolomlabels**. Sleep de velden in die volgorde.
1. Als u de analyse wilt uitvoeren voor een bepaald jaar of kwartaal, past u een filter toe in het menu **Analysefilters** (aan de rechterkant onder het menu **Kolommen**).
1. Hernoem uw analysetabblad naar **Oudere accounts per maand** of iets dat deze analyse beschrijft.

De volgende afbeelding toont het resultaat van deze stappen.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Voorbeeld van hoe u gegevensanalyse uitvoert op de pagina Klantenposten." lightbox="media/data-analysis-vendor-ledger-entries.png":::

### <a name="example-finance-sales-invoices-by-gl-account"></a>Voorbeeld: Financiën (verkoopfacturen per grootboekrekening)

Om te zien hoe uw verkoopfacturen vanuit het rekeningschema over de grootboekrekeningen worden verdeeld, bijvoorbeeld uitgesplitst in tijdsintervallen voor het moment waarop bedragen zijn geboekt, volgt u deze stappen:

1. Open de pagina  [grootboekposten](https://businesscentral.dynamics.com/?page=20) .
1. Voeg de velden  **G/L Account Name** en **Broncode**  toe door de pagina te personaliseren. Kies in het menu **Instellingen** **Personaliseren**.
1. Verlaat de personalisatiemodus.
1. Kies :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus openen."::: om de analysemodus in te schakelen.
1. Stel in het menu  **Analysefilters**  een filter in het veld  **Broncode**  in op **VERKOOP**. Als u aanpassingen heeft die andere waarden toevoegen, kunt u deze ook toevoegen.
1. Verwijder in naar het menu **Kolommen** alle kolommen (selecteer het vakje naast het veld **Zoeken**).
1. Schakel de schakelaar **Draaimodus** in (bevindt zich boven het veld **Zoeken**, rechts).
1. Sleep de velden  **G/L-rekeningnaam** en **G/L-rekeningnummer** naar de **Rijgroepen** gebied.
1. Sleep de velden  **Debetbedrag** en **Creditbedrag** naar de **Waarden** gebied.
1. Versleep de  **Postdatum Jaar**, **Postdatum Kwartaal** en **Postdatum Maand** velden naar het gebied  **Kolomlabels** .
1. Hernoem het tabblad Analyse naar **Factuurspecificatie per account**, of iets dat deze analyse beschrijft.

De volgende afbeelding toont het resultaat van deze stappen.

:::image type="content" source="media/data-analysis-gl-entries-invoices.png" alt-text="Voorbeeld van hoe u gegevensanalyse uitvoert op de pagina grootboekposten (om verkoopboekingen te begrijpen)." lightbox="media/data-analysis-gl-entries-invoices.png":::

### <a name="example-finance-income-statement"></a>Voorbeeld: Financiën (Resultatenrekening)

Als u uw inkomsten wilt zien over de inkomstenrekeningen uit het rekeningschema, opgesplitst in tijdsintervallen voor wanneer bedragen zijn geboekt, volgt u deze stappen:

1. Open de lijst [Grootboekposten](https://businesscentral.dynamics.com/?page=20) en kies :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus openen."::: om de analysemodus in te schakelen.
1. Ga naar het menu **Kolommen** en verwijder alle kolommen (selecteer het vakje naast het veld **Zoeken**, rechts).
1. Schakel de schakelaar **Draaimodus** in (bevindt zich boven het veld **Zoeken**, rechts).
1. Sleep het veld **Grootboekrekeningnr.** naar het gebied **Rijgroepen** en sleep **Bedrag** naar het gebied **Waarden**.
1. Sleep het veld **Boekingsdatum (maand)** naar het gebied **Kolomlabels** .
1. Voor de resultatenrekening filtert u op de rekeningen die u gebruikt. In de [!INCLUDE [prod_short](includes/prod_short.md)]-demogegevens beginnen deze accounts met '4', maar uw rekeningschema kan afwijken. Stel een filter in voor de rekeningen in het menu **Analysefilters** (aan de rechterkant, onder het menu **Kolommen**).

   > [!TIP]
   > Als u wilt zien welke rekeningen worden gebruikt in uw instelling, voert u het rapport [Proefsaldo per periode](https://businesscentral.dynamics.com/?report=38) uit.

1. Hernoem uw analysetabblad naar **Inkomen per maand** of iets dat deze analyse voor u beschrijft.

### <a name="example-finance-total-assets"></a>Voorbeeld: Financiën (totale activa)

Als u uw activa wilt zien over de activarekeningen uit het rekeningschema, opgesplitst in tijdsintervallen voor wanneer bedragen zijn geboekt, doet u het volgende:

1. Open de lijst [Grootboekposten](https://businesscentral.dynamics.com/?page=20) en kies :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus openen."::: om de analysemodus in te schakelen.
1. Ga naar het menu **Kolommen** en verwijder alle kolommen (selecteer het vakje naast het veld **Zoeken**, rechts).
1. Schakel de schakelaar **Draaimodus** in (bevindt zich boven het veld **Zoeken**, rechts).
1. Sleep het veld **Grootboekrekeningnr.** naar het gebied **Rijgroepen** en sleep **Bedrag** naar het gebied **Waarden**.
1. Sleep het veld **Boekingsdatum (maand)** naar het gebied **Kolomlabels** .
1. Voor het overzicht van totale activa filtert u op de rekeningen die u gebruikt. In de [!INCLUDE [prod_short](includes/prod_short.md)]-demogegevens beginnen deze accounts met '10', maar uw rekeningschema kan afwijken. Stel een filter in voor de juiste rekeningen in het menu **Extra filters** (aan de rechterkant, onder het menu **Kolommen**).

   > [!TIP]
   > Als u wilt zien welke rekeningen worden gebruikt in uw instelling, voert u het rapport [Proefsaldo per periode](https://businesscentral.dynamics.com/?report=38) uit.

1. Hernoem uw analysetabblad naar **Inkomen per maand** of iets dat deze analyse voor u beschrijft.

## <a name="data-foundation-for-ad-hoc-analysis-on-finance"></a>Gegevensbasis voor ad-hocanalyse van financiën

Wanneer u dagboeken boekt, [!INCLUDE [prod_short](includes/prod_short.md)] worden er posten gemaakt in de tabel **Grootboekpost**. Daarom wordt een ad-hocanalyse van algemene financiën doorgaans uitgevoerd op de pagina [Grootboekposten](https://businesscentral.dynamics.com/?page=20). Voor debiteuren- en crediteuren kunt u respectievelijk [Klantenposten](https://businesscentral.dynamics.com/?page=25) en [Leveranciersposten](https://businesscentral.dynamics.com/?page=29) analyseren.

Ga voor meer informatie naar de volgende artikelen:

- [Gegevensbasis voor ad-hocanalyse van verkopen](ad-hoc-analysis-sales.md#data-foundation-for-ad-hoc-analysis-on-sales)
- [Gegevensbasis voor ad-hocanalyse van inkopen](ad-hoc-analysis-purchasing.md#data-foundation-for-ad-hoc-analysis-on-purchasing)

## <a name="see-also"></a>Zie ook

[Lijst- en querygegevens analyseren met de analysemodus](analysis-mode.md)  
[Overzicht van financiële analyse](bi.md)  
[Overzicht van analyses, bedrijfsinformatie en rapportage](reports-bi-reporting.md)  
[Overzicht van financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
