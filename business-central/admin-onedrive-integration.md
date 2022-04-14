---
title: OneDrive-integratie met Business Central beheren
description: Meer informatie over wat u kunt doen om integratie tussen Business Central en OneDrive te beheren.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OneDrive, share, browser
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: 7f630f8c13f692889f1d8526698d42633c42a4ee
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8514607"
---
# <a name="managing-onedrive-integration-with-business-central"></a>OneDrive-integratie met Business Central beheren

Dit artikel geeft een overzicht van wat een beheerder kan doen om OneDrive-integratie met [!INCLUDE[prod_short](includes/prod_short.md)] te beheren. [!INCLUDE[prod_short](includes/prod_short.md)] online-klanten profiteren van automatische integratie, zonder dat er extra instellingen nodig zijn om deze functies te gebruiken. 

## <a name="minimum-requirements"></a>Minimumvereisten

* Elke gebruiker moet een licentie hebben voor [!INCLUDE[prod_short](includes/prod_short.md)] en OneDrive als onderdeel van een Microsoft 365-abonnement.
* OneDrive moet voor elke gebruiker worden ingesteld.

## <a name="governance"></a>Bestuur

Het SharePoint-beheercentrum biedt uitgebreide controle over het beleid dat het gebruik van OneDrive door de hele organisatie bepaalt. Globale beheerders of gebruikers met de SharePoint-beheerdersrol kunnen beleid instellen dat bepaalt wie toegang heeft tot OneDrive, waar gegevens zich bevinden, de levenscyclus van content en nog veel meer. De volgende koppelingen geven informatie over veelgebruikte functies en instellingen die uw integratie met [!INCLUDE[prod_short](includes/prod_short.md)] kunnen verbeteren. 

* [Instellingen voor delen beheren](/sharepoint/turn-external-sharing-on-or-off)
* [Informatiebarrières gebruiken met SharePoint](/sharepoint/information-barriers)
* [Meer informatie over het voorkomen van gegevensverlies](/microsoft-365/compliance/dlp-learn-about-dlp)
* [De standaardopslagruimte instellen voor OneDrive-gebruikers](/onedrive/set-default-storage-space)
* [Beheerders voor OneDrive van een gebruiker toevoegen en verwijderen](/sharepoint/manage-user-profiles#add-and-remove-admins-for-a-users-onedrive)
* [Maken van OneDrive uitschakelen voor sommige gebruikers](/sharepoint/manage-user-profiles#disable-onedrive-creation-for-some-users)
* [Multiregiomogelijkheden in OneDrive en SharePoint Online](/microsoft-365/enterprise/multi-geo-capabilities-in-onedrive-and-sharepoint-online-in-microsoft-365)

> [!NOTE]
> Sommige functies zijn mogelijk alleen beschikbaar voor specifieke abonnementen.

## <a name="managing-privacy"></a>Privacy beheren

Beheerders en eindgebruikers beheren de inhoud die is opgeslagen in OneDrive en deze gegevens zijn uitsluitend eigendom van uw organisatie. Voor meer informatie zie [Hoe SharePoint en OneDrive uw gegevens in de cloud beveiligen](/sharepoint/safeguarding-your-data). U kunt ook een bezoek brengen aan onze [Privacyverklaring van Microsoft](https://privacy.microsoft.com/en-us/privacystatement), waarin wordt uitgelegd welke gegevens Microsoft verwerkt, hoe Microsoft deze verwerkt en voor welke doeleinden.

## <a name="restoring-onedrive-and-prod_short"></a>OneDrive en [!INCLUDE[prod_short](includes/prod_short.md)] herstellen

Als onderdeel van een noodhersteloefening moeten beheerders mogelijk een [!INCLUDE[prod_short](includes/prod_short.md)]-omgeving herstellen naar een back-up van een moment in het verleden, en OneDrive-opslag synchroniseren tot datzelfde tijdstip. OneDrive biedt hiervoor verschillende tools, zoals het herstellen van OneDrive van een gebruiker naar een eerdere tijd, een eerdere versie van een afzonderlijk bestand herstellen of verwijderde bestanden herstellen. Zie de volgende artikelen voor meer informatie:

* Zie voor [!INCLUDE[prod_short](includes/prod_short.md)] [Een omgeving herstellen in het beheercentrum](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).
* Zie voor OneDrive [Uw OneDrive herstellen](https://support.microsoft.com/en-us/office/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15?ui=en-us&rs=en-us&ad=us)

## <a name="configuring-business-central-on-premises"></a>Business Central On-Premises configureren

Een beheerder moet de verbinding opzetten tussen [!INCLUDE[prod_short](includes/prod_short.md)] on premises en OneDrive. In tegenstelling tot [!INCLUDE[prod_short](includes/prod_short.md)] online is de verbinding niet automatisch. Als de verbinding niet is geconfigureerd, kunnen gebruikers de functies niet gebruiken voor OneDrive. 

[!INCLUDE[prod_short](includes/prod_short.md)] on-premises kan alleen worden verbonden met OneDrive gehost door Microsoft in de cloud. [!INCLUDE[prod_short](includes/prod_short.md)] on premises verbinden met de My Sites-opslag van SharePoint Server wordt niet ondersteund.

> [!IMPORTANT]
> Door deze functie te configureren schakelt u ook oudere functies in die bestanden verzenden naar OneDrive.  
>
>* De functie Openen in Excel kopieert het Excel-bestand automatisch naar OneDrive en opent het vervolgens in Excel Online. 
>* Als u een rapport naar een bestand exporteert, wordt het bestand automatisch gekopieerd naar OneDrive en vervolgens geopend in Excel Online, Word Online of OneDrive. 
>* Andere functies kunnen ook automatisch worden geopend in OneDrive.

### <a name="to-prepare-prod_short-on-premises-for-connecting-to-onedrive"></a>[!INCLUDE[prod_short](includes/prod_short.md)] on-premises voorbereiden om verbinding te maken met OneDrive

<!-- 
1. For the best experience Configure Azure Active Directory (AD) authentication.

   For more information, see [Authenticating Business Central Users with Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory)-->

Voeg een geregistreerde toepassing voor Business Central toe aan uw Azure AD-tenant van uw Microsoft 365-abonnement. Net als andere Azure-services die werken met Business Central, vereist OneDrive een app-registratie in Azure Active Directory (Azure AD). De app-registratie biedt verificatie- en autorisatieservices tussen Business Central en SharePoint, wat wordt gebruikt door OneDrive.

Configureer de geregistreerde toepassing met de volgende gedelegeerde machtigingen voor de SharePoint API:

- AllSites.FullControl
- User.ReadWrite.All 

Stel in plaats daarvan de volgende machtigingen in voor Business Central 2021 releasewave 2 (versie 19):

- AllSites.Write
- MyFiles.Write
- User.Read.All 

Dit werk doet u in de Azure Portal. Zorg ervoor dat u de toepassings-id (client-id) en het clientgeheim kopieert die door de geregistreerde toepassing worden gebruikt. U hebt deze informatie nodig bij de volgende taak.

Voor meer informatie over het registreren van een applicatie en het configureren van machtigingen zie [Een toepassing registreren in Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) in de help van ontwikkelaars en IT-professionals.

> [!TIP]
> Als u al een toepassing hebt geregistreerd als onderdeel van een integratie met een ander Microsoft-product, zoals Power BI, dan kunt u die app-registratie opnieuw gebruiken. In dit geval hoeft u alleen de SharePoint-rechten in te stellen.

### <a name="to-set-up-the-connection-in-prod_short-on-premises"></a>De verbinding instellen in [!INCLUDE[prod_short](includes/prod_short.md)] on premises

<!--
> [!NOTE]
> This requires the following types of authentication credentials:
>
> * Windows
> * NavUserPassword
> * Azure Active Directory
-->
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instellingen Microsoft SharePoint-verbinding** in en kies vervolgens de gerelateerde koppeling.
2. Voer in het veld **Omschrijving** een omschrijving in voor de verbinding, zoals **OneDrive**.
3. Voer in het veld **Map** **Business Central** in.
4. Voer in het veld **Locatie** de URL in voor uw OneDrive.

    De URL voor OneDrive is meestal in het volgende formaat: `https://<tenant name>-my.sharepoint.com`. Voor meer informatie zie [OneDrive-URL's voor gebruikers in uw organisatie](/onedrive/list-onedrive-urls) in de OneDrive-documentatie.
5. Voer in het veld **Client-id** de client-id van uw toepassingsregistratie in.
6. Voer in het veld **Clientgeheim** het geheim van uw toepassingsregistratie in. 
   <!-- 
   For information about how to find the URLs, see the following:
   * [How to find your SharePoint server URL]
   * [How to find your OneDrive URL]-->

> [!IMPORTANT]
> De pagina Instellingen SharePoint-verbinding wordt gebruikt om meerdere verouderde functies te configureren. De sectie **Algemeen** configureert de verbinding met OneDrive en de sectie **Gedeelde documenten** leidt bestanden om naar SharePoint. De oude SharePoint-functie zal in de nabije toekomst worden beëindigd. We raden u aan de sectie **Gedeelde documenten** te gebruiken.

## <a name="see-also"></a>Zie ook
[Business Central en integratie met OneDrive voor Bedrijven](across-onedrive-overview.md)  
[Business Central-bestanden openen in OneDrive](across-share-onedrive.md)  
[Veelgestelde vragen over OneDrive](admin-onedrive-faq.md)

