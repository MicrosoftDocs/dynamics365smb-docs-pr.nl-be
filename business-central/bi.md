---
title: Financiële analyse
description: 'Business Central helpt u bij het verzamelen, analyseren en delen van bedrijfsgegevens voor business intelligence.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '103, 108, 198, 490'
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Financiële analyse

Bedrijven leggen tijdens dagelijkse activiteiten een enorme hoeveelheid gegevens vast die waardevolle business intelligence (BI) voor besluitvormers ondersteunen:

- Omzetcijfers
- Inkopen
- Bedrijfskosten
- Werknemerssalarissen
- Budgetten

[!INCLUDE[prod_short](includes/prod_short.md)] bevat veel functies voor het verzamelen, analyseren en delen van de financiële gegevens van uw organisatie:

- Financiële rapportage (voor financiële overzichten en KPI’s)
- Ad-hocanalyse in lijsten
- Ad-hocanalyse van gegevens in Excel (met behulp van Openen in Excel)
- Ingebouwde financiële rapporten

Elk van deze functies heeft eigen voor- en nadelen, afhankelijk van het type gegevensanalyse en de rol van de gebruiker. Ga voor meer informatie naar [Overzicht van analyses, bedrijfsinformatie en rapportage](reports-bi-reporting.md).

In dit artikel wordt beschreven hoe u deze analytische functies kunt gebruiken om financiële inzichten te verschaffen.

## Analysebehoefte in de financiële wereld

Bij het in kaart brengen van analysebehoeften in de financiële wereld kan het helpen om een mentaal model te gebruiken dat gebaseerd is op persona's die op een hoog niveau worden beschreven en hun verschillende analysebehoeften.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustratie van verschillende persona's voor analyse" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Mensen in verschillende rollen hebben verschillende behoeften als het om gegevens gaat, en ze gebruiken de gegevens op verschillende manieren. Mensen in de financiële wereld gaan bijvoorbeeld anders met gegevens om dan mensen in de verkoop.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustratie van hoe verschillende persona's verschillende analysebehoeften hebben." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

| Rol              | Gegevensaggregatie  | Typische manieren om gegevens te gebruiken                          | 
|-------------------|-------------------| ----------------------------------------------------- |
|CFO/CEO          | Prestatiegegevens  | KPI's <br> Dashboards <br> Financiële rapporten           |
|Financieel beheer | Trends, overzichten | Ingebouwde managementrapporten <br> Ad-hocanalyse      | 
|Boekhouder         | Gedetailleerde gegevens     | Ingebouwde operationele rapporten <br> Taakgegevens op het scherm |

## Financiële KPI's

Een Key Performance Indicator (KPI) is een meetbare waarde die laat zien hoe effectief u uw doelen bereikt. In de financiële wereld gebruiken mensen vaak de volgende KPI’s om de financiële gezondheid van hun organisatie te monitoren:

- Marge brutowinst
- Nettowinstmarge
- Werkkapitaal
- Current/quick ratio (liquiditeitskengetallen)
- Financiële hefboomeffect, ook wel de aandelenvermenigvuldiger genoemd
- Verhouding schuld/eigen vermogen
- Omzet totale activa
- Rendement op eigen vermogen
- Rendement op activa

<!-- Not ready to publish yet
For more information, see [Financial KPIs in Business Central](bi-finance-kpis.md) 
-->

## Financiële rapportage gebruiken om financiële overzichten en KPI’s te produceren

De functie **Financiële rapporten** geeft u inzichten in de financiële gegevens die in uw rekeningschema zijn opgeslagen. U kunt financiële rapporten instellen om cijfers in grootboekrekeningen (GB) te analyseren en grootboekposten te vergelijken met budgetposten. De resultaten worden weergegeven in grafieken en rapporten op uw startpagina, zoals het cashflowdiagram, en de rapporten Resultatenrekening en Balans.

