---
title: Betalingsregels en dagboekregels samenvatten
description: In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] worden verschillende soorten transacties op dezelfde manier afgehandeld.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1be4e60b54340f10e985e794a0d571d91aace05f
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="summarizing-payment-lines-and-general-journal-lines"></a><span data-ttu-id="1487b-103">Betalingsregels en dagboekregels samenvatten</span><span class="sxs-lookup"><span data-stu-id="1487b-103">Summarizing Payment Lines and General Journal Lines</span></span>
<span data-ttu-id="1487b-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] worden de volgende soorten transacties op dezelfde manier afgehandeld:</span><span class="sxs-lookup"><span data-stu-id="1487b-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] handles the following types of transactions in the same way:</span></span>  

- <span data-ttu-id="1487b-105">Binnenlandse betalingen</span><span class="sxs-lookup"><span data-stu-id="1487b-105">Domestic payments</span></span>  
- <span data-ttu-id="1487b-106">Internationale betalingen</span><span class="sxs-lookup"><span data-stu-id="1487b-106">International payments</span></span>  
- <span data-ttu-id="1487b-107">SEPA-betalingen</span><span class="sxs-lookup"><span data-stu-id="1487b-107">SEPA payments</span></span>  
- <span data-ttu-id="1487b-108">Niet-euro SEPA-betalingen</span><span class="sxs-lookup"><span data-stu-id="1487b-108">Non-euro SEPA payments</span></span>  

## <a name="how-payment-journal-lines-are-transferred-to-the-general-journal"></a><span data-ttu-id="1487b-109">Hoe betalingsdagboekregels naar het grootboek worden overgebracht</span><span class="sxs-lookup"><span data-stu-id="1487b-109">How Payment Journal Lines are Transferred to the General Journal</span></span>  
<span data-ttu-id="1487b-110">Wanneer u de betalingsdagboekregels naar een bestand exporteert, brengt [!INCLUDE[d365fin](../../includes/d365fin_md.md)] de betalingsdagboekregels naar het opgegeven dagboek over.</span><span class="sxs-lookup"><span data-stu-id="1487b-110">When you export the payment journal lines to a file, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] transfers the payment journal lines to the specified general journal.</span></span> <span data-ttu-id="1487b-111">Standaard wordt een dagboekregel gemaakt voor elke betalingsdagboekregel.</span><span class="sxs-lookup"><span data-stu-id="1487b-111">By default, a general journal line is created for each payment journal line.</span></span>  

<span data-ttu-id="1487b-112">De volgende twee velden in het venster **Elektronisch bankieren instellen** bepalen hoe de betalingsregels worden samengevat:</span><span class="sxs-lookup"><span data-stu-id="1487b-112">The following two fields in the **Electronic Banking Setup** window affect how the payment lines are summarized:</span></span>  

- <span data-ttu-id="1487b-113">**Alg. dagb.regels samenvatten**</span><span class="sxs-lookup"><span data-stu-id="1487b-113">**Summarize Gen. Jnl. Lines**</span></span>  
- <span data-ttu-id="1487b-114">**Tekst van betaalberichten afbreken**</span><span class="sxs-lookup"><span data-stu-id="1487b-114">**Cut off Payment Message Texts**</span></span>  

<span data-ttu-id="1487b-115">Als u het selectievakje **Alg. dagb.regels samenvatten** in het venster **Elektronisch bankieren instellen** hebt geselecteerd, vat [!INCLUDE[d365fin](../../includes/d365fin_md.md)] alle betalingsdagboekregels voor een bepaalde leverancier in één dagboekregel samen.</span><span class="sxs-lookup"><span data-stu-id="1487b-115">If you have selected the **Summarize Gen. Jnl. Lines** check box in the **Electronic Banking Setup** window, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] summarizes all payment journal lines for a specific vendor into one general journal line.</span></span> <span data-ttu-id="1487b-116">De algemene omschrijving 'Betaling %1', waarbij %1 het leveranciersnummer is, wordt gebruikt voor de samengevatte dagboekregelomschrijving.</span><span class="sxs-lookup"><span data-stu-id="1487b-116">The general description "Payment %1," where %1 is the vendor number, is used for the summarized journal line description.</span></span> <span data-ttu-id="1487b-117">Er worden een afzonderlijke betalingsregel en een aparte dagboekregel gemaakt om het volgende af te handelen:</span><span class="sxs-lookup"><span data-stu-id="1487b-117">A separate payment line and a separate general journal line are created to handle:</span></span>  

