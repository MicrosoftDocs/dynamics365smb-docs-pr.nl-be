---
title: Een dagboekboeking ongedaan maken door een tegenboeking te boeken| Microsoft Docs
description: Als u een foutieve boeking in het dagboek hebt gemaakt, kunt u vervolgens de functie Transactie tegenboeken gebruiken om de boeking ongedaan te maken met de juiste audittrail.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 8126a53d59e72276eb1558fd65fe3c0cd53600cc
ms.contentlocale: nl-be
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-reverse-journal-posting"></a><span data-ttu-id="90fdf-103">Procedure: Dagboekboeking tegenboeken</span><span class="sxs-lookup"><span data-stu-id="90fdf-103">How to: Reverse Journal Posting</span></span>
<span data-ttu-id="90fdf-104">Om een foutieve dagboekpost ongedaan te maken, selecteert en maakt u een tegenboeking (posten die identiek zijn aan de oorspronkelijke post, maar met een tegenovergesteld teken in het bedragveld) met hetzelfde documentnummer en dezelfde boekingsdatum als de originele post.</span><span class="sxs-lookup"><span data-stu-id="90fdf-104">To undo an erroneous journal posting, you select the entry and create a reverse entry (entries identical to the original entry but with opposite sign in the amount field) with the same document number and posting date as the original entry.</span></span> <span data-ttu-id="90fdf-105">Nadat een post is tegengeboekt, moet u de juiste post maken.</span><span class="sxs-lookup"><span data-stu-id="90fdf-105">After reversing an entry, you must make the correct entry.</span></span>

<span data-ttu-id="90fdf-106">U kunt alleen posten tegenboeken die zijn geboekt vanaf een algemene dagboekregel.</span><span class="sxs-lookup"><span data-stu-id="90fdf-106">You can only reverse entries that are posted from a general journal line.</span></span> <span data-ttu-id="90fdf-107">Een post kan slechts één keer worden tegengeboekt.</span><span class="sxs-lookup"><span data-stu-id="90fdf-107">An entry can only be reversed once.</span></span>

<span data-ttu-id="90fdf-108">Voor meer informatie over het boeken vanuit een dagboek zie [Procedure: Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md)</span><span class="sxs-lookup"><span data-stu-id="90fdf-108">For more information about posting from a general journal, see [How to: Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>

<span data-ttu-id="90fdf-109">U kunt posten vanuit alle **Posten**-vensters tegenboeken.</span><span class="sxs-lookup"><span data-stu-id="90fdf-109">You can reverse entries from all **Ledger Entries** windows.</span></span> <span data-ttu-id="90fdf-110">De volgende procedure is gebaseerd op het venster **Grootboekposten**.</span><span class="sxs-lookup"><span data-stu-id="90fdf-110">The following procedure is based on the **General Ledger Entries** window.</span></span>

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a><span data-ttu-id="90fdf-111">De dagboekboeking van een grootboekpost tegenboeken</span><span class="sxs-lookup"><span data-stu-id="90fdf-111">To reverse the journal posting of a general ledger entry</span></span>
1. <span data-ttu-id="90fdf-112">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Grootboekposten** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="90fdf-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="90fdf-113">Selecteer de post die u wilt tegenboeken en kies vervolgens de actie **Transactie tegenboeken**.</span><span class="sxs-lookup"><span data-stu-id="90fdf-113">Select the entry that you want to reverse, and then choose the **Reverse Transaction** action.</span></span> <span data-ttu-id="90fdf-114">Het moet afkomstig zijn uit een dagboekboeking.</span><span class="sxs-lookup"><span data-stu-id="90fdf-114">Note that is must originate from a journal posting.</span></span>
3. <span data-ttu-id="90fdf-115">Selecteer in het venster **Transactieposten tegenboeken** de relevante post en kies de actie **Tegenboeken**.</span><span class="sxs-lookup"><span data-stu-id="90fdf-115">In the **Reverse Transaction Entries** window, select the relevant entry, and then choose the **Reverse** action.</span></span>
4. <span data-ttu-id="90fdf-116">Kies de knop **Ja** in het bevestigingsbericht.</span><span class="sxs-lookup"><span data-stu-id="90fdf-116">Choose the **Yes** button on the confirmation message.</span></span>

## <a name="see-also"></a><span data-ttu-id="90fdf-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="90fdf-117">See Also</span></span>
[<span data-ttu-id="90fdf-118">Procedure: Transacties direct naar het grootboek boeken</span><span class="sxs-lookup"><span data-stu-id="90fdf-118">How to: Post Transactions Directly to the General Ledger</span></span>](finance-how-post-transactions-directly.md)  
[<span data-ttu-id="90fdf-119">Werken met diversendagboeken</span><span class="sxs-lookup"><span data-stu-id="90fdf-119">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="90fdf-120">Financiën</span><span class="sxs-lookup"><span data-stu-id="90fdf-120">Finance</span></span>](finance.md)  
<span data-ttu-id="90fdf-121">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="90fdf-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

