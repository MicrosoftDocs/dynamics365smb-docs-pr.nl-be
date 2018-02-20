---
title: Automatische overdracht en gecombineerde posten | Microsoft Docs
description: In kostprijsboekhouding kunt u grootboekposten overbrengen naar een kostensoort door middel van een gecombineerde boeking. U kunt opgeven of een kostensoort gecombineerde posten ontvangt in het veld **Posten combineren** in de definitie van het kostensoort. De volgende tabel beschrijft de verschillende opties.
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: f4796d9796788d2fbbf5706688aec75a4ed9a6d8
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="ceed7-105">Automatische overdracht en gecombineerde posten</span><span class="sxs-lookup"><span data-stu-id="ceed7-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="ceed7-106">In kostprijsboekhouding kunt u grootboekposten overbrengen naar een kostensoort door middel van een gecombineerde boeking.</span><span class="sxs-lookup"><span data-stu-id="ceed7-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="ceed7-107">U kunt opgeven of een kostensoort gecombineerde posten ontvangt in het veld **Posten combineren** in de definitie van het kostensoort.</span><span class="sxs-lookup"><span data-stu-id="ceed7-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="ceed7-108">De volgende tabel beschrijft de verschillende opties.</span><span class="sxs-lookup"><span data-stu-id="ceed7-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="ceed7-109">Posten combineren</span><span class="sxs-lookup"><span data-stu-id="ceed7-109">Combine entries</span></span>|<span data-ttu-id="ceed7-110">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="ceed7-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="ceed7-111">Geen</span><span class="sxs-lookup"><span data-stu-id="ceed7-111">None</span></span>|<span data-ttu-id="ceed7-112">Elke grootboekpost wordt afzonderlijk overgebracht naar het bijbehorende kostensoort.</span><span class="sxs-lookup"><span data-stu-id="ceed7-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="ceed7-113">Dag</span><span class="sxs-lookup"><span data-stu-id="ceed7-113">Day</span></span>|<span data-ttu-id="ceed7-114">Grootboekposten met dezelfde boekingsdatum worden als één post overgeboekt naar de bijbehorende kostensoort.</span><span class="sxs-lookup"><span data-stu-id="ceed7-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="ceed7-115">Maand</span><span class="sxs-lookup"><span data-stu-id="ceed7-115">Month</span></span>|<span data-ttu-id="ceed7-116">Alle grootboekposten in dezelfde kalendermaand worden als één post overgeboekt naar de bijbehorende kostensoort.</span><span class="sxs-lookup"><span data-stu-id="ceed7-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="ceed7-117">Als u het selectievakje **Automatisch overdragen van GB** in het venster **Instelling kostprijsboekhouding** hebt ingeschakeld, wordt de kostprijsboekhouding automatisch bijgewerkt in [!INCLUDE[d365fin](includes/d365fin_md.md)] na elke boeking in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="ceed7-117">If you have selected the **Auto Transfer from G/L** check box in the **Cost Accounting Setup** window, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="ceed7-118">Gecombineerde posten zijn niet mogelijk.</span><span class="sxs-lookup"><span data-stu-id="ceed7-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ceed7-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ceed7-119">See Also</span></span>  
 <span data-ttu-id="ceed7-120">[Grootboekposten overbrengen naar kostenposten](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="ceed7-120">[Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="ceed7-121">[Criteria voor het overbrengen van grootboekposten naar kostenposten.](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="ceed7-121">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="ceed7-122">[Resultaten van de overboeking](finance-results-of-the-transfer.md) </span><span class="sxs-lookup"><span data-stu-id="ceed7-122">[Results of the Transfer](finance-results-of-the-transfer.md) </span></span>  
 [<span data-ttu-id="ceed7-123">Kostenposten overbrengen en boeken</span><span class="sxs-lookup"><span data-stu-id="ceed7-123">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)  
 <span data-ttu-id="ceed7-124">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ceed7-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

