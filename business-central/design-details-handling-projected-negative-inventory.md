---
title: 'Ontwerpdetails: Verwachte negatieve voorraad verwerken | Microsoft Docs'
description: Het bestelpunt drukt de verwachte vraag uit tijdens de doorlooptijd van het artikel. Wanneer het bestelpunt is verstreken, is het tijd om meer te bestellen. Maar de geplande voorraad moet groot genoeg zijn om de vraag te dekken totdat de nieuwe order wordt ontvangen. In de tussentijd moet de veiligheidsvoorraad zorgen voor schommelingen in de vraag tot aan een bepaald serviceniveau.
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
ms.openlocfilehash: 25a2017fd91f09a9d7725c68ffaa0df48a041294
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-handling-projected-negative-inventory"></a>Ontwerpdetails: Verwachte negatieve voorraad verwerken
Het bestelpunt drukt de verwachte vraag uit tijdens de doorlooptijd van het artikel. Wanneer het bestelpunt is verstreken, is het tijd om meer te bestellen. Maar de geplande voorraad moet groot genoeg zijn om de vraag te dekken totdat de nieuwe order wordt ontvangen. In de tussentijd moet de veiligheidsvoorraad zorgen voor schommelingen in de vraag tot aan een bepaald serviceniveau.  

 Dus beschouwt het planningssysteem het als een noodgeval als aan toekomstige vraag niet kan worden voldaan vanuit de voorspelde voorraad, of anders uitgedrukt, als de voorspelde voorraad negatief wordt. Het systeem verwerkt dergelijke uitzonderingen door een nieuwe voorzieningenorder voor te stellen om te voldoen aan het deel van de vraag waaraan de voorraad of andere voorzieningen niet kunnen voldoen. Voor de ordergrootte van de nieuwe voorzieningenorder wordt geen rekening gehouden met de maximale voorraad of het bestelaantal. Dit geldt ook voor de ordervelden Min. bestelaantal, Max. bestelaantal en Vaste lotgrootte. In plaats hiervan is dit het exacte tekort.  

 De planningsregel voor dit soort voorzieningenorder geeft een waarschuwingspictogram Noodgeval weer en er worden extra gegevens getoond bij het opzoeken om de gebruiker te informeren over de situatie.  

 In de volgende illustratie staat aanbod D voor een noodorder om een correctie uit te voeren voor negatieve voorraad.  

 ![Suggestie van noodplanning om negatieve voorraad te voorkomen](media/nav_app_supply_planning_2_negative_inventory.png "Suggestie van noodplanning om negatieve voorraad te voorkomen")  

1.  Voorziening **A**, de oorspronkelijk geplande voorraad, is onder het bestelpunt.  
2.  Er is een nieuwe voorwaarts-geplande voorziening gemaakt (**C**).  

     (Aantal = Maximale voorraad – Gepland voorraadniveau)  
3.  Voorziening **A** wordt afgesloten door vraag **B**, die niet volledig is verwerkt.  

     (Vraag **B** zou kunnen proberen Aanbod C in te plannen, maar dat gebeurt niet op basis van het tijdsintervalconcept.)  
4.  Er wordt nieuw aanbod (**D**) gemaakt om te voldoen aan het resterende aantal van de vraag **B**.  
5.  Vraag **B** wordt gesloten (waarbij een aanmaning voor de geplande voorraad wordt gemaakt).  
6.  De nieuwe voorziening **D** is afgesloten.  
7.  Geplande voorraad wordt gecontroleerd; bestelpunt is niet overschreden.  
8.  Voorziening **C** is afgesloten (er bestaat geen vraag meer).  
9. Laatste controle: Er bestaan geen openstaande voorraadniveauaanmaningen.  

> [!NOTE]  
>  Stap 4 geeft aan hoe het systeem in eerdere versies dan Microsoft Dynamics NAV 2009 SP1 reageert.  

 Hiermee wordt de omschrijving afgerond van centrale principes met betrekking tot voorraadplanning op basis van bestelbeleid. In het volgende gedeelte worden de kenmerken van de vier ondersteunde soorten bestelbeleid beschreven.  

## <a name="see-also"></a>Zie ook  
 [Ontwerpdetails: Bestelbeleid](design-details-reordering-policies.md)   
 [Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md)   
 [Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md)   
 [Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)

