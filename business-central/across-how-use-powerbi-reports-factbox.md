---
title: Aangepaste Power BI-rapporten voor Business Central-gegevens weergeven | Microsoft Docs
description: U kunt Power BI-rapporten gebruiken om extra inzicht te krijgen in gegevens in lijsten.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 5d3acaf05952a61845eb8bb72b2556f2e54f8208
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697710"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prodshort"></a><span data-ttu-id="5ea8f-103">Power BI-rapporten maken voor het weergeven van lijstgegevens in [!INCLUDE[prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="5ea8f-103">Creating Power BI Reports for Displaying List Data in [!INCLUDE[prodshort](includes/prodshort.md)]</span></span>

<span data-ttu-id="5ea8f-104">In [!INCLUDE[prodlong](includes/prodlong.md)] is in een aantal belangrijke lijstpagina's het besturingselement Feitenblok opgenomen, waarmee lezers van het rapport extra inzicht kunnen krijgen in de gegevens in de lijst.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-104">[!INCLUDE[prodlong](includes/prodlong.md)] includes a FactBox control element on a number of key list pages that provide additional insight into the data in the list.</span></span> <span data-ttu-id="5ea8f-105">Wanneer u tussen rijen in de lijst verplaatst, wordt het rapport bijgewerkt en voor de geselecteerde post gefilterd.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-105">As you move between rows in the list, the report is updated and filtered for the selected entry.</span></span> <span data-ttu-id="5ea8f-106">U kunt aangepaste rapporten maken om in dit besturingselement weer te geven.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-106">You can create custom reports to display in this control.</span></span> <span data-ttu-id="5ea8f-107">Er zijn echter een paar regels die u moet volgen om ervoor te zorgen dat rapporten werken zoals verwacht.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-107">However, there are a few rules to follow to ensure that reports work as expected.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="5ea8f-108">Vereisten</span><span class="sxs-lookup"><span data-stu-id="5ea8f-108">Prerequisites</span></span>

- <span data-ttu-id="5ea8f-109">Een Power BI-account.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-109">A Power BI account.</span></span>
- <span data-ttu-id="5ea8f-110">Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-110">Power BI Desktop.</span></span>

<span data-ttu-id="5ea8f-111">Zie [[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken als Power BI-gegevensbron](across-how-use-financials-data-source-powerbi.md) voor meer informatie om aan de slag te gaan.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-111">For more information about getting started, see [Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).</span></span>

## <a name="defining-the-report-data-set"></a><span data-ttu-id="5ea8f-112">De rapportgegevensset definiëren</span><span class="sxs-lookup"><span data-stu-id="5ea8f-112">Defining the report data set</span></span>

<span data-ttu-id="5ea8f-113">Geef de gegevensbron op die de gegevens bevat die gerelateerd zijn aan de lijst.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-113">Specify the data source that contains the data related to the list.</span></span> <span data-ttu-id="5ea8f-114">Als u bijvoorbeeld een rapport wilt maken voor de lijst Verkoop, moet u ervoor zorgen dat de gegevensset informatie bevat die verband houdt met de verkoop.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-114">For example, to create a report for the Sales List, ensure the data set contains information related to sales.</span></span>  

## <a name="defining-the-report-filter"></a><span data-ttu-id="5ea8f-115">Het rapportfilter definiëren</span><span class="sxs-lookup"><span data-stu-id="5ea8f-115">Defining the report filter</span></span>

<span data-ttu-id="5ea8f-116">Als u wilt dat de gegevens worden bijgewerkt op basis van de geselecteerde record in de lijst, voegt u een filter toe aan het rapport.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-116">To make the data update to the selected record in the list, you add a filter to the report.</span></span> <span data-ttu-id="5ea8f-117">Het filter moet een veld bevatten van de gegevensbron die wordt gebruikt als *primaire sleutel*.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-117">The filter must include a field of the data source that's used as the *primary key*.</span></span> <span data-ttu-id="5ea8f-118">In de meeste gevallen is de primaire sleutel voor een lijst **Nr.**</span><span class="sxs-lookup"><span data-stu-id="5ea8f-118">In most cases, the primary key for a list is the **No.**</span></span> <span data-ttu-id="5ea8f-119">toevoegen.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-119">field.</span></span>

<span data-ttu-id="5ea8f-120">Als u een filter voor het rapport wilt definiëren, selecteert u de primaire sleutel in de lijst met beschikbare velden en sleept u dat veld vervolgens en zet u het neer in de sectie **Rapportfilter**.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-120">To define a filter for the report, select the primary key from the list of available fields, and then drag and drop that field into the **Report Filter** section.</span></span> <span data-ttu-id="5ea8f-121">Het filter moet een basisrapportfilter zijn.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-121">The filter must be basic report filter.</span></span> <span data-ttu-id="5ea8f-122">Het kan geen pagina, visueel element of geavanceerd filter zijn.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-122">It can't be page, visual, or advanced filter.</span></span> 

![Het rapportfilter instellen voor het rapport Verkoopfactuuractiviteit](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter.png)

## <a name="setting-the-report-size-and-color"></a><span data-ttu-id="5ea8f-124">De rapportgrootte en kleur instellen</span><span class="sxs-lookup"><span data-stu-id="5ea8f-124">Setting the report size and color</span></span>

<span data-ttu-id="5ea8f-125">De grootte van het rapport moet worden ingesteld op 325 bij 310 pixels.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-125">The size of the report must be set to 325 pixels by 310 pixels.</span></span> <span data-ttu-id="5ea8f-126">Deze grootte is vereist voor een juiste schaling van het rapport in de beschikbare ruimte van het Power BI-besturingselement Feitenblok in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5ea8f-126">This size provides the proper scaling of the report in the available space of the Power BI FactBox control in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="5ea8f-127">Als u de grootte van het rapport wilt definiëren, plaatst u de focus buiten het rapportlay-outgebied en kiest u vervolgens het pictogram met de verfroller.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-127">To define the size of the report, place focus outside of the report layout area, and then choose the paint roller icon.</span></span>

![De breedte en hoogte van het rapport instellen voor het rapport Verkoopfactuuractiviteit](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing.png)

<span data-ttu-id="5ea8f-129">U kunt de breedte en hoogte van het rapport wijzigen door **Aangepast** in het veld **Soort** te kiezen.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-129">You can change the width and height of the report by choosing **Custom** in the **Type** field.</span></span>

<span data-ttu-id="5ea8f-130">Als u wilt dat de achtergrond van het rapport wordt vermengd met de achtergrondkleur van het Power BI-besturingselement Feitenblok, stelt u de achtergrondkleur van het rapport in op *#FFFFFF*.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-130">If you want the background of the report to blend with the background color of the Power BI FactBox control, set report background color to *#FFFFFF*.</span></span> 

## <a name="using-reports-with-multiple-pages"></a><span data-ttu-id="5ea8f-131">Rapporten met meerdere pagina's gebruiken</span><span class="sxs-lookup"><span data-stu-id="5ea8f-131">Using reports with multiple pages</span></span>

<span data-ttu-id="5ea8f-132">Met Power BI kunt u één rapport met meerdere pagina's maken.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-132">With Power BI, you can create a single report with multiple pages.</span></span> <span data-ttu-id="5ea8f-133">Voor rapporten die worden weergegeven met lijstpagina's, raden we echter af om meer dan één pagina te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-133">However, for reports that will display with list pages, we don't recommend that they have more than one page.</span></span> <span data-ttu-id="5ea8f-134">In het Power BI-besturingselement Feitenblok wordt alleen de eerste pagina van uw rapport weergegeven.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-134">The Power BI FactBox will only show the first page of your report.</span></span>

## <a name="naming-the-report"></a><span data-ttu-id="5ea8f-135">Het rapport een naam geven</span><span class="sxs-lookup"><span data-stu-id="5ea8f-135">Naming the report</span></span>

<span data-ttu-id="5ea8f-136">Geef het rapport een naam die de naam bevat van de lijstpagina die aan het rapport is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-136">Give the report a name that contains the name of the list page associated with the report.</span></span> <span data-ttu-id="5ea8f-137">Is het rapport bijvoorbeeld gemaakt voor de lijstpagina **Verkoper**, neem dan het woord *verkoper* op in de naam.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-137">For example, if the report is for the **Vendor** list page, include the word *vendor* somewhere in the name.</span></span>  

<span data-ttu-id="5ea8f-138">Deze naamgevingsconventie is geen vereiste.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-138">This naming convention isn't a requirement.</span></span> <span data-ttu-id="5ea8f-139">Deze zorgt er echter wel voor dat gebruikers de gewenste rapporten sneller kunnen selecteren in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5ea8f-139">However, it makes selecting reports in [!INCLUDE[d365fin](includes/d365fin_md.md)] quicker.</span></span> <span data-ttu-id="5ea8f-140">Wanneer de rapportselectiepagina wordt geopend vanuit een lijstpagina, wordt de lijst met rapporten automatisch gefilterd op basis van de paginanaam.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-140">When the report selection page opens from a list page, it's automatically filtered based on the page name.</span></span> <span data-ttu-id="5ea8f-141">De rapporten worden gefilterd om het aantal weergegeven rapporten te beperken.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-141">This filtering is done to limit the reports that are displayed.</span></span> <span data-ttu-id="5ea8f-142">Gebruikers kunnen het filter ook verwijderen als ze de volledige lijst met rapporten die beschikbaar zijn in Power BI, willen bekijken.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-142">Users can clear the filter to get a full list of reports available in Power BI.</span></span>  

## <a name="fixing-problems"></a><span data-ttu-id="5ea8f-143">Problemen oplossen</span><span class="sxs-lookup"><span data-stu-id="5ea8f-143">Fixing problems</span></span>

<span data-ttu-id="5ea8f-144">Dit gedeelte bevat een tijdelijke oplossing voor de meest voorkomende problemen die zich kunnen voordoen wanneer u het Power BI-rapport maakt.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-144">This section provides a workaround for the most typical problems that can occur when you create the Power BI report.</span></span>  

#### <a name="you-cant-see-a-report-on-the-select-report-page"></a><span data-ttu-id="5ea8f-145">U ziet geen rapport op de pagina Rapport selecteren</span><span class="sxs-lookup"><span data-stu-id="5ea8f-145">You can't see a report on the Select Report page</span></span>

<span data-ttu-id="5ea8f-146">Dit komt waarschijnlijk omdat de naam van het rapport niet de naam van de lijstpagina bevat.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-146">It's probably because the report's name doesn't contain the name of the list page.</span></span> <span data-ttu-id="5ea8f-147">Wis het filter om de volledige lijst met rapporten die beschikbaar zijn in Power BI, weer te geven.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-147">Clear the filter to get a full list of Power BI reports available.</span></span>  

#### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a><span data-ttu-id="5ea8f-148">Het rapport is geladen, maar is leeg, niet gefilterd of onjuist gefilterd</span><span class="sxs-lookup"><span data-stu-id="5ea8f-148">Report is loaded but blank, not filtered or filtered incorrectly</span></span>

<span data-ttu-id="5ea8f-149">Controleer of het rapportfilter de juiste primaire sleutel bevat.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-149">Verify that the report filter contains the right primary key.</span></span> <span data-ttu-id="5ea8f-150">In de meeste gevallen is dit het veld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="5ea8f-150">In most cases, this field is the **No.**</span></span> <span data-ttu-id="5ea8f-151">maar in de tabel **Grootboekpost** moet u bijvoorbeeld het veld **Postnr.** gebruiken.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-151">field, but in the **G/L Entry** table, for example, you must use the **Entry No.** field.</span></span>

#### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a><span data-ttu-id="5ea8f-152">Het rapport is geladen, maar er wordt een pagina weergegeven die u niet had verwacht</span><span class="sxs-lookup"><span data-stu-id="5ea8f-152">Report is loaded, but it shows a page you didn't expect</span></span>

<span data-ttu-id="5ea8f-153">Controleer of de pagina die u wilt weergeven, de eerste pagina in uw rapport is.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-153">Verify that the page you want displayed is the first page in your report.</span></span>  

#### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a><span data-ttu-id="5ea8f-154">Rapporten worden met ongewenste grijze randen weergegeven, zijn te klein of te groot</span><span class="sxs-lookup"><span data-stu-id="5ea8f-154">Report appears with an unwanted gray boarder, or it's too small or too large</span></span>

<span data-ttu-id="5ea8f-155">Controleer of de grootte van het rapport is ingesteld op 325 x 310 pixels.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-155">Verify that the report size is set to 325 pixels x 310 pixels.</span></span> <span data-ttu-id="5ea8f-156">Sla het rapport op en vernieuw vervolgens de lijstpagina.</span><span class="sxs-lookup"><span data-stu-id="5ea8f-156">Save the report, and then refresh the list page.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="5ea8f-157">Zie Gerelateerde training op [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="5ea8f-157">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="5ea8f-158">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5ea8f-158">See Also</span></span>

[<span data-ttu-id="5ea8f-159">Uw bedrijfsgegevens inschakelen voor Power BI</span><span class="sxs-lookup"><span data-stu-id="5ea8f-159">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
<span data-ttu-id="5ea8f-160">[[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken als Power BI-gegevensbron](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="5ea8f-160">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
[<span data-ttu-id="5ea8f-161">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="5ea8f-161">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="5ea8f-162">[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="5ea8f-162">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="5ea8f-163">Financiën</span><span class="sxs-lookup"><span data-stu-id="5ea8f-163">Finance</span></span>](finance.md)  
