---
title: Veelgestelde vragen over chatten met Copilot
description: In dit artikel worden enkele veelgestelde vragen beantwoord over chatten met Copilot in Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 05/17/2024
ms.custom: bap-template jswymer
---
# <a name="chat-with-copilot-faq"></a>Veelgestelde vragen over chatten met Copilot

[!INCLUDE[preview-banner](includes/preview-banner.md)]

In dit artikel worden enkele veelgestelde vragen beantwoord over chatten met Copilot in [!INCLUDE[prod_short](includes/prod_short.md)]. Voor vragen over AI en chatten raadpleegt u [Veelgestelde vragen over verantwoorde AI voor chatten met Copilot](faqs-chat-with-copilot.md).

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="can-admins-grant-or-deny-permission-to-individual-users-to-get-access-to-chat"></a>Kunnen beheerders individuele gebruikers toestemming geven of weigeren om toegang te krijgen tot de chat?

Nee, er is geen toestemming of machtiging ingesteld voor chatten. Als chatten is geactiveerd op de pagina [Copilot en AI-mogelijkheden](enable-ai.md), heeft elke gebruiker in een omgeving toegang tot chatten.
 
## <a name="is-chat-available-on-tablet-phone-or-other-form-factors"></a>Is chatten beschikbaar op tablet, telefoon en dergelijke?

Nee, het chatvenster is alleen beschikbaar via de [!INCLUDE[web_client](includes/web_client.md)]-webclient.

## <a name="i-dont-use-business-central-in-english-what-are-my-options"></a>Ik gebruik Business Central niet in het Engels. Wat zijn mijn opties?

Op dit moment is chatten alleen beschikbaar in het Engels. U kunt uw gebruikerstaal wijzigen in het Engels via [Mijn instellingen](ui-change-basic-settings.md#language).

## <a name="which-business-central-version-do-i-need-to-experience-chat"></a>Welke Business Central-versie heb ik nodig om te kunnen chatten?

Chatten is beschikbaar in de openbare preview vanaf versie 24.0 (releasewave 1 van 2024).

## <a name="does-chat-work-with-my-customizations"></a>Werkt chatten met mijn aanpassingen?

Het hangt af van het soort vraag dat u aan Copilot stelt. Voorbeeld:

- Wanneer u vragen stelt om records te lokaliseren, kan Copilot records in uw aangepaste tabellen vinden die worden geïdentificeerd met behulp van aangepaste velden.
- Wanneer u om uitleg of begeleiding vraagt, heeft Copilot geen toegang tot informatie over uw aanpassingen of documentatie voor uw add-ons.

## <a name="copilot-never-seems-to-open-the-record-or-page-i-asked-for-what-am-i-doing-wrong"></a>Het lijkt of Copilot nooit de record of pagina opent waar ik om vraag. Wat doe ik verkeerd?

Wanneer u Copilot vraagt om records te zoeken in [!INCLUDE[prod_short](includes/prod_short.md)], worden alle gevonden records weergegeven als selecteerbare tegels of koppelingen in het chatvenster. In de preview-versie navigeert Copilot niet automatisch naar een pagina.

## <a name="the-answers-i-get-from-copilot-vary-even-though-i-ask-the-same-question-is-it-a-bug"></a>Ook al stel ik dezelfde vraag, de antwoorden die ik van Copilot krijg variëren. Is het een bug?

Copilot kan af en toe op verschillende manieren antwoorden. Antwoorden zijn niet noodzakelijkerwijs identiek.

## <a name="when-should-i-use-the-copy-function-on-chat-messages"></a>Wanneer moet ik de kopieerfunctie in chatberichten gebruiken?

U kunt de knop Kopiëren gebruiken om een bericht van eerder in uw gesprek met Copilot te kopiëren, het in het invoervak ​​te plakken om het opnieuw te proberen of een variant van uw bericht voor Copilot te proberen.

## <a name="how-do-i-customize-or-extend-chat"></a>Hoe kan ik de chat aanpassen of uitbreiden?

In de preview-versie kunnen het chatvenster en de reacties van Copilot op geen enkele manier worden gewijzigd door middel van aanpassingen, invoegtoepassingen of personalisatie.

## <a name="does-copilot-find-data-in-other-companies-or-environments"></a>Vindt Copilot gegevens in andere bedrijven of omgevingen?

Copilot zoekt alleen naar records in het bedrijf waarbij u momenteel bent ingelogd&mdash; zelfs als uw organisatie meerdere omgevingen of bedrijven gebruikt om gegevens te scheiden.

## <a name="the-copilot-chat-pane-doesnt-show-what-can-i-do"></a>Het Copilot-chatvenster wordt niet weergegeven. Wat kan ik doen?

Controleer of uw gebruikerstaal in Mijn instellingen is ingesteld op Engels en of uw omgeving versie 24.0 of hoger heeft. Zorg ervoor dat beheerders op de pagina Copilot en AI-mogelijkheden de toestemming voor gegevens in verschillende regio's hebben ingeschakeld en de chat hebben geactiveerd. Zorg ervoor dat uw omgevingslokalisatie niet Canada is.

Als u de chatfunctie met Copilot nog steeds niet ziet, is het mogelijk dat Microsoft de functie nog steeds uitrolt naar uw regio. Copilot wordt eerst in april 2024 uitgerold naar Amerikaanse klanten en zal vervolgens in de loop van weken worden uitgerold naar andere land-/regiolokalisaties.

## <a name="why-does-copilot-only-show-three-records-in-the-chat-pane"></a>Waarom toont Copilot slechts drie records in het chatvenster?

Wanneer u Copilot vraagt ​​om records op te halen, bepaalt de manier waarop u de vraag formuleert hoe Copilot filters op pagina's identificeert en toepast om te vinden wat u zoekt. Om de antwoorden compact en beknopt te houden, worden in het chatvenster maximaal drie recordtegels weergegeven, zelfs wanneer Copilot een groter aantal relevante records vindt.

## <a name="copilot-returns-incorrect-answers-to-totals-and-other-calculations"></a>Copilot retourneert onjuiste antwoorden op totalen en andere berekeningen

In de preview-versie kan Chat met Copilot records lokaliseren, concepten uitleggen en u begeleiden bij het voltooien van taken in Business Central. Andere gebruiksscenario's worden niet ondersteund, zoals het optellen van een veld tussen records of het berekenen van het gemiddelde maandbedrag. We hopen in de toekomst elementaire wiskundige vaardigheden aan Copilot toe te voegen.

## <a name="can-i-use-speech-instead-of-typing-my-prompts"></a>Kan ik spraak gebruiken in plaats van mijn aanwijzingen te typen?

U kunt met Copilot chatten door spraakgestuurd typen te gebruiken in plaats van uw woorden in het chatvenster te typen. Spraakgestuurd typen maakt gebruik van online spraakherkenning en is beschikbaar in Windows. Om spraak te gebruiken, activeert u het chatberichtvenster, gebruikt u vervolgens de  <kbd>Windows</kbd>+<kbd>H</kbd> snelkoppeling en begint u te spreken. Zie [Gesproken typen gebruiken om te praten in plaats van te typen op uw pc voor meer informatie](https://support.microsoft.com/windows/use-voice-typing-to-talk-instead-of-type-on-your-pc-fec94565-c4bd-329d-e59a-af033fa5689f).

## <a name="next-steps"></a>Volgende stappen

[Chatten met Copilot (preview)](chat-with-copilot.md)
