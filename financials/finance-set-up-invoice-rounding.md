---
title: Factuurafronding instellen | Microsoft Docs
description: U kunt factuurbedragen afronden wanneer u facturen maakt. Volgens lokale voorschriften of gebruiken moet de factuur mogelijk op een specifieke manier worden afgerond, bijvoorbeeld op een bedrag dat door 0,05 kan worden gedeeld.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f56e94d0914aaacc722381790688faedbb75ffda
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="set-up-invoice-rounding"></a><span data-ttu-id="dca75-104">Factuurafronding instellen</span><span class="sxs-lookup"><span data-stu-id="dca75-104">Set Up Invoice Rounding</span></span>
<span data-ttu-id="dca75-105">Als u factuurbedragen moet afronden wanneer u facturen maakt, kunt u de automatische afrondingsfunctie gebruiken.</span><span class="sxs-lookup"><span data-stu-id="dca75-105">If you need to round invoice amounts when you create invoices, you can use the automatic rounding function.</span></span> <span data-ttu-id="dca75-106">Wanneer een factuur wordt afgerond, wordt een extra regel met het afrondingsbedrag toegevoegd. Deze regel wordt tegelijk met andere factuurregels geboekt.</span><span class="sxs-lookup"><span data-stu-id="dca75-106">When an invoice is rounded, an extra line is added with the rounding amount and posted with the other invoice lines.</span></span>

> [!NOTE]  
>  <span data-ttu-id="dca75-107">Volgens lokale voorschriften of gebruiken moet de factuur mogelijk op een specifieke manier worden afgerond, bijvoorbeeld op een bedrag dat door 0,05 kan worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="dca75-107">Local regulations or local custom may require the invoice to be rounded in a specific way, for example, to an amount divisible by 0.05.</span></span>  
  
<span data-ttu-id="dca75-108">Als u automatische factuurafronding wilt gebruiken, moet u het volgende doen:</span><span class="sxs-lookup"><span data-stu-id="dca75-108">To use automatic invoice rounding, you must:</span></span>  
  
* <span data-ttu-id="dca75-109">Opgeven naar welke grootboekrekeningen de afrondingsverschillen worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="dca75-109">Specify the general ledger accounts to which rounding differences will be posted.</span></span>  
* <span data-ttu-id="dca75-110">Regels voor afrondingsfacturen in lokale en vreemde valuta's instellen.</span><span class="sxs-lookup"><span data-stu-id="dca75-110">Set up rules for rounding invoices in local currency and in foreign currency.</span></span>  
* <span data-ttu-id="dca75-111">De functie activeren.</span><span class="sxs-lookup"><span data-stu-id="dca75-111">Activate the function.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="dca75-112">U kunt factuurbedragen niet alleen afronden met de functies voor factuurafronding, maar ook met de functie voor prijsafronding en de functie voor bedragafronding.</span><span class="sxs-lookup"><span data-stu-id="dca75-112">In addition to the invoice rounding features, you can round amounts on invoices by the unit-amount rounding feature and the amount rounding feature.</span></span>  
 
## <a name="how-to-set-up-general-ledger-accounts-for-invoice-rounding-differences"></a><span data-ttu-id="dca75-113">Procedure: grootboekrekeningen voor factuurafrondingsverschillen instellen</span><span class="sxs-lookup"><span data-stu-id="dca75-113">How to: Set up general ledger accounts for invoice rounding differences</span></span>
<span data-ttu-id="dca75-114">Als u de functie voor automatische factuurafronding wilt gebruiken, moet u de grootboekrekening(en) instellen waarnaar de afrondingsverschillen moeten worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="dca75-114">To use the automatic invoice rounding function, you must set up the general ledger account or accounts where rounding differences will be posted.</span></span> <span data-ttu-id="dca75-115">Als u dit wilt doen, moet u Btw-productboekingsgroepen instellen.</span><span class="sxs-lookup"><span data-stu-id="dca75-115">Before you can do this, you must set up VAT product posting groups.</span></span> <span data-ttu-id="dca75-116">Zie voor meer informatie [Btw instellen](finance-setup-vat.md).</span><span class="sxs-lookup"><span data-stu-id="dca75-116">For more information, see [Set up VAT](finance-setup-vat.md).</span></span>  
  
### <a name="to-set-up-general-ledger-accounts-for-invoice-rounding-differences"></a><span data-ttu-id="dca75-117">Grootboekrekeningen voor factuurafrondingsverschillen instellen</span><span class="sxs-lookup"><span data-stu-id="dca75-117">To set up general ledger accounts for invoice rounding differences</span></span>  
1. <span data-ttu-id="dca75-118">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rekeningschema** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="dca75-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dca75-119">Stel de rekening op de pagina **Rekeningschema** in en geef deze de naam **Factuurafronding** of iets dergelijks.</span><span class="sxs-lookup"><span data-stu-id="dca75-119">On the **Chart of Accounts** page, set up the account and name it **Invoice Rounding** or something similar.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="dca75-120"> gebruikt de rekeningnaam als tekst voor facturen die worden afgerond.</span><span class="sxs-lookup"><span data-stu-id="dca75-120"> will use the account name as text for invoices that are rounded.</span></span>  
3. <span data-ttu-id="dca75-121">Afhankelijk van of u btw gebruikt of sales tax, kiest u in de velden **Btw-productboekingsgroep** of **Btw-prod.-boekingsgroep** een boekingsgroep voor afgeronde bedragen.</span><span class="sxs-lookup"><span data-stu-id="dca75-121">Depending on whether you use VAT or sales tax, in the **Tax Prod. Posting Group** or **VAT Prod. Posting Group** fields, choose a posting group for rounded amounts.</span></span> <span data-ttu-id="dca75-122">U wilt wellicht een nieuwe groepcode instellen die u kunt gebruiken voor factuurafronding.</span><span class="sxs-lookup"><span data-stu-id="dca75-122">You may want to set up a new group code to use for invoice rounding.</span></span>
4. <span data-ttu-id="dca75-123">Laat de velden **Algemeen boekingssoort**, en **Btw-bedrijfsboekingsgroep** of **Btw-bedr.-boekingsgroep** leeg.</span><span class="sxs-lookup"><span data-stu-id="dca75-123">Leave the **Gen. Posting Type**, and either the **Tax Bus. Posting Group** or **VAT Bus. Posting Group** fields blank.</span></span> <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  
  
