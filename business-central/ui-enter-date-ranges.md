---
title: Datumbereiken instellen in Business Central | Microsoft Docs
description: Leren hoe u een rapport kunt verkrijgen om gegevens te tonen uit specifieke tijdperioden met behulp van datumbereiken in Business Central.
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 07/05/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7664360941313da6ea0b797ef00df2e9810ad62
ms.openlocfilehash: ff63ae71a78f956dddb7b5247ee66f9416cf7cf1
ms.contentlocale: nl-be
ms.lasthandoff: 07/09/2018

---
# <a name="entering-date-ranges"></a><span data-ttu-id="ce932-103">Datumbereiken invoeren</span><span class="sxs-lookup"><span data-stu-id="ce932-103">Entering Date Ranges</span></span>
<span data-ttu-id="ce932-104">U kunt filters met een begin- en einddatum instellen om alleen de gegevens in dat datumbereik of tijdsinterval in te stellen.</span><span class="sxs-lookup"><span data-stu-id="ce932-104">You can set filters containing a start date and an end date to display only the data contained in that date range or time interval.</span></span> <span data-ttu-id="ce932-105">Voor het instellen van een datumbereik gelden speciale regels.</span><span class="sxs-lookup"><span data-stu-id="ce932-105">Special rules apply to the way you set date ranges.</span></span> <span data-ttu-id="ce932-106">Neem als voorbeeld de **Klanten top 10**:</span><span class="sxs-lookup"><span data-stu-id="ce932-106">Let's take the **Customer Top 10** as an example:</span></span>

![Een datumbereik instellen op de aanvraagpagina voor de lijst Klanten top 10](./media/ui-enter-date-ranges/customer-top10-list.png)

<span data-ttu-id="ce932-108">Hier kunt u de lijst tot een datumbereik beperken, zoals de afgelopen 2 weken of een totaal van 6 weken, of wat voor bereik u ook nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="ce932-108">Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want.</span></span> <span data-ttu-id="ce932-109">Als u datumbereiken wilt invoeren, voert u datums in en gebruikt u **..**</span><span class="sxs-lookup"><span data-stu-id="ce932-109">To set date ranges, you enter dates and then use either **..**</span></span> <span data-ttu-id="ce932-110">of **|** om het bereik in te stellen.</span><span class="sxs-lookup"><span data-stu-id="ce932-110">or **|** to set the range.</span></span> <span data-ttu-id="ce932-111">Als u in ons voorbeeld de top 10 klanten voor de eerste twee weken van mei wilt invoeren, stelt u het datumfilter in op *05 01 17..05 14 17*.</span><span class="sxs-lookup"><span data-stu-id="ce932-111">In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.</span></span>
<span data-ttu-id="ce932-112">Hier volgen enkele andere voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="ce932-112">Here are a couple of other examples:</span></span>

