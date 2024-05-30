---
title: Ad-hoc analyses bij inkoop
description: Leer hoe u de gegevensanalysemodus gebruikt om gegevens te analyseren bij inkoop.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '9306, 9307, 518, 29'
ms.date: 04/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Ad-hoc analyses bij inkoop

In dit artikel leert u hoe u inkoopgegevens vanaf lijstpagina's en query's analyseert met behulp van de functie **Gegevensanalyse**. Met de functie kunt u gegevens rechtstreeks vanaf de pagina analyseren, zonder dat u een rapport hoeft uit te voeren of te openen of naar een andere toepassing zoals Excel hoeft te schakelen. Gegevensanalyse biedt een interactieve en veelzijdige manier om gegevens te berekenen, samen te vatten en te onderzoeken. In plaats van rapporten uit te voeren met opties en filters, kunt u meerdere tabbladen toevoegen die verschillende taken of weergaven van de gegevens vertegenwoordigen. Enkele voorbeelden zijn 'Mijn leveranciers' of 'Inkoopstatistieken', of elke andere weergave die u maar kunt bedenken. Voor meer informatie over het gebruik van de functie **Gegevensanalyse** gaat u naar [Lijst- en querygegevens analyseren met de analysemodus](analysis-mode.md).

Gebruik de volgende lijstpagina's voor ad-hocanalyse van inkoopprocessen:

- [Inkooporders](https://businesscentral.dynamics.com/?page=9307)
- [Inkoopregels](https://businesscentral.dynamics.com/?page=518)
- [Geboekte inkoopfacturen](https://businesscentral.dynamics.com/?page=146)
- [Leveranciersposten](https://businesscentral.dynamics.com/?page=29)
- [Grootboekposten](https://businesscentral.dynamics.com/?page=20)

## Ad-hoc analysescenario's voor inkoop

Gebruik de functie **Gegevensanalyse** voor snelle feitencontrole en ad-hocanalyse:

- Als u geen rapport wilt uitvoeren
- Als er geen rapport voor uw specifieke behoeften bestaat
- Als u snel wilt herhalen om een goed overzicht te krijgen van een deel van uw bedrijf.

In de volgende secties vindt u voorbeelden van inkoopscenario's in [!INCLUDE [prod_short](includes/prod_short.md)].

| Vlak | Actie | Deze pagina openen in de analysemodus | Deze velden gebruiken |
| ---- | ----- | ------------------------------- |------------------- |
| [Overzicht van GRNI](#example-goods-received-not-invoiced-grni-overview) | Ontvang een overzicht van ontvangen goederen, niet gefactureerd (GRNI) voor alle leveranciers. | [Inkoopregels](https://businesscentral.dynamics.com/?page=518) | **Type**, **Ontv./Niet gefact. bedrag (LV)** (filter op deze velden), **Leveranciersnr.**, **Documentnr.**, **Nr.** en **Ontv./Niet gefact. bedrag (LV)** <br><br> **Opmerking:** Om deze velden toe te voegen moet u de pagina personaliseren. Zie voor meer informatie [Uw werkruimte personaliseren](ui-personalization-user.md). | 
| [Financiën (crediteuren)](#example-finance-accounts-payable) | Bekijk wat u uw leveranciers verschuldigd bent, uitgesplitst in tijdsintervallen voor wanneer bedragen moeten worden betaald. | [Leveranciersposten](https://businesscentral.dynamics.com/?page=29) | **Leveranciersnaam**, **Documentsoort**, **Documentnr.**, **Vervaldatum (jaar)**, **Vervaldatum (maand)** en **Resterend bedrag**. |

## Voorbeeld: overzicht ontvangen goederen, niet gefactureerd (GRNI)

Volg deze stappen om een overzicht van ontvangen, niet gefactureerde goederen (GRNI) voor leveranciers te maken:

1. Open de lijstpagina [Inkoopregels](https://businesscentral.dynamics.com/?page=518).
1. Personaliseer de pagina door het veld **Ontvangen niet gefactureerd bedrag** toe te voegen. Als u de pagina wilt personaliseren, kiest u **Instellingen** en vervolgens **Personaliseren**.
1. Kies :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus openen."::: om de analysemodus in te schakelen.
1. Ga naar het menu **Kolommen** en verwijder alle kolommen (selecteer het vakje naast het veld **Zoeken**, rechts).
1. Stel in het menu **Extra filters** (aan de rechterkant, onder het menu **Kolommen**) de volgende filters in:
    - **Type = Artikel**
    - **Ontv./Niet gefact. bedrag (LV) >0**. 
1. Sleep de velden **Leveranciersnr.**, **Documentnr.** en **Nr.** naar het gebied **Rijgroepen**. Sleep de velden in die volgorde.
1. Voeg het veld **Ontv./Niet gefact. bedrag (LV)** toe om dit op te nemen in het overzicht.
1. Om de analyse voor een bepaald jaar of kwartaal uit te voeren, past u een filter toe in het menu **Analysefilters**. Het menu bevindt zich aan de rechterkant van de pagina, net onder het menu **Kolommen**.
1. Hernoem uw analysetabblad naar **Overzicht ontvangen goederen, niet gefactureerd (GRNI)** of iets dat deze analyse beschrijft.

## Voorbeeld: financiën (schulden)

Als u wilt zien wat u uw leveranciers verschuldigd bent, wellicht uitgesplitst in tijdsintervallen voor wanneer bedragen moeten worden betaald, doet u het volgende:

1. Open de lijstpagina [Leveranciersposten](https://businesscentral.dynamics.com/?page=29) en schakel de analysemodus in.
1. Ga naar het menu **Kolommen** en verwijder alle kolommen (selecteer het vakje naast het veld **Zoeken**, rechts).
1. Schakel de schakelaar **Draaimodus** in (bevindt zich boven het veld **Zoeken**, rechts).
1. Sleep de velden **Leveranciersnaam**, **Documentsoort** en **Documentnummer** naar het gebied **Rijgroepen** en sleep vervolgens het veld **Resterend bedrag** naar het gebied **Waarden**.
1. Sleep de velden **Vervaldatum (jaar)** en **Vervaldatum (maand)** naar het gebied **Kolomlabels**. Sleep de velden in die volgorde.
1. Als u de analyse wilt uitvoeren voor een bepaald jaar of kwartaal, past u een filter toe in het menu **Analysefilters** (aan de rechterkant onder het menu **Kolommen**).
1. Hernoem uw analysetabblad naar **Oudere accounts per maand** of iets dat deze analyse beschrijft.

De volgende afbeelding toont het resultaat van deze stappen.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Voorbeeld van hoe u gegevensanalyse uitvoert op de pagina Klantenposten." lightbox="media/data-analysis-vendor-ledger-entries.png":::

## Gegevensbasis voor ad-hocanalyse van inkopen

Wanneer u een inkoopdocument boekt, werkt [!INCLUDE [prod_short](includes/prod_short.md)] de rekening van de leverancier, het grootboek, de artikelposten en de resourceposten bij:

- Voor elk inkoopdocument wordt een inkooppost gemaakt in de tabel **Grootboekpost**. Ook wordt een post in de leveranciersrekening in de tabel **Leverancierspost** gemaakt en wordt er een grootboekpost in de betreffende schuldenrekening gemaakt. Bovendien kan het boeken van de inkoop resulteren in een btw-post en een grootboekpost voor het totale kortingsbedrag.

- Voor elke inkoopregel worden, indien van toepassing, boekingen gemaakt in de:
  - Tabel **Artikelpost** als de inkoopregel van het type Artikel is.
  - Tabel **Grootboekpost** als de inkoopregel van het type Grootboekrekening is
  - Tabel **Resourcepost** als de inkoopregel van het type Resource is.
- Daarnaast worden inkoopdocumenten altijd vastgelegd in de tabellen **Inkoopontvangst** en **Inkoopfactuur**.

Ga voor meer informatie naar [Inkopen boeken](purchasing-how-record-purchases.md#posting-purchases).

## Zie ook

[Inkopen boeken](purchasing-how-record-purchases.md#posting-purchases)  
[Lijst- en querygegevens analyseren met de analysemodus](analysis-mode.md)  
[Overzicht van analyses, bedrijfsinformatie en rapportage](reports-bi-reporting.md)  
[Overzicht van inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]