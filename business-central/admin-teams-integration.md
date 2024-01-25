---
title: Microsoft Teams-integratie met Business Central beheren | Microsoft Docs
description: Business Central-integratie met Microsoft Teams beheren.
author: jswymer
ms.topic: overview
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork'
ms.date: 02/03/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Microsoft Teams-integratie met [!INCLUDE [prod_short](includes/prod_short.md)] beheren

[!INCLUDE [online_only](includes/online_only.md)]

Dit artikel geeft een overzicht van wat u als beheerder kunt doen om Microsoft Teams-integratie met [!INCLUDE [prod_short](includes/prod_short.md)] te beheren.

## In Microsoft Teams

### Minimumvereisten

In dit gedeelte worden de minimumvereisten voor de functies van de [!INCLUDE [prod_short](includes/prod_short.md)]-app beschreven om in Teams te werken.

- Vereiste licenties

    De [!INCLUDE[prod_short](includes/prod_short.md)]-app vereist een Teams-licentie via een Microsoft 365 Business- of Enterprise-abonnement. Zelfstandige Teams-abonnementen zoals Microsoft Teams (gratis) of Microsoft Teams Essentials worden niet ondersteund.

    De meeste kenmerken van de [!INCLUDE[prod_short](includes/prod_short.md)]-app voor Teams vereisen ook een [!INCLUDE [prod_short](includes/prod_short.md)]-licentie, zoals weergegeven in de volgende tabel.

    |Wat|[!INCLUDE [prod_short](includes/prod_short.md)]-licentie|
    |----|---|
    |Zoeken naar [!INCLUDE [prod_short](includes/prod_short.md)]-contacten.|![vinkje](media/check.png "vinkje")|
    |Een link naar een [!INCLUDE [prod_short](includes/prod_short.md)]-record opnemen in een gesprek en het verzenden als een kaart.|![vinkje](media/check.png "vinkje")|
    |Deel een link vanaf een pagina in [!INCLUDE [prod_short](includes/prod_short.md)] naar een Teams-gesprek.|![vinkje](media/check.png "vinkje")|
    |Een kaart van een [!INCLUDE [prod_short](includes/prod_short.md)]-record weergeven in een gesprek.||
    |Meer details van een kaart voor een [!INCLUDE [prod_short](includes/prod_short.md)]-record weergeven in een gesprek.|![vinkje](media/check.png "vinkje")|
    |Open een paginalink in [!INCLUDE [prod_short](includes/prod_short.md)] vanuit een gesprek.|![vinkje](media/check.png "vinkje")|

- URL-voorbeelden toestaan

    Beleidsinstelling **URL-voorbeelden toestaan** moet zijn ingeschakeld. Anders kan er geen kaart worden gegenereerd voor [!INCLUDE [prod_short](includes/prod_short.md)]-koppelingen die in een Teams-gesprek worden geplakt. Zie voor meer informatie over deze instelling [Berichtenbeleid beheren in Teams](/microsoftteams/messaging-policies-in-teams).

### De [!INCLUDE [prod_short](includes/prod_short.md)]-app beheren (optioneel)

Als Teams-beheerder kunt u alle apps voor uw organisatie beheren, inclusief de [!INCLUDE [prod_short](includes/prod_short.md)]-app. U kunt de [!INCLUDE [prod_short](includes/prod_short.md)]-app voor uw organisatie beheren, gebruikers blokkeren tegen het installeren van de app en meer.

Zie de volgende artikelen in de Microsoft Teams-documentatie voor meer informatie:

- [Uw apps beheren in het Microsoft Teams-beheercentrum](/MicrosoftTeams/manage-apps)
- [Installatiebeleid voor apps beheren in Microsoft Teams](/microsoftteams/teams-app-setup-policies)

## In [!INCLUDE [prod_short](includes/prod_short.md)]

### Minimumvereisten

- [!INCLUDE [prod_short](includes/prod_short.md)]-versie:

    [!INCLUDE [prod_short](includes/prod_short.md)] 2021 releasewave 1 of hoger. Teams-integratie wordt alleen ondersteund voor [!INCLUDE [prod_short](includes/prod_short.md)] online; niet on-premises.

- Codeunit **2718 Page Summary Provider** wordt gepubliceerd als een webservice:

    Deze codeunit wordt standaard als webservice gepubliceerd. De codeunit is onderdeel van de [!INCLUDE [prod_short](includes/prod_short.md)]-systeemtoepassing. De codeunit wordt gebruikt om de veldgegevens op te halen voor een [!INCLUDE [prod_short](includes/prod_short.md)]-pagina die wordt toegevoegd aan een Teams-gesprek. Zie [Een webservice publiceren](across-how-publish-web-service.md) voor informatie over het publiceren van webservices.

