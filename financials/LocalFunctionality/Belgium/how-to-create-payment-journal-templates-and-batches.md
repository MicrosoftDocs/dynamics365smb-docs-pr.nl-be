---
title: Betalingsdagboeksjablonen en -batches maken
description: In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] worden betalingsvoorstellen gegenereerd en geboekt in betalingsdagboeken. De structuur van het betalingsdagboek lijkt op die van andere dagboeksoorten.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 02a1b3a9226abdd1278dab5fb43566243cd85172
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="create-payment-journal-templates-and-batches"></a><span data-ttu-id="fc976-104">Betalingsdagboeksjablonen en -batches maken</span><span class="sxs-lookup"><span data-stu-id="fc976-104">Create Payment Journal Templates and Batches</span></span>
<span data-ttu-id="fc976-105">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] worden betalingsvoorstellen gegenereerd en geboekt in betalingsdagboeken.</span><span class="sxs-lookup"><span data-stu-id="fc976-105">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], payment suggestions are generated and posted in payment journals.</span></span> <span data-ttu-id="fc976-106">De structuur van het betalingsdagboek lijkt op die van andere dagboeksoorten.</span><span class="sxs-lookup"><span data-stu-id="fc976-106">The structure of the payment journal is similar to the structure of other journal types.</span></span> <span data-ttu-id="fc976-107">Het betalingsdagboek bevat echter enkele velden die specifiek betrekking hebben op het verwerken van betalingen.</span><span class="sxs-lookup"><span data-stu-id="fc976-107">However, the payment journal contains some fields that are specific for processing payments.</span></span> <span data-ttu-id="fc976-108">Voordat u betalingsvoorstellen kunt genereren, moet u een betalingsdagboeksjabloon en een betalingsdagboekbatch instellen.</span><span class="sxs-lookup"><span data-stu-id="fc976-108">Before you can start generating payment suggestions, you have to set up a payment journal template and a payment journal batch.</span></span>  

<span data-ttu-id="fc976-109">Als u een bankrekening toewijst aan de betalingsdagboeksjabloon, wordt de bankrekening ingevoegd in alle betalingsdagboekbatches en betalingsdagboekregels die met deze sjabloon worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fc976-109">If you assign a bank account to the payment journal template, the bank account will be inserted on all payment journal batches and payment journal lines that are created by using this template.</span></span> <span data-ttu-id="fc976-110">Door een bankrekening voor de dagboeksjabloon op te geven, kunt u de benodigde tijd voor het controleren van de betalingsvoorstellen beperken.</span><span class="sxs-lookup"><span data-stu-id="fc976-110">By specifying a bank account for the journal template, you can reduce the time that is required for checking the payment suggestions.</span></span>  

## <a name="to-create-a-payment-journal-template"></a><span data-ttu-id="fc976-111">Een betalingsdagboeksjabloon maken</span><span class="sxs-lookup"><span data-stu-id="fc976-111">To create a payment journal template</span></span>  

1.  <span data-ttu-id="fc976-112">Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsdagboeksjablonen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="fc976-112">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journal Templates**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="fc976-113">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="fc976-113">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="fc976-114">Vul in het venster **Betalingsdagboeksjablonen** de velden in zoals wordt beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="fc976-114">In the **EB Payment Journal Templates** window, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="fc976-115">Veld</span><span class="sxs-lookup"><span data-stu-id="fc976-115">Field</span></span>|<span data-ttu-id="fc976-116">Description</span><span class="sxs-lookup"><span data-stu-id="fc976-116">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="fc976-117">**Naam**</span><span class="sxs-lookup"><span data-stu-id="fc976-117">**Name**</span></span>|<span data-ttu-id="fc976-118">Voer de unieke naam in van de betalingsdagboeksjabloon die u maakt.</span><span class="sxs-lookup"><span data-stu-id="fc976-118">Enter the unique name for the payment journal template that you are creating.</span></span>|  
    |<span data-ttu-id="fc976-119">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="fc976-119">**Description**</span></span>|<span data-ttu-id="fc976-120">Voer een omschrijving voor de betalingsdagboeksjabloon in.</span><span class="sxs-lookup"><span data-stu-id="fc976-120">Enter a description of the payment journal template.</span></span>|  
    |<span data-ttu-id="fc976-121">**Bankrekening**</span><span class="sxs-lookup"><span data-stu-id="fc976-121">**Bank Account**</span></span>|<span data-ttu-id="fc976-122">Selecteer de bankrekening die wordt gebruikt als u een betalingsvoorstel maakt.</span><span class="sxs-lookup"><span data-stu-id="fc976-122">Select the bank account that will be used when you create a payment suggestion.</span></span>|  
    |<span data-ttu-id="fc976-123">**Redencode**</span><span class="sxs-lookup"><span data-stu-id="fc976-123">**Reason Code**</span></span>|<span data-ttu-id="fc976-124">Selecteer de redencode die wordt gebruikt voor alle dagboekbatches en regels die worden gemaakt met de dagboeksjabloon.</span><span class="sxs-lookup"><span data-stu-id="fc976-124">Select the reason code that will be used on all the journal batches and lines that are created by using the journal template.</span></span> <span data-ttu-id="fc976-125">Als u een andere redencode op een dagboekregel wilt gebruiken, kunt u deze handmatig wijzigen.</span><span class="sxs-lookup"><span data-stu-id="fc976-125">If you want to use a different reason code on a journal line, you can manually change it.</span></span>|  
    |<span data-ttu-id="fc976-126">**Broncode**</span><span class="sxs-lookup"><span data-stu-id="fc976-126">**Source Code**</span></span>|<span data-ttu-id="fc976-127">Selecteer de broncode die wordt gebruikt voor alle dagboekbatches en regels die worden gemaakt met de dagboeksjabloon.</span><span class="sxs-lookup"><span data-stu-id="fc976-127">Select the source code that will be used on all the journal batches and lines that are created by using the journal template.</span></span>|  

