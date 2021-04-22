---
title: Rentefactuurcondities instellen
description: Leer hoe u Business Central zo instelt dat u klanten op de hoogte kunt stellen van extra kosten door rentefacturen te verzenden.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 08a2443f94efbc9920145109b4b7499a3a4e05b3
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783634"
---
# <a name="set-up-finance-charge-terms"></a><span data-ttu-id="67ead-103">Rentefactuurcondities instellen</span><span class="sxs-lookup"><span data-stu-id="67ead-103">Set Up Finance Charge Terms</span></span>

<span data-ttu-id="67ead-104">Wanneer een klant niet op de vervaldatum betaalt, kunt u automatisch aanmaningskosten laten berekenen en die optellen bij de openstaande bedragen op de rekening van de klant.</span><span class="sxs-lookup"><span data-stu-id="67ead-104">When a customer does not pay by the due date, you can have finance charges calculated automatically and add them to the overdue amounts on the customer's account.</span></span> <span data-ttu-id="67ead-105">U kunt klanten op de hoogte stellen van de toeslagen door rentefacturen te versturen.</span><span class="sxs-lookup"><span data-stu-id="67ead-105">You can inform customers of the added charges by sending finance charge memos.</span></span> <span data-ttu-id="67ead-106">Maar u moet eerst een code instellen die elke renteberekening vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="67ead-106">But first, you must set up a code that represents each finance charge calculation.</span></span> <span data-ttu-id="67ead-107">Vervolgens kunt u deze code opgeven in het veld Rentefactuurconditie op de klantenkaarten.</span><span class="sxs-lookup"><span data-stu-id="67ead-107">Then you can enter this code in the Fin. Charge Terms Code field on customer cards.</span></span>  

## <a name="finance-charge-terms"></a><span data-ttu-id="67ead-108">Rentefactuurcondities</span><span class="sxs-lookup"><span data-stu-id="67ead-108">Finance charge terms</span></span>

<span data-ttu-id="67ead-109">U moet rentefactuurcondities instellen voor elke berekening van financieringskosten en vervolgens de voorwaarden toewijzen aan de klant in het veld **Rentefactuurconditie** op de pagina **Klant**.</span><span class="sxs-lookup"><span data-stu-id="67ead-109">You must set up finance charge terms for each finance charge calculation, and then assign the terms to the customer in the **Fin. Charge Terms Code** field on the **Customer** page.</span></span>

<span data-ttu-id="67ead-110">U berekent rentefacturen via de rentedagenmethode of de methode voor openstaande saldi.</span><span class="sxs-lookup"><span data-stu-id="67ead-110">Finance charges can be calculated using either the average daily balance or the balance due methods.</span></span>

* <span data-ttu-id="67ead-111">Rentedagen</span><span class="sxs-lookup"><span data-stu-id="67ead-111">Average daily balance</span></span>  
  
  <span data-ttu-id="67ead-112">Er wordt rekening gehouden met het aantal dagen dat de betalingstermijn is verstreken:</span><span class="sxs-lookup"><span data-stu-id="67ead-112">The number of days the payment is overdue is taken into account:</span></span>  
  <span data-ttu-id="67ead-113">*Methode Rentedagen* - *Rente* = *Openstaand bedrag* x *(Dagen overschreden/Renteperiode)* x *(Rentepercentage/100)*</span><span class="sxs-lookup"><span data-stu-id="67ead-113">*Average Daily Balance method* - *Finance Charge* = *Overdue Amount* x *(Days Overdue / Interest Period)* x *(Interest Rate/100)*</span></span>

* <span data-ttu-id="67ead-114">Openstaand bedrag</span><span class="sxs-lookup"><span data-stu-id="67ead-114">Balance due</span></span>  
  
  <span data-ttu-id="67ead-115">De rentefactuur is een percentage van het openstaande bedrag:</span><span class="sxs-lookup"><span data-stu-id="67ead-115">The finance charge is a percentage of the overdue amount:</span></span>  
  <span data-ttu-id="67ead-116">*Methode Openstaand bedrag* - *Rente* = *Openstaand bedrag* x *(rentepercentage/100)*</span><span class="sxs-lookup"><span data-stu-id="67ead-116">*Balance Due method* - *Finance Charge* = *Overdue Amount* x *(Interest Rate / 100)*</span></span>

