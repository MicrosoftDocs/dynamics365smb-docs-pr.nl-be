---
title: CODA-bankafschriften
description: CODA (geCOdeerd DAgafschrift) is een nationale bankstandaard, ontworpen door de Belgische Vereniging van Banken, waarmee elektronische bankafschriften automatisch kunnen worden verwerkt.
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
ms.openlocfilehash: bd2a7465c9b7264c7084b2abf899caab55293e6c
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1237546"
---
# <a name="coda-bank-statements"></a><span data-ttu-id="1529e-103">CODA-bankafschriften</span><span class="sxs-lookup"><span data-stu-id="1529e-103">CODA Bank Statements</span></span>
<span data-ttu-id="1529e-104">CODA (geCOdeerd DAgafschrift) is een nationale bankstandaard, ontworpen door de Belgische Vereniging van Banken, waarmee elektronische bankafschriften automatisch kunnen worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="1529e-104">The Coded Statement of Account (CODA) is a national banking standard, designed by the Belgian Banker's Association, which allows you to automatically process electronic bank statements.</span></span>  

<span data-ttu-id="1529e-105">Aan elke soort transactie in een CODA-afschrift wordt een unieke code toegewezen.</span><span class="sxs-lookup"><span data-stu-id="1529e-105">Each type of transaction in a CODA statement is assigned a unique code.</span></span> [!INCLUDE[d365fin](../../includes/d365fin_md.md)] <span data-ttu-id="1529e-106">gebruikt deze code om transacties te interpreteren en deze te vereffenen met de betreffende posten.</span><span class="sxs-lookup"><span data-stu-id="1529e-106">uses this code to interpret transactions and apply them to the corresponding ledger entries.</span></span>  

## <a name="applying-statement-lines"></a><span data-ttu-id="1529e-107">Afschriftregels vereffenen</span><span class="sxs-lookup"><span data-stu-id="1529e-107">Applying Statement Lines</span></span>  
<span data-ttu-id="1529e-108">Wanneer u een CODA-afschrift hebt geïmporteerd, kunt u de afschriftregels vereffenen met bestaande posten, op basis van de gegevens in de tabel **Transactiecodering**.</span><span class="sxs-lookup"><span data-stu-id="1529e-108">When you have imported a CODA statement, you can apply the statement lines to existing ledger entries, based on the information in the **Transaction Coding** table.</span></span>  

<span data-ttu-id="1529e-109">Als de transactiecodering van de afschriftregel niet wordt gevonden, stopt [!INCLUDE[d365fin](../../includes/d365fin_md.md)] met de verwerking en wordt doorgegaan naar de volgende afschriftregel.</span><span class="sxs-lookup"><span data-stu-id="1529e-109">If the transaction coding of the statement line is not found, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] will stop processing and continue with the next statement line.</span></span> <span data-ttu-id="1529e-110">Als u het veld **Standaardboeking** selecteert, wordt de afschriftregel als standaardboeking gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1529e-110">If you select the **Default Posting** field, the statement line will be used as a default posting.</span></span>  

<span data-ttu-id="1529e-111">Als de transactiecodering van de afschriftregel wordt gevonden, worden de afschriftregels vergeleken met de volgende rekeningsoorten en bijbehorende rekeningnummers:</span><span class="sxs-lookup"><span data-stu-id="1529e-111">If the transaction coding of the statement line is found, the statement lines will be matched to the following account types and corresponding account numbers:</span></span>  

- <span data-ttu-id="1529e-112">Grootboek: als de rekeningsoort een grootboekrekening is, wordt de afschriftregel geboekt op de bijhorende grootboekrekening.</span><span class="sxs-lookup"><span data-stu-id="1529e-112">General ledger - If the account type is general ledger account, the statement line is posted on the corresponding general ledger account.</span></span>  

