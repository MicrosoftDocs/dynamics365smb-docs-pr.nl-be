---
title: 'Ontwerpdetails: Artikeltracering en planning | Microsoft Docs'
description: 'Omdat ze in het reserveringsysteem worden opgeslagen, zijn artikeltraceringsnummers volledig gecoördineerd met ordertraceringsrecords.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# Ontwerpdetails: Artikeltracering en planning
Omdat ze in het reserveringsysteem worden opgeslagen, zijn artikeltraceringsnummers volledig gecoördineerd met ordertraceringsrecords. Dit betekent dat aan artikelen met ordertraceringsrecords artikeltraceringsnummers kunnen worden toegewezen. Andersom kunnen artikelen die artikeltraceringsnummers hebben, ordertraceringsrecords worden. Zie [Ontwerpdetails: artikeltraceringsontwerp](design-details-item-tracking-design.md) voor meer informatie.

Voor meer informatie over de geïntegreerde systemen raadpleegt u [Ontwerpdetails: reserveringen, ordertracering en planningsboodschappen](design-details-reservation-order-tracking-and-action-messaging.md).

Omdat ordertracering alleen rekening houdt met specifieke artikelvereffening, is de coördinatie met artikeltraceringsnummers alleen van toepassing op artikelen die zijn ingesteld om specifieke artikeltracering te gebruiken. Dit wordt ingesteld door de velden **Specifieke serienr.-tracering** en **Specifieke lottracering** op de artikelkaart, die het volgende specificeren:

- Het artikel moet een serie- of lotnummer hebben wanneer het wordt geboekt.
- Het artikel moet betrekking hebben op hetzelfde serie- of lotnummer wanneer het uitgaand wordt geboekt.

In overeenstemming met standaardafstemmingsprincipes voor vraag en aanbod stemmen het planningssysteem en de gerelateerde ordertraceringsfunctie alleen vraag en aanbod met artikeltraceringsnummers af als het desbetreffende artikel specifieke artikeltracering gebruikt. In alle overige gevallen negeert het planning- en het ordertraceringsysteem artikeltraceringsnummers wanneer er aanbod mee wordt toegepast op vraag of vraag op aanbod. Zie voor meer informatie [Reservering, ordertracering en planningsboodschappen](design-details-reservation-order-tracking-and-action-messaging.md).

Wanneer er bijvoorbeeld ordertracering bestaat voor een bepaald artikel, impliceert dit dat records voor het artikel zich al in de tabel **Reserveringspost** bevinden. Dat is de kern van het reserveringsysteem, voordat de artikeltraceringsnummers worden gedefinieerd. De volgende koppelingsbeperkingen zijn daarom van toepassing op de artikeltraceringsnummers voor ordertracering:

- Vraag met een serienummer of lotnummer kan alleen voldoen aan aanbod met hetzelfde serienummer of lotnummer.
- Vraag zonder een serienummer of lotnummer kan voldoen aan alle vraag, met of zonder serienummer of lotnummer.

Afgezien van de gevolgen voor dynamische ordertracering hebben de koppelingsbeperkingen van artikeltracering geen grote gevolgen voor het planningssysteem.

Aan de aanbodzijde wordt meestal geen serienummer of lotnummer ingevoerd tot vlak voordat de order wordt geboekt, bijvoorbeeld een inkoopontvangst in het magazijn. Bij het invoeren van een serie- of lotnummer aan de vraagzijde, zoals een verkooporder, is dat serie- of lotnummer al op voorraad. Artikeltraceringsnummers zijn meestal geen punt in voorraadplanning.

Voor artikelen waarvoor specifieke artikeltracering wordt gebruikt, moet alle vraag met serie- of lotnummers overeenkomen met corresponderend aanbod. In de meeste gevallen is het niet zinnig een specifiek serie- of lotnummer te herbestellen, dus wordt de planning van inkoop- of productievoorzieningen waarschijnlijk niet beïnvloed. Wanneer artikelen van de ene vestiging naar de andere worden verplaatst, is het echter waarschijnlijk dat de transfer voor een bepaalde lot is, zodat de planning van transfervoorzieningen kan worden beïnvloed door de specifieke koppelingsbeperking.

Zie [Ontwerpdetails: Transfers in planning](design-details-transfers-in-planning.md) voor meer informatie.

## Vraag en aanbod afstemmen
Als een artikel specifieke artikeltracering vereist, wordt een ordertraceringskoppeling gemaakt van alle artikeltraceringsvraag van het artikel naar corresponderend artikeltraceringsaanbod, met als enige beperking dat aanbod vóór vraag komt. Als in die gevallen geen artikeltraceringvoorziening wordt gevonden die correspondeert met de artikeltraceringspecifieke vraag, wordt direct een nieuwe artikeltraceringvoorziening gemaakt zonder dat wordt gekeken naar ordergrootte, planningsparameters of herplanning van bestaande voorziening van hetzelfde serie- of lotnummer.

Als artikeltraceringsnummers worden toegewezen aan de vraagkant of de aanbodkant zonder dat specifieke artikeltracering is vereist, wordt een ordertraceringskoppeling gemaakt van de vraag naar dat aanbod, op basis van de beste timing en het beste aantal, zoals in de gebruikelijke vereffeningsprocedure. Het opgegeven artikeltraceringsnummer wordt op dezelfde manier in de ordertraceringsrecord opgenomen als voor een willekeurig artikeltraceringsaantal één deel van de ordertraceringskoppeling wordt gedefinieerd. Dit betekent dat het ingevoerde artikeltraceringsnummer wordt bewaard terwijl het ook een deel van de ordertraceringsrecord is.

Als artikeltraceringsnummers worden toegewezen aan de aanbodzijde zonder dat specifieke artikeltracering is vereist, wordt dit aanbod door het planningssysteem als vast beschouwd. De omvang wijzigen of herplannen wordt niet voorgesteld voor deze voorziening, maar er wordt rekening met de voorziening gehouden wanneer het planningssysteem probeert te voldoen aan de brutovereisten.

Zie voor meer informatie [Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md).  

## Zie ook  
[Ontwerpdetails: Ontwerp artikeltracering](design-details-item-tracking-design.md)  
[Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md)  
[Ontwerpdetails: Reservering, ordertracering en planningsboodschappen](design-details-reservation-order-tracking-and-action-messaging.md)   
[Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]