---
title: Gegevens analyseren op lijstpagina's en query's met behulp van de gegevensanalysemodus
description: Leer hoe u de gegevensanalysemodus in Business Central gebruikt om gegevens te analyseren.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 10/05/2023
ms.custom: bap-template
ms.service: dynamics365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# <a name="analyze-list-page-and-query-data-using-data-analysis-mode"></a>Lijstpagina- en querygegevens analyseren met behulp van de gegevensanalysemodus

> **VAN TOEPASSING OP:** openbare preview in Business Central 2023 releasewave 1 en hoger voor het analyseren van lijstpagina's; algemeen beschikbaar in Business Central 2023 releasewave 2 voor het analyseren van gegevens van lijstpagina's en query's.

In dit artikel leert u hoe u gegevens vanaf lijstpagina's en query's analyseert met behulp van de *gegevensanalysemodus*. Met de gegevensanalysemodus kunt u gegevens rechtstreeks vanaf de pagina analyseren, zonder dat u een rapport hoeft uit te voeren of naar een andere toepassing zoals Excel hoeft te schakelen. Het biedt een interactieve en veelzijdige manier om gegevens te berekenen, samen te vatten en te onderzoeken. In plaats van rapporten uit te voeren met verschillende opties en filters, kunt u meerdere tabbladen toevoegen die verschillende taken of weergaven van de gegevens vertegenwoordigen. Voorbeelden kunnen zijn "Mijn klanten", "Opvolgitems", "Onlangs toegevoegde leveranciers", "Verkoopstatistieken" of elke andere weergave die u maar kunt bedenken.

> [!TIP]
> Een goede zaak van de gegevensanalysemodus is dat het geen van de onderliggende gegevens van de lijstpagina of query of de lay-out van de pagina of query verandert wanneer deze zich niet in de gegevensanalysemodus bevindt. Dus de beste manier om te leren wat u kunt doen in de gegevensanalysemodus, is door dingen uit te proberen.

## <a name="prerequisites"></a>Vereisten

- Als u Business Central versie 22 gebruikt, is de gegevensanalysemodus in preview. Een beheerder moet het dus inschakelen voordat u het kunt gebruiken. Om dit in te schakelen gaat u naar de pagina **Functiebeheer** en schakelt u **Functie-update: snel gegevens rechtstreeks in Business Central analyseren** in. [Meer informatie over functiebeheer](/dynamics365/business-central/dev-itpro/administration/feature-management).
- In versie 23 en hoger moet aan uw account de machtigingenset **DATA ANALYSIS - EXEC** zijn toegewezen of moet deze de uitvoermachtiging bevatten voor het systeemobject **9640 Gegevensanalysemodus toestaan**. Als beheerder kunt u deze machtigingen uitsluiten voor gebruikers die u geen toegang wilt hebben tot de analysemodus.

> [!NOTE]
> Mogelijk ziet u op sommige lijstpagina's geen **Analyseren**-schakelaar voor het overschakelen naar de analysemodus. De reden hiervoor is dat ontwikkelaars de analysemodus op specifieke pagina's kunnen uitschakelen door de [eigenschap AnalysisModeEnabled](/dynamics365/business-central/dev-itpro/developer/properties/devenv-analysismodeenabled-property) in AL te gebruiken.

## <a name="get-started"></a>Aan de slag

1. Open de lijstpagina of query.

   Als u bijvoorbeeld wilt werken met de pagina **Klantenposten**, selecteert u het pictogram ![Vergrootglas dat de functie Vertel me opent](media/ui-search/search_small.png) (<kbd>Alt</kbd>+<kbd>Q</kbd>), voert u *klantenposten* in en kiest u vervolgens de gerelateerde koppeling. 

