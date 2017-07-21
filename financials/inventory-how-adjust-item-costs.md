---
title: Artikelkosten handmatig herwaarderen| Microsoft Docs
description: U kunt de voorraadwaarde van een artikel herwaarderen met de waarderingsmethoden FIFO of Gemiddeld, bijvoorbeeld als de kosten van een artikel veranderen om andere redenen dan transacties.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost adjustment, cost forwarding, costing method, inventory valuation, costing
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a1f682b60b7b9ae402c27093f13aa3db2368ed5b
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-adjust-item-costs-manually"></a>Procedure: Artikelkosten handmatig herwaarderen
De kostprijs van een artikel (voorraadwaarde) dat u inkoopt en later verkoopt, kan tijdens de levensduur veranderen, bijvoorbeeld omdat vrachtkosten worden toegevoegd aan aanschafkosten nadat u het artikel hebt verkocht. Kostenherwaardering is met name belangrijk als u goederen verkoopt voordat u de inkoop van deze goederen factureert. Als u altijd de juiste voorraadwaarde wilt weten, moeten artikelkosten daarom regelmatig worden geherwaardeerd. Hierdoor worden verkoop- en winststatistieken bijgewerkt en gezorgd dat de financiële KPI's kloppen.

In [!INCLUDE[d365fin](includes/d365fin_md.md)] worden artikelkosten automatisch aangepast steeds wanneer een voorraadtransactie plaatsvindt, zoals bij het boeken van een inkoopfactuur voor een artikel.

U kunt een functie ook gebruiken om de kosten van een of meer artikelen handmatig aan te passen. Dit is bijvoorbeeld handig als u weet dat artikelkosten om andere redenen dan artikeltransacties zijn gewijzigd.

Artikelkosten worden geherwaardeerd door de waarderingsmethode FIFO of Gemiddeld, afhankelijk van uw keuze in de begeleide instelling **Mijn bedrijf instellen**. Zie voor meer informatie [Voorbereid zijn om zaken te doen](ui-get-ready-business.md).  

Als u de waarderingsmethode FIFO gebruikt, zijn de eenheidskosten van een artikel de werkelijke waarde van een ontvangst van het artikel. Voorraad wordt gewaardeerd met de aanname dat de eerste in voorraad geplaatste artikelen het eerst worden verkocht.

Als u de waarderingsmethode Gemiddeld gebruikt, worden de eenheidskosten van een artikel berekend als de gemiddelde eenheidskosten op een bepaald moment na een aanschaf. Voorraad wordt gewaardeerd met de aanname dat alle voorraad tegelijkertijd wordt verkocht.

De kostenherwaardering verwerkt alleen posten die nog niet zijn geherwaardeerd. Als de functie een post aantreft waarbij gewijzigde inkomende kosten moeten worden doorgeschoven naar de bijbehorende uitgaande posten, worden nieuwe waardeposten gemaakt. Deze posten zijn op de gegevens van de oorspronkelijke waardeposten gebaseerd, maar bevatten het geherwaardeerde bedrag. De kostenherwaarderingsfunctie gebruikt de boekingsdatum van de oorspronkelijke waardepost in de herwaarderingspost, tenzij die datum in een afgesloten voorraadperiode valt. In dat geval wordt de begindatum van de volgende open voorraadperiode gehanteerd. Als de voorraadperioden niet worden gebruikt, bepaalt de datum in het veld **Boeken toegest. vanaf** in het venster **Boekhoudinstellingen** wanneer de herwaarderingspost wordt geboekt.

Wijzigingen in voorraadwaarde van handel worden automatisch met uw financiële boeken afgestemd wanneer u artikeltransacties boekt. Zie de sectie "Voorraadreconciliatie" in [Voorraad](inventory-manage-inventory.md).

## <a name="to-adjust-item-costs-manually"></a>Artikelkosten handmatig herwaarderen
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Kostprijs herwaarderen - Artikelposten** in en kies vervolgens de gerelateerde koppeling.
2. Geef in het venster **Kostprijs herwaarderen - Artikelposten** op voor welke artikelen kosten moeten worden aangepast.
3. Kies de knop **OK**.

## <a name="see-also"></a>Zie ook
[Voorraad](inventory-manage-inventory.md)  
[Verkoop](sales-manage-sales.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