- <span data-ttu-id="1487b-118">Betalingsdagboekregels die gedeeltelijke betalingen bevatten, met zowel het veld **Gedeeltelijke betaling** als het veld **Afzonderlijke regel** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="1487b-118">Payment journal lines that contain partial payments, with both the **Partial Payment** and the **Separate Line** fields selected.</span></span>  

- <span data-ttu-id="1487b-119">Betalingsdagboekregels die een bericht met een standaardindeling bevatten (dus slagen voor de MOD97-test), waarmee **Bericht met standaardindeling** op Waar wordt ingesteld in het dagboek voor elektronisch bankieren.</span><span class="sxs-lookup"><span data-stu-id="1487b-119">Payment journal lines that contain a standard format message (that is, passes the MOD97 test), which sets **Standard Format Message** to True in the electronic banking journal.</span></span>  

## <a name="example-1"></a><span data-ttu-id="1487b-120">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="1487b-120">Example 1</span></span>  
<span data-ttu-id="1487b-121">In dit voorbeeld exporteert u betalingsregels en is het selectievakje **Alg. dagb.regels samenvatten** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="1487b-121">In this example, you export payment lines, and the **Summarize Gen. Jnl. Lines** check box is selected.</span></span> [!INCLUDE[d365fin](../../includes/d365fin_md.md)] <span data-ttu-id="1487b-122">maakt:</span><span class="sxs-lookup"><span data-stu-id="1487b-122"> creates:</span></span>  

- <span data-ttu-id="1487b-123">Een gecombineerde betalingsregel in een XML-bestand met een samengevoegd betalingsbericht.</span><span class="sxs-lookup"><span data-stu-id="1487b-123">One combined payment line in a XML file that has a concatenated payment message.</span></span> <span data-ttu-id="1487b-124">Spaties zijn het scheidingsteken.</span><span class="sxs-lookup"><span data-stu-id="1487b-124">White space is the delimiter.</span></span>  
- <span data-ttu-id="1487b-125">Eén betaling in het grootboek met een algemene beschrijving die ../../de leveranciersnaam bevat.</span><span class="sxs-lookup"><span data-stu-id="1487b-125">One payment line in the general journal with a generic description that ../../includes the vendor name.</span></span>  

## <a name="example-2"></a><span data-ttu-id="1487b-126">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="1487b-126">Example 2</span></span>  
<span data-ttu-id="1487b-127">In dit voorbeeld exporteert u betalingsregels en is het selectievakje **Alg. dagb.regels samenvatten** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="1487b-127">In this example, you export payment lines, and the **Summarize Gen. Jnl. Lines** check box is selected.</span></span> <span data-ttu-id="1487b-128">Het selectievakje **Tekst van betaalberichten afbreken** wordt gewist en gecombineerde SEPA- en niet-auto SEPA-betalingsregels overschrijden 140 tekens in het betalingsbericht.</span><span class="sxs-lookup"><span data-stu-id="1487b-128">The **Cut off Payment Message Texts** check box is cleared, and combined SEPA and non-euro SEPA payment lines exceed 140 characters in payment message.</span></span> [!INCLUDE[d365fin](../../includes/d365fin_md.md)] <span data-ttu-id="1487b-129">maakt:</span><span class="sxs-lookup"><span data-stu-id="1487b-129"> creates:</span></span>  

- <span data-ttu-id="1487b-130">Twee gecombineerde betalingsregels in een XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="1487b-130">Two combined payment lines in a XML file.</span></span> <span data-ttu-id="1487b-131">De eerste betalingsregel bevat de eerste samengevoegde betalingsberichten.</span><span class="sxs-lookup"><span data-stu-id="1487b-131">The first payment line contains the first concatenated payment messages.</span></span> <span data-ttu-id="1487b-132">De tweede betalingsregel bevat het betalingsbericht vanaf de derde regel.</span><span class="sxs-lookup"><span data-stu-id="1487b-132">The second payment line contains the payment message from the third line.</span></span>  

