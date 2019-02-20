---
title: Aanvullende valuta's instellen | Microsoft Docs
description: Uw grootboek is ingesteld om uw lokale valuta (LV) te gebruiken en er is een andere valuta ingesteld als aanvullende valuta, waaraan een huidige wisselkoers is toegewezen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 01/07/2019
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: a98027c3ef3171491f84197897f93cbed4e288c2
ms.openlocfilehash: 294ed8019b12287e4b4ad59d46e842e4022a637f
ms.contentlocale: nl-be
ms.lasthandoff: 01/07/2019

---
# <a name="set-up-an-additional-reporting-currency"></a><span data-ttu-id="ebf9d-103">Een extra rapportagevaluta instellen.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-103">Set Up an Additional Reporting Currency</span></span>
<span data-ttu-id="ebf9d-104">Aangezien bedrijven steeds vaker in andere landen/regio's opereren, is het belangrijk dat zij de financiële gegevens in meer dan één valuta kunnen controleren en rapporteren.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-104">As companies operate in increasingly more countries/regions, it becomes more important that they are able to review and report financial data in more than one currency.</span></span>

<span data-ttu-id="ebf9d-105">Uw grootboek is ingesteld om uw lokale valuta (LV) te gebruiken, maar u kunt het ook instellen om een andere valuta te gebruiken, waaraan een huidige wisselkoers is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-105">Your general ledger is set up to use your local currency (LCY), but you can set it up to also use another currency with a current exchange rate assigned.</span></span> <span data-ttu-id="ebf9d-106">Door een tweede valuta in te stellen als een zogenaamde aanvullende rapportagevaluta, legt [!INCLUDE[d365fin](includes/d365fin_md.md)] bedragen automatisch vast in zowel de LV als deze aanvullende rapportagevaluta voor elke grootboekpost en andere posten, zoals btw-posten.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-106">By designating a second currency as a so-called additional reporting currency, [!INCLUDE[d365fin](includes/d365fin_md.md)] will automatically record amounts in both LCY and this additional reporting currency on each G/L entry and other entries, such as VAT entries.</span></span>

> [!Warning]
> <span data-ttu-id="ebf9d-107">De functie Extra rapportagevaluta mag niet worden gebruikt als basis voor de vertaling van een financieel overzicht.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-107">The Additional Reporting Currency functionality should not be used as a basis for financial statement translation.</span></span> <span data-ttu-id="ebf9d-108">Het is geen programma dat een vertaling kan uitvoeren van financiële overzichten van buitenlandse dochterondernemingen als onderdeel van een bedrijfsconsolidatie.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-108">It is not a tool that can perform translation of foreign subsidiary financial statements as part of a company consolidation.</span></span> <span data-ttu-id="ebf9d-109">De extra rapportagevalutafunctie kan alleen worden gebruikt om rapporten in een andere valuta voor te bereiden, alsof die valuta de lokale valuta van het bedrijf was.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-109">The additional reporting currency can only be used to prepare reports in another currency, as if that currency was the company’s local currency.</span></span>

## <a name="displaying-reports-and-amounts-in-the-additional-reporting-currency"></a><span data-ttu-id="ebf9d-110">Rapporten en bedragen weergeven in de extra rapportagevaluta</span><span class="sxs-lookup"><span data-stu-id="ebf9d-110">Displaying Reports and Amounts in the Additional Reporting Currency</span></span>
<span data-ttu-id="ebf9d-111">Het gebruik van een extra rapportagevaluta kan in de volgende gevallen hulp bieden bij het rapportageproces voor een bedrijf:</span><span class="sxs-lookup"><span data-stu-id="ebf9d-111">Using an additional reporting currency can assist the reporting process for a company in the following cases:</span></span>

