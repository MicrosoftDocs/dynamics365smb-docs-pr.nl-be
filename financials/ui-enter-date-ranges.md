---
title: Datumbereiken instellen in Finance and Operations, Business edition | Microsoft Docs
description: Leer hoe u een rapport met gegevens uit specifieke perioden op basis van datumbereiken in Finance and Operations, Business edition maakt.
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 05/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0494a04e67803049df71cfefe779c831c9f31674
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="entering-date-ranges"></a>Datumbereiken invoeren 
U kunt filters met een begin- en einddatum instellen om alleen de gegevens in dat datumbereik of tijdsinterval in te stellen. Voor het instellen van een datumbereik gelden speciale regels. Neem als voorbeeld de **Klanten top 10**:

![Een datumbereik instellen op de aanvraagpagina voor de lijst Klanten top 10](./media/ui-enter-date-ranges/customer-top10-list.png)

Hier kunt u de lijst tot een datumbereik beperken, zoals de afgelopen 2 weken of een totaal van 6 weken, of wat voor bereik u ook nodig hebt. Als u datumbereiken wilt invoeren, voert u datums in en gebruikt u **..** of **|** om het bereik in te stellen. Als u in ons voorbeeld de top 10 klanten voor de eerste twee weken van mei wilt invoeren, stelt u het datumfilter in op *05 01 17..05 14 17*.
Hier volgen enkele andere voorbeelden:

| Betekenis | Opmerking | Opgenomen posten |
|---|---|---|
|Gelijk aan| 12 15 16 |Alleen posten die zijn geboekt op 15 december 2016.|
|Interval| 12 15 16..01 15 17<br /><br />..12 15 16|Posten die zijn geboekt in de periode tussen en tot en met 15 december 2016 en 15 januari 2017.<br /><br />Posten die zijn geboekt op 15 december 2016 of eerder.|
|Of/of|12 15 16&#124;12 16 16|Posten die zijn geboekt op 15 december of 16 december 2016. Als deze posten zijn geboekt op beide dagen, worden ze allebei weergegeven.|

U kunt de verschillende notatiesoorten ook combineren.

| Opmerking | Opgenomen posten |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Posten die zijn geboekt op 15 december 2016 of op datums tussen en tot en met 1 december 2016 en 31 mei 2017. |
|..12 14 16&#124;12 30 16.. | Posten die zijn geboekt op 14 december of eerder, of posten die zijn geboekt op 30 december of later. Dit wil zeggen, alle posten behalve die zijn geboekt tussen 15 december en 29 december tot en met. |

U ziet dat we hier de Amerikaanse datumnotatie MMDDYY hebben gebruikt. Zodra [!INCLUDE[d365fin](includes/d365fin_md.md)] beschikbaar wordt in andere markten, zult u de indelingen kunnen gebruiken die u gewend bent.

## <a name="see-also"></a>Zie ook
[Werken met [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Criteria in filters invoeren](ui-enter-criteria-filters.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)

