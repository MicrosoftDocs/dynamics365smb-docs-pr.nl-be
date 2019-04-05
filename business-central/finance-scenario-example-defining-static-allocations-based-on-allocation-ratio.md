---
title: Statische toewijzingen op basis van de verdeelsleutel definiëren | Microsoft Docs
description: De methode voor statische toewijzingen baseert zich op een vaste waarde voor bijvoorbeeld gebruikte vierkante meters of een vastgestelde verdeelsleutel, zoals 5:2:4.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: d35fd5de7a0583c3864268d0749384322bf947ed
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "817083"
---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a><span data-ttu-id="34af7-103">Voorbeeld scenario: statische toewijzingen op basis van de verdeelsleutel definiëren</span><span class="sxs-lookup"><span data-stu-id="34af7-103">Scenario Example: Defining Static Allocations Based on Allocation Ratio</span></span>
<span data-ttu-id="34af7-104">De methode voor statische toewijzingen baseert zich op een vaste waarde voor bijvoorbeeld gebruikte vierkante meters of een vastgestelde verdeelsleutel, zoals 5:2:4.</span><span class="sxs-lookup"><span data-stu-id="34af7-104">Static allocation method is based on a definite value, such as square meters used, or an established allocation ratio such as 5:2:4.</span></span>  

<span data-ttu-id="34af7-105">In dit onderwerp wordt beschreven hoe u drie nieuwe verdeeldoelen voor kostenobjecten kunt definiëren voor de verdelingsbron van kostenplaats PROD met behulp van de vastgestelde verdeelsleutel 5: 2: 4.</span><span class="sxs-lookup"><span data-stu-id="34af7-105">This topic describes how to define three new allocation target cost objects for the allocation source PROD cost center using the established allocation ratio 5:2:4.</span></span> <span data-ttu-id="34af7-106">De drie doelkostenobjecten zijn ACCESSO, VERF en TOEBEHOREN.</span><span class="sxs-lookup"><span data-stu-id="34af7-106">The three target cost objects are ACCESSO, PAINT, and FITTINGS.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="34af7-107">In het voorbeeld worden de demogegevens in de [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruikt.</span><span class="sxs-lookup"><span data-stu-id="34af7-107">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a><span data-ttu-id="34af7-108">De verdelingsbron van kostenplaats PROD op het sneltabblad Algemeen definiëren</span><span class="sxs-lookup"><span data-stu-id="34af7-108">To define the allocation source PROD cost center on the General FastTab</span></span>  

1.  <span data-ttu-id="34af7-109">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Kostenverdeling** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="34af7-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Allocation**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="34af7-110">Kies op de pagina **Kostenverdeling** de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="34af7-110">On the **Cost Allocation** page, choose the **New** action.</span></span>  
3.  <span data-ttu-id="34af7-111">Druk in het veld **ID** op Enter of voer een id in.</span><span class="sxs-lookup"><span data-stu-id="34af7-111">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="34af7-112">Geef **1** op in het veld **Niveau**.</span><span class="sxs-lookup"><span data-stu-id="34af7-112">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="34af7-113">Voer in de velden **Geldig vanaf** en **Geldig tot** juiste datums in.</span><span class="sxs-lookup"><span data-stu-id="34af7-113">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="34af7-114">Voer in het veld **Kostenplaatscode** **PROD** in.</span><span class="sxs-lookup"><span data-stu-id="34af7-114">In the **Cost Center Code** field, enter **PROD**.</span></span>  
7.  <span data-ttu-id="34af7-115">Voer in het veld **Credit naar kostensoort** het kostensoort **9903** in.</span><span class="sxs-lookup"><span data-stu-id="34af7-115">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a><span data-ttu-id="34af7-116">Verdeeldoelen voor kostenobjecten op de sneltabblad Regels definiëren</span><span class="sxs-lookup"><span data-stu-id="34af7-116">To define the allocation target cost objects on the Lines FastTab</span></span>  

1.  <span data-ttu-id="34af7-117">Voer op de eerste regel in het veld **Doelkostensoort** **9903** in.</span><span class="sxs-lookup"><span data-stu-id="34af7-117">On the first line, in the **Target Cost Type** field, enter **9903**.</span></span>  
2.  <span data-ttu-id="34af7-118">Selecteer op de eerste regel in het veld **Doelkostenobject** **ACCESSO**.</span><span class="sxs-lookup"><span data-stu-id="34af7-118">On the first line, in the **Target Cost Object** field, select **ACCESSO**.</span></span>  
3.  <span data-ttu-id="34af7-119">Selecteer op de eerste regel in het veld **Verdelingsdoelsoort** de optie **Alle kosten** om te definiëren hoe te betalen kosten moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="34af7-119">On the first line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
4.  <span data-ttu-id="34af7-120">Op de eerste regel in het veld **Basis** selecteert u **Statisch** om de statische toewijzingsmethode te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="34af7-120">On the first line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
5.  <span data-ttu-id="34af7-121">Op de eerste regel in het veld **Deel** voert u de verdeelsleutel **5** in.</span><span class="sxs-lookup"><span data-stu-id="34af7-121">On the first line, in the **Share** field, enter the allocation ratio **5**.</span></span>  
6.  <span data-ttu-id="34af7-122">Voer op de tweede regel in het veld **Doelkostensoort** **9903** in.</span><span class="sxs-lookup"><span data-stu-id="34af7-122">On the second line, in the **Target Cost Type** field, enter **9903**.</span></span>  
7.  <span data-ttu-id="34af7-123">Selecteer op de tweede regel in het veld **Doelkostenobject** **PAINT**.</span><span class="sxs-lookup"><span data-stu-id="34af7-123">On the second line, in the **Target Cost Object** field, select **PAINT**.</span></span>  
8.  <span data-ttu-id="34af7-124">Selecteer op de tweede regel in het veld **Verdelingsdoelsoort** de optie **Alle kosten** om te definiëren hoe te betalen kosten moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="34af7-124">On the second line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
9. <span data-ttu-id="34af7-125">Op de tweede regel in het veld **Basis** selecteert u **Statisch** om de statische toewijzingsmethode te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="34af7-125">On the second line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
10. <span data-ttu-id="34af7-126">Op de tweede regel in het veld **Deel** voert u de verdeelsleutel **2** in.</span><span class="sxs-lookup"><span data-stu-id="34af7-126">On the second line, in the **Share** field, enter the allocation ratio **2**.</span></span>  
11. <span data-ttu-id="34af7-127">Voer op de derde regel in het veld **Doelkostensoort** **9903** in.</span><span class="sxs-lookup"><span data-stu-id="34af7-127">On the third line, in the **Target Cost Type** field, enter **9903**.</span></span>  
12. <span data-ttu-id="34af7-128">Selecteer op de derde regel in het veld **Doelkostenobject** **FITTINGS**.</span><span class="sxs-lookup"><span data-stu-id="34af7-128">On the third line, in the **Target Cost Object** field, select **FITTINGS**.</span></span>  
13. <span data-ttu-id="34af7-129">Selecteer op de derde regel in het veld **Verdelingsdoelsoort** de optie **Alle kosten** om te definiëren hoe te betalen kosten moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="34af7-129">On the third line, in the **Allocation Target Type** field, select **All Costs** to define how all accrued costs are allocated.</span></span>  
14. <span data-ttu-id="34af7-130">Op de derde regel in het veld **Basis** selecteert u **Statisch** om de statische toewijzingsmethode te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="34af7-130">On the third line, in the **Base** field, select **Static** to use the static allocation method.</span></span>  
15. <span data-ttu-id="34af7-131">Op de derde regel in het veld **Deel** voert u de verdeelsleutel **4** in.</span><span class="sxs-lookup"><span data-stu-id="34af7-131">On the third line, in the **Share** field, enter the allocation ratio **4**.</span></span>  

> [!IMPORTANT]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="34af7-132">berekent automatisch het veld **Percentage** met een percentage dat wordt bepaald door alle drie de verdeelsleutels die zijn ingevoerd in het veld **Deel** voor alle drie de regels.</span><span class="sxs-lookup"><span data-stu-id="34af7-132">automatically calculates the **Percent** field using a percentage rate that is dependent on all three allocation ratios that are entered in the **Share** field for all three lines.</span></span>  

## <a name="see-also"></a><span data-ttu-id="34af7-133">Zie ook</span><span class="sxs-lookup"><span data-stu-id="34af7-133">See Also</span></span>  
[<span data-ttu-id="34af7-134">Kosten definiëren en toewijzen</span><span class="sxs-lookup"><span data-stu-id="34af7-134">Defining and Allocating Costs</span></span>](finance-define-and-allocate-costs.md)   
