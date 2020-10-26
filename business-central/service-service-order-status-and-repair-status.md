---
title: Serviceorderstatus en herstelstatus | Microsoft Docs
description: Tussen het veld Status op de pagina Serviceorder en de herstelstatus van het serviceartikel, weergegeven in het veld Herstelstatuscode op de pagina Serviceorder, bestaat een bepaalde relatie in de module CRM - Service. Met de serviceorderstatus wordt de herstelstatus van de serviceartikelen in de serviceorder aangegeven.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 638b1f560dc28374e0e8d5afbc94f6ef8d416c83
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3913158"
---
# <a name="service-order-status-and-repair-status"></a>Serviceorderstatus en herstelstatus
Tussen het veld **Status** op de pagina **Serviceorder** en de herstelstatus van het serviceartikel, weergegeven in het veld **Herstelstatuscode** op de pagina **Serviceorder** , bestaat een bepaalde relatie in de module CRM - Service. Met de serviceorderstatus wordt de herstelstatus van de serviceartikelen in de serviceorder aangegeven.  

> [!NOTE]  
>  Deze twee statusvelden zijn niet gerelateerd aan het veld **Vrijgavestatus** op de serviceorderkop, dat bepaalt hoe serviceartikelen in het magazijn worden verwerkt.  

 Telkens wanneer de herstelstatus van een serviceartikel wordt gewijzigd in een serviceorder, wordt de orderstatus bijgewerkt. Als de algemene herstelstatus van de afzonderlijke serviceartikelen moet worden aangegeven, moet u het volgende opgeven:  

* De serviceorderstatus die aan elke herstelstatus is gekoppeld. Zie voor meer informatie Serviceorderstatus.  
* Het prioriteitsniveau van elke optie voor serviceorderstatus. Zie voormeer informatie Prioriteit.  

 Wanneer u een serviceofferte omzet in een serviceorder, wordt de herstelstatus van elk serviceartikel in de order gewijzigd in **Eerste** en de serviceorderstatus in **In behandeling** .  

## <a name="specifying-service-order-status-for-repair-status"></a>Serviceorderstatus opgeven voor herstelstatus  
Elke herstelstatus is gekoppeld aan een bepaalde serviceorderstatus. De opties voor de serviceorderstatus zijn als volgt: **In behandeling** , **In verwerking** , **Afwachten** en **Gereedgemeld** . De volgende herstelstatusopties zijn beschikbaar: **Eerste** , **In verwerking** , **Toegewezen** , **Deels service verleend** , **Offerte gereed** , **Wachten op klant** , **Reserveonderdeel besteld** , **Reserveonderdeel ontvangen** en **Gereedgemeld** .  

### <a name="pending"></a>In behandeling  
Met de serviceorderstatus **In behandeling** wordt aangegeven dat de service op elk moment kan worden begonnen of hervat. De herstelstatusopties **Eerste** , **Toegewezen** , **Deels service verleend** en **Reserveonderdeel ontvangen** kunnen daarom worden gekoppeld aan deze serviceorderstatus.  

### <a name="in-process"></a>In verwerking  
Met de serviceorderstatus **In verwerking** wordt aangegeven dat de service wordt uitgevoerd. De herstelstatusopties **In verwerking** en **Reserveonderdeel besteld** kunnen daarom worden gekoppeld aan deze serviceorderstatus. Als u de status **Reserveonderdeel besteld** koppelt aan de serviceorderstatus **In verwerking** , moet u ook de status **Reserveonderdeel ontvangen** koppelen aan deze serviceorderstatus.  

### <a name="on-hold"></a>Wachten  
Met de serviceorderstatus **Afwachten** wordt aangegeven dat de service tijdelijk is stilgelegd, omdat u op een antwoord van de klant of op reserveonderdelen wacht voordat de service kan worden begonnen. De herstelstatusopties **Offerte gereed** , **Reserveonderdeel besteld** en **Wachten op klant** kunnen daarom worden gekoppeld aan deze serviceorderstatus.  

### <a name="finished"></a>Gereedgemeld  
Met de serviceorderstatus **Gereedgemeld** wordt aangegeven dat de service is voltooid. De herstelstatus **Gereedgemeld** is daarom gekoppeld aan deze status.  

## <a name="assigning-priority-to-service-order-status"></a>Prioriteit toewijzen aan serviceorderstatus  
Wanneer een herstelstatus van een serviceartikel wordt gewijzigd, worden de opties voor serviceorderstatus geïdentificeerd die zijn gekoppeld aan de verschillende herstelstatusopties van de serviceartikelen in de order. Als de serviceartikelen zijn gekoppeld aan twee of meer opties voor serviceorderstatus, wordt de serviceorderstatusoptie met de hoogste prioriteit geselecteerd.  

U moet bepalen welke serviceorderstatus de belangrijkste gegevens over de status van de serviceorder bevat en aan deze status de hoogste prioriteit toewijzen, enzovoort.  

### <a name="example"></a>Opmerking  
Hier volgt een typisch voorbeeld van een toewijzing van prioriteitsniveau:  

* In verwerking: Hoog  
* In behandeling: Relatief hoog  
* Afwachten: Relatief laag  
* Gereedgemeld: Laag  

Als één serviceartikel bijvoorbeeld de herstelstatus **Eerste** heeft, gekoppeld aan de serviceorderstatus **In behandeling** , een ander serviceartikel de herstelstatus **In verwerking** heeft, gekoppeld aan de serviceorderstatus **In verwerking** , en een derde serviceartikel de herstelstatus **Reserveonderdeel besteld** , gekoppeld aan de serviceorderstatus **Afwachten** , dan is de uiteindelijke serviceorderstatus **In verwerking** , omdat deze de hoogste prioriteit heeft.  

## <a name="see-also"></a>Zie ook  
[Statussen instellen voor serviceorders en reparaties](service-order-repair-status.md)  
[CRM - Service instellen](service-setup-service.md)  
