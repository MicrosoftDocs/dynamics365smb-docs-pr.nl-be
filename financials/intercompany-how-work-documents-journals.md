---
title: Intercompany-documenten en -dagboeken boeken | Microsoft Docs
description: IC-documenten te gebruiken om transacties met uw IC-partners te boeken.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 06/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 98e0d9012dfdd998431aaed8dade02f592af47c8
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-intercompany-documents-and-journals"></a><span data-ttu-id="622db-103">Werken met intercompany-documenten en -dagboeken</span><span class="sxs-lookup"><span data-stu-id="622db-103">Work with Intercompany Documents and Journals</span></span>
<span data-ttu-id="622db-104">Door middel van intercompany-documenten of -dagboeken kunt u transacties met uw IC-partners boeken.</span><span class="sxs-lookup"><span data-stu-id="622db-104">You use intercompany documents or journals to post transactions with your intercompany partners.</span></span> <span data-ttu-id="622db-105">Wanneer u een IC-document of -dagboekregel boekt in uw bedrijf, wordt een corresponderend document of dagboekregel gemaakt in uw IC-outbox, dat/die u kunt overbrengen naar uw partner.</span><span class="sxs-lookup"><span data-stu-id="622db-105">When you post an intercompany document or journal line in your company, a corresponding document or journal line is created in your intercompany outbox that you can transfer to your partner.</span></span> <span data-ttu-id="622db-106">Uw partner kan de bijbehorende transactie vervolgens boeken in zijn bedrijf, zonder de gegevens opnieuw te hoeven invoeren.</span><span class="sxs-lookup"><span data-stu-id="622db-106">Your partner can then post the corresponding transaction in their company, without having to re-enter the data.</span></span>

<span data-ttu-id="622db-107">Bij inkoop- en verkoopdocumenten zorgt de IC-partnercode voor de betrokken klant of leverancier ervoor dat alle gegenereerde orders en facturen die verband houden met transacties met deze bedrijven de bijbehorende documenten aanmaken in het partnerbedrijf, zodat de rekeningen overal sluitend zijn.</span><span class="sxs-lookup"><span data-stu-id="622db-107">For sales and purchase documents, the intercompany partner code on the involved customer or vendor ensures that all orders and invoices generated pertaining to transactions with these companies will produce corresponding documents in the partner company, resulting in correct balancing of the accounts.</span></span>

<span data-ttu-id="622db-108">Voor IC-diversendagboekregels hoeft u geen rekeningen op te geven voor een aparte reeks boeken, maar geeft u eenvoudigweg de ID van het partnerbedrijf op.</span><span class="sxs-lookup"><span data-stu-id="622db-108">For intercompany general journal lines, you do not need to specify the accounts for an individual set of books, but simply give the identification of the partner company.</span></span> <span data-ttu-id="622db-109">Corresponderende IC-grootboekregels worden dan in het partnerbedrijf gemaakt, die resulteren in het sluitend maken van de boeken van beide bedrijven die bij de transactie zijn betrokken.</span><span class="sxs-lookup"><span data-stu-id="622db-109">Corresponding intercompany general journal lines are then created in the partner company that result in the balancing of the books of both companies involved in a transaction.</span></span>

## <a name="to-fill-in-and-send-an-intercompany-sales-order"></a><span data-ttu-id="622db-110">Een IC-verkooporder invullen en verzenden</span><span class="sxs-lookup"><span data-stu-id="622db-110">To fill in and send an intercompany sales order</span></span>
<span data-ttu-id="622db-111">U kunt verkoop- en inkooporders en retourorders verzenden voordat u deze boekt.</span><span class="sxs-lookup"><span data-stu-id="622db-111">You can send sales and purchase orders and return orders before posting.</span></span> <span data-ttu-id="622db-112">Facturen en creditnota's kunnen pas worden verzonden nadat u deze hebt geboekt.</span><span class="sxs-lookup"><span data-stu-id="622db-112">Invoices and credit memos cannot be sent until they are posted.</span></span>

<span data-ttu-id="622db-113">In de volgende procedure wordt beschreven hoe u een IC-verkooporder kunt invullen en verzenden.</span><span class="sxs-lookup"><span data-stu-id="622db-113">The following procedure describes how to fill in and send an intercompany sales order.</span></span> <span data-ttu-id="622db-114">Dezelfde stappen gelden voor IC-inkooporders en -retourorders en voor geboekte IC-facturen en -creditnota's.</span><span class="sxs-lookup"><span data-stu-id="622db-114">The same steps apply to intercompany purchase orders and return orders, and to posted intercompany invoices and credit memos.</span></span>  

1. <span data-ttu-id="622db-115">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verkooporders** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="622db-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="622db-116">Kies **Nieuw** om een nieuwe verkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="622db-116">Choose **New** to create a new sales order.</span></span> <span data-ttu-id="622db-117">Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="622db-117">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>  
3. <span data-ttu-id="622db-118">Vul de velden in.</span><span class="sxs-lookup"><span data-stu-id="622db-118">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="622db-119">Controleer of de klant een IC-partner is.</span><span class="sxs-lookup"><span data-stu-id="622db-119">Make sure the customer is an intercompany partner.</span></span>
5. <span data-ttu-id="622db-120">Als u de verkooporder wilt verzenden voordat u hem boekt, kiest u de actie **IC-verkooporder verzenden**.</span><span class="sxs-lookup"><span data-stu-id="622db-120">To send the sales order before you post it, choose the **Send IC Sales Order** action.</span></span>

