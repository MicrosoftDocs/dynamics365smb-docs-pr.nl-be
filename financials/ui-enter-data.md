---
title: Gegevens invoeren in velden | Microsoft Docs
description: Er zijn veel algemene functies waarmee u snel en gemakkelijk gegevens kunt invoeren. De algemene functies voor het invoeren van gegevens worden allemaal in dit onderwerp beschreven.
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/19/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 5f95efb5cad24db9848752035172bc7bb76db716
ms.contentlocale: nl-be
ms.lasthandoff: 09/27/2017

---
# <a name="entering-data"></a><span data-ttu-id="3d127-104">Gegevens invoeren</span><span class="sxs-lookup"><span data-stu-id="3d127-104">Entering Data</span></span>
<span data-ttu-id="3d127-105">Er zijn veel algemene functies waarmee u snel en gemakkelijk gegevens kunt invoeren.</span><span class="sxs-lookup"><span data-stu-id="3d127-105">There are many general functions that help you enter data  in a quick and easy way.</span></span> <span data-ttu-id="3d127-106">De algemene functies voor het invoeren van gegevens worden in dit artikel beschreven.</span><span class="sxs-lookup"><span data-stu-id="3d127-106">The general functions for entering data are described in this article.</span></span>  

<span data-ttu-id="3d127-107">In de voorbeelden in dit artikel worden de demonstratiegegevens gebruikt.</span><span class="sxs-lookup"><span data-stu-id="3d127-107">The examples in this article use the demonstration data.</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="3d127-108">Verplichte velden</span><span class="sxs-lookup"><span data-stu-id="3d127-108">Mandatory Fields</span></span>
<span data-ttu-id="3d127-109">Wanneer u gegevens invoert op pagina's, zijn bepaalde velden gemarkeerd met een rode asterisk.</span><span class="sxs-lookup"><span data-stu-id="3d127-109">When you enter data on pages, certain fields are marked with a red asterisk.</span></span> <span data-ttu-id="3d127-110">De rode asterisk betekent dat het veld moet worden ingevuld om een bepaald proces te voltooien dat het veld gebruikt, zoals het boeken van een transactie die de waarde in het veld gebruikt.</span><span class="sxs-lookup"><span data-stu-id="3d127-110">The red asterisk means that the field must be filled to complete a certain process that uses the field, such as posting a transaction that uses the value in the field.</span></span>  

<span data-ttu-id="3d127-111">Zelfs als het veld een rode asterisk bevat, wordt u niet gedwongen het veld te vullen voordat u verdergaat naar andere velden of de pagina sluit.</span><span class="sxs-lookup"><span data-stu-id="3d127-111">Even though the field contains a red asterisk, you are not forced to fill the field before you continue to other fields or close the page.</span></span> <span data-ttu-id="3d127-112">De rode asterisk dient alleen als een herinnering dat u wordt geblokkeerd van het voltooien van een bepaald proces.</span><span class="sxs-lookup"><span data-stu-id="3d127-112">The red asterisk only serves as a reminder that you will be blocked from completing a certain process.</span></span>  


## <a name="finding-data-as-you-type"></a><span data-ttu-id="3d127-113">Gegevens zoeken terwijl u typt</span><span class="sxs-lookup"><span data-stu-id="3d127-113">Finding Data As You Type</span></span>  
 <span data-ttu-id="3d127-114">Als u begint met het typen van tekens in een veld, wordt een vervolgkeuzelijst weergeven met de mogelijke veldwaarden.</span><span class="sxs-lookup"><span data-stu-id="3d127-114">When you start to type characters in a field, a drop-down list is displayed and shows possible field values.</span></span> <span data-ttu-id="3d127-115">De lijst verandert naarmate u meer tekens typt en u kunt de juiste waarde selecteren wanneer deze wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3d127-115">The list changes as you type more characters, and you can select the correct value when it is displayed.</span></span>  

 <span data-ttu-id="3d127-116">Veel velden hebben een knop met een pijl-omlaag die u kunt kiezen.</span><span class="sxs-lookup"><span data-stu-id="3d127-116">Many fields have a down arrow button that you can choose.</span></span> <span data-ttu-id="3d127-117">U kunt op de pijl klikken om een lijst met gegevens te krijgen die u in het veld kunt instellen.</span><span class="sxs-lookup"><span data-stu-id="3d127-117">You choose the arrow to get a list of data that is available to enter in the field.</span></span> <span data-ttu-id="3d127-118">De knop heeft twee functies, afhankelijk van het type veld:</span><span class="sxs-lookup"><span data-stu-id="3d127-118">The button has two functions depending on the type of field:</span></span>  

