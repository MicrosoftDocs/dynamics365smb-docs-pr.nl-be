---
title: Handmatige synchronisatie van tabeltoewijzingen | Microsoft Docs
description: Synchronisatie kopieert gegevens tussen Dynamics 365 for Sales-posten en Business Central en houdt de gegevens in beide systemen up-to-date.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 368bfc191aea4ae00c53d0c7ee892f3cc82c0ff7
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245743"
---
# <a name="manually-synchronize-table-mappings"></a>Handmatig tabeltoewijzingen synchroniseren
Een toewijzing van een integratietabel koppelt een [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel (recordtype), zoals een klant, aan een [!INCLUDE[crm_md](includes/crm_md.md)]-entiteit, zoals een rekening. Als een integratietabeltoewijzing wordt gesynchroniseerd, kunt u gegevens in alle records van de [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel en de [!INCLUDE[crm_md](includes/crm_md.md)]-entiteit die zijn gekoppeld, synchroniseren. Bovendien kan synchronisatie, afhankelijk van de configuratie van de tabelkoppeling, nieuwe records maken en koppelen in de doeloplossing voor ongekoppelde records in de bron.  

Handmatig synchroniseren van integratietabeltoewijzingen kan nuttig zijn tijdens de initiële instelling van een integratie en wanneer synchronisatiefouten worden gediagnosticeerd.  

Dit artikel beschrijft drie methoden om integratietabeltoewijzingen handmatig te synchroniseren. Elke methode biedt een ander niveau van synchronisatie.

## <a name="run-a-full-synchronization"></a>Een volledige synchronisatie uitvoeren
Een volledige synchronisatie voert alle standaard integratiesynchronisatietaken uit voor het synchroniseren van [!INCLUDE[d365fin](includes/d365fin_md.md)]-records en [!INCLUDE[crm_md](includes/crm_md.md)]-entiteiten, zoals gedefinieerd op de pagina **Toewijzingen van integratietabellen**. 

Een volledige synchronisatie voert de volgende bewerkingen uit voor [!INCLUDE[d365fin](includes/d365fin_md.md)]- of [!INCLUDE[crm_md](includes/crm_md.md)]-records die:

* Niet zijn gekoppeld; er wordt een nieuwe overeenkomende record gemaakt en gekoppeld in de andere oplossing.
Of en waar een record wordt gemaakt, is afhankelijk van de synchronisatierichting. Bijvoorbeeld wanneer gegevens van [!INCLUDE[d365fin](includes/d365fin_md.md)]-klanten worden gesynchroniseerd met [!INCLUDE[crm_md](includes/crm_md.md)]-accounts als er een klant is die niet is gekoppeld aan een account, wordt automatisch een nieuw account gemaakt in [!INCLUDE[crm_md](includes/crm_md.md)] en aan de klant gekoppeld in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Het tegenovergestelde is waar wanneer de synchronisatierichting van [!INCLUDE[crm_md](includes/crm_md.md)] naar [!INCLUDE[d365fin](includes/d365fin_md.md)] is. Voor elke rekening die niet al aan een klant is gekoppeld, wordt een nieuwe overeenkomende klant gemaakt in [!INCLUDE[d365fin](includes/d365fin_md.md)] en gekoppeld aan de rekening in [!INCLUDE[crm_md](includes/crm_md.md)].  

     > [!NOTE]  
     >  Om dit te bereiken wist de volledige synchronisatie tijdelijk de optie **Alleen gekoppelde records synchr.** in de integratietabeltoewijzing die wordt gebruikt door de synchronisatietaak. Aan het eind van het volledige synchronisatieproces, wordt u gevraagd of u deze optie voor alle taken gewist wilt houden.  

* Gekoppeld zijn; de synchronisatierichting (bijvoorbeeld van [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)] of van [!INCLUDE[crm_md](includes/crm_md.md)] naar [!INCLUDE[d365fin](includes/d365fin_md.md)]) is vooraf bepaald door de integratietabeltoewijzingen. Zie voor meer informatie [Standaardtoewijzing van Sales-entiteit voor synchronisatie](admin-synchronizing-business-central-and-sales.md#standard-sales-entity-mapping-for-synchronization).  

De taken worden uitgevoerd in de volgende volgorde om koppelingsafhankelijkheden tussen entiteiten te voorkomen.  

1.  VALUTA - Dynamics 365 for Sales-synchronisatietaak  
2.  VERKOPERS - Dynamics 365 for Sales-synchronisatietaak  
3.  MAATEENHEID - Dynamics 365 for Sales-synchronisatietaak  
4.  KLANT - Dynamics 365 for Sales-synchronisatietaak  
5.  CONTACTEN - Dynamics 365 for Sales-synchronisatietaak  
6.  RESOURCE - PRODUCT - Dynamics 365 for Sales-synchronisatietaak  
7.  ARTIKEL-PRODUCT - Dynamics 365 for Sales-synchronisatietaak  

> [!IMPORTANT]  
>  U kunt meestal alleen de hele synchronisatie gebruiken wanneer u integratie voor het eerst instelt tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] en slechts één oplossing gegevens bevat, die u naar de andere oplossing wilt kopiëren. Een volledige synchronisatie kan nuttig zijn in een demonstratieomgeving. Omdat de hele synchronisatie automatisch records maakt en koppelt tussen de oplossingen, wordt het sneller om te beginnen met werken met het synchroniseren van gegevens tussen records. Van de andere kant moet u alleen een volledige synchronisatie uitvoeren als u een record in [!INCLUDE[d365fin](includes/d365fin_md.md)] wilt voor elke record in [!INCLUDE[crm_md](includes/crm_md.md)], voor de betrokken tabeltoewijzingen. Anders kunt u ongewenste of dubbele records [!INCLUDE[d365fin](includes/d365fin_md.md)] of [!INCLUDE[crm_md](includes/crm_md.md)] hebben.  

### <a name="see-the-process-for-a-full-synchronization"></a>Zie het proces voor een hele synchronisatie
> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085502]

