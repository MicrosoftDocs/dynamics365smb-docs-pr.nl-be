---
title: Kosten of inkomsten rechtstreeks in grootboek registreren| Microsoft Docs
description: Voor zakelijke activiteiten die niet door een document worden vertegenwoordigd, zoals kleinere ontvangsten of kasontvangsten, kunt u de gerelateerde transacties maken door dagboekregels te boeken op de pagina Diversendagboek.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct posting, general ledger
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: f0c1efcee7db0239efa739dd0ea8d8ce45e2dbd7
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183968"
---
# <a name="post-transactions-directly-to-the-general-ledger"></a><span data-ttu-id="20b8d-103">Transacties direct naar het grootboek boeken</span><span class="sxs-lookup"><span data-stu-id="20b8d-103">Post Transactions Directly to the General Ledger</span></span>

<span data-ttu-id="20b8d-104">Met diversendagboeken kunt u financiële transacties direct naar grootboekrekeningen en andere rekeningen boeken, zoals bank-, klant-, leveranciers- en werknemersrekeningen.</span><span class="sxs-lookup"><span data-stu-id="20b8d-104">You use general journals to post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span>  

<span data-ttu-id="20b8d-105">Een veelvoorkomend gebruik van het dagboek is uitgaven van werknemers van eigen geld tijdens zakelijke activiteiten te boeken, voor latere terugbetaling.</span><span class="sxs-lookup"><span data-stu-id="20b8d-105">A typical use of the general journal is to post employees' expenditure of own money during business activities, for later reimbursement.</span></span> <span data-ttu-id="20b8d-106">Zie voor meer informatie [Uitgaven van werknemers vastleggen en terugbetalen](finance-how-record-reimburse-employee-expenses.md).</span><span class="sxs-lookup"><span data-stu-id="20b8d-106">For more information, see [Record and Reimburse Employees' Expenses](finance-how-record-reimburse-employee-expenses.md).</span></span>

<span data-ttu-id="20b8d-107">Dagboeken boeken financiële transacties direct naar grootboekrekeningen en andere rekeningen zoals bank-, klant-, leveranciers- en werknemersrekeningen.</span><span class="sxs-lookup"><span data-stu-id="20b8d-107">General journals post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts.</span></span> <span data-ttu-id="20b8d-108">Door te boeken met een dagboek worden er altijd posten gemaakt in grootboekrekeningen.</span><span class="sxs-lookup"><span data-stu-id="20b8d-108">Posting with a general journal always creates entries on general ledger accounts.</span></span> <span data-ttu-id="20b8d-109">Dit geldt zelfs ook als u bijvoorbeeld een dagboekregel naar een klantrekening boekt, omdat een post via een boekingsgroep is geboekt naar een rekening met vorderingen in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="20b8d-109">This is true even when, for example, you post a journal line to a customer account, because an entry is posted to a general ledger receivables account through a posting group.</span></span> <span data-ttu-id="20b8d-110">U kunt uw versie van een dagboek aanpassen door een dagboekbatch of -sjabloon in te stellen.</span><span class="sxs-lookup"><span data-stu-id="20b8d-110">You can personalize your version of a general journal by setting up a journal batch or template.</span></span> <span data-ttu-id="20b8d-111">Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="20b8d-111">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

<span data-ttu-id="20b8d-112">In tegenstelling tot posten die zijn geboekt met documenten, die een creditnotaproces vereisen, kunt posten correct tegenboeken die met het diversendagboek zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="20b8d-112">Unlike for entries that are posted with documents, which require a credit memo process, you can correctly reverse entries that are posted with the general journal.</span></span> <span data-ttu-id="20b8d-113">Zie voor meer informatie [Journaalboekingen tegenboeken en ontvangsten/zendingen ongedaan maken](finance-how-reverse-journal-posting.md).</span><span class="sxs-lookup"><span data-stu-id="20b8d-113">For more information, see [Reverse Journal Postings and Undo Receipts/Shipments](finance-how-reverse-journal-posting.md).</span></span>

## <a name="to-post-a-transaction-directly-to-a-general-ledger-account"></a><span data-ttu-id="20b8d-114">Een transactie direct naar het grootboek boeken</span><span class="sxs-lookup"><span data-stu-id="20b8d-114">To post a transaction directly to a general ledger account</span></span>

1. <span data-ttu-id="20b8d-115">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële dagboeken** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="20b8d-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="20b8d-116">Open de relevante dagboekbatch.</span><span class="sxs-lookup"><span data-stu-id="20b8d-116">Open the relevant general journal batch.</span></span> <span data-ttu-id="20b8d-117">Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="20b8d-117">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="20b8d-118">Vul op een nieuwe dagboekregel de velden indien nodig in.</span><span class="sxs-lookup"><span data-stu-id="20b8d-118">On a new journal line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]    

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. <span data-ttu-id="20b8d-119">Herhaal stap 3 voor alle afzonderlijke transacties die u wilt boeken.</span><span class="sxs-lookup"><span data-stu-id="20b8d-119">Repeat step 3 for all the separate transactions that you want to post.</span></span>

    > [!TIP]  
    > <span data-ttu-id="20b8d-120">Als u meerdere transactieregels boven één tegenrekeningsregel wilt invoeren, bijvoorbeeld, voor één bankrekening, selecteert u het selectievakje **Salderingsbedrag voorstellen** op de regel voor uw batch op de pagina **Fin. dagboekbatches**.</span><span class="sxs-lookup"><span data-stu-id="20b8d-120">If you want to enter multiple transaction lines above one balance-account line, for example, for one bank account, then select the **Suggest Balancing Amount** check box on the line for your batch on the **General Journal Batches** page.</span></span> <span data-ttu-id="20b8d-121">Vervolgens wordt het veld **Bedrag** op de tegenrekeningsregel automatisch ingevuld met de waarde die nodig is om de transacties in balans te brengen.</span><span class="sxs-lookup"><span data-stu-id="20b8d-121">Then the **Amount** field on the balance-account line is automatically prefilled with the value that is required to balance the transactions.</span></span>
5. <span data-ttu-id="20b8d-122">Kies de actie **Boeken** om de transacties op de betreffende grootboekrekeningen te registreren.</span><span class="sxs-lookup"><span data-stu-id="20b8d-122">Choose the **Post** action to record the transactions on the specified G/L accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="20b8d-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="20b8d-123">See Also</span></span>

[<span data-ttu-id="20b8d-124">Werken met diversendagboeken</span><span class="sxs-lookup"><span data-stu-id="20b8d-124">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="20b8d-125">Kosten van werknemers registreren en terugbetalen</span><span class="sxs-lookup"><span data-stu-id="20b8d-125">Record and Reimburse Employees' Expenses</span></span>](finance-how-record-reimburse-employee-expenses.md)  
[<span data-ttu-id="20b8d-126">Journaalboekingen tegenboeken en ontvangsten/zendingen ongedaan maken</span><span class="sxs-lookup"><span data-stu-id="20b8d-126">Reverse Journal Postings and Undo Receipts/Shipments</span></span>](finance-how-reverse-journal-posting.md)  
[<span data-ttu-id="20b8d-127">Financiën</span><span class="sxs-lookup"><span data-stu-id="20b8d-127">Finance</span></span>](finance.md)  
<span data-ttu-id="20b8d-128">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="20b8d-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
