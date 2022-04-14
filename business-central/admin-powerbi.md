---
title: Inleiding in Business Central en Power BI
description: Met Power BI kunt u eenvoudig inzicht verwerven, bedrijfsinformatie genereren en KPI's vaststellen op basis van uw Business Central-gegevens.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.search.form: 6316, 6317
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: c1935c51fbcabfc0371530532f18b2aaf6005dbb
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511817"
---
# <a name="prod_short-and-power-bi"></a>[!INCLUDE[prod_short](includes/prod_short.md)] en Power BI

Inzicht krijgen in uw [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens is eenvoudig met [Power BI](https://powerbi.microsoft.com), een datavisualisatiesysteem van Microsoft. Power BI haalt [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens op, zodat u dashboards en rapporten kunt maken op basis van die gegevens. Power BI biedt een flexibel alternatief voor de ingebouwde rapporten van [!INCLUDE[prod_short](includes/prod_short.md)] en stelt u in staat verder in te zoomen op gegevens om ze te analyseren en om de visualisatie aan te passen. U kunt hiermee zelfs gegevens van verschillende bedrijven samenvoegen in [!INCLUDE[prod_short](includes/prod_short.md)]. Sommige Power BI-rapporten kunnen ook worden ingesloten in Business Central en worden bekeken zonder dat de gebruiker het systeem hoeft te verlaten. Als u werkt met complexere dashboards, kunt u beter de Power BI-website gebruiken.

![Power BI en Business Central.](media/power-bi-intro.png)

## <a name="what-you-can-do-with-power-bi-and-prod_short"></a>Wat u kunt doen met Power BI en [!INCLUDE[prod_short](includes/prod_short.md)]

Er zijn verschillende functies voor het werken met [!INCLUDE[prod_short](includes/prod_short.md)] en Power BI. Sommige dingen kunt u doen vanuit Power BI, terwijl u andere dingen kunt doen vanuit [!INCLUDE[prod_short](includes/prod_short.md)]. Sommige functies zijn ook alleen beschikbaar in [!INCLUDE[prod_short](includes/prod_short.md)] online en niet in on-premises. De volgende tabel biedt u een overzicht.

|Functie|Omschrijving|Online|On-premises|Meer informatie|
|-------|-----------|--------------|-----------|----------------|
|[!INCLUDE[prod_short](includes/prod_short.md)]-gegevens weergeven in Power BI|U kunt uw gegevens vanuit [!INCLUDE[prod_short](includes/prod_short.md)] weergeven in rapporten in Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online bevat een aantal vooraf gedefinieerde Power BI-rapporten. Mogelijk heeft uw organisatie enkele aangepaste rapporten aan u beschikbaar gesteld.|![Werkt online.](media/check.png)|![Werkt on-premises](media/check.png)|[Zie...](across-working-with-business-central-in-powerbi.md)|
|Power BI-rapporten weergeven in de [!INCLUDE[prod_short](includes/prod_short.md)]-client.| Power BI-rapporten waarin [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens worden weergegeven, kunnen rechtstreeks worden ingesloten in gedeelten in [!INCLUDE[prod_short](includes/prod_short.md)]-pagina's. U kunt in een dergelijk gedeelte van een pagina elk gewenst rapport weergeven dat beschikbaar is gemaakt voor u. |![werkt online.](media/check.png)|![Werkt on-premises](media/check.png)<sup>[*](#onprem)</sup>|[Zie...](across-working-with-powerbi.md).|
|Maak rapporten en dashboards in Power BI waarin [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens worden weergegeven.|Gebruik Power BI Desktop om uw eigen rapporten en dashboards te maken. U kunt de rapporten publiceren naar uw eigen Power BI-service of deze delen met anderen binnen uw organisatie.|![Werkt online.](media/check.png)|![werkt on-premises](media/check.png)|[Zie...](across-how-use-financials-data-source-powerbi.md)
|[!INCLUDE[prod_short](includes/prod_short.md)]-apps in Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] publiceert drie apps voor Power BI in Microsoft AppSource. Met deze apps kunnen gedetailleerde rapporten en dashboards worden gemaakt in uw Power BI-service voor het weergeven van [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens. De volgende apps zijn beschikbaar: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] - CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Sales </li></ul>  |![Werkt online.](media/check.png)||[Zie...](across-powerbi-business-central-apps.md)

<a name="onprem"><sup>*</sup></a> Deze functie vereist een geregistreerde toepassing voor Business Central in Microsoft Azure. Zie [Business Central On-Premises registeren in Azure AD voor integratie met andere services](/dynamics365/business-central/dev-itpro/administration/register-app-azure) voor meer informatie.

## <a name="getting-ready-to-use-power-bi"></a>Voorbereidingen voor het gebruik van Power BI

Er zijn een paar taken die moeten worden uitgevoerd voordat u Power BI kunt gaan gebruiken in combinatie met [!INCLUDE[prod_short](includes/prod_short.md)]. <!-- Some of the tasks are typically only done by administrators or super users.--> De taken zijn afhankelijk van uw rol in uw organisatie en wat u wilt doen met Power BI:

- Als een *zakelijke gebruiker* wilt u Power BI-rapporten bekijken, hetzij in de Power BI-service of in Business Central
- Als een *beheerder* bent u verantwoordelijk voor het beheer van de organisatiebrede instellingen die bepalen hoe Business Central en Power BI werken.
- Als een *rapportmaker* wilt u aangepaste Power BI-rapporten maken die u kunt delen met andere gebruikers.

|Taak|Bedrijfsgebruiker|Beheerder|Rapportmaker|Meer informatie|
|----|-------------|-------------|-----------------------|----------------|
|Maak een Power BI-account aan.|![nog een vinkje.](media/check.png)|![het is een vinkje](media/check.png)|![weer een vinkje](media/check.png)|Ga naar [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Gebruik voor de aanmelding bij een account uw zakelijke e-mailadres en wachtwoord. <br /><br/>U hebt een licentie nodig om u te kunnen aanmelden, maar in de meeste gevallen beschikt u al over een gratis licentie. Zie voor meer informatie [Power BI-licenties](admin-powerbi-setup.md#license).|
|Power BI Desktop ophalen|||![weer een vinkje.](media/check.png)|Ga om te downloaden naar [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Zie [Power BI Desktop downloaden](/power-bi/fundamentals/desktop-get-the-desktop) voor meer informatie.
|Business Central-gegevens beschikbaar stellen aan Power BI||![het is een vinkje.](media/check.png)|![weer een vinkje](media/check.png)|[Gegevens beschikbaar stellen via API-pagina's of OData-webservices](admin-powerbi-setup.md#exposedata)
|Power BI-integratie inschakelen<br />(alleen voor on-premises)||![het is een vinkje.](media/check.png)||[Business Central on-premises instellen voor Power BI-integratie](admin-powerbi-setup.md#setup)|


<!--



1. If you're using [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, make sure your deployment meets the requirements outlined in [Set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for Power BI integration](admin-powerbi-setup.md#setup). This task is typically an administrative task.

2. Expose Business Central data through API pages or published web services.

    Business Central online automatically included several pages as APIs. For more information, see [Business Central API V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/). Application developers for Business Central online can create custom API pages that you can then consume in reports. For more information, see [Developing a Custom API](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

   Codeunit, page, and query objects can be published as OData web services. There are many web services published by default. An easy way to find the web services is to search for *web services* in [!INCLUDE[prod_short](includes/prod_short.md)]. For more information about publishing web services, see [Publish a Web Service](across-how-publish-web-service.md).

3. Get a Power BI account.

   To do anything with Power BI and [!INCLUDE[prod_short](includes/prod_short.md)], whether you're an administrator or just a consumer, you'll need Power BI service account. To get an account, go to [https://powerbi.microsoft.com](https://powerbi.microsoft.com). To sign up for an account, use your work email address and password. Sign-up requires that you have a license, but in most cases you should already have a free license. For more information, see [Power BI Licensing](admin-powerbi-setup.md#license).

4. If you want to create your own Power BI reports, get Power BI Desktop.

   You can download [Power BI Desktop](https://powerbi.microsoft.com/desktop/). For more information, see [Get Power BI Desktop](/power-bi/fundamentals/desktop-get-the-desktop).

-->

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

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