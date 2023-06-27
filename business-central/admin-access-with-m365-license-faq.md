---
title: Veelgestelde vragen over toegang met Microsoft 365-licenties
description: Krijg antwoorden op veelgestelde vragen over toegang tot Business Central met Microsoft 365-licenties.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: faq
ms.date: 11/22/2022
ms.custom: bap-template
---
# <a name="access-with-microsoft-365-licenses-faq"></a>Veelgestelde vragen over toegang met Microsoft 365-licenties

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Gebruikers hebben toegang tot Business Central-gegevens in Microsoft Teams met hun Microsoft 365-licentie. Dit artikel beantwoordt veelgestelde vragen van bestuurders, adviseurs en anderen. Ontwikkelaars dienen de veelgestelde vragen voor ontwikkelaars te raadplegen. Ga voor vragen over het integreren van Business Central met Microsoft Teams naar [Veelgestelde vragen over Teams](teams-faq.md).

## [Machtigingen](#tab/permissions) 

### <a name="can-i-proactively-configure-different-starting-permissions-for-different-groups-of-users"></a>Kan ik proactief verschillende startmachtigingen configureren voor verschillende groepen gebruikers?

Niet op dit moment. Met Business Central kan slechts één groep machtigingen worden geconfigureerd die aan alle Microsoft 365-gebruikers wordt toegewezen wanneer ze zich voor het eerst aanmelden bij Business Central.

### <a name="can-i-proactively-configure-permissions-profiles-and-settings-for-individual-users-before-they-sign-in"></a>Kan ik proactief machtigingen, profielen en instellingen configureren voor individuele gebruikers voordat ze inloggen?

Ja. Dit kan worden bereikt via beveiligingsgroepen. Door een beveiligingsgroep toe te passen op een omgeving definieert u de totale set gebruikers die toegang hebben tot die omgeving. Deze beveiligingsgroep kan gebruikers met een Business Central-licentie en gebruikers met een Microsoft 365-licentie bevatten. Wanneer u de volgende keer gebruikers bijwerkt vanuit Microsoft 365 in de lijst **Gebruikers**, worden de Microsoft 365-gebruikersrecords gemaakt. U kunt vervolgens gebruikersgroepen, machtigingen, profielen en andere instellingen toewijzen voordat ze zich hebben aangemeld.

### <a name="after-a-user-signs-in-can-i-change-which-objects-they-have-access-to"></a>Kan ik nadat een gebruiker zich heeft aangemeld, wijzigen tot welke objecten ze toegang hebben?

Ja. Nadat een gebruiker zich voor de eerste keer heeft aangemeld en zijn of haar gebruikersrecord is ingericht, beheren beheerders die gebruikers net als elke andere Business Central-gebruiker. Ze kunnen bijvoorbeeld machtigingen voor verschillende objecten toevoegen of verwijderen. Als u de machtigingensets wijzigt die zijn toegewezen aan de Microsoft 365-licentie op de pagina Licentieconfiguratie, heeft de wijziging alleen invloed op de volgende gebruikers die zich voor de eerste keer aanmelden.

### <a name="how-do-i-prevent-access-to-sensitive-tables"></a>Hoe voorkom ik toegang tot gevoelige tabellen?

Business Central biedt een krachtig en flexibel machtigingsmodel waarbij beheerders machtigingensets kunnen definiëren die toegang verlenen tot specifieke objecten, bedrijfsprocessen of volledige rollen. Om toegang tot gevoelige tabellen te voorkomen, kunt u aangepaste machtigingensets maken die machtigingen voor gevoelige objecten uitsluiten. Zie [Een machtigingenset maken](ui-define-granular-permissions.md) voor meer informatie over het uitsluiten van machtigingen.  

### <a name="instead-of-customizing-the-license-configuration-can-i-customize-a-user-group"></a>Kan ik een gebruikersgroep aanpassen in plaats van de licentieconfiguratie aan te passen?

Ja. Het toevoegen van machtigingensets aan de Microsoft Teams-gebruikersgroep Interne gebruikers in Business Central heeft hetzelfde netto-effect als het toevoegen van machtigingensets aan de Microsoft 365-licentie, zo lang de Microsoft 365-licentie blijft toegewezen aan deze gebruikersgroep. Deze aanpak heeft als bijkomend voordeel dat machtigingensets altijd worden gesynchroniseerd met leden van de groep wanneer u de gebruikersgroep wijzigt.

