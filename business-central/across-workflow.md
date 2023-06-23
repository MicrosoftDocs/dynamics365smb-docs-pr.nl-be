---
title: Werkstromen in Dynamics 365 Business Central
description: Gebruik de ingebouwde werkstroommogelijkheden om goedkeuringswerkstromen in te stellen als aanvulling op geautomatiseerde werkstromen op basis van Power Automate. U kunt stappen instellen om taken aan verschillende mensen toe te wijzen als onderdeel van de verschillende bedrijfsprocessen.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 10/10/2022
ms.custom: bap-template
---
# <a name="workflows-in-dynamics-365-business-central" />Werkstromen in Dynamics 365 Business Central

U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd. Systeemtaken, zoals automatisch boeken, kunnen als stappen in werkstromen worden opgenomen. Systeemtaken kunnen worden voorafgegaan of gevolgd door gebruikerstaken. Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen.

De standaardversie van [!INCLUDE [prod_short](includes/prod_short.md)] ondersteunt drie soorten werkstromen:
  
* Power Automate-stromen

  * Geautomatiseerde stromen worden geactiveerd door gebeurtenissen (zoals het maken, wijzigen of verwijderen van records of documenten) in [!INCLUDE[prod_short](includes/prod_short.md)]. Ook inbegrepen zijn goedkeuringsstromen die zijn gemaakt in Power Automate, die triggeren wanneer een goedkeuring wordt aangevraagd in [!INCLUDE[prod_short](includes/prod_short.md)].
  * Directe stromen die handmatig worden geactiveerd door de actie **Automatiseren** vanuit lijsten, kaarten en documentpagina's.

    Creëer en activeer handmatig een Power Automate-stroom op een [!INCLUDE[prod_short](includes/prod_short.md)]-record, zoals een klant, artikel of verkooporder, met opties om informatie zowel intern als extern te manipuleren (met behulp van geïntegreerde tools).

* Goedkeuringswerkstromen op basis van ingebouwde werkstroomsjablonen

  Op de pagina **Werkstroomsjablonen** kunt u alle beschikbare werkstromen zien. De proefversie van [!INCLUDE[prod_short](includes/prod_short.md)] bevat veel vooraf geconfigureerde werkstromen die worden vertegenwoordigd door werkstroomsjablonen die u kunt kopiëren om nieuwe werkstromen te maken. Wanneer u een sjabloon opent vanuit de pagina **Werkstroomsjablonen** en de naam van de werkstroom begint met *MS-*, is de werkstroomsjabloon door Microsoft toegevoegd.

## <a name="power-automate-flows" />Power Automate-stromen

Met [!INCLUDE [prod_short](includes/prod_short.md)] Online kunt u zich aanmelden voor Power Automate om krachtige geautomatiseerde werkstromen te bouwen. U voert die werkstromen uit vanuit [!INCLUDE [prod_short](includes/prod_short.md)]. De stromen kunnen interne en externe gegevensbronnen en tools met elkaar verbinden, zonder codeerkennis.

|**Als u dit wilt doen** |**Zie**|
|-------|-------|
|Ga aan de slag met Power Automate en het maken en uitvoeren van directe stromen|[Power Automate-stromen gebruiken in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md)|
|Meer informatie over het maken, bewerken en beheren van stromen|[Geautomatiseerde stromen instellen](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) en [Directe stromen instellen](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)|
|Power Automate-integratie met [!INCLUDE[prod_short](includes/prod_short.md)] instellen voor gebruikers als beheerder|[Power Automate-integratie instellen](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup)|

## <a name="approval-workflows" />Goedkeuringswerkstromen

Maak een goedkeuringswerkstroom door als volgt te definiëren waardoor de werkstroom wordt gestart en wat er daarna gebeurt:

* Een werkstroomgebeurtenis, die wordt beheerd door gebeurtenisvoorwaarden.
* Een werkstroomreactie, die wordt gemodereerd door antwoordopties.

Als u werkstroomstappen wilt definiëren, vult u velden op werkstroomregels in met behulp van gebeurtenis- en reactiewaarden die ondersteunde scenario's vertegenwoordigen.

Voorbeelden van gebeurtenissen voor goedkeuringswerkstromen zijn het maken van verkoop- of inkooporders/-offertes/-facturen, prijswijzigingen, wijzigingen van leveranciers of klanten en meer.

[!INCLUDE[workflow](includes/workflow.md)]

| **Als u dit wilt doen** | **Zie** |
|--|--|
| Stel gebruikers van goedkeuringswerkstromen in, geef op hoe gebruikers berichten krijgen en maak nieuwe werkstromen. (Als u nieuwe werkstromen wilt maken voor niet-ondersteunde scenario's, implementeert u de vereiste werkstroomelementen door de toepassingscode aan te passen.) | [Goedkeuringswerkstromen instellen](across-set-up-workflows.md) |
| Goedkeuringswerkstromen inschakelen, reageren op werkstroomberichten, inclusief een werkstroomstap aanvragen en goedkeuren. Werkstromen archiveren en verwijderen. | [Goedkeuringswerkstromen gebruiken](across-use-workflows.md) |

<!--
| Integrate company data with Power Automate workflows, using both internal and external sources and events to create and automate tasks or workflows. | [Use Power Automate Flows in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md) |-->

## <a name="see-related-microsoft-trainingtrainingmodulescreate-workflows" />Zie gerelateerde [Microsoft-training](/training/modules/create-workflows/)

## <a name="see-also" />Zie ook

[Verkoop](sales-manage-sales.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Projecten beheren](projects-manage-projects.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Problemen met uw [!INCLUDE[prod_short](includes/prod_short.md)] geautomatiseerde werkstromen](across-flow-troubleshoot.md) oplossen  


[!INCLUDE[footer-include](includes/footer-banner.md)]
