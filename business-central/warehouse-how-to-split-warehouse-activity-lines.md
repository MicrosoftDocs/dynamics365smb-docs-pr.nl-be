---
title: Magazijnactiviteitsregels splitsen
description: Lees hoe u magazijnactiviteitsregels kunt splitsen als de beschikbare capaciteit in een voorgestelde opslaglocatie niet voldoende is.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '931, 9314, 9313, 9315, 9330'
---
# <a name="split-warehouse-activity-lines"></a>Magazijnactiviteitsregels splitsen

Voor magazijnopslag en magazijnverplaatsingen of -picks en voor voorraadopslag en voorraadpicks worden opslaglocaties voorgesteld voor het opslaan en picken van artikelen. Het werkelijke aantal artikelen in de voorgestelde opslaglocatie is mogelijk onvoldoende of er is te weinig ruimte in de opslaglocatie om het vereiste aantal op te slaan. Als dat het geval is, kunt u de desbetreffende regel splitsen, zodat de artikelen voor de regel in meerdere opslaglocaties worden geplaatst of uit meerdere opslaglocaties worden gepickt.  

De volgende procedure is van toepassing op de volgende magazijndocumenten:

* Magazijnopslag
* Magazijnverplaatsingen
* Magazijnpicks
* Voorraadopslag
* Voorraadverplaatsingen
* Voorraadpicks  

## <a name="to-split-warehouse-activity-lines"></a>Magazijnactiviteitsregels splitsen

1. Open een magazijnactiviteitsregel waar u probeert een ontoereikend aantal te verwerken.  
2. Voer in het veld **Te verwerken aantal** het verlaagde aantal in dat u kunt verwerken.  
3. Kies op het sneltabblad **Regels** de actie **Acties**, kies **Functies** en kies vervolgens **Regel splitsen**. Er wordt een nieuwe regel weergegeven. Dit is een kopie van de oorspronkelijke regel, met uitzondering van het veld **Te verwerken aantal**, dat het aantal bevat dat u uit de oorspronkelijke regel hebt verwijderd.  
4. Wijs een opslaglocatie en een zone toe, als u met gestuurde opslag en pick werkt, of blijf de regel splitsen tot u het volledige aantal artikelen over verschillende opslaglocaties hebt verdeeld.  

> [!NOTE]  
> Als voor de vestiging gestuurde opslag en pick is ingesteld en u regels splitst, moet u het magazijn kennen en een opslaglocatie kunnen kiezen die overeenkomt met de opslagvereisten van het desbetreffende artikel. De opslaglocatie moet bovendien voldoen aan de algemene vereisten van het magazijndocument. U zou bijvoorbeeld niet een regel op een pickdocument splitsen en enkele artikelen in bulk-opslag plaatsen.  

## <a name="see-also"></a>Zie ook

[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
