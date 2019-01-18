---
title: Automatische overdracht en gecombineerde posten | Microsoft Docs
description: In kostprijsboekhouding kunt u grootboekposten overbrengen naar een kostensoort door middel van een gecombineerde boeking. U kunt opgeven of een kostensoort gecombineerde posten ontvangt in het veld **Posten combineren** in de definitie van het kostensoort. De volgende tabel beschrijft de verschillende opties.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 6f58e569bea6a42a9ee695095ce308e7a69e2a8d
ms.contentlocale: nl-be
ms.lasthandoff: 11/26/2018

---
# <a name="automatic-transfer-and-combined-entries"></a><span data-ttu-id="a3797-105">Automatische overdracht en gecombineerde posten</span><span class="sxs-lookup"><span data-stu-id="a3797-105">Automatic Transfer and Combined Entries</span></span>
<span data-ttu-id="a3797-106">In kostprijsboekhouding kunt u grootboekposten overbrengen naar een kostensoort door middel van een gecombineerde boeking.</span><span class="sxs-lookup"><span data-stu-id="a3797-106">In cost accounting, you can transfer general ledger entries to a cost type by using a combined posting.</span></span> <span data-ttu-id="a3797-107">U kunt opgeven of een kostensoort gecombineerde posten ontvangt in het veld **Posten combineren** in de definitie van het kostensoort.</span><span class="sxs-lookup"><span data-stu-id="a3797-107">You can specify if a cost type receives combined entries in the **Combine Entries** field in the cost type definition.</span></span> <span data-ttu-id="a3797-108">De volgende tabel beschrijft de verschillende opties.</span><span class="sxs-lookup"><span data-stu-id="a3797-108">The following table describes the different options.</span></span>  

|<span data-ttu-id="a3797-109">Posten combineren</span><span class="sxs-lookup"><span data-stu-id="a3797-109">Combine entries</span></span>|<span data-ttu-id="a3797-110">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="a3797-110">Description</span></span>|  
|---------------------|-----------------|  
|<span data-ttu-id="a3797-111">Geen</span><span class="sxs-lookup"><span data-stu-id="a3797-111">None</span></span>|<span data-ttu-id="a3797-112">Elke grootboekpost wordt afzonderlijk overgebracht naar het bijbehorende kostensoort.</span><span class="sxs-lookup"><span data-stu-id="a3797-112">Each general ledger entry is transferred individually to the corresponding cost type.</span></span>|  
|<span data-ttu-id="a3797-113">Dag</span><span class="sxs-lookup"><span data-stu-id="a3797-113">Day</span></span>|<span data-ttu-id="a3797-114">Grootboekposten met dezelfde boekingsdatum worden als één post overgeboekt naar de bijbehorende kostensoort.</span><span class="sxs-lookup"><span data-stu-id="a3797-114">General ledger entries with the same posting date are transferred as one entry to the corresponding cost type.</span></span>|  
|<span data-ttu-id="a3797-115">Maand</span><span class="sxs-lookup"><span data-stu-id="a3797-115">Month</span></span>|<span data-ttu-id="a3797-116">Alle grootboekposten in dezelfde kalendermaand worden als één post overgeboekt naar de bijbehorende kostensoort.</span><span class="sxs-lookup"><span data-stu-id="a3797-116">All general ledger entries in the same calendar month are transferred as one entry to the corresponding cost type.</span></span>|  

> [!IMPORTANT]  
>  <span data-ttu-id="a3797-117">Als u het selectievakje **Automatisch overdragen van GB** op de pagina **Instelling kostprijsboekhouding** hebt ingeschakeld, wordt de kostprijsboekhouding automatisch bijgewerkt in [!INCLUDE[d365fin](includes/d365fin_md.md)] na elke boeking in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="a3797-117">If you have selected the **Auto Transfer from G/L** check box on the **Cost Accounting Setup** page, [!INCLUDE[d365fin](includes/d365fin_md.md)] updates the cost accounting after every posting in the general ledger.</span></span> <span data-ttu-id="a3797-118">Gecombineerde posten zijn niet mogelijk.</span><span class="sxs-lookup"><span data-stu-id="a3797-118">Combined entries are not possible.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a3797-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a3797-119">See Also</span></span>  
 <span data-ttu-id="a3797-120">[Kostenposten overbrengen en boeken](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="a3797-120">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 <span data-ttu-id="a3797-121">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a3797-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

