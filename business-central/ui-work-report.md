---
title: Een rapport plannen voor uitvoering op een bepaalde datum en tijd | Microsoft Docs
description: Leren over het invoeren van een lijst in een verwerkingswachtrij en het plannen om te worden verwerkt op een specifieke datum en tijd.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 06/10/2020
ms.author: edupont
ms.openlocfilehash: f209088459f29ba5618b065c3a340b0e3bd250e5
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788424"
---
# <a name="working-with-reports-batch-jobs-and-xmlports"></a>Werken met rapporten, batchverwerkingen en XMLports

In een rapport wordt informatie verzameld op basis van een bepaalde reeks criteria. De informatie wordt hierin weergegeven in een makkelijk leesbare indeling die u kunt afdrukken of opslaan als een bestand. In de toepassing zijn er vele diverse rapporten die u kunt openen en gebruiken. De rapporten bieden veelal informatie in de context van de pagina waarop u werkt. De pagina **Klant** biedt bijvoorbeeld rapporten voor de top 10 van klanten, verkoopstatistieken en meer.

Batchtaken en XMLports doen min of meer hetzelfde als rapporten, maar met als doel een proces uit te voeren of gegevens te exporteren. De batchverwerking **Aanmaningen maken** maakt bijvoorbeeld aanmaningsdocumenten voor klanten met achterstallige betalingen.  

> [!NOTE]
> Dit onderwerp verwijst hoofdzakelijk naar 'rapport', maar soortgelijke informatie geldt voor batchverwerkingen en XMLports.

U vindt rapporten op het tabblad **Rapporten** op bepaalde pagina's of u kunt zoeken in ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen") om rapporten op naam te vinden.

## <a name="specifying-the-data-to-include-in-reports"></a>De gegevens opgeven die in rapporten moeten worden opgenomen
Wanneer u een rapport, batchtaak of XMLport opent, ziet u meestal een aanvraagpagina waarop u verschillende opties en filters kunt kiezen die bepalen wat er in het rapport wordt opgenomen.