### <a name="when-a-business-central-user-shares-a-record-in-teams-do-they-grant-new-permissions"></a>Wanneer Business Central-gebruikers een record delen in Teams, verlenen ze dan nieuwe machtigingen?

Nr. Deze actie is niet hetzelfde als het delen van een link naar een SharePoint-document waarbij de persoon die het document deelt kan kiezen om anderen toestemming te geven. In Business Central kunnen alleen beheerders machtigingen configureren en toewijzen. In vergelijking met SharePoint-documenten delen is dit het equivalent van het kiezen van de optie "Delen met personen met bestaande toegang".

### <a name="does-this-feature-support-row-level-security"></a>Ondersteunt deze functie beveiliging op rijniveau?

Ja. Hoewel een persoon die toegang heeft tot een record in Teams met zijn of haar Microsoft 365-licentie mogelijk de juiste machtigingen voor tabellen en paginaobjecten heeft, worden machtigingen op rijniveau afgedwongen als dit voor die tabel is geïmplementeerd.  

### <a name="if-i-configure-permissions-that-include-write-access-will-users-be-able-to-write-in-teams"></a>Als ik machtigingen configureer die schrijftoegang bevatten, kunnen gebruikers dan in Teams schrijven?

Als u Business Central configureert om een machtigingenset toe te wijzen die invoeg-, wijzig- of verwijdertoegang tot een of meer objecten omvat, kunnen gebruikers met die machtigingenset toch niet in Teams schrijven als ze alleen een Microsoft 365-licentie hebben. De Business Central-service dwingt alleen-lezen toegang af, ongeacht de machtiging voor invoegen, wijzigen of verwijderen die u toewijst.  

Hoewel Business Central dit beveiligingsniveau biedt, raden we toch aan om machtigingensets met schrijftoegang te vermijden. Dit voorkomt problemen verder stroomafwaarts wanneer gebruikers van rol veranderen of nieuwe licenties verwerven.  

## [Instelling en configuratie](#tab/setup)

### <a name="why-is-the-setting-to-enable-access-not-available-for-my-environment"></a>Waarom is de instelling om toegang in te schakelen niet beschikbaar voor mijn omgeving?

Toegang inschakelen met Microsoft 365-licenties is alleen beschikbaar voor Business Central-omgevingen van platformversie 21.1 of hoger. Wanneer uw omgeving wordt geüpgraded naar deze minimale versie, komt de instelling automatisch beschikbaar. Om de versie van uw omgeving te controleren gaat u naar de pagina met omgevingsdetails voor de omgeving in het Business Central-beheercentrum. Of log in bij de omgeving en ga naar de pagina **Help en ondersteuning** vanuit het menu **Help**.

### <a name="can-i-access-business-central-on-premises-with-microsoft-365-licenses"></a>Kan ik toegang tot Business Central krijgen met Microsoft 365-licenties?

Nee, dat wordt niet ondersteund. Business Central geeft een foutmelding weer wanneer gebruikers toegang proberen te krijgen tot Business Central on premises-records in Teams.

### <a name="what-is-the-employee-profile"></a>Wat is het werknemersprofiel?

Het profiel **Werknemer** dat wordt weergegeven op de lijstpagina **Profielen (rollen)** is geïntroduceerd met update 21.1. Dit is het standaardprofiel dat wordt toegewezen aan gebruikers die toegang tot Business Central hebben met hun Microsoft 365-licentie. Dit profiel is bedoeld voor mensen in een organisatie die geen specifieke rol hebben in Business Central en alleen gegevens hoeven te bekijken die met hen zijn gedeeld.

### <a name="what-is-the-teams-users-user-group"></a>Wat is de gebruikersgroep Teams-gebruikers?

De groep **Interne Microsoft Teams-gebruikers** die wordt weergegeven op de pagina **Gebruikersgroepen**, is geïntroduceerd met update 21.1. Deze groep is de standaardgebruikersgroep die wordt toegewezen aan gebruikers die toegang tot Business Central hebben met hun Microsoft 365-licentie. De gebruikersgroep is bedoeld voor mensen binnen dezelfde organisatie waarin Business Central wordt gehost, die samenwerken in Microsoft Teams.  

