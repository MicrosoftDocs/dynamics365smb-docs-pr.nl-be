---
title: Verbinden met Common Data Service | Microsoft Docs
description: U kunt via Common Data Service andere apps integreren met Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/30/2020
ms.author: bholtorf
ms.openlocfilehash: 4c57d8c79f91319675527f514b01b6ddeb83e722
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3529225"
---
# <a name="connect-to-common-data-service"></a>Verbinding maken met Common Data Service
In dit onderwerp wordt beschreven hoe u een verbinding tot stand brengt tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[d365fin](includes/cds_long_md.md)]. Bedrijven maken doorgaans de verbinding om gegevens te integreren en te synchroniseren met een andere Dynamics 365-bedrijfsapp, zoals [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Voordat u begint
Voordat u de verbinding maakt, moet u een aantal gegevens gereed hebben:  

* De URL van de [!INCLUDE[d365fin](includes/cds_long_md.md)]-omgeving waarmee u verbinding wilt maken. Als u de begeleide instelling **CDS-verbinding instellen** gebruikt om de verbinding tot stand te brengen, ontdekken we uw omgevingen, maar u kunt ook de URL van een andere omgeving in uw tenant invoeren.  
* De gebruikersnaam en het wachtwoord van een account dat beheerdersmachtigingen heeft in [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[d365fin](includes/cds_long_md.md)].  

> [!Note]
> Deze stappen beschrijven de procedure voor de online versie van [!INCLUDE[d365fin](includes/d365fin_md.md)].
> Als u Business Central on-premises gebruikt en geen Azure Active Directory-account gebruikt om verbinding te maken met Common Data Service, moet u ook een gebruikersnaam en wachtwoord van een gebruikersaccount opgeven voor de integratie. Dit account wordt de 'integratiegebruiker' genoemd. Als u een Azure Active Directory-account gebruikt, is het gebruikersaccount voor integratie niet vereist of weergegeven. De integratiegebruiker wordt automatisch ingesteld en heeft geen licentie nodig.

## <a name="set-up-a-connection-to-d365fin"></a>Een verbinding instellen met [!INCLUDE[d365fin](includes/cds_long_md.md)]  
Voor alle verificatiesoorten anders dan Office 365-verificatie stelt u de verbinding met [!INCLUDE[d365fin](includes/cds_long_md.md)] in op de pagina **CDS-verbinding instellen**. Het is raadzaam de begeleide instelling **Common Data Service-verbinding instellen** te gebruiken voor Office 365-verificatie. De begeleide instelling maakt het gemakkelijker om de verbinding in te stellen en geavanceerde functies op te geven, zoals het eigendomsmodel en initiële synchronisatie.  

> [!Important]
> Tijdens het instellen van de verbinding met [!INCLUDE[d365fin](includes/cds_long_md.md)] wordt de beheerder gevraagd om de volgende machtigingen te geven aan de geregistreerde Azure-toepassing met de naam [!INCLUDE[d365fin](includes/d365fin_md.md)]-integratie met [!INCLUDE[d365fin](includes/cds_long_md.md)]:
> * De machtiging **Toegang tot [!INCLUDE[d365fin](includes/cds_long_md.md)] krijgen als uzelf** is nodig, dus kan [!INCLUDE[d365fin](includes/d365fin_md.md)] namens de beheerder automatisch een niet-gelicentieerde niet-interactieve gebruiker van de [!INCLUDE[d365fin](includes/d365fin_md.md)]-integratietoepassing maken, beveiligingsrollen toewijzen aan deze gebruiker en [!INCLUDE[d365fin](includes/d365fin_md.md)] Basis-CDS-integratieoplossing implementeren naar [!INCLUDE[d365fin](includes/cds_long_md.md)]. Deze toestemming wordt slechts één keer gebruikt tijdens het instellen van de verbinding met [!INCLUDE[d365fin](includes/cds_long_md.md)]. 
> * De machtiging **Volledige toegang tot Dynamics 365 [!INCLUDE[d365fin](includes/d365fin_md.md)]** hebben is nodig zodat de automatisch gemaakte gebruiker van de [!INCLUDE[d365fin](includes/d365fin_md.md)]-integratietoepassing toegang tot [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens kan krijgen die worden gesynchroniseerd. 
> * De machtiging **Aanmelden en uw profiel lezen** is nodig om te verifiëren dat de gebruiker die zich aanmeldt de beveiligingsrol Systeembeheerder toegewezen heeft gekregen in [!INCLUDE[d365fin](includes/cds_long_md.md)]. 
>
> Door namens de organisatie toestemming te geven geeft de beheerder de geregistreerde Azure-toepassing genaamd [!INCLUDE[d365fin](includes/d365fin_md.md)]-integratie met [!INCLUDE[d365fin](includes/cds_long_md.md)] het recht gegevens te synchroniseren met de referenties van de automatisch gemaakte gebruiker van de [!INCLUDE[d365fin](includes/d365fin_md.md)]-integratietoepassing.

### <a name="to-use-the-set-up-common-data-service-connection-assisted-setup-guide"></a>De begeleide instelling Common Data Service-verbinding instellen gebruiken 
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Begeleide instelling** in en kies de gerelateerde koppeling.
2. Kies **Common Data Service-verbinding instellen** om de begeleide instelling te starten.
3. Vul de vereiste velden in.

### <a name="to-create-or-maintain-the-connection-manually"></a>De verbinding handmatig maken of onderhouden
In de volgende procedure wordt beschreven hoe u de verbinding op de pagina **CDS-verbinding instellen** handmatig instelt. Dit is ook de pagina waar u instellingen voor de integratie beheert.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **CDS-verbinding instellen** in en kies de gerelateerde koppeling.
2. Voer de volgende gegevens in voor de verbinding van [!INCLUDE[d365fin](includes/d365fin_md.md)] met [!INCLUDE[d365fin](includes/cds_long_md.md)].

|Veld|Omschrijving|
|-----|-----|
|**Omgevings-URL**|Als u eigenaar bent van omgevingen in [!INCLUDE[d365fin](includes/cds_long_md.md)], vinden we die voor u wanneer u de instelling uitvoert. Als u verbinding wilt maken met een andere omgeving in een andere tenant, kunt u de beheerdersreferenties voor de omgeving invoeren en zullen we die ontdekken. |
|**Ingeschakeld**|Begin de integratie te gebruiken. Als u de verbinding niet nu inschakelt, worden de verbindingsinstellingen opgeslagen, maar hebben gebruikers geen toegang tot [!INCLUDE[d365fin](includes/cds_long_md.md)]-gegevens uit [!INCLUDE[d365fin](includes/d365fin_md.md)]. U kunt naar deze pagina terugkeren en de verbinding later inschakelen.  |

3. Kies in het veld **Eigendomsmodel** of u wilt dat een teamentiteit in [!INCLUDE[d365fin](includes/cds_long_md.md)] eigenaar is van nieuwe records of een of meer specifieke gebruikers. Als u **Persoon** kiest, moet u elke gebruiker opgeven. Als u **Team** kiest, wordt de standaardbedrijfsunit BCI_bedrijf weergegeven in het veld **Gekoppelde bedrijfsunit**.

<!--Need to verify the details in this table, are these specific to Sales maybe?
Enter the following advanced settings.

|Field|Description|
|-----|-----|
|**[!INCLUDE[d365fin](includes/d365fin_md.md)] Users Must Map to CDS Users**|If you are using the Person ownership model, specify whether [!INCLUDE[d365fin](includes/d365fin_md.md)] user accounts must have a matching user accounts in [!INCLUDE[d365fin](includes/cds_long_md.md)]. The **Office 365 Authentication Email** of the [!INCLUDE[d365fin](includes/d365fin_md.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[d365fin](includes/d365fin_md.md)] users who do not have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account will not have [!INCLUDE[d365fin](includes/d365fin_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[d365fin](includes/d365fin_md.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[d365fin](includes/d365fin_md.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
|**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] <!--double check the name of this field|-->

4. Als u de verbindingsinstellingen wilt testen, kiest u **Verbinding** en vervolgens **Verbinding testen**.  

    > [!NOTE]  
    >  Als gegevensversleuteling niet is ingeschakeld in [!INCLUDE[d365fin](includes/d365fin_md.md)], wordt u gevraagd of u het wilt inschakelen. Als u gegevensversleuteling wilt inschakelen, kiest u **Ja** en geeft u de vereiste informatie op. Anders kiest u **Nee**. U kunt gegevenscodering later inschakelen. Zie voor meer informatie [Gegevens versleutelen in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) in de Help voor ontwikkelaars en beheerders.  

5. Als [!INCLUDE[d365fin](includes/cds_long_md.md)]-synchronisatie niet al is ingesteld, wordt u gevraagd of u de standaardinstellingen voor synchronisatie wilt gebruiken. Afhankelijk van of u records uitgelijnd wilt houden in [!INCLUDE[d365fin](includes/cds_long_md.md)] en [!INCLUDE[d365fin](includes/d365fin_md.md)], kiest u **Ja** of **Nee**.

## <a name="connecting-on-premises-versions"></a>Verbinding maken met on-premises versies
Als u [!INCLUDE[d365fin](includes/d365fin_md.md)] on-premises wilt verbinden met [!INCLUDE[d365fin](includes/cds_long_md.md)], moet u wat informatie opgeven op de pagina **Common Data Service-verbinding instellen**.

Als u verbinding wilt maken met een Azure Active Directory (Azure AD)-account, moet u een toepassing registreren in Azure AD en de toepassings-id, het sleutelkluisgeheim en de omleidings-URL opgeven die moeten worden gebruikt. De omleidings-URL wordt vooraf ingevuld en zou voor de meeste installaties moeten werken. U moet uw installatie instellen om HTTPS te gebruiken. Zie voor meer informatie [SSL configureren om de Business Central Web Client-verbinding te beveiligen](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Als u uw server instelt om een andere startpagina te hebben, kunt u altijd de URL wijzigen. Het clientgeheim wordt opgeslagen als een versleutelde tekenreeks in uw database. 

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-common-data-service"></a>Een toepassing registreren in Azure AD voor verbinding van Business Central met Common Data Service
Bij de volgende stappen wordt ervan uitgegaan dat u Azure AD gebruikt om identiteiten en toegang te beheren. Voor meer informatie over het registreren van een toepassing in Azure AD raadpleegt u [Quickstart: een toepassing registreren bij het Microsoft-identiteitsplatform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app). Als u Azure AD niet gebruikt, raadpleegt u [Een andere identiteits- en toegangsbeheerservice gebruiken](admin-how-to-set-up-a-dynamics-crm-connection.md#using-another-identity-and-access-management-service). 

1. Kies in de Azure Portal onder **Beheren** in het navigatiedeelvenster **Verificatie**. 
2. Voeg onder **URL's omleiden** de omleidings-URL toe die wordt voorgesteld op de pagina **Common Data Service-verbinding instellen** in [!INCLUDE[d365fin](includes/d365fin_md.md)].
3. Kies **Beheren** **API-machtigingen**.
4. Kies onder **Geconfigureerde machtigingen** **Een machtiging toevoegen** en voeg daarna als volgt gedelegeerde machtigingen toe aan het tabblad **Microsoft-API's**:
    * Voeg voor Business Central de machtiging **Financials.ReadWrite.All** toe.
    * Voeg voor Dynamics CRM de **user-impersonation**-machtigingen toe. 

> [!NOTE]
> De naam van de Dynamics CRM-API kan veranderen.

5.  Kies onder **Beheren** **Certificaten en geheimen** en maak vervolgens een nieuw geheim voor uw app. U gebruikt het geheim in [!INCLUDE[d365fin](includes/d365fin_md.md)], in het veld **Clientgeheim** op de pagina **Common Data Service-verbinding instellen** of slaat het op een veilige locatie op en verschaft het in een gebeurtenisabonnee zoals eerder in dit onderwerp beschreven.
6. Kies **Overzicht** en zoek de waarde **Toepassing (client)-id**. Dit is de client-id van uw toepassing. U moet het invoeren op de pagina **Common Data Service-verbinding instellen** in het veld **Client-id** of bewaren op een veilige locatie en verschaffen in een gebeurtenisabonnee.
7. Voer in [!INCLUDE[d365fin](includes/d365fin_md.md)] op de pagina **Common Data Service-verbinding instellen** in het veld **Omgeving-URL** de URL voor uw [!INCLUDE[d365fin](includes/cds_long_md.md)]-omgeving in.
8. Als u de verbinding met [!INCLUDE[d365fin](includes/cds_long_md.md)] wilt inschakelen, zet u de schakelaar **Ingeschakeld** aan.
9. Meld u aan met uw beheerdersaccount voor Azure Active Directory (dit account moet een geldige licentie hebben voor [!INCLUDE[d365fin](includes/cds_long_md.md)] en een beheerder zijn in uw [!INCLUDE[d365fin](includes/cds_long_md.md)]-omgeving). Nadat u zich hebt aangemeld, wordt u gevraagd toe te staan dat uw geregistreerde toepassing zich aanmeldt bij [!INCLUDE[d365fin](includes/cds_long_md.md)] namens de organisatie. U moet toestemming geven om de instelling te voltooien.

   > [!NOTE]
   > Als u niet wordt gevraagd om u aan te melden met uw beheerdersaccount, komt dit waarschijnlijk omdat pop-ups worden geblokkeerd. Sta pop-ups vanaf https://login.microsoftonline.com toe om u aan te melden.

#### <a name="using-another-identity-and-access-management-service"></a>Een andere identiteits- en toegangsbeheerservice gebruiken
Als u Azure Active Directory niet gebruikt om identiteiten en toegang te beheren, hebt u wat hulp nodig van een ontwikkelaar. Als u de app-id en het geheim liever op een andere locatie opslaat, kunt u de velden Client-id en Clientgeheim leeg laten en een extensie schrijven om de id en het geheim van de locatie op te halen. U kunt het geheim tijdens runtime verstrekken door u te abonneren op de gebeurtenissen OnGetCDSConnectionClientId en OnGetCDSConnectionClientSecret in codeunit 7201 'CDS Integration Impl.'

### <a name="to-disconnect-from-d365fin"></a>Verbinding met [!INCLUDE[d365fin](includes/cds_long_md.md)] verbreken  
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **CDS-verbinding instellen** in en kies de gerelateerde koppeling.
2. Schakel op de pagina **CDS-verbinding instellen** de schakelaar **Geactiveerd** uit.  

## <a name="see-also"></a>Zie ook  
[De status van een synchronisatie weergeven](admin-how-to-view-synchronization-status.md)  
