---
title: E-mail instellen in Business Central (bevat video)
description: 'Beschrijft hoe u e-mailaccounts verbindt met Business Central, zodat u uitgaande berichten kunt verzenden zonder een andere app te hoeven openen.'
author: brentholtorf
ms.author: bholtorf
ms.topic: get-started
ms.search.keywords: 'SMTP, email, Office 365, connector'
ms.search.form: '1805, 9813, 9814, 1262, 1263'
ms.date: 03/04/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="set-up-email"></a>E-mail instellen

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Mensen in bedrijven sturen dagelijks informatie en documenten, zoals verkoop- en inkooporders en facturen, per e-mail. Beheerders kunnen een of meer e-mailaccounts verbinden met [!INCLUDE[prod_short](includes/prod_short.md)], zodat u documenten kunt verzenden zonder een e-mailapp te hoeven openen. U kunt elk bericht afzonderlijk opstellen met basisopmaakhulpmiddelen, zoals lettertypen, stijlen, kleuren, enzovoort, en bijlagen tot 100 MB toevoegen. Daarnaast kunnen beheerders met rapportlay-outs alleen de belangrijkste informatie uit documenten opnemen. Meer informatie op [Documenten per e-mail verzenden](ui-how-send-documents-email.md).

E-mailmogelijkheden in [!INCLUDE[prod_short](includes/prod_short.md)] zijn alleen voor uitgaande berichten. U kunt geen antwoorden ontvangen, met andere woorden, er is geen inboxpagina.

> [!NOTE]
> U kunt de e-mailmogelijkheden van [!INCLUDE[prod_short](includes/prod_short.md)] online alleen met Exchange Online gebruiken. We ondersteunen geen hybride scenario's, zoals [!INCLUDE[prod_short](includes/prod_short.md)] online verbinden met een on-premises versie van Exchange.
>
> Als u [!INCLUDE[prod_short](includes/prod_short.md)] on-premises gebruikt, moet u voordat u e-mail kunt instellen, een app-registratie maken voor [!INCLUDE[prod_short](includes/prod_short.md)] in de Azure-portal. Door de app-registratie kan [!INCLUDE[prod_short](includes/prod_short.md)] autoriseren en verifiëren bij uw e-mailprovider. Meer informatie op [E-mail instellen voor Business Central On-Premises](admin-how-setup-email.md#set-up-email-for-business-central-on-premises). In [!INCLUDE[prod_short](includes/prod_short.md)] online regelen wij dit voor u.

## <a name="requirements"></a>Vereisten

Er is een aantal vereisten voor het instellen en gebruiken van de e-mailfuncties.

* Om e-mail in te stellen moet u de machtigingenset **Instelling van e-mail** hebben. Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie.
* Iedereen die de e-mailfuncties gaat gebruiken, moet een volledige licentie hebben voor [!INCLUDE [prod_short](includes/prod_short.md)]. Gedelegeerde beheerders en gastgebruikers kunnen bijvoorbeeld het e-mailaccount van de tenant niet gebruiken.

## <a name="add-email-accounts"></a>E-mailaccounts toevoegen

U voegt e-mailaccounts toe via extensies waarmee accounts van verschillende providers verbinding kunnen maken met [!INCLUDE[prod_short](includes/prod_short.md)]. Met de standaardextensies kunt u accounts gebruiken vanuit Microsoft Exchange Online. Er zijn echter mogelijk ook andere extensies beschikbaar waarmee u accounts van andere providers kunt koppelen, zoals Gmail.

U kunt vooraf gedefinieerde bedrijfsscenario's opgeven waarin een e-mailaccount wordt gebruikt om e-mails te verzenden. U kunt bijvoorbeeld specificeren dat alle gebruikers verkoopdocumenten vanuit het ene account verzenden en inkoopdocumenten vanuit een ander. Meer informatie op [E-mailscenario's toewijzen aan e-mailaccounts](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

De volgende tabel beschrijft de e-mailextensies die standaard beschikbaar zijn.

|Extensie  |Omschrijving  |Voorbeelden van wanneer te gebruiken  |
|---------|---------|---------|
|**Microsoft 365-connector**|Iedereen verstuurt e-mail vanuit een gedeelde mailbox in Exchange Online.|Wanneer alle berichten bijvoorbeeld van dezelfde afdeling komen, verstuurt uw verkooporganisatie berichten vanaf een sales@cronus.com-account. Deze optie vereist dat u een gedeelde mailbox instelt in het Microsoft 365-beheercentrum. Zie voor meer informatie [Gedeelde mailboxen](/Exchange/collaboration/shared-mailboxes/shared-mailboxes).|
|**Huidige gebruikersconnector**|Iedereen verstuurt e-mail vanaf het account waarmee ze zich hebben aangemeld bij [!INCLUDE[prod_short](includes/prod_short.md)].|Communicatie vanuit individuele accounts toestaan.|
|**SMTP-connector**|SMTP-protocol gebruiken om e-mails te verzenden.|Communicatie via uw SMTP-mailserver toestaan. |

> [!NOTE]
> De extensies **Microsoft 365-connector** en **Huidige gebruikersconnector** gebruiken de accounts die u voor gebruikers instelt in het Microsoft 365-beheercentrum, voor uw Microsoft 365-abonnement. Om e-mail te verzenden met de extensies moeten gebruikers een geldige licentie hebben voor Exchange Online. In sandboxomgevingen vereisen deze extensies, inclusief de extensie **Outlook REST API**, dat de instelling **HttpClient-aanvragen toestaan** is geactiveerd. Als u wilt controleren of het voor deze extensies is ingeschakeld, gaat u naar de pagina **Extensiebeheer**, kiest u de extensie en kiest u vervolgens de optie **Configureren**.

> Externe gebruikers, zoals gedelegeerde beheerders en externe accountants, kunnen deze extensies niet gebruiken om e-mailberichten te verzenden vanuit [!INCLUDE[prod_short](includes/prod_short.md)].

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4JsUk]

