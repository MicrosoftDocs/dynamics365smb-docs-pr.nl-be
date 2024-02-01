---
title: Handmatige synchronisatie van tabeltoewijzingen | Microsoft Docs
description: Synchronisatie kopieert gegevens tussen Microsoft Dataverse-tabellen en Business Central en houdt de gegevens in beide systemen up-to-date.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Handmatig tabeltoewijzingen synchroniseren


Een toewijzing van een integratietabel koppelt een [!INCLUDE[prod_short](includes/prod_short.md)]-tabel, zoals een klant, aan een [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabel, zoals een rekening. Als een integratietabeltoewijzing wordt gesynchroniseerd, kunt u gegevens in alle records van de [!INCLUDE[prod_short](includes/prod_short.md)]-tabel en de [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabel die zijn gekoppeld, synchroniseren. Bovendien kan synchronisatie, afhankelijk van de configuratie van de tabelkoppeling, nieuwe records maken en koppelen in de doeloplossing voor ongekoppelde records in de bron.  

Handmatig synchroniseren van integratietabeltoewijzingen kan nuttig zijn tijdens de initiële instelling van een integratie en wanneer synchronisatiefouten worden gediagnosticeerd.  

Dit artikel beschrijft drie methoden om integratietabeltoewijzingen handmatig te synchroniseren. Elke methode biedt een ander niveau van synchronisatie.

## Een volledige synchronisatie uitvoeren
Een volledige synchronisatie voert alle standaard integratiesynchronisatietaken uit voor het synchroniseren van [!INCLUDE[prod_short](includes/prod_short.md)]-records en [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabellen, zoals gedefinieerd op de pagina **Toewijzingen van integratietabellen**. 

Een volledige synchronisatie voert de volgende bewerkingen uit voor [!INCLUDE[prod_short](includes/prod_short.md)]- of [!INCLUDE[prod_short](includes/cds_long_md.md)]-records die:

* Niet zijn gekoppeld; er wordt een nieuwe overeenkomende rij gemaakt en gekoppeld in de andere oplossing.
Of en waar een rij wordt gemaakt, is afhankelijk van de synchronisatierichting. Bijvoorbeeld wanneer gegevens van [!INCLUDE[prod_short](includes/prod_short.md)]-klanten worden gesynchroniseerd met [!INCLUDE[prod_short](includes/cds_long_md.md)]-accounts als er een klant is die niet is gekoppeld aan een account, wordt automatisch een nieuw account gemaakt in [!INCLUDE[prod_short](includes/cds_long_md.md)] en aan de klant gekoppeld in [!INCLUDE[prod_short](includes/prod_short.md)]. Het tegenovergestelde is waar wanneer de synchronisatierichting van [!INCLUDE[prod_short](includes/cds_long_md.md)] naar [!INCLUDE[prod_short](includes/prod_short.md)] is. Voor elke rekening die niet al aan een klant is gekoppeld, wordt een nieuwe overeenkomende klant gemaakt in [!INCLUDE[prod_short](includes/prod_short.md)] en gekoppeld aan de rekening in [!INCLUDE[prod_short](includes/cds_long_md.md)].  

     > [!NOTE]  
     >  Om dit te bereiken wist de volledige synchronisatie tijdelijk de optie **Alleen gekoppelde records synchr.** in de integratietabeltoewijzing die wordt gebruikt door de synchronisatietaak. Aan het eind van het volledige synchronisatieproces, wordt u gevraagd of u deze optie voor alle taken gewist wilt houden.  

* Gekoppeld zijn; de synchronisatierichting (bijvoorbeeld van [!INCLUDE[prod_short](includes/prod_short.md)] naar [!INCLUDE[prod_short](includes/cds_long_md.md)] of van [!INCLUDE[prod_short](includes/cds_long_md.md)] naar [!INCLUDE[prod_short](includes/prod_short.md)]) is vooraf bepaald door de integratietabeltoewijzingen. Zie voor meer informatie [Standaardtoewijzing van tabel voor synchronisatie](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).  

> [!IMPORTANT]  
>  U kunt meestal alleen de hele synchronisatie gebruiken wanneer u integratie voor het eerst instelt tussen [!INCLUDE[prod_short](includes/prod_short.md)] en [!INCLUDE[prod_short](includes/cds_long_md.md)] en slechts één oplossing gegevens bevat, die u naar de andere oplossing wilt kopiëren. Een volledige synchronisatie kan nuttig zijn in een demonstratieomgeving. Omdat de hele synchronisatie automatisch records maakt en koppelt tussen de oplossingen, wordt het sneller om te beginnen met werken met het synchroniseren van gegevens tussen records. Van de andere kant moet u alleen een volledige synchronisatie uitvoeren als u een rij in [!INCLUDE[prod_short](includes/prod_short.md)] wilt voor elke rij in [!INCLUDE[prod_short](includes/cds_long_md.md)], voor de betrokken tabeltoewijzingen. Anders kunt u ongewenste of dubbele records [!INCLUDE[prod_short](includes/prod_short.md)] of [!INCLUDE[prod_short](includes/cds_long_md.md)] hebben.  

### Een volledige synchronisatie uitvoeren  
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Dataverse-verbinding instellen** in en kies vervolgens de gerelateerde koppeling.

    > [!NOTE]
    > Als u een volledige synchronisatie voor tabellen wilt uitvoeren via Dynamics 365 Sales, gebruikt u de pagina **Microsoft Dynamics 365 Sales-verbinding instellen**.

2.  Kies de actie **Volledige synchronisatie uitvoeren** en kies vervolgens de knop **Ja**.  
3.  Wanneer de volledige synchronisatie is voltooid, kunt u opgeven of geplande synchronisatietaken nieuwe records mogen maken.  

    Als u wilt dat alle synchronisatietaken nieuwe records maken op de bestemming voor ongekoppelde records in de bron, kiest u **Ja**. Dit stelt het veld **Alleen gekoppelde records synchr.** in de tabeltoewijzingen in die worden gebruikt door de synchronisatietaken.  

    Als u wilt dat synchronisatietaken worden uitgevoerd zoals vóór de volledige synchronisatie, met betrekking tot het maken van nieuwe records, kiest u **Nee**. Dit stelt het veld **Alleen gekoppelde records synchr.** in op de instelling van vóór de volledige synchronisatie.  

U kunt de resultaten van de volledige synchronisatie bekijken op de pagina **Synchronisatietaken voor integratie**. Zie voor meer informatie [De status van een synchronisatie weergeven](admin-how-to-view-synchronization-status.md),  

## Alle gewijzigde records synchroniseren
U kunt de pagina **Common Data Service-verbinding instellen** gebruiken om wijzigingen in gegevens te synchroniseren in alle integratietabeltoewijzingen. Dit is vergelijkbaar met een volledige synchronisatie. Gegevens worden gesynchroniseerd in alle gekoppelde records in de [!INCLUDE[prod_short](includes/prod_short.md)]-tabellen en [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabellen die zijn gedefinieerd in de tabeltoewijzingen. Standaard worden alleen gegevens gesynchroniseerd die zijn gewijzigd na de laatste synchronisatie. Synchronisatietaken synchroniseren tabeltoewijzingen in de volgende volgorde om koppelingsafhankelijkheden tussen de tabellen te voorkomen:  

1.  VALUTA  
2.  VERKOPERS  
3.  LEVERANCIER  
4.  KLANT  
5.  CONTACTEN  

U kunt de resultaten van de synchronisatie bekijken op de pagina **Synchronisatietaken voor integratie**. Zie voor meer informatie [De status van een synchronisatie weergeven](admin-how-to-view-synchronization-status.md),  

> [!TIP]  
>  Door de integratietabeltoewijzing vooraf te wijzigen kunt u filters maken om te bepalen welke gegevens worden gesynchroniseerd of toewijzingen configureren om nieuwe gegevens te maken in de doeloplossing voor niet-gekoppelde records of rijen in de bron. Zie voor meer informatie [Tabeltoewijzingen wijzigen voor synchronisatie](admin-how-to-modify-table-mappings-for-synchronization.md).

### Gegevens voor alle tabellen synchroniseren  
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Instellingen Microsoft Dynamics 365 Sales-verbinding** in en kies vervolgens de gerelateerde koppeling.
2.  Kies de actie **Gewijzigde records synchroniseren**, en kies vervolgens **Ja**.  

## Afzonderlijke tabeltoewijzingen synchroniseren
U kunt de pagina **Toewijzingen van integratietabellen** gebruiken om een synchronisatietaak uit te voeren voor tabeltoewijzingen. Gegevens worden dan gesynchroniseerd voor alle gekoppelde records en rijen in de [!INCLUDE[prod_short](includes/prod_short.md)]-tabel en de [!INCLUDE[prod_short](includes/cds_long_md.md)]-tabel die worden gedefinieerd door de tabeltoewijzing. Standaard worden alleen gegevens gesynchroniseerd die zijn gewijzigd na de laatste synchronisatie.  

### Records synchroniseren van een integratietabeltoewijzing  
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Toewijzingen van integratietabellen** in en kies vervolgens de gerelateerde koppeling.
2.  Kies de actie **Gewijzigde records synchroniseren**, en kies vervolgens **Ja**.  

## Zie ook  
[Business Central en Dynamics 365 Sales synchroniseren](admin-synchronizing-business-central-and-sales.md)   
[Gebruikersaccounts instellen voor integratie met Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]