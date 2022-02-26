---
title: Uw gegevens verbinden met Power Automate | Microsoft Docs
description: U kunt uw Business Central-gegevens als gegevensbron beschikbaar maken en een OData-URL van uw webservices opgeven om een geautomatiseerde werkstroom te maken.
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions
ms.date: 07/27/2021
ms.author: edupont
author: jswymer
ms.openlocfilehash: fb79c3ab799c5a77ff725ce05d1469f5bec7c9f5
ms.sourcegitcommit: 769d20d299155cba30c35636d02b2ef021e4ecc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/29/2021
ms.locfileid: "6688388"
---
# <a name="using-prod_short-in-an-automated-workflow"></a>[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken in een geautomatiseerde werkstroom

U kunt uw [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens als onderdeel van een werkstroom in Microsoft Power Automate gebruiken.

> [!NOTE]
> Naast Power Automate kunt u de werkstroomfunctionaliteit binnen [!INCLUDE[prod_short](includes/prod_short.md)] gebruiken. Het zijn twee aparte werkstroomsystemen, maar elke werkstroomsjabloon die u maakt met Power Automate, wordt toegevoegd aan de lijst met werkstromen in [!INCLUDE[prod_short](includes/prod_short.md)]. Zie [Werkstroom](across-workflow.md) voor meer informatie.  

> [!NOTE]  
> U moet een geldig account bij [!INCLUDE[prod_short](includes/prod_short.md)] en Power Automate hebben.  

## <a name="add-prod_short-as-a-data-source-in-power-automate"></a>[!INCLUDE[prod_short](includes/prod_short.md)] als gegevensbron toevoegen in Power Automate

1. Navigeer in uw browser naar [flow.microsoft.com](https://flow.microsoft.com) en meld u aan.
2. Kies **Mijn Flows** vanuit het lint boven aan de pagina.
3. Er zijn 3 manieren om een stroom te maken; **Beginnen met sjabloon**, **Geheel nieuw maken** en **Beginnen met een connector**. Een sjabloon is een vooraf gedefinieerde stroom die voor u is gemaakt. Als u een sjabloon wilt gebruiken, selecteert u deze en maakt u een verbinding voor elke service die de sjabloon gebruikt. Met de opties **Geheel nieuw maken** en **Beginnen met een connector** kunt u een volledig nieuwe stroom maken.
4. Als u een geheel nieuwe stroom wilt maken, kiest u op de pagina **Mijn Flows** de opties **Geheel nieuw maken** en **Geautomatiseerde stroom**.
5. Zoek **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]**-connector.
6. Definieer een naam en kies de trigger die u voor uw stroom wilt gebruiken.
7. Selecteer in de lijst met beschikbare triggers een van de beschikbare [!INCLUDE[prod_short](includes/prod_short.md)]-triggers:  

    - *Wanneer goedkeuring van een leverancier wordt aangevraagd*  
    - *Wanneer goedkeuring van een dagboekregel wordt aangevraagd* 
    - *Wanneer een record wordt verwijderd*
    - *Wanneer een record wordt gewijzigd*
    - *Wanneer een record wordt gemaakt*
    - *Wanneer een record wordt aangepast*
    - *Wanneer goedkeuring van een dagboekbatch wordt aangevraagd* 
    - *Wanneer een klantgoedkeuring wordt aangevraagd*
    - *Wanneer goedkeuring van een artikel wordt aangevraagd*
    - *Wanneer goedkeuring van een inkoopdocument wordt aangevraagd*
    - *Wanneer goedkeuring van een verkoopdocument wordt aangevraagd*

8. Power Automate vraagt u een omgeving en bedrijf in uw [!INCLUDE[prod_short](includes/prod_short.md)]-tenant te selecteren, plus eventuele voorwaarden in uw gegevens te selecteren waarop u moet letten.

    > [!NOTE]
    > De [!INCLUDE[prod_short](includes/prod_short.md)]-connector voor Power Automate ondersteunt meerdere productie- en sandboxomgevingen. Als u niet meerdere productie- of sandboxomgevingen hebt gemaakt, is **Productie** de enige beschikbare optie die u kunt kiezen.  

    Nu hebt u met succes een verbinding gemaakt met uw Business Central[!INCLUDE[prod_short](includes/prod_short.md)]-gegevens en kunt u uw stroom gaan maken.

9. Als u een flow van een sjabloon wilt maken, kiest u de optie **Beginnen met sjabloon**.
10. Zoek **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]**-sjablonen.
11. Selecteer een van de sjablonen in de lijst met beschikbare sjablonen en kies vervolgens **Maken**.  

    - *Goedkeuring aanvragen voor Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-verkooporder*
    - *Goedkeuring aanvragen voor Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-verkoopofferte*
    - *Goedkeuring aanvragen voor Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-verkoopfactuur*
    - *Goedkeuring aanvragen voor Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-verkoopcreditnota*
    - *Goedkeuring aanvragen voor Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-klant*
    - *Goedkeuring aanvragen voor Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-inkooporder*
    - *Goedkeuring aanvragen voor Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-inkoopfactuur*
    - *Goedkeuring aanvragen voor Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-inkoopcreditnota*  
    - *Goedkeuring aanvragen voor Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-artikel*
    - *Goedkeuring aanvragen voor Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-leverancier*
    - *Goedkeuring aanvragen voor Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-dagboekbatch*  
    - *Goedkeuring aanvragen voor Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]-dagboekregels*
