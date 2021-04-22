---
title: Aangepaste Power BI-rapporten voor Business Central-gegevens weergeven | Microsoft Docs
description: U kunt Power BI-rapporten gebruiken om extra inzicht te krijgen in gegevens in lijsten.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: a600b24e16172134d4f8e78cf47efa4e262cac09
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777528"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a><span data-ttu-id="60652-103">Power BI-rapporten maken voor het weergeven van lijstgegevens in [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="60652-103">Creating Power BI Reports for Displaying List Data in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="60652-104">bevat een Power BI-feitenblokbesturingselement op veel belangrijke lijstpagina's.</span><span class="sxs-lookup"><span data-stu-id="60652-104">includes a Power BI FactBox control element on many key list pages.</span></span> <span data-ttu-id="60652-105">Het doel van dit feitenblok is om Power BI-rapporten weer te geven die betrekking hebben op records in de lijsten, waardoor extra inzicht in de gegevens ontstaat.</span><span class="sxs-lookup"><span data-stu-id="60652-105">The purpose of this FactBox is to display Power BI reports that are related to records in the lists, providing extra insight into the data.</span></span> <span data-ttu-id="60652-106">Het idee is dat terwijl u van de ene naar de andere rij gaat, het rapport wordt bijgewerkt en gefilterd op de geselecteerde vermelding.</span><span class="sxs-lookup"><span data-stu-id="60652-106">The idea is that as you move between rows in the list, the report is updated and filtered for the selected entry.</span></span>

[!INCLUDE[prod_long](includes/prod_long.md)] <span data-ttu-id="60652-107">wordt geleverd met enkele van deze rapporten.</span><span class="sxs-lookup"><span data-stu-id="60652-107">comes ready with some of these reports.</span></span> <span data-ttu-id="60652-108">U kunt ook uw eigen aangepaste rapporten maken die in dit feitenblok worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="60652-108">You can also create your own custom reports that display in this FactBox.</span></span> <span data-ttu-id="60652-109">Het maken van deze rapporten is vergelijkbaar met andere rapporten.</span><span class="sxs-lookup"><span data-stu-id="60652-109">Creating these reports is similar to other reports.</span></span> <span data-ttu-id="60652-110">Maar er zijn een paar ontwerpregels die u moet volgen om ervoor te zorgen dat de rapporten worden weergegeven zoals verwacht.</span><span class="sxs-lookup"><span data-stu-id="60652-110">But there are a few design rules you'll have to follow to make sure the reports display as expected.</span></span> <span data-ttu-id="60652-111">Deze regels worden in dit artikel uitgelegd.</span><span class="sxs-lookup"><span data-stu-id="60652-111">These rules are explained in this article.</span></span>

> [!NOTE]
> <span data-ttu-id="60652-112">Voor algemene informatie over maken en publiceren van Power BI-rapporten voor Business Central raadpleegt u [Power BI-rapporten maken om [!INCLUDE [prod_long](includes/prod_long.md)]-gegevens](across-how-use-financials-data-source-powerbi.md) weer te geven.</span><span class="sxs-lookup"><span data-stu-id="60652-112">For general information about creating and publishing Power BI reports for Business Central, see [Building Power BI Reports to Display [!INCLUDE [prod_long](includes/prod_long.md)] Data](across-how-use-financials-data-source-powerbi.md).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="60652-113">Vereisten</span><span class="sxs-lookup"><span data-stu-id="60652-113">Prerequisites</span></span>

- <span data-ttu-id="60652-114">Een Power BI-account.</span><span class="sxs-lookup"><span data-stu-id="60652-114">A Power BI account.</span></span>
- <span data-ttu-id="60652-115">Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="60652-115">Power BI Desktop.</span></span>

<!-- 
For more information about getting started, see [Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).-->

## <a name="create-a-report-for-a-list-page"></a><span data-ttu-id="60652-116">Een rapport maken voor een lijstpagina</span><span class="sxs-lookup"><span data-stu-id="60652-116">Create a report for a list page</span></span>

