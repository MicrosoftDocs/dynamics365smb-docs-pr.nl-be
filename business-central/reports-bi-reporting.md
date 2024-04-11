---
title: 'Overzicht van analyses, bedrijfsinformatie en rapportage'
description: 'Biedt een overzicht van alle analyses, bedrijfsinformatie en rapportagefuncties die worden ondersteund in Business Central.'
author: KennieNP
ms.topic: get-started
ms.devlang: al
ms.search.keywords: feature overview
ms.reviewer: bholtorf
ms.date: 09/22/2022
ms.author: kepontop
ms.service: dynamics-365-business-central
---

# Overzicht van analyses, bedrijfsinformatie en rapportage

Kleine en middelgrote bedrijven vertrouwen op ingebouwde analyse- en rapportagemogelijkheden die ze kant-en-klaar kunnen gebruiken om hun bedrijf bij te houden. [!INCLUDE[prod_short](includes/prod_short.md)] biedt rapporten en analysetools die basis- en complexe bedrijfsprocessen voor dergelijke organisaties bestrijken. U kunt ook ad-hocanalyses rechtstreeks vanaf uw startpagina uitvoeren.  

## Analysebehoefte in organisaties

Bij het in kaart brengen van analysebehoeften in organisaties kan het helpen om een mentaal model te gebruiken dat gebaseerd is op persona's die op een hoog niveau worden beschreven en hun verschillende analysebehoeften.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg" alt-text="Illustratie van verschillende persona's voor analyse" lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas.svg":::

Het model is gebaseerd op het feit dat verschillende rollen in een organisatie verschillende behoeften hebben als het om data gaat. Hoe hoger een rol in het organigram wordt geplaatst, hoe meer geaggregeerde gegevens iemand in de rol nodig heeft om zijn werk te doen.

Rollen hebben vaak de voorkeuren om data te consumeren en te analyseren, die het niveau van data-aggregatie aangeven dat ze nodig hebben.

:::image type="content" source="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg" alt-text="Illustratie van hoe verschillende persona's verschillende analysebehoeften hebben." lightbox="/dynamics365/business-central/dev-itpro/developer/media/analytics-personas-scenarios.svg":::

Gebruik de volgende secties voor meer informatie over manieren om gegevens te gebruiken van [!INCLUDE[prod_short](includes/prod_short.md)]:

- Financiële rapporten
- KPI's en dashboards
- Ad-hocanalyse
- Rapporten

## Financiële rapporten gebruiken om financiële overzichten en KPI’s te produceren

Financiële rapporten geven u inzicht in de financiële gegevens die in uw rekeningschema (COA) zijn opgeslagen. U kunt financiële rapporten instellen om cijfers in grootboekrekeningen (GB) te analyseren en grootboekposten te vergelijken met budgetposten.

:::image type="content" source="media/acc_schedule_13_columns.jpg" alt-text="Schermopname van een financieel rapport." lightbox="media/acc_schedule_13_columns.jpg":::

Dimensies spelen een belangrijke rol bij bedrijfsinformatie. Een dimensie bestaat uit gegevens die u kunt toevoegen aan een post als een parameter. Met dimensies kunt u invoergegevens groeperen met vergelijkbare kenmerken, zoals klanten, regio's, producten en verkopers, en kunt u deze groepen eenvoudig ophalen voor analyse. U kunt dimensies onder andere ook gebruiken wanneer u analyseweergaven definieert en wanneer u financiële rapporten maakt. Zie [Werken met dimensies](finance-dimensions.md) voor meer informatie.

Voor meer informatie over financiële overzichten en KPI's gaat u naar [Financiële rapportage gebruiken om financiële overzichten en KPI's te produceren](bi.md).

## KPI's gebruiken om uw bedrijfsdoelen te halen

Een Key Performance Indicator (KPI) is een meetbare waarde die laat zien hoe effectief u uw doelen bereikt. Beschouw KPI's als de scorekaart van uw bedrijf, een manier om te meten of u uw doelstellingen wel haalt.

Door KPI's te identificeren en bij te houden, weet u of uw bedrijf op de goede weg is, of dat u van koers moet veranderen. Wanneer ze op de juiste manier worden gebruikt, zijn KPI's krachtige hulpmiddelen die u helpen bij het volgende:

- Bewaak de financiële gezondheid van het bedrijf.
- Meet de voortgang ten opzichte van strategische doelen.
- Spoor problemen vroegtijdig op.
- Pas tijdig de tactieken aan.
- Motiveer teamleden.
- Neem sneller betere beslissingen.

Meer informatie over KPI's vindt u in [KPI's gebruiken om uw bedrijfsdoelen te halen](./analytics-about-kpis.md)

## Ad-hocgegevensanalyse

Soms wilt u misschien gewoon controleren of de cijfers kloppen, snel een hypothese over het bedrijf bevestigen of ontkrachten, of op zoek gaan naar afwijkingen in uw financiële gegevens. Voor ad-hocanalyses beschikt u mogelijk niet over een ingebouwd rapport dat u helpt uw ​​vragen te beantwoorden. Gebruik deze twee functies voor ad-hocanalyses:

- Gegevensanalyse op grootboeklijstpagina´s
- Openen in Excel

Met de functie Gegevensanalyse kunt u een lijstpagina openen, zoals de pagina's Grootboekposten of Klantenposten, de analysemodus invoeren en vervolgens gegevens naar eigen inzicht groeperen, filteren en draaien. 