- <a name="permissions"></a>Gebruikersmachtigingen:

    De contactzoekopdrachten, pagina's en gegevens die gebruikers kunnen bekijken en bewerken in een Teams-gesprek worden voor het grootste deel bepaald door hun machtigingen in [!INCLUDE [prod_short](includes/prod_short.md)].

    - Om contacten te zoeken moeten gebruikers ten minste leesbevoegdheid hebben voor de tabel **Contacten**. 
    - Om een [!INCLUDE [prod_short](includes/prod_short.md)]-koppeling te plakken in een Teams-gesprek en deze te laten uitbreiden naar een kaart, moeten gebruikers ten minste leesrechten hebben voor de pagina en de gegevens ervan.
    - Zodra een kaart in een gesprek is ingediend, kan elke gebruiker in dat gesprek die kaart bekijken zonder toestemming voor [!INCLUDE [prod_short](includes/prod_short.md)].
    - Om meer details van een kaart te zien of de record te openen in [!INCLUDE [prod_short](includes/prod_short.md)] moeten gebruikers leesbevoegdheid hebben voor de pagina en de gegevens ervan.
    - Om gegevens te wijzigen hebben gebruikers wijzigingsmachtiging nodig.
    
    Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie over machtigingen.

## De Business Central-app installeren met behulp van gecentraliseerde implementatie

In het Microsoft Teams-beheercentrum configureert u het installatiebeleid voor Teams-apps voor de organisatie. In het Teams-beheercentrum kunt u de functie Gecentraliseerde implementatie gebruiken om de Business Central-app automatisch in Teams te installeren voor alle gebruikers in uw organisatie, specifieke groepen of individuele gebruikers.

> [!NOTE]
> Om gecentraliseerde implementatie in te stellen moet uw Teams-account de rol **Teams-servicebeheerder** of **Globale beheerder** hebben.

