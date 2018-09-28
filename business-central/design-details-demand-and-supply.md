---
title: 'Ontwerpdetails: Vraag en aanbod | Microsoft Docs'
description: Vraag is de verzamelterm voor elk soort brutovraag, zoals een verkooporder en materiaalbehoefte van een productieorder. Bovendien staat het programma meer technische soorten vraag toe, zoals negatieve voorraad en inkoopretouren
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
ms.openlocfilehash: db4defc0a2bccd7c4aaa69cd06832c486178e70a
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-demand-and-supply"></a>Ontwerpdetails: Vraag en aanbod
Vraag is de verzamelterm voor elk soort brutovraag, zoals een verkooporder en materiaalbehoefte van een productieorder. Bovendien staat het programma meer technische soorten vraag toe, zoals negatieve voorraad en inkoopretouren  
  
 Voorziening is de algemene term voor elke soort positief of inkomend aantal, zoals voorraad, inkopen, assemblage, productie of inkomende transfers. Een verkoopretour kan bovendien ook voorziening vertegenwoordigen.  
  
 Om de vele bronnen van vraag en voorzieningen te sorteren, ordent het planningssysteem deze op twee tijdpaden die voorraadprofielen worden genoemd. Eén profiel bevat vraaggebeurtenissen en het andere bevat de corresponderende voorzieninggebeurtenissen. Elke gebeurtenis vertegenwoordigt een entiteit uit het ordernetwerk, bijvoorbeeld een verkooporderregel, een artikelpost of een productieorderregel.  
  
 Wanneer voorraadprofielen worden geladen, worden de verschillende vraag-voorzieningcombinaties vereffend om een voorzieningenplan uit te voeren dat aan de genoemde doelstellingen voldoet.  
  
 Planningsparameters en voorraadniveaus zijn respectievelijk andere soorten vraag en aanbod, die geïntegreerde afstemming ondergaan om voorraadartikelen aan te vullen. Zie voor meer informatie [Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md).  
  
## <a name="see-also"></a>Zie ook  
 [Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md)   
 [Ontwerpdetails: Centrale begrippen van het planningssysteem](design-details-central-concepts-of-the-planning-system.md)   
 [Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)
