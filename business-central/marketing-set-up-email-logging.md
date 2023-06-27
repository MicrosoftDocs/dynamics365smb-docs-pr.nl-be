---
title: E-maillogboekregistratie instellen
description: Leer hoe u e-mailinteracties tussen verkopers en klanten kunt omzetten in echte opportunities.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: dcenic
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.keywords: 'relationship, prospect, opportunity, email'
ms.search.form: '1680, 1811, 5076'
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts" />E-mailberichtuitwisselingen volgen tussen verkopers en contactpersonen

Haal meer uit de communicatie tussen uw verkopers en klanten door e-mailuitwisselingen om te zetten in bruikbare kansen. [!INCLUDE[prod_short](includes/prod_short.md)] kan werken met Exchange Online om een logboek bij te houden van de inkomende en uitgaande berichten. U kunt de inhoud van elk bericht bekijken en analyseren op de pagina **Interactielogposten**.

> [!IMPORTANT]
> Voor [!INCLUDE[prod_short](includes/prod_short.md)] online, [!INCLUDE[prod_short](includes/prod_short.md)] en Exchange Online moet van dezelfde tenant zijn.

## <a name="to-set-up-email-logging" />E-maillogboekregistratie instellen

### <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online" />Openbare mappen en regels instellen voor e-mailregistratie in Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Vervolgens verbindt u [!INCLUDE[prod_short](includes/prod_short.md)] met Exchange Online.

### <a name="set-up-a-shared-mailbox-and-rules-for-email-logging-in-exchange-online" />Een gedeelde mailbox en regel instellen voor e-maillogboekregistratie in Exchange Online

> [!NOTE]
> Voor deze stappen is beheerderstoegang vereist voor Exchange Online.

Bereid een gedeelde mailbox voor in het Exchange-beheercentrum. Als alternatief kunt u ook Exchange Online PowerShell gebruiken. Zie voor meer informatie [Een gedeelde mailbox maken](/microsoft-365/admin/email/create-a-shared-mailbox) of [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true).

> [!NOTE]
> Als u Exchange Management PowerShell gebruiken, zijn uw wijzigingen met vertraging beschikbaar in het Exchange-beheercentrum. De vertraging kan enkele uren duren.

### <a name="add-a-user-account-for-members-of-the-shared-mailbox" />Een gebruikersaccount toevoegen voor leden van de gedeelde mailbox

Het account dat u gaat gebruiken voor e-maillogboekregistratie is een Exchange Online-account. De geplande taak gebruikt het account om verbinding te maken met de gedeelde mailbox en e-mails te verwerken. Dit account mag niet aan een specifieke persoon worden gekoppeld. Voeg het e-mailaccount toe aan de leden voor de gedeelde mailbox. Zie voor meer informatie [De EAC gebruiken om delegatie van gedeelde mailboxen te bewerken](/exchange/collaboration-exo/shared-mailboxes#use-the-eac-to-edit-shared-mailbox-delegation).

### <a name="allow-other-users-to-see-logged-emails" />Toestaan dat andere gebruikers gelogde e-mails zien

U kunt een andere gebruiker toestaan om een e-mailbericht in Exchange te openen dat is gerelateerd aan een Interactielogpost van [!INCLUDE[prod_short](includes/prod_short.md)]. Om dat te doen geeft u de gebruiker ``Read``-machtiging voor de map **Archief** in de gedeelde mailbox. Zie [Exchange Online PowerShell](/powershell/exchange/exchange-online-powershell?view=exchange-ps&preserve-view=true) voor meer informatie.

### <a name="create-mail-flow-rules" />Regels voor e-mailstroom maken

Regels voor e-mailstroom zoeken naar specifieke voorwaarden voor berichten en ondernemen hierop actie. Maak twee e-mailstroomregels op basis van de informatie in de volgende tabel. Zie voor meer informatie [Poststroomregels beheren in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules?preserve-view=true) en [Poststroomregelacties in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-actions?preserve-view=true).

|Doel  |Name  |Pas deze regel toe als...  |Ga als volgt te werk...  |
|---------|---------|---------|---------|
|Een regel voor inkomende e-mail     |Naar deze organisatie verzonden e-mail registreren|De afzender bevindt zich buiten de organisatie en de ontvanger bevindt zich binnen de organisatie|BCC het e-mailaccount dat is opgegeven voor de gedeelde mailbox.|
|Een regel voor uitgaande e-mail     |Uit deze organisatie verzonden e-mail registreren|De afzender bevindt zich buiten de organisatie en de ontvanger bevindt zich binnen de organisatie.|BCC het e-mailaccount dat is opgegeven voor de gedeelde mailbox.|

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] verwerkt alleen berichten in de map Inbox in de gedeelde mailbox. Als door een regel berichten van de Inbox naar een andere map worden verplaatst, worden die berichten niet verwerkt. Bovendien worden berichten in de map Ongewenste e-mails ook genegeerd.