- <span data-ttu-id="ebf9d-112">Bedrijven in landen/regio's die niet bij de EU horen en die grote hoeveelheden transacties aangaan met bedrijven in EU-landen/regio's.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-112">Companies in non-EU countries/regions that have a high proportion of transactions with EU country/region companies.</span></span> <span data-ttu-id="ebf9d-113">In dit geval wil het bedrijf buiten de EU mogelijk tevens in euro rapporteren om de financiële rapporten beter bruikbaar te maken voor handelspartners in de EU.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-113">In this case, the non-EU company may also wish to report in euro to make its financial reports more usable for EU trade partners.</span></span>
- <span data-ttu-id="ebf9d-114">Bedrijven die tevens rapporten in een internationale handelsvaluta in plaats van hun eigen lokale valuta willen weergeven.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-114">Companies that also wish to display reports in a more internationally traded currency than their own local currency.</span></span>

<span data-ttu-id="ebf9d-115">Verschillende financiële rapporten worden gebaseerd op grootboekposten.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-115">Several financial reports are based on G/L entries.</span></span> <span data-ttu-id="ebf9d-116">Als u rapportgegevens in de extra rapportagevaluta wilt weergeven, plaatst u eenvoudigweg een vinkje in het veld **Bedragen in rapp.-valuta weergeven** van het sneltabblad **Opties** voor het betreffende grootboekrapport.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-116">To display report data in the additional reporting currency, you simply place a check mark in the **Show Amounts in Add. Reporting Currency** field on the **Options** FastTab for the relevant G/L report.</span></span>

## <a name="adjusting-exchange-rates"></a><span data-ttu-id="ebf9d-117">Wisselkoersen corrigeren</span><span class="sxs-lookup"><span data-stu-id="ebf9d-117">Adjusting Exchange Rates</span></span>
<span data-ttu-id="ebf9d-118">Aangezien valutakoersen constant wisselen, moeten de extra valuta-equivalenten in uw systeem periodiek worden gecorrigeerd.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-118">Because exchange rates fluctuate constantly, additional currency equivalents in your system must be adjusted periodically.</span></span> <span data-ttu-id="ebf9d-119">Als deze correcties niet worden uitgevoerd, kunnen de bedragen die omgerekend zijn van vreemde (of extra) valuta's en geboekt zijn in het grootboek in LV misleidend zijn.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-119">If these adjustments are not done, amounts that have been converted from foreign (or additional) currencies and posted to the general ledger in LCY may be misleading.</span></span> <span data-ttu-id="ebf9d-120">Bovendien moeten dagelijkse posten die geboekt zijn doordat een dagwisselkoers is ingevoerd in het programma worden bijgewerkt nadat de dagwisselkoersgegevens zijn ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-120">In addition, daily entries posted before a daily exchange rate is entered into the program must be updated after the daily exchange rate information is entered.</span></span> <span data-ttu-id="ebf9d-121">De batchverwerking **Wisselkoers herwaarderen** wordt gebruikt om de wisselkoersen van de geboekte klant, leverancier en bankrekeningposten te corrigeren.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-121">The **Adjust Exchange Rates** batch job is used to adjust the exchange rates of posted customer, vendor and bank account entries.</span></span> <span data-ttu-id="ebf9d-122">U kunt er tevens extra rapportagevalutabedragen in grootboekposten mee bijwerken.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-122">It can also update additional reporting currency amounts on G/L entries.</span></span> <span data-ttu-id="ebf9d-123">Zie voor meer informatie [Valutawisselkoersen bijwerken](finance-how-update-currencies.md).</span><span class="sxs-lookup"><span data-stu-id="ebf9d-123">For more information, see [Update Currency Exchange Rates](finance-how-update-currencies.md).</span></span>

## <a name="setting-up-an-additional-reporting-currency"></a><span data-ttu-id="ebf9d-124">Een extra rapportagevaluta instellen</span><span class="sxs-lookup"><span data-stu-id="ebf9d-124">Setting Up an Additional Reporting Currency</span></span>
<span data-ttu-id="ebf9d-125">Volg deze stappen om een extra rapportagevaluta in te stellen:</span><span class="sxs-lookup"><span data-stu-id="ebf9d-125">To set up an additional reporting currency, you must follow these steps:</span></span>

