---
title: 'Ontwerpdetails: Dimensiecombinaties zoeken | Microsoft Docs'
description: Wanneer u een pagina sluit nadat u een dimensieset hebt bewerkt, evalueert Business Central of de bewerkte dimensieset bestaat. Als de verzameling niet bestaat, wordt een nieuwe verzameling gemaakt en wordt de dimensiecombinatie-id geretourneerd.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c3867c45f659f054a3bdee1605f2d8541e72dec1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751142"
---
# <a name="design-details-searching-for-dimension-combinations"></a><span data-ttu-id="30c18-104">Ontwerpdetails: Dimensiecombinaties zoeken</span><span class="sxs-lookup"><span data-stu-id="30c18-104">Design Details: Searching for Dimension Combinations</span></span>
<span data-ttu-id="30c18-105">Wanneer u een pagina sluit nadat u een dimensieset hebt bewerkt, evalueert [!INCLUDE[prod_short](includes/prod_short.md)] of de bewerkte dimensieset bestaat.</span><span class="sxs-lookup"><span data-stu-id="30c18-105">When you close a page after you edit a set of dimensions, [!INCLUDE[prod_short](includes/prod_short.md)] evaluates whether the edited set of dimensions exists.</span></span> <span data-ttu-id="30c18-106">Als de verzameling niet bestaat, wordt een nieuwe verzameling gemaakt en wordt de dimensiecombinatie-id geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="30c18-106">If the set does not exist, a new set is created and the dimension combination ID is returned.</span></span>  

## <a name="building-search-tree"></a><span data-ttu-id="30c18-107">Zoekactiestructuur opzetten</span><span class="sxs-lookup"><span data-stu-id="30c18-107">Building Search Tree</span></span>  
 <span data-ttu-id="30c18-108">Tabel 481 **Boomstructuurpunt dimensieset** wordt gebruikt wanneer [!INCLUDE[prod_short](includes/prod_short.md)] evalueert of een set dimensies al bestaat in tabel 480 **Dimensiesetpost**.</span><span class="sxs-lookup"><span data-stu-id="30c18-108">Table 481 **Dimension Set Tree Node** is used when [!INCLUDE[prod_short](includes/prod_short.md)] evaluates whether a set of dimensions already exists in table 480 **Dimension Set Entry** table.</span></span> <span data-ttu-id="30c18-109">De evaluatie wordt uitgevoerd doordat de zoekstructuur recursief wordt doorlopen vanaf het hoogste niveau met nummer 0.</span><span class="sxs-lookup"><span data-stu-id="30c18-109">The evaluation is performed by recursively traversing the search tree starting at the top level numbered 0.</span></span> <span data-ttu-id="30c18-110">Hoogste niveau 0 staat voor een dimensieset zonder dimensiesetposten.</span><span class="sxs-lookup"><span data-stu-id="30c18-110">The top level 0 represents a dimension set with no dimension set entries.</span></span> <span data-ttu-id="30c18-111">De onderliggende elementen van deze dimensieset vertegenwoordigen dimensiesets met slechts één dimensiesetpost.</span><span class="sxs-lookup"><span data-stu-id="30c18-111">The children of this dimension set represent dimension sets with only one dimension set entry.</span></span> <span data-ttu-id="30c18-112">De onderliggende elementen van deze dimensiesets vertegenwoordigen dimensiesets met twee onderliggende elementen, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="30c18-112">The children of these dimension sets represent dimension sets with two children, and so on.</span></span>  

### <a name="example-1"></a><span data-ttu-id="30c18-113">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="30c18-113">Example 1</span></span>  
 <span data-ttu-id="30c18-114">Het volgende diagram vertegenwoordigt een zoekactiestructuur met zes dimensiesets.</span><span class="sxs-lookup"><span data-stu-id="30c18-114">The following diagram represents a search tree with six dimension sets.</span></span> <span data-ttu-id="30c18-115">Alleen de onderscheidende dimensiesetpost wordt weergegeven in het diagram.</span><span class="sxs-lookup"><span data-stu-id="30c18-115">Only the distinguishing dimension set entry is displayed in the diagram.</span></span>  

 <span data-ttu-id="30c18-116">![Voorbeeld van een dimensieboomstructuur](media/nav2013_dimension_tree.png "Voorbeeld van een dimensieboomstructuur")</span><span class="sxs-lookup"><span data-stu-id="30c18-116">![Example of dimension tree structure](media/nav2013_dimension_tree.png "Example of dimension tree structure")</span></span>  

 <span data-ttu-id="30c18-117">In de volgende tabel wordt een volledig overzicht beschreven van dimensiesetposten waaruit elke dimensieset bestaan.</span><span class="sxs-lookup"><span data-stu-id="30c18-117">The following table describes a complete list of dimension set entries that make up each dimension set.</span></span>  

