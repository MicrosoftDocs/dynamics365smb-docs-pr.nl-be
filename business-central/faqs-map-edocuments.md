---
title: Veelgestelde vragen over het toewijzen van e-documenten aan inkooporders
description: 'Deze veelgestelde vragen geven informatie over de AI-technologie die wordt gebruikt in Business Central, samen met belangrijke overwegingen en details over hoe AI wordt gebruikt, hoe deze werd getest en geëvalueerd, en eventuele specifieke beperkingen.'
ms.date: 02/23/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.collection:
  - bap-ai-copilot
---

# <a name="faq-for-mapping-e-documents-with-purchase-orders-using-copilot-preview"></a>Veelgestelde vragen over het toewijzen van e-documenten aan inkooporders met Copilot (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Deze veelgestelde vragen (FAQ) beschrijven de AI-impact van de functie **Hulp bij afstemming van e-document** in [!INCLUDE [prod_short](includes/prod_short.md)].

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-e-documents-matching-assistance"></a>Wat houdt Hulp bij afstemming van e-document in?

Elektronische documenten (e-documenten) dienen als het fundament van moderne zakelijke transacties. Ze vertegenwoordigen kritisch papierwerk, zoals facturen en bonnen, die via levering en ontvangst in beide richtingen stromen. U kunt elektronische facturen digitaal genereren en verzenden in een gestructureerde indeling die geautomatiseerde factuurverwerking mogelijk maakt. Voor crediteurenteams kan het verwerken van inkomende digitale facturen echter ingewikkelder zijn.  

In het midden- en kleinbedrijf (MKB) speelt het crediteurenteam een cruciale rol bij het nauwkeurig bijhouden van de verplichtingen van leveranciers. Hun primaire verantwoordelijkheid is het nauwkeurig registreren van inkomende facturen. Het bereiken van precisie kan inspanning vergen, vooral wanneer externe facturen van leveranciers worden afgestemd op bestaande inkooporders. Discrepanties in codes, beschrijvingen en meeteenheden vormen vaak een uitdaging omdat deze elementen mogelijk niet overeenkomen in verschillende systemen en bedrijven. Ook kunnen onverwachte kosten, zoals transportkosten, worden weergegeven als afzonderlijke regelitems die handmatig moeten worden aangepast. Accountants moeten ook factuurnummers en datums in de documenten opnemen. Belangrijk is dat de relatie tussen inkooporders en externe facturen niet altijd één-op-één is. Het kan zijn dat u meerdere externe facturen ontvangt voor dezelfde inkooporder.

In het verleden kon [!INCLUDE [prod_short](includes/prod_short.md)] nieuwe inkoopfacturen genereren op basis van ontvangen elektronische facturen. Het handmatig afstemmen van facturen met bestaande inkooporders was echter een tijdrovend en foutgevoelig proces.

