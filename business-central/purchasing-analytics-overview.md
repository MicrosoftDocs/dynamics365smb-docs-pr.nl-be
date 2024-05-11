---
title: Analyse bij inkoop
description: 'Business Central bevat veel functies die u helpen bij het verzamelen, analyseren en delen van waardevolle verkoopgegevens voor business intelligence en besluitvorming binnen de inkooporganisatie.'
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

# <a name="analytics-in-purchasing"></a>Analyse bij inkoop

Bedrijven leggen tijdens dagelijkse activiteiten een veel gegevens vast die waardevolle business intelligence (BI) voor inkoopmanagers ondersteunen:

- Inkoopoffertes
- Inkooporders
- Inkoopfacturen

[!INCLUDE[prod_short](includes/prod_short.md)] biedt veel functies voor het verzamelen, analyseren en delen van de inkoopgegevens van uw organisatie:

- Ad-hocanalyse in lijsten
- Ad-hocanalyse van gegevens in Excel (met behulp van Openen in Excel)
- Ingebouwde verkooprapporten

Elk van deze functies heeft voor- en nadelen, afhankelijk van het type gegevensanalyse en de rol van de gebruiker. Ga voor meer informatie naar [Overzicht van analyses, bedrijfsinformatie en rapportage](reports-bi-reporting.md).

In dit artikel wordt beschreven hoe u deze analytische functies kunt gebruiken om inkoopinzichten te verschaffen.

## <a name="analytics-needs-in-purchasing"></a>Analysebehoefte in inkoop

Bij het in kaart brengen van de analysebehoeften in inkoop kan het helpen om een model te gebruiken dat gebaseerd is op persona's en dat verschillende analysebehoeften op een hoog niveau beschrijft.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustratie van verschillende persona's voor analyse" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Mensen in verschillende rollen hebben verschillende behoeften als het om gegevens gaat, en ze gebruiken de gegevens op verschillende manieren. Mensen in activabeheer gaan bijvoorbeeld anders met gegevens om dan mensen in verkoop.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustratie van hoe verschillende persona's verschillende analysebehoeften hebben." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rol              | Gegevensaggregatie  | Typische manieren om gegevens te gebruiken                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|COO/CSO/CFO/CEO    | Prestatiegegevens  | KPI's <br> Dashboards <br> Financiële rapporten           |
|Inkoopmanager      | Trends, overzichten | Ingebouwde managementrapporten <br> Ad-hocanalyse      | 
|Inkoper/Inkoopagent | Gedetailleerde gegevens     | Ingebouwde operationele rapporten <br> Taakgegevens op het scherm |

<!-- 
## <a name="purchasing-kpis"></a>Purchasing KPIs

A key performance indicator (KPI) is a measurable value that shows how effectively you’re meeting your goals. In purchasing management, people often use the following KPIs to monitor their organization's purchasing performance:

- TODO  
-->

## <a name="use-financial-reporting-to-produce-financial-statements-and-kpis-related-to-purchasing"></a>Financiële rapportage gebruiken om financiële overzichten en KPI’s te produceren (in verband met inkoop)

De functie **Financiële rapportage** geeft u inzichten in de financiële gegevens die in uw rekeningschema zijn opgeslagen. U kunt financiële rapporten instellen om cijfers in grootboekrekeningen (GB) te analyseren en grootboekposten te vergelijken met budgetposten. Specifiek voor inkoop kunt u financiële rapporten instellen voor de grootboekrekeningen die u gebruikt om inkoopboekingen bij te houden.

Dimensies spelen een belangrijke rol bij bedrijfsinformatie. Een dimensie bestaat uit gegevens die u kunt toevoegen aan een post als een parameter. Met dimensies kunt u invoergegevens groeperen met vergelijkbare kenmerken, zoals klanten, regio's en producten, en kunt u deze groepen eenvoudig ophalen voor analyse. U gebruikt dimensies ook wanneer u analyseweergaven definieert en wanneer u financiële rapporten maakt. Zie [Werken met dimensies](finance-dimensions.md) voor meer informatie.

Als u meer wilt weten over financiële rapporten, gaat u naar [Financiële rapporten voorbereiden met financiële gegevens en rekeningcategorieën](bi-how-work-account-schedule.md).

## <a name="finance-reporting-across-business-units-or-legal-entities-related-to-purchasing"></a>Financiële rapportage voor bedrijfseenheden of rechtspersonen (in verband met inkoop)

Sommige organisaties gebruiken [!INCLUDE [prod_short](includes/prod_short.md)] in meerdere bedrijfsunits of rechtspersonen. Anderen gebruiken [!INCLUDE [prod_short](includes/prod_short.md)] in dochterondernemingen die rapporteren aan moederorganisaties. [!INCLUDE [prod_short](includes/prod_short.md)] geeft accountants tools waarmee ze grootboekposten van twee of meer bedrijven (dochterondernemingen) kunnen overbrengen naar een geconsolideerd bedrijf. Specifiek voor inkoopbeheer wilt u mogelijk grootboekposten voor uw inkooprekeningen consolideren om verkoop-KPI's voor bedrijfsunits of rechtspersonen bij te houden.

Ga naar [Bedrijfsconsolidatie](finance-consolidated-company-reporting.md) voor meer informatie.

## <a name="ad-hoc-analysis-of-purchasing-data"></a>Adhoc-analyse van inkoopgegevens

Soms hoeft u alleen maar te controleren of de getallen correct zijn, of snel een cijfer bevestigen. De volgende functies zijn ideaal voor ad-hocanalyses:

