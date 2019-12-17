---
title: Veelgestelde vragen over lijstweergaven
description: Gedetailleerde informatie over het opslaan van filters als lijstweergaven.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: list, filter, pane, views
ms.date: 01/01/2019
ms.author: mikebc
ms.openlocfilehash: 6357a025c58df8e55bf7aaad5961190ad6ed3350
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882002"
---
# <a name="list-views-faq"></a>Veelgestelde vragen over lijstweergaven
Dit onderwerp beantwoordt vragen die onze geavanceerde gebruikers vaak stellen over het werken met lijstweergaven en het opslaan van filters.  

### <a name="how-do-views-handle-expressions"></a>Hoe gaan weergaven om met expressies?
Wanneer u een weergave opslaat die filters met expressies bevat, zoals datumbereiken, operatoren, trefwoorden of filtertokens, wordt de expressie en niet de resulterende waarden opgeslagen. Als u bijvoorbeeld een weergave opslaat die filtert op het veld **Aanmaakdatum** met de expressie **-1W..vandaag** worden altijd records gevonden met betrekking tot de huidige datum, zelfs wanneer de weergave volgende maand wordt geopend.

### <a name="where-are-list-views-saved"></a>Waar worden lijstweergaven opgeslagen?
Net zoals bij het verbergen van een veld of het opnieuw ordenen van uw navigatiemenu zijn lijstweergaven een onderdeel van gebruikerspersonalisatie en worden ze opgeslagen in de database. Als u alle personalisatie in een lijst wist, worden ook uw persoonlijke weergaven permanent verwijderd en wordt aanvullende personalisatie gewist, zoals het opnieuw ordenen van weergaven. Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.

### <a name="why-dont-i-have-a-save-icon"></a>Waarom heb ik geen pictogram Opslaan?
Het pictogram Opslaan en het optiemenu worden niet weergegeven naast weergaven in het filtervenster als personalisatie is uitgeschakeld voor een gebruikersrol. Gebruikers die personalisatie niet hebben ingeschakeld, hebben nog steeds toegang tot systeemweergaven die standaard deel uitmaken van de pagina en kunnen filters wijzigen of meer filters maken.

### <a name="on-which-page-types-can-i-use-list-views"></a>Op welke paginatypen kan ik lijstweergaven gebruiken?
Weergaven zijn alleen beschikbaar op lijst- en werkbladpagina's.

### <a name="are-views-also-available-on-other-form-factors"></a>Zijn weergaven ook beschikbaar voor andere formulierfactoren?
Ja. Alle weergaven die u opslaat in uw desktopbrowser of desktop-app, zijn ook beschikbaar op uw tablet of smartphone. U kunt weergaven op mobiele apparaten niet wijzigen of personaliseren.

### <a name="are-my-personal-views-always-accessible"></a>Zijn mijn persoonlijke weergaven altijd toegankelijk?
Dezelfde weergaven zijn beschikbaar op een lijstpagina als u deze opent vanuit het navigatiemenu, via het venster **Vertel het me** of via een URL-koppeling naar de lijstpagina. Weergaven zijn niet beschikbaar in lijstonderdelen, opzoekbewerkingen of wanneer een lijstpagina wordt weergegeven als een dialoogvenster.

### <a name="how-do-i-return-a-view-to-its-original-filters-after-modifying-them"></a>Hoe breng ik een weergave terug naar de oorspronkelijke filters nadat ik ze heb gewijzigd?
Kies onder aan het filtervenster de actie **Filters opnieuw instellen** om filterwijzigingen die u in de weergave hebt aangebracht, te wissen en terug te keren naar de oorspronkelijke gefilterde velden en filtercriteria.

### <a name="what-is-the-difference-between-hiding-and-removing-views"></a>Wat is het verschil tussen het verbergen en verwijderen van weergaven?
Als u een weergave verwijdert, wordt die weergave permanent verwijderd. Als u een weergave verbergt, kunt u deze tijdelijk verbergen in het filtervenster, maar u kunt deze later weer zichtbaar maken door de actie **Weergeven** te kiezen.

