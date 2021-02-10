---
title: Aangepaste en ingebouwde lay-outs voor rapporten en documenten | Microsoft Docs
description: Gebruik rapportlay-outs om documenten aan te passen, bijvoorbeeld om het lettertype of logo aan te passen of pagina-instellingen of PDF-bestanden die u naar klanten verzendt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8a3cfebf90ba639b8d8563ce437c6f5605acf2eb
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756829"
---
# <a name="managing-report-and-document-layouts"></a>Lay-outs van rapporten en documenten beheren
Een rapportlay-out bepaalt de inhoud en de indeling van het rapport, inclusief welke gegevensvelden van een rapportgegevensset in het rapport worden weergegeven, hoe ze worden gerangschikt, welke tekststijl en afbeeldingen worden gebruikt, enzovoort. Vanuit [!INCLUDE[prod_short](includes/prod_short.md)] kunt u bepalen welke lay-out wordt gebruikt in een rapport, een nieuwe lay-out maken of de huidige lay-outs wijzigen.

> [!NOTE]  
>   In [!INCLUDE[prod_short](includes/prod_short.md)] omvat de term 'rapport' ook documenten die extern worden verspreid, zoals verkoopfacturen en orderbevestigingen die u aan klanten als pdf-bestanden verzendt.

Met een rapportlay-out wordt met name het volgende ingesteld:

* De label- en gegevensvelden die moeten worden opgenomen uit de gegevensset van het [!INCLUDE[prod_short](includes/prod_short.md)]-rapport.
* De tekstindeling, bijvoorbeeld lettertype, -grootte en -kleur.
* Het bedrijfslogo en de positie ervan.
* Algemene pagina-instellingen, zoals marges en achtergrondafbeeldingen.

Een rapport kan worden ingesteld met meerdere rapportlay-outs, waartussen u indien nodig kunt schakelen. U kunt een van de ingebouwde rapportlay-outs gebruiken of u kunt aangepaste rapportlay-outs maken en ze indien nodig aan uw rapporten toewijzen. Zie voor meer informatie [Een aangepaste lay-out voor een rapport of document maken](ui-how-create-custom-report-layout.md).

Er zijn twee soorten rapportlay-outs die u in rapporten kunt gebruiken: Word en RDLC.

## <a name="word-report-layout-overview"></a>Overzicht van de Word-rapportlay-out
Een Word-rapportlay-out wordt gebaseerd op een Word-document (.docx-bestandstype). Met Word-rapportlay-outs kunt u rapportlay-outs ontwerpen door Microsoft Word 2013 of later te gebruiken. Een Word-rapportlay-out bepaalt de inhoud van het rapport: hoe de inhoudelementen worden gerangschikt en hoe ze eruit zien. Een Word-document met een rapportlay-out gebruikt meestal tabellen om inhoud te rangschikken. De cellen kunnen gegevensvelden, tekst of afbeeldingen bevatten.

 ![Voorbeeld van een Word-rapportdocument voor NAV](media/nav_wordreportlayout_edit_in_word_example.png "NAV_WordReportLayout_Edit_In_Word_Example")  

## <a name="rdlc-layout-overview"></a>Overzicht van de RDLC-lay-out
RDLC-lay-outs zijn gebaseerd op clientrapportdefinitielay-outs (.rdlc- of .rdl-bestandstypen). Deze lay-outs worden gemaakt en gewijzigd vanuit SQL Server Report Builder. Het ontwerpconcept voor RDLC-lay-outs lijkt op Word-lay-outs, waarbij de lay-out de algemene indeling van het rapport definieert en bepaalt welke velden uit de database worden opgenomen. RDLC-lay-outs ontwerpen is geavanceerder dan Word-lay-outs ontwerpen. Zie voor meer informatie [RDLC-rapportlay-outs ontwerpen](/dynamics-nav/Designing-RDLC-Report-Layouts).

## <a name="built-in-and-custom-report-layouts"></a>Ingebouwde en aangepaste rapportlay-outs
[!INCLUDE[prod_short](includes/prod_short.md)] bevat verschillende geïntegreerde lay-outs. Ingebouwde lay-outs zijn vooraf gedefinieerde lay-outs die voor bepaalde rapporten zijn ontworpen. Rapporten in [!INCLUDE[prod_short](includes/prod_short.md)] hebben een geïntegreerde lay-out zoals een RDLC-rapportlay-out, Word-rapportlay-outs of in bepaalde gevallen beide. U kunt een geïntegreerde rapportlay-out niet vanuit [!INCLUDE[prod_short](includes/prod_short.md)] wijzigen, maar u gebruikt deze als uitgangspunt voor het maken van uw eigen aangepaste rapportlay-outs.

Aangepaste lay-outs zijn rapportlay-outs die u ontwerpt om de weergave van een rapport te wijzigen. U maakt meestal een aangepaste lay-out op basis van een ingebouwde lay-out, maar u kunt ze ook nieuw maken of op basis van een kopie van een bestaande aangepaste lay-out. Met aangepaste lay-outs kunt u meerdere lay-outs voor hetzelfde rapport hebben waartussen u indien nodig kunt schakelen. U kunt bijvoorbeeld verschillende lay-outs voor elk [!INCLUDE[prod_short](includes/prod_short.md)]-bedrijf hebben of u kunt verschillende lay-outs voor hetzelfde bedrijf hebben voor bepaalde situaties of gebeurtenissen, zoals een speciale campagne of feestdagen.

## <a name="deciding-whether-to-use-a-word-or-rdlc-report-layout"></a>Besluiten of u een Word- of een RDLC-rapportlay-out wilt gebruiken
Een rapportlay-out kan worden gebaseerd op een Word-document of op een RDLC-bestand. Het besluit om een Word-rapportlay-out of een RDLC-rapportlay-out te gebruiken is afhankelijk van hoe u wilt dat het gegenereerde rapport eruitziet en van uw kennis van Word en SQL Server Report Builder.

De algemene ontwerpconcepten voor Word- en RDLC-lay-outs lijken erg op elkaar. Elk type heeft echter bepaalde ontwerpfuncties die bepalen hoe het gegenereerde rapport eruitziet in [!INCLUDE[prod_short](includes/prod_short.md)]. Dit houdt in dat hetzelfde rapport er anders uit kan zien wanneer u de Word-rapportlay-out gebruikt dan wanneer u de RDLC-rapportlay-out gebruikt.

Het proces voor het instellen van Word-rapportlay-outs en RDLC-rapportlay-outs in rapporten is hetzelfde. Het belangrijkste verschil is de manier waarop u de lay-outs wijzigt. Word-rapportlay-outs zijn in het algemeen gemakkelijker te maken en te wijzigen dan RDLC-rapportlay-outs, omdat u Word kunt gebruiken. RDLC-rapportlay-outs worden gewijzigd met SQL Server Report Builder, dat voor geavanceerdere gebruikers is bedoeld.

Zie [De huidige rapportindeling wijzigen](ui-how-change-layout-currently-used-report.md) voor informatie over het wijzigen van de te gebruiken indeling.

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook
[Aangepaste rapportlay-outs bijwerken](ui-update-report-layouts.md)  
[Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md)  
[Een aangepaste indeling voor een rapport of document importeren en exporteren](ui-how-import-and-export-report-layout.md)  
[Speciale documentlay-outs definiëren voor klanten en leveranciers](ui-define-customer-vendor-document-layouts.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[Werken met rapporten, batchverwerkingen en XMLports](ui-work-report.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
