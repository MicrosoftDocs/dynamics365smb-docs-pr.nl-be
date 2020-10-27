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
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: 3c04dfb2f77eba906b2567ca9438849e1cc20861
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989371"
---
# <a name="managing-microsoft-teams-integration-with-business-central"></a>Microsoft Teams-integratie met Business Central beheren

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

Dit artikel geeft een overzicht van wat u als beheerder kunt doen om Microsoft Teams-integratie met [!INCLUDE [prodshort](includes/prodshort.md)] te beheren.

## <a name="in-microsoft-teams"></a>In Microsoft Teams

### <a name="minimum-requirements"></a>Minimumvereisten

In dit gedeelte worden de minimumvereisten voor de functies van de [!INCLUDE [prodshort](includes/prodshort.md)]-app beschreven om in Teams te werken.

- Vereiste licenties

    Deze tabel geeft u een overzicht van de licenties die nodig zijn voor de functies van de [!INCLUDE [prodshort](includes/prodshort.md)]-app om in Teams te werken.

    |Wat|Teams-licentie|Business Central-licentie|
    |----|---|---|
    |Een link naar een [!INCLUDE [prodshort](includes/prodshort.md)]-record opnemen in een gesprek en het verzenden als een kaart.|![vinkje](media/check.png "vinkje")|![vinkje](media/check.png "vinkje")|
    |Een kaart van een [!INCLUDE [prodshort](includes/prodshort.md)]-record weergeven in een gesprek.|![vinkje](media/check.png "vinkje")||
    |Meer details van een kaart voor een [!INCLUDE [prodshort](includes/prodshort.md)]-record weergeven in een gesprek.|![vinkje](media/check.png "vinkje")|![vinkje](media/check.png "vinkje")|

- URL-voorbeelden toestaan

    Beleidsinstelling **URL-voorbeelden toestaan** moet zijn ingeschakeld. Anders kan er geen kaart worden gegenereerd voor Business Central-koppelingen die in een Teams-gesprek worden geplakt. Zie voor meer informatie over deze instelling [Berichtenbeleid beheren in Teams](/microsoftteams/messaging-policies-in-teams).

### <a name="managing-the-business-central-app-optional"></a>De Business Central-app beheren (optioneel)

Als Teams-beheerder kunt u alle apps voor uw organisatie beheren, inclusief de [!INCLUDE [prodshort](includes/prodshort.md)]-app. U kunt de [!INCLUDE [prodshort](includes/prodshort.md)]-app voor uw organisatie beheren, gebruikers blokkeren tegen het installeren van de app en meer.

Zie de volgende artikelen in de Microsoft Teams-documentatie voor meer informatie:

- [Uw apps beheren in het Microsoft Teams-beheercentrum](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [Installatiebeleid voor apps beheren in Microsoft Teams](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prodshort"></a>In [!INCLUDE [prodshort](includes/prodshort.md)]

### <a name="minimum-requirements"></a>Minimumvereisten

- [!INCLUDE [prodshort](includes/prodshort.md)]-versie:

    [!INCLUDE [prodshort](includes/prodshort.md)]-releasewave 2 van 2020 (versie 17) of hoger. Teams-integratie wordt alleen ondersteund voor [!INCLUDE [prodshort](includes/prodshort.md)] online; niet on-premises.

- Codeunit **2718 Page Summary Provider** wordt gepubliceerd als een webservice:

    Deze codeunit wordt standaard als webservice gepubliceerd. De codeunit is onderdeel van de [!INCLUDE [prodshort](includes/prodshort.md)]-systeemtoepassing. De codeunit wordt gebruikt om de veldgegevens op te halen voor een [!INCLUDE [prodshort](includes/prodshort.md)]-pagina die wordt toegevoegd aan een Teams-gesprek. 

- Gebruikersmachtigingen:

    De pagina's en gegevens die gebruikers kunnen bekijken en bewerken in een Teams-gesprek worden voor het grootste deel bepaald door hun machtigingen in [!INCLUDE [prodshort](includes/prodshort.md)].
    
    - Om een [!INCLUDE [prodshort](includes/prodshort.md)]-koppeling te plakken in een Teams-gesprek en deze te laten uitbreiden naar een kaart, moeten gebruikers ten minste leesrechten hebben voor de pagina en de gegevens ervan.
    - Zodra een kaart in een gesprek is ingediend, kan elke gebruiker in dat gesprek die kaart bekijken zonder toestemming voor Business Central.
    - Om meer details van een kaart te zien of de record te openen in [!INCLUDE [prodshort](includes/prodshort.md)] moeten gebruikers leesbevoegdheid hebben voor de pagina en de gegevens ervan.
    - Om gegevens te wijzigen hebben gebruikers wijzigingsmachtiging nodig.
    
    Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie over machtigingen.

## <a name="see-also"></a>Zie ook
[Integratieoverzicht van Business Central en Microsoft Teams](across-teams-overview.md)  
[De [!INCLUDE [prodshort](includes/prodshort.md)]-app installeren voor Microsoft Teams](across-install-app-for-teams.md)  
[Ontwikkeling voor Teams-integratie](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[Aan de slag](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
