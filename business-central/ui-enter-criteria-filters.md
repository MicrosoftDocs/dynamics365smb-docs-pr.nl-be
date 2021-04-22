---
title: Lijsten sorteren, doorzoeken en filteren | Microsoft Docs
description: Werk efficiënt in lijsten door te zoeken in uw gegevens, kolommen te sorteren en resultaten te verfijnen met filtersymbolen en toetsenbordsneltoetsen.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a3d42fccebafdfa80346f04b43a0e3dd29f467d8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5770650"
---
# <a name="sorting-searching-and-filtering"></a><span data-ttu-id="85ea8-103">Sorteren, zoeken en filteren</span><span class="sxs-lookup"><span data-stu-id="85ea8-103">Sorting, Searching, and Filtering</span></span>

<span data-ttu-id="85ea8-104">U kunt een paar dingen doen om records in een lijst, in een rapport of XMLport te scannen, te vinden en te beperken.</span><span class="sxs-lookup"><span data-stu-id="85ea8-104">There are a few things that you can do that will help you scan, find, and limit records on a list or in a report or XMLport.</span></span> <span data-ttu-id="85ea8-105">U kunt de records bijvoorbeeld sorteren, doorzoeken en filteren.</span><span class="sxs-lookup"><span data-stu-id="85ea8-105">These include sorting, searching, and filtering.</span></span> <span data-ttu-id="85ea8-106">U kunt sommige of al deze methoden tegelijkertijd toepassen om snel uw gegevens te zoeken of te analyseren.</span><span class="sxs-lookup"><span data-stu-id="85ea8-106">You can apply some or all of these simultaneously to quickly find or analyze your data.</span></span>

<span data-ttu-id="85ea8-107">Voor rapporten en XMLports, kunt u filters instellen zoals in lijsten om af te bakenen welke gegevens in het rapport of de XMLport moeten worden opgenomen, maar u kunt niet sorteren en zoeken.</span><span class="sxs-lookup"><span data-stu-id="85ea8-107">For reports and XMLports, as on lists, you can set filters to delimit which data to include in the report or XMLport, but you can't sort and search.</span></span>

> [!TIP]
> <span data-ttu-id="85ea8-108">Wanneer u uw gegevens weergeeft als tegels, kunt u zoeken en filtering gebruiken.</span><span class="sxs-lookup"><span data-stu-id="85ea8-108">When viewing your data as tiles, you can search and use filtering.</span></span> <span data-ttu-id="85ea8-109">Als u de volledige set functies wilt gebruiken voor sorteren, zoeken en filteren, kiest u het pictogram ![Als overzicht weergeven](media/ui_show_as_list_icon.png "Weergeven als lijst pijl naar links") om de records als lijst weer te geven.</span><span class="sxs-lookup"><span data-stu-id="85ea8-109">To use the full set of powerful features for sorting, searching, and filtering, choose the ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to view the records as a list.</span></span>

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a><span data-ttu-id="85ea8-110">Sorteervolgorde</span><span class="sxs-lookup"><span data-stu-id="85ea8-110">Sorting</span></span>

<span data-ttu-id="85ea8-111">Met de sorteerfunctie krijgt u snel een overzicht van de gegevens.</span><span class="sxs-lookup"><span data-stu-id="85ea8-111">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="85ea8-112">Als u bijvoorbeeld veel klanten heeft, kunt u ze sorteren op **Klantnr.**, **Valutacode** of **Land-/regiocode** om het overzicht te krijgen dat u nodig heeft.</span><span class="sxs-lookup"><span data-stu-id="85ea8-112">For example, if you have many customers,  you could sort them by **Customer No.**, **Currency Code**, or **Country Region Code** to get the overview you need.</span></span>

<span data-ttu-id="85ea8-113">Om een lijst te sorteren, kunt u:</span><span class="sxs-lookup"><span data-stu-id="85ea8-113">To sort a list, you can either:</span></span>

- <span data-ttu-id="85ea8-114">Een kolomkoptekst kiezen om te wisselen tussen oplopende en aflopende volgorde of</span><span class="sxs-lookup"><span data-stu-id="85ea8-114">Choose a column heading text to toggle between ascending and descending order, or</span></span>
- <span data-ttu-id="85ea8-115">De vervolgkeuzepijl in de kolomkop kiezen en vervolgens de actie **Oplopend** of **Aflopend** kiezen.</span><span class="sxs-lookup"><span data-stu-id="85ea8-115">Choose the drop-down arrow in the column heading, then choose the **Ascending** or **Descending** action.</span></span>  

> [!NOTE]  
> <span data-ttu-id="85ea8-116">Sorteren wordt niet ondersteund bij afbeeldingen, BLOB-velden, FlowFilters en velden die niet deel van een tabel zijn.</span><span class="sxs-lookup"><span data-stu-id="85ea8-116">Sorting isn't supported on images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching"></a><span data-ttu-id="85ea8-117">Zoeken</span><span class="sxs-lookup"><span data-stu-id="85ea8-117">Searching</span></span>

<!--## Searching by using the Quick Filter -->
<span data-ttu-id="85ea8-118">Boven aan elke lijstpagina staat een actie ![Zoeken in lijst](media/ui-search/search-list.png "Pictogram Zoeken in lijst") **Zoeken** die een snelle en gemakkelijke manier biedt om de records in een lijst te reduceren en alleen de records weer te geven die de gegevens bevatten die u wilt zien.</span><span class="sxs-lookup"><span data-stu-id="85ea8-118">At the top of each list page, there's a ![Search list](media/ui-search/search-list.png "Search list icon") **Search** action that provides a quick and easy way to reduce the records in a list and display only those records that contain the data that you're interested in seeing.</span></span>

<span data-ttu-id="85ea8-119">Als u wilt zoeken, kiest u gewoon de actie **Zoeken** en typt u de tekst die u zoekt, in het vak.</span><span class="sxs-lookup"><span data-stu-id="85ea8-119">To search, just choose the **Search** action, and then in the box, type the text that you're looking for.</span></span> <span data-ttu-id="85ea8-120">U kunt letters, cijfers en andere symbolen invoeren.</span><span class="sxs-lookup"><span data-stu-id="85ea8-120">You can enter letters, numbers, and other symbols.</span></span>

<span data-ttu-id="85ea8-121">Over het algemeen wordt geprobeerd in alle velden tekst overeen te laten komen.</span><span class="sxs-lookup"><span data-stu-id="85ea8-121">In general, search will attempt to match text across all fields.</span></span> <span data-ttu-id="85ea8-122">Er wordt geen onderscheid gemaakt tussen hoofdletters en kleine letters (hoofdletterongevoelig) en wordt gezocht naar overeenkomst met tekst die ergens in het veld, aan het begin, aan het einde of in het midden wordt geplaatst.</span><span class="sxs-lookup"><span data-stu-id="85ea8-122">It doesn't distinguish between uppercase and lowercase characters (case insensitive) and will match text placed anywhere in the field, at the beginning, end, or in the middle.</span></span>

