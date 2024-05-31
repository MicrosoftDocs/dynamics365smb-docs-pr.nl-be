---
title: Business Central-tabblad toevoegen in Microsoft Teams
description: Ontdek hoe u tabbladen kunt toevoegen in Teams waarop Business Central-pagina's worden weergeven.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 12/12/2023
ms.custom: bap-template
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records, tab'
---

# Business Central-tabblad toevoegen in Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

In Teams verschijnen tabbladen bovenaan kanalen en chats, waardoor deelnemers snel toegang hebben tot relevante informatie. In dit artikel worden verschillende manieren uitgelegd om een tabblad toe te voegen waarop [!INCLUDE [prod_short](includes/prod_short.md)]-gegevens worden weergegeven.

![Tabbladen in Teams](media/teams-tabs-border.png)

## Over Business Central-tabbladen

Een [!INCLUDE [prod_short](includes/prod_short.md)]-tabblad biedt een gerichte weergave van [!INCLUDE [prod_short](includes/prod_short.md)]-lijst- en kaartpagina's. Het tabblad toont niet de volledige [!INCLUDE [prod_short](includes/prod_short.md)]-webclient. Er is geen browserrand, [!INCLUDE [prod_short](includes/prod_short.md)]-banner (bijvoorbeeld met Vertel me, zoeken, help) of navigatiemenu aan de bovenkant&mdash;alleen pagina-inhoud en bijbehorende acties. De inhoud is interactief, wat betekent dat u acties en koppelingen kunt selecteren, gegevens kunt wijzigen en meer. U wordt beperkt in wat u ziet en kunt doen door dezelfde machtigingen die zijn toegewezen aan uw account in [!INCLUDE [prod_short](includes/prod_short.md)].

