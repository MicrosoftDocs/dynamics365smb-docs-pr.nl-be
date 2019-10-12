---
title: Productieagenda's instellen | Microsoft Docs
description: 'Op een afdelingsagenda staan de werkdagen en -tijden, de diensten, vakanties en afwezigheid genoteerd die bepalend zijn voor de brutocapaciteit. gemeten in tijd, van de afdeling op basis van de gedefinieerde efficiëntie en capaciteitswaarden. Voordat er een afdelingsagenda kan worden gemaakt, moet diverse voorbereidingen worden getroffen:'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 1663f9092c21e1955f3e2531efc9935ba1c68982
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2314084"
---
# <a name="set-up-shop-calendars"></a><span data-ttu-id="570d5-104">Productieagenda's instellen</span><span class="sxs-lookup"><span data-stu-id="570d5-104">Set Up Shop Calendars</span></span>
<span data-ttu-id="570d5-105">Een afdelings- of bewerkingsplaatsagenda bevat de werkdagen en -tijden, de diensten, vakanties en afwezigheid die bepalend zijn voor de brutocapaciteit, gemeten in tijd, van de afdeling op basis van de gedefinieerde efficiëntie- en capaciteitswaarden.</span><span class="sxs-lookup"><span data-stu-id="570d5-105">A work center or machine calendar specifies the working days and hours, shifts, holidays, and absences that determine the center’s gross available capacity, measured in time, according to its defined efficiency and capacity values.</span></span>

<span data-ttu-id="570d5-106">Voordat een bepaalde afdelings- of bewerkingsplaatsagenda kan worden berekend, moeten er eerst een of meer algemene productieagenda's worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="570d5-106">As a foundation for calculating a specific work or machine center calendar, you must first set up one or more general shop calendars.</span></span> <span data-ttu-id="570d5-107">In een productieagenda wordt een standaardwerkweek gedefinieerd in termen van begin- en eindtijden van een werkdag en de ploegen die er werkzaam zijn.</span><span class="sxs-lookup"><span data-stu-id="570d5-107">A shop calendar defines a standard work week according to start and end times of each working day and the work shift relation.</span></span> <span data-ttu-id="570d5-108">Bovendien zijn in een productieagenda de vastgestelde vakantiedagen gedurende het jaar opgenomen.</span><span class="sxs-lookup"><span data-stu-id="570d5-108">In addition, the shop calendar defines the fixed holidays during a year.</span></span>  

<span data-ttu-id="570d5-109">Hier wordt beschreven hoe u afdelingsagenda's instelt.</span><span class="sxs-lookup"><span data-stu-id="570d5-109">The following describes how to set up work center calendars.</span></span> <span data-ttu-id="570d5-110">Voor het instellen van bewerkingsplaatsagenda's zijn de stappen vergelijkbaar.</span><span class="sxs-lookup"><span data-stu-id="570d5-110">The steps are similar when setting up machine center calendars.</span></span>  

## <a name="to-create-work-shifts"></a><span data-ttu-id="570d5-111">Ploegen maken</span><span class="sxs-lookup"><span data-stu-id="570d5-111">To create work shifts</span></span>  
1.  <span data-ttu-id="570d5-112">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Ploegen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="570d5-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Shifts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="570d5-113">Geef op een lege regel in het veld **Code** een nummer op om de ploeg aan te duiden, bijvoorbeeld **1**.</span><span class="sxs-lookup"><span data-stu-id="570d5-113">On a blank line, enter a number in the **Code** field to identify the work shift, for example, **1**.</span></span>  
3.  <span data-ttu-id="570d5-114">Geef een omschrijving voor de ploeg in het veld **Omschrijving**, bijvoorbeeld **Vroege ploeg**.</span><span class="sxs-lookup"><span data-stu-id="570d5-114">Describe the work shift in the **Description** field, for example, **1st shift**.</span></span>  
4.  <span data-ttu-id="570d5-115">Vul eventueel regels voor een tweede of derde ploeg in.</span><span class="sxs-lookup"><span data-stu-id="570d5-115">Optionally, fill in lines for a second or third work shift.</span></span>  

