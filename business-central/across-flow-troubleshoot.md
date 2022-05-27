---
title: Problemen met uw geautomatiseerde werkstromen oplossen
description: Meer informatie over het oplossen van problemen tussen Business Central en Power Automate wanneer u een geautomatiseerde workflow maakt.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2022
ms.author: edupont
author: jswymer
ms.openlocfilehash: b8fff95ced93e7ee2a3112969f45525532b19445
ms.sourcegitcommit: e86f0bd15604c2fb327e3182929c44a4172790c7
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 05/20/2022
ms.locfileid: "8786208"
---
# <a name="troubleshoot-your-prod_short-automated-workflows"></a>Problemen met uw geautomatiseerde [!INCLUDE[prod_short](includes/prod_short.md)]-werkstromen oplossen

Wanneer u [!INCLUDE [prod_short](includes/prod_short.md)] verbindt met Power Automate om geautomatiseerde werkstromen te maken, kunt u foutmeldingen tegenkomen. Dit artikel biedt voorgestelde oplossingen voor vaak terugkerende problemen.

## <a name="flow-doesnt-run-on-all-records-created-or-changed"></a>Stroom wordt niet uitgevoerd op alle records die zijn gemaakt of gewijzigd

### <a name="problem"></a>Probleem

Als een gebeurtenis veel records maakt of wijzigt, wordt de stroom niet uitgevoerd voor sommige of alle records.

### <a name="possible-cause"></a>Mogelijke oorzaak

Momenteel is er een limiet voor het aantal records dat een stroom kan verwerken. Als er binnen 30 seconden meer dan 100 records worden gemaakt of gewijzigd, wordt de stroom niet geactiveerd.

> [!NOTE]
> Voor ontwikkelaars wordt de stroomtriggering gedaan via webhook-berichten en deze beperking is te wijten aan de manier waarop de Business Central-connector omgaat met `collection`-berichten. Zie voor meer informatie [Werken met webhooks in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/api-reference/v2.0/dynamics-subscriptions#notes-for-power-automate-flows) in de Help voor ontwikkelaars en beheerders.

## <a name="entity-set-not-found-error"></a>Fout "Entiteitset niet gevonden"

### <a name="problem"></a>Probleem

Bij het aanmaken van een nieuwe Power Automate-stroom met een [!INCLUDE[prod_short](includes/prod_short.md)]-goedkeuringstrigger, zoals *Wanneer goedkeuring van een inkoopdocument wordt aangevraagd*, kunt u een foutmelding krijgen die lijkt op:

`Entity set not found: \<name\>`

De plaatshouder `\<name\>` is de servicenaam van de ontbrekende webservice, zoals *workflowWebhookSubscriptions* of *workflowPurchaseDocumentLines*.

### <a name="possible-cause"></a>Mogelijke oorzaak

Gebruik van Power Automate voor uw goedkeuringen vereist dat bepaalde pagina- en codeunit-objecten worden gepubliceerd als webservices. Standaard worden de meeste vereiste objecten voor u gepubliceerd als webservices. Maar in sommige gevallen is uw omgeving mogelijk aangepast zodat deze objecten niet langer worden gepubliceerd.

### <a name="fix"></a>Oplossing

Ga naar de pagina **Webservices** en zorg ervoor dat de volgende objecten worden gepubliceerd als webservices. Er moet een item in de lijst zijn voor elk object, met het selectievakje **Gepubliceerd** geselecteerd.  

|Objecttype|Object-id|Objectnaam|Servicenaam|
|-----------|---------|-----------|------------|
|Codeunit|  1544    |WorkflowWebhookSubscription|WorkflowActionResponse|
|Pagina|  6408|   workflowCustomers|  workflowCustomers|
|Pagina   |6406   |workflowGenJournalBatches| workflowGenJournalBatches|
|Pagina   |6407   |workflowGenJournalLines|workflowGenJournalLines|
|Pagina   |6409   |workflowItems| workflowItems|
|Pagina   |6405   |Entiteit inkoopdocumentregel|workflowPurchaseDocumentLines|
|Pagina|  6404    |workflowPurchaseDocuments| workflowPurchaseDocuments|
|Pagina|  6403    |Entiteit verkoopdocumentregel |workflowSalesDocumentLines|
|Pagina|  6402|   workflowSalesDocuments| workflowSalesDocuments|
|Pagina|  6410    |workflowVendors|   workflowVendors|
|Pagina|  831 |workflowWebhookSubscriptions|  workflowWebhookSubscriptions|

> [!NOTE]
> De waarde van **Servicenaam** moet precies zijn zoals weergegeven in de tabel. Wijzig of vertaal de servicenaam niet.

Zie [Een webservice publiceren](across-how-publish-web-service.md) voor meer informatie over het publiceren van webservices.

## <a name="see-also"></a>Zie ook

[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken in een geautomatiseerde werkstroom](across-how-use-financials-data-source-flow.md)  
[Werkstroom](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]