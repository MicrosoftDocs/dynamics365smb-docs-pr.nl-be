---
title: OneDrive-integratie met Business Central beheren
description: Meer informatie over wat u kunt doen om integratie tussen Business Central en OneDrive te beheren.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'OneDrive, share, browser'
ms.date: 02/28/2022
ms.author: jswymer
---
# <a name="managing-onedrive-integration-with-business-central"></a><a name="managing-onedrive-integration-with-business-central"></a>OneDrive-integratie met Business Central beheren

Dit artikel geeft een overzicht van wat een beheerder kan doen om OneDrive-integratie met [!INCLUDE[prod_short](includes/prod_short.md)] te beheren. [!INCLUDE[prod_short](includes/prod_short.md)] online-klanten profiteren van automatische integratie, zonder dat er extra instellingen nodig zijn om de functies Openen in OneDrive en Delen te gebruiken. Met de begeleide instelling **Configuratie van OneDrive** kunt u gebruikers toegang geven tot nog meer OneDrive-functies, zoals het openen van een Excel-bestand in OneDrive&mdash;of zelfs het uitschakelen van alle functies.  

## <a name="configure-onedrive-for-integration-with-business-central"></a><a name="configure-onedrive-for-integration-with-business-central"></a>OneDrive configureren voor integratie met Business Central

In dit gedeelte worden de vereisten besproken waaraan moet worden voldaan in OneDrive voor Bedrijven om de integratie met Business Central te configureren en de taak die u kunt uitvoeren om de integratie te beheren.

### <a name="minimum-requirements"></a><a name="minimum-requirements"></a>Minimumvereisten

* Elke gebruiker moet een licentie hebben voor [!INCLUDE[prod_short](includes/prod_short.md)] en OneDrive als onderdeel van een Microsoft 365-abonnement.
* OneDrive moet voor elke gebruiker worden ingesteld.

### <a name="managing-privacy"></a><a name="managing-privacy"></a>Privacy beheren

> [!IMPORTANT]
> Als u ervoor hebt gekozen om Business Central en OneDrive voor verschillende landen of regio's te implementeren, kunnen de bestanden die zijn gegenereerd door Business Central en in OneDrive zijn geplaatst, de grenzen van gegevensresidentie overschrijden. Zorg ervoor dat u het beleid van uw organisatie en de nalevingsvereisten van de overheid voor gegevensresidentie bevestigt voordat u de verbinding met OneDrive inschakelt.

Beheerders en eindgebruikers beheren de inhoud die is opgeslagen in OneDrive en deze gegevens zijn uitsluitend eigendom van uw organisatie. Voor meer informatie zie [Hoe SharePoint en OneDrive uw gegevens in de cloud beveiligen](/sharepoint/safeguarding-your-data). U kunt ook een bezoek brengen aan onze [Privacyverklaring van Microsoft](https://privacy.microsoft.com/en-us/privacystatement), waarin wordt uitgelegd welke gegevens Microsoft verwerkt, hoe Microsoft deze verwerkt en voor welke doeleinden.

Door deze serviceverbinding in te schakelen gaat u akkoord met het volgende:

(a) om gegevens uit Dynamics 365 Business Central te delen met de serviceprovider, die ze gebruikt op basis van eigen voorwaarden en privacybeleid; (b) de nalevingsniveaus van de serviceprovider kunnen verschillen van Dynamics 365 Business Central; en (c) Microsoft kan uw contactgegevens met deze serviceprovider delen als dit nodig is om de service te gebruiken en er problemen mee op te lossen.

## <a name="configure-business-central"></a><a name="configure-business-central"></a>Business Central configureren

Met Business Central online wordt de verbinding tussen Business Central en OneDrive automatisch voor u geconfigureerd en zijn de OneDrive-functies standaard direct beschikbaar voor gebruikers. Als u sommige of alle functies wilt uitschakelen, kunt u de begeleide instelling **Configuratie van OneDrive** in de Business Central-client gebruiken.

Het configureren van Business Central on-premises is anders omdat de verbinding tussen Business Central en OneDrive niet voor u is geconfigureerd. U moet dit handmatig doen. Zie voor meer informatie [OneDrive-integratie met Business Central On-Premises configureren](admin-onedrive-integration-onpremises.md).

### <a name="about-multiple-environments"></a><a name="about-multiple-environments"></a>Informatie over meerdere omgevingen

OneDrive-integratie wordt per omgeving geconfigureerd, dat wil zeggen dat uw instellingen gelden voor alle bedrijven in die omgeving. Als uw organisatie meer dan één omgeving heeft, moet u OneDrive-integratie voor elke omgeving configureren.

### <a name="prerequisites"></a><a name="prerequisites"></a>Vereisten

- Minimaal imd-machtiging (indirect, modify, delete) voor tabel **Documentservicescenario**

### <a name="configure-onedrive-using-onedrive-setup"></a><a name="configure-onedrive-using-onedrive-setup"></a>OneDrive configureren met Configuratie van OneDrive

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Configuratie van OneDrive** in en kies vervolgens de gerelateerde koppeling. 
2. De eerste keer dat u de begeleide instelling uitvoert, ziet u **Uw privacy**. Lees de informatie op de pagina, en als u akkoord gaat met de voorwaarden, kiest u **Akkoord** om door te gaan.
3. Op de pagina **Bestandsverwerking configureren** hebt u de volgende opties om uit te kiezen:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]
4. Kies **Volgende**>**Gereed**.

