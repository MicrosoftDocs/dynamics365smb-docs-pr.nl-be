---
title: Werkstromen instellen | Microsoft Docs
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
ms.openlocfilehash: 59805de35ca1ebe01255eafeb4fff12efacde934
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-workflows"></a>Werkstromen instellen
U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd. Systeemtaken, zoals automatische boekingen, kunnen als stappen in werkstromen worden opgenomen, die worden voorafgegaan of gevolgd door gebruikerstaken. Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen. Zie voor meer informatie [Werkstromen gebruiken](across-use-workflows.md).  

 Voordat u kunt beginnen met werkstromen gebruiken, moet u de werkstroomgebruikers en goedkeuringgebruikers instellen, opgeven hoe gebruikers berichten ontvangen over werkstroomstappen, mogelijk de code aanpassen en vervolgens de werkstromen maken.  

 In het venster **Werkstroom** kunt u een werkstroom maken door de betrokken stappen te vermelden op de regels. Elke stap bestaat uit een werkstroomgebeurtenis, aangepast door gebeurtenistoestanden, en een werkstroomantwoord, aangepast door antwoordopties. U definieert werkstroomregels door velden op werkstroomregels te vullen vanuit lijsten met vaste gebeurtenis- en reactiewaarden die scenario's vertegenwoordigen die worden ondersteund door de toepassingscode.  

 Als een bedrijfsscenario een werkstroomgebeurtenis of -reactie vereist die niet wordt ondersteund, moet een Microsoft-partner ze implementeren door de toepassingscode aan te passen. Zie voor meer informatie [Procedure: Nieuwe werkstroomgebeurtenissen en -responsen implementeren](https://msdn.microsoft.com/en-us/library/mt574349.aspx) op MSDN.

 In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.  

|**Als u dit wilt doen**|**Onderwerp**|  
|------------|-------------|  
|Werkstroomgebruikers en gebruikersgroepen instellen|[Procedure: Werkstroomgebruikers instellen](across-how-to-set-up-workflow-users.md)|  
|Werkstroomgebruikers die deelnemen aan werkstromen voor goedkeuring, instellen.|[Procedure: Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md)|  
|Aangeven hoe werkstroomgebruikers op hoogte worden gebracht van werkstroomstappen, inclusief goedkeuringsaanvragen.|[Werkstroomberichten instellen](across-setting-up-workflow-notifications.md)|  
|Geef op wanneer gebruikers berichten ontvangen en of berichten in een periode moeten worden geaggregeerd om het aantal berichten zo klein mogelijk te maken.|[Procedure: Vastleggen wanneer en hoe gebruikers berichten ontvangen](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|De lay-out en algemene inhoud van nieuwe e-mails voor werkstroomberichten instellen, of bestaande sjablonen exporteren, wijzigen en weer importeren.|[Procedure: Berichtsjablonen beheren](across-how-to-manage-notification-templates.md)|  
|Stel een SMTP-server in om communicatie per e-mail in en vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)] in te schakelen.|[Procedure: E-mail instellen](madeira-how-setup-email.md)|
|De verschillende stappen van een werkstroom opgeven door werkstroomgebeurtenissen te koppelen aan werkstroomantwoorden.|[Procedure: Werkstromen maken](across-how-to-create-workflows.md)|  
|Gebruik werkstroomsjablonen om nieuwe werkstromen te maken.|[Procedure: Werkstromen maken van werkstroomsjablonen](across-how-to-create-workflows-from-workflow-templates.md)|  
|Werkstromen delen met andere [!INCLUDE[d365fin](includes/d365fin_md.md)]-databases.|[Procedure: Werkstromen exporteren en importeren](across-how-to-export-and-import-workflows.md)|  
|Lees meer informatie over het instellen van een werkstroom voor de goedkeuring van verkoopdocumenten door een end-to-end procedure te volgen.|[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  
|Voeg ondersteuning toe voor een bedrijfsscenario dat nieuwe werkstroomgebeurtenissen of -antwoorden vereist, door de toepassingscode aan te passen.|[Procedure: Nieuwe werkstroomgebeurtenissen en -reacties implementeren](https://msdn.microsoft.com/en-us/library/mt574349.aspx) op MSDN.|  

## <a name="see-also"></a>Zie ook  
 [Werkstromen gebruiken](across-use-workflows.md)   
 [Werkstroom](across-workflow.md)   
 [Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
 [Werken met Financials](ui-work-product.md)

