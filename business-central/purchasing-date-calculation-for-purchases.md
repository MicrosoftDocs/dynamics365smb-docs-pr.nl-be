---
title: Datumberekening voor inkoop
description: De toepassing berekent automatisch de datum waarop u een artikel moet bestellen zodat u het op een bepaalde datum in voorraad hebt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 6758c631fcddf157894ed06a483b811342a44e0d
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/30/2021
ms.locfileid: "6321051"
---
# <a name="date-calculation-for-purchases"></a>Datumberekening voor inkoop

[!INCLUDE[prod_short](includes/prod_short.md)] berekent automatisch de datum waarop u een artikel moet bestellen om het op een bepaalde datum in voorraad te hebben. Dit is de datum waarop u kunt verwachten dat artikelen die op een bepaalde datum zijn besteld beschikbaar zijn om te worden gepickt.  

Als u een aangevraagde ontvangstdatum opgeeft op een inkooporder is de berekende besteldatum de datum waarop de order moet worden geplaatst om de artikelen te ontvangen op de datum die u hebt aangevraagd. Vervolgens wordt de datum waarop de artikelen beschikbaar zijn om te worden gepickt berekend en ingevoerd in het veld **Verwachte ontvangstdatum**.  

Als u geen aangevraagde ontvangstdatum opgeeft, wordt automatisch de orderdatum op de regel gebruikt voor de berekening van de datum waarop de artikelen naar verwachting worden ontvangen en de datum waarop de artikelen beschikbaar zijn voor picken.  

## <a name="calculating-with-a-requested-receipt-date"></a>Berekenen met een aangevraagde ontvangstdatum

Als er een aangevraagde ontvangstdatum op de inkooporderregel staat, wordt automatisch deze datum gebruikt als uitgangspunt voor de volgende berekeningen.  

- aangevraagde ontvangstdatum - levertermijn = orderdatum  
- aangevraagde ontvangstdatum + inslagtijd + veiligheidstijd = verwachte ontvangstdatum  

Als u een aangevraagde ontvangstdatum op de inkooporderkop hebt ingevoerd, wordt deze datum gekopieerd naar het bijbehorende veld op alle regels. U kunt deze datum op elke orderregel desgewenst wijzigen of verwijderen.  

> [!NOTE]
> Als uw proces is gebaseerd op achterwaartse berekening, bijvoorbeeld als u de gevraagde ontvangstdatum gebruikt om de besteldatum te verkrijgen, raden we u aan datumformules te gebruiken met vaste looptijden, zoals '5D' voor vijf dagen of '1W' voor een week. Datumformules zonder vaste duur, zoals 'CW' voor de huidige week of CM voor de huidige maand, kunnen leiden tot onjuiste datumberekeningen. Zie voor meer informatie over datumformules [Werken met kalenderdatums en -tijden](ui-enter-date-ranges.md).

## <a name="calculating-without-a-requested-delivery-date"></a>Berekenen zonder aangevraagde leverdatum

Als u een inkooporderregel invoert zonder een verzochte leverdatum, wordt in het veld **Orderdatum** op de regel de datum ingevuld uit het veld **Orderdatum** op de inkooporderkop. Dit kan de datum zijn die u hebt ingevoerd of de werkdatum. Vervolgens worden automatisch de volgende datums voor de inkooporderregel berekend, met de orderdatum als uitgangspunt.  

- orderdatum + levertermijn = geplande ontvangstdatum  
- geplande ontvangstdatum + inslagtijd + veiligheidstijd = verwachte ontvangstdatum  

Als u de orderdatum op de regel wijzigt, bijvoorbeeld omdat de artikelen pas later bij de leverancier beschikbaar zijn, worden de relevante datums op de regel automatisch opnieuw berekend.  

Als u de orderdatum op de kop wijzigt, wordt deze datum automatisch gekopieerd naar het veld **Order Date** op alle regels en worden alle bijbehorende datumvelden vervolgens opnieuw berekend.  

## <a name="default-values-for-lead-time-calculation"></a>Standaardwaarden voor levertijdtijdberekening

[!INCLUDE[prod_short](includes/prod_short.md)] gebruikt de waarde van het veld **Levertermijnberek.** op de inkooporderregel om de order en de verwachte ontvangstdatums te berekenen.  

U kunt de waarde op de regel handmatig specificeren of het programma de waarden laten gebruiken die zijn gedefinieerd op de leverancierskaart, artikelkaart, SKU-kaart of de artikelleverancierscatalogus.
De levertermijnwaarde op de leverancierskaart wordt echter alleen gebruikt als er geen doorlooptijd is opgegeven op de artikelkaart, de SKU-kaart of de artikelleverancierscatalogus voor het artikel. Dit is ook de escalerende volgorde van prioriteit voor deze waarden. Als ze allemaal worden verstrekt, heeft de levertermijn van de leverancierskaart de laagste prioriteit en heeft de levertermijn van de artikelleverancierscatalogus de hoogste prioriteit.  

## <a name="see-also"></a>Zie ook

[Datumberekening voor verkoop](sales-date-calculation-for-sales.md)   
[Ordertoezeggingsdatums berekenen](sales-how-to-calculate-order-promising-dates.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]