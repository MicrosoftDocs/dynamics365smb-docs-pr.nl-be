---
title: "Procedure: Cashflowprognoses maken met behulp van rapportageschema's | Microsoft Docs"
description: In dit scenario wordt beschreven hoe u rapportageschema's kunt maken maken van cashflowprognoses. Rapportageschema's voeren berekeningen uit die niet rechtstreeks in het schema met cashflowrekeningen kunnen worden uitgevoerd. In de rapportageschema's kunt u subtotalen voor cashflowontvangsten en -betalingen instellen. Deze subtotalen kunnen worden opgenomen in nieuwe totalen die vervolgens kunnen worden gebruikt bij het maken van cashflowprognoses.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 67a6e963800bf5f0ce8e1a293463d53b51470ee5
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3914797"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="639f7-106">Procedure: cashflow met behulp van rapportageschema's maken</span><span class="sxs-lookup"><span data-stu-id="639f7-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="639f7-107">In dit scenario wordt beschreven hoe u rapportageschema's kunt maken maken van cashflowprognoses.</span><span class="sxs-lookup"><span data-stu-id="639f7-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="639f7-108">Rapportageschema's voeren berekeningen uit die niet rechtstreeks in het schema met cashflowrekeningen kunnen worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="639f7-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="639f7-109">In de rapportageschema's kunt u subtotalen voor cashflowontvangsten en -betalingen instellen.</span><span class="sxs-lookup"><span data-stu-id="639f7-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="639f7-110">Deze subtotalen kunnen worden opgenomen in nieuwe totalen die vervolgens kunnen worden gebruikt bij het maken van cashflowprognoses.</span><span class="sxs-lookup"><span data-stu-id="639f7-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="639f7-111">Informatie over deze procedure</span><span class="sxs-lookup"><span data-stu-id="639f7-111">About This Walkthrough</span></span>  
<span data-ttu-id="639f7-112">In deze procedure worden de volgende taken omschreven:</span><span class="sxs-lookup"><span data-stu-id="639f7-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="639f7-113">Een nieuwe naam voor een cashflowrekening instellen.</span><span class="sxs-lookup"><span data-stu-id="639f7-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="639f7-114">Nieuwe rapportageschemaregels instellen.</span><span class="sxs-lookup"><span data-stu-id="639f7-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="639f7-115">Een nieuwe kolomindeling instellen.</span><span class="sxs-lookup"><span data-stu-id="639f7-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="639f7-116">Een kolomindeling toewijzen aan een rapportageschema.</span><span class="sxs-lookup"><span data-stu-id="639f7-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="639f7-117">De cashflowprognose weergeven en afdrukken.</span><span class="sxs-lookup"><span data-stu-id="639f7-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="639f7-118">Vereisten</span><span class="sxs-lookup"><span data-stu-id="639f7-118">Prerequisites</span></span>  
<span data-ttu-id="639f7-119">U moet het volgende doen om deze procedure uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="639f7-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="639f7-120">installeren.</span><span class="sxs-lookup"><span data-stu-id="639f7-120">installed.</span></span>  
- <span data-ttu-id="639f7-121">De cashflowvoorstelregels worden geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="639f7-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="639f7-122">Rollen</span><span class="sxs-lookup"><span data-stu-id="639f7-122">Roles</span></span>  
<span data-ttu-id="639f7-123">In dit overzicht worden taken gedemonstreerd die worden uitgevoerd door de volgende gebruikersrol:</span><span class="sxs-lookup"><span data-stu-id="639f7-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="639f7-124">Controller</span><span class="sxs-lookup"><span data-stu-id="639f7-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="639f7-125">Scenario</span><span class="sxs-lookup"><span data-stu-id="639f7-125">Story</span></span>  
<span data-ttu-id="639f7-126">Ken is controller bij CRONUS die de maandelijkse cashflowprognoses maakt.</span><span class="sxs-lookup"><span data-stu-id="639f7-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="639f7-127">Hij neemt financiële gegevens, verkoop, inkoop en vaste activa op in de prognose en vervolgens presenteert hij deze aan CFO Sara voor het zakelijk perspectief.</span><span class="sxs-lookup"><span data-stu-id="639f7-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="639f7-128">Een nieuwe naam voor een rapportschema instellen.</span><span class="sxs-lookup"><span data-stu-id="639f7-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="639f7-129">Een rapportageschema bestaat uit een cashflowrekening met een reeks regels en een kolomindeling.</span><span class="sxs-lookup"><span data-stu-id="639f7-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="639f7-130">Een nieuwe naam voor een rekeningstelsel instellen</span><span class="sxs-lookup"><span data-stu-id="639f7-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="639f7-131">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema's** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="639f7-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules** , and then choose the related link.</span></span>  
2.  <span data-ttu-id="639f7-132">Kies op de pagina **Rapportageschema's** de actie **Nieuw** om een nieuwe naam voor een cashflowrekening te maken.</span><span class="sxs-lookup"><span data-stu-id="639f7-132">On the **Account Schedule Names** page, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="639f7-133">Voer in het veld **Naam** de tekst **Prognose** in.</span><span class="sxs-lookup"><span data-stu-id="639f7-133">In the **Name** field, enter **Forecast** .</span></span>  
4.  <span data-ttu-id="639f7-134">Voer in het veld **Omschrijving** **Cashflowprognose** in.</span><span class="sxs-lookup"><span data-stu-id="639f7-134">In the **Description** field, enter **Cash Flow Forecast** .</span></span>  
5.  <span data-ttu-id="639f7-135">Laat de velden **Std. kolomindeling** en **Analyseweergavenaam** leeg.</span><span class="sxs-lookup"><span data-stu-id="639f7-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="639f7-136">Nieuwe rapportageschemaregels instellen.</span><span class="sxs-lookup"><span data-stu-id="639f7-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="639f7-137">Nadat een naam voor het rapportageschema is ingesteld, definieert Ken elke regel die in de cashflowrekening wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="639f7-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="639f7-138">Ken definieert de regels die kunnen worden weergegeven in rapporten en daarnaast extra regels die alleen voor het maken van berekeningen dienen.</span><span class="sxs-lookup"><span data-stu-id="639f7-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="639f7-139">Nieuwe rapportageschemaregels instellen</span><span class="sxs-lookup"><span data-stu-id="639f7-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="639f7-140">Selecteer op de pagina **Rapportageschema's** de naam van het nieuwe rapportageschema **Prognose** dat u hebt gemaakt en kies vervolgens de actie **Rapportageschema bewerken** .</span><span class="sxs-lookup"><span data-stu-id="639f7-140">On the **Account Schedule Names** page, select the new **Forecast** account schedule name that you have created, and then choose the **Edit Account Schedule** action.</span></span>  
2.  <span data-ttu-id="639f7-141">Voer op de pagina **Rapportageschema** elke regel in zoals deze in de volgende tabel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="639f7-141">On the **Account Schedule** page, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="639f7-142">Met de functie **CF rekeningen invoegen** kunt u snel de cashflowrekeningen in het schema met cashflowrekeningen markeren en deze naar rapportageschemaregels kopiëren.</span><span class="sxs-lookup"><span data-stu-id="639f7-142">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    |<span data-ttu-id="639f7-143">Rijnr.</span><span class="sxs-lookup"><span data-stu-id="639f7-143">Row No.</span></span>|<span data-ttu-id="639f7-144">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="639f7-144">Description</span></span>|<span data-ttu-id="639f7-145">Samentellingssoort</span><span class="sxs-lookup"><span data-stu-id="639f7-145">Totaling Type</span></span>|<span data-ttu-id="639f7-146">Samentelling</span><span class="sxs-lookup"><span data-stu-id="639f7-146">Totaling</span></span>|<span data-ttu-id="639f7-147">Rijsoort</span><span class="sxs-lookup"><span data-stu-id="639f7-147">Row Type</span></span>|<span data-ttu-id="639f7-148">Bedragsoort</span><span class="sxs-lookup"><span data-stu-id="639f7-148">Amount Type</span></span>|<span data-ttu-id="639f7-149">Weergeven</span><span class="sxs-lookup"><span data-stu-id="639f7-149">Show</span></span>|  
    |-------|-----------|-------------|--------|--------|-----------|----|
    |<span data-ttu-id="639f7-150">K10</span><span class="sxs-lookup"><span data-stu-id="639f7-150">C10</span></span>|<span data-ttu-id="639f7-151">Bedrag</span><span class="sxs-lookup"><span data-stu-id="639f7-151">Amount</span></span>|<span data-ttu-id="639f7-152">Mutatie</span><span class="sxs-lookup"><span data-stu-id="639f7-152">Net Change</span></span>|<span data-ttu-id="639f7-153">Posten</span><span class="sxs-lookup"><span data-stu-id="639f7-153">Entries</span></span>|<span data-ttu-id="639f7-154">Nettobedrag</span><span class="sxs-lookup"><span data-stu-id="639f7-154">Net Amount</span></span>|<span data-ttu-id="639f7-155">Altijd</span><span class="sxs-lookup"><span data-stu-id="639f7-155">Always</span></span>|  
    |<span data-ttu-id="639f7-156">K20</span><span class="sxs-lookup"><span data-stu-id="639f7-156">C20</span></span>|<span data-ttu-id="639f7-157">Bedrag tot datum</span><span class="sxs-lookup"><span data-stu-id="639f7-157">Amount until Date</span></span>|<span data-ttu-id="639f7-158">Saldo t/m datum</span><span class="sxs-lookup"><span data-stu-id="639f7-158">Balance at Date</span></span>|<span data-ttu-id="639f7-159">Posten</span><span class="sxs-lookup"><span data-stu-id="639f7-159">Entries</span></span>|<span data-ttu-id="639f7-160">Nettobedrag</span><span class="sxs-lookup"><span data-stu-id="639f7-160">Net Amount</span></span>|<span data-ttu-id="639f7-161">Altijd</span><span class="sxs-lookup"><span data-stu-id="639f7-161">Always</span></span>|  
    |<span data-ttu-id="639f7-162">K30</span><span class="sxs-lookup"><span data-stu-id="639f7-162">C30</span></span>|<span data-ttu-id="639f7-163">Volledig boekjaar</span><span class="sxs-lookup"><span data-stu-id="639f7-163">Entire Fiscal Year</span></span>|<span data-ttu-id="639f7-164">Volledig boekjaar</span><span class="sxs-lookup"><span data-stu-id="639f7-164">Entire Fiscal Year</span></span>|<span data-ttu-id="639f7-165">Posten</span><span class="sxs-lookup"><span data-stu-id="639f7-165">Entries</span></span>|<span data-ttu-id="639f7-166">Nettobedrag</span><span class="sxs-lookup"><span data-stu-id="639f7-166">Net Amount</span></span>|<span data-ttu-id="639f7-167">Altijd</span><span class="sxs-lookup"><span data-stu-id="639f7-167">Always</span></span>|  

