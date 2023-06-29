---
title: Problemen met Microsoft Teams-integratie oplossen
description: Lees wat u als beheerder kunt doen om Microsoft Teams-integratie te beheren.
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, troubleshooting, errors'
ms.date: 10/01/2021
ms.author: jswymer
---

# <a name="troubleshooting-microsoft-teams-integration-with-"></a><a name="troubleshooting-microsoft-teams-integration-with-"></a>Problemen met Microsoft Teams-integratie oplossen met [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Dit artikel bevat informatie over het identificeren en oplossen van problemen die u kunt ondervinden tijdens het gebruik van Microsoft Teams met [!INCLUDE [prod_short](includes/prod_short.md)], als een typische gebruiker of beheerder.

## <a name="the-sign-in-link-doesnt-work"></a><a name="the-sign-in-link-doesnt-work"></a>De aanmeldkoppeling werkt niet

Als u probeert in te loggen bij de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams, onmiddellijk na het installeren van de app, en de aanmeldkoppeling niet reageert, kan het zijn dat de app de installatie niet volledig heeft voltooid. Om het probleem op te lossen logt u uit bij uw Teams-client en logt u vervolgens opnieuw in.

## <a name="the-settings-page-is-empty"></a><a name="the-settings-page-is-empty"></a>De pagina Instellingen is leeg

U moet eerst inloggen om bij uw instellingen te komen. Om in te loggen op de app, plakt u een koppeling naar een [!INCLUDE [prod_short.md](includes/prod_short.md)]-record of probeert u contacten te zoeken. Beide acties leiden u door een aanmeldingservaring, waarna u de pagina **Instellingen** kunt gebruiken.

## <a name="i-changed-company-but-it-didnt-seem-to-work"></a><a name="i-changed-company-but-it-didnt-seem-to-work"></a>Ik ben van bedrijf veranderd, maar het lijkt niet te werken

Nadat u het bedrijf op de pagina **Instellingen** hebt gewijzigd, merkt u misschien dat de vervolgkeuzelijst met het opdrachtvak aangeeft dat u nog steeds naar het vorige bedrijf zoekt. Dit probleem treedt op wanneer u de pagina **Instellingen** rechtstreeks vanuit het opdrachtvenster opent. In dit geval is het bedrijf succesvol gewijzigd en zoekt u in feite in het bedrijf waarnaar u bent overgeschakeld. Het probleem is dat de vervolgkeuzelijst met het opdrachtvak nog niet is bijgewerkt. Als u wilt dat de vervolgkeuzelijst nauwkeurig het bedrijf weergeeft waarin u zoekt, sluit u [!INCLUDE [prod_short.md](includes/prod_short.md)] of maakt u het los vanuit het opdrachtvenster en opent u de app opnieuw.


<!--When you change company from the **Settings** page that you reach from the command box, returning to the command box drop-down continues to show the previous company even though the company was successfully changed. For the drop-down accurately reflect the company you'll search in, you must close or unpin [!INCLUDE [prod_short.md](includes/prod_short.md)] from the command box and then find it again.-->

## <a name="something-went-wrong-error-when-searching-for-contacts"></a><a name="something-went-wrong-error-when-searching-for-contacts"></a>Fout 'Er is iets fout gegaan' bij het zoeken naar contacten

Deze fout kan optreden wanneer u zoekt in een bedrijf dat niet is geïnitialiseerd of niet meer reageert. U kunt bijvoorbeeld niet zoeken in een nieuw proefbedrijf dat de gebruiksvoorwaarden nog niet heeft geaccepteerd. Om dit probleem op te lossen probeert u zich aan te melden bij de [!INCLUDE [prod_short.md](includes/prod_short.md)]-webclient, en handelt u naar of sluit u eventuele initiële dialoogvensters die verschijnen.

## <a name="cannot-find-the-contactcontact-summary-api-error-when-searching-for-contacts"></a><a name="cannot-find-the-contactcontact-summary-api-error-when-searching-for-contacts"></a>De fout Kan de contact-/contactoverzicht-API niet vinden bij het zoeken naar contactpersonen

Dit probleem kan worden veroorzaakt door aanpassingen of brancheoplossingen die van invloed zijn op [!INCLUDE [prod_short.md](includes/prod_short.md)] of ze bieden geen contact- of contactoverzicht-API. Neem contact op met uw beheerder of ondersteunende partner als het probleem zich blijft voordoen.

## <a name="none-of-my-links-expand-into-a-card"></a><a name="none-of-my-links-expand-into-a-card"></a>Geen van mijn koppelingen breidt zich uit tot een kaart

Als u dit probleem ondervindt, kunt u het volgende proberen:

1. Zorg er eerst voor dat de [!INCLUDE [prod_short](includes/prod_short.md)]-app voor Teams is geïnstalleerd.

    Meld u aan bij de Teams-desktop-app of Teams in de browser om dit te controleren. Selecteer vervolgens aan de linkerkant **Apps** en zoek naar **[!INCLUDE [prod_short](includes/prod_short.md)]**. Als u de **[!INCLUDE [prod_short](includes/prod_short.md)]**-app vindt, selecteert u deze om de pagina met app-details te openen. Als de knop **Voor mij toevoegen** wordt weergegeven, is de app [!INCLUDE [prod_short](includes/prod_short.md)] niet geïnstalleerd. Zie voor meer informatie over het installeren van de app [De [!INCLUDE [prod_short](includes/prod_short.md)]-app voor Microsoft Teams](across-install-app-for-teams.md) installeren.

    > [!NOTE]
    > Gastgebruikers kunnen niet meteen apps installeren. Zie onze veelgestelde vragen over samenwerken met gasten voor meer informatie over gastgebruikers. 

2. Controleer vervolgens of u bent aangemeld met de juiste identiteit.

    In Teams gaat u naar een chat, onder het vak voor het samenstellen van een bericht, klikt u met de rechtermuisknop op het pictogram [!INCLUDE [prod_short](includes/prod_short.md)] en kiest u vervolgens **Instellingen**. Als het venster verschijnt, controleert u of de gebruiker als wie u bent verbonden, overeenkomt met wat u gebruikt om verbinding te maken met [!INCLUDE [prod_short](includes/prod_short.md)].

3. Zorg dat codeunit 2718 **Page Summary Provider** is gepubliceerd als een webservice.

    Teams maakt verbinding met [!INCLUDE [prod_short](includes/prod_short.md)] met behulp van een eindpunt voor deze codeunit in de service [!INCLUDE [prod_short](includes/prod_short.md)]. Zie [Een webservice publiceren](across-how-publish-web-service.md) voor informatie over het publiceren van webservices.

4. Uw organisatie kan u ook beperken in het plakken van koppelingen die tot kaarten worden uitgevouwen. Neem contact op met uw beheerder om het organisatiebeleid van Teams te begrijpen dat op u van toepassing kan zijn.

## <a name="my-link-sometimes-doesnt-expand-into-a-card"></a><a name="my-link-sometimes-doesnt-expand-into-a-card"></a>Mijn koppeling breidt zich soms niet uit tot een kaart

Een koppeling wordt in de volgende situaties niet uitgebreid naar een kaart:

- De koppeling is gericht op een pagina die (op technisch niveau) niet is verbonden met een brontabel in [!INCLUDE [prod_short](includes/prod_short.md)]. U kunt controleren of een pagina een brontabel heeft met het pagina-inspectievenster in de webclient in [!INCLUDE [prod_short](includes/prod_short.md)]. Zie voor meer informatie over pagina-inspectie [Pagina's inspecteren](across-inspect-page.md).
- Teams ondersteunt in sommige functies geen koppelingsvoorbeelden. Wanneer u bijvoorbeeld een chat uitklapt of u een gast bent bij een andere organisatie.
- Teams stopt geruisloos na 15 seconden met proberen de kaart weer te geven, bijvoorbeeld vanwege netwerkproblemen.
- Teams mag de koppeling niet uitvouwen als u al een koppeling in hetzelfde berichtopstelvak hebt geplakt en de kaart hebt verwijderd.

De koppeling moet ook alle benodigde informatie bevatten om de record te vinden en de bijbehorende kaart weer te geven. Deze informatie omvat:

- De omgevingsnaam, door deze op te nemen in het URL-pad. Als u de omgevingsnaam niet opgeeft, gaat Teams ervan uit dat u probeert de omgeving met de naam 'Productie' te bereiken.
- De bedrijfsnaam, met behulp van de parameter *company=*
- De pagina-id, met behulp van de parameter *page=*
- De bladwijzer naar de record, met behulp van de parameter *bookmark=*

Voorbeeld:

`https://businesscentral.dynamics.com/?environmentname=Production&company=CRONUS%20USA%2C%20Inc.&page=21&dc=0&bookmark=21%3bEgAAAAJ7BTEAMAAwADAAMA%3d%3d`

Voor technische details over [!INCLUDE [prod_short](includes/prod_short.md)]-URL's, zie [Webclient-URL](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls) in de [!INCLUDE [prod_short](includes/prod_short.md)] Help voor ontwikkelaars en IT Pro.

## <a name="the-details-window-opens-but-shows-an-error-before-details-are-shown"></a><a name="the-details-window-opens-but-shows-an-error-before-details-are-shown"></a>Het detailvenster wordt geopend, maar toont een fout voordat details worden weergegeven

Dit probleem kan worden veroorzaakt door een paar dingen: gebrek aan machtigingen in [!INCLUDE [prod_short](includes/prod_short.md)] of browserinstellingen (bij gebruik van Teams in de browser).

1. Controleer uw machtigingen in [!INCLUDE [prod_short](includes/prod_short.md)].

    Om details van een kaart weer te geven, controleert [!INCLUDE [prod_short](includes/prod_short.md)] uw licentie en machtigingen om die specifieke record en pagina in het specifieke bedrijf en de specifieke omgeving weer te geven. Als u voor geen van deze dingen geautoriseerd bent, worden standaard [!INCLUDE [prod_short](includes/prod_short.md)]-foutmeldingen over machtigingen weergegeven in het detailvenster. 

    Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie over machtigingen

2. Controleer uw browserinstellingen als u Teams in de browser gebruikt.

    - De pop-upblokkering van uw browser moet zijn uitgeschakeld of zijn ingesteld om pop-ups van het domein *businesscentral.dynamics.com* of *bc.dynamics.com* toe te staan. Voor informatie over het toestaan van pop-ups voor [!INCLUDE [prod_short](includes/prod_short.md)], zie [Uw browser instellen](across-browser-settings.md#popup).
    - Uw browser moet toegang hebben tot de lokale browseropslag voor cookies en voorkeuren terwijl u werkt.
    - Gebruik geen gast- of privé-browsing, tenzij dit nodig is, omdat ze bepaalde inhoud in sommige browsers verwijderen of blokkeren.

    Zie voor meer informatie over minimale browservereisten [Minimumvereisten voor gebruik van [!INCLUDE [prod_short](includes/prod_short.md)]](product-requirements.md#browsers) 

## <a name="im-having-problems-with-the-camera-or-location-in-teams"></a><a name="im-having-problems-with-the-camera-or-location-in-teams"></a>Ik heb problemen met de camera of locatie in Teams

Tijdens gebruik van [!INCLUDE [prod_short](includes/prod_short.md)]-functies in het detailvenster waarvoor toegang tot uw locatie of apparaatcamera is vereist, moet u Teams eerst toestemming geven om toegang te krijgen tot deze apparaatfuncties.  

- Zorg er voor Teams in de browser voor dat uw browserinstellingen toegang toestaan tot camera en locatie voor https://teams.microsoft.com. 

- Zorg er voor Teams voor iOS of Android voor dat uw apparaatinstellingen toegang toestaan tot camera en locatie voor de mobiele Teams-app. 

Zie voor hulp bij het wijzigen van deze instellingen [Mijn camera werkt niet in Teams](https://support.microsoft.com/office/my-camera-isn-t-working-in-teams-9581983b-c6f9-40e3-b0d8-122857972ade?ns=msftteams&version=16&ui=en-us&rs=en-us&ad=us) bij Microsoft Ondersteuning.

De [!INCLUDE [prod_short](includes/prod_short.md)]-app biedt geen ondersteuning voor locatie in de Teams-desktop-app. Zie de [Veelgestelde vragen over Teams](teams-faq.md#location) voor meer informatie.

Met sommige browsers, zoals het nieuwe Microsoft Edge, kunt u kiezen welke apparaatcamera u wilt gebruiken wanneer uw apparaat meerdere camera's ondersteunt. 

## <a name="teams-displays-mixed-languages-for-my-cards-and-card-details"></a><a name="teams-displays-mixed-languages-for-my-cards-and-card-details"></a>Teams geeft verschillende talen weer voor mijn kaarten en kaartgegevens

Om kaarten en kaartdetails consistent weer te geven in dezelfde taal in Teams, moeten de taal van uw Teams-client en de taal die u gebruikt in de [!INCLUDE [prod_short](includes/prod_short.md)]-webclient, overeenkomen.

- Zie voor meer informatie over het wijzigen van de taal in Teams [Instellingen wijzigen in Teams](https://support.microsoft.com/en-us/office/change-settings-in-teams-b506e8f1-1a96-4cf1-8c6b-b6ed4f424bc7) op Microsoft-ondersteuning. 

- Voor meer informatie over het wijzigen van de taal in [!INCLUDE [prod_short](includes/prod_short.md)] raadpleegt u [Basisinstellingen wijzigen - taal](ui-change-basic-settings.md#language).

Voor meer informatie over hoe talen werken tussen Teams en [!INCLUDE [prod_short](includes/prod_short.md)] raadpleegt u [Veelgestelde vragen over Teams](teams-faq.md#language).

## <a name="i-edited-a-field-in-the-details-window-but-my-change-wasnt-saved"></a><a name="i-edited-a-field-in-the-details-window-but-my-change-wasnt-saved"></a>Ik heb een veld in het detailvenster bewerkt, maar mijn wijziging is niet opgeslagen

Wijzigingen die u aanbrengt in een veld in de detailvensters, worden automatisch opgeslagen wanneer u het veld verlaat. Voordat u het venster sluit nadat u een veld heeft gewijzigd, moet u de <kbd>Tab</kbd>-toets selecteren of buiten het veld klikken/tikken.

## <a name="a-new-tile-appeared-in-the-app-launcher-how-do-i-remove-it"></a><a name="a-new-tile-appeared-in-the-app-launcher-how-do-i-remove-it"></a>Er is een nieuwe tegel verschenen in het startprogramma. Hoe verwijder ik deze?

Wanneer u uw apps op de Office 365-startpagina (https://home.office.com) of in het startprogramma bekijkt, verschijnt een nieuwe tegel met de naam 'Business Central Teams Integration Service Connector' na installatie van de [!INCLUDE [prod_short](includes/prod_short.md)]-app voor Teams. Deze tegel heeft op zichzelf geen waarde en kan veilig worden verborgen.

Als beheerder met Azure Active Directory-beheerdersmachtigingen kunt u de tegel verbergen door de volgende stappen uit te voeren:

1. Meld u aan bij het [Azure Active Directory-beheercentrum](https://aad.portal.azure.com/).
2. Selecteer **Enterprise-apps** en selecteer **Business Central Teams Integration Service Connector**.
3. Selecteer **Eigenschappen** en stel vervolgens de schakelaar **Zichtbaar voor gebruikers** in op **Nee**.
4. Selecteer **Opslaan**.

> [!NOTE]
> Het zal even duren voordat deze wijziging van kracht wordt.

## <a name="duplicate-text-in-the-share-to-teams-window"></a><a name="duplicate-text-in-the-share-to-teams-window"></a>Dubbele tekst in het venster Delen met Teams

Wanneer u tekst in het berichtvenster plakt in het venster **Delen met Teams** wordt de tekst gedupliceerd. Dit probleem is bekend bij Microsoft en zal in een latere update worden verholpen. 

## <a name="unable-to-sign-into-the-share-to-teams-window"></a><a name="unable-to-sign-into-the-share-to-teams-window"></a>Kan niet inloggen op het venster Delen met Teams

Dit probleem kan verschillende oorzaken hebben. De identiteit die u gebruikt om in te loggen, moet bijvoorbeeld toegang hebben tot Microsoft Teams, bijvoorbeeld via een Microsoft 365-abonnement.

## <a name="my-cards-no-longer-have-a-popout-button"></a><a name="my-cards-no-longer-have-a-popout-button"></a>Mijn kaarten hebben geen pop-outknop meer

Vanaf april 2022 bevatten koppelingen die in Teams als compacte kaart worden weergegeven niet langer de knop **Pop-out**. Als u die kaart in een eigen venster wilt openen, kiest u de knop **Details** en vervolgens **Openen in browser** in het menu met het beletselteken (**...**) in de rechterbovenhoek van het venster.

## <a name="cant-pin-a-card-to-tab"></a><a name="cant-pin-a-card-to-tab"></a>Kan een kaart niet vastzetten op tabblad

Hiervoor zijn een aantal redenen.

- Als de kaart is gedeeld vanuit Search ME, kan deze niet aan een tabblad worden vastgemaakt. 

- U kunt de kaart pas vastzetten als u uw eerste Business Central-tabblad toevoegt. Dit probleem is bekend in Teams. 

## <a name="someone-added-a-tab-but-the-tab-doesnt-show-up-for-me"></a><a name="someone-added-a-tab-but-the-tab-doesnt-show-up-for-me"></a>Iemand heeft een tabblad toegevoegd, maar ik kan het tabblad niet zien

Dit probleem wordt veroorzaakt doordat u de BC-app voor Teams niet hebt geïnstalleerd. Alleen mensen die de app hebben geïnstalleerd, zien Business Central-tabbladen.

## <a name="others-see-different-sorting-or-column-layout-than-what-the-tab-author-sees"></a><a name="others-see-different-sorting-or-column-layout-than-what-the-tab-author-sees"></a>Anderen zien een andere sortering of kolomindeling dan die de auteur van het tabblad ziet

Dit probleem wordt waarschijnlijk veroorzaakt doordat u een lijstweergave hebt gedeeld die een persoonlijke weergave is. Werk in dit geval samen met uw beheerder om rolspecifieke lijstweergaven te maken die de verschillende rollen in het kanaal/de chat beslaan of maak deze weergave voor de hele organisatie zodat iedereen een consistente weergave kan krijgen.


## <a name="see-also"></a><a name="see-also"></a>Zie ook

Overzicht van integratie tussen [[!INCLUDE [prod_short](includes/prod_short.md)] en Microsoft Teams](across-teams-overview.md)  
[De [!INCLUDE [prod_short](includes/prod_short.md)]-app installeren voor Microsoft Teams](across-install-app-for-teams.md)  
[Zoeken naar klanten, leveranciers en andere contacten vanuit Microsoft Teams](across-search-contacts-teams.md)  
[Records delen in Microsoft Teams](across-working-with-teams.md)  
[Veelgestelde vragen over Teams](teams-faq.md)  
[Bedrijfs- en andere instellingen in Teams wijzigen](across-teams-settings.md)  
[Ontwikkeling voor Teams-integratie](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
