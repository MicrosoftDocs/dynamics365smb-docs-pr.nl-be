---
title: 'Ontwerpdetails: Venster Artikeltraceringsregels | Microsoft Docs'
description: Lees hoe u de stroom van serie- en lotnummers in uw voorraad beheert.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, item, tracking, serial number, lot number
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 62070ef4e580a3bd665130c9b017bf164bbe2142
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-item-tracking-lines-window"></a>Ontwerpdetails: Venster Artikeltraceringsregels
Artikeltraceringsrecords en reserveringsrecords worden gemaakt in het reserveringsysteem en hun beschikbaarheid wordt dynamisch berekend. Gegevens die in het venster **Artikeltraceringsregels** worden ingevoerd, worden beheerd in een tijdelijke versie van de tabel **Traceringsspecificatie**. Wanneer het venster is gesloten, worden de actieve gegevens vastgelegd in de tabel **Reserveringspost** en worden de historische gegevens vastgelegd in de tabel **Traceringsspecificatie**. Zie voor meer informatie [Ontwerpdetails: Actieve tegenover historische artikeltraceringsposten](design-details-active-versus-historic-item-tracking-entries.md).  
  
Opzoekacties vanuit de velden **Serienr.** en **Partijnr.** tonen beschikbaarheid op basis van zowel de tabel **Artikelpost** als de tabel **Reserveringspost**, zonder datumfilter. De matrix van aantalvelden op de kop van het venster **Artikeltraceringsregels** geeft een dynamische weergave van de aantallen en totalen van artikeltraceringsnummers die op de regels van het venster worden ingevoerd. De aantallen moeten overeenkomen met de waarden op de documentregel, wat wordt aangegeven door de **0** in de **Niet gedefinieerd**-velden in de koptekst van het venster.  
  
Voor het coördineren van de stroom serie- en lotnummers door de voorraad bestaan de volgende regels voor het invoeren van gegevens in het venster **Artikeltraceringsregels**:  
  
* Voor zowel inkomende als uitgaande artikeltraceringsregels kunt u slechts eenmaal een serienummer, met of zonder een lotnummer, invoeren in hetzelfde exemplaar van het venster **Artikeltraceringsregels**. Als u probeert een combinatie van serie- of lotnummers in te voeren die al aanwezig is in het venster, wordt de gegevensinvoer geblokkeerd door een foutbericht.  
* Voor inkomende artikeltraceringsregels kunt u het betreffende document niet boeken als een artikel in dezelfde variant en met hetzelfde serienummer zich al in voorraad bevindt. Als u een positieve regel probeert te boeken voor een voorraadartikel met dezelfde variant en hetzelfde serienummer, wordt de boeking geblokkeerd door een foutbericht. Voor zowel inkomende als uitgaande artikeltraceringsregels in open documenten kunt u echter dezelfde combinatie hebben van serie- of lotnummers die verband houden met verschillende brondocumentregels, dat wil zeggen: die in verschillende exemplaren van het venster **Artikeltraceringsregels** bestaan totdat het gerelateerde document wordt geboekt.  
* Als het artikel is ingesteld voor serienummerspecifieke of lotnummerspecifieke tracering, kunt u geen uitgaande documentregel boeken tenzij er een artikel met het gedefinieerde serie- of lotnummer bestaat in voorraad. Als u een uitgaande documentregel probeert te boeken voor een artikel met een serie- of lotnummer dat niet in de voorraad voorkomt, wordt de boeking geblokkeerd door een foutbericht.  
  
De regels voor het invoeren van gegevens in het venster **Artikeltraceringsregels** ondersteunen ook de koppelingsprincipes waarop ordertracering, planning en reservering zijn gebaseerd. Zie voor meer informatie [Ontwerpdetails: Artikeltracering en planning](design-details-item-tracking-and-planning.md).  
  
## <a name="see-also"></a>Zie ook  
[Ontwerpdetails: Artikeltracering](design-details-item-tracking.md)