Dimensies spelen een belangrijke rol bij bedrijfsinformatie. Een dimensie bestaat uit gegevens die u kunt toevoegen aan een post als een parameter. Met dimensies kunt u posten groeperen die vergelijkbare kenmerken hebben, zodat ze gemakkelijker te analyseren zijn. Bijvoorbeeld klanten, regio's, producten en verkopers. U gebruikt dimensies ook wanneer u analyseweergaven definieert en wanneer u financiële rapporten maakt. Zie [Werken met dimensies](finance-dimensions.md) voor meer informatie.

> [!TIP]
> Als snelle manier om transactiegegevens te analyseren kunt u totalen in het rekeningschema en alle posten op de pagina's **Posten** filteren op dimensies. Zoek de actie **Dimensiefilter instellen**.  

De volgende tabel beschrijft een reeks taken in financiële rapportage, met koppelingen naar de artikelen waarin deze worden beschreven.  

| Tot | Zie |
| --- | --- |
| Nieuwe financiële rapporten maken voor financiële overzichten voor rapportage of voor weergave als grafieken.| [Financiële rapporten voorbereiden met financiële gegevens en rekeningcategorieën](bi-how-work-account-schedule.md)|
| Gebruik statistiekrekeningen om informatie in financiële rapporten aan te vullen. Met statistiekrekeningen kunt u statistieken toevoegen die zijn gebaseerd op niet-transactionele gegevens. U kunt de niet-transactionele gegevens toevoegen als op cijfers gebaseerde eenheden, zoals het personeelsbestand, het aantal vierkante meters of het aantal klanten met achterstallige rekeningen. | [Gegevens analyseren met statistiekrekeningen](bi-use-statistical-accounts.md) |
| Meer informatie over hoe u een nieuw financieel rapport kunt instellen via voorbeelden. | [Procedure: financiële rapporten gebruiken voor een cashflowprognose](walkthrough-making-cash-flow-forecasts-by-using-account-schedules.md) |
| Uw financiële prestaties analyseren door KPI's (Key Performance Indicators) in te stellen op basis van financiële rapporten, en die vervolgens publiceren als webservices. De gepubliceerde KPI's voor financiële rapporten kunnen worden weergegeven op een website of naar Microsoft Excel worden geïmporteerd met OData-webservices. |[KPI-webservices instellen en publiceren op basis van financiële rapporten](bi-how-to-set-up-and-publish-kpi-web-services-based-on-account-schedules.md) |
| Weergaven instellen om gegevens te analyseren met dimensies.|[Gegevens analyseren per dimensie](bi-how-analyze-data-dimension.md)|
| Nieuwe analyselijsten te maken voor verkopen, inkopen en voorraad en om analysesjablonen in te stellen. |[Analyserapporten maken](bi-how-create-analysis-views-reports.md)|

## Financiële rapportage verwerken voor verschillende bedrijfseenheden of rechtspersonen

Sommige organisaties gebruiken [!INCLUDE [prod_short](includes/prod_short.md)] in meerdere bedrijfsunits of rechtspersonen. Andere gebruiken [!INCLUDE [prod_short](includes/prod_short.md)] in dochterondernemingen die moeten rapporteren aan moederorganisaties. [!INCLUDE [prod_short](includes/prod_short.md)] geeft accountants tools waarmee ze grootboekposten van twee of meer bedrijven (dochterondernemingen) kunnen overbrengen naar een geconsolideerd bedrijf.  

Ga naar [Bedrijfsconsolidatie](finance-consolidated-company-reporting.md) voor meer informatie.

## Adhoc-analyse van financiële gegevens

Soms hoeft u alleen maar te controleren of de getallen correct zijn, of snel een cijfer bevestigen. De volgende functies zijn ideaal voor ad-hocanalyses:

- Gegevensanalyse op grootboeklijstpagina´s
- Openen in Excel

Met de functie Gegevensanalyse kunt u een lijstpagina openen, zoals voor grootboekposten, grootboekposten voor vaste activa, chequeposten of grootboekposten voor bankrekeningen, de analysemodus openen en vervolgens gegevens naar eigen inzicht groeperen, filteren en draaien.

