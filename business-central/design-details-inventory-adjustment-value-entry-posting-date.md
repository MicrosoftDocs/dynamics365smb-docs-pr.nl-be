---
title: Boekingsdatum in waardeposten
description: Leren hoe de batchverwerking Kostprijs herwaarderen - Artikelposten een boekingsdatum bepaalt en toewijst aan de waardeposten die de batchverwerking gaat maken.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 9d0a5ab6bebdc9723fe8e3621fdda3cb16d5e6e1
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a><span data-ttu-id="c8478-103">Ontwerpdetails: Boekingsdatum op herwaarderingswaardepost</span><span class="sxs-lookup"><span data-stu-id="c8478-103">Design Details: Posting Date on Adjustment Value Entry</span></span>
<span data-ttu-id="c8478-104">Dit artikel begeleidt gebruikers bij de functionaliteit Voorraadwaardering in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c8478-104">This article provides guidance for users of the Inventory Costing functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c8478-105">Het specifieke artikel legt uit hoe de batchverwerking **Kostprijs herwaarderen - Artikelposten** een boekingsdatum bepaalt en toewijst aan de waardeposten die de batchverwerking gaat maken.</span><span class="sxs-lookup"><span data-stu-id="c8478-105">The specific article is providing guidance in how the **Adjust Cost - Item Entries** batch job identifies and assigns a posting date to the value entries that the batch job is about to create.</span></span>  

<span data-ttu-id="c8478-106">Eerst wordt het concept van het proces bekeken, hoe de batchverwerking de boekingsdatum bepaalt en toewijst aan de waardepost die wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c8478-106">First the concept of the process is reviewed, how the batch job identifies and assigns the Posting Date to the Value Entry to be created.</span></span> <span data-ttu-id="c8478-107">Daarna zijn er enkele gedeelde scenario's die we in het ondersteuningsteam van tijd tot tijd tegenkomen en uiteindelijk is er een lijst met de begrippen die vanaf versie 3.0 worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c8478-107">Thereafter there are some scenarios shared that we in the support team come across from time to time and finally there is a summary of the concepts used from version 3.0.</span></span>  

## <a name="the-concept"></a><span data-ttu-id="c8478-108">Het concept</span><span class="sxs-lookup"><span data-stu-id="c8478-108">The Concept</span></span>  
<span data-ttu-id="c8478-109">Vanaf versie 5.0 wijst de batchverwerking **Kostprijs herwaarderen - Artikelposten** een boekingsdatum toe aan de waardepost die gaat worden gemaakt in de volgende stappen:</span><span class="sxs-lookup"><span data-stu-id="c8478-109">From version 5.0, the **Adjust Cost – Item Entries** batch job assigns a posting date to the value entry it is about to create in the following steps:</span></span>  

1.  <span data-ttu-id="c8478-110">Eerst is de boekingsdatum van de post die wordt gemaakt, hetzelfde als de datum van de post die wordt aangepast.</span><span class="sxs-lookup"><span data-stu-id="c8478-110">Initially the Posting Date of the entry to be created is the same date as the entry it adjusts.</span></span>  

2.  <span data-ttu-id="c8478-111">De boekingsdatum wordt gevalideerd tegen voorraadperioden en/of boekhoudinstellingen.</span><span class="sxs-lookup"><span data-stu-id="c8478-111">The Posting Date is validated against Inventory Periods and/or General Ledger Setup.</span></span>  

3.  <span data-ttu-id="c8478-112">Toewijzing van boekingsdatum; als de oorspronkelijke boekingsdatum niet binnen het toegestane boekingsdatumbereik ligt, wijst de batchverwerking een toegestane boekingsdatum uit Boekhoudinstellingen of Voorraadperiode toe.</span><span class="sxs-lookup"><span data-stu-id="c8478-112">Assignment of Posting Date; If the initial Posting Date is not within allowed posting date range the batch job will assign an allowed Posting Date from either General Ledger Setup or Inventory Period.</span></span> <span data-ttu-id="c8478-113">Als zowel voorraadperioden als toegestane boekingsdatums in grootboekinstellingen zijn gedefinieerd, wordt de latere datum van de twee toegewezen aan de herwaarderingswaardepost.</span><span class="sxs-lookup"><span data-stu-id="c8478-113">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will be assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="c8478-114">Laten we dit proces eens in de praktijk bekijken.</span><span class="sxs-lookup"><span data-stu-id="c8478-114">Let’s review this process more in practice.</span></span> <span data-ttu-id="c8478-115">Stel dat we een artikelpost Verkoop hebben.</span><span class="sxs-lookup"><span data-stu-id="c8478-115">Assume we have an Item Ledger Entry of Sale.</span></span> <span data-ttu-id="c8478-116">Het artikel is verzonden op 5 september 2013 en de dag erna gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="c8478-116">The item was shipped on September 5th, 2013 and it was invoiced the day after.</span></span>  

<span data-ttu-id="c8478-117">![Status van artikelposten in het scenario](media/helene/TechArticleAdjustcost1.png "Status van artikelposten in het scenario")</span><span class="sxs-lookup"><span data-stu-id="c8478-117">![State of item ledger entries in the scenario](media/helene/TechArticleAdjustcost1.png "State of item ledger entries in the scenario")</span></span>  

<span data-ttu-id="c8478-118">Hieronder vertegenwoordigt de eerste waardepost (379) de verzending en heeft dezelfde boekingsdatum als de bovenliggende artikelpost.</span><span class="sxs-lookup"><span data-stu-id="c8478-118">Below, the first Value Entry (379) represents the shipment and carry the same Posting Date as the parent Item ledger Entry.</span></span>  

<span data-ttu-id="c8478-119">De tweede artikelpost (381) vertegenwoordigt de factuur.</span><span class="sxs-lookup"><span data-stu-id="c8478-119">The second Value Entry (381) represents the invoice.</span></span>  

 <span data-ttu-id="c8478-120">De derde waardepost (391) is een herwaardering van de factuurwaardepost (381)</span><span class="sxs-lookup"><span data-stu-id="c8478-120">The third Value Entry (391) is an Adjustment of the invoicing Value Entry (381)</span></span>  

 <span data-ttu-id="c8478-121">![Status van waardeposten in het scenario](media/helene/TechArticleAdjustcost2.png "Status van waardeposten in het scenario")</span><span class="sxs-lookup"><span data-stu-id="c8478-121">![State of value entries in the scenario](media/helene/TechArticleAdjustcost2.png "State of value entries in the scenario")</span></span>  

 <span data-ttu-id="c8478-122">Stap 1: De te maken herwaarderingspost krijgt dezelfde boekingsdatum toegewezen als de post die ermee wordt geherwaardeerd, hierboven geïllustreerd door waardepost 391.</span><span class="sxs-lookup"><span data-stu-id="c8478-122">Step 1: Adjustment Value Entry to be created is assigned same Posting Date as the entry it adjusts, illustrated above by Value entry 391.</span></span>  

 <span data-ttu-id="c8478-123">Stap 2: Validatie van in eerste instantie toegewezen boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="c8478-123">Step 2: Validation of initial assigned Posting Date.</span></span>  

<span data-ttu-id="c8478-124">De batchverwerking **Kostprijs herwaarderen - Artikelposten** bepaalt of de oorspronkelijke boekingsdatum van de herwaarderingswaardepost binnen het toegestane boekingsdatumbereik ligt, op basis van voorraadperioden en/of boekhoudinstellingen.</span><span class="sxs-lookup"><span data-stu-id="c8478-124">The **Adjust Cost – Item Entries** batch job determines if the initial Posting Date of the Adjustment Value Entry is within allowed posting date range based upon Inventory Periods and/or General Ledger Setup.</span></span>  

 <span data-ttu-id="c8478-125">Laten we de hierboven genoemde Verkoop bekijken door instelling van toegestane boekingsdatumbereiken toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="c8478-125">Let’s review the above mentioned Sale by adding setup of allowed posting date ranges.</span></span>  

 <span data-ttu-id="c8478-126">Voorraadperioden:</span><span class="sxs-lookup"><span data-stu-id="c8478-126">Inventory Periods:</span></span>  

