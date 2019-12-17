---
title: Uw bedrijfsgegevens inschakelen voor Power BI | Microsoft Docs
description: Inzicht, bedrijfsinformatie en KPI's krijgen uit uw Business Central-gegevens is gemakkelijk met Business Central-apps voor Power BI.
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2019
ms.author: bmeier
ms.openlocfilehash: 0750f1724260eb7767757d947f30dcb074ef1aeb
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879118"
---
# <a name="enabling-your-business-data-for-power-bi"></a>Uw bedrijfsgegevens inschakelen voor Power BI

Inzicht krijgen in uw [!INCLUDE[prodshort](includes/prodshort.md)]-gegevens is gemakkelijk met de [!INCLUDE[prodshort](includes/prodshort.md)]-apps voor Power BI. Power BI haalt uw gegevens op en maakt vervolgens een kant-en-klaar dashboard en rapporteert op basis van die gegevens.  

U moet een geldige account bij [!INCLUDE[prodshort](includes/prodshort.md)] en Power BI hebben. Ook moet u [Power BI Desktop](https://powerbi.microsoft.com/desktop/) downloaden als u uw eigen Power BI-rapporten wilt maken. Power BI-apps vereisen machtigingen voor de tabellen waaruit de gegevens worden opgehaald. Meer details over de vereisten worden verderop beschreven.  

> [!IMPORTANT]
> De Power BI-apps die in dit artikel worden beschreven, zijn ontworpen om Azure Active Directory te gebruiken als het verificatiemechanisme, tenzij anders vermeld. Als u een Power BI-app wilt installeren, moet u ook een Power BI Pro-licentie hebben.  Zodra de Power BI-app is geïnstalleerd, kan deze worden gedeeld met gebruikers met elk licentietype.

[!INCLUDE [prodlong](includes/prodlong.md)] heeft de volgende apps gepubliceerd voor Power BI:

- [!INCLUDE [prodlong](includes/prodlong.md)] - CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Sales  
- [!INCLUDE [prodlong](includes/prodlong.md)](on-premises) - CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)](on-premises) - Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)](on-premises) - Sales  

## <a name="using-the-include-prodshortincludesprodshortmd-dashboards-in-power-bi"></a>De [!INCLUDE [prodshort](includes/prodshort.md)]-dashboards gebruiken in Power BI

Elke app bevat rapporten met verschillende detailniveaus:

- Kies een dashboardfunctie om een van de onderliggende rapporten weer te geven.  
- Filter het rapport of voeg velden toe die u wilt controleren.  
- Vergrendel deze aangepaste weergave op het dashboard om door te gaan met tracking.  
  U kunt gegevens handmatig vernieuwen en u kunt een schema voor vernieuwen instellen. Zie voor meer informatie [Gepland vernieuwen configureren](/power-bi/refresh-scheduled-refresh).  

De apps zijn ontworpen om te werken met gegevens van elk bedrijf dat u in uw [!INCLUDE[prodshort](includes/prodshort.md)] hebt. Wanneer u de Power BI-app installeert, geeft u een of meer parameters op om verbinding te maken met uw [!INCLUDE [prodshort](includes/prodshort.md)].  