4.  <span data-ttu-id="639f7-168">Kies de knop **Ok** .</span><span class="sxs-lookup"><span data-stu-id="639f7-168">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="639f7-169">De kolomindeling toewijzen aan de naam van het rekeningstelsel</span><span class="sxs-lookup"><span data-stu-id="639f7-169">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="639f7-170">Ken kan nu de kolomindeling toewijzen aan de naam van het rapportageschema.</span><span class="sxs-lookup"><span data-stu-id="639f7-170">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="639f7-171">De kolomindeling toewijzen aan de naam van het rekeningstelsel</span><span class="sxs-lookup"><span data-stu-id="639f7-171">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="639f7-172">Selecteer op de pagina **Rapportageschema's** in het veld **Naam** **Prognose** .</span><span class="sxs-lookup"><span data-stu-id="639f7-172">On the **Account Schedule Names** page, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="639f7-173">Kies in het veld **Std. kolomindeling** de kolomindeling **Cashflow** om deze toe te wijzen als de standaardkolomindeling.</span><span class="sxs-lookup"><span data-stu-id="639f7-173">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="639f7-174">De cashflowprognose weergeven en afdrukken</span><span class="sxs-lookup"><span data-stu-id="639f7-174">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="639f7-175">Kies op de pagina **Rapportageschema's** de actie **Overzicht** om de cashflowprognose weer te geven.</span><span class="sxs-lookup"><span data-stu-id="639f7-175">On the **Account Schedule Names** page, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="639f7-176">Op de pagina **Rapportageschemaoverzicht** kunt u een bedrag selecteren en vervolgens de cashflowprognoseposten weergeven waaruit het bedrag bestaat.</span><span class="sxs-lookup"><span data-stu-id="639f7-176">On the **Acc. Schedule Overview** page, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="639f7-177">Bovendien kunt u de formule weergegeven die voor het berekenen van het bedrag wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="639f7-177">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="639f7-178">U kunt de bedragen ook filteren op datum en dimensie.</span><span class="sxs-lookup"><span data-stu-id="639f7-178">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="639f7-179">Kies de actie **Afdrukken** om de cashflowprognose af te drukken.</span><span class="sxs-lookup"><span data-stu-id="639f7-179">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="639f7-180">Zie ook</span><span class="sxs-lookup"><span data-stu-id="639f7-180">See Also</span></span>  
 <span data-ttu-id="639f7-181">[Werken met rekeningschema's](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="639f7-181">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="639f7-182">Procedures voor bedrijfsprocessen</span><span class="sxs-lookup"><span data-stu-id="639f7-182">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="639f7-183">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="639f7-183">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
