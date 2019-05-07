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
ms.openlocfilehash: d55d8d5ab916cee6600deaf891702a625d76d7ee
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "940565"
---
# <a name="view-the-status-of-a-synchronization"></a>De status van een synchronisatie weergeven
U kunt de status van de afzonderlijke synchronisatietaken weergeven die voor [!INCLUDE[crm_md](includes/crm_md.md)]-integratie zijn uitgevoerd. Hieronder vallen synchronisatietaken die zijn uitgevoerd vanuit de verwerkingswachtrij en handmatige synchronisatietaken die zijn uitgevoerd op records vanuit de [!INCLUDE[d365fin](includes/d365fin_md.md)]-client. Dit is handig bij het oplossen van synchronisatieproblemen omdat u toegang hebt tot details van specifieke fouten die optreden.

### <a name="to-view-all-synchronization-issues"></a>Alle synchronisatieproblemen weergeven
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Synchronisatiefouten met gekoppelde gegevens** in en kies vervolgens de gerelateerde koppeling.
2. Op de pagina **Synchronisatiefouten met gekoppelde gegevens** kunt u alle problemen weergeven die zijn opgetreden tijdens de synchronisatie van gegevens tussen [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[d365fin](includes/d365fin_md.md)], records op de pagina filteren en sorteren op tabel of foutbericht, en acties ondernemen zoals **Opnieuw** of **Koppeling verwijderen** om problemen een voor een of massaal op te lossen.

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a>Het synchronisatielogboek weergeven voor een specifieke (handmatig gesynchroniseerde) record
1. Open bijvoorbeeld de klant-, artikel- of andere record die gegevens synchroniseert tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en Sales
2. Kies de actie **Synchronisatielogbestand** om het synchronisatielogbestand voor de geselecteerde record weer te geven, bijvoorbeeld een specifieke klant die u handmatig hebt gesynchroniseerd.

## <a name="see-also"></a>Zie ook  
[Dynamics 365 for Sales-integratie instellen in Business Central](admin-setting-up-integration-with-dynamics-sales.md)  
[Dynamics 365 for Sales gebruiken vanuit Business Central](marketing-integrate-dynamicscrm.md)
