---
title: De Business Central-apps gebruiken in Power BI
description: 'Inzicht, bedrijfsinformatie en KPI''s krijgen uit uw Business Central-gegevens is gemakkelijk met Business Central-apps voor Power BI.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 09/07/2023
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# <a name="use-the--apps-in-power-bi"></a>De [!INCLUDE [prod_short](includes/prod_short.md)]-apps gebruiken in Power BI

> **GELDT VOOR:** [!INCLUDE [prod_long](includes/prod_long.md)] online 

[!INCLUDE [prod_long](includes/prod_long.md)] publiceert de volgende Power BI-apps, die gedetailleerde dashboards bieden voor het weergeven van gegevens:

- [!INCLUDE [prod_long](includes/prod_long.md)] - CRM  
- [!INCLUDE [prod_long](includes/prod_long.md)] - Finance  
- [!INCLUDE [prod_long](includes/prod_long.md)] - Sales

## <a name="overview"></a>Overzicht

Elke app bevat verschillende rapporten waarin u gegevens kunt analyseren met behulp van onder andere de volgende functies:

- Kies een dashboardfunctie om een van de onderliggende rapporten weer te geven.  
- Filter het rapport of voeg velden toe die u wilt controleren.  
- Maak een aangepaste weergave vast op het dashboard om de gegevens te kunnen blijven volgen.  
  U kunt gegevens handmatig vernieuwen en u kunt een schema voor vernieuwen instellen. Zie voor meer informatie [Gepland vernieuwen configureren](/power-bi/refresh-scheduled-refresh).  

De apps zijn ontworpen om te werken met gegevens van elk bedrijf in [!INCLUDE[prod_short](includes/prod_short.md)]. Wanneer u de Power BI-app installeert, geeft u een of meer parameters op om verbinding te maken met uw [!INCLUDE [prod_short](includes/prod_short.md)].  

