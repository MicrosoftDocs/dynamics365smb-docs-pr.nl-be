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
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 24df541a8f1d1cf5df3f53a00922ae0d88d7192f
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="0b9d0-103">Ontwerpdetails: dagboekboekingsregel</span><span class="sxs-lookup"><span data-stu-id="0b9d0-103">Design Details: General Journal Post Line</span></span>
<span data-ttu-id="0b9d0-104">Deze documentatie biedt gedetailleerd technisch inzicht in de concepten en principes die worden gebruikt om de functie voor dagboekboekingsregels in [!INCLUDE[d365fin](includes/d365fin_md.md)] opnieuw te ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="0b9d0-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the general journal posting line feature in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="0b9d0-105">Door het nieuwe ontwerp wordt codeunit 12 eenvoudiger en makkelijker te beheren.</span><span class="sxs-lookup"><span data-stu-id="0b9d0-105">The redesign makes codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="0b9d0-106">In de documentatie wordt als eerste het conceptoverzicht van het nieuwe ontwerp beschreven.</span><span class="sxs-lookup"><span data-stu-id="0b9d0-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="0b9d0-107">Vervolgens wordt de technische architectuur uitgelegd om de wijzigingen door het nieuwe ontwerp te tonen.</span><span class="sxs-lookup"><span data-stu-id="0b9d0-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="0b9d0-108">In dit gedeelte</span><span class="sxs-lookup"><span data-stu-id="0b9d0-108">In This Section</span></span>  
[<span data-ttu-id="0b9d0-109">Overzicht dagboekboekingsregel</span><span class="sxs-lookup"><span data-stu-id="0b9d0-109">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="0b9d0-110">Ontwerpdetails: boekingsinterfacestructuur</span><span class="sxs-lookup"><span data-stu-id="0b9d0-110">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="0b9d0-111">Ontwerpdetails: boekingsenginestructuur</span><span class="sxs-lookup"><span data-stu-id="0b9d0-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="0b9d0-112">Wijzigingen in codeunit 12: Algemene variabelen toewijzen voor dagboekboekingsregel</span><span class="sxs-lookup"><span data-stu-id="0b9d0-112">Codeunit 12 Changes: Mapping Global Variables for General Journal Post Line</span></span>](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[<span data-ttu-id="0b9d0-113">Wijzigingen in codeunit 12: Wijzigingen in procedures voor grootboekboekingen</span><span class="sxs-lookup"><span data-stu-id="0b9d0-113">Codeunit 12 Changes: Changes in General Journal Post Procedures</span></span>](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a><span data-ttu-id="0b9d0-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0b9d0-114">See Also</span></span>  
[<span data-ttu-id="0b9d0-115">Werken met diversendagboeken</span><span class="sxs-lookup"><span data-stu-id="0b9d0-115">Working with General Journals</span></span>](ui-work-general-journals.md)

