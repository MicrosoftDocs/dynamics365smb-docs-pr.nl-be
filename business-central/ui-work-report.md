---
title: Rapporten uitvoeren en afdrukken
description: Leren over het invoeren van een rapport in een verwerkingswachtrij en het plannen om te worden verwerkt op een specifieke datum en tijd.
author: jswymer
ms.topic: conceptual
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, Word, dataset'
ms.search.form: null
ms.date: 09/09/2022
ms.author: jswymer
---
# Rapporten uitvoeren en afdrukken

Een rapport verzamelt informatie op basis van een gespecificeerde set criteria. Het organiseert en presenteert de informatie in een gemakkelijk te lezen formaat dat u kunt afdrukken of opslaan als een bestand. In de toepassing zijn er vele diverse rapporten die u kunt openen en gebruiken. De rapporten bieden veelal informatie in de context van de pagina waarop u werkt. De pagina **Klant** biedt bijvoorbeeld rapporten voor de top 10 van klanten, verkoopstatistieken en meer.

> [!NOTE]
> Batchtaken en XMLports doen min of meer hetzelfde als rapporten, maar worden meer gebruikt voor de verwerking of export van gegevens. De batchverwerking **Aanmaningen maken** maakt bijvoorbeeld aanmaningsdocumenten om te verzenden naar klanten met achterstallige betalingen. Dit artikel verwijst hoofdzakelijk naar 'rapporten', maar soortgelijke informatie geldt voor batchverwerkingen en XMLports.

## Aan de slag

U vindt rapporten in het menu **Rapporten** op bepaalde pagina's, lijsten en kaarten of u kunt de zoekactie ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen") gebruiken om rapporten op naam te vinden. Voor een overzicht van ingebouwde rapporten in [!INCLUDE[prod_short](includes/prod_short.md)] die u kunt gebruiken, gesorteerd op categorieën, zie [Beschikbare rapporten in [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md).

Wanneer u een rapport kiest, ziet u meestal een aanvraagpagina&mdash;genoemd naar de naam van het rapport&mdash;, waarop u verschillende opties en filters kunt instellen die bepalen welke gegevens worden opgenomen. In de volgende secties wordt uitgelegd hoe u de aanvraagpagina gebruikt om een rapport te maken, te bekijken en af te drukken.

## <a name="SavedSettings"></a>Standaardwaarden gebruiken&mdash;vooraf gedefinieerde instellingen

De meeste aanvraagpagina's bevatten het veld **Standaardwaarden gebruiken uit**. Met dit veld kunt u vooraf gedefinieerde instellingen voor het rapport selecteren, waarmee automatisch opties en filters worden ingesteld. Selecteer een item in de vervolgkeuzelijst en u zult zien dat de opties en filters op de rapportaanvraagpagina dienovereenkomstig veranderen.

Het item genaamd **Laatst gebruikte opties en filters** is altijd beschikbaar. Dit item stelt het rapport in op de opties en filters die u gebruikte toen u het rapport voor de laatste keer uitvoerde.

Het veld **Standaardwaarden gebruiken uit** biedt een snelle en betrouwbare manier om consistent rapporten te genereren die de juiste gegevens bevatten. Nadat u een item hebt geselecteerd, kunt u de opties en filters wijzigen voordat u een voorbeeld bekijkt of het rapport afdrukt. De wijzigingen die u aanbrengt, worden niet opgeslagen in het item met vooraf gedefinieerde instellingen dat u hebt geselecteerd, maar worden wel opgeslagen in het item **Laatst gebruikte opties en filters**.

> [!NOTE]
> De vooraf gedefinieerde instellingen worden doorgaans ingesteld en beheerd door een beheerder. Meer informatie op [Opgeslagen instellingen beheren voor rapporten en batchtaken](reports-saving-reusing-settings.md).

## De gegevens opgeven die in rapporten moeten worden opgenomen

