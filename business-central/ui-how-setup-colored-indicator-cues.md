---
title: Visuele signalen aanpassen over de activiteit van een indicatiestapel | Microsoft Docs
description: Stel een gekleurde indicator op een indicatiestapeltegel in om een aangepast visueel signaal van de activiteit van de indicatiestapel te bieden.
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c93bd33d972b030ede02ad7b24a8127ff2174141
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-a-colored-indicator-on-cues"></a><span data-ttu-id="0ced5-103">Een gekleurde indicator instellen voor indicatiestapels</span><span class="sxs-lookup"><span data-stu-id="0ced5-103">Set Up a Colored Indicator on Cues</span></span>
<span data-ttu-id="0ced5-104">U kunt indicatiestapels instellen die op de pagina **Start** worden weergegeven om een indicator op te nemen die van kleur verandert afhankelijk van de gegevenswaarden in de indicatiestapels.</span><span class="sxs-lookup"><span data-stu-id="0ced5-104">You can set up Cues that appear on the **Home** page to include an indicator that changes color based on the data values in the Cues.</span></span>

<span data-ttu-id="0ced5-105">De indicator wordt als een gekleurde balk weergegeven langs de bovenrand van de indicatiestapeltegel.</span><span class="sxs-lookup"><span data-stu-id="0ced5-105">The indicator appears as a colored bar along the top border of the Cue tile.</span></span> <span data-ttu-id="0ced5-106">Het geeft een visueel signaal van de status van de activiteit van de indicatiestapel. Het signaal kan gunstige of ongunstige condities aangeven om de gebruiker tot actie te laten overgaan.</span><span class="sxs-lookup"><span data-stu-id="0ced5-106">It provides a visual signal of the status of the Cue's activity, which can indicate favorable or unfavorable conditions to prompt the user to take action.</span></span> <span data-ttu-id="0ced5-107">Als een indicatiestapel bijvoorbeeld doorlopende verkoopfacturen weergeeft, kunt u de indicator zo instellen dat deze groen (gunstig) is wanneer het totale aantal doorlopende verkoopfacturen kleiner is dan 10 en dat deze rood (ongunstig) is wanneer het totaal groter is dan 20.</span><span class="sxs-lookup"><span data-stu-id="0ced5-107">For example, if a Cue displays ongoing sales invoices, you can set up the indicator to appear green (favorable) when total number of ongoing sales invoices is below 10, and appears red (unfavorable) when the total is greater than 20.</span></span>

<span data-ttu-id="0ced5-108">Vanuit het venster **Instelling indicatiestapel** kunt u indicatoren instellen voor alle indicatiestapels die beschikbaar zijn in de bedrijfsdatabase.</span><span class="sxs-lookup"><span data-stu-id="0ced5-108">From the **Cue Setup** window, you set up indicators for all the Cues that are available in the company database.</span></span>

<span data-ttu-id="0ced5-109">Als u de indicator wilt instellen, geeft u maximaal twee drempelwaarden op die de drie bereiken van gegevenswaarden definiëren (laag, gemiddeld en hoog) waarop u een andere kleur (of stijl) kunt toepassen.</span><span class="sxs-lookup"><span data-stu-id="0ced5-109">To set up the indicator, you specify up to two threshold values that define three ranges of data values (low, middle, and high) to which you can apply a different color (or style).</span></span>

## <a name="to-set-up-colored-indicators-on-cues"></a><span data-ttu-id="0ced5-110">Gekleurde indicatoren instellen voor indicatiestapels</span><span class="sxs-lookup"><span data-stu-id="0ced5-110">To set up colored indicators on Cues</span></span>
1. <span data-ttu-id="0ced5-111">Kies onder **Activititen** op uw pagina **Start** **Instelling indicatiestapel**.</span><span class="sxs-lookup"><span data-stu-id="0ced5-111">Under **Activities** on your **Home** page, choose **Set Up Cues**.</span></span>  
   <span data-ttu-id="0ced5-112">Het venster **Instelling indicatiestapel** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="0ced5-112">The **Cue Setup** window appears.</span></span> <span data-ttu-id="0ced5-113">Het venster bevat de indicatoren die op het moment zijn ingesteld voor indicatiestapels.</span><span class="sxs-lookup"><span data-stu-id="0ced5-113">The window lists the indicators that are currently setup up on Cues.</span></span>
2. <span data-ttu-id="0ced5-114">Als u een indicator wilt wijzigen, bewerkt u de velden en wijzigt u bijvoorbeeld de waarden voor de verschillende drempelwaarden.</span><span class="sxs-lookup"><span data-stu-id="0ced5-114">To modify an indicator, edit the fields and modify, for example, the values for the different thresholds.</span></span>  

<span data-ttu-id="0ced5-115">De volgende tabel bevat de kleuren die overeenkomen met de opties van de velden **Stijl laag bereik**, **Stijl middenbereik** en **Stijl hoog bereik**.</span><span class="sxs-lookup"><span data-stu-id="0ced5-115">The following table lists the colors that correspond to the options of the **Low Range Style**, **Middle Range Style**, and **High Range Style** fields.</span></span>

| <span data-ttu-id="0ced5-116">Optie</span><span class="sxs-lookup"><span data-stu-id="0ced5-116">Option</span></span> | <span data-ttu-id="0ced5-117">Kleur</span><span class="sxs-lookup"><span data-stu-id="0ced5-117">Color</span></span> |
| --- | --- |
| <span data-ttu-id="0ced5-118">**Geen**</span><span class="sxs-lookup"><span data-stu-id="0ced5-118">**None**</span></span> |<span data-ttu-id="0ced5-119">Geen kleur (dezelfde kleur als de indicatiestapeltegel)</span><span class="sxs-lookup"><span data-stu-id="0ced5-119">No color (same color as the Cue tile)</span></span>|
| <span data-ttu-id="0ced5-120">**Gunstig**</span><span class="sxs-lookup"><span data-stu-id="0ced5-120">**Favorable**</span></span> |<span data-ttu-id="0ced5-121">Groen</span><span class="sxs-lookup"><span data-stu-id="0ced5-121">Green</span></span> |
| <span data-ttu-id="0ced5-122">**Ongunstig**</span><span class="sxs-lookup"><span data-stu-id="0ced5-122">**Unfavorable**</span></span> |<span data-ttu-id="0ced5-123">Rood</span><span class="sxs-lookup"><span data-stu-id="0ced5-123">Red</span></span> |
| <span data-ttu-id="0ced5-124">**Dubbelzinnig**</span><span class="sxs-lookup"><span data-stu-id="0ced5-124">**Ambiguous**</span></span> |<span data-ttu-id="0ced5-125">Geel</span><span class="sxs-lookup"><span data-stu-id="0ced5-125">Yellow</span></span> |
| <span data-ttu-id="0ced5-126">**Ondergeschikt**</span><span class="sxs-lookup"><span data-stu-id="0ced5-126">**Subordinate**</span></span> |<span data-ttu-id="0ced5-127">Grijs</span><span class="sxs-lookup"><span data-stu-id="0ced5-127">Gray</span></span> |

## <a name="see-also"></a><span data-ttu-id="0ced5-128">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0ced5-128">See Also</span></span>
<span data-ttu-id="0ced5-129">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0ced5-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

