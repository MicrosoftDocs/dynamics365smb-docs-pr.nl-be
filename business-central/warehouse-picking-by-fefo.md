---
title: Picken volgens FEFO inschakelen | Microsoft Docs
description: Eerste-verlopen-First-Out (FEFO) is een sorteringsmethode die ervoor zorgt dat de oudste artikelen, die met de vroegste vervaldata, eerst worden gepickt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 3a47c9daeeab036055a0644e1b389735f7440106
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784079"
---
# <a name="enable-picking-items-by-fefo"></a>Artikelen picken volgens FEFO inschakelen
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

## <a name="see-also"></a>Zie ook  
[artikelen picken](warehouse-pick-items.md)   
[Picken van artikelen voor magazijnverzending](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Artikelen picken met een voorraadpick](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]