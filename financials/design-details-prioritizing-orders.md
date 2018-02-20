---
title: 'Ontwerpdetails: Prioriteit geven aan orders | Microsoft Docs'
description: Lees hoe u prioriteiten stelt om aan de vereisten van vraag en aanbod te voldoen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, priority, prioritize, order, sku, demand, supply
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7af645f5a9dd7f34619d05cb2d4f0f7f8ad1921d
ms.contentlocale: nl-be
ms.lasthandoff: 12/14/2017

---
# <a name="design-details-prioritizing-orders"></a>Ontwerpdetails: Prioriteit geven aan orders
Binnen een bepaalde SKU staat de verzochte of beschikbare datum voor de hoogste prioriteit; de vraag van vandaag moet worden verwerkt vóór de vraag van volgende week. Naast deze algemene prioriteit zal het planningssysteem ook voorstellen aan welk soort vraag moet worden voldaan voordat aan andere vraag wordt voldaan. Zo wordt ook voorgesteld welke voorzieningenbron moet worden toegepast voordat andere voorzieningenbronnen worden toegepast. Dit gebeurt op basis van orderprioriteiten.  
  
Geladen vraag en aanbod dragen bij aan een profiel voor de voorspelde voorraad op basis van de volgende prioriteiten:  
  
## <a name="priorities-on-the-demand-side"></a>Prioriteiten aan de vraagkant  
1. Al verzonden: Artikelpost  
2. Inkoopretourorder  
3. Verkooporder  
4. Onderhoudsorder  
5. Behoefte aan productieonderdelen  
6. Assemblageorderregel  
7. Uitgaande transferorder  
8. Raamcontract (dat niet al is verbruikt door verwante verkooporders)  
9. Prognose (die niet al is verbruikt door andere verkooporders)  
  
> [!NOTE]  
>  Inkoopretouren zijn meestal niet betrokken bij voorraadplanning; ze moeten altijd worden gereserveerd vanuit de lot die geretourneerd zal worden. Indien niet gereserveerd, spelen inkoopretouren een rol in de beschikbaarheid en hebben ze een hoge prioriteit om te voorkomen dat het planningssysteem een voorzieningenorder voorstelt, puur met het oog op een inkoopretour.  
  
## <a name="priorities-on-the-supply-side"></a>Prioriteiten aan de aanbodkant  
1. Al in voorraad: Artikelpost (Planningsflexibiliteit = geen)  
2. Verkoopretourorder (Planningsflexibiliteit = Geen)  
3. Inkomende transferorder  
4. Productieorder  
5. Assemblageorder  
6. Inkooporder  
  
## <a name="priority-related-to-the-state-of-demand-and-supply"></a>Prioriteit met betrekking tot de status van vraag en aanbod  
Afgezien van prioriteiten als gevolg van het soort vraag en aanbod geeft de huidige status van de orders in het uitvoeringsproces ook een prioriteit aan. Magazijnactiviteiten hebben bijvoorbeeld invloed en er wordt rekening gehouden met de status van verkoop-, inkoop-, transfer-, assemblage- en productieorders:  
  
1. Gedeeltelijk verwerkt (Planningsflexibiliteit = Geen)  
2. Al in verwerking in het magazijn (Planningsflexibiliteit = geen)  
3. Vrijgegeven - alle ordersoorten (Planningsflexibiliteit = Onbeperkt)  
4. Vaste geplande productieorder (Planningsflexibiliteit = Onbeperkt)  
5. Gepland/open - alle ordersoorten (Planningsflexibiliteit = Onbeperkt)  
  
## <a name="see-also"></a>Zie ook  
[Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md)   
[Ontwerpdetails: Centrale begrippen van het planningssysteem](design-details-central-concepts-of-the-planning-system.md)   
[Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)
