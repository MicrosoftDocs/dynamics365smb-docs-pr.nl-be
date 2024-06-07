---
title: Gegevens delen
description: Meer informatie over de verschillende manieren om zakelijke gegevens te delen vanuit Business Central.
author: jswymer
ms.topic: conceptual
ms.search.keywords: null
ms.date: 09/21/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Zakelijke gegevens delen vanuit Business Central

Samenwerking tussen mensen binnen en buiten een organisatie is een integraal onderdeel van de meeste bedrijven. [!INCLUDE[prod_short](includes/prod_short.md)] biedt verschillende functies voor het delen van zakelijke gegevens, zoals een lijst met records, specifieke records of documenten. <!--, with others&mdash;even those people who don't have a Business Central license in some cases.-->

Bij al deze functies wordt de toegang tot gegevens beschermd door de licentie en machtigingen van Business Central.

## Een koppeling kopiëren

![Ondersteund](media/check.png) Business Central Online ![Ondersteund](media/check.png) Business Central On-premises

Vanaf elke pagina kunt u de URL van de pagina kopiëren en plakken en verspreiden in andere media, zoals e-mails, Teams-chats of sms-berichten. De gemakkelijkste manier om een koppeling te kopiëren is door **Delen** > **Koppeling kopiëren** te selecteren boven aan de pagina. Een andere manier is om de URL rechtstreeks vanuit het adresvak van de browser te kopiëren.

Wanneer u de URL in een rich-text-editor, zoals Word, Outlook of Teams, plakt, in plaats van de volledige URL weer te geven, krijgt de koppeling een beter leesbare naam die duidelijk de context van het doel aangeeft. De naam en het patroon variëren afhankelijk van de pagina waarnaar u koppelt. Bekijk de volgende voorbeelden:

|Patroon|Paginavoorbeeld|Koppelingsnaam|
|-|-|-|
|Lijstpagina's|Lijstpagina **Artikelen** | **Artikelen**|
|Lijstweergave| **Open** gefilterde weergave op lijst **Verkooporders**|**Verkooporders - Open**|
| Enkel record|Artikelkaart met één record|"Artikelkaart - 1896 ∙ ATHENE Bureau"|
|Conceptrecords| Nieuwe klantenkaart|**Nieuwe klantenkaart**|
|Bedrijf dat badge gebruikt|Lijstpagina **Artikelen** voor bedrijf met badge **CRONUS**| **Artikelen (CRONUS)**|

> [!TIP]
> Een soortgelijke naamgevingsconventie wordt gebruikt op browsertabbladen.

### Gegevensanalyse delen
Als u een pagina of zoekopdracht bekijkt in de gegevensanalysemodus, kunt u een specifiek analysetabblad delen door de pijl-omlaag op het tabblad te selecteren en vervolgens **Koppeling kopiëren** te selecteren. [Meer informatie over de gegevensanalysemodus](analysis-mode.md). 

### De paginakoppeling wijzigen

Nadat u een koppeling hebt gekopieerd, kunt u voordat u deze verzendt de URL wijzigen om te bewerken wat wordt weergegeven wanneer de pagina wordt geopend. U kunt bijvoorbeeld filters toevoegen of een ander bedrijf opgeven.

[Meer informatie over de URL van de webclient](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls).

### Over gefilterde lijsten

Met behulp van het filtervenster op lijstpagina's kunt u filters toepassen om de records in de lijst te verfijnen. Als u de actie **Koppeling kopiëren** gebruikt of de URL vanuit de browser kopieert, bevat de paginakoppeling uw filterwijzigingen niet. Gebruikers die de koppeling openen, zien de volledige verzameling. De manier om de filtering op een koppeling voor een verzamelingspagina te behouden, is door de gefilterde pagina eerst op te slaan als **weergave**. Open vervolgens de weergave en kopieer de koppeling daar vandaan.

[Meer informatie over sorteren, zoeken en filteren](ui-enter-criteria-filters.md).

## Delen met Teams

![Ondersteund](media/check.png) Business Central Online ![Niet ondersteund](media/x-icon.png) Business Central On-premises

Rechtstreeks vanaf de meeste verzamelingspagina's en detailpagina's kunt u een koppeling naar de pagina verzenden naar personen, groepschats of kanalen. Deel bijvoorbeeld een koppeling naar een gefilterde weergave van uw records. Als u de [!INCLUDE[prod_short](includes/prod_short.md)]-app voor Teams hebt geïnstalleerd, wordt de koppeling automatisch uitgevouwen tot een compacte kaart die u bij uw bericht kunt voegen. Ontvangers selecteren vervolgens de koppeling of de kaart om de pagina te openen in Business Central.

[Meer informatie over het delen van records en paginakoppelingen in Teams](across-working-with-teams.md).

## Delen via OneDrive

![Ondersteund](media/check.png) Business Central Online ![Ondersteund](media/check.png) Business Central On-premises

Business Central maakt het gemakkelijk om bestanden op te slaan, te beheren en te delen met andere mensen via OneDrive voor Bedrijven. Op de meeste pagina's waar bestanden beschikbaar zijn, zoals de Rapportinbox of bestanden die aan records zijn toegevoegd, vindt u de acties **Openen in OneDrive** en **Delen**. Beide acties slaan een kopie van een bestand op naar OneDrive. Eenmaal in OneDrive, kunt u de functies voor delen en bijdragen gebruiken voor het bestand. Het verschil in de acties is dat **Openen in OneDrive** het bestand opent in OneDrive. **Delen** opent een pagina waar u kunt selecteren met wie u het bestand wilt delen. Ontvangers ontvangen een e-mailmelding om toegang te krijgen tot het bestand vanuit uw OneDrive.

[Lees meer over het delen van bestanden in OneDrive](across-share-onedrive.md).

## Openen in Excel

![Ondersteund](media/check.png) Business Central Online ![Ondersteund](media/check.png) Business Central On-premises

Voor lijstpagina's en lijsten die op een pagina zijn ingesloten, kunt u de actie **Openen in Excel** gebruiken. Met deze actie wordt de lijst met records naar een Excel-werkmap (.xlsx-bestand) geëxporteerd, die u met anderen kunt delen. In de werkmap kunt u ook de functie Delen gebruiken die deel uitmaakt van Excel.

[Meer informatie over bekijken en bewerken in Excel](across-work-with-excel.md).

## Rijen of tabellen delen

![Ondersteund](media/check.png) Business Central Online ![Ondersteund](media/check.png) Business Central On-premises

U kunt een of meer records in een lijst delen. Selecteer simpelweg de sneltoetscombinatie <kbd>Ctrl</kbd>+<kbd>C</kbd> om naar uw klembord te kopiëren. Plak vervolgens wat u hebt gekopieerd in een andere toepassing door op <kbd>Ctrl</kbd>+<kbd>V</kbd> te drukken. Als u bijvoorbeeld drie verkooporders kopieert en in een e-mail plakt, worden de orders weergegeven in een fraai opgemaakte tabel.

[Meer informatie over kopiëren en plakken vindt u in de FAQ](faq-copy-paste.yml).

## Zie ook

[Integratie van Business Central en OneDrive](across-onedrive-overview.md)  
[OneDrive-integratie met Business Central beheren](admin-onedrive-integration.md)  
[Veelgestelde vragen over OneDrive](admin-onedrive-faq.md)
