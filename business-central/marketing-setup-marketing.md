---
title: Marketing- en contactbeheergegevens instellen
description: U kunt marketing- en contactpersonenbeheer in Business Central instellen om relaties met prospects of klanten te optimaliseren en campagnes en promoties te verbeteren.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'relationship, prospect, client, customer, campaign, promo'
ms.search.forms: '5172, 5173, 5170, 5094, 429'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# CRM instellen

Voordat u met uw contacten en marketing gaat werken, moet u enkele beslissingen en stappen nemen om in te stellen hoe het marketinggebied bepaalde aspecten van uw contacten beheert. Bijvoorbeeld kunt u aangeven of u de contactkaart wilt synchroniseren met de klantenkaart, leverancierskaart en bankrekeningkaart, hoe nummerreeksen worden gedefinieerd of wat de standaardaanhef moet zijn wanneer u naar uw contacten schrijft.

Door uw contacten te beheren en een strategie te volgen waarmee u klanten vaststelt, aantrekt en behoudt, kunt u beter uw bedrijf optimaliseren en klanten tevreden stellen. Met behulp van een goed systeem voor contactbeheer kunt u ook relaties met uw klanten opbouwen en onderhouden. Communicatie is essentieel bij deze relaties. Bedrijven kunnen alleen succesvol zijn als ze communicatie met potentiële en bestaande klanten, leveranciers en zakenpartners kunnen aanpassen aan hun behoeften. Als eerste stap dient u een strategie op te zetten en vast te stellen hoe contactgegevens in uw bedrijf worden gebruikt. Deze informatie wordt door allerlei groepen in uw bedrijf bekeken, dus als u over een goed systeem beschikt, helpt u iedereen productiever te zijn.

U stelt marketing en contactbeheer in vanaf de pagina **Marketinginstellingen**. Om de pagina **Marketinginstellingen** te openen kiest u het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Marketinginstellingen** in en kiest u vervolgens de gerelateerde koppeling.

## Bepaalde informatie automatisch kopiëren van contactbedrijven naar contactpersonen.
Een aantal gegevens voor de contactbedrijven is gelijk aan de gegevens voor de contacten die in deze bedrijven werken, bijvoorbeeld de adresgegevens. In het gedeelte **Overerving** van de pagina **Marketinginstellingen** kunt u instellen dat de toepassing automatisch specifieke velden kopieert van de contactbedrijfkaart naar de contactpersoonskaart, elke keer dat u een contactpersoon maakt voor een contactbedrijf. Bijvoorbeeld kunt u selecteren om de verkoperscode, de adresgegevens (adres, adres 2, postcode, plaats en land,) en de communicatiegegevens (faxnummer, telexantwoord en telefoonnummer) en meer te kopiëren.

Als u een van deze velden wijzigt op de contactbedrijfskaart, wordt het veld op de contactkaart automatisch gewijzigd, tenzij u het veld op de contactkaart handmatig hebt gewijzigd.

Zie [Contactpersonen maken](marketing-create-contact-companies.md) voor meer informatie.

## Vooraf bepaalde standaardwaarden van nieuwe contacten gebruiken
U kunt bepalen of er automatisch een bepaalde taalcode, regiocode, verkoperscode en land-/regiocode als standaardwaarde moet worden toegewezen aan elk nieuw contact. U kunt ook een standaardverkoopcycluscode invoeren die automatisch wordt toegewezen aan elke nieuwe opportunity.

Als u velden overneemt, worden de ingestelde standaardwaarden overschreven. Als u bijvoorbeeld Engels als standaardtaal hebt ingesteld, maar de taal van het contactbedrijf is Duits, wordt Duits automatisch toegewezen als de taal voor de contacten die zijn vastgelegd voor het desbetreffende bedrijf.

<!--You can also setup a default salutation that application automatically assigns to your contacts. You can use these salutations in your interaction template attachments (for example, Microsoft Word documents). When setting up a default salutation, you can enter a salutation text and a salutation format. For example, if the salutation text is Dear, and the salutation format is Salutation Text + Title + Name, application will automatically enter Dear Mr. John Smith as a salutation for a contact called John Smith.-->

## Automatisch interacties vastleggen
In [!INCLUDE[prod_short](includes/prod_short.md)] kunnen verkoop- en inkoopdocumenten automatisch worden geregistreerd als interacties (bijvoorbeeld orders, facturen, ontvangsten, enzovoort), alsmede e-mails, telefoongesprekken en contactkaarten.

Zie voor meer informatie [Automatisch interacties met contacten registreren](marketing-auto-record-interactions.md).

## Contacten met klanten synchroniseren en meer
Als u de contactkaart wilt synchroniseren met de klantenkaart, leverancierskaart en bankrekeningkaart, moet u een zakenrelatiecode selecteren voor klanten, leveranciers en bankrekeningen. U kunt bijvoorbeeld alleen een contact koppelen aan een bestaande klant als u een zakenrelatiecode voor klanten hebt geselecteerd op de pagina **Marketinginstellingen**.

Zie voor meer informatie [Contacten synchroniseren met klanten, leveranciers en bankrekeningen](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).  

## Een nummerreeks toewijzen aan opportunity's en contacten
U kunt een nummerreeks instellen voor contacten en opportunities. Als u een nummerreeks hebt ingesteld voor contacten, wordt automatisch het volgende beschikbare contactnummer ingevoerd wanneer u een contact maakt en <kbd>Enter</kbd> selecteert in het veld Nr. op de contactkaart.

Zie voor meer informatie over nummerreeksen [Nummerreeksen maken](ui-create-number-series.md).

## Dubbele contacten zoeken als contacten worden gemaakt
U kunt de toepassing automatisch laten zoeken naar dubbele records telkens wanneer u een contactbedrijf maakt, of u kunt ervoor kiezen handmatig te zoeken nadat u contacten hebt gemaakt. U kunt de zoekstrings ook automatisch laten bijwerken door de toepassing, telkens wanneer u contactgegevens wijzigt of een contact maakt. U kunt zelf het zoekresultaatpercentage bepalen, dat wil zeggen, het percentage van identieke strings dat twee contactpersonen moeten hebben zodat ze als dubbele records worden beschouwd.

## Zie ook
[Contactpersonen beheren](marketing-contacts.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]