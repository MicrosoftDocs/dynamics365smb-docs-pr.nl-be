---
title: 'Ontwerpdetails: Onder het overflowniveau blijven | Microsoft Docs'
description: Wanneer Maximum aantal en Vast bestelaantal worden gebruikt, richt het planningssysteem zich alleen op de geplande voorraad in het betreffende tijdsinterval. Dit betekent dat het planningssysteem overbodige voorziening kan voorstellen wanneer negatieve vraag- of positieve voorzieningswijzigingen buiten het betreffende tijdsinterval plaatsvinden.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: 250de9bf843dac7bfca08d8f3a9dcd4ea44586df
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240062"
---
# <a name="design-details-staying-under-the-overflow-level"></a>Ontwerpdetails: Onder het overflowniveau blijven
Wanneer de beleidsopties Maximum aantal en Vast bestelaantal worden gebruikt, richt het planningssysteem zich alleen op de geplande voorraad in het betreffende tijdsinterval. Dit betekent dat het planningssysteem overbodige voorziening kan voorstellen wanneer negatieve vraag- of positieve voorzieningswijzigingen buiten het betreffende tijdsinterval plaatsvinden. Als om deze reden een overbodige voorziening wordt voorgesteld, berekent het planningssysteem tot welk aantal de voorziening moet worden teruggebracht (of verwijderd) om de overbodige voorziening te voorkomen. Dit aantal wordt het overflowniveau genoemd. De overflow wordt gecommuniceerd als een planningsregel met een actie **Aantal wijzigen (afname)** of **Annuleren** en het volgende waarschuwingsbericht:  

*Let op: De geplande voorraad [xx] is groter dan het overflowniveau [xx] op de Vervaldatum [xx].*  

![Voorraadoverflowniveau](media/supplyplanning_2_overflow1_new.png "Voorraadoverflowniveau")  

##  <a name="calculating-the-overflow-level"></a>Het overflowniveau berekenen  
Het overflowniveau wordt op verschillende manieren berekend, afhankelijk van de planningsinstelling.  

### <a name="maximum-qty-reordering-policy"></a>Bestelbeleid Maximum aantal  
Overflowniveau = Maximale voorraad  

> [!NOTE]  
>  Als een minimaal orderaantal bestaat, wordt het als volgt toegevoegd: overflowniveau = maximale voorraad + minimaal orderaantal.  

### <a name="fixed-reorder-qty-reordering-policy"></a>Bestelbeleid voor vast bestelaantal  
Overflowniveau = Bestelaantal + bestelpunt  

> [!NOTE]  
>  Als het minimale bestelaantal hoger is dan het bestelpunt, wordt dit als volgt vervangen: overflowniveau = bestelaantal + minimum bestelaantal.  

### <a name="order-multiple"></a>Vaste lotgrootte  
Als een vaste lotgrootte bestaat, wordt het overflowniveau voor zowel het bestelbeleid Maximum aantal als Vast bestelaantal aangepast.  

##  <a name="creating-the-planning-line-with-overflow-warning"></a>De planningsregel met overflowwaarschuwing maken  
Als door een bestaande voorraad de geplande voorziening groter is dan het overflowniveau aan het einde van het tijdsinterval, wordt een planningsregel gemaakt. Om te waarschuwen voor de mogelijke overbodige voorziening, bevat de planningsregel een waarschuwing, is het veld **Planningsboodschap accepteren** niet geselecteerd en is de planningsboodschap Annuleren of Aantal wijzigen.  

### <a name="calculating-the-planning-line-quantity"></a>Het planningsregelaantal berekenen  
Planningsregelaantal = Voorzieningaantal - (Geplande voorraad - Overflowniveau)  

> [!NOTE]  
>  Net als alle waarschuwingsregels worden eventuele maximale/minimale orderaantallen of vaste ordergrootte genegeerd.  

### <a name="defining-the-action-message-type"></a>De soort planningsboodschap definiëren  

-   Als het planningsregelaantal groter is dan 0, is de planningsboodschap Aantal wijzigen.  
-   Als het planningsregelaantal gelijk is aan of kleiner is dan 0, is de planningsboodschap Annuleren  

### <a name="composing-the-warning-message"></a>Het waarschuwingsbericht opstellen  
In het geval van overflow wordt op de pagina **Niet-getraceerde planningselementen** een waarschuwing weergegeven met de volgende informatie:  

-   Het geplande voorraadniveau dat de waarschuwing heeft geactiveerd  
-   Het berekenende overflowniveau  
-   De vervaldatum van de voorzieningsgebeurtenis.  

Voorbeeld: “De verwachte voorraad 120 is hoger dan het overflowniveau 60 op 28-01-11“  

## <a name="scenario"></a>Scenario  
In dit scenario verandert een klant een verkooporder van 70 in 40 stuks tussen twee planningen. De overflowfunctie wordt geactiveerd om de inkoop te beperken die werd voorgesteld voor het oorspronkelijke verkoopaantal.  

### <a name="item-setup"></a>Artikelinstellingen  

|Bestelbeleid|Maximum aantal|  
|-----------------------|------------------|  
|Max. bestelaantal|100|  
|Bestelpunt|50|  
|Voorraad|80|  

### <a name="situation-before-sales-decrease"></a>Situatie voor verkoopafname  

|Gebeurtenis|Aantal wijzigen|Geschatte inventaris|  
|-----------|-----------------|-------------------------|  
|Dag één|Geen|80|  
|Verkoop|-70|10|  
|Einde van periode|Geen|10|  
|Nieuwe inkooporder voorstellen|+90|100|  

### <a name="situation-after-sales-decrease"></a>Situatie na verkoopafname  

|Wijzigen|Aantal wijzigen|Geschatte inventaris|  
|------------|-----------------|-------------------------|  
|Dag één|Geen|80|  
|Verkoop|-40|40|  
|Inkoop|+90|130|  
|Einde van periode|Geen|130|  
|Voorstellen om inkoop te verminderen<br /><br /> van 90 naar 60|-30|100|  

### <a name="resulting-planning-lines"></a>Resulterende planningsregels  
 Er wordt één planningsregel (waarschuwing) gemaakt om de inkoop met 30 te reduceren, van 90 tot 60, om de geplande voorraad op 100 te houden, op basis van het overflowniveau.  

![Plannen volgens overflowniveau](media/nav_app_supply_planning_2_overflow2.png "Plannen volgens overflowniveau")  

> [!NOTE]  
>  Zonder de overflowfunctie wordt er geen waarschuwing gemaakt als het geplande voorraadniveau boven de maximale voorraad is. Dit kan een overbodige voorziening van 30 genereren.  

## <a name="see-also"></a>Zie ook  
[Ontwerpdetails: Bestelbeleid](design-details-reordering-policies.md)   
[Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md)   
[Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md)   
[Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)
