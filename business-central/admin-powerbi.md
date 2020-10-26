---
title: Business Central en Power BI - een inleiding| Microsoft Docs
description: U kunt eenvoudig inzichten verwerven, bedrijfsinformatie genereren en KPI's vaststellen op basis van uw Business Central-gegevens met de Business Central-apps voor Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: e339033e8529f59f548e8bf71fd683f9a2a17eba
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3917888"
---
# <a name="prodshort-and-power-bi"></a>[!INCLUDE[prodshort](includes/prodshort.md)] en Power BI

Inzicht krijgen in uw [!INCLUDE[prodshort](includes/prodshort.md)]-gegevens is eenvoudig met [Power BI](https://powerbi.microsoft.com), een datavisualisatiesysteem van Microsoft. Power BI haalt [!INCLUDE[prodshort](includes/prodshort.md)]-gegevens op, zodat u dashboards en rapporten kunt maken op basis van die gegevens. Power BI biedt een flexibel alternatief voor de ingebouwde rapporten van [!INCLUDE[prodshort](includes/prodshort.md)] en stelt u in staat verder in te zoomen op gegevens om ze te analyseren en om de visualisatie aan te passen. U kunt hiermee zelfs gegevens van verschillende bedrijven samenvoegen in [!INCLUDE[prodshort](includes/prodshort.md)]. Sommige Power BI-rapporten kunnen ook worden ingesloten in Business Central en worden bekeken zonder dat de gebruiker het systeem hoeft te verlaten. Als u werkt met complexere dashboards, kunt u beter de Power BI-website gebruiken.

![Power BI en Business Central](media/power-bi-intro.png)


## <a name="what-you-can-do-with-power-bi-and-prodshort"></a>Wat u kunt doen met Power BI en [!INCLUDE[prodshort](includes/prodshort.md)]

Er zijn verschillende functies voor het werken met [!INCLUDE[prodshort](includes/prodshort.md)] en Power BI. Sommige dingen kunt u doen vanuit Power BI, terwijl u andere dingen kunt doen vanuit [!INCLUDE[prodshort](includes/prodshort.md)]. Sommige functies zijn ook alleen beschikbaar in [!INCLUDE[prodshort](includes/prodshort.md)] online en niet in on-premises. De volgende tabel biedt u een overzicht.

|Functie|Omschrijving|Online|On-premises|Meer informatie|
|-------|-----------|--------------|-----------|----------------|
|[!INCLUDE[prodshort](includes/prodshort.md)]-gegevens weergeven in Power BI|U kunt uw gegevens vanuit [!INCLUDE[prodshort](includes/prodshort.md)] weergeven in rapporten in Power BI. [!INCLUDE[prodshort](includes/prodshort.md)] online bevat een aantal vooraf gedefinieerde Power BI-rapporten. Mogelijk heeft uw organisatie enkele aangepaste rapporten aan u beschikbaar gesteld.|![Werkt online](media/check.png)|![Werkt on-premises](media/check.png)|[Zie...](across-working-with-powerbi.md)|
|Power BI-rapporten weergeven in de [!INCLUDE[prodshort](includes/prodshort.md)]-client.| Power BI-rapporten waarin [!INCLUDE[prodshort](includes/prodshort.md)]-gegevens worden weergegeven, kunnen rechtstreeks worden ingesloten in gedeelten in [!INCLUDE[prodshort](includes/prodshort.md)]-pagina's. U kunt in een dergelijk gedeelte van een pagina elk gewenst rapport weergeven dat beschikbaar is gemaakt voor u. |![werkt online](media/check.png)|![Werkt on-premises](media/check.png)<sup>[*](#onprem)</sup>|[Zie...](across-working-with-business-central-in-powerbi.md).|
|Maak rapporten en dashboards in Power BI waarin [!INCLUDE[prodshort](includes/prodshort.md)]-gegevens worden weergegeven.|Gebruik Power BI Desktop om uw eigen rapporten en dashboards te maken. U kunt de rapporten publiceren naar uw eigen Power BI-service of deze delen met anderen binnen uw organisatie.|![Werkt online](media/check.png)|![werkt on-premises](media/check.png)|[Zie...](across-how-use-financials-data-source-powerbi.md)
|[!INCLUDE[prodshort](includes/prodshort.md)]-apps in Power BI| [!INCLUDE[prodshort](includes/prodshort.md)] publiceert drie apps voor Power BI in Microsoft AppSource. Met deze apps kunnen gedetailleerde rapporten en dashboards worden gemaakt in uw Power BI-service voor het weergeven van [!INCLUDE[prodshort](includes/prodshort.md)]-gegevens. De volgende apps zijn beschikbaar: <ul><li>[!INCLUDE [prodlong](includes/prodlong.md)] - CRM </li><li>[!INCLUDE [prodlong](includes/prodlong.md)] - Finance </li><li>[!INCLUDE [prodlong](includes/prodlong.md)] - Sales </li></ul>  |![Werkt online](media/check.png)||[Zie...](across-powerbi-business-central-apps.md)

<a name="onprem"><sup>*</sup></a> Deze functie vereist een geregistreerde toepassing voor Business Central in Microsoft Azure. Zie [Business Central On-Premises registeren in Azure AD voor integratie met andere services](/dynamics365/business-central/dev-itpro/administration/register-app-azure) voor meer informatie.

## <a name="getting-ready-to-use-power-bi"></a>Voorbereidingen voor het gebruik van Power BI

Er zijn een paar taken die moeten worden uitgevoerd voordat u Power BI kunt gaan gebruiken in combinatie met [!INCLUDE[prodshort](includes/prodshort.md)]. Enkele van deze taken worden doorgaans alleen uitgevoerd door beheerders of supergebruikers.

1. Als u [!INCLUDE[prodshort](includes/prodshort.md)] on-premises gebruikt, moet u ervoor zorgen dat uw implementatie voldoet aan de vereisten die zijn beschreven in [[!INCLUDE[prodshort](includes/prodshort.md)] on-premises instellen voor Power BI-integratie](admin-powerbi-setup.md#setup). Deze taak is gewoonlijk een beheertaak.

2. Publiceer gegevens als webservices.

    Codeunits, pagina's en query's die u wilt gebruiken als gegevensbron in Power BI-rapporten, moeten als webservices worden gepubliceerd. Er worden standaard veel webservices gepubliceerd. Een eenvoudige manier om de webservices te vinden, is te zoeken naar *webservices* in [!INCLUDE[prodshort](includes/prodshort.md)].
    
    Zie [Een webservice publiceren](across-how-publish-web-service.md) voor meer informatie over het publiceren van webservices.

3. Maak een Power BI-account aan.

    Voor alles wat u wilt doen met Power BI en [!INCLUDE[prodshort](includes/prodshort.md)] hebt u een Power BI-serviceaccount nodig, of u nu een beheerder bent of gewoon een consument. Als u een account wilt aanmaken, gaat u naar [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Gebruik voor de aanmelding bij een account uw zakelijke e-mailadres en wachtwoord. U hebt een licentie nodig om u te kunnen aanmelden, maar in de meeste gevallen beschikt u al over een gratis licentie. Zie [Power BI-licenties](admin-powerbi-setup.md#license) voor meer informatie.

4. Als u uw eigen Power BI-rapporten wilt maken, hebt u Power BI Desktop nodig.

    U kunt [Power BI Desktop](https://powerbi.microsoft.com/desktop/) downloaden. Zie [Power BI Desktop downloaden](/power-bi/fundamentals/desktop-get-the-desktop) voor meer informatie.

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

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
