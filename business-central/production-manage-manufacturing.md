---
title: Productie uitvoeren | Microsoft Docs
description: Wanneer er voor vraag is gepland en de materialen zijn uitgegeven op basis van productiestuklijsten, kunnen de daadwerkelijke productiebewerkingen starten en vervolgens worden uitgevoerd in de volgorde die is gedefinieerd in het bewerkingsplan van de productieorder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a4490f216158c1a4391a2845ef5e445bba4ef223
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758854"
---
# <a name="manufacturing"></a>Productie
> [!NOTE]
> Functionaliteit die in dit onderwerp wordt beschreven, is alleen zichtbaar in de gebruikersinterface als u de **Premium**-ervaring hebt. Zie voor meer informatie [Wijzigen welke functies worden weergegeven](ui-experiences.md).

Wanneer er voor vraag is gepland en de materialen zijn uitgegeven op basis van productiestuklijsten, kunnen de daadwerkelijke productiebewerkingen starten en vervolgens worden uitgevoerd in de volgorde die is gedefinieerd in het bewerkingsplan van de productieorder.  

Een uit systeemoogpunt belangrijk deel van de uitvoering van productie is het boeken van productie-output in de database om voortgang te melden en om de voorraad met de gereedgemelde artikelen bij te werken. Output-boeking kan handmatig worden gedaan door na de productiebewerkingen dagboekregels in te vullen en te boeken. Of het kan automatisch worden gedaan door middel van achterwaarts afboeken. In dat geval wordt materiaalverbruik automatisch samen met de output geboekt, wanneer de productieorder wordt gereedgemeld.  

Als alternatief voor het in batches boeken van output voor meerdere productieorders kunt u de pagina **Productiedagboek** gebruiken om verbruik en/of output voor één productieorderregel te boeken.

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
|Output ongedaan maken, bijvoorbeeld vanwege een opgetreden fout met gegevensinvoer en een verkeerd bedrag.  |[Outputboeking tegenboeken](production-how-to-reverse-output-posting.md)|  
|Het aantal artikelen boeken dat is geproduceerd in elke voltooide bewerking, maar niet geldt als voltooide output maar als uitgevallen materiaal.|[Uitval boeken](production-how-to-post-scrap.md)|
|De werklast voor de shopfloor als resultaat van geplande en vrijgegeven productieorders weergeven.|[De werklast in afdelingen en bewerkingsplaatsen weergeven](production-how-to-view-the-load-on-work-centers.md)|      
|De pagina **Capaciteitsdagboek** gebruiken om verbruikte capaciteit te boeken die niet is toegewezen aan een productieorder, zoals onderhoudswerkzaamheden.|[Capaciteit boeken](production-how-to-post-capacities.md)|  
|De kosten van gereedgemelde productieartikelen en verbruikte materialen berekenen en aanpassen voor financiële reconciliatie.|[Over de kosten van de gereedgemelde productieorder](finance-about-finished-production-order-costs.md)|  

## <a name="see-also"></a>Zie ook  
[Productie instellen](production-configure-production-processes.md)  
[Gepland](production-planning.md)      
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]