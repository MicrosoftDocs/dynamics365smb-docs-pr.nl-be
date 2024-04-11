---
title: Veelgestelde vragen over hulp bij bankrekeningreconciliatie (preview) met Copilot
description: 'Deze veelgestelde vragen bieden informatie over de AI-technologie die wordt gebruikt voor het reconciliëren van bankrekeningen en afschriften in Business Central. Dit bevat belangrijke overwegingen en details over hoe AI wordt gebruikt, hoe het is getest en geëvalueerd en eventuele specifieke beperkingen.'
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

# <a name="faq-for-bank-account-reconciliation-assist-with-copilot-preview"></a>Veelgestelde vragen over hulp bij bankrekeningreconciliatie met Copilot (preview)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Deze veelgestelde vragen (FAQ) beschrijven de AI-impact van Copilot-hulp bij bankrekeningreconciliatie [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-bank-reconciliation-assist"></a>Wat is hulp bij bankreconciliatie?

Bankreconciliatie is een veel voorkomende boekhoudkundige taak waarbij organisaties hun bankrekeningafschriften controleren om transacties te identificeren die moeten worden geregistreerd in [!INCLUDE[prod_short](includes/prod_short.md)]. Deze taak zou bijvoorbeeld worden gebruikt om periodieke bankkosten of kleine personeelskosten te identificeren. Deze taak bestaat doorgaans uit meerdere stappen, te beginnen met het importeren van bankafschriften in [!INCLUDE[prod_short](includes/prod_short.md)], gevolgd door het afstemmen van transacties met grootboekposten en het boeken van nieuwe grootboekposten om eventuele resterende transacties weer te geven die voorheen niet bekend waren in uw grootboeken. Copilot in [!INCLUDE[prod_short](includes/prod_short.md)] vermindert handmatige inspanningen door meer transacties af te stemmen en grootboekrekeningen voor te stellen waarnaar u kunt boeken. 

## <a name="what-are-capabilities-of-bank-reconciliation-assist"></a>Wat zijn de mogelijkheden van hulp bij bankreconciliatie?

Copilot biedt AI-aangedreven hulp met twee verschillende taken: 

- Verbeterde afstemming van transacties met grootboekposten 

   [!INCLUDE[prod_short](includes/prod_short.md)] biedt geautomatiseerde regels die veel banktransacties automatisch afstemmen met grootboekposten. Deze regels zijn echter inflexibel en resulteren vaak in veel niet-afgestemde transacties die allemaal handmatige inspectie en vergelijking vereisen. Copilot gebruikt AI-technologie om resterende transacties te inspecteren en meer overeenkomsten te identificeren, op basis van de datums, bedragen en beschrijvingen. Als bijvoorbeeld meerdere facturen als één forfaitair bedrag door een klant zijn betaald, stemt Copilot de enkele bankafschriftregel af met de meerdere factuurposten. 
 
- Voorgestelde grootboekrekeningen 

   Voor resterende banktransacties die niet met grootboekposten konden worden afgestemd, gebruikt Copilot AI-technologie om de transactiebeschrijving te vergelijken met grootboekrekeningnamen, waarbij de meest waarschijnlijke grootboekrekening wordt voorgesteld om naar te boeken. Copilot kan bijvoorbeeld voorstellen dat transacties met het verhaal 'Brandstofstop 24' worden geboekt naar het account 'Transport'. 

Copilot maakt geen verbinding met uw bank om transacties op te halen of te verzenden. Deze taak blijft volledig binnen uw controle en is een voorwaarde om de hulp van Copilot te gaan gebruiken, ongeacht of deze transacties worden toegevoegd aan [!INCLUDE[prod_short](includes/prod_short.md)] via een digitale bankverbinding, geïmporteerd uit een bankafschriftbestand of handmatig ingevoerd. 

## <a name="what-is-the-intended-use-of-bank-reconciliation-assist"></a>Wat is het beoogde gebruik van de hulp bij bankreconciliatie?

Hulp bij bankrekeningreconciliatie is bedoeld om nieuwe transacties te helpen identificeren waar klanten rekening mee moeten houden in [!INCLUDE[prod_short](includes/prod_short.md)], om de nauwkeurigheid van hun grootboeken te verbeteren. Deze activiteit is niet bedoeld voor het opsporen van fraude of het vaststellen of klanten op tijd hebben betaald.   

## <a name="how-was-bank-reconciliation-assist-evaluated-what-metrics-are-used-to-measure-performance"></a>Hoe werd de hulp bij bankreconciliatie beoordeeld? Welke statistieken worden gebruikt om de prestaties te meten?

Deze functionaliteit is getest met combinaties van synthetische banktransactiegegevens en vergelijkbare grootboekrekeningen en grootboekposten die de typische variaties en gegevenslimieten voor elk veld en in verschillende talen dekken. Testgegevens vertegenwoordigen zowel typisch gebruik als gebruik door slechte actoren. De prestaties werden gemeten in vergelijking met handmatige reconciliatie van dezelfde gegevens. 

## <a name="what-are-the-limitations-of-bank-reconciliation-assist-how-can-users-minimize-the-impact-of-the-bank-reconciliation-limitations-when-using-the-system"></a>Wat zijn de beperkingen van bij bankreconciliatie? Hoe kunnen gebruikers de impact van de beperkingen op het gebied van bankreconciliatie minimaliseren bij het gebruik van het systeem?

