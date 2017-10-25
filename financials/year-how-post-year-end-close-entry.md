---
title: Jaareinde-ultimopost controleren en boeken | Microsoft Docs
description: Beschrijft hoe u het dagboek opent dat u hebt opgegeven in de batchverwerking Afsluiten WenV-rekening en vervolgens de jaareinde-ultimopost controleert en boekt.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 68017b8b031ee4bd368936b6fb4de157328d7030
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-post-the-year-end-closing-entry"></a><span data-ttu-id="aa466-103">Procedure: de jaareinde-ultimopost boeken</span><span class="sxs-lookup"><span data-stu-id="aa466-103">How to: Post the Year-End Closing Entry</span></span>
<span data-ttu-id="aa466-104">Nadat u de batchverwerking **Afsluiten WenV-rekening** hebt gebruikt om de jaareinde-ultimopost of -posten te boeken, moet u het dagboek openen dat u in de batchverwerking hebt opgegeven en vervolgens de posten herzien en boeken.</span><span class="sxs-lookup"><span data-stu-id="aa466-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="aa466-105">De jaareinde-ultimopost boeken</span><span class="sxs-lookup"><span data-stu-id="aa466-105">To post the year end closing entry</span></span>
1. <span data-ttu-id="aa466-106">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Diversendagboek** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="aa466-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="aa466-107">Selecteer in het venster **Diversendagboek** in het veld **Batchnaam** de batch die de ultimoposten bevat.</span><span class="sxs-lookup"><span data-stu-id="aa466-107">In the **General Journal** window, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="aa466-108">Controleer de posten.</span><span class="sxs-lookup"><span data-stu-id="aa466-108">Review the entries.</span></span>
4. <span data-ttu-id="aa466-109">Kies de actie **Boeken** om het dagboek te boeken.</span><span class="sxs-lookup"><span data-stu-id="aa466-109">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="aa466-110">Als een fout wordt gedetecteerd, wordt een foutbericht weergegeven.</span><span class="sxs-lookup"><span data-stu-id="aa466-110">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="aa466-111">Als de boeking is geslaagd, worden de geboekte posten uit het dagboek gehaald.</span><span class="sxs-lookup"><span data-stu-id="aa466-111">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="aa466-112">Nadat de boeking is voltooid, wordt een post geboekt in elke resultatenrekening zodat het saldo nul wordt en het jaarresultaat wordt overgebracht naar de balans.</span><span class="sxs-lookup"><span data-stu-id="aa466-112">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa466-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="aa466-113">See Also</span></span>
[<span data-ttu-id="aa466-114">Procedure: Boekhoudperioden afsluiten</span><span class="sxs-lookup"><span data-stu-id="aa466-114">How to: Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="aa466-115">Boeken afsluiten</span><span class="sxs-lookup"><span data-stu-id="aa466-115">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="aa466-116">Afsluiten WenV-rekening</span><span class="sxs-lookup"><span data-stu-id="aa466-116">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="aa466-117">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="aa466-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

