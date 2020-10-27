---
title: Werken met Business Central-gegevens in Microsoft Teams | Microsoft Docs
description: Lees hoe u de Business Central-app gebruikt voor Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: fbe024f724f018aae6d3aeb5251281bf4c3bfbde
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989447"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a>Werken met Business Central-gegevens in Microsoft Teams

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

[!INCLUDE [prodshort](includes/prodshort.md)] biedt een app die Microsoft Teams verbindt met uw bedrijfsgegevens in [!INCLUDE [prodshort](includes/prodshort.md)], zodat u snel details met teamleden kunt delen en sneller op vragen kunt reageren. In dit artikel leert u hoe u de app gebruikt om [!INCLUDE [prodshort](includes/prodshort.md)]-gegevens te delen met collega's in een Teams-gesprek.

## <a name="overview"></a>Overzicht

Met de [!INCLUDE [prodshort](includes/prodshort.md)]-app kunt u:

- Een koppeling kopiëren naar een Business Central-record en plakken in een Teams-gesprek om met uw collega's te delen. De koppeling wordt uitgebreid tot een compacte, interactieve kaart die informatie over de record weergeeft.
- Eenmaal in het gesprek kunnen u en collega's meer details over de record bekijken, gegevens bewerken en actie ondernemen zonder Teams te verlaten.

[![Teams-integratie met Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

## <a name="prerequisites"></a>Vereisten

- U hebt toegang tot Microsoft Teams.
- U hebt de [!INCLUDE [prodshort](includes/prodshort.md)]-app in Teams geïnstalleerd. Zie voor meer informatie [De [!INCLUDE [prodshort](includes/prodshort.md)]-app voor Microsoft Teams](across-install-app-for-teams.md) installeren

> [!NOTE]
> Alle deelnemers aan een Teams-gesprek kunnen kaarten bekijken voor Business Central-records die u indient bij het gesprek. Maar om meer details over records te bekijken door de knop **Details** of **Nieuw venster** op een kaart te gebruiken, hebben ze toegang nodig tot [!INCLUDE [prodshort](includes/prodshort.md)]. Zie voor meer informatie [Microsoft Teams-integratie beheren](admin-teams-integration.md#minimum-requirements-1).
<!--
- People You and your coworkers have the following permissions in [!INCLUDE [prodshort](includes/prodshort.md)]
  - To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, you have to have at least permission to view the page and its data.
  - Once a card is submitted into a conversation, any user in that conversation can view that card without having permission to Business Central.
  - For other users to view more details from card, they must also have view permission, as a minimum, to the page and its data. If they want to change data, they'll need modify permissions.

  Setting up permissions is typically done by an administrator. For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md).-->

## <a name="include-a-business-central-card-in-a-teams-conversation"></a>Een Business Central-kaart opnemen in een Teams-gesprek

1. Log in bij [!INCLUDE [prodshort](includes/prodshort.md)] met uw browser.
2. Open de record die u wilt delen.

    De app is ontworpen om pagina's van het kaarttype weer te geven vanuit [!INCLUDE [prodshort](includes/prodshort.md)]. Open dus een pagina met één record, zoals een artikel, klant of verkooporder. U kunt de app niet gebruiken voor rolcentra of pagina's die meerdere records in een lijst weergeven.

3. Kopieer de volledige URL uit de adresbalk van de browser.

   ![Kopieer de Business Central-URL vanuit de browser](media/teams-url.png)
4. Ga naar Teams en start een gesprek. Dat kan chatten met een persoon, een groep personen of een teamkanaal zijn.

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Plak de URL in het vak waarin u een bericht toevoegt.

   ![Plak de Business Central-URL in Teams](media/teams-paste-url.png)
6. De eerste keer dat u een koppeling in een gesprek plakt, wordt u gevraagd u aan te melden bij [!INCLUDE [prodshort](includes/prodshort.md)] en toestemming te geven aan de app om gegevens op te halen. Volg gewoon de instructies op het scherm.

    > [!NOTE]
    > U hoeft deze stap maar één keer uit te voeren.

7. Wacht even terwijl er een kaart wordt gegenereerd in het berichtvenster.

8. Als de kaart verschijnt, controleert u de inhoud van de kaart zorgvuldig op gevoelige informatie voordat u het bericht verzendt. Deze stap is belangrijk omdat zodra u het bericht verzendt, iedereen in het gesprek de kaart kan zien.

9. Selecteer als de kaart er goed uitziet **Verzenden** om de kaart bij het gesprek in te dienen.

    > [!TIP]
    > Nadat de kaart is verschenen en voordat u **Verzenden** selecteert, kunt u de geplakte URL desgewenst verwijderen.

10. Selecteer om meer details te bekijken of wijzigingen aan te brengen in de record **Details** .

    De detailpagina is vergelijkbaar met wat u zou zien in [!INCLUDE [prodshort](includes/prodshort.md)]. Maar het is enigszins ingekort voor Teams. Als u klaar bent met het bekijken en aanbrengen van wijzigingen, sluit u het venster om terug te keren naar het Teams-gesprek.

    > [!NOTE]
    > Alle wijzigingen die u aanbrengt, worden pas op de kaart weergegeven als u de koppeling de volgende keer in een gesprek plakt.

## <a name="see-also"></a>Zie ook

[Integratieoverzicht van Business Central en Microsoft Teams](across-teams-overview.md)  
[De [!INCLUDE [prodshort](includes/prodshort.md)]-app installeren voor Microsoft Teams](across-install-app-for-teams.md)  
[Ontwikkeling voor Teams-integratie](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[Aan de slag](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
