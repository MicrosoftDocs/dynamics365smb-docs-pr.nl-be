---
title: Picken volgens FEFO inschakelen | Microsoft Docs
description: Eerste-verlopen-First-Out (FEFO) is een sorteringsmethode die ervoor zorgt dat de oudste artikelen, die met de vroegste vervaldata, eerst worden gepickt.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e4ee3dc56de6c4ca6b6229c0b436c9407d73534a
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="enable-picking-items-by-fefo"></a>Artikelen picken volgens FEFO inschakelen
First-Expired-First-Out (FEFO) is een sorteringsmethode die ervoor zorgt dat de oudste artikelen, die met de vroegste vervaldata, eerst worden gepickt.  

 Deze functie werkt alleen wanneer aan de volgende criteria wordt voldaan:  

-   Het artikel moet een serie-/partijnummer hebben.  
-   Op de tracking-code van het artikel moet het veld **Serienr. specifieke magazijn tracering** of **Partij-specifieke magazijn tracering** worden geselecteerd.  
-   Het artikel moet met een verloopdatum naar de voorraad worden geboekt.  
-   Op de vestigingskaart moet het selectievakje **Picken vereisen** zijn ingeschakeld.  
-   Op de vestigingskaart moet het selectievakje **Picken volgens FEFO** zijn ingeschakeld.  
-   Op de vestigingskaart moet het selectievakje **Opslaglocatie verplicht** zijn ingeschakeld.  

 Wanneer aan alle criteria wordt voldaan, worden artikelen met serie- of partijnummers die moeten worden gepickt, gesorteerd met de oudste eerst bij alle picks en verplaatsingen, behalve artikelen waarvoor specifieke tracering van Serienr. of partijnummer plaatsvindt.  

> [!NOTE]  
>  Indien voor sommige artikelen met serie- of partijnummers specifieke tracering plaatsvindt, wordt dit eerst nageleefd en worden daarna de overige, niet-specifieke, serie- en partijnummers gerangschikt volgens FEFO.  

 Als twee artikelen met serie- of lotnummer dezelfde vervaldatum hebben, wordt het artikel met het laagste lot- of serienummer geselecteerd. Als de lot- of serienummers gelijk zijn, wordt het artikel geselecteerd dat als eerste is geregistreerd.  

> [!NOTE]  
>  -   Tijdens het picken van artikelen met een serie-/lotnummer op locaties die zijn ingesteld op gestuurde opslag en pick, worden alleen aantallen in locaties van het type *Pick* gepicked volgens FEFO.  
> -   U kunt verplaatsingen volgens FEFO mogelijk maken, hetzij in het venster **Voorraadverplaatsing** of **Werkblad verplaatsing**, door het veld **Uit opslaglocatie** leeg te maken.  
> -   Als het veld **Strikte vervaldatumboeking** is ingeschakeld, worden alleen artikelen die niet zijn verlopen, opgenomen in de pick. Dit geldt ook als u niet picken volgens FEFO gebruikt.  

## <a name="see-also"></a>Zie ook  
[artikelen picken](warehouse-pick-items.md)   
[Picken van artikelen voor magazijnverzending](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Artikelen picken met een voorraadpick](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

