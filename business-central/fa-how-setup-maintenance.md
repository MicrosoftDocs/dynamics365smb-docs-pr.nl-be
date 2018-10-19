---
title: VA-onderhoud instellen| Microsoft Docs
description: Als u reparaties en service van vaste activa wilt beheren, geeft u algemene onderhoudsinformatie, codes voor het soort werk en een boekingsrekening voor kosten op.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: aef3d672bf01425a36bdd599e18d9ee9dac73b2d
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-fixed-asset-maintenance"></a><span data-ttu-id="93bb6-103">Onderhoud van vaste activa instellen</span><span class="sxs-lookup"><span data-stu-id="93bb6-103">Set Up Fixed Asset Maintenance</span></span>
<span data-ttu-id="93bb6-104">Als u onderhoud voor vaste activa wilt beheren, moet u eerst enkele algemene onderhoudsgegevens instellen, een boekingsrekening voor onderhoudskosten en onderhoudscodes voor soorten werk, zoals periodiek onderhoud of reparatie.</span><span class="sxs-lookup"><span data-stu-id="93bb6-104">To manage fixed asset maintenance, you must first set up some general maintenance information, a posting account for maintenance costs, and maintenance codes for types of work, such as Routine Service or Repair.</span></span>

## <a name="to-set-up-general-maintenance-information"></a><span data-ttu-id="93bb6-105">Algemene onderhoudsgegevens instellen</span><span class="sxs-lookup"><span data-stu-id="93bb6-105">To set up general maintenance information</span></span>
<span data-ttu-id="93bb6-106">Als u de velden voor onderhoud instelt, kunt u onderhoudskosten boeken vanuit een dagboek voor vaste activa.</span><span class="sxs-lookup"><span data-stu-id="93bb6-106">If you set up the fields for maintenance, you can post maintenance expenses from the fixed asset journal.</span></span>

1. <span data-ttu-id="93bb6-107">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vaste activa** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="93bb6-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="93bb6-108">Selecteer het vaste activum waarvoor u verzekeringsdekking wilt definiëren en kies vervolgens de actie **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="93bb6-108">Select the fixed asset that you to define insurance coverage for, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="93bb6-109">Vul indien nodig de velden op het sneltabblad **Onderhoud** in.</span><span class="sxs-lookup"><span data-stu-id="93bb6-109">On the **Maintenance** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a><span data-ttu-id="93bb6-110">Onderhoudscodes instellen</span><span class="sxs-lookup"><span data-stu-id="93bb6-110">To set up maintenance codes</span></span>
<span data-ttu-id="93bb6-111">Als u onderhoudskosten boekt vanuit een algemeen dagboek, vult u het veld **Onderhoudscode** in om te registreren wat voor onderhoud is uitgevoerd, zoals periodiek onderhoud of reparatie.</span><span class="sxs-lookup"><span data-stu-id="93bb6-111">When you post maintenance costs from a general journal, you fill in the **Maintenance Code** field to record what kind of maintenance has been performed, such as routine service or repair.</span></span>

1. <span data-ttu-id="93bb6-112">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Onderhoud** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="93bb6-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Maintenance**, and then choose the related link.</span></span>
2. <span data-ttu-id="93bb6-113">Stel in het venster **Onderhoud** codes voor verschillende soorten onderhoudswerk in.</span><span class="sxs-lookup"><span data-stu-id="93bb6-113">In the **Maintenance** window, set up codes for different types of maintenance work.</span></span>

## <a name="to-set-up-maintenance-expense-accounts"></a><span data-ttu-id="93bb6-114">Onderhoudskostenrekeningen instellen</span><span class="sxs-lookup"><span data-stu-id="93bb6-114">To set up maintenance expense accounts</span></span>
<span data-ttu-id="93bb6-115">Als u onderhoudskosten wilt boeken, moet u eerst een rekeningnummer invoeren in het venster **VA-boekingsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="93bb6-115">To post maintenance costs, you must first enter an account number in the **FA Posting Groups** window.</span></span>

1. <span data-ttu-id="93bb6-116">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **VA-boekingsgroepen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="93bb6-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **FA Posting Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="93bb6-117">Vul voor elke boekingsgroep het veld **Onderhoudskostenrek.** in.</span><span class="sxs-lookup"><span data-stu-id="93bb6-117">Fill in the **Maintenance Expense Account** field for each posting group.</span></span>

> [!NOTE]  
>   <span data-ttu-id="93bb6-118">Als u wilt definiëren dat onderhoudskosten worden verdeeld over afdelingen of projecten, stelt u een verdeelsleutel in.</span><span class="sxs-lookup"><span data-stu-id="93bb6-118">To define that maintenance costs are allocated to departments or projects, set up an allocation keys.</span></span> <span data-ttu-id="93bb6-119">Zie [Algemene functies voor vaste activa instellen](fa-how-setup-general.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="93bb6-119">For more information, see [Set Up General Fixed Assets Features](fa-how-setup-general.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="93bb6-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="93bb6-120">See Also</span></span>
[<span data-ttu-id="93bb6-121">Vaste activa instellen</span><span class="sxs-lookup"><span data-stu-id="93bb6-121">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="93bb6-122">Vast activum</span><span class="sxs-lookup"><span data-stu-id="93bb6-122">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="93bb6-123">Financiën</span><span class="sxs-lookup"><span data-stu-id="93bb6-123">Finance</span></span>](finance.md)  
[<span data-ttu-id="93bb6-124">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="93bb6-124">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="93bb6-125">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="93bb6-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

