---
title: 'Ontwerpdetails: Boekingsstructuur artikeltracering'
description: Leer hoe u artikelposten gebruikt als de primaire drager van artikeltraceringsnummers in de boekingsstructuur Artikeltracering.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, item tracking, posting, inventory'
ms.date: 06/15/2021
ms.author: edupont
---
# Ontwerpdetails: Boekingsstructuur artikeltracering
Artikelposten worden gebruikt als primaire bron van artikeltraceringsnummers om af te stemmen met de functionaliteit voor voorraadwaardering en om een eenvoudigere en robuustere oplossing te bieden.  
  
Artikeltraceringsnummers van ordernetwerkentiteiten en niet-ordernetwerkentiteiten worden opgegeven in tabel (T337) **Reserveringspost**. Artikeltraceringsnummers die zijn gerelateerd aan historische gegevens, worden direct opgehaald uit de artikelposten die gerelateerd zijn aan de desbetreffende transactie. Dit betekent dat de artikelposten de artikeltraceringspecificatie van de geboekte orderregel aangeven.  
  
Op de pagina **Artikeltraceringsregels** wordt de informatie opgehaald uit T337 en de artikelposten, en wordt deze getoond via de tijdelijke tabel **Traceringsspecificatie** (T336). T336 bevat ook de tijdelijke gegevens op de pagina **Artikeltraceringsregels** voor artikeltraceringsaantallen die nog moet worden gefactureerd.  
  
## Een-op-veel-relatie  
De tabel **Artikelpostrelatie**, die wordt gebruikt om een geboekte documentregel te koppelen aan de gerelateerde artikelposten, bestaat uit twee hoofdonderdelen:  
  
* Een verwijzing naar de geboekte documentregel, het veld **Orderregelnr.**. te kiezen.  
* Een volgnummer dat verwijst naar een artikelpost, het veld **Artikelpostnr.**.  
  
De functionaliteit van het bestaande veld **Volgnummer**, waarmee een artikelpost aan een geboekte documentregel wordt gekoppeld, verwerkt de veelvoorkomende één-op-één-relatie wanneer er geen artikeltraceringsnummers bestaan op de geboekte documentregel. Als er artikeltraceringsnummers bestaan, wordt het veld **Volgnummer** leeg gelaten en wordt de één-op-veel relatie verwerkt door de tabel **Artikelpostrelatie**. Als de geboekte documentregel artikeltraceringsnummers heeft, maar slechts betrekking heeft op één artikelpost, verwerkt het veld **Volgnummer** de relatie en wordt geen record gemaakt in de tabel **Artikelpostrelatie**.  
  
## Codeunits 80 en 90  
Om de artikelposten te splitsen tijdens het boeken, wordt de code in codeunit 80 en 90 omringd door lussen die door globale tijdelijke recordvariabelen lopen. Deze code roept de codeunit 22 aan met een artikeldagboekregel. Deze variabelen zijn geïnitialiseerd wanneer artikeltraceringsnummers aanwezig zijn voor de documentregel. Om de code eenvoudig te houden, wordt deze lusstructuur altijd gebruikt. Als er geen artikeltraceringsnummers bestaan voor de documentregel, wordt één record ingevoegd en wordt de lus slechts eenmaal uitgevoerd.  
  
## Het artikeldagboek boeken  
Artikeltraceringsnummers worden overgebracht via de reserveringsposten die aan de artikelpost relateren, en de koppeling via artikeltraceringsnummers vindt plaats in codeunit 22. Dit concept werkt op dezelfde manier als wanneer een artikeldagboekregel indirect wordt gebruikt om een verkoop- of inkooporder te boeken als wanneer een artikeldagboekregel rechtstreeks wordt gebruikt. Wanneer het artikeldagboek direct wordt gebruikt, wijst het veld **Bronrij-id** naar de artikeldagboekregel zelf.  
  
## Codeunit 22  
Codeunits 80 en 90 lussen de aanroep van codeunit 22 door tijdens de factuurboeking van artikeltraceringsnummers en tijdens het factureren van bestaande verzendingen of ontvangsten.  
  
Tijdens het boeken van aantallen van artikeltraceringsnummers, haalt codeunit 22 artikeltraceringsnummers op van de posten in T337 die betrekking hebben op de boeking. Deze posten worden direct op de artikeldagboekregel geplaatst.  
  
Codeunit 22 doorloopt de artikeltraceringsnummers en splitst de boeking in de respectievelijke artikelposten die de artikeltraceringsnummers hebben. Gegevens over welke artikelposten zijn gemaakt, worden teruggezonden naar T337 door een tijdelijke T336-record gebruiken, die wordt aangeroepen door een procedure in codeunit 22. Deze procedure wordt geactiveerd wanneer de uitvoering van codeunit 22 is beëindigd omdat op dat moment het codeunit 22-object de informatie bevat. Wanneer de tijdelijke record T336 wordt opgehaald, maken codeunits 80 en 90 records in de tabel **Artikelpostrelatie** om de gemaakte artikelposten te koppelen aan de gemaakte verzendings- of ontvangstregel. Codeunit 80 of 90 zet vervolgens de tijdelijke T336-records om in werkelijke T336-records die verband houden met de desbetreffende regel. Deze conversie vindt echter alleen plaats als de geboekte documentregel niet wordt verwijderd, omdat deze slechts gedeeltelijk wordt geboekt.  
  
## Zie ook  
[Ontwerpdetails: Artikeltracering](design-details-item-tracking.md)   
[Ontwerpdetails: Ontwerp artikeltracering](design-details-item-tracking-design.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]