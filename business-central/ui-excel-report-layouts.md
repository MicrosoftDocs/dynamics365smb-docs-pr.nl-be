---
title: Werken met Excel-lay-outs
description: Meer informatie over hoe u rapportlay-outs maakt en wijzigt die zijn ontwikkeld met Excel.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9650, 9652
ms.date: 03/14/2022
ms.author: jswymer
ms.openlocfilehash: 609678742ccf9593407e96ea412a377f37c8abf9
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8525387"
---
# <a name="working-with-excel-layouts"></a>Werken met Excel-lay-outs

Excel-rapportlay-outs zijn gebaseerd op Microsoft Excel werkmappen (.xlsx-bestanden). Hiermee kunt u rapporten maken met behulp van vertrouwde Excel-functies voor het samenvatten, analyseren en presenteren van gegevens, zoals formules, draaitabellen en draaigrafieken.

![Toont een voorbeeld van een Excel-lay-out.](media/excel-layout-2.png)

In dit artikel worden enkele van de belangrijkste dingen uitgelegd die u moet weten om aan de slag te gaan met Excel-lay-outs.

## <a name="why-use-excel-layouts"></a>Waarom Excel-lay-outs gebruiken?

Hier zijn nog enkele voordelen van het gebruik van Excel-lay-outs:

- Interactieve rapporten maken met behulp van visualisaties zoals slicers
- Onbewerkte gegevens bekijken uit de rapportgegevensset om te begrijpen hoe het rapport werkt en waar de gegevens op visuele elementen vandaan komen
- Ingebouwde Office-functies gebruiken voor nabewerking van weergegeven rapporten, zoals:
  - [De werkbladen beschermen](https://support.microsoft.com/en-us/office/protect-a-worksheet-3179efdb-1285-4d49-a9c3-f4ca36276de6)
  - [Vertrouwelijkheidslabels toepassen](https://support.microsoft.com/en-us/office/apply-sensitivity-labels-to-your-files-and-email-in-office-2f96e7cd-d5a4-403b-8bd7-4cc636bae0f9)
  - [Opmerkingen en notities toevoegen](https://support.microsoft.com/en-us/office/insert-comments-and-notes-in-excel-65f504d8-160b-4a05-ac30-46fbd5227a52)
  - [Prognose en analyse](https://support.microsoft.com/en-us/office/introduction-to-what-if-analysis-22bffa5f-e891-4acc-bf7a-e4645c446fb4) 
- Gebruik geïnstalleerde invoegtoepassingen en app-integraties, zoals Power Automate-stromen of OneDrive.

## <a name="get-started"></a>Aan de slag

Er zijn in principe twee taken betrokken bij het instellen van een Excel-lay-out voor een rapport:

1. Maak het bestand met de nieuwe Excel-lay-out.
2. Voeg de nieuwe lay-out toe aan het rapport.

## <a name="task-1-create-the-excel-layout-file"></a>Taak 1: het bestand met de nieuwe Excel-lay-out maken

Er zijn drie manieren om een Excel-lay-outbestand voor een rapport te maken, zoals uitgelegd in deze sectie

### <a name="from-any-report"></a>[Vanuit een willekeurig rapport](#tab/any-report)

U kunt de volgende stappen gebruiken om een Excel-lay-out te maken vanuit een willekeurig rapport, ongeacht het huidige lay-outtype. De Excel-lay-out bevat het blad en de tabel **Gegevens** die vereist zijn, een blad **Rappportmetagegevens** en verder niets.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Selecteer in de lijst **Rapportlay-outs** een lay-out voor het rapport en kies vervolgens de actie **Rapport uitvoeren**.
3. Selecteer op de rapportaanvraagpagina **Verzenden naar** > **Microsoft Excel-document (alleen gegevens)** > **OK**.

   Met deze stap wordt een Excel-werkmap gedownload die de rapportgegevensset bevat.
4. Open het gedownloade bestand in Excel, breng de wijzigingen aan en sla het bestand op.

### <a name="from-another-excel-layout-on-a-report"></a>[Vanuit een andere Excel-lay-out in een rapport](#tab/other-layout)

Als er al een Excel-lay-out voor een rapport is, gebruikt u de bestaande lay-out als uitgangspunt. Er zijn twee manieren om een kopie van de lay-out te krijgen. U kunt de bestaande lay-out exporteren vanaf de pagina **Rapportlay-outs** of de lay-out downloaden vanaf de aanvraagpagina van het rapport. Met beide manieren wordt een Excel-lay-outbestand gedownload dat alle bladen van het bestaande bestand bevat. Het verschil is dat vanaf de aanvraagpagina de lay-out feitelijke gegevens zal bevatten. De gegevens zijn niet vereist, maar helpen bij het ontwerpen van de lay-out.

#### <a name="approach-1-export-the-layout-from-the-report-layouts-page"></a>Manier 1: de lay-out vanaf de pagina **Rapportlay-outs** exporteren

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Selecteer de Excel-lay-out in de lijst en kies vervolgens de actie **Lay-out exporteren** boven aan de pagina.
3. Open het bestand in Excel, breng de wijzigingen aan en sla het bestand op.

#### <a name="approach-2-download-the-layout-from-the-reports-request-page"></a>Manier 2: de lay-out vanaf de aanvraag pagina van het rapport downloaden

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Selecteer in de lijst **Rapportlay-outs** een lay-out voor het rapport en kies vervolgens de actie **Rapport uitvoeren**.
3. Selecteer **Downloaden** op de rapportaanvraagpagina.
4. Open het bestand in Excel, breng de wijzigingen aan en sla het bestand op.

### <a name="from-al-code"></a>[Van AL-code](#tab/from-code)

Deze manier is het meest geavanceerd. Het vereist kennis van AL-code, dus het is gericht op programmeurs. De Excel-lay-outs maken in dit geval deel uit van een extensiepakket dat u installeert. Zie voor meer informatie [Een Excel-lay-outrapport maken](/dynamics365/business-central/dev-itpro/developer/devenv-howto-excel-report-layout) in de Help voor ontwikkelaars en IT-professionals.

---

## <a name="task-2-add-the-excel-layout-to-the-report"></a>Taak 2: de Excel-lay-out toevoegen aan het rapport

Zodra u het Excel-lay-outbestand hebt, is de volgende taak om het toe te voegen als een nieuwe lay-out voor het rapport.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Selecteer **Nieuwe lay-out**.
3. Stel de **Rapport-id** in op rapport.
4. Voer een naam in **Lay-outnaam** in.
5. Stel **Opties voor opmaak** in op **Excel**.
6. Selecteer **OK** > **Kiezen** om de bestandsverkenner op uw apparaat te openen. 
7. Zoek en selecteer het Excel-bestand en kies vervolgens **Openen**.

   Het geselecteerde bestand wordt geüpload naar de lay-out en u keert terug naar de pagina **Rapportlay-outs**.
8. Als u wilt zien hoe het rapport eruitziet met de nieuwe lay-out, selecteert u de lay-out in de lijst en selecteert u vervolgens **Rapport uitvoeren**.


<!--

**Data** sheet
  - An Excel layout must contain a sheet named **Data**.
  - The **Data** sheet can only include one table named **Data**.

**Data** table
  - The **Data** sheet must include a table that has the name **Data**.
  - The table must have at least one column and can only include columns that are also in report dataset.
  - The table must start in the first cell A1 of the **Data** sheet.

3. Report Metadata 
-->

## <a name="understanding-excel-layouts"></a>Excel-lay-outs begrijpen

Er zijn een paar dingen die u moet weten of overwegen wanneer u begint met het maken of wijzigen van Excel-lay-outs. Elke Excel-lay-out moet twee elementen bevatten: een blad **Gegevens** en een tabel **Gegevens**. Deze elementen vormen de basis van de lay-out door de bedrijfsgegevens uit Business Central te definiëren waarmee u aan de slag kunt. Zie het blad **Gegevens** als een soort contract tussen de lay-outs in de bedrijfsgegevens. U gebruikt deze gegevens als bron van berekeningen en visualisaties die u op andere werkbladen wilt presenteren.

Er zijn enkele specifieke vereisten voor de structuur van de Excel-werkmap. Als niet aan de vereisten wordt voldaan, ondervindt u problemen bij het gebruik van de lay-out. Het volgende diagram en de tabel geven een overzicht van de elementen van een Excel-lay-out en de vereisten.

[![Toont de verschillende elementen van een Excel-lay-out.](media/excel-layout-callouts-2.png)](media/excel-layout-callouts-2.png#lightbox)

|Nee.|Element|Omschrijving|Verplicht|
|---|-------|----|---|
|1|Blad **Gegevens**|<ul><li>Moet de naam **Gegevens** hebben</li><li>Kan slechts één tabel bevatten en de tabel moet de naam **Gegevens** hebben</li></ul>|![Is verplicht](media/check.png) | 
|2|Tabel **Gegevens**|<ul><li>Moet de naam **Gegevens** hebben</li><li>Moet minimaal één kolom hebben.</li><li>Kan alleen kolommen bevatten die in de rapportgegevensset staan.</li><li>Moet in de eerste cel, **A1**, van het blad **Gegevens** beginnen.</li></ul>|![Is verplicht](media/check.png)|
|3|Presentatiebladen|<ul><li>Wordt gebruikt om gegevens te presenteren.</li><li>Gegevens komen van het blad **Gegevens**. </li></ul>||
|4|Blad **Rappportmetagegevens**|<ul><li>Wordt automatisch opgenomen als de lay-out is gemaakt door een ander rapport als Excel te exporteren</li><li>Bevat algemene informatie over het rapport</li><li>Kan worden verwijderd</li></ul>|

Om samen te vatten wat u wel en niet kunt doen op het blad **Gegevens**:

- Verander de naam van het blad **Gegevens**, de tabel **Gegevens** of van kolommen niet.
- U kunt kolommen verwijderen of verbergen.
- Voeg geen kolommen toe, tenzij deze zijn opgenomen in de rapportgegevensset.
- U kunt de bladen in willekeurige volgorde plaatsen. Bijvoorbeeld het blad **Gegevens** kan het eerste of het laatste zijn.

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Rapportlay-outs beheren](ui-manage-report-layouts.md)  
[De huidige rapportindeling wijzigen](ui-how-change-layout-currently-used-report.md)  
[Een aangepaste indeling voor een rapport of document importeren of exporteren](ui-how-import-and-export-report-layout.md)  
[Werken met rapporten, batchverwerkingen en XMLports](ui-work-report.md)  
[Financiële rapportage voorbereiden met rapportageschema's en rekeningcategorieën](bi-how-work-account-schedule.md) 
[Bedrijfsinformatie](bi.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Rapportgegevens analyseren met Excel](report-analyze-excel.md).


[!INCLUDE[footer-include](includes/footer-banner.md)]