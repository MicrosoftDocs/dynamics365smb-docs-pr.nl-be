---
title: Boekingsdatum in waardeposten
description: Leren hoe de batchverwerking Kostprijs herwaarderen - Artikelposten een boekingsdatum bepaalt en toewijst aan de waardeposten die de batchverwerking gaat maken.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 918a450ea40676447f872ba95eb489c7cc210211
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215115"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a><span data-ttu-id="052a9-103">Ontwerpdetails: Boekingsdatum op herwaarderingswaardepost</span><span class="sxs-lookup"><span data-stu-id="052a9-103">Design Details: Posting Date on Adjustment Value Entry</span></span>
<span data-ttu-id="052a9-104">Dit artikel begeleidt gebruikers bij de functionaliteit Voorraadwaardering in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="052a9-104">This article provides guidance for users of the Inventory Costing functionality in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="052a9-105">Het specifieke artikel legt uit hoe de batchverwerking **Kostprijs herwaarderen - Artikelposten** een boekingsdatum bepaalt en toewijst aan de waardeposten die de batchverwerking gaat maken.</span><span class="sxs-lookup"><span data-stu-id="052a9-105">The specific article is providing guidance in how the **Adjust Cost - Item Entries** batch job identifies and assigns a posting date to the value entries that the batch job is about to create.</span></span>  

<span data-ttu-id="052a9-106">Eerst wordt het concept van het proces bekeken, hoe de batchverwerking de boekingsdatum bepaalt en toewijst aan de waardepost die wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="052a9-106">First the concept of the process is reviewed, how the batch job identifies and assigns the Posting Date to the Value Entry to be created.</span></span> <span data-ttu-id="052a9-107">Daarna zijn er enkele gedeelde scenario's die we in het ondersteuningsteam van tijd tot tijd tegenkomen en uiteindelijk is er een lijst met de begrippen die worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="052a9-107">Thereafter there are some scenarios shared that we in the support team come across from time to time and finally there is a summary of the concepts used.</span></span>  

## <a name="the-concept"></a><span data-ttu-id="052a9-108">Het concept</span><span class="sxs-lookup"><span data-stu-id="052a9-108">The Concept</span></span>  
<span data-ttu-id="052a9-109">De batchverwerking **Kostprijs herwaarderen - Artikelposten** wijst een boekingsdatum toe aan de waardepost die gaat worden gemaakt in de volgende stappen:</span><span class="sxs-lookup"><span data-stu-id="052a9-109">The **Adjust Cost – Item Entries** batch job assigns a posting date to the value entry it is about to create in the following steps:</span></span>  

1.  <span data-ttu-id="052a9-110">Eerst is de boekingsdatum van de post die wordt gemaakt, hetzelfde als de datum van de post die wordt aangepast.</span><span class="sxs-lookup"><span data-stu-id="052a9-110">Initially the Posting Date of the entry to be created is the same date as the entry it adjusts.</span></span>  

2.  <span data-ttu-id="052a9-111">De boekingsdatum wordt gevalideerd tegen voorraadperioden en/of boekhoudinstellingen.</span><span class="sxs-lookup"><span data-stu-id="052a9-111">The Posting Date is validated against Inventory Periods and/or General Ledger Setup.</span></span>  

3.  <span data-ttu-id="052a9-112">Toewijzing van boekingsdatum; als de oorspronkelijke boekingsdatum niet binnen het toegestane boekingsdatumbereik ligt, wijst de batchverwerking een toegestane boekingsdatum uit Boekhoudinstellingen of Voorraadperiode toe.</span><span class="sxs-lookup"><span data-stu-id="052a9-112">Assignment of Posting Date; If the initial Posting Date is not within allowed posting date range the batch job will assign an allowed Posting Date from either General Ledger Setup or Inventory Period.</span></span> <span data-ttu-id="052a9-113">Als zowel voorraadperioden als toegestane boekingsdatums in grootboekinstellingen zijn gedefinieerd, wordt de latere datum van de twee toegewezen aan de herwaarderingswaardepost.</span><span class="sxs-lookup"><span data-stu-id="052a9-113">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will be assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="052a9-114">Laten we dit proces eens in de praktijk bekijken.</span><span class="sxs-lookup"><span data-stu-id="052a9-114">Let’s review this process more in practice.</span></span> <span data-ttu-id="052a9-115">Stel dat we een artikelpost Verkoop hebben.</span><span class="sxs-lookup"><span data-stu-id="052a9-115">Assume we have an Item Ledger Entry of Sale.</span></span> <span data-ttu-id="052a9-116">Het artikel is verzonden op 5 september 2013 en de dag erna gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="052a9-116">The item was shipped on September 5, 2013 and it was invoiced the day after.</span></span>  

<span data-ttu-id="052a9-117">![Status van artikelposten in het scenario](media/helene/TechArticleAdjustcost1.png "Status van artikelposten in het scenario")</span><span class="sxs-lookup"><span data-stu-id="052a9-117">![State of item ledger entries in the scenario](media/helene/TechArticleAdjustcost1.png "State of item ledger entries in the scenario")</span></span>  

<span data-ttu-id="052a9-118">Hieronder vertegenwoordigt de eerste waardepost (379) de verzending en heeft dezelfde boekingsdatum als de bovenliggende artikelpost.</span><span class="sxs-lookup"><span data-stu-id="052a9-118">Below, the first Value Entry (379) represents the shipment and carry the same Posting Date as the parent Item ledger Entry.</span></span>  

<span data-ttu-id="052a9-119">De tweede artikelpost (381) vertegenwoordigt de factuur.</span><span class="sxs-lookup"><span data-stu-id="052a9-119">The second Value Entry (381) represents the invoice.</span></span>  

 <span data-ttu-id="052a9-120">De derde waardepost (391) is een herwaardering van de factuurwaardepost (381)</span><span class="sxs-lookup"><span data-stu-id="052a9-120">The third Value Entry (391) is an Adjustment of the invoicing Value Entry (381)</span></span>  

 <span data-ttu-id="052a9-121">![Status van waardeposten in het scenario](media/helene/TechArticleAdjustcost2.png "Status van waardeposten in het scenario")</span><span class="sxs-lookup"><span data-stu-id="052a9-121">![State of value entries in the scenario](media/helene/TechArticleAdjustcost2.png "State of value entries in the scenario")</span></span>  

 <span data-ttu-id="052a9-122">Stap 1: De te maken herwaarderingspost krijgt dezelfde boekingsdatum toegewezen als de post die ermee wordt geherwaardeerd, hierboven geïllustreerd door waardepost 391.</span><span class="sxs-lookup"><span data-stu-id="052a9-122">Step 1: Adjustment Value Entry to be created is assigned same Posting Date as the entry it adjusts, illustrated above by Value entry 391.</span></span>  

 <span data-ttu-id="052a9-123">Stap 2: Validatie van in eerste instantie toegewezen boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="052a9-123">Step 2: Validation of initial assigned Posting Date.</span></span>  

