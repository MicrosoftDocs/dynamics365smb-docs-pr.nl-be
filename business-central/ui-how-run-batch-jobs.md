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
ms.date: 04/01/2020
ms.author: solsen
ms.openlocfilehash: c54edd1e907c27aca719898319f69f98c0a0a068
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195615"
---
# <a name="run-batch-jobs-and-xmlports"></a>Batchtaken en XMLports uitvoeren
Een batchtaak is een routine waarmee gegevens in batches worden verwerkt, zoals bij de batchtaak **Wisselkoers herwaarderen**. Er zijn batchverwerkingen die periodieke boekhoudingactiviteiten uitvoeren, zoals het afsluiten van de resultatenrekening aan het einde van een boekjaar. Veel batchtaken voeren berekeningswerk uit, zoals de berekening van de financieringskosten, herwaardering van de wisselkoers en de berekening van eenheidsprijzen.

Een batchverwerking lijkt op een lijst, alleen wordt bij een batchverwerking het resultaat van de bewerking niet gebruikt om de resultaten af te drukken, maar om gegevens direct bij te werken.

U kunt plannen wanneer een batchtaak wordt uitgevoerd. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).

## <a name="to-run-a-batch-job"></a>Een batchverwerking uitvoeren
1. Als u de aanvraagpagina wilt openen voor de relevante batchverwerking, kiest u het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u de naam van de batchverwerking in en kiest u de gerelateerde koppeling.
2. Als het sneltabblad **Opties** aanwezig is voor de batchverwerking, vult u de velden in om te bepalen wat er met de batchverwerking gebeurt.
3. De pagina kan een of meer sneltabbladen met filters bevatten waarmee u kunt beperken welke gegevens worden gebruikt in de batchverwerking. U kunt criteria in de voorgestelde velden invoeren of meer filters toevoegen.
4. Kies **OK** om de batchverwerking te starten.

## <a name="see-also"></a>Zie ook
[Lijsten sorteren, doorzoeken en filteren](ui-enter-criteria-filters.md)  
[Taakwachtrijen gebruiken om taken te plannen](admin-job-queues-schedule-tasks.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
