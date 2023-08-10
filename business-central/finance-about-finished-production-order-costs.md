---
title: Over de kosten van de gereedgemelde productieorder
description: Het voltooien van de productieorder is de sleutel tot het voltooien van de levenscyclus van een productieartikel. De uiteindelijke kosten worden berekend in de batchverwerking Kostprijs herwaarderen - Artikelposten.
author: SorenGP
ms.topic: conceptual
ms.search.form: 99000867
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="about-finished-production-order-costs"></a>Over de kosten van de gereedgemelde productieorder

Het gereedmelden van de productieorder is een belangrijke taak in het voltooien van de levenscyclus van de waardering van het artikel dat wordt geproduceerd. De uiteindelijke kosten (inclusief verschillen in een standaard waarderingsomgeving; werkelijke kosten in een FIFO, gemiddelde, of LIFO waarderingsomgeving) worden berekend met behulp van de batchverwerking **Kostprijs herwaarderen - Artikelposten**, die voorziet in financiële reconciliatie van de kostprijzen van artikelproductie. Een productieorder kan alleen in aanmerking komen voor kostenwaardering als de status **Gereedgemeld** is. Het is daarom van groot belang dat na voltooiing de status van een productieorder wordt gewijzigd in **Gereedgemeld**.  

## <a name="example"></a>Opmerking

Als u in een omgeving met vaste verrekenprijzen materiaal verbruikt voor het produceren van een artikel, worden de kosten van het artikel plus arbeid en overhead simpelweg naar OHW overgebracht. Wanneer het item wordt geproduceerd, wordt OHW verminderd met het bedrag van de vaste verrekenprijs van het artikel. Gewoonlijk is het saldo hiervan niet nul. Om met deze kosten op nul uit te komen, moet u de batchverwerking **Kostprijs herwaarderen - Artikelposten** uitvoeren, waarbij u erop moet letten dat alleen productieorders met de status **Gereedgemeld** in aanmerking komen voor herwaardering.  

## <a name="see-also"></a>Zie ook

[Voorraadkosten beheren](finance-manage-inventory-costs.md)  
[Productie](production-manage-manufacturing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
