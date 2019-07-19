---
title: Verbinden met Dynamics 365 for Sales | Microsoft Docs
description: U kunt integreren met Dynamics 365 for Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/06/2019
ms.author: bholtorf
ms.openlocfilehash: dfcb664d352683566df233d6b9b95900f2d76a5a
ms.sourcegitcommit: f2e3b571eab6e01d9f5aa8ef47056b6bd313dcbd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/13/2019
ms.locfileid: "1629654"
---
# <a name="set-up-a-connection-to-dynamics-365-for-sales"></a>Een verbinding instellen met Dynamics 365 for Sales
Voor integratie met [!INCLUDE[crm_md](includes/crm_md.md)] moet u een verbinding instellen tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)].

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085501]

## <a name="before-you-start"></a>Voordat u begint
Voordat u de apps begint te verbinden, zijn er enkele stuks van informatie die nuttig zijn om gereed te hebben:  

* Een URL voor uw [!INCLUDE[crm_md](includes/crm_md.md)]-app. Een snelle manier om de URL te krijgen is [!INCLUDE[crm_md](includes/crm_md.md)] te openen, de URL te kopiëren en deze vervolgens te plakken in het veld **Dynamics 365 for Sales-URL** in [!INCLUDE[d365fin](includes/d365fin_md.md)]. [!INCLUDE[d365fin](includes/d365fin_md.md)] corrigeert de opmaak voor u.  
* Een gebruikersnaam en wachtwoord van een gebruikersaccount dat alleen voor de integratie wordt gebruikt.  
* De gebruikersnaam en het wachtwoord van het account dat beheerdersmachtigingen heeft.  

