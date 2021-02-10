---
title: Boekingsperioden afsluiten voor een boekjaar | Microsoft Docs
description: Beschrijft hoe u de boekhoudperioden afsluit die een boekjaar vormen.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6acdc86afc195185f66836bf723c83d4a1647927
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755679"
---
# <a name="close-accounting-periods"></a><span data-ttu-id="487de-103">Boekhoudperioden afsluiten</span><span class="sxs-lookup"><span data-stu-id="487de-103">Close Accounting Periods</span></span>
<span data-ttu-id="487de-104">Wanneer een boekjaar is afgelopen, moet u de hierin opgenomen perioden afsluiten.</span><span class="sxs-lookup"><span data-stu-id="487de-104">When a fiscal year is over, you must close the periods that comprise it.</span></span>

## <a name="to-close-accounting-periods"></a><span data-ttu-id="487de-105">Boekhoudperioden afsluiten</span><span class="sxs-lookup"><span data-stu-id="487de-105">To close accounting periods</span></span>
1. <span data-ttu-id="487de-106">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Boekhoudperioden** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="487de-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Accounting Periods**, and then choose the related link.</span></span>
2. <span data-ttu-id="487de-107">Kies op de pagina **Boekingsperioden** de actie **Jaar afsluiten**.</span><span class="sxs-lookup"><span data-stu-id="487de-107">On the **Accounting Periods** page, choose the **Close Year** action.</span></span>

    <span data-ttu-id="487de-108">Als er meerdere boekjaren zijn geopend, wordt het vroegste boekjaar automatisch geselecteerd om te worden afgesloten.</span><span class="sxs-lookup"><span data-stu-id="487de-108">If more than one fiscal year is open, the earliest one is automatically selected to be closed.</span></span> <span data-ttu-id="487de-109">Er verschijnt een bericht waarin wordt aangegeven welk jaar wordt afgesloten en welke gevolgen dit heeft.</span><span class="sxs-lookup"><span data-stu-id="487de-109">A message displays identifying the year that will close and the consequences of closing the year.</span></span>
3. <span data-ttu-id="487de-110">Kies de knop **Ja** om het jaar af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="487de-110">To close the year, choose the **Yes** button.</span></span>

<span data-ttu-id="487de-111">Het boekjaar is nu afgesloten en de selectievakjes **Afgesloten** en **Geblokkeerd** zijn ingeschakeld voor alle perioden van het jaar.</span><span class="sxs-lookup"><span data-stu-id="487de-111">The fiscal year is closed, and the **Closed** and **Date Locked** fields for all the periods in the year are selected.</span></span> <span data-ttu-id="487de-112">U kunt het boekjaar niet meer openen en de selectievakjes **Afgesloten** en **Geblokkeerd** niet uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="487de-112">The fiscal year cannot be opened again and you cannot remove the check mark from the **Closed** or **Date Locked** fields.</span></span>

> [!NOTE]  
>   <span data-ttu-id="487de-113">U kunt een boekjaar niet afsluiten voordat u een nieuw boekjaar hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="487de-113">You cannot close a fiscal year before you create a new one.</span></span> <span data-ttu-id="487de-114">Wanneer een boekjaar is afgesloten, kunt u de begindatum van het volgende boekjaar niet meer wijzigen.</span><span class="sxs-lookup"><span data-stu-id="487de-114">Notice that when a fiscal year has been closed, you cannot change the starting date of the following fiscal year.</span></span>

<span data-ttu-id="487de-115">Zelfs als een boekjaar is afgesloten, kunt u er nog steeds grootboekposten voor boeken.</span><span class="sxs-lookup"><span data-stu-id="487de-115">Even though a fiscal year has been closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="487de-116">Als u dit doet, worden de posten gemarkeerd als zijnde geboekt naar een afgesloten boekjaar en wordt het veld **Naboeking** geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="487de-116">When you do this, the entries will be marked as posted to a closed fiscal year and the **Prior-Year Entry** field will be selected.</span></span>

<span data-ttu-id="487de-117">Nadat een boekjaar is afgesloten, moet u de resultaten- of winst- en verliesrekeningen afsluiten en de jaarresultaten naar een balansrekening overbrengen.</span><span class="sxs-lookup"><span data-stu-id="487de-117">After a fiscal year is closed, you must close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="487de-118">U kunt deze procedure herhalen telkens wanneer u boekt naar een afgesloten boekjaar.</span><span class="sxs-lookup"><span data-stu-id="487de-118">You can repeat this every time that you post to the closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="487de-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="487de-119">See Also</span></span>

[<span data-ttu-id="487de-120">Boeken afsluiten</span><span class="sxs-lookup"><span data-stu-id="487de-120">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="487de-121">De jaareinde-ultimopost boeken</span><span class="sxs-lookup"><span data-stu-id="487de-121">Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="487de-122">Werken met boekingsperioden en boekjaren</span><span class="sxs-lookup"><span data-stu-id="487de-122">Work with Accounting Periods and Fiscal Years</span></span>](finance-accounting-periods-and-fiscal-years.md)  
<span data-ttu-id="487de-123">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="487de-123">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