U stelt filters in een rapport op ongeveer dezelfde manier in als filters in lijsten. Zie [Filteren](ui-enter-criteria-filters.md#filtering) voor meer informatie.

> [!CAUTION]
> De sectie **Filter lijst op** op een aanvraagpagina biedt een algemene filtermogelijkheid voor rapporten. Deze filters zijn optioneel.
>
> Sommige rapporten negeren dergelijke filters, wat inhoudt dat het niet uitmaakt welk filter is ingesteld in de sectie **Filter lijst op**. De uitvoer van het rapport is hetzelfde. U kunt geen lijst opgeven met welke velden worden genegeerd in welke rapporten, dus u zult met de filters moeten experimenteren wanneer u deze gebruikt.
>
> **Voorbeeld**: wanneer u de batchverwerking **Aanmaningen maken** gebruikt, wordt het filter **Laatste verz. aanmaningsniveau** voor het veld **Klantenposten** genegeerd omdat filters voor die batchverwerking vast zijn.

## <a name="using-saved-settings"></a><a name="SavedSettings"></a>Opgeslagen instellingen gebruiken
De aanvraagpagina kan de sectie **Opgeslagen instellingen** bevatten, die een of meer items bevat in het vak **Standaardwaarde gebruiken uit**. Een opgeslagen instelling is een vooraf gedefinieerde groep opties en filters, die u op het rapport kunt toepassen voordat u er een voorbeeld van bekijkt of het rapport naar een bestand stuurt. De opgeslagen instelling met de naam **Laatst gebruikte opties en filters** is altijd beschikbaar. Deze vermelding stelt het rapport in op de opties en filters die waren ingesteld toen het rapport voor de laatste keer werd gebruikt.

Met behulp van opgeslagen instellingen kunt u snel en betrouwbaar rapporten genereren die de juiste gegevens bevatten. Nadat u het vak **Standaardwaarde gebruiken uit** hebt ingesteld op een vermelding van een opgeslagen instelling, kunt u de opties en filters aanpassen voordat u een voorbeeld van het rapport bekijkt of het opslaat. De wijzigingen die u aanbrengt, worden niet opgeslagen in de vermelding van opgeslagen instellingen die u hebt geselecteerd, maar worden wel opgeslagen in de vermelding **Laatst gebruikte opties en filters**.

>[!NOTE]
>Als u beheerder bent, kunt u de opgeslagen instellingen van rapporten maken en beheren voor alle gebruikers. Zie voor meer informatie [Opgeslagen instellingen voor rapporten en batchtaken beheren](reports-saving-reusing-settings.md).

## <a name="previewing-a-report"></a>Een voorbeeld van een rapport bekijken

Kies de knop **Voorbeeld** om het rapport te zien op de rapportaanvraagpagina. Gebruik de menubalk in het rapportvoorbeeld om:

- Door pagina's bladeren
- In- en uitzoomen
- Het formaat aanpassen aan de afmetingen van de pagina
- Tekst selecteren

    U kunt tekst uit een rapport kopiëren en die vervolgens ergens anders plakken, zoals als op een pagina in [!INCLUDE[d365fin](includes/d365fin_md.md)] of Microsoft Word.  Met een muis kunt u bijvoorbeeld klikken op het punt van waaraf u wilt kopiëren, de muisknop ingedrukt houden en de muis verplaatsen om een of meer woorden, zinnen of alinea's te selecteren. Vervolgens kunt u met de rechtermuisknop klikken en **Kopiëren** selecteren. U kunt de geselecteerde tekst vervolgens overal plakken.
- Document pannen

    U kunt het zichtbare deel van het rapport in iedere richting verplaatsen, zodat u andere delen kunt bekijken. Dit is handig als u hebt ingezooomd om details te zien.  U kunt bijvoorbeeld op een willekeurige plek in het rapportvoorbeeld klikken, de muisknop vasthouden en dan de muis verplaatsen.

- Downloaden naar een PDF-bestand op uw computer of netwerk.
- Afdrukken

## <a name="saving-a-report"></a>Een rapport opslaan
U kunt een rapport opslaan als een PDF-document, een Microsoft Word-document of een Microsoft Excel-document. Kies hiervoor de knop **Verzenden naar** en maak uw selectie.

## <a name="scheduling-a-report-to-run"></a><a name="ScheduleReport"></a>Een rapport plannen voor uitvoering

U kunt een batchtaak plannen voor uitvoering op een bepaalde datum en tijd. Geplande rapporten en batchtaken worden in de verwerkingswachtrij ingevoerd en verwerkt op het geplande tijdstip, net zoals andere taken. U kiest de optie **Schema** nadat u de knop **Verzenden naar** hebt gekozen en voert vervolgens informatie in zoals de printer en tijd en datum. Het rapport wordt vervolgens toegevoegd aan de taakwachtrij en wordt op de opgegeven tijd uitgevoerd. Als het rapport is verwerkt, wordt het artikel verwijderd uit de verwerkingswachtrij. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).  