:::image type="content" source="media/data-analysis-gl-entries.png" alt-text="Voorbeeld van hoe u gegevensanalyse uitvoert op de pagina Grootboekposten." lightbox="media/data-analysis-gl-entries.png":::

Op dezelfde manier kunt u de actie **Openen in Excel** gebruiken om een lijstpagina voor grootboekposten te openen, de lijst optioneel te filteren op een subset van de gegevens en vervolgens Excel te gebruiken om met de gegevens te werken. Bijvoorbeeld door gebruik te maken van functies zoals Gegevens analyseren, Wat-als-analyse of Prognoseblad.

:::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Voorbeeld van hoe u gegevensanalyse uitvoert op de gegevens van grootboekposten met Excel." lightbox="media/open-in-excel-gl-entries.png":::

> [!TIP]
> Als u OneDrive configureert voor systeemfuncties, wordt de Excel-werkmap in uw browser geopend met behulp van Excel voor het web. 


Voor meer informatie over het uitvoeren van ad-hocanalyses van grootboeken, zie [Ad-hocanalyse van financiële gegevens](ad-hoc-analysis-finance.md). 

## Ingebouwde financiële rapporten

[!INCLUDE [prod_short](includes/prod_short.md)] bevat verschillende ingebouwde rapporten, traceerfuncties en tools die auditors of controllers helpen die verantwoordelijk zijn voor rapportage aan de financiële afdeling.

Om een overzicht te krijgen van de beschikbare rapporten kunt u **Alle rapporten** kiezen in het bovenste deelvenster van uw startpagina. Met deze actie gaat u naar de Rolverkenner, die wordt gefilterd op de functies in de optie **Rapport en analyse**. Ga voor meer informatie naar [Rapporten zoeken met de Rolverkenner](ui-role-explorer.md).

:::image type="content" source="media/report-explorer-finance.png" alt-text="Voorbeeld van rapporten over het financiële rolcentrum." lightbox="media/report-explorer-finance.png":::

Er zijn twee soorten ingebouwde rapporten:

- Ontworpen om af te drukken (pdf).
- Ontworpen voor analyse in Excel.

Zie voor meer informatie deze overzichten voor rapporten die relevant zijn voor financiën.

- [Ingebouwde financiële Excel-rapporten](finance-analyze-excel.md)
- [Ingebouwde belangrijke financiële rapporten](finance-reports.md)
- [Ingebouwde vaste-activarapporten](fa-reports.md)
- [Ingebouwde debiteurenrapporten](receivables-reports.md)
- [Ingebouwde crediteurenrapporten](payables-reports.md)

<!-- TODO: add when we have these articles
* [Built-in Cost Accounting reports](cost-accounting-reports.md) 
* [Built-in Cash Management reports](cost-accounting-reports.md) 
* [Built-in Tax and VAT reports](tax-and-vat-reports.md) 
-->

## Financiële taakpagina's op het scherm

[!INCLUDE [prod_short](includes/prod_short.md)] heeft een aantal pagina's waarop u financiële overzichten en taken kunt vinden.

### Grootboekposten en saldi weergeven via de pagina Rekeningschema

Op de pagina Rekeningschema worden alle grootboekrekeningen weergegeven met samengevoegde cijfers die naar het grootboek zijn geboekt. Vanaf deze pagina kunt u het volgende doen:  

- Rapporten weergeven waarin grootboekposten en saldi worden weergegeven.  
- Bekijk een lijst met boekingsgroepen voor die rekening.
- Afzonderlijke debet- en creditsaldo's voor één rekening bekijken.

:::image type="content" source="media/chart-of-accounts-page.png" alt-text="Voorbeeld van hoe op de pagina Rekeningschema financiële inzichten worden weergegeven" lightbox="media/chart-of-accounts-page.png":::

