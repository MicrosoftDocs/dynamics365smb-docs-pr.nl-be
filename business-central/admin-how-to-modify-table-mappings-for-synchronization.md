---
title: De te synchroniseren tabellen en velden toewijzen | Microsoft Docs
description: Hier vindt u informatie over het toewijzen van tabellen en velden voor de synchronisatie van gegevens tussen Business Central en Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 12/18/2019
ms.author: bholtorf
ms.openlocfilehash: 371bd80c04917495ea1b35f214d10d716ed5f9ad
ms.sourcegitcommit: b570997f93d1f7141bc9539c93a67a91226660a8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/08/2020
ms.locfileid: "2943125"
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a>De te synchroniseren tabellen en velden toewijzen
De basis voor de synchronisatie van gegevens in [!INCLUDE[d365fin](includes/d365fin_md.md)]met gegevens in [!INCLUDE[crm_md](includes/crm_md.md)] is de toewijzing van de tabellen en velden met de gegevens aan elkaar. Toewijzing gebeurt via integratietabellen. 

## <a name="mapping-integration-tables"></a>Integratietabellen toewijzen
Een integratietabel is een tabel in de [!INCLUDE[d365fin](includes/d365fin_md.md)]-database die een entiteit vertegenwoordigt, zoals een account, in [!INCLUDE[crm_md](includes/crm_md.md)]. Integratietabellen bevatten velden die overeenkomen met de velden in de tabel voor de [!INCLUDE[crm_md](includes/crm_md.md)]-entiteit. De tabel Accountintegratie maakt bijvoorbeeld verbinding met de entiteit Accounts in [!INCLUDE[crm_md](includes/crm_md.md)]. Voor elke entiteit in [!INCLUDE[crm_md](includes/crm_md.md)] die u wilt synchroniseren met gegevens in [!INCLUDE[d365fin](includes/d365fin_md.md)], moet er een integratietabeltoewijzing zijn.

Wanneer u de verbinding tussen de apps maakt, stelt [!INCLUDE[d365fin](includes/d365fin_md.md)] enkele standaardtabel- en veldtoewijzingen in. U kunt desgewenst de tabeltoewijzingen wijzigen. Zie voor meer informatie [Standaardtoewijzing van Sales-entiteit voor synchronisatie](admin-synchronizing-business-central-and-sales.md#standard-sales-entity-mapping-for-synchronization). Als u de standaardtoewijzingen hebt gewijzigd en uw wijzigingen wilt terugdraaien, gaat u naar de pagina **Dynamics 365-verbinding instellen** en kiest u **Standaardsynchronisatie-instellingen gebruiken**.

> [!Note]
> Als u een lokale versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruikt, worden de integratietabeltoewijzingen opgeslagen in tabel 5335 Integratietabeltoewijzingen en kunnen deze worden weergegeven en gewijzigd vanaf pagina 5335 Integratietabeltoewijzingen. Complexe toewijzingen en synchronisatieregels worden gedefinieerd in codeunit 5341. 

### <a name="synchronization-rules"></a>Synchronisatieregels
Een integratietabeltoewijzing bevat ook regels die bepalen hoe integratie-synchronisatietaken records in een [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel en een entiteit in [!INCLUDE[crm_md](includes/crm_md.md)] synchroniseren. Zie voor meer informatie [Synchronisatieregels](admin-synchronizing-business-central-and-sales.md#synchronization-rules). 

## <a name="mapping-integration-fields"></a>Integratievelden toewijzen
Het toewijzen van tabellen is slechts de eerste stap. U moet ook de velden in de tabellen toewijzen. Integratieveldtoewijzingen koppelen velden in [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen met overeenkomstige velden in [!INCLUDE[crm_md](includes/crm_md.md)] en bepalen of gegevens in elke tabel moeten worden gesynchroniseerd. De standaardtabeltoewijzing die [!INCLUDE[d365fin](includes/d365fin_md.md)] biedt, bevat veldtoewijzingen, maar u kunt deze desgewenst wijzigen. Zie [Entiteittoewijzingen weergeven](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-entity-mappings) voor meer informatie.

> [!Note]
> Als u een on-premises versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruikt, zijn integratieveldtoewijzingen gedefinieerd in tabel 5336 Integratieveldtoewijzing.

## <a name="coupling-records"></a>Records koppelen
Koppeling koppelt records in [!INCLUDE[crm_md](includes/crm_md.md)] aan records in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Bijvoorbeeld: accounts in [!INCLUDE[crm_md](includes/crm_md.md)] worden meestal gekoppeld aan klanten in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Records koppelen biedt de volgende voordelen:

* Het maakt synchronisatie mogelijk.
* Gebruikers kunnen in de ene zakelijke app de records van een andere openen. Hiervoor moet de [!INCLUDE[d365fin](includes/d365fin_md.md)]-integratieoplossing zijn geïnstalleerd in [!INCLUDE[crm_md](includes/crm_md.md)].

Koppelingen kunnen automatisch worden ingesteld met behulp van de synchronisatietaken of door de record handmatig te bewerken in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Zie [Gegevens synchroniseren in [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md) en [Records handmatig koppelen en synchroniseren](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings) voor meer informatie.

## <a name="filtering-records"></a>Records filteren  
Als u niet alle records voor een bepaalde [!INCLUDE[crm_md](includes/crm_md.md)]-entiteit of [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabel wilt synchroniseren, kunt u filters instellen om de records te beperken die worden gesynchroniseerd. U stelt filters in op de pagina **Toewijzingen van integratietabellen**.  

#### <a name="to-filter-records-for-synchronization"></a>Records filteren voor synchronisatie  
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Toewijzingen van integratietabellen** in en kies de desbetreffende koppeling.

2.  Als u de [!INCLUDE[d365fin](includes/d365fin_md.md)]-records wilt filteren, stelt u het veld **Tabelfilter** in.  

3.  Als u de [!INCLUDE[crm_md](includes/crm_md.md)]-records wilt filteren, stelt u het veld **Filter integratietabel** in.  

## <a name="creating-new-records"></a>Nieuwe records maken  
 Standaard worden alleen records in [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] die zijn gekoppeld, door de integratiesynchronisatietaken gesynchroniseerd. U kunt tabeltoewijzingen zo instellen dat nieuwe records worden gemaakt op de bestemming (bijvoorbeeld [!INCLUDE[d365fin](includes/d365fin_md.md)]) voor elke record in de bron (bijvoorbeeld [!INCLUDE[crm_md](includes/crm_md.md)]) die nog niet is gekoppeld.  

 De Dynamics 365 Sales-synchronisatietaak gebruikt bijvoorbeeld de tabeltoewijzing VERKOPERS. De synchronisatietaak kopieert gegevens uit gebruikersrecords in [!INCLUDE[crm_md](includes/crm_md.md)] naar verkopersrecords in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Als u de tabeltoewijzing instelt om nieuwe records te maken, wordt voor elke gebruiker in [!INCLUDE[crm_md](includes/crm_md.md)] die niet al is gekoppeld aan een verkoper in [!INCLUDE[d365fin](includes/d365fin_md.md)], een nieuwe verkopersrecord gemaakt in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-create-new-records-during-synchronization"></a>Nieuwe records maken tijdens synchronisatie  
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Toewijzingen van integratietabellen** in en kies de desbetreffende koppeling.

2.  Wis in het tabeltoewijzingsitem in de lijst het veld **Alleen gekoppelde records synchr.**.  

## <a name="using-configuration-templates-on-table-mappings"></a>Configuratiesjablonen gebruiken met tabeltoewijzingen
U kunt configuratiesjablonen aan tabeltoewijzingen toewijzen om te gebruiken voor nieuwe records die worden gemaakt in [!INCLUDE[d365fin](includes/d365fin_md.md)] of [!INCLUDE[crm_md](includes/crm_md.md)]. Voor elke tabeltoewijzing kunt u een configuratiesjabloon opgeven voor nieuwe [!INCLUDE[d365fin](includes/d365fin_md.md)]-records en een andere sjabloon om nieuwe [!INCLUDE[crm_md](includes/crm_md.md)]-records te gebruiken.  

Als u de standaardsynchronisatie-instelling installeert, worden meestal automatisch twee configuratiesjablonen gemaakt en gebruikt voor de tabeltoewijzing voor [!INCLUDE[d365fin](includes/d365fin_md.md)]-klanten en [!INCLUDE[crm_md](includes/crm_md.md)]-accounts: **CRMCUST** en **CRMACCOUNT**.  

-   **CRMCUST** wordt gebruikt om nieuwe klanten te maken en te synchroniseren in [!INCLUDE[d365fin](includes/d365fin_md.md)], op basis van een account in [!INCLUDE[crm_md](includes/crm_md.md)].  

     Deze sjabloon wordt gemaakt door een bestaande configuratiesjabloon te kopiëren voor klanten in de toepassing. **CRMCUST** wordt alleen gemaakt als er een bestaande configuratiesjabloon is en het veld **Valutacode** in de sjabloon leeg is. Als een veld in de configuratiesjabloon een waarde bevat, wordt die waarde gebruikt in plaats van de waarde in het toegewezen veld in het [!INCLUDE[crm_md](includes/crm_md.md)]-account. Bijvoorbeeld als het veld **Land/regio** in een [!INCLUDE[crm_md](includes/crm_md.md)]-account *VS* is en het veld **Land/regio** in de configuratiesjabloon *GB* is, wordt *GB* gebruikt als **Land/regio** voor de klant in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   **CRMACCOUNT** maakt en synchroniseert nieuwe accounts in [!INCLUDE[crm_md](includes/crm_md.md)] op basis van een account in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Configuratiesjablonen opgeven voor een tabeltoewijzing  
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Toewijzingen van integratietabellen** in en kies de desbetreffende koppeling.

2.  Kies in de tabeltoewijzingspost in de lijst in het veld **Sjablooncode voor tabelconfiguratie** de configuratiesjabloon die moet worden gebruikt voor nieuwe records in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

3.  Stel het veld **Sjablooncode voor int. tabelconfig.** in op de configuratiesjabloon die moet worden gebruikt voor nieuwe records in [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Zie ook  
[Over integratie van Dynamics 365 Business Central met Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Business Central en Dynamics 365 Sales synchroniseren](admin-synchronizing-business-central-and-sales.md)   
[Een synchronisatie plannen](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
