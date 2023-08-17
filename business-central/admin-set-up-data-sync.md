---
title: Bedrijven instellen om hoofdgegevens te synchroniseren
description: Leer hoe u een of meer bedrijven kunt instellen om hoofdgegevens te synchroniseren.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---

# <a name="get-ready-to-synchronize-master-data"></a>Voorbereiden op het synchroniseren van hoofdgegevens

Wanneer twee of meer bedrijven enkele van dezelfde hoofdgegevens gebruiken, kunt u de gegevens synchroniseren in plaats van deze handmatig in elk bedrijf toe te voegen. Het synchroniseren van gegevens is bijvoorbeeld handig wanneer u nieuwe dochterondernemingen instelt.

Hoofdgegevens omvatten instellingen en niet-transactionele informatie over bedrijfsentiteiten. Bijvoorbeeld klanten, leveranciers, artikelen en werknemers. De gegevens bieden context voor zakelijke transacties. Hieronder volgen enkele voorbeelden van hoofdgegevens voor een klant:

* Name
* Identificatienummer
* Adres
* Betalingsvoorwaarden
* Kredietlimiet

U stelt synchronisatie in de dochterondernemingen in. Met behulp van een pull-model halen dochterondernemingen de gegevens op van het bronbedrijf die ze nodig hebben om zaken met hen te doen. Nadat u synchronisatie hebt ingesteld en gegevens voor de eerste keer hebt gesynchroniseerd, bent u helemaal klaar. Taakwachtrij-items werken gekoppelde records in de dochterondernemingen bij wanneer iemand gegevens wijzigt in het bronbedrijf.

## <a name="uni-directional-synchronization-only"></a>Alleen unidirectionele synchronisatie

U kunt alleen gegevens van het bronbedrijf naar de dochterondernemingen op een pull-manier synchroniseren. Dochterondernemingen kunnen geen gegevens naar het bronbedrijf pushen.

> [!NOTE]
> Hoewel het mogelijk is, raden we u niet aan bidirectionele synchronisatie in te stellen. Dat wil zeggen, het synchroniseren van gegevens van het bronbedrijf naar de dochterondernemingen en van de dochterondernemingen naar het bronbedrijf. Het synchroniseren van gegevens in beide richtingen kan leiden tot conflicten of ongewenste overschrijvingen.

## <a name="before-you-start"></a>Voordat u begint

Dit zijn vereisten voor het instellen van synchronisatie.

* Alle bedrijven moeten zich in dezelfde omgeving bevinden.
* De gebruiker die de dochteronderneming opzet, moet beschikken over de licentie **Essential**, **Premium** of **Basic ISV**.

> [!NOTE]
> Met de Teamlid- en Interne beheerder-licentie kunt u records openen, maar niet wijzigen, en deze licenties kunnen dus niet worden gebruikt om de synchronisatie in te stellen. Met de licentie voor gedelegeerde beheerders kunt u geen achtergrondtaken plannen, dus u kunt de installatie niet voltooien.

## <a name="specify-the-source-company"></a>Het bronbedrijf opgeven

De eerste stappen zijn het specificeren van het bedrijf dat de gegevensbron zal zijn en het inschakelen van synchronisatie. Dochterondernemingen halen gegevens uit het bronbedrijf.

