---
title: Power BI-integratieonderdeel en architectuuroverzicht voor Business Central | Microsoft Docs
description: Lees meer over de verschillende aspecten van Power BI-integratie met Business Central.
author: jswymer
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.reviewer: bholtorf
ms.date: 04/01/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="power-bi-integration-component-and-architecture-overview-for-"></a>Power BI-integratieonderdeel en architectuuroverzicht voor [!INCLUDE[prod_short](includes/prod_short.md)]

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

:::image type="content" source="./media/power-bi-architecture.png" alt-text="Alt-tekst van afbeelding." lightbox="./media/power-bi-architecture.png":::

Vanaf februari 2022 zijn Power BI-rapporten voor [!INCLUDE[prod_short](includes/prod_short.md)] online afkomstig van een secundaire, alleen-lezen databasereplica. De database-replica maakt deel uit van de ["read scale-out"](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview)-mogelijkheid in [!INCLUDE[prod_short](includes/prod_short.md)] online. Deze configuratie maakt de hoofddatabase vrij voor transacties, wat de prestaties van het systeem verbetert. Verbinding maken met de alleen-lezen databasereplica is een integraal onderdeel van de Business Central online-connector en vereist geen extra configuratie van uw kant. Alle nieuwe rapporten maken standaard verbinding met de alleen-lezen databasereplica. Oude rapporten zullen nog steeds de hoofddatabase gebruiken. Zie voor meer informatie [Business Central 2021 releasewave 2-abonnement](/dynamics365-release-plan/2021wave2/smb/dynamics365-business-central/use-secondary-read-only-database-power-bi-reporting).

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
