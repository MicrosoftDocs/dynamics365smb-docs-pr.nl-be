---
title: Assembleren op order voor project
description: Meer informatie over hoe assembleren op order kunt gebruiken voor projecten.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'project management, task'
ms.search.form: '88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020'
ms.date: 08/03/2022
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="assemble-to-project"></a>Assembleren voor project

Met assembleren voor projecten kunt u het voorraadbeheer verbeteren door alleen op order te assembleren wanneer dat nodig is.

Wanneer u een op-order-assembleren-artikel op een projectplanningsregel kiest, wordt met [!INCLUDE [prod_short](includes/prod_short.md)] een assemblageorder gemaakt. De assemblageorder is gebaseerd op de projectplanningsregel en de regels ervan zijn gebaseerd op de assemblagestuklijst van het artikel. Ga voor meer informatie over assemblagestuklijsten naar [Werken met assemblagestuklijsten](assembly-how-work-assembly-boms.md). Het aantal materialen op de assemblagestuklijst wordt vermenigvuldigd met de orderhoeveelheid. De pagina **Op orderregels assembleren** toont details over de gekoppelde assemblageorderregels. De details kunnen u helpen bij het aanpassen van het assemblageartikel. Net als bij de verkoop kunt u gekoppelde assemblageorders niet rechtstreeks boeken. Ga voor meer informatie over assemblageorders naar [Voorraadartikelen in op-order-assembleren-stromen verkopen](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).

Assemblageorders zijn gereserveerd voor projecten, en [!INCLUDE [prod_short](includes/prod_short.md)] synchroniseert artikeltracering tussen projectplanningsregels en assemblageorder.

## <a name="integrate-with-warehouse-management"></a>Integreren met Warehouse Management

Assembleren voor project wordt geïntegreerd met magazijnbeheerfuncties om de assemblage en verzending eenvoudiger te maken. Het proces zorgt er ook voor dat de stroom van projectmontage tot levering soepel verloopt in interne magazijnprocessen. Ga voor meer informatie over interne magazijnstromen voor projecten naar [Stromen voor productie, assemblage en projecten](design-details-internal-warehouse-flows.md#flows-to-and-from-assembly-in-a-basic-warehouse-configuration).

De volgende tabel beschrijft de magazijnconfiguraties die door op order assembleren worden ondersteund.

|Configuratie  |Omschrijving  |
|---------|---------|
|**Geen magazijnverwerking**|Gebruik een projectdagboek om volledig of gedeeltelijk gebruik te boeken. De output en het verbruik van onderdelen worden automatisch geboekt voor de assemblageorder.         |
|**Voorraadpick**|Gebruik een voorraadpick om volledig of gedeeltelijk gebruik te boeken. De output en het verbruik van onderdelen worden automatisch geboekt voor de assemblageorder.          |
|**Magazijnpick**|Maak en registreer magazijnpicks voor onderdelen en gebruik vervolgens een projectdagboek om het gebruik te boeken. [!INCLUDE [prod_short](includes/prod_short.md)] controleert of de verbruikte assemblageonderdelen zijn gepickt. De output en het verbruik van onderdelen worden automatisch geboekt voor de assemblageorder.         |

## <a name="known-limitations"></a>Bekende beperkingen

In dit gedeelte worden bekende beperkingen voor assembleren voor project beschreven.

* Het veld **Aantal voor op order assembleren** is niet beschikbaar voor projecten die zijn gesloten.
* Voor magazijnpickscenario's kan **Aantal voor op order assembleren** nul zijn of gelijk zijn aan het aantal. Op een projectplanningsregel kunt u assembleren op order en assembleren op voorraad niet combineren. U moet afzonderlijke projectplanningsregels maken.
* Op order assembleren heeft geen invloed op de factureerbare delen van een project. Op verkoopfacturen wordt een assemblage vermeld, maar niet de onderdelen ervan. U kunt het veld **Aantal voor op order assembleren** voor factureerbare regels niet bewerken.
* De orderplanning en het planningsvoorstel worden niet beïnvloed, omdat het project de input voor de planning is. De planningsengine beschouwt de assemblage als vraag.
* U kunt geen negatief aantal invoeren in het veld **Aantal voor op order assembleren**.
* U kunt een assemblage niet ongedaan maken.

## <a name="see-also"></a>Zie ook

[Projectbeheer](projects-manage-projects.md)  
[Assemblage](assembly-assemble-items.md)  
[Projecten maken](projects-how-create-jobs.md)
