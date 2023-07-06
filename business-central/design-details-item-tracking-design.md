---
title: 'Ontwerpdetails: Ontwerp artikeltracering'
description: Dit onderwerp beschrijft het ontwerp achter artikeltracering in Business Central naarmate het productversies doorloopt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, item, tracking, tracing'
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-item-tracking-design"></a><a name="design-details-item-tracking-design"></a><a name="design-details-item-tracking-design"></a>Ontwerpdetails: Ontwerp artikeltracering

Artikeltracering in [!INCLUDE[prod_short](includes/prod_short.md)] begon met [!INCLUDE [navnow_md](includes/navnow_md.md)]. De artikeltracering bevindt zich in een aparte objectstructuur met ingewikkelde koppelingen naar geboekte documenten en artikelposten, en is geïntegreerd met het reserveringssysteem, dat de reservering, ordertracering en actieberichten afhandelt. Zie voor meer informatie [Ontwerpdetails: Reservering, ordertracering en planningsboodschappen](design-details-reservation-order-tracking-and-action-messaging.md) in de ontwerpdetails van voorzieningplanning.  

Dit ontwerp integreert artikeltraceringsposten in berekeningen van de totale beschikbaarheid in het hele systeem, inclusief planning, productie en magazijnactiviteiten. Serie- en lotnummers worden toegepast op de artikelposten om te zorgen voor eenvoudige toegang tot historische gegevens voor artikeltracering. Met releasewave 1 van 2021 omvat artikeltracering in [!INCLUDE [prod_short](includes/prod_short.md)] pakketnummers.  

Met het toevoegen van serie-, lot- en pakketnummers verwerkt het reserveringssysteem permanente artikelkenmerken terwijl ook cyclische koppelingen tussen voorziening en vraag in de vorm van ordertraceringsposten en reserveringsposten worden verwerkt. Een ander kenmerk van serie- of lotnummers in vergelijking met de conventionele reserveringsgegevens is het feit dat deze gedeeltelijk of volledig kunnen worden geboekt. De tabel **Reserveringspost** (T337) werkt daarom nu met een gekoppelde tabel, de tabel **Traceringsspecificatie** (T336), waarmee optellingen tussen traceringsaantallen actieve en geboekte artikelen worden beheerd en weergegeven. Zie voor meer informatie [Ontwerpdetails: Actieve tegenover historische artikeltraceringsposten](design-details-active-versus-historic-item-tracking-entries.md).  

In het volgende diagram wordt het ontwerp van artikeltraceringfunctionaliteit in [!INCLUDE[prod_short](includes/prod_short.md)] aangegeven.  

![Voorbeeld van een artikeltraceringsstroom.](media/design_details_item_tracking_design.png "Voorbeeld van een artikeltraceringsstroom")  

Het centrale boekingsobject is opnieuw ontworpen om de unieke subclassificatie van een documentregel te verwerken in de vorm van serie- of lotnummers. Er zijn speciale relatietabellen toegevoegd om de één-op-veel relaties tussen geboekte documenten en de gesplitste artikelposten en waardeposten te maken.  

Codeunit 22, **Artikeldagboek. - Regel boeken** splitst nu de boeking volgens de artikeltraceringsnummers die zijn opgegeven op de documentregel. Voor ieder uniek artikeltraceringsnummer op de regel wordt een eigen artikelpost voor het artikel gemaakt. Dit betekent dat de koppeling van de geboekte documentregel naar de bijbehorende artikelposten nu een één-op-veel relatie is. Deze relatie wordt uitgevoerd door de volgende tabellen met artikeltraceringrelaties.  

|Veld|Omschrijving|  
|---------------|---------------------------------------|  
|**Artikelpostrelatie** (T6507)|Relateert verzonden of ontvangen regels aan artikelposten|  
|**Waardepostrelatie** (T6508)|Relateert gefactureerde regels aan waardeposten|  

Zie voor meer informatie [Ontwerpdetails: Boekingsstructuur artikeltracering](design-details-item-tracking-posting-structure.md).  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Zie ook

[Ontwerpdetails: Artikeltracering](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]  
