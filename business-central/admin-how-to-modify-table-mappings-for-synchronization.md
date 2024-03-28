---
title: De te synchroniseren tabellen en velden toewijzen
description: Hier vindt u informatie over het toewijzen van tabellen en velden voor de synchronisatie van gegevens tussen Business Central en Microsoft Dataverse.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 03/31/2023
ms.custom: bap-template
ms.search.keywords: 'sales, crm, integration, sync, synchronize, table mapping'
ms.service: dynamics-365-business-central
---
# De te synchroniseren tabellen en velden toewijzen

De basis voor de synchronisatie van gegevens is de toewijzing van de tabellen en velden in [!INCLUDE[prod_short](includes/prod_short.md)] aan tabellen en kolommen in [!INCLUDE[prod_short](includes/cds_long_md.md)], zodat de gegevens kunnen worden uitgewisseld. Toewijzing gebeurt via integratietabellen.

## Integratietabellen in kaart brengen

Een integratietabel is een tabel in de [!INCLUDE[prod_short](includes/prod_short.md)]-database die een tabel vertegenwoordigt, zoals een account, in [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Integratietabellen bevatten velden die overeenkomen met kolommen in de tabel voor de [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-tabel. De tabel Accountintegratie maakt bijvoorbeeld verbinding met de tabel Accounts in [!INCLUDE[cds_short_md](includes/cds_long_md.md)]. Voor elke tabel in [!INCLUDE[cds_short_md](includes/cds_short_md.md)] die u wilt synchroniseren met gegevens in [!INCLUDE[prod_short](includes/prod_short.md)], moet er een integratietabeltoewijzing zijn.

Wanneer u de verbinding tussen de apps maakt, stelt [!INCLUDE[prod_short](includes/prod_short.md)] enkele standaardtoewijzingen in. U kunt desgewenst de tabeltoewijzingen wijzigen. Zie voor meer informatie [Standaardtoewijzing van tabel voor synchronisatie](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization). Als u de standaardtoewijzingen hebt gewijzigd en uw wijzigingen wilt terugdraaien, kiest u op de pagina **Toewijzingen van integratietabellen** **Standaardsynchronisatie-instellingen gebruiken**.

> [!Note]
> Als u een on-premises versie van [!INCLUDE[prod_short](includes/prod_short.md)] gebruikt, worden de integratietabeltoewijzingen opgeslagen in tabel 5335 Integratietabeltoewijzingen, waar u de toewijzingen kunt bekijken en bewerken. Complexe toewijzingen en synchronisatieregels worden gedefinieerd in codeunit 5341.

> [!TIP]
> Wanneer een gekoppeld record verandert, synchroniseert [!INCLUDE [prod_short](includes/prod_short.md)] de gegevens automatisch met Dataverse. Automatische synchronisatie is in de meeste gevallen geweldig. Frequente wijzigingen in grote hoeveelheden gekoppelde records in een tabel kunnen de gegevenssynchronisatie echter vertragen.
>
> Om trage prestaties te voorkomen, kunt u op de pagina **Toewijzingen van integratietabellen** gebeurtenisgebaseerde gegevenssynchronisatie voor elke tabel in- of uitschakelen. Op gebeurtenissen gebaseerde synchronisatie is standaard ingeschakeld, zodat bestaande integraties niet worden beïnvloed. Uw beheerder kan het voor specifieke tabellen in- of uitschakelen.

### Aanvullende toewijzingen

Betalingscondities, verzendmethoden en expediteurs kunnen veranderen en het kan belangrijk zijn om deze aan te kunnen passen. Als u de functie **Functie-update: zonder code aan optiesets toewijzen in Dataverse** inschakelt op de pagina [Functiebeheer](https://businesscentral.dynamics.com/?page=2610), kunt u handmatig integratietabeltoewijzingen toevoegen voor betalingsvoorwaarden (BETALINGSVOORWAARDEN), verzendmethoden (VERZENDMETHODE) en expediteurs (EXPEDITEUR). Deze toewijzing kan ervoor zorgen dat uw beleid hetzelfde is voor deze instellingen in [!INCLUDE[prod_short](includes/cds_long_md.md)] en [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

### Synchronisatieregels

Een integratietabeltoewijzing bevat ook regels die bepalen hoe integratie-synchronisatietaken records in een [!INCLUDE[prod_short](includes/prod_short.md)]-tabel en een tabel in [!INCLUDE[prod_short](includes/cds_long_md.md)] synchroniseren. Ga voor voorbeelden van regels voor een integratie met Sales naar [Synchronisatieregels](#synchronization-rules).

### Strategieën voor het automatisch oplossen van conflicten

Gegevensconflicten kunnen gemakkelijk optreden wanneer bedrijfsapplicaties voortdurend gegevens uitwisselen. Iemand kan bijvoorbeeld een rij in een van de toepassingen of beide verwijderen of wijzigen. Om het aantal conflicten dat u handmatig moet oplossen te verminderen kunt u oplossingsstrategieën specificeren en [!INCLUDE[prod_short](includes/prod_short.md)] lost dan automatisch conflicten op volgens de regels in de strategieën.

Toewijzingen van integratietabellen bevatten regels die bepalen hoe synchronisatietaken records synchroniseren. Op de pagina **Toewijzing van integratietabel** in de kolommen **Verwijderingsconflicten oplossen** en **Updateconflicten oplossen** kunt u aangeven hoe [!INCLUDE[prod_short](includes/prod_short.md)] conflicten oplost die optreden omdat records zijn verwijderd in tabellen in de ene of de andere bedrijfstoepassing, of zijn bijgewerkt in beide. 

In de kolom **Verwijderingsconflicten oplossen** kunt u ervoor kiezen om [!INCLUDE[prod_short](includes/prod_short.md)] automatisch verwijderde records te laten herstellen, de koppeling tussen de records te laten verwijderen of niets doen. Als u niets doet, moet u de conflicten handmatig oplossen. 

In de kolom **Updateconflicten oplossen** kunt u ervoor kiezen om [!INCLUDE[prod_short](includes/prod_short.md)] automatisch een gegevensupdate naar de integratietabel te laten sturen wanneer gegevens worden verzonden naar [!INCLUDE[prod_short](includes/cds_long_md.md)] of om een gegevensupdate uit de integratietabel op te halen wanneer gegevens worden gehaald uit [!INCLUDE[prod_short](includes/cds_long_md.md)], of niets te doen. Als u niets doet, moet u de conflicten handmatig oplossen.

Nadat u de strategie hebt gespecificeerd, kunt u op de pagina **Synchronisatiefouten met gekoppelde gegevens** de actie **Alles opnieuw proberen** kiezen om conflicten automatisch op te lossen.

## Integratievelden toewijzen

Het toewijzen van tabellen is slechts de eerste stap. U moet ook de velden in de tabellen toewijzen. Integratieveldtoewijzingen koppelen velden in [!INCLUDE[prod_short](includes/prod_short.md)]-tabellen aan overeenkomstige kolommen in [!INCLUDE[prod_short](includes/cds_long_md.md)] en bepalen of gegevens in elke tabel moeten worden gesynchroniseerd. De standaardtabeltoewijzing die [!INCLUDE[prod_short](includes/prod_short.md)] biedt, bevat veldtoewijzingen, maar u kunt deze desgewenst wijzigen. Zie [Tabeltoewijzingen weergeven](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-table-mappings) voor meer informatie.

> [!Note]
> Als u een on-premises versie van [!INCLUDE[prod_short](includes/prod_short.md)] gebruikt, zijn integratieveldtoewijzingen gedefinieerd in tabel 5336 Integratieveldtoewijzing.

U kunt de velden handmatig toewijzen of u kunt het proces automatiseren door meerdere velden tegelijk toe te wijzen op basis van criteria voor het afstemmen van hun waarden. Voor meer informatie zie [Meerdere records koppelen op basis van veldwaardeovereenkomst](admin-how-to-couple-and-synchronize-records-manually.md).

### Omgaan met verschillen in veldwaarden

Soms verschillen de waarden in de velden die u wilt toewijzen. In [!INCLUDE[crm_md](includes/crm_md.md)] is de taalcode voor de Verenigde Staten bijvoorbeeld 'V.S.', maar in [!INCLUDE[prod_short](includes/prod_short.md)] is het 'VS'. Dat betekent dat u de waarde moet transformeren wanneer u gegevens synchroniseert. Dit gebeurt door middel van transformatieregels die u voor de velden definieert. U definieert transformatieregels op de pagina **Toewijzingen van integratietabellen** door **Toewijzing** te kiezen en vervolgens **Velden**. Er zijn vooraf gedefinieerde regels beschikbaar, maar u kunt ook uw eigen regels maken. Zie [Transformatieregels](across-how-to-set-up-data-exchange-definitions.md#transformation-rules) voor meer informatie.

### Ontbrekende optiewaarden verwerken

[!INCLUDE[prod_short](includes/cds_long_md.md)] bevat optiesetkolommen die waarden bieden die u kunt toewijzen aan [!INCLUDE[prod_short](includes/prod_short.md)]-velden van het type **Optie**, voor automatische synchronisatie. Tijdens synchronisatie worden niet-toegewezen opties genegeerd en worden de ontbrekende opties toegevoegd aan de gerelateerde [!INCLUDE[prod_short](includes/prod_short.md)]-tabel en toegevoegd aan de systeemtabel **Toewijzing van CDS-optie** om later handmatig af te handelen. Bijvoorbeeld door de ontbrekende opties in beide producten toe te voegen en vervolgens de toewijzing bij te werken. Zie voor meer informatie [Afhandeling van ontbrekende optiewaarden](admin-cds-missing-option-values.md).

## Koppelrecords

Koppeling koppelt rijen in [!INCLUDE[prod_short](includes/cds_long_md.md)] aan records in [!INCLUDE[prod_short](includes/prod_short.md)]. Bijvoorbeeld: accounts in [!INCLUDE[prod_short](includes/cds_long_md.md)] worden meestal gekoppeld aan klanten in [!INCLUDE[prod_short](includes/prod_short.md)]. Records koppelen biedt de volgende voordelen:

* Het maakt synchronisatie mogelijk.
* Gebruikers kunnen in de ene zakelijke app de records of rijen van een andere openen. Dit vereist dat de apps al zijn geïntegreerd.

Koppelingen kunnen automatisch worden ingesteld met behulp van de synchronisatietaken of door de record handmatig te bewerken in [!INCLUDE[prod_short](includes/prod_short.md)]. Zie [Gegevens synchroniseren in [!INCLUDE[prod_short](includes/prod_short.md)] en [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md) en [Records handmatig koppelen en synchroniseren](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings) voor meer informatie.

## Records en rijen filteren  

Als u niet alle rijen voor een bepaalde tabel in [!INCLUDE[prod_short](includes/cds_long_md.md)] of [!INCLUDE[prod_short](includes/prod_short.md)] wilt synchroniseren, kunt u filters instellen om de gegevens te beperken die worden gesynchroniseerd. U stelt filters in op de pagina **Toewijzingen van integratietabellen**.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Toewijzingen van integratietabellen** in en kies vervolgens de gerelateerde koppeling.
2. Als u de [!INCLUDE[prod_short](includes/prod_short.md)]-records wilt filteren, stelt u het veld **Tabelfilter** in.  
3. Als u de [!INCLUDE[prod_short](includes/cds_long_md.md)]-rijen wilt filteren, stelt u het veld **Filter integratietabel** in.  

## Nieuwe records maken  

Standaard worden alleen records in [!INCLUDE[prod_short](includes/prod_short.md)] en rijen in [!INCLUDE[prod_short](includes/cds_long_md.md)] die zijn gekoppeld, door de integratiesynchronisatietaken gesynchroniseerd. U kunt tabeltoewijzingen zo instellen dat nieuwe records of rijen worden gemaakt op de bestemming (bijvoorbeeld [!INCLUDE[prod_short](includes/prod_short.md)]) voor elke rij in de bron (bijvoorbeeld [!INCLUDE[prod_short](includes/cds_long_md.md)]) die nog niet is gekoppeld.  

De Dynamics 365 Sales-synchronisatietaak gebruikt bijvoorbeeld de tabeltoewijzing VERKOPERS. De synchronisatietaak kopieert gegevens uit gebruikers in [!INCLUDE[prod_short](includes/cds_long_md.md)] naar verkopers in [!INCLUDE[prod_short](includes/prod_short.md)]. Als u de tabeltoewijzing instelt om nieuwe records te maken, wordt voor elke gebruiker in [!INCLUDE[prod_short](includes/cds_long_md.md)] die niet al is gekoppeld aan een verkoper in [!INCLUDE[prod_short](includes/prod_short.md)], een nieuwe verkopersrij gemaakt in [!INCLUDE[prod_short](includes/prod_short.md)].  

### Nieuwe records maken tijdens synchronisatie  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Toewijzingen van integratietabellen** in en kies vervolgens de gerelateerde koppeling.
2. Wis in het tabeltoewijzingsitem in de lijst het veld **Alleen gekoppelde records synchr.**.  

## Configuratiesjablonen gebruiken met tabeltoewijzingen

U kunt configuratiesjablonen aan tabeltoewijzingen toewijzen om te gebruiken voor nieuwe records of rijen die worden gemaakt in [!INCLUDE[prod_short](includes/prod_short.md)] of [!INCLUDE[prod_short](includes/cds_long_md.md)]. Voor elke tabeltoewijzing kunt u een configuratiesjabloon opgeven voor nieuwe [!INCLUDE[prod_short](includes/prod_short.md)]-records en een andere sjabloon om nieuwe [!INCLUDE[prod_short](includes/cds_long_md.md)]-rijen te gebruiken.  

Als u de standaardsynchronisatie-instelling installeert, worden meestal automatisch twee configuratiesjablonen gemaakt en gebruikt voor de tabeltoewijzing voor [!INCLUDE[prod_short](includes/prod_short.md)]-klanten en [!INCLUDE[crm_md](includes/crm_md.md)]-accounts: **CDSKLANT** en **CDSACCOUNT**.  

* **CDSCUST** maakt en synchroniseert nieuwe klanten in [!INCLUDE[prod_short](includes/prod_short.md)] op basis van accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  

     Maak deze sjabloon door een bestaande configuratiesjabloon voor klanten te kopiëren. **CDSKLANT** wordt alleen gemaakt als er een bestaande configuratiesjabloon is en het veld **Valutacode** in de sjabloon leeg is. Als een veld in de configuratiesjabloon een waarde bevat, wordt die waarde gebruikt in plaats van de waarde in de toegewezen kolom in het [!INCLUDE[prod_short](includes/cds_long_md.md)]-account. Bijvoorbeeld als de kolom **Land/regio** in een [!INCLUDE[prod_short](includes/cds_long_md.md)]-account *VS* is en het veld **Land/regio** in de configuratiesjabloon **GB** is, wordt **GB** gebruikt als **Land/regio** voor de klant in [!INCLUDE[prod_short](includes/prod_short.md)].  

* **CDSACCOUNT** maakt en synchroniseert nieuwe accounts in [!INCLUDE[prod_short](includes/cds_long_md.md)] op basis van een account in [!INCLUDE[prod_short](includes/prod_short.md)].  

### Configuratiesjablonen opgeven voor een tabeltoewijzing  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Toewijzingen van integratietabellen** in en kies vervolgens de gerelateerde koppeling.
2. Kies in de tabeltoewijzingspost in de lijst in het veld **Sjablooncode voor tabelconfiguratie** de configuratiesjabloon die moet worden gebruikt voor nieuwe records in [!INCLUDE[prod_short](includes/prod_short.md)].  
3. Stel het veld **Sjablooncode voor int. tabelconfig.** in op de configuratiesjabloon die moet worden gebruikt voor nieuwe records in [!INCLUDE[prod_short](includes/cds_long_md.md)].

## Zie ook  

[Over integratie van Dynamics 365 Business Central met [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md )  
[Gegevens synchroniseren in Business Central en [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Een synchronisatie plannen](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]