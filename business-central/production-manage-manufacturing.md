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
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: b1712215a392d8abdb0ca549c621d77490e6341c
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="manufacturing"></a>Productie
> [!NOTE]
> Functionaliteit die in dit onderwerp wordt beschreven, is alleen zichtbaar in de gebruikersinterface als u de **Premium**-ervaring hebt. Zie voor meer informatie [Wijzigen welke functies worden weergegeven](ui-experiences.md).

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