-   <span data-ttu-id="3d127-119">Opzoeken - Hiermee toont u gegevens uit een andere tabel die u in het veld kunt invoeren.</span><span class="sxs-lookup"><span data-stu-id="3d127-119">Lookup - Displays information from another table that you can enter in the field.</span></span> <span data-ttu-id="3d127-120">U kunt slechts één gegevensitem tegelijk selecteren.</span><span class="sxs-lookup"><span data-stu-id="3d127-120">You can select one piece of data at a time.</span></span>  

-   <span data-ttu-id="3d127-121">Vervolgkeuze - Hiermee toont u de verzameling opties die beschikbaar zijn voor het veld.</span><span class="sxs-lookup"><span data-stu-id="3d127-121">Drop-down - Displays the set of options that exist for the field.</span></span> <span data-ttu-id="3d127-122">U kunt slechts één optie tegelijk selecteren.</span><span class="sxs-lookup"><span data-stu-id="3d127-122">You can select only one of the options.</span></span>  

<!--Onprem ## Copy Fields or Lines  
 Depending on the type of writable document, you can copy individual line fields or whole lines to other lines in the document. Read-only data, such as posted entries, cannot be copied.  

 Several database dependencies are used to determine if fields or lines can be copied. One way to determine these dependencies is to view the shortcut menu. The content of the shortcut menu indicates which copy functions are supported by displaying either of these functions:  

-   Copy Cell  

-   Copy Rows  

-   Paste Rows  

 For example, database records, such as lines on a sales order, and master data, such as cards in the **Items** window, cannot be duplicated. For this kind of data, the shortcut menu typically has the **Copy Cell** or **Copy Rows**  functions. If the **Paste** function is not available this indicates that you can only paste the data into external documents. Single fields on a sales line, however, can be copied to the same column in other sales lines.  

 Journal lines are very flexible and can be copied freely in the same journal, indicated by the presence of **Paste** on the shortcut menu.  

> [!NOTE]  
>   If you copy a journal line or document line, the fields that are not in your view are not copied to the new line.

#### To copy previous field  

-   To enter the value of the field immediately above the active field, select **Copy Previous** from the shortcut menu.-->

## <a name="entering-quantities-by-calculation"></a><span data-ttu-id="3d127-123">Hoeveelheden invoeren door berekening</span><span class="sxs-lookup"><span data-stu-id="3d127-123">Entering Quantities by Calculation</span></span>  
 <span data-ttu-id="3d127-124">Als u getallen in velden voor hoeveelheden invoert, zoals het veld **Hoeveelheid** op een artikeldagboekregel, kunt u de formule invoeren in plaats van de totale hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="3d127-124">When entering numbers into quantity fields, such as the **Quantity** field on an item journal line, you can enter the formula instead of the sum quantity.</span></span>  

## <a name="examples"></a><span data-ttu-id="3d127-125">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="3d127-125">Examples</span></span>  

-   <span data-ttu-id="3d127-126">Als u 19+19 invoert, wordt het veld berekend als 38.</span><span class="sxs-lookup"><span data-stu-id="3d127-126">If you enter 19+19, the field is calculated to 38.</span></span>  

-   <span data-ttu-id="3d127-127">Als u 41-9, wordt het veld berekend als 32.</span><span class="sxs-lookup"><span data-stu-id="3d127-127">If you enter 41-9, the field is calculated to 32.</span></span>  

-   <span data-ttu-id="3d127-128">Als u 12*4 invoert, wordt het veld berekend als 48.</span><span class="sxs-lookup"><span data-stu-id="3d127-128">If you enter 12*4, the field is calculated to 48.</span></span>  

-   <span data-ttu-id="3d127-129">Als u 12/4 invoert, wordt het veld berekend als 3.</span><span class="sxs-lookup"><span data-stu-id="3d127-129">If you enter 12/4, the field is calculated to 3.</span></span>  

# <a name="entering-negative-numbers"></a><span data-ttu-id="3d127-130">Negatieve getallen invoeren</span><span class="sxs-lookup"><span data-stu-id="3d127-130">Entering Negative Numbers</span></span>
<span data-ttu-id="3d127-131">U kunt negatieve getallen op twee manieren invoeren.</span><span class="sxs-lookup"><span data-stu-id="3d127-131">You can enter negative numbers in two ways.</span></span> <span data-ttu-id="3d127-132">Nummer -20.5 kan worden ingevoerd als:</span><span class="sxs-lookup"><span data-stu-id="3d127-132">The number -20.5 can be entered as:</span></span>  

-   <span data-ttu-id="3d127-133">-20,5</span><span class="sxs-lookup"><span data-stu-id="3d127-133">-20.5</span></span>  

    <span data-ttu-id="3d127-134">of</span><span class="sxs-lookup"><span data-stu-id="3d127-134">or</span></span>
