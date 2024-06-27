---
title: Veelgestelde vragen over hulp bij bankrekeningreconciliatie met Copilot (preview)
description: 'Deze veelgestelde vragen bieden informatie over de AI-technologie die wordt gebruikt voor het reconciliëren van bankrekeningen en afschriften in Business Central. Het bevat belangrijke overwegingen en details over hoe AI wordt gebruikt, hoe het is getest en geëvalueerd en eventuele specifieke beperkingen.'
ms.date: 03/27/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI'
ms.collection:
  - bap-ai-copilot
---

# Veelgestelde vragen over hulp bij bankrekeningreconciliatie met Copilot (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Deze veelgestelde vragen (FAQ) beschrijven de AI-impact van Microsoft Copilot-hulp bij bankrekeningreconciliatie in [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## Wat is hulp bij bankreconciliatie?

Bankreconciliatie is een veel voorkomende boekhoudkundige taak waarbij organisaties hun bankrekeningafschriften controleren om transacties te identificeren die moeten worden geregistreerd in [!INCLUDE[prod_short](includes/prod_short.md)]. Deze taak wordt bijvoorbeeld gebruikt om periodieke bankkosten of kleine personeelskosten te identificeren.

Bankafstemming is doorgaans een proces dat uit meerdere stappen bestaat. Eerst worden bankafschriften geïmporteerd in [!INCLUDE[prod_short](includes/prod_short.md)]. Vervolgens worden transacties afgestemd met grootboekposten. Ten slotte worden nieuwe grootboekposten geboekt om eventuele resterende transacties weer te geven die voorheen niet bekend waren in uw grootboeken.

Copilot in [!INCLUDE[prod_short](includes/prod_short.md)] vermindert de handmatige inspanning door meer transacties af te stemmen en grootboekrekeningen voor te stellen waarnaar u kunt boeken.

## Wat zijn de mogelijkheden van hulp bij bankreconciliatie?

Copilot biedt AI-aangedreven hulp met twee verschillende taken:

- Verbeterde afstemming van transacties met grootboekposten

    [!INCLUDE[prod_short](includes/prod_short.md)] biedt geautomatiseerde regels die veel banktransacties automatisch afstemmen met grootboekposten. Deze regels zijn echter inflexibel en resulteren vaak in veel niet-afgestemde transacties die allemaal handmatige inspectie en vergelijking vereisen. Copilot gebruikt AI-technologie om deze niet-afgestemde transacties te inspecteren en meer overeenkomsten te identificeren, op basis van de datums, bedragen en beschrijvingen. Als een klant bijvoorbeeld meerdere facturen als één lump-sum heeft betaald, stemt Copilot de afzonderlijke bankafschriftregel af met de meerdere factuurposten.

- Voorgestelde grootboekrekeningen

    Voor resterende banktransacties die niet met grootboekposten kunnen worden afgestemd, gebruikt Copilot AI-technologie om de transactiebeschrijving te vergelijken met grootboekrekeningnamen en worden vervolgens de meest waarschijnlijke grootboekrekeningen voorgesteld om naar te boeken. A;s niet-afgestemde transacties bijvoorbeeld vallen onder *Brandstofstop 24*, kan Copilot bijvoorbeeld voorstellen dat u ze boekt naar het account *Transport*.

Copilot maakt geen verbinding met uw bank om transacties op te halen of te verzenden. Deze taak blijft volledig binnen uw controle. Dat is een voorwaarde om de hulp van Copilot te gaan gebruiken, ongeacht of de transacties worden toegevoegd aan [!INCLUDE[prod_short](includes/prod_short.md)] via een digitale bankverbinding, geïmporteerd uit een bankafschriftbestand of handmatig ingevoerd.

## Wat is het beoogde gebruik van de hulp bij bankreconciliatie?

Hulp bij bankrekeningreconciliatie is bedoeld om de accuratesse van grootboeken te vergroten door klanten te helpen nieuwe transacties te identificeren waar klanten rekening mee moeten houden in [!INCLUDE[prod_short](includes/prod_short.md)]. Dit is niet bedoeld voor het opsporen van fraude of het vaststellen of klanten op tijd hebben betaald.

## Hoe werd de hulp bij bankreconciliatie beoordeeld? Welke statistieken worden gebruikt om de prestaties te meten?

Hulp bij reconciliatie van bankrekeningen is getest met combinaties van synthetische banktransactiegegevens en vergelijkbare grootboekrekeningen en grootboekposten die de typische variaties en gegevenslimieten voor elk veld en in verschillende talen dekken. Testgegevens vertegenwoordigen zowel typisch gebruik als gebruik door slechte actoren. De prestaties werden gemeten in vergelijking met handmatige reconciliatie van dezelfde gegevens.

## Wat zijn de beperkingen van bij bankreconciliatie? Hoe kunnen gebruikers de impact van de beperkingen tot een minimum terugbrengen bij het gebruik van het systeem?

