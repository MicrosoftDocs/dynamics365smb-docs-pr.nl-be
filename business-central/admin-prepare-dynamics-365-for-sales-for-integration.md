---
title: Integreren met Dynamics 365 Sales
description: Leren hoe u Dynamics 365 Business Central voorbereidt op integratie met Dynamics 365 Sales.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'sales, crm, integration, integrating'
ms.date: 06/14/2021
ms.author: bholtorf
---
# Integreren met Dynamics 365 Sales

De functie van verkoper wordt vaak beschouwd als een van de meest naar buiten gerichte taken in een bedrijf. Het kan voor verkopers echter handig zijn in het bedrijf te kunnen kijken en te zien wat er bij de backend gebeurt. Door [!INCLUDE[prod_short](includes/prod_short.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] te integreren kunt u uw verkopers dat inzicht geven. Met de integratie kunnen gebruikers informatie bekijken in [!INCLUDE[prod_short](includes/prod_short.md)] terwijl ze werken in [!INCLUDE[crm_md](includes/crm_md.md)]. Bijvoorbeeld, tijdens het voorbereiden van een verkoopofferte kan het handig zijn om te weten of u voldoende voorraad hebt om de order te kunnen vervullen. Zie voor meer informatie [Dynamics 365 Sales gebruiken vanuit Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Dit onderwerp beschrijft de integratie van de online versies van [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[prod_short](includes/prod_short.md)] via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Zie voor informatie over on-premises configuratie [Dynamics 365 Sales voorbereiden voor on-premises integratie](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## Integreren via Dataverse
Om het gemakkelijk te maken om gegevens te verbinden en te synchroniseren met andere Dynamics 365-toepassingen integreert [!INCLUDE[prod_short](includes/prod_short.md)] ook met [!INCLUDE[prod_short](includes/cds_long_md.md)]. U kunt bijvoorbeeld verbinding maken met [!INCLUDE[crm_md](includes/crm_md.md)] of met apps die u zelf hebt gemaakt. Als u voor de eerste keer integreert, moet u dat doen via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Zie voor meer informatie [Integratie met Dataverse](admin-common-data-service.md).

Als u [!INCLUDE[crm_md](includes/crm_md.md)] al hebt geïntegreerd met [!INCLUDE[prod_short](includes/prod_short.md)], kunt u gegevens blijven synchroniseren met uw setup. Als u echter een upgrade uitvoert of uw [!INCLUDE[crm_md](includes/crm_md.md)]-integratie uitschakelt, moet u om het weer in te schakelen verbinding maken via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Zie voor meer informatie [Een integratie upgraden met Dynamics 365 Sales](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> Opnieuw verbinding maken via [!INCLUDE[prod_short](includes/cds_long_md.md)] past standaard synchronisatie-instellingen toe en overschrijft alle configuraties die u hebt. Zo worden de standaardtabeltoewijzingen toegepast.

## Integratie-instellingen die specifiek zijn voor een [!INCLUDE[crm_md](includes/crm_md.md)]-integratie
Integratie met [!INCLUDE[prod_short](includes/prod_short.md)] gebeurt via [!INCLUDE[prod_short](includes/cds_long_md.md)] en er zijn veel standaardinstellingen en tabellen beschikbaar. Naast de standaardinstellingen zijn er enkele die specifiek zijn voor [!INCLUDE[crm_md](includes/crm_md.md)]. In de volgende secties worden deze instellingen vermeld.

## Machtigingen en beveiligingsrollen voor gebruikersaccounts in Sales
Wanneer u de integratieoplossing installeert, worden machtigingen voor het integratiegebruikersaccount geconfigureerd. Als deze machtigingen zijn gewijzigd, moet u deze mogelijk opnieuw instellen. U kunt dat doen door de integratieoplossing opnieuw te installeren door te kiezen voor **Integratieoplossing opnieuw implementeren** op de pagina **Dynamics 365-verbinding instellen**. De volgende beveiligingsrollen worden ingezet:

* Dynamics 365 Business Central-integratiebeheerder
* Dynamics 365 Business Central-integratiegebruiker
* Dynamics 365 Business Central-gebruiker van productbeschikbaarheid

### Verbindingsinstellingen in de installatiehandleiding
U kunt een begeleide instelling gebruiken om snel de verbinding in te stellen en geavanceerde functies op te geven, zoals koppeling tussen records.

1. Kies **Instellingen en extensies** en kies vervolgens **Begeleide instelling**.
2. Kies **Dynamics 365 Sales-verbinding instellen** om de begeleide instelling te starten.
3. Vul de velden in.
4. Optioneel zijn er geavanceerde instellingen die de beveiliging kunnen verbeteren en meer mogelijkheden kunnen bieden. De volgende tabel beschrijft de geavanceerde instellingen.  

| Veld | Omschrijving |
|--|--|
| **Dynamics 365 Sales-oplossing importeren** | Installeer en configureer de integratieoplossing in [!INCLUDE[crm_md](includes/crm_md.md)]. <!--For more information, see [About the Base CDS Integration Solution](admin-common-data-service.md#about-the-business-central-integration-solution). Need to add a new topic--> |
|**Artikelbeschikbaarheid automatisch synchroniseren**|Hiermee wordt opgegeven dat de taakwachtrij voor artikelbeschikbaarheid moet worden gepland. De taakwachtrij wordt elke 30 minuten uitgevoerd en werkt de beschikbaarheid van de gekoppelde artikelen bij.|
| **Integratie van verkooporders inschakelen** | Wanneer mensen verkooporders maken in [!INCLUDE[crm_md](includes/crm_md.md)] en bestellingen uitvoeren in [!INCLUDE[prod_short](includes/prod_short.md)], integreert deze instelling het proces in [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie [Integratie van verkooporderverwerking inschakelen](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). U moet referenties opgeven voor een beheerdersaccount in [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie het gedeelte [Verkoopordergegevens verwerken](marketing-integrate-dynamicscrm.md#handling-sales-order-data). |
|**Dynamics 365 Sales-verbinding inschakelen** | De verbinding met [!INCLUDE[crm_md](includes/crm_md.md)] inschakelen. |
| **Dynamics 365 SDK-versie** | Dit is alleen relevant als u integreert met een on-premises versie van [!INCLUDE[crm_md](includes/crm_md.md)]. Deze SDK is de software-ontwikkelingskit van Dynamics 365 (ook Xrm genoemd) die u gebruikt om [!INCLUDE[prod_short](includes/prod_short.md)] te verbinden met [!INCLUDE[crm_md](includes/crm_md.md)]. De versie moet compatibel zijn met de SDK-versie die wordt gebruikt door [!INCLUDE[crm_md](includes/crm_md.md)] en gelijk zijn aan of nieuwer zijn dan de versie die wordt gebruikt door [!INCLUDE[crm_md](includes/crm_md.md)]. |

### Verbindingsinstellingen op de pagina Microsoft Dynamics 365-verbinding instellen

Voer de volgende gegevens in voor de verbinding van [!INCLUDE[crm_md](includes/crm_md.md)] met [!INCLUDE[prod_short](includes/prod_short.md)].

| Veld | Omschrijving |
|--|--|
|**Dynamics 365 Sales-URL**|De URL van uw [!INCLUDE[crm_md](includes/crm_md.md)]-exemplaar. Met deze instelling kunnen gebruikers de records in [!INCLUDE[prod_short](includes/prod_short.md)] openen die overeenkomen met records in [!INCLUDE[crm_md](includes/crm_md.md)]. Bijvoorbeeld een account of product. De [!INCLUDE[prod_short](includes/prod_short.md)]-records worden geopend in [!INCLUDE[prod_short](includes/prod_short.md)].|
|**Artikelbeschikbaarheid automatisch synchroniseren**|Hiermee wordt opgegeven dat de taakwachtrij voor artikelbeschikbaarheid moet worden gepland. De taakwachtrij wordt elke 30 minuten uitgevoerd en werkt de beschikbaarheid van de gekoppelde artikelen bij.|
|**Dynamics 365 SDK-versie**|Als u integreert met een on-premises versie van [!INCLUDE[crm_md](includes/crm_md.md)], is dit de Dynamics 365-softwareontwikkelingskit (ook Xrm genoemd) die u gebruikt om [!INCLUDE[prod_short](includes/prod_short.md)] te verbinden met [!INCLUDE[crm_md](includes/crm_md.md)]. De versie die u selecteert moet compatibel zijn met de SDK-versie die wordt gebruikt door [!INCLUDE[crm_md](includes/crm_md.md)]. Deze versie is gelijk aan of nieuwer dan de versie die wordt gebruikt door [!INCLUDE[crm_md](includes/crm_md.md)].|

Voer naast de bovenstaande instellingen de volgende instellingen in voor [!INCLUDE[crm_md](includes/crm_md.md)].

| Veld | Omschrijving |
|--|--|
| **Verkooporderintegratie is ingeschakeld** | Gebruikers de mogelijkheid bieden verkooporders en geactiveerde offertes in te dienen in [!INCLUDE[crm_md](includes/crm_md.md)] deze vervolgens weer te geven en te verwerken in [!INCLUDE[prod_short](includes/prod_short.md)]. Deze instelling integreert het proces in [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie [Integratie van verkooporderverwerking inschakelen](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). |
| **Automatisch verkooporders maken** | Maak een verkooporder in [!INCLUDE[prod_short](includes/prod_short.md)] wanneer een gebruiker er een maakt en indient in [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Verkoopoffertes automatisch verwerken** | Verwerk een verkoopofferte in [!INCLUDE[prod_short](includes/prod_short.md)] als een gebruiker er een maakt en activeert in [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie [Verkoopoffertegegevens verwerken](/dynamics365/business-central/marketing-integrate-dynamicscrm?tabs=new-experience#handling-sales-quotes-data). |
|**Bidirectionele synchronisatie van verkooporders**|Synchroniseer verkooporders in beide richtingen. Als een klant bijvoorbeeld van gedachten verandert over het product of de hoeveelheid die hij of zij heeft besteld in [!INCLUDE[crm_md](includes/crm_md.md)], kunt u het verkoopdocument archiveren en een nieuw document maken in [!INCLUDE[prod_short](includes/prod_short.md)]. Hetzelfde geldt voor wijzigingen in [!INCLUDE[prod_short](includes/prod_short.md)]. Als bijvoorbeeld prijzen, belastingbedragen of verwachte verzenddatums veranderen, worden de wijzigingen automatisch gesynchroniseerd met [!INCLUDE[crm_md](includes/crm_md.md)]. Bidirectionele synchronisatie helpt uw verkopers op de hoogte te blijven van de laatste wijzigingen en de status van prijsopgaven en orders.|

<!--
### User Account Settings
Integration with Business Central through Dataverse requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->

### Standaardtoewijzing van Sales-entiteit voor synchronisatie

Entiteiten in [!INCLUDE[crm_md](includes/crm_md.md)], zoals orders, zijn geïntegreerd met equivalente soorten tabellen in [!INCLUDE[prod_short](includes/prod_short.md)], zoals verkooporders. Als u wilt werken met [!INCLUDE[crm_md](includes/crm_md.md)]-gegevens, stelt u koppelingen in tussen tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] en [!INCLUDE[crm_md](includes/crm_md.md)].

In de volgende tabel staat de standaardtoewijzing tussen tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] die [!INCLUDE[prod_short](includes/prod_short.md)] biedt.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[crm_md](includes/crm_md.md)] | Synchronisatierichting | Standaardfilter |
|--|--|--|--|
| Eenheid | Eenhedengroep | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Artikel | Product | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Sales-contactfilter: **Producttype** is **Verkoopvoorraad** |
| Bron | Product | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Sales-contactfilter: **Producttype** is **Services** |
| Artikeleenheid | CRM-eenheid |[!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
| Resource-eenheid | CRM-eenheid |[!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]||
| Eenhedengroep | CRM-eenhedengroepen | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ||
| Klantenprijsgroep | Prijslijst | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Verkoopprijs | Productprijslijst | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | [!INCLUDE[prod_short](includes/prod_short.md)]-contactfilter: **Verkoopcode** is niet leeg, **Verkoopsoort** is **Klantenprijsgroep** |
| Verkoopkans | Verkoopkans | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |
| Verkoopfactuur | Factureren | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Verkoopfactuurregel | Factuurproduct | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Verkooporderkop | Verkooporder | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] <br><br> Als u in beide richtingen wilt synchroniseren, moet u de schakelaar **Bidirectionele synchronisatie van verkooporders** op de pagina **Dynamics 365-verbinding instellen** aanzetten.| [!INCLUDE[prod_short](includes/prod_short.md)]-verkoopkopfilter: **Documenttype** is Order, **Status** is Vrijgegeven |
| Verkoopordernotities | Verkoopordernotities | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |

> [!NOTE]
> De toewijzingen voor de tabellen Artikeleenheid, Resource-eenheid en Eenheidsgroep zijn alleen beschikbaar als uw beheerder de functieschakelaar **Functie-update: synchronisatie van meerdere maateenheden met Dynamics 365 Sales** op de pagina **Functiebeheer** heeft aangezet. Zie voor meer informatie [Artikelen en resources synchroniseren met producten in verschillende eenheden](admin-prepare-dynamics-365-for-sales-for-integration.md#synchronizing-items-and-resources-with-products-with-different-units-of-measure).

## Artikelen en resources synchroniseren met producten met verschillende eenheden
Bedrijven produceren of kopen de artikelen vaak in één eenheid en verkopen ze vervolgens in een andere. Als u artikelen wilt synchroniseren die meerdere eenheden gebruiken, moet u de functieschakelaar **Functie-update: synchronisatie van meerdere maateenheden met Dynamics 365 Sales** aanzetten op de pagina **Functiebeheer**. 

Als u de functie-update inschakelt, wordt er een nieuwe eenhedengroeptabel gemaakt en toegewezen aan elk artikel en elke resource in [!INCLUDE[prod_short](includes/prod_short.md)]. Met de tabellen kunt u de Eenhedengroep, Artikeleenheid en Resource-eenheid in [!INCLUDE[prod_short](includes/prod_short.md)] toewijzen aan de Dynamics 365 Sales-eenhedengroep in [!INCLUDE[crm_md](includes/crm_md.md)]. De volgende afbeelding toont de toewijzingen.

:::image type="content" source="media/unit group 1.png" alt-text="Tabeltoewijzingen voor eenhedengroepen":::

U kunt meerdere eenheden maken voor elke eenhedengroep en de groepen toewijzen aan producten in [!INCLUDE[crm_md](includes/crm_md.md)]. Daarna kunt u de producten synchroniseren met artikelen en bronnen in [!INCLUDE[prod_short](includes/prod_short.md)]. U kunt handmatig artikeleenheden of resource-eenheden koppelen aan een eenhedengroep. Wanneer u dat doet en de eenhedengroep voor het artikel of de resource niet is gekoppeld aan een eenhedengroep in [!INCLUDE[crm_md](includes/crm_md.md)], bijvoorbeeld omdat de eenhedengroep niet bestond, maakt [!INCLUDE[prod_short](includes/prod_short.md)] automatisch de eenhedengroep in [!INCLUDE[crm_md](includes/crm_md.md)].

### Artikelen en resources toewijzen aan producten
Wanneer u de functieschakelaar **Functie-update: synchronisatie van meerdere maateenheden met Dynamics 365 Sales** aanzet, gebeurt het volgende:

* Er worden nieuwe toewijzingen gemaakt voor artikelen en resources.
* Bestaande toewijzingen worden verwijderd. <!--which mappings?-->
* Een gegevensupgrade maakt eenhedengroepen voor artikelen en resources.

Als u de nieuwe toewijzingen wilt gebruiken, moet u eenhedengroepen, artikeleenheid en resource-eenheden synchroniseren. U moet ook artikelen en resources opnieuw synchroniseren. 

> [!NOTE]
> [!INCLUDE[crm_md](includes/crm_md.md)] staat niet toe dat u een eenhedengroep voor een product wijzigt. Daarom moet u uw producten buiten gebruik stellen en de artikelen en resources ontkoppelen, en vervolgens synchroniseren door nieuwe producten te maken in [!INCLUDE[crm_md](includes/crm_md.md)]. 

De volgende stappen beschrijven de stappen om te beginnen eenhedengroepen toe te wijzen:

1. Zorg ervoor dat producten in [!INCLUDE[crm_md](includes/crm_md.md)] niet zijn gekoppeld aan artikelen of resources in [!INCLUDE[prod_short](includes/prod_short.md)]. Als dat wel zo is, ga dan naar de pagina **Artikelen** en/of **Resources** en gebruik de filteropties om de gekoppelde records te selecteren. Kies vervolgens de actie **Dynamics 365 Sales** en selecteer **Ontkoppelen**. Met deze actie wordt een achtergrondtaak gepland om de records te ontkoppelen. Terwijl de taak wordt uitgevoerd, kunt u de status controleren met behulp van de actie **Synchronisatielogboek**. Zie voor meer informatie [Koppelen en synchroniseren](admin-how-to-couple-and-synchronize-records-manually.md). 
2. Omdat nieuwe producten worden gemaakt in [!INCLUDE[crm_md](includes/crm_md.md)] met nieuwe eenhedengroepen, doet u een van de volgende dingen om dubbele namen te voorkomen:
    
    * Hernoem uw producten en stel ze vervolgens buiten gebruik in [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie [Producten terugtrekken (Verkoophub)](/dynamics365/sales-enterprise/retire-product). Om uw producten in bulk te bewerken in Microsoft Excel meldt u zich aan bij Power Apps, kiest u uw omgeving, gaat u naar de tabel **Product** en kiest u het tabblad **Gegevens**. Wis alle filters die zijn toegepast. Kies in de groep **Gegevens** de actie **Gegevens bewerken in Excel**. Voeg een voor- of achtervoegsel toe aan de gekoppelde producten en trek ze vervolgens in.
    * Trek uw producten in en verwijder ze. 

3. Volg deze stappen om **Eenhedengroepen**, **Eenheden**, **Artikelen** en **Resources** te synchroniseren:
    1. Open in [!INCLUDE[prod_short](includes/prod_short.md)] de pagina **Instellingen Dynamics 365 Sales-verbinding**.
    2. Gebruik de actie **Volledige synchronisatie uitvoeren** om de pagina **Controle van volledige Dataverse-synchronisatie** te openen.
    3. Kies voor de toewijzingen **ARTIKELEENHEID**, **RESOURCE-EENHEID** en **EENHEDENGROEP** de actie **Volledige synchronisatie aanbevelen**.
    4. Kies de actie **Alles synchroniseren**.

    > [!NOTE]
    > Voor toewijzingen die nog niet volledig zijn gesynchroniseerd, worden ze met deze actie volledig gesynchroniseerd. Om te voorkomen dat die toewijzingen worden gesynchroniseerd, verwijdert u de toewijzingen van de pagina. Hierdoor worden ze alleen verwijderd uit de huidige volledige synchronisatie en worden de toewijzingen niet verwijderd.
    
5. Kies de toewijzing **ARTIKEL-PRODUCT** en kies vervolgens de actie **Opnieuw starten**. Door opnieuw starten ontstaan nieuwe producten vanuit de artikelen in [!INCLUDE[crm_md](includes/crm_md.md)] en wordt een nieuwe eenhedengroep toegewezen die specifiek is voor het artikel.
6. Kies de toewijzing **RESOURCE-PRODUCT** en kies vervolgens de actie **Opnieuw starten**. Door opnieuw starten ontstaan nieuwe producten vanuit de resources in [!INCLUDE[crm_md](includes/crm_md.md)] en wordt een nieuwe eenhedengroep toegewezen die specifiek is voor de resources.

### Synchronisatieregels

De volgende tabel beschrijft de regels die de synchronisatie tussen de [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[prod_short](includes/prod_short.md)] bepalen. Deze regels komen boven op de regels die zijn gedefinieerd voor Dataverse, die ook van toepassing zijn. Zie [Standaardentiteitstoewijzing](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization) voor meer informatie.

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
|Verkooporders|Wanneer integratie van verkooporders is ingeschakeld, worden verkooporders binnen [!INCLUDE[prod_short](includes/prod_short.md)] die zijn gemaakt op basis van ingediende verkooporders in [!INCLUDE[crm_md](includes/crm_md.md)], gesynchroniseerd met verkooporders in [!INCLUDE[crm_md](includes/crm_md.md)] wanneer ze worden vrijgegeven. Voordat u orders synchroniseert, raden we u aan eerst alle tabellen te synchroniseren die bij de order betrokken zijn, zoals verkoopmedewerkers en prijslijsten. Het veld Verkoperscode in de orderkop definieert de eigenaar van de gekoppelde tabel in [!INCLUDE[crm_md](includes/crm_md.md)].|

### Synchronisatietaken voor een Sales-integratie

De taken worden uitgevoerd in de volgende volgorde om koppelingsafhankelijkheden tussen tabellen te voorkomen. Er zijn meer banen beschikbaar vanuit Dataverse. Zie voor meer informatie [Taakwachtrijen gebruiken om taken te plannen](./admin-job-queues-schedule-tasks.md).

1. MAATEENHEID - Dynamics 365 Sales-synchronisatietaak  
2. RESOURCE-PRODUCT - Dynamics 365 Sales-synchronisatietaak  
3. ARTIKEL-PRODUCT - Dynamics 365 Sales-synchronisatietaak  
4. KLANTENPRIJSGROEPPRIJS - Dynamics 365 Sales-synchronisatietaak.
5. VERKOOPPRIJS-PRODUCTPRIJS - Dynamics 365 Sales-synchronisatietaak.
6. GEBOEKTEVERKOOPFACTUUR-FACTUUR - Dynamics 365 Sales-synchronisatietaak.

### Standaardsynchronisatieposten in de taakwachtrij

De volgende tabel beschrijft de standaardsynchronisatietaken voor Sales.  

|Taakwachtrij-item|Omschrijving|Richting|Toewijzing van integratietabel|Standaardsynchronisatiefrequentie (minuten)|Standaardinactiviteitslaaptijd (minuten)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|MAATEENHEID - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-eenhedengroepen met [!INCLUDE[prod_short](includes/prod_short.md)]-maateenheden.|Van [!INCLUDE[prod_short](includes/prod_short.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|EENHEID|30|720<br> (12 uur)|
|RESOURCE-PRODUCT - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-producten met [!INCLUDE[prod_short](includes/prod_short.md)]-resources.|Van [!INCLUDE[prod_short](includes/prod_short.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|RESOURCE-PRODUCT|30|720<br> (12 uur)|
|ARTIKEL - PRODUCT - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-producten met [!INCLUDE[prod_short](includes/prod_short.md)]-artikelen.|Van [!INCLUDE[prod_short](includes/prod_short.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|ARTIKEL-PRODUCT|30|1440<br> (24 uur)|
|KLANTENPRIJSGROEPPRIJS - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-verkoopprijslijsten met [!INCLUDE[prod_short](includes/prod_short.md)]-klantenprijsgroepen| |KLANTENPRIJSGROEPEN-VERKOOPPRIJSLIJSTEN|30|1440<br> (24 uur)|
|VERKOOPPRIJS-PRODUCTPRIJS - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-productprijzen met [!INCLUDE[prod_short](includes/prod_short.md)]-verkoopprijzen.||PRODUCTPRIJS-VERKOOPPRIJS|30|1440<br> (24 uur)|
|GEBOEKTEVERKOOPFACTUUR-FACT - Dynamics 365 Sales-synchronisatietaak|Synchroniseert [!INCLUDE[crm_md](includes/crm_md.md)]-facturen met [!INCLUDE[prod_short](includes/prod_short.md)] geboekte verkoopfacturen.|Van [!INCLUDE[prod_short](includes/prod_short.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)]|FACTUREN-GEBOEKTE VERKOOPFACTUREN|30|1440<br> (24 uur)|
|Klantstatistieken - Dynamics 365 Sales-synchronisatie|Werkt [!INCLUDE[crm_md](includes/crm_md.md)]-rekeningen bij met de recentste [!INCLUDE[prod_short](includes/prod_short.md)]-klantgegevens In [!INCLUDE[crm_md](includes/crm_md.md)] wordt deze informatie in het snelle weergaveformulier **Statistiek van Business Central-account** weergegeven van accounts die zijn gekoppeld aan [!INCLUDE[prod_short](includes/prod_short.md)]-klanten.<br /><br /> Deze gegevens kunnen ook handmatig worden bijgewerkt vanuit van elke klantrecord. Zie voor meer informatie [Records handmatig koppelen en synchroniseren](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Opmerking:** Dit taakwachtrij-item is alleen van belang als de [!INCLUDE[prod_short](includes/prod_short.md)]-integratieoplossing is geïnstalleerd in [!INCLUDE[crm_md](includes/crm_md.md)]. |Niet van toepassing|Niet van toepassing|30|Niet van toepassing| 

## Verbinding maken met on-premises versies van Business Central 2019 releasewave 1 en Microsoft Dynamics NAV 2018
Het Microsoft Power Platform-team heeft [bekend gemaakt](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse) dat het Office365-verificatietype wordt afgeschaft. Als u een versie van [!INCLUDE[prod_short](includes/prod_short.md)] on-premises gebruikt die ouder is dan Business Central 2019 releasewave 1, moet u het OAuth-verificatietype gebruiken om verbinding te maken met [!INCLUDE[crm_md](includes/crm_md.md)] online. In de stappen in deze sectie wordt beschreven hoe u verbinding maakt met de volgende productversies:

* Business Central 2019 releasewave 1
* Microsoft Dynamics NAV 2018

### Vereisten

- U moet een Microsoft Azure-abonnement hebben. Een proefaccount werkt voor registratie van de toepassing.
- [!INCLUDE[crm_md](includes/crm_md.md)] is geconfigureerd om een van de volgende verificatietypen te gebruiken:

   - Office365 (oud)

     > [!IMPORTANT]
     > Met ingang van april 2022 wordt Office365 (oud) niet langer ondersteund. Zie voor meer informatie [Belangrijke veranderingen (afschrijvingen) die aanstaande zijn in Power Apps, Power Automate en apps voor klantbetrokkenheid](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse).

   - OAuth

### Verbinding maken met Business Central 2019 releasewave 1 en Dynamics NAV 2018

1. Importeer de Microsoft Dynamics 365 Business Central-integratieoplossing in uw [!INCLUDE[crm_md](includes/crm_md.md)]-omgeving. De integratieoplossing is beschikbaar in de map CrmCustomization op uw [!INCLUDE[prod_short](includes/prod_short.md)]- of Dynamics NAV 2018-installatie-dvd. Importeer een van de volgende oplossingen, afhankelijk van uw productversie:

   * Voor [!INCLUDE[prod_short](includes/prod_short.md)] bevat de map de DynamicsNAVIntegrationSolution_v9 en DynamicsNAVIntegrationSolution_v91. oplossingen. Welke oplossing u moet importeren, is afhankelijk van de versie van [!INCLUDE[crm_md](includes/crm_md.md)] waarmee u verbinding maakt. [!INCLUDE[crm_md](includes/crm_md.md)] online vereist de DynamicsNAVIntegrationSolution_v91-integratieoplossing.
   * Voor Dynamics NAV 2018 installeert u de oplossing DynamicsNAVIntegrationSolution.

2. Maak een niet-interactieve integratiegebruiker in uw [!INCLUDE[crm_md](includes/crm_md.md)]-omgeving en wijs de gebruiker de volgende beveiligingsrollen toe. Zie voor meer informatie [Een niet-interactief gebruikersaccount maken](/power-platform/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

   * Dynamics 365 Business Central-integratiebeheerder
   * Dynamics 365 Business Central-integratiegebruiker

   > [!Important]
   > Deze gebruiker mag niet de beveiligingsrol Systeembeheerder hebben. U kunt het systeembeheerdersaccount ook niet gebruiken als integratiegebruiker.

3.  Maak in de Azure Portal een app-registratie voor [!INCLUDE[prod_short](includes/prod_short.md)]. Zie voor meer informatie [Een toepassing registreren in Azure Active Directory](/powerapps/developer/data-platform/walkthrough-register-app-azure-active-directory). 
  
   > [!NOTE]
   > We raden u aan de app te registreren in dezelfde tenant als uw Dataverse-omgeving, zodat u geen toestemming hoeft te geven om de app toegang te geven tot de omgeving. Als u de app in een andere omgeving registreert, moet u inloggen op Azure AD met behulp van het beheerdersaccount voor uw Dataverse-omgeving en toestemming geven.
   >
   > Bovendien mag de app die u registreert geen geheim hebben. Een app met een geheim verbinden met Dataverse is alleen beschikbaar in Business Central 2020 releasewave 1 en hoger.
  
4. Doe van de volgende dingen, afhankelijk van uw productversie:

    * Zoek in [!INCLUDE[prod_short](includes/prod_short.md)] naar **Microsoft Dynamics 365-verbinding instellen** en kies vervolgens de gerelateerde koppeling. 
    * Zoek in Dynamics NAV 2018 naar **Microsoft Dynamics 365 for Sales-verbinding instellen** en kies vervolgens de gerelateerde koppeling.

5. Kies in het veld **Verificatietype** de optie voor OAuth. 
6. Kies de CRM SDK-versie die overeenkomt met de oplossingsversie die u in stap 1 hebt geïmporteerd.

   > [!NOTE]
   > Deze stap is alleen relevant voor [!INCLUDE[prod_short](includes/prod_short.md)].

7. Voer de URL van uw [!INCLUDE[crm_md](includes/crm_md.md)]-omgeving in en voer vervolgens de gebruikersnaam en het wachtwoord voor de integratiegebruiker in. 

   * Gebruik in [!INCLUDE[prod_short](includes/prod_short.md)] het veld **Serveradres**.
   * Gebruik in Dynamics NAV 2018 het veld **Dynamics 365 Sales-URL**.

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
> Als u een verbinding met een [!INCLUDE[crm_md](includes/crm_md.md)]-exemplaar wilt configureren met een bepaald verificatietype, vult u de velden op het sneltabblad **Gegevens van verificatietype** in. Zie voor meer informatie [Verificatie met Microsoft Dataverse-webservices](/powerapps/developer/data-platform/authentication). Deze stap is niet vereist wanneer u verbinding maakt met een online versie van [!INCLUDE[prod_short](includes/prod_short.md)].

## Zie ook

[Gebruikersaccounts instellen voor integratie met [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Een verbinding instellen met [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Business Central en [!INCLUDE[crm_md](includes/crm_md.md)] synchroniseren](admin-synchronizing-business-central-and-sales.md)  
[Integratie voorbereiden van Dynamics 365 Sales On-Premises](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)


[!INCLUDE[footer-include](includes/footer-banner.md)]
