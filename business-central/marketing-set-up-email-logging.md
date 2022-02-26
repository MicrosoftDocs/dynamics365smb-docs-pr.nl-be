---
title: E-maillogboekregistratie instellen | Microsoft Docs
description: Leer hoe u e-mailinteracties tussen verkopers en klanten kunt omzetten in echte opportunities.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: c1e47dba1c10b994cb43c21afbfdd548f85c774b
ms.sourcegitcommit: 04055135ff13db551dc74a2467a1f79d2953b8ed
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/08/2021
ms.locfileid: "7482359"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a>E-mailberichtuitwisselingen volgen tussen verkopers en contactpersonen

Haal meer uit de communicatie tussen verkopers en uw bestaande of potentiële klanten door e-mailuitwisselingen bij te houden en deze vervolgens om te zetten in bruikbare kansen. [!INCLUDE[prod_short](includes/prod_short.md)] kan werken met Exchange Online om een logboek bij te houden van de inkomende en uitgaande berichten. U kunt de inhoud van elk bericht bekijken en analyseren op de pagina **Interactielogposten**.

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a>Openbare mappen en regels instellen voor e-mailregistratie in Exchange Online

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

Vervolgens verbindt u [!INCLUDE[prod_short](includes/prod_short.md)] met Exchange Online.

## <a name="setting-up-prod_short-to-log-email-messages"></a>[!INCLUDE[prod_short](includes/prod_short.md)] instellen om e-mailberichten te registreren

Ga aan de slag met e-maillogboekregistratie in twee eenvoudige stappen:

1. Verbind [!INCLUDE[prod_short](includes/prod_short.md)] met Exchange Online voor uw Microsoft 365-abonnement. Exchange Online behandelt uw e-mailberichten. We hebben deze stap eenvoudig gemaakt door een begeleide instelling te bieden. U hebt alleen uw beheerdersreferenties nodig voor uw beheerdersaccount in Microsoft 365. Start de guide door naar **Begeleide instelling** te gaan en vervolgens de guide **E-maillogboekregistratie instellen** te kiezen.  

2. Zorg ervoor dat geldige e-mailadressen zijn ingevoerd [!INCLUDE[prod_short](includes/prod_short.md)] voor uw verkopers en contacten, afhankelijk van of ze potentiële of bestaande klanten zijn. Om dit te doen opent u voor elke klant of verkoper de kaart **Contact** of **Verkoper/Koper** en kijkt u naar het veld **E-mail**.

> [!Tip]
> Nadat u de stappen in de guide hebt voltooid, kunt u controleren of de verbinding is geslaagd. Zoek **Marketinginstellingen** en selecteer **Toegang**, dan **Functies** en dan **Instellingen voor e-maillogboekregistratie valideren**.

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a>Uitwisseling van e-mailberichten bekijken in het interactielogboek

[!INCLUDE[prod_short](includes/prod_short.md)] maakt een post op de pagina **Interactielogboek** telkens wanneer een verkoper en een contactpersoon een e-mailbericht uitwisselen. Om het interactielogboek te bekijken opent u de kaart **Contact** voor de persoon, kiest u **Verwant**, dan **Historie** en vervolgens **Interactielogposten**. Er zijn een paar dingen die u met elke post in het logboek kunt doen, bijvoorbeeld:

- De inhoud bekijken van het e-mailbericht dat is uitgewisseld door **Verwerken** te selecteren en vervolgens **Bijlagen weergeven**.
- Een e-mailuitwisseling veranderen in een opportunity. Als een item er veelbelovend uitziet, kunt u er een opportunity van maken en vervolgens de voortgang naar een verkoop beheren. Om dit te doen selecteert u de post en selecteert u vervolgens **Verwerken** en dan **Opportunity maken**. Zie voor meer informatie [Verkoopopportunities beheren](marketing-manage-sales-opportunities.md).

## <a name="connecting-on-premises-versions-to-microsoft-exchange"></a>On-premises versies verbinden met Microsoft Exchange

U kunt [!INCLUDE[prod_short](includes/prod_short.md)] on-premises met Exchange on-premises of Exchange Online verbinden voor e-mailregistratie. Voor beide versies van Exchange zijn instellingen voor de verbinding beschikbaar op de pagina **Marketinginstellingen**. Voor Exchange Online kunt u ook een begeleide instelling gebruiken.

### <a name="connecting-to-exchange-on-premises"></a>Verbinding maken met Exchange on-premises

Als u [!INCLUDE[prod_short](includes/prod_short.md)] on-premises wilt verbinden met Exchange on-premises, kunt u op de pagina **Marketinginstellingen** **Basis** gebruiken als het **Verificatietype** en vervolgens referenties invoeren voor het gebruikersaccount voor Exchange on-premises. Schakel vervolgens de schakelaar **Ingeschakeld** in om te beginnen met het registreren van e-mail.

### <a name="connecting-to-exchange-online"></a>Verbinding maken met Exchange Online

Om verbinding te maken met Exchange Online moet u **OAuth2** gebruiken als het **Verificatietype**. U moet ook een toepassing registreren in Azure Active Directory en de toepassings-id, het sleutelkluisgeheim en de omleidings-URL opgeven die moet worden gebruikt. De omleidings-URL wordt vooraf ingevuld en zou voor de meeste installaties moeten werken. Zie voor meer informatie Een toepassing registreren in Azure AD voor verbinding vanuit Business Central met Exchange Online, hieronder.

