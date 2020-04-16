---
title: Niet-aftrekbare btw instellen
description: U kunt btw-bedragen voor bepaalde soorten onkosten berekenen die gedeeltelijk als btw kunnen worden aangegeven.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 6c55566a1d048461d5a02a6f124e1f81d00e70c8
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3180850"
---
# <a name="set-up-non-deductible-vat"></a><span data-ttu-id="8a0a9-103">Niet-aftrekbare btw instellen</span><span class="sxs-lookup"><span data-stu-id="8a0a9-103">Set Up Non-Deductible VAT</span></span>
<span data-ttu-id="8a0a9-104">U kunt btw-bedragen voor bepaalde soorten onkosten berekenen die gedeeltelijk als btw kunnen worden aangegeven.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-104">You can calculate VAT amounts for specific types of expenses that can be partially declared as VAT.</span></span> <span data-ttu-id="8a0a9-105">Wanneer u op de pagina **Grootboekrekening** 75 opgeeft in het veld **% niet-aftrekbare btw**, wordt 75 procent van het normale btw-bedrag beschouwd als bijkomende kosten en tijdens het boeken toegevoegd aan het nettobedrag.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-105">For example, on the **G/L Account Card** page, if you enter 75 in the **% Non-Deductible VAT** field, then 75 percent of the regular VAT amount is considered an additional cost and will be added to the net amount during posting.</span></span> <span data-ttu-id="8a0a9-106">De resterende 25 procent wordt als normale btw geboekt.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-106">The remaining 25 percent will be posted as regular VAT.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="8a0a9-107">Als geen waarde wordt opgegeven in het veld **% niet-aftrekbare btw**, is het btw-bedrag 100 procent aftrekbaar.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-107">If no value is entered in the **% Non-Deductible VAT** field, the VAT amount is 100 percent deductible.</span></span>  

## <a name="to-set-up-the-non-deductible-vat-percentage"></a><span data-ttu-id="8a0a9-108">Het niet-aftrekbare btw-percentage instellen</span><span class="sxs-lookup"><span data-stu-id="8a0a9-108">To set up the non-deductible VAT percentage</span></span>  

1.  <span data-ttu-id="8a0a9-109">Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "Het pictogram Zoeken naar pagina of rapport"), voer **Rekeningschema** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-109">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="8a0a9-110">Selecteer een onkostengrootboekrekening waarvoor de gedeeltelijke aftrek nodig is en kies vervolgens de actie **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-110">Select a general ledger expense account that requires the partial deduction, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="8a0a9-111">Voer het bedrag in het veld **Niet-aftrekbare btw** in.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-111">Enter the amount in **% Non deductible VAT** field.</span></span>  
4.  <span data-ttu-id="8a0a9-112">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="8a0a9-112">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8a0a9-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8a0a9-113">See Also</span></span>  
 <span data-ttu-id="8a0a9-114">[Belgische btw](belgian-vat.md) </span><span class="sxs-lookup"><span data-stu-id="8a0a9-114">[Belgian VAT](belgian-vat.md) </span></span>  
 [<span data-ttu-id="8a0a9-115">Periodieke btw-rapporten afdrukken</span><span class="sxs-lookup"><span data-stu-id="8a0a9-115">Print Periodic VAT Reports</span></span>](how-to-print-periodic-vat-reports.md)
