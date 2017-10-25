---
title: 'Ontwerpdetails: Dimensiesetposten | Microsoft Docs'
description: Deze documentatie biedt gedetailleerd technisch inzicht in de concepten en principes die worden gebruikt om de opslag- en boekingsfunctie voor dimensieposten opnieuw te ontwerpen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, dimensions, codeunit
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 17fd783bd44faa914d473aae35ddc31145c181ef
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-dimension-set-entries"></a><span data-ttu-id="a1705-103">Ontwerpdetails: Dimensiesetposten</span><span class="sxs-lookup"><span data-stu-id="a1705-103">Design Details: Dimension Set Entries</span></span>
<span data-ttu-id="a1705-104">Deze documentatie biedt gedetailleerd technisch inzicht in de concepten en principes die worden gebruikt om de opslag- en boekingsfunctie voor dimensieposten in [!INCLUDE[d365fin](includes/d365fin_md.md)] opnieuw te ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="a1705-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the dimension entry storing and posting feature in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="a1705-105">In de documentatie wordt als eerste het conceptoverzicht van het nieuwe ontwerp beschreven.</span><span class="sxs-lookup"><span data-stu-id="a1705-105">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="a1705-106">Vervolgens wordt de technische architectuur uitgelegd om te tonen hoe het nieuwe ontwerp wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a1705-106">Then it explains the technical architecture to show how the redesign is made.</span></span> <span data-ttu-id="a1705-107">Ten slotte worden codevoorbeelden geleverd om u voor te bereiden op dimensiecodemigratie en -upgrade.</span><span class="sxs-lookup"><span data-stu-id="a1705-107">Finally, it provides code examples to prepare you for dimension code migration and upgrade.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="a1705-108">In dit gedeelte</span><span class="sxs-lookup"><span data-stu-id="a1705-108">In This Section</span></span>  
[<span data-ttu-id="a1705-109">Dimensiesetposten - overzicht</span><span class="sxs-lookup"><span data-stu-id="a1705-109">Dimension Set Entries Overview</span></span>](design-details-dimension-set-entries-overview.md)  
[<span data-ttu-id="a1705-110">Ontwerpdetails: Dimensiecombinaties zoeken</span><span class="sxs-lookup"><span data-stu-id="a1705-110">Design Details: Searching for Dimension Combinations</span></span>](design-details-searching-for-dimension-combinations.md)  
[<span data-ttu-id="a1705-111">Ontwerpdetails: Tabelstructuur</span><span class="sxs-lookup"><span data-stu-id="a1705-111">Design Details: Table Structure</span></span>](design-details-table-structure.md)  
[<span data-ttu-id="a1705-112">Ontwerpdetails: Codeunit 408 dimensiebeheer</span><span class="sxs-lookup"><span data-stu-id="a1705-112">Design Details: Codeunit 408 Dimension Management</span></span>](design-details-codeunit-408-dimension-management.md)  
[<span data-ttu-id="a1705-113">Ontwerpdetails: Codevoorbeelden van gewijzigde patronen in wijzigingen</span><span class="sxs-lookup"><span data-stu-id="a1705-113">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)

