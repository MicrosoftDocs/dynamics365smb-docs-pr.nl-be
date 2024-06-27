---
title: Werken met stuklijsten
description: U maakt een assemblagestuklijst om de onderdelen of resources op te geven die vereist zijn om het artikel samen te stellen dat de assemblagestuklijst vertegenwoordigt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bills of material, assembly BOM, production BOM,'
ms.search.form: null
ms.date: 06/06/2024
ms.service: dynamics-365-business-central
---
# <a name="work-with-bills-of-material"></a>Werken met stuklijsten

U gebruikt stuklijsten om bovenliggende artikelen te structureren die door resources of bewerkingsplaatsen moeten worden geassembleerd uit andere artikelen of geproduceerd van onderdelen.

## <a name="assembly-boms-or-production-boms"></a>Assemblagestuklijsten of productiestuklijsten

[!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt twee verschillende typen stuklijsten:

| Type stuklijst | Algemene categorie | Opmerking |
| -------- | ---------------- | ------- |
| [Assemblagestuklijsten](assembly-how-work-assembly-boms.md) | Magazijn/assemblage | Artikelen die bestaan uit andere artikelen, geassembleerd met basis- of geen resources. |
| [Productiestuklijsten](production-how-to-create-production-boms.md) | Productie | Artikelen die bestaan uit verschillende componenten en subassemblages, geproduceerd in een werk- of bewerkingsplaats. |

Gebruik assemblageorders voor het maken van eindartikelen van onderdelen in een eenvoudig proces dat kan worden uitgevoerd door een of meer basisbronnen die geen bewerkingsplaatsen of -afdelingen betreffen of waarbij geen bronnen gebruikt worden. Een assemblageproces kan bijvoorbeeld zijn het picken van twee flessen wijn en één pak koffie en deze als een cadeau-item verpakken.  

Een assemblagestuklijst betreft de hoofdgegevens die bepalen welke onderdelen gebruikt worden in een samengesteld eindartikel en welke bronnen gebruikt worden voor het samenstellen van het assemblageartikel. Wanneer u een assemblageartikel en een aantal in een nieuwe assemblageorderkop invoert, worden de assemblageorderregels automatisch op basis van de assemblagestuklijst ingevuld met één assemblageorderregel per onderdeel of bron. Zie voor meer informatie [Assemblagebeheer](assembly-assemble-items.md).

U gebruikt productieorders voor het maken van eindartikelen van onderdelen in een complex proces, waarvoor een productiebewerkingsplan en bewerkingsplaatsen of -afdelingen nodig zijn die productiecapaciteit vertegenwoordigen. Een productieproces kan bijvoorbeeld zijn het knippen van stalen platen in één bewerking, deze lassen in een volgende bewerking en het eindartikel verfen in de laatste bewerking. Zie [Productie](production-manage-manufacturing.md) voor meer informatie.

Een productiestuklijst is de stamgegevens die een productieartikel en de componenten erin definieert. Voor componenten moet de productiestuklijst worden gecertificeerd en toegewezen aan het productieartikel voordat het in een productieorder kan worden gebruikt. Wanneer u het productieartikel op een productieorderregel handmatig of door het vernieuwen van de order invoert, wordt de inhoud van de productiestuklijst omgezet in de onderdelen van de productieorder . Zie [Productiestuklijsten maken](production-how-to-create-production-boms.md) voor meer informatie.

Het concept van bronnen in de productie is veel geavanceerder dan in de assemblage. Afdelingen en bewerkingsplaatsen fungeren als hulpmiddelen. De bewerkingen die aan resources in productieroutes zijn toegewezen, vertegenwoordigen productiestappen. Lees meer in het artikel [Bewerkingsplannen maken](production-how-to-create-routings.md).

Zowel assemblage- als productieorders kunnen rechtstreeks aan verkooporders worden gekoppeld. U kunt echter alleen assemblageorders gebruiken om het eindartikel rechtstreeks voor een klantverzoek aan de verkooporder te koppelen.

## <a name="see-also"></a>Zie ook

[Werken met assemblagestuklijsten](assembly-how-work-assembly-boms.md)  
[Productiestuklijsten maken](production-how-to-create-production-boms.md)  
[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Productvarianten beheren](inventory-item-variants.md)  
[Voorraad](inventory-manage-inventory.md)  
[Productie](production-manage-manufacturing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