## <a name="use-smtp"></a>SMTP gebruiken

Als u het SMTP-protocol wilt gebruiken om e-mails te verzenden vanaf [!INCLUDE[prod_short](includes/prod_short.md)], kunt u de extensie SMTP-connector gebruiken. Wanneer u een account instelt dat SMTP gebruikt, is het veld **Type afzender** belangrijk. Als u **Specifieke gebruiker** kiest, worden e-mails verzonden met de naam en andere informatie van het account dat u instelt. Als u echter **Huidige gebruiker** kiest, worden e-mails verzonden vanaf het e-mailaccount dat is opgegeven voor het account van elke gebruiker. Huidige gebruiker is vergelijkbaar met de functie Verzenden als. Voor meer informatie zie [Een vervangend afzenderadres gebruiken voor uitgaande e-mailberichten](admin-how-setup-email.md#use-a-substitute-sender-address-on-outbound-email-messages). 

> [!IMPORTANT]
> Als u OAuth voor SMTP wilt gebruiken, moeten alle gebruikers zich op dezelfde Microsoft Entra-tenant bevinden. 
> 
> U moet een toepassingsregistratie maken in de Azure-portal en vervolgens de begeleide instelling **Microsoft Entra ID instellen** in [!INCLUDE[prod_short](includes/prod_short.md)] gebruiken om verbinding te maken met Microsoft Entra ID. Zie voor meer informatie [Een app-registratie voor Business Central maken in Azure Portal](admin-how-setup-email.md#create-an-app-registration-for-business-central-in-azure-portal).
>
> Exchange Online schaft het gebruik van basisverificatie voor SMTP af. Tenants die momenteel SMTP AUTH gebruiken, worden niet beïnvloed door deze wijziging. We raden echter ten zeerste aan om de nieuwste versie van [!INCLUDE [prod_short](includes/prod_short.md)] te gebruiken en OAuth 2.0-verificatie voor SMTP in te stellen. We zullen geen op certificaten gebaseerde verificatie toevoegen voor eerdere versies van [!INCLUDE [prod_short](includes/prod_short.md)], bijvoorbeeld versie 14. Als u geen OAuth 2.0-authenticatie kunt instellen, raden we u aan alternatieven van derden te verkennen als u SMTP-e-mail in eerdere versies wilt gebruiken.

[!INCLUDE [email-copy-company](includes/email-copy-company.md)]

## <a name="use-the-set-up-email-assisted-setup-guide"></a>De begeleide instelling E-mail instellen gebruiken

De begeleide instelling **E-mail instellen** kan u helpen snel aan de slag te gaan met e-mails.

> [!NOTE]
> U moet een standaard e-mailaccount hebben, zelfs als u slechts één account toevoegt. Het standaardaccount wordt gebruikt voor alle e-mailscenario's die niet aan een account zijn toegewezen. Meer informatie op [E-mailscenario's toewijzen aan e-mailaccounts](admin-how-setup-email.md#assign-email-scenarios-to-email-accounts).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **E-mailaccounts instellen** in en kies vervolgens de gerelateerde koppeling.
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 


<!--
> [!NOTE]
> If you choose **Other (SMTP)** and are using an account that requires two-factor authentication, the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription, and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords). 

is this still true?-->
## <a name="assign-email-scenarios-to-email-accounts"></a>E-mailscenario's toewijzen aan e-mailaccounts

E-mailscenario's zijn processen waarbij een document wordt verzonden. Bijvoorbeeld een verkoop- of inkooporder of een melding, zoals een uitnodiging aan een externe accountant. U kunt specifieke e-mailaccounts gebruiken voor specifieke scenario's. U kunt bijvoorbeeld specificeren dat alle gebruikers altijd verkoopdocumenten verzenden vanaf het ene account, inkoopdocumenten vanuit een ander en magazijn- of productiedocumenten vanaf een derde account. U kunt scenario's toewijzen, opnieuw toewijzen en verwijderen wanneer u maar wilt. Een scenario kan slechts aan één e-mailaccount tegelijk worden toegewezen. Het standaardaccount voor e-mail wordt gebruikt voor alle scenario's die niet aan een account zijn toegewezen.

Op de pagina **Toewijzing van e-mailscenario** kunt u de actie **Standaardbijlagen instellen** kiezen om bijlagen aan e-mailscenario's toe te voegen. De bijlagen zijn altijd beschikbaar wanneer u een e-mail opstelt voor een document dat betrekking heeft op het scenario. Elk e-mailscenario kan een of meer standaardbijlagen hebben. Standaardbijlagen worden automatisch toegevoegd aan e-mails voor het e-mailscenario. Als u bijvoorbeeld een verkooporder per e-mail verzendt, wordt de standaardbijlage die is opgegeven voor het scenario Verkooporder toegevoegd. Standaardbijlagen worden weergegeven in de sectie **Bijlagen** onderaan de pagina **Een e-mail opstellen**. U kunt handmatig niet-standaardbijlagen aan de e-mail toevoegen.

<!--
## <a name="to-set-up-email"></a>To set up email
1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > If you are using an account that requires two-factor authentication, then the password that you enter in the **Password** field must be the same that you use for your Microsoft 365 subscription and it must be of type **App Password**. For more information, see [Manage app passwords for two-step verification](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Alternatively, choose the **Apply Microsoft 365 Server Settings** action to insert any information that is already defined for your Microsoft 365 subscription.
4. When all the fields are correctly filled in, choose the **Test Email Setup** action.
5. When the test succeeds, close the page.

-->

## <a name="set-up-view-policies"></a>Weergavebeleid instellen

U kunt de e-mailberichten beheren waartoe een gebruiker toegang heeft op de pagina's Postvak UIT en Verzonden e-mails.

Kies bij **E-mailweergavebeleid van gebruiker** een gebruiker en kies vervolgens een van de volgende opties in het veld **E-mailweergavebeleid**:

* **Eigen e-mails weergeven**: de gebruiker kan alleen de eigen e-mailberichten bekijken.
* **Alle e-mails weergeven**: de gebruiker kan alle e-mailberichten bekijken, inclusief e-mails die door andere gebruikers zijn verzonden.
* **Weergeven bij toegang tot alle gerelateerde records**: dit weergavebeleid wordt gebruikt als er geen ander beleid is opgegeven. Een gebruiker kan e-mailberichten bekijken die andere gebruikers hebben verzonden als de gebruiker toegang heeft tot de verzonden record en alle gerelateerde records. Gebruiker A heeft bijvoorbeeld een geboekte verkoopfactuur naar een klant verzonden. Gebruiker B kan het e-mailbericht bekijken als hij of zij toegang heeft tot zowel de factuur als de klant.
* **Weergeven bij toegang tot gerelateerde records**: de gebruiker kan e-mailberichten bekijken die door andere mensen zijn verzonden als de gebruiker toegang heeft tot ten minste één record die gerelateerd is aan de verzonden record. Gebruiker A heeft bijvoorbeeld een geboekte verkoopfactuur naar een klant verzonden. Gebruiker B kan het e-mailbericht bekijken als hij of zij toegang heeft tot de factuur of de klant.

> [!NOTE]
> Als u het veld **Gebruikers-id** leeg laat en vervolgens de actie **E-mailweergavebeleid** kiest, is het beleid dat u definieert, van toepassing op alle gebruikers.

## <a name="specify-how-many-messages-an-account-can-send-per-minute"></a>Geef op hoeveel berichten een account per minuut kan verzenden

Sommige e-mailproviders (ISP's) beperken het aantal e-mailberichten dat een e-mailaccount in één keer, of binnen een bepaalde tijd, of beide kan verzenden. Deze praktijk staat bekend als *e-mailbeperking* en helpt ISP's het verkeer op hun servers te controleren en spam te voorkomen. Als een e-mailaccount de limiet overschrijdt, kan de ISP de berichten blokkeren. Om ervoor te zorgen dat het aantal berichten dat u verstuurt vanuit [!INCLUDE [prod_short](includes/prod_short.md)] voldoet aan de limiet van uw ISP, geeft u de limiet op voor elk van uw e-mailaccounts.

De standaardlimiet voor de accounttypen Microsoft 365 en Huidige gebruiker is 30, wat overeenkomt met de limiet die is ingesteld door Exchange Online.

Er zijn twee manieren om de limiet op te geven.

* Wanneer u de begeleide instelling voor het instellen van e-mail gebruikt om een nieuw account aan te maken, geeft u de limiet op in het veld **Frequentielimiet per minuut** .
* Geef voor bestaande e-mailaccounts de limiet op in het veld **E-mailfrequentielimiet** van het account.

## <a name="set-up-reusable-email-texts-and-layouts"></a>Herbruikbare e-mailteksten en lay-outs instellen

U kunt rapporten gebruiken om belangrijke informatie uit verkoop-, inkoop- en servicedocumenten op te nemen in teksten voor e-mails. Rapportlay-outs bepalen de stijl en de inhoud van de tekst in de e-mail. De inhoud kan bijvoorbeeld tekst bevatten zoals een begroeting of instructies die voorafgaan aan de documentinformatie. Deze procedure beschrijft hoe u het rapport **Verkoop - Factuur** voor geboekte verkoopfacturen instelt, maar het proces is vergelijkbaar voor andere rapporten.

> [!NOTE]
> Als u de lay-out wilt gebruiken om inhoud voor e-mailberichten te maken, moet u het Word-bestandstype voor uw lay-out gebruiken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rapportselectie - verkoop** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Rapportselectie - Verkoop** in het veld **Gebruik** de optie **Factuur**.
3. Selecteer op een nieuwe regel in het veld **Rapport-ID** bijvoorbeeld standaardrapport 1306.
4. Schakel het selectievakje **Gebruiken voor hoofdtekst van e-mailbericht** in.
5. Kies het veld **Indelingsomschrijving van hoofdtekst van e-mailbericht** en selecteer vervolgens een lay-out in de lijst.
6. Als u de lay-out wilt weergeven of bewerken waarop de e-mailtekst is gebaseerd, selecteert u op de pagina **Aangepaste rapportlay-outs** de lay-out en kiest u vervolgens de actie **Lay-out exporteren**. Als u de lay-out aanpast, gebruikt u de actie **Lay-out importeren** om de nieuwe lay-out te uploaden.
    > [!NOTE]
    > Om een standaard rapportlay-out aan te passen, zoals 1306, moet u een kopie van het rapport maken. [!INCLUDE [prod_short](includes/prod_short.md)] helpt u bij het maken van een kopie wanneer u een aangepaste lay-out voor een standaardrapport importeert. De naam van uw nieuwe aangepaste rapportlay-out wordt voorafgegaan door 'Kopie van'.
7. Als u klanten een betalingsservice, zoals PayPal, wilt laten gebruiken, moet u de service instellen. Daarna worden de PayPal-gegevens en de koppeling in de e-mailtekst ingevoegd. Zie [Klantbetalingen via PayPal inschakelen](sales-how-enable-payment-service-extensions.md) voor meer informatie.
8. Kies de knop **OK**.

Wanneer u nu bijvoorbeeld de actie **Verzenden** kiest op de pagina **Geboekte verkoopfactuur**, bevat de e-mailhoofdtekst de documentgegevens van rapport 1306, voorafgegaan door standaardtekst die is geformatteerd volgens de rapportlay-out die u in stap 5 hebt geselecteerd.

## <a name="use-a-substitute-sender-address-on-outbound-email-messages"></a>Een vervangend afzenderadres gebruiken voor uitgaande e-mailberichten

Als u de extensie SMTP-connector gebruikt, kunt u de mogelijkheden **Verzenden als** of **Verzenden namens** vanuit Microsoft Exchange gebruiken om het afzenderadres van uitgaande berichten te wijzigen. [!INCLUDE[prod_short](includes/prod_short.md)] zal het SMTP-account gebruiken om te verifiëren bij Exchange, maar zal het afzenderadres vervangen door het adres dat u opgeeft, of het wijzigen met 'namens'.

Wanneer u een account maakt en u wilt de mogelijkheden Verzenden als of Verzenden namens uit Exchange gebruiken, kiest u in het veld **Type afzender** de optie **Specifieke gebruiker**.

Als alternatief kunt u kiezen voor **Huidige gebruiker** zodat mensen berichten kunnen verzenden via de SMTP-connector. Het bericht lijkt te zijn verzonden vanaf het e-mailaccount dat is opgegeven in het veld Contact-e-mail op de gebruikerskaart voor de gebruiker waarmee ze zijn aangemeld. Het werkt echter vergelijkbaar met de functie Verzenden als en wordt verzonden vanaf het account dat is opgegeven in de instellingen van de SMTP-connector.

Hierna volgen voorbeelden van hoe Verzenden als en Verzenden namens worden gebruikt in [!INCLUDE[prod_short](includes/prod_short.md)]:

* U wilt mogelijk dat de inkoop- of verkooporders die u naar leveranciers en klanten verzendt, afkomstig lijken te zijn van een _noreply@yourcompanyname.com_-adres.
* Wanneer uw werkstroom een goedkeuringsverzoek per e-mail verzendt met behulp van het e-mailadres van de aanvrager.

> [!Note]
> U kunt slechts één account gebruiken om afzenderadressen te vervangen. Dat wil zeggen, u kunt niet één vervangend adres hebben voor inkoopprocessen en een ander voor verkoopprocessen.

<!--
### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>To set up the substitute sender address for all outbound email messages
1. In the **Exchange admin center** for your Microsoft 365 account, find the mailbox to use as the substitute address, and then copy or make a note of the address. If you need a new address, go to your Microsoft 365 admin center to create a new user and set up their mailbox.
2. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
3. In the **Send As** field, enter the substitute address.
4. Copy or make a note of the address in the **User ID** field.
5. In the **Exchange admin center**, find the mailbox to use as the substitute address, and then enter the address from the **User ID** field in the **Send As** field. For more information, see [Use the EAC to assign permissions to individual mailboxes](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>To use the substitute address in approval workflows
1. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
2. Copy or make a note of the address in the **User ID** field.
3. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Approval User Setup**, and then choose the related link.
4. In the **Exchange admin center**, find the mailboxes for each user listed in the **Approval User Setup** page, and in the **Send As** field enter the address from the **User ID** field of the **SMTP Email Setup** page in [!INCLUDE[prod_short](includes/prod_short.md)]. For more information, see [Manage permissions for recipients](/Exchange/recipients/mailbox-permissions?view=exchserver-2019&preserve-view=true).
5. In [!INCLUDE[prod_short](includes/prod_short.md)] choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **SMTP Email Setup**, and then choose the related link.
6. To enable substitution, turn on the **Allow Sender Substitution** toggle.

> [!Note]
> [!INCLUDE[prod_short](includes/prod_short.md)] will determine which address to display in the following order: <br><br> 1. The address specified in the **E-Mail** field on the **Approval User Setup** page for messages in a workflow. <br> 2. The address specified in the **Send As** field in the **SMTP Email Setup** page. <br> 3. The address specified in the **User ID** field in the **SMTP Email Setup** page. -->

## <a name="set-up-document-sending-profiles"></a>Verzendprofielen van documenten instellen

U kunt tijd besparen door voor elk van uw klanten een voorkeursmethode voor het verzenden van verkoopdocumenten in te stellen. U hoeft niet elke keer dat u een document verzendt een verzendoptie te selecteren, zoals of u het document per e-mail of als elektronisch document wilt verzenden. Zie [Verzendprofielen voor documenten instellen](sales-how-setup-document-send-profiles.md) voor meer informatie.

## <a name="optional-set-up-email-logging-in-exchange-online"></a>Optioneel: E-maillogboekregistratie instellen in Exchange Online

Haal meer uit de communicatie tussen verkopers en uw bestaande of potentiële klanten. U kunt e-mailuitwisselingen volgen en deze vervolgens omzetten in bruikbare verkoopkansen. Meer informatie op [E-mailberichtuitwisselingen volgen tussen verkopers en contactpersonen](marketing-set-up-email-logging.md).  
<!--
[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Next, you connect [!INCLUDE[prod_short](includes/prod_short.md)] with Exchange Online. For more information, see [Track Email Message Exchanges Between Salespeople and Contacts](marketing-set-up-email-logging.md).  -->

## <a name="optional-monitor-email-usage-and-troubleshoot-email-failures-with-telemetry"></a>Optioneel: bewaak het e-mailgebruik en los e-mailfouten op met telemetrie

Beheerders kunnen de telemetriefunctie inschakelen in [!INCLUDE[prod_short](includes/prod_short.md)] om gegevens te krijgen over het gebruik en storingen van verschillende mogelijkheden in het systeem. Voor e-mail loggen we de volgende bewerkingen:

- Een e-mail is succesvol verzonden  
- Een poging om een e-mail te verzenden is mislukt   
- Verificatie bij een SMTP-server geslaagd/mislukt  
- Verbinding met een SMTP-server geslaagd/mislukt  

U kunt deze gegevens gebruiken om het e-mailgebruik te controleren en om e-mailstoringen op te lossen. Ga voor meer informatie naar [E-mailtelemetrie analyseren (beheerinhoud)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace).  

## <a name="set-up-email-for-business-central-on-premises"></a>E-mail instellen voor Business Central On-Premises

[!INCLUDE[prod_short](includes/prod_short.md)] on-premises kan worden geïntegreerd met services die zijn gebaseerd op Microsoft Azure. U kunt bijvoorbeeld Cortana Intelligence voor slimmere cashflowprognoses gebruiken, Power BI gebruiken om uw bedrijf te visualiseren en Exchange Online gebruiken voor het verzenden van e-mail. Integratie met deze services is gebaseerd op een app-registratie in Microsoft Entra ID. De app-registratie biedt verificatie- en autorisatieservices voor communicatie. Om de e-mailmogelijkheden in [!INCLUDE[prod_short](includes/prod_short.md)] on-premises te gebruiken, moet u [!INCLUDE[prod_short](includes/prod_short.md)] registreren als een app in de Azure Portal en vervolgens [!INCLUDE[prod_short](includes/prod_short.md)] verbinden met de app-registratie. In de volgende secties wordt uitgelegd hoe u dat doet.

### <a name="create-an-app-registration-for-business-central-in-azure-portal"></a>Een appregistratie voor Business Central maken in Azure Portal

De stappen om [!INCLUDE[prod_short](includes/prod_short.md)] te registreren in Azure Portal worden beschreven in [Een toepassing registreren in Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory).

> [!NOTE]
> Om de e-mailfuncties te gebruiken moet uw app-registratie een multitenantconfiguratie gebruiken.

De instellingen die specifiek zijn voor de e-mailmogelijkheden, zijn de gedelegeerde machtigingen die u verleent aan uw app-registratie. De volgende tabel bevat de minimale machtigingen.

|API-/machtigingsnaam  |Soort  |Omschrijving  |
|---------|---------|---------|
|Microsoft Graph/User.Read |Gedelegeerd|Aanmelden en gebruikersprofiel lezen.         |
|Microsoft Graph/Mail.ReadWrite |Gedelegeerd|E-mailberichten opstellen.         |
|Microsoft Graph/Mail.Send|Gedelegeerd|E-mailberichten verzenden.         |
|Microsoft Graph / offline_access|Gedelegeerd|Toestemming voor gegevenstoegang behouden.|

Als u de extensie SMTP-connector gebruikt en OAuth 2.0 voor verificatie wilt gebruiken, zijn de machtigingen iets anders. De volgende tabel bevat de machtigingen.

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

Meer informatie over algemene richtlijnen voor het registreren van een app op [Quickstart: een toepassing registreren bij het Microsoft-identiteitsplatform](/azure/active-directory/develop/quickstart-register-app).

> [!NOTE]
Als u problemen ondervindt bij het gebruik van het SMTP-protocol om e-mail te verzenden nadat u [!INCLUDE[prod_short](includes/prod_short.md)] hebt verbonden met uw appregistratie, kan het zijn dat SMTP AUTH niet is ingeschakeld voor uw tenant. We raden u aan om in plaats daarvan de e-mailconnectoren Microsoft 365 en Huidige gebruiker te gebruiken, omdat deze de API's van Microsoft Graph Mail gebruiken. Als u echter het SMTP-protocol moet gebruiken, kunt u SMTP AUTH inschakelen. Zie voor meer informatie [Geverifieerde client SMTP-verzending (SMTP AUTH) in- of uitschakelen Exchange Online](/exchange/clients-and-mobile-in-exchange-online/authenticated-client-smtp-submission#disable-smtp-auth-in-your-organization).

### <a name="connect--to-your-app-registration"></a>[!INCLUDE[prod_short](includes/prod_short.md)] verbinden met uw app-registratie

Nadat u uw toepassing in Azure Portal hebt geregistreerd, gebruikt u in [!INCLUDE[prod_short](includes/prod_short.md)] de pagina **Microsoft Entra ID-registratie van e-mailtoepassing** om [!INCLUDE[prod_short](includes/prod_short.md)] ermee te verbinden.

1. Kies in [!INCLUDE[prod_short](includes/prod_short.md)] het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Microsoft Entra ID-registratie van e-mailtoepassing** in en kies vervolgens de gerelateerde koppeling.
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Als alternatief, als u voor de eerste keer verbinding maakt, kunt u de begeleide instelling **E-mail instellen** uitvoeren. In dit geval bevat de guide ook de Microsoft Entra ID-registratiepagina voor e-mailtoepassingen voor het toevoegen van de informatie voor het verbinden met uw app-registratie. <!--Need to verify this too. Ask John to clear the aad settings, delete the email accounts, and then run the guide.-->

<!--

1. In [!INCLUDE[prod_short](includes/prod_short.md)], start the **Email Application AAD Registration** assisted setup guide.
2. On the first page of the guide, copy the value in the **Redirect URL** field.
3. In Microsoft Entra ID, search for **App registrations**, and then open the **App registrations** page.
4. Choose **New registration**.
5. In the **Name** field, enter a name for your app.
6. Under **Supported account types**, choose either the **Accounts in any organizational directory (Any Microsoft Entra Directory - Multitenant)** or **Accounts in any organizational directory (Any Microsoft Entra Directory - Multitenant) and personal Microsoft accounts (/e.g. Skype, Xbox)** options, depending on your needs. If you're unsure, choose **Help me choose** for more information.
7. Under **Redirect URI (optional)**, choose **Web**, paste the URL you copied from the **Redirect URL** field in the assisted setup guide in Business Central, and then choose **Register**.
8. On the navigation pane, choose **Overview**, and then copy the value in the **Application (client) ID** field.
9. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide, paste the ID in **Client ID** field.
10. In Microsoft Entra ID, on the navigation pane, choose **API permissions**, and then choose **Add a permission**.
11. On the **Request API permissions** pane, on the **Microsoft APIs** tab, choose **Microsoft Graph**.  
12. Choose **Delegated permissions**, and then in the **Select permissions** field, search for **Mail.ReadWrite**, **Mail.Send**, and **offline_access**. Choose those permissions, and then choose **Add permissions**.
13. On the navigation pane, choose **Certificates & secrets**.
14. Under **Client secrets**, choose **New client secret**.
15. Under **Add a client secret**, enter a description of the client, specify how long you want your secret to be available, and then choose **Add**.
16. When the secret is generated, copy it. 
17. In [!INCLUDE[prod_short](includes/prod_short.md)], in the assisted setup guide paste the secret in the **Client Secret field**.
18. The **Verify Registration** button becomes available. 

-->

## <a name="see-also"></a>Zie ook

[Gedeelde postbussen in Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Instellen van [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Documenten verzenden via e-mail](ui-how-send-documents-email.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met behulp van extensies](ui-extensions.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken als uw bedrijfsinbox in Outlook](admin-outlook.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] installeren op mijn mobiele apparaat](install-mobile-app.md)   
[[!INCLUDE[prod_short](includes/prod_short.md)] installeren op mijn mobiele apparaat](install-mobile-app.md)   
[E-mailtelemetrie analyseren (beheerinhoud)](/dynamics365/business-central/dev-itpro/administration/telemetry-email-trace)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
