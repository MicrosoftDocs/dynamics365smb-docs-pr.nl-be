---
title: Domiciliëringsvoorstellen genereren
description: Als u domiciliëringen hebt ingesteld, kunt u beginnen met het genereren van domiciliëringsvoorstellen. U kunt domiciliëringsvoorstellen alleen voor binnenlandse klanten maken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 89ffe59d74528502bc6549b6b642164264ee62fb
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2300259"
---
# <a name="generate-domiciliation-suggestions"></a><span data-ttu-id="b7a27-104">Domiciliëringsvoorstellen genereren</span><span class="sxs-lookup"><span data-stu-id="b7a27-104">Generate Domiciliation Suggestions</span></span>
<span data-ttu-id="b7a27-105">Als u domiciliëringen hebt ingesteld, kunt u beginnen met het genereren van domiciliëringsvoorstellen.</span><span class="sxs-lookup"><span data-stu-id="b7a27-105">After you have set up domiciliations, you can start generating domiciliation suggestions.</span></span> <span data-ttu-id="b7a27-106">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kunt u domiciliëringsvoorstellen alleen voor binnenlandse klanten maken.</span><span class="sxs-lookup"><span data-stu-id="b7a27-106">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can create domiciliation suggestions for domestic customers only.</span></span>  

## <a name="to-generate-domiciliation-suggestions"></a><span data-ttu-id="b7a27-107">Domiciliëringsvoorstellen genereren</span><span class="sxs-lookup"><span data-stu-id="b7a27-107">To generate domiciliation suggestions</span></span>  

1.  <span data-ttu-id="b7a27-108">Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Domiciliëringsdagboek** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="b7a27-108">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Domiciliation Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b7a27-109">Selecteer in het veld **Batchnaam** de vereiste dagboekbatch en kies vervolgens de actie **Domiciliëringen voorstellen**.</span><span class="sxs-lookup"><span data-stu-id="b7a27-109">In the **Batch Name** field, select the required journal batch, and then choose the **Suggest Domiciliations** action.</span></span>  
3.  <span data-ttu-id="b7a27-110">Vul de velden in zoals weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="b7a27-110">Fill in the fields as displayed in the following table.</span></span>  

    |<span data-ttu-id="b7a27-111">Veld</span><span class="sxs-lookup"><span data-stu-id="b7a27-111">Field</span></span>|<span data-ttu-id="b7a27-112">Description</span><span class="sxs-lookup"><span data-stu-id="b7a27-112">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="b7a27-113">**Vervaldatum**</span><span class="sxs-lookup"><span data-stu-id="b7a27-113">**Due Date**</span></span>|<span data-ttu-id="b7a27-114">Geef hier de vervaldatum voor de batchverwerking op.</span><span class="sxs-lookup"><span data-stu-id="b7a27-114">Enter the due date to be included in the batch job.</span></span> <span data-ttu-id="b7a27-115">Alleen posten met een vervaldatum vóór of op deze datum worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="b7a27-115">Only entries that have a due date before or on this date will be included.</span></span>|  
    |<span data-ttu-id="b7a27-116">**Contantkorting nemen**</span><span class="sxs-lookup"><span data-stu-id="b7a27-116">**Take Payment Discounts**</span></span>|<span data-ttu-id="b7a27-117">Selecteer deze optie als u in de batchverwerking klantposten wilt opnemen waarvoor u een contantkorting kunt krijgen.</span><span class="sxs-lookup"><span data-stu-id="b7a27-117">Select if you want the batch job to include customer ledger entries for which you can receive a payment discount.</span></span>|  
    |<span data-ttu-id="b7a27-118">**Kortingsvervaldatum betaling**</span><span class="sxs-lookup"><span data-stu-id="b7a27-118">**Payment Discount Date**</span></span>|<span data-ttu-id="b7a27-119">Typ de datum die wordt gebruikt om de contantkorting te berekenen.</span><span class="sxs-lookup"><span data-stu-id="b7a27-119">Enter the date that will be used to calculate the payment discount.</span></span>|  
    |<span data-ttu-id="b7a27-120">**Mogelijke terugbetalingen selecteren**</span><span class="sxs-lookup"><span data-stu-id="b7a27-120">**Select Possible Refunds**</span></span>|<span data-ttu-id="b7a27-121">Selecteer deze optie als in de batchverwerking terugbetalingen moeten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="b7a27-121">Select if you want the batch job to include refunds.</span></span>|  
    |<span data-ttu-id="b7a27-122">**Boekingsdatum**</span><span class="sxs-lookup"><span data-stu-id="b7a27-122">**Posting Date**</span></span>|<span data-ttu-id="b7a27-123">Typ de datum die als boekingsdatum verschijnt op de regels die tijdens de batchverwerking in het domiciliëringsdagboek worden ingevoegd.</span><span class="sxs-lookup"><span data-stu-id="b7a27-123">Enter the date that will appear as the posting date on the lines that the batch job inserts in the domiciliation journal.</span></span>|  

