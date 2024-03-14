---
author: brentholtorf
ms.topic: include
ms.date: 03/04/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
Als uw bedrijf in meer dan één land of regio actief is, is het waarschijnlijk belangrijk dat u in meer dan één valuta zaken kunt doen. U definieert uw lokale valuta (LV) op de pagina **Grootboekinstellingen**. Daarna wordt uw lokale valuta weergegeven als een blanco valuta op documenten en transacties. Als het veld **Valuta** leeg is, is de valuta LV.

In de volgende video wordt uitgelegd hoe u uw lokale valuta instelt.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1iM1n]

Vervolgens moet u valutacodes instellen voor elke valuta die u gebruikt als u koopt of verkoopt in andere valuta's dan uw lokale valuta (LV). Ook kunnen bankrekeningen worden gemaakt met valuta. Het is mogelijk om grootboektransacties in verschillende valuta's vast te leggen, maar de grootboektransactie wordt altijd geboekt in de lokale valuta (LV).

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

Uw grootboek is ingesteld om uw lokale valuta (LV) te gebruiken, maar u kunt het ook instellen om een andere valuta te gebruiken, waaraan een valutawisselkoers is toegewezen. Door een tweede valuta in te stellen als een zogenaamde extra rapportagevaluta, legt [!INCLUDE[prod_short](prod_short.md)] bedragen automatisch vast in zowel de LV als deze extra rapportagevaluta voor grootboekposten en andere posten, zoals btw-posten. Zie [Een extra rapportagevaluta instellen](../finance-how-setup-additional-currencies.md) voor meer informatie. De aanvullende rapportagevaluta wordt meestal gebruikt om financiële rapportage te vergemakkelijken voor eigenaren die woonachtig zijn in landen/regio's die andere valuta's gebruiken dan de lokale valuta (LV).  

> [!IMPORTANT]
> Als u een extra rapportagevaluta wilt gebruiken voor financiële rapportage, zorg er dan voor dat u de beperkingen begrijpt. Zie [Een extra rapportagevaluta instellen](../finance-how-setup-additional-currencies.md) voor meer informatie.

> [!NOTE]  
> Wanneer u naar het grootboek boekt met een vreemde valuta, [!INCLUDE [prod_short](prod_short.md)] wordt de transactie naar LV geconverteerd op basis van de wisselkoers van de boekingsdatum. De grootboekpost bevat geen informatie over welke valuta is gebruikt, alleen de waarde in LV. Om de oorspronkelijke valuta bij te houden, gebruikt u de verkoop- en inkoopdocumenten en bankrekeningen waarop valuta-informatie voor posten wordt opgeslagen.