> [!NOTE]
> U kunt ook uw eigen rapporten en dashboards in Power BI samenstellen op basis van de [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens. Zie voor meer informatie [Uw bedrijfsgegevens verbinden met Power BI](across-how-use-financials-data-source-powerbi.md). 

## <a name="prerequisites"></a>Vereisten

Power BI-apps hebben machtigingen nodig voor toegang tot de tabellen waaruit gegevens worden opgehaald en toegang tot de webservices die worden gebruikt om gegevens op te halen. In de volgende tabel worden de webservices vermeld die voor elke Power BI-app vereist zijn:
    
|App|Webservices |
|--|-------------|
|[!INCLUDE[prod_short](includes/prod_short.md)] – CRM| <ul><li>Opportuniteiten</li><li>Bedrijfsgegevens van weergave van Excel-sjabloon</li><li>Labels van Power BI-rapport</li></ul>|
|[!INCLUDE[prod_short](includes/prod_short.md)] – Finance| <ul><li>PowerBIFinance</li><li>Bedrijfsgegevens van weergave van Excel-sjabloon</li><li>Labels van Power BI-rapport</li></ul>|
|[!INCLUDE[prod_short](includes/prod_short.md)] – Sales| <ul><li>Artikelverkopen per klant</li><li>Verkoopdashboard</li><li>Bedrijfsgegevens van weergave van Excel-sjabloon</li><li>Labels van Power BI-rapport</li></ul>|

> [!TIP] 
> Een eenvoudige manier om de webservices te vinden is te zoeken naar *webservices* in [!INCLUDE[prod_short](includes/prod_short.md)]. Zorg op de pagina **Webservices** dat het veld **Publiceren** is geselecteerd voor de hierboven genoemde webservices. Zie [Een webservice publiceren](across-how-publish-web-service.md) voor meer informatie.

## <a name="get-ready"></a>Bereid u voor

Meld u aan voor de Power BI-service. Als u zich nog niet hebt aangemeld, gaat u naar [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Gebruik wanneer u zich aanmeldt uw zakelijke e-mailadres en wachtwoord.

## <a name="install-a--app-in-power-bi"></a>Een [!INCLUDE[prod_short](includes/prod_short.md)]-app installeren in Power BI

1. Open uw browser, ga naar [https://powerbi.microsoft.com](https://powerbi.microsoft.com) en meld u aan bij uw account.
2. Selecteer **Apps** in het navigatievenster.
    
    De pagina **Apps** wordt weergegeven.

3. Selecteer op de pagina **Apps** **Apps downloaden** in de rechterbovenhoek van de pagina.
    
    De pagina **Power BI-apps** wordt geopend, waar u kunt bladeren naar de apps die beschikbaar zijn voor [!INCLUDE[prod_short](includes/prod_short.md)].

    ![Navigeren om apps op te halen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

> [!TIP] 
> U kunt ook toegang tot het **Power BI-rapport** krijgen vanuit [!INCLUDE [prod_short](includes/prod_short.md)]. Navigeer op uw startpagina naar de sectie Power BI-rapporten en **Rapporten selecteren**. Kies **Services** of **Mijn organisatie** vanuit **Rapporten downloaden**. Nu wordt de Organisatiegalerie in Power BI of Microsoft AppSource geopend met alleen apps die zijn gerelateerd aan [!INCLUDE[prod_short](includes/prod_short.md)].

5. Voer in het vak **Zoeken** de tekst **Dynamics 365 Business Central** in.
6. Selecteer de app die u wilt gebruiken, selecteer **Nu downloaden** en selecteer vervolgens **Installeren**.  

    Na voltooiing is de app beschikbaar via **Apps** in het navigatiemenu in Power BI.

## <a name="connect-the--app-to-your-data"></a>De [!INCLUDE[prod_short](includes/prod_short.md)]-app verbinden met uw gegevens

1. Selecteer onder **Apps** de Business Central-app en selecteer vervolgens **Verbinden**.
2. Voer desgevraagd in de velden **Bedrijfsnaam** en **Omgeving** informatie in over het [!INCLUDE[prod_short](includes/prod_short.md)]-exemplaar waarmee u verbinding wilt maken.

    - Zorg ervoor dat u bij **Bedrijfsnaam** de volledige naam gebruikt en niet de weergavenaam. U vindt de bedrijfsnaam op de pagina **Bedrijven** in [!INCLUDE[prod_short](includes/prod_short.md)]. 
    - Als u nog niet meerdere omgevingen hebt gemaakt, voert u bij **Omgeving** de naam **Productie**.

3. Selecteer **Volgende**.
4. Selecteer **Aanmelden**.
5. Voer desgevraagd de gebruikersnaam en het wachtwoord in om u aan te melden bij [!INCLUDE[prod_short](includes/prod_short.md)].
6. Eenmaal verbonden worden een dashboard en rapporten aan uw Power BI-werkruimte toegevoegd. Wanneer dit is voltooid, bevatten de tegels gegevens uit uw [!INCLUDE[prod_short](includes/prod_short.md)]-bedrijf.

    ![Selecteer Dynamics 365 Business Central en selecteer Nu ophalen.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="fixing-problems"></a>Problemen oplossen

Het Power BI-dashboard is voor zijn gegevens afhankelijk van de gepubliceerde webservices die hierboven worden vermeld. Op het dashboard worden gegevens weergegeven van het voorbeeldbedrijf of van uw eigen bedrijf als u gegevens importeert uit uw huidige financiële oplossing. Als er echter iets verkeerd gaat, biedt deze sectie een oplossing voor de meest voorkomende problemen.  

### <a name="you-dont-have-a-power-bi-account"></a>U hebt geen Power BI-account

Er is geen Power BI-account ingesteld. U moet een licentie hebben om een geldig Power BI-account te verkrijgen. Ook moet u zich eerder hebben aangemeld Power BI om uw Power BI-werkruimte te maken.  

### <a name="message-there-are-no-enabled-reports-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Bericht: Er zijn geen ingeschakelde rapporten. Kies een rapport om een lijst met rapporten te tonen die u kunt weergeven.

Dit bericht verschijnt als het standaardrapport niet kon worden geïmplementeerd in uw Power BI-werkruimte. Of het rapport is geïmplementeerd maar is niet vernieuwd. Als dit probleem zich voordoet, navigeert u naar het rapport in uw Power BI-werkruimte, selecteert u **Gegevensset**, **Instellingen** en werkt u vervolgens de referenties handmatig bij. Nadat de gegevensset met succes is vernieuwd, navigeert u terug naar [!INCLUDE[prod_short](includes/prod_short.md)] en selecteert u handmatig het rapport vanaf de pagina **Rapporten selecteren**.

### <a name="you-need-a-power-bi-pro-license-to-install-the--app-in-power-bi"></a>U hebt een Power BI Pro-licentie nodig om de [!INCLUDE[prod_short](includes/prod_short.md)]-app in Power BI te installeren

U hebt een [Power BI Pro-licentie](/power-bi/service-features-license-type) nodig om uw inhoud te delen en de mensen met wie u deze inhoud deelt, hebben die licentie ook nodig. De inhoud moet zich in een werkruimte in een [Premium-capaciteit](/power-bi/service-premium-what-is) bevinden. Zie voor meer informatie [Manieren om uw werk te delen in Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).  

### <a name="parameter-validation-failed-please-make-sure-all-parameters-are-valid"></a>"Parametervalidatie mislukt; zorg dat alle parameters geldig zijn"

Deze fout geeft aan dat een of meer parameters niet geldig zijn.

- De opgegeven omgevingsparameter komt niet overeen met een bestaande productie- of sandboxomgeving in [!INCLUDE[prod_short](includes/prod_short.md)].
- De opgegeven bedrijfsparameter komt niet overeen met bestaande [!INCLUDE[prod_short](includes/prod_short.md)]-bedrijven. Controleer de bedrijfsnaam op de pagina **Bedrijven** in [!INCLUDE[prod_short](includes/prod_short.md)].
- Als u verbinding maakt met [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, hebt u een URL ingevoerd die niet geldig is. U kunt de URL verifiëren op de pagina **Webservices** in [!INCLUDE[prod_short](includes/prod_short.md)]  
- Er staat geen poort open om het verzoek door uw firewall te laten gaan.

### <a name="cant-sign-in"></a>Kan me niet aanmelden

Als u de fout 'Aanmelding mislukt' krijgt nadat u zich hebt aangemeld met uw [!INCLUDE[prod_short](includes/prod_short.md)]-aanmeldingsgegevens, kan dat een van de volgende oorzaken hebben:

- Het account dat u gebruikt, heeft geen machtigingen voor het ophalen van de [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens uit uw account. Controleer of u machtigingen hebt voor de vereiste gegevens in [!INCLUDE[prod_short](includes/prod_short.md)] en probeer het opnieuw.
- U hebt een ander verificatietype dan Basis geselecteerd als u verbinding maakt met [!INCLUDE[prod_short](includes/prod_short.md)] on-premises.
- U hebt geen geldige gebruikersnaam of wachtwoord ingevoerd.

### <a name="message-your-data-source-cant-be-refreshed-because-the-credentials-are-invalid-please-update-your-credentials-and-try-again"></a>Bericht: uw gegevensbron kan niet worden vernieuwd omdat de aanmeldingsgegevens ongeldig zijn. Werk uw aanmeldingsgegevens bij en probeer het opnieuw

Voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises is het probleem mogelijk dat de OData-URL alleen wordt weergegeven op het lokale netwerk.

### <a name="incorrect-company-name"></a>Onjuiste bedrijfsnaam

Een veel voorkomende fout is de weergavenaam van het bedrijf in te voeren in plaats van de bedrijfsnaam. Als u de bedrijfsnaam wilt vinden, zoekt u naar **Bedrijven**. Gebruik vervolgens het veld **Naam** wanneer u uw bedrijfsnaam invoert.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>De sleutel kwam met geen rijen uit de tabel overeen

Als u een ongeldige bedrijfsnaam invoert tijdens het verbindingsproces, kunt u de foutmelding "De sleutel kwam met geen rijen uit de tabel overeen" krijgen. Geef de juiste bedrijfsnaam op en probeer opnieuw verbinding te maken.

### <a name="historical-data-appears-to-be-missing"></a>Historische gegevens lijken te ontbreken

Als de Power BI-app eenmaal is geïnstalleerd en uw gegevens in Power BI worden weergegeven, merkt u dat niet al uw gegevens worden weergegeven. De gegevenssets worden gefilterd om alleen de voorgaande 365 dagen aan gegevens te retourneren. Deze standaard is aanwezig om de rapporten sneller te maken.  

### <a name="i-only-see-data-for-a-single-company"></a>Ik zie alleen gegevens voor één bedrijf

De Power BI-app toont alleen gegevens van het [!INCLUDE[prod_short](includes/prod_short.md)]-bedrijf dat is gedefinieerd toen de Power BI-app werd geïnstalleerd. Gegevens van extra bedrijven kunnen aan de rapporten worden toegevoegd door nieuwe query's toe te voegen die verschillende bedrijven als gegevensbron gebruiken.  

### <a name="what-now"></a>Wat nu?

- Probeer [een vraag te stellen in het vraag- en antwoordvak](/power-bi/service-q-and-a-tips) boven aan het dashboard.
- [Wijzig de tegels](/power-bi/service-dashboard-edit-tile) in het dashboard.  
- [Selecteer een tegel](/power-bi/service-dashboard-tiles) om het onderliggende rapport te openen.  
- Standaard wordt uw gegevensset niet volgens een schema vernieuwd. U kunt het vernieuwingsschema wijzigen of de gegevensset op aanvraag proberen te vernieuwen met de opdracht **Nu vernieuwen**. Zie voor meer informatie [Gepland vernieuwen configureren](/power-bi/refresh-scheduled-refresh).

## <a name="see-also"></a>Zie ook

[Business Central en Power BI](admin-powerbi.md)  
[Power BI-integratieonderdeel en architectuuroverzicht voor [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Verbinding met Power BI maken vanuit [!INCLUDE [prod_short](includes/prod_short.md)] on-premises](across-working-with-business-central-in-powerbi.md)  
[Power BI-rapporten maken om [!INCLUDE [prod_long](includes/prod_long.md)]-gegevens weer te geven](across-how-use-financials-data-source-powerbi.md)  
[Bedrijfsinformatie](bi.md)  
[Voorbereiden om aan de slag te gaan](ui-get-ready-business.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]](setup.md) instellen  
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken als Power BI-gegevensbron](across-how-use-financials-data-source-powerbi.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken als Power Apps-gegevensbron](across-how-use-financials-data-source-powerapps.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken in Power Automate](across-how-use-financials-data-source-flow.md)  
[Power BI-documentatie](/power-bi/)  
[Wat is Power BI?](/power-bi/fundamentals/power-bi-overview)  
[Snelle start: Uw gegevens verbinden in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Inleiding in datamarts](/power-bi/transform-model/datamarts/datamarts-overview)  
[Inleiding in gegevensstromen en selfservice-gegevensvoorbereiding](/power-bi/transform-model/dataflows/dataflows-introduction-self-service)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