| <span data-ttu-id="ce932-113">Betekenis</span><span class="sxs-lookup"><span data-stu-id="ce932-113">Meaning</span></span> | <span data-ttu-id="ce932-114">Opmerking</span><span class="sxs-lookup"><span data-stu-id="ce932-114">Example</span></span> | <span data-ttu-id="ce932-115">Opgenomen posten</span><span class="sxs-lookup"><span data-stu-id="ce932-115">Entries included</span></span> |
|---|---|---|
|<span data-ttu-id="ce932-116">Gelijk aan</span><span class="sxs-lookup"><span data-stu-id="ce932-116">Equal to</span></span>| <span data-ttu-id="ce932-117">12 15 16</span><span class="sxs-lookup"><span data-stu-id="ce932-117">12 15 16</span></span> |<span data-ttu-id="ce932-118">Alleen posten die zijn geboekt op 15 december 2016.</span><span class="sxs-lookup"><span data-stu-id="ce932-118">Only those posted on December 15 2016.</span></span>|
|<span data-ttu-id="ce932-119">Interval</span><span class="sxs-lookup"><span data-stu-id="ce932-119">Interval</span></span>| <span data-ttu-id="ce932-120">12 15 16..01 15 17</span><span class="sxs-lookup"><span data-stu-id="ce932-120">12 15 16..01 15 17</span></span><br /><br /><span data-ttu-id="ce932-121">..12 15 16</span><span class="sxs-lookup"><span data-stu-id="ce932-121">..12 15 16</span></span>|<span data-ttu-id="ce932-122">Posten die zijn geboekt in de periode tussen en tot en met 15 december 2016 en 15 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="ce932-122">Those posted on dates between and including December 15 2016 and January 15 2017.</span></span><br /><br /><span data-ttu-id="ce932-123">Posten die zijn geboekt op 15 december 2016 of eerder.</span><span class="sxs-lookup"><span data-stu-id="ce932-123">Those posted on December 15 2016 or earlier.</span></span>|
|<span data-ttu-id="ce932-124">Of/of</span><span class="sxs-lookup"><span data-stu-id="ce932-124">Either/or</span></span>|<span data-ttu-id="ce932-125">12 15 16&#124;12 16 16</span><span class="sxs-lookup"><span data-stu-id="ce932-125">12 15 16&#124;12 16 16</span></span>|<span data-ttu-id="ce932-126">Posten die zijn geboekt op 15 december of 16 december 2016.</span><span class="sxs-lookup"><span data-stu-id="ce932-126">Those posted on either December 15 or December 16 2016.</span></span> <span data-ttu-id="ce932-127">Als deze posten zijn geboekt op beide dagen, worden ze allebei weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ce932-127">If there are entries posted on both days, they will all be displayed.</span></span>|

<span data-ttu-id="ce932-128">U kunt de verschillende notatiesoorten ook combineren.</span><span class="sxs-lookup"><span data-stu-id="ce932-128">You can also combine the various format types.</span></span>

| <span data-ttu-id="ce932-129">Opmerking</span><span class="sxs-lookup"><span data-stu-id="ce932-129">Example</span></span> | <span data-ttu-id="ce932-130">Opgenomen posten</span><span class="sxs-lookup"><span data-stu-id="ce932-130">Entries included</span></span> |
|---|---|
|<span data-ttu-id="ce932-131">12 15 16&#124;12 01 16..05 31 17</span><span class="sxs-lookup"><span data-stu-id="ce932-131">12 15 16&#124;12 01 16..05 31 17</span></span> | <span data-ttu-id="ce932-132">Posten die zijn geboekt op 15 december 2016 of op datums tussen en tot en met 1 december 2016 en 31 mei 2017.</span><span class="sxs-lookup"><span data-stu-id="ce932-132">Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017.</span></span> |
|<span data-ttu-id="ce932-133">..12 14 16&#124;12 30 16..</span><span class="sxs-lookup"><span data-stu-id="ce932-133">..12 14 16&#124;12 30 16..</span></span> | <span data-ttu-id="ce932-134">Posten die zijn geboekt op 14 december of eerder, of posten die zijn geboekt op 30 december of later. Dit wil zeggen, alle posten behalve die zijn geboekt tussen 15 december en 29 december tot en met.</span><span class="sxs-lookup"><span data-stu-id="ce932-134">Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29.</span></span> |

<span data-ttu-id="ce932-135">U ziet dat we hier de Amerikaanse datumnotatie MMDDYY hebben gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ce932-135">Note that we have used the US date format MMDDYY here.</span></span> <span data-ttu-id="ce932-136">Zodra [!INCLUDE[d365fin](includes/d365fin_md.md)] beschikbaar wordt in andere markten, zult u de indelingen kunnen gebruiken die u gewend bent.</span><span class="sxs-lookup"><span data-stu-id="ce932-136">As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.</span></span>

## <a name="using-date-formulas"></a><span data-ttu-id="ce932-137">Datumformules gebruiken</span><span class="sxs-lookup"><span data-stu-id="ce932-137">Using Date Formulas</span></span>
<span data-ttu-id="ce932-138">Een datumformule is een korte, afgekorte combinatie van letters en cijfers op basis waarvan datums worden berekend.</span><span class="sxs-lookup"><span data-stu-id="ce932-138">A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates.</span></span> <span data-ttu-id="ce932-139">U kunt datumformules invoeren in verschillende datumberekeningsvelden en in de frequentievelden van periodieke dagboeken.</span><span class="sxs-lookup"><span data-stu-id="ce932-139">You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.</span></span>

