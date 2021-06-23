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
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 8492c83437be4cd850bafdaaa5dc70d00a075674
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215240"
---
# <a name="design-details-general-journal-post-line"></a><span data-ttu-id="ef655-103">Ontwerpdetails: dagboekboekingsregel</span><span class="sxs-lookup"><span data-stu-id="ef655-103">Design Details: General Journal Post Line</span></span>

<span data-ttu-id="ef655-104">Deze documentatie biedt gedetailleerd technisch inzicht in de concepten en principes die werden gebruikt om de functie voor dagboekboekingsregels in [!INCLUDE[prod_short](includes/prod_short.md)] opnieuw te ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="ef655-104">This documentation provides detailed technical insight into the concepts and principles that were used to redesign the general journal posting line feature in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="ef655-105">Door het nieuwe ontwerp werd codeunit 12 eenvoudiger en makkelijker te beheren.</span><span class="sxs-lookup"><span data-stu-id="ef655-105">The redesign made codeunit 12 simpler and more maintainable.</span></span> <span data-ttu-id="ef655-106">In de documentatie wordt als eerste het conceptoverzicht van het nieuwe ontwerp beschreven.</span><span class="sxs-lookup"><span data-stu-id="ef655-106">The documentation starts by describing conceptual overviews of the redesign.</span></span> <span data-ttu-id="ef655-107">Vervolgens wordt de technische architectuur uitgelegd om de wijzigingen door het nieuwe ontwerp te tonen.</span><span class="sxs-lookup"><span data-stu-id="ef655-107">Then it explains the technical architecture to show the changes that result from the redesign.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="ef655-108">De informatie in deze sectie is van toepassing op het herontwerp in een eerdere versie van het product, Microsoft Dynamics NAV 2013 R2.</span><span class="sxs-lookup"><span data-stu-id="ef655-108">The information in this section applies to the redesign in an earlier version of the product, Microsoft Dynamics NAV 2013 R2.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ef655-109">In dit gedeelte</span><span class="sxs-lookup"><span data-stu-id="ef655-109">In This Section</span></span>

[<span data-ttu-id="ef655-110">Overzicht dagboekboekingsregel</span><span class="sxs-lookup"><span data-stu-id="ef655-110">General Journal Post Line Overview</span></span>](design-details-general-journal-post-line-overview.md)  
[<span data-ttu-id="ef655-111">Ontwerpdetails: boekingsinterfacestructuur</span><span class="sxs-lookup"><span data-stu-id="ef655-111">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="ef655-112">Ontwerpdetails: boekingsenginestructuur</span><span class="sxs-lookup"><span data-stu-id="ef655-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  

## <a name="see-also"></a><span data-ttu-id="ef655-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ef655-113">See Also</span></span>

<span data-ttu-id="ef655-114">[Werken met dagboeken](ui-work-general-journals.md)
[Ontwerpdetails: Dagboekboekingsregel (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)</span><span class="sxs-lookup"><span data-stu-id="ef655-114">[Working with General Journals](ui-work-general-journals.md)
[Design Details: General Journal Post Line (Dynamics NAV)](/dynamics-nav-app/design-details-general-journal-post-line)</span></span>  

[!INCLUDE[footer-include](includes/footer-banner.md)]