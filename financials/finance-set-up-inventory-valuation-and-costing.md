---
title: Voorraadwaardering en kostprijsberekening instellen | Microsoft Docs
description: In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 86fd8f6b15b8a2f868db2938278df6147a092725
ms.contentlocale: nl-be
ms.lasthandoff: 11/10/2017

---
# <a name="setting-up-inventory-valuation-and-costing"></a>Voorraadwaardering en kostprijsberekening instellen
Als u ervoor wilt zorgen dat voorraadkosten correct worden vastgelegd, moet u verschillende velden en vensters instellen voordat u artikeltransacties gaat maken.

In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.

|**Als u dit wilt doen**|**Zie**|  
|------------|-------------|  
|Een waarderingsmethode in te stellen voor elk artikel om te bepalen hoe de inkomende kostprijs ervan wordt gebruikt om voorraadwaarde en de kostprijs van verkochte goederen vast te leggen.|[Procedure: Nieuwe artikelen registreren](inventory-how-register-new-items.md)|  
|Ervoor te zorgen dat de kostprijs automatisch wordt geboekt in het grootboek elke keer wanneer een voorraadtransactie wordt geboekt.|Het veld **Autom. voorraadwaarde boeken** op de pagina **Voorraadinstelling**|  
|Ervoor te zorgen dat verwachte kosten worden geboekt in het grootboek om vanuit de interimgrootboekrekeningen een schatting te kunnen zien van de te betalen bedragen en de kostprijs van de verhandelde artikelen voordat ze worden gefactureerd.|Het veld **Verw. kostprijs naar GB boeken** op de pagina **Voorraadinstelling**|  
|Het systeem in te stellen zodat het bij het boeken van voorraadtransacties automatisch wordt aangepast in het geval van eventuele wijzigingen van de kostprijs.|[Procedure: Artikelkosten herwaarderen](inventory-how-adjust-item-costs.md)|  
|Definieer of de gemiddelde kostprijs alleen moet worden berekend per artikel of per artikel voor elke voorraadunit en voor elke variant van het artikel.|Het veld **Gem. kostprijsberekeningsoort** op de pagina **Voorraadinstelling**|  
|De tijdsperiode te selecteren die het programma moet gebruiken voor het berekenen van de gewogen gemiddelde kostprijs van artikelen die gebruik maken van de gemiddelde waarderingsmethode.|Het veld **Periode gemiddelde kostprijsberekening** op de pagina **Voorraadinstelling**|  
|Voorraadperioden te definiëren om de voorraadwaarde in het verloop van tijd te controleren door het boeken van transacties niet toe te staan in gesloten voorraadperioden.|[Procedure: werken met voorraadperioden](finance-how-to-work-with-inventory-periods.md)|  
|Zorg dat verkoopretouren worden vereffend met de oorspronkelijke uitgaande transactie om voorraadwaarde te behouden.|Het veld **Precieze kostenvereff. verplicht** op de pagina **Verkopen en Klanten**|  
|Zorg dat inkoopretouren worden vereffend met de oorspronkelijke inkomende transactie om voorraadwaarde te behouden.|Het veld **Precieze kostenvereff. verplicht** op de pagina **Inkopen en Leveranciers**|
|De afrondingsregels in te stellen die van toepassing zijn bij het aanpassen of suggereren van artikelprijzen en bij het aanpassen of suggereren van vaste verrekenprijzen.|De pagina **Afrondingsmethode**|  

## <a name="see-also"></a>Zie ook  
[Voorraadkosten beheren](finance-manage-inventory-costs.md)  
[Werken met Dynamics 365](ui-work-product.md)  
[Financiën](finance.md)  

