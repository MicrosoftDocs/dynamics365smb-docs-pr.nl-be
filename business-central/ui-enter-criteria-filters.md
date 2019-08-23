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
# <a name="sorting-searching-and-filtering-lists"></a><span data-ttu-id="30dc2-103">Lijsten sorteren, doorzoeken en filteren</span><span class="sxs-lookup"><span data-stu-id="30dc2-103">Sorting, Searching, and Filtering Lists</span></span>
<span data-ttu-id="30dc2-104">U kunt een paar dingen doen om records in een lijst te scannen, te vinden en te beperken.</span><span class="sxs-lookup"><span data-stu-id="30dc2-104">There are a few things that you can do that will help you scan, find, and limit records in a list.</span></span> <span data-ttu-id="30dc2-105">U kunt de records bijvoorbeeld sorteren, doorzoeken en filteren.</span><span class="sxs-lookup"><span data-stu-id="30dc2-105">These include sorting, searching and filtering.</span></span> <span data-ttu-id="30dc2-106">U kunt sommige of al deze methoden tegelijkertijd toepassen om snel uw gegevens te zoeken of te analyseren.</span><span class="sxs-lookup"><span data-stu-id="30dc2-106">You can apply some or all of these simultaneously to quickly find or analyze your data.</span></span>

> [!TIP]
> <span data-ttu-id="30dc2-107">Wanneer u uw gegevens weergeeft als tegels, kunt u zoeken en elementaire filtering gebruiken.</span><span class="sxs-lookup"><span data-stu-id="30dc2-107">When viewing your data as tiles, you can search and use basic filtering.</span></span> <span data-ttu-id="30dc2-108">Als u de volledige set functies wilt gebruiken voor sorteren, zoeken en filteren, kiest u het pictogram ![Als overzicht weergeven](media/ui_show_as_list_icon.png "linkerpijl Als overzicht weergeven") om gegevens als lijst weer te geven.</span><span class="sxs-lookup"><span data-stu-id="30dc2-108">To use the full set of powerful features for sorting, searching and filtering, choose the ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to show as a list.</span></span>

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a><span data-ttu-id="30dc2-109">Sorteervolgorde</span><span class="sxs-lookup"><span data-stu-id="30dc2-109">Sorting</span></span>
<span data-ttu-id="30dc2-110">Met de sorteerfunctie krijgt u snel een overzicht van de gegevens.</span><span class="sxs-lookup"><span data-stu-id="30dc2-110">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="30dc2-111">Als u veel klanten hebt, kunt u er bijvoorbeeld voor kiezen hen te sorteren op **Klantnr.**, **Klantboekingsgroep**, **Valutacode**, **Land-/regiocode** of **Btw-nummer** voor het door u gewenste overzicht.</span><span class="sxs-lookup"><span data-stu-id="30dc2-111">If you have many customers, for example, you can choose to sort them by **Customer No.**, **Customer Posting Group**, **Currency Code**, **Country Region Code**, or **Sales Tax Registration No.** to get the overview you need.</span></span>

<span data-ttu-id="30dc2-112">Als u een lijst wilt sorteren, kunt u een kolomkoptekst kiezen om te schakelen tussen op- en aflopend, of de kleine pijl-omlaag in de kolomkop kiezen en vervolgens **Oplopend** of **Aflopend** kiezen.</span><span class="sxs-lookup"><span data-stu-id="30dc2-112">To sort a list, you can either choose a column heading text to toggle between ascending and descending order, or choose the small down arrow in the column heading, and then choose **Ascending** or **Descending**.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="30dc2-113">Sorteren wordt niet ondersteund bij afbeeldingen, BLOB-velden, FlowFilters en velden die niet deel van een tabel zijn.</span><span class="sxs-lookup"><span data-stu-id="30dc2-113">Sorting is not supported on images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching"></a><span data-ttu-id="30dc2-114">Zoeken</span><span class="sxs-lookup"><span data-stu-id="30dc2-114">Searching</span></span>
<!--## Searching by using the Quick Filter -->
<span data-ttu-id="30dc2-115">Boven aan elke lijstpagina staat een ![lijst Zoeken](media/ui-search/search-list.png "pictogram Lijst Zoeken") pictogram **Zoeken** dat een snelle en gemakkelijke manier biedt om de records in een lijst te reduceren en alleen de records weer te geven die de gegevens bevatten die u wilt zien.</span><span class="sxs-lookup"><span data-stu-id="30dc2-115">At the top of each list page, there is a ![Search list](media/ui-search/search-list.png "Search list icon") **Search** icon that provides a quick and easy way to reduce the records in a list and display only those records that contain the data that you are interested in seeing.</span></span>

<span data-ttu-id="30dc2-116">Als u wilt zoeken, selecteert u het zoekpictogram en typt u de tekst die u zoekt, in het vak.</span><span class="sxs-lookup"><span data-stu-id="30dc2-116">To search, simply select the search icon, and then in the box, type the text that you are looking for.</span></span> <span data-ttu-id="30dc2-117">U kunt letters, cijfers en andere symbolen invoeren.</span><span class="sxs-lookup"><span data-stu-id="30dc2-117">You can enter letters, numbers, and other symbols.</span></span>

### <a name="fine-tuning-the-search"></a><span data-ttu-id="30dc2-118">De zoekactie verfijnen</span><span class="sxs-lookup"><span data-stu-id="30dc2-118">Fine-tuning the Search</span></span>
<span data-ttu-id="30dc2-119">Over het algemeen probeert de zoekactie tekst te vinden in alle velden. Er wordt geen onderscheid gemaakt tussen kleine letters en hoofdletters (hoofdletterongevoelig dus) en er wordt tekst overal in het veld gezocht (aan het begin, aan het einde of in het midden).</span><span class="sxs-lookup"><span data-stu-id="30dc2-119">In general, search will attempt to match text across all fields; it does not distinguish between uppercase and lowercase characters (in other words, case insensitive), and will match text placed anywhere in the field (at the beginning, end, or in the middle).</span></span>

<span data-ttu-id="30dc2-120">U kunt echter een exactere zoekactie maken door de volgende speciale tekens te gebruiken:</span><span class="sxs-lookup"><span data-stu-id="30dc2-120">However, you can make a more exact search by using the following special characters:</span></span>