-   <span data-ttu-id="3d127-135">20,5-</span><span class="sxs-lookup"><span data-stu-id="3d127-135">20.5-</span></span>  

 <span data-ttu-id="3d127-136">In beide gevallen wordt het bedrag als -20,5 geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="3d127-136">In both cases, the amount will be recorded in as -20.5.</span></span>  

 <span data-ttu-id="3d127-137">Als het laatste teken van de expressie een **+** of een **-** is, wordt de volledige expressie vastgelegd met dat teken.</span><span class="sxs-lookup"><span data-stu-id="3d127-137">If the last character of the expression is a **+** or a **-**, the entire expression will be recorded with that sign.</span></span> <span data-ttu-id="3d127-138">Een voorbeeld: **10-20+** resulteert in 10 en niet -10.</span><span class="sxs-lookup"><span data-stu-id="3d127-138">An example, **10-20+** will result in 10 and not -10.</span></span>  

## <a name="entering-dates-and-times"></a><span data-ttu-id="3d127-139">Datums en tijden invoeren</span><span class="sxs-lookup"><span data-stu-id="3d127-139">Entering Dates and Times</span></span>
<span data-ttu-id="3d127-140">U kunt datums en tijden invoeren in alle velden die speciaal zijn toegewezen aan datums (datumvelden).</span><span class="sxs-lookup"><span data-stu-id="3d127-140">You can enter dates and times in all the fields that are specifically assigned to dates (date fields).</span></span> <span data-ttu-id="3d127-141">U kunt datums met of zonder scheidingstekens invoeren.</span><span class="sxs-lookup"><span data-stu-id="3d127-141">You can enter dates with or without separators.</span></span>