4.  <span data-ttu-id="fc976-128">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc976-128">Choose the **OK** button.</span></span>  

## <a name="to-add-payment-journal-batches-to-the-journal-template"></a><span data-ttu-id="fc976-129">Betalingsdagboekbatches toevoegen aan de dagboeksjabloon</span><span class="sxs-lookup"><span data-stu-id="fc976-129">To add payment journal batches to the journal template</span></span>  

1.  <span data-ttu-id="fc976-130">Kies in het venster **Betalingsdagboeksjablonen** de actie **Batches**.</span><span class="sxs-lookup"><span data-stu-id="fc976-130">In the **Payment Journal Templates** window, choose the **Batches** action.</span></span>  
2.  <span data-ttu-id="fc976-131">Vul in het venster **Betalingsdagboekbatch** de velden in zoals wordt beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="fc976-131">In the **Paym. Journal Batch** window, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="fc976-132">Veld</span><span class="sxs-lookup"><span data-stu-id="fc976-132">Field</span></span>|<span data-ttu-id="fc976-133">Description</span><span class="sxs-lookup"><span data-stu-id="fc976-133">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="fc976-134">**Dagboeksjabloon**</span><span class="sxs-lookup"><span data-stu-id="fc976-134">**Journal Template Name**</span></span>|<span data-ttu-id="fc976-135">Geef een dagboeksjabloonnaam op voor de betalingsdagboekbatch.</span><span class="sxs-lookup"><span data-stu-id="fc976-135">Specify a journal template name for the payment journal batch.</span></span>|  
    |<span data-ttu-id="fc976-136">**Naam**</span><span class="sxs-lookup"><span data-stu-id="fc976-136">**Name**</span></span>|<span data-ttu-id="fc976-137">Voer een unieke naam voor de dagboekbatch in.</span><span class="sxs-lookup"><span data-stu-id="fc976-137">Enter a unique name for the journal batch.</span></span><br /><br /> <span data-ttu-id="fc976-138">**OPMERKING:** als de dagboeknaam numeriek moet wordt bijgewerkt, neemt u een nummer op in de dagboekbatchnaam.</span><span class="sxs-lookup"><span data-stu-id="fc976-138">**NOTE:** To have the journal name update numerically, include a number in the journal batch name.</span></span> <span data-ttu-id="fc976-139">Zo wordt de waarde in de batchnaam KBC1 bij elke nieuwe boeking verhoogd (KBC2, KBC3, enzovoort).</span><span class="sxs-lookup"><span data-stu-id="fc976-139">For example, the name KBC1 will increment by one number with every posting to KBC2, KBC3, and so on.</span></span>|  
    |<span data-ttu-id="fc976-140">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="fc976-140">**Description**</span></span>|<span data-ttu-id="fc976-141">Voer een omschrijving voor de dagboekbatch in.</span><span class="sxs-lookup"><span data-stu-id="fc976-141">Enter a description for the journal batch.</span></span>|  
    |<span data-ttu-id="fc976-142">**Redencode**</span><span class="sxs-lookup"><span data-stu-id="fc976-142">**Reason Code**</span></span>|<span data-ttu-id="fc976-143">Hiermee wordt de redencode opgegeven die is gekoppeld aan de dagboekbatch.</span><span class="sxs-lookup"><span data-stu-id="fc976-143">Specifies the reason code that is linked to this journal batch.</span></span>|  
    |<span data-ttu-id="fc976-144">**Status**</span><span class="sxs-lookup"><span data-stu-id="fc976-144">**Status**</span></span>|<span data-ttu-id="fc976-145">Hiermee wordt de status van de batch opgegeven.</span><span class="sxs-lookup"><span data-stu-id="fc976-145">Specifies the status of the batch.</span></span>|  

3.  <span data-ttu-id="fc976-146">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc976-146">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fc976-147">Zie ook</span><span class="sxs-lookup"><span data-stu-id="fc976-147">See Also</span></span>  
 <span data-ttu-id="fc976-148">[Belgische elektronische betalingen](belgian-electronic-payments.md) </span><span class="sxs-lookup"><span data-stu-id="fc976-148">[Belgian Electronic Payments](belgian-electronic-payments.md) </span></span>  
 <span data-ttu-id="fc976-149">[Elektronisch bankieren instellen](how-to-set-up-electronic-banking.md) </span><span class="sxs-lookup"><span data-stu-id="fc976-149">[Set Up Electronic Banking](how-to-set-up-electronic-banking.md) </span></span>  
 [<span data-ttu-id="fc976-150">IBLC-BLWI-transactiecodes instellen</span><span class="sxs-lookup"><span data-stu-id="fc976-150">Set Up IBLC-BLWI Transaction Codes</span></span>](how-to-set-up-iblc-blwi-transaction-codes.md)

