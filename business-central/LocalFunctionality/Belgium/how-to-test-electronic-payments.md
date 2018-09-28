---
title: Elektronische betalingen testen
description: Nadat u elektronisch bankieren hebt ingesteld en betalingsvoorstellen hebt gegenereerd, kunt u de betalingsdagboekregels op fouten testen voordat u ze boekt.
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
ms.openlocfilehash: b38cc5fda1718d38e947b456bf404e15f06c8aad
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="test-electronic-payments"></a><span data-ttu-id="bd009-103">Elektronische betalingen testen</span><span class="sxs-lookup"><span data-stu-id="bd009-103">Test Electronic Payments</span></span>
> [!Note]
> [!INCLUDE[onprem_only](../../includes/onprem_only_md.md)]

<span data-ttu-id="bd009-104">Nadat u elektronisch bankieren hebt ingesteld en betalingsvoorstellen hebt gegenereerd, kunt u de betalingsdagboekregels op fouten testen voordat u ze boekt.</span><span class="sxs-lookup"><span data-stu-id="bd009-104">After you have set up electronic banking and generated payment suggestions, you can test the payment journal lines for errors before posting them.</span></span>  

<span data-ttu-id="bd009-105">Hierbij wordt onder andere het volgende gevalideerd:</span><span class="sxs-lookup"><span data-stu-id="bd009-105">Some of the information that is validated includes:</span></span>  

- <span data-ttu-id="bd009-106">Bankrekeningnummers zijn geldig.</span><span class="sxs-lookup"><span data-stu-id="bd009-106">Bank accounts numbers are valid.</span></span>  
- <span data-ttu-id="bd009-107">Positieve betalingsregels zijn aanwezig.</span><span class="sxs-lookup"><span data-stu-id="bd009-107">Positive payment lines are present.</span></span>  
- <span data-ttu-id="bd009-108">Of binnenlandse en internationale betalingen via slechts één rekening worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="bd009-108">If domestic and international payments are made from only one bank account.</span></span>  
- <span data-ttu-id="bd009-109">Of slechts één bankrekening kan worden gebruikt voor Isabel.</span><span class="sxs-lookup"><span data-stu-id="bd009-109">If only one bank account can be used for Isabel.</span></span>  
- <span data-ttu-id="bd009-110">Of betalingsregels in euro's worden weergegeven voor SEPA.</span><span class="sxs-lookup"><span data-stu-id="bd009-110">If payment lines are in Euro for SEPA.</span></span>  
- <span data-ttu-id="bd009-111">Of er een nummerreeks voor SEPA is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="bd009-111">If a number series has been defined for SEPA.</span></span>  

<span data-ttu-id="bd009-112">U kunt de fouten bekijken in het venster **Logboeken voor controlefouten exporteren**.</span><span class="sxs-lookup"><span data-stu-id="bd009-112">You can view any errors in the **Export Check Error Logs** window.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="bd009-113">U moet alle fouten corrigeren voordat u de regels kunt boeken.</span><span class="sxs-lookup"><span data-stu-id="bd009-113">You have to correct all errors before you can post the lines.</span></span>  

## <a name="to-test-payment-journal-lines"></a><span data-ttu-id="bd009-114">Betalingsdagboekregels testen</span><span class="sxs-lookup"><span data-stu-id="bd009-114">To test payment journal lines</span></span>  

1.  <span data-ttu-id="bd009-115">Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsdagboeken** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="bd009-115">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="bd009-116">Selecteer in het veld **Batchnaam** de vereiste dagboekbatch.</span><span class="sxs-lookup"><span data-stu-id="bd009-116">In the **Batch Name** field, select the required journal batch.</span></span>  
3.  <span data-ttu-id="bd009-117">Selecteer in het veld **Exportprotocol** het exportprotocol.</span><span class="sxs-lookup"><span data-stu-id="bd009-117">In the **Export Protocol** field, select the export protocol.</span></span>  
4.  <span data-ttu-id="bd009-118">Voer de betalingsdagboekregelinformatie in en kies vervolgens de actie **Betalingsregels controleren** om de betalingsdagboekregels te valideren.</span><span class="sxs-lookup"><span data-stu-id="bd009-118">Enter the payment journal line information, and then choose the **Check Payment Lines** action to validate the payment journal lines.</span></span> <span data-ttu-id="bd009-119">Welke validatie op de dagboekregels wordt uitgevoerd, is afhankelijk van de soort controle die in het venster **Exportprotocollen** is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="bd009-119">The validation that is performed on the journal lines depends on the type of check that is specified in the **Export Protocols** window.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bd009-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="bd009-120">See Also</span></span>  
 <span data-ttu-id="bd009-121">[Belgische elektronische betalingen](belgian-electronic-payments.md) </span><span class="sxs-lookup"><span data-stu-id="bd009-121">[Belgian Electronic Payments](belgian-electronic-payments.md) </span></span>  
 <span data-ttu-id="bd009-122">[Leveranciers voor automatische betalingsvoorstellen instellen](how-to-set-up-vendors-for-automatic-payment-suggestions.md) </span><span class="sxs-lookup"><span data-stu-id="bd009-122">[Set Up Vendors for Automatic Payment Suggestions](how-to-set-up-vendors-for-automatic-payment-suggestions.md) </span></span>  
 <span data-ttu-id="bd009-123">[Betalingsvoorstellen genereren](how-to-generate-payment-suggestions.md) </span><span class="sxs-lookup"><span data-stu-id="bd009-123">[Generate Payment Suggestions](how-to-generate-payment-suggestions.md) </span></span>  
 [<span data-ttu-id="bd009-124">Betalingsbestanden afdrukken</span><span class="sxs-lookup"><span data-stu-id="bd009-124">Print Payment Files</span></span>](how-to-print-payment-files.md)