<span data-ttu-id="570d5-116">Ook als de afdeling niet met ploegen werkt, moet er toch minstens één ploegcode worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="570d5-116">Even if your work centers do not work in different work shifts, enter at least one work shift code.</span></span>  

## <a name="to-set-up-a-shop-calendar"></a><span data-ttu-id="570d5-117">Een productieagenda instellen</span><span class="sxs-lookup"><span data-stu-id="570d5-117">To set up a shop calendar</span></span>  
1.  <span data-ttu-id="570d5-118">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Productieagenda's** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="570d5-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shop Calendars**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="570d5-119">Geef op een lege regel in het veld **Code** een nummer op ter aanduiding van de productieagenda.</span><span class="sxs-lookup"><span data-stu-id="570d5-119">On a blank line, enter a number in the **Code** field to identify the shop calendar.</span></span>  
3.  <span data-ttu-id="570d5-120">Beschrijf de productieagenda in het veld **Omschrijving**.</span><span class="sxs-lookup"><span data-stu-id="570d5-120">Describe the shop calendar in the **Description** field.</span></span>  
4.  <span data-ttu-id="570d5-121">Kies de actie **Werkdagen**.</span><span class="sxs-lookup"><span data-stu-id="570d5-121">Choose the **Working Days** action.</span></span>
5.  <span data-ttu-id="570d5-122">Geef op de pagina **Productieagendawerkdagen** een volledige werkweek, met de begin- en eindtijden voor elke dag, op.</span><span class="sxs-lookup"><span data-stu-id="570d5-122">On the **Shop Calendar Working Days** page, define a complete work week, with the start and end times for each day.</span></span>  

    <span data-ttu-id="570d5-123">Selecteer in het veld **Ploeg** een van de ploegen die u eerder hebt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="570d5-123">In the **Work Shift Code** field, select one of the shifts that you previously defined.</span></span> <span data-ttu-id="570d5-124">Voeg een regel toe voor elke werkdag en elke ploeg.</span><span class="sxs-lookup"><span data-stu-id="570d5-124">Add a line for every working day and every shift.</span></span> <span data-ttu-id="570d5-125">Voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="570d5-125">For example:</span></span>  

    <span data-ttu-id="570d5-126">maandag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="570d5-126">Monday  07:00 15:00 1</span></span>   
    <span data-ttu-id="570d5-127">dinsdag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="570d5-127">Tuesday 07:00 15:00 1</span></span>  

    <span data-ttu-id="570d5-128">Als u een productieagenda met twee ploegen nodig hebt, gaat u op de volgende manier te werk:</span><span class="sxs-lookup"><span data-stu-id="570d5-128">If you need a shop calendar with two work shifts, you must fill it in in this manner:</span></span>  

    <span data-ttu-id="570d5-129">maandag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="570d5-129">Monday 07:00 15:00 1</span></span>   
    <span data-ttu-id="570d5-130">maandag 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="570d5-130">Monday 15:00 23:00 2</span></span>  
    <span data-ttu-id="570d5-131">dinsdag 07:00 15:00 1</span><span class="sxs-lookup"><span data-stu-id="570d5-131">Tuesday 07:00 15:00 1</span></span>  
    <span data-ttu-id="570d5-132">dinsdag 15:00 23:00 2</span><span class="sxs-lookup"><span data-stu-id="570d5-132">Tuesday 15:00 23:00 2</span></span>  

    <span data-ttu-id="570d5-133">Weekdagen die u niet in de productieagenda definieert, zoals zaterdag en zondag, worden beschouwd als niet-werkdagen en hebben in een afdelingsagenda een beschikbare capaciteit van nul.</span><span class="sxs-lookup"><span data-stu-id="570d5-133">Any week days that you do not define in the shop calendar, such as Saturday and Sunday, are considered non-working days and will have zero available capacity in a work center calendar.</span></span>  

    <span data-ttu-id="570d5-134">Wanneer alle werkdagen van een week zijn gedefinieerd, kunt u de pagina **Productieagendawerkdagen** sluiten en doorgaan met het invoeren van vakanties en vrije dagen.</span><span class="sxs-lookup"><span data-stu-id="570d5-134">When all the working days of a week are defined, you can close the **Shop Calendar Working Days** page and proceed to enter holidays.</span></span>  

