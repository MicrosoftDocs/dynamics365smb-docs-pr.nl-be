---
title: Adhoc-analyse van duurzaamheidsgegevens
description: Leer hoe u de gegevensanalysemodus gebruikt om duurzaamheidsgegevens te analyseren.
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI, sustainability, ESG'
ms.search.form: '6220,'
ms.date: 06/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Adhoc-analyse van duurzaamheidsgegevens

In dit artikel leert u hoe u de functie **Gegevensanalyse** gebruikt om duurzaamheidsgegevens te analyseren direct vanaf lijstpagina's en query's. U hoeft geen rapport uit te voeren of over te stappen naar een andere toepassing, zoals Excel. De functie biedt een interactieve en veelzijdige manier om gegevens te berekenen, samen te vatten en te onderzoeken. In plaats van rapporten uit te voeren met opties en filters, kunt u meerdere tabbladen toevoegen die verschillende taken of weergaven van de gegevens vertegenwoordigen. Enkele voorbeelden zijn 'Uitstootoverzicht' of 'Uitstoot per bereik' of elke andere weergave die u maar kunt bedenken. Voor meer informatie over het gebruik van de functie **Gegevensanalyse** gaat u naar [Lijst- en querygegevens analyseren met de analysemodus](analysis-mode.md).

Gebruik de volgende lijstpagina's voor ad-hocanalyse van duurzaamheidsgegevens:

- [Duurzaamheidsposten](https://businesscentral.dynamics.com/?page=6220)

## Ad-hoc analysescenario's voor duurzaamheid

Gebruik de functie **Gegevensanalyse** voor snelle feitencontrole en ad-hocanalyse:

- Als u geen rapport wilt uitvoeren.
- Als er geen rapport voor uw specifieke behoefte bestaat.
- Als u snel wilt herhalen om een goed overzicht te krijgen van een deel van uw bedrijf.

In de volgende secties vindt u voorbeelden van duurzaamheidsscenario's in [!INCLUDE [prod_short](includes/prod_short.md)].

| Vlak | Actie | Deze pagina openen in de analysemodus | Deze velden gebruiken |
| ---- | ----- | ------------------------------- |------------------- |
| [Uitstootoverzicht (som per categorie)](#example-emission-overview-sum-by-category) | Analyseer uw uitstoot per categorie. | [Duurzaamheidsposten](https://businesscentral.dynamics.com/?page=6220) | **Accountcategorie**, **Accountnaam**, **Uitstoot NH4**, **Uitstoot CO2** en **Uitstoot N2O**.|
| [Gemiddelde uitstoot per categorie](#example-average-emissions-by-category) | Analyseer uw gemiddelde uitstoot per categorie. | [Duurzaamheidsposten](https://businesscentral.dynamics.com/?page=6220) | **Accountcategorie**, **Accountnaam**, **Uitstoot NH4**, **Uitstoot CO2** en **Uitstoot N2O**.|
| [Uitstoot per bereik](#example-emissions-by-scope) | Analyseer uw uitstoot per bereik. | [Duurzaamheidsposten](https://businesscentral.dynamics.com/?page=6220) | **Uitstootbereik**, **Accountcategorie**, **Uitstoot NH4**, **Uitstoot CO2** en **Uitstoot N2O**.|

## Voorbeeld: Uitstootoverzicht (som per categorie)

Volg deze stappen om uw uitstoot per categorie te analyseren:

1. Open de pagina [Duurzaamheidsposten](https://businesscentral.dynamics.com/?page=6220) en schakel de analysemodus in.
1. Ga naar het menu **Kolommen** en verwijder alle kolommen (selecteer het vakje naast het veld **Zoeken**).
1. Zet **Draaimodus** aan (direct boven het veld **Zoeken**).
1. Sleep de velden **Accountcategorie** en **Accountnaam** naar het gebied **Rijgroepen**. Sleep de velden in die volgorde.
1. Sleep de velden **Uitstoot NH4**, **Uitstoot CO2** en **Uitstoot N2O** naar het gebied **Waarden**.
1. Hernoem uw analysetabblad naar **Uitstootoverzicht (som)** of iets dat deze analyse voor u beschrijft.

De volgende afbeelding toont het resultaat van deze stappen.

:::image type="content" source="media/data-analysis-sustainability-entries.png" alt-text="Voorbeeld 1 van hoe u gegevensanalyse uitvoert op de pagina Duurzaamheidsposten." lightbox="media/data-analysis-sustainability-entries.png":::

## Voorbeeld: Gemiddelde uitstoot per categorie

Volg deze stappen om uw gemiddelde uitstoot per categorie te analyseren:

1. Open de pagina [Duurzaamheidsposten](https://businesscentral.dynamics.com/?page=6220) en schakel de analysemodus in.
1. Ga naar het menu **Kolommen** en verwijder alle kolommen (selecteer het vakje naast het veld **Zoeken**).
1. Zet **Draaimodus** aan (direct boven het veld **Zoeken**).
1. Sleep de velden **Accountcategorie** en **Accountnaam** naar het gebied **Rijgroepen**. Sleep de velden in die volgorde.
1. Sleep de velden **Uitstoot NH4**, **Uitstoot CO2** en **Uitstoot N2O** naar het gebied **Waarden**.
1. Voor elk veld in het gebied **Waarden** selecteert u het en wijzigt u de aggregatiefunctie in `Average`.
1. Hernoem uw analysetabblad naar **Uitstootoverzicht (gem)** of iets dat deze analyse voor u beschrijft.

De volgende afbeelding toont het resultaat van deze stappen.

:::image type="content" source="media/data-analysis-sustainability-entries-avg.png" alt-text="Voorbeeld 2 van hoe u gegevensanalyse uitvoert op de pagina Duurzaamheidsposten." lightbox="media/data-analysis-sustainability-entries-avg.png":::

## Voorbeeld: Uitstoot per bereik

Volg deze stappen om uw uitstoot per bereik te analyseren:

1. Open de pagina [Duurzaamheidsposten](https://businesscentral.dynamics.com/?page=6220) en schakel de analysemodus in.
1. Ga naar het menu **Kolommen** en verwijder alle kolommen (selecteer het vakje naast het veld **Zoeken**).
1. Zet **Draaimodus** aan (direct boven het veld **Zoeken**).
1. Sleep de velden **Uitstootbereik** en **Accountcategorie** naar het gebied **Rijgroepen**. Sleep de velden in die volgorde.
1. Sleep de velden **Uitstoot NH4**, **Uitstoot CO2** en **Uitstoot N2O** naar het gebied **Waarden**.
1. Hernoem uw analysetabblad naar **Uitstootoverzicht per bereik** of iets dat deze analyse voor u beschrijft.

De volgende afbeelding toont het resultaat van deze stappen.

:::image type="content" source="media/data-analysis-sustainability-entries-scope.png" alt-text="Voorbeeld 3 van hoe u gegevensanalyse uitvoert op de pagina Duurzaamheidsposten." lightbox="media/data-analysis-sustainability-entries-scope.png":::

## Gegevensbasis voor ad-hocanalyse van duurzaamheid

De informatie die u invoert in een duurzaamheidsdagboek is tijdelijk en u kunt deze in het dagboek wijzigen. Wanneer u een duurzaamheidsdagboek boekt, wordt de informatie overgebracht naar duurzaamheidsposten op afzonderlijke duurzaamheidsrekeningen, waar u deze niet kunt wijzigen. U kunt echter wel tegenboekingen of correcties boeken. De lijstpagina [Duurzaamheidsposten](https://businesscentral.dynamics.com/?page=6220) is de belangrijkste gegevensbron voor ad-hocanalyse van duurzaamheidsgegevens.

Voor meer informatie over het plaatsen van duurzaamheidsposten gaat u naar [Duurzaamheidsposten registreren](finance-sustainability-journal.md).

## Zie ook

[Duurzaamheidsposten vastleggen](finance-sustainability-journal.md)  
[Ingebouwde duurzaamheidsrapporten](sustainability-reports.md)   
[Overzicht van analyses, bedrijfsinformatie en rapportage](reports-bi-reporting.md)  
[Overzicht van duurzaamheidsbeheer](finance-manage-sustainability.md)   
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
