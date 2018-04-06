---
title: Artikelen verplaatsen | Microsoft Docs
description: Artikelen op voorraad moeten soms tussen locaties worden verplaatst ter ondersteuning van de dagelijkse magazijnactiviteiten die worden uitgevoerd om artikelen in het magazijn te laten stromen. Sommige verplaatsingen houden rechtstreeks verband met interne bewerkingen, zoals een productieorder waarvoor componenten moeten worden geleverd of waarvoor eindartikelen moeten worden opgeslagen. Andere verplaatsingen vinden plaats ten behoeve van magazijnruimte-optimalisatie of als ad hoc verplaatsingen naar en van bewerkingen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6efb709151ea98b5c8d89d67138b52bac5751c56
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="moving-items"></a>Artikelen verplaatsen
De magazijnactiviteit van het verplaatsen van artikelen in het magazijn wordt op verschillende manieren uitgevoerd, afhankelijk van hoe de functies voor magazijnbeheer zijn geconfigureerd. De complexiteit varieert, van geen magazijnfuncties via standaardmagazijnconfiguraties voor de afzonderlijke verwerking van orders in een of meer activiteiten tot geavanceerde configuraties waarbij alle activiteiten in een gestuurde werkstroom moeten worden uitgevoerd. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).

Artikelen in één magazijnlocatie moeten soms tussen opslaglocaties worden verplaatst ter ondersteuning van de dagelijkse magazijnactiviteiten die worden uitgevoerd om artikelen in het magazijn te laten stromen. Sommige verplaatsingen houden rechtstreeks verband met interne bewerkingen, zoals een productieorder waarvoor componenten moeten worden geleverd of waarvoor eindartikelen moeten worden opgeslagen. Andere verplaatsingen vinden plaats ten behoeve van magazijnruimteoptimalisatie of als ad hoc verplaatsingen naar en van bewerkingen.

Het verplaatsen van artikelen naar andere vestigingen heeft zijn weerslag op de artikelposten en moet daarom met een transferorder worden uitgevoerd. Zie voor meer informatie [Voorraad overbrengen tussen vestigingen](inventory-how-transfer-between-locations.md).  

Aanvullende verplaatsingstaken zijn bedoeld om periodiek pickopslaglocaties shopflooropslaglocaties aan te vullen en de informatie over de inhoud van de opslaglocaties te wijzigen.  

 In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.   

|**Als u dit wilt doen**|**Zie**|  
|------------|-------------|  
|Verplaats artikelen op elk gewenst moment en zonder brondocumenten tussen opslaglocaties in standaardmagazijnconfiguraties.|[Artikelen verplaatsen in standaardmagazijnconfiguraties](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)|
|Gebruik het magazijnverplaatsingsvoorstel om artikelen in geavanceerde magazijnconfiguraties ad hoc of voor brondocumenten te verplaatsen.|[Artikelen verplaatsen in geavanceerde magazijnconfiguraties](warehouse-how-to-move-items-in-advanced-warehousing.md)|  
|Breng componentartikelen naar interne bewerkingen in standaardmagazijnconfiguraties, zoals via brondocumenten voor deze bewerkingen wordt aangevraagd.|[Onderdelen verplaatsen naar een bewerkingsgebied in standaardmagazijnconfiguraties](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)|
|Plannen welke opslaglocaties moeten worden gevuld of geleegd om een efficiënte stroom te behouden, zoals het legen van een bulkopslaggebied voor een grote ontvangst.|[Plannen van magazijnverplaatsingen in werkbladen](warehouse-how-to-plan-warehouse-movements-in-worksheets.md)|
|De frequentie bijwerken waarmee opslaglocaties, zoals pickingopslaglocaties, moeten worden aangevuld als gevolg van schommelingen in de vraag.|[Opslaglocatieaanvulling berekenen](warehouse-how-to-calculate-bin-replenishment.md)|
|De magazijnstructuur aanpassen met nieuwe opslaglocatiecodes en -kenmerken.|[Magazijnen herstructureren](warehouse-how-to-restructure-warehouses.md)|  

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

