---
title: Analyserapporten maken
description: 'Beschrijft hoe u nieuwe analyselijsten maakt voor verkopen, inkopen en voorraad, en analysesjablonen instelt.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 04/08/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Analyserapporten maken

Verkoopmanagers moeten de omzet, de brutowinst en andere belangrijke indicatoren voor verkoopprestaties regelmatig analyseren. Inkopers zijn meer geïnteresseerd in de dynamiek van inkoopvolumes, prestaties van leveranciers en inkoopprijzen. Logistieke managers zijn gebaat bij gegevens over de omloopsnelheid van de voorraad, analyses van voorraadverplaatsingen en statistieken over de voorraadwaarde. Er is dus geen analyselijst die voor alle doeleinden kan worden gebruikt.

U kunt analyselijsten aanpassen op basis van uw records van geboekte transacties, bijvoorbeeld verkoop, inkoop, transfers en voorraadherwaarderingen. In persoonlijke lijsten kunt u de brongegevens, die worden afgeleid van artikelposten (met bijbehorende waardeposten), combineren, vergelijken en presenteren op de door u gewenste manier. In dit verband lijkt de analyselijst op een draaitabelrapport in Microsoft Excel.  

U kunt bijvoorbeeld een persoonlijke lijst maken die zich richt op uw belangrijkste accounts voor wat betreft totale productomzet in verkochte bedragen en hoeveelheden, brutowinst en brutowinstpercentage gedurende de huidige maand. Dan kunt u die cijfers laten vergelijken met de resultaten van voorgaande maanden of dezelfde maand vorig jaar, en afwijkingen laten berekenen. Dit kan allemaal in één weergave, wat u de mogelijkheid geeft om te navigeren naar de oorzaak van geïdentificeerde probleemgebieden en zelfs door de vervolgkeuzeknop te kiezen om in te zoomen op details tot op het niveau van afzonderlijke transacties.  

De analyselijst bestaat uit de te analyseren objecten (bijvoorbeeld klanten, klantgroepen, verkopers enzovoort, weergegeven als regels) en de analyseparameters. Dat is de wijze waarop u het object wilt analyseren (bijvoorbeeld winstberekeningen, periodieke vergelijkingen van totale omzet en volumes of periodieke vergelijkingen van werkelijke en gebudgetteerde cijfers, weergegeven als kolommen). 

Naast analyselijsten kunt u soortgelijke informatie maken en weergeven in analyseweergaven (gebaseerd op dimensies). Meer informatie vindt u op [Gegevens analyseren per dimensie](bi-how-analyze-data-dimension.md).

## Opmerking

U kunt deze regels instellen (objecten die u wilt analyseren):  

- Computers  
- Monitoren  
- Onderdelen  

Vervolgens kunt u deze kolommen instellen (hoe u de objecten wilt laten analyseren):  

- Omzet huidige maand  
- Omzet vorige maand  
- % van omzet vorige maand  

## Regel- en kolomindelingen instellen

Op de pagina **Analyselijst** kunt u afhankelijk van uw instellingen verschillende regel- en kolomindelingen bekijken die u instelt op de:

* pagina **Analyseregelsjablonen** waar u de naam van de lijst kunt definiëren en de objecten die u in de regels van de lijst wilt weergeven, en de
* pagina **Analysekolomsjablonen** waar u de naam van de kolomsjabloon kunt definiëren en de analyseparameters die in de kolommen van de lijst worden weergegeven. Elke regel op deze pagina staat voor een kolom in de lijst. 

Analyseregels en analysekolommen zijn niet aan elkaar gekoppeld.  

Op basis van de regels en de kolommen die u hebt ingesteld, aggregeert [!INCLUDE[prod_short](includes/prod_short.md)] het resultaat van uw lijst op de pagina **Analyselijst**, zoals getoond in de volgende tabel.  

|- |Omzet lopende maand|Omzet vorige maand|% van omzet vorige maand|  
|-|-|-|-|  
|Computers| | | |  
|Monitoren| | | |  
|Reserveonderdelen| | | |  
|Totaal| | | |  

U kunt, bijvoorbeeld, één groep met regels en verschillende groepen met kolomindelingen instellen, bijvoorbeeld om lijsten per maand en per jaar weer te geven.

## Analysekolomsjablonen instellen

De volgende procedure is gebaseerd op verkoopanalyseweergaven. De stappen lijken hierop voor inkoop- en voorraadanalyseweergaven.