- <span data-ttu-id="1529e-113">Klant of leverancier: als de rekeningsoort een klant- of leveranciersrekening is, wordt een overeenkomende klant- of leverancierspost gevonden op basis van de volgende criteria:</span><span class="sxs-lookup"><span data-stu-id="1529e-113">Customer or vendor - If the account type is customer or vendor, a matching customer or vendor ledger entry is found based on the following criteria:</span></span>  

    - <span data-ttu-id="1529e-114">Als een post met de standaardindeling wordt gevonden, wordt de post vergeleken met de afschriftregel en wordt de vereffeningsstatus ingesteld op **Vereffend**.</span><span class="sxs-lookup"><span data-stu-id="1529e-114">If a ledger entry is found using the standard format, the ledger entry will be matched to the statement line and the application status will be set to **Applied**.</span></span> <span data-ttu-id="1529e-115">Als de post niet de standaardindeling gebruikt, wordt het bankrekeningnummer van de klant of leverancier gebruikt om de klant of leverancier te vinden.</span><span class="sxs-lookup"><span data-stu-id="1529e-115">If the ledger entry does not use the standard format, the bank account number of the customer or vendor is used to find the customer or vendor.</span></span>  

    - <span data-ttu-id="1529e-116">Als er geen post met een corresponderend restbedrag wordt gevonden, wordt de klant- of leveranciersrekening gebruikt en wordt de vereffeningsstatus ingesteld op **Gedeeltelijk vereffend**.</span><span class="sxs-lookup"><span data-stu-id="1529e-116">If no ledger entry with a matching remaining amount is found, the customer or vendor account is used and the application status will be set to **Partly Applied**.</span></span>  

    - <span data-ttu-id="1529e-117">Als het bankrekeningnummer wordt gebruikt om de klant of leverancier te zoeken, wordt een bijbehorende post gevonden op basis van het bedrag van de afschriftregel.</span><span class="sxs-lookup"><span data-stu-id="1529e-117">If the bank account number is used to find the customer or vendor, a matching ledger entry is found based on the amount of the statement line.</span></span> <span data-ttu-id="1529e-118">Als het bedrag wordt gevonden, wordt de afschriftregel vergeleken met de bijbehorende post en wordt de vereffeningsstatus ingesteld op **Vereffend**.</span><span class="sxs-lookup"><span data-stu-id="1529e-118">If the amount is found, the statement line is matched to the corresponding ledger entry and the application status will be set to **Applied**.</span></span>  

    - <span data-ttu-id="1529e-119">Als het bankrekeningnummer niet kan worden gebruikt om de klant of leverancier te zoeken, wordt in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] gestopt met de verwerking of wordt de huidige regel als standaardboeking gebruikt, voordat wordt doorgegaan met de volgende afschriftregel.</span><span class="sxs-lookup"><span data-stu-id="1529e-119">If the bank account number cannot be used to find the customer or vendor, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] will either stop processing the current line or use the line as a default posting, before continuing with the next statement line.</span></span>  

<span data-ttu-id="1529e-120">U kunt het proces zo vaak uitvoeren als u wilt.</span><span class="sxs-lookup"><span data-stu-id="1529e-120">You can run the process as many times as you like.</span></span> <span data-ttu-id="1529e-121">Alleen afschriftregels met een lege vereffeningsstatus worden vereffend.</span><span class="sxs-lookup"><span data-stu-id="1529e-121">Only statement lines with a blank application status will be applied.</span></span>  

<span data-ttu-id="1529e-122">Wanneer u alle afschriftregels hebt vereffend met een grootboekrekening of een bijbehorende klanten- of leverancierspost, kunt u de CODA-afschriftregels boeken.</span><span class="sxs-lookup"><span data-stu-id="1529e-122">When you have applied all statement lines to a general ledger account or to a matching customer ledger entry or vendor ledger entry, you are ready to post the CODA statement lines.</span></span> <span data-ttu-id="1529e-123">Zie voor meer informatie [CODA-afschriften automatisch overbrengen en boeken](how-to-manually-transfer-and-post-coda-statements.md).</span><span class="sxs-lookup"><span data-stu-id="1529e-123">For more information, see [Automatically Transfer and Post CODA Statements](how-to-manually-transfer-and-post-coda-statements.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="1529e-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1529e-124">See Also</span></span>  
 <span data-ttu-id="1529e-125">[Elektronisch bankieren voor België](belgian-electronic-banking.md) </span><span class="sxs-lookup"><span data-stu-id="1529e-125">[Belgian Electronic Banking](belgian-electronic-banking.md) </span></span>  
 <span data-ttu-id="1529e-126">[Bankrekeningen instellen voor CODA](how-to-set-up-bank-accounts-for-coda.md) </span><span class="sxs-lookup"><span data-stu-id="1529e-126">[Set Up Bank Accounts for CODA](how-to-set-up-bank-accounts-for-coda.md) </span></span>  
 <span data-ttu-id="1529e-127">[IBLC-BLWI-transactiecodes instellen](how-to-set-up-iblc-blwi-transaction-codes.md) </span><span class="sxs-lookup"><span data-stu-id="1529e-127">[Set Up IBLC-BLWI Transaction Codes](how-to-set-up-iblc-blwi-transaction-codes.md) </span></span>  
 <span data-ttu-id="1529e-128">[CODA-afschriften importeren](how-to-import-coda-statements.md) </span><span class="sxs-lookup"><span data-stu-id="1529e-128">[Import CODA Statements](how-to-import-coda-statements.md) </span></span>  
 <span data-ttu-id="1529e-129">[CODA-afschriften vereffenen](how-to-apply-coda-statements.md) </span><span class="sxs-lookup"><span data-stu-id="1529e-129">[Apply CODA Statements](how-to-apply-coda-statements.md) </span></span>  
 <span data-ttu-id="1529e-130">[Financiële dagboeken maken](how-to-create-financial-journals.md) </span><span class="sxs-lookup"><span data-stu-id="1529e-130">[Create Financial Journals](how-to-create-financial-journals.md) </span></span>  
 <span data-ttu-id="1529e-131">[CODA-afschriften automatisch overbrengen en boeken](how-to-automatically-transfer-and-post-coda-statements.md) </span><span class="sxs-lookup"><span data-stu-id="1529e-131">[Automatically Transfer and Post CODA Statements](how-to-automatically-transfer-and-post-coda-statements.md) </span></span>  
 [<span data-ttu-id="1529e-132">CODA-afschriften handmatig overbrengen en boeken</span><span class="sxs-lookup"><span data-stu-id="1529e-132">Manually Transfer and Post CODA Statements</span></span>](how-to-manually-transfer-and-post-coda-statements.md)
