---
title: Datums en tijden invoeren in Business Central | Microsoft Docs
description: Leren hoe u datums en tijden invoert, inclusief verschillende productiviteitstips, zoals steno, en expressies en bereiken. Lijsten of rapporten filteren op specifieke datums of perioden.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 853a45dc32907c2d9b69f7b2e592dc164c20a094
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757379"
---
# <a name="working-with-calendar-dates-and-times"></a>Werken met agendadatums en -tijden

[!INCLUDE[prod_short](includes/prod_long.md)] biedt meerdere manieren om datums en tijden in te voeren, inclusief krachtige functies die gegevensinvoer versnellen of u helpen complexe agenda-expressies te schrijven. Er zijn verschillende plaatsen in de toepassing waar u datums en tijden in velden kunt invoeren. Bijvoorbeeld in een verkooporder kunt u de verzenddatum instellen. Wanneer u lijsten of rapportgegevens filtert, kunt u datums en tijden invoeren om alleen de gegevens te krijgen waarin u geïnteresseerd bent.

## <a name="check-your-region-and-language-settings"></a>Uw regio- en taalinstellingen controleren
De pagina **Mijn instellingen** geeft de **Regio** en **Taal** op die u in de toepassing gebruikt. Deze instellingen bepalen hoe u datums en tijden invoert.

-   De instelling bij **Regio** bepaalt de weergave of notatie van datums, tijden, nummers en valuta's.

-   Voor datumpatronen met woorden moet de taal van de woorden overeenkomen met de instelling **Taal**.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_long.md)] gebruikt het Gregoriaanse kalendersysteem.

<!--
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a>Datums invoeren

In een datumveld kunt u een datum invoeren met de standaardnotatie voor uw regio-instelling. Verschillende regio's kunnen verschillende scheidingstekens hebben tussen de dagen, maanden en jaren. Sommige regio's gebruiken bijvoorbeeld streepjes (mm-dd-jjjj) en andere gebruiken voorwaartse schuine strepen (mm/dd/jjjj). U kunt echter elk scheidingsteken gebruiken, zelfs een spatie, en de datum wordt automatisch aangepast aan het scheidingsteken dat overeenkomt met uw regio.

De notatie waarin datums in afgedrukte rapporten of ge-e-mailde documenten worden weergegeven, wordt niet beïnvloed door uw persoonlijke keuze van de regio-instelling.

Als u productiever met datums en tijden wilt werken, kunt u elke methode of notatie gebruiken die in de volgende gedeelten wordt beschreven.

### <a name="picking-dates-from-the-calendar"></a>Datums ophalen uit de kalender

Een veld waarbij een kalenderpictogram wordt weergegeven, kan worden ingesteld met de kalenderdatumkiezer. Als u de kalenderdatumkiezer wilt weergeven, activeert u het kalenderpictogram of drukt u op de toetsenbordsneltoets Ctrl+Home in het veld.

![Datumvelden](media/ui-date-field.png "Voorbeeld van een datumveld")

