---
title: OneDrive-integratie configureren met Business Central On-Premises
description: Meer informatie over het instellen van Business Central On-Premises voor integratie met OneDrive voor Bedrijven.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'OneDrive, share, browser'
ms.date: 12/12/2023
ms.author: jswymer
---
# <a name="configuring-onedrive-integration-with-business-central-on-premises"></a>OneDrive-integratie configureren met Business Central On-Premises

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

In dit artikel wordt uitgelegd hoe u OneDrive-integratie kunt configureren met Business Central On-Premises. In tegenstelling tot [!INCLUDE[prod_short](includes/prod_short.md)] online wordt de verbinding tussen Business Central en OneDrive voor Bedrijven niet automatisch ingesteld. Als de verbinding niet is geconfigureerd, kunnen gebruikers de functies niet gebruiken voor OneDrive.

Er zijn twee taken die moeten worden uitgevoerd om de OneDrive-integratie te configureren.

- De eerste taak betreft het registreren van een toepassing (app) op uw Microsoft Entra-tenant van uw Microsoft 365-abonnement. De geregistreerde app wordt gebruikt voor verificatiedoeleinden. Deze taak wordt meestal uitgevoerd in de Azure-portal en in de Business Central-webclient.
- De tweede taak betreft het instellen van de verbinding met de OneDrive-URL en het inschakelen van de OneDrive-functies in Business Central. Deze taak wordt uitgevoerd in de Business Central-webclient. Voor versie 21 wordt dit anders gedaan dan voor versies 19 en 20. Versie 21 introduceert de optie **Configuratie van OneDrive** waarmee **Instellingen SharePoint-verbinding** wordt vervangen.  

> [!IMPORTANT]
> [!INCLUDE[prod_short](includes/prod_short.md)] on-premises kan alleen worden verbonden met OneDrive gehost door Microsoft in de cloud. [!INCLUDE[prod_short](includes/prod_short.md)] on premises verbinden met de My Sites-opslag van SharePoint Server wordt niet ondersteund.

## <a name="register-an-app-in-microsoft-entra-id-for-onedrive-integration"></a><a name="registerapp"></a>Een app in Microsoft Entra ID registreren voor OneDrive-integratie

In deze taak voegt u een geregistreerde app voor Business Central toe in de Microsoft Entra-tenant van uw Microsoft 365-abonnement. Net als andere Azure-services die werken met Business Central, vereist OneDrive een geregistreerde app in Microsoft Entra ID. De geregistreerde app biedt verificatie- en autorisatieservices tussen Business Central en SharePoint, wat wordt gebruikt door OneDrive.

Zie voor gedetailleerde stappen voor het voltooien van deze stap [Een toepassing registreren in Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) in de Help voor ontwikkelaars en IT-professionals.

Houd bij het registreren van de toepassing rekening met de volgende punten:

- Als u al een toepassing hebt geregistreerd als onderdeel van een integratie met een ander Microsoft-product, zoals Power BI, dan gebruikt u die geregistreerde app opnieuw. In dit geval hoeft u alleen de SharePoint-machtigingen in te stellen voor de bestaande geregistreerde app.

- Zorg ervoor dat u de geregistreerde app met de volgende gedelegeerde machtigingen voor de SharePoint-API configureert:

    - AllSites.FullControl
    - User.ReadWrite.All
    
    Stel in plaats daarvan de volgende machtigingen in voor Business Central 2021 releasewave 2 (versie 19):
    
    - AllSites.Write
    - MyFiles.Write
    - User.Read.All 

- Als u Business Central versie 19 of 20 gebruikt, kopieert u **Id van toepassing (client)** en **Clientgeheim** die door de geregistreerde app worden gebruikt. U hebt deze informatie nodig bij de volgende taak.

## <a name="get-your-onedrive-url"></a><a name="url"></a>Uw OneDrive -URL ophalen

[!INCLUDE[onedrive-url](includes/onedrive-url.md)]

## <a name="set-up-the-onedrive-connection-in-version-21-and-later"></a>De OneDrive-verbinding instellen in versie 21 en later