- Gegevensanalyse op grootboeklijstpagina´s
- Openen in Excel

Met de functie **Gegevensanalyse** kunt u vrijwel elke lijstpagina openen, zoals **Inkooporders**, **Geboekte inkoopfacturen**, **Leveranciersposten** of **Grootboekposten**, de analysemodus openen en vervolgens gegevens naar eigen inzicht groeperen, filteren en draaien.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Voorbeeld van hoe u gegevensanalyse uitvoert op de pagina Klantenposten." lightbox="media/data-analysis-vendor-ledger-entries.png":::

Op dezelfde manier kunt u de actie **Openen in Excel** gebruiken om een lijstpagina te openen, de lijst te filteren op een subset van de gegevens en vervolgens Excel te gebruiken om met de gegevens te werken. Bijvoorbeeld door gebruik te maken van functies zoals Gegevens analyseren, Wat-als-analyse of Prognoseblad.

:::image type="content" source="media/open-in-excel-vendor-ledger-entries.png" alt-text="Voorbeeld van hoe u gegevensanalyse uitvoert op de gegevens van klantenposten met Excel." lightbox="media/open-in-excel-vendor-ledger-entries.png":::

> [!TIP]
> Als u OneDrive configureert voor systeemfuncties, wordt de Excel-werkmap in uw browser geopend.

Voor meer informatie over het uitvoeren van ad-hocanalyses van inkoopgegevens gaat u naar [Ad-hocanalyse van inkoopgegevens](ad-hoc-analysis-purchasing.md).

## <a name="built-in-reports-for-purchasing"></a>Ingebouwde rapporten voor inkoop

[!INCLUDE [prod_short](includes/prod_short.md)] bevat verschillende ingebouwde rapporten, traceringsfuncties en tools waarmee inkooporganisaties kunnen rapporteren over hun gegevens.

Om een overzicht te krijgen van beschikbare rapporten kiest u **Alle rapporten**, boven aan de startpagina. Met deze actie gaat u naar de Rolverkenner, die wordt gefilterd op de functies in de optie **Rapport en analyse**. Ga voor meer informatie naar [Rapporten zoeken met de Rolverkenner](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-purchasing.png" alt-text="Voorbeeld van rapporten over het rolcentrum XXX." lightbox="media/report-explorer-purchasing.png":::

<!-- Built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Ga naar [Ingebouwde rapporten voor inkoop](purchase-reports.md) voor meer informatie over rapporten die relevant zijn voor inkopen.

## <a name="on-screen-purchasing-analytics"></a>Inkoopanalyses op het scherm

[!INCLUDE [prod_short](includes/prod_short.md)] heeft een aantal pagina's waarop u inkoopoverzichten en taken kunt vinden. Hier is een voorbeeld om u op weg te helpen:

- [Datums berekenen voor inkoop](purchasing-date-calculation-for-purchases.md)

### <a name="show-purchasing-related-general-ledger-entries-and-balances-from-the-chart-of-accounts-page"></a>Aan inkoop gerelateerde grootboekposten en saldi weergeven via de pagina Rekeningschema

Op de pagina Rekeningschema worden alle grootboekrekeningen weergegeven met samengevoegde cijfers die naar het grootboek zijn geboekt. Vanaf deze pagina kunt u het volgende doen:  

- Rapporten weergeven waarin grootboekposten en saldi worden weergegeven.  
- Bekijk een lijst met boekingsgroepen voor die rekening.
- Afzonderlijke debet- en creditsaldo's voor één rekening bekijken.

Specifiek voor inkoop kunt u op de pagina Rekeningschema een weergave maken waarin alleen de rekeningen worden weergegeven die u gebruikt om inkoopgegevens te boeken.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Voorbeeld van hoe op de pagina Rekeningschema financiële inzichten worden weergegeven" lightbox="media/chart-of-accounts-page.png":::

Ga voor meer informatie naar [Het rekeningschema begrijpen](finance-general-ledger.md#the-chart-of-accounts).

### <a name="analyze-data-by-dimensions-related-to-purchasing"></a>Gegevens analyseren per dimensie (in verband met inkoop)

Dimensies zijn waarden waarmee posten worden gecategoriseerd, zodat u ze kunt bijhouden en analyseren in documenten, zoals inkooporders. Dimensies kunnen bijvoorbeeld aangeven tot welk project of welke afdeling een post behoort.  

In plaats van voor elke afdeling of locatie aparte grootboekrekeningen in te stellen, kunt u dus bijvoorbeeld dimensies gebruiken als basis voor analyse en hoeft u geen ingewikkelde rekeningschemastructuur te maken.

Ga voor meer informatie naar [Gegevens analyseren per dimensie](bi-how-analyze-data-dimension.md).

## <a name="see-also"></a>Zie ook

[Bedrijfsconsolidatie](finance-consolidated-company-reporting.md)  
[Financiële rapporten voorbereiden met financiële gegevens en rekeningcategorieën](bi-how-work-account-schedule.md)  
[Financiële rapportage verwerken voor verschillende bedrijfseenheden of rechtspersonen](finance-consolidated-company-reporting.md)  
[Adhoc-analyse van inkoopgegevens](ad-hoc-analysis-purchasing.md)  
[Ingebouwde rapporten voor inkoop](purchase-reports.md)  
[Het rekeningschema begrijpen](finance-general-ledger.md#the-chart-of-accounts)  
[Gegevens analyseren per dimensie](bi-how-analyze-data-dimension.md)  
[Overzicht van analyses, bedrijfsinformatie en rapportage](reports-bi-reporting.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