Voor meer informatie over wie de inhoud kan bekijken in een [!INCLUDE [prod_short](includes/prod_short.md)]-tabblad, zie [Wie kan de inhoud van een tabblad zien?](/dynamics365/business-central/teams-faq?tabs=tabs#who-can-view).

> [!TIP]
> Bent u een ontwikkelaar? U kunt ook programmatisch tabbladen toevoegen met behulp van de Microsoft Graph API. Zie [Business Central-tabbladen configureren](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams-tabs) voor meer informatie.  

## Vereisten

Om een [!INCLUDE [prod_short](includes/prod_short.md)]-tabblad toe te voegen, moet aan de volgende vereisten zijn voldaan:

- U hebt toegang tot Microsoft Teams.
- U hebt een [!INCLUDE [prod_short](includes/prod_short.md)]-licentie.
- U hebt de [!INCLUDE [prod_short](includes/prod_short.md)]-app in Teams geïnstalleerd. Zie voor meer informatie [De [!INCLUDE [prod_short](includes/prod_short.md)]-app voor Microsoft Teams](across-install-app-for-teams.md) installeren.

Om een [!INCLUDE [prod_short](includes/prod_short.md)]-tabblad te bekijken dat door een andere deelnemer aan het kanaal of de chat is toegevoegd, moet aan de volgende vereisten worden voldaan:

- U hebt toegang tot Microsoft Teams.
- U hebt een [!INCLUDE [prod_short](includes/prod_short.md)]-licentie of beperkte toegang tot Business Central met alleen een Microsoft 365-licentie. Zie [Business Central-toegang met Microsoft 365-licenties](admin-access-with-m365-license.md) voor meer informatie.
- U hebt de [!INCLUDE [prod_short](includes/prod_short.md)]-app in Teams geïnstalleerd.

## Een tabblad toevoegen met aanbevolen inhoud

Gebruik deze stappen om een tabblad toe te voegen door te kiezen wat u wilt weergeven uit een direct beschikbare lijst met aanbevolen inhoud die is gebaseerd op uw rolcentrum&mdash;zonder Teams te verlaten. Voor meer informatie over de inhoud waaruit u kunt kiezen, zie [Waar komt de aanbevolen inhoud vandaan?](/dynamics365/business-central/teams-faq?tabs=tabs#where-does-the-recommended-content-come-from).

1. Selecteer boven aan een kanaal of chat in Teams **+ Een tabblad toevoegen**.
2. Typ in het vak **Zoeken** *Business Central* en selecteer vervolgens het **[!INCLUDE [prod_short](includes/prod_short.md)]**-pictogram en wacht tot het [!INCLUDE [prod_short](includes/prod_short.md)]-tabbladconfiguratievenster verschijnt.

   ![Toont het configuratievenster van het Business Central-tabblad in Teams](media/teams-bc-tab-config-window.png)

3. De optie **Kiezen uit inhoud die wordt aanbevolen voor** toont het bedrijf in [!INCLUDE [prod_short](includes/prod_short.md)] waar u mee werkt. Als u inhoud van een ander bedrijf wilt weergeven, selecteert u het huidige bedrijf en gebruikt u de opties **Omgeving** en **Bedrijf** om aan te geven met welk bedrijf u wilt werken.
4. Selecteer pijl-omlaag in de optie **Tabbladinhoud** en kies de inhoud die u wilt weergeven.

   <!-- The list shows all pages that are bookmarked on your role center in [!INCLUDE [prod_short](includes/prod_short.md)]. To learn more about the content that you can choose from, see [Where does the recommended content come from?](teams-faq.md#recommended-content).-->
5. Sommige pagina's kunnen verschillende weergaven bevatten. Dit zijn varianten van de gefilterde pagina die specifieke gegevens weergeven. Om de weergave voor de inhoud te wijzigen, selecteert u de pijl omlaag voor de optie **Voorkeursweergave** en kiest u de weergave uit de lijst.

   Voor meer informatie over weergaven, zie [Lijstweergaven opslaan en personaliseren](ui-views.md).
6. Selecteer **Posten naar het kanaal over dit tabblad** om automatisch een aankondiging in het Teams-kanaal of de Teams-chat te plaatsen om deelnemers te laten weten dat u dit tabblad hebt toegevoegd.
7. Selecteer **Opslaan**.

## Een tabblad toevoegen met een paginakoppeling

Een andere manier om een tabblad toe te voegen door een koppeling (URL) te gebruiken naar de pagina die u wilt weergeven. Deze manier is handig wanneer u een specifieke [!INCLUDE [prod_short](includes/prod_short.md)]-record of een lijstpagina wilt weergeven die niet is gemarkeerd als bladwijzer in uw rolcentrum.

1. Selecteer boven aan een kanaal of chat in Teams **+ Een tabblad toevoegen**.
2. Typ *Business Central* in het vak **Zoeken** en selecteer vervolgens het **[!INCLUDE [prod_short](includes/prod_short.md)]**-pictogram .
3. Wacht tot het venster voor [!INCLUDE [prod_short](includes/prod_short.md)]-tabbladconfiguratie verschijnt en selecteer vervolgens de optie **Plak in plaats daarvan een [!INCLUDE [prod_short](includes/prod_short.md)]-koppeling**.

   ![Toont het configuratievenster van het Business Central-tabblad in Teams en markeert de koppelingsoptie](media/teams-bc-tab-config-window-page-link.png)
4. Ga naar [!INCLUDE [prod_short](includes/prod_short.md)] en open de pagina die u op het tabblad wilt weergeven.
5. Kopieer de koppeling naar de pagina.

   Er zijn twee manieren om de koppeling te kopiëren. De gemakkelijkste en voorkeursmanier is via het selecteren van **Delen** ![Pictogram delen in Business Central](media/share-icon.png) > **Koppeling kopiëren**. De andere manier is door de volledige URL vanuit de adresbalk van de browser te kopiëren. Voor meer informatie over deze stap, zie [Business Central-records en paginakoppelingen delen](across-working-with-teams.md).

6. Ga terug naar Teams en plak de koppeling in het vak **URL**.
7. Voer in het vak **Naam tabblad** een naam in die op het tabblad wordt weergegeven.
8. Selecteer **Posten naar het kanaal over dit tabblad** om automatisch een aankondiging in het Teams-kanaal of de Teams-chat te plaatsen om deelnemers te laten weten dat u dit tabblad hebt toegevoegd.
9. Selecteer **Opslaan**.

## Een tabblad toevoegen door kaartgegevens vast te zetten

Gebruik deze stappen om een tabblad toe te voegen voor een record dat werd gedeeld of geplakt in een Teams-kanaal of -chat. Voor meer informatie over het delen van records en paginakoppelingen in Teams, zie [Records en paginakoppelingen delen in teams](across-working-with-teams.md).

1. Selecteer in Teams de knop **Details** op de kaart.
2. Selecteer in de rechterbovenhoek van de kaartgegevens het pictogram **Vastzetten bovenaan de chat** ![Vastzetten-pictogram voor het toevoegen van het Teams-tabblad in Business Central](media/pin-teams.png).

## Een tabblad en de inhoud ervan wijzigen

Nadat een tabblad is toegevoegd, kunt u bepaalde wijzigingen in het tabblad aanbrengen. U kunt het tabblad bijvoorbeeld een nieuwe naam geven, verplaatsen en verwijderen. Deze acties vindt u in de tabbladopties die beschikbaar zijn door de pijl-omlaag op het tabblad te selecteren.

![Toont het configuratievenster van het Business Central-tabblad in Teams en het menu met tabbladopties](media/teams-bc-tab-config-window-options.png)

Wat de inhoud van een tabblad betreft, kunt u de gegevens wijzigen als u toestemming hebt. Als u de gegevens wijzigt, zien anderen de wijzigingen pas als ze het tabblad verlaten en terugkomen. Hetzelfde geldt voor u als iemand anders wijzigingen aanbrengt in gegevens. U kunt de pagina die op het tabblad wordt weergegeven niet wijzigen, dus verwijder gewoon het tabblad en voeg een ander passend tabblad toe.

Ook kunt u de weergave van de pagina en de bijbehorende gegevens wijzigen, zoals sorteren en schakelen tussen lijst- en tegelweergaven. Wanneer u dit soort wijzigingen aanbrengt, hebben ze geen invloed op wat anderen zien. Zij zien wat u oorspronkelijk hebt gepost, totdat ze zelf vergelijkbare wijzigingen aanbrengen.

## Zie ook

[Integratieoverzicht van Business Central en Microsoft Teams](across-teams-overview.md)  
[De [!INCLUDE [prod_short](includes/prod_short.md)]-app installeren voor Microsoft Teams](across-install-app-for-teams.md)  
[Business Central-records en paginakoppelingen delen in Microsoft Teams](across-working-with-teams.md).
[Veelgestelde vragen over Teams](teams-faq.md)  
[Zoeken naar klanten, leveranciers en andere contacten vanuit Microsoft Teams](across-search-contacts-teams.md)  
[Bedrijfs- en andere instellingen in Teams wijzigen](across-teams-settings.md)  
[Problemen met Teams oplossen](admin-teams-troubleshooting.md)  
[Ontwikkeling voor Teams-integratie](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
