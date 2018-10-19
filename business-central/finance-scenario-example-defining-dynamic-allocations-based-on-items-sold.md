---
title: "Voorbeeldscenario: Dynamische toewijzingen op basis van de verkochte artikelen definiëren | Microsoft Docs"
description: "Dit onderwerp bevat een voorbeeld van het definiëren van toewijzingen met behulp van de methode voor dynamische toewijzing."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 85d58264b14d191389bdf23a792dff7ad30bf9c3
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a><span data-ttu-id="537be-103">Voorbeeld scenario: dynamische toewijzingen op basis van de verkochte artikelen definiëren</span><span class="sxs-lookup"><span data-stu-id="537be-103">Scenario Example: Defining Dynamic Allocations Based on Items Sold</span></span>
<span data-ttu-id="537be-104">Dit onderwerp bevat een voorbeeld van het definiëren van toewijzingen met behulp van de methode voor dynamische toewijzing.</span><span class="sxs-lookup"><span data-stu-id="537be-104">This topic shows an example of how to define allocations by using the dynamic allocation method.</span></span> <span data-ttu-id="537be-105">In het voorbeeld wijzigt u de dynamische toewijzing van de kosten voor kostenplaats VERKOOP ter ondersteuning van het nieuwe kostenobject IT-APPARATUUR.</span><span class="sxs-lookup"><span data-stu-id="537be-105">In the example, you change the dynamic allocation of the costs for the SALES cost center to support the new cost object IT EQUIPMENT.</span></span> <span data-ttu-id="537be-106">Pakketten voor IT-APPARATUUR hebben artikelnummers in het bereik van 8904-W t/m 8924-W.</span><span class="sxs-lookup"><span data-stu-id="537be-106">IT EQUIPMENT packages have item numbers in the range from 8904-W to 8924-W.</span></span> <span data-ttu-id="537be-107">De verkoopcijfers van het vorige jaar kunt u gebruiken om het aandeel te berekenen.</span><span class="sxs-lookup"><span data-stu-id="537be-107">You use the previous year’s sales figures to calculate the share.</span></span> <span data-ttu-id="537be-108">De toewijzing wordt geboekt op het ondersteunende kostensoort 9903.</span><span class="sxs-lookup"><span data-stu-id="537be-108">The allocation is posted to the helping cost type 9903.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="537be-109">In het voorbeeld worden de demogegevens in de [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruikt.</span><span class="sxs-lookup"><span data-stu-id="537be-109">The example uses the demo data in the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a><span data-ttu-id="537be-110">Dynamische toewijzingen definiëren op basis van artikelen die het vorige jaar zijn verkocht</span><span class="sxs-lookup"><span data-stu-id="537be-110">To define dynamic allocations based on items sold in the previous year</span></span>  

1.  <span data-ttu-id="537be-111">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Kostenverdelingen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="537be-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Allocations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="537be-112">Kies in het venster **Kostenverdeling** de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="537be-112">In the **Cost Allocation** window, choose the **New** action.</span></span>  
3.  <span data-ttu-id="537be-113">Druk in het veld **ID** op Enter of voer een id in.</span><span class="sxs-lookup"><span data-stu-id="537be-113">In the **ID** field, press Enter or enter an ID.</span></span>  
4.  <span data-ttu-id="537be-114">Geef **1** op in het veld **Niveau**.</span><span class="sxs-lookup"><span data-stu-id="537be-114">In the **Level** field, enter **1**.</span></span>  
5.  <span data-ttu-id="537be-115">Voer in de velden **Geldig vanaf** en **Geldig tot** juiste datums in.</span><span class="sxs-lookup"><span data-stu-id="537be-115">In the **Valid From** and **Valid To** fields, enter appropriate dates.</span></span>  
6.  <span data-ttu-id="537be-116">Voer in het veld **Kostenplaatscode** **SALES** in.</span><span class="sxs-lookup"><span data-stu-id="537be-116">In the **Cost Center Code** field, enter **SALES**.</span></span>  
7.  <span data-ttu-id="537be-117">Voer in het veld **Credit naar kostensoort** het kostensoort **9903** in.</span><span class="sxs-lookup"><span data-stu-id="537be-117">In the **Credit to Cost Type** field, enter the cost type **9903**.</span></span>  
8.  <span data-ttu-id="537be-118">Voer in het veld **Doelkostensoort** het kostensoort **9903** in.</span><span class="sxs-lookup"><span data-stu-id="537be-118">In the **Target Cost Type** field, enter the cost type **9903**.</span></span>  
9. <span data-ttu-id="537be-119">Kies in het veld **Doelkostenobject** de optie **Nieuw** om een nieuw kostenobject IT-APPARATUUR te maken en vul waar nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="537be-119">In the **Target Cost Object** field, choose **New** to create a new cost object IT EQUIPMENT and fill in fields as necessary.</span></span> <span data-ttu-id="537be-120">Selecteer **IT-APPARATUUR**.</span><span class="sxs-lookup"><span data-stu-id="537be-120">Select **IT EQUIPMENT**.</span></span> <span data-ttu-id="537be-121">Laat het veld **Doelkostenplaats** leeg.</span><span class="sxs-lookup"><span data-stu-id="537be-121">Leave the **Target Cost Center** field blank.</span></span>  
10. <span data-ttu-id="537be-122">Selecteer in het veld **Verdelingsdoelsoort** de optie **Alle kosten** om te definiëren hoe alle gecumuleerde kosten moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="537be-122">In the **Allocation Target Type** field, select **All Costs** to define how all accumulated costs are allocated.</span></span>  
11. <span data-ttu-id="537be-123">In het veld **Basis** selecteert u de toewijzingsbasis **Artikelen verkocht (bedrag)**.</span><span class="sxs-lookup"><span data-stu-id="537be-123">In the **Base** field, select the allocation base **Items Sold (Amount)**.</span></span>  
12. <span data-ttu-id="537be-124">Voer in het veld **Nr.-filter** **8904-W..8924-W** in.</span><span class="sxs-lookup"><span data-stu-id="537be-124">In the **No. Filter** field, enter **8904-W..8924-W**.</span></span>  
13. <span data-ttu-id="537be-125">Voer in het veld **Datumfiltercode** **Vorig jaar** in.</span><span class="sxs-lookup"><span data-stu-id="537be-125">In the **Date Filter Code** field, enter **Last Year**.</span></span>  
14. <span data-ttu-id="537be-126">Kies de actie **Verdeelsleutel berekenen** om het aandeel te berekenen.</span><span class="sxs-lookup"><span data-stu-id="537be-126">Choose the **Calculate Allocation Key** action to calculate the share.</span></span>  

    > [!IMPORTANT]  
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="537be-127">gebruikt de verkoopcijfers van de voorgaande jaren voor het berekenen van een aandeel van 1596,50 LV met 100 procent voor de pakketten voor IT-APPARATUUR.</span><span class="sxs-lookup"><span data-stu-id="537be-127">uses the previous years’ sales figures to calculate a share of 1596.50 LCY with 100 percent for the IT EQUIPMENT packages.</span></span> <span data-ttu-id="537be-128">Dit betekent dat alle artikelen die vorig jaar zijn verkocht, worden toegewezen aan kostenobject IT-APPARATUUR.</span><span class="sxs-lookup"><span data-stu-id="537be-128">This means that all of the items sold last year will be allocated to the cost object IT EQUIPMENT.</span></span>  

## <a name="see-also"></a><span data-ttu-id="537be-129">Zie ook</span><span class="sxs-lookup"><span data-stu-id="537be-129">See Also</span></span>  
 <span data-ttu-id="537be-130">[Filters instellen voor dynamische toewijzingsgrondslagen](finance-setting-filters-for-dynamic-allocation-bases.md) </span><span class="sxs-lookup"><span data-stu-id="537be-130">[Setting Filters for Dynamic Allocation Bases](finance-setting-filters-for-dynamic-allocation-bases.md) </span></span>  
 <span data-ttu-id="537be-131">[Een verdelingsbron en de doelen ervoor instellen](finance-how-to-set-up-allocation-source-and-targets.md) </span><span class="sxs-lookup"><span data-stu-id="537be-131">[Set Up Allocation Source and Targets](finance-how-to-set-up-allocation-source-and-targets.md) </span></span>  
 <span data-ttu-id="537be-132">[Kosten definiëren en toewijzen](finance-define-and-allocate-costs.md) </span><span class="sxs-lookup"><span data-stu-id="537be-132">[Defining and Allocating Costs](finance-define-and-allocate-costs.md) </span></span>  
 <span data-ttu-id="537be-133">[Terminologie in kostprijsboekhouding](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="537be-133">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
 [<span data-ttu-id="537be-134">Kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="537be-134">About Cost Accounting</span></span>](finance-about-cost-accounting.md)