### <a name="to-run-a-full-synchronization"></a>Een volledige synchronisatie uitvoeren  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Microsoft Dynamics 365 for Sales-verbinding instellen** in en kies vervolgens de gerelateerde koppeling.
2.  Kies de actie **Volledige synchronisatie uitvoeren** en kies vervolgens de knop **Ja**.  
3.  Wanneer de volledige synchronisatie is voltooid, kunt u opgeven of geplande synchronisatietaken nieuwe records mogen maken.  

    Als u wilt dat alle synchronisatietaken nieuwe records maken op de bestemming voor ongekoppelde records in de bron, kiest u **Ja**. Dit stelt het veld **Alleen gekoppelde records synchr.** in de tabeltoewijzingen in die worden gebruikt door de synchronisatietaken.  

    Als u wilt dat synchronisatietaken worden uitgevoerd zoals vóór de volledige synchronisatie, met betrekking tot het maken van nieuwe records, kiest u **Nee**. Dit stelt het veld **Alleen gekoppelde records synchr.** in op de instelling van vóór de volledige synchronisatie.  

U kunt de resultaten van de volledige synchronisatie bekijken op de pagina **Synchronisatietaken voor integratie**. Zie voor meer informatie [De status van een synchronisatie weergeven](admin-how-to-view-synchronization-status.md),  

## <a name="synchronizing-all-modified-records"></a>Alle gewijzigde records synchroniseren
U kunt de pagina **Microsoft Dynamics 365 for Sales-verbinding instellen** gebruiken om wijzigingen in gegevens te synchroniseren in alle integratietabeltoewijzingen. Dit is vergelijkbaar met een volledige synchronisatie. Gegevens worden gesynchroniseerd in alle gekoppelde records in de [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen en [!INCLUDE[crm_md](includes/crm_md.md)]-entiteiten die zijn gedefinieerd in de tabeltoewijzingen. Standaard worden alleen records gesynchroniseerd die zijn gewijzigd na de vorige keer dat ze zijn gesynchroniseerd. De tabeltoewijzingen worden gesynchroniseerd in de volgende volgorde om koppelingsafhankelijkheden tussen de entiteiten te voorkomen:  

1.  VALUTA - Dynamics 365 for Sales-synchronisatietaak  
2.  VERKOPERS - Dynamics 365 for Sales-synchronisatietaak  
3.  MAATEENHEID - Dynamics 365 for Sales-synchronisatietaak  
4.  KLANT - Dynamics 365 for Sales-synchronisatietaak  
5.  CONTACTEN - Dynamics 365 for Sales-synchronisatietaak  
6.  RESOURCE-PRODUCT \- Dynamics 365 for Sales-synchronisatietaak  
7.  ARTIKEL-PRODUCT - Dynamics 365 for Sales-synchronisatietaak  

U kunt de resultaten van de synchronisatie bekijken op de pagina **Synchronisatietaken voor integratie**. Zie voor meer informatie [De status van een synchronisatie weergeven](admin-how-to-view-synchronization-status.md),  

> [!TIP]  
>  Door de integratietabeltoewijzing vooraf te wijzigen kunt u de synchronisatie configureren met filters om te bepalen welke records worden gesynchroniseerd of deze configureren om nieuwe records te maken in de doeloplossing voor niet-gekoppelde records in de bron. Zie voor meer informatie [Tabeltoewijzingen wijzigen voor synchronisatie](admin-how-to-modify-table-mappings-for-synchronization.md).

### <a name="to-synchronize-records-for-all-tables"></a>Records voor alle tabellen synchroniseren  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Microsoft Dynamics 365 for Sales-verbinding instellen** in en kies vervolgens de gerelateerde koppeling.
2.  Kies de actie **Gewijzigde records synchroniseren**, en kies vervolgens **Ja**.  

## <a name="synchronize-individual-table-mappings"></a>Afzonderlijke tabeltoewijzingen synchroniseren
U kunt de pagina **Toewijzingen van integratietabellen** gebruiken om een synchronisatietaak uit te voeren voor specifieke tabeltoewijzingen. Gegevens worden dan gesynchroniseerd in alle gekoppelde records in de [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel en de [!INCLUDE[crm_md](includes/crm_md.md)]-entiteit die worden gedefinieerd door de tabeltoewijzing. Standaard worden alleen records gesynchroniseerd die zijn gewijzigd na de vorige keer dat ze zijn gesynchroniseerd.  

Door de integratietabeltoewijzing vooraf te wijzigen kunt u de synchronisatietaak configureren om nieuwe records in de doeloplossing te maken voor niet-gekoppelde records in de bron.

### <a name="to-synchronize-records-of-an-integration-table-mapping"></a>Records synchroniseren van een integratietabeltoewijzing  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Toewijzingen van integratietabellen** in en kies vervolgens de gerelateerde koppeling.
2.  Kies de actie **Gewijzigde records synchroniseren**, en kies vervolgens **Ja**.  

## <a name="see-also"></a>Zie ook  
[Gegevens synchroniseren in Business Central en Dynamics 365 for Sales](admin-synchronizing-business-central-and-sales.md)   
[Dynamics 365 for Sales-integratie instellen in Business Central](admin-setting-up-integration-with-dynamics-sales.md)   
