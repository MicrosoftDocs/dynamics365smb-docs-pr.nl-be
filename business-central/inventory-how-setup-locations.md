---
title: Een vestigingskaart instellen en transferroutes definiëren
description: Als u artikelen op meer dan één plaats of magazijn koopt, opslaat of verkoopt, moet u elke vestiging instellen met een vestigingskaart en transferroutes definiëren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: d22bbea911bed7e1ea3c756e0861111a26b5df0a
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435584"
---
# <a name="set-up-locations"></a>Vestigingen instellen

Als u artikelen op meer dan één plaats of magazijn koopt, opslaat of verkoopt, moet u elke vestiging instellen met een vestigingskaart en transferroutes definiëren. [!INCLUDE [prod_short](includes/prod_short.md)] gebruikt vestigingen om de voorraad bij te houden in zowel eenvoudigere gevallen als de meer complexe magazijnprocessen.

U kunt vervolgens documentregels voor een bepaalde vestiging maken, beschikbaarheid per locatie weergeven en voorraad tussen locaties overbrengen. Zie [Voorraad beheren](inventory-manage-inventory.md) voor meer informatie.
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Vestigingskaarten

Op de vestigingskaart staat informatie over een vestiging, zoals een magazijn of distributiecentrum. U wijst aan elke vestiging een naam toe en een code die de vestiging vertegenwoordigt. U kunt de vestigingscode in andere delen van het programma invoeren om transacties voor een bepaalde vestiging vast te leggen.  

U kunt informatie invoeren over opslaglocaties en magazijnbeleid voor elke vestiging. Op basis van het geselecteerde magazijnbeleid gebruikt u de opties op het sneltabblad **Opslaglocaties** om de opslaglocaties te definiëren die als standaardopslaglocaties worden gebruikt wanneer u transacties uitvoert. Als u gestuurde opslag en pick gebruikt, gebruikt u de meeste opties op het sneltabblad **Opslaglocatiebeleid** om te definiëren hoe u de verschillende magazijnfuncties wilt gebruiken.  

Sommige optievelden zijn niet beschikbaar en uitgeschakeld door andere instellingen op de pagina **Vestigingskaart** om niet-ondersteunde combinaties te beperken.  

Kies de actie **Zones** of **Opslaglocaties** voor informatie over zones en opslaglocaties die zijn gedefinieerd voor de vestiging.

### <a name="to-create-a-location-card"></a>Een vestigingskaart maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Locaties** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul indien nodig de velden op de pagina **Vestiging** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Herhaal stap 2 en 3 voor elke locatie waar u voorraad wilt houden.

> [!NOTE]  
> Veel velden op de vestigingskaart verwijzen naar de verwerking van artikelen in inkomende en uitgaande magazijnprocessen. De velden zijn niet relevant voor bedrijven die de meer complexe magazijnfunctionaliteit niet nodig hebben. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).

U kunt de configuratie van een vestiging later wijzigen, maar u kunt de instellingen van vestigingen met artikelposten niet bewerken.  

Als u meerdere vestigingen heeft, kunt u vervolgens transferroutes tussen vestigingen definiëren.  

### <a name="to-create-a-transfer-route"></a>Een transferroute maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Transferroutes** in en kies vervolgens de gerelateerde koppeling
2. U kunt ook vanuit elke **Vestiging**-pagina de actie **Transferroutes** kiezen.
3. Kies de actie **Nieuw**.
4. Vul indien nodig de velden op de pagina **Vestiging** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

U kunt nu voorraadartikelen tussen twee vestigingen overbrengen. Zie voor meer informatie [Voorraad overbrengen tussen vestigingen](inventory-how-transfer-between-locations.md).    

## <a name="bins"></a>Opslaglocaties

Opslaglocaties vertegenwoordigen de standaard magazijnstructuur en worden gebruikt voor het doen van voorstellen over de plaatsing van artikelen. Wanneer u uw opslaglocaties hebt gemaakt, kunt u de inhoud die u in de afzonderlijke opslaglocaties wilt plaatsen precies definiëren. De opslaglocatie kan echter ook functioneren als een vrije opslaglocatie zonder opgegeven inhoud. Opslaglocaties worden voornamelijk gebruikt in basis- en geavanceerde magazijnactiviteiten. Als u voorraad op een eenvoudigere manier beheert, heeft u waarschijnlijk geen opslaglocaties nodig.

Om de opslaglocatiefunctionaliteit op een vestiging te gebruiken, activeert u eerst de functionaliteit op de **vestigingskaart** door het veld **Opslaglocatie verplicht** op het sneltabblad **Magazijn** te selecteren. U ontwerpt vervolgens de artikelstroom op de locatie door de opslaglocatiecodes op te geven in de instellingsvelden voor de verschillende stromen.

> [!NOTE]
> Voordat u opslaglocatiecodes op de vestigingskaart kunt opgeven, moeten de opslaglocatiecodes worden gemaakt.

Zie [Opslaglocaties maken](warehouse-how-to-create-individual-bins.md) en [Opslaglocatiesoorten instellen](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Zones

Als u uw opslaglocaties onder zones wilt structureren, kunt u dat doen op de pagina **Zones**.

[!INCLUDE [prod_short](includes/prod_short.md)] kopieert de velden die u voor een bepaalde zone instelt, naar de opslaglocaties erin. Op deze manier kunt u een zone toewijzen aan een opslaglocatie of een opslaglocatiesjabloon (filter voor het maken van opslaglocaties), worden diverse andere velden automatisch ingevuld.

U kunt echter ook slechts één zone instellen en uw magazijn indelen op basis van alleen de opslaglocaties. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).  

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