---
title: De Business Central-invoegtoepassing voor Excel verkrijgen
description: Meer informatie over hoe u gebruikers de Business Central-invoegtoepassing voor Excel kunt geven.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.form: 1480
ms.search.keywords: 'Excel, add-in, centralized deployment, M365 admin center, individual acquisition, appsource'
ms.date: 10/07/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="get-the-business-central-add-in-for-excel"></a>De Business Central-invoegtoepassing voor Excel verkrijgen

[!INCLUDE[prod_short](includes/prod_short.md)] bevat een invoegtoepassing voor Excel waarmee gebruikers een **Bewerken in Excel**-actie op bepaalde pagina's kunnen selecteren om de gegevens in een Excel-werkblad te openen. Deze actie is anders dan de actie **Openen in Excel** omdat het gebruikers in staat stelt wijzigingen aan te brengen in Excel en de wijzigingen vervolgens weer te publiceren naar [!INCLUDE[prod_short](includes/prod_short.md)]

## <a name="overview"></a>Overzicht

### <a name="about-the-add-in"></a>Over de invoegtoepassing

De invoegtoepassing heet **Microsoft Dynamics Office-invoegtoepassing** en is beschikbaar voor installatie vanuit de [Office Store (AppSource)](https://appsource.microsoft.com/). Met de invoegtoepassing geïnstalleerd is de **Bewerken in Excel**-actie beschikbaar op de meeste lijst- en lijstonderdeelpagina's vanuit het pictogram **Delen** ![Een pagina delen in een andere app.](media/share-icon.png). Zie voor meer informatie over het gebruik van de invoegtoepassing [Weergeven en bewerken in Excel vanuit Business Central](across-work-with-excel.md).

> [!NOTE]
> De invoegtoepassing werkt alleen onder Windows, niet onder MacOS.

### <a name="about-deployment-as-an-admin"></a>Over implementatie als beheerder

Met [!INCLUDE[prod_short](includes/prod_short.md)] online zijn er een paar implementatieopties om de invoegtoepassing voor gebruikers te krijgen. Eén optie is *individuele acquisitie*, waarbij u gebruikers de invoegtoepassing zelf laat installeren. Met deze optie moeten gebruikers toegang hebben tot het downloaden van bestanden uit de Office Store. Een andere optie is om *Gecentraliseerde implementatie* in te stellen in het Microsoft 365-beheercentrum om de invoegtoepassing automatisch te implementeren voor uw hele organisatie, groepen of specifieke gebruikers. Gecentraliseerde implementatie biedt een manier om de invoegtoepassing voor gebruikers te krijgen als uw organisatie gebruikers geen toegang geeft tot de Office Store.

Voor de eindgebruiker is de installatie-ervaring verschillend voor de twee implementatiescenario's:

- Met individuele acquisitie wordt de eerste keer dat gebruikers de actie **Bewerken in Excel** kiezen het deelvenster **Nieuwe Office-invoegtoepassing** geopend in Excel. Om de invoegtoepassing te installeren kiest de gebruiker **Deze invoegtoepassing vertrouwen**, waardoor de invoegtoepassing rechtstreeks vanuit de Office Store wordt geïnstalleerd. Gebruikers melden zich vervolgens aan bij [!INCLUDE[prod_short](includes/prod_short.md)] met behulp van hun gebruikersnaam en wachtwoord.

- Met gecentraliseerde implementatie wordt de invoegtoepassing, wanneer gebruikers voor het eerst voor de actie **Bewerken in Excel** kiezen, automatisch geïnstalleerd in Excel vanuit gecentraliseerde implementatie; niet vanuit de Office Store. Het enige dat gebruikers hoeven te doen, is aanmelden bij [!INCLUDE[prod_short](includes/prod_short.md)]

Met beide implementatieopties wordt de invoegtoepassing automatisch geconfigureerd om verbinding te maken met [!INCLUDE[prod_short](includes/prod_short.md)]. Een derde implementatieoptie is een handmatige installatie van de invoegtoepassing rechtstreeks vanuit Excel. Met deze optie moeten gebruikers de invoegtoepassing configureren om verbinding te maken met [!INCLUDE[prod_short](includes/prod_short.md)]

### <a name="switching-from-individual-acquisition-to-centralized-deployment-or-the-other-way-around"></a><a name="switch"></a>Overschakelen van individuele acquisitie naar gecentraliseerde implementatie of andersom

Wanneer u overstapt van individuele acquisitie van de invoegtoepassing naar gecentraliseerde implementatie, of vice versa, heeft dit gevolgen voor Excel-bestanden die gebruikers vóór de overgang hebben gemaakt. Na de overgang kunnen gebruikers nog steeds Excel-werkbladen openen die eerder zijn gemaakt met de **Bewerken in Excel**-actie of die handmatig zijn gemaakt, door de Excel-invoegtoepassing te configureren. Maar ze kunnen de gegevens in het bestand niet bijwerken vanuit Business Central of updates naar Business Central pushen

Dit komt doordat elk Excel-bestand een 'invoegtoepassing'-id krijgt toegewezen. Bij de overgang van of naar gecentraliseerde implementatie wordt een andere id toegewezen, waardoor de eerdere id wordt geblokkeerd.

## <a name="preparation-on-premises-only"></a>Voorbereiding (alleen voor on-premises)

[!INCLUDE[prod_short](includes/prod_short.md)] on-premises vereist dat uw omgeving is geconfigureerd voor de invoegtoepassing. Zo niet, dan is de actie **Bewerken in Excel** niet beschikbaar voor gebruikers. Zie voor meer informatie [De Excel-invoegtoepassing instellen om Business Central-gegevens te bewerken](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin) in de Help voor ontwikkelaars en IT Pro.

## <a name="deploy-the-add-in-by-using-centralized-deployment"></a>De invoegtoepassing implementeren met behulp van gecentraliseerde implementatie

Gecentraliseerde implementatie is een functie in het Microsoft 365-beheercentrum die u gebruikt om automatisch invoegtoepassingen te installeren in Office-apps van gebruikers, zoals Excel. Om u te helpen met gecentraliseerde implementatie, bevat [!INCLUDE[prod_short](includes/prod_short.md)] de begeleide instelling **Gecentraliseerde implementatie van Excel-invoegtoepassing**.

### <a name="before-you-begin"></a>Voordat u begint

- Zie voor meer informatie over het voorkomen dat gebruikers downloaden uit de Office Store [Invoegtoepassingen beheren in het beheercentrum](/microsoft-365/admin/manage/manage-addins-in-the-admin-center).
- Controleer of gecentraliseerde implementatie werkt voor uw organisatie. Zie voor meer informatie [Bepalen of gecentraliseerde implementatie van invoegtoepassingen werkt voor uw organisatie](/microsoft-365/admin/manage/centralized-deployment-of-add-ins)
- Als u overstapt van individuele acquisitie, zie [Overschakelen van individuele acquisitie naar gecentraliseerde implementatie](#switch)

> [!NOTE]
> Het inschakelen van gecentraliseerde implementatie is van invloed op functies die gebruikmaken van de Excel-invoegtoepassing, zoals de actie **Bewerken in Excel**. Het heeft geen effect op andere Excel-gerelateerde functies en/of machtigingen die zijn toegewezen aan gebruikers in [!INCLUDE[prod_short](includes/prod_short.md)]

### <a name="set-up-centralized-deployment-of-the-add-in"></a>Gecentraliseerde implementatie van de invoegtoepassing instellen

U werkt in [!INCLUDE[prod_short](includes/prod_short.md)] en het Microsoft 365-beheercentrum.

1. Kies in [!INCLUDE[prod_short](includes/prod_short.md)] het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gecentraliseerde implementatie van Excel-invoegtoepassing** in en kies vervolgens de gerelateerde koppeling.
2. Lees de informatie op de pagina **Instelling van Excel-invoegtoepassing van Business Central** en kies **Volgende**.
3. Meld u aan bij het [Microsoft 365-beheercentrum](https://go.microsoft.com/fwlink/?linkid=2163967) en ga naar **Geïntegreerde apps**<!--**Add-ins**-->.

    Voer de volgende stappen uit om de invoegtoepassing te configureren voor implementatie vanuit de Office Store: 
    1. Kies **Apps downloaden** om de Office Store (AppSource) te openen. <!--**Deploy Add-in** 5. In the **Deploy a new add-in**, select **Choose from the store**.-->
    2. Zoek **Microsoft Dynamics Office-invoegtoepassing** en selecteer vervolgens **Nu ophalen**. <!--On the **Select add-in** page, search for and select **Microsoft Dynamics Office Add-in** > **Add** > **Continue**.-->
    3. Geef op de pagina **Gebruikers toevoegen** de gebruikers op voor wie u de invoegtoepassing wilt implementeren en kies **Volgende**.<!--On the **Configure add-in**, specify the users that you want to deploy the add-in for.-->
    4. Bekijk de **Verzoeken om machtigingen te accepteren** en kies dan **Volgende** > **Implementatie voltooien**.
    5. Wacht tot het groene vinkje naast **Geïmplementeerd** verschijnt voor de invoegtoepassing en kies vervolgens **Gereed**. <!--Select **Deploy** and wait til successful, then **Next** > **Continue**.-->

       De invoegtoepassing verschijnt op de pagina **Invoegtoepassingen**. Zie [Invoegtoepassingen implementeren in het beheercentrum](/power-platform/admin/use-service-admin-role-manage-tenant?azure-portal=true) voor meer informatie over het implementeren van invoegtoepassingen in het Microsoft 365-beheercentrum.
4. Ga terug naar de begeleide instelling **Gecentraliseerde implementatie van Excel-invoegtoepassing** in [!INCLUDE[prod_short](includes/prod_short.md)] en kies **Volgende**.
5. Zet **Gecentraliseerde implementatie gebruiken** aan en kies **Voltooien**.

    Als u deze schakelaar niet aanzet, haalt [!INCLUDE[prod_short](includes/prod_short.md)] de invoegtoepassing rechtstreeks uit de Office Store.

Als u klaar bent, kunt u de implementatie altijd wijzigen in het Microsoft 365-beheercentrum, zoals het toewijzen van meer gebruikers. Zie [Invoegtoepassingen implementeren in het beheercentrum](/power-platform/admin/use-service-admin-role-manage-tenant?azure-portal=true) voor meer informatie over het implementeren van invoegtoepassingen in het beheercentrum.

> [!IMPORTANT]
> Als u meer dan één omgeving hebt, moet u de begeleide instelling **Gecentraliseerde implementatie van Excel-invoegtoepassing** uitvoeren in elke omgeving waarin u gecentraliseerde implementatie wilt gebruiken. U hoeft de gecentraliseerde implementatie in Microsoft 365 echter niet opnieuw te configureren. Het enige wat u hoeft te doen, is de schakelaar **Gecentraliseerde implementatie gebruiken** aanzetten in de begeleide instelling. 

> [!NOTE]
> Het kan tot 24 uur duren voordat gebruikers de invoegtoepassing automatisch implementeren in de Excel van gebruikers.

## <a name="individual-acquisition-install-the-add-in-manually-for-your-own-use"></a><a name="install"></a>Individuele acquisitie: de invoegtoepassing handmatig installeren voor eigen gebruik

In de meeste gevallen, wanneer u Excel opent vanuit Business Central, wordt de invoegtoepassing automatisch voor u geïnstalleerd of wordt u gevraagd deze te installeren. Er kunnen echter gevallen zijn waarin u de invoegtoepassing handmatig moet installeren.

1. Open Excel en open vervolgens een Excel-werkmap.
2. Kies in het menu **Invoegen** **Invoegtoepassingen** > **Invoegtoepassingen ophalen**
3. Ga naar **Door beheerder beheerd** en zoek naar **Microsoft Dynamics Office-invoegtoepassing**. Als u het daar ziet, selecteert u het en kiest u **Toevoegen**. Als u het niet ziet, gaat u naar **Winkel**, zoekt u naar *Microsoft Dynamics Office-invoegtoepassing* en volgt u de instructies op het scherm om het toe te voegen.

Wanneer de invoegtoepassing is geïnstalleerd, wordt deze weergegeven als een deelvenster in Excel. Configureer vervolgens de verbinding.

### <a name="configure-the-business-central-connection"></a>De Business Central-verbinding configureren

Als een gebruiker niet automatisch verbinding kan maken, kunt u de blokkering opheffen door hem of haar te vragen deze stappen te volgen:

1. Kies in het deelvenster van de **Microsoft Dynamics**-invoegtoepassing in Excel **Serverinformatie toevoegen**. Als u het niet ziet, kies dan het pictogram ![keuzerondje Meer in Excel.](media/cogwheel.png) bovenaan om het dialoogvenster met opties te openen. 
2. Stel voor [!INCLUDE[prod_short](includes/prod_short.md)] online **Server-URL** in op `https://exceladdinprovider.smb.dynamics.com`. Stel voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises de URL van de webclient in, bijvoorbeeld `https://myBCserver/190`.
3. Kies **OK** en bevestig vervolgens dat de app opnieuw wordt geladen.
4. Meld u wanneer daarom wordt gevraagd, aan met uw Business Central-gebruikersnaam en -wachtwoord.
5. Kies desgewenst de omgeving en het bedrijf waarmee u verbinding wilt maken.

De invoegtoepassing is nu verbonden met [!INCLUDE [prod_short](includes/prod_short.md)] en u kunt gegevens bewerken en de wijzigingen publiceren naar [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="prepare-devices-and-network-for-the-excel-add-in"></a>Apparaten en netwerk voorbereiden voor de Excel-invoegtoepassing

Netwerkservices zoals proxy's of firewalls moeten routering toestaan tussen elk clientapparaat waarop de invoegtoepassing is geïnstalleerd en vele service-eindpunten. Zie voor een lijst met eindpunten [Uw netwerk voorbereiden op de Excel-invoegtoepassing](/dynamics365/business-central/dev-itpro/administration/configuring-network-for-addins).

## <a name="troubleshooting"></a>Problemen oplossen

Soms ondervinden gebruikers problemen met de Excel-invoegtoepassing. Dit gedeelte geeft enkele tips voor het deblokkeren van gebruikers in bepaalde omstandigheden.

|Probleem  |Oplossing of tijdelijke oplossing  |Opmerkingen  |
|---------|---------|---------|
|De invoegtoepassing start niet <br><br>De gebruiker krijgt bijvoorbeeld het bericht "Waarschuwing over invoegtoepassing: deze invoegtoepassing is niet meer beschikbaar" wanneer u de invoegtoepassing probeert te gebruiken. Dit specifieke probleem kan optreden als gecentraliseerde implementatie correct is geconfigureerd, maar de gebruiker geen toegang heeft gekregen.|Controleer of de invoegtoepassing centraal wordt geïmplementeerd. Of controleer of de gebruiker is geblokkeerd tegen lokale installatie. | De beheerder kan Office zo configureren dat gebruikers geen invoegtoepassingen kunnen verkrijgen. In die gevallen moet de beheerder de invoegtoepassing centraal implementeren. Voor meer informatie zie [Invoegtoepassingen implementeren in het beheercentrum](/microsoft-365/admin/manage/manage-deployment-of-add-ins?view=o365-worldwide&preserve-view=true).|
|Gegevens worden niet in Excel geladen|Test de verbinding door een andere lijst in Excel te openen vanuit [!INCLUDE [prod_short](includes/prod_short.md)]. Of open de werkmap in Excel in een browser.|Als de gebruiker een bedrijfsnaam heeft opgegeven die speciale tekens bevat, kan de invoegtoepassing geen verbinding maken. |
|Gegevens kunnen niet terug worden gepubliceerd naar [!INCLUDE [prod_short](includes/prod_short.md)].|Test de verbinding door de werkmap in Excel in een browser te openen. |Soms kan een extensie de publicatietaak blokkeren. Als de pagina is uitgebreid of aangepast, verwijdert u de extensies en probeert u het opnieuw.|
|De datums zijn fout  |Excel toont mogelijk tijden en datums in een ander formaat dan [!INCLUDE [prod_short](includes/prod_short.md)]. Ze zijn echter niet verkeerd en de gegevens in [!INCLUDE [prod_short](includes/prod_short.md)] blijven intact.|         |
|Voor sommige lijstpagina's veroorzaakt het bewerken van meerdere regels in Excel consequent fouten. Dit kan optreden als OData-aanroepen FlowFields en velden buiten het repeaterbesturingselement bevatten.|Selecteer op de pagina **Webservices** de selectievakjes **Niet-bewerkbare FlowFields uitsluiten** en **Velden buiten de repeater uitsluiten** voor de gepubliceerde pagina. Door deze selectievakjes in te schakelen worden niet-bewerkbare FlowFields en velden uitgesloten van de eTag-berekening. |Deze selectievakjes zijn standaard verborgen. Om ze te laten zien op de pagina **Webservices**, gebruikt u [personalisatie](/dynamics365/business-central/ui-personalization-user). |
|Gebruikers kunnen niet langer inloggen op de invoegtoepassing. Wanneer ze proberen in te loggen, stopt het proces zonder te voltooien.| Dit probleem kan worden veroorzaakt door een update die we hebben aangebracht in de invoegtoepassing, ergens in juli 2022. Voor meer informatie en een oplossing, zie [De configuratie van de Excel-invoegtoepassing wijzigen om de update van juli 2022 te ondersteunen](/dynamics365/business-central/dev-itpro/administration/update-excel-addin-configuration).|Geldt alleen voor [!INCLUDE [prod_short](includes/prod_short.md)] on-premises|

<!--
## <a name="deploy-the-excel-add-in-for-business-central-online"></a>Deploy the Excel add-in for Business Central online

For [!INCLUDE [prod_short](includes/prod_short.md)] online, the administrator can deploy the add-in for all users. But users can also install the add-in themselves, provided they have permission to configure their Office experience.  

> [!TIP]
> In some organizations, administrators cannot deploy add-ins centrally. For more information, see [Determine if Centralized Deployment of add-ins works for your organization](/microsoft-365/admin/manage/centralized-deployment-of-add-ins?view=o365-worldwide&preserve-view=true).

### <a name="to-deploy-the-excel-add-in-for-all-users"></a>To deploy the Excel add-in for all users

1. As the administrator, sign in to the Microsoft commercial website and find the add-in at [https://appsource.microsoft.com/product/office/WA104379629](https://appsource.microsoft.com/product/office/WA104379629).
2. Choose the **Get it now** button.

    You'll be redirected to the Microsoft 365 admin center.
3. In the left panel, go to **Settings**, and then choose **Add-ins**.
4. In the **Configure add-in** pane, specify which users to grant access to the add-in.
5. Save your changes.


### <a name="to-add-the-excel-add-in-locally"></a>To add the Excel add-in locally

1. Open Excel, and then open any Excel workbook.
2. On the **Insert** menu, choose **Office Add-ins**, and then choose **Admin managed** or **Store** as appropriate.
3. Search for *Dynamics Office Add-In*, and then install the add-in.

When the add-in is installed, it shows up as a panel in Excel. Next, you must configure the connection.

> [!TIP]
> If the workbook is not automatically saved to the user's OneDrive, then recommend them to save all workbooks that they export from [!INCLUDE [prod_short](includes/prod_short.md)].When they open the workbook again, the connection is still available, so they do not have to configure the connection again.

> [!NOTE]
> In certain deployments, the administrator must configure network access to unblock the Excel add-in. For more information, see [Preparing Your Network for the Excel Add-In](configuring-network-for-addins.md).-->

## <a name="see-also"></a>Zie ook

[Financiële overzichten analyseren in Microsoft Excel](finance-analyze-excel.md)  
[Werken met Business Central](ui-work-product.md)  
[Verbeteringen aan Excel-integratie in releasewave 2 van 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
