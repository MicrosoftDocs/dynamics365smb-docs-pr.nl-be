---
title: "Procedure: Cashflowprognoses maken met behulp van rapportageschema's | Microsoft Docs"
description: In dit scenario wordt beschreven hoe u rapportageschema's kunt maken maken van cashflowprognoses. Rapportageschema's voeren berekeningen uit die niet rechtstreeks in het schema met cashflowrekeningen kunnen worden uitgevoerd. In de rapportageschema's kunt u subtotalen voor cashflowontvangsten en -betalingen instellen. Deze subtotalen kunnen worden opgenomen in nieuwe totalen die vervolgens kunnen worden gebruikt bij het maken van cashflowprognoses.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c09eedbb812df909a43e514dc462dcf8c1cf182a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "932635"
---
# <a name="walkthrough-making-cash-flow-forecasts-by-using-account-schedules"></a><span data-ttu-id="ad0b8-106">Procedure: cashflow met behulp van rapportageschema's maken</span><span class="sxs-lookup"><span data-stu-id="ad0b8-106">Walkthrough: Making Cash Flow Forecasts by Using Account Schedules</span></span>
<span data-ttu-id="ad0b8-107">In dit scenario wordt beschreven hoe u rapportageschema's kunt maken maken van cashflowprognoses.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-107">This walkthrough describes how you can use account schedules to make cash flow forecasts.</span></span> <span data-ttu-id="ad0b8-108">Rapportageschema's voeren berekeningen uit die niet rechtstreeks in het schema met cashflowrekeningen kunnen worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-108">Account schedules perform calculations that cannot be done directly in the chart of cash flow accounts.</span></span> <span data-ttu-id="ad0b8-109">In de rapportageschema's kunt u subtotalen voor cashflowontvangsten en -betalingen instellen.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-109">In the account schedules, you can set up subtotals for cash flow receipts and disbursements.</span></span> <span data-ttu-id="ad0b8-110">Deze subtotalen kunnen worden opgenomen in nieuwe totalen die vervolgens kunnen worden gebruikt bij het maken van cashflowprognoses.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-110">These subtotals can be included in new totals that can then be used in making cash flow forecasts.</span></span>  

## <a name="about-this-walkthrough"></a><span data-ttu-id="ad0b8-111">Informatie over deze procedure</span><span class="sxs-lookup"><span data-stu-id="ad0b8-111">About This Walkthrough</span></span>  
<span data-ttu-id="ad0b8-112">In deze procedure worden de volgende taken omschreven:</span><span class="sxs-lookup"><span data-stu-id="ad0b8-112">This walkthrough describes the following tasks:</span></span>  

- <span data-ttu-id="ad0b8-113">Een nieuwe naam voor een cashflowrekening instellen.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-113">Setting up a new cash flow account schedule name.</span></span>  
- <span data-ttu-id="ad0b8-114">Nieuwe rapportageschemaregels instellen.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-114">Setting up account schedule lines.</span></span>  
- <span data-ttu-id="ad0b8-115">Een nieuwe kolomindeling instellen.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-115">Setting up a new column layout.</span></span>  
- <span data-ttu-id="ad0b8-116">Een kolomindeling toewijzen aan een rapportageschema.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-116">Assigning a column layout to an account schedule.</span></span>  
- <span data-ttu-id="ad0b8-117">De cashflowprognose weergeven en afdrukken.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-117">Viewing and printing the cash flow forecast.</span></span>  

### <a name="prerequisites"></a><span data-ttu-id="ad0b8-118">Vereisten</span><span class="sxs-lookup"><span data-stu-id="ad0b8-118">Prerequisites</span></span>  
<span data-ttu-id="ad0b8-119">U moet het volgende doen om deze procedure uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="ad0b8-119">To complete this walkthrough, you will need:</span></span>  