> [!TIP]
> <span data-ttu-id="85ea8-123">U kunt op **F3** drukken om het zoekvak te activeren en te deactiveren.</span><span class="sxs-lookup"><span data-stu-id="85ea8-123">You can press **F3** to activate and deactivate the search box.</span></span> <span data-ttu-id="85ea8-124">Zie voor meer informatie [Toetsenbordsneltoetsen](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="85ea8-124">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

> [!NOTE]  
> <span data-ttu-id="85ea8-125">Zoeken kijkt niet naar waarden in afbeeldingen, BLOB-velden, FlowFilters, FlowFields en andere velden die geen deel uitmaken van een tabel.</span><span class="sxs-lookup"><span data-stu-id="85ea8-125">Search won't match values in images, BLOB fields, FlowFilters, FlowFields, and other fields that aren't part of a table.</span></span>


### <a name="fine-tuning-the-search-with-filter-criteria"></a><span data-ttu-id="85ea8-126">De criteria voor Zoeken met filter verfijnen</span><span class="sxs-lookup"><span data-stu-id="85ea8-126">Fine-tuning the Search with Filter criteria</span></span>

<span data-ttu-id="85ea8-127">U kunt nauwkeuriger zoeken door filteroperatoren, uitdrukkingen en filtertokens te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="85ea8-127">You can make a more exact search by using filter operators, expressions, and filter tokens.</span></span> <span data-ttu-id="85ea8-128">In tegenstelling tot filteren, worden deze bij gebruik in het zoekvak op alle velden toegepast, waardoor ze minder efficiënt zijn dan filteren.</span><span class="sxs-lookup"><span data-stu-id="85ea8-128">Unlike filtering, these are applied across all fields when used in the search box, making them less efficient than filtering.</span></span>

- <span data-ttu-id="85ea8-129">Als u alleen veldwaarden wilt zoeken die exact overeenkomen met de volledige tekst en de hoofdletters/kleine letters, plaatst u de zoektekst tussen enkele aanhalingstekens (`''` bijvoorbeeld `'man'`).</span><span class="sxs-lookup"><span data-stu-id="85ea8-129">To find only field values that match the entire text and case exactly, place the search text between single quotes `''` (for example, `'man'`).</span></span>

- <span data-ttu-id="85ea8-130">Als u veldwaarden wilt zoeken die beginnen met een bepaalde tekst en overeenkomen met de hoofdletters/kleine letters, plaatst u `*` achter de tekst (bijvoorbeeld `man*`).</span><span class="sxs-lookup"><span data-stu-id="85ea8-130">To find field values that start with a certain text and match the case, place `*` after the search text (for example `man*`).</span></span>

- <span data-ttu-id="85ea8-131">Als u veldwaarden wilt zoeken die eindigen met een bepaalde tekst en overeenkomen met de hoofdletters/kleine letters, plaatst u `*` vóór de tekst (bijvoorbeeld `*man`).</span><span class="sxs-lookup"><span data-stu-id="85ea8-131">To find field values that end with a certain text and match the case, place `*` before the search text (for example `*man`).</span></span>

- <span data-ttu-id="85ea8-132">Wanneer u `''` of `*` gebruikt, wordt onderscheid gemaakt tussen hoofdletters en kleine letters.</span><span class="sxs-lookup"><span data-stu-id="85ea8-132">When using  `''` or `*`, the search is case-sensitive.</span></span> <span data-ttu-id="85ea8-133">Als u hoofdletterongevoelig wilt zoeken, plaatst u `@` vóór de zoektekst (bijvoorbeeld `@man*`).</span><span class="sxs-lookup"><span data-stu-id="85ea8-133">If you want to make the search case insensitive, place `@` before the search text (for example `@man*`).</span></span>

<span data-ttu-id="85ea8-134">In de volgende tabel vindt u enkele voorbeelden om aan te geven hoe u de zoekactie kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="85ea8-134">The following table provides some examples to explain how you can use the search.</span></span>

|<span data-ttu-id="85ea8-135">Zoekcriteria</span><span class="sxs-lookup"><span data-stu-id="85ea8-135">Search Criteria</span></span>|<span data-ttu-id="85ea8-136">Zoekt…</span><span class="sxs-lookup"><span data-stu-id="85ea8-136">Finds...</span></span>|
|---------------|----------|
|`man`<br /><span data-ttu-id="85ea8-137">of</span><span class="sxs-lookup"><span data-stu-id="85ea8-137">or</span></span> <br />`Man`|<span data-ttu-id="85ea8-138">Alle records met velden die de tekst **man** bevatten, ongeacht hoofdletters.</span><span class="sxs-lookup"><span data-stu-id="85ea8-138">All records with fields that contain the text **man**, regardless of the case.</span></span> <span data-ttu-id="85ea8-139">Bijvoorbeeld **Manchester**, **manual** of **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="85ea8-139">For example, **Manchester**, **manual**, or **Sportsman**.</span></span> |
|`'Man'`|<span data-ttu-id="85ea8-140">Alle records met velden die alleen **Man** bevatten, ongeacht hoofdletters.</span><span class="sxs-lookup"><span data-stu-id="85ea8-140">All records with fields that contain only **Man**, matching the case.</span></span>|
|`Man*`|<span data-ttu-id="85ea8-141">Alle records met velden die beginnen met de tekst <b>Man</b>, met identieke hoofdletters/kleine letters.</span><span class="sxs-lookup"><span data-stu-id="85ea8-141">All records with fields that start with the text <b>Man</b>, matching the case.</span></span> <span data-ttu-id="85ea8-142">Bijvoorbeeld **Manchester**, maar niet **manual** of **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="85ea8-142">For example, **Manchester** but not **manual** or **Sportsman**.</span></span>|
|`@Man*`|<span data-ttu-id="85ea8-143">Alle records met velden die beginnen met **man**, ongeacht hoofdletters.</span><span class="sxs-lookup"><span data-stu-id="85ea8-143">All records with fields that start with **man**, regardless of the case.</span></span> <span data-ttu-id="85ea8-144">Bijvoorbeeld **Manchester** en **manual**, maar niet **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="85ea8-144">For example, **Manchester** and **manual**, but not **Sportsman**.</span></span>|
|`@*man`|<span data-ttu-id="85ea8-145">Alle records met velden die eindigen met **man**, ongeacht hoofdletters.</span><span class="sxs-lookup"><span data-stu-id="85ea8-145">All records that end with **man**, regardless of the case.</span></span> <span data-ttu-id="85ea8-146">Bijvoorbeeld **Sportsman**, maar niet **Manchester** of **manual**.</span><span class="sxs-lookup"><span data-stu-id="85ea8-146">For example **Sportsman**, but not **Manchester** or **manual**.</span></span>|


## <a name="filtering"></a><a name="filtering"></a><span data-ttu-id="85ea8-147">Filteren</span><span class="sxs-lookup"><span data-stu-id="85ea8-147">Filtering</span></span>

<span data-ttu-id="85ea8-148">Filtering biedt een geavanceerdere en flexibelere manier om te bepalen welke records in een lijst, rapport of XMLport worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="85ea8-148">Filtering provides a more advanced and versatile way to control which records are included in a list, report, or XMLport.</span></span> <span data-ttu-id="85ea8-149">Er zijn twee belangrijke verschillen tussen zoeken en filteren, zoals wordt beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="85ea8-149">There are two major differences between searching and filtering, as described in the table below.</span></span>

|| <span data-ttu-id="85ea8-150">**Zoeken**</span><span class="sxs-lookup"><span data-stu-id="85ea8-150">**Searching**</span></span> | <span data-ttu-id="85ea8-151">**Filteren**</span><span class="sxs-lookup"><span data-stu-id="85ea8-151">**Filtering**</span></span> |
|--|----------|------------|
| <span data-ttu-id="85ea8-152">**Toepasselijke velden**</span><span class="sxs-lookup"><span data-stu-id="85ea8-152">**Applicable Fields**</span></span> | <span data-ttu-id="85ea8-153">Zoekt in alle velden die zichtbaar zijn op de pagina.</span><span class="sxs-lookup"><span data-stu-id="85ea8-153">Searches across all fields that are visible on the page.</span></span> | <span data-ttu-id="85ea8-154">Filtert een of meer velden afzonderlijk, selecterend vanuit een veld in de tabel, inclusief velden die niet zichtbaar zijn op de pagina.</span><span class="sxs-lookup"><span data-stu-id="85ea8-154">Filters one or more fields individually, selecting from any field on the table, including fields that aren't visible on the page.</span></span> |
| <span data-ttu-id="85ea8-155">**Afstemmen**</span><span class="sxs-lookup"><span data-stu-id="85ea8-155">**Matching**</span></span> | <span data-ttu-id="85ea8-156">Geeft records weer met velden die voldoen aan de zoektekst, ongeacht hoofdletters/kleine letters of plaatsing van de tekst.</span><span class="sxs-lookup"><span data-stu-id="85ea8-156">Displays records with fields that match the search text, no matter the text's case or placement in the field.</span></span> | <span data-ttu-id="85ea8-157">Geeft records weer waar het veld exact overeenkomt met het filter en is hoofdlettergevoelig, tenzij speciale filtersymbolen worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="85ea8-157">Displays records where the field exactly matches the filter, including the text's case, unless special filter symbols are entered.</span></span>

<span data-ttu-id="85ea8-158">Filteren stelt u in staat records weer te geven voor bepaalde rekeningen of klanten, datums, bedragen en andere informatie door filtercriteria op te geven.</span><span class="sxs-lookup"><span data-stu-id="85ea8-158">Filtering enables you to display records for specific accounts or customers, dates, amounts, and other information by specifying filter criteria.</span></span> <span data-ttu-id="85ea8-159">Alleen records die voldoen aan de criteria, worden weergegeven in de lijst of opgenomen in het rapport, de batchtaak of de XMLport.</span><span class="sxs-lookup"><span data-stu-id="85ea8-159">Only records that match the criteria are displayed on the list or included in the report, batch job, or XMLport.</span></span> <span data-ttu-id="85ea8-160">Als u criteria opgeeft voor meerdere velden, worden alleen de records weergegeven die overeenkomen met alle criteria.</span><span class="sxs-lookup"><span data-stu-id="85ea8-160">If you specify criteria for multiple fields, then only records that match all criteria will be displayed.</span></span>

<span data-ttu-id="85ea8-161">Voor lijsten worden de filters weergegeven in een filtervenster dat links van de lijst verschijnt wanneer u deze activeert.</span><span class="sxs-lookup"><span data-stu-id="85ea8-161">For lists, the filters are displayed on a filter pane that appears to the left of the list when you activate it.</span></span> <span data-ttu-id="85ea8-162">Voor rapporten, batchtaken en XMLports zijn de filters direct zichtbaar op de aanvraagpagina.</span><span class="sxs-lookup"><span data-stu-id="85ea8-162">For reports, batch jobs, and XMLports, the filters are visible directly on the request page.</span></span>

### <a name="filtering-with-option-fields"></a><span data-ttu-id="85ea8-163">Filteren met optievelden</span><span class="sxs-lookup"><span data-stu-id="85ea8-163">Filtering with Option Fields</span></span>

<span data-ttu-id="85ea8-164">Voor 'gewone' velden die gegevens, instellingsdatum of bedrijfsgegevens bevatten, kunt u filters instellen door gegevens te selecteren en filterwaarden te typen, en u kunt symbolen gebruiken om geavanceerde filtercriteria te definiëren.</span><span class="sxs-lookup"><span data-stu-id="85ea8-164">For "ordinary" fields that hold data, setup date, or business data, you can set filters both by selecting data and by typing filter values, and you can use symbols to define advanced filter criteria.</span></span> <span data-ttu-id="85ea8-165">Zie voor meer informatie [Filtercriteria invoeren](ui-enter-criteria-filters.md#entering-filter-criteria).</span><span class="sxs-lookup"><span data-stu-id="85ea8-165">For more information, see [Entering Filter Criteria](ui-enter-criteria-filters.md#entering-filter-criteria).</span></span>

<span data-ttu-id="85ea8-166">Voor velden van het type **Optie** kunt u echter alleen een filter instellen door een of meer opties te selecteren in een vervolgkeuzelijst met beschikbare opties.</span><span class="sxs-lookup"><span data-stu-id="85ea8-166">For fields of type **Option**, however, you can only set a filter by selecting one or more options from a drop-down list of the available options.</span></span> <span data-ttu-id="85ea8-167">Een voorbeeld van een optieveld is het veld **Status** op de pagina **Verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="85ea8-167">An example of an option field is the **Status** field on the **Sales Orders** page.</span></span>

> [!NOTE]
> <span data-ttu-id="85ea8-168">Wanneer u meerdere opties als filterwaarde selecteert, wordt de relatie tussen de opties gedefinieerd als *OF*.</span><span class="sxs-lookup"><span data-stu-id="85ea8-168">When you select multiple options as a filter value, the relationship between the options is defined as *OR*.</span></span> <span data-ttu-id="85ea8-169">Als u bijvoorbeeld zowel het selectievakje **Open** als **Vrijgegeven** selecteert in het filterveld **Status** op de pagina **Verkooporders**, betekent dit dat verkooporders die open of vrijgegeven zijn, worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="85ea8-169">For example, if you select both the **Open** and the **Released** check box in the **Status** filter field on the **Sales Orders** page, it means that sales orders that are either open or released are displayed.</span></span>

### <a name="setting-filters-on-lists"></a><span data-ttu-id="85ea8-170">Filters instellen voor lijsten</span><span class="sxs-lookup"><span data-stu-id="85ea8-170">Setting Filters on Lists</span></span>

<span data-ttu-id="85ea8-171">In lijsten stelt u filters in met behulp van het filtervenster.</span><span class="sxs-lookup"><span data-stu-id="85ea8-171">On lists, you set filters by using the filter pane.</span></span> <span data-ttu-id="85ea8-172">Als u het filtervenster voor een lijst wilt weergeven, kiest u de vervolgkeuzepijl naast de naam van de pagina en kiest u vervolgens de actie **Filtervenster weergeven**.</span><span class="sxs-lookup"><span data-stu-id="85ea8-172">To display the filter pane for a list, choose the drop-down arrow next to the name of the page, and then choose the **Show filter pane** action.</span></span> <span data-ttu-id="85ea8-173">U kunt ook drukken op **Shift+F3**.</span><span class="sxs-lookup"><span data-stu-id="85ea8-173">Alternatively, press **Shift+F3**.</span></span>

<span data-ttu-id="85ea8-174">Als u het filtervenster voor een kolom in een lijst wilt weergeven, kiest u de vervolgkeuzepijl en kiest u vervolgens de actie **Filter**.</span><span class="sxs-lookup"><span data-stu-id="85ea8-174">To display the filter pane for a column on a list, choose the drop-down arrow, and then choose the **Filter** action.</span></span> <span data-ttu-id="85ea8-175">U kunt ook drukken op **Shift+F3**.</span><span class="sxs-lookup"><span data-stu-id="85ea8-175">Alternatively, press **Shift+F3**.</span></span> <span data-ttu-id="85ea8-176">Het filtervenster wordt geopend met de geselecteerde kolom weergegeven als een filterveld in de sectie **Filter lijst op**.</span><span class="sxs-lookup"><span data-stu-id="85ea8-176">The filter pane opens with the selected column shown as a filter field in the **Filter list by** section.</span></span>

<span data-ttu-id="85ea8-177">Het filterdeelvenster bevat de huidige filters voor een lijst en biedt u de mogelijkheid uw eigen filters in te stellen op een of meer velden door de actie **+ Filter** te kiezen.</span><span class="sxs-lookup"><span data-stu-id="85ea8-177">The filter pane displays the current filters for a list, and enables you to set your own custom filters on one or more fields by choosing the **+ Filter** action.</span></span>

 <span data-ttu-id="85ea8-178">Een filterdeelvenster is verdeeld in drie gedeelten: **Weergaven**, **Filter lijst op** en **Filter totalen op**:</span><span class="sxs-lookup"><span data-stu-id="85ea8-178">A filter pane is divided in three sections: **Views**, **Filter list by**, and **Filter totals by**:</span></span>

- <span data-ttu-id="85ea8-179">**Weergaven**</span><span class="sxs-lookup"><span data-stu-id="85ea8-179">**Views**</span></span>

  <span data-ttu-id="85ea8-180">Sommige lijsten bevatten het gedeelte **Weergaven**.</span><span class="sxs-lookup"><span data-stu-id="85ea8-180">Some lists include the **Views** section.</span></span> <span data-ttu-id="85ea8-181">Weergaven zijn variaties van de lijst die vooraf zijn ingesteld met filters.</span><span class="sxs-lookup"><span data-stu-id="85ea8-181">Views are variations of the list that have been preconfigured with filters.</span></span> <span data-ttu-id="85ea8-182">U kunt per lijst zoveel weergaven definiëren en opslaan als u wilt.</span><span class="sxs-lookup"><span data-stu-id="85ea8-182">You can define and save as many views as you want per list.</span></span> <span data-ttu-id="85ea8-183">De weergaven zijn voor u beschikbaar op elk apparaat waarop u inlogt.</span><span class="sxs-lookup"><span data-stu-id="85ea8-183">The views will be available to you on any device you sign into.</span></span> <span data-ttu-id="85ea8-184">Zie voor meer informatie [Lijstweergaven opslaan en personaliseren](ui-views.md).</span><span class="sxs-lookup"><span data-stu-id="85ea8-184">For more information, see [Save and Personalize List Views](ui-views.md).</span></span>

- <span data-ttu-id="85ea8-185">**Filter lijst op**</span><span class="sxs-lookup"><span data-stu-id="85ea8-185">**Filter list by**</span></span>

  <span data-ttu-id="85ea8-186">In deze sectie voegt u filters toe aan specifieke velden om het aantal weergegeven records te reduceren.</span><span class="sxs-lookup"><span data-stu-id="85ea8-186">This section is where you add filters on specific fields to reduce the number of displayed records.</span></span> <span data-ttu-id="85ea8-187">Als u een filter wilt toevoegen, kiest u de actie **+ Filter**.</span><span class="sxs-lookup"><span data-stu-id="85ea8-187">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="85ea8-188">Typ vervolgens de naam van het veld waarop u de lijst wilt filteren of kies een veld in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="85ea8-188">Then, type the name of the field that you want to filter the list by or pick a field from the drop-down list.</span></span>

- <span data-ttu-id="85ea8-189">**Filter totalen op**</span><span class="sxs-lookup"><span data-stu-id="85ea8-189">**Filter totals by**</span></span>

  <span data-ttu-id="85ea8-190">Sommige lijsten met berekende velden, zoals bedragen en aantallen, bevatten het gedeelte **Filter totalen op**, waarin u verschillende dimensies kunt aanpassen die van invloed zijn op berekeningen.</span><span class="sxs-lookup"><span data-stu-id="85ea8-190">Some lists that display calculated fields, such as amounts and quantities, will include the **Filter totals by** section where you can adjust various dimensions that influence calculations.</span></span> <span data-ttu-id="85ea8-191">Als u een filter wilt toevoegen, kiest u de actie **+ Filter**.</span><span class="sxs-lookup"><span data-stu-id="85ea8-191">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="85ea8-192">Typ vervolgens de naam van het veld waarop u de lijst wilt filteren of kies een veld in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="85ea8-192">Then, type the name of the field that you want to filter the list by or pick a field from the drop-down list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="85ea8-193">Filters in het gedeelte **Filter totalen op** worden bepaald door FlowFilters in het paginaontwerp.</span><span class="sxs-lookup"><span data-stu-id="85ea8-193">Filters in the **Filter totals by** section are controlled by FlowFilters on the page design.</span></span> <span data-ttu-id="85ea8-194">Zie voor technische informatie [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span><span class="sxs-lookup"><span data-stu-id="85ea8-194">For technical information, see [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span></span>

<span data-ttu-id="85ea8-195">U kunt een eenvoudig filter rechtstreeks in een lijst instellen met behulp van het filtervenster, namelijk een filter dat alleen records weergeeft met dezelfde waarde als in de geselecteerde cel.</span><span class="sxs-lookup"><span data-stu-id="85ea8-195">You can set a simple filter directly on a list within using the filter pane, namely a filter that displays only records with the same value as in the selected cell.</span></span> <span data-ttu-id="85ea8-196">Selecteer een cel in de lijst, kies de vervolgkeuzepijl en kies vervolgens de actie **Filteren op deze waarde**.</span><span class="sxs-lookup"><span data-stu-id="85ea8-196">Select a cell on the list, choose the drop-down arrow, and then choose the **Filter to This Value** action.</span></span> <span data-ttu-id="85ea8-197">U kunt ook drukken op **Alt+F3**.</span><span class="sxs-lookup"><span data-stu-id="85ea8-197">Alternatively, press **Alt+F3**.</span></span>

### <a name="setting-filters-in-reports-batch-jobs-and-xmlports"></a><span data-ttu-id="85ea8-198">Filters instellen in rapporten, batchtaken en XMLports</span><span class="sxs-lookup"><span data-stu-id="85ea8-198">Setting Filters in Reports, Batch Jobs, and XMLports</span></span>

<span data-ttu-id="85ea8-199">Voor rapporten, batchtaken en XMLports zijn de filters direct zichtbaar op de aanvraagpagina.</span><span class="sxs-lookup"><span data-stu-id="85ea8-199">For reports and XMLports, the filters are visible directly on the request page.</span></span> <span data-ttu-id="85ea8-200">De aanvraagpagina toont de laatst gebruikte filters volgens uw selectie in het veld **Standaardwaarden gebruiken uit**.</span><span class="sxs-lookup"><span data-stu-id="85ea8-200">The request page displays the last used filters according to your selection in the **Use default values from** field.</span></span> <span data-ttu-id="85ea8-201">Zie voor meer informatie [Opgeslagen instellingen gebruiken](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="85ea8-201">For more information, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

<span data-ttu-id="85ea8-202">De hoofdsectie **Filter** toont de standaardfiltervelden die u gebruikt om af te bakenen welke records in het rapport of de XMLport moeten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="85ea8-202">The main **Filter** section shows the default filter fields that you use to delimit which records to include in the report or XMLport.</span></span> <span data-ttu-id="85ea8-203">Als u een filter wilt toevoegen, kiest u de actie **+ Filter**.</span><span class="sxs-lookup"><span data-stu-id="85ea8-203">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="85ea8-204">Typ vervolgens de naam van het veld waarop u wilt filteren of kies een veld in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="85ea8-204">Then, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

<span data-ttu-id="85ea8-205">In de sectie **Totalen filteren op** kunt u verschillende dimensies aanpassen die van invloed zijn op berekeningen in het rapport of de XMLport.</span><span class="sxs-lookup"><span data-stu-id="85ea8-205">In the **Filter totals by** section, you can adjust various dimensions that influence calculations in the report or XMLport.</span></span> <span data-ttu-id="85ea8-206">Als u een filter wilt toevoegen, kiest u de actie **+ Filter**.</span><span class="sxs-lookup"><span data-stu-id="85ea8-206">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="85ea8-207">Typ vervolgens de naam van het veld waarop u wilt filteren of kies een veld in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="85ea8-207">Then, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

## <a name="entering-filter-criteria"></a><span data-ttu-id="85ea8-208">Filtercriteria invoeren</span><span class="sxs-lookup"><span data-stu-id="85ea8-208">Entering Filter Criteria</span></span>

<span data-ttu-id="85ea8-209">Zowel in het filtervenster als op een aanvraagpagina voert u uw filtercriteria in het vak onder het filterveld in.</span><span class="sxs-lookup"><span data-stu-id="85ea8-209">Both in the filter pane and on a request page, you enter your filter criteria in the box under the filter field.</span></span>

<span data-ttu-id="85ea8-210">Het type filterveld bepaalt welke criteria u kunt invoeren.</span><span class="sxs-lookup"><span data-stu-id="85ea8-210">The type of the filter field determines which criteria you can enter.</span></span> <span data-ttu-id="85ea8-211">Als u bijvoorbeeld filtert op een veld dat vaste waarden heeft, kunt u alleen kiezen uit die waarden.</span><span class="sxs-lookup"><span data-stu-id="85ea8-211">For example, filtering a field that has fixed values will only let you choose from those values.</span></span> <span data-ttu-id="85ea8-212">Voor meer informatie over speciale filtersymbolen raadpleegt u [Filtercriteria](#FilterCriteria) en [Filtertokens](#FilterTokens)</span><span class="sxs-lookup"><span data-stu-id="85ea8-212">For more information about special filter symbols, see [Filter criteria](#FilterCriteria) and [Filter tokens](#FilterTokens).</span></span>

<span data-ttu-id="85ea8-213">Kolommen die al filters bevatten, worden aangegeven door het pictogram ![Filterpictogram](media/ui-search/filter-icon.png "Pictogram Filter") in de kolomkop.</span><span class="sxs-lookup"><span data-stu-id="85ea8-213">Columns that already have filters are indicated by the ![Filter icon](media/ui-search/filter-icon.png "Filter icon") icon in the column heading.</span></span> <span data-ttu-id="85ea8-214">Als u een filter wilt verwijderen, kiest u de vervolgkeuzepijl en kiest u vervolgens de actie **Filter wissen**.</span><span class="sxs-lookup"><span data-stu-id="85ea8-214">To remove a filter, choose the drop-down arrow, and then choose the **Clear Filter** action.</span></span>

> [!TIP]
> <span data-ttu-id="85ea8-215">Versnel het zoeken en analyseren van uw gegevens met combinaties van toetsenbordsneltoetsen.</span><span class="sxs-lookup"><span data-stu-id="85ea8-215">Accelerate finding and analyzing your data by using combinations of keyboard shortcuts.</span></span> <span data-ttu-id="85ea8-216">Selecteer bijvoorbeeld een veld, gebruik **Shift+Alt+F3** om dat veld aan het filterdeelvenster toe te voegen, typ het filtercriterium, gebruik **Ctrl+Enter** om terug te keren naar de rijen, selecteer een ander veld en gebruik **Alt+F3** om op die waarde te filteren.</span><span class="sxs-lookup"><span data-stu-id="85ea8-216">For example, select a field, use **Shift+Alt+F3** to add that field to the filter pane, type the filter criteria, use **Ctrl+Enter** to return to the rows, select another field, and use **Alt+F3** to filter to that value.</span></span> <span data-ttu-id="85ea8-217">Zie voor meer informatie [Toetsenbordsneltoetsen](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="85ea8-217">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

### <a name="filter-criteria-and-operators"></a><span data-ttu-id="85ea8-218"><a name="FilterCriteria"> </a>Filtercriteria en -operatoren</span><span class="sxs-lookup"><span data-stu-id="85ea8-218"><a name="FilterCriteria"> </a>Filter Criteria and Operators</span></span>

<span data-ttu-id="85ea8-219">U kunt bij de invoer van criteria alle cijfers en letters gebruiken die u normaal ook kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="85ea8-219">When you enter criteria, you can use all the numbers and letters that you normally use in the field.</span></span> <span data-ttu-id="85ea8-220">Maar er is ook een reeks speciale symbolen die u als operatoren kunt gebruiken om de resultaten verder te filteren.</span><span class="sxs-lookup"><span data-stu-id="85ea8-220">But there's also a set of special symbols that you can use as operators to further filter the results.</span></span> <span data-ttu-id="85ea8-221">In de volgende secties worden deze symbolen beschreven en hoe u ze als operators in filters kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="85ea8-221">The following sections describe these symbols and how to use them as operators in filters.</span></span>

> [!TIP]
> <span data-ttu-id="85ea8-222">Zie voor meer informatie over het filteren van datums en tijden [Werken met kalenderdatums en -tijden](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="85ea8-222">For more information about filtering dates and times, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="85ea8-223">Er kunnen situaties zijn waarin de waarde waarop u wilt filteren een symbool bevat dat een operator is.</span><span class="sxs-lookup"><span data-stu-id="85ea8-223">There may be situations where the value that you want to filter on contains a symbol that's an operator.</span></span> <span data-ttu-id="85ea8-224">Zie voor meer informatie over het omgaan met deze situaties [Filteren op waarden die symbolen bevatten](#symbols) voor meer instructies over het omgaan met deze situatie.</span><span class="sxs-lookup"><span data-stu-id="85ea8-224">For more information about handling these situtions, see [Filtering on Values That Contain Symbols](#symbols) for more instructions about handling this situation.</span></span>
>
> - <span data-ttu-id="85ea8-225">Als er meer dan 200 operatoren in één filter zijn, groepeert het systeem automatisch enkele uitdrukkingen tussen haakjes `()` met het oog op verwerking.</span><span class="sxs-lookup"><span data-stu-id="85ea8-225">If there are more than 200 operators in a single filter, the system will automatically group some expressions in parentheses `()` for the purpose of processing.</span></span> <span data-ttu-id="85ea8-226">Dit heeft geen effect op het filter of de resultaten.</span><span class="sxs-lookup"><span data-stu-id="85ea8-226">This has no effect on the filter or the results.</span></span>  

#### <a name="-interval"></a><span data-ttu-id="85ea8-227">(..) Interval</span><span class="sxs-lookup"><span data-stu-id="85ea8-227">(..) Interval</span></span>

|<span data-ttu-id="85ea8-228">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="85ea8-228">Sample Expression</span></span>|<span data-ttu-id="85ea8-229">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="85ea8-229">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1100..2100`|<span data-ttu-id="85ea8-230">Nummers 1100 t/m 2100</span><span class="sxs-lookup"><span data-stu-id="85ea8-230">Numbers 1100 through 2100</span></span>|  
|`..2500`|<span data-ttu-id="85ea8-231">Tot en met 2500</span><span class="sxs-lookup"><span data-stu-id="85ea8-231">Up to and including 2500</span></span>|  
|`..12 31 00`|<span data-ttu-id="85ea8-232">Datums tot en met 31.12.00</span><span class="sxs-lookup"><span data-stu-id="85ea8-232">Dates up to and including 12 31 00</span></span>|  
|`P8..`|<span data-ttu-id="85ea8-233">Informatie voor boekhoudperiode 8 en daarna</span><span class="sxs-lookup"><span data-stu-id="85ea8-233">Information for accounting period 8 and after</span></span>|  
|`..23`|<span data-ttu-id="85ea8-234">Van begindatum tot 23 lopende maand, lopend jaar 23:59:59</span><span class="sxs-lookup"><span data-stu-id="85ea8-234">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|`23..`|<span data-ttu-id="85ea8-235">Van 23 lopende maand, lopend jaar 00:00:00 tot eindtijd</span><span class="sxs-lookup"><span data-stu-id="85ea8-235">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|`22..23`|<span data-ttu-id="85ea8-236">Van 22 lopende maand, lopend jaar 0:00:00 tot 23 lopende maand, lopend jaar 23:59:59</span><span class="sxs-lookup"><span data-stu-id="85ea8-236">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  

#### <a name="124-eitheror"></a><span data-ttu-id="85ea8-237">(&#124;) Of/of</span><span class="sxs-lookup"><span data-stu-id="85ea8-237">(&#124;) Either/or</span></span>

|<span data-ttu-id="85ea8-238">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="85ea8-238">Sample Expression</span></span>|<span data-ttu-id="85ea8-239">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="85ea8-239">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1200|1300`|<span data-ttu-id="85ea8-240">Nummers met 1200 of 1300</span><span class="sxs-lookup"><span data-stu-id="85ea8-240">Numbers with 1200 or 1300</span></span>|  

#### <a name="-not-equal-to"></a><span data-ttu-id="85ea8-241">(<>) Niet gelijk aan</span><span class="sxs-lookup"><span data-stu-id="85ea8-241">(<>) Not equal to</span></span>  

|<span data-ttu-id="85ea8-242">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="85ea8-242">Sample Expression</span></span>|<span data-ttu-id="85ea8-243">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="85ea8-243">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<>0`|<span data-ttu-id="85ea8-244">Alle nummers behalve 0</span><span class="sxs-lookup"><span data-stu-id="85ea8-244">All numbers except 0</span></span><br /><br /> <span data-ttu-id="85ea8-245">Met de SQL Server-optie kunt u dit symbool combineren met jokertekens.</span><span class="sxs-lookup"><span data-stu-id="85ea8-245">The SQL Server Option allows you to combine this symbol with a wild-card expression.</span></span> <span data-ttu-id="85ea8-246"><>A\* betekent bijvoorbeeld 'Niet gelijk aan tekst die begint met A'.</span><span class="sxs-lookup"><span data-stu-id="85ea8-246">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  

#### <a name="-greater-than"></a><span data-ttu-id="85ea8-247">(>) Groter dan</span><span class="sxs-lookup"><span data-stu-id="85ea8-247">(>) Greater than</span></span>  

|<span data-ttu-id="85ea8-248">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="85ea8-248">Sample Expression</span></span>|<span data-ttu-id="85ea8-249">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="85ea8-249">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>1200`|<span data-ttu-id="85ea8-250">Nummers groter dan 1200</span><span class="sxs-lookup"><span data-stu-id="85ea8-250">Numbers greater than 1200</span></span>|  

#### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="85ea8-251">(>=) Groter dan of gelijk aan</span><span class="sxs-lookup"><span data-stu-id="85ea8-251">(>=) Greater than or equal to</span></span>  

|<span data-ttu-id="85ea8-252">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="85ea8-252">Sample Expression</span></span>|<span data-ttu-id="85ea8-253">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="85ea8-253">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>=1200`|<span data-ttu-id="85ea8-254">Nummers groter dan of gelijk aan 1200</span><span class="sxs-lookup"><span data-stu-id="85ea8-254">Numbers greater than or equal to 1200</span></span>|  

#### <a name="-less-than"></a><span data-ttu-id="85ea8-255">(<) Kleiner dan</span><span class="sxs-lookup"><span data-stu-id="85ea8-255">(<) Less than</span></span>  

|<span data-ttu-id="85ea8-256">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="85ea8-256">Sample Expression</span></span>|<span data-ttu-id="85ea8-257">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="85ea8-257">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<1200`|<span data-ttu-id="85ea8-258">Nummers kleiner dan 1200</span><span class="sxs-lookup"><span data-stu-id="85ea8-258">Numbers less than 1200</span></span>|  

#### <a name="-less-than-or-equal-to"></a><span data-ttu-id="85ea8-259">(<=) Kleiner dan of gelijk aan</span><span class="sxs-lookup"><span data-stu-id="85ea8-259">(<=) Less than or equal to</span></span>  

|<span data-ttu-id="85ea8-260">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="85ea8-260">Sample Expression</span></span>|<span data-ttu-id="85ea8-261">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="85ea8-261">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<=1200`|<span data-ttu-id="85ea8-262">Nummers kleiner dan of gelijk aan 1200</span><span class="sxs-lookup"><span data-stu-id="85ea8-262">Numbers less than or equal to 1200</span></span>|  

#### <a name="-and"></a><span data-ttu-id="85ea8-263">(&) En</span><span class="sxs-lookup"><span data-stu-id="85ea8-263">(&) And</span></span>  

|<span data-ttu-id="85ea8-264">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="85ea8-264">Sample Expression</span></span>|<span data-ttu-id="85ea8-265">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="85ea8-265">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>200&<1200`|<span data-ttu-id="85ea8-266">Getallen groter dan 200 en kleiner dan 1200</span><span class="sxs-lookup"><span data-stu-id="85ea8-266">Numbers greater than 200 and less than 1200</span></span>|  

#### <a name="-an-exact-character-match"></a><span data-ttu-id="85ea8-267">('') Een exacte tekenovereenkomst</span><span class="sxs-lookup"><span data-stu-id="85ea8-267">('') An exact character match</span></span>  

|<span data-ttu-id="85ea8-268">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="85ea8-268">Sample Expression</span></span>|<span data-ttu-id="85ea8-269">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="85ea8-269">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`'man'`|<span data-ttu-id="85ea8-270">Tekst die exact overeenkomt met **man** en hoofdlettergevoelig is.</span><span class="sxs-lookup"><span data-stu-id="85ea8-270">Text that matches **man** exactly and is case-sensitive.</span></span>|  

#### <a name="-case-insensitive"></a><span data-ttu-id="85ea8-271">(@) Niet hoofdlettergevoelig</span><span class="sxs-lookup"><span data-stu-id="85ea8-271">(@) Case insensitive</span></span>  

|<span data-ttu-id="85ea8-272">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="85ea8-272">Sample Expression</span></span>|<span data-ttu-id="85ea8-273">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="85ea8-273">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`@man*`|<span data-ttu-id="85ea8-274">Tekst die begint met **man** en niet hoofdlettergevoelig is.</span><span class="sxs-lookup"><span data-stu-id="85ea8-274">Text that starts with **man** and is case insensitive.</span></span>|  

#### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="85ea8-275">(\*) Een onbeperkt aantal onbekende tekens</span><span class="sxs-lookup"><span data-stu-id="85ea8-275">(\*) An indefinite number of unknown characters</span></span>

|<span data-ttu-id="85ea8-276">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="85ea8-276">Sample Expression</span></span>|<span data-ttu-id="85ea8-277">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="85ea8-277">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`*Co*`|<span data-ttu-id="85ea8-278">Tekst die **Co** bevat en hoofdlettergevoelig is.</span><span class="sxs-lookup"><span data-stu-id="85ea8-278">Text that contains **Co** and is case-sensitive.</span></span>|  
|`*Co`|<span data-ttu-id="85ea8-279">Tekst die eindigt met **Co** en hoofdlettergevoelig is.</span><span class="sxs-lookup"><span data-stu-id="85ea8-279">Text that ends with **Co"** and is case-sensitive.</span></span>|  
|`Co*`|<span data-ttu-id="85ea8-280">Tekst die begint met **Co** en hoofdlettergevoelig is.</span><span class="sxs-lookup"><span data-stu-id="85ea8-280">Text that begins with **Co** and is case-sensitive.</span></span>|  

#### <a name="-one-unknown-character"></a><span data-ttu-id="85ea8-281">(?) Een onbekend teken</span><span class="sxs-lookup"><span data-stu-id="85ea8-281">(?) One unknown character</span></span>  

|<span data-ttu-id="85ea8-282">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="85ea8-282">Sample Expression</span></span>|<span data-ttu-id="85ea8-283">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="85ea8-283">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`Hans?n`|<span data-ttu-id="85ea8-284">Tekst zoals **Jansen** of **Jansma**</span><span class="sxs-lookup"><span data-stu-id="85ea8-284">Text such as **Hansen** or **Hanson**</span></span>|  

#### <a name="combined-format-expressions"></a><span data-ttu-id="85ea8-285">Gecombineerde notatiesoorten</span><span class="sxs-lookup"><span data-stu-id="85ea8-285">Combined Format Expressions</span></span>  

|<span data-ttu-id="85ea8-286">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="85ea8-286">Sample Expression</span></span>|<span data-ttu-id="85ea8-287">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="85ea8-287">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|<span data-ttu-id="85ea8-288">Alle records met het nummer 5999 of een nummer uit het interval 8100 tot en met 8490.</span><span class="sxs-lookup"><span data-stu-id="85ea8-288">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|`..1299|1400..`|<span data-ttu-id="85ea8-289">Records met een nummer kleiner dan of gelijk aan 1299 of gelijk aan 1400 en hoger. Met andere woorden: alle nummers behalve 1300 tot en met 1399.</span><span class="sxs-lookup"><span data-stu-id="85ea8-289">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|`>50&<100`|<span data-ttu-id="85ea8-290">Records met een nummer groter dan 50 en kleiner dan 100, ofwel nummer 51 tot en met 99.</span><span class="sxs-lookup"><span data-stu-id="85ea8-290">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  

### <a name="filtering-on-values-that-contain-symbols"></a><a name="symbols"></a><span data-ttu-id="85ea8-291">Filteren op waarden die symbolen bevatten</span><span class="sxs-lookup"><span data-stu-id="85ea8-291">Filtering on Values That Contain Symbols</span></span>

<span data-ttu-id="85ea8-292">Er kunnen gevallen zijn waarin veldwaarden een van de volgende symbolen bevatten:</span><span class="sxs-lookup"><span data-stu-id="85ea8-292">There may be cases where field values contain the one of the following symbols:</span></span>

- &
- <span data-ttu-id="85ea8-293">(</span><span class="sxs-lookup"><span data-stu-id="85ea8-293">(</span></span>
- <span data-ttu-id="85ea8-294">)</span><span class="sxs-lookup"><span data-stu-id="85ea8-294">)</span></span>
- =
- <span data-ttu-id="85ea8-295">&#124;</span><span class="sxs-lookup"><span data-stu-id="85ea8-295">&#124;</span></span>

<span data-ttu-id="85ea8-296">Als u op een van deze symbolen wilt filteren, plaatst u de filterexpressie tussen aanhalingstekens ('').</span><span class="sxs-lookup"><span data-stu-id="85ea8-296">If you want to filter on any of these symbols, place the filter expression in quotation marks ('').</span></span> <span data-ttu-id="85ea8-297">Als u bijvoorbeeld wilt filteren op records die beginnen met de tekst *J & V*, is de filterexpressie `'J & V*'`.</span><span class="sxs-lookup"><span data-stu-id="85ea8-297">For example, if you wanted to filter on records that start with the text *J & V*, the filter expression would be `'J & V*'`.</span></span>

<span data-ttu-id="85ea8-298">Deze vereiste is niet nodig voor andere symbolen.</span><span class="sxs-lookup"><span data-stu-id="85ea8-298">This requirement isn't necessary for other symbols.</span></span>

### <a name="filter-tokens"></a><span data-ttu-id="85ea8-299"><a name="FilterTokens"> </a>Filtertokens</span><span class="sxs-lookup"><span data-stu-id="85ea8-299"><a name="FilterTokens"> </a>Filter Tokens</span></span>

<span data-ttu-id="85ea8-300">Wanneer u filtercriteria invoert, kunt u ook woorden typen die een speciale betekenis hebben, filtertokens genaamd.</span><span class="sxs-lookup"><span data-stu-id="85ea8-300">When entering filter criteria, you can also type words that have special meaning, called filter tokens.</span></span> <span data-ttu-id="85ea8-301">Na het invoeren van het tokenwoord wordt het woord vervangen door de waarde of waarden die het woord vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="85ea8-301">After entering the token word, the word is replaced by the value or values that it represents.</span></span> <span data-ttu-id="85ea8-302">Filtertokens maken filtering eenvoudiger doordat u niet naar andere pagina's hoeft te navigeren om waarden op te zoeken die u aan uw filter wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="85ea8-302">Filter tokens make filtering easier by reducing the need to navigate to other pages to look up values you want to add to your filter.</span></span> <span data-ttu-id="85ea8-303">In de onderstaande tabellen worden enkele van de tokens beschreven die u als filtercriteria kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="85ea8-303">The tables below describe some of the tokens you can type as filter criteria.</span></span>

> [!TIP]
> <span data-ttu-id="85ea8-304">Uw organisatie kan aangepaste tokens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="85ea8-304">Your organization may use custom tokens.</span></span> <span data-ttu-id="85ea8-305">Als u informatie wilt over de volledige set tokens die voor u beschikbaar zijn of als u aangepaste tokens wilt toevoegen, overlegt u met uw beheerder.</span><span class="sxs-lookup"><span data-stu-id="85ea8-305">To learn about the complete set of tokens available to you or to add more custom tokens, talk to your administrator.</span></span> <span data-ttu-id="85ea8-306">Voor technische informatie raadpleegt u [Filtertokens toevoegen](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span><span class="sxs-lookup"><span data-stu-id="85ea8-306">For technical information see [Adding Filter Tokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span></span>

#### <a name="me-or-userid-records-assigned-to-you"></a><span data-ttu-id="85ea8-307">(%me of %userid) Records die aan u zijn toegewezen</span><span class="sxs-lookup"><span data-stu-id="85ea8-307">(%me or %userid) Records Assigned to You</span></span>

<span data-ttu-id="85ea8-308">Gebruik `%me` of `%userid` wanneer u velden filtert die de gebruikers-id bevatten, zoals het veld **Toegewezen aan gebruikers-id**, om alle records weer te geven die aan u zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="85ea8-308">Use `%me` or `%userid` when filtering fields that contain the user ID, such as **Assigned to User ID** field, to display all records that are assigned to you.</span></span>

|<span data-ttu-id="85ea8-309">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="85ea8-309">Sample Expression</span></span>|<span data-ttu-id="85ea8-310">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="85ea8-310">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%me`<br /><span data-ttu-id="85ea8-311">of</span><span class="sxs-lookup"><span data-stu-id="85ea8-311">or</span></span><br />`%userid`|<span data-ttu-id="85ea8-312">Records die aan uw gebruikersaccount zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="85ea8-312">Records that are assigned to your user account.</span></span> |  

#### <a name="mycustomers-customers-in-my-customers"></a><span data-ttu-id="85ea8-313">(%mycustomers) Klanten in Mijn klanten</span><span class="sxs-lookup"><span data-stu-id="85ea8-313">(%mycustomers) Customers in My Customers</span></span>

<span data-ttu-id="85ea8-314">Gebruik `%mycustomers` in het veld klant **nr.** om alle records weer te geven voor klanten die deel uitmaken van de lijst **Mijn klanten** in uw rolcentrum.</span><span class="sxs-lookup"><span data-stu-id="85ea8-314">Use `%mycustomers` in the customer **No** field to display all records for customers that are included in the **My Customers** list on your Role Center.</span></span>

|<span data-ttu-id="85ea8-315">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="85ea8-315">Sample Expression</span></span>|<span data-ttu-id="85ea8-316">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="85ea8-316">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%mycustomers`|<span data-ttu-id="85ea8-317">Klanten in **Mijn klanten** in uw rolcentrum.</span><span class="sxs-lookup"><span data-stu-id="85ea8-317">Customers in the **My Customers** on your Role Center.</span></span> |  

#### <a name="myitems-items-in-my-items"></a><span data-ttu-id="85ea8-318">(%myitems) Artikelen in Mijn artikelen</span><span class="sxs-lookup"><span data-stu-id="85ea8-318">(%myitems) Items in My Items</span></span>

<span data-ttu-id="85ea8-319">Gebruik `%myitems` in het veld artikel **nr.** om alle records weer te geven voor artikelen die deel uitmaken van de lijst **Mijn artikelen** in uw rolcentrum.</span><span class="sxs-lookup"><span data-stu-id="85ea8-319">Use `%myitems` in the item **No** field to display all records for items that are included in the **My Items** list on your Role Center.</span></span>

|<span data-ttu-id="85ea8-320">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="85ea8-320">Sample Expression</span></span>|<span data-ttu-id="85ea8-321">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="85ea8-321">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myitems`|<span data-ttu-id="85ea8-322">Artikelen in **Mijn artikelen** in uw rolcentrum.</span><span class="sxs-lookup"><span data-stu-id="85ea8-322">Items in the **My Items** on your Role Center.</span></span> |  

#### <a name="myvendors-vendors-in-my-vendors"></a><span data-ttu-id="85ea8-323">(%myvendors) Leveranciers in Mijn leveranciers</span><span class="sxs-lookup"><span data-stu-id="85ea8-323">(%myvendors) Vendors in My Vendors</span></span>

<span data-ttu-id="85ea8-324">Gebruik `%myvendors` in het veld leveranciers **nr.** om alle records weer te geven voor leveranciers die deel uitmaken van de lijst **Mijn leveranciers** in uw rolcentrum.</span><span class="sxs-lookup"><span data-stu-id="85ea8-324">Use `%myvendors` in the vendor **No** field to display all records for vendors that are included in the **My Vendors** list on your Role Center.</span></span>

|<span data-ttu-id="85ea8-325">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="85ea8-325">Sample Expression</span></span>|<span data-ttu-id="85ea8-326">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="85ea8-326">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myvendors`|<span data-ttu-id="85ea8-327">Leveranciers in **Mijn leveranciers** in uw rolcentrum.</span><span class="sxs-lookup"><span data-stu-id="85ea8-327">Vendors in the **My Vendors** on your Role Center.</span></span> |  

## <a name="see-also"></a><span data-ttu-id="85ea8-328">Zie ook</span><span class="sxs-lookup"><span data-stu-id="85ea8-328">See Also</span></span>

[<span data-ttu-id="85ea8-329">Zoeken en filteren - Veelgestelde vragen</span><span class="sxs-lookup"><span data-stu-id="85ea8-329">Searching and Filtering FAQ</span></span>](ui-search-filter-faq.md)  
[<span data-ttu-id="85ea8-330">Lijstweergaven opslaan en personaliseren</span><span class="sxs-lookup"><span data-stu-id="85ea8-330">Save and Personalize List Views</span></span>](ui-views.md)  
<span data-ttu-id="85ea8-331">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="85ea8-331">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]