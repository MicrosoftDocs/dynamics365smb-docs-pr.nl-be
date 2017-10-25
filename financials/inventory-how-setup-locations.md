---
title: "Een vestigingskaart instellen en transferroutes definiëren| Microsoft Docs"
description: U maakt een vestigingskaart voor elke plaats waar u voorraadartikelen opslaat, bijvoorbeeld een magazijn of een distributiecentrum, en u stelt routes in om artikelen tussen vestigingen over te brengen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/02/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7d82b1c63bb1da367736f8dd044640b583493af8
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-locations"></a>Procedure: vestigingen instellen
Als u artikelen op meer dan één plaats of magazijn koopt, opslaat of verkoopt, moet u elke vestiging instellen met een vestigingskaart en transferroutes definiëren.

U kunt vervolgens documentregels voor een bepaalde vestiging maken, beschikbaarheid per locatie weergeven en voorraad tussen locaties overbrengen. Zie [Voorraad beheren](inventory-manage-inventory.md) voor meer informatie.

> [!NOTE]  
>   Deze functionaliteit vereist dat uw ervaring is ingesteld op **Suite**. Zie voor meer informatie [Uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-ervaring aanpassen](ui-experiences.md).

## <a name="to-create-a-location-card"></a>Een vestigingskaart maken
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Vestigingen** in en klik vervolgens op de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul indien nodig de velden in het venster **Vestigingskaart** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Herhaal stap 2 en 3 voor elke locatie waar u voorraad wilt houden.

> [!NOTE]  
> Veel velden op de vestigingskaart verwijzen naar de verwerking van artikelen in inkomende en uitgaande magazijnprocessen. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md). 

## <a name="to-create-a-transfer-route"></a>Een transferroute maken
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Transferroutes** in en klik op de gerelateerde koppeling.
2. U kunt ook vanuit elk **Vestiging**-venster de actie **Transferroutes** kiezen.
3. Kies de actie **Nieuw**.
4. Vul indien nodig de velden in het venster **Vestigingskaart** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

U kunt nu voorraadartikelen tussen twee vestigingen overbrengen. Zie voor meer informatie [Procedure: Voorraad overbrengen tussen vestigingen](inventory-how-transfer-between-locations.md).    

## <a name="see-also"></a>Zie ook
[Voorraad beheren](inventory-manage-inventory.md)  
[Procedure: Voorraad overbrengen tussen vestigingen](inventory-how-transfer-between-locations.md)    
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-ervaring aanpassen](ui-experiences.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)

