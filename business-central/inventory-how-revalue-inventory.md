---
title: Nieuwe waardeposten maken voor artikelen in de voorraad| Microsoft Docs
description: Beschrijft hoe u de waardeposten vermeerdert of vermindert van een of meer artikelen in de voorraad door de huidige, berekende waarde ervan te boeken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 2bcd09876f18bb948e060b06199d3d36facaa83f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750067"
---
# <a name="revalue-inventory"></a>Voorraad herwaarderen
Gebruik het herwaarderingsdagboek als u de voorraadwaarde van een artikel of een bepaalde artikelpost wilt vermeerderen of verminderen.

## <a name="to-revalue-inventory"></a>Voorraad herwaarderen
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Herwaarderingsdagboek** in en kies de gerelateerde koppeling.
2. Kies de actie **Voorraadwaarde berekenen**.
3. Vul op de pagina **Voorraadwaarde berekenen** indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Kies de knop **OK**.
5. Voer op elke regel op de pagina **Herwaarderingsdagboek** het veld **Kostprijs (Geherwaardeerd)** in en voer de nieuwe eenheidskosten in. U kunt ook het nieuwe totale bedrag in het veld **Voorraadwaarde (Geherwaardeerd)** invoeren.

    De bijbehorende velden worden automatisch bijgewerkt. In het veld **Bedrag** wordt de werkelijke wijziging in de voorraadwaarde voor de geselecteerde artikelpost weergegeven. Het verschil tussen de waarden in de velden **Voorraadwaarde (Berekend)** en **Voorraadwaarde (Geherwaardeerd)** wordt berekend.
6. Wanneer u alle regels in het herwaarderingsdagboek hebt ingevuld, kiest u de actie **Boeken**.

Nieuwe waardeposten worden nu gemaakt om de herwaarderingen weer te geven die u hebt geboekt. U kunt de nieuwe waarden op de desbetreffende artikelkaarten bekijken.

## <a name="see-also"></a>Zie ook
[Ontwerpdetails: Herwaardering](design-details-revaluation.md)  
[Voorraad](inventory-manage-inventory.md)  
[Verkoop](sales-manage-sales.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]