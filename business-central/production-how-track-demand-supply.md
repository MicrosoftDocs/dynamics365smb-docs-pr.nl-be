---
title: Relatie tussen vraag en aanbod bijhouden | Microsoft Docs
description: Vanuit elk document voor aanbod of vraag in het zogenaamde ordernetwerk kunt u de ordervraag (getraceerd aantal), prognose , raamverkooporder of planningsparameter (niet-getraceerd aantal) traceren die een planningregel heeft doen stijgen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: de71e4c305b775df8c10306ecc474bc6944d0787
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816852"
---
# <a name="track-relations-between-demand-and-supply"></a>Relaties tussen vraag en aanbod bijhouden
Vanuit elk document voor aanbod of vraag in het zogenaamde ordernetwerk kunt u de ordervraag (getraceerd aantal), prognose , raamverkooporder of planningsparameter (niet-getraceerd aantal) traceren die een planningregel heeft doen stijgen.

De planningsvoorstellen bevatten ook ondersteunende planninginformatie over entiteiten die geen orders zijn om de planner te helpen een optimaal leveringsplan op te stellen. Zie [Niet-getraceerde planningselementen](production-how-track-demand-supply.md#untracked-planning-elements) voor meer informatie.

## <a name="to-track-linked-items"></a>Gekoppelde artikelen traceren
Met behulp van ordertracering kunt u nagaan hoe verkooporders, productieorders en inkooporders aan de productieorder zijn gekoppeld via de plannings- en reserveringssystemen.

Hieronder wordt beschreven hoe u gekoppelde artikelen in een vast geplande productieorder traceert. De stappen voor alle andere soorten orders en vanuit planningsvoorstelregels zijn vergelijkbaar.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vast geplande productieorder** in en kies vervolgens de gerelateerde koppeling.
2. Open de betreffende vast geplande productieorder in de lijst.
3. Op het sneltabblad **Regels** kiest u de actie **Functies** en vervolgens **Ordertracering**.

Op de regels in het venster **Ordertracering** worden de documenten weergegeven die zijn gekoppeld aan de huidige productieorderregel.

## <a name="untracked-planning-elements"></a>Niet-getraceerde planningselementen
De pagina **Niet-getraceerde planningselementen** wordt geopend wanneer u het veld **Niet-getraceerd aantal** op de pagina **Orderplanning** kiest. Dit dient twee doelen:

1. De tabel bevat informatie over ongetraceerde hoeveelheden die worden weergegeven wanneer de gebruiker opzoekt op de pagina Ordertracering om de ongetraceerde aantallen weer te geven.
2. De tabel bevat waarschuwingsberichten die worden weergegeven wanneer de gebruiker op het pictogram **Waarschuwing** op de pagina **Planningsvoorstel** klikt.

De pagina bevat posten die een verklaring kunnen geven voor niet-getraceerde overschotaantallen in het ordertraceringsnetwerk. Deze posten worden gegenereerd tijdens het planningsproces en verklaren waar het niet-getraceerde overschotaantal in de ordertraceringsregels vandaan kwam. Dit niet-getraceerde overschot kan afkomstig zijn uit:

- Productieprognose
- Raamcontractenorders
- Veiligheidsvoorraad
- Bestelpunt
- Maximale voorraad
- Bestelaantal
- Max. bestelaantal
- Min. bestelaantal
- Vaste lotgrootte
- Demping (% van lotgrootte)

## <a name="see-also"></a>Zie ook  
[Gepland](production-planning.md)   
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)    
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Ontwerpdetails: Reservering, tracering en planningsboodschappen](design-details-reservation-order-tracking-and-action-messaging.md)  
[Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md)   
[Aanbevolen procedures instellen: voorraadplanning](setup-best-practices-supply-planning.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
