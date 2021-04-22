---
title: Onderdelen afboeken op basis van de uitvoer van een bewerking
description: Voor artikelen die zijn ingesteld met de achterwaartse afboekingsmethode, wordt standaard het verbruik van onderdelen berekend en geboekt wanneer u de status van een vrijgegeven productieorder wijzigt in Voltooid.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d1448b9105426103d70abfb820bd38b6adb41db8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779265"
---
# <a name="flush-components-according-to-operation-output"></a>Onderdelen afboeken op basis van de uitvoer van een bewerking
U kunt verschillende afboekingsstrategieën definiëren om de registratie van het verbruik van componenten te automatiseren. 

Als bijvoorbeeld een productieorder voor het vervaardigen van 800 meter 8 kg van een component vereist, worden als u 200 meter als uitvoer boekt automatisch 2 kg als verbruik geboekt. 

Deze functionaliteit is handig om de volgende redenen:  

- **Voorraadwaardering**

    Waardeposten voor uitvoer en verbruik worden parallel geproduceerd naarmate de productieorder vordert. Zonder bewerkingsplankoppelingen neemt de voorraadwaarde toe als uitvoer wordt geboekt en vervolgens op een later tijdstip weer af wanneer de waarde van het materiaalverbruik wordt geboekt samen met de gereedgemelde productieorder.  
- **Beschikbaarheid van voorraad**

    Bij geleidelijke verbruiksboeking is de beschikbaarheid van artikelonderdelen meer actueel, hetgeen belangrijk is voor het handhaven van het interne evenwicht tussen vraag en aanbod. Zonder bewerkingsplankoppelingen kan bij andere vraag naar het materiaal de misvatting ontstaan dat het materiaal beschikbaar is zolang een vertraagde verbruiksboeking uitstaat.  
- **Just In Time**

    Via de mogelijkheid om producten aan te passen aan de vraag van de klant kunt u verspilling tot een minimum beperken door ervoor te zorgen dat werk en systeemwijzigingen alleen optreden wanneer het nodig is.  

U kunt dat bereiken door de achterwaartse afboekingsmethode te combineren met codes van bewerkingsplankoppelingen, zodat het aantal dat per bewerking wordt afgeboekt, in verhouding staat tot de werkelijke uitvoer van de voltooide bewerking. Voor artikelen die zijn ingesteld met de achterwaartse afboekingsmethode wordt standaard het verbruik van onderdelen berekend en geboekt wanneer u de status van een vrijgegeven productieorder wijzigt in **Voltooid**. Als u ook bewerkingsplankoppelingen definieert, vinden berekening en boeking plaats wanneer elke bewerking is voltooid en wordt de hoeveelheid geboekt die daadwerkelijk is verbruikt in de bewerking. Zie voor meer informatie [Bewerkingsplannen maken](production-how-to-create-routings.md).  

## <a name="to-flush-components-according-to-operation-output"></a>Onderdelen afboeken op basis van de uitvoer van een bewerking

1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies de gerelateerde koppeling.  
2.  Kies de actie **Bewerken**.  
3.  Selecteer op het sneltabblad **Aanvulling** in het veld **Afboekingsmethode** de optie **Achterwaarts**.  

    > [!NOTE]  
    >  Selecteer **Pick + Achterwaarts** als het onderdeel wordt gebruikt op een locatie die is ingesteld voor gestuurde opslag en pick.  

4.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bewerkingsplannen** in en kies de desbetreffende koppeling.  
5.  Definieer bewerkingsplankoppelingen voor elke bewerking waarbij het onderdeel wordt verbruikt. Zie voor meer informatie [Bewerkingsplannen maken](production-how-to-create-routings.md).  
    > [!IMPORTANT]  
    > Gebruik niet dezelfde routeringskoppeling voor verschillende bewerkingen in de routering, aangezien dit zal leiden tot registratie van het verbruik van een component voor elke gekoppelde bewerking.  
6.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Productiestuklijst** in en kies de desbetreffende koppeling.  
7.  Definieer bewerkingsplankoppelingen op basis van elk exemplaar van de component voor de bewerking waarbij de component wordt verbruikt.

Het verbruik wordt automatisch geboekt wanneer u output registreert. Zie voor meer informatie [Output en bewerkingstijden in batches boeken](production-how-to-post-output-quantity.md)

## <a name="flushing-methods"></a>Afboekingsmethoden

De volgende tabel beschrijft de beschikbare afboekingsmethodeopties die u kunt specificeren op **artikel** kaarten en **SKU**-kaarten.

