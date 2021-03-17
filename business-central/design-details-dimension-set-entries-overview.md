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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c0df3fc05935f5a3142564b132e89931fb2647f1
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377200"
---
# <a name="dimension-set-entries-overview"></a><span data-ttu-id="8aec4-103">Overzicht dimensiesetposten</span><span class="sxs-lookup"><span data-stu-id="8aec4-103">Dimension Set Entries Overview</span></span>
<span data-ttu-id="8aec4-104">In dit onderwerp wordt beschreven hoe dimensiesetposten worden opgeslagen en geboekt in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="8aec4-104">This topic describes how dimension set entries are stored and posted in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="dimension-sets"></a><span data-ttu-id="8aec4-105">Dimensiesets</span><span class="sxs-lookup"><span data-stu-id="8aec4-105">Dimension Sets</span></span>  
<span data-ttu-id="8aec4-106">Een dimensieset is een unieke combinatie dimensiewaarden.</span><span class="sxs-lookup"><span data-stu-id="8aec4-106">A dimension set is a unique combination of dimension values.</span></span> <span data-ttu-id="8aec4-107">Een dimensieset wordt als dimensiesetposten in de database opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="8aec4-107">It is stored as dimension set entries in the database.</span></span> <span data-ttu-id="8aec4-108">Elke dimensiesetpost vertegenwoordigt één dimensiewaarde.</span><span class="sxs-lookup"><span data-stu-id="8aec4-108">Each dimension set entry represents a single dimension value.</span></span> <span data-ttu-id="8aec4-109">De dimensiesetpost wordt geïdentificeerd door een gemeenschappelijke dimensieset-id die is toegewezen aan elke dimensiesetpost die tot de dimensieset behoort.</span><span class="sxs-lookup"><span data-stu-id="8aec4-109">The dimension set is identified by a common dimension set ID that is assigned to each dimension set entry that belongs to the dimension set.</span></span>  

<span data-ttu-id="8aec4-110">In het volgende voorbeeld ziet u een dimensieset met drie dimensiesetposten.</span><span class="sxs-lookup"><span data-stu-id="8aec4-110">The following example shows a dimension set that has three dimension set entries.</span></span> <span data-ttu-id="8aec4-111">De dimensieset wordt geïdentificeerd door een dimensieset-id 108.</span><span class="sxs-lookup"><span data-stu-id="8aec4-111">The dimension set is identified by a dimension set ID, which is 108.</span></span>  

|<span data-ttu-id="8aec4-112">Dimensieset-id</span><span class="sxs-lookup"><span data-stu-id="8aec4-112">Dimension Set ID</span></span>|<span data-ttu-id="8aec4-113">Dimensiecode</span><span class="sxs-lookup"><span data-stu-id="8aec4-113">Dimension Code</span></span>|<span data-ttu-id="8aec4-114">Dimensiewaardecode</span><span class="sxs-lookup"><span data-stu-id="8aec4-114">Dimension Value Code</span></span>|<span data-ttu-id="8aec4-115">Dimensiewaardenaam</span><span class="sxs-lookup"><span data-stu-id="8aec4-115">Dimension Value Name</span></span>|  
|----------------------|--------------------|--------------------------|--------------------------|  
|<span data-ttu-id="8aec4-116">108</span><span class="sxs-lookup"><span data-stu-id="8aec4-116">108</span></span>|<span data-ttu-id="8aec4-117">DISTRICT</span><span class="sxs-lookup"><span data-stu-id="8aec4-117">AREA</span></span>|<span data-ttu-id="8aec4-118">70</span><span class="sxs-lookup"><span data-stu-id="8aec4-118">70</span></span>|<span data-ttu-id="8aec4-119">Noord-Amerika</span><span class="sxs-lookup"><span data-stu-id="8aec4-119">America North</span></span>|  
|<span data-ttu-id="8aec4-120">108</span><span class="sxs-lookup"><span data-stu-id="8aec4-120">108</span></span>|<span data-ttu-id="8aec4-121">BEDRIJFSGROEP</span><span class="sxs-lookup"><span data-stu-id="8aec4-121">BUSINESSGROUP</span></span>|<span data-ttu-id="8aec4-122">HOME</span><span class="sxs-lookup"><span data-stu-id="8aec4-122">HOME</span></span>|<span data-ttu-id="8aec4-123">Home</span><span class="sxs-lookup"><span data-stu-id="8aec4-123">Home</span></span>|  
|<span data-ttu-id="8aec4-124">108</span><span class="sxs-lookup"><span data-stu-id="8aec4-124">108</span></span>|<span data-ttu-id="8aec4-125">KSTNPLAATS</span><span class="sxs-lookup"><span data-stu-id="8aec4-125">DEPARTMENT</span></span>|<span data-ttu-id="8aec4-126">VERKOOP</span><span class="sxs-lookup"><span data-stu-id="8aec4-126">SALES</span></span>|<span data-ttu-id="8aec4-127">Verkoop</span><span class="sxs-lookup"><span data-stu-id="8aec4-127">Sales</span></span>|  

