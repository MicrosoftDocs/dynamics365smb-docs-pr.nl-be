---
title: De status van een synchronisatie weergeven | Microsoft Docs
description: Leer hoe u de status van een afzonderlijke synchronisatietaak weergeeft.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 11e29674c2d12031fdf4e7f66e767be4fcc74795
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620896"
---
# <a name="view-the-status-of-a-synchronization"></a>De status van een synchronisatie weergeven
U kunt de status van de afzonderlijke synchronisatietaken weergeven die voor [!INCLUDE[crm_md](includes/crm_md.md)]-integratie zijn uitgevoerd. Hieronder vallen synchronisatietaken die zijn uitgevoerd vanuit de verwerkingswachtrij en handmatige synchronisatietaken die zijn uitgevoerd op records vanuit de [!INCLUDE[d365fin](includes/d365fin_md.md)]-client. Dit is handig bij het oplossen van synchronisatieproblemen omdat u toegang hebt tot details van specifieke fouten die optreden.

### <a name="to-view-synchronization-issues-for-coupled-records"></a>Synchronisatieproblemen weergeven voor gekoppelde records
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Synchronisatiefouten met gekoppelde gegevens** in en kies vervolgens de gerelateerde koppeling.
2. De pagina **Synchronisatiefouten met gekoppelde gegevens** bevat problemen die zijn opgetreden toen u gekoppelde records synchroniseerde. U kunt records filteren en sorteren en acties zoals **Herstellen** of **Records verwijderen** uitvoeren om problemen een voor een op te lossen.

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a>Het synchronisatielogboek weergeven voor een specifieke (handmatig gesynchroniseerde) record
1. Open bijvoorbeeld een klant-, artikel- of andere record die gegevens synchroniseert tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en Sales.
2. Kies de actie **Synchronisatielogbestand** om het synchronisatielogbestand voor een geselecteerde record weer te geven. Bijvoorbeeld een specifieke klant die u handmatig hebt gesynchroniseerd.

## <a name="see-also"></a>Zie ook  
[Dynamics 365 for Sales-integratie instellen in Business Central](admin-setting-up-integration-with-dynamics-sales.md)  
[Dynamics 365 for Sales gebruiken vanuit Business Central](marketing-integrate-dynamicscrm.md)
