---
title: Niet-aftrekbare btw instellen
description: U kunt btw-bedragen voor bepaalde soorten onkosten berekenen die gedeeltelijk als btw kunnen worden aangegeven.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 00fe4c0fc0450585cd3e7a6cbb14b9b4b6d57f54
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-non-deductible-vat"></a><span data-ttu-id="b0342-103">Niet-aftrekbare btw instellen</span><span class="sxs-lookup"><span data-stu-id="b0342-103">Set Up Non-Deductible VAT</span></span>
<span data-ttu-id="b0342-104">U kunt btw-bedragen voor bepaalde soorten onkosten berekenen die gedeeltelijk als btw kunnen worden aangegeven.</span><span class="sxs-lookup"><span data-stu-id="b0342-104">You can calculate VAT amounts for specific types of expenses which can be partially declared as VAT.</span></span> <span data-ttu-id="b0342-105">Wanneer u in het venster **Grootboekrekening** 75 procent opgeeft in het veld **% niet-aftrekbare btw**, wordt 75 procent van het normale btw-bedrag beschouwd als bijkomende kosten en tijdens het boeken toegevoegd aan het nettobedrag.</span><span class="sxs-lookup"><span data-stu-id="b0342-105">For example, in the **G/L Account Card** window, if you enter 75 percent in the **% Non-Deductible VAT** field, then 75 percent of the regular VAT amount is considered an additional cost and will be added to the net amount during posting.</span></span> <span data-ttu-id="b0342-106">De resterende 25 procent wordt als normale btw geboekt.</span><span class="sxs-lookup"><span data-stu-id="b0342-106">The remaining 25 percent will be posted as regular VAT.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b0342-107">Als geen waarde wordt opgegeven in het veld **% niet-aftrekbare btw**, is het btw-bedrag 100 procent aftrekbaar.</span><span class="sxs-lookup"><span data-stu-id="b0342-107">If no value is entered in the **% Non-Deductible VAT** field, the VAT amount is 100 percent deductible.</span></span>  

## <a name="to-set-up-the-non-deductible-vat-percentage"></a><span data-ttu-id="b0342-108">Het niet-aftrekbare btw-percentage instellen</span><span class="sxs-lookup"><span data-stu-id="b0342-108">To set up the non-deductible VAT percentage</span></span>  

1.  <span data-ttu-id="b0342-109">Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rekeningschema** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="b0342-109">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b0342-110">Selecteer een onkostengrootboekrekening waarvoor de gedeeltelijke aftrek nodig is en kies vervolgens de actie **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="b0342-110">Select a general ledger expense account that requires the partial deduction, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="b0342-111">Voer op het sneltabblad **Boeken** het bedrag in het veld **% niet-aftrekbare btw** in.</span><span class="sxs-lookup"><span data-stu-id="b0342-111">On the **Posting** FastTab, enter the amount in **% Non deductible VAT** field.</span></span>  
4.  <span data-ttu-id="b0342-112">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="b0342-112">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b0342-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b0342-113">See Also</span></span>  
 <span data-ttu-id="b0342-114">[Belgische btw](belgian-vat.md) </span><span class="sxs-lookup"><span data-stu-id="b0342-114">[Belgian VAT](belgian-vat.md) </span></span>  
 [<span data-ttu-id="b0342-115">Periodieke btw-rapporten afdrukken</span><span class="sxs-lookup"><span data-stu-id="b0342-115">Print Periodic VAT Reports</span></span>](how-to-print-periodic-vat-reports.md)

