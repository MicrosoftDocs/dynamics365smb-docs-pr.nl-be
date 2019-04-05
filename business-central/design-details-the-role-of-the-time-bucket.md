---
title: 'Ontwerpdetails: De rol van het tijdsinterval | Microsoft Docs'
description: Het doel van het tijdsinterval is vraaggebeurtenissen binnen het tijdskader te verzamelen om een gezamenlijke voorzieningenorder te maken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: ff748a192d8d1650a708ab70ec33ccc7bfd53c48
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816312"
---
# <a name="design-details-the-role-of-the-time-bucket"></a>Ontwerpdetails: De rol van het tijdsinterval
Het doel van het tijdsinterval is vraaggebeurtenissen binnen het tijdskader te verzamelen om een gezamenlijke voorzieningenorder te maken.  

 Voor bestelbeleid dat een bestelpunt gebruikt, kunt u een tijdsinterval opgeven. Dit zorgt ervoor dat de vraag in dezelfde periode wordt opgeteld voordat wordt gecontroleerd wat het effect op de geplande voorraad is en of het bestelpunt is verstreken. Als het bestelpunt is overschreden, wordt een nieuwe voorzieningenorder voorwaarts gepland vanaf het einde van de periode die wordt gedefinieerd door het tijdsinterval. De tijdsintervallen beginnen op de begindatum van de planning.  

 Het tijdsinterval geeft het handmatige proces aan om het voorraadniveau op frequente basis te controleren in plaats van voor elke transactie. De gebruiker moet de frequentie (het tijdsinterval) definiëren. De gebruiker verzamelt bijvoorbeeld alle artikelbehoeften van één leverancier om een wekelijkse order te plaatsen.  

 ![Voorbeeld van tijdverzameling bij planning](media/nav_app_supply_planning_2_reorder_cycle.png "Voorbeeld van tijdverzameling bij planning")  

 Het tijdsinterval wordt doorgaans gebruikt om een watervaleffect te voorkomen. Een vereffende rij van vraag en aanbod waarbij bijvoorbeeld een vroege vraag wordt geannuleerd of een nieuwe wordt gemaakt. Het resultaat is dat elke voorzieningenorder (behalve de laatste) opnieuw wordt gepland.  

## <a name="see-also"></a>Zie ook  
 [Ontwerpdetails: Bestelbeleid](design-details-reordering-policies.md)   
 [Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md)   
 [Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md)   
 [Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)