### <a name="how-can-i-share-my-views-with-others"></a>Hoe kan ik mijn weergaven met anderen delen?
[!INCLUDE[d365fin](includes/d365fin_md.md)] biedt geen manier om de precieze lijstweergave te delen, maar u kunt uw huidige filters delen zodat andere gebruikers een vergelijkbare lijst met records kunnen zien. Kopieer in uw desktopbrowser eenvoudig de URL en deel deze met uw collega's. Het delen van filters geeft de ontvanger niet per se een identieke set filters die u in uw browser ziet.

### <a name="can-i-search-for-views-in-the-tell-me-window"></a>Kan ik zoeken naar weergaven in het venster Vertel me?
Nee. Het venster **Vertel me** toont alleen zoekresultaten voor de pagina, maar u bent slechts een stap verwijderd van uw favoriete weergave zodra u naar de pagina navigeert.

### <a name="what-is-shared-layout"></a>Wat is een gedeelde indeling?
Alle weergaven op een lijstpagina delen een gemeenschappelijke kolomindeling die omvat welke kolommen worden weergegeven, hun volgorde, breedte, bevroren deelvenster en instellingen voor snelle invoer. Het personaliseren van een kolomindeling heeft ook invloed op andere weergaven die dezelfde indeling op de lijstpagina delen.

Sommige systeemweergaven kunnen unieke indelingen van de kolommen in de lijst hebben. Ze kunnen bijvoorbeeld kolommen herschikken om alleen de kolommen weer te geven die het meest relevant zijn voor die weergave. U kunt bepalen welke weergaven unieke indelingen hebben door het pictogram ![Meer opties weergeven](media/show-more-options-icon.png "Meer opties weergeven") te kiezen en te zien dat het selectievakje **Gedeelde indeling** niet is ingeschakeld. Als gebruiker kunt u de kolomindeling voor een weergave met een unieke indeling personaliseren zonder dat dit van invloed is op de andere weergaven op de lijstpagina. Alleen ontwikkelaars kunnen een unieke kolomindeling definiëren voor een weergave die in eerste instantie een gedeelde indeling heeft.

### <a name="what-does-the-show-system-filters-link-do"></a>Wat doet de link Systeemfilters weergeven?
Op sommige lijstpagina's bevat het filtervenster **Systeemfilters weergeven** onder aan het filtervenster wanneer de pagina filters bevat die door het systeem zijn opgegeven. Deze speciale filters worden meestal gebruikt om records weer te geven op basis van de huidige context, bijvoorbeeld wanneer een lijst met orders voor een specifieke klant moet worden gefilterd.

Systeemfilters worden door ontwikkelaars ingesteld met behulp van filtergroep 0. Zie voor technische details over systeemfilters [Methode Filtergroep](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-filtergroup-method)

### <a name="i-see-multiple-views-on-my-page-but-i-did-not-create-them-where-did-they-come-from"></a>Ik zie meerdere weergaven op mijn pagina, maar ik heb ze niet gemaakt. Waar komen ze vandaan?
De weergaven die u in een lijst ziet, zijn een combinatie van uw persoonlijke weergaven samen met systeemweergaven. Systeemweergaven kunnen afkomstig zijn van de bedrijfstoepassing, van extensies of kunnen rolspecifiek zijn als de lijst is aangepast voor uw rol.

