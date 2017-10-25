---
title: 'Ontwerpdetails: De rol van het tijdsinterval | Microsoft Docs'
description: Het doel van het tijdsinterval is vraaggebeurtenissen binnen het tijdvenster te verzamelen om een gezamenlijke voorzieningenorder te maken.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: eb1b1a401dabe09a77c44558e9f5a83388078aaa
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-the-role-of-the-time-bucket"></a>Ontwerpdetails: De rol van het tijdsinterval
Het doel van het tijdsinterval is vraaggebeurtenissen binnen het tijdvenster te verzamelen om een gezamenlijke voorzieningenorder te maken.  
  
 Voor bestelbeleid dat een bestelpunt gebruikt, kunt u een tijdsinterval opgeven. Dit zorgt ervoor dat de vraag in dezelfde periode wordt opgeteld voordat wordt gecontroleerd wat het effect op de geplande voorraad is en of het bestelpunt is verstreken. Als het bestelpunt is overschreden, wordt een nieuwe voorzieningenorder voorwaarts gepland vanaf het einde van de periode die wordt gedefinieerd door het tijdsinterval. De tijdsintervallen beginnen op de begindatum van de planning.  
  
 Het tijdsinterval geeft het handmatige proces aan om het voorraadniveau op frequente basis te controleren in plaats van voor elke transactie. De gebruiker moet de frequentie (het tijdsinterval) definiëren. De gebruiker verzamelt bijvoorbeeld alle artikelbehoeften van één leverancier om een wekelijkse order te plaatsen.  
  
 ![](media/nav_app_supply_planning_2_reorder_cycle.png "NAV_APP_supply_planning_2_reorder_cycle")  
  
 Het tijdsinterval wordt doorgaans gebruikt om een watervaleffect te voorkomen. Een vereffende rij van vraag en aanbod waarbij bijvoorbeeld een vroege vraag wordt geannuleerd of een nieuwe wordt gemaakt. Het resultaat is dat elke voorzieningenorder (behalve de laatste) opnieuw wordt gepland.  
  
## <a name="see-also"></a>Zie ook  
 [Ontwerpdetails: Bestelbeleid](design-details-reordering-policies.md)   
 [Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md)   
 [Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md)   
 [Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)