## <a name="set-up--to-log-email-messages" />[!INCLUDE[prod_short](includes/prod_short.md)] instellen om e-mailberichten te registreren

Ga aan de slag met e-maillogboekregistratie in twee eenvoudige stappen:

1. Verbind [!INCLUDE[prod_short](includes/prod_short.md)] met Exchange Online voor uw Microsoft 365-abonnement. Exchange Online behandelt uw e-mailberichten. We hebben deze stap eenvoudig gemaakt door een begeleide instelling te bieden. U hebt alleen uw beheerdersreferenties nodig voor uw beheerdersaccount in Microsoft 365. Start de guide door naar **Begeleide instelling** te gaan en vervolgens de guide **E-maillogboekregistratie instellen** te kiezen.  

2. Zorg ervoor dat de e-mailadressen van uw verkopers en contacten in [!INCLUDE[prod_short](includes/prod_short.md)] geldig zijn. Om dit te doen opent u voor elke klant of verkoper de kaart **Contact** of **Verkoper/Koper** en kijkt u naar het veld **E-mail**.

    > [!Tip]
    > Nadat u de stappen in de guide hebt voltooid, kunt u controleren of de verbinding is geslaagd. Zoek naar **E-maillogboekregistratie**, kies **Acties** en kies vervolgens **Instelling valideren**.

## <a name="view-email-message-exchanges-in-the-interaction-log" />Uitwisseling van e-mailberichten bekijken in het interactielogboek

[!INCLUDE[prod_short](includes/prod_short.md)] maakt een post op de pagina **Interactielogboek** telkens wanneer een verkoper en een contactpersoon een e-mailbericht uitwisselen. Om het interactielogboek te bekijken opent u de kaart **Contact** voor de persoon, kiest u **Verwant**, dan **Historie** en vervolgens **Interactielogposten**. Er zijn een paar dingen die u met elke post in het logboek kunt doen, bijvoorbeeld:

* De inhoud bekijken van het e-mailbericht dat is uitgewisseld door **Verwerken** te selecteren en vervolgens **Bijlagen weergeven**.
* Verander een e-mailuitwisseling in een verkoopkans. Als een item er veelbelovend uitziet, kunt u er een opportunity van maken en vervolgens de voortgang naar een verkoop beheren. Om van een e-mailuitwisseling een verkoopkans te maken, kiest u het item en vervolgens **Proces** en **Verkoopkans maken**. Zie voor meer informatie [Verkoopopportunities beheren](marketing-manage-sales-opportunities.md).

## <a name="mailbox-and-folder-limits-in-exchange-online" />Postbus- en maplimieten in Exchange Online

