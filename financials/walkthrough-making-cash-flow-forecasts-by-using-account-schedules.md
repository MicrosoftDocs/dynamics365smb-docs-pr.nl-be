---
title: 'Procedure: Cashflowprognoses maken met behulp van rapportageschema''s | Microsoft Docs'
description: In dit scenario wordt beschreven hoe u rapportageschema's kunt maken maken van cashflowprognoses. Rapportageschema's voeren berekeningen uit die niet rechtstreeks in het schema met cashflowrekeningen kunnen worden uitgevoerd. In de rapportageschema's kunt u subtotalen voor cashflowontvangsten en -betalingen instellen. Deze subtotalen kunnen worden opgenomen in nieuwe totalen die vervolgens kunnen worden gebruikt bij het maken van cashflowprognoses.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 25319bae1d601d6beddca35cf8edc032ac11eda6
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="2f918-106">Procedure: cashflow met behulp van rapportageschema's maken</span><span class="sxs-lookup"><span data-stu-id="2f918-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="2f918-107">In dit scenario wordt beschreven hoe u rapportageschema's kunt maken maken van cashflowprognoses.</span><span class="sxs-lookup"><span data-stu-id="2f918-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="2f918-108">Rapportageschema's voeren berekeningen uit die niet rechtstreeks in het schema met cashflowrekeningen kunnen worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="2f918-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="2f918-109">In de rapportageschema's kunt u subtotalen voor cashflowontvangsten en -betalingen instellen.</span><span class="sxs-lookup"><span data-stu-id="2f918-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="2f918-110">Deze subtotalen kunnen worden opgenomen in nieuwe totalen die vervolgens kunnen worden gebruikt bij het maken van cashflowprognoses.</span><span class="sxs-lookup"><span data-stu-id="2f918-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="2f918-111">Informatie over deze procedure</span><span class="sxs-lookup"><span data-stu-id="2f918-111">About This Walkthrough</span></span>  
<span data-ttu-id="2f918-112">In deze procedure worden de volgende taken omschreven:</span><span class="sxs-lookup"><span data-stu-id="2f918-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="2f918-113">Een nieuwe naam voor een cashflowrekening instellen.</span><span class="sxs-lookup"><span data-stu-id="2f918-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="2f918-114">Nieuwe rapportageschemaregels instellen.</span><span class="sxs-lookup"><span data-stu-id="2f918-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="2f918-115">Een nieuwe kolomindeling instellen.</span><span class="sxs-lookup"><span data-stu-id="2f918-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="2f918-116">Een kolomindeling toewijzen aan een rapportageschema.</span><span class="sxs-lookup"><span data-stu-id="2f918-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="2f918-117">De cashflowprognose weergeven en afdrukken.</span><span class="sxs-lookup"><span data-stu-id="2f918-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="2f918-118">Vereisten</span><span class="sxs-lookup"><span data-stu-id="2f918-118">Prerequisites</span></span>  
<span data-ttu-id="2f918-119">U moet het volgende doen om deze procedure uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="2f918-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="2f918-120"> installeren.</span><span class="sxs-lookup"><span data-stu-id="2f918-120"> installed.</span></span>  
- <span data-ttu-id="2f918-121">De cashflowvoorstelregels worden geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="2f918-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="2f918-122">Rollen</span><span class="sxs-lookup"><span data-stu-id="2f918-122">Roles</span></span>  
<span data-ttu-id="2f918-123">In dit overzicht worden taken gedemonstreerd die worden uitgevoerd door de volgende gebruikersrol:</span><span class="sxs-lookup"><span data-stu-id="2f918-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="2f918-124">Controller</span><span class="sxs-lookup"><span data-stu-id="2f918-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="2f918-125">Scenario</span><span class="sxs-lookup"><span data-stu-id="2f918-125">Story</span></span>  
<span data-ttu-id="2f918-126">Ken is controller bij CRONUS en maakt de maandelijkse cashflowprognoses.</span><span class="sxs-lookup"><span data-stu-id="2f918-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="2f918-127">Hij neemt financiële gegevens, verkoop, inkoop en vaste activa op in de prognose en vervolgens presenteert hij deze aan CFO Sara voor het zakelijk perspectief.</span><span class="sxs-lookup"><span data-stu-id="2f918-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="2f918-128">Een nieuwe naam voor een rapportschema instellen.</span><span class="sxs-lookup"><span data-stu-id="2f918-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="2f918-129">Een rapportageschema bestaat uit een cashflowrekening met een reeks regels en een kolomindeling.</span><span class="sxs-lookup"><span data-stu-id="2f918-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="2f918-130">Een nieuwe naam voor een rekeningstelsel instellen</span><span class="sxs-lookup"><span data-stu-id="2f918-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="2f918-131">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rapportageschema's** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="2f918-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2f918-132">Kies in het venster **Rapportageschema's** de actie **Nieuw** om een nieuwe naam voor een cashflowrekening te maken.</span><span class="sxs-lookup"><span data-stu-id="2f918-132">In the **Account Schedule Names** window, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="2f918-133">Voer in het veld **Naam** de tekst **Prognose** in.</span><span class="sxs-lookup"><span data-stu-id="2f918-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="2f918-134">Voer in het veld **Omschrijving** **Cashflowprognose** in.</span><span class="sxs-lookup"><span data-stu-id="2f918-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="2f918-135">Laat de velden **Std. kolomindeling** en **Analyseweergavenaam** leeg.</span><span class="sxs-lookup"><span data-stu-id="2f918-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="2f918-136">Nieuwe rapportageschemaregels instellen.</span><span class="sxs-lookup"><span data-stu-id="2f918-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="2f918-137">Nadat een naam voor het rapportageschema is ingesteld, definieert Ken elke regel die in de cashflowrekening wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="2f918-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="2f918-138">Ken definieert de regels die kunnen worden weergegeven in rapporten en daarnaast extra regels die alleen voor het maken van berekeningen dienen.</span><span class="sxs-lookup"><span data-stu-id="2f918-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="2f918-139">Nieuwe rapportageschemaregels instellen</span><span class="sxs-lookup"><span data-stu-id="2f918-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="2f918-140">In het venster **Rapportageschema's** selecteert u de nieuwe naam voor het rapportageschema **Prognose** dat u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="2f918-140">In the **Account Schedule Names** window, select the new **Forecast** account schedule name that you have created.</span></span> <span data-ttu-id="2f918-141">Klik op het tabblad **Start** in de groep **Verwerken** op **Rekeningschema bewerken**.</span><span class="sxs-lookup"><span data-stu-id="2f918-141">On the **Home** tab, in the **Process** group, choose **Edit Account Schedule**.</span></span>  
2.  <span data-ttu-id="2f918-142">Voer in het venster **Rapportageschema** elke regel in zoals deze in de volgende tabel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="2f918-142">In the **Account Schedule** window, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="2f918-143">Met de functie **CF rekeningen invoegen** kunt u snel de cashflowrekeningen in het schema met cashflowrekeningen markeren en deze naar rapportageschemaregels kopiëren.</span><span class="sxs-lookup"><span data-stu-id="2f918-143">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    <span data-ttu-id="2f918-144">|Rijnr.|Beschrijving|Samentellingssoort|Samentelling|Rijsoort|Bedragsoort|Weergeven|</span><span class="sxs-lookup"><span data-stu-id="2f918-144">|Row No.|Description|Totaling Type|Totaling|Row Type|Amount Type|Show|</span></span>  
    <span data-ttu-id="2f918-145">|-------|-----------|-------------|--------|--------|---  ------|----| ||C10|Bedrag|Mutatie|Posten|Nettobedrag|Altijd|</span><span class="sxs-lookup"><span data-stu-id="2f918-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Amount|Net Change|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="2f918-146">|C20|Bedrag tot datum|Saldo t/m datum|Posten|Nettobedrag|Altijd|</span><span class="sxs-lookup"><span data-stu-id="2f918-146">|C20|Amount until Date|Balance at Date|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="2f918-147">|C30|Volledig boekjaar|Volledig boekjaar|Posten|Nettobedrag|Altijd|</span><span class="sxs-lookup"><span data-stu-id="2f918-147">|C30|Entire Fiscal Year|Entire Fiscal Year|Entries|Net Amount|Always|</span></span>  

