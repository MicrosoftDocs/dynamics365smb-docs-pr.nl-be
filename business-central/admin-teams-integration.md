---
title: Microsoft Teams-integratie met Business Central beheren | Microsoft Docs
description: Business Central-integratie met Microsoft Teams beheren.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: 5fc5957695145ad3bbc4225c7c7e18dd7ca0c728
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5386311"
---
# <a name="managing-microsoft-teams-integration-with-prod_short"></a>Microsoft Teams-integratie met [!INCLUDE [prod_short](includes/prod_short.md)] beheren

[!INCLUDE [online_only](includes/online_only.md)]

Dit artikel geeft een overzicht van wat u als beheerder kunt doen om Microsoft Teams-integratie met [!INCLUDE [prod_short](includes/prod_short.md)] te beheren.

## <a name="in-microsoft-teams"></a>In Microsoft Teams

### <a name="minimum-requirements"></a>Minimumvereisten

In dit gedeelte worden de minimumvereisten voor de functies van de [!INCLUDE [prod_short](includes/prod_short.md)]-app beschreven om in Teams te werken.

- Vereiste licenties

    Deze tabel geeft u een overzicht van de licenties die nodig zijn voor de functies van de [!INCLUDE [prod_short](includes/prod_short.md)]-app om in Teams te werken.

    |Wat|Teams-licentie|[!INCLUDE [prod_short](includes/prod_short.md)]-licentie|
    |----|---|---|
    |Een link naar een [!INCLUDE [prod_short](includes/prod_short.md)]-record opnemen in een gesprek en het verzenden als een kaart.|![vinkje](media/check.png "vinkje")|![vinkje](media/check.png "vinkje")|
    |Een kaart van een [!INCLUDE [prod_short](includes/prod_short.md)]-record weergeven in een gesprek.|![vinkje](media/check.png "vinkje")||
    |Meer details van een kaart voor een [!INCLUDE [prod_short](includes/prod_short.md)]-record weergeven in een gesprek.|![vinkje](media/check.png "vinkje")|![vinkje](media/check.png "vinkje")|