Hulp bij het reconciliëren van bankrekeningen werkt het beste wanneer grootboekrekeningnamen, beschrijvingen van grootboekposten en beschrijvingen van banktransacties allemaal in dezelfde taal zijn. Gemengde talen of gemengde taal van transactiebeschrijvingen resulteren vaak in minder overeenkomsten en suggesties. 

Voorgestelde grootboekrekeningen presteren het beste in de Engelse taal. Hoewel deze functie in elk van de beschikbare [!INCLUDE[prod_short](includes/prod_short.md)]-talen kan worden gebruikt, ervaren gebruikers mogelijk minder transactieafstemmingen en minder voorgestelde grootboekrekeningen in andere talen. 
<!--

## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-feature"></a>What operational factors and settings allow for effective and responsible use of the feature?


-->
## <a name="in-which-geographies-and-languages-is-bank-reconciliation-assist-available"></a>In welke geografieën en talen is hulp bij bankreconciliatie beschikbaar?

Deze mogelijkheid is beschikbaar voor elke omgeving van land/regio en in elke gebruikerstaal. Voor klantomgevingen in landen/regio's waar de Azure OpenAI-service niet wordt geïmplementeerd, moeten beheerders eerst toestemming geven om gegevensverplaatsing over de grenzen heen toe te staan voor [!INCLUDE[prod_short](includes/prod_short.md)] om verbinding te maken met de Azure OpenAI-service en deze mogelijkheid beschikbaar te maken. 

Zie de vorige vraag over beperkingen voor meer informatie over taal.  

## <a name="what-is-expected-of-end-users-when-operating-bank-account-reconciliation-assist"></a>Wat wordt er van eindgebruikers verwacht bij het gebruik van hulp bij bankrekeningreconciliatie?

### <a name="while-using-bank-account-reconciliation"></a>Tijdens gebruik van bankrekeningreconciliatie

Afstemmingen en suggesties op basis van AI kunnen soms onjuist of onvolledig zijn. Gebruikers van hulp bij bankrekeningreconciliatie moeten de nauwkeurigheid van afstemmingen en suggesties van Copilot controleren voordat ze ervoor kiezen deze te behouden. Afstemmingen en suggesties van Copilot worden pas in de [!INCLUDE[prod_short](includes/prod_short.md)]-database opgeslagen als u de knop Behouden kiest en het Copilot-venster sluit. U kunt ook eventuele afstemmingen of suggesties bewerken en corrigeren voordat u ervoor kiest deze te behouden. 

### <a name="after-completing-bank-account-reconciliation"></a>Na voltooiing van bankrekeningreconciliatie

Het wordt aanbevolen dat gebruikers ook de nauwkeurigheid controleren en eventuele discrepanties corrigeren nadat ze het Copilot-venster hebben verlaten, inclusief de volgende activiteiten: 

- Bekijk het reconciliatietestrapport. 
- Zorg ervoor dat uw organisatie over de juiste beoordelings- en controleprocessen beschikt. 
- Open eventuele geboekte reconciliaties opnieuw met behulp van de functie Ongedaan maken. 
- Corrigeer eventuele foutieve grootboekposten door posten tegen te boeken. 

## <a name="what-is-expected-of-administrators-and-end-users-when-operating-bank-account-reconciliation-assist"></a>Wat wordt er van beheerders verwacht bij het gebruik van hulp bij bankrekeningreconciliatie?

Eindgebruikers, zoals accountants, penningmeesters of anderen die aan de bedrijfsboekhouding werken, moeten altijd de juistheid van afstemmingen en suggesties van Copilot controleren voordat ze ervoor kiezen deze te behouden. Na de reconciliatie met Copilot raden we u aan het reconciliatietestrapport te bekijken om de nauwkeurigheid te verifiëren en eventuele discrepanties te identificeren. 

Beheerders moeten ervoor zorgen dat de juiste accountinggebruikers toegang hebben gekregen tot deze mogelijkheid. 

## <a name="is-copilot-the-only-means-to-completing-bank-account-reconciliation"></a>Is Copilot het enige middel om bankrekeningreconciliatie te voltooien?

Nee: gebruik van Copilot is optioneel. [!INCLUDE[prod_short](includes/prod_short.md)] biedt traditionele, niet door AI aangedreven middelen voor het importeren van bankafschriften, het uitvoeren van vooraf gedefinieerde afstemmingsregels en het handmatig toepassen van afstemmingen en boeken naar de juiste grootboekrekeningen. Zowel de traditionele aanpak als Copilot kunnen gelijktijdig binnen een organisatie worden ingezet. 

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Hoe geef ik feedback over door AI gegenereerde inhoud?

Elke keer dat Copilot afstemmingen of suggesties levert, kunt u rechtstreeks vanuit het Copilot-venster feedback aan Microsoft geven met behulp van de besturingselementen 'Vind ik leuk' en 'Niet leuk'. Uw feedback blijft anoniem en wij gebruiken deze gegevens om de kwaliteit van de dienstverlening te verbeteren.


## <a name="see-also"></a>Zie ook

[Bankrekeningen reconciliëren met hulp bij bankreconciliatie (preview)](bank-reconciliation-with-copilot.md)
