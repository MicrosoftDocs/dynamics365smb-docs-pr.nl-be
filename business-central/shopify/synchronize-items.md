---
title: Artikelen en voorraad synchroniseren
description: Synchronisaties van artikelen instellen en uitvoeren tussen Shopify en Business Central
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30116, 30117, 30126, 30127,'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# <a name="synchronize-items-and-inventory"></a>Artikelen en voorraad synchroniseren

De **artikelen** in [!INCLUDE[prod_short](../includes/prod_short.md)] zijn het equivalent van de *producten* in Shopify en omvatten fysieke goederen, digitale downloads, services en cadeaubonnen die u verkoopt. Er zijn twee belangrijke redenen om artikelen te synchroniseren:

1. Gegevensbeheer gebeurt voornamelijk in [!INCLUDE[prod_short](../includes/prod_short.md)]. U moet alle of sommige gegevens van daaruit exporteren naar Shopify en zichtbaar maken. U kunt de artikelnaam, beschrijving, afbeelding, prijzen, beschikbaarheid, varianten, leveranciersdetails en streepjescodes exporteren. Na het exporteren kunt u de artikelen bekijken of direct zichtbaar maken.
2. Wanneer een bestelling vanuit Shopify wordt geïmporteerd, is de informatie over artikelen essentieel voor de verdere verwerking van het document in [!INCLUDE[prod_short](../includes/prod_short.md)].

De voorgaande twee scenario's zijn altijd ingeschakeld.

Een derde scenario is het beheren van gegevens in Shopify maar die artikelen in bulk importeren naar [!INCLUDE[prod_short](../includes/prod_short.md)]. Dit scenario kan handig zijn voor gegevensmigratiegebeurtenissen, zoals wanneer u een bestaande online winkel wilt verbinden met een nieuwe [!INCLUDE[prod_short](../includes/prod_short.md)]-omgeving.

## <a name="define-item-synchronizations"></a>Artikelsynchronisaties definiëren

1. Kies het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") en voer **Shopify-winkel** in. Open de winkel waarvoor u de artikelsynchronisatie wilt configureren.
2. Kies in het veld **Artikel synchroniseren** de juiste optie.

   De volgende tabel beschrijft de opties.

