---
title: Overzicht dagboekboekingsregel | Microsoft Docs
description: In dit onderwerp worden de wijzigingen beschreven die zijn doorgevoerd in Codeunit 12, **Dagboek - Boekingsregel**, het belangrijkste toepassingsobject voor grootboekboekingen en de enige plaats om grootboek-, btw-, klanten- en leveranciersposten in te voegen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, general ledger, post
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 1f6060eb7672b332fb570eb13fe027a3b58e6594
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215265"
---
# <a name="general-journal-post-line-overview"></a><span data-ttu-id="d418d-103">Overzicht dagboekboekingsregel</span><span class="sxs-lookup"><span data-stu-id="d418d-103">General Journal Post Line Overview</span></span>

<span data-ttu-id="d418d-104">Codeunit 12, **Dagboek - Boekingsregel**, is het belangrijkste toepassingsobject voor grootboekboekingen en is de enige plaats om grootboek-, btw, klanten- en leveranciersposten in te voegen.</span><span class="sxs-lookup"><span data-stu-id="d418d-104">Codeunit 12, **Gen. Jnl.-Post Line**, is the major application object for general ledger posting and is the only place to insert general ledger, VAT, and customer and vendor ledger entries.</span></span> <span data-ttu-id="d418d-105">Deze codeunit wordt ook gebruikt voor de bewerkingen Vereffenen, Vereffening ongedaan maken en Tegenboeken.</span><span class="sxs-lookup"><span data-stu-id="d418d-105">This codeunit is also used for all Apply, Unapply and Reverse operations.</span></span>  
  
<span data-ttu-id="d418d-106">In Microsoft Dynamics NAV 2013 R2 werd de codeunit opnieuw ontworpen omdat deze erg groot was geworden, met ongeveer 7.600 coderegels.</span><span class="sxs-lookup"><span data-stu-id="d418d-106">In Microsoft Dynamics NAV 2013 R2, the codeunit was redesigned because it had become very large, with approximately 7,600 code lines.</span></span> <span data-ttu-id="d418d-107">De architectuur is gewijzigd en de codeunit is eenvoudiger en makkelijker te beheren gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d418d-107">The architecture was changed and the codeunit has been made simpler and more maintainable.</span></span> <span data-ttu-id="d418d-108">Deze documentatie beschrijft de wijzigingen en bevat informatie die u nodig hebt voor upgrades.</span><span class="sxs-lookup"><span data-stu-id="d418d-108">This documentation describes the changes and provides information that you will need for upgrade.</span></span>  
  
## <a name="old-architecture"></a><span data-ttu-id="d418d-109">Oude architectuur</span><span class="sxs-lookup"><span data-stu-id="d418d-109">Old Architecture</span></span>  
<span data-ttu-id="d418d-110">De oude architectuur had de volgende functies:</span><span class="sxs-lookup"><span data-stu-id="d418d-110">The old architecture had the following features:</span></span>  
  
* <span data-ttu-id="d418d-111">Er werd uitgebreid gebruikgemaakt van algemene variabelen, waardoor de kans op verborgen fouten als gevolg van variabelen met het verkeerde bereik, groter werd.</span><span class="sxs-lookup"><span data-stu-id="d418d-111">There was extensive use of global variables, which increased the possibility of hidden errors due to use of variables with the wrong scope.</span></span>  
* <span data-ttu-id="d418d-112">Er waren veel lange procedures (met meer dan 100 coderegels) die ook zeer cyclomatisch complex waren (er werden veel geneste instructies met CASE, REPEAT en IF gebruikt), waardoor de code erg moeilijk te lezen en onderhouden was.</span><span class="sxs-lookup"><span data-stu-id="d418d-112">There were many long procedures (with more than 100 code lines) that also had high cyclomatic complexity (that is, a lot of CASE, REPEAT, IF nested statements), which made the code very difficult to read and maintain.</span></span>  
* <span data-ttu-id="d418d-113">Meerdere procedures die alleen lokaal werden gebruikt en alleen waren bedoeld voor lokaal gebruik, waren niet gemarkeerd als lokaal.</span><span class="sxs-lookup"><span data-stu-id="d418d-113">Several procedures that were only used locally and were only meant to be used locally were not marked as local.</span></span>  
* <span data-ttu-id="d418d-114">De meeste procedures hadden geen parameters en gebruikten algemene variabelen.</span><span class="sxs-lookup"><span data-stu-id="d418d-114">Most procedures had no parameters and used global variables.</span></span> <span data-ttu-id="d418d-115">Sommige gebruikten parameters en overschreven algemene door lokale variabelen.</span><span class="sxs-lookup"><span data-stu-id="d418d-115">Some used parameters and overrode global variables with locals.</span></span>  
* <span data-ttu-id="d418d-116">De codepatronen voor het zoeken van grootboekrekeningen en het maken van grootboek- en btw-posten waren niet gestandaardiseerd en verschilden per plek.</span><span class="sxs-lookup"><span data-stu-id="d418d-116">Code patterns for searching the general ledger accounts and creating general ledger and VAT entries was not standardized and varied from place to place.</span></span> <span data-ttu-id="d418d-117">Bovendien waren er veel codedubbelingen en verbroken symmetrie tussen klant- en leverancierscode.</span><span class="sxs-lookup"><span data-stu-id="d418d-117">In addition, there was a lot of code duplication and broken symmetry between customer and vendor code.</span></span>  
* <span data-ttu-id="d418d-118">Een groot deel van de code in codeunit 12, ongeveer 30 procent, heeft betrekking op berekeningen van contantkorting en betalingstolerantie, hoewel deze voorzieningen in veel landen of regio's niet nodig zijn.</span><span class="sxs-lookup"><span data-stu-id="d418d-118">A large part of the code in codeunit 12, approximately 30 percent, related to payment discount and tolerance calculations, although these features are not needed in many countries or regions.</span></span>  
* <span data-ttu-id="d418d-119">Boeken, Vereffenen, Vereffening ongedaan maken, Tegenboeken, Contantkorting en betalingstolerantie, en Wisselkoersherwaardering waren aan elkaar gekoppeld in codeunit 12 met gebruik van een lange lijst van algemene variabelen.</span><span class="sxs-lookup"><span data-stu-id="d418d-119">Posting, Apply, Unapply, Reverse, Payment Discount and Tolerance, and Exchange Rate Adjustment were married together in codeunit 12 using a long list of global variables.</span></span>  
  
