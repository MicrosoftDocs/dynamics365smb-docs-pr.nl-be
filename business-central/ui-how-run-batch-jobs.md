---
title: Een batchverwerking maken en uitvoeren | Microsoft Docs
description: U voert batchverwerkingen uit om gegevens te verwerken en gegevens bij te werken om bijvoorbeeld periodieke boekhoudactiviteiten uit te voeren en berekeningen uit te voeren.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, process
ms.date: 04/01/2019
ms.author: solsen
ms.openlocfilehash: 0b9bf37f9054d767938b851e399a1b2c347f77c3
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "937398"
---
# <a name="run-batch-jobs"></a><span data-ttu-id="cb77c-103">Batchverwerkingen uitvoeren</span><span class="sxs-lookup"><span data-stu-id="cb77c-103">Run Batch Jobs</span></span>
<span data-ttu-id="cb77c-104">Een batchtaak is een routine waarmee gegevens in batches worden verwerkt, zoals bij de batchtaak **Wisselkoers herwaarderen**.</span><span class="sxs-lookup"><span data-stu-id="cb77c-104">A batch job is a routine that processes data in batches, for example the **Adjust Exchange Rates** batch job.</span></span> <span data-ttu-id="cb77c-105">Er zijn batchverwerkingen die periodieke boekhoudingactiviteiten uitvoeren, zoals het afsluiten van de resultatenrekening aan het einde van een boekjaar.</span><span class="sxs-lookup"><span data-stu-id="cb77c-105">There are batch jobs that perform periodic accounting activities, such as closing the income statement at the end of a fiscal year.</span></span> <span data-ttu-id="cb77c-106">Veel batchtaken voeren berekeningswerk uit, zoals de berekening van de financieringskosten, herwaardering van de wisselkoers en de berekening van eenheidsprijzen.</span><span class="sxs-lookup"><span data-stu-id="cb77c-106">Many batch jobs do calculation work, such as calculation of finance charges, exchange rate adjustment, and calculation of unit prices.</span></span>

<span data-ttu-id="cb77c-107">Een batchverwerking lijkt op een lijst, alleen wordt bij een batchverwerking het resultaat van de bewerking niet gebruikt om de resultaten af te drukken, maar om gegevens direct bij te werken.</span><span class="sxs-lookup"><span data-stu-id="cb77c-107">A batch job is like a report, except the batch job uses the result of its work to update information directly, instead of printing the results.</span></span>

## <a name="to-run-a-batch-job"></a><span data-ttu-id="cb77c-108">Een batchverwerking uitvoeren</span><span class="sxs-lookup"><span data-stu-id="cb77c-108">To run a batch job</span></span>
1. <span data-ttu-id="cb77c-109">Als u de aanvraagpagina wilt openen voor de relevante batchverwerking, kiest u het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u de naam van de batchverwerking in en kiest u de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="cb77c-109">To open the request page for the relevant batch job, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter the name of the batch job, and then choose the related link.</span></span>
2. <span data-ttu-id="cb77c-110">Als het sneltabblad **Opties** aanwezig is voor de batchverwerking, vult u de velden in om te bepalen wat er met de batchverwerking gebeurt.</span><span class="sxs-lookup"><span data-stu-id="cb77c-110">If there is an **Options** FastTab for the batch job, fill in the fields to determine what the batch job will do.</span></span>
3. <span data-ttu-id="cb77c-111">De pagina kan een of meer sneltabbladen met filters bevatten waarmee u kunt beperken welke gegevens worden gebruikt in de batchverwerking.</span><span class="sxs-lookup"><span data-stu-id="cb77c-111">The page may contain one or more FastTab with filters, which you can use to limit the data included in the batch job.</span></span> <span data-ttu-id="cb77c-112">U kunt criteria in de voorgestelde velden invoeren of meer filters toevoegen.</span><span class="sxs-lookup"><span data-stu-id="cb77c-112">You can enter criteria in the suggested filters or add more filters.</span></span>
4. <span data-ttu-id="cb77c-113">Kies **OK** om de batchverwerking te starten.</span><span class="sxs-lookup"><span data-stu-id="cb77c-113">Choose the **OK** button to start the batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb77c-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="cb77c-114">See Also</span></span>
[<span data-ttu-id="cb77c-115">Lijsten sorteren, doorzoeken en filteren</span><span class="sxs-lookup"><span data-stu-id="cb77c-115">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
<span data-ttu-id="cb77c-116">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cb77c-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
