---
title: Picken volgens FEFO inschakelen | Microsoft Docs
description: 'Eerste-verlopen-First-Out (FEFO) is een sorteringsmethode die ervoor zorgt dat de oudste artikelen, die met de vroegste vervaldata, eerst worden gepickt.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Artikelen picken volgens FEFO inschakelen
First-Expired-First-Out (FEFO) is een sorteringsmethode die ervoor zorgt dat de oudste artikelen, die met de vroegste vervaldata, eerst worden gepickt.  

 Deze functie werkt alleen wanneer aan de volgende criteria wordt voldaan:  

-   Het artikel moet een serie-/partijnummer hebben.  
-   Op de tracking-code van het artikel moet het veld **Magazijnserienr.-tracering** of **Magazijnlottracering** worden geselecteerd.  
-   Het artikel moet met een verloopdatum naar de voorraad worden geboekt.  
-   Op de locatie moeten de schakelaars **Pick vereist**, **Picken volgens FEFO** en **Opslaglocatie verplicht** zijn ingeschakeld.  

 Wanneer aan alle criteria wordt voldaan, worden artikelen met serie- of partijnummers die moeten worden gepickt, gesorteerd met de oudste eerst bij alle picks en verplaatsingen, behalve artikelen waarvoor specifieke tracering van Serienr. of partijnummer plaatsvindt.  

> [!NOTE]  
> Indien voor sommige artikelen met serie- of partijnummers specifieke tracering plaatsvindt, wordt dit eerst nageleefd en worden daarna de overige, niet-specifieke, serie- en partijnummers gerangschikt volgens FEFO.
<br /><br />
Als twee artikelen met serie- of lotnummer dezelfde vervaldatum hebben, wordt het artikel met het laagste lot- of serienummer geselecteerd.
<br /><br />
Tijdens het picken van artikelen met een serie- of lotnummer op locaties die zijn ingesteld op gestuurde opslag en pick, worden alleen aantallen in locaties van het type *Pick* gepickt volgens FEFO.  
<br /><br />
Als u verplaatsingen volgens FEFO mogelijk wilt maken, laat u het veld **Van opslaglocatie** leeg op de pagina **Voorraadverplaatsing** of **Verplaatsingsvoorstel**.  
<br /><br />
Als het veld **Strikte verloopdatumboeking** is geselecteerd op de kaart met de **Artikeltraceringscode**, worden alleen artikelen die niet zijn verlopen, in de pick opgenomen en worden de regels gesorteerd volgens het FEFO-principe.

## Zie ook  
[Picken van artikelen voor magazijnverzending](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Artikelen picken met een voorraadpick](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]