|<span data-ttu-id="30c18-118">Dimensiesets</span><span class="sxs-lookup"><span data-stu-id="30c18-118">Dimension Sets</span></span>|<span data-ttu-id="30c18-119">Dimensiesetposten</span><span class="sxs-lookup"><span data-stu-id="30c18-119">Dimension Set Entries</span></span>|  
|--------------------|---------------------------|  
|<span data-ttu-id="30c18-120">Set 0</span><span class="sxs-lookup"><span data-stu-id="30c18-120">Set 0</span></span>|<span data-ttu-id="30c18-121">Geen</span><span class="sxs-lookup"><span data-stu-id="30c18-121">None</span></span>|  
|<span data-ttu-id="30c18-122">Set 1</span><span class="sxs-lookup"><span data-stu-id="30c18-122">Set 1</span></span>|<span data-ttu-id="30c18-123">AREA 30</span><span class="sxs-lookup"><span data-stu-id="30c18-123">AREA 30</span></span>|  
|<span data-ttu-id="30c18-124">Set 2</span><span class="sxs-lookup"><span data-stu-id="30c18-124">Set 2</span></span>|<span data-ttu-id="30c18-125">AREA 30, DEPT ADM</span><span class="sxs-lookup"><span data-stu-id="30c18-125">AREA 30, DEPT ADM</span></span>|  
|<span data-ttu-id="30c18-126">Set 3</span><span class="sxs-lookup"><span data-stu-id="30c18-126">Set 3</span></span>|<span data-ttu-id="30c18-127">AREA 30, DEPT PROD</span><span class="sxs-lookup"><span data-stu-id="30c18-127">AREA 30, DEPT PROD</span></span>|  
|<span data-ttu-id="30c18-128">Set 4</span><span class="sxs-lookup"><span data-stu-id="30c18-128">Set 4</span></span>|<span data-ttu-id="30c18-129">AREA 30, DEPT ADM, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="30c18-129">AREA 30, DEPT ADM, PROJ VW</span></span>|  
|<span data-ttu-id="30c18-130">Set 5</span><span class="sxs-lookup"><span data-stu-id="30c18-130">Set 5</span></span>|<span data-ttu-id="30c18-131">AREA 40</span><span class="sxs-lookup"><span data-stu-id="30c18-131">AREA 40</span></span>|  
|<span data-ttu-id="30c18-132">Set 6</span><span class="sxs-lookup"><span data-stu-id="30c18-132">Set 6</span></span>|<span data-ttu-id="30c18-133">AREA 40, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="30c18-133">AREA 40, PROJ VW</span></span>|  

### <a name="example-2"></a><span data-ttu-id="30c18-134">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="30c18-134">Example 2</span></span>  
 <span data-ttu-id="30c18-135">Dit voorbeeld geeft aan hoe [!INCLUDE[prod_short](includes/prod_short.md)] evalueert of een dimensieset die bestaat uit de dimensiesetposten AREA 40, DEPT PROD bestaat.</span><span class="sxs-lookup"><span data-stu-id="30c18-135">This example shows how [!INCLUDE[prod_short](includes/prod_short.md)] evaluates whether a dimension set that consists of the dimension set entries AREA 40, DEPT PROD exists.</span></span>  

 <span data-ttu-id="30c18-136">Eerst werkt [!INCLUDE[prod_short](includes/prod_short.md)] ook de tabel **Boomstructuurpunt dimensieset** bij om ervoor te zorgen dat de zoekstructuur lijkt op het volgende diagram.</span><span class="sxs-lookup"><span data-stu-id="30c18-136">First, [!INCLUDE[prod_short](includes/prod_short.md)] also updates the **Dimension Set Tree Node** table to make sure that the search tree looks like the following diagram.</span></span> <span data-ttu-id="30c18-137">Zodoende wordt dimensieset 7 een onderliggend niveau van dimensieset 5.</span><span class="sxs-lookup"><span data-stu-id="30c18-137">Thus dimension set 7 becomes a child of the dimension set 5.</span></span>  

 <span data-ttu-id="30c18-138">![Voorbeeld van een dimensieboomstructuur in NAV 2013](media/nav2013_dimension_tree_example2.png "Voorbeeld van een dimensieboomstructuur in NAV 2013")</span><span class="sxs-lookup"><span data-stu-id="30c18-138">![Example of dimension tree structure in NAV 2013](media/nav2013_dimension_tree_example2.png "Example of dimension tree structure in NAV 2013")</span></span>  