Wanneer u een rapport plant dat moet worden uitgevoerd, kunt u bijvoorbeeld opgeven dat het elke donderdag moet worden uitgevoerd door het veld **Formule voor volgende uitvoeringsdatum** in te stellen op *D4*. Zie voor meer informatie [Datumformules gebruiken](ui-enter-date-ranges.md#using-date-formulas).  

U kunt ervoor kiezen het verwerkte rapport op te slaan in een bestand, zoals een Excel-, Word- of PDF-bestand, het afdrukken op een geselecteerde printer of het rapport alleen verwerken. Als u ervoor kiest het rapport in een bestand op te slaan, wordt het verwerkte rapport naar het gebied **Rapportinbox** in uw rolcentrum verzonden, waar u het kunt bekijken.  

## <a name="printing-a-report"></a><a name="PrintReport"></a>Een rapport afdrukken

U kunt een rapport afdrukken door de knop **Afdrukken** te kiezen op de rapportaanvraagpagina of op de menubalk op de pagina **Voorbeeld**.

### <a name="printer-selection"></a>Printerselectie

Het rapport wordt afgedrukt naar de printer die wordt weergegeven in het **Geselecteerde printer** op de rapportaanvraagpagina. U kunt de printer vanaf deze pagina niet wijzigen.

De geselecteerde printer is ofwel ingesteld op de pagina **Printerselecties** of het is de standaardprinter die is ingesteld op de pagina **Printerbeheer**. Als u een andere printer wilt gebruiken, raadpleegt u [Printers instellen](ui-specify-printer-selection-reports.md).

Als er geen printer is opgegeven op de pagina **Printerselecties** of als standaard is ingesteld op de pagina **Printerbeheer**, wordt de afdrukfunctie van de browser gebruikt. In dit geval verschijnt **Browser** in het veld **Geselecteerde printer** op de rapportaanvraagpagina. 

### <a name="browser-printing"></a>Afdrukken met browser

Omdat [!INCLUDE[prodshort](includes/prodshort.md)] een cloudservice is, kan het geen lokale printers bereiken die zijn aangesloten op uw computer. Het kan echter verbinding maken met printers met cloudfunctionaliteit. In de generieke versie van [!INCLUDE[prodshort](includes/prodshort.md)], wordt een cloudprinter genaamd **E-mailprinter** geïnstalleerd als een extensie en is deze klaar voor gebruik na de eerste installatie.

Als geen cloudprinter is geïnstalleerd en ingesteld of als een geïnstalleerde printer niet werkt, wordt het afdrukken standaard ingesteld op de afdrukopties voor de browser.

> [!NOTE]
> De afdrukopties van de browser werken onafhankelijk van [!INCLUDE[prodshort](includes/prodshort.md)]. Dus alle printerinstellingen die mogelijk zijn ingesteld vanaf printers in [!INCLUDE[prodshort](includes/prodshort.md)], worden niet overgedragen naar de afdrukopties van de browser.

<!-- 
On the **Printer Management** page, you can see the printers that are set up. For more information, see [Set Up Printers](ui-specify-printer-selection-reports.md).

> [!NOTE]
> You can't change the **Printer** field on the report request page. To use another printer, you must select it from the **Printer Management** page.
-->
### <a name="printing-reports-in-thai"></a>Rapporten afdrukken in het Thai
Specifiek voor de Thaise versie van [!INCLUDE[prodshort](includes/prodshort.md)] kan de knop **Afdrukken** geen rapporten correct afdrukken vanwege beperkingen in de service die het afdrukbare PDF-bestand genereert. In plaats hiervan kunt u het rapport openen in Word en vervolgens opslaan als een afdrukbare PDF.  

U kunt ook de beheerder vragen een Word-rapportlay-out te maken voor uw meest gebruikte rapporten. Zie voor meer informatie [Lay-outs van rapporten en documenten beheren](ui-manage-report-layouts.md).  

## <a name="changing-report-layouts"></a>Rapportindelingen wijzigen
Een rapportlay-out bepaalt wat in een rapport wordt weergegeven, hoe het is ingedeeld en hoe het is opgemaakt. Zie [De huidige rapportindeling wijzigen](ui-how-change-layout-currently-used-report.md) als u naar een andere indeling wilt overschakelen. Of zie [Een aangepaste lay-out voor een rapport maken en wijzigen](ui-how-create-custom-report-layout.md) als u uw eigen rapportlay-out wilt aanpassen.

## <a name="see-also"></a>Zie ook

[Printers instellen](ui-specify-printer-selection-reports.md)  
[Werken met agendadatums en -tijden](ui-enter-date-ranges.md)  
[Indelingen van rapporten en documenten beheren](ui-manage-report-layouts.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
