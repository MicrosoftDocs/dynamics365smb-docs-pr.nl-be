---
title: 'Ontwerpdetails: Ontwerp artikeltracering | Microsoft Docs'
description: In dit onderwerp komt het ontwerp achter artikeltracering in Business Central aan bod.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, tracing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 87c85de9f501e093679512b709841d0027fe17bf
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751342"
---
# <a name="design-details-item-tracking-design"></a>Ontwerpdetails: Ontwerp artikeltracering
In de eerste versie van Artikeltracering in [!INCLUDE[prod_short](includes/prod_short.md)] 2.60 werden serienummers of lotnummers direct geregistreerd in artikelposten. Dit ontwerp bood volledige beschikbaarheidsgegevens en eenvoudige tracering van historische posten, maar het miste flexibiliteit en functionaliteit.  

Vanaf [!INCLUDE[prod_short](includes/prod_short.md)] 3.00 bevond de artikeltraceringfunctionaliteit zich in een afzonderlijke objectstructuur met complexe koppelingen naar geboekte documenten en artikelposten. Dit ontwerp was flexibel en bood uitgebreide functionaliteit, maar artikeltraceringsposten werden niet volledig betrokken bij beschikbaarheidsberekeningen.  

Vanaf [!INCLUDE[prod_short](includes/prod_short.md)] 3.60 is de artikeltraceringfunctionaliteit geïntegreerd in het reserveringsysteem, waarmee reserveringen, ordertracering en planningsboodschappen worden verwerkt. Zie voor meer informatie "Ontwerpdetails: Reservering, ordertracering en planningsboodschappen" in "Ontwerpdetails: Voorraadplanning".  

Dit laatste ontwerp integreert artikeltraceringsposten in berekeningen van de totale beschikbaarheid in het hele systeem, inclusief planning, productie en magazijnactiviteiten. Het klassieke concept van het overzetten van serie- en lotnummers in de artikelposten, wordt opnieuw gebruikt om te zorgen voor eenvoudige toegang tot historische gegevens voor artikeltracering. In verband met verbeteringen in de artikeltracering in [!INCLUDE[prod_short](includes/prod_short.md)] 3.60 is het reserveringsysteem uitgebreid tot niet-order netwerkentiteiten, zoals dagboeken, facturen en creditnota's.  

Met het toevoegen van serie- of lotnummers verwerkt het reserveringssysteem permanente artikelkenmerken terwijl ook cyclische koppelingen tussen voorziening en vraag in de vorm van ordertraceringsposten en reserveringsposten worden verwerkt. Een ander kenmerk van serie- of lotnummers in vergelijking met de conventionele reserveringsgegevens is het feit dat deze gedeeltelijk of volledig kunnen worden geboekt. De tabel **Reserveringspost** (T337) werkt daarom nu met een gekoppelde tabel, de tabel **Traceringsspecificatie** (T336), waarmee optellingen tussen traceringsaantallen actieve en geboekte artikelen worden beheerd en weergegeven. Zie voor meer informatie [Ontwerpdetails: Actieve tegenover historische artikeltraceringsposten](design-details-active-versus-historic-item-tracking-entries.md).  

In het volgende diagram wordt het ontwerp van artikeltraceringfunctionaliteit in [!INCLUDE[prod_short](includes/prod_short.md)] aangegeven.  

![Voorbeeld van een artikeltraceringsstroom](media/design_details_item_tracking_design.png "Voorbeeld van een artikeltraceringsstroom")  

Het centrale boekingsobject is opnieuw ontworpen om de unieke subclassificatie van een documentregel te verwerken in de vorm van serie- of lotnummers. Er zijn speciale relatietabellen toegevoegd om de één-op-veel relaties tussen geboekte documenten en de gesplitste artikelposten en waardeposten te maken.  

Codeunit 22, **Artikeldagboek. - Regel boeken** splitst nu de boeking volgens de artikeltraceringsnummers die zijn opgegeven op de documentregel. Voor ieder uniek artikeltraceringsnummer op de regel wordt een eigen artikelpost voor het artikel gemaakt. Dit betekent dat de koppeling van de geboekte documentregel naar de bijbehorende artikelposten nu een één-op-veel relatie is. Deze relatie wordt uitgevoerd door de volgende tabellen met artikeltraceringrelaties.  

|Veld|Omschrijving|  
|---------------|---------------------------------------|  
|**Artikelpostrelatie** (T6507)|Relateert verzonden of ontvangen regels aan artikelposten|  
|**Waardepostrelatie** (T6508)|Relateert gefactureerde regels aan waardeposten|  

Zie voor meer informatie [Ontwerpdetails: Boekingsstructuur artikeltracering](design-details-item-tracking-posting-structure.md).  

## <a name="see-also"></a>Zie ook  
[Ontwerpdetails: Artikeltracering](design-details-item-tracking.md)
