---
title: Datums berekenen voor inkoop
description: In dit artikel wordt beschreven hoe u datums voor aankopen kunt berekenen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'purchase order, purchase, date, receipt, delivery, lead time'
ms.search.forms: null
ms.date: 10/28/2022
ms.author: bholtorf
---
# Datums berekenen voor inkoop

Als u artikelen op een bepaalde datum in voorraad wilt hebben, kan [!INCLUDE[prod_short](includes/prod_short.md)] automatisch de datum berekenen waarop u ze moet bestellen. 

Het resultaat is de datum waarop u de door u bestelde artikelen kunt picken.  

Als u op een inkooporderregel een gevraagde ontvangstdatum opgeeft, is de berekende orderdatum de datum waarop u de order moet plaatsen. De datum waarop de artikelen beschikbaar zijn om te worden gepickt wordt weergegeven in het veld **Verwachte ontvangstdatum**.  

Als u geen gevraagde ontvangstdatum opgeeft, is de datum waarop u de artikelen verwacht te ontvangen gebaseerd op de orderdatum op de regel. 

De ontvangstdatum is ook de datum waarop de artikelen beschikbaar zijn voor picken.  

> [!TIP]
> Veel van de datumvelden die in dit artikel worden genoemd, zijn standaard verborgen op inkooporderregels. Als een veld niet beschikbaar is, kunt u het toevoegen door de pagina te personaliseren. Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.

## Berekenen met een aangevraagde ontvangstdatum

Als er een aangevraagde ontvangstdatum op de inkooporderregel staat, wordt deze datum gebruikt als uitgangspunt voor de volgende berekeningen:  

- aangevraagde ontvangstdatum - levertermijn = orderdatum  
- aangevraagde ontvangstdatum + inslagtijd + veiligheidstijd = verwachte ontvangstdatum  

Als u een gevraagde ontvangstdatum opgeeft op een inkooporderregel, wordt die datum toegewezen aan nieuwe regels wanneer u deze maakt. U kunt de datum op de regels wijzigen of verwijderen.  

> [!NOTE]
> Als uw proces is gebaseerd op achterwaartse berekening, bijvoorbeeld als u de gevraagde ontvangstdatum gebruikt om de besteldatum te verkrijgen, raden we u aan datumformules te gebruiken met vaste looptijden, zoals '5D' voor vijf dagen of '1W' voor een week. Datumformules zonder vaste duur, zoals 'CW' voor de huidige week of CM voor de huidige maand, kunnen leiden tot onjuiste datumberekeningen. Zie voor meer informatie over datumformules [Werken met kalenderdatums en -tijden](ui-enter-date-ranges.md).

## Berekenen zonder een aangevraagde ontvangstdatum

Als u een inkooporderregel invoert zonder een aangevraagde ontvangstdatum, bevat het veld **Orderdatum** op de regel de datum uit het veld **Orderdatum** op de inkooporderkop. Deze datum is de datum die u hebt ingevoerd of de werkdatum. Vervolgens worden als volgt de datums voor de inkooporderregel berekend, met de orderdatum als uitgangspunt:  

- orderdatum + levertermijn = geplande ontvangstdatum  
- geplande ontvangstdatum + inslagtijd + veiligheidstijd = verwachte ontvangstdatum  

Als u de orderdatum op de regel wijzigt, berekent [!INCLUDE[prod_short](includes/prod_short.md)] de overige datums opnieuw.  

## Standaardwaarden voor levertijdtijdberekening

[!INCLUDE[prod_short](includes/prod_short.md)] gebruikt de datumformule in het veld **Levertermijn** op de inkooporderregel om de orderdatum en de verwachte ontvangstdatum te berekenen.  

U kunt de datumformule op regels handmatig opgeven. Anders gebruikt [!INCLUDE[prod_short](includes/prod_short.md)] de formules die op de volgende pagina's zijn gedefinieerd in deze volgorde van prioriteit:

1. Voorraad - Lev.-catalogus
2. Artikel
3. SKU
4. Leverancierskaart

## Zie gerelateerde [Microsoft-training](/training/modules/estimate-receipt-dates-dynamics-365-business-central/)

## Zie ook

[Datumberekening voor verkoop](sales-date-calculation-for-sales.md)  
[Ordertoezeggingsdatums berekenen](sales-how-to-calculate-order-promising-dates.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
