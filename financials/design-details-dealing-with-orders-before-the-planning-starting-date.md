---
title: 'Ontwerpdetails: Werken met orders voor de geplande begindatum | Microsoft Docs'
description: In dit onderwerp worden de regels beschreven die door planning op orders worden toegepast in de vaste zone.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: planning, frozen, design serial, lot
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5545fe1c2c8833eb1c97765f261777cbb1781098
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-dealing-with-orders-before-the-planning-starting-date"></a>Ontwerpdetails: Werken met orders voor de geplande begindatum
Om te voorkomen dat een voorzieningenplan onmogelijke en daarom nutteloze voorstellen toont, beschouwt het planningssysteem de periode tot de begindatum van de planning als een vaste zone waarvoor niets wordt gepland. De volgende regel geldt voor de vaste zone:  
  
Alle vraag en aanbod vóór de begindatum van de planningsperiode wordt beschouwd als deel van de voorraad of wordt verzonden.  
  
Het planningssysteem zal, met enkele uitzonderingen, geen wijzigingen in voorzieningenorders in de vaste zone voorstellen en er worden voor die periode geen ordertraceringskoppelingen gemaakt of onderhouden.  
  
De uitzonderingen op deze regel zijn als volgt:  
  
* Als de verwachte beschikbare voorraad, inclusief totale vraag en aanbod in de vaste zone, lager is dan nul.  
* Als serie-/lotnummers vereist zijn op de geantidateerde order(s).  
* Als de aanbod/vraag-combinatie is gekoppeld door een order-aan-order beleid.  
  
Als de eerste beschikbare voorraad onder nul is, wordt er op de dag vóór de planningsperiode door het planningssysteem een noodvoorzieningenorder voorgesteld voor het ontbrekende aantal. Dus is de voorspelde en beschikbare voorraad altijd minstens nul wanneer het plannen voor de toekomstige periode begint. De planningsregel voor deze voorzieningenorder geeft een waarschuwingspictogram Noodgeval weer en er worden extra gegevens getoond bij het opzoeken.  
  
## <a name="seriallot-numbers-and-order-to-order-links-are-exempt-from-the-frozen-zone"></a>Serie-/lotnummers en order-naar-order koppelingen zijn vrijgesteld van de vaste zone  
Als serie-/lotnummers vereist zijn of als een order-naar-order koppeling bestaat, zal het planningssysteem de vaste zone negeren en zulke aantallen opnemen die geantidateerd zijn vanaf de begindatum, en mogelijk corrigerende acties voorstellen als vraag en aanbod niet zijn gesynchroniseerd. De bedrijfsreden voor dit principe is dat dergelijke specifieke vraag-voorzieningcombinaties moeten overeenkomen om te zorgen dat aan deze specifieke vraag wordt voldaan.  
  
## <a name="see-also"></a>Zie ook  
[Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md)   
[Ontwerpdetails: Centrale begrippen van het planningssysteem](design-details-central-concepts-of-the-planning-system.md)   
[Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)