-   <span data-ttu-id="ebf9d-126">Geef grootboekrekeningen op voor het boeken van wisselkoerscorrecties.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-126">Specify general ledger accounts for posting exchange rate adjustments.</span></span>  
-   <span data-ttu-id="ebf9d-127">Geef de wisselkoerscorrectiemethode op voor alle grootboekrekeningen.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-127">Specify the exchange rate adjustment method for all general ledger accounts.</span></span>  
-   <span data-ttu-id="ebf9d-128">Geef de wisselkoersherwaarderingsmethode op voor btw-boekingen.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-128">Specify the exchange rate adjustment method for VAT entries.</span></span>  
-   <span data-ttu-id="ebf9d-129">Activeer de extra rapportagevaluta.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-129">Activate the additional reporting currency.</span></span>  

### <a name="to-specify-general-ledger-accounts-for-posting-exchange-rate-adjustments"></a><span data-ttu-id="ebf9d-130">Grootboekrekeningen opgeven voor het boeken van wisselkoerscorrecties</span><span class="sxs-lookup"><span data-stu-id="ebf9d-130">To specify general ledger accounts for posting exchange rate adjustments</span></span>  

1. <span data-ttu-id="ebf9d-131">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Valuta's** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Currencies**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ebf9d-132">Vul op de pagina **Valuta's** de volgende velden in voor de extra rapportagevaluta.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-132">On the **Currencies** page, fill in the following fields for the additional reporting currency.</span></span>  

|<span data-ttu-id="ebf9d-133">Veld</span><span class="sxs-lookup"><span data-stu-id="ebf9d-133">Field</span></span>|<span data-ttu-id="ebf9d-134">Description</span><span class="sxs-lookup"><span data-stu-id="ebf9d-134">Description</span></span>|  
|---------------------------------|---------------------------------------|  
|<span data-ttu-id="ebf9d-135">**Gereal. grootboekwinstrek.**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-135">**Realized GL Gains Account**</span></span>|<span data-ttu-id="ebf9d-136">De grootboekrekening waarnaar wisselkoerswinsten worden geboekt bij valutaherwaarderingen van de lokale valuta en de rapportagevaluta.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-136">The general ledger account to which exchange rate gains for currency adjustments between LCY and the additional reporting currency will be posted.</span></span>|  
|<span data-ttu-id="ebf9d-137">**Gereal. grootboekverliesrek.**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-137">**Realized GL Losses Account**</span></span>|<span data-ttu-id="ebf9d-138">De grootboekrekening waarnaar wisselkoersverliezen worden geboekt bij valutaherwaarderingen van de lokale valuta en de rapportagevaluta.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-138">The general ledger account to which exchange rate losses for currency adjustments between LCY and the additional reporting currency will be posted.</span></span>|  
|<span data-ttu-id="ebf9d-139">**Verschillenrekening (Winst)**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-139">**Residual Gains Account**</span></span>|<span data-ttu-id="ebf9d-140">De grootboekrekening waarnaar verschilbedragen (winst) worden geboekt als u in de lokale valuta en de rapportagevaluta boekingen uitvoert in de module Financieel.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-140">The general ledger account to which residual amounts that are gains are posted if you post in the general ledger application area in both LCY and an additional reporting currency.</span></span>|  
|<span data-ttu-id="ebf9d-141">**Verschillenrekening (Verlies)**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-141">**Residual Losses Account**</span></span>|<span data-ttu-id="ebf9d-142">De grootboekrekening waarnaar verschilbedragen (verlies) worden geboekt als u in de lokale valuta en de rapportagevaluta boekingen uitvoert in de module Financieel.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-142">The general ledger account to which residual amounts that are losses are posted if you post in the general ledger application area in both LCY and an additional reporting currency.</span></span>|

