---
title: Verbruik in batches boeken
description: Als de afboekingsmethode **Handmatig** is, moet u de materialen handmatig boeken met behulp van een verbruiksdagboek.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 66a19b624c74ec844806c27c490c300746b46704
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787914"
---
# <a name="batch-post-production-consumption"></a>Productieverbruik in batches boeken

Als de afboekingsmethode **Handmatig** is, moet u de materialen handmatig boeken met behulp van een verbruiksdagboek.  

>[!NOTE]
> Als u het selectievakje **Pick vereist** op de vestigingskaart hebt ingeschakeld om aan te geven dat de vestiging voorraadpickverwerking vereist, hoeft u deze batchverwerking niet uit te voeren. [!INCLUDE[prod_short](includes/prod_short.md)] handelt het verbruik dan af wanneer u de voorraadpick boekt. Zie [Picken voor productie of assemblage](warehouse-how-to-pick-for-production.md#to-pick-components-in-basic-warehouse-configurations) voor meer informatie. 

U kunt [!INCLUDE[prod_short](includes/prod_short.md)] ook zo instellen materialen automatisch worden geboekt (*afgeboekt*) als u productieorders start of voltooit. Zie voor meer informatie [Afboeking van materialen op basis van de uitvoer van een bewerking inschakelen](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Verbruik boeken voor een of meer productieorderregels

1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verbruiksdagboek** in en kies de desbetreffende koppeling.  
2.  Voer in de velden informatie over de productieorder en verbruik in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Gebruik de actie **Verbruik berekenen** om journaalregels vanuit productieorders te genereren gebaseerd op de werkelijke output (het aantal gereedgemelde goederen dat u hebt gemeld) of de verwachte output (het aantal gereedgemelde goederen dat u verwacht te produceren).

    > [!NOTE]
    > Als u de vestigingskaart zo hebt geconfigureerd dat magazijnpickverwerking vereist is, kunnen alleen hoeveelheden die al via een magazijnactiviteit zijn gepickt, worden ingevoerd in het veld **Aantal** op de pagina **Verbruiksdagboek**, niet een berekende hoeveelheid. Zie voor meer informatie [Picken voor productie of assemblage in geavanceerde magazijnconfiguraties](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)

3.  Kies de actie **Boeken** om het verbruik te boeken. De gerelateerde voorraden worden verminderd.



## <a name="see-also"></a>Zie ook

[Productie](production-manage-manufacturing.md)    
[Productie instellen](production-configure-production-processes.md)  
[Gepland](production-planning.md)      
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
