---
title: 'Ontwerpdetails: Dimensiecombinaties zoeken | Microsoft Docs'
description: Wanneer u een pagina sluit nadat u een dimensieset hebt bewerkt, evalueert Business Central of de bewerkte dimensieset bestaat. Als de verzameling niet bestaat, wordt een nieuwe verzameling gemaakt en wordt de dimensiecombinatie-id geretourneerd.
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
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 1814d6e34fc2ab2d0c64a26ba85fa19074be4dda
ms.contentlocale: nl-be
ms.lasthandoff: 11/22/2018

---
# <a name="design-details-searching-for-dimension-combinations"></a><span data-ttu-id="5001b-104">Ontwerpdetails: Dimensiecombinaties zoeken</span><span class="sxs-lookup"><span data-stu-id="5001b-104">Design Details: Searching for Dimension Combinations</span></span>
<span data-ttu-id="5001b-105">Wanneer u een pagina sluit nadat u een dimensieset hebt bewerkt, evalueert [!INCLUDE[d365fin](includes/d365fin_md.md)] of de bewerkte dimensieset bestaat.</span><span class="sxs-lookup"><span data-stu-id="5001b-105">When you close a page after you edit a set of dimensions, [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether the edited set of dimensions exists.</span></span> <span data-ttu-id="5001b-106">Als de verzameling niet bestaat, wordt een nieuwe verzameling gemaakt en wordt de dimensiecombinatie-id geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="5001b-106">If the set does not exist, a new set is created and the dimension combination ID is returned.</span></span>  

## <a name="building-search-tree"></a><span data-ttu-id="5001b-107">Zoekactiestructuur opzetten</span><span class="sxs-lookup"><span data-stu-id="5001b-107">Building Search Tree</span></span>  
 <span data-ttu-id="5001b-108">Tabel 481 **Boomstructuurpunt dimensieset** wordt gebruikt wanneer [!INCLUDE[d365fin](includes/d365fin_md.md)] evalueert of een set dimensies al bestaat in tabel 480 **Dimensiesetpost**.</span><span class="sxs-lookup"><span data-stu-id="5001b-108">Table 481 **Dimension Set Tree Node** is used when [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether a set of dimensions already exists in table 480 **Dimension Set Entry** table.</span></span> <span data-ttu-id="5001b-109">De evaluatie wordt uitgevoerd doordat de zoekstructuur recursief wordt doorlopen vanaf het hoogste niveau met nummer 0.</span><span class="sxs-lookup"><span data-stu-id="5001b-109">The evaluation is performed by recursively traversing the search tree starting at the top level numbered 0.</span></span> <span data-ttu-id="5001b-110">Hoogste niveau 0 staat voor een dimensieset zonder dimensiesetposten.</span><span class="sxs-lookup"><span data-stu-id="5001b-110">The top level 0 represents a dimension set with no dimension set entries.</span></span> <span data-ttu-id="5001b-111">De onderliggende elementen van deze dimensieset vertegenwoordigen dimensiesets met slechts één dimensiesetpost.</span><span class="sxs-lookup"><span data-stu-id="5001b-111">The children of this dimension set represent dimension sets with only one dimension set entry.</span></span> <span data-ttu-id="5001b-112">De onderliggende elementen van deze dimensiesets vertegenwoordigen dimensiesets met twee onderliggende elementen, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="5001b-112">The children of these dimension sets represent dimension sets with two children, and so on.</span></span>  

### <a name="example-1"></a><span data-ttu-id="5001b-113">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="5001b-113">Example 1</span></span>  
 <span data-ttu-id="5001b-114">Het volgende diagram vertegenwoordigt een zoekactiestructuur met zes dimensiesets.</span><span class="sxs-lookup"><span data-stu-id="5001b-114">The following diagram represents a search tree with six dimension sets.</span></span> <span data-ttu-id="5001b-115">Alleen de onderscheidende dimensiesetpost wordt weergegeven in het diagram.</span><span class="sxs-lookup"><span data-stu-id="5001b-115">Only the distinguishing dimension set entry is displayed in the diagram.</span></span>  

 <span data-ttu-id="5001b-116">![Voorbeeld van dimensieboomstructuur](media/nav2013_dimension_tree.png "Voorbeeld van dimensieboomstructuur")</span><span class="sxs-lookup"><span data-stu-id="5001b-116">![Example of dimension tree structure](media/nav2013_dimension_tree.png "Example of dimension tree structure")</span></span>  

 <span data-ttu-id="5001b-117">In de volgende tabel wordt een volledig overzicht beschreven van dimensiesetposten waaruit elke dimensieset bestaan.</span><span class="sxs-lookup"><span data-stu-id="5001b-117">The following table describes a complete list of dimension set entries that make up each dimension set.</span></span>  

|<span data-ttu-id="5001b-118">Dimensiesets</span><span class="sxs-lookup"><span data-stu-id="5001b-118">Dimension Sets</span></span>|<span data-ttu-id="5001b-119">Dimensiesetposten</span><span class="sxs-lookup"><span data-stu-id="5001b-119">Dimension Set Entries</span></span>|  
|--------------------|---------------------------|  
|<span data-ttu-id="5001b-120">Set 0</span><span class="sxs-lookup"><span data-stu-id="5001b-120">Set 0</span></span>|<span data-ttu-id="5001b-121">Geen</span><span class="sxs-lookup"><span data-stu-id="5001b-121">None</span></span>|  
|<span data-ttu-id="5001b-122">Set 1</span><span class="sxs-lookup"><span data-stu-id="5001b-122">Set 1</span></span>|<span data-ttu-id="5001b-123">AREA 30</span><span class="sxs-lookup"><span data-stu-id="5001b-123">AREA 30</span></span>|  
|<span data-ttu-id="5001b-124">Set 2</span><span class="sxs-lookup"><span data-stu-id="5001b-124">Set 2</span></span>|<span data-ttu-id="5001b-125">AREA 30, DEPT ADM</span><span class="sxs-lookup"><span data-stu-id="5001b-125">AREA 30, DEPT ADM</span></span>|  
|<span data-ttu-id="5001b-126">Set 3</span><span class="sxs-lookup"><span data-stu-id="5001b-126">Set 3</span></span>|<span data-ttu-id="5001b-127">AREA 30, DEPT PROD</span><span class="sxs-lookup"><span data-stu-id="5001b-127">AREA 30, DEPT PROD</span></span>|  
|<span data-ttu-id="5001b-128">Set 4</span><span class="sxs-lookup"><span data-stu-id="5001b-128">Set 4</span></span>|<span data-ttu-id="5001b-129">AREA 30, DEPT ADM, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="5001b-129">AREA 30, DEPT ADM, PROJ VW</span></span>|  
|<span data-ttu-id="5001b-130">Set 5</span><span class="sxs-lookup"><span data-stu-id="5001b-130">Set 5</span></span>|<span data-ttu-id="5001b-131">AREA 40</span><span class="sxs-lookup"><span data-stu-id="5001b-131">AREA 40</span></span>|  
|<span data-ttu-id="5001b-132">Set 6</span><span class="sxs-lookup"><span data-stu-id="5001b-132">Set 6</span></span>|<span data-ttu-id="5001b-133">AREA 40, PROJ VW</span><span class="sxs-lookup"><span data-stu-id="5001b-133">AREA 40, PROJ VW</span></span>|  

### <a name="example-2"></a><span data-ttu-id="5001b-134">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="5001b-134">Example 2</span></span>  
 <span data-ttu-id="5001b-135">Dit voorbeeld geeft aan hoe [!INCLUDE[d365fin](includes/d365fin_md.md)] evalueert of een dimensieset die bestaat uit de dimensiesetposten AREA 40, DEPT PROD bestaat.</span><span class="sxs-lookup"><span data-stu-id="5001b-135">This example shows how [!INCLUDE[d365fin](includes/d365fin_md.md)] evaluates whether a dimension set that consists of the dimension set entries AREA 40, DEPT PROD exists.</span></span>  

 <span data-ttu-id="5001b-136">Eerst werkt [!INCLUDE[d365fin](includes/d365fin_md.md)] ook de tabel **Boomstructuurpunt dimensieset** bij om ervoor te zorgen dat de zoekstructuur lijkt op het volgende diagram.</span><span class="sxs-lookup"><span data-stu-id="5001b-136">First, [!INCLUDE[d365fin](includes/d365fin_md.md)] also updates the **Dimension Set Tree Node** table to make sure that the search tree looks like the following diagram.</span></span> <span data-ttu-id="5001b-137">Zodoende wordt dimensieset 7 een onderliggend niveau van dimensieset 5.</span><span class="sxs-lookup"><span data-stu-id="5001b-137">Thus dimension set 7 becomes a child of the dimension set 5.</span></span>  

 <span data-ttu-id="5001b-138">![Voorbeeld van dimensieboomstructuur in NAV 2013](media/nav2013_dimension_tree_example2.png "Voorbeeld van dimensieboomstructuur in NAV 2013")</span><span class="sxs-lookup"><span data-stu-id="5001b-138">![Example of dimension tree structure in NAV 2013](media/nav2013_dimension_tree_example2.png "Example of dimension tree structure in NAV 2013")</span></span>  

### <a name="finding-dimension-set-id"></a><span data-ttu-id="5001b-139">Dimensieset-id zoeken</span><span class="sxs-lookup"><span data-stu-id="5001b-139">Finding Dimension Set ID</span></span>  
 <span data-ttu-id="5001b-140">Op conceptueel niveau zijn **Hoofd-id**, **Dimensie** en **Dimensiewaarde** in de zoekstructuur gecombineerd en gebruikt als de primaire sleutel omdat [!INCLUDE[d365fin](includes/d365fin_md.md)] de structuur doorloopt in dezelfde volgorde als de dimensieposten.</span><span class="sxs-lookup"><span data-stu-id="5001b-140">At a conceptual level, **Parent ID**, **Dimension**, and **Dimension Value**, in the search tree, are combined and used as the primary key because [!INCLUDE[d365fin](includes/d365fin_md.md)] traverses the tree in the same order as the dimension entries.</span></span> <span data-ttu-id="5001b-141">De functie GET (record) wordt gebruikt om te zoeken naar dimensieset-id.</span><span class="sxs-lookup"><span data-stu-id="5001b-141">The GET function (record) is used to search for dimension set ID.</span></span> <span data-ttu-id="5001b-142">In het volgende codevoorbeeld wordt aangegeven hoe u de dimensieset-id kunt vinden als er drie dimensiewaarden zijn.</span><span class="sxs-lookup"><span data-stu-id="5001b-142">The following code example shows how to find the dimension set ID when there are three dimension values.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

 <span data-ttu-id="5001b-143">Om het vermogen van [!INCLUDE[d365fin](includes/d365fin_md.md)] te behouden om een dimensie en dimensiewaarde te kunnen hernoemen wordt tabel 348 **Dimensiewaarde** uitgebreid met een geheelgetalveld genaamd **Dimensiewaarde-id**.</span><span class="sxs-lookup"><span data-stu-id="5001b-143">However, to preserve the ability of [!INCLUDE[d365fin](includes/d365fin_md.md)] to rename a dimension and dimension value, table 348 **Dimension Value** is extended with an integer field of **Dimension Value ID**.</span></span> <span data-ttu-id="5001b-144">In deze tabel wordt het veldpaar **Dimensie** en **Dimensiewaarde** omgezet in een geheel getal.</span><span class="sxs-lookup"><span data-stu-id="5001b-144">This table converts the field pair **Dimension** and **Dimension Value** to an integer value.</span></span> <span data-ttu-id="5001b-145">Wanneer u de naam van de dimensie en dimensiewaarde wijzigt, wordt de waarde voor het gehele getal niet gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="5001b-145">When you rename the dimension and dimension value, the integer value is not changed.</span></span>  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a><span data-ttu-id="5001b-146">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5001b-146">See Also</span></span>  
 <span data-ttu-id="5001b-147">[GET-functie (record)](/dynamics-nav/GET-Function--Record-)  </span><span class="sxs-lookup"><span data-stu-id="5001b-147">[GET Function (Record)](/dynamics-nav/GET-Function--Record-)  </span></span>  
 <span data-ttu-id="5001b-148">[Ontwerpdetails: Dimensiesetposten](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="5001b-148">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="5001b-149">[Dimensiesetposten - overzicht](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="5001b-149">[Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="5001b-150">[Ontwerpdetails: Tabelstructuur](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="5001b-150">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
 <span data-ttu-id="5001b-151">[Ontwerpdetails: Codeunit 408 Dimensiebeheer](design-details-codeunit-408-dimension-management.md) </span><span class="sxs-lookup"><span data-stu-id="5001b-151">[Design Details: Codeunit 408 Dimension Management](design-details-codeunit-408-dimension-management.md) </span></span>  
 [<span data-ttu-id="5001b-152">Ontwerpdetails: Codevoorbeelden van gewijzigde patronen in wijzigingen</span><span class="sxs-lookup"><span data-stu-id="5001b-152">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)