Gebruik de velden onder **Opties** en **Filters** om de informatie die u in het rapport wilt, te wijzigen of te beperken. U kunt filters in een rapport instellen op ongeveer dezelfde manier als filters in lijsten. Lees meer in de sectie [Filteren](ui-enter-criteria-filters.md#filtering).

> [!CAUTION]
> De sectie **Filteren** op een rapportaanvraagpagina biedt een algemene filtermogelijkheid voor rapporten. Deze filters zijn optioneel.
>
> Sommige rapporten negeren dergelijke filters, wat inhoudt dat het niet uitmaakt welk filter is ingesteld op het sneltabblad **Filteren**. De uitvoer van het rapport is hetzelfde. U kunt geen lijst opgeven met welke velden worden genegeerd in welke rapporten, dus u zult met de filters moeten experimenteren wanneer u deze gebruikt.
>
> **Voorbeeld**: wanneer u de batchverwerking **Aanmaningen maken** gebruikt, wordt het filter **Laatste verz. aanmaningsniveau** voor het veld **Klantenposten** genegeerd omdat filters voor die batchverwerking vast zijn.

## Een voorbeeld van een rapport bekijken

Als u een voorbeeld van een rapport bekijkt, kunt u zien hoe het rapport eruitziet voordat u het afdrukt. Het voorbeeld is niet gebaseerd op de geselecteerde printer in het veld **Printer** op de aanvraagpagina. Het wordt bestuurd door de browser. Nadat u een voorbeeld hebt bekeken, kunt u teruggaan naar de aanvraagpagina en indien nodig wijzigingen aanbrengen in opties en filters.

De voorbeeldopties op de pagina **Rapportaanvraag** zijn afhankelijk van het rapport. Dus voor sommige rapporten kunt u **Voorbeeld** kiezen, terwijl voor andere de keuze **Voorbeeld en sluiten** is. Beide keuzen openen een voorbeeld van het rapport. Het verschil is dat **Voorbeeld** de aanvraagpagina open houdt, zodat u ernaar kunt terugkeren, wijzigingen kunt aanbrengen, opnieuw een voorbeeld kunt bekijken of kunt afdrukken. Met **Voorbeeld en sluiten** wordt de aanvraagpagina daarentegen gesloten en moet u het rapport opnieuw openen om wijzigingen aan te brengen of af te drukken.

> [!NOTE]
> Als u Business Central 2020 releasewave 1 of eerder gebruikt, is de enige keuze **Voorbeeld**, waarmee de aanvraagpagina met het voorbeeld wordt gesloten, zoals hierboven beschreven voor **Voorbeeld en sluiten**.

### Werken met het voorbeeld

Gebruik in het rapportvoorbeeld de menubalk om het volgende te doen:

- Door pagina's bladeren
- In- en uitzoomen
- Het formaat aanpassen aan de afmetingen van de pagina
- Tekst selecteren

    U kunt tekst uit een rapport kopiëren en die vervolgens ergens anders plakken, zoals als op een pagina in [!INCLUDE[prod_short](includes/prod_short.md)] of Microsoft Word. Met bijvoorbeeld een muis houdt u de linkermuisknop ingedrukt waar u wilt beginnen. Veeg vervolgens met de muis om een of meer woorden, zinnen of alinea's te selecteren. Druk vervolgens op de rechtermuisknop en selecteer **Kopiëren**. U kunt de geselecteerde tekst nu op elke gewenste plek plakken.
- Document pannen

    U kunt het zichtbare deel van het rapport in iedere richting verplaatsen, zodat u andere delen van het rapport kunt bekijken. Pannen is handig als u hebt ingezoomd om details te zien. U kunt met de muis bijvoorbeeld de linkermuisknop ergens in het rapportvoorbeeld ingedrukt houden en vervolgens de muis verplaatsen om een deel van het rapport te selecteren.

- Downloaden naar een PDF-bestand op uw computer of netwerk.
- Afdrukken

## Een rapport opslaan in een bestand

U kunt een rapport opslaan als een PDF-document, een Microsoft Word-document, een Microsoft Excel-werkmap of een XML-document. Kies hiervoor **Verzenden naar** en maak uw keuze. Er wordt een bestand naar uw apparaat gedownload.

Als uw organisatie OneDrive heeft geconfigureerd voor systeemfuncties, worden Excel-werkmappen en Word-documenten niet gedownload, maar in uw browser geopend met Excel of Word voor het web.

> [!TIP]
> De opties **Microsoft Excel-document (alleen gegevens)** en **XML-document** zijn meestal voor geavanceerde doeleinden. Normaal gesproken gebruikt u deze opties voor het uitvoeren van gedetailleerde gegevensanalyses. Zie voor meer informatie [Rapportgegevens analyseren met Excel en XML](report-analyze-excel.md).
>
> U kunt ook **Microsoft Excel-document (alleen gegevens)** gebruiken om nieuwe Excel-indelingen voor een bepaald rapport te maken. Meer informatie op [Werken met Excel-indelingen](ui-excel-report-layouts.md).  

## <a name="ScheduleReport"></a> Een rapport plannen om het later of periodiek uit te voeren

U kunt een één rapport of een periodiek rapport plannen voor uitvoering op een bepaalde datum en tijd. Geplande rapporten worden in de verwerkingswachtrij ingevoerd en verwerkt op het geplande tijdstip, net zoals andere taken. Kies de optie **Schema** nadat u de knop **Verzenden naar** hebt gekozen en voer vervolgens informatie in zoals de printer en tijd en datum. Het rapport wordt vervolgens toegevoegd aan de taakwachtrij en wordt op de opgegeven tijd uitgevoerd. Als het rapport is verwerkt, wordt het artikel verwijderd uit de verwerkingswachtrij. Zie voor meer informatie [Taakwachtrijen gebruiken om taken te plannen](admin-job-queues-schedule-tasks.md).  

Wanneer u een rapport plant dat moet worden uitgevoerd, kunt u bijvoorbeeld opgeven dat het elke donderdag moet worden uitgevoerd door het veld **Formule voor volgende uitvoeringsdatum** in te stellen op *D4*. Lees meer in de sectie [Datumformules gebruiken](ui-enter-date-ranges.md#use-date-formulas).  

U kunt ervoor kiezen het rapport op te slaan in een bestand, zoals een Excel-, Word- of PDF-bestand, het af te drukken of het rapport alleen te genereren. Als u ervoor kiest het rapport in een bestand op te slaan, wordt het verwerkte rapport naar de pagina **Rapportinbox** in uw rolcentrum verzonden, waar u het kunt bekijken. Meer informatie op [Rapporten delen en exporteren met de Rapportinbox](ui-work-report-inbox.md)

### Geplande periodieke rapporten beheren

Geplande rapporten worden gegenereerd door batchtaken die worden beheerd op de pagina **Taakwachtrijposten**. U kunt de status en andere informatie voor elk rapport op de pagina zien, de rapportbatchtaak pauzeren/hervatten en het rapport op verzoek genereren.

Vanaf de pagina **Taakwachtrijposten** kunt u ook enkele rapportparameters wijzigen, zoals het type uitvoerbestand, de herhaling, de uitvoeringsdatum en begin- en eindtijden. Voordat u een bestaand gepland rapport bewerkt, is het echter noodzakelijk om de wachtrij voor rapporttaken in de wacht te zetten:

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Taakwachtrijposten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Taakwachtrijposten** het gewenste rapport.
3. Kies de actie **Instellen op afwachten**.
4. Open en bewerk het geplande rapport door de status te selecteren (*Afwachten*).

Herhaal na het bewerken van de rapportopties de eerste twee stappen en selecteer vervolgens de actie **Status instellen op Gereed** om het genereren van het rapport te hervatten.

Lees meer over taakwachtrijbeheer op [Taakwachtrijen gebruiken om taken te plannen](admin-job-queues-schedule-tasks.md).  

## <a name="PrintReport"></a>Een rapport afdrukken

Als u een rapport wilt afdrukken, kiest u de knop **Afdrukken** op de rapportaanvraagpagina of op de menubalk op de pagina **Voorbeeld**.

Wanneer een rapport een Excel-indeling gebruikt, ziet u niet het veld **Printer**, de knop **Afdrukken** of de knop **Voorbeeld**. In plaats daarvan is er een optie **Downloaden**. Om af te drukken, selecteert u **Downloaden**, vervolgens opent u het gedownloade bestand in Excel en drukt u van daaruit af.

### <a name="Printer"></a>Printer

Het veld **Printer** op de aanvraagpagina bevat de naam van de printer waar het rapport heen wordt gestuurd. Om een printer te wijzigen selecteert u de printer in de lijst.

> [!NOTE]
> De optie **(Afgehandeld door de browser)** geeft aan dat er geen aangewezen printer is voor het rapport. In dit geval zal de browser de afdruk afhandelen en de standaardafdrukstappen weergeven, waarbij u een lokale printer kunt kiezen die op uw apparaat is aangesloten. De optie **(Afgehandeld door de browser)** is niet beschikbaar in de mobiele [!INCLUDE[prod_short](includes/prod_short.md)]-app of de app voor Microsoft Teams.

> [!TIP]
> De printer die standaard voor u is geselecteerd, wordt ingesteld op de pagina **Printerselecties**. Lees meer over het wijzigen van de standaardprinter in de sectie [Standaardprinters instellen](ui-specify-printer-selection-reports.md#default).

### Rapporten afdrukken in Thai

Specifiek voor de Thaise versie van [!INCLUDE[prod_short](includes/prod_short.md)] kan de knop **Afdrukken** geen rapporten correct afdrukken vanwege beperkingen in de service die het afdrukbare PDF-bestand genereert. In plaats hiervan kunt u het rapport openen in Word en vervolgens opslaan als een afdrukbare PDF.  

U kunt ook de beheerder vragen een Word-rapportlay-out te maken voor uw meest gebruikte rapporten. Meer informatie op [Rapport- en documentlay-outs beheren](ui-manage-report-layouts.md).  

## Overgaan op een andere rapportlay-out

Een rapportlay-out bepaalt wat in een rapport wordt weergegeven, hoe het is ingedeeld en hoe het is opgemaakt. Er zijn een paar manieren om de lay-out te wijzigen:

- Wanneer u zich instelt om een rapport uit te voeren, ziet u de huidige lay-out in het veld **Rapportlay-out** op de aanvraagpagina. Om tijdelijk over te schakelen naar een andere lay-out, selecteert u het veld **Rapportlay-out** en kiest u vervolgens uit een lijst met beschikbare lay-outs voor het rapport.
- Om de standaardlay-out die door een rapport wordt gebruikt te wijzigen, gaat u naar de pagina **Rapportlay-outs** of **Selectie rapportlay-out**.

Meer informatie op [De lay-out instellen die door een rapport wordt gebruikt](ui-set-report-layout.md). Of zie [Aan de slag met het maken van lay-outs](ui-get-started-layouts.md) als u uw eigen rapportlay-out wilt aanpassen.

## Wijzig de taal en het formaat van getallen, datums en tijden

Standaard zijn de taal van de tekst en de notatie van getallen, datums en tijden in een rapport gebaseerd op uw werktaal- en regio-instellingen, die zijn gedefinieerd op de pagina **Mijn instellingen**. U kunt de taal en de indelingsregio echter van geval tot geval wijzigen wanneer u een voorbeeld bekijkt, afdrukt of een rapport verzendt. Selecteer **Geavanceerd** op de aanvraagpagina en stel vervolgens de opties voor **Taal** en **Notatieregio** naar wens in.

Ga voor meer informatie over de pagina **Mijn instellingen** naar [Basisinstellingen wijzigen](ui-change-basic-settings.md#region).

## Geavanceerde opties

De velden op het sneltabblad **Geavanceerd** stellen beperkingen in voor het gegenereerde rapport om printerbronnen te beheren. U hoeft deze instellingen doorgaans niet te wijzigen, tenzij u een groot rapport hebt. Als een rapport deze beperkingen overschrijdt wanneer u een voorbeeld probeert te bekijken of probeert af te drukken, verschijnt er een bericht waarin staat welke beperking u hebt overschreden. U kunt de instellingen vervolgens aanpassen aan uw rapport. Elk veld heeft echter een maximale waarde waarvan u op de hoogte moet zijn:

|Veld|Maximale waarde|
|-----|-------------|
|Maximale weergavetijd|12:00:00|
|Maximaal aantal rijen|1000000|
|Maximaal aantal documenten|500|

> [!NOTE]
> De maximale waarden kunnen verschillen voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises en een beheerder kan ze wijzigen. Zie de sectie [Business Central Server configureren: rapporten](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#Reports) voor meer informatie. Voor een overzicht van rapportbeperkingen in [!INCLUDE[prod_short](includes/prod_short.md)] online, raadpleegt u [Operationele limieten](/dynamics365/business-central/dev-itpro/administration/operational-limits-online).

## Zie ook

[Beschikbare rapporten [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
[Rapporten gebruiken in het dagelijkse werk](reports-use-reports.md)  
[Overzicht van bedrijfsinformatie en rapportage](reports-bi-reporting.md)  
[Printers instellen](ui-specify-printer-selection-reports.md)  
[Batchtaken en XMLports uitvoeren](ui-how-run-batch-jobs.md)  
[Werken met agendadatums en -tijden](ui-enter-date-ranges.md)  
[Rapport- en documentlay-outs beheren](ui-manage-report-layouts.md)  
[Financiële bedrijfsinformatie](bi.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
