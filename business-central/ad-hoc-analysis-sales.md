---
title: Adhoc-analyse van verkoopgegevens
description: Leer hoe u de gegevensanalysemodus gebruikt om verkoopgegevens te analyseren.
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 04/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Adhoc-analyse van verkoopgegevens

In dit artikel leert u hoe u de functie **Gegevensanalyse** gebruikt om verkoopgegevens te analyseren direct vanaf lijstpagina's en query's. U hoeft geen rapport uit te voeren of over te stappen naar een andere toepassing, zoals Excel. De functie biedt een interactieve en veelzijdige manier om gegevens te berekenen, samen te vatten en te onderzoeken. In plaats van rapporten uit te voeren met opties en filters, kunt u meerdere tabbladen toevoegen die verschillende taken of weergaven van de gegevens vertegenwoordigen. Enkele voorbeelden zijn 'Mijn klanten' of 'Verkoopstatistieken', of elke andere weergave die u maar kunt bedenken. Voor meer informatie over het gebruik van de functie **Gegevensanalyse** gaat u naar [Lijst- en querygegevens analyseren met de analysemodus](analysis-mode.md).

Gebruik de volgende lijstpagina's voor ad-hocanalyse van verkoopprocessen:

- [Verkooporders](https://businesscentral.dynamics.com/?page=9305)
- Grootboekposten
- [Klantenposten](https://businesscentral.dynamics.com/?page=25)
- Artikelposten
- Geboekte verkoopfacturen
- Verkoopretourorders

## Ad-hocanalysescenario's voor verkoop

Gebruik de functie **Gegevensanalyse** voor snelle feitencontrole en ad-hocanalyse:

- Als u geen rapport wilt uitvoeren.
- Als er geen rapport voor uw specifieke behoefte bestaat.
- Als u snel wilt herhalen om een goed overzicht te krijgen van een deel van uw bedrijf.

In de volgende secties vindt u voorbeelden van verkoopscenario's in [!INCLUDE [prod_short](includes/prod_short.md)].

| Vlak | Actie | Deze pagina openen in de analysemodus | Deze velden gebruiken |
| ---- | ----- | ------------------------------- |------------------- |
| [Verkoop (verwacht verkoopvolume)](#example-sales-expected-sales-volume) | Analyseer uw verwachte verkoopvolume. | [Verkooporders](https://businesscentral.dynamics.com/?page=9305) | **Naam van orderklant**, **Orderklantnr.**, **Nr.** , **Hoeveelheid**, **Documentdatum (jaar)** en **Documentdatum (maand)**. |
| [Verkoop (klantverkopen naar volume)](#example-sales-customer-sales-by-volume) | Een overzicht krijgen van welke klanten de meeste inkopen hebben gedaan of het hoogste saldo hebben openstaan. | [Klantenposten](https://businesscentral.dynamics.com/?page=25) | **Klantnaam**, **Documentnr.**, **Bedrag** en **Resterend bedrag**. |
| [Financiën (Tegoeden)](#example-finance-accounts-receivables) | Bekijk bijvoorbeeld wat uw klanten u verschuldigd zijn, uitgesplitst in tijdsintervallen voor wanneer bedragen moeten worden betaald. | [Klantenposten](https://businesscentral.dynamics.com/?page=25) | **Klantnaam**, **Vervaldatum** en **Resterend bedrag**. |

## Voorbeeld: Verkoop (verwacht verkoopvolume)

Volg deze stappen om uw verwachte verkoopvolume en verkoopbedragen voor niet-verzonden orders voor elke klant per jaar of maand te analyseren:

1. Open de lijst [Verkooporders](https://businesscentral.dynamics.com/?page=9305) en schakel de analysemodus in.
1. Ga naar het menu **Kolommen** en verwijder alle kolommen (selecteer het vakje naast het veld **Zoeken**).
1. Zet **Draaimodus** aan (direct boven het veld **Zoeken**).
1. Sleep de velden **Naam van orderklant**, **Orderklantnr.** en **Nr.** naar het gebied **Rijgroepen**. Sleep de velden in die volgorde.
1. Sleep het veld **Bedrag** naar het gebied **Waarden**.
1. Sleep de velden **Documentdatum (jaar)** en **Documentdatum (maand)** naar het gebied **Kolomlabels**. Sleep de velden in die volgorde.
1. Om de analyse voor een bepaald jaar of kwartaal uit te voeren, past u een filter toe in het menu **Extra filters**. Het menu bevindt zich aan de rechterkant van de pagina, net onder het menu **Kolommen**.
1. Hernoem uw analysetabblad naar **Verwacht verkoopvolume** of iets dat deze analyse voor u beschrijft.

## Voorbeeld: Verkoop (klantverkopen naar volume)

Als u een overzicht wilt produceren van de klanten die de meeste inkopen doen of het hoogste saldo hebben openstaan, volgt u deze stappen:

1. Open de lijst [Klantenposten](https://businesscentral.dynamics.com/?page=25) en schakel de analysemodus in.
1. Ga naar het menu **Kolommen** en verwijder alle kolommen (selecteer het vakje naast het veld **Zoeken**).
1. Sleep het veld **Klantnaam** naar het gebied **Rijgroepen** en het veld **Documentnr.** eronder.
1. Kies de velden **Bedrag** en **Resterend bedrag**.
1. Om de analyse voor een bepaald jaar of kwartaal uit te voeren, past u een filter toe in het menu **Extra filters**. Het menu bevindt zich aan de rechterkant van de pagina, net onder het menu **Kolommen**.
1. Hernoem uw analysetabblad naar **Klant naar verkoopvolume** of iets dat deze analyse voor u beschrijft.

De volgende afbeelding toont het resultaat van deze stappen.

:::image type="content" source="media/data-analysis-customer-ledger-entries.png" alt-text="Voorbeeld van hoe u gegevensanalyse uitvoert op de pagina Klantenposten." lightbox="media/data-analysis-customer-ledger-entries.png":::

## Voorbeeld: Financiën (Tegoeden)

Als u wilt zien wat uw klanten u verschuldigd zijn, wellicht uitgesplitst in tijdsintervallen voor wanneer bedragen moeten worden betaald, doet u het volgende:

1. Open de lijst [Klantenposten](https://businesscentral.dynamics.com/?page=25) en schakel de analysemodus in.
1. Verwijder in naar het menu **Kolommen** alle kolommen (selecteer het vakje naast het veld **Zoeken**).
1. Zet **Draaimodus** aan (direct boven het veld **Zoeken**).
1. Sleep het veld **Klantnaam** naar het gebied **Rijgroepen** en sleep het veld **Resterend bedrag** naar het gebied **Waarden**.
1. Sleep het veld **Vervaldatum (maand)** naar het gebied **Kolomlabels** .
1. Om de analyse voor een bepaald jaar of kwartaal uit te voeren, past u een filter toe in het menu **Extra filters**. Het menu bevindt zich aan de rechterkant van de pagina, net onder het menu **Kolommen**.
1. Hernoem uw analysetabblad naar **Oudere accounts per maand** of iets dat deze analyse voor u beschrijft.

## Gegevensbasis voor ad-hocanalyse van verkopen

Nadat u informatie over een verkooporder hebt ingevoerd en alle verkooporderregels hebt toegevoegd, kunt u de order boeken. Met boeken worden een verzending en een factuur gemaakt. [!INCLUDE [prod_short](includes/prod_short.md)] werkt de rekening van de klant, het grootboek en de artikelposten bij:

- Voor elke verkooporder wordt een verkooppost gemaakt in de tabel **Grootboekpost**. Ook wordt er een post in de klantrekening in de tabel **Klantpost** en een grootboekpost wordt in de desbetreffende rekening voor tegoeden gemaakt. Bovendien kan het boeken van de order resulteren in een btw-post en een grootboekpost voor de totale korting.
- Voor elke verkooporderregel wordt een artikelpost gemaakt in de tabel **Artikelpost** (als de verkoopregels artikelnummers bevatten) of wordt een grootboekpost gemaakt in de tabel **Grootboekpost** (als de verkoopregels een grootboekrekening bevatten). Daarnaast worden verkooporders altijd geregistreerd in de tabellen **Verkoopverzendkop** en **Verkoopfactuurkop**.

Ga voor meer informatie over direct verkopen naar [Verkopen boeken](ui-post-sales.md).

## Zie ook

[Verkopen boeken](ui-post-sales.md)  
[Lijst- en querygegevens analyseren met de analysemodus](analysis-mode.md)  
[Overzicht van verkoopanalyses](sales-analytics-overview.md)  
[Overzicht van analyses, bedrijfsinformatie en rapportage](reports-bi-reporting.md)  
[Overzicht van verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]