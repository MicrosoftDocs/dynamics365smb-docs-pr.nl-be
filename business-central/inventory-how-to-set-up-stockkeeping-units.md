---
title: SKU's instellen
description: In SKU's kunt u gegevens opnemen over de artikelen voor een bepaalde vestiging of een bepaalde variantcode.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.forms: '5704, 5700, 5702, 5701'
ms.date: 04/01/2021
ms.author: edupont
---
# SKU's instellen

U kunt SKU's gebruiken om gegevens op te nemen over artikelen voor een bepaalde vestiging of een bepaalde variantcode.  

SKU's zijn een aanvulling op de artikelkaarten. Ze vervangen ze niet, hoewel ze wel zijn gekoppeld. Met SKU's kunt u voor een bepaald artikel onderscheid maken tussen gegevens betreffende een bepaalde vestiging (bijvoorbeeld een magazijn of distributiecentrum) of een bepaalde variant (bijvoorbeeld verschillende opslaglocatienummers of aanvullingsgegevens).  

## SKU's instellen  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **SKU's** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Nieuw**.  
3.  Vul de velden op de kaart in. De volgende velden zijn vereist: **Artikelnr.**, **Vestigingscode** en/of **variantcode**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Als u de eerste SKU voor een artikel hebt ingesteld, wordt het selectievakje **SKU bestaat** op de kaart **Artikel** ingeschakeld.  

Als u meerdere SKU's voor een artikel wilt maken, kunt u de batchverwerking **SKU maken** gebruiken.  

> [!NOTE]  
>  De gegevens op de **SKU**-kaart hebben voorrang op de gegevens op de **artikelkaart**.

> [!Warning]
> Wanneer de SKU wordt geleverd via productie, wordt het veld **Vaste verrekenprijs** niet gebruikt bij de facturering en de berekening van de werkelijke kosten van een geproduceerd artikel. In plaats daarvan wordt het veld **Vaste verrekenprijs** van de onderliggende artikelkaart gebruikt en worden eventuele afwijkingen berekend tegen het kostenaandeel van dat artikel.<br /><br />
> Omdat productiestuklijsten en routering niet kunnen worden toegewezen aan SKU´s, zijn de berekening van kosten per eenheid en de bijbehorende berekening van het kostenaandeel ook niet beschikbaar voor SKU's. Zie [Vaste verrekenprijs berekenen](finance-about-calculating-standard-cost.md) voor nadere informatie

## Zie gerelateerde [Microsoft-training](/training/modules/control-inventory-multiple-locations/)

## Zie ook

[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Voorraad](inventory-manage-inventory.md)  
[Assemblagebeheer](assembly-assemble-items.md)    
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
