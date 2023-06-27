---
title: Ontwerpdetails - Verschil | Microsoft Docs
description: 'Verschil wordt gedefinieerd als het verschil tussen de werkelijke kosten en de vaste verrekenprijs, zoals in de volgende formule wordt beschreven.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-variance"></a>Ontwerpdetails: Verschil
Verschil wordt gedefinieerd als het verschil tussen de werkelijke kosten en de vaste verrekenprijs, zoals in de volgende formule wordt beschreven.  

 werkelijke kosten – standaardkosten = verschil  

 Als de werkelijke kosten veranderen, bijvoorbeeld omdat u een artikeltoeslag boekt op een latere datum, wordt het verschil overeenkomstig bijgewerkt.  

> [!NOTE]  
>  Herwaardering heeft geen invloed op de verschilberekening, omdat herwaardering alleen de voorraadwaarde wijzigt.  

## <a name="example"></a>Opmerking
 In het volgende voorbeeld ziet u hoe het verschil wordt berekend voor aangeschafte artikelen. Het is gebaseerd op het volgende scenario:  

1.  De gebruiker koopt een artikel tegen LV 90,00, maar de vaste verrekenprijs is LV 100,00. Het inkoopverschil is dus LV -10,00.  
2.  LV 10,00 wordt gecrediteerd naar de inkoopverschillenrekening.  
3.  De gebruiker boekt een artikeltoeslag van LV 20,00. De werkelijke kosten worden verhoogd tot LV 110,00 en de waarde van het inkoopverschil wordt LV 10,00.  
4.  LV 20,00 wordt gedebiteerd naar de inkoopverschillenrekening. Het netto-inkoopverschil wordt LV 10,00.  
5.  De gebruiker herwaardeert het artikel van LV 100,00 naar LV 70,00. Dit heeft geen invloed op de verschilberekening, alleen op de voorraadwaarde.  

 De volgende tabel toont de twee soorten resulterende waardeposten.  

 ![Berekening van het inkoopverschil.](media/design_details_inventory_costing_11_purchase_variance.png "Berekening van het inkoopverschil")  

## <a name="determining-the-standard-cost"></a>De standaardkosten bepalen
 De vaste verrekenprijs wordt gebruikt bij het berekenen van het te kapitaliseren verschil en aantal. Aangezien de vaste verrekenprijs na verloop van tijd kan worden gewijzigd als gevolg van handmatige updateberekeningen, hebt u een tijdstip nodig waarop de vaste verrekenprijs wordt vastgesteld voor verschilberekening. Dit punt is wanneer de voorraadtoename wordt gefactureerd. Voor geproduceerde of geassembleerde artikelen worden standaardkosten bepaald wanneer de kosten worden gewaardeerd.  

 De volgende tabel toont hoe verschillende kostenaandelen worden gegenereerd voor geproduceerde en geassembleerde artikelen als u de functie Vaste verrekenprijs berekenen gebruikt.  

|Aandeel kosten|Ingekocht artikel|Geproduceerd/geassembleerd artikel|  
|----------------|--------------------|------------------------------|  
|**Vaste verrekenprijs**||Materiaalkosten (één niveau) + Capaciteitskosten (één niveau) + Uitbestedingskosten (één niveau) + Cap.-overheadkosten (één niveau) + Prod.-overheadkosten (één niveau)|  
|**Materiaalkosten (Eén niv.)**|Kostprijs|![Vergelijking 1.](media/design_details_inventory_costing_11_equation_1.png "Vergelijking 1")|  
|**Capaciteitskosten (Eén niv.)**|Niet van toepassing|![Vergelijking 2.](media/design_details_inventory_costing_11_equation_2.png "Vergelijking 2")|  
|**Uitbestedingskosten (Eén niv.)**|Niet van toepassing|![Vergelijking 3.](media/design_details_inventory_costing_11_equation_3.png "Vergelijking 3")|  
|**Cap.-overheadkosten (Eén niv.)**|Niet van toepassing|![Vergelijking 4.](media/design_details_inventory_costing_11_equation_4.png "Vergelijking 4")|  
|**Prod.-overheadkosten. (Eén niv.)**|Niet van toepassing|(Materiaalkosten (één niveau) + Capaciteitskosten (één niveau) + Uitbestedingskosten (één niveau)) * Indirecte kosten % / 100 + Overheadtarief|  
|**Materiaalkosten (Alle niv.)**|Kostprijs|![Vergelijking 5.](media/design_details_inventory_costing_11_equation_5.png "Vergelijking 5")|  
|**Capaciteitskosten (Alle niv.)**|Niet van toepassing|![Vergelijking 6.](media/design_details_inventory_costing_11_equation_6.png "Vergelijking 6")|  
|**Uitbestedingskosten (Alle niv.)**|Niet van toepassing|![Vergelijking 7.](media/design_details_inventory_costing_11_equation_7.png "Vergelijking 7")|  
|**Samengevouwen capaciteitsoverheadkosten**|Niet van toepassing|![Vergelijking 8.](media/design_details_inventory_costing_11_equation_8.png "Vergelijking 8")|  
|**Prod.-overheadkosten (Alle niv.)**|Niet van toepassing|![Vergelijking 9.](media/design_details_inventory_costing_11_equation_9.png "Vergelijking 9")|  

## <a name="see-also"></a>Zie ook
 [Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)   
 [Ontwerpdetails: Waarderingsmethoden](design-details-costing-methods.md) [Voorraadkosten beheren](finance-manage-inventory-costs.md)  
 [Financiën](finance.md)  
 [Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