> [!NOTE]  
>  <span data-ttu-id="ebf9d-143">Verschillenbedragen kunnen ontstaan wanneer [!INCLUDE[d365fin](includes/d365fin_md.md)] debet- en creditbedragen afrondt die omgerekend zijn van de LV naar een extra rapportagevaluta.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-143">Residual amounts can occur when [!INCLUDE[d365fin](includes/d365fin_md.md)] rounds debit and credit amounts that have been converted from LCY to an additional reporting currency.</span></span>  

<span data-ttu-id="ebf9d-144">U moet voor elke grootboekrekening opgeven hoe grootboekbedragen voor die rekening worden gecorrigeerd bij wisselkoersschommelingen tussen de LV en de extra rapportagevaluta.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-144">For each general ledger account, you must specify how general ledger amounts for that account will be adjusted for exchange rate fluctuations between LCY and the additional reporting currency.</span></span>  

### <a name="to-specify-the-exchange-rate-adjustment-method-for-all-general-ledger-accounts"></a><span data-ttu-id="ebf9d-145">De wisselkoerscorrectiemethode opgeven voor alle grootboekrekeningen</span><span class="sxs-lookup"><span data-stu-id="ebf9d-145">To specify the exchange rate adjustment method for all general ledger accounts</span></span>  
1. <span data-ttu-id="ebf9d-146">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-146">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ebf9d-147">Selecteer op de pagina **Rekeningschema** de relevante rekening en kies de actie **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-147">On the **Chart of Accounts** page, select the relevant account, and then choose the **Edit** action.</span></span>  
3. <span data-ttu-id="ebf9d-148">Selecteer op de pagina **Grootboekrekening** de relevante methode in het veld **Wisselkoersherwaardering**.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-148">On the **GL Account Card** page, select the relevant method in the **Exchange Rate Adjustment** field.</span></span>  

    <span data-ttu-id="ebf9d-149">Als u in een extra rapportagevaluta boekt, geeft u in het veld **Wisselkoersherwaardering** aan hoe deze grootboekrekening wordt gecorrigeerd bij wisselkoersschommelingen tussen de LV en de extra rapportagevaluta.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-149">If you post in an additional reporting currency, specify in the **Exchange Rate Adjustment** field how this general ledger account will be adjusted for exchange-rate fluctuations between LCY and the additional reporting currency.</span></span> <span data-ttu-id="ebf9d-150">De volgende tabel bevat de opties waaruit u kunt kiezen.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-150">The following table shows the options to choose from.</span></span>  

    |<span data-ttu-id="ebf9d-151">Veld</span><span class="sxs-lookup"><span data-stu-id="ebf9d-151">Field</span></span>|<span data-ttu-id="ebf9d-152">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ebf9d-152">Decription</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="ebf9d-153">**Geen**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-153">**No Adjustment**</span></span>|<span data-ttu-id="ebf9d-154">Er wordt geen wisselkoersherwaardering uitgevoerd op de grootboekrekening.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-154">No exchange rate adjustment is made to the general ledger account.</span></span> <span data-ttu-id="ebf9d-155">Dit is de standaardwaarde.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-155">This is the default option.</span></span><br /><br /> <span data-ttu-id="ebf9d-156">**OPMERKING:** Deze optie moet altijd zijn geselecteerd als de wisselkoers tussen het LV en de extra rapportagevaluta altijd vast is.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-156">**NOTE:** This option should be selected if the exchange rate between the LCY and additional reporting currency is always fixed.</span></span>|  
    |<span data-ttu-id="ebf9d-157">**Bedrag**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-157">**Adjust Amount**</span></span>|<span data-ttu-id="ebf9d-158">Het bedrag in LV is aangepast voor eventuele wisselkoerswinsten of -verliezen.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-158">The LCY amount is adjusted for any exchange rate gains or losses.</span></span> <span data-ttu-id="ebf9d-159">Wisselkoerswinsten of -verliezen worden geboekt naar de grootboekrekening in het veld **Bedrag** en de rekeningen die u hebt gespecificeerd voor winsten of verliezen in de velden **Gereal. grootbk.-winstrek.** en **Gereal. grootbk.-verliesrek.** op de pagina **Valuta's**.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-159">Exchange rate gains or losses are posted to the general ledger account in the **Amount** field and to the accounts you specified for gains or losses in the **Realized G/L Gains Account** and **Realized G/L Losses Account** fields on the **Currencies** page.</span></span>|  
    |<span data-ttu-id="ebf9d-160">**Bedrag (Rapp.-val.)**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-160">**Adjust Additional-Currency Amount**</span></span>|<span data-ttu-id="ebf9d-161">De extra rapportagevaluta is aangepast voor eventuele wisselkoerswinsten of -verliezen.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-161">The additional reporting currency is adjusted for any exchange rate gains or losses.</span></span> <span data-ttu-id="ebf9d-162">Wisselkoerswinsten of -verliezen worden geboekt naar de grootboekrekening in het veld **Bedrag (Rapp.-val.)** en de rekeningen die u hebt gespecificeerd voor winsten of verliezen in de velden **Gereal. grootbk.-winstrek.** en **Gereal. grootbk.-verliesrek.** op de pagina **Valuta's**.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-162">Exchange rate gains or losses are posted to the general ledger account in the **Additional-Currency Amount** field and to the accounts you specified for gains or losses in the **Realized G/L Gains Account** and **Realized G/L Losses Account** fields on the **Currencies** page.</span></span>|  

    <span data-ttu-id="ebf9d-163">Wisselkoerswinsten en -verliezen worden geboekt wanneer u de batchverwerking **Wisselkoers herwaarderen** uitvoert.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-163">Exchange rate gains and losses are posted when you run the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="ebf9d-164">In die batchverwerking wordt de herwaarderingswisselkoers geïdentificeerd op de pagina **Valutawisselkoersen** en worden vervolgens de bedragen in de velden **Bedrag** en **Bedrag (Rapp.-val.)** in de grootboekpost vergeleken om te bepalen of er een wisselkoerswinst of -verlies is.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-164">In that batch job, the adjustment exchange rate is identified on the **Currency Exchange Rates** page, and then the amounts in the **Amount** and **Additional-Currency Amount** fields on the general ledger entry are compared to determine whether there is an exchange rate gain or loss.</span></span> <span data-ttu-id="ebf9d-165">Voor de batchverwerking wordt de optie gebruikt die u in het veld **Wisselkoersherwaardering** selecteert om te bepalen hoe wisselkoerswinsten of -verliezen voor grootboekrekeningen moeten worden berekend en geboekt.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-165">The batch job uses the option that you select in the **Exchange Rate Adjustment** field to determine how to calculate and post exchange rate gains or losses for general ledger accounts.</span></span>  

