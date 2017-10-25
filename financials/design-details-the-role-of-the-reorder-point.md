---
title: 'Ontwerpdetails: De rol van het bestelpunt | Microsoft Docs'
description: In dit onderwerp wordt het belang van het instellen van een bestelpunt aangegeven, zodat u weet wanneer u meer voorraad moet bestellen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5b5e3cec4bc5af8188470ea1d711422c0130677e
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-the-role-of-the-reorder-point"></a>Ontwerpdetails: De rol van het bestelpunt
Naast de algemene afstemming van vraag en aanbod, moet het planningssysteem ook voorraadniveaus voor de betrokken artikelen controleren om rekening te houden met gedefinieerd bestelbeleid.  
  
Een bestelpunt vertegenwoordigt vraag tijdens doorlooptijd. Wanneer de geplande voorraad onder het voorraadniveau komt dat door het bestelpunt is gedefinieerd, is het tijd om het bestelaantal te verhogen. Ondertussen wordt verwacht dat de voorraad afneemt en mogelijk nul wordt (of het veiligheidsvoorraadniveau bereikt), totdat de aanvulling plaatsvindt.  
  
Het planningssysteem zal een voorwaarts geplande voorzieningenorder voorstellen op het moment dat de verwachte voorraad onder het bestelpunt komt.  
  
Het bestelpunt geeft een bepaald voorraadniveau aan. Voorraadniveaus kunnen tijdens het tijdsinterval echter aanzienlijk schommelen en daarom moet het planningssysteem constant de geplande beschikbare voorraad controleren.  
  
## <a name="see-also"></a>Zie ook  
[Ontwerpdetails: Bestelbeleid](design-details-reordering-policies.md)   
[Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md)   
[Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md)   
[Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)
