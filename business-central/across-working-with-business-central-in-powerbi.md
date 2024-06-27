---
title: Verbinding met Power BI maken vanuit Business Central on-premises | Microsoft Docs
description: 'Met Power BI kunt u eenvoudig inzicht verwerven, bedrijfsinformatie genereren en KPI''s vaststellen op basis van uw Business Central-gegevens.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 01/22/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# Verbinding met Power BI maken vanuit Business Central on-premises

<!--In this article, you learn some of the basics about working with reports and dashboards in Power BI that use [!INCLUDE [prod_short](includes/prod_short.md)] as a data source. The article discusses some aspects that will help you get started as a [!INCLUDE[prod_short](includes/prod_short.md)] user. For general guidelines and instructions about using Power BI, see [Power BI documentation for consumers](/power-bi/consumer).

## Get ready

Sign up for the Power BI service. If you haven't already signed up, go to [https://powerbi.microsoft.com](https://powerbi.microsoft.com). When you sign up, use a work email address and password.-->

## Aan de slag

Als u [!INCLUDE [prod_short](includes/prod_short.md)] on-premises wilt gebruiken, moet Power BI-integratie zijn ingeschakeld. Deze taak wordt doorgaans uitgevoerd door een beheerder. Voor meer informatie over het inschakelen van Power BI-integratie met Business Central online, zie [Business Central on-premises instellen voor Power BI-integratie](admin-powerbi-setup.md).

