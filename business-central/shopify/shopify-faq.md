---
title: Veelgestelde vragen voor technische details
description: Implementatiedetails met betrekking tot de Shopify-connector
ms.date: 01/24/2024
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
---

# <a name="faq-for-technical-details"></a>Veelgestelde vragen voor technische details

Dit artikel beantwoordt een lijst met veelgestelde vragen over de Shopify-connector.

## <a name="what-is-shopify"></a>Wat is Shopify?

Shopify is op abonnementen gebaseerde applicatie waarmee iedereen een online winkel kan opzetten en zijn of haar producten kan verkopen. Het Shopify-platform biedt online retailers een reeks diensten voor betalingen, marketing, verzending en klantbetrokkenheid.

## <a name="what-is-the-microsoft-dynamics-365-business-central-shopify-connector"></a>Wat is de Microsoft Dynamics 365 Business Central Shopify-connector?

Met de Shopify-connector kunnen bedrijven hun Shopify winkel (of winkels) aan [!INCLUDE[prod_short](../includes/prod_short.md)] koppelen om de bedrijfsproductiviteit te maximaliseren. Met de Shopify-connector kunnen ze inzichten uit hun bedrijf en hun online Shopify-winkel als één eenheid bekijken en beheren.

### <a name="capabilities"></a>Mogelijkheden

- Ondersteuning voor meer dan één Shopify-winkel
  - Elke winkel heeft zijn eigen opzet, waaronder een verzameling producten en vestigingen die worden gebruikt om de voorraad en prijslijsten te berekenen.  
- Bidirectionele synchronisatie van artikelen of producten
  - De connector synchroniseert afbeeldingen, artikelvarianten, streepjescodes, artikelnummers van leveranciers, uitgebreide teksten en tags.  
  - Artikelkenmerken exporteren naar Shopify.  
  - Gebruik geselecteerde klantprijsgroepen en kortingen om prijzen te definiëren die worden geëxporteerd naar Shopify.  
  - Bepaal of items automatisch kunnen worden gemaakt of alleen updates van bestaande producten toestaan.  
- Synchronisatie van voorraadniveaus
  - Kies enkele of alle beschikbare locaties in [!INCLUDE [prod_short](../includes/prod_short.md)].  
  - Werk voorraadniveaus op meerdere locaties bij in Shopify.  
- Bidirectionele synchronisatie van klanten
  - Wijs klanten slim toe per telefoon en e-mail.  
  - Gebruik land/regio-specifieke sjablonen bij het maken van klanten, zodat u zeker weet dat de belastinginstellingen correct zijn.  
- Importeren van orders uit Shopify
  - Voeg bestellingen toe die zijn gemaakt in verschillende verkoopkanalen, zoals een online winkel of **Shopify POS**.
  - Verzendkosten, cadeaubonnen, fooien, verzend- en betaalmethoden, transacties en risico op fraude.  
  - Tijdens het importeren kunt u automatisch klanten maken in [!INCLUDE [prod_short](../includes/prod_short.md)] of besluiten de klanten te beheren in Shopify.  
  - Uitbetalingsinformatie ontvangen van Shopify Payments.
- Afhandelingsinformatie volgen
  - Kies er optioneel voor om trackinginformatie uit [!INCLUDE [prod_short](../includes/prod_short.md)] over te dragen naar Shopify.  

## <a name="why-did-microsoft-and-shopify-form-this-partnership"></a>Waarom hebben Microsoft en Shopify deze samenwerking gecreëerd?

[!INCLUDE[prod_short](../includes/prod_long.md)] werkt samen met Shopify om onze klanten te helpen een betere winkelervaring te creëren. Shopify biedt handelaren een eenvoudige handelsoplossing en [!INCLUDE[prod_short](../includes/prod_short.md)] is een alles-in-één oplossing voor bedrijfsmanagement waarmee bedrijven hun financiën, verkoop, service en activiteiten kunnen beheren. Gebruik de naadloze verbinding tussen de applicaties om orders, voorraad en klantinformatie te synchroniseren om orders sneller uit te voeren en klanten beter van dienst te zijn.

## <a name="which-microsoft-products-is-the-shopify-connector-available-for"></a>Voor welke Microsoft-producten is de Shopify-connector beschikbaar?

Deze functie is alleen beschikbaar voor [!INCLUDE[prod_short](../includes/prod_short.md)] online, te beginnen met versie 20.1. Het is niet beschikbaar voor on-premises implementaties. De connector wordt vooraf geïnstalleerd voor nieuwe omgevingen. Organisaties met bestaande omgevingen kunnen de connector downloaden en installeren vanaf AppSource. De organisatie moet zowel een [!INCLUDE [prod_short](../includes/prod_short.md)]-licentie als een Shopify-licentie hebben om de connector te kunnen gebruiken. Ga voor meer informatie over ondersteunde landen/regio's, talen en edities van [!INCLUDE[prod_short](../includes/prod_short.md)] naar [Shopify-connector op de AppSource](https://go.microsoft.com/fwlink/?linkid=2196238).

De Shopify-connector werkt niet voor [App insluiten](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), waarbij de client-URL de indeling `https://[application name].bc.dynamics.com` heeft.

## <a name="what-support-is-offered-for-the-shopify-connector"></a>Welke ondersteuning wordt geboden voor de Shopify-connector?

### [!INCLUDE[prod_short](../includes/prod_short.md)]

De Shopify-connector valt onder het huidige ondersteuningsmodel. Zie voor meer informatie [Technische ondersteuning](/dynamics365/business-central/dev-itpro/administration//manage-technical-support) (alleen in het Engels).

Krijg hulp van een consultant die de Shopify-connector voor [!INCLUDE[prod_short](../includes/prod_short.md)] kent, om aan uw unieke bedrijfsspecifieke vereisten te voldoen. Zoek in [Adviesdiensten](https://aka.ms/BCShopifyConsultant).

### <a name="shopify"></a>Shopify

Krijg hulp met Shopify in [Algemeen Shopify Helpcentrum](https://help.shopify.com/) of via [24/7 ondersteuning voor uw winkel als een Shopify-handelaar](https://help.shopify.com/questions#/).

U kunt ook de [Experts Marketplace](https://experts.shopify.com/) verkennen om de juiste experts te vinden die diensten aanbieden voor Shopify-verkopers.

## <a name="currently-unsupported-features-however-were-tracking-them-and-may-consider-adding-them"></a>Functies die momenteel niet worden ondersteund, houden we echter bij en we kunnen overwegen ze toe te voegen

- B2B-functies, waaronder bedrijven, prijslijsten van bedrijven en betalingsvoorwaarden
  - Uitgebreide ondersteuning voor B2B zal beschikbaar zijn in releasewave 1 van 2024. Zie [Business Central verbinden met Shopify B2B](/dynamics365/release-plan/2023wave2/smb/dynamics365-business-central/connect-business-central-shopify-b2b) voor meer informatie
- Markten
  - Meerdere vertalingen van hoofdgegevens. U kunt één taal kiezen die wordt gebruikt voor het exporteren van productinformatie.
  - Prijzen per land/regio. Er is één prijslijst beschikbaar voor de geselecteerde valuta. De conversie naar andere valuta's wordt afgehandeld door Shopify.
- Conceptorders

## <a name="is-the-shopify-connector-extensible"></a>Is de Shopify-connector uitbreidbaar?

Ja, de Shopify-connector is uitbreidbaar. Controleer GitHub om toegang te krijgen tot de [lijst met uitbreidbaarheidspunten](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) en verken enkele [voorbeelden](https://github.com/microsoft/ALAppExtensions/blob/main/Apps/W1/Shopify/extensibility_examples.md).

## <a name="is-the-shopify-connector-open-for-contribution"></a>Staat de Shopify-connector open voor bijdragen?

Ja, deze extensie staat open voor bijdragen vanuit de community. U vindt de [broncode](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) in de opslagplaats voor add-ons voor Microsoft AL-toepassingen.

## <a name="building-your-version-of-shopify-connector"></a>Uw versie van Shopify-connector maken

Als u volgens Shopify een connector-app op de Shopify marktplaats wilt bouwen en publiceren met als voornaamste doel het overdragen of delen van verkopersgegevens aan een derde partij ([!INCLUDE [prod_short](../includes/prod_short.md)]), moet u schriftelijke toestemming hebben van Shopify. Als onderdeel van dit proces moet u toestemming krijgen van Microsoft via het "formulier voor gegevensbevestiging van eindontvangers". We moeten u vragen de zaak af te handelen met Shopify omdat Microsoft geen overeenkomsten met derden kan ondertekenen.

### <a name="what-to-do"></a>Wat u moet doen

Controleer de Shopify-vereisten, omdat u mogelijk nog steeds een niet-vermelde app hebt.

Als alternatief krijgt de Shopify-connector voor [!INCLUDE [prod_short](../includes/prod_short.md)] voortdurend nieuwe functies en nieuwe klanten. Als u een specifiek hiaat ontdekt, kunt u overwegen een productsuggestie (https://aka.ms/bcideas) of een codebijdrage aan [!INCLUDE [prod_short](../includes/prod_short.md)] in te dienen. Voor vereisten die mogelijk niet relevant zijn voor de meerderheid van de klanten en die niet gemakkelijk kunnen worden aangepakt door het huidige uitbreidbaarheidsmodel, kunt u contact opnemen met het [!INCLUDE [prod_short](../includes/prod_short.md)]-ontwikkelteam om het praktijkgeval te bespreken. We moeten een haalbare oplossing kunnen vinden.

## <a name="see-also"></a>Zie ook

[Aan de slag met de connector voor Shopify](get-started.md)  
