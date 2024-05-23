---
title: Power BI-integratie met Business Central inschakelen
description: 'Leer hoe u de verbinding met Power BI instelt. Met Power BI-rapporten kunt u inzicht, bedrijfsinformatie en KPI''s krijgen uit uw Business Central-gegevens.'
author: jswymer
ms.topic: get-started
ms.search.keywords: 'Power BI, setup, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 01/28/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="enabling-power-bi-integration-with-"></a>Power BI-integratie met [!INCLUDE[prod_short](includes/prod_short.md)] mogelijk maken

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

In dit artikel wordt beschreven hoe u [!INCLUDE[prod_short](includes/prod_short.md)] gereedmaakt voor integratie met Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online is al gereedgemaakt voor integratie, hoewel er enige informatie over licenties beschikbaar is die u misschien wilt lezen. Voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises moet u uw omgeving zodanig instellen dat deze verbinding kan maken met Power BI voordat gebruikers ermee kunnen werken.

## <a name="power-bi-licensing"></a><a name="license"></a>Power BI-licenties

Bij [!INCLUDE[prod_short](includes/prod_short.md)] krijgen gebruikers een gratis Power BI-licentie die toegang biedt tot de meest voorkomende functies in [!INCLUDE[prod_short](includes/prod_short.md)] en Power BI. U kunt ook een Power BI Pro-licentie aanschaffen die toegang biedt tot extra functies. De volgende tabel geeft een overzicht van de functies die beschikbaar zijn bij elke licentie.

|Power-licentie|Rapporten weergeven|Rapporten maken|Rapporten delen|Rapporten vernieuwen| [!INCLUDE[prod_short](includes/prod_short.md)]-apps|
|-------------|--------||
|Power BI gratis|![een vinkje.](media/check.png)|![nog een vinkje](media/check.png)|(beperkt)|(beperkt)||
|Power BI Pro|![nog een vinkje.](media/check.png)|![het is een vinkje](media/check.png)|![weer een vinkje](media/check.png)|(uitgebreid)|![laatste vinkje](media/check.png)|

Zie [Licenties voor de Power BI-service voor gebruikers in uw organisatie](/power-bi/admin/service-admin-licensing-organization) of [U aanmelden voor de Power BI-service als individu](/power-bi/fundamentals/service-self-service-signup-for-power-bi) voor meer informatie.

## <a name="expose-data-through-api-or-odata-web-services"></a><a name="exposedata"></a>Gegevens beschikbaar stellen via API of OData-webservices

Business Central biedt twee manieren om gegevens beschikbaar te stellen die kunnen worden gebruikt door Power BI-rapporten of -query's: API-pagina's en Open Data Protocol (OData) webservices.

### <a name="api-pages-and-queries"></a>API-pagina's en query's

> **VAN TOEPASSING OP:** alleen Business Central online

Ontwikkelaars kunnen paginaobjecten en queryobjecten definiëren van het type *API*. Op deze manier kunnen ze gegevens uit databasetabellen blootleggen via een door webhook ondersteunde, OData v4-enabled REST-service. Dit type gegevens kan niet worden weergegeven in de gebruikersinterface, maar is bedoeld voor het bouwen van betrouwbare integratieservices.

Business Central online wordt geleverd met een set ingebouwde API's, die u kunt gebruiken om gegevens op te halen voor de meest voorkomende zakelijke entiteiten, zoals klanten, artikelen, verkooporders en meer. Er is geen extra werk of configuratie vereist om deze API's als gegevensbron te gebruiken voor Power BI-rapporten. Voor meer informatie over deze API's zie [Business Central API V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

Business Central online ondersteunt ook aangepaste API's. Applicatieontwikkelaars van Business Central-oplossingen kunnen hun eigen API-pagina's en -query's maken en deze in apps verpakken. U installeert de apps vervolgens in uw tenant. Eenmaal geïnstalleerd kunt u de API-pagina's gebruiken voor uw Power BI-rapporten, zoals u zou doen met de ingebouwde API's (v2.0). Zie voor meer informatie over het maken van een API-pagina door pagina's of query's toegankelijk te maken [Een aangepaste API ontwikkelen](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

