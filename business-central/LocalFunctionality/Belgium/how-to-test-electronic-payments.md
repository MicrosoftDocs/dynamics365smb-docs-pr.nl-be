---
title: Elektronische betalingen testen
description: Nadat u elektronisch bankieren hebt ingesteld en betalingsvoorstellen hebt gegenereerd, kunt u de betalingsdagboekregels op fouten testen voordat u ze boekt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1fca14d85e9754b187297c145b6f228d60fb44fb
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379761"
---
# <a name="test-electronic-payments"></a><span data-ttu-id="c5da0-103">Elektronische betalingen testen</span><span class="sxs-lookup"><span data-stu-id="c5da0-103">Test Electronic Payments</span></span>
<span data-ttu-id="c5da0-104">Nadat u elektronisch bankieren hebt ingesteld en betalingsvoorstellen hebt gegenereerd, kunt u de betalingsdagboekregels op fouten testen voordat u ze boekt.</span><span class="sxs-lookup"><span data-stu-id="c5da0-104">After you have set up electronic banking and generated payment suggestions, you can test the payment journal lines for errors before posting them.</span></span>  

<span data-ttu-id="c5da0-105">Hierbij wordt onder andere het volgende gevalideerd:</span><span class="sxs-lookup"><span data-stu-id="c5da0-105">Some of the information that is validated includes:</span></span>  

- <span data-ttu-id="c5da0-106">Of bankrekeningnummers geldig zijn.</span><span class="sxs-lookup"><span data-stu-id="c5da0-106">Whether bank account numbers are valid.</span></span>  
- <span data-ttu-id="c5da0-107">Of positieve betalingsregels aanwezig zijn.</span><span class="sxs-lookup"><span data-stu-id="c5da0-107">Whether positive payment lines are present.</span></span>  
- <span data-ttu-id="c5da0-108">Of binnenlandse en internationale betalingen via slechts één rekening worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c5da0-108">Whether domestic and international payments are made from only one bank account.</span></span>  
- <span data-ttu-id="c5da0-109">Of er slechts één bankrekening kan worden gebruikt voor Isabel (Interbanks Standards Association Belgium).</span><span class="sxs-lookup"><span data-stu-id="c5da0-109">Whether only one bank account can be used for Interbanks Standards Association Belgium (Isabel).</span></span>  
- <span data-ttu-id="c5da0-110">Of betalingsregels in euro zijn voor SEPA (Single Euro Payments Area).</span><span class="sxs-lookup"><span data-stu-id="c5da0-110">Whether payment lines are in euro for Single Euro Payments Area (SEPA).</span></span>  
- <span data-ttu-id="c5da0-111">Of er een nummerreeks voor SEPA is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="c5da0-111">Whether a number series has been defined for SEPA.</span></span>  

<span data-ttu-id="c5da0-112">U kunt de fouten bekijken op de pagina **Logboeken voor controlefouten exporteren**.</span><span class="sxs-lookup"><span data-stu-id="c5da0-112">You can view any errors on the **Export Check Error Logs** page.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="c5da0-113">U moet alle fouten corrigeren voordat u de regels kunt boeken.</span><span class="sxs-lookup"><span data-stu-id="c5da0-113">You have to correct all errors before you can post the lines.</span></span>  

## <a name="to-test-payment-journal-lines"></a><span data-ttu-id="c5da0-114">Betalingsdagboekregels testen</span><span class="sxs-lookup"><span data-stu-id="c5da0-114">To test payment journal lines</span></span>  

1.  <span data-ttu-id="c5da0-115">Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsdagboeken** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="c5da0-115">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c5da0-116">Selecteer in het veld **Batchnaam** de vereiste dagboekbatch.</span><span class="sxs-lookup"><span data-stu-id="c5da0-116">In the **Batch Name** field, select the required journal batch.</span></span>  
3.  <span data-ttu-id="c5da0-117">Selecteer in het veld **Exportprotocol** het exportprotocol.</span><span class="sxs-lookup"><span data-stu-id="c5da0-117">In the **Export Protocol** field, select the export protocol.</span></span>  
4.  <span data-ttu-id="c5da0-118">Voer de betalingsdagboekregelinformatie in en kies vervolgens de actie **Betalingsregels controleren** om de betalingsdagboekregels te valideren.</span><span class="sxs-lookup"><span data-stu-id="c5da0-118">Enter the payment journal line information, and then choose the **Check Payment Lines** action to validate the payment journal lines.</span></span> <span data-ttu-id="c5da0-119">Welke validatie op de dagboekregels wordt uitgevoerd, is afhankelijk van de soort controle die op de pagina **Exportprotocollen** is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="c5da0-119">The validation that is performed on the journal lines depends on the type of check that is specified on the **Export Protocols** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c5da0-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c5da0-120">See Also</span></span>  
 <span data-ttu-id="c5da0-121">[Belgische elektronische betalingen](belgian-electronic-payments.md) </span><span class="sxs-lookup"><span data-stu-id="c5da0-121">[Belgian Electronic Payments](belgian-electronic-payments.md) </span></span>  
 <span data-ttu-id="c5da0-122">[Leveranciers voor automatische betalingsvoorstellen instellen](how-to-set-up-vendors-for-automatic-payment-suggestions.md) </span><span class="sxs-lookup"><span data-stu-id="c5da0-122">[Set Up Vendors for Automatic Payment Suggestions](how-to-set-up-vendors-for-automatic-payment-suggestions.md) </span></span>  
 <span data-ttu-id="c5da0-123">[Betalingsvoorstellen genereren](how-to-generate-payment-suggestions.md) </span><span class="sxs-lookup"><span data-stu-id="c5da0-123">[Generate Payment Suggestions](how-to-generate-payment-suggestions.md) </span></span>  
 [<span data-ttu-id="c5da0-124">Betalingsbestanden afdrukken</span><span class="sxs-lookup"><span data-stu-id="c5da0-124">Print Payment Files</span></span>](how-to-print-payment-files.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]