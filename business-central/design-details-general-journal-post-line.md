---
title: 'Ontwerpdetails: Dagboekboekingsregel | Microsoft Docs'
description: Dit onderwerp biedt inzicht in de concepten en principes die worden gebruikt om de functie voor dagboekboekingsregels in Business Central opnieuw te ontwerpen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 337f1e679ba2f0b1fcfc0ceb8b3f0ea45ca86ecc
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "935648"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="41581-103">Ontwerpdetails: dagboekboekingsregel</span><span class="sxs-lookup"><span data-stu-id="41581-103">Design Details: General Journal Post Line</span></span>
<span data-ttu-id="41581-104">Deze documentatie biedt gedetailleerd technisch inzicht in de concepten en principes die worden gebruikt om de functie voor dagboekboekingsregels in [!INCLUDE[d365fin](includes/d365fin_md.md)] opnieuw te ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="41581-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the general journal posting line feature in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="41581-105">Door het nieuwe ontwerp wordt codeunit 12 eenvoudiger en makkelijker te beheren.</span><span class="sxs-lookup"><span data-stu-id="41581-105">The redesign makes codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="41581-106">In de documentatie wordt als eerste het conceptoverzicht van het nieuwe ontwerp beschreven.</span><span class="sxs-lookup"><span data-stu-id="41581-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="41581-107">Vervolgens wordt de technische architectuur uitgelegd om de wijzigingen door het nieuwe ontwerp te tonen.</span><span class="sxs-lookup"><span data-stu-id="41581-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="41581-108">In dit gedeelte</span><span class="sxs-lookup"><span data-stu-id="41581-108">In This Section</span></span>  
[<span data-ttu-id="41581-109">Overzicht dagboekboekingsregel</span><span class="sxs-lookup"><span data-stu-id="41581-109">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="41581-110">Ontwerpdetails: boekingsinterfacestructuur</span><span class="sxs-lookup"><span data-stu-id="41581-110">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="41581-111">Ontwerpdetails: boekingsenginestructuur</span><span class="sxs-lookup"><span data-stu-id="41581-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="41581-112">Wijzigingen in codeunit 12: Algemene variabelen toewijzen voor dagboekboekingsregel</span><span class="sxs-lookup"><span data-stu-id="41581-112">Codeunit 12 Changes: Mapping Global Variables for General Journal Post Line</span></span>](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[<span data-ttu-id="41581-113">Wijzigingen in codeunit 12: Wijzigingen in procedures voor grootboekboekingen</span><span class="sxs-lookup"><span data-stu-id="41581-113">Codeunit 12 Changes: Changes in General Journal Post Procedures</span></span>](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a><span data-ttu-id="41581-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="41581-114">See Also</span></span>  
[<span data-ttu-id="41581-115">Werken met diversendagboeken</span><span class="sxs-lookup"><span data-stu-id="41581-115">Working with General Journals</span></span>](ui-work-general-journals.md)
