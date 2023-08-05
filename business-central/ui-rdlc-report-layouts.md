---
title: Werken met RDLC-lay-outs
description: Een inleiding krijgen tot RDLC-rapportlay-outs.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/14/2022
ms.author: jswymer
---
# Werken met RDLC-lay-outs

RDLC-lay-outs zijn gebaseerd op clientrapportdefinitielay-outs (.rdl- of .rdlc-bestandstypen). De grondslagen voor het ontwerp van RDLC-lay-outs zijn vergelijkbaar met die voor andere lay-outtypen. De lay-out bepaalt welke velden worden weergegeven en hoe ze zijn gerangschikt. RDLC-lay-outs ontwerpen is echter veel geavanceerder dan Word- en Excel-lay-outs ontwerpen.

[![Toont de verschillende elementen van een RDLC-lay-out.](media/rdlc-layout.png)](media/rdlc-layout.png#lightbox)

## Vereiste hulpprogramma's

Om RDL-lay-outs te wijzigen, kunt u Microsoft SQL Server Report Builder of Microsoft RDLC Report Designer gebruiken.

- Report Builder is een zelfstandige app die door u of een beheerder op uw computer is geïnstalleerd. Met Business Central on-premises wordt Report Builder automatisch geïnstalleerd met de Business Central Server-installatie. Voor meer informatie over het installeren van Report Builder, zie [Report Builder installeren](/sql/reporting-services/install-windows/install-report-builder) in de SQL Server-documentatie.

- RDLC Report Designer is een extensie voor Visual Studio 2017 en hoger. U kunt RDLC Report Designer downloaden en installeren vanaf de [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=ProBITools.MicrosoftRdlcReportDesignerforVisualStudio-18001).

## RDLC-lay-outs maken en wijzigen

Het maken en wijzigen van RDLC-lay-outs is een geavanceerde taak, die doorgaans wordt uitgevoerd door ervaren gebruikers of ontwikkelaars. De grondslagen zijn niet specifiek voor Business Central-rapportlay-outs. Om deze reden verwijzen wij u naar de volgende documentatie:

- [RDL-lay-outrapport maken](/dynamics365/business-central/dev-itpro/developer/devenv-howto-rdl-report-layout)

    In dit artikel wordt uitgelegd hoe u een RDLC-rapportlay-out maakt op basis van AL-code.

- [Rapporten, rapportonderdelen en rapportdefinities ](/sql/reporting-services/report-design/reports-report-parts-and-report-definitions-report-builder-and-ssrs?)

 Hiermee krijgt u een koppeling naar de SQL Server Reporting Services-documentatie voor RDL/RDLC. Deze documentatie geeft uitleg bij de begrippen  
die ten grondslag liggen aan RDL/RDLC en over hoe u Report Builder gebruikt.

> [!NOTE]
> Report Builder herkent alleen het .rdl-bestandstype;, niet .rdlc. Lay-outbestanden die uit Business Central worden geëxporteerd, zijn .rdlc-bestandstypen. Dus om deze lay-out in Report Builder te wijzigen, hernoemt u het bestandstype naar .rdl.

## Zie gerelateerde [Microsoft-training](/training/modules/change-documents-dynamics-365-business-central/index)

## Zie ook

[Rapportlay-outs beheren](ui-manage-report-layouts.md)  
[De lay-out instellen die door een rapport wordt gebruikt](ui-set-report-layout.md)  
[Aan de slag met het maken van rapportlay-outs](ui-get-started-layouts.md)  
[Werken met rapporten, batchverwerkingen en XMLports](ui-work-report.md)  
[Bedrijfsinformatie](bi.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Rapportgegevens analyseren met Excel](report-analyze-excel.md).

[!INCLUDE[footer-include](includes/footer-banner.md)]
