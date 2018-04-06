---
title: SEPA-betalingen activeren
description: Als u leveranciersbetalingen elektronisch wilt verzenden in de betalingsindeling SEPA (Single Euro Payments Area) ISO 20022, moet u eerst de vereiste instellingen aanbrengen voor het activeren van SEPA-betalingen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 9d87cea4036d86ca418bc3e9ac0c042cee3eca74
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="activate-sepa-payments"></a><span data-ttu-id="f93ed-103">SEPA-betalingen activeren</span><span class="sxs-lookup"><span data-stu-id="f93ed-103">Activate SEPA Payments</span></span>
<span data-ttu-id="f93ed-104">Als u leveranciersbetalingen elektronisch wilt verzenden in de betalingsindeling SEPA (Single Euro Payments Area) ISO 20022, moet u eerst de vereiste instellingen aanbrengen voor het activeren van SEPA-betalingen.</span><span class="sxs-lookup"><span data-stu-id="f93ed-104">To submit vendor payments electronically in Single Euro Payments Area (SEPA) ISO 20022 payment format, you must set up prerequisites for enabling SEPA payments.</span></span>  

<span data-ttu-id="f93ed-105">In de volgende procedures wordt beschreven hoe u SEPA-betaling inschakelt en leveranciersbankrekeningen inschakelt.</span><span class="sxs-lookup"><span data-stu-id="f93ed-105">In the following procedures describe how to enable SEPA payment and set up vendor bank accounts.</span></span>  

## <a name="to-enable-countriesregions-for-sepa"></a><span data-ttu-id="f93ed-106">Landen/regio's activeren voor SEPA</span><span class="sxs-lookup"><span data-stu-id="f93ed-106">To enable countries/regions for SEPA</span></span>  

1.  <span data-ttu-id="f93ed-107">Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Landen/regio's** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="f93ed-107">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Countries/Regions**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f93ed-108">Kies de actie **Lijst bewerken**.</span><span class="sxs-lookup"><span data-stu-id="f93ed-108">Choose the **Edit List** action.</span></span>  
3.  <span data-ttu-id="f93ed-109">Schakel het selectievakje **SEPA toegestaan** in voor elk land of elke regio dat/die u wilt activeren voor SEPA.</span><span class="sxs-lookup"><span data-stu-id="f93ed-109">Select the **SEPA Allowed** check box for each country or region that you want to enable for SEPA.</span></span>  
4.  <span data-ttu-id="f93ed-110">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="f93ed-110">Choose the **OK** button.</span></span>  

## <a name="to-enable-bank-accounts-for-sepa"></a><span data-ttu-id="f93ed-111">Bankrekeningen activeren voor SEPA</span><span class="sxs-lookup"><span data-stu-id="f93ed-111">To enable bank accounts for SEPA</span></span>  

1.  <span data-ttu-id="f93ed-112">Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bankrekeningen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="f93ed-112">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f93ed-113">Selecteer de bankrekening die u wilt activeren voor SEPA en kies vervolgens de actie **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="f93ed-113">Select the bank account that you want to enable for SEPA, and then choose the **Edit** action.</span></span>  
3.  <span data-ttu-id="f93ed-114">Selecteer in het veld **Land-/regiocode** van het sneltabblad **Algemeen** de gewenste code.</span><span class="sxs-lookup"><span data-stu-id="f93ed-114">On the **General** FastTab, in the **Country/Region Code** field, select the appropriate code.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="f93ed-115">De opgegeven land-/regiocode moet zijn geactiveerd voor SEPA, zoals is beschreven in de vorige procedure.</span><span class="sxs-lookup"><span data-stu-id="f93ed-115">The specified country/region code must be enabled for SEPA as described in the previous procedure.</span></span>  

4.  <span data-ttu-id="f93ed-116">Geef een waarde op in het veld **Minimumsaldo**.</span><span class="sxs-lookup"><span data-stu-id="f93ed-116">Enter a value in the **Min. Balance** field.</span></span>  
5.  <span data-ttu-id="f93ed-117">Geef in het veld **SWIFT-code** van het sneltabblad **Transfer** een code op.</span><span class="sxs-lookup"><span data-stu-id="f93ed-117">On the **Transfer** FastTab, in the **SWIFT Code** field, enter a code.</span></span>  
6.  <span data-ttu-id="f93ed-118">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="f93ed-118">Choose the **OK** button.</span></span>  

## <a name="to-set-up-vendor-bank-accounts-for-sepa"></a><span data-ttu-id="f93ed-119">Bankrekeningen van leveranciers instellen voor SEPA</span><span class="sxs-lookup"><span data-stu-id="f93ed-119">To set up vendor bank accounts for SEPA</span></span>  

1.  <span data-ttu-id="f93ed-120">Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Leveranciers** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="f93ed-120">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f93ed-121">Selecteer de betreffende leverancier en kies vervolgens de actie **Bankrekeningen**.</span><span class="sxs-lookup"><span data-stu-id="f93ed-121">Select the relevant vendor, and then choose the **Bank Accounts** action.</span></span>  
3.  <span data-ttu-id="f93ed-122">Selecteer de bankrekening van een leverancier die u wilt instellen voor SEPA, en kies vervolgens **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="f93ed-122">Select the vendor bank account to set up for SEPA, and then choose the **Edit**.</span></span>  
4.  <span data-ttu-id="f93ed-123">Geef in de velden **IBAN** en **SWIFT-code** van het sneltabblad **Transfer** de internationale bankidentificatiecode op van de bank waarbij de leverancier de rekening heeft.</span><span class="sxs-lookup"><span data-stu-id="f93ed-123">On the **Transfer** FastTab, in the **IBAN** and **SWIFT Code** fields, enter the international bank identifier code of the bank where the vendor has the account.</span></span>  
5.  <span data-ttu-id="f93ed-124">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="f93ed-124">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f93ed-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f93ed-125">See Also</span></span>  
 <span data-ttu-id="f93ed-126">[SEPA-betalingen](sepa-payments.md) </span><span class="sxs-lookup"><span data-stu-id="f93ed-126">[SEPA Payments](sepa-payments.md) </span></span>  
 <span data-ttu-id="f93ed-127">[SEPA-betalingen indienen](how-to-file-sepa-payments.md) </span><span class="sxs-lookup"><span data-stu-id="f93ed-127">[File SEPA Payments](how-to-file-sepa-payments.md) </span></span>  
 <span data-ttu-id="f93ed-128">[SEPA-betalingen in andere valuta's dan de euro indienen](how-to-file-non-euro-sepa-payments.md) </span><span class="sxs-lookup"><span data-stu-id="f93ed-128">[File Non-Euro SEPA Payments](how-to-file-non-euro-sepa-payments.md) </span></span>  
 [<span data-ttu-id="f93ed-129">Exportprotocollen instellen</span><span class="sxs-lookup"><span data-stu-id="f93ed-129">Set Up Export Protocols</span></span>](how-to-set-up-export-protocols.md)