6.  <span data-ttu-id="570d5-135">Selecteer op de pagina **Productieagenda's** de productieagenda en kies de actie **Vakantiedagen**.</span><span class="sxs-lookup"><span data-stu-id="570d5-135">On the **Shop Calendars** page, select the shop calendar, and then choose the **Holidays** action.</span></span>
7. <span data-ttu-id="570d5-136">Definieer op de pagina **Productieagendavakantiedagen** de vakantiedagen van het jaar door voor elke vakantiedag op afzonderlijke regels de begindatum en -tijd, de eindtijd en een omschrijving op te geven.</span><span class="sxs-lookup"><span data-stu-id="570d5-136">On the **Shop Calendar Holidays** page, define the holidays of the year by entering the start date and time, the end time, and description of each holiday on individual lines.</span></span> <span data-ttu-id="570d5-137">Voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="570d5-137">For example:</span></span>  

    <span data-ttu-id="570d5-138">04 juli 2014 0:00:00 23:59:00 Zomervakantie</span><span class="sxs-lookup"><span data-stu-id="570d5-138">04/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="570d5-139">05 juli 2014 0:00:00 23:59:00 Zomervakantie</span><span class="sxs-lookup"><span data-stu-id="570d5-139">05/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  
    <span data-ttu-id="570d5-140">06 juli 2014 0:00:00 23:59:00 Zomervakantie</span><span class="sxs-lookup"><span data-stu-id="570d5-140">06/07/14 0:00:00 23:59:00 Summer Holiday</span></span>  

<span data-ttu-id="570d5-141">De gedefinieerde vakantiedagen hebben in een afdelingsagenda een beschikbare capaciteit van nul.</span><span class="sxs-lookup"><span data-stu-id="570d5-141">The defined holidays will have zero available capacity in a work center calendar.</span></span>  

<span data-ttu-id="570d5-142">Nu kan de productieagenda worden toegewezen aan een afdeling om de afdelingsagenda te berekenen waarop de volledige tijdsplanning van alle bewerkingen op die afdeling wordt gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="570d5-142">The shop calendar can now be assigned to a work center to calculate the work shop calendar that will govern all operation scheduling at that work center.</span></span>  

## <a name="to-calculate-a-work-center-calendar"></a><span data-ttu-id="570d5-143">Een afdelingsagenda berekenen</span><span class="sxs-lookup"><span data-stu-id="570d5-143">To calculate a work center calendar</span></span>  

