---
title: Criteria voor het overbrengen van grootboekposten naar kostenposten | Microsoft Docs
description: Het is belangrijk dat u een goed begrip heeft van de criteria voor het overbrengen van grootboekposten naar kostenposten. Tijdens de overdracht maakt de batchverwerking **Grootboekposten overbrengen naar kostprijsboekhouding** gebruik van de volgende criteria om te bepalen of en hoe de grootboekposten worden overgebracht.
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
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 62d19b5ff112871f7f44f0945bdcfd38306ed8b3
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "931663"
---
# <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="4925c-104">Criteria voor het overbrengen van grootboekposten naar kostenposten.</span><span class="sxs-lookup"><span data-stu-id="4925c-104">Criteria for Transferring General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="4925c-105">Het is belangrijk dat u een goed begrip heeft van de criteria voor het overbrengen van grootboekposten naar kostenposten.</span><span class="sxs-lookup"><span data-stu-id="4925c-105">It is important to understand the criteria for transferring general ledger entries to cost entries.</span></span> <span data-ttu-id="4925c-106">Tijdens de overdracht maakt de batchverwerking **Grootboekposten overbrengen naar kostprijsboekhouding** gebruik van de volgende criteria om te bepalen of en hoe de grootboekposten worden overgebracht.</span><span class="sxs-lookup"><span data-stu-id="4925c-106">During the transfer, the **Transfer GL Entries to CA** batch job uses the following criteria to determine if and how the general ledger entries are transferred.</span></span>  

<span data-ttu-id="4925c-107">Grootboekposten worden overgebracht in de volgende gevallen:</span><span class="sxs-lookup"><span data-stu-id="4925c-107">General ledger entries are transferred if:</span></span>  

-   <span data-ttu-id="4925c-108">De posten hebben dimensiewaarden die een bijbehorende kostenplaats of kostenobject hebben.</span><span class="sxs-lookup"><span data-stu-id="4925c-108">The entries have dimension values corresponding to either a cost center or a cost object.</span></span>  
-   <span data-ttu-id="4925c-109">De posten hebben dimensiewaarden die een bijbehorende kostenplaats en kostenobject hebben.</span><span class="sxs-lookup"><span data-stu-id="4925c-109">The entries have dimension values that correspond to a cost center and a cost object.</span></span> <span data-ttu-id="4925c-110">Voor deze posten heeft de kostenplaats voorrang.</span><span class="sxs-lookup"><span data-stu-id="4925c-110">For these entries, the cost center takes precedence.</span></span> <span data-ttu-id="4925c-111">Dit voorkomt de situatie waarin een kostensoort zowel in een kostenobject als kostenplaats wordt weergegeven, en daarom twee keer in de statistieken wordt meegeteld.</span><span class="sxs-lookup"><span data-stu-id="4925c-111">This helps avoid a situation where a cost type appears in both a cost object and a cost center and is therefore counted twice in the statistics.</span></span>  
-   <span data-ttu-id="4925c-112">Het documentnummer in de posten is leeg, en wordt daarom weergegeven met documentnummer 0000 in de kostenposten.</span><span class="sxs-lookup"><span data-stu-id="4925c-112">The document number in the entries is empty, so it will appear with a document number of 0000 in the cost entries.</span></span>  
-   <span data-ttu-id="4925c-113">De posten worden overgebracht naar een kostensoort dat gecombineerde posten toestaat, en deze posten worden maandelijks of dagelijks overgebracht als een gecombineerde post.</span><span class="sxs-lookup"><span data-stu-id="4925c-113">The entries are transferred to a cost type that allows for combined entries and these entries are transferred as a combined entry either monthly or daily.</span></span>  

<span data-ttu-id="4925c-114">Grootboekposten worden niet overgebracht in de volgende gevallen:</span><span class="sxs-lookup"><span data-stu-id="4925c-114">General ledger entries are not transferred if:</span></span>  

-   <span data-ttu-id="4925c-115">De posten hebben dimensiewaarden die geen bijbehorende kostenplaats of kostenobject hebben.</span><span class="sxs-lookup"><span data-stu-id="4925c-115">The entries have dimension values that do not correspond to a cost center or a cost object.</span></span>  
-   <span data-ttu-id="4925c-116">De posten bevatten een bedrag met waarde nul.</span><span class="sxs-lookup"><span data-stu-id="4925c-116">The entries have an amount of zero.</span></span>  
-   <span data-ttu-id="4925c-117">De posten zijn van een grootboekrekening die is verwijderd.</span><span class="sxs-lookup"><span data-stu-id="4925c-117">The entries have a general ledger account that has been deleted.</span></span>  
-   <span data-ttu-id="4925c-118">De posten hebben een grootboekrekening die niet van het soort **Resultatenrekening** is.</span><span class="sxs-lookup"><span data-stu-id="4925c-118">The entries have a general ledger account that is not of the type **Income Statement**.</span></span>  
-   <span data-ttu-id="4925c-119">De posten hebben een grootboekrekening waaraan geen kostensoort is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="4925c-119">The entries have a general ledger account that is not assigned a cost type.</span></span>  
-   <span data-ttu-id="4925c-120">De posten hebben een boekingsdatum vóór de **Begindatum voor GB-overdracht**.</span><span class="sxs-lookup"><span data-stu-id="4925c-120">The entries have a posting date before the **Starting Date for G/L Transfer**.</span></span>  
-   <span data-ttu-id="4925c-121">De posten zijn geboekt met een ultimodatum.</span><span class="sxs-lookup"><span data-stu-id="4925c-121">The entries have been posted with a closing date.</span></span> <span data-ttu-id="4925c-122">Dit zijn meestal de posten die een negatief effect hebben op het saldo van de resultatenrekening aan het einde van het jaar.</span><span class="sxs-lookup"><span data-stu-id="4925c-122">These are typically entries that set back the balance of the income statement at the end of the year.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4925c-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="4925c-123">See Also</span></span>  
[<span data-ttu-id="4925c-124">Kosten verantwoorden</span><span class="sxs-lookup"><span data-stu-id="4925c-124">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
 <span data-ttu-id="4925c-125">[Grootboekposten overbrengen naar kostenposten](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="4925c-125">[Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="4925c-126">[Kostenposten overbrengen en boeken](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="4925c-126">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 [<span data-ttu-id="4925c-127">Kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="4925c-127">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
 <span data-ttu-id="4925c-128">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4925c-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
