---
title: Veelgestelde vragen over Teams
description: Krijg antwoorden op enkele veelvoorkomende vragen over het werken met Teams en Business Central.
author: jswymer
ms.author: jswymer
ms.topic: faq
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, faq, errors'
ms.date: 09/28/2022
ms.custom: bap-template
---
# <a name="teams-faq"></a>Veelgestelde vragen over Teams

[!INCLUDE [online_only](includes/online_only.md)]

In dit artikel worden enkele van de vragen beantwoord die u mogelijk hebt over het werken met Microsoft Teams en [!INCLUDE [prod_short](includes/prod_short.md)].

## [Algemeen](#tab/general)

### <a name="how-do-i-sign-in-to-the--app-in-teams"></a>Hoe log ik in bij de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app in Teams?

Nadat u de app hebt geïnstalleerd, wordt u gevraagd om in te loggen wanneer u de app voor het eerst gebruikt, wanneer u een [!INCLUDE [prod_short.md](includes/prod_short.md)]-koppeling in Teams-chat plakt of wanneer u de actie **Details** kiest op een kaart in Teams. Afhankelijk van uw Teams-client, moet u mogelijk uw inloggegevens invoeren die u gebruikt om toegang te krijgen tot [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="how-do-i-sign-out-of-the--app-in-teams"></a>Hoe log ik uit bij de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app in Teams?

Om u af te melden bij de identiteit in Teams waarmee u verbinding hebt gemaakt met [!INCLUDE [prod_short.md](includes/prod_short.md)], gaat u naar een willekeurig chatvak, klikt u met de rechtermuisknop op het pictogram [!INCLUDE [prod_short.md](includes/prod_short.md)] eronder en kiest u **Instellingen**. Wanneer het venster verschijnt, controleert u uw momenteel aangemelde identiteit en kiest u vervolgens **Afmelden**.

### <a name="does-the-app-for-teams-connect-to--on-premises"></a>Maakt de app voor Teams verbinding met [!INCLUDE [prod_short.md](includes/prod_short.md)] on premises?

Nee De [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor teams werkt alleen met [!INCLUDE [prod_short.md](includes/prod_short.md)] online. Er zijn geen plannen om [!INCLUDE [prod_short.md](includes/prod_short.md)]-implementatietypen te ondersteunen&mdash;zoals on-premises, hybride cloud of privécloud&mdash;die Microsoft niet rechtstreeks host of beheert.

### <a name="does-the-app-work-with-multiple-companies-and-environments"></a>Werkt de app met meerdere bedrijven en omgevingen?

Ja. Als u contacten in een ander bedrijf wilt zoeken, gaat u naar [Instellingen](across-teams-settings.md). Wanneer de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app een koppeling uitbreidt tot een kaart, moet de koppeling de omgeving en bedrijfsnamen voor de app bevatten om de record te koppelen aan het juiste bedrijf. U kunt koppelingen plakken naar alle bedrijven en omgevingen waartoe u toegang heeft binnen uw organisatie en vanuit het [!INCLUDE [prod_short.md](includes/prod_short.md)]-account waarmee u zich heeft aangemeld. Deelnemers aan de chat zien de kaart. Maar ze kunnen de kaartgegevens niet bekijken, tenzij ze machtigingen hebben voor het bedrijf of de omgeving waar die record is opgeslagen.

### <a name="in-which-countries-or-regions-is-the--app-available"></a>In welke landen of regio's is de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app beschikbaar?

De [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams is niet beperkt per land of regio. De app is beschikbaar in alle markten die momenteel worden ondersteund door de Teams-marktplaats. 

### <a name="does-the--app-work-with-any-localization-of-include-prod_shortmd"></a>Werkt de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app met elke lokalisatie van [!INCLUDE [prod_short.md](includes/prod_short.md)]?

Ja. De app is bedoeld om te werken met elke lokalisatie van [!INCLUDE [prod_short.md](includes/prod_short.md)], of die lokalisatie nu rechtstreeks van Microsoft of via een partner wordt aangeboden. Meer informatie op [Beschikbaarheid in landen/regio's en ondersteunde vertalingen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

### <a name="which-languages-does-the--app-support"></a><a name="language"></a>Welke talen ondersteunt de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app?

Twee dingen bepalen de taal die wordt gebruikt voor kaarten en kaartdetails in Teams:

1. Uw taal in Teams, die u kunt zien in uw accountinstellingen in Teams. 
2. Uw taal in [!INCLUDE [prod_short.md](includes/prod_short.md)], die u kunt zien in de [!INCLUDE [prod_short.md](includes/prod_short.md)]-webclient (zie [Basisinstelling wijzigen - taal](ui-change-basic-settings.md#language)).

In de volgende tabel wordt uitgelegd hoe de ervaring verschilt voor berichtauteurs en ontvangers, afhankelijk van de taalinstellingen en de beschikbaarheid van talen.

|Wie|Kaart|Kaartdetails |
|-|----|--------------| 
|Berichtauteur |Wordt weergegeven in de taal die voor u is opgegeven in Teams. Als [!INCLUDE [prod_short.md](includes/prod_short.md)] die taal niet biedt, wordt de kaart weergegeven in het Engels. |Weergegeven in de taal die voor u is opgegeven in [!INCLUDE [prod_short.md](includes/prod_short.md)], waaronder mogelijk talen uit taal-apps van partners. |
|Berichtontvanger |Wordt weergegeven in de taal van de auteur van het bericht. |Wordt weergegeven in de taal die voor u is opgegeven in [!INCLUDE [prod_short.md](includes/prod_short.md)]. |

Voor de lijst met ondersteunde talen voor [!INCLUDE [prod_short.md](includes/prod_short.md)] raadpleegt u [Ondersteunde talen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json#supported-languages).

### <a name="does-the--app-work-with-industry-solutions"></a>Werkt de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app met brancheoplossingen?

Ja. Maar slechts enkele functies van de app werken met [Apps insluiten](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview).

- De app werkt met koppelingen op basis van het patroon **\*.bc.dynamics.com**, dat doorgaans wordt gebruikt met Apps insluiten.
- Zoeken naar contactpersonen is niet beschikbaar voor Apps insluiten die de basistoepassing van Microsoft vervangen.

### <a name="does--work-with-the-teams-mobile-app"></a>Werkt [!INCLUDE [prod_short.md](includes/prod_short.md)] met de mobiele Teams-app?

Ja. De [!INCLUDE [prod_short.md](includes/prod_short.md)]-app kan worden geïnstalleerd vanuit de Teams-desktopapp of browser, of door een beheerder voor alle gebruikers. Eenmaal geïnstalleerd is de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app automatisch beschikbaar in Teams voor iOS en Android. Op mobiele apparaten kunt u alleen kaarten bekijken die door anderen zijn verzonden, toegang krijgen tot details of de kaart eruit laten springen voor de volledige ervaring in de mobiele [!INCLUDE [prod_short.md](includes/prod_short.md)]-app. U kunt bij het opstellen van berichten of het zoeken naar contacten geen koppelingen plakken die tot kaarten worden uitgevouwen. Meer informatie over minimumvereisten voor mobiel op [Minimumvereisten voor het gebruik van Business Central](product-requirements.md).

### <a name="is-the--app-for-teams-the-same-as-the-include-prod_shortmd-app-for-ios-and-android"></a>Is de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams hetzelfde als de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor iOS en Android?

Nee De app voor Teams is een add-in voor Microsoft Teams en is exclusief ontworpen voor samenwerking binnen Teams. Aan de andere kant biedt de mobiele [!INCLUDE [prod_short.md](includes/prod_short.md)]-app een rijke ervaring voor u om te werken met [!INCLUDE [prod_short.md](includes/prod_short.md)]-gegevens op uw mobiele apparaten.

Mobiele gebruikers worden aangemoedigd om zowel de mobiele app als de app voor Teams te installeren, om maximaal te profiteren van [!INCLUDE [prod_short.md](includes/prod_short.md)]. Als beide zijn geïnstalleerd, kunt u de actie **Nieuw venster** op een kaart in Teams kiezen om de kaartdetails in de mobiele [!INCLUDE [prod_short.md](includes/prod_short.md)]-app te openen. Voor informatie over het installeren van de mobiele [!INCLUDE [prod_short.md](includes/prod_short.md)]- en Teams-app raadpleegt u:

- [Business Central op uw mobiele apparaat krijgen](install-mobile-app.md)
- [De mobiele Teams-app](https://support.microsoft.com/office/download-the-mobile-app-for-teams-5940ebdc-0082-4fb1-83c4-751edc23dcb5) downloaden bij Microsoft-ondersteuning

### <a name="does-the--app-work-in-all-teams-clients"></a>Werkt de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app in alle Teams-clients?

Nee De [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams wordt niet ondersteund als deze is geïnstalleerd als pakket voor macOS of Linux. Op die platforms kunt u Teams in plaats daarvan openen met een ondersteunde browser.

Voor minimumvereisten in [!INCLUDE [prod_short.md](includes/prod_short.md)] raadpleegt u [Minimumvereisten voor het gebruik van Business Central](product-requirements.md#teams).

Als u meer informatie wilt over de keuze van Teams-clients en hoe u deze kunt installeren, raadpleegt u [Klanten krijgen voor Microsoft Teams](/microsoftteams/get-clients) in de Teams-documentatie.

### <a name="which-teams-client-is-best-for-"></a>Welke Teams-client is het beste voor [!INCLUDE [prod_short.md](includes/prod_short.md)]?

Er zijn slechts kleine verschillen en beperkingen tussen Teams-clients die van invloed kunnen zijn op uw ervaring met de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams. Houd bij het kiezen van een Teams-client rekening met het volgende:

- De camera en locatie zijn niet toegankelijk vanuit het detailvenster in de Teams-desktopapp.
- Telefoonnummers kunnen niet worden geactiveerd vanuit het detailvenster in Teams voor iOS, Android of in de browser.
- Als u Microsoft Edge met Teams in de browser gebruikt, kunt u gemakkelijk met meerdere identiteiten en accounts werken door vanuit verschillende profielen in te loggen bij Teams. Voor meer informatie over het gebruik van profielen in Microsoft Edge raadpleegt u [Aanmelden en meerdere profielen maken in Microsoft Edge](https://support.microsoft.com/office/sign-in-and-create-multiple-profiles-in-microsoft-edge-df94e622-2061-49ae-ad1d-6f0e43ce6435) bij Microsoft Ondersteuning.

### <a name="what-is-the-best-way-for-me-to-demonstrate--and-microsoft-teams-to-prospective-customers"></a>Wat is voor mij de beste manier om [!INCLUDE [prod_short.md](includes/prod_short.md)] en Microsoft Teams te demonstreren aan potentiële klanten?

Als u een doorverkopende partner bent, wilt u misschien een omgeving hebben die u potentiële klanten kunt laten zien als onderdeel van pre-sales demonstraties. Om gevolgen voor Microsoft Teams in uw organisatie te voorkomen kunt u een Microsoft 365-demoaccount krijgen op [https://aka.ms/CDX](https://aka.ms/CDX). Met dit account hebt u volledige controle over een onafhankelijke Azure-organisatie die Microsoft Teams en [!INCLUDE [prod_short.md](includes/prod_short.md)] omvat. Zie voor meer informatie [Demonstratieomgevingen voorbereiden van Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment).

### <a name="does-the--app-for-teams-cater-to-my-customization-and-personalization"></a>Voorziet de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams in aanpassing en personalisatie?

De [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams kan kaarten weergeven voor koppelingen naar klantpagina's en tabellen in [!INCLUDE [prod_short.md](includes/prod_short.md)], zoals de pagina's en tabellen die afkomstig zijn van uw eigen aangepaste extensies of van AppSource.

De velden die op een kaart in Teams worden weergegeven, kunnen ook worden beïnvloed door [!INCLUDE [prod_short.md](includes/prod_short.md)]-aanpassingen die voor uw organisatie zijn geïnstalleerd. Kaarten houden geen rekening met rolspecifieke aanpassingen of gebruikerspersonalisatie. Het venster met kaartdetails toont echter de recorddetails zoals u ze zou zien in [!INCLUDE [prod_short.md](includes/prod_short.md)], inclusief extensies, rolaanpassingen en gebruikerspersonalisatie.

Wanneer u contacten zoekt, worden de velden die overeenkomen in de tabel **Contacten** en velden die in de zoekresultaten worden weergegeven, niet beïnvloed door enige aanpassing of personalisatie.

### <a name="how-do-the-permissions-required-by-the-app-affect-my-privacy"></a>Hoe beïnvloeden de machtigingen die vereist zijn door de app mijn privacy?

Voordat u de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams installeert, kunt u de minimale machtigingen bekijken die nodig zijn om de app te laten functioneren. Door de app te installeren, geeft u de app toestemming om de berichten en gegevens te ontvangen die u eraan verstrekt, en geeft u Teams toestemming om die berichten op te slaan en te verwerken.

Ook bepaalde [!INCLUDE [prod_short.md](includes/prod_short.md)]-functies vereisen het openen van externe koppelingen of toegang tot uw camera of geografische locatie. Stel dat u een foto van een aankoopfactuur wilt maken voor verwerking. De [!INCLUDE [prod_short.md](includes/prod_short.md)]-app gebruikt deze mogelijkheden niet zonder uw toestemming en ze worden alleen gebruikt door specifieke functies in het venster **Details**. Wanneer u een van deze functies voor het eerst gebruikt, geeft Teams een dialoogvenster weer waarin u wordt gevraagd toegang te verlenen tot de vereiste apparaatfuncties.

- Op het Teams-bureaublad kunt u app-machtigingen bekijken en aanpassen vanuit het venster **Instellingen**. Selecteer uw profielfoto bovenaan de app en selecteer **Instellingen** > **Machtigingen** en selecteer vervolgens de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app.

- Voor Teams in de browser en Teams voor iOS of Android kunt u machtigingen bekijken of aanpassen vanuit uw browser of apparaatinstellingen.

> [!NOTE]
> Precies welke [!INCLUDE [prod_short.md](includes/prod_short.md)]-functies u om toestemming vragen, is afhankelijk van de add-on-apps en aanpassingen die zijn toegepast op de [!INCLUDE [prod_short.md](includes/prod_short.md)]-omgeving waarmee u verbinding maakt.

### <a name="where-can-i-learn-about-my-privacy"></a>Waar kan ik meer te weten komen over mijn privacy?

Hoe Microsoft met uw gegevens omgaat, leest u in de [Privacyverklaring van Microsoft](https://go.microsoft.com/fwlink/?linkid=2030602). 

Neem contact op met uw beheerder voor informatie over hoe uw organisatie omgaat met de privacy van uw gegevens.

### <a name="how-do-i-uninstall-the--app-for-teams"></a>Hoe verwijder ik de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams?

Om de app te verwijderen die u voor uzelf hebt geïnstalleerd, gaat u naar een chatvak en zoekt u het pictogram [!INCLUDE [prod_short.md](includes/prod_short.md)] onderaan, klikt u met de rechtermuisknop op het pictogram en kiest u **Verwijderen**.  

### <a name="will-microsoft-continue-to-improve-the--app-for-teams"></a>Zal Microsoft de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams blijven verbeteren?

Bij Microsoft luisteren we constant naar feedback van onze zeer uiteenlopende gebruikerscommunity en handelen we naar de beste suggesties. Om te weten wat de toekomst biedt voor de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams raadpleegt u het [Releaseplan voor Dynamics 365](/dynamics365-release-plan/2021wave1/).

Als u wilt deelnemen aan het verbeteren van de app voor Teams, of als u een idee hebt dat uw werk- of samenwerkingservaringen in Teams zou vereenvoudigen, voeg dan een idee toe of stem op bestaande ideeën op [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

### <a name="where-can-i-find-teams-integration-inside-the-business-central-web-client"></a>Waar kan ik Teams-integratie vinden in de Business Central-webclient?

Voor functionaliteit in de webclient die linkt naar Teams, zie [Records en paginakoppelingen delen in Microsoft Teams](across-working-with-teams.md#share-link).

## [Business Central-tabbladen](#tab/tabs)

### <a name="who-can-see-the-content-of-a-tab"></a><a name="who-can-view"></a>Wie kan de inhoud van een tabblad zien?

Elke persoon in uw chat of kanaal die:

1. de Business Central-app voor Teams heeft geïnstalleerd.
2. een Business Central-licentie heeft of toegang heeft tot Business Central met zijn of haar Microsoft 365-licentie.
3. machtigingen heeft om de gegevens op de pagina te bekijken.

### <a name="where-does-the-recommended-content-come-from"></a><a name=#recommended-content></a>Waar komt de aanbevolen inhoud vandaan?

De aanbevolen inhoud waaruit u kunt kiezen in de optie **Tabbladinhoud** op een tabblad is gebaseerd op uw Rolcentrum. De aanbevolen inhoud bevat alleen lijstpagina's, zoals Klanten, Verkooporders en Leveranciers - geen individuele kaartpagina zoals een specifieke klant of leverancier.

De aanbevolen inhoud omvat met name:

- Acties in het bovenste navigatiemenu van het rolcentrum
- Alle lijstpagina's waarvoor u een bladwijzer hebt gemaakt.
- Als een lijstpagina verschillende weergaven biedt, inclusief alle weergaven die u hebt gemaakt, kunt u ook uit die weergaven kiezen

U kunt lijstpagina's toevoegen aan de aanbevolen inhoud door bladwijzers toe te voegen. U kunt aanbevolen inhoud ook verwijderen door bladwijzers te verwijderen. Voor meer informatie over het toevoegen of verwijderen van bladwijzers, zie [Een bladwijzer maken voor een pagina of rapport in uw Rolcentrum](ui-bookmarks.md).

Als u de omgeving of het bedrijf wijzigt op de tabbladoptie, wordt de aanbevolen inhoud gewijzigd op basis van het Rolcentrum en bladwijzers voor de omgeving en het bedrijf waarnaar u overschakelt.

### <a name="when-i-create-a-tab-does-it-grant-permissions-to-the-people-in-the-channel-or-chat"></a>Als ik een tabblad maak, verleent dit dan machtigingen aan de mensen in het kanaal of de chat?

Nee. Het maken van tabbladen heeft geen invloed op de machtigingen en gebruikers moeten al toestemming hebben voor die gegevens wanneer ze het tabblad openen.

### <a name="can-i-chat-alongside-a-tab"></a>Kan ik naast een tabblad chatten?

Ja. Gebruik het chatpictogram om het gesprek te starten. Dit chatgesprek wordt dan gekoppeld aan het tabblad. 

### <a name="if-i-remove-a-tab-from-a-chat-or-channel-is-any-business-central-data-deleted"></a>Als ik een tabblad uit een chat of kanaal verwijder, worden er dan Business Central-gegevens verwijderd?

Nee

### <a name="can-i-safely-rename-a-tab"></a>Kan ik de naam van een tabblad veilig wijzigen?

Ja. De inhoud van het tabblad staat los van de werkelijke naam van het tabblad. Wijzig de naam wanneer u maar wilt! 

### <a name="i-need-to-work-across-tasks-in-different-windows-can-i-do-this"></a>Ik moet verschillende taken in verschillende vensters uitvoeren. Kan dat?

Ja. U kunt het tabblad uitklappen naar een eigen browservenster om de Business Central-webclient weer te geven. 

### <a name="can-i-add-or-pin-tab-in-team-meetings"></a>Kan ik een tabblad toevoegen of vastzetten in Teams-vergaderingen?

Nee De Business Central-app voor Teams ondersteunt geen tabbladen in vergaderingen.

### <a name="cant-add-a-tab-if-using-isv-urls-like-bcdynamicscom-but-can-pin"></a>Kan geen tabblad toevoegen bij gebruik van ISV-URL's, zoals *.bc.dynamics.com (maar kan wel vastzetten)

Niet ondersteund.

### <a name="when-i-do-things-in-the-tab-like-navigate-resort-apply-a-filter-or-search-do-others-see-my-changes"></a>Als ik dingen op het tabblad doe, zoals navigeren, opnieuw sorteren, een filter toepassen of zoeken, zien anderen dan mijn wijzigingen?

Nee Alleen veldwijzigingen of actieve acties beïnvloeden hoe anderen de inhoud van het tabblad zien.

### <a name="does-the-tab-content-refresh-automatically-if-not-how-do-i-refresh-it"></a>Wordt de inhoud van het tabblad automatisch vernieuwd? Zo niet, hoe vernieuw ik het dan?

De inhoud wordt niet automatisch vernieuwd en op dit moment is er geen knop Vernieuwen. De beste manier om de inhoud te vernieuwen om er zeker van te zijn dat deze up-to-date is, is het tabblad sluiten en dan opnieuw openen. 

### <a name="does-this-show-lists-and-records-from-my-customizations-and-add-ons"></a>Worden lijsten en records van mijn aanpassingen en add-ons weergegeven?

Ja. 

### <a name="when-i-add-a-tab-will-people-see-it-in-my-language"></a>Als ik een tabblad toevoeg, zien mensen dit dan in mijn taal?

Nee Elke gebruiker bekijkt de tabbladinhoud in de taal-, regio- en tijdzone-instellingen van Business Central. 

### <a name="can-i-have-multiple-tabs-pointing-to-different-content"></a>Kan ik meerdere tabbladen naar verschillende inhoud laten verwijzen?

Ja.

### <a name="can-i-also-add-tabs-to-chat-with-a-single-person"></a>Kan ik ook tabbladen toevoegen om met één persoon te chatten?

Ja, zolang de chat geen concept is (dat wil zeggen dat er geen bericht is verzonden om die chat te starten) en de andere persoon ook de Business Central-app heeft geïnstalleerd.

### <a name="can-i-switch-companies-within-a-tab"></a>Kan ik binnen een tabblad van bedrijf wisselen?

Nee 

### <a name="is-this-different-than-using-teams-generic-ability-to-create-a-tab-that-hosts-a-website"></a>Is dit anders dan het gebruik van de algemene mogelijkheid van Teams om een tabblad te maken waarop een website wordt gehost?

Ja. We raden het u niet aan om die benadering te kiezen. In veel gevallen werkt het niet voor Business Central.

## [Contacten zoeken](#tab/contacts)

### <a name="which-tables-does-the-app-search-in"></a>In welke tabellen zoekt de app?

Bij het zoeken naar contacten vanuit de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams, worden uw zoektermen vergeleken met records in de tabel **Contacten** in [!INCLUDE [prod_short.md](includes/prod_short.md)]. 

### <a name="which-fields-in-the-contacts-table-can-i-search"></a>Welke velden in de contactentabel kan ik zoeken?

Terwijl u uw zoektermen in het zoekvak typt, worden de termen vergeleken met de meeste velden in de tabel **Contacten**. De velden omvatten bijvoorbeeld de velden **Nee**, **Naam**, **Adres**, **TelefoonNee** of **Mobiel telefoonNee** en **E-mail**. 

Zoektermen komen niet overeen met aangepaste velden die zijn toegevoegd aan de tabel **Contacten** door apps en extensies.

### <a name="do-search-results-include-companies-and-persons"></a>Bevatten zoekresultaten bedrijven en personen?

Ja. In [!INCLUDE [prod_short.md](includes/prod_short.md)] kunnen contacten van het type **Bedrijf** of **Persoon** zijn, waarbij een of meer personen aan een bedrijf kunnen zijn verbonden. In de zoekresultaten hebben bedrijven en personen verschillende pictogrammen.

### <a name="do-contacts-of-any-business-relationship-appear-in-the-results"></a>Komen contacten van een zakelijke relatie in de resultaten voor?

Ja. Sommige contacten vertegenwoordigen mogelijk klanten of leveranciers of beide. Andere contacten zonder gedefinieerde zakelijke relatie vertegenwoordigen doorgaans potentiële klanten. Contacten met andere zakelijke relaties, inclusief eventuele aangepaste relaties die u hebt geconfigureerd in [!INCLUDE [prod_short.md](includes/prod_short.md)], worden ook weergegeven in de zoekresultaten.

### <a name="can-i-look-up-contact-details-during-meetings"></a>Kan ik tijdens vergaderingen contactgegevens opzoeken?

Ja. U kunt contactgegevens, interactiegeschiedenis en gerelateerde documenten voor uw klant of leverancier opzoeken tijdens een Teams-vergadering of bellen terwijl de vergadering plaatsvindt, zonder Teams te verlaten.

U kunt zelfs overal in Teams contactgegevens opzoeken met behulp van het opdrachtvak. U kunt bijvoorbeeld contactgegevens opzoeken in de Teams-agenda om u te helpen bij het opzetten van vergaderingen.

### <a name="how-do-i-view-my-last-interactions-with-a-contact"></a>Hoe bekijk ik mijn laatste interacties met een contact?

In het detailvenster voor een contact worden interactielogboekvermeldingen weergegeven. De interactielogboekvermeldingen geven de geschiedenis weer van interacties die uw organisatie heeft gehad met het specifieke contact. De interacties kunnen bestaan uit e-mails die u hebt uitgewisseld, telefoontjes die u hebt ontvangen of documenten die u hebt verzonden.

Om interacties weer te geven, moet [!INCLUDE [prod_short.md](includes/prod_short.md)] geconfigureerd zijn om interacties bij te houden. Zie voor meer informatie over het loggen van interacties [Interacties met contacten vastleggen](marketing-interactions.md).

### <a name="how-do-i-register-a-teams-call-or-meeting-as-an-interaction"></a>Hoe registreer ik een Teams-gesprek of -vergadering als een interactie?

Zoek in het detailvenster voor een contact de actie **Interactie maken** en kies uit de inkomende of uitgaande oproepen als interactiesjablonen. U kunt ook uw eigen aangepaste interactiesjablonen maken, specifiek voor gebruik met Teams-gesprekken.

### <a name="can-i-call-a-contact-from-the--app-for-teams"></a>Kan ik een contactpersoon bellen vanuit de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams?

[!INCLUDE [prod_short.md](includes/prod_short.md)] heeft een beperkte integratie met de belmogelijkheden van Teams. Het is niet mogelijk om direct een VOIP-gesprek te starten vanuit de contactkaart of het venster met contactgegevens. Wanneer u echter de contactgegevens in de Teams-desktopapp bekijkt, kunt u het telefoonnummerveld selecteren om dat nummer te bellen als Teams is ingesteld als uw standaardbel-app op uw apparaat. Om vaste lijnen of mobiele telefoonnummers te bellen met PSTN, het traditionele telefoonsysteem, heeft Teams de Microsoft 365 Business Voice-app nodig. Zie [Wat is Microsoft 365 Business Voice?](/MicrosoftTeams/business-voice/whats-business-voice) voor meer informatie.

### <a name="how-do-i-view-recent-documents-for-a-customer-or-vendor"></a>Hoe bekijk ik recente documenten voor een klant of leverancier?

[!INCLUDE [prod_short.md](includes/prod_short.md)] relateert een contact doorgaans aan een klant- of leveranciersrecord die op zijn beurt weer gerelateerd is aan zakelijke transactierecords, zoals verkoopoffertes of inkoopfacturen. Om gerelateerde documenten voor een contactpersoon te bekijken, gaat u naar het detailvenster van het contact en kiest u de veldwaarde **Zakenrelatie** of gebruikt u de acties om naar de gekoppelde klant of leverancier te navigeren. Vouw op de klant- of leverancierspagina het feitenblokvenster uit om statistieken weer te geven voor verschillende documenten waarop u kunt inzoomen. Uw ervaring kan verschillen op basis van uw aanpassingen en personalisatie.

### <a name="how-do-i-search-for-contacts-using-special-characters"></a>Hoe zoek ik contacten met speciale tekens?

U kunt zoekcriteria invoeren met bijna alle Unicode-tekens. [!INCLUDE [prod_short.md](includes/prod_short.md)] reserveert echter de volgende symbolen voor ander gebruik: **=**, **.**, **\*** en **@**. Als u deze symbolen in uw zoektermen gebruikt, levert dit mogelijk niet de verwachte resultaten op. Als u de verwachte resultaten niet ziet, plaatst u de symbolen in uw zoektermen tussen enkele aanhalingstekens, bijvoorbeeld **Contoso'='2**.

### <a name="how-can-i-search-contacts-stored-in-a-different-company"></a>Hoe kan ik zoeken naar contacten die in een ander bedrijf zijn opgeslagen?

De [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams kan zoeken naar klanten, leveranciers en andere contacten in één bedrijf tegelijk.  
Om contacten te zoeken die zijn opgeslagen in een ander [!INCLUDE [prod_short.md](includes/prod_short.md)]-bedrijf, opent u [Instellingen](across-teams-settings.md) en verandert u de omgeving en het bedrijf van daaruit.

### <a name="are--contacts-different-than-the-ones-in-the-teams-contacts-screen"></a>Zijn [!INCLUDE [prod_short.md](includes/prod_short.md)]-contacten anders dan de contacten in het Teams-contactenscherm?

Ja. Contacten die zijn opgeslagen in [!INCLUDE [prod_short.md](includes/prod_short.md)], vertegenwoordigen zakelijke contacten die beschikbaar zijn voor uw organisatie. Het zijn contacten waarmee u een gevestigde en goed gedefinieerde zakelijke relatie hebt, of contacten die potentiële klanten vertegenwoordigen. Deze contacten zijn doorgaans externe contacten. Ter vergelijking: de contacten die in de lijst Contacten bellen van Teams worden weergegeven, zijn uw eigen contacten. Deze contacten worden niet noodzakelijkerwijs gedeeld met anderen in uw organisatie en vertegenwoordigen doorgaans interne contacten binnen uw organisatie.

### <a name="does--synchronize-contacts-with-teams"></a>Synchroniseert [!INCLUDE [prod_short.md](includes/prod_short.md)] contacten met Teams?

Nee. Contacten die zijn opgeslagen in [!INCLUDE [prod_short.md](includes/prod_short.md)], blijven gescheiden van uw contacten die zijn opgeslagen in Teams.
Er zijn momenteel geen plannen om de twee lijsten samen te synchroniseren.

### <a name="what-is-the-minimum-version-of--for-contact-search"></a>Wat is de minimumversie van [!INCLUDE [prod_short.md](includes/prod_short.md)] voor contacten zoeken?

Voor het zoeken naar contacten moet u de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams versie 1.0.4 of hoger hebben geïnstalleerd en u maakt verbinding met [!INCLUDE [prod_short.md](includes/prod_short.md)]-omgevingen van versie 18 of hoger.

### <a name="can-i-search-from-my-mobile-device"></a>Kan ik zoeken vanaf mijn mobiele apparaat?

Zoeken naar contacten is momenteel niet beschikbaar vanuit Teams voor iOS en Teams voor Android.

### <a name="which-permissions-do-i-need-for-contact-search"></a>Welke machtigingen heb ik nodig om contacten te zoeken?

Als u contacten wilt zoeken, hebt u machtiging op objectniveau nodig voor de tabel **Contacten** binnen het [!INCLUDE [prod_short.md](includes/prod_short.md)]-bedrijf dat wordt doorzocht. Om het detailvenster van een contact te bekijken, heeft u ten minste leestoestemming nodig voor de pagina **Contact** binnen het [!INCLUDE [prod_short.md](includes/prod_short.md)]-bedrijf en andere gerelateerde objecten.

### <a name="can-i-use-contact-search-if-im-a-delegated-admin"></a>Kan ik contacten zoeken gebruiken als ik een gedelegeerde beheerder ben?

Ja. U kunt ook contacten en contactgegevens opzoeken als u een gedelegeerde beheerdersrol heeft in een organisatie.

### <a name="is-contact-search-affected-by-api-limits"></a>Wordt het zoeken naar contacten beïnvloed door API-limieten?

Ja. Zoeken naar contacten vanuit Teams is gebaseerd op [!INCLUDE [prod_short.md](includes/prod_short.md)] v2.0-API's en onderhevig aan eventuele API-limieten die het gebruik beheren. U kunt meer lezen over de limieten op [Huidige API-limieten](/dynamics-nav/api-reference/v2.0/dynamics-current-limits).

### <a name="why-does-it-sometimes-ask-me-to-set-up-the-app"></a>Waarom word ik soms gevraagd om de app in te stellen?

Nadat u zich voor de eerste keer hebt aangemeld bij de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams, zal de app proberen uw voorkeursbedrijf te bepalen in [!INCLUDE [prod_short.md](includes/prod_short.md)]. Als de app het bedrijf niet kan bepalen, moet u mogelijk naar de **Instellingen** gaan en het bedrijf kiezen waarin u wilt zoeken. Deze situatie doet zich bijvoorbeeld voor als u toegang heeft tot meerdere bedrijven in verschillende omgevingen in uw organisatie. In dat geval moet u een bedrijf kiezen voordat u kunt gaan zoeken.  

De app kan u ook vragen naar **Instellingen** te gaan als u geen [!INCLUDE [prod_short.md](includes/prod_short.md)]-abonnement hebt, zijn er geen [!INCLUDE [prod_short.md](includes/prod_short.md)]-omgevingen of als uw account geen [!INCLUDE [prod_short.md](includes/prod_short.md)]-licentie heeft.

### <a name="id-like-to-search-for-items-or-records-from-other-tables-can-i-do-this-from-teams"></a>Ik zou graag willen zoeken naar items of records uit andere tabellen. Kan ik dit vanuit Teams doen?

Zoeken in andere tabellen is op dit moment niet mogelijk. De [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams zoekt alleen in de [!INCLUDE [prod_short.md](includes/prod_short.md)]-contactenlijst, die leveranciers, klanten en andere contacten kan bevatten.

Als u wilt dat de zoekmogelijkheden evolueren en andere tabellen gaan omvatten, moedigen we onze gemeenschap aan om een idee toe te voegen of op bestaande ideeën te stemmen op https://aka.ms/BusinessCentralIdeas.

## [Werken met kaarten](#tab/cards)

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

### <a name="why-dont-cards-show-more-information-instead-of-just-the-page-name-and-details-button"></a>Waarom tonen kaarten niet meer informatie dan de paginanaam en de detailknop?

Een beheerder heeft mogelijk de Teams-integratie zo geconfigureerd dat kaarten geen gegevens over records tonen. Raadpleeg voor meer informatie [Recordgegevens op kaarten weergeven of verbergen](admin-teams-integration.md#show-or-hide-record-data-on-cards).

### <a name="will-others-see-my-card-if-they-dont-have-the--app-for-teams"></a>Zullen anderen mijn kaart zien als ze de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams niet hebben?

Wanneer u een chatbericht opstelt en verzendt dat een kaart bevat, zullen alle gebruikers de kaart zien&mdash;zelfs als ze de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams niet hebben geïnstalleerd.

### <a name="how-do-i-find-out-which-company-a-card-in-teams-belongs-to"></a>Hoe kom ik erachter tot welk bedrijf een kaart in Teams behoort?

Als u in meerdere [!INCLUDE [prod_short.md](includes/prod_short.md)]-bedrijven werkt, overleg dan met uw beheerder over het inschakelen van een bedrijfsbadge voor elk bedrijf. Indien ingeschakeld, verschijnt deze in het oog springende hint in elk detailvenster in Teams en toont het bedrijf en de omgeving waartoe de record behoort. Voor meer informatie over het instellen van een bedrijfsbadge zie [Een bedrijfsbadge weergeven](admin-company-information.md#badge).

## [Werken met kaartgegevens](#tab/carddetails)

### <a name="where-is-the-save-button-in-the-details-window-in-teams"></a>Waar is de knop Opslaan in het detailvenster in Teams?

[!INCLUDE [prod_short.md](includes/prod_short.md)] slaat automatisch wijzigingen op die u in een veld aanbrengt, zodra u het veld verlaat. Om een veld te verlaten, klikt/tikt u ergens buiten het veld of gebruikt u de Tab-toets om naar het volgende veld te gaan. Als er gegevens verschijnen in een dialoogvenster in het detailvenster, moet u mogelijk de knop **OK** kiezen om [!INCLUDE [prod_short.md](includes/prod_short.md)] uw wijzigingen te laten opslaan.

### <a name="if-i-choose-to-view-details-for-a-card-will-other-users-see-my-details-window"></a>Als ik ervoor kies om details van een kaart te bekijken, zien andere gebruikers dan mijn detailvenster?

Nee. Hoewel iedereen in de chat of vergadering de kaart zelf kan zien, verschijnt het detailvenster alleen voor u op uw apparaat wanneer u **Details** kiest. Andere gebruikers moeten **Details** kiezen als ze het detailvenster op hun apparaat willen zien.

### <a name="can-i-start-a-teams-call-from-the-details-window-in-teams"></a>Kan ik een Teams-gesprek starten vanuit het detailvenster in Teams?

Ja. Als u de Teams-desktopapp gebruikt, start u een gesprek door het gekoppelde nummer te kiezen in een telefoonnummerveld, zoals het veld **Mobiel telefoonNee** op de kaart **Contact**. Teams moet uw aangewezen belapp zijn.

Als u vanuit Teams lokale of internationale vaste lijnen en mobiele telefoons wilt bellen, vereist Teams dat u een Business Voice-licentie hebt voor zakelijk bellen. Ook moet u Teams instellen als uw gespreksoplossing. Zie voor meer informatie [Uw Teams-spraakoplossing plannen](/microsoftteams/cloud-voice-landing-page) in de Teams-documentatie.

### <a name="can-i-print-documents-from-the-details-window-in-teams"></a>Kan ik documenten afdrukken vanuit het detailvenster in Teams?

Ja. U kunt rapporten en andere documenten afdrukken met behulp van standaardafdrukfunctionaliteit van [!INCLUDE [prod_short.md](includes/prod_short.md)] en elke cloud-compatibele printer die is geconfigureerd op de pagina **Printerbeheer** in [!INCLUDE [prod_short.md](includes/prod_short.md)]. U kunt niet vanuit Teams afdrukken naar lokale printers die op uw clientapparaat bekend zijn, zoals printers waarnaar u normaal gesproken vanuit uw browser afdrukt. Om deze reden kunt u niet rechtstreeks vanuit het rapportvoorbeeldvenster afdrukken, maar alleen vanaf de hoofdpagina voor rapportaanvragen, rechtstreeks naar uw cloudprinters.

Zie voor meer informatie over het instellen van cloudprinters [Printers instellen](ui-specify-printer-selection-reports.md).

### <a name="can-i-access-the-camera-from-the-details-window-in-teams"></a>Heb ik toegang tot de camera vanuit het detailvenster in Teams?

Ja. Alle [!INCLUDE [prod_short.md](includes/prod_short.md)]-functies in het detailvenster die de camera gebruiken, zijn beschikbaar op alle Teams-clients.

### <a name="can-i-access-my-location-from-the-details-window-in-teams"></a><a name="location"></a>Heb ik toegang tot mijn locatie vanuit het detailvenster in Teams?

Als u functionaliteit gebruikt in [!INCLUDE [prod_short.md](includes/prod_short.md)] die toegang heeft tot uw huidige locatiecoördinaten, zoals bij kaarten, moet u Teams in de browser of de mobiele Teams-app gebruiken. Locatie is niet beschikbaar bij gebruik van de Teams-desktop-app.

### <a name="how-do-i-open-the-details-in-a-new-window"></a>Hoe open ik de details in een nieuw venster?

Het uitklappen van het detailvenster als apart venster is handig voor multitasking of om met bedrijfsgegevens te kunnen werken terwijl u Teams-chat en andere Teams-functies gebruikt. Als u details in een eigen venster wilt openen, kiest u **Openen in browser** in het menu met het beletselteken (**...**) in de rechterbovenhoek van het venster.

## [Samenwerken met gasten](#tab/collaborating)

### <a name="can-i-share-cards-with-users-outside-my-organization"></a>Kan ik kaarten delen met gebruikers buiten mijn organisatie?

Ja. Wanneer u een bericht opstelt en verzendt dat een kaart bevat, zien alle ontvangers in de chat de kaart&mdash;zelfs als het gasten zijn of buiten uw organisatie. Gasten kunnen ook het detailvenster openen als ze toestemming hebben gekregen voor toegang tot die gegevens in [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="is-the-experience-any-different-for-users-that-are-guests"></a>Is de ervaring anders voor gebruikers die gasten zijn?

Ja. Door gastgebruikers van buiten uw organisatie uit te nodigen om deel te nemen aan chat of een kanaal, krijgen ze een vergelijkbare, maar niet identieke ervaring als gebruikers binnen uw organisatie. Als een gast een bericht ontvangt met een kaart, kan hij of zij dit bekijken. Gasten kunnen ook de detailpagina openen als ze toestemming hebben voor toegang tot die gegevens in [!INCLUDE [prod_short.md](includes/prod_short.md)] en een [!INCLUDE [prod_short.md](includes/prod_short.md)]-licentie binnen uw organisatie toegewezen hebben gekregen.

Als u de detaillink op een Business Central-kaart kiest, wordt u aangemeld bij de omgeving van waaruit de kaart is gedeeld, ervan uitgaande dat u toestemming hebt voor de omgeving.

Gastgebruikers mogen geen contact zoeken, omdat dit gebonden is aan de oorspronkelijke tenant en we een dergelijk gedelegeerd scenario momenteel niet ondersteunen.

Als een gast een bericht opstelt, worden koppelingen naar hun [!INCLUDE [prod_short.md](includes/prod_short.md)] of de uwe niet uitgebreid naar kaarten.

Zie voor meer informatie over overeenkomsten en verschillen tussen gasten en teamleden [Gastervaring in Teams](/MicrosoftTeams/guest-experience) in de Teams-documentatie.

### <a name="how-does-a-guest-user-install-the--app"></a>Hoe installeert een gastgebruiker de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app?

Gasten hebben geen toegang tot de app-marktplaats om zelf apps te installeren. De app kan echter automatisch voor hen worden geïnstalleerd op basis van het beleid van uw organisatie. Een andere manier voor een gastgebruiker om de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app te installeren is wanneer ze een chatbericht ontvangen met een [!INCLUDE [prod_short.md](includes/prod_short.md)]-kaart. In dit geval kiest de gebruiker de knop **Details** of het menu op de kaart en installeert deze vervolgens de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor gebruik met uw organisatie. Na het installeren van de app krijgt een gebruiker niet automatisch toestemming om toegang te krijgen tot gegevens uit uw [!INCLUDE [prod_short.md](includes/prod_short.md)].

## [Delen met Teams](#tab/share)

### <a name="does-share-to-teams-send-a-compact-card"></a>Verstuurt Delen met Teams een compacte kaart?

Ja. De link wordt automatisch uitgevouwen tot een kaart als u de Business Central-app voor Teams hebt geïnstalleerd. 

### <a name="will-recipients-receive-the-message-from-me-or-from-a-business-central-service-account"></a>Ontvangen ontvangers het bericht van mij of van een Business Central-serviceaccount?

Wanneer u Delen met Teams gebruikt, wordt het bericht naar een persoon, groep of kanaal verzonden, alsof u het bericht zelf vanuit Microsoft Teams hebt verzonden. Ontvangers zien het bericht van u op hun favoriete Teams-client en kunnen reageren en antwoorden zoals ze normaal zouden doen op een bericht van u. 

### <a name="is-share-to-teams-available-in-business-central-on-premises"></a>Is Delen met Teams beschikbaar in Business Central on premises?

Nee. Net als bij de [!INCLUDE [prod_short.md](includes/prod_short.md)]-app voor Teams is deze functie alleen beschikbaar voor de webclient in [!INCLUDE [prod_short.md](includes/prod_short.md)] online. Er zijn geen plannen om [!INCLUDE [prod_short.md](includes/prod_short.md)]-implementatietypen te ondersteunen&mdash;zoals on-premises, hybride cloud of privécloud&mdash;die Microsoft niet rechtstreeks host of beheert.

### <a name="does-share-to-teams-grant-permissions-to-recipients"></a>Verleent Delen met Teams machtigingen aan ontvangers?

Nee. Wanneer u deelt met een persoon, groep of kanaal, worden de machtigingen niet beïnvloed. Gebruikers die al gemachtigd zijn om de pagina en de door de koppeling getargete gegevens te bekijken, kunnen dit doen. Gebruikers die geen toestemming hebben om die pagina en gegevens te bekijken, of geen [!INCLUDE [prod_short.md](includes/prod_short.md)]-licentie hebben, krijgen een foutmelding te zien. 
 
### <a name="must-i-have-the-teams-desktop-app-installed-to-use-share-to-teams"></a>Moet ik de Teams desktop-app hebben geïnstalleerd om Delen met Teams te kunnen gebruiken?

Nee. Het enige wat u nodig hebt, is een geldig account dat toegang heeft tot Microsoft Teams. 

### <a name="is-share-to-teams-available-in-all-business-central-clients"></a>Is Delen met Teams beschikbaar in alle Business Central-clients?

Op dit moment is Delen met Teams beschikbaar in de desktop-webclient, in het detailvenster in Teams en bij het openen van een pagina in een nieuw venster vanuit de Outlook-invoegtoepassing.

### <a name="where-do-i-find-share-to-teams-in-business-central"></a>Waar vind ik Delen met teams in Business Central?

De actie **Delen met teams** is te vinden in het menu **Delen** op alle pagina's, zoals kaart- en documentpagina's, lijst- of werkbladpagina's, inclusief aangepaste pagina's. De actie is niet beschikbaar in dialoogvensters of pagina's die worden weergegeven als dialoogvensters, zoals opzoekpagina's of wizards.

---
## <a name="see-also"></a>Zie ook

Overzicht van integratie tussen [[!INCLUDE [prod_short](includes/prod_short.md)] en Microsoft Teams](across-teams-overview.md)  
[De [!INCLUDE [prod_short](includes/prod_short.md)]-app installeren voor Microsoft Teams](across-install-app-for-teams.md)  
[Zoeken naar klanten, leveranciers en andere contacten vanuit Microsoft Teams](across-search-contacts-teams.md)  
[Records delen in Microsoft Teams](across-working-with-teams.md)  
[Problemen met Teams oplossen](admin-teams-troubleshooting.md)  
[Bedrijfs- en andere instellingen in Teams wijzigen](across-teams-settings.md)  
[Ontwikkeling voor Teams-integratie](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