- <span data-ttu-id="30dc2-121">Als u alleen veldwaarden wilt zoeken die exact overeenkomen met de volledige tekst en de hoofdletters/kleine letters, plaatst u de zoektekst tussen enkele aanhalingstekens (`''` bijvoorbeeld `'man'`).</span><span class="sxs-lookup"><span data-stu-id="30dc2-121">To find only field values that match the entire text and case exactly, place the search text between single quotes `''` (for example, `'man'`).</span></span>

- <span data-ttu-id="30dc2-122">Als u veldwaarden wilt zoeken die beginnen met een bepaalde tekst en overeenkomen met de hoofdletters/kleine letters, plaatst u `*` achter de tekst (bijvoorbeeld `man*`).</span><span class="sxs-lookup"><span data-stu-id="30dc2-122">To find field values that start with a certain text and match the case, place `*` after the search text (for example `man*`).</span></span>

- <span data-ttu-id="30dc2-123">Als u veldwaarden wilt zoeken die eindigen met een bepaalde tekst en overeenkomen met de hoofdletters/kleine letters, plaatst u `*` vóór de tekst (bijvoorbeeld `*man`).</span><span class="sxs-lookup"><span data-stu-id="30dc2-123">To find field values that end with a certain text and match the case, place `*` before the search text (for example `*man`).</span></span>

- <span data-ttu-id="30dc2-124">Wanneer u `''` of `*` gebruikt, wordt onderscheid gemaakt tussen hoofdletters en kleine letters.</span><span class="sxs-lookup"><span data-stu-id="30dc2-124">When using  `''` or `*`, the search is case sensitive.</span></span> <span data-ttu-id="30dc2-125">Als u hoofdletterongevoelig wilt zoeken, plaatst u `@` vóór de zoektekst (bijvoorbeeld `@man*`).</span><span class="sxs-lookup"><span data-stu-id="30dc2-125">If you want to make the search case insensitive, place `@` before the search text (for example `@man*`).</span></span>

<span data-ttu-id="30dc2-126">In de volgende tabel vindt u enkele voorbeelden om aan te geven hoe u de zoekactie kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="30dc2-126">The following table provides some examples to explain how you can use the search.</span></span>

|<span data-ttu-id="30dc2-127">Zoekcriteria</span><span class="sxs-lookup"><span data-stu-id="30dc2-127">Search Criteria</span></span>|<span data-ttu-id="30dc2-128">Zoekt…</span><span class="sxs-lookup"><span data-stu-id="30dc2-128">Finds...</span></span>|
|---------------|----------|
|`man`<br /><span data-ttu-id="30dc2-129">of</span><span class="sxs-lookup"><span data-stu-id="30dc2-129">or</span></span> <br />`Man`|<span data-ttu-id="30dc2-130">Alle records met velden die de tekst **man** bevatten, ongeacht hoofdletters.</span><span class="sxs-lookup"><span data-stu-id="30dc2-130">All records with fields that contain the text **man**, regardless of the case.</span></span> <span data-ttu-id="30dc2-131">Bijvoorbeeld **Manchester**, **manual** of **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="30dc2-131">For example, **Manchester**, **manual**, or **Sportsman**.</span></span> |
|`'Man'`|<span data-ttu-id="30dc2-132">Alle records met velden die alleen **Man** bevatten, ongeacht hoofdletters.</span><span class="sxs-lookup"><span data-stu-id="30dc2-132">All records with fields that contain only **Man**, matching the case.</span></span>|
|`Man*`|<span data-ttu-id="30dc2-133">Alle records met velden die beginnen met de tekst <b>Man</b>, met identieke hoofdletters/kleine letters.</span><span class="sxs-lookup"><span data-stu-id="30dc2-133">All records with fields that start with the text <b>Man</b>, matching the case.</span></span> <span data-ttu-id="30dc2-134">Bijvoorbeeld **Manchester**, maar niet **manual** of **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="30dc2-134">For example, **Manchester** but not **manual** or **Sportsman**.</span></span>|
|`@Man*`|<span data-ttu-id="30dc2-135">Alle records met velden die beginnen met **man**, ongeacht hoofdletters.</span><span class="sxs-lookup"><span data-stu-id="30dc2-135">All records with fields that start with **man**, regardless of the case.</span></span> <span data-ttu-id="30dc2-136">Bijvoorbeeld **Manchester** en **manual**, maar niet **Sportsman**.</span><span class="sxs-lookup"><span data-stu-id="30dc2-136">For example, **Manchester** and **manual**, but not **Sportsman**.</span></span>|
|`@*man`|<span data-ttu-id="30dc2-137">Alle records met velden die eindigen met **man**, ongeacht hoofdletters.</span><span class="sxs-lookup"><span data-stu-id="30dc2-137">All records that end with **man**, regardless of the case.</span></span> <span data-ttu-id="30dc2-138">Bijvoorbeeld **Sportsman**, maar niet **Manchester** of **manual**.</span><span class="sxs-lookup"><span data-stu-id="30dc2-138">For example **Sportsman**, but not **Manchester** or **manual**.</span></span>|

