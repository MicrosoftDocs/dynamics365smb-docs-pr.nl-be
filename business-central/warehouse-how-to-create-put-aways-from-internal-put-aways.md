---
title: Opslag maken vanuit interne opslag
description: Dit onderwerp behandelt hoe u kunt picken en opslaan zonder een brondocument, zowel hoe u een interne pick maakt als hoe u een interne opslag maakt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 609564faa1e0d5b1e7c364360315ca71b9ba3d06
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8140097"
---
# <a name="pick-and-put-away-without-a-source-document"></a>Picken en opslaan zonder een brondocument
Artikelen die worden opgeslagen om te worden gepickt voor een productieorder of verzending, maken deel uit van de beschikbare voorraad in het magazijn.  

Er kunnen situaties ontstaan waarbij artikelen tijdelijk uit de magazijn-opslaglocaties gehaald moeten worden om bijvoorbeeld als demonstratiemodel te dienen tijdens een verkooppresentatie. Deze artikelen zijn nog steeds eigendom van het bedrijf en maken deel uit van de voorraad, maar ze zijn niet beschikbaar voor picken. Ze worden geregistreerd in een speciale opslaglocatie die u voor dit doel maakt; officieel bevinden de artikelen zich in het magazijn, maar fysiek kunnen ze in een vergadering of demonstratie in gebruik zijn.  

In andere situaties kan de productie-eenheid onverwacht enkele onderdelen nodig hebben voor een proces. U kunt artikelen picken voor productieopslaglocaties met de interne pick. Wanneer het proces uitgevoerd is en de uitvoer wordt gemaakt, kunt u het verbruik van de artikelen boeken en de productieopslaglocatie legen, wat leidt tot een verlaging van het aantal van het artikel op uw locatie.  

Op vergelijkbare wijze kunnen artikelen naar het magazijn worden geretourneerd voor opslag. Het kan bijvoorbeeld voorkomen dat er artikelen uit de beschikbare voorraad worden verwijderd voor een productieorder en vervolgens niet worden gebruikt. Om de artikelen weer toe te voegen aan de beschikbare voorraad, moet u ze opslaan in de opslaglocatie.  

Met **Interne opslag** hebt u de mogelijkheid opslagactiviteiten uit te voeren zonder te verwijzen naar een bepaald brondocument. U kunt eenvoudig alle benodigde gegevens instellen voor een opslagmagazijninstructie.  

> [!NOTE]  
>  Als u geen interne picks en interne opslag gebruikt, kunt u deze correcties uitvoeren door artikelen te verplaatsen tussen opslaglocaties of correcties van aantallen artikelen in een opslaglocatie te boeken.  
>   
>  Als in de vestiging gestuurde opslag en pick wordt gebruikt, en dus opslaglocatiesoorten, kunt u artikelen niet handmatig van of naar de opslaglocatie van het soort Ontvangen verplaatsen, omdat artikelen in deze opslaglocatie moeten worden geregistreerd als opgeslagen voordat ze deel uitmaken van de beschikbare voorraad.  

## <a name="to-create-an-internal-pick"></a>Een interne pick maken  
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Interne mag.-pick** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.
3. Vul het veld **Nr.**, het veld **Vestiging** en het veld **Naar opslaglocatie** in op het sneltabblad **Algemeen**. Het veld **Naar opslaglocatie** geeft aan waar u de gepickte artikelen wilt plaatsen. Voor productiedoeleinden is deze locatie de inkomende productieopslaglocatie of open-shopopslaglocatie. In alle andere gevallen moet u een opslaglocatiecode kiezen van een soort die niet wordt gebruikt voor pickactiviteiten, zoals een opslaglocatie voor staging, verzending of speciale doeleinden.  
4.  Selecteer een artikel in het veld **Artikelnr.** en geef het gewenste pickaantal op.  
5. Kies de actie **Pick maken**. De pickinstructie voor het magazijn kan nu worden uitgevoerd door een magazijnmedewerker. Als alternatief kunt u de actie **Vrijgeven** kiezen en magazijnpicks maken met het **Pickvoorstel**. Zie [Picks plannen in voorstellen](warehouse-how-to-plan-picks-in-worksheets.md) voor meer informatie

## <a name="to-create-an-internal-put-away"></a>Een interne opslag maken  
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Interne mag.-opslag** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.
3. Vul de kop van een nieuwe interne opslag in met ten minste het **nummer**. en de **vestiging**.
4. Vul voor ieder artikel dat u naar het magazijn wilt verplaatsen een regel in. U hoeft alleen de velden **Artikelnr.** en **Aantal** in te vullen.

  > [!NOTE]  
  > Wanneer u het veld **Artikelnr.** kiest, wordt het **Opslaglocatie-inhoudsoverzicht** geopend in plaats van de **artikellijst**. U wilt namelijk een artikel in een bepaalde opslaglocatie - *bininhoud* - opslaan, niet een willekeurig artikel. Bovendien weet u al uit welke opslaglocatie het artikel moet worden gehaald.  <!--If you filled in **From Bin Code** in the header, the bin content will be filtered by value defined in the **From Bin Code**.-->
5. Kies de actie **Opslaglocatie-inhoud ophalen** om de voorstelregels te vullen met de volledige of gefilterde inhoud van de opslaglocaties in de vestiging.  
6. Kies de actie **Opslag maken**. De opslaginstructie voor het magazijn kan nu worden uitgevoerd door een magazijnmedewerker. Als alternatief kunt u de actie **Vrijgeven** kiezen en magazijnopslag maken met het **Opslagvoorstel**. Zie [Opslag plannen in voorstellen](warehouse-how-to-plan-put-aways-in-worksheets.md) voor meer informatie

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
