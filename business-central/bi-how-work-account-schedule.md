---
title: "Financiële rapporten maken met rapportageschema's"
description: "Beschrijft hoe u rapportageschema's gebruikt om diverse weergaven en lijsten te maken om financiële prestatiegegevens te analyseren."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/16/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: f9f5b3a25a24d4d10c80d048153e68030733bf9e
ms.contentlocale: nl-be
ms.lasthandoff: 04/18/2018

---
# <a name="work-with-account-schedules"></a><span data-ttu-id="371e7-103">Werken met rekeningschema's</span><span class="sxs-lookup"><span data-stu-id="371e7-103">Work with Account Schedules</span></span>
<span data-ttu-id="371e7-104">Gebruik rapportageschema's om inzicht te krijgen in de financiële gegevens die in uw rekeningschema zijn opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="371e7-104">Use account schedules to get insight into the financial data stored in your chart of accounts.</span></span> <span data-ttu-id="371e7-105">Met rapportageschema's worden cijfers geanalyseerd in grootboekrekeningen en worden grootboekposten vergeleken met budgetposten voor het grootboek.</span><span class="sxs-lookup"><span data-stu-id="371e7-105">Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="371e7-106">De resultaten worden weergegeven in diagrammen in uw rolcentrum, zoals het cashflowdiagram.</span><span class="sxs-lookup"><span data-stu-id="371e7-106">The results display in charts on your Role Center, such as the Cash Flow chart.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="371e7-107"> biedt een aantal voorbeeldrapportageschema's die u direct kunt gebruiken, of u kunt uw eigen rijen en kolommen instellen om de te vergelijken cijfers op te geven.</span><span class="sxs-lookup"><span data-stu-id="371e7-107"> provides a few sample account schedules that you can use right away, or you can set up your own rows and columns to specify the figures to compare.</span></span> <span data-ttu-id="371e7-108">U kunt bijvoorbeeld rapportageschema's maken om winstmarges te berekenen voor dimensies, zoals afdelingen of klantengroepen.</span><span class="sxs-lookup"><span data-stu-id="371e7-108">For example, you can create account schedules to calculate profit margins on dimensions like departments or customer groups.</span></span> <span data-ttu-id="371e7-109">U kunt zoveel aangepaste financiële overzichten maken als u wilt.</span><span class="sxs-lookup"><span data-stu-id="371e7-109">You can create as many customized financial statements as you want.</span></span>  

