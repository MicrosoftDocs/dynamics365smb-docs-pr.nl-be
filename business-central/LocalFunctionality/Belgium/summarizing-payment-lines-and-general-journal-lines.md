---
title: Betalingsregels en dagboekregels samenvatten
description: Business Central geeft een overzicht van betalingsregels en dagboekregels.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: a3418af9a7865a051cfbb6d2fc2e2b12953fe8c9
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778404"
---
# <a name="summarizing-payment-lines-and-general-journal-lines"></a><span data-ttu-id="e3852-103">Betalingsregels en dagboekregels samenvatten</span><span class="sxs-lookup"><span data-stu-id="e3852-103">Summarizing Payment Lines and General Journal Lines</span></span>
<span data-ttu-id="e3852-104">Business Central geeft een overzicht van betalingsregels en dagboekregels van de volgende typen betalingen:</span><span class="sxs-lookup"><span data-stu-id="e3852-104">Business Central summarizes payment lines and journal line across the following types of payments:</span></span>  

- <span data-ttu-id="e3852-105">Binnenlandse betalingen</span><span class="sxs-lookup"><span data-stu-id="e3852-105">Domestic payments</span></span>  
- <span data-ttu-id="e3852-106">Internationale betalingen</span><span class="sxs-lookup"><span data-stu-id="e3852-106">International payments</span></span>  
- <span data-ttu-id="e3852-107">SEPA-betalingen</span><span class="sxs-lookup"><span data-stu-id="e3852-107">SEPA payments</span></span>  
- <span data-ttu-id="e3852-108">Niet-euro SEPA-betalingen</span><span class="sxs-lookup"><span data-stu-id="e3852-108">Non-euro SEPA payments</span></span>  

## <a name="how-payment-journal-lines-are-transferred-to-the-general-journal"></a><span data-ttu-id="e3852-109">Hoe betalingsdagboekregels naar het grootboek worden overgebracht</span><span class="sxs-lookup"><span data-stu-id="e3852-109">How Payment Journal Lines are Transferred to the General Journal</span></span>  
<span data-ttu-id="e3852-110">Wanneer u de betalingsdagboekregels naar een bestand exporteert, brengt [!INCLUDE[d365fin](../../includes/d365fin_md.md)] de betalingsdagboekregels naar het opgegeven dagboek over.</span><span class="sxs-lookup"><span data-stu-id="e3852-110">When you export the payment journal lines to a file, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] transfers the payment journal lines to the specified general journal.</span></span> <span data-ttu-id="e3852-111">Standaard wordt een dagboekregel gemaakt voor elke betalingsdagboekregel.</span><span class="sxs-lookup"><span data-stu-id="e3852-111">By default, a general journal line is created for each payment journal line.</span></span>  

<span data-ttu-id="e3852-112">De volgende twee velden op de pagina **Elektronisch bankieren instellen** bepalen hoe de betalingsregels worden samengevat:</span><span class="sxs-lookup"><span data-stu-id="e3852-112">The following two fields on the **Electronic Banking Setup** page affect how the payment lines are summarized:</span></span>  

- <span data-ttu-id="e3852-113">**Alg. dagb.regels samenvatten**</span><span class="sxs-lookup"><span data-stu-id="e3852-113">**Summarize Gen. Jnl. Lines**</span></span>  
- <span data-ttu-id="e3852-114">**Tekst van betaalberichten afbreken**</span><span class="sxs-lookup"><span data-stu-id="e3852-114">**Cut off Payment Message Texts**</span></span>  

<span data-ttu-id="e3852-115">Als u het selectievakje **Alg. dagb.regels samenvatten** op de pagina **Elektronisch bankieren instellen** hebt geselecteerd, vat [!INCLUDE[d365fin](../../includes/d365fin_md.md)] alle betalingsdagboekregels voor een bepaalde leverancier in één dagboekregel samen.</span><span class="sxs-lookup"><span data-stu-id="e3852-115">If you have selected the **Summarize Gen. Jnl. Lines** check box on the **Electronic Banking Setup** page, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] summarizes all payment journal lines for a specific vendor into one general journal line.</span></span> <span data-ttu-id="e3852-116">De algemene beschrijving "Betaling %1", waarbij %1 het nummer van de leverancier is, wordt gebruikt voor de beknopte journaalregelbeschrijving.</span><span class="sxs-lookup"><span data-stu-id="e3852-116">The general description "Payment %1," where %1 is the vendor number, is used for the summarized journal line description.</span></span> <span data-ttu-id="e3852-117">Er worden een afzonderlijke betalingsregel en een aparte dagboekregel gemaakt om het volgende af te handelen:</span><span class="sxs-lookup"><span data-stu-id="e3852-117">A separate payment line and a separate general journal line are created to handle:</span></span>  

