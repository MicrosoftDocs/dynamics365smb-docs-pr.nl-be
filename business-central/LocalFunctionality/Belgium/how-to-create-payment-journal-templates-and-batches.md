---
title: Betalingsdagboeksjablonen en -batches maken
description: In de Belgische versie van Business Central worden betalingsvoorstellen gegenereerd en geboekt in betalingsdagboeken. De structuur van het betalingsdagboek lijkt op die van andere dagboeksoorten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1cbfb5a74c54a39ab3ed2bc11b7f4c3eca5964bd
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775007"
---
# <a name="create-payment-journal-templates-and-batches"></a><span data-ttu-id="aa199-104">Betalingsdagboeksjablonen en -batches maken</span><span class="sxs-lookup"><span data-stu-id="aa199-104">Create Payment Journal Templates and Batches</span></span>
<span data-ttu-id="aa199-105">In [!INCLUDE[prod_short](../../includes/prod_short.md)] worden betalingsvoorstellen gegenereerd en geboekt in betalingsdagboeken.</span><span class="sxs-lookup"><span data-stu-id="aa199-105">In [!INCLUDE[prod_short](../../includes/prod_short.md)], payment suggestions are generated and posted in payment journals.</span></span> <span data-ttu-id="aa199-106">De structuur van het betalingsdagboek lijkt op die van andere dagboeksoorten.</span><span class="sxs-lookup"><span data-stu-id="aa199-106">The structure of the payment journal is similar to the structure of other journal types.</span></span> <span data-ttu-id="aa199-107">Het betalingsdagboek bevat echter enkele velden die specifiek betrekking hebben op het verwerken van betalingen.</span><span class="sxs-lookup"><span data-stu-id="aa199-107">However, the payment journal contains some fields that are specific for processing payments.</span></span> <span data-ttu-id="aa199-108">Voordat u betalingsvoorstellen kunt genereren, moet u een betalingsdagboeksjabloon en een betalingsdagboekbatch instellen.</span><span class="sxs-lookup"><span data-stu-id="aa199-108">Before you can start generating payment suggestions, you have to set up a payment journal template and a payment journal batch.</span></span>  

<span data-ttu-id="aa199-109">Als u een bankrekening toewijst aan de betalingsdagboeksjabloon, wordt de bankrekening ingevoegd in alle betalingsdagboekbatches en betalingsdagboekregels die met deze sjabloon worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="aa199-109">If you assign a bank account to the payment journal template, the bank account will be inserted on all payment journal batches and payment journal lines that are created by using this template.</span></span> <span data-ttu-id="aa199-110">Door een bankrekening voor de dagboeksjabloon op te geven, kunt u de benodigde tijd voor het controleren van de betalingsvoorstellen beperken.</span><span class="sxs-lookup"><span data-stu-id="aa199-110">By specifying a bank account for the journal template, you can reduce the time that is required for checking the payment suggestions.</span></span>  

## <a name="to-create-a-payment-journal-template"></a><span data-ttu-id="aa199-111">Een betalingsdagboeksjabloon maken</span><span class="sxs-lookup"><span data-stu-id="aa199-111">To create a payment journal template</span></span>  

1. <span data-ttu-id="aa199-112">Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsdagboeksjablonen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="aa199-112">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journal Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="aa199-113">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="aa199-113">Choose the **New** action.</span></span>  
3. <span data-ttu-id="aa199-114">Vul de velden op de pagina **EB-betalingsdagboeksjablonen** in.</span><span class="sxs-lookup"><span data-stu-id="aa199-114">On the **EB Payment Journal Templates** page, fill in the fields.</span></span>  

    [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > <span data-ttu-id="aa199-115">Als de velden **Pagina-id** en **Testrapport-id** niet worden weergegeven, moet u deze velden toevoegen via personalisatie.</span><span class="sxs-lookup"><span data-stu-id="aa199-115">If the **Page ID** and **Test Report ID** fields are not shown, you must add them through personalization.</span></span> <span data-ttu-id="aa199-116">U kunt pas doorgaan als de velden zijn ingevuld.</span><span class="sxs-lookup"><span data-stu-id="aa199-116">The fields must be filled in before you continue.</span></span> <span data-ttu-id="aa199-117">Zie [Uw werkruimte personaliseren](../../ui-personalization-user.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="aa199-117">For more information, see [Personalize Your Workspace](../../ui-personalization-user.md).</span></span>
4. <span data-ttu-id="aa199-118">Herhaal stap 2 voor aanvullende sjablonen.</span><span class="sxs-lookup"><span data-stu-id="aa199-118">Repeat step 2 for any additional templates.</span></span>

5. <span data-ttu-id="aa199-119">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="aa199-119">Choose the **OK** button.</span></span>  

## <a name="to-add-payment-journal-batches-to-the-journal-template"></a><span data-ttu-id="aa199-120">Betalingsdagboekbatches toevoegen aan de dagboeksjabloon</span><span class="sxs-lookup"><span data-stu-id="aa199-120">To add payment journal batches to the journal template</span></span>  

1.  <span data-ttu-id="aa199-121">Kies op de pagina **Betalingsdagboeksjablonen** de actie **Batches**.</span><span class="sxs-lookup"><span data-stu-id="aa199-121">On the **Payment Journal Templates** page, choose the **Batches** action.</span></span>  
2.  <span data-ttu-id="aa199-122">Vul op de pagina **Betalingsdagboekbatch** de velden in zoals wordt beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="aa199-122">On the **Paym. Journal Batch** page, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="aa199-123">Veld</span><span class="sxs-lookup"><span data-stu-id="aa199-123">Field</span></span>|<span data-ttu-id="aa199-124">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="aa199-124">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="aa199-125">**Naam**</span><span class="sxs-lookup"><span data-stu-id="aa199-125">**Name**</span></span>|<span data-ttu-id="aa199-126">Voer een unieke naam voor de dagboekbatch in.</span><span class="sxs-lookup"><span data-stu-id="aa199-126">Enter a unique name for the journal batch.</span></span><br /><br /> <span data-ttu-id="aa199-127">**OPMERKING:** als de dagboeknaam numeriek moet wordt bijgewerkt, neemt u een nummer op in de dagboekbatchnaam.</span><span class="sxs-lookup"><span data-stu-id="aa199-127">**NOTE:** To have the journal name update numerically, include a number in the journal batch name.</span></span> <span data-ttu-id="aa199-128">Zo wordt de waarde in de batchnaam KBC1 bij elke nieuwe boeking verhoogd (KBC2, KBC3, enzovoort).</span><span class="sxs-lookup"><span data-stu-id="aa199-128">For example, the name KBC1 will increment by one number with every posting to KBC2, KBC3, and so on.</span></span>|  
    |<span data-ttu-id="aa199-129">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="aa199-129">**Description**</span></span>|<span data-ttu-id="aa199-130">Voer een omschrijving voor de dagboekbatch in.</span><span class="sxs-lookup"><span data-stu-id="aa199-130">Enter a description for the journal batch.</span></span>|  
    |<span data-ttu-id="aa199-131">**Redencode**</span><span class="sxs-lookup"><span data-stu-id="aa199-131">**Reason Code**</span></span>|<span data-ttu-id="aa199-132">Optioneel kunt u de redencode opgeven die is gekoppeld aan de dagboekbatch.</span><span class="sxs-lookup"><span data-stu-id="aa199-132">Optionally, specify the reason code that is linked to this journal batch.</span></span>|  
    |<span data-ttu-id="aa199-133">**Status**</span><span class="sxs-lookup"><span data-stu-id="aa199-133">**Status**</span></span>|<span data-ttu-id="aa199-134">Hiermee wordt de status van de batch opgegeven.</span><span class="sxs-lookup"><span data-stu-id="aa199-134">Specifies the status of the batch.</span></span>|

<span data-ttu-id="aa199-135">Vervolgens kunt u de configuratie testen.</span><span class="sxs-lookup"><span data-stu-id="aa199-135">Next, you can test the configuration.</span></span> <span data-ttu-id="aa199-136">Zie [Elektronische documenten testen](how-to-test-electronic-payments.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="aa199-136">For more information, see [Test Electronic Payments](how-to-test-electronic-payments.md).</span></span>  

3.  <span data-ttu-id="aa199-137">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa199-137">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="aa199-138">Zie ook</span><span class="sxs-lookup"><span data-stu-id="aa199-138">See Also</span></span>  
 <span data-ttu-id="aa199-139">[Belgische elektronische betalingen](belgian-electronic-payments.md) </span><span class="sxs-lookup"><span data-stu-id="aa199-139">[Belgian Electronic Payments](belgian-electronic-payments.md) </span></span>  
 <span data-ttu-id="aa199-140">[Elektronisch bankieren instellen](how-to-set-up-electronic-banking.md) </span><span class="sxs-lookup"><span data-stu-id="aa199-140">[Set Up Electronic Banking](how-to-set-up-electronic-banking.md) </span></span>  
 [<span data-ttu-id="aa199-141">IBLC-BLWI-transactiecodes instellen</span><span class="sxs-lookup"><span data-stu-id="aa199-141">Set Up IBLC-BLWI Transaction Codes</span></span>](how-to-set-up-iblc-blwi-transaction-codes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]