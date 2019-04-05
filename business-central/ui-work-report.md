---
title: Een rapport plannen voor uitvoering op een bepaalde datum en tijd | Microsoft Docs
description: Leren over het invoeren van een lijst in een verwerkingswachtrij en het plannen om te worden verwerkt op een specifieke datum en tijd.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process, report
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: 98d51b10d3ca415a463b58405cb3c4f2449b75ad
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/19/2019
ms.locfileid: "852436"
---
# <a name="working-with-reports-and-batch-jobs"></a>Werken met rapporten en batchverwerkingen
In een rapport wordt informatie verzameld op basis van een bepaalde reeks criteria. De informatie wordt hierin weergegeven in een makkelijk leesbare en afdrukbare indeling. In de toepassing zijn er vele diverse rapporten die u kunt openen en gebruiken. De rapporten bieden veelal informatie in de context van de pagina waarop u werkt. De pagina **Klant** biedt bijvoorbeeld rapporten voor de top 10 van klanten, voor de verkoopstatistieken en nog veel meer.

Batchverwerkingen doen min of meer hetzelfde als rapporten maar met het doel een proces uit te voeren. De batchverwerking **Aanmaningen maken** maakt bijvoorbeeld aanmaningsdocumenten voor klanten met achterstallige betalingen.  

> [!NOTE]
> Dit onderwerp verwijst hoofdzakelijk naar 'rapport', maar soortgelijke informatie geldt voor batchverwerkingen.

U vindt rapporten op het tabblad **Rapporten** op bepaalde pagina's of u kunt zoeken in ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen") om rapporten op naam te vinden.


## <a name="specifying-the-data-to-include-in-the-report"></a>De gegevens opgeven die in het rapport moeten worden opgenomen
Wanneer u een rapport opent, ziet u meestal een pagina waarop u verschillende opties en filters kunt kiezen die bepalen wat er in het rapport wordt opgenomen. Deze pagina wordt de rapportaanvraagpagina genoemd. Op de rapportaanvraagpagina kunt u bijvoorbeeld een rapport voor een specifieke klant maken, een bepaald datumbereik of de informatie in het rapport sorteren. Hier volgt een voorbeeld van een rapportaanvraagpagina:

![Rapportopties](media/report_options.png "Rapportopties")

> [!Caution]
> De sectie **Resultaten weergeven** op een aanvraagpagina biedt een algemene filtermogelijkheid voor rapporten. Deze filters zijn optioneel.<br /><br /> Sommige rapporten negeren dergelijke filters, wat inhoudt dat het niet uitmaakt welk filter is ingesteld in de sectie **Resultaten weergeven**. De uitvoer van het rapport is hetzelfde. U kunt geen lijst opgeven met welke velden worden genegeerd in welke rapporten, dus u zult met de filters moeten experimenteren wanneer u deze gebruikt.<br /><br />
**Voorbeeld**: wanneer u de batchverwerking **Aanmaningen maken** gebruikt, wordt het filter **Laatste verz. aanmaningsniveau** voor het veld **Klantenposten** genegeerd omdat filters voor die batchverwerking vast zijn.

### <a name="SavedSettings"></a>Opgeslagen instellingen gebruiken
Met sommige rapporten, afhankelijk van hoe ze zijn ontworpen, kan de rapportpagina het gedeelte **Opgeslagen instellingen** bevatten dat een of meer vermeldingen in het vak **Standaardwaarde gebruiken uit** bevat. De vermeldingen in dit vak worden *opgeslagen instellingen* genoemd. Een opgeslagen instelling is een vooraf gedefinieerde groep opties en filters, die u op het rapport kunt toepassen voordat u er een voorbeeld van bekijkt of het rapport naar een bestand stuurt. De opgeslagen instelling met de naam **Laatst gebruikte opties en filters** is altijd beschikbaar. Deze vermelding stelt het rapport in op de opties en filters die waren ingesteld toen het rapport voor de laatste keer werd bekeken.

Met behulp van opgeslagen instellingen kunt u snel en betrouwbaar rapporten genereren die de juiste gegevens bevatten. Nadat u het vak **Standaardwaarde gebruiken uit** hebt ingesteld op een vermelding van een opgeslagen instelling, kunt u de opties en filters aanpassen voordat u een voorbeeld van het rapport bekijkt of het opslaat. De wijzigingen die u aanbrengt, worden niet opgeslagen in de vermelding van opgeslagen instellingen die u hebt geselecteerd, maar ze worden wel opgeslagen in de **Laatst gebruikte opties en filters**.

>[!NOTE]
>Als u beheerder bent, kunt u de opgeslagen instellingen van rapporten maken en beheren voor alle gebruikers. Zie voor meer informatie [Opgeslagen instellingen in rapporten beheren](reports-saving-reusing-settings.md).

### <a name="setting-options-and-filters"></a>Opties en filters instellen
Als u de gegevens die in een rapport worden opgenomen verder wilt beperken of verfijnen, kunt u aanvullende filters en opties instellen.

