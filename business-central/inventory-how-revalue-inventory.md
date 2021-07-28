---
title: Nieuwe waardeposten maken voor artikelen in de voorraad| Microsoft Docs
description: Beschrijft hoe u de waardeposten vermeerdert of vermindert van een of meer artikelen in de voorraad door de huidige, berekende waarde ervan te boeken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 01710b23c56634b91b86f3f1c6e6c87415a787c6
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435609"
---
# <a name="revalue-inventory"></a>Voorraad herwaarderen
Gebruik het herwaarderingsdagboek als u de voorraadwaarde van een artikel of een bepaalde artikelpost wilt vermeerderen of verminderen.

## <a name="to-revalue-inventory"></a>Voorraad herwaarderen
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Herwaarderingsdagboek** in en kies vervolgens de gerelateerde koppeling.
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