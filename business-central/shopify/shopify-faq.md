---
title: Veelgestelde vragen voor technische details
description: Implementatiedetails met betrekking tot de Shopify-connector
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
---

# Veelgestelde vragen voor technische details

Dit artikel beantwoordt een lijst met veelgestelde vragen over de Shopify-connector.

## Wat is Shopify? 

Shopify is op abonnementen gebaseerde software waarmee iedereen een online winkel kan opzetten en zijn of haar producten kan verkopen. Het Shopify-platform biedt online retailers een reeks diensten, waaronder tools voor betalingen, marketing, verzending en klantbetrokkenheid. 

## Wat is de Microsoft Dynamics 365 Business Central Shopify-connector? 

Met de Shopify-connector kunnen bedrijven hun Shopify winkel (of winkels) aan [!INCLUDE[prod_short](../includes/prod_short.md)] koppelen om de bedrijfsproductiviteit te maximaliseren. Met de Shopify-connector kunnen ze inzichten uit hun bedrijf en online Shopify-winkel als één eenheid bekijken en beheren. 

### Mogelijkheden

- Ondersteuning voor meer dan één Shopify-winkel
  - Elke winkel heeft zijn eigen opzet, waaronder een verzameling producten, locaties die worden gebruikt om de voorraad te berekenen en prijslijsten.  
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
  - Gebruik landspecifieke sjablonen bij het maken van klanten, zodat u zeker weet dat de belastinginstellingen correct zijn.  
- Importeren van bestellingen uit Shopify
  - Voeg bestellingen toe die zijn gemaakt in verschillende verkoopkanalen, zoals een online winkel of **Shopify POS**. 
  - Verzendkosten, cadeaubonnen, fooien, verzend- en betaalmethoden, transacties en risico op fraude.  
  - Tijdens het importeren kunt u automatisch klanten maken in [!INCLUDE [prod_short](../includes/prod_short.md)] of besluiten de klanten te beheren in Shopify.  
  - Uitbetalingsinformatie ontvangen van Shopify Payments. 
- Afhandelingsinformatie volgen
  - Kies er optioneel voor om trackinginformatie uit [!INCLUDE [prod_short](../includes/prod_short.md)] over te dragen naar Shopify.  

## Waarom hebben Microsoft en Shopify deze samenwerking gecreëerd? 

[!INCLUDE[prod_short](../includes/prod_long.md)] werkt samen met Shopify om onze klanten te helpen een betere winkelervaring te creëren. Shopify biedt handelaren een eenvoudige handelsoplossing en [!INCLUDE[prod_short](../includes/prod_short.md)] is een alles-in-één oplossing voor bedrijfsmanagement waarmee bedrijven hun financiën, verkoop, service en activiteiten kunnen beheren in één toepassing. Naadloze verbinding tussen de twee systemen synchroniseert orders, voorraad en klantinformatie om ervoor te zorgen dat verkopers orders sneller kunnen uitvoeren en klanten beter kunnen bedienen.

## Voor welke Microsoft-producten is de Shopify-connector beschikbaar?

Deze functie is alleen beschikbaar voor [!INCLUDE[prod_short](../includes/prod_short.md)] online, te beginnen met versie 20.1. Het is niet beschikbaar voor on-premises implementaties. De app met de connector wordt vooraf geïnstalleerd voor nieuwe omgevingen. Organisaties met bestaande omgevingen kunnen de app downloaden en installeren vanaf AppSource. De organisatie moet zowel een Business Central-licentie als een Shopify-licentie hebben om de connector te gebruiken. Zie voor meer informatie over ondersteunde landen/regio's, talen en edities van [!INCLUDE[prod_short](../includes/prod_short.md)] [Shopify-connector op de AppSource](https://go.microsoft.com/fwlink/?linkid=2196238).

De Shopify-connector werkt niet voor [App insluiten](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview), waarbij de client-URL de indeling `https://[application name].bc.dynamics.com` heeft. 

## Welke ondersteuning wordt geboden voor de Shopify-connector?

### [!INCLUDE[prod_short](../includes/prod_short.md)]

De Shopify-connector valt onder het huidige ondersteuningsmodel. Zie voor meer informatie [Technische ondersteuning](/dynamics365/business-central/dev-itpro/administration//manage-technical-support) (alleen in het Engels). 

Krijg hulp van een consultant die de Shopify-connector voor [!INCLUDE[prod_short](../includes/prod_short.md)] kent, om aan uw unieke bedrijfsspecifieke vereisten te voldoen.
 
Zoek in [Adviesdiensten](https://aka.ms/BCShopifyConsultant).

### Shopify

U krijgt hulp met Shopify door te beginnen met [Algemeen Shopify Helpcentrum](https://help.shopify.com/) of [24/7 ondersteuning voor uw winkel als een Shopify-handelaar](https://help.shopify.com/questions#/). 

U kunt ook de [Experts Marketplace](https://experts.shopify.com/) verkennen om de juiste experts te vinden die diensten aanbieden voor Shopify-verkopers.

## Functies die momenteel niet worden ondersteund, houden we echter bij en kunnen overwegen ze in de toekomst toe te voegen:

- B2B-functies, waaronder Bedrijven, prijslijsten van bedrijven, betalingsvoorwaarden
- Markten
  - Meerdere vertalingen van hoofdgegevens. U kunt één taal kiezen die wordt gebruikt voor het exporteren van productinformatie.
  - Prijzen per land/regio. Er is één prijslijst beschikbaar voor de geselecteerde valuta. De conversie naar andere valuta's wordt afgehandeld door Shopify.

## Is de Shopify-connector uitbreidbaar?

Momenteel is deze app niet uitbreidbaar met plannen om deze in 2023 uitbreidbaar te maken. 

## Staat de Shopify-connector open voor bijdragen?

Ja, deze extensie staat open voor bijdragen van de community. U vindt de [broncode](https://github.com/microsoft/ALAppExtensions/tree/main/Apps/W1/Shopify) in de opslagplaats voor add-ons voor Microsoft AL-toepassingen.


## Zie ook

[Aan de slag met de connector voor Shopify](get-started.md)  
