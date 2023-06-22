---
title: Gegevens analyseren op lijstpagina's met behulp van de gegevensanalysemodus
description: Leer hoe u de gegevensanalysemodus in Business Central gebruikt om gegevens te analyseren.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/30/2023
ms.custom: bap-template
ms.service: dynamics365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# <a name="analyze-list-data-using-data-analysis-mode" />Gegevens analyseren op lijstpagina's met behulp van de gegevensanalysemodus

In dit artikel leert u hoe u gegevens vanaf lijstpagina's analyseert met behulp van de *gegevensanalysemodus*. Met de gegevensanalysemodus kunt u gegevens rechtstreeks vanaf de pagina analyseren, zonder dat u een rapport hoeft uit te voeren of naar een andere toepassing zoals Excel hoeft te schakelen. Het biedt een interactieve en veelzijdige manier om gegevens te berekenen, samen te vatten en te onderzoeken. In plaats van rapporten uit te voeren met verschillende opties en filters, kunt u meerdere tabbladen toevoegen die verschillende taken of weergaven van de gegevens vertegenwoordigen. Voorbeelden kunnen zijn "Mijn klanten", "Opvolgitems", "Onlangs toegevoegde leveranciers", "Verkoopstatistieken" of elke andere weergave die u maar kunt bedenken.

> [!TIP]
> Een goede zaak van de gegevensanalysemodus is dat het geen van de onderliggende gegevens van de lijstpagina of de lay-out van de pagina verandert wanneer deze zich niet in de gegevensanalysemodus bevindt. Dus de beste manier om te leren wat u kunt doen in de gegevensanalysemodus, is door dingen uit te proberen.

## <a name="prerequisite" />Vereiste

De gegevensanalysemodus is momenteel in preview, wat betekent dat een beheerder deze moet inschakelen voordat u deze kunt gebruiken. Als u een beheerder bent en u de gegevensanalysemodus wilt inschakelen, gaat u naar de pagina **Functiebeheer** en schakelt u **Functie-update: Analysemodus, snel gegevens rechtstreeks in Business Central analyseren** in. Ga voor meer informatie over het in- en uitschakelen van functies naar [Functiebeheer](/dynamics365/business-central/dev-itpro/administration/feature-management).

## <a name="get-started" />Aan de slag

1. Open de lijstpagina.

   Als u bijvoorbeeld wilt werken met **Klantenposten**, selecteert u het pictogram ![vergrootglas dat de functie Vertel me opent](media/ui-search/search_small.png) (<kbd>Alt</kbd>+<kbd>Q</kbd>), voert u *klantenposten* in en kiest u vervolgens de gerelateerde koppeling.  
