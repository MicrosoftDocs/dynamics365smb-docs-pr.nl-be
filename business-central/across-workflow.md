---
title: Werkstroom | Microsoft Docs
description: U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd. Systeemtaken, zoals automatische boekingen, kunnen als stappen in werkstromen worden opgenomen, die worden voorafgegaan of gevolgd door gebruikerstaken. Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 128d20233d1750b2b89c3c7e2de6e497bd32b342
ms.contentlocale: nl-be
ms.lasthandoff: 05/15/2018

---
# <a name="workflow"></a>Werkstroom
U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd. Systeemtaken, zoals automatische boekingen, kunnen als stappen in werkstromen worden opgenomen, die worden voorafgegaan of gevolgd door gebruikerstaken. Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen.  

 In het venster **Werkstroom** kunt u een werkstroom maken door de betrokken stappen te vermelden op de regels. Elke stap bestaat uit een werkstroomgebeurtenis, aangepast door gebeurtenistoestanden, en een werkstroomantwoord, aangepast door antwoordopties. U definieert werkstroomregels door velden op werkstroomregels te vullen vanuit lijsten met vaste gebeurtenis- en reactiewaarden die scenario's vertegenwoordigen die worden ondersteund door de toepassingscode.  

 De algemene versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] bevat een aantal vooraf geconfigureerde werkstromen die worden vertegenwoordigd door werkstroomsjablonen die u kunt kopiëren om werkstromen te maken. De code voor werkstroomsjablonen die door Microsoft worden toegevoegd, heeft het voorvoegsel "MS-". Zie voor meer informatie de lijst met werkstroomsjablonen in het venster Werkstroomsjablonen venster.  

 Als een bedrijfsscenario een werkstroomgebeurtenis of -reactie vereist die niet wordt ondersteund, moet een Microsoft-partner ze implementeren door de toepassingscode aan te passen. Raadpleeg [Procedure: Nieuwe werkstroomgebeurtenissen en -reacties implementeren](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) in de Help voor ontwikkelaars en IT-professionals voor meer informatie.

> [!NOTE]  
> Werkstromen kunnen ook worden gestart vanuit Microsoft Flow. Zie voor meer informatie [Business Central gebruiken in een geautomatiseerde werkstroom](across-how-use-financials-data-source-flow.md).  

 In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.  

|**Als u dit wilt doen**|**Onderwerp**|  
|------------|-------------|  
|Gebruikers van werkstromen instellen, opgeven hoe gebruikers berichten krijgen en nieuwe werkstromen maken. Voor nieuwe werkstromen voor niet-ondersteunde scenario's implementeert u de vereiste workflowelementen door de toepassingcode aan te passen.|[Werkstromen instellen](across-set-up-workflows.md)|  
|Werkstromen inschakelen, reageren op werkstroomberichten, inclusief goedkeuringen aanvragen en aanvragen goedkeuren om een werkstroomstap uit te voeren. Werkstromen archiveren en verwijderen.|[Werkstromen gebruiken](across-use-workflows.md)|  

## <a name="see-also"></a>Zie ook  
[Verkoop](sales-manage-sales.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Projecten beheren](projects-manage-projects.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

