---
title: De te synchroniseren tabellen en velden toewijzen | Microsoft Docs
description: Hier vindt u informatie over het toewijzen van tabellen en velden voor de synchronisatie van gegevens tussen Business Central en Microsoft Dataverse.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 185d0a1c55830f6e4ed979154744076d457b5724
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6446402"
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a>De te synchroniseren tabellen en velden toewijzen
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

De basis voor de synchronisatie van gegevens is de toewijzing van de tabellen en velden in [!INCLUDE[prod_short](includes/prod_short.md)] aan tabellen en kolommen in [!INCLUDE[prod_short](includes/cds_long_md.md)], zodat de gegevens kunnen worden uitgewisseld. Toewijzing gebeurt via integratietabellen. 

## <a name="mapping-integration-tables"></a>Integratietabellen toewijzen
Een integratietabel is een tabel in de [!INCLUDE[prod_short](includes/prod_short.md)]-database die een tabel vertegenwoordigt, zoals een account, in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Integratietabellen bevatten velden die overeenkomen met kolommen in de tabel voor de [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabel. De tabel Accountintegratie maakt bijvoorbeeld verbinding met de tabel Accounts in [!INCLUDE[cds_short_md](includes/cds_long_md.md)]. Voor elke tabel in [!INCLUDE[cds_short_md](includes/cds_short_md.md)] die u wilt synchroniseren met gegevens in [!INCLUDE[prod_short](includes/prod_short.md)], moet er een integratietabeltoewijzing zijn.

Wanneer u de verbinding tussen de apps maakt, stelt [!INCLUDE[prod_short](includes/prod_short.md)] enkele standaardtoewijzingen in. U kunt desgewenst de tabeltoewijzingen wijzigen. Zie voor meer informatie [Standaardtoewijzing van tabel voor synchronisatie](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization). Als u de standaardtoewijzingen hebt gewijzigd en uw wijzigingen wilt terugdraaien, kiest u op de pagina **Toewijzingen van integratietabellen** **Standaardsynchronisatie-instellingen gebruiken**.

> [!Note]
> Als u een on-premises versie van [!INCLUDE[prod_short](includes/prod_short.md)] gebruikt, worden de integratietabeltoewijzingen opgeslagen in tabel 5335 Integratietabeltoewijzingen, waar u de toewijzingen kunt bekijken en bewerken. Complexe toewijzingen en synchronisatieregels worden gedefinieerd in codeunit 5341. 

### <a name="synchronization-rules"></a>Synchronisatieregels
Een integratietabeltoewijzing bevat ook regels die bepalen hoe integratie-synchronisatietaken records in een [!INCLUDE[prod_short](includes/prod_short.md)]-tabel en een tabel in [!INCLUDE[prod_short](includes/cds_long_md.md)] synchroniseren. <!--For examples of rules for an integration with Sales, see [Synchronization Rules](admin-synchronizing-business-central-and-sales.md#synchronization-rules). need to verify link -->

### <a name="strategies-for-auto-resolving-conflicts"></a>Strategieën voor het automatisch oplossen van conflicten
Gegevensconflicten kunnen gemakkelijk optreden wanneer bedrijfsapplicaties voortdurend gegevens uitwisselen. Iemand kan bijvoorbeeld een rij in een van de toepassingen of beide verwijderen of wijzigen. Om het aantal conflicten dat u handmatig moet oplossen te verminderen kunt u oplossingsstrategieën specificeren en [!INCLUDE[prod_short](includes/prod_short.md)] lost dan automatisch conflicten op volgens de regels in de strategieën.

Toewijzingen van integratietabellen bevatten regels die bepalen hoe synchronisatietaken records synchroniseren. Op de pagina **Toewijzing van integratietabel** in de kolommen **Verwijderingsconflicten oplossen** en **Updateconflicten oplossen** kunt u aangeven hoe [!INCLUDE[prod_short](includes/prod_short.md)] conflicten oplost die optreden omdat records zijn verwijderd in tabellen in de ene of de andere bedrijfstoepassing, of zijn bijgewerkt in beide. 

In de kolom **Verwijderingsconflicten oplossen** kunt u ervoor kiezen om [!INCLUDE[prod_short](includes/prod_short.md)] automatisch verwijderde records te laten herstellen, de koppeling tussen de records te laten verwijderen of niets doen. Als u niets doet, moet u de conflicten handmatig oplossen. 

In de kolom **Updateconflicten oplossen** kunt u ervoor kiezen om [!INCLUDE[prod_short](includes/prod_short.md)] automatisch een gegevensupdate naar de integratietabel te laten sturen wanneer gegevens worden verzonden naar [!INCLUDE[prod_short](includes/cds_long_md.md)] of om een gegevensupdate uit de integratietabel op te halen wanneer gegevens worden gehaald uit [!INCLUDE[prod_short](includes/cds_long_md.md)], of niets te doen. Als u niets doet, moet u de conflicten handmatig oplossen.

Nadat u de strategie hebt gespecificeerd, kunt u op de pagina **Synchronisatiefouten met gekoppelde gegevens** de actie **Alles opnieuw proberen** kiezen om conflicten automatisch op te lossen. 

## <a name="mapping-integration-fields"></a>Integratievelden toewijzen
Het toewijzen van tabellen is slechts de eerste stap. U moet ook de velden in de tabellen toewijzen. Integratieveldtoewijzingen koppelen velden in [!INCLUDE[prod_short](includes/prod_short.md)]-tabellen aan overeenkomstige kolommen in [!INCLUDE[prod_short](includes/cds_long_md.md)] en bepalen of gegevens in elke tabel moeten worden gesynchroniseerd. De standaardtabeltoewijzing die [!INCLUDE[prod_short](includes/prod_short.md)] biedt, bevat veldtoewijzingen, maar u kunt deze desgewenst wijzigen. Zie [Tabeltoewijzingen weergeven](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-table-mappings) voor meer informatie.

> [!Note]
> Als u een on-premises versie van [!INCLUDE[prod_short](includes/prod_short.md)] gebruikt, zijn integratieveldtoewijzingen gedefinieerd in tabel 5336 Integratieveldtoewijzing.

### <a name="handling-differences-in-field-values"></a>Omgaan met verschillen in veldwaarden
Soms verschillen de waarden in de velden die u wilt toewijzen. In [!INCLUDE[crm_md](includes/crm_md.md)] is de taalcode voor de Verenigde Staten bijvoorbeeld 'V.S.', maar in [!INCLUDE[prod_short](includes/prod_short.md)] is het 'VS'. Dat betekent dat u de waarde moet transformeren wanneer u gegevens synchroniseert. Dit gebeurt door middel van transformatieregels die u voor de velden definieert. U definieert transformatieregels op de pagina **Toewijzingen van integratietabellen** door **Toewijzing** te kiezen en vervolgens **Velden**. Er zijn vooraf gedefinieerde regels beschikbaar, maar u kunt ook uw eigen regels maken. Zie [Transformatieregels](across-how-to-set-up-data-exchange-definitions.md#transformation-rules) voor meer informatie.

### <a name="handling-missing-option-values-in-mapping"></a>Ontbrekende optiewaarden bij toewijzing verwerken
[!INCLUDE[prod_short](includes/cds_long_md.md)] bevat optiesetkolommen die waarden bieden die u kunt toewijzen aan [!INCLUDE[prod_short](includes/prod_short.md)]-velden van het type **Optie**, voor automatische synchronisatie. Tijdens synchronisatie worden niet-toegewezen opties genegeerd en worden de ontbrekende opties toegevoegd aan de gerelateerde [!INCLUDE[prod_short](includes/prod_short.md)]-tabel en toegevoegd aan de systeemtabel **Toewijzing van CDS-optie** om later handmatig af te handelen. Bijvoorbeeld door de ontbrekende opties in beide producten toe te voegen en vervolgens de toewijzing bij te werken. Zie voor meer informatie [Afhandeling van ontbrekende optiewaarden](admin-cds-missing-option-values.md).

## <a name="coupling-records"></a>Records koppelen
Koppeling koppelt rijen in [!INCLUDE[prod_short](includes/cds_long_md.md)] aan records in [!INCLUDE[prod_short](includes/prod_short.md)]. Bijvoorbeeld: accounts in [!INCLUDE[prod_short](includes/cds_long_md.md)] worden meestal gekoppeld aan klanten in [!INCLUDE[prod_short](includes/prod_short.md)]. Records koppelen biedt de volgende voordelen:

* Het maakt synchronisatie mogelijk.
* Gebruikers kunnen in de ene zakelijke app de records of rijen van een andere openen. Dit vereist dat de apps al zijn geïntegreerd.

Koppelingen kunnen automatisch worden ingesteld met behulp van de synchronisatietaken of door de record handmatig te bewerken in [!INCLUDE[prod_short](includes/prod_short.md)]. Zie [Gegevens synchroniseren in [!INCLUDE[prod_short](includes/prod_short.md)] en [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md) en [Records handmatig koppelen en synchroniseren](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings) voor meer informatie.

## <a name="filtering-records-and-rows"></a>Records en rijen filteren  
Als u niet alle rijen voor een bepaalde tabel in [!INCLUDE[prod_short](includes/cds_long_md.md)] of [!INCLUDE[prod_short](includes/prod_short.md)] wilt synchroniseren, kunt u filters instellen om de gegevens te beperken die worden gesynchroniseerd. U stelt filters in op de pagina **Toewijzingen van integratietabellen**.  

#### <a name="to-filter-records-or-rows-for-synchronization"></a>Records of rijen filteren voor synchronisatie  
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Toewijzingen van integratietabellen** in en kies vervolgens de gerelateerde koppeling.

2.  Als u de [!INCLUDE[prod_short](includes/prod_short.md)]-records wilt filteren, stelt u het veld **Tabelfilter** in.  

3.  Als u de [!INCLUDE[prod_short](includes/cds_long_md.md)]-rijen wilt filteren, stelt u het veld **Filter integratietabel** in.  

## <a name="creating-new-records"></a>Nieuwe records maken  
Standaard worden alleen records in [!INCLUDE[prod_short](includes/prod_short.md)] en rijen in [!INCLUDE[prod_short](includes/cds_long_md.md)] die zijn gekoppeld, door de integratiesynchronisatietaken gesynchroniseerd. U kunt tabeltoewijzingen zo instellen dat nieuwe records of rijen worden gemaakt op de bestemming (bijvoorbeeld [!INCLUDE[prod_short](includes/prod_short.md)]) voor elke rij in de bron (bijvoorbeeld [!INCLUDE[prod_short](includes/cds_long_md.md)]) die nog niet is gekoppeld.  

De Dynamics 365 Sales-synchronisatietaak gebruikt bijvoorbeeld de tabeltoewijzing VERKOPERS. De synchronisatietaak kopieert gegevens uit gebruikers in [!INCLUDE[prod_short](includes/cds_long_md.md)] naar verkopers in [!INCLUDE[prod_short](includes/prod_short.md)]. Als u de tabeltoewijzing instelt om nieuwe records te maken, wordt voor elke gebruiker in [!INCLUDE[prod_short](includes/cds_long_md.md)] die niet al is gekoppeld aan een verkoper in [!INCLUDE[prod_short](includes/prod_short.md)], een nieuwe verkopersrij gemaakt in [!INCLUDE[prod_short](includes/prod_short.md)].  

#### <a name="to-create-new-records-during-synchronization"></a>Nieuwe records maken tijdens synchronisatie  
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Toewijzingen van integratietabellen** in en kies vervolgens de gerelateerde koppeling.

2.  Wis in het tabeltoewijzingsitem in de lijst het veld **Alleen gekoppelde records synchr.**.  

## <a name="using-configuration-templates-on-table-mappings"></a>Configuratiesjablonen gebruiken met tabeltoewijzingen
U kunt configuratiesjablonen aan tabeltoewijzingen toewijzen om te gebruiken voor nieuwe records of rijen die worden gemaakt in [!INCLUDE[prod_short](includes/prod_short.md)] of [!INCLUDE[prod_short](includes/cds_long_md.md)]. Voor elke tabeltoewijzing kunt u een configuratiesjabloon opgeven voor nieuwe [!INCLUDE[prod_short](includes/prod_short.md)]-records en een andere sjabloon om nieuwe [!INCLUDE[prod_short](includes/cds_long_md.md)]-rijen te gebruiken.  

Als u de standaardsynchronisatie-instelling installeert, worden meestal automatisch twee configuratiesjablonen gemaakt en gebruikt voor de tabeltoewijzing voor [!INCLUDE[prod_short](includes/prod_short.md)]-klanten en [!INCLUDE[crm_md](includes/crm_md.md)]-accounts: **CDSKLANT** en **CDSACCOUNT**.  

-   **CDSKLANT** wordt gebruikt om nieuwe klanten te maken en te synchroniseren in [!INCLUDE[prod_short](includes/prod_short.md)], op basis van een account in [!INCLUDE[crm_md](includes/crm_md.md)].  

     Deze sjabloon wordt gemaakt door een bestaande configuratiesjabloon te kopiëren voor klanten in de toepassing. **CDSKLANT** wordt alleen gemaakt als er een bestaande configuratiesjabloon is en het veld **Valutacode** in de sjabloon leeg is. Als een veld in de configuratiesjabloon een waarde bevat, wordt die waarde gebruikt in plaats van de waarde in de toegewezen kolom in het [!INCLUDE[prod_short](includes/cds_long_md.md)]-account. Bijvoorbeeld als de kolom **Land/regio** in een [!INCLUDE[prod_short](includes/cds_long_md.md)]-account *VS* is en het veld **Land/regio** in de configuratiesjabloon *GB* is, wordt *GB* gebruikt als **Land/regio** voor de klant in [!INCLUDE[prod_short](includes/prod_short.md)].  

-   **CDSACCOUNT** maakt en synchroniseert nieuwe accounts in [!INCLUDE[prod_short](includes/cds_long_md.md)] op basis van een account in [!INCLUDE[prod_short](includes/prod_short.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Configuratiesjablonen opgeven voor een tabeltoewijzing  
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Toewijzingen van integratietabellen** in en kies vervolgens de gerelateerde koppeling.

2.  Kies in de tabeltoewijzingspost in de lijst in het veld **Sjablooncode voor tabelconfiguratie** de configuratiesjabloon die moet worden gebruikt voor nieuwe records in [!INCLUDE[prod_short](includes/prod_short.md)].  

3.  Stel het veld **Sjablooncode voor int. tabelconfig.** in op de configuratiesjabloon die moet worden gebruikt voor nieuwe records in [!INCLUDE[prod_short](includes/cds_long_md.md)].

## <a name="see-also"></a>Zie ook  
[Over integratie van Dynamics 365 Business Central met [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Gegevens synchroniseren in Business Central en [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)   
[Een synchronisatie plannen](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]