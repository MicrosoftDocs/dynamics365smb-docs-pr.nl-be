---
title: 'Ontwerpdetails: Dimensiesetposten | Microsoft Docs'
description: Deze documentatie biedt gedetailleerd technisch inzicht in de concepten en principes die worden gebruikt om de opslag- en boekingsfunctie voor dimensieposten opnieuw te ontwerpen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, dimensions, codeunit
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c6b66ecee87e1fd128733f541d46b97f44af0453
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242756"
---
# <a name="design-details-dimension-set-entries"></a><span data-ttu-id="2818c-103">Ontwerpdetails: Dimensiesetposten</span><span class="sxs-lookup"><span data-stu-id="2818c-103">Design Details: Dimension Set Entries</span></span>
<span data-ttu-id="2818c-104">Deze documentatie biedt gedetailleerd technisch inzicht in de concepten en principes van de opslag- en boekingsfunctionaliteit voor dimensieposten in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2818c-104">This documentation provides detailed technical insight into the concepts and principles of the dimension-entry storing and posting functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="2818c-105">In de documentatie wordt als eerste het conceptoverzicht beschreven.</span><span class="sxs-lookup"><span data-stu-id="2818c-105">The documentation starts by describing conceptual overviews.</span></span> <span data-ttu-id="2818c-106">Vervolgens wordt de technische architectuur uitgelegd.</span><span class="sxs-lookup"><span data-stu-id="2818c-106">Then it explains the technical architecture.</span></span> <span data-ttu-id="2818c-107">Ten slotte worden codevoorbeelden gegeven om u voor te bereiden op migratie van dimensiecode en een upgrade vanaf eerdere versies dan Dynamics NAV 2013R2.</span><span class="sxs-lookup"><span data-stu-id="2818c-107">Finally, it provides code examples to prepare you for dimension code migration and upgrade from versions earlier than Dynamics NAV 2013R2.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="2818c-108">In dit gedeelte</span><span class="sxs-lookup"><span data-stu-id="2818c-108">In This Section</span></span>  
[<span data-ttu-id="2818c-109">Dimensiesetposten - overzicht</span><span class="sxs-lookup"><span data-stu-id="2818c-109">Dimension Set Entries Overview</span></span>](design-details-dimension-set-entries-overview.md)  
[<span data-ttu-id="2818c-110">Ontwerpdetails: Dimensiecombinaties zoeken</span><span class="sxs-lookup"><span data-stu-id="2818c-110">Design Details: Searching for Dimension Combinations</span></span>](design-details-searching-for-dimension-combinations.md)  
[<span data-ttu-id="2818c-111">Ontwerpdetails: Tabelstructuur</span><span class="sxs-lookup"><span data-stu-id="2818c-111">Design Details: Table Structure</span></span>](design-details-table-structure.md)  
[<span data-ttu-id="2818c-112">Ontwerpdetails: Codeunit 408 dimensiebeheer</span><span class="sxs-lookup"><span data-stu-id="2818c-112">Design Details: Codeunit 408 Dimension Management</span></span>](design-details-codeunit-408-dimension-management.md)  
[<span data-ttu-id="2818c-113">Ontwerpdetails: Codevoorbeelden van gewijzigde patronen in wijzigingen</span><span class="sxs-lookup"><span data-stu-id="2818c-113">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)
