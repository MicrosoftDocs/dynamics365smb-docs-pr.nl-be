---
title: Werkstromen in Dynamics 365 Business Central
description: Gebruik de ingebouwde werkstroommogelijkheden om goedkeuringswerkstromen in te stellen als aanvulling op geautomatiseerde werkstromen op basis van Power Automate. U kunt stappen instellen om taken aan verschillende mensen toe te wijzen als onderdeel van de verschillende bedrijfsprocessen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 05/12/2022
ms.author: edupont
ms.openlocfilehash: 7ea61d359bbdaf0ac788a0fada151fe3e0ad5960
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9075094"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Werkstromen in Dynamics 365 Business Central

U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd. Systeemtaken, zoals automatische boekingen, kunnen als stappen in werkstromen worden opgenomen, die worden voorafgegaan of gevolgd door gebruikerstaken. Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen.  

De standaardversie van [!INCLUDE [prod_short](includes/prod_short.md)] ondersteunt drie soorten werkstromen:

* Geautomatiseerde goedkeuringswerkstromen op basis van ingebouwde werkstroomsjablonen  

  Op de pagina **Werkstroomsjablonen** kunt u alle beschikbare werkstromen zien. De proefversie van [!INCLUDE[prod_short](includes/prod_short.md)] bevat een aantal vooraf geconfigureerde werkstromen die worden vertegenwoordigd door werkstroomsjablonen die u kunt kopiëren om werkstromen te maken. Wanneer u een werkstroomsjabloon opent vanuit de pagina **Werkstroomsjablonen** en de naam van de werkstroom begint met *MS-*, wordt de werkstroomsjabloon door Microsoft toegevoegd.  
* Geautomatiseerde stromen die u zelf instelt  

  Elke werkstroomsjabloon die u maakt met Power Automate wordt toegevoegd aan de lijst met werkstroomsjablonen binnen [!INCLUDE[prod_short](includes/prod_short.md)]. Zie voor meer informatie [Business Central gebruiken in Power Automate-stromen](across-how-use-financials-data-source-flow.md).  
* Handmatig getriggerde stromen vanuit de actie **Automatiseren** (alleen [!INCLUDE [prod_short](includes/prod_short.md)] online). Zie voor meer informatie [Handmatige directe stromen](across-how-use-financials-data-source-flow.md#manual-instant-flows).  

## <a name="power-automate-flows"></a>Power Automate-stromen

Voor [!INCLUDE [prod_short](includes/prod_short.md)] online u kunt zich aanmelden voor Power Automate en vervolgens krachtige geautomatiseerde stromen maken die u vanuit [!INCLUDE [prod_short](includes/prod_short.md)] kunt uitvoeren. Zie voor meer informatie [[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken in Power Automate-stromen](across-how-use-financials-data-source-flow.md).  

## <a name="automated-approval-workflows"></a>Geautomatiseerde goedkeuringswerkstromen

U maakt een goedkeuringswerkstroom door de betrokken stappen te vermelden op de regels. Elke stap bestaat uit een werkstroomgebeurtenis, aangepast door gebeurtenistoestanden, en een werkstroomantwoord, aangepast door antwoordopties. U definieert werkstroomregels door velden op werkstroomregels te vullen vanuit lijsten met vaste gebeurtenis- en reactiewaarden die scenario's vertegenwoordigen die worden ondersteund door de toepassingscode.  

Als een bedrijfsscenario een werkstroomgebeurtenis of -reactie vereist die niet wordt ondersteund in de standaardversie, meld u dan aan voor Power Automate. Zie voor meer informatie [[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken in Power Automate-stromen](across-how-use-financials-data-source-flow.md). U kunt ook een app aanschaffen of samenwerken met een Microsoft-partner om de toepassingscode aan te passen.  

Om werkstromen in te stellen en te gebruiken die niet zijn gedefinieerd in Power Automate, bekijkt u de volgende artikelen:  

|**Als u dit wilt doen**|**Zie**|  
|------------|-------------|  
|Gebruikers van werkstromen instellen, opgeven hoe gebruikers berichten krijgen en nieuwe werkstromen maken. Voor nieuwe werkstromen voor niet-ondersteunde scenario's implementeert u de vereiste workflowelementen door de toepassingcode aan te passen.|[Werkstromen instellen](across-set-up-workflows.md)|  
|Werkstromen inschakelen, reageren op werkstroomberichten, inclusief goedkeuringen aanvragen en aanvragen goedkeuren om een werkstroomstap uit te voeren. Werkstromen archiveren en verwijderen.|[Werkstromen gebruiken](across-use-workflows.md)|  

## <a name="see-related-training-at-microsoft-learn"></a>Zie gerelateerde training op [Microsoft Learn](/learn/modules/create-workflows/)

## <a name="see-also"></a>Zie ook

[Verkoop](sales-manage-sales.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Projecten beheren](projects-manage-projects.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken in Power Automate-stromen](across-how-use-financials-data-source-flow.md)  
[Problemen met uw [!INCLUDE[prod_short](includes/prod_short.md)] geautomatiseerde werkstromen](across-flow-troubleshoot.md) oplossen  


[!INCLUDE[footer-include](includes/footer-banner.md)]