4.  <span data-ttu-id="ebf9d-166">Sluit de pagina **Grootboekrekening**.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-166">Close the **G/L Account Card** page.</span></span>  

### <a name="to-specify-exchange-rate-adjustment-method-for-vat-entries"></a><span data-ttu-id="ebf9d-167">Wisselkoersherwaarderingsmethode opgeven voor btw-boekingen</span><span class="sxs-lookup"><span data-stu-id="ebf9d-167">To specify exchange rate adjustment method for VAT entries</span></span>  
1. <span data-ttu-id="ebf9d-168">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Grootboekinstellingen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-168">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Ledger Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ebf9d-169">Selecteer op de pagina **Boekhoudinstellingen** de relevante methode in het veld **Btw-herwaardering**.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-169">On the **General Ledger Setup** page, select the relevant method in the **VAT Exchange Rate Adjustment** field.</span></span>  
3. <span data-ttu-id="ebf9d-170">Als u in een extra valuta boekt, kunt u in het veld **Btw-herwaardering** aangeven hoe de rekeningen die zijn ingesteld voor btw-boekingen op de pagina **Btw-boekingsinstellingen** worden geherwaardeerd bij wisselkoersschommelingen tussen de LV en de extra rapportagevaluta.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-170">If you post in an additional reporting currency, you can specify in the **VAT Exchange Rate Adjustment** field how the accounts set up for VAT posting on the **VAT Posting Setup** page will be adjusted for exchange-rate fluctuations between LCY and the additional reporting currency.</span></span>  

    <span data-ttu-id="ebf9d-171">Wanneer u de batchverwerking **Wisselkoers herwaarderen** uitvoert, wordt de wisselkoersherwaardering bepaald op de pagina **Valutawisselkoers** en worden vervolgens de bedragen in het veld **Bedrag** en **Bedrag (Rapp.-val.)** in de btw-boeking vergeleken om te bepalen of er een wisselkoerswinst of -verlies is.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-171">When you run the **Adjust Exchange Rates** batch job, the adjustment exchange rate is identified on the **Currency Exchange Rate** page and then the amounts in the **Amount** and **Additional-Currency Amount** fields on the VAT entry are compared to determine if there is an exchange rate gain or loss.</span></span> <span data-ttu-id="ebf9d-172">Op basis van de optie die u opgeeft in dit veld, wordt in de batchverwerking bepaald hoe wisselkoerswinsten of -verliezen voor btw-rekeningen worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-172">The batch job uses the option that you select in this field to determine how to post exchange rate gains or losses for VAT accounts.</span></span>  

    <span data-ttu-id="ebf9d-173">U hebt dezelfde opties als met grootboekposten, maar in dit geval zijn de geherwaardeerde posten de btw-posten.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-173">You have the same options as with general ledger entries but in this case the entries adjusted will be the VAT entries.</span></span> <span data-ttu-id="ebf9d-174">De volgende tabel bevat de opties waaruit u kunt kiezen.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-174">The following table shows the options to choose from.</span></span>

    |<span data-ttu-id="ebf9d-175">Veld</span><span class="sxs-lookup"><span data-stu-id="ebf9d-175">Field</span></span>|<span data-ttu-id="ebf9d-176">Description</span><span class="sxs-lookup"><span data-stu-id="ebf9d-176">Description</span></span>|  
    |----------------------------------|---------------------------------------|  
    |<span data-ttu-id="ebf9d-177">**Geen**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-177">**No Adjustment**</span></span>|<span data-ttu-id="ebf9d-178">Er wordt geen wisselkoersherwaardering uitgevoerd op de grootboekrekening.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-178">No exchange rate adjustment is made to the general ledger account.</span></span> <span data-ttu-id="ebf9d-179">Dit is de standaardwaarde.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-179">This is the default option.</span></span>|  
    |<span data-ttu-id="ebf9d-180">**Bedrag**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-180">**Adjust Amount**</span></span>|<span data-ttu-id="ebf9d-181">Het bedrag in LV is aangepast voor eventuele wisselkoerswinsten of -verliezen.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-181">The LCY amount is adjusted for any exchange rate gains or losses.</span></span> <span data-ttu-id="ebf9d-182">Wisselkoerswinsten of -verliezen worden geboekt naar de grootboekrekening in het veld **Bedrag** en de rekeningen die u hebt gespecificeerd voor winsten of verliezen in de velden **Gereal. grootbk.-winstrek.** en **Gereal. grootbk.-verliesrek.** op de pagina **Valuta's**.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-182">Exchange rate gains or losses are posted to the general ledger account in the **Amount** field and to the accounts you specified for gains or losses in the **Realized G/L Gains Account** and **Realized G/L Losses Account** fields on the **Currencies** page.</span></span>|  
    |<span data-ttu-id="ebf9d-183">**Bedrag (Rapp.-val.)**</span><span class="sxs-lookup"><span data-stu-id="ebf9d-183">**Adjust Additional-Currency Amount**</span></span>|<span data-ttu-id="ebf9d-184">De extra rapportagevaluta is aangepast voor eventuele wisselkoerswinsten of -verliezen.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-184">The additional reporting currency is adjusted for any exchange rate gains or losses.</span></span> <span data-ttu-id="ebf9d-185">Wisselkoerswinsten of -verliezen worden geboekt naar de grootboekrekening in het veld **Bedrag (Rapp.-val.)** en de rekeningen die u hebt gespecificeerd voor winsten of verliezen in de velden **Gereal. grootbk.-winstrek.** en **Gereal. grootbk.-verliesrek.** op de pagina **Valuta's**.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-185">Exchange rate gains or losses are posted to the general ledger account in the **Additional-Currency Amount** field and to the accounts you specified for gains or losses in the **Realized G/L Gains Account** and **Realized G/L Losses Account** fields on the **Currencies** page.</span></span>|  

