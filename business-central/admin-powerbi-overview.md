---
title: Power BI-integratieonderdeel en architectuuroverzicht voor Business Central | Microsoft Docs
description: Lees meer over de verschillende aspecten van Power BI-integratie met Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 9ce0b5232a0629bb6248eaaaade69b7c7ebceb02
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/19/2022
ms.locfileid: "8012353"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prod_short"></a>Power BI-integratieonderdeel en architectuuroverzicht voor [!INCLUDE[prod_short](includes/prod_short.md)]

In dit artikel komt u meer te weten over de verschillende aspecten van de Power BI-integratie met [!INCLUDE[prod_short](includes/prod_short.md)], wat u kan helpen bij de implementatie en het gebruik ervan.

## <a name="components"></a>Onderdelen

In de volgende tabel worden de belangrijkste onderdelen beschreven die betrokken zijn bij de Power BI-integratie.

|Onderdeel|Omschrijving|
|---------|-----------|
|Power BI|Een cloudservice voor het hosten en beheren van rapporten.|
|Power BI Desktop|Een bewerkingsprogramma waarmee u rapporten en dashboards kunt maken en waarmee u ook rapporten kunt uitvoeren. Het programma is beschikbaar als gratis download in de Microsoft Store en wordt lokaal geïnstalleerd.|
|[!INCLUDE[prod_short](includes/prod_short.md)]|Online- of on-premises oplossing met connectors die beschikbaar zijn voor Power BI en de mogelijkheid om een Power BI-gedeelte in te sluiten.|

## <a name="whats-available-from-the-start"></a>Wat er vanaf het begin beschikbaar is

In de volgende tabel worden de beschikbare functies beschreven.

|Functie|Ondersteuning voor [!INCLUDE[prod_short](includes/prod_short.md)] online of on-premises|
|-------|---------------------|
|Power BI-connectors|Beide. Verschillende connectors voor online en on-premises. Dezelfde connector wordt gebruikt voor Power BI Desktop en de Power BI-service |
|Ingesloten gedeelte voor het weergeven van een bepaald rapport in een feitenblok in [!INCLUDE[prod_short](includes/prod_short.md)]|Beide. Vereist configuratie om rapporten weer te geven voor on-premises.|
|Power BI-rapportbeheer vanuit [!INCLUDE[prod_short](includes/prod_short.md)]|Online|
|Standaard Power BI-rapporten in rolcentra die zijn geïmplementeerd in Power BI|Online|
|Power BI-apps in Microsoft AppSource|Online|

## <a name="architecture"></a>Architectuur

[!INCLUDE[prod_short](includes/prod_short.md)] kan worden geïntegreerd met Power BI via een connector die OData gebruikt. De gegevensbron voor Power BI-rapporten wordt beschikbaar gemaakt in de vorm van API-pagina's en OData-webservices.

![Power BI-architectuur voor integratie met Business Central.](./media/power-bi-architecture.png)

## <a name="general-flow"></a>Algemene stroom

In het volgende diagram wordt de basiswerkstroom voor gebruikers getoond wanneer ze [!INCLUDE[prod_short](includes/prod_short.md)] verbinden met Power BI.

![Power BI-werkstroom voor integratie met Business Central.](./media/power-bi-flow.png)

1. Gebruiker meldt zich aan voor een Power BI-account.
2. Gebruiker maakt verbinding met Power BI vanuit [!INCLUDE[prod_short](includes/prod_short.md)].
3. [!INCLUDE[prod_short](includes/prod_short.md)] verifieert de licentie.
4. [!INCLUDE[prod_short](includes/prod_short.md)] implementeert standaardrapporten in de Power BI-service. Deze stap vindt alleen plaats voor [!INCLUDE[prod_short](includes/prod_short.md)] online.
5. [!INCLUDE[prod_short](includes/prod_short.md)] maakt rapporten in Power BI beschikbaar voor selectie in [!INCLUDE[prod_short](includes/prod_short.md)]. Standaardrapporten worden automatisch weergegeven in Power BI-gedeeltes.
6. Gebruiker maakt een rapport aan in Power BI Desktop.
7. Gebruiker publiceert het rapport naar de Power BI-service. De rapporten zijn vervolgens beschikbaar voor selectie in [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Business Central en Power BI](admin-powerbi.md)  
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