<span data-ttu-id="67ead-117">Elke conditie in de tabel Rentefactuurcondities is bovendien gekoppeld aan de subtabel Rentefactuurtekst.</span><span class="sxs-lookup"><span data-stu-id="67ead-117">Additionally, each term in the Finance Charge Terms table is linked to a subtable, the Finance Charge Text table.</span></span> <span data-ttu-id="67ead-118">Voor elke set rentefactuurcondities kunt u een begin- en/of eindtekst definiëren die in de rentefactuur wordt opgenomen.</span><span class="sxs-lookup"><span data-stu-id="67ead-118">For each set of finance charge terms, you can define a beginning and/or an ending text to include on the finance charge memo.</span></span>

### <a name="to-set-up-finance-charge-terms"></a><span data-ttu-id="67ead-119">Rentefactuurcondities instellen</span><span class="sxs-lookup"><span data-stu-id="67ead-119">To set up finance charge terms</span></span>

1. <span data-ttu-id="67ead-120">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rentefactuurcondities** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="67ead-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Finance Charge Terms**, and then choose the related link.</span></span>  
2. <span data-ttu-id="67ead-121">Vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="67ead-121">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="67ead-122">Als u meer dan één combinatie van rentefactuurcondities wilt gebruiken, stelt u een code in voor elke.</span><span class="sxs-lookup"><span data-stu-id="67ead-122">To use more than one combination of finance charge terms, set up a code for each one.</span></span>

    <span data-ttu-id="67ead-123">Voor elke rentefactuurconditie kunt u afzonderlijke voorwaarden specificeren, die extra kosten in zowel de lokale valuta als in vreemde valuta kunnen bevatten.</span><span class="sxs-lookup"><span data-stu-id="67ead-123">For each finance charge term, you can specify individual conditions that can include additional fees in both LCY and in foreign currency.</span></span> <span data-ttu-id="67ead-124">U kunt aanvullende toeslagen in vreemde valuta's definiëren voor elke conditie op de pagina **Rentefactuurcondities**.</span><span class="sxs-lookup"><span data-stu-id="67ead-124">You can define additional fees in foreign currencies for each term on the **Finance Charge Terms** page.</span></span>
4. <span data-ttu-id="67ead-125">Kies de actie **Valuta's**.</span><span class="sxs-lookup"><span data-stu-id="67ead-125">Choose the **Currencies** action.</span></span>
5. <span data-ttu-id="67ead-126">Op de pagina **Valuta's voor rentefactuurcondities** definieert u voor elke conditie een valutacode en een toeslag.</span><span class="sxs-lookup"><span data-stu-id="67ead-126">On the **Currencies for Fin. Chrg. Terms** page, define for each term a currency code and an additional fee.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="67ead-127">Wanneer u aanmaningskosten in een vreemde valuta maakt, worden de vreemdevalutacondities die u instelt, gebruikt om rentefacturen te maken.</span><span class="sxs-lookup"><span data-stu-id="67ead-127">When you create finance charges in a foreign currency, the foreign currency conditions that you set up here will be used to create finance charge memos.</span></span> <span data-ttu-id="67ead-128">Als u geen condities voor rentefactuurcondities in vreemde valuta's hebt ingesteld, worden de condities in de lokale valuta die op de pagina **Rentefactuurcondities** zijn opgegeven, gebruikt en omgerekend naar de betreffende valuta.</span><span class="sxs-lookup"><span data-stu-id="67ead-128">If there are no foreign currency finance charge conditions set up, the LCY finance charge conditions specified on the **Finance Charge Terms** page will be used and then converted to the relevant currency.</span></span>

    <span data-ttu-id="67ead-129">Voor elke rentefactuurconditie kunt u tekst opgeven die wordt afgedrukt vóór (**Begintekst**) of na (**Eindtekst**) in de posten op de rentefactuur.</span><span class="sxs-lookup"><span data-stu-id="67ead-129">For each finance charge term, you can specify text that will be printed before (**Beginning Text**) or after (**Ending Text**) on the entries on the finance charge memo.</span></span>  
6. <span data-ttu-id="67ead-130">Kies respectievelijk de acties **Begintekst** of **Eindtekst** en vul de pagina **Rentefactuurtekst** in.</span><span class="sxs-lookup"><span data-stu-id="67ead-130">Choose the **Beginning Text** or **Ending Text** actions respectively, and fill on the **Finance Charge Text** page.</span></span>
7. <span data-ttu-id="67ead-131">Als u automatisch gerelateerde waarden in de resulterende rentefactuurtekst wilt invoegen, voert u de volgende tijdelijke aanduidingen in het veld **Tekst** in.</span><span class="sxs-lookup"><span data-stu-id="67ead-131">To automatically insert related values in the resulting finance charge text, enter the following placeholders in the **Text** field.</span></span>

