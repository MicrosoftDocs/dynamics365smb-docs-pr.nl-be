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
ms.date: 05/31/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e73c2dd0533aade4aa6225c9d2f385baaea3cfd1
ms.openlocfilehash: 69034b0eb97b595d0fbf5795e1fac34ecd775afe
ms.contentlocale: nl-be
ms.lasthandoff: 06/11/2018

---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a><span data-ttu-id="194f7-103">Financiële rapportage voorbereiden met rapportageschema's en rekeningcategorieën</span><span class="sxs-lookup"><span data-stu-id="194f7-103">Prepare Financial Reporting with Account Schedules and Account Categories</span></span>
<span data-ttu-id="194f7-104">Gebruik rapportageschema's om inzicht te krijgen in de financiële gegevens die in uw rekeningschema zijn opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="194f7-104">Use account schedules to get insight into the financial data stored in your chart of accounts.</span></span> <span data-ttu-id="194f7-105">Met rapportageschema's worden cijfers geanalyseerd in grootboekrekeningen en worden grootboekposten vergeleken met budgetposten voor het grootboek.</span><span class="sxs-lookup"><span data-stu-id="194f7-105">Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="194f7-106">De resultaten worden weergegeven in grafieken in uw rolcentrum, zoals het Cashflowdiagram, en in rapporten, zoals de Resultatenrekening en de Balans.</span><span class="sxs-lookup"><span data-stu-id="194f7-106">The results display in charts on your Role Center, such as the Cash Flow chart, and in reports, such as the Income Statement and the Balance Sheet reports.</span></span>

<span data-ttu-id="194f7-107">U opent deze twee rapporten, bijvoorbeeld, met de actie **Financiële afschriften** in de rolcentra Bedrijfsmanager en Accountant.</span><span class="sxs-lookup"><span data-stu-id="194f7-107">You access these two reports, for example, with the **Financials Statements** action on the Business Manager and Accountant Role Centers.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="194f7-108"> biedt een aantal voorbeeldrapportageschema's die u direct kunt gebruiken, of u kunt uw eigen rijen en kolommen instellen om de te vergelijken cijfers op te geven.</span><span class="sxs-lookup"><span data-stu-id="194f7-108"> provides a few sample account schedules that you can use right away, or you can set up your own rows and columns to specify the figures to compare.</span></span> <span data-ttu-id="194f7-109">U kunt bijvoorbeeld rapportageschema's maken om winstmarges te berekenen voor dimensies, zoals afdelingen of klantengroepen.</span><span class="sxs-lookup"><span data-stu-id="194f7-109">For example, you can create account schedules to calculate profit margins on dimensions like departments or customer groups.</span></span> <span data-ttu-id="194f7-110">U kunt zoveel aangepaste financiële overzichten maken als u wilt.</span><span class="sxs-lookup"><span data-stu-id="194f7-110">You can create as many customized financial statements as you want.</span></span>  

<span data-ttu-id="194f7-111">Het instellen van rapportageschema's vereist begrip van de financiële gegevens in het rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="194f7-111">Setting up account schedules requires an understanding of the financial data in the chart of accounts.</span></span> <span data-ttu-id="194f7-112">U kunt bijvoorbeeld grootboekposten weergeven als percentages van budgetposten.</span><span class="sxs-lookup"><span data-stu-id="194f7-112">For example, you can view general ledger entries as percentages of budget entries.</span></span> <span data-ttu-id="194f7-113">Hiertoe moeten budgetten worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="194f7-113">This requires that budgets are created.</span></span> <span data-ttu-id="194f7-114">Zie [Grootboekbudgetten maken](finance-how-create-budgets.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="194f7-114">For more information, see [Create G/L Budgets](finance-how-create-budgets.md).</span></span>

