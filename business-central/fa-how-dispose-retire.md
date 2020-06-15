---
title: Activa afstoten of van de hand doen| Microsoft Docs
description: U moet een buitengebruikstellingwaarde boeken wanneer u een vast activum laat uitvallen, verkoopt of buiten gebruik stelt.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 06/04/2020
ms.author: edupont
ms.openlocfilehash: 29293e957617fea91c9a8e8b8c1f988b06104494
ms.sourcegitcommit: ccae3ff6aaeaa52db9d6456042acdede19fb9f7b
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435219"
---
# <a name="dispose-of-or-retire-fixed-assets"></a><span data-ttu-id="e65e2-103">Vaste activa afstoten of van de hand doen</span><span class="sxs-lookup"><span data-stu-id="e65e2-103">Dispose of or Retire Fixed Assets</span></span>

<span data-ttu-id="e65e2-104">Als u een vast activum verkoopt of anderszins buiten gebruik stelt, moet u de buitengebruikstellingswaarde boeken om de winst of het verlies te berekenen en te registreren.</span><span class="sxs-lookup"><span data-stu-id="e65e2-104">When you sell or otherwise dispose of a fixed asset, the disposal value must be posted to calculate and record the gain or loss.</span></span> <span data-ttu-id="e65e2-105">Een buitengebruikstellingspost is de laatste post die voor een vast activum wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="e65e2-105">A disposal entry must be the last entry posted for a fixed asset.</span></span> <span data-ttu-id="e65e2-106">Voor vaste activa die gedeeltelijk buiten gebruik zijn gesteld, kunt u meerdere buitengebruikstellingsposten boeken.</span><span class="sxs-lookup"><span data-stu-id="e65e2-106">For partially disposed fixed assets, you can post more than one disposal entry.</span></span> <span data-ttu-id="e65e2-107">Het totaal van alle geboekte buitengebruikstellingsbedragen moet een creditbedrag zijn.</span><span class="sxs-lookup"><span data-stu-id="e65e2-107">The total of all posted disposal amounts must be a credit amount.</span></span>  