### <a name="to-activate-the-additional-reporting-currency"></a><span data-ttu-id="ebf9d-186">De extra rapportagevaluta activeren</span><span class="sxs-lookup"><span data-stu-id="ebf9d-186">To activate the additional reporting currency</span></span>  
1. <span data-ttu-id="ebf9d-187">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Grootboekinstellingen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-187">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Ledger Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ebf9d-188">Kies op de pagina **Boekhoudinstellingen** het veld **Extra rapportagevaluta** om de extra valuta te selecteren die u voor de rapportage wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-188">On the **General Ledger Setup** page, choose the **Additional Reporting Currency** field to select the additional currency that you want to report in.</span></span>  
3. <span data-ttu-id="ebf9d-189">Wanneer u het veld verlaat, geeft [!INCLUDE[d365fin](includes/d365fin_md.md)] een bevestigingsbericht weer waarin de effecten worden beschreven die het activeren van de rapportagevaluta tot gevolg heeft.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-189">When you leave the field, [!INCLUDE[d365fin](includes/d365fin_md.md)] displays a confirmation message describing the effects of activating the additional reporting currency.</span></span>  
4. <span data-ttu-id="ebf9d-190">Kies de knop **Ja** om te bevestigen dat u de valuta wilt activeren.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-190">Choose the **Yes** button to confirm that you want to activate the currency.</span></span>  
5. <span data-ttu-id="ebf9d-191">De batchtaak **Rapp.-val. herwaarderen** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-191">The **Adjust Add. Reporting Currency** batch job opens.</span></span>

    <span data-ttu-id="ebf9d-192">Met deze batchverwerking worden LV-bedragen van bestaande posten geconverteerd in de rapportagevaluta.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-192">This batch job converts LCY amounts on existing entries to the additional reporting currency.</span></span> <span data-ttu-id="ebf9d-193">Voor de batchverwerking wordt een standaardwisselkoers gebruikt die gekopieerd wordt van de wisselkoers die geldig is op de werkdatum op de pagina **Valutawisselkoersen**.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-193">The batch job uses a default exchange rate copied from the exchange rate that is valid on the work date on the **Currency Exchange Rates** page.</span></span> <span data-ttu-id="ebf9d-194">Verschillenbedragen die ontstaan bij de conversie van LV naar de rapportagevaluta worden geboekt naar de verschillenrekeningen (winst of verlies) die zijn opgegeven op de pagina **Valuta's**.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-194">Residual amounts that occur on conversion of LCY to additional reporting currency are posted to the residual gains and losses accounts specified on the **Currencies** page.</span></span> <span data-ttu-id="ebf9d-195">De boekingsdatum en het documentnummer van deze posten zijn gelijk aan de oorspronkelijke grootboekpost.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-195">The posting date and document number for these entries are the same as for the original general ledger entry.</span></span> <span data-ttu-id="ebf9d-196">Nadat alle verschilposten zijn geboekt, boekt de batchverwerking vervolgens een afrondingspost op de sluitdatum van elk afgesloten jaar naar de rekening voor ingehouden winst.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-196">After all these residual entries are posted, the batch job posts a rounding entry on the closing date of each closed year to the retained earnings account.</span></span> <span data-ttu-id="ebf9d-197">Hiermee wordt ervoor gezorgd dat het eindsaldo van de resultatenrekeningen voor elk afgesloten jaar 0 is voor de LV en de rapportagevaluta.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-197">This is to make sure that the ending balance of the income accounts for each closed years is 0 in both LCY and the additional reporting currency.</span></span>
