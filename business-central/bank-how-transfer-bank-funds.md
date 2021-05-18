---
title: Bankfondsen overboeken
description: U kunt bedragen overbrengen van de ene naar de andere bankrekening, inclusief andere valuta's, door de transactie in het dagboek te boeken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 04/29/2021
ms.author: edupont
ms.openlocfilehash: da9c8711751040cecb267a3b2209bad2534b618b
ms.sourcegitcommit: 08ca5798cf3f04fc3ea38fff40c1860196a70adf
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 05/06/2021
ms.locfileid: "5985399"
---
# <a name="transfer-bank-funds"></a><span data-ttu-id="d35fe-103">Bankfondsen overboeken</span><span class="sxs-lookup"><span data-stu-id="d35fe-103">Transfer Bank Funds</span></span>

<span data-ttu-id="d35fe-104">Soms moet u een bedrag van de ene naar de andere bankrekening overboeken in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d35fe-104">You may sometimes need to transfer an amount from one bank account in [!INCLUDE[prod_short](includes/prod_short.md)] to another.</span></span> <span data-ttu-id="d35fe-105">Als u dit wilt doen, moet u de transactie boeken op de pagina **Dagboek**.</span><span class="sxs-lookup"><span data-stu-id="d35fe-105">To do this, you must post the transaction on the **General Journal** page.</span></span> <span data-ttu-id="d35fe-106">De taak verschilt afhankelijk van of de bankrekeningen dezelfde valuta gebruiken of niet.</span><span class="sxs-lookup"><span data-stu-id="d35fe-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="d35fe-107">Een transfer boeken tussen bankrekeningen met dezelfde valutacode</span><span class="sxs-lookup"><span data-stu-id="d35fe-107">To post a transfer between bank accounts with the same currency code</span></span>

1. <span data-ttu-id="d35fe-108">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Dagboek** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="d35fe-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="d35fe-109">Vul op een dagboekregel de velden **Boekingsdatum** en **Documentnr.** in.</span><span class="sxs-lookup"><span data-stu-id="d35fe-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="d35fe-110">Selecteer in het veld **Rekeningsoort** de optie **Bankrekening**.</span><span class="sxs-lookup"><span data-stu-id="d35fe-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="d35fe-111">Selecteer in het veld **Rekeningnr.** de bankrekening waarvan u de fondsen wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="d35fe-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="d35fe-112">Voer in het veld **Bedrag** het bedrag in dat u wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="d35fe-112">In the **Amount** field, enter the amount to be transferred.</span></span>

    <span data-ttu-id="d35fe-113">Vervolgens moet u de tegenrekening opgeven.</span><span class="sxs-lookup"><span data-stu-id="d35fe-113">Next, you must specify the balancing account.</span></span> <span data-ttu-id="d35fe-114">Als u de relevante velden niet kunt zien, kiest u de actie **Meer kolommen weergeven** om alle beschikbare velden te bekijken.</span><span class="sxs-lookup"><span data-stu-id="d35fe-114">If you can't see the relevant fields, then choose the **Show More Columns** action to view all available fields.</span></span>
6. <span data-ttu-id="d35fe-115">Selecteer in het veld **Tegenrekeningtype** **Bankrekening**.</span><span class="sxs-lookup"><span data-stu-id="d35fe-115">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="d35fe-116">Selecteer in het veld **Tegenrekeningnr.** de bankrekening waarnaar u de fondsen wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="d35fe-116">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="d35fe-117">Boek het dagboek.</span><span class="sxs-lookup"><span data-stu-id="d35fe-117">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="d35fe-118">Transfers boeken tussen bankrekeningen met verschillende valutacodes</span><span class="sxs-lookup"><span data-stu-id="d35fe-118">To post a transfer between bank accounts with different currency codes</span></span>