- URL-voorbeelden toestaan

    Beleidsinstelling **URL-voorbeelden toestaan** moet zijn ingeschakeld. Anders kan er geen kaart worden gegenereerd voor [!INCLUDE [prod_short](includes/prod_short.md)]-koppelingen die in een Teams-gesprek worden geplakt. Zie voor meer informatie over deze instelling [Berichtenbeleid beheren in Teams](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-prod_short-app-optional"></a>De [!INCLUDE [prod_short](includes/prod_short.md)]-app beheren (optioneel)

Als Teams-beheerder kunt u alle apps voor uw organisatie beheren, inclusief de [!INCLUDE [prod_short](includes/prod_short.md)]-app. U kunt de [!INCLUDE [prod_short](includes/prod_short.md)]-app voor uw organisatie beheren, gebruikers blokkeren tegen het installeren van de app en meer.

Zie de volgende artikelen in de Microsoft Teams-documentatie voor meer informatie:

- [Uw apps beheren in het Microsoft Teams-beheercentrum](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [Installatiebeleid voor apps beheren in Microsoft Teams](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prod_short"></a>In [!INCLUDE [prod_short](includes/prod_short.md)]

### <a name="minimum-requirements"></a>Minimumvereisten

- [!INCLUDE [prod_short](includes/prod_short.md)]-versie:

    [!INCLUDE [prod_short](includes/prod_short.md)]-releasewave 2 van 2020, update 17.3 of hoger. Teams-integratie wordt alleen ondersteund voor [!INCLUDE [prod_short](includes/prod_short.md)] online; niet on-premises.

- Codeunit **2718 Page Summary Provider** wordt gepubliceerd als een webservice:

    Deze codeunit wordt standaard als webservice gepubliceerd. De codeunit is onderdeel van de [!INCLUDE [prod_short](includes/prod_short.md)]-systeemtoepassing. De codeunit wordt gebruikt om de veldgegevens op te halen voor een [!INCLUDE [prod_short](includes/prod_short.md)]-pagina die wordt toegevoegd aan een Teams-gesprek. Zie [Een webservice publiceren](across-how-publish-web-service.md) voor informatie over het publiceren van webservices.

- <a name="permissions"></a>Gebruikersmachtigingen:

    De pagina's en gegevens die gebruikers kunnen bekijken en bewerken in een Teams-gesprek worden voor het grootste deel bepaald door hun machtigingen in [!INCLUDE [prod_short](includes/prod_short.md)].
    
    - Om een [!INCLUDE [prod_short](includes/prod_short.md)]-koppeling te plakken in een Teams-gesprek en deze te laten uitbreiden naar een kaart, moeten gebruikers ten minste leesrechten hebben voor de pagina en de gegevens ervan.
    - Zodra een kaart in een gesprek is ingediend, kan elke gebruiker in dat gesprek die kaart bekijken zonder toestemming voor [!INCLUDE [prod_short](includes/prod_short.md)].
    - Om meer details van een kaart te zien of de record te openen in [!INCLUDE [prod_short](includes/prod_short.md)] moeten gebruikers leesbevoegdheid hebben voor de pagina en de gegevens ervan.
    - Om gegevens te wijzigen hebben gebruikers wijzigingsmachtiging nodig.
    
    Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie over machtigingen.

## <a name="managing-privacy-and-compliance"></a>Beheer van privacy en compliance 

Microsoft Teams biedt uitgebreide controles voor naleving en beheer van gevoelige of persoonlijk identificeerbare gegevens&mdash;inclusief gegevens die zijn toegevoegd aan chats en kanalen door de [!INCLUDE [prod_short](includes/prod_short.md)]-app.

### <a name="understanding-where-prod_short-cards-are-stored"></a>Begrijpen waar [!INCLUDE [prod_short](includes/prod_short.md)]-kaarten worden opgeslagen 

Nadat een kaart naar een chat is verzonden, worden de kaart en de velden op de kaart gekopieerd naar Teams. Deze informatie valt onder het Teams-beleid voor uw organisatie, zoals het beleid voor het bewaren van gegevens. Bij het weergeven van kaartdetails wordt geen van de gegevens in het detailvenster opgeslagen in Teams. De gegevens blijven opgeslagen in [!INCLUDE [prod_short](includes/prod_short.md)] en worden alleen opgehaald door Teams wanneer de gebruiker ervoor kiest om de details te bekijken. 

- Zie voor meer informatie over waar Teams die gegevens opslaat [Locatie van gegevens in Microsoft Teams](/microsoftteams/location-of-data-in-teams).
- Zie voor meer informatie over het bewaarbeleid in Teams [Bewaarbeleid in Microsoft Teams](/microsoftteams/retention-policies).

### <a name="restricting-sharing-of-cards"></a>Het delen van kaarten beperken 

U voorkomt dat specifieke gebruikers of groepen kaarten naar chats of kanalen sturen door berichtenbeleid in te stellen dat de instelling **URL-voorbeelden** uitschakelt. Zie voor meer informatie over deze instelling [Berichtenbeleid beheren in Teams](/microsoftteams/messaging-policies-in-teams). 

U kunt ook informatiebarrières gebruiken om te voorkomen dat personen of groepen met elkaar communiceren. Zie voor meer informatie [Informatiebarrières in Microsoft Teams](/microsoftteams/information-barriers-in-teams).

Functies voor het voorkomen van gegevensverlies in het Microsoft 365 Security & Compliance Center kunnen niet specifiek op kaarten worden toegepast. Maar ze kunnen worden toegepast op de chatberichten die de kaarten bevatten. Zie voor het volgen van toekomstige geavanceerde functies, waaronder het inschakelen van DLP voor kaarten [https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093](https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093).

### <a name="responding-to-data-requests"></a>Reageren op gegevensaanvragen

U staat teamleden en teameigenaren toe om berichten te verwijderen die gevoelige kaarten bevatten door een berichtenbeleid in te stellen, zoals: **Eigenaren kunnen verzonden berichten verwijderen** en **Gebruikers kunnen verzonden berichten verwijderen**. Zie voor meer informatie [Berichtenbeleid beheren in Teams](/microsoftteams/messaging-policies-in-teams).

Functies voor het zoeken van inhoud en eDiscovery-naleving in het Microsoft 365 Security & Compliance Center kunnen niet specifiek op kaarten worden toegepast. Maar ze kunnen worden toegepast op de chatberichten die kaarten bevatten. Zie voor het volgen van aankomende nalevingsfuncties voor kaarten [https://www.microsoft.com/microsoft-365/roadmap?featureid=68875](https://www.microsoft.com/microsoft-365/roadmap?featureid=68875).

Omdat kaartgegevens in Teams een kopie zijn van gegevens in [!INCLUDE [prod_short](includes/prod_short.md)], kunt u ook [!INCLUDE [prod_short](includes/prod_short.md)]-functies gebruiken om gegevens van een klant op verzoek te exporteren. Zie voor meer informatie over privacy in [!INCLUDE [prod_short](includes/prod_short.md)] [Veelgestelde vragen over privacy voor Business Central-klanten](/dynamics365/business-central/dev-itpro/security/privacyfaq).

## <a name="see-also"></a>Zie ook
Overzicht van integratie tussen [[!INCLUDE [prod_short](includes/prod_short.md)] en Microsoft Teams](across-teams-overview.md)  
[De [!INCLUDE [prod_short](includes/prod_short.md)]-app installeren voor Microsoft Teams](across-install-app-for-teams.md)  
[Veelgestelde vragen over Teams](teams-faq.md)  
[Problemen met Teams oplossen](admin-teams-troubleshooting.md)  
[Ontwikkeling voor Teams-integratie](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]