:::image type="content" source="media/data-analysis-gl-entries.png" alt-text="Voorbeeld van hoe u gegevensanalyse uitvoert op de pagina Grootboekposten." lightbox="media/data-analysis-gl-entries.png":::

Op dezelfde manier kunt u de actie **Openen in Excel** gebruiken om een lijstpagina te openen, de lijst optioneel te filteren op een subset van de gegevens en vervolgens Excel te gebruiken om met de gegevens te werken. Bijvoorbeeld door gebruik te maken van functies zoals Gegevens analyseren, Wat-als-analyse of Prognoseblad.

:::image type="content" source="media/open-in-excel-gl-entries.png" alt-text="Voorbeeld van hoe u gegevensanalyse uitvoert op de gegevens van grootboekposten met Excel." lightbox="media/open-in-excel-gl-entries.png":::

> [!TIP]
> Als u OneDrive configureert voor systeemfuncties, wordt de Excel-werkmap in uw browser geopend met behulp van Excel voor het web.

Ga voor meer informatie over ad-hocanalyses naar [Ad-hocgegevensanalyse](reports-adhoc-analysis.md).

## Rapporten

Een rapport in [!INCLUDE[prod_short](includes/prod_short.md)] verzamelt informatie op basis van een gespecificeerde set criteria. Rapoorten organiseren en presenteren de informatie in een gemakkelijk te lezen formaat dat u kunt gebruiken in Excel, afdrukken of opslaan als een bestand.  

Een voorbeeld van een interactief rapport in Excel is het rapport **Vervallen vorderingen** waarmee u kunt analyseren wat uw klanten u verschuldigd zijn en wanneer betalingen verschuldigd zijn.

:::image type="content" source="media/aged-accounts-receivables-excel.png" alt-text="Voorbeeld van het interactieve rapport Vervallen vorderingen in Excel." lightbox="media/aged-accounts-receivables-excel.png":::

Voor vervallen vorderingen bevat [!INCLUDE[prod_short](includes/prod_short.md)] ook een rapport dat bedoeld is om af te drukken. De mogelijkheid om af te drukken is handig als u de gegevens liever in een .pdf-bestand heeft.

:::image type="content" source="media/aged-accounts-receivables-pdf.png" alt-text="Voorbeeld van het rapport Vervallen vorderingen in pdf." lightbox="media/aged-accounts-receivables-pdf.png":::

[!INCLUDE[prod_short](includes/prod_short.md)] wordt geleverd met meer dan 300 ingebouwde rapporten die u kunt gebruiken om uw bedrijfsprocessen te ondersteunen met inzichten op basis van gegevens. Om een ​​snel overzicht te krijgen van alle rapporten die beschikbaar zijn voor uw rol, kunt u de rapportverkenner openen vanuit het rolcentrum, alle lijstpagina's en vanuit  **Vertel het me**.

:::image type="content" source="media/report-explorer-finance.png" alt-text="Voorbeeld van hoe de rapportverkenner alle rapporten voor een rol toont." lightbox="media/report-explorer-finance.png":::

Voor meer informatie over het gebruik van de rapportverkenner om alle ingebouwde rapporten te bekijken, gaat u naar [Rapporten verkennen per rol](ui-role-explorer.md).

In de volgende tabel vindt u artikelen over het gebruik van ingebouwde rapporten in [!INCLUDE[prod_short](includes/prod_short.md)].

| Tot  | Zie |
| --- | --- |
| Leer rapporten gebruiken (bladwijzer maken, uitvoeren, afdrukken, plannen en de indeling wijzigen). | [Rapporten gebruiken in het dagelijkse werk](reports-use-reports.md) |
| Meer informatie over de ingebouwde rapporten vindt u in [!INCLUDE[prod_short](includes/prod_short.md)]. |[Rapportoverzicht](reports-available-reports.md)| 
| Gebruik de Rapportverkenner om alle ingebouwde rapporten te bekijken. | [Rapporten per rol verkennen](ui-role-explorer.md) |

## Externe bedrijfsinformatie- en rapportagetools

Als u liever bedrijfsinformatietools gebruikt die niet zijn ingesloten in [!INCLUDE[prod_short](includes/prod_short.md)], vindt u in de volgende tabel links naar hulpprogramma's en manieren om externe tools te gebruiken.

| Tot  | Zie |
| --- | --- |
| Power BI gebruiken met Business Central-gegevens | [Power BI gebruiken met Business Central](admin-powerbi.md) |
| Externe bedrijfsinformatietools integreren met [!INCLUDE[prod_short](includes/prod_short.md)].| [Externe bedrijfsinformatietools](reports-external-analysis.md) |
| Gegevens extraheren naar data warehouses of data lakes| [Gegevens extraheren naar datawarehouses of data lakes](/dynamics365/business-central/dev-itpro/performance/performance-developer#efficient-extracts-to-data-lakes-or-data-warehouses) |
| Business Central-gegevens analyseren met Microsoft Fabric| [Inleiding bij Microsoft Fabric en Business Central](admin-fabric.md) |
| Gegevens lezen uit Business Central met API's | [Business Central API v2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/) |

## Zie ook

[Financiële rapportage gebruiken om financiële overzichten en KPI’s te produceren](bi.md)  
[KPI's gebruiken om uw bedrijfsdoelen te halen](analytics-about-kpis.md)  
[Ad-hocgegevensanalyse uitvoeren](reports-adhoc-analysis.md)  
[Rapporten gebruiken in uw dagelijkse werk](reports-use-reports.md)  
[Overzicht van ingebouwde rapporten](reports-available-reports.md)  
[Rapporten per rol verkennen](ui-role-explorer.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