### <a name="do-users-that-only-have-a-microsoft-365-license-show-up-in-the-users-list-in-business-central"></a>Worden gebruikers die alleen een Microsoft 365-licentie hebben, weergegeven in de gebruikerslijst in Business Central?

Ja. Als u beveiligingsgroepen toepast op omgevingen, worden die gebruikers weergegeven in de lijst Gebruikers nadat u de actie Gebruikers bijwerken hebt gebruikt vanuit de lijst **Gebruikers** van Microsoft 365. Als u geen beveiligingsgroepen toepast, verschijnen gebruikersrecords in de lijst Gebruikers nadat ze voor het eerst toegang hebben tot een Business Central-record.

### <a name="does-this-feature-work-for-embed-isv-solutions"></a>Werkt deze functie voor ingesloten ISV-oplossingen?

Ja. Gebruikers met alleen een Microsoft 365-licentie hebben ook toegang tot records in omgevingen die draaien onder het domein *.bc.dynamics.com.

## [Licenties](#tab/license)

### <a name="can-a-customer-use-this-feature-if-they-dont-have-business-central"></a>Kan een klant deze functie gebruiken als deze geen Business Central heeft?

Toegang tot Business Central met een Microsoft 365-licentie is bedoeld voor organisaties die al geabonneerd zijn op Business Central en een of meer Business Central-omgevingen gebruiken of beheren met gelicentieerde Business Central-gebruikers. Het biedt geen nieuwe functionaliteit of gebruiksrechten voor Microsoft 365-klanten die geen Business Central-abonnement hebben.

### <a name="how-does-this-help-me-manage-subscription-costs-in-my-organization"></a>Hoe helpt dit mij om de abonnementskosten in mijn organisatie te beheren?

Om de productiviteit te maximaliseren en hun activiteiten te stroomlijnen, kopen MKB's vaak Microsoft 365 samen met Dynamics 365 Business Central . In dat geval krijgen de meeste mensen een Microsoft 365-licentie, maar krijgen alleen specifieke rollen of mensen een Business Central-licentie. Business Central biedt licentieflexibiliteit zodat klanten alleen betalen voor wat ze nodig hebben:

- Gebruikers die volledige toegang tot Business Central nodig hebben, krijgen doorgaans een Business Central Essentials- of Business Central Premium-licentie toegewezen. 
- Gebruikers die beperkte schrijftoegang nodig hebben, krijgen doorgaans een Business Central Teamlid-licentie toegewezen.
- Alle andere medewerkers in de hele organisatie die slechts af en toe zakelijke gegevens hoeven te lezen die met hen worden gedeeld, kunnen dit doen als ze een Microsoft 365-licentie hebben. Ze hoeven geen Teamlid-licentie toegewezen te krijgen. Er zijn andere licentieopties beschikbaar. Download en lees voor meer informatie de [Dynamics 365-licentiehandleiding](https://go.microsoft.com/fwlink/?LinkId=866544).

### <a name="is-this-100-free-of-charge"></a>Is dit 100% gratis?
 
Nr. Voor toegang tot Business Central-gegevens in Microsoft Teams moet elke gebruiker een Business Central-licentie of een Microsoft 365-licentie uit de lijst met ondersteunde abonnementen hebben.

### <a name="does-this-work-with-microsoft-365-trials-and-business-central-trials"></a>Werkt dit met Microsoft 365-proefversies en Business Central-proefversies?

Ja. Als een gebruiker een Microsoft 365-licentie vanuit een proefversie van een ondersteund abonnement krijgt toegewezen, heeft deze ook toegang tot Business Central-records in Teams. Het is dan mogelijk voor klanten om de samenwerking tussen Microsoft-productiviteit en zakelijke apps uit te proberen, en verkopers en consultants van partners kunnen deze functie eenvoudig demonstreren. Partners kunnen bijvoorbeeld hun eigen Azure AD-tenants voorzien vanuit [https://aka.ms/CDX](https://aka.ms/CDX), waaronder Microsoft 365-proefversies en Business Central-proefversies voor het demonstreren van Business Central.

### <a name="the-list-of-licenses-in-business-central-shows-a-microsoft-365-license-whats-that"></a>De lijst met licenties in Business Central toont een Microsoft 365-licentie. Wat is dat?

Op de pagina **Licentieconfiguratie** in Business Central worden de verschillende soorten licenties weergegeven die toegang kunnen bieden tot de Business Central-service. In versie 21 heeft Microsoft Microsoft 365 aan deze lijst toegevoegd als een nieuwe manier om toegang te krijgen tot Business Central. Deze lijst met licenties impliceert niet dat uw organisatie abonnementen op een van deze licenties heeft gekocht of dat uw organisatie toegang via die licenties heeft ingeschakeld.

### <a name="do-i-need-to-acquire-a-new-type-of-microsoft-365-license-for-this-feature-to-work"></a>Moet ik een nieuw type Microsoft 365-licentie aanschaffen om deze functie te laten werken?

Microsoft heeft geen nieuwe licenties of nieuwe plannen gemaakt om deze functie mogelijk te maken. Deze functie is volledig afhankelijk van bestaande Microsoft 365-abonnementen en -licenties. Als u al geabonneerd bent op een van de ondersteunde Microsoft 365-abonnementen, hebt u dit nieuwe gebruiksrecht al. Anders, als u zich vandaag niet abonneert op Microsoft 365, kunt u zich hier aanmelden voor Microsoft 365 Business Premium of soortgelijke abonnementen. 

### <a name="how-do-i-find-out-which-users-have-only-a-microsoft-365-license"></a>Hoe kom ik erachter welke gebruikers alleen een Microsoft 365-licentie hebben?

Er zijn meerdere manieren. Ga in het beheercentrum van Microsoft 365 naar de lijst **Actieve gebruikers** en kijk naar de kolom **Licenties**. Ga in Business Central naar de lijst **Gebruikers**, kies een van de gebruikers en bekijk het feitenblok **Licenties**.  

### <a name="how-do-i-filter-the-users-list-in-business-central-to-see-users-that-only-have-a-microsoft-365-license"></a>Hoe filter ik de lijst Gebruikers in Business Central om gebruikers te zien die alleen een Microsoft 365-licentie hebben?

Deze taak is momenteel niet mogelijk met behulp van een filter of lijstweergave. U kunt echter een gebruiker in de lijst selecteren en het feitenblok Licenties bekijken dat alleen Microsoft 365 bevat als de gebruiker alleen een Microsoft 365-licentie heeft.

### <a name="what-about-users-that-have-both-a-microsoft-365-license-and-a-business-central-license"></a>Hoe zit het met gebruikers die zowel een Microsoft 365-licentie als een Business Central-licentie hebben?

Wanneer er meerdere licenties aan een gebruiker worden toegewezen, winnen de gebruikersrechten van de grotere licentie van de gebruikersrechten van de kleinere licentie bij toegang tot Business Central. In dit geval geeft de Business Central-licentie de gebruiker recht op meer gebruikersrechten. Gebruikers kunnen dus Business Central-records lezen en schrijven in Teams en toegang krijgen tot de Business Central-webclient in de browser, net als elke andere Business Central-licentiehouder. Als er specifieke machtigingensets zijn geconfigureerd voor de Microsoft 365-licentie, krijgt de gebruiker de geconfigureerde machtigingensets gecombineerd met de machtigingensets uit de Business Central-licentie of die al aan de gebruiker zijn toegewezen.

### <a name="is-this-licensing-related-to-the-business-central-team-member-license"></a>Is deze licentie gerelateerd aan de Business Central Teamlid-licentie?

Er is geen verband tussen licenties voor Business Central-teamleden en toegang tot Business Central in Microsoft Teams met Microsoft 365-licenties. Hoewel Microsoft Teams en de bijbehorende documentatie verwijzen naar mensen in een team als *teamleden*, is het een verzamelnaam voor een groep Microsoft Teams-gebruikers. Het verwijst niet naar Business Central-licenties.

### <a name="does-business-central-enforce-any-of-the-constraints"></a>Dwingt Business Central een van de beperkingen af?

Ja, alle platformbeperkingen en minimumvereisten, inclusief licentievereisten, worden afgedwongen door het Business Central-platform. Dit begeleidt gebruikers met specifieke foutmeldingen om hen te helpen bij het oplossen van problemen met hun installatie en om misbruik te voorkomen. Als een gebruiker die alleen een Microsoft 365-licentie heeft, bijvoorbeeld toegang probeert te krijgen tot de Business Central-webclient in de browser, wordt de toegang geweigerd en wordt er een begeleidend foutbericht weergegeven. 

## [Gebruik](#tab/usage)
 
### <a name="can-i-access-records-on-teams-for-ios-and-teams-for-android"></a>Heb ik toegang tot records op Teams voor iOS en Teams voor Android?

Momenteel is het niet mogelijk om toegang te krijgen tot Business Central-gegevens in Teams mobiel met alleen een Microsoft 365-licentie. Microsoft werkt eraan om deze mogelijkheid binnenkort in te schakelen. 

### <a name="how-do-users-change-their-personal-settings-in-my-settings"></a>Hoe kunnen gebruikers hun persoonlijke instellingen wijzigen in Mijn instellingen?

Wanneer een gebruiker Business Central voor het eerst opent met alleen zijn of haar Microsoft 365-licentie, worden de gebruikersinstellingen zoals taal, tijdzone en regionale instellingen automatisch ingesteld op basis van het besturingssysteem of de browserinstellingen van de gebruiker. Beheerders kunnen deze instellingen voor elke gebruiker wijzigen vanuit Business Central. 

### <a name="what-determines-the-choice-of-language-when-you-sign-in-for-the-first-time"></a>Wat bepaalt de taalkeuze bij de eerste keer inloggen?

De taal waarmee u Business Central ervaart, wordt bepaald op basis van verschillende factoren, waaronder de Teams-client waarmee u Business Central voor het eerst hebt geopend. Voor de Teams-desktopapp, Teams voor iOS en Teams voor Android wordt de taal van het besturingssysteem toegepast. Voor Teams voor het web wordt de browsertaal toegepast. In alle gevallen wordt er geen rekening gehouden met de Teams-taal. 

### <a name="why-cant-i-activate-some-of-the-colored-links-in-tabs-and-card-details"></a>Waarom kan ik sommige gekleurde links in tabbladen en kaartgegevens niet activeren?

Bruikbare koppelingen op Business Central-pagina's worden vaak weergegeven als vetgedrukte hyperlinks die kunnen worden geactiveerd om ergens anders heen te gaan of een bewerking uit te voeren. Op technisch niveau worden deze koppelingen meestal geïmplementeerd als veldwaarden zonder bijschrift die code activeren en waarbij de stijlkeuze vaak de status weerspiegelt. Wanneer gebruikers Business Central-pagina's openen met hun Microsoft 365-licentie, zijn de koppelingen gestileerd alsof ze bruikbaar zijn. Maar ze kunnen niet worden geactiveerd omdat deze licentie geen gebruiksrechten biedt om acties uit te voeren.  

### <a name="why-cant-i-activate-page-notification-actions"></a>Waarom kan ik acties voor paginameldingen niet activeren?

Contextuele meldingen die op pagina's worden weergegeven, gaan vaak vergezeld van bruikbare links. Wanneer gebruikers Business Central-pagina's openen met hun Microsoft 365-licentie, worden deze links weergegeven, maar kunnen ze niet worden geactiveerd omdat deze licentie geen gebruiksrechten biedt om acties uit te voeren. Op technisch niveau worden deze koppelingen geïmplementeerd als acties.

### <a name="can-microsoft-365-users-remove-tabs"></a>Kunnen Microsoft 365-gebruikers tabbladen verwijderen?

Ja. Iedereen in de chat of het kanaal kan tabbladen verwijderen die door anderen zijn gemaakt. Het verwijderen van een tabblad heeft geen invloed op gegevens in Business Central, maar het tabblad wordt wel verwijderd voor alle gebruikers in de chat of het kanaal.

### <a name="if-i-cant-filter-will-i-still-see-a-filtered-list-that-was-created-by-others"></a>Als ik niet kan filteren, zie ik dan nog steeds een gefilterde lijst die door anderen is gemaakt?

Gebruikers die toegang hebben tot Business Central met hun Microsoft 365-licentie hebben niet de gebruiksrechten om te filteren met behulp van het filtervenster of om lijstweergaven toe te passen. Maar als een andere gebruiker een tabblad heeft gemaakt met een gefilterde lijstpagina, zien Microsoft 365-gebruikers ook de filters die op het tabblad zijn toegepast.

---

## <a name="see-also"></a>Zie ook

[Overzicht van toegang tot Business Central met Microsoft 365-licenties](admin-access-with-m365-license.md#minimum-requirements)  
[Toegang met Microsoft 365-licenties instellen](admin-access-with-m365-license-setup.md)  
