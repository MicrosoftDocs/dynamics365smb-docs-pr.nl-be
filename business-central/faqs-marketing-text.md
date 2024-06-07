---
title: Veelgestelde vragen voor marketingtekstsuggesties
description: 'Deze veelgestelde vragen geven informatie over de AI-technologie die wordt gebruikt in Business Central, samen met belangrijke overwegingen en details over hoe AI wordt gebruikt, hoe deze werd getest en geëvalueerd, en eventuele specifieke beperkingen.'
ms.date: 10/07/2023
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.collection:
  - bap-ai-copilot
---

# <a name="faq-for-marketing-text-suggestions-with-copilot"></a>Veelgestelde vragen voor marketingtekstsuggesties met Copilot

Deze veelgestelde vragen (FAQ) beschrijven de AI-impact van de [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] functie in [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="what-is-item-marketing-text-suggestions"></a>Wat zijn suggesties voor marketingtekst van artikelen?

Copilot biedt schrijfhulp voor gebruikers die verantwoordelijk zijn voor het schrijven van marketingtekst (ook wel kopij genoemd) voor artikelen in [!INCLUDE[prod_short](includes/prod_short.md)]. Deze functie staat bekend als [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]. De functie [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] biedt schrijfhulp voor gebruikers die verantwoordelijk zijn voor het schrijven van marketingtekst (ook wel *kopij* genoemd) voor artikelen in [!INCLUDE[prod_short](includes/prod_short.md)].

De functie is beschikbaar op elke artikelkaart in [!INCLUDE[prod_short](includes/prod_short.md)]. Om het te gebruiken opent u gewoon een artikel en selecteert u vervolgens **Marketingtekst** > **Opstellen met Copilot**. Deze actie genereert automatisch een tekstsuggestie die aantrekkelijk, creatief en specifiek is voor het weergegeven artikel. Suggesties zijn gebaseerd op verschillende input, waaronder:

- De kenmerken, categorie en naam van het artikel.
- Persoonlijke schrijfstijlvoorkeuren zoals toon, benadrukte kwaliteit, formaat en lengte.

U kunt de waarde van deze invoeropties wijzigen om de uitkomst van de door AI gegenereerde tekst te beïnvloeden. Voordat u een suggestie opslaat, kunt u deze eenvoudig controleren en bewerken op nauwkeurigheid, of een andere suggestie proberen.

Enkele belangrijke voordelen van deze functie zijn onder meer:

- Verkort de tijd die wordt besteed aan het schrijven van teksten, wat de time-to-market kan versnellen voor artikelen die in online winkels worden verkocht.
- Ontgrendelt creativiteit om aantrekkelijkere productbeschrijvingen te geven.
- Verbetert de consistentie van marketingmateriaal voor productlijnen.

## <a name="what-are-the-systems-capabilities"></a>Wat zijn de mogelijkheden van het systeem?

De functie [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] gebruikt de [Azure OpenAI-service van Microsoft](/azure/cognitive-services/openai/overview) om toegang te krijgen tot krachtige taalmodellen die natuurlijke taal analyseren en genereren. Deze modellen zijn getraind op een groot aantal tekstgegevenssets. Hierdoor kan Copilot voorgestelde, gepersonaliseerde antwoorden in het Engels genereren op basis van een minimale hoeveelheid invoergegevens, zoals de kenmerken, categorie of beschrijving van een artikel. 

## <a name="what-is-the-systems-intended-use"></a>Wat is het beoogde gebruik van het systeem?

Deze functie is bedoeld om gebruikers te helpen bij het maken van marketingtekst voor artikelen in [!INCLUDE[prod_short](includes/prod_short.md)]. Schrijvers gebruiken de functie om snel overtuigende en boeiende tekstsuggesties te krijgen, die vervolgens worden beoordeeld en bewerkt op nauwkeurigheid. 

## <a name="how-was-item-marketing-text-evaluated-what-metrics-are-used-to-measure-performance"></a>Hoe werd artikelmarketingtekst beoordeeld? Welke statistieken worden gebruikt om de prestaties te meten?

- De functie werd uitgebreid getest, waarbij talloze teksten in verschillende talen door taalexperts werden beoordeeld op basis van verschillende criteria. De tests waren gebaseerd op de demonstratiegegevens van [!INCLUDE[prod_short](includes/prod_short.md)] en andere fictieve productcatalogi.
- Deze functie is gebouwd in overeenstemming met de Responsible AI Standard van Microsoft. [Lees meer over verantwoorde AI van Microsoft](https://aka.ms/RAI).

## <a name="how-does-microsoft-monitor-the-quality-of-generated-content"></a>Hoe bewaakt Microsoft de kwaliteit van de gegenereerde inhoud?

Microsoft beschikt over verschillende systemen om ervoor te zorgen dat de mogelijkheden van Copilot operationeel blijven en inhoud van de hoogste kwaliteit genereren.

- Gebruikers hebben de mogelijkheid om feedback te geven om ongepaste inhoud te melden en de functionaliteit te verbeteren.

  - Als u ongepast gegenereerde inhoud tegenkomt, rapporteer dit dan aan Microsoft met behulp van dit feedbackformulier: [Misbruik melden](https://go.microsoft.com/fwlink/?linkid=2249810). 

    Microsoft schakelt mogelijk de door Copilot aangestuurde functies uit voor geselecteerde klanten als misbruik van de functionaliteit wordt gedetecteerd. 

  - We houden gebruikersfeedback bij in [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] om ons te helpen suggesties te verbeteren. 

    U geeft feedback door het pictogram Vind ik leuk (duim omhoog) of Niet leuk (duim omlaag) te gebruiken op de pagina **Copilot** in [!INCLUDE[prod_short](includes/prod_short.md)]. We verzamelen de telemetrie van deze gebaren voor elke AI-uitvoer waarvoor u feedback indient.

    ![Toont een artikelkaart met het deelvenster Marketingtekst](media/create-with-copilot-window-feedback.svg)

- De Azure OpenAI-service slaat prompts en voltooiingen vanuit de service op om te controleren op misbruik en om de kwaliteit van de inhoudsbeheersystemen van Azure OpenAI te ontwikkelen en te verbeteren. [Meer informatie over ons inhoudsbeheer en filtering](/azure/cognitive-services/openai/concepts/content-filter). Uw bedrijfsgegevens worden niet gebruikt om AI-modellen te trainen in de Azure OpenAI-service.

   Geautoriseerde Microsoft-medewerkers hebben toegang tot uw prompt- en voltooiingsgegevens die onze geautomatiseerde systemen hebben geactiveerd voor het onderzoeken en verifiëren van mogelijk misbruik; voor klanten die [!INCLUDE[prod_short](includes/prod_short.md)] in de Europese Unie gebruiken, bevinden de geautoriseerde Microsoft-medewerkers zich in de Europese Unie. Deze gegevens kunnen worden gebruikt om onze inhoudsbeheersystemen te verbeteren. In het geval van een bevestigde beleidsschending kunnen we u vragen om onmiddellijk actie te ondernemen om het probleem op te lossen en om verder misbruik te voorkomen. Als het probleem niet wordt verholpen, kan de toegang tot Azure OpenAI-bronnen worden opgeschort of beëindigd.

   Raadpleeg [Gegevens, privacy en beveiliging voor de Azure OpenAI-service](/legal/cognitive-services/openai/data-privacy#abuse-and-harmful-content-generation) voor meer informatie.

## <a name="is-there-a-logging-and-human-review-process-as-part-of-azure-openai-service-and-if-so-can-i-opt-out"></a>Bestaat er een proces voor logboekregistratie en menselijke beoordeling als onderdeel van de Azure OpenAI-service, en zo ja, kan ik mij hiervoor afmelden?

Als onderdeel van het leveren van de Azure OpenAI-service verwerkt en bewaart Microsoft klantgegevens die bij de service zijn ingediend, evenals uitvoerinhoud, met als doel toezicht te houden op misbruik of schadelijk gebruik of uitvoer van de service en dit te voorkomen; en voor het ontwikkelen, testen en verbeteren van mogelijkheden die zijn ontworpen om misbruik van en schadelijke uitvoer van de service te voorkomen. 

Geautoriseerd Microsoft-personeel kan gegevens bekijken die onze geautomatiseerde systemen hebben geactiveerd om mogelijk misbruik te onderzoeken en te verifiëren, en kan een beperkte willekeurige steekproef nemen van termen die niet door onze geautomatiseerde systemen zijn gemarkeerd om ervoor te zorgen dat de systemen correct werken. Geautoriseerd Microsoft-personeel heeft ook toegang tot deze gegevens en kan deze gebruiken om onze systemen te verbeteren die misbruik of schadelijk gebruik of uitvoer van de service controleren en voorkomen. Lees meer op [preview-voorwaarden](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/)

Zodat Microsoft de service en zijn klanten kan beschermen is het niet mogelijk om u af te melden voor logboekregistratie en menselijke beoordelingsprocessen.

## <a name="what-data-does-the-capability-collect-how-is-the-data-used"></a>Welke gegevens worden door de functie verzameld? Hoe worden de gegevens gebruikt?

De mogelijkheid voor marketingtekstsuggesties verzamelt de minimale gegevens die Business Central nodig heeft om de service aan te bieden. Zie [Dynamics 365-voorwaarden voor door Azure OpenAI aangedreven functies](https://go.microsoft.com/fwlink/?linkid=2236010) voor meer informatie.

De mogelijkheid verzamelt ook gegevens van de feedback die gebruikers kunnen geven met behulp van de pictogrammen 'Vind ik leuk' (duim omhoog) of 'Niet leuk' (duim omlaag) bovenaan de pagina **Copilot**. De gegevens zijn anoniem en omvatten de keuze tussen Vind ik leuk of Niet leuk, de reden voor Niet leuk (indien opgegeven) en de Copilot-functie waarop de feedback van toepassing is. We gebruiken deze gegevens om de kwaliteit van de functie te beoordelen en te verbeteren.

## <a name="what-are-the-limitations-of--how-can-users-minimize-the-impact-of-the-includefeature-marketing-text-suggestions-limitations-when-using-the-system"></a>Wat zijn de huidige beperkingen van [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]? Hoe kunnen gebruikers de impact van de beperkingen van [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] tot een minimum terugbrengen bij het gebruik van het systeem?

- Omdat de onderliggende technologie achter de functie AI gebruikt die is getraind op een breed scala aan bronnen, is de gegenereerde inhoud niet altijd feitelijk of geschikt. Sommige suggesties kunnen zelfs twijfelachtige of ongepaste inhoud bevatten. Het is uw verantwoordelijkheid om gegenereerde suggesties te bekijken en te bewerken om er zeker van te zijn dat deze nauwkeurig en gepast zijn.
- [!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]

  Onnauwkeurige antwoorden kunnen worden geretourneerd wanneer gebruikers met het systeem communiceren in andere dan de ondersteunde talen. Ook kan er onnauwkeurige tekst worden gegenereerd als de taal van de gebruiker en de primaire gegevenstaal in de [!INCLUDE[prod_short](includes/prod_short.md)]-database niet identiek zijn.

## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-system"></a>Welke operationele factoren en instellingen maken een effectief en verantwoordelijk gebruik van het systeem mogelijk?

Er zijn een paar dingen die u kunt doen om de functie optimaal te benutten:

- Voeg meer kenmerken toe aan een artikel om de specifieke functies en eigenschappen waarin u geïnteresseerd bent te promoten.
- Pas de opties voor de toon van de stem en de nadruk op kwaliteit aan uw persoonlijke voorkeuren aan.
- Verbeter de beschrijving van een artikel.
- Zorg ervoor dat het artikel in de meest geschikte categorie wordt ingedeeld.

Ga voor meer informatie naar [Tekstsuggesties verbeteren en aanpassen](item-marketing-text.md#improve-and-tailor-text-suggestions).

> [!TIP]
> Controleer de suggesties altijd op nauwkeurigheid voordat u ze opslaat en publiceert voor openbaar gebruik.


## <a name="see-also"></a>Zie ook

- [Suggesties voor marketingteksten](ai-overview.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
