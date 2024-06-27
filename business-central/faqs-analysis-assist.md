---
title: Veelgestelde vragen over hulp bij analyse (preview)
description: 'Deze veelgestelde vragen bieden informatie over de AI-technologie die wordt gebruikt voor het analyseren van gegevens op pagina´s in Business Central. Het bevat belangrijke overwegingen en details over hoe AI wordt gebruikt, hoe het is getest en geëvalueerd en eventuele specifieke beperkingen.'
ms.date: 06/13/2024
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

# Veelgestelde vragen over hulp bij analyse (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Deze veelgestelde vragen (FAQ) beschrijven de AI-impact van de functie voor hulp bij analyse in [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## Wat is hulp bij analyse?

Hulp bij analyse is een copilot die hulp biedt bij het werken met de [gegevensanalysemodus](analysis-mode.md) in Business Central. Met de gegevensanalysemodus kunt u gegevens op pagina's en query's ordenen, aggregeren en samenvatten, zodat deze geschikter worden voor het analyseren en verkrijgen van betekenisvolle inzichten. Met hulp bij analyse kunt u automatisch de weergave van de gegevens samenstellen die u wilt analyseren door uw behoeften in eenvoudige, natuurlijke taal uit te drukken, zoals 'toon leveranciers op locatie, gesorteerd op aantal aankopen'. Hulp bij analyse maakt het gemakkelijker om met gegevens te werken zonder de noodzaak van complexe technische vaardigheden.

## Wat zijn de mogelijkheden van hulp bij analyse?

Hulp bij analyse is gebaseerd op de ontwikkelaarstools voor Copilot in Business Central. Het maakt gebruik van Azure OpenAI Service om ongestructureerde instructies om te zetten in een gestructureerd ontwerp voor het weergeven van gegevens in de analysemodus, zonder zelf bedrijfsgegevens van klanten te maken, wijzigen of bijwerken.

## Wat is het beoogde gebruik van hulp bij analyse?

Hulp bij analyse helpt analysetabbladen te helpen maken in de gegevensanalysemodus om gegevens te presenteren op een manier die het gemakkelijker maakt om conclusies te trekken. Het is echter belangrijk er rekening mee te houden dat hulp bij analyse geen directe inzichten of conclusies over de gegevens biedt. Het is een tool waarmee gebruikers hun gegevens kunnen ordenen en weergeven. Het is echter aan de gebruiker om bruikbare informatie te verzamelen, trends te ontdekken en weloverwogen beslissingen te nemen om de bedrijfswaarde te vergroten.

## Hoe is hulp bij analyse beoordeeld? Welke statistieken worden gebruikt om de prestaties te meten?

- De functie is uitgebreid getest gebaseerd op de demonstratiegegevens van [!INCLUDE[prod_short](includes/prod_short.md)] en andere fictieve productcatalogi. Copilot kreeg talloze aanwijzingen in de ondersteunde Engelse landinstellingen. De prompts bestreken een breed scala aan instructies voor gegevensanalyse en stijlen voor het uiten van intenties. De resultaten werden beoordeeld op nauwkeurigheid, relevantie en veiligheid.

- De functie is gebouwd in overeenstemming met de verantwoorde AI-standaard van Microsoft. [Lees meer over verantwoorde AI van Microsoft](https://aka.ms/RAI)

## Hoe bewaakt Microsoft de kwaliteit van de gegenereerde inhoud?

Microsoft beschikt over verschillende systemen om ervoor te zorgen dat de door Copilot gegenereerde inhoud van de hoogste kwaliteit is, misbruik op te sporen en de veiligheid van onze klanten en hun gegevens te garanderen.

Gebruikers hebben de mogelijkheid om feedback te geven op elke Copilot-reactie en onnauwkeurige of ongepaste inhoud te melden om Microsoft te helpen deze functie te verbeteren.

- Als u ongepaste gegenereerde inhoud tegenkomt, rapporteer dit dan aan Microsoft met behulp van dit feedbackformulier: [Misbruik melden](https://go.microsoft.com/fwlink/?linkid=2249810)

- We analyseren gebruikersfeedback over de functie en gebruiken deze zodat reacties kunnen worden verbeterd.

  U geeft feedback door het pictogram Vind ik leuk (duim omhoog) of Niet leuk (duim omlaag) te gebruiken in het deelvenster **Copilot** in [!INCLUDE[prod_short](includes/prod_short.md)].

- Microsoft schakelt mogelijk de door Copilot aangestuurde functies uit voor geselecteerde klanten als misbruik van de functionaliteit wordt gedetecteerd.

## Wat zijn de beperkingen van hulp bij analyse? Hoe kunnen gebruikers de impact van de beperkingen van hulp bij analyse minimaliseren bij het gebruik van het systeem?

- Algemene AI-beperkingen:

  AI-systemen zijn waardevolle hulpmiddelen, maar ze zijn niet-deterministisch. De inhoud die ze genereren is mogelijk niet nauwkeurig. Het is belangrijk dat u uw oordeel gebruikt om de reacties te beoordelen en te verifiëren voordat u beslissingen neemt die van invloed kunnen zijn op belanghebbenden, zoals klanten en partners.

- Beschikbare talen

   [!INCLUDE[analysis-assist-language-support](includes/analysis-assist-language-support.md)]

   De kwaliteit van antwoorden kan ook minder worden als de taalinstelling voor de gebruiker in Business Central verschilt van de primaire taal van de bedrijfsgegevens in de [!INCLUDE[prod_short](includes/prod_short.md)]-database.
  
- Geografische beperking:
  
   De functie is beschikbaar in alle ondersteunde [Business Central-landen/regio's](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)<!-- except for Canada-->. Voor de functie wordt echter Microsoft Azure OpenAI Service gebruikt, wat momenteel alleen in bepaalde geografische regio's beschikbaar is voor Business Central. Als uw omgeving zich in een land/regio bevindt waar de Azure OpenAI Service niet beschikbaar is, moeten beheerders toestaan dat gegevens tussen geografische gebieden worden verplaatst. Meer informatie over [Copilot-gegevensverplaatsing tussen geografische gebieden](/dynamics365/business-central/ai-copilot-data-movement).

- Bepaalde branche-, product- en onderwerpbeperkingen:

  Organisaties die actief zijn in bepaalde bedrijfsdomeinen, zoals de medische sector, de drugssector, de juridische sector en de wapensector, kunnen te maken krijgen met een lagere kwaliteit van de dienstverlening.

## Welke gegevens worden door analyse verzameld en hoe worden deze gebruikt?

Met de mogelijkheid van hulp bij analyse wordt het minimum aan gegevens verzameld die Business Central nodig heeft om de service aan te bieden. Microsoft gebruikt uw bedrijfsgegevens, inclusief de tekst die u naar Copilot verzendt, niet om de fundamentele modellen te trainen ten behoeve van anderen. Zie [Dynamics 365-voorwaarden voor door Azure OpenAI aangedreven functies](https://go.microsoft.com/fwlink/?linkid=2236010) voor meer informatie.

Met de mogelijkheid worden ook gegevens verzameld van de feedback die gebruikers kunnen geven met behulp van de pictogrammen 'Vind ik leuk' (duim omhoog) of 'Niet leuk' (duim omlaag) in hulp bij analyse op de pagina **Copilot**. De gegevens zijn anoniem en omvatten de keuze van Vind ik leuk of Niet leuk, de reden voor het niet leuk vinden en de Copilot-functie waarop de feedback van toepassing is.

## Zie ook

[Gegevens analyseren in Copilot (preview)](analysis-assist.md)
