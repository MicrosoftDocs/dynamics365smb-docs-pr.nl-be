---
title: Goedkeuringswerkstromen instellen (bevat video)
description: 'Stel werkstromen, werkstroomgebruikers en goedkeuringsgebruikers in om de systeemtaken van de bedrijfsprocessen die door deze verschillende gebruikers worden uitgevoerd, met elkaar te verbinden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/13/2022
ms.author: bholtorf
---
# <a name="set-up-approval-workflows"></a>Goedkeuringswerkstromen instellen

U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd. Systeemtaken, zoals automatische boekingen, kunnen als stappen in werkstromen worden opgenomen, die worden voorafgegaan of gevolgd door gebruikerstaken. Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen. Zie voor meer informatie [Goedkeuringswerkstromen gebruiken](across-use-workflows.md).

Voordat u kunt beginnen met goedkeuringswerkstromen gebruiken, moet u de werkstroomgebruikers en goedkeuringgebruikers instellen, opgeven hoe gebruikers berichten ontvangen over werkstroomstappen en vervolgens de werkstromen maken.

Op de pagina **Werkstroom** kunt u een werkstroom maken door de betrokken stappen te vermelden op de regels. Elke stap bestaat uit een werkstroomgebeurtenis, aangepast door gebeurtenistoestanden, en een werkstroomreactie, aangepast door antwoordopties. U definieert werkstroomregels door velden op werkstroomregels te vullen met behulp van lijsten met vaste gebeurtenis- en reactiewaarden die scenario's vertegenwoordigen die worden ondersteund door de toepassingscode.

[!INCLUDE[workflow](includes/workflow.md)]

De volgende tabel beschrijft een reeks taken, met koppelingen naar de artikelen waarin deze worden beschreven.

|**Als u dit wilt doen**|**Zie**|  
|------------|-------------|  
|Werkstroomgebruikers en gebruikersgroepen instellen|[Werkstroomgebruikers instellen](across-how-to-set-up-workflow-users.md)|  
|Werkstroomgebruikers die deelnemen aan werkstromen voor goedkeuring, instellen.|[Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md)|  
|Aangeven hoe werkstroomgebruikers op hoogte worden gebracht van werkstroomstappen, inclusief goedkeuringsaanvragen.|[Werkstroomberichten instellen](across-setting-up-workflow-notifications.md)|  
|Geef op of gebruikers via e-mail of een notitie worden geïnformeerd en hoe vaak berichten worden verzonden.|[Opgeven wanneer en hoe gebruikers berichten ontvangen](across-how-to-specify-when-and-how-to-receive-notifications.md)|  
|Pas de inhoud van het e-mailbericht aan door rapport 1320, Berichte-mail te wijzigen.|[Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md)|  
|Stel een SMTP-server in om communicatie per e-mail in en vanuit [!INCLUDE[prod_short](includes/prod_short.md)] in te schakelen.|[E-mail instellen](admin-how-setup-email.md)|
|Geef de verschillende stappen van een werkstroom op door werkstroomgebeurtenissen te verbinden met werkstroomantwoorden.|[Goedkeuringswerkstromen maken](across-how-to-create-workflows.md)|  
|Gebruik werkstroomsjablonen om nieuwe werkstromen te maken.|[Goedkeuringswerkstromen maken van werkstroomsjablonen](across-how-to-create-workflows-from-workflow-templates.md)|  
|Werkstromen delen met andere [!INCLUDE[prod_short](includes/prod_short.md)]-databases.|[Goedkeuringswerkstromen exporteren en importeren](across-how-to-export-and-import-workflows.md)|  
|Lees meer informatie over het instellen van een werkstroom voor de goedkeuring van verkoopdocumenten door een end-to-end procedure te volgen.|[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)|  

## <a name="example-of-an-approval-workflow"></a>Voorbeeld van een goedkeuringswerkstroom

Deze video laat zien hoe u een werkstroom instelt waarvoor een gebruiker de goedkeuring van iemand anders moet vragen voordat deze informatie over een bestaande klant kan wijzigen of een nieuwe klant kan maken.  
<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4jzHI?rel=0]

## <a name="see-also"></a>Zie ook

[Goedkeuringswerkstromen gebruiken](across-use-workflows.md)  
[Werkstroom](across-workflow.md)  
[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Werken met Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
