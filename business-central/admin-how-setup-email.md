---
title: E-mail instellen in Business Central (bevat video)
description: Beschrijft hoe u e-mailaccounts verbindt met Business Central, zodat u uitgaande berichten kunt verzenden zonder een andere app te hoeven openen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, email, Office 365, connector
ms.search.form: 1805
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: de40994a555fbc657eacc18e8b2e8b33ce430fcb
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/19/2022
ms.locfileid: "8011138"
---
# <a name="set-up-email"></a>E-mail instellen
Mensen in bedrijven sturen dagelijks informatie en documenten, zoals verkoop- en inkooporders en facturen, per e-mail. Beheerders kunnen dat gemakkelijker maken door een of meer e-mailaccounts te verbinden met [!INCLUDE[prod_short](includes/prod_short.md)], zodat u documenten kunt verzenden zonder een e-mailapp te hoeven openen. U kunt elk bericht afzonderlijk opstellen met basisopmaakhulpmiddelen, zoals lettertypen, stijlen, kleuren, enzovoort, en bijlagen tot 100 MB toevoegen. Beheerders kunnen ook rapportlay-outs instellen die alleen de belangrijkste informatie uit documenten bevatten. Zie [Documenten per e-mail verzenden](ui-how-send-documents-email.md) voor meer informatie.

