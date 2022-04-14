---
title: Assemblagebeheer
description: Ondersteun bedrijven die producten aan hun klanten leveren door componenten te combineren in eenvoudige processen zonder de noodzaak van productiefunctionaliteit.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.search.form: 900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: ce0b3e4208cddba15c7358659e404ba2c868f11c
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8514555"
---
# <a name="assembly-management"></a>Assemblagebeheer
[!INCLUDE[prod_short](includes/prod_short.md)] biedt functies voor het assembleren van artikelen voor bedrijven die via eenvoudige processen, zonder noodzaak voor productiefunctionaliteit, componenten combineren om hun klanten van producten te voorzien. Deze functies kunnen worden geïntegreerd met bestaande functies, zoals verkoop, planning, reserveringen en magazijnbeheer.  

 Een assemblageartikel is gedefinieerd als een verkoopbaar artikel dat een assemblagestuklijst bevat. Zie [Werken met stuklijsten](inventory-how-work-BOMs.md) voor meer informatie.

 Assemblageorders zijn, evenals productieorders, interne orders die worden gebruikt om het assemblageproces te beheren en om de verkoopvereisten aan de betrokken magazijnactiviteiten te koppelen. Assemblageorders verschillen van andere typen omdat deze bij het boeken zowel betrekking kunnen hebben op uitvoer als op verbruik. De assemblageorderkop gedraagt zich op een soortgelijke wijze als een outputdagboekregel en de assemblageorderregels gedragen zich op een soortgelijke wijze als verbruiksdagboekregels.  

 Ter ondersteuning van een just-in-time voorraadstrategie en de mogelijkheid tot het aanpassen van producten op basis van klantaanvragen, kunnen assemblageorders zodra de verkooporderregel is gemaakt automatisch worden gemaakt en worden gekoppeld. De koppeling tussen de verkoopvraag en het assemblage-aanbod stelt de verkooporderverwerkers in staat om het assemblageartikel in een handomdraai aanpassen, om leveringsdatums af te spreken op basis van de beschikbaarheid van componenten en om de uitvoer en verzending van het geassembleerde artikel rechtstreeks vanuit hun verkooporderinterface te boeken. Zie voor meer informatie [Op order geassembleerde artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md).  

 U kunt op een verkooporderregel een beschikbaar aantal dat uit de voorraad moet worden gepickt, verkopen met een aantal dat op basis van de order moet worden geassembleerd. Er bestaan bepaalde regels voor het beheren van de distributie van dergelijke aantallen om ervoor te zorgen dat aantallen voor assemblage op basis van orders voorrang krijgen op voorraadaantallen die betrekking hebben op gedeeltelijke verzending. Zie voor meer informatie de sectie 'Combinatiescenario's' in [Op voorraad assembleren of Op order assembleren begrijpen](assembly-assemble-to-order-or-assemble-to-stock.md).  

 Er bestaan speciale functies voor het beheren van aantallen voor assemblage op basis van orders. Wanneer een aantal voor assembleren op basis van orders klaar is om te worden verzonden, boekt de magazijnmedewerker die verantwoordelijk is voor een voorraadpick de verkooporderregel(s) in kwestie. Dit leidt vervolgens tot het maken van een voorraadverplaatsing voor de componenten, tot het boeken van de assemblage-uitvoer en tot de verkooporderverzending. Zie voor meer informatie de sectie 'Op-order-assembleren-artikelen in voorraadpicks afhandelen' in [Artikelen picken met een voorraadpick](warehouse-how-to-pick-items-with-inventory-picks.md).

De volgende tabel beschrijft een reeks taken, met koppelingen naar de onderwerpen waarin deze worden beschreven.   

|**Als u dit wilt doen**|**Zie**|  
|------------|-------------|  
|Meer informatie weergeven over het verschil tussen het assembleren van artikelen voor het verzenden van verkooporders en het assembleren van artikelen die voor opslag zijn bestemd.|[Op voorraad assembleren of Op order assembleren begrijpen](assembly-assemble-to-order-or-assemble-to-stock.md)|
|Velden op vestigingskaarten en in de voorraadinstellingen invullen om te bepalen hoe artikelen van en naar de assemblageafdeling stromen.|[Standaardmagazijnen met bewerkingsgebieden instellen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|
|Pas een assemblageartikel aan op verzoek van een klant tijdens het verkoopproces en converteer het naar een verkoop wanneer het wordt geaccepteerd.|[Een offerte maken voor een assembleren voor order-verkoop](assembly-how-to-quote-an-assemble-to-order-sale.md)|
|Combineer onderdelen om een artikel te maken in een eenvoudig proces, om te bestellen of in voorraad te plaatsen.|[Artikelen samenstellen](assembly-how-to-assemble-items.md)|  
|Verkoop componenten die nu niet verkrijgbaar zijn door een gekoppelde assemblageorder te maken om het volledige of gedeeltelijke verkooporderaantal te leveren.|[Assembleren voor order-artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md)|
|Als sommige op-order-assembleren-artikelen al in de voorraad zijn, trekt u die hoeveelheid af van de assemblageorder en reserveert u deze vanuit voorraad.|[Voorraadartikelen in assembleren-op-order-stromen verkopen](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)|  
|Wanneer u assemblageartikelen uit voorraad verkoopt en niet alle artikelen zijn beschikbaar, kunt u ook een assemblageorder starten om automatisch een gedeelte van of het hele verkooporderaantal te leveren.|[Op-order-assembleren-artikelen en voorraadartikelen samen verkopen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)|
|Maak aangepaste componenten voor verkoopraamcontracten voordat u periodiek de feitelijke verkooporders maakt volgens de raamcontractovereenkomst.|[Afroepassemblyorders maken](assembly-how-to-create-blanket-assembly-orders.md)|
|Een geboekte assemblyorder ongedaan maken, bijvoorbeeld omdat de order met fouten is geboekt die moeten worden gecorrigeerd.|[Boeken van assemblage ongedaan maken](assembly-how-to-undo-assembly-posting.md)|
|Informatie weergeven over het verschil tussen de assemblagestuklijsten en productiestuklijsten en de bijbehorende verwerkingsverschillen.|[Werken met stuklijsten](inventory-how-work-BOMs.md)|
|Meer informatie weergeven over hoe assemblageverbruik en -output worden verwerkt wanneer u assemblageorders boekt en over hoe het afgeleide artikel- en resourcekosten worden verwerkt en naar het grootboek worden gedistribueerd.|[Ontwerpdetails: Assemblageorderboeking](design-details-assembly-order-posting.md)|  

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/paths/assemble-items-dynamics-365-business-central/)

## <a name="see-also"></a>Zie ook

[Werken met stuklijsten](inventory-how-work-BOMs.md)  
[Voorraad](inventory-manage-inventory.md)  
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)  
<!-- [Walkthrough: Planning Supplies Manually](walkthrough-planning-supplies-manually.md)   -->
<!-- [Walkthrough: Selling, Assembling, and Shipping Kits](walkthrough-selling-assembling-and-shipping-kits.md)   -->
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]