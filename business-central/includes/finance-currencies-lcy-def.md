---
author: brentholtorf
ms.topic: include
ms.date: 03/15/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
Aangezien bedrijven steeds vaker in andere landen/regio's opereren, is het belangrijk dat zij kunnen handelen en de financiële gegevens kunnen controleren en rapporteren in meer dan één valuta. De lokale valuta (LV) wordt gedefinieerd op de pagina **Grootboekinstellingen** zoals beschreven in het artikel [Het grootboek en het rekeningschema begrijpen](../finance-general-ledger.md). Zodra de lokale valuta (LV) is gedefinieerd, wordt deze weergegeven als een blanco valuta, dus wanneer het veld **Valuta** leeg is, betekent dit dat de valuta LV is.  

Vervolgens moet u valutacodes instellen voor elke valuta die u gebruikt als u koopt of verkoopt in andere valuta's dan uw lokale valuta (LV). Ook kunnen bankrekeningen worden gemaakt met valuta. Het is mogelijk om grootboektransacties in verschillende valuta's vast te leggen, maar de grootboektransactie wordt altijd geboekt in de lokale valuta (LV).

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

Uw grootboek is ingesteld om uw lokale valuta (LV) te gebruiken, maar u kunt het ook instellen om een andere valuta te gebruiken, waaraan een valutawisselkoers is toegewezen. Door een tweede valuta in te stellen als een zogenaamde extra rapportagevaluta, legt [!INCLUDE[prod_short](prod_short.md)] bedragen automatisch vast in zowel de LV als deze extra rapportagevaluta voor elke grootboekpost en andere posten, zoals btw-posten. Zie [Een extra rapportagevaluta instellen](../finance-how-setup-additional-currencies.md) voor meer informatie. De aanvullende rapportagevaluta wordt meestal gebruikt om financiële rapportage te vergemakkelijken voor eigenaren die woonachtig zijn in landen/regio's die andere valuta's gebruiken dan de lokale valuta (LV).  

> [!IMPORTANT]
> Als u een extra rapportagevaluta wilt gebruiken voor financiële rapportage, zorg er dan voor dat u de beperkingen begrijpt. Zie [Een extra rapportagevaluta instellen](../finance-how-setup-additional-currencies.md) voor meer informatie.

> [!NOTE]  
> Wanneer u met een valutacode naar het grootboek boekt, bijvoorbeeld om een uitgave in een dagboek te boeken met een valutacode, wordt de transactie geconverteerd naar LV met behulp van de valutakoers voor de boekingsdatum. De grootboekpost bevat geen informatie over welke valuta is gebruikt, alleen de waarde in LV. Als u de oorspronkelijke valuta wilt bijhouden, bijvoorbeeld voor een factuur, moet u de verkoop- en inkoopdocumenten gebruiken, evenals bankrekeningen die informatie over de valutacode voor de posten opslaan.
