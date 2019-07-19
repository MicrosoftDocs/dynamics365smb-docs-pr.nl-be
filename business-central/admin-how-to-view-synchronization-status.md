---
title: De status van synchronisatietaken weergeven | Microsoft Docs
description: Leer hoe u de status kunt bekijken na het synchroniseren van gekoppelde records.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 06/13/2019
ms.author: bholtorf
ms.openlocfilehash: 8d7421d5fee1a6498c204730f873c3746aafc637
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726756"
---
# <a name="view-the-status-of-synchronization-jobs"></a>De status van synchronisatietaken weergeven
Gebruik de pagina **Synchronisatiefouten met gekoppelde gegevens** om de status weer te geven van synchronisatietaken die zijn uitgevoerd voor gekoppelde records in een [!INCLUDE[crm_md](includes/crm_md.md)]-integratie. Hieronder vallen taken die zijn uitgevoerd vanuit de verwerkingswachtrij en handmatige synchronisatietaken die zijn uitgevoerd op records vanuit de [!INCLUDE[d365fin](includes/d365fin_md.md)]-client. Het bekijken van hun status is bijvoorbeeld handig bij het oplossen van problemen omdat het u toegang geeft tot details over fouten met betrekking tot gekoppelde records. Meestal worden dit soort fouten veroorzaakt door gebruikersacties, bijvoorbeeld wanneer:  

* Twee mensen hebben in beide zakelijke apps een wijziging aangebracht in dezelfde record.
* Iemand heeft een record verwijderd in een van de apps, maar niet in beide.

> [!Note]
> De pagina **Synchronisatiefouten met gekoppelde gegevens** toont informatie over taken gerelateerd aan gekoppelde records. Als u alle fouten oplost maar records nog steeds niet synchroniseren, heeft dit mogelijk te maken met een instelling voor de integratie. Doorgaans moet uw beheerder dit soort fouten oplossen.   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098171]

## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Synchronisatiefouten voor gekoppelde records weergeven en oplossen
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Synchronisatiefouten met gekoppelde gegevens** in en kies vervolgens de gerelateerde koppeling.
2. De pagina **Synchronisatiefouten met gekoppelde gegevens** bevat problemen die zijn opgetreden toen u gekoppelde records synchroniseerde. De volgende tabel bevat acties die u kunt gebruiken om problemen één voor één op te lossen:

|Actie|Omschrijving|
|----|----|
|**Koppeling verwijderen**|Ontkoppelt de records en deze zullen niet langer synchroniseren. Om het synchroniseren van de records te hervatten, moet u ze opnieuw koppelen.|
|**Opnieuw**|Voor elke record waarin een fout wordt gevonden, wordt de synchronisatie overgeslagen, tenzij u het probleem handmatig verhelpt. Met Opnieuw wordt de record opgenomen in de volgende synchronisatie.|
|**Synchroniseren**|De app probeert een conflict op te lossen waarbij een record is gewijzigd in beide zakelijke apps. U kunt de versie van de record kiezen die u in beide apps wilt gebruiken.|
|**Records herstellen** en **Records verwijderen**|Deze zijn handig wanneer een record in een van de apps is verwijderd. Records verwijderen verwijdert de record in de app waar deze nog steeds bestaat. Met Herstellen wordt de record opnieuw gemaakt in de app waarin deze is verwijderd.|

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a>Het synchronisatielogboek weergeven voor een specifieke (handmatig gesynchroniseerde) record
1. Open bijvoorbeeld een klant-, artikel- of andere record die gegevens synchroniseert tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)].
2. Kies de actie **Synchronisatielogbestand** om het synchronisatielogbestand voor een geselecteerde record weer te geven. Bijvoorbeeld een specifieke klant die u handmatig hebt gesynchroniseerd.

## <a name="see-also"></a>Zie ook  
[Gebruikersaccounts instellen voor integratie met Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Dynamics 365 for Sales gebruiken vanuit Business Central](marketing-integrate-dynamicscrm.md)