1. Kies in Business Central het pictogram ![Vergrootglas dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gecentraliseerde implementatie van Teams-app** in en kies vervolgens de gerelateerde koppeling. Of selecteer [hier](https://businesscentral.dynamics.com/?page=1833) om de pagina direct te openen.
2. Lees de informatie op de pagina **De Business Central-app voor Teams instellen** en kies dan **Volgende** wanneer u klaar bent.
3. Open het [Teams-beheercentrum](https://go.microsoft.com/fwlink/?linkid=2163970) en voer de volgende stappen uit.
    1. Ga naar **Teams-apps** > **Beleid instellen**.
    2. Maak een nieuw beleid of selecteer het beleid dat u wilt gebruiken om de Business Central-app te installeren en selecteer vervolgens **Apps toevoegen**.
    3. Zoek en selecteer op de pagina **Geïnstalleerde apps toevoegen** **Business Central**.
    4. Kies **Toevoegen**.

       Business Central zou nu moeten verschijnen onder **Geïnstalleerde apps** voor het beleid.
    5. Configureer indien nodig meer instellingen en kies vervolgens **Opslaan**.

    Voor meer informatie over het instellingsbeleid in Teams zie [Installatiebeleid voor apps beheren in Microsoft Teams](/MicrosoftTeams/teams-app-setup-policies) in de Teams-documentatie.
4. Ga terug naar **Gecentraliseerde implementatie van Teams-app** in Business Central en selecteer **Gereed**.

> [!IMPORTANT]
> Het kan tot 24 uur duren voordat het app-instellingsbeleid is toegepast en de app is geïmplementeerd voor gebruikers.

## Beheer van privacy en compliance 

Microsoft Teams biedt uitgebreide controles voor naleving en beheer van gevoelige of persoonlijk identificeerbare gegevens&mdash;inclusief gegevens die zijn toegevoegd aan chats en kanalen door de [!INCLUDE [prod_short](includes/prod_short.md)]-app.

### Begrijpen waar [!INCLUDE [prod_short](includes/prod_short.md)]-kaarten worden opgeslagen

Nadat een kaart naar een chat is verzonden, worden de kaart en de velden op de kaart gekopieerd naar Teams. Deze informatie valt onder het Teams-beleid voor uw organisatie, zoals het beleid voor het bewaren van gegevens. Bij het weergeven van kaartdetails wordt geen van de gegevens in het detailvenster opgeslagen in Teams. De gegevens blijven opgeslagen in [!INCLUDE [prod_short](includes/prod_short.md)] en worden alleen opgehaald door Teams wanneer de gebruiker ervoor kiest om de details te bekijken. 

- Zie voor meer informatie over waar Teams die gegevens opslaat [Locatie van gegevens in Microsoft Teams](/microsoftteams/location-of-data-in-teams).
- Zie voor meer informatie over het bewaarbeleid in Teams [Bewaarbeleid in Microsoft Teams](/microsoftteams/retention-policies).

### Het delen van kaarten beperken 

U voorkomt dat specifieke gebruikers of groepen kaarten naar chats of kanalen sturen door berichtenbeleid in te stellen dat de instelling **URL-voorbeelden** uitschakelt. Zie voor meer informatie over deze instelling [Berichtenbeleid beheren in Teams](/microsoftteams/messaging-policies-in-teams). 

U kunt ook informatiebarrières gebruiken om te voorkomen dat personen of groepen met elkaar communiceren. Zie voor meer informatie [Informatiebarrières in Microsoft Teams](/microsoftteams/information-barriers-in-teams).

Functies voor het voorkomen van gegevensverlies in het Microsoft 365 Security & Compliance Center kunnen niet specifiek op kaarten worden toegepast. Maar ze kunnen worden toegepast op de chatberichten die de kaarten bevatten. <!-- To track upcoming advanced features that include enabling DLP for cards, see [https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093](https://www.microsoft.com/en-us/microsoft-365/roadmap?featureid=67093).-->

### Reageren op gegevensaanvragen

U staat teamleden en teameigenaren toe om berichten te verwijderen die gevoelige kaarten bevatten door een berichtenbeleid in te stellen, zoals: **Eigenaren kunnen verzonden berichten verwijderen** en **Gebruikers kunnen verzonden berichten verwijderen**. Zie voor meer informatie [Berichtenbeleid beheren in Teams](/microsoftteams/messaging-policies-in-teams).

Functies voor het zoeken van inhoud en eDiscovery-naleving in het Microsoft 365 Security & Compliance Center kunnen ook op kaarten worden toegepast.

Omdat kaartgegevens in Teams een kopie zijn van gegevens in [!INCLUDE [prod_short](includes/prod_short.md)], kunt u ook [!INCLUDE [prod_short](includes/prod_short.md)]-functies gebruiken om gegevens van een klant op verzoek te exporteren. Zie voor meer informatie over privacy in [!INCLUDE [prod_short](includes/prod_short.md)] [Veelgestelde vragen over privacy voor Business Central-klanten](/dynamics365/business-central/dev-itpro/security/privacyfaq).

## Toon of verberg recordgegevens op kaarten

Wanneer een record wordt gedeeld met anderen in een Teams-chat of -kanaal, wordt een kaart weergegeven met velden die gegevens over de record bevatten. Alle ontvangers kunnen deze gegevens (of recordsamenvatting) standaard bekijken, ongeacht hun licentie of machtigingen in Business Central. Als u een beheerder bent, kunt u de begeleide instelling **Kaartinstellingen** gebruiken om het recordoverzicht te verbergen voor weergave op kaarten in Teams. Als u het recordoverzicht verbergt, worden alle velden en afbeeldingen verwijderd, maar blijven de knop **Details** en andere, niet-recordinformatie op de kaart wel zichtbaar.

|Recordoverzicht ingeschakeld|Recordoverzicht uitgeschakeld|
|-|-|
|![Afbeelding die een kaart laat zien in Teams wanneer het recordoverzicht is ingeschakeld.](media/card-settings-example-on.png)|![Afbeelding die een kaart laat zien in Teams wanneer het recordoverzicht is uitgeschakeld.](media/card-settings-example-off.png)|

U configureert de instelling per omgeving. Dus wanneer u het recordoverzicht in- of uitschakelt, heeft dit gevolgen voor alle bedrijven in de omgeving.

1. Open de omgeving die u wilt wijzigen in Business Central.

   > [!TIP]
   > Om van omgeving te wisselen, selecteert u <kbd>Ctrl</kbd>+<kbd>O</kbd>.
2. Kies het ![Vergrootglas dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), pictogram, voer **Kaartinstellingen** in en kies de gerelateerde koppeling. <!--Or, select [here](https://businesscentral.dynamics.com/?page=1833) to open the page directly.-->
3. Lees de informatie op de **Kaartinstellingen** en kies vervolgens **Volgende** als u klaar bent.
4. Zet op de pagina **Zichtbaarheid van gegevens** de schakelaar **Recordoverzicht weergeven** aan om de gegevens op de kaart weer te geven of uit om deze te verbergen.
5. Selecteer **Volgende** en volg de instructies om de installatiegids te voltooien.

## Zie ook

Overzicht van integratie tussen [[!INCLUDE [prod_short](includes/prod_short.md)] en Microsoft Teams](across-teams-overview.md)  
[De [!INCLUDE [prod_short](includes/prod_short.md)]-app installeren voor Microsoft Teams](across-install-app-for-teams.md)  
[Veelgestelde vragen over Teams](teams-faq.md)  
[Problemen met Teams oplossen](admin-teams-troubleshooting.md)  
[Ontwikkeling voor Teams-integratie](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]