## <a name="dimension-set-entries"></a><span data-ttu-id="8aec4-128">Dimensiesetposten</span><span class="sxs-lookup"><span data-stu-id="8aec4-128">Dimension Set Entries</span></span>  
<span data-ttu-id="8aec4-129">Dimensiesets worden opgeslagen in de tabel **Dimensiesetpost** als dimensiesetposten met dezelfde dimensieset-id.</span><span class="sxs-lookup"><span data-stu-id="8aec4-129">Dimension sets are stored in the **Dimension Set Entry** table as dimension set entries with the same dimension set ID.</span></span>  

<span data-ttu-id="8aec4-130">![Stroom van dimensiesetposten](media/dimensionentrynav7.png "Stroom van dimensiesetposten")</span><span class="sxs-lookup"><span data-stu-id="8aec4-130">![Flow of dimension set entries](media/dimensionentrynav7.png "Flow of dimension set entries")</span></span>  

<span data-ttu-id="8aec4-131">Wanneer u een nieuwe dagboekregel, documentkop of documentregel maakt, kunt u een combinatie van dimensiewaarden opgeven.</span><span class="sxs-lookup"><span data-stu-id="8aec4-131">When you create a new journal line, document header, or document line, you can specify a combination of dimension values.</span></span> <span data-ttu-id="8aec4-132">In plaats van elke dimensiewaarde expliciet in de database op te slaan, wordt een dimensieset-id toegewezen aan de dagboekregel, documentkop of documentregel om zo de dimensieset op te geven.</span><span class="sxs-lookup"><span data-stu-id="8aec4-132">Instead of explicitly storing each dimension value in the database, a dimension set ID is assigned to the journal line, document header, or document line to specify the dimension set.</span></span>  

<span data-ttu-id="8aec4-133">Wanneer u de pagina **Dimensiesetposten bewerken** bewerkt en sluit, wordt gecontroleerd of de combinatie van dimensiewaarden als een dimensieset in de tabel voorkomt.</span><span class="sxs-lookup"><span data-stu-id="8aec4-133">When you edit and close the **Edit Dimension Set Entries** page, a check is performed to see whether the combination of dimension values exists as a dimension set in the table.</span></span> <span data-ttu-id="8aec4-134">Als de combinatie in de tabel voorkomt, wordt de overeenkomende dimensieset-id toegewezen aan de dagboekregel, documentkop of documentregel.</span><span class="sxs-lookup"><span data-stu-id="8aec4-134">If the combination occurs in the table, then the corresponding dimension set ID is assigned to the journal line, document header, or document line.</span></span> <span data-ttu-id="8aec4-135">Anders wordt een nieuwe dimensieset toegevoegd aan de tabel en wordt de nieuwe dimensieset-id toegewezen aan de dagboekregel, documentkop of documentregel.</span><span class="sxs-lookup"><span data-stu-id="8aec4-135">Otherwise, a new dimension set is added to the table, and the new dimension set ID is assigned to the journal line, document header, or document line.</span></span>

## <a name="codeunit-408-dimension-management"></a><span data-ttu-id="8aec4-136">Codeunit 408 Dimensiebeheer</span><span class="sxs-lookup"><span data-stu-id="8aec4-136">Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="8aec4-137">Codeunit 408, Dimensiebeheer, is een functiebibliotheek die veel voorkomende taken afhandelt die verband houden met dimensies, zoals kopiëren van de ene tabel naar de andere of van het ene document naar het andere.</span><span class="sxs-lookup"><span data-stu-id="8aec4-137">Codeunit 408, Dimension Management, is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span>

## <a name="performance-improvement"></a><span data-ttu-id="8aec4-138">Prestatieverbetering</span><span class="sxs-lookup"><span data-stu-id="8aec4-138">Performance Improvement</span></span>  
<span data-ttu-id="8aec4-139">Door dimensiesets eenmalig in de database op te slaan, wordt databaseruimte bespaard en wordt de algehele prestatie verbeterd.</span><span class="sxs-lookup"><span data-stu-id="8aec4-139">By storing dimension sets once in the database, database space is preserved and overall performance is improved.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8aec4-140">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8aec4-140">See Also</span></span>  
<span data-ttu-id="8aec4-141">[Ontwerpdetails: Dimensiecombinaties zoeken](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="8aec4-141">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
<span data-ttu-id="8aec4-142">[Ontwerpdetails: Tabelstructuur](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="8aec4-142">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
[<span data-ttu-id="8aec4-143">Ontwerpdetails: Dimensiesetposten</span><span class="sxs-lookup"><span data-stu-id="8aec4-143">Design Details: Dimension Set Entries</span></span>](design-details-dimension-set-entries.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]