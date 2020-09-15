---
title: CODA-afschriften automatisch overbrengen en boeken
description: Nadat u alle CODA-afschriftregels hebt vereffend en verwerkt, kunt u de CODA-afschriftregels overbrengen naar een financieel dagboek.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 66255add1efcf68f4b73dc95f2f531e3abf98732
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778978"
---
# <a name="automatically-transfer-and-post-coda-statements"></a><span data-ttu-id="c9810-103">CODA-afschriften automatisch overbrengen en boeken</span><span class="sxs-lookup"><span data-stu-id="c9810-103">Automatically Transfer and Post CODA Statements</span></span>
<span data-ttu-id="c9810-104">Nadat u alle CODA-afschriftregels hebt vereffend en verwerkt, kunt u de CODA-afschriftregels overbrengen naar een financieel dagboek.</span><span class="sxs-lookup"><span data-stu-id="c9810-104">After you have applied and processed all CODA statement lines, you can transfer the CODA statement lines to a financial journal.</span></span>  

<span data-ttu-id="c9810-105">Na het overbrengen van de afschriftregels kunt u de regels boeken in een corresponderend dagboek.</span><span class="sxs-lookup"><span data-stu-id="c9810-105">After transferring the statement lines, you can post the lines in a corresponding general journal.</span></span> <span data-ttu-id="c9810-106">Als een dergelijk dagboek niet bestaat, kunt u de regels niet overbrengen.</span><span class="sxs-lookup"><span data-stu-id="c9810-106">If no such general journal exists, you cannot transfer the lines.</span></span> <span data-ttu-id="c9810-107">U kunt een dagboek maken om CODA-afschriften te verwerken.</span><span class="sxs-lookup"><span data-stu-id="c9810-107">You can create a journal to handle CODA statements.</span></span> <span data-ttu-id="c9810-108">Zie voor meer informatie [Financiële dagboeken maken](how-to-create-financial-journals.md).</span><span class="sxs-lookup"><span data-stu-id="c9810-108">For more information, see [Create Financial Journals](how-to-create-financial-journals.md).</span></span>  

<span data-ttu-id="c9810-109">U kunt CODA-afschriften ook handmatig overbrengen en boeken.</span><span class="sxs-lookup"><span data-stu-id="c9810-109">Alternatively, you can manually transfer and post CODA statements.</span></span> <span data-ttu-id="c9810-110">Zie voor meer informatie [CODA-afschriften handmatig overbrengen en boeken](how-to-manually-transfer-and-post-coda-statements.md).</span><span class="sxs-lookup"><span data-stu-id="c9810-110">For information, see [Manually Transfer and Post CODA Statements](how-to-manually-transfer-and-post-coda-statements.md).</span></span>  

## <a name="to-automatically-transfer-statement-lines"></a><span data-ttu-id="c9810-111">Afschriftregels automatisch overbrengen</span><span class="sxs-lookup"><span data-stu-id="c9810-111">To automatically transfer statement lines</span></span>  

1.  <span data-ttu-id="c9810-112">Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="c9810-112">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c9810-113">Selecteer de bankrekening en kies de actie **CODA-afschriften**.</span><span class="sxs-lookup"><span data-stu-id="c9810-113">Select the bank account, and then choose the **CODA Statements** action.</span></span>  
3.  <span data-ttu-id="c9810-114">Selecteer het CODA-afschrift en kies vervolgens de actie **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="c9810-114">Select the CODA statement, and then choose the **Edit** action.</span></span>  
4.  <span data-ttu-id="c9810-115">Kies de actie **Naar dagboek overbrengen**.</span><span class="sxs-lookup"><span data-stu-id="c9810-115">Choose the **Transfer to General Ledger** action.</span></span>  
5.  <span data-ttu-id="c9810-116">Kies de knop **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c9810-116">Choose the **Yes** button.</span></span>  

<span data-ttu-id="c9810-117">De CODA-afschriftregels worden nu overgebracht naar het financiële dagboek.</span><span class="sxs-lookup"><span data-stu-id="c9810-117">The batch job will now transfer the CODA statement lines to the financial journal.</span></span>  

<span data-ttu-id="c9810-118">Als de afschriftregels naar het dagboek zijn overgebracht, kunt u de afschriftregels in het bijbehorende financiële dagboek boeken.</span><span class="sxs-lookup"><span data-stu-id="c9810-118">After transferring the statement lines to the journal, you can post the statement lines in the corresponding financial journal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c9810-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c9810-119">See Also</span></span>  
 <span data-ttu-id="c9810-120">[CODA-bankafschriften](coda-bank-statements.md) </span><span class="sxs-lookup"><span data-stu-id="c9810-120">[CODA Bank Statements](coda-bank-statements.md) </span></span>  
 <span data-ttu-id="c9810-121">[CODA-afschriften importeren](how-to-import-coda-statements.md) </span><span class="sxs-lookup"><span data-stu-id="c9810-121">[Import CODA Statements](how-to-import-coda-statements.md) </span></span>  
 <span data-ttu-id="c9810-122">[CODA-afschriften vereffenen](how-to-apply-coda-statements.md) </span><span class="sxs-lookup"><span data-stu-id="c9810-122">[Apply CODA Statements](how-to-apply-coda-statements.md) </span></span>  
 <span data-ttu-id="c9810-123">[Financiële dagboeken maken](how-to-create-financial-journals.md) </span><span class="sxs-lookup"><span data-stu-id="c9810-123">[Create Financial Journals](how-to-create-financial-journals.md) </span></span>  
 [<span data-ttu-id="c9810-124">CODA-afschriften handmatig overbrengen en boeken</span><span class="sxs-lookup"><span data-stu-id="c9810-124">Manually Transfer and Post CODA Statements</span></span>](how-to-manually-transfer-and-post-coda-statements.md)