2. Zet op de actiebalk boven aan de pagina de schakelaar **Analyseren** aan.

    De gegevensanalysemodus opent de gegevens in een ervaring die is geoptimaliseerd voor gegevensanalyse.  In de gegevensanalysemodus wordt de normale actiebalk vervangen door een speciale gegevensanalysebalk. De volgende afbeelding illustreert de verschillende gebieden van een pagina in de gegevensanalysemodus.

   [![Toont een overzicht van een pagina in de gegevensanalysemodus](media/analysis-mode-overview-2.png)](media/analysis-mode-overview-2.png#lightbox)

   Elk gebied wordt in de volgende secties uitgelegd.

3. Gebruik de verschillende gebieden om gegevens te manipuleren, samen te vatten en te analyseren. Zie de volgende secties voor meer informatie.

4. Als u de analysemodus wilt verlaten, schakelt u de schakelaar **Analyseren** uit.

   De analysetabbladen die u hebt toegevoegd, blijven staan totdat u ze verwijdert. Dus als u weer terugkeert naar de gegevensanalysemodus, ziet u ze precies zoals u ze achterliet.

> [!NOTE]
> De gegevens die in de analysemodus worden weergegeven, worden beheerd door de filters of weergaven die op de lijstpagina zijn ingesteld. Hierdoor kunt u gegevens vooraf filteren voordat u naar de analysemodus gaat.

## <a name="work-with-data-analysis-mode"></a>Werken met de gegevensanalysemodus

In de gegevensanalysemodus is de pagina verdeeld in twee gebieden:

- Het hoofdgebied, dat bestaat uit het gegevensgebied (1), overzichtsbalk (2) en tabbladenbalk (5)
- Het gebied voor gegevensmanipulatie, dat bestaat uit twee deelvensters: kolommen (3) en analysefilters (4).

### <a name="data-area-1"></a>Gegevensgebied (1)

In het gegevensgebied worden de rijen en kolommen van de lijstpaginaquery weergegeven en worden de gegevens samengevat. Het gegevensgebied biedt een veelzijdige manier om de lay-out van kolommen te regelen en een snelle manier om een samenvatting van de gegevens te krijgen. Voor kolommen die numerieke waarden bevatten, wordt de som van alle waarden in de kolom weergegeven in een laatste rij, tenzij u rijgroepen hebt gedefinieerd. In dit geval verschijnen de sommen als een subtotaal voor de groepen.  

![Toont een overzicht van een gegevensgebied op een pagina in de gegevensanalysemodus](media/analysis-mode-data-area.png)

- Als u een kolom wilt verplaatsen, selecteert u deze en sleept u deze naar de plaats waar deze het meest logisch is in uw analyse.
- Klik met de rechtermuisknop op de kolom of plaats de muisaanwijzer erop en selecteer het menupictogram ![Toont het pictogram op een kolom in de gegevensanalysemodus waarmee een menu met acties wordt geopend](media/analysis-mode-column-menu-icon.png) om toegang te krijgen tot verschillende acties die u op kolommen kunt uitvoeren. Voorbeeld:

  - Als u een kolom links of rechts van het gegevensgebied wilt vastzetten zodat deze niet van het scherm af beweegt wanneer u schuift, selecteert u ![Toont het pictogram op een kolom in de gegevensanalysemodus waarmee een menu met acties wordt geopend](media/analysis-mode-column-menu-icon.png) > **Kolom vastmaken** > **Links vastmaken** het kolomgedeelte.
  - Definieer gegevensfilters rechtstreeks op de kolomdefinitie in plaats van naar de **Analysefilters**-deelvensters te gaan. U kunt nog steeds details bekijken over gerelateerde gegevens en voor elke regel, en de kaart openen voor meer informatie over een bepaalde entiteit.
- Gebruik het gegevensgebied om met de gegevens te werken. Voor kolommen die numerieke, optelbare waarden bevatten, kunt u beschrijvende statistieken voor een reeks velden verkrijgen door ze te markeren. De statistieken verschijnen in de statusbalk (2) onder aan de pagina.
- Exporteer gegevens in Excel- of csv-indeling. Klik met de rechtermuisknop op het gegevensgebied of een selectie van cellen om te exporteren.

### <a name="summary-bar-2"></a>Overzichtsbalk (2)

De overzichtsbalk bevindt zich onder aan de pagina en geeft statistieken weer over de gegevens in de lijstpagina of query. Terwijl u werkt met kolommen waarvan de waarden kunnen worden opgeteld, zoals het selecteren van meerdere rijen in een kolom die bedragen bevat, worden de gegevens bijgewerkt.

![Toont een overzicht van een overzichtsbalk in de gegevensanalysemodus](media/analysis-mode-totals-row.png)

De volgende tabel beschrijft de verschillende getallen die worden weergegeven in het totalengebied:

|Nummer|Omschrijving|
|-|-|
|Rijen|Het aantal geselecteerde rijen als onderdeel van het totale aantal beschikbare rijen. |
|Totaal aantal rijen|Het aantal rijen in de ongefilterde lijst of query.|
|Gefilterd|Het aantal rijen dat wordt weergegeven als resultaat van de filters die op de lijst of query zijn toegepast.|
|Gemiddeld|De gemiddelde waarde in alle geselecteerde optelbare velden.|
|Aantal|Het aantal geselecteerde rijen.|
|Min|De minimale waarde in alle geselecteerde optelbare velden.|
|Max|De maximale waarde in alle geselecteerde optelbare velden.|
|Som|Het totaal van alle waarden in de geselecteerde optelbare velden.|

### <a name="columns-3"></a>Kolommen (3)

**Kolommen** is een van de twee deelvensters die samenwerken om uw analyse te definiëren. Het andere gebied is het deelvenster **Analysefilters**. Het deelvenster **Kolommen** wordt gebruikt om de gegevens samen te vatten. Gebruik het deelvenster **Kolommen** om te definiëren welke kolommen in de analyse moeten worden opgenomen.

![Toont een overzicht van het kolommendeelvenster in de gegevensanalysemodus](media/analysis-mode-columns-2.png)

|Districten|Omschrijving|
|-|-|
|Zoeken/alle vakjes in- of uitschakelen|Zoeken naar kolommen. Schakel het selectievakje in om alle kolommen te selecteren/wissen.|
|Selectievakjes|Dit gebied bevat een selectievakje voor elk veld in de brontabel van de lijst of query. Gebruik dit gebied om te wijzigen welke kolommen worden weergegeven. Schakel een selectievakje in om de kolom voor het veld op de pagina weer te geven; schakel het selectievakje uit om de kolom te verbergen. |
|Rijgroepen|Gebruik dit gebied om gegevens te groeperen en op te tellen op een of meer velden. U kunt alleen niet-numerieke velden opnemen, zoals tekst-, datum- en tijdvelden. Rijgroepen worden vaak gebruikt in de draaimodus.|
|Waarden|Gebruik dit gebied om velden op te geven waarvoor u een totaal wilt hebben. U kunt alleen velden opnemen die getallen bevatten die bij elkaar kunnen worden opgeteld; bijvoorbeeld geen tekst-, datum- of tijdvelden.|

Selecteer het grijppictogram om een veld van het ene gebied naar het andere te verplaatsen ![Toont een overzicht van een pagina in de analysemodus](media/column-grab-icon.png) naast de kolom in de bovenstaande lijst en sleep naar het doelgebied. U mag een veld niet verplaatsen naar een gebied waar het niet is toegestaan.

### <a name="analysis-filters-4"></a>Analysefilters (4)

Met het deelvenster **Analysefilters** kunt u verdere gegevensfilters op kolommen instellen om de vermeldingen in de lijst te beperken. Stel filters in op kolommen om de vermeldingen in de lijst en de daaropvolgende sommen te beperken tot alleen die vermeldingen waarin u bent geïnteresseerd op basis van een criterium dat u definieert. Stel dat u alleen geïnteresseerd bent in gegevens van een specifieke klant of verkooporders die een bepaald bedrag overschrijden. Om een filter in te stellen selecteert u de kolom, kiest u de vergelijkingsbewerking uit de lijst (zoals **Is gelijk aan** of **Begint met**) en voert u de waarde in.

![Toont een overzicht van het filterdeelvenster in de analysemodus](media/analysis-mode-filters.png)

> [!NOTE]
> De extra filters zijn alleen van toepassing op het huidige analysetabblad. Hierdoor kunt u precies de extra datafilters definiëren die nodig zijn voor een specifieke analyse.

### <a name="tabs-5"></a>Tabbladen (5)

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


## <a name="date-hierarchies"></a>Datumhiërarchieën

In de analysemodus worden datumvelden van de gegevensset gegenereerd in een jaar-kwartaal-maand-hiërarchie van drie afzonderlijke velden. Deze hiërarchie is gebaseerd op de normale kalender, niet op eventuele fiscale kalenders die zijn gedefinieerd in Business Central.

De extra velden heten _\<field name\> jaar_, _\<field name\> kwartaal_ en _\<field name\> maand_. Als de gegevensset bijvoorbeeld een veld bevat met de naam _Boekingsdatum_, bestaat de overeenkomstige datumhiërarchie uit velden met de naam _Boekingsdatum jaar_, _Boekingsdatum kwartaal_, en _Boekingsdatum maand_.

> [!NOTE]
> De datumhiërarchie is momenteel alleen van toepassing op velden van het type datum, niet op velden van het type datumtijd.

## <a name="pivot-mode"></a>Draaimodus

U kunt de draaimodus gebruiken om grote hoeveelheden numerieke gegevens te analyseren, waarbij gegevens worden opgeteld op categorieën en subcategorieën. De draaimodus is vergelijkbaar met [draaitabellen in Microsoft Excel](https://support.microsoft.com/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576).

Om de draaimodus in en uit te schakelen verschuift u de schakelaar **Draaimodus** in het deelvenster **Kolommen** (3). Wanneer u de draaimodus inschakelt, verschijnt het gebied **Kolomlabels** in het deelvenster. Gebruik het gebied **Kolomlabels** om somtotalen voor rijen in categorieën te groeperen. Velden die u toevoegt aan het gebied **Kolomlabels**, worden weergegeven als kolommen in het gegevensgebied (1).

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


## <a name="analyze-large-amounts-of-data"></a>Grote hoeveelheden gegevens analyseren

Als de gegevensset die u wilt analyseren groter is dan 100.000 rijen, wordt u aangeraden een analysemodus in te voeren die is geoptimaliseerd voor grote gegevenssets. Er zijn momenteel twee beperkingen als u naar deze modus overschakelt: 

- De opmaak van velden van de volgende vier gegevenstypen kan veranderen: 

   - valuta 
   - decimalen (altijd weergegeven met twee decimalen) 
   - datums (altijd weergegeven in het formaat JJJJ-MM-DD)
   - tijdzones
- Velden die in de draaitabelmodus worden gebruikt en aan kolomlabels worden toegevoegd, moeten een klein aantal afzonderlijke waarden hebben.

   Als u de draaitabelmodus inschakelt en een veld naar het gebied **Kolomlabels** sleept, waar de onderliggende gegevens voor dat veld te veel verschillende waarden bevatten, reageert het browsertabblad mogelijk niet meer en wordt het uiteindelijk gesloten, waardoor u opnieuw moet beginnen in een nieuwe sessie. In dit geval moet u niet op dat veld draaien of een filter op het veld instellen voordat u het toevoegt aan het gebied **Kolomlabels**.

## <a name="share-data-analysis"></a>Gegevensanalyse delen

Nadat u een analyse op een tabblad heeft voorbereid, kunt u deze rechtstreeks vanuit de client als koppeling delen met collega's en anderen in uw organisatie. Alleen ontvangers die machtiging hebben voor het bedrijf en de gegevens kunnen de koppeling gebruiken.

1. Selecteer op het tabblad Analyse de pijl-omlaag en selecteer vervolgens **Koppeling kopiëren**.

   ![Toont de actie voor het kopiëren van een analyse](media/copy-analysis.svg)

   Het dialoogvenster **Koppeling naar \<tab name\>** wordt geopend.

1. Standaard wordt de analyse die u deelt, gekoppeld aan de pagina of query in het bedrijf waar u momenteel werkt, wat wordt aangegeven met `company=<company_name>` in het URL-veld naast de knop **Kopiëren**. Als u een koppeling wilt sturen naar een analyse die niet aan een specifiek bedrijf is gekoppeld, stelt u het veld **Bedrijf:** in op **Niet koppelen aan een specifiek bedrijf**.

   ![Toont het dialoogvenster voor kopiëren van een koppeling voor een analysetabblad](media/analysis-link-copied.svg)

1. Selecteer **Kopiëren**.

1. Plak de koppeling in de communicatiemedia van uw keuze, zoals Word, Outlook, Teams, OneNote, enzovoort. 

2. Na ontvangst kunnen ontvangers vervolgens de koppeling selecteren en de analyse voor de pagina of query openen in Business Central. Ze worden gevraagd een naam op te geven voor het nieuwe analysetabblad dat wordt gemaakt.  

## <a name="limitations-in-2023-release-wave-1-preview"></a>Beperkingen in releasewave 1 van 2023 (preview)

De openbare preview van deze functie heeft de volgende beperkingen:

- De analysemodusweergave heeft momenteel een limiet van 100.000 rijen. Als u deze limiet overschrijdt, krijgt u daar een melding van. Om deze beperking te omzeilen stelt u indien mogelijk filters op de pagina in voordat u overschakelt naar de analysemodus. U wilt mogelijk bijvoorbeeld een bepaalde groep klanten analyseren of wilt u alleen gegevens van het huidige jaar. U kunt ook een vooraf gedefinieerde weergave kiezen als dit geschikt is voor uw analyse.
- De functie voor het analyseren van gegevens voor delen is niet beschikbaar.
- De mogelijkheid om voorkeurskeuzes voor gegevensanalyse op lijstpagina's op te slaan en analysemenu's per analysetabblad op te slaan, is momenteel niet beschikbaar.

## <a name="see-also"></a>Zie ook

[Ad-hocgegevensanalyse](reports-adhoc-analysis.md)  
[Weergeven en bewerken in Excel](across-work-with-excel.md)  
