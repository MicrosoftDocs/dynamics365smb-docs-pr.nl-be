---
title: Lay-outs van rapporten en documenten beheren
description: 'Gebruik rapportlay-outs om documenten aan te passen, bijvoorbeeld om het lettertype of logo aan te passen of pagina-instellingen of PDF-bestanden die u naar klanten verzendt.'
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9652, 9650, 9660'
ms.date: 01/18/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Overzicht van lay-outs van rapporten en documenten beheren

Een rapportlay-out bepaalt de inhoud en de indeling van het rapport, inclusief welke gegevensvelden van een rapportgegevensset in het rapport worden weergegeven, hoe ze worden gerangschikt, welke tekststijl en afbeeldingen worden gebruikt, enzovoort. Vanuit [!INCLUDE[prod_short](includes/prod_short.md)] kunt u bepalen welke lay-out wordt gebruikt in een rapport, een nieuwe lay-out maken of de huidige lay-outs wijzigen.

> [!NOTE]  
> In [!INCLUDE[prod_short](includes/prod_short.md)] omvat de term 'rapport' ook documenten die extern worden verspreid, zoals verkoopfacturen en orderbevestigingen die u aan klanten als pdf-bestanden verzendt.

U kunt ook rapportlay-outs gebruiken om inhoud aan e-mailberichten toe te voegen. Rapportlay-outs kunnen bijvoorbeeld tijd besparen en zorgen voor consistentie door dezelfde inhoud opnieuw te gebruiken wanneer u met uw klanten communiceert. Als u aangepaste rapportlay-outs met e-mail wilt gebruiken, moet het bestandstype voor de lay-out Word zijn. U kunt het RDLC-bestandstype niet gebruiken. Voor meer informatie zie [Herbruikbare e-mailteksten en lay-outs instellen](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## Inleiding

Met een rapportlay-out worden met name de volgende zaken ingesteld:

* De label- en gegevensvelden die moeten worden opgenomen uit de gegevensset van het [!INCLUDE[prod_short](includes/prod_short.md)]-rapport.
* De tekstindeling, bijvoorbeeld lettertype, -grootte en -kleur.
* Het bedrijfslogo en de positie ervan.
* Algemene pagina-instellingen, zoals marges en achtergrondafbeeldingen.

Een rapport kan worden ingesteld met meerdere rapportlay-outs, waartussen u indien nodig kunt schakelen. 

<!--You can use one of the built-in report layouts or you can create custom report layouts and assign them to your reports as needed. For more information, see [Create a Custom Report or Document Layout](ui-how-create-custom-report-layout.md).-->

Er zijn twee belangrijke aspecten van rapportlay-outs die van invloed zijn op hoe u ermee werkt: het *lay-outtype* en de *lay-out bron*. Het lay-outtype geeft aan op welk type bestand de lay-out is gebaseerd. De lay-outbron geeft de oorsprong van de lay-out aan.

## Lay-outtypen

Er zijn vier typen rapportlay-outs die u in rapporten kunt gebruiken: Word, RDLC, Excel en extern.

### Word

Word-rapportlay-outs worden gebaseerd op Word-documenten (.docx-bestandstype). Met Word-lay-outs kunt u rapportlay-outs ontwerpen met behulp van Microsoft Word. Een Word-lay-out bepaalt de inhoud van het rapport: hoe de inhoudelementen worden gerangschikt en hoe ze eruitzien. Een Word-document met een lay-out gebruikt meestal tabellen om inhoud te rangschikken. De cellen kunnen gegevensvelden, tekst of afbeeldingen bevatten.

[![Voorbeeld van een Word-rapportlay-outdocument voor Business Central.](media/word-layout-overview.png)](media/word-layout-overview.png#lightbox) 

<!--![Example of a word report layout document for Business Central.](media/nav_wordreportlayout_edit_in_word_example.png) -->

Zie voor meer informatie [Werken met Word-lay-outs](ui-how-add-fields-word-report-layout.md).

### Excel

Excel-lay-outs zijn gebaseerd op Microsoft Excel-werkmappen (.xlsx-bestandstype). Hiermee kunt u rapporten maken met behulp van vertrouwde Excel-functies voor het samenvatten, analyseren en presenteren van gegevens met hulpmiddelen zoals onder meer formules, draaitabellen en draaigrafieken.

[![Toont een voorbeeld van een Excel-lay-out.](media/excel-layout-2.png)](media/excel-layout-2.png#lightbox)

Zie voor meer informatie [Werken met Excel-lay-outs](ui-excel-report-layouts.md).

### RDLC

RDLC-lay-outs zijn gebaseerd op clientrapportdefinitielay-outs (.rdl- of .rdlc-bestandstypen). Deze lay-outs worden gemaakt en gewijzigd vanuit SQL Server Report Builder of Microsoft RDLC Report Designer. De grondslag voor het ontwerp van RDLC-lay-outs is vergelijkbaar met Word-lay-outs, waarbij de lay-out bepaalt welke velden moeten worden weergegeven en hoe ze zijn gerangschikt. RDLC-lay-outs ontwerpen is echter veel geavanceerder dan Word-lay-outs ontwerpen.

[![Toont een voorbeeld van een RDLC-lay-out.](media/rdlc-layout-overview.png)](media/rdlc-layout-overview.png#lightbox)

Zie voor meer informatie [Werken met RDLC-lay-outs](ui-rdlc-report-layouts.md).

### Extern

Een extern lay-outtype verwijst naar een geavanceerd type dat speciaal is ontworpen voor specifieke rapporten. De rapporten en de lay-outs zelf worden doorgaans geleverd door partners, niet door Microsoft. Het daadwerkelijke bestandstype van de lay-out is afhankelijk van de provider.

Voor meer informatie, zie [Een aangepaste rapportweergave ontwikkelen](/dynamics365/business-central/dev-itpro/developer/devenv-report-custom-render).

## Lay-outbronnen

Naast het type zijn lay-outs verder onderverdeeld in drie categorieën, op basis van hun bron of herkomst.

* Extensielay-outs

   Extensielay-outs zijn lay-outs die deel uitmaken van een extensie die op de omgeving is geïnstalleerd. Deze lay-outs zijn doorgaans standaardlay-outs die door Microsoft worden geleverd, bijvoorbeeld in de basistoepassing. Of het kunnen lay-outs zijn die zijn opgenomen in extensies van andere softwareleveranciers. U herkent extensielay-outs op de pagina **Rapportlay-outs** omdat de extensienaam en -uitgever worden weergegeven in de kolom **Extensie**.

* Door de gebruiker ingestelde lay-outs

   De andere bron van lay-outs is de eindgebruiker. Vanuit Business Central kan een gebruiker met de juiste machtigingen op verschillende manieren nieuwe lay-outs toevoegen. U kunt bijvoorbeeld uitgaan van een bestaande extensielay-out of een andere door de gebruiker ingestelde lay-out. Op de pagina **Rapportlay-outs** is de kolom **Extensie** van een door de gebruiker ingestelde lay-out leeg.

   Zie voor meer informatie [Aan de slag met het maken van lay-outs](ui-get-started-layouts.md).

* Aangepaste lay-outs

  Aangepaste lay-outs zijn ook lay-outs die door gebruikers zijn gemaakt. Het verschil is dat deze lay-outs zijn gemaakt op basis van de oude **Aangepaste rapportlay-outs**-pagina en ze kunnen alleen van het Word- en RDLC-type zijn. Hoewel u nog steeds aangepaste lay-outs kunt maken, worden deze geleidelijk uitgefaseerd ten gunste van door de gebruiker ingestelde lay-outs (zie hierboven).

  Zie voor meer informatie [Aangepaste rapportlay-outs maken en wijzigen (verouderde versie)](ui-how-create-custom-report-layout.md).

Voor informatie die u zal helpen beslissen welk type het beste voor u is, zie [Bepalen welk type lay-out u wilt](ui-get-started-layouts.md#decide).

> [!IMPORTANT]
> Een belangrijk ding om te onthouden is dat u extensielay-outs niet kunt wijzigen vanuit de Business Central-client. U mag bijvoorbeeld de lay-outnaam of het type niet wijzigen of dit uploaden en vervangen door een andere versie. Als u het probeert, verschijnt er een foutmelding. U moet in plaats daarvan een door de gebruiker ingestelde of aangepaste lay-out maken op basis van de extensielay-out.

<!--
### Built-in and custom report layouts



[!INCLUDE[prod_short](includes/prod_short.md)] includes several built-in layouts. Built-in layouts are predefined layouts that are designed for specific reports. [!INCLUDE[prod_short](includes/prod_short.md)] reports will have a built-in layout as either an RDLC report layout, Word report layout, or in some cases both. You can’t modify a built-in report layout from [!INCLUDE[prod_short](includes/prod_short.md)] but you use them as a starting point for building your own custom report layouts.

Custom layouts are report layouts that you design to change the appearance of a report. You typically create a custom layout based on a built-in layout, but you can create them from scratch or from a copy of an existing custom layout. Custom layouts enable you to have multiple layouts for the same report, which you switch among as needed. For example, you can have different layouts for each [!INCLUDE[prod_short](includes/prod_short.md)] company, or you can have different layouts for the same company for specific occasions or events, like a special campaign or holiday season.


Deciding on whether to use a Word, Excel, or RDLC layout type will depend on how you want the generated report to look and your knowledge of tools for creating the layouts, like Word, Excel, and SQL Server Report Builder.

* The general design concepts for Word and RDLC layouts are similar. However each type has certain design features that affect how the generated report appears in [!INCLUDE[prod_short](includes/prod_short.md)]. This means that the same report might look different when using the Word report layout compared to the RDLC report layout.

* The process for setting up Word, Excel, and RDLC report layouts on reports is the same. The main difference is in the way you modify the layouts. Word and especially Excel layouts are typically easier to create and modify than RDLC report layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.

* Not all reports and document have a dataset that is optimized for use with an Excel layout. For example, aggregations and complex calculations work best with RDLC or Word layouts. The same is true for documents.

For information about how to switch the layout currently used on a report, see [Set the Layout Used by a Report](ui-set-report-layout.md).

-->
## Zie ook

[Aangepaste rapportlay-outs bijwerken](ui-update-report-layouts.md)  
[Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md)  
[Een aangepaste indeling voor een rapport of document importeren en exporteren](ui-how-import-and-export-report-layout.md)  
[Speciale documentlay-outs definiëren voor klanten en leveranciers](ui-define-customer-vendor-document-layouts.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[Werken met rapporten, batchverwerkingen en XMLports](ui-work-report.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
