---
title: Een vestigingskaart instellen en transferroutes definiëren| Microsoft Docs
description: U maakt een vestigingskaart voor elke plaats waar u voorraadartikelen opslaat, bijvoorbeeld een magazijn of een distributiecentrum, en u stelt routes in om artikelen tussen vestigingen over te brengen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 04/01/2019
ms.author: SorenGP
ms.openlocfilehash: d94f1bb2fe45263f013119954622b995e902b30f
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1244302"
---
# <a name="set-up-locations"></a>Vestigingen instellen
Als u artikelen op meer dan één plaats of magazijn koopt, opslaat of verkoopt, moet u elke vestiging instellen met een vestigingskaart en transferroutes definiëren.

U kunt vervolgens documentregels voor een bepaalde vestiging maken, beschikbaarheid per locatie weergeven en voorraad tussen locaties overbrengen. Zie [Voorraad beheren](inventory-manage-inventory.md) voor meer informatie.

## <a name="to-create-a-location-card"></a>Een vestigingskaart maken
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Locaties** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul indien nodig de velden op de pagina **Vestiging** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Herhaal stap 2 en 3 voor elke locatie waar u voorraad wilt houden.

> [!NOTE]  
> Veel velden op de vestigingskaart verwijzen naar de verwerking van artikelen in inkomende en uitgaande magazijnprocessen. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).

## <a name="to-create-a-transfer-route"></a>Een transferroute maken
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Transferroutes** in en kies vervolgens de gerelateerde koppeling.
2. U kunt ook vanuit elke **Vestiging**-pagina de actie **Transferroutes** kiezen.
3. Kies de actie **Nieuw**.
4. Vul indien nodig de velden op de pagina **Vestiging** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

U kunt nu voorraadartikelen tussen twee vestigingen overbrengen. Zie voor meer informatie [Voorraad overbrengen tussen vestigingen](inventory-how-transfer-between-locations.md).    

## <a name="see-also"></a>Zie ook
[Voorraad beheren](inventory-manage-inventory.md)  
[Voorraad overbrengen tussen vestigingen](inventory-how-transfer-between-locations.md)    
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)
