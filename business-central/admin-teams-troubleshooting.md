---
title: Problemen met Microsoft Teams-integratie oplossen
description: Lees wat u als beheerder kunt doen om Microsoft Teams-integratie te beheren.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, troubleshooting, errors
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: 7a98b53a34ddf403cf6507da7740b97924d4c81c
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385211"
---
# <a name="troubleshooting-microsoft-teams-integration-with-prod_short"></a>Problemen met Microsoft Teams-integratie oplossen met [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Dit artikel bevat informatie over het identificeren en oplossen van problemen die u kunt ondervinden tijdens het gebruik van Microsoft Teams met [!INCLUDE [prod_short](includes/prod_short.md)], als een typische gebruiker of beheerder.

## <a name="none-of-my-links-expand-into-a-card"></a>Geen van mijn koppelingen breidt zich uit tot een kaart 

Als u dit probleem ondervindt, kunt u het volgende proberen:

1. Zorg er eerst voor dat de [!INCLUDE [prod_short](includes/prod_short.md)]-app voor Teams is geïnstalleerd.

    Meld u aan bij de Teams-desktop-app of Teams in de browser om dit te controleren. Selecteer vervolgens aan de linkerkant **Apps** en zoek naar **[!INCLUDE [prod_short](includes/prod_short.md)]**. Als u de **[!INCLUDE [prod_short](includes/prod_short.md)]**-app vindt, selecteert u deze om de pagina met app-details te openen. Als de knop **Voor mij toevoegen** wordt weergegeven, is de app [!INCLUDE [prod_short](includes/prod_short.md)] niet geïnstalleerd. Zie voor meer informatie over het installeren van de app [De [!INCLUDE [prod_short](includes/prod_short.md)]-app voor Microsoft Teams](across-install-app-for-teams.md) installeren.

    > [!NOTE]
    > Gastgebruikers kunnen niet meteen apps installeren. Zie onze veelgestelde vragen over samenwerken met gasten voor meer informatie over gastgebruikers. 

2. Controleer vervolgens of u bent aangemeld met de juiste identiteit.

    Ga in Teams naar een willekeurige chat en kies onder het vak voor het opstellen van berichten het pictogram [!INCLUDE [prod_short](includes/prod_short.md)]. Als het venster verschijnt, controleert u of de gebruiker als wie u bent verbonden, overeenkomt met wat u gebruikt om verbinding te maken met [!INCLUDE [prod_short](includes/prod_short.md)].

3. Zorg dat codeunit 2718 **Page Summary Provider** is gepubliceerd als een webservice.

    Teams maakt verbinding met [!INCLUDE [prod_short](includes/prod_short.md)] met behulp van een eindpunt voor deze codeunit in de service [!INCLUDE [prod_short](includes/prod_short.md)]. Zie [Een webservice publiceren](across-how-publish-web-service.md) voor informatie over het publiceren van webservices.

4. Uw organisatie kan u ook beperken in het plakken van koppelingen die tot kaarten worden uitgevouwen. Neem contact op met uw beheerder om het organisatiebeleid van Teams te begrijpen dat op u van toepassing kan zijn.

## <a name="my-link-sometimes-doesnt-expand-into-a-card"></a>Mijn koppeling breidt zich soms niet uit tot een kaart 

Een koppeling wordt in de volgende situaties niet uitgebreid naar een kaart:

