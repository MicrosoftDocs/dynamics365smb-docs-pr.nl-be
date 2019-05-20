---
title: De lay-out opgeven van een cheque| Microsoft Docs
description: U kunt uw cheques ontwerpen en afdrukken in verschillende indelingen, om te voldoen aan standaards.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/24/2019
ms.author: edupont
ms.openlocfilehash: f2b7fa01cff36e3aab335f7d5921954343c69b74
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243607"
---
# <a name="define-check-layouts"></a><span data-ttu-id="37866-103">Cheque-indelingen definiëren</span><span class="sxs-lookup"><span data-stu-id="37866-103">Define Check Layouts</span></span>
<span data-ttu-id="37866-104">U kunt uw eigen cheques ontwerpen in overeenstemming met de standaards die zijn ingesteld door de plaatselijke autoriteiten.</span><span class="sxs-lookup"><span data-stu-id="37866-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="37866-105">Chequeafbeeldingen kunnen worden afgedrukt in het Engels, Frans of Spaans.</span><span class="sxs-lookup"><span data-stu-id="37866-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="37866-106">Cheques worden ontworpen om te worden afgedrukt in zowel Amerikaanse als Canadese chequeafbeeldingsindelingen, in een cheque-strook-cheque indeling of een strook-strook-cheque indeling.</span><span class="sxs-lookup"><span data-stu-id="37866-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="37866-107">Cheque-indelingen definiëren</span><span class="sxs-lookup"><span data-stu-id="37866-107">To define check layouts</span></span>
1. <span data-ttu-id="37866-108">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bankrekening van rapportselecties** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="37866-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="37866-109">Selecteer op de pagina **Rapportselectie - Bank** in het veld **Gebruik** de optie **Cheque**.</span><span class="sxs-lookup"><span data-stu-id="37866-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="37866-110">Selecteer een van de volgende rapport-id's.</span><span class="sxs-lookup"><span data-stu-id="37866-110">Select one of the following report IDs.</span></span>

  | <span data-ttu-id="37866-111">Rapport-id</span><span class="sxs-lookup"><span data-stu-id="37866-111">Report ID</span></span> | <span data-ttu-id="37866-112">Rapportnaam</span><span class="sxs-lookup"><span data-stu-id="37866-112">Report Name</span></span> | <span data-ttu-id="37866-113">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="37866-113">Description</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="37866-114">1401</span><span class="sxs-lookup"><span data-stu-id="37866-114">1401</span></span> |<span data-ttu-id="37866-115">Cheque</span><span class="sxs-lookup"><span data-stu-id="37866-115">Check</span></span> |<span data-ttu-id="37866-116">Dit is het standaardrapport.</span><span class="sxs-lookup"><span data-stu-id="37866-116">This is the default report.</span></span> |
  | <span data-ttu-id="37866-117">10411</span><span class="sxs-lookup"><span data-stu-id="37866-117">10411</span></span> |<span data-ttu-id="37866-118">Cheque (strook/strook/cheque)</span><span class="sxs-lookup"><span data-stu-id="37866-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="37866-119">Dit rapport is ontworpen om cheques af te drukken in de indeling strook/strook/cheque.</span><span class="sxs-lookup"><span data-stu-id="37866-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
  | <span data-ttu-id="37866-120">10412</span><span class="sxs-lookup"><span data-stu-id="37866-120">10412</span></span> |<span data-ttu-id="37866-121">Cheque (strook/cheque/strook)</span><span class="sxs-lookup"><span data-stu-id="37866-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="37866-122">Dit rapport is ontworpen om cheques af te drukken in de indeling strook/cheque/strook.</span><span class="sxs-lookup"><span data-stu-id="37866-122">This report is designed to print checks in a stub/check/stub format.</span></span> |
  | <span data-ttu-id="37866-123">10413</span><span class="sxs-lookup"><span data-stu-id="37866-123">10413</span></span> |<span data-ttu-id="37866-124">Drie cheques per pagina</span><span class="sxs-lookup"><span data-stu-id="37866-124">Three Checks per Page</span></span> |<span data-ttu-id="37866-125">Dit rapport is ontworpen voor het afdrukken van drie cheques op elke pagina.</span><span class="sxs-lookup"><span data-stu-id="37866-125">This report is designed to print three checks on each page.</span></span> |

<span data-ttu-id="37866-126">Wanneer u de cheque-indelingen hebt ingesteld, kunt u cheques afdrukken vanuit de pagina **Betalingsdagboek**.</span><span class="sxs-lookup"><span data-stu-id="37866-126">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="37866-127">Zie voor meer informatie [Werken met cheques](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="37866-127">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="37866-128">Zie ook</span><span class="sxs-lookup"><span data-stu-id="37866-128">See Also</span></span>
[<span data-ttu-id="37866-129">Betalingsverplichtingen beheren</span><span class="sxs-lookup"><span data-stu-id="37866-129">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="37866-130">[Bankrekeningen beheren](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="37866-130">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="37866-131">Periodeafsluitingsprocessen voltooien</span><span class="sxs-lookup"><span data-stu-id="37866-131">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="37866-132">[Werken met [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="37866-132">[Working with [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="37866-133">Algemene bedrijfsfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="37866-133">General Business Functionality</span></span>](ui-across-business-areas.md)
