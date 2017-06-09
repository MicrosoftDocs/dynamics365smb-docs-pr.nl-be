---
title: 'Procedure: Artikelkosten handmatig herwaarderen| Microsoft Docs'
description: 'Procedure: Artikelkosten herwaarderen'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost adjustment, cost forwarding, costing method, inventory valuation, costing
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 00b5ac40bd0d3df346618b57173df67daba6c7fc
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-adjust-item-costs-manually"></a>Procedure: Artikelkosten handmatig herwaarderen
De kostprijs van een artikel (voorraadwaarde) dat u inkoopt en later verkoopt, kan tijdens de levensduur veranderen, bijvoorbeeld omdat vrachtkosten worden toegevoegd aan aanschafkosten nadat u het artikel hebt verkocht. Kostenherwaardering is met name belangrijk als u goederen verkoopt voordat u de inkoop van deze goederen factureert. Als u altijd de juiste voorraadwaarde wilt weten, moeten artikelkosten daarom regelmatig worden geherwaardeerd. Hierdoor worden verkoop- en winststatistieken bijgewerkt en gezorgd dat de financiële KPI's kloppen.

In [!INCLUDE[d365fin](includes/d365fin_md.md)] worden artikelkosten automatisch aangepast steeds wanneer een voorraadtransactie plaatsvindt, zoals bij het boeken van een inkoopfactuur voor een artikel.

U kunt een functie ook gebruiken om de kosten van een of meer artikelen handmatig aan te passen. Dit is bijvoorbeeld handig als u weet dat artikelkosten om andere redenen dan artikeltransacties zijn gewijzigd.

**Opmerking**: artikelkosten worden alleen aangepast door de waarderingsmethode FIFO. Dit betekent dat de kostprijs van een artikel de werkelijke waarden van de ontvangst van het artikel is, en dat de voorraad wordt gewaardeerd op basis van de aanname dat artikelen die het eerst in voorraad zijn geplaatst, het eerst worden verkocht.

De kostenherwaardering verwerkt alleen posten die nog niet zijn geherwaardeerd. Als de functie een post aantreft waarbij gewijzigde inkomende kosten moeten worden doorgeschoven naar de bijbehorende uitgaande posten, worden nieuwe waardeposten gemaakt. Deze posten zijn op de gegevens van de oorspronkelijke waardeposten gebaseerd, maar bevatten het geherwaardeerde bedrag. De kostenherwaarderingsfunctie gebruikt de boekingsdatum van de oorspronkelijke waardepost in de herwaarderingspost, tenzij die datum in een afgesloten voorraadperiode valt. In dat geval wordt de begindatum van de volgende open voorraadperiode gehanteerd. Als de voorraadperioden niet worden gebruikt, bepaalt de datum in het veld **Boeken toegest. vanaf** in het venster **Boekhoudinstellingen** wanneer de herwaarderingspost wordt geboekt.

Wijzigingen in voorraadwaarde van handel worden automatisch met uw financiële boeken afgestemd wanneer u artikeltransacties boekt. Zie [Geavanceerd: Voorraadreconciliatie](advanced-inventory-reconciliation.md) voor meer informatie.

## <a name="to-adjust-item-costs-manually"></a>Artikelkosten handmatig herwaarderen
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Kostprijs herwaarderen - Artikelposten** in en kies vervolgens de gerelateerde koppeling.
2. Geef in het venster **Kostprijs herwaarderen - Artikelposten** op voor welke artikelen kosten moeten worden aangepast.
3. Kies de knop **Ok**.

## <a name="see-also"></a>Zie ook
[Geavanceerd: Voorraadreconciliatie](advanced-inventory-reconciliation.md)  
[Voorraad](inventory-manage-inventory.md)  
[Verkoop](sales-manage-sales.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

