---
title: Artikelfamilies gebruiken in productie | Microsoft Docs
description: De belangrijkste taak bij het aanpassen van een basisagenda voor uw bedrijf of voor een van uw zakelijke partners is het invoeren van wijzigingen in de statuswaarden Werkdag en Vrije dag.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f33ac3e581325eb714af67ee7040157a61e59fc7
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758879"
---
# <a name="work-with-production-families"></a>Werken met productfamilies
Een productfamilie is een verzameling afzonderlijke artikelen die vanwege een vergelijkbaar productieproces onderling gerelateerd zijn. Door de vorming van productfamilies kunnen sommige artikelen twee keer of vaker worden geproduceerd tijdens één verwerking, wat het materiaalverbruik optimaliseert.

In het veld **Aantal** van de pagina **Familie** voert u het aantal in dat wordt geproduceerd nadat de hele familie één keer is geproduceerd.

## <a name="example"></a>Opmerking
Bij een stansproces kunnen uit één vel tegelijkertijd vier stuks van het ene artikel en tien stuks van een ander artikel worden geproduceerd. De stansmachine produceert de veertien stuks in één stap.

Wanneer u productfamilies vormt, vermindert u de uitvalhoeveelheid. Wat bij de productie van grote artikelen doorgaans wordt beschouwd als uitval, wordt nu gebruikt voor de productie van kleinere artikelen.

## <a name="to-set-up-a-production-family"></a>Een productfamilie instellen
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Productfamilies** in en kies de gerelateerde koppeling.
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-family"></a>Produceren op basis van een productfamilie
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vast geplande productieorders** in en kies de gerelateerde koppeling.
2. Maak een nieuwe productieorder. Zie voor meer informatie [Productieorders maken](production-how-to-create-production-orders.md).
3. Selecteer in het veld **Brontype** de optie **Familie**.  
4. Selecteer de relevante productfamilie in het veld **Bronnr.**

## <a name="see-also"></a>Zie ook
[Productiestuklijsten maken](production-how-to-create-production-boms.md)  
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)    
[Gepland](production-planning.md)   
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