1.  <span data-ttu-id="570d5-144">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Afdelingen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="570d5-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Work Centers**, and then choose the related link.</span></span>
2. <span data-ttu-id="570d5-145">Open de afdeling die u wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="570d5-145">Open the work center that you want to update.</span></span>  
3. <span data-ttu-id="570d5-146">Geef in het veld **Productieagendacode** op welke productieagenda moet worden gebruikt als basis voor de agenda van de afdeling.</span><span class="sxs-lookup"><span data-stu-id="570d5-146">In the **Shop Calendar Code** field, select which shop calendar to use as the foundation for a work center calendar.</span></span>  
4. <span data-ttu-id="570d5-147">Kies de actie **Agenda**.</span><span class="sxs-lookup"><span data-stu-id="570d5-147">Choose the **Calendar** action.</span></span>  
5. <span data-ttu-id="570d5-148">Kies op de pagina **Afdelingsagenda** de actie **Matrix weergeven**.</span><span class="sxs-lookup"><span data-stu-id="570d5-148">On the **Work Center Calendar** page, choose the **Show Matrix** action.</span></span>  

    <span data-ttu-id="570d5-149">In het linkerdeel van de matrixpagina worden alle afdelingen weergegeven die zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="570d5-149">The left side of the matrix page lists the work centers that are set up.</span></span> <span data-ttu-id="570d5-150">In het rechterdeel ziet u een agenda met daarop de beschikbare capaciteitswaarden voor elke werkdag in de gedefinieerde eenheid, bijvoorbeeld **480** minuten.</span><span class="sxs-lookup"><span data-stu-id="570d5-150">The right side shows a calendar displaying the available capacity values for each working day in the defined unit of measure, for example, **480** minutes.</span></span> <span data-ttu-id="570d5-151">Elke regel geeft de agenda van één afdeling weer.</span><span class="sxs-lookup"><span data-stu-id="570d5-151">Each line represents the calendar of one work center.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="570d5-152">U kunt de capaciteitswaarden voor elke week of maand ook bekijken door te schakelen tussen opties in het veld **Weergeven per** op de pagina **Afdelingsagenda**.</span><span class="sxs-lookup"><span data-stu-id="570d5-152">You can also select to view the capacity values for each week or month by changing the selection in the **View By** field on the **Work Center Calendar** page.</span></span>  

    <span data-ttu-id="570d5-153">Als u de nieuwe productieagenda wilt weergeven als een lijn op de geselecteerde afdeling, moet deze productieagenda eerst worden berekend.</span><span class="sxs-lookup"><span data-stu-id="570d5-153">To reflect the new shop calendar as a line on the selected work center, it must first be calculated.</span></span>  

6.  <span data-ttu-id="570d5-154">Kies de actie **Berekenen**.</span><span class="sxs-lookup"><span data-stu-id="570d5-154">Choose the **Calculate** action.</span></span>  
7.  <span data-ttu-id="570d5-155">Op het sneltabblad **Afdeling** kunt u een filter instellen, zodat er maar voor één afdeling een berekening wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="570d5-155">On the **Work Center** FastTab, you can set a filter to only calculate for one work center.</span></span> <span data-ttu-id="570d5-156">Stelt u geen filter in, dan worden alle bestaande afdelingsagenda's berekend.</span><span class="sxs-lookup"><span data-stu-id="570d5-156">If you do not set a filter, all existing work center calendars will be calculated.</span></span>  
8.  <span data-ttu-id="570d5-157">Definieer de begin- en einddatum van de agendaperiode die moet worden berekend, bijvoorbeeld één jaar, van 1 jan. 2004 tot 31 dec. 2004.</span><span class="sxs-lookup"><span data-stu-id="570d5-157">Define the starting and ending dates of the calendar period that should be calculated, for example, one year from 01/01/14 to 31/12/14.</span></span>
9. <span data-ttu-id="570d5-158">Kies de knop **OK** om de capaciteit te berekenen.</span><span class="sxs-lookup"><span data-stu-id="570d5-158">Choose the **OK** button to calculate capacity.</span></span>  

<span data-ttu-id="570d5-159">Er zijn nu agendaposten gemaakt (of bijgewerkt) waarin de beschikbare capaciteit per dag (of per andere periode) wordt weergegeven op basis van de volgende drie sets stamgegevens:</span><span class="sxs-lookup"><span data-stu-id="570d5-159">Calendar entries are now created or updated displaying the available capacity for each period according to the following three sets of master data:</span></span>  

- <span data-ttu-id="570d5-160">de in de productieagenda gedefinieerde werkdagen en ploeg</span><span class="sxs-lookup"><span data-stu-id="570d5-160">The working days and shift defined in the assigned shop calendar.</span></span>  
- <span data-ttu-id="570d5-161">de waarde in het veld **Capaciteit** op de afdelingskaart</span><span class="sxs-lookup"><span data-stu-id="570d5-161">The value in the **Capacity** field on the work center card.</span></span>  
- <span data-ttu-id="570d5-162">de waarde in het veld **Efficiëntie** op de afdelingskaart.</span><span class="sxs-lookup"><span data-stu-id="570d5-162">The value in the **Efficiency** field on the work center card.</span></span>  

