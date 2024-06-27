---
title: SKU's instellen
description: Gebruik SKU's om gegevens op te nemen over uw artikelen voor een bepaalde vestiging of een bepaalde variant.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 06/10/2024
ms.custom: bap-template
ms.search.forms: '5704, 5700, 5702, 5701'
ms.service: dynamics-365-business-central
---

# <a name="set-up-stock-keeping-units"></a>SKU's instellen

Gebruik SKU's om gegevens op te nemen over artikelen voor een bepaalde vestiging of variant. Hiermee kunt u verschillende informatie over een artikel voor een specifieke vestiging toevoegen, bijvoorbeeld:

* Een magazijn of distributiecentrum
* Varianten, zoals verschillende schapnummers en verschillende aanvullingsinformatie, voor hetzelfde artikel  

## <a name="to-set-up-a-sku"></a>Een SKU instellen

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **SKU's** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Vul de vereiste velden in. De volgende velden zijn vereist: **Artikelnr.**, **Vestigingscode** en/of **variantcode**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Nadat u de eerste SKU voor een artikel hebt ingesteld, wordt het selectievakje **SKU bestaat** op de kaart **Artikel** ingeschakeld.  

Als u meerdere SKU's voor een artikel wilt maken, kunt u de batchverwerking **SKU maken** gebruiken. Lees meer over batchverwerking op [Taakwachtrijen gebruiken om taken te plannen](admin-job-queues-schedule-tasks.md).  

> [!NOTE]  
> De gegevens op de **SKU**-kaart hebben voorrang op de gegevens op de **artikelkaart**.

> [!Warning]
> Wanneer de SKU wordt geleverd via productie, wordt het veld **Vaste verrekenprijs** niet gebruikt bij de facturering en de berekening van de werkelijke kosten van het geproduceerde artikel. In plaats daarvan gebruikt [!INCLUDE [prod_short](includes/prod_short.md)] de waarde in het veld **Vaste verrekenprijs** van de artikelkaart en worden eventuele afwijkingen berekend tegen het kostenaandeel van dat artikel.<br><br>
> Hoewel u productiestuklijsten en bewerkingsplannen aan SKU's kunt toewijzen, zijn de berekening van kosten per eenheid en de bijbehorende berekening van het kostenaandeel niet beschikbaar voor SKU's. Ga voor meer informatie over vaste verrekenprijzen naar [Informatie over het berekenen van vaste verrekenprijzen](finance-about-calculating-standard-cost.md)

## <a name="see-also"></a>Zie ook

[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Voorraad](inventory-manage-inventory.md)  
[Assemblagebeheer](assembly-assemble-items.md)    
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