Een analysekolomsjabloon bevat een set regels, die elk een analysekolom vertegenwoordigen die u in de analyselijst wilt zien. Als u een kolom wilt definiëren, moet u een code voor het soort analyse aan een regel toewijzen. Deze code voor het soort analyse bepaalt het type brongegevens in de artikelposten waarop de analyse wordt gebaseerd. Brongegevens kun kosten, totale omzet of hoeveelheid bevatten en hun bijbehorende waardeposten. U kunt zoveel kolomsjablonen instellen als u wilt en deze vervolgens gebruiken om nieuwe analyselijsten te maken.    

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopkolomsjablonen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de eerste lege regel en vul de benodigde velden in.
3. Kies de actie **Kolommen**.  
4. Vul de velden op de pagina **Analysekolommen** in om op te geven welke kolommen u in de analyselijst wilt.  

    > [!NOTE]  
    > Als u een kolom wilt definiëren, moet u het veld **Code soort analyse** invullen voor alle soorten kolommen, behalve **Formule**. Stel de analysetypecodes op de pagina **Soorten analyse** in.  
    
    Als u **Artikelposten** selecteert in het veld **Boekingssoort grootboek**, worden de werkelijke cijfers van de artikelpost ook gekopieerd. Selecteert u hier **Artikelbudgetposten**, dan worden de gebudgetteerde cijfers van het budget gekopieerd.  
5. Kies **OK** om de wijzigingen op te slaan.  

## Analyseregelsjablonen instellen

De volgende procedure is gebaseerd op analyserapporten voor verkopen. De stappen lijken hierop voor inkoop- en voorraadanalyserapporten.

Een analyseregelsjabloon bevat een set regels, die elk een analyseregel vertegenwoordigen die u in de analyselijst wilt zien. Per regel kunt u één of meerdere artikelen, klanten, leveranciers of groepen opgeven. U kunt ook een formule invoegen om de bovenliggende regels te totaliseren. U kunt zoveel regelsjablonen maken als u wilt en deze vervolgens gebruiken om nieuwe analyselijsten te maken.   

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopregelsjablonen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de eerste lege regel en vul de benodigde velden in.
3. Kies de actie **Regels**.  
4. Maak op de pagina **Analyseregels** regels voor de artikelen, klanten, leveranciers of verkopers waarvan of voor wie u cijfers in de analyselijst wilt bekijken. U bent verplicht de velden **Soort**, **Reeks** en **Omschrijving** in te vullen.  

> [!NOTE]  
> Als u per artikel, klant, enzovoort een groot aantal afzonderlijke regels wilt maken, kunt u ook de juiste invoegoptie selecteren. Alle betreffende velden op de regel worden dan ingevuld. Indien nodig kunt u de regels vervolgens handmatig bewerken. Om regels in te voegen kiest u de actie **Artikelen invoegen** of **Artikelgroepen invoegen**.  

## Een nieuwe verkoopanalyselijst maken

De volgende procedure is gebaseerd op analyserapporten voor verkopen. De stappen lijken hierop voor inkoop- en voorraadanalyserapporten.

Met analyselijsten kunt u de dynamiek van uw omzet analyseren op basis van indicatoren voor verkoopprestaties, zoals de omzetbedragen en -aantallen, de bijdrage aan de brutowinst of de progressie van de werkelijke verkoop ten opzichte van het budget. U kunt de analyselijsten ook gebruiken om de gemiddelde verkoopprijs te analyseren en de prestaties van het verkoopteam te evalueren.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopanalyselijsten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Analyserapport verkoop** de actie **Nieuw**.
3. Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Kies de actie **Analyserapport bewerken**.
5. Kies op de pagina **Verkoopanalyserapport** de actie **Matrix weergeven**.  

> [!NOTE]  
> Optioneel kunt u rapporten maken op basis van een combinatie van regel- en kolomsjablonen en hier unieke namen aan toewijzen. Als u hiervoor kiest, hoeft u geen regel- en kolomsjablonen te selecteren op de pagina **Verkoopanalyselijst**. Nadat u een rapportnaam hebt gekozen, kunt u regel- en kolomsjablonen onafhankelijk van elkaar wijzigen en de rapportnaam later weer selecteren om de oorspronkelijke combinatie te herstellen.

## Zie ook

[Financiële bedrijfsinformatie](bi.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