<span data-ttu-id="570d5-163">De berekende afdelingsagenda bepaalt nu wanneer en hoe veel capaciteit beschikbaar is op deze afdeling.</span><span class="sxs-lookup"><span data-stu-id="570d5-163">The calculated work center calendar will now define when and how much capacity is available at this work center.</span></span> <span data-ttu-id="570d5-164">Hiermee bepaalt u de gedetailleerde planning van bewerkingen die worden uitgevoerd op de afdeling.</span><span class="sxs-lookup"><span data-stu-id="570d5-164">This controls the detailed scheduling of operations performed at the work center.</span></span>  

## <a name="to-record-work-center-absence"></a><span data-ttu-id="570d5-165">Afwezigheid op de afdeling registreren</span><span class="sxs-lookup"><span data-stu-id="570d5-165">To record work center absence</span></span>  
1.  <span data-ttu-id="570d5-166">Kies op de pagina **Afdelingsagenda** de actie **Matrix weergeven**.</span><span class="sxs-lookup"><span data-stu-id="570d5-166">On the **Work Center Calendar** page, choose the **Show Matrix** action.</span></span>
2. <span data-ttu-id="570d5-167">Selecteer op de pagina **Afdelingsagendamatrix** de afdeling en de agendadag waarop de afwezigheid moet worden geregistreerd en kies vervolgens de actie **Afwezigheid**.</span><span class="sxs-lookup"><span data-stu-id="570d5-167">On the **Work Center Calendar Matrix** page, select the work center and calendar day when the absence time should be recorded, and then choose the **Absence** action.</span></span>  
3.  <span data-ttu-id="570d5-168">Definieer op de pagina **Afwezigheid** de begintijd, de eindtijd en de omschrijving van de afwezigheid van die dag, bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="570d5-168">On the **Absence** page, define the starting time, ending time, and description of that day’s absence.</span></span> <span data-ttu-id="570d5-169">Voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="570d5-169">For example:</span></span>  

    <span data-ttu-id="570d5-170">25 jan. 2001 08:00 10:00 Onderhoud</span><span class="sxs-lookup"><span data-stu-id="570d5-170">25/01/01 08:00 10:00 Maintenance</span></span>  

4.  <span data-ttu-id="570d5-171">Kies de actie **Bijwerken** en sluit vervolgens de pagina **Afwezigheid**.</span><span class="sxs-lookup"><span data-stu-id="570d5-171">Choose the **Update** action, and then close the **Absence** page.</span></span>  

<span data-ttu-id="570d5-172">De geregistreerde afwezigheid is nu in mindering gebracht op de capaciteit van de geselecteerde dag.</span><span class="sxs-lookup"><span data-stu-id="570d5-172">The capacity of the selected day has now decreased by the recorded absence time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="570d5-173">Zie ook</span><span class="sxs-lookup"><span data-stu-id="570d5-173">See Also</span></span>  
[<span data-ttu-id="570d5-174">Basisagenda's instellen</span><span class="sxs-lookup"><span data-stu-id="570d5-174">Set Up Base Calendars</span></span>](across-how-to-assign-base-calendars.md)  
[<span data-ttu-id="570d5-175">Afdelingen en bewerkingsplaatsen instellen</span><span class="sxs-lookup"><span data-stu-id="570d5-175">Set Up Work Centers and Machine Centers</span></span>](production-how-to-set-up-work-and-machine-centers.md)  
[<span data-ttu-id="570d5-176">Productie instellen</span><span class="sxs-lookup"><span data-stu-id="570d5-176">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
[<span data-ttu-id="570d5-177">Productie</span><span class="sxs-lookup"><span data-stu-id="570d5-177">Manufacturing</span></span>](production-manage-manufacturing.md)  
<span data-ttu-id="570d5-178">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="570d5-178">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
