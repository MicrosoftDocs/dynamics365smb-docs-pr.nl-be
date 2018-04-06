---
title: Een batchverwerking maken en uitvoeren | Microsoft Docs
description: U voert batchverwerkingen uit om gegevens te verwerken en gegevens bij te werken om bijvoorbeeld periodieke boekhoudactiviteiten uit te voeren en berekeningen uit te voeren.
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ac50d0ca59ece5365c000a9bfca06a0c18654512
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="run-batch-jobs"></a><span data-ttu-id="2bdb3-103">Batchverwerkingen uitvoeren</span><span class="sxs-lookup"><span data-stu-id="2bdb3-103">Run Batch Jobs</span></span>
<span data-ttu-id="2bdb3-104">Een batchtaak is een routine waarmee gegevens in batches worden verwerkt, zoals bij de batchtaak **Wisselkoers herwaarderen**.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="2bdb3-105">Er zijn batchverwerkingen die periodieke boekhoudingactiviteiten uitvoeren, zoals het afsluiten van de resultatenrekening aan het einde van een boekjaar.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="2bdb3-106">Veel batchtaken voeren berekeningswerk uit, zoals de berekening van de financieringskosten, herwaardering van de wisselkoers en de berekening van eenheidsprijzen.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="2bdb3-107">Een batchverwerking lijkt op een lijst, alleen wordt bij een batchverwerking het resultaat van de bewerking niet gebruikt om de resultaten af te drukken, maar om gegevens direct bij te werken.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="2bdb3-108">Een batchverwerking uitvoeren</span><span class="sxs-lookup"><span data-stu-id="2bdb3-108">To run a batch job</span></span>
1. <span data-ttu-id="2bdb3-109">Als u het aanvraagvenster voor de betreffende batchverwerking wilt openen, kiest u het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voert u de naam van de batchverwerking in en kiest u vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-109">To open the request window for the relevant batch job, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="2bdb3-110">Als het sneltabblad **Opties** aanwezig is voor de batchverwerking, vult u de velden in om te bepalen wat er met de batchverwerking gebeurt.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-110">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="2bdb3-111">Het venster kan een of meer sneltabbladen met filters bevatten waarmee u kunt beperken welke gegevens worden gebruikt in de batchverwerking.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-111">The window may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="2bdb3-112">U kunt criteria in de voorgestelde velden invoeren of meer filters toevoegen.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-112">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="2bdb3-113">Kies **OK** om de batchverwerking te starten.</span><span class="sxs-lookup"><span data-stu-id="2bdb3-113">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="2bdb3-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2bdb3-114">See Also</span></span>
[<span data-ttu-id="2bdb3-115">Criteria in filters invoeren</span><span class="sxs-lookup"><span data-stu-id="2bdb3-115">Entering Criteria in Filters</span></span>](ui-enter-criteria-filters.md)  
<span data-ttu-id="2bdb3-116">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2bdb3-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

