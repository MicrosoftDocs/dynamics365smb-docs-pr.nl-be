---
title: Productieorderkoppen maken | Microsoft Docs
description: U kunt een productieorder handmatig maken. De eerste stap is het maken van een productieorderkop.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0c792dbb7d7261e8f8b89ca4f3d39d875142c4eb
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-production-order-headers"></a>Procedure: productieorderkoppen maken
U kunt een productieorder handmatig maken. De eerste stap is het maken van een productieorderkop.

Productieorders worden meestal automatisch op basis van een planningsfunctie gemaakt om te voldoen aan een bekende vraag. Zie [Planning](production-planning.md) voor meer informatie.   

In de volgende procedure wordt een vast geplande productieorder gemaakt. U kunt ook productieorders maken met een andere status.  

## <a name="to-create-a-production-order-header"></a>Productieorderkoppen maken  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Vast geplande productieorders** in en klik op de gerelateerde koppeling.  
2.  Kies de actie **Nieuw**.  
3.  Selecteer in het veld **Nr.** het volgende nummer uit de reeks in.  
4.  Selecteer in het veld **Bronsoort** de bron van de productieorder.

    Hier kunt u opgeven of er voor een familie van artikelen moet worden geproduceerd. Zie [Procedure: Werken met productfamilies](production-how-work-family.md) voor meer informatie.
5.  Selecteer in het veld **Bronnr.** het artikelnummer, de productfamilie of de verkoopkop waarvoor de productieorder moet worden gegenereerd.  
6.  Vul de velden **Aantal** en **Vervaldatum** in op basis van de specificaties.  

Wanneer productievereisten veranderen, bijvoorbeeld onderdelen of bewerkingen, kunt u de productieorder snel herplannen. Zie [Procedure: Productieorders direct opnieuw plannen of vernieuwen](production-how-to-replan-refresh-production-orders.md) voor meer informatie. 

## <a name="see-also"></a>Zie ook  
[Productie](production-manage-manufacturing.md)    
[Productie instellen](production-configure-production-processes.md)  
[Gepland](production-planning.md)      
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

