---
title: SKU's instellen | Microsoft Docs
description: In SKU's kunt u gegevens opnemen over de artikelen voor een bepaalde vestiging of een bepaalde variantcode.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: c94a02cdbd658efcf96c5cff443ebfe03cb3feef
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3785908"
---
# <a name="set-up-stockkeeping-units"></a>SKU's instellen
In SKU's kunt u gegevens opnemen over de artikelen voor een bepaalde vestiging of een bepaalde variantcode.  

 SKU's zijn een aanvulling op de artikelkaarten. Ze vervangen ze niet, hoewel ze wel zijn gekoppeld. Met SKU's kunt u voor een bepaald artikel onderscheid maken tussen gegevens betreffende een bepaalde vestiging (bijvoorbeeld een magazijn of distributiecentrum) of een bepaalde variant (bijvoorbeeld verschillende opslaglocatienummers of aanvullingsgegevens).  

## <a name="to-set-up-a-stockkeeping-unit"></a>SKU's instellen  

1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **SKU's** in en kies de gerelateerde koppeling.  
2.  Kies de actie **Nieuw**.  
3.  Vul de velden op de kaart in. De volgende velden zijn vereist: **Artikelnr.**, **Vestigingscode** en/of **variantcode**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Als u de eerste SKU voor een artikel hebt ingesteld, wordt het selectievakje **SKU bestaat** op de kaart **Artikel** ingeschakeld.  

Als u meerdere SKU's voor een artikel wilt maken, kunt u de batchverwerking **SKU maken** gebruiken.  

> [!NOTE]  
>  De gegevens op de **SKU**-kaart hebben voorrang op de gegevens op de **artikelkaart**.

> [!Warning]
> Wanneer de SKU wordt geleverd via productie, wordt het veld **Vaste verrekenprijs** niet gebruikt bij de facturering en de berekening van de werkelijke kosten van een geproduceerd artikel. In plaats daarvan wordt het veld **Vaste verrekenprijs** van de onderliggende artikelkaart gebruikt en worden eventuele afwijkingen berekend tegen het kostenaandeel van dat artikel.<br /><br />
> Omdat productiestuklijsten en routering niet kunnen worden toegewezen aan SKU´s, zijn de berekening van kosten per eenheid en de bijbehorende berekening van het kostenaandeel ook niet beschikbaar voor SKU's. Zie [Vaste verrekenprijs berekenen](finance-about-calculating-standard-cost.md) voor nadere informatie

## <a name="see-also"></a>Zie ook  
[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
