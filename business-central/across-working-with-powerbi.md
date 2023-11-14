---
title: Werken met Power BI-rapporten in Business Central| Microsoft Docs
description: 'Krijg inzicht, bedrijfsinformatie en KPI''s uit uw Business Central-gegevens met Power BI.'
author: jswymer
ms.topic: get-started
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 04/01/2021
ms.author: jswymer
---
# Werken met Power BI-rapporten in [!INCLUDE [prod_short](includes/prod_short.md)]

In dit artikel leert u enkele basisbeginselen over het weergeven van Power BI-rapporten, inclusief scorekaarten in [!INCLUDE [prod_short](includes/prod_short.md)].

## Overzicht

Power BI-rapporten geven u inzicht in uw [!INCLUDE[prod_short](includes/prod_short.md)]. Diverse pagina's in [!INCLUDE [prod_short](includes/prod_short.md)] hebben een Power BI-rapportgedeelte waarin Power BI-rapporten kunnen worden weergegeven. Het rolcentrum is een pagina waar u gewoonlijk gedeelte voor een Power BI-rapporten aantreft. Bepaalde lijstpagina's, zoals **Artikelen**, bevatten ook een Power BI-gedeelte.

[!INCLUDE [prod_short](includes/prod_short.md)] werkt samen met de Power BI-service. Rapporten die bestemd zijn om te worden weergegeven in [!INCLUDE [prod_short](includes/prod_short.md)], worden opgeslagen in een Power BI-service. In [!INCLUDE [prod_short](includes/prod_short.md)] kunt u het rapport dat wordt weergegeven in het Power BI-gedeelte, veranderen in elk ander Power BI-rapport dat beschikbaar is in de Power BI-service. De eerste keer dat u zich aanmeldt bij [!INCLUDE [prod_short](includes/prod_short.md)] zijn de gedeelten voor Power BI-rapporten leeg en dat blijft zo totdat u verbinding maakt met een Power BI-service, zoals hier wordt weergegeven:

![Power BI-gedeelte in Business Central.](./media/power-bi-part.png)

## Aan de slag

### Vereisten