- <span data-ttu-id="e3852-118">Betalingsdagboekregels die gedeeltelijke betalingen bevatten, met zowel het veld **Gedeeltelijke betaling** als het veld **Afzonderlijke regel** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="e3852-118">Payment journal lines that contain partial payments, with both the **Partial Payment** and the **Separate Line** fields selected.</span></span>  

- <span data-ttu-id="e3852-119">Betalingsdagboekregels die een bericht met een standaardindeling bevatten (slagen voor de MOD97-test), waarmee **Bericht met standaardindeling** op Waar wordt ingesteld in het dagboek voor elektronisch bankieren.</span><span class="sxs-lookup"><span data-stu-id="e3852-119">Payment journal lines that contain a standard format message (passes the MOD97 test), which sets **Standard Format Message** to True in the electronic banking journal.</span></span>

## <a name="example-1"></a><span data-ttu-id="e3852-120">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="e3852-120">Example 1</span></span>  
<span data-ttu-id="e3852-121">In dit voorbeeld exporteert u betalingsregels en is het selectievakje **Alg. dagb.regels samenvatten** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="e3852-121">In this example, you export payment lines, and the **Summarize Gen. Jnl. Lines** check box is selected.</span></span> [!INCLUDE[d365fin](../../includes/d365fin_md.md)] <span data-ttu-id="e3852-122">maakt:</span><span class="sxs-lookup"><span data-stu-id="e3852-122">creates:</span></span>  

- <span data-ttu-id="e3852-123">Een gecombineerde betalingsregel in een XML-bestand met een samengevoegd betalingsbericht.</span><span class="sxs-lookup"><span data-stu-id="e3852-123">One combined payment line in an XML file that has a concatenated payment message.</span></span> <span data-ttu-id="e3852-124">Spaties zijn het scheidingsteken.</span><span class="sxs-lookup"><span data-stu-id="e3852-124">White space is the delimiter.</span></span>  
- <span data-ttu-id="e3852-125">Eén betalingsregel in het grootboek met een algemene beschrijving die de leveranciersnaam bevat.</span><span class="sxs-lookup"><span data-stu-id="e3852-125">One payment line in the general journal with a generic description that includes the vendor name.</span></span>  

## <a name="example-2"></a><span data-ttu-id="e3852-126">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="e3852-126">Example 2</span></span>  
<span data-ttu-id="e3852-127">In dit voorbeeld exporteert u betalingsregels en is het selectievakje **Alg. dagb.regels samenvatten** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="e3852-127">In this example, you export payment lines, and the **Summarize Gen. Jnl. Lines** check box is selected.</span></span> <span data-ttu-id="e3852-128">Het selectievakje **Tekst van betaalberichten afbreken** wordt gewist en de gecombineerde SEPA- en niet-auto SEPA-betalingsregels overschrijden 140 tekens in het betalingsbericht.</span><span class="sxs-lookup"><span data-stu-id="e3852-128">The **Cut off Payment Message Texts** check box is cleared, and the combined SEPA and non-euro SEPA payment lines exceed 140 characters in the payment message.</span></span> [!INCLUDE[d365fin](../../includes/d365fin_md.md)] <span data-ttu-id="e3852-129">maakt:</span><span class="sxs-lookup"><span data-stu-id="e3852-129">creates:</span></span>  

- <span data-ttu-id="e3852-130">Twee gecombineerde betalingsregels in een XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="e3852-130">Two combined payment lines in an XML file.</span></span> <span data-ttu-id="e3852-131">De eerste betalingsregel bevat de eerste samengevoegde betalingsberichten.</span><span class="sxs-lookup"><span data-stu-id="e3852-131">The first payment line contains the first concatenated payment messages.</span></span> <span data-ttu-id="e3852-132">De tweede betalingsregel bevat het betalingsbericht vanaf de derde regel.</span><span class="sxs-lookup"><span data-stu-id="e3852-132">The second payment line contains the payment message from the third line.</span></span>  