## <a name="account-categories-and-account-schedules"></a><span data-ttu-id="194f7-115">Rekeningcategorieën en rekeningschema's</span><span class="sxs-lookup"><span data-stu-id="194f7-115">Account Categories and Account Schedules</span></span>
<span data-ttu-id="194f7-116">U kunt rekeningcategorieën gebruiken om de indeling te wijzigen van uw financiële overzichten.</span><span class="sxs-lookup"><span data-stu-id="194f7-116">You can use account categories to change the layout of your financial statements.</span></span> <span data-ttu-id="194f7-117">Nadat u de rekeningcategorieën hebt ingesteld in het venster **GB-rekeningcategorieën** en u kiest de actie **Rapportageschema's genereren**, worden de onderliggende rapportageschema's voor de financiële kernrapporten bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="194f7-117">After you set up your account categories in the **G/L Account Categories** window, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated.</span></span> <span data-ttu-id="194f7-118">De volgende keer dat u een van deze rapporten uitvoert, zoals het rapport Balans, worden nieuwe totalen en subposten toegevoegd op basis van uw wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="194f7-118">The next time you run one of these reports, such as the Balance Statement report, new totals and subentries are added, based on your changes.</span></span> <span data-ttu-id="194f7-119">Zie voor meer informatie het gedeelte "Rekeningcategorieën" in [Het grootboek en COA begrijpen](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="194f7-119">For more information, see The "Account Categories" section in [Understanding the General Ledger and the COA](finance-general-ledger.md).</span></span>  

## <a name="to-create-new-account-schedules"></a><span data-ttu-id="194f7-120">Nieuwe rekeningstelsels maken</span><span class="sxs-lookup"><span data-stu-id="194f7-120">To create new account schedules</span></span>  
 <span data-ttu-id="194f7-121">U kunt rekeningstelsels gebruiken om de cijfers in grootboekrekeningen te analyseren, of om grootboekposten te vergelijken met grootboekbegrotingsposten.</span><span class="sxs-lookup"><span data-stu-id="194f7-121">You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries.</span></span> <span data-ttu-id="194f7-122">U kunt bijvoorbeeld de grootboekposten weergeven als percentages van de begrotingsposten.</span><span class="sxs-lookup"><span data-stu-id="194f7-122">For example, you can view the general ledger entries as percentages of the budget entries.</span></span>

1. <span data-ttu-id="194f7-123">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rapportageschema's** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="194f7-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2. <span data-ttu-id="194f7-124">Kies in het venster **Rapportageschema's** de actie **Nieuw** om een nieuwe naam voor een rekeningschema te maken.</span><span class="sxs-lookup"><span data-stu-id="194f7-124">In the **Account Schedule Names** window, choose the **New** action to create a new account schedule name.</span></span>
3. <span data-ttu-id="194f7-125">Vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="194f7-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="194f7-126">Kies de actie **Rapportageschema bewerken**.</span><span class="sxs-lookup"><span data-stu-id="194f7-126">Choose the **Edit Account Schedule** action.</span></span>
5. <span data-ttu-id="194f7-127">Vul de benodigde velden in het venster **Rapportageschema** in.</span><span class="sxs-lookup"><span data-stu-id="194f7-127">In the **Account Schedule** window, fill in the fields as necessary.</span></span>  

    <span data-ttu-id="194f7-128">Nadat u een nieuw rapportageschema hebt gemaakt en de rijen hebt ingesteld, moet u kolommen instellen.</span><span class="sxs-lookup"><span data-stu-id="194f7-128">When you have created a new account schedule and set up the rows, you must set up columns.</span></span> <span data-ttu-id="194f7-129">U kunt de kolommen handmatig instellen of een vooraf gedefinieerde kolomindeling toewijzen aan het rapportageschema.</span><span class="sxs-lookup"><span data-stu-id="194f7-129">You can either set them up manually or assign a predefined column layout to your account schedule.</span></span>
6. <span data-ttu-id="194f7-130">Kies de actie **Instellingen kolomindeling bewerken**.</span><span class="sxs-lookup"><span data-stu-id="194f7-130">Choose the **Edit Column Layout Setup** action.</span></span>
7. <span data-ttu-id="194f7-131">Vul indien nodig in het venster **Kolomindeling** de velden in.</span><span class="sxs-lookup"><span data-stu-id="194f7-131">In the **Column Layout** window, fill in the fields as necessary.</span></span>

> [!NOTE]  
> <span data-ttu-id="194f7-132">Als u geen standaardkolomindeling hebt toegewezen aan het rapportageschema, moet u de kolommen handmatig instellen.</span><span class="sxs-lookup"><span data-stu-id="194f7-132">If you did not assign a default column layout to the account schedule, you must set the columns up manually.</span></span>

### <a name="to-copy-an-existing-account-schedule"></a><span data-ttu-id="194f7-133">Een bestaand rekeningschema kopiëren</span><span class="sxs-lookup"><span data-stu-id="194f7-133">To copy an existing account schedule</span></span>
<span data-ttu-id="194f7-134">De rapportageschema's in de standaardversie van [!INCLUDE[d365fin](includes/d365fin_md.md)] zijn de basis van de financiële standaardrapporten, die mogelijk niet overeenkomen met de wensen van uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="194f7-134">The account schedules in the standard version of [!INCLUDE[d365fin](includes/d365fin_md.md)] are the basis of the standard financial reports, which may not suit the needs of your business.</span></span> <span data-ttu-id="194f7-135">Als u snel uw eigen financiële rapporten wilt maken, kunt u beginnen met een bestaand rapportageschema te kopiëren.</span><span class="sxs-lookup"><span data-stu-id="194f7-135">To quickly create your own financial reports, you can start by copying an existing account schedule.</span></span>
1. <span data-ttu-id="194f7-136">Selecteer in het venster **Rapportageschema** een rapportageschema en kies vervolgens de actie **Rapportageschema kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="194f7-136">In the **Account Schedules** window, select an account schedule, and then choose the **Copy Account Schedule** action.</span></span>
2. <span data-ttu-id="194f7-137">Vul in het venster **Rapportageschema kopiëren** de benodigde velden in en kies vervolgens de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="194f7-137">In the **Copy Account Schedule** window, fill in the fields as necessary, and then choose the **OK** button.</span></span>

### <a name="to-create-a-column-that-calculates-percentages"></a><span data-ttu-id="194f7-138">Een kolom maken die percentages berekent</span><span class="sxs-lookup"><span data-stu-id="194f7-138">To create a column that calculates percentages</span></span>  
<span data-ttu-id="194f7-139">U wilt mogelijk soms een kolom opnemen in een rekeningschema om percentages van een totaal te berekenen.</span><span class="sxs-lookup"><span data-stu-id="194f7-139">Sometimes you may want to include a column in an account schedule to calculate percentages of a total.</span></span> <span data-ttu-id="194f7-140">U hebt bijvoorbeeld een aantal rijen die zijn onderverdeeld op dimensie, en u wilt wellicht een kolom maken om het percentage aan te geven van de totale verkoop van elke rij.</span><span class="sxs-lookup"><span data-stu-id="194f7-140">For example, if you have a number of rows that break down sales by dimension, you may want a column to indicate the percentage of total sales that each row represents.</span></span>

1. <span data-ttu-id="194f7-141">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rapportageschema's** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="194f7-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="194f7-142">Selecteer een rapportageschema in het venster **Rapportageschema's**.</span><span class="sxs-lookup"><span data-stu-id="194f7-142">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="194f7-143">Kies de actie **Rapportageschema bewerken** om een rapportageschemarij te definiëren die de totalen moet berekenen waarop de percentages worden gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="194f7-143">Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.</span></span>  
4. <span data-ttu-id="194f7-144">Voeg een regel in rechtstreeks boven de eerste rij waarvoor u een percentage wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="194f7-144">Insert a line immediately above the first row for which you want to display a percentage.</span></span>  
5. <span data-ttu-id="194f7-145">Vul de velden als volgt op de regel in: voer in het veld **Samentellingssoort** **Basis voor percentage** in.</span><span class="sxs-lookup"><span data-stu-id="194f7-145">Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**.</span></span> <span data-ttu-id="194f7-146">Voer in het veld **Samentelling** een formule in voor het totaal waarop het percentage wordt gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="194f7-146">In the **Totaling** field, enter a formula for the total that the percentage will be based on.</span></span> <span data-ttu-id="194f7-147">Als bijvoorbeeld rij 11 de totale omzet bevat, voert u **11** in.</span><span class="sxs-lookup"><span data-stu-id="194f7-147">For example, if row 11 contains the total sales, enter **11**.</span></span>  
6. <span data-ttu-id="194f7-148">Kies de actie **Instellingen kolomindeling bewerken** om een kolom in te stellen.</span><span class="sxs-lookup"><span data-stu-id="194f7-148">Choose the **Edit Column Layout Setup** action to set up a column.</span></span>  
7. <span data-ttu-id="194f7-149">Vul de velden als volgt op de regel in: selecteer in het veld **Kolomsoort** **Formule**.</span><span class="sxs-lookup"><span data-stu-id="194f7-149">Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**.</span></span> <span data-ttu-id="194f7-150">Voer in het veld **Formule** een formule in voor het bedrag waarvoor u een percentage wilt berekenen, gevolgd door %.</span><span class="sxs-lookup"><span data-stu-id="194f7-150">In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %.</span></span> <span data-ttu-id="194f7-151">Bijvoorbeeld, als kolomnummer N de mutatie bevat, voert u **N%** in.</span><span class="sxs-lookup"><span data-stu-id="194f7-151">For example, if column number N contains the net change, enter **N%**.</span></span>  
8. <span data-ttu-id="194f7-152">Herhaal stap 4 tot en met 7 voor elke groep rijen die u wilt uitsplitsen op percentage.</span><span class="sxs-lookup"><span data-stu-id="194f7-152">Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.</span></span>

## <a name="to-set-up-account-schedules-with-overviews"></a><span data-ttu-id="194f7-153">Rekeningstelsels met overzichten instellen</span><span class="sxs-lookup"><span data-stu-id="194f7-153">To set up account schedules with overviews</span></span>  
<span data-ttu-id="194f7-154">U kunt een rekeningstelsel gebruiken om een rekeningoverzicht te maken waarin grootboekcijfers en begrotingscijfers van grootboeken worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="194f7-154">You can use an account schedule to create a statement comparing general ledger figures and general leger budget figures.</span></span>

1. <span data-ttu-id="194f7-155">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rapportageschema's** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="194f7-155">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>
2. <span data-ttu-id="194f7-156">Selecteer een rapportageschema in het venster **Rapportageschema's**.</span><span class="sxs-lookup"><span data-stu-id="194f7-156">In the **Account Schedule Names** window, select an account schedule.</span></span>  
3. <span data-ttu-id="194f7-157">Kies de actie **Rapportageschema bewerken**</span><span class="sxs-lookup"><span data-stu-id="194f7-157">Choose the **Edit Account Schedule** action</span></span>  
4. <span data-ttu-id="194f7-158">Selecteer in het venster **Rapportageschema** in het veld **Naam** de naam van het standaardrapportageschema.</span><span class="sxs-lookup"><span data-stu-id="194f7-158">In the **Account Schedule** window, in the **Name** field, select the default account schedule name.</span></span>
5. <span data-ttu-id="194f7-159">Kies de actie **Rekeningen invoegen**.</span><span class="sxs-lookup"><span data-stu-id="194f7-159">Choose the **Insert Accounts** action.</span></span>  
6. <span data-ttu-id="194f7-160">Selecteer de rekeningen die u wilt opnemen in uw overzicht en klik vervolgens op **OK**.</span><span class="sxs-lookup"><span data-stu-id="194f7-160">Select the accounts that you want to include in your statement, and then choose the **OK** button.</span></span>

    <span data-ttu-id="194f7-161">De rekeningen worden nu opgenomen in het rapportageschema.</span><span class="sxs-lookup"><span data-stu-id="194f7-161">The accounts are now inserted into your account schedule.</span></span> <span data-ttu-id="194f7-162">Indien gewenst kunt u ook de kolomindeling wijzigen.</span><span class="sxs-lookup"><span data-stu-id="194f7-162">If you want you can also change the column layout.</span></span>  
7. <span data-ttu-id="194f7-163">Kies de actie **Overzicht**.</span><span class="sxs-lookup"><span data-stu-id="194f7-163">Choose the **Overview** action.</span></span>  
8. <span data-ttu-id="194f7-164">Stel op het sneltabblad **Dimensiefilters** het begrotingsfilter in met de gewenste filternaam.</span><span class="sxs-lookup"><span data-stu-id="194f7-164">On the **Dimension Filters** FastTab, set the budget filter to the desired filter name.</span></span>  
9. <span data-ttu-id="194f7-165">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="194f7-165">Choose the **OK** button.</span></span>  

<span data-ttu-id="194f7-166">Nu kunt u het budgetoverzicht kopiëren en in een spreadsheet plakken.</span><span class="sxs-lookup"><span data-stu-id="194f7-166">Now you can copy and paste your budget statement into a spreadsheet.</span></span>  

## <a name="comparing-accounting-periods-using-period-formulas"></a><span data-ttu-id="194f7-167">Boekingsperioden vergelijken met behulp van periodeformules</span><span class="sxs-lookup"><span data-stu-id="194f7-167">Comparing Accounting Periods using Period Formulas</span></span>
<span data-ttu-id="194f7-168">Uw rapportageschema kan de resultaten vergelijken van verschillende boekingsperioden, zoals deze maand vergeleken met dezelfde maand vorig jaar.</span><span class="sxs-lookup"><span data-stu-id="194f7-168">Your account schedule can compare the results of different accounting periods, such as this month versus same month last year.</span></span> <span data-ttu-id="194f7-169">Daarvoor voegt u een kolom met het veld **Periodevergelijkingsformule** toe en stelt u dat veld in op een periodeformule.</span><span class="sxs-lookup"><span data-stu-id="194f7-169">To do that, you add a column with the **Comparison Period Formula** field, and then set that field to a period formula.</span></span>  

<span data-ttu-id="194f7-170">Een boekhoudperiode hoeft niet gelijk te zijn aan een agendaperiode, maar ieder boekjaar moet hetzelfde aantal boekhoudperioden hebben, zelfs wanneer de boekhoudperioden onderling in lengte verschillen.</span><span class="sxs-lookup"><span data-stu-id="194f7-170">An accounting period does not have to match the calendar, but each fiscal year must have the same number of accounting periods, even though each period can be different in length.</span></span>   

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="194f7-171"> gebruikt de periodeformule om het bedrag uit de vergelijkingsperiode te berekenen in verhouding tot de periode die wordt voorgesteld door het datumfilter in de rapportaanvraag.</span><span class="sxs-lookup"><span data-stu-id="194f7-171"> uses the period formula to calculate the amount from the comparison period in relation to the period represented by the date filter on the report request.</span></span> <span data-ttu-id="194f7-172">De vergelijkingsperiode is gebaseerd op de begindatum van het datumfilter.</span><span class="sxs-lookup"><span data-stu-id="194f7-172">The comparison period is based on the period of the start date of the date filter.</span></span> <span data-ttu-id="194f7-173">Dit zijn de afkortingen voor periodenpecificaties:</span><span class="sxs-lookup"><span data-stu-id="194f7-173">The abbreviations for period specifications are:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="194f7-174">Afkorting</span><span class="sxs-lookup"><span data-stu-id="194f7-174">Abbreviation</span></span></th>
<th><span data-ttu-id="194f7-175">Description</span><span class="sxs-lookup"><span data-stu-id="194f7-175">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="194f7-176">P</span><span class="sxs-lookup"><span data-stu-id="194f7-176">P</span></span></p></td>
<td><p><span data-ttu-id="194f7-177">Periode</span><span class="sxs-lookup"><span data-stu-id="194f7-177">Period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="194f7-178">LP</span><span class="sxs-lookup"><span data-stu-id="194f7-178">LP</span></span></p></td>
<td><p><span data-ttu-id="194f7-179">Laatste periode van een boekjaar, half jaar of kwartaal.</span><span class="sxs-lookup"><span data-stu-id="194f7-179">Last period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="194f7-180">HP</span><span class="sxs-lookup"><span data-stu-id="194f7-180">CP</span></span></p></td>
<td><p><span data-ttu-id="194f7-181">Huidige periode van een boekjaar, half jaar of kwartaal.</span><span class="sxs-lookup"><span data-stu-id="194f7-181">Current period of a fiscal year, half-year or quarter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="194f7-182">BJ</span><span class="sxs-lookup"><span data-stu-id="194f7-182">FY</span></span></p></td>
<td><p><span data-ttu-id="194f7-183">Boekjaar.</span><span class="sxs-lookup"><span data-stu-id="194f7-183">Fiscal year.</span></span> <span data-ttu-id="194f7-184">Met BJ[1..3] wordt bijvoorbeeld het eerste kwartaal van het huidige boekjaar aangeduid.</span><span class="sxs-lookup"><span data-stu-id="194f7-184">For example, FY[1..3] denotes first quarter of the current fiscal year</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="194f7-185">Voorbeelden van formules:</span><span class="sxs-lookup"><span data-stu-id="194f7-185">Examples of formulas:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="194f7-186">Formule</span><span class="sxs-lookup"><span data-stu-id="194f7-186">Formula</span></span></th>
<th><span data-ttu-id="194f7-187">Description</span><span class="sxs-lookup"><span data-stu-id="194f7-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="194f7-188">&lt;Leeg&gt;</span><span class="sxs-lookup"><span data-stu-id="194f7-188">&lt;Blank&gt;</span></span></p></td>
<td><p><span data-ttu-id="194f7-189">Huidige periode</span><span class="sxs-lookup"><span data-stu-id="194f7-189">Current period</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="194f7-190">-1P</span><span class="sxs-lookup"><span data-stu-id="194f7-190">-1P</span></span></p></td>
<td><p><span data-ttu-id="194f7-191">Vorige periode</span><span class="sxs-lookup"><span data-stu-id="194f7-191">Previous period</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="194f7-192">-1BJ[1..LP]</span><span class="sxs-lookup"><span data-stu-id="194f7-192">-1FY[1..LP]</span></span></p></td>
<td><p><span data-ttu-id="194f7-193">Volledig vorig boekjaar</span><span class="sxs-lookup"><span data-stu-id="194f7-193">Entire previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="194f7-194">-1BJ</span><span class="sxs-lookup"><span data-stu-id="194f7-194">-1FY</span></span></p></td>
<td><p><span data-ttu-id="194f7-195">Huidige periode in vorig boekjaar</span><span class="sxs-lookup"><span data-stu-id="194f7-195">Current period in previous fiscal year</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="194f7-196">-1BJ[1..3]</span><span class="sxs-lookup"><span data-stu-id="194f7-196">-1FY[1..3]</span></span></p></td>
<td><p><span data-ttu-id="194f7-197">Eerste kwartaal van vorig boekjaar</span><span class="sxs-lookup"><span data-stu-id="194f7-197">First quarter of previous fiscal year</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="194f7-198">-1BJ[1..HP]</span><span class="sxs-lookup"><span data-stu-id="194f7-198">-1FY[1..CP]</span></span></p></td>
<td><p><span data-ttu-id="194f7-199">Van het begin van het vorige boekjaar tot en met de huidige periode in het vorige boekjaar</span><span class="sxs-lookup"><span data-stu-id="194f7-199">From the beginning of previous fiscal year to current period in previous fiscal year, inclusive</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="194f7-200">-1BJ[HP..LP]</span><span class="sxs-lookup"><span data-stu-id="194f7-200">-1FY[CP..LP]</span></span></p></td>
<td><p><span data-ttu-id="194f7-201">Van de huidige periode in het vorige boekjaar tot en met de laatste periode van het vorige boekjaar</span><span class="sxs-lookup"><span data-stu-id="194f7-201">From current period in previous fiscal year to last period of previous fiscal year, inclusive</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="194f7-202">Als u de berekening volgens normale tijdsperioden wilt uitvoeren, moet u in plaats daarvan een formule in het veld **Datumvergelijkingsformule** invoeren.</span><span class="sxs-lookup"><span data-stu-id="194f7-202">If you want to calculate by regular time periods, you must enter a formula in the **Comparison Date Formula** field instead.</span></span>

> [!NOTE]
> <span data-ttu-id="194f7-203">Het is niet altijd transparant welke perioden u vergelijkt omdat u een datumfilter op een rapport kunt instellen dat andere datums omvat dan de boekingsperioden die worden gereflecteerd in de gegevens in het rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="194f7-203">It is not always transparent which periods you are comparing because you can set a date filter on a report that spans different dates than the accounting periods that are reflected in the data in the chart of accounts.</span></span> <span data-ttu-id="194f7-204">U maakt bijvoorbeeld een rapportageschema waarin u deze periode wilt vergelijken met dezelfde periode vorig jaar, dus u stelt het veld **Filter van vergelijkingsdatumperiode** in op *-1BJ*.</span><span class="sxs-lookup"><span data-stu-id="194f7-204">For example, you create an account schedule where you want to compare this period with the same period last year, so you set the **Comparison Date Period Filter** field to *-1FY*.</span></span> <span data-ttu-id="194f7-205">Vervolgens voert u het rapport uit op 28 februari en stelt u het datumfilter in op januari en februari.</span><span class="sxs-lookup"><span data-stu-id="194f7-205">Then, you run the report on February 28th and set the date filter to January and February.</span></span> <span data-ttu-id="194f7-206">Daardoor vergelijkt het rapportageschema januari en februari dit jaar met januari vorig jaar, wat de enige voltooide boekingsperiode van de twee voor vorig jaar is.</span><span class="sxs-lookup"><span data-stu-id="194f7-206">As a result, the account schedule compares January and February this year to January last year, which is the only completed accounting period of the two for last year.</span></span>  


## <a name="see-also"></a><span data-ttu-id="194f7-207">Zie ook</span><span class="sxs-lookup"><span data-stu-id="194f7-207">See Also</span></span>
[<span data-ttu-id="194f7-208">Bedrijfsinformatie</span><span class="sxs-lookup"><span data-stu-id="194f7-208">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="194f7-209">Financiën</span><span class="sxs-lookup"><span data-stu-id="194f7-209">Finance</span></span>](finance.md)  
[<span data-ttu-id="194f7-210">Financiën instellen</span><span class="sxs-lookup"><span data-stu-id="194f7-210">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="194f7-211">Het grootboek en het rekeningschema</span><span class="sxs-lookup"><span data-stu-id="194f7-211">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
<span data-ttu-id="194f7-212">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="194f7-212">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