|Optie|Omschrijving|
|------------|-------------|  
|Handmatig|Hierbij moet u handmatig het verbruik boeken en invoeren in het verbruiksdagboek.|
|Voorwaarts|Boekt automatisch het verbruik op basis van productieordermateriaalregels. <br><br>Het boeken van materiaalverbruik treedt standaard op wanneer u de status van een productieorder wijzigt in **Vrijgegeven**. Als u echter het veld **Bewerkingsplankoppeling** op de productieordermateriaalregels gebruikt, vinden boekingen per bewerking plaats wanneer de bewerking wordt gestart. Zie [Procedure: Bewerkingsplankoppelingen maken](production-how-to-create-routings.md#to-create-routing-links) voor meer informatie. <br><br> **Opmerking**<br>Bij voorwaarts afboeken is de boeking van een specifieke bewerking die u met bewerkingsplankoppelingen verkrijgt, gebaseerd op het verwachte aantal dat gedefinieerd is op de materiaalregel. Zie de beschrijving van **Achterwaarts** in dit onderwerp voor informatie over het afboeken van specifieke bewerkingen gebaseerd op de werkelijke output.<br><br>Als de vestiging of de resources waar dit onderdeel wordt verbruikt, is ingesteld met een standaardopslaglocatiestructuur, wordt het artikel verbruikt vanuit de **Code grijpvoorraadlocatie**. Zie [Procedure: standaard magazijnen met bewerkingsgebieden instellen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md) voor meer informatie. <br><br> **Belangrijk** <br>Voorwaarts afboeken vindt ook plaats wanneer u **Vernieuwen** kiest bij een geheel nieuw vrijgegeven productieorder. U kunt bij deze rechtstreeks vrijgegeven productieorders geen informatie over de opslaglocatie wijzigen omdat de productieordermateriaalregels gegenereerd worden wanneer u de order ververst, waarbij tegelijkertijd de onderdelen voorwaarts afgeboekt worden. Als u dus informatie over de opslaglocatie van een productieorder wilt wijzigen voordat voorwaartse afboeking plaats vindt, moet die order worden gemaakt met de *Geplande* of *Vast geplande* status.|
|Achterwaarts|Berekent en boekt automatisch verbruik op basis van de productieordermateriaalregels.<br><br> De berekening en boeking van materiaalverbruik vindt standaard plaats wanneer u de status van een vrijgegeven productieorder wijzigt in **Gereedgemeld**. Als u echter het veld **Bewerkingsplankoppeling** op de productieordermateriaalregels gebruikt, vinden de berekening en boeking plaats wanneer elke bewerking is voltooid.<br><br> **Opmerking** <br>Achterwaarts afboeken en bewerkingsplankoppelingen kunnen worden gecombineerd zodat het aantal dat per bewerking leeggemaakt wordt, in verhouding staat tot de werkelijke output van die bewerking. Zie voor meer informatie [Procedure: materialen afboeken op basis van de uitvoer van een bewerking](#to-flush-components-according-to-operation-output).<br><br> Als de vestiging of de bewerkingsplaats waar dit onderdeel wordt verbruikt, is ingesteld met een standaardopslaglocatiestructuur, wordt het artikel verbruikt vanuit de **Code grijpvoorraadlocatie**.|
|Picken + voorwaarts|Hetzelfde geldt voor de voorwaartse afboekingsmethode, behalve dat het alleen werkt voor vestigingen die gestuurde opslag en picks gebruiken.<br><br> Verbruik wordt berekend en geboekt op basis van de opslaglocatie die gedefinieerd is in het veld **Code opslaglocatie voor productie** op de vestiging of bewerkingsplaats nadat het onderdeel uit het magazijn is gepickt.<br><br> **Opmerking** <br>Als een onderdeel is ingesteld met de Pick + Voorwaartse afboekingsmethode, kan het geen bewerkingsplankoppeling hebben met een bewerking die ingesteld is met de voorwaartse afboekingsmethode. Het onderdeel zou vervolgens automatisch worden leeggemaakt wanneer de bewerking wordt gestart, waardoor het onmogelijk is om de pickactiviteit aan te vragen.|
|Picken + achterwaarts|Hetzelfde geldt voor de achterwaartse afboekingsmethode, behalve dat het alleen werkt voor vestigingen die gestuurde opslag en pick gebruiken.<br><br> Verbruik wordt berekend en geboekt op basis van de opslaglocatie die gedefinieerd is in het veld **Code opslaglocatie voor productie** op de vestiging of bewerkingsplaats nadat het onderdeel uit het magazijn is gepickt.|

## <a name="see-also"></a>Zie ook

[Productiestuklijsten maken](production-how-to-create-production-boms.md)  
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)  
[Gepland](production-planning.md)  
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
