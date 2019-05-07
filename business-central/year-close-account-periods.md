---
title: Boekingsperioden afsluiten voor een boekjaar | Microsoft Docs
description: Beschrijft hoe u de boekhoudperioden afsluit die een boekjaar vormen.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: e51d25b90a3f51953479906a35380541e02d7380
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "922923"
---
# <a name="close-accounting-periods"></a><span data-ttu-id="6383d-103">Boekhoudperioden afsluiten</span><span class="sxs-lookup"><span data-stu-id="6383d-103">Close Accounting Periods</span></span>
<span data-ttu-id="6383d-104">Wanneer een boekjaar is afgelopen, moet u de hierin opgenomen perioden afsluiten.</span><span class="sxs-lookup"><span data-stu-id="6383d-104">When a fiscal year is over, you must close the periods that comprise it.</span></span>

## <a name="to-close-accounting-periods"></a><span data-ttu-id="6383d-105">Boekhoudperioden afsluiten</span><span class="sxs-lookup"><span data-stu-id="6383d-105">To close accounting periods</span></span>
1. <span data-ttu-id="6383d-106">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Boekingsperioden** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="6383d-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Accounting Periods**, and then choose the related link.</span></span>
2. <span data-ttu-id="6383d-107">Kies op de pagina **Boekingsperioden** de actie **Jaar afsluiten**.</span><span class="sxs-lookup"><span data-stu-id="6383d-107">On the **Accounting Periods** page, choose the **Close Year** action.</span></span>

    <span data-ttu-id="6383d-108">Als er meerdere boekjaren zijn geopend, wordt het vroegste boekjaar automatisch geselecteerd om te worden afgesloten.</span><span class="sxs-lookup"><span data-stu-id="6383d-108">If more than one fiscal year is open, the earliest one is automatically selected to be closed.</span></span> <span data-ttu-id="6383d-109">Er verschijnt een bericht waarin wordt aangegeven welk jaar wordt afgesloten en welke gevolgen dit heeft.</span><span class="sxs-lookup"><span data-stu-id="6383d-109">A message displays identifying the year that will close and the consequences of closing the year.</span></span>
3. <span data-ttu-id="6383d-110">Kies de knop **Ja** om het jaar af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="6383d-110">To close the year, choose the **Yes** button.</span></span>

<span data-ttu-id="6383d-111">Het boekjaar is nu afgesloten en de selectievakjes **Afgesloten** en **Geblokkeerd** zijn ingeschakeld voor alle perioden van het jaar.</span><span class="sxs-lookup"><span data-stu-id="6383d-111">The fiscal year is closed, and the **Closed** and **Date Locked** fields for all the periods in the year are selected.</span></span> <span data-ttu-id="6383d-112">U kunt het boekjaar niet meer openen en de selectievakjes **Afgesloten** en **Geblokkeerd** niet uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="6383d-112">The fiscal year cannot be opened again and you cannot remove the check mark from the **Closed** or **Date Locked** fields.</span></span>

> [!NOTE]  
>   <span data-ttu-id="6383d-113">U kunt een boekjaar niet afsluiten voordat u een nieuw boekjaar hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="6383d-113">You cannot close a fiscal year before you create a new one.</span></span> <span data-ttu-id="6383d-114">Wanneer een boekjaar is afgesloten, kunt u de begindatum van het volgende boekjaar niet meer wijzigen.</span><span class="sxs-lookup"><span data-stu-id="6383d-114">Notice that when a fiscal year has been closed, you cannot change the starting date of the following fiscal year.</span></span>

<span data-ttu-id="6383d-115">Zelfs als een boekjaar is afgesloten, kunt u er nog steeds grootboekposten voor boeken.</span><span class="sxs-lookup"><span data-stu-id="6383d-115">Even though a fiscal year has been closed, you can still post general ledger entries to it.</span></span> <span data-ttu-id="6383d-116">Als u dit doet, worden de posten gemarkeerd als zijnde geboekt naar een afgesloten boekjaar en wordt het veld **Naboeking** geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="6383d-116">When you do this, the entries will be marked as posted to a closed fiscal year and the **Prior-Year Entry** field will be selected.</span></span>

<span data-ttu-id="6383d-117">Nadat een boekjaar is afgesloten, moet u de resultaten- of winst- en verliesrekeningen afsluiten en de jaarresultaten naar een balansrekening overbrengen.</span><span class="sxs-lookup"><span data-stu-id="6383d-117">After a fiscal year is closed, you must close the income statement accounts and transfer the year's results to an account in the balance sheet.</span></span> <span data-ttu-id="6383d-118">U kunt deze procedure herhalen telkens wanneer u boekt naar een afgesloten boekjaar.</span><span class="sxs-lookup"><span data-stu-id="6383d-118">You can repeat this every time that you post to the closed fiscal year.</span></span>

## <a name="see-also"></a><span data-ttu-id="6383d-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6383d-119">See Also</span></span>
[<span data-ttu-id="6383d-120">Boeken afsluiten</span><span class="sxs-lookup"><span data-stu-id="6383d-120">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="6383d-121">De jaareinde-ultimopost boeken</span><span class="sxs-lookup"><span data-stu-id="6383d-121">Post the Year-End Closing Entry</span></span>](year-how-post-year-end-close-entry.md)  
[<span data-ttu-id="6383d-122">Een nieuw boekjaar openen</span><span class="sxs-lookup"><span data-stu-id="6383d-122">Open a New Fiscal Year</span></span>](finance-how-open-new-fiscal-year.md)  
<span data-ttu-id="6383d-123">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6383d-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
