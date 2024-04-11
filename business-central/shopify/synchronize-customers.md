---
title: Klanten synchroniseren
description: Klanten importeren uit of exporteren naar Shopify
ms.date: 03/25/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30105, 30106, 30107, 30108, 30109,'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
---

# <a name="synchronize-customers-and-companies"></a>Klanten en bedrijven synchroniseren

Wanneer u een order uit Shopify importeert, is verkrijgen van de informatie over de klant essentieel voor de verdere verwerking van het document in [!INCLUDE[prod_short](../includes/prod_short.md)]. Er zijn twee hoofdopties hiervoor en verschillende combinaties:

* Gebruik een speciale klant voor alle orders.
* Importeer de klantinformatie uit Shopify. Deze optie is ook beschikbaar wanneer u klanten exporteert naar Shopify vanuit [!INCLUDE[prod_short](../includes/prod_short.md)].

Shopify stelt u in staat uw B2B- en DTC-activiteiten vanaf één plek te runnen met de kracht en het gemak van het alles-in-één-platform van Shopify. Shopify -connector werkt ook met verschillende smaken van e-Commerce.

Shopify werkt met de twee entiteiten klant en bedrijf, maar [!INCLUDE[prod_short](../includes/prod_short.md)] heeft alleen de klantentiteit, wat van invloed is op de manier waarop synchronisatie werkt.

Wanneer u DTC uitvoert, wordt de koper in Shopify aangemaakt als klant. Vervolgens wordt de klant geïmporteerd in [!INCLUDE[prod_short](../includes/prod_short.md)]  als een Shopify-klant, en gekoppeld of geconverteerd naar een klant.

Als u B2B uitvoert, wordt de koper aangemaakt in Shopify als een klant die verbonden is aan een bedrijf. De klant wordt geïmporteerd in [!INCLUDE[prod_short](../includes/prod_short.md)] als een Shopify-klant en het bedrijf wordt geïmporteerd in [!INCLUDE[prod_short](../includes/prod_short.md)] als een Shopify-bedrijf en gekoppeld of omgezet in een klant.

Om een ​​klant te exporteren uit [!INCLUDE[prod_short](../includes/prod_short.md)] naar Shopify, zijn de stappen enigszins verschillend, afhankelijk van wat u wilt doen:

* Exporteer een klant als een Shopify-klant voor DTC.
* Exporteer een klant als een bedrijf-en-klantenpaar voor de B2B-stroom.

## <a name="important-settings-when-importing-dtc-customers-from-shopify"></a>Belangrijke instellingen bij het importeren van DTC-klanten uit Shopify

Of u nu klanten uit Shopify in bulk importeert of samen met de import van orders, met de volgende instellingen kunt u het proces beheren:

|Veld|Omschrijving|
|------|-----------|
|**Klant importeren vanuit Shopify**|Selecteer **Alle klanten** als u van plan bent klanten in bulk te importeren vanuit Shopify ofwel handmatig met behulp van de actie **Klanten synchroniseren** of via de taakwachtrij voor terugkerende updates. Ongeacht de selectie wordt de klantinformatie altijd samen met de order geïmporteerd. Het gebruik van deze informatie is echter afhankelijk van de **Shopify-klantsjablonen** en instellingen in het veld **Type klanttoewijzing**.|
|**Type klanttoewijzing**|Definieer hoe u wilt dat de connector de toewijzing uitvoert.</br></br>- **Op e-mail/telefoon** als u wilt dat de connector met behulp van het e-mailaccount en telefoongegevens de geïmporteerde Shopify-klant toewijst aan een bestaande klant in Business Central.</br></br>- **Op factureringsadresinfo** als u wilt dat de connector het adres van de factuurontvanger gebruikt om de geïmporteerde Shopify-klant toe te wijzen aan een bestaande klant in Business Central.</br></br>Selecteer **Altijd de standaardklant nemen** als u wilt dat het systeem een klant uit het veld **Standaardklantnr.** gebruikt. |
|**Shopify kan klanten bijwerken**| Selecteer dit veld als u wilt dat de connector de gevonden klanten bijwerkt wanneer de opties **Op e-mail/telefoon** of **Op factureringsadresinfo** zijn geselecteerd in het veld **Type klanttoewijzing**.|
|**Automatisch onbekende klanten maken**| Selecteer dit veld als u wilt dat de connector ontbrekende klanten maakt wanneer de opties **Op e-mail/telefoon** of **Op factureringsadresinfo** zijn geselecteerd in het veld **Type klanttoewijzing**. Er wordt een nieuwe klant gemaakt met behulp van geïmporteerde gegevens en de **Klantensjablooncode** gedefinieerd op de pagina **Shopify-winkelkaart** of **Shopify-klantensjabloon**. Merk op dat de Shopify-klant minimaal één adres moet hebben. Bij orders die zijn gemaakt via het verkoopkanaal Shopify POS ontbreken vaak adresgegevens. Als deze optie niet is ingeschakeld, moet u een klant handmatig maken en deze koppelen aan de Shopify-klant.|
|**Klant-/bedrijfssjablooncode**|Gebruik dit veld samen met **Automatisch onbekende klanten maken**.</br></br> Kies de standaardsjabloon die moet worden gebruikt voor automatisch gemaakte klanten. Zorg ervoor dat de geselecteerde sjabloon de verplichte velden bevat, zoals de **Bedrijfsboekingsgroep**, **Klantboekingsgroep** en btw- of belastinggerelateerde velden.</br></br>U kunt sjablonen per land/regio definiëren op de pagina **Shopify-klantensjablonen**, wat handig is voor een juiste belastingberekening.</br></br>Meer informatie op [Belastingen instellen](setup-taxes.md).|

