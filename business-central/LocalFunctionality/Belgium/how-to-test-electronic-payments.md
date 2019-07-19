---
title: Elektronische betalingen testen
description: Nadat u elektronisch bankieren hebt ingesteld en betalingsvoorstellen hebt gegenereerd, kunt u de betalingsdagboekregels op fouten testen voordat u ze boekt.
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
ms.openlocfilehash: 0e0df0dc2ed18ad9df732389e88aa8a98eda2f30
ms.sourcegitcommit: 5b6dd8d881c0eb65ece6936a94dfda3185574335
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/28/2019
ms.locfileid: "1710997"
---
# <a name="test-electronic-payments"></a><span data-ttu-id="4c164-103">Elektronische betalingen testen</span><span class="sxs-lookup"><span data-stu-id="4c164-103">Test Electronic Payments</span></span>
> [!Note]
> [!INCLUDE[onprem_only](../../includes/onprem_only_md.md)]

<span data-ttu-id="4c164-104">Nadat u elektronisch bankieren hebt ingesteld en betalingsvoorstellen hebt gegenereerd, kunt u de betalingsdagboekregels op fouten testen voordat u ze boekt.</span><span class="sxs-lookup"><span data-stu-id="4c164-104">After you have set up electronic banking and generated payment suggestions, you can test the payment journal lines for errors before posting them.</span></span>  

<span data-ttu-id="4c164-105">Hierbij wordt onder andere het volgende gevalideerd:</span><span class="sxs-lookup"><span data-stu-id="4c164-105">Some of the information that is validated includes:</span></span>  

- <span data-ttu-id="4c164-106">Of bankrekeningnummers geldig zijn.</span><span class="sxs-lookup"><span data-stu-id="4c164-106">Whether bank account numbers are valid.</span></span>  
- <span data-ttu-id="4c164-107">Of positieve betalingsregels aanwezig zijn.</span><span class="sxs-lookup"><span data-stu-id="4c164-107">Whether positive payment lines are present.</span></span>  
- <span data-ttu-id="4c164-108">Of binnenlandse en internationale betalingen via slechts één rekening worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="4c164-108">Whether domestic and international payments are made from only one bank account.</span></span>  
- <span data-ttu-id="4c164-109">Of er slechts één bankrekening kan worden gebruikt voor Isabel (Interbanks Standards Association Belgium).</span><span class="sxs-lookup"><span data-stu-id="4c164-109">Whether only one bank account can be used for Interbanks Standards Association Belgium (Isabel).</span></span>  
- <span data-ttu-id="4c164-110">Of betalingsregels in euro zijn voor SEPA (Single Euro Payments Area).</span><span class="sxs-lookup"><span data-stu-id="4c164-110">Whether payment lines are in euro for Single Euro Payments Area (SEPA).</span></span>  
- <span data-ttu-id="4c164-111">Of er een nummerreeks voor SEPA is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="4c164-111">Whether a number series has been defined for SEPA.</span></span>  

<span data-ttu-id="4c164-112">U kunt de fouten bekijken op de pagina **Logboeken voor controlefouten exporteren**.</span><span class="sxs-lookup"><span data-stu-id="4c164-112">You can view any errors on the **Export Check Error Logs** page.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="4c164-113">U moet alle fouten corrigeren voordat u de regels kunt boeken.</span><span class="sxs-lookup"><span data-stu-id="4c164-113">You have to correct all errors before you can post the lines.</span></span>  

## <a name="to-test-payment-journal-lines"></a><span data-ttu-id="4c164-114">Betalingsdagboekregels testen</span><span class="sxs-lookup"><span data-stu-id="4c164-114">To test payment journal lines</span></span>  

1.  <span data-ttu-id="4c164-115">Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsdagboeken** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="4c164-115">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="4c164-116">Selecteer in het veld **Batchnaam** de vereiste dagboekbatch.</span><span class="sxs-lookup"><span data-stu-id="4c164-116">In the **Batch Name** field, select the required journal batch.</span></span>  
3.  <span data-ttu-id="4c164-117">Selecteer in het veld **Exportprotocol** het exportprotocol.</span><span class="sxs-lookup"><span data-stu-id="4c164-117">In the **Export Protocol** field, select the export protocol.</span></span>  
4.  <span data-ttu-id="4c164-118">Voer de betalingsdagboekregelinformatie in en kies vervolgens de actie **Betalingsregels controleren** om de betalingsdagboekregels te valideren.</span><span class="sxs-lookup"><span data-stu-id="4c164-118">Enter the payment journal line information, and then choose the **Check Payment Lines** action to validate the payment journal lines.</span></span> <span data-ttu-id="4c164-119">Welke validatie op de dagboekregels wordt uitgevoerd, is afhankelijk van de soort controle die op de pagina **Exportprotocollen** is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="4c164-119">The validation that is performed on the journal lines depends on the type of check that is specified on the **Export Protocols** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4c164-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="4c164-120">See Also</span></span>  
 <span data-ttu-id="4c164-121">[Belgische elektronische betalingen](belgian-electronic-payments.md) </span><span class="sxs-lookup"><span data-stu-id="4c164-121">[Belgian Electronic Payments](belgian-electronic-payments.md) </span></span>  
 <span data-ttu-id="4c164-122">[Leveranciers voor automatische betalingsvoorstellen instellen](how-to-set-up-vendors-for-automatic-payment-suggestions.md) </span><span class="sxs-lookup"><span data-stu-id="4c164-122">[Set Up Vendors for Automatic Payment Suggestions](how-to-set-up-vendors-for-automatic-payment-suggestions.md) </span></span>  
 <span data-ttu-id="4c164-123">[Betalingsvoorstellen genereren](how-to-generate-payment-suggestions.md) </span><span class="sxs-lookup"><span data-stu-id="4c164-123">[Generate Payment Suggestions](how-to-generate-payment-suggestions.md) </span></span>  
 [<span data-ttu-id="4c164-124">Betalingsbestanden afdrukken</span><span class="sxs-lookup"><span data-stu-id="4c164-124">Print Payment Files</span></span>](how-to-print-payment-files.md)
