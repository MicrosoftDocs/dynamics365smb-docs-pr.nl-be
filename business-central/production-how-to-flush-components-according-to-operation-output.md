---
title: Materialen afboeken op basis van de uitvoer van een bewerking | Microsoft Docs
description: Voor artikelen die zijn ingesteld met de achterwaartse afboekingsmethode wordt standaard het verbruik van onderdelen berekend en geboekt wanneer u de status van een vrijgegeven productieorder wijzigt in **Voltooid**. Zie voor meer informatie Afboekingsmethode.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f7f6c0c4be56c5f7e25f44063923cfe02e03e4c8
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4759304"
---
# <a name="flush-components-according-to-operation-output"></a>Onderdelen afboeken op basis van de uitvoer van een bewerking
Voor artikelen die zijn ingesteld met de achterwaartse afboekingsmethode wordt standaard het verbruik van onderdelen berekend en geboekt wanneer u de status van een vrijgegeven productieorder wijzigt in **Voltooid**.  

Als u ook bewerkingsplankoppelingen definieert, vinden berekening en boeking plaats wanneer elke bewerking is voltooid en wordt de hoeveelheid geboekt die daadwerkelijk is verbruikt in de bewerking. Zie voor meer informatie [Bewerkingsplannen maken](production-how-to-create-routings.md).  

Als bijvoorbeeld een productieorder voor het vervaardigen van 800 meter 8 kg van een component vereist, worden als u 200 meter als uitvoer boekt automatisch 2 kg als verbruik geboekt.  

Deze functionaliteit is handig om de volgende redenen:  

-   **Voorraadwaardering** - Waardeposten voor uitvoer en verbruik worden parallel geproduceerd naarmate de productieorder vordert. Zonder bewerkingsplankoppelingen neemt de voorraadwaarde toe als uitvoer wordt geboekt en vervolgens op een later tijdstip weer af wanneer de waarde van het materiaalverbruik wordt geboekt samen met de gereedgemelde productieorder.  
-   **Beschikbaarheid van voorraad** - Bij geleidelijke verbruiksboeking is de beschikbaarheid van artikelonderdelen meer actueel, hetgeen belangrijk is voor het handhaven van het interne evenwicht tussen vraag en aanbod. Zonder bewerkingsplankoppelingen kan bij andere vraag naar het materiaal de misvatting ontstaan dat het materiaal beschikbaar is zolang een vertraagde verbruiksboeking uitstaat.  
-   **Just-In-Time** – Via de mogelijkheid om producten aan te passen aan de vraag van de klant kunt u verspilling tot een minimum beperken door ervoor te zorgen dat werk en systeemwijzigingen alleen optreden wanneer het nodig is.  

In de volgende procedure ziet u hoe achterwaarts afboeken en bewerkingsplankoppelingen kunnen worden gecombineerd zodat het aantal dat per bewerking wordt afgeboekt, in verhouding staat tot de werkelijke uitvoer van de voltooide bewerking.  

## <a name="to-flush-components-according-to-operation-output"></a>Onderdelen afboeken op basis van de uitvoer van een bewerking  
1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies de gerelateerde koppeling.  
2.  Kies de actie **Bewerken**.  
3.  Selecteer op het sneltabblad **Aanvulling** in het veld **Methode** de optie **Voorwaarts**.  

    > [!NOTE]  
    >  Selecteer **Pick + Voorwaarts** als het onderdeel wordt gebruikt op een locatie die is ingesteld voor gestuurde opslag en pick.  

4.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bewerkingsplannen** in en kies de desbetreffende koppeling.  
5.  Definieer bewerkingsplankoppelingen voor elke bewerking waarbij het onderdeel wordt verbruikt. Zie voor meer informatie [Bewerkingsplannen maken](production-how-to-create-routings.md).  
6.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Productiestuklijst** in en kies de desbetreffende koppeling.  
7.  Definieer bewerkingsplankoppelingen op basis van elk exemplaar van de component voor de bewerking waarbij de component wordt verbruikt.

    > [!IMPORTANT]  
    >  Het onderdeel moet een bewerkingsplankoppeling naar de laatste bewerking in het bewerkingsplan hebben.  

## <a name="see-also"></a>Zie ook  
[Productiestuklijsten maken](production-how-to-create-production-boms.md)  
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)    
[Gepland](production-planning.md)   
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]