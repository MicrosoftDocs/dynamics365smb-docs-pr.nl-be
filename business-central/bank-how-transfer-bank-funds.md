---
title: Bankfondsen overboeken| Microsoft Docs
description: U kunt bedragen overbrengen van de ene naar de andere bankrekening, inclusief andere valuta's, door de transactie in het dagboek te boeken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 12/13/2019
ms.author: sgroespe
ms.openlocfilehash: 3618ad87377ebc47f183292207d2f25dc6c3ed34
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910432"
---
# <a name="transfer-bank-funds"></a><span data-ttu-id="8d1e4-103">Bankfondsen overboeken</span><span class="sxs-lookup"><span data-stu-id="8d1e4-103">Transfer Bank Funds</span></span>
<span data-ttu-id="8d1e4-104">Soms moet u een bedrag van de ene naar de andere bankrekening overboeken in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8d1e4-104">You may sometimes need to transfer an amount from one bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] to another.</span></span> <span data-ttu-id="8d1e4-105">Als u dit wilt doen, moet u een transactie boeken op de pagina **Dagboek**.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-105">To do this, you must post the a transaction on the **General Journal** page.</span></span> <span data-ttu-id="8d1e4-106">De taak verschilt afhankelijk van of de bankrekeningen dezelfde valuta gebruiken of niet.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="8d1e4-107">Een transfer boeken tussen bankrekeningen met dezelfde valutacode</span><span class="sxs-lookup"><span data-stu-id="8d1e4-107">To post a transfer between bank accounts with the same currency code</span></span>
1. <span data-ttu-id="8d1e4-108">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Dagboek** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="8d1e4-109">Vul op een dagboekregel de velden **Boekingsdatum** en **Documentnr.** in.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="8d1e4-110">Selecteer in het veld **Rekeningsoort** de optie **Bankrekening**.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="8d1e4-111">Selecteer in het veld **Rekeningnr.** de bankrekening waarvan u de fondsen wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="8d1e4-112">Voer in het veld **Bedrag** het bedrag in dat u wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-112">In the **Amount** field, enter the amount to be transferred.</span></span>
6. <span data-ttu-id="8d1e4-113">Kies de actie **Meer kolommen weergeven** om alle beschikbare velden te bekijken.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-113">Choose the **Show More Columns** action to view all available fields.</span></span>
7. <span data-ttu-id="8d1e4-114">Selecteer in het veld **Tegenrekeningtype** **Bankrekening**.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-114">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
8. <span data-ttu-id="8d1e4-115">Selecteer in het veld **Tegenrekeningnr.** de bankrekening waarnaar u de fondsen wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-115">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
9. <span data-ttu-id="8d1e4-116">Boek het dagboek.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-116">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="8d1e4-117">Transfers boeken tussen bankrekeningen met verschillende valutacodes</span><span class="sxs-lookup"><span data-stu-id="8d1e4-117">To post a transfer between bank accounts with different currency codes</span></span>
<span data-ttu-id="8d1e4-118">Als u gelden wilt overbrengen tussen bankrekeningen die verschillende valuta's gebruiken, moet u twee dagboekregels boeken.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-118">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="8d1e4-119">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Dagboek** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="8d1e4-120">Maak twee dagboekregels en vul de velden **Boekingsdatum** en **Documentnr.** in.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-120">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="8d1e4-121">Selecteer op de eerste dagboekregel **Bankrekening** in het veld **Soort**.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-121">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="8d1e4-122">Selecteer in het veld **Rekeningnr.** de bankrekening waarvan u de fondsen wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-122">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="8d1e4-123">Voer in het veld **Bedrag** het bedrag in de valuta van de bankrekening in.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-123">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="8d1e4-124">Voer creditbedragen met een minteken in.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-124">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="8d1e4-125">Voer debetbedragen zonder een minteken in.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-125">Enter debit amounts without a minus sign.</span></span>
6. <span data-ttu-id="8d1e4-126">Selecteer in het veld **Tegenrekeningtype** **Bankrekening**.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-126">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="8d1e4-127">Selecteer in het veld **Tegenrekeningnr.** de bankrekening waarnaar u de fondsen wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-127">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="8d1e4-128">Selecteer op de tweede dagboekregel **Bankrekening** in het veld **Soort**.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-128">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
9. <span data-ttu-id="8d1e4-129">Selecteer in het veld **Rekeningnr.** de bankrekening waarnaar u de fondsen wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-129">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
10. <span data-ttu-id="8d1e4-130">Voer in het veld **Bedrag** het bedrag in de valuta van de bankrekening in.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-130">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="8d1e4-131">Voer creditbedragen met een minteken in.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-131">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="8d1e4-132">Voer debetbedragen zonder een minteken in.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-132">Enter debit amounts without a minus sign.</span></span>
11. <span data-ttu-id="8d1e4-133">Selecteer in het veld **Tegenrekeningtype** **Bankrekening**.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-133">In the **Bal. Account Type** field, select **Bank Account**.</span></span>  
12. <span data-ttu-id="8d1e4-134">Selecteer in het veld **Tegenrekeningnr.** de bankrekening waarvan u de fondsen wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-134">In the **Bal. Account No.** field, select the bank account from which you want to transfer the funds.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="8d1e4-135">Als de gebruikte wisselkoersen in het dagboek verschillen van de wisselkoersen op de pagina **Valutawisselkoersen**, voert u een derde regel in voor de wisselkoerswinsten of -verliezen.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-135">If the exchange rates used in the journal are different than the exchange rates on the **Currency Exchange Rates** page, enter a third line for the exchange rate gain or loss.</span></span> <span data-ttu-id="8d1e4-136">Geef **Grootboekrekening** op in het veld **Rekeningsoort**.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-136">Enter **G/L Account** in the **Account Type** field.</span></span> <span data-ttu-id="8d1e4-137">Voer in het veld **Rekeningnr.** het grootboekrekeningnummer voor wisselkoerswinst of -verlies in.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-137">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span> <span data-ttu-id="8d1e4-138">Voer de wisselkoerswinst of - verlies in het veld **Bedrag** in met of zonder een minteken voor respectievelijk debet- en creditbedragen.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-138">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign for credits and debits respectively.</span></span>
13. <span data-ttu-id="8d1e4-139">Boek het dagboek.</span><span class="sxs-lookup"><span data-stu-id="8d1e4-139">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="8d1e4-140">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8d1e4-140">See Also</span></span>
[<span data-ttu-id="8d1e4-141">Bankrekeningen reconciliëren</span><span class="sxs-lookup"><span data-stu-id="8d1e4-141">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="8d1e4-142">Bankieren instellen</span><span class="sxs-lookup"><span data-stu-id="8d1e4-142">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="8d1e4-143">Werken met diversendagboeken</span><span class="sxs-lookup"><span data-stu-id="8d1e4-143">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="8d1e4-144">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8d1e4-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