<span data-ttu-id="371e7-110">Het instellen van rapportageschema's vereist begrip van de financiële gegevens in het rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="371e7-110">Setting up account schedules requires an understanding of the financial data in the chart of accounts.</span></span> <span data-ttu-id="371e7-111">U kunt bijvoorbeeld grootboekposten weergeven als percentages van budgetposten.</span><span class="sxs-lookup"><span data-stu-id="371e7-111">For example, you can view general ledger entries as percentages of budget entries.</span></span> <span data-ttu-id="371e7-112">Hiertoe moeten budgetten worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="371e7-112">This requires that budgets are created.</span></span> <span data-ttu-id="371e7-113">Zie [Grootboekbudgetten maken](finance-how-create-budgets.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="371e7-113">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="account-categories-and-account-schedules"></a><span data-ttu-id="371e7-114">Rekeningcategorieën en rekeningschema's</span><span class="sxs-lookup"><span data-stu-id="371e7-114">Account Categories and Account Schedules</span></span>
<span data-ttu-id="371e7-115">U kunt rekeningcategorieën gebruiken om de indeling te wijzigen van uw financiële overzichten.</span><span class="sxs-lookup"><span data-stu-id="371e7-115">You can use account categories to change the layout of your financial statements.</span></span> <span data-ttu-id="371e7-116">Nadat u de rekeningcategorieën hebt ingesteld in het venster **GB-rekeningcategorieën** en u kiest de actie **Rapportageschema's genereren**, worden de onderliggende rapportageschema's voor de financiële kernrapporten bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="371e7-116">After you set up your account categories in the **G/L Account Categories** window, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated.</span></span> <span data-ttu-id="371e7-117">De volgende keer dat u een van deze rapporten uitvoert, zoals het saldo-overzicht, worden nieuwe totalen en subposten toegevoegd op basis van uw wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="371e7-117">The next time you run one of these reports, such as the balance statement, new totals and subentries are added, based on your changes.</span></span> <span data-ttu-id="371e7-118">Zie voor meer informatie [Het grootboek en het rekeningschema](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="371e7-118">For more information, see [The General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>  

## <a name="to-create-new-account-schedules"></a><span data-ttu-id="371e7-119">Nieuwe rekeningstelsels maken</span><span class="sxs-lookup"><span data-stu-id="371e7-119">To create new account schedules</span></span>  
 <span data-ttu-id="371e7-120">U kunt rekeningstelsels gebruiken om de cijfers in grootboekrekeningen te analyseren, of om grootboekposten te vergelijken met grootboekbegrotingsposten.</span><span class="sxs-lookup"><span data-stu-id="371e7-120">You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="371e7-121">U kunt bijvoorbeeld de grootboekposten weergeven als percentages van de begrotingsposten.</span><span class="sxs-lookup"><span data-stu-id="371e7-121">For example, you can view the general ledger entries as percentages of the budget entries.</span></span>

1. <span data-ttu-id="371e7-122">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rapportageschema's** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="371e7-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2. <span data-ttu-id="371e7-123">Kies in het venster **Rapportageschema's** de actie **Nieuw** om een nieuwe naam voor een rekeningschema te maken.</span><span class="sxs-lookup"><span data-stu-id="371e7-123">In the **Account Schedule Names** window, choose the **New** action to create a new account schedule name.</span></span>
3. <span data-ttu-id="371e7-124">Vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="371e7-124">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="371e7-125">Kies de actie **Rapportageschema bewerken**.</span><span class="sxs-lookup"><span data-stu-id="371e7-125">Choose the **Edit Account Schedule** action.</span></span>
5. <span data-ttu-id="371e7-126">Vul de benodigde velden in het venster **Rapportageschema** in.</span><span class="sxs-lookup"><span data-stu-id="371e7-126">In the **Account Schedule** window, fill in the fields as necessary.</span></span>  

    <span data-ttu-id="371e7-127">Nadat u een nieuw rapportageschema hebt gemaakt en de rijen hebt ingesteld, moet u kolommen instellen.</span><span class="sxs-lookup"><span data-stu-id="371e7-127">When you have created a new account schedule and set up the rows, you must set up columns.</span></span> <span data-ttu-id="371e7-128">U kunt de kolommen handmatig instellen of een vooraf gedefinieerde kolomindeling toewijzen aan het rapportageschema.</span><span class="sxs-lookup"><span data-stu-id="371e7-128">You can either set them up manually or assign a predefined column layout to your account schedule.</span></span>
6. <span data-ttu-id="371e7-129">Kies de actie **Instellingen kolomindeling bewerken**.</span><span class="sxs-lookup"><span data-stu-id="371e7-129">Choose the **Edit Column Layout Setup** action.</span></span>
7. <span data-ttu-id="371e7-130">Vul indien nodig in het venster **Kolomindeling** de velden in.</span><span class="sxs-lookup"><span data-stu-id="371e7-130">In the **Column Layout** window, fill in the fields as necessary.</span></span>

> [!NOTE]  
>   <span data-ttu-id="371e7-131">Als u geen standaardkolomindeling hebt toegewezen aan het rapportageschema, moet u de kolommen handmatig instellen.</span><span class="sxs-lookup"><span data-stu-id="371e7-131">If you did not assign a default column layout to the account schedule, you must set the columns up manually.</span></span>   

### <a name="to-create-a-column-that-calculates-percentages"></a><span data-ttu-id="371e7-132">Een kolom maken die percentages berekent</span><span class="sxs-lookup"><span data-stu-id="371e7-132">To create a column that calculates percentages</span></span>  
<span data-ttu-id="371e7-133">U wilt mogelijk soms een kolom opnemen in een rekeningschema om percentages van een totaal te berekenen.</span><span class="sxs-lookup"><span data-stu-id="371e7-133">Sometimes you may want to include a column in an account schedule to calculate percentages of a total.</span></span> <span data-ttu-id="371e7-134">U hebt bijvoorbeeld een aantal rijen die zijn onderverdeeld op dimensie, en u wilt wellicht een kolom maken om het percentage aan te geven van de totale verkoop van elke rij.</span><span class="sxs-lookup"><span data-stu-id="371e7-134">For example, if you have a number of rows that break down sales by dimension, you may want a column to indicate the percentage of total sales that each row represents.</span></span>

1. <span data-ttu-id="371e7-135">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rapportageschema's** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="371e7-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="371e7-136">Selecteer een rapportageschema in het venster **Rapportageschema's**.</span><span class="sxs-lookup"><span data-stu-id="371e7-136">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="371e7-137">Kies de actie **Rapportageschema bewerken** om een rapportageschemarij te definiëren die de totalen moet berekenen waarop de percentages worden gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="371e7-137">Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.</span></span>  
4. <span data-ttu-id="371e7-138">Voeg een regel in rechtstreeks boven de eerste rij waarvoor u een percentage wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="371e7-138">Insert a line immediately above the first row for which you want to display a percentage.</span></span>  
5. <span data-ttu-id="371e7-139">Vul de velden als volgt op de regel in: voer in het veld **Samentellingssoort** **Basis voor percentage** in.</span><span class="sxs-lookup"><span data-stu-id="371e7-139">Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**.</span></span> <span data-ttu-id="371e7-140">Voer in het veld **Samentelling** een formule in voor het totaal waarop het percentage wordt gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="371e7-140">In the **Totaling** field, enter a formula for the total that the percentage will be based on.</span></span> <span data-ttu-id="371e7-141">Als bijvoorbeeld rij 11 de totale omzet bevat, voert u **11** in.</span><span class="sxs-lookup"><span data-stu-id="371e7-141">For example, if row 11 contains the total sales, enter **11**.</span></span>  
6. <span data-ttu-id="371e7-142">Kies de actie **Instellingen kolomindeling bewerken** om een kolom in te stellen.</span><span class="sxs-lookup"><span data-stu-id="371e7-142">Choose the **Edit Column Layout Setup** action to set up a column.</span></span>  
7. <span data-ttu-id="371e7-143">Vul de velden als volgt op de regel in: selecteer in het veld **Kolomsoort** **Formule**.</span><span class="sxs-lookup"><span data-stu-id="371e7-143">Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**.</span></span> <span data-ttu-id="371e7-144">Voer in het veld **Formule** een formule in voor het bedrag waarvoor u een percentage wilt berekenen, gevolgd door %.</span><span class="sxs-lookup"><span data-stu-id="371e7-144">In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %.</span></span> <span data-ttu-id="371e7-145">Bijvoorbeeld, als kolomnummer N de mutatie bevat, voert u **N%** in.</span><span class="sxs-lookup"><span data-stu-id="371e7-145">For example, if column number N contains the net change, enter **N%**.</span></span>  
8. <span data-ttu-id="371e7-146">Herhaal stap 4 tot en met 7 voor elke groep rijen die u wilt uitsplitsen op percentage.</span><span class="sxs-lookup"><span data-stu-id="371e7-146">Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.</span></span>

## <a name="to-set-up-account-schedules-with-overviews"></a><span data-ttu-id="371e7-147">Rekeningstelsels met overzichten instellen</span><span class="sxs-lookup"><span data-stu-id="371e7-147">To set up account schedules with overviews</span></span>  
<span data-ttu-id="371e7-148">U kunt een rekeningstelsel gebruiken om een rekeningoverzicht te maken waarin grootboekcijfers en begrotingscijfers van grootboeken worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="371e7-148">You can use an account schedule to create a statement comparing general ledger figures and general leger budget figures.</span></span>

1. <span data-ttu-id="371e7-149">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rapportageschema's** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="371e7-149">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="371e7-150">Selecteer een rapportageschema in het venster **Rapportageschema's**.</span><span class="sxs-lookup"><span data-stu-id="371e7-150">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="371e7-151">Kies de actie **Rapportageschema bewerken**</span><span class="sxs-lookup"><span data-stu-id="371e7-151">Choose the **Edit Account Schedule** action</span></span>  
4. <span data-ttu-id="371e7-152">Selecteer in het venster **Rapportageschema** in het veld **Naam** de naam van het standaardrapportageschema.</span><span class="sxs-lookup"><span data-stu-id="371e7-152">In the **Account Schedule** window, in the **Name** field, select the default account schedule name.</span></span>
5. <span data-ttu-id="371e7-153">Kies de actie **Rekeningen invoegen**.</span><span class="sxs-lookup"><span data-stu-id="371e7-153">Choose the **Insert Accounts** action.</span></span>  
6. <span data-ttu-id="371e7-154">Selecteer de rekeningen die u wilt opnemen in uw overzicht en klik vervolgens op **OK**.</span><span class="sxs-lookup"><span data-stu-id="371e7-154">Select the accounts that you want to include in your statement, and then choose the **OK** button.</span></span>

    <span data-ttu-id="371e7-155">De rekeningen worden nu opgenomen in het rapportageschema.</span><span class="sxs-lookup"><span data-stu-id="371e7-155">The accounts are now inserted into your account schedule.</span></span> <span data-ttu-id="371e7-156">Indien gewenst kunt u ook de kolomindeling wijzigen.</span><span class="sxs-lookup"><span data-stu-id="371e7-156">If you want you can also change the column layout.</span></span>  
7. <span data-ttu-id="371e7-157">Kies de actie **Overzicht**.</span><span class="sxs-lookup"><span data-stu-id="371e7-157">Choose the **Overview** action.</span></span>  
8. <span data-ttu-id="371e7-158">Stel op het sneltabblad **Dimensiefilters** het begrotingsfilter in met de gewenste filternaam.</span><span class="sxs-lookup"><span data-stu-id="371e7-158">On the **Dimension Filters** FastTab, set the budget filter to the desired filter name.</span></span>  
9. <span data-ttu-id="371e7-159">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="371e7-159">Choose the **OK** button.</span></span>  

<span data-ttu-id="371e7-160">Nu kunt u het budgetoverzicht kopiëren en in een spreadsheet plakken.</span><span class="sxs-lookup"><span data-stu-id="371e7-160">Now you can copy and paste your budget statement into a spreadsheet.</span></span>  

## <a name="comparing-accounting-periods-using-period-formulas"></a><span data-ttu-id="371e7-161">Boekingsperioden vergelijken met behulp van periodeformules</span><span class="sxs-lookup"><span data-stu-id="371e7-161">Comparing Accounting Periods using Period Formulas</span></span>
<span data-ttu-id="371e7-162">Uw rapportageschema kan de resultaten vergelijken van verschillende boekingsperioden, zoals deze maand vergeleken met dezelfde maand vorig jaar.</span><span class="sxs-lookup"><span data-stu-id="371e7-162">Your account schedule can compare the results of different accounting periods, such as this month versus same month last year.</span></span> <span data-ttu-id="371e7-163">Daarvoor voegt u een kolom met het veld **Periodevergelijkingsformule** toe en stelt u dat veld in op een periodeformule.</span><span class="sxs-lookup"><span data-stu-id="371e7-163">To do that, you add a column with the **Comparison Period Formula** field, and then set that field to a period formula.</span></span>  

<span data-ttu-id="371e7-164">Een boekhoudperiode hoeft niet gelijk te zijn aan een agendaperiode, maar ieder boekjaar moet hetzelfde aantal boekhoudperioden hebben, zelfs wanneer de boekhoudperioden onderling in lengte verschillen.</span><span class="sxs-lookup"><span data-stu-id="371e7-164">An accounting period does not have to match the calendar, but each fiscal year must have the same number of accounting periods, even though each period can be different in length.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="371e7-165"> gebruikt de periodeformule om het bedrag uit de vergelijkingsperiode te berekenen in verhouding tot de periode die wordt voorgesteld door het datumfilter in de rapportaanvraag.</span><span class="sxs-lookup"><span data-stu-id="371e7-165"> uses the period formula to calculate the amount from the comparison period in relation to the period represented by the date filter on the report request.</span></span> <span data-ttu-id="371e7-166">De vergelijkingsperiode is gebaseerd op de begindatum van het datumfilter.</span><span class="sxs-lookup"><span data-stu-id="371e7-166">The comparison period is based on the period of the start date of the date filter.</span></span> <span data-ttu-id="371e7-167">Dit zijn de afkortingen voor periodenpecificaties:</span><span class="sxs-lookup"><span data-stu-id="371e7-167">The abbreviations for period specifications are:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="371e7-168">Afkorting</span><span class="sxs-lookup"><span data-stu-id="371e7-168">Abbreviation</span></span></th>
<th><span data-ttu-id="371e7-169">Description</span><span class="sxs-lookup"><span data-stu-id="371e7-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="371e7-170">P</span><span class="sxs-lookup"><span data-stu-id="371e7-170">P</span></span></p></td>
<td><p><span data-ttu-id="371e7-171">Periode</span><span class="sxs-lookup"><span data-stu-id="371e7-171">Period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="371e7-172">LP</span><span class="sxs-lookup"><span data-stu-id="371e7-172">LP</span></span></p></td>
<td><p><span data-ttu-id="371e7-173">Laatste periode van een boekjaar, half jaar of kwartaal.</span><span class="sxs-lookup"><span data-stu-id="371e7-173">Last period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="371e7-174">HP</span><span class="sxs-lookup"><span data-stu-id="371e7-174">CP</span></span></p></td>
<td><p><span data-ttu-id="371e7-175">Huidige periode van een boekjaar, half jaar of kwartaal.</span><span class="sxs-lookup"><span data-stu-id="371e7-175">Current period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="371e7-176">BJ</span><span class="sxs-lookup"><span data-stu-id="371e7-176">FY</span></span></p></td>
<td><p><span data-ttu-id="371e7-177">Boekjaar.</span><span class="sxs-lookup"><span data-stu-id="371e7-177">Fiscal year.</span></span> <span data-ttu-id="371e7-178">Met BJ[1..3] wordt bijvoorbeeld het eerste kwartaal van het huidige boekjaar aangeduid.</span><span class="sxs-lookup"><span data-stu-id="371e7-178">For example, FY[1..3] denotes first quarter of the current fiscal year</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="371e7-179">Voorbeelden van formules:</span><span class="sxs-lookup"><span data-stu-id="371e7-179">Examples of formulas:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="371e7-180">Formule</span><span class="sxs-lookup"><span data-stu-id="371e7-180">Formula</span></span></th>
<th><span data-ttu-id="371e7-181">Description</span><span class="sxs-lookup"><span data-stu-id="371e7-181">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="371e7-182">&lt;Leeg&gt;</span><span class="sxs-lookup"><span data-stu-id="371e7-182">&lt;Blank&gt;</span></span></p></td>
<td><p><span data-ttu-id="371e7-183">Huidige periode</span><span class="sxs-lookup"><span data-stu-id="371e7-183">Current period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="371e7-184">-1P</span><span class="sxs-lookup"><span data-stu-id="371e7-184">-1P</span></span></p></td>
<td><p><span data-ttu-id="371e7-185">Vorige periode</span><span class="sxs-lookup"><span data-stu-id="371e7-185">Previous period</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="371e7-186">-1BJ[1..LP]</span><span class="sxs-lookup"><span data-stu-id="371e7-186">-1FY[1..LP]</span></span></p></td>
<td><p><span data-ttu-id="371e7-187">Volledig vorig boekjaar</span><span class="sxs-lookup"><span data-stu-id="371e7-187">Entire previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="371e7-188">-1BJ</span><span class="sxs-lookup"><span data-stu-id="371e7-188">-1FY</span></span></p></td>
<td><p><span data-ttu-id="371e7-189">Huidige periode in vorig boekjaar</span><span class="sxs-lookup"><span data-stu-id="371e7-189">Current period in previous fiscal year</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="371e7-190">-1BJ[1..3]</span><span class="sxs-lookup"><span data-stu-id="371e7-190">-1FY[1..3]</span></span></p></td>
<td><p><span data-ttu-id="371e7-191">Eerste kwartaal van vorig boekjaar</span><span class="sxs-lookup"><span data-stu-id="371e7-191">First quarter of previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="371e7-192">-1BJ[1..HP]</span><span class="sxs-lookup"><span data-stu-id="371e7-192">-1FY[1..CP]</span></span></p></td>
<td><p><span data-ttu-id="371e7-193">Van het begin van het vorige boekjaar tot en met de huidige periode in het vorige boekjaar</span><span class="sxs-lookup"><span data-stu-id="371e7-193">From the beginning of previous fiscal year to current period in previous fiscal year, inclusive</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="371e7-194">-1BJ[HP..LP]</span><span class="sxs-lookup"><span data-stu-id="371e7-194">-1FY[CP..LP]</span></span></p></td>
<td><p><span data-ttu-id="371e7-195">Van de huidige periode in het vorige boekjaar tot en met de laatste periode van het vorige boekjaar</span><span class="sxs-lookup"><span data-stu-id="371e7-195">From current period in previous fiscal year to last period of previous fiscal year, inclusive</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="371e7-196">Als u de berekening volgens normale tijdsperioden wilt uitvoeren, moet u in plaats daarvan een formule in het veld **Datumvergelijkingsformule** invoeren.</span><span class="sxs-lookup"><span data-stu-id="371e7-196">If you want to calculate by regular time periods, you must enter a formula in the **Comparison Date Formula** field instead.</span></span>

> [!NOTE]
> <span data-ttu-id="371e7-197">Het is niet altijd transparant welke perioden u vergelijkt omdat u een datumfilter op een rapport kunt instellen dat andere datums omvat dan de boekingsperioden die worden gereflecteerd in de gegevens in het rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="371e7-197">It is not always transparent which periods you are comparing because you can set a date filter on a report that spans different dates than the accounting periods that are reflected in the data in the chart of accounts.</span></span> <span data-ttu-id="371e7-198">U maakt bijvoorbeeld een rapportageschema waarin u deze periode wilt vergelijken met dezelfde periode vorig jaar, dus u stelt het veld **Filter van vergelijkingsdatumperiode** in op *-1BJ*.</span><span class="sxs-lookup"><span data-stu-id="371e7-198">For example, you create an account schedule where you want to compare this period with the same period last year, so you set the **Comparison Date Period Filter** field to *-1FY*.</span></span> <span data-ttu-id="371e7-199">Vervolgens voert u het rapport uit op 28 februari en stelt u het datumfilter in op januari en februari.</span><span class="sxs-lookup"><span data-stu-id="371e7-199">Then, you run the report on February 28th and set the date filter to January and February.</span></span> <span data-ttu-id="371e7-200">Daardoor vergelijkt het rapportageschema januari en februari dit jaar met januari vorig jaar, wat de enige voltooide boekingsperiode van de twee voor vorig jaar is.</span><span class="sxs-lookup"><span data-stu-id="371e7-200">As a result, the account schedule compares January and February this year to January last year, which is the only completed accounting period of the two for last year.</span></span>  


## <a name="see-also"></a><span data-ttu-id="371e7-201">Zie ook</span><span class="sxs-lookup"><span data-stu-id="371e7-201">See Also</span></span>
[<span data-ttu-id="371e7-202">Bedrijfsinformatie</span><span class="sxs-lookup"><span data-stu-id="371e7-202">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="371e7-203">Financiën</span><span class="sxs-lookup"><span data-stu-id="371e7-203">Finance</span></span>](finance.md)  
[<span data-ttu-id="371e7-204">Financiën instellen</span><span class="sxs-lookup"><span data-stu-id="371e7-204">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="371e7-205">Het grootboek en het rekeningschema</span><span class="sxs-lookup"><span data-stu-id="371e7-205">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="371e7-206">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="371e7-206">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

