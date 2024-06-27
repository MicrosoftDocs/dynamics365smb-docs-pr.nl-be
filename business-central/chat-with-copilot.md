---
title: Chatten met Copilot (preview)
description: Meer informatie over hoe u chatten met Copilot kunt gebruiken om gegevens te vinden en hulp te krijgen in Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 06/13/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
  - get-started
---

# <a name="chat-with-copilot-preview"></a>Chatten met Copilot (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

In dit artikel wordt uitgelegd hoe u met Copilot kunt chatten om antwoorden te krijgen over uw bedrijfsgegevens en hulp bij taken en onderwerpen met betrekking tot Business Central.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="about-chat-with-copilot"></a>Informatie over chatten met Copilot

Microsoft Copilot is de door AI aangestuurde assistent die de creativiteit stimuleert, de productiviteit verhoogt en vervelende taken elimineert. U kunt met Copilot in Business Central chatten om vragen te stellen en bedrijfsgegevens te vinden met behulp van natuurlijke taal. U kunt het volgende doen:

- Bedrijfsgegevens zoeken voor uw bedrijf in Business Central. Chatten gebruiken om gegevens op te zoeken (en te openen) over entiteiten/records die verband houden met bedrijfsprocessen, zoals klanten, leveranciers, verkooporders en artikelen, en meer. Vraag Copilot bijvoorbeeld: "Laat mij de laatste verkooporder voor Adatum zien."
- Uitleg of stapsgewijze begeleiding krijgen bij verschillende taken. Vraag bijvoorbeeld 'Help me dimensies te begrijpen' of 'Hoe plaats ik een verkooporder'.
- Het doel en het typische gebruik van individuele velden begrijpen. Wanneer u **Copilot vragen** in de knopinfo van een veld kiest, wordt de chat geopend met een uitlegprompt voor de veldnaam en geeft Copilot informatie hierover. Copilot geeft een koppeling naar de artikelen waarnaar wordt verwezen, zodat u de beschrijving eenvoudig kunt verifiëren.

De antwoorden van Copilot zijn gebaseerd op de officiële informatie die beschikbaar is op Microsoft Learn op [Dynamics 365 Business Central-documentatie](/dynamics365/business-central/).
  
Het gebruik van chat met Copilot stroomlijnt uw werkstroom door traditionele navigatie en producthulp te omzeilen.
  
