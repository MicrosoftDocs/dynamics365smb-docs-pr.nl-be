---
title: Posten vereffenen in verschillende valuta's| Microsoft Docs
description: U kunt posten in meerdere valuta's vereffenen, bijvoorbeeld als u verkoopt in een bepaalde valuta en een betaling in een andere ontvangt.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 035f4c0e98e3b7ba308319c2017568de832e26c5
ms.contentlocale: nl-be
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="d0f54-103">Procedure: Vereffening van posten in verschillende valuta's inschakelen</span><span class="sxs-lookup"><span data-stu-id="d0f54-103">How to: Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="d0f54-104">Als de betaling in een andere valuta dan de valuta van de inkoop wordt ingediend, kunt u de betaling met de inkoop vereffenen.</span><span class="sxs-lookup"><span data-stu-id="d0f54-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="d0f54-105">Als u aan een klant verkoopt in een bepaalde valuta en een betaling in een andere valuta ontvangt, kunt u de betaling ook vereffenen met de verkoopfactuur.</span><span class="sxs-lookup"><span data-stu-id="d0f54-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="d0f54-106">In de volgende procedure wordt beschreven hoe u dit instelt voor leveranciersposten in het venster **Inkoopinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="d0f54-106">The following procedure describes how to set this up for vendor ledger entries in the **Purchases & Payables Setup** window.</span></span> <span data-ttu-id="d0f54-107">De instelling is soortgelijk voor klantenposten in het venster **Verkoopinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="d0f54-107">The setup is similar for customer ledger entries in the **Sales & Receivables Setup** window.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d0f54-108">Deze functionaliteit vereist dat uw ervaring is ingesteld op **Pakket**.</span><span class="sxs-lookup"><span data-stu-id="d0f54-108">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="d0f54-109">Zie voor meer informatie [Uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-ervaring aanpassen](ui-experiences.md).</span><span class="sxs-lookup"><span data-stu-id="d0f54-109">For more information, see [Customizing Your [!INCLUDE[d365fin](includes/d365fin_md.md)] Experience](ui-experiences.md).</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="d0f54-110">Vereffening van leveranciersposten in verschillende valuta's inschakelen</span><span class="sxs-lookup"><span data-stu-id="d0f54-110">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="d0f54-111">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Inkoopinstellingen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="d0f54-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="d0f54-112">Selecteer een van de volgende opties in het veld **Valuta's vereffenen**.</span><span class="sxs-lookup"><span data-stu-id="d0f54-112">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="d0f54-113">Optie</span><span class="sxs-lookup"><span data-stu-id="d0f54-113">Option</span></span> | <span data-ttu-id="d0f54-114">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="d0f54-114">Description</span></span> |
| --- | --- |
| <span data-ttu-id="d0f54-115">Geen</span><span class="sxs-lookup"><span data-stu-id="d0f54-115">None</span></span> |<span data-ttu-id="d0f54-116">De vereffening tussen valuta's is niet toegestaan.</span><span class="sxs-lookup"><span data-stu-id="d0f54-116">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="d0f54-117">EMU</span><span class="sxs-lookup"><span data-stu-id="d0f54-117">EMU</span></span> |<span data-ttu-id="d0f54-118">De vereffening tussen EMU-valuta's is toegestaan.</span><span class="sxs-lookup"><span data-stu-id="d0f54-118">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="d0f54-119">Alle</span><span class="sxs-lookup"><span data-stu-id="d0f54-119">All</span></span> |<span data-ttu-id="d0f54-120">De vereffening tussen alle valuta's is toegestaan.</span><span class="sxs-lookup"><span data-stu-id="d0f54-120">Application between all currencies is allowed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="d0f54-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d0f54-121">See Also</span></span>
[<span data-ttu-id="d0f54-122">Betalingsverplichtingen beheren</span><span class="sxs-lookup"><span data-stu-id="d0f54-122">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="d0f54-123">Tegoeden beheren</span><span class="sxs-lookup"><span data-stu-id="d0f54-123">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="d0f54-124">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d0f54-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

