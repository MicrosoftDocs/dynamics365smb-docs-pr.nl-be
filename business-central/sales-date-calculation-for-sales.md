---
title: Leveringsdatumberekening voor verkoop
description: De toepassing berekent automatisch de datum waarop u een artikel moet bestellen zodat u het op een bepaalde datum in voorraad hebt en beschikbaar hebt voor picken.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/22/2022
ms.author: bholtorf
---
# Leveringsdatumberekening voor verkoop

[!INCLUDE[prod_short](includes/prod_short.md)] berekent automatisch de vroegst mogelijke datum waarop een artikel op een verkooporderregel kan worden verzonden.

* Als de klant om een specifieke leverdatum heeft verzocht, wordt berekend op welke datum de artikelen moeten kunnen worden gepickt, zodat ze op deze datum kunnen worden geleverd.
* Indien de klant geen specifieke leveringsdatum vraagt, wordt de datum berekend waarop de artikelen geleverd kunnen worden. De berekening start vanaf de datum waarop de artikelen beschikbaar zijn voor picken.

## Een verzochte leverdatum berekenen

Als u een aangevraagde leverdatum op de verkooporderregel plaatst, wordt automatisch deze datum gebruikt als uitgangspunt voor de volgende berekeningen.

- *verzochte leverdatum - verzendtijd = geplande verzenddatum*
- *geplande verzenddatum - verwerkingstijd uitgaand magazijn = verzenddatum*

Als de artikelen op de verzenddatum kunnen worden gepickt, kan het verkoopproces worden voortgezet. Anders wordt een voorraadwaarschuwing weergegeven.

> [!NOTE]
> Als uw proces is gebaseerd op achterwaartse berekening, bijvoorbeeld als u de gevraagde leveringsdatum gebruikt om de geplande verzenddatum te verkrijgen, raden we u aan datumformules te gebruiken met vaste looptijden, zoals '5D' voor vijf dagen of '1W' voor een week. Datumformules zonder vaste duur, zoals 'CW' voor de huidige week of CM voor de huidige maand, kunnen leiden tot onjuiste datumberekeningen. Zie voor meer informatie over datumformules [Werken met kalenderdatums en -tijden](ui-enter-date-ranges.md).

## De eerst mogelijke leverdatum berekenen

Als u geen aangevraagde leverdatum op de verkooporderregel hebt opgegeven of als u niet aan de aangevraagde leverdatum kunt voldoen, wordt gezocht naar de vroegste datum waarop de artikelen beschikbaar zijn. Vervolgens wordt deze datum ingevuld op de regel in het veld **Verzenddatum** waarna de volgende formules worden gebruikt om te bepalen op welke datum de artikelen volgens planning worden verzonden en geleverd aan de klant.

- *verzenddatum + verwerkingstijd uitgaand magazijn = geplande verzenddatum*
- *geplande verzenddatum + verzendtijd = geplande leverdatum*

## Zie ook

[Datumberekening voor inkopen](purchasing-date-calculation-for-purchases.md)  
[Ordertoezeggingsdatums berekenen](sales-how-to-calculate-order-promising-dates.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