### <a name="new-architecture"></a><span data-ttu-id="d418d-120">Nieuwe architectuur</span><span class="sxs-lookup"><span data-stu-id="d418d-120">New Architecture</span></span>  
<span data-ttu-id="d418d-121">In [!INCLUDE[prod_short](includes/prod_short.md)] heeft codeunit 12 de volgende verbeteringen:</span><span class="sxs-lookup"><span data-stu-id="d418d-121">In [!INCLUDE[prod_short](includes/prod_short.md)], codeunit 12 has had the following improvements:</span></span>  
  
* <span data-ttu-id="d418d-122">Codeunit 12 is opnieuw gestructureerd in kleinere procedures (alle korter dan 100 coderegels).</span><span class="sxs-lookup"><span data-stu-id="d418d-122">Codeunit 12 has been refactored into smaller procedures (all less than 100 code lines).</span></span>  
* <span data-ttu-id="d418d-123">Gestandaardiseerde patronen voor de zoekopdracht van grootboekrekeningen zijn geïmplementeerd door het gebruik van Help-functies uit de boekingsgroeptabellen.</span><span class="sxs-lookup"><span data-stu-id="d418d-123">Standardized patterns for the search of general ledger accounts have been implemented by using helper functions from Posting Group tables.</span></span>  
* <span data-ttu-id="d418d-124">Er is een boekingsengineframework geïmplementeerd om het begin en eind van transacties te beheren, en het maken van grootboek- en btw-posten, het verzamelen van btw-aanpassingen en het berekenen van aanvullende valutabedragen te scheiden.</span><span class="sxs-lookup"><span data-stu-id="d418d-124">A Posting Engine Framework has been implemented to manage the start and finish of transactions and to isolate the creation to general ledger and VAT entries, the collection of VAT adjustment, and the calculation of additional currency amounts.</span></span>  
* <span data-ttu-id="d418d-125">Codeverdubbeling is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="d418d-125">Code duplication has been eliminated.</span></span>  
* <span data-ttu-id="d418d-126">Veel Help-functies zijn overgebracht naar overeenkomstige tabellen voor klant- en leveranciersposten.</span><span class="sxs-lookup"><span data-stu-id="d418d-126">Many helper functions have been transferred to corresponding customer and vendor ledger entry tables.</span></span>  
* <span data-ttu-id="d418d-127">Het gebruik van algemene variabelen is geminimaliseerd, zodat elke procedure parameters gebruikt en een eigen toepassingslogica omvat.</span><span class="sxs-lookup"><span data-stu-id="d418d-127">The use of global variables has been minimized, so that each procedure uses parameters and encapsulates its own application logic.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d418d-128">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d418d-128">See Also</span></span>

[<span data-ttu-id="d418d-129">Ontwerpdetails: boekingsinterfacestructuur</span><span class="sxs-lookup"><span data-stu-id="d418d-129">Design Details: Posting Interface Structure</span></span>](design-details-posting-interface-structure.md)  
[<span data-ttu-id="d418d-130">Ontwerpdetails: boekingsenginestructuur</span><span class="sxs-lookup"><span data-stu-id="d418d-130">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)  
[<span data-ttu-id="d418d-131">Ontwerpdetails: dagboekboekingsregel (Dynamics NAV)</span><span class="sxs-lookup"><span data-stu-id="d418d-131">Design Details: General Journal Post Line (Dynamics NAV)</span></span>](/dynamics-nav-app/design-details-general-journal-post-line)  


[!INCLUDE[footer-include](includes/footer-banner.md)]