Hulp bij het reconciliëren van bankrekeningen werkt het beste wanneer grootboekrekeningnamen, beschrijvingen van grootboekposten en beschrijvingen van banktransacties allemaal in dezelfde taal zijn. Gemengde talen of gemengde taal van transactiebeschrijvingen resulteren vaak in minder overeenkomsten en suggesties.

Voorgestelde grootboekrekeningen presteren het beste in een van de ondersteunde talen (zie de volgende sectie voor een lijst met talen). Gebruikers ervaren mogelijk minder transactieovereenkomsten en minder voorgestelde grootboekrekeningen in andere talen.

## In welke geografieën en talen is hulp bij bankreconciliatie beschikbaar? 

- Beschikbare geografische gebieden

  Hulp bij het afstemmen van bankrekeningen is beschikbaar in alle ondersteunde [Business Central-landen/-regio's](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations). Voor klantomgevingen in landen/regio's waar de Azure OpenAI-service niet wordt geïmplementeerd, moeten beheerders toestemming geven om verplaatsing van hun gegevens over de grenzen heen toe te staan voor [!INCLUDE [prod_short](includes/prod_short.md)] om verbinding te maken met de Azure OpenAI-service. Meer informatie op [Copilot-gegevensverplaatsing tussen geografieën](ai-copilot-data-movement.md).

- Beschikbare talen

  [!INCLUDE[bank-recon-assist-language-support](includes/bank-recon-assist-language-support.md)]

Zie de vorige vraag over beperkingen voor meer informatie over talen.

## Wat wordt er van systeemgebruikers verwacht bij het gebruik van hulp bij bankrekeningreconciliatie?

### Tijdens bankrekeningreconciliatie

Afstemmingen en suggesties op basis van AI kunnen soms onjuist of onvolledig zijn. Gebruikers van hulp bij bankrekeningreconciliatie moeten de nauwkeurigheid van de afstemmingen en suggesties van Copilot controleren voordat ze ervoor kiezen deze te behouden. Afstemmingen en suggesties van Copilot worden pas in de [!INCLUDE[prod_short](includes/prod_short.md)]-database opgeslagen als u de knop **Behouden** selecteert en het Copilot-venster sluit. U kunt ook eventuele afstemmingen of suggesties bewerken en corrigeren voordat u ervoor kiest deze te behouden.

### Na voltooiing van bankrekeningreconciliatie

We raden gebruikers aan ook de nauwkeurigheid te verifiëren en eventuele discrepanties te corrigeren nadat ze het Copilot-venster hebben gesloten. Dit proces moet de volgende activiteiten omvatten:

- Bekijk het reconciliatietestrapport.
- Zorg ervoor dat uw organisatie over de juiste beoordelings- en controleprocessen beschikt.
- Open eventuele geboekte reconciliaties opnieuw met behulp van de functie **Ongedaan maken**.
- Corrigeer eventuele foutieve grootboekposten door posten tegen te boeken.

## Wat wordt er van beheerders en systeemgebruikers verwacht bij het gebruik van hulp bij bankrekeningreconciliatie?

Systeemgebruikers, zoals accountants, penningmeesters of anderen die aan de bedrijfsboekhouding werken, moeten altijd de juistheid van afstemmingen en suggesties van Copilot controleren voordat ze ervoor kiezen deze te behouden. Na reconciliatie met Copilot raden we aan dat deze gebruikers het reconciliatietestrapport bekijken om de nauwkeurigheid te verifiëren en eventuele discrepanties te identificeren.

Beheerders moeten ervoor zorgen dat de juiste accountinggebruikers toegang hebben gekregen tot deze mogelijkheid.

## Is Copilot het enige middel om bankrekeningreconciliatie te voltooien?

Nr. Gebruik van Copilot is optioneel. [!INCLUDE[prod_short](includes/prod_short.md)] biedt traditionele, niet door AI aangedreven middelen voor het importeren van bankafschriften, het uitvoeren van vooraf gedefinieerde afstemmingsregels en het handmatig toepassen van afstemmingen en boeken naar de juiste grootboekrekeningen. Zowel de traditionele aanpak als Copilot kunnen gelijktijdig binnen een organisatie worden ingezet.

## Hoe geef ik feedback over door AI gegenereerde inhoud?

Elke keer dat Copilot afstemmingen of suggesties levert, kunt u rechtstreeks vanuit het Copilot-venster feedback aan Microsoft geven met behulp van de besturingselementen Vind ik leuk (duim omhoog) en Niet leuk (duim omlaag). Uw feedback blijft anoniem en wij gebruiken deze gegevens om de kwaliteit van de dienstverlening te verbeteren.

## Zie ook

[Bankrekeningen reconciliëren met Copilot (preview)](bank-reconciliation-with-copilot.md)