> [!NOTE]
>  <span data-ttu-id="ce932-140">In alle datumformulevelden wordt automatisch één dag opgenomen om ervoor te zorgen dat de huidige dag wordt gebruikt als begindatum van de periode.</span><span class="sxs-lookup"><span data-stu-id="ce932-140">In all data formula fields, one day is automatically included to cover today as the day when the period starts.</span></span> <span data-ttu-id="ce932-141">Als u dus bijvoorbeeld **1W** invoert, zal de periode in feite acht dagen bestrijken omdat vandaag ook is opgenomen.</span><span class="sxs-lookup"><span data-stu-id="ce932-141">Accordingly, for example, if you enter **1W**, then the period is actually eight days because today is included.</span></span> <span data-ttu-id="ce932-142">Als u een periode van zeven dagen (exact één week) wilt opgeven, inclusief de begindatum van de periode, moet u **6D** of **1W\-1D**. opgeven.</span><span class="sxs-lookup"><span data-stu-id="ce932-142">To specify a period of seven days (one true week) including the period starting date, then you must enter **6D** or **1W\-1D**.</span></span>

<span data-ttu-id="ce932-143">Hier volgen enkele voorbeelden van het gebruik van datumformules:</span><span class="sxs-lookup"><span data-stu-id="ce932-143">Here are some examples of how date formulas can be used:</span></span>

-   <span data-ttu-id="ce932-144">De datumformule in de frequentievelden van periodieke dagboeken geeft aan hoe vaak de dagboekregel moet worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="ce932-144">The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.</span></span>

-   <span data-ttu-id="ce932-145">De datumformule in het veld **Respijtperiode** van een bepaald aanmaningsniveau bepaalt hoelang de vervaldatum (of de vervaldatum van de vorige aanmaning) moet zijn verstreken voordat een aanmaning wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ce932-145">The date formula in the **Grace Period** field for a specified reminder level determines the period of time that must pass from the due date (or from the due date of the previous reminder) before a reminder will be created.</span></span>

-   <span data-ttu-id="ce932-146">De datumformule in het veld **Vervaldatumformule** bepaalt hoe de vervaldatum voor de aanmaning wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="ce932-146">The date formula in the **Due Date Calculation** field determines how to calculate the due date on the reminder.</span></span>

<span data-ttu-id="ce932-147">In de berekeningsformule voor de datum kunt u maximaal 20 tekens gebruiken (cijfers en/of letters).</span><span class="sxs-lookup"><span data-stu-id="ce932-147">The date calculation formula can contain a maximum of 20 characters, both numbers and letters.</span></span> <span data-ttu-id="ce932-148">U kunt de volgende letters gebruiken als afkorting voor tijdsaanduidingen.</span><span class="sxs-lookup"><span data-stu-id="ce932-148">You can use the following letters, which are abbreviations for time specifications.</span></span>

