---
title: Werken met Power BI-rapporten in Business Central | Microsoft Docs
description: 'Krijg inzicht, bedrijfsinformatie en KPI''s uit uw Business Central-gegevens met Power BI.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 04/24/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="work-with-power-bi-reports-in-"></a>Werken met Power BI-rapporten in [!INCLUDE [prod_short](includes/prod_short.md)]

In dit artikel leert u enkele basisbeginselen over het werken met rapporten. Dit omvat het bekijken van Power BI-rapporten binnen [!INCLUDE [prod_short](includes/prod_short.md)] (inclusief scorekaarten en dashboards) en het bewerken van Power BI-rapporten die [!INCLUDE [prod_short](includes/prod_short.md)] als gegevensbron gebruiken. In het artikel worden enkele aspecten besproken die u op weg helpen als [!INCLUDE[prod_short](includes/prod_short.md)]-gebruiker. Raadpleeg voor algemene richtlijnen en instructies voor het gebruik van Power BI de [Power BI-documentatie voor consumenten](/power-bi/consumer).

## <a name="overview"></a>Overzicht

Power BI-rapporten geven u inzicht in uw [!INCLUDE[prod_short](includes/prod_short.md)]. Diverse pagina's in [!INCLUDE [prod_short](includes/prod_short.md)] hebben een Power BI-rapportgedeelte waarin Power BI-rapporten kunnen worden weergegeven. Het rolcentrum is een pagina waar u gewoonlijk gedeelte voor een Power BI-rapporten aantreft. Bepaalde lijstpagina's, zoals **Artikelen**, bevatten ook een Power BI-gedeelte.

[!INCLUDE [prod_short](includes/prod_short.md)] werkt samen met de Power BI-service. Rapporten die bestemd zijn om te worden weergegeven in [!INCLUDE [prod_short](includes/prod_short.md)], worden opgeslagen in een Power BI-service. In [!INCLUDE [prod_short](includes/prod_short.md)] kunt u het rapport dat wordt weergegeven in het Power BI-gedeelte, veranderen in elk ander Power BI-rapport dat beschikbaar is in de Power BI-service. De eerste keer dat u zich aanmeldt bij [!INCLUDE [prod_short](includes/prod_short.md)] zijn de gedeelten voor Power BI-rapporten leeg en dat blijft zo totdat u verbinding maakt met een Power BI-service, zoals hier wordt weergegeven:

![Power BI-gedeelte in Business Central.](./media/power-bi-part.png)

## <a name="get-started"></a>Aan de slag

> [!NOTE]
> [!INCLUDE [prod_short](includes/prod_short.md)] online is al ingesteld voor integratie met Power BI.

### <a name="sign-up-power-bi"></a>Power BI aanmelden

