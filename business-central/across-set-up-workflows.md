---
title: Werkstromen instellen | Microsoft Docs
description: U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd. Systeemtaken, zoals automatische boekingen, kunnen als stappen in werkstromen worden opgenomen, die worden voorafgegaan of gevolgd door gebruikerstaken. Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 041e4fe663712ae7856e46386a6a13e1f7a6e440
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3785808"
---
# <a name="setting-up-workflows"></a>Werkstromen instellen
U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd. Systeemtaken, zoals automatische boekingen, kunnen als stappen in werkstromen worden opgenomen, die worden voorafgegaan of gevolgd door gebruikerstaken. Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen. Zie voor meer informatie [Werkstromen gebruiken](across-use-workflows.md).  

 Voordat u kunt beginnen met werkstromen gebruiken, moet u de werkstroomgebruikers en goedkeuringgebruikers instellen, opgeven hoe gebruikers berichten ontvangen over werkstroomstappen, mogelijk de code aanpassen en vervolgens de werkstromen maken.  

 Op de pagina **Werkstroom** kunt u een werkstroom maken door de betrokken stappen te vermelden op de regels. Elke stap bestaat uit een werkstroomgebeurtenis, aangepast door gebeurtenistoestanden, en een werkstroomantwoord, aangepast door antwoordopties. U definieert werkstroomregels door velden op werkstroomregels te vullen vanuit lijsten met vaste gebeurtenis- en reactiewaarden die scenario's vertegenwoordigen die worden ondersteund door de toepassingscode.  

 Als een bedrijfsscenario een werkstroomgebeurtenis of -reactie vereist die niet wordt ondersteund, moet een Microsoft-partner ze implementeren door de toepassingscode aan te passen. Raadpleeg [Procedure: Nieuwe werkstroomgebeurtenissen en -reacties implementeren](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) in de Help voor ontwikkelaars en IT-professionals voor meer informatie.

 In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.  

|**Als u dit wilt doen**|**Onderwerp**|  
|------------|-------------|  
|Werkstroomgebruikers en gebruikersgroepen instellen|[Werkstroomgebruikers instellen](across-how-to-set-up-workflow-users.md)|  
|Werkstroomgebruikers die deelnemen aan werkstromen voor goedkeuring, instellen.|[Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md)|  
|Aangeven hoe werkstroomgebruikers op hoogte worden gebracht van werkstroomstappen, inclusief goedkeuringsaanvragen.|[Werkstroomberichten instellen](across-setting-up-workflow-notifications.md)|  
|Geef op of gebruikers via e-mail of een notitie worden geïnformeerd en hoe vaak berichten worden verzonden.|[Opgeven wanneer en hoe gebruikers berichten ontvangen](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Pas de inhoud van het e-mailbericht aan door rapport 1320, Berichte-mail te wijzigen.|[Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md)|  
|Stel een SMTP-server in om communicatie per e-mail in en vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)] in te schakelen.|[E-mail instellen](admin-how-setup-email.md)|
|De verschillende stappen van een werkstroom opgeven door werkstroomgebeurtenissen te koppelen aan werkstroomantwoorden.|[Werkstromen maken](across-how-to-create-workflows.md)|  
|Gebruik werkstroomsjablonen om nieuwe werkstromen te maken.|[Werkstromen maken van werkstroomsjablonen](across-how-to-create-workflows-from-workflow-templates.md)|  
|Werkstromen delen met andere [!INCLUDE[d365fin](includes/d365fin_md.md)]-databases.|[Werkstromen exporteren en importeren](across-how-to-export-and-import-workflows.md)|  
|Lees meer informatie over het instellen van een werkstroom voor de goedkeuring van verkoopdocumenten door een end-to-end procedure te volgen.|[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  
|Voeg ondersteuning toe voor een bedrijfsscenario dat nieuwe werkstroomgebeurtenissen of -antwoorden vereist, door de toepassingscode aan te passen.|[Procedure: Nieuwe werkstroomgebeurtenissen en -reacties implementeren](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses)|  

## <a name="example-of-an-approval-workflow"></a>Voorbeeld van een goedkeuringswerkstroom
Deze video laat zien hoe u een werkstroom instelt waarvoor iemand de goedkeuring van iemand anders moet vragen voordat deze informatie over een bestaande klant kan wijzigen of een nieuwe klant kan maken.  
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHI?rel=0]

## <a name="see-also"></a>Zie ook  
 [Werkstromen gebruiken](across-use-workflows.md)   
 [Werkstroom](across-workflow.md)   
 [Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
 [Werken met Business Central](ui-work-product.md)