|  <span data-ttu-id="ce932-149">Letter</span><span class="sxs-lookup"><span data-stu-id="ce932-149">Letter</span></span>  |  <span data-ttu-id="ce932-150">Tijdspecificatie</span><span class="sxs-lookup"><span data-stu-id="ce932-150">Time specification</span></span>  |
|----------|----------------------|
|<span data-ttu-id="ce932-151">U</span><span class="sxs-lookup"><span data-stu-id="ce932-151">C</span></span>|<span data-ttu-id="ce932-152">Actueel</span><span class="sxs-lookup"><span data-stu-id="ce932-152">Current</span></span>|
|<span data-ttu-id="ce932-153">D</span><span class="sxs-lookup"><span data-stu-id="ce932-153">D</span></span>|<span data-ttu-id="ce932-154">Dag\(en\)</span><span class="sxs-lookup"><span data-stu-id="ce932-154">Day\(s\)</span></span>|
|<span data-ttu-id="ce932-155">W</span><span class="sxs-lookup"><span data-stu-id="ce932-155">W</span></span>|<span data-ttu-id="ce932-156">We(e)k\(en\)</span><span class="sxs-lookup"><span data-stu-id="ce932-156">Week\(s\)</span></span>|
|<span data-ttu-id="ce932-157">M</span><span class="sxs-lookup"><span data-stu-id="ce932-157">M</span></span>|<span data-ttu-id="ce932-158">Maand\(en\)</span><span class="sxs-lookup"><span data-stu-id="ce932-158">Month\(s\)</span></span>|
|<span data-ttu-id="ce932-159">K</span><span class="sxs-lookup"><span data-stu-id="ce932-159">Q</span></span>|<span data-ttu-id="ce932-160">Kwarta(a)l\(en\)</span><span class="sxs-lookup"><span data-stu-id="ce932-160">Quarter\(s\)</span></span>|
|<span data-ttu-id="ce932-161">J</span><span class="sxs-lookup"><span data-stu-id="ce932-161">Y</span></span>|<span data-ttu-id="ce932-162">Ja(a)r\(en\)</span><span class="sxs-lookup"><span data-stu-id="ce932-162">Year\(s\)</span></span>|

<span data-ttu-id="ce932-163">Er zijn drie soorten datumformules.</span><span class="sxs-lookup"><span data-stu-id="ce932-163">You can construct a date formula in three ways.</span></span>

<span data-ttu-id="ce932-164">In het volgende voorbeeld wordt weergegeven hoe **C** kan worden gebruikt voor huidig en een tijdseenheid.</span><span class="sxs-lookup"><span data-stu-id="ce932-164">The following example shows how to use **C**, for current, and a time unit.</span></span>

|  <span data-ttu-id="ce932-165">Expressie</span><span class="sxs-lookup"><span data-stu-id="ce932-165">Expression</span></span>  |  <span data-ttu-id="ce932-166">Betekenis</span><span class="sxs-lookup"><span data-stu-id="ce932-166">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="ce932-167">LW</span><span class="sxs-lookup"><span data-stu-id="ce932-167">CW</span></span>|<span data-ttu-id="ce932-168">Lopende week</span><span class="sxs-lookup"><span data-stu-id="ce932-168">Current week</span></span>|
|<span data-ttu-id="ce932-169">LM</span><span class="sxs-lookup"><span data-stu-id="ce932-169">CM</span></span>|<span data-ttu-id="ce932-170">Lopende maand</span><span class="sxs-lookup"><span data-stu-id="ce932-170">Current month</span></span>|

<span data-ttu-id="ce932-171">In het volgende voorbeeld wordt weergegeven hoe een getal en een tijdseenheid moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ce932-171">The following example shows how to use a number and a time unit.</span></span> <span data-ttu-id="ce932-172">Nummers mogen niet groter zijn dan 9999.</span><span class="sxs-lookup"><span data-stu-id="ce932-172">A number cannot be larger than 9999.</span></span>

|  <span data-ttu-id="ce932-173">Expressie</span><span class="sxs-lookup"><span data-stu-id="ce932-173">Expression</span></span>  |  <span data-ttu-id="ce932-174">Betekenis</span><span class="sxs-lookup"><span data-stu-id="ce932-174">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="ce932-175">10D</span><span class="sxs-lookup"><span data-stu-id="ce932-175">10D</span></span>|<span data-ttu-id="ce932-176">10 dagen vanaf vandaag</span><span class="sxs-lookup"><span data-stu-id="ce932-176">10 days from today</span></span>|
|<span data-ttu-id="ce932-177">2W</span><span class="sxs-lookup"><span data-stu-id="ce932-177">2W</span></span>|<span data-ttu-id="ce932-178">2 weken vanaf vandaag</span><span class="sxs-lookup"><span data-stu-id="ce932-178">2 weeks from today</span></span>|