### <a name="why-do-some-views-provide-fewer-options"></a>Waarom bieden sommige weergaven minder opties?
Sommige weergaven bieden alleen de optie om een kopie van de weergave op te slaan, terwijl andere het opslaan van wijzigingen in de weergave niet toestaan. Hoe de weergave is gemaakt, bepaalt de beschikbare opties voor die weergave. Weergaven kunnen op verschillende manieren worden gemaakt:
- Persoonlijke weergaven die u hebt opgeslagen
- Systeemweergaven die standaard deel uitmaken van de bedrijfstoepassing of worden toegevoegd door extensies of rolspecifieke weergaven. In tegenstelling tot persoonlijke weergaven kunt u wijzigingen in filters niet opslaan in die systeemweergave.
- Verouderde systeemweergaven die standaard deel uitmaken van de bedrijfstoepassing maar zijn gemaakt met oudere versies van [!INCLUDE[d365fin](includes/d365fin_md.md)]. Deze weergaven bieden aanzienlijk minder opties. U kunt ze alleen opslaan als een nieuwe weergave en u kunt ze ook niet verbergen of opnieuw ordenen. Houd er rekening mee dat oudere systeemweergaven zullen worden stopgezet in een toekomstige update van [!INCLUDE[d365fin](includes/d365fin_md.md)].

### <a name="how-do-i-convert-legacy-system-views"></a>Hoe converteer ik oudere systeemweergaven?
Oude systeemweergaven zijn lijstweergaven die door ontwikkelaars in oudere versies van [!INCLUDE[d365fin](includes/d365fin_md.md)] zijn gemaakt door ze op de pagina Rolcentrum te plaatsen. Deze weergaven worden nu rechtstreeks op de lijstpagina weergegeven, maar bieden een verslechterde ervaring en aanzienlijk minder opties. U kunt een oude systeemweergave omzetten in een persoonlijke weergave die volledig aanpasbaar is, gewoon door die oude weergave op te slaan als een nieuwe weergave. Op dezelfde manier kunnen beheerders ervoor kiezen om rolspecifieke oudere systeemweergaven te converteren door de gebruikersrol aan te passen en de oude weergave op te slaan als een nieuwe rolspecifieke weergave.

Houd er rekening mee dat oudere systeemweergaven zullen worden stopgezet in een toekomstige update van [!INCLUDE[d365fin](includes/d365fin_md.md)].

### <a name="others-in-my-organization-need-similar-list-views-as-standard-what-can-i-do"></a>Anderen in mijn organisatie hebben standaard vergelijkbare lijstweergaven nodig. Wat kan ik doen?
Werken met persoonlijke weergaven is snel en effectief, maar [!INCLUDE[d365fin](includes/d365fin_md.md)] biedt extra hulpmiddelen om lijstweergaven te definiëren die nodig zijn voor specifieke gebruikersrollen of alle gebruikers in de organisatie.
 - Ontwikkelaars kunnen de omgeving aanpassen en lijstweergaven maken in extensies voor alle gebruikers in de organisatie.
 - Niet-codeerders zoals beheerders of afdelingsmanagers kunnen rolspecifieke lijstweergaven maken bij het aanpassen van een rol vanaf de pagina **Profielen (rollen)**.

### <a name="i-work-with-multiple-languages-how-do-i-translate-the-name-of-the-view"></a>Ik werk met meerdere talen: hoe vertaal ik de naam van de weergave?
Wanneer u een nieuwe weergave opslaat of een bestaande weergave hernoemt, moet u een herkenbare en betekenisvolle naam voor die weergave invoeren. De naam wordt opgeslagen voor uw huidige taal en wordt ook weergegeven wanneer u of andere gebruikers in verschillende talen werken in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Als u vertaalde weergavenamen wilt opgeven, moet u van taal wisselen met de pagina **Mijn instellingen** en de weergave vervolgens hernoemen, waardoor de vertaalde naam in de nieuwe taal wordt opgeslagen.

### <a name="do-views-with-expressions-work-in-all-languages"></a>Werken weergaven met expressies in alle talen?
Expressies die alleen symbolen gebruiken, zoals '**|**' of **..**, worden als veilig beschouwd voor gebruikers in elke taal. Weergaven met expressies die letters, trefwoorden of filtertokens bevatten, werken alleen voor de taal waarin ze zijn geschreven.


### <a name="see-also"></a>Zie ook  
[Lijstweergaven opslaan en personaliseren](ui-views.md)  
[Functies en informatie zoeken](ui-search.md)    
[Sorteren, zoeken en filteren](ui-enter-criteria-filters.md)  