- <span data-ttu-id="e3852-133">Eén betalingsregel in het grootboek met een algemene beschrijving die de leveranciersnaam bevat.</span><span class="sxs-lookup"><span data-stu-id="e3852-133">One payment line in the general journal with a generic description that includes the vendor name.</span></span>  

## <a name="example-3"></a><span data-ttu-id="e3852-134">Voorbeeld 3</span><span class="sxs-lookup"><span data-stu-id="e3852-134">Example 3</span></span>  
<span data-ttu-id="e3852-135">In dit voorbeeld exporteert u betalingsregels en is het selectievakje **Alg. dagb.regels samenvatten** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="e3852-135">In this example, you export payment lines, and the **Summarize Gen. Jnl. Lines** check box is selected.</span></span> <span data-ttu-id="e3852-136">Het selectievakje **Tekst van betaalberichten afbreken** wordt ook ingeschakeld en de gecombineerde SEPA- en niet-SEPA betalingsregels overschrijden 140 tekens in het betalingsbericht.</span><span class="sxs-lookup"><span data-stu-id="e3852-136">The **Cut off Payment Message Texts** check box is also selected, and the combined SEPA and non-SEPA payment lines exceed 140 characters in the payment message.</span></span> [!INCLUDE[d365fin](../../includes/d365fin_md.md)] <span data-ttu-id="e3852-137">maakt:</span><span class="sxs-lookup"><span data-stu-id="e3852-137">creates:</span></span>  

- <span data-ttu-id="e3852-138">Eén gecombineerde betalingsregel in een XML-bestand met twee samengevoegde betalingsberichten.</span><span class="sxs-lookup"><span data-stu-id="e3852-138">One combined payment line in an XML file that has two concatenated payment messages.</span></span> <span data-ttu-id="e3852-139">Een beletselteken (…) wordt gebruikt om aan te geven dat het bericht afgekapt is.</span><span class="sxs-lookup"><span data-stu-id="e3852-139">An ellipsis (…) is used to indicate that the message is truncated.</span></span>  

- <span data-ttu-id="e3852-140">Eén betalingsregel in het grootboek met een algemene beschrijving die de leveranciersnaam bevat.</span><span class="sxs-lookup"><span data-stu-id="e3852-140">One payment line in the general journal with a generic description that includes the vendor name.</span></span>  

<span data-ttu-id="e3852-141">Op basis van de XML-structuur worden betalingen samengevat per rekeningnummer, bankrekeningnummer van de begunstigde en bankrekeningnummer.</span><span class="sxs-lookup"><span data-stu-id="e3852-141">Based on the XML structure, the payments are summarized per account number, beneficiary bank account number, and bank account number.</span></span> <span data-ttu-id="e3852-142">Het filter voor de bankrekening kan leeg zijn.</span><span class="sxs-lookup"><span data-stu-id="e3852-142">The bank account filter can be empty.</span></span>  

<span data-ttu-id="e3852-143">De EndToEndId in het SEPA-bericht wordt gehaald uit het betalingsbericht en kan worden afgekapt tot de maximumlengte van 45 tekens.</span><span class="sxs-lookup"><span data-stu-id="e3852-143">The EndToEndId in the SEPA message is taken from the payment message and can be truncated to the maximum length of 45 characters.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e3852-144">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e3852-144">See Also</span></span>  
 <span data-ttu-id="e3852-145">[Elektronisch bankieren instellen](how-to-set-up-electronic-banking.md) </span><span class="sxs-lookup"><span data-stu-id="e3852-145">[Set Up Electronic Banking](how-to-set-up-electronic-banking.md) </span></span>  
 [<span data-ttu-id="e3852-146">Financiën instellen</span><span class="sxs-lookup"><span data-stu-id="e3852-146">Setting Up Finance</span></span>](../../finance-setup-finance.md)  
 [<span data-ttu-id="e3852-147">Inkopen vastleggen</span><span class="sxs-lookup"><span data-stu-id="e3852-147">Record Purchases</span></span>](../../purchasing-how-record-purchases.md)