2. Zet op de actiebalk boven aan de pagina de schakelaar **Analyseren** aan.

    De gegevensanalysemodus opent de gegevens in een ervaring die is geoptimaliseerd voor gegevensanalyse.  In de gegevensanalysemodus wordt de normale actiebalk vervangen door een speciale gegevensanalysebalk. De volgende afbeelding illustreert de verschillende gebieden van een pagina in de gegevensanalysemodus.

   [![Toont een overzicht van een pagina in de gegevensanalysemodus](media/analysis-mode-overview-2.png)](media/analysis-mode-overview-2.png#lightbox)

   Elk gebied wordt in de volgende secties uitgelegd.

3. Gebruik de verschillende gebieden om gegevens te manipuleren, samen te vatten en te analyseren. Zie de volgende secties voor meer informatie.

4. Als u de analysemodus wilt verlaten, schakelt u de schakelaar **Analyseren** uit.

   De analysetabbladen die u hebt toegevoegd, blijven staan totdat u ze verwijdert. Dus als u weer terugkeert naar de gegevensanalysemodus, ziet u ze precies zoals u ze achterliet.

> [!NOTE]
> De gegevens die in de analysemodus worden weergegeven, worden beheerd door de filters of weergaven die op de lijstpagina zijn ingesteld. Hierdoor kunt u gegevens vooraf filteren voordat u naar de analysemodus gaat.

## <a name="work-with-data-analysis-mode" />Werken met de gegevensanalysemodus

In de gegevensanalysemodus is de pagina verdeeld in twee gebieden:

- Het hoofdgebied, dat bestaat uit het gegevensgebied (1), overzichtsbalk (2) en tabbladenbalk (5)
- Het gebied voor gegevensmanipulatie, dat bestaat uit twee deelvensters: kolommen (3) en analysefilters (4).

### <a name="data-area-" />Gegevensgebied (1)

In het gegevensgebied worden de rijen en kolommen van de lijstpagina weergegeven en worden de gegevens samengevat. Het gegevensgebied biedt een veelzijdige manier om de lay-out van kolommen te regelen en een snelle manier om een samenvatting van de gegevens te krijgen. Voor kolommen die numerieke waarden bevatten, wordt de som van alle waarden in de kolom weergegeven in een laatste rij, tenzij u rijgroepen hebt gedefinieerd. In dit geval verschijnen de sommen als een subtotaal voor de groepen.  

![Toont een overzicht van een gegevensgebied op een pagina in de gegevensanalysemodus](media/analysis-mode-data-area.png)

- Als u een kolom wilt verplaatsen, selecteert u deze en sleept u deze naar de plaats waar deze het meest logisch is in uw analyse.
- Klik met de rechtermuisknop op de kolom of plaats de muisaanwijzer erop en selecteer het menupictogram ![Toont het pictogram op een kolom in de gegevensanalysemodus waarmee een menu met acties wordt geopend](media/analysis-mode-column-menu-icon.png) om toegang te krijgen tot verschillende acties die u op kolommen kunt uitvoeren. Voorbeeld:

  - Als u een kolom links of rechts van het gegevensgebied wilt vastzetten zodat deze niet van het scherm af beweegt wanneer u schuift, selecteert u ![Toont het pictogram op een kolom in de gegevensanalysemodus waarmee een menu met acties wordt geopend](media/analysis-mode-column-menu-icon.png) > **Kolom vastmaken** > **Links vastmaken** het kolomgedeelte.
  - Definieer gegevensfilters rechtstreeks op de kolomdefinitie in plaats van naar de **Analysefilters**-deelvensters te gaan. U kunt nog steeds details bekijken over gerelateerde gegevens en voor elke regel, en de kaart openen voor meer informatie over een bepaalde entiteit.
- Gebruik het gegevensgebied om met de gegevens te werken. Voor kolommen die numerieke, optelbare waarden bevatten, kunt u beschrijvende statistieken voor een reeks velden verkrijgen door ze te markeren. De statistieken verschijnen in de statusbalk (2) onder aan de pagina.
- Exporteer gegevens in Excel- of csv-indeling. Klik met de rechtermuisknop op het gegevensgebied of een selectie van cellen om te exporteren.

### <a name="summary-bar-" />Overzichtsbalk (2)

De overzichtsbalk bevindt zich onder aan de pagina en geeft statistieken weer over de gegevens in de lijst. Terwijl u werkt met kolommen waarvan de waarden kunnen worden opgeteld, zoals het selecteren van meerdere rijen in een kolom die bedragen bevat, worden de gegevens bijgewerkt.

![Toont een overzicht van een overzichtsbalk in de gegevensanalysemodus](media/analysis-mode-totals-row.png)

De volgende tabel beschrijft de verschillende getallen die worden weergegeven in het totalengebied:

|Nummer|Omschrijving|
|-|-|
|Rijen|Het aantal geselecteerde rijen als onderdeel van het totale aantal beschikbare rijen. |
|Totaal aantal rijen|Het aantal rijen in de ongefilterde lijst.|
|Gefilterd|Het aantal rijen dat wordt weergegeven als resultaat van de filters die op de lijst zijn toegepast.|
|Gemiddelde|De gemiddelde waarde in alle geselecteerde optelbare velden.|
|Aantal|Het aantal geselecteerde rijen.|
|Min|De minimale waarde in alle geselecteerde optelbare velden.|
|Max|De maximale waarde in alle geselecteerde optelbare velden.|
|Som|Het totaal van alle waarden in de geselecteerde optelbare velden.|

### <a name="columns-" />Kolommen (3)

**Kolommen** is een van de twee deelvensters die samenwerken om uw analyse te definiëren. Het andere gebied is het deelvenster **Analysefilters**. Het deelvenster **Kolommen** wordt gebruikt om de gegevens samen te vatten. Gebruik het deelvenster **Kolommen** om te definiëren welke kolommen in de analyse moeten worden opgenomen.

![Toont een overzicht van het kolommendeelvenster in de gegevensanalysemodus](media/analysis-mode-columns-2.png)

|Districten|Omschrijving|
|-|-|
|Zoeken/alle vakjes in- of uitschakelen|Zoeken naar kolommen. Schakel het selectievakje in om alle kolommen te selecteren/wissen.|
|Selectievakjes|Dit gebied bevat een selectievakje voor elk veld in de brontabel van de lijst. Gebruik dit gebied om te wijzigen welke kolommen in de lijst worden weergegeven. Schakel een selectievakje in om de kolom voor het veld op de pagina weer te geven; schakel het selectievakje uit om de kolom te verbergen. |
|Rijgroepen|Gebruik dit gebied om gegevens te groeperen en op te tellen op een of meer velden. U kunt alleen niet-numerieke velden opnemen, zoals tekst-, datum- en tijdvelden. Rijgroepen worden vaak gebruikt in de draaimodus.|
|Waarden|Gebruik dit gebied om velden op te geven waarvoor u een totaal wilt hebben. U kunt alleen velden opnemen die getallen bevatten die bij elkaar kunnen worden opgeteld; bijvoorbeeld geen tekst-, datum- of tijdvelden.|

Selecteer het grijppictogram om een veld van het ene gebied naar het andere te verplaatsen ![Toont een overzicht van een pagina in de analysemodus](media/column-grab-icon.png) naast de kolom in de bovenstaande lijst en sleep naar het doelgebied. U mag een veld niet verplaatsen naar een gebied waar het niet is toegestaan.

### <a name="analysis-filters-" />Analysefilters (4)

Met het deelvenster **Analysefilters** kunt u verdere gegevensfilters op kolommen instellen om de vermeldingen in de lijst te beperken. Stel filters in op kolommen om de vermeldingen in de lijst en de daaropvolgende sommen te beperken tot alleen die vermeldingen waarin u bent geïnteresseerd op basis van een criterium dat u definieert. Stel dat u alleen geïnteresseerd bent in gegevens van een specifieke klant of verkooporders die een bepaald bedrag overschrijden. Om een filter in te stellen selecteert u de kolom, kiest u de vergelijkingsbewerking uit de lijst (zoals **Is gelijk aan** of **Begint met**) en voert u de waarde in.

![Toont een overzicht van het filterdeelvenster in de analysemodus](media/analysis-mode-filters.png)

> [!NOTE]
> De extra filters zijn alleen van toepassing op het huidige analysetabblad. Hierdoor kunt u precies de extra datafilters definiëren die nodig zijn voor een specifieke analyse.

### <a name="tabs-" />Tabbladen (5)

In het tabbladengebied bovenaan kunt u verschillende configuraties (kolommen en analysefilters) maken op afzonderlijke tabbladen, waar u gegevens op de tabbladen onafhankelijk van elkaar kunt manipuleren. Er is altijd minimaal één tabblad, standaard genaamd **Analyse 1** . Het toevoegen van meer tabbladen is gunstig voor het opslaan van veelgebruikte analyseconfiguraties op een gegevensset. U kunt bijvoorbeeld tabbladen hebben voor het analyseren van gegevens in de draaimodus en andere tabbladen die filteren op een subset van rijen. Sommige tabbladen tonen mogelijk een gedetailleerde weergave met veel kolommen en andere geven slechts enkele sleutelkolommen weer.

Hier volgen enkele tips voor het werken met meerdere analysetabbladen:

- Selecteer het grote **+**-teken naast het laatste analysetabblad om een nieuw tabblad toe te voegen.
- Selecteer de pijl-omlaag op een tabblad om toegang te krijgen tot een lijst met acties die u op een tabblad kunt uitvoeren, zoals hernoemen, dupliceren, verwijderen en verplaatsen.

   - **Verwijderen** verwijdert het tabblad dat u momenteel hebt geopend. **Alles verwijderen** verwijdert alle tabbladen die u hebt toegevoegd, behalve het standaardtabblad **Analyse 1**.
- U kunt **Analyse 1** niet volledig verwijderen, maar u kunt de naam wel wijzigen met de actie **Hernoemen** en de wijzigingen wissen die u hebt aangebracht met behulp van **Verwijderen** of **Alles verwijderen**.  

- De analysetabbladen die u hebt toegevoegd en geconfigureerd, blijven staan totdat u ze verwijdert. Dus als u weer terugkeert naar de gegevensanalysemodus, ziet u ze precies zoals u ze achterliet.

   > [!TIP]
   > De tabbladen die u instelt, zijn alleen voor u zichtbaar. Andere gebruikers zien alleen tabbladen die ze hebben ingesteld.
- U kunt analysetabbladen kopiëren. Kopiëren kan handig zijn als u wilt experimenteren met het wijzigen van een tabblad zonder het origineel te wijzigen, of als u verschillende varianten van dezelfde analyse wilt maken.

## <a name="pivot-mode" />Draaimodus

U kunt de draaimodus gebruiken om grote hoeveelheden numerieke gegevens te analyseren, waarbij gegevens worden opgeteld op categorieën en subcategorieën. De draaimodus is vergelijkbaar met [draaitabellen in Microsoft Excel](https://support.microsoft.com/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576).

Om de draaimodus in en uit te schakelen verschuift u de schakelaar **Draaimodus** in het deelvenster **Kolommen** (3). Wanneer u de draaimodus inschakelt, verschijnt het gebied **Kolomlabels** in het deelvenster. Gebruik het gebied **Kolomlabels** om somtotalen voor rijen in categorieën te groeperen. Velden die u toevoegt aan het gebied **Kolomlabels** worden weergegeven als kolommen in het gegevensgebied (1).

Het opbouwen van de gegevensanalyse in de draaimodus omvat het verplaatsen van velden naar de drie gebieden: **Rijgroepen**, **Kolomlabels** en **Waarden**. De volgende afbeelding illustreert waar de velden worden toegewezen aan het gegevensgebied (1), waarbij `sum` de berekende gegevens zijn en optioneel **Waarden**.

<table>
<tr><th></th><th>Kolomlabel</th><th></th><th>Kolomlabel</th><th></th></tr>
<tr><th>Rijgroep</th><th>Waarde</th><th>Waarde</th><th>Waarde</th><th>Waarde</th></tr>
<tr><td>rij</td><td>som</td><td>som</td><td>som</td><td>som</td></tr>
<tr><td>rij</td><td>som</td><td>som</td><td>som</td><td>som</td></tr>
<tr><td>rij</td><td>som</td><td>som</td><td>som</td><td>som</td></tr>
<tr><td>rij</td><td>som</td><td>som</td><td>som</td><td>som</td></tr>
</table>

> [!TIP]
> Kolommen die maar een paar mogelijke waarden hebben, zijn de beste kandidaten voor gebruik in de kolom **Waarden**.

## <a name="limitations" />Beperkingen

De analyseweergave heeft momenteel een limiet van 100.000 rijen. Als u deze limiet overschrijdt, krijgt u daar een melding van. Om deze beperking te omzeilen stelt u indien mogelijk filters op de pagina in voordat u overschakelt naar de gegevensanalysemodus.  Misschien wilt u een bepaalde groep klanten analyseren of wilt u alleen gegevens van het huidige jaar. U kunt ook een vooraf gedefinieerde weergave kiezen als dit geschikt is voor uw analyse.

## <a name="see-also" />Zie ook

[Ad-hoc gegevensanalyse](reports-adhoc-analysis.md)  
[Bekijken en bewerken in Excel](across-work-with-excel.md)  
