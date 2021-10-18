---
title: Business Central-records delen in Microsoft Teams
description: Lees hoe u de Business Central-app gebruikt voor Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records
ms.date: 05/19/2021
ms.author: jswymer
ms.openlocfilehash: 3ad8b25fef8b486d4b2064e8c5117f0b25c6ec5b
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2021
ms.locfileid: "7587846"
---
# <a name="sharing-business-central-records-and-page-links-in-microsoft-teams"></a>Business Central-records en paginakoppelingen delen in Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

[!INCLUDE [prod_short](includes/prod_short.md)] biedt een aantal manieren om gegevens uit Business Central rechtstreeks te delen in een Microsoft Teams-gesprek:

<!-- 
## Overview
In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.
The [!INCLUDE [prod_short](includes/prod_short.md)] app lets you:
[!INCLUDE [prod_short](includes/prod_short.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)], so you can quickly share details across team members and respond faster to inquiries. In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.

-->
- Met de [!INCLUDE [prod_short](includes/prod_short.md)]-app geïnstalleerd in Teams kunt u een interactieve kaart van een Business Central-record opnemen in een Teams-gesprek.

<!--   Copy a link from any Business Central record, like a customer or sales order, then paste the link into a Teams conversation. The app connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)]. It then expands the link into a compact, interactive card that displays information about the record. Once in the conversation, you and coworkers can view more details about the record, edit data, and take action&mdash;without leaving Teams.

  [![Teams integration with Business Central.](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)-->

- Met of zonder de [!INCLUDE [prod_short](includes/prod_short.md)]-app geïnstalleerd kunt u een koppeling vanuit pagina's in Business Central naar een Teams-gesprek delen.

  <!-- ![!The Share menu displayed on a card.](media/teams-share-link.png "The Share menu displayed on a card.")-->

In de volgende secties worden de verschillende manieren gedetailleerd beschreven.

## <a name="include-and-view-a-business-central-card-in-a-teams-conversation"></a>Een Business Central-kaart opnemen en weergeven in een Teams-gesprek

Met de Business Central-app voor Teams kunt u een koppeling kopiëren vanuit elke Business Central-record, zoals een klant of verkooporder, en de koppeling in een Teams-gesprek plakken. De app maakt verbindt Microsoft Teams met uw bedrijfsgegevens in [!INCLUDE [prod_short](includes/prod_short.md)]\. De koppeling wordt vervolgens uitgebreid tot een compacte, interactieve kaart die informatie over de record weergeeft. Eenmaal in het gesprek kunnen u en collega's meer details over de record bekijken, gegevens bewerken en actie ondernemen&mdash;zonder Teams te verlaten.

[![Teams-integratie met Business Central.](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

### <a name="prerequisites"></a>Vereisten

- U hebt toegang tot Microsoft Teams.
- U hebt de [!INCLUDE [prod_short](includes/prod_short.md)]-app in Teams geïnstalleerd. Zie voor meer informatie [De [!INCLUDE [prod_short](includes/prod_short.md)]-app voor Microsoft Teams](across-install-app-for-teams.md) installeren

> [!NOTE]
> Alle deelnemers aan een Teams-gesprek kunnen kaarten bekijken voor Business Central-records die u indient bij het gesprek. Maar om meer details over records te bekijken door de knop **Details** of **Nieuw venster** op een kaart te gebruiken, hebben ze toegang nodig tot [!INCLUDE [prod_short](includes/prod_short.md)]. Zie voor meer informatie [Microsoft Teams-integratie beheren](admin-teams-integration.md#minimum-requirements-1).

### <a name="include-a-business-central-card-in-a-teams-conversation"></a>Een Business Central-kaart opnemen in een Teams-gesprek

1. Log in bij [!INCLUDE [prod_short](includes/prod_short.md)] met uw browser.
2. Open de record die u wilt delen.

    De app is ontworpen om pagina's van het kaarttype weer te geven vanuit [!INCLUDE [prod_short](includes/prod_short.md)]\.. Open dus een pagina met één record, zoals een artikel, klant of verkooporder. U kunt de app niet gebruiken voor rolcentra of pagina's die meerdere records in een lijst weergeven.

3. Kopieer de volledige URL uit de adresbalk van de browser.

   ![De Business Central-URL kopiëren vanuit de browser.](media/teams-url-v2.png)
4. Ga naar Teams en start een gesprek. Dat kan chatten met een persoon, een groep personen of een teamkanaal zijn.

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Plak de URL in het berichtvak waarin u een bericht opstelt.

   ![Plak de Business Central-URL in Teams.](media/teams-paste-url-v2.png)
6. De eerste keer dat u een koppeling in een gesprek plakt, wordt u gevraagd u aan te melden bij [!INCLUDE [prod_short](includes/prod_short.md)] en toestemming te geven aan de app om gegevens op te halen. Volg gewoon de instructies op het scherm.

    > [!NOTE]
    > U hoeft deze stap maar één keer uit te voeren.

7. Wacht even terwijl er een kaart wordt gegenereerd in het berichtvenster.

8. Als de kaart verschijnt, controleert u de inhoud van de kaart zorgvuldig op gevoelige informatie voordat u het bericht verzendt. Deze stap is belangrijk omdat zodra u het bericht verzendt, iedereen in het gesprek de kaart kan zien.

9. Selecteer als de kaart er goed uitziet **Verzenden** om de kaart bij het gesprek in te dienen.

    > [!TIP]
    > Nadat de kaart is verschenen en voordat u **Verzenden** selecteert, kunt u de geplakte URL desgewenst verwijderen.

10. Selecteer om meer details te bekijken of wijzigingen aan te brengen in de record die op de kaart wordt weergegeven, **Details**. Zie de volgende sectie voor meer informatie.

### <a name="view-card-details"></a>Kaartdetails weergeven

Zodra een kaart naar een gesprek is verzonden, kunnen alle deelnemers met de [juiste machtigingen](admin-teams-integration.md#permissions) **Details** selecteren om een venster te openen met meer informatie over de record&mdash;en eventueel wijzigingen aanbrengen in het record. Het maakt niet uit of u degene bent die de kaart verstuurt of degene die de kaart ontvangt. De functie **Details** is vooral handig voor ontvangers, omdat deze hen snel beknopte, gerichte informatie over de record biedt, in plaats van de volledige record te moeten scannen.

Het detailvenster is vergelijkbaar met wat u zou zien in [!INCLUDE [prod_short](includes/prod_short.md)]. Maar het is enigszins ingekort voor Teams. Als u klaar bent met het bekijken en aanbrengen van wijzigingen, sluit u het venster om terug te keren naar het Teams-gesprek.

Hier zijn een paar dingen waarmee u rekening moet houden wanneer u met de kaartgegevens werkt:

- Om de kaartdetails te openen moeten gebruikers de machtiging op de pagina en de gegevens ervan hebben in [!INCLUDE [prod_short](includes/prod_short.md)]\..
- Kaarten in Teams-chats worden niet automatisch bijgewerkt met wijzigingen. Alle wijzigingen die u opslaat in een record in het detailvenster, worden opgeslagen in [!INCLUDE [prod_short](includes/prod_short.md)]\.. Maar de kaart in Teams geeft de wijzigingen in de conversie pas weer als u de koppeling opnieuw plakt.

Zie voor meer informatie over het werken met kaarten en kaartdetails [Veelgestelde vragen over Teams](teams-faq.md).

## <a name="share-a-link-to-page-from-business-central-to-teams"></a><a name="share-link"></a>Een koppeling naar een pagina vanuit Business Central delen met Teams

Rechtstreeks vanuit de meeste collectiepagina's, zoals de pagina **Artikelen** en detailpagina's, zoals de **Artikel** kaart kunt u een link naar de pagina naar specifieke ontvangers sturen in een Teams-gesprek. U kunt bijvoorbeeld een koppeling naar een gefilterde weergave van uw records delen. Ontvangers kunnen vervolgens de link selecteren om de pagina te openen in [!INCLUDE [prod_short](includes/prod_short.md)]\.

 ![!Het menu Delen weergegeven op een kaart.](media/teams-share-link.png "Het menu Delen weergegeven op een kaart.")

### <a name="prerequisites"></a>Vereisten
U hebt toegang tot Microsoft Teams.

### <a name="share-a-link"></a>Een koppeling delen

1. Open in [!INCLUDE [prod_short](includes/prod_short.md)]\, de pagina die u wilt delen.
2. Kies boven aan de pagina het pictogram ![!Actie Delen met andere apps op pagina's.](media/share-icon.png) en vervolgens **Delen met teams**.
3. Log desgevraagd in bij Teams met uw gebruikersnaam en wachtwoord.
4. Typ op de pagina **Delen met teams** een naam van een persoon, groep of kanaal waarnaar u het bericht wilt verzenden. 
5. Het berichtvenster bevat een link naar de pagina. Voeg eventueel meer informatie toe en kies dan **Delen**.
6. De link is nu gedeeld. Als u naar het gesprek wilt gaan, kiest u **Ga naar Teams**.

## <a name="see-also"></a>Zie ook

[Integratieoverzicht van Business Central en Microsoft Teams](across-teams-overview.md)  
[De [!INCLUDE [prod_short](includes/prod_short.md)]-app installeren voor Microsoft Teams](across-install-app-for-teams.md)  
[Veelgestelde vragen over Teams](teams-faq.md)  
[Zoeken naar klanten, leveranciers en andere contacten vanuit Microsoft Teams](across-search-contacts-teams.md)  
[Bedrijfs- en andere instellingen in Teams wijzigen](across-teams-settings.md)  
[Problemen met Teams oplossen](admin-teams-troubleshooting.md)  
[Ontwikkeling voor Teams-integratie](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]