4.  <span data-ttu-id="b7a27-124">Voer aanvullende filtercriteria in.</span><span class="sxs-lookup"><span data-stu-id="b7a27-124">Enter any additional filter criteria.</span></span>  
5.  <span data-ttu-id="b7a27-125">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="b7a27-125">Choose the **OK** button.</span></span>  

<span data-ttu-id="b7a27-126">Wanneer de batchverwerking is uitgevoerd, bevat het domiciliëringsdagboek alle openstaande klantenposten die overeenkomen met de filters.</span><span class="sxs-lookup"><span data-stu-id="b7a27-126">When the batch job is finished, the domiciliation journal contains all open customer ledger entries that match the filters.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b7a27-127">De domiciliëringsvoorstellen bevatten alleen klanten waarvoor een domiciliëringsnummer is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="b7a27-127">The domiciliation suggestions will include only customers who have a Domiciliation number set up.</span></span> <span data-ttu-id="b7a27-128">Zie [Domiciliëringen instellen](how-to-set-up-domiciliations.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="b7a27-128">For more information, see [Set Up Domiciliations](how-to-set-up-domiciliations.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="b7a27-129">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b7a27-129">See Also</span></span>  
 <span data-ttu-id="b7a27-130">[Elektronisch bankieren voor België](belgian-electronic-banking.md) </span><span class="sxs-lookup"><span data-stu-id="b7a27-130">[Belgian Electronic Banking](belgian-electronic-banking.md) </span></span>  
 <span data-ttu-id="b7a27-131">[Incasso via domiciliëring](direct-debit-using-domiciliation.md) </span><span class="sxs-lookup"><span data-stu-id="b7a27-131">[Direct Debit Using Domiciliation](direct-debit-using-domiciliation.md) </span></span>  
 <span data-ttu-id="b7a27-132">[Domiciliëringen instellen](how-to-set-up-domiciliations.md) </span><span class="sxs-lookup"><span data-stu-id="b7a27-132">[Set Up Domiciliations](how-to-set-up-domiciliations.md) </span></span>  
 <span data-ttu-id="b7a27-133">[Domiciliëringen testen](how-to-test-domiciliations.md) </span><span class="sxs-lookup"><span data-stu-id="b7a27-133">[Test Domiciliations](how-to-test-domiciliations.md) </span></span>  
 <span data-ttu-id="b7a27-134">[Domiciliëringsregels bewerken en verwijderen](how-to-edit-and-delete-domiciliation-lines.md) </span><span class="sxs-lookup"><span data-stu-id="b7a27-134">[Edit and Delete Domiciliation Lines](how-to-edit-and-delete-domiciliation-lines.md) </span></span>  
 [<span data-ttu-id="b7a27-135">Domiciliëringen exporteren en boeken</span><span class="sxs-lookup"><span data-stu-id="b7a27-135">Export and Post Domiciliations</span></span>](how-to-export-and-post-domiciliations.md)