12. Power Automate geeft een lijst met services weer die in de stroomsjabloon worden gebruikt en probeert automatisch verbinding te maken met die services. Als u nog niet eerder verbinding hebt gemaakt met een service, wordt u gevraagd zich aan te melden bij elke service waarmee u verbinding wilt maken. Een groen vinkje verschijnt naast elke service zodra een verbinding tot stand is gebracht. Selecteer **Doorgaan**.
13. Power Automate vraagt u een omgeving en bedrijf in uw [!INCLUDE[prod_short](includes/prod_short.md)]-tenant te selecteren. Aangezien elke stap in de stroom onafhankelijk is van de volgende, moet u de omgeving en het bedrijf mogelijk meerdere malen definiëren wanneer u een [!INCLUDE[prod_short](includes/prod_short.md)] Power Automate-sjabloon gebruikt.

Zie voor meer informatie de [documentatie van Power Automate](/power-automate/getting-started).

## <a name="troubleshooting"></a>Problemen oplossen

### <a name="entity-set-not-found-error"></a>Fout "Entiteitset niet gevonden"

#### <a name="problem"></a>Probleem

Bij het aanmaken van een nieuwe Power Automate-stroom met een [!INCLUDE[prod_short](includes/prod_short.md)]-goedkeuringstrigger, zoals *Wanneer goedkeuring van een inkoopdocument wordt aangevraagd*, krijgt u een foutmelding die lijkt op:

**Entiteitset niet gevonden: \<name\>**

waarbij **\<name\>** de servicenaam van de ontbrekende webservice is, bijvoorbeeld **workflowWebhookSubscriptions** of **workflowPurchaseDocumentLines**.

#### <a name="possible-cause"></a>Mogelijke oorzaak

Gebruik maken van Power Automate om te integreren met uw [!INCLUDE[prod_short](includes/prod_short.md)]-goedkeuringen vereist dat bepaalde pagina- en codeunit-objecten worden gepubliceerd als webservices. Standaard worden de meeste vereiste objecten voor u gepubliceerd als webservices. Maar in sommige gevallen is uw omgeving mogelijk aangepast zodat deze objecten niet langer worden gepubliceerd.

#### <a name="fix"></a>Oplossing

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

[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Werkstroom](across-workflow.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)  
[[!INCLUDE[prod_long](includes/prod_long.md)]-werkstromen beheren](across-use-workflows.md)  
[Gebruikersinstellingen voor goedkeuring](across-how-to-set-up-approval-users.md)  
[Instellen van [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Financiën](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]