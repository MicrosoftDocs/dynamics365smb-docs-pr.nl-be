---
title: 'Ontwerpdetails: Dimensiecombinaties zoeken | Microsoft Docs'
description: Wanneer u een pagina sluit nadat u een dimensieset hebt bewerkt, evalueert Business Central of de bewerkte dimensieset bestaat. Als de verzameling niet bestaat, wordt een nieuwe verzameling gemaakt en wordt de dimensiecombinatie-id geretourneerd.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 544cb3a1844aaf85ab937031a23d6d00506ffa74
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215766"
---
# <a name="design-details-searching-for-dimension-combinations"></a><span data-ttu-id="6a05b-104">Ontwerpdetails: Dimensiecombinaties zoeken</span><span class="sxs-lookup"><span data-stu-id="6a05b-104">Design Details: Searching for Dimension Combinations</span></span>
<span data-ttu-id="6a05b-105">Wanneer u een pagina sluit nadat u een dimensieset hebt bewerkt, evalueert [!INCLUDE[prod_short](includes/prod_short.md)] of de bewerkte dimensieset bestaat.</span><span class="sxs-lookup"><span data-stu-id="6a05b-105">When you close a page after you edit a set of dimensions, [!INCLUDE[prod_short](includes/prod_short.md)] evaluates whether the edited set of dimensions exists.</span></span> <span data-ttu-id="6a05b-106">Als de verzameling niet bestaat, wordt een nieuwe verzameling gemaakt en wordt de dimensiecombinatie-id geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="6a05b-106">If the set does not exist, a new set is created and the dimension combination ID is returned.</span></span>  

## <a name="building-search-tree"></a><span data-ttu-id="6a05b-107">Zoekactiestructuur opzetten</span><span class="sxs-lookup"><span data-stu-id="6a05b-107">Building Search Tree</span></span>  
 <span data-ttu-id="6a05b-108">Tabel 481 **Boomstructuurpunt dimensieset** wordt gebruikt wanneer [!INCLUDE[prod_short](includes/prod_short.md)] evalueert of een set dimensies al bestaat in tabel 480 **Dimensiesetpost**.</span><span class="sxs-lookup"><span data-stu-id="6a05b-108">Table 481 **Dimension Set Tree Node** is used when [!INCLUDE[prod_short](includes/prod_short.md)] evaluates whether a set of dimensions already exists in table 480 **Dimension Set Entry** table.</span></span> <span data-ttu-id="6a05b-109">De evaluatie wordt uitgevoerd doordat de zoekstructuur recursief wordt doorlopen vanaf het hoogste niveau met nummer 0.</span><span class="sxs-lookup"><span data-stu-id="6a05b-109">The evaluation is performed by recursively traversing the search tree starting at the top level numbered 0.</span></span> <span data-ttu-id="6a05b-110">Hoogste niveau 0 staat voor een dimensieset zonder dimensiesetposten.</span><span class="sxs-lookup"><span data-stu-id="6a05b-110">The top level 0 represents a dimension set with no dimension set entries.</span></span> <span data-ttu-id="6a05b-111">De onderliggende elementen van deze dimensieset vertegenwoordigen dimensiesets met slechts één dimensiesetpost.</span><span class="sxs-lookup"><span data-stu-id="6a05b-111">The children of this dimension set represent dimension sets with only one dimension set entry.</span></span> <span data-ttu-id="6a05b-112">De onderliggende elementen van deze dimensiesets vertegenwoordigen dimensiesets met twee onderliggende elementen, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="6a05b-112">The children of these dimension sets represent dimension sets with two children, and so on.</span></span>  

### <a name="example-1"></a><span data-ttu-id="6a05b-113">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="6a05b-113">Example 1</span></span>  
 <span data-ttu-id="6a05b-114">Het volgende diagram vertegenwoordigt een zoekactiestructuur met zes dimensiesets.</span><span class="sxs-lookup"><span data-stu-id="6a05b-114">The following diagram represents a search tree with six dimension sets.</span></span> <span data-ttu-id="6a05b-115">Alleen de onderscheidende dimensiesetpost wordt weergegeven in het diagram.</span><span class="sxs-lookup"><span data-stu-id="6a05b-115">Only the distinguishing dimension set entry is displayed in the diagram.</span></span>  

 <span data-ttu-id="6a05b-116">![Voorbeeld van een dimensieboomstructuur](media/nav2013_dimension_tree.png "Voorbeeld van een dimensieboomstructuur")</span><span class="sxs-lookup"><span data-stu-id="6a05b-116">![Example of dimension tree structure](media/nav2013_dimension_tree.png "Example of dimension tree structure")</span></span>  

 <span data-ttu-id="6a05b-117">In de volgende tabel wordt een volledig overzicht beschreven van dimensiesetposten waaruit elke dimensieset bestaan.</span><span class="sxs-lookup"><span data-stu-id="6a05b-117">The following table describes a complete list of dimension set entries that make up each dimension set.</span></span>  

|<span data-ttu-id="6a05b-118">Dimensiesets</span><span class="sxs-lookup"><span data-stu-id="6a05b-118">Dimension Sets</span></span>|<span data-ttu-id="6a05b-119">Dimensiesetposten</span><span class="sxs-lookup"><span data-stu-id="6a05b-119">Dimension Set Entries</span></span>|  
|--------------------|---------------------------|  
|<span data-ttu-id="6a05b-120">Set 0</span><span class="sxs-lookup"><span data-stu-id="6a05b-120">Set 0</span></span>|<span data-ttu-id="6a05b-121">Geen</span><span class="sxs-lookup"><span data-stu-id="6a05b-121">None</span></span>|  
|<span data-ttu-id="6a05b-122">Set 1</span><span class="sxs-lookup"><span data-stu-id="6a05b-122">Set 1</span></span>|<span data-ttu-id="6a05b-123">AREA 30</span><span class="sxs-lookup"><span data-stu-id="6a05b-123">AREA 30</span></span>|  
|<span data-ttu-id="6a05b-124">Set 2</span><span class="sxs-lookup"><span data-stu-id="6a05b-124">Set 2</span></span>|<span data-ttu-id="6a05b-125">AREA 30, DEPT ADM</span><span class="sxs-lookup"><span data-stu-id="6a05b-125">AREA 30, DEPT ADM</span></span>|  
|<span data-ttu-id="6a05b-126">Set 3</span><span class="sxs-lookup"><span data-stu-id="6a05b-126">Set 3</span></span>|<span data-ttu-id="6a05b-127">AREA 30, DEPT PROD</span><span class="sxs-lookup"><span data-stu-id="6a05b-127">AREA 30, DEPT PROD</span></span>|  
|<span data-ttu-id="6a05b-128">Set 4</span><span class="sxs-lookup"><span data-stu-id="6a05b-128">Set 4</span></span>|<span data-ttu-id="6a05b-129">AREA 30, DEPT ADM, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="6a05b-129">AREA 30, DEPT ADM, PROJ VW</span></span>|  
|<span data-ttu-id="6a05b-130">Set 5</span><span class="sxs-lookup"><span data-stu-id="6a05b-130">Set 5</span></span>|<span data-ttu-id="6a05b-131">AREA 40</span><span class="sxs-lookup"><span data-stu-id="6a05b-131">AREA 40</span></span>|  
|<span data-ttu-id="6a05b-132">Set 6</span><span class="sxs-lookup"><span data-stu-id="6a05b-132">Set 6</span></span>|<span data-ttu-id="6a05b-133">AREA 40, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="6a05b-133">AREA 40, PROJ VW</span></span>|  

### <a name="example-2"></a><span data-ttu-id="6a05b-134">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="6a05b-134">Example 2</span></span>  
 <span data-ttu-id="6a05b-135">Dit voorbeeld geeft aan hoe [!INCLUDE[prod_short](includes/prod_short.md)] evalueert of een dimensieset die bestaat uit de dimensiesetposten AREA 40, DEPT PROD bestaat.</span><span class="sxs-lookup"><span data-stu-id="6a05b-135">This example shows how [!INCLUDE[prod_short](includes/prod_short.md)] evaluates whether a dimension set that consists of the dimension set entries AREA 40, DEPT PROD exists.</span></span>  

 <span data-ttu-id="6a05b-136">Eerst werkt [!INCLUDE[prod_short](includes/prod_short.md)] ook de tabel **Boomstructuurpunt dimensieset** bij om ervoor te zorgen dat de zoekstructuur lijkt op het volgende diagram.</span><span class="sxs-lookup"><span data-stu-id="6a05b-136">First, [!INCLUDE[prod_short](includes/prod_short.md)] also updates the **Dimension Set Tree Node** table to make sure that the search tree looks like the following diagram.</span></span> <span data-ttu-id="6a05b-137">Zodoende wordt dimensieset 7 een onderliggend niveau van dimensieset 5.</span><span class="sxs-lookup"><span data-stu-id="6a05b-137">Thus dimension set 7 becomes a child of the dimension set 5.</span></span>  

 <span data-ttu-id="6a05b-138">![Voorbeeld van een dimensieboomstructuur in NAV 2013](media/nav2013_dimension_tree_example2.png "Voorbeeld van een dimensieboomstructuur in NAV 2013")</span><span class="sxs-lookup"><span data-stu-id="6a05b-138">![Example of dimension tree structure in NAV 2013](media/nav2013_dimension_tree_example2.png "Example of dimension tree structure in NAV 2013")</span></span>  

### <a name="finding-dimension-set-id"></a><span data-ttu-id="6a05b-139">Dimensieset-id zoeken</span><span class="sxs-lookup"><span data-stu-id="6a05b-139">Finding Dimension Set ID</span></span>  
 <span data-ttu-id="6a05b-140">Op conceptueel niveau zijn **Hoofd-id**, **Dimensie** en **Dimensiewaarde** in de zoekstructuur gecombineerd en gebruikt als de primaire sleutel omdat [!INCLUDE[prod_short](includes/prod_short.md)] de structuur doorloopt in dezelfde volgorde als de dimensieposten.</span><span class="sxs-lookup"><span data-stu-id="6a05b-140">At a conceptual level, **Parent ID**, **Dimension**, and **Dimension Value**, in the search tree, are combined and used as the primary key because [!INCLUDE[prod_short](includes/prod_short.md)] traverses the tree in the same order as the dimension entries.</span></span> <span data-ttu-id="6a05b-141">De functie GET (record) wordt gebruikt om te zoeken naar dimensieset-id.</span><span class="sxs-lookup"><span data-stu-id="6a05b-141">The GET function (record) is used to search for dimension set ID.</span></span> <span data-ttu-id="6a05b-142">In het volgende codevoorbeeld wordt aangegeven hoe u de dimensieset-id kunt vinden als er drie dimensiewaarden zijn.</span><span class="sxs-lookup"><span data-stu-id="6a05b-142">The following code example shows how to find the dimension set ID when there are three dimension values.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

<span data-ttu-id="6a05b-143">Om het vermogen van [!INCLUDE[prod_short](includes/prod_short.md)] te behouden om zowel een dimensie als dimensiewaarde te kunnen hernoemen wordt tabel 349 **Dimensiewaarde** uitgebreid met een geheelgetalveld genaamd **Dimensiewaarde-id**.</span><span class="sxs-lookup"><span data-stu-id="6a05b-143">However, to preserve the ability of [!INCLUDE[prod_short](includes/prod_short.md)] to rename both a dimension and a dimension value, table 349, **Dimension Value**, is extended with an integer field, **Dimension Value ID**.</span></span> <span data-ttu-id="6a05b-144">In deze tabel wordt het veldpaar **Dimensie** en **Dimensiewaarde** omgezet in een geheel getal.</span><span class="sxs-lookup"><span data-stu-id="6a05b-144">This table converts the field pair, **Dimension** and **Dimension Value**, to an integer value.</span></span> <span data-ttu-id="6a05b-145">Wanneer u de naam van de dimensie en dimensiewaarde wijzigt, wordt de waarde voor het gehele getal niet gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="6a05b-145">When you rename the dimension and dimension value, the integer value is not changed.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a><span data-ttu-id="6a05b-146">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6a05b-146">See Also</span></span>
    
 <span data-ttu-id="6a05b-147">[Ontwerpdetails: Dimensiesetposten](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="6a05b-147">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="6a05b-148">[Dimensiesetposten - overzicht](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="6a05b-148">[Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 [<span data-ttu-id="6a05b-149">Ontwerpdetails: Tabelstructuur</span><span class="sxs-lookup"><span data-stu-id="6a05b-149">Design Details: Table Structure</span></span>](design-details-table-structure.md)   
 


[!INCLUDE[footer-include](includes/footer-banner.md)]