1. <span data-ttu-id="60652-117">Start Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="60652-117">Start Power BI Desktop.</span></span>
2. <span data-ttu-id="60652-118">Selecteer **Gegevens verkrijgen** en begin met het kiezen van de gegevensbron voor het rapport.</span><span class="sxs-lookup"><span data-stu-id="60652-118">Select **Get Data**, and start choosing the data source for the report.</span></span>

    <span data-ttu-id="60652-119">In deze stap geeft u de Business Central-lijstpagina's op die de gegevens bevatten die u in het rapport wilt hebben.</span><span class="sxs-lookup"><span data-stu-id="60652-119">In this step, you specify the Business Central list pages that contain the data that you want in the report.</span></span> <span data-ttu-id="60652-120">Als u bijvoorbeeld een rapport wilt maken voor de lijst Verkoop, moet u ervoor zorgen dat de gegevensset informatie bevat die verband houdt met de verkoop.</span><span class="sxs-lookup"><span data-stu-id="60652-120">For example, to create a report for the Sales List, ensure the data set contains information related to sales.</span></span>

    <span data-ttu-id="60652-121">Volg de instructies voor meer informatie [[!INCLUDE[prod_short](includes/prod_short.md)] toevoegen als gegevensbron in Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).</span><span class="sxs-lookup"><span data-stu-id="60652-121">For more information, follow the instructions [Add [!INCLUDE[prod_short](includes/prod_short.md)] as a data source in Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).</span></span>

3. <span data-ttu-id="60652-122">Stel het rapportfilter in.</span><span class="sxs-lookup"><span data-stu-id="60652-122">Set the report filter.</span></span>

    <span data-ttu-id="60652-123">Als u wilt dat de gegevens worden bijgewerkt op basis van de geselecteerde record in de lijst, voegt u een filter toe aan het rapport.</span><span class="sxs-lookup"><span data-stu-id="60652-123">To make the data update to the selected record in the list, you add a filter to the report.</span></span> <span data-ttu-id="60652-124">Het filter moet een veld van de gegevensbron bevatten dat wordt gebruikt om elke record in de lijst uniek te identificeren.</span><span class="sxs-lookup"><span data-stu-id="60652-124">The filter must include a field of the data source that's used to uniquely identify each record in the list.</span></span> <span data-ttu-id="60652-125">In termen van ontwikkelaars is dit veld de *primaire sleutel*.</span><span class="sxs-lookup"><span data-stu-id="60652-125">In developer terms, this field is the *primary key*.</span></span> <span data-ttu-id="60652-126">In de meeste gevallen is de primaire sleutel voor een lijst **Nr.**</span><span class="sxs-lookup"><span data-stu-id="60652-126">In most cases, the primary key for a list is the **No.**</span></span> <span data-ttu-id="60652-127">toevoegen.</span><span class="sxs-lookup"><span data-stu-id="60652-127">field.</span></span>

    <span data-ttu-id="60652-128">Voer de volgende stappen uit om het filter in te stellen:</span><span class="sxs-lookup"><span data-stu-id="60652-128">To set the filter, do the following steps:</span></span>

    1. <span data-ttu-id="60652-129">Selecteer bij **Filters** het primaire sleutelveld in de lijst met beschikbare velden.</span><span class="sxs-lookup"><span data-stu-id="60652-129">In the **Filters**, select the primary key field from the list of available fields.</span></span>
    2. <span data-ttu-id="60652-130">Sleep het veld naar het deelvenster **Filters** en zet het neer in het vak **Filters op alle pagina's**.</span><span class="sxs-lookup"><span data-stu-id="60652-130">Drag the field to **Filters** pane and drop it in the **Filters on all pages** box.</span></span>
    3. <span data-ttu-id="60652-131">Stel het **Filtertype** in op **Basisfiltering**.</span><span class="sxs-lookup"><span data-stu-id="60652-131">Set the **Filter type** to **Basic filtering**.</span></span> <span data-ttu-id="60652-132">Het kan geen pagina, visueel element of geavanceerd filter zijn.</span><span class="sxs-lookup"><span data-stu-id="60652-132">It can't be page, visual, or advanced filter.</span></span>

    ![Het rapportfilter instellen voor het rapport Verkoopfactuuractiviteit](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)