<span data-ttu-id="052a9-124">De batchverwerking **Kostprijs herwaarderen - Artikelposten** bepaalt of de oorspronkelijke boekingsdatum van de herwaarderingswaardepost binnen het toegestane boekingsdatumbereik ligt, op basis van voorraadperioden en/of boekhoudinstellingen.</span><span class="sxs-lookup"><span data-stu-id="052a9-124">The **Adjust Cost – Item Entries** batch job determines if the initial Posting Date of the Adjustment Value Entry is within allowed posting date range based upon Inventory Periods and/or General Ledger Setup.</span></span>  

 <span data-ttu-id="052a9-125">Laten we de hierboven genoemde Verkoop bekijken door instelling van toegestane boekingsdatumbereiken toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="052a9-125">Let’s review the above mentioned Sale by adding setup of allowed posting date ranges.</span></span>  

 <span data-ttu-id="052a9-126">Voorraadperioden:</span><span class="sxs-lookup"><span data-stu-id="052a9-126">Inventory Periods:</span></span>  

<span data-ttu-id="052a9-127">![Voorraadperioden in het scenario](media/helene/TechArticleAdjustcost3.png "Voorraadperioden in het scenario")</span><span class="sxs-lookup"><span data-stu-id="052a9-127">![Inventory periods in the scenario](media/helene/TechArticleAdjustcost3.png "Inventory periods in the scenario")</span></span>

 <span data-ttu-id="052a9-128">De eerste toegestane boekingsdatum is de eerste dag van de eerste open periode.</span><span class="sxs-lookup"><span data-stu-id="052a9-128">First allowed posting date is the first day in the first open period.</span></span> <span data-ttu-id="052a9-129">1 september 2013.</span><span class="sxs-lookup"><span data-stu-id="052a9-129">September 1, 2013.</span></span>  

 <span data-ttu-id="052a9-130">Grootboekinstellingen:</span><span class="sxs-lookup"><span data-stu-id="052a9-130">General Ledger Setup:</span></span>  

<span data-ttu-id="052a9-131">![Grootboekinstellingen in het scenario](media/helene/TechArticleAdjustcost4.png "Grootboekinstellingen in het scenario")</span><span class="sxs-lookup"><span data-stu-id="052a9-131">![G/L Setup in the scenario](media/helene/TechArticleAdjustcost4.png "G/L Setup in the scenario")</span></span>

 <span data-ttu-id="052a9-132">De eerste toegestane boekingsdatum is de datum in het veld Boeken toegest. vanaf: 10 september 2013.</span><span class="sxs-lookup"><span data-stu-id="052a9-132">First allowed posting date is the date stated in field Allow Posting From: September 10, 2013.</span></span>  

 <span data-ttu-id="052a9-133">Als zowel voorraadperioden als toegestane boekingsdatums in grootboekinstellingen zijn gedefinieerd, definieert de latere datum van de twee het toegestane boekingsdatumbereik.</span><span class="sxs-lookup"><span data-stu-id="052a9-133">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will define the allowed posting date range.</span></span>  

 <span data-ttu-id="052a9-134">Stap 3: Toewijzing van een toegestane boekingsdatum;</span><span class="sxs-lookup"><span data-stu-id="052a9-134">Step 3: Assignment of an allowed posting date;</span></span>  

 <span data-ttu-id="052a9-135">De aanvankelijke toegewezen Boekingsdatum was 6 september, zoals in stap 1 wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="052a9-135">The initial assigned Posting Date was September 6 as illustrated in step 1.</span></span> <span data-ttu-id="052a9-136">Echter, in de tweede stap identificeert de batchverwerking Kostprijs herwaarderen - Artikelposten dat de vroegste toegestane boekingsdatum 10 september is en wijst dus 10 september toe aan de herwaarderingswaardepost, onder.</span><span class="sxs-lookup"><span data-stu-id="052a9-136">However, in the second step the Adjust Cost – Item entries batch job identifies that earliest allowed Posting Date is September 10 and thereby assigns September 10 to the Adjustment Value Entry, below.</span></span>  

 <span data-ttu-id="052a9-137">![Status van waardeposten in scenario 2](media/helene/TechArticleAdjustcost5.png "Status van waardeposten in scenario 2")</span><span class="sxs-lookup"><span data-stu-id="052a9-137">![State of value entries in the scenario 2](media/helene/TechArticleAdjustcost5.png "State of value entries in the scenario 2")</span></span>

 <span data-ttu-id="052a9-138">We hebben nu het concept bekeken voor het toewijzen van Boekingsdatums aan waardeposten die worden gemaakt door de batchverwerking Kostprijs herwaarderen - Artikelposten.</span><span class="sxs-lookup"><span data-stu-id="052a9-138">We have now reviewed the concept for assigning Posting Dates to Value Entries created by the Adjust Cost - Item entries batch job.</span></span>  

 <span data-ttu-id="052a9-139">Laten we enkele scenario's bekijken die we in het ondersteuningsteam van tijd tot tijd tegenkomen in verband met toegewezen boekingsdatums in de batchverwerking Kostprijs herwaarderen - Artikelposten en gerelateerde instellingen.</span><span class="sxs-lookup"><span data-stu-id="052a9-139">Let’s continue to review some scenarios that we in the support team comes across from time to time in relation to assigned Posting Dates in the Adjust Cost – Item entries batch job and related setups.</span></span>  

## <a name="scenarios"></a><span data-ttu-id="052a9-140">Scenario's</span><span class="sxs-lookup"><span data-stu-id="052a9-140">Scenarios</span></span>  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a><span data-ttu-id="052a9-141">Scenario I: "De boekingsdatum ligt niet binnen het bereik van toegestane boekingsdatums."</span><span class="sxs-lookup"><span data-stu-id="052a9-141">Scenario I: “Posting Date is not within your range of allowed posting dates…”</span></span>  
 <span data-ttu-id="052a9-142">Dit is een scenario waarin een gebruiker het genoemde foutbericht krijgt wanneer de batchverwerking Kostprijs herwaarderen - Artikelposten wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="052a9-142">This is a scenario where a user is experiencing mentioned error message when the Adjust Cost – Item entries batch job is run.</span></span>  

 <span data-ttu-id="052a9-143">In de vorige sectie, waar het concept van het toewijzen van boekingsdatums wordt besproken, is het de bedoeling van de batchverwerking Kostprijs herwaarderen - Artikelposten een waardepost te maken met de boekingsdatum 10 september.</span><span class="sxs-lookup"><span data-stu-id="052a9-143">In the previous section, describing the concept of assigning posting dates, the intention of the Adjust Cost – Item entries batch job is to create a Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="052a9-144">![Foutbericht over boekingsdatum](media/helene/TechArticleAdjustcost6.png "Foutbericht over boekingsdatum")</span><span class="sxs-lookup"><span data-stu-id="052a9-144">![Error message about posting date](media/helene/TechArticleAdjustcost6.png "Error message about posting date")</span></span>

 <span data-ttu-id="052a9-145">We gaan door op de gebruikersinstelling:</span><span class="sxs-lookup"><span data-stu-id="052a9-145">We follow up on the User Setup:</span></span>  