> [Video bekijken](https://go.microsoft.com/fwlink/?linkid=2250609)

## <a name="prerequisites"></a>Vereisten

- Zorg ervoor dat de chatten met Copilot-mogelijkheid is geactiveerd door een beheerder. [Meer informatie over het configureren van Copilot- en AI-mogelijkheden](enable-ai.md).
- Stel uw weergavetaal in Business Central in op een van de volgende Engelse landinstellingen: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA. [Meer informatie over het wijzigen van de taal](ui-change-basic-settings.md#language).
- Uw Business Central-omgeving kan zich in elk land/regio bevinden behalve Canada (deze functie is nog niet beschikbaar in Canada).

## <a name="get-started-using-chat-with-copilot"></a>Ga aan de slag met chatten met Copilot

1. Selecteer in de rechterbovenhoek van het scherm het pictogram ![Toont het pictogram voor chatten met Copilot](media/chat-copilot-icon.png) **Copilot** ![Toont toelichtingsnummer 1](media/callout-number-1.svg).

   Het deelvenster **Copilot** verschijnt zoals weergegeven in de afbeelding:
   
    ![Toont het pictogram voor het deelvenster voor chatten met Copilot met toelichtingen](media/chat-with-copilot-pane.svg)

1. Voer in het vak **Een vraag stellen** onderaan ![Toont toelichtingsnummer 2](media/callout-number-2.svg) uw vraag in en selecteer vervolgens de pijlpunt of druk op <kbd>Enter</kbd> om een antwoord te krijgen.

   Uw invoer, ook wel een *prompt* genoemd, kan een vraag, verklaring of opdracht zijn.

   > [!TIP]
   > Copilot bevat een aantal functies die u kunnen helpen bij het schrijven van vragen:
   > - Om aan de slag te gaan met het formuleren van een vraag, selecteert u een van de promptguides&mdash;**Zoeken**, **Uitleggen** of **Guide**&mdash;beschikbaar boven in het deelvenster ![Toont toelichtingsnummer 3](media/callout-number-3.svg) of via het pictogram ![Toont pictogram Promptguide](media/prompt-guide-icon.png) **Prompts weergeven** boven het vak **Een vraag stellen** ![Toont toelichtingsnummer 4](media/callout-number-4.svg). Promptguides zijn vooraf gedefinieerde korte zinnen waarmee een vraag of prompt begint. Ze besparen u tijd, sturen de antwoorden van Copilot naar een categorie antwoorden en helpen u te leren hoe u vragen kunt formuleren om de beste antwoorden te krijgen.
   > - Selecteer de promptsuggesties boven de knop **Prompts weergeven** ![Toont toelichtingsnummer 5](media/callout-number-5.svg) om automatisch een vooraf gedefinieerde vraag te stellen om te zien hoe de vragen en antwoorden werken. Promptsuggesties zijn alleen beschikbaar als u het voorbeeldbedrijf CRONUS gebruikt.

1. Bekijk de antwoorden die worden weergegeven in het Copilot-deelvenster ![Toont toelichtingsnummer 6](media/callout-number-6.svg).

   Afhankelijk van uw vraag kan het antwoord tekst, koppelingen naar records of pagina's in Business Central bevatten, en koppelingen naar Help-artikelen van Business Central in Microsoft Learn.

1. Stel nog een vraag om het antwoord te verfijnen.

   Chat onthoudt de context, waardoor u belangrijke punten uit de oorspronkelijke vraag niet hoeft te herhalen.

## <a name="clear-chat-to-start-over"></a>Chat wissen om opnieuw te beginnen

Als u met Copilot naar een ander gespreksonderwerp wilt overschakelen, selecteert u het pictogram ![Toont het pictogram Chat wissen](media/clear-chat-icon.png) **Een nieuwe Copilot-chatsessie starten** onder aan het Copilot-deelvenster boven het vraagvak. Met deze actie wordt uw laatste paar berichten uit het geheugen van Copilot gewist. Opnieuw beginnen is vaak nuttig na een langdurig gesprek met veel berichten, en het kan Copilot helpen nauwkeurigere antwoorden te geven.

De chat wordt ook gewist als u Business Central sluit of afmeldt.

## <a name="tips-for-better-questions"></a>Tips voor betere vragen

Hier zijn enkele manieren waarop u de antwoorden die u van Copilot krijgt, kunt verbeteren:

- Stel duidelijke en gerichte vragen.
- Wees beknopt en vermijd lange zinnen of meerdere zinnen.
- Stel één vraag tegelijk. <!--Avoid asking about multiple questions in one message.-->
- Gebruik natuurlijke taal waarbij u de vragen op een vriendelijke en gemoedelijke manier uitdrukt.
- Gebruik trefwoorden, woordgroepen en termen waarvan u weet dat ze in Business Central worden gebruikt, hetzij in de app, hetzij in de documentatie.
- Als het eerste antwoord uw vragen niet volledig beantwoordt, stel dan vervolgvragen of herformuleer de laatste vraag.
- Als u een vraag stelt over een ander onderwerp dan de vorige vraag, wis dan de huidige chatsessie om opnieuw te beginnen.

## <a name="example-prompts"></a>Voorbeeldprompts

Uw vragen aan Copilot variëren uiteraard afhankelijk van uw rol, huidige taak, de processen die uw organisatie volgt en hoe u zich in woorden uitdrukt. Hieronder volgen voorbeelden van verschillende manieren om vragen te stellen in het chatvenster, die u kunnen inspireren om uw eigen vragen te schrijven op basis van uw eigen unieke situatie.

Prompt: `Find the Item with Description 'ATHENS Desk'`

In dit voorbeeld geeft u duidelijke instructies aan Copilot om één record te lokaliseren. U geeft bijvoorbeeld aan dat de record in het artikeloverzicht te vinden is. U geeft aan dat het veld 'Omschrijving' een specifieke tekst moet zijn die u met aanhalingstekens en met correct hoofdlettergebruik hebt getypt. Copilot reageert meestal accuraat als een paar precieze hints worden gegeven, maar u kunt ook wat informeler taalgebruik hanteren, zoals in het volgende voorbeeld.

Prompt: `Give me the latest invoice for adatum`

In dit voorbeeld vraagt u Copilot om een record te lokaliseren, maar de vraag is minder nauwkeurig en kan resulteren in een minder nauwkeurig antwoord. Copilot kan vaak begrijpen (of raden) dat de factuur die u zoekt geen inkoopfactuur is, maar een verkoopfactuur uit de lijst Geboekte verkoopfacturen. Copilot moet ook `adatum` matchen met `Adatum Corporation` en dat is de volledige en precieze naam voor de orderklant die aan de factuur is gekoppeld.

Prompt: `Show me customer ledger entries for Adatum from about three weeks ago`

In dit voorbeeld vraagt u de Copilot een vaak voorkomende datumpuzzel op te lossen, waarbij u doorgaans een kalender ter referentie moet openen of geavanceerde datumbereikfilters moet gebruiken. Copilot kan doorgaans algemene uitdrukkingen en zakelijke termen begrijpen.

Prompt: `How does I save my filterrings for later?`

In dit voorbeeld vraagt u Copilot om begeleiding bij het uitvoeren van een bepaalde taak in Business Central. Copilot begrijpt meestal de bedoeling van uw vraag, zelfs als er enkele grammaticale fouten, spelfouten of afkortingen in voorkomen.

## <a name="provide-feedback-on-answers"></a>Feedback geven op antwoorden

U kunt de antwoorden die u krijgt van Copilot beoordelen door de knop Vind ik leuk (duim omhoog) te gebruiken voor een goede beoordeling of de knop Niet leuk (duim omlaag) voor een slechte beoordeling. Wanneer u de knop 'Niet leuk' selecteert, kunt u een reden kiezen, waaronder onnauwkeurig, ongepast of iets anders. Deze informatie kan ons helpen suggesties te verbeteren.

<!--
1. If you want help getting you're question started, select the prompts either from the **Find**, **Explain**, or **Guide** buttons at the top of the Coplit pane or use the **View Prompts** menu above **Ask a question** box at the bottom.

   Prompts are predefined short phrases that start a question. Apart from saving you time, they're designed to target responses to specific categories. They also help you undestand how you can phrase questions to get the responses.-->
   
## <a name="see-also"></a>Zie ook

- [Problemen oplossen met Copilot- en AI-mogelijkheden](ai-copilot-troubleshooting.md)  
- [Copilot- en AI-mogelijkheden configureren](enable-ai.md)  
- [Veelgestelde vragen over verantwoorde AI voor chatten met Copilot](faqs-chat-with-copilot.md)  
- [Resources voor hulp in Business Central](product-help-and-support.md)  
