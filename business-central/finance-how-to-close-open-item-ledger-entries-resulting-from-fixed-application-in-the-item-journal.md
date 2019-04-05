---
title: 'Procedure: Open artikelposten die uit een vaste vereffening in het artikeldagboek voortkomen sluiten | Microsoft Docs'
description: U kunt het veld **Vereffenen van post** op de pagina **Artikeldagboek** gebruiken om een vaste vereffening tussen een inkomende transactie en de oorspronkelijke uitgaande transactie te maken. Bijvoorbeeld om de uitgaande transactie te corrigeren of de retourzending te verwerken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: e3f210b86168d34ec775f85b416b6d0e365cce88
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816264"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a>Open artikelposten die uit een vaste vereffening in het artikeldagboek voortkomen sluiten
U kunt het veld **Vereffenen van post** op de pagina **Artikeldagboek** gebruiken om een vaste vereffening tussen een inkomende transactie en de oorspronkelijke uitgaande transactie te maken. Bijvoorbeeld om de uitgaande transactie te corrigeren of de retourzending te verwerken. Zie voor meer informatie Vereffenen van post.  

> [!IMPORTANT]  
>  Vaste vereffeningen die op deze manier worden uitgevoerd, worden alleen toegepast op de kosten, niet op de hoeveelheid. Bijgevolg sluit de geboekte positieve artikelpost niet de toegepaste uitgaande post en blijft deze zelf ook geopend. Dit geldt ook wanneer u een vaste vereffening voor een positieve post toepast op een negatieve post die niet is afgesloten door een gewone positieve post. In dat geval blijven de negatieve en de positieve posten geopend.  
>   
>  Dit betekent dat u een voorraadperiode waarin een dergelijke vermelding bestaat, niet kunt sluiten.  

De volgende procedure laat zien hoe u dergelijke posten kunt sluiten door het uitvoeren van twee corrigerende boekingen in het artikeldagboek.  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a>Openstaande artikelposten die uit een vaste vereffening in het artikeldagboek voortkomen sluiten  

1.  Gebruik het veld **Vereffenen van post** om een positieve aanpassing met de overeenkomstige hoeveelheid te boeken. De oorspronkelijke negatieve post met een vaste vereffening wordt gesloten.  
2.  Gebruik het veld **Vereffenen van post** om een negatieve vereffening te boeken. De oorspronkelijke positieve correctiepost met een vaste vereffening wordt gesloten.  

## <a name="see-also"></a>Zie ook  
[Artikelposten verwijderen en opnieuw toepassen](finance-how-to-remove-and-reapply-item-entries.md)  
 [Verkoopretouren en annuleringen verwerken](sales-how-process-sales-returns-cancellations.md)   
 [Voorraadwaardering en kostprijsberekening instellen](finance-set-up-inventory-valuation-and-costing.md)   
 [Voorraadkosten beheren](finance-manage-inventory-costs.md)   
 [Ontwerpdetails: Waarderingsmethoden](design-details-costing-methods.md)
