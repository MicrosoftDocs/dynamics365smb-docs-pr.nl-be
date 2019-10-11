---
title: Niet-aftrekbare btw instellen
description: U kunt btw-bedragen voor bepaalde soorten onkosten berekenen die gedeeltelijk als btw kunnen worden aangegeven.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: b7e950288be5c5bd9a31d286280392c5fda7d628
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2301374"
---
# <a name="set-up-non-deductible-vat"></a><span data-ttu-id="c823f-103">Niet-aftrekbare btw instellen</span><span class="sxs-lookup"><span data-stu-id="c823f-103">Set Up Non-Deductible VAT</span></span>
<span data-ttu-id="c823f-104">U kunt btw-bedragen voor bepaalde soorten onkosten berekenen die gedeeltelijk als btw kunnen worden aangegeven.</span><span class="sxs-lookup"><span data-stu-id="c823f-104">You can calculate VAT amounts for specific types of expenses that can be partially declared as VAT.</span></span> <span data-ttu-id="c823f-105">Wanneer u op de pagina **Grootboekrekening** 75 opgeeft in het veld **% niet-aftrekbare btw**, wordt 75 procent van het normale btw-bedrag beschouwd als bijkomende kosten en tijdens het boeken toegevoegd aan het nettobedrag.</span><span class="sxs-lookup"><span data-stu-id="c823f-105">For example, on the **G/L Account Card** page, if you enter 75 in the **% Non-Deductible VAT** field, then 75 percent of the regular VAT amount is considered an additional cost and will be added to the net amount during posting.</span></span> <span data-ttu-id="c823f-106">De resterende 25 procent wordt als normale btw geboekt.</span><span class="sxs-lookup"><span data-stu-id="c823f-106">The remaining 25 percent will be posted as regular VAT.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="c823f-107">Als geen waarde wordt opgegeven in het veld **% niet-aftrekbare btw**, is het btw-bedrag 100 procent aftrekbaar.</span><span class="sxs-lookup"><span data-stu-id="c823f-107">If no value is entered in the **% Non-Deductible VAT** field, the VAT amount is 100 percent deductible.</span></span>  

## <a name="to-set-up-the-non-deductible-vat-percentage"></a><span data-ttu-id="c823f-108">Het niet-aftrekbare btw-percentage instellen</span><span class="sxs-lookup"><span data-stu-id="c823f-108">To set up the non-deductible VAT percentage</span></span>  

1.  <span data-ttu-id="c823f-109">Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rekeningschema** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="c823f-109">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c823f-110">Selecteer een onkostengrootboekrekening waarvoor de gedeeltelijke aftrek nodig is en kies vervolgens de actie **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="c823f-110">Select a general ledger expense account that requires the partial deduction, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="c823f-111">Voer het bedrag in het veld **Niet-aftrekbare btw** in.</span><span class="sxs-lookup"><span data-stu-id="c823f-111">Enter the amount in **% Non deductible VAT** field.</span></span>  
4.  <span data-ttu-id="c823f-112">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="c823f-112">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c823f-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c823f-113">See Also</span></span>  
 <span data-ttu-id="c823f-114">[Belgische btw](belgian-vat.md) </span><span class="sxs-lookup"><span data-stu-id="c823f-114">[Belgian VAT](belgian-vat.md) </span></span>  
 [<span data-ttu-id="c823f-115">Periodieke btw-rapporten afdrukken</span><span class="sxs-lookup"><span data-stu-id="c823f-115">Print Periodic VAT Reports</span></span>](how-to-print-periodic-vat-reports.md)
