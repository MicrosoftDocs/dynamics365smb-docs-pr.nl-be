---
title: 'Ontwerpdetails: De rol van het bestelpunt | Microsoft Docs'
description: In dit onderwerp wordt het belang van het instellen van een bestelpunt aangegeven, zodat u weet wanneer u meer voorraad moet bestellen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: desigh, reorder, demand, supply
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: e39a7efdc796e8745bd9d8f7d74cdcfb171d851f
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "817198"
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