Ga voor meer informatie naar [Het rekeningschema begrijpen](finance-general-ledger.md#the-chart-of-accounts).

### Werkelijke bedragen vergeleken met gebudgetteerde bedragen weergeven voor alle rekeningen en voor verschillende perioden

Als onderdeel van het verzamelen, analyseren en delen van uw bedrijfsgegevens kunt u werkelijke bedragen in vergelijking met gebudgetteerde bedragen weergeven voor alle rekeningen en voor verschillende perioden. U kunt deze vergelijking uitvoeren dit doen via de pagina **Rekeningschema** door de actie **Saldo/Budget (Grootboek)** te kiezen.

Ga voor meer informatie naar [Werkelijke bedragen analyseren in vergelijking met budgetbedragen](bi-how-analyze-actual-versus-budget.md).

### Gegevens analyseren per dimensie

Dimensies zijn waarden waarmee posten worden gecategoriseerd, zodat u ze kunt bijhouden en analyseren in documenten, zoals verkooporders. Dimensies kunnen bijvoorbeeld aangeven tot welk project of welke afdeling een post behoort.  

In plaats van voor elke afdeling en project aparte grootboekrekeningen in te stellen, kunt u dus bijvoorbeeld dimensies gebruiken als basis voor analyse en hoeft u geen ingewikkelde rekeningschemastructuur te maken.

In financiële analyses is een dimensie informatie die u toevoegt aan een grootboekpost als een soort markering. Deze informatie wordt gebruikt om grootboekposten met vergelijkbare kenmerken te groeperen, zoals klanten, regio's, producten en verkopers, en om deze groepen eenvoudig te kunnen opvragen voor analyse. U kunt dimensies gebruiken voor posten in dagboeken, documenten en budgetten. Zie voor meer informatie [Gegevens analyseren per dimensies](bi-how-analyze-data-dimension.md)

### Cashflow analyseren

Op de startpagina Accountant vindt u onder **Rapportageschema** de diagrammen Cashcyclus, Cashflow en Inkomsten en uitgaven waarmee u cashflow kunt analyseren:

- Bekijk cijfers voor een bepaalde periode met de tijdlijnschuifregelaar.
- Filter het diagram door de bron in de legenda te kiezen.
- Wijzig de lengte van de periode of ga naar de vorige of volgende periode door opties te kiezen in de vervolgkeuzelijst Rapportageschema.

:::image type="content" source="media/cashflow-accountant-rolecentre.png" alt-text="Voorbeeld van hoe de cashflow-visuals eruitzien in het rolcentrum voor accountants" lightbox="media/cashflow-accountant-rolecentre.png":::

Als u de prognose naast prognoseposten wilt onderzoeken, kunt u ook het cashflowvoorstel bekijken. U kunt bijvoorbeeld zien hoe de prognose:

- Bevestigde verkopen en inkopen verwerkt.
- Schulden aftrekt en tegoeden optelt.
- Dubbele verkooporders en inkooporders overslaat.

Ga voor meer informatie naar [Cashflow in uw bedrijf analyseren](finance-analyze-cash-flow.md).

## Zie ook

[Financiële rapportage verwerken voor verschillende bedrijfseenheden of rechtspersonen](finance-consolidated-company-reporting.md)  
<!-- [Financial KPIs in Business Central](bi-finance-kpis.md)    -->
[Financiële rapporten voorbereiden met financiële gegevens en rekeningcategorieën](bi-how-work-account-schedule.md)  
[Adhoc-analyse van financiële gegevens](ad-hoc-analysis-finance.md)   
[Het rekeningschema begrijpen](finance-general-ledger.md#the-chart-of-accounts)  
[Ingebouwde financiële Excel-rapporten](finance-analyze-excel.md)  
[Ingebouwde belangrijke financiële rapporten](finance-reports.md)  
[Ingebouwde vaste-activarapporten](fa-reports.md)  
[Ingebouwde debiteurenrapporten](receivables-reports.md)  
[Ingebouwde crediteurenrapporten](payables-reports.md)  
[Overzicht van financiën](finance.md)  
[Overzicht van analyses, bedrijfsinformatie en rapportage](reports-bi-reporting.md)   
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