<span data-ttu-id="d35fe-119">Als u gelden wilt overbrengen tussen bankrekeningen die verschillende valuta's gebruiken, moet u twee dagboekregels boeken.</span><span class="sxs-lookup"><span data-stu-id="d35fe-119">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="d35fe-120">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Dagboek** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="d35fe-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="d35fe-121">Maak twee dagboekregels en vul de velden **Boekingsdatum** en **Documentnr.** in.</span><span class="sxs-lookup"><span data-stu-id="d35fe-121">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="d35fe-122">Selecteer op de eerste dagboekregel **Bankrekening** in het veld **Soort**.</span><span class="sxs-lookup"><span data-stu-id="d35fe-122">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="d35fe-123">Selecteer in het veld **Rekeningnr.** de bankrekening waarvan u de fondsen wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="d35fe-123">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="d35fe-124">Voer in het veld **Bedrag** het bedrag in de valuta van de bankrekening in, met of zonder minteken.</span><span class="sxs-lookup"><span data-stu-id="d35fe-124">In the **Amount** field, enter the amount in the currency of the bank account with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="d35fe-125">Een bedrag zonder minteken is een debetbedrag, een bedrag met een minteken is een kredietbedrag.</span><span class="sxs-lookup"><span data-stu-id="d35fe-125">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d35fe-126">Sommige bedrijven geven er de voorkeur aan om tussen rekeningen over te boeken op afzonderlijke dagboekregels.</span><span class="sxs-lookup"><span data-stu-id="d35fe-126">Some companies prefer to transfer between accounts on separate journal lines.</span></span> <span data-ttu-id="d35fe-127">Andere bedrijven geven er de voorkeur aan om alles op één dagboekregel te boeken met behulp van een tegenrekening.</span><span class="sxs-lookup"><span data-stu-id="d35fe-127">Other companies prefer to post everything on one journal line by using a balancing account.</span></span> <span data-ttu-id="d35fe-128">Neem contact op met uw plaatselijke expert als u niet zeker weet wat u moet doen.</span><span class="sxs-lookup"><span data-stu-id="d35fe-128">Check with your local expert if you're not sure what to do.</span></span>
    >
    > <span data-ttu-id="d35fe-129">Als uw bedrijf liever een tegenrekening gebruikt, stelt u het veld **Tegenrekeningsoort** in op **Bankrekening** en stelt u het veld **Tegenrekeningnr.** in op de bankrekening waarnaar u het geld wilt overboeken.</span><span class="sxs-lookup"><span data-stu-id="d35fe-129">If your company prefers to use a balancing account, then set the **Bal. Account Type** field to **Bank Account**, and set the **Bal. Account No.** field to the bank account to which you want to transfer the funds.</span></span> <span data-ttu-id="d35fe-130">Ga dan verder met stap 9 of 10.</span><span class="sxs-lookup"><span data-stu-id="d35fe-130">Then proceed to step 9 or 10.</span></span>
    >
    > <span data-ttu-id="d35fe-131">Als uw bedrijf liever een aparte dagboekregel gebruikt, gaat u verder met de volgende stap.</span><span class="sxs-lookup"><span data-stu-id="d35fe-131">If your company prefers to use a separate journal line, then move on to the next step.</span></span>
6. <span data-ttu-id="d35fe-132">Selecteer op de tweede dagboekregel **Bankrekening** in het veld **Soort**.</span><span class="sxs-lookup"><span data-stu-id="d35fe-132">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="d35fe-133">Selecteer in het veld **Rekeningnr.** de bankrekening waarnaar u de fondsen wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="d35fe-133">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="d35fe-134">Voer in het veld **Bedrag** het bedrag in de valuta van de bankrekening in, met of zonder minteken.</span><span class="sxs-lookup"><span data-stu-id="d35fe-134">In the **Amount** field, enter the amount in the currency of the bank account with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="d35fe-135">Een bedrag zonder minteken is een debetbedrag, een bedrag met een minteken is een kredietbedrag.</span><span class="sxs-lookup"><span data-stu-id="d35fe-135">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>
9. <span data-ttu-id="d35fe-136">Als de gebruikte wisselkoersen in het dagboek verschillen van de wisselkoersen op de pagina **Valutawisselkoersen**, voert u een nieuwe dagboekregel in voor de wisselkoerswinsten of -verliezen.</span><span class="sxs-lookup"><span data-stu-id="d35fe-136">If the exchange rates used in the journal are different than the exchange rates on the **Currency Exchange Rates** page, enter a new journal line for the exchange rate gain or loss.</span></span>  

    1. <span data-ttu-id="d35fe-137">Geef **Grootboekrekening** op in het veld **Rekeningsoort**.</span><span class="sxs-lookup"><span data-stu-id="d35fe-137">Enter **G/L Account** in the **Account Type** field.</span></span>  

    2. <span data-ttu-id="d35fe-138">Voer in het veld **Rekeningnr.** het grootboekrekeningnummer voor wisselkoerswinst of -verlies in.</span><span class="sxs-lookup"><span data-stu-id="d35fe-138">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span>  

    3. <span data-ttu-id="d35fe-139">Voer de wisselkoerswinsten of -verliezen in het veld **Bedrag** in, met of zonder minteken.</span><span class="sxs-lookup"><span data-stu-id="d35fe-139">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="d35fe-140">Een bedrag zonder minteken is een debetbedrag, een bedrag met een minteken is een kredietbedrag.</span><span class="sxs-lookup"><span data-stu-id="d35fe-140">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>
10. <span data-ttu-id="d35fe-141">Boek het dagboek.</span><span class="sxs-lookup"><span data-stu-id="d35fe-141">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="d35fe-142">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d35fe-142">See Also</span></span>

[<span data-ttu-id="d35fe-143">Bankrekeningen reconciliëren</span><span class="sxs-lookup"><span data-stu-id="d35fe-143">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="d35fe-144">Bankieren instellen</span><span class="sxs-lookup"><span data-stu-id="d35fe-144">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="d35fe-145">Werken met diversendagboeken</span><span class="sxs-lookup"><span data-stu-id="d35fe-145">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="d35fe-146">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d35fe-146">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]