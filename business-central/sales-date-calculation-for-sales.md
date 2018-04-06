---
title: Datumberekening voor verkoop | Microsoft Docs
description: Het programma berekent automatisch de datum waarop u een artikel moet bestellen zodat u het op een bepaalde datum in voorraad hebt. Dit is de datum waarop u kunt verwachten dat artikelen die op een bepaalde datum zijn besteld beschikbaar zijn om te worden gepickt.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: cc73a03c44896bda5d1fdf789a8b349f796c6e58
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="date-calculation-for-sales"></a>Datumberekening voor verkoop
[!INCLUDE[d365fin](includes/d365fin_md.md)] berekent automatisch de vroegst mogelijke datum waarop een artikel op een verkooporderregel kan worden verzonden.

Als de klant om een specifieke leverdatum heeft verzocht, wordt berekend op welke datum de artikelen moeten kunnen worden gepickt, zodat ze op deze datum kunnen worden geleverd.

Als de klant geen specifieke leverdatum heeft aangevraagd, wordt berekend op welke datum de artikelen kunnen worden geleverd op basis van de datum waarop de artikelen kunnen worden gepickt.

## <a name="calculating-a-requested-delivery-date"></a>Een verzochte leverdatum berekenen
Als u een aangevraagde leverdatum op de verkooporderregel plaatst, wordt automatisch deze datum gebruikt als uitgangspunt voor de volgende berekeningen.

- verzochte leverdatum - verzendtijd = geplande verzenddatum
- geplande verzenddatum - verwerkingstijd uitgaand magazijn = verzenddatum

Als de artikelen op de verzenddatum kunnen worden gepickt, kan het verkoopproces worden voortgezet.

Als de artikelen niet op de verzenddatum kunnen worden gepickt, wordt een voorraadwaarschuwing gegeven.

## <a name="calculating-the-earliest-possible-delivery-date"></a>De eerst mogelijke leverdatum berekenen
Als u geen aangevraagde leverdatum op de verkooporderregel hebt opgegeven of als u niet aan de aangevraagde leverdatum kunt voldoen, wordt gezocht naar de vroegste datum waarop de artikelen beschikbaar zijn. Vervolgens wordt deze datum ingevuld op de regel in het veld Verzenddatum waarna de volgende formules worden gebruikt om te bepalen op welke datum de artikelen volgens planning worden verzonden en geleverd aan de klant.

- verzenddatum + verwerkingstijd uitgaand magazijn = geplande verzenddatum
- Geplande verzenddatum + Verzendtijd = Geplande leverdatum


## <a name="see-also"></a>Zie ook  
 [Datumberekening voor inkoop](purchasing-date-calculation-for-purchases.md)   
 [Ordertoezeggingsdatums berekenen](sales-how-to-calculate-order-promising-dates.md)  
 [Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