> [!NOTE]  
> <span data-ttu-id="e65e2-108">Als u een vast activum inruilt, moet u zowel de verkoop van het oude activum (buitengebruikstelling) als de aankoop van het nieuwe activum (aanschaf) registreren.</span><span class="sxs-lookup"><span data-stu-id="e65e2-108">If you trade-in a fixed asset for another one, you must record both the sale of the old asset (disposal) and the purchase of the new one (acquisition).</span></span> <span data-ttu-id="e65e2-109">Zie [Vaste activa aanschaffen](fa-how-acquire.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e65e2-109">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>  

<span data-ttu-id="e65e2-110">Bij de volgende stappen wordt ervan uitgegaan dat u de relevante boekingsgroepen al hebt ingesteld op de pagina **FA-boekingsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="e65e2-110">The following steps assume that you have already set up the relevant posting groups in the **FA Posting Groups** page.</span></span> <span data-ttu-id="e65e2-111">Zie [Boekingsgroepen voor vaste activa instellen](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e65e2-111">For more information, see [To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a><span data-ttu-id="e65e2-112">Een buitengebruikstelling boeken vanuit het financieel dagboek voor vaste activa</span><span class="sxs-lookup"><span data-stu-id="e65e2-112">To post a disposal from the fixed asset G/L journal</span></span>

1. <span data-ttu-id="e65e2-113">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **VA fin. dagboeken** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="e65e2-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Asset G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e65e2-114">Maak een eerste dagboekregel en vul de velden indien nodig in.</span><span class="sxs-lookup"><span data-stu-id="e65e2-114">Create an initial journal line and fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="e65e2-115">In het veld **VA-boekingssoort** selecteert u **Buitengebruikstelling**.</span><span class="sxs-lookup"><span data-stu-id="e65e2-115">In the **FA Posting Type** field, select **Disposal**.</span></span>  
4. <span data-ttu-id="e65e2-116">Kies de actie **VA-tegenrekening invoegen**.</span><span class="sxs-lookup"><span data-stu-id="e65e2-116">Choose the **Insert FA Bal. Account** action.</span></span> <span data-ttu-id="e65e2-117">Er wordt een tweede dagboekregel gemaakt voor de tegenrekening die voor de boeking van de buitengebruikstelling is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="e65e2-117">A second journal line is created for the balancing account that is set up for disposal posting.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="e65e2-118">Stap 4 werkt alleen als u het volgende hebt ingesteld: op de pagina **VA-boekingsgroep** voor de boekingsgroep van het vaste activum bevat het veld **Buitengebruikstellingsrekening** de grootboekdebetrekening en het veld **Tegenrekening buitengebruikstelling** bevat de grootboekrekening waarnaar u tegenrekeningsposten voor buitengebruikstelling wilt boeken.</span><span class="sxs-lookup"><span data-stu-id="e65e2-118">Step 4 only works if you have set up the following: On the **FA Posting Group Card** page for the posting group of the fixed asset, the **Disposal Account** field contains the general ledger debit account and the **Disposal Bal. Account** field contains the general ledger account to which you want to post balancing entries for appreciation.</span></span> <span data-ttu-id="e65e2-119">Zie [Boekingsgroepen voor vaste activa instellen](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e65e2-119">For more information, see [To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  
5. <span data-ttu-id="e65e2-120">Kies de actie **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="e65e2-120">Choose the **Post** action.</span></span>  

<span data-ttu-id="e65e2-121">Als u een gedeelte van een vast activum verkoopt of het niet langer meer gebruikt, moet u het activum opsplitsen voordat u de buitengebruikstellingstransactie kunt vastleggen.</span><span class="sxs-lookup"><span data-stu-id="e65e2-121">If you sell or dispose of part of a fixed asset, you must split up the asset before you can record the disposal transaction.</span></span> <span data-ttu-id="e65e2-122">Zie [Vaste activa overbrengen, splitsen of combineren](fa-how-trans-split-combine.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e65e2-122">For more information, see [Transfer, Split, or Combine Fixed Assets](fa-how-trans-split-combine.md).</span></span>  

## <a name="to-view-disposal-ledger-entries"></a><span data-ttu-id="e65e2-123">Buitengebruikstellingsposten bekijken</span><span class="sxs-lookup"><span data-stu-id="e65e2-123">To view disposal ledger entries</span></span>
<span data-ttu-id="e65e2-124">Als u een vast activum verkoopt of buiten gebruik stelt, moet u de buitengebruikstellingswaarde boeken naar het grootboek waar u het resultaat kunt bekijken.</span><span class="sxs-lookup"><span data-stu-id="e65e2-124">When you sell or dispose of a fixed asset, the disposal value is posted to the general ledger where you can view the result.</span></span>  

1. <span data-ttu-id="e65e2-125">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vaste activa** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="e65e2-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e65e2-126">Selecteer het vaste activum waarvoor u posten wilt bekijken en kies vervolgens de actie **Afschrijvingsboeken**.</span><span class="sxs-lookup"><span data-stu-id="e65e2-126">Select the fixed asset that you want to view entries for, and then choose the **Depreciation Books** action.</span></span>  
3. <span data-ttu-id="e65e2-127">Selecteer het afschrijvingsboek waarvoor u posten wilt bekijken en kies vervolgens de actie **Posten**.</span><span class="sxs-lookup"><span data-stu-id="e65e2-127">Select the depreciation book that you want to view entries for, and then choose the **Ledger Entries** action.</span></span>  
4. <span data-ttu-id="e65e2-128">Selecteer een regel die de waarde **Buitengebruikstelling** in het veld **VA-boekingscategorie** bevat en kies vervolgens de actie **Navigeren**.</span><span class="sxs-lookup"><span data-stu-id="e65e2-128">Select a line with **Disposal** in the **FA Posting Category** field, and then choose the **Navigate** action.</span></span>  
5. <span data-ttu-id="e65e2-129">Selecteer op de pagina **Navigeren** de regel van de grootboekpost en klik op de actie **Weergeven**.</span><span class="sxs-lookup"><span data-stu-id="e65e2-129">On the **Navigate** page, select the general ledger entry line, and then choose the **Show** action.</span></span>  

<span data-ttu-id="e65e2-130">De pagina **Grootboekposten** wordt geopend. Op deze pagina kunt u de posten zien waarin de boeking van de buitengebruikstelling is geresulteerd.</span><span class="sxs-lookup"><span data-stu-id="e65e2-130">The **General Ledger Entries** page opens where you can see the entries that the disposal posting resulted in.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e65e2-131">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e65e2-131">See Also</span></span>

[<span data-ttu-id="e65e2-132">Vaste activa</span><span class="sxs-lookup"><span data-stu-id="e65e2-132">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="e65e2-133">Vaste activa instellen</span><span class="sxs-lookup"><span data-stu-id="e65e2-133">Setting Up Fixed Assets</span></span>](fa-setup.md)  
<span data-ttu-id="e65e2-134">[Boekingsgroepen voor vaste activa instellen](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span><span class="sxs-lookup"><span data-stu-id="e65e2-134">[To set up fixed asset posting groups](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).</span></span>  
[<span data-ttu-id="e65e2-135">Financiën</span><span class="sxs-lookup"><span data-stu-id="e65e2-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="e65e2-136">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="e65e2-136">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="e65e2-137">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e65e2-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
