---
title: Power BI-integratieonderdeel en architectuuroverzicht voor Business Central | Microsoft Docs
description: U kunt eenvoudig inzichten verwerven, bedrijfsinformatie genereren en KPI's vaststellen op basis van uw Business Central-gegevens met de Business Central-apps voor Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 9514f0355932c1b1cbd30acfdb9f6dab46db8a0a
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697822"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prodshort"></a>Power BI-integratieonderdeel en architectuuroverzicht voor [!INCLUDE[prodshort](includes/prodshort.md)]

In dit artikel komt u meer te weten over de verschillende aspecten van de Power BI-integratie met [!INCLUDE[prodshort](includes/prodshort.md)], wat u kan helpen bij de implementatie en het gebruik ervan.

## <a name="components"></a>Onderdelen

In de volgende tabel worden de belangrijkste onderdelen beschreven die betrokken zijn bij de Power BI-integratie.

|Onderdeel|Omschrijving|
|---------|-----------|
|Power BI|Een cloudservice voor het hosten en beheren van rapporten.|
|Power BI Desktop|Een bewerkingsprogramma waarmee u rapporten en dashboards kunt maken en waarmee u ook rapporten kunt uitvoeren. Het programma is beschikbaar als gratis download in de Microsoft Store en wordt lokaal geïnstalleerd.|
|[!INCLUDE[prodshort](includes/prodshort.md)]|Online- of on-premises oplossing met connectors die beschikbaar zijn voor Power BI en de mogelijkheid om een Power BI-gedeelte in te sluiten.|

## <a name="whats-available-from-the-start"></a>Wat er vanaf het begin beschikbaar is

In de volgende tabel worden de beschikbare functies beschreven.

|Functie|Ondersteuning voor [!INCLUDE[prodshort](includes/prodshort.md)] online of on-premises|
|-------|---------------------|
|Power BI-connectors|Beide. Verschillende connectors voor online en on-premises. Dezelfde connector wordt gebruikt voor Power BI Desktop en de Power BI-service |
|Ingesloten gedeelte voor het weergeven van een bepaald rapport in een feitenblok in [!INCLUDE[prodshort](includes/prodshort.md)]|Beide. Vereist configuratie om rapporten weer te geven voor on-premises.|
|Power BI-rapportbeheer vanuit [!INCLUDE[prodshort](includes/prodshort.md)]|Online|
|Standaard Power BI-rapporten in rolcentra die zijn geïmplementeerd in Power BI|Online|
|Power BI-apps in Microsoft AppSource|Online.|

## <a name="architecture"></a>Architectuur

[!INCLUDE[prodshort](includes/prodshort.md)] kan worden geïntegreerd met Power BI via een connector die OData gebruikt. De gegevensbron voor Power BI-rapporten wordt beschikbaar gemaakt in de vorm van OData-webservices.

![Power BI-architectuur voor integratie met Business Central](./media/power-bi-architecture.png)

## <a name="general-flow"></a>Algemene stroom

In het volgende diagram wordt de basiswerkstroom voor gebruikers getoond wanneer ze [!INCLUDE[prodshort](includes/prodshort.md)] verbinden met Power BI.

![Power BI-werkstroom voor integratie met Business Central](./media/power-bi-flow.png)

1. Gebruiker meldt zich aan voor een Power BI-account.
2. Gebruiker maakt verbinding met Power BI vanuit [!INCLUDE[prodshort](includes/prodshort.md)].
3. [!INCLUDE[prodshort](includes/prodshort.md)] verifieert de licentie.
4. [!INCLUDE[prodshort](includes/prodshort.md)] implementeert standaardrapporten in de Power BI-service. Deze stap vindt alleen plaats voor [!INCLUDE[prodshort](includes/prodshort.md)] online.
5. [!INCLUDE[prodshort](includes/prodshort.md)] maakt rapporten in Power BI beschikbaar voor selectie in [!INCLUDE[prodshort](includes/prodshort.md)]. Standaardrapporten worden automatisch weergegeven in Power BI-gedeeltes.
6. Gebruiker maakt een rapport aan in Power BI Desktop.
7. Gebruiker publiceert het rapport naar de Power BI-service. De rapporten zijn vervolgens beschikbaar voor selectie in [!INCLUDE[prodshort](includes/prodshort.md)].

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Business Central en Power BI](admin-powerbi.md)  
[Power BI voor consumenten](/power-bi/consumer/end-user-consumer)  
[De 'nieuwe look' van de Power BI-service](/power-bi/service-new-look)  
[Snelle start: verbinding maken met uw gegevens in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI-documentatie](/power-bi/)  
[Bedrijfsinformatie](bi.md)  
[Aan de slag](product-get-started.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken als Power BI-gegevensbron](across-how-use-financials-data-source-powerbi.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken als Power Apps-gegevensbron](across-how-use-financials-data-source-powerapps.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken in Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