Er zijn postbus- en maplimieten in Exchange Online, zoals limieten voor mapgroottes en het aantal berichten. Voor meer informatie zie [Exchange Online-limieten](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#storage-limits) en [Limieten voor openbare mappen in Exchange Server](/Exchange/collaboration/public-folders/limits?view=exchserver-2019&preserve-view=true).

[!INCLUDE[prod_short](includes/prod_short.md)] slaat gelogde e-mailberichten op in een map in Exchange Online. [!INCLUDE[prod_short](includes/prod_short.md)] slaat ook een link op naar elk gelogd bericht. De links openen de gelogde berichten in Exchange Online vanuit de pagina's Interactielogposten, Contactkaart en Verkoperskaart in [!INCLUDE[prod_short](includes/prod_short.md)]. Als een gelogd bericht naar een andere map wordt verplaatst, wordt de link verbroken. Een bericht kan bijvoorbeeld handmatig worden verplaatst, of Exchange Online kan automatisch AutoSplit starten wanneer een opslaglimiet is bereikt.

De volgende stappen kunnen u helpen voorkomen dat koppelingen naar berichten in Exchange Online worden verbroken.

1. Verplaats bestaande berichten niet naar een andere map nadat u instellingen voor uw e-mailregistratie heeft gewijzigd. Door bestaande berichten te bewaren waar ze zijn, blijven de links behouden. Links naar berichten in de nieuwe map zijn geldig.
2. Vermijd het bereiken van de postbus- en maplimieten. Als u op het punt staat een limiet te bereiken, voert u de volgende stappen uit:
    1. Stel een nieuwe gedeelde mailbox in Exchange Online in.
    2. Werk uw e-mailstroomregels bij in Exchange Online.
    3. Werk uw instellingen voor e-mailregistratie in Business Central dienovereenkomstig bij

## <a name="connect-on-premises-versions-to-microsoft-exchange" />Verbind on-premises versies met Microsoft Exchange

U kunt [!INCLUDE[prod_short](includes/prod_short.md)] on-premises met Exchange on-premises of Exchange Online verbinden voor e-mailregistratie. Voor beide versies van Exchange zijn instellingen voor de verbinding beschikbaar op de pagina **Marketinginstellingen**. Voor Exchange Online kunt u ook een begeleide instelling gebruiken.

<!-- [!IMPORTANT]
> The new experience doesn't support a connection to Exchange on-premises. If you must use Exchange on-premises, do not enable the feature update for the new experience.

## <a name="connect-to-exchange-on-premises" />Connect to Exchange on-premises
<!--
## [Current Experience](#tab/current-experience)
To connect [!INCLUDE[prod_short](includes/prod_short.md)] on-premises to Exchange on-premises, on the **Marketing Setup** page, you can use **Basic** as the **Authentication Type**, and then enter credentials for the user account for Exchange on-premises. Then turn on the **Enabled** toggle to start logging email.

## [New Experience](#tab/new-experience)
The new experience does not support connections to Exchange on-premises.
-->
## <a name="connect-to-exchange-online" />Maak verbinding met Exchange Online

Als u verbinding wilt maken met Exchange Online, moet u een aanvraag registreren in Azure Active Directory. Geef de toepassings-id, het sleutelkluisgeheim en de omleidings-URL op voor de registratie. De omleidings-URL wordt vooraf ingesteld en zou voor de meeste installaties moeten werken. Zie voor meer informatie [Een toepassing registreren in Azure AD voor verbinding van Business Central met Exchange Online](marketing-set-up-email-logging.md#to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online). 

Om verbinding te maken moet u **OAuth2** gebruiken als het **Verificatietype**. U moet ook een aanvraag registreren in Azure Active Directory. Geef de toepassings-id, het sleutelkluisgeheim en de omleidings-URL op voor de registratie. De omleidings-URL wordt vooraf ingevuld en zou voor de meeste installaties moeten werken. Zie voor meer informatie Een toepassing registreren in Azure AD voor verbinding vanuit Business Central met Exchange Online, hieronder.

U moet uw installatie instellen om HTTPS te gebruiken. Zie voor meer informatie [SSL configureren om de Business Central Web Client-verbinding te beveiligen](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Als u uw server instelt om een andere startpagina te hebben, kunt u de URL wijzigen. Het clientgeheim wordt opgeslagen als een versleutelde tekenreeks in uw database.

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online" />Een toepassing registreren in Azure AD voor verbinding van Business Central met Exchange Online

Bij de volgende stappen wordt ervan uitgegaan dat u Azure Active Directory gebruikt om identiteiten en toegang te beheren. Zie voor meer informatie [Snelle start: een toepassing registreren bij het Microsoft-identiteitsplatform](/azure/active-directory/develop/quickstart-register-app). 

1. Kies in de Azure Portal onder **Beheren** **Verificatie**.
2. Voeg onder **Omleidings-URL** de omleidings-URL toe die wordt voorgesteld op de pagina **E-maillogboekregistratie** in [!INCLUDE[prod_short](includes/prod_short.md)]. Als het veld Omleidings-URL op de pagina E-maillogboekregistratie leeg is, zoekt u de voorgestelde omleidings-URL op de pagina **Begeleide instelling**. Om de pagina te openen kiest u op de pagina **E-maillogboekregistratie** de optie **Acties** en vervolgens **Begeleide instelling**.

    > [!NOTE]
    > Als u de omleidings-URL niet opgeeft, kunt u dit later doen door **Een platform toevoegen** te kiezen en dan **Web** te kiezen om de webtoepassing en de omleidings-URL toe te voegen.

3. Kies onder **Beheren** de optie **API-machtigingen**, en dan **Microsoft Graph** en **Gedelegeerde machtigingen**.
4. Gebruik het zoekvak om **Mail** te zoeken en te selecteren en voeg vervolgens de machtiging **Mail.ReadWrite.Shared** toe. 
5. Kies onder **Beheren** **Certificaten en geheimen** en maak vervolgens een nieuw geheim voor uw app. U gebruikt het geheim in het veld **Clientgeheim** op de pagina **E-maillogboekregistratie** in [!INCLUDE[prod_short](includes/prod_short.md)].
6. Kies **Overzicht** en zoek de waarde **Toepassing (client)-id**. Dit is de client-id van uw toepassing. U moet deze invoeren in het veld **Client-id** op de pagina **E-maillogboekregistratie**.
7. Stel in [!INCLUDE[prod_short](includes/prod_short.md)] e-mailregistratie in op de pagina **E-maillogboekregistratie** of gebruik de **Begeleide instelling** voor hulp.

### <a name="use-another-identity-and-access-management-service" />Een andere identiteits- en toegangsbeheerservice gebruiken

Als u Azure Active Directory niet gebruikt om identiteiten en toegang te beheren, hebt u wat hulp nodig van een ontwikkelaar. Als u de app-id en het geheim liever op een andere locatie opslaat, kunt u de velden Client-id en Clientgeheim leeg laten en een extensie schrijven om de id en het geheim van de locatie op te halen. U kunt het geheim tijdens runtime verstrekken door u te abonneren op de gebeurtenissen OnGetEmailLoggingClientId en OnGetEmailLoggingClientSecret in codeunit 1641 'E-maillogboekregistratie instellen'.

## <a name="to-start-logging-email" />Starten met registratie van e-mail

1. Schakel de schakelaar **Ingeschakeld** in om te beginnen met het registreren van e-mail op de pagina **E-maillogboekregistratie**.
2. Meld u aan met het account Exchange Online dat de geplande taak gebruikt om verbinding te maken met de gedeelde mailbox en e-mails te verwerken.

    > [!NOTE]
    > Als u niet wordt gevraagd om u aan te melden met uw Exchange Online-account, komt dit waarschijnlijk omdat pop-ups worden geblokkeerd in de browser. Sta pop-ups vanaf https://login.microsoftonline.com toe om u aan te melden.

## <a name="to-stop-logging-email" />Stoppen met registratie van e-mail

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **E-maillogboekregistratie** in en kies vervolgens de gerelateerde koppeling.
2. Zet de schakelaar **Ingeschakeld** uit.

## <a name="to-change-the-user-account-used-for-email-logging" />Het gebruikersaccount wijzigen dat wordt gebruikt voor e-maillogboekregistratie

### <a name="-online" />[!INCLUDE[prod_short](includes/prod_short.md)] Online

1. Meld u aan bij [!INCLUDE[prod_short](includes/prod_short.md)] met het account dat de geplande taak gebruikt om verbinding te maken met de gedeelde mailbox en e-mails te verwerken. Dit account moet toegang hebben tot [!INCLUDE[prod_short](includes/prod_short.md)] en Exchange Online.
2. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **E-maillogboekregistratie** in en kies vervolgens de gerelateerde koppeling. 
3. Kies **Verwant** en **Taakwachtrij-item**.
4. Herstart de taak **E-maillogboekregistratie**.

### <a name="-on-premises" />[!INCLUDE[prod_short](includes/prod_short.md)] on-premises

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **E-maillogboekregistratie** in en kies vervolgens de gerelateerde koppeling.
2. Kies **Acties** en dan **Token vernieuwen**.
3. Meld u aan met het account Exchange Online dat de geplande taak gebruikt om verbinding te maken met de gedeelde mailbox en e-mails te verwerken.

## <a name="see-also" />Zie ook
[Relaties beheren](marketing-relationship-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