- <span data-ttu-id="1487b-133">Eén betaling in het grootboek met een algemene beschrijving die ../../de leveranciersnaam bevat.</span><span class="sxs-lookup"><span data-stu-id="1487b-133">One payment line in the general journal with a generic description that ../../includes the vendor name.</span></span>  

## <a name="example-3"></a><span data-ttu-id="1487b-134">Voorbeeld 3</span><span class="sxs-lookup"><span data-stu-id="1487b-134">Example 3</span></span>  
<span data-ttu-id="1487b-135">In dit voorbeeld exporteert u betalingsregels en is het selectievakje **Alg. dagb.regels samenvatten** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="1487b-135">In this example, you export payment lines, and the **Summarize Gen. Jnl. Lines** check box is selected.</span></span> <span data-ttu-id="1487b-136">Het selectievakje **Tekst van betaalberichten afbreken** wordt ook ingeschakeld en gecombineerde SEPA- en niet-SEPA betalingsregels overschrijden 140 tekens in het betalingsbericht.</span><span class="sxs-lookup"><span data-stu-id="1487b-136">The **Cut off Payment Message Texts** check box is also selected and combined SEPA and non-SEPA payment lines exceed 140 characters in payment message.</span></span> [!INCLUDE[d365fin](../../includes/d365fin_md.md)] <span data-ttu-id="1487b-137">maakt:</span><span class="sxs-lookup"><span data-stu-id="1487b-137"> creates:</span></span>  

- <span data-ttu-id="1487b-138">Eén gecombineerde betalingsregel in een XML-bestand met twee samengevoegde betalingsberichten.</span><span class="sxs-lookup"><span data-stu-id="1487b-138">One combined payment line in a XML file that has two concatenated payment messages.</span></span> <span data-ttu-id="1487b-139">Een beletselteken (…) wordt gebruikt om aan te geven dat het bericht afgekapt is.</span><span class="sxs-lookup"><span data-stu-id="1487b-139">An ellipsis (…) is used to indicate that the message is truncated.</span></span>  

- <span data-ttu-id="1487b-140">Eén betalingsregel in het grootboek met een algemene beschrijving die de leveranciersnaam bevat.</span><span class="sxs-lookup"><span data-stu-id="1487b-140">One payment line in the general journal with a generic description that includes the vendor name.</span></span>  

<span data-ttu-id="1487b-141">Op basis van de XML-structuur worden betalingen samengevat per rekeningnummer en bankrekeningnummer van de begunstigde en bankrekening. Het bankrekeningfilter mag leeg zijn.</span><span class="sxs-lookup"><span data-stu-id="1487b-141">Based on the XML structure, the payments are summarized per account number and beneficiary bank account no and bank account no. The bank account filter can be empty.</span></span>  

<span data-ttu-id="1487b-142">De EndToEndId in het SEPA-bericht wordt gehaald uit het betalingsbericht en kan worden afgekapt tot de maximumlengte van 45 tekens.</span><span class="sxs-lookup"><span data-stu-id="1487b-142">The EndToEndId in the SEPA message is taken from the payment message and can be truncated to the maximum length of 45 characters.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1487b-143">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1487b-143">See Also</span></span>  
 <span data-ttu-id="1487b-144">[Elektronisch bankieren instellen](how-to-set-up-electronic-banking.md) </span><span class="sxs-lookup"><span data-stu-id="1487b-144">[Set Up Electronic Banking](how-to-set-up-electronic-banking.md) </span></span>  
 [<span data-ttu-id="1487b-145">Financiën instellen</span><span class="sxs-lookup"><span data-stu-id="1487b-145">Setting Up Finance</span></span>](../../finance-setup-finance.md)  
 [<span data-ttu-id="1487b-146">Inkopen vastleggen</span><span class="sxs-lookup"><span data-stu-id="1487b-146">Record Purchases</span></span>](../../purchasing-how-record-purchases.md) 

