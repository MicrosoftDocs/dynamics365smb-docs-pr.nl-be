---
title: Werken met rapporten, batchverwerkingen en XMLports
description: Leren over het invoeren van een lijst in een verwerkingswachtrij en het plannen om te worden verwerkt op een specifieke datum en tijd.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report, print, schedule, save, Excel, PDF, Word, dataset
ms.date: 06/21/2021
ms.author: jswymer
ms.openlocfilehash: 9deb7e30e05da74e6ea263a0262680d2e99b8b4b
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6439962"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Werken met rapporten, batchverwerkingen en XMLports

Een rapport verzamelt informatie op basis van een gespecificeerde set criteria. Het organiseert en presenteert de informatie in een gemakkelijk te lezen formaat dat u kunt afdrukken of opslaan als een bestand. In de toepassing zijn er vele diverse rapporten die u kunt openen en gebruiken. De rapporten bieden veelal informatie in de context van de pagina waarop u werkt. De pagina **Klant** biedt bijvoorbeeld rapporten voor de top 10 van klanten, verkoopstatistieken en meer.

Batchtaken en XMLports doen min of meer hetzelfde als rapporten, maar worden meer gebruikt voor de verwerking of export van gegevens. De batchverwerking **Aanmaningen maken** maakt bijvoorbeeld aanmaningsdocumenten voor klanten met achterstallige betalingen.  

> [!NOTE]
> Dit onderwerp verwijst hoofdzakelijk naar 'rapport', maar soortgelijke informatie geldt voor batchverwerkingen en XMLports.

## <a name="getting-started"></a>Aan de slag

U vindt rapporten op het tabblad **Rapporten** op bepaalde pagina's of u kunt zoeken gebruiken ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen") om rapporten op naam te vinden.

Wanneer u een rapport, batchtaak of XMLport opent, ziet u meestal een aanvraagpagina waarop u verschillende opties en filters kunt kiezen die bepalen wat er in het rapport wordt opgenomen. In de volgende secties wordt uitgelegd hoe u de aanvraagpagina gebruikt om een rapport te maken, te bekijken en af te drukken.

## <a name="using-default-values---predefined-settings"></a><a name="SavedSettings"></a>Standaardwaarden gebruiken: vooraf gedefinieerde instellingen 

De meeste aanvraagpagina's bevatten het veld **Standaardwaarden gebruiken uit**. In dit veld kunt u vooraf gedefinieerde instellingen voor het rapport selecteren, waarmee automatisch opties en filters voor het rapport worden ingesteld. Selecteer een item in de vervolgkeuzelijst en u zult zien dat de opties en filters op de aanvraagpagina dienovereenkomstig veranderen.

Het item genaamd **Laatst gebruikte opties en filters** is altijd beschikbaar. Dit item stelt het rapport in op opties en filters die waren gebruikt toen u het rapport voor de laatste keer uitvoerde.

Het veld **Standaardwaarden gebruiken uit** biedt een snelle en betrouwbare manier om consistent rapporten te genereren die de juiste gegevens bevatten. Nadat u een item hebt geselecteerd, kunt u de opties en filters wijzigen voordat u een voorbeeld bekijkt of het rapport afdrukt. De wijzigingen die u aanbrengt, worden niet opgeslagen in het item met vooraf gedefinieerde instellingen dat u hebt geselecteerd, maar worden wel opgeslagen in het item **Laatst gebruikte opties en filters**.

>[!NOTE]
> De vooraf gedefinieerde instellingen worden doorgaans ingesteld en beheerd door een beheerder. Als u meer wilt weten, raadpleegt u [Opgeslagen instellingen voor rapporten en batchtaken beheren](reports-saving-reusing-settings.md).

## <a name="specifying-the-data-to-include-in-reports"></a>De gegevens opgeven die in rapporten moeten worden opgenomen

