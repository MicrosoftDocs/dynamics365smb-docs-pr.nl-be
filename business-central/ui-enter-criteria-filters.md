---
title: 'Lijsten sorteren, doorzoeken en filteren'
description: 'Werk efficiënt in lijsten door te zoeken in uw gegevens, kolommen te sorteren en resultaten te verfijnen met filtersymbolen en toetsenbordsneltoetsen.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'delimit, FlowFilter, totals, limit, advanced'
ms.search.form: null
ms.date: 10/30/2023
ms.author: jswymer
---
# <a name="sorting-searching-and-filtering"></a>Sorteren, zoeken en filteren

U kunt een paar dingen doen om records in een lijst, in een rapport of XMLport te scannen, te vinden en te beperken. U kunt de records bijvoorbeeld sorteren, doorzoeken en filteren. U kunt sommige of al deze methoden tegelijkertijd toepassen om snel uw gegevens te zoeken of te analyseren.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Voor rapporten en XMLports, kunt u filters instellen zoals in lijsten om af te bakenen welke gegevens in het rapport of de XMLport moeten worden opgenomen, maar u kunt niet sorteren en zoeken.

> [!TIP]
> Wanneer u uw gegevens weergeeft als tegels, kunt u zoeken en filtering gebruiken. Als u de volledige set functies wilt gebruiken voor sorteren, zoeken en filteren, kiest u het pictogram ![Als overzicht weergeven](media/ui_show_as_list_icon.png "Weergeven als lijst pijl naar links"). om de records als een lijst te bekijken.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a>Sorteervolgorde

Met de sorteerfunctie krijgt u snel een overzicht van de gegevens. Als u bijvoorbeeld veel klanten heeft, kunt u ze sorteren op **Klantnr.**, **Valutacode** of **Land-/regiocode** om het overzicht te krijgen dat u nodig heeft.

Om een lijst te sorteren, kunt u:

- Een kolomkoptekst kiezen om te wisselen tussen oplopende en aflopende volgorde of
- De vervolgkeuzepijl in de kolomkop kiezen en vervolgens de actie **Oplopend** of **Aflopend** kiezen.  

> [!NOTE]  
> Sorteren wordt niet ondersteund bij afbeeldingen, BLOB-velden, FlowFilters en velden die niet deel van een tabel zijn.  

## <a name="searching"></a>Zoeken

<!--## Searching by using the Quick Filter -->
Boven aan elke lijstpagina staat een ![Zoeklijst.](media/ui-search/search-list.png "Pictogram Zoeken in lijst") actie **Zoeken** die een snelle en gemakkelijke manier biedt om de records in een lijst te reduceren en alleen de records weer te geven die de gegevens bevatten die u wilt zien.

Als u wilt zoeken, kiest u gewoon de actie **Zoeken** en typt u de tekst die u zoekt, in het vak. U kunt letters, cijfers en andere symbolen invoeren.

Over het algemeen wordt geprobeerd in alle velden tekst overeen te laten komen. Er wordt geen onderscheid gemaakt tussen hoofdletters en kleine letters (hoofdletterongevoelig) en wordt gezocht naar overeenkomst met tekst die ergens in het veld, aan het begin, aan het einde of in het midden wordt geplaatst.

