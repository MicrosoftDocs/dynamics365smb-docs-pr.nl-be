---
title: Veelgestelde vragen over op AI gebaseerde artikelmarketingtekst (preview) met Copilot
description: Krijg antwoorden op veelgestelde vragen over de door AI gegenereerde tekstmogelijkheden met Copilot.
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: faq
ms.date: 04/03/2023
ms.custom: bap-template
author: jswymer
ms.service: dynamics365-business-central
---

# Veelgestelde vragen over op AI gebaseerde artikelmarketingtekst (preview) met Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Dit artikel gebruikt vragen en antwoorden om belangrijke aspecten uit te leggen over de AI-technologie achter Copilot en de tekst die het genereert.

## [Algemeen](#tab/general)

### Wat is Copilot?

Copilot biedt door AI gegenereerde tekstsuggesties voor artikelen in Business Central. Het is bedoeld voor gebruikers die marketingteksten voor artikelen schrijven om hen te helpen boeiende en interessante inhoud te produceren. Dit zijn enkele belangrijke voordelen:

- Verkort de tijd die wordt besteed aan het schrijven van teksten, wat de time-to-market kan versnellen voor artikelen die in online winkels worden verkocht.
- Ontgrendelt creativiteit om aantrekkelijkere productbeschrijvingen te geven.
- Verbetert de consistentie van marketingmateriaal voor productlijnen.

Gebruikers moeten de door AI gegenereerde tekst beschouwen als een suggestie die moet worden beoordeeld en bewerkt op juistheid voordat deze openbaar beschikbaar is.

### Waarom is Copilot niet beschikbaar voor marketingtekst voor mijn artikelen in Business Central?

Copilot is alleen beschikbaar als aan de volgende vereisten wordt voldaan:

- De taal die u gebruikt in Business Central moet Engels zijn. Alle beschikbare Engelse landinstellingen werken, zoals Engels (Verenigde Staten), Engels (Verenigd Koninkrijk) of Engels (Zuid-Afrika).

  Om de taal te wijzigen, selecteert u in de rechterbovenhoek het pictogram **Instellingen** ![Instellingen](media/ui-experience/settings_icon_small.png "Pictogram Instellingen voor rolcentrum"). > **Mijn instellingen** > **Taal**. Ga voor meer informatie naar [Basisinstellingen wijzigen](ui-change-basic-settings.md#language).
- U moet de Business Central online versie 22 of hoger gebruiken (als u een bestaande klant bent) of een proefversie.  <!--**22.0.54157.54311 (Preview - Copilot edition)**-->

   Selecteer het vraagteken in de rechterbovenhoek en selecteer vervolgens **Help en ondersteuning**. Zoek onder **Problemen oplossen** naar de toepassingsversie. Ga naar [Aan de slag met een preview-versie van Business Central - Copilot-editie](ai-preview-getstarted.md) voor informatie over het verkrijgen van de juiste preview-versie.
- De functie **Op AI gebaseerde productbeschrijvingen maken met Copilot** moet zijn geactiveerd.

   Ga voor meer informatie naar [De functie "Op AI gebaseerde productbeschrijvingen maken met Copilot" in- of uitschakelen](enable-ai.md#enable-or-disable-create-ai-powered-product-descriptions-with-copilot).
- Een beheerder heeft ingestemd met de voorwaarden.

   Ga voor meer informatie naar [De preview en privacyvoorwaarden accepteren of afwijzen voor alle gebruikers](enable-ai.md#consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users).

### Is Copilot voor preview beschikbaar in Business Central on-premises?

Nee, dit wordt momenteel niet ondersteund in Business Central on-premises.

### Hoe werkt Copilot en waar komt de voorgestelde tekst vandaan?

Copilot gebruikt de [Azure OpenAI-service van Microsoft](/azure/cognitive-services/openai/overview) om toegang te krijgen tot krachtige taalmodellen die natuurlijke taal analyseren en genereren. Deze modellen zijn getraind op een groot aantal tekstgegevenssets. Hierdoor kan Copilot voorgestelde, gepersonaliseerde antwoorden in het Engels genereren op basis van een minimale hoeveelheid invoergegevens, zoals de kenmerken, categorie of beschrijving van een artikel. 

### Wat is de kwaliteit van de tekst die door Copilot wordt voorgesteld?

Omdat de onderliggende technologie achter Copilot AI gebruikt die is getraind op een breed scala aan bronnen, is de gegenereerde inhoud niet altijd feitelijk of geschikt. Sommige suggesties kunnen zelfs twijfelachtige of ongepaste inhoud bevatten. Het is uw verantwoordelijkheid om gegenereerde suggesties te bekijken en te bewerken om er zeker van te zijn dat deze nauwkeurig en gepast zijn.

Ga voor informatie over ongepaste suggesties naar [Wat wordt er gedaan aan beledigende en schadelijke tekstsuggesties?](/dynamics365/business-central/ai-faq?&tabs=oversight#whats-done-about-abusive-and-harmful-text-suggestions).

### Hoe kan ik de suggesties die ik krijg van Copilot verbeteren?

Er zijn een paar dingen die u kunt doen om de suggesties van Copilot optimaal te benutten:

- Voeg meer kenmerken toe aan een artikel om de specifieke functies en eigenschappen waarin u geïnteresseerd bent te promoten.
- Pas de opties voor de toon van de stem en de nadruk op kwaliteit aan uw persoonlijke voorkeuren aan.
- Verbeter de beschrijving van een artikel.
- Zorg ervoor dat het artikel in de meest geschikte categorie wordt ingedeeld.

Ga voor meer informatie naar [Tekstsuggesties verbeteren en aanpassen](item-marketing-text.md#improve-and-tailor-text-suggestions).

### Wat als ik niet tevreden ben met de gegenereerde tekst?

Selecteer **Is dit een goede suggestie?** op de pagina **Maken met Copilot** om ons te helpen de tekst te verbeteren. U kunt antwoorden met een duim omhoog (vind ik leuk) of duim omlaag (moet worden verbeterd).

![Toont een artikelkaart met het deelvenster Marketingtekst](media/create-with-copilot-window-feedback.png)

### Kunnen beheerders Copilot uitschakelen? Zo ja, hoe?

Business Central biedt beheerders twee manieren om Copilot in de preview uit te schakelen:

- Wijs de privacyverklaring van Azure OpenAI voor alle gebruikers af.

  of

- Schakel de functie **Op AI gebaseerde productbeschrijvingen maken met Copilot** uit op de pagina **Functiebeheer**.

Ga voor meer informatie naar [Artikelmarketingtekst op basis van AI configureren (preview) met Copilot als beheerder](enable-ai.md).

## [Eerlijkheid](#tab/fairness)

### Werkt Copilot met andere talen dan Engels?

Momenteel ondersteunt Copilot alleen Engels. Onnauwkeurige antwoorden kunnen worden geretourneerd wanneer gebruikers met het systeem praten in andere talen dan het Engels.

## [Menselijk toezicht](#tab/oversight)

### Wat wordt er gedaan aan beledigende en schadelijke tekstsuggesties?

De Azure OpenAI-service slaat prompts en voltooiingen vanuit de service op om te controleren op misbruik en om de kwaliteit van de inhoudsbeheersystemen van Azure OpenAI te ontwikkelen en te verbeteren. [Meer informatie over ons inhoudsbeheer en filtering.](/azure/cognitive-services/openai/concepts/content-filter)

Geautoriseerde Microsoft-medewerkers hebben toegang tot uw prompt- en voltooiingsgegevens die onze geautomatiseerde systemen hebben geactiveerd voor het onderzoeken en verifiëren van mogelijk misbruik; voor klanten die de Azure OpenAI-service in de Europese Unie hebben geïmplementeerd, zullen de geautoriseerde Microsoft-medewerkers zich in de Europese Unie bevinden. Deze gegevens kunnen worden gebruikt om onze inhoudsbeheersystemen te verbeteren. In het geval van een bevestigde beleidsschending kunnen we u vragen om onmiddellijk actie te ondernemen om het probleem op te lossen en om verder misbruik te voorkomen. Als het probleem niet wordt verholpen, kan de toegang tot Azure OpenAI-bronnen worden opgeschort of beëindigd.

Zie [Gegevens, privacy en beveiliging voor de Azure OpenAI-service](/legal/cognitive-services/openai/data-privacy#abuse-and-harmful-content-generation) voor meer informatie.

### Kan ik me afmelden voor het vastleggen en het menselijke beoordelingsproces?  

Als onderdeel van het leveren van de Azure Open AI-previews, verwerkt en bewaart Microsoft klantgegevens die bij de service zijn ingediend, evenals uitvoerinhoud, met als doel toezicht te houden op misbruik of schadelijk gebruik of uitvoer van de service en dit te voorkomen; en voor het ontwikkelen, testen en verbeteren van mogelijkheden die zijn ontworpen om misbruik van en schadelijke uitvoer van de service te voorkomen. 

Geautoriseerd Microsoft-personeel kan gegevens bekijken die onze geautomatiseerde systemen hebben geactiveerd om mogelijk misbruik te onderzoeken en te verifiëren, en kan een beperkte willekeurige steekproef nemen van termen die niet door onze geautomatiseerde systemen zijn gemarkeerd om ervoor te zorgen dat de systemen correct werken. Geautoriseerd Microsoft-personeel heeft ook toegang tot deze gegevens en kan deze gebruiken om onze systemen te verbeteren die misbruik of schadelijk gebruik of uitvoer van de service controleren en voorkomen. Lees meer op [preview-voorwaarden](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/)

## [Privacy](#tab/privacy)

### Welke gegevens worden door de functie verzameld? Hoe worden de gegevens gebruikt?

De functie verzamelt uw antwoord op de vraag **Is dit een goede suggestie?** op de pagina **Maken met Copilot**. U kunt antwoorden met een duim omhoog (vind ik leuk) of duim omlaag (moet worden verbeterd).

We gebruiken deze gegevens om de kwaliteit van de functie te beoordelen en te verbeteren. Meer informatie over welke gegevens worden verzameld, vindt u in de [preview-voorwaarden](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

![Toont een artikelkaart met het deelvenster Marketingtekst](media/create-with-copilot-window-feedback.png)

---

## Zie ook

[Overzicht van op AI gebaseerde artikelmarketingtekst met Copilot configureren](ai-overview.md)  
[Op AI gebaseerde artikelmarketingtekst met Copilot configureren als beheerder](enable-ai.md)  
[Marketingteksten voor artikelen maken met Copilot](item-marketing-text.md)  

