---
title: Productie uitvoeren | Microsoft Docs
description: Wanneer er voor vraag is gepland en de materialen zijn uitgegeven op basis van productiestuklijsten, kunnen de daadwerkelijke productiebewerkingen starten en vervolgens worden uitgevoerd in de volgorde die is gedefinieerd in het bewerkingsplan van de productieorder.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/26/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c97cdafceb5fbf8df403309dddda0faeac7a26b6
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="manufacturing"></a>Productie
Wanneer er voor vraag is gepland en de materialen zijn uitgegeven op basis van productiestuklijsten, kunnen de daadwerkelijke productiebewerkingen starten en vervolgens worden uitgevoerd in de volgorde die is gedefinieerd in het bewerkingsplan van de productieorder.  

Een uit systeemoogpunt belangrijk deel van de uitvoering van productie is het boeken van productie-output in de database om voortgang te melden en om de voorraad met de gereedgemelde artikelen bij te werken. Output-boeking kan handmatig worden gedaan door na de productiebewerkingen dagboekregels in te vullen en te boeken. Of het kan automatisch worden gedaan door middel van achterwaarts afboeken. In dat geval wordt materiaalverbruik automatisch samen met de output geboekt, wanneer de productieorder wordt gereedgemeld.  

Als alternatief voor het in batches boeken van output voor meerdere productieorders kunt u het venster **Productiedagboek** gebruiken om verbruik en/of output voor één productieorderregel te boeken.

Voordat u artikelen kunt gaan produceren, moet u verschillende zaken instellen, zoals afdelingen, bewerkingsplannen en productiestuklijsten. Zie [Productie instellen](production-configure-production-processes.md) voor meer informatie.

In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.   

|**Als u dit wilt doen**|**Zie**|  
|------------|-------------|  
|Begrijpen hoe de productieorders werken.|[Informatie over productieorders](production-about-production-orders.md)|
|Handmatig productieorders maken.|[Productieorders maken](production-how-to-create-production-orders.md)|
|Alle of bepaalde bewerkingen in een productieorder uitbesteden aan een toeleverancier.|[Productie uitbesteden](production-how-to-subcontract-manufacturing.md)|
|Productie-output en verbruikte materiaal en tijd vastleggen voor één vrijgegeven productieorderregel.|[Verbruik en output boeken voor één vrijgegeven productieorderregel.](production-how-to-register-consumption-and-output.md)|  
|Het aantal gebruikte onderdelen per bewerking in batches in een dagboek boeken waarin meerdere geplande productieorders kunnen worden verwerkt.|[Verbruik in batches boeken](production-how-to-post-consumption.md)|
|Het aantal voltooide artikelen en de bestede tijd per bewerking in een dagboek boeken waarin meerdere vrijgegeven productieorders kunnen worden verwerkt.|[Output en bewerkingstijden in batches boeken](production-how-to-post-output-quantity.md)|  
|Het aantal artikelen boeken dat is geproduceerd in elke voltooide bewerking, maar niet geldt als voltooide output maar als uitgevallen materiaal.|[Uitval boeken](production-how-to-post-scrap.md)|
|De werklast voor de shopfloor als resultaat van geplande en vrijgegeven productieorders weergeven.|[De werklast in afdelingen en bewerkingsplaatsen weergeven](production-how-to-view-the-load-on-work-centers.md)|      
|Het venster **Capaciteitsdagboek** gebruiken om verbruikte capaciteit te boeken die niet is toegewezen aan een productieorder, zoals onderhoudswerkzaamheden.|[Capaciteit boeken](production-how-to-post-capacities.md)|  
|De kosten van gereedgemelde productieartikelen en verbruikte materialen berekenen en aanpassen voor financiële reconciliatie.|[Over de kosten van de gereedgemelde productieorder](finance-about-finished-production-order-costs.md)|  

## <a name="see-also"></a>Zie ook  
[Productie instellen](production-configure-production-processes.md)  
[Gepland](production-planning.md)      
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

