---
title: Marketing- en contactbeheergegevens instellen| Microsoft Docs
description: U kunt marketing- en contactpersonenbeheer in Financials instellen om relaties met prospects of klanten te optimaliseren en campagnes en promoties te verbeteren.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, client, customer, campaign, promo
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 1bac6c541a07f5da6c42fa076627e174249f708b
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---
# <a name="setting-up-relationship-management"></a>CRM instellen
Voordat u met uw contacten en marketing gaat werken, moet u enkele beslissingen en stappen nemen om in te stellen hoe het marketinggebied bepaalde aspecten van uw contacten beheert. Bijvoorbeeld kunt u aangeven of u de contactkaart wilt synchroniseren met de klantenkaart, leverancierskaart en bankrekeningkaart, hoe nummerreeksen worden gedefinieerd of wat de standaardaanhef moet zijn wanneer u naar uw contacten schrijft.

Door uw contacten te beheren en een strategie te volgen waarmee u klanten vaststelt, aantrekt en behoudt, kunt u beter uw bedrijf optimaliseren en klanten tevreden stellen. Met behulp van een goed systeem voor contactbeheer kunt u ook relaties met uw klanten opbouwen en onderhouden. Communicatie is essentieel bij deze relaties. Bedrijven kunnen alleen succesvol zijn als ze communicatie met potentiële en bestaande klanten, leveranciers en zakenpartners kunnen aanpassen aan hun behoeften. Als eerste stap dient u een strategie op te zetten en vast te stellen hoe contactgegevens in uw bedrijf worden gebruikt. Deze informatie wordt door allerlei groepen in uw bedrijf bekeken, dus als u over een goed systeem beschikt, helpt u iedereen productiever te zijn.

U stelt marketing en contactbeheer in vanuit het venster **Marketinginstellingen**. Om de pagina **Marketinginstellingen** te openen, kiest u in de rechterbovenhoek het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voert u **Marketinginstellingen** in en klikt u op de gerelateerde koppeling.

## <a name="automatically-copying-specific-information-from-the-contact-companies-to-the-contact-persons"></a>Bepaalde informatie automatisch kopiëren van de contactbedrijven naar de contactpersonen.
Een aantal gegevens voor de contactbedrijven is gelijk aan de gegevens voor de contacten die in deze bedrijven werken, bijvoorbeeld de adresgegevens. In het gedeelte **Overerving** van het venster **Marketinginstellingen** kunt u instellen dat de toepassing automatisch specifieke velden kopieert van de contactbedrijfkaart naar de contactpersoonskaart, elke keer dat u een contactpersoon maakt voor een contactbedrijf. Bijvoorbeeld kunt u selecteren om de verkoperscode, de adresgegevens (adres, adres 2, postcode, plaats en land,) en de communicatiegegevens (faxnummer, telexantwoord en telefoonnummer) en meer te kopiëren.

Als u een van deze velden wijzigt op de contactbedrijfkaart, wordt het veld op de contactkaart automatisch gewijzigd, tenzij u het veld op de contactkaart handmatig hebt gewijzigd.

Zie voor meer informatie [Procedure: Contactpersonen maken](marketing-how-create-contact-persons.md).

## <a name="using-predefined-defaults-on-new-contacts"></a>Vooraf bepaalde standaardwaarden van nieuwe contacten gebruiken
U kunt bepalen of er automatisch een bepaalde taalcode, regiocode, verkoperscode en land-/regiocode als standaardwaarde moet worden toegewezen aan elk nieuw contact. U kunt ook een standaardverkoopcycluscode invoeren die automatisch wordt toegewezen aan elke nieuwe opportunity.

Als u velden overneemt, worden de ingestelde standaardwaarden overschreven. Als u bijvoorbeeld Engels als standaardtaal hebt ingesteld, maar de taal van het contactbedrijf is Duits, wordt Duits automatisch toegewezen als de taal voor de contacten die zijn vastgelegd voor het desbetreffende bedrijf.

<!--You can also setup a default salutation that the program automatically assigns to your contacts. You can use these salutations in your interaction template attachments (for example, Microsoft Word documents). When setting up a default salutation, you can enter a salutation text and a salutation format. For example, if the salutation text is Dear, and the salutation format is Salutation Text + Title + Name, the program will automatically enter Dear Mr. John Smith as a salutation for a contact called John Smith.-->

## <a name="automatically-recording-interactions"></a>Automatisch interacties vastleggen
In [!INCLUDE[d365fin](includes/d365fin_md.md)] kunnen verkoop- en inkoopdocumenten automatisch worden geregistreerd als interacties (bijvoorbeeld orders, facturen, ontvangsten, enzovoort), alsmede e-mails, telefoongesprekken en contactkaarten.

Zie voor meer informatie [Automatisch interacties met contacten registreren](marketing-auto-record-interactions.md).

## <a name="synchronizing-contacts-with-customers-and-more"></a>Contacten met klanten synchroniseren en meer
Als u de contactkaart wilt synchroniseren met de klantenkaart, leverancierskaart en bankrekeningkaart, moet u een zakenrelatiecode selecteren voor klanten, leveranciers en bankrekeningen. U kunt bijvoorbeeld alleen een contact koppelen aan een bestaande klant als u een zakenrelatiecode voor klanten hebt geselecteerd in het venster **Marketinginstellingen**.

Zie voor meer informatie [Contacten synchroniseren met klanten, leveranciers en bankrekeningen](marketing-synchronize-contacts-customers-vendors-bank-accounts.md).

## <a name="assigning-a-number-series-to-contacts-and-opportunities"></a>Een nummerreeks toewijzen aan opportunity's en contacten
U kunt een nummerreeks instellen voor contacten en opportunities. Als u een nummerreeks hebt ingesteld voor contacten, wordt automatisch het volgende beschikbare contactnummer ingevoerd wanneer u een contact maakt en op Enter drukt in het veld Nr.

Zie voor meer informatie over nummerreeksen [Nummerreeksen maken](ui-create-number-series.md).

## <a name="searching-for-duplicate-contacts-when-contacts-are-created"></a>Dubbele contacten zoeken als contacten worden gemaakt
U kunt het programma automatisch laten zoeken naar dubbele records telkens wanneer u een contactbedrijf maakt, of u kunt ervoor kiezen handmatig te zoeken nadat u contacten hebt gemaakt. U kunt de zoekstrings ook automatisch laten bijwerken door het programma, telkens wanneer u contactgegevens wijzigt of een contact maakt. U kunt zelf het zoekresultaatpercentage bepalen, dat wil zeggen, het percentage van identieke strings dat twee contactpersonen moeten hebben zodat ze als dubbele records worden beschouwd.

## <a name="setting-up-email-logging"></a>E-mailregistratie instellen
U kunt e-mailberichten uitwisselen met bijvoorbeeld uw contacten, klanten of leveranciers. U kunt e-mailberichten vanuit de toepassing of vanuit Outlook verzenden en ontvangen. Voordat u op deze manier berichten kunt uitwisselen en deze op het systeem kunt laten opslaan en in de wachtrij plaatsen, moet u enkele parameters instellen, zoals de frequentie waarmee het programma controleert of er e-mailberichten zijn die moeten worden verwerkt en de profielnaam voor het bijhouden van e-mail.

## <a name="see-also"></a>Zie ook
[Contactpersonen beheren](marketing-contacts.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

