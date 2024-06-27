---
title: Analyse van vaste activa
description: 'Leer hoe u gegevens over vaste activa verzamelt, analyseert en deelt voor business intelligence.'
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '5601, 5600, 5615, 5616, 5617'
ms.date: 05/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="fixed-assets-analytics"></a>Analyse van vaste activa

Bedrijven met vaste activa verzamelen tijdens hun dagelijkse activiteiten veel gegevens over deze activa. Die gegevens ondersteunen waardevolle business intelligence (BI) voor beheerders van vaste activa:

- Aanschaf van activa
- Afschrijving van activa
- Verzekering en onderhoud
- Activabudgetten

[!INCLUDE[prod_short](includes/prod_short.md)] biedt veel functies voor het verzamelen, analyseren en delen van gegevens over vaste activa van uw organisatie:

- Financiële rapportage (voor financiële overzichten en KPI's op vaste-activarekeningen)
- Ad-hocanalyse in lijsten
- Ad-hocanalyse van gegevens in Excel (met behulp van Openen in Excel)
- Ingebouwde analysetools voor vaste activa
- Ingebouwde vaste-activarapporten

> [!NOTE]
> Analyses voor vaste activa zijn iets anders dan op andere gebieden. U moet gegevens analyseren die al aanwezig zijn, zoals de aanschaf van activa, afschrijving en verzekering, maar ook gegevens over toekomstige (voorspelde) gegevens, zoals afschrijving en buitengebruikstelling van activa. Voor dit laatste type analyse heeft [!INCLUDE[prod_short](includes/prod_short.md)] ingebouwde rapporten die deze cijfers kunnen berekenen.

Elke functie heeft voor- en nadelen, afhankelijk van het type gegevensanalyse en de rol van de gebruiker. Ga voor meer informatie naar [Overzicht van analyses, bedrijfsinformatie en rapportage](reports-bi-reporting.md).

In dit artikel worden manieren beschreven waarop u deze analytische functies kunt gebruiken om inzicht te krijgen in uw vaste activa.

## <a name="analytics-needs-in-asset-management"></a>Analytics-behoeften op het gebied van activamanagement

Bij het in kaart brengen van de analysebehoeften in activamanagement kan het helpen om een model te gebruiken dat gebaseerd is op persona's en dat hun analysebehoeften op een hoog niveau beschrijft.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustratie van verschillende persona's voor analyse" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Als het gaat om gegevens, hebben mensen in verschillende rollen verschillende behoeften, en ze gebruiken de gegevens op verschillende manieren. Mensen in activabeheer gaan bijvoorbeeld anders met gegevens om dan mensen in verkoop.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustratie van hoe verschillende persona's verschillende analysebehoeften hebben." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rol              | Gegevensaggregatie  | Typische manieren om gegevens te gebruiken                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|CFO/COO/CEO                 | Prestatiegegevens  | KPI's <br> Dashboards <br> Financiële rapporten           |
|Activabeheer/Controller   | Trends, overzichten | Ingebouwde managementrapporten <br> Ad-hocanalyse      | 
|Boekhouder                      | Gedetailleerde gegevens     | Ingebouwde operationele rapporten <br> Taakgegevens op het scherm |

## <a name="asset-management-kpis"></a>Activabeheer-KPI's

Een Key Performance Indicator (KPI) is een meetbare waarde die laat zien hoe effectief u uw doelen bereikt. In activabeheer gebruiken mensen vaak de volgende KPI’s om het gebruik van activa in hun organisatie te monitoren:

- Omzet totale activa
- Rendement op activa

## <a name="use-financial-reporting-to-produce-financial-statements-and-kpis-related-to-fixed-assets"></a>Financiële rapportage gebruiken om financiële overzichten en KPI’s te produceren in verband met vaste activa

De functie **Financiële rapportage** geeft u inzichten in de financiële gegevens die in uw rekeningschema zijn opgeslagen. U kunt financiële rapporten instellen om cijfers in grootboekrekeningen (GB) te analyseren en grootboekposten te vergelijken met budgetposten. Specifiek voor activamanagement kunt u financiële rapporten instellen voor de grootboekrekeningen die u gebruikt om vaste-activaboekingen bij te houden.

Dimensies spelen een belangrijke rol bij bedrijfsinformatie. Een dimensie bestaat uit gegevens die u kunt toevoegen aan een post als een parameter. Met dimensies kunt u invoergegevens groeperen met vergelijkbare kenmerken, zoals klanten, producten en verkoper, en kunt u deze groepen eenvoudig ophalen voor analyse. U kunt dimensies onder andere ook gebruiken wanneer u analyseweergaven definieert en wanneer u financiële rapporten maakt. Zie [Werken met dimensies](finance-dimensions.md) voor meer informatie.

Als u meer wilt weten over financiële rapportage, gaat u naar [Financiële rapporten voorbereiden met financiële gegevens en rekeningcategorieën](bi-how-work-account-schedule.md).

## <a name="finance-reporting-across-business-units-or-legal-entities-related-to-fixed-assets"></a>Financiële rapportage voor bedrijfsunits of rechtspersonen (in verband met vaste activa)

Sommige organisaties gebruiken [!INCLUDE [prod_short](includes/prod_short.md)] in meerdere bedrijfsunits of rechtspersonen. Anderen gebruiken [!INCLUDE [prod_short](includes/prod_short.md)] in dochterondernemingen die rapporteren aan moederorganisaties. [!INCLUDE [prod_short](includes/prod_short.md)] geeft accountants tools waarmee ze grootboekposten van twee of meer bedrijven (dochterondernemingen) kunnen overbrengen naar een geconsolideerd bedrijf. Specifiek voor activabeheer wilt u mogelijk grootboekposten voor uw vaste-activarekeningen consolideren om vaste-activa-KPI's voor bedrijfsunits of rechtspersonen bij te kunnen houden.

Ga naar [Bedrijfsconsolidatie](finance-consolidated-company-reporting.md) voor meer informatie.

## <a name="ad-hoc-analysis-of-fixed-assets-data"></a>Adhoc-analyse van vaste-activagegevens

Soms hoeft u alleen maar te controleren of de getallen correct zijn, of snel een cijfer bevestigen. De volgende functies zijn ideaal voor ad-hocanalyses:

- Gegevensanalyse op grootboeklijstpagina´s
- Openen in Excel

Met de functie gegevensanalyse kunt u een lijstpagina openen, zoals **Grootboekposten** of **VA-posten**, de analysemodus openen en vervolgens gegevens naar eigen inzicht groeperen, filteren en draaien.

:::image type="content" source="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png" alt-text="Voorbeeld van hoe u gegevensanalyse uitvoert op de pagina VA-posten om activawaarde te bekijken." lightbox="media/data-analysis-fa-ledger-entries-asset-overview-current-value.png":::

Op dezelfde manier kunt u de actie **Openen in Excel** gebruiken om een lijstpagina voor grootboekposten te openen, de lijst optioneel te filteren op een subset van de gegevens en vervolgens Excel te gebruiken om met de gegevens te werken. Bijvoorbeeld door gebruik te maken van functies zoals Gegevens analyseren, Wat-als-analyse of Prognoseblad.

<!-- :::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Example of how to do data analysis on the G/L entries data using Excel." lightbox="media/open-in-excel-gl-entries.png"::: -->

> [!TIP]
> Als u OneDrive configureert voor systeemfuncties, wordt de Excel-werkmap in uw browser geopend met behulp van Excel voor het web. 

Voor meer informatie over het uitvoeren van ad-hocanalyses van vaste-activagrootboeken zie [Ad-hocanalyse van vaste-activagegevens](ad-hoc-analysis-fa.md).


## <a name="built-in-reports-for-fixed-assets"></a>Ingebouwde rapporten voor vaste activa

[!INCLUDE [prod_short](includes/prod_short.md)] bevat verschillende ingebouwde rapporten, traceerfuncties en tools die auditors of controllers helpen die rapporteren over vaste activa.

Om een overzicht te krijgen van beschikbare rapporten kiest u **Alle rapporten**, boven aan uw startpagina. Met deze actie gaat u naar de pagina Rolverkenner, die wordt gefilterd op de functies in de optie **Rapport en analyse**. Als u rapporten met betrekking tot vaste activa wilt vinden, voert u in het veld **Zoeken** **vaste activa** in. Ga voor meer informatie naar [Rapporten zoeken met de Rolverkenner](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-fixed-assets.png" alt-text="Voorbeeld van rapporten over het financiële rolcentrum." lightbox="media/report-explorer-fixed-assets.png":::

<!-- Built-in reports come in two flavors:

- Designed for print (pdf).
- Designed for analysis in Excel. -->

Voor meer informatie over rapporten die relevant zijn voor vaste activa, zie [Ingebouwde VA-rapporten](fa-reports.md).

## <a name="on-screen-fixed-assets-analytics"></a>Analyse van vaste activa op het scherm

[!INCLUDE [prod_short](includes/prod_short.md)] heeft een aantal pagina's waarop u VA-overzichten en taken kunt vinden. Hier zijn enkele voorbeelden om u op weg te helpen:

- [Afschrijving berekenen, afschrijving boeken en afschrijving analyseren.](fa-how-depreciate-amortize.md)
- [Onderhoudskosten controleren](fa-how-maintain.md#monitor-maintenance-costs)
- [Verzekeringsdekking controleren](fa-how-insure.md#to-monitor-insurance-coverage)
- [Gewijzigde afschrijvingsboekwaarden weergeven](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification)
- [Buitengebruikstellingsposten weergeven](fa-how-dispose-retire.md#to-view-disposal-ledger-entries)
- [Voorspelde buitengebruikstellingswaarden weergeven](fa-how-manage-budgets.md#to-view-projected-disposal-values)

### <a name="show-fixed-asset-general-ledger-entries-and-balances-from-the-chart-of-accounts-page"></a>VA-grootboekposten en -saldi weergeven via de pagina Rekeningschema

Op de pagina Rekeningschema worden alle grootboekrekeningen weergegeven met samengevoegde cijfers in het grootboek. Vanaf deze pagina kunt u het volgende doen:  

- Rapporten weergeven waarin grootboekposten en saldi worden weergegeven.  
- Bekijk een lijst met boekingsgroepen voor die rekening.
- Afzonderlijke debet- en creditsaldo's voor één rekening bekijken.

Specifiek voor vaste activa kunt u op de pagina Rekeningschema een weergave maken waarin alleen de activarekeningen worden weergegeven of wellicht alleen de activarekeningen die u gebruikt om vaste activa te boeken.

:::image type="content" source="media/chart-of-accounts-page-fa.png" alt-text="Voorbeeld van hoe op de pagina Rekeningschema financiële inzichten worden weergegeven" lightbox="media/chart-of-accounts-page-fa.png":::

Ga voor meer informatie naar [Het rekeningschema begrijpen](finance-general-ledger.md#the-chart-of-accounts).

### <a name="analyze-data-by-dimensions-related-to-fixed-assets"></a>Gegevens analyseren per dimensie (in verband met vaste activa)

Dimensies zijn waarden waarmee posten worden gecategoriseerd, zodat u ze kunt bijhouden en analyseren in documenten, zoals VA-dagboeken. Dimensies kunnen bijvoorbeeld aangeven van welke afdeling of locatie een post afkomstig is.  

In plaats van voor elke afdeling of locatie aparte grootboekrekeningen in te stellen, kunt u dus bijvoorbeeld dimensies gebruiken als basis voor analyse en hoeft u geen ingewikkelde rekeningschemastructuur te maken.

Ga voor meer informatie naar [Gegevens analyseren per dimensie](bi-how-analyze-data-dimension.md)

## <a name="see-also"></a>Zie ook

[Financiële rapportage verwerken voor verschillende bedrijfseenheden of rechtspersonen](finance-consolidated-company-reporting.md)  
[Financiële rapporten voorbereiden met financiële gegevens en rekeningcategorieën](bi-how-work-account-schedule.md)  
[Het rekeningschema begrijpen](finance-general-ledger.md#the-chart-of-accounts)  
[Adhoc-analyse van vaste-activagegevens](ad-hoc-analysis-fa.md)   
[Ingebouwde vaste-activarapporten](fa-reports.md)  
[Overzicht van analyses, bedrijfsinformatie en rapportage](reports-bi-reporting.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
