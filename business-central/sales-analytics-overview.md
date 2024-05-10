---
title: Verkoopanalyse
description: 'Business Central bevat veel functies die u helpen bij het verzamelen, analyseren en delen van waardevolle verkoopgegevens voor business intelligence en besluitvorming binnen de verkooporganisatie.'
author: kennienp
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 04/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="sales-analytics"></a>Verkoopanalyse

Bedrijven leggen tijdens dagelijkse activiteiten een veel gegevens vast die waardevolle business intelligence (BI) voor verkoopmanagers ondersteunen:

- Verkoopkansen
- Verkoopoffertes
- Verkooporders
- Verkoopfacturen

[!INCLUDE[prod_short](includes/prod_short.md)] biedt veel functies voor het verzamelen, analyseren en delen van de verkoopgegevens van uw organisatie:

- Ad-hocanalyse in lijsten
- Ad-hocanalyse van gegevens in Excel (met behulp van Openen in Excel)
- Ingebouwde verkoopanalysetools
- Ingebouwde verkooprapporten

Elk van deze functies heeft voor- en nadelen, afhankelijk van het type gegevensanalyse en de rol van de gebruiker. Ga voor meer informatie naar [Overzicht van analyses, bedrijfsinformatie en rapportage](reports-bi-reporting.md).

In dit artikel wordt beschreven hoe u deze analytische functies kunt gebruiken om verkoopinzichten te verschaffen.

## <a name="analytics-needs-in-sales"></a>Analysebehoefte in verkoop

Bij het in kaart brengen van de analysebehoeften in verkoopmanagement kan het helpen om een model te gebruiken dat gebaseerd is op persona's en dat verschillende analysebehoeften op een hoog niveau beschrijft.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustratie van verschillende persona's voor analyse" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Mensen in verschillende rollen hebben verschillende behoeften als het om gegevens gaat, en ze gebruiken de gegevens op verschillende manieren. Mensen in activabeheer gaan bijvoorbeeld anders met gegevens om dan mensen in verkoop.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustratie van hoe verschillende persona's verschillende analysebehoeften hebben." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rol              | Gegevensaggregatie  | Typische manieren om gegevens te gebruiken                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|CCO/CFO/CEO    | Prestatiegegevens  | KPI's <br> Dashboards <br> Financiële rapporten           |
|Verkoopmanager      | Trends, overzichten | Ingebouwde managementrapporten <br> Ad-hocanalyse      | 
|Accountmanager/verkoopmedewerker | Gedetailleerde gegevens     | Ingebouwde operationele rapporten <br> Taakgegevens op het scherm |

<!-- 
## <a name="sales-kpis"></a>Sales KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In sales management, people often use the following KPIs to monitor their organization's sales performance:

- TODO  
-->

## <a name="use-financial-reporting-to-produce-financial-statements-and-kpis-related-to-sales"></a>Financiële rapportage gebruiken om financiële overzichten en KPI’s te produceren (in verband met verkoop)

De functie **Financiële rapportage** geeft u inzichten in de financiële gegevens die in uw rekeningschema zijn opgeslagen. U kunt financiële rapporten instellen om cijfers in grootboekrekeningen (GB) te analyseren en grootboekposten te vergelijken met budgetposten. Specifiek voor verkoopmanagement kunt u financiële rapporten instellen voor de grootboekrekeningen die u gebruikt om verkoopboekingen bij te houden.

Dimensies spelen een belangrijke rol bij bedrijfsinformatie. Een dimensie bestaat uit gegevens die u toevoegt aan een post als een parameter. Met dimensies kunt u posten groeperen met soortgelijke kenmerken, zoals klanten, regio's, producten en verkoper. U gebruikt dimensies ook wanneer u analyseweergaven definieert en wanneer u financiële rapporten maakt. Zie [Werken met dimensies](finance-dimensions.md) voor meer informatie.

