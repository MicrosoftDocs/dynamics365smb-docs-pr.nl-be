---
title: Een rapport plannen voor uitvoering op een bepaalde datum en tijd | Microsoft Docs
description: Leren over het invoeren van een lijst in een verwerkingswachtrij en het plannen om te worden verwerkt op een specifieke datum en tijd.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: e4b1615ebf177db94e3dfb372809fa71ed2f1459
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4760179"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Werken met rapporten, batchverwerkingen en XMLports

In een rapport wordt informatie verzameld op basis van een bepaalde reeks criteria. De informatie wordt hierin weergegeven in een makkelijk leesbare indeling die u kunt afdrukken of opslaan als een bestand. In de toepassing zijn er vele diverse rapporten die u kunt openen en gebruiken. De rapporten bieden veelal informatie in de context van de pagina waarop u werkt. De pagina **Klant** biedt bijvoorbeeld rapporten voor de top 10 van klanten, verkoopstatistieken en meer.

Batchtaken en XMLports doen min of meer hetzelfde als rapporten, maar met als doel een proces uit te voeren of gegevens te exporteren. De batchverwerking **Aanmaningen maken** maakt bijvoorbeeld aanmaningsdocumenten voor klanten met achterstallige betalingen.  

> [!NOTE]
> Dit onderwerp verwijst hoofdzakelijk naar 'rapport', maar soortgelijke informatie geldt voor batchverwerkingen en XMLports.

## <a name="getting-started"></a>Aan de slag

U vindt rapporten op het tabblad **Rapporten** op bepaalde pagina's of u kunt zoeken ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen") om rapporten op naam te vinden.

Wanneer u een rapport, batchtaak of XMLport opent, ziet u meestal een aanvraagpagina waarop u verschillende opties en filters kunt kiezen die bepalen wat er in het rapport wordt opgenomen. In de volgende secties wordt uitgelegd hoe u de aanvraagpagina gebruikt om een rapport te maken, te bekijken en af te drukken.

## <a name="using-default-values---predefined-settings"></a><a name="SavedSettings"></a>Standaardwaarden gebruiken: vooraf gedefinieerde instellingen 

De meeste aanvraagpagina's bevatten het veld **Standaardwaarden gebruiken uit**. In dit veld kunt u vooraf gedefinieerde instellingen voor het rapport selecteren, waarmee automatisch opties en filters voor het rapport worden ingesteld. Selecteer een item in de vervolgkeuzelijst en u zult zien dat de opties en filters op de aanvraagpagina dienovereenkomstig veranderen.

Het item genaamd **Laatst gebruikte opties en filters** is altijd beschikbaar. Dit item stelt het rapport in op opties en filters die waren gebruikt toen u het rapport voor de laatste keer uitvoerde.

Het veld **Standaardwaarden gebruiken uit** biedt een snelle en betrouwbare manier om consistent rapporten te genereren die de juiste gegevens bevatten. Nadat u een item hebt geselecteerd, kunt u de opties en filters wijzigen voordat u een voorbeeld bekijkt of het rapport afdrukt. De wijzigingen die u aanbrengt, worden niet opgeslagen in het item met vooraf gedefinieerde instellingen dat u hebt geselecteerd, maar worden wel opgeslagen in het item **Laatst gebruikte opties en filters**.

>[!NOTE]
> De vooraf gedefinieerde instellingen worden doorgaans ingesteld en beheerd door een beheerder. Als u meer wilt weten, raadpleegt u [Opgeslagen instellingen voor rapporten en batchtaken beheren](reports-saving-reusing-settings.md).
<!--
Depending on the report, the request page might include the **Use default values from** field. This field lets you select a predefined set of can include the **Saved Settings** section that contains one or more entries in the **Use default value from** box. A saved setting is basically a predefined group of options and filters that you can apply to the report before previewing or sending the report to a file. The saved settings entry called **Last used options and filters** is always available. This entry sets the report to use options and filters that were used the last time you used the report.

Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data. After you set the **Use default value from** box to a saved settings entry, you can change any of the options and filters before previewing or saving the report. The changes that you make will not be saved to the saved settings entry you selected, but they will be saved to the **Last used options and filters** entry.

