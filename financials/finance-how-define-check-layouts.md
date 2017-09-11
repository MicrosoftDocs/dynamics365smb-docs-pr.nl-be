---
title: De lay-out opgeven van een cheque| Microsoft Docs
description: U kunt uw cheques ontwerpen en afdrukken in verschillende indelingen, om te voldoen aan standaards.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 06/15/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a2db2860846cd9b8010222faf580f0c9889e39a4
ms.contentlocale: nl-be
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-define-check-layouts"></a><span data-ttu-id="0c684-103">Procedure: Cheque-indelingen definiëren</span><span class="sxs-lookup"><span data-stu-id="0c684-103">How to: Define Check Layouts</span></span>
<span data-ttu-id="0c684-104">U kunt uw eigen cheques ontwerpen in overeenstemming met de standaards die zijn ingesteld door de plaatselijke autoriteiten.</span><span class="sxs-lookup"><span data-stu-id="0c684-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="0c684-105">Chequeafbeeldingen kunnen worden afgedrukt in het Engels, Frans of Spaans.</span><span class="sxs-lookup"><span data-stu-id="0c684-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="0c684-106">Cheques worden ontworpen om te worden afgedrukt in zowel Amerikaanse als Canadese chequeafbeeldingsindelingen, in een cheque-strook-cheque indeling of een strook-strook-cheque indeling.</span><span class="sxs-lookup"><span data-stu-id="0c684-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="0c684-107">Cheque-indelingen definiëren</span><span class="sxs-lookup"><span data-stu-id="0c684-107">To define check layouts</span></span>
1. <span data-ttu-id="0c684-108">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Zoeken naar pagina of rapport"), voer **Rapportselecties bankrekening** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="0c684-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="0c684-109">Selecteer in het venster **Rapportselectie - Bankrekening**</span><span class="sxs-lookup"><span data-stu-id="0c684-109">In the **Report Selection - Bank Acc.**</span></span> <span data-ttu-id="0c684-110">in het veld **Gebruik** **Cheque**.</span><span class="sxs-lookup"><span data-stu-id="0c684-110">window, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="0c684-111">Selecteer een van de volgende rapport-id's.</span><span class="sxs-lookup"><span data-stu-id="0c684-111">Select one of the following report IDs.</span></span>

| <span data-ttu-id="0c684-112">Rapport-id</span><span class="sxs-lookup"><span data-stu-id="0c684-112">Report ID</span></span> | <span data-ttu-id="0c684-113">Rapportnaam</span><span class="sxs-lookup"><span data-stu-id="0c684-113">Report Name</span></span> | <span data-ttu-id="0c684-114">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="0c684-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0c684-115">1401</span><span class="sxs-lookup"><span data-stu-id="0c684-115">1401</span></span> |<span data-ttu-id="0c684-116">Cheque</span><span class="sxs-lookup"><span data-stu-id="0c684-116">Check</span></span> |<span data-ttu-id="0c684-117">Dit is het standaardrapport.</span><span class="sxs-lookup"><span data-stu-id="0c684-117">This is the default report.</span></span> |
| <span data-ttu-id="0c684-118">10401</span><span class="sxs-lookup"><span data-stu-id="0c684-118">10401</span></span> |<span data-ttu-id="0c684-119">Cheque (strook/strook/cheque)</span><span class="sxs-lookup"><span data-stu-id="0c684-119">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="0c684-120">Dit rapport is ontworpen om cheques af te drukken in de indeling strook/strook/cheque.</span><span class="sxs-lookup"><span data-stu-id="0c684-120">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="0c684-121">10411</span><span class="sxs-lookup"><span data-stu-id="0c684-121">10411</span></span> |<span data-ttu-id="0c684-122">Cheque (strook/cheque/strook)</span><span class="sxs-lookup"><span data-stu-id="0c684-122">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="0c684-123">Dit rapport is ontworpen om cheques af te drukken in de indeling cheque/strook/cheque.</span><span class="sxs-lookup"><span data-stu-id="0c684-123">This report is designed to print checks in a check/stub/check format.</span></span> |

<span data-ttu-id="0c684-124">Wanneer u de cheque-indelingen hebt ingesteld, kunt u cheques afdrukken vanuit het venster **Betalingsdagboek**.</span><span class="sxs-lookup"><span data-stu-id="0c684-124">When you have set up check layouts, you can print checks from the **Payment Journal** window.</span></span> <span data-ttu-id="0c684-125">Zie voor meer informatie [Procedure: Werken met cheques](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="0c684-125">For more information, see [How to: Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0c684-126">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0c684-126">See Also</span></span>
[<span data-ttu-id="0c684-127">Betalingsverplichtingen beheren</span><span class="sxs-lookup"><span data-stu-id="0c684-127">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="0c684-128">[Bankrekeningen beheren](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="0c684-128">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="0c684-129">Periodeafsluitingsprocessen voltooien</span><span class="sxs-lookup"><span data-stu-id="0c684-129">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="0c684-130">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0c684-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="0c684-131">Algemene bedrijfsfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="0c684-131">General Business Functionality</span></span>](ui-across-business-areas.md)