4. <span data-ttu-id="60652-134">Ontwerp de rapportlay-out.</span><span class="sxs-lookup"><span data-stu-id="60652-134">Design the report layout.</span></span>

    <span data-ttu-id="60652-135">Maak de lay-out door velden te slepen en visualisaties toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="60652-135">Create the layout by dragging fields and adding visualizations.</span></span> <span data-ttu-id="60652-136">Zie voor meer informatie [Werken met de rapportweergave in Power BI Desktop](/power-bi/create-reports/desktop-report-view) in de Power BI-documentatie.</span><span class="sxs-lookup"><span data-stu-id="60652-136">For more information, see, [Work with Report view in Power BI Desktop](/power-bi/create-reports/desktop-report-view) in the Power BI documentation.</span></span>

5. <span data-ttu-id="60652-137">Zie de volgende secties over het formaat van het rapport en het gebruik van meerdere pagina's.</span><span class="sxs-lookup"><span data-stu-id="60652-137">See the next sections about sizing the report and using multiple pages.</span></span>

6. <span data-ttu-id="60652-138">Sla het rapport op en geef het een naam.</span><span class="sxs-lookup"><span data-stu-id="60652-138">Save and name the report.</span></span>

    <span data-ttu-id="60652-139">Het is belangrijk het rapport een naam te geven die de naam bevat van de lijstpagina die aan het rapport is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="60652-139">It's important to give the report a name that contains the name of the list page associated with the report.</span></span> <span data-ttu-id="60652-140">Is het rapport bijvoorbeeld gemaakt voor de lijstpagina **Artikelen**, neem dan het woord *artikelen* op in de naam.</span><span class="sxs-lookup"><span data-stu-id="60652-140">For example, if the report is for the **Items** list page, include the word *items* somewhere in the name.</span></span>  

    <span data-ttu-id="60652-141">Deze naamgevingsconventie is geen vereiste.</span><span class="sxs-lookup"><span data-stu-id="60652-141">This naming convention isn't a requirement.</span></span> <span data-ttu-id="60652-142">Deze zorgt er echter wel voor dat gebruikers de gewenste rapporten sneller kunnen selecteren in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="60652-142">However, it makes selecting reports in [!INCLUDE[prod_short](includes/prod_short.md)] quicker.</span></span> <span data-ttu-id="60652-143">Wanneer de rapportselectiepagina wordt geopend vanuit een lijstpagina, wordt de lijst met rapporten automatisch gefilterd op basis van de paginanaam.</span><span class="sxs-lookup"><span data-stu-id="60652-143">When the report selection page opens from a list page, it's automatically filtered based on the page name.</span></span> <span data-ttu-id="60652-144">De rapporten worden gefilterd om het aantal weergegeven rapporten te beperken.</span><span class="sxs-lookup"><span data-stu-id="60652-144">This filtering is done to limit the reports that are displayed.</span></span> <span data-ttu-id="60652-145">Gebruikers kunnen het filter ook verwijderen als ze de volledige lijst met rapporten die beschikbaar zijn in Power BI, willen bekijken.</span><span class="sxs-lookup"><span data-stu-id="60652-145">Users can clear the filter to get a full list of reports available in Power BI.</span></span>

