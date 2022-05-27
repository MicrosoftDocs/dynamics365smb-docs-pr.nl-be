---
title: Artikelen en voorraad synchroniseren
description: Synchronisaties van artikelen instellen en uitvoeren tussen Shopify en Business Central
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: fac1a3df12070a2030d6d2d8dfd5e740d8cca4f9
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768190"
---
# <a name="synchronize-items-and-inventory"></a>Artikelen en voorraad synchroniseren

De **artikelen** in [!INCLUDE[prod_short](../includes/prod_short.md)] zijn gelijk aan de *producten* in Shopify, waaronder fysieke goederen, digitale downloads, services en cadeaubonnen die u verkoopt. Er zijn twee belangrijke redenen om de artikelen te synchroniseren:

1. Het gegevensbeheer vindt in de eerste plaats plaats in [!INCLUDE[prod_short](../includes/prod_short.md)]. U moet alle of sommige gegevens exporteren naar Shopify en het zichtbaar maken. U kunt artikelnaam, beschrijving, afbeelding, prijzen, beschikbaarheid, varianten, leveranciersdetails en streepjescodes exporteren. Eenmaal geïmporteerd kunnen de artikelen direct zichtbaar worden of ze kunnen eerst worden beoordeeld en verbeterd door een verantwoordelijke persoon.
2. Wanneer een bestelling van Shopify wordt geïmporteerd, is de informatie over artikelen essentieel voor de verdere verwerking van het document in [!INCLUDE[prod_short](../includes/prod_short.md)].

Deze twee scenario's zijn altijd ingeschakeld.

