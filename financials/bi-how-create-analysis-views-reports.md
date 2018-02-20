---
title: Analyselijsten maken| Microsoft Docs
description: Beschrijft hoe u nieuwe analyselijsten maakt voor verkopen, inkopen en voorraad, en analysesjablonen instelt.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 378c3d2b0429390c303c723dbfafd07c531b3958
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
#  <a name="create-analysis-reports"></a>Analyselijsten maken
Verkoopmanagers moeten de omzet, de brutowinst en andere belangrijke indicatoren voor verkoopprestaties regelmatig analyseren. Inkopers zijn meer geïnteresseerd in de dynamiek van inkoopvolumes, prestaties van leveranciers en inkoopprijzen. Logistieke managers zijn gebaat bij gegevens over de omloopsnelheid van de voorraad, analyses van voorraadverplaatsingen en statistieken over de voorraadwaarde.  

Met analyselijsten kunt u persoonlijke lijsten genereren op basis van records van geboekte transacties, bijvoorbeeld verkoop, inkoop, transfers en voorraadherwaarderingen. In persoonlijke lijsten kunt u de brongegevens, die worden afgeleid van artikelposten (met bijbehorende waardeposten), combineren, vergelijken en presenteren op de door u gewenste manier. In deze zin lijkt de analyselijst in grote mate op een draaitabelrapport in Microsoft Excel.  

In een persoonlijke lijst kunt u zich richten op de totale omzet (in bedragen en in verkochte aantallen), brutowinst en brutowinstmarge van uw belangrijkste klanten in de lopende maand. U kunt deze cijfers vergelijken met de resultaten van voorgaande maanden of van dezelfde maand van vorig jaar en afwijkingen berekenen. Dit kan allemaal in één weergave, met de mogelijkheid te navigeren naar de oorzaak van geïdentificeerde probleemgebieden door de vervolgkeuzeknop te kiezen om toegang te krijgen tot details op het niveau van afzonderlijke transacties.  

De analyselijst bestaat uit regels met de te analyseren objecten (bijvoorbeeld klanten, klantgroepen, verkopers, enzovoort) en de analyseparameters. Dat wil zeggen: de wijze waarop u het object in de bijbehorende kolommen wilt analyseren (bijvoorbeeld winstberekeningen, periodieke vergelijkingen van totale omzet en volumes of periodieke vergelijkingen van werkelijke en gebudgetteerde cijfers).

Naast analyselijsten kunt u soortgelijke informatie maken en weergeven in analyseweergaven, die zijn gebaseerd op dimensies. Zie voor meer informatie [Gegevens analyseren per dimensies](bi-how-analyze-data-dimension.md).

## <a name="example"></a>Opmerking  
U kunt bijvoorbeeld de volgende regels instellen:  
- Computers  
- Monitoren  
- Reserveonderdelen  

Vervolgens kunt u de volgende kolommen instellen:  

- Omzet lopende maand  
- Omzet vorige maand  
- % van omzet vorige maand  

## <a name="setting-up-line-and-column-layouts"></a>Regel- en kolomindelingen instellen  
 In het venster **Analyserapport** kunt u afhankelijk van uw instellingen verschillende regel- en kolomindelingen bekijken, volgens wat u hebt ingesteld. U stelt uw regels of regelsjablonen in het venster **Analyseregelsjablonen** in. In dit venster kunt u de naam van de lijst definiëren en de objecten die u in de regels van de lijst wilt weergeven. U stelt de kolommen in het venster **Analysekolomsjablonen** in. In dit venster kunt u de naam van de kolomsjabloon definiëren en de analyseparameters die u in de kolommen van de lijst wilt weergeven. Iedere regel in het venster **Analysekolomsjablonen** staat voor een kolom in de lijst. Analyseregels en analysekolommen zijn niet aan elkaar gekoppeld.  

Op basis van de regels en de kolommen die u hebt ingesteld, wordt het resultaat van de lijst in het venster **Analyselijst** opgesteld met behulp van een matrix. Een voorbeeld:  

| |Omzet lopende maand|Omzet vorige maand|% van omzet vorige maand|  
|-|-|-|-|  
|Computers| | | |  
|Monitoren| | | |  
|Reserveonderdelen| | | |  
|Totaal| | | |  

 U kunt één set met regels en verschillende sets met kolomindelingen instellen, bijvoorbeeld om lijsten per maand en per jaar weer te geven.

 ## <a name="to-set-up-analysis-column-templates"></a>Analysekolomsjablonen instellen
De volgende procedure is gebaseerd op analyseweergaven voor verkopen. De stappen lijken hierop voor inkoop- en voorraadanalyseweergaven.

In een analyselijst worden de analyseparameters als kolommen weergegeven. Met een analysekolomsjabloon kunt u aangeven welke kolommen u in de analyselijst wilt opnemen.  

