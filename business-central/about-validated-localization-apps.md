---
title: Ontwikkeling van gevalideerde lokalisatie-apps
description: Voldoen aan de wettelijke vereisten in Dynamics 365 Business Central als gevalideerde lokalisatie-app.
author: altotovi
ms.date: 04/24/2024
ms.reviewer: solsen
ms.topic: conceptual
ms.author: altotovi
---


# <a name="development-of-validated-localization-apps"></a>Ontwikkeling van gevalideerde lokalisatie-apps

In dit artikel worden de vereisten en richtlijnen beschreven voor het ontwikkelen van een gevalideerde lokalisatie-app voor [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="what-is-a-validated-localization-app"></a>Wat is een gevalideerde lokalisatie-app?

[!INCLUDE[prod_short](includes/prod_short.md)] is [wereldwijd op meer dan 170 markten](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json) beschikbaar. In een aantal markten werkt Microsoft samen met ISV-partners om [!INCLUDE[prod_short](includes/prod_short.md)] te lokaliseren via lokalisatie-apps die beschikbaar zijn op [Microsoft AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). Voor die regio's kunnen lokalisaties beschikbaar zijn via het voorkeursprogramma voor lokalisatie-apps. Het voorkeursprogramma voor lokalisatie-apps herkent die apps, die zijn gebouwd volgens de specifieke kwaliteitsrichtlijnen van Microsoft. ISV-partners die aan deze programmavereisten en richtlijnen voldoen, kunnen er technisch en commercieel van profiteren om hun wederverkopers en klanten te bedienen.  

In de volgende secties vindt u vereisten en richtlijnen. Als u aan dit programma wilt deelnemen en aan de onderstaande vereisten wilt voldoen, kunt u contact met het programmateam opnemen via het [Microsoft-lokalisatieteam](mailto:d365bcloc@microsoft.com).   

> [!IMPORTANT]
> Het initiatief [!INCLUDE[prod_short](includes/prod_short.md)] voor gevalideerde lokalisatie-apps wordt momenteel uitgerold als pilotprogramma. Onderstaande vereisten en voordelen kunnen veranderen op basis van de feedback van partners en klanten.  

Apps in het gevalideerde pilotprogramma voor lokalisatie bevatten een reeks functionaliteiten die voldoen aan lokale wettelijke vereisten die binnen een van de categorieën in de volgende lijst vallen.  

- **Regelgevende vereisten** - lokale functionaliteit waarmee bedrijven aan hun wettelijke vereisten kunnen voldoen, zoals belastingaangifte, lokale indelingen voor e-facturering, lokale GAAP en andere wettelijke vereisten.
- **Vereisten voor nationale standaarden** – lokale functionaliteit die betrekking heeft op lokale standaarden, zoals adresindelingen, nationale bankindelingen of lokale interpretaties van mondiale standaarden.
- **Lokale taal** - lokale taal in de lokalisatie-app, maar ook voor een basis-app als deze taal momenteel niet op de lijst staat met [ondersteunde talen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).
- **Lokale taal** - lokale taal in een lokalisatie-app, maar ook voor een basis-app als deze taal momenteel niet op de lijst staat met [ondersteunde talen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

> [!NOTE]
> Lokale marktbehoeften of branchevereisten mogen niet worden opgenomen in de voorkeurslokalisatie-apps. Als apps deze functionaliteiten bevatten, kunnen de apps niet worden goedgekeurd als gevalideerde lokalisatie-apps.

> [!NOTE]
> Lokale functionaliteit is gunstig voor de productiviteit van bedrijfsprocessen in een land/regio en voegt daardoor waarde toe aan het bedrijf, maar is niet vereist vanuit een regelgevend perspectief, zoals specifieke bank- en betalingsindelingen, onkostendeclaraties, HR-functies, salarisadministratie en soortgelijke kleinere of grotere, en leuke functies moeten in andere apps worden geïsoleerd. Als apps deze functionaliteiten bevatten, worden ze niet goedgekeurd als gevalideerde lokalisatie-apps.   

## <a name="validated-localization-app-business-requirements"></a>Gevalideerde bedrijfsvereisten voor lokalisatie-apps

- De aanbieder van de gevalideerde lokalisatie-app voldoet aan alle vereisten om een indirecte aanbieder van CSP te zijn.  
- De aanbieder van de gevalideerde lokalisatie-app brengt een minimum van aanbod in vijf landen/regio's, die Dynamics 365 Business Central bundelen met een gevalideerde lokalisatie-app. 
- De aanbieder van de gevalideerde lokalisatie-app heeft een minimum van 10 [!INCLUDE[prod_short](includes/prod_short.md)] online klanten met productieomgevingen, die actief gebruik maken van de gevalideerde lokalisatie-app. 
- De aanbieder van de gevalideerde lokalisatie-app dient jaarlijks een bedrijfsplan in bij het v-team van het programma. Dit omvat geplande marketing- en gereedheidsactiviteiten om het gebundelde aanbod met indirecte resellers van CSP in toepasselijke landen/regio's te promoten. Plan kan aan het begin van ieder kwartaal worden ingediend bij [Microsoft-lokalisatieteam](mailto:d365bcloc@microsoft.com).  
- Gevalideerde lokalisatie-apps worden beschikbaar gesteld aan alle klanten en partners die hiervan willen profiteren.  
- De aanbieder van de gevalideerde lokalisatie-app brengt een minimum van aanbod op de markt in vijf landen/regio's, die Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)] bundelen met een gevalideerde lokalisatie-app. 
- De aanbieder van de gevalideerde lokalisatie-app heeft een minimum van 10 [!INCLUDE[prod_short](includes/prod_short.md)] online klanten met productieomgevingen, die actief gebruik maken van de gevalideerde lokalisatie-app. 
- De aanbieder van de gevalideerde lokalisatie-app dient jaarlijks een bedrijfsplan in bij het v-team van het programma. Dit omvat geplande marketing- en gereedheidsactiviteiten om het gebundelde aanbod met indirecte resellers van CSP in toepasselijke landen/regio's te promoten. Plan kan aan het begin van een kwartaal worden ingediend bij het [Microsoft-lokalisatieteam](mailto:d365bcloc@microsoft.com).  
- Gevalideerde lokalisatie-apps worden beschikbaar gesteld aan alle klanten en partners die hiervan willen profiteren.  
- De aanbieder van de gevalideerde lokalisatie-app houdt zich bezig met terugkerende werkstromen met Microsoft.

## <a name="validated-localization-app-functional-and-technical-requirements"></a>Functionele en technische vereisten voor de gevalideerde lokalisatie-app

### <a name="functionality-requirements"></a>Functionaliteitsvereisten

Naast het voldoen aan de technische vereisten voor de voorkeurslokalisatie-app, is de minimaal haalbare productomvang voor de voorkeurslokalisatie-app:  

- Lokale regelgevingsfuncties:   
  - Wettelijke vereisten.   
  - Officieel verplichte functies. 
  - Alleen horizontale functies (niet branchespecifiek).  
  - Toepasbaar in de meeste bedrijven.  
  - Binnen de volgende blauwdruk:   
    - Gebieden met de meest voorkomende wetswijzigingen. 
    - Al bijgehouden als lokalisatie in Microsoft-lokalisaties. 
    - Functiereferenties – zelden nieuw.  
    - Geen leveranciers-/bankspecifieke indelingen, salarisadministratie of iets dergelijks. 
    - Geen globale functies als ze niet door Microsoft zijn gebouwd. 
- Vertalingen: 
  - Vertaling van een lokalisatie-app naar lokale talen. 
  - Vertaling van een basisapp naar lokale talen – als de taal nog niet wordt [ondersteund](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).  
  - Vertaling van de documentatie van de lokalisatie-app naar lokale talen. 
- Ook al maken ze beide deel uit van de lokalisatie, toch wordt aanbevolen om de nationale standaardfuncties (het lokale deel) te bouwen als afzonderlijke apps, los van de lokale regelgevende functies. 
- Demogegevens in de lokale taal, van toepassing op de specifieke markt.   
- Alle functies moeten worden ontworpen om een vereenvoudigde gebruikersinterface te behouden. Houd er rekening mee dat ze in de eerste plaats bedoeld zijn voor de MKB-markt.  
- Vermijd het bouwen van nieuwe functies als dezelfde of vergelijkbare functionaliteiten al bestaan in de basisapp, zoals elektronische facturering, controle-exports, btw-functies, gegevensuitwisseling en andere waarbij de meeste functionaliteit gemeenschappelijk is voor alle landen/regio's, maar er enkele lokale regels of bedrijfsindelingen zijn die uitbreidingen zijn van globale raamwerken of indelingen. In plaats van nieuwe functies te bouwen kunt u bestaande uitbreiden.  
- Stel installatiehandleidingen (wizards) op voor gebieden die complex zijn om in te stellen, zodat gebruikers uw lokalisatie-app kunnen inschakelen, ontdekken en er een goede eerste ervaring mee kunnen opdoen.  
- Alle functies moeten worden ontworpen om een vereenvoudigde gebruikersinterface te behouden. Houd er rekening mee dat ze in de eerste plaats bedoeld zijn voor de MKB-markt.  
- Vermijd het bouwen van nieuwe functies als dezelfde of vergelijkbare functionaliteiten al bestaan in de basisapp, zoals elektronische facturering, controle-exports, btw-functies, gegevensuitwisseling en andere waarbij de meeste functionaliteit gemeenschappelijk is voor alle landen/regio's, maar er enkele lokale regels of bedrijfsindelingen zijn die uitbreidingen zijn van globale raamwerken of indelingen. In plaats van nieuwe functies te bouwen kunt u bestaande uitbreiden.    
- Stel installatiehandleidingen (wizards) op voor gebieden die complex zijn om in te stellen, zodat gebruikers uw lokalisatie-app kunnen inschakelen, ontdekken en er een goede eerste ervaring mee kunnen opdoen.  
- Partners moeten functionele documentatie verstrekken voor alle aspecten van hun lokalisatie.  

### <a name="technical-requirements"></a>Technische vereisten

Hieronder vindt u een lijst met vereisten waaraan u moet voldoen voordat u de gevalideerde lokalisatie-app als extensie ter validatie indient. Deze lijst verandert niets aan de [technische validatielijst](/dynamics365/business-central/dev-itpro/developer/devenv-checklist-submission) en breidt vanaf daar alleen de vereisten uit.  

- De aanbieders van gevalideerde lokalisatie-apps moeten de gevalideerde lokalisatie-app bouwen op basis van de W1-basisapp.  
- De aanbieders van gevalideerde lokalisatie-apps moeten het levenscyclus- en ondersteuningsbeleid van Microsoft volgen.   
- Verplichte testautomatisering moet minstens 80% van de code omvatten en alle bedrijfsprocessen die veranderen met de gevalideerde lokalisatie-app moeten worden gedekt door testautomatisering.  
- De aanbieders van de gevalideerde lokalisatie-app moeten de app updaten en/of testen vóór de officiële introductie van een nieuwe release (minimaal met de RC vóór de nieuwe release) om te bevestigen dat er geen problemen zijn. 
- Alle objecten in de code van de gevalideerde lokalisatie-app moeten in het Engels zijn.   
- De aanbieders van gevalideerde lokalisatie-apps moeten het Microsoft-beleid volgen voor verouderde objecten en onderbrekende wijzigingen en best practices voor de afschaffing van de AL-code.  
- De aanbieders van gevalideerde lokalisatie-apps moeten nieuwe gebeurtenissen toevoegen als dit door de markt wordt vereist (andere implementatiepartners of klanten) als dit vanuit zakelijk oogpunt zinvol is, in overeenstemming met het beleid en de praktijk van Microsoft. Anders moeten de aanbieders van gevalideerde lokalisatie-apps antwoorden op dergelijke vragen geven, met de juiste motivering waarom het zakelijk gezien niet zinvol is om hieraan toe te voegen. 
- De aanbieders van gevalideerde lokalisatie-apps moeten schriftelijke testscenario's in het Engels leveren en Microsoft in staat stellen handmatige tests uit te voeren, indien vereist door Microsoft.  
- Als een gevalideerde lokalisatie-app het [!INCLUDE[prod_short](includes/prod_short.md)]-gegevensmodel uitbreidt met nieuwe tabellen en/of velden, moet de aanbieder van de gevalideerde lokalisatie-app de eigenschap **DataClassification** correct instellen.
- De aanbieders van gevalideerde lokalisatie-apps moeten de gevalideerde lokalisatie-app bouwen op basis van de W1-basisapp.  
- De aanbieders van gevalideerde lokalisatie-apps moeten het levenscyclus- en ondersteuningsbeleid van Microsoft volgen.   

> [!NOTE]  
> U kunt ook een integratie maken als u het nuttig vindt om bepaalde functionaliteit buiten de [!INCLUDE[prod_short](includes/prod_short.md)]-omgeving te plaatsen en in plaats daarvan verbinding te maken met [!INCLUDE[prod_short](includes/prod_short.md)] met behulp van bijvoorbeeld API's of webservices.

## <a name="see-also"></a>Zie ook

[Technische validatie](/dynamics365/business-central/dev-itpro/developer/devenv-checklist-submission)  
[Ontwikkeling van een standaardlokalisatieoplossing](/dynamics365/business-central/dev-itpro/developer/readiness/readiness-develop-localization)  
[Beschikbaarheid in landen/regio's en ondersteunde vertalingen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Wat is lokale functionaliteit in Dynamics 365? [!INCLUDE[prod_short](includes/prod_short.md)]](about-localization.md)  
[Internationale beschikbaarheid van Microsoft Dynamics 365](/dynamics365/get-started/availability)  
[Overzicht van naleving](compliance/compliance-overview.md)  
[Geografische beschikbaarheid voor Dynamics 365](https://dynamics.microsoft.com/en-us/availability-reports/georeport/)  
