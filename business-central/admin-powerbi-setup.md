---
title: Power BI-integratie met Business Central inschakelen
description: Leer hoe u de verbinding met Power Bi instelt, zodat u inzichten, business intelligence en KPI's uit uw Business Central-gegevens kunt halen met de Business Central-apps voor Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: dd0974c20f8c038fcc0cac27c9ef165b2aadcd36
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752512"
---
# <a name="enabling-power-bi-integration-with-prod_short"></a>Power BI-integratie met [!INCLUDE[prod_short](includes/prod_short.md)] mogelijk maken

In dit artikel wordt beschreven hoe u [!INCLUDE[prod_short](includes/prod_short.md)] gereedmaakt voor integratie met Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online is al gereedgemaakt voor integratie, hoewel er enige informatie over licenties beschikbaar is die u misschien wilt lezen. Voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises moet u uw omgeving zodanig instellen dat deze verbinding kan maken met Power BI voordat gebruikers ermee kunnen werken.

## <a name="power-bi-licensing"></a><a name="license"></a>Power BI-licenties

Bij [!INCLUDE[prod_short](includes/prod_short.md)] krijgen gebruikers een gratis Power BI-licentie die toegang biedt tot de meest voorkomende functies in [!INCLUDE[prod_short](includes/prod_short.md)] en Power BI. U kunt ook een Power BI Pro-licentie aanschaffen die toegang biedt tot extra functies. De volgende tabel geeft een overzicht van de functies die beschikbaar zijn bij elke licentie.

|Power-licentie|Rapporten weergeven|Rapporten maken|Rapporten delen|Rapporten vernieuwen| [!INCLUDE[prod_short](includes/prod_short.md)]-apps|
|-------------|--------||
|Power BI gratis|![een vinkje](media/check.png)|![nog een vinkje](media/check.png)|(beperkt)|(beperkt)||
|Power BI Pro|![en nog een vinkje](media/check.png)|![het is een vinkje](media/check.png)|![weer een vinkje](media/check.png)|(uitgebreid)|![laatste vinkje](media/check.png)|

Zie [Licenties voor de Power BI-service voor gebruikers in uw organisatie](/power-bi/admin/service-admin-licensing-organization) of [U aanmelden voor de Power BI-service als individu](/power-bi/fundamentals/service-self-service-signup-for-power-bi) voor meer informatie.

## <a name="set-up-prod_short-on-premises-for-power-bi-integration"></a><a name="setup"></a>[!INCLUDE[prod_short](includes/prod_short.md)] on-premises configureren voor integratie met Power BI

In dit gedeelte wordt uitgelegd wat de vereisten zijn voor de integratie van een implementatie van [!INCLUDE[prod_short](includes/prod_short.md)] on-premises met Power BI.

1. OData-webservices en het ODataV4-eindpunt zijn ingeschakeld.

    De OData-webservice moet zijn ingeschakeld op de [!INCLUDE[server](includes/server.md)] en de OData-poort moet zijn geopend in firewall. Zie [Business Central Server configureren - OData-webservices](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices) voor meer informatie.
    
    De lokale server moet toegankelijk zijn vanaf internet.

2. [!INCLUDE[prod_short](includes/prod_short.md)]-gebruikersaccounts hebben een toegangssleutel voor de webservice.

    Er is een toegangssleutel voor de webservice nodig om [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens weer te geven in Power BI. U kunt aan elk gebruikersaccount een webservicetoegangssleutel toewijzen. U kunt in plaats daarvan ook een specifiek account maken met webservicetoegangssleutel die door alle gebruikers kan worden gebruikt. Zie [Verificatie voor webservices](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key) voor meer informatie.

3. NavUserPassword of Azure Active Directory-verificatie is geconfigureerd.

4. Voor het weergeven van Power BI-rapporten die zijn ingesloten in [!INCLUDE[prod_short](includes/prod_short.md)]-pagina's, moet een toepassing zijn geregistreerd voor [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure.

    De geregistreerde toepassing heeft toestemming nodig voor Power BI-services. Zie [[!INCLUDE[prod_short](includes/prod_short.md)] on-premises registreren in Azure AD voor integratie met andere services](/dynamics365/business-central/dev-itpro/administration/register-app-azure) voor meer informatie.

    > [!NOTE]
    > Als voor uw implementatie NavUserPassword-verificatie wordt gebruikt, maakt [!INCLUDE[prod_short](includes/prod_short.md)] verbinding met dezelfde Power BI-service voor alle gebruikers. U kunt dit serviceaccount specificeren bij het registreren van de toepassing. Als er Azure AD-verificatie wordt gebruikt, maakt [!INCLUDE[prod_short](includes/prod_short.md)] verbinding met de Power BI-service die is gekoppeld aan de individuele gebruikersaccounts.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->

## <a name="publish-data-as-web-services"></a>Gegevens als webservices publiceren

Codeunits, pagina's en query's die u wilt gebruiken als gegevensbron in Power BI-rapporten, moeten als webservices worden gepubliceerd. Er worden standaard veel webservices gepubliceerd. Een eenvoudige manier om de webservices te vinden, is te zoeken naar *webservices* in [!INCLUDE[prod_short](includes/prod_short.md)]. Zorg dat op de pagina **Webservices** het veld **Publiceren** is geselecteerd voor de hierboven genoemde webservices. Deze taak is gewoonlijk een beheertaak.

Zie [Een webservice publiceren](across-how-publish-web-service.md) voor meer informatie over het publiceren van webservices.

> [!TIP]
> Als u wilt weten wat u kunt doen om ervoor te zorgen dat de webservices optimaal presteren, gezien vanuit de Business Central-server (het eindpunt) en vanuit de consument (de client), leest u [Efficiënte webservices creëren](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).




## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/Configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Business Central en Power BI](admin-powerbi.md)  
[Power BI-integratieonderdeel en architectuuroverzicht voor [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Power BI voor consumenten](/power-bi/consumer/end-user-consumer)  
[De 'nieuwe look' van de Power BI-service](/power-bi/service-new-look)  
[Snelle start: verbinding maken met uw gegevens in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI-documentatie](/power-bi/)  
[Bedrijfsinformatie](bi.md)  
[Aan de slag](product-get-started.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Instellen van [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken als Power BI-gegevensbron](across-how-use-financials-data-source-powerbi.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken als Power Apps-gegevensbron](across-how-use-financials-data-source-powerapps.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken in Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]