---
title: Domiciliëringsvoorstellen genereren
description: Als u domiciliëringen hebt ingesteld, kunt u beginnen met het genereren van domiciliëringsvoorstellen. U kunt domiciliëringsvoorstellen alleen voor binnenlandse klanten maken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6d6bfed431e60079f086d79e2e55ac2e99fa0165
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749702"
---
# <a name="generate-domiciliation-suggestions"></a><span data-ttu-id="f44a8-104">Domiciliëringsvoorstellen genereren</span><span class="sxs-lookup"><span data-stu-id="f44a8-104">Generate Domiciliation Suggestions</span></span>
<span data-ttu-id="f44a8-105">Als u domiciliëringen hebt ingesteld, kunt u beginnen met het genereren van domiciliëringsvoorstellen.</span><span class="sxs-lookup"><span data-stu-id="f44a8-105">After you have set up domiciliations, you can start generating domiciliation suggestions.</span></span> <span data-ttu-id="f44a8-106">In [!INCLUDE[prod_short](../../includes/prod_short.md)] kunt u domiciliëringsvoorstellen alleen voor binnenlandse klanten maken.</span><span class="sxs-lookup"><span data-stu-id="f44a8-106">In [!INCLUDE[prod_short](../../includes/prod_short.md)], you can create domiciliation suggestions for domestic customers only.</span></span>  

## <a name="to-generate-domiciliation-suggestions"></a><span data-ttu-id="f44a8-107">Domiciliëringsvoorstellen genereren</span><span class="sxs-lookup"><span data-stu-id="f44a8-107">To generate domiciliation suggestions</span></span>  

1.  <span data-ttu-id="f44a8-108">Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Domiciliëringsdagboek** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="f44a8-108">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Domiciliation Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f44a8-109">Selecteer in het veld **Batchnaam** de vereiste dagboekbatch en kies vervolgens de actie **Domiciliëringen voorstellen**.</span><span class="sxs-lookup"><span data-stu-id="f44a8-109">In the **Batch Name** field, select the required journal batch, and then choose the **Suggest Domiciliations** action.</span></span>  
3.  <span data-ttu-id="f44a8-110">Vul de velden in zoals weergegeven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="f44a8-110">Fill in the fields as displayed in the following table.</span></span>  

    |<span data-ttu-id="f44a8-111">Veld</span><span class="sxs-lookup"><span data-stu-id="f44a8-111">Field</span></span>|<span data-ttu-id="f44a8-112">Description</span><span class="sxs-lookup"><span data-stu-id="f44a8-112">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="f44a8-113">**Vervaldatum**</span><span class="sxs-lookup"><span data-stu-id="f44a8-113">**Due Date**</span></span>|<span data-ttu-id="f44a8-114">Geef hier de vervaldatum voor de batchverwerking op.</span><span class="sxs-lookup"><span data-stu-id="f44a8-114">Enter the due date to be included in the batch job.</span></span> <span data-ttu-id="f44a8-115">Alleen posten met een vervaldatum vóór of op deze datum worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="f44a8-115">Only entries that have a due date before or on this date will be included.</span></span>|  
    |<span data-ttu-id="f44a8-116">**Contantkorting nemen**</span><span class="sxs-lookup"><span data-stu-id="f44a8-116">**Take Payment Discounts**</span></span>|<span data-ttu-id="f44a8-117">Selecteer deze optie als u in de batchverwerking klantposten wilt opnemen waarvoor u een contantkorting kunt krijgen.</span><span class="sxs-lookup"><span data-stu-id="f44a8-117">Select if you want the batch job to include customer ledger entries for which you can receive a payment discount.</span></span>|  
    |<span data-ttu-id="f44a8-118">**Kortingsvervaldatum betaling**</span><span class="sxs-lookup"><span data-stu-id="f44a8-118">**Payment Discount Date**</span></span>|<span data-ttu-id="f44a8-119">Typ de datum die wordt gebruikt om de contantkorting te berekenen.</span><span class="sxs-lookup"><span data-stu-id="f44a8-119">Enter the date that will be used to calculate the payment discount.</span></span>|  
    |<span data-ttu-id="f44a8-120">**Mogelijke terugbetalingen selecteren**</span><span class="sxs-lookup"><span data-stu-id="f44a8-120">**Select Possible Refunds**</span></span>|<span data-ttu-id="f44a8-121">Selecteer deze optie als in de batchverwerking terugbetalingen moeten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="f44a8-121">Select if you want the batch job to include refunds.</span></span>|  
    |<span data-ttu-id="f44a8-122">**Boekingsdatum**</span><span class="sxs-lookup"><span data-stu-id="f44a8-122">**Posting Date**</span></span>|<span data-ttu-id="f44a8-123">Typ de datum die als boekingsdatum verschijnt op de regels die tijdens de batchverwerking in het domiciliëringsdagboek worden ingevoegd.</span><span class="sxs-lookup"><span data-stu-id="f44a8-123">Enter the date that will appear as the posting date on the lines that the batch job inserts in the domiciliation journal.</span></span>|  

