---
title: Ontwerpdetails - Afronding | Microsoft Docs
description: Afrondingsverschillen kunnen optreden wanneer u de kosten waardeert van een negatieve voorraadmutatie die in een andere hoeveelheid wordt gemeten dan de overeenkomende positieve voorraadmutatie. Afrondingsverschillen worden berekend voor alle waarderingsmethoden wanneer u de batchverwerking **Kostprijs herwaarderen - Artikelposten** uitvoert.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: d8fac07df8d83b46a6ab8ed4d20a50a81c0731d5
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6214865"
---
# <a name="design-details-rounding"></a>Ontwerpdetails: Afronding
Afrondingsverschillen kunnen optreden wanneer u de kosten waardeert van een negatieve voorraadmutatie die in een andere hoeveelheid wordt gemeten dan de overeenkomende positieve voorraadmutatie. Afrondingsverschillen worden berekend voor alle waarderingsmethoden wanneer u de batchverwerking **Kostprijs herwaarderen - Artikelposten** uitvoert.  

 Wanneer u de waarderingsmethode Gemiddeld gebruikt, wordt het afrondingsverschil berekend en vastgelegd op een cumulatieve post-per-post-basis.  

 Als u een andere waarderingsmethode dan Gemiddeld gebruikt, wordt het afrondingsverschil berekend wanneer de voorraadtoename volledig is vereffend, oftewel wanneer het resterende aantal voor de voorraadtoename gelijk is aan nul. Vervolgens is een afzonderlijke post gemaakt voor het afrondingsverschil en de boekingsdatum van deze afrondingspost is de boekingsdatum van de laatst gefactureerde waardepost van de positieve voorraadmutatie.  

## <a name="example"></a>Opmerking  
 In het volgende voorbeeld ziet u hoe de verschillende afrondingsverschillen voor respectievelijk de gemiddelde waarderingsmethode en de niet-gemiddelde waarderingsmethode worden verwerkt. In beide gevallen is de batchverwerking **Kostprijs herwaarderen - Artikelposten** uitgevoerd.  

 De volgende tabel toont de artikelposten waarop het voorbeeld is gebaseerd.  

|Boekingsdatum|Aantal|Volgnummer|  
|------------------|--------------|---------------|  
|01-01-20|3|1|  
|01-02-20|-1|2|  
|01-03-20|-1|3|  
|01-04-20|-1|4|  

 Voor een artikel dat de waarderingsmethode Gemiddeld gebruikt, wordt de afrondingsrest (1/300) berekend met de eerste vermindering (postnummer 2) en vervolgens overgedragen aan postnummer 3. Daarom wordt volgnummer 3 gewaardeerd op -3,34.  

 De volgende tabel toont de twee soorten resulterende waardeposten.  

|Boekingsdatum|Aantal|Tot. werk. kosten|Artikelpostnr.|Volgnummer|  
|------------------|--------------|----------------------------|---------------------------|---------------|  
|01-01-20|3|10|1|1|  
|01-02-20|-1|-3,33|2|2|  
|01-03-20|-1|-3,34|3|3|  
|01-04-20|-1|-3,33|4|4|  

 Voor een artikel waarvoor u een andere waarderingsmethode dan Gemiddelde gebruikt, wordt het afrondingsrestant (0,01) berekend wanneer het resterende aantal voor de voorraadtoename nul is. Het afrondingsverschil heeft een afzonderlijke post (nummer 5).  

 De volgende tabel toont de twee soorten resulterende waardeposten.  

|Boekingsdatum|Aantal|Tot. werk. kosten|Artikelpostnr.|Volgnummer|  
|------------------|--------------|----------------------------|---------------------------|---------------|  
|01-01-20|3|10|1|1|  
|01-02-20|-1|-3,33|2|2|  
|01-03-20|-1|-3,33|3|3|  
|01-04-20|-1|-3,33|4|4|  
|01-01-20|0|-0,01|1|5|  

## <a name="see-also"></a>Zie ook  
 [Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)   
 [Ontwerpdetails: Kostenwaardering](design-details-cost-adjustment.md)   
 [Ontwerpdetails: Waarderingsmethoden](design-details-costing-methods.md) [Voorraadkosten beheren](finance-manage-inventory-costs.md)  
 [Financiën](finance.md)  
 [Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]