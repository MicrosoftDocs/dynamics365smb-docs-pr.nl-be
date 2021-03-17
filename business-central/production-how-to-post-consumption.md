---
title: Verbruik in batches boeken | Microsoft Docs
description: Als de afboekingsmethode **Handmatig** is, moet u de materialen handmatig boeken met behulp van een verbruiksdagboek.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0bf0a92d05b6c9ecb3d5a5ba054b4675680ad43c
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391811"
---
# <a name="batch-post-production-consumption"></a>Productieverbruik in batches boeken
Als de afboekingsmethode **Handmatig** is, moet u de materialen handmatig boeken met behulp van een verbruiksdagboek.

U kunt het systeem ook zo instellen materialen automatisch worden geboekt (*afgeboekt*) als u productieorders start of voltooit. Zie voor meer informatie [Afboeking van materialen op basis van de uitvoer van een bewerking inschakelen](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Verbruik boeken voor een of meer productieorderregels  
1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verbruiksdagboek** in en kies de desbetreffende koppeling.  
2.  Voer in de velden informatie over de productieorder en verbruik in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Als het magazijn waar de materialen zijn opgeslagen opslaglocaties gebruikt, maar geen pickverwerking vereist, kunt u een opslaglocatie toewijzen aan de dagboekregel om aan te geven waar de artikelen uit het magazijn moeten worden gehaald. Zie [Picken voor productie of assemblage](warehouse-how-to-pick-for-production.md) voor meer informatie.  
3.  Kies de actie **Boeken** om het verbruik te boeken. De betreffende artikelposten worden verminderd.

## <a name="see-also"></a>Zie ook  
[Productie](production-manage-manufacturing.md)    
[Productie instellen](production-configure-production-processes.md)  
[Gepland](production-planning.md)      
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]