> [!IMPORTANT]
> Vanaf februari 2022 zijn Power BI-rapporten voor [!INCLUDE[prod_short](includes/prod_short.md)] online om prestatieredenen afkomstig van een secundaire, alleen-lezen databasereplica. Daarom moeten AL-ontwikkelaars vermijden om API-pagina's te ontwerpen die databasewijzigingen aanbrengen terwijl de pagina's records openen of laden. Overweeg met name de code van de AL-triggers: OnInit, OnOpenPage, OnFindRecord, OnNextRecord, OnAfterGetRecord en OnAfterGetCurrRecord. Deze databasewijzigingen kunnen in sommige gevallen prestatieproblemen veroorzaken en voorkomen dat het rapport gegevens ververst. Zie voor meer informatie [Prestatieartikelen voor ontwikkelaars](/dynamics365/business-central/dev-itpro/performance/performance-developer?branch=main#writing-efficient-web-services) in de ontwikkelingsinhoud van Business Central.
>
> In zeldzame gevallen zal het gedrag een fout veroorzaken wanneer een gebruiker gegevens probeert op te halen vanuit de API voor een rapport in Power BI Desktop. Als er echter wijzigingen in de database nodig zijn in de aangepaste API, kunnen Power BI Desktop-gebruikers het gedrag forceren. Zie voor meer informatie [Power BI-rapporten maken om Business Central-gegevens weer te geven](across-how-use-financials-data-source-powerbi.md#fixing-problems).

### <a name="odata-web-services"></a>OData-webservices

U kunt Business Central-toepassingsobjecten, zoals codeunits, pagina's en query's, publiceren als [OData-webservices](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). Met Business Central online worden standaard veel webservices gepubliceerd. Een eenvoudige manier om de webservices te vinden is te zoeken naar *webservices* in [!INCLUDE[prod_short](includes/prod_short.md)]. Zorg dat op de pagina **Webservices** het veld **Publiceren** is geselecteerd voor de hierboven genoemde webservices. Zie [Een webservice publiceren](across-how-publish-web-service.md) voor meer informatie over het publiceren van webservices.

Als u wilt weten wat u kunt doen om ervoor te zorgen dat de webservices optimaal presteren, gezien vanuit de Business Central-server (het eindpunt) en vanuit de consument (de client), leest u [Efficiënte webservices creëren](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).

### <a name="choosing-whether-to-use-api-pages-or-odata-web-services"></a>Kiezen of u API-pagina's of OData-webservices wilt gebruiken

Waar mogelijk wordt u aangemoedigd om API-pagina's te gebruiken in plaats van de OData-webservice. API-pagina's zijn sneller in het laden van gegevens in Power BI-rapporten dan OData-webservices. Bovendien zijn ze flexibeler omdat u gegevens kunt ophalen uit tabelvelden die niet in een paginaobject zijn gedefinieerd.

<!--## <a name="setup"></a>Set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for Power BI integration

This section explains the requirements for a [!INCLUDE[prod_short](includes/prod_short.md)] on-premises deployment to integrate with Power BI.

1. Configure either [NavUserPassword](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-navuserpassword) or [Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-ad-overview) as the authentication method for the deployment.  
    
    > [!NOTE]
    > Power BI integration doesn't support Windows authentication and is not supported on Windows Client.

2. Enable OData web services and the ODataV4 endpoint.

    OData web service must be enabled on the [!INCLUDE[server](includes/server.md)], and OData port opened in firewall. For more information, see [Configuring Business Central Server - OData Web Services](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    The local server must be accessible from the Internet.

3. Give [!INCLUDE[prod_short](includes/prod_short.md)] user accounts a web service access key.

    A web service access key is only needed to view [!INCLUDE[prod_short](includes/prod_short.md)] data in Power BI. You can assign a web service access key to each user account. Or instead, create a specific account with a web service access key for use by all users. For more information, see [Web Services Authentication](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

    <!--
    > [!IMPORTANT]
    > With [!INCLUDE[prod_short](../developer/includes/prod_short.md)] online, the use of access keys (Basic Auth) for web service authentication is [deprecated](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#accesskeys). We recommend that you use OAuth2 instead. For more information, see [Use OAuth to Authorize Business Central Web Services](/dynamics365/business-central/dev-itpro/webservices/authenticate-web-services-using-oauth).-->

<!--4. Create an application registration for [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure.

    To view Power BI reports embedded in [!INCLUDE[prod_short](includes/prod_short.md)] pages, an application must be registered for [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure. The registered application needs permission to Power BI services. At a minimum, the app requires  **User.ReadWrite.All** permission. For users to view reports from shared Power BI workspaces, the app requires **Workspace.Read.All** permission. For more information, see [Registering [!INCLUDE[prod_short](includes/prod_short.md)] On-Premises in Microsoft Entra ID for Integrating with Other Services](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > If your deployment uses NavUserPassword authentication, [!INCLUDE[prod_short](includes/prod_short.md)] connects to the same Power BI service for all users. You'll specify this service account as part of registering the application. With Microsoft Entra authentication, [!INCLUDE[prod_short](includes/prod_short.md)] connects to the Power BI service associated with the individual user accounts.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
<!--5. Make the initial connection from Business Central to Power BI.

    Before end-users can use Power BI in [!INCLUDE[prod_short](includes/prod_short.md)], an Azure application administrator will have to give consent to the Power BI service.

    To make the initial connection, open [!INCLUDE[prod_short](includes/prod_short.md)], and run **Get Started with Power BI** from the Home page. This action will lead you through the consent process, and check your Power BI license. When prompted sign in using an Microsoft Entra admin account. For more information, see [Connect to Power BI - one time only](across-working-with-powerbi.md#connect).-->

## <a name="setting-up-dataflows"></a>Gegevensstromen instellen

Met gegevensstromen kunt u gegevens opnemen, transformeren en laden in een Power BI-werkruimte en de gegevens vervolgens gebruiken als basis voor uw rapporten. Deze gegevensstromen kunnen in sommige gevallen tijdelijke fouten ondervinden tijdens het uitvoeren van een geplande vernieuwing. De foutmelding ziet er als volgt uit: `DataSource.Error: OData: Unable to read data from the transport connection: An existing connection was forcibly closed by the remote host.` 

Met Power Automate kunt u nieuwe pogingen voor deze situatie instellen. Zie [Een gegevensstroom automatisch opnieuw proberen bij een fout](/power-query/dataflows/automatically-retry-dataflow) voor meer informatie.

## <a name="see-also"></a>Zie ook

[Business Central en Power BI](admin-powerbi.md)  
[Power BI-integratieonderdeel en architectuuroverzicht voor [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Power BI voor consumenten](/power-bi/consumer/end-user-consumer)  
[De 'nieuwe look' van de Power BI-service](/power-bi/service-new-look)  
[Snelle start: verbinding maken met uw gegevens in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI-documentatie](/power-bi/)  
[Bedrijfsinformatie](bi.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Instellen van [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken als Power BI-gegevensbron](across-how-use-financials-data-source-powerbi.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken als Power Apps-gegevensbron](across-how-use-financials-data-source-powerapps.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken in Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]