De e-mailmogelijkheden in [!INCLUDE[prod_short](includes/prod_short.md)] zijn alleen voor uitgaande berichten. U kunt geen antwoorden ontvangen, dat wil zeggen, er is geen inboxpagina in [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> U kunt de e-mailmogelijkheden van [!INCLUDE[prod_short](includes/prod_short.md)] online alleen met Exchange Online gebruiken. We ondersteunen geen hybride scenario's, zoals [!INCLUDE[prod_short](includes/prod_short.md)] online verbinden met een on-premises versie van Exchange.
> 
> Als u [!INCLUDE[prod_short](includes/prod_short.md)] on-premises gebruikt, moet u voordat u e-mail kunt instellen, een app-registratie maken voor [!INCLUDE[prod_short](includes/prod_short.md)] in Azure Portal. Door de app-registratie kan [!INCLUDE[prod_short](includes/prod_short.md)] autoriseren en verifiëren bij uw e-mailprovider. Zie voor meer informatie [E-mail instellen voor Business Central On-premises](admin-how-setup-email.md#setting-up-email-for-business-central-on-premises). In [!INCLUDE[prod_short](includes/prod_short.md)] online regelen wij dit voor u.

## <a name="required-permissions"></a>Vereiste machtigingen
Om e-mail in te stellen moet u de machtigingenset **Instelling van e-mail** hebben. Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie. 

## <a name="adding-email-accounts"></a>E-mailaccounts toevoegen
U voegt e-mailaccounts toe via extensies waarmee accounts van verschillende providers verbinding kunnen maken met [!INCLUDE[prod_short](includes/prod_short.md)]. Met de standaardextensies kunt u accounts gebruiken vanuit Microsoft Exchange Online, maar er zijn mogelijk andere extensies beschikbaar waarmee u accounts van andere providers kunt verbinden, zoals Gmail.

Nadat u een e-mailaccount heeft toegevoegd, kunt u vooraf gedefinieerde bedrijfsscenario's specificeren waarin u het account wilt gebruiken om e-mails te verzenden. U kunt bijvoorbeeld specificeren dat alle gebruikers verkoopdocumenten vanuit het ene account verzenden en inkoopdocumenten vanuit een ander. Zie voor meer informatie [E-mailscenario's toewijzen aan e-mailaccounts](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

De volgende tabel beschrijft de e-mailextensies die standaard beschikbaar zijn.

|Extensie  |Omschrijving  |Voorbeelden van wanneer te gebruiken  |
|---------|---------|---------|
|**Microsoft 365**|Iedereen verstuurt e-mail vanuit een gedeelde mailbox in Exchange Online.|Wanneer alle berichten bijvoorbeeld van dezelfde afdeling komen, verstuurt uw verkooporganisatie berichten vanaf een sales@cronus.com-account. Dit vereist dat u een gedeelde mailbox instelt in het Microsoft 365-beheercentrum. Zie voor meer informatie [Gedeelde mailboxen](/Exchange/collaboration/shared-mailboxes/shared-mailboxes).|
|**Huidige gebruiker**|Iedereen verstuurt e-mail vanaf het account waarmee ze zich hebben aangemeld bij [!INCLUDE[prod_short](includes/prod_short.md)].|Communicatie vanuit individuele accounts toestaan.|
|**Overige (SMTP)**|SMTP-protocol gebruiken om e-mails te verzenden.|Communicatie via uw SMTP-mailserver toestaan. |

> [!NOTE]
> De extensies **Microsoft 365** en **Huidige gebruiker** gebruiken de accounts die u voor gebruikers instelt in het Microsoft 365-beheercentrum, voor uw Microsoft 365-abonnement. Om e-mail te verzenden met de extensies moeten gebruikers een geldige licentie hebben voor Exchange Online. 
>
> Bovendien kunnen externe gebruikers, zoals gedelegeerde beheerders en externe accountants, deze extensies niet gebruiken om e-mailberichten te verzenden vanuit [!INCLUDE[prod_short](includes/prod_short.md)].

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4JsUk]

## <a name="legacy-smtp-settings-and-the-email---smtp-connector-extension"></a>Oude SMTP-instellingen en de extensie E-mail - SMTP-connector
Als u al gebruikmaakt van [!INCLUDE[prod_short](includes/prod_short.md)] en e-mail hebt geconfigureerd via de oude SMTP-instelling, kunt u uw instelling parallel met de extensie E-mail - SMTP-connector blijven gebruiken. Wanneer we uw [!INCLUDE[prod_short](includes/prod_short.md)] naar de volgende releaseversie bijwerken, zullen we uw oude SMTP-instellingen kopiëren naar de extensie E-mail - SMTP-connector. Als u klaar bent, kan uw beheerder de verbeterde e-mailmogelijkheden inschakelen en gaat u de extensie E-mail - SMTP-connector gebruiken. Zie [Over functiebeheer](/dynamics365/business-central/dev-itpro/administration/feature-management#about-feature-management) voor meer informatie. Er is echter geen synchronisatie tussen de extensie SMTP-connector en de oude instellingen. Als u de SMTP-instellingen in de extensie wijzigt, moet u dezelfde wijzigingen aanbrengen in de oude SMTP-instellingen of vice versa.

> [!NOTE]
> Als u aanpassingen heeft die afhankelijk zijn van de oude SMTP-e-mailconfiguratie, bestaat de kans dat er iets misgaat met uw aanpassingen als u e-mailextensies gaat gebruiken. We raden u aan de extensies in te stellen en te testen voordat u de functieschakelaar inschakelt voor verbeterde e-mailmogelijkheden.

> [!IMPORTANT]
> Als u [!INCLUDE[prod_short](includes/prod_short.md)] on-premises gebruikt, kunt u OAuth 2.0 gebruiken voor verificatie, maar u moet een toepassingsregistratie maken in de Azure-portal en vervolgens de begeleide instelling **Azure Active Directory instellen** in [!INCLUDE[prod_short](includes/prod_short.md)] gebruiken om verbinding te maken met Azure AD. Zie voor meer informatie [Een app-registratie voor Business Central maken in Azure Portal](admin-how-setup-email.md#create-an-app-registration-for-business-central-in-azure-portal).

## <a name="add-email-accounts"></a>E-mailaccounts toevoegen
De begeleide instelling **E-mail instellen** kan u helpen snel aan de slag te gaan met e-mails.

> [!NOTE]
> U moet een standaard e-mailaccount hebben, zelfs als u slechts één account toevoegt. Het standaardaccount wordt gebruikt voor alle e-mailscenario's die niet aan een account zijn toegewezen. Zie voor meer informatie [E-mailscenario's toewijzen aan e-mailaccounts](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **E-mailaccounts instellen** in en kies vervolgens de gerelateerde koppeling.
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 


<!--
> [!NOTE]
> If you choose **Other (SMTP)** and are using an account that requires two-factor authentication, the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription, and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 

is this still true?-->
## <a name="assign-email-scenarios-to-email-accounts"></a>E-mailscenario's toewijzen aan e-mailaccounts
E-mailscenario's zijn processen waarbij een document wordt verzonden, zoals een verkoop- of inkooporder, of een melding, zoals een uitnodiging aan een externe accountant. U kunt specifieke e-mailaccounts gebruiken voor specifieke scenario's. U kunt bijvoorbeeld specificeren dat alle gebruikers altijd verkoopdocumenten verzenden vanaf het ene account, inkoopdocumenten vanuit een ander en magazijn- of productiedocumenten vanaf een derde account. U kunt scenario's op elk gewenst moment toewijzen, opnieuw toewijzen en verwijderen, maar u kunt een scenario slechts aan één e-mailaccount tegelijk toewijzen. Het standaarde-mailaccount wordt gebruikt voor alle scenario's die niet aan een account zijn toegewezen.
 
<!--
## To set up email
1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > If you are using an account that requires two-factor authentication, then the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Alternatively, choose the **Apply Microsoft 365 Server Settings** action to insert any information that is already defined for your Microsoft 365 subscription.
4. When all the fields are correctly filled in, choose the **Test Email Setup** action.
5. When the test succeeds, close the page.

-->

## <a name="set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents"></a>Herbruikbare e-mailteksten en lay-outs instellen voor verkoop- en inkoopdocumenten
U kunt rapporten gebruiken om belangrijke informatie uit verkoop- en inkoopdocumenten op te nemen in teksten voor e-mails. Deze procedure beschrijft hoe u het rapport **Verkoop - Factuur** voor geboekte verkoopfacturen instelt, maar het proces is vergelijkbaar voor andere rapporten.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Rapportselectie - Verkoop** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Rapportselectie - Verkoop** in het veld **Gebruik** de optie **Factuur**.
3. Selecteer op een nieuwe regel in het veld **Rapport-ID** bijvoorbeeld standaardrapport 1306.
4. Schakel het selectievakje **Gebruiken voor hoofdtekst van e-mailbericht** in.
5. Kies het veld **Indelingsomschrijving van hoofdtekst van e-mailbericht** en selecteer vervolgens een lay-out in de lijst.

    Met rapportlay-outs wordt zowel de stijl als de inhoud van de e-mailhoofdtekst gedefinieerd, inclusief teksten zoals een begroeting, die voorafgaan aan de documentinformatie. Als uw organisatie veel lay-outs heeft, kunt u alle beschikbare rapportlay-outs zien als u **Selecteren vanuit volledige lijst** kiest.
6. Als u de lay-out wilt weergeven of bewerken waarop de e-mailtekst is gebaseerd, selecteert u op de pagina **Aangepaste rapportlay-outs** de lay-out en kiest u vervolgens de actie **Lay-out bijwerken**.
7. Als u klanten wilt aanbieden om voor verkoop elektronisch te betalen, kunt u de gerelateerde betalingsservice, zoals PayPal, instellen en vervolgens ook de PayPal-informatie en -koppeling in de e-mailtekst invoegen. Zie [Klantbetalingen via PayPal inschakelen](sales-how-enable-payment-service-extensions.md) voor meer informatie.
8. Kies de knop **OK**.

Wanneer u nu bijvoorbeeld de actie **Verzenden** kiest op de pagina **Geboekte verkoopfactuur**, bevat de e-mailhoofdtekst de documentgegevens van rapport 1306, voorafgegaan door standaardtekst die is geformatteerd volgens de rapportlay-out die u in stap 5 hebt geselecteerd.

## <a name="using-a-substitute-sender-address-on-outbound-email-messages"></a>Een vervangend afzenderadres gebruiken voor uitgaande e-mailberichten
Als u de oude SMTP-instellingen gebruikt, kunt u de mogelijkheden **Verzenden als** of **Verzenden namens** vanuit Microsoft Exchange gebruiken om het afzenderadres van uitgaande berichten te wijzigen. [!INCLUDE[prod_short](includes/prod_short.md)] zal het SMTP-account gebruiken om te verifiëren bij Exchange, maar zal het afzenderadres vervangen door het adres dat u opgeeft, of het wijzigen met 'namens'.

Hierna volgen voorbeelden van hoe Verzenden als en Verzenden namens worden gebruikt in [!INCLUDE[prod_short](includes/prod_short.md)]:

 * Wanneer u documenten zoals inkoop- of verkooporders naar leveranciers en klanten verzendt, wilt u misschien dat ze afkomstig lijken te zijn van een _noreply@yourcompanyname.com_-adres.
 * Wanneer uw werkstroom een goedkeuringsverzoek per e-mail verzendt met behulp van het e-mailadres van de aanvrager.

> [!Note]
> U kunt slechts één account gebruiken om afzenderadressen te vervangen. Dat wil zeggen, u kunt niet één vervangend adres hebben voor inkoopprocessen en een ander voor verkoopprocessen.

### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>Een vervangend afzenderadres instellen voor alle uitgaande e-mailberichten
1. Zoek in het **Exchange-beheercentrum** voor uw Microsoft 365-account de postbus die u als vervangend adres wilt gebruiken en kopieer of noteer het adres. Als u een nieuw adres nodig hebt, gaat u naar uw Microsoft 365-beheercentrum om een nieuwe gebruiker te maken en hun mailbox in te stellen.
2. Kies in [!INCLUDE[prod_short](includes/prod_short.md)] het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"). voer **SMTP-e-mailinstellingen** in en kies vervolgens de gerelateerde koppeling.
3. Voer in het veld **Verzenden als** het vervangende adres in.
4. Kopieer of noteer het adres in het veld **Gebruikersnaam**.
5. Zoek in het **Exchange-beheercentrum** de postbus die u als vervangend adres wilt gebruiken en voer vervolgens het adres uit het veld **Gebruikersnaam** in het veld **Verzenden als** in. Zie voor meer informatie [De EAC gebruiken om machtigingen toe te wijzen aan afzonderlijke mailboxen](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true#use-the-eac-to-assign-permissions-to-individual-mailboxes) voor meer informatie.

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>Het vervangende adres gebruiken in goedkeuringswerkstromen
1. Kies in [!INCLUDE[prod_short](includes/prod_short.md)] het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"). voer **SMTP-e-mailinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Kopieer of noteer het adres in het veld **Gebruikersnaam**.
3. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Gebruikersinstellingen voor goedkeuring** in en kies vervolgens de gerelateerde koppeling.
4. Zoek in het **Exchange-beheercentrum** de postvakken voor elke gebruiker die wordt vermeld op de pagina **Gebruikersinstellingen voor goedkeuring** en voer in het veld **Verzenden als** het adres uit het veld **Gebruikersnaam** van de pagina **SMTP-e-mailinstellingen** in [!INCLUDE[prod_short](includes/prod_short.md)] in. Zie [Machtigingen beheren voor ontvangers](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true) voor meer informatie.
5. Kies in [!INCLUDE[prod_short](includes/prod_short.md)] het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"). voer **SMTP-e-mailinstellingen** in en kies vervolgens de gerelateerde koppeling.
6. Als u vervanging wilt inschakelen, zet u de schakelaar **Vervanging van afzender toestaan** aan.

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] bepaalt welk adres wordt weergegeven in de volgende volgorde: <br><br> 1. Het adres dat is opgegeven in het veld **E-mail** op de pagina **Gebruikersinstellingen voor goedkeuring** voor berichten in een werkstroom. <br> 2. Het adres dat is opgegeven in het veld **Verzenden als** op de pagina **SMTP-e-mailinstellingen**. <br> 3. Het adres dat is opgegeven in het veld **Gebruikersnaam** op de pagina **SMTP-e-mailinstellingen**.

## <a name="set-up-document-sending-profiles"></a>Verzendprofielen van documenten instellen
U kunt een voorkeursmethode instellen voor het verzenden van verkoopdocumenten voor elk van uw klanten, zodat u geen verzendoptie hoeft te selecteren, bijvoorbeeld of u het document per e-mail of als elektronisch document wilt verzenden, elke keer dat u een document verzendt. Zie [Verzendprofielen voor documenten instellen](sales-how-setup-document-send-profiles.md) voor meer informatie.

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Openbare mappen en regels instellen voor e-mailregistratie in Exchange Online
Haal meer uit de communicatie tussen verkopers en uw bestaande of potentiële klanten door e-mailuitwisselingen bij te houden en deze vervolgens om te zetten in bruikbare kansen. Zie voor meer informatie [E-mailberichtuitwisselingen volgen tussen verkopers en contactpersonen](marketing-set-up-email-logging.md).  

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Vervolgens verbindt u [!INCLUDE[prod_short](includes/prod_short.md)] met Exchange Online. Zie voor meer informatie [E-mailberichtuitwisselingen volgen tussen verkopers en contactpersonen](marketing-set-up-email-logging.md).  

## <a name="setting-up-email-for-business-central-on-premises"></a>E-mail instellen voor Business Central On-Premises 
[!INCLUDE[prod_short](includes/prod_short.md)] on-premises kan worden geïntegreerd met services die zijn gebaseerd op Microsoft Azure. U kunt bijvoorbeeld Cortana Intelligence voor slimmere cashflowprognoses gebruiken, Power BI gebruiken om uw bedrijf te visualiseren en Exchange Online gebruiken voor het verzenden van e-mail. Integratie met deze services is gebaseerd op een app-registratie in Azure Active Directory. De app-registratie biedt verificatie- en autorisatieservices voor communicatie. Om de e-mailmogelijkheden in [!INCLUDE[prod_short](includes/prod_short.md)] on-premises te gebruiken, moet u [!INCLUDE[prod_short](includes/prod_short.md)] registreren als een app in de Azure Portal en vervolgens [!INCLUDE[prod_short](includes/prod_short.md)] verbinden met de app-registratie. In de volgende secties wordt uitgelegd hoe u dat doet.

### <a name="create-an-app-registration-for-business-central-in-azure-portal"></a>Een app-registratie voor Business Central maken in Azure Portal
De stappen om [!INCLUDE[prod_short](includes/prod_short.md)] te registreren in Azure Portal worden beschreven in [Een toepassing registreren in Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory). De instellingen die specifiek zijn voor de e-mailmogelijkheden, zijn de gedelegeerde machtigingen die u verleent aan uw app-registratie. De volgende tabel bevat de minimale machtigingen.

|API-/machtigingsnaam  |Soort  |Omschrijving  |
|---------|---------|---------|
|Microsoft Graph/User.Read |Gedelegeerd|Aanmelden en gebruikersprofiel lezen.         |
|Microsoft Graph/Mail.ReadWrite |Gedelegeerd|E-mailberichten opstellen.         |
|Microsoft Graph/Mail.Send|Gedelegeerd|E-mailberichten verzenden.         |
|Microsoft Graph/offline_access|Gedelegeerd|Toestemming voor gegevenstoegang behouden.|

Als u een oude SMTP-instelling of de SMTP-connector gebruikt en OAuth voor verificatie wilt gebruiken, zijn de machtigingen iets anders. De volgende tabel bevat de machtigingen.

|API-/machtigingsnaam  |Soort  |Omschrijving  |
|---------|---------|---------|
|Microsoft Graph / offline_access|Gedelegeerd|Toestemming voor gegevenstoegang behouden.|
|Microsoft Graph / openid|Gedelegeerd|Log gebruikers in.|
|Microsoft Graph/User.Read |Gedelegeerd|Aanmelden en gebruikersprofiel lezen.         |
|Microsoft Graph / SMTP.Send|Gedelegeerd|Verzend e-mails vanuit mailboxen met SMTP AUTH.         |
|Office 365 Exchange Online / User.Read |Gedelegeerd|Meld u aan en lees het gebruikersprofiel.         |

Wanneer u de app-registratie maakt, moet u rekening houden met de volgende informatie. U hebt deze nodig om [!INCLUDE[prod_short](includes/prod_short.md)] te verbinden met uw app-registratie.
 
* Id van toepassing (client) 
* Omleidings-URI (optioneel)
* Clientgeheim

Voor algemene richtlijnen voor het registreren van een app raadpleegt u [Quickstart: een toepassing registreren bij het Microsoft-identiteitsplatform](/azure/active-directory/develop/quickstart-register-app). 

> [!NOTE]
Als u problemen ondervindt bij het gebruik van de oude SMTP-instelling om e-mail te verzenden nadat u [!INCLUDE[prod_short](includes/prod_short.md)] hebt verbonden met uw app-registratie, kan het zijn dat SMTP AUTH niet is ingeschakeld voor uw tenant. We raden u aan om in plaats daarvan de e-mailconnectoren Microsoft 365 en Huidige gebruiker te gebruiken, omdat deze de API's van Microsoft Graph Mail gebruiken. Als u echter de SMTP-instellingen moet gebruiken, kunt u SMTP AUTH inschakelen. Zie voor meer informatie [Geverifieerde client SMTP-verzending (SMTP AUTH) in- of uitschakelen Exchange Online](/exchange/clients-and-mobile-in-exchange-online/authenticated-client-smtp-submission#disable-smtp-auth-in-your-organization).

### <a name="connect-prod_short-to-your-app-registration"></a>[!INCLUDE[prod_short](includes/prod_short.md)] verbinden met uw app-registratie
Nadat u uw toepassing in Azure Portal hebt geregistreerd, gebruikt u in [!INCLUDE[prod_short](includes/prod_short.md)] de begeleide instelling **AAD-registratie van e-mailtoepassing** om [!INCLUDE[prod_short](includes/prod_short.md)] ermee te verbinden.

1. Kies in [!INCLUDE[prod_short](includes/prod_short.md)] het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"). voer **AAD-registratie van e-mailtoepassing** in en kies vervolgens de gerelateerde koppeling.
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Als alternatief, als u voor de eerste keer verbinding maakt, kunt u de begeleide instelling **E-mail instellen** uitvoeren. De begeleide instelling heeft de informatie nodig om verbinding te maken met uw app-registratie. <!--Need to verify this too. Ask John to clear the aad settings, delete the email accounts, and then run the guide.-->

<!--

1. In [!INCLUDE[prod_short](includes/prod_short.md)], start the **Email Application AAD Registration** assisted setup guide.
2. On the first page of the guide, copy the value in the **Redirect URL** field.
3. In Azure Active Directory, search for **App registrations**, and then open the **App registrations** page.
4. Choose **New registration**.
5. In the **Name** field, enter a name for your app.
6. Under **Supported account types**, choose either the **Accounts in any organizational directory (Any Azure AD Directory - Multitenant)** or **Accounts in any organizational directory (Any Azure AD Directory - Multitenant) and personal Microsoft accounts (/e.g. Skype, Xbox)** options, depending on your needs. If you're unsure, choose **Help me choose** for more information.
7. Under **Redirect URI (optional)**, choose **Web**, paste the URL you copied from the **Redirect URL** field in the assisted setup guide in Business Central, and then choose **Register**.
8. On the navigation pane, choose **Overview**, and then copy the value in the **Application (client) ID** field.
9. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide, paste the ID in **Client ID** field.
10. In Azure Active Directory, on the navigation pane, choose **API permissions**, and then choose **Add a permission**.
11. On the **Request API permissions** pane, on the **Microsoft APIs** tab, choose **Microsoft Graph**.  
12. Choose **Delegated permissions**, and then in the **Select permissions** field, search for **Mail.ReadWrite**, **Mail.Send**, and **offline_access**. Choose those permissions, and then choose **Add permissions**.
13. On the navigation pane, choose **Certificates & secrets**.
14. Under **Client secrets**, choose **New client secret**.
15. Under **Add a client secret**, enter a description of the client, specify how long you want your secret to be available, and then choose **Add**.
16. When the secret is generated, copy it. 
17. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide paste the secret in the **Client Secret field**.
18. The **Verify Registration** button becomes available. 

-->

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/set-up-email/)

## <a name="see-also"></a>Zie ook

[Gedeelde postbussen in Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Instellen van [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met behulp van extensies](ui-extensions.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken als uw bedrijfsinbox in Outlook](admin-outlook.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] installeren op mijn mobiele apparaat](install-mobile-app.md)
[[!INCLUDE[prod_short](includes/prod_short.md)] installeren op mijn mobiele apparaat](install-mobile-app.md)
[E-mailtelemetrie analyseren (beheerinhoud)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