>[!NOTE]
>If you are an administrator, you can create and manage the saved settings for reports for all users. For more information, see [Manage Saved Settings for Reports and Batch Jobs](reports-saving-reusing-settings.md).
-->
## <a name="specifying-the-data-to-include-in-reports"></a>De gegevens opgeven die in rapporten moeten worden opgenomen

Gebruik de velden onder **Opties** en **Filters** om de informatie die u in het rapport wilt, te wijzigen. U stelt filters in een rapport op ongeveer dezelfde manier in als filters in lijsten. Zie [Filteren](ui-enter-criteria-filters.md#filtering) voor meer informatie.

> [!CAUTION]
> De sectie **Filter lijst op** op een aanvraagpagina biedt een algemene filtermogelijkheid voor rapporten. Deze filters zijn optioneel.
>
> Sommige rapporten negeren dergelijke filters, wat inhoudt dat het niet uitmaakt welk filter is ingesteld in de sectie **Filter lijst op**. De uitvoer van het rapport is hetzelfde. U kunt geen lijst opgeven met welke velden worden genegeerd in welke rapporten, dus u zult met de filters moeten experimenteren wanneer u deze gebruikt.
>
> **Voorbeeld**: wanneer u de batchverwerking **Aanmaningen maken** gebruikt, wordt het filter **Laatste verz. aanmaningsniveau** voor het veld **Klantenposten** genegeerd omdat filters voor die batchverwerking vast zijn.

## <a name="previewing-a-report"></a>Een voorbeeld van een rapport bekijken

Als u een voorbeeld van een rapport bekijkt, kunt u zien hoe het rapport eruitziet voordat u het afdrukt. Het voorbeeld zal het rapport opmaken op basis van de [printer](#Printer) die wordt weergegeven in het veld **Printer** op de aanvraagpagina. Nadat u een voorbeeld hebt bekeken, kunt u teruggaan naar de aanvraagpagina en indien nodig wijzigingen aanbrengen in opties en filters.

Om een voorbeeld van een rapport te bekijken kiest u de knop **Voorbeeld** of **Voorbeeld en sluiten** op de rapportverzoekpagina. De knop die wordt weergegeven, is afhankelijk van het rapport, dus sommige rapporten hebben de knop **Voorbeeld** terwijl andere de knop **Voorbeeld en sluiten** hebben. Beide knoppen openen een voorbeeld van het rapport. Het verschil is dat **Voorbeeld** de aanvraagpagina open houdt, zodat u ernaar kunt terugkeren, wijzigingen kunt aanbrengen, opnieuw een voorbeeld kunt bekijken of kunt afdrukken. Met **Voorbeeld en sluiten** wordt de aanvraagpagina gesloten, dus u moet het rapport opnieuw openen om wijzigingen aan te brengen of af te drukken.

> [!NOTE]
> Als u Business Central 2020 releasewave 1 of eerder gebruikt, is er alleen een knop **Voorbeeld**, die de aanvraagpagina met het voorbeeld sluit, zoals beschreven voor **Voorbeeld en sluiten**.

### <a name="working-with-the-preview"></a>Werken met de preview

Gebruik in het rapportvoorbeeld de menubalk om het volgende te doen:

- Door pagina's bladeren
- In- en uitzoomen
- Het formaat aanpassen aan de afmetingen van de pagina
- Tekst selecteren

    U kunt tekst uit een rapport kopiëren en die vervolgens ergens anders plakken, zoals als op een pagina in [!INCLUDE[prod_short](includes/prod_short.md)] of Microsoft Word.  Met een muis kunt u bijvoorbeeld drukken en vasthouden op het punt van waaraf u wilt beginnen, en dan de muis verplaatsen om een of meer woorden, zinnen of alinea's te selecteren. Druk op de rechtermuisknop en selecteer **Kopiëren**. U kunt de geselecteerde tekst vervolgens overal plakken.
- Document pannen

    U kunt het zichtbare deel van het rapport in iedere richting verplaatsen, zodat u andere delen kunt bekijken. Pannen is handig als u hebt ingezoomd om details te zien.  U kunt bijvoorbeeld op een willekeurige plek in het rapportvoorbeeld klikken, de muisknop vasthouden en dan de muis verplaatsen.

- Downloaden naar een PDF-bestand op uw computer of netwerk.
- Afdrukken

## <a name="saving-a-report"></a>Een rapport opslaan

U kunt een rapport opslaan als een PDF-document, een Microsoft Word-document of een Microsoft Excel-document. Kies hiervoor de knop **Verzenden naar** en maak uw selectie.

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a>Een rapport plannen voor uitvoering

U kunt een batchtaak plannen voor uitvoering op een bepaalde datum en tijd. Geplande rapporten en batchtaken worden in de verwerkingswachtrij ingevoerd en verwerkt op het geplande tijdstip, net zoals andere taken. U kiest de optie **Schema** nadat u de knop **Verzenden naar** hebt gekozen en voert vervolgens informatie in zoals de printer en tijd en datum. Het rapport wordt vervolgens toegevoegd aan de taakwachtrij en wordt op de opgegeven tijd uitgevoerd. Als het rapport is verwerkt, wordt het artikel verwijderd uit de verwerkingswachtrij. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).  

Wanneer u een rapport plant dat moet worden uitgevoerd, kunt u bijvoorbeeld opgeven dat het elke donderdag moet worden uitgevoerd door het veld **Formule voor volgende uitvoeringsdatum** in te stellen op *D4*. Zie voor meer informatie [Datumformules gebruiken](ui-enter-date-ranges.md#using-date-formulas).  

U kunt ervoor kiezen het rapport op te slaan in een bestand, zoals een Excel-, Word- of PDF-bestand, het af te drukken op een geselecteerde printer of het rapport alleen te genereren. Als u ervoor kiest het rapport in een bestand op te slaan, wordt het verwerkte rapport naar het gebied **Rapportinbox** in uw rolcentrum verzonden, waar u het kunt bekijken.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Een rapport afdrukken

Als u een rapport wilt afdrukken, kiest u de knop **Afdrukken** op de aanvraagpagina of op de menubalk op de pagina **Voorbeeld**.

<!--
### Printer selection

The report prints to the printer shown in the **Selected printer** field on the report request page. You can't change the printer from this page.

The selected printer is either set on the **Printer Selections** page or it's the default printer set up on the **Printer Management** page. If you want to use another printer, see  [Set Up Printers](ui-specify-printer-selection-reports.md).

If no printer is specified on the **Printer Selections** page or set as default on the **Printer Management** page, the browser printing feature is used. In this case, **Browser** appears in the **Selected printer** field on the report request page.
-->
### <a name="printer"></a><a name="Printer"></a>Printer

Het veld **Printer** op de aanvraagpagina bevat de naam van de printer waar het rapport heen wordt gestuurd. **(Door de browser afgehandeld)** geeft aan dat er geen aangewezen printer is voor het rapport. In dit geval zal de browser de afdruk afhandelen en een standaardervaring weergeven, waarbij u een lokale printer kunt kiezen die op uw apparaat is aangesloten.

U kunt de printer niet wijzigen met het veld **Printer**. Om de printer te wijzigen moet u naar de pagina **Printerselecties** of **Printerbeheer** gaan. Het instellen van de printer is doorgaans een beheerderstaak. Als u meer wilt weten, raadpleegt u [Printers instellen](ui-specify-printer-selection-reports.md).

<!--
### Browser printing

Because [!INCLUDE[prod_short](includes/prod_short.md)] is a cloud service, it can't reach local printers connected to your computer. However, it can connect to cloud-enabled printers. In the generic version of [!INCLUDE[prod_short](includes/prod_short.md)], a cloud printer named **Email Printer** is installed as an extension and is ready to use after initial setup.

If a cloud printer is not installed and set up, or if an installed printer fails, then printing will default to the printing options for the browser.

> [!NOTE]
> The browser printing options work independently of [!INCLUDE[prod_short](includes/prod_short.md)]. So any printer settings that might have been set up from printers in [!INCLUDE[prod_short](includes/prod_short.md)] aren't carried over to the browser print options.

<!-- 
On the **Printer Management** page, you can see the printers that are set up. For more information, see [Set Up Printers](ui-specify-printer-selection-reports.md).

> [!NOTE]
> You can't change the **Printer** field on the report request page. To use another printer, you must select it from the **Printer Management** page.
-->
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
