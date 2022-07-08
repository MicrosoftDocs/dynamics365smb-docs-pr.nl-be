---
title: Een vestigingskaart instellen en transferroutes definiëren (bevat video)
description: Als u artikelen op meer dan één plaats of magazijn koopt, opslaat of verkoopt, moet u elke vestiging instellen met een vestigingskaart en transferroutes definiëren.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.search.forms: 5703, 15
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 870effafbd38cdee0733097fa6fb0c0340fa77b8
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9077279"
---
# <a name="set-up-locations"></a>Vestigingen instellen

Vestigingen zijn plaatsen zoals magazijnen waar u artikelen koopt, opslaat of verkoopt. [!INCLUDE [prod_short](includes/prod_short.md)] gebruikt vestigingen om de voorraad bij te houden in zowel eenvoudige als complexere magazijnprocessen.

U kunt vervolgens documentregels voor een bepaalde vestiging maken, beschikbaarheid per locatie weergeven en voorraad tussen locaties overbrengen. Zie [Voorraad beheren](inventory-manage-inventory.md) voor meer informatie.
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Vestigingskaarten

U geeft informatie over een vestiging, zoals een magazijn of een distributiecentrum, op de pagina **Vestiging** op. U wijst aan elke vestiging een naam toe en een code die de vestiging vertegenwoordigt. U kunt de vestigingscode in andere delen van het programma invoeren om transacties voor een bepaalde vestiging vast te leggen.  

U kunt informatie invoeren over opslaglocaties en magazijnbeleid voor elke vestiging. Op basis van het geselecteerde magazijnbeleid gebruikt u de opties op het sneltabblad **Opslaglocaties** om de opslaglocaties te definiëren die als standaardopslaglocaties worden gebruikt wanneer u transacties uitvoert. Als u gestuurde opslag en pick gebruikt, gebruikt u de meeste opties op het sneltabblad **Opslaglocatiebeleid** om te definiëren hoe u de verschillende magazijnfuncties wilt gebruiken.  

Sommige optievelden zijn afhankelijk van instellingen op de pagina **Vestiging** om niet-ondersteunde combinaties te beperken.  

Kies de actie **Zones** of **Opslaglocaties** voor informatie over zones en opslaglocaties die zijn gedefinieerd voor de vestiging.

### <a name="to-set-up-a-location"></a>Een vestiging instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Locaties** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul indien nodig de velden op de pagina **Vestiging** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Herhaal stap 2 en 3 voor elke locatie waar u voorraad wilt houden.

> [!NOTE]  
> Veel velden op de pagina Vestigingskaart verwijzen naar de verwerking van artikelen in inkomende en uitgaande magazijnprocessen. Deze velden zijn niet relevant voor bedrijven die de meer complexe magazijnfunctionaliteit niet nodig hebben. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).

U kunt de configuratie van een vestiging later wijzigen, maar u kunt de instellingen van vestigingen met artikelposten niet bewerken.  

Als u meerdere vestigingen heeft, kunt u vervolgens transferroutes tussen vestigingen definiëren. Zie voor meer informatie [Een transferroute maken ](inventory-how-setup-locations.md#to-create-a-transfer-route). 

### <a name="to-create-a-transfer-route"></a>Een transferroute maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Transferroutes** in en kies vervolgens de gerelateerde koppeling
2. U kunt ook vanuit elke **Vestiging**-pagina de actie **Transferroutes** kiezen.
3. Kies de actie **Nieuw**.
4. Vul indien nodig de velden op de pagina **Vestiging** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

U kunt nu voorraadartikelen tussen twee vestigingen overbrengen. Zie voor meer informatie [Voorraad overbrengen tussen vestigingen](inventory-how-transfer-between-locations.md).    

## <a name="bins"></a>Opslaglocaties

Opslaglocaties vertegenwoordigen de standaard magazijnstructuur en worden gebruikt voor het doen van voorstellen over de plaatsing van artikelen. Wanneer u uw opslaglocaties hebt gemaakt, kunt u de inhoud ervan definiëren of kunnen ze functioneren als vrije opslaglocaties zonder opgegeven inhoud. Opslaglocaties worden voornamelijk gebruikt in basis- en geavanceerde magazijnactiviteiten. Als u voorraad op een eenvoudigere manier beheert, heeft u waarschijnlijk geen opslaglocaties nodig.

Om de opslaglocatiefunctionaliteit op een vestiging te gebruiken, activeert u eerst de functionaliteit op de pagina **Vestiging** door het veld **Opslaglocaties verplicht** op het sneltabblad **Magazijn** te selecteren. U ontwerpt vervolgens de artikelstroom op de locatie door de opslaglocatiecodes op te geven in de instellingsvelden voor de verschillende stromen.

> [!NOTE]
> Voordat u opslaglocatiecodes voor een vestiging kunt opgeven, moet u opslaglocatiecodes maken. Zie [Opslaglocaties maken](warehouse-how-to-create-individual-bins.md) en [Opslaglocatiesoorten instellen](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Zones

Als u uw opslaglocaties onder zones wilt structureren, kunt u dat doen op de pagina **Zones**.

[!INCLUDE [prod_short](includes/prod_short.md)] kopieert de velden die u voor een bepaalde zone instelt, naar de opslaglocaties erin. Op deze manier kunt u een zone toewijzen aan een opslaglocatie of een opslaglocatiesjabloon (filter voor het maken van opslaglocaties), worden diverse andere velden automatisch ingevuld.

U kunt echter ook slechts één zone instellen en uw magazijn indelen op basis van alleen de opslaglocaties. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).  

## <a name="default-dimensions-for-locations"></a>Standaardafmetingen voor locaties

U stelt standaardafmetingen in voor een locatie op de pagina **Locatiekaart** door **Locatie** te kiezen en vervolgens **Dimensies**. De standaarddimensies van de locatie worden gekopieerd naar journalen en documenten wanneer u de locatie op een regel opgeeft, maar u kunt de dimensie op de regel indien nodig verwijderen of wijzigen. U kunt eisen dat mensen dimensies opgeven voor specifieke locaties voordat ze een item kunnen boeken. U kunt ook locatiedimensiewaarden opnemen in **Prioriteiten voor standaarddimensie** en **Dimensiecombinaties** voor combinaties van prioriteits- en dimensieregels.

## <a name="see-related-training-at-microsoft-learn"></a>Zie gerelateerde training op [Microsoft Learn](/learn/modules/trade-set-up-dynamics-365-business-central/)

## <a name="see-also"></a>Zie ook

[Voorraad beheren](inventory-manage-inventory.md)  
[Voorraad overbrengen tussen vestigingen](inventory-how-transfer-between-locations.md)  
[Opslaglocaties maken](warehouse-how-to-create-individual-bins.md)  
[Opslaglocatiesoorten instellen](warehouse-how-to-set-up-bin-types.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]