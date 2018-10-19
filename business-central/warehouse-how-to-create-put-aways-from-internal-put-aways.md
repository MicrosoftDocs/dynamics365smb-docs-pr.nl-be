---
title: Een opslaginstructie maken van de interne opslaginstructie | Microsoft Docs
description: Artikelen die worden opgeslagen om te worden gepickt voor een productieorder of verzending, maken deel uit van de beschikbare voorraad in het magazijn.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 17955c3ea1294811cd7b9ac6f726d26b0de2755c
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

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
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Interne mag.-pick** in en kies vervolgens de gerelateerde koppeling.  
2.  Vul het veld **Nr.** en **Naar opslaglocatie** in op het sneltabblad **Algemeen**. Het veld **Naar opslaglocatie** geeft aan uit welke opslaglocatie de artikelen moeten worden gehaald. Voor productiedoeleinden is deze locatie de inkomende productieopslaglocatie of open-shopopslaglocatie. In alle andere gevallen moet u een opslaglocatie kiezen van een soort die niet wordt gebruikt voor pickactiviteiten, zoals een opslaglocatie voor staging, verzending of speciale doeleinden.  
3.  Selecteer een artikel in het veld **Artikelnr.** en geef het gewenste pickaantal op.  
4. Kies de actie **Pick maken**. De pickinstructie voor het magazijn kan nu worden uitgevoerd door een magazijnmedewerker.  

## <a name="to-create-an-internal-put-away"></a>Een interne opslag maken  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Interne mag.-opslag** in en kies vervolgens de gerelateerde koppeling.  
2.  Vul het veld **Nr.** en **Van opslaglocatie** in op het sneltabblad **Algemeen**. Het veld **Naar opslaglocatie** geeft aan naar welke opslaglocatie het artikel wordt geretourneerd (mogelijk vanuit de productieafdeling).  
3.  Voer de artikelnummers en aantallen in op de regels.  
4.  Kies de actie **Opslag maken**. De opslaginstructie voor het magazijn kan nu worden uitgevoerd door een magazijnmedewerker.  

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