Een ander scenario is wanneer gegevens worden beheerd in Shopify en u wilt die artikelen in bulk importeren naar [!INCLUDE[prod_short](../includes/prod_short.md)]. Dit scenario kan handig zijn voor gegevensmigratiegebeurtenissen, wanneer een bestaande online winkel moet worden verbonden met een nieuwe [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="to-define-item-synchronizations"></a>Artikelsynchronisaties definiëren

1. Kies het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") en voer **Shopify-winkel** in. Open een winkel waarvoor u artikelsynchronisatie wilt configureren.
2. Kies in het veld **Artikel synchroniseren** de juiste optie. <br>De volgende tabel geeft een overzicht van het verschil tussen de opties.

|Optie|Omschrijving|
|------|-----------|
|**Leeg**| Producten worden geïmporteerd samen met import van bestellingen. Producten worden geëxporteerd naar Shopify als de gebruiker de actie **Artikel toevoegen** uitvoert vanuit het venster **Shopify-producten**. Dit is het standaardgedrag. |
|**Naar Shopify**| Selecteer deze optie als u na de eerste synchronisatie, geactiveerd door de actie **Artikel toevoegen**, producten handmatig wilt bijwerken met de actie **Product synchroniseren** of via de taakwachtrij voor terugkerende updates. Vergeet niet om het veld **Kan Shopify-producten bijwerken** in te schakelen. Indien niet ingeschakeld is het gelijk aan de optie **Leeg**. |
|**Van Shopify**| Kies deze optie als u van plan bent producten in bulk te importeren vanuit Shopify; ofwel handmatig met behulp van de actie **Product synchroniseren** of via de taakwachtrij voor terugkerende updates. Als er geen optie is geselecteerd, is dit gelijk aan de optie **Leeg**.|

## <a name="import-items-from-shopify"></a>Artikelen importeren vanuit Shopify

Ofwel u importeert artikelen vanuit Shopify in bulk of samen met import van bestellingen. Deze artikelen worden eerst toegevoegd aan de tabellen **Shopify-product** en **Shopify-variant**. Met de volgende instellingen kunt u het proces beheren:

|Veld|Omschrijving|
|------|-----------|
|**Automatisch onbekende artikelen maken**|Wanneer Shopify-producten en -varianten worden geïmporteerd naar [!INCLUDE[prod_short](../includes/prod_short.md)], probeert de functie [!INCLUDE[prod_short](../includes/prod_short.md)] altijd eerst een overeenkomende record in de artikellijst te vinden. **SKU-toewijzing** heeft invloed op hoe de matching wordt uitgevoerd en creëert een nieuw artikel en/of een nieuwe artikelvariant. Zie [Producttoewijzing](synchronize-items.md#) voor meer informatie. Schakel deze optie in als u een nieuw artikel wilt maken of als er geen overeenkomende record bestaat. Het nieuwe artikel wordt gemaakt met geïmporteerde gegevens en **Code van artikelsjabloon**. Als deze optie niet is ingeschakeld, moet u handmatig een artikel maken en de actie **Product toewijzen** gebruiken vanuit de pagina **Shopify-producten**.|
|**Code van artikelsjabloon**|Gebruikt samen met **Automatisch onbekende artikelen maken**. <br> Kies de sjabloon die moet worden gebruikt voor automatisch gemaakte artikelen.|
|**SKU-toewijzing**|Kies hoe u de **SKU**-waarde wilt gebruiken die uit Shopify wordt geïmporteerd tijdens het toewijzen en maken van artikelen/varianten. Zie voor meer informatie [Hoe SKU en barcode, gedefinieerd in een Shopify-product, van invloed zijn op het toewijzen en maken van artikelen en varianten](synchronize-items.md#how-sku-and-barcode-defined-in-shopify-product-affects-mapping-and-creation-of-items-and-variants-in-business-central)|
|**SKU-veldscheidingsteken**|Gebruikt samen met **SKU-toewijzing** ingesteld op de optie **Artikelnr. + Variant**.<br> Definieer een scheidingsteken dat moet worden gebruikt om SKU's te splitsen. <br>Als u in Shopify bijvoorbeeld de variant met SKU '1000/001' maakt, typt u '/' in het veld **SKU-veldscheidingsteken** om het artikelnummer in [!INCLUDE[prod_short](../includes/prod_short.md)] te krijgen als '1000' en de artikelvariantcode als '001'.
|**Prefix voor variant**|Gebruikt samen met **SKU-toewijzing** ingesteld op de opties **Variant** of **Artikelnr. + Variant** als oplossing wanneer de SKU uit Shopify leeg is.<br>Als u de artikelvariant automatisch wilt maken in [!INCLUDE[prod_short](../includes/prod_short.md)], moet u een waarde invoeren in **Code**. Standaard wordt de waarde gebruikt die is gedefinieerd in het SKU-veld dat wordt geïmporteerd uit Shopify. Als de SKU echter leeg is, wordt een code gegenereerd die begint met het gedefinieerde variantvoorvoegsel en "001".|
|**Shopify kan artikelen bijwerken**| Kies deze optie als u artikelen en/of varianten automatisch wilt bijwerken.|

### <a name="how-skus-and-barcodes-defined-in-shopify-product-affects-mapping-and-creation-of-items-and-variants-in-business-central"></a>Hoe SKU en barcode, gedefinieerd in een Shopify-product, van invloed zijn op het toewijzen en maken van artikelen en varianten in Business Central

Wanneer producten worden geïmporteerd uit Shopify naar tabellen met **Shopify-producten** en **Shopify-varianten**, probeert [!INCLUDE[prod_short](../includes/prod_short.md)] bestaande records te vinden. De volgende tabel geeft een overzicht van het verschil tussen de opties in het veld **SKU-toewijzing**.

|Optie|Effect op toewijzing|Effect op maken|
|------|-----------------|------------------|
|**Leeg**|Het veld SKU wordt niet gebruikt in de routine voor artikeltoewijzing.|Geen effect op het maken van het artikel. <br>Voorkomt het maken van varianten. Het is handig wanneer in een verkooporder alleen het hoofdartikel wordt gebruikt. Een variant kan nog steeds handmatig worden toegewezen vanuit het venster **Shopify-product**.|
|**Artikelnr.**|Kies dit als het SKU het artikelnummer bevat.|Geen effect op het maken van artikel zonder varianten. Voor een artikel met varianten wordt elke variant als een apart artikel gemaakt.<br> Bijvoorbeeld als Shopify een product heeft met twee varianten en hun SKU's zijn '1000' en '2000', worden in het [!INCLUDE[prod_short](../includes/prod_short.md)]-systeem twee artikelen gemaakt met de nummers '1000' en '2000'.|
|**Variant**|Het veld SKU wordt niet gebruikt in de routine voor artikeltoewijzing.|Geen effect op het maken van het artikel. Wanneer een artikelvariant wordt gemaakt, wordt de waarde van het veld SKU gebruikt als een code. Als de SKU leeg is, wordt een code gegenereerd met behulp van het veld **Prefix voor variant**.|
|**Artikelnr. + variant**| Selecteer dit als het SKU-veld een artikelnummer bevat en de artikelvariantcode wordt gescheiden door de waarde die is gedefinieerd in het veld **SKU-veldscheidingsteken**.|Wanneer een artikel wordt gemaakt, wordt het eerste deel van de waarde van het SKU-veld gebruikt als **Nr.** Als de SKU leeg is, wordt een artikelnummer gegenereerd met behulp van nummerreeksen gedefinieerd in de **Artikelsjablooncode** of **Artikelnummers** van het venster **Voorraad**.<br>Wanneer een artikel wordt gemaakt, gebruikt de variantfunctie het tweede deel van de waarde van het SKU-veld als **Code**. Als de SKU leeg is, wordt een code gegenereerd met behulp van het veld **Prefix voor variant**.|
|**Artikelnr. van leverancier**| Kies of het veld SKU het artikelnummer van de leverancier bevat. In dit geval wordt het veld **Artikelnr. leverancier** niet gebruikt in het venster **Artikelkaart**, maar wordt **Artikelnr. leverancier** uit **Artikel-/leverancierscatalogus** gebruikt. Als de gevonden *Artikel-/leverancierscatalogus*-record een variantcode bevat, wordt deze variantcode gebruikt om de Shopify-variant toe te wijzen.|Als er een corresponderende leverancier bestaat in [!INCLUDE[prod_short](../includes/prod_short.md)], wordt de SKU-waarde gebruikt als **Artikelnr. leverancier** in de **Artikelkaart** en als **Artikelreferentie:** van het type Leverancier. <br>Voorkomt het maken van varianten. Dit is handig wanneer u het hoofdartikel alleen in de verkooporder wilt gebruiken. U kunt nog steeds handmatig een variant toewijzen vanuit het venster **Shopify-product**.|
|**Barcode**| Kies dit als het SKU-veld een barcode bevat. Er wordt gezocht onder **Artikelreferenties** van het type Leverancier. Als de gevonden artikelreferentierecord een variantcode bevat, wordt deze variantcode gebruikt om de Shopify-variant toe te wijzen.|Geen effect op het maken van het artikel. <br>Voorkomt het maken van varianten. Het is handig wanneer in de verkooporder alleen het hoofdartikel wordt gebruikt. Een variant kan nog steeds handmatig worden toegewezen vanuit het venster **Shopify-product**.|

De volgende tabel geeft een overzicht van het effect van het veld **Barcode**.

|Effect op toewijzing|Effect op maken|
|-----------------|------------------|
|Er wordt gezocht onder **Artikelreferenties** van het type barcode voor de waarde die is gedefinieerd in het veld Barcode in Shopify. Als de gevonden artikelreferentierecord een variantcode bevat, wordt deze variantcode gebruikt om de Shopify-variant toe te wijzen.|Barcode wordt opgeslagen als **Artikelreferentie** voor artikel en artikelvariant.|

> [!NOTE]  
> U kunt toewijzing activeren voor het geselecteerde product/de varianten of alle geïmporteerde niet-toegewezen producten door te kiezen voor **Producttoewijzing zoeken** (voor selectie) of **Toewijzingen zoeken** (voor alles).

## <a name="export-items-to-shopify"></a>Artikelen exporteren naar Shopify

Kies de elementen uit uw artikellijst die worden geëxporteerd naar Shopify. Gebruik de actie **Artikel toevoegen** uit het venster **Shopify-producten** om artikelen toe te voegen aan de lijst met Shopify-producten.

Met de volgende instellingen kunt u het proces van het exporteren van artikelen beheren:

|Veld|Omschrijving|
|------|-----------|
|**Klantenprijsgroep**|Bepaal de prijs voor een artikel in Shopify. De verkoopprijs van deze klantenprijsgroep wordt genomen. Als er geen groep is ingevoerd, wordt de prijs van de artikelkaart gebruikt.|
|**Klantenkortingsgroep**|Bepaal de korting die moet worden gebruikt voor het berekenen van de prijs van een artikel in Shopify. Gereduceerde prijzen worden opgeslagen in het veld **Prijs** en de volledige prijs wordt opgeslagen in het veld **Prijs vergelijken**.|
|**Uitgebreide tekst voor synchronisatieartikel**|Selecteer om de uitgebreide tekst van het artikel te synchroniseren. Zoals het zal worden toegevoegd aan *Beschrijving*, kan het HTML-code bevatten. |
|**Artikelkenmerken synchroniseren**|Selecteer dit om de artikelkenmerken te synchroniseren. Kenmerken worden opgemaakt als een tabel en opgenomen in het veld *Beschrijving* in Shopify.|
|**Taalcode**|Indien geselecteerd worden de vertaalde versies gebruikt voor titel, kenmerken en uitgebreide tekst.|
|**SKU-toewijzing**|Kies hoe u het SKU-veld wilt invullen in Shopify. Ondersteunde opties zijn:<br> - **Artikelnr.** om het artikelnummer te gebruiken voor zowel producten als varianten.<br> - **Artikelnr. + variant** om een SKU te maken door waarden van twee velden samen te voegen. Voor artikelen zonder varianten wordt alleen het artikelnr. gebruikt.<br>- **Artikelnr. leverancier** om het artikelleveranciersnummer te gebruiken dat is gedefinieerd in de *Artikelkaart* voor zowel producten als varianten.<br> - **Barcode** - gebruikt **Artikelreferentie** van het type barcode. Deze optie respecteert varianten. |
|**SKU-veldscheidingsteken**|Definieer een scheidingsteken voor de optie **Artikelnr. + variant**.|
|**Voorraad getraceerd**|Kies hoe het systeem het veld **Voorraad bijhouden** moet vullen voor producten die worden geëxporteerd naar Shopify. U kunt de beschikbaarheidsinformatie bijwerken vanuit [!INCLUDE[prod_short](../includes/prod_short.md)] voor producten in Shopify waarvan voorraad traceren is ingeschakeld. Zie [Voorraad](synchronize-items.md#sync-inventory-to-shopify) voor meer informatie.|
|**Standaardvoorraadbeleid**|Kies *Afwijzen* om negatieve voorraad van de Shopify-kant te voorkomen. |
|**Kan Shopify-producten bijwerken**|Definieer of [!INCLUDE[prod_short](../includes/prod_short.md)] alleen artikelen kan maken of ook artikelen kan bijwerken. Selecteer deze optie als u na de eerste synchronisatie, geactiveerd door de actie **Artikel toevoegen**, producten handmatig wilt bijwerken met de actie **Product synchroniseren** of via de taakwachtrij voor terugkerende updates. Vergeet niet **Naar Shopify** te selecteren in het veld **Artikel synchroniseren**.|

### <a name="fields-mapping-overview"></a>Overzicht van veldtoewijzing

|Shopify|Bron bij export vanuit [!INCLUDE[prod_short](../includes/prod_short.md)]|Doel bij import naar [!INCLUDE[prod_short](../includes/prod_short.md)]|
|------|-----------------|-----------------|
|Status|Volgens de **Status voor gemaakte producten** op de **Shopify-winkelkaart**. Zie voor meer informatie [Adhoc updates van Shopify-producten](synchronize-items.md#ad-hock-updates-of-shopify-products).|Niet gebruikt.|
|Title|**Beschrijving**. Als de taalcode is gedefinieerd en er een corresponderende artikelvertaling bestaat, wordt de artikelvertaling gebruikt in plaats van de beschrijving.|**Beschrijving**|
|Omschrijving|Combineert uitgebreide teksten en kenmerken als de corresponderende schakelaars op de Shopify-winkelkaart zijn ingeschakeld. Respecteert taalcode.|Niet gebruikt.|
|SEO-paginatitel|Waarde herstellen: leeg, zie [Adhoc updates van Shopify-producten](synchronize-items.md#ad-hock-updates-of-shopify-products). |Niet gebruikt.|
|SEO-metabeschrijving|Waarde herstellen: leeg, zie [Adhoc updates van Shopify-producten](synchronize-items.md#ad-hock-updates-of-shopify-products). |Niet gebruikt.|
|Media|**Afbeelding**, zie voor meer informatie [Artikelafbeeldingen synchroniseren](synchronize-items.md#sync-item-images)|**Afbeelding**|
|Prijs|De eindklantprijs wordt berekend op basis van artikelprijsgroep, artikelkortingsgroep, valutacode en klantsjablooncode. |Niet gebruikt.|
|Prijs vergelijken|Prijs zonder korting wordt berekend op basis van artikelprijsgroep, artikelkortingsgroep, valutacode en klantsjablooncode. |Niet gebruikt.|
|Kosten per artikel|**Kostprijs**|**Kostprijs**|
|SKU|Zie **SKU-toewijzing** in [Exporteren naar Shopify](synchronize-items.md#export-items-to-shopify)| Zie [Hoe SKU en barcode, gedefinieerd in een Shopify-product, van invloed zijn op het toewijzen en maken van artikelen en varianten](synchronize-items.md#how-sku-and-barcode-defined-in-shopify-product-impact-mapping-and-creation-of-items-and-variants-in-business-central)|
|Barcode|**Artikelreferenties** van het type barcode|**Artikelreferenties** van het type barcode|
|Te traceren aantal|Volgens **Voorraad getraceerd** op de **Shopify-winkelkaart**. Zie [Voorraad](synchronize-items.md#sync-inventory-to-shopify) voor meer informatie.|Niet gebruikt.|
|Doorgaan met verkopen wanneer niet op voorraad|Volgens het **Standaardvoorraadbeleid** op de **Shopify-winkelkaart**. Niet geïmporteerd.|Niet gebruikt.|
|Type|**Beschrijving** van **Artikelcategoriecode**. Als het type niet is opgegeven in Shopify, wordt het toegevoegd als een aangepast type.|**Artikelcategoriecode**. Toewijzing op beschrijving.|
|Leverancier|**Naam** van leverancier uit **Leveranciersnr.** |**Leveranciersnr.** Toewijzing op naam.|
|Gewicht|**Brutogewicht**.|Niet gebruikt.|
|Belastbaar|Vaste waarde: Ingeschakeld.|Niet gebruikt.|
|Belastingcodes|**Belastinggroepcode**. Alleen relevant voor omzetbelasting. Zie [belasting](synchronize-orders.md#tax-remarks) voor meer informatie. |Niet gebruikt.|

### <a name="tags"></a>Labels

Geïmporteerde labels kunnen worden bekeken in het feitenblok **Labels** in het **Shopify-product**. Om tags te bewerken kiest u de actie **Labels** op de pagina **Shopify-product**.
Als de optie **Naar Shopify** is geselecteerd in het veld **Artikel synchroniseren**, worden toegewezen labels geëxporteerd naar Shopify bij de volgende synchronisatie.

## <a name="run-item-synchronization"></a>Artikelsynchronisatie uitvoeren

Volledige of gedeeltelijke synchronisatie van artikelen kan op veel verschillende manieren worden uitgevoerd.

### <a name="initial-sync-of-items-from-business-central-to-shopify"></a>Initiële synchronisatie van artikelen van Business Central naar Shopify

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-producten** in en kies de gerelateerde koppeling.
2. Kies de actie **Artikelen toevoegen**.
3. Voer in het veld **Winkelcode** de code in. Als u het venster **Shopify-product** opent vanuit het venster **Winkelkaart**, wordt de winkelcode automatisch ingevuld.
4. Definieer desgewenst filters voor artikelen. U kunt bijvoorbeeld filteren op artikelnummer of artikelcategoriecode.
5. Klik op **OK**.

De resulterende artikelen worden automatisch gemaakt in Shopify met prijzen, maar afbeeldingen en voorraadniveaus zijn niet inbegrepen. De bewerking kan enige tijd duren als er een groot aantal artikelen wordt toegevoegd.

### <a name="sync-products-from-shopify-to-business-central"></a>Producten synchroniseren vanuit Shopify naar Business Central

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-winkel** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u artikelen wilt synchroniseren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Producten synchroniseren**.

Of gebruik de actie **Producten synchroniseren** in het venster **Shopify-producten** of zoek naar de batchverwerking **Producten synchroniseren**.

### <a name="ad-hock-updates-of-shopify-products"></a>Adhoc updates van Shopify-producten

Wanneer de records worden bijgewerkt in de tabel **Shopify-product**, worden de volgende wijzigingen gesynchroniseerd met Shopify.

Bijwerken:

* **Status** - u kunt kiezen tussen actief, gearchiveerd of concept.
* **SEO-titel**
* **SEO-beschrijving**

Verwijdering:

Op basis van de waarde in **Actie voor verwijderde producten** in **Shopify-winkelkaart** worden de producten bijgewerkt in Shopify wanneer een record wordt verwijderd vanaf de pagina **Shopify-producten**.

* **Leeg** - er gebeurt niets. Indien nodig moet de gebruiker de vereiste actie uitvoeren vanuit Shopify-beheer.
* **Status naar Concept** - status van product in Shopify wordt ingesteld op *Concept*.
* **Status naar Gearchiveerd** - product wordt gearchiveerd in Shopify.

## <a name="sync-item-images"></a>Artikelafbeeldingen synchroniseren

Synchronisatie van afbeeldingen kan worden geconfigureerd voor gesynchroniseerde artikelen. U kunt kiezen uit de volgende opties:

* **Leeg** - afbeeldingssynchronisatie is gedeactiveerd.
* **Naar Shopify** - afbeeldingen van artikelen worden geëxporteerd naar Shopify
* **Van Shopify** - afbeeldingen vanuit Shopify worden geïmporteerd naar [!INCLUDE[prod_short](../includes/prod_short.md)]

Afbeeldingssynchronisatie kan op twee manieren worden geïnitialiseerd.

### <a name="sync-product-images-from-the-shopify-shop-window"></a>Productafbeeldingen synchroniseren vanuit het venster Shopify-winkel

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u afbeeldingen wilt synchroniseren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Productafbeeldingen synchroniseren**.

### <a name="sync-product-images-from-the-shopify-products-window"></a>Productafbeeldingen synchroniseren vanuit het venster Shopify-producten

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-producten** in en kies de gerelateerde koppeling.
2. Kies de actie **Productafbeeldingen synchroniseren**.

### <a name="image-synchronization-remarks"></a>Opmerkingen over afbeeldingssynchronisatie

* Bij het exporteren van afbeeldingen vanuit [!INCLUDE[prod_short](../includes/prod_short.md)] naar Shopify, worden de nieuwe afbeeldingen toegevoegd aan Shopify, waarbij oude afbeeldingen intact blijven. Als een afbeelding wordt bijgewerkt in [!INCLUDE[prod_short](../includes/prod_short.md)], moet u oude afbeeldingen verwijderen uit Shopify-beheer.
* Afbeeldingen die worden geëxporteerd naar Shopify en niet voldoen aan de vereisten zoals gedefinieerd door Shopify, worden niet geïmporteerd. Zie voor meer informatie [Typen productmedia op help.shopify.com](https://help.shopify.com/en/manual/products/product-media/product-media-types#images)

## <a name="sync-prices-with-shopify"></a>Prijzen synchroniseren met Shopify

Prijzen kunnen worden geëxporteerd voor gesynchroniseerde artikelen op de hieronder beschreven manieren.

### <a name="sync-prices-from-the-shopify-products-window"></a>Prijzen synchroniseren vanuit het venster Shopify-producten

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-producten** in en kies de gerelateerde koppeling.
2. Kies de actie **Prijzen synchroniseren met Shopify**.

### <a name="price-calculation-remarks"></a>Opmerkingen over prijsberekening

* Voor prijsberekening is het belangrijk om een waarde in het veld **Standaardklantensjabloon** te hebben.
* Vergeet niet om een **Valutacode** in te voeren als uw online winkel een andere valuta gebruikt dan LV.
* Bij het bepalen van een prijs gebruikt [!INCLUDE[prod_short](../includes/prod_short.md)] de 'Laagste prijs'-logica. Dit betekent dat als de eenheidsprijs die is gedefinieerd op de artikelkaart, lager is dan wat is gedefinieerd in de prijsgroep, de eenheidsprijs van de artikelkaart wordt gebruikt.

## <a name="sync-inventory-to-shopify"></a>Voorraad synchroniseren met Shopify

Voorraad synchronisatie kan worden geconfigureerd voor reeds gesynchroniseerde artikelen. Er zijn twee voorwaarden waaraan moet worden voldaan:

1. Voorraad bijhouden moet zijn ingeschakeld voor een product in Shopify. Als artikelen worden geëxporteerd naar Shopify, overweeg dan **Voorraad getraceerd** in te schakelen op de **Shopify-winkel** kaart. Zie voor meer informatie [Artikelen exporteren naar Shopify](synchronize-items.md#export-items-to-shopify).
2. Voorraadsynchronisatie moet zijn ingeschakeld voor **Shopify-vestigingen**.

### <a name="to-enable-inventory-sync"></a>Voorraadsynchronisatie inschakelen

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-winkel** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u voorraad wilt synchroniseren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Vestigingen** om **Shopify-winkellocaties** te openen.
4. Kies de actie **Shopify-vestigingen ophalen** om alle locaties te importeren die zijn gedefinieerd in Shopify. U vindt ze in de [**Vestigingen**](https://www.shopify.com/admin/settings/locations)-instellingen in uw **Shopify beheer**.
5. Voeg in het veld **Locatiefilter** locaties toe als u alleen voorraad van specifieke locaties wilt opnemen. U kunt bijvoorbeeld *OOST|WEST* invoeren, zodat alleen voorraad van deze twee vestigingen beschikbaar is voor verkoop via de online winkel.
6. Deselecteer de schakelaar **Uitgeschakeld** om voorraadsynchronisatie in te schakelen voor geselecteerde Shopify-vestigingen.

U kunt voorraadsynchronisatie op twee manieren initialiseren.

### <a name="sync-inventory-from-the-shopify-shop-window"></a>Voorraad synchroniseren vanuit het venster Shopify-winkel

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u voorraad wilt synchroniseren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Voorraad synchroniseren**.

### <a name="sync-inventory-from-the-shopify-products-window"></a>Voorraad synchroniseren vanuit het venster Shopify-producten

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-producten** in en kies de gerelateerde koppeling.
2. Kies de actie **Voorraad synchroniseren**.

### <a name="inventory-remarks"></a>Opmerkingen over voorraad

* De connector berekent de **Voorspelde beschikbare voorraad** en exporteer deze naar Shopify.
* U kunt de voorraadinformatie inspecteren die u hebt ontvangen van Shopify op de pagina **Feitenblok Shopify-voorraad**. In dit feitenblok krijgt u een overzicht van de Shopify-voorraad en de laatst berekende voorraad in [!INCLUDE[prod_short](../includes/prod_short.md)]. Er is een record per vestiging.
* Als de voorraadinformatie in Shopify verschilt van **Voorspelde beschikbare voorraad** in [!INCLUDE[prod_short](../includes/prod_short.md)], wordt voorraad bijgewerkt in Shopify.

## <a name="see-also"></a>Zie ook

[Aan de slag met de connector voor Shopify](get-started.md)  