Gebruik de velden onder **Opties** en **Filters** om de informatie die u in het rapport wilt, te wijzigen. U stelt filters in een rapport op ongeveer dezelfde manier in als filters in lijsten. Zie [Filteren](ui-enter-criteria-filters.md#filtering) voor meer informatie.

> [!CAUTION]
> De sectie **Filter lijst op** op een aanvraagpagina biedt een algemene filtermogelijkheid voor rapporten. Deze filters zijn optioneel.
>
> Sommige rapporten negeren dergelijke filters, wat inhoudt dat het niet uitmaakt welk filter is ingesteld in de sectie **Filter lijst op**. De uitvoer van het rapport is hetzelfde. U kunt geen lijst opgeven met welke velden worden genegeerd in welke rapporten, dus u zult met de filters moeten experimenteren wanneer u deze gebruikt.
>
> **Voorbeeld**: wanneer u de batchverwerking **Aanmaningen maken** gebruikt, wordt het filter **Laatste verz. aanmaningsniveau** voor het veld **Klantenposten** genegeerd omdat filters voor die batchverwerking vast zijn.

## <a name="previewing-a-report"></a>Een voorbeeld van een rapport bekijken

Als u een voorbeeld van een rapport bekijkt, kunt u zien hoe het rapport eruitziet voordat u het afdrukt. Het voorbeeld is niet gebaseerd op de geselecteerde printer in het veld **Printer** op de aanvraagpagina. Het wordt bestuurd door de browser. Nadat u een voorbeeld hebt bekeken, kunt u teruggaan naar de aanvraagpagina en indien nodig wijzigingen aanbrengen in opties en filters.

Om een voorbeeld van een rapport te bekijken kiest u de knop **Voorbeeld** of **Voorbeeld en sluiten** op de rapportverzoekpagina. De knop die wordt weergegeven, is afhankelijk van het rapport, dus sommige rapporten hebben de knop **Voorbeeld** terwijl andere de knop **Voorbeeld en sluiten** hebben. Beide knoppen openen een voorbeeld van het rapport. Het verschil is dat **Voorbeeld** de aanvraagpagina open houdt, zodat u ernaar kunt terugkeren, wijzigingen kunt aanbrengen, opnieuw een voorbeeld kunt bekijken of kunt afdrukken. Met **Voorbeeld en sluiten** wordt de aanvraagpagina gesloten, dus u moet het rapport opnieuw openen om wijzigingen aan te brengen of af te drukken.

> [!NOTE]
> Als u Business Central 2020 releasewave 1 of eerder gebruikt, is er alleen een knop **Voorbeeld**, die de aanvraagpagina met het voorbeeld sluit, zoals beschreven voor **Voorbeeld en sluiten**.

### <a name="working-with-the-preview"></a>Werken met de preview

Gebruik in het rapportvoorbeeld de menubalk om het volgende te doen:

- Door pagina's bladeren
- In- en uitzoomen
- Het formaat aanpassen aan de afmetingen van de pagina
- Tekst selecteren

    U kunt tekst uit een rapport kopiëren en die vervolgens ergens anders plakken, zoals als op een pagina in [!INCLUDE[prod_short](includes/prod_short.md)] of Microsoft Word.  Met bijvoorbeeld een muis houdt u ingedrukt waar u wilt beginnen. Beweeg vervolgens de muis om een of meer woorden, zinnen of alinea's te selecteren. Druk op de rechtermuisknop en selecteer **Kopiëren**. U kunt de geselecteerde tekst vervolgens overal plakken.
- Document pannen

    U kunt het zichtbare deel van het rapport in iedere richting verplaatsen, zodat u andere delen kunt bekijken. Pannen is handig als u hebt ingezoomd om details te zien.  U kunt bijvoorbeeld op een willekeurige plek in het rapportvoorbeeld klikken, de muisknop vasthouden en dan de muis verplaatsen.

- Downloaden naar een PDF-bestand op uw computer of netwerk.
- Afdrukken

## <a name="saving-a-report-to-a-file"></a>Een rapport opslaan in een bestand

U kunt een rapport opslaan als een PDF-document, een Microsoft Word-document of een Microsoft Excel-werkblad. Kies hiervoor de knop **Verzenden naar** en maak uw selectie.

### <a name="send-to-excel"></a>Verzenden naar Excel

<!-- The following table describes the options for saving the report results as a worksheet in an Excel workbook.

|Option  |Description  |
|---------|---------|
|Microsoft Excel Document (data and layout)|Export the report results with the RDLC layout applied. Use this option if you want to export the data one time, and only want to make minor changes to its appearance, such as font and color scheme. <br><br>**Note**: Some reports might export numbers as text, so it's a good idea to verify the numbers. |
|Microsoft Excel Document (data only)|Export the report results and the criteria that was used to generate them, such as the parameters you specified on the request page, metadata, and the fields that control the layout of the printed report. Use this option when you want to do ad hoc analysis of the data or diagnose data issues in reports. For example, you can filter the data and use Power Pivot to display it.<br><br>This option exports all columns, including columns that hold formatting instructions for other values and filters. In columns that hold binary data like images, instead of actually values, fields will include the text **Binary data ({0} bytes)**, where **{0}** indicates the number of bytes.<br><br>**NOTE** With Business Central on-premises, the Business Central Server includes a configurations setting, called **Max Data Rows Allowed to Send to Excel**. This setting limits the number of rows that can be exported to Excel. If you don't see the expected number of rows, it might be because of this setting. For more information, see [Configuring Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) or contact your administrator.|-->

Er zijn twee opties om de rapportresultaten op te slaan als een werkblad in een Excel-werkmap: **Microsoft Excel-document (gegevens en lay-out)** en **Microsoft Excel-document (alleen gegevens)**

#### <a name="microsoft-excel-document-data-and-layout"></a>[Microsoft Excel-document (gegevens en lay-out)](#tab/data-and-layout)

Deze optie is alleen beschikbaar voor rapporten die een RDLC-lay-out gebruiken. Het exporteert de rapportresultaten met de RDLC-lay-out. Gebruik deze optie als u de gegevens eenmalig wilt exporteren en alleen kleine wijzigingen wilt aanbrengen in het uiterlijk, zoals lettertype en kleurenschema.

#### <a name="microsoft-excel-document-data-only"></a><a name="exportdataonly"></a>[Microsoft Excel-document (alleen gegevens)](#tab/data-only)

De optie **Microsoft Excel-document (alleen gegevens)** exporteert de rapportresultaten en de criteria die werden gebruikt om ze te genereren&mdash;maar het omvat niet de rapportlay-out. Het Excel-bestand bevat de volledige dataset, als onbewerkte gegevens, gerangschikt in rijen en kolommen. Alle gegevenskolommen van de gegevensset van het rapport worden opgenomen, ongeacht of ze in de rapportlay-out worden gebruikt.  Gebruik deze optie wanneer u:

- Adhoc-analyse van de gegevens uitvoert. U kunt bijvoorbeeld de gegevens filteren en Power Pivot gebruiken om ze weer te geven.

  Elke keer dat u resultaten exporteert, wordt er een nieuw werkblad gemaakt. Met de optie **Microsoft Excel document (alleen gegevens)** kunt u hetzelfde rapport uitvoeren en opmaakwijzigingen opnieuw gebruiken. Bijvoorbeeld voor Power Pivot kunt u het rapport opnieuw uitvoeren voor een andere periode, de resultaten naar het werkblad kopiëren en het werkblad vervolgens vernieuwen. U vindt ook een rapportage-app op [AppSource](https://appsource.microsoft.com/).
- Inspecteer de rapportgegevensset wanneer u aangepaste rapportlay-outs maakt of wijzigt.

  Zie voor informatie over het maken van aangepaste rapportlay-outs: [Aangepaste rapportlay-outs maken of wijzigen](ui-how-create-custom-report-layout.md)
- Diagnose van gegevensproblemen in rapporten.

##### <a name="for-administrators"></a>Voor beheerders

- **Microsoft Excel-document (alleen gegevens)** werd geïntroduceerd als een optionele functie in de releasewave 1 van 2021, update 18.3. Om gebruikers toegang te geven tot deze functie, schakelt u de functie-update **Rapportgegevensset opslaan in Microsoft Excel-document** in **Functiebeheer** in. Zie voor meer informatie [Aankomende functies van tevoren inschakelen](/dynamics365/business-central/dev-itpro/administration/feature-management). In releasewave 2 van 2021 wordt deze functie permanent, dus hoeft u deze niet in te schakelen.

- Gebruikersaccounts hebben de machtiging **<!--Export Report Dataset To Excel-->Actie Rapportgegevensset exporteren naar Excel toestaan** nodig, die u kunt toepassen met behulp van de machtigingenset **Hulpprogramma's voor probleemoplossing** of **Rapport naar Excel exporteren**.  

- U kunt geen rapport exporteren met meer dan 1,048,576 rijen of 16.384 kolommen.

    > [!NOTE]
    > Met Business Central on-premises is het maximum aantal geëxporteerde rijen mogelijk nog lager. Business Central Server bevat een configuratie-instelling, genaamd **Max. gegevensrijen die naar Excel kunnen worden verzonden**, voor het verlagen van de limiet vanaf de maximale waarde. Voor meer informatie zie [Business Central Server configureren](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) of neem contact op met uw beheerder.

##### <a name="for-developers-and-advanced-users"></a>Voor ontwikkelaars en gevorderde gebruikers

De optie **Microsoft Excel-document (alleen gegevens)** exporteert alle kolommen, inclusief kolommen die filters en opmaakinstructies voor andere waarden bevatten. Hier zijn een paar aandachtspunten:

- Binaire gegevens in een veld, zoals een afbeelding, worden niet geëxporteerd.

  In kolommen die binaire gegevens bevatten, bevatten velden de tekst **Binaire gegevens ({0} bytes)**, waar **{0}** het aantal bytes aangeeft.
- Vanaf Business Central 2021 releasewave 2 bevat het Excel-bestand ook het werkblad **Metagegevens rapporteren**.

  Dit werkblad toont de filters die zijn toegepast op het rapport en algemene rapporteigenschappen, zoals de naam, id en extensiedetails. De filters worden weergegeven in de kolom **Filter (DataItem::Table::FilterGroupNo::FieldName)**. De filters in deze kolom bevatten filters die zijn ingesteld op de aanvraagpagina van het rapport. Het bevat ook filters die zijn gedefinieerd in AL-code, bijvoorbeeld door de [eigenschap DataItemLink](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemlink-reports-property) en de [eigenschap DataItemTableView](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataitemtableview-property).

Voor meer informatie over rapportontwerp zie [Rapportoverzicht](/dynamics365/business-central/dev-itpro/developer/devenv-reports).

---

> [!NOTE]
> Sommige rapporten exporteren getallen als tekst, waardoor u geen berekeningen kunt maken of Power Pivot kunt gebruiken op de cellen in het Excel-werkblad. Na het exporteren is het een goed idee om de getallen in het werkblad te controleren. Als u de cijfers wilt analyseren en in kaart wilt brengen, wijzigt u het formaat van de relevante cellen van **Tekst** in **Getal**. Zie deze video voor meer informatie over het opmaken van getallen in cellen: [Getallen opmaken in cellen in Microsoft Excel](https://www.youtube.com/watch?v=2suE4YmZu_Q).

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a>Een rapport plannen voor uitvoering

U kunt een batchtaak plannen voor uitvoering op een bepaalde datum en tijd. Geplande rapporten en batchtaken worden in de verwerkingswachtrij ingevoerd en verwerkt op het geplande tijdstip, net zoals andere taken. U kiest de optie **Schema** nadat u de knop **Verzenden naar** hebt gekozen en voert vervolgens informatie in zoals de printer en tijd en datum. Het rapport wordt vervolgens toegevoegd aan de taakwachtrij en wordt op de opgegeven tijd uitgevoerd. Als het rapport is verwerkt, wordt het artikel verwijderd uit de verwerkingswachtrij. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).  

Wanneer u een rapport plant dat moet worden uitgevoerd, kunt u bijvoorbeeld opgeven dat het elke donderdag moet worden uitgevoerd door het veld **Formule voor volgende uitvoeringsdatum** in te stellen op *D4*. Zie voor meer informatie [Datumformules gebruiken](ui-enter-date-ranges.md#using-date-formulas).  

U kunt ervoor kiezen het rapport op te slaan in een bestand, zoals een Excel-, Word- of PDF-bestand, het af te drukken of het rapport alleen te genereren. Als u ervoor kiest het rapport in een bestand op te slaan, wordt het verwerkte rapport naar het gebied **Rapportinbox** in uw rolcentrum verzonden, waar u het kunt bekijken.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Een rapport afdrukken

Als u een rapport wilt afdrukken, kiest u de knop **Afdrukken** op de aanvraagpagina of op de menubalk op de pagina **Voorbeeld**.

### <a name="printer"></a><a name="Printer"></a>Printer

Het veld **Printer** op de aanvraagpagina bevat de naam van de printer waar het rapport heen wordt gestuurd. Om een printer te wijzigen selecteert u de printer in de lijst.

> [!NOTE]
> **(Door de browser afgehandeld)** geeft aan dat er geen aangewezen printer is voor het rapport. In dit geval zal de browser de afdruk afhandelen en een standaardervaring weergeven, waarbij u een lokale printer kunt kiezen die op uw apparaat is aangesloten. **(Afgehandeld door de browser)** is niet beschikbaar in de mobiele [!INCLUDE[prod_short](includes/prod_short.md)]-app of de app voor Microsoft Teams.

> [!TIP]
> De printer die standaard voor u is geselecteerd, wordt ingesteld op de pagina **Printerselecties**. Zie voor informatie over het wijzigen van de standaardprinter [Selecteren welke printers welke rapporten afdrukken](ui-specify-printer-selection-reports.md#default).

### <a name="printing-reports-in-thai"></a>Rapporten afdrukken in het Thai

Specifiek voor de Thaise versie van [!INCLUDE[prod_short](includes/prod_short.md)] kan de knop **Afdrukken** geen rapporten correct afdrukken vanwege beperkingen in de service die het afdrukbare PDF-bestand genereert. In plaats hiervan kunt u het rapport openen in Word en vervolgens opslaan als een afdrukbare PDF.  

U kunt ook de beheerder vragen een Word-rapportlay-out te maken voor uw meest gebruikte rapporten. Zie voor meer informatie [Lay-outs van rapporten en documenten beheren](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Rapportindelingen wijzigen

Een rapportlay-out bepaalt wat in een rapport wordt weergegeven, hoe het is ingedeeld en hoe het is opgemaakt. Zie [De huidige rapportindeling wijzigen](ui-how-change-layout-currently-used-report.md) als u naar een andere indeling wilt overschakelen. Of zie [Een aangepaste lay-out voor een rapport maken en wijzigen](ui-how-create-custom-report-layout.md) als u uw eigen rapportlay-out wilt aanpassen.

## <a name="advanced-options"></a>Geavanceerde opties

De velden onder **Geavanceerd** stellen beperkingen in voor het gegenereerde rapport om printerbronnen te beheren. U hoeft deze instellingen doorgaans niet te wijzigen, tenzij u een groot rapport hebt. Als een rapport deze beperkingen overschrijdt wanneer u een voorbeeld probeert te bekijken of probeert af te drukken, verschijnt er een bericht waarin staat welke beperking is overschreden. U kunt de instellingen vervolgens aanpassen aan uw rapport. Elk veld heeft echter een maximale waarde waarvan u op de hoogte moet zijn:

|Veld|Maximale waarde|
|-----|-------------|
|Maximale weergavetijd|12:00:00|
|Maximaal aantal rijen|1000000|
|Maximaal aantal documenten|500|

> [!NOTE]
> De maximale waarden kunnen verschillen voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises en een beheerder kan ze wijzigen. Zie [Business Central Server configureren: rapporten](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports) voor meer informatie. Voor een overzicht van rapportbeperkingen in [!INCLUDE[prod_short](includes/prod_short.md)] online, raadpleegt u [Operationele limieten](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## <a name="see-also"></a>Zie ook

[Printers instellen](ui-specify-printer-selection-reports.md)  
[Werken met agendadatums en -tijden](ui-enter-date-ranges.md)  
[Indelingen van rapporten en documenten beheren](ui-manage-report-layouts.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]