> [!TIP]
> <span data-ttu-id="30dc2-139">U kunt op F3 drukken om het zoekvak te activeren en te deactiveren.</span><span class="sxs-lookup"><span data-stu-id="30dc2-139">You can press F3 to activate and deactivate the search box.</span></span> <span data-ttu-id="30dc2-140">Zie voor meer informatie [Toetsenbordsneltoetsen](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="30dc2-140">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

## <span data-ttu-id="30dc2-141"><a name="Filtering"> </a>Filteren</span><span class="sxs-lookup"><span data-stu-id="30dc2-141"><a name="Filtering"> </a>Filtering</span></span>
<span data-ttu-id="30dc2-142">Filtering biedt een geavanceerdere en flexibelere manier om te bepalen welke records in een lijst worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="30dc2-142">Filtering provides a more advanced and versatile way of controlling which records display in a list.</span></span> <span data-ttu-id="30dc2-143">Er zijn twee belangrijke verschillen tussen zoeken en filteren, zoals wordt beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="30dc2-143">There are two major differences between searching and filtering, as described in the table below.</span></span>

|| <span data-ttu-id="30dc2-144">**Zoeken**</span><span class="sxs-lookup"><span data-stu-id="30dc2-144">**Searching**</span></span> | <span data-ttu-id="30dc2-145">**Filteren**</span><span class="sxs-lookup"><span data-stu-id="30dc2-145">**Filtering**</span></span> |
|--|----------|------------|
| <span data-ttu-id="30dc2-146">**Toepasselijke velden**</span><span class="sxs-lookup"><span data-stu-id="30dc2-146">**Applicable fields**</span></span> | <span data-ttu-id="30dc2-147">Zoekt in alle velden die zichtbaar zijn op de pagina.</span><span class="sxs-lookup"><span data-stu-id="30dc2-147">Searches across all fields that are visible on the page.</span></span> | <span data-ttu-id="30dc2-148">Filtert een of meer velden afzonderlijk, selecterend vanuit een veld in de tabel, inclusief velden die niet zichtbaar zijn op de pagina.</span><span class="sxs-lookup"><span data-stu-id="30dc2-148">Filters one or more fields individually, selecting from any field on the table, including fields that are not visible on the page.</span></span> |
| <span data-ttu-id="30dc2-149">**Afstemmen**</span><span class="sxs-lookup"><span data-stu-id="30dc2-149">**Matching**</span></span> | <span data-ttu-id="30dc2-150">Geeft records weer met velden die voldoen aan de zoektekst, ongeacht hoofdletters/kleine letters of plaatsing van de tekst.</span><span class="sxs-lookup"><span data-stu-id="30dc2-150">Displays records with fields that match the search text, irrespective of casing or placement of that text.</span></span> | <span data-ttu-id="30dc2-151">Geeft records weer waar het veld exact overeenkomt met het filter en is hoofdlettergevoelig, tenzij speciale filtersymbolen worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="30dc2-151">Displays records where the field matches the filter exactly and is case sensitive, unless special filter symbols are entered.</span></span>

<span data-ttu-id="30dc2-152">Filteren stelt u in staat records weer te geven voor bepaalde rekeningen of klanten, datums, bedragen en andere informatie door filtercriteria op te geven.</span><span class="sxs-lookup"><span data-stu-id="30dc2-152">Filtering enables you to display records for specific accounts or customers, dates, amounts, and other information by specifying filter criteria.</span></span> <span data-ttu-id="30dc2-153">Alleen records die voldoen aan de criteria, worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="30dc2-153">Only records that match the criteria are displayed.</span></span> <span data-ttu-id="30dc2-154">Als u criteria opgeeft voor meerdere velden, worden alleen de records weergegeven die overeenkomen met alle criteria.</span><span class="sxs-lookup"><span data-stu-id="30dc2-154">If you specify criteria for multiple fields, then only records that match all criteria will be displayed.</span></span>

### <a name="working-in-the-filter-pane"></a><span data-ttu-id="30dc2-155">Werken in het filterdeelvenster</span><span class="sxs-lookup"><span data-stu-id="30dc2-155">Working in the Filter Pane</span></span>

<span data-ttu-id="30dc2-156">Als u het filterdeelvenster wilt weergeven, selecteert u het ![pictogram Filterdeelvenster](media/open-filter-pane-icon.png "pictogram Filterdeelvenster") boven aan de lijst of drukt u op **Shift+F3**.</span><span class="sxs-lookup"><span data-stu-id="30dc2-156">To display the filter pane, select ![Filter pane icon](media/open-filter-pane-icon.png "Filter pane icon") at the top of the list or press **Shift+F3**.</span></span> <span data-ttu-id="30dc2-157">Voor lijsten in het Rolcentrum kunt u ook de pijl omlaag kiezen naast de paginatitel op de navigatiebalk boven de lijst en vervolgens **Filterdeelvenster weergeven** kiezen, zoals u hier ziet:</span><span class="sxs-lookup"><span data-stu-id="30dc2-157">For lists within the Role Center, you can also choose the down arrow near the page title in the navigation bar above the list, and then choose **Show filter pane** as shown here:</span></span>

<span data-ttu-id="30dc2-158">![Filterdeelvenster weergeven](media/open-filter-pane.png "Filterdeelvenster weergeven")</span><span class="sxs-lookup"><span data-stu-id="30dc2-158">![Show filter pane](media/open-filter-pane.png "Show filter pane")</span></span>

<span data-ttu-id="30dc2-159">Het filterdeelvenster bevat de huidige filters voor een lijst en biedt u de mogelijkheid uw eigen filters in te stellen op een of meer velden.</span><span class="sxs-lookup"><span data-stu-id="30dc2-159">The filter pane displays the current filters for a list, and enables you to set your own custom filters on one or more fields.</span></span> <span data-ttu-id="30dc2-160">De volgende afbeelding toont een voorbeeldfilterdeelvenster voor een lijst verkoopoffertes.</span><span class="sxs-lookup"><span data-stu-id="30dc2-160">The following figure shows an example filter pane for a Sales Quotes list.</span></span>

<span data-ttu-id="30dc2-161">![Overzicht van filterdeelvenster ](media/filter-pane-overview.png "pictogram Filter")</span><span class="sxs-lookup"><span data-stu-id="30dc2-161">![Filter pane overview ](media/filter-pane-overview.png "Filter icon")</span></span>

<span data-ttu-id="30dc2-162">Een filterdeelvenster is verdeeld in drie gedeelten: **Weergaven**, **Filter lijst op** en **Filter totalen op**:</span><span class="sxs-lookup"><span data-stu-id="30dc2-162">A filter pane is divided in three sections: **Views**, **Filter list by**, and **Filter totals by**:</span></span>

- <span data-ttu-id="30dc2-163">**Weergaven**</span><span class="sxs-lookup"><span data-stu-id="30dc2-163">**Views**</span></span>

  <span data-ttu-id="30dc2-164">Sommige lijsten bevatten het gedeelte **Weergaven**.</span><span class="sxs-lookup"><span data-stu-id="30dc2-164">Some lists will include the **Views** section.</span></span> <span data-ttu-id="30dc2-165">Weergaven zijn variaties van de lijst die vooraf zijn ingesteld met filters.</span><span class="sxs-lookup"><span data-stu-id="30dc2-165">Views are variations of the list that have been preconfigured with filters.</span></span> <span data-ttu-id="30dc2-166">Als u naar een andere weergave van uw lijst wilt schakelen, selecteert u gewoon een koppeling.</span><span class="sxs-lookup"><span data-stu-id="30dc2-166">To switch to a different view of your list, simply select another link.</span></span> <span data-ttu-id="30dc2-167">U kunt de filters in een weergave tijdelijk wijzigen, maar de wijzigingen worden niet permanent opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="30dc2-167">You can temporarily change the filters on a view, but the changes will not be permanently saved.</span></span>

- <span data-ttu-id="30dc2-168">**Filter lijst op**</span><span class="sxs-lookup"><span data-stu-id="30dc2-168">**Filter list by**</span></span>

  <span data-ttu-id="30dc2-169">In het gedeelte **Filter lijst op** voegt u filters toe aan specifieke velden om het aantal weergegeven records te reduceren.</span><span class="sxs-lookup"><span data-stu-id="30dc2-169">The **Filter list by** section is where you add filters on specific fields to reduce the number of displayed records.</span></span> <span data-ttu-id="30dc2-170">Als u een filter wilt toevoegen, selecteert u **+ Filter**, selecteert u het veld dat u wilt filteren uit de velden in de tabel en voert u filtercriteria in het vak in.</span><span class="sxs-lookup"><span data-stu-id="30dc2-170">To add a filter, select **+ Filter**, select the field that you want to filter from any field in the table, and then enter filter criteria in the box.</span></span>

- <span data-ttu-id="30dc2-171">**Filter totalen op**</span><span class="sxs-lookup"><span data-stu-id="30dc2-171">**Filter totals by**</span></span>

  <span data-ttu-id="30dc2-172">Sommige lijsten met berekende velden, zoals bedragen en aantallen, bevatten het gedeelte **Filter totalen op**, waarin u verschillende dimensies kunt aanpassen die van invloed zijn op berekeningen.</span><span class="sxs-lookup"><span data-stu-id="30dc2-172">Some lists that display calculated fields, such as amounts and quantities, will include the **Filter totals by** section where you can adjust various dimensions that influence calculations.</span></span> <span data-ttu-id="30dc2-173">U kunt bijvoorbeeld snel uw rekeningschema analyseren door bedragen te filteren op een bepaalde periode of u kunt de totalen voor verkooporders uit alleen een bepaald magazijn weergeven.</span><span class="sxs-lookup"><span data-stu-id="30dc2-173">For example, you can quickly analyze your chart of accounts by filtering amounts to a specific period, or you can view the totals for sales orders only from a specific warehouse.</span></span>

  <span data-ttu-id="30dc2-174">Als u een filter wilt toevoegen, selecteert u **+ Filter**, selecteert een van de voorgedefinieerde dimensies en voegt u de filtercriteria in het vak toe.</span><span class="sxs-lookup"><span data-stu-id="30dc2-174">To add a filter, select **+ Filter**, select one of the predefined dimensions, and then add the filter criteria in the box.</span></span>

  > [!NOTE]
  > <span data-ttu-id="30dc2-175">Filters in het gedeelte **Filter totalen op** worden bepaald door FlowFilters in het paginaontwerp.</span><span class="sxs-lookup"><span data-stu-id="30dc2-175">Filters in the **Filter totals by** section are controlled by FlowFilters on the page design.</span></span> <span data-ttu-id="30dc2-176">Zie voor technische informatie [FlowFilters](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span><span class="sxs-lookup"><span data-stu-id="30dc2-176">For technical information, see [FlowFilters](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span></span>


### <a name="entering-filter-criteria-in-the-filter-pane"></a><span data-ttu-id="30dc2-177">Filtercriteria invoeren in het filterdeelvenster</span><span class="sxs-lookup"><span data-stu-id="30dc2-177">Entering Filter Criteria in the Filter Pane</span></span>
<span data-ttu-id="30dc2-178">Als u een veld wilt selecteren om op te filteren, voert u een van de volgende handelingen uit:</span><span class="sxs-lookup"><span data-stu-id="30dc2-178">To select a field to filter, do one of the following:</span></span>
  - <span data-ttu-id="30dc2-179">Kies in het filterdeelvenster **+ Veld**.</span><span class="sxs-lookup"><span data-stu-id="30dc2-179">In the filter pane, choose **+ Field**.</span></span> <span data-ttu-id="30dc2-180">Typ de naam van het veld dat u wilt filteren of kies een veld uit het menu met alle velden in de tabel.</span><span class="sxs-lookup"><span data-stu-id="30dc2-180">Type the name of the field you wish to filter, or pick a field from the menu that displays all fields in the table.</span></span>

  - <span data-ttu-id="30dc2-181">Kies in een kolomkop de pijl omlaag en kies vervolgens **Filteren...**. Zo opent u het filterdeelvenster en voegt u de kolom aan het filterdeelvenster toe.</span><span class="sxs-lookup"><span data-stu-id="30dc2-181">In a column heading, choose the down arrow, and then choose **Filter...**. This will open the filter pane and add the column to the filter pane.</span></span>

<span data-ttu-id="30dc2-182">U kunt nu uw filtercriteria in het vak typen of selecteren.</span><span class="sxs-lookup"><span data-stu-id="30dc2-182">You can now type or select your filter criteria in the box.</span></span> <span data-ttu-id="30dc2-183">Het type veld waarop u filtert, bepaalt welke criteria u kunt invoeren.</span><span class="sxs-lookup"><span data-stu-id="30dc2-183">The type of field you filter determines which criteria you can enter.</span></span> <span data-ttu-id="30dc2-184">Als u bijvoorbeeld filtert op een veld dat vaste waarden heeft, kunt u alleen kiezen uit die waarden.</span><span class="sxs-lookup"><span data-stu-id="30dc2-184">For example, filtering a field that has fixed values will only let you choose from those values.</span></span> <span data-ttu-id="30dc2-185">Voor meer informatie over speciale filtersymbolen raadpleegt u [Filtercriteria](#FilterCriteria) en [Filtertokens](#FilterTokens)</span><span class="sxs-lookup"><span data-stu-id="30dc2-185">For more information about special filter symbols, see [Filter criteria](#FilterCriteria) and [Filter tokens](#FilterTokens).</span></span>

<span data-ttu-id="30dc2-186">Kolommen die al filters bevatten, worden aangegeven door het ![pictogram Filter](media/ui-search/filter-icon.png "pictogram Filter") in de kolomkop.</span><span class="sxs-lookup"><span data-stu-id="30dc2-186">Columns that already have filters are indicated by the ![Filter icon](media/ui-search/filter-icon.png "Filter icon") in the column heading.</span></span> <span data-ttu-id="30dc2-187">Als u een filter wilt verwijderen, selecteert u de kolomkop en kiest u vervolgens **Filter wissen**.</span><span class="sxs-lookup"><span data-stu-id="30dc2-187">To remove a filter, select the column heading, then choose **Clear Filter**.</span></span>


### <a name="entering-filter-criteria-without-using-the-filter-pane"></a><span data-ttu-id="30dc2-188">Filtercriteria invoeren zonder het filterdeelvenster te gebruiken</span><span class="sxs-lookup"><span data-stu-id="30dc2-188">Entering Filter Criteria Without Using the Filter Pane</span></span>
<span data-ttu-id="30dc2-189">U kunt eenvoudige filters rechtstreeks in de lijst opgeven zonder het filterdeelvenster te hoeven gebruiken.</span><span class="sxs-lookup"><span data-stu-id="30dc2-189">You can specify simple filters directly within the list without having to use the filter pane.</span></span>
<span data-ttu-id="30dc2-190">Druk terwijl een veld in een rij is ingeschakeld op de toetsenbordsneltoets **Alt+F3** om alleen de records weer te geven die dezelfde waarde hebben.</span><span class="sxs-lookup"><span data-stu-id="30dc2-190">With any field selected on a row, use the **Alt+F3** keyboard shortcut to display only the records having that same value.</span></span> <span data-ttu-id="30dc2-191">U kunt een ander veld selecteren en dezelfde snelkoppeling opnieuw gebruiken om door te gaan met het verfijnen van uw filters.</span><span class="sxs-lookup"><span data-stu-id="30dc2-191">You can then select another field and use the same shortcut again to continue refining your filters.</span></span> <span data-ttu-id="30dc2-192">Als het geselecteerde veld al is gefilterd, wordt het filter met **Alt+F3** uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="30dc2-192">If the selected field is already filtered, using **Alt+F3** will clear that filter.</span></span>

> [!TIP]
> <span data-ttu-id="30dc2-193">Versnel het zoeken en analyseren van uw gegevens met combinaties van toetsenbordsneltoetsen.</span><span class="sxs-lookup"><span data-stu-id="30dc2-193">Accelerate finding and analyzing your data by using combinations of keyboard shortcuts.</span></span> <span data-ttu-id="30dc2-194">Selecteer bijvoorbeeld een veld, gebruik **Shift+Alt+F3** om dat veld aan het filterdeelvenster toe te voegen, typ het filtercriterium, gebruik **Ctrl+Enter** om terug te keren naar de rijen, selecteer een ander veld en gebruik **Alt+F3** om op die waarde te filteren.</span><span class="sxs-lookup"><span data-stu-id="30dc2-194">For example, select a field, use **Shift+Alt+F3** to add that field to the filter pane, type the filter criteria, use **Ctrl+Enter** to return to the rows, select another field, and use **Alt+F3** to filter to that value.</span></span>
<span data-ttu-id="30dc2-195">Zie voor meer informatie [Toetsenbordsneltoetsen](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="30dc2-195">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>


## <span data-ttu-id="30dc2-196"><a name="FilterCriteria"> </a>Filtercriteria en -symbolen</span><span class="sxs-lookup"><span data-stu-id="30dc2-196"><a name="FilterCriteria"> </a>Filter Criteria and Symbols</span></span>
<span data-ttu-id="30dc2-197">U kunt bij de invoer van criteria alle cijfers en letters gebruiken die u normaal ook kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="30dc2-197">When you enter criteria, you can use all the numbers and letters that you can normally use in the field.</span></span> <span data-ttu-id="30dc2-198">Daarnaast kunt u speciale symbolen (of operatoren) gebruiken om de resultaten verder te filteren.</span><span class="sxs-lookup"><span data-stu-id="30dc2-198">In addition, you can use special symbols (or operators) to further filter the results.</span></span> <span data-ttu-id="30dc2-199">De volgende tabellen bevatten de tekens die in filters kunnen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="30dc2-199">The following tables show the symbols which can be used in filters.</span></span> <span data-ttu-id="30dc2-200">Voor datums en tijden kunt u ook [Werken met kalenderdatums en -tijden](ui-enter-date-ranges.md) raadplegen voor meer gedetailleerde informatie.</span><span class="sxs-lookup"><span data-stu-id="30dc2-200">For dates and times, you can also refer to [Working with Calendar Dates and Times](ui-enter-date-ranges.md) for more detailed information.</span></span>

> [!IMPORTANT]  
>  <span data-ttu-id="30dc2-201">Het kan voorkomen dat veldwaarden deze symbolen bevatten en u hierop wilt filteren.</span><span class="sxs-lookup"><span data-stu-id="30dc2-201">There may be instances where field values contain these symbols and you want to filter on them.</span></span> <span data-ttu-id="30dc2-202">Hiervoor moet u de filterexpressie opnemen die het symbool tussen aanhalingstekens (“) bevat.</span><span class="sxs-lookup"><span data-stu-id="30dc2-202">To do this, you must include the filter expression that contains the symbol in quotation marks ('').</span></span> <span data-ttu-id="30dc2-203">Als u wilt filteren op records die beginnen met de tekst *S&R*, is de filterexpressie bijvoorbeeld `'S&R*'`.</span><span class="sxs-lookup"><span data-stu-id="30dc2-203">For example, if you want to filter on records that start with the text *S&R*, the filter expression is `'S&R*'`.</span></span>

<span data-ttu-id="30dc2-204">In de volgende secties wordt beschreven hoe u de verschillende operatoren kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="30dc2-204">The following sections describe how to use the different operators.</span></span>

> [!NOTE]
> <span data-ttu-id="30dc2-205">Als er meer dan 200 operatoren in één filter zijn, groepeert het systeem automatisch enkele uitdrukkingen tussen haakjes `()` met het oog op verwerking.</span><span class="sxs-lookup"><span data-stu-id="30dc2-205">If there are more than 200 operators in a single filter, the system will automatically group some expressions in parentheses `()` for the purpose of processing.</span></span> <span data-ttu-id="30dc2-206">Dit heeft geen effect op het filter of de resultaten.</span><span class="sxs-lookup"><span data-stu-id="30dc2-206">This has no effect on the filter or the results.</span></span>  

### <a name="-interval"></a><span data-ttu-id="30dc2-207">(..) Interval</span><span class="sxs-lookup"><span data-stu-id="30dc2-207">(..) Interval</span></span>

|<span data-ttu-id="30dc2-208">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="30dc2-208">Sample Expression</span></span>|<span data-ttu-id="30dc2-209">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="30dc2-209">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1100..2100`|<span data-ttu-id="30dc2-210">Nummers 1100 t/m 2100</span><span class="sxs-lookup"><span data-stu-id="30dc2-210">Numbers 1100 through 2100</span></span>|  
|`..2500`|<span data-ttu-id="30dc2-211">Tot en met 2500</span><span class="sxs-lookup"><span data-stu-id="30dc2-211">Up to and including 2500</span></span>|  
|`..12 31 00`|<span data-ttu-id="30dc2-212">Datums tot en met 31.12.00</span><span class="sxs-lookup"><span data-stu-id="30dc2-212">Dates up to and including 12 31 00</span></span>|  
|`P8..`|<span data-ttu-id="30dc2-213">Gegevens voor boekhoudperiode 8 en verder</span><span class="sxs-lookup"><span data-stu-id="30dc2-213">Information for accounting period 8 and thereafter</span></span>|  
|`..23`|<span data-ttu-id="30dc2-214">Van begindatum tot 23 lopende maand, lopend jaar 23:59:59</span><span class="sxs-lookup"><span data-stu-id="30dc2-214">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|`23..`|<span data-ttu-id="30dc2-215">Van 23 lopende maand, lopend jaar 00:00:00 tot eindtijd</span><span class="sxs-lookup"><span data-stu-id="30dc2-215">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|`22..23`|<span data-ttu-id="30dc2-216">Van 22 lopende maand, lopend jaar 0:00:00 tot 23 lopende maand, lopend jaar 23:59:59</span><span class="sxs-lookup"><span data-stu-id="30dc2-216">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  

### <a name="124-eitheror"></a><span data-ttu-id="30dc2-217">(&#124;) Of/of</span><span class="sxs-lookup"><span data-stu-id="30dc2-217">(&#124;) Either/or</span></span> 

|<span data-ttu-id="30dc2-218">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="30dc2-218">Sample Expression</span></span>|<span data-ttu-id="30dc2-219">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="30dc2-219">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1200|1300`|<span data-ttu-id="30dc2-220">Nummers met 1200 of 1300</span><span class="sxs-lookup"><span data-stu-id="30dc2-220">Numbers with 1200 or 1300</span></span>|  

### <a name="-not-equal-to"></a><span data-ttu-id="30dc2-221">(<>) Niet gelijk aan</span><span class="sxs-lookup"><span data-stu-id="30dc2-221">(<>) Not equal to</span></span>  

|<span data-ttu-id="30dc2-222">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="30dc2-222">Sample Expression</span></span>|<span data-ttu-id="30dc2-223">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="30dc2-223">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<>0`|<span data-ttu-id="30dc2-224">Alle nummers behalve 0</span><span class="sxs-lookup"><span data-stu-id="30dc2-224">All numbers except 0</span></span><br /><br /> <span data-ttu-id="30dc2-225">Met de SQL Server-optie kunt u dit teken combineren met jokertekens.</span><span class="sxs-lookup"><span data-stu-id="30dc2-225">The SQL Server Option allows you to combine this symbol with a wild card expression.</span></span> <span data-ttu-id="30dc2-226"><>A\* betekent bijvoorbeeld 'Niet gelijk aan tekst die begint met A'.</span><span class="sxs-lookup"><span data-stu-id="30dc2-226">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  

### <a name="-greater-than"></a><span data-ttu-id="30dc2-227">(>) Groter dan</span><span class="sxs-lookup"><span data-stu-id="30dc2-227">(>) Greater than</span></span>  

|<span data-ttu-id="30dc2-228">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="30dc2-228">Sample Expression</span></span>|<span data-ttu-id="30dc2-229">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="30dc2-229">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>1200`|<span data-ttu-id="30dc2-230">Nummers groter dan 1200</span><span class="sxs-lookup"><span data-stu-id="30dc2-230">Numbers greater than 1200</span></span>|  

### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="30dc2-231">(>=) Groter dan of gelijk aan</span><span class="sxs-lookup"><span data-stu-id="30dc2-231">(>=) Greater than or equal to</span></span>  

|<span data-ttu-id="30dc2-232">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="30dc2-232">Sample Expression</span></span>|<span data-ttu-id="30dc2-233">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="30dc2-233">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>=1200`|<span data-ttu-id="30dc2-234">Nummers groter dan of gelijk aan 1200</span><span class="sxs-lookup"><span data-stu-id="30dc2-234">Numbers greater than or equal to 1200</span></span>|  

### <a name="-less-than"></a><span data-ttu-id="30dc2-235">(<) Kleiner dan</span><span class="sxs-lookup"><span data-stu-id="30dc2-235">(<) Less than</span></span>  

|<span data-ttu-id="30dc2-236">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="30dc2-236">Sample Expression</span></span>|<span data-ttu-id="30dc2-237">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="30dc2-237">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<1200`|<span data-ttu-id="30dc2-238">Nummers kleiner dan 1200</span><span class="sxs-lookup"><span data-stu-id="30dc2-238">Numbers less than 1200</span></span>|  

### <a name="-less-than-or-equal-to"></a><span data-ttu-id="30dc2-239">(<=) Kleiner dan of gelijk aan</span><span class="sxs-lookup"><span data-stu-id="30dc2-239">(<=) Less than or equal to</span></span>  

|<span data-ttu-id="30dc2-240">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="30dc2-240">Sample Expression</span></span>|<span data-ttu-id="30dc2-241">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="30dc2-241">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<=1200`|<span data-ttu-id="30dc2-242">Nummers kleiner dan of gelijk aan 1200</span><span class="sxs-lookup"><span data-stu-id="30dc2-242">Numbers less than or equal to 1200</span></span>|  

### <a name="-and"></a><span data-ttu-id="30dc2-243">(&) En</span><span class="sxs-lookup"><span data-stu-id="30dc2-243">(&) And</span></span>  

|<span data-ttu-id="30dc2-244">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="30dc2-244">Sample Expression</span></span>|<span data-ttu-id="30dc2-245">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="30dc2-245">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>200&<1200`|<span data-ttu-id="30dc2-246">Getallen groter dan 200 en kleiner dan 1200</span><span class="sxs-lookup"><span data-stu-id="30dc2-246">Numbers greater than 200 and less than 1200</span></span>|  

### <a name="-an-exact-character-match"></a><span data-ttu-id="30dc2-247">('') Een exacte tekenovereenkomst</span><span class="sxs-lookup"><span data-stu-id="30dc2-247">('') An exact character match</span></span>  

|<span data-ttu-id="30dc2-248">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="30dc2-248">Sample Expression</span></span>|<span data-ttu-id="30dc2-249">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="30dc2-249">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`'man'`|<span data-ttu-id="30dc2-250">Tekst die exact overeenkomt met man en hoofdlettergevoelig is.</span><span class="sxs-lookup"><span data-stu-id="30dc2-250">Text that matches man exactly and is case sensitive.</span></span>|  

### <a name="-case-insensitive"></a><span data-ttu-id="30dc2-251">(@) Niet hoofdlettergevoelig</span><span class="sxs-lookup"><span data-stu-id="30dc2-251">(@) Case insensitive</span></span>  

|<span data-ttu-id="30dc2-252">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="30dc2-252">Sample Expression</span></span>|<span data-ttu-id="30dc2-253">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="30dc2-253">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`@man*`|<span data-ttu-id="30dc2-254">Tekst die begint met man en niet hoofdlettergevoelig is.</span><span class="sxs-lookup"><span data-stu-id="30dc2-254">Text that starts with man and is case insensitive.</span></span>|  

### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="30dc2-255">(\*) Een onbeperkt aantal onbekende tekens</span><span class="sxs-lookup"><span data-stu-id="30dc2-255">(\*) An indefinite number of unknown characters</span></span>

|<span data-ttu-id="30dc2-256">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="30dc2-256">Sample Expression</span></span>|<span data-ttu-id="30dc2-257">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="30dc2-257">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`*Co*`|<span data-ttu-id="30dc2-258">Tekst die “Co“ bevat en hoofdlettergevoelig is.</span><span class="sxs-lookup"><span data-stu-id="30dc2-258">Text that contains "Co" and is case sensitive.</span></span>|  
|`*Co`|<span data-ttu-id="30dc2-259">Tekst die eindigt met “Co“ en hoofdlettergevoelig is.</span><span class="sxs-lookup"><span data-stu-id="30dc2-259">Text that ends with "Co" and is case sensitive.</span></span>|  
|`Co*`|<span data-ttu-id="30dc2-260">Tekst die begint met “Co“ en hoofdlettergevoelig is.</span><span class="sxs-lookup"><span data-stu-id="30dc2-260">Text that begins with "Co" and is case sensitive.</span></span>|  

> [!NOTE]  
>   <span data-ttu-id="30dc2-261">U kunt `*` niet gebruiken wanneer u filtert op optievelden (opsommingen), zoals het veld **Status** in verkooporders.</span><span class="sxs-lookup"><span data-stu-id="30dc2-261">You cannot use `*` when filtering on option (enumeration) fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="30dc2-262">Om een filter voor deze veldsoort in te voeren, kunt u de numerieke waarde als een filterparameter invoeren.</span><span class="sxs-lookup"><span data-stu-id="30dc2-262">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="30dc2-263">In het veld **Status** in een verkooporder dat de waarden **Open**, **Vrijgegeven**, **Wacht op goedkeuring** en **Wacht op vooruitbetaling** heeft, gebruikt u de waarden `0`, `1`, `2` en `3` om te filteren op deze opties.</span><span class="sxs-lookup"><span data-stu-id="30dc2-263">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values `0`, `1`, `2`, and `3` to filter for these options.</span></span>

### <a name="-one-unknown-character"></a><span data-ttu-id="30dc2-264">(?) Een onbekend teken</span><span class="sxs-lookup"><span data-stu-id="30dc2-264">(?) One unknown character</span></span>  

|<span data-ttu-id="30dc2-265">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="30dc2-265">Sample Expression</span></span>|<span data-ttu-id="30dc2-266">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="30dc2-266">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`Hans?n`|<span data-ttu-id="30dc2-267">Tekst zoals Jansen of Jansma</span><span class="sxs-lookup"><span data-stu-id="30dc2-267">Text such as Hansen or Hanson</span></span>|  

### <a name="combined-format-expressions"></a><span data-ttu-id="30dc2-268">Gecombineerde notatiesoorten</span><span class="sxs-lookup"><span data-stu-id="30dc2-268">Combined Format Expressions</span></span>  

|<span data-ttu-id="30dc2-269">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="30dc2-269">Sample Expression</span></span>|<span data-ttu-id="30dc2-270">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="30dc2-270">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|<span data-ttu-id="30dc2-271">Alle records met het nummer 5999 of een nummer uit het interval 8100 tot en met 8490.</span><span class="sxs-lookup"><span data-stu-id="30dc2-271">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|`..1299|1400..`|<span data-ttu-id="30dc2-272">Records met een nummer kleiner dan of gelijk aan 1299 of gelijk aan 1400 en hoger. Met andere woorden: alle nummers behalve 1300 tot en met 1399.</span><span class="sxs-lookup"><span data-stu-id="30dc2-272">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|`>50&<100`|<span data-ttu-id="30dc2-273">Records met een nummer groter dan 50 en kleiner dan 100, ofwel nummer 51 tot en met 99.</span><span class="sxs-lookup"><span data-stu-id="30dc2-273">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  


## <span data-ttu-id="30dc2-274"><a name="FilterTokens"> </a>Filtertokens</span><span class="sxs-lookup"><span data-stu-id="30dc2-274"><a name="FilterTokens"> </a>Filter Tokens</span></span>
<span data-ttu-id="30dc2-275">Wanneer u filtercriteria invoert, kunt u ook woorden typen die een speciale betekenis hebben, filtertokens genaamd.</span><span class="sxs-lookup"><span data-stu-id="30dc2-275">When entering filter criteria, you can also type words that have special meaning, called filter tokens.</span></span> <span data-ttu-id="30dc2-276">Na het invoeren van het tokenwoord wordt het woord vervangen door de waarde of waarden die het woord vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="30dc2-276">After entering the token word, the word is replaced by the value or values that it represents.</span></span> <span data-ttu-id="30dc2-277">Dit maakt filtering eenvoudiger doordat u niet naar andere pagina's hoeft te navigeren om waarden op te zoeken die u aan uw filter wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="30dc2-277">This makes filtering easier by reducing the need to navigate to other pages to look up values you want to add to your filter.</span></span> <span data-ttu-id="30dc2-278">In de onderstaande tabellen worden enkele van de tokens beschreven die u als filtercriteria kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="30dc2-278">The tables below describe some of the tokens you can type as filter criteria.</span></span>

> [!TIP]
> <span data-ttu-id="30dc2-279">Uw organisatie kan aangepaste tokens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="30dc2-279">Your organization may use custom tokens.</span></span> <span data-ttu-id="30dc2-280">Als u informatie wilt over de volledige set tokens die voor u beschikbaar zijn of als u aangepaste tokens wilt toevoegen, overlegt u met uw beheerder.</span><span class="sxs-lookup"><span data-stu-id="30dc2-280">To learn about the complete set of tokens available to you or to add more custom tokens, talk to your administrator.</span></span> <span data-ttu-id="30dc2-281">Voor technische informatie raadpleegt u [Filtertokens toevoegen](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span><span class="sxs-lookup"><span data-stu-id="30dc2-281">For technical information see [Adding Filter Tokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span></span>


### <a name="me-or-userid-records-assigned-to-you"></a><span data-ttu-id="30dc2-282">(%me of %userid) Records die aan u zijn toegewezen</span><span class="sxs-lookup"><span data-stu-id="30dc2-282">(%me or %userid) Records Assigned to You</span></span>

<span data-ttu-id="30dc2-283">Gebruik `%me` of `%userid` wanneer u velden filtert die de gebruikers-id bevatten, zoals het veld **Toegewezen aan gebruikers-id**, om alle records weer te geven die aan u zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="30dc2-283">Use `%me` or `%userid` when filtering fields that contain the user ID, such as **Assigned to User ID** field, to display all records that are assigned to you.</span></span>

|<span data-ttu-id="30dc2-284">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="30dc2-284">Sample Expression</span></span>|<span data-ttu-id="30dc2-285">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="30dc2-285">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%me`<br /><span data-ttu-id="30dc2-286">of</span><span class="sxs-lookup"><span data-stu-id="30dc2-286">or</span></span><br />`%userid`|<span data-ttu-id="30dc2-287">Records die aan uw gebruikersaccount zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="30dc2-287">Records that are assigned to your user account.</span></span> |  

### <a name="mycustomers-customers-in-my-customers"></a><span data-ttu-id="30dc2-288">(%mycustomers) Klanten in Mijn klanten</span><span class="sxs-lookup"><span data-stu-id="30dc2-288">(%mycustomers) Customers in My Customers</span></span>

<span data-ttu-id="30dc2-289">Gebruik `%mycustomers` in het veld klant**nr.** om alle records weer te geven voor klanten die deel uitmaken van de lijst **Mijn klanten** in uw rolcentrum.</span><span class="sxs-lookup"><span data-stu-id="30dc2-289">Use `%mycustomers` in the customer **No** field to display all records for customers that are included in the **My Customers** list on your Role Center.</span></span>

|<span data-ttu-id="30dc2-290">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="30dc2-290">Sample Expression</span></span>|<span data-ttu-id="30dc2-291">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="30dc2-291">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%mycustomers`|<span data-ttu-id="30dc2-292">Klanten in **Mijn klanten** in uw rolcentrum.</span><span class="sxs-lookup"><span data-stu-id="30dc2-292">Customers in the **My Customers** on your Role Center.</span></span> |  

### <a name="myitems-items-in-my-items"></a><span data-ttu-id="30dc2-293">(%myitems) Artikelen in Mijn artikelen</span><span class="sxs-lookup"><span data-stu-id="30dc2-293">(%myitems) Items in My Items</span></span>

<span data-ttu-id="30dc2-294">Gebruik `%myitems` in het veld artikel**nr.** om alle records weer te geven voor artikelen die deel uitmaken van de lijst **Mijn artikelen** in uw rolcentrum.</span><span class="sxs-lookup"><span data-stu-id="30dc2-294">Use `%myitems` in the item **No** field to display all records for items that are included in the **My Items** list on your Role Center.</span></span>

|<span data-ttu-id="30dc2-295">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="30dc2-295">Sample Expression</span></span>|<span data-ttu-id="30dc2-296">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="30dc2-296">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myitems`|<span data-ttu-id="30dc2-297">Artikelen in **Mijn artikelen** in uw rolcentrum.</span><span class="sxs-lookup"><span data-stu-id="30dc2-297">Items in the **My Items** on your Role Center.</span></span> |  

### <a name="myvendors-vendors-in-my-vendors"></a><span data-ttu-id="30dc2-298">(%myvendors) Leveranciers in Mijn leveranciers</span><span class="sxs-lookup"><span data-stu-id="30dc2-298">(%myvendors) Vendors in My Vendors</span></span>

<span data-ttu-id="30dc2-299">Gebruik `%myvendors` in het veld leveranciers**nr.** om alle records weer te geven voor leveranciers die deel uitmaken van de lijst **Mijn leveranciers** in uw rolcentrum.</span><span class="sxs-lookup"><span data-stu-id="30dc2-299">Use `%myvendors` in the vendor **No** field to display all records for vendors that are included in the **My Vendors** list on your Role Center.</span></span>

|<span data-ttu-id="30dc2-300">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="30dc2-300">Sample Expression</span></span>|<span data-ttu-id="30dc2-301">Weergegeven records</span><span class="sxs-lookup"><span data-stu-id="30dc2-301">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myvendors`|<span data-ttu-id="30dc2-302">Leveranciers in **Mijn leveranciers** in uw rolcentrum.</span><span class="sxs-lookup"><span data-stu-id="30dc2-302">Vendors in the **My Vendors** on your Role Center.</span></span> |  


## <a name="see-also"></a><span data-ttu-id="30dc2-303">Zie ook</span><span class="sxs-lookup"><span data-stu-id="30dc2-303">See Also</span></span>
<span data-ttu-id="30dc2-304">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="30dc2-304">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="30dc2-305">Veelgestelde vragen over zoeken en filteren</span><span class="sxs-lookup"><span data-stu-id="30dc2-305">Common questions about Searching and Filtering</span></span>](ui-search-filter-faq.md)