- [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="ad0b8-120">installeren.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-120">installed.</span></span>  
- <span data-ttu-id="ad0b8-121">De cashflowvoorstelregels worden geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-121">The cash flow worksheet lines are registered.</span></span>  

## <a name="roles"></a><span data-ttu-id="ad0b8-122">Rollen</span><span class="sxs-lookup"><span data-stu-id="ad0b8-122">Roles</span></span>  
<span data-ttu-id="ad0b8-123">In dit overzicht worden taken gedemonstreerd die worden uitgevoerd door de volgende gebruikersrol:</span><span class="sxs-lookup"><span data-stu-id="ad0b8-123">This walkthrough demonstrates tasks that are performed by the following user role:</span></span>  

- <span data-ttu-id="ad0b8-124">Controller</span><span class="sxs-lookup"><span data-stu-id="ad0b8-124">Controller</span></span>  

## <a name="story"></a><span data-ttu-id="ad0b8-125">Scenario</span><span class="sxs-lookup"><span data-stu-id="ad0b8-125">Story</span></span>  
<span data-ttu-id="ad0b8-126">Ken is controller bij CRONUS die de maandelijkse cashflowprognoses maakt.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-126">Ken is a controller at CRONUS who makes monthly cash flow forecasts.</span></span> <span data-ttu-id="ad0b8-127">Hij neemt financiële gegevens, verkoop, inkoop en vaste activa op in de prognose en vervolgens presenteert hij deze aan CFO Sara voor het zakelijk perspectief.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-127">He includes finance, sales, purchase, and fixed assets in the forecast, and then he presents it to CFO Sara for business insight.</span></span>  

## <a name="setting-up-a-new-account-schedule-name"></a><span data-ttu-id="ad0b8-128">Een nieuwe naam voor een rapportschema instellen.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-128">Setting Up a New Account Schedule Name</span></span>  
<span data-ttu-id="ad0b8-129">Een rapportageschema bestaat uit een cashflowrekening met een reeks regels en een kolomindeling.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-129">An account schedule consists of a cash flow account schedule name with a series of lines and a column layout.</span></span>  

### <a name="to-set-up-a-new-account-schedule-name"></a><span data-ttu-id="ad0b8-130">Een nieuwe naam voor een rekeningstelsel instellen</span><span class="sxs-lookup"><span data-stu-id="ad0b8-130">To set up a new account schedule name</span></span>  

1.  <span data-ttu-id="ad0b8-131">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema's** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ad0b8-132">Kies op de pagina **Rapportageschema's** de actie **Nieuw** om een nieuwe naam voor een cashflowrekening te maken.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-132">On the **Account Schedule Names** page, choose the **New** to create a new cash flow account schedule name.</span></span>  
3.  <span data-ttu-id="ad0b8-133">Voer in het veld **Naam** de tekst **Prognose** in.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-133">In the **Name** field, enter **Forecast**.</span></span>  
4.  <span data-ttu-id="ad0b8-134">Voer in het veld **Omschrijving** **Cashflowprognose** in.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-134">In the **Description** field, enter **Cash Flow Forecast**.</span></span>  
5.  <span data-ttu-id="ad0b8-135">Laat de velden **Std. kolomindeling** en **Analyseweergavenaam** leeg.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-135">Leave the **Default Column Layout** and **Analysis View Name** fields blank.</span></span>  

## <a name="setting-up-account-schedule-lines"></a><span data-ttu-id="ad0b8-136">Nieuwe rapportageschemaregels instellen.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-136">Setting Up Account Schedule Lines</span></span>  
<span data-ttu-id="ad0b8-137">Nadat een naam voor het rapportageschema is ingesteld, definieert Ken elke regel die in de cashflowrekening wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-137">After an account schedule name is set up, Ken defines each line that appears in the cash flow account schedule.</span></span> <span data-ttu-id="ad0b8-138">Ken definieert de regels die kunnen worden weergegeven in rapporten en daarnaast extra regels die alleen voor het maken van berekeningen dienen.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-138">Ken defines lines that can be shown in reports in addition to lines that are only for calculation purposes.</span></span>  

### <a name="to-set-up-account-schedule-lines"></a><span data-ttu-id="ad0b8-139">Nieuwe rapportageschemaregels instellen</span><span class="sxs-lookup"><span data-stu-id="ad0b8-139">To set up account schedule lines</span></span>  

1.  <span data-ttu-id="ad0b8-140">Op de pagina **Rapportageschema's** selecteert u de nieuwe naam voor het rapportageschema **Prognose** dat u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-140">On the **Account Schedule Names** page, select the new **Forecast** account schedule name that you have created.</span></span> <span data-ttu-id="ad0b8-141">Klik op het tabblad **Start** in de groep **Verwerken** op **Rekeningschema bewerken**.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-141">On the **Home** tab, in the **Process** group, choose **Edit Account Schedule**.</span></span>  
2.  <span data-ttu-id="ad0b8-142">Voer op de pagina **Rapportageschema** elke regel in zoals deze in de volgende tabel wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-142">On the **Account Schedule** page, enter each line exactly as shown in the following table.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="ad0b8-143">Met de functie **CF rekeningen invoegen** kunt u snel de cashflowrekeningen in het schema met cashflowrekeningen markeren en deze naar rapportageschemaregels kopiëren.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-143">Using the **Insert CF Accounts** function, you can quickly mark the cash flow accounts from the chart of cash flow accounts and copy them to account schedule lines.</span></span>  

    <span data-ttu-id="ad0b8-144">|Rijnr.|Beschrijving|Samentellingssoort|Samentelling|Rijsoort|Bedragsoort|Weergeven|</span><span class="sxs-lookup"><span data-stu-id="ad0b8-144">|Row No.|Description|Totaling Type|Totaling|Row Type|Amount Type|Show|</span></span>  
    <span data-ttu-id="ad0b8-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Bedrag|Mutatie|Posten|Nettobedrag|Altijd|</span><span class="sxs-lookup"><span data-stu-id="ad0b8-145">|-------|-----------|-------------|--------|--------|---  ------|----| |C10|Amount|Net Change|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="ad0b8-146">|C20|Bedrag tot datum|Saldo t/m datum|Posten|Nettobedrag|Altijd|</span><span class="sxs-lookup"><span data-stu-id="ad0b8-146">|C20|Amount until Date|Balance at Date|Entries|Net Amount|Always|</span></span>  
    <span data-ttu-id="ad0b8-147">|C30|Volledig boekjaar|Volledig boekjaar|Posten|Nettobedrag|Altijd|</span><span class="sxs-lookup"><span data-stu-id="ad0b8-147">|C30|Entire Fiscal Year|Entire Fiscal Year|Entries|Net Amount|Always|</span></span>  

4.  <span data-ttu-id="ad0b8-148">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-148">Choose the **OK** button.</span></span>  

## <a name="assigning-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="ad0b8-149">De kolomindeling toewijzen aan de naam van het rekeningstelsel</span><span class="sxs-lookup"><span data-stu-id="ad0b8-149">Assigning the Column Layout to the Account Schedule Name</span></span>  
<span data-ttu-id="ad0b8-150">Ken kan nu de kolomindeling toewijzen aan de naam van het rapportageschema.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-150">Ken is now ready to assign the column layout to the account schedule name.</span></span>  

### <a name="to-assign-the-column-layout-to-the-account-schedule-name"></a><span data-ttu-id="ad0b8-151">De kolomindeling toewijzen aan de naam van het rekeningstelsel</span><span class="sxs-lookup"><span data-stu-id="ad0b8-151">To assign the column layout to the account schedule name</span></span>  

1.  <span data-ttu-id="ad0b8-152">Selecteer op de pagina **Rapportageschema's** in het veld **Naam** **Prognose**.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-152">On the **Account Schedule Names** page, select **Forecast** in the **Name** field.</span></span>  
2.  <span data-ttu-id="ad0b8-153">Kies in het veld **Std. kolomindeling** de kolomindeling **Cashflow** om deze toe te wijzen als de standaardkolomindeling.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-153">In the **Default Column Layout** field, choose the column layout **Cash Flow** to assign as the default column layout.</span></span>  

### <a name="to-view-and-print-the-cash-flow-forecast"></a><span data-ttu-id="ad0b8-154">De cashflowprognose weergeven en afdrukken</span><span class="sxs-lookup"><span data-stu-id="ad0b8-154">To view and print the cash flow forecast</span></span>  
1.  <span data-ttu-id="ad0b8-155">Kies op de pagina **Rapportageschema's** de actie **Overzicht** om de cashflowprognose weer te geven.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-155">On the **Account Schedule Names** page, choose the **Overview** action to view the cash flow forecast.</span></span>  
2.  <span data-ttu-id="ad0b8-156">Op de pagina **Rapportageschemaoverzicht** kunt u een bedrag selecteren en vervolgens de cashflowprognoseposten weergeven waaruit het bedrag bestaat.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-156">On the **Acc. Schedule Overview** page, you can select an amount and then view the cash flow forecast entries that make up the amount.</span></span> <span data-ttu-id="ad0b8-157">Bovendien kunt u de formule weergegeven die voor het berekenen van het bedrag wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-157">In addition, you can view the formula that is used to calculate the amount.</span></span> <span data-ttu-id="ad0b8-158">U kunt de bedragen ook filteren op datum en dimensie.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-158">You can also filter the amounts by date and dimension.</span></span>  
3.  <span data-ttu-id="ad0b8-159">Kies de actie **Afdrukken** om de cashflowprognose af te drukken.</span><span class="sxs-lookup"><span data-stu-id="ad0b8-159">Choose the **Print** action to print the cash flow forecast.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ad0b8-160">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ad0b8-160">See Also</span></span>  
 <span data-ttu-id="ad0b8-161">[Werken met rekeningschema's](bi-how-work-account-schedule.md) </span><span class="sxs-lookup"><span data-stu-id="ad0b8-161">[Work with Account Schedules](bi-how-work-account-schedule.md) </span></span>  
 [<span data-ttu-id="ad0b8-162">Procedures voor bedrijfsprocessen</span><span class="sxs-lookup"><span data-stu-id="ad0b8-162">Business Process Walkthroughs</span></span>](walkthrough-business-process-walkthroughs.md)  
 <span data-ttu-id="ad0b8-163">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ad0b8-163">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
