---
title: Bankfondsen overboeken| Microsoft Docs
description: U kunt bedragen overbrengen van de ene naar de andere bankrekening, inclusief andere valuta's, door de transactie in het dagboek te boeken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: dea39ba380eee574205d57ba198f15213c341ea0
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779744"
---
# <a name="transfer-bank-funds"></a><span data-ttu-id="bf293-103">Bankfondsen overboeken</span><span class="sxs-lookup"><span data-stu-id="bf293-103">Transfer Bank Funds</span></span>
<span data-ttu-id="bf293-104">Soms moet u een bedrag van de ene naar de andere bankrekening overboeken in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="bf293-104">You may sometimes need to transfer an amount from one bank account in [!INCLUDE[prod_short](includes/prod_short.md)] to another.</span></span> <span data-ttu-id="bf293-105">Als u dit wilt doen, moet u een transactie boeken op de pagina **Dagboek**.</span><span class="sxs-lookup"><span data-stu-id="bf293-105">To do this, you must post the a transaction on the **General Journal** page.</span></span> <span data-ttu-id="bf293-106">De taak verschilt afhankelijk van of de bankrekeningen dezelfde valuta gebruiken of niet.</span><span class="sxs-lookup"><span data-stu-id="bf293-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="bf293-107">Een transfer boeken tussen bankrekeningen met dezelfde valutacode</span><span class="sxs-lookup"><span data-stu-id="bf293-107">To post a transfer between bank accounts with the same currency code</span></span>
1. <span data-ttu-id="bf293-108">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Dagboek** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="bf293-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="bf293-109">Vul op een dagboekregel de velden **Boekingsdatum** en **Documentnr.** in.</span><span class="sxs-lookup"><span data-stu-id="bf293-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="bf293-110">Selecteer in het veld **Rekeningsoort** de optie **Bankrekening**.</span><span class="sxs-lookup"><span data-stu-id="bf293-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="bf293-111">Selecteer in het veld **Rekeningnr.** de bankrekening waarvan u de fondsen wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="bf293-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="bf293-112">Voer in het veld **Bedrag** het bedrag in dat u wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="bf293-112">In the **Amount** field, enter the amount to be transferred.</span></span>
6. <span data-ttu-id="bf293-113">Kies de actie **Meer kolommen weergeven** om alle beschikbare velden te bekijken.</span><span class="sxs-lookup"><span data-stu-id="bf293-113">Choose the **Show More Columns** action to view all available fields.</span></span>
7. <span data-ttu-id="bf293-114">Selecteer in het veld **Tegenrekeningtype** **Bankrekening**.</span><span class="sxs-lookup"><span data-stu-id="bf293-114">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
8. <span data-ttu-id="bf293-115">Selecteer in het veld **Tegenrekeningnr.** de bankrekening waarnaar u de fondsen wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="bf293-115">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
9. <span data-ttu-id="bf293-116">Boek het dagboek.</span><span class="sxs-lookup"><span data-stu-id="bf293-116">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="bf293-117">Transfers boeken tussen bankrekeningen met verschillende valutacodes</span><span class="sxs-lookup"><span data-stu-id="bf293-117">To post a transfer between bank accounts with different currency codes</span></span>
<span data-ttu-id="bf293-118">Als u gelden wilt overbrengen tussen bankrekeningen die verschillende valuta's gebruiken, moet u twee dagboekregels boeken.</span><span class="sxs-lookup"><span data-stu-id="bf293-118">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="bf293-119">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Dagboek** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="bf293-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="bf293-120">Maak twee dagboekregels en vul de velden **Boekingsdatum** en **Documentnr.** in.</span><span class="sxs-lookup"><span data-stu-id="bf293-120">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="bf293-121">Selecteer op de eerste dagboekregel **Bankrekening** in het veld **Soort**.</span><span class="sxs-lookup"><span data-stu-id="bf293-121">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="bf293-122">Selecteer in het veld **Rekeningnr.** de bankrekening waarvan u de fondsen wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="bf293-122">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="bf293-123">Voer in het veld **Bedrag** het bedrag in de valuta van de bankrekening in.</span><span class="sxs-lookup"><span data-stu-id="bf293-123">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="bf293-124">Voer creditbedragen met een minteken in.</span><span class="sxs-lookup"><span data-stu-id="bf293-124">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="bf293-125">Voer debetbedragen zonder een minteken in.</span><span class="sxs-lookup"><span data-stu-id="bf293-125">Enter debit amounts without a minus sign.</span></span>
6. <span data-ttu-id="bf293-126">Selecteer in het veld **Tegenrekeningtype** **Bankrekening**.</span><span class="sxs-lookup"><span data-stu-id="bf293-126">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="bf293-127">Selecteer in het veld **Tegenrekeningnr.** de bankrekening waarnaar u de fondsen wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="bf293-127">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="bf293-128">Selecteer op de tweede dagboekregel **Bankrekening** in het veld **Soort**.</span><span class="sxs-lookup"><span data-stu-id="bf293-128">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
9. <span data-ttu-id="bf293-129">Selecteer in het veld **Rekeningnr.** de bankrekening waarnaar u de fondsen wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="bf293-129">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
10. <span data-ttu-id="bf293-130">Voer in het veld **Bedrag** het bedrag in de valuta van de bankrekening in.</span><span class="sxs-lookup"><span data-stu-id="bf293-130">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="bf293-131">Voer creditbedragen met een minteken in.</span><span class="sxs-lookup"><span data-stu-id="bf293-131">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="bf293-132">Voer debetbedragen zonder een minteken in.</span><span class="sxs-lookup"><span data-stu-id="bf293-132">Enter debit amounts without a minus sign.</span></span>
11. <span data-ttu-id="bf293-133">Selecteer in het veld **Tegenrekeningtype** **Bankrekening**.</span><span class="sxs-lookup"><span data-stu-id="bf293-133">In the **Bal. Account Type** field, select **Bank Account**.</span></span>  
12. <span data-ttu-id="bf293-134">Selecteer in het veld **Tegenrekeningnr.** de bankrekening waarvan u de fondsen wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="bf293-134">In the **Bal. Account No.** field, select the bank account from which you want to transfer the funds.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="bf293-135">Als de gebruikte wisselkoersen in het dagboek verschillen van de wisselkoersen op de pagina **Valutawisselkoersen**, voert u een derde regel in voor de wisselkoerswinsten of -verliezen.</span><span class="sxs-lookup"><span data-stu-id="bf293-135">If the exchange rates used in the journal are different than the exchange rates on the **Currency Exchange Rates** page, enter a third line for the exchange rate gain or loss.</span></span> <span data-ttu-id="bf293-136">Geef **Grootboekrekening** op in het veld **Rekeningsoort**.</span><span class="sxs-lookup"><span data-stu-id="bf293-136">Enter **G/L Account** in the **Account Type** field.</span></span> <span data-ttu-id="bf293-137">Voer in het veld **Rekeningnr.** het grootboekrekeningnummer voor wisselkoerswinst of -verlies in.</span><span class="sxs-lookup"><span data-stu-id="bf293-137">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span> <span data-ttu-id="bf293-138">Voer de wisselkoerswinst of - verlies in het veld **Bedrag** in met of zonder een minteken voor respectievelijk debet- en creditbedragen.</span><span class="sxs-lookup"><span data-stu-id="bf293-138">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign for credits and debits respectively.</span></span>
13. <span data-ttu-id="bf293-139">Boek het dagboek.</span><span class="sxs-lookup"><span data-stu-id="bf293-139">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="bf293-140">Zie ook</span><span class="sxs-lookup"><span data-stu-id="bf293-140">See Also</span></span>
[<span data-ttu-id="bf293-141">Bankrekeningen reconciliëren</span><span class="sxs-lookup"><span data-stu-id="bf293-141">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="bf293-142">Bankieren instellen</span><span class="sxs-lookup"><span data-stu-id="bf293-142">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="bf293-143">Werken met diversendagboeken</span><span class="sxs-lookup"><span data-stu-id="bf293-143">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="bf293-144">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bf293-144">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]