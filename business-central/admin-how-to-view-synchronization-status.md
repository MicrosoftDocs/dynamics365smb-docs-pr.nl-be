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
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: c185ab8fecc8f8d70dad7696a5fb5f67207717aa
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924615"
---
# <a name="view-the-status-of-synchronization-jobs"></a>De status van synchronisatietaken weergeven
Gebruik de pagina **Synchronisatiefouten met gekoppelde gegevens** om de status weer te geven van synchronisatietaken die zijn uitgevoerd voor gekoppelde records in een Common Data Service- of een [!INCLUDE[crm_md](includes/crm_md.md)]-integratie. Hieronder vallen taken die zijn uitgevoerd vanuit de verwerkingswachtrij en handmatige synchronisatietaken die zijn uitgevoerd op records vanuit de [!INCLUDE[d365fin](includes/d365fin_md.md)]-client. Het bekijken van hun status is bijvoorbeeld handig bij het oplossen van problemen omdat het u toegang geeft tot details over fouten met betrekking tot gekoppelde records. Meestal worden dit soort fouten veroorzaakt door gebruikersacties, bijvoorbeeld wanneer:  

* Twee mensen hebben in beide zakelijke apps een wijziging aangebracht in dezelfde record.
* Iemand heeft een record verwijderd in een van de apps, maar niet in beide.

> [!Note]
> De pagina **Synchronisatiefouten met gekoppelde gegevens** toont informatie over taken gerelateerd aan gekoppelde records. Als u alle fouten oplost maar records nog steeds niet synchroniseren, heeft dit mogelijk te maken met een instelling voor de integratie. Doorgaans moet uw beheerder dit soort fouten oplossen.   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098171]

## <a name="to-view-and-resolve-synchronization-errors-for-coupled-records"></a>Synchronisatiefouten voor gekoppelde records weergeven en oplossen
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Synchronisatiefouten met gekoppelde gegevens** in en kies de desbetreffende koppeling.
2. De pagina **Synchronisatiefouten met gekoppelde gegevens** bevat problemen die zijn opgetreden toen u gekoppelde records synchroniseerde. De volgende tabel bevat acties die u kunt gebruiken om problemen één voor één op te lossen:

|Actie|Omschrijving|
|----|----|
|**Koppeling verwijderen**|Ontkoppelt de records en deze zullen niet langer synchroniseren. Om de synchronisatie te hervatten moet u ze opnieuw koppelen. |
|**Opnieuw** en **Alles opnieuw proberen**|Voor elke record waarin een fout wordt gevonden, wordt de synchronisatie overgeslagen, tenzij u het probleem verhelpt. Met Opnieuw zal de geselecteerde record worden opgenomen in de volgende synchronisatie en met **Alles opnieuw proberen** worden alle records opgenomen.|
|**Synchroniseren**|De app probeert een conflict op te lossen waarbij een record is gewijzigd in beide zakelijke apps. U kunt de versie van de record kiezen die u wilt gebruiken.|
|**Records herstellen** en **Records verwijderen**|Deze zijn handig wanneer een record in een van de bedrijfsapps is verwijderd. Records verwijderen verwijdert de record in de app waar deze nog steeds bestaat. Met Herstellen wordt de record opnieuw gemaakt in de bedrijfsapp waarin deze is verwijderd.|

> [!NOTE]
> Om het aantal conflicten dat u moet oplossen te verminderen, kunt u uw integratietabeltoewijzingen zo instellen dat deze acties automatisch worden toegepast. Zie voor meer informatie [Integratietabellen toewijzen](admin-how-to-modify-table-mappings-for-synchronization.md#mapping-integration-tables).

## <a name="to-view-the-synchronization-log-for-a-specific-manually-synchronized-record"></a>Het synchronisatielogboek weergeven voor een specifieke (handmatig gesynchroniseerde) record
1. Open bijvoorbeeld een klant-, artikel- of andere record die gegevens synchroniseert tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en Common Data Service of [!INCLUDE[crm_md](includes/crm_md.md)].
2. Kies de actie **Synchronisatielogbestand** om het synchronisatielogbestand voor een geselecteerde record weer te geven. Bijvoorbeeld een specifieke klant die u handmatig hebt gesynchroniseerd.

## <a name="see-also"></a>Zie ook  
[Gebruikersaccounts instellen voor integratie met Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Microsoft Dynamics 365 Sales gebruiken vanuit Business Central](marketing-integrate-dynamicscrm.md)