> [!NOTE]
> U kunt ook uw eigen rapporten en dashboards in Power BI samenstellen op basis van de [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens. Zie voor meer informatie [Uw bedrijfsgegevens verbinden met Power BI](across-how-use-financials-data-source-powerbi.md).  

### <a name="to-connect-your-data-in-power-bi"></a>Uw gegevens verbinden in Power BI

1. Open uw browser, ga naar https://powerbi.microsoft.com en log in op uw account.
2. Selecteer **Gegevens ophalen** onder in het linkernavigatiedeelvenster.  

    ![Navigeren om gegevens op te halen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

    U kunt ook aan de slag gaan vanuit [!INCLUDE [prodshort](includes/prodshort.md)]. Navigeer vanaf uw startpagina naar **Rapportselectie** in de sectie Power BI. Selecteer **Service** of **Mijn organisatie** vanuit het lint. Wanneer een van deze acties wordt geselecteerd, gaat u naar de Organisatiegalerie in Power BI of naar Microsoft AppSource, die ook wordt gefilterd op alleen weergave van apps die verband houden met [!INCLUDE[prodshort](includes/prodshort.md)].

3. Selecteer **Ophalen** in het vak **Diensten**. Hierdoor wordt een pagina geopend met de **AppSource** en **apps voor Power BI**.  

<!--    ![Choose apps from online services that you use.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)-->
4. Selecteer **Apps** op het tabblad **Apps voor Power BI** en kies de **Microsoft Dynamics 365 Business Central**-app die u wilt gebruiken. Selecteer vervolgens **Nu ophalen**.  
<!--    ![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packspowerbi-dynamics365-for-financials-get-it-now.png)/-->
5. Voer desgevraagd de naam van de omgeving en het bedrijf in uw [!INCLUDE[prodshort](includes/prodshort.md)] in waarmee u verbinding wilt maken. Als u niet meerdere omgevingen hebt gemaakt, voert u **Productie** in. Zorg ervoor dat u voor de bedrijfsparameter de naam invoert en niet de weergavenaam. U vindt de bedrijfsnaam op de pagina **Bedrijven** in uw [!INCLUDE[prodshort](includes/prodshort.md)]-exemplaar.  

    > [!NOTE]
    > Als u verbinding maakt met [!INCLUDE [prodshort](includes/prodshort.md)] on-premises moet u de parameter *Webservice-URL* opgeven. U vindt dit op de pagina **Webservices** in [!INCLUDE [prodshort](includes/prodshort.md)]. Uw [!INCLUDE [server](includes/server.md)]-exemplaar moet zijn geconfigureerd voor basisverificatie en u moet een gebruiker en de webtoegangssleutel van die gebruiker opgeven als hun wachtwoord. Vervang in het volgende voorbeeld *myserver:7048* door uw [!INCLUDE [server](includes/server.md)]-naam en *CRONUS%20US* door uw bedrijfsnaam.  
    > ```https://myserver:7048/BC140/ODataV4/Company('CRONUS%20US')/```

6. Eenmaal verbonden worden een dashboard en rapporten aan uw Power BI-werkruimte toegevoegd. Wanneer dit is voltooid, bevatten de tegels gegevens uit uw [!INCLUDE[prodshort](includes/prodshort.md)]-bedrijf.

    ![Selecteer Dynamics 365 Business Central en selecteer Nu ophalen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

### <a name="what-now"></a>Wat nu?

- Probeer [een vraag te stellen in het vraag- en antwoordvak](/power-bi/service-q-and-a-tips) boven aan het dashboard.
- [Wijzig de tegels](/power-bi/service-dashboard-edit-tile) in het dashboard.  
- [Selecteer een tegel](/power-bi/service-dashboard-tiles) om het onderliggende rapport te openen.  
- Standaard is uw gegevensset niet gepland om te vernieuwen. U kunt het vernieuwingsschema wijzigen of het op aanvraag proberen te vernieuwen met **Nu vernieuwen**. Zie voor meer informatie [Gepland vernieuwen configureren](/power-bi/refresh-scheduled-refresh).

## <a name="power-bi-in-include-prodshortincludesprodshortmd"></a>Power BI in [!INCLUDE [prodshort](includes/prodshort.md)]

Uw startpagina in [!INCLUDE [prodshort](includes/prodshort.md)] kan een Power BI-besturingselement bevatten dat kan worden geconfigureerd om Power BI-rapporten weer te geven op uw startpagina.

> [!IMPORTANT]
> U moet een geldige account bij [!INCLUDE [prodshort](includes/prodshort.md)] en Power BI hebben. Als u rapporten wilt wijzigen, moet u ook Power BI Desktop downloaden. Zie voor meer informatie [Business Central gebruiken als een Power BI-gegevensbron](across-how-use-financials-data-source-powerbi.md).  

### <a name="on-first-login"></a>Bij eerste aanmelding

Wanneer u zich voor het eerst aanmeldt bij [!INCLUDE [prodshort](includes/prodshort.md)], ziet u een leeg Power BI-deel op uw startpagina. Om de rapporten te bekijken moet u eerst verbinding maken met Power BI door de koppeling *Aan de slag met Power BI* te selecteren.

[!INCLUDE [prodshort](includes/prodshort.md)] communiceert vervolgens met de Power BI-service om te bepalen of u een geldig Power BI-account hebt. Zodra uw licentie is geverifieerd, worden de standaard Power BI-rapporten weergegeven op uw startpagina.

### <a name="selecting-power-bi-reports"></a>Power BI-rapporten selecteren

Het Power BI-besturingselement op uw startpagina kan elk Power BI-rapport weergeven. Als u een bestaand rapport wilt weergeven, kiest u de actie **Rapport selecteren** in de Power BI-vervolgkeuzelijst met opdrachten.  

De pagina voor het selecteren van rapporten toont een lijst met alle Power BI-rapporten waartoe u toegang hebt. Deze lijst wordt opgehaald uit uw Power BI-werkruimte. Schakel elk rapport in dat u op de startpagina wilt weergeven en kies vervolgens OK. U keert terug naar uw startpagina en het laatste rapport dat u hebt ingeschakeld, wordt weergegeven. Gebruik de vervolgkeuzelijst met opdrachten om de vorige en volgende opdracht te gebruiken om tussen rapporten te navigeren.  

### <a name="get-reports"></a>Rapporten ophalen

Als u geen rapporten ziet op de pagina Rapporten selecteren of het gewenste rapport niet ziet. U kunt ervoor kiezen rapporten op te halen uit *Mijn organisatie* of uit *Diensten*.
Kies *Mijn organisatie* om naar de Power BI-services te gaan waarmee u de rapporten binnen uw organisatie kunt bekijken waarvoor u weergaverechten hebt, en deze toe te voegen aan uw werkruimte. Kies *Diensten* om naar Microsoft AppSource te gaan, waar u Power BI-apps kunt installeren.  

U kunt er ook voor kiezen om nieuwe Power BI-rapporten te maken. Zodra die rapporten naar uw Power BI-werkruimte zijn gepubliceerd, verschijnen ze op deze pagina.  

### <a name="managing-reports"></a>Rapporten beheren

In de Power BI-sectie op uw startpagina kunt u de actie **Rapport beheren** kiezen uit de vervolgkeuzelijst met opdrachten, zodat u het rapport dat in focus was in het rolcentrum kunt wijzigen.  

Wijzigingen kunnen in het rapport worden aangebracht en opgeslagen.  Wijzigingen in het rapport worden gewijzigd voor elke gebruiker met wie dit rapport wordt gedeeld, aangezien u het rapport wijzigt dat is opgeslagen in de Power BI-service.  

Nadat u uw wijzigingen hebt voltooid, selecteert u Opslaan. Als dit een gedeeld rapport is, kunt u Opslaan als selecteren om te voorkomen dat deze wijziging voor alle gebruikers wordt aangebracht.
Keer terug naar het rolcentrum en het bijgewerkte rapport verschijnt. Als u de opdracht Opslaan als hebt uitgevoerd, moet u de pagina Rapport selecteren openen en het nieuwe rapport inschakelen.

### <a name="uploading-reports"></a>Rapporten uploaden

U kunt nieuwe Power BI-rapporten uploaden en delen met alle gebruikers van uw [!INCLUDE [prodshort](includes/prodshort.md)]. De rapporten worden binnen elk bedrijf binnen gedeeld in [!INCLUDE [prodshort](includes/prodshort.md)].  

Als u een rapport wilt uploaden, kiest u de actie **Rapport uploaden** in de vervolgkeuzelijst met opdrachten. U kunt vervolgens een .pbix-bestand uploaden dat de rapporten definieert die u wilt delen. U kunt de standaardnaam van het bestand wijzigen.  

Zodra het rapport naar uw Power BI-werkruimte is geüpload, wordt het automatisch geüpload naar de Power BI-werkruimten van alle andere gebruikers in dat bedrijf bij hun volgende aanmelding bij [!INCLUDE [prodshort](includes/prodshort.md)].

## <a name="system-requirements"></a>Systeemvereisten

Als u uw [!INCLUDE[prodshort](includes/prodshort.md)]-gegevens in Power BI wilt importeren, moet u machtigingen hebben voor de webservices die worden gebruikt om gegevens op te halen. De webservices die voor elke Power BI-app vereist zijn, omvatten:

### <a name="microsoft-dynamics-365-business-central--crm"></a>Microsoft Dynamics 365 Business Central – CRM

- Verkoopopportunities
- Bedrijfsgegevens van weergave van Excel-sjabloon
- Labels van Power BI-rapport

### <a name="microsoft-dynamics-365-business-central--finance"></a>Microsoft Dynamics 365 Business Central – Finance

- PowerBIFinance
- Bedrijfsgegevens van weergave van Excel-sjabloon
- Labels van Power BI-rapport

### <a name="microsoft-dynamics-365-business-central---sales"></a>Microsoft Dynamics 365 Business Central - Sales

- Artikelverkopen per klant
- Verkoopdashboard
- Excel-sjabloonweergave Bedrijf
- Labels van Power BI-rapport

> [!NOTE]
> [!INCLUDE [prodshort](includes/prodshort.md)] on-premises gebruikt dezelfde eindpunten voor webservices als [!INCLUDE [prodshort](includes/prodshort.md)] online.

## <a name="web-services"></a>Webservices

Een eenvoudige manier om de webservices te vinden is te zoeken naar *webservices* in [!INCLUDE[prodshort](includes/prodshort.md)]. Zorg op de pagina **Webservices** dat het veld **Publiceren** is geselecteerd voor de hierboven genoemde webservices.

## <a name="troubleshooting"></a>Problemen oplossen

Het dashboard van Power BI gebruikt de gepubliceerde webservices die hierboven worden genoemd en bevat gegevens van het demobedrijf of uw eigen bedrijf als u gegevens importeert uit uw huidige financiële oplossing. Als er echter iets verkeerd gaat, biedt deze sectie een oplossing voor de meest voorkomende problemen.  

### <a name="you-do-not-have-a-power-bi-account"></a>U hebt geen Power BI-account

Er is geen Power BI-account ingesteld. Als u een geldig Power BI-account wilt hebben, moet u een licentie hebben en moet u zich eerder hebben aangemeld bij Power BI, zodat uw Power BI-werkruimte kan worden gemaakt.  

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Bericht: Er zijn geen ingeschakelde rapporten. Kies Rapport selecteren om een lijst met rapporten weer te geven die u kunt weergeven.

Dit bericht verschijnt als het standaardrapport niet naar uw Power BI-werkruimte kan worden geïmplementeerd of het rapport is geïmplementeerd maar niet met succes is vernieuwd. Als dit gebeurt, navigeert u naar het rapport in uw Power BI-werkruimte, selecteert u **Gegevensset**, **Instellingen** en werkt u vervolgens de referenties handmatig bij. Nadat de gegevensset met succes is vernieuwd, navigeert u terug naar Business Central en selecteert u handmatig het rapport vanaf de pagina **Rapporten selecteren**. 

### <a name="you-need-a-power-bi-pro-license-to-install-the-include-prodshortincludesprodshortmd-app-in-power-bi"></a>U hebt een Power BI Pro-licentie nodig om de [!INCLUDE [prodshort](includes/prodshort.md)]-app in Power BI te installeren

Power BI-apps kunnen alleen worden geïnstalleerd door gebruikers met een Power BI Pro-licentie. Zodra de Power BI-app is geïnstalleerd, kunt u deze delen met gebruikers die geen Power BI Pro-licentie hebben.  

### <a name="parameter-validation-failed-please-make-sure-all-parameters-are-valid"></a>"Parametervalidatie mislukt; zorg dat alle parameters geldig zijn"

Deze fout geeft aan dat een van de parameters niet geldig is.

- De opgegeven omgevingsparameter komt niet overeen met een bestaande [!INCLUDE [prodshort](includes/prodshort.md)]-productie of sandboxomgeving. 
- De opgegeven bedrijfsparameter komt niet overeen met bestaande [!INCLUDE [prodshort](includes/prodshort.md)]-bedrijven. Controleer de bedrijfsnaam op de pagina **Bedrijven** in [!INCLUDE [prodshort](includes/prodshort.md)].
- Als u verbinding maakt met [!INCLUDE [prodshort](includes/prodshort.md)] on-premises. u hebt een URL ingevoerd die niet geldig is. U kunt de URL verifiëren op de pagina **Webservices** in [!INCLUDE [prodshort](includes/prodshort.md)]  
- Er staat geen poort open om het verzoek door uw firewall te laten gaan.

### <a name="login-failed"></a>Aanmelding mislukt

Als u de fout "Aanmelding mislukt" krijgt nadat u zich aanmeldt met uw [!INCLUDE [prodshort](includes/prodshort.md)]-referenties, kan dat een van de volgende oorzaken hebben:

- Het account dat u gebruikt, heeft geen machtigingen om de [!INCLUDE [prodshort](includes/prodshort.md)]-gegevens uit uw account op te halen. Controleer of u machtigingen hebt voor de vereiste gegevens in [!INCLUDE [prodshort](includes/prodshort.md)] en probeer het opnieuw.
- U hebt een ander verificatietype dan Basis geselecteerd als u verbinding maakt met [!INCLUDE [prodshort](includes/prodshort.md)] on-premises.
- U hebt geen geldige gebruikersnaam of wachtwoord ingevoerd.

### <a name="incorrect-company-name"></a>Onjuiste bedrijfsnaam

Een veel voorkomende fout is de weergavenaam van het bedrijf in te voeren in plaats van de bedrijfsnaam. Als u de bedrijfsnaam wilt vinden, zoekt u naar **Bedrijven**. Gebruik vervolgens het veld **Naam** wanneer u uw bedrijfsnaam invoert.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>De sleutel kwam met geen rijen uit de tabel overeen

Als u een ongeldige bedrijfsnaam invoert tijdens het verbindingsproces, kunt u de foutmelding "De sleutel kwam met geen rijen uit de tabel overeen" krijgen. Geef de juiste bedrijfsnaam op en probeer opnieuw verbinding te maken.

### <a name="historical-data-appears-to-be-missing"></a>Historische gegevens lijken te ontbreken

Zodra de Power BI-app is geïnstalleerd en uw gegevens verschijnen in Power BI, merkt u mogelijk dat niet al uw gegevens worden weergegeven. De gegevenssets worden gefilterd om alleen de voorgaande 365 dagen aan gegevens te retourneren. Deze standaard is aanwezig om de rapporten sneller te maken.  

### <a name="i-only-see-data-for-a-single-company"></a>Ik zie alleen gegevens voor één bedrijf

De Power BI-app toont alleen gegevens van het [!INCLUDE [prodshort](includes/prodshort.md)]-bedrijf dat is gedefinieerd toen de Power BI-app werd geïnstalleerd. Gegevens van extra bedrijven kunnen aan de rapporten worden toegevoegd door nieuwe query's toe te voegen die verschillende bedrijven als gegevensbron gebruiken.  

## <a name="see-also"></a>Zie ook

[Power BI voor consumenten](/power-bi/consumer/end-user-consumer)  
[De 'nieuwe look' van de Power BI-service](/power-bi/service-new-look)  
[Snelle start: Uw gegevens verbinden in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI-documentatie](/power-bi/)  
[Bedrijfsinformatie](bi.md)  
[Aan de slag](product-get-started.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken als Power BI-gegevensbron](across-how-use-financials-data-source-powerbi.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken als Power Apps-gegevensbron](across-how-use-financials-data-source-powerapps.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken in Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