|Optie|Omschrijving|
|------|-----------|
|**Leeg**| Producten worden geïmporteerd samen met de orders. Producten worden geëxporteerd naar Shopify als een gebruiker de actie **Artikel toevoegen** uitvoert vanuit de pagina **Shopify-producten**. Deze optie is het standaardproces.|
|**Naar Shopify**| Selecteer deze optie als u nadat de eerste synchronisatie is geactiveerd door de actie **Artikel toevoegen**, producten handmatig wilt bijwerken met de actie **Product synchroniseren** of via de taakwachtrij voor periodieke updates. Vergeet niet om het veld **Kan Shopify-producten bijwerken** in te schakelen. Als het niet is ingeschakeld, is dat gelijk aan de (standaardverwerkings)optie **Blanco**. Lees meer in de sectie [Artikelen exporteren naar Shopify](synchronize-items.md#export-items-to-shopify).|
|**Van Shopify**| Kies deze optie als u van plan bent producten in bulk te importeren vanuit Shopify; ofwel handmatig met behulp van de actie **Product synchroniseren** of via de taakwachtrij voor periodieke updates. Lees meer in de sectie [Artikelen importeren vanuit Shopify](synchronize-items.md#import-items-from-shopify).|

> [!NOTE]
> **Artikel synchroniseren** wijzigen van **Van Shopify** in **Naar Shopify** heeft alleen effect als u **Kan Shopify-producten bijwerken** inschakelt. 

## <a name="import-items-from-shopify"></a>Artikelen importeren vanuit Shopify

Eerst importeert u artikelen in bulk vanuit Shopify of samen met bestellingen om ze toe te voegen aan de tabellen **Shopify-product** en **Shopify-variant**. Wijs vervolgens geïmporteerde producten en varianten toe aan artikelen en varianten in [!INCLUDE[prod_short](../includes/prod_short.md)]. Met de volgende instellingen kunt u het proces beheren:

|Veld|Omschrijving|
|------|-----------|
|**Automatisch onbekende artikelen maken**|Wanneer Shopify-producten en -varianten worden geïmporteerd in [!INCLUDE[prod_short](../includes/prod_short.md)] , probeert de [!INCLUDE[prod_short](../includes/prod_short.md)]-functie altijd eerst de overeenkomende record in de artikellijst te vinden. **SKU-toewijzing** heeft invloed op hoe de matching wordt uitgevoerd en creëert een nieuw artikel en/of een nieuwe artikelvariant. Schakel deze optie in als u een nieuw artikel wilt maken of als er geen overeenkomende record bestaat. Het nieuwe artikel wordt gemaakt met geïmporteerde gegevens en de **Code van artikelsjabloon**. Als deze optie niet is ingeschakeld, moet u handmatig een artikel maken en de actie **Product toewijzen** gebruiken op de pagina **Shopify-producten**.|
|**Code van artikelsjabloon**|Gebruik dit veld met de schakelaar **Automatisch onbekende artikelen maken**.<br>Kies de sjabloon die u wilt gebruiken voor automatisch gemaakte artikelen.|
|**SKU-toewijzing**|Kies hoe u de **SKU**-waarde wilt gebruiken die uit Shopify wordt geïmporteerd tijdens het toewijzen en maken van artikelen/varianten. Lees meer in de sectie [Effect van SKU's van Shopify producten en barcodes op het toewijzen en maken van artikelen en varianten in Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).|
|**SKU-veldscheidingsteken**|Gebruik dit veld samen met **SKU-toewijzing** ingesteld op de optie **[Artikelnr. + variant](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central)**.<br>Definieer een scheidingsteken dat moet worden gebruikt om SKU te splitsen.<br>Als u in Shopify de variant met SKU '1000/001' zou maken, typt u dus '/' in het veld **SKU-veldscheidingsteken** om van het artikelnummer in [!INCLUDE[prod_short](../includes/prod_short.md)] '1000' te maken en de artikelvariantcode '001'.|
|**Prefix voor variant**|Gebruik dit samen met **SKU-toewijzing** ingesteld op de opties **Variant** of **Artikelnr. + variant** als alternatief wanneer de SKU die uit Shopify komt, leeg is.<br>Als u de artikelvariant automatisch wilt maken in [!INCLUDE[prod_short](../includes/prod_short.md)], moet u een waarde invoeren in **Code**. Standaard wordt de waarde gebruikt die is gedefinieerd in het SKU-veld dat wordt geïmporteerd uit Shopify. Als de SKU echter leeg is, wordt een code gegenereerd die begint met het gedefinieerde variantvoorvoegsel en "001".|
|**Shopify kan artikelen bijwerken**|Kies deze optie als u artikelen en/of varianten automatisch wilt bijwerken.|

### <a name="effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central"></a>Effect van Shopify-product-SKU's en barcodes op het toewijzen en maken van artikelen en varianten in Business Central

Wanneer producten worden geïmporteerd uit Shopify naar tabellen met **Shopify-producten** en **Shopify-varianten**, probeert [!INCLUDE[prod_short](../includes/prod_short.md)] bestaande records te vinden.

De volgende tabel geeft een overzicht van de verschillen tussen de opties in het veld **SKU-toewijzing**.

|Optie|Effect op toewijzing|Effect op maken|
|------|-----------------|------------------|
|**Leeg**|Het veld SKU wordt niet gebruikt in de routine voor artikeltoewijzing.|Geen effect op het maken van het artikel.<br>Deze optie voorkomt het maken van varianten. In een verkooporder wordt alleen het hoofdartikel gebruikt. Een variant kan nog steeds handmatig worden toegewezen op de pagina **Shopify-product**.|
|**Artikelnr.**|Kies dit als de SKU het artikelnummer bevat|Geen effect op het maken van een artikel zonder varianten. Voor een artikel met varianten wordt elke variant als een apart artikel gemaakt.<br>Als Shopify een product heeft met twee varianten en hun SKU's zijn '1000' en '2000', worden in [!INCLUDE[prod_short](../includes/prod_short.md)] twee artikelen gemaakt met de nummers '1000' en '2000'.|
|**Variantcode**|Het veld SKU wordt niet gebruikt in de routine voor artikeltoewijzing.|Geen effect op het maken van het artikel. Wanneer een artikelvariant wordt gemaakt, wordt de waarde van het veld SKU gebruikt als een code. Als de SKU leeg is, wordt een code gegenereerd met behulp van het veld **Prefix voor variant**.|
|**Artikelnr. + variant**|Selecteer deze optie als het SKU-veld een artikelnummer bevat en de artikelvariantcode wordt gescheiden door de waarde die is gedefinieerd in het veld **SKU-veldscheidingsteken**.|Wanneer een artikel wordt gemaakt, wordt het eerste deel van de waarde van het SKU-veld aangeduid als **Nr.** Als het veld SKU leeg is, wordt een artikelnummer gegenereerd met behulp van nummerreeksen gedefinieerd in het veld **Artikelsjablooncode** of **Artikelnummers** van de pagina **Voorraadinstellingen**.<br>Wanneer een artikel wordt gemaakt, gebruikt de variantfunctie het tweede deel van de waarde van het SKU-veld als **Code**. Als het veld SKU leeg is, wordt een code gegenereerd met behulp van het veld **Prefix voor variant**.|
|**Artikelnr. van leverancier**|Kies dit als het veld SKU het leveranciersartikelnummer bevat. In dit geval wordt het veld **Artikelnr. leverancier** niet gebruikt op de pagina **Artikelkaart**, maar wordt het **Artikelnr. van leverancier** uit de **Artikel-/leverancierscatalogus** gebruikt. Als de gevonden *Artikel-/leverancierscatalogus*-record een variantcode bevat, wordt die variantcode gebruikt om de Shopify-variant toe te wijzen.|Als er een corresponderende leverancier bestaat in [!INCLUDE[prod_short](../includes/prod_short.md)], wordt de SKU-waarde gebruikt als het **Artikelnr. van leverancier** op de pagina **Artikelkaart** en als de **Artikelreferentie** van het type *leverancier*. <br>Voorkomt het maken van varianten. Dit is handig wanneer u alleen het hoofdartikel in de verkooporder wilt gebruiken. U kunt nog steeds handmatig een variant toewijzen vanaf de pagina **Shopify-product**.|
|**Barcode**|Kies dit als het SKU-veld een barcode bevat. Er wordt gezocht onder **Artikelreferenties** van het type *streepjescode*. Als de gevonden artikelreferentierecord een variantcode bevat, wordt deze variantcode gebruikt om de Shopify-variant toe te wijzen.|Geen effect op het maken van het artikel. <br>Voorkomt het maken van varianten. Dit is handig wanneer u alleen het hoofdartikel in de verkooporder wilt gebruiken. U kunt nog steeds handmatig een variant toewijzen vanaf de pagina **Shopify-product**.|

De volgende tabel geeft een overzicht van het effect van het veld **Barcode**.

|Effect op toewijzing|Effect op maken|
|-----------------|------------------|
|Er wordt gezocht onder **Artikelreferenties** die een type barcode bevatten als de waarde die is gedefinieerd in het veld **Barcode** in Shopify. Als de gevonden artikelreferentierecord een variantcode bevat, wordt deze variantcode gebruikt om de Shopify-variant toe te wijzen.|De barcode wordt opgeslagen als **Artikelreferentie** voor het artikel en de artikelvariant.|

> [!NOTE]  
> U kunt toewijzing activeren van het geselecteerde product/de varianten door **Producttoewijzing zoeken** te kiezen of van alle geïmporteerde niet-toegewezen producten door **Toewijzingen zoeken** te kiezen.

## <a name="export-items-to-shopify"></a>Artikelen exporteren naar Shopify

Kies de elementen uit uw artikellijst die worden geëxporteerd naar Shopify. Gebruik de actie **Artikel toevoegen** op de pagina **Shopify-producten** om artikelen toe te voegen aan de lijst met Shopify-producten. 

>[!IMPORTANT]
>Het product wordt alleen toegevoegd aan het verkoopkanaal **Online winkel**. U moet producten publiceren naar andere verkoopkanalen, zoals Shopify POS, vanuit Shopify.

U beheert het proces van het exporteren van artikelen met deze instellingen:

|Veld|Omschrijving|
|------|-----------|
|**Uitgebreide tekst voor synchronisatieartikel**|Selecteer dit veld om de uitgebreide tekst van het artikel te synchroniseren. Aangezien het zal worden toegevoegd aan het veld **Beschrijving**, kan het HTML-code bevatten. |
|**Artikelkenmerken synchroniseren**|Selecteer dit veld om de artikelkenmerken te synchroniseren. Kenmerken worden opgemaakt als een tabel en opgenomen in het veld **Beschrijving** in Shopify.|
|**Marketingtekst van synchronisatieartikel**|Selecteer dit veld om marketingtekst voor het artikel te synchroniseren. Hoewel marketingtekst een soort beschrijving is, is het anders dan het veld **Beschrijving**. Het veld **Beschrijving** wordt meestal gebruikt als een beknopte weergavenaam om het product snel te identificeren. De marketingtekst daarentegen rijker en meer beschrijvend. Het doel is om marketing- en promotionele inhoud toe te voegen. Deze tekst kan dan worden gepubliceerd bij het artikel in Shopify. Er zijn twee manieren om de marketingtekst te maken. Gebruik Copilot, dat door AI gegenereerde tekst voor u voorstelt, of begin helemaal opnieuw.|
|**Taalcode**|Selecteer dit veld als u wilt dat de vertaalde versies worden gebruikt voor titel, kenmerken en uitgebreide tekst.|
|**SKU-toewijzing**|Kies hoe u het SKU-veld wilt invullen in Shopify. Ondersteunde opties zijn:<br> - **Artikelnr.** om het artikelnummer te gebruiken voor zowel producten als varianten.<br> - **Artikelnr. + variant** om een SKU te maken door waarden van twee velden samen te voegen. Voor artikelen zonder varianten wordt alleen het artikelnr. gebruikt.<br>- **Artikelnr. leverancier** om het artikelleveranciersnummer te gebruiken dat is gedefinieerd op de **artikelkaart** voor zowel producten als varianten.<br> - **Barcode** om het barcodetype van **Artikelreferentie** te gebruiken. Deze optie respecteert varianten.<br>Als **Kan Shopify producten bijwerken** is ingeschakeld, worden wijzigingen in het veld **SKU-toewijzing** doorgegeven aan Shopify na de volgende synchronisatie voor alle producten en varianten die vermeld staan op de pagina **Shopify-producten** pagina voor de geselecteerde winkel.|
|**SKU-veldscheidingsteken**|Definieer een scheidingsteken voor de optie **Artikelnr. + variant**.|
|**Voorraad getraceerd**| Kies hoe het systeem het veld **Voorraad bijhouden** moet vullen voor producten die worden geëxporteerd naar Shopify. U kunt de beschikbaarheidsinformatie bijwerken vanuit [!INCLUDE[prod_short](../includes/prod_short.md)] voor producten in Shopify waarvan voorraad traceren is ingeschakeld. Lees meer in de sectie [Voorraad](synchronize-items.md#sync-inventory-to-shopify).|
|**Standaardvoorraadbeleid**|Kies *Afwijzen* om negatieve voorraad aan de Shopify-kant te voorkomen. <br>Als **Kan Shopify producten bijwerken** is ingeschakeld, worden wijzigingen in het veld **Standaardvoorraadbeleid** doorgegeven aan Shopify na de volgende synchronisatie voor alle producten en varianten die vermeld staan op de pagina **Shopify-producten** voor de geselecteerde winkel.|
|**Kan Shopify-producten bijwerken**|Definieer dit veld als [!INCLUDE[prod_short](../includes/prod_short.md)] alleen artikelen kan maken of ook artikelen kan bijwerken. Selecteer deze optie als u nadat de eerste synchronisatie is geactiveerd door de actie **Artikel toevoegen**, producten handmatig wilt bijwerken met de actie **Product synchroniseren** of via de taakwachtrij voor periodieke updates. Vergeet niet **Naar Shopify** te selecteren in het veld **Artikel synchroniseren**.<br>**Kan Shopify-producten bijwerken** heeft geen invloed op de synchronisatie van prijzen, afbeeldingen of voorraadniveaus, die worden geconfigureerd door onafhankelijke besturingselementen.<br>Als **Kan Shopify-producten bijwerken** is ingeschakeld, worden de volgende velden aan de Shopify-zijde bijgewerkt op product- en indien nodig variantniveau: **SKU**, **Barcode** en **Gewicht**. De velden **Titel**, **Producttype**, **Leverancier** en **Beschrijving** op van productniveau worden ook bijgewerkt als geëxporteerde waarden niet leeg zijn. Voor de beschrijving betekent dit dat u een van de volgende schakelaars moet inschakelen: **Uitgebreide tekst voor synchronisatieartikel**, **Marketingtekst van synchronisatieartikel**, **Artikelkenmerken synchroniseren**. Bovendien moeten kenmerken, uitgebreide tekst of marketingtekst waarden hebben. Als het product varianten gebruikt, wordt indien nodig een variant toegevoegd of verwijderd. <br>Houd er rekening mee dat als het product in Shopify is geconfigureerd om een​variantmatrix te gebruiken die twee of meer opties combineert, de Shopify-connector geen variant voor dat product kan maken. Er is in [!INCLUDE[prod_short](../includes/prod_short.md)] geen manier om de optiematrix te definiëren. Daarom gebruikt de connector de **variantcode** als de enige optie. Shopify verwacht echter meerdere opties en weigert varianten te maken als informatie over tweede en andere opties ontbreekt. |

### <a name="fields-mapping-overview"></a>Overzicht van veldtoewijzing

|Shopify|Bron bij export vanuit [!INCLUDE[prod_short](../includes/prod_short.md)]|Doel bij import naar [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Status|Volgens het veld **Status voor gemaakte producten** op de **Shopify-winkelkaart**. Lees meer in de sectie [Ad-hocupdates van Shopify-producten](synchronize-items.md#ad-hoc-updates-of-shopify-products).|Niet gebruikt.|
|Title | **Beschrijving**. Als de taalcode is gedefinieerd en er een corresponderende artikelvertaling bestaat, wordt de artikelvertaling gebruikt in plaats van de beschrijving.|**Beschrijving**|
|Varianttitel | **Variantcode**.|**Beschrijving** van variant|
|Omschrijving|Combineert uitgebreide teksten, marketingtekst en kenmerken als u de corresponderende schakelaars op de Shopify-winkelkaart inschakelt. Respecteert de taalcode.|Niet gebruikt.|
|SEO-paginatitel|Vaste waarde: leeg. Lees meer in de sectie [Ad-hocupdates van Shopify-producten](synchronize-items.md#ad-hoc-updates-of-shopify-products).|Niet gebruikt.|
|SEO-metabeschrijving|Vaste waarde: leeg. Lees meer in de sectie [Ad-hocupdates van Shopify-producten](synchronize-items.md#ad-hoc-updates-of-shopify-products).|Niet gebruikt.|
|Media|**Afbeelding**. Lees meer in de sectie [Artikelafbeeldingen synchroniseren](synchronize-items.md#sync-item-images)|**Afbeelding**|
|Prijs|De berekening van de eindklantprijs omvat de eenheidsprijs van het artikel, de klantprijsgroep, de klantkortingsgroep en de valutacode. Lees meer in het gedeelte [Prijzen synchroniseren](synchronize-items.md#sync-prices-with-shopify)|**Eenheidsprijs**. De prijs wordt alleen geïmporteerd voor nieuw gemaakte artikelen, maar wordt niet bijgewerkt bij latere synchronisaties.|
|Prijs vergelijken|De berekening van de prijs zonder korting.|Niet gebruikt.|
|Kosten per artikel|**Kostprijs**|**Kostprijs**. De kostprijs wordt alleen geïmporteerd voor nieuw gemaakte artikelen en wordt niet bijgewerkt bij latere synchronisaties.|
|SKU|Lees hierover onder **SKU-toewijzing** in de sectie [Artikelen exporteren naar Shopify](synchronize-items.md#export-items-to-shopify).|Lees hier meer over in de sectie [Effect van SKU's van Shopify producten en barcodes op het toewijzen en maken van artikelen en varianten in Business Central](synchronize-items.md#effect-of-shopify-product-skus-and-barcodes-on-mapping-and-creating-items-and-variants-in-business-central).|
|Barcode|**Artikelreferenties** van het type barcode.|**Artikelreferenties** van het type barcode.|
|Voorraad wordt opgeslagen op| Afhankelijk van Shopify-winkelvestigingen. Als **Business Central-afhandelingsservices** het veld **Standaard** heeft ingeschakeld, wordt de voorraad opgeslagen en verzonden vanaf **Business Central-afhandelingsservices**, anders wordt de primaire Shopify-vestiging of meerdere vestigingen gebruikt.
| Niet gebruikt.|
|Te traceren aantal|Volgens het veld **Voorraad getraceerd** op de pagina **Shopify-winkelkaart**. Lees meer in de sectie [Voorraad](synchronize-items.md#sync-inventory-to-shopify). Alleen gebruikt wanneer u een product voor de eerste keer exporteert.|Niet gebruikt.|
|Doorgaan met verkopen wanneer niet op voorraad|Volgens het **Standaardvoorraadbeleid** op de **Shopify-winkelkaart**.|Niet gebruikt.|
|Type|**Beschrijving** van **Artikelcategoriecode**. Als het type niet is opgegeven in Shopify, wordt het toegevoegd als een aangepast type.|**Artikelcategoriecode**. Toewijzing op beschrijving.|
|Leverancier|**Naam** van leverancier uit **Leveranciersnr.**|**Leveranciersnr.** Toewijzing op naam.|
|Gewicht|**Brutogewicht**.|Niet gebruikt.|
|Belastbaar|Vaste waarde: ingeschakeld.|Niet gebruikt.|
|Belastingcodes|**Belastinggroepcode**. Alleen relevant voor omzetbelasting. Meer informatie op [Belastingen instellen](setup-taxes.md).|Niet gebruikt.|


### <a name="tags"></a>Labels

Bekijk de geïmporteerde labels in het feitenblok **Labels** op de pagina **Shopify-product**. Om labels te bewerken op dezelfde pagina kiest u de actie **Labels**.
Als de optie **Naar Shopify** is geselecteerd in het veld **Artikel synchroniseren**, worden toegewezen labels geëxporteerd naar Shopify bij de volgende synchronisatie.

## <a name="run-item-synchronization"></a>Artikelsynchronisatie uitvoeren

Volledige of gedeeltelijke artikelsynchronisatie kan op veel verschillende manieren worden uitgevoerd.

### <a name="initial-sync-of-items-from-business-central-to-shopify"></a>Initiële synchronisatie van artikelen van Business Central naar Shopify

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-producten** in en kies de gerelateerde koppeling.
2. Kies de actie **Artikelen toevoegen**.
3. Voer in het veld **Winkelcode** de code in. Als u het venster **Shopify-product** opent vanaf de pagina **Winkelkaart**, wordt de winkelcode automatisch ingevuld.
4. Als u synchronisatie van afbeeldingen en inventaris hebt geconfigureerd, kunt u deze in hetzelfde proces opnemen. Het opnemen ervan in hetzelfde proces is handig voor demoscenario's of wanneer het gaat om kleinere hoeveelheden gegevens. 
5. Definieer desgewenst filters voor artikelen. U kunt bijvoorbeeld filteren op artikelnummer of artikelcategoriecode.
6. Klik op **OK**.

De resulterende artikelen worden automatisch in Shopify gemaakt met prijzen. Afhankelijk van de keuzes die u hebt gemaakt, kunnen afbeeldingen en voorraadniveaus worden opgenomen. De bewerking kan enige tijd duren als er een groot aantal artikelen wordt toegevoegd.

### <a name="sync-products-from-shopify-to-business-central"></a>Producten synchroniseren vanuit Shopify naar Business Central

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-winkel** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u artikelen wilt synchroniseren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Producten synchroniseren**.

Of gebruik de actie **Producten synchroniseren** op de pagina **Shopify-producten** of zoek naar de batchverwerking **Producten synchroniseren**.

U kunt de volgende taken plannen om geautomatiseerd te worden uitgevoerd. Zie voor meer informatie [Periodieke taken plannen](background.md#to-schedule-recurring-tasks).

### <a name="url-and-preview-url"></a>URL en voorbeeld-URL

Artikel toegevoegd aan Shopify of geïmporteerd uit Shopify heeft mogelijk de **URL** of **Voorbeeld-URL** ingevuld. Het veld **URL** is leeg als het product niet in de online winkel is gepubliceerd, bijvoorbeeld omdat de status concept is. De **URL** zal leeg zijn als de winkel met een wachtwoord is beveiligd, bijvoorbeeld omdat dit een ontwikkelingswinkel is. In de meeste gevallen kunt u **Voorbeeld-URL** gebruiken om te controleren hoe het product er na publicatie uit zal zien.

### <a name="ad-hoc-updates-of-shopify-products"></a>Ad-hocupdates van Shopify-producten

Wanneer de records worden bijgewerkt in de tabel **Shopify-product**, worden de volgende wijzigingen gesynchroniseerd met Shopify.

Bijwerken:

* **Status** - u kunt kiezen tussen actief, gearchiveerd of concept.
* **SEO-titel**
* **SEO-beschrijving**

Verwijdering:

Op basis van de waarde in **Actie voor verwijderde producten** op de pagina **Shopify-winkelkaart** worden de producten bijgewerkt in Shopify wanneer de record wordt verwijderd vanaf de pagina **Shopify-producten**.

* **Leeg** - er gebeurt niets. Indien nodig moet de gebruiker de vereiste actie uitvoeren vanuit **Shopify-beheer**.
* **Status naar Concept** - de status van het product in Shopify wordt ingesteld op *Concept*.
* **Status naar Gearchiveerd** - het product wordt gearchiveerd in Shopify.

## <a name="sync-item-images"></a>Artikelafbeeldingen synchroniseren

Synchronisatie van afbeeldingen kan worden geconfigureerd voor gesynchroniseerde artikelen. Kies uit de volgende opties:

* **Uitgeschakeld** - afbeeldingssynchronisatie wordt gedeactiveerd.
* **Naar Shopify** - afbeeldingen van artikelen worden geëxporteerd naar Shopify
* **Van Shopify** - afbeeldingen vanuit Shopify worden geïmporteerd naar [!INCLUDE[prod_short](../includes/prod_short.md)]

Afbeeldingssynchronisatie kan op de hieronder beschreven twee manieren worden geïnitialiseerd.

### <a name="sync-product-images-from-the-shopify-shop-page"></a>Productafbeeldingen synchroniseren vanaf de pagina Shopify-winkel

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u afbeeldingen wilt synchroniseren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Productafbeeldingen synchroniseren**.

### <a name="sync-product-images-from-the-shopify-products-page"></a>Productafbeeldingen synchroniseren vanaf de pagina Shopify-producten

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-producten** in en kies de gerelateerde koppeling.
2. Kies de actie **Productafbeeldingen synchroniseren**.

### <a name="image-synchronization-remarks"></a>Opmerkingen over afbeeldingssynchronisatie

* Wanneer u afbeeldingen exporteert van [!INCLUDE[prod_short](../includes/prod_short.md)] naar Shopify, vervangen de afbeeldingen de afbeeldingen die u eerder hebt geëxporteerd. De eerdere afbeeldingen zijn niet langer beschikbaar.
* Als u een afbeelding in [!INCLUDE[prod_short](../includes/prod_short.md)] verwijdert, wordt de afbeelding in Shopify niet ook verwijderd. U moet de oude afbeeldingen handmatig verwijderen in de **Shopify-beheer**.
* Afbeeldingen die u naar Shopify exporteert, moeten voldoen aan de vereisten van Shopify. Anders kunt u ze niet importeren. Ga voor meer informatie over mediavereisten naar [productmediatypen op help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images).

## <a name="sync-prices-with-shopify"></a>Prijzen synchroniseren met Shopify

U beheert het proces van het exporteren van prijzen met deze instellingen:

|Veld|Omschrijving|
|------|-----------|
|**Klantenprijsgroep**|Bepaal de prijs voor een artikel in Shopify. De verkoopprijs van deze klantenprijsgroep wordt genomen. Als er geen groep is gespecificeerd, wordt de prijs op de artikelkaart gebruikt.|
|**Klantenkortingsgroep**|Bepaal de korting die moet worden gebruikt voor het berekenen van de prijs van een artikel in Shopify. Gereduceerde prijzen worden opgeslagen in het veld **Prijs** en de volledige prijs wordt opgeslagen in het veld **Prijs vergelijken**.|
|**Regelkorting toestaan**|Hiermee wordt opgegeven of u een regelkorting toestaat bij het berekenen van prijzen voor Shopify. Deze instelling is alleen van toepassing op prijzen van het artikel. Prijzen voor de klantprijsgroep hebben hun eigen schakelaar op regels.|
|**Prijzen inclusief btw**|Specificeert of prijsberekeningen voor Shopify btw bevatten. Meer informatie op [Belastingen instellen](setup-taxes.md).|
|**Btw-bedrijfsboekingsgroepen**|Hiermee wordt opgegeven welke btw-bedrijfsboekingsgroep wordt gebruikt om de prijzen te berekenen in Shopify. Dit moet de groep zijn die u gebruikt voor binnenlandse klanten. Meer informatie op [Belastingen instellen](setup-taxes.md).|
|**Valutacode**|Voer alleen een Valutacode in als uw online winkel een andere valuta gebruikt dan de lokale valuta (LV). Voor de opgegeven valuta moeten wisselkoersen zijn geconfigureerd. Als uw online winkel dezelfde valuta gebruikt als [!INCLUDE[prod_short](../includes/prod_short.md)], laat u het veld leeg.|

U kunt prijzen voor gesynchroniseerde artikelen exporteren op de twee hieronder beschreven manieren.

### <a name="sync-prices-from-the-shopify-products-page"></a>Prijzen synchroniseren vanaf de pagina Shopify-producten

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-producten** in en kies de gerelateerde koppeling.
2. Kies de actie **Prijzen synchroniseren met Shopify**.

### <a name="price-calculation-remarks"></a>Opmerkingen over prijsberekening

* Bij het bepalen van een prijs gebruikt [!INCLUDE[prod_short](../includes/prod_short.md)] 'laagste prijs'-logica. De logica voor de laagste prijs negeert echter de eenheidsprijs die is gedefinieerd op de artikelkaart als er een prijs is gedefinieerd in de prijsgroep. Dit geldt zelfs als de eenheidsprijs van de artikelkaartprijs lager is.
* Om prijzen te berekenen, maakt de connector een tijdelijke verkoopofferte voor het artikel met een hoeveelheid van 1 en gebruikt standaard prijsberekeningslogica. Alleen prijzen en kortingen die gelden voor hoeveelheid 1 worden gebruikt. U kunt geen verschillende prijzen of kortingen exporteren op basis van hoeveelheid.

## <a name="sync-inventory-to-shopify"></a>Voorraad synchroniseren met Shopify

Voorraad synchronisatie kan worden geconfigureerd voor reeds gesynchroniseerde artikelen. Er zijn twee voorwaarden waaraan moet worden voldaan:

1. Voorraad bijhouden moet zijn ingeschakeld voor een product in Shopify. Als artikelen worden geëxporteerd naar Shopify, overweeg dan **Voorraad getraceerd** in te schakelen op de pagina **Shopify-winkel**. Lees meer in de sectie [Artikelen exporteren naar Shopify](synchronize-items.md#export-items-to-shopify).
2. Voorraadsynchronisatie moet zijn ingeschakeld voor **Shopify-vestigingen**.

### <a name="to-enable-inventory-sync"></a>Voorraadsynchronisatie inschakelen

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-winkel** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u voorraad wilt synchroniseren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Vestigingen** om **Shopify-winkellocaties** te openen.
4. Kies de actie **Shopify-vestigingen ophalen** om alle locaties te importeren die zijn gedefinieerd in Shopify. U vindt ze in de [**Vestigingen**](https://www.shopify.com/admin/settings/locations)-instellingen in uw **Shopify beheer**.
5. Voeg in het veld **Locatiefilter** locaties toe als u alleen voorraad van specifieke locaties wilt opnemen. U kunt bijvoorbeeld *OOST|WEST* invoeren, om alleen voorraad van deze twee vestigingen beschikbaar te maken voor verkoop via de online winkel.
6. Selecteer de voorraadberekeningsmethode die u wilt gebruiken voor de geselecteerde Shopify-vestigingen.
7. Schakel **Standaard** in als u wilt dat de vestiging wordt gebruikt voor het maken van voorraadrecords en voor deelname aan de inventarissynchronisatie. Activeer **Standaard** voor **Business Central-afhandelingsservices** om een voorraadrecord te maken die de afhandelingsservice vertegenwoordigt, anders wordt er een voorraadrecord gemaakt voor de primaire Shopify-vestiging en alle normale vestigingen waar **Standaard** is ingeschakeld.


U kunt afbeeldingssynchronisatie op de hieronder beschreven twee manieren initialiseren.

### <a name="sync-inventory-from-the-shopify-shop-page"></a>Voorraad synchroniseren vanaf de pagina Shopify-winkel

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u voorraad wilt synchroniseren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Voorraad synchroniseren**.

### <a name="sync-inventory-from-the-shopify-products-page"></a>Voorraad synchroniseren vanaf de pagina Shopify-producten

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-producten** in en kies de gerelateerde koppeling.
2. Kies de actie **Voorraad synchroniseren**.

### <a name="inventory-remarks"></a>Opmerkingen over voorraad

* De standaardvoorraadberekeningsmethode is **Voorspelde beschikbare voorraad op datum**. Met uitbreidbaarheid kunt u meer opties toevoegen. Ga voor meer informatie over uitbreidbaarheid naar [voorbeelden](/dynamics365/business-central/dev-itpro/developer/devenv-extending-shopify#stock-calculation). 
* U kunt de voorraadinformatie inspecteren die u hebt ontvangen van Shopify op de pagina **Feitenblok Shopify-voorraad**. In dit feitenblok krijgt u een overzicht van de Shopify-voorraad en de laatst berekende voorraad in [!INCLUDE[prod_short](../includes/prod_short.md)]. Er is één record per vestiging.
* Als de voorraadinformatie in Shopify verschilt van **Voorspelde beschikbare voorraad** in [!INCLUDE[prod_short](../includes/prod_short.md)], wordt de voorraad bijgewerkt in Shopify.
* Wanneer u een nieuwe locatie toevoegt in Shopify, moet u er ook inventarisrecords voor toevoegen. Shopify doet dat niet automatisch voor bestaande producten en varianten, en de connector synchroniseert geen voorraadniveaus voor dergelijke artikelen op een nieuwe vestiging. Ga voor meer informatie naar [Voorraad toewijzen aan vestigingen](https://help.shopify.com/manual/locations/assigning-inventory-to-locations).
* Zowel **Business Central-afhandelingsservices** als normale vestigingen worden ondersteund en kunnen worden gebruikt voor verzending en voorraad.

#### <a name="example-of-calculation-of-projected-available-balance"></a>Voorbeeld van berekening van voorspeld beschikbaar saldo

Er zijn tien stuks van artikel A beschikbaar en twee openstaande verkooporders. Eén voor maandag met aantal *Eén* en één voor donderdag met aantal *Twee*. Afhankelijk van wanneer u de voorraad synchroniseert, werkt het systeem het voorraadniveau in Shopify bij met verschillende hoeveelheden:

|Wanneer voorraadsynchronisatie wordt uitgevoerd|Waarde gebruikt om het voorraadniveau bij te werken|Opmerking|
|------|-----------------|-----------------|
|Dinsdag|9|Voorraad tien minus verkooporder ingesteld op verzending op maandag|
|Vrijdag|7|Voorraad tien minus beide verkooporders|

## <a name="see-also"></a>Zie ook

[Aan de slag met de connector voor Shopify](get-started.md)  