4.  <span data-ttu-id="f44a8-124">Voer aanvullende filtercriteria in.</span><span class="sxs-lookup"><span data-stu-id="f44a8-124">Enter any additional filter criteria.</span></span>  
5.  <span data-ttu-id="f44a8-125">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="f44a8-125">Choose the **OK** button.</span></span>  

<span data-ttu-id="f44a8-126">Wanneer de batchverwerking is uitgevoerd, bevat het domiciliëringsdagboek alle openstaande klantenposten die overeenkomen met de filters.</span><span class="sxs-lookup"><span data-stu-id="f44a8-126">When the batch job is finished, the domiciliation journal contains all open customer ledger entries that match the filters.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f44a8-127">De domiciliëringsvoorstellen bevatten alleen klanten waarvoor een domiciliëringsnummer is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="f44a8-127">The domiciliation suggestions will include only customers who have a Domiciliation number set up.</span></span> <span data-ttu-id="f44a8-128">Zie [Domiciliëringen instellen](how-to-set-up-domiciliations.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f44a8-128">For more information, see [Set Up Domiciliations](how-to-set-up-domiciliations.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="f44a8-129">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f44a8-129">See Also</span></span>  
 <span data-ttu-id="f44a8-130">[Elektronisch bankieren voor België](belgian-electronic-banking.md) </span><span class="sxs-lookup"><span data-stu-id="f44a8-130">[Belgian Electronic Banking](belgian-electronic-banking.md) </span></span>  
 <span data-ttu-id="f44a8-131">[Incasso via domiciliëring](direct-debit-using-domiciliation.md) </span><span class="sxs-lookup"><span data-stu-id="f44a8-131">[Direct Debit Using Domiciliation](direct-debit-using-domiciliation.md) </span></span>  
 <span data-ttu-id="f44a8-132">[Domiciliëringen instellen](how-to-set-up-domiciliations.md) </span><span class="sxs-lookup"><span data-stu-id="f44a8-132">[Set Up Domiciliations](how-to-set-up-domiciliations.md) </span></span>  
 <span data-ttu-id="f44a8-133">[Domiciliëringen testen](how-to-test-domiciliations.md) </span><span class="sxs-lookup"><span data-stu-id="f44a8-133">[Test Domiciliations](how-to-test-domiciliations.md) </span></span>  
 <span data-ttu-id="f44a8-134">[Domiciliëringsregels bewerken en verwijderen](how-to-edit-and-delete-domiciliation-lines.md) </span><span class="sxs-lookup"><span data-stu-id="f44a8-134">[Edit and Delete Domiciliation Lines](how-to-edit-and-delete-domiciliation-lines.md) </span></span>  
 [<span data-ttu-id="f44a8-135">Domiciliëringen exporteren en boeken</span><span class="sxs-lookup"><span data-stu-id="f44a8-135">Export and Post Domiciliations</span></span>](how-to-export-and-post-domiciliations.md)