Zie ook [Sneltoetsen in de kalenderdatumkiezer](keyboard-shortcuts.md#calendarshortcuts).

### <a name="day-week-year-pattern"></a>Dag\-week\-jaar patroon

U kunt een datum als dag van de week invoeren, gevolgd door een weeknummer en desgewenst een jaar. Bijvoorbeeld Maa25 of maa25 betekent maandag in week 25. Als u geen jaar invoert, wordt het jaar van de werkdatum gebruikt.

U kunt in plaats van het volledige woord voor de dag van de week een deel van het woord invoeren, vanaf het begin. In het geval van conflicten (zoals met z, wat zowel zaterdag als zondag kan zijn), worden de dagen geëvalueerd op basis van de instellingen van de regio. De invoer wordt ook eerst geëvalueerd tegen werkdatum en vandaag, dus houd daar rekening mee wanneer u afkortingen gebruikt. v betekent bijvoorbeeld al vandaag, dus het kan niet ook vrijdag betekenen.

Het schema van het weeknummer is altijd ISO 8601, waar week 1 de week met 4 januari erin is of de week met de eerste donderdag van het jaar.

### <a name="digit-patterns"></a>Cijferpatronen

Een datumveld kan twee, vier, zes of acht cijfers bevatten:

-   Als u slechts twee cijfers invoert, wordt dit als een dag beschouwd en wordt de maand en het jaar van de werkdag automatisch toegevoegd.

-   Als u vier cijfers invoert, wordt dit als een dag en een maand beschouwd en wordt het jaar van de werkdag automatisch toegevoegd. De volgorde van de dag en de maand wordt bepaald door uw regio-instellingen. Zelfs als uw regio-instellingen het jaar vóór de dag en de maand bevatten, worden vier cijfers geïnterpreteerd als de dag en de maand.

-   Als de ingevoerde datum in de reeks 01.01.1930 tot en met 31.12.2029 valt, hoeft u slechts twee cijfers voor het jaartal in te voeren; anders moet u vier cijfers voor het jaartal invoeren.

### <a name="today"></a>Vandaag

Voer voor vandaag in de taal die is ingesteld door **Taal**, het woord in waarmee de datum op de huidige datum wordt ingesteld. In plaats van het hele woord in te voeren kunt u een deel van het woord invoeren, te beginnen met het begin, bijvoorbeeld v of van, zolang het niet ook het begin van een ander woord is.

### <a name="period"></a>Periode

Als u wilt filteren op een specifieke boekingsperiode, voert u in een datumveld de letter p of het woord periode in, gevolgd door een nummer dat de boekingsperiode aangeeft, zoals p2 of periode4. De boekhoudperiode is relatief aan het boekjaar van de huidige werkdatum die u instelt in uw rolcentrum. Als de werkdatum bijvoorbeeld **21.3.20** is, wordt met p1 of alleen p gefilterd op de eerste boekingsperiode van het boekjaar 2020 (bijvoorbeeld 1.1.20..31.1.20). Met p15 wordt gefilterd op de vijftiende boekingsperiode vanaf het begin van het boekjaar 2020 (bijvoorbeeld 1.3.21..31.3.21).

De boekhoudperioden worden gedefinieerd op de pagina **Boekingsperioden**. Als u de boekingsperioden wilt weergeven of wijzigen, opent u de pagina [hier](https://businesscentral.dynamics.com/?page=100).

### <a name="current-work-date"></a>Huidige werkdatum

Met de werkdatumfunctie kunt u transacties vastleggen met een datum die afwijkt van de huidige datum.

Het woord voor 'werkdatum' in de taal die is ingesteld door de instelling **Taal**, stelt de datum in op de huidige ingestelde werkdatum die wordt opgegeven op de pagina **Mijn instellingen**. U kunt in plaats van het volledige woord een deel van het woord invoeren, vanaf het begin, bijvoorbeeld 'w' of 'werk'.

Als u geen werkdatum hebt gedefinieerd, wordt de huidige datum als de werkdatum gebruikt. Het gebruik van een werkdatum is handig als u veel transacties hebt met een andere datum dan de huidige.

Zie ook [Basisinstellingen wijzigen, zoals de werkdatum](ui-change-basic-settings.md#work-date).

### <a name="closing-date"></a>Ultimodatum

Als u een boekjaar afsluit, kunt u ultimodatums gebruiken om aan te geven dat het om een ultimopost gaat. Een ultimodatum ligt technisch gezien tussen twee datums in, zoals tussen 31 december en 1 januari.

Als u een datum wilt opgeven die een ultimodatum is, plaatst u U vlak vóór de datum, bijvoorbeeld U311201. Dit kan in combinatie met alle datumpatronen worden gebruikt.

### <a name="examples"></a>Voorbeelden

De volgende tabel bevat voorbeelden van datums met alle indelingen. Er wordt uitgegaan van regio-instellingen die datums noteren volgens: **jaar.maand.dag.**, een week na maandag en de Engelse taal.

|**Invoer**      |**Interpretatie**      |
|---------------|------------------------|
|2018.12.31.|31.12.2018.|
|181231|31.12.2018.|
|18.12.31.|31.12.2018.|
|18.12.31.|31.12.2018.|
|20181231|31.12.2018.|
|18/12,31|31.12.2018.|
|11|jaar van werkdatum.maand van werkdatum.11.|
|1112|jaar van werkdatum.11.12.|
|h of huidige datum|datum van vandaag|
|p4|datumbereik dat de vierde boekhoudperiode bevat, bijvoorbeeld 1.4.20..30.4.20|
|w of werkdatum|de werkdatum|
|ma of maandag|Maandag van de werkdatumweek|
|di of dinsdag|Dinsdag van de werkdatumweek|
|za of zaterdag|Zaterdag van de werkdatumweek|
|z of zondag|Zondag van de werkdatumweek|
|d23|Dinsdag van week 23 van het werkdatumjaar|
|d 23|Dinsdag van week 23 van het werkdatumjaar|
|d-1|Dinsdag van week 1 van het werkdatumjaar|

##  <a name="setting-ranges"></a><a name="BKMK_SettingDateRanges"></a> Datumbereiken instellen

In lijsten, totalen en rapporten kunt u filters instellen op datum, tijden en datumtijden. De filters kunnen een begindatum en desgewenst een einddatum bevatten om alleen de gegevens uit dat bereik weer te geven. Voor het instellen van een datumbereik gelden de standaardregels.

|**Betekenis**|**Voorbeeldexpressie (datum)**|**Gegevens opgenomen in het filter**|
|-----------|---------------------|--------------------|
|Interval|15.12.00..15.01.01<br /><br />..15.12.00<br /><br />p1..p4|Records met datums tussen 15.12.00 en 15.01.01.<br /><br />Records met datums van 15.12.00 of eerder.<br /><br />Datumbereik dat de tweede, derde en vierde boekhoudperiode bevat, bijvoorbeeld 1.1.20..30.4.20..|
|Of/of|12 15 00\|12 16 00|Records met datums van of 15.12.00 of 16.12.00. Als er records zijn met datums op beide dagen, worden ze allemaal weergegeven.|
|Combinatie|12 15 00\|12 01 00..12 10 00  <br /><br />..12 14 00\|12 30 00..|Records met datums van 15.12.00 of op datums in de periode 01.12.00 t/m 10.12.00.  <br /><br />Records met datums van 12-14 00 of eerder, of datums van 12 30 00 of later. Dit wil zeggen, alle records, behalve records met datums tussen 12 15 00 en 12 29 00.|

U kunt iedere geldige indeling in datumbereikfilters gebruiken. Bijvoorbeeld maa14 3..v 4p, toegepast op een datum/tijd-veld leidt tot een filter van 3 uur 's morgens op maandag, in week 14 van het huidige werkdatumjaar tot en met vandaag om 4 uur 's middags.

## <a name="using-date-formulas"></a>Datumformules gebruiken
Een datumformule is een korte, afgekorte combinatie van letters en cijfers op basis waarvan datums worden berekend. U kunt datumformules invoeren in verschillende datumberekeningsvelden of -filters.

> [!NOTE]
>  In alle datumformulevelden wordt automatisch één dag opgenomen om ervoor te zorgen dat de huidige dag wordt gebruikt als begindatum van de periode. Als u dus bijvoorbeeld 1W invoert, zal de periode in feite acht dagen bestrijken omdat vandaag ook wordt opgenomen. Als u een periode van zeven dagen \(exact één week\) wilt opgeven, inclusief de begindatum van de periode, moet u 6D of 1W-1D opgeven.

Hier volgen enkele voorbeelden van het gebruik van datumformules:

-   De datumformule in de frequentievelden van periodieke dagboeken geeft aan hoe vaak de dagboekregel moet worden geboekt.

-   De datumformule in het veld **Respijtperiode** van een bepaald aanmaningsniveau bepaalt hoelang de vervaldatum \(of de datum van de vorige aanmaning\) moet zijn verstreken voordat een aanmaning wordt gemaakt.

-   De datumformule in het veld **Vervaldatumformule** bepaalt hoe de vervaldatum voor de aanmaning wordt berekend.

De datumformule kan maximaal 20 tekens bevatten (cijfers en letters). U kunt de volgende letters gebruiken als afkorting voor kalendereenheden.

|  Letter  |  Betekenis  |
|----------|----------------------|
|H|Huidig|
|D|Dag\(en\)|
|W|We(e)k\(en\)|
|M|Maand\(en\)|
|K|Kwarta(a)l\(en\)|
|J|Ja(a)r\(en\)|

Er zijn drie soorten datumformules.

In het volgende voorbeeld wordt weergegeven hoe H kan worden gebruikt voor huidig en een tijdseenheid.

|  Expressie  |  Betekenis  |
|--------------|-----------|
|LW|Lopende week|
|LM|Lopende maand|

In het volgende voorbeeld wordt weergegeven hoe een getal en een tijdseenheid moet worden gebruikt. Nummers mogen niet groter zijn dan 9999.

|  Expressie  |  Betekenis  |
|--------------|-----------|
|10D|10 dagen vanaf vandaag|
|2W|2 weken vanaf vandaag|

In het volgende voorbeeld wordt weergegeven hoe een tijdseenheid en een getal moet worden gebruikt.

|  Expressie  |  Betekenis  |
|--------------|-----------|
|D10|De volgende tiende dag van een maand|
|WD4|De volgende vierde dag van een week \(donderdag\)|

Het volgende voorbeeld geeft weer hoe u deze drie soorten naar wens kunt combineren.

|  Expressie  |  Betekenis  |
|--------------|-----------|
|LM+10D|Lopende maand \+ 10 dagen|

In het volgende voorbeeld ziet u hoe u een minteken gebruikt om een datum in het verleden aan te duiden.

|  Expressie  |  Betekenis  |
|--------------|-----------|
|-1J|1 jaar geleden vanaf vandaag|

> [!IMPORTANT]
>  Als de vestiging een basisagenda gebruikt, wordt de datumformule die u invoert in dit veld, bijvoorbeeld het veld **Verzendtijd** beschouwd als agendawerkdag. Bijvoorbeeld: 1W betekent zeven werkdagen.
<!--
# Entering Date Ranges
You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges. Let's take the **Customer Top 10** as an example:

![Setting a date range in the request page for the Customer Top 10 list](./media/ui-enter-date-ranges/customer-top10-list.png)

Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want. To set date ranges, you enter dates and then use either **..** or **|** to set the range. In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.
Here are a couple of other examples:

| Meaning | Example | Entries included |
|---|---|---|
|Equal to| 12 15 16 |Only those posted on December 15 2016.|
|Interval| 12 15 16..01 15 17<br /><br />..12 15 16|Those posted on dates between and including December 15 2016 and January 15 2017.<br /><br />Those posted on December 15 2016 or earlier.|
|Either/or|12 15 16&#124;12 16 16|Those posted on either December 15 or December 16 2016. If there are entries posted on both days, they will all be displayed.|

You can also combine the various format types.

| Example | Entries included |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017. |
|..12 14 16&#124;12 30 16.. | Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29. |

Note that we have used the US date format MMDDYY here. As [!INCLUDE[prod_short](includes/prod_short.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

## Using Date Formulas
A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.

> [!NOTE]
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.

Here are some examples of how date formulas can be used:

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.

-   The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.

-   The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.

The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.

|  Letter  |  Time specification  |
|----------|----------------------|
|C|Current|
|D|Day\(s\)|
|W|Week\(s\)|
|M|Month\(s\)|
|Q|Quarter\(s\)|
|Y|Year\(s\)|

You can construct a date formula in three ways.

The following example shows how to use **C**, for current, and a time unit.

|  Expression  |  Meaning  |
|--------------|-----------|
|CW|Current week|
|CM|Current month|

The following example shows how to use a number and a time unit. A number cannot be larger than 9999.

|  Expression  |  Meaning  |
|--------------|-----------|
|10D|10 days from today|
|2W|2 weeks from today|

The following example shows how to use a time unit and a number.

|  Expression  |  Meaning  |
|--------------|-----------|
|D10|The next 10th day of a month|
|WD4|The next 4th day of a week \(Thursday\)|

The following example shows how you can combine these three forms as needed.

|  Expression  |  Meaning  |
|--------------|-----------|
|CM\+10D|Current month \+ 10 days|

The following example shows how you can use a minus sign to indicate a date in the past.

|  Expression  |  Meaning  |
|--------------|-----------|
|-1Y|1 year ago from today|

> [!IMPORTANT]
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, **1W**  means seven working days.

-->

## <a name="entering-times"></a>Tijden invoeren
Wanneer u tijden invoert, kunt u alle gewenste niet-spatie scheidingstekens invoegen tussen de eenheden, maar als u dubbele cijfers gebruikt voor elke eenheid tot aan milliseconden, is het niet vereist.

U hoeft de alleen grootste eenheden te gebruiken die u nodig hebt. De rest wordt op nul ingesteld. U kunt de AM/PM-indicator ook weglaten.

In de volgende tabel wordt aangegeven op welke manieren u tijden kunt invoeren en hoe de invoer wordt geïnterpreteerd. Er wordt uitgegaan van een regio-instelling die tijden noteert volgens: **Uren:Minuten:Seconden.Milliseconden.** en die respectievelijk de indicatoren 'AM' en 'PM' gebruikt.

|**Invoer**      |**Interpretatie**      |
|---------------|------------------------|
|05:23:17|05:23:17|
|5|05:00:00|
|5AM|05:00:00|
|5P|17:00:00|
|12|12:00:00|
|12A|00:00:00|
|12P|12:00:00|
|17|17:00:00|
|5:30|05:30:00|
|0530|05:30:00|
|5:30:5|05:30:05|
|053005|05:30:05|
|5:30:5.50|05:30:05,5|
|053005050|05:30:05.05|

Houd er rekening mee dat milliseconden als decimale notatie worden geïnterpreteerd. Bijvoorbeeld 3, 30 en 300 betekenen allemaal 300 milliseconden, en 03 betekent 30 en 003 betekent 3 milliseconden.

U kunt 24:00 niet voor middernacht gebruiken of een waarde groter dan 24:00 gebruiken.

Het woord voor 'tijd' in de taal die [!INCLUDE[prod_short](includes/prod_long.md)] gebruikt, wordt geëvalueerd als de huidige tijd op uw computer of mobiele apparaat. U kunt elk deel van het woord invoeren, beginnend bij het begin, zoals t of TIJ.

## <a name="entering-combined-dates-and-times"></a>Gecombineerde datums en tijden invoeren
Wanneer u een datumtijd invoert (een datum en een tijd gecombineerd tot één veld), moet u een spatie invoeren tussen de datum en de tijd. Het datumdeel kan alleen spaties in de vorm van het officiële datumscheidingsteken van uw regio-instellingen bevatten. De tijd kan spaties bevatten rond de AM/PM-indicator.

Het is ook mogelijk alleen een datum in een datumtijdveld in te voeren, maar u kunt niet alleen een tijd invoeren.

In de volgende tabel staan enkele voorbeelden van datum/tijd-combinaties. Met de regio-instellingen in de voorbeelden worden datums weergegeven in de notatie dag\-maand\-jaar, met AM/PM-indicatoren, Engelse taal en zondag als begin van de week.

|**Invoer**      |**Interpretatie**      |
|---------------|------------------------|
|08-01-2016 05:48:12 PM|08.01.2016 17:48:12|
|131202 132455|13.12.2002 13:24:55|
|1-12-02 10|01.12.2002 10:00:00|
|1.12.02 5|01.12.2002 05:00:00|
|1.12.02|01.12.2002 00:00:00|
|11 12|11.werkdatummaand.werkdatumjaar 12:00:00|
|1112 12|11.12.werkdatumjaar 12:00:00|
|h of huidige datum|huidige datum 00:00:00|
|h 10:30|huidige datum 10:30:00|
|h 3:3:3|huidige datum 03:03:03|
|w of werkdatum|de werkdatum 00:00:00|
|ma of maandag|Maandag van de werkdatumweek 00:00:00|
|di of dinsdag|Dinsdag van de werkdatumweek 00:00:00|
|za of zaterdag|Zaterdag van de werkdatumweek 00:00:00|
|z of zondag|Zondag van de werkdatumweek 00:00:00|
|di 10:30|Dinsdag van de werkdatumweek 10:30:00|
|di 3:3:3|Dinsdag van de werkdatumweek 03:03:03|
|d23 t|Dinsdag van week 23 van het werkdatumjaar huidige tijd van dag|
|d23|Dinsdag van week 23 van het werkdatumjaar|
|d 23|Vandaag 23:00:00|
|d-1|Dinsdag van week 1 van het werkdatumjaar|

## <a name="entering-duration"></a>Duur invoeren
Sommige velden in toepassingsmodule vertegenwoordigen een duur of hoeveelheid verstreken tijd, in plaats van een specifieke datum of tijd. De duur moet worden ingevoerd als een getal gevolgd door de eenheid.

Hier volgen enkele voorbeelden.

|**Duur**|**Eenheid**|
|------------|-------------------|
|2u|2 uur|
|6u 30 m|6 uur en 30 minuten|
|6,5u|6 uur en 30 minuten|
|90m|1 uur en 30 minuten|
|2d 6u 30m|2 dagen, 6 uur en 30 minuten|
|2d 6u 30m 56s 600ms|2 dagen, 6 uur, 30 minuten, 56 seconden en 600 milliseconden|

U kunt ook een getal invoeren, dat automatisch naar een duur wordt geconverteerd. Dit gebeurt op basis van de standaardeenheid die in het veld Duur is ingevoerd.

Als u wilt nagaan welke eenheid wordt gebruikt in het veld Duur, voert u een getal in en bekijkt u in welke eenheid het getal wordt omgezet.

Als de maateenheid bijvoorbeeld uren is, wordt het getal 5 bijvoorbeeld naar 5 uur geconverteerd.

## <a name="see-also"></a>Zie ook
[Werken met [!INCLUDE[prod_short](includes/prod_long.md)]](ui-work-product.md)  
[Datumberekening voor inkoop](purchasing-date-calculation-for-purchases.md)  
[Criteria in filters invoeren](ui-enter-criteria-filters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]