Als u meer wilt weten over financiële rapporten, gaat u naar [Financiële rapporten voorbereiden met financiële gegevens en rekeningcategorieën](bi-how-work-account-schedule.md).

## <a name="finance-reporting-across-business-units-or-legal-entities-related-to-sales"></a>Financiële rapportage voor bedrijfsunits of rechtspersonen in verband met verkoop

Sommige organisaties gebruiken [!INCLUDE [prod_short](includes/prod_short.md)] in meerdere bedrijfsunits of rechtspersonen. Anderen gebruiken [!INCLUDE [prod_short](includes/prod_short.md)] in dochterondernemingen die rapporteren aan moederorganisaties. [!INCLUDE [prod_short](includes/prod_short.md)] geeft accountants tools waarmee ze grootboekposten van twee of meer bedrijven (dochterondernemingen) kunnen overbrengen naar een geconsolideerd bedrijf. Specifiek voor verkoopbeheer wilt u mogelijk grootboekposten voor uw verkooprekeningen consolideren om verkoop-KPI's voor bedrijfsunits of rechtspersonen bij te kunnen houden.

Ga naar [Bedrijfsconsolidatie](finance-consolidated-company-reporting.md) voor meer informatie.

## <a name="ad-hoc-analysis-of-sales-data"></a>Adhoc-analyse van verkoopgegevens

Soms hoeft u alleen maar te controleren of de getallen correct zijn, of snel een cijfer bevestigen. De volgende functies zijn ideaal voor ad-hocanalyses:

- Gegevensanalyse op grootboeklijstpagina´s
- Openen in Excel

Met de functie Gegevensanalyse kunt u een lijstpagina openen, zoals de pagina's **Grootboekposten**, **Klantenposten**, **Artikelposten** of **Geboekte facturen**, de analysemodus openen en vervolgens gegevens naar eigen inzicht groeperen, filteren en draaien.

:::image type="content" source="media/data-analysis-customer-ledger-entries.png" alt-text="Voorbeeld van hoe u gegevensanalyse uitvoert op de pagina Klantenposten." lightbox="media/data-analysis-customer-ledger-entries.png":::

Op dezelfde manier kunt u de actie **Openen in Excel** gebruiken om een lijstpagina te openen, de lijst optioneel te filteren op een subset van de gegevens en vervolgens Excel te gebruiken om met de gegevens te werken. Bijvoorbeeld door gebruik te maken van functies zoals Gegevens analyseren, Wat-als-analyse of Prognoseblad.

:::image type="content" source="media/open-in-excel-customer-ledger-entries.png" alt-text="Voorbeeld van hoe u gegevensanalyse uitvoert op de gegevens van klantenposten met Excel." lightbox="media/open-in-excel-customer-ledger-entries.png":::

> [!TIP]
> Als u OneDrive configureert voor systeemfuncties, wordt de Excel-werkmap in uw browser geopend.

Voor meer informatie over het uitvoeren van ad-hocanalyses van verkoopgegevens gaat u naar [Ad-hocanalyse van verkoopgegevens](ad-hoc-analysis-sales.md). 

## <a name="built-in-reports-for-sales"></a>Ingebouwde verkooprapporten

[!INCLUDE [prod_short](includes/prod_short.md)] bevat verschillende ingebouwde rapporten, traceringsfuncties en tools waarmee verkooporganisaties kunnen rapporteren over hun gegevens.

Om een overzicht te krijgen van beschikbare rapporten kiest u **Alle rapporten** in het bovenste deelvenster van uw startpagina. Met deze actie gaat u naar de Rolverkenner, die wordt gefilterd op de functies in de optie **Rapport en analyse**. Ga voor meer informatie naar [Rapporten zoeken met de Rolverkenner](ui-role-explorer.md). 

:::image type="content" source="media/report-explorer-sales.png" alt-text="Voorbeeld van rapporten over het financiële rolcentrum." lightbox="media/report-explorer-sales.png":::

Er zijn twee soorten ingebouwde rapporten:

- Ontworpen om af te drukken (pdf).
- Ontworpen voor analyse in Excel.

Ga naar [Ingebouwde rapporten voor verkoop](sales-reports.md) voor meer informatie over rapporten die relevant zijn voor verkopen.

## <a name="on-screen-sales-analytics"></a>Verkoopanalyses op het scherm

[!INCLUDE [prod_short](includes/prod_short.md)] heeft een aantal pagina's waarop u verkoopoverzichten en taken kunt vinden. Hier zijn enkele voorbeelden om u op weg te helpen:

- [De lijst **Verkoopoffertes** openen](https://businesscentral.dynamics.com/?page=9300)
- [De lijst **Verkooporders** openen](https://businesscentral.dynamics.com/?page=9305)
- [De lijst **Geboekte verkoopfacturen** openen](https://businesscentral.dynamics.com/?page=143)
- [De lijst **Verkoopretourorders** openen](https://businesscentral.dynamics.com/?page=9304)
- [Ordertoezeggingsdatums berekenen](sales-how-to-calculate-order-promising-dates.md)
- [Leveringsdatums berekenen voor verkooporders](sales-date-calculation-for-sales.md)
- [Pakketten traceren](sales-how-track-packages.md)

### <a name="show-sales-related-general-ledger-entries-and-balances-from-the-chart-of-accounts-page"></a>Aan verkoop gerelateerde grootboekposten en saldi weergeven vanaf de pagina Rekeningschema

Op de pagina Rekeningschema worden alle grootboekrekeningen weergegeven met samengevoegde cijfers die naar het grootboek zijn geboekt. Vanaf deze pagina kunt u het volgende doen:  

- Rapporten weergeven waarin grootboekposten en saldi worden weergegeven.  
- Bekijk een lijst met boekingsgroepen voor die rekening.
- Afzonderlijke debet- en creditsaldo's voor één rekening bekijken.

Specifiek voor verkoop kunt u op de pagina Rekeningschema een weergave maken waarin alleen de rekeningen worden weergegeven die u gebruikt om verkoopposten te boeken.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Voorbeeld van hoe op de pagina Rekeningschema financiële inzichten worden weergegeven" lightbox="media/chart-of-accounts-page.png":::

Ga voor meer informatie naar [Het rekeningschema begrijpen](finance-general-ledger.md#the-chart-of-accounts).

### <a name="analyze-data-by-dimensions-related-to-sales"></a>Gegevens analyseren per dimensie (in verband met verkoop)

Dimensies zijn waarden waarmee posten worden gecategoriseerd, zodat u ze kunt bijhouden en analyseren in documenten, zoals verkooporders. Dimensies kunnen bijvoorbeeld aangeven tot welk project of welke afdeling een post behoort.  

In plaats van voor elke afdeling of locatie aparte grootboekrekeningen in te stellen, kunt u dus bijvoorbeeld dimensies gebruiken als basis voor analyse en hoeft u geen ingewikkelde rekeningschemastructuur te maken.

Ga voor meer informatie naar [Gegevens analyseren per dimensie](bi-how-analyze-data-dimension.md).

## <a name="see-also"></a>Zie ook

[Bedrijfsconsolidatie](finance-consolidated-company-reporting.md)   
[Financiële rapporten voorbereiden met financiële gegevens en rekeningcategorieën](bi-how-work-account-schedule.md)  
[Financiële rapportage verwerken voor verschillende bedrijfseenheden of rechtspersonen](finance-consolidated-company-reporting.md)  
[Adhoc-analyse van verkoopgegevens](ad-hoc-analysis-sales.md)   
[Ingebouwde verkooprapporten](sales-reports.md)   
[Het rekeningschema begrijpen](finance-general-ledger.md#the-chart-of-accounts)  
[Gegevens analyseren per dimensie](bi-how-analyze-data-dimension.md)  
[Overzicht van analyses, bedrijfsinformatie en rapportage](reports-bi-reporting.md)   
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
