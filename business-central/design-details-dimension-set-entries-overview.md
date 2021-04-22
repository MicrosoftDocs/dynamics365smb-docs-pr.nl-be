---
title: Overzicht van dimensiesetposten | Microsoft Docs
description: In dit onderwerp wordt beschreven hoe dimensiesetposten worden opgeslagen en geboekt in Dynamics 365.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: e03275c55290cccb2d8e91d7a934379184744a36
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788345"
---
# <a name="dimension-set-entries-overview"></a><span data-ttu-id="e1631-103">Overzicht dimensiesetposten</span><span class="sxs-lookup"><span data-stu-id="e1631-103">Dimension Set Entries Overview</span></span>
<span data-ttu-id="e1631-104">In dit onderwerp wordt beschreven hoe dimensiesetposten worden opgeslagen en geboekt in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="e1631-104">This topic describes how dimension set entries are stored and posted in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="dimension-sets"></a><span data-ttu-id="e1631-105">Dimensiesets</span><span class="sxs-lookup"><span data-stu-id="e1631-105">Dimension Sets</span></span>  
<span data-ttu-id="e1631-106">Een dimensieset is een unieke combinatie dimensiewaarden.</span><span class="sxs-lookup"><span data-stu-id="e1631-106">A dimension set is a unique combination of dimension values.</span></span> <span data-ttu-id="e1631-107">Een dimensieset wordt als dimensiesetposten in de database opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="e1631-107">It is stored as dimension set entries in the database.</span></span> <span data-ttu-id="e1631-108">Elke dimensiesetpost vertegenwoordigt één dimensiewaarde.</span><span class="sxs-lookup"><span data-stu-id="e1631-108">Each dimension set entry represents a single dimension value.</span></span> <span data-ttu-id="e1631-109">De dimensiesetpost wordt geïdentificeerd door een gemeenschappelijke dimensieset-id die is toegewezen aan elke dimensiesetpost die tot de dimensieset behoort.</span><span class="sxs-lookup"><span data-stu-id="e1631-109">The dimension set is identified by a common dimension set ID that is assigned to each dimension set entry that belongs to the dimension set.</span></span>  

<span data-ttu-id="e1631-110">In het volgende voorbeeld ziet u een dimensieset met drie dimensiesetposten.</span><span class="sxs-lookup"><span data-stu-id="e1631-110">The following example shows a dimension set that has three dimension set entries.</span></span> <span data-ttu-id="e1631-111">De dimensieset wordt geïdentificeerd door een dimensieset-id 108.</span><span class="sxs-lookup"><span data-stu-id="e1631-111">The dimension set is identified by a dimension set ID, which is 108.</span></span>  

|<span data-ttu-id="e1631-112">Dimensieset-id</span><span class="sxs-lookup"><span data-stu-id="e1631-112">Dimension Set ID</span></span>|<span data-ttu-id="e1631-113">Dimensiecode</span><span class="sxs-lookup"><span data-stu-id="e1631-113">Dimension Code</span></span>|<span data-ttu-id="e1631-114">Dimensiewaardecode</span><span class="sxs-lookup"><span data-stu-id="e1631-114">Dimension Value Code</span></span>|<span data-ttu-id="e1631-115">Dimensiewaardenaam</span><span class="sxs-lookup"><span data-stu-id="e1631-115">Dimension Value Name</span></span>|  
|----------------------|--------------------|--------------------------|--------------------------|  
|<span data-ttu-id="e1631-116">108</span><span class="sxs-lookup"><span data-stu-id="e1631-116">108</span></span>|<span data-ttu-id="e1631-117">DISTRICT</span><span class="sxs-lookup"><span data-stu-id="e1631-117">AREA</span></span>|<span data-ttu-id="e1631-118">70</span><span class="sxs-lookup"><span data-stu-id="e1631-118">70</span></span>|<span data-ttu-id="e1631-119">Noord-Amerika</span><span class="sxs-lookup"><span data-stu-id="e1631-119">America North</span></span>|  
|<span data-ttu-id="e1631-120">108</span><span class="sxs-lookup"><span data-stu-id="e1631-120">108</span></span>|<span data-ttu-id="e1631-121">BEDRIJFSGROEP</span><span class="sxs-lookup"><span data-stu-id="e1631-121">BUSINESSGROUP</span></span>|<span data-ttu-id="e1631-122">HOME</span><span class="sxs-lookup"><span data-stu-id="e1631-122">HOME</span></span>|<span data-ttu-id="e1631-123">Home</span><span class="sxs-lookup"><span data-stu-id="e1631-123">Home</span></span>|  
|<span data-ttu-id="e1631-124">108</span><span class="sxs-lookup"><span data-stu-id="e1631-124">108</span></span>|<span data-ttu-id="e1631-125">KSTNPLAATS</span><span class="sxs-lookup"><span data-stu-id="e1631-125">DEPARTMENT</span></span>|<span data-ttu-id="e1631-126">VERKOOP</span><span class="sxs-lookup"><span data-stu-id="e1631-126">SALES</span></span>|<span data-ttu-id="e1631-127">Verkoop</span><span class="sxs-lookup"><span data-stu-id="e1631-127">Sales</span></span>|  

