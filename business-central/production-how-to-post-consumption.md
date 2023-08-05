---
title: Verbruik in batches boeken
description: 'Als de afboekingsmethode Handmatig is, moet u de materialen handmatig boeken met behulp van een verbruiksdagboek.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000846, 99000850'
ms.date: 03/08/2023
ms.author: edupont
---
# Productieverbruik in batches boeken

Als de afboekingsmethode **Handmatig** is, gebruikt u een verbruiksdagboek om de componenten handmatig te boeken.  

> [!NOTE]
> Als u het selectievakje **Pick vereist** op de vestigingskaart hebt ingeschakeld om aan te geven dat de vestiging voorraadpickverwerking vereist, hoeft u deze batchverwerking niet uit te voeren. [!INCLUDE[prod_short](includes/prod_short.md)] handelt het verbruik dan af wanneer u de voorraadpick boekt. Zie voor meer informatie [Picken voor productie in standaardmagazijnconfiguraties](warehouse-how-to-pick-for-production.md).  

U kunt [!INCLUDE[prod_short](includes/prod_short.md)] ook zo instellen materialen automatisch worden geboekt (*afgeboekt*) als u productieorders start of voltooit. Zie voor meer informatie [Afboeking van materialen op basis van de uitvoer van een bewerking inschakelen](production-how-to-flush-components-according-to-operation-output.md).

## Verbruik boeken voor een of meer productieorderregels

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verbruiksdagboek** in en kies vervolgens de gerelateerde koppeling.  
2. Voer in de velden informatie over de productieorder en verbruik in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Gebruik de actie **Verbruik berekenen** om journaalregels vanuit productieorders te genereren gebaseerd op de werkelijke output (het aantal gereedgemelde goederen dat u hebt gemeld) of de verwachte output (het aantal gereedgemelde goederen dat u verwacht te produceren).

    > [!NOTE]
    > Als u de vestigingskaart zo hebt geconfigureerd dat magazijnpickverwerking vereist is, kunnen alleen hoeveelheden die al via een magazijnactiviteit zijn gepickt, worden ingevoerd in het veld **Aantal** op de pagina **Verbruiksdagboek**, niet een berekende hoeveelheid. Zie voor meer informatie [Picken voor productie of assemblage in geavanceerde magazijnconfiguraties](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)

3. Kies de actie **Boeken** om het verbruik te boeken. De gerelateerde voorraden worden verminderd.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Zie ook

[Productie](production-manage-manufacturing.md)  
[Productie instellen](production-configure-production-processes.md)  
[Gepland](production-planning.md)  
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
