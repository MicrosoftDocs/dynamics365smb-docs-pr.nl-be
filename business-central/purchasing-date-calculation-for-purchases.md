---
title: Datumberekening voor inkoop | Microsoft Docs
description: De toepassing berekent automatisch de datum waarop u een artikel moet bestellen zodat u het op een bepaalde datum in voorraad hebt. Dit is de datum waarop u kunt verwachten dat artikelen die op een bepaalde datum zijn besteld beschikbaar zijn om te worden gepickt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 41b1b1b0459706a8c061a0044824b5b7c4c9aa62
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312592"
---
# <a name="date-calculation-for-purchases"></a>Datumberekening voor inkoop
[!INCLUDE[d365fin](includes/d365fin_md.md)] berekent automatisch de datum waarop u een artikel moet bestellen om het op een bepaalde datum in voorraad te hebben. Dit is de datum waarop u kunt verwachten dat artikelen die op een bepaalde datum zijn besteld beschikbaar zijn om te worden gepickt.  

Als u een aangevraagde ontvangstdatum opgeeft op een inkooporder is de berekende besteldatum de datum waarop de order moet worden geplaatst om de artikelen te ontvangen op de datum die u hebt aangevraagd. Vervolgens wordt de datum waarop de artikelen beschikbaar zijn om te worden gepickt berekend en ingevoerd in het veld **Verwachte ontvangstdatum**.  

Als u geen aangevraagde ontvangstdatum opgeeft, wordt automatisch de orderdatum op de regel gebruikt voor de berekening van de datum waarop de artikelen naar verwachting worden ontvangen en de datum waarop de artikelen beschikbaar zijn voor picken.  

## <a name="calculating-with-a-requested-receipt-date"></a>Datums berekenen met een verzochte ontvangstdatum  
Als er een aangevraagde ontvangstdatum op de inkooporderregel staat, wordt automatisch deze datum gebruikt als uitgangspunt voor de volgende berekeningen.  

- aangevraagde ontvangstdatum - levertermijn = orderdatum  
- aangevraagde ontvangstdatum + inslagtijd + veiligheidstijd = verwachte ontvangstdatum  

Als u een aangevraagde ontvangstdatum op de inkooporderkop hebt ingevoerd, wordt deze datum gekopieerd naar het bijbehorende veld op alle regels. U kunt deze datum op elke orderregel desgewenst wijzigen of verwijderen.  

> [!Note]
> Als uw proces is gebaseerd op achterwaartse berekening, bijvoorbeeld als u de gevraagde ontvangstdatum gebruikt om de besteldatum te verkrijgen, raden we u aan datumformules te gebruiken met vaste looptijden, zoals '5D' voor vijf dagen of '1W' voor een week. Datumformules zonder vaste duur, zoals 'CW' voor de huidige week of CM voor de huidige maand, kunnen leiden tot onjuiste datumberekeningen. Zie voor meer informatie over datumformules [Werken met kalenderdatums en -tijden](ui-enter-date-ranges.md).

## <a name="calculating-without-a-requested-delivery-date"></a>Datums berekenen zonder verzochte leverdatum  
Als u een inkooporderregel invoert zonder een verzochte leverdatum, wordt in het veld **Orderdatum** op de regel de datum ingevuld uit het veld **Orderdatum** op de inkooporderkop. Dit kan de datum zijn die u hebt ingevoerd of de werkdatum. Vervolgens worden automatisch de volgende datums voor de inkooporderregel berekend, met de orderdatum als uitgangspunt.  

- orderdatum + levertermijn = geplande ontvangstdatum  
- geplande ontvangstdatum + inslagtijd + veiligheidstijd = verwachte ontvangstdatum  

Als u de orderdatum op de regel wijzigt, bijvoorbeeld omdat de artikelen pas later bij de leverancier beschikbaar zijn, worden de relevante datums op de regel automatisch opnieuw berekend.  

Als u de orderdatum op de kop wijzigt, wordt deze datum automatisch gekopieerd naar het veld **Order Date** op alle regels en worden alle bijbehorende datumvelden vervolgens opnieuw berekend.  

## <a name="see-also"></a>Zie ook  
 [Datumberekening voor verkoop](sales-date-calculation-for-sales.md)   
 [Ordertoezeggingsdatums berekenen](sales-how-to-calculate-order-promising-dates.md)  
 [Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
