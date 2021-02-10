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
# <a name="working-with-calendar-dates-and-times"></a><span data-ttu-id="9cbc5-104">Werken met agendadatums en -tijden</span><span class="sxs-lookup"><span data-stu-id="9cbc5-104">Working with Calendar Dates and Times</span></span>

[!INCLUDE[prod_short](includes/prod_long.md)] <span data-ttu-id="9cbc5-105">biedt meerdere manieren om datums en tijden in te voeren, inclusief krachtige functies die gegevensinvoer versnellen of u helpen complexe agenda-expressies te schrijven.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-105">offers multiple ways to enter dates and times, including powerful features that accelerate data entry, or help you write complex calendar expressions.</span></span> <span data-ttu-id="9cbc5-106">Er zijn verschillende plaatsen in de toepassing waar u datums en tijden in velden kunt invoeren.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-106">There are various places throughout the application where you can enter dates and times in fields.</span></span> <span data-ttu-id="9cbc5-107">Bijvoorbeeld in een verkooporder kunt u de verzenddatum instellen.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-107">For example, on a sales order, you can set the shipment date.</span></span> <span data-ttu-id="9cbc5-108">Wanneer u lijsten of rapportgegevens filtert, kunt u datums en tijden invoeren om alleen de gegevens te krijgen waarin u geïnteresseerd bent.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-108">When filtering lists or report data, you can enter dates and times to pinpoint only the data that you are interested in.</span></span>

## <a name="check-your-region-and-language-settings"></a><span data-ttu-id="9cbc5-109">Uw regio- en taalinstellingen controleren</span><span class="sxs-lookup"><span data-stu-id="9cbc5-109">Check your region and language settings</span></span>
<span data-ttu-id="9cbc5-110">De pagina **Mijn instellingen** geeft de **Regio** en **Taal** op die u in de toepassing gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-110">The **My Settings** page specifies the **Region** and **Language** that you are using in the application.</span></span> <span data-ttu-id="9cbc5-111">Deze instellingen bepalen hoe u datums en tijden invoert.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-111">These settings influence how you enter dates and times.</span></span>

-   <span data-ttu-id="9cbc5-112">De instelling bij **Regio** bepaalt de weergave of notatie van datums, tijden, nummers en valuta's.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-112">The **Region** setting determines how dates, times, numbers, and currencies are shown or formatted.</span></span>

-   <span data-ttu-id="9cbc5-113">Voor datumpatronen met woorden moet de taal van de woorden overeenkomen met de instelling **Taal**.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-113">For date patterns that involve words, the language of the words that you use must correspond to the **Language** setting.</span></span>

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_long.md)] <span data-ttu-id="9cbc5-114">gebruikt het Gregoriaanse kalendersysteem.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-114">uses the Gregorian calendar system.</span></span>

<!--
The following sections describe how you can enter dates, times, datetimes, durations, date ranges, and how you use date formulas.
-->

## <a name="entering-dates"></a><span data-ttu-id="9cbc5-115">Datums invoeren</span><span class="sxs-lookup"><span data-stu-id="9cbc5-115">Entering Dates</span></span>

<span data-ttu-id="9cbc5-116">In een datumveld kunt u een datum invoeren met de standaardnotatie voor uw regio-instelling.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-116">In a date field, you can enter a date using the standard format for your region setting.</span></span> <span data-ttu-id="9cbc5-117">Verschillende regio's kunnen verschillende scheidingstekens hebben tussen de dagen, maanden en jaren.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-117">Different regions can use different separators between the days, months and years.</span></span> <span data-ttu-id="9cbc5-118">Sommige regio's gebruiken bijvoorbeeld streepjes (mm-dd-jjjj) en andere gebruiken voorwaartse schuine strepen (mm/dd/jjjj).</span><span class="sxs-lookup"><span data-stu-id="9cbc5-118">For example, some regions use dashes (mm-dd-yyyy) and others use forward slashes (mm/dd/yyyy).</span></span> <span data-ttu-id="9cbc5-119">U kunt echter elk scheidingsteken gebruiken, zelfs een spatie, en de datum wordt automatisch aangepast aan het scheidingsteken dat overeenkomt met uw regio.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-119">However, you can use any separators, even a space, and the date will automatically be changed to use separators that match your region.</span></span>

<span data-ttu-id="9cbc5-120">De notatie waarin datums in afgedrukte rapporten of ge-e-mailde documenten worden weergegeven, wordt niet beïnvloed door uw persoonlijke keuze van de regio-instelling.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-120">Note that the format in which dates are displayed on printed reports or emailed documents is not influenced by your personal choice of region setting.</span></span>

<span data-ttu-id="9cbc5-121">Als u productiever met datums en tijden wilt werken, kunt u elke methode of notatie gebruiken die in de volgende gedeelten wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-121">To work more productively with dates and times, you can use any of the methods or formats that are described in the following sections.</span></span>

### <a name="picking-dates-from-the-calendar"></a><span data-ttu-id="9cbc5-122">Datums ophalen uit de kalender</span><span class="sxs-lookup"><span data-stu-id="9cbc5-122">Picking dates from the calendar</span></span>

<span data-ttu-id="9cbc5-123">Een veld waarbij een kalenderpictogram wordt weergegeven, kan worden ingesteld met de kalenderdatumkiezer.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-123">Any field displaying a calendar icon can be set using the calendar date picker.</span></span> <span data-ttu-id="9cbc5-124">Als u de kalenderdatumkiezer wilt weergeven, activeert u het kalenderpictogram of drukt u op de toetsenbordsneltoets Ctrl+Home in het veld.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-124">To display the calendar date picker, activate the calendar icon or press the Ctrl + Home keyboard shortcut in the field.</span></span>

<span data-ttu-id="9cbc5-125">![Datumvelden](media/ui-date-field.png "Voorbeeld van een datumveld")</span><span class="sxs-lookup"><span data-stu-id="9cbc5-125">![Date fields](media/ui-date-field.png "Example of a date field")</span></span>