<span data-ttu-id="dca75-124">U kunt nu de factuurafrondingsrekening toewijzen aan boekingsgroepen in het venster **Leveranciersboekingsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="dca75-124">Now you can assign the invoice rounding account to posting groups on the **Vendor Posting Groups** page.</span></span>  <!-- Why only the vendor posting groups? -->

## <a name="how-to-set-up-rounding-for-foreign-and-local-currencies"></a><span data-ttu-id="dca75-125">Procedure: afronding instellen voor vreemde en lokale valuta's</span><span class="sxs-lookup"><span data-stu-id="dca75-125">How to: Set up rounding for foreign and local currencies</span></span>
<span data-ttu-id="dca75-126">Voordat u de automatische factuurafrondingsfunctie kunt gebruiken, moet u afrondingsregels instellen voor vreemde en lokale valuta's.</span><span class="sxs-lookup"><span data-stu-id="dca75-126">Before you can use the automatic invoice rounding function, you must set up rounding rules for foreign and local currencies.</span></span>

### <a name="to-set-up-rounding-for-foreign-currencies"></a><span data-ttu-id="dca75-127">Afronding instellen voor vreemde valuta's</span><span class="sxs-lookup"><span data-stu-id="dca75-127">To set up rounding for foreign currencies</span></span>  
1. <span data-ttu-id="dca75-128">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Valuta's** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="dca75-128">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Currencies**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dca75-129">Kies op de pagina **Valuta's** de vreemde valuta om de **valutakaart** te openen en vul de velden **Bedragafrondingsprecisie**, **Prijsafrondingsprecisie**, **Factuurafrondingsprecisie** en **Factuurafrondingsmethode** in.</span><span class="sxs-lookup"><span data-stu-id="dca75-129">On the **Currencies** page, choose the foreign currency to open the **Currency Card**, and then fill in the **Amount Rounding Precision**, **Unit-Amount Rounding Precision**, **Invoice Rounding Precision** and **Invoice Rounding Type** fields.</span></span>
  
### <a name="to-set-up-rounding-for-your-local-currency"></a><span data-ttu-id="dca75-130">Afronding instellen voor uw lokale valuta</span><span class="sxs-lookup"><span data-stu-id="dca75-130">To set up rounding for your local currency</span></span>
1. <span data-ttu-id="dca75-131">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Grootboekinstellingen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="dca75-131">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Ledger Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dca75-132">Vul op de pagina **Boekhoudinstellingen** op het sneltabblad **Algemeen** de velden **Factuurafr.-precisie** en **Factuurafr.-methode** in.</span><span class="sxs-lookup"><span data-stu-id="dca75-132">On the **General Ledger Setup** page, on the **General** FastTab, fill in the **Inv. Rounding Precision** and **Inv. Rounding Type** fields.</span></span>  

## <a name="how-to-activate-the-invoice-rounding-function"></a><span data-ttu-id="dca75-133">Procedure: De functie voor factuurafronding inschakelen</span><span class="sxs-lookup"><span data-stu-id="dca75-133">How to: Activate the invoice rounding function</span></span>  
<span data-ttu-id="dca75-134">Om ervoor te zorgen dat verkoop- en inkoopfacturen automatisch worden afgerond, moet u de functie voor factuurafronding inschakelen.</span><span class="sxs-lookup"><span data-stu-id="dca75-134">To ensure that sales and purchase invoices are rounded automatically, you must activate the invoice rounding function.</span></span> <span data-ttu-id="dca75-135">U kunt factuurafronding apart instellen voor verkoopfacturen en inkoopfacturen.</span><span class="sxs-lookup"><span data-stu-id="dca75-135">You activate invoice rounding separately for sales and purchase invoices.</span></span>

1. <span data-ttu-id="dca75-136">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Instellingen van verkoop en tegoeden** of **Inkoopinstellingen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="dca75-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales & Receivables Setup** or **Purchases & Payables Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dca75-137">Kies op het sneltabblad **Algemeen** het selectievakje **Factuurafronding**.</span><span class="sxs-lookup"><span data-stu-id="dca75-137">On the **General** FastTab, choose the **Invoice Rounding** check box.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dca75-138">Zie ook</span><span class="sxs-lookup"><span data-stu-id="dca75-138">See Also</span></span>  
[<span data-ttu-id="dca75-139">Procedure: Verkopen factureren</span><span class="sxs-lookup"><span data-stu-id="dca75-139">How to: Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="dca75-140">Procedure: Inkopen vastleggen</span><span class="sxs-lookup"><span data-stu-id="dca75-140">How to: Record Purchases</span></span>](purchasing-how-record-purchases.md)
