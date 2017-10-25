---
title: Werkstroom | Microsoft Docs
description: U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd. Systeemtaken, zoals automatische boekingen, kunnen als stappen in werkstromen worden opgenomen, die worden voorafgegaan of gevolgd door gebruikerstaken. Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f65c0e577e839928809f7afda3dbdb4c9b7702c8
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="workflow"></a>Werkstroom
U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd. Systeemtaken, zoals automatische boekingen, kunnen als stappen in werkstromen worden opgenomen, die worden voorafgegaan of gevolgd door gebruikerstaken. Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen.  

 In het venster **Werkstroom** kunt u een werkstroom maken door de betrokken stappen te vermelden op de regels. Elke stap bestaat uit een werkstroomgebeurtenis, aangepast door gebeurtenistoestanden, en een werkstroomantwoord, aangepast door antwoordopties. U definieert werkstroomregels door velden op werkstroomregels te vullen vanuit lijsten met vaste gebeurtenis- en reactiewaarden die scenario's vertegenwoordigen die worden ondersteund door de toepassingscode.  

 De algemene versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] bevat een aantal vooraf geconfigureerde werkstromen die worden vertegenwoordigd door werkstroomsjablonen die u kunt kopiëren om werkstromen te maken. De code voor werkstroomsjablonen die door Microsoft worden toegevoegd, heeft het voorvoegsel "MS-". Zie voor meer informatie de lijst met werkstroomsjablonen in het venster Werkstroomsjablonen venster.  

 Als een bedrijfsscenario een werkstroomgebeurtenis of -reactie vereist die niet wordt ondersteund, moet een Microsoft-partner ze implementeren door de toepassingscode aan te passen. Zie voor meer informatie [Procedure: Nieuwe werkstroomgebeurtenissen en -responsen implementeren](https://msdn.microsoft.com/en-us/library/mt574349.aspx) op MSDN.  

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

