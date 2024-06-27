---
title: Inleiding in Microsoft Fabric en Business Central
description: 'Met Microsoft Fabric kunt u eenvoudig inzicht verwerven, bedrijfsinformatie genereren en KPI''s vaststellen op basis van uw Business Central-gegevens.'
author: kennienp
ms.topic: overview
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.search.form: '6316, 6317'
ms.reviewer: bholtorf
ms.date: 04/24/2024
ms.author: kepontop
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="introduction-to-microsoft-fabric-and-business-central"></a>Inleiding in Microsoft Fabric en Business Central

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] is een end-to-end analyseoplossing met complete mogelijkheden, waaronder gegevensverplaatsing, data lakes, gegevensengineering, gegevensintegratie, data science, realtime analyse en bedrijfsinformatie&mdash;allemaal ondersteund door een gedeeld platform dat robuuste gegevensbeveiliging, governance en compliance biedt. Uw organisatie hoeft niet langer individuele analysediensten van meerdere leveranciers te combineren. Gebruik in plaats daarvan een gestroomlijnde oplossing die eenvoudig kan worden verbonden, geïntroduceerd en bediend.

> [!NOTE]
> Zie voor meer informatie over het Microsoft Fabric-releaseplan [aka.ms/FabricRoadmap](https://aka.ms/FabricRoadmap)
> 
> Doordat regelmatig deze routekaart wordt gepubliceerd, blijft u op de hoogte van hoe [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] aan uw behoeften voldoet.

## <a name="where-does--fit-into-includeprod_short-analytics"></a>Waar past [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] in [!INCLUDE[prod_short](includes/prod_short.md)]-analyses

[!INCLUDE[prod_short](includes/prod_short.md)] wordt geleverd met veel kant-en-klare rapporten en mogelijkheden voor gegevensanalyse, zoals financiële rapportage, openen in Excel en analysemodi voor lijsten en query's. Bovendien is het eenvoudig Power BI-rapporten te definiëren die gegevens uit standaard- en aangepaste API's lezen, scorecards met Power BI-meetgegevens te definiëren en dit allemaal rechtstreeks in de [!INCLUDE[prod_short](includes/prod_short.md)]-cliënt in te sluiten. Maar voor klanten met geavanceerdere data science- of bedrijfsinformatiescenario's die rijkere gegevensengineering of gegevensintegratie vereisen, zou [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] een goede optie kunnen zijn. 

## <a name="onelake"></a>OneLake

Een belangrijk onderdeel van het [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)]-aanbod is OneLake. OneLake is één enkel, verenigd, logisch data lake voor de hele organisatie. U kunt OneLake zien als de OneDrive voor gegevens. Het biedt u data lake als een service zonder dat u het zelf hoeft te bouwen. OneLake wordt automatisch meegeleverd met elke [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)]-tenant zonder infrastructuur om te beheren. Alle gegevens die in OneLake terechtkomen, nemen automatisch deel aan out-of-the-box datagovernance, zoals gegevensafstamming, gegevensbescherming, certificering en catalogusintegratie. Het breekt datasilo's af door verschillende delen van de organisatie in staat te stellen onafhankelijk te werken en toch bij te dragen aan hetzelfde data lake.

[!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)]-items slaan uw gegevens op in OneLake in een open bestandsindeling. Voor gestructureerde tabelgegevens is deze indeling: *delta parquet*. De indeling delta parquet maakt het voor elke analyse-engine in [!INCLUDE[microsoft_fabric](includes/microsoft_fabric.md)] mogelijk om toegang te krijgen tot de gegevens van andere analyse-engines. Op deze manier biedt het flexibiliteit voor dataprofessionals om de tools van uw keuze te gebruiken.


## <a name="see-also"></a>Zie ook
[Power BI gebruiken met Business Central](admin-powerbi.md)   

[!INCLUDE[footer-include](includes/footer-banner.md)]