> [!Note]
> Deze stappen beschrijven de procedure voor de online versie van [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="set-up-test-and-enable-a-connection-to-includecrmmdincludescrmmdmd"></a>Instellen, testen en een verbinding inschakelen met [!INCLUDE[crm_md](includes/crm_md.md)]  
Voor alle verificatiesoorten anders dan Office 365-verificatie stelt u de verbinding met Dynamics 365 for Sales in op de pagina **Microsoft Dynamics 365 for Sales-verbinding instellen**. Voor Office 365-verificatie kunt u ook de begeleide instelling **Dynamics 365 for Sales-verbinding instellen** gebruiken, die u helpt de vereiste informatie op te geven.

### <a name="to-use-an-assisted-setup-guide"></a>Een begeleide instelling gebruiken
De begeleide instelling **Dynamics 365 for Sales-verbinding instellen** kan u helpen de verbinding in te stellen en op te geven of geavanceerde functies moeten worden ingeschakeld, zoals koppeling tussen records.

1. Kies **Instellingen en extensies** en kies vervolgens **Begeleide instelling**.
2. Kies **Dynamics 365 for Sales-verbinding instellen** om de begeleide instelling te starten.
3. Vul de velden in.
4. Eventueel zijn er geavanceerde instellingen die beveiliging kunnen vergroten en aanvullende [!INCLUDE[crm_md](includes/crm_md.md)]-mogelijkheden inschakelen, zoals verwerking van verkooporders en weergave van voorraadniveaus. De volgende tabel beschrijft de geavanceerde instellingen.  

|Veld|Omschrijving|
|-----|-----|
|**Dynamics 365 for Sales-oplossing importeren**|Schakel dit in om de integratieoplossing te installeren en configureren in [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie [Over de Business Central-integratieoplossing](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|
|**Webservice Artikelbeschikbaarheid publiceren**|Zorg dat personen die [!INCLUDE[crm_md](includes/crm_md.md)] gebruiken de beschikbaarheid van producten (artikelen) in voorraad in [!INCLUDE[d365fin](includes/d365fin_md.md)] kunnen bekijken. Hiervoor moet het [!INCLUDE[d365fin](includes/d365fin_md.md)]-gebruikersaccount een webservicetoegangssleutel hebben. De sleutel toewijzen is een proces van twee stappen. In het gebruikersaccount in [!INCLUDE[d365fin](includes/d365fin_md.md)] moet u de actie **Sleutel van webservice wijzigen** kiezen. In de begeleide instelling Dynamics 365 for Sales-verbinding instellen moet u de URL van de Dynamics 365 Business Central OData-webservice opgeven en [!INCLUDE[d365fin](includes/d365fin_md.md)]-gebruikersreferenties opgeven voor toegang tot de service. Zie voor meer informatie [OData-webservices](/dynamics365/business-central/dev-itpro/webservices/odata-web-services.md).|
|**URL van Dynamics 365 Business Central OData-webservice**|Als u de webservice Artikelbeschikbaarheid inschakelt, wordt de URL van de OData-webservice voor u verschaft.|
|**Gebruikersnaam van Dynamics 365 Business Central OData-webservice**|De naam van het [!INCLUDE[d365fin](includes/d365fin_md.md)]-gebruikersaccount dat de [!INCLUDE[crm_md](includes/crm_md.md)] gebruikt om informatie over artikelbeschikbaarheid in [!INCLUDE[d365fin](includes/d365fin_md.md)] op te halen met de OData-webservice.|
|**Toegangssleutel van Dynamics 365 Business Central OData-webservice**|De toegangssleutel voor het gebruikersaccount dat de [!INCLUDE[crm_md](includes/crm_md.md)] gebruikt om informatie over artikelbeschikbaarheid uit [!INCLUDE[d365fin](includes/d365fin_md.md)] op te halen met de OData-webservice. De sleutel wordt toegewezen aan de gebruiker die is gekozen in het veld **Gebruikersnaam van Dynamics 365 Business Central OData-webservice**. Als u de sleutel wilt krijgen, kiest u de knop **Opzoekwaarde** naast de gebruikersnaam, kiest u de gebruiker, kiest u **Beheren** en klikt u vervolgens op **Bewerken**. Kies op de gebruikerskaart **Acties**, **Verificatie** en kies vervolgens **Sleutel van webservice wijzigen**|
|**Integratie van verkooporders inschakelen**|Wanneer personen verkooporders maken in [!INCLUDE[crm_md](includes/crm_md.md)], kopieert u de orders naar [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hiervoor moet u referenties opgeven voor een beheerdersaccount in [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie het gedeelte [Verkoopordergegevens verwerken](marketing-integrate-dynamicscrm.md#handling-sales-order-data).|
|**Dynamics 365 for Sales-verbinding inschakelen**|De verbinding met [!INCLUDE[crm_md](includes/crm_md.md)] inschakelen.|
|**Dynamics 365 SDK-versie**|Dit is alleen relevant als u integreert met een on-premises versie van [!INCLUDE[crm_md](includes/crm_md.md)]. Dit is de software-ontwikkelingskit van Dynamics 365 (ook Xrm genoemd) die u gebruikt om [!INCLUDE[d365fin](includes/d365fin_md.md)] te verbinden met [!INCLUDE[crm_md](includes/crm_md.md)]. De versie moet compatibel zijn met de SDK-versie die wordt gebruikt door [!INCLUDE[crm_md](includes/crm_md.md)] en gelijk zijn aan of nieuwer zijn dan de versie die wordt gebruikt door [!INCLUDE[crm_md](includes/crm_md.md)].|

> [!Note]
> De begeleide instelling **Dynamics 365 for Sales-verbinding instellen** wijst automatisch de beveiligingsrollen **Integratiebeheerder** en **Integratiegebruiker** toe aan het gebruikersaccount dat wordt gebruikt voor integratie. 

### <a name="to-create-or-maintain-the-connection-manually"></a>De verbinding handmatig maken of onderhouden
In de volgende procedure wordt beschreven hoe u de velden op de pagina **Microsoft Dynamics 365 for Sales-verbinding instellen** handmatig invult. Dit is ook de pagina waar u instellingen voor de integratie beheert.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Microsoft Dynamics 365-verbinding instellen** in en kies vervolgens de gerelateerde koppeling.
2. Voer de volgende gegevens in voor de verbinding van [!INCLUDE[d365fin](includes/d365fin_md.md)] met [!INCLUDE[crm_md](includes/crm_md.md)].

|Veld|Omschrijving|
|-----|-----|
|**Dynamics 365 for Sales-URL**|De URL voor uw exemplaar van [!INCLUDE[crm_md](includes/crm_md.md)]. Als u de URL wilt krijgen, opent u [!INCLUDE[crm_md](includes/crm_md.md)], kopieert u de URL vanaf de adresbalk in uw browser en plakt u de URL vervolgens in het veld. [!INCLUDE[d365fin](includes/d365fin_md.md)] zorgt dat de indeling klopt.|
|**Gebruikersnaam** en **Wachtwoord**|De referenties van het gebruikersaccount voor de integratie. Zie voor meer informatie [Gebruikersaccounts instellen voor integratie met Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md).|
|**Ingeschakeld**|Begin de integratie te gebruiken. Als u de verbinding niet nu inschakelt, worden de verbindingsinstellingen opgeslagen, maar hebben gebruikers geen toegang tot [!INCLUDE[crm_md](includes/crm_md.md)]-gegevens uit [!INCLUDE[d365fin](includes/d365fin_md.md)]. U kunt naar deze pagina terugkeren en de verbinding later inschakelen.  |
|**Dynamics 365 SDK-versie**|Als u integreert met een on-premises versie van [!INCLUDE[crm_md](includes/crm_md.md)], is dit de Dynamics 365-softwareontwikkelingskit (ook Xrm genoemd) die u gebruikt om [!INCLUDE[d365fin](includes/d365fin_md.md)] te verbinden met [!INCLUDE[crm_md](includes/crm_md.md)]. De versie die u selecteert moet compatibel zijn met de SDK-versie die wordt gebruikt door [!INCLUDE[crm_md](includes/crm_md.md)]. Deze versie is gelijk aan of nieuwer dan de versie die wordt gebruikt door [!INCLUDE[crm_md](includes/crm_md.md)].|

> [!Note]
> Als u een on-premises versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] verbindt met [!INCLUDE[crm_md](includes/crm_md.md)] en u een verbinding met een [!INCLUDE[crm_md](includes/crm_md.md)]-exemplaar wilt configureren met een specifiek verificatietype, vult u de velden op het sneltabblad **Gegevens van verificatietype** in. Zie voor meer informatie [Verbindingstekenreeken in XRM tooling gebruiken om verbinding te maken met Dynamics 365](https://go.microsoft.com/fwlink/?linkid=843055). Deze stap is niet vereist wanneer u verbinding maakt met een online versie van [!INCLUDE[d365fin](includes/d365fin_md.md)].

3. Voer de volgende gegevens in voor de verbinding van [!INCLUDE[crm_md](includes/crm_md.md)] met [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Veld|Omschrijving|
|-----|-----|
|**Dynamics 365 Business Central Webclient-URL**|De URL van uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-exemplaar. Hierdoor kunnen gebruikers in [!INCLUDE[crm_md](includes/crm_md.md)] bijbehorende records openen in [!INCLUDE[d365fin](includes/d365fin_md.md)] vanuit records in [!INCLUDE[crm_md](includes/crm_md.md)], zoals een account of product. De [!INCLUDE[d365fin](includes/d365fin_md.md)]-records worden geopend in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Stel dit veld in op de URL van het te gebruiken [!INCLUDE[d365fin](includes/d365fin_md.md)]-exemplaar.<br /><br /> Als u het veld opnieuw wilt instellen op de standaard-URL voor de [!INCLUDE[d365fin](includes/d365fin_md.md)], kiest u de actie **Webclient-URL opnieuw instellen**.<br /><br /> Dit veld is alleen van belang als de [!INCLUDE[d365fin](includes/d365fin_md.md)]-integratieoplossing is geïnstalleerd in [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Webservice Artikelbeschikbaarheid ingeschakeld**|Zorg dat personen die [!INCLUDE[crm_md](includes/crm_md.md)] gebruiken de beschikbaarheid van producten (artikelen) in voorraad in [!INCLUDE[d365fin](includes/d365fin_md.md)] kunnen bekijken. Als u dit inschakelt, moet u ook een gebruikersnaam en een toegangssleutel opgeven die de [!INCLUDE[crm_md](includes/crm_md.md)] moet gebruiken om bij de OData webservice te vragen naar beschikbaarheid van (artikelen). Zie voor meer informatie [OData-webservices](/dynamics365/business-central/dev-itpro/webservices/odata-web-services.md).|
|**URL van Dynamics 365 Business Central OData-webservice**|Als u de webservice Artikelbeschikbaarheid inschakelt, wordt de URL van de OData-webservice voor u verschaft.|
|**Gebruikersnaam van Dynamics 365 Business Central OData-webservice**|De naam van het gebruikersaccount dat de [!INCLUDE[crm_md](includes/crm_md.md)] gebruikt om informatie over artikelbeschikbaarheid in [!INCLUDE[d365fin](includes/d365fin_md.md)] op te halen met de OData-webservice.|
|**Toegangssleutel van Dynamics 365 Business Central OData-webservice**|De toegangssleutel voor het gebruikersaccount dat de [!INCLUDE[crm_md](includes/crm_md.md)] gebruikt om informatie over artikelbeschikbaarheid uit [!INCLUDE[d365fin](includes/d365fin_md.md)] op te halen met de OData-webservice. De sleutel wordt toegewezen aan de gebruiker die is gekozen in het veld **Gebruikersnaam van Dynamics 365 Business Central OData-webservice**. Als u de sleutel wilt krijgen, kiest u de knop **Opzoekwaarde** naast de gebruikersnaam, kiest u de gebruiker, kiest u **Beheren** en klikt u vervolgens op **Bewerken**. Kies op de gebruikerskaart **Acties**, **Verificatie** en kies vervolgens **Sleutel van webservice wijzigen**|

4. Voer de volgende instellingen in voor [!INCLUDE[crm_md](includes/crm_md.md)].

|Veld|Omschrijving|
|-----|-----|
|**Verkooporderintegratie is ingeschakeld**|Gebruikers de mogelijkheid bieden verkooporders en geactiveerde offertes in te dienen in [!INCLUDE[crm_md](includes/crm_md.md)] deze vervolgens weer te geven en te verwerken in [!INCLUDE[d365fin](includes/d365fin_md.md)].|
|**Automatisch verkooporders maken**|Maak een verkooporder in [!INCLUDE[d365fin](includes/d365fin_md.md)] wanneer een gebruiker er een maakt en indient in [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Verkoopoffertes automatisch verwerken**|Verwerk een verkoopofferte in [!INCLUDE[d365fin](includes/d365fin_md.md)] als een gebruiker er een maakt en activeert in [!INCLUDE[crm_md](includes/crm_md.md)].|

5. Voer de volgende geavanceerde instellingen in.

|Veld|Omschrijving|
|-----|-----|
|**[!INCLUDE[d365fin](includes/d365fin_md.md)]-gebruikers moeten worden toegewezen aan Dynamics 365 for Sales-gebruikers**|Geef op of [!INCLUDE[d365fin](includes/d365fin_md.md)]-gebruikersaccounts overeenkomstige gebruikersaccounts in [!INCLUDE[crm_md](includes/crm_md.md)] moeten hebben. Het **Office 365 e-mailadres voor verificatie** van de [!INCLUDE[d365fin](includes/d365fin_md.md)]-gebruiker moet hetzelfde zijn als het **Primaire e-mailadres** van de [!INCLUDE[crm_md](includes/crm_md.md)]-gebruiker.<br /><br /> Als u de waarde instelt op **Ja**, hebben [!INCLUDE[d365fin](includes/d365fin_md.md)]-gebruikers die geen overeenkomend [!INCLUDE[crm_md](includes/crm_md.md)]-gebruikersaccount hebben, geen [!INCLUDE[d365fin](includes/d365fin_md.md)]-integratiemogelijkheden in de gebruikersinterface. Toegang tot [!INCLUDE[crm_md](includes/crm_md.md)]-gegevens, direct vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt uitgevoerd namens het [!INCLUDE[crm_md](includes/crm_md.md)]-gebruikersaccount.<br /><br /> Als u de waarde instelt op **Nee**, hebben alle [!INCLUDE[d365fin](includes/d365fin_md.md)]-gebruikers [!INCLUDE[crm_md](includes/crm_md.md)]-integratiemogelijkheden in de gebruikersinterface. Toegang tot [!INCLUDE[crm_md](includes/crm_md.md)]-gegevens wordt uitgevoerd namens de gebruiker van de [!INCLUDE[crm_md](includes/crm_md.md)]-verbinding (integratie).|
|**Huidige Business Central-gebruiker is toegewezen aan een Dynamics 365 for Sales-gebruiker**|Geeft aan of uw gebruikersaccount is toegewezen aan een account in [!INCLUDE[crm_md](includes/crm_md.md)].|

6. Als u de verbindingsinstellingen wilt testen, kiest u **Verbinding testen**.  

    > [!NOTE]  
    >  Als gegevensversleuteling niet is ingeschakeld in [!INCLUDE[d365fin](includes/d365fin_md.md)], wordt u gevraagd of u het wilt inschakelen. Als u gegevensversleuteling wilt inschakelen, kiest u **Ja** en geeft u de vereiste informatie op. Anders kiest u **Nee**. U kunt gegevenscodering later inschakelen. Zie voor meer informatie [Gegevens versleutelen in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) in Help voor ontwikkelaars en IT-pro.  

7. Als [!INCLUDE[crm_md](includes/crm_md.md)]-synchronisatie niet al is ingesteld, wordt u gevraagd of u de standaardinstellingen voor synchronisatie wilt gebruiken. Afhankelijk van of u records uitgelijnd wilt houden in [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[d365fin](includes/d365fin_md.md)], kiest u **Ja** of **Nee**.

> [!Note]
> Voor het maken van verbinding met Dynamics 365 for Sales met behulp van **Microsoft Dynamics 365 for Sales-verbinding instellen** moet u mogelijk de beveiligingsrollen Integratiebeheerder en Integratiegebruiker toewijzen aan het gebruikersaccount dat wordt gebruikt voor integratie. Zie voor meer informatie [Een beveiligingsrol toewijzen aan een gebruiker](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user).


> [!Note]
> Voor het maken van verbinding met Dynamics 365 for Sales met behulp van **Microsoft Dynamics 365 for Sales-verbinding instellen** moet u mogelijk [de beveiligingsrollen **Integratiebeheerder** en **Integratiegebruiker** toewijzen](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user) aan gebruikersaccounts die worden gebruikt voor integratie.


### <a name="to-disconnect-from-includecrmmdincludescrmmdmd"></a>Verbinding met [!INCLUDE[crm_md](includes/crm_md.md)] verbreken  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Microsoft Dynamics 365 for Sales-verbinding instellen** in en kies vervolgens de gerelateerde koppeling.
2. Schakel op de pagina **Microsoft Dynamics 365 for Sales-verbinding instellen** het selectievakje **Ingeschakeld** uit.  

<!--## Install the [!INCLUDE[d365fin](includes/d365fin_md.md) Integration Solution
[!INCLUDE[d365fin](includes/d365fin_md.md)] includes a solution that enables users to access coupled records, such as customers and items, from records in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts and products. The solution adds a link to the pages in [!INCLUDE[crm_md](includes/crm_md.md)] to open the coupled [!INCLUDE[d365fin](includes/d365fin_md.md)] record. The solution also displays information from [!INCLUDE[d365fin](includes/d365fin_md.md)]on certain entities in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts. Installing this solution is optional. <!--"Solution" sounds old school. Is it an app, or an add-in, or an extension?


1.  From [!INCLUDE[d365fin](includes/d365fin_md.md)] installation media \(DVD\), copy the DynamicsNAVIntegrationSolution.zip file to your computer.  

     The DynamicsNAVIntegrationSolution.zip file is located in the **CrmCustomization** folder. This file is the solution package.   

2.  In [!INCLUDE[crm_md](includes/crm_md.md)], import the DynamicsNAVIntegrationSolution.zip as a solution.  

     This step adds the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity and **[!INCLUDE[d365fin](includes/d365fin_md.md) Account Statistics** entity in the system and additional items such as [!INCLUDE[d365fin](includes/d365fin_md.md)] integration security roles.  

     For more information about how to manage solutions in [!INCLUDE[crm_md](includes/crm_md.md)], [http://go.microsoft.com/fwlink/?LinkID=616519](http://go.microsoft.com/fwlink/?LinkID=616519).  

3.  Optional: Set up the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity to display in the **Settings** area of [!INCLUDE[crm_md](includes/crm_md.md)].  

     This enables [!INCLUDE[crm_md](includes/crm_md.md)] users who are assigned the **[!INCLUDE[d365fin](includes/d365fin_md.md) Admin** role to modify the entity in [!INCLUDE[crm_md](includes/crm_md.md)]. For more information about how to modify entities in [!INCLUDE[crm_md](includes/crm_md.md)], see [View or edit entity information](http://go.microsoft.com/fwlink/?LinkID=616521).  

4.  Assign the **[!INCLUDE[d365fin](includes/d365fin_md.md) Integration Administrator** role to the user account for the connection to [!INCLUDE[d365fin](includes/d365fin_md.md)].  

5.  Assign the **Business Central Integration User** role to all users who will use the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution.  

If you install the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution after you have set up the connection to [!INCLUDE[crm_md](includes/crm_md.md)] in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must modify the connection setup to point to the URL.-->

<!--of the [!INCLUDE[nav_web_md](../developer/includes/nav_web_md.md)]. For more information, see [How to: Set Up a Microsoft Dynamics 365 for Sales Connection]() -->

<!--
# View Item Availability - Support Matrix
For most versions of [!INCLUDE[d365fin](includes/d365fin_md.md) and Dynamics 365 for Sales, you can view availability figures for items across the integrated products. The following table shows which version combinations support viewing item availability.

| |Dynamics 365 for Sales version|2015/Update 1/Online|2016/Update 1/Online|Dynamics 365 for Sales|
|-|---------------------|---------------------|--------------------------|-----------------|
|**Dynamics NAV version**|
|**2016**||Not supported|Not supported|Not supported|
|**2017**||Not supported - Install from 2016|Supported|Supported|
|**Dynamics 365 for Financials**||Not supported - Install from 2016|Supported|Supported|


> [Note]
> You can obtain item availability support for combinations of Dynamics CRM 2015 and Business Central by running the DynamicsNAVIntegrationSolution.zip file on the Business Central product DVD.

For more information, see [System Requirements for Business Central](../deployment/system-requirement-business-central.md).

-->

## <a name="see-also"></a>Zie ook  
[De status van een synchronisatie weergeven](admin-how-to-view-synchronization-status.md)  