6. <span data-ttu-id="ebf9d-198">Vul de benodigde velden in.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-198">Fill in the fields as necessary.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]      
7. <span data-ttu-id="ebf9d-199">Kies **OK** om de batchverwerking te starten.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-199">Choose the **OK** button to run the batch job.</span></span>  

<span data-ttu-id="ebf9d-200">Nadat u de batchverwerking hebt uitgevoerd, staan de bedragen van de volgende bestaande posten zowel in de LV als in de rapportagevaluta:</span><span class="sxs-lookup"><span data-stu-id="ebf9d-200">After running the batch job, amounts on the following existing entries will be in both LCY and in the additional reporting currency:</span></span>  

- <span data-ttu-id="ebf9d-201">Grootboekposten</span><span class="sxs-lookup"><span data-stu-id="ebf9d-201">General ledger entries</span></span>  
- <span data-ttu-id="ebf9d-202">Artikelvereffeningsposten</span><span class="sxs-lookup"><span data-stu-id="ebf9d-202">Item application entries</span></span>  
- <span data-ttu-id="ebf9d-203">Btw-posten</span><span class="sxs-lookup"><span data-stu-id="ebf9d-203">VAT entries</span></span>  
- <span data-ttu-id="ebf9d-204">Projectposten</span><span class="sxs-lookup"><span data-stu-id="ebf9d-204">Job ledger entries</span></span>  
- <span data-ttu-id="ebf9d-205">Waardeposten</span><span class="sxs-lookup"><span data-stu-id="ebf9d-205">Value entries</span></span>  
- <span data-ttu-id="ebf9d-206">Productieorderregels</span><span class="sxs-lookup"><span data-stu-id="ebf9d-206">Production order lines</span></span>  
- <span data-ttu-id="ebf9d-207">Productieorderposten</span><span class="sxs-lookup"><span data-stu-id="ebf9d-207">Production order ledger entries</span></span>  

<span data-ttu-id="ebf9d-208">Bovendien hebben alle toekomstige posten van hetzelfde type bedragen in zowel de LV als de rapportagevaluta.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-208">In addition, all future entries of the same type will have amounts recorded in both LCY and the additional reporting currency.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ebf9d-209">Het veld **Rapportagevaluta** wordt pas geactiveerd nadat u op de knop **OK** in de batchverwerking **Rapp.-val. herwaarderen** hebt geklikt.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-209">The **Add. Reporting Currency** field will only be activated after you choose the **OK** button in the **Adjust Add. Reporting Currency** batch job.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ebf9d-210">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ebf9d-210">See Also</span></span>
[<span data-ttu-id="ebf9d-211">Valutawisselkoersen bijwerken</span><span class="sxs-lookup"><span data-stu-id="ebf9d-211">Update Currency Exchange Rates</span></span>](finance-how-update-currencies.md)  
[<span data-ttu-id="ebf9d-212">Afsluitingsjaren en -perioden</span><span class="sxs-lookup"><span data-stu-id="ebf9d-212">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="ebf9d-213">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ebf9d-213">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