## <a name="dimension-set-entries"></a><span data-ttu-id="e1631-128">Dimensiesetposten</span><span class="sxs-lookup"><span data-stu-id="e1631-128">Dimension Set Entries</span></span>  
<span data-ttu-id="e1631-129">Dimensiesets worden opgeslagen in de tabel **Dimensiesetpost** als dimensiesetposten met dezelfde dimensieset-id.</span><span class="sxs-lookup"><span data-stu-id="e1631-129">Dimension sets are stored in the **Dimension Set Entry** table as dimension set entries with the same dimension set ID.</span></span>  

<span data-ttu-id="e1631-130">![Stroom van dimensiesetposten](media/dimensionentrynav7.png "Stroom van dimensiesetposten")</span><span class="sxs-lookup"><span data-stu-id="e1631-130">![Flow of dimension set entries](media/dimensionentrynav7.png "Flow of dimension set entries")</span></span>  

<span data-ttu-id="e1631-131">Wanneer u een nieuwe dagboekregel, documentkop of documentregel maakt, kunt u een combinatie van dimensiewaarden opgeven.</span><span class="sxs-lookup"><span data-stu-id="e1631-131">When you create a new journal line, document header, or document line, you can specify a combination of dimension values.</span></span> <span data-ttu-id="e1631-132">In plaats van elke dimensiewaarde expliciet in de database op te slaan, wordt een dimensieset-id toegewezen aan de dagboekregel, documentkop of documentregel om zo de dimensieset op te geven.</span><span class="sxs-lookup"><span data-stu-id="e1631-132">Instead of explicitly storing each dimension value in the database, a dimension set ID is assigned to the journal line, document header, or document line to specify the dimension set.</span></span>  

<span data-ttu-id="e1631-133">Wanneer u de pagina **Dimensiesetposten bewerken** bewerkt en sluit, wordt gecontroleerd of de combinatie van dimensiewaarden als een dimensieset in de tabel voorkomt.</span><span class="sxs-lookup"><span data-stu-id="e1631-133">When you edit and close the **Edit Dimension Set Entries** page, a check is performed to see whether the combination of dimension values exists as a dimension set in the table.</span></span> <span data-ttu-id="e1631-134">Als de combinatie in de tabel voorkomt, wordt de overeenkomende dimensieset-id toegewezen aan de dagboekregel, documentkop of documentregel.</span><span class="sxs-lookup"><span data-stu-id="e1631-134">If the combination occurs in the table, then the corresponding dimension set ID is assigned to the journal line, document header, or document line.</span></span> <span data-ttu-id="e1631-135">Anders wordt een nieuwe dimensieset toegevoegd aan de tabel en wordt de nieuwe dimensieset-id toegewezen aan de dagboekregel, documentkop of documentregel.</span><span class="sxs-lookup"><span data-stu-id="e1631-135">Otherwise, a new dimension set is added to the table, and the new dimension set ID is assigned to the journal line, document header, or document line.</span></span>

## <a name="codeunit-408-dimension-management"></a><span data-ttu-id="e1631-136">Codeunit 408 Dimensiebeheer</span><span class="sxs-lookup"><span data-stu-id="e1631-136">Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="e1631-137">Codeunit 408, Dimensiebeheer, is een functiebibliotheek die veel voorkomende taken afhandelt die verband houden met dimensies, zoals kopiëren van de ene tabel naar de andere of van het ene document naar het andere.</span><span class="sxs-lookup"><span data-stu-id="e1631-137">Codeunit 408, Dimension Management, is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span>

## <a name="performance-improvement"></a><span data-ttu-id="e1631-138">Prestatieverbetering</span><span class="sxs-lookup"><span data-stu-id="e1631-138">Performance Improvement</span></span>  
<span data-ttu-id="e1631-139">Door dimensiesets eenmalig in de database op te slaan, wordt databaseruimte bespaard en wordt de algehele prestatie verbeterd.</span><span class="sxs-lookup"><span data-stu-id="e1631-139">By storing dimension sets once in the database, database space is preserved and overall performance is improved.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e1631-140">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e1631-140">See Also</span></span>
<span data-ttu-id="e1631-141">[Ontwerpdetails: Dimensiecombinaties zoeken](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="e1631-141">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
<span data-ttu-id="e1631-142">[Ontwerpdetails: Tabelstructuur](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="e1631-142">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
[<span data-ttu-id="e1631-143">Ontwerpdetails: Dimensiesetposten</span><span class="sxs-lookup"><span data-stu-id="e1631-143">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
