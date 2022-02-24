---
title: E-mail instellen in Business Central | Microsoft Docs
description: Hier wordt beschreven hoe u de SMTP-server van het bedrijf gebruikt om e-mailberichten te verzenden en ontvangen binnen Business Central, of hoe u de e-mailserverinstellingen gebruikt die met het Office 365-abonnement zijn gemaakt.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 9ece89b1d797d31a99c92f1bb292280b7f54ab7b
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187280"
---
# <a name="set-up-email"></a>E-mail instellen
Als u e-mails wilt versturen en ontvangen in [!INCLUDE[d365fin](includes/d365fin_md.md)], moet u de velden op de pagina **SMTP-mailinstellingen** invullen.

In plaats van de SMTP-serverdetails handmatig in te voeren, kunt u de functie **Office 365 Server-instellingen toepassen** gebruiken om ze in te voeren met informatie uit uw Office 365-abonnement.

U kunt uw e-mail handmatig instellen, zoals hieronder beschreven, of u kunt hulp krijgen door de begeleide instelling **Instelling van e-mail** te gebruiken. Zie voor meer informatie [Voorbereid zijn om zaken te doen](ui-get-ready-business.md).  

## <a name="to-set-up-email"></a>E-mail instellen
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **SMTP-e-mailinstellingen** in en kies de desbetreffende koppeling.
2. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Als u een account gebruikt waarvoor tweefactorauthenticatie is vereist, moet het wachtwoord dat u invoert in het veld **Wachtwoord**, hetzelfde zijn als het wachtwoord dat u gebruikt voor uw Office 365-abonnement en moet het van het type **App-wachtwoord** zijn. Zie voor meer informatie [App-wachtwoorden beheren voor tweestapsverificatie](/azure/active-directory/user-help/multi-factor-authentication-end-user-app-passwords).
3. Of u kiest de actie **Office 365 Server-instellingen toepassen** om alle informatie in te voegen die al voor uw Office 365-abonnement is gedefinieerd.
4. Als alle velden correct zijn ingevuld, kiest u de actie **Instelling e-mail testen**.
5. Als de test is geslaagd, sluit u de pagina.

## <a name="using-a-substitute-sender-address-on-outbound-email-messages"></a>Een vervangend afzenderadres gebruiken voor uitgaande e-mailberichten
Alle uitgaande e-mailberichten vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken het standaardadres voor het account dat u hebt opgegeven op de pagina SMTP-e-mailinstellingen, zoals hierboven beschreven. U kunt echter de mogelijkheden **Verzenden als** of **Verzenden namens** op uw Exchange-server gebruiken om het afzenderadres van uitgaande berichten te wijzigen. [!INCLUDE[d365fin](includes/d365fin_md.md)] zal het standaardaccount gebruiken om te verifiëren bij Exchange, maar zal het afzenderadres vervangen door het adres dat u opgeeft, of het wijzigen met 'namens'.

Hierna volgen voorbeelden van hoe Verzenden als en Verzenden namens worden gebruikt in [!INCLUDE[d365fin](includes/d365fin_md.md)].

 * Wanneer u documenten zoals inkoop- of verkooporders naar leveranciers en klanten verzendt, wilt u misschien dat ze afkomstig lijken te zijn van een _noreply@yourcompanyname.com_-adres.
 * Wanneer uw werkstroom een goedkeuringsverzoek per e-mail verzendt met behulp van het e-mailadres van de aanvrager.

> [!Note]
> U kunt slechts één account gebruiken om afzenderadressen te vervangen. Dat wil zeggen, u kunt niet één vervangend adres hebben voor inkoopprocessen en een ander voor verkoopprocessen.

### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>Een vervangend afzenderadres instellen voor alle uitgaande e-mailberichten
1. Zoek in het **Exchange-beheercentrum** voor uw Office 365-account de postbus die u als vervangend adres wilt gebruiken en kopieer of noteer het adres. Als u een nieuw adres nodig hebt, gaat u naar uw Microsoft 365-beheercentrum om een nieuwe gebruiker te maken en hun mailbox in te stellen.
2. Kies in [!INCLUDE[d365fin](includes/d365fin_md.md)] het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **SMTP-e-mailinstellingen** in en kies de desbetreffende koppeling.
3. Voer in het veld **Verzenden als** het vervangende adres in.
4. Kopieer of noteer het adres in het veld **Gebruikersnaam**.
5. Zoek in het **Exchange-beheercentrum** de postbus die u als vervangend adres wilt gebruiken en voer vervolgens het adres uit het veld **Gebruikersnaam** in het veld **Verzenden als** in. Zie voor [De EAC gebruiken om machtigingen toe te wijzen aan afzonderlijke mailboxen](/Exchange/recipients/mailbox-permissions?view=exchserver-2019#use-the-eac-to-assign-permissions-to-individual-mailboxes) voor meer informatie.

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>Het vervangende adres gebruiken in goedkeuringswerkstromen
1. Kies in [!INCLUDE[d365fin](includes/d365fin_md.md)] het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **SMTP-e-mailinstellingen** in en kies de desbetreffende koppeling.
2. Kopieer of noteer het adres in het veld **Gebruikersnaam**.
3. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikersinstellingen voor goedkeuring** in en kies de gerelateerde koppeling.
4. Zoek in het **Exchange-beheercentrum** de postvakken voor elke gebruiker die wordt vermeld op de pagina **Gebruikersinstellingen voor goedkeuring** en voer in het veld **Verzenden als** het adres uit het veld **Gebruikersnaam** van de pagina **SMTP-e-mailinstellingen** in [!INCLUDE[d365fin](includes/d365fin_md.md)] in. Zie [Machtigingen beheren voor ontvangers](/Exchange/recipients/mailbox-permissions?view=exchserver-2019) voor meer informatie.
5. Kies in [!INCLUDE[d365fin](includes/d365fin_md.md)] het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **SMTP-e-mailinstellingen** in en kies de desbetreffende koppeling.
6. Als u vervanging wilt inschakelen, zet u de schakelaar **Vervanging van afzender toestaan** aan.

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] bepaalt welk adres wordt weergegeven in de volgende volgorde: <br><br> 1. Het adres dat is opgegeven in het veld **E-mail** op de pagina **Gebruikersinstellingen voor goedkeuring** voor berichten in een werkstroom. <br> 2. Het adres dat is opgegeven in het veld **Verzenden als** op de pagina **SMTP-e-mailinstellingen**. <br> 3. Het adres dat is opgegeven in het veld **Gebruikersnaam** op de pagina **SMTP-e-mailinstellingen**.


## <a name="see-also"></a>Zie ook

[Gedeelde postbussen in Exchange Online](/exchange/collaboration-exo/shared-mailboxes)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken als uw bedrijfsinbox in Outlook](admin-outlook.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] installeren op mijn mobiele apparaat](install-mobile-app.md)
