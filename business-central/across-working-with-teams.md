---
title: Business Central-records delen in Microsoft Teams
description: Lees hoe u de Business Central-app gebruikt voor Microsoft Teams.
author: jswymer
ms.topic: how-to
ms.service: dynamics365-business-central
ms.reviewer: jswymer
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records'
ms.date: 12/12/2023
ms.author: jswymer
ms.custom: bap-template
---

# Business Central-records en paginakoppelingen delen in Microsoft Teams

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

## Een Business Central-kaart opnemen en weergeven in een Teams-gesprek

Met de Business Central-app voor Teams kunt u een koppeling kopiëren vanuit elke Business Central-record, zoals een klant of verkooporder, en de koppeling in een Teams-gesprek plakken. De app maakt verbindt Microsoft Teams met uw bedrijfsgegevens in [!INCLUDE [prod_short](includes/prod_short.md)]\. De koppeling wordt vervolgens uitgebreid tot een compacte, interactieve kaart die informatie over de record weergeeft. Eenmaal in het gesprek kunnen u en collega's meer details over de record bekijken, gegevens bewerken en actie ondernemen&mdash;zonder Teams te verlaten.

[![Teams-integratie met Business Central.](media/teams-intro-vBC20.png)](media/teams-intro-vBC20.png#lightbox)

### Vereisten

- U hebt toegang tot Microsoft Teams.
- U hebt de [!INCLUDE [prod_short](includes/prod_short.md)]-app in Teams geïnstalleerd. Zie voor meer informatie [De [!INCLUDE [prod_short](includes/prod_short.md)]-app voor Microsoft Teams](across-install-app-for-teams.md) installeren

> [!NOTE]
> Alle deelnemers aan een Teams-gesprek kunnen kaarten bekijken voor Business Central-records die u indient bij het gesprek. Maar om meer details over records te bekijken door de knop **Details** of **Nieuw venster** op een kaart te gebruiken, hebben ze toegang nodig tot [!INCLUDE [prod_short](includes/prod_short.md)]. Zie voor meer informatie [Microsoft Teams-integratie beheren](admin-teams-integration.md#minimum-requirements-1).

### Een Business Central-kaart opnemen in een Teams-gesprek

1. Log in bij [!INCLUDE [prod_short](includes/prod_short.md)] met uw browser.
2. Open de record die u wilt delen.

    De app is ontworpen om een kaart weer te geven voor vrijwel elk type [!INCLUDE [prod_short](includes/prod_short.md)]-pagina. Maar de app biedt de beste ervaring wanneer deze wordt gebruikt voor pagina's die een enkele record weergeven, zoals een artikel, klant of verkooporder.
3. Kopieer de koppeling naar de pagina.

    Er zijn twee manieren om de koppeling te kopiëren. De gemakkelijkste en geprefereerde manier is via het selecteren van **Delen** ![Pictogram Delen in Business Central](media/share-icon.png) > **Koppeling kopiëren**. De andere manier is door de volledige URL vanuit de adresbalk van de browser te kopiëren.

    [![De Business Central-URL kopiëren vanuit de browser.](media/teams-copy-link.png)](media/teams-copy-link.png#lightbox)
4. Ga naar Teams en start een gesprek. Dat kan chatten met een persoon, een groep personen of een teamkanaal zijn.
5. Plak de koppeling (URL) in het berichtvak waarin u een bericht opstelt.

    ![Plak de Business Central-URL in Teams.](media/teams-paste-url-v2.png)

    > [!TIP]
    > Als u een bericht krijgt als *Business Central wil een voorbeeld van deze koppeling laten zien.*, betekent dit dat u de Business Central-app voor Teams niet hebt geïnstalleerd. Als u de app wilt installeren, selecteert u **Voorbeeld weergeven** en volgt u de instructies.

    > [!NOTE]
    > Afhankelijk van uw Business Central-versie kan u, de eerste keer dat u een koppeling in een gesprek plakt, worden gevraagd u aan te melden bij [!INCLUDE [prod_short](includes/prod_short.md)] en toestemming te geven aan de app om gegevens op te halen. Volg gewoon de instructies op het scherm. U hoeft deze stap maar één keer uit te voeren.
6. Wacht even terwijl er een kaart wordt gegenereerd in het berichtvenster.
7. Als de kaart verschijnt, controleert u de inhoud van de kaart zorgvuldig op gevoelige informatie voordat u het bericht verzendt. Deze stap is belangrijk omdat zodra u het bericht verzendt, iedereen in het gesprek de kaart kan zien.
8. Selecteer als de kaart er goed uitziet **Verzenden** om de kaart bij het gesprek in te dienen.

    > [!TIP]
    > Nadat de kaart is verschenen en voordat u **Verzenden** selecteert, kunt u de geplakte URL desgewenst verwijderen.
9. Selecteer om meer details te bekijken of wijzigingen aan te brengen in de record die op de kaart wordt weergegeven, **Details**. Zie de volgende sectie voor meer informatie.

### Kaartdetails weergeven

Zodra een kaart naar een gesprek is verzonden, kunnen alle deelnemers met de [juiste machtigingen](admin-teams-integration.md#permissions) **Details** selecteren om een venster te openen met meer informatie over de record&mdash;en eventueel wijzigingen aanbrengen in het record. Het maakt niet uit of u degene bent die de kaart verstuurt of degene die de kaart ontvangt. De functie **Details** is vooral handig voor ontvangers, omdat deze hen snel beknopte, gerichte informatie over de record biedt.

Het detailvenster is vergelijkbaar met wat u zou zien in [!INCLUDE [prod_short](includes/prod_short.md)], maar het is gericht op de pagina of record waar de kaart over gaat. Als u klaar bent met het bekijken en aanbrengen van wijzigingen, sluit u het venster om terug te keren naar het Teams-gesprek.

Hier zijn een paar dingen waarmee u rekening moet houden wanneer u met de kaartgegevens werkt:

- Om de kaartdetails te openen moeten gebruikers de machtiging op de pagina en de gegevens ervan hebben in [!INCLUDE [prod_short](includes/prod_short.md)]\..
- Kaarten in Teams-chats worden niet automatisch bijgewerkt met wijzigingen. Alle wijzigingen die u opslaat in een record in het detailvenster, worden opgeslagen in [!INCLUDE [prod_short](includes/prod_short.md)]\.. Maar de kaart in Teams geeft de wijzigingen in de conversie pas weer als u de koppeling opnieuw plakt.

Zie voor meer informatie over het werken met kaarten en kaartdetails [Veelgestelde vragen over Teams](teams-faq.md).

## <a name="share-link"></a>Een koppeling naar een pagina vanuit Business Central delen met Teams

Rechtstreeks vanuit de meeste collectiepagina's, zoals de pagina **Artikelen** en detailpagina's, zoals de kaart **Artikel** kunt u een link naar de pagina naar specifieke ontvangers sturen in een Teams-gesprek. U kunt bijvoorbeeld een koppeling naar een gefilterde weergave van uw records delen. Ontvangers kunnen vervolgens de link selecteren om de pagina te openen in [!INCLUDE [prod_short](includes/prod_short.md)]\.

[![Het menu Delen weergegeven op een kaart.](media/teams-share-link-v2.png "Het menu Delen weergegeven op een kaart.")](media/teams-share-link-v2.png#lightbox)

### Vereisten

- U hebt toegang tot Microsoft Teams.
- (Optioneel) U hebt de [!INCLUDE [prod_short](includes/prod_short.md)]-app in Teams geïnstalleerd. 

  Als de app is geïnstalleerd, bevatten berichten die u met de koppeling verzendt ook een compacte kaart voor de pagina. Zie voor meer informatie over het installeren van de app [De [!INCLUDE [prod_short](includes/prod_short.md)]-app voor Microsoft Teams](across-install-app-for-teams.md) installeren.

### Een koppeling delen

1. Open in [!INCLUDE [prod_short](includes/prod_short.md)]\, de pagina die u wilt delen.
2. Kies boven aan de pagina het pictogram ![!Actie Delen met andere apps op pagina's.](media/share-icon.png) en vervolgens **Delen met teams**.
3. Log desgevraagd in bij Teams met uw gebruikersnaam en wachtwoord.
4. Typ op de pagina **Delen met teams** een naam van een persoon, groep of kanaal waarnaar u het bericht wilt verzenden.
5. Het berichtvenster bevat een link naar de pagina. Als de [!INCLUDE [prod_short](includes/prod_short.md)]-app voor Teams is geïnstalleerd, verschijnt er ook een kaart voor het gekoppelde record of de gekoppelde pagina in het berichtvenster.

   Voeg eventueel meer informatie toe en kies dan **Delen**.
6. De link is nu gedeeld. Als u naar het gesprek wilt gaan, kiest u **Ga naar Teams**.

## Zie ook

[Integratieoverzicht van Business Central en Microsoft Teams](across-teams-overview.md)  
[De [!INCLUDE [prod_short](includes/prod_short.md)]-app installeren voor Microsoft Teams](across-install-app-for-teams.md)  
[Veelgestelde vragen over Teams](teams-faq.md)  
[Zoeken naar klanten, leveranciers en andere contacten vanuit Microsoft Teams](across-search-contacts-teams.md)  
[Bedrijfs- en andere instellingen in Teams wijzigen](across-teams-settings.md)  
[Problemen met Teams oplossen](admin-teams-troubleshooting.md)  
[Ontwikkeling voor Teams-integratie](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
