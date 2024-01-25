---
title: Belastingen instellen voor Shopify-verbinding
description: Hoe u belastingen instelt in Shopify en Business Central.
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
---

# <a name="set-up-taxes-for-the-shopify-connection"></a>Belastingen instellen voor de Shopify-verbinding

In dit artikel zullen we onderzoeken hoe verschillende instellingen in Shopify invloed hebben op de winkelprijzen en belastingen die aan klanten worden getoond. We zullen ook kijken naar hoe [!INCLUDE[prod_short](../includes/prod_short.md)] te configureren om de instellingen in Shopify te ondersteunen. Dit artikel is niet bedoeld als een uitgebreide belastinggids. Neem voor meer informatie contact op met uw lokale belastingdienst of een belastingadviseur.  

In het artikel wordt ervan uitgegaan dat u belasting moet betalen als u goederen lokaal of internationaal verkoopt.

## <a name="if-you-sell-domestically"></a>Als u in het binnenland verkoopt

Nadat u uw Shopify hebt geconfigureerd om belastingen te innen in uw eigen land/regio, kunt u beslissen hoe u de prijzen in uw winkel wilt weergeven.

U geeft op of belasting in prijzen wordt opgenomen door de schakelaar **Alle prijzen zijn inclusief btw** aan of uit te zetten in de [**Belastingen en verplichtingen**](https://www.shopify.com/admin/settings/taxes)-instellingen in uw **Shopify-beheer**.

De schakelaar is meestal geactiveerd voor de volgende landen/regio's:

* Australië
* Oostenrijk
* België
* Tsjechië
* Denemarken
* Finland
* Frankrijk
* Duitsland
* IJsland
* Italië
* Nederland
* Nieuw-Zeeland
* Noorwegen
* Spanje
* Zweden
* Zwitserland
* Verenigd Koninkrijk. 

In dergelijke markten bevat een op de productkaart gedefinieerde prijs van 100 EUR al btw. De prijs, inclusief btw, wordt aan de klant weergegeven in de winkel en bij het afrekenen.  

In de VS en Canada verwachten klanten niet dat prijzen inclusief btw zijn. Btw wordt toegevoegd bij het afrekenen, dus de schakelaar **Alle prijzen zijn inclusief btw** is meestal uitgeschakeld. In dit geval is de prijs $100, die is gedefinieerd op de productkaart, de prijs zonder belasting. Bij het afrekenen worden belastingen toegevoegd aan de prijs.

Ter ondersteuning van het scenario waarbij **Alle prijzen zijn inclusief btw** is geselecteerd, vult u in [!INCLUDE[prod_short](../includes/prod_short.md)] de volgende velden op de pagina **Shopify - Winkelkaart** in:  

1. Zet de schakelaar **Prijzen zijn inclusief btw** aan.  
2. Geef in het veld **Btw-bedrijfsboekingsgroep** de boekingsgroep op die u voor binnenlandse klanten gebruikt.  

Definieer nu artikelprijzen op de **Artikelkaart** of in de **Verkoopprijslijst**-velden, met of zonder belasting. Bij het exporteren van prijzen naar Shopify berekent [!INCLUDE [prod_short](../includes/prod_short.md)] de berekende prijs inclusief binnenlandse belastingen en toont die prijs vervolgens voor het product in Shopify.

[!Note]
> Deze instellingen zijn van invloed op de export van prijzen. Wanneer u orders importeert uit Shopify, komt de instelling voor het veld **Prijzen zijn inclusief btw** uit de **Klantensjabloon** op de Shopify-winkelkaart, of de klantensjabloon per land/regio. Ook als u de standaardklant gebruikt voor geïmporteerde bestellingen, moet u de **Klantensjablooncode** invullen.

## <a name="if-you-sell-internationally"></a>Als u internationaal verkoopt

In dit gedeelte bekijken we instellingen voor scenario's waarin u belasting moet innen bij verkoop aan een ander land/regio, zoals andere landen/regio's in de EU.

Momenteel ondersteunt de Shopify-connector alleen export van één prijs. Shopify past automatisch lokale belastingen, valuta's en afronding toe. De schakelaar **Alle prijzen zijn inclusief btw** resulteert tot de beschreven acties in de volgende subsecties.

### <a name="all-prices-include-tax-is-selected"></a>Alle prijzen zijn inclusief btw is geselecteerd

|-|Binnenlandse verkoop|Buitenland/regio waar u belasting int|Buitenland/regio waar u geen belasting int|
|------------------------|--------|--------|--------|
|Prijs weergegeven in de winkel|1200|1200|1200|
|Belastingpercentage|20|25|0|
|Prijs bij afrekenen|1200|1200|1200|

De prijs voor de klant blijft intact, ongeacht hun locatie, maar uw marge wordt beïnvloed door belastingtarieven die per land/regio verschillen.

### <a name="all-prices-include-tax-is-not-selected"></a>Alle prijzen zijn inclusief btw is niet geselecteerd

|-|Binnenlandse verkoop|Buitenland waar u belasting int|Buitenland waar u geen belasting int|
|------------------------|--------|--------|--------|
|Prijs weergegeven in de winkel|1000|1000|1000|
|Belastingpercentage|20|25|0|
|Prijs bij afrekenen|1200|1250|1000|

Shopify voegt lokale belastingen toe aan de prijs die is gedefinieerd op de productkaart op basis van waar goederen naar worden verzonden.

## <a name="dynamic-tax-inclusive-pricing"></a>Dynamische prijzen inclusief btw

Landen/regio's hebben verschillende vereisten voor het opnemen van belasting in prijzen. Als u wilt dat prijzen automatisch inclusief btw zijn, kunt u [Dynamische prijzen inclusief btw](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing) in Shopify inschakelen.

Selecteer in uw **Shopify-beheer** **Inclusief of exclusief belasting op basis van het land/regio van uw klant** in het gedeelte **Andere markten - Voorkeuren** van de [**Markten**](https://www.shopify.com/admin/settings/markets)-instellingen.  

> [!NOTE]
> Deze instelling heeft geen invloed op de prijzen op binnenlandse markten, die wordt beheerd door de schakelaar **Alle prijzen zijn inclusief btw**.

### <a name="all-prices-include-tax-is-selected-1"></a>Alle prijzen zijn inclusief btw is geselecteerd

|-|Binnenlandse verkoop|Buitenland/regio waar belasting bij de prijs is inbegrepen|Buitenland/regio waar belasting niet bij de prijs is inbegrepen|
|------------------------|---------------|---------------|--------|
|Prijs weergegeven in de winkel|1200|1250|1000|
|Belastingpercentage|20|25|10|
|Prijs bij afrekenen|1200|1250|1100|

De prijs voor elke klant verandert afhankelijk van hun locatie.

### <a name="all-prices-include-tax-is-not-selected-1"></a>Alle prijzen zijn inclusief btw is niet geselecteerd

|-|Binnenlandse verkoop|Buitenland/regio waar belasting bij de prijs is inbegrepen|Buitenland/regio waar belasting niet is inbegrepen|
|------------------------|--------|--------|--------|
|Prijs weergegeven in de winkel|1000|1250|1000|
|Belastingpercentage|20|25|10|
|Prijs bij afrekenen|1200|1250|1100|

> [!NOTE]
> De schakelaar **Alle prijzen zijn inclusief btw** verandert niet hoe prijzen worden weergegeven aan internationale klanten.

## <a name="if-you-sell-to-eu-customers"></a>Als u aan klanten in de EU verkoopt

Verschillende EU-landen/regio's hebben verschillende lokale belastingtarieven. Als u zich echter in de EU bevindt en aan andere EU-landen/regio's verkoopt, kunt u in sommige gevallen uw lokale belastingtarief gebruiken.  

Schakel in uw **Shopify-beheer** het vak **Btw innen** in het gedeelte **Europese Unie** van de [**Belastingen en verplichtingen**](https://www.shopify.com/admin/settings/taxes)-instellingen in.

|Btw innen|Btw-tarief|
|-|-|
|Vrijstelling voor micro-ondernemingen|Gebruik uw binnenlandse belastingtarief voor alle verkopen binnen de EU|
|One-stop-shop of land/regio-specifieke registratie|Het btw-tarief van het land/regio van uw klant gebruiken|

### <a name="collect-vat-set-to-one-stop-shop-registration"></a>Btw innen ingesteld op one-stop-shop registratie

In het volgende voorbeeld is de schakelaar **Alle prijzen zijn inclusief btw** ingeschakeld. De prijs op de productkaart is ingesteld op *1200*.

|-|Binnenlandse verkoop|Buitenland/regio|
|------------------------|--------|--------|
|Prijs weergegeven in de winkel|1200|1250|
|Belastingpercentage|20|25|
|Prijs bij afrekenen|1200|1250|

### <a name="collect-vat-set-to-micro-business-exemption"></a>Btw innen ingesteld op vrijstelling voor micro-ondernemingen

In het volgende voorbeeld is de schakelaar **Alle prijzen zijn inclusief btw** ingeschakeld. De prijs op de productkaart is ingesteld op *1200*.

|-|Binnenlandse verkoop|Buitenland/regio met lokaal belastingtarief van 25 procent.|
|------------------------|--------|--------|
|Prijs weergegeven in de winkel|1200|1200|
|Belastingpercentage|20|20|
|Prijs bij afrekenen|1200|1200|

Shopify gebruikt het binnenlandse belastingtarief en negeert het belastingtarief in het buitenland/regio wanneer uiteindelijke prijzen worden berekend.

## <a name="importing-shopify-orders-sold-to-international-customers"></a>Shopify-orders importeren die aan internationale klanten zijn verkocht

Als u belastingen int uit meerdere landen/regio's, moet u een land/regio-specifieke instelling definiëren in [!INCLUDE[prod_short](../includes/prod_short.md)]. Er is een reden waarom deze instelling vereist is. Wanneer een verkoopdocument wordt gemaakt in [!INCLUDE[prod_short](../includes/prod_short.md)], berekent [!INCLUDE [prod_short](../includes/prod_short.md)] belastingen in plaats van de belastingen opnieuw te gebruiken die zijn geïmporteerd uit Shopify.

U geeft land/regio-specifieke instellingen op de pagina **Shopify-klantensjabloon** op. U kunt het **Standaardklantnr.** of het **Klantensjablooncodenr.** definiëren. Zorg er in beide gevallen voor dat de geselecteerde klant of sjabloon de volgende velden heeft ingevuld:

1. **Algemene bedrijfsboekingsgroep** (gebruikt voor buitenlandse klanten).
2. **Btw-bedrijfsboekingsgroep** (gebruikt voor buitenlandse klanten).
3. **Prijzen inclusief btw** (afgestemd op de instelling aan de Shopify-zijde):

* Kiezen **Ja** als **Alle prijzen zijn inclusief btw** is ingeschakeld en **Inclusief of exclusief belasting op basis van het land/regio van uw klant** is uitgeschakeld.
* Kies **Nee** als **Alle prijzen zijn inclusief btw** is uitgeschakeld en **Inclusief of exclusief belasting op basis van het land/regio van uw klant** is uitgeschakeld.
* Kies **Ja** als **Inclusief of exclusief belasting op basis van het land/regio van uw klant** is geactiveerd en land/regio wordt vermeld in de [Belastinginclusieve landen/regio's](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
* Kies **Nee** als **Inclusief of exclusief belasting op basis van het land/regio van uw klant** is geactiveerd en land/regio niet wordt vermeld in de [Belastinginclusieve landen/regio's](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).

> [!NOTE]
> De instelling van het veld **Prijzen inclusief btw** komt van de sjabloon, niet van de specifieke klant. Het is belangrijk om de klantsjabloon te definiëren.

## <a name="other-tax-remarks"></a>Andere fiscale opmerkingen

Terwijl de geïmporteerde Shopify-order informatie over belastingen bevat, worden de belastingen opnieuw berekend wanneer u het verkoopdocument maakt. Vanwege de herberekening is het belangrijk dat de btw/belasting-instellingen correct zijn in [!INCLUDE[prod_short](../includes/prod_short.md)].

* Meerdere productbelasting/btw-tarieven. Sommige productcategorieën zijn bijvoorbeeld onderworpen aan verlaagde belastingtarieven. U kunt de functie [belasting overschrijven](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override) in Shopify gebruiken. Wanneer u artikelen importeert en maakt in [!INCLUDE[prod_short](../includes/prod_short.md)], gebruiken ze de belastinginstellingen zoals opgegeven op de artikelsjablooncode in de Shopify winkel. Voordat u orders met dergelijke artikelen importeert, werkt u de btw-productboekingsgroep bij.  
* Adresafhankelijke belastingtarieven. Gebruik het veld **Prioriteit van belastinggebied** samen met de tabel **Klantensjablonen** om standaardlogica te overschrijven die de **Code van belastinggebied** invult in het verkoopdocument. Het veld **Prioriteit van belastinggebied** specificeert de prioriteit met betrekking tot waar de functie de informatie over land/regio en staat/provincie vandaan moet halen. Dan wordt de bijbehorende record in de Shopify-klantsjablonen gevonden en worden **Code van belastinggebied**, **Belastingplichtig** en **Btw-bedrijfsboekingsgroep** gebruikt wanneer een verkoopdocument wordt gemaakt.  

## <a name="see-also"></a>Zie ook

[Aan de slag met de connector voor Shopify](get-started.md)  