De regels op een sjabloon vertegenwoordigen stuk voor stuk de analysekolommen die u in de analyselijst ziet. Als u een kolom wilt definiëren, moet u een code voor het soort analyse aan een regel toewijzen. Deze code voor het soort analyse bepaalt het type brongegevens in de artikelposten waarop de analyse wordt gebaseerd. Brongegevens omvatten kosten, totale omzet of aantal en hun bijbehorende waardeposten. U kunt zoveel kolomsjablonen instellen als u wilt en deze vervolgens gebruiken om nieuwe analyselijsten te maken.    

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Analysekolomsjablonen verkoop** in en klik vervolgens op de gerelateerde koppeling.  
2. Selecteer de eerste lege regel en vul de benodigde velden in.
3. Kies de actie **Kolommen**.  
4. Geef in de velden in het venster **Analysekolommen** op welke kolommen u in de analyselijst wilt opnemen.  

    > [!NOTE]  
>   Als u een kolom wilt definiëren, moet u het veld **Code soort analyse** invullen voor alle soorten kolommen, behalve **Formule**. Stel de analysetypecodes in het venster **Soorten analyse** in.  

    **Opmerking**. Als u **Artikelposten** selecteert in het veld **Boekingssoort grootboek**, worden de werkelijke cijfers van de artikelpost gekopieerd. Selecteert u hier **Artikelbudgetposten**, dan worden de gebudgetteerde cijfers van het budget gekopieerd.  
5.  Kies de knop **OK** om de wijzigingen op te slaan.  

## <a name="to-set-up-analysis-line-templates"></a>Analyseregelsjablonen instellen  
De volgende procedure is gebaseerd op analyserapporten voor verkopen. De stappen lijken hierop voor inkoop- en voorraadanalyserapporten.

De objecten die u wilt analyseren worden in een analyselijst op de regels weergegeven. Met een analyseregelsjabloon kunt u aangeven welke regels u in de analyselijst wilt opnemen.  

Een sjabloon bevat een set regels die de analyseregels in de analyselijst vertegenwoordigen. Per regel kunt u één of meerdere artikelen, klanten, leveranciers of groepen opgeven. U kunt ook een formule invoegen om de bovenliggende regels te totaliseren. U kunt zoveel regelsjablonen maken als u wilt en deze vervolgens gebruiken om nieuwe analyselijsten te maken.    

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Analyseregelsjablonen verkoop** in en klik vervolgens op de gerelateerde koppeling.  
2. Selecteer de eerste lege regel en vul de benodigde velden in.
3. Kies de actie **Regels**.  
4. Maak in het venster **Analyseregels** regels voor de artikelen, klanten, leveranciers of verkopers waarvan of voor wie u cijfers in de analyselijst wilt bekijken. U bent verplicht de velden **Soort**, **Reeks** en **Omschrijving** in te vullen.  

> [!NOTE]  
>   Als u per artikel, klant, enzovoort een groot aantal afzonderlijke regels wilt maken, kunt u ook een invoegoptie selecteren. Alle betreffende velden op de regel worden dan ingevuld.  Indien nodig kunt u de regels vervolgens handmatig bewerken. Om regels in te voegen kiest u de actie **Artikelen invoegen** of **Artikelgroepen invoegen**.  

## <a name="to-create-a-new-sales-analysis-report"></a>Een nieuwe verkoopanalyselijst maken
De volgende procedure is gebaseerd op analyserapporten voor verkopen. De stappen lijken hierop voor inkoop- en voorraadanalyserapporten.

Met verkoopanalyselijsten kunt u de dynamiek van uw omzet analyseren op basis van geselecteerde indicatoren voor verkoopprestaties, bijvoorbeeld de omzetbedragen en -aantallen, de bijdrage aan de brutowinst en de progressie van de werkelijke verkoop ten opzichte van het budget. U kunt de rapporten ook gebruiken om de gemiddelde verkoopprijs te analyseren en de prestaties van het verkoopteam te evalueren.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verkoopanalyserapporten** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies in het venster **Analyserapport verkoop** de actie **Nieuw**.
3. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Kies de actie **Analyserapport bewerken**.
5. Kies in het venster **Verkoopanalyserapport** de actie **Matrix weergeven**.  

> [!NOTE]  
>   Optioneel kunt u rapporten maken op basis van een combinatie van regel- en kolomsjablonen en hier unieke namen aan toewijzen. Als u dat doet, hoeft u bij het selecteren van een lijstnaam geen regel- en kolomsjablonen te selecteren in het venster **Verkoopanalyselijst**. Nadat u een rapportnaam hebt gekozen, kunt u regel- en kolomsjablonen onafhankelijk van elkaar wijzigen en de rapportnaam later weer selecteren om de oorspronkelijke combinatie te herstellen.

## <a name="see-also"></a>Zie ook
[Bedrijfsinformatie](bi.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