4.  <span data-ttu-id="2f918-148">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f918-148">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="2f918-149">De kolomindeling toewijzen aan de naam van het rekeningstelsel</span><span class="sxs-lookup"><span data-stu-id="2f918-149">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="2f918-150">Ken kan nu de kolomindeling toewijzen aan de naam van het rapportageschema.</span><span class="sxs-lookup"><span data-stu-id="2f918-150">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="2f918-151">De kolomindeling toewijzen aan de naam van het rekeningstelsel</span><span class="sxs-lookup"><span data-stu-id="2f918-151">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="2f918-152">Selecteer in het venster **Rapportageschema's** in het veld **Naam** **Prognose**.</span><span class="sxs-lookup"><span data-stu-id="2f918-152">In the **Account Schedule Names** window, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="2f918-153">Kies in het veld **Std. kolomindeling** de kolomindeling **Cashflow** om deze toe te wijzen als de standaardkolomindeling.</span><span class="sxs-lookup"><span data-stu-id="2f918-153">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="2f918-154">De cashflowprognose weergeven en afdrukken</span><span class="sxs-lookup"><span data-stu-id="2f918-154">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="2f918-155">Kies in het venster **Rapportageschema's** de actie **Overzicht** om de cashflowprognose weer te geven.</span><span class="sxs-lookup"><span data-stu-id="2f918-155">In the **Account Schedule Names** window, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="2f918-156">In het venster **Rapportageschemaoverzicht** kunt u een bedrag selecteren en vervolgens de cashflowprognoseposten weergeven waaruit het bedrag bestaat.</span><span class="sxs-lookup"><span data-stu-id="2f918-156">In the **Acc. Schedule Overview** window, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="2f918-157">Bovendien kunt u de formule weergegeven die voor het berekenen van het bedrag wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="2f918-157">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="2f918-158">U kunt de bedragen ook filteren op datum en dimensie.</span><span class="sxs-lookup"><span data-stu-id="2f918-158">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="2f918-159">Kies de actie **Afdrukken** om de cashflowprognose af te drukken.</span><span class="sxs-lookup"><span data-stu-id="2f918-159">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2f918-160">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2f918-160">See Also</span></span>  
 <span data-ttu-id="2f918-161">[Werken met rekeningschema's](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="2f918-161">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="2f918-162">Procedures voor bedrijfsprocessen</span><span class="sxs-lookup"><span data-stu-id="2f918-162">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="2f918-163">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2f918-163">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