<span data-ttu-id="052a9-146">![Instelling van toegestane boekingsdatums van gebruiker](media/helene/TechArticleAdjustcost7.png "Instelling van toegestane boekingsdatums van gebruiker")</span><span class="sxs-lookup"><span data-stu-id="052a9-146">![User's allowed posting dates setup](media/helene/TechArticleAdjustcost7.png "User's allowed posting dates setup")</span></span>

 <span data-ttu-id="052a9-147">De gebruiker heeft in dit geval een toegestane boekingsdatumreeks van 11 september tot 30 september en mag daardoor de herwaarderingswaardepost niet boeken met boekingsdatum 10 september.</span><span class="sxs-lookup"><span data-stu-id="052a9-147">The user in this case has an allowed posting date range from September 11 to September 30 and is thereby not allowed to post the Adjustment Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="052a9-148">![Overzicht van betrokken instelling van boekingsdatum](media/helene/TechArticleAdjustcost8.png "Overzicht van betrokken instelling van boekingsdatum")</span><span class="sxs-lookup"><span data-stu-id="052a9-148">![Overview of involved posting date setup](media/helene/TechArticleAdjustcost8.png "Overview of involved posting date setup")</span></span>

 <span data-ttu-id="052a9-149">Knowledge Base-artikel [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) bespreekt meer scenario's in verband met het genoemde foutbericht.</span><span class="sxs-lookup"><span data-stu-id="052a9-149">Knowledge Base article [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) discusses more scenarios related to mentioned error message.</span></span>  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a><span data-ttu-id="052a9-150">Scenario II: Boekingsdatum op Herwaarderingswaardepost versus Boekingsdatum op post die de correctie veroorzaakt, zoals Herwaardering of productie Artikeltoeslag.</span><span class="sxs-lookup"><span data-stu-id="052a9-150">Scenario II: Posting Date on Adjustment Value Entry versus Posting Date on entry causing the adjustment such as Revaluation or Item charge.</span></span>  

### <a name="revaluation-scenario"></a><span data-ttu-id="052a9-151">Herwaarderingsscenario:</span><span class="sxs-lookup"><span data-stu-id="052a9-151">Revaluation scenario:</span></span>  
 <span data-ttu-id="052a9-152">Vereisten:</span><span class="sxs-lookup"><span data-stu-id="052a9-152">Prerequisites:</span></span>  

 <span data-ttu-id="052a9-153">Voorraadinstelling:</span><span class="sxs-lookup"><span data-stu-id="052a9-153">Inventory setup:</span></span>  

-   <span data-ttu-id="052a9-154">Autom. voorraadwaarde boeken = Ja</span><span class="sxs-lookup"><span data-stu-id="052a9-154">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="052a9-155">Automatische kostenwaardering = Altijd</span><span class="sxs-lookup"><span data-stu-id="052a9-155">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="052a9-156">Gem. kostprijsberekeningsoort = artikel</span><span class="sxs-lookup"><span data-stu-id="052a9-156">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="052a9-157">Periode gemiddelde kostprijsberekening = Dag</span><span class="sxs-lookup"><span data-stu-id="052a9-157">Average Cost Period=Day</span></span>  

 <span data-ttu-id="052a9-158">Grootboekinstellingen:</span><span class="sxs-lookup"><span data-stu-id="052a9-158">General Ledger Setup:</span></span>  

-   <span data-ttu-id="052a9-159">Boeken toegest. vanaf = 1 januari 2014</span><span class="sxs-lookup"><span data-stu-id="052a9-159">Allow Posting From = January 1, 2014</span></span>  

-   <span data-ttu-id="052a9-160">Boeken toegest. tot = leeg</span><span class="sxs-lookup"><span data-stu-id="052a9-160">Allow Posting To = empty</span></span>  

 <span data-ttu-id="052a9-161">Gebruikersinstellingen:</span><span class="sxs-lookup"><span data-stu-id="052a9-161">User Setup:</span></span>  

-   <span data-ttu-id="052a9-162">Boeken toegest. vanaf = 1 december 2013.</span><span class="sxs-lookup"><span data-stu-id="052a9-162">Allow Posting From = December 1, 2013.</span></span>  

-   <span data-ttu-id="052a9-163">Boeken toegest. tot = leeg</span><span class="sxs-lookup"><span data-stu-id="052a9-163">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="052a9-164">Het scenario testen</span><span class="sxs-lookup"><span data-stu-id="052a9-164">To test the scenario</span></span>  

1.  <span data-ttu-id="052a9-165">ArtikelTEST maken:</span><span class="sxs-lookup"><span data-stu-id="052a9-165">Create item TEST:</span></span>  

     <span data-ttu-id="052a9-166">Basiseenheid = Stuks</span><span class="sxs-lookup"><span data-stu-id="052a9-166">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="052a9-167">Waarderingsmethode = Gemiddelde</span><span class="sxs-lookup"><span data-stu-id="052a9-167">Costing Method = Average</span></span>  

     <span data-ttu-id="052a9-168">Selecteer optionele boekingsgroepen.</span><span class="sxs-lookup"><span data-stu-id="052a9-168">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="052a9-169">Open artikeldagboek, maak en boek een regel als volgt:</span><span class="sxs-lookup"><span data-stu-id="052a9-169">Open Item Journal, create, and post a line as follows:</span></span>  

     <span data-ttu-id="052a9-170">Boekingsdatum = 15 december 2013</span><span class="sxs-lookup"><span data-stu-id="052a9-170">Posting Date = December 15, 2013</span></span>  

     <span data-ttu-id="052a9-171">Artikel = TEST</span><span class="sxs-lookup"><span data-stu-id="052a9-171">Item = TEST</span></span>  

     <span data-ttu-id="052a9-172">Boekingssoort = Inkoop</span><span class="sxs-lookup"><span data-stu-id="052a9-172">Entry Type = Purchase</span></span>  

     <span data-ttu-id="052a9-173">Aantal = 100</span><span class="sxs-lookup"><span data-stu-id="052a9-173">Quantity = 100</span></span>  

     <span data-ttu-id="052a9-174">Eenheidsprijs = 10</span><span class="sxs-lookup"><span data-stu-id="052a9-174">Unit Amount = 10</span></span>  

3.  <span data-ttu-id="052a9-175">Open artikeldagboek, maak en boek een regel als volgt:</span><span class="sxs-lookup"><span data-stu-id="052a9-175">Open Item Journal, create, and post a line as follows:</span></span>  

     <span data-ttu-id="052a9-176">Datum = 20 december 2013</span><span class="sxs-lookup"><span data-stu-id="052a9-176">Date = December 20, 2013</span></span>  

     <span data-ttu-id="052a9-177">Artikel = TEST</span><span class="sxs-lookup"><span data-stu-id="052a9-177">Item = TEST</span></span>  

     <span data-ttu-id="052a9-178">Boekingssoort = Negatieve herwaardering</span><span class="sxs-lookup"><span data-stu-id="052a9-178">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="052a9-179">Aantal = 2</span><span class="sxs-lookup"><span data-stu-id="052a9-179">Quantity = 2</span></span>  

4.  <span data-ttu-id="052a9-180">Open artikeldagboek, maak en boek een regel als volgt:</span><span class="sxs-lookup"><span data-stu-id="052a9-180">Open Item Journal, create, and post a line as follows:</span></span>  

     <span data-ttu-id="052a9-181">Datum = 15 januari 2014</span><span class="sxs-lookup"><span data-stu-id="052a9-181">Date = January 15, 2014</span></span>  

     <span data-ttu-id="052a9-182">Artikel = TEST</span><span class="sxs-lookup"><span data-stu-id="052a9-182">Item = TEST</span></span>  

     <span data-ttu-id="052a9-183">Boekingssoort = Negatieve herwaardering</span><span class="sxs-lookup"><span data-stu-id="052a9-183">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="052a9-184">Aantal = 3</span><span class="sxs-lookup"><span data-stu-id="052a9-184">Quantity = 3</span></span>  

5.  <span data-ttu-id="052a9-185">Open herwaarderingsdagboek, maak en boek een regel als volgt:</span><span class="sxs-lookup"><span data-stu-id="052a9-185">Open Revaluation Journal, create, and post a line as follows:</span></span>  

     <span data-ttu-id="052a9-186">Artikel = TEST</span><span class="sxs-lookup"><span data-stu-id="052a9-186">Item = TEST</span></span>  

     <span data-ttu-id="052a9-187">Vereffenen met post = selecteer inkooppost die is geboekt in stap 2.</span><span class="sxs-lookup"><span data-stu-id="052a9-187">Applies-to Entry = select Purchase entry posted at step 2.</span></span> <span data-ttu-id="052a9-188">De boekingsdatum van de herwaardering is dezelfde als van de post die wordt aangepast.</span><span class="sxs-lookup"><span data-stu-id="052a9-188">The Posting Date of the revaluation will be the same as the entry it adjusts.</span></span>  

     <span data-ttu-id="052a9-189">Kostprijs (Geherwaardeerd) = 40</span><span class="sxs-lookup"><span data-stu-id="052a9-189">Unit Cost Revalued = 40</span></span>  

 <span data-ttu-id="052a9-190">De volgende artikel- en waardeposten zijn geboekt:</span><span class="sxs-lookup"><span data-stu-id="052a9-190">The following Item Ledger and Value Entries have been posted:</span></span>  

<span data-ttu-id="052a9-191">![Overzicht van resulterende artikel- en waardeposten 1](media/helene/TechArticleAdjustcost9.png "Overzicht van resulterende artikel- en waardeposten 1")</span><span class="sxs-lookup"><span data-stu-id="052a9-191">![Overview of resulting item ledger and value entries 1](media/helene/TechArticleAdjustcost9.png "Overview of resulting item ledger and value entries 1")</span></span>

 <span data-ttu-id="052a9-192">![Overzicht van resulterende artikel- en waardeposten 2](media/helene/TechArticleAdjustcost10.png "Overzicht van resulterende artikel- en waardeposten 2")</span><span class="sxs-lookup"><span data-stu-id="052a9-192">![Overview of resulting item ledger and value entries 2](media/helene/TechArticleAdjustcost10.png "Overview of resulting item ledger and value entries 2")</span></span>

 <span data-ttu-id="052a9-193">De batchverwerking Kostprijs herwaarderen - Artikelposten heeft een wijziging in kosten herkend en de negatieve herwaarderingen aangepast.</span><span class="sxs-lookup"><span data-stu-id="052a9-193">The Adjust Cost – Item entries batch job has recognized a change in cost and adjusted the Negative Adjustments.</span></span>  

 <span data-ttu-id="052a9-194">**Controle van boekingsdatums in gemaakte herwaarderingswaardeposten:** de vroegste toegestane boekingsdatum waarop de batchverwerking Kostprijs herwaarderen - Artikelposten betrekking moet hebben is 1 januari 2014, zoals gesteld in de boekhoudinstellingen.</span><span class="sxs-lookup"><span data-stu-id="052a9-194">**Review of Posting Dates on created Adjustment Value Entries:** The earliest allowed Posting Date the Adjust Cost - Item Entries batch job has to relate to is January 1, 2014 as stated in the General Ledger Setup.</span></span>  

 <span data-ttu-id="052a9-195">**Negatieve herwaardering in stap 3:** toegewezen boekingsdatum is 1 januari, bepaald door boekhoudinstellingen.</span><span class="sxs-lookup"><span data-stu-id="052a9-195">**Negative Adjustment in step 3:** assigned Posting Date is January 1, provided by General Ledger Setup.</span></span> <span data-ttu-id="052a9-196">De boekingsdatum van de waardepost in het bereik voor herwaardering is 20 december 2013.</span><span class="sxs-lookup"><span data-stu-id="052a9-196">The Posting Date of the Value Entry in scope for adjustment is December 20, 2013.</span></span> <span data-ttu-id="052a9-197">Volgens de boekhoudinstellingen ligt de datum niet binnen het toegestane boekingsdatumbereik.</span><span class="sxs-lookup"><span data-stu-id="052a9-197">According to General Ledger Setup, the date is not within allowed posting date range.</span></span> <span data-ttu-id="052a9-198">Daarom wordt de boekingsdatum in het veld Boeken toegest. vanaf in de boekhoudinstellingen toegewezen aan de herwaarderingswaardepost.</span><span class="sxs-lookup"><span data-stu-id="052a9-198">Therefore the Posting Date stated in the Allow Posting From field in the General Ledger Setup is assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="052a9-199">**Negatieve herwaardering in stap 4:** toegewezen boekingsdatum is 15 januari.</span><span class="sxs-lookup"><span data-stu-id="052a9-199">**Negative Adjustment in step 4:** assigned Posting Date is January 15.</span></span> <span data-ttu-id="052a9-200">De waardepost in het bereik van herwaardering heeft boekingsdatum 15 januari, wat ligt binnen het toegestane boekingsdatumbereik, volgens de boekhoudinstellingen.</span><span class="sxs-lookup"><span data-stu-id="052a9-200">The Value Entry in scope of adjustment has Posting Date January 15, which is within the allowed posting date range according to General Ledger Setup.</span></span>  

 <span data-ttu-id="052a9-201">De herwaardering die wordt aangebracht voor de Negatieve herwaardering in stap 3 leidt tot discussie.</span><span class="sxs-lookup"><span data-stu-id="052a9-201">The adjustment made for the Negative Adjustment in step 3 causes discussion.</span></span> <span data-ttu-id="052a9-202">De gunstige boekingsdatum voor de herwaarderingswaardepost zou 20 december zijn of ten minste in december liggen aangezien de herwaardering die de wijziging in KPV heeft veroorzaakt, is geboekt in december.</span><span class="sxs-lookup"><span data-stu-id="052a9-202">The favorable Posting Date for the Adjustment Value Entry would have been December 20 or at least within December as the revaluation causing the change in COGS was posted in December.</span></span>  

 <span data-ttu-id="052a9-203">Om herwaardering in december te bereiken van de negatieve correctie in stap 3, moet het veld Boeken toegest. vanaf in de boekhoudinstellingen een datum in december bevatten.</span><span class="sxs-lookup"><span data-stu-id="052a9-203">To achieve adjustment in December of the Negative Adjustment in step 3, the General Ledger Setup, Allow Posting From field, need to state a date in December.</span></span>  

 <span data-ttu-id="052a9-204">**Conclusie:**</span><span class="sxs-lookup"><span data-stu-id="052a9-204">**Conclusion:**</span></span>  

 <span data-ttu-id="052a9-205">Overweeg met de ervaringen uit dit scenario de geschiktste instelling van toegestane boekingsdatumbereik voor een bedrijf. U kunt rekening houden met de volgende informatie: zo lang u toestaat dat wijzigingen in voorraadwaarde in een periode worden geboekt, december in dit geval, moet de instelling die het bedrijf gebruikt voor toegestane boekingsdatumbereiken, overeenstemmen met deze beslissing.</span><span class="sxs-lookup"><span data-stu-id="052a9-205">With the experiences from this scenario, considering most suitable setup of allowed posting date range for a company, you might want to consider the following information: As long as you allow changes in inventory value to be posted in a period, December in this case, the setup that the company uses for allowed posting date ranges should be aligned with this decision.</span></span> <span data-ttu-id="052a9-206">Het veld Boeken toegest. in de boekhoudinstellingen, dat 1 december bevat, zou toestaan dat de herwaardering die in december is aangebracht, wordt doorgestuurd naar betrokken uitgaande posten in dezelfde periode.</span><span class="sxs-lookup"><span data-stu-id="052a9-206">The Allow Posting From in the General Ledger Setup, stating December 1, would allow the revaluation made in December to be forwarded to affected outbound entries in the same period.</span></span>  

 <span data-ttu-id="052a9-207">Gebruikersgroepen die niet in december mogen boeken, maar in januari, een beperking die waarschijnlijk de bedoeling was van de boekhoudinstellingen in dit scenario, moeten in plaats daarvan worden geregeld met de gebruikersinstellingen.</span><span class="sxs-lookup"><span data-stu-id="052a9-207">User groups not allowed to post in December but in January, which was probably intended to be limited by the General Ledger Setup in this scenario, should instead be addressed via the User setup.</span></span>  

### <a name="item-charge-scenario"></a><span data-ttu-id="052a9-208">Artikeltoeslagscenario:</span><span class="sxs-lookup"><span data-stu-id="052a9-208">Item charge scenario:</span></span>  
 <span data-ttu-id="052a9-209">Vereisten:</span><span class="sxs-lookup"><span data-stu-id="052a9-209">Prerequisites:</span></span>  

 <span data-ttu-id="052a9-210">Voorraadinstelling:</span><span class="sxs-lookup"><span data-stu-id="052a9-210">Inventory setup:</span></span>  

-   <span data-ttu-id="052a9-211">Autom. voorraadwaarde boeken = Ja</span><span class="sxs-lookup"><span data-stu-id="052a9-211">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="052a9-212">Automatische kostenwaardering = Altijd</span><span class="sxs-lookup"><span data-stu-id="052a9-212">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="052a9-213">Gem. kostprijsberekeningsoort = artikel</span><span class="sxs-lookup"><span data-stu-id="052a9-213">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="052a9-214">Periode gemiddelde kostprijsberekening = Dag</span><span class="sxs-lookup"><span data-stu-id="052a9-214">Average Cost Period=Day</span></span>  

 <span data-ttu-id="052a9-215">Grootboekinstellingen:</span><span class="sxs-lookup"><span data-stu-id="052a9-215">General Ledger Setup:</span></span>  

-   <span data-ttu-id="052a9-216">Boeken toegest. vanaf = 1 december 2013.</span><span class="sxs-lookup"><span data-stu-id="052a9-216">Allow Posting From = December 1, 2013.</span></span>  

-   <span data-ttu-id="052a9-217">Boeken toegest. tot = leeg</span><span class="sxs-lookup"><span data-stu-id="052a9-217">Allow Posting To = empty</span></span>  

 <span data-ttu-id="052a9-218">Gebruikersinstellingen:</span><span class="sxs-lookup"><span data-stu-id="052a9-218">User Setup:</span></span>  

-   <span data-ttu-id="052a9-219">Boeken toegest. vanaf = 1 december 2013.</span><span class="sxs-lookup"><span data-stu-id="052a9-219">Allow Posting From = December 1, 2013.</span></span>  

-   <span data-ttu-id="052a9-220">Boeken toegest. tot = leeg</span><span class="sxs-lookup"><span data-stu-id="052a9-220">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="052a9-221">Het scenario testen</span><span class="sxs-lookup"><span data-stu-id="052a9-221">To test the scenario</span></span>  

1.  <span data-ttu-id="052a9-222">Artikeltoeslag maken:</span><span class="sxs-lookup"><span data-stu-id="052a9-222">Create item charge:</span></span>  

     <span data-ttu-id="052a9-223">Basiseenheid = Stuks</span><span class="sxs-lookup"><span data-stu-id="052a9-223">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="052a9-224">Waarderingsmethode = Gemiddelde</span><span class="sxs-lookup"><span data-stu-id="052a9-224">Costing Method = Average</span></span>  

     <span data-ttu-id="052a9-225">Selecteer optionele boekingsgroepen.</span><span class="sxs-lookup"><span data-stu-id="052a9-225">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="052a9-226">Nieuwe inkooporder maken</span><span class="sxs-lookup"><span data-stu-id="052a9-226">Create new purchase order</span></span>  

     <span data-ttu-id="052a9-227">Orderleveranciersnr.: 10000</span><span class="sxs-lookup"><span data-stu-id="052a9-227">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="052a9-228">Boekingsdatum = 15 december 2013</span><span class="sxs-lookup"><span data-stu-id="052a9-228">Posting Date = December 15, 2013</span></span>  

     <span data-ttu-id="052a9-229">Leveranciersfactuurnr.: 1234</span><span class="sxs-lookup"><span data-stu-id="052a9-229">Vendor Invoice No.: 1234</span></span>  

     <span data-ttu-id="052a9-230">Op de inkooporderregel:</span><span class="sxs-lookup"><span data-stu-id="052a9-230">On the purchase order line:</span></span>  

     <span data-ttu-id="052a9-231">Artikel = TOESLAG</span><span class="sxs-lookup"><span data-stu-id="052a9-231">Item = CHARGE</span></span>  

     <span data-ttu-id="052a9-232">Aantal = 1</span><span class="sxs-lookup"><span data-stu-id="052a9-232">Quantity = 1</span></span>  

     <span data-ttu-id="052a9-233">Directe kostprijs = 100</span><span class="sxs-lookup"><span data-stu-id="052a9-233">Direct Unit Cost = 100</span></span>  

     <span data-ttu-id="052a9-234">Ontvangst en factuur boeken.</span><span class="sxs-lookup"><span data-stu-id="052a9-234">Post Receive and Invoice.</span></span>  

3.  <span data-ttu-id="052a9-235">Nieuwe verkooporder maken:</span><span class="sxs-lookup"><span data-stu-id="052a9-235">Create new sales order:</span></span>  

     <span data-ttu-id="052a9-236">Orderklantnr.: 10000</span><span class="sxs-lookup"><span data-stu-id="052a9-236">Sell-to Customer No.: 10000</span></span>  

     <span data-ttu-id="052a9-237">Boekingsdatum = 16 december 2013</span><span class="sxs-lookup"><span data-stu-id="052a9-237">Posting Date = December 16, 2013</span></span>  

     <span data-ttu-id="052a9-238">Op de verkooporderregel:</span><span class="sxs-lookup"><span data-stu-id="052a9-238">On the sales order line:</span></span>  

     <span data-ttu-id="052a9-239">Artikel = TOESLAG</span><span class="sxs-lookup"><span data-stu-id="052a9-239">Item = CHARGE</span></span>  

     <span data-ttu-id="052a9-240">Aantal = 1</span><span class="sxs-lookup"><span data-stu-id="052a9-240">Quantity = 1</span></span>  

     <span data-ttu-id="052a9-241">Eenheidsprijs - 135</span><span class="sxs-lookup"><span data-stu-id="052a9-241">Unit Price = 135</span></span>  

     <span data-ttu-id="052a9-242">Verzenden en factureren boeken.</span><span class="sxs-lookup"><span data-stu-id="052a9-242">Post Ship and Invoice.</span></span>  

4.  <span data-ttu-id="052a9-243">Grootboekinstellingen:</span><span class="sxs-lookup"><span data-stu-id="052a9-243">General Ledger Setup:</span></span>  

     <span data-ttu-id="052a9-244">Boeken toegest. vanaf = 1 januari 2014</span><span class="sxs-lookup"><span data-stu-id="052a9-244">Allow Posting From = January 1, 2014</span></span>  

     <span data-ttu-id="052a9-245">Boeken toegest. tot = leeg</span><span class="sxs-lookup"><span data-stu-id="052a9-245">Allow Posting To = blank</span></span>  

5.  <span data-ttu-id="052a9-246">Nieuwe inkooporder maken:</span><span class="sxs-lookup"><span data-stu-id="052a9-246">Create new purchase order:</span></span>  

     <span data-ttu-id="052a9-247">Orderleveranciersnr.: 10000</span><span class="sxs-lookup"><span data-stu-id="052a9-247">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="052a9-248">Boekingsdatum = 2 januari 2014</span><span class="sxs-lookup"><span data-stu-id="052a9-248">Posting Date = January 2, 2014</span></span>  

     <span data-ttu-id="052a9-249">Leveranciersfactuurnr.: 2345</span><span class="sxs-lookup"><span data-stu-id="052a9-249">Vendor Invoice No.: 2345</span></span>  

     <span data-ttu-id="052a9-250">Op de inkooporderregel:</span><span class="sxs-lookup"><span data-stu-id="052a9-250">On the purchase order line:</span></span>  

     <span data-ttu-id="052a9-251">Artikeltoeslag = JB-VRACHT</span><span class="sxs-lookup"><span data-stu-id="052a9-251">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="052a9-252">Aantal = 1</span><span class="sxs-lookup"><span data-stu-id="052a9-252">Quantity = 1</span></span>  

     <span data-ttu-id="052a9-253">Directe kostprijs = 3</span><span class="sxs-lookup"><span data-stu-id="052a9-253">Direct Unit Cost = 3</span></span>  

     <span data-ttu-id="052a9-254">Wijs artikeltoeslag toe aan inkoopontvangst uit stap 2.</span><span class="sxs-lookup"><span data-stu-id="052a9-254">Assign Item Charge to Purchase Receipt from step 2.</span></span>  

     <span data-ttu-id="052a9-255">Ontvangst en factuur boeken.</span><span class="sxs-lookup"><span data-stu-id="052a9-255">Post Receipt and Invoice.</span></span>  

     <span data-ttu-id="052a9-256">![Overzicht van resulterende artikel- en waardeposten 3](media/helene/TechArticleAdjustcost11.png "Overzicht van resulterende artikel- en waardeposten 3")</span><span class="sxs-lookup"><span data-stu-id="052a9-256">![Overview of resulting item ledger and value entries 3](media/helene/TechArticleAdjustcost11.png "Overview of resulting item ledger and value entries 3")</span></span>

6.  <span data-ttu-id="052a9-257">Op werkdatum 3 januari arriveert een inkoopfactuur met een aanvullende artikeltoeslag bovenop de inkoop die in stap 2 is gedaan.</span><span class="sxs-lookup"><span data-stu-id="052a9-257">On work date January 3, a purchase invoice arrives, containing an additional item charge to the purchase made in step 2.</span></span> <span data-ttu-id="052a9-258">Deze factuur heeft documentdatum 30 december en is dus geboekt met boekingsdatum 30 december 2013.</span><span class="sxs-lookup"><span data-stu-id="052a9-258">This invoice has document date December 30 and is therefore posted with Posting Date December 30, 2013.</span></span>  

     <span data-ttu-id="052a9-259">Nieuwe inkooporder maken:</span><span class="sxs-lookup"><span data-stu-id="052a9-259">Create new purchase order:</span></span>  

     <span data-ttu-id="052a9-260">Orderleveranciersnr.: 10000</span><span class="sxs-lookup"><span data-stu-id="052a9-260">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="052a9-261">Boekingsdatum = 30 december 2013</span><span class="sxs-lookup"><span data-stu-id="052a9-261">Posting Date = December 30, 2013</span></span>  

     <span data-ttu-id="052a9-262">Leveranciersfactuurnr.: 3456</span><span class="sxs-lookup"><span data-stu-id="052a9-262">Vendor Invoice No.: 3456</span></span>  

     <span data-ttu-id="052a9-263">Op de inkooporderregel:</span><span class="sxs-lookup"><span data-stu-id="052a9-263">On the purchase order line:</span></span>  

     <span data-ttu-id="052a9-264">Artikeltoeslag = JB-VRACHT</span><span class="sxs-lookup"><span data-stu-id="052a9-264">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="052a9-265">Aantal = 1</span><span class="sxs-lookup"><span data-stu-id="052a9-265">Quantity = 1</span></span>  

     <span data-ttu-id="052a9-266">Directe kostprijs = 2</span><span class="sxs-lookup"><span data-stu-id="052a9-266">Direct Unit Cost = 2</span></span>  

     <span data-ttu-id="052a9-267">Wijs artikeltoeslag toe aan inkoopontvangst uit stap 2</span><span class="sxs-lookup"><span data-stu-id="052a9-267">Assign Item Charge to Purchase Receipt from step 2</span></span>  

     <span data-ttu-id="052a9-268">Ontvangst en factuur boeken.</span><span class="sxs-lookup"><span data-stu-id="052a9-268">Post Receipt and Invoice.</span></span>  

   <span data-ttu-id="052a9-269">![Overzicht van resulterende artikel- en waardeposten 4](media/helene/TechArticleAdjustcost12.png "Overzicht van resulterende artikel- en waardeposten 4")</span><span class="sxs-lookup"><span data-stu-id="052a9-269">![Overview of resulting item ledger and value entries 4](media/helene/TechArticleAdjustcost12.png "Overview of resulting item ledger and value entries 4")</span></span>

 <span data-ttu-id="052a9-270">Het rapport Voorraadwaardering wordt afgedrukt vanaf 31 december 2013</span><span class="sxs-lookup"><span data-stu-id="052a9-270">Inventory Valuation report is printed as of Date December 31 , 2013</span></span>  

<span data-ttu-id="052a9-271">![Inhoud van het voorraadwaarderingsrapport](media/helene/TechArticleAdjustcost13.png "Inhoud van het voorraadwaarderingsrapport")</span><span class="sxs-lookup"><span data-stu-id="052a9-271">![Content of the Inventory Valuation report](media/helene/TechArticleAdjustcost13.png "Content of the Inventory Valuation report")</span></span>

 <span data-ttu-id="052a9-272">**Overzicht van scenario:**</span><span class="sxs-lookup"><span data-stu-id="052a9-272">**Summary of scenario:**</span></span>  

 <span data-ttu-id="052a9-273">Het beschreven scenario eindigt met een rapport Voorraadwaardering dat Aantal = 0 aangeeft terwijl de waarde = 2.</span><span class="sxs-lookup"><span data-stu-id="052a9-273">The described scenario ends up with an Inventory Valuation report demonstrating Quantity = 0 while the Value = 2.</span></span> <span data-ttu-id="052a9-274">De artikeltoeslag die in stap 11 is geboekt, maakt deel uit van de positieve voorraadmutatiewaarde van december terwijl de negatieve voorraadmutatie van dezelfde periode niet wordt beïnvloed.</span><span class="sxs-lookup"><span data-stu-id="052a9-274">The Item charge posted in step 11 is part of the Inventory Increase value of December while the Inventory Decrease of the same period is not affected.</span></span>  

 <span data-ttu-id="052a9-275">Dat de boekhoudinstellingen Boeken toegest. vanaf 1 januari aangeven, was goed voor de eerste artikeltoeslag.</span><span class="sxs-lookup"><span data-stu-id="052a9-275">Having the General Ledger Setup stating Allow Posting From January 1 was a good thing for the first Item charge.</span></span> <span data-ttu-id="052a9-276">De kosten van de positieve en de negatieve voorraadmutatie zijn in dezelfde periode vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="052a9-276">The costs of the Inventory Increase and Decrease was recorded in the same period.</span></span> <span data-ttu-id="052a9-277">Voor de tweede artikeltoeslag leiden de boekhoudinstellingen er echter toe dat de wijziging in COGS in de volgende periode wordt herkend.</span><span class="sxs-lookup"><span data-stu-id="052a9-277">For the second Item charge however, the General Ledger Setup causes the change in COGS to be recognized in the period after.</span></span>  

 <span data-ttu-id="052a9-278">**Conclusie:**</span><span class="sxs-lookup"><span data-stu-id="052a9-278">**Conclusion:**</span></span>  

 <span data-ttu-id="052a9-279">Het is een uitdaging om het rapport Voorraadwaardering Aantal = 0 aan te laten geven terwijl de Waarde <> 0.</span><span class="sxs-lookup"><span data-stu-id="052a9-279">It’s a challenge to have the Inventory Valuation report to demonstrate Quantity = 0 while the Value <> 0.</span></span> <span data-ttu-id="052a9-280">In dat geval is het ook moeilijker de optimale instellingen aan te geven, wanneer inkoopfacturen op dezelfde dag arriveren, maar verschillende perioden of zelfs boekjaren betreffen.</span><span class="sxs-lookup"><span data-stu-id="052a9-280">In this case it’s also more difficult to express the optimal settings, having purchase invoices arriving the same day but addressing different periods or even fiscal years.</span></span> <span data-ttu-id="052a9-281">De overgang naar een nieuw boekjaar vereist meestal enige planning en als onderdeel daarvan moet het proces Kostprijs herwaarderen - Artikelposten, rekening houdend met COGS, worden overwogen.</span><span class="sxs-lookup"><span data-stu-id="052a9-281">Crossing to a new fiscal year usually requires some planning and as part of that the insight of Adjust Cost – Item entries process, recognizing COGS, is to be considered.</span></span>  

 <span data-ttu-id="052a9-282">In dit scenario zou één scenario kunnen zijn het veld Boekhoudinstellingen, Boeken toegest. vanaf voor enkele dagen een datum in december te geven en de boeking van de eerste artikeltoeslag uit te stellen om mogelijk te maken dat alle kosten voor de vorige periode/boekjaar eerst worden herkend voor de periode waartoe ze behoren, de batchverwerking Kosten herwaarderen - Artikelposten uit te voeren en daarna de toegestane boekingsdatum te verplaatsen naar de nieuwe periode\/boekjaar.</span><span class="sxs-lookup"><span data-stu-id="052a9-282">In this scenario one option could have been to have the General Ledger Setup, field Allow Posting From, stating a date in December for a couple of more days and the posting of the first item charge postponed to allow all costs for the previous period/fiscal year to be recognized for the period they belong to first, having the Adjust Cost – Item entries batch job run and thereafter move the allowed posting date to the new period\/fiscal year.</span></span> <span data-ttu-id="052a9-283">De eerste artikeltoeslag met boekingsdatum 2 januari kan dan worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="052a9-283">The first item charge with posting date January 2 could then be posted.</span></span>  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a><span data-ttu-id="052a9-284">Historie van batchverwerking Kostprijs herwaarderen - Artikelposten</span><span class="sxs-lookup"><span data-stu-id="052a9-284">History of Adjust Cost – Item entries batch job</span></span>  
 <span data-ttu-id="052a9-285">Hieronder vindt u een overzicht van het concept boekingsdatums toewijzen aan herwaarderingswaardeposten door de batchverwerking Kostprijs herwaarderen - Artikelposten.</span><span class="sxs-lookup"><span data-stu-id="052a9-285">Below is a summary of the concept assigning Posting Dates to Adjustment Value Entries by the Adjust Cost – Item entries batch job.</span></span>  

### <a name="about-the-request-form-posting-date"></a><span data-ttu-id="052a9-286">Over de boekingsdatum van het aanvraagformulier:</span><span class="sxs-lookup"><span data-stu-id="052a9-286">About the request form posting date:</span></span>  
 <span data-ttu-id="052a9-287">Er hoeft geen boekingsdatum meer te worden vermeld in het aanvraagformulier van de batchverwerking Kostprijs herwaarderen - Artikelposten.</span><span class="sxs-lookup"><span data-stu-id="052a9-287">There is no longer a posting date to be stated in the request form of the Adjust Cost - Item entries batch job.</span></span> <span data-ttu-id="052a9-288">De batchverwerking doorloopt alle benodigde wijzigingen en maakt waardeposten met de boekingsdatum van de waardepost die wordt geherwaardeerd.</span><span class="sxs-lookup"><span data-stu-id="052a9-288">The batch job runs through all necessary changes and creates value entries with the posting date of the value entry it adjusts.</span></span> <span data-ttu-id="052a9-289">Als de boekingsdatum niet binnen het toegestane boekingsdatumbereik ligt, wordt de boekingsdatum in het veld Boeken toegest. vanaf in de boekhoudinstellingen gebruikt, OF als de voorraadperioden worden gebruikt, wordt de laatste datum van de twee gebruikt.</span><span class="sxs-lookup"><span data-stu-id="052a9-289">If the posting date is not within allowed posting date range the posting date in the Allow Posting From field in the General Ledger Setup, OR if the Inventory periods are used, the later date of the two will be used.</span></span> <span data-ttu-id="052a9-290">Zie hierboven beschreven concept.</span><span class="sxs-lookup"><span data-stu-id="052a9-290">See described concept above.</span></span>  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a><span data-ttu-id="052a9-291">Historie van batchverwerking Voorraadwaarde boeken.</span><span class="sxs-lookup"><span data-stu-id="052a9-291">History of Post Inventory cost to G/L batch job</span></span>  
 <span data-ttu-id="052a9-292">De batchverwerking Voorraadwaarde boeken is nauw verbonden met de batchverwerking Kostprijs herwaarderen - Artikelposten. Daarom wordt de historie van deze batchverwerking hier ook samengevat en gedeeld.</span><span class="sxs-lookup"><span data-stu-id="052a9-292">The Post Inventory Cost to G/L batch job is closely related to the Adjust Cost – Item entries batch job why the history of this batch job is summarized and shared here as well.</span></span>  
 
<span data-ttu-id="052a9-293">![Werkelijke kosten versus verwachte kosten](media/helene/TechArticleAdjustcost14.png "Werkelijke kosten versus verwachte kosten")</span><span class="sxs-lookup"><span data-stu-id="052a9-293">![Actual cost versus expected cost](media/helene/TechArticleAdjustcost14.png "Actual cost versus expected cost")</span></span>

### <a name="about-the-posting-date"></a><span data-ttu-id="052a9-294">Over de boekingsdatum</span><span class="sxs-lookup"><span data-stu-id="052a9-294">About the posting date</span></span>
 <span data-ttu-id="052a9-295">Er hoeft geen boekingsdatum meer te worden vermeld in het aanvraagformulier van de batchverwerking Voorraadwaarde boeken.</span><span class="sxs-lookup"><span data-stu-id="052a9-295">There is no longer a posting date to be stated in the request form of the Post Inventory Cost to G/L batch job.</span></span> <span data-ttu-id="052a9-296">De grootboekpost wordt gemaakt met dezelfde boekingsdatum als de gerelateerde waardepost.</span><span class="sxs-lookup"><span data-stu-id="052a9-296">The G/L entry is created with the same Posting Date as the related value entry.</span></span> <span data-ttu-id="052a9-297">Als u de batchverwerking wilt voltooien, moet het toegestane boekingsdatumbereik de boekingsdatum van de gemaakte grootboekpost toestaan.</span><span class="sxs-lookup"><span data-stu-id="052a9-297">In order to complete the batch job, the allowed posting date range must allow the Posting Date of the created G/L entry.</span></span> <span data-ttu-id="052a9-298">Als dit niet het geval is, moet de toegestane boekingsdatumreeks tijdelijk opnieuw worden geopend door de datums in het veld Boeken toegest. vanaf en tot in Boekhoudinstellingen te wijzigen of te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="052a9-298">If not, the allowed posting date range must be temporarily reopened by changing or removing the dates in the Allow Posting From and To fields in the General Ledger Setup.</span></span> <span data-ttu-id="052a9-299">Om reconciliatieproblemen te voorkomen is het vereist dat de boekingsdatum van de grootboekpost correspondeert met de boekingsdatum van de waardepost.</span><span class="sxs-lookup"><span data-stu-id="052a9-299">To avoid reconciliation issues, it is required that Posting Date of the G/L Entry corresponds to the Posting Date of the Value Entry.</span></span>  

 <span data-ttu-id="052a9-300">De batchverwerking scant tabel 5811 - Waardepost naar GB boeken om de waardeposten te bepalen in het bereik voor boeking naar het grootboek.</span><span class="sxs-lookup"><span data-stu-id="052a9-300">The batch job scans Table 5811 - Post Value Entry to G/L, to identify the Value Entries in scope for posting to General Ledger.</span></span> <span data-ttu-id="052a9-301">Na een succesvolle uitvoering wordt de tabel geleegd.</span><span class="sxs-lookup"><span data-stu-id="052a9-301">After a successful run, the table is emptied.</span></span>

## <a name="see-also"></a><span data-ttu-id="052a9-302">Zie ook</span><span class="sxs-lookup"><span data-stu-id="052a9-302">See Also</span></span>  
[<span data-ttu-id="052a9-303">Ontwerpdetails: Voorraadwaardering</span><span class="sxs-lookup"><span data-stu-id="052a9-303">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)  
[<span data-ttu-id="052a9-304">Ontwerpdetails: Artikelvereffening</span><span class="sxs-lookup"><span data-stu-id="052a9-304">Design Details: Item Application</span></span>](design-details-item-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
