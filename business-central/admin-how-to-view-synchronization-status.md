---
title: De status van synchronisatietaken weergeven (bevat video)
description: Gebruik de pagina Synchronisatiefouten met gekoppelde gegevens om de status weer te geven van synchronisatietaken die zijn uitgevoerd voor gekoppelde records in integraties.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
ms.search.form: 6250
ms.date: 06/14/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# De status van synchronisatietaken weergeven


Gebruik de pagina **Synchronisatiefouten met gekoppelde gegevens** om de status weer te geven van synchronisatietaken die zijn uitgevoerd voor gekoppelde records in een Dataverse- of een [!INCLUDE[crm_md](includes/crm_md.md)]-integratie. Hieronder vallen taken die zijn uitgevoerd vanuit de verwerkingswachtrij en handmatige synchronisatietaken die zijn uitgevoerd op records vanuit de [!INCLUDE[prod_short](includes/prod_short.md)]-client. Het bekijken van hun status is bijvoorbeeld handig bij het oplossen van problemen omdat het u toegang geeft tot details over fouten met betrekking tot gekoppelde records. Meestal worden dit soort fouten veroorzaakt door gebruikersacties, bijvoorbeeld wanneer:  

* Twee personen hebben in beide zakelijke apps een wijziging aangebracht in dezelfde gegevens.
* Iemand heeft gegevens verwijderd in een van de apps, maar niet in beide.

> [!Note]
> De pagina **Synchronisatiefouten met gekoppelde gegevens** toont informatie over taken gerelateerd aan gekoppelde records. Als u alle fouten oplost maar records nog steeds niet synchroniseren, heeft dit mogelijk te maken met een instelling voor de integratie. Doorgaans moet uw beheerder dit soort fouten oplossen.   

## Voorbeeld
Deze video toont een voorbeeld van het oplossen van fouten die zijn opgetreden tijdens het synchroniseren met [!INCLUDE[prod_short](includes/cds_long_md.md)]. Het proces is voor alle integraties hetzelfde. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]


## Synchronisatiefouten voor gekoppelde records weergeven en oplossen
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Synchronisatiefouten met gekoppelde gegevens** in en kies vervolgens de gerelateerde koppeling.
2. De pagina **Synchronisatiefouten met gekoppelde gegevens** bevat problemen die zijn opgetreden toen u gekoppelde records synchroniseerde. De volgende tabel bevat acties die u kunt gebruiken om problemen één voor één op te lossen:

|Actie|Omschrijving|
|----|----|
|**Koppeling verwijderen**|Ontkoppelt de records en deze zullen niet langer synchroniseren. Om de synchronisatie te hervatten moet u ze opnieuw koppelen. |
|**Opnieuw** en **Alles opnieuw proberen**|Voor elke record waarin een fout wordt gevonden, wordt de synchronisatie overgeslagen, tenzij u het probleem verhelpt. Met Opnieuw zal de geselecteerde record worden opgenomen in de volgende synchronisatie en met **Alles opnieuw proberen** worden alle records opgenomen.|
|**Synchroniseren**|De app probeert een conflict op te lossen waarbij gegevens zijn gewijzigd in beide zakelijke apps. U kunt kiezen welke gegevens worden gebruikt.|
|**Records herstellen** en **Records verwijderen**|Deze zijn handig wanneer een record in een van de bedrijfsapps is verwijderd. Records verwijderen verwijdert de record of rij in de app waar deze nog steeds bestaat. Met Records herstellen wordt de record of rij opnieuw gemaakt in de bedrijfsapp waarin deze is verwijderd.|

> [!NOTE]
> Om het aantal conflicten dat u moet oplossen te verminderen, kunt u uw integratietabeltoewijzingen zo instellen dat deze acties automatisch worden toegepast. Zie voor meer informatie [Integratietabellen toewijzen](admin-how-to-modify-table-mappings-for-synchronization.md#mapping-integration-tables).

## Het synchronisatielogboek weergeven voor een specifieke (handmatig gesynchroniseerde) record
1. Open bijvoorbeeld een klant-, artikel- of andere record die gegevens synchroniseert tussen [!INCLUDE[prod_short](includes/prod_short.md)] en Dataverse of [!INCLUDE[crm_md](includes/crm_md.md)].
2. Kies de actie **Synchronisatielogbestand** om het synchronisatielogbestand voor een geselecteerde record weer te geven. Bijvoorbeeld een specifieke klant die u handmatig hebt gesynchroniseerd.

## Koppelingen tussen records verwijderen
Als er iets misgaat in uw integratie en u records moet ontkoppelen om ze niet meer te laten synchroniseren, kunt u dit voor één of meer records tegelijk doen. U kunt een of meer records loskoppelen van lijstpagina's of de pagina **Fouten met gekoppelde gegevenssynchronisatie** door een of meer regels te kiezen en **Koppeling verwijderen** te kiezen. U kunt ook alle koppelingen verwijderen voor een of meer tabeltoewijzingen op de pagina **Integratietabeltoewijzingen**. 

Als een entiteit met een unidirectionele koppeling wordt verwijderd in [!INCLUDE[prod_short](includes/prod_short.md)], moet u de verbroken koppeling handmatig verwijderen. Om dat te doen, kiest u op de pagina **Synchronisatiefouten met gekoppelde gegevens**, kiest u de actie **Zoeken naar verwijderde** en verwijdert u vervolgens de koppelingen.

## Zie ook  
[Gebruikersaccounts instellen voor integratie met Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Microsoft Dynamics 365 Sales gebruiken vanuit Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]