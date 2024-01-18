---
title: Artikelposten sluiten die afkomstig zijn van het gebruik van een vaste vereffening
description: Leer hoe u een vaste vereffening kunt gebruiken tussen een inkomende transactie en de oorspronkelijke uitgaande transactie te maken in het artikeldagboek.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 40
ms.date: 12/12/2023
ms.author: bholtorf
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a>Open artikelposten die uit een vaste vereffening in het artikeldagboek voortkomen sluiten

U kunt het veld **Vereffenen van post** op de pagina **Artikeldagboek** gebruiken om een vaste vereffening tussen een inkomende transactie en de oorspronkelijke uitgaande transactie te maken. Bijvoorbeeld om de uitgaande transactie te corrigeren of de retourzending te verwerken.  

> [!IMPORTANT]  
> Vaste vereffeningen die op deze manier worden uitgevoerd, worden alleen toegepast op de kosten, niet op de hoeveelheid. Bijgevolg sluit de geboekte positieve artikelpost niet de toegepaste uitgaande post en blijft deze zelf ook geopend. Dit geldt ook wanneer u een vaste vereffening voor een positieve post toepast op een negatieve post die niet is afgesloten door een gewone positieve post. In dat geval blijven de negatieve en de positieve posten geopend.  
>
> Dit betekent dat u een voorraadperiode waarin een dergelijke vermelding bestaat, niet kunt sluiten.  

U kunt vereffeningsposten in bepaalde omstandigheden wijzigen en opnieuw toepassen met de pagina **Vereffeningsvoorstel**.  

De volgende procedure laat zien hoe u dergelijke posten kunt sluiten door het uitvoeren van twee corrigerende boekingen in het artikeldagboek.  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a>Openstaande artikelposten die uit een vaste vereffening in het artikeldagboek voortkomen sluiten

1. Gebruik het veld **Vereffenen van post** om een positieve aanpassing met de overeenkomstige hoeveelheid te boeken. De oorspronkelijke negatieve post met een vaste vereffening wordt gesloten.  

    Met het veld **Vereffenen van post** wordt het nummer opgegeven van de uitgaande artikelpost waarvan de kosten worden doorgestuurd naar de inkomende artikelpost tijdens het boeken van een inkomende transactie van het type **Pos. correctie** of **Inkoop** naar het artikeldagboek.  
2. Gebruik het veld **Vereffenen van post** om een negatieve vereffening te boeken. De oorspronkelijke positieve correctiepost met een vaste vereffening wordt gesloten.  

    Met het veld **Vereffenen met post** wordt opgegeven of het aantal op de artikeldagboekregel moet worden vereffend met een reeds geboekt document. Als dat het geval is, voert u hier het nummer in van de artikelpost waarmee de artikeldagboekregel moet worden vereffend.

## <a name="see-also"></a>Zie ook

[Artikelposten verwijderen en opnieuw toepassen](finance-how-to-remove-and-reapply-item-entries.md)  
[Verkoopretouren en annuleringen verwerken](sales-how-process-sales-returns-cancellations.md)  
[Voorraadwaardering en kostprijsberekening instellen](finance-set-up-inventory-valuation-and-costing.md)  
[Voorraadkosten beheren](finance-manage-inventory-costs.md)  
[Ontwerpdetails: Waarderingsmethoden](design-details-costing-methods.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
