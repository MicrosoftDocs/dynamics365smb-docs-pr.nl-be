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
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: e20208d50eb65f1a92e6661396bf53007ab88eb8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786894"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a>Werken met Business Central-gegevens in Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

[!INCLUDE [prod_short](includes/prod_short.md)] biedt een app die Microsoft Teams verbindt met uw bedrijfsgegevens in [!INCLUDE [prod_short](includes/prod_short.md)], zodat u snel details met teamleden kunt delen en sneller op vragen kunt reageren. In dit artikel leert u hoe u de app gebruikt om [!INCLUDE [prod_short](includes/prod_short.md)]-gegevens te delen met collega's in een Teams-gesprek.

## <a name="overview"></a>Overzicht

Met de [!INCLUDE [prod_short](includes/prod_short.md)]-app kunt u:

- Een koppeling naar een Business Central-record kopiëren en plakken in een Teams-gesprek om met uw collega's te delen. De app breidt de koppeling dan uit tot een compacte, interactieve kaart die informatie over de record weergeeft.
- Eenmaal in het gesprek kunnen u en collega's meer details over de record bekijken, gegevens bewerken en actie ondernemen&mdash;zonder Teams te verlaten.

[![Teams-integratie met Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

## <a name="prerequisites"></a>Vereisten

- U hebt toegang tot Microsoft Teams.
- U hebt de [!INCLUDE [prod_short](includes/prod_short.md)]-app in Teams geïnstalleerd. Zie voor meer informatie [De [!INCLUDE [prod_short](includes/prod_short.md)]-app voor Microsoft Teams](across-install-app-for-teams.md) installeren

> [!NOTE]
> Alle deelnemers aan een Teams-gesprek kunnen kaarten bekijken voor Business Central-records die u indient bij het gesprek. Maar om meer details over records te bekijken door de knop **Details** of **Nieuw venster** op een kaart te gebruiken, hebben ze toegang nodig tot [!INCLUDE [prod_short](includes/prod_short.md)]. Zie voor meer informatie [Microsoft Teams-integratie beheren](admin-teams-integration.md#minimum-requirements-1).

## <a name="include-a-business-central-card-in-a-teams-conversation"></a>Een Business Central-kaart opnemen in een Teams-gesprek

1. Log in bij [!INCLUDE [prod_short](includes/prod_short.md)] met uw browser.
2. Open de record die u wilt delen.

    De app is ontworpen om pagina's van het kaarttype weer te geven vanuit [!INCLUDE [prod_short](includes/prod_short.md)]. Open dus een pagina met één record, zoals een artikel, klant of verkooporder. U kunt de app niet gebruiken voor rolcentra of pagina's die meerdere records in een lijst weergeven.

3. Kopieer de volledige URL uit de adresbalk van de browser.

   ![Kopieer de Business Central-URL vanuit de browser](media/teams-url-v2.png)
4. Ga naar Teams en start een gesprek. Dat kan chatten met een persoon, een groep personen of een teamkanaal zijn.

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Plak de URL in het berichtvak waarin u een bericht opstelt.

   ![Plak de Business Central-URL in Teams](media/teams-paste-url-v2.png)
6. De eerste keer dat u een koppeling in een gesprek plakt, wordt u gevraagd u aan te melden bij [!INCLUDE [prod_short](includes/prod_short.md)] en toestemming te geven aan de app om gegevens op te halen. Volg gewoon de instructies op het scherm.

    > [!NOTE]
    > U hoeft deze stap maar één keer uit te voeren.

7. Wacht even terwijl er een kaart wordt gegenereerd in het berichtvenster.

8. Als de kaart verschijnt, controleert u de inhoud van de kaart zorgvuldig op gevoelige informatie voordat u het bericht verzendt. Deze stap is belangrijk omdat zodra u het bericht verzendt, iedereen in het gesprek de kaart kan zien.

9. Selecteer als de kaart er goed uitziet **Verzenden** om de kaart bij het gesprek in te dienen.

    > [!TIP]
    > Nadat de kaart is verschenen en voordat u **Verzenden** selecteert, kunt u de geplakte URL desgewenst verwijderen.

10. Selecteer om meer details te bekijken of wijzigingen aan te brengen in de record die op de kaart wordt weergegeven, **Details**. Zie de volgende sectie voor meer informatie.

## <a name="view-card-details"></a>Kaartdetails weergeven

Zodra een kaart naar een gesprek is verzonden, kunnen alle deelnemers met de [juiste machtigingen](admin-teams-integration.md#permissions) **Details** selecteren om een venster te openen met meer informatie over de record&mdash;en eventueel wijzigingen aanbrengen in het record. Het maakt niet uit of u degene bent die de kaart verstuurt of degene die de kaart ontvangt. De functie **Details** is vooral handig voor ontvangers, omdat deze hen snel beknopte, gerichte informatie over de record biedt, in plaats van de volledige record te moeten scannen.

Het detailvenster is vergelijkbaar met wat u zou zien in [!INCLUDE [prod_short](includes/prod_short.md)]. Maar het is enigszins ingekort voor Teams. Als u klaar bent met het bekijken en aanbrengen van wijzigingen, sluit u het venster om terug te keren naar het Teams-gesprek.

Hier zijn een paar dingen waarmee u rekening moet houden wanneer u met de kaartgegevens werkt:

- Om de kaartdetails te openen moeten gebruikers de machtiging op de pagina en de gegevens ervan hebben in [!INCLUDE [prod_short](includes/prod_short.md)].
- Kaarten in Teams-chats worden niet automatisch bijgewerkt met wijzigingen. Alle wijzigingen die u opslaat in een record in het detailvenster, worden opgeslagen in [!INCLUDE [prod_short](includes/prod_short.md)]. Maar de kaart in Teams geeft de wijzigingen in de conversie pas weer als u de koppeling opnieuw plakt.

Zie voor meer informatie over het werken met kaarten en kaartdetails [Veelgestelde vragen over Teams](teams-faq.md).

## <a name="see-also"></a>Zie ook

[Integratieoverzicht van Business Central en Microsoft Teams](across-teams-overview.md)  
[De [!INCLUDE [prod_short](includes/prod_short.md)]-app installeren voor Microsoft Teams](across-install-app-for-teams.md)  
[Veelgestelde vragen over Teams](teams-faq.md)  
[Problemen met Teams oplossen](admin-teams-troubleshooting.md)  
[Ontwikkeling voor Teams-integratie](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]