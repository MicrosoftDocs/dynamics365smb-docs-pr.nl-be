---
title: Nieuwe waardeposten maken voor artikelen in de voorraad| Microsoft Docs
description: Beschrijft hoe u de waardeposten vermeerdert of vermindert van een of meer artikelen in de voorraad door de huidige, berekende waarde ervan te boeken.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: cfccd4f4ac6e2599ebc4b53b43163f4dfcc4d0ef
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-revalue-inventory"></a>Procedure: Voorraad herwaarderen
Gebruik het herwaarderingsdagboek als u de voorraadwaarde van een artikel of een bepaalde artikelpost wilt vermeerderen of verminderen.

## <a name="to-revalue-inventory"></a>Voorraad herwaarderen
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Herwaarderingsdagboek** in en klik vervolgens op de gerelateerde koppeling.
2. Kies de actie **Voorraadwaarde berekenen**.
3. Vul in het venster **Voorraadwaarde berekenen** indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Kies de knop **Ok**.
5. Voer op elke regel in het venster **Herwaarderingsdagboek** het veld **Kostprijs (Geherwaardeerd)** in en voer de nieuwe eenheidskosten in. U kunt ook het nieuwe totale bedrag in het veld **Voorraadwaarde (Geherwaardeerd)** invoeren.

    De bijbehorende velden worden automatisch bijgewerkt. In het veld **Bedrag** wordt de werkelijke wijziging in de voorraadwaarde voor de geselecteerde artikelpost weergegeven. Het verschil tussen de waarden in de velden **Voorraadwaarde (Berekend)** en **Voorraadwaarde (Geherwaardeerd)** wordt berekend.
6. Wanneer u alle regels in het herwaarderingsdagboek hebt ingevuld, kiest u de actie **Boeken**.

Nieuwe waardeposten worden nu gemaakt om de herwaarderingen weer te geven die u hebt geboekt. U kunt de nieuwe waarden op de desbetreffende artikelkaarten bekijken.

## <a name="see-also"></a>Zie ook
[Ontwerpdetails: Herwaardering](design-details-revaluation.md)  
[Voorraad](inventory-manage-inventory.md)  
[Verkoop](sales-manage-sales.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

