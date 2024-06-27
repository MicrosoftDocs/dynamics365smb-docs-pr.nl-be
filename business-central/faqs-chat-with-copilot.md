---
title: Veelgestelde vragen over verantwoorde AI voor chatten met Copilot (preview)
description: 'Deze veelgestelde vragen bieden informatie over de AI-technologie die wordt gebruikt voor het chatten met Copilot in Business Central. Het bevat belangrijke overwegingen en details over hoe AI wordt gebruikt, hoe het is getest en geëvalueerd en eventuele specifieke beperkingen.'
ms.date: 06/13/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI, chat'
---
# <a name="responsible-ai-faq-for-chat-with-copilot-preview"></a>Veelgestelde vragen over verantwoorde AI voor chatten met Copilot (preview)

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

Deze veelgestelde vragen (FAQ) beschrijven de AI-impact van Chatten met Copilot in [!INCLUDE[prod_short](includes/prod_short.md)]. Als u geïnteresseerd bent in algemene vragen over het gebruik van de functie, ga dan naar [Veelgestelde vragen over chatten met Copilot](chat-with-copilot-faq.md).

## <a name="what-is-chat-with-copilot"></a>Wat is Chatten met Copilot?

Microsoft Copilot is een AI-aangedreven assistent die u helpt creatiever, productiever en efficiënter te zijn. U kunt met Copilot chatten in Business Central om antwoorden en inzichten te krijgen over [!INCLUDE[prod_short](includes/prod_short.md)] en uw bedrijfsgegevens door in natuurlijke taal te typen wat u wilt weten.

Chatten met Copilot, ook wel chat genoemd, is een interactieve functie die uw vragen beantwoordt zonder dat u door de gebruikersinterface of de productdocumentatie hoeft te navigeren. Het Copilot-deelvenster is overal beschikbaar in de [!INCLUDE[prod_short](includes/prod_short.md)]-client.

U kunt vragen stellen in natuurlijke taal, zoals "Hoe lever ik goederen rechtstreeks van mijn leveranciers aan mijn klanten?" of "Hebben we bureaustoelen op voorraad voor onder 600 euro?" Als reactie hierop geeft Copilot antwoorden in natuurlijke taal. Afhankelijk van de vragen kunnen de antwoorden platte tekst, koppelingen naar records of pagina's bevatten in [!INCLUDE[prod_short](includes/prod_short.md)] en koppelingen naar [!INCLUDE[prod_short](includes/prod_short.md)]-Help-artikelen over Microsoft Learn.

## <a name="what-are-capabilities-of-chat-with-copilot"></a>Wat zijn de mogelijkheden van Chatten met Copilot?

U kunt met Copilot chatten om antwoorden te krijgen op de volgende soorten vragen:

### <a name="explain-and-guide"></a>Uitleggen en begeleiden

U kunt Copilot vragen om een specifiek concept uit te leggen dat is gerelateerd aan [!INCLUDE[prod_short](includes/prod_short.md)], zoals wat dimensies zijn, of het bieden van richtlijnen voor het voltooien van een taak, zoals het boeken van een verkooporder. Copilot doorzoekt de officiële [!INCLUDE[prod_short](includes/prod_short.md)]-documentatie die door Microsoft is gepubliceerd, en geeft een antwoord op basis van de documentatie.

- Copilot gebruikt de kennis van Microsoft Learn(geen uitgebreide zoekopdracht op internet) om alleen semantisch in Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]-documentatie in Microsoft Learn te zoeken.

- Copilot onderneemt geen actie, maakt geen nieuwe gegevens aan en wijzigt geen configuratie. Het vat eenvoudig alle alinea´s samen die worden gevonden in Microsoft Learn en die overeenkomen met de vraag of prompt in de chat.

### <a name="find-business-data-and-related-pages"></a>Bedrijfsgegevens en gerelateerde pagina's zoeken

U kunt Copilot vragen om pagina's op naam te lokaliseren of om records op te vragen op basis van de velden en beperkingen ervan. Als Copilot een overeenkomst vindt, wordt gereageerd met een koppeling naar de betreffende record of pagina die u vervolgens kunt selecteren om te openen.

- Copilot zet de natuurlijke taalinvoer om in een query die bestaat uit tabelzoek-, sorteer- en filtercriteria.

  De mogelijkheid maakt gebruik van de eigen gegevenszoekfuncties van [!INCLUDE[prod_short](includes/prod_short.md)] om overeenkomende gegevens te vinden uit tabellen in de bedrijfsdatabase. De zoekopdracht wordt uitgevoerd onder uw eigen identiteit voor beveiliging en compliance. Er wordt niet buiten de [!INCLUDE[prod_short](includes/prod_short.md)]-database gezocht.

- Copilot onderneemt geen actie, maakt geen nieuwe gegevens aan en wijzigt geen configuratie. Alleen de records die zijn ontvangen van de eigen [!INCLUDE[prod_short](includes/prod_short.md)]-gegevenszoekopdracht worden samengevat. 

## <a name="what-is-the-intended-use-of-chat-with-copilot"></a>Wat is het beoogde gebruik van Chatten met Copilot?

Chatten is ontworpen voor zakelijk gebruik en voor het beantwoorden van vragen die betrekking hebben op [!INCLUDE[prod_short](includes/prod_short.md)] en de bedrijfsgegevens die het bevat. Met deze functie kunt u algemene taken oplossen, zoals het vinden van records of het verkrijgen van begeleiding. U kunt uzelf in uw eigen woorden uitdrukken, waardoor uw werk gemakkelijker en toegankelijker wordt als u werkt met [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="how-was-chat-with-copilot-evaluated-what-metrics-are-used-to-measure-performance"></a>Hoe is Chatten met Copilot beoordeeld? Welke statistieken worden gebruikt om de prestaties te meten?

- De functie is uitgebreid getest, waarbij talloze Engelstalige teksten over een breed scala aan onderwerpen en manieren om intenties uit te drukken aan Copilot werden doorgegeven. De resultaten werden beoordeeld op nauwkeurigheid, relevantie en veiligheid.
  
- De functie is gebouwd in overeenstemming met de verantwoorde AI-standaard van Microsoft. [Lees meer over verantwoorde AI van Microsoft](https://aka.ms/RAI).

## <a name="how-does-microsoft-monitor-the-quality-of-generated-content"></a>Hoe bewaakt Microsoft de kwaliteit van de gegenereerde inhoud?

Microsoft beschikt over verschillende systemen om ervoor te zorgen dat de door Copilot gegenereerde inhoud van de hoogste kwaliteit is, misbruik op te sporen en de veiligheid van onze klanten en hun gegevens te garanderen.

U kunt feedback geven op elke Copilot-reactie en onnauwkeurige of ongepaste inhoud melden om Microsoft te helpen deze functie te verbeteren. 

- U geeft feedback door het pictogram Vind ik leuk (duim omhoog) of Niet leuk (duim omlaag) te gebruiken in het deelvenster **Copilot** in [!INCLUDE[prod_short](includes/prod_short.md)].
  
- We analyseren en gebruiken uw feedback over de functie zodat reacties kunnen worden verbeterd.
  
- Als u ongepast gegenereerde inhoud tegenkomt, rapporteer dit dan aan Microsoft met behulp van dit feedbackformulier: [Misbruik melden](https://go.microsoft.com/fwlink/?linkid=2249810).
  
- Microsoft schakelt mogelijk de door Copilot aangestuurde functies uit voor geselecteerde klanten als misbruik van de functionaliteit wordt gedetecteerd.

## <a name="what-are-the-limitations-of-chat-with-copilot-how-can-users-minimize-the-impact-of-the-chat-with-copilot-limitations-when-using-the-system"></a>Wat zijn de beperkingen van Chatten met Copilot? Hoe kunnen gebruikers de impact van de beperkingen van Chatten met Copilot minimaliseren bij het gebruik van het systeem?

- Algemene beperkingen van AI

  AI-systemen zijn waardevolle hulpmiddelen, maar ze zijn niet-deterministisch. De inhoud die ze genereren is mogelijk niet nauwkeurig. Het is dus belangrijk dat u uw oordeel gebruikt om de reacties van Copilot te beoordelen en te verifiëren voordat u beslissingen neemt die van invloed kunnen zijn op belanghebbenden, zoals klanten en partners. Voor de meeste reacties neemt Copilot ook citaten of verwijzingskoppelingen op die u kunt gebruiken om snel te verifiëren of Copilot tot het juiste antwoord is gekomen. Als er bijvoorbeeld wordt gevraagd hoe een bepaalde taak moet worden uitgevoerd, bevat Copilot koppelingen naar het bronartikel. Wanneer u wordt gevraagd een record te zoeken op basis van specifieke criteria, voegt Copilot koppelingen toe die de lijstpagina beschrijven die het als gespreksonderwerp heeft geïdentificeerd. Het biedt ook informatie over eventuele filters of sorteringen die zijn toegepast om tot een antwoord te komen.

- Taalbeperkingen

  - Chatten wordt alleen in het Engels ondersteund voor de volgende landinstellingen: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA.

    Als de weergavetaal in [!INCLUDE[prod_short](includes/prod_short.md)] niet een van deze landinstellingen is, is chatten niet beschikbaar.

  - De kwaliteit van de antwoorden kan minder zijn in de volgende gevallen:
    - De taalinstelling is iets anders dan en-US.
    - De taalinstelling voor de gebruiker in [!INCLUDE[prod_short](includes/prod_short.md)] verschilt van de primaire taal van de gegevens in de [!INCLUDE[prod_short](includes/prod_short.md)]-database.

- Specifieke branche-, product- en onderwerpbeperkingen

   Chat bevat ingebouwde veiligheidsmechanismen die het ongewenst genereren van schadelijke inhoud, zoals seksueel expliciete inhoud of het aanzetten tot geweld, voorkomen. Soms zijn klanten actief in bedrijfstakken, verkopen ze producten en diensten, of werken ze met processen die op natuurlijke wijze overlappen met wat in andere contexten als ongepast zou kunnen worden beschouwd, of werken ze met gegevens die deze voorzorgsmaatregelen kunnen activeren. Chatten werkt in deze gevallen mogelijk niet zo goed.

<!--## What operational factors and settings allow for effective and responsible use of the feature?-->

## <a name="what-data-does-chat-with-copilot-collect-and-how-is-it-used"></a>Welke gegevens worden door Chatten met Copilot verzameld en hoe worden deze gebruikt?

Microsoft gebruikt uw bedrijfsgegevens, inclusief de tekst die u naar Copilot verzendt, niet om de fundamentele AI-modellen te trainen ten behoeve van anderen. Bedrijfsbeheerders hebben volledige controle over deze gegevens die deel uitmaken van hun Azure-abonnement. Omdat beheerders of anderen in uw bedrijf mogelijk toegang hebben tot deze gegevens, zoals bepaald door uw werkgever, raden we u aan geen gevoelige gegevens in te voeren, zoals wachtwoorden of andere geheimen.

## <a name="what-does-chat-with-copilot-offer-for-security"></a>Wat biedt Chatten met Copilot voor beveiliging?

Chatten is ontworpen om veilig te zijn en wordt uitgevoerd onder de identiteit van de gebruiker, waarbij alle beveiligingsmachtigingen en andere beperkingen worden overgenomen en nooit buiten de platformbeveiliging van [!INCLUDE[prod_short](includes/prod_short.md)] wordt gebruikt. Dit betekent dat Copilot alleen toegang heeft tot gegevens waartoe u toegang hebt.

Voor gebruikers met SUPER-machtiging kan chatten gemakkelijker onbeveiligde gegevens vinden die doorgaans moeilijker te bereiken zijn voor andere gebruikers. Organisaties die het [!INCLUDE[prod_short](includes/prod_short.md)]-beveiligingsmodel niet toepassen om te beperken tot welke tabellen en objecten elke gebruiker of gebruikersrol toegang heeft, lopen mogelijk een verhoogd risico als ze chatten gebruiken. Daarom raden we aan dat uw organisatie het beveiligingsmodel van [!INCLUDE[prod_short](includes/prod_short.md)] implementeert of chatten uitschakelt.

## <a name="see-also"></a>Zie ook

- [Chatten met Copilot (preview)](chat-with-copilot.md)

