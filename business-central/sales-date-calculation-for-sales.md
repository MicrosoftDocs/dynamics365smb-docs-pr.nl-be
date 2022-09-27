---
title: Datumberekening voor verkoop
description: De toepassing berekent automatisch de datum waarop u een artikel moet bestellen zodat u het op een bepaalde datum in voorraad hebt en beschikbaar hebt voor picken.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 538392cd86dfc348877e8ef349d42a8961934262
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9532578"
---
# <a name="date-calculation-for-sales"></a>Datumberekening voor verkoop

[!INCLUDE[prod_short](includes/prod_short.md)] berekent automatisch de vroegst mogelijke datum waarop een artikel op een verkooporderregel kan worden verzonden.

Als de klant om een specifieke leverdatum heeft verzocht, wordt berekend op welke datum de artikelen moeten kunnen worden gepickt, zodat ze op deze datum kunnen worden geleverd.

Als de klant geen specifieke leverdatum heeft aangevraagd, wordt berekend op welke datum de artikelen kunnen worden geleverd op basis van de datum waarop de artikelen kunnen worden gepickt.

## <a name="calculating-a-requested-delivery-date"></a>Een verzochte leverdatum berekenen

Als u een aangevraagde leverdatum op de verkooporderregel plaatst, wordt automatisch deze datum gebruikt als uitgangspunt voor de volgende berekeningen.

- verzochte leverdatum - verzendtijd = geplande verzenddatum
- geplande verzenddatum - verwerkingstijd uitgaand magazijn = verzenddatum

Als de artikelen op de verzenddatum kunnen worden gepickt, kan het verkoopproces worden voortgezet. Anders wordt een voorraadwaarschuwing weergegeven.

> [!Note]
> Als uw proces is gebaseerd op achterwaartse berekening, bijvoorbeeld als u de gevraagde leveringsdatum gebruikt om de geplande verzenddatum te verkrijgen, raden we u aan datumformules te gebruiken met vaste looptijden, zoals '5D' voor vijf dagen of '1W' voor een week. Datumformules zonder vaste duur, zoals 'CW' voor de huidige week of CM voor de huidige maand, kunnen leiden tot onjuiste datumberekeningen. Zie voor meer informatie over datumformules [Werken met kalenderdatums en -tijden](ui-enter-date-ranges.md).

## <a name="calculating-the-earliest-possible-delivery-date"></a>De eerst mogelijke leverdatum berekenen

Als u geen aangevraagde leverdatum op de verkooporderregel hebt opgegeven of als u niet aan de aangevraagde leverdatum kunt voldoen, wordt gezocht naar de vroegste datum waarop de artikelen beschikbaar zijn. Vervolgens wordt deze datum ingevuld op de regel in het veld Verzenddatum waarna de volgende formules worden gebruikt om te bepalen op welke datum de artikelen volgens planning worden verzonden en geleverd aan de klant.

- verzenddatum + verwerkingstijd uitgaand magazijn = geplande verzenddatum
- Geplande verzenddatum + Verzendtijd = Geplande leverdatum

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/promising-sales-order-delivery-dynamics-365-business-central/)

## <a name="see-also"></a>Zie ook

 [Datumberekening voor inkoop](purchasing-date-calculation-for-purchases.md)  
 [Ordertoezeggingsdatums berekenen](sales-how-to-calculate-order-promising-dates.md)  
 [Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
