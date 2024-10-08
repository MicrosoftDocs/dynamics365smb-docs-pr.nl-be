---
title: Inleiding in Business Central en Power BI
description: Met Power BI kunt u eenvoudig inzichten en KPI's verwerven op basis van uw Business Central-gegevens.
author: jswymer
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.reviewer: jswymer
ms.date: 04/24/2024
ms.author: jswymer
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="introduction-to-business-central-and-power-bi"></a>Inleiding in Business Central en Power BI

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Het is gemakkelijk inzicht te krijgen in uw [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens met [Power BI](https://powerbi.microsoft.com), een datavisualisatiesysteem van Microsoft. Power BI haalt [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens op, zodat u dashboards en rapporten kunt maken op basis van die gegevens. Power BI biedt een flexibel alternatief voor de ingebouwde rapporten van [!INCLUDE[prod_short](includes/prod_short.md)] en stelt u in staat verder in te zoomen op gegevens om ze te analyseren en om de visualisatie aan te passen. U kunt hiermee zelfs gegevens van verschillende bedrijven samenvoegen in [!INCLUDE[prod_short](includes/prod_short.md)]. Sommige Power BI-rapporten kunnen ook worden ingesloten in Business Central en worden bekeken zonder dat de gebruiker het systeem hoeft te verlaten. Als u werkt met complexere dashboards, kunt u beter de Power BI-website gebruiken.

![Power BI en Business Central.](media/power-bi-intro.png)

## <a name="what-you-can-do-with-power-bi-and-business-central"></a>Wat u kunt doen met Power BI en Business Central

Er zijn verschillende functies voor het werken met [!INCLUDE[prod_short](includes/prod_short.md)] en Power BI. Sommige dingen kunt u doen vanuit Power BI, terwijl u andere dingen kunt doen vanuit [!INCLUDE[prod_short](includes/prod_short.md)]. Sommige functies zijn ook alleen beschikbaar in [!INCLUDE[prod_short](includes/prod_short.md)] online en niet in on-premises. De volgende tabel biedt u een overzicht.

|Functie|Beschrijving|Online|On-premises|Meer informatie|
|-------|-----------|--------------|-----------|----------------|
|[!INCLUDE[prod_short](includes/prod_short.md)]-gegevens weergeven in Power BI|U kunt uw gegevens vanuit [!INCLUDE[prod_short](includes/prod_short.md)] weergeven in rapporten in Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online bevat een aantal vooraf gedefinieerde Power BI-rapporten. Mogelijk heeft uw organisatie enkele aangepaste rapporten beschikbaar gesteld.|![Werkt online.](media/check.png)|![Werkt on-premises](media/check.png)|[Hier...](across-working-with-powerbi.md)|
|Power BI-rapporten weergeven in de [!INCLUDE[prod_short](includes/prod_short.md)]-client.| Power BI-rapporten waarin [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens worden weergegeven, kunnen rechtstreeks worden ingesloten in gedeelten in [!INCLUDE[prod_short](includes/prod_short.md)]-pagina's. U kunt in een dergelijk gedeelte van een pagina elk gewenst rapport weergeven dat beschikbaar is gemaakt voor u. |![werkt online.](media/check.png)|![Werkt on-premises](media/check.png)<sup>[*](#onprem)</sup>|[Hier...](across-working-with-powerbi.md).|
|Maak rapporten en dashboards in Power BI waarin [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens worden weergegeven.|Gebruik Power BI Desktop om uw eigen rapporten en dashboards te maken. U kunt de rapporten publiceren naar uw eigen Power BI-service of deze delen met anderen binnen uw organisatie.|![Werkt online.](media/check.png)|![werkt on-premises](media/check.png)|[Hier...](across-how-use-financials-data-source-powerbi.md)|
|[!INCLUDE[prod_short](includes/prod_short.md)]-apps in Power BI| [!INCLUDE[prod_short](includes/prod_short.md)] publiceert drie apps voor Power BI in Microsoft AppSource. Met deze apps kunnen gedetailleerde rapporten en dashboards worden gemaakt in uw Power BI-service voor het weergeven van [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens. De volgende apps zijn beschikbaar: <ul><li>[!INCLUDE [prod_long](includes/prod_long.md)] - CRM </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Finance </li><li>[!INCLUDE [prod_long](includes/prod_long.md)] - Sales </li></ul>  |![Werkt online.](media/check.png)||[Hier...](across-powerbi-business-central-apps.md)|
|Werken met [!INCLUDE [prod_short](includes/prod_short.md)]-gegevens in datamarts en gegevensstromen|Vanaf juli 2022 kunt u gebruik maken van de [!INCLUDE [prod_short](includes/prod_short.md)]-connector in Power Query Online naar gegevensstromen die u deelt over verschillende rapporten en dashboards.|![werkt online.](media/check.png)||[Hier...](across-powerbi-business-central-apps.md)|

<a name="onprem"><sup>*</sup></a> Deze functie vereist een geregistreerde toepassing voor Business Central in Microsoft Azure. Zie [Business Central On-Premises registeren in Microsoft Entra ID voor integratie met andere services](/dynamics365/business-central/dev-itpro/administration/register-app-azure) voor meer informatie.

## <a name="get-ready-to-use-power-bi"></a>Voorbereiden voor het gebruik van Power BI

Er zijn een paar taken die moeten worden uitgevoerd voordat u Power BI kunt gaan gebruiken in combinatie met [!INCLUDE[prod_short](includes/prod_short.md)].<!-- Some of the tasks are typically only done by administrators or super users.--> De taken zijn afhankelijk van uw rol in uw organisatie en wat u wilt doen met Power BI:

- Als een *zakelijke gebruiker* wilt u Power BI-rapporten bekijken, hetzij in de Power BI-service of in Business Central
- Als een *beheerder* bent u verantwoordelijk voor het beheer van de organisatiebrede instellingen die bepalen hoe Business Central en Power BI werken.
- Als een *rapportmaker* wilt u aangepaste Power BI-rapporten maken die u kunt delen met andere gebruikers.

|Taak|Bedrijfsgebruiker|Beheerder|Rapporten maken|Meer informatie|
|----|-------------|-------------|-----------------------|----------------|
|Maak een Power BI-account aan.|![nog een vinkje.](media/check.png)|![het is een vinkje](media/check.png)|![weer een vinkje](media/check.png)|Ga naar [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Gebruik voor de aanmelding bij een account uw zakelijke e-mailadres en wachtwoord. <br /><br/>U hebt een licentie nodig om u te kunnen aanmelden, maar in de meeste gevallen beschikt u al over een gratis licentie. Zie voor meer informatie [Power BI-licenties](admin-powerbi-setup.md#license).|
|Power BI Desktop ophalen|||![weer een vinkje.](media/check.png)|Ga om te downloaden naar [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Zie [Power BI Desktop downloaden](/power-bi/fundamentals/desktop-get-the-desktop) voor meer informatie.
|Business Central-gegevens beschikbaar stellen aan Power BI||![het is een vinkje.](media/check.png)|![weer een vinkje](media/check.png)|[Gegevens beschikbaar stellen via API-pagina's of OData-webservices](admin-powerbi-setup.md#exposedata)
|Power BI-integratie inschakelen<br />(alleen voor on-premises)||![het is een vinkje.](media/check.png)||[Business Central on-premises instellen voor Power BI-integratie](across-working-with-business-central-in-powerbi.md#setup)|


## <a name="next-steps"></a>Volgende stappen

- Als u een beheerder bent die Power BI moet instellen in [!INCLUDE[prod_short](includes/prod_short.md)], gaat u naar [Power BI-integratie inschakelen](admin-powerbi-setup.md).
- Als Power BI al is ingesteld en u de functies wilt uitproberen, gaat u naar [Werken met Power BI-rapporten in Business Central](across-working-with-powerbi.md).

## <a name="see-also"></a>Zie ook

[Overzicht van analyses](reports-bi-reporting.md)   
[KPI's bijhouden met Power BI statistieken](track-kpis-with-power-bi-metrics.md)   
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken als Power BI-gegevensbron](across-how-use-financials-data-source-powerbi.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken als Power Apps-gegevensbron](across-how-use-financials-data-source-powerapps.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken in Power Automate](across-how-use-financials-data-source-flow.md)  
[Power BI-documentatie](/power-bi/)  
[Wat is Power BI?](/power-bi/fundamentals/power-bi-overview)  
[Snelle start: Uw gegevens verbinden in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Inleiding in datamarts](/power-bi/transform-model/datamarts/datamarts-overview)  
[Inleiding in gegevensstromen en selfservice-gegevensvoorbereiding](/power-bi/transform-model/dataflows/dataflows-introduction-self-service)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
