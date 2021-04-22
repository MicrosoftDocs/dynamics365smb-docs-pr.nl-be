---
title: Een batchverwerking maken en uitvoeren | Microsoft Docs
description: U voert batchverwerkingen uit om gegevens te verwerken en gegevens bij te werken om bijvoorbeeld periodieke boekhoudactiviteiten uit te voeren en berekeningen uit te voeren.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 04/01/2021
ms.author: solsen
ms.openlocfilehash: 05b65f5b001259fff25d0f59dfc6267d9ee00c7f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782265"
---
# <a name="run-batch-jobs-and-xmlports"></a><span data-ttu-id="8f212-103">Batchtaken en XMLports uitvoeren</span><span class="sxs-lookup"><span data-stu-id="8f212-103">Run Batch Jobs and XMLports</span></span>
<span data-ttu-id="8f212-104">Een batchtaak is een routine waarmee gegevens in batches worden verwerkt, zoals bij de batchtaak **Wisselkoers herwaarderen**.</span><span class="sxs-lookup"><span data-stu-id="8f212-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="8f212-105">Er zijn batchverwerkingen die periodieke boekhoudingactiviteiten uitvoeren, zoals het afsluiten van de resultatenrekening aan het einde van een boekjaar.</span><span class="sxs-lookup"><span data-stu-id="8f212-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="8f212-106">Veel batchtaken voeren berekeningswerk uit, zoals de berekening van de financieringskosten, herwaardering van de wisselkoers en de berekening van eenheidsprijzen.</span><span class="sxs-lookup"><span data-stu-id="8f212-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="8f212-107">Een batchverwerking lijkt op een lijst, alleen wordt bij een batchverwerking het resultaat van de bewerking niet gebruikt om de resultaten af te drukken, maar om gegevens direct bij te werken.</span><span class="sxs-lookup"><span data-stu-id="8f212-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

<span data-ttu-id="8f212-108">U kunt plannen wanneer een batchtaak wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="8f212-108">You can schedule when a batch job runs.</span></span> <span data-ttu-id="8f212-109">Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="8f212-109">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="8f212-110">Een batchverwerking uitvoeren</span><span class="sxs-lookup"><span data-stu-id="8f212-110">To run a batch job</span></span>
1. <span data-ttu-id="8f212-111">Als u de aanvraagpagina wilt openen voor de relevante batchverwerking, kiest u het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u de naam van de batchverwerking in en kiest u de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="8f212-111">To open the request page for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="8f212-112">Als het sneltabblad **Opties** aanwezig is voor de batchverwerking, vult u de velden in om te bepalen wat er met de batchverwerking gebeurt.</span><span class="sxs-lookup"><span data-stu-id="8f212-112">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="8f212-113">De pagina kan een of meer sneltabbladen met filters bevatten waarmee u kunt beperken welke gegevens worden gebruikt in de batchverwerking.</span><span class="sxs-lookup"><span data-stu-id="8f212-113">The page may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="8f212-114">U kunt criteria in de voorgestelde velden invoeren of meer filters toevoegen.</span><span class="sxs-lookup"><span data-stu-id="8f212-114">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="8f212-115">Kies **OK** om de batchverwerking te starten.</span><span class="sxs-lookup"><span data-stu-id="8f212-115">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="8f212-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8f212-116">See Also</span></span>
[<span data-ttu-id="8f212-117">Lijsten sorteren, doorzoeken en filteren</span><span class="sxs-lookup"><span data-stu-id="8f212-117">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="8f212-118">Taakwachtrijen gebruiken om taken te plannen</span><span class="sxs-lookup"><span data-stu-id="8f212-118">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
<span data-ttu-id="8f212-119">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8f212-119">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]