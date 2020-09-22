---
title: Ontwerpdetails - Kostenonderdelen | Microsoft Docs
description: Kostenonderdelen zijn verschillende soorten kosten die de waarde vormen van een artikeltoename of -afname.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 639a982c81b29a2a51f24551d9c0814f7a3ac1c5
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3788058"
---
# <a name="design-details-cost-components"></a>Ontwerpdetails: Kostenonderdelen
Kostenonderdelen zijn verschillende soorten kosten die de waarde vormen van een artikeltoename of -afname.  

 De volgende tabel toont de verschillende kostenonderdelen en eventuele onderliggende kostenonderdelen waaruit ze bestaan.  

|Kostenonderdeel|Ondergeschikt kostenonderdeel|Description|  
|--------------------|--------------------------------|---------------------------------------|  
|Directe kosten|Kostprijs (directe inkoopprijs)|Kosten die kunnen worden herleid tot een kostenobject.|  
|Directe kosten|Vrachtkosten (artikeltoeslag)|Kosten die kunnen worden herleid tot een kostenobject.|  
|Directe kosten|Verzekeringskosten (artikeltoeslag)|Kosten die kunnen worden herleid tot een kostenobject.|  
|Indirecte kosten||Kosten die niet kunnen worden herleid tot een kostenobject.|  
|Verschil|Inkoopverschil|Het verschil tussen werkelijke kosten en de vaste verrekenprijs. Wordt uitsluitend geboekt voor artikelen met de waarderingsmethode **Standaard**.|  
|Verschil|Materiaalverschil|Het verschil tussen werkelijke kosten en de vaste verrekenprijs. Wordt uitsluitend geboekt voor artikelen met de waarderingsmethode **Standaard**.|  
|Verschil|Capaciteitsverschil|Het verschil tussen werkelijke kosten en de vaste verrekenprijs. Wordt uitsluitend geboekt voor artikelen met de waarderingsmethode **Standaard**.|  
|Verschil|Uitbestedingsverschil|Het verschil tussen werkelijke kosten en de vaste verrekenprijs. Wordt uitsluitend geboekt voor artikelen met de waarderingsmethode **Standaard**.|  
|Verschil|Verschillen cap.-overhead|Het verschil tussen werkelijke kosten en de vaste verrekenprijs. Wordt uitsluitend geboekt voor artikelen met de waarderingsmethode **Standaard**.|  
|Verschil|Productieoverheadverschil|Het verschil tussen werkelijke kosten en de vaste verrekenprijs. Wordt uitsluitend geboekt voor artikelen met de waarderingsmethode **Standaard**.|  
|Herwaardering||Waardevermindering of -vermeerdering van de huidige voorraadwaarde.|  
|Afronding||Restwaarden die ontstaan door de manier waarop de waardering van negatieve voorraadmutaties wordt berekend.|  

> [!NOTE]  
>  Vracht- en verzekeringskosten zijn artikeltoeslagen die op elk moment aan de kosten van een artikel kunnen worden toegevoegd. Wanneer u de batchverwerking **Kostprijs herwaarderen - Artikelposten** uitvoert, wordt de waarde van gerelateerde negatieve voorraadmutaties overeenkomstig bijgewerkt.  

## <a name="see-also"></a>Zie ook  
 [Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)   
 [Ontwerpdetails: Verschil](design-details-variance.md) [Voorraadkosten beheren](finance-manage-inventory-costs.md)  
 [Financiën](finance.md)  
 [Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
