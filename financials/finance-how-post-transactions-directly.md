---
title: Kosten of inkomsten rechtstreeks in grootboek registreren| Microsoft Docs
description: Voor zakelijke activiteiten die niet door een document worden vertegenwoordigd, zoals kleinere ontvangsten of kasontvangsten, kunt u de gerelateerde transacties maken door dagboekregels te boeken in het venster Diversendagboek.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 06/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7fa0d6b604a60e000208287546d831690a914931
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-post-transactions-directly-to-the-general-ledger"></a><span data-ttu-id="4e08d-103">Procedure: Transacties direct naar het grootboek boeken</span><span class="sxs-lookup"><span data-stu-id="4e08d-103">How to: Post Transactions Directly to the General Ledger</span></span>
<span data-ttu-id="4e08d-104">De meeste financiële transacties worden geboekt naar het grootboek door bepaalde bedrijfsdocumenten, zoals inkoopfacturen en verkooporders.</span><span class="sxs-lookup"><span data-stu-id="4e08d-104">Most financial transactions are posted to the general ledger through dedicated business documents, such as purchase invoices and sales orders.</span></span> <span data-ttu-id="4e08d-105">Voor zakelijke activiteiten die niet door een document worden vertegenwoordigd in [!INCLUDE[d365fin](includes/d365fin_md.md)], zoals kleinere ontvangsten of kasontvangsten, kunt u de gerelateerde transacties maken door dagboekregels te boeken in het venster **Diversendagboek**.</span><span class="sxs-lookup"><span data-stu-id="4e08d-105">For business activities that are not represented by a document in [!INCLUDE[d365fin](includes/d365fin_md.md)], such as smaller expenses or cash receipts, you can create the related transactions by posting journal lines in the **General Journal** window.</span></span>

<span data-ttu-id="4e08d-106">Dagboeken boeken financiële transacties direct naar grootboekrekeningen en andere rekeningen zoals bank-, klant- en leveranciersrekeningen.</span><span class="sxs-lookup"><span data-stu-id="4e08d-106">General journals post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, and vendor accounts.</span></span> <span data-ttu-id="4e08d-107">Door te boeken met een dagboek worden er altijd posten gemaakt in grootboekrekeningen.</span><span class="sxs-lookup"><span data-stu-id="4e08d-107">Posting with a general journal always creates entries on general ledger accounts.</span></span> <span data-ttu-id="4e08d-108">Dit geldt zelfs ook als u bijvoorbeeld een dagboekregel naar een klantrekening boekt, omdat een post via een boekingsgroep is geboekt naar een rekening met vorderingen in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="4e08d-108">This is true even when, for example, you post a journal line to a customer account, because an entry is posted to a general ledger receivables account through a posting group.</span></span> <span data-ttu-id="4e08d-109">U kunt uw versie van een dagboek aanpassen door een dagboekbatch of -sjabloon in te stellen.</span><span class="sxs-lookup"><span data-stu-id="4e08d-109">You can personalize your version of a general journal by setting up a journal batch or template.</span></span> <span data-ttu-id="4e08d-110">Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="4e08d-110">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

<span data-ttu-id="4e08d-111">In tegenstelling tot posten die zijn geboekt met documenten, die een creditnotaproces vereisen, kunt posten correct tegenboeken die met het diversendagboek zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="4e08d-111">Unlike for entries that are posted with documents, which require a credit memo process, you can correctly reverse entries that are posted with the general journal.</span></span> <span data-ttu-id="4e08d-112">Zie [Dagboekboeking tegenboeken](finance-how-reverse-journal-posting.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="4e08d-112">For more information, see [How to: Reverse Journal Posting](finance-how-reverse-journal-posting.md).</span></span>

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a><span data-ttu-id="4e08d-113">Een transactie direct naar het grootboek boeken</span><span class="sxs-lookup"><span data-stu-id="4e08d-113">To post a transaction directly to a general ledger account</span></span>
1. <span data-ttu-id="4e08d-114">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Dagboeken** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="4e08d-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="4e08d-115">Open de relevante dagboekbatch.</span><span class="sxs-lookup"><span data-stu-id="4e08d-115">Open the relevant general journal batch.</span></span> <span data-ttu-id="4e08d-116">Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="4e08d-116">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="4e08d-117">Vul op een nieuwe dagboekregel de velden indien nodig in.</span><span class="sxs-lookup"><span data-stu-id="4e08d-117">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    
4. <span data-ttu-id="4e08d-118">Herhaal stap 3 voor alle afzonderlijke transacties die u wilt boeken.</span><span class="sxs-lookup"><span data-stu-id="4e08d-118">Repeat step 3 for all the separate transactions that you want to post.</span></span>

    > [!TIP]  
    > <span data-ttu-id="4e08d-119">Als u meerdere transactieregels boven één tegenrekeningsregel wilt invoeren, bijvoorbeeld, voor één bankrekening, selecteert u het selectievakje **Salderingsbedrag voorstellen** op de regel voor uw batch in het venster **Fin. dagboekbatches**.</span><span class="sxs-lookup"><span data-stu-id="4e08d-119">If you want to enter multiple transaction lines above one balance-account line, for example, for one bank account, then select the **Suggest Balancing Amount** check box on the line for your batch in the **General Journal Batches** window.</span></span> <span data-ttu-id="4e08d-120">Vervolgens wordt het veld **Bedrag** op de tegenrekeningsregel automatisch ingevuld met de waarde die nodig is om de transacties in balans te brengen.</span><span class="sxs-lookup"><span data-stu-id="4e08d-120">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the transactions.</span></span>
5. <span data-ttu-id="4e08d-121">Kies de actie **Boeken** om de transacties op de betreffende grootboekrekeningen te registreren.</span><span class="sxs-lookup"><span data-stu-id="4e08d-121">Choose the **Post** action to record the transactions on the specified G/L accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e08d-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="4e08d-122">See Also</span></span>
[<span data-ttu-id="4e08d-123">Werken met diversendagboeken</span><span class="sxs-lookup"><span data-stu-id="4e08d-123">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="4e08d-124">Procedure: dagboekboeking tegenboeken</span><span class="sxs-lookup"><span data-stu-id="4e08d-124">How to: Reverse Journal Posting</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="4e08d-125">Financiën</span><span class="sxs-lookup"><span data-stu-id="4e08d-125">Finance</span></span>](finance.md)  
<span data-ttu-id="4e08d-126">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4e08d-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