<span data-ttu-id="ce932-179">In het volgende voorbeeld wordt weergegeven hoe een tijdseenheid en een getal moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ce932-179">The following example shows how to use a time unit and a number.</span></span>

|  <span data-ttu-id="ce932-180">Expressie</span><span class="sxs-lookup"><span data-stu-id="ce932-180">Expression</span></span>  |  <span data-ttu-id="ce932-181">Betekenis</span><span class="sxs-lookup"><span data-stu-id="ce932-181">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="ce932-182">D10</span><span class="sxs-lookup"><span data-stu-id="ce932-182">D10</span></span>|<span data-ttu-id="ce932-183">De volgende tiende dag van een maand</span><span class="sxs-lookup"><span data-stu-id="ce932-183">The next 10th day of a month</span></span>|
|<span data-ttu-id="ce932-184">WD4</span><span class="sxs-lookup"><span data-stu-id="ce932-184">WD4</span></span>|<span data-ttu-id="ce932-185">De volgende vierde dag van een week \(donderdag\)</span><span class="sxs-lookup"><span data-stu-id="ce932-185">The next 4th day of a week \(Thursday\)</span></span>|

<span data-ttu-id="ce932-186">Het volgende voorbeeld geeft weer hoe u deze drie soorten naar wens kunt combineren.</span><span class="sxs-lookup"><span data-stu-id="ce932-186">The following example shows how you can combine these three forms as needed.</span></span>

|  <span data-ttu-id="ce932-187">Expressie</span><span class="sxs-lookup"><span data-stu-id="ce932-187">Expression</span></span>  |  <span data-ttu-id="ce932-188">Betekenis</span><span class="sxs-lookup"><span data-stu-id="ce932-188">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="ce932-189">CM\+10D</span><span class="sxs-lookup"><span data-stu-id="ce932-189">CM\+10D</span></span>|<span data-ttu-id="ce932-190">Lopende maand \+ 10 dagen</span><span class="sxs-lookup"><span data-stu-id="ce932-190">Current month \+ 10 days</span></span>|

<span data-ttu-id="ce932-191">In het volgende voorbeeld ziet u hoe u een minteken gebruikt om een datum in het verleden aan te duiden.</span><span class="sxs-lookup"><span data-stu-id="ce932-191">The following example shows how you can use a minus sign to indicate a date in the past.</span></span>

|  <span data-ttu-id="ce932-192">Expressie</span><span class="sxs-lookup"><span data-stu-id="ce932-192">Expression</span></span>  |  <span data-ttu-id="ce932-193">Betekenis</span><span class="sxs-lookup"><span data-stu-id="ce932-193">Meaning</span></span>  |
|--------------|-----------|
|<span data-ttu-id="ce932-194">-1J</span><span class="sxs-lookup"><span data-stu-id="ce932-194">-1Y</span></span>|<span data-ttu-id="ce932-195">1 jaar geleden vanaf vandaag</span><span class="sxs-lookup"><span data-stu-id="ce932-195">1 year ago from today</span></span>|

> [!IMPORTANT]
>  <span data-ttu-id="ce932-196">Als de vestiging een basisagenda gebruikt, wordt de datumformule die u invoert in dit veld, bijvoorbeeld het veld **Verzendtijd** beschouwd als agendawerkdag.</span><span class="sxs-lookup"><span data-stu-id="ce932-196">If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days.</span></span> <span data-ttu-id="ce932-197">Bijvoorbeeld: **1W** betekent zeven werkdagen.</span><span class="sxs-lookup"><span data-stu-id="ce932-197">For example, **1W**  means seven working days.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce932-198">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ce932-198">See Also</span></span>
<span data-ttu-id="ce932-199">[Werken met [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ce932-199">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="ce932-200">Datumberekening voor inkoop</span><span class="sxs-lookup"><span data-stu-id="ce932-200">Date Calculation for Purchases</span></span>](purchasing-date-calculation-for-purchases.md)  
[<span data-ttu-id="ce932-201">Criteria in filters invoeren</span><span class="sxs-lookup"><span data-stu-id="ce932-201">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  