7. <span data-ttu-id="60652-146">Als u klaar bent, publiceert u het rapport zoals u gewend bent.</span><span class="sxs-lookup"><span data-stu-id="60652-146">When you're done, publish the report as usual.</span></span>

    <span data-ttu-id="60652-147">Zie voor meer informatie [Een rapport publiceren](across-how-use-financials-data-source-powerbi.md#publish-reports).</span><span class="sxs-lookup"><span data-stu-id="60652-147">For more information, see [Publishing a Report](across-how-use-financials-data-source-powerbi.md#publish-reports).</span></span>

8. <span data-ttu-id="60652-148">Test het rapport.</span><span class="sxs-lookup"><span data-stu-id="60652-148">Test the report.</span></span>

    <span data-ttu-id="60652-149">Zodra de rapporten naar uw werkruimte zijn gepubliceerd, zou het beschikbaar moeten zijn in het feitenblok Power BI op de lijstpagina in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="60652-149">Once the reports been published to your workspace, it should be available from the Power BI FactBox on the list page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

    <span data-ttu-id="60652-150">Voer de volgende stappen uit om het te testen.</span><span class="sxs-lookup"><span data-stu-id="60652-150">To test it, do the following steps.</span></span>

    1. <span data-ttu-id="60652-151">Open [!INCLUDE[prod_short](includes/prod_short.md)] en ga naar de lijstpagina.</span><span class="sxs-lookup"><span data-stu-id="60652-151">Open [!INCLUDE[prod_short](includes/prod_short.md)] and go to the list page.</span></span>
    2. <span data-ttu-id="60652-152">Als u het feitenblok Power BI niet ziet, gaat u naar de actiebalk en selecteert u **Acties** > **Weergeven** > **Power BI-rapporten weergeven/verbergen**.</span><span class="sxs-lookup"><span data-stu-id="60652-152">If you don't see the Power BI FactBox, go the action bar, then select **Actions** > **Display** > **Show/Hide Power BI Reports**.</span></span>
    3. <span data-ttu-id="60652-153">Selecteer in het feitenblok Power BI **Rapporten selecteren**, schakel het vakje **Inschakelen** voor het rapport in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="60652-153">In the Power BI FactBox, select **Select Reports**, select the **Enable** box for the report, then select **OK**.</span></span>

    <span data-ttu-id="60652-154">Als het correct is ontworpen, wordt het rapport weergegeven.</span><span class="sxs-lookup"><span data-stu-id="60652-154">If designed correctly, the report displays.</span></span>  

## <a name="set-the-report-size-and-color"></a><span data-ttu-id="60652-155">De rapportgrootte en kleur instellen</span><span class="sxs-lookup"><span data-stu-id="60652-155">Set the report size and color</span></span>

<span data-ttu-id="60652-156">De grootte van het rapport moet worden ingesteld op 325 bij 310 pixels.</span><span class="sxs-lookup"><span data-stu-id="60652-156">The size of the report must be set to 325 pixels by 310 pixels.</span></span> <span data-ttu-id="60652-157">Deze grootte is vereist voor een juiste schaling van het rapport in de beschikbare ruimte van het Power BI-besturingselement Feitenblok in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="60652-157">This size provides the proper scaling of the report in the available space of the Power BI FactBox control in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="60652-158">Als u de grootte van het rapport wilt definiëren, plaatst u de focus buiten het rapportlay-outgebied en kiest u vervolgens het pictogram met de verfroller.</span><span class="sxs-lookup"><span data-stu-id="60652-158">To define the size of the report, place focus outside of the report layout area, and then choose the paint roller icon.</span></span>

![De breedte en hoogte van het rapport instellen voor het rapport Verkoopfactuuractiviteit](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

<span data-ttu-id="60652-160">U kunt de breedte en hoogte van het rapport wijzigen door **Aangepast** in het veld **Soort** te kiezen.</span><span class="sxs-lookup"><span data-stu-id="60652-160">You can change the width and height of the report by choosing **Custom** in the **Type** field.</span></span>

<span data-ttu-id="60652-161">Als u wilt dat de achtergrond van het rapport wordt vermengd met de achtergrondkleur van het Power BI-feitenblokbesturingselement, stelt u de achtergrondkleur van het rapport in op *#FFFFFF* (wit).</span><span class="sxs-lookup"><span data-stu-id="60652-161">If you want the background of the report to blend with the background color of the Power BI FactBox control, set report background color to *#FFFFFF* (white).</span></span> 

> [!TIP]
> <span data-ttu-id="60652-162">Gebruik het [!INCLUDE [prod_short](includes/prod_short.md)]-themabestand om rapporten samen te stellen met dezelfde kleurstijlen als de [!INCLUDE [prod_short](includes/prod_short.md)]-apps.</span><span class="sxs-lookup"><span data-stu-id="60652-162">Use the [!INCLUDE [prod_short](includes/prod_short.md)] theme file to build reports with the same color styling as the [!INCLUDE [prod_short](includes/prod_short.md)] apps.</span></span> <span data-ttu-id="60652-163">Zie voor meer informatie [Het rapportthema [!INCLUDE [prod_short](includes/prod_short.md)] gebruiken](across-how-use-financials-data-source-powerbi.md#theme).</span><span class="sxs-lookup"><span data-stu-id="60652-163">For more information, see [Using the [!INCLUDE [prod_short](includes/prod_short.md)] report theme](across-how-use-financials-data-source-powerbi.md#theme).</span></span>

## <a name="reports-with-multiple-pages"></a><span data-ttu-id="60652-164">Rapporten met meerdere pagina's</span><span class="sxs-lookup"><span data-stu-id="60652-164">Reports with multiple pages</span></span>

<span data-ttu-id="60652-165">Met Power BI kunt u één rapport met meerdere pagina's maken.</span><span class="sxs-lookup"><span data-stu-id="60652-165">With Power BI, you can create a single report with multiple pages.</span></span> <span data-ttu-id="60652-166">Voor rapporten die worden weergegeven met lijstpagina's, raden we echter af om meer dan één pagina te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="60652-166">However, for reports that will display with list pages, we don't recommend that they have more than one page.</span></span> <span data-ttu-id="60652-167">In het Power BI-besturingselement Feitenblok wordt alleen de eerste pagina van uw rapport weergegeven.</span><span class="sxs-lookup"><span data-stu-id="60652-167">The Power BI FactBox will only show the first page of your report.</span></span>

## <a name="fixing-problems"></a><span data-ttu-id="60652-168">Problemen oplossen</span><span class="sxs-lookup"><span data-stu-id="60652-168">Fixing problems</span></span>

<span data-ttu-id="60652-169">In dit gedeelte vindt u instructies voor het oplossen van problemen die u kunt tegenkomen wanneer u een Power BI-rapport voor een lijstpagina in [!INCLUDE[prod_short](includes/prod_short.md)] probeert weer te geven.</span><span class="sxs-lookup"><span data-stu-id="60652-169">This section provides instructions about how to fix problems that you might run into when trying to view a Power BI report for a list page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

### <a name="you-cant-see-the-power-bi-factbox-on-a-list-page"></a><span data-ttu-id="60652-170">U kunt het feitenblok Power BI niet zien op een lijstpagina</span><span class="sxs-lookup"><span data-stu-id="60652-170">You can't see the Power BI FactBox on a list page</span></span>

<span data-ttu-id="60652-171">Standaard is het feitenblok Power BI verborgen.</span><span class="sxs-lookup"><span data-stu-id="60652-171">By default, the Power BI FactBox is hidden from view.</span></span> <span data-ttu-id="60652-172">Als u het feitenblok op een pagina wilt weergeven, selecteert u op de actiebalk **Acties** > **Weergeven** > **Power BI-rapporten weergeven/verbergen**.</span><span class="sxs-lookup"><span data-stu-id="60652-172">To show the FactBox on a page, from the action bar, select **Actions** > **Display** > **Show/Hide Power BI Reports**.</span></span>

### <a name="you-cant-see-the-report-in-the-select-report-pane"></a><span data-ttu-id="60652-173">U kunt het rapport niet zien in het deelvenster Rapport selecteren</span><span class="sxs-lookup"><span data-stu-id="60652-173">You can't see the report in the Select Report pane</span></span>

<span data-ttu-id="60652-174">Dit komt waarschijnlijk omdat de naam van het rapport niet de naam bevat van de lijstpagina die wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="60652-174">It's probably because the report's name doesn't contain the name of the list page that's being shown.</span></span> <span data-ttu-id="60652-175">Wis het filter om de volledige lijst met rapporten die beschikbaar zijn in Power BI, weer te geven.</span><span class="sxs-lookup"><span data-stu-id="60652-175">Clear the filter to get a full list of Power BI reports available.</span></span>  

### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a><span data-ttu-id="60652-176">Het rapport is geladen, maar is leeg, niet gefilterd of onjuist gefilterd</span><span class="sxs-lookup"><span data-stu-id="60652-176">Report is loaded but blank, not filtered, or filtered incorrectly</span></span>

<span data-ttu-id="60652-177">Controleer of het rapportfilter de juiste primaire sleutel bevat.</span><span class="sxs-lookup"><span data-stu-id="60652-177">Verify that the report filter contains the right primary key.</span></span> <span data-ttu-id="60652-178">In de meeste gevallen is dit het veld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="60652-178">In most cases, this field is the **No.**</span></span> <span data-ttu-id="60652-179">maar in de tabel **Grootboekpost** moet u bijvoorbeeld het veld **Postnr.** gebruiken.</span><span class="sxs-lookup"><span data-stu-id="60652-179">field, but in the **G/L Entry** table, for example, you must use the **Entry No.** field.</span></span>

### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a><span data-ttu-id="60652-180">Het rapport is geladen, maar er wordt een pagina weergegeven die u niet had verwacht</span><span class="sxs-lookup"><span data-stu-id="60652-180">Report is loaded, but it shows a page you didn't expect</span></span>

<span data-ttu-id="60652-181">Controleer of de pagina die u wilt weergeven, de eerste pagina in uw rapport is.</span><span class="sxs-lookup"><span data-stu-id="60652-181">Verify that the page you want displayed is the first page in your report.</span></span>  

### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a><span data-ttu-id="60652-182">Rapporten worden met ongewenste grijze randen weergegeven, zijn te klein of te groot</span><span class="sxs-lookup"><span data-stu-id="60652-182">Report appears with an unwanted gray boarder, or it's too small or too large</span></span>

<span data-ttu-id="60652-183">Controleer of de grootte van het rapport is ingesteld op 325 x 310 pixels.</span><span class="sxs-lookup"><span data-stu-id="60652-183">Verify that the report size is set to 325 pixels x 310 pixels.</span></span> <span data-ttu-id="60652-184">Sla het rapport op en vernieuw vervolgens de lijstpagina.</span><span class="sxs-lookup"><span data-stu-id="60652-184">Save the report, and then refresh the list page.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="60652-185">Zie Gerelateerde training op [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="60652-185">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="60652-186">Zie ook</span><span class="sxs-lookup"><span data-stu-id="60652-186">See Also</span></span>

[<span data-ttu-id="60652-187">Uw bedrijfsgegevens inschakelen voor Power BI</span><span class="sxs-lookup"><span data-stu-id="60652-187">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
<span data-ttu-id="60652-188">[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken als Power BI-gegevensbron](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="60652-188">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
[<span data-ttu-id="60652-189">Voorbereid zijn om zaken te doen</span><span class="sxs-lookup"><span data-stu-id="60652-189">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
<span data-ttu-id="60652-190">[Instellen van [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="60652-190">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
[<span data-ttu-id="60652-191">Financiën</span><span class="sxs-lookup"><span data-stu-id="60652-191">Finance</span></span>](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]