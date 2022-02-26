---
title: Productieorders maken op basis van verkooporders
description: Leer de verschillende manieren om productieorders te maken voor geproduceerde artikelen, rechtstreeks van verkooporders.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 99000883, 99000884
ms.date: 06/22/2021
ms.author: edupont
ms.openlocfilehash: 493d47e13d9ad1d7a2424dec4cd3691e92068d73
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/14/2022
ms.locfileid: "7973374"
---
# <a name="create-production-orders-from-sales-orders"></a>Productieorders maken op basis van verkooporders
U kunt direct op basis van verkooporders productieorders maken voor geproduceerde artikelen.  

## <a name="to-create-a-production-order-from-a-sales-order"></a>Een productieorder maken op basis van een verkooporder  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer de verkooporder die u wilt omzetten in een productieorder.  
3.  Kies de actie **Planning**. Op de pagina **Verkooporderplanning** kunt u de beschikbaarheid van het verkooporderartikel weergeven.  
4.  Kies de actie **Prod.-order maken**.  
5.  Selecteer de status en het ordersoort.  
6.  Kies de knop **Ja** om een of meer productieorders te maken voor de regels die **Prod.order** in het veld **Aanvullingsmethode** hebben.


> [!NOTE]  
> Vraagregels in de gemaakte productieorder die **Prod.-order** hebben in het veld **Aanvullingsmethode**, vertegenwoordigen onderliggende productieorders. Nadat u deze productieorders hebt gemaakt, moet u er onvervulde componentvraag voor bepalen met de pagina **Orderplanning** of de functie **Opnieuw plannen** vanuit gemaakte orders. 

## <a name="order-type"></a>Ordersoort  
U kunt kiezen uit twee manieren om de productieorders te maken, zoals beschreven in de volgende tabel.

|Optie|Omschrijving|
|------|-----------|
|Artikelorder|Eén productieorder wordt gemaakt voor elke benodigde productieorder die wordt vertegenwoordigd door een regel in het venster **Verkooporderplanning**.|
|Projectorder|Eén productieorder wordt gemaakt voor alle benodigde productieorders die worden vertegenwoordigd door regels in het venster **Verkooporderplanning**. |

Wanneer u projectorders gebruikt, bevat het veld **Bronsoort** van de productieorder **Verkoopkop** en heeft de order heeft meerdere regels (één voor elk verkoopregelartikel dat moet worden geproduceerd).  


## <a name="see-also"></a>Zie ook  
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)    
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md)   
[Aanbevolen procedures instellen: voorraadplanning](setup-best-practices-supply-planning.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
