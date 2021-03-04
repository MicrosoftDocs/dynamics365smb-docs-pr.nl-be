---
title: Veelgestelde vragen over Teams
description: Krijg antwoorden op enkele veelvoorkomende vragen over het werken met Teams en Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, faq, errors
ms.date: 01/26/2021
ms.author: jswymer
ms.openlocfilehash: 79b6069ffb4c73d783b2c05d3a44a55763805a52
ms.sourcegitcommit: 1c9eec7554305603d688bf85ce3986d0b1f72ede
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/26/2021
ms.locfileid: "5068446"
---
# <a name="teams-faq"></a>Veelgestelde vragen over Teams

[!INCLUDE [online_only](includes/online_only.md)]

In dit artikel worden enkele van de vragen beantwoord die u mogelijk hebt over het werken met Teams en [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="general"></a>[Alge&meen](#tab/general)

### <a name="how-do-i-sign-in-to-the-prod_shortmd-app-in-teams"></a>Hoe log ik in bij de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app in Teams? 

Nadat u de app heeft geïnstalleerd, wordt u gevraagd om in te loggen wanneer u voor het eerst een [!INCLUDE [prod_short.md](includes/prod_short.md)]-koppeling in Teams-chat plakt of wanneer u de actie **Details** kiest op een kaart in Teams. Afhankelijk van uw Teams-client, moet u mogelijk uw inloggegevens invoeren die u gebruikt om toegang te krijgen tot [!INCLUDE [prod_short.md](includes/prod_short.md)]. 

### <a name="how-do-i-sign-out-of-the-prod_shortmd-app-in-teams"></a>Hoe log ik uit bij de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app in Teams? 

Om u af te melden bij uw huidige gebruikersidentiteit in Teams waarmee u verbinding heeft gemaakt met [!INCLUDE [prod_short.md](includes/prod_short.md)], gaat u naar een willekeurig chatvak en kiest u het pictogram [!INCLUDE [prod_short.md](includes/prod_short.md)] eronder. Als het venster verschijnt, controleert u uw momenteel aangemelde identiteit en kiest u vervolgens **Afmelden**. Als u Teams in de browser gebruikt, wordt u ook uitgelogd bij een eventuele [!INCLUDE [prod_short.md](includes/prod_short.md)]-webclient in hetzelfde browservenster.

### <a name="does-the-app-for-teams-connect-to-prod_shortmd-on-premises"></a>Maakt de app voor Teams verbinding met [!INCLUDE [prod_short.md](includes/prod_short.md)] on premises? 

Nee. De [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor teams werkt alleen met [!INCLUDE [prod_short.md](includes/prod_short.md)] online. Er zijn geen plannen om [!INCLUDE [prod_short.md](includes/prod_short.md)]-implementatietypen te ondersteunen&mdash;zoals on-premises, hybride cloud of privécloud&mdash;die Microsoft niet rechtstreeks host of beheert.

### <a name="does-the-app-work-with-multiple-companies-and-environments"></a>Werkt de app met meerdere bedrijven en omgevingen? 

Ja. Wanneer de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app een koppeling uitbreidt tot een kaart, moet de koppeling de omgeving en bedrijfsnamen voor de app bevatten om overeen te komen met de record in het juiste bedrijf. U kunt koppelingen plakken naar alle bedrijven en omgevingen waartoe u toegang heeft binnen uw organisatie en vanuit het [!INCLUDE [prod_short.md](includes/prod_short.md)]-account waarmee u zich heeft aangemeld. Deelnemers aan de chat zien de kaart. Maar ze kunnen de kaartgegevens niet bekijken, tenzij ze machtigingen hebben voor het bedrijf of de omgeving waar die record is opgeslagen.

### <a name="in-which-countries-or-regions-is-the-prod_shortmd-app-available"></a>In welke landen of regio's is de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app beschikbaar? 

De [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams is niet beperkt per land of regio. De app is beschikbaar in alle markten die momenteel worden ondersteund door de Teams-marktplaats. 

### <a name="does-the-prod_shortmd-app-work-with-any-localization-of-prod_shortmd"></a>Werkt de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app met elke lokalisatie van [!INCLUDE [prod_short.md](includes/prod_short.md)]? 

Ja. De app is bedoeld om te werken met elke lokalisatie van [!INCLUDE [prod_short.md](includes/prod_short.md)], of die lokalisatie nu rechtstreeks van Microsoft of via een partner wordt aangeboden. Zie voor meer informatie [Beschikbaarheid per land/regio en ondersteunde talen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

### <a name="which-languages-does-the-prod_shortmd-app-support"></a><a name="language"></a>Welke talen ondersteunt de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app?
<!--TODO Run by Mike -->

Twee dingen bepalen de taal die wordt gebruikt voor kaarten en kaartdetails in Teams:

1. Uw taal in Teams, die u kunt zien in uw accountinstellingen in Teams. 
2. Uw taal in [!INCLUDE [prod_short.md](includes/prod_short.md)], die u kunt zien in de [!INCLUDE [prod_short.md](includes/prod_short.md)]-webclient (zie [Basisinstelling wijzigen - taal](ui-change-basic-settings.md#language)).

In de volgende tabel wordt uitgelegd hoe de ervaring verschilt voor berichtauteurs en ontvangers, afhankelijk van de taalinstellingen en de beschikbaarheid van talen.

|Wie|Kaart|Kaartdetails |
|-|----|--------------| 
|Berichtauteur |Wordt weergegeven in de taal die voor u is opgegeven in Teams. Als [!INCLUDE [prod_short.md](includes/prod_short.md)] die taal niet biedt, wordt de kaart weergegeven in het Engels. |Wordt weergegeven in de taal die voor u is opgegeven in [!INCLUDE [prod_short.md](includes/prod_short.md)].  waaronder mogelijk talen van taalapps van partners. |
|Berichtontvanger |Wordt weergegeven in de taal van de auteur van het bericht. |Wordt weergegeven in de taal die voor u is opgegeven in [!INCLUDE [prod_short.md](includes/prod_short.md)]. |

Voor de lijst met ondersteunde talen voor [!INCLUDE [prod_short.md](includes/prod_short.md)] raadpleegt u [Ondersteunde talen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json#supported-languages).

### <a name="where-can-i-find-teams-integration-inside-the-prod_shortmd-web-client"></a>Waar kan ik Teams-integratie vinden in de [!INCLUDE [prod_short.md](includes/prod_short.md)]-webclient? 

Er is momenteel geen insluiting van Teams-besturingselementen of aanwezigheid van Teams-functies in de [!INCLUDE [prod_short.md](includes/prod_short.md)]-webclient of andere clients.  

### <a name="does-prod_shortmd-work-with-the-teams-mobile-app"></a>Werkt [!INCLUDE [prod_short.md](includes/prod_short.md)] met de mobiele Teams-app?

Ja. De [!INCLUDE [prod_short.md](includes/prod_short.md)]-app kan worden geïnstalleerd vanuit de Teams-desktopapp of browser, of door een beheerder voor alle gebruikers. Eenmaal geïnstalleerd is de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app automatisch beschikbaar in Teams voor iOS en Android. Op mobiele apparaten kunt u kaarten bekijken die door anderen zijn verzonden, toegang krijgen tot details of de kaart eruit laten springen voor de volledige ervaring in de mobiele [!INCLUDE [prod_short.md](includes/prod_short.md)]-app. U kunt bij het opstellen van berichten echter geen koppelingen plakken die tot kaarten worden uitgevouwen. Zie voor minimumvereisten voor mobiel [Minimumvereisten voor het gebruik van Business Central](product-requirements.md).

### <a name="is-the-prod_shortmd-app-for-teams-the-same-as-the-prod_shortmd-app-for-ios-and-android"></a>Is de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor teams hetzelfde als de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor iOS en Android? 

Nee. De app voor Teams is een add-in voor Microsoft Teams en is exclusief ontworpen voor samenwerkingservaringen die oplichten binnen Teams. Aan de andere kant biedt de mobiele [!INCLUDE [prod_short.md](includes/prod_short.md)]-app een rijke ervaring voor u om te werken met [!INCLUDE [prod_short.md](includes/prod_short.md)]-gegevens op uw mobiele apparaten.

Mobiele gebruikers worden aangemoedigd om zowel de mobiele app als de app voor Teams te installeren, om maximaal te profiteren van [!INCLUDE [prod_short.md](includes/prod_short.md)]. Als beide zijn geïnstalleerd, kunt u de actie **Nieuw venster** op een kaart in Teams kiezen om de kaartdetails in de mobiele [!INCLUDE [prod_short.md](includes/prod_short.md)]-app te openen. Voor informatie over het installeren van de mobiele [!INCLUDE [prod_short.md](includes/prod_short.md)]- en Teams-app raadpleegt u:

- [Business Central op uw mobiele apparaat krijgen](install-mobile-app.md)
- [De mobiele Teams-app](https://support.microsoft.com/office/download-the-mobile-app-for-teams-5940ebdc-0082-4fb1-83c4-751edc23dcb5) downloaden bij Microsoft-ondersteuning

### <a name="does-the-prod_shortmd-app-work-in-all-teams-clients"></a>Werkt de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app in alle Teams-clients?

Nee. De [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams wordt niet ondersteund als deze is geïnstalleerd als pakket voor macOS of Linux. Op deze platforms kunt u Teams in plaats daarvan openen met een ondersteunde browser.

Voor minimumvereisten in [!INCLUDE [prod_short.md](includes/prod_short.md)] raadpleegt u [Minimumvereisten voor het gebruik van Business Central](product-requirements.md#teams).

Zie voor informatie over de keuze van Teams-clients en hoe u deze kunt installeren [Klanten krijgen voor Microsoft Teams](/microsoftteams/get-clients) in de Teams-documentatie.

### <a name="which-teams-client-is-best-for-prod_shortmd"></a>Welke Teams-client is het beste voor [!INCLUDE [prod_short.md](includes/prod_short.md)]?

Er zijn slechts kleine verschillen en beperkingen tussen Teams-clients die van invloed kunnen zijn op uw ervaring met de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams. Houd bij het kiezen van een Teams-client rekening met het volgende:

- De camera en locatie zijn niet toegankelijk vanuit het detailvenster in de Teams-desktopapp 
- Als u Microsoft Edge met Teams in de browser gebruikt, kunt u gemakkelijk met meerdere identiteiten en accounts werken door vanuit verschillende profielen in te loggen bij Teams. Voor meer informatie over het gebruik van profielen in Microsoft Edge raadpleegt u [Aanmelden en meerdere profielen maken in Microsoft Edge](https://support.microsoft.com/office/sign-in-and-create-multiple-profiles-in-microsoft-edge-df94e622-2061-49ae-ad1d-6f0e43ce6435) bij Microsoft Ondersteuning.

### <a name="what-is-the-best-way-for-me-to-demonstrate-prod_shortmd-and-microsoft-teams-to-prospective-customers"></a>Wat is voor mij de beste manier om [!INCLUDE [prod_short.md](includes/prod_short.md)] en Microsoft Teams te demonstreren aan potentiële klanten?

Als u een doorverkopende partner bent, wilt u misschien een omgeving hebben die u potentiële klanten kunt laten zien als onderdeel van pre-sales demonstraties. Om gevolgen voor Microsoft Teams in uw organisatie te voorkomen kunt u een Microsoft 365-demoaccount krijgen op [https://aka.ms/CDX](https://aka.ms/CDX). Met dit account hebt u volledige controle over een onafhankelijke Azure-organisatie die Microsoft Teams en [!INCLUDE [prod_short.md](includes/prod_short.md)] omvat. Zie voor meer informatie [Demonstratieomgevingen voorbereiden van Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment).

### <a name="does-the-prod_shortmd-app-for-teams-cater-for-my-customization-and-personalization"></a>Voorziet de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams in aanpassing en personalisatie?

De [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams kan kaarten weergeven voor koppelingen naar klantpagina's en tabellen in [!INCLUDE [prod_short.md](includes/prod_short.md)], zoals de pagina's en tabellen die afkomstig zijn van uw eigen aangepaste extensies of van AppSource.

De velden die op een kaart in Teams worden weergegeven, kunnen ook worden beïnvloed door [!INCLUDE [prod_short.md](includes/prod_short.md)]-aanpassingen die voor uw organisatie zijn geïnstalleerd. Kaarten houden geen rekening met rolspecifieke aanpassingen of gebruikerspersonalisatie. Het venster met kaartdetails toont echter de recorddetails zoals u ze zou zien in [!INCLUDE [prod_short.md](includes/prod_short.md)], inclusief eventuele extensies, rolaanpassingen en gebruikerspersonalisatie.

### <a name="where-can-i-learn-about-my-privacy"></a>Waar kan ik meer te weten komen over mijn privacy? 

Hoe Microsoft met uw gegevens omgaat, leest u in de [Privacyverklaring van Microsoft](https://go.microsoft.com/fwlink/?linkid=2030602). 

Neem contact op met uw beheerder voor informatie over hoe uw organisatie omgaat met de privacy van uw gegevens. 

### <a name="how-do-i-uninstall-the-prod_shortmd-app-for-teams"></a>Hoe verwijder ik de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams? 

Om de app te verwijderen die u voor uzelf hebt geïnstalleerd, gaat u naar een chatvak en zoekt u het pictogram [!INCLUDE [prod_short.md](includes/prod_short.md)] onderaan, klikt u met de rechtermuisknop op het pictogram en kiest u Verwijderen.  

### <a name="will-microsoft-continue-to-improve-the-prod_shortmd-app-for-teams"></a>Zal Microsoft de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams blijven verbeteren?

Bij Microsoft luisteren we constant naar feedback van onze zeer uiteenlopende gebruikerscommunity en handelen we naar de beste suggesties. Om te weten wat de toekomst biedt voor de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams raadpleegt u het [Releaseplan voor Dynamics 365](https://aka.ms/dynamics365releaseplan).

Als u wilt deelnemen aan het verbeteren van de app voor Teams, of als u een geweldig idee hebt dat uw werk- of samenwerkingservaringen in Teams zou vereenvoudigen, voeg dan een idee toe of stem op bestaande ideeën op [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## <a name="working-with-cards"></a>[Werken met kaarten](#tab/cards)

### <a name="which-types-of-links-does-the-app-support"></a>Welke soorten koppelingen ondersteunt de app?

De [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams reageert op de meeste [!INCLUDE [prod_short.md](includes/prod_short.md)]-webclientkoppelingen. Als de koppeling verwijst naar een enkele record op een pagina, geeft de kaart velden voor die record weer. De ondersteunde paginatypen zijn: 

- Kaartpagina's, zoals de artikelkaart
- Documentpagina's, zoals het verkooporderdocument
- ListPlus-pagina's die één record vertegenwoordigen die is samengesteld uit andere records, zoals een reconciliatieoverzicht voor een bankrekening
- Eenvoudige lijstpagina's waar een record niet de mogelijkheid biedt om in te zoomen op een afzonderlijke detailpagina, zoals de postcodelijst

Bij het plakken van een koppeling naar de root-URL van de webclient, zoals https://businesscentral.dynamics.com, geeft de kaart in plaats daarvan informatie weer om nieuwe gebruikers op weg te helpen met toegang tot [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="how-do-i-delete-a-card-i-sent-to-a-chat"></a>Hoe verwijder ik een kaart die ik naar een chat heb gestuurd? 

U kunt een kaart die u al naar chat hebt verzonden, niet verwijderen. Maar u kunt het hele bericht waarvan de kaart deel uitmaakt, verwijderen.

Als berichtauteur kunt u alle berichten verwijderen die u naar chats met een persoon, groep of kanaal hebt verzonden&mdash;tenzij uw beheerder beleid heeft ingesteld dat het verwijderen van berichten verhindert. Als u een kanaal modereert als kanaaleigenaar, heeft uw beheerder u mogelijk ook toestemming gegeven om berichten in het kanaal te verwijderen, inclusief berichten die door andere gebruikers zijn verzonden.

Als u een bericht verwijdert dat een kaart bevat, worden de gegevens in [!INCLUDE [prod_short.md](includes/prod_short.md)] niet verwijderd of gewijzigd.

### <a name="do-cards-always-show-up-to-date-information"></a>Bevatten kaarten altijd up-to-date informatie?

Nee. De veldwaarden op een kaart in Teams, inclusief eventuele afbeeldingen, zijn gebaseerd op de gegevens die beschikbaar waren toen die kaart naar de chat werd gestuurd. [!INCLUDE [prod_short.md](includes/prod_short.md)]-kaarten worden niet automatisch vernieuwd in Teams. 

### <a name="will-others-see-my-card-if-they-dont-have-the-prod_shortmd-app-for-teams"></a>Zullen anderen mijn kaart zien als ze de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams niet hebben? 

Wanneer u een chatbericht opstelt en verzendt dat een kaart bevat, zullen alle gebruikers de kaart zien, zelfs als ze de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams niet hebben geïnstalleerd.

## <a name="working-with-card-details"></a>[Werken met kaartgegevens](#tab/carddetails)

### <a name="where-is-the-save-button-in-the-details-window-in-teams"></a>Waar is de knop Opslaan in het detailvenster in Teams? 

[!INCLUDE [prod_short.md](includes/prod_short.md)] slaat automatisch wijzigingen op die u in een veld aanbrengt, zodra u het veld verlaat. Om een veld te verlaten, klikt/tikt u ergens buiten het veld of gebruikt u de Tab-toets om naar het volgende veld te gaan. Als er gegevens verschijnen in een dialoogvenster in het detailvenster, moet u mogelijk de knop **OK** kiezen om [!INCLUDE [prod_short.md](includes/prod_short.md)] uw wijzigingen te laten opslaan.

### <a name="if-i-choose-to-view-details-for-a-card-will-other-users-see-my-details-window"></a>Als ik ervoor kies om details van een kaart te bekijken, zien andere gebruikers dan mijn detailvenster? 

Nee. Hoewel iedereen in de chat de kaart zelf kan zien, verschijnt het detailvenster alleen voor u op uw apparaat wanneer u **Details** kiest. Andere gebruikers moeten **Details** kiezen als ze het detailvenster op hun apparaat willen zien.

### <a name="can-i-start-a-teams-call-from-the-details-window-in-teams"></a>Kan ik een Teams-gesprek starten vanuit het detailvenster in Teams? 

Ja. U kunt een gesprek starten door het gekoppelde nummer te kiezen in een telefoonnummerveld, zoals het veld **Mobiel telefoonnr.** op de kaart **Contact**. Teams moet uw aangewezen belapp zijn.

Als u vanuit Teams lokale of internationale vaste lijnen en mobiele telefoons wilt bellen, moet u een Teams-licentie hebben voor zakelijk bellen. Ook moet u Teams instellen als uw gespreksoplossing. Zie voor meer informatie [Uw Teams-spraakoplossing plannen](/microsoftteams/cloud-voice-landing-page) in de Teams-documentatie.

### <a name="can-i-print-documents-from-the-details-window-in-teams"></a>Kan ik documenten afdrukken vanuit het detailvenster in Teams? 

Ja. U kunt rapporten en andere documenten afdrukken met behulp van standaardafdrukfunctionaliteit van [!INCLUDE [prod_short.md](includes/prod_short.md)] en elke cloud-compatibele printer die is geconfigureerd op de pagina **Printerbeheer** in [!INCLUDE [prod_short.md](includes/prod_short.md)]. U kunt niet vanuit Teams afdrukken naar lokale printers die op uw clientapparaat bekend zijn, zoals printers waarnaar u normaal gesproken vanuit uw browser afdrukt. Om deze reden kunt u niet rechtstreeks vanuit het rapportvoorbeeldvenster afdrukken, maar alleen vanaf de hoofdpagina voor rapportaanvragen, rechtstreeks naar uw cloudprinters.

Zie voor meer informatie over het instellen van cloudprinters [Printers instellen](ui-specify-printer-selection-reports.md).

### <a name="can-i-access-the-camera-from-the-details-window-in-teams"></a>Heb ik toegang tot de camera vanuit het detailvenster in Teams? 

Ja. Alle [!INCLUDE [prod_short.md](includes/prod_short.md)]-functies in het detailvenster die de camera gebruiken, zijn beschikbaar op alle Teams-clients.

### <a name="can-i-access-my-location-from-the-details-window-in-teams"></a><a name="location"></a>Heb ik toegang tot mijn locatie vanuit het detailvenster in Teams?

Als u functionaliteit gebruikt in [!INCLUDE [prod_short.md](includes/prod_short.md)] die toegang heeft tot uw huidige locatiecoördinaten, zoals bij kaarten, moet u Teams in de browser of de mobiele Teams-app gebruiken. Locatie is niet beschikbaar bij gebruik van de Teams-desktop-app. 

## <a name="collaborating-with-guests"></a>[Samenwerken met gasten ](#tab/collaborating)

### <a name="can-i-share-cards-with-users-outside-my-organization"></a>Kan ik kaarten delen met gebruikers buiten mijn organisatie? 

Ja. Wanneer u een bericht opstelt en verzendt dat een kaart bevat, zien alle ontvangers in de chat de kaart&mdash;zelfs als het gasten zijn of buiten uw organisatie. Gasten kunnen ook het detailvenster openen als ze toestemming hebben gekregen voor toegang tot die gegevens in [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="is-the-experience-any-different-for-users-that-are-guests"></a>Is de ervaring anders voor gebruikers die gasten zijn?

Ja. Door gastgebruikers van buiten uw organisatie uit te nodigen om deel te nemen aan chat of een kanaal, krijgen ze een vergelijkbare, maar niet identieke ervaring als gebruikers binnen uw organisatie. Als een gast een bericht ontvangt met een kaart, kan hij of zij dit bekijken. Gasten kunnen ook het detailvenster openen als ze toestemming hebben gekregen voor toegang tot die gegevens in [!INCLUDE [prod_short.md](includes/prod_short.md)] en een [!INCLUDE [prod_short.md](includes/prod_short.md)]-licentie binnen uw organisatie toegewezen hebben gekregen. Als een gast een bericht opstelt, worden koppelingen naar uw [!INCLUDE [prod_short.md](includes/prod_short.md)] niet uitgebreid naar kaarten.

Zie voor meer informatie over overeenkomsten en verschillen tussen gasten en teamleden [Gastervaring in Teams](/MicrosoftTeams/guest-experience) in de Teams-documentatie.

### <a name="how-does-a-guest-user-install-the-prod_shortmd-app"></a>Hoe installeert een gastgebruiker de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app? 

Gasten hebben geen toegang tot de app-marktplaats om zelf apps te installeren. De app kan echter automatisch voor hen worden geïnstalleerd op basis van het beleid van uw organisatie. Een andere manier voor een gastgebruiker om de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app te installeren is wanneer ze een chatbericht ontvangen met een [!INCLUDE [prod_short.md](includes/prod_short.md)]-kaart. In dit geval kiest de gebruiker de knop **Details** of het menu op de kaart en installeert deze vervolgens de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor gebruik met uw organisatie. Na het installeren van de app krijgt een gebruiker niet automatisch toestemming om toegang te krijgen tot gegevens uit uw [!INCLUDE [prod_short.md](includes/prod_short.md)].

<!--TODO - check with Mike on this -->
---

## <a name="see-also"></a>Zie ook

Overzicht van integratie tussen [[!INCLUDE [prod_short](includes/prod_short.md)] en Microsoft Teams](across-teams-overview.md)  
[De [!INCLUDE [prod_short](includes/prod_short.md)]-app installeren voor Microsoft Teams](across-install-app-for-teams.md)  
[Problemen met Teams oplossen](admin-teams-troubleshooting.md)  
[Ontwikkeling voor Teams-integratie](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]