Met filters kunt u gegevens weergeven op basis van bepaalde criteria. Filters worden gegroepeerd door de entiteit waartoe ze behoren, zoals **Klant** in de illustratie hierboven. U definieert een filter door het vak **Waar** in te stellen op het veld waarop u wilt filteren en vervolgens het criterium toe te voegen in het vak **is:**. In de illustratie hierboven bijvoorbeeld is er één filter dat het rapport maakt voor de klant van wie het **Nr.** gelijk is aan **01121212**.

U kunt meer filters toevoegen door de vakken **Toevoegen** in te stellen. Als u meer dan één filter hebt, worden alleen resultaten die aan de criteria van alle filters voldoen, opgenomen in het rapport.

Afhankelijk van het type veld dat u filtert, kunt u de filtercriteria opgeven om een exacte overeenkomst te zoeken, een gedeeltelijke overeenkomst, een bereik waarden en meer. Zie voor hulp bij het instellen van filters:
-   [Filteren](ui-enter-criteria-filters.md#FilterCriteria)
-   [Werken met agendadatums en -tijden](ui-enter-date-ranges.md)

## <a name="previewing-a-report"></a>Een voorbeeld van een rapport bekijken
Klik op **Voorbeeld** om het rapport te openen in uw internetbrowser. Wijs met de muisaanwijzer een gebied in het rapport aan om de menubalk op te roepen.  

![Werkbalk Afdrukvoorbeeld van rapport](media/report_viewer.png "Werkbalk Afdrukvoorbeeld van rapport")

Met de menubalk kunt u de volgende handelingen uitvoeren:

-   Door pagina's bladeren
-   In- en uitzoomen
-   Het formaat aanpassen aan de afmetingen van de pagina
-   Tekst selecteren

    U kunt tekst uit een rapport kopiëren en die vervolgens ergens anders plakken, zoals als op een pagina in [!INCLUDE[d365fin](includes/d365fin_md.md)] of Microsoft Word.  Met een muis kunt u bijvoorbeeld klikken op het punt van waaraf u wilt kopiëren, de muisknop ingedrukt houden en de muis verplaatsen om een of meer woorden, zinnen of alinea's te selecteren. Vervolgens klikt u met de rechtermuisknop en selecteert u **Kopiëren**. U kunt de geselecteerde tekst op elke gewenste plek plakken.
-   Document pannen

    U kunt het zichtbare deel van het rapport in iedere richting verplaatsen, zodat u andere delen kunt bekijken. Dit is handig als u hebt ingezooomd om details te zien.  U kunt bijvoorbeeld op een willekeurige plek in het rapportvoorbeeld klikken, de muisknop vasthouden en dan de muis verplaatsen.

-   Downloaden naar een PDF-bestand op uw computer of netwerk.
-   Afdrukken


## <a name="saving-a-report"></a>Een rapport opslaan
U kunt een rapport opslaan als een PDF-document, een Microsoft Word-document of een Microsoft Excel-document. Kies hiervoor **Verzenden naar** en selecteer de gewenste bestandsindeling.

## <a name="ScheduleReport"></a>Een rapport plannen voor uitvoering
U kunt een rapport plannen voor uitvoering op een bepaalde datum en tijd. Geplande rapporten worden in de verwerkingswachtrij ingevoerd en verwerkt op het geplande tijdstip, net zoals andere taken. U kunt ervoor kiezen het verwerkte rapport op te slaan in een bestand, zoals een Excel-, Word- of PDF-bestand, het afdrukken op een geselecteerde printer of het rapport alleen verwerken. Als u ervoor kiest het rapport in een bestand op te slaan, wordt het verwerkte rapport naar het gebied **Rapportinbox** in uw rolcentrum verzonden, waar u het kunt bekijken.

U kunt een rapport plannen wanneer u een rapport opent. U kiest de actie **Plannen** en voert vervolgens gegevens in, zoals printer en datum en tijd. Het rapport wordt vervolgens toegevoegd aan de taakwachtrij en wordt op de opgegeven tijd uitgevoerd. Als het rapport is verwerkt, wordt het artikel verwijderd uit de verwerkingswachtrij. Als u het verwerkte rapport in een bestand hebt opgeslagen, is het beschikbaar in het gebied **Rapportinbox**.

## <a name="PrintReport"></a>Een rapport afdrukken
U kunt een rapport afdrukken via de knop **Afdrukken** op de optiepagina die wordt weergegeven als u het rapport opent of via de menubalk in Voorbeeld.

## <a name="changing-the-layout-and-look-of-a-report"></a>De lay-out en weergave van een rapport weergeven
Een rapportlay-out bepaalt wat in een rapport wordt weergegeven, hoe het is ingedeeld en hoe het is opgemaakt. Zie [Wijzigen welke lay-out momenteel in een rapport wordt gebruikt](ui-how-change-layout-currently-used-report.md) als u naar een andere lay-out wilt schakelen. Of zie [Een aangepaste lay-out voor een rapport maken en wijzigen](ui-how-create-custom-report-layout.md) als u uw eigen rapportlay-out wilt aanpassen.

## <a name="see-also"></a>Zie ook
[Printerselectie opgeven voor rapporten](ui-specify-printer-selection-reports.md)  
[Lay-outs van rapporten en documenten beheren](ui-manage-report-layouts.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
