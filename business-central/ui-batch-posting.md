---
title: Hoe u meerdere documenten tegelijkertijd boekt | Microsoft Docs
description: In plaats van afzonderlijke documenten een voor een te boeken kunt u meerdere niet-geboekte documenten in een lijst selecteren voor batchboeking, hetzij voor onmiddellijke boeking, hetzij gepland voor bijvoorbeeld het einde van de dag.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1fd25f8b07a359414f62ef4757162f8a73889c27
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912733"
---
# <a name="post-multiple-documents-at-the-same-time"></a>Meerdere documenten tegelijkertijd boeken

In plaats van afzonderlijke documenten een voor een te boeken kunt u meerdere niet-geboekte documenten in een lijst selecteren voor directe batchboeking of voor batchboeking volgens een planning, bijvoorbeeld aan het einde van de dag. Dit kan handig zijn als alleen een supervisor documenten kan boeken die door andere gebruikers zijn gemaakt of om problemen met de systeemprestaties te voorkomen door boeking tijdens werkuren.

## <a name="to-post-multiple-purchase-orders-immediately"></a>Meerdere inkooporders onmiddellijk boeken

In de volgende procedure wordt uitgelegd hoe u meerdere inkooporders onmiddellijk kunt boeken. De stappen zijn vergelijkbaar voor alle inkoop- en verkoopdocumenten.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies de gerelateerde koppeling.
2. Ga op de pagina **Inkooporders** door met het selecteren van alle te boeken orders:
3. Voer in het veld **Nr.** de drie verticale stippen om het contextmenu te openen en kies vervolgens de actie **Meer selecteren** .
4. Schakel het selectievakje in voor alle regels die orders vertegenwoordigen die u tegelijkertijd wilt boeken.
5. Kies de actie **Boeken** en kies vervolgens weer de actie **Boeken** .
6. Kies de knop **Ja** in het bevestigingsbericht.

## <a name="to-batch-post-multiple-purchase-orders"></a>Meerdere inkooporders in een batch boeken

In de volgende procedure wordt uitgelegd hoe u inkooporders in een batch boekt. De stappen zijn vergelijkbaar voor alle inkoop- en verkoopdocumenten waarbij de actie **Batchboeken** beschikbaar is.

> [!NOTE]
> Het batchboeken van documenten gebeurt op de achtergrond. [!INCLUDE [prodshort](includes/prodshort.md)] online bevat standaardtaken voor boeken op de achtergrond en boeken in batches. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies de gerelateerde koppeling.  
2. Ga op de pagina **Inkooporders** door met het selecteren van alle te boeken orders:
3. Voer in het veld **Nr.** de drie verticale stippen om het contextmenu te openen en kies vervolgens de actie **Meer selecteren** .
4. Schakel het selectievakje in voor alle regels die orders vertegenwoordigen die u tegelijkertijd wilt boeken.
5. Kies de actie **Boeken** en kies vervolgens de actie **Batchboeken** .
6. Vul desgewenst de velden op de pagina **Batchboeken inkooporders** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Kies de knop **Ok** .
8. Als u mogelijke problemen wilt zien die zijn opgetreden tijdens het batchboeken van documenten, opent u de pagina **Foutberichtregister** .

De inkooporders worden nu toegevoegd aan een speciale taakwachtrijpost, die bepaalt wanneer de documenten worden geboekt. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).

Als u **PDF** selecteert in het veld **Soort rapportuitvoer** , zijn succesvol geboekte inkooporders beschikbaar in het onderdeel **Rapportinbox** in uw rolcentrum.

## <a name="see-also"></a>Zie ook

[Documenten en dagboeken boeken](ui-post-documents-journals.md)  
[Taakwachtrijen gebruiken om taken te plannen](admin-job-queues-schedule-tasks.md)  
[Geboekte documenten bewerken](across-edit-posted-document.md)  
[Niet-betaalde inkoopfacturen corrigeren of annuleren](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Pagina's en informatie zoeken met Vertel me](ui-search.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
