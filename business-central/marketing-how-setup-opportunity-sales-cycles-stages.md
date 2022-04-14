---
title: 'Procedure: Verkoopcycli en cyclusfasen instellen voor opportunities| Microsoft Docs'
description: Beschrijft hoe u verkoopstadia definieert, van eerste contact tot sluiten, om een verkoopcyclus te maken en toe te wijzen aan opportunities in Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.search.forms: 5122, 5121, 5120, 5175, 5119
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: bc42d30cfbfd664ec3d60576f21f4e7cbf3967e8
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8522940"
---
# <a name="set-up-opportunity-sales-cycles-and-cycle-stages"></a>Verkoopcycli instellen voor opportunities en cyclusfasen
Voordat u verkoopopportunities in gebruik kunt nemen, moet u verkoopcycli en verkoopcyclusfasen instellen. Een verkoopcyclus bestaat uit een reeks fasen vanaf het eerste contact tot aan het sluiten van een verkoop. Elke fase kan bepaalde vereisten hebben waaraan moet worden voldaan, zoals een verkoopofferte, voordat een opportunity naar de volgende fase kan gaan. U kunt ook aangeven of een fase kan worden overgeslagen. U kunt elk gewenst aantal verkoopcycli instellen en u kunt binnen een verkoopcyclus elk gewenst aantal verkoopcyclusfasen instellen.

Het implementeren van opportunityverkoopcycli betreft het instellen van de verkoopcycluscode, het definiëren van de verschillende fasen van de cyclus en het toewijzen van de cyclus aan opportunities. Het toekennen van de relevante activiteit of taken aan de opportunity kan ook deel uitmaken van het instellen van een verkoopcyclus.

In dit onderwerp wordt ook beschreven hoe u taken en activiteiten instelt en hoe u taken toewijst aan activiteiten. Zie voor meer informatie [Activiteiten instellen met taken](marketing-how-setup-opportunity-sales-cycles-stages.md#to-set-up-activities-with-tasks).

## <a name="to-set-up-opportunity-sales-cycle-codes"></a>Opportunityverkoopcycluscodes instellen
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopcycli** in en kies vervolgens de gerelateerde koppeling. De pagina **Verkoopcycli** wordt geopend en bevat alle bestaande verkoopcycli.
2. Kies de actie **Nieuw** en vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Herhaal deze stappen om het gewenste aantal verkoopcycli in te stellen. Nadat u de opportunityverkoopcycli hebt ingesteld, kunt u de verschillende fases instellen binnen elke cyclus.

## <a name="to-define-opportunity-sales-cycle-stages"></a>Fasen van opportunityverkoopcycli definiëren
1. Selecteer op de pagina **Verkoopcycli** de opportunityverkoopcyclus waarvoor u fases wilt instellen en kies vervolgens de actie **Fasen**. De pagina **Verkoopcyclusfasen** verschijnt.
2. Kies de actie **Nieuw** om een nieuwe fase in de verkoopcyclus in te voeren.

Herhaal deze stappen om het gewenste aantal fasen binnen de verkoopcyclus in te stellen.

## <a name="to-assign-stage-cycles-to-opportunities"></a>Verkoopfasecycli aan opportunities toewijzen
Nadat u de opportunityfasecyclus toevoegt, kunt u beginnen om verkoopopportunities toe te voegen en vervolgens de fasecyclus aan opportunities toewijzen door het veld **Verkoopcycluscode** in te stellen. Zie voor meer informatie [Verkoopopportunities maken](marketing-how-create-opportunities.md).

## <a name="to-set-up-activities-with-tasks"></a>Activiteiten instellen met taken
U kunt meerdere taken combineren, bijvoorbeeld taken die elk een stap in activiteiten vertegenwoordigen. Activiteittaken worden gerelateerd aan elkaar met een datumformule. U kunt activiteiten aan opportunities, verkopers of contacten toewijzen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Activiteiten** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw** en vul indien nodig de velden in.
3. Vul op het sneltabblad **Regels** de velden indien nodig in om een of meer taken in de activiteit te definiëren.

## <a name="to-assign-tasks-or-activities-of-tasks-to-opportunities"></a>Taken of activiteiten van taken toewijzen aan opportunities
Wanneer u een taak hebt ingesteld, kunt u deze toewijzen aan een verkoopopportunity en daarmee de activiteit toewijzen waartoe de taak behoort.

> [!NOTE]  
>   In deze procedure wordt beschreven hoe u activiteittaken toekent aan opportunities. de stappen zijn soortgelijk wanneer u taken toewijst aan contacten en verkopers.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Opportunities** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer een opportunity en kies vervolgens de actie **Taken**.
3. Kies op de pagina **Taakoverzicht** de actie **Taak maken**.
4.  Vul op de pagina **Taak maken** de benodigde velden in.

    U ziet in het veld **Opportunity** dat het automatisch is toegewezen aan de betreffende opportunity.
5. Kies de knop **OK**.
6. Selecteer op de pagina **Taakoverzicht** de nieuwe taak en kies vervolgens de actie **Activiteiten toewijzen**.
7. Vul op de pagina **Activiteit toewijzen** desgewenst de velden in en kies vervolgens de knop **OK**.

## <a name="see-also"></a>Zie ook
[Verkoopopportunities verwerken](marketing-processing-sales-opportunities.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]