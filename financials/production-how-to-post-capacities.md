---
title: Capaciteit boeken | Microsoft Docs
description: In het capaciteitsdagboek boekt u de verbruikte capaciteit die niet is toegewezen aan de productieorder. Onderhoudswerk moet bijvoorbeeld worden toegewezen aan capaciteit, maar niet aan een productieorder.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 4b0bb12f86a8984ca4a87d679bc22a0e34e51c88
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-post-capacities"></a><span data-ttu-id="72d5d-104">Procedure: capaciteit boeken</span><span class="sxs-lookup"><span data-stu-id="72d5d-104">How to: Post Capacities</span></span>
<span data-ttu-id="72d5d-105">In het capaciteitsdagboek boekt u de verbruikte capaciteit die niet is toegewezen aan de productieorder.</span><span class="sxs-lookup"><span data-stu-id="72d5d-105">In the capacity journal, you post consumed capacities that are not assigned to the production order.</span></span> <span data-ttu-id="72d5d-106">Onderhoudswerk moet bijvoorbeeld worden toegewezen aan capaciteit, maar niet aan een productieorder.</span><span class="sxs-lookup"><span data-stu-id="72d5d-106">For example, maintenance work must be assigned to capacity, but not to a production order.</span></span>  

## <a name="to-post-capacities"></a><span data-ttu-id="72d5d-107">Capaciteit boeken</span><span class="sxs-lookup"><span data-stu-id="72d5d-107">To post capacities</span></span>  
1.  <span data-ttu-id="72d5d-108">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png ""pictogram Zoeken naar pagina of rapport"), voer **Capaciteitsdagboeken** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="72d5d-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Capacity Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="72d5d-109">Vul de velden **Boekingsdatum** en **Documentnr.** in.</span><span class="sxs-lookup"><span data-stu-id="72d5d-109">Fill in the **Posting Date** and **Document No.** fields.</span></span>  
3.  <span data-ttu-id="72d5d-110">Voer in het veld **Soort** het soort capaciteit in dat u wilt boeken, dat kan **Bewerkingsplaats** of **Afdeling** zijn.</span><span class="sxs-lookup"><span data-stu-id="72d5d-110">In the **Type** field, enter the type of the capacity, either **Machine Center** or **Work Center**, that you are posting.</span></span>  
4.  <span data-ttu-id="72d5d-111">Selecteer in het veld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="72d5d-111">In the **No.**</span></span> <span data-ttu-id="72d5d-112">het nummer in van de bewerkingsplaats of afdeling.</span><span class="sxs-lookup"><span data-stu-id="72d5d-112">field, enter the number of the machine center or work center.</span></span>  
5.  <span data-ttu-id="72d5d-113">Voer in de andere velden de relevante gegevens in, bijvoorbeeld **Begintijd**, **Eindtijd**, **Aantal** en **Uitval**.</span><span class="sxs-lookup"><span data-stu-id="72d5d-113">Enter the relevant data in the other fields, such as **Starting Time**, **Ending Time**, **Quantity**, and **Scrap**.</span></span>  
6.  <span data-ttu-id="72d5d-114">Kies de actie **Boeken** om de capaciteit te boeken.</span><span class="sxs-lookup"><span data-stu-id="72d5d-114">Choose the **Post** action to post the capacities.</span></span>  

## <a name="to-view-work-center-ledger-entries"></a><span data-ttu-id="72d5d-115">Afdelingsposten weergeven</span><span class="sxs-lookup"><span data-stu-id="72d5d-115">To view work center ledger entries</span></span>  
<span data-ttu-id="72d5d-116">In de vensters **Afdeling** en **Bewerkingsplaats** kunt u de geboekte capaciteit als gevolg van gereedgemelde productieorders bekijken.</span><span class="sxs-lookup"><span data-stu-id="72d5d-116">In the **Work Center Card** and **Machine Center Card** windows, you can view the posted capacities as a result of finished production orders.</span></span>    
1.  <span data-ttu-id="72d5d-117">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Afdelingen** in en klik op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="72d5d-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Work Centers**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="72d5d-118">Open de betreffende kaart **Afdeling** in de lijst en kies de actie **Capaciteitsposten**.</span><span class="sxs-lookup"><span data-stu-id="72d5d-118">Open the relevant **Work Center** card from the list, and then choose the **Capacity Ledger Entries** action.</span></span>  

<span data-ttu-id="72d5d-119">Het venster **Capaciteitsposten** bevat de geboekte posten van de afdeling, in de volgorde waarin deze zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="72d5d-119">The **Capacity Ledger Entries** window displays the posted entries from the work center in the order they were posted.</span></span>   

## <a name="see-also"></a><span data-ttu-id="72d5d-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="72d5d-120">See Also</span></span>  
<span data-ttu-id="72d5d-121">[Productie](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="72d5d-121">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="72d5d-122">Productie instellen</span><span class="sxs-lookup"><span data-stu-id="72d5d-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="72d5d-123">[Gepland](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="72d5d-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="72d5d-124">Voorraad</span><span class="sxs-lookup"><span data-stu-id="72d5d-124">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="72d5d-125">Inkoop</span><span class="sxs-lookup"><span data-stu-id="72d5d-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="72d5d-126">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="72d5d-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

