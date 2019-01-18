---
title: Datums en tijden invoeren in Business Central | Microsoft Docs
description: Leren hoe u datums en tijden invoert, inclusief verschillende productiviteitstips, zoals steno, en expressies en bereiken. Lijsten of rapporten filteren op specifieke datums of perioden.
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter, calendar, shorthand, range
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 54466c381bbeb3653a239920c00dd6f45536d9e3
ms.contentlocale: nl-be
ms.lasthandoff: 11/22/2018

---

# <a name="working-with-calendar-dates-and-times"></a><span data-ttu-id="71fd5-104">Werken met agendadatums en -tijden</span><span class="sxs-lookup"><span data-stu-id="71fd5-104">Working with Calendar Dates and Times</span></span>

[!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="71fd5-105">biedt meerdere manieren om datums en tijden in te voeren, inclusief krachtige functies die gegevensinvoer versnellen of u helpen complexe agenda-expressies te schrijven.</span><span class="sxs-lookup"><span data-stu-id="71fd5-105">offers multiple ways to enter dates and times, including powerful features that accelerate data entry, or help you write complex calendar expressions.</span></span> <span data-ttu-id="71fd5-106">Er zijn verschillende plaatsen in de toepassing waar u datums en tijden in velden kunt invoeren.</span><span class="sxs-lookup"><span data-stu-id="71fd5-106">There are various places throughout the application where you can enter dates and times in fields.</span></span> <span data-ttu-id="71fd5-107">Bijvoorbeeld in een verkooporder kunt u de verzenddatum instellen.</span><span class="sxs-lookup"><span data-stu-id="71fd5-107">For example, on a sales order, you can set the shipment date.</span></span> <span data-ttu-id="71fd5-108">Wanneer u lijsten of rapportgegevens filtert, kunt u datums en tijden invoeren om alleen de gegevens te krijgen waarin u geïnteresseerd bent.</span><span class="sxs-lookup"><span data-stu-id="71fd5-108">When filtering lists or report data, you can enter dates and times to pinpoint only the data that you are interested in.</span></span>

## <a name="check-your-region-and-language-settings"></a><span data-ttu-id="71fd5-109">Uw regio- en taalinstellingen controleren</span><span class="sxs-lookup"><span data-stu-id="71fd5-109">Check your region and language settings</span></span>

<span data-ttu-id="71fd5-110">Op de pagina [**Mijn instellingen**](https://businesscentral.dynamics.com?page=9176 " Ga direct naar de pagina met uw gebruikersinstellingen in Business Central") worden de **Regio** en de **Taal** opgegeven die u in de toepassing gebruikt.</span><span class="sxs-lookup"><span data-stu-id="71fd5-110">The [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page specifies the **Region** and **Language** that you are using in the application.</span></span> <span data-ttu-id="71fd5-111">Deze instellingen bepalen hoe u datums en tijden invoert.</span><span class="sxs-lookup"><span data-stu-id="71fd5-111">These settings influence how you enter dates and times.</span></span> 

-   <span data-ttu-id="71fd5-112">De instelling bij **Regio** bepaalt de weergave of notatie van datums, tijden, nummers en valuta's.</span><span class="sxs-lookup"><span data-stu-id="71fd5-112">The **Region** setting determines how dates, times, numbers, and currencies are shown or formatted.</span></span>

-   <span data-ttu-id="71fd5-113">Voor datumpatronen met woorden moet de taal van de woorden overeenkomen met de instelling **Taal**.</span><span class="sxs-lookup"><span data-stu-id="71fd5-113">For date patterns that involve words, the language of the words that you use must correspond to the **Language** setting.</span></span>

> [!NOTE]
> [!INCLUDE[d365fin](includes/d365fin_long_md.md)] <span data-ttu-id="71fd5-114">gebruikt het Gregoriaanse kalendersysteem.</span><span class="sxs-lookup"><span data-stu-id="71fd5-114">uses the Gregorian calendar system.</span></span>

<!-- 
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a><span data-ttu-id="71fd5-115">Datums invoeren</span><span class="sxs-lookup"><span data-stu-id="71fd5-115">Entering Dates</span></span>

<span data-ttu-id="71fd5-116">In een datumveld kunt u een datum invoeren met de standaardnotatie voor uw regio-instelling.</span><span class="sxs-lookup"><span data-stu-id="71fd5-116">In a date field, you can enter a date using the standard format for your region setting.</span></span> <span data-ttu-id="71fd5-117">Verschillende regio's kunnen verschillende scheidingstekens hebben tussen de dagen, maanden en jaren.</span><span class="sxs-lookup"><span data-stu-id="71fd5-117">Different regions can use different separators between the days, months and years.</span></span> <span data-ttu-id="71fd5-118">Sommige regio's gebruiken bijvoorbeeld streepjes (mm-dd-jjjj) en andere gebruiken voorwaartse schuine strepen (mm/dd/jjjj).</span><span class="sxs-lookup"><span data-stu-id="71fd5-118">For example, some regions use dashes (mm-dd-yyyy) and others use forward slashes (mm/dd/yyyy).</span></span> <span data-ttu-id="71fd5-119">U kunt echter elk scheidingsteken gebruiken, zelfs een spatie, en de datum wordt automatisch aangepast aan het scheidingsteken dat overeenkomt met uw regio.</span><span class="sxs-lookup"><span data-stu-id="71fd5-119">However, you can use any separators, even a space, and the date will automatically be changed to use separators that match your region.</span></span>

<span data-ttu-id="71fd5-120">De notatie waarin datums in afgedrukte rapporten of ge-e-mailde documenten worden weergegeven, wordt niet beïnvloed door uw persoonlijke keuze van de regio-instelling.</span><span class="sxs-lookup"><span data-stu-id="71fd5-120">Note that the format in which dates are displayed on printed reports or emailed documents is not influenced by your personal choice of region setting.</span></span>

<span data-ttu-id="71fd5-121">Als u productiever met datums en tijden wilt werken, kunt u elke methode of notatie gebruiken die in de volgende gedeelten wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="71fd5-121">To work more productively with dates and times, you can use any of the methods or formats that are described in the following sections.</span></span> 

### <a name="picking-dates-from-the-calendar"></a><span data-ttu-id="71fd5-122">Datums ophalen uit de kalender</span><span class="sxs-lookup"><span data-stu-id="71fd5-122">Picking dates from the calendar</span></span>

<span data-ttu-id="71fd5-123">Een veld waarbij een kalenderpictogram wordt weergegeven, kan worden ingesteld met de kalenderdatumkiezer.</span><span class="sxs-lookup"><span data-stu-id="71fd5-123">Any field displaying a calendar icon can be set using the calendar date picker.</span></span> <span data-ttu-id="71fd5-124">Als u de kalenderdatumkiezer wilt weergeven, activeert u het kalenderpictogram of drukt u op de toetsenbordsneltoets Ctrl+Home in het veld.</span><span class="sxs-lookup"><span data-stu-id="71fd5-124">To display the calendar date picker, activate the calendar icon or press the Ctrl + Home keyboard shortcut in the field.</span></span>

<span data-ttu-id="71fd5-125">![Datumvelden](media/ui-date-field.png "Voorbeeld van een datumveld")</span><span class="sxs-lookup"><span data-stu-id="71fd5-125">![Date fields](media/ui-date-field.png "Example of a date field")</span></span>

<span data-ttu-id="71fd5-126">Zie ook [Toetsenbordsneltoetsen in de kalenderdatumkiezer](keyboard-shortcuts.md#calendarshortcuts)</span><span class="sxs-lookup"><span data-stu-id="71fd5-126">See also [Keyboard Shortcuts in the calendar date picker](keyboard-shortcuts.md#calendarshortcuts)</span></span>

### <a name="day-week-year-pattern"></a><span data-ttu-id="71fd5-127">Dag\-week\-jaar patroon</span><span class="sxs-lookup"><span data-stu-id="71fd5-127">Day\-week\-year pattern</span></span>

<span data-ttu-id="71fd5-128">U kunt een datum als dag van de week invoeren, gevolgd door een weeknummer en desgewenst een jaar.</span><span class="sxs-lookup"><span data-stu-id="71fd5-128">You can enter a date as a weekday followed by a week number and, optionally, a year.</span></span> <span data-ttu-id="71fd5-129">Bijvoorbeeld `Mon25` of `mon25` betekent maandag in week 25.</span><span class="sxs-lookup"><span data-stu-id="71fd5-129">For example, `Mon25` or `mon25` means Monday in week 25.</span></span> <span data-ttu-id="71fd5-130">Als u geen jaar invoert, wordt het jaar van de werkdatum gebruikt.</span><span class="sxs-lookup"><span data-stu-id="71fd5-130">If you do not enter a year, the year of the work date is used.</span></span>

<span data-ttu-id="71fd5-131">U kunt in plaats van het volledige woord voor de dag van de week een deel van het woord invoeren, vanaf het begin.</span><span class="sxs-lookup"><span data-stu-id="71fd5-131">Instead of entering the entire word for the day of the week, you can enter part of the word, starting from the beginning.</span></span> <span data-ttu-id="71fd5-132">In het geval van conflicten (zoals met `s`, wat zowel Saturday als Sunday kan zijn), worden de dagen geëvalueerd op basis van de instellingen van de regio.</span><span class="sxs-lookup"><span data-stu-id="71fd5-132">In case of conflicts (such as with `s` which could be Saturday or Sunday), the days are evaluated according to the region setting.</span></span> <span data-ttu-id="71fd5-133">De invoer wordt ook eerst geëvalueerd tegen `workdate` en `today`, dus houd daar rekening mee wanneer u afkortingen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="71fd5-133">The input is first evaluated against `workdate` and `today` as well, so keep this in mind when abbreviating.</span></span> <span data-ttu-id="71fd5-134">`t` betekent bijvoorbeeld al vandaag, dus het kan niet ook Tuesday of Thursday betekenen.</span><span class="sxs-lookup"><span data-stu-id="71fd5-134">For example, `t` already means today, so it cannot mean Tuesday or Thursday.</span></span>

<span data-ttu-id="71fd5-135">Het schema van het weeknummer is altijd ISO 8601, waar week 1 de week met 4 januari erin is of de week met de eerste donderdag van het jaar.</span><span class="sxs-lookup"><span data-stu-id="71fd5-135">The week number scheme is always ISO 8601, where week 1 is the week with 4 January in it, or the week with the first Thursday of the year.</span></span>

### <a name="digit-patterns"></a><span data-ttu-id="71fd5-136">Cijferpatronen</span><span class="sxs-lookup"><span data-stu-id="71fd5-136">Digit patterns</span></span>

<span data-ttu-id="71fd5-137">Een datumveld kan twee, vier, zes of acht cijfers bevatten:</span><span class="sxs-lookup"><span data-stu-id="71fd5-137">In a date field you can enter two, four, six, or eight digits:</span></span>

-   <span data-ttu-id="71fd5-138">Als u slechts twee cijfers invoert, wordt dit als een dag beschouwd en wordt de maand en het jaar van de werkdag automatisch toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="71fd5-138">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>

-   <span data-ttu-id="71fd5-139">Als u vier cijfers invoert, wordt dit als een dag en een maand beschouwd en wordt het jaar van de werkdag automatisch toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="71fd5-139">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span> <span data-ttu-id="71fd5-140">De volgorde van de dag en de maand wordt bepaald door uw regio-instellingen.</span><span class="sxs-lookup"><span data-stu-id="71fd5-140">The order of the day and month is determined by your region settings.</span></span> <span data-ttu-id="71fd5-141">Zelfs als uw regio-instellingen het jaar vóór de dag en de maand bevatten, worden vier cijfers geïnterpreteerd als de dag en de maand.</span><span class="sxs-lookup"><span data-stu-id="71fd5-141">Even if your region settings have the year before the day and month, four digits are interpreted as the day and month.</span></span>

-   <span data-ttu-id="71fd5-142">Als de ingevoerde datum in de reeks 01/01/1930 tot en met 31/12/2029 valt, hoeft u slechts twee cijfers voor het jaartal in te voeren; anders moet u vier cijfers voor het jaartal invoeren.</span><span class="sxs-lookup"><span data-stu-id="71fd5-142">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>

### <a name="today"></a><span data-ttu-id="71fd5-143">Vandaag</span><span class="sxs-lookup"><span data-stu-id="71fd5-143">Today</span></span>

<span data-ttu-id="71fd5-144">Voer voor `today` in de taal die is ingesteld door **Taal**, het woord in waarmee de datum op de huidige datum wordt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="71fd5-144">Enter the word for `today`, in the language set by **Language** setting, that will set the date to the current date.</span></span> <span data-ttu-id="71fd5-145">In plaats van het hele woord in te voeren kunt u een deel van het woord invoeren, te beginnen met het begin, bijvoorbeeld `t` of `tod`, zolang het niet ook het begin van een ander woord is.</span><span class="sxs-lookup"><span data-stu-id="71fd5-145">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as `t` or `tod`, as long as it is not also the start of another word.</span></span>

### <a name="period"></a><span data-ttu-id="71fd5-146">Periode</span><span class="sxs-lookup"><span data-stu-id="71fd5-146">Period</span></span>

<span data-ttu-id="71fd5-147">Als u wilt filteren op een specifieke boekingsperiode, voert u in een datumveld de letter `p` of het woord `period` in, gevolgd door een nummer dat de boekingsperiode aangeeft, zoals `p2` of `period4`.</span><span class="sxs-lookup"><span data-stu-id="71fd5-147">To filter on a specific accounting period, in a date field enter the letter `p`, or the word `period`, followed by a number that identifies the accounting period, like `p2` or `period4`.</span></span> <span data-ttu-id="71fd5-148">De boekhoudperiode is relatief aan het boekjaar van de huidige werkdatum die u instelt in uw rolcentrum.</span><span class="sxs-lookup"><span data-stu-id="71fd5-148">The accounting period is relative to the fiscal year of the current work date that set in your Role Center.</span></span> <span data-ttu-id="71fd5-149">Als de werkdatum bijvoorbeeld **21-3-20** is, wordt met `p1` of alleen `p` gefilterd op de eerste boekingsperiode van het boekjaar 2020 (bijvoorbeeld `01/01/20..01/31/20`).</span><span class="sxs-lookup"><span data-stu-id="71fd5-149">For example, if the work date is **03/21/20**, then `p1`, or just `p`, filters on the first accounting period of the fiscal year 2020 (such as `01/01/20..01/31/20`).</span></span> <span data-ttu-id="71fd5-150">Met `p15` wordt gefilterd op de vijftiende boekingsperiode vanaf het begin van het boekjaar 2020 (bijvoorbeeld `03/01/21..03/31/21`).</span><span class="sxs-lookup"><span data-stu-id="71fd5-150">`p15` filters on the fifteenth accounting period from the start of fiscal year 2020 (such as `03/01/21..03/31/21`).</span></span> 

<span data-ttu-id="71fd5-151">De boekhoudperioden worden gedefinieerd op de pagina **Boekingsperioden**.</span><span class="sxs-lookup"><span data-stu-id="71fd5-151">The accounting periods are defined on the **Accounting Periods** page.</span></span> <span data-ttu-id="71fd5-152">Als u de boekingsperioden wilt weergeven of wijzigen, opent u de pagina [hier](https://businesscentral.dynamics.com/?page=100).</span><span class="sxs-lookup"><span data-stu-id="71fd5-152">To view or change the accounting periods, open the page [here](https://businesscentral.dynamics.com/?page=100).</span></span>

### <a name="current-work-date"></a><span data-ttu-id="71fd5-153">Huidige werkdatum</span><span class="sxs-lookup"><span data-stu-id="71fd5-153">Current work date</span></span>

<span data-ttu-id="71fd5-154">Met de werkdatumfunctie kunt u transacties vastleggen met een datum die afwijkt van de huidige datum.</span><span class="sxs-lookup"><span data-stu-id="71fd5-154">The work date feature allows you to record transactions using a date that is different from the current date.</span></span>

<span data-ttu-id="71fd5-155">Het woord voor 'werkdatum' in de taal die is ingesteld door de instelling **Taal**, stelt de datum in op de huidige ingestelde werkdatum die wordt opgegeven op de pagina [**Mijn instellingen**](https://businesscentral.dynamics.com?page=9176 "Ga direct naar de pagina met uw gebruikersinstellingen in Business Central").</span><span class="sxs-lookup"><span data-stu-id="71fd5-155">The word for 'workdate', in the language set by **Language** setting, will set the date to the currently set work date that is specified on the [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central") page.</span></span> <span data-ttu-id="71fd5-156">U kunt in plaats van het volledige woord een deel van het woord invoeren, vanaf het begin, bijvoorbeeld 'w' of 'werk'.</span><span class="sxs-lookup"><span data-stu-id="71fd5-156">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as 'w' or 'work'.</span></span>

<span data-ttu-id="71fd5-157">Als u geen werkdatum hebt gedefinieerd, wordt de huidige datum als de werkdatum gebruikt.</span><span class="sxs-lookup"><span data-stu-id="71fd5-157">If you have not defined a work date, the current date will be used as the work date.</span></span> <span data-ttu-id="71fd5-158">Het gebruik van een werkdatum is handig als u veel transacties hebt met een andere datum dan de huidige.</span><span class="sxs-lookup"><span data-stu-id="71fd5-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>

<span data-ttu-id="71fd5-159">Zie ook [Basisinstellingen wijzigen, zoals de werkdatum](ui-change-basic-settings.md#work-date).</span><span class="sxs-lookup"><span data-stu-id="71fd5-159">See also [Changing Basic Settings, such as the Work Date](ui-change-basic-settings.md#work-date).</span></span>

### <a name="closing-date"></a><span data-ttu-id="71fd5-160">Ultimodatum</span><span class="sxs-lookup"><span data-stu-id="71fd5-160">Closing Date</span></span>

<span data-ttu-id="71fd5-161">Als u een boekjaar afsluit, kunt u ultimodatums gebruiken om aan te geven dat het om een ultimopost gaat.</span><span class="sxs-lookup"><span data-stu-id="71fd5-161">When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry.</span></span> <span data-ttu-id="71fd5-162">Een ultimodatum ligt technisch gezien tussen twee datums in, zoals tussen 31 december en 1 januari.</span><span class="sxs-lookup"><span data-stu-id="71fd5-162">A closing date technically is between two dates, for example between Dec 31 and Jan 1.</span></span>

<span data-ttu-id="71fd5-163">Als u een datum wilt opgeven die een ultimodatum is, plaatst u `C` vlak vóór de datum, bijvoorbeeld `C123101`.</span><span class="sxs-lookup"><span data-stu-id="71fd5-163">To specify that a date is a closing date, put `C` just before the date, such as `C123101`.</span></span> <span data-ttu-id="71fd5-164">Dit kan in combinatie met alle datumpatronen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="71fd5-164">This can be used in combination with all the date patterns.</span></span>

### <a name="examples"></a><span data-ttu-id="71fd5-165">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="71fd5-165">Examples</span></span>

<span data-ttu-id="71fd5-166">De volgende tabel bevat voorbeelden van datums met alle indelingen.</span><span class="sxs-lookup"><span data-stu-id="71fd5-166">The following table contains examples of dates using all the formats.</span></span> <span data-ttu-id="71fd5-167">Er wordt uitgegaan van regio-instellingen die datums noteren volgens: **jaar.maand.dag.**, een week na maandag en de Engelse taal.</span><span class="sxs-lookup"><span data-stu-id="71fd5-167">It assumes region settings that format dates according to: **year.month.day.**, a week starting on Monday, and the English language.</span></span>

|<span data-ttu-id="71fd5-168">**Invoer**</span><span class="sxs-lookup"><span data-stu-id="71fd5-168">**Entry**</span></span>      |<span data-ttu-id="71fd5-169">**Interpretatie**</span><span class="sxs-lookup"><span data-stu-id="71fd5-169">**Interpretation**</span></span>      |
|---------------|------------------------|
|`2018.12.31.`|<span data-ttu-id="71fd5-170">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="71fd5-170">2018.12.31.</span></span>|
|`181231`|<span data-ttu-id="71fd5-171">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="71fd5-171">2018.12.31.</span></span>|
|`18.12.31.`|<span data-ttu-id="71fd5-172">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="71fd5-172">2018.12.31.</span></span>|
|`18.12.31.`|<span data-ttu-id="71fd5-173">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="71fd5-173">2018.12.31.</span></span>|
|`20181231`|<span data-ttu-id="71fd5-174">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="71fd5-174">2018.12.31.</span></span>|
|`18/12,31`|<span data-ttu-id="71fd5-175">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="71fd5-175">2018.12.31.</span></span>|
|`11`|<span data-ttu-id="71fd5-176">jaar van werkdatum.maand van werkdatum.11.</span><span class="sxs-lookup"><span data-stu-id="71fd5-176">work date year.work date month.11.</span></span>|
|`1112`|<span data-ttu-id="71fd5-177">jaar van werkdatum.11.12.</span><span class="sxs-lookup"><span data-stu-id="71fd5-177">work date year.11.12.</span></span>|
|<span data-ttu-id="71fd5-178">`t` of `today`</span><span class="sxs-lookup"><span data-stu-id="71fd5-178">`t` or `today`</span></span>|<span data-ttu-id="71fd5-179">datum van vandaag</span><span class="sxs-lookup"><span data-stu-id="71fd5-179">today's date</span></span>|
|`p4`|<span data-ttu-id="71fd5-180">datumbereik dat de vierde boekhoudperiode bevat, bijvoorbeeld `04/01/20..04/30/20`</span><span class="sxs-lookup"><span data-stu-id="71fd5-180">date range that includes the fourth accounting period, such as `04/01/20..04/30/20`</span></span>|
|<span data-ttu-id="71fd5-181">`w` of `workdate`</span><span class="sxs-lookup"><span data-stu-id="71fd5-181">`w` or `workdate`</span></span>|<span data-ttu-id="71fd5-182">de werkdatum</span><span class="sxs-lookup"><span data-stu-id="71fd5-182">the working date</span></span>|
|<span data-ttu-id="71fd5-183">`m` of `Monday`</span><span class="sxs-lookup"><span data-stu-id="71fd5-183">`m` or `Monday`</span></span>|<span data-ttu-id="71fd5-184">Maandag van de werkdatumweek</span><span class="sxs-lookup"><span data-stu-id="71fd5-184">Monday of the work date week</span></span>|
|<span data-ttu-id="71fd5-185">`tu` of `Tuesday`</span><span class="sxs-lookup"><span data-stu-id="71fd5-185">`tu` or `Tuesday`</span></span>|<span data-ttu-id="71fd5-186">Dinsdag van de werkdatumweek</span><span class="sxs-lookup"><span data-stu-id="71fd5-186">Tuesday of the work date week</span></span>|
|<span data-ttu-id="71fd5-187">`sa` of `Saturday`</span><span class="sxs-lookup"><span data-stu-id="71fd5-187">`sa` or `Saturday`</span></span>|<span data-ttu-id="71fd5-188">Zaterdag van de werkdatumweek</span><span class="sxs-lookup"><span data-stu-id="71fd5-188">Saturday of the work date week</span></span>|
|<span data-ttu-id="71fd5-189">`s` of `Sunday`</span><span class="sxs-lookup"><span data-stu-id="71fd5-189">`s` or `Sunday`</span></span>|<span data-ttu-id="71fd5-190">Zondag van de werkdatumweek</span><span class="sxs-lookup"><span data-stu-id="71fd5-190">Sunday of the work date week</span></span>|
|`t23`|<span data-ttu-id="71fd5-191">Dinsdag van week 23 van het werkdatumjaar</span><span class="sxs-lookup"><span data-stu-id="71fd5-191">Tuesday of week 23 of the work date year</span></span>|
|`t 23`|<span data-ttu-id="71fd5-192">Dinsdag van week 23 van het werkdatumjaar</span><span class="sxs-lookup"><span data-stu-id="71fd5-192">Tuesday of week 23 of the work date year</span></span>|
|`t-1`|<span data-ttu-id="71fd5-193">Dinsdag van week 1 van het werkdatumjaar</span><span class="sxs-lookup"><span data-stu-id="71fd5-193">Tuesday of week 1 of the work date year</span></span>|

##  <a name="BKMK_SettingDateRanges"></a> <span data-ttu-id="71fd5-194">Datumbereiken instellen</span><span class="sxs-lookup"><span data-stu-id="71fd5-194">Setting Ranges</span></span>

<span data-ttu-id="71fd5-195">In lijsten, totalen en rapporten kunt u filters instellen op datum, tijden en datumtijden. De filters kunnen een begindatum en desgewenst een einddatum bevatten om alleen de gegevens uit dat bereik weer te geven.</span><span class="sxs-lookup"><span data-stu-id="71fd5-195">On lists, totals and reports, you can set filters on dates, times and datetimes containing a start value and optionally an end value to display only the data contained in that range.</span></span> <span data-ttu-id="71fd5-196">Voor het instellen van een datumbereik gelden de standaardregels.</span><span class="sxs-lookup"><span data-stu-id="71fd5-196">The standard rules apply to the way you set date ranges.</span></span>

|<span data-ttu-id="71fd5-197">**Betekenis**</span><span class="sxs-lookup"><span data-stu-id="71fd5-197">**Meaning**</span></span>|<span data-ttu-id="71fd5-198">**Voorbeeldexpressie (datum)**</span><span class="sxs-lookup"><span data-stu-id="71fd5-198">**Sample expression (Date)**</span></span>|<span data-ttu-id="71fd5-199">**Gegevens opgenomen in het filter**</span><span class="sxs-lookup"><span data-stu-id="71fd5-199">**Data included in the filter**</span></span>|
|-----------|---------------------|--------------------|
|<span data-ttu-id="71fd5-200">Interval</span><span class="sxs-lookup"><span data-stu-id="71fd5-200">Interval</span></span>|`12 15 00..01 15 01`<br /><br />`..12 15 00`<br /><br />`p1..p4`|<span data-ttu-id="71fd5-201">Records met datums tussen 12 15 00 en 01 15 01.</span><span class="sxs-lookup"><span data-stu-id="71fd5-201">Records with dates between and including 12 15 00 and 01 15 01.</span></span><br /><br /><span data-ttu-id="71fd5-202">Records met datums van 12 15 00 of eerder.</span><span class="sxs-lookup"><span data-stu-id="71fd5-202">Records with dates of 12 15 00 or earlier.</span></span><br /><br /><span data-ttu-id="71fd5-203">Datumbereik dat de tweede, derde en vierde boekhoudperiode bevat, bijvoorbeeld `01/01/20..04/30/20`.</span><span class="sxs-lookup"><span data-stu-id="71fd5-203">Date range that includes the second, third, and fourth accounting periods, such as `01/01/20..04/30/20`.</span></span>|
|<span data-ttu-id="71fd5-204">Of/of</span><span class="sxs-lookup"><span data-stu-id="71fd5-204">Either/or</span></span>|<span data-ttu-id="71fd5-205">\`12 15 00</span><span class="sxs-lookup"><span data-stu-id="71fd5-205">\`12 15 00</span></span>|<span data-ttu-id="71fd5-206">12 16 00\`</span><span class="sxs-lookup"><span data-stu-id="71fd5-206">12 16 00\`</span></span>|<span data-ttu-id="71fd5-207">Records met datums van of 12 15 00 of 12 16 00.</span><span class="sxs-lookup"><span data-stu-id="71fd5-207">Records with dates of either 12 15 00 or 12 16 00.</span></span> <span data-ttu-id="71fd5-208">Als er records zijn met datums op beide dagen, worden ze allemaal weergegeven.</span><span class="sxs-lookup"><span data-stu-id="71fd5-208">If there are records with dates on both days, they will all be displayed.</span></span>|
|<span data-ttu-id="71fd5-209">Combinatie</span><span class="sxs-lookup"><span data-stu-id="71fd5-209">Combination</span></span>|<span data-ttu-id="71fd5-210">\`12 15 00</span><span class="sxs-lookup"><span data-stu-id="71fd5-210">\`12 15 00</span></span>|<span data-ttu-id="71fd5-211">12 01 00..12 10 00`  \n`..12 14 00</span><span class="sxs-lookup"><span data-stu-id="71fd5-211">12 01 00..12 10 00`  \n`..12 14 00</span></span>|<span data-ttu-id="71fd5-212">12 30 00..\`</span><span class="sxs-lookup"><span data-stu-id="71fd5-212">12 30 00..\`</span></span>|<span data-ttu-id="71fd5-213">Records met datums van 12-15-00 of op datums in de periode 12-01-00 t/m 12-10-00.</span><span class="sxs-lookup"><span data-stu-id="71fd5-213">Records with dates of 12 15 00 or on dates between and including 12 01 00 and 12 10 00.</span></span>  <span data-ttu-id="71fd5-214">\nRecords met datums van 12-14 00 of eerder, of datums van 12 30 00 of later. Dit wil zeggen, alle records, behalve records met datums tussen 12 15 00 en 12 29 00.</span><span class="sxs-lookup"><span data-stu-id="71fd5-214">\nRecords with dates of 12 14 00 or earlier, or dates of 12 30 00 or later, that is, all records except those with dates between and including 12 15 00 and 12 29 00.</span></span>|

<span data-ttu-id="71fd5-215">U kunt iedere geldige indeling in datumbereikfilters gebruiken.</span><span class="sxs-lookup"><span data-stu-id="71fd5-215">You can use any of the valid formats in date range filters.</span></span> <span data-ttu-id="71fd5-216">Bijvoorbeeld `mon14 3..t 4p`, toegepast op een datum/tijd-veld leidt tot een filter van 3 uur 's morgens op maandag, in week 14 van het huidige werkdatumjaar tot en met vandaag om 4 uur 's middags.</span><span class="sxs-lookup"><span data-stu-id="71fd5-216">For example, `mon14 3..t 4p` applied on a datetime field results in a filter from 3 AM on Monday in week 14 of the current work date year, inclusive, until today at 4PM, inclusive.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="71fd5-217">Datumformules gebruiken</span><span class="sxs-lookup"><span data-stu-id="71fd5-217">Using Date Formulas</span></span>
<span data-ttu-id="71fd5-218">Een datumformule is een korte, afgekorte combinatie van letters en cijfers op basis waarvan datums worden berekend.</span><span class="sxs-lookup"><span data-stu-id="71fd5-218">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="71fd5-219">U kunt datumformules invoeren in verschillende datumberekeningsvelden of -filters.</span><span class="sxs-lookup"><span data-stu-id="71fd5-219">You can enter date formulas in various date calculation fields or filters.</span></span>

> [!NOTE]
>  <span data-ttu-id="71fd5-220">In alle datumformulevelden wordt automatisch één dag opgenomen om ervoor te zorgen dat de huidige dag wordt gebruikt als begindatum van de periode.</span><span class="sxs-lookup"><span data-stu-id="71fd5-220">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="71fd5-221">Als u dus bijvoorbeeld `1W` invoert, zal de periode in feite acht dagen bestrijken omdat vandaag ook wordt opgenomen.</span><span class="sxs-lookup"><span data-stu-id="71fd5-221">Accordingly, for example, if you enter `1W`, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="71fd5-222">Als u een periode van zeven dagen \(exact één week\) wilt opgeven, inclusief de begindatum van de periode, moet u `6D` of `1W-1D` invoeren.</span><span class="sxs-lookup"><span data-stu-id="71fd5-222">To specify a period of seven days \(one true week\) including the period starting date, then you must enter `6D` or `1W-1D`.</span></span>

<span data-ttu-id="71fd5-223">Hier volgen enkele voorbeelden van het gebruik van datumformules:</span><span class="sxs-lookup"><span data-stu-id="71fd5-223">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="71fd5-224">De datumformule in de frequentievelden van periodieke dagboeken geeft aan hoe vaak de dagboekregel moet worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="71fd5-224">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="71fd5-225">De datumformule in het veld **Respijtperiode** van een bepaald aanmaningsniveau bepaalt hoelang de vervaldatum \(of de datum van de vorige aanmaning\) moet zijn verstreken voordat een aanmaning wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="71fd5-225">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date \(or from the date of the previous reminder\) before a reminder will be created.</span></span>

-   <span data-ttu-id="71fd5-226">De datumformule in het veld **Vervaldatumformule** bepaalt hoe de vervaldatum voor de aanmaning wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="71fd5-226">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="71fd5-227">De datumformule kan maximaal 20 tekens bevatten (cijfers en letters).</span><span class="sxs-lookup"><span data-stu-id="71fd5-227">The date formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="71fd5-228">U kunt de volgende letters gebruiken als afkorting voor kalendereenheden.</span><span class="sxs-lookup"><span data-stu-id="71fd5-228">You can use the following letters, which are abbreviations for calendar units.</span></span>

|  <span data-ttu-id="71fd5-229">Letter</span><span class="sxs-lookup"><span data-stu-id="71fd5-229">Letter</span></span>  |  <span data-ttu-id="71fd5-230">Betekenis</span><span class="sxs-lookup"><span data-stu-id="71fd5-230">Meaning</span></span>  |
|----------|----------------------|
|`C`|<span data-ttu-id="71fd5-231">Actueel</span><span class="sxs-lookup"><span data-stu-id="71fd5-231">Current</span></span>|
|`D`|<span data-ttu-id="71fd5-232">Dag\(en\)</span><span class="sxs-lookup"><span data-stu-id="71fd5-232">Day\(s\)</span></span>|
|`W`|<span data-ttu-id="71fd5-233">We(e)k\(en\)</span><span class="sxs-lookup"><span data-stu-id="71fd5-233">Week\(s\)</span></span>|
|`M`|<span data-ttu-id="71fd5-234">Maand\(en\)</span><span class="sxs-lookup"><span data-stu-id="71fd5-234">Month\(s\)</span></span>|
|`Q`|<span data-ttu-id="71fd5-235">Kwarta(a)l\(en\)</span><span class="sxs-lookup"><span data-stu-id="71fd5-235">Quarter\(s\)</span></span>|
|`Y`|<span data-ttu-id="71fd5-236">Ja(a)r\(en\)</span><span class="sxs-lookup"><span data-stu-id="71fd5-236">Year\(s\)</span></span>|

<span data-ttu-id="71fd5-237">Er zijn drie soorten datumformules.</span><span class="sxs-lookup"><span data-stu-id="71fd5-237">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="71fd5-238">In het volgende voorbeeld wordt weergegeven hoe `C` kan worden gebruikt voor huidig en een tijdseenheid.</span><span class="sxs-lookup"><span data-stu-id="71fd5-238">The following example shows how to use `C`, for current, and a time unit.</span></span>

|  <span data-ttu-id="71fd5-239">Expressie</span><span class="sxs-lookup"><span data-stu-id="71fd5-239">Expression</span></span>  |  <span data-ttu-id="71fd5-240">Betekenis</span><span class="sxs-lookup"><span data-stu-id="71fd5-240">Meaning</span></span>  |
|--------------|-----------|
|`CW`|<span data-ttu-id="71fd5-241">Lopende week</span><span class="sxs-lookup"><span data-stu-id="71fd5-241">Current week</span></span>|
|`CM`|<span data-ttu-id="71fd5-242">Lopende maand</span><span class="sxs-lookup"><span data-stu-id="71fd5-242">Current month</span></span>|

<span data-ttu-id="71fd5-243">In het volgende voorbeeld wordt weergegeven hoe een getal en een tijdseenheid moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="71fd5-243">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="71fd5-244">Nummers mogen niet groter zijn dan 9999.</span><span class="sxs-lookup"><span data-stu-id="71fd5-244">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="71fd5-245">Expressie</span><span class="sxs-lookup"><span data-stu-id="71fd5-245">Expression</span></span>  |  <span data-ttu-id="71fd5-246">Betekenis</span><span class="sxs-lookup"><span data-stu-id="71fd5-246">Meaning</span></span>  |
|--------------|-----------|
|`10D`|<span data-ttu-id="71fd5-247">10 dagen vanaf vandaag</span><span class="sxs-lookup"><span data-stu-id="71fd5-247">10 days from today</span></span>|
|`2W`|<span data-ttu-id="71fd5-248">2 weken vanaf vandaag</span><span class="sxs-lookup"><span data-stu-id="71fd5-248">2 weeks from today</span></span>|

<span data-ttu-id="71fd5-249">In het volgende voorbeeld wordt weergegeven hoe een tijdseenheid en een getal moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="71fd5-249">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="71fd5-250">Expressie</span><span class="sxs-lookup"><span data-stu-id="71fd5-250">Expression</span></span>  |  <span data-ttu-id="71fd5-251">Betekenis</span><span class="sxs-lookup"><span data-stu-id="71fd5-251">Meaning</span></span>  |
|--------------|-----------|
|`D10`|<span data-ttu-id="71fd5-252">De volgende tiende dag van een maand</span><span class="sxs-lookup"><span data-stu-id="71fd5-252">The next 10th day of a month</span></span>|
|`WD4`|<span data-ttu-id="71fd5-253">De volgende vierde dag van een week \(donderdag\)</span><span class="sxs-lookup"><span data-stu-id="71fd5-253">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="71fd5-254">Het volgende voorbeeld geeft weer hoe u deze drie soorten naar wens kunt combineren.</span><span class="sxs-lookup"><span data-stu-id="71fd5-254">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="71fd5-255">Expressie</span><span class="sxs-lookup"><span data-stu-id="71fd5-255">Expression</span></span>  |  <span data-ttu-id="71fd5-256">Betekenis</span><span class="sxs-lookup"><span data-stu-id="71fd5-256">Meaning</span></span>  |
|--------------|-----------|
|`CM+10D`|<span data-ttu-id="71fd5-257">Lopende maand \+ 10 dagen</span><span class="sxs-lookup"><span data-stu-id="71fd5-257">Current month \+ 10 days</span></span>|

<span data-ttu-id="71fd5-258">In het volgende voorbeeld ziet u hoe u een minteken gebruikt om een datum in het verleden aan te duiden.</span><span class="sxs-lookup"><span data-stu-id="71fd5-258">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="71fd5-259">Expressie</span><span class="sxs-lookup"><span data-stu-id="71fd5-259">Expression</span></span>  |  <span data-ttu-id="71fd5-260">Betekenis</span><span class="sxs-lookup"><span data-stu-id="71fd5-260">Meaning</span></span>  |
|--------------|-----------|
|`-1Y`|<span data-ttu-id="71fd5-261">1 jaar geleden vanaf vandaag</span><span class="sxs-lookup"><span data-stu-id="71fd5-261">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="71fd5-262">Als de vestiging een basisagenda gebruikt, wordt de datumformule die u invoert in dit veld, bijvoorbeeld het veld **Verzendtijd** beschouwd als agendawerkdag.</span><span class="sxs-lookup"><span data-stu-id="71fd5-262">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="71fd5-263">Bijvoorbeeld: `1W` betekent zeven werkdagen.</span><span class="sxs-lookup"><span data-stu-id="71fd5-263">For example, `1W`  means seven working days.</span></span>
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

Note that we have used the US date format MMDDYY here. As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.

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

## <a name="entering-times"></a><span data-ttu-id="71fd5-264">Tijden invoeren</span><span class="sxs-lookup"><span data-stu-id="71fd5-264">Entering Times</span></span>
<span data-ttu-id="71fd5-265">Wanneer u tijden invoert, kunt u alle gewenste niet-spatie scheidingstekens invoegen tussen de eenheden, maar als u dubbele cijfers gebruikt voor elke eenheid tot aan milliseconden, is het niet vereist.</span><span class="sxs-lookup"><span data-stu-id="71fd5-265">When you enter times, you can insert any non-space separators that you want between the units, but if you use double digits for each unit up to milliseconds, then it is not required.</span></span>

<span data-ttu-id="71fd5-266">U hoeft de alleen grootste eenheden te gebruiken die u nodig hebt. De rest wordt op nul ingesteld.</span><span class="sxs-lookup"><span data-stu-id="71fd5-266">You only have to write the largest units that you require; the rest will be set to zero.</span></span> <span data-ttu-id="71fd5-267">U kunt de AM/PM-indicator ook weglaten.</span><span class="sxs-lookup"><span data-stu-id="71fd5-267">You can also leave out any AM/PM indicator.</span></span>

<span data-ttu-id="71fd5-268">In de volgende tabel wordt aangegeven op welke manieren u tijden kunt invoeren en hoe de invoer wordt geïnterpreteerd.</span><span class="sxs-lookup"><span data-stu-id="71fd5-268">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span> <span data-ttu-id="71fd5-269">Er wordt uitgegaan van een regio-instelling die tijden noteert volgens: **Uren:Minuten:Seconden.Milliseconden.**</span><span class="sxs-lookup"><span data-stu-id="71fd5-269">It assumes region settings that format times according to: **Hours:Minutes:Seconds.Milliseconds.**</span></span> <span data-ttu-id="71fd5-270">en die respectievelijk de indicatoren 'AM' en 'PM' gebruikt.</span><span class="sxs-lookup"><span data-stu-id="71fd5-270">and use the AM and PM indicators of 'AM' and 'PM', respectively.</span></span>

|<span data-ttu-id="71fd5-271">**Invoer**</span><span class="sxs-lookup"><span data-stu-id="71fd5-271">**Entry**</span></span>      |<span data-ttu-id="71fd5-272">**Interpretatie**</span><span class="sxs-lookup"><span data-stu-id="71fd5-272">**Interpretation**</span></span>      |
|---------------|------------------------|
|`05:23:17`|<span data-ttu-id="71fd5-273">05:23:17</span><span class="sxs-lookup"><span data-stu-id="71fd5-273">05:23:17</span></span>|
|`5`|<span data-ttu-id="71fd5-274">05:00:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-274">05:00:00</span></span>|
|`5AM`|<span data-ttu-id="71fd5-275">05:00:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-275">05:00:00</span></span>|
|`5P`|<span data-ttu-id="71fd5-276">17:00:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-276">17:00:00</span></span>|
|`12`|<span data-ttu-id="71fd5-277">12:00:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-277">12:00:00</span></span>|
|`12A`|<span data-ttu-id="71fd5-278">00:00:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-278">00:00:00</span></span>|
|`12P`|<span data-ttu-id="71fd5-279">12:00:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-279">12:00:00</span></span>|
|`17`|<span data-ttu-id="71fd5-280">17:00:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-280">17:00:00</span></span>|
|`5:30`|<span data-ttu-id="71fd5-281">05:30:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-281">05:30:00</span></span>|
|`0530`|<span data-ttu-id="71fd5-282">05:30:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-282">05:30:00</span></span>|
|`5:30:5`|<span data-ttu-id="71fd5-283">05:30:05</span><span class="sxs-lookup"><span data-stu-id="71fd5-283">05:30:05</span></span>|
|`053005`|<span data-ttu-id="71fd5-284">05:30:05</span><span class="sxs-lookup"><span data-stu-id="71fd5-284">05:30:05</span></span>|
|`5:30:5,50`|<span data-ttu-id="71fd5-285">05:30:05,5</span><span class="sxs-lookup"><span data-stu-id="71fd5-285">05:30:05.5</span></span>|
|`053005050`|<span data-ttu-id="71fd5-286">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="71fd5-286">05:30:05.05</span></span>|

<span data-ttu-id="71fd5-287">Houd er rekening mee dat milliseconden als decimale notatie worden geïnterpreteerd.</span><span class="sxs-lookup"><span data-stu-id="71fd5-287">You should be aware that milliseconds are interpreted as decimal notation.</span></span> <span data-ttu-id="71fd5-288">Bijvoorbeeld `3`, `30` en `300` betekenen allemaal 300 milliseconden, en `03` betekent `30` en `003` betekent 3 milliseconden.</span><span class="sxs-lookup"><span data-stu-id="71fd5-288">So, for example, `3`, `30`, and `300` all mean 300 milliseconds, while `03` means `30` and `003` means 3 milliseconds.</span></span>

<span data-ttu-id="71fd5-289">U kunt `24:00` niet voor middernacht gebruiken of gebruiken als waarde groter dan 24:00.</span><span class="sxs-lookup"><span data-stu-id="71fd5-289">You cannot use `24:00` to mean midnight, or use any value greater than 24:00.</span></span>

<span data-ttu-id="71fd5-290">Het woord voor 'tijd' in de taal die [!INCLUDE[d365fin](includes/d365fin_long_md.md)] gebruikt, wordt geëvalueerd als de huidige tijd op uw computer of mobiele apparaat.</span><span class="sxs-lookup"><span data-stu-id="71fd5-290">The word for 'time' in the language used by [!INCLUDE[d365fin](includes/d365fin_long_md.md)] will be evaluated to the current time on your computer or mobile device.</span></span> <span data-ttu-id="71fd5-291">U kunt elk deel van het woord invoeren, beginnend bij het begin, zoals `t` of `TIM`.</span><span class="sxs-lookup"><span data-stu-id="71fd5-291">You can enter any part of the word, starting from the beginning, such as `t` or `TIM`.</span></span>

## <a name="entering-combined-dates-and-times"></a><span data-ttu-id="71fd5-292">Gecombineerde datums en tijden invoeren</span><span class="sxs-lookup"><span data-stu-id="71fd5-292">Entering combined Dates and Times</span></span>
<span data-ttu-id="71fd5-293">Wanneer u een datumtijd invoert (een datum en een tijd gecombineerd tot één veld), moet u een spatie invoeren tussen de datum en de tijd.</span><span class="sxs-lookup"><span data-stu-id="71fd5-293">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="71fd5-294">Het datumdeel kan alleen spaties in de vorm van het officiële datumscheidingsteken van uw regio-instellingen bevatten.</span><span class="sxs-lookup"><span data-stu-id="71fd5-294">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="71fd5-295">De tijd kan spaties bevatten rond de AM/PM-indicator.</span><span class="sxs-lookup"><span data-stu-id="71fd5-295">The time can contain spaces around the AM/PM indicator.</span></span>

<span data-ttu-id="71fd5-296">Het is ook mogelijk alleen een datum in een datumtijdveld in te voeren, maar u kunt niet alleen een tijd invoeren.</span><span class="sxs-lookup"><span data-stu-id="71fd5-296">It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.</span></span>

<span data-ttu-id="71fd5-297">In de volgende tabel staan enkele voorbeelden van datum/tijd-combinaties.</span><span class="sxs-lookup"><span data-stu-id="71fd5-297">The following table lists some examples of date/time combinations.</span></span> <span data-ttu-id="71fd5-298">Met de regio-instellingen in de voorbeelden worden datums weergegeven in de notatie dag\-maand\-jaar, met AM/PM-indicatoren, Engelse taal en zondag als begin van de week.</span><span class="sxs-lookup"><span data-stu-id="71fd5-298">The region settings in the examples displays dates in the day\-month\-year format, using AM/PM designators, English language, and Sunday as the start of the week.</span></span>

|<span data-ttu-id="71fd5-299">**Invoer**</span><span class="sxs-lookup"><span data-stu-id="71fd5-299">**Entry**</span></span>      |<span data-ttu-id="71fd5-300">**Interpretatie**</span><span class="sxs-lookup"><span data-stu-id="71fd5-300">**Interpretation**</span></span>      |
|---------------|------------------------|
|`08-01-2016 05:48:12 PM`|<span data-ttu-id="71fd5-301">08\-01\-2016 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="71fd5-301">08\-01\-2016 05:48:12 PM</span></span>|
|`131202 132455`|<span data-ttu-id="71fd5-302">13\-12\-2002 13:24:55</span><span class="sxs-lookup"><span data-stu-id="71fd5-302">13\-12\-2002 13:24:55</span></span>|
|`1-12-02 10`|<span data-ttu-id="71fd5-303">01\-12\-2002 10:00:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-303">01\-12\-2002 10:00:00</span></span>|
|`1.12.02 5`|<span data-ttu-id="71fd5-304">01\-12\-2002 05:00:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-304">01\-12\-2002 05:00:00</span></span>|
|`1.12.02`|<span data-ttu-id="71fd5-305">01\-12\-2002 00:00:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-305">01\-12\-2002 00:00:00</span></span>|
|`11 12`|<span data-ttu-id="71fd5-306">11\-werkdatummaand\-werkdatumjaar 12:00:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-306">11\-work date month\-work date year 12:00:00</span></span>|
|`1112 12`|<span data-ttu-id="71fd5-307">11\-12\-werkdatumjaar 12:00:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-307">11\-12\-work date year 12:00:00</span></span>|
|<span data-ttu-id="71fd5-308">`t` of `today`</span><span class="sxs-lookup"><span data-stu-id="71fd5-308">`t` or `today`</span></span>|<span data-ttu-id="71fd5-309">huidige datum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-309">today's date 00:00:00</span></span>|
|`t 10:30`|<span data-ttu-id="71fd5-310">huidige datum 10:30:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-310">today's date 10:30:00</span></span>|
|`t 3:3:3`|<span data-ttu-id="71fd5-311">huidige datum 03:03:03</span><span class="sxs-lookup"><span data-stu-id="71fd5-311">today's date 03:03:03</span></span>|
|<span data-ttu-id="71fd5-312">`w` of `workdate`</span><span class="sxs-lookup"><span data-stu-id="71fd5-312">`w` or `workdate`</span></span>|<span data-ttu-id="71fd5-313">de werkdatum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-313">the working date 00:00:00</span></span>|
|<span data-ttu-id="71fd5-314">`m` of `Monday`</span><span class="sxs-lookup"><span data-stu-id="71fd5-314">`m` or `Monday`</span></span>|<span data-ttu-id="71fd5-315">Maandag van de werkdatumweek 00:00:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-315">Monday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="71fd5-316">`tu` of `Tuesday`</span><span class="sxs-lookup"><span data-stu-id="71fd5-316">`tu` or `Tuesday`</span></span>|<span data-ttu-id="71fd5-317">Dinsdag van de werkdatumweek 00:00:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-317">Tuesday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="71fd5-318">`sa` of `Saturday`</span><span class="sxs-lookup"><span data-stu-id="71fd5-318">`sa` or `Saturday`</span></span>|<span data-ttu-id="71fd5-319">Zaterdag van de werkdatumweek 00:00:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-319">Saturday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="71fd5-320">`s` of `Sunday`</span><span class="sxs-lookup"><span data-stu-id="71fd5-320">`s` or `Sunday`</span></span>|<span data-ttu-id="71fd5-321">Zondag van de werkdatumweek 00:00:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-321">Sunday of the work date week 00:00:00</span></span>|
|`tu 10:30`|<span data-ttu-id="71fd5-322">Dinsdag van de werkdatumweek 10:30:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-322">Tuesday of the work date week 10:30:00</span></span>|
|`tu 3:3:3`|<span data-ttu-id="71fd5-323">Dinsdag van de werkdatumweek 03:03:03</span><span class="sxs-lookup"><span data-stu-id="71fd5-323">Tuesday of the work date week 03:03:03</span></span>|
|`t23 t`|<span data-ttu-id="71fd5-324">Dinsdag van week 23 van het werkdatumjaar huidige tijd van dag</span><span class="sxs-lookup"><span data-stu-id="71fd5-324">Tuesday of week 23 of the work date year, current time of day</span></span>|
|`t23`|<span data-ttu-id="71fd5-325">Dinsdag van week 23 van het werkdatumjaar</span><span class="sxs-lookup"><span data-stu-id="71fd5-325">Tuesday of week 23 of the work date year</span></span>|
|`t 23`|<span data-ttu-id="71fd5-326">Vandaag 23:00:00</span><span class="sxs-lookup"><span data-stu-id="71fd5-326">Today 23:00:00</span></span>|
|`t-1`|<span data-ttu-id="71fd5-327">Dinsdag van week 1 van het werkdatumjaar</span><span class="sxs-lookup"><span data-stu-id="71fd5-327">Tuesday of week 1 of the work date year</span></span>|

## <a name="entering-duration"></a><span data-ttu-id="71fd5-328">Duur invoeren</span><span class="sxs-lookup"><span data-stu-id="71fd5-328">Entering Duration</span></span>
<span data-ttu-id="71fd5-329">Sommige velden in toepassingsmodule vertegenwoordigen een duur of hoeveelheid verstreken tijd, in plaats van een specifieke datum of tijd.</span><span class="sxs-lookup"><span data-stu-id="71fd5-329">Some fields in the application represent a duration, or amount of elapsed time, instead of a specific date or time.</span></span> <span data-ttu-id="71fd5-330">De duur moet worden ingevoerd als een getal gevolgd door de eenheid.</span><span class="sxs-lookup"><span data-stu-id="71fd5-330">You enter a duration as a number followed by its unit of measure.</span></span>

<span data-ttu-id="71fd5-331">Hier volgen enkele voorbeelden.</span><span class="sxs-lookup"><span data-stu-id="71fd5-331">Here are some examples.</span></span>

|<span data-ttu-id="71fd5-332">**Duur**</span><span class="sxs-lookup"><span data-stu-id="71fd5-332">**Duration**</span></span>|<span data-ttu-id="71fd5-333">**Eenheid**</span><span class="sxs-lookup"><span data-stu-id="71fd5-333">**Unit of measure**</span></span>|
|------------|-------------------|
|`2h`|<span data-ttu-id="71fd5-334">2 uur</span><span class="sxs-lookup"><span data-stu-id="71fd5-334">2 hrs</span></span>|
|`6h 30 m`|<span data-ttu-id="71fd5-335">6 uur en 30 minuten</span><span class="sxs-lookup"><span data-stu-id="71fd5-335">6 hrs 30 mins</span></span>|
|`6.5h`|<span data-ttu-id="71fd5-336">6 uur en 30 minuten</span><span class="sxs-lookup"><span data-stu-id="71fd5-336">6 hrs 30 mins</span></span>|
|`90m`|<span data-ttu-id="71fd5-337">1 uur en 30 minuten</span><span class="sxs-lookup"><span data-stu-id="71fd5-337">1 hr 30 mins</span></span>|
|`2d 6h 30m`|<span data-ttu-id="71fd5-338">2 dagen, 6 uur en 30 minuten</span><span class="sxs-lookup"><span data-stu-id="71fd5-338">2 days 6 hrs 30 mins</span></span>|
|`2d 6h 30m 56s 600ms`|<span data-ttu-id="71fd5-339">2 dagen, 6 uur, 30 minuten, 56 seconden en 600 milliseconden</span><span class="sxs-lookup"><span data-stu-id="71fd5-339">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|

<span data-ttu-id="71fd5-340">U kunt ook een getal invoeren, dat automatisch naar een duur wordt geconverteerd.</span><span class="sxs-lookup"><span data-stu-id="71fd5-340">You can also enter a number, which will be automatically converted to a duration.</span></span> <span data-ttu-id="71fd5-341">Dit gebeurt op basis van de standaardeenheid die in het veld Duur is ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="71fd5-341">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>

<span data-ttu-id="71fd5-342">Als u wilt nagaan welke eenheid wordt gebruikt in het veld Duur, voert u een getal in en bekijkt u in welke eenheid het getal wordt omgezet.</span><span class="sxs-lookup"><span data-stu-id="71fd5-342">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>

<span data-ttu-id="71fd5-343">Als de maateenheid uren is, wordt het getal `5` bijvoorbeeld naar 5 uur geconverteerd.</span><span class="sxs-lookup"><span data-stu-id="71fd5-343">For example, if the unit of measure is hours, the number `5` is converted to 5 hrs.</span></span>


## <a name="see-also"></a><span data-ttu-id="71fd5-344">Zie ook</span><span class="sxs-lookup"><span data-stu-id="71fd5-344">See Also</span></span>
<span data-ttu-id="71fd5-345">[Werken met [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="71fd5-345">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="71fd5-346">Datumberekening voor inkoop</span><span class="sxs-lookup"><span data-stu-id="71fd5-346">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="71fd5-347">Criteria in filters invoeren</span><span class="sxs-lookup"><span data-stu-id="71fd5-347">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  

