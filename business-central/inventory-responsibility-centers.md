---
title: Werken met divisies | Microsoft Docs
description: Divisies bieden de mogelijkheid tot beheercentra. Een divisie kan een kostencentrum, een winstcentrum, een investeringscentrum of een ander door het bedrijf gedefinieerd administratief centrum zijn.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: ee54a60705a3dff4313522500e9457243ea4907d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "927168"
---
# <a name="work-with-responsibility-centers"></a>Werken met divisies
Divisies bieden mogelijkheden voor beheercentra. Een divisie kan een kostencentrum, een winstcentrum, een investeringscentrum of een ander door het bedrijf gedefinieerd administratief centrum zijn. Voorbeelden van divisies zijn een verkoopkantoor, een inkoopafdeling voor meerdere locaties en een planningskantoor voor een fabriek. Met deze functionaliteit kunnen bedrijven bijvoorbeeld gebruikersspecifieke weergaven instellen van verkoop- en inkoopdocumenten die uitsluitend betrekking hebben op een bepaalde divisie.  

Door meerdere locaties met divisies te gebruiken, kunnen bedrijven hun bedrijfsvoering flexibel maar toch optimaal beheren.

Met meerdere locaties kunnen bedrijven hun voorraad in verschillende locaties met één database beheren. De hoekstenen van deze granule zijn twee concepten: locaties en SKU's. Een locatie is een plaats waar de fysieke plaatsing en aantallen van artikelen worden verzorgd. Het concept is breed genoeg om locaties te omvatten als fabrieken of productieafdelingen, maar ook distributiecentra, magazijnen, showrooms en servicevoertuigen. Een SKU is een artikel op een bepaalde locatie en/of een variant. Met SKU's kunnen bedrijven met meerdere locaties aanvullingsgegevens, adressen en bepaalde financiële boekingsgegevens toevoegen op locatieniveau. Hierdoor kunnen ze varianten van hetzelfde artikel aanvullen voor elke locatie en artikelen bestellen voor elke locatie op basis van locatiespecifieke aanvullingsgegevens.  

De functionaliteit voor meerdere locaties wordt uitgebreid met divisies, doordat gebruikers administratieve centra kunnen afhandelen. Een divisie kan een kostencentrum, een winstcentrum, een investeringscentrum of een ander door het bedrijf gedefinieerd administratief centrum zijn. Voorbeelden van divisies zijn een verkoopkantoor, een inkoopafdeling voor meerdere locaties en een planningskantoor voor een fabriek. Met deze functionaliteit kunnen bedrijven bijvoorbeeld gebruikersspecifieke weergaven instellen van verkoop- en inkoopdocumenten die uitsluitend betrekking hebben op een bepaalde divisie.

## <a name="to-set-up-a-responsibility-center"></a>Een divisie instellen  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Divisies** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Nieuw**.  
3.  Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Als u divisies gebruikt om uw bedrijf te beheren, kan het handig zijn om een standaarddivisie voor uw bedrijf te hebben.
4. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bedrijfsgegevens** in en kies vervolgens de gerelateerde koppeling.
5. Voer in het veld **Divisie** een divisiecode in.

Deze code wordt in alle inkoop-, verkoop- of servicedocumenten gebruikt als de gebruiker, klant of leverancier geen standaarddivisie heeft. In elk verkoop-, inkoop- of servicedocument kunt u een andere divisie invoeren dan de standaarddivisie.

> [!NOTE]  
>  Wanneer u een divisiecode in een document invoert, heeft dit invloed op het adres, de dimensies en de prijzen in het document.  

## <a name="to-assign-responsibility-centers-to-users"></a>Divisies toewijzen aan gebruikers  
Voor gebruikers kunt u instellen dat tijdens de dagelijkse handelingen alleen de documenten worden opgehaald die van toepassing zijn op de werkgebieden van de gebruikers. Doorgaans zijn gebruikers verbonden aan een divisie en werken ze alleen met documenten die van toepassing zijn op de bepaalde modules voor deze divisie.  

Als u dit wilt instellen, moet u divisies toewijzen aan gebruikers in drie basismodules: Inkoop, Verkoop en CRM - Service.  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikersinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2.  Ga op de pagina **Gebruikersinstellingen** naar de gebruiker waaraan u een divisie wilt toewijzen. Als de gebruiker niet voorkomt in het overzicht, moet u een gebruikers-id invoeren in het veld **Gebruikers-id**.  
3.  In het veld **Verkoopdivisiefilter** voert u de divisie in waaraan de verkooptaken van de gebruiker zijn gekoppeld.  
4.  In het veld **Inkoopdivisiefilter** voert u de divisie in waaraan de inkooptaken van de gebruiker zijn gekoppeld.  
5.  In het veld **Servicedivisiefilter** voert u de divisie in waaraan de servicebeheertaken van de gebruiker zijn gekoppeld.  

> [!NOTE]  
>  Gebruikers kunnen nog steeds alle geboekte documenten en posten bekijken, niet alleen de documenten en posten die horen bij de betreffende divisie.

## <a name="see-also"></a>Zie ook  
[Voorraad instellen](inventory-setup-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)
[Voorraad](inventory-manage-inventory.md)[Voorraadbeheer](warehouse-manage-warehouse.md)  
[Magazijnbeheer](warehouse-manage-warehouse.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
