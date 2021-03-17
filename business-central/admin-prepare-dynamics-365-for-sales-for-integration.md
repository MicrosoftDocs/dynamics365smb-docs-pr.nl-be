---
title: Integratie met Dynamics 365 Sales | Microsoft Docs
description: Leren hoe u Dynamics 365 Business Central voorbereidt op integratie met Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 02633c21025fe13b3cb781d8750d7c839640289c
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385386"
---
# <a name="integrating-with-dynamics-365-sales"></a>Integreren met Dynamics 365 Sales
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

De functie van verkoper wordt vaak beschouwd als een van de meest naar buiten gerichte taken in een bedrijf. Het kan voor verkopers echter handig zijn in het bedrijf te kunnen kijken en te zien wat er bij de backend gebeurt. Door [!INCLUDE[prod_short](includes/prod_short.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] te integreren kunt u uw verkopers dat inzicht geven door ze informatie in [!INCLUDE[prod_short](includes/prod_short.md)] te laten zien terwijl ze werken in [!INCLUDE[crm_md](includes/crm_md.md)]. Bijvoorbeeld, tijdens het voorbereiden van een verkoopofferte kan het handig zijn om te weten of u voldoende voorraad hebt om de order te kunnen vervullen. Zie voor meer informatie [Dynamics 365 Sales gebruiken vanuit Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Dit onderwerp beschrijft de integratie van de online versies van [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[prod_short](includes/prod_short.md)] via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Zie voor informatie over on-premises configuratie [Dynamics 365 Sales voorbereiden voor on-premises integratie](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## <a name="integrating-through-dataverse"></a>Integreren via Dataverse
[!INCLUDE[prod_short](includes/prod_short.md)] integreert ook met [!INCLUDE[prod_short](includes/cds_long_md.md)], waardoor het eenvoudig is om gegevens te verbinden en te synchroniseren met andere Dynamics 365-toepassingen, zoals [!INCLUDE[crm_md](includes/crm_md.md)], of zelfs apps die u zelf bouwt. Als u voor de eerste keer integreert, raden we u aan dit te doen via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Zie voor meer informatie [Integratie met Dataverse](admin-common-data-service.md).

Als u al [!INCLUDE[crm_md](includes/crm_md.md)] hebt geïntegreerd met [!INCLUDE[prod_short](includes/prod_short.md)], kunt u gegevens blijven synchroniseren met uw setup. Als u echter een upgrade uitvoert of uw [!INCLUDE[crm_md](includes/crm_md.md)]-integratie uitschakelt, moet u om het weer in te schakelen verbinding maken via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Zie voor meer informatie [Een integratie upgraden met Dynamics 365 Sales](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> Opnieuw verbinding maken via [!INCLUDE[prod_short](includes/cds_long_md.md)] past standaard synchronisatie-instellingen toe en overschrijft alle configuraties die u hebt. Zo worden de standaardtabeltoewijzingen toegepast.

## <a name="integration-settings-that-are-specific-to-a-crm_md-integration"></a>Integratie-instellingen die specifiek zijn voor een [!INCLUDE[crm_md](includes/crm_md.md)]-integratie
Integratie met [!INCLUDE[prod_short](includes/prod_short.md)] gebeurt door [!INCLUDE[prod_short](includes/cds_long_md.md)] en er zijn veel standaardinstellingen en tabellen die door de integratie worden geleverd. Naast de standaardinstellingen zijn er enkele die specifiek zijn voor [!INCLUDE[crm_md](includes/crm_md.md)]. In de volgende secties worden die vermeld.

## <a name="permissions-and-security-roles-for-user-accounts-in-sales"></a>Machtigingen en beveiligingsrollen voor gebruikersaccounts in Sales
Wanneer u de integratieoplossing installeert, worden machtigingen voor het integratiegebruikersaccount geconfigureerd. Als deze machtigingen zijn gewijzigd, moet u deze mogelijk opnieuw instellen. U kunt dat doen door de integratieoplossing opnieuw te installeren door te kiezen voor **Integratieoplossing opnieuw implementeren** op de pagina **Dynamics 365-verbinding instellen**. De volgende beveiligingsrollen worden ingezet:

* Dynamics 365 Business Central-integratiebeheerder
* Dynamics 365 Business Central-integratiegebruiker
* Dynamics 365 Business Central-gebruiker van productbeschikbaarheid

### <a name="connection-settings-in-the-setup-guide"></a>Verbindingsinstellingen in de installatiehandleiding

U kunt een begeleide instelling gebruiken om snel de verbinding in te stellen en geavanceerde functies op te geven, zoals koppeling tussen records.

1. Kies **Instellingen en extensies** en kies vervolgens **Begeleide instelling**.
2. Kies **Dynamics 365 Sales-verbinding instellen** om de begeleide instelling te starten.
3. Vul de velden in.
4. Eventueel zijn er geavanceerde instellingen die beveiliging kunnen vergroten en aanvullende mogelijkheden inschakelen, zoals verwerking van verkooporders en weergave van voorraadniveaus. De volgende tabel beschrijft de geavanceerde instellingen.  

| Veld | Omschrijving |
|--|--|
| **Dynamics 365 Sales-oplossing importeren** | Schakel dit in om de integratieoplossing te installeren en configureren in [!INCLUDE[crm_md](includes/crm_md.md)]. <!--For more information, see [About the Base CDS Integration Solution](admin-common-data-service.md#about-the-business-central-integration-solution). Need to add a new topic--> |
| **Webservice Artikelbeschikbaarheid publiceren** | Zorg dat personen die [!INCLUDE[crm_md](includes/crm_md.md)] gebruiken de beschikbaarheid van producten (artikelen) in voorraad in [!INCLUDE[prod_short](includes/prod_short.md)] kunnen bekijken. Dit vereist een [!INCLUDE[prod_short](includes/prod_short.md)]-gebruikersaccount met een webservicetoegangssleutel. De sleutel toewijzen is een proces van twee stappen. In het gebruikersaccount in [!INCLUDE[prod_short](includes/prod_short.md)] moet u de actie **Sleutel van webservice wijzigen** kiezen. In de begeleide instelling Dynamics 365 Sales-verbinding instellen moet u de URL van de Dynamics 365 Business Central OData-webservice opgeven en [!INCLUDE[prod_short](includes/prod_short.md)]-gebruikersreferenties opgeven voor toegang tot de service. Zie voor meer informatie [OData-webservices](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). |
| **URL van Business Central OData-webservice** | Als u de webservice voor het weergeven van artikelbeschikbaarheid inschakelt, wordt de URL van de OData-webservice voor u verschaft. |
| **Gebruikersnaam van Business Central OData-webservice** | De naam van het [!INCLUDE[prod_short](includes/prod_short.md)]-gebruikersaccount dat [!INCLUDE[crm_md](includes/crm_md.md)] gebruikt om informatie over artikelbeschikbaarheid in [!INCLUDE[prod_short](includes/prod_short.md)] op te halen met de OData-webservice. |
| **Toegangssleutel van Business Central OData-webservice** | De toegangssleutel voor het gebruikersaccount dat [!INCLUDE[crm_md](includes/crm_md.md)] gebruikt om informatie over artikelbeschikbaarheid uit [!INCLUDE[prod_short](includes/prod_short.md)] op te halen met de OData-webservice. De sleutel wordt toegewezen aan de gebruiker die is gekozen in het veld **Gebruikersnaam van Business Central OData-webservice**. Als u de sleutel wilt krijgen, kiest u de knop **Opzoekwaarde** naast de gebruikersnaam, kiest u de gebruiker, kiest u **Beheren** en klikt u vervolgens op **Bewerken**. Kies op de gebruikerskaart **Acties**, **Verificatie** en kies vervolgens **Sleutel van webservice wijzigen** |
| **Integratie van verkooporders inschakelen** | Wanneer mensen verkooporders maken in [!INCLUDE[crm_md](includes/crm_md.md)] en bestellingen uitvoeren in [!INCLUDE[prod_short](includes/prod_short.md)], integreert dit het proces in [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie [Integratie van verkooporderverwerking inschakelen](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). Hiervoor moet u referenties opgeven voor een beheerdersaccount in [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie het gedeelte [Verkoopordergegevens verwerken](marketing-integrate-dynamicscrm.md#handling-sales-order-data). |
| **CDS-verbinding inschakelen** | De verbinding met [!INCLUDE[prod_short](includes/cds_long_md.md)] inschakelen. |
| **Dynamics 365 SDK-versie** | Dit is alleen relevant als u integreert met een on-premises versie van [!INCLUDE[crm_md](includes/crm_md.md)]. Dit is de software-ontwikkelingskit van Dynamics 365 (ook Xrm genoemd) die u gebruikt om [!INCLUDE[prod_short](includes/prod_short.md)] te verbinden met [!INCLUDE[crm_md](includes/crm_md.md)]. De versie moet compatibel zijn met de SDK-versie die wordt gebruikt door [!INCLUDE[crm_md](includes/crm_md.md)] en gelijk zijn aan of nieuwer zijn dan de versie die wordt gebruikt door [!INCLUDE[crm_md](includes/crm_md.md)]. |

### <a name="connection-settings-on-the-microsoft-dynamics-365-connection-setup-page"></a>Verbindingsinstellingen op de pagina Microsoft Dynamics 365-verbinding instellen

Voer de volgende gegevens in voor de verbinding van [!INCLUDE[crm_md](includes/crm_md.md)] met [!INCLUDE[prod_short](includes/prod_short.md)].

| Veld | Omschrijving |
|--|--|
| **Dynamics 365 Sales-URL** | De URL van uw [!INCLUDE[crm_md](includes/crm_md.md)]-exemplaar. Hierdoor kunnen gebruikers in [!INCLUDE[prod_short](includes/prod_short.md)] bijbehorende records openen vanuit records in [!INCLUDE[crm_md](includes/crm_md.md)], zoals een account of product. De [!INCLUDE[prod_short](includes/prod_short.md)]-records worden geopend in [!INCLUDE[prod_short](includes/prod_short.md)]. |
|**Dynamics 365 Sales-URL**|De URL van uw [!INCLUDE[crm_md](includes/crm_md.md)]-exemplaar. Hierdoor kunnen gebruikers in [!INCLUDE[prod_short](includes/prod_short.md)] bijbehorende records openen vanuit records in [!INCLUDE[crm_md](includes/crm_md.md)], zoals een account of product. De [!INCLUDE[prod_short](includes/prod_short.md)]-records worden geopend in [!INCLUDE[prod_short](includes/prod_short.md)].|
|**Webservice Artikelbeschikbaarheid ingeschakeld**|Zorg dat personen die [!INCLUDE[crm_md](includes/crm_md.md)] gebruiken de beschikbaarheid van producten (artikelen) in voorraad in [!INCLUDE[prod_short](includes/prod_short.md)] kunnen bekijken. Als u dit inschakelt, moet u ook een gebruikersnaam en een toegangssleutel opgeven die de [!INCLUDE[crm_md](includes/crm_md.md)] moet gebruiken om bij de OData webservice te vragen naar beschikbaarheid van (artikelen). Zie voor meer informatie [OData-webservices](/dynamics365/business-central/dev-itpro/webservices/odata-web-services).|
|**URL van Dynamics 365 Business Central OData-webservice**|Als u de webservice Artikelbeschikbaarheid inschakelt, wordt de URL van de OData-webservice voor u verschaft. Stel dit veld in op de URL van het te gebruiken [!INCLUDE[prod_short](includes/prod_short.md)]-exemplaar.<br /><br /> Als u het veld opnieuw wilt instellen op de standaard-URL voor de [!INCLUDE[prod_short](includes/prod_short.md)], kiest u de actie **Webclient-URL opnieuw instellen**.<br /><br /> Dit veld is alleen van belang als de [!INCLUDE[prod_short](includes/prod_short.md)]-integratieoplossing is geïnstalleerd in [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Gebruikersnaam van Dynamics 365 Business Central OData-webservice**|De naam van het gebruikersaccount dat de [!INCLUDE[crm_md](includes/crm_md.md)] gebruikt om informatie over artikelbeschikbaarheid in [!INCLUDE[prod_short](includes/prod_short.md)] op te halen met de OData-webservice.|
|**Toegangssleutel van Dynamics 365 Business Central OData-webservice**|De toegangssleutel voor het gebruikersaccount dat de [!INCLUDE[crm_md](includes/crm_md.md)] gebruikt om informatie over artikelbeschikbaarheid uit [!INCLUDE[prod_short](includes/prod_short.md)] op te halen met de OData-webservice. De sleutel wordt toegewezen aan de gebruiker die is gekozen in het veld **Gebruikersnaam van Dynamics 365 Business Central OData-webservice**. Als u de sleutel wilt krijgen, kiest u de knop **Opzoekwaarde** naast de gebruikersnaam, kiest u de gebruiker, kiest u **Beheren** en klikt u vervolgens op **Bewerken**. Kies op de gebruikerskaart **Acties**, **Verificatie** en kies vervolgens **Sleutel van webservice wijzigen**|
|**Dynamics 365 SDK-versie**|Als u integreert met een on-premises versie van [!INCLUDE[crm_md](includes/crm_md.md)], is dit de Dynamics 365-softwareontwikkelingskit (ook Xrm genoemd) die u gebruikt om [!INCLUDE[prod_short](includes/prod_short.md)] te verbinden met [!INCLUDE[crm_md](includes/crm_md.md)]. De versie die u selecteert moet compatibel zijn met de SDK-versie die wordt gebruikt door [!INCLUDE[crm_md](includes/crm_md.md)]. Deze versie is gelijk aan of nieuwer dan de versie die wordt gebruikt door [!INCLUDE[crm_md](includes/crm_md.md)].|-->

Voer naast de bovenstaande instellingen de volgende instellingen in voor [!INCLUDE[crm_md](includes/crm_md.md)].

| Veld | Omschrijving |
|--|--|
| **Verkooporderintegratie is ingeschakeld** | Gebruikers de mogelijkheid bieden verkooporders en geactiveerde offertes in te dienen in [!INCLUDE[crm_md](includes/crm_md.md)] deze vervolgens weer te geven en te verwerken in [!INCLUDE[prod_short](includes/prod_short.md)]. Dit integreert het proces in [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie [Integratie van verkooporderverwerking inschakelen](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). |
| **Automatisch verkooporders maken** | Maak een verkooporder in [!INCLUDE[prod_short](includes/prod_short.md)] wanneer een gebruiker er een maakt en indient in [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Verkoopoffertes automatisch verwerken** | Verwerk een verkoopofferte in [!INCLUDE[prod_short](includes/prod_short.md)] als een gebruiker er een maakt en activeert in [!INCLUDE[crm_md](includes/crm_md.md)]. |

<!--
### User Account Settings
Integration with Business Central through Dataverse requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->

### <a name="standard-sales-entity-mapping-for-synchronization"></a>Standaardtoewijzing van Sales-entiteit voor synchronisatie

Entiteiten in [!INCLUDE[crm_md](includes/crm_md.md)], zoals orders, zijn geïntegreerd met equivalente soorten tabellen in [!INCLUDE[prod_short](includes/prod_short.md)], zoals verkooporders. Als u wilt werken met [!INCLUDE[crm_md](includes/crm_md.md)]-gegevens, stelt u koppelingen in tussen tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] en [!INCLUDE[crm_md](includes/crm_md.md)].

In de volgende tabel staat de standaardtoewijzing tussen tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] die [!INCLUDE[prod_short](includes/prod_short.md)] biedt.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[crm_md](includes/crm_md.md)] | Synchronisatierichting | Standaardfilter |
|--|--|--|--|
| Maateenheid | Eenhedengroep | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Artikel | Product | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Sales-contactfilter: **Producttype** is **Verkoopvoorraad** |
| Bron | Product | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Sales-contactfilter: **Producttype** is **Services** |
| Klantenprijsgroep | Prijslijst | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Verkoopprijs | Productprijslijst | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[prod_short](includes/prod_short.md)]-contactfilter: **Verkoopcode** is niet leeg, **Verkoopsoort** is **Klantenprijsgroep** |
| Opportunity | Opportunity | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |
| Verkoopfactuur | Factureren | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Verkoopfactuurregel | Factuurproduct | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Verkooporderkop | Verkooporder | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[prod_short](includes/prod_short.md)]-verkoopkopfilter: **Documenttype** is Order, **Status** is Vrijgegeven |
| Verkoopordernotities | Verkoopordernotities | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |

### <a name="synchronization-rules"></a>Synchronisatieregels

De volgende tabel beschrijft de regels die de synchronisatie tussen de [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[prod_short](includes/prod_short.md)] bepalen. Deze komen boven op de regels die zijn gedefinieerd voor Dataverse, die ook van toepassing zijn. Zie [Standaardentiteitstoewijzing](/dynamics365/business-central/admin-synchronizing-business-central-and-sales?branch=master-cds-crm#standard-table-mapping-for-synchronization) voor meer informatie.

> [!NOTE]  
> Wijzigingen in gegevens die zijn gemaakt door het integratiegebruikersaccount, worden niet gesynchroniseerd. Daarom raden we aan dat u geen gegevens wijzigt terwijl u dat account gebruikt. Zie voor meer informatie [Gebruikersaccounts instellen voor integratie met Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Tafel|Regel|
|-----|----|
|Eenheden|Maateenheden worden gesynchroniseerd met eenheidsgroepen in [!INCLUDE[crm_md](includes/crm_md.md)]. Er kan slechts één eenheid worden gedefinieerd in de eenhedengroep.|
|Artikelen|Wanneer artikelen worden gesynchroniseerd met [!INCLUDE[crm_md](includes/crm_md.md)]-producten, maakt [!INCLUDE[prod_short](includes/prod_short.md)] automatisch een prijslijst in [!INCLUDE[crm_md](includes/crm_md.md)]. Als u synchronisatiefouten wilt voorkomen, moet u deze prijslijst niet handmatig wijzigen.|
|Resources|Resources worden gesynchroniseerd met [!INCLUDE[crm_md](includes/crm_md.md)]-producten van het producttype Service.|
|Klantenprijsgroepen|Klantenprijsgroepen worden gesynchroniseerd met Sales-prijslijsten.|
|Verkoopprijzen|Sales-prijzen die het verkoopsoort Klantenprijsgroep hebben en waarvoor een verkoopcode is gedefinieerd, worden gesynchroniseerd met [!INCLUDE[crm_md](includes/crm_md.md)]-prijslijstregels|
|Opportunity's|Opportunity's worden gesynchroniseerd met [!INCLUDE[crm_md](includes/crm_md.md)]-opportunity's. De waarde van Verkoperscode definieert de eigenaar van de gekoppelde tabel in [!INCLUDE[crm_md](includes/crm_md.md)].|
|Geboekte verkoopfacturen|Geboekte verkoopfacturen worden gesynchroniseerd met verkoopfacturen. Voordat een factuur kan worden gesynchroniseerd, is het beter om alle andere tabellen die deel kunnen nemen aan de factuur, te synchroniseren van verkopers naar prijslijsten. De waarde van Verkoperscode op de factuurkop definieert de eigenaar van de gekoppelde tabel in Sales.|
|Verkooporders|Wanneer integratie van verkooporders is ingeschakeld, worden verkooporders binnen [!INCLUDE[prod_short](includes/prod_short.md)] die zijn gemaakt op basis van ingediende verkooporders in [!INCLUDE[crm_md](includes/crm_md.md)], gesynchroniseerd met verkooporders in VERKOOP OPNEMEN wanneer ze worden vrijgegeven. Voordat u orders synchroniseert, raden we u aan eerst alle tabellen te synchroniseren die bij de order betrokken zijn, zoals verkoopmedewerkers en prijslijsten. Het veld Verkoperscode in de orderkop definieert de eigenaar van de gekoppelde tabel in [!INCLUDE[crm_md](includes/crm_md.md)].|

### <a name="synchronization-jobs-for-a-sales-integration"></a>Synchronisatietaken voor een Sales-integratie

De taken worden uitgevoerd in de volgende volgorde om koppelingsafhankelijkheden tussen tabellen te voorkomen. Er zijn extra banen beschikbaar vanaf Dataverse. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](/dynamics365/business-central/admin-job-queues-schedule-tasks).

1. MAATEENHEID - Dynamics 365 Sales-synchronisatietaak  
2. RESOURCE-PRODUCT - Dynamics 365 Sales-synchronisatietaak  
3. ARTIKEL-PRODUCT - Dynamics 365 Sales-synchronisatietaak  
4. KLANTENPRIJSGROEPPRIJS - Dynamics 365 Sales-synchronisatietaak.
5. VERKOOPPRIJS-PRODUCTPRIJS - Dynamics 365 Sales-synchronisatietaak.
6. GEBOEKTEVERKOOPFACTUUR-FACTUUR - Dynamics 365 Sales-synchronisatietaak.

### <a name="default-synchronization-job-queue-entries"></a>Standaardsynchronisatieposten in de taakwachtrij

De volgende tabel beschrijft de standaardsynchronisatietaken voor Sales.  

|Taakwachtrij-item|Omschrijving|Richting|Toewijzing van integratietabel|Standaardsynchronisatiefrequentie (minuten)|Standaardinactiviteitslaaptijd (minuten)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|MAATEENHEID - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-eenhedengroepen met [!INCLUDE[prod_short](includes/prod_short.md)]-maateenheden.|Van [!INCLUDE[prod_short](includes/prod_short.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|MAATEENHEID|30|720<br> (12 uur)|
|RESOURCE-PRODUCT - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-producten met [!INCLUDE[prod_short](includes/prod_short.md)]-resources.|Van [!INCLUDE[prod_short](includes/prod_short.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|RESOURCE-PRODUCT|30|720<br> (12 uur)|
|ARTIKEL - PRODUCT - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-producten met [!INCLUDE[prod_short](includes/prod_short.md)]-artikelen.|Van [!INCLUDE[prod_short](includes/prod_short.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|ARTIKEL-PRODUCT|30|1440<br> (24 uur)|
|KLANTENPRIJSGROEPPRIJS - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-verkoopprijslijsten met [!INCLUDE[prod_short](includes/prod_short.md)]-klantenprijsgroepen| |KLANTENPRIJSGROEPEN-VERKOOPPRIJSLIJSTEN|30|1440<br> (24 uur)|
|VERKOOPPRIJS-PRODUCTPRIJS - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-productprijzen met [!INCLUDE[prod_short](includes/prod_short.md)]-verkoopprijzen.||PRODUCTPRIJS-VERKOOPPRIJS|30|1440<br> (24 uur)|
|GEBOEKTEVERKOOPFACTUUR-FACT - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-facturen met [!INCLUDE[prod_short](includes/prod_short.md)] geboekte verkoopfacturen.|Van [!INCLUDE[prod_short](includes/prod_short.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|FACTUREN-GEBOEKTE VERKOOPFACTUREN|30|1440<br> (24 uur)|
|Klantstatistieken - Dynamics 365 Sales-synchronisatie|Werkt [!INCLUDE[crm_md](includes/crm_md.md)]-rekeningen bij met de recentste [!INCLUDE[prod_short](includes/prod_short.md)]-klantgegevens In [!INCLUDE[crm_md](includes/crm_md.md)] wordt deze informatie in het snelle weergaveformulier **Statistiek van Business Central-account** weergegeven van accounts die zijn gekoppeld aan [!INCLUDE[prod_short](includes/prod_short.md)]-klanten.<br /><br /> Deze gegevens kunnen ook handmatig worden bijgewerkt vanuit van elke klantrecord. Zie voor meer informatie [Records handmatig koppelen en synchroniseren](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Opmerking:** Dit taakwachtrij-item is alleen van belang als de [!INCLUDE[prod_short](includes/prod_short.md)]-integratieoplossing is geïnstalleerd in [!INCLUDE[crm_md](includes/crm_md.md)]. |Niet van toepassing|Niet van toepassing|30|Niet van toepassing| 

## <a name="connecting-business-central-on-premises-versions-earlier-than-version-16"></a>Verbinding maken met Business Central On-Premises-versies ouder dan versie 16
Het Microsoft Power Platform-team heeft [bekend gemaakt](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse) dat het Office365-verificatietype wordt afgeschaft. Als u een versie van [!INCLUDE[prod_short](includes/prod_short.md)] on-premises gebruikt die ouder is dan versie 16, moet u het OAuth-verificatietype gebruiken om verbinding te maken met [!INCLUDE[crm_md](includes/crm_md.md)] online. In de stappen in deze sectie wordt beschreven hoe u de verbinding tot stand brengt.

### <a name="requirements"></a>Vereisten
U moet een Microsoft Azure-abonnement hebben. Een proefaccount werkt voor registratie van de toepassing.

### <a name="to-connect-a-version-of-business-central-earlier-than-version-16"></a>Verbinding maken met Business Central On-Premises-versies ouder dan versie 16
1. Importeer de Microsoft Dynamics 365 Business Central-integratieoplossing in uw [!INCLUDE[crm_md](includes/crm_md.md)]-omgeving. De integratieoplossing is beschikbaar in de map CrmCustomization op uw Business Central-installatie-dvd. Er zijn meerdere versies van de oplossing, zoals DynamicsNAVIntegrationSolution_v8 of DynamicsNAVIntegrationSolution_v9 of DynamicsNAVIntegrationSolution_v91. Welke oplossing u moet importeren, is afhankelijk van de versie van [!INCLUDE[crm_md](includes/crm_md.md)] waarmee u verbinding maakt. [!INCLUDE[crm_md](includes/crm_md.md)] online vereist de DynamicsNAVIntegrationSolution_v91-integratieoplossing.
2. Maak een niet-interactieve integratiegebruiker in uw [!INCLUDE[crm_md](includes/crm_md.md)]-omgeving en wijs de gebruiker de volgende beveiligingsrollen toe. Zie voor meer informatie [Een niet-interactief gebruikersaccount maken](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

   * Dynamics 365 Business Central-integratiebeheerder
   * Dynamics 365 Business Central-integratiegebruiker

   > [!Important]
   > Deze gebruiker mag niet de beveiligingsrol Systeembeheerder hebben. U kunt het systeembeheerdersaccount ook niet gebruiken als integratiegebruiker.

3.  Maak in de Azure Portal een app-registratie voor [!INCLUDE[prod_short](includes/prod_short.md)]. Zie voor de stappen [Een toepassing registreren in Azure Active Directory](/business-central/dev-itpro/administration/register-app-azure?branch=live#register-an-application-in-azure-active-directory). De instellingen die specifiek zijn voor het verbinden met [!INCLUDE[crm_md](includes/crm_md.md)], zijn de gedelegeerde machtigingen. De volgende tabel bevat en beschrijft de machtigingen.

   |API-/machtigingsnaam |Soort  |Omschrijving  |
   |---------|---------|---------|
   |Financieel.ReadWrite.All     |Gedelegeerd|Vereist voor [!INCLUDE[prod_short](includes/prod_short.md)].    |
   |user_impersonation     |Gedelegeerd|Vereist voor [!INCLUDE[crm_md](includes/crm_md.md)].|
   
4. Zoek in [!INCLUDE[prod_short](includes/prod_short.md)] naar **Microsoft Dynamics 365-verbinding instellen** en kies vervolgens de gerelateerde koppeling. 
5. Kies op de pagina **Microsoft Dynamics 365-verbinding instellen** in het veld **Verificatietype** de optie voor OAuth. 
6. Kies de CRM SDK-versie die overeenkomt met de oplossingsversie die u in stap 1 hebt geïmporteerd.
7. Voer in het veld **Serveradres** de URL van uw [!INCLUDE[crm_md](includes/crm_md.md)]-omgeving in en voer vervolgens de gebruikersnaam en het wachtwoord voor de integratiegebruiker in.
8. Geef in het veld **Verbindingstekenreeks** de id van de app-registratie op. Dit veld heeft twee tokens waarin de id van uw toepassing moet worden opgegeven.

   |Token           |Omschrijving  |
   |----------------|-------------|
   |**AppId**       |Stel in op de toepassings-id.      |
   |**RedirectUri** |Stel in op de toepassings-ID, maar voeg het prefix **app://** toe.         |

    **Voorbeeld** Het volgende voorbeeld toont een verbindingstekenreeks.

    ```
    AuthType=OAuth;Username=jsmith@contoso.onmicrosoft.com;Password=****;Url=https://contosotest.crm.dynamics.com;AppId=<your AppId>;RedirectUri=app://<your AppId>;TokenCacheStorePath=;LoginPrompt=Auto
    ```
9. Schakel de verbinding in.

> [!Note]
> Als u een verbinding met een [!INCLUDE[crm_md](includes/crm_md.md)]-exemplaar wilt configureren met een bepaald verificatietype, vult u de velden op het sneltabblad **Gegevens van verificatietype** in. Zie voor meer informatie [Verbindingstekenreeken in XRM tooling gebruiken om verbinding te maken met Dynamics 365](https://go.microsoft.com/fwlink/?linkid=843055). Deze stap is niet vereist wanneer u verbinding maakt met een online versie van [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-also"></a>Zie ook

[Gebruikersaccounts instellen voor integratie met [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Een verbinding instellen met [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Business Central en [!INCLUDE[crm_md](includes/crm_md.md)] synchroniseren](admin-synchronizing-business-central-and-sales.md)  
[Integratie voorbereiden van Dynamics 365 Sales On-Premises](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)


[!INCLUDE[footer-include](includes/footer-banner.md)]