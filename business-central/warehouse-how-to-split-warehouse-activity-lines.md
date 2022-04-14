---
title: Magazijnactiviteitsregels splitsen
description: Lees hoe u magazijnactiviteitsregels kunt splitsen als de beschikbare capaciteit in een voorgestelde opslaglocatie niet voldoende is.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 4ef7003110c32cf498121dd8886acc710107d869
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8511314"
---
# <a name="split-warehouse-activity-lines"></a>Magazijnactiviteitsregels splitsen
Voor magazijnopslag en magazijnverplaatsingen of -picks en voor voorraadopslag en voorraadpicks worden opslaglocaties voorgesteld voor het opslaan en picken van artikelen. Het werkelijke aantal artikelen in de voorgestelde opslaglocatie is mogelijk onvoldoende of er is te weinig ruimte in de voorgestelde opslaglocatie om het vereiste aantal op te slaan. Als dat het geval is, moet u de desbetreffende regel splitsen, zodat de artikelen voor de regel in meerdere opslaglocaties worden geplaatst of uit meerdere opslaglocaties worden gepickt.  

De volgende procedure geldt voor magazijndocumenten, zoals magazijnopslag, -verplaatsing en -pickregels of voorraadopslag, -verplaatsing en -pickregels.  

## <a name="to-split-warehouse-activity-lines"></a>Magazijnactiviteitsregels splitsen  
1.  Open een magazijnactiviteitsregel waar u probeert een ontoereikend aantal te verwerken.  
2.  Voer in het veld **Te verwerken aantal** het verlaagde aantal in dat u kunt verwerken.  
3.  Kies op het sneltabblad **Regels** de actie **Acties**, kies **Functies** en kies vervolgens **Regel splitsen**. Er verschijnt een nieuwe regel. Dit is een kopie van de oorspronkelijke regel, met uitzondering van het veld **Te verwerken aantal**, dat het aantal bevat dat u uit de oorspronkelijke regel hebt verwijderd.  
4.  Wijs een opslaglocatie en een zone, als u met gestuurde opslag en pick werkt, aan deze nieuwe regel toe of blijf de regel splitsen tot u het volledige aantal artikelen over verschillende opslaglocaties hebt verdeeld.  

> [!NOTE]  
>  Als voor de vestiging gestuurde opslag en pick is ingesteld en u regels splitst, moet u het magazijn kennen en een opslaglocatie kunnen kiezen die overeenkomt met de opslagvereisten van het desbetreffende artikel. De opslaglocatie moet bovendien voldoen aan de algemene vereisten van het magazijndocument. U zou bijvoorbeeld niet een regel op een pickdocument splitsen en enkele artikelen in de bulk-opslag plaatsen.  

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]