|<span data-ttu-id="67ead-132">Tijdelijke aanduiding</span><span class="sxs-lookup"><span data-stu-id="67ead-132">Placeholder</span></span>|<span data-ttu-id="67ead-133">Waarde</span><span class="sxs-lookup"><span data-stu-id="67ead-133">Value</span></span>|  
|-----------------|-----------|  
|<span data-ttu-id="67ead-134">%1</span><span class="sxs-lookup"><span data-stu-id="67ead-134">%1</span></span>|<span data-ttu-id="67ead-135">Inhoud van het veld **Documentdatum** in de rentefactuurkoptekst</span><span class="sxs-lookup"><span data-stu-id="67ead-135">Content of the **Document Date** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="67ead-136">%2</span><span class="sxs-lookup"><span data-stu-id="67ead-136">%2</span></span>|<span data-ttu-id="67ead-137">Inhoud van het veld **Vervaldatum** in de rentefactuurkoptekst</span><span class="sxs-lookup"><span data-stu-id="67ead-137">Content of the **Due Date** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="67ead-138">%3</span><span class="sxs-lookup"><span data-stu-id="67ead-138">%3</span></span>|<span data-ttu-id="67ead-139">Inhoud van het veld **Rente** in de gerelateerde rentefactuurcondities</span><span class="sxs-lookup"><span data-stu-id="67ead-139">Content of the **Interest Rate** field on the related finance charge terms</span></span>|  
|<span data-ttu-id="67ead-140">%4</span><span class="sxs-lookup"><span data-stu-id="67ead-140">%4</span></span>|<span data-ttu-id="67ead-141">Inhoud van het veld **Restbedrag** in de rentefactuurkoptekst</span><span class="sxs-lookup"><span data-stu-id="67ead-141">Content of the **Remaining Amount** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="67ead-142">%5</span><span class="sxs-lookup"><span data-stu-id="67ead-142">%5</span></span>|<span data-ttu-id="67ead-143">Inhoud van het veld **Rentebedrag** in de rentefactuurkoptekst</span><span class="sxs-lookup"><span data-stu-id="67ead-143">Content of the **Interest Amount** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="67ead-144">%6</span><span class="sxs-lookup"><span data-stu-id="67ead-144">%6</span></span>|<span data-ttu-id="67ead-145">Inhoud van het veld **Toeslag** in de rentefactuurkoptekst</span><span class="sxs-lookup"><span data-stu-id="67ead-145">Content of the **Additional Fee** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="67ead-146">%7</span><span class="sxs-lookup"><span data-stu-id="67ead-146">%7</span></span>|<span data-ttu-id="67ead-147">Het totaalbedrag van de aanmaning</span><span class="sxs-lookup"><span data-stu-id="67ead-147">The total amount of the reminder</span></span>|  
|<span data-ttu-id="67ead-148">%8</span><span class="sxs-lookup"><span data-stu-id="67ead-148">%8</span></span>|<span data-ttu-id="67ead-149">Inhoud van het veld **Valutacode** in de rentefactuurkoptekst</span><span class="sxs-lookup"><span data-stu-id="67ead-149">Content of the **Currency Code** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="67ead-150">%9</span><span class="sxs-lookup"><span data-stu-id="67ead-150">%9</span></span>|<span data-ttu-id="67ead-151">Inhoud van het veld **Boekingsdatum** in de rentefactuurkoptekst</span><span class="sxs-lookup"><span data-stu-id="67ead-151">Content of the **Posting Date** field on the finance charge memo header</span></span>|  

## <a name="see-also"></a><span data-ttu-id="67ead-152">Zie ook</span><span class="sxs-lookup"><span data-stu-id="67ead-152">See also</span></span>

[<span data-ttu-id="67ead-153">Openstaande saldi innen</span><span class="sxs-lookup"><span data-stu-id="67ead-153">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="67ead-154">De termijnen en niveaus van aanmaningen instellen</span><span class="sxs-lookup"><span data-stu-id="67ead-154">Set Up Reminder Terms and Levels</span></span>](finance-setup-reminders.md)  
[<span data-ttu-id="67ead-155">Financiën instellen</span><span class="sxs-lookup"><span data-stu-id="67ead-155">Setting Up Finance</span></span>](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]