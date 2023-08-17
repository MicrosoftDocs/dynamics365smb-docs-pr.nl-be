---
title: Verkoopcycli instellen voor opportunities en cyclusfasen
description: 'Beschrijft hoe u verkoopstadia definieert, van eerste contact tot sluiten, om een verkoopcyclus te maken en toe te wijzen aan opportunities in Business Central.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'relationship, prospect'
ms.search.forms: '5122, 5121, 5120, 5175, 5119, 5098, 5096'
ms.date: 05/27/2022
ms.author: jswymer
---
# <a name="set-up-opportunity-sales-cycles-and-cycle-stages"></a>Verkoopcycli instellen voor opportunities en cyclusfasen

Voordat u verkoopkansen in gebruik kunt nemen, moet u verkoopcycli en verkoopcyclusfasen instellen. Een verkoopcyclus bestaat uit een reeks fasen vanaf het eerste contact tot aan het sluiten van een verkoop. Voor elke fase definieert u vereisten waaraan moet worden voldaan, zoals een verkoopofferte, voordat een verkoopkans naar de volgende fase kan gaan. U kunt ook aangeven of een fase kan worden overgeslagen. U kunt zoveel verkoopcyclussen instellen als u nodig hebt. U kunt binnen een verkoopcyclus zoveel verkoopcyclusfasen instellen als nodig is.

Als u verkoopkanscycli wilt gebruiken, moet u de verkoopcyclus instellen, de verschillende fasen van de cyclus definiëren en de cyclus toewijzen aan verkoopkansen. Het toekennen van de relevante activiteit of taken aan de opportunity kan ook deel uitmaken van het instellen van een verkoopcyclus.

In dit artikel wordt ook beschreven hoe u taken en activiteiten instelt en hoe u taken toewijst aan activiteiten. Zie voor meer informatie [Activiteiten instellen met taken](marketing-how-setup-opportunity-sales-cycles-stages.md#to-set-up-activities-with-tasks).

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

U kunt meerdere taken, bijvoorbeeld taken die elk een stap vertegenwoordigen, combineren tot activiteiten. Activiteittaken worden gerelateerd aan elkaar met een datumformule. U kunt activiteiten aan opportunities, verkopers of contacten toewijzen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Activiteiten** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw** en vul indien nodig de velden in. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
3. Vul op het sneltabblad **Regels** de velden indien nodig in om een of meer taken in de activiteit te definiëren.

## <a name="to-assign-tasks-or-activities-of-tasks-to-opportunities"></a>Taken of activiteiten van taken toewijzen aan opportunities

Wanneer u een taak hebt ingesteld, kunt u deze toewijzen aan een verkoopopportunity en daarmee de activiteit toewijzen waartoe de taak behoort.

> [!NOTE]
> U kunt geen taken van het type *Vergadering* maken in [!INCLUDE [prod_short](includes/prod_short.md)] online. Die mogelijkheid vereist toegang tot een on-premises implementatie.

In de volgende procedure wordt beschreven hoe u activiteittaken toekent aan verkoopkansen. de stappen zijn soortgelijk wanneer u taken toewijst aan contacten en verkopers.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Opportunities** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer een opportunity en kies vervolgens de actie **Taken**.
3. Kies op de pagina **Taakoverzicht** de actie **Taak maken**.
4. Vul op de pagina **Taak maken** de benodigde velden in. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

    > [!TIP]
    > Zoals u ziet in het veld **Verkoopkans** wordt de taak automatisch toegewezen aan de betreffende verkoopkans.
5. Kies de knop **Ok**.
6. Selecteer op de pagina **Taakoverzicht** de nieuwe taak en kies vervolgens de actie **Activiteiten toewijzen**.
7. Vul op de pagina **Activiteit toewijzen** desgewenst de velden in en kies vervolgens de knop **OK**.

## <a name="see-also"></a>Zie ook

[Verkoopopportunities verwerken](marketing-processing-sales-opportunities.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