Gebruik deze procedure als u Business Central 2022 releasewave 2 (versie 21) of hoger gebruikt.

### <a name="prerequisites"></a>Vereisten

- Minimaal imd-machtiging (indirect, modify, delete) voor tabel **Documentservicescenario**

### <a name="run-onedrive-setup"></a>Configuratie van OneDrive uitvoeren

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Configuratie van OneDrive** in en kies vervolgens de gerelateerde koppeling.
2. De eerste keer dat u de begeleide instelling uitvoert, ziet u **Uw privacy**. Lees de informatie op de pagina, en als u akkoord gaat met de voorwaarden, kiest u **Akkoord** om door te gaan.
3. Op de pagina **Bestandsverwerking configureren** hebt u de volgende opties om uit te kiezen:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

4. Op de pagina **Business Central configureren** voert u de URL van OneDrive in het veld **OneDrive-URL** in.

   [Hoe kan ik mijn OneDrive-URL vinden?](#url)
5. Kies **Verbinding testen** en wacht op de resultaten.
   - Als de test slaagt, kiest u **Gereed**. Dan kunt u aan de slag.
   - Als de test mislukt, krijgt u een bericht waarin het probleem wordt beschreven. Meestal heeft het probleem te maken met de URL die u hebt opgegeven. Kies **OK** om terug te keren naar de pagina **Business Central configureren**, controleer de URL en probeer het opnieuw.
   - Als u de geregistreerde Microsoft Entra ID-app nog niet hebt ingesteld, wordt de guide **Microsoft Entra ID instellen** geopend.
6. Wanneer dit is voltooid, wordt voor alle gebruikers akkoord gegaan met de privacyverklaring voor OneDrive-integratie. Als u dit wilt wijzigen zodat gebruikers zelf al dan niet akkoord moeten gaan, gaat u naar de pagina **Status van privacyverklaringen** en selecteert u **Gebruiker laten beslissen** voor de OneDrive-integratie. Gebruikers wordt vervolgens gevraagd om al dan niet akkoord te gaan met de privacyverklaring wanneer ze de OneDrive-functies voor het eerst gebruiken. Zie [Privacyverklaringen](privacy-notices-status.md) voor meer informatie.

## <a name="set-up-the-connection-in--version-19-and-20"></a>De verbinding in [!INCLUDE[prod_short](includes/prod_short.md)] instellen in versie 19 en 20

Gebruik deze procedure als u Business Central 2022 releasewave 1 (versie 20) of 2021 releasewave 2 (versie 19) gebruikt.
> [!IMPORTANT]
> Door deze functie te configureren schakelt u ook oudere functies in die bestanden verzenden naar OneDrive.  
>
>* De functie Openen in Excel kopieert het Excel-bestand automatisch naar OneDrive en opent het vervolgens in Excel Online. 
>* Als u een rapport naar een bestand exporteert, wordt het bestand automatisch gekopieerd naar OneDrive en vervolgens geopend in Excel Online, Word Online of OneDrive. 
>* Andere functies kunnen ook automatisch worden geopend in OneDrive.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instellingen Microsoft SharePoint-verbinding** in en kies vervolgens de gerelateerde koppeling.
2. Voer in het veld **Omschrijving** een omschrijving in voor de verbinding, zoals **OneDrive**.
3. Voer in het veld **Map** **Business Central** in.
4. Voer in het veld **Locatie** de URL in voor uw OneDrive.

   [Hoe kan ik mijn OneDrive-URL vinden?](#url)
5. Voer in het veld **Client-id** de client-id van uw geregistreerde app in.
6. Voer in het veld **Clientgeheim** het geheim van uw geregistreerde app in. 

> [!IMPORTANT]
> De pagina **Instellingen SharePoint-verbinding** wordt gebruikt om meerdere verouderde functies te configureren. De sectie **Algemeen** configureert de verbinding met OneDrive en de sectie **Gedeelde documenten** leidt bestanden om naar SharePoint. **Instellingen SharePoint-verbinding** is verouderd en wordt in de komende release verwijderd. We raden u aan de sectie **Gedeelde documenten** te gebruiken. Zie voor meer informatie [Verouderde functies in de basisapp ](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#microsoft-sharepoint-connection-setup).

## <a name="after-upgrade-to-version-21"></a>Na upgrade naar versie 21

Wanneer u een upgrade uitvoert naar versie 21 of hoger, werkt de bestaande verbinding met OneDrive die is geconfigureerd op de pagina **Instellingen SharePoint-verbinding** nog steeds. Maar omdat de pagina **Instellingen SharePoint-verbinding** wordt verwijderd in versie 23, raden we u aan over te schakelen naar de nieuwe OneDrive-integratie, zoals wordt beschreven in het volgende gedeelte. Als u deze overstap nu maakt, wordt het gemakkelijker wanneer **Instellingen SharePoint-verbinding** uiteindelijk wordt verwijderd. Bovendien kunt u dan de begeleide instelling **Configuratie van OneDrive** gebruiken voor het beheren van de OneDrive-functies die toegankelijk zijn voor gebruikers.

## <a name="switching-from-legacy-sharepoint-to-new-onedrive-integration"></a>Overschakelen van oude SharePoint naar nieuwe OneDrive-integratie

Als u wilt overschakelen naar de nieuwe OneDrive-integratie, voert u de begeleide instelling **Configuratie van OneDrive** uit die u rechtstreeks kunt openen of via de oude pagina **Instellingen SharePoint-verbinding**. De begeleide instelling **Configuratie van OneDrive** begeleidt u bij de overgang en geeft informatie over de wijzigingen die worden aangebracht.

Voordat u aan de slag gaat met de overschakeling of terwijl u dit doet, raadpleegt u het volgende gedeelte voor meer informatie over enkele aspecten en overwegingen over het proces. 

### <a name="about-switching-to-the-new-onedrive-integration"></a><a name="onedrivesetupmigration"></a>Over overschakelen naar de nieuwe OneDrive-integratie

Naast OneDrive-integratie kan Business Central ook worden geïntegreerd met andere services, zoals Power BI en Universeel afdrukken. Integratie met deze andere services vereist ook een geregistreerde Microsoft Entra-app voor verificatie. De Microsoft Entra-app die door deze andere services wordt gebruikt, wordt geconfigureerd in de begeleide instelling **Uw Microsoft Entra-accounts instellen**. Wanneer u overschakelt van de oude SharePoint-verbindingsinstelling, wordt met de nieuwe begeleide instelling **Configuratie van OneDrive** uw OneDrive-integratie gewijzigd om ook de functie **Uw Microsoft Entra-accounts instellen** te gebruiken&mdash;dus voor alle integraties wordt dezelfde Microsoft Entra-app gebruikt.

Deze wijziging heeft gevolgen bij het overschakelen naar de nieuwe OneDrive-integratie, afhankelijk van de vraag of er al een Microsoft-app is geconfigureerd in de begeleide instelling **Uw Microsoft Entra-accounts instellen**. 

> [!IMPORTANT]
> Nadat u bent overgeschakeld naar de nieuwe OneDrive-instelling, kunt u de pagina **Instellingen SharePoint-verbinding** niet meer gebruiken om OneDrive-integratie te configureren.

#### <a name="how-the-changes-affect-the-integration"></a>Hoe de wijzigingen van invloed zijn op de integratie

Voor de begeleide instelling **Configuratie van OneDrive** wordt altijd de app gebruikt die is geconfigureerd in de begeleide instelling **Uw Microsoft Entra-accounts instellen**, als die er is. Wanneer u de begeleide instelling **Configuratie van OneDrive** uitvoert, wordt de app die is geconfigureerd in **Uw Microsoft Entra-accounts instellen**, vergeleken met uw huidige app die is geconfigureerd in **Instellingen SharePoint-verbinding**.

> [!TIP]
> Op de pagina **Instellingen SharePoint-verbinding** en de begeleide instelling **Uw Microsoft Entra-accounts instellen** wordt de Microsoft Entra-app geïdentificeerd door de **client-id**.

- Als de app in **Uw Microsoft Entra-accounts instellen** verschilt van de app in **Instellingen SharePoint-verbinding**, wordt de OneDrive-integratie gewijzigd voor gebruik van de app in **Uw Microsoft Entra-accounts instellen**.

   U krijgt in **Configuratie van OneDrive** tijdens de overschakeling een bericht dat lijkt op de volgende tekst: 

  `The Microsoft Entra application used for authentication will be configured for all Business Central integrations. This means the client id will change to NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN, you may want to test it has the correct permissions.`

  `NNNNNNNNN-NNNN-NNNN-NNNN-NNNNNNNNNNNN` staat voor de client-id van de app in **Uw Microsoft Entra-accounts instellen** waarnaar de OneDrive-integratie is overgeschakeld. 

  > [!IMPORTANT]
  > Om de nieuwe OneDrive-integratie te laten werken na de overschakeling, moet u de app toestemming geven voor de SharePoint-API in Azure-portal. U kunt deze stap uitvoeren voordat of nadat u overschakelt naar de nieuwe OneDrive-configuratie. Zie voor meer informatie het gedeelte [Een app registreren in Microsoft Entra ID voor OneDrive-integratie](#registerapp).

- Als de app in **Uw Microsoft Entra-accounts instellen** hetzelfde is als de app in **Instellingen SharePoint-verbinding**, wordt voor de OneDrive-integratie dezelfde app gebruikt als voorheen, met uitzondering van de configuratie in de instelling **Uw Microsoft Entra-accounts instellen**.

   U krijgt in **Configuratie van OneDrive** tijdens de overschakeling een bericht dat lijkt op de volgende tekst:

    `The Microsoft Entra application used for authentication will be configured for all Business Central integrations. This has already been configured with the same client id (5F78CADE-19C0-49BF-AF84-306D0579B50E).`

- Als er geen app is geconfigureerd in de instelling **Uw Microsoft Entra-accounts instellen**, gebruikt de OneDrive-integratie dezelfde app als voorheen.

   De begeleide instelling **Configuratie van OneDrive** kopieert app-configuratie naar de instelling **Uw Microsoft Entra-accounts instellen**, dus het wordt gebruikt voor andere integraties die mogelijk later worden ingesteld.

   U krijgt in **Configuratie van OneDrive** tijdens de overschakeling een bericht dat lijkt op de volgende tekst:

   `The Microsoft Entra application used for authentication will be configured for all Business Central integrations`.

### <a name="run-onedrive-setup-to-switch-to-the-new-onedrive-integration"></a>Configuratie van OneDrive uitvoeren om over te schakelen naar de nieuwe OneDrive-integratie

1. Open de pagina **Configuratie van OneDrive** of de pagina **Instellingen SharePoint-verbinding**.
2. Als u de pagina **Instellingen SharePoint-verbinding** gebruikt, kiest u **Ga naar nieuw OneDrive-instelling** in de melding bovenaan de pagina.
3. Volg de begeleide instelling **Configuratie van OneDrive**.
4. Wanneer u bij de pagina **Bestandsverwerking configureren** komt, kiest u een van de volgende opties om functies in te schakelen:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]

5. De pagina **Business Central configureren** bevat dezelfde URL die wordt gebruikt door de bestaande OneDrive-integratie. U kunt de URL indien nodig wijzigen.
6. Selecteer **Verbinding testen** en volg de instructies.

   Als de test slaagt, selecteert u **Gereed**. Dan kunt u aan de slag. Gebruik anders de berichten op de pagina om u te helpen het probleem op te lossen.

## <a name="see-also"></a>Zie ook
[Business Central en integratie met OneDrive voor Bedrijven](across-onedrive-overview.md)  
[Business Central-bestanden openen in OneDrive](across-share-onedrive.md)  
[Veelgestelde vragen over OneDrive](admin-onedrive-faq.md)

