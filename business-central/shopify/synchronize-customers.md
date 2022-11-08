---
title: Klanten synchroniseren
description: Klanten importeren uit of exporteren naar Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 30105, 30106, 30107, 30108, 30109,
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 1a796d1094401cd2ebc0efd54f752211d22bfb12
ms.sourcegitcommit: 5bb13966e9ba8d7a3c2f00dd32f167acccf90b82
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728666"
---
# <a name="synchronize-customers"></a>Klanten synchroniseren

Wanneer een order uit Shopify wordt geïmporteerd, is verkrijgen van de informatie over de klant essentieel voor de verdere verwerking van het document in [!INCLUDE[prod_short](../includes/prod_short.md)]. Dit zijn de twee hoofdopties hiervoor en hun combinaties:

* Gebruik een speciale klant voor alle orders.
* Importeer de actuele klantinformatie uit Shopify. Deze optie is ook beschikbaar wanneer u klanten eerst exporteert naar Shopify vanuit [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="important-settings-when-importing-customers-from-shopify"></a>Belangrijke instellingen bij het importeren van klanten uit Shopify

Of u nu klanten uit Shopify in bulk importeert of tegelijk met de import van orders, met de volgende instellingen kunt u het proces beheren:

|Veld|Omschrijving|
|------|-----------|
|**Klant importeren vanuit Shopify**|Selecteer **Alle klanten** als u van plan bent klanten in bulk te importeren vanuit Shopify ofwel handmatig met behulp van de actie **Klanten synchroniseren** of via de taakwachtrij voor terugkerende updates. Ongeacht de selectie wordt de klantinformatie altijd samen met de order geïmporteerd. Het gebruik van deze informatie is echter afhankelijk van de **Shopify-klantsjablonen** en instellingen in het veld **Type klanttoewijzing**.|
|**Type klanttoewijzing**|Definieer hoe u wilt dat de connector de toewijzing uitvoert.<br>- **Op e-mail/telefoon** als u wilt dat de connector de geïmporteerde Shopify-klanten toewijst aan een bestaande klant in [!INCLUDE[prod_short](../includes/prod_short.md)], met behulp van e-mailadres en telefoon.</br>- **Op factureringsadresinfo** als u wilt dat de connector het adres van de factuurontvanger gebruikt om de geïmporteerde Shopify-klant toe te wijzen aan een bestaande klant in [!INCLUDE[prod_short](../includes/prod_short.md)].</br>- Selecteer **Altijd de standaardklant nemen** als u wilt dat het systeem een klant uit het veld **Standaardklantnr.** gebruikt. |
|**Shopify kan klanten bijwerken**| Selecteer dit veld als u wilt dat de connector de gevonden klanten bijwerkt wanneer de opties **Op e-mail/telefoon** of **Op factureringsadresinfo** zijn geselecteerd in het veld **Type klanttoewijzing**.|
|**Automatisch onbekende klanten maken**| Selecteer dit veld als u wilt dat de connector ontbrekende klanten maakt wanneer de opties **Op e-mail/telefoon** of **Op factureringsadresinfo** zijn geselecteerd in het veld **Type klanttoewijzing**. Er wordt een nieuwe klant gemaakt met behulp van geïmporteerde gegevens en de **Klantensjablooncode** gedefinieerd op de pagina **Shopify-winkelkaart** of **Shopify-klantensjabloon**. Merk op dat de Shopify-klant minimaal één adres moet hebben. Als deze optie niet is ingeschakeld, moet u een klant handmatig maken en deze koppelen aan de Shopify-klant. U kunt het maken van een klant altijd handmatig starten vanuit de pagina **Shopify-order**.|
|**Klantensjablooncode**|Dit veld wordt gebruikt samen met **Automatisch onbekende klanten maken**.<br>- Kies de standaardsjabloon die moet worden gebruikt voor automatisch gemaakte klanten. Zorg ervoor dat de geselecteerde sjabloon de verplichte velden bevat, zoals de **Bedrijfsboekingsgroep**, **Klantboekingsgroep** en btw- of belastinggerelateerde velden.<br>- U kunt sjablonen per land/regio definiëren op de pagina **Shopify-klantensjablonen**, wat handig is voor een juiste belastingberekening. <br>- Meer informatie op [Belastingen instellen](setup-taxes.md).|

### <a name="customer-template-per-country"></a>Klantensjabloon per land/regio

Sommige instellingen kunnen worden gedefinieerd op land/regio-niveau of op staat/provincie-niveau. De instellingen kunnen worden geconfigureerd in [Verzending en levering](https://www.shopify.com/admin/settings/shipping) in Shopify.

U kunt voor elke klant het volgende doen met behulp van de **Shopify-klantensjabloon**:

1. Specificeer het **Standaardklantnr.**, dat voorrang heeft op de selectie in de velden **Klant importeren uit Shopify** en **Type klanttoewijzing**. Het wordt gebruikt in de geïmporteerde verkooporder.
2. Definieer de **Klantensjablooncode**, die wordt gebruikt om ontbrekende klanten te maken als **Automatisch onbekende klanten maken** is ingeschakeld. Als de **Klantensjablooncode** leeg is, gebruikt de functie **de Klantensjablooncode**, gedefinieerd op de **Shopify-winkelkaart**.
3. Definiëren of prijzen inclusief belasting/btw voor geïmporteerde orders zijn.
4. In sommige gevallen is de **Klantensjablooncode** die is gedefinieerd voor een land/regio, niet voldoende om de juiste berekening van belastingen te garanderen (bijvoorbeeld voor landen/regio's met sales tax). In dit geval kan **Belastinggebieden** opnemen een nuttige aanvulling zijn.

> [!NOTE]  
> De land/regio-codes zijn ISO 3166-1 alpha-2-land/regio-codes. Meer informatie op [Land/regio-code](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="export-customers-to-shopify"></a>Klanten exporteren naar Shopify

U kunt bestaande klanten in bulk exporteren naar Shopify. In elk geval worden een klant en één standaardadres gemaakt. U kunt het proces beheren met de volgende instellingen:

|Veld|Omschrijving|
|------|-----------|
|**Klanten exporteren naar Shopify**|Selecteer dit als u alle klanten in bulk wilt exporteren vanuit [!INCLUDE[prod_short](../includes/prod_short.md)] naar Shopify. U kunt het handmatig doen, met behulp van de actie **Klanten synchroniseren** of automatisch, met behulp van een taakwachtrij voor periodieke updates.<br> Zorg er bij het exporteren van klanten met adressen die provincies/staten bevatten, voor dat **ISO-code** is ingevuld voor landen/regio's.|
|**Kan Shopify-klanten bijwerken**|Dit wordt gebruikt samen met de instelling **Klant exporteren naar Shopify**. Schakel het in als u later updates wilt genereren vanuit [!INCLUDE[prod_short](../includes/prod_short.md)] voor klanten die al bestaan in Shopify.|

De volgende vereisten zijn voor het exporteren van een klant:

* De klant moet een geldig e-mailadres hebben.
* Een land/regio is geselecteerd op de klantenkaart. Voor lokale klanten, met blanco land/regio, moet voor het land/regio dat is opgegeven op de pagina **Bedrijfsgegevens** een ISO-code zijn gedefinieerd.
* Als de klant een telefoonnummer heeft, moet het nummer uniek zijn omdat Shopify geen tweede klant met hetzelfde telefoonnummer accepteert.
* Als de klant een telefoonnummer heeft, moet dit het E.164-formaat hebben. Verschillende formaten worden ondersteund als ze een nummer vertegenwoordigen dat overal ter wereld kan worden gebeld. De volgende formaten zijn geldig:
  * xxxxxxxxxx
  * +xxxxxxxxxxx
  * (xxx)xxx-xxxx
  * +x xxx-xxx-xxxx

Zodra u de klanten hebt gemaakt in Shopify, kunt u ze rechtstreekse uitnodigingen sturen om hen aan te moedigen hun account te activeren.

### <a name="populate-customer-information-in-shopify"></a>Klantgegevens invullen in Shopify

Een klant in Shopify heeft een voornaam, achternaam, e-mailadres en/of telefoonnummer. U kunt de voornaam en achternaam invoeren op basis van de klantenkaart in [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioriteit|Veld op klantenkaart|Omschrijving|
|------|------|-----------|
|1|**Contactnaam**|Hoogste prioriteit, als het veld **Contactnaam** is ingevuld en het veld **Contactbron** op de **Shopify-winkelkaart** de optie *Voornaam en achternaam* of *Achternaam en voornaam* bevat, die bepalen hoe de waarden moeten worden gesplitst.|
|2|**Naam 2**|Als het veld **Naam 2** is ingevuld en het veld **Bron van naam 2** op de **Shopify-winkelkaart** de optie *Voornaam en achternaam* of *Achternaam en voornaam* bevat, die bepalen hoe de waarden moeten worden gesplitst.|
|3|**Naam**|Laagste prioriteit, als het veld **Contactnaam** is ingevuld en het veld **Naambron** op de **Shopify-winkelkaart** de optie *Voornaam en achternaam* of *Achternaam en voornaam* bevat, die bepalen hoe de waarden moeten worden gesplitst.|

Een klant in Shopify heeft ook een standaardadres, dat een bedrijf en adres kan bevatten, naast de voornaam, de achternaam, het e-mailadres en/of het telefoonnummer. U kunt het veld **Bedrijf** invullen gebaseerd op gegevens van de klantenkaart in [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioriteit|Veld op klantenkaart|Omschrijving|
|------|------|-----------|
|1|**Naam**|Hoogste prioriteit, als het veld **Naambron** op de **Shopify-winkelkaart** *Bedrijfsnaam* bevat.|
|2|**Naam 2**|Laagste prioriteit, als het veld **Bron van naam 2** op de **Shopify-winkelkaart** *Bedrijfsnaam* bevat.|

Voor adressen waar het land/de provincie wordt gebruikt, selecteert u *Code* of *Naam* in het veld **Land/regio-bron** op de **Shopify-winkelkaart**. Dit specificeert het type gegevens dat is opgeslagen in [!INCLUDE[prod_short](../includes/prod_short.md)] in het veld **Land**.

## <a name="sync-customers"></a>Klanten synchroniseren

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkel** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de specifieke winkel waarvoor u klanten wilt synchroniseren.
3. Kies de actie **Klanten synchroniseren**.

Of gebruik de actie **Synchronisatie van klanten starten** in het venster **Shopify-klanten** of zoek de batchverwerking **Klanten synchroniseren**.

U kunt de volgende taken plannen om geautomatiseerd te worden uitgevoerd. Zie voor meer informatie [Periodieke taken plannen](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Zie ook

[Aan de slag met de connector voor Shopify](get-started.md)  
