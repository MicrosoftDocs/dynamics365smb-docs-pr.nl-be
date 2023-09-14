---
title: 'Ontwerpdetails: Pagina Artikeltraceringsregels'
description: Lees hoe u de stroom van serie- en lotnummers in uw voorraad beheert met de pagina Artikeltraceringsregels.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, inventory, item, tracking, serial number, lot number'
ms.date: 06/15/2021
ms.author: bholtorf
---
# <a name="design-details-item-tracking-lines-page"></a>Ontwerpdetails: Pagina Artikeltraceringsregels
Artikeltraceringsrecords en reserveringsrecords worden gemaakt in het reserveringsysteem en hun beschikbaarheid wordt dynamisch berekend. Gegevens die op de pagina **Artikeltraceringsregels** worden ingevoerd, worden beheerd in een tijdelijke versie van de tabel **Traceringsspecificatie**. Wanneer de pagina is gesloten, worden de actieve gegevens vastgelegd in de tabel **Reserveringspost** en worden de historische gegevens vastgelegd in de tabel **Traceringsspecificatie**. Zie voor meer informatie [Ontwerpdetails: Actieve tegenover historische artikeltraceringsposten](design-details-active-versus-historic-item-tracking-entries.md).  
  
Opzoekacties vanuit de velden **Serienr.** en **Partijnr.** tonen beschikbaarheid op basis van zowel de tabel **Artikelpost** als de tabel **Reserveringspost**, zonder datumfilter. De matrix van aantalvelden op de kop van de pagina **Artikeltraceringsregels** geeft een dynamische weergave van de aantallen en totalen van artikeltraceringsnummers die op de regels van de pagina worden ingevoerd. De aantallen moeten overeenkomen met de waarden op de documentregel, wat wordt aangegeven door de **0** in de **Niet gedefinieerd**-velden in de koptekst van de pagina .  
  
Voor het coördineren van de stroom serie- en lotnummers door de voorraad bestaan de volgende regels voor het invoeren van gegevens op de pagina **Artikeltraceringsregels**:  
  
* Voor zowel inkomende als uitgaande artikeltraceringsregels kunt u slechts eenmaal een serienummer, met of zonder een lotnummer, invoeren in hetzelfde exemplaar van de pagina **Artikeltraceringsregels**. Als u probeert een combinatie van serie- of lotnummers in te voeren die al aanwezig is op de pagina, wordt de gegevensinvoer geblokkeerd door een foutbericht.  
* Voor inkomende artikeltraceringsregels kunt u het betreffende document niet boeken als een artikel in dezelfde variant en met hetzelfde serienummer zich al in voorraad bevindt. Als u een positieve regel probeert te boeken voor een voorraadartikel met dezelfde variant en hetzelfde serienummer, wordt de boeking geblokkeerd door een foutbericht. Voor zowel inkomende als uitgaande artikeltraceringsregels in open documenten kunt u echter dezelfde combinatie hebben van serie- of lotnummers die verband houden met verschillende brondocumentregels, dat wil zeggen: die in verschillende exemplaren van de pagina **Artikeltraceringsregels** bestaan totdat het gerelateerde document wordt geboekt.  
* Als het artikel is ingesteld voor serienummerspecifieke of lotnummerspecifieke tracering, kunt u geen uitgaande documentregel boeken tenzij er een artikel met het gedefinieerde serie- of lotnummer bestaat in voorraad. Als u een uitgaande documentregel probeert te boeken voor een artikel met een serie- of lotnummer dat niet in de voorraad voorkomt, wordt de boeking geblokkeerd door een foutbericht.  
  
De regels voor het invoeren van gegevens op de pagina **Artikeltraceringsregels** ondersteunen ook de koppelingsprincipes waarop ordertracering, planning en reservering zijn gebaseerd. Zie voor meer informatie [Ontwerpdetails: Artikeltracering en planning](design-details-item-tracking-and-planning.md).  
  
## <a name="see-also"></a>Zie ook
[Ontwerpdetails: Artikeltracering](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