<span data-ttu-id="c8478-127">![Voorraadperioden in het scenario](media/helene/TechArticleAdjustcost3.png "Voorraadperioden in het scenario")</span><span class="sxs-lookup"><span data-stu-id="c8478-127">![Inventory periods in the scenario](media/helene/TechArticleAdjustcost3.png "Inventory periods in the scenario")</span></span>

 <span data-ttu-id="c8478-128">De eerste toegestane boekingsdatum is de eerste dag van de eerste open periode.</span><span class="sxs-lookup"><span data-stu-id="c8478-128">First allowed posting date is the first day in the first open period.</span></span> <span data-ttu-id="c8478-129">1 September 2013.</span><span class="sxs-lookup"><span data-stu-id="c8478-129">September 1st, 2013.</span></span>  

 <span data-ttu-id="c8478-130">Grootboekinstellingen:</span><span class="sxs-lookup"><span data-stu-id="c8478-130">General Ledger Setup:</span></span>  

<span data-ttu-id="c8478-131">![Grootboekinstelling in het scenario](media/helene/TechArticleAdjustcost4.png "Grootboekinstelling in het scenario")</span><span class="sxs-lookup"><span data-stu-id="c8478-131">![G/L Setup in the scenario](media/helene/TechArticleAdjustcost4.png "G/L Setup in the scenario")</span></span>

 <span data-ttu-id="c8478-132">De eerste toegestane boekingsdatum is de datum in het veld Boeken toegest. vanaf: 10 september 2013.</span><span class="sxs-lookup"><span data-stu-id="c8478-132">First allowed posting date is the date stated in field Allow Posting From: September 10th, 2013.</span></span>  

 <span data-ttu-id="c8478-133">Als zowel voorraadperioden als toegestane boekingsdatums in grootboekinstellingen zijn gedefinieerd, definieert de latere datum van de twee het toegestane boekingsdatumbereik.</span><span class="sxs-lookup"><span data-stu-id="c8478-133">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will define the allowed posting date range.</span></span>  

 <span data-ttu-id="c8478-134">Stap 3: Toewijzing van een toegestane boekingsdatum;</span><span class="sxs-lookup"><span data-stu-id="c8478-134">Step 3: Assignment of an allowed posting date;</span></span>  

 <span data-ttu-id="c8478-135">De aanvankelijke toegewezen Boekingsdatum was 6 september, zoals in stap 1 wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="c8478-135">The initial assigned Posting Date was September 6th as illustrated in step 1.</span></span> <span data-ttu-id="c8478-136">Echter, in de tweede stap identificeert de batchverwerking Kostprijs herwaarderen - Artikelposten dat de vroegste toegestane boekingsdatum 10 september is en wijst dus 10 september toe aan de herwaarderingswaardepost, onder.</span><span class="sxs-lookup"><span data-stu-id="c8478-136">However, in the 2nd step the Adjust Cost – Item entries batch job identifies that earliest allowed Posting Date is September 10th and thereby assigns September 10th to the Adjustment Value Entry, below.</span></span>  

 <span data-ttu-id="c8478-137">![Status van waardeposten in het scenario 2](media/helene/TechArticleAdjustcost5.png "Status van waardeposten in het scenario 2")</span><span class="sxs-lookup"><span data-stu-id="c8478-137">![State of value entries in the scenario 2](media/helene/TechArticleAdjustcost5.png "State of value entries in the scenario 2")</span></span>

 <span data-ttu-id="c8478-138">We hebben nu het concept bekeken voor het toewijzen van Boekingsdatums aan waardeposten die worden gemaakt door de batchverwerking Kostprijs herwaarderen - Artikelposten.</span><span class="sxs-lookup"><span data-stu-id="c8478-138">We have now reviewed the concept for assigning Posting Dates to Value Entries created by the Adjust Cost - Item entries batch job.</span></span>  

 <span data-ttu-id="c8478-139">Laten we enkele scenario's bekijken die we in het ondersteuningsteam van tijd tot tijd tegenkomen in verband met toegewezen boekingsdatums in de batchverwerking Kostprijs herwaarderen - Artikelposten en gerelateerde instellingen.</span><span class="sxs-lookup"><span data-stu-id="c8478-139">Let’s continue to review some scenarios that we in the support team comes across from time to time in relation to assigned Posting Dates in the Adjust Cost – Item entries batch job and related setups.</span></span>  

## <a name="scenarios"></a><span data-ttu-id="c8478-140">Scenario's</span><span class="sxs-lookup"><span data-stu-id="c8478-140">Scenarios</span></span>  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a><span data-ttu-id="c8478-141">Scenario I: "De boekingsdatum ligt niet binnen het bereik van toegestane boekingsdatums."</span><span class="sxs-lookup"><span data-stu-id="c8478-141">Scenario I: “Posting Date is not within your range of allowed posting dates…”</span></span>  
 <span data-ttu-id="c8478-142">Dit is een scenario waarin een gebruiker het genoemde foutbericht krijgt wanneer de batchverwerking Kostprijs herwaarderen - Artikelposten wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c8478-142">This is a scenario where a user is experiencing mentioned error message when the Adjust Cost – Item entries batch job is run.</span></span>  

 <span data-ttu-id="c8478-143">In de vorige sectie, waar het concept van het toewijzen van boekingsdatums wordt besproken, is het de bedoeling van de batchverwerking Kostprijs herwaarderen - Artikelposten een waardepost te maken met de boekingsdatum 10 september.</span><span class="sxs-lookup"><span data-stu-id="c8478-143">In the previous section, describing the concept of assigning posting dates, the intention of the Adjust Cost – Item entries batch job is to create a Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="c8478-144">![Foutmelding over boekingsdatum](media/helene/TechArticleAdjustcost6.png "Foutmelding over boekingsdatum")</span><span class="sxs-lookup"><span data-stu-id="c8478-144">![Error message about posting date](media/helene/TechArticleAdjustcost6.png "Error message about posting date")</span></span>

 <span data-ttu-id="c8478-145">We gaan door op de gebruikersinstelling:</span><span class="sxs-lookup"><span data-stu-id="c8478-145">We follow up on the User Setup:</span></span>  