<span data-ttu-id="9cbc5-126">Zie ook [Sneltoetsen in de kalenderdatumkiezer](keyboard-shortcuts.md#calendarshortcuts).</span><span class="sxs-lookup"><span data-stu-id="9cbc5-126">See also [Keyboard Shortcuts in the calendar date picker](keyboard-shortcuts.md#calendarshortcuts).</span></span>

### <a name="day-week-year-pattern"></a><span data-ttu-id="9cbc5-127">Dag\-week\-jaar patroon</span><span class="sxs-lookup"><span data-stu-id="9cbc5-127">Day\-week\-year pattern</span></span>

<span data-ttu-id="9cbc5-128">U kunt een datum als dag van de week invoeren, gevolgd door een weeknummer en desgewenst een jaar.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-128">You can enter a date as a weekday followed by a week number and, optionally, a year.</span></span> <span data-ttu-id="9cbc5-129">Bijvoorbeeld Maa25 of maa25 betekent maandag in week 25.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-129">For example, Mon25 or mon25 means Monday in week 25.</span></span> <span data-ttu-id="9cbc5-130">Als u geen jaar invoert, wordt het jaar van de werkdatum gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-130">If you do not enter a year, the year of the work date is used.</span></span>

<span data-ttu-id="9cbc5-131">U kunt in plaats van het volledige woord voor de dag van de week een deel van het woord invoeren, vanaf het begin.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-131">Instead of entering the entire word for the day of the week, you can enter part of the word, starting from the beginning.</span></span> <span data-ttu-id="9cbc5-132">In het geval van conflicten (zoals met z, wat zowel zaterdag als zondag kan zijn), worden de dagen geëvalueerd op basis van de instellingen van de regio.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-132">In case of conflicts (such as with s which could be Saturday or Sunday), the days are evaluated according to the region setting.</span></span> <span data-ttu-id="9cbc5-133">De invoer wordt ook eerst geëvalueerd tegen werkdatum en vandaag, dus houd daar rekening mee wanneer u afkortingen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-133">The input is first evaluated against workdate and today as well, so keep this in mind when abbreviating.</span></span> <span data-ttu-id="9cbc5-134">v betekent bijvoorbeeld al vandaag, dus het kan niet ook vrijdag betekenen.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-134">For example, t already means today, so it cannot mean Tuesday or Thursday.</span></span>

<span data-ttu-id="9cbc5-135">Het schema van het weeknummer is altijd ISO 8601, waar week 1 de week met 4 januari erin is of de week met de eerste donderdag van het jaar.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-135">The week number scheme is always ISO 8601, where week 1 is the week with 4 January in it, or the week with the first Thursday of the year.</span></span>

### <a name="digit-patterns"></a><span data-ttu-id="9cbc5-136">Cijferpatronen</span><span class="sxs-lookup"><span data-stu-id="9cbc5-136">Digit patterns</span></span>

<span data-ttu-id="9cbc5-137">Een datumveld kan twee, vier, zes of acht cijfers bevatten:</span><span class="sxs-lookup"><span data-stu-id="9cbc5-137">In a date field you can enter two, four, six, or eight digits:</span></span>

-   <span data-ttu-id="9cbc5-138">Als u slechts twee cijfers invoert, wordt dit als een dag beschouwd en wordt de maand en het jaar van de werkdag automatisch toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-138">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>

-   <span data-ttu-id="9cbc5-139">Als u vier cijfers invoert, wordt dit als een dag en een maand beschouwd en wordt het jaar van de werkdag automatisch toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-139">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span> <span data-ttu-id="9cbc5-140">De volgorde van de dag en de maand wordt bepaald door uw regio-instellingen.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-140">The order of the day and month is determined by your region settings.</span></span> <span data-ttu-id="9cbc5-141">Zelfs als uw regio-instellingen het jaar vóór de dag en de maand bevatten, worden vier cijfers geïnterpreteerd als de dag en de maand.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-141">Even if your region settings have the year before the day and month, four digits are interpreted as the day and month.</span></span>

-   <span data-ttu-id="9cbc5-142">Als de ingevoerde datum in de reeks 01.01.1930 tot en met 31.12.2029 valt, hoeft u slechts twee cijfers voor het jaartal in te voeren; anders moet u vier cijfers voor het jaartal invoeren.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-142">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>

### <a name="today"></a><span data-ttu-id="9cbc5-143">Vandaag</span><span class="sxs-lookup"><span data-stu-id="9cbc5-143">Today</span></span>

<span data-ttu-id="9cbc5-144">Voer voor vandaag in de taal die is ingesteld door **Taal**, het woord in waarmee de datum op de huidige datum wordt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-144">Enter the word for today, in the language set by **Language** setting, that will set the date to the current date.</span></span> <span data-ttu-id="9cbc5-145">In plaats van het hele woord in te voeren kunt u een deel van het woord invoeren, te beginnen met het begin, bijvoorbeeld v of van, zolang het niet ook het begin van een ander woord is.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-145">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as t or tod, as long as it is not also the start of another word.</span></span>

### <a name="period"></a><span data-ttu-id="9cbc5-146">Periode</span><span class="sxs-lookup"><span data-stu-id="9cbc5-146">Period</span></span>

<span data-ttu-id="9cbc5-147">Als u wilt filteren op een specifieke boekingsperiode, voert u in een datumveld de letter p of het woord periode in, gevolgd door een nummer dat de boekingsperiode aangeeft, zoals p2 of periode4.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-147">To filter on a specific accounting period, in a date field enter the letter p, or the word period, followed by a number that identifies the accounting period, like p2 or period4.</span></span> <span data-ttu-id="9cbc5-148">De boekhoudperiode is relatief aan het boekjaar van de huidige werkdatum die u instelt in uw rolcentrum.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-148">The accounting period is relative to the fiscal year of the current work date that set in your Role Center.</span></span> <span data-ttu-id="9cbc5-149">Als de werkdatum bijvoorbeeld **21.3.20** is, wordt met p1 of alleen p gefilterd op de eerste boekingsperiode van het boekjaar 2020 (bijvoorbeeld 1.1.20..31.1.20).</span><span class="sxs-lookup"><span data-stu-id="9cbc5-149">For example, if the work date is **03/21/20**, then p1, or just p, filters on the first accounting period of the fiscal year 2020 (such as 01/01/20..01/31/20).</span></span> <span data-ttu-id="9cbc5-150">Met p15 wordt gefilterd op de vijftiende boekingsperiode vanaf het begin van het boekjaar 2020 (bijvoorbeeld 1.3.21..31.3.21).</span><span class="sxs-lookup"><span data-stu-id="9cbc5-150">p15 filters on the fifteenth accounting period from the start of fiscal year 2020 (such as 03/01/21..03/31/21).</span></span>

<span data-ttu-id="9cbc5-151">De boekhoudperioden worden gedefinieerd op de pagina **Boekingsperioden**.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-151">The accounting periods are defined on the **Accounting Periods** page.</span></span> <span data-ttu-id="9cbc5-152">Als u de boekingsperioden wilt weergeven of wijzigen, opent u de pagina [hier](https://businesscentral.dynamics.com/?page=100).</span><span class="sxs-lookup"><span data-stu-id="9cbc5-152">To view or change the accounting periods, open the page [here](https://businesscentral.dynamics.com/?page=100).</span></span>

### <a name="current-work-date"></a><span data-ttu-id="9cbc5-153">Huidige werkdatum</span><span class="sxs-lookup"><span data-stu-id="9cbc5-153">Current work date</span></span>

<span data-ttu-id="9cbc5-154">Met de werkdatumfunctie kunt u transacties vastleggen met een datum die afwijkt van de huidige datum.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-154">The work date feature allows you to record transactions using a date that is different from the current date.</span></span>

<span data-ttu-id="9cbc5-155">Het woord voor 'werkdatum' in de taal die is ingesteld door de instelling **Taal**, stelt de datum in op de huidige ingestelde werkdatum die wordt opgegeven op de pagina **Mijn instellingen**.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-155">The word for 'workdate', in the language set by **Language** setting, will set the date to the currently set work date that is specified on the **My Settings** page.</span></span> <span data-ttu-id="9cbc5-156">U kunt in plaats van het volledige woord een deel van het woord invoeren, vanaf het begin, bijvoorbeeld 'w' of 'werk'.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-156">Instead of entering the entire word, you can enter part of the word, starting from the beginning, such as 'w' or 'work'.</span></span>

<span data-ttu-id="9cbc5-157">Als u geen werkdatum hebt gedefinieerd, wordt de huidige datum als de werkdatum gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-157">If you have not defined a work date, the current date will be used as the work date.</span></span> <span data-ttu-id="9cbc5-158">Het gebruik van een werkdatum is handig als u veel transacties hebt met een andere datum dan de huidige.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>

<span data-ttu-id="9cbc5-159">Zie ook [Basisinstellingen wijzigen, zoals de werkdatum](ui-change-basic-settings.md#work-date).</span><span class="sxs-lookup"><span data-stu-id="9cbc5-159">See also [Change Basic Settings, such as the Work Date](ui-change-basic-settings.md#work-date).</span></span>

### <a name="closing-date"></a><span data-ttu-id="9cbc5-160">Ultimodatum</span><span class="sxs-lookup"><span data-stu-id="9cbc5-160">Closing Date</span></span>

<span data-ttu-id="9cbc5-161">Als u een boekjaar afsluit, kunt u ultimodatums gebruiken om aan te geven dat het om een ultimopost gaat.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-161">When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry.</span></span> <span data-ttu-id="9cbc5-162">Een ultimodatum ligt technisch gezien tussen twee datums in, zoals tussen 31 december en 1 januari.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-162">A closing date technically is between two dates, for example between Dec 31 and Jan 1.</span></span>

<span data-ttu-id="9cbc5-163">Als u een datum wilt opgeven die een ultimodatum is, plaatst u U vlak vóór de datum, bijvoorbeeld U311201.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-163">To specify that a date is a closing date, put C just before the date, such as C123101.</span></span> <span data-ttu-id="9cbc5-164">Dit kan in combinatie met alle datumpatronen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-164">This can be used in combination with all the date patterns.</span></span>

### <a name="examples"></a><span data-ttu-id="9cbc5-165">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="9cbc5-165">Examples</span></span>

<span data-ttu-id="9cbc5-166">De volgende tabel bevat voorbeelden van datums met alle indelingen.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-166">The following table contains examples of dates using all the formats.</span></span> <span data-ttu-id="9cbc5-167">Er wordt uitgegaan van regio-instellingen die datums noteren volgens: **jaar.maand.dag.**, een week na maandag en de Engelse taal.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-167">It assumes region settings that format dates according to: **year.month.day.**, a week starting on Monday, and the English language.</span></span>

|<span data-ttu-id="9cbc5-168">**Invoer**</span><span class="sxs-lookup"><span data-stu-id="9cbc5-168">**Entry**</span></span>      |<span data-ttu-id="9cbc5-169">**Interpretatie**</span><span class="sxs-lookup"><span data-stu-id="9cbc5-169">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="9cbc5-170">2018.12.31.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-170">2018.12.31.</span></span>|<span data-ttu-id="9cbc5-171">31.12.2018.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-171">2018.12.31.</span></span>|
|<span data-ttu-id="9cbc5-172">181231</span><span class="sxs-lookup"><span data-stu-id="9cbc5-172">181231</span></span>|<span data-ttu-id="9cbc5-173">31.12.2018.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-173">2018.12.31.</span></span>|
|<span data-ttu-id="9cbc5-174">18.12.31.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-174">18.12.31.</span></span>|<span data-ttu-id="9cbc5-175">31.12.2018.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-175">2018.12.31.</span></span>|
|<span data-ttu-id="9cbc5-176">18.12.31.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-176">18.12.31.</span></span>|<span data-ttu-id="9cbc5-177">31.12.2018.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-177">2018.12.31.</span></span>|
|<span data-ttu-id="9cbc5-178">20181231</span><span class="sxs-lookup"><span data-stu-id="9cbc5-178">20181231</span></span>|<span data-ttu-id="9cbc5-179">31.12.2018.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-179">2018.12.31.</span></span>|
|<span data-ttu-id="9cbc5-180">18/12,31</span><span class="sxs-lookup"><span data-stu-id="9cbc5-180">18/12,31</span></span>|<span data-ttu-id="9cbc5-181">31.12.2018.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-181">2018.12.31.</span></span>|
|<span data-ttu-id="9cbc5-182">11</span><span class="sxs-lookup"><span data-stu-id="9cbc5-182">11</span></span>|<span data-ttu-id="9cbc5-183">jaar van werkdatum.maand van werkdatum.11.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-183">work date year.work date month.11.</span></span>|
|<span data-ttu-id="9cbc5-184">1112</span><span class="sxs-lookup"><span data-stu-id="9cbc5-184">1112</span></span>|<span data-ttu-id="9cbc5-185">jaar van werkdatum.11.12.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-185">work date year.11.12.</span></span>|
|<span data-ttu-id="9cbc5-186">h of huidige datum</span><span class="sxs-lookup"><span data-stu-id="9cbc5-186">t or today</span></span>|<span data-ttu-id="9cbc5-187">datum van vandaag</span><span class="sxs-lookup"><span data-stu-id="9cbc5-187">today's date</span></span>|
|<span data-ttu-id="9cbc5-188">p4</span><span class="sxs-lookup"><span data-stu-id="9cbc5-188">p4</span></span>|<span data-ttu-id="9cbc5-189">datumbereik dat de vierde boekhoudperiode bevat, bijvoorbeeld 1.4.20..30.4.20</span><span class="sxs-lookup"><span data-stu-id="9cbc5-189">date range that includes the fourth accounting period, such as 04/01/20..04/30/20</span></span>|
|<span data-ttu-id="9cbc5-190">w of werkdatum</span><span class="sxs-lookup"><span data-stu-id="9cbc5-190">w or workdate</span></span>|<span data-ttu-id="9cbc5-191">de werkdatum</span><span class="sxs-lookup"><span data-stu-id="9cbc5-191">the working date</span></span>|
|<span data-ttu-id="9cbc5-192">ma of maandag</span><span class="sxs-lookup"><span data-stu-id="9cbc5-192">m or Monday</span></span>|<span data-ttu-id="9cbc5-193">Maandag van de werkdatumweek</span><span class="sxs-lookup"><span data-stu-id="9cbc5-193">Monday of the work date week</span></span>|
|<span data-ttu-id="9cbc5-194">di of dinsdag</span><span class="sxs-lookup"><span data-stu-id="9cbc5-194">tu or Tuesday</span></span>|<span data-ttu-id="9cbc5-195">Dinsdag van de werkdatumweek</span><span class="sxs-lookup"><span data-stu-id="9cbc5-195">Tuesday of the work date week</span></span>|
|<span data-ttu-id="9cbc5-196">za of zaterdag</span><span class="sxs-lookup"><span data-stu-id="9cbc5-196">sa or Saturday</span></span>|<span data-ttu-id="9cbc5-197">Zaterdag van de werkdatumweek</span><span class="sxs-lookup"><span data-stu-id="9cbc5-197">Saturday of the work date week</span></span>|
|<span data-ttu-id="9cbc5-198">z of zondag</span><span class="sxs-lookup"><span data-stu-id="9cbc5-198">s or Sunday</span></span>|<span data-ttu-id="9cbc5-199">Zondag van de werkdatumweek</span><span class="sxs-lookup"><span data-stu-id="9cbc5-199">Sunday of the work date week</span></span>|
|<span data-ttu-id="9cbc5-200">d23</span><span class="sxs-lookup"><span data-stu-id="9cbc5-200">t23</span></span>|<span data-ttu-id="9cbc5-201">Dinsdag van week 23 van het werkdatumjaar</span><span class="sxs-lookup"><span data-stu-id="9cbc5-201">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="9cbc5-202">d 23</span><span class="sxs-lookup"><span data-stu-id="9cbc5-202">t 23</span></span>|<span data-ttu-id="9cbc5-203">Dinsdag van week 23 van het werkdatumjaar</span><span class="sxs-lookup"><span data-stu-id="9cbc5-203">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="9cbc5-204">d-1</span><span class="sxs-lookup"><span data-stu-id="9cbc5-204">t-1</span></span>|<span data-ttu-id="9cbc5-205">Dinsdag van week 1 van het werkdatumjaar</span><span class="sxs-lookup"><span data-stu-id="9cbc5-205">Tuesday of week 1 of the work date year</span></span>|

##  <a name="setting-ranges"></a><a name="BKMK_SettingDateRanges"></a> <span data-ttu-id="9cbc5-206">Datumbereiken instellen</span><span class="sxs-lookup"><span data-stu-id="9cbc5-206">Setting Ranges</span></span>

<span data-ttu-id="9cbc5-207">In lijsten, totalen en rapporten kunt u filters instellen op datum, tijden en datumtijden. De filters kunnen een begindatum en desgewenst een einddatum bevatten om alleen de gegevens uit dat bereik weer te geven.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-207">On lists, totals and reports, you can set filters on dates, times and datetimes containing a start value and optionally an end value to display only the data contained in that range.</span></span> <span data-ttu-id="9cbc5-208">Voor het instellen van een datumbereik gelden de standaardregels.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-208">The standard rules apply to the way you set date ranges.</span></span>

|<span data-ttu-id="9cbc5-209">**Betekenis**</span><span class="sxs-lookup"><span data-stu-id="9cbc5-209">**Meaning**</span></span>|<span data-ttu-id="9cbc5-210">**Voorbeeldexpressie (datum)**</span><span class="sxs-lookup"><span data-stu-id="9cbc5-210">**Sample expression (Date)**</span></span>|<span data-ttu-id="9cbc5-211">**Gegevens opgenomen in het filter**</span><span class="sxs-lookup"><span data-stu-id="9cbc5-211">**Data included in the filter**</span></span>|
|-----------|---------------------|--------------------|
|<span data-ttu-id="9cbc5-212">Interval</span><span class="sxs-lookup"><span data-stu-id="9cbc5-212">Interval</span></span>|<span data-ttu-id="9cbc5-213">15.12.00..15.01.01</span><span class="sxs-lookup"><span data-stu-id="9cbc5-213">12 15 00..01 15 01</span></span><br /><br /><span data-ttu-id="9cbc5-214">..15.12.00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-214">..12 15 00</span></span><br /><br /><span data-ttu-id="9cbc5-215">p1..p4</span><span class="sxs-lookup"><span data-stu-id="9cbc5-215">p1..p4</span></span>|<span data-ttu-id="9cbc5-216">Records met datums tussen 15.12.00 en 15.01.01.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-216">Records with dates between and including 12 15 00 and 01 15 01.</span></span><br /><br /><span data-ttu-id="9cbc5-217">Records met datums van 15.12.00 of eerder.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-217">Records with dates of 12 15 00 or earlier.</span></span><br /><br /><span data-ttu-id="9cbc5-218">Datumbereik dat de tweede, derde en vierde boekhoudperiode bevat, bijvoorbeeld 1.1.20..30.4.20..</span><span class="sxs-lookup"><span data-stu-id="9cbc5-218">Date range that includes the second, third, and fourth accounting periods, such as 01/01/20..04/30/20.</span></span>|
|<span data-ttu-id="9cbc5-219">Of/of</span><span class="sxs-lookup"><span data-stu-id="9cbc5-219">Either/or</span></span>|<span data-ttu-id="9cbc5-220">12 15 00\|12 16 00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-220">12 15 00\|12 16 00</span></span>|<span data-ttu-id="9cbc5-221">Records met datums van of 15.12.00 of 16.12.00.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-221">Records with dates of either 12 15 00 or 12 16 00.</span></span> <span data-ttu-id="9cbc5-222">Als er records zijn met datums op beide dagen, worden ze allemaal weergegeven.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-222">If there are records with dates on both days, they will all be displayed.</span></span>|
|<span data-ttu-id="9cbc5-223">Combinatie</span><span class="sxs-lookup"><span data-stu-id="9cbc5-223">Combination</span></span>|<span data-ttu-id="9cbc5-224">12 15 00\|12 01 00..12 10 00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-224">12 15 00\|12 01 00..12 10 00</span></span>  <br /><br /><span data-ttu-id="9cbc5-225">..12 14 00\|12 30 00..</span><span class="sxs-lookup"><span data-stu-id="9cbc5-225">..12 14 00\|12 30 00..</span></span>|<span data-ttu-id="9cbc5-226">Records met datums van 15.12.00 of op datums in de periode 01.12.00 t/m 10.12.00.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-226">Records with dates of 12 15 00 or on dates between and including 12 01 00 and 12 10 00.</span></span>  <br /><br /><span data-ttu-id="9cbc5-227">Records met datums van 12-14 00 of eerder, of datums van 12 30 00 of later. Dit wil zeggen, alle records, behalve records met datums tussen 12 15 00 en 12 29 00.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-227">Records with dates of 12 14 00 or earlier, or dates of 12 30 00 or later, that is, all records except those with dates between and including 12 15 00 and 12 29 00.</span></span>|

<span data-ttu-id="9cbc5-228">U kunt iedere geldige indeling in datumbereikfilters gebruiken.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-228">You can use any of the valid formats in date range filters.</span></span> <span data-ttu-id="9cbc5-229">Bijvoorbeeld maa14 3..v 4p, toegepast op een datum/tijd-veld leidt tot een filter van 3 uur 's morgens op maandag, in week 14 van het huidige werkdatumjaar tot en met vandaag om 4 uur 's middags.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-229">For example, mon14 3..t 4p applied on a datetime field results in a filter from 3 AM on Monday in week 14 of the current work date year, inclusive, until today at 4PM, inclusive.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="9cbc5-230">Datumformules gebruiken</span><span class="sxs-lookup"><span data-stu-id="9cbc5-230">Using Date Formulas</span></span>
<span data-ttu-id="9cbc5-231">Een datumformule is een korte, afgekorte combinatie van letters en cijfers op basis waarvan datums worden berekend.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-231">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="9cbc5-232">U kunt datumformules invoeren in verschillende datumberekeningsvelden of -filters.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-232">You can enter date formulas in various date calculation fields or filters.</span></span>

> [!NOTE]
>  <span data-ttu-id="9cbc5-233">In alle datumformulevelden wordt automatisch één dag opgenomen om ervoor te zorgen dat de huidige dag wordt gebruikt als begindatum van de periode.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-233">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="9cbc5-234">Als u dus bijvoorbeeld 1W invoert, zal de periode in feite acht dagen bestrijken omdat vandaag ook wordt opgenomen.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-234">Accordingly, for example, if you enter 1W, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="9cbc5-235">Als u een periode van zeven dagen \(exact één week\) wilt opgeven, inclusief de begindatum van de periode, moet u 6D of 1W-1D opgeven.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-235">To specify a period of seven days \(one true week\) including the period starting date, then you must enter 6D or 1W-1D.</span></span>

<span data-ttu-id="9cbc5-236">Hier volgen enkele voorbeelden van het gebruik van datumformules:</span><span class="sxs-lookup"><span data-stu-id="9cbc5-236">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="9cbc5-237">De datumformule in de frequentievelden van periodieke dagboeken geeft aan hoe vaak de dagboekregel moet worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-237">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="9cbc5-238">De datumformule in het veld **Respijtperiode** van een bepaald aanmaningsniveau bepaalt hoelang de vervaldatum \(of de datum van de vorige aanmaning\) moet zijn verstreken voordat een aanmaning wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-238">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date \(or from the date of the previous reminder\) before a reminder will be created.</span></span>

-   <span data-ttu-id="9cbc5-239">De datumformule in het veld **Vervaldatumformule** bepaalt hoe de vervaldatum voor de aanmaning wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-239">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="9cbc5-240">De datumformule kan maximaal 20 tekens bevatten (cijfers en letters).</span><span class="sxs-lookup"><span data-stu-id="9cbc5-240">The date formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="9cbc5-241">U kunt de volgende letters gebruiken als afkorting voor kalendereenheden.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-241">You can use the following letters, which are abbreviations for calendar units.</span></span>

|  <span data-ttu-id="9cbc5-242">Letter</span><span class="sxs-lookup"><span data-stu-id="9cbc5-242">Letter</span></span>  |  <span data-ttu-id="9cbc5-243">Betekenis</span><span class="sxs-lookup"><span data-stu-id="9cbc5-243">Meaning</span></span>  |
|----------|----------------------|
|<span data-ttu-id="9cbc5-244">H</span><span class="sxs-lookup"><span data-stu-id="9cbc5-244">C</span></span>|<span data-ttu-id="9cbc5-245">Huidig</span><span class="sxs-lookup"><span data-stu-id="9cbc5-245">Current</span></span>|
|<span data-ttu-id="9cbc5-246">D</span><span class="sxs-lookup"><span data-stu-id="9cbc5-246">D</span></span>|<span data-ttu-id="9cbc5-247">Dag\(en\)</span><span class="sxs-lookup"><span data-stu-id="9cbc5-247">Day\(s\)</span></span>|
|<span data-ttu-id="9cbc5-248">W</span><span class="sxs-lookup"><span data-stu-id="9cbc5-248">W</span></span>|<span data-ttu-id="9cbc5-249">We(e)k\(en\)</span><span class="sxs-lookup"><span data-stu-id="9cbc5-249">Week\(s\)</span></span>|
|<span data-ttu-id="9cbc5-250">M</span><span class="sxs-lookup"><span data-stu-id="9cbc5-250">M</span></span>|<span data-ttu-id="9cbc5-251">Maand\(en\)</span><span class="sxs-lookup"><span data-stu-id="9cbc5-251">Month\(s\)</span></span>|
|<span data-ttu-id="9cbc5-252">K</span><span class="sxs-lookup"><span data-stu-id="9cbc5-252">Q</span></span>|<span data-ttu-id="9cbc5-253">Kwarta(a)l\(en\)</span><span class="sxs-lookup"><span data-stu-id="9cbc5-253">Quarter\(s\)</span></span>|
|<span data-ttu-id="9cbc5-254">J</span><span class="sxs-lookup"><span data-stu-id="9cbc5-254">Y</span></span>|<span data-ttu-id="9cbc5-255">Ja(a)r\(en\)</span><span class="sxs-lookup"><span data-stu-id="9cbc5-255">Year\(s\)</span></span>|

<span data-ttu-id="9cbc5-256">Er zijn drie soorten datumformules.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-256">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="9cbc5-257">In het volgende voorbeeld wordt weergegeven hoe H kan worden gebruikt voor huidig en een tijdseenheid.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-257">The following example shows how to use C, for current, and a time unit.</span></span>

|  <span data-ttu-id="9cbc5-258">Expressie</span><span class="sxs-lookup"><span data-stu-id="9cbc5-258">Expression</span></span>  |  <span data-ttu-id="9cbc5-259">Betekenis</span><span class="sxs-lookup"><span data-stu-id="9cbc5-259">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="9cbc5-260">LW</span><span class="sxs-lookup"><span data-stu-id="9cbc5-260">CW</span></span>|<span data-ttu-id="9cbc5-261">Lopende week</span><span class="sxs-lookup"><span data-stu-id="9cbc5-261">Current week</span></span>|
|<span data-ttu-id="9cbc5-262">LM</span><span class="sxs-lookup"><span data-stu-id="9cbc5-262">CM</span></span>|<span data-ttu-id="9cbc5-263">Lopende maand</span><span class="sxs-lookup"><span data-stu-id="9cbc5-263">Current month</span></span>|

<span data-ttu-id="9cbc5-264">In het volgende voorbeeld wordt weergegeven hoe een getal en een tijdseenheid moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-264">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="9cbc5-265">Nummers mogen niet groter zijn dan 9999.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-265">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="9cbc5-266">Expressie</span><span class="sxs-lookup"><span data-stu-id="9cbc5-266">Expression</span></span>  |  <span data-ttu-id="9cbc5-267">Betekenis</span><span class="sxs-lookup"><span data-stu-id="9cbc5-267">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="9cbc5-268">10D</span><span class="sxs-lookup"><span data-stu-id="9cbc5-268">10D</span></span>|<span data-ttu-id="9cbc5-269">10 dagen vanaf vandaag</span><span class="sxs-lookup"><span data-stu-id="9cbc5-269">10 days from today</span></span>|
|<span data-ttu-id="9cbc5-270">2W</span><span class="sxs-lookup"><span data-stu-id="9cbc5-270">2W</span></span>|<span data-ttu-id="9cbc5-271">2 weken vanaf vandaag</span><span class="sxs-lookup"><span data-stu-id="9cbc5-271">2 weeks from today</span></span>|

<span data-ttu-id="9cbc5-272">In het volgende voorbeeld wordt weergegeven hoe een tijdseenheid en een getal moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-272">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="9cbc5-273">Expressie</span><span class="sxs-lookup"><span data-stu-id="9cbc5-273">Expression</span></span>  |  <span data-ttu-id="9cbc5-274">Betekenis</span><span class="sxs-lookup"><span data-stu-id="9cbc5-274">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="9cbc5-275">D10</span><span class="sxs-lookup"><span data-stu-id="9cbc5-275">D10</span></span>|<span data-ttu-id="9cbc5-276">De volgende tiende dag van een maand</span><span class="sxs-lookup"><span data-stu-id="9cbc5-276">The next 10th day of a month</span></span>|
|<span data-ttu-id="9cbc5-277">WD4</span><span class="sxs-lookup"><span data-stu-id="9cbc5-277">WD4</span></span>|<span data-ttu-id="9cbc5-278">De volgende vierde dag van een week \(donderdag\)</span><span class="sxs-lookup"><span data-stu-id="9cbc5-278">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="9cbc5-279">Het volgende voorbeeld geeft weer hoe u deze drie soorten naar wens kunt combineren.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-279">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="9cbc5-280">Expressie</span><span class="sxs-lookup"><span data-stu-id="9cbc5-280">Expression</span></span>  |  <span data-ttu-id="9cbc5-281">Betekenis</span><span class="sxs-lookup"><span data-stu-id="9cbc5-281">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="9cbc5-282">LM+10D</span><span class="sxs-lookup"><span data-stu-id="9cbc5-282">CM+10D</span></span>|<span data-ttu-id="9cbc5-283">Lopende maand \+ 10 dagen</span><span class="sxs-lookup"><span data-stu-id="9cbc5-283">Current month \+ 10 days</span></span>|

<span data-ttu-id="9cbc5-284">In het volgende voorbeeld ziet u hoe u een minteken gebruikt om een datum in het verleden aan te duiden.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-284">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="9cbc5-285">Expressie</span><span class="sxs-lookup"><span data-stu-id="9cbc5-285">Expression</span></span>  |  <span data-ttu-id="9cbc5-286">Betekenis</span><span class="sxs-lookup"><span data-stu-id="9cbc5-286">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="9cbc5-287">-1J</span><span class="sxs-lookup"><span data-stu-id="9cbc5-287">-1Y</span></span>|<span data-ttu-id="9cbc5-288">1 jaar geleden vanaf vandaag</span><span class="sxs-lookup"><span data-stu-id="9cbc5-288">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="9cbc5-289">Als de vestiging een basisagenda gebruikt, wordt de datumformule die u invoert in dit veld, bijvoorbeeld het veld **Verzendtijd** beschouwd als agendawerkdag.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-289">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="9cbc5-290">Bijvoorbeeld: 1W betekent zeven werkdagen.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-290">For example, 1W  means seven working days.</span></span>
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

## <a name="entering-times"></a><span data-ttu-id="9cbc5-291">Tijden invoeren</span><span class="sxs-lookup"><span data-stu-id="9cbc5-291">Entering Times</span></span>
<span data-ttu-id="9cbc5-292">Wanneer u tijden invoert, kunt u alle gewenste niet-spatie scheidingstekens invoegen tussen de eenheden, maar als u dubbele cijfers gebruikt voor elke eenheid tot aan milliseconden, is het niet vereist.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-292">When you enter times, you can insert any non-space separators that you want between the units, but if you use double digits for each unit up to milliseconds, then it is not required.</span></span>

<span data-ttu-id="9cbc5-293">U hoeft de alleen grootste eenheden te gebruiken die u nodig hebt. De rest wordt op nul ingesteld.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-293">You only have to write the largest units that you require; the rest will be set to zero.</span></span> <span data-ttu-id="9cbc5-294">U kunt de AM/PM-indicator ook weglaten.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-294">You can also leave out any AM/PM indicator.</span></span>

<span data-ttu-id="9cbc5-295">In de volgende tabel wordt aangegeven op welke manieren u tijden kunt invoeren en hoe de invoer wordt geïnterpreteerd.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-295">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span> <span data-ttu-id="9cbc5-296">Er wordt uitgegaan van een regio-instelling die tijden noteert volgens: **Uren:Minuten:Seconden.Milliseconden.**</span><span class="sxs-lookup"><span data-stu-id="9cbc5-296">It assumes region settings that format times according to: **Hours:Minutes:Seconds.Milliseconds.**</span></span> <span data-ttu-id="9cbc5-297">en die respectievelijk de indicatoren 'AM' en 'PM' gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-297">and use the AM and PM indicators of 'AM' and 'PM', respectively.</span></span>

|<span data-ttu-id="9cbc5-298">**Invoer**</span><span class="sxs-lookup"><span data-stu-id="9cbc5-298">**Entry**</span></span>      |<span data-ttu-id="9cbc5-299">**Interpretatie**</span><span class="sxs-lookup"><span data-stu-id="9cbc5-299">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="9cbc5-300">05:23:17</span><span class="sxs-lookup"><span data-stu-id="9cbc5-300">05:23:17</span></span>|<span data-ttu-id="9cbc5-301">05:23:17</span><span class="sxs-lookup"><span data-stu-id="9cbc5-301">05:23:17</span></span>|
|<span data-ttu-id="9cbc5-302">5</span><span class="sxs-lookup"><span data-stu-id="9cbc5-302">5</span></span>|<span data-ttu-id="9cbc5-303">05:00:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-303">05:00:00</span></span>|
|<span data-ttu-id="9cbc5-304">5AM</span><span class="sxs-lookup"><span data-stu-id="9cbc5-304">5AM</span></span>|<span data-ttu-id="9cbc5-305">05:00:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-305">05:00:00</span></span>|
|<span data-ttu-id="9cbc5-306">5P</span><span class="sxs-lookup"><span data-stu-id="9cbc5-306">5P</span></span>|<span data-ttu-id="9cbc5-307">17:00:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-307">17:00:00</span></span>|
|<span data-ttu-id="9cbc5-308">12</span><span class="sxs-lookup"><span data-stu-id="9cbc5-308">12</span></span>|<span data-ttu-id="9cbc5-309">12:00:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-309">12:00:00</span></span>|
|<span data-ttu-id="9cbc5-310">12A</span><span class="sxs-lookup"><span data-stu-id="9cbc5-310">12A</span></span>|<span data-ttu-id="9cbc5-311">00:00:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-311">00:00:00</span></span>|
|<span data-ttu-id="9cbc5-312">12P</span><span class="sxs-lookup"><span data-stu-id="9cbc5-312">12P</span></span>|<span data-ttu-id="9cbc5-313">12:00:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-313">12:00:00</span></span>|
|<span data-ttu-id="9cbc5-314">17</span><span class="sxs-lookup"><span data-stu-id="9cbc5-314">17</span></span>|<span data-ttu-id="9cbc5-315">17:00:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-315">17:00:00</span></span>|
|<span data-ttu-id="9cbc5-316">5:30</span><span class="sxs-lookup"><span data-stu-id="9cbc5-316">5:30</span></span>|<span data-ttu-id="9cbc5-317">05:30:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-317">05:30:00</span></span>|
|<span data-ttu-id="9cbc5-318">0530</span><span class="sxs-lookup"><span data-stu-id="9cbc5-318">0530</span></span>|<span data-ttu-id="9cbc5-319">05:30:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-319">05:30:00</span></span>|
|<span data-ttu-id="9cbc5-320">5:30:5</span><span class="sxs-lookup"><span data-stu-id="9cbc5-320">5:30:5</span></span>|<span data-ttu-id="9cbc5-321">05:30:05</span><span class="sxs-lookup"><span data-stu-id="9cbc5-321">05:30:05</span></span>|
|<span data-ttu-id="9cbc5-322">053005</span><span class="sxs-lookup"><span data-stu-id="9cbc5-322">053005</span></span>|<span data-ttu-id="9cbc5-323">05:30:05</span><span class="sxs-lookup"><span data-stu-id="9cbc5-323">05:30:05</span></span>|
|<span data-ttu-id="9cbc5-324">5:30:5.50</span><span class="sxs-lookup"><span data-stu-id="9cbc5-324">5:30:5,50</span></span>|<span data-ttu-id="9cbc5-325">05:30:05,5</span><span class="sxs-lookup"><span data-stu-id="9cbc5-325">05:30:05.5</span></span>|
|<span data-ttu-id="9cbc5-326">053005050</span><span class="sxs-lookup"><span data-stu-id="9cbc5-326">053005050</span></span>|<span data-ttu-id="9cbc5-327">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="9cbc5-327">05:30:05.05</span></span>|

<span data-ttu-id="9cbc5-328">Houd er rekening mee dat milliseconden als decimale notatie worden geïnterpreteerd.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-328">You should be aware that milliseconds are interpreted as decimal notation.</span></span> <span data-ttu-id="9cbc5-329">Bijvoorbeeld 3, 30 en 300 betekenen allemaal 300 milliseconden, en 03 betekent 30 en 003 betekent 3 milliseconden.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-329">So, for example, 3, 30, and 300 all mean 300 milliseconds, while 03 means 30 and 003 means 3 milliseconds.</span></span>

<span data-ttu-id="9cbc5-330">U kunt 24:00 niet voor middernacht gebruiken of een waarde groter dan 24:00 gebruiken.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-330">You cannot use 24:00 to mean midnight, or use any value greater than 24:00.</span></span>

<span data-ttu-id="9cbc5-331">Het woord voor 'tijd' in de taal die [!INCLUDE[prod_short](includes/prod_long.md)] gebruikt, wordt geëvalueerd als de huidige tijd op uw computer of mobiele apparaat.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-331">The word for 'time' in the language used by [!INCLUDE[prod_short](includes/prod_long.md)] will be evaluated to the current time on your computer or mobile device.</span></span> <span data-ttu-id="9cbc5-332">U kunt elk deel van het woord invoeren, beginnend bij het begin, zoals t of TIJ.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-332">You can enter any part of the word, starting from the beginning, such as t or TIM.</span></span>

## <a name="entering-combined-dates-and-times"></a><span data-ttu-id="9cbc5-333">Gecombineerde datums en tijden invoeren</span><span class="sxs-lookup"><span data-stu-id="9cbc5-333">Entering combined Dates and Times</span></span>
<span data-ttu-id="9cbc5-334">Wanneer u een datumtijd invoert (een datum en een tijd gecombineerd tot één veld), moet u een spatie invoeren tussen de datum en de tijd.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-334">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="9cbc5-335">Het datumdeel kan alleen spaties in de vorm van het officiële datumscheidingsteken van uw regio-instellingen bevatten.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-335">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="9cbc5-336">De tijd kan spaties bevatten rond de AM/PM-indicator.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-336">The time can contain spaces around the AM/PM indicator.</span></span>

<span data-ttu-id="9cbc5-337">Het is ook mogelijk alleen een datum in een datumtijdveld in te voeren, maar u kunt niet alleen een tijd invoeren.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-337">It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.</span></span>

<span data-ttu-id="9cbc5-338">In de volgende tabel staan enkele voorbeelden van datum/tijd-combinaties.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-338">The following table lists some examples of date/time combinations.</span></span> <span data-ttu-id="9cbc5-339">Met de regio-instellingen in de voorbeelden worden datums weergegeven in de notatie dag\-maand\-jaar, met AM/PM-indicatoren, Engelse taal en zondag als begin van de week.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-339">The region settings in the examples displays dates in the day\-month\-year format, using AM/PM designators, English language, and Sunday as the start of the week.</span></span>

|<span data-ttu-id="9cbc5-340">**Invoer**</span><span class="sxs-lookup"><span data-stu-id="9cbc5-340">**Entry**</span></span>      |<span data-ttu-id="9cbc5-341">**Interpretatie**</span><span class="sxs-lookup"><span data-stu-id="9cbc5-341">**Interpretation**</span></span>      |
|---------------|------------------------|
|<span data-ttu-id="9cbc5-342">08-01-2016 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="9cbc5-342">08-01-2016 05:48:12 PM</span></span>|<span data-ttu-id="9cbc5-343">08.01.2016 17:48:12</span><span class="sxs-lookup"><span data-stu-id="9cbc5-343">08\-01\-2016 05:48:12 PM</span></span>|
|<span data-ttu-id="9cbc5-344">131202 132455</span><span class="sxs-lookup"><span data-stu-id="9cbc5-344">131202 132455</span></span>|<span data-ttu-id="9cbc5-345">13.12.2002 13:24:55</span><span class="sxs-lookup"><span data-stu-id="9cbc5-345">13\-12\-2002 13:24:55</span></span>|
|<span data-ttu-id="9cbc5-346">1-12-02 10</span><span class="sxs-lookup"><span data-stu-id="9cbc5-346">1-12-02 10</span></span>|<span data-ttu-id="9cbc5-347">01.12.2002 10:00:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-347">01\-12\-2002 10:00:00</span></span>|
|<span data-ttu-id="9cbc5-348">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="9cbc5-348">1.12.02 5</span></span>|<span data-ttu-id="9cbc5-349">01.12.2002 05:00:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-349">01\-12\-2002 05:00:00</span></span>|
|<span data-ttu-id="9cbc5-350">1.12.02</span><span class="sxs-lookup"><span data-stu-id="9cbc5-350">1.12.02</span></span>|<span data-ttu-id="9cbc5-351">01.12.2002 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-351">01\-12\-2002 00:00:00</span></span>|
|<span data-ttu-id="9cbc5-352">11 12</span><span class="sxs-lookup"><span data-stu-id="9cbc5-352">11 12</span></span>|<span data-ttu-id="9cbc5-353">11.werkdatummaand.werkdatumjaar 12:00:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-353">11\-work date month\-work date year 12:00:00</span></span>|
|<span data-ttu-id="9cbc5-354">1112 12</span><span class="sxs-lookup"><span data-stu-id="9cbc5-354">1112 12</span></span>|<span data-ttu-id="9cbc5-355">11.12.werkdatumjaar 12:00:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-355">11\-12\-work date year 12:00:00</span></span>|
|<span data-ttu-id="9cbc5-356">h of huidige datum</span><span class="sxs-lookup"><span data-stu-id="9cbc5-356">t or today</span></span>|<span data-ttu-id="9cbc5-357">huidige datum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-357">today's date 00:00:00</span></span>|
|<span data-ttu-id="9cbc5-358">h 10:30</span><span class="sxs-lookup"><span data-stu-id="9cbc5-358">t 10:30</span></span>|<span data-ttu-id="9cbc5-359">huidige datum 10:30:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-359">today's date 10:30:00</span></span>|
|<span data-ttu-id="9cbc5-360">h 3:3:3</span><span class="sxs-lookup"><span data-stu-id="9cbc5-360">t 3:3:3</span></span>|<span data-ttu-id="9cbc5-361">huidige datum 03:03:03</span><span class="sxs-lookup"><span data-stu-id="9cbc5-361">today's date 03:03:03</span></span>|
|<span data-ttu-id="9cbc5-362">w of werkdatum</span><span class="sxs-lookup"><span data-stu-id="9cbc5-362">w or workdate</span></span>|<span data-ttu-id="9cbc5-363">de werkdatum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-363">the working date 00:00:00</span></span>|
|<span data-ttu-id="9cbc5-364">ma of maandag</span><span class="sxs-lookup"><span data-stu-id="9cbc5-364">m or Monday</span></span>|<span data-ttu-id="9cbc5-365">Maandag van de werkdatumweek 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-365">Monday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="9cbc5-366">di of dinsdag</span><span class="sxs-lookup"><span data-stu-id="9cbc5-366">tu or Tuesday</span></span>|<span data-ttu-id="9cbc5-367">Dinsdag van de werkdatumweek 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-367">Tuesday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="9cbc5-368">za of zaterdag</span><span class="sxs-lookup"><span data-stu-id="9cbc5-368">sa or Saturday</span></span>|<span data-ttu-id="9cbc5-369">Zaterdag van de werkdatumweek 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-369">Saturday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="9cbc5-370">z of zondag</span><span class="sxs-lookup"><span data-stu-id="9cbc5-370">s or Sunday</span></span>|<span data-ttu-id="9cbc5-371">Zondag van de werkdatumweek 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-371">Sunday of the work date week 00:00:00</span></span>|
|<span data-ttu-id="9cbc5-372">di 10:30</span><span class="sxs-lookup"><span data-stu-id="9cbc5-372">tu 10:30</span></span>|<span data-ttu-id="9cbc5-373">Dinsdag van de werkdatumweek 10:30:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-373">Tuesday of the work date week 10:30:00</span></span>|
|<span data-ttu-id="9cbc5-374">di 3:3:3</span><span class="sxs-lookup"><span data-stu-id="9cbc5-374">tu 3:3:3</span></span>|<span data-ttu-id="9cbc5-375">Dinsdag van de werkdatumweek 03:03:03</span><span class="sxs-lookup"><span data-stu-id="9cbc5-375">Tuesday of the work date week 03:03:03</span></span>|
|<span data-ttu-id="9cbc5-376">d23 t</span><span class="sxs-lookup"><span data-stu-id="9cbc5-376">t23 t</span></span>|<span data-ttu-id="9cbc5-377">Dinsdag van week 23 van het werkdatumjaar huidige tijd van dag</span><span class="sxs-lookup"><span data-stu-id="9cbc5-377">Tuesday of week 23 of the work date year, current time of day</span></span>|
|<span data-ttu-id="9cbc5-378">d23</span><span class="sxs-lookup"><span data-stu-id="9cbc5-378">t23</span></span>|<span data-ttu-id="9cbc5-379">Dinsdag van week 23 van het werkdatumjaar</span><span class="sxs-lookup"><span data-stu-id="9cbc5-379">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="9cbc5-380">d 23</span><span class="sxs-lookup"><span data-stu-id="9cbc5-380">t 23</span></span>|<span data-ttu-id="9cbc5-381">Vandaag 23:00:00</span><span class="sxs-lookup"><span data-stu-id="9cbc5-381">Today 23:00:00</span></span>|
|<span data-ttu-id="9cbc5-382">d-1</span><span class="sxs-lookup"><span data-stu-id="9cbc5-382">t-1</span></span>|<span data-ttu-id="9cbc5-383">Dinsdag van week 1 van het werkdatumjaar</span><span class="sxs-lookup"><span data-stu-id="9cbc5-383">Tuesday of week 1 of the work date year</span></span>|

## <a name="entering-duration"></a><span data-ttu-id="9cbc5-384">Duur invoeren</span><span class="sxs-lookup"><span data-stu-id="9cbc5-384">Entering Duration</span></span>
<span data-ttu-id="9cbc5-385">Sommige velden in toepassingsmodule vertegenwoordigen een duur of hoeveelheid verstreken tijd, in plaats van een specifieke datum of tijd.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-385">Some fields in the application represent a duration, or amount of elapsed time, instead of a specific date or time.</span></span> <span data-ttu-id="9cbc5-386">De duur moet worden ingevoerd als een getal gevolgd door de eenheid.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-386">You enter a duration as a number followed by its unit of measure.</span></span>

<span data-ttu-id="9cbc5-387">Hier volgen enkele voorbeelden.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-387">Here are some examples.</span></span>

|<span data-ttu-id="9cbc5-388">**Duur**</span><span class="sxs-lookup"><span data-stu-id="9cbc5-388">**Duration**</span></span>|<span data-ttu-id="9cbc5-389">**Eenheid**</span><span class="sxs-lookup"><span data-stu-id="9cbc5-389">**Unit of measure**</span></span>|
|------------|-------------------|
|<span data-ttu-id="9cbc5-390">2u</span><span class="sxs-lookup"><span data-stu-id="9cbc5-390">2h</span></span>|<span data-ttu-id="9cbc5-391">2 uur</span><span class="sxs-lookup"><span data-stu-id="9cbc5-391">2 hrs</span></span>|
|<span data-ttu-id="9cbc5-392">6u 30 m</span><span class="sxs-lookup"><span data-stu-id="9cbc5-392">6h 30 m</span></span>|<span data-ttu-id="9cbc5-393">6 uur en 30 minuten</span><span class="sxs-lookup"><span data-stu-id="9cbc5-393">6 hrs 30 mins</span></span>|
|<span data-ttu-id="9cbc5-394">6,5u</span><span class="sxs-lookup"><span data-stu-id="9cbc5-394">6.5h</span></span>|<span data-ttu-id="9cbc5-395">6 uur en 30 minuten</span><span class="sxs-lookup"><span data-stu-id="9cbc5-395">6 hrs 30 mins</span></span>|
|<span data-ttu-id="9cbc5-396">90m</span><span class="sxs-lookup"><span data-stu-id="9cbc5-396">90m</span></span>|<span data-ttu-id="9cbc5-397">1 uur en 30 minuten</span><span class="sxs-lookup"><span data-stu-id="9cbc5-397">1 hr 30 mins</span></span>|
|<span data-ttu-id="9cbc5-398">2d 6u 30m</span><span class="sxs-lookup"><span data-stu-id="9cbc5-398">2d 6h 30m</span></span>|<span data-ttu-id="9cbc5-399">2 dagen, 6 uur en 30 minuten</span><span class="sxs-lookup"><span data-stu-id="9cbc5-399">2 days 6 hrs 30 mins</span></span>|
|<span data-ttu-id="9cbc5-400">2d 6u 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="9cbc5-400">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="9cbc5-401">2 dagen, 6 uur, 30 minuten, 56 seconden en 600 milliseconden</span><span class="sxs-lookup"><span data-stu-id="9cbc5-401">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|

<span data-ttu-id="9cbc5-402">U kunt ook een getal invoeren, dat automatisch naar een duur wordt geconverteerd.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-402">You can also enter a number, which will be automatically converted to a duration.</span></span> <span data-ttu-id="9cbc5-403">Dit gebeurt op basis van de standaardeenheid die in het veld Duur is ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-403">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>

<span data-ttu-id="9cbc5-404">Als u wilt nagaan welke eenheid wordt gebruikt in het veld Duur, voert u een getal in en bekijkt u in welke eenheid het getal wordt omgezet.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-404">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>

<span data-ttu-id="9cbc5-405">Als de maateenheid bijvoorbeeld uren is, wordt het getal 5 bijvoorbeeld naar 5 uur geconverteerd.</span><span class="sxs-lookup"><span data-stu-id="9cbc5-405">For example, if the unit of measure is hours, the number 5 is converted to 5 hrs.</span></span>

## <a name="see-also"></a><span data-ttu-id="9cbc5-406">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9cbc5-406">See Also</span></span>
<span data-ttu-id="9cbc5-407">[Werken met [!INCLUDE[prod_short](includes/prod_long.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9cbc5-407">[Working with [!INCLUDE[prod_short](includes/prod_long.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="9cbc5-408">Datumberekening voor inkoop</span><span class="sxs-lookup"><span data-stu-id="9cbc5-408">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="9cbc5-409">Criteria in filters invoeren</span><span class="sxs-lookup"><span data-stu-id="9cbc5-409">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
