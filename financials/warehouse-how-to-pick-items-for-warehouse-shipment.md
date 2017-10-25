---
title: Artikelen picken voor magazijnverzending | Microsoft Docs
description: Als voor de locatie zowel magazijnpickverwerking als magazijnverzendingsverwerking is vereist, gebruikt u magazijnpickdocumenten om de pickinformatie te beheren voordat u de magazijnverzending boekt.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: e4568214469e80dce7ea91ff7574d1be8ca9ac7a
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-pick-items-for-warehouse-shipment"></a>Procedure: picken van artikelen voor magazijnverzending
Als voor de locatie zowel magazijnpickverwerking als magazijnverzendingsverwerking vereist is, gebruikt u magazijnpickdocumenten om de pickinformatie te beheren voordat u de magazijnverzending boekt.  

Een magazijn-pickdocument kan niet van het begin af gemaakt worden, omdat een pick-activiteit altijd onderdeel is van een werkstroom, zowel bij een pull- als bij een push-scenario.  

U kunt magazijn-pickdocumenten op een pull-manier maken door het openen van een leeg document voor magazijnverzending, detecteren van brondocumenten die zijn vrijgegeven voor verzending en vervolgens maken van magazijnpickregels voor deze verzendingen. U kunt de functies **Brondocumenten ophalen** of **Filter gebruiken om brondocumenten op te halen** voor het detecteren van brondocumenten die gereed zijn voor verzending.

U kunt ook het venster **Werkblad Pick** gebruiken om pickregels in de batchmodus te halen en te maken. Zie [Procedure: picks plannen in het voorstel](warehouse-how-to-plan-picks-in-worksheets.md) voor meer informatie.  

U kunt ook magazijn-pickdocumenten op push-wijze vanuit het venster **Magazijnverzending** maken door **Pick maken** te selecteren.  

> [!NOTE]  
>  Het picken voor magazijnverzending van artikelen die worden samengesteld voor de verkooporder die wordt verzonden volgt dezelfde stappen als gewone magazijnpicks voor verzending, zoals beschreven in dit onderwerp. Het aantal pickregels per te verzenden aantal is mogelijk echter veel-op-één omdat u de componenten pickt, niet het assemblageartikel.  
>   
>  De magazijnpickregels zijn gemaakt voor de waarde in het veld **Resterend aantal** op de regels van de assemblage die is gekoppeld aan de verkooporderregel die wordt verzonden. Dit zorgt ervoor dat alle onderdelen in één actie worden gepickt.  
>   
>  Zie de sectie Op-order-assembleren-artikelen in magazijnverzendingen afhandelen voor meer informatie.  
>   
>  Zie [Procedure: Picken voor productie of assemblage](warehouse-how-to-pick-for-production.md) voor informatie over het picken van onderdelen voor assemblageorders in het algemeen, met inbegrip van situaties waar de assemblage niet voor een verkoopverzending is.  

## <a name="to-pick-items-for-warehouse-shipment"></a>Picken van artikelen voor magazijnverzending  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Magazijnpicks** in en klik vervolgens op de gerelateerde koppeling.  

    Als u een bepaalde pick wilt bewerken, selecteert u het pickformulier of het overzicht. U kunt het overzicht ook filteren op picks die speciaal aan u zijn toegewezen. De pickkaart openen.  
2.  Indien het veld **Toegewezen gebruikers-ID** leeg is, voert u uw ID in om uzelf te identificeren indien nodig.  
3.  Uitvoeren van het werkelijke picken van artikelen.  

    Indien het magazijn opslaglocaties gebruikt, worden de standaard opslaglocaties voor de artikelen voorgesteld om de artikelen uit te halen. De instructies worden op twee afzonderlijke regels weergegeven, minimaal één voor elk soort actie, Nemen en Plaatsen.  

    Indien voor het magazijn gestuurde opslag en pick is ingesteld, wordt de opslaglocatievolgorde gebruikt voor het berekenen van de beste opslaglocaties waaruit gepickt kan worden en deze opslaglocaties worden vervolgens voorgesteld op de pickregels. De instructies worden op twee afzonderlijke regels weergegeven, minimaal één voor elk soort actie, Nemen en Plaatsen.  

4.  Als u de pick hebt uitgevoerd en de artikelen op de verzendlocatie hebt geplaatst, kiest u de actie **Pick registreren**.  

De persoon die verantwoordelijk is voor verzending kan nu de artikelen naar de afdeling voor verzending overbrengen en de verzending boeken, inclusief het verwante brondocument, in het venster **Mag. -verzending**. Zie [Procedure: Artikelen verzenden](warehouse-how-ship-items.md) voor meer informatie.   

Naast het picken voor brondocumenten zoals beschreven in dit onderwerp kunt u artikelen tussen opslaglocaties nemen en plaatsen zonder te verwijzen naar de brondocumenten. Zie [Procedure: Picken en opslaan zonder een brondocument](warehouse-how-to-create-put-aways-from-internal-put-aways.md).  

## <a name="handling-assemble-to-order-items-in-warehouse-shipments"></a>Op-order-assembleren-artikelen in magazijnverzendingen afhandelen
In scenario's voor het assembleren op order, wordt het veld **Te verzenden aantal** op magazijnverzendingsregels gebruikt om vast te leggen hoeveel eenheden worden geassembleerd. Het opgegeven aantal wordt vervolgens geboekt als assemblageuitvoer wanneer de magazijnverzending wordt geboekt.

Voor andere magazijnverzendingsregels is de waarde in het veld **Te verzenden aantal** nul vanaf het begin.

Wanneer werknemers die verantwoordelijk zijn voor het assembleren klaar zijn met het assembleren van onderdelen of de volledige hoeveelheid voor op order assembleren, registreren ze dit in het veld **Te verzenden aantal** op de magazijnverzendingsregel en kiezen ze de actie **Verzending boeken**. Het resultaat is dat de bijbehorende assemblageuitvoer wordt geboekt, inclusief het materiaalverbruik. Een verkoopverzending voor de hoeveelheid wordt geboekt voor de verkooporder.

Op de assemblageorder kunt u **Magazijnverzendregel op order assembleren** om toegang te krijgen tot de magazijnverzendregel. Dit is handig voor werknemers die gewoonlijk niet het venster **Magazijnverzending** gebruiken.

Na het boeken van de magazijnverzending, worden verschillende velden op de orderregel bijgewerkt om de voortgang in het magazijn weer te geven. De volgende velden worden ook bijgewerkt om weer te geven hoeveel op-order-assembleren-aantallen nog moeten worden geassembleerd en verzonden:

- **AoO-mag. uitstaand aantal**
- **AoO-mag. uitst. aant. (basis)**

> [!NOTE]
> In combinatiescenario's waarbij een deel van de hoeveelheid eerst moet worden geassembleerd en een ander deel uit voorraad moet worden verzonden, worden twee magazijnverzendregels gemaakt. Eén voor het op-order-assembleren-aantal, en één voor het voorraadaantal.

> In dat geval wordt het op-order-assembleren-aantal verwerkt zoals beschreven in dit onderwerp, en het voorraadaantal wordt verwerkt als een gewone magazijnverzendregel. Zie [Op voorraad assembleren of Op order assembleren begrijpen](assembly-assemble-to-order-or-assemble-to-stock.md) voor meer informatie over combinatiescenario's.

## <a name="see-also"></a>Zie ook  
[Magazijnbeheer](warehouse-manage-warehouse.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

