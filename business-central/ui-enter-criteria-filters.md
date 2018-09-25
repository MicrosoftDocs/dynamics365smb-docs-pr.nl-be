---
title: Gegevens zoeken en filtercriteria invoeren | Microsoft Docs
description: Beschrijft hoe u met filters werkt, zoals het Snelfilter, om de resultaten te verfijnen die u krijgt wanneer u gegevens zoekt.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d0ef9148b082b05a46283f89c3cb98bb1cd0c6d0
ms.openlocfilehash: 10aac3906d9da8b9e0791db614142eeb90940a9b
ms.contentlocale: nl-be
ms.lasthandoff: 08/06/2018

---
# <a name="searching-filtering-and-sorting-data"></a>Gegevens zoeken, filteren en sorteren
U kunt een paar dingen doen om records in een lijst te vinden, te lokaliseren en te scannen. U kunt de records bijvoorbeeld sorteren, doorzoeken en filteren.

Wanneer u naar gegevens, zoals klantnamen, adressen of productgroepen wilt zoeken, voert u criteria in. In zoekcriteria kunt u alle cijfers en letters gebruiken die u normaal in het specifieke veld gebruikt. Daarnaast kunt u speciale symbolen gebruiken om de resultaten verder te filteren. U kunt op twee manieren zoeken: met het snelfilter of kolomfilters.

## <a name="sorting"></a>Sorteervolgorde
Met de sorteerfunctie krijgt u snel een overzicht van de gegevens. Als u veel klanten hebt, kunt u er bijvoorbeeld voor kiezen hen te sorteren op **Klantnr.**, **Klantboekingsgroep**, **Valutacode**, **Land-/regiocode** of **Btw-nummer** voor het door u gewenste overzicht.

Als u een lijst wilt sorteren, kunt u een kolomkoptekst kiezen om te schakelen tussen op- en aflopend, of de kleine pijl-omlaag in de kolomkop kiezen en vervolgens **Oplopend** of **Aflopend** kiezen.  

> [!NOTE]  
>   Sorteren wordt niet ondersteund bij afbeeldingen, BLOB-velden, FlowFilters en velden die niet deel van een tabel zijn.  

## <a name="searching-by-using-the-quick-filter"></a>Zoeken met het snelfilter
U kunt filters toevoegen aan alle pagina's met het Snelfilter. Het Snelfilter wordt ingeschakeld door het vergrootglaspictogram in de rechterbovenhoek van een pagina te kiezen. Dit type filter wordt gebruikt voor een snelle invoer van criteria.

> [!IMPORTANT]  
>   Het snelfilter biedt een eenvoudig toegang tot filtergegevens door onbewerkte tekst in te voeren, maar biedt ook veel opties voor zoekcriteria. Afhankelijk van of u normale tekst of tekst met symbolen invoert, werkt het snelfilter anders.  

* Als u gewone tekst in de zoekcriteria opgeeft, worden de zoekcriteria geïnterpreteerd als een hoofdletterongevoelige zoekactie die bepaalde tekst bevat.  
* Als u tekst inclusief symbolen in de zoekcriteria opgeeft, worden de zoekcriteria precies zo geïnterpreteerd als u ze hebt ingevoerd en wordt onderscheid gemaakt tussen hoofdletters en kleine letters.

### <a name="quick-filter-criteria"></a>Snelfiltercriteria
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH>Zoekcriteria</TH>
    <TH>Geïnterpreteerd als...</TH>
    <TH>Retourneert...</TH>
  </TR>
  <TR>
    <TD>man</TD>
    <TD>@&#42;man&#42;</TD>
    <TD>Alle records met de tekst <b>man</b> en ongevoelig voor hoofdletters en kleine letters.</TD>
  </TR>
  <TR>
    <TD>se</TD>
    <TD>@&#42;zo&#42;</TD>
    <TD>Alle records met de tekst <b>se</b> en ongevoelig voor hoofdletters en kleine letters.</TD>
  </TR>
  <TR>
    <TD>Man&#42;</TD>
    <TD>Begint met <b>Man</b> en is hoofdlettergevoelig.</TD>
    <TD>Alle records die beginnen met de tekst <b>Man</b>.</TD>
  </TR>
  <TR>
    <TD>'man'</TD>
    <TD>Een exacte tekst en gevoelig voor hoofdletters en kleine letters.</TD>
    <TD>Alle records die precies overeenkomen met <b>man</b>.</TD>
  </TR>
  <TR>
    <TD>@man* </TD>
    <TD>Begint met en is niet hoofdlettergevoelig.</TD>
    <TD>Alle records die beginnen met <b>man</b>.</TD>
  </TR>
    <TR>
    <TD>@&#42;man</TD>
    <TD>Eindigt met en is niet hoofdlettergevoelig.</TD>
    <TD>Alle records die eindigen met <b>man</b>.</TD>
  </TR>
</TABLE>

> [!NOTE]  
>   U kunt geen jokerteken gebruiken bij het filteren op opsommingsvelden, zoals het veld **Status** op verkooporders. Om een filter voor deze veldsoort in te voeren, kunt u de numerieke waarde als een filterparameter invoeren. Bijvoorbeeld: gebruik in het veld **Status** op een verkooporder met de waarden **Open**, **Vrijgegeven**, **Wacht op goedkeuring** en **Wacht op vooruitbetaling** de waarden **0**, **1**, **2** en **3** om voor deze opties te filteren.

