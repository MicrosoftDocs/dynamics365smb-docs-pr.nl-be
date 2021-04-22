---
title: 'Ontwerpdetails: Dagboekboekingsregel | Microsoft Docs'
description: Dit onderwerp biedt inzicht in de concepten en principes die worden gebruikt om de functie voor dagboekboekingsregels in Business Central opnieuw te ontwerpen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general journal, posting, codeunit 12
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3ea2ea8a4ef5bbdff70346022ee226fd5e26748d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777835"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="9a36e-103">Ontwerpdetails: dagboekboekingsregel</span><span class="sxs-lookup"><span data-stu-id="9a36e-103">Design Details: General Journal Post Line</span></span>
<span data-ttu-id="9a36e-104">Deze documentatie biedt gedetailleerd technisch inzicht in de concepten en principes die worden gebruikt om de functie voor dagboekboekingsregels in [!INCLUDE[prod_short](includes/prod_short.md)] opnieuw te ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="9a36e-104">This documentation provides detailed technical insight into the concepts and principles that are used to redesign the general journal posting line feature in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="9a36e-105">Door het nieuwe ontwerp wordt codeunit 12 eenvoudiger en makkelijker te beheren.</span><span class="sxs-lookup"><span data-stu-id="9a36e-105">The redesign makes codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="9a36e-106">In de documentatie wordt als eerste het conceptoverzicht van het nieuwe ontwerp beschreven.</span><span class="sxs-lookup"><span data-stu-id="9a36e-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="9a36e-107">Vervolgens wordt de technische architectuur uitgelegd om de wijzigingen door het nieuwe ontwerp te tonen.</span><span class="sxs-lookup"><span data-stu-id="9a36e-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="9a36e-108">In dit gedeelte</span><span class="sxs-lookup"><span data-stu-id="9a36e-108">In This Section</span></span>  
[<span data-ttu-id="9a36e-109">Overzicht dagboekboekingsregel</span><span class="sxs-lookup"><span data-stu-id="9a36e-109">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="9a36e-110">Ontwerpdetails: boekingsinterfacestructuur</span><span class="sxs-lookup"><span data-stu-id="9a36e-110">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="9a36e-111">Ontwerpdetails: boekingsenginestructuur</span><span class="sxs-lookup"><span data-stu-id="9a36e-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="9a36e-112">Wijzigingen in codeunit 12: Algemene variabelen toewijzen voor dagboekboekingsregel</span><span class="sxs-lookup"><span data-stu-id="9a36e-112">Codeunit 12 Changes: Mapping Global Variables for General Journal Post Line</span></span>](design-details-codeunit-12-changes-mapping-global-variables-for-general-journal-post-line.md)  
[<span data-ttu-id="9a36e-113">Wijzigingen in codeunit 12: Wijzigingen in procedures voor grootboekboekingen</span><span class="sxs-lookup"><span data-stu-id="9a36e-113">Codeunit 12 Changes: Changes in General Journal Post Procedures</span></span>](design-details-codeunit-12-changes-changes-in-general-journal-post-procedures.md)  

## <a name="see-also"></a><span data-ttu-id="9a36e-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9a36e-114">See Also</span></span>  
[<span data-ttu-id="9a36e-115">Werken met diversendagboeken</span><span class="sxs-lookup"><span data-stu-id="9a36e-115">Working with General Journals</span></span>](ui-work-general-journals.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]