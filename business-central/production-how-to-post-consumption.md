---
title: Verbruik in batches boeken | Microsoft Docs
description: Als de afboekingsmethode **Handmatig** is, moet u de materialen handmatig boeken met behulp van een verbruiksdagboek.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: b7799e652394e8b9b96a168c0cb8945ec332734e
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816384"
---
# <a name="batch-post-production-consumption"></a>Productieverbruik in batches boeken
Als de afboekingsmethode **Handmatig** is, moet u de materialen handmatig boeken met behulp van een verbruiksdagboek.

U kunt het systeem ook zo instellen materialen automatisch worden geboekt (*afgeboekt**) als u productieorders start of voltooit. Zie voor meer informatie [Afboeking van materialen op basis van de uitvoer van een bewerking inschakelen](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Verbruik boeken voor een of meer productieorderregels  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verbruiksdagboek** in en kies vervolgens de gerelateerde koppeling.  
2.  Voer in de velden informatie over de productieorder en verbruik in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Als het magazijn waar de materialen zijn opgeslagen opslaglocaties gebruikt, maar geen pickverwerking vereist, kunt u een opslaglocatie toewijzen aan de dagboekregel om aan te geven waar de artikelen uit het magazijn moeten worden gehaald. Zie [Picken voor productie of assemblage](warehouse-how-to-pick-for-production.md) voor meer informatie.  
3.  Kies de actie **Boeken** om het verbruik te boeken. De betreffende artikelposten worden verminderd.

## <a name="see-also"></a>Zie ook  
[Productie](production-manage-manufacturing.md)    
[Productie instellen](production-configure-production-processes.md)  
[Gepland](production-planning.md)      
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