Sommige functies zijn alleen beschikbaar met Business Central Online en niet met on-premises. Zie voor meer informatie [Inleiding in Business Central en Power BI](admin-powerbi.md#what-you-can-do-with-power-bi-and-business-central)

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

4. Maak een toepassingsregistratie voor [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure.

    Voor het weergeven van Power BI-rapporten die zijn ingesloten in [!INCLUDE[prod_short](includes/prod_short.md)]-pagina's, moet een toepassing zijn geregistreerd voor [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure. De geregistreerde toepassing heeft toestemming nodig voor Power BI-services. De app vereist minimaal de machtiging **User.ReadWrite.All**. Als gebruikers rapporten van gedeelde Power BI-werkruimten willen kunnen bekijken, vereist de app de machtiging **Workspace.Read.All**. Zie [[!INCLUDE[prod_short](includes/prod_short.md)] on-premises registreren in Microsoft Entra ID voor integratie met andere services](/dynamics365/business-central/dev-itpro/administration/register-app-azure) voor meer informatie.

    > [!NOTE]
    > Als voor uw implementatie NavUserPassword-verificatie wordt gebruikt, maakt [!INCLUDE[prod_short](includes/prod_short.md)] verbinding met dezelfde Power BI-service voor alle gebruikers. U kunt dit serviceaccount specificeren bij het registreren van de toepassing. Als er Microsoft Entra-verificatie wordt gebruikt, maakt [!INCLUDE[prod_short](includes/prod_short.md)] verbinding met de Power BI-service die is gekoppeld aan de individuele gebruikersaccounts.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Maak de eerste verbinding van Business Central met Power BI.

    Voordat eindgebruikers Power BI in [!INCLUDE[prod_short](includes/prod_short.md)] kunnen gebruiken, zal een Azure-applicatiebeheerder toestemming moeten geven voor de Power BI-service.

    Open om de eerste verbinding te maken [!INCLUDE[prod_short](includes/prod_short.md)] en voer **Aan de slag met Power BI** uit vanaf de startpagina. Deze actie leidt u door het toestemmingsproces en controleert uw Power BI-licentie. Meld u aan met een Microsoft Entra-beheerdersaccount wanneer daarom wordt gevraagd. Zie voor meer informatie [Verbinding maken met Power BI - eenmalig](across-working-with-powerbi.md#connect).

## Power BI-rapporten maken om [!INCLUDE [prod_long](includes/prod_long.md)]-gegevens weer te geven

U kunt uw Dynamics 365 Business Central-gegevens als gegevensbron beschikbaar maken in Power BI Desktop en krachtige rapporten maken met de status van uw bedrijf.

Power BI Desktop gebruiken om rapporten te maken voor het weergeven van Dynamics 365 Business Central-gegevens. Nadat u rapporten hebt gemaakt, kunt u deze publiceren via uw Power BI-service of delen met alle gebruikers in uw organisatie. Zodra deze rapporten zich in de Power BI-service bevinden, kunnen gebruikers die ervoor zijn ingesteld, vervolgens de rapporten bekijken in Dynamics 365 Business Central.

- Zorg dat u voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises over de volgende informatie beschikt:

  - De OData-URL voor [!INCLUDE[prod_short](includes/prod_short.md)].
  
    Deze URL heeft doorgaans de indeling `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, bijvoorbeeld `https://localhost:7048/BC190/ODataV4`. Als u een implementatie met meerdere tenants hebt, neemt u de tenant op in de URL, bijvoorbeeld `https://localhost:7048/BC190/ODataV4?tenant=tenant1`.
  - Een gebruikersnaam en een webservicetoegangssleutel van een [!INCLUDE[prod_short](includes/prod_short.md)]-account.

    Power BI maakt gebruik van basisverificatie om gegevens op te halen uit [!INCLUDE[prod_short](includes/prod_short.md)]. U hebt dus een gebruikersnaam en een webservicetoegangssleutel nodig om verbinding te maken. Het account kan uw eigen gebruikersaccount zijn. Het kan ook zijn dat uw organisatie een specifiek account heeft voor dit doel.

## <a name="getdata"></a>[!INCLUDE[prod_short](includes/prod_short.md)] als gegevensbron toevoegen in Power BI Desktop

De eerste taak bij het maken van rapporten is het toevoegen van [!INCLUDE[prod_short](includes/prod_short.md)] als een gegevensbron in Power BI Desktop. Als de verbinding tot stand is gebracht, kunt u beginnen met het maken van het rapport.

1. Start Power BI Desktop.
2. Selecteer **Gegevens ophalen**.

    Als u de optie **Gegevens ophalen** niet ziet, selecteert u het menu **Bestand** en vervolgens de optie **Gegevens ophalen**.
3. Selecteer op de pagina **Gegevens ophalen** de optie **Onlineservices**.
4. Maak in het deelvenster **Onlineservices** verbinding met [!INCLUDE [prod_short](includes/prod_short.md)] on-premises, selecteer **Dynamics 365 Business Central (on-premises)** en vervolgens **Verbinden**.
5. Meld u aan bij [!INCLUDE [prod_short](includes/prod_short.md)] (eenmalig).

    Als u zich niet eerder hebt aangemeld bij [!INCLUDE [prod_short](includes/prod_short.md)] vanuit Power BI desktop, wordt u gevraagd zich aan te melden.

   - Voor [!INCLUDE [prod_short](includes/prod_short.md)] on-premises voert u eerst de OData-URL in voor [!INCLUDE[prod_short](includes/prod_short.md)] en selecteert u vervolgens **OK**. Voer wanneer daarom wordt gevraagd de gebruikersnaam en het wachtwoord in van het account dat u wilt gebruiken voor het maken van verbinding met [!INCLUDE[prod_short](includes/prod_short.md)]. Voer in het vak **Wachtwoord** de toegangssleutel voor de webservice in. Wanneer u klaar bent, selecteert u **Verbinden**.
   
    > [!NOTE]  
    > Zodra u met succes verbinding hebt gemaakt met [!INCLUDE[prod_short](includes/prod_short.md)], wordt u niet opnieuw gevraagd zich aan te melden. [Hoe wijzig of wis ik het account dat ik momenteel gebruik om verbinding te maken met Business Central vanuit Power BI Desktop?](/dynamics365/business-central/power-bi-faq?tabs=designer#perms)

6. Eenmaal verbonden neemt Power BI contract op met de Business Central-service. Het **navigatie**venster verschijnt en toont beschikbare gegevensbronnen voor het maken van rapporten. Selecteer een map om deze uit te vouwen en de beschikbare gegevensbronnen te bekijken. 

   Deze gegevensbronnen vertegenwoordigen alle webservices en API-pagina's die zijn gepubliceerd vanuit [!INCLUDE [prod_short](includes/prod_short.md)]. De gegevensbronnen zijn gegroepeerd op de Business Central-omgevingen en -bedrijven.

   > [!NOTE]
    > De structuur voor Business Central on-premises is anders omdat het geen API-pagina's ondersteunt.

7. Selecteer de gegevensbron of -bronnen die u aan uw gegevensmodel wilt toevoegen en selecteer vervolgens de knop **Laden**.
8. Als u later meer Business Central-gegevens wilt toevoegen, kunt u de vorige stappen herhalen.

Zodra de gegevens zijn geladen, ziet u deze in de rechternavigatie op de pagina. U hebt nu met succes verbinding gemaakt met uw [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens en u kunt uw Power BI-rapport gaan maken.  

> [!TIP]
> Zie [Aan de slag met Power BI Desktop](/power-bi/fundamentals/desktop-getting-started) voor meer informatie over het gebruik van Power BI Desktop.

## Rapporten beheren en wijzigen

> [!NOTE]
> U kunt geen rapporten beheren en wijzigen. 

## Rapporten uploaden

Voor [!INCLUDE [prod_short](includes/prod_short.md)] on-premises zijn er geen demorapporten beschikbaar, dus u zult opnieuw moeten beginnen met Power BI Desktop. Als alternatief kunnen Power BI-rapporten worden gedistribueerd als bestanden die u rechtstreeks vanuit Power BI online service kunt uploaden. Zie [Het rapport uploaden naar de service](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service) voor meer informatie.

<!--
> [!NOTE]
> Uploading a report requires that you have SUPER user permissions in [!INCLUDE[prod_short](includes/prod_short.md)]. Also, you can't upload reports with [!INCLUDE [prod_short](includes/prod_short.md)] on-premises. With on-premises, you upload reports directly to your Power BI workspace. For more information, see [Connect to Power BI from [!INCLUDE [prod_short](includes/prod_short.md)] on-premises](across-working-with-business-central-in-powerbi.md).

<!--Once you have a Power BI account, you can sign in at [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

The Power BI service hosts all the reports available to you. To see the report, select **My Workspace** > **Reports**. Then just select the report that you want to view.

With [!INCLUDE[prod_short](includes/prod_short.md)] online, you'll automatically have a set of default reports on your workspace. If you want to create your own reports, you can use Power BI Desktop to create reports, and then publish them to your workspace. For more information, see [Getting Started Building Reports in Power BI Desktop to Display [!INCLUDE [prod_long](includes/prod_long.md)] Data](across-how-use-financials-data-source-powerbi.md).

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

If you're using [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, you'll have to start from scratch by using Power BI Desktop. Optionally, Power BI reports can be distributed as files, that you can upload.

<!--## Get the latest data

Each Power BI report is based on a dataset that gets data from the [!INCLUDE[prod_short](includes/prod_short.md)] sources. You want to make sure that the data in your Power BI reports is up to date with the data in [!INCLUDE[prod_short](includes/prod_short.md)]. This concept is referred to as *refreshing*.  Depending on how your organization has set up Power BI, refreshing might not happen automatically. There are two ways to refresh data: manually or by scheduling a refresh. Manual refreshing is done on-demand, as needed. Scheduled refreshing lets you refresh automatically at defined time intervals.

### Refresh manually

In the navigation pane, under **Datasets**, select **More options (...)** next to the dataset, then select **Refresh now**.

### Schedule a refresh

In the navigation pane, under Datasets, select More options (...) next to the dataset, then select **Schedule refresh**. Fill in the information under the **Schedule refresh** section, and select **Apply**.

For more information, see [Configure scheduled refresh](/power-bi/connect-data/refresh-scheduled-refresh)-->

<!--## <a name="upload"></a>Upload reports from files

Power BI Reports can be distributed among users as .pbix files. If you have a .pbix file, you can upload the file to a workspace. To upload a report, do the following steps:

1. In your new workspace, select **Get Data**.

2. In the Files box, select **Get**.

3. Select **Local File**, navigate to where you saved the file, and select **Open**.

For more information, see [Upload the report to the service](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

> [!NOTE]
> Uploading a report requires that you have a [Premium capacity](/power-bi/service-premium-what-is) work space. For more information, see [Managing Premium capacities](/power-bi/admin/service-premium-capacity-manage). 

> [!TIP]
> If you're using [!INCLUDE[prod_short](includes/prod_short.md)] online, you can also upload a report from within [!INCLUDE[prod_short](includes/prod_short.md)]. For more information, see [Work with Power BI Reports in [!INCLUDE [prod_short](includes/prod_short.md)] - Upload Reports](across-working-with-powerbi.md#upload).

## <a name="share"></a>Share reports with others

Once a report is in your workspace, you can share it with others in your organization.

To share a report, in a list reports, or in an open report, select **Share**. In the **Share report** pane, enter the full email addresses for individuals or distribution groups you want to share with. Follow the instructions on screen to complete the sharing. For more information, see [Share a dashboard or report](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

> [!NOTE]
> You must have  [Power BI Pro license](/power-bi/service-features-license-type), and the people you share with do too. The content must be in a workspace in a [Premium capacity](/power-bi/service-premium-what-is). For more information, see [Ways to share your work in Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).-->

## Zie ook

[Business Central en Power BI](admin-powerbi.md)  
[Rapporten uploaden](across-working-with-business-central-in-powerbi.md#upload-reports)
 
[!INCLUDE[footer-include](includes/footer-banner.md)]
