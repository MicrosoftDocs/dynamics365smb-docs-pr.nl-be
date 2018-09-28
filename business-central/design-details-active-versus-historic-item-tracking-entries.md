---
title: 'Ontwerpdetails: Actieve tegenover historische artikeltraceringsposten | Microsoft Docs'
description: Wanneer delen van een documentregelaantal worden geboekt, wordt alleen dat bepaalde aantal overgebracht naar de artikelposten en de bijbehorende artikeltraceringsnummers. U zult echter direct vanaf de actieve documentregel toegang willen tot alle relevante artikeltraceringsinformatie. U wilt dus niet alleen de posten bekijken die zijn gekoppeld aan het resterende aantal, u wilt ook informatie over de eenheden die zijn geboekt. Wanneer u het venster **Artikeltraceringsregels** weergeeft of wijzigt, wordt de collectieve inhoud van de tabel **Traceringsspecificatie** (T336) en de tabel **Reserveringspost** (T337) weergegeven in een tijdelijke versie van T336. Hierdoor wordt gezorgd dat de historische en actieve artikeltraceringsgegevens gezamenlijk toegankelijk zijn.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 34654f907759bc0bdfcb2fb2f1265a74cdcdce4f
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-active-versus-historic-item-tracking-entries"></a>Ontwerpdetails: Actieve tegenover historische artikeltraceringsposten
Wanneer delen van een documentregelaantal worden geboekt, wordt alleen dat bepaalde aantal overgebracht naar de artikelposten en de bijbehorende artikeltraceringsnummers. U zult echter direct vanaf de actieve documentregel toegang willen tot alle relevante artikeltraceringsinformatie. U wilt dus niet alleen de posten bekijken die zijn gekoppeld aan het resterende aantal, u wilt ook informatie over de eenheden die zijn geboekt. Wanneer u het venster **Artikeltraceringsregels** weergeeft of wijzigt, wordt de collectieve inhoud van de tabel **Traceringsspecificatie** (T336) en de tabel **Reserveringspost** (T337) weergegeven in een tijdelijke versie van T336. Hierdoor wordt gezorgd dat de historische en actieve artikeltraceringsgegevens gezamenlijk toegankelijk zijn.  

 De volgende tabel toont hoe T336 en T337 worden gebruikt in een inkoopscenario. De vet gedrukte cijfers vertegenwoordigen waarden die de gebruiker handmatig invoert in het venster **Artikeltraceringsregels**.  

 Stap 1: Maak een inkooporderregel van zeven stuks met artikeltraceringsnummers.  

||**Aantal (Basis)**|**Te verwerken aantal**|**Te factureren aantal (Basis)**|**Verwerkt aantal (Basis)**|**Gefactureerd aantal (Basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**T337**|7|0|0|0|0|  
|**T336**|0|0|0|0|0|  

 Stap 2: Ontvang vier stuks.  

||**Aantal (Basis)**|**Te verwerken aantal**|**Te factureren aantal (Basis)**|**Verwerkt aantal (Basis)**|**Gefactureerd aantal (Basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Venster **Artikeltraceringsregels**|7|**4**|**0**|0|0|  
|**T337**|3|0|0|0|0|  
|**T336**|4|0|0|4|0|  

 Stap 3: Ontvang twee stuks en factureer twee stuks.  

||**Aantal (Basis)**|**Te verwerken aantal**|**Te factureren aantal (Basis)**|**Verwerkt aantal (Basis)**|**Gefactureerd aantal (Basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Venster **Artikeltraceringsregels**|7|**2**|**2**|4|0|  
|**T337**|1|0|0|0|0|  
|**T336**|6|0|0|6|2|  

 Stap 4: Ontvang één stuk.  

||**Aantal (Basis)**|**Te verwerken aantal**|**Te factureren aantal (Basis)**|**Verwerkt aantal (Basis)**|**Gefactureerd aantal (Basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Venster **Artikeltraceringsregels**|7|**1**|**0**|6|2|  
|**T336**|7|0|0|7|2|  

 Factureer 5 stuks.  

||**Aantal (Basis)**|**Te verwerken aantal**|**Te factureren aantal (Basis)**|**Verwerkt aantal (Basis)**|**Gefactureerd aantal (Basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Venster **Artikeltraceringsregels**|7|0|**5**|7|2|  
|**T336**|7|0|0|7|7|  

## <a name="see-also"></a>Zie ook  
 [Ontwerpdetails: Artikeltracering](design-details-item-tracking.md)   
 [Ontwerpdetails: Venster Artikeltraceringsregels](design-details-item-tracking-lines-window.md)

