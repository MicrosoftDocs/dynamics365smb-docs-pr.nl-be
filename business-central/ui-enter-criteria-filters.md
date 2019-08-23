---
title: Lijsten sorteren, doorzoeken en filteren | Microsoft Docs
description: Werk efficiënt in lijsten door te zoeken in uw gegevens, kolommen te sorteren en resultaten te verfijnen met krachtige filtersymbolen en toetsenbordsneltoetsen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 06/13/2019
ms.author: sgroespe
ms.openlocfilehash: 5f3bab58a2387f5bf21042da782756f7b36d4792
ms.sourcegitcommit: f5050fd209b8d66722c81abe48c4c0a6f749a1f7
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/12/2019
ms.locfileid: "1740514"
---
# <a name="sorting-searching-and-filtering-lists"></a>Lijsten sorteren, doorzoeken en filteren
U kunt een paar dingen doen om records in een lijst te scannen, te vinden en te beperken. U kunt de records bijvoorbeeld sorteren, doorzoeken en filteren. U kunt sommige of al deze methoden tegelijkertijd toepassen om snel uw gegevens te zoeken of te analyseren.

> [!TIP]
> Wanneer u uw gegevens weergeeft als tegels, kunt u zoeken en elementaire filtering gebruiken. Als u de volledige set functies wilt gebruiken voor sorteren, zoeken en filteren, kiest u het pictogram ![Als overzicht weergeven](media/ui_show_as_list_icon.png "linkerpijl Als overzicht weergeven") om gegevens als lijst weer te geven.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a>Sorteervolgorde
Met de sorteerfunctie krijgt u snel een overzicht van de gegevens. Als u veel klanten hebt, kunt u er bijvoorbeeld voor kiezen hen te sorteren op **Klantnr.**, **Klantboekingsgroep**, **Valutacode**, **Land-/regiocode** of **Btw-nummer** voor het door u gewenste overzicht.

Als u een lijst wilt sorteren, kunt u een kolomkoptekst kiezen om te schakelen tussen op- en aflopend, of de kleine pijl-omlaag in de kolomkop kiezen en vervolgens **Oplopend** of **Aflopend** kiezen.  

> [!NOTE]  
>   Sorteren wordt niet ondersteund bij afbeeldingen, BLOB-velden, FlowFilters en velden die niet deel van een tabel zijn.  

## <a name="searching"></a>Zoeken
<!--## Searching by using the Quick Filter -->
Boven aan elke lijstpagina staat een ![lijst Zoeken](media/ui-search/search-list.png "pictogram Lijst Zoeken") pictogram **Zoeken** dat een snelle en gemakkelijke manier biedt om de records in een lijst te reduceren en alleen de records weer te geven die de gegevens bevatten die u wilt zien.

Als u wilt zoeken, selecteert u het zoekpictogram en typt u de tekst die u zoekt, in het vak. U kunt letters, cijfers en andere symbolen invoeren.

### <a name="fine-tuning-the-search"></a>De zoekactie verfijnen
Over het algemeen probeert de zoekactie tekst te vinden in alle velden. Er wordt geen onderscheid gemaakt tussen kleine letters en hoofdletters (hoofdletterongevoelig dus) en er wordt tekst overal in het veld gezocht (aan het begin, aan het einde of in het midden).

U kunt echter een exactere zoekactie maken door de volgende speciale tekens te gebruiken:

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

> [!TIP]
> U kunt op F3 drukken om het zoekvak te activeren en te deactiveren. Zie voor meer informatie [Toetsenbordsneltoetsen](keyboard-shortcuts.md#KeyboardFilter).

## <a name="Filtering"> </a>Filteren
Filtering biedt een geavanceerdere en flexibelere manier om te bepalen welke records in een lijst worden weergegeven. Er zijn twee belangrijke verschillen tussen zoeken en filteren, zoals wordt beschreven in de volgende tabel.

|| **Zoeken** | **Filteren** |
|--|----------|------------|
| **Toepasselijke velden** | Zoekt in alle velden die zichtbaar zijn op de pagina. | Filtert een of meer velden afzonderlijk, selecterend vanuit een veld in de tabel, inclusief velden die niet zichtbaar zijn op de pagina. |
| **Afstemmen** | Geeft records weer met velden die voldoen aan de zoektekst, ongeacht hoofdletters/kleine letters of plaatsing van de tekst. | Geeft records weer waar het veld exact overeenkomt met het filter en is hoofdlettergevoelig, tenzij speciale filtersymbolen worden ingevoerd.

Filteren stelt u in staat records weer te geven voor bepaalde rekeningen of klanten, datums, bedragen en andere informatie door filtercriteria op te geven. Alleen records die voldoen aan de criteria, worden weergegeven. Als u criteria opgeeft voor meerdere velden, worden alleen de records weergegeven die overeenkomen met alle criteria.

### <a name="working-in-the-filter-pane"></a>Werken in het filterdeelvenster

Als u het filterdeelvenster wilt weergeven, selecteert u het ![pictogram Filterdeelvenster](media/open-filter-pane-icon.png "pictogram Filterdeelvenster") boven aan de lijst of drukt u op **Shift+F3**. Voor lijsten in het Rolcentrum kunt u ook de pijl omlaag kiezen naast de paginatitel op de navigatiebalk boven de lijst en vervolgens **Filterdeelvenster weergeven** kiezen, zoals u hier ziet:

![Filterdeelvenster weergeven](media/open-filter-pane.png "Filterdeelvenster weergeven")

Het filterdeelvenster bevat de huidige filters voor een lijst en biedt u de mogelijkheid uw eigen filters in te stellen op een of meer velden. De volgende afbeelding toont een voorbeeldfilterdeelvenster voor een lijst verkoopoffertes.

![Overzicht van filterdeelvenster ](media/filter-pane-overview.png "pictogram Filter")

Een filterdeelvenster is verdeeld in drie gedeelten: **Weergaven**, **Filter lijst op** en **Filter totalen op**:

- **Weergaven**

  Sommige lijsten bevatten het gedeelte **Weergaven**. Weergaven zijn variaties van de lijst die vooraf zijn ingesteld met filters. Als u naar een andere weergave van uw lijst wilt schakelen, selecteert u gewoon een koppeling. U kunt de filters in een weergave tijdelijk wijzigen, maar de wijzigingen worden niet permanent opgeslagen.

- **Filter lijst op**

  In het gedeelte **Filter lijst op** voegt u filters toe aan specifieke velden om het aantal weergegeven records te reduceren. Als u een filter wilt toevoegen, selecteert u **+ Filter**, selecteert u het veld dat u wilt filteren uit de velden in de tabel en voert u filtercriteria in het vak in.

- **Filter totalen op**

  Sommige lijsten met berekende velden, zoals bedragen en aantallen, bevatten het gedeelte **Filter totalen op**, waarin u verschillende dimensies kunt aanpassen die van invloed zijn op berekeningen. U kunt bijvoorbeeld snel uw rekeningschema analyseren door bedragen te filteren op een bepaalde periode of u kunt de totalen voor verkooporders uit alleen een bepaald magazijn weergeven.

  Als u een filter wilt toevoegen, selecteert u **+ Filter**, selecteert een van de voorgedefinieerde dimensies en voegt u de filtercriteria in het vak toe.

  > [!NOTE]
  > Filters in het gedeelte **Filter totalen op** worden bepaald door FlowFilters in het paginaontwerp. Zie voor technische informatie [FlowFilters](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).


### <a name="entering-filter-criteria-in-the-filter-pane"></a>Filtercriteria invoeren in het filterdeelvenster
Als u een veld wilt selecteren om op te filteren, voert u een van de volgende handelingen uit:
  - Kies in het filterdeelvenster **+ Veld**. Typ de naam van het veld dat u wilt filteren of kies een veld uit het menu met alle velden in de tabel.

  - Kies in een kolomkop de pijl omlaag en kies vervolgens **Filteren...**. Zo opent u het filterdeelvenster en voegt u de kolom aan het filterdeelvenster toe.

U kunt nu uw filtercriteria in het vak typen of selecteren. Het type veld waarop u filtert, bepaalt welke criteria u kunt invoeren. Als u bijvoorbeeld filtert op een veld dat vaste waarden heeft, kunt u alleen kiezen uit die waarden. Voor meer informatie over speciale filtersymbolen raadpleegt u [Filtercriteria](#FilterCriteria) en [Filtertokens](#FilterTokens)

Kolommen die al filters bevatten, worden aangegeven door het ![pictogram Filter](media/ui-search/filter-icon.png "pictogram Filter") in de kolomkop. Als u een filter wilt verwijderen, selecteert u de kolomkop en kiest u vervolgens **Filter wissen**.


### <a name="entering-filter-criteria-without-using-the-filter-pane"></a>Filtercriteria invoeren zonder het filterdeelvenster te gebruiken
U kunt eenvoudige filters rechtstreeks in de lijst opgeven zonder het filterdeelvenster te hoeven gebruiken.
Druk terwijl een veld in een rij is ingeschakeld op de toetsenbordsneltoets **Alt+F3** om alleen de records weer te geven die dezelfde waarde hebben. U kunt een ander veld selecteren en dezelfde snelkoppeling opnieuw gebruiken om door te gaan met het verfijnen van uw filters. Als het geselecteerde veld al is gefilterd, wordt het filter met **Alt+F3** uitgeschakeld.

> [!TIP]
> Versnel het zoeken en analyseren van uw gegevens met combinaties van toetsenbordsneltoetsen. Selecteer bijvoorbeeld een veld, gebruik **Shift+Alt+F3** om dat veld aan het filterdeelvenster toe te voegen, typ het filtercriterium, gebruik **Ctrl+Enter** om terug te keren naar de rijen, selecteer een ander veld en gebruik **Alt+F3** om op die waarde te filteren.
Zie voor meer informatie [Toetsenbordsneltoetsen](keyboard-shortcuts.md#KeyboardFilter).


## <a name="FilterCriteria"> </a>Filtercriteria en -symbolen
U kunt bij de invoer van criteria alle cijfers en letters gebruiken die u normaal ook kunt gebruiken. Daarnaast kunt u speciale symbolen (of operatoren) gebruiken om de resultaten verder te filteren. De volgende tabellen bevatten de tekens die in filters kunnen worden gebruikt. Voor datums en tijden kunt u ook [Werken met kalenderdatums en -tijden](ui-enter-date-ranges.md) raadplegen voor meer gedetailleerde informatie.

> [!IMPORTANT]  
>  Het kan voorkomen dat veldwaarden deze symbolen bevatten en u hierop wilt filteren. Hiervoor moet u de filterexpressie opnemen die het symbool tussen aanhalingstekens (“) bevat. Als u wilt filteren op records die beginnen met de tekst *S&R*, is de filterexpressie bijvoorbeeld `'S&R*'`.

In de volgende secties wordt beschreven hoe u de verschillende operatoren kunt gebruiken.

> [!NOTE]
> Als er meer dan 200 operatoren in één filter zijn, groepeert het systeem automatisch enkele uitdrukkingen tussen haakjes `()` met het oog op verwerking. Dit heeft geen effect op het filter of de resultaten.  

### <a name="-interval"></a>(..) Interval

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`1100..2100`|Nummers 1100 t/m 2100|  
|`..2500`|Tot en met 2500|  
|`..12 31 00`|Datums tot en met 31.12.00|  
|`P8..`|Gegevens voor boekhoudperiode 8 en verder|  
|`..23`|Van begindatum tot 23 lopende maand, lopend jaar 23:59:59|  
|`23..`|Van 23 lopende maand, lopend jaar 00:00:00 tot eindtijd|  
|`22..23`|Van 22 lopende maand, lopend jaar 0:00:00 tot 23 lopende maand, lopend jaar 23:59:59|  

### <a name="124-eitheror"></a>(&#124;) Of/of 

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`1200|1300`|Nummers met 1200 of 1300|  

### <a name="-not-equal-to"></a>(<>) Niet gelijk aan  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`<>0`|Alle nummers behalve 0<br /><br /> Met de SQL Server-optie kunt u dit teken combineren met jokertekens. <>A* betekent bijvoorbeeld 'Niet gelijk aan tekst die begint met A'.|  

### <a name="-greater-than"></a>(>) Groter dan  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`>1200`|Nummers groter dan 1200|  

### <a name="-greater-than-or-equal-to"></a>(>=) Groter dan of gelijk aan  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`>=1200`|Nummers groter dan of gelijk aan 1200|  

### <a name="-less-than"></a>(<) Kleiner dan  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`<1200`|Nummers kleiner dan 1200|  

### <a name="-less-than-or-equal-to"></a>(<=) Kleiner dan of gelijk aan  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`<=1200`|Nummers kleiner dan of gelijk aan 1200|  

### <a name="-and"></a>(&) En  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`>200&<1200`|Getallen groter dan 200 en kleiner dan 1200|  

### <a name="-an-exact-character-match"></a>('') Een exacte tekenovereenkomst  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`'man'`|Tekst die exact overeenkomt met man en hoofdlettergevoelig is.|  

### <a name="-case-insensitive"></a>(@) Niet hoofdlettergevoelig  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`@man*`|Tekst die begint met man en niet hoofdlettergevoelig is.|  

### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Een onbeperkt aantal onbekende tekens

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`*Co*`|Tekst die “Co“ bevat en hoofdlettergevoelig is.|  
|`*Co`|Tekst die eindigt met “Co“ en hoofdlettergevoelig is.|  
|`Co*`|Tekst die begint met “Co“ en hoofdlettergevoelig is.|  

> [!NOTE]  
>   U kunt `*` niet gebruiken wanneer u filtert op optievelden (opsommingen), zoals het veld **Status** in verkooporders. Om een filter voor deze veldsoort in te voeren, kunt u de numerieke waarde als een filterparameter invoeren. In het veld **Status** in een verkooporder dat de waarden **Open**, **Vrijgegeven**, **Wacht op goedkeuring** en **Wacht op vooruitbetaling** heeft, gebruikt u de waarden `0`, `1`, `2` en `3` om te filteren op deze opties.

### <a name="-one-unknown-character"></a>(?) Een onbekend teken  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`Hans?n`|Tekst zoals Jansen of Jansma|  

### <a name="combined-format-expressions"></a>Gecombineerde notatiesoorten  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Alle records met het nummer 5999 of een nummer uit het interval 8100 tot en met 8490.|  
|`..1299|1400..`|Records met een nummer kleiner dan of gelijk aan 1299 of gelijk aan 1400 en hoger. Met andere woorden: alle nummers behalve 1300 tot en met 1399.|  
|`>50&<100`|Records met een nummer groter dan 50 en kleiner dan 100, ofwel nummer 51 tot en met 99.|  


## <a name="FilterTokens"> </a>Filtertokens
Wanneer u filtercriteria invoert, kunt u ook woorden typen die een speciale betekenis hebben, filtertokens genaamd. Na het invoeren van het tokenwoord wordt het woord vervangen door de waarde of waarden die het woord vertegenwoordigt. Dit maakt filtering eenvoudiger doordat u niet naar andere pagina's hoeft te navigeren om waarden op te zoeken die u aan uw filter wilt toevoegen. In de onderstaande tabellen worden enkele van de tokens beschreven die u als filtercriteria kunt gebruiken.

> [!TIP]
> Uw organisatie kan aangepaste tokens gebruiken. Als u informatie wilt over de volledige set tokens die voor u beschikbaar zijn of als u aangepaste tokens wilt toevoegen, overlegt u met uw beheerder. Voor technische informatie raadpleegt u [Filtertokens toevoegen](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).


### <a name="me-or-userid-records-assigned-to-you"></a>(%me of %userid) Records die aan u zijn toegewezen

Gebruik `%me` of `%userid` wanneer u velden filtert die de gebruikers-id bevatten, zoals het veld **Toegewezen aan gebruikers-id**, om alle records weer te geven die aan u zijn toegewezen.

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`%me`<br />of<br />`%userid`|Records die aan uw gebruikersaccount zijn toegewezen. |  

### <a name="mycustomers-customers-in-my-customers"></a>(%mycustomers) Klanten in Mijn klanten

Gebruik `%mycustomers` in het veld klant**nr.** om alle records weer te geven voor klanten die deel uitmaken van de lijst **Mijn klanten** in uw rolcentrum.

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`%mycustomers`|Klanten in **Mijn klanten** in uw rolcentrum. |  

### <a name="myitems-items-in-my-items"></a>(%myitems) Artikelen in Mijn artikelen

Gebruik `%myitems` in het veld artikel**nr.** om alle records weer te geven voor artikelen die deel uitmaken van de lijst **Mijn artikelen** in uw rolcentrum.

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`%myitems`|Artikelen in **Mijn artikelen** in uw rolcentrum. |  

### <a name="myvendors-vendors-in-my-vendors"></a>(%myvendors) Leveranciers in Mijn leveranciers

Gebruik `%myvendors` in het veld leveranciers**nr.** om alle records weer te geven voor leveranciers die deel uitmaken van de lijst **Mijn leveranciers** in uw rolcentrum.

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|`%myvendors`|Leveranciers in **Mijn leveranciers** in uw rolcentrum. |  


## <a name="see-also"></a>Zie ook
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Veelgestelde vragen over zoeken en filteren](ui-search-filter-faq.md)
