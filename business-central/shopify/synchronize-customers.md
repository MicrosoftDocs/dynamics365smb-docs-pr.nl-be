---
title: Klanten synchroniseren
description: Klanten importeren uit of exporteren naar Shopify
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 92ac46e9f7e69204b4c7edee4aa430a8786b6c0b
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768213"
---
# <a name="synchronize-customers"></a>Klanten synchroniseren

Wanneer een order uit Shopify wordt geïmporteerd, is de informatie over de klant essentieel voor de verdere verwerking van het document in [!INCLUDE[prod_short](../includes/prod_short.md)]. Er zijn twee hoofdopties en hun combinaties:

* Gebruik speciale klant voor alle orders.
* Importeer actuele klantinformatie uit Shopify. Deze optie is ook beschikbaar wanneer u een klant eerst exporteert naar Shopify vanuit [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="how-connector-chooses-which-customer-to-use"></a>Hoe connector kiest welke klant te gebruiken

De functie *Order importeren uit Shopify* probeert de klant in de volgende volgorde te selecteren:

1. Als het **Standaardklantnr.** is gedefinieerd in de **Shopify-klantsjabloon** voor het corresponderende land/regio, dan **Standaardklantnr.** wordt gebruikt, ongeacht de instellingen in **Klant importeren uit Shopify** en **Type klanttoewijzing**.
2. Als **Klant importeren uit Shopify** en **Standaardklantnr.** Is gedefinieerd, dan het **Standaardklantnr.** wordt gebruikt.

Volgende stappen zijn afhankelijk van **Type klanttoewijzing**.

* **Altijd de standaardklant nemen**, gebruik dan de klant die is gedefinieerd in het **Standaardklantnr.** veld in venster **Shopify-winkelkaart**.
* **Op e-mail/telefoon**, probeert de connector eerst een bestaande klant te vinden op id, vervolgens op e-mail en vervolgens op telefoon. Als de klant niet wordt gevonden, maakt de connector een nieuwe klant.
* **Op factureringsadresinfo**, probeert de connector eerst een bestaande klant te vinden op id en vervolgens op factuuradres. Als de klant niet wordt gevonden, maakt de connector een nieuwe klant.

> [!NOTE]  
> De connector gebruikt informatie van het factuuradres en creëert factuurklantgegevens [!INCLUDE[prod_short](../includes/prod_short.md)]. Orderklant is gelijk aan factuurklant.

## <a name="important-settings-when-importing-customers-from-shopify"></a>Belangrijke instellingen bij het importeren van klanten uit Shopify

Of u nu klanten uit Shopify in bulk importeert of samen met de import van orders, met de volgende instellingen kunt u het proces beheren:

|Veld|Omschrijving|
|------|-----------|
|**Klant importeren vanuit Shopify**|Selecteer **Alle klanten** als u van plan bent klanten in bulk te importeren vanuit Shopify ofwel handmatig met behulp van de actie **Klanten synchroniseren** of via de taakwachtrij voor terugkerende updates. Ongeacht de selectie wordt klantinformatie altijd samen met de order geïmporteerd. Het gebruik van deze informatie is echter afhankelijk van **Shopify-klantsjablonen** en instellingen in het veld **Type klanttoewijzing**.|
|**Type klanttoewijzing**|Definieer hoe u wilt dat de connector toewijzing uitvoert.<br>- **Op e-mail/telefoon** als u wilt dat de connector geïmporteerde Shopify-klanten toewijst aan bestaande klanten in [!INCLUDE[prod_short](../includes/prod_short.md)], met behulp van e-mailadres en telefoon.</br>- **Op factureringsadresinfo** als u wilt dat de connector geïmporteerde Shopify-klanten toewijst aan bestaande klanten in [!INCLUDE[prod_short](../includes/prod_short.md)], met behulp van adresgegevens van de partij die de factuur ontvangt.</br>Selecteer **Altijd de standaardklant nemen** als u wilt dat het systeem een klant uit het veld **Standaardklantnr.** gebruikt. |
|**Shopify kan klanten bijwerken**| Selecteer of u wilt dat de connector gevonden klanten bijwerkt wanneer de opties **Op e-mail/telefoon** of **Op factureringsadresinfo** zijn geselecteerd in het veld **Type klanttoewijzing**.|
|**Automatisch onbekende klanten maken**| Selecteer of u wilt dat de connector ontbrekende klanten maakt wanneer de opties **Op e-mail/telefoon** of **Op factureringsadresinfo** zijn geselecteerd in het veld **Type klanttoewijzing**. Er wordt een nieuwe klant gemaakt met behulp van geïmporteerde gegevens en **Klantensjablooncode** gedefinieerd op de pagina **Shopify-winkelkaart** of **Shopify-klantensjabloon**. Merk op dat de Shopify-klant minimaal één adres moet hebben. Als deze optie niet is ingeschakeld, moet u de klant handmatig maken en deze koppelen aan de Shopify-klant. U kunt het maken van een klant altijd handmatig starten vanuit de pagina **Shopify-order**.|
|**Klantensjablooncode**|Gebruikt samen met **Automatisch onbekende klanten maken**.<br> Kies de standaardsjabloon die moet worden gebruikt voor automatisch gemaakte klanten. U kunt sjablonen per land/regio definiëren in het venster **Shopify-klantensjablonen**, wat handig is voor een juiste belastingberekening. Zie [Opmerkingen over belasting](synchronize-orders.md#tax-remarks) voor meer informatie.|

### <a name="customer-template-per-country"></a>Klantensjabloon per land/regio

Sommige instellingen kunnen worden gedefinieerd op land/regio-niveau of op staats-/provinciaal niveau. De instellingen kunnen worden geconfigureerd in [Verzending en levering](https://www.shopify.com/admin/settings/shipping) bij Shopify.

Met de **Shopify-klantensjabloon** kunt u voor elk land/regio het volgende doen:

1. Specificeer het **Standaardklantnr.**, dat voorrang heeft op de selectie in de velden **Klant importeren uit Shopify** en **Type klanttoewijzing**. Het wordt gebruikt in de geïmporteerde verkooporder.
2. Definieer de **Klantensjablooncode**, die wordt gebruikt om ontbrekende klanten te maken als **Automatisch onbekende klanten maken** is ingeschakeld. Als **Klantensjablooncode** leeg is, gebruikt de functie **Klantensjablooncode**, gedefinieerd op de **Shopify-winkelkaart**.
3. In sommige gevallen is **Klantensjablooncode** per land/regio is niet voldoende om een juiste berekening van belastingen te garanderen. Bijvoorbeeld voor landen/regio's met sales tax.

> [!NOTE]  
> De land/regio-codes zijn ISO 3166-1 alpha-2-land/regio-codes. Zie voor meer informatie [Land/regio-code](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="export-customers-to-shopify"></a>Klanten exporteren naar Shopify

Bestaande klanten kunnen in bulk geëxporteerd worden naar Shopify. Hierdoor worden een klant en één standaardadres gemaakt. Met de volgende instellingen kunt u het proces beheren:

|Veld|Omschrijving|
|------|-----------|
|**Klanten exporteren naar Shopify**|Selecteer dit als u van plan bent alle klanten met een geldig e-mailadres in bulk te importeren vanuit [!INCLUDE[prod_short](../includes/prod_short.md)] naar Shopify ofwel handmatig met behulp van de actie **Klanten synchroniseren** of via de taakwachtrij voor terugkerende updates.|
|**Kan Shopify-klanten bijwerken**|Gebruikt samen met **Klant exporteren naar Shopify**. Schakel het in als u later updates wilt genereren vanuit [!INCLUDE[prod_short](../includes/prod_short.md)] voor klanten die al bestaan in Shopify.|

> [!NOTE]  
> Zodra u klanten hebt gemaakt in Shopify, wilt u misschien directe uitnodigingen naar klanten sturen. Het zal hen aanmoedigen om hun account te activeren.

### <a name="populate-customer-information-in-shopify"></a>Klantgegevens invullen in Shopify

Een klant in Shopify heeft voornaam, achternaam, e-mailadres en/of telefoonnummer. U kunt de voornaam en achternaam invullen op basis van de gegevens van de klantenkaart in [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioriteit|Veld op klantenkaart|Omschrijving|
|------|------|-----------|
|1|**Contactnaam**|Hoogste prioriteit, als het veld **Contactnaam** is ingevuld en het veld **Contactbron** op de **Shopify-winkelkaart** de opties *Voornaam en achternaam* of *Achternaam en voornaam* bevat, die bepalen hoe de waarden moeten worden gesplitst.|
|2|**Naam 2**|Als het veld **Naam 2** is ingevuld en het veld **Bron van naam 2** op de **Shopify-winkelkaart** de opties *Voornaam en achternaam* of *Achternaam en voornaam* bevat, die bepalen hoe de waarden moeten worden gesplitst.|
|3|**Naam**|Laagste prioriteit, als het veld **Contactnaam** is ingevuld en het veld **Naambron** op de **Shopify-winkelkaart** de opties *Voornaam en achternaam* of *Achternaam en voornaam* bevat, die bepalen hoe de waarden moeten worden gesplitst.|

Een klant in Shopify heeft ook een standaardadres, dat naast de voornaam, achternaam, e-mail en/of telefoon ook bedrijf en adres kan bevatten. U kunt het veld **Bedrijf** invullen gebaseerd op gegevens van de klantenkaart in [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioriteit|Veld op klantenkaart|Omschrijving|
|------|------|-----------|
|1|**Naam**|Hoogste prioriteit, als het veld **Naambron** op de **Shopify-winkelkaart** *Bedrijfsnaam* bevat.|
|2|**Naam 2**|Laagste prioriteit, als het veld **Bron van naam 2** op de **Shopify-winkelkaart** *Bedrijfsnaam* bevat.|

Voor adressen waar land/regio/provincie wordt gebruikt, selecteert u *Code* of *Naam* in het veld **Land/regio-bron** op de **Shopify-winkelkaart** om aan te geven welk type gegevens wordt opgeslagen in [!INCLUDE[prod_short](../includes/prod_short.md)], in het veld **Land/regio**.

## <a name="sync-customers"></a>Klanten synchroniseren

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-winkel** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u klanten wilt synchroniseren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Klanten synchroniseren**.

Of gebruik de actie **Synchronisatie van klanten starten** in het venster **Shopify-klanten** of zoek de batchverwerking **Klanten synchroniseren**.

## <a name="see-also"></a>Zie ook

[Aan de slag met de connector voor Shopify](get-started.md)  