> [!NOTE]
> Wanneer u synchronisatie inschakelt, maakt en plant [!INCLUDE [prod_short](includes/prod_short.md)] de taakwachtrij-items die de gegevens synchroniseren. Het lijkt misschien alsof de items de gegevens onmiddellijk synchroniseren, maar dat is niet het geval. De gemaakte taakwachtrij-items synchroniseren alleen gekoppelde records en op dit moment hebt u dat nog niet ingesteld. De synchronisatie begint nadat u [alle tabellen en velden in- of uitschakelt](#enable-or-disable-tables-and-fields) en [voor de eerste keer synchroniseert](#synchronize-for-the-first-time).

1. Kies in een dochteronderneming het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instelling van Hoofdgegevensbeheer** in en kies vervolgens de gerelateerde koppeling.
1. Geef in het veld **Bronbedrijf** het bedrijf op waarvan u wijzigingen wilt ophalen.
1. Zet de schakelaar **Synchronisatie inschakelen** aan.
1. Kies in het bevestigingsdialoogvenster **OK**. [!INCLUDE [prod_short](includes/prod_short.md)] vindt de tabellen en velden die beschikbaar zijn bij het bronbedrijf.

De volgende stap is het inschakelen van tabellen en velden voor synchronisatie.

## <a name="enable-or-disable-tables-and-fields"></a>Tabellen en velden in- of uitschakelen

[!INCLUDE [prod_short](includes/prod_short.md)] biedt een lijst met tabellen die bedrijven vaak synchroniseren om tijd te besparen. Deze tabellen zijn standaard ingeschakeld voor synchronisatie. U kunt ze naar eigen inzicht aanpassen, uitschakelen of verwijderen. Als extra tijdsbesparing zijn sommige velden in de tabellen al uitgeschakeld omdat ze waarschijnlijk niet relevant zijn voor de dochteronderneming.

> [!NOTE]
> Als een of meer extensies zijn geïnstalleerd in het bronbedrijf en een dochteronderneming synchronisatie instelt, bevat de pagina **Synchronisatietabellen** tabellen van de extensies en hebt u toegang tot hun velden. Als het bronbedrijf echter een extensie toevoegt nadat de synchronisatie is ingesteld, moet elke dochteronderneming de tabellen handmatig toevoegen. Ga voor meer informatie over het toevoegen van tabellen naar [Tabellen toevoegen aan of verwijderen uit de lijst met synchronisatietabellen](#add-or-delete-tables-from-the-synchronization-tables-list). Ga voor meer informatie over verlengen van [!INCLUDE [prod_short](includes/prod_short.md)] naar [Extensies ontwikkelen in Visual Studio Code](/dynamics365/business-central/dev-itpro/developer/devenv-dev-overview#developing-extensions-in-visual-studio-code).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instelling van Hoofdgegevensbeheer** in en kies vervolgens de gerelateerde koppeling.
1. Kies de actie **Synchronisatietabellen**.
1. Vul de vereiste velden in. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Het veld **Tabelfilter** is handig om te bepalen wat er moet worden gesynchroniseerd voor een tabel. U kunt filters instellen om alleen te synchroniseren wanneer aan bepaalde voorwaarden is voldaan. U kunt bijvoorbeeld filters toevoegen die specificeren dat u alleen leveranciers in een bepaalde regio synchroniseert. Of klanten die een bepaalde valuta gebruiken.
>
> Als de dochteronderneming al gegevens in hun tabellen heeft staan, is een andere goede manier om criteria voor synchronisatie in te stellen het instellen van op overeenkomsten gebaseerde koppeling. Ga voor meer informatie over koppeling naar [Op match gebaseerde koppeling gebruiken](#use-match-based-coupling).

1. Om velden voor een tabel in te schakelen kiest u de tabel en kiest u vervolgens de actie **Velden**.
1. Vul de vereiste velden in. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Een snelle manier om meerdere velden tegelijkertijd in of uit te schakelen, is door ze in de lijst te selecteren en vervolgens de actie **Inschakelen** of **Uitschakelen** te gebruiken.

### <a name="use-match-based-coupling"></a>Koppeling op basis van overeenkomsten gebruiken

U kunt specificeren welke gegevens voor een tabel moeten worden gesynchroniseerd door records te koppelen op basis van criteria. Kies op de pagina **Instelling van Hoofdgegevensbeheer** de actie **Op overeenkomsten gebaseerde koppeling** om de pagina **Koppelingscriteria selecteren** te openen. U kunt de volgende criteria definiëren voor uw koppeling:

* Of u wilt synchroniseren nadat u records hebt gekoppeld.
* Of u een nieuwe record wilt maken in de dochteronderneming als er geen unieke niet-gekoppelde overeenkomst kan worden gevonden met behulp van de overeenkomstcriteria. Om deze mogelijkheid te activeren schakelt u de actie **Nieuw maken als geen overeenkomst is gevonden** in.
* De velden die moeten worden gebruikt om records te koppelen en of de koppeling hoofdlettergevoelig is.
* Geef prioriteit aan de volgorde waarin records worden doorzocht door een overeenkomstprioriteit op te geven. [!INCLUDE [prod_short](includes/prod_short.md)] zal zoeken naar een overeenkomst in oplopende volgorde op basis van de overeenkomstprioriteit. Een blanco waarde staat gelijk aan prioriteit 0, wat de hoogste prioriteit is. Velden met prioriteit 0 worden als eerste in overweging genomen.

## <a name="synchronize-for-the-first-time"></a>Voor de eerste keer synchroniseren

Wanneer u klaar bent, kiest u op de pagina **Instelling van Hoofdgegevensbeheer** de actie **Initiële synchronisatie starten**. Kies op de pagina **Initiële synchronisatie van hoofdgegevens** het type synchronisatie dat u voor elke tabel wilt gebruiken.

* Als u al records hebt in zowel de bron- als de dochterondernemingen en u bestaande records wilt koppelen, kiest u de actie **Koppeling op basis van overeenkomsten gebruiken**. [!INCLUDE [prod_short](includes/prod_short.md)] stemt records in het dochteronderneming af met records in het bronbedrijf. De overeenkomsten zijn gebaseerd op overeenkomstencriteria die u definieert. Voor verschillende standaardtabellen heeft [!INCLUDE [prod_short](includes/prod_short.md)] al bestaande records gekoppeld door hun primaire sleutel te gebruiken, maar u kunt dat desgewenst wijzigen. U kunt de synchronisatie ook nieuwe records laten maken in de dochteronderneming voor records in het bronbedrijf die de dochteronderneming niet heeft. Ga voor meer informatie over koppeling naar [Op match gebaseerde koppeling gebruiken](#use-match-based-coupling).
* Als u **Volledige synchronisatie uitvoeren** kiest, maakt de synchronisatie nieuwe records voor alle records in het bronbedrijf die nog niet gekoppeld zijn. Deze optie is bijvoorbeeld handig in de volgende scenario's:

    * De dochteronderneming heeft geen gegevens in de tabel.
    * U wilt records van het bronbedrijf toevoegen zonder af te stemmen.  

Nadat u de optie hebt gekozen die u wilt gebruiken, kiest u de actie **Alles starten** om de synchronisatie te starten.

Terwijl de synchronisatie bezig is, toont de kolom **Taakstatus** op de pagina **Eerste volledige synchronisatie van hoofdgegevens** de status van elk taakwachtrij-item. Druk op **F5** op uw toetsenbord om de status bij te werken.

> [!TIP]
> Tabellen synchroniseren in een vooraf gedefinieerde volgorde. Als de synchronisatie vastloopt op een tabel, selecteert u de tabel en kiest u vervolgens de actie **Opnieuw starten** om de synchronisatie weer op gang te krijgen.

Voor toegang tot details, zoals het aantal records dat is ingevoegd of gewijzigd, kiest u de waarde in de kolom **Taakstatus** om de pagina **Weergeven - Synchronisatietaken voor integratie** te openen. Voor records die zijn ingevoegd, kunt u het nummer kiezen in de kolom **Ingevoegd** voor meer informatie over de nieuwe records.

## <a name="add-or-delete-tables-from-the-synchronization-tables-list"></a>Tabellen toevoegen aan of verwijderen uit de lijst met synchronisatietabellen

### <a name="add-a-table"></a>Een tabel toevoegen

> [!IMPORTANT]
> Hoewel tabellen met transactiegegevens beschikbaar zijn in de lijst, zoals tabellen met grootboekposten, moet u deze niet kiezen. Synchronisatie werkt alleen voor tabellen die niet-transactionele gegevens bevatten.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Synchronisatietabellen** in en kies vervolgens de gerelateerde koppeling.
1. Kies **Nieuw** en kies vervolgens de toe te voegen tabel.
1. Vul de vereiste velden in. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

### <a name="delete-a-table"></a>Een tabel verwijderen

> [!NOTE]
> Als u een record verwijdert in het bronbedrijf, wordt deze niet ook verwijderd in de dochteronderneming. Dit helpt ongewenst verlies van gegevens te voorkomen. De dochteronderneming kan desgewenst besluiten de tabel te verwijderen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Synchronisatietabellen** in en kies vervolgens de gerelateerde koppeling.
1. Kies de actie **Verwijderen**.

## <a name="use-export-and-import-to-share-a-synchronization-setup"></a>Exporteren en importeren gebruiken om een synchronisatie-instelling te delen

Als u meerdere dochterondernemingen instelt die dezelfde of vergelijkbare synchronisatie-instellingen gebruiken, kunt u tijd besparen. Stel één dochteronderneming in en exporteer de instellingen vervolgens naar een .xml-bestand. Het bestand bevat de volledige instelling, inclusief tabel- en veldtoewijzingen en filtercriteria. U kunt het bestand vervolgens importeren in de volgende dochteronderneming. Om een instelling te importeren of exporteren, gebruikt u op de pagina **Instelling van Hoofdgegevensbeheer** de actie **Importeren** of **Exporteren**.

## <a name="see-also"></a>Zie ook

[Synchronisatie van hoofdgegevens beheren](admin-sync-master-data.md)