Voordat u Power BI kunt gebruiken met [!INCLUDE[prod_short](includes/prod_short.md)], moet u zich aanmelden voor de Power BI-service. Als u zich nog niet hebt aangemeld, gaat u naar [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Gebruik wanneer u zich aanmeldt uw zakelijke e-mailadres en wachtwoord.

Als u eenmaal een Power BI-account hebt, kunt u zich aanmelden via [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

De Power BI-service host alle rapporten die voor u beschikbaar zijn. Als u een rapport in uw persoonlijke werkruimte wilt bekijken, selecteert u **Mijn werkruimte** > **Rapporten**. Selecteer vervolgens het rapport dat u wilt bekijken. Als u toegang heeft tot een of meer gedeelde Power BI-werkruimten, kunt u in die werkruimten ook rapporten bekijken.

Met [!INCLUDE[prod_short](includes/prod_short.md)] online hebt u automatisch de beschikking over een set standaardrapporten in uw werkruimte. Als u uw eigen rapporten wilt maken, kunt u gebruikmaken van Power BI Desktop om rapporten te maken en deze vervolgens te publiceren naar uw werkruimte. Zie [Aan de slag met het maken van rapporten in Power BI Desktop om [!INCLUDE [prod_long](includes/prod_long.md)]-gegevens weer te geven](across-how-use-financials-data-source-powerbi.md) voor meer informatie.

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

## <a name="connect-to-power-bi---one-time-only"></a><a name="connect"></a>Verbinding maken met Power BI - eenmalig

Wanneer u zich voor het eerst aanmeldt bij [!INCLUDE [prod_short](includes/prod_short.md)], ziet u waarschijnlijk een leeg Power BI-gedeelte op verschillende pagina's (zoals weergegeven in de vorige afbeelding). Het eerste dat u moet doen, is verbinding maken met uw Power BI-account. Als de verbinding eenmaal tot stand is gebracht, worden er rapporten weergegeven. U hoeft deze stap maar één keer uit te voeren.

1. Selecteer de koppeling **Aan de slag met Power BI** in het gedeelte **Power BI-rapporten**.
2. De begeleide instelling **Power BI-rapporten instellen in Business Central** wordt gestart. Selecteer **Volgende** om door te gaan.
3. Op de pagina **Controleer uw Power BI-licentie**. Ga op een van de volgende manieren te werk:

    - Als u zich nog niet hebt aangemeld voor Power BI, selecteert u [Ga naar Power BI-startpagina](https://powerbi.microsoft.com). Meld u aan voor een account en kom dan terug naar [!INCLUDE[prod_short](includes/prod_short.md)] en voltooi de instelling.

    - Als u al een licentie heeft, selecteert u **Volgende**.
4. Op de volgende pagina uploadt [!INCLUDE[prod_short](includes/prod_short.md)] nu een demo-rapport naar Power BI. Deze stap duurt een paar minuten, dus het gebeurt op de achtergrond. Selecteer om de instelling te voltooien **Volgende** en dan **Voltooien**.

Het verbindingsproces begint. Tijdens het proces communiceert [!INCLUDE [prod_short](includes/prod_short.md)] met de Power BI-service om te bepalen of u een geldig Power BI-account en geldige licentie hebt. Zodra uw licentie is geverifieerd, wordt het standaard Power BI-rapport weergegeven op de pagina. Als er geen rapport wordt weergegeven, kunt u in het gedeelte een rapport selecteren.

> [!TIP]
> Als u [!INCLUDE [prod_short](includes/prod_short.md)] online gebruikt, worden met deze stap automatisch de standaard Power BI-rapporten die worden gebruikt in [!INCLUDE [prod_short](includes/prod_short.md)], naar uw Power BI-werkruimte geüpload.

<!--#### From [!INCLUDE [prod_short](includes/prod_short.md)] on-premises

Connecting to Power BI from [!INCLUDE [prod_short](includes/prod_short.md)] is similar to online. However, you might be prompted on the **MICROSOFT ENTRA SERVICE PERMISSIONS** page to grant access to Power BI Services. To grant access, select **Authorize Azure Services**, and then **Accept**.

Once connected, you can select a report from the Power BI part on pages.-->

## <a name="work-with-power-bi-reports"></a>Werken met Power BI-rapporten

### <a name="get-the-latest-data"></a>De meest recente gegevens ophalen

Elk Power BI-rapport is gebaseerd op een gegevensset die gegevens ophaalt uit de [!INCLUDE[prod_short](includes/prod_short.md)]-bronnen. U wilt er uiteraard zeker van zijn dat de gegevens in uw Power BI-rapporten altijd up-to-date zijn, dus overeenkomen met de gegevens in [!INCLUDE[prod_short](includes/prod_short.md)]. Dit concept wordt *vernieuwen* genoemd.  Of de gegevens automatisch worden vernieuwd, hangt af van de manier waarop uw organisatie Power BI heeft geconfigureerd. Er zijn twee manieren om gegevens te vernieuwen: handmatig of via een geplande automatische vernieuwingsactie. Handmatig vernieuwen kan op aanvraag, wanneer dat nodig is. Met gepland vernieuwen kunt u de gegevens steeds automatisch laten vernieuwen na een bepaald tijdsinterval.

#### <a name="refresh-manually"></a>Handmatig vernieuwen

Selecteer vanuit Power BI online in het navigatievenster onder **Gegevenssets** de opdracht **Meer opties (...)** naast de gegevensset en selecteer vervolgens **Nu vernieuwen**.

#### <a name="schedule-a-refresh"></a>Het vernieuwen van gegevens plannen

Selecteer vanuit Power BI online in het navigatievenster onder Gegevenssets de opdracht Meer opties (...) naast de gegevensset en selecteer vervolgens **Vernieuwen plannen**. Vul de gegevens in in het gedeelte **Vernieuwen plannen** en selecteer **Toepassen**.

Zie [Geplande vernieuwing configureren](/power-bi/connect-data/refresh-scheduled-refresh) voor meer informatie.

### <a name="show-reports-on-list-pages"></a>Rapporten weergeven op lijstpagina's

Verschillende belangrijke lijstpagina's van [!INCLUDE[prod_long](includes/prod_long.md)] bevatten een Power BI-feitenblok. Dit feitenblok geeft extra inzicht in de gegevens in de lijst. Terwijl u van de ene naar de andere rij gaat, wordt het rapport bijgewerkt en gefilterd op de geselecteerde vermelding.

Zie voor meer informatie over het maken van rapporten voor lijstpagina's [Power BI-rapporten maken voor het weergeven van lijstgegevens in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

> [!TIP]
> Als u het Power BI-feitenblok niet ziet, wordt het mogelijk door personalisatie op uw werkruimte verborgen. Selecteer het pictogram ![Instellingen.](media/ui-experience/settings_icon_small.png "Pictogram Instellingen voor rolcentrum") en vervolgens de actie **Personaliseren**. Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.
>
> Of als u een oudere versie van Business Central heeft, gaat u naar de actiebalk, selecteert u **Acties** > **Weergave** > **Power BI-rapporten weergeven/verbergen**.

### <a name="switch-reports"></a>Schakelen tussen rapporten

In een Power BI-gedeelte op een pagina kan elk Power BI-rapport worden weergegeven dat voor u beschikbaar is. Als u wilt overschakelen naar een ander rapport, kiest u de actie **Rapport selecteren** in de vervolgkeuzelijst met opdrachten boven aan het gedeelte.  

Op de pagina **Selectie van Power BI-rapporten** wordt een lijst weergegeven van alle Power BI-rapporten waartoe u toegang hebt. Deze lijst wordt opgehaald uit uw eigen werkruimten of werkruimten die met u zijn gedeeld in de Power BI-service. Selecteer het vak **Inschakelen** voor elk rapport dat u op de pagina wilt weergeven en kies vervolgens **OK**. U keert terug naar de pagina en het laatste rapport dat u hebt ingeschakeld, wordt weergegeven. Gebruik de vervolgkeuzelijst met opdrachten de opdrachten **Vorige** en **Volgende** om van het ene naar het andere rapport te navigeren.  

### <a name="get-more-reports"></a>Meer rapporten krijgen

Als er geen rapporten worden weergegeven op de pagina **Selectie van Power BI-rapporten** of als het gewenste rapport niet wordt weergegeven, kiest u **Rapporten ophalen**. Met deze actie kunt zoeken naar rapporten vanuit twee locaties: *Mijn organisatie* of *Services*.

- Kies **Mijn organisatie** om naar de Power BI-services te gaan. Van hieruit kunt u de rapporten binnen uw organisatie weergeven waarvoor u de rechten hebt om ze weer te geven. U kunt ze vervolgens toevoegen aan uw werkruimte.
- Kies **Services** om naar Microsoft AppSource te gaan, waar u Power BI-apps kunt installeren.  

> [!TIP]
> Als u Power BI Desktop hebt, kunt u ook nieuwe Power BI-rapporten maken. Als deze rapporten eenmaal zijn gepubliceerd naar uw Power BI-werkruimte, verschijnen ze op de pagina Selectie van **Power BI-rapporten**.  

### <a name="manage-and-modify-reports"></a>Rapporten beheren en wijzigen

U kunt wijzigingen aanbrengen in een rapport in het Power BI-gedeelte. De wijzigingen die u aanbrengt, worden vervolgens gepubliceerd naar de Power BI-service. Als het rapport wordt gedeeld met andere gebruikers, zien ook zij de wijzigingen, tenzij u de wijzigingen opslaat in een nieuw rapport.

Als u een rapport wilt wijzigen, kiest u de actie **Rapport beheren** in de vervolgkeuzelijst met opdrachten in het Power BI-gedeelte. Vervolgens kunt u de gewenste wijzigingen aanbrengen. Selecteer als u klaar bent met het aanbrengen van wijzigingen de opties **Bestand** > **Opslaan**. Als het rapport waarin u de wijzigingen aanbrengt, een gedeeld rapport is en u de wijzigingen niet voor alle gebruikers wilt aanbrengen, selecteert u **Opslaan als** om te voorkomen dat deze wijzigingen voor alle gebruikers worden aangebracht.

Wanneer u terugkeert naar het rolcentrum, ziet u daar het bijgewerkte rapport verschijnen. Als u **Opslaan als** hebt gebruikt, moet u eerst de actie **Rapport selecteren** kiezen en vervolgens het nieuwe rapport inschakelen om het weer te geven.

> [!NOTE]
> Deze mogelijkheid is niet beschikbaar voor [!INCLUDE [prod_short](includes/prod_short.md)] on-premises.

### <a name="upload-reports"></a><a name="upload"></a>Rapporten uploaden

Power BI-rapporten kunnen onder gebruikers worden verspreid als PBIX-bestanden. Als u PBIX-bestanden hebt, kunt u deze uploaden en delen met alle gebruikers van [!INCLUDE [prod_short](includes/prod_short.md)]. De rapporten worden binnen elk bedrijf binnen gedeeld in [!INCLUDE [prod_short](includes/prod_short.md)].  

Als u een rapport wilt uploaden, kiest u de actie **Rapport uploaden** in de vervolgkeuzelijst met opdrachten in het gedeelte **Power BI-rapporten**. Ga vervolgens op zoek naar het PBIX-bestand dat de rapporten definieert die u wilt delen. U kunt de standaardnaam van het bestand wijzigen.  

Nadat het rapport is geüpload naar uw Power BI-werkruimte, wordt het automatisch geüpload naar de Power BI-werkruimten van andere gebruikers.

> [!NOTE]
> Om een rapport te kunnen uploaden met [!INCLUDE[prod_short](includes/prod_short.md)], moet u de machtigingen van een SUPER-gebruiker hebben in [!INCLUDE[prod_short](includes/prod_short.md)]. U heeft geen speciale toestemming nodig om rapporten naar uw werkruimte te uploaden via de Power BI-service.

## <a name="upload-reports-from-files"></a><a name="upload"></a>Rapporten uploaden vanuit bestanden

Power BI-rapporten kunnen onder gebruikers worden verspreid als PBIX-bestanden. Als u een PBIX-bestand heeft, kunt u het bestand uploaden naar een werkruimte. Voer de volgende stappen uit om een rapport te uploaden:

1. Selecteer in uw nieuwe werkruimte de optie **Gegevens ophalen**.

2. Selecteer in het vak Bestanden de optie **Ophalen**.

3. Selecteer **Lokaal bestand**, navigeer naar de plaats waar u het bestand hebt opgeslagen en selecteer **Openen**.

Zie [Het rapport uploaden naar de service](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service) voor meer informatie.

<!--
> [!NOTE]
> Uploading a report requires that you have a [Premium capacity](/power-bi/service-premium-what-is) work space. For more information, see [Managing Premium capacities](/power-bi/admin/service-premium-capacity-manage). -->

> [!TIP]
> Als u [!INCLUDE[prod_short](includes/prod_short.md)] online gebruikt, kunt u ook een rapport uploaden vanuit [!INCLUDE[prod_short](includes/prod_short.md)]. Zie [Werken met Power BI-rapporten in [!INCLUDE [prod_short](includes/prod_short.md)] - Rapporten uploaden](across-working-with-powerbi.md#upload) voor meer informatie.

## <a name="share-reports-with-others"></a><a name="share"></a>Rapporten met anderen delen

Zodra een rapport zich in uw werkruimte bevindt, kunt u het delen met anderen in uw organisatie.

Als u een rapport wilt delen, selecteert u in een lijst met rapporten of in een geopend rapport de optie **Delen**. Voer in het deelvenster **Rapport delen** het volledige e-mailadres in van individuen of distributiegroepen waarmee u het rapport wilt delen. Volg de instructies op het scherm om het delen te voltooien. Zie [Een dashboard of rapport delen](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report) voor meer informatie.

> [!NOTE]
> Het is vereist dat zowel u als de mensen met wie u het rapport deelt, een [Power BI Pro-licentie](/power-bi/service-features-license-type) hebben. Anders moet de inhoud zich in de [Premium-capaciteit](/power-bi/service-premium-what-is) bevinden. Zie [Manieren om uw werk te delen in Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports) voor meer informatie.

## <a name="fixing-problems"></a>Problemen oplossen

Als er echter iets verkeerd gaat, biedt deze sectie een oplossing voor de meest voorkomende problemen.  

### <a name="you-dont-have-a-power-bi-account"></a>U hebt geen Power BI-account

Er is geen Power BI-account ingesteld. Als u een geldig Power BI-account wilt aanvragen, moet u een licentie hebben en moet u zich eerder hebben aangemeld bij Power BI om een Power BI-werkruimte te maken.

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Bericht: Er zijn geen ingeschakelde rapporten. Kies Rapport selecteren om een lijst met rapporten te tonen die u kunt weergeven.

Dit bericht verschijnt als het standaardrapport niet kon worden geïmplementeerd in uw Power BI-werkruimte. Het bericht wordt ook weergegeven als het rapport is geïmplementeerd maar kon worden vernieuwd. Navigeer naar het rapport in uw Power BI-werkruimte, selecteer **Gegevensset**, **Instellingen** en werk vervolgens de referenties handmatig bij. Nadat de gegevensset met succes is vernieuwd, navigeert u terug naar [!INCLUDE[prod_short](includes/prod_short.md)] en selecteert u handmatig het rapport via de pagina **Rapporten selecteren**.

#### <a name="you-cant-see-a-report-on-the-select-report-page-on-a-list-page"></a>U kunt geen rapport zien op de pagina Rapport selecteren op een lijstpagina

Dit komt waarschijnlijk omdat de naam van het rapport niet de naam van de lijstpagina bevat. Wis het filter om de volledige lijst met beschikbare Power BI-rapporten weer te geven.

## <a name="see-also"></a>Zie ook

[Business Central en Power BI](admin-powerbi.md)    
[Power BI-rapporten maken om [!INCLUDE [prod_long](includes/prod_long.md)] gegevens weer te geven](across-how-use-financials-data-source-powerbi.md)    
[Power BI--integratieonderdeel en architectuuroverzicht voor [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)    
[Power BI verbinden vanuit [!INCLUDE [prod_short](includes/prod_short.md)] on-premises](across-working-with-business-central-in-powerbi.md)    
[Power BI voor consumenten](/power-bi/consumer/end-user-consumer)     
[De 'nieuwe look' van de Power BI-service](/power-bi/service-new-look)    
[Snelle start: verbinding maken met uw gegevens in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)    
[Power BI-documentatie](/power-bi/)    
[Bedrijfsinformatie](bi.md)    
[Uzelf gereedmaken om zaken te doen.](ui-get-ready-business.md)    
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)    
[Instellen van [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)    
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken als een Power BI-gegevensbron](across-how-use-financials-data-source-powerapps.md)    
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken als een Power Apps-gegevensbron](across-how-use-financials-data-source-powerapps.md)    
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken in Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]