## <a name="searching-by-using-column-filters"></a>Zoeken met kolomfilters
U kunt een filter toevoegen aan een of meer kolommen in een lijst. Kolomfilters bieden een meer flexibele en geavanceerde methode dan het snelfilter.

### <a name="to-add-a-filter-on-a-column"></a>Een filter toevoegen aan een kolom
1.  Voordat u een filter toevoegt, klikt u op het pictogram ![Als overzicht weergeven](media/ui_show_as_list_icon.png "pijl-links Als overzicht weergeven") om de weergave te wijzigen.
2. Kies de pijl-omlaag in de kolomkop en kies **Filter**.
3. Ga op een van de volgende manieren te werk:
  -  Kies *...* naast het vak om een waarde in de lijst te selecteren.
  -  Voer filtercriteria in het vak in. Zie het volgende gedeelte voor details.
4. Kies de knop **OK**.

## <a name="FilterCriteria"> </a>Filtercriteria en -symbolen
U kunt bij de invoer van criteria alle cijfers en letters gebruiken die u normaal ook kunt gebruiken. Daarnaast kunt u speciale symbolen gebruiken om de resultaten verder te filteren. De volgende tabellen bevatten de tekens die in filters kunnen worden gebruikt.  

> [!IMPORTANT]  
>  Het kan voorkomen dat veldwaarden deze symbolen bevatten en u hierop wilt filteren. Hiervoor moet u de filterexpressie opnemen die het symbool tussen aanhalingstekens (“) bevat. Als u wilt filteren op records die beginnen met de tekst *S&R*, is de filterexpressie bijvoorbeeld **'S&R*'**.  

### <a name="-interval"></a>(..) Interval  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|1.100..2.100|Nummers 1100 t/m 2100|  
|..2.500|Tot en met 2500|  
|..31 12 00|Datums tot en met 31.12.00|  
|P8..|Gegevens voor boekhoudperiode 8 en verder|  
|..23|Van begindatum tot 23 lopende maand, lopend jaar 23:59:59|  
|23..|Van 23 lopende maand, lopend jaar 00:00:00 tot eindtijd|  
|22..23|Van 22 lopende maand, lopend jaar 0:00:00 tot 23 lopende maand, lopend jaar 23:59:59|  

### <a name="124-eitheror"></a>(&#124;) Of/of  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|1200&#124;1300|Nummers met 1200 of 1300|  

### <a name="-not-equal-to"></a>(<>) Niet gelijk aan  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|<>0|Alle nummers behalve 0<br /><br /> Met de SQL Server-optie kunt u dit teken combineren met jokertekens. <>A* betekent bijvoorbeeld 'Niet gelijk aan tekst die begint met A'.|  

### <a name="-greater-than"></a>(>) Groter dan  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|>1.200|Nummers groter dan 1200|  

### <a name="-greater-than-or-equal-to"></a>(>=) Groter dan of gelijk aan  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|>=1.200|Nummers groter dan of gelijk aan 1200|  

### <a name="-less-than"></a>(<) Kleiner dan  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|<1.200|Nummers kleiner dan 1200|  

### <a name="-less-than-or-equal-to"></a>(<=) Kleiner dan of gelijk aan  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|<=1.200|Nummers kleiner dan of gelijk aan 1200|  

### <a name="-and"></a>(&) En  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|>200&<1200|Getallen groter dan 200 en kleiner dan 1200|  

### <a name="-an-exact-character-match"></a>('') Een exacte tekenovereenkomst  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|'man'|Tekst die exact overeenkomt met man en hoofdlettergevoelig is.|  

### <a name="-case-insensitive"></a>(@) Niet hoofdlettergevoelig  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|@man*|Tekst die begint met man en niet hoofdlettergevoelig is.|  

### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Een onbeperkt aantal onbekende tekens  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|*Co*|Tekst die “Co“ bevat en hoofdlettergevoelig is.|  
|*Be|Tekst die eindigt met “Co“ en hoofdlettergevoelig is.|  
|Be*|Tekst die begint met “Co“ en hoofdlettergevoelig is.|  

### <a name="-one-unknown-character"></a>(?) Een onbekend teken  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|Jans?n|Tekst zoals Jansen of Jansma|  

### <a name="combined-format-expressions"></a>Gecombineerde notatiesoorten  

|Voorbeeld|Weergegeven records|  
|-----------------------|-----------------------|  
|5999&#124;8100..8490|Alle records met het nummer 5999 of een nummer uit het interval 8100 tot en met 8490.|  
|..1299&#124;1400..|Records met een nummer kleiner dan of gelijk aan 1299 of gelijk aan 1400 en hoger. Met andere woorden: alle nummers behalve 1300 tot en met 1399.|  
|>50&<100|Records met een nummer groter dan 50 en kleiner dan 100, ofwel nummer 51 tot en met 99.|  

## <a name="see-also"></a>Zie ook
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

