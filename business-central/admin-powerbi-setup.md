---
title: Power BI-integratie met Business Central inschakelen
description: 'Leer hoe u de verbinding met Power BI instelt. Met Power BI-rapporten kunt u inzicht, bedrijfsinformatie en KPI''s krijgen uit uw Business Central-gegevens.'
author: jswymer
ms.topic: get-started
ms.search.keywords: 'Power BI, setup, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 09/28/2023
ms.author: jswymer
---
# Power BI-integratie met [!INCLUDE[prod_short](includes/prod_short.md)] mogelijk maken

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

In dit artikel wordt beschreven hoe u [!INCLUDE[prod_short](includes/prod_short.md)] gereedmaakt voor integratie met Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online is al gereedgemaakt voor integratie, hoewel er enige informatie over licenties beschikbaar is die u misschien wilt lezen. Voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises moet u uw omgeving zodanig instellen dat deze verbinding kan maken met Power BI voordat gebruikers ermee kunnen werken.

## <a name="license"></a>Power BI-licenties

Bij [!INCLUDE[prod_short](includes/prod_short.md)] krijgen gebruikers een gratis Power BI-licentie die toegang biedt tot de meest voorkomende functies in [!INCLUDE[prod_short](includes/prod_short.md)] en Power BI. U kunt ook een Power BI Pro-licentie aanschaffen die toegang biedt tot extra functies. De volgende tabel geeft een overzicht van de functies die beschikbaar zijn bij elke licentie.

|Power-licentie|Rapporten weergeven|Rapporten maken|Rapporten delen|Rapporten vernieuwen| [!INCLUDE[prod_short](includes/prod_short.md)]-apps|
|-------------|--------||
|Power BI gratis|![een vinkje.](media/check.png)|![nog een vinkje](media/check.png)|(beperkt)|(beperkt)||
|Power BI Pro|![nog een vinkje.](media/check.png)|![het is een vinkje](media/check.png)|![weer een vinkje](media/check.png)|(uitgebreid)|![laatste vinkje](media/check.png)|

Zie [Licenties voor de Power BI-service voor gebruikers in uw organisatie](/power-bi/admin/service-admin-licensing-organization) of [U aanmelden voor de Power BI-service als individu](/power-bi/fundamentals/service-self-service-signup-for-power-bi) voor meer informatie.

## <a name="exposedata"></a>Gegevens beschikbaar stellen via API of OData-webservices

Business Central biedt twee manieren om gegevens beschikbaar te stellen die kunnen worden gebruikt door Power BI-rapporten of -query's: API-pagina's en Open Data Protocol (OData) webservices.

### API-pagina's en query's

> **VAN TOEPASSING OP:** alleen Business Central online

Ontwikkelaars kunnen paginaobjecten en queryobjecten definiëren van het type *API*. Op deze manier kunnen ze gegevens uit databasetabellen blootleggen via een door webhook ondersteunde, OData v4-enabled REST-service. Dit type gegevens kan niet worden weergegeven in de gebruikersinterface, maar is bedoeld voor het bouwen van betrouwbare integratieservices.

Business Central online wordt geleverd met een set ingebouwde API's, die u kunt gebruiken om gegevens op te halen voor de meest voorkomende zakelijke entiteiten, zoals klanten, artikelen, verkooporders en meer. Er is geen extra werk of configuratie vereist om deze API's als gegevensbron te gebruiken voor Power BI-rapporten. Voor meer informatie over deze API's zie [Business Central API V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

Business Central online ondersteunt ook aangepaste API's. Applicatieontwikkelaars van Business Central-oplossingen kunnen hun eigen API-pagina's en -query's maken en deze in apps verpakken. U installeert de apps vervolgens in uw tenant. Eenmaal geïnstalleerd kunt u de API-pagina's gebruiken voor uw Power BI-rapporten, zoals u zou doen met de ingebouwde API's (v2.0). Zie voor meer informatie over het maken van een API-pagina door pagina's of query's toegankelijk te maken [Een aangepaste API ontwikkelen](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

> [!IMPORTANT]
> Vanaf februari 2022 zijn Power BI-rapporten voor [!INCLUDE[prod_short](includes/prod_short.md)] online om prestatieredenen afkomstig van een secundaire, alleen-lezen databasereplica. Daarom moeten AL-ontwikkelaars vermijden om API-pagina's te ontwerpen die databasewijzigingen aanbrengen terwijl de pagina's records openen of laden. Overweeg met name de code van de AL-triggers: OnInit, OnOpenPage, OnFindRecord, OnNextRecord, OnAfterGetRecord en OnAfterGetCurrRecord. Deze databasewijzigingen kunnen in sommige gevallen prestatieproblemen veroorzaken en voorkomen dat het rapport gegevens ververst. Zie voor meer informatie [Prestatieartikelen voor ontwikkelaars](/dynamics365/business-central/dev-itpro/performance/performance-developer?branch=main#writing-efficient-web-services) in de ontwikkelingsinhoud van Business Central.
>
> In zeldzame gevallen zal het gedrag een fout veroorzaken wanneer een gebruiker gegevens probeert op te halen vanuit de API voor een rapport in Power BI Desktop. Als er echter wijzigingen in de database nodig zijn in de aangepaste API, kunnen Power BI Desktop-gebruikers het gedrag forceren. Zie voor meer informatie [Power BI-rapporten maken om Business Central-gegevens weer te geven](across-how-use-financials-data-source-powerbi.md#fixing-problems).

### OData-webservices

U kunt Business Central-toepassingsobjecten, zoals codeunits, pagina's en query's, publiceren als [OData-webservices](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). Met Business Central online worden standaard veel webservices gepubliceerd. Een eenvoudige manier om de webservices te vinden is te zoeken naar *webservices* in [!INCLUDE[prod_short](includes/prod_short.md)]. Zorg dat op de pagina **Webservices** het veld **Publiceren** is geselecteerd voor de hierboven genoemde webservices. Zie [Een webservice publiceren](across-how-publish-web-service.md) voor meer informatie over het publiceren van webservices.

Als u wilt weten wat u kunt doen om ervoor te zorgen dat de webservices optimaal presteren, gezien vanuit de Business Central-server (het eindpunt) en vanuit de consument (de client), leest u [Efficiënte webservices creëren](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).

### Kiezen of u API-pagina's of OData-webservices wilt gebruiken

Waar mogelijk wordt u aangemoedigd om API-pagina's te gebruiken in plaats van de OData-webservice. API-pagina's zijn over het algemeen sneller in het laden van gegevens in Power BI-rapporten dan OData-webservices. Bovendien zijn ze flexibeler omdat u gegevens kunt ophalen uit tabelvelden die niet in een paginaobject zijn gedefinieerd.

## <a name="setup"></a>[!INCLUDE[prod_short](includes/prod_short.md)] on-premises configureren voor integratie met Power BI

In dit gedeelte wordt uitgelegd wat de vereisten zijn voor de integratie van een implementatie van [!INCLUDE[prod_short](includes/prod_short.md)] on-premises met Power BI.

1. Configureer [NavUserPassword](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-navuserpassword) of [Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-ad-overview) als de verificatiemethode voor de implementatie.  
    
    > [!NOTE]
    > Power BI-integratie ondersteunt geen Windows-verificatie en wordt niet ondersteund op Windows Client.

2. Schakel OData-webservices en het ODataV4-eindpunt in.

    De OData-webservice moet zijn ingeschakeld op de [!INCLUDE[server](includes/server.md)] en de OData-poort moet zijn geopend in firewall. Zie [Business Central Server configureren - OData-webservices](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices) voor meer informatie.

    De lokale server moet toegankelijk zijn vanaf internet.

3. Geef [!INCLUDE[prod_short](includes/prod_short.md)]-gebruikersaccounts een toegangssleutel voor de webservice.

    Er is alleen een toegangssleutel voor de webservice nodig om [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens weer te geven in Power BI. U kunt aan elk gebruikersaccount een webservicetoegangssleutel toewijzen. U kunt in plaats daarvan ook een specifiek account maken met webservicetoegangssleutel die door alle gebruikers kan worden gebruikt. Zie [Verificatie voor webservices](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key) voor meer informatie.

    <!--
    > [!IMPORTANT]
    > With [!INCLUDE[prod_short](../developer/includes/prod_short.md)] online, the use of access keys (Basic Auth) for web service authentication is [deprecated](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#accesskeys). We recommend that you use OAuth2 instead. For more information, see [Use OAuth to Authorize Business Central Web Services](/dynamics365/business-central/dev-itpro/webservices/authenticate-web-services-using-oauth).-->

4. Maak een toepassingsregistratie voor [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure.

    Voor het weergeven van Power BI-rapporten die zijn ingesloten in [!INCLUDE[prod_short](includes/prod_short.md)]-pagina's, moet een toepassing zijn geregistreerd voor [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure. De geregistreerde toepassing heeft toestemming nodig voor Power BI-services. De app vereist minimaal de machtiging **User.ReadWrite.All**. Als gebruikers rapporten van gedeelde Power BI-werkruimten willen kunnen bekijken, vereist de app de machtiging **Workspace.Read.All**. Zie [[!INCLUDE[prod_short](includes/prod_short.md)] on-premises registreren in Microsoft Entra ID voor integratie met andere services](/dynamics365/business-central/dev-itpro/administration/register-app-azure) voor meer informatie.

    > [!NOTE]
    > Als voor uw implementatie NavUserPassword-verificatie wordt gebruikt, maakt [!INCLUDE[prod_short](includes/prod_short.md)] verbinding met dezelfde Power BI-service voor alle gebruikers. U kunt dit serviceaccount specificeren bij het registreren van de toepassing. Als er Microsoft Entra-verificatie wordt gebruikt, maakt [!INCLUDE[prod_short](includes/prod_short.md)] verbinding met de Power BI-service die is gekoppeld aan de individuele gebruikersaccounts.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Maak de eerste verbinding van Business Central met Power BI.

    Voordat eindgebruikers Power BI in [!INCLUDE[prod_short](includes/prod_short.md)] kunnen gebruiken, zal een Azure-applicatiebeheerder toestemming moeten geven voor de Power BI-service.

    Open om de eerste verbinding te maken [!INCLUDE[prod_short](includes/prod_short.md)] en voer **Aan de slag met Power BI** uit vanaf de startpagina. Deze actie leidt u door het toestemmingsproces en controleert uw Power BI-licentie. Meld u aan met een Microsoft Entra-beheerdersaccount wanneer daarom wordt gevraagd. Zie voor meer informatie [Verbinding maken met Power BI - eenmalig](across-working-with-powerbi.md#connect).

## Zie ook

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
