---
title: SEPA-betalingen via automatische incasso boeken | Microsoft Docs
description: Wanneer een incasso-opdracht wordt verwerkt door uw bank, kunt u doorgaan met het boeken van de ontvangst van de betaling voor de betrokken verkoopfacturen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2daa52e1ee4546356ecb7d94b5c01ab9e22bbbd6
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="post-sepa-direct-debit-payment-receipts"></a><span data-ttu-id="7de56-103">SEPA-betalingsontvangsten via automatische incasso boeken</span><span class="sxs-lookup"><span data-stu-id="7de56-103">Post SEPA Direct Debit Payment Receipts</span></span>
<span data-ttu-id="7de56-104">Wanneer een incasso-opdracht wordt verwerkt door uw bank, kunt u doorgaan met het boeken van de ontvangst van de betaling voor de betrokken verkoopfacturen.</span><span class="sxs-lookup"><span data-stu-id="7de56-104">When a direct debit collection is successfully processed by your bank, you can proceed to post receipt of the payment for the involved sales invoices.</span></span> <span data-ttu-id="7de56-105">Zie voor meer informatie [SEPA-verzamelingsposten van automatische incasso maken en exporteren naar een bankbestand](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="7de56-105">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  

<span data-ttu-id="7de56-106">U kunt de betalingsontvangst van het venster **Incasso-opdrachten** of het venster **Verzamelingsposten van incasso** direct boeken.</span><span class="sxs-lookup"><span data-stu-id="7de56-106">You can post the payment receipt directly from the **Direct Debit Collections** window or the **Direct Debit Collect. Entries** window.</span></span> <span data-ttu-id="7de56-107">U kunt ook het werk aan een andere gebruiker doorgeven door de dagboekregels voor te bereiden.</span><span class="sxs-lookup"><span data-stu-id="7de56-107">Alternatively, you can relay the work to another user by preparing the related journal lines.</span></span>  

## <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-window"></a><span data-ttu-id="7de56-108">Een betalingsontvangst van een automatische incasso boeken vanuit het venster Verzamelingen van automatische incasso</span><span class="sxs-lookup"><span data-stu-id="7de56-108">To post a direct-debit payment receipt from the Direct Debit Collections window</span></span>  
1. <span data-ttu-id="7de56-109">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Incasso-opdrachten** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="7de56-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Direct Debit Collections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7de56-110">Selecteer een regel voor een verzameling automatische incasso die is geëxporteerd naar een bankbestand en verwerkt door de bank.</span><span class="sxs-lookup"><span data-stu-id="7de56-110">Select a line for a direct debit collection that has been exported to a bank file and successfully processed by the bank.</span></span> <span data-ttu-id="7de56-111">Zie voor meer informatie [SEPA-verzamelingsposten van automatische incasso maken en exporteren naar een bankbestand](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="7de56-111">For more information, see [Create SEPA Direct Debit Collection Entries and Export to a Bank File](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md).</span></span>  
3. <span data-ttu-id="7de56-112">Kies de actie **Betalingsontvangsten boeken**.</span><span class="sxs-lookup"><span data-stu-id="7de56-112">Choose the **Post Payment Receipts** action.</span></span>  
4. <span data-ttu-id="7de56-113">Vul in het venster **Incasso-opdracht boeken** de velden in, zoals is beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="7de56-113">In the **Post Direct Debit Collection** window, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="7de56-114">Veld</span><span class="sxs-lookup"><span data-stu-id="7de56-114">Field</span></span>|<span data-ttu-id="7de56-115">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="7de56-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="7de56-116">**Incasso-opdrachtnr.**</span><span class="sxs-lookup"><span data-stu-id="7de56-116">**Direct Debit Collection No.**</span></span>|<span data-ttu-id="7de56-117">Geef de verzameling automatische incasso op waar u een betalingsontvangst voor wilt boeken.</span><span class="sxs-lookup"><span data-stu-id="7de56-117">Specify the direct debit collection that you want to post payment receipt for.</span></span>|  
    |<span data-ttu-id="7de56-118">**Algemeen dagboeksjabloon**</span><span class="sxs-lookup"><span data-stu-id="7de56-118">**General Journal Template**</span></span>|<span data-ttu-id="7de56-119">Geef op welk dagboeksjabloon te gebruiken voor het boeken van de betalingsontvangst, zoals de sjabloon voor ontvangsten.</span><span class="sxs-lookup"><span data-stu-id="7de56-119">Specify which general journal template to use for posting the payment receipt, such as the template for cash receipts.</span></span>|  
    |<span data-ttu-id="7de56-120">**Batchnaam financieel dagboek**</span><span class="sxs-lookup"><span data-stu-id="7de56-120">**General Journal Batch Name**</span></span>|<span data-ttu-id="7de56-121">Geef op welke dagboekbatch moet worden gebruikt voor het boeken van de betalingsontvangst.</span><span class="sxs-lookup"><span data-stu-id="7de56-121">Specify which general journal batch to use for posting the payment receipt.</span></span>|  
    |<span data-ttu-id="7de56-122">**Alleen dagboek aanmaken**</span><span class="sxs-lookup"><span data-stu-id="7de56-122">**Create Journal Only**</span></span>|<span data-ttu-id="7de56-123">Schakel dit selectievakje in als u niet de betalingsontvangst boeken wilt wanneer u de **OK** knop kiest.</span><span class="sxs-lookup"><span data-stu-id="7de56-123">Select this check box if you do not want to post the payment receipt when you choose the **OK** button.</span></span> <span data-ttu-id="7de56-124">De betalingsontvangst in het opgegeven dagboek wordt voorbereid en wordt niet geboekt totdat iemand de dagboekregels in kwestie boekt.</span><span class="sxs-lookup"><span data-stu-id="7de56-124">The payment receipt will be prepared in the specified journal and will not be posted until someone posts the journal lines in question.</span></span>|  

5. <span data-ttu-id="7de56-125">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="7de56-125">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7de56-126">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7de56-126">See Also</span></span>  
 <span data-ttu-id="7de56-127">[Betalingen verzamelen via automatische incasso van SEPA](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="7de56-127">[Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
 [<span data-ttu-id="7de56-128">Verkoop</span><span class="sxs-lookup"><span data-stu-id="7de56-128">Sales</span></span>](sales-manage-sales.md)