### <a name="customer-template-per-countryregion"></a>Klantensjabloon per land/regio

Sommige instellingen kunnen worden gedefinieerd op land/regio-niveau of op staat/provincie-niveau. De instellingen kunnen worden geconfigureerd in [Verzending en levering](https://www.shopify.com/admin/settings/shipping) in Shopify.

U kunt voor elke klant het volgende doen met behulp van de **Shopify-klantensjabloon**:

1. Specificeer het **Standaardklantnr.**, dat voorrang heeft op de selectie in de velden **Klant importeren uit Shopify** en **Type klanttoewijzing**. Het wordt gebruikt in de geïmporteerde verkooporder.
2. Definieer de **Klantensjablooncode**, die wordt gebruikt om ontbrekende klanten te maken als **Automatisch onbekende klanten maken** is ingeschakeld. Als de **Klantensjablooncode** leeg is, gebruikt de functie **de Klantensjablooncode**, gedefinieerd op de **Shopify-winkelkaart**. Het systeem probeert eerst een sjabloon te vinden voor de **Land-/regiocode** voor het standaardadres. Als het geen sjabloon vindt, gebruikt het het eerste adres.
3. In sommige gevallen is de **Klantensjablooncode** die is gedefinieerd voor een land/regio, niet voldoende om juiste berekening van belastingen te garanderen (bijvoorbeeld voor landen/regio's met sales tax). In dit geval kan **Belastinggebied** opnemen een nuttige aanvulling zijn.
4. Het veld **Belastinggebied** bevat ook een paar **Landcode** en **Naam van provincie**. Dit paar is handig wanneer de connector een code naar een naam moet converteren, of vice versa.

> [!NOTE]  
> De land/regio-codes zijn ISO 3166-1 alpha-2-land/regio-codes. Meer informatie op [Land/regio-code](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="important-settings-when-exporting-dtc-customers-to-shopify"></a>Belangrijke instellingen bij het exporteren van DTC-klanten naar Shopify

U kunt bestaande klanten in bulk exporteren naar Shopify. In elk geval worden een klant en één standaardadres gemaakt. U kunt het proces beheren met de volgende instellingen:

|Veld|Omschrijving|
|------|-----------|
|**Kan Shopify-klanten bijwerken**| Schakel deze optie in als u later updates wilt genereren vanuit Business Central voor klanten die al bestaan in Shopify.|

De volgende vereisten zijn voor het exporteren van een klant:

* De klant moet een geldig e-mailadres hebben.
* Zorg er bij het exporteren van klanten met adressen die provincies/staten bevatten, voor dat **ISO-code** is ingevuld voor landen/regio's.|
* Als land/regio is geselecteerd op de klantenkaart, gebruik dan de **ISO-code**. Voor lokale klanten, met blanco land/regio, gebruikt de Shopify-connector het land/de regio dat/die is opgegeven in de **Bedrijfsgegevens**.
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
|2|**Naam 2**|Als het veld **Naam 2** is ingevuld en het veld **Bron van naam 2** op de **Shopify-winkelkaart** de optie *Voornaam en achternaam* of *Achternaam en voornaam* bevat om te bepalen hoe de waarden moeten worden gesplitst.|
|3|**Naam**|Laagste prioriteit, als het veld **Contactnaam** is ingevuld en het veld **Naambron** op de **Shopify-winkelkaart** de optie *Voornaam en achternaam* of *Achternaam en voornaam* bevat, die bepalen hoe de waarden moeten worden gesplitst.|

Een klant in Shopify heeft ook een standaardadres. Het adres kan een bedrijf en adres bevatten, naast de voornaam, de achternaam, het e-mailadres en/of het telefoonnummer. U kunt het veld **Bedrijf** invullen gebaseerd op gegevens van de klantenkaart in [!INCLUDE[prod_short](../includes/prod_short.md)].

|Prioriteit|Veld op klantenkaart|Omschrijving|
|------|------|-----------|
|1|**Naam**|Hoogste prioriteit, als het veld **Naambron** op de **Shopify-winkelkaart** *Bedrijfsnaam* bevat.|
|2|**Naam 2**|Laagste prioriteit, als het veld **Bron van naam 2** op de **Shopify-winkelkaart** *Bedrijfsnaam* bevat.|

Voor adressen waar de regio/provincie wordt gebruikt, selecteert u **Code** of **Naam** in het veld **Regiobron** op de pagina **Shopify-winkelkaart**. De code of naam specificeert het type gegevens dat is opgeslagen in [!INCLUDE[prod_short](../includes/prod_short.md)] in het veld **Provincie**. Vergeet niet om klantsjablonen per land/regio te initialiseren, zodat de provinciecode/naam-toewijzing gereed is. 

## <a name="export-dtc-customers-to-shopify"></a>DTC-klanten exporteren naar Shopify

### <a name="initial-sync-of-customers-from-business-central-to-shopify"></a>Initiële synchronisatie van klanten van Business Central naar Shopify

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-klanten** in en kies de gerelateerde koppeling.
2. Kies de actie **Klant toevoegen**.
3. Voer in het veld **Winkelcode** de code in. Als u het venster **Shopify-klanten** opent vanaf de pagina **Winkelkaart**, wordt de winkelcode automatisch ingevuld.
4. Definieer desgewenst filters voor klanten. Filter bijvoorbeeld op Kand/-regiocode.
5. Klik op **OK**.

De resulterende klanten worden automatisch in Shopify gemaakt met adres.

> [!NOTE]  
> Bij de eerste synchronisatie van klanten uit [!INCLUDE[prod_short](../includes/prod_short.md)] naar Shopify, wordt niet rekening behouden met de instellingen voor **Kan Shopify-klanten bijwerken**.

### <a name="sync-customers"></a>Klanten synchroniseren

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkel** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de specifieke winkel waarvoor u klanten wilt synchroniseren.
3. Kies de actie **Klanten synchroniseren**.

Of gebruik de actie **Synchronisatie van klanten starten** in het venster **Shopify-klanten** of zoek de batchverwerking **Klanten synchroniseren**.

U kunt de volgende taken plannen om geautomatiseerd te worden uitgevoerd. Zie voor meer informatie [Periodieke taken plannen](background.md#to-schedule-recurring-tasks).

## <a name="b2b-companies"></a>B2B-bedrijven

Als u B2B gebruikt in Shopify, kunt u behalve klanten ook bedrijven aanmaken. U kunt één of meerdere individuele klanten aan een bedrijf koppelen. U kunt ook betalingsvoorwaarden, locaties en catalogi definiëren.

## <a name="important-settings-when-importing-b2b-companies-from-shopify"></a>Belangrijke instellingen bij het importeren van B2B-bedrijven uit Shopify

Of u nu bedrijven uit Shopify in bulk importeert of samen met de import van orders, met de instellingen in de volgende tabel kunt u het proces beheren:

|Veld|Omschrijving|
|------|-----------|
|**Bedrijf importeren vanuit Shopify**|Selecteer **Alle bedrijven** als u van plan bent klanten in bulk te importeren vanuit Shopify ofwel handmatig met behulp van de actie **Bedrijven synchroniseren** of via de taakwachtrij voor terugkerende updates. Ongeacht de selectie wordt de klantinformatie altijd samen met de order geïmporteerd. Het gebruik van deze informatie is echter afhankelijk van de **Shopify-bedrijfsjablonen** en instellingen in het veld **Type bedrijfstoewijzing**.|
|**Type bedrijfstoewijzing**|Definieer hoe u wilt dat de connector de toewijzing uitvoert.</br></br>- **Op e-mail/telefoon** als u wilt dat de connector de geïmporteerde Shopify-bedrijventoewijst aan een bestaande klant in Business Central, met behulp van e-mailadres en telefoon van de hoofdcontactpersoon.</br></br>- Selecteer **Altijd de standaardbedrijf nemen** als u wilt dat het systeem het bedrijf uit het veld **Standaardbedrijfsnr.** . |
|**Shopify kan bedrijf bijwerken**| Selecteer dit veld als u wilt dat de connector de gevonden klanten bijwerkt wanneer de optie **Op e-mail/telefoon** is geselecteerd in het veld **Type klanttoewijzing**.|
|**Automatisch onbekende bedrijven maken**| Selecteer dit veld als u wilt dat de connector nieuwe klanten maakt wanneer de optie **Op e-mail/telefoon** is geselecteerd in het veld **Type bedrijfstoewijzing**. Er wordt een nieuwe klant gemaakt met de geïmporteerde gegevens en de **Klant-/bedrijfsjablooncode** die is gedefinieerd op de pagina **Shopify-winkelkaart** of **Shopify-klantensjabloon**.|
|**Klant-/bedrijfssjablooncode**|Gebruik dit veld samen met **Automatisch onbekend bedrijf maken**.</br></br>- Kies de standaardsjabloon die moet worden gebruikt voor automatisch gemaakte klanten. Zorg ervoor dat de sjabloon de verplichte velden bevat, zoals de **Bedrijfsboekingsgroep**, **Klantboekingsgroep** en **Btw** of andere belastinggerelateerde velden.</br></br>- U kunt sjablonen per land/regio definiëren op de pagina **Shopify-klantensjablonen**, wat handig is voor een juiste belastingberekening.</br></br>Zie voor meer informatie [Belastingen instellen](setup-taxes.md).|

> [!NOTE]  
> Het bedrijf moet een hoofdcontactpersoon hebben. Anders gaat de connector verder naar bedrijf.
> Er wordt slechts één oudste locatie geïmporteerd.
> Alleen de hoofdcontactpersoon wordt geïmporteerd.

## <a name="important-settings-when-exporting-b2b-companies-to-shopify"></a>Belangrijke instellingen bij het exporteren van B2B-bedrijven naar Shopify

U kunt bestaande klanten in bulk als een bedrijf exporteren naar Shopify. In elk geval worden een bedrijf, één standaardlocatie en één hoofdcontactpersoon aangemaakt. Het is ook mogelijk om een ​​catalogus aan te maken.

|Veld|Omschrijving|
|------|-----------|
|**Kan Shopify-bedrijven bijwerken**| Schakel deze optie in als u later updates wilt genereren vanuit Business Central voor bedrijven die al bestaan in Shopify.|
|**Standaardmachtigingen van contact**| Geef op welke rechten aan de hoofdcontactpersoon moeten worden toegewezen. U kunt kiezen tussen **Geen**, **Alleen bestellen** en **Locatiebeheerder**.|
|**Automatisch catalogus maken**| Schakel deze optie in als u een catalogus wilt maken die alle producten bevat. Voor elk geëxporteerd bedrijf wordt een catalogus aangemaakt.|

## <a name="export-b2b-company-to-shopify"></a>B2B-bedrijf exporteren naar Shopify

### <a name="initial-sync-of-b2b-companies-from-business-central-to-shopify"></a>Initiële synchronisatie van B2B-bedrijven uit Business Central naar Shopify

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") Voer **Shopify-bedrijf** in en kies de gerelateerde koppeling.
2. Kies de actie **Bedrijf toevoegen**.
3. Voer in het veld **Winkelcode** de code in. Als u het venster **Shopify-bedrijf** opent vanaf de pagina **Winkelkaart**, wordt de winkelcode automatisch ingevuld.
4. Definieer desgewenst filters voor klanten. Filter bijvoorbeeld op Kand/-regiocode.
5. Klik op **OK**.

Het resulterende bedrijf worden automatisch in Shopify gemaakt.

> [!NOTE]  
> Bij de eerste synchronisatie van bedrijven uit [!INCLUDE[prod_short](../includes/prod_short.md)] naar Shopify, wordt niet rekening behouden met de instellingen voor **Kan Shopify-bedrijf bijwerken**.

### <a name="sync-b2b-company"></a>B2B-bedrij synchroniseren

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkel** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de specifieke winkel waarvoor u klanten wilt synchroniseren.
3. Kies de actie **Bedrijf synchroniseren**.

Of gebruik de actie **Bedrijf synchroniseren starten** op de pagina **Shopify-bedrijf** of zoek naar de batchverwerking **Bedrijf synchroniseren**.

U kunt de volgende taken plannen om geautomatiseerd uit te voeren. Zie voor meer informatie [Periodieke taken plannen](background.md#to-schedule-recurring-tasks).

## <a name="see-also"></a>Zie ook

[Aan de slag met de connector voor Shopify](get-started.md)  