> [!NOTE]  
> <span data-ttu-id="3d127-142">Hoe u datums en tijden invoert, hangt af van uw instellingen onder **Regio**.</span><span class="sxs-lookup"><span data-stu-id="3d127-142">How you enter dates and times depends on your **Region** settings.</span></span> <span data-ttu-id="3d127-143">Zie voor meer informatie [Basisinstellingen wijzigen](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="3d127-143">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>  

### <a name="entering-dates"></a><span data-ttu-id="3d127-144">Datums invoeren</span><span class="sxs-lookup"><span data-stu-id="3d127-144">Entering Dates</span></span>  
 <span data-ttu-id="3d127-145">Een datumveld kan twee, vier, zes of acht cijfers bevatten:</span><span class="sxs-lookup"><span data-stu-id="3d127-145">In a date field you can enter two, four, six, or eight digits:</span></span>  

-   <span data-ttu-id="3d127-146">Als u slechts twee cijfers invoert, wordt dit als een dag beschouwd en wordt de maand en het jaar van de werkdag automatisch toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="3d127-146">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>  

-   <span data-ttu-id="3d127-147">Als u vier cijfers invoert, wordt dit als een dag en een maand beschouwd en wordt het jaar van de werkdag automatisch toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="3d127-147">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span>  

-   <span data-ttu-id="3d127-148">Als de ingevoerde datum in de reeks 01/01/1930 tot en met 31/12/2029 valt, hoeft u slechts twee cijfers voor het jaartal in te voeren; anders moet u vier cijfers voor het jaartal invoeren.</span><span class="sxs-lookup"><span data-stu-id="3d127-148">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>  

 <span data-ttu-id="3d127-149">U kunt een datum ook invoeren als een weekdag gevolgd door een weeknummer en eventueel het jaar (Ma25 of ma25 duidt bijvoorbeeld op maandag in week 25).</span><span class="sxs-lookup"><span data-stu-id="3d127-149">You can also enter a date as a weekday followed by a week number and, optionally, a year (for example, Mon25 or mon25 means Monday in week 25).</span></span>  

 <span data-ttu-id="3d127-150">U kunt in plaats van een specifieke datum ook een van de volgende codes invoeren.</span><span class="sxs-lookup"><span data-stu-id="3d127-150">Instead of entering a specific date, you can enter one of two codes.</span></span>  

|<span data-ttu-id="3d127-151">Code</span><span class="sxs-lookup"><span data-stu-id="3d127-151">Code</span></span>|<span data-ttu-id="3d127-152">Resultaat</span><span class="sxs-lookup"><span data-stu-id="3d127-152">Result</span></span>|  
|--------------|----------------|  
|<span data-ttu-id="3d127-153">h</span><span class="sxs-lookup"><span data-stu-id="3d127-153">t</span></span>|<span data-ttu-id="3d127-154">Dit is de datum van vandaag (de systeemdatum voor de computer).</span><span class="sxs-lookup"><span data-stu-id="3d127-154">This is today's date (the system date for the computer).</span></span>|  
|<span data-ttu-id="3d127-155">w</span><span class="sxs-lookup"><span data-stu-id="3d127-155">w</span></span>|<span data-ttu-id="3d127-156">Dit is de werkdatum die is ingesteld in de toepassing.</span><span class="sxs-lookup"><span data-stu-id="3d127-156">This is the work date that is setup in the application.</span></span> <span data-ttu-id="3d127-157">Zie [Basisinstellingen wijzigen](ui-change-basic-settings.md) als u de werkdatum wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="3d127-157">To change the work date, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span> <span data-ttu-id="3d127-158">Het gebruik van een werkdatum is handig als u veel transacties hebt met een andere datum dan de huidige.</span><span class="sxs-lookup"><span data-stu-id="3d127-158">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>|  

<!--Onprem ## Closing Date  
 When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry. A closing date technically is between two dates, for example between Dec 31 and Jan 1.  

 To specify that a date is a closing date, put C just before the date: C123101. -->

## <a name="entering-times"></a><span data-ttu-id="3d127-159">Tijden invoeren</span><span class="sxs-lookup"><span data-stu-id="3d127-159">Entering Times</span></span>  
 <span data-ttu-id="3d127-160">Hoewel het niet vereist is, kunt u bij de invoer van tijden elk willekeurig scheidingsteken tussen de eenheden plaatsen.</span><span class="sxs-lookup"><span data-stu-id="3d127-160">When you enter times, you can insert any separator sign that you want between the units, but it is not required.</span></span> <span data-ttu-id="3d127-161">U hoeft geen minuten, seconden of AM/PM-aanduiding in te voeren.</span><span class="sxs-lookup"><span data-stu-id="3d127-161">You do not have to write minutes, seconds, or AM/PM.</span></span>  

 <span data-ttu-id="3d127-162">In de volgende tabel wordt aangegeven op welke manieren u tijden kunt invoeren en hoe de invoer wordt geïnterpreteerd.</span><span class="sxs-lookup"><span data-stu-id="3d127-162">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span>  

|<span data-ttu-id="3d127-163">Post</span><span class="sxs-lookup"><span data-stu-id="3d127-163">Entry</span></span>|<span data-ttu-id="3d127-164">Interpretatie</span><span class="sxs-lookup"><span data-stu-id="3d127-164">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="3d127-165">5</span><span class="sxs-lookup"><span data-stu-id="3d127-165">5</span></span>|<span data-ttu-id="3d127-166">05:00:00</span><span class="sxs-lookup"><span data-stu-id="3d127-166">05:00:00</span></span>|  
|<span data-ttu-id="3d127-167">5:30</span><span class="sxs-lookup"><span data-stu-id="3d127-167">5:30</span></span>|<span data-ttu-id="3d127-168">05:30:00</span><span class="sxs-lookup"><span data-stu-id="3d127-168">05:30:00</span></span>|  
|<span data-ttu-id="3d127-169">0530</span><span class="sxs-lookup"><span data-stu-id="3d127-169">0530</span></span>|<span data-ttu-id="3d127-170">05:30:00</span><span class="sxs-lookup"><span data-stu-id="3d127-170">05:30:00</span></span>|  
|<span data-ttu-id="3d127-171">5:30:5</span><span class="sxs-lookup"><span data-stu-id="3d127-171">5:30:5</span></span>|<span data-ttu-id="3d127-172">05:30:05</span><span class="sxs-lookup"><span data-stu-id="3d127-172">05:30:05</span></span>|  
|<span data-ttu-id="3d127-173">053005</span><span class="sxs-lookup"><span data-stu-id="3d127-173">053005</span></span>|<span data-ttu-id="3d127-174">05:30:05</span><span class="sxs-lookup"><span data-stu-id="3d127-174">05:30:05</span></span>|  
|<span data-ttu-id="3d127-175">5:30:5.50</span><span class="sxs-lookup"><span data-stu-id="3d127-175">5:30:5,50</span></span>|<span data-ttu-id="3d127-176">05:30:05,5</span><span class="sxs-lookup"><span data-stu-id="3d127-176">05:30:05.5</span></span>|  
|<span data-ttu-id="3d127-177">053005050</span><span class="sxs-lookup"><span data-stu-id="3d127-177">053005050</span></span>|<span data-ttu-id="3d127-178">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="3d127-178">05:30:05.05</span></span>|  

 <span data-ttu-id="3d127-179">Als u geen scheidingsteken invoert, moet u twee cijfers invoeren voor elke eenheid.</span><span class="sxs-lookup"><span data-stu-id="3d127-179">You must enter two digits for each unit of time if you do not enter a separator.</span></span>  

## <a name="entering-datetimes"></a><span data-ttu-id="3d127-180">Datum/tijd invoeren</span><span class="sxs-lookup"><span data-stu-id="3d127-180">Entering Datetimes</span></span>  
 <span data-ttu-id="3d127-181">Wanneer u datum/tijd invoert, moet u een spatie plaatsen tussen de datum en de tijd.</span><span class="sxs-lookup"><span data-stu-id="3d127-181">When you enter datetimes you must enter a space between the date and the time.</span></span>  

 <span data-ttu-id="3d127-182">In de volgende tabel wordt aangegeven op welke manier u de datum/tijd kunt invoeren en hoe de verschillende manieren worden geïnterpreteerd.</span><span class="sxs-lookup"><span data-stu-id="3d127-182">The following table lists the various ways in which you can enter datetimes and how they are interpreted.</span></span>  

|<span data-ttu-id="3d127-183">Post</span><span class="sxs-lookup"><span data-stu-id="3d127-183">Entry</span></span>|<span data-ttu-id="3d127-184">Interpretatie</span><span class="sxs-lookup"><span data-stu-id="3d127-184">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="3d127-185">131202 132455</span><span class="sxs-lookup"><span data-stu-id="3d127-185">131202 132455</span></span>|<span data-ttu-id="3d127-186">13-12-02 13:24:55</span><span class="sxs-lookup"><span data-stu-id="3d127-186">13-12-02 13:24:55</span></span>|  
|<span data-ttu-id="3d127-187">1-12-02 10</span><span class="sxs-lookup"><span data-stu-id="3d127-187">1-12-02 10</span></span>|<span data-ttu-id="3d127-188">01-12-02 10:00:00</span><span class="sxs-lookup"><span data-stu-id="3d127-188">01-12-02 10:00:00</span></span>|  
|<span data-ttu-id="3d127-189">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="3d127-189">1.12.02 5</span></span>|<span data-ttu-id="3d127-190">01-12-02 05:00:00</span><span class="sxs-lookup"><span data-stu-id="3d127-190">01-12-02 05:00:00</span></span>|  
|<span data-ttu-id="3d127-191">1.12.02</span><span class="sxs-lookup"><span data-stu-id="3d127-191">1.12.02</span></span>|<span data-ttu-id="3d127-192">01-12-02 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3d127-192">01-12-02 00:00:00</span></span>|  
|<span data-ttu-id="3d127-193">11 12</span><span class="sxs-lookup"><span data-stu-id="3d127-193">11 12</span></span>|<span data-ttu-id="3d127-194">11-huidige maand-huidig jaar 12:00:00</span><span class="sxs-lookup"><span data-stu-id="3d127-194">11-current month-current year 12:00:00</span></span>|  
|<span data-ttu-id="3d127-195">1112 12</span><span class="sxs-lookup"><span data-stu-id="3d127-195">1112 12</span></span>|<span data-ttu-id="3d127-196">11-12-huidig jaar 12:00:00</span><span class="sxs-lookup"><span data-stu-id="3d127-196">11-12-current year 12:00:00</span></span>|  
|<span data-ttu-id="3d127-197">h of huidige datum</span><span class="sxs-lookup"><span data-stu-id="3d127-197">t or today</span></span>|<span data-ttu-id="3d127-198">huidige datum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3d127-198">today's date 00:00:00</span></span>|  
|<span data-ttu-id="3d127-199">h tijd</span><span class="sxs-lookup"><span data-stu-id="3d127-199">t time</span></span>|<span data-ttu-id="3d127-200">huidige datum werkelijke tijd</span><span class="sxs-lookup"><span data-stu-id="3d127-200">today's date actual time</span></span>|  
|<span data-ttu-id="3d127-201">h 10:30</span><span class="sxs-lookup"><span data-stu-id="3d127-201">t 10:30</span></span>|<span data-ttu-id="3d127-202">huidige datum 10:30:00</span><span class="sxs-lookup"><span data-stu-id="3d127-202">today's date 10:30:00</span></span>|  
|<span data-ttu-id="3d127-203">h 3:3:3</span><span class="sxs-lookup"><span data-stu-id="3d127-203">t 3:3:3</span></span>|<span data-ttu-id="3d127-204">huidige datum 03:03:03</span><span class="sxs-lookup"><span data-stu-id="3d127-204">today's date 03:03:03</span></span>|  
|<span data-ttu-id="3d127-205">w of werkdatum</span><span class="sxs-lookup"><span data-stu-id="3d127-205">w or workdate</span></span>|<span data-ttu-id="3d127-206">de werkdatum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3d127-206">the working date 00:00:00</span></span>|  
|<span data-ttu-id="3d127-207">ma of maandag</span><span class="sxs-lookup"><span data-stu-id="3d127-207">m or Monday</span></span>|<span data-ttu-id="3d127-208">Maandag van de huidige week 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3d127-208">Monday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="3d127-209">di of dinsdag</span><span class="sxs-lookup"><span data-stu-id="3d127-209">tu or Tuesday</span></span>|<span data-ttu-id="3d127-210">Dinsdag van de huidige week 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3d127-210">Tuesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="3d127-211">wo of woensdag</span><span class="sxs-lookup"><span data-stu-id="3d127-211">we or Wednesday</span></span>|<span data-ttu-id="3d127-212">Woensdag van de huidige week 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3d127-212">Wednesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="3d127-213">do of donderdag</span><span class="sxs-lookup"><span data-stu-id="3d127-213">th or Thursday</span></span>|<span data-ttu-id="3d127-214">Donderdag van de huidige week 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3d127-214">Thursday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="3d127-215">vr of vrijdag</span><span class="sxs-lookup"><span data-stu-id="3d127-215">f or Friday</span></span>|<span data-ttu-id="3d127-216">Vrijdag van de huidige week 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3d127-216">Friday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="3d127-217">za of zaterdag</span><span class="sxs-lookup"><span data-stu-id="3d127-217">s or Saturday</span></span>|<span data-ttu-id="3d127-218">Zaterdag van de huidige week 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3d127-218">Saturday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="3d127-219">zo of zondag</span><span class="sxs-lookup"><span data-stu-id="3d127-219">su or Sunday</span></span>|<span data-ttu-id="3d127-220">Zondag van de huidige week 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3d127-220">Sunday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="3d127-221">di 10:30</span><span class="sxs-lookup"><span data-stu-id="3d127-221">tu 10:30</span></span>|<span data-ttu-id="3d127-222">Dinsdag van de huidige week 10:30:00</span><span class="sxs-lookup"><span data-stu-id="3d127-222">Tuesday of the current week 10:30:00</span></span>|  
|<span data-ttu-id="3d127-223">di 3:3:3</span><span class="sxs-lookup"><span data-stu-id="3d127-223">tu 3:3:3</span></span>|<span data-ttu-id="3d127-224">Dinsdag van de huidige week 03:03:03</span><span class="sxs-lookup"><span data-stu-id="3d127-224">Tuesday of the current week 03:03:03</span></span>|  

## <a name="entering-duration"></a><span data-ttu-id="3d127-225">Duur invoeren</span><span class="sxs-lookup"><span data-stu-id="3d127-225">Entering Duration</span></span>  
 <span data-ttu-id="3d127-226">De duur moet worden ingevoerd als een getal gevolgd door de eenheid.</span><span class="sxs-lookup"><span data-stu-id="3d127-226">You enter a duration as a number followed by its unit of measure.</span></span>  

 <span data-ttu-id="3d127-227">Hier volgen enkele voorbeelden.</span><span class="sxs-lookup"><span data-stu-id="3d127-227">Here are some examples.</span></span>  

|<span data-ttu-id="3d127-228">Duur</span><span class="sxs-lookup"><span data-stu-id="3d127-228">Duration</span></span>|<span data-ttu-id="3d127-229">Eenheid**</span><span class="sxs-lookup"><span data-stu-id="3d127-229">Unit of measure**</span></span>|  
|------------------|-------------------------|  
|<span data-ttu-id="3d127-230">2u</span><span class="sxs-lookup"><span data-stu-id="3d127-230">2h</span></span>|<span data-ttu-id="3d127-231">2 uur</span><span class="sxs-lookup"><span data-stu-id="3d127-231">2 hrs</span></span>|  
|<span data-ttu-id="3d127-232">6u 30 m</span><span class="sxs-lookup"><span data-stu-id="3d127-232">6h 30 m</span></span>|<span data-ttu-id="3d127-233">6 uur en 30 minuten</span><span class="sxs-lookup"><span data-stu-id="3d127-233">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="3d127-234">6,5u</span><span class="sxs-lookup"><span data-stu-id="3d127-234">6.5h</span></span>|<span data-ttu-id="3d127-235">6 uur en 30 minuten</span><span class="sxs-lookup"><span data-stu-id="3d127-235">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="3d127-236">90m</span><span class="sxs-lookup"><span data-stu-id="3d127-236">90m</span></span>|<span data-ttu-id="3d127-237">1 uur en 30 minuten</span><span class="sxs-lookup"><span data-stu-id="3d127-237">1 hr 30 mins</span></span>|  
|<span data-ttu-id="3d127-238">2d 6u 30m</span><span class="sxs-lookup"><span data-stu-id="3d127-238">2d 6h 30m</span></span>|<span data-ttu-id="3d127-239">2 dagen, 6 uur en 30 minuten</span><span class="sxs-lookup"><span data-stu-id="3d127-239">2 days 6 hrs 30 mins</span></span>|  
|<span data-ttu-id="3d127-240">2d 6u 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="3d127-240">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="3d127-241">2 dagen, 6 uur, 30 minuten, 56 seconden en 600 milliseconden</span><span class="sxs-lookup"><span data-stu-id="3d127-241">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|  

 <span data-ttu-id="3d127-242">Als u een getal invoert, wordt het getal automatisch omgezet naar een duur.</span><span class="sxs-lookup"><span data-stu-id="3d127-242">You can also enter a number and it is automatically converted to a duration.</span></span> <span data-ttu-id="3d127-243">Dit gebeurt op basis van de standaardeenheid die in het veld Duur is ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="3d127-243">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>  

 <span data-ttu-id="3d127-244">Als u wilt nagaan welke eenheid wordt gebruikt in het veld Duur, voert u een getal in en bekijkt u in welke eenheid het getal wordt omgezet.</span><span class="sxs-lookup"><span data-stu-id="3d127-244">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>  

 <span data-ttu-id="3d127-245">Het getal 5 wordt omgezet in 5 uur, als de eenheid uit uren bestaat.</span><span class="sxs-lookup"><span data-stu-id="3d127-245">The number 5 is converted to 5 hrs, if the unit of measure is hours.</span></span>  

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|  -->

## <a name="using-date-formulas"></a><span data-ttu-id="3d127-246">Datumformules gebruiken</span><span class="sxs-lookup"><span data-stu-id="3d127-246">Using Date Formulas</span></span>  
 <span data-ttu-id="3d127-247">Een datumformule is een korte, afgekorte combinatie van letters en cijfers op basis waarvan datums worden berekend.</span><span class="sxs-lookup"><span data-stu-id="3d127-247">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="3d127-248">U kunt datumformules invoeren in verschillende datumberekeningsvelden en in de frequentievelden van periodieke dagboeken.</span><span class="sxs-lookup"><span data-stu-id="3d127-248">You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="3d127-249">In alle datumformulevelden wordt automatisch één dag opgenomen om ervoor te zorgen dat de huidige dag wordt gebruikt als begindatum van de periode.</span><span class="sxs-lookup"><span data-stu-id="3d127-249">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="3d127-250">Als u bijvoorbeeld 1W invoert, zal de periode in feite acht dagen bestrijken omdat vandaag ook is opgenomen.</span><span class="sxs-lookup"><span data-stu-id="3d127-250">Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="3d127-251">Als u een periode van zeven dagen (exact één week) wilt opgeven, inclusief de begindatum van de periode, moet u 6D of 1W-1D opgeven.</span><span class="sxs-lookup"><span data-stu-id="3d127-251">To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.</span></span>  

 <span data-ttu-id="3d127-252">Hier volgen enkele voorbeelden van het gebruik van datumformules:</span><span class="sxs-lookup"><span data-stu-id="3d127-252">Here are some examples of how date formulas can be used:</span></span>  

-   <span data-ttu-id="3d127-253">De datumformule in de frequentievelden van periodieke dagboeken geeft aan hoe vaak de dagboekregel moet worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="3d127-253">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>  

-   <span data-ttu-id="3d127-254">De datumformule in het veld Respijtperiode van een bepaald aanmaningsniveau bepaalt hoelang de vervaldatum (of de datum van de vorige aanmaning) moet zijn verstreken voordat een aanmaning wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="3d127-254">The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.</span></span>  

-   <span data-ttu-id="3d127-255">De datumformule in het veld Vervaldatumformule bepaalt hoe de vervaldatum voor de aanmaning wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="3d127-255">The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.</span></span>  

 <span data-ttu-id="3d127-256">In de berekeningsformule voor de datum kunt u maximaal 20 tekens gebruiken (cijfers en/of letters).</span><span class="sxs-lookup"><span data-stu-id="3d127-256">The date calculation formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="3d127-257">U kunt de volgende letters gebruiken als afkorting voor tijdsaanduidingen.</span><span class="sxs-lookup"><span data-stu-id="3d127-257">You can use the following letters, which are abbreviations for time specifications.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="3d127-258">L</span><span class="sxs-lookup"><span data-stu-id="3d127-258">C</span></span>|<span data-ttu-id="3d127-259">Lopend</span><span class="sxs-lookup"><span data-stu-id="3d127-259">Current</span></span>|  
|<span data-ttu-id="3d127-260">D</span><span class="sxs-lookup"><span data-stu-id="3d127-260">D</span></span>|<span data-ttu-id="3d127-261">Dag</span><span class="sxs-lookup"><span data-stu-id="3d127-261">Day(s)</span></span>|  
|<span data-ttu-id="3d127-262">W</span><span class="sxs-lookup"><span data-stu-id="3d127-262">W</span></span>|<span data-ttu-id="3d127-263">Week</span><span class="sxs-lookup"><span data-stu-id="3d127-263">Week(s)</span></span>|  
|<span data-ttu-id="3d127-264">M</span><span class="sxs-lookup"><span data-stu-id="3d127-264">M</span></span>|<span data-ttu-id="3d127-265">Maand</span><span class="sxs-lookup"><span data-stu-id="3d127-265">Month(s)</span></span>|  
|<span data-ttu-id="3d127-266">K</span><span class="sxs-lookup"><span data-stu-id="3d127-266">Q</span></span>|<span data-ttu-id="3d127-267">Kwartaal</span><span class="sxs-lookup"><span data-stu-id="3d127-267">Quarter(s)</span></span>|  
|<span data-ttu-id="3d127-268">J</span><span class="sxs-lookup"><span data-stu-id="3d127-268">Y</span></span>|<span data-ttu-id="3d127-269">Jaar</span><span class="sxs-lookup"><span data-stu-id="3d127-269">Year(s)</span></span>|  

 <span data-ttu-id="3d127-270">Er zijn drie soorten datumformules.</span><span class="sxs-lookup"><span data-stu-id="3d127-270">You can construct a date formula in three ways.</span></span>  

 <span data-ttu-id="3d127-271">In het volgende voorbeeld wordt weergegeven hoe huidig en een getal.</span><span class="sxs-lookup"><span data-stu-id="3d127-271">The following example shows how current plus a time unit.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="3d127-272">LW</span><span class="sxs-lookup"><span data-stu-id="3d127-272">CW</span></span>|<span data-ttu-id="3d127-273">Lopende week</span><span class="sxs-lookup"><span data-stu-id="3d127-273">Current week</span></span>|  
|<span data-ttu-id="3d127-274">LM</span><span class="sxs-lookup"><span data-stu-id="3d127-274">CM</span></span>|<span data-ttu-id="3d127-275">Lopende maand</span><span class="sxs-lookup"><span data-stu-id="3d127-275">Current month</span></span>|  

 <span data-ttu-id="3d127-276">In het volgende voorbeeld wordt weergegeven hoe een getal en een tijdseenheid.</span><span class="sxs-lookup"><span data-stu-id="3d127-276">The following example shows how a number and a time unit.</span></span> <span data-ttu-id="3d127-277">Nummers mogen niet groter zijn dan 9999.</span><span class="sxs-lookup"><span data-stu-id="3d127-277">A number cannot be larger than 9999.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="3d127-278">10D</span><span class="sxs-lookup"><span data-stu-id="3d127-278">10D</span></span>|<span data-ttu-id="3d127-279">10 dagen vanaf vandaag</span><span class="sxs-lookup"><span data-stu-id="3d127-279">10 days from today</span></span>|  
|<span data-ttu-id="3d127-280">2W</span><span class="sxs-lookup"><span data-stu-id="3d127-280">2W</span></span>|<span data-ttu-id="3d127-281">2 weken vanaf vandaag</span><span class="sxs-lookup"><span data-stu-id="3d127-281">2 weeks from today</span></span>|  

 <span data-ttu-id="3d127-282">In het volgende voorbeeld wordt weergegeven hoe een tijdseenheid en een getal.</span><span class="sxs-lookup"><span data-stu-id="3d127-282">The following example shows how a time unit and a number.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="3d127-283">D10</span><span class="sxs-lookup"><span data-stu-id="3d127-283">D10</span></span>|<span data-ttu-id="3d127-284">De volgende tiende dag van een maand</span><span class="sxs-lookup"><span data-stu-id="3d127-284">The next 10th day of a month</span></span>|  
|<span data-ttu-id="3d127-285">WD4</span><span class="sxs-lookup"><span data-stu-id="3d127-285">WD4</span></span>|<span data-ttu-id="3d127-286">De volgende vierde dag van een week (donderdag)</span><span class="sxs-lookup"><span data-stu-id="3d127-286">The next 4th day of a week (Thursday)</span></span>|  

 <span data-ttu-id="3d127-287">Het volgende voorbeeld geeft weer hoe u deze drie soorten naar wens kunt combineren.</span><span class="sxs-lookup"><span data-stu-id="3d127-287">The following example shows how you can combine these three forms as needed.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="3d127-288">LM+10D</span><span class="sxs-lookup"><span data-stu-id="3d127-288">CM+10D</span></span>|<span data-ttu-id="3d127-289">Lopende maand + 10 dagen</span><span class="sxs-lookup"><span data-stu-id="3d127-289">Current month + 10 days</span></span>|  

 <span data-ttu-id="3d127-290">In het volgende voorbeeld ziet u hoe u een minteken gebruikt om een datum in het verleden aan te duiden.</span><span class="sxs-lookup"><span data-stu-id="3d127-290">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>  

|||  
|-|-|  
|<span data-ttu-id="3d127-291">-1J</span><span class="sxs-lookup"><span data-stu-id="3d127-291">-1Y</span></span>|<span data-ttu-id="3d127-292">1 jaar geleden vanaf vandaag</span><span class="sxs-lookup"><span data-stu-id="3d127-292">1 year ago from today</span></span>|  

<!--OnPrem > [!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->  
## <a name="see-also"></a><span data-ttu-id="3d127-293">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3d127-293">See Also</span></span>  
 [<span data-ttu-id="3d127-294">Gegevens zoeken, filteren en sorteren</span><span class="sxs-lookup"><span data-stu-id="3d127-294">Searching, Filtering, and Sorting Data</span></span>](ui-enter-criteria-filters.md)  
 <span data-ttu-id="3d127-295">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3d127-295">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

