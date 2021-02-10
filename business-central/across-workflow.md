---
title: Werkstroom | Microsoft Docs
description: U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd. Systeemtaken, zoals automatische boekingen, kunnen als stappen in werkstromen worden opgenomen, die worden voorafgegaan of gevolgd door gebruikerstaken. Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 95290ba7170e2390e83d4b12e5d988760c2f3c5f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752937"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Werkstromen in Dynamics 365 Business Central

U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd. Systeemtaken, zoals automatische boekingen, kunnen als stappen in werkstromen worden opgenomen, die worden voorafgegaan of gevolgd door gebruikerstaken. Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen.  

 Op de pagina **Werkstroom** kunt u een werkstroom maken door de betrokken stappen te vermelden op de regels. Elke stap bestaat uit een werkstroomgebeurtenis, aangepast door gebeurtenistoestanden, en een werkstroomantwoord, aangepast door antwoordopties. U definieert werkstroomregels door velden op werkstroomregels te vullen vanuit lijsten met vaste gebeurtenis- en reactiewaarden die scenario's vertegenwoordigen die worden ondersteund door de toepassingscode.  

 De algemene versie van [!INCLUDE[prod_short](includes/prod_short.md)] bevat een aantal vooraf geconfigureerde werkstromen die worden vertegenwoordigd door werkstroomsjablonen die u kunt kopiëren om werkstromen te maken. De code voor werkstroomsjablonen die door Microsoft worden toegevoegd, heeft het voorvoegsel "MS-". Zie voor meer informatie de lijst met werkstroomsjablonen op de pagina Werkstroomsjablonen.  

 Als een bedrijfsscenario een werkstroomgebeurtenis of -reactie vereist die niet wordt ondersteund, kunt u Power Automate gebruiken of met een Microsoft-partner samenwerken om de toepassingscode aan te passen. Zie voor meer informatie [[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken in een geautomatiseerde werkstroom](across-how-use-financials-data-source-flow.md).

Elke werkstroomsjabloon die u maakt met Power Automate wordt toegevoegd aan de lijst met werkstroomsjablonen binnen [!INCLUDE[prod_short](includes/prod_short.md)]. Zie voor meer informatie [Business Central gebruiken in een geautomatiseerde werkstroom](across-how-use-financials-data-source-flow.md).  

 In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.  

|**Als u dit wilt doen**|**Onderwerp**|  
|------------|-------------|  
|Gebruikers van werkstromen instellen, opgeven hoe gebruikers berichten krijgen en nieuwe werkstromen maken. Voor nieuwe werkstromen voor niet-ondersteunde scenario's implementeert u de vereiste workflowelementen door de toepassingcode aan te passen.|[Werkstromen instellen](across-set-up-workflows.md)|  
|Werkstromen inschakelen, reageren op werkstroomberichten, inclusief goedkeuringen aanvragen en aanvragen goedkeuren om een werkstroomstap uit te voeren. Werkstromen archiveren en verwijderen.|[Werkstromen gebruiken](across-use-workflows.md)|  

## <a name="see-also"></a>Zie ook

[Verkoop](sales-manage-sales.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Projecten beheren](projects-manage-projects.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