> [!NOTE]
> <span data-ttu-id="622db-121">Als u stap 4 uitvoert, wordt de verkooporder naar uw IC-outbox verplaatst van waaruit u hem later kunt verzenden.</span><span class="sxs-lookup"><span data-stu-id="622db-121">If you do perform step 4, then the sales order will be moved to your intercompany outbox where you can send it later.</span></span> <span data-ttu-id="622db-122">Zie voor meer informatie [De intercompany-inbox en outbox beheren](intercompany-how-manage-intercompany-inbox.md).</span><span class="sxs-lookup"><span data-stu-id="622db-122">For more information, see [Manage the Intercompany Inbox and Outbox](intercompany-how-manage-intercompany-inbox.md).</span></span>

## <a name="to-fill-in-and-post-an-intercompany-journal"></a><span data-ttu-id="622db-123">Een IC-dagboek invullen en boeken</span><span class="sxs-lookup"><span data-stu-id="622db-123">To fill in and post an intercompany journal</span></span>
<span data-ttu-id="622db-124">Wanneer u een IC--diversendagboekregel boekt in uw bedrijf, wordt een corresponderende dagboekregel gemaakt in uw IC-outbox, die u kunt overbrengen naar uw partner.</span><span class="sxs-lookup"><span data-stu-id="622db-124">When you post an intercompany general journal line in your company, a corresponding journal line is created in your intercompany outbox that you can transfer to your partner.</span></span> <span data-ttu-id="622db-125">Uw partner kan de bijbehorende transactie vervolgens boeken in zijn bedrijf, zonder de gegevens opnieuw te hoeven invoeren.</span><span class="sxs-lookup"><span data-stu-id="622db-125">Your partner can then post the corresponding transaction in their company, without having to re-enter the data.</span></span>

1. <span data-ttu-id="622db-126">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **IC-diversendagboeken** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="622db-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **IC General Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="622db-127">Open de relevante dagboekbatch.</span><span class="sxs-lookup"><span data-stu-id="622db-127">Open the relevant journal batch.</span></span> <span data-ttu-id="622db-128">Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="622db-128">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>
3. <span data-ttu-id="622db-129">Vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="622db-129">Fill in the fields as necessary.</span></span>
4. <span data-ttu-id="622db-130">In het veld **Grootboekrekeningnr. IC-partner** voert u de IC-grootboekrekening in waarop het bedrag wordt geboekt in het bedrijf van uw partner.</span><span class="sxs-lookup"><span data-stu-id="622db-130">In the **IC Partner G/L Acc. No.** field, enter the intercompany general ledger account that the amount will be posted to in your partner's company.</span></span>

    > [!NOTE]
    > <span data-ttu-id="622db-131">Dit veld moet worden ingevuld op een regel met een bankrekening of grootboekrekening in het veld **Rek.-nr.** of in het veld **Tegenrekeningnr.**</span><span class="sxs-lookup"><span data-stu-id="622db-131">This field must be filled in on a line with a bank account or general ledger account in either the **Account No.** field or the **Bal. Account No.** field.</span></span>  
5. <span data-ttu-id="622db-132">Kies de actie **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="622db-132">Choose the **Post** action.</span></span>

<span data-ttu-id="622db-133">De betreffende posten worden geboekt in uw bedrijf en een dagboek met de bijbehorende posten wordt gemaakt in uw IC-outbox, die u naar uw partnerbedrijf kunt verzenden.</span><span class="sxs-lookup"><span data-stu-id="622db-133">The involved entries are posted in your company and a journal with the corresponding entries are created in your intercompany outbox that you can send to your partner company.</span></span> <span data-ttu-id="622db-134">Zie voor meer informatie [De intercompany-inbox en outbox beheren](intercompany-how-manage-intercompany-inbox.md).</span><span class="sxs-lookup"><span data-stu-id="622db-134">For more information, see [Manage the Intercompany Inbox and Outbox](intercompany-how-manage-intercompany-inbox.md).</span></span> 

## <a name="see-also"></a><span data-ttu-id="622db-135">Zie ook</span><span class="sxs-lookup"><span data-stu-id="622db-135">See Also</span></span>
[<span data-ttu-id="622db-136">Intercompany-transacties beheren</span><span class="sxs-lookup"><span data-stu-id="622db-136">Managing Intercompany Transactions</span></span>](intercompany-manage.md)  
[<span data-ttu-id="622db-137">Financiën</span><span class="sxs-lookup"><span data-stu-id="622db-137">Finance</span></span>](finance.md)  
[<span data-ttu-id="622db-138">Financiën instellen</span><span class="sxs-lookup"><span data-stu-id="622db-138">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="622db-139">Werken met diversendagboeken</span><span class="sxs-lookup"><span data-stu-id="622db-139">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="622db-140">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="622db-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