Als u [!INCLUDE[prod_short](includes/prod_short.md)] on-premises gebruikt, moet Power BI-integratie zijn ingeschakeld. Deze taak wordt doorgaans uitgevoerd door een beheerder. Zie [[!INCLUDE[prod_short](includes/prod_short.md)] on-premises instellen voor Power BI-integratie](admin-powerbi-setup.md#setup) voor meer informatie.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] online is al ingesteld voor integratie met Power BI.

### Power BI aanmelden

Voordat u Power BI kunt gebruiken met [!INCLUDE[prod_short](includes/prod_short.md)], moet u zich aanmelden voor de Power BI-service. Als u zich nog niet hebt aangemeld, gaat u naar [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Gebruik wanneer u zich aanmeldt uw zakelijke e-mailadres en wachtwoord.

## <a name="connect"></a>Verbinding maken met Power BI - eenmalig

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

#### Vanuit [!INCLUDE [prod_short](includes/prod_short.md)] on-premises

Het maken van een verbinding met Power BI vanuit [!INCLUDE [prod_short](includes/prod_short.md)] gaat op ongeveer dezelfde manier als in de online versie. U kunt echter op de pagina **MICROSOFT ENTRA SERVICEMACHTIGINGEN** worden gevraagd om toegang te verlenen tot Power BI-services. Selecteer om toegang te verlenen de optie **Azure-services autoriseren** en vervolgens **Accepteren**.

Als de verbinding eenmaal tot stand is gebracht, kunt u een rapport selecteren uit het Power BI-gedeelte op pagina's.

## Werken met Power BI-rapporten

### Rapporten weergeven op lijstpagina's

Verschillende belangrijke lijstpagina's van [!INCLUDE[prod_long](includes/prod_long.md)] bevatten een Power BI-feitenblok. Dit feitenblok geeft extra inzicht in de gegevens in de lijst. Terwijl u van de ene naar de andere rij gaat, wordt het rapport bijgewerkt en gefilterd op de geselecteerde vermelding.

Zie voor meer informatie over het maken van rapporten voor lijstpagina's [Power BI-rapporten maken voor het weergeven van lijstgegevens in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

> [!TIP]
> Als u het Power BI-feitenblok niet ziet, wordt het mogelijk door personalisatie op uw werkruimte verborgen. Selecteer het pictogram ![Instellingen.](media/ui-experience/settings_icon_small.png "Pictogram Instellingen voor rolcentrum") en vervolgens de actie **Personaliseren**. Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.
>
> Of als u een oudere versie van Business Central heeft, gaat u naar de actiebalk, selecteert u **Acties** > **Weergave** > **Power BI-rapporten weergeven/verbergen**.

### Schakelen tussen rapporten

In een Power BI-gedeelte op een pagina kan elk Power BI-rapport worden weergegeven dat voor u beschikbaar is. Als u wilt overschakelen naar een ander rapport, kiest u de actie **Rapport selecteren** in de vervolgkeuzelijst met opdrachten boven aan het gedeelte.  

Op de pagina **Selectie van Power BI-rapporten** wordt een lijst weergegeven van alle Power BI-rapporten waartoe u toegang hebt. Deze lijst wordt opgehaald uit uw eigen werkruimten of werkruimten die met u zijn gedeeld in de Power BI-service. Selecteer het vak **Inschakelen** voor elk rapport dat u op de pagina wilt weergeven en kies vervolgens **OK**. U keert terug naar de pagina en het laatste rapport dat u hebt ingeschakeld, wordt weergegeven. Gebruik de vervolgkeuzelijst met opdrachten de opdrachten **Vorige** en **Volgende** om van het ene naar het andere rapport te navigeren.  

### Meer rapporten krijgen

Als er geen rapporten worden weergegeven op de pagina **Selectie van Power BI-rapporten** of als het gewenste rapport niet wordt weergegeven, kiest u **Rapporten ophalen**. Met deze actie kunt zoeken naar rapporten vanuit twee locaties: *Mijn organisatie* of *Services*.

- Kies **Mijn organisatie** om naar de Power BI-services te gaan. Van hieruit kunt u de rapporten binnen uw organisatie weergeven waarvoor u de rechten hebt om ze weer te geven. U kunt ze vervolgens toevoegen aan uw werkruimte.
- Kies **Services** om naar Microsoft AppSource te gaan, waar u Power BI-apps kunt installeren.  

> [!TIP]
> Als u Power BI Desktop hebt, kunt u ook nieuwe Power BI-rapporten maken. Als deze rapporten eenmaal zijn gepubliceerd naar uw Power BI-werkruimte, verschijnen ze op de pagina Selectie van **Power BI-rapporten**.  

### Rapporten beheren en wijzigen

U kunt wijzigingen aanbrengen in een rapport in het Power BI-gedeelte. De wijzigingen die u aanbrengt, worden vervolgens gepubliceerd naar de Power BI-service. Als het rapport wordt gedeeld met andere gebruikers, zien ook zij de wijzigingen, tenzij u de wijzigingen opslaat in een nieuw rapport.

Als u een rapport wilt wijzigen, kiest u de actie **Rapport beheren** in de vervolgkeuzelijst met opdrachten in het Power BI-gedeelte. Vervolgens kunt u de gewenste wijzigingen aanbrengen. Selecteer als u klaar bent met het aanbrengen van wijzigingen de opties **Bestand** > **Opslaan**. Als het rapport waarin u de wijzigingen aanbrengt, een gedeeld rapport is en u de wijzigingen niet voor alle gebruikers wilt aanbrengen, selecteert u **Opslaan als** om te voorkomen dat deze wijzigingen voor alle gebruikers worden aangebracht.

Wanneer u terugkeert naar het rolcentrum, ziet u daar het bijgewerkte rapport verschijnen. Als u **Opslaan als** hebt gebruikt, moet u eerst de actie **Rapport selecteren** kiezen en vervolgens het nieuwe rapport inschakelen om het weer te geven.

> [!NOTE]
> Deze mogelijkheid is niet beschikbaar voor [!INCLUDE [prod_short](includes/prod_short.md)] on-premises.

### <a name="upload"></a>Rapporten uploaden

Power BI-rapporten kunnen onder gebruikers worden verspreid als PBIX-bestanden. Als u PBIX-bestanden hebt, kunt u deze uploaden en delen met alle gebruikers van [!INCLUDE [prod_short](includes/prod_short.md)]. De rapporten worden binnen elk bedrijf binnen gedeeld in [!INCLUDE [prod_short](includes/prod_short.md)].  

Als u een rapport wilt uploaden, kiest u de actie **Rapport uploaden** in de vervolgkeuzelijst met opdrachten in het gedeelte **Power BI-rapporten**. Ga vervolgens op zoek naar het PBIX-bestand dat de rapporten definieert die u wilt delen. U kunt de standaardnaam van het bestand wijzigen.  

Nadat het rapport is geüpload naar uw Power BI-werkruimte, wordt het automatisch geüpload naar de Power BI-werkruimten van andere gebruikers.

> [!NOTE]
> Om een rapport te kunnen uploaden, moet u de machtigingen van een SUPER-gebruiker hebben in [!INCLUDE[prod_short](includes/prod_short.md)]. Ook kunt u geen rapporten uploaden met [!INCLUDE [prod_short](includes/prod_short.md)] on-premises. Met on-premises moet u rapporten rechtstreeks naar uw Power BI-werkruimte uploaden. Zie [Werken met [!INCLUDE [prod_short](includes/prod_short.md)]-gegevens in Power BI](across-working-with-business-central-in-powerbi.md) voor meer informatie.

## Problemen oplossen

Als er echter iets verkeerd gaat, biedt deze sectie een oplossing voor de meest voorkomende problemen.  

### U hebt geen Power BI-account

Er is geen Power BI-account ingesteld. Als u een geldig Power BI-account wilt aanvragen, moet u een licentie hebben en moet u zich eerder hebben aangemeld bij Power BI om een Power BI-werkruimte te maken.

### Bericht: Er zijn geen ingeschakelde rapporten. Kies Rapport selecteren om een lijst met rapporten te tonen die u kunt weergeven.

Dit bericht verschijnt als het standaardrapport niet kon worden geïmplementeerd in uw Power BI-werkruimte. Het bericht wordt ook weergegeven als het rapport is geïmplementeerd maar kon worden vernieuwd. Navigeer naar het rapport in uw Power BI-werkruimte, selecteer **Gegevensset**, **Instellingen** en werk vervolgens de referenties handmatig bij. Nadat de gegevensset met succes is vernieuwd, navigeert u terug naar [!INCLUDE[prod_short](includes/prod_short.md)] en selecteert u handmatig het rapport via de pagina **Rapporten selecteren**.

#### U kunt geen rapport zien op de pagina Rapport selecteren op een lijstpagina

Dit komt waarschijnlijk omdat de naam van het rapport niet de naam van de lijstpagina bevat. Wis het filter om de volledige lijst met beschikbare Power BI-rapporten weer te geven.

## Zie ook

[Business Central en Power BI](admin-powerbi.md)  
[Power BI-rapporten maken om [!INCLUDE [prod_long](includes/prod_long.md)]-gegevens weer te geven](across-how-use-financials-data-source-powerbi.md)  
[Power BI-integratieonderdeel en architectuuroverzicht voor [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Werken met [!INCLUDE [prod_short](includes/prod_short.md)]-gegevens in Power BI](across-working-with-business-central-in-powerbi.md)  
[Power BI voor consumenten](/power-bi/consumer/end-user-consumer)  
[De 'nieuwe look' van de Power BI-service](/power-bi/service-new-look)  
[Snelle start: verbinding maken met uw gegevens in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI-documentatie](/power-bi/)  
[Bedrijfsinformatie](bi.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Instellen van [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken als Power Apps-gegevensbron](across-how-use-financials-data-source-powerapps.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken in Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]