> [!TIP]
> U kunt op <kbd>F3</kbd> drukken om het zoekvak te activeren en te deactiveren. Zie voor meer informatie [Toetsenbordsneltoetsen](keyboard-shortcuts.md#KeyboardFilter).

> [!NOTE]  
> Zoeken kijkt niet naar waarden in afbeeldingen, BLOB-velden, FlowFilters, FlowFields en andere velden die geen deel uitmaken van een tabel.


### <a name="fine-tuning-the-search-with-filter-criteria"></a>De criteria voor Zoeken met filter verfijnen

U kunt nauwkeuriger zoeken door filteroperatoren, uitdrukkingen en filtertokens te gebruiken. In tegenstelling tot filteren, worden deze bij gebruik in het zoekvak op alle velden toegepast, waardoor ze minder efficiënt zijn dan filteren.

- Als u alleen veldwaarden wilt zoeken die exact overeenkomen met de volledige tekst en de hoofdletters/kleine letters, plaatst u de zoektekst tussen enkele aanhalingstekens (`''` bijvoorbeeld `'man'`).

- Als u veldwaarden wilt zoeken die beginnen met een bepaalde tekst en overeenkomen met de hoofdletters/kleine letters, plaatst u `*` achter de tekst (bijvoorbeeld `man*`).

- Als u veldwaarden wilt zoeken die eindigen met een bepaalde tekst en overeenkomen met de hoofdletters/kleine letters, plaatst u `*` vóór de tekst (bijvoorbeeld `*man`).

- Wanneer u `''` of `*` gebruikt, wordt onderscheid gemaakt tussen hoofdletters en kleine letters. Als u hoofdletterongevoelig wilt zoeken, plaatst u `@` vóór de zoektekst (bijvoorbeeld `@man*`).

In de volgende tabel vindt u enkele voorbeelden om aan te geven hoe u de zoekactie kunt gebruiken.

|Zoekcriteria|Zoekt…|
|---------------|----------|
|`man`<br />of <br />`Man`|Alle records met velden die de tekst **man** bevatten, ongeacht hoofdletters. Bijvoorbeeld **Manchester**, **manual** of **Sportsman**. |
|`'Man'`|Alle records met velden die alleen **Man** bevatten, ongeacht hoofdletters.|
|`Man*`|Alle records met velden die beginnen met de tekst <b>Man</b>, met identieke hoofdletters/kleine letters. Bijvoorbeeld **Manchester**, maar niet **manual** of **Sportsman**.|
|`@Man*`|Alle records met velden die beginnen met **man**, ongeacht hoofdletters. Bijvoorbeeld **Manchester** en **manual**, maar niet **Sportsman**.|
|`@*man`|Alle records met velden die eindigen met **man**, ongeacht hoofdletters. Bijvoorbeeld **Sportsman**, maar niet **Manchester** of **manual**.|


## <a name="filtering"></a><a name="filtering"></a>Filteren

Filtering biedt een geavanceerdere en flexibelere manier om te bepalen welke records in een lijst, rapport of XMLport worden opgenomen. Er zijn twee belangrijke verschillen tussen zoeken en filteren, zoals wordt beschreven in de volgende tabel.

|| **Zoeken** | **Filteren** |
|--|----------|------------|
| **Toepasselijke velden** | Zoekt in alle velden die zichtbaar zijn op de pagina. | Filtert een of meer velden afzonderlijk, selecterend vanuit een veld in de tabel, inclusief velden die niet zichtbaar zijn op de pagina. |
| **Afstemmen** | Geeft records weer met velden die voldoen aan de zoektekst, ongeacht hoofdletters/kleine letters of plaatsing van de tekst. | Geeft records weer waar het veld exact overeenkomt met het filter en is hoofdlettergevoelig, tenzij speciale filtersymbolen worden ingevoerd.

Filteren stelt u in staat records weer te geven voor bepaalde rekeningen of klanten, datums, bedragen en andere informatie door filtercriteria op te geven. Alleen records die voldoen aan de criteria, worden weergegeven in de lijst of opgenomen in het rapport, de batchtaak of de XMLport. Als u criteria opgeeft voor meerdere velden, worden alleen de records weergegeven die overeenkomen met alle criteria.

Voor lijsten worden de filters weergegeven in een filtervenster dat links van de lijst verschijnt wanneer u deze activeert. Voor rapporten, batchtaken en XMLports zijn de filters direct zichtbaar op de aanvraagpagina.

### <a name="filtering-with-option-fields"></a>Filteren met optievelden

Voor 'gewone' velden die gegevens, instellingsdatum of bedrijfsgegevens bevatten, kunt u filters instellen door gegevens te selecteren en filterwaarden te typen, en u kunt symbolen gebruiken om geavanceerde filtercriteria te definiëren. Zie voor meer informatie [Filtercriteria invoeren](ui-enter-criteria-filters.md#entering-filter-criteria).

Voor velden van het type **Optie** kunt u echter alleen een filter instellen door een of meer opties te selecteren in een vervolgkeuzelijst met beschikbare opties. Een voorbeeld van een optieveld is het veld **Status** op de pagina **Verkooporders**.

> [!NOTE]
> Wanneer u meerdere opties als filterwaarde selecteert, wordt de relatie tussen de opties gedefinieerd als *OF*. Als u bijvoorbeeld zowel het selectievakje **Open** als **Vrijgegeven** selecteert in het filterveld **Status** op de pagina **Verkooporders**, betekent dit dat verkooporders die open of vrijgegeven zijn, worden weergegeven.

### <a name="setting-filters-on-lists"></a>Filters instellen voor lijsten

In lijsten stelt u filters in met behulp van het filtervenster. Als u het filtervenster voor een lijst wilt weergeven, kiest u de vervolgkeuzepijl naast de naam van de pagina en kiest u vervolgens de actie **Filtervenster weergeven**. U kunt ook drukken op <kbd>Shift</kbd>+<kbd>F3</kbd>.

Als u het filtervenster voor een kolom in een lijst wilt weergeven, kiest u de vervolgkeuzepijl en kiest u vervolgens de actie **Filter**. U kunt ook drukken op <kbd>Shift</kbd>+<kbd>F3</kbd>. Het filtervenster wordt geopend met de geselecteerde kolom weergegeven als een filterveld in de sectie **Filter lijst op**.

Het filterdeelvenster bevat de huidige filters voor een lijst en biedt u de mogelijkheid uw eigen filters in te stellen op een of meer velden door de actie **+ Filter** te kiezen.

 Een filterdeelvenster is verdeeld in drie gedeelten: **Weergaven**, **Filter lijst op** en **Filter totalen op**:

- **Weergaven**

  Sommige lijsten bevatten het gedeelte **Weergaven**. Weergaven zijn variaties van de lijst die vooraf zijn ingesteld met filters. U kunt per lijst zoveel weergaven definiëren en opslaan als u wilt. De weergaven zijn voor u beschikbaar op elk apparaat waarop u inlogt. Zie voor meer informatie [Lijstweergaven opslaan en personaliseren](ui-views.md).

- **Filter lijst op**

  In deze sectie voegt u filters toe aan specifieke velden om het aantal weergegeven records te reduceren. Als u een filter wilt toevoegen, kiest u de actie **+ Filter**. Typ vervolgens de naam van het veld waarop u de lijst wilt filteren of kies een veld in de vervolgkeuzelijst.

- **Filter totalen op**

  Sommige lijsten met berekende velden, zoals bedragen en aantallen, bevatten het gedeelte **Filter totalen op**, waarin u verschillende dimensies kunt aanpassen die van invloed zijn op berekeningen. Als u een filter wilt toevoegen, kiest u de actie **+ Filter**. Typ vervolgens de naam van het veld waarop u de lijst wilt filteren of kies een veld in de vervolgkeuzelijst.

  > [!NOTE]
  > Filters in het gedeelte **Filter totalen op** worden bepaald door FlowFilters in het paginaontwerp. Zie voor technische informatie [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).

U kunt een eenvoudig filter rechtstreeks in een lijst instellen met behulp van het filtervenster, namelijk een filter dat alleen records weergeeft met dezelfde waarde als in de geselecteerde cel. Selecteer een cel in de lijst, kies de vervolgkeuzepijl en kies vervolgens de actie **Filteren op deze waarde**. U kunt ook drukken op <kbd>Alt</kbd>+<kbd>F3</kbd>.

### <a name="setting-filters-in-reports-batch-jobs-and-xmlports"></a>Filters instellen in rapporten, batchtaken en XMLports

Voor rapporten, batchtaken en XMLports zijn de filters direct zichtbaar op de aanvraagpagina. De aanvraagpagina toont de laatst gebruikte filters volgens uw selectie in het veld **Standaardwaarden gebruiken uit**. Zie voor meer informatie [Opgeslagen instellingen gebruiken](ui-work-report.md#SavedSettings).

De hoofdsectie **Filter** toont de standaardfiltervelden die u gebruikt om af te bakenen welke records in het rapport of de XMLport moeten worden opgenomen. Als u een filter wilt toevoegen, kiest u de actie **+ Filter**. Typ vervolgens de naam van het veld waarop u wilt filteren of kies een veld in de vervolgkeuzelijst.

In de sectie **Totalen filteren op** kunt u verschillende dimensies aanpassen die van invloed zijn op berekeningen in het rapport of de XMLport. Als u een filter wilt toevoegen, kiest u de actie **+ Filter**. Typ vervolgens de naam van het veld waarop u wilt filteren of kies een veld in de vervolgkeuzelijst.

## <a name="entering-filter-criteria"></a>Filtercriteria invoeren

Zowel in het filtervenster als op een aanvraagpagina voert u uw filtercriteria in het vak onder het filterveld in.

Het type filterveld bepaalt welke criteria u kunt invoeren. Als u bijvoorbeeld filtert op een veld dat vaste waarden heeft, kunt u alleen kiezen uit die waarden. Voor meer informatie over speciale filtersymbolen raadpleegt u [Filtercriteria](#FilterCriteria) en [Filtertokens](#FilterTokens)

Kolommen die al filters hebben, worden aangegeven met het ![pictogram Filter.](media/ui-search/filter-icon.png "Pictogram Filter") in de kolomkop. Als u een filter wilt verwijderen, kiest u de vervolgkeuzepijl en kiest u vervolgens de actie **Filter wissen**.

> [!TIP]
> Versnel het zoeken en analyseren van uw gegevens met combinaties van toetsenbordsneltoetsen. Selecteer bijvoorbeeld een veld, gebruik <kbd>Shift</kbd>+<kbd>Alt</kbd>+<kbd>F3</kbd> om dat veld aan het filterdeelvenster toe te voegen, typ het filtercriterium, gebruik <kbd>Ctrl</kbd>+<kbd>Enter</kbd> om terug te keren naar de rijen, selecteer een ander veld en gebruik <kbd>Alt</kbd>+<kbd>F3</kbd> om op die waarde te filteren. Zie voor meer informatie [Toetsenbordsneltoetsen](keyboard-shortcuts.md#KeyboardFilter).

### <a name="a-namefiltercriteria-afilter-criteria-and-operators"></a><a name="FilterCriteria"> </a>Filtercriteria en -operatoren

U kunt bij de invoer van criteria alle cijfers en letters gebruiken die u normaal ook kunt gebruiken. Maar er is ook een reeks speciale symbolen die u als operatoren kunt gebruiken om de resultaten verder te filteren. In de volgende secties worden deze symbolen beschreven en hoe u ze als operators in filters kunt gebruiken.

> [!TIP]
> Zie voor meer informatie over het filteren van datums en tijden [Werken met kalenderdatums en -tijden](ui-enter-date-ranges.md).

> [!IMPORTANT]
> - Er kunnen situaties zijn waarin de waarde waarop u wilt filteren een symbool bevat dat een operator is. Zie voor meer informatie over het omgaan met deze situaties [Filteren op waarden die symbolen bevatten](#symbols) voor meer instructies over het omgaan met deze situatie.
>
> - Als er meer dan 200 operatoren in één filter zijn, groepeert het systeem automatisch enkele uitdrukkingen tussen haakjes `()` met het oog op verwerking. Dit heeft geen effect op het filter of de resultaten.  

#### <a name="-interval"></a>(..) Interval

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`1100..2100`|Nummers 1100 t/m 2100|  
|`..2500`|Tot en met 2500|  
|`..12 31 00`|Datums tot en met 31.12.00|  
|`P8..`|Informatie voor boekhoudperiode 8 en daarna|  
|`..23`|Van begindatum tot 23 lopende maand, lopend jaar 23:59:59|  
|`23..`|Van 23 lopende maand, lopend jaar 00:00:00 tot eindtijd|  
|`22..23`|Van 22 lopende maand, lopend jaar 0:00:00 tot 23 lopende maand, lopend jaar 23:59:59| 

> [!TIP]
> Als u een numeriek toetsenbord gebruikt, kan de decimaaltekentoets een ander teken dan een punt (.) weergeven. Selecteer hiervoor de toetsen <kbd>Alt</kbd>+<kbd>Decimaalteken</kbd> op het numerieke toetsenbord om te wisselen naar een punt. Wanneer u terug wilt schakelen, selecteert u <kbd>Alt</kbd>+<kbd>Decimaalteken</kbd> nogmaals. Zie [Het decimale scheidingsteken instellen dat wordt gebruikt door numerieke toetsenborden](ui-enter-data.md#decimal) voor meer informatie.

#### <a name="124-eitheror"></a>(&#124;) Of/of

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`1200|1300`|Nummers met 1200 of 1300|  

#### <a name="-not-equal-to"></a>(<>) Niet gelijk aan

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`<>0`|Alle nummers behalve 0<br /><br /> Met de SQL Server-optie kunt u dit symbool combineren met jokertekens. <>A* betekent bijvoorbeeld 'Niet gelijk aan tekst die begint met A'.|  

#### <a name="-greater-than"></a>(>) Groter dan

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`>1200`|Nummers groter dan 1200|  

#### <a name="-greater-than-or-equal-to"></a>(>=) Groter dan of gelijk aan

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`>=1200`|Nummers groter dan of gelijk aan 1200|  

#### <a name="-less-than"></a>(<) Kleiner dan

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`<1200`|Nummers kleiner dan 1200|  

#### <a name="-less-than-or-equal-to"></a>(<=) Kleiner dan of gelijk aan

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`<=1200`|Nummers kleiner dan of gelijk aan 1200|  

#### <a name="-and"></a>(&) En

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`>200&<1200`|Getallen groter dan 200 en kleiner dan 1200|  

#### <a name="-an-exact-character-match"></a>('') Een exacte tekenovereenkomst

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`'man'`|Tekst die exact overeenkomt met **man** en hoofdlettergevoelig is.|  
|`''`|Tekst die leeg is.|  

#### <a name="-case-insensitive"></a>(@) Niet hoofdlettergevoelig

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`@man*`|Tekst die begint met **man** en niet hoofdlettergevoelig is.|  

#### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Een onbeperkt aantal onbekende tekens

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`*Co*`|Tekst die **Co** bevat en hoofdlettergevoelig is.|  
|`*Co`|Tekst die eindigt met **Co** en hoofdlettergevoelig is.|  
|`Co*`|Tekst die begint met **Co** en hoofdlettergevoelig is.|  

#### <a name="-one-unknown-character"></a>(?) Een onbekend teken

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`Hans?n`|Tekst zoals **Jansen** of **Jansma**|  

#### <a name="combined-format-expressions"></a>Gecombineerde notatiesoorten

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Alle records met het nummer 5999 of een nummer uit het interval 8100 tot en met 8490.|  
|`..1299|1400..`|Records met een nummer kleiner dan of gelijk aan 1299 of gelijk aan 1400 en hoger. Met andere woorden: alle nummers behalve 1300 tot en met 1399.|  
|`>50&<100`|Records met een nummer groter dan 50 en kleiner dan 100, ofwel nummer 51 tot en met 99.|  

### <a name="filtering-on-values-that-contain-symbols"></a><a name="symbols"></a>Filteren op waarden die symbolen bevatten

Er kunnen gevallen zijn waarin veldwaarden een van de volgende symbolen bevatten:

- &
- (
- )
- =
- &#124;

Als u op een van deze symbolen wilt filteren, plaatst u de filterexpressie tussen enkele aanhalingstekens (`'<expression with symbol>'`). Als u bijvoorbeeld wilt filteren op records die beginnen met de tekst *J & V*, is de filterexpressie `'J & V*'`.

Deze vereiste is niet nodig voor andere symbolen.

### <a name="a-namefiltertokens-afilter-tokens"></a><a name="FilterTokens"> </a>Filtertokens

Wanneer u filtercriteria invoert, kunt u ook woorden typen die een speciale betekenis hebben, filtertokens genaamd. Na het invoeren van het tokenwoord wordt het woord vervangen door de waarde of waarden die het woord vertegenwoordigt. Filtertokens maken filtering eenvoudiger doordat u niet naar andere pagina's hoeft te navigeren om waarden op te zoeken die u aan uw filter wilt toevoegen. In de onderstaande tabellen worden enkele van de tokens beschreven die u als filtercriteria kunt gebruiken.

> [!TIP]
> Uw organisatie kan aangepaste tokens gebruiken. Als u informatie wilt over de volledige set tokens die voor u beschikbaar zijn of als u aangepaste tokens wilt toevoegen, overlegt u met uw beheerder. Voor technische informatie raadpleegt u [Filtertokens toevoegen](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).

#### <a name="me-or-userid-records-assigned-to-you"></a>(%me of %userid) Records die aan u zijn toegewezen

Gebruik `%me` of `%userid` wanneer u velden filtert die de gebruikers-id bevatten, zoals het veld **Toegewezen aan gebruikers-id**, om alle records weer te geven die aan u zijn toegewezen.

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`%me`<br />of<br />`%userid`|Records die aan uw gebruikersaccount zijn toegewezen. |  

#### <a name="mycustomers-customers-in-my-customers"></a>(%mycustomers) Klanten in Mijn klanten

Gebruik `%mycustomers` in het veld klant**nr.** om alle records weer te geven voor klanten die deel uitmaken van de lijst **Mijn klanten** in uw rolcentrum.

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`%mycustomers`|Klanten in **Mijn klanten** in uw rolcentrum. |  

#### <a name="myitems-items-in-my-items"></a>(%myitems) Artikelen in Mijn artikelen

Gebruik `%myitems` in het veld artikel**nr.** om alle records weer te geven voor artikelen die deel uitmaken van de lijst **Mijn artikelen** in uw rolcentrum.

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`%myitems`|Artikelen in **Mijn artikelen** in uw rolcentrum. |  

#### <a name="myvendors-vendors-in-my-vendors"></a>(%myvendors) Leveranciers in Mijn leveranciers

Gebruik `%myvendors` in het veld leveranciers**nr.** om alle records weer te geven voor leveranciers die deel uitmaken van de lijst **Mijn leveranciers** in uw rolcentrum.

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`%myvendors`|Leveranciers in **Mijn leveranciers** in uw rolcentrum. |  

## <a name="see-also"></a>Zie ook

[Veelgestelde vragen over zoeken en filteren](ui-search-filter-faq.yml)  
[Lijstweergaven opslaan en personaliseren](ui-views.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