**Hulp bij afstemming van e-document** gebruikt generatieve AI om dit proces te stroomlijnen door de analyse van externe elektronische facturen te automatiseren. Met de functie kunnen accountants Copilot vragen om regels op inkomende elektronische facturen af te stemmen met regels op inkooporders in [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="what-are-capabilities-of-the-e-documents-matching-assistance"></a>Wat zijn de mogelijkheden van Hulp bij afstemming van e-document?

Copilot biedt door AI aangestuurde hulp om ontvangen digitale facturen af te stemmen met bestaande inkooporders in [!INCLUDE [prod_short](includes/prod_short.md)]. Copilot stemt regels af op basis van het volgende:

- Overeenkomst van beschrijvingen
- Maateenheden
- Hoeveelheden beschikbaar voor facturering
- Bedragen

Copilot identificeert vergelijkbare beschrijvingen als ze de juiste maateenheden en prijzen hebben, maar kan ook overeenkomsten vinden in complexere gevallen. Copilot kan bijvoorbeeld identificeren of een elektronische factuur twee regels heeft met een variant van hetzelfde artikel, en slechts één regel in de inkooporder. Met [!INCLUDE [prod_short](includes/prod_short.md)] worden deze regels afgestemd zolang de beschrijvingen vergelijkbaar zijn en de prijzen hetzelfde zijn.

Copilot maakt geen verbinding met uw eindpuntservice voor e-documenten om digitale bonnen op te halen of te verzenden. Deze taak blijft volledig binnen uw controle en is een voorwaarde om gebruik te kunnen maken van de hulp van Copilot. Dit geldt ongeacht of de digitale documenten worden toegevoegd aan [!INCLUDE [prod_short](includes/prod_short.md)] via een verbinding met een eindpuntservice, of handmatig worden ingevoerd.  

## <a name="what-is-the-intended-use-of-the-e-documents-matching-assistance"></a>Wat is het beoogde gebruik van Hulp bij afstemming van e-document?

Het doel van de functie **Hulp bij afstemming van e-document** is om het crediteurenteam te helpen bestaande inkooporders af te stemmen met inkomende elektronische facturen. Een groot deel van deze activiteit draait om het afstemmen van tekenreeksen. [!INCLUDE [prod_short](includes/prod_short.md)] biedt een functie die een deel van deze activiteit automatiseert, en LLM's zijn geïdentificeerd als een mogelijkheid om die functie aan te vullen en de handmatige inspanning verder te verminderen.  

## <a name="how-was-e-documents-matching-assistance-evaluated-what-metrics-are-used-to-measure-performance"></a>Hoe is Hulp bij afstemming van e-document beoordeeld? Welke statistieken worden gebruikt om de prestaties te meten?

Deze functie is getest met combinaties van de volgende gegevens:

- Externe artikelbeschrijvingen
- Maateenheden
- Hoeveelheden en bedragen
- Standaard artikelbeschrijvingen
- Verschillende talen
- Andere parameters die de typische variaties en gegevenslimieten voor elk veld dekken 

Testgegevens vertegenwoordigen zowel typisch gebruik als gebruik door slechte actoren. De prestaties zijn gemeten in vergelijking met het handmatig afstemmen van dezelfde gegevens op elektronische facturen en inkooporders.

## <a name="what-are-the-limitations-of-e-documents-matching-assistance-how-can-users-minimize-the-impact-of-the-e-documents-matching-assistance-limitations-when-using-the-system"></a>Wat zijn de beperkingen van Hulp bij afstemming van e-document? Hoe kunnen gebruikers de impact van de beperkingen van Hulp bij afstemming van e-document minimaliseren bij het gebruik van het systeem?

**Hulp bij afstemming van e-document** presteert het beste wanneer externe (e-factuur) en interne ([!INCLUDE [prod_short](includes/prod_short.md)]) artikelbeschrijvingen en maateenheden allemaal in dezelfde taal zijn. Gemengde talen of gemengde taal van artikelbeschrijvingen resulteren vaak in minder overeenkomsten en suggesties.  

Voorgestelde afstemming van artikelen van e-facturen met artikelen in inkooporders werkt het beste in het Engels. Hoewel u deze functie kunt gebruiken in elke taal die [!INCLUDE [prod_short](includes/prod_short.md)] ondersteunt, kunt u in andere talen mogelijk minder artikelovereenkomsten tegenkomen. Voor meer informatie over taal gaat u naar [In welke geografieën en talen is Hulp bij afstemming van e-document beschikbaar?](#in-which-geographies-and-languages-is-e-documents-matching-assistance-available).

## <a name="in-which-geographies-and-languages-is-e-documents-matching-assistance-available"></a>In welke geografieën en talen is Hulp bij afstemming van e-document beschikbaar?

- Beschikbare geografische gebieden

   Deze Copilot-functie is beschikbaar in alle ondersteunde [Business Central-landen/regio's](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations). Voor klantomgevingen in landen/regio's waar de Azure OpenAI-service niet wordt geïmplementeerd, moeten beheerders echter eerst toestemming geven om verplaatsing van hun gegevens over de grenzen heen toe te staan voor [!INCLUDE [prod_short](includes/prod_short.md)] om verbinding te maken met de Azure OpenAI-service. Meer informatie op [Copilot-gegevensverplaatsing tussen geografieën](ai-copilot-data-movement.md).

- Beschikbare talen

   [!INCLUDE[e-docs-matching-language-support](includes/e-docs-matching-language-support.md)]

## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-feature"></a>Welke operationele factoren en instellingen maken een effectief en verantwoordelijk gebruik van de functie mogelijk?

Met Copilot wordt het toewijzingsalgoritme aangevuld dat [!INCLUDE [prod_short](includes/prod_short.md)] al biedt en worden de regels toegewezen die het algoritme niet heeft toegewezen.

### <a name="what-is-expected-of-users-while-using-e-documents-matching-assistance"></a>Wat wordt er van gebruikers verwacht bij het gebruik van Hulp bij afstemming van e-document?

<!--Not sure that this is the right content for this section. Seems like it belongs more in the overview article because it's more related to how to use the feature-->

Nadat u inkomende elektronische facturen met inkooporders hebt toegewezen, moet u de regels op de documenten toewijzen.

Op de pagina **Inkoopordertoewijzing** worden alle regels uit beide documenten weergegeven. Hier kunt u de toewijzing handmatig uitvoeren, wat lastig kan zijn als er veel regels zijn.

U kunt **Hulp bij afstemming van e-document** gebruiken om regels toe te wijzen op basis van de volgende criteria:

- Overeenkomst in de beschrijvingen ervan
- Maateenheden
- Hoeveelheden beschikbaar voor facturering
- Bedragen

De afstemmingen van Copilot kunnen onjuist of onvolledig zijn. U moet altijd de juistheid ervan controleren voordat u ervoor kiest ze te behouden. De afstemmingen en suggesties van Copilot worden opgeslagen in [!INCLUDE [prod_short](includes/prod_short.md)] wanneer u **Behouden** kiest en Copilot afsluit. U kunt ook eventuele afstemmingen of suggesties bewerken en corrigeren voordat u ervoor kiest deze te behouden. 

### <a name="what-is-expected-of-administrators-and-users-when-operating-e-documents-matching-assistance"></a>Wat wordt er van beheerders en gebruikers verwacht bij het gebruik van Hulp bij afstemming van e-document?

Gebruikers, zoals accountants of anderen die e-facturen ontvangen, moeten altijd de juistheid van afstemmingen en suggesties van Copilot controleren voordat ze ervoor kiezen deze te behouden. We raden u aan de inkooporderregels te controleren om de juistheid ervan te verifiëren en eventuele verschillen op te sporen. U beslist of u gebruik wilt maken van **Hulp bij afstemming van e-document**. Zelfs als de functie **Hulp bij afstemming van e-document** is ingeschakeld door beheerders en beschikbaar is, kunt u er nog steeds voor kiezen deze altijd, soms of nooit te gebruiken.  

Beheerders nemen de algemene beslissing over het al dan niet gebruiken van Copilot in [!INCLUDE [prod_short](includes/prod_short.md)]. Als beheerders Copilot inschakelen, moeten ze ervoor zorgen dat ze toegang verlenen aan de juiste gebruikers.

> [OPMERKING!]
> - We ondersteunen de functie niet voor [!INCLUDE [prod_short](includes/prod_short.md)] on-premises of in privéclouds.
> - Partners kunnen deze functie niet uitbreiden. Partnerontwikkelaars kunnen deze functie niet wijzigen, vervangen of uitbreiden. 

## <a name="is-copilot-the-only-way-to-match-e-documents-to-purchase-orders"></a>Is Copilot de enige manier om e-documenten af te stemmen met inkooporders?

Nee, het is aan u of u Copilot gebruikt. [!INCLUDE [prod_short](includes/prod_short.md)] biedt niet door AI aangestuurde manieren om artikelen van ontvangen elektronische facturen af te stemmen met artikelen op inkooporders in [!INCLUDE [prod_short](includes/prod_short.md)]. Organisaties kunnen ook beide benaderingen tegelijkertijd gebruiken.  

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Hoe geef ik feedback over door AI gegenereerde inhoud?

Elke keer dat Copilot afstemmingen of suggesties levert, kunt u rechtstreeks vanuit het Copilot-venster feedback aan Microsoft geven met behulp van de besturingselementen **Vind ik leuk** en **Niet leuk**. Uw feedback blijft anoniem en wij gebruiken deze gegevens om de kwaliteit van de dienstverlening te verbeteren.  

## <a name="see-also"></a>Zie ook

[Overzicht van e-documenten](finance-edocuments-overview.md)  
[E-documenten toewijzen aan inkooporderregels met Copilot](map-edocuments-with-copilot.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
