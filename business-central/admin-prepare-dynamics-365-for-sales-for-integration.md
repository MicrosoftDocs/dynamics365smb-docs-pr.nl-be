---
title: Integratie met Dynamics 365 Sales | Microsoft Docs
description: Leren hoe u Dynamics 365 Business Central voorbereidt op integratie met Dynamics 365 Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: b4e3181564f351979bcb22512ab02a9a43456bde
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196579"
---
# <a name="integrating-with-dynamics-365-sales"></a>Integreren met Dynamics 365 Sales
De functie van verkoper wordt vaak beschouwd als een van de meest naar buiten gerichte taken in een bedrijf. Het kan voor verkopers echter handig zijn in het bedrijf te kunnen kijken en te zien wat er bij de backend gebeurt. Door [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] te integreren kunt u uw verkopers dat inzicht geven door ze informatie in [!INCLUDE[d365fin](includes/d365fin_md.md)] te laten zien terwijl ze werken in [!INCLUDE[crm_md](includes/crm_md.md)]. Bijvoorbeeld, tijdens het voorbereiden van een verkoopofferte kan het handig zijn om te weten of u voldoende voorraad hebt om de order te kunnen vervullen. Zie voor meer informatie [Dynamics 365 Sales gebruiken vanuit Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Dit onderwerp beschrijft de integratie van de online versies van [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[d365fin](includes/d365fin_md.md)] via [!INCLUDE[d365fin](includes/cds_long_md.md)]. Zie voor informatie over on-premises configuratie [Dynamics 365 Sales voorbereiden voor on-premises integratie](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration.md).

## <a name="integrating-through-common-data-service"></a>Integreren via Common Data Service
[!INCLUDE[d365fin](includes/d365fin_md.md)] integreert ook met [!INCLUDE[d365fin](includes/cds_long_md.md)], waardoor het eenvoudig is om gegevens te verbinden en te synchroniseren met andere Dynamics 365-toepassingen, zoals [!INCLUDE[crm_md](includes/crm_md.md)], of zelfs apps die u zelf bouwt. Als u voor de eerste keer integreert, raden we u aan dit te doen via [!INCLUDE[d365fin](includes/cds_long_md.md)]. Zie voor meer informatie [Integratie met Common Data Service](admin-common-data-service.md).

Als u al [!INCLUDE[crm_md](includes/crm_md.md)] hebt geïntegreerd met [!INCLUDE[d365fin](includes/d365fin_md.md)], kunt u gegevens blijven synchroniseren met uw setup. Als u echter een upgrade uitvoert of uw [!INCLUDE[crm_md](includes/crm_md.md)]-integratie uitschakelt, moet u om het weer in te schakelen verbinding maken via [!INCLUDE[d365fin](includes/cds_long_md.md)]. Zie voor meer informatie [Een integratie upgraden met Dynamics 365 Sales](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> Opnieuw verbinding maken via [!INCLUDE[d365fin](includes/cds_long_md.md)] past standaard synchronisatie-instellingen toe en overschrijft alle configuraties die u hebt. Zo worden de standaardtabeltoewijzingen toegepast.

## <a name="integration-settings-that-are-specific-to-a-crm_md-integration"></a>Integratie-instellingen die specifiek zijn voor een [!INCLUDE[crm_md](includes/crm_md.md)]-integratie
Integratie met [!INCLUDE[d365fin](includes/d365fin_md.md)] gebeurt door [!INCLUDE[d365fin](includes/cds_long_md.md)] en er zijn veel standaardinstellingen en entiteiten die door de integratie worden geleverd. Naast de standaardinstellingen zijn er enkele die specifiek zijn voor [!INCLUDE[crm_md](includes/crm_md.md)]. In de volgende secties worden die vermeld.

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

|Veld|Omschrijving|
|-----|-----|
|**Dynamics 365 Sales-oplossing importeren**|Schakel dit in om de integratieoplossing te installeren en configureren in [!INCLUDE[crm_md](includes/crm_md.md)]. <!--For more information, see [About the Base CDS Integration Solution](admin-common-data-service.md#about-the-business-central-integration-solution). Need to add a new topic-->|
|**Webservice Artikelbeschikbaarheid publiceren**|Zorg dat personen die [!INCLUDE[crm_md](includes/crm_md.md)] gebruiken de beschikbaarheid van producten (artikelen) in voorraad in [!INCLUDE[d365fin](includes/d365fin_md.md)] kunnen bekijken. Dit vereist een [!INCLUDE[d365fin](includes/d365fin_md.md)]-gebruikersaccount met een webservicetoegangssleutel. De sleutel toewijzen is een proces van twee stappen. In het gebruikersaccount in [!INCLUDE[d365fin](includes/d365fin_md.md)] moet u de actie **Sleutel van webservice wijzigen** kiezen. In de begeleide instelling Dynamics 365 Sales-verbinding instellen moet u de URL van de Dynamics 365 Business Central OData-webservice opgeven en [!INCLUDE[d365fin](includes/d365fin_md.md)]-gebruikersreferenties opgeven voor toegang tot de service. Zie voor meer informatie [OData-webservices](/dynamics365/business-central/dev-itpro/webservices/odata-web-services).|
|**URL van Business Central OData-webservice**|Als u de webservice voor het weergeven van artikelbeschikbaarheid inschakelt, wordt de URL van de OData-webservice voor u verschaft.|
|**Gebruikersnaam van Business Central OData-webservice**|De naam van het [!INCLUDE[d365fin](includes/d365fin_md.md)]-gebruikersaccount dat [!INCLUDE[crm_md](includes/crm_md.md)] gebruikt om informatie over artikelbeschikbaarheid in [!INCLUDE[d365fin](includes/d365fin_md.md)] op te halen met de OData-webservice.|
|**Toegangssleutel van Business Central OData-webservice**|De toegangssleutel voor het gebruikersaccount dat [!INCLUDE[crm_md](includes/crm_md.md)] gebruikt om informatie over artikelbeschikbaarheid uit [!INCLUDE[d365fin](includes/d365fin_md.md)] op te halen met de OData-webservice. De sleutel wordt toegewezen aan de gebruiker die is gekozen in het veld **Gebruikersnaam van Business Central OData-webservice**. Als u de sleutel wilt krijgen, kiest u de knop **Opzoekwaarde** naast de gebruikersnaam, kiest u de gebruiker, kiest u **Beheren** en klikt u vervolgens op **Bewerken**. Kies op de gebruikerskaart **Acties**, **Verificatie** en kies vervolgens **Sleutel van webservice wijzigen**|
|**Integratie van verkooporders inschakelen**|Wanneer mensen verkooporders maken in [!INCLUDE[crm_md](includes/crm_md.md)] en bestellingen uitvoeren in [!INCLUDE[d365fin](includes/d365fin_md.md)], integreert dit het proces in [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie [Integratie van verkooporderverwerking inschakelen](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). Hiervoor moet u referenties opgeven voor een beheerdersaccount in [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie het gedeelte [Verkoopordergegevens verwerken](marketing-integrate-dynamicscrm.md#handling-sales-order-data).|
|**CDS-verbinding inschakelen**|De verbinding met [!INCLUDE[d365fin](includes/cds_long_md.md)] inschakelen.|
|**Dynamics 365 SDK-versie**|Dit is alleen relevant als u integreert met een on-premises versie van [!INCLUDE[crm_md](includes/crm_md.md)]. Dit is de software-ontwikkelingskit van Dynamics 365 (ook Xrm genoemd) die u gebruikt om [!INCLUDE[d365fin](includes/d365fin_md.md)] te verbinden met [!INCLUDE[crm_md](includes/crm_md.md)]. De versie moet compatibel zijn met de SDK-versie die wordt gebruikt door [!INCLUDE[crm_md](includes/crm_md.md)] en gelijk zijn aan of nieuwer zijn dan de versie die wordt gebruikt door [!INCLUDE[crm_md](includes/crm_md.md)].|

### <a name="connection-settings-on-the-microsoft-dynamics-365-connection-setup-page"></a>Verbindingsinstellingen op de pagina Microsoft Dynamics 365-verbinding instellen 
Voer de volgende gegevens in voor de verbinding van [!INCLUDE[crm_md](includes/crm_md.md)] met [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Veld|Omschrijving|
|-----|-----|
|**Dynamics 365 Sales-URL**|De URL van uw [!INCLUDE[crm_md](includes/crm_md.md)]-exemplaar. Hierdoor kunnen gebruikers in [!INCLUDE[d365fin](includes/d365fin_md.md)] bijbehorende records openen vanuit records in [!INCLUDE[crm_md](includes/crm_md.md)], zoals een account of product. De [!INCLUDE[d365fin](includes/d365fin_md.md)]-records worden geopend in [!INCLUDE[d365fin](includes/d365fin_md.md)].|
|**Webservice Artikelbeschikbaarheid ingeschakeld**|Zorg dat personen die [!INCLUDE[crm_md](includes/crm_md.md)] gebruiken de beschikbaarheid van producten (artikelen) in voorraad in [!INCLUDE[d365fin](includes/d365fin_md.md)] kunnen bekijken. Als u dit inschakelt, moet u ook een gebruikersnaam en een toegangssleutel opgeven die de [!INCLUDE[crm_md](includes/crm_md.md)] moet gebruiken om bij de OData webservice te vragen naar beschikbaarheid van (artikelen). Zie voor meer informatie [OData-webservices](/dynamics365/business-central/dev-itpro/webservices/odata-web-services.md).|
|**URL van Dynamics 365 Business Central OData-webservice**|Als u de webservice Artikelbeschikbaarheid inschakelt, wordt de URL van de OData-webservice voor u verschaft. Stel dit veld in op de URL van het te gebruiken [!INCLUDE[d365fin](includes/d365fin_md.md)]-exemplaar.<br /><br /> Als u het veld opnieuw wilt instellen op de standaard-URL voor de [!INCLUDE[d365fin](includes/d365fin_md.md)], kiest u de actie **Webclient-URL opnieuw instellen**.<br /><br /> Dit veld is alleen van belang als de [!INCLUDE[d365fin](includes/d365fin_md.md)]-integratieoplossing is geïnstalleerd in [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Gebruikersnaam van Dynamics 365 Business Central OData-webservice**|De naam van het gebruikersaccount dat de [!INCLUDE[crm_md](includes/crm_md.md)] gebruikt om informatie over artikelbeschikbaarheid in [!INCLUDE[d365fin](includes/d365fin_md.md)] op te halen met de OData-webservice.|
|**Toegangssleutel van Dynamics 365 Business Central OData-webservice**|De toegangssleutel voor het gebruikersaccount dat de [!INCLUDE[crm_md](includes/crm_md.md)] gebruikt om informatie over artikelbeschikbaarheid uit [!INCLUDE[d365fin](includes/d365fin_md.md)] op te halen met de OData-webservice. De sleutel wordt toegewezen aan de gebruiker die is gekozen in het veld **Gebruikersnaam van Dynamics 365 Business Central OData-webservice**. Als u de sleutel wilt krijgen, kiest u de knop **Opzoekwaarde** naast de gebruikersnaam, kiest u de gebruiker, kiest u **Beheren** en klikt u vervolgens op **Bewerken**. Kies op de gebruikerskaart **Acties**, **Verificatie** en kies vervolgens **Sleutel van webservice wijzigen**|
|**Dynamics 365 SDK-versie**|Als u integreert met een on-premises versie van [!INCLUDE[crm_md](includes/crm_md.md)], is dit de Dynamics 365-softwareontwikkelingskit (ook Xrm genoemd) die u gebruikt om [!INCLUDE[d365fin](includes/d365fin_md.md)] te verbinden met [!INCLUDE[crm_md](includes/crm_md.md)]. De versie die u selecteert moet compatibel zijn met de SDK-versie die wordt gebruikt door [!INCLUDE[crm_md](includes/crm_md.md)]. Deze versie is gelijk aan of nieuwer dan de versie die wordt gebruikt door [!INCLUDE[crm_md](includes/crm_md.md)].|-->

Voer naast de bovenstaande instellingen de volgende instellingen in voor [!INCLUDE[crm_md](includes/crm_md.md)].

|Veld|Omschrijving|
|-----|-----|
|**Verkooporderintegratie is ingeschakeld**|Gebruikers de mogelijkheid bieden verkooporders en geactiveerde offertes in te dienen in [!INCLUDE[crm_md](includes/crm_md.md)] deze vervolgens weer te geven en te verwerken in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dit integreert het proces in [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie [Integratie van verkooporderverwerking inschakelen](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration).|
|**Automatisch verkooporders maken**|Maak een verkooporder in [!INCLUDE[d365fin](includes/d365fin_md.md)] wanneer een gebruiker er een maakt en indient in [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Verkoopoffertes automatisch verwerken**|Verwerk een verkoopofferte in [!INCLUDE[d365fin](includes/d365fin_md.md)] als een gebruiker er een maakt en activeert in [!INCLUDE[crm_md](includes/crm_md.md)].|

<!--
### User Account Settings
Integrate with Business Central through Common Data Service requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->

### <a name="standard-sales-entity-mapping-for-synchronization"></a>Standaardtoewijzing van Sales-entiteit voor synchronisatie
Entiteiten in [!INCLUDE[crm_md](includes/crm_md.md)], zoals orders, zijn geïntegreerd met equivalente soorten entiteiten in [!INCLUDE[d365fin](includes/d365fin_md.md)], zoals verkooporders. Als u wilt werken met [!INCLUDE[crm_md](includes/crm_md.md)]-gegevens, stelt u koppelingen in tussen entiteiten in [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)].

In de volgende tabel staat de standaardtoewijzing tussen entiteiten in [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] die [!INCLUDE[d365fin](includes/d365fin_md.md)] biedt.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[crm_md](includes/crm_md.md)]|Synchronisatierichting|Standaardfilter|
|-------------------------------------------|-----|-------------------------|--------------|
|Maateenheid|Eenhedengroep|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Artikel|Product|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-contactfilter: **Producttype** is **Verkoopvoorraad**|
|Bron|Product|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Sales-contactfilter: **Producttype** is **Services**|
|Klantenprijsgroep|Prijslijst|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Verkoopprijs|Productprijslijst|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)]-contactfilter: **Verkoopcode** is niet leeg, **Verkoopsoort** is **Klantenprijsgroep**|
|Opportunity|Opportunity|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |
|Verkoopfactuur|Factureren|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Verkoopfactuurregel|Factuurproduct|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Verkooporderkop|Verkooporder|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|[!INCLUDE[d365fin](includes/d365fin_md.md)]-verkoopkopfilter: **Documenttype** is Order, **Status** is Vrijgegeven|
|Verkoopordernotities|Verkoopordernotities|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |

### <a name="synchronization-rules"></a>Synchronisatieregels
De volgende tabel beschrijft de regels die de synchronisatie tussen de [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[d365fin](includes/d365fin_md.md)] bepalen. Deze komen boven op de regels die zijn gedefinieerd voor Common Data Service, die ook van toepassing zijn. Zie [Standaardentiteitstoewijzing](/dynamics365/business-central/admin-synchronizing-business-central-and-sales?branch=master-cds-crm#standard-entity-mapping-for-synchronization) voor meer informatie.

> [!NOTE]  
> Wijzigingen in gegevens die zijn gemaakt door het integratiegebruikersaccount, worden niet gesynchroniseerd. Daarom raden we aan dat u geen gegevens wijzigt terwijl u dat account gebruikt. Zie voor meer informatie [Gebruikersaccounts instellen voor integratie met Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Tafel|Regel|
|-----|----|
|Eenheden|Maateenheden worden gesynchroniseerd met eenheidsgroepen in [!INCLUDE[crm_md](includes/crm_md.md)]. Er kan slechts één eenheid worden gedefinieerd in de eenhedengroep.|
|Artikelen|Wanneer artikelen worden gesynchroniseerd met [!INCLUDE[crm_md](includes/crm_md.md)]-producten, maakt [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisch een prijslijst in [!INCLUDE[crm_md](includes/crm_md.md)]. Als u synchronisatiefouten wilt voorkomen, moet u deze prijslijst niet handmatig wijzigen.|
|Resources|Resources worden gesynchroniseerd met [!INCLUDE[crm_md](includes/crm_md.md)]-producten van het producttype Service.|
|Klantenprijsgroepen|Klantenprijsgroepen worden gesynchroniseerd met Sales-prijslijsten.|
|Verkoopprijzen|Sales-prijzen die het verkoopsoort Klantenprijsgroep hebben en waarvoor een verkoopcode is gedefinieerd, worden gesynchroniseerd met [!INCLUDE[crm_md](includes/crm_md.md)]-prijslijstregels|
|Opportunity's|Opportunity's worden gesynchroniseerd met [!INCLUDE[crm_md](includes/crm_md.md)]-opportunity's. De waarde van Verkoperscode definieert de eigenaar van de gekoppelde entiteit in [!INCLUDE[crm_md](includes/crm_md.md)].|
|Geboekte verkoopfacturen|Geboekte verkoopfacturen worden gesynchroniseerd met verkoopfacturen. Voordat een factuur kan worden gesynchroniseerd, is het beter om alle andere entiteiten die deel kunnen nemen aan de factuur, te synchroniseren van verkopers naar prijslijsten. De waarde van Verkoperscode op de factuurkop definieert de eigenaar van de gekoppelde entiteit in Sales.|
|Verkooporders|Wanneer integratie van verkooporders is ingeschakeld, worden verkooporders binnen [!INCLUDE[d365fin](includes/d365fin_md.md)] die zijn gemaakt op basis van ingediende verkooporders in [!INCLUDE[crm_md](includes/crm_md.md)], gesynchroniseerd met verkooporders in VERKOOP OPNEMEN wanneer ze worden vrijgegeven. Voordat u orders synchroniseert, raden we u aan eerst alle entiteiten te synchroniseren die bij de order betrokken zijn, zoals verkoopmedewerkers en prijslijsten. Het veld Verkoperscode in de orderkop definieert de eigenaar van de gekoppelde entiteit in [!INCLUDE[crm_md](includes/crm_md.md)].|

### <a name="synchronization-jobs-for-a-sales-integration"></a>Synchronisatietaken voor een Sales-integratie
De taken worden uitgevoerd in de volgende volgorde om koppelingsafhankelijkheden tussen entiteiten te voorkomen. Er zijn extra banen beschikbaar vanaf Common Data Service. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](/dynamics365/business-central/admin-job-queues-schedule-tasks.md).

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
|MAATEENHEID - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-eenhedengroepen met [!INCLUDE[d365fin](includes/d365fin_md.md)]-maateenheden.|Van [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|MAATEENHEID|30|720<br> (12 uur)|
|RESOURCE-PRODUCT - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-producten met [!INCLUDE[d365fin](includes/d365fin_md.md)]-resources.|Van [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|RESOURCE-PRODUCT|30|720<br> (12 uur)|
|ARTIKEL - PRODUCT - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-producten met [!INCLUDE[d365fin](includes/d365fin_md.md)]-artikelen.|Van [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|ARTIKEL-PRODUCT|30|1440<br> (24 uur)|
|KLANTENPRIJSGROEPPRIJS - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-verkoopprijslijsten met [!INCLUDE[d365fin](includes/d365fin_md.md)]-klantenprijsgroepen| |KLANTENPRIJSGROEPEN-VERKOOPPRIJSLIJSTEN|30|1440<br> (24 uur)|
|VERKOOPPRIJS-PRODUCTPRIJS - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-productprijzen met [!INCLUDE[d365fin](includes/d365fin_md.md)]-verkoopprijzen.||PRODUCTPRIJS-VERKOOPPRIJS|30|1440<br> (24 uur)|
|GEBOEKTEVERKOOPFACTUUR-FACT - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-facturen met [!INCLUDE[d365fin](includes/d365fin_md.md)] geboekte verkoopfacturen.|Van [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|FACTUREN-GEBOEKTE VERKOOPFACTUREN|30|1440<br> (24 uur)|
|Klantstatistieken - Dynamics 365 Sales-synchronisatie|Werkt [!INCLUDE[crm_md](includes/crm_md.md)]-rekeningen bij met de recentste [!INCLUDE[d365fin](includes/d365fin_md.md)]-klantgegevens In [!INCLUDE[crm_md](includes/crm_md.md)] wordt deze informatie in het snelle weergaveformulier **Statistiek van Business Central-account** weergegeven van accounts die zijn gekoppeld aan [!INCLUDE[d365fin](includes/d365fin_md.md)]-klanten.<br /><br /> Deze gegevens kunnen ook handmatig worden bijgewerkt vanuit van elke klantrecord. Zie voor meer informatie [Records handmatig koppelen en synchroniseren](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Opmerking:** Dit taakwachtrij-item is alleen van belang als de [!INCLUDE[d365fin](includes/d365fin_md.md)]-integratieoplossing is geïnstalleerd in [!INCLUDE[crm_md](includes/crm_md.md)]. |Niet van toepassing|Niet van toepassing|30|Niet van toepassing| 


### <a name="note-for-on-premises-versions"></a>Opmerking voor on-premises versies
> [!Note]
> Als u een on-premises versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] verbindt met [!INCLUDE[crm_md](includes/crm_md.md)] en u een verbinding met een [!INCLUDE[crm_md](includes/crm_md.md)]-exemplaar wilt configureren met een specifiek verificatietype, vult u de velden op het sneltabblad **Gegevens van verificatietype** in. Zie voor meer informatie [Verbindingstekenreeken in XRM tooling gebruiken om verbinding te maken met Dynamics 365](https://go.microsoft.com/fwlink/?linkid=843055). Deze stap is niet vereist wanneer u verbinding maakt met een online versie van [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Zie ook  
[Gebruikersaccounts instellen voor integratie met [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Een verbinding instellen met [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Business Central en [!INCLUDE[crm_md](includes/crm_md.md)] synchroniseren](admin-synchronizing-business-central-and-sales.md)  
[Integratie voorbereiden van Dynamics 365 Sales On-Premises](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)
