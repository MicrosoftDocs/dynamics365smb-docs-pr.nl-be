---
author: brentholtorf
ms.topic: include
ms.date: 03/15/2022
ms.author: bholtorf
---
Wanneer u een factuur van een bedrijf in een vreemde valuta ontvangt, is het vrij eenvoudig om de LV-waarde van de factuur te berekenen op basis van de huidige valutakoers. De factuur wordt echter vaak geleverd met betalingsvoorwaarden, zodat u de betaling kunt uitstellen naar een latere datum, wat een mogelijk andere valutakoers impliceert. Dit probleem in combinatie met het feit dat de bankvaluta's altijd verschillen van de officiële valutakoersen, maakt het onmogelijk om het exacte bedrag in lokale valuta (LV) te voorspellen dat nodig is om de factuur te dekken. Als de vervaldatum van de factuur zich uitstrekt tot de volgende maand, moet u mogelijk ook het bedrag in lokale valuta (LV) aan het einde van de maand herwaarderen. De valutacorrectie is nodig omdat de nieuwe LV-waarde die nodig is om het factuurbedrag te dekken mogelijk anders is en de bedrijfsschuld aan de leverancier mogelijk is gewijzigd. Het nieuwe LV-bedrag kan hoger of lager zijn dan het vorige bedrag en zal daarom een winst of een verlies vertegenwoordigen. Aangezien de factuur echter nog niet is betaald, wordt de winst of het verlies beschouwd als *niet gerealiseerd*. Later wordt de factuur betaald en komt de bank met de werkelijke valutakoers voor de betaling. Nu pas wordt de *gerealiseerde* winst of verlies berekend. Deze niet-gerealiseerde winst of verlies wordt vervolgens teruggeboekt en in plaats daarvan wordt de gerealiseerde winst of het gerealiseerde verlies geboekt.

In het volgende voorbeeld wordt op 1 januari een factuur ontvangen met het valutabedrag 1000. Op dat moment is de wisselkoers 1,123.

|Datum|Actie|Valutabedrag|Documentkoers|LV-bedrag in document|Vereffeningskoers|Ongerealiseerd winstbedrag|Betalingskoers|Gerealiseerd verliesbedrag|  
|-----|----------|------------|-----------|---------|-----------|-------------|---------|---------|
|1/1|**Factuur**|1000|1,123|1123|||||
|1/31|**Herwaardering**|1000||1125|1,125|2|||
|2/15|**Herwaarderingsterugboeking bij betaling**|1000||||-2|||
|2/15|**Betaling**|1000||1120|||1,120|-3|

Aan het einde van de maand wordt een valuta-aanpassing uitgevoerd waarbij de aanpassingsvalutakoers is ingesteld op 1,125, wat een niet-gerealiseerde winst van 2 veroorzaakt.

Op het moment van betaling toont de werkelijke valutakoers die is geregistreerd voor de banktransactie, een valutakoers van 1,120.

Hier is sprake van een niet-gerealiseerde transactie en het wordt daarom samen met de betaling teruggeboekt.

Ten slotte wordt de betaling geregistreerd en wordt het werkelijke verlies geboekt op de rekening voor gerealiseerde verliezen.