U moet uw installatie instellen om HTTPS te gebruiken. Zie voor meer informatie [SSL configureren om de Business Central Web Client-verbinding te beveiligen](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Als u uw server instelt om een andere startpagina te hebben, kunt u de URL wijzigen. Het clientgeheim wordt opgeslagen als een versleutelde tekenreeks in uw database.

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-exchange-online"></a>Een toepassing registreren in Azure AD voor verbinding van Business Central met Exchange Online

Bij de volgende stappen wordt ervan uitgegaan dat u Azure Active Directory gebruikt om identiteiten en toegang te beheren. Zie voor meer informatie [Snelle start: een toepassing registreren bij het Microsoft-identiteitsplatform](/azure/active-directory/develop/quickstart-register-app). Als u Azure Active Directory niet gebruikt, raadpleegt u [Een andere identiteits- en toegangsbeheerservice gebruiken](marketing-set-up-email-logging.md#using-another-identity-and-access-management-service). 

1. Kies in de Azure Portal onder **Beheren** **Verificatie**.
2. Voeg onder **Omleidings-URL** de omleidings-URL toe die wordt voorgesteld op de pagina **Marketinginstellingen** in [!INCLUDE[prod_short](includes/prod_short.md)]. Als de omleidings-URL op de pagina Marketinginstellingen leeg is, zoekt u de voorgestelde omleidings-URL op de pagina **Begeleide instelling E-maillogboekregistratie**.

    > [!NOTE]
    > Als u de omleidings-URL niet opgeeft, kunt u dit later doen door **Een platform toevoegen** te kiezen en dan **Web** te kiezen om de webtoepassing en de omleidings-URL toe te voegen. 

3. Kies onder **Beheren** **Manifest**.
4. Zoek de eigenschap **requiredResourceAccess** in het manifest en voeg de volgende code tussen haakjes ([]) toe om de vereiste machtigingen toe te voegen. Zie [Uw toepassing registreren](/exchange/client-developer/exchange-web-services/how-to-authenticate-an-ews-application-by-using-oauth#register-your-application) voor meer informatie.

```
{
    "resourceAppId": "00000002-0000-0ff1-ce00-000000000000",
    "resourceAccess": [
        {
            "id": "3b5f3d61-589b-4a3c-a359-5dd4b5ee5bd5",
            "type": "Scope"
        },
        {
            "id": "dc890d15-9560-4a4c-9b7f-a736ec74ec40",
            "type": "Role"
        }
    ]
}
```

5. Kies **Opslaan**.
6. Kies onder **Beheer** **API-machtigingen** en controleer of de volgende machtigingen worden vermeld:  

    * EWS.AccessAsUser.All
    * full_access_as_app

7. Kies onder **Beheren** **Certificaten en geheimen** en maak vervolgens een nieuw geheim voor uw app. U gebruikt het geheim in [!INCLUDE[prod_short](includes/prod_short.md)], in het veld **Clientgeheim** op de pagina **Marketinginstellingen** of slaat het op een veilige plaats op en verschaft het in een gebeurtenisabonnee.
8. Kies **Overzicht** en zoek de waarde **Toepassing (client)-id**. Dit is de client-id van uw toepassing. U moet deze invoeren op de pagina **Marketinginstellingen** in het veld **Client-id** of op een veilige plaats opslaan en verschaffen in een gebeurtenisabonnee.
9. Stel in [!INCLUDE[prod_short](includes/prod_short.md)] e-mailregistratie in op de pagina **Marketinginstellingen** of gebruik de begeleiding **Begeleide instelling E-maillogboekregistratie** voor hulp bij het proces.
    * Geef het e-mailaccount op van de gebruiker namens wie het geplande project verbinding met Exchange Online maakt en e-mails verwerkt. De gebruiker moet een geldige licentie hebben voor Exchange Online.
    * Geef de URL op voor uw Exchange Online. Meestal is dit het domein dat u heeft opgegeven in het e-mailadres van de gebruiker.
    * Verschaf het **Pad van wachtrijmap** en het **Pad van opslagmap**.
10. Schakel de schakelaar **Ingeschakeld** in om te beginnen met het registreren van e-mail.
11. Meld u aan met uw beheerdersaccount voor Azure Active Directory (dit account moet een geldige licentie hebben voor Exchange en een beheerder zijn in uw Exchange Online). Nadat u zich hebt aangemeld, wordt u gevraagd toe te staan dat uw geregistreerde toepassing zich aanmeldt bij Exchange Online namens de organisatie. U moet toestemming geven om de instelling te voltooien.

   > [!NOTE]
   > Als u niet wordt gevraagd om u aan te melden met uw beheerdersaccount, komt dit waarschijnlijk omdat pop-ups worden geblokkeerd. Sta pop-ups vanaf https://login.microsoftonline.com toe om u aan te melden.

### <a name="using-another-identity-and-access-management-service"></a>Een andere identiteits- en toegangsbeheerservice gebruiken
Als u Azure Active Directory niet gebruikt om identiteiten en toegang te beheren, hebt u wat hulp nodig van een ontwikkelaar. Als u de app-id en het geheim liever op een andere locatie opslaat, kunt u de velden Client-id en Clientgeheim leeg laten en een extensie schrijven om de id en het geheim van de locatie op te halen. U kunt het geheim tijdens runtime verstrekken door u te abonneren op de gebeurtenissen OnGetEmailLoggingClientId en OnGetEmailLoggingClientSecret in codeunit 1641 'E-maillogboekregistratie instellen'.

### <a name="to-stop-logging-email"></a>Stoppen met registratie van e-mail
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voert u **Marketinginstellingen** in en kiest u vervolgens de gerelateerde koppeling.
2. Zet de schakelaar **Ingeschakeld** uit.

## <a name="see-also"></a>Zie ook
[Relaties beheren](marketing-relationship-management.md)



[!INCLUDE[footer-include](includes/footer-banner.md)]