- De koppeling is gericht op een pagina van een type dat geen record vertegenwoordigt. Het kan bijvoorbeeld een koppeling zijn naar het rolcentrum van [!INCLUDE [prod_short](includes/prod_short.md)]. U kunt het paginatype controleren met behulp van het pagina-inspectievenster in de webclient in [!INCLUDE [prod_short](includes/prod_short.md)]. Zie voor meer informatie over pagina-inspectie [Pagina's inspecteren](across-inspect-page.md).
- De koppeling is gericht op een pagina die (op technisch niveau) niet is verbonden met een brontabel in [!INCLUDE [prod_short](includes/prod_short.md)]. U kunt controleren of een pagina een brontabel heeft met het pagina-inspectievenster in de webclient in [!INCLUDE [prod_short](includes/prod_short.md)]. Zie voor meer informatie over pagina-inspectie [Pagina's inspecteren](across-inspect-page.md). 
- Teams ondersteunt in sommige functies geen koppelingsvoorbeelden. Wanneer u bijvoorbeeld een chat opent, u in een vergadering zit of u een gast bent bij een andere organisatie.
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

## <a name="the-card-is-displayed-in-the-message-compose-box-but-selecting-the-details-button-does-nothing"></a>De kaart wordt weergegeven in het berichtopstelvak, maar het selecteren van de knop Details doet niets 

Nadat een koppeling is uitgevouwen tot een kaart in het berichtopstelvak, moet u het bericht naar de chat sturen voordat u de knop **Details** kunt gebruiken.

## <a name="the-details-window-opens-but-shows-an-error-before-details-are-shown"></a>Het detailvenster wordt geopend, maar toont een fout voordat details worden weergegeven

Dit probleem kan worden veroorzaakt door een paar dingen: gebrek aan machtigingen in [!INCLUDE [prod_short](includes/prod_short.md)] of browserinstellingen (bij gebruik van Teams in de browser).

1. Controleer uw machtigingen in [!INCLUDE [prod_short](includes/prod_short.md)].

    Om details van een kaart weer te geven, controleert [!INCLUDE [prod_short](includes/prod_short.md)] uw licentie en machtigingen om die specifieke record en pagina in het specifieke bedrijf en de specifieke omgeving weer te geven. Als u voor geen van deze dingen geautoriseerd bent, worden standaard [!INCLUDE [prod_short](includes/prod_short.md)]-foutmeldingen over machtigingen weergegeven in het detailvenster. 

    Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie over machtigingen

2. Controleer uw browserinstellingen als u Teams in de browser gebruikt.

    - De pop-upblokkering van uw browser moet zijn uitgeschakeld of zijn ingesteld om pop-ups van het domein *businesscentral.dynamics.com* of *bc.dynamics.com* toe te staan. Voor informatie over het toestaan van pop-ups voor [!INCLUDE [prod_short](includes/prod_short.md)], zie [Uw browser instellen](across-browser-settings.md#popup).
    - Uw browser moet toegang hebben tot de lokale browseropslag voor cookies en voorkeuren terwijl u werkt.
    - Gebruik geen gast- of privé-browsing, tenzij dit nodig is, omdat ze bepaalde inhoud in sommige browsers verwijderen of blokkeren.

    Zie voor meer informatie over minimale browservereisten [Minimumvereisten voor gebruik van [!INCLUDE [prod_short](includes/prod_short.md)]](product-requirements.md#browsers) 

## <a name="im-having-problems-with-the-camera-or-location-in-teams"></a>Ik heb problemen met de camera of locatie in Teams 

Tijdens gebruik van [!INCLUDE [prod_short](includes/prod_short.md)]-functies in het detailvenster waarvoor toegang tot uw locatie of apparaatcamera is vereist, moet u Teams eerst toestemming geven om toegang te krijgen tot deze apparaatfuncties.  

- Zorg er voor Teams in de browser voor dat uw browserinstellingen toegang toestaan tot camera en locatie voor https://teams.microsoft.com. 

- Zorg er voor Teams voor iOS of Android voor dat uw apparaatinstellingen toegang toestaan tot camera en locatie voor de mobiele Teams-app. 

Zie voor hulp bij het wijzigen van deze instellingen [Mijn camera werkt niet in Teams](https://support.microsoft.com/office/my-camera-isn-t-working-in-teams-9581983b-c6f9-40e3-b0d8-122857972ade?ns=msftteams&version=16&ui=en-us&rs=en-us&ad=us) bij Microsoft Ondersteuning.

De [!INCLUDE [prod_short](includes/prod_short.md)]-app biedt geen ondersteuning voor locatie in de Teams-desktop-app. Zie de [Veelgestelde vragen over Teams](teams-faq.md#location) voor meer informatie.

Met sommige browsers, zoals het nieuwe Microsoft Edge, kunt u kiezen welke apparaatcamera u wilt gebruiken wanneer uw apparaat meerdere camera's ondersteunt. 

## <a name="teams-displays-mixed-languages-for-my-cards-and-card-details"></a>Teams geeft verschillende talen weer voor mijn kaarten en kaartgegevens

Om kaarten en kaartdetails consistent weer te geven in dezelfde taal in Teams, moeten de taal van uw Teams-client en de taal die u gebruikt in de [!INCLUDE [prod_short](includes/prod_short.md)]-webclient, overeenkomen.

- Zie voor meer informatie over het wijzigen van de taal in Teams [Instellingen wijzigen in Teams](https://support.microsoft.com/en-us/office/change-settings-in-teams-b506e8f1-1a96-4cf1-8c6b-b6ed4f424bc7) op Microsoft-ondersteuning. 

- Voor meer informatie over het wijzigen van de taal in [!INCLUDE [prod_short](includes/prod_short.md)] raadpleegt u [Basisinstellingen wijzigen - taal](ui-change-basic-settings.md#language).

Voor meer informatie over hoe talen werken tussen Teams en [!INCLUDE [prod_short](includes/prod_short.md)] raadpleegt u [Veelgestelde vragen over Teams](teams-faq.md#language).

## <a name="i-edited-a-field-in-the-details-window-but-my-change-wasnt-saved"></a>Ik heb een veld in het detailvenster bewerkt, maar mijn wijziging is niet opgeslagen

Wijzigingen die u aanbrengt in een veld in de detailvensters, worden automatisch opgeslagen wanneer u het veld verlaat. Voordat u het venster sluit nadat u een veld heeft gewijzigd, moet u op de Tab-toets drukken of buiten het veld klikken/tikken.

## <a name="a-new-tile-appeared-in-the-app-launcher-how-do-i-remove-it"></a>Er is een nieuwe tegel verschenen in het startprogramma. Hoe verwijder ik deze?

Wanneer u uw apps op de Office 365-startpagina (https://home.office.com) of in het startprogramma bekijkt, verschijnt een nieuwe tegel met de naam 'Business Central Teams Integration Service Connector' na installatie van de [!INCLUDE [prod_short](includes/prod_short.md)]-app voor Teams. Deze tegel heeft op zichzelf geen waarde en kan veilig worden verborgen.

Als beheerder met Azure Active Directory-beheerdersmachtigingen kunt u de tegel verbergen door de volgende stappen uit te voeren:

1. Meld u aan bij het [Azure Active Directory-beheercentrum](https://aad.portal.azure.com/).
2. Selecteer **Enterprise-apps** en selecteer **Business Central Teams Integration Service Connector**.
3. Selecteer **Eigenschappen** en stel vervolgens de schakelaar **Zichtbaar voor gebruikers** in op **Nee**.
4. Selecteer **Opslaan**.

> [!NOTE]
> Het zal even duren voordat deze wijziging van kracht wordt.


## <a name="see-also"></a>Zie ook

Overzicht van integratie tussen [[!INCLUDE [prod_short](includes/prod_short.md)] en Microsoft Teams](across-teams-overview.md)  
[De [!INCLUDE [prod_short](includes/prod_short.md)]-app installeren voor Microsoft Teams](across-install-app-for-teams.md)  
[Veelgestelde vragen over Teams](teams-faq.md)  
[Ontwikkeling voor Teams-integratie](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]