### <a name="switching-to-new-onedrive-integration-after-upgrade"></a><a name="switching-to-new-onedrive-integration-after-upgrade"></a>Overschakelen naar nieuwe OneDrive-integratie na upgrade

De begeleide instelling **Configuratie van OneDrive** is geïntroduceerd in releasewave 2 van 2022, versie 21.0. Voorheen maakte de OneDrive-integratie gebruik van **Instellingen SharePoint-verbinding**. Deze optie is verouderd en wordt in releasewave 2 van 2023, versie 23.0 verwijderd. Nadat u een upgrade naar versie 21 hebt uitgevoerd, werkt OneDrive nog steeds zoals voorheen. Maar we raden u aan over te schakelen naar de nieuwe OneDrive-integratie. Als u deze overstap nu maakt, wordt het gemakkelijker wanneer **Instellingen SharePoint-verbinding** uiteindelijk wordt verwijderd. Bovendien kunt u dan de begeleide instelling **Configuratie van OneDrive** gebruiken voor het beheren van de OneDrive-functies die toegankelijk zijn voor gebruikers. Met de begeleide instelling **Configuratie van OneDrive** verloopt de overgang van de oude SharePoint-instelling eenvoudig en naadloos.

Om over te schakelen opent u de begeleide instelling **Configuratie van OneDrive** en voert u deze direct uit. U kunt ook de pagina **Instellingen SharePoint-verbinding** openen en **Ga naar nieuwe OneDrive-instelling** kiezen in de melding bovenaan de pagina. Volg de begeleide instelling zoals beschreven in het vorige gedeelte.

## <a name="restoring-onedrive-and-"></a><a name="restoring-onedrive-and-"></a>OneDrive en [!INCLUDE[prod_short](includes/prod_short.md)] herstellen

Als onderdeel van een noodhersteloefening moeten beheerders mogelijk een [!INCLUDE[prod_short](includes/prod_short.md)] online-omgeving herstellen naar een back-up van een moment in het verleden, en OneDrive-opslag synchroniseren tot datzelfde tijdstip. OneDrive biedt verschillende hersteltools, zoals het herstellen van OneDrive van een gebruiker naar een eerdere tijd, het herstellen een eerdere versie van een afzonderlijk bestand of het herstellen van verwijderde bestanden. Zie de volgende artikelen voor meer informatie:

* Zie voor [!INCLUDE[prod_short](includes/prod_short.md)] [Een omgeving herstellen in het beheercentrum](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).
* Zie voor OneDrive [Uw OneDrive herstellen](https://support.microsoft.com/en-us/office/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15?ui=en-us&rs=en-us&ad=us)

## <a name="governance"></a><a name="governance"></a>Bestuur

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

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Business Central en integratie met OneDrive voor Bedrijven](across-onedrive-overview.md)  
[Business Central-bestanden openen in OneDrive](across-share-onedrive.md)  
[Veelgestelde vragen over OneDrive](admin-onedrive-faq.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
