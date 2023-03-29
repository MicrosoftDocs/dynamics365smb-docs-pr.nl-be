---
title: Belastingen instellen voor Shopify-verbinding
description: Hoe u belastingen instelt in Shopify en Business Central.
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
author: AndreiPanko
ms.author: andreipa
---

# Belastingen instellen voor de Shopify-verbinding

In dit artikel zullen we onderzoeken hoe verschillende instellingen in Shopify invloed hebben op de winkelprijzen en belastingen die aan de klant worden getoond. We zullen ook kijken naar hoe [!INCLUDE[prod_short](../includes/prod_short.md)] te configureren om de instellingen in Shopify te ondersteunen. Dit artikel is niet bedoeld als een uitgebreide belastinggids. Neem voor meer informatie contact op met uw lokale belastingdienst of een belastingadviseur.  

In het artikel wordt ervan uitgegaan dat u belasting moet betalen als u goederen lokaal of internationaal verkoopt.

## Als u in het binnenland verkoopt

Nadat u uw Shopify hebt geconfigureerd om belastingen te innen in uw eigen land/regio, kunt u beslissen hoe u de prijzen in uw winkel wilt weergeven.
U regelt dit door het in- of uitschakelen van de schakelaar **Alle prijzen zijn inclusief btw** in de [**Belastingen en verplichtingen**](https://www.shopify.com/admin/settings/taxes)-instellingen in uw **Shopify-beheer**.

Het is gebruikelijk dat deze schakelaar is ingeschakeld voor landen/regio's als Australië, Oostenrijk, België, Tsjechië, Denemarken, Finland, Frankrijk, Duitsland, IJsland, Italië, Nederland, Nieuw-Zeeland, Noorwegen, Spanje, Zweden, Zwitserland en het Verenigd Koninkrijk. In markten zoals deze bevat de prijs *100 EUR* die is gedefinieerd op de productkaart, al btw en wordt diezelfde prijs aan de klant getoond in de winkel en bij het afrekenen.  

In de VS en Canada verwachten klanten productprijzen zonder belastingen te zien, die bij het afrekenen worden toegevoegd. Dus het veld **Alle prijzen zijn inclusief btw** is meestal niet geselecteerd. In dit geval is de prijs *$100*, die is gedefinieerd op de productkaart, de prijs zonder belasting. In het afrekenstadium worden belastingen bovenop de prijs toegevoegd om het afrekentotaal te berekenen.

Ter ondersteuning van het scenario waarin **Alle prijzen zijn inclusief btw** is geselecteerd aan de [!INCLUDE[prod_short](../includes/prod_short.md)]-zijde, vult u het veld **Klantensjablooncode** op de pagina **Shopify-winkelkaart** in om toegang te krijgen tot de sjabloon met de volgende velden gedefinieerd:  

1. **Algemene bedrijfsboekingsgroep**, gebruikt voor binnenlandse klanten.  
2. **Btw-bedrijfsboekingsgroep**, gebruikt voor binnenlandse klanten.  
3. **Prijzen inclusief btw** ingesteld op *ja*.  

Definieer nu artikelprijzen op de **Artikelkaart** of in de **Verkoopprijslijst**, met of zonder belasting. Bij het exporteren van prijzen naar Shopify berekent het systeem de prijs inclusief binnenlandse belastingen en toont die prijs vervolgens op de productkaart in Shopify.

> [!NOTE]
> Als u de Shopify-connector hebt geconfigureerd om automatisch klanten te maken, hebt u mogelijk meer velden in uw sjabloon nodig, zoals **Klantboekingsgroep**. Als u de standaardklant gebruikt voor geïmporteerde bestellingen, zorg er dan voor dat de klant dezelfde velden heeft ingevuld. U moet nog steeds de **Klantensjablooncode** invullen zoals hierboven opgegeven, omdat het veld **Prijzen inclusief sales tax**/**Prijzen inclusief btw** in het gemaakte verkoopdocument niet afhankelijk is van de klant, maar van de **Klantensjabloon** op de Shopify-winkelkaart of de klantensjabloon per land/regio.

## Als u internationaal verkoopt

In dit gedeelte bekijken we instellingen voor scenario's waarin u belasting moet innen bij verkoop aan een ander land/regio, zoals andere landen/regio's in de EU.

Momenteel ondersteunt de **Shopify-connector** export van slechts één prijs. Shopify past automatisch lokale belastingen, valuta's en afronding toe. De schakelaar **Alle prijzen zijn inclusief btw** resulteert tot de beschreven acties in de volgende subsecties.

### *Alle prijzen zijn inclusief btw* is geselecteerd

|-|Binnenlandse verkoop|Buitenland waar u belasting int|Buitenland waar u geen belasting int|
|------------------------|--------|--------|--------|
|Prijs weergegeven in de winkel|1200|1200|1200|
|Belastingpercentage|20|25|0|
|Prijs bij afrekenen|1200|1200|1200|

De prijs voor klanten blijft intact, ongeacht hun locatie, maar uw marge wordt beïnvloed door belastingtarieven die per land/regio verschillen.

### *Alle prijzen zijn inclusief btw* is niet geselecteerd

|-|Binnenlandse verkoop|Buitenland waar u belasting int|Buitenland waar u geen belasting int|
|------------------------|--------|--------|--------|
|Prijs weergegeven in de winkel|1000|1000|1000|
|Belastingpercentage|20|25|0|
|Prijs bij afrekenen|1200|1250|1000|

Shopify voegt lokale belastingen toe boven op de prijs die is gedefinieerd op de productkaart op basis van waarnaar goederen worden verzonden.

## Dynamische prijzen inclusief btw

Omdat verschillende landen/regio's verschillende vereisten hebben, afhankelijk van of u belasting in de weergegeven prijs opneemt of niet, kunt u [dynamische prijzen inclusief btw](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing) inschakelen in Shopify. Dit automatiseert de functie voor het opnemen van belastingen.

Selecteer **Inclusief of exclusief belasting op basis van het land/regio van uw klant** in het gedeelte **Andere markten - Voorkeuren** van de [**Markten**](https://www.shopify.com/admin/settings/markets)-instellingen in uw **Shopify-beheer**.  

> [!NOTE]
> Deze instelling heeft geen invloed op de weergave van prijzen op binnenlandse markten, die wordt beheerd door de schakelaar **Alle prijzen zijn inclusief btw**.

### *Alle prijzen zijn inclusief btw* is geselecteerd

|-|Binnenlandse verkoop|Buitenland waar belasting bij de prijs is inbegrepen|Buitenland waar belasting niet bij de prijs is inbegrepen|
|------------------------|--------|--------|--------|
|Prijs weergegeven in de winkel|1200|1250|1000|
|Belastingpercentage|20|25|10|
|Prijs bij afrekenen|1200|1250|1100|

De prijs voor elke klant verandert afhankelijk van hun locatie.

### *Alle prijzen zijn inclusief btw* is niet geselecteerd

|-|Binnenlandse verkoop|Buitenland waar belasting bij de prijs is inbegrepen|Buitenland waar belasting niet bij de prijs is inbegrepen|
|------------------------|--------|--------|--------|
|Prijs weergegeven in de winkel|1000|1250|1000|
|Belastingpercentage|20|25|10|
|Prijs bij afrekenen|1200|1250|1100|

> [!NOTE]
> De schakelaar **Alle prijzen zijn inclusief btw** verandert niet hoe prijzen worden weergegeven aan internationale klanten.

## Als u aan klanten in de EU verkoopt

Verschillende EU-landen/regio's hebben verschillende lokale belastingtarieven. Als u zich echter in de EU bevindt en aan andere EU-landen/regio's verkoopt, kunt u in sommige gevallen uw lokale belastingtarief gebruiken.  

Schakel het vak **Btw innen** in het gedeelte **Europese Unie** van de [**Belastingen en verplichtingen**](https://www.shopify.com/admin/settings/taxes)-instellingen in uw **Shopify-beheer** in.

|Btw innen|Btw-tarief|
|-|-|
|Vrijstelling voor micro-ondernemingen|Gebruik uw binnenlandse belastingtarief voor alle verkopen binnen de EU|
|One-stop-shop of land/regio-specifieke registratie|Het btw-tarief van het land/regio van uw klant gebruiken|


### Btw innen ingesteld op one-stop-shop registratie

In het volgende voorbeeld is de schakelaar **Alle prijzen zijn inclusief btw** ingeschakeld. De prijs op de productkaart is ingesteld op *1200*.
        
|-|Binnenlandse verkoop|Buitenland|
|------------------------|--------|--------|
|Prijs weergegeven in de winkel|1200|1250|
|Belastingpercentage|20|25|
|Prijs bij afrekenen|1200|1250|       
        
### Btw innen ingesteld op vrijstelling voor micro-ondernemingen

In het volgende voorbeeld is de schakelaar **Alle prijzen zijn inclusief btw** ingeschakeld. De prijs op de productkaart is ingesteld op *1200*.
        
|-|Binnenlandse verkoop|Buitenland met lokaal belastingtarief van 25 procent.|
|------------------------|--------|--------|
|Prijs weergegeven in de winkel|1200|1200|
|Belastingpercentage|20|20|
|Prijs bij afrekenen|1200|1200|           
    
Shopify negeert het belastingtarief in een buitenland wanneer uiteindelijke prijzen worden berekend en gebruikt het binnenlandse btw-tarief.

## Shopify-orders importeren die aan internationale klanten zijn verkocht

Als u belastingen int uit meerdere landen/regio's, moet u hoogstwaarschijnlijk een land/regio-specifieke instelling definiëren in [!INCLUDE[prod_short](../includes/prod_short.md)]. Dit is vereist omdat wanneer een verkoopdocument wordt gemaakt in [!INCLUDE[prod_short](../includes/prod_short.md)], berekent het systeem belastingen in plaats ze uit Shopify te importeren.

Land-/regiospecifieke instellingen worden gekozen in het venster **Shopify-klantensjabloon**. Daar kunt u het **Standaardklantnr.** of het **Klantensjablooncodenr.** definiëren. Zorg er in beide gevallen voor dat de geselecteerde klant of sjabloon de volgende velden heeft gedefinieerd:

1. **Algemene bedrijfsboekingsgroep** (gebruikt voor buitenlandse klanten).
2. **Btw-bedrijfsboekingsgroep** (gebruikt voor buitenlandse klanten).
3. **Prijzen inclusief btw** (afgestemd op de instelling aan de Shopify-zijde):
* Kiezen *Ja* als **Alle prijzen zijn inclusief btw** is ingeschakeld en **Inclusief of exclusief belasting op basis van het land/regio van uw klant** is uitgeschakeld.
* Kies *Nee* als **Alle prijzen zijn inclusief btw** is uitgeschakeld en **Inclusief of exclusief belasting op basis van het land/regio van uw klant** is uitgeschakeld.
* Kies *Ja* als **Inclusief of exclusief belasting op basis van het land/regio van uw klant** is ingeschakeld en land/regio wordt vermeld in de [Belastinginclusieve landen/regio's](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).
* Kies *Nee* als **Inclusief of exclusief belasting op basis van het land/regio van uw klant** is ingeschakeld en land/regio niet wordt vermeld in de [Belastinginclusieve landen/regio's](https://help.shopify.com/en/manual/markets/pricing/dynamic-tax-inclusive-pricing#tax-inclusive-versus-tax-exclusive-countries-and-regions).

[!Note]
> De instelling van het veld **Prijzen inclusief btw** komt van de sjabloon, niet van de specifieke klant. Daarom is het belangrijk om de klantsjabloon te hebben gedefinieerd.

## Andere fiscale opmerkingen

Terwijl de geïmporteerde Shopify-order informatie over belastingen bevat, worden de belastingen opnieuw berekend wanneer u het verkoopdocument maakt. Vanwege de herberekening is het belangrijk dat de btw/belasting-instellingen correct zijn in [!INCLUDE[prod_short](../includes/prod_short.md)].

- Meerdere productbelasting/btw-tarieven. Sommige productcategorieën zijn bijvoorbeeld onderworpen aan verlaagde belastingtarieven. U kunt de functie [belasting overschrijven](https://help.shopify.com/en/manual/taxes/tax-overrides#create-a-manual-collection-for-products-that-need-a-tax-override) in Shopify gebruiken. Wanneer artikelen worden geïmporteerd en gemaakt in [!INCLUDE[prod_short](../includes/prod_short.md)], gebruiken ze de belastinginstellingen zoals ingevuld op de artikelsjablooncode in de Shopify winkel. Voordat u orders met dergelijke artikelen importeert, moet u de btw-productboekingsgroep bijwerken.  

- Adresafhankelijke belastingtarieven. Gebruik het veld **Prioriteit van belastinggebied** samen met de tabel **Klantensjablonen** om standaardlogica te overschrijven die de **Code van belastinggebied** invult in het verkoopdocument. Het veld **Prioriteit van belastinggebied** specificeert de prioriteit met betrekking tot waar de functie de informatie over land/regio en staat/provincie vandaan moet halen. Dan wordt de bijbehorende record in de Shopify-klantsjablonen gevonden en worden **Code van belastinggebied**, **Belastingplichtig** en **Btw-bedrijfsboekingsgroep** gebruikt wanneer een verkoopdocument wordt gemaakt.  

## Zie ook

[Aan de slag met de connector voor Shopify](get-started.md)  
