---
title: Artikelfamilies gebruiken in productie | Microsoft Docs
description: De belangrijkste taak bij het aanpassen van een basisagenda voor uw bedrijf of voor een van uw zakelijke partners is het invoeren van wijzigingen in de statuswaarden Werkdag en Vrije dag.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/05/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2e76520cdab388d3430ea50fb8e88f7dce26715a
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-production-families"></a>Werken met productfamilies
Een productfamilie is een verzameling afzonderlijke artikelen die vanwege een vergelijkbaar productieproces onderling gerelateerd zijn. Door de vorming van productfamilies kunnen sommige artikelen twee keer of vaker worden geproduceerd tijdens één verwerking, wat het materiaalverbruik optimaliseert.

In het veld **Aantal** van het venster **Familie** voert u het aantal in dat wordt geproduceerd nadat de hele familie één keer is geproduceerd.

## <a name="example"></a>Opmerking
Bij een stansproces kunnen uit één vel tegelijkertijd vier stuks van het ene artikel en tien stuks van een ander artikel worden geproduceerd. De stansmachine produceert de veertien stuks in één stap.

Wanneer u productfamilies vormt, vermindert u de uitvalhoeveelheid. Wat bij de productie van grote artikelen doorgaans wordt beschouwd als uitval, wordt nu gebruikt voor de productie van kleinere artikelen.

## <a name="to-set-up-a-production-family"></a>Een productfamilie instellen
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Families** in en klik vervolgens op de gerelateerde koppeling.
2. Vul de velden in. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-familily"></a>Produceren op basis van een productfamilie
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Vast geplande productieorders** in en klik op de gerelateerde koppeling.
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
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

