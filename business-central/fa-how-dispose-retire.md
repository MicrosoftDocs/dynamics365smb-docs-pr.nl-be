---
title: Activa afstoten of van de hand doen| Microsoft Docs
description: U moet een buitengebruikstellingwaarde boeken wanneer u een vast activum laat uitvallen, verkoopt of buiten gebruik stelt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 10e7939378d222e2e2f915c89f820e000615ac1e
ms.contentlocale: nl-be
ms.lasthandoff: 11/26/2018

---
# <a name="dispose-of-or-retire-fixed-assets"></a><span data-ttu-id="3a513-103">Vaste activa afstoten of van de hand doen</span><span class="sxs-lookup"><span data-stu-id="3a513-103">Dispose of or Retire Fixed Assets</span></span>
<span data-ttu-id="3a513-104">Als u een vast activum verkoopt of anderszins buiten gebruik stelt, moet u de buitengebruikstellingswaarde boeken om de winst of het verlies te berekenen en te registreren.</span><span class="sxs-lookup"><span data-stu-id="3a513-104">When you sell or otherwise dispose of a fixed asset, the disposal value must be posted to calculate and record the gain or loss.</span></span> <span data-ttu-id="3a513-105">Een buitengebruikstellingspost is de laatste post die voor een vast activum wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="3a513-105">A disposal entry must be the last entry posted for a fixed asset.</span></span> <span data-ttu-id="3a513-106">Voor vaste activa die gedeeltelijk buiten gebruik zijn gesteld, kunt u meerdere buitengebruikstellingsposten boeken.</span><span class="sxs-lookup"><span data-stu-id="3a513-106">For partially disposed fixed assets, you can post more than one disposal entry.</span></span> <span data-ttu-id="3a513-107">Het totaal van alle geboekte buitengebruikstellingsbedragen moet een creditbedrag zijn.</span><span class="sxs-lookup"><span data-stu-id="3a513-107">The total of all posted disposal amounts must be a credit amount.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="3a513-108">Als u een vast activum inruilt, moet u zowel de verkoop van het oude activum (buitengebruikstelling) als de aankoop van het nieuwe activum (aanschaf) registreren.</span><span class="sxs-lookup"><span data-stu-id="3a513-108">If you trade-in a fixed asset for another one, you must record both the sale of the old asset (disposal) and the purchase of the new one (acquisition).</span></span> <span data-ttu-id="3a513-109">Zie [Vaste activa aanschaffen](fa-how-acquire.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="3a513-109">For more information, see [Acquire Fixed Assets](fa-how-acquire.md).</span></span>  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a><span data-ttu-id="3a513-110">Een buitengebruikstelling boeken vanuit het financieel dagboek voor vaste activa</span><span class="sxs-lookup"><span data-stu-id="3a513-110">To post a disposal from the fixed asset G/L journal</span></span>
1. <span data-ttu-id="3a513-111">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **VA-fin. dagboeken** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="3a513-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3a513-112">Maak een eerste dagboekregel en vul de velden indien nodig in.</span><span class="sxs-lookup"><span data-stu-id="3a513-112">Create an initial journal line and fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. <span data-ttu-id="3a513-113">In het veld **VA-boekingssoort** selecteert u **Buitengebruikstelling**.</span><span class="sxs-lookup"><span data-stu-id="3a513-113">In the **FA Posting Type** field, select **Disposal**.</span></span>  
4. <span data-ttu-id="3a513-114">Kies de actie **VA-tegenrekening invoegen**.</span><span class="sxs-lookup"><span data-stu-id="3a513-114">Choose the **Insert FA Bal. Account** action.</span></span> <span data-ttu-id="3a513-115">Er wordt een tweede dagboekregel gemaakt voor de tegenrekening die voor de boeking van de buitengebruikstelling is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="3a513-115">A second journal line is created for the balancing account that is set up for disposal posting.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="3a513-116">Stap 4 werkt alleen als u het volgende hebt ingesteld: op de pagina **VA-boekingsgroep** voor de boekingsgroep van het vaste activum bevat het veld **Buitengebruikstellingsrekening** de grootboekdebetrekening en het veld **Tegenrekening buitengebruikstelling** bevat de grootboekrekening waarnaar u tegenrekeningsposten voor buitengebruikstelling wilt boeken.</span><span class="sxs-lookup"><span data-stu-id="3a513-116">Step 4 only works if you have set up the following: On the **FA Posting Group Card** page for the posting group of the fixed asset, the **Disposal Account** field contains the general ledger debit account and the **Disposal Bal. Account** field contains the general ledger account to which you want to post balancing entries for appreciation.</span></span> <span data-ttu-id="3a513-117">Zie het gedeelte 'Boekingsgroepen voor vaste activa instellen' in [Algemene gegevens voor vaste activa instellen](fa-how-setup-general.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="3a513-117">For more information, see the "To set up fixed asset posting groups" section in [Set Up General Fixed Asset Information](fa-how-setup-general.md).</span></span>  
5. <span data-ttu-id="3a513-118">Kies de actie **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="3a513-118">Choose the **Post** action.</span></span>  

<span data-ttu-id="3a513-119">Als u een gedeelte van een vast activum verkoopt of het niet langer meer gebruikt, moet u het activum opsplitsen voordat u de buitengebruikstellingstransactie kunt vastleggen.</span><span class="sxs-lookup"><span data-stu-id="3a513-119">If you sell or dispose of part of a fixed asset, you must split up the asset before you can record the disposal transaction.</span></span> <span data-ttu-id="3a513-120">Zie [Vaste activa overbrengen, splitsen of combineren](fa-how-trans-split-combine.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="3a513-120">For more information, see [Transfer, Split, or Combine Fixed Assets](fa-how-trans-split-combine.md).</span></span>  

## <a name="to-view-disposal-ledger-entries"></a><span data-ttu-id="3a513-121">Buitengebruikstellingsposten bekijken</span><span class="sxs-lookup"><span data-stu-id="3a513-121">To view disposal ledger entries</span></span>
<span data-ttu-id="3a513-122">Als u een vast activum verkoopt of buiten gebruik stelt, moet u de buitengebruikstellingswaarde boeken naar het grootboek waar u het resultaat kunt bekijken.</span><span class="sxs-lookup"><span data-stu-id="3a513-122">When you sell or dispose of a fixed asset, the disposal value is posted to the general ledger where you can view the result.</span></span>  

1. <span data-ttu-id="3a513-123">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vaste activa** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="3a513-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3a513-124">Selecteer het vaste activum waarvoor u posten wilt bekijken en kies vervolgens de actie **Afschrijvingsboeken**.</span><span class="sxs-lookup"><span data-stu-id="3a513-124">Select the fixed asset that you want to view entries for, and then choose the **Depreciation Books** action.</span></span>  
3. <span data-ttu-id="3a513-125">Selecteer het afschrijvingsboek waarvoor u posten wilt bekijken en kies vervolgens de actie **Posten**.</span><span class="sxs-lookup"><span data-stu-id="3a513-125">Select the depreciation book that you want to view entries for, and then choose the **Ledger Entries** action.</span></span>  
4. <span data-ttu-id="3a513-126">Selecteer een regel die de waarde **Buitengebruikstelling** in het veld **VA-boekingscategorie** bevat en kies vervolgens de actie **Navigeren**.</span><span class="sxs-lookup"><span data-stu-id="3a513-126">Select a line with **Disposal** in the **FA Posting Category** field, and then choose the **Navigate** action.</span></span>  
5. <span data-ttu-id="3a513-127">Selecteer op de pagina **Navigeren** de regel van de grootboekpost en klik op de actie **Weergeven**.</span><span class="sxs-lookup"><span data-stu-id="3a513-127">On the **Navigate** page, select the general ledger entry line, and then choose the **Show** action.</span></span>  

<span data-ttu-id="3a513-128">De pagina **Grootboekposten** wordt geopend. Op deze pagina kunt u de posten zien waarin de boeking van de buitengebruikstelling is geresulteerd.</span><span class="sxs-lookup"><span data-stu-id="3a513-128">The **General Ledger Entries** page opens where you can see the entries that the disposal posting resulted in.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3a513-129">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3a513-129">See Also</span></span>
[<span data-ttu-id="3a513-130">Vast activum</span><span class="sxs-lookup"><span data-stu-id="3a513-130">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="3a513-131">Vaste activa instellen</span><span class="sxs-lookup"><span data-stu-id="3a513-131">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="3a513-132">Financiën</span><span class="sxs-lookup"><span data-stu-id="3a513-132">Finance</span></span>](finance.md)  
[<span data-ttu-id="3a513-133">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="3a513-133">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="3a513-134">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3a513-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