### <a name="finding-dimension-set-id"></a><span data-ttu-id="30c18-139">Dimensieset-id zoeken</span><span class="sxs-lookup"><span data-stu-id="30c18-139">Finding Dimension Set ID</span></span>  
 <span data-ttu-id="30c18-140">Op conceptueel niveau zijn **Hoofd-id**, **Dimensie** en **Dimensiewaarde** in de zoekstructuur gecombineerd en gebruikt als de primaire sleutel omdat [!INCLUDE[prod_short](includes/prod_short.md)] de structuur doorloopt in dezelfde volgorde als de dimensieposten.</span><span class="sxs-lookup"><span data-stu-id="30c18-140">At a conceptual level, **Parent ID**, **Dimension**, and **Dimension Value**, in the search tree, are combined and used as the primary key because [!INCLUDE[prod_short](includes/prod_short.md)] traverses the tree in the same order as the dimension entries.</span></span> <span data-ttu-id="30c18-141">De functie GET (record) wordt gebruikt om te zoeken naar dimensieset-id.</span><span class="sxs-lookup"><span data-stu-id="30c18-141">The GET function (record) is used to search for dimension set ID.</span></span> <span data-ttu-id="30c18-142">In het volgende codevoorbeeld wordt aangegeven hoe u de dimensieset-id kunt vinden als er drie dimensiewaarden zijn.</span><span class="sxs-lookup"><span data-stu-id="30c18-142">The following code example shows how to find the dimension set ID when there are three dimension values.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

<span data-ttu-id="30c18-143">Om het vermogen van [!INCLUDE[prod_short](includes/prod_short.md)] te behouden om zowel een dimensie als dimensiewaarde te kunnen hernoemen wordt tabel 349 **Dimensiewaarde** uitgebreid met een geheelgetalveld genaamd **Dimensiewaarde-id**.</span><span class="sxs-lookup"><span data-stu-id="30c18-143">However, to preserve the ability of [!INCLUDE[prod_short](includes/prod_short.md)] to rename both a dimension and a dimension value, table 349, **Dimension Value**, is extended with an integer field, **Dimension Value ID**.</span></span> <span data-ttu-id="30c18-144">In deze tabel wordt het veldpaar **Dimensie** en **Dimensiewaarde** omgezet in een geheel getal.</span><span class="sxs-lookup"><span data-stu-id="30c18-144">This table converts the field pair, **Dimension** and **Dimension Value**, to an integer value.</span></span> <span data-ttu-id="30c18-145">Wanneer u de naam van de dimensie en dimensiewaarde wijzigt, wordt de waarde voor het gehele getal niet gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="30c18-145">When you rename the dimension and dimension value, the integer value is not changed.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a><span data-ttu-id="30c18-146">Zie ook</span><span class="sxs-lookup"><span data-stu-id="30c18-146">See Also</span></span>  
 <span data-ttu-id="30c18-147">[GET-functie (record)](/dynamics-nav/GET-Function--Record-)  </span><span class="sxs-lookup"><span data-stu-id="30c18-147">[GET Function (Record)](/dynamics-nav/GET-Function--Record-)  </span></span>  
 <span data-ttu-id="30c18-148">[Ontwerpdetails: Dimensiesetposten](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="30c18-148">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="30c18-149">[Dimensiesetposten - overzicht](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="30c18-149">[Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 [<span data-ttu-id="30c18-150">Ontwerpdetails: Tabelstructuur</span><span class="sxs-lookup"><span data-stu-id="30c18-150">Design Details: Table Structure</span></span>](design-details-table-structure.md)   
 