<span data-ttu-id="c8478-146">![Instelling van toegestane boekingsdatum van gebruiker](media/helene/TechArticleAdjustcost7.png "Instelling van toegestane boekingsdatum van gebruiker")</span><span class="sxs-lookup"><span data-stu-id="c8478-146">![User's allowed posting dates setup](media/helene/TechArticleAdjustcost7.png "User's allowed posting dates setup")</span></span>

 <span data-ttu-id="c8478-147">De gebruiker heeft in dit geval een toegestane boekingsdatumreeks van 11 september tot 30 september en mag daardoor de herwaarderingswaardepost niet boeken met boekingsdatum 10 september.</span><span class="sxs-lookup"><span data-stu-id="c8478-147">The user in this case has an allowed posting date range from September 11th to September 30th and is thereby not allowed to post the Adjustment Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="c8478-148">![Overzicht van betrokken instelling van boekingsdatum](media/helene/TechArticleAdjustcost8.png "Overzicht van betrokken instelling van boekingsdatum")</span><span class="sxs-lookup"><span data-stu-id="c8478-148">![Overview of involved posting date setup](media/helene/TechArticleAdjustcost8.png "Overview of involved posting date setup")</span></span>

 <span data-ttu-id="c8478-149">Knowledge Base-artikel [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) bespreekt aanvullende scenario's in verband met het genoemde foutbericht.</span><span class="sxs-lookup"><span data-stu-id="c8478-149">Knowledge Base article [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) discusses additional scenarios related to mentioned error message.</span></span>  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a><span data-ttu-id="c8478-150">Scenario II: Boekingsdatum op Herwaarderingswaardepost versus Boekingsdatum op post die de correctie veroorzaakt, zoals Herwaardering of productie Artikeltoeslag.</span><span class="sxs-lookup"><span data-stu-id="c8478-150">Scenario II: Posting Date on Adjustment Value Entry versus Posting Date on entry causing the adjustment such as Revaluation or Item charge.</span></span>  

### <a name="revaluation-scenario"></a><span data-ttu-id="c8478-151">Herwaarderingsscenario:</span><span class="sxs-lookup"><span data-stu-id="c8478-151">Revaluation scenario:</span></span>  
 <span data-ttu-id="c8478-152">Vereisten:</span><span class="sxs-lookup"><span data-stu-id="c8478-152">Prerequisites:</span></span>  

 <span data-ttu-id="c8478-153">Voorraadinstelling:</span><span class="sxs-lookup"><span data-stu-id="c8478-153">Inventory setup:</span></span>  

-   <span data-ttu-id="c8478-154">Autom. voorraadwaarde boeken = Ja</span><span class="sxs-lookup"><span data-stu-id="c8478-154">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="c8478-155">Automatische kostenwaardering = Altijd</span><span class="sxs-lookup"><span data-stu-id="c8478-155">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="c8478-156">Gem. kostprijsberekeningsoort = artikel</span><span class="sxs-lookup"><span data-stu-id="c8478-156">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="c8478-157">Periode gemiddelde kostprijsberekening = Dag</span><span class="sxs-lookup"><span data-stu-id="c8478-157">Average Cost Period=Day</span></span>  

 <span data-ttu-id="c8478-158">Grootboekinstellingen:</span><span class="sxs-lookup"><span data-stu-id="c8478-158">General Ledger Setup:</span></span>  

-   <span data-ttu-id="c8478-159">Boeken toegest. vanaf = 1 januari 2014</span><span class="sxs-lookup"><span data-stu-id="c8478-159">Allow Posting From = January 1st, 2014</span></span>  

-   <span data-ttu-id="c8478-160">Boeken toegest. tot = leeg</span><span class="sxs-lookup"><span data-stu-id="c8478-160">Allow Posting To = empty</span></span>  

 <span data-ttu-id="c8478-161">Gebruikersinstellingen:</span><span class="sxs-lookup"><span data-stu-id="c8478-161">User Setup:</span></span>  

-   <span data-ttu-id="c8478-162">Boeken toegest. vanaf = 1 december 2013.</span><span class="sxs-lookup"><span data-stu-id="c8478-162">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="c8478-163">Boeken toegest. tot = leeg</span><span class="sxs-lookup"><span data-stu-id="c8478-163">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="c8478-164">Het scenario testen</span><span class="sxs-lookup"><span data-stu-id="c8478-164">To test the scenario</span></span>  

1.  <span data-ttu-id="c8478-165">ArtikelTEST maken:</span><span class="sxs-lookup"><span data-stu-id="c8478-165">Create item TEST:</span></span>  

     <span data-ttu-id="c8478-166">Basiseenheid = Stuks</span><span class="sxs-lookup"><span data-stu-id="c8478-166">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="c8478-167">Waarderingsmethode = Gemiddelde</span><span class="sxs-lookup"><span data-stu-id="c8478-167">Costing Method = Average</span></span>  

     <span data-ttu-id="c8478-168">Selecteer optionele boekingsgroepen.</span><span class="sxs-lookup"><span data-stu-id="c8478-168">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="c8478-169">Open artikeldagboek, maak en boek een regel als volgt:</span><span class="sxs-lookup"><span data-stu-id="c8478-169">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="c8478-170">Boekingsdatum = 15 december 2013</span><span class="sxs-lookup"><span data-stu-id="c8478-170">Posting Date = December 15th, 2013</span></span>  

     <span data-ttu-id="c8478-171">Artikel = TEST</span><span class="sxs-lookup"><span data-stu-id="c8478-171">Item = TEST</span></span>  

     <span data-ttu-id="c8478-172">Boekingssoort = Inkoop</span><span class="sxs-lookup"><span data-stu-id="c8478-172">Entry Type = Purchase</span></span>  

     <span data-ttu-id="c8478-173">Aantal = 100</span><span class="sxs-lookup"><span data-stu-id="c8478-173">Quantity = 100</span></span>  

     <span data-ttu-id="c8478-174">Eenheidsprijs = 10</span><span class="sxs-lookup"><span data-stu-id="c8478-174">Unit Amount = 10</span></span>  

3.  <span data-ttu-id="c8478-175">Open artikeldagboek, maak en boek een regel als volgt:</span><span class="sxs-lookup"><span data-stu-id="c8478-175">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="c8478-176">Datum = 20 december 2013</span><span class="sxs-lookup"><span data-stu-id="c8478-176">Date = December 20th, 2013</span></span>  

     <span data-ttu-id="c8478-177">Artikel = TEST</span><span class="sxs-lookup"><span data-stu-id="c8478-177">Item = TEST</span></span>  

     <span data-ttu-id="c8478-178">Boekingssoort = Negatieve herwaardering</span><span class="sxs-lookup"><span data-stu-id="c8478-178">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="c8478-179">Aantal = 2</span><span class="sxs-lookup"><span data-stu-id="c8478-179">Quantity = 2</span></span>  

4.  <span data-ttu-id="c8478-180">Open artikeldagboek, maak en boek een regel als volgt:</span><span class="sxs-lookup"><span data-stu-id="c8478-180">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="c8478-181">Datum = 15 januari 2014</span><span class="sxs-lookup"><span data-stu-id="c8478-181">Date = January 15th, 2014</span></span>  

     <span data-ttu-id="c8478-182">Artikel = TEST</span><span class="sxs-lookup"><span data-stu-id="c8478-182">Item = TEST</span></span>  

     <span data-ttu-id="c8478-183">Boekingssoort = Negatieve herwaardering</span><span class="sxs-lookup"><span data-stu-id="c8478-183">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="c8478-184">Aantal = 3</span><span class="sxs-lookup"><span data-stu-id="c8478-184">Quantity = 3</span></span>  

5.  <span data-ttu-id="c8478-185">Open herwaarderingsdagboek, maak en boek een regel als volgt:</span><span class="sxs-lookup"><span data-stu-id="c8478-185">Open Revaluation Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="c8478-186">Artikel = TEST</span><span class="sxs-lookup"><span data-stu-id="c8478-186">Item = TEST</span></span>  

     <span data-ttu-id="c8478-187">Vereffenen met post = selecteer inkooppost die is geboekt in stap 2.</span><span class="sxs-lookup"><span data-stu-id="c8478-187">Applies-to Entry = select Purchase entry posted at step 2.</span></span> <span data-ttu-id="c8478-188">De boekingsdatum van de herwaardering is dezelfde als van de post die wordt aangepast.</span><span class="sxs-lookup"><span data-stu-id="c8478-188">The Posting Date of the revaluation will be the same as the entry it adjusts.</span></span>  

     <span data-ttu-id="c8478-189">Kostprijs (Geherwaardeerd) = 40</span><span class="sxs-lookup"><span data-stu-id="c8478-189">Unit Cost Revalued = 40</span></span>  

 <span data-ttu-id="c8478-190">De volgende artikel- en waardeposten zijn geboekt:</span><span class="sxs-lookup"><span data-stu-id="c8478-190">The following Item Ledger and Value Entries have been posted:</span></span>  

<span data-ttu-id="c8478-191">![Overzicht van resulterende artikel- en waardeposten 1](media/helene/TechArticleAdjustcost9.png "Overzicht van resulterende artikel- en waardeposten 1")</span><span class="sxs-lookup"><span data-stu-id="c8478-191">![Overview of resulting item ledger and value entries 1](media/helene/TechArticleAdjustcost9.png "Overview of resulting item ledger and value entries 1")</span></span>

 <span data-ttu-id="c8478-192">![Overzicht van resulterende artikel- en waardeposten 2](media/helene/TechArticleAdjustcost10.png "Overzicht van resulterende artikel- en waardeposten 2")</span><span class="sxs-lookup"><span data-stu-id="c8478-192">![Overview of resulting item ledger and value entries 2](media/helene/TechArticleAdjustcost10.png "Overview of resulting item ledger and value entries 2")</span></span>

 <span data-ttu-id="c8478-193">De batchverwerking Kostprijs herwaarderen - Artikelposten heeft een wijziging in kosten herkend en de negatieve herwaarderingen aangepast.</span><span class="sxs-lookup"><span data-stu-id="c8478-193">The Adjust Cost – Item entries batch job has recognized a change in cost and adjusted the Negative Adjustments.</span></span>  

 <span data-ttu-id="c8478-194">**Controle van boekingsdatums in gemaakte herwaarderingswaardeposten:** De vroegste toegestane boekingsdatum waarop de batchverwerking Kostprijs herwaarderen - Artikelposten betrekking moet hebben is 1 januari 2014, zoals gesteld in de boekhoudinstellingen.</span><span class="sxs-lookup"><span data-stu-id="c8478-194">**Review of Posting Dates on created Adjustment Value Entries:** The earliest allowed Posting Date the Adjust Cost - Item Entries batch job has to relate to is January 1st, 2014 as stated in the General Ledger Setup.</span></span>  

 <span data-ttu-id="c8478-195">**Negatieve herwaardering in stap 3:** toegewezen boekingsdatum is 1 januari, bepaald door boekhoudinstellingen.</span><span class="sxs-lookup"><span data-stu-id="c8478-195">**Negative Adjustment in step 3:** assigned Posting Date is January 1st, provided by General Ledger Setup.</span></span> <span data-ttu-id="c8478-196">De boekingsdatum van de waardepost in het bereik voor herwaardering is 20 december 2013.</span><span class="sxs-lookup"><span data-stu-id="c8478-196">The Posting Date of the Value Entry in scope for adjustment is December 20, 2013.</span></span> <span data-ttu-id="c8478-197">Volgens de boekhoudinstellingen ligt de datum niet binnen het toegestane boekingsdatumbereik.</span><span class="sxs-lookup"><span data-stu-id="c8478-197">According to General Ledger Setup the date is not within allowed posting date range.</span></span> <span data-ttu-id="c8478-198">Daarom wordt de boekingsdatum in het veld Boeken toegest. vanaf in de boekhoudinstellingen toegewezen aan de herwaarderingswaardepost.</span><span class="sxs-lookup"><span data-stu-id="c8478-198">Therefore the Posting Date stated in the Allow Posting From field in the General Ledger Setup is assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="c8478-199">**Negatieve herwaardering in stap 4:** toegewezen boekingsdatum is 15 januari.</span><span class="sxs-lookup"><span data-stu-id="c8478-199">**Negative Adjustment in step 4:** assigned Posting Date is January 15th.</span></span> <span data-ttu-id="c8478-200">De waardepost in het bereik van herwaardering heeft boekingsdatum 15 januari, wat ligt binnen het toegestane boekingsdatumbereik, volgens de boekhoudinstellingen.</span><span class="sxs-lookup"><span data-stu-id="c8478-200">The Value Entry in scope of adjustment has Posting Date January 15th, which is within the allowed posting date range according to General Ledger Setup.</span></span>  

 <span data-ttu-id="c8478-201">De herwaardering die wordt aangebracht voor de Negatieve herwaardering in stap 3 leidt tot discussie.</span><span class="sxs-lookup"><span data-stu-id="c8478-201">The adjustment made for the Negative Adjustment in step 3 causes discussion.</span></span> <span data-ttu-id="c8478-202">De gunstige boekingsdatum voor de Herwaarderingswaardepost zou 20 december zijn of ten minste in december liggen aangezien de herwaardering die de wijziging in COGS heeft veroorzaakt, is geboekt in december.</span><span class="sxs-lookup"><span data-stu-id="c8478-202">The favorable Posting Date for the Adjustment Value Entry would have been December 20th or at least within December as the revaluation causing the change in COGS was posted in December.</span></span>  

 <span data-ttu-id="c8478-203">Om herwaardering in december te bereiken van de negatieve correctie in stap 3, moet het veld Boeken toegest. vanaf in de boekhoudinstellingen een datum in december bevatten.</span><span class="sxs-lookup"><span data-stu-id="c8478-203">To achieve adjustment in December of the Negative Adjustment in step 3, the General Ledger Setup, Allow Posting From field, need to state a date in December.</span></span>  

 <span data-ttu-id="c8478-204">**Conclusie:**</span><span class="sxs-lookup"><span data-stu-id="c8478-204">**Conclusion:**</span></span>  

 <span data-ttu-id="c8478-205">Overweeg met de ervaringen uit dit scenario de geschiktste instelling van toegestane boekingsdatumbereik voor een bedrijf. Het volgende kan nuttig zijn: zolang wijzigingen in voorraadwaarde in een periode mogen worden geboekt, december in dit geval, moet de instelling die het bedrijf gebruikt voor toegestane boekingsdatumbereiken, overeenstemmen met deze beslissing.</span><span class="sxs-lookup"><span data-stu-id="c8478-205">With the experiences from this scenario, considering most suitable setup of allowed posting date range for a company, the following might be useful: As long as changes in inventory value is allowed to be posted in a period, December in this case, the setup the company uses for allowed posting date ranges should be aligned with this decision.</span></span> <span data-ttu-id="c8478-206">Het veld Boeken toegest. vanaf in de boekhoudinstellingen, dat 1 december bevat, zou toestaan dat de herwaardering die in december is aangebracht, wordt doorgestuurd naar betrokken uitgaande posten in dezelfde periode.</span><span class="sxs-lookup"><span data-stu-id="c8478-206">The Allow Posting From in the General Ledger Setup, stating December 1st  would allow the revaluation made in December to be forwarded to affected outbound entries in the same period.</span></span>  

 <span data-ttu-id="c8478-207">Gebruikersgroepen die niet in december mogen boeken, maar in januari, een beperking die waarschijnlijk de bedoeling was van de boekhoudinstellingen in dit scenario, moeten in plaats daarvan worden geregeld met de gebruikersinstellingen.</span><span class="sxs-lookup"><span data-stu-id="c8478-207">User groups not allowed to post in December but in January, which was probably intended to be limited by the General Ledger Setup in this scenario, should instead be addressed via the User setup.</span></span>  

### <a name="item-charge-scenario"></a><span data-ttu-id="c8478-208">Artikeltoeslagscenario:</span><span class="sxs-lookup"><span data-stu-id="c8478-208">Item charge scenario:</span></span>  
 <span data-ttu-id="c8478-209">Vereisten:</span><span class="sxs-lookup"><span data-stu-id="c8478-209">Prerequisites:</span></span>  

 <span data-ttu-id="c8478-210">Voorraadinstelling:</span><span class="sxs-lookup"><span data-stu-id="c8478-210">Inventory setup:</span></span>  

-   <span data-ttu-id="c8478-211">Autom. voorraadwaarde boeken = Ja</span><span class="sxs-lookup"><span data-stu-id="c8478-211">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="c8478-212">Automatische kostenwaardering = Altijd</span><span class="sxs-lookup"><span data-stu-id="c8478-212">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="c8478-213">Gem. kostprijsberekeningsoort = artikel</span><span class="sxs-lookup"><span data-stu-id="c8478-213">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="c8478-214">Periode gemiddelde kostprijsberekening = Dag</span><span class="sxs-lookup"><span data-stu-id="c8478-214">Average Cost Period=Day</span></span>  

 <span data-ttu-id="c8478-215">Grootboekinstellingen:</span><span class="sxs-lookup"><span data-stu-id="c8478-215">General Ledger Setup:</span></span>  

-   <span data-ttu-id="c8478-216">Boeken toegest. vanaf = 1 december 2013.</span><span class="sxs-lookup"><span data-stu-id="c8478-216">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="c8478-217">Boeken toegest. tot = leeg</span><span class="sxs-lookup"><span data-stu-id="c8478-217">Allow Posting To = empty</span></span>  

 <span data-ttu-id="c8478-218">Gebruikersinstellingen:</span><span class="sxs-lookup"><span data-stu-id="c8478-218">User Setup:</span></span>  

-   <span data-ttu-id="c8478-219">Boeken toegest. vanaf = 1 december 2013.</span><span class="sxs-lookup"><span data-stu-id="c8478-219">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="c8478-220">Boeken toegest. tot = leeg</span><span class="sxs-lookup"><span data-stu-id="c8478-220">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="c8478-221">Het scenario testen</span><span class="sxs-lookup"><span data-stu-id="c8478-221">To test the scenario</span></span>  

1.  <span data-ttu-id="c8478-222">Artikeltoeslag maken:</span><span class="sxs-lookup"><span data-stu-id="c8478-222">Create item charge:</span></span>  

     <span data-ttu-id="c8478-223">Basiseenheid = Stuks</span><span class="sxs-lookup"><span data-stu-id="c8478-223">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="c8478-224">Waarderingsmethode = Gemiddelde</span><span class="sxs-lookup"><span data-stu-id="c8478-224">Costing Method = Average</span></span>  

     <span data-ttu-id="c8478-225">Selecteer optionele boekingsgroepen.</span><span class="sxs-lookup"><span data-stu-id="c8478-225">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="c8478-226">Nieuwe inkooporder maken</span><span class="sxs-lookup"><span data-stu-id="c8478-226">Create new purchase order</span></span>  

     <span data-ttu-id="c8478-227">Orderleveranciersnr.: 10000</span><span class="sxs-lookup"><span data-stu-id="c8478-227">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="c8478-228">Boekingsdatum = 15 december 2013</span><span class="sxs-lookup"><span data-stu-id="c8478-228">Posting Date = December 15th, 2013</span></span>  

     <span data-ttu-id="c8478-229">Leveranciersfactuurnr.: 1234</span><span class="sxs-lookup"><span data-stu-id="c8478-229">Vendor Invoice No.: 1234</span></span>  

     <span data-ttu-id="c8478-230">Op de inkooporderregel:</span><span class="sxs-lookup"><span data-stu-id="c8478-230">On the purchase order line:</span></span>  

     <span data-ttu-id="c8478-231">Artikel = TOESLAG</span><span class="sxs-lookup"><span data-stu-id="c8478-231">Item = CHARGE</span></span>  

     <span data-ttu-id="c8478-232">Aantal = 1</span><span class="sxs-lookup"><span data-stu-id="c8478-232">Quantity = 1</span></span>  

     <span data-ttu-id="c8478-233">Directe kostprijs = 100</span><span class="sxs-lookup"><span data-stu-id="c8478-233">Direct Unit Cost = 100</span></span>  

     <span data-ttu-id="c8478-234">Ontvangst en factuur boeken.</span><span class="sxs-lookup"><span data-stu-id="c8478-234">Post Receive and Invoice.</span></span>  

3.  <span data-ttu-id="c8478-235">Nieuwe verkooporder maken:</span><span class="sxs-lookup"><span data-stu-id="c8478-235">Create new sales order:</span></span>  

     <span data-ttu-id="c8478-236">Orderklantnr.: 10000</span><span class="sxs-lookup"><span data-stu-id="c8478-236">Sell-to Customer No.: 10000</span></span>  

     <span data-ttu-id="c8478-237">Boekingsdatum = 16 december 2013</span><span class="sxs-lookup"><span data-stu-id="c8478-237">Posting Date = December 16th, 2013</span></span>  

     <span data-ttu-id="c8478-238">Op de verkooporderregel:</span><span class="sxs-lookup"><span data-stu-id="c8478-238">On the sales order line:</span></span>  

     <span data-ttu-id="c8478-239">Artikel = TOESLAG</span><span class="sxs-lookup"><span data-stu-id="c8478-239">Item = CHARGE</span></span>  

     <span data-ttu-id="c8478-240">Aantal = 1</span><span class="sxs-lookup"><span data-stu-id="c8478-240">Quantity = 1</span></span>  

     <span data-ttu-id="c8478-241">Eenheidsprijs - 135</span><span class="sxs-lookup"><span data-stu-id="c8478-241">Unit Price = 135</span></span>  

     <span data-ttu-id="c8478-242">Verzenden en factureren boeken.</span><span class="sxs-lookup"><span data-stu-id="c8478-242">Post Ship and Invoice.</span></span>  

4.  <span data-ttu-id="c8478-243">Grootboekinstellingen:</span><span class="sxs-lookup"><span data-stu-id="c8478-243">General Ledger Setup:</span></span>  

     <span data-ttu-id="c8478-244">Boeken toegest. vanaf = 1 januari 2014</span><span class="sxs-lookup"><span data-stu-id="c8478-244">Allow Posting From = January 1st, 2014</span></span>  

     <span data-ttu-id="c8478-245">Boeken toegest. tot = leeg</span><span class="sxs-lookup"><span data-stu-id="c8478-245">Allow Posting To = blank</span></span>  

5.  <span data-ttu-id="c8478-246">Nieuwe inkooporder maken:</span><span class="sxs-lookup"><span data-stu-id="c8478-246">Create new purchase order:</span></span>  

     <span data-ttu-id="c8478-247">Orderleveranciersnr.: 10000</span><span class="sxs-lookup"><span data-stu-id="c8478-247">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="c8478-248">Boekingsdatum = 2 januari 2014</span><span class="sxs-lookup"><span data-stu-id="c8478-248">Posting Date = January 2nd, 2014</span></span>  

     <span data-ttu-id="c8478-249">Leveranciersfactuurnr.: 2345</span><span class="sxs-lookup"><span data-stu-id="c8478-249">Vendor Invoice No.: 2345</span></span>  

     <span data-ttu-id="c8478-250">Op de inkooporderregel:</span><span class="sxs-lookup"><span data-stu-id="c8478-250">On the purchase order line:</span></span>  

     <span data-ttu-id="c8478-251">Artikeltoeslag = JB-VRACHT</span><span class="sxs-lookup"><span data-stu-id="c8478-251">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="c8478-252">Aantal = 1</span><span class="sxs-lookup"><span data-stu-id="c8478-252">Quantity = 1</span></span>  

     <span data-ttu-id="c8478-253">Directe kostprijs = 3</span><span class="sxs-lookup"><span data-stu-id="c8478-253">Direct Unit Cost = 3</span></span>  

     <span data-ttu-id="c8478-254">Wijs artikeltoeslag toe aan inkoopontvangst uit stap 2.</span><span class="sxs-lookup"><span data-stu-id="c8478-254">Assign Item Charge to Purchase Receipt from step 2.</span></span>  

     <span data-ttu-id="c8478-255">Ontvangst en factuur boeken.</span><span class="sxs-lookup"><span data-stu-id="c8478-255">Post Receipt and Invoice.</span></span>  

     <span data-ttu-id="c8478-256">![Overzicht van resulterende artikel- en waardeposten 3](media/helene/TechArticleAdjustcost11.png "Overzicht van resulterende artikel- en waardeposten 3")</span><span class="sxs-lookup"><span data-stu-id="c8478-256">![Overview of resulting item ledger and value entries 3](media/helene/TechArticleAdjustcost11.png "Overview of resulting item ledger and value entries 3")</span></span>

6.  <span data-ttu-id="c8478-257">Op werkdatum 3 januari arriveert een inkoopfactuur met een aanvullende artikeltoeslag bovenop de inkoop die in stap 2 is gedaan.</span><span class="sxs-lookup"><span data-stu-id="c8478-257">On work date January 3rd a purchase invoice arrives, containing an additional item charge to the purchase made in step 2.</span></span> <span data-ttu-id="c8478-258">Deze factuur heeft documentdatum 30 december en is dus geboekt met boekingsdatum 30 december 2013.</span><span class="sxs-lookup"><span data-stu-id="c8478-258">This invoice has document date December 30th and is therefore posted with Posting Date December 30th, 2013.</span></span>  

     <span data-ttu-id="c8478-259">Nieuwe inkooporder maken:</span><span class="sxs-lookup"><span data-stu-id="c8478-259">Create new purchase order:</span></span>  

     <span data-ttu-id="c8478-260">Orderleveranciersnr.: 10000</span><span class="sxs-lookup"><span data-stu-id="c8478-260">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="c8478-261">Boekingsdatum = 30 december 2013</span><span class="sxs-lookup"><span data-stu-id="c8478-261">Posting Date = December 30th, 2013</span></span>  

     <span data-ttu-id="c8478-262">Leveranciersfactuurnr.: 3456</span><span class="sxs-lookup"><span data-stu-id="c8478-262">Vendor Invoice No.: 3456</span></span>  

     <span data-ttu-id="c8478-263">Op de inkooporderregel:</span><span class="sxs-lookup"><span data-stu-id="c8478-263">On the purchase order line:</span></span>  

     <span data-ttu-id="c8478-264">Artikeltoeslag = JB-VRACHT</span><span class="sxs-lookup"><span data-stu-id="c8478-264">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="c8478-265">Aantal = 1</span><span class="sxs-lookup"><span data-stu-id="c8478-265">Quantity = 1</span></span>  

     <span data-ttu-id="c8478-266">Directe kostprijs = 2</span><span class="sxs-lookup"><span data-stu-id="c8478-266">Direct Unit Cost = 2</span></span>  

     <span data-ttu-id="c8478-267">Wijs artikeltoeslag toe aan inkoopontvangst uit stap 2</span><span class="sxs-lookup"><span data-stu-id="c8478-267">Assign Item Charge to Purchase Receipt from step 2</span></span>  

     <span data-ttu-id="c8478-268">Ontvangst en factuur boeken.</span><span class="sxs-lookup"><span data-stu-id="c8478-268">Post Receipt and Invoice.</span></span>  

   <span data-ttu-id="c8478-269">![Overzicht van resulterende artikel- en waardeposten 4](media/helene/TechArticleAdjustcost12.png "Overzicht van resulterende artikel- en waardeposten 4")</span><span class="sxs-lookup"><span data-stu-id="c8478-269">![Overview of resulting item ledger and value entries 4](media/helene/TechArticleAdjustcost12.png "Overview of resulting item ledger and value entries 4")</span></span>

 <span data-ttu-id="c8478-270">Het rapport Voorraadwaardering wordt afgedrukt vanaf 31 december 2013</span><span class="sxs-lookup"><span data-stu-id="c8478-270">Inventory Valuation report is printed as of Date December 31st , 2013</span></span>  

<span data-ttu-id="c8478-271">![Inhoud van het voorraadwaarderingsrapport](media/helene/TechArticleAdjustcost13.png "Inhoud van het voorraadwaarderingsrapport")</span><span class="sxs-lookup"><span data-stu-id="c8478-271">![Content of the Inventory Valuation report](media/helene/TechArticleAdjustcost13.png "Content of the Inventory Valuation report")</span></span>

 <span data-ttu-id="c8478-272">**Overzicht van scenario:**</span><span class="sxs-lookup"><span data-stu-id="c8478-272">**Summary of scenario:**</span></span>  

 <span data-ttu-id="c8478-273">Het beschreven scenario eindigt met een rapport Voorraadwaardering dat Aantal = 0 aangeeft terwijl de waarde = 2.</span><span class="sxs-lookup"><span data-stu-id="c8478-273">The described scenario ends up with an Inventory Valuation report demonstrating Quantity = 0 while the Value = 2.</span></span> <span data-ttu-id="c8478-274">De artikeltoeslag die in stap 11 is geboekt, maakt deel uit van de positieve voorraadmutatiewaarde van december terwijl de negatieve voorraadmutatie van dezelfde periode niet wordt beïnvloed.</span><span class="sxs-lookup"><span data-stu-id="c8478-274">The Item charge posted in step 11 is part of the Inventory Increase value of December while the Inventory Decrease of the same period is not affected.</span></span>  

 <span data-ttu-id="c8478-275">Dat de boekhoudinstellingen Boeken toegest. vanaf 1 januari aangeven, was goed voor de eerste artikeltoeslag.</span><span class="sxs-lookup"><span data-stu-id="c8478-275">Having the General Ledger Setup stating Allow Posting From January 1st was a good thing for the first Item charge.</span></span> <span data-ttu-id="c8478-276">De kosten van de positieve en de negatieve voorraadmutatie zijn in dezelfde periode vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="c8478-276">The costs of the Inventory Increase and Decrease was recorded in the same period.</span></span> <span data-ttu-id="c8478-277">Voor de tweede artikeltoeslag leiden de boekhoudinstellingen er echter toe dat de wijziging in COGS in de volgende periode wordt herkend.</span><span class="sxs-lookup"><span data-stu-id="c8478-277">For the second Item charge however, the General Ledger Setup causes the change in COGS to be recognized in the period after.</span></span>  

 <span data-ttu-id="c8478-278">**Conclusie:**</span><span class="sxs-lookup"><span data-stu-id="c8478-278">**Conclusion:**</span></span>  

 <span data-ttu-id="c8478-279">Het is een uitdaging om het rapport Voorraadwaardering Aantal = 0 aan te laten geven terwijl de Waarde <> 0.</span><span class="sxs-lookup"><span data-stu-id="c8478-279">It’s a challenge to have the Inventory Valuation report to demonstrate Quantity = 0 while the Value <> 0.</span></span> <span data-ttu-id="c8478-280">In dat geval is het ook moeilijker de optimale instellingen aan te geven, wanneer inkoopfacturen op dezelfde dag arriveren, maar verschillende perioden of zelfs boekjaren betreffen.</span><span class="sxs-lookup"><span data-stu-id="c8478-280">In this case it’s also more difficult to express the optimal settings, having purchase invoices arriving the same day but addressing different periods or even fiscal years.</span></span> <span data-ttu-id="c8478-281">De overgang naar een nieuw boekjaar vereist meestal enige planning en als onderdeel daarvan moet het proces Kostprijs herwaarderen - Artikelposten, rekening houdend met COGS, worden overwogen.</span><span class="sxs-lookup"><span data-stu-id="c8478-281">Crossing to a new fiscal year usually requires some planning and as part of that the insight of Adjust Cost – Item entries process, recognizing COGS, is to be considered.</span></span>  

 <span data-ttu-id="c8478-282">In dit scenario zou één scenario kunnen zijn het veld Boekhoudinstellingen, Boeken toegest. vanaf voor enkele dagen een datum in december te geven en de boeking van de eerste artikeltoeslag uit te stellen om mogelijk te maken dat alle kosten voor de vorige periode/boekjaar eerst worden herkend voor de periode waartoe ze behoren, de batchverwerking Kosten herwaarderen - Artikelposten uit te voeren en daarna de toegestane boekingsdatum te verplaatsen naar de nieuwe periode\/boekjaar.</span><span class="sxs-lookup"><span data-stu-id="c8478-282">In this scenario one option could have been to have the General Ledger Setup, field Allow Posting From, stating a date in December for a couple of more days and the posting of the first item charge postponed to allow all costs for the previous period/fiscal year to be recognized for the period they belong to first, having the Adjust Cost – Item entries batch job run and thereafter move the allowed posting date to the new period\/fiscal year.</span></span> <span data-ttu-id="c8478-283">De eerste artikeltoeslag met boekingsdatum 2 januari kan dan worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="c8478-283">The first item charge with posting date January 2nd could then be posted.</span></span>  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a><span data-ttu-id="c8478-284">Historie van batchverwerking Kostprijs herwaarderen - Artikelposten</span><span class="sxs-lookup"><span data-stu-id="c8478-284">History of Adjust Cost – Item entries batch job</span></span>  
 <span data-ttu-id="c8478-285">Hieronder vindt u een overzicht van het concept boekingsdatums toewijzen aan herwaarderingswaardeposten door de batchverwerking Kostprijs herwaarderen - Artikelposten, sinds versie 3.0.</span><span class="sxs-lookup"><span data-stu-id="c8478-285">Below is a summary of the concept assigning Posting Dates to Adjustment Value Entries by the Adjust Cost – Item entries batch job since version 3.0.</span></span>  

### <a name="from-version-30370a"></a><span data-ttu-id="c8478-286">Vanaf versie 3.0..3.70.A</span><span class="sxs-lookup"><span data-stu-id="c8478-286">From version 3.0..3.70.A</span></span>  
 <span data-ttu-id="c8478-287">In het aanvraagformulier van de batchverwerking Kostprijs herwaarderen - Artikelposten moet een boekingsdatum worden ingevoerd door de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="c8478-287">In the request form of the Adjust Cost - Item Entries batch job there is a Posting Date to be entered by the user.</span></span> <span data-ttu-id="c8478-288">De batchverwerking doorloopt alle benodigde wijzigingen en maakt waardeposten met de boekingsdatum ingevoerd in het aanvraagformulier.</span><span class="sxs-lookup"><span data-stu-id="c8478-288">The batch job runs through all necessary changes and creates value entries with the posting date entered in the request form.</span></span> <span data-ttu-id="c8478-289">Te gebruiken voorgestelde boekingsdatum is de datum van vandaag.</span><span class="sxs-lookup"><span data-stu-id="c8478-289">Suggested posting date to use is today’s date.</span></span>  

### <a name="version-370b40"></a><span data-ttu-id="c8478-290">Versie 3.70.B..4.0</span><span class="sxs-lookup"><span data-stu-id="c8478-290">Version 3.70.B..4.0</span></span>  
 <span data-ttu-id="c8478-291">In het aanvraagformulier van de batchverwerking Kostprijs herwaarderen - Artikelposten moet een Boekingsdatum post afgesloten periode worden ingevoerd door de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="c8478-291">In the request form of the Adjust Cost - Item Entries batch job there is a Closed Period Entry Posting Date to be entered by the user.</span></span> <span data-ttu-id="c8478-292">De batchverwerking doorloopt alle noodzakelijke wijzigingen en maakt waardeposten met de boekingsdatum van de hoofdartikelpost (verzenddatum van de verkoop waarop de herwaardering betrekking heeft).</span><span class="sxs-lookup"><span data-stu-id="c8478-292">The batch job runs through all necessary changes and creates value entries with the posting date of the parent item ledger entry (shipment date of the sale that the adjustment address).</span></span> <span data-ttu-id="c8478-293">Als de boekingsdatum van de hoofdartikelpost niet binnen het toegestane boekingsdatumbereik ligt, krijgt de postboekingsdatum die is vermeld als Boekingsdatum post afgesloten periode de Herwaarderingswaardepost toegewezen.</span><span class="sxs-lookup"><span data-stu-id="c8478-293">If the posting date of the parent item ledger entry is not within allowed posting date range the posting date stated as Closed Period Entry Posting Date will be assigned the Adjustment Value Entry.</span></span> <span data-ttu-id="c8478-294">De datum wordt geacht zich in een afgesloten periode te bevinden wanneer deze eerder ligt dan de datum in het veld Boeken toegest. vanaf in de Boekhoudinstellingen.</span><span class="sxs-lookup"><span data-stu-id="c8478-294">A date is considered to be in a closed period when it is earlier than the date in the Allow Posting From field in the General Ledger Setup.</span></span>  

### <a name="from-version-50"></a><span data-ttu-id="c8478-295">Vanaf versie 5.0:</span><span class="sxs-lookup"><span data-stu-id="c8478-295">From version 5.0:</span></span>  
 <span data-ttu-id="c8478-296">Er hoeft geen boekingsdatum meer te worden vermeld in het aanvraagformulier van de batchverwerking Kostprijs herwaarderen - Artikelposten.</span><span class="sxs-lookup"><span data-stu-id="c8478-296">There is no longer a posting date to be stated in the request form of the Adjust Cost - Item entries batch job.</span></span> <span data-ttu-id="c8478-297">De batchverwerking doorloopt alle benodigde wijzigingen en maakt waardeposten met de boekingsdatum van de waardepost die wordt geherwaardeerd.</span><span class="sxs-lookup"><span data-stu-id="c8478-297">The batch job runs through all necessary changes and creates value entries with the posting date of the value entry it adjusts.</span></span> <span data-ttu-id="c8478-298">Als de boekingsdatum niet binnen het toegestane boekingsdatumbereik ligt, wordt de boekingsdatum in het veld Boeken toegest. vanaf in de boekhoudinstellingen gebruikt, OF als de voorraadperioden worden gebruikt, wordt de laatste datum van de twee gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c8478-298">If the posting date is not within allowed posting date range the posting date in the Allow Posting From field in the General Ledger Setup, OR if the Inventory periods are used, the later date of the two will be used.</span></span> <span data-ttu-id="c8478-299">Zie hierboven beschreven concept.</span><span class="sxs-lookup"><span data-stu-id="c8478-299">See described concept above.</span></span>  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a><span data-ttu-id="c8478-300">Historie van batchverwerking Voorraadwaarde boeken.</span><span class="sxs-lookup"><span data-stu-id="c8478-300">History of Post Inventory cost to G/L batch job</span></span>  
 <span data-ttu-id="c8478-301">De batchverwerking Voorraadwaarde boeken is nauw verbonden met de batchverwerking Kostprijs herwaarderen - Artikelposten. Daarom wordt de historie van deze batchverwerking hier ook samengevat en gedeeld.</span><span class="sxs-lookup"><span data-stu-id="c8478-301">The Post Inventory Cost to G/L batch job is closely related to the Adjust Cost – Item entries batch job why the history of this batch job is summarized and shared here as well.</span></span>  

### <a name="from-version-30370a"></a><span data-ttu-id="c8478-302">Vanaf versie 3.0..3.70.A</span><span class="sxs-lookup"><span data-stu-id="c8478-302">From version 3.0..3.70.A</span></span>  
 <span data-ttu-id="c8478-303">In het aanvraagformulier van de batchverwerking Voorraadwaarde boeken moet een boekingsdatum worden ingevoerd door de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="c8478-303">In the request form of the Post Inventory Cost to G/L there is a Posting Date to be entered by the user.</span></span> <span data-ttu-id="c8478-304">De batchverwerking doorloopt alle waardeposten binnen het filter, als die er zijn, en maakt grootboekposten met de boekingsdatum die is ingevoerd in het aanvraagformulier.</span><span class="sxs-lookup"><span data-stu-id="c8478-304">The batch job runs through all value entries within the filter, if any, and creates General Ledger Entries with Posting Date entered in the request form.</span></span>  

### <a name="version-370b40"></a><span data-ttu-id="c8478-305">Versie 3.70.B..4.0</span><span class="sxs-lookup"><span data-stu-id="c8478-305">Version 3.70.B..4.0</span></span>  
 <span data-ttu-id="c8478-306">In het aanvraagformulier van de batchverwerking Voorraadwaarde boeken is het veld Boekingsdatum post afgesloten periode beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="c8478-306">In the request form of the Post Inventory Cost to G/L the Closed Period Entry Posting Date field is available.</span></span> <span data-ttu-id="c8478-307">Die datum die u in dit veld invoert, wordt als de boekingsdatum gebruikt voor de grootboekposten die worden gemaakt voor waardeposten waarvan de boekingsdatum in gesloten boekingsperioden ligt.</span><span class="sxs-lookup"><span data-stu-id="c8478-307">The program uses the date you enter in this field as the posting date for the general ledger entries it creates for value entries whose posting dates are in closed accounting periods.</span></span> <span data-ttu-id="c8478-308">Anders hebben de grootboekposten dezelfde boekingsdatum als de oorspronkelijke waardeposten.</span><span class="sxs-lookup"><span data-stu-id="c8478-308">Otherwise, the general ledger entries will have the same posting date as the original value entries.</span></span> <span data-ttu-id="c8478-309">De datum wordt geacht zich in een afgesloten periode te bevinden wanneer deze eerder ligt dan de datum in het veld Boeken toegest. vanaf in de Boekhoudinstellingen.</span><span class="sxs-lookup"><span data-stu-id="c8478-309">A date is considered to be in a closed period when it is earlier than the date in the Allow Posting From field in the General Ledger Setup.</span></span> <span data-ttu-id="c8478-310">Als per boekingsgroep naar het grootboek wordt geboekt, krijgen de grootboekposten de boekingsdatum die is opgegeven in het veld Boekingsdatum op het aanvraagformulier.</span><span class="sxs-lookup"><span data-stu-id="c8478-310">If posting to G\/L Per Posting Group, the general ledger entries will have the posting date that is specified in the Posting Date field in the request form.</span></span>  

 <span data-ttu-id="c8478-311">In versie 3 en 4 worden tijdens de batchverwerking alle waardeposten gescand om te detecteren of er waardeposten zijn waarbij Tot. werk. kosten verschilt van Vrd.-waarde geboekt.</span><span class="sxs-lookup"><span data-stu-id="c8478-311">In version 3 and 4 the batch job scans all value entries to detect if there are any value entries where Cost Amount (Actual) differs from Cost Posted to G/L.</span></span> <span data-ttu-id="c8478-312">Als er een verschil wordt gedetecteerd, wordt het afwijkende bedrag geboekt in een grootboekpost.</span><span class="sxs-lookup"><span data-stu-id="c8478-312">If there is a difference detected the differing amount will be posted in a G/L entry.</span></span> <span data-ttu-id="c8478-313">Als boeking van verwachte kosten wordt gebruikt, worden corresponderende velden op dezelfde manier behandeld.</span><span class="sxs-lookup"><span data-stu-id="c8478-313">If expected cost posting is used corresponding fields are processed in the same way.</span></span>  

<span data-ttu-id="c8478-314">![Werkelijke kosten versus verwachte kosten](media/helene/TechArticleAdjustcost14.png "Werkelijke kosten versus verwachte kosten")</span><span class="sxs-lookup"><span data-stu-id="c8478-314">![Actual cost versus expected cost](media/helene/TechArticleAdjustcost14.png "Actual cost versus expected cost")</span></span>

### <a name="from-version-50"></a><span data-ttu-id="c8478-315">Vanaf versie 5.0:</span><span class="sxs-lookup"><span data-stu-id="c8478-315">From version 5.0:</span></span>  
 <span data-ttu-id="c8478-316">Er hoeft geen boekingsdatum meer te worden vermeld in het aanvraagformulier van de batchverwerking Voorraadwaarde boeken.</span><span class="sxs-lookup"><span data-stu-id="c8478-316">There is no longer a posting date to be stated in the request form of the Post Inventory Cost to G/L batch job.</span></span> <span data-ttu-id="c8478-317">De grootboekpost wordt gemaakt met dezelfde boekingsdatum als de gerelateerde waardepost.</span><span class="sxs-lookup"><span data-stu-id="c8478-317">The G/L entry is created with the same Posting Date as the related value entry.</span></span> <span data-ttu-id="c8478-318">Als u de batchverwerking wilt voltooien, moet het toegestane boekingsdatumbereik de boekingsdatum van de gemaakte grootboekpost toestaan.</span><span class="sxs-lookup"><span data-stu-id="c8478-318">In order to complete the batch job the allowed posting date range must allow the Posting Date of the created G/L entry.</span></span> <span data-ttu-id="c8478-319">Als dit niet het geval is, moet de toegestane boekingsdatumreeks tijdelijk opnieuw worden geopend door de datums in het veld Boeken toegest. vanaf en tot in Boekhoudinstellingen te wijzigen of te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="c8478-319">If not, the allowed posting date range must be temporarily re-opened by changing or removing the dates in the Allow Posting From and To fields in the General Ledger Setup.</span></span> <span data-ttu-id="c8478-320">Om reconciliatieproblemen te voorkomen is het vereist dat de boekingsdatum van de grootboekpost correspondeert met de boekingsdatum van de waardepost.</span><span class="sxs-lookup"><span data-stu-id="c8478-320">To avoid reconciliation issues it is required that Posting Date of the G/L Entry corresponds to the Posting Date of the Value Entry.</span></span>  

 <span data-ttu-id="c8478-321">De batchverwerking scant tabel 5811 - Waardepost naar GB boeken om de waardeposten te bepalen in het bereik voor boeking naar het grootboek.</span><span class="sxs-lookup"><span data-stu-id="c8478-321">The batch job scans Table 5811 - Post Value Entry to G/L, to identify the Value Entries in scope for posting to General Ledger.</span></span> <span data-ttu-id="c8478-322">Na een succesvolle uitvoering wordt de tabel geleegd.</span><span class="sxs-lookup"><span data-stu-id="c8478-322">After successful run the table is emptied.</span></span>

## <a name="see-also"></a><span data-ttu-id="c8478-323">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c8478-323">See Also</span></span>  
[<span data-ttu-id="c8478-324">Ontwerpdetails: Voorraadwaardering</span><span class="sxs-lookup"><span data-stu-id="c8478-324">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)  
[<span data-ttu-id="c8478-325">Ontwerpdetails: Artikelvereffening</span><span class="sxs-lookup"><span data-stu-id="c8478-325">Design Details: Item Application</span></span>](design-details-item-application.md)  

