---
title: Werkstromen in Dynamics 365 Business Central
description: Gebruik de ingebouwde werkstroommogelijkheden om goedkeuringswerkstromen in te stellen als aanvulling op geautomatiseerde werkstromen op basis van Power Automate. U kunt stappen instellen om taken aan verschillende mensen toe te wijzen als onderdeel van de verschillende bedrijfsprocessen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: ecaaf9bbb56e1c1b47f9f617319b32f32a2920fd
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585634"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Werkstromen in Dynamics 365 Business Central

U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd. Systeemtaken, zoals automatische boekingen, kunnen als stappen in werkstromen worden opgenomen, die worden voorafgegaan of gevolgd door gebruikerstaken. Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen.

De standaardversie van [!INCLUDE [prod_short](includes/prod_short.md)] ondersteunt drie soorten werkstromen:

* Goedkeuringswerkstromen op basis van ingebouwde werkstroomsjablonen

  Op de pagina **Werkstroomsjablonen** kunt u alle beschikbare werkstromen zien. De proefversie van [!INCLUDE[prod_short](includes/prod_short.md)] bevat veel vooraf geconfigureerde werkstromen die worden vertegenwoordigd door werkstroomsjablonen die u kunt kopiëren om nieuwe werkstromen te maken. Wanneer u een sjabloon opent vanuit de pagina **Werkstroomsjablonen** en de naam van de werkstroom begint met *MS-*, is de werkstroomsjabloon door Microsoft toegevoegd.
  
* Power Automate-stromen die u zelf instelt

  Elke werkstroomsjabloon die u maakt met Microsoft Power Automate, wordt toegevoegd aan de lijst met werkstroomsjablonen binnen [!INCLUDE[prod_short](includes/prod_short.md)]. Zie voor meer informatie [[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken in Power Automate-stromen](across-how-use-financials-data-source-flow.md). 
  
* Directe stromen die handmatig zijn getriggerd door de actie **Automatiseren** (alleen [!INCLUDE [prod_short](includes/prod_short.md)] online).

  Creëer en activeer handmatig een Power Automate-stroom op een [!INCLUDE[prod_short](includes/prod_short.md)]-record, zoals een klant, artikel of verkooporder, met opties om informatie zowel intern als extern te manipuleren (met behulp van geïntegreerde tools). Lees meer in de sectie [Directe stromen](across-how-use-financials-data-source-flow.md#instant-flows).

## <a name="power-automate-flows"></a>Power Automate-stromen

Gebruik makend van [!INCLUDE [prod_short](includes/prod_short.md)] online u kunt zich aanmelden voor Power Automate om krachtige geautomatiseerde werkstromen te bouwen. U kunt deze werkstromen van binnen [!INCLUDE [prod_short](includes/prod_short.md)] uitvoeren en interne en externe gegevensbronnen en tools verbinden zonder codeerkennis.

Power Automate-stromen kunnen worden geactiveerd door gebeurtenissen (zoals het maken, wijzigen of verwijderen van records of documenten) en worden uitgevoerd volgens een door de gebruiker gedefinieerd schema of op aanvraag (een **directe stroom** genoemd).

## <a name="approval-workflows"></a>Goedkeuringswerkstromen

U maakt een goedkeuringswerkstroom door de betrokken stappen te vermelden op de regels. Elke stap bestaat uit een werkstroomgebeurtenis, aangepast door gebeurtenistoestanden, en een werkstroomantwoord, aangepast door antwoordopties. U definieert werkstroomregels door velden op werkstroomregels te vullen met behulp van lijsten met vaste gebeurtenis- en reactiewaarden die scenario's vertegenwoordigen die worden ondersteund door de toepassingscode.<!--What are the "values"? Can we give an example?-->

Voorbeelden van gebeurtenissen voor goedkeuringswerkstromen zijn onder meer het maken van verkoop- of inkooporders/-offertes/-facturen, prijswijzigingen en wijzigingen van leveranciers of klanten.

[!INCLUDE[workflow](includes/workflow.md)]

| **Als u dit wilt doen** | **Zie** |
|--|--|
| Stel gebruikers van goedkeuringswerkstromen in, geef op hoe gebruikers berichten krijgen en maak nieuwe werkstromen. (Als u nieuwe werkstromen wilt maken voor niet-ondersteunde scenario's, implementeert u de vereiste werkstroomelementen door de toepassingscode aan te passen.) | [Goedkeuringswerkstromen instellen](across-set-up-workflows.md) |
| Goedkeuringswerkstromen inschakelen, reageren op werkstroomberichten, inclusief een werkstroomstap aanvragen en goedkeuren. Werkstromen archiveren en verwijderen. | [Goedkeuringswerkstromen gebruiken](across-use-workflows.md) |
| Integreer bedrijfsgegevens met Power Automate-werkstromen, waarbij zowel interne als externe bronnen en gebeurtenissen worden gebruikt om taken of werkstromen te creëren en te automatiseren. | [Power Automate-stromen gebruiken in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md) |

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/create-workflows/)

## <a name="see-also"></a>Zie ook

[Verkoop](sales-manage-sales.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Projecten beheren](projects-manage-projects.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Problemen met uw [!INCLUDE[prod_short](includes/prod_short.md)] geautomatiseerde werkstromen](across-flow-troubleshoot.md) oplossen  


[!INCLUDE[footer-include](includes/footer-banner.md)]
