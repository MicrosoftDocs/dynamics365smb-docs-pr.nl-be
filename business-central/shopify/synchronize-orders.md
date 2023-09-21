---
title: Verkooporders synchroniseren en uitvoeren
description: Import en verwerking van verkooporders vanuit Shopify instellen en uitvoeren.
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30110, 30111, 30112, 30113, 30114, 30115, 30121, 30122, 30123, 30128, 30129, 30150, 30151, 30145, 30147'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
---

# Verkooporders synchroniseren en uitvoeren

In dit artikel worden de benodigde instellingen en stappen beschreven die u moet uitvoeren om verkooporders te synchroniseren en af te handelen met Shopify in [!INCLUDE[prod_short](../includes/prod_short.md)].

## De import van orders instellen op de Shopify-winkelkaart

Voer een **Valutacode** in als uw online winkel een andere valuta gebruikt dan de lokale valuta (LV). Voor de opgegeven valuta moeten wisselkoersen zijn geconfigureerd. Als uw online winkel dezelfde valuta gebruikt als [!INCLUDE[prod_short](../includes/prod_short.md)], laat u het veld leeg. 

U kunt winkelvaluta zien in de [Winkelgegevens](https://www.shopify.com/admin/settings/general)-instellingen in uw Shopify-beheer. Shopify kan worden geconfigureerd om verschillende valuta's te accepteren, maar in [!INCLUDE[prod_short](../includes/prod_short.md)] geïmporteerde orders gebruiken de winkelvaluta.

Een normale Shopify-order kan kosten bevatten naast het subtotaal, zoals verzendkosten of, indien ingeschakeld, fooien. Deze bedragen worden direct geboekt op de grootboekrekening die u wilt gebruiken voor specifieke transactiesoorten:

* **Rekening voor verzendkosten**
* **Rekening voor verkochte geschenkbonnen**; zie voor meer informatie [Geschenkbon](synchronize-orders.md#gift-cards)
* **Fooienrekening**  

Schakel **Automatisch orders maken** in om automatisch verkoopdocumenten te maken in [!INCLUDE[prod_short](../includes/prod_short.md)] zodra de Shopify-order is geïmporteerd.

Als u automatisch een verkoopdocument wilt vrijgeven, schakelt u de schakelaar **Verkooporder automatisch vrijgeven** in.

Als u het veld **Shopify-order-nr. op documentregel** selecteert, wordt deze informatie door [!INCLUDE [prod_short](../includes/prod_short.md)] herhaald op de verkoopregels van het type **Opmerking**, met het Shopify-ordernummer.

>[!NOTE]
>Het verkoopdocument in [!INCLUDE[prod_short](../includes/prod_short.md)] linkt naar de Shopify-order en u kunt het **Shopify-ordernummer toevoegen** aan de lijst- of kaartpagina's voor verkooporders, facturen en verzendingen. Ga voor meer informatie over het toevoegen van een veld naar [Een pagina personaliseren via de banner **Personaliseren**](../ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner). 

In het veld **Prioriteit van belastinggebied** kunt u de prioriteit definiëren voor het selecteren van de btw-gebiedscode voor adressen in orders. De Shopify-order die u importeert, bevat informatie over belastingen. Belastingen worden opnieuw berekend wanneer u verkoopdocumenten maakt, dus het is belangrijk dat de btw-/belastinginstellingen correct zijn in [!INCLUDE[prod_short](../includes/prod_short.md)]. Voor meer informatie over belastingen zie [Belastingen instellen voor de Shopify-verbinding](setup-taxes.md).

Specificeer hoe u retouren en terugbetalingen verwerkt:

* **Leeg** geeft aan dat u geen retouren en terugbetalingen importeert en verwerkt.
* **Alleen importeren** geeft aan dat u informatie importeert, maar dat u handmatig de bijbehorende creditnota maakt.
* **Creditnota automatisch maken** geeft aan dat u informatie importeert en dat [!INCLUDE[prod_short](../includes/prod_short.md)] automatisch de creditnota's maakt. Voor deze optie moet u de schakelaar **Automatisch verkooporder maken** inschakelen.

Geef een vestiging op voor retouren en grootboekrekeningen voor terugbetalingen voor goederen en andere terugbetalingen.

* **Terugbetalingsrekening voor niet-herbevoorradingsartikelen**: geeft een grootboekrekeningnummer op voor artikelen waarvoor u geen voorraadcorrectie wilt.
* **Terugbetalingsrekening**: geeft een grootboekrekening op voor het verschil tussen het totale terugbetaalde bedrag en het totaalbedrag van de artikelen.

Lees meer op [Retouren en terugbetalingen](synchronize-orders.md#returns-and-refunds)

### Toewijzing van verzendwijzen

De **Code van verzendwijze** voor verkoopdocumenten die worden geïmporteerd uit Shopify; kan automatisch worden ingevuld. U moet de **Toewijzing van verzendwijzen** configureren.

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u een toewijzing wilt definiëren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Toewijzing van verzendwijzen**. Hierdoor worden automatisch records gemaakt voor verzendmethoden die zijn gedefinieerd in de [**Verzenden**](https://www.shopify.com/admin/settings/payments)-instellingen in uw **Shopify-beheer**.
4. In het veld **Naam** kunt u de naam van de verzendmethode zien vanuit Shopify.
5. Voer de **Code van verzendwijze** in met de bijbehorende verzendmethode in [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Als er meerdere verzendkosten aan een verkooporder zijn gekoppeld, wordt er slechts één geselecteerd als de verzendmethode en toegewezen aan het verkoopdocument.

### Locatietoewijzing

De locatietoewijzing is vereist voor drie doeleinden:

* Als u voorraad wilt synchroniseren, raadpleegt u voor meer informatie [Voorraad synchroniseren met Shopify](synchronize-items.md#sync-inventory-to-shopify)
* De **Vestiging** invullen voor verkoopdocumenten die zijn geïmporteerd uit Shopify. Dat is belangrijk wanneer de schakelaar **Vestiging verplicht** is ingeschakeld op de kaart **Voorraadinstellingen**, anders kunt u geen verkoopdocumenten maken.
* De Shopify-order bijwerken met de afhandelingsinformatie op basis van de pagina **Geboekte verkoopzending**.

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u de toewijzing van vestigingen wilt configureren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Vestigingen** om de **Shopify-winkellocaties** te openen.
4. Kies de actie **Shopify-vestigingen ophalen** om alle locaties te importeren die zijn gedefinieerd in Shopify. U vindt ze in de [**Vestigingen**](https://www.shopify.com/admin/settings/locations)-instellingen in uw **Shopify beheer**-venster. Merk op dat de locatie gemarkeerd als *Standaard* wordt gebruikt bij het importeren van onvervulde Shopify-orders.
5. Voer de **Standaard vestiging** in met de bijbehorende locatie in [!INCLUDE[prod_short](../includes/prod_short.md)].

## De ordersynchronisatie uitvoeren

In de volgende procedure wordt beschreven hoe u de verkooporders importeert en bijwerkt.

> [!NOTE]  
> Gearchiveerde orders in Shopify kunnen niet worden geïmporteerd. Deactiveer de optie **De order automatisch archiveren** in het gedeelte **Orderverwerking** van de **Afrekening**-instellingen in uw deelvenster **Shopify-beheer** om ervoor te zorgen dat alle orders worden geïmporteerd naar [!INCLUDE[prod_short](../includes/prod_short.md)]. Als u gearchiveerde orders moet importeren, gebruikt u de actie **Orders dearchiveren** op de pagina [Orders](https://www.shopify.com/admin/orders) van het deelvenster **Shopify-beheer**.

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u orders wilt importeren, om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Orders**.
4. Kies de actie **Orders synchroniseren vanuit Shopify**.
5. Definieer indien nodig filters op orders. U kunt bijvoorbeeld volledig betaalde orders of orders met een laag risiconiveau importeren.

> [!NOTE]  
> Bij het filteren op tag moet u filtertokens `@` en `*` gebruiken. Als u bijvoorbeeld orders wilt importeren die *tag1* bevatten, gebruikt u `@*tag1*`. `@` zorgt dat het resultaat niet hoofdlettergevoelig is, terwijl `*` orders met meerdere tags vindt.

6. Kies de knop **Ok**.

U kunt ook zoeken naar de batchverwerking **Orders synchroniseren vanuit Shopify**.

U kunt plannen dat de taak automatisch wordt uitgevoerd. Zie voor meer informatie [Periodieke taken plannen](background.md#to-schedule-recurring-tasks).

### Onder de motorkap

De Shopify-connector importeert orders in twee stappen:

1.  Het importeert orderkoppen naar de tabel **Shopify - Te importeren orders** wanneer ze aan bepaalde voorwaarden voldoen:
    
* Ze worden niet gearchiveerd.
* Ze zijn gemaakt of gewijzigd na de laatste synchronisatie.

2.  Het importeert Shopify-orders en aanvullende informatie.
* De Shopify-connector verwerkt alle records in de tabel **Shopify - Te importeren orders** die overeenkomen met de filtercriteria die u hebt gedefinieerd op de aanvraagpagina **Orders synchroniseren vanuit Shopify**. Bijvoorbeeld tags, kanaal of de afhandelingsstatus. Als u geen filters hebt opgegeven, worden alle records verwerkt.
* Bij het importeren van een Shopify-order vraagt de Shopify-connector om aanvullende informatie vanuit Shopify:

    * Orderkoptekst
    * Orderregels
    * Informatie over verzending en afhandeling
    * Transacties
    * Retourzendingen en terugbetalingen, indien geconfigureerd

De pagina **Shopify - Te importeren orders** is handig voor het oplossen van problemen met het importeren van orders. U kunt de beschikbare orders beoordelen en de volgende stappen uitvoeren:

* Controleer of een fout de import van een specifieke order heeft geblokkeerd en bekijk de details van de fout. Controleer het veld **Bevat fout**.
* Verwerk alleen specifieke orders. U moet het veld **Winkelcode** invullen, een of meer orders selecteren en vervolgens de actie **Geselecteerde orders importeren** kiezen.
* Verwijder orders van de pagina **Shopify - Te importeren orders** om ze uit te sluiten van de synchronisatie.

## Geïmporteerde bestellingen bekijken

Zodra het importeren is voltooid, kunt u de Shopify-order verkennen en alle gerelateerde informatie zoeken, zoals de betalingstransacties, verzendkosten, risiconiveau, orderkenmerken en -tags of afhandelingen, als de order al is afgehandeld in Shopify. U kunt ook een orderbevestiging zien die naar de klant is verzonden door de actie **Shopify-statuspagina** te kiezen.

> [!NOTE]  
> U kunt rechtstreeks navigeren naar het venster **Shopify-orders** en u ziet dan orders met de status *Geopend* van alle winkels. Om voltooide orders te bekijken moet u de pagina **Shopify-orders** openen vanuit het specifieke **Shopify-winkelkaart** venster.

## Verkoopdocument maken in Business Central

Als de schakelaar **Automatisch orders maken** is ingeschakeld op de **Shopify-winkelkaart**, probeert [!INCLUDE[prod_short](../includes/prod_short.md)] een verkoopdocument te maken nadat de order is geïmporteerd. Als er problemen optreden, zoals een ontbrekende klant of product, moet u de problemen oplossen en vervolgens de verkooporder opnieuw maken.

### Verkoopdocumenten maken

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u orders wilt synchroniseren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Orders**.
4. Selecteer de order waarvoor u een verkoopdocument wilt maken en kies de actie **Verkoopdocumenten maken**.
5. Kies **Ja**.

Als de Shopify-order afhandeling vereist, wordt een **verkooporder** gemaakt. Voor volledig afgehandelde Shopify-orders, zoals bestellingen die alleen een cadeaubon bevatten of die al zijn afgehandeld in Shopify, wordt een **verkoopfactuur** gemaakt.

Er wordt nu een verkoopdocument gemaakt en het kan worden beheerd met behulp van de standaardfunctionaliteit van [!INCLUDE[prod_short](../includes/prod_short.md)].

### Ontbrekende klanten beheren

Als uw instellingen voorkomen dat automatisch een klant wordt gemaakt en geen juiste bestaande klant kan worden gevonden, moet u handmatig een klant toewijzen aan een Shopify-order. Dit kunt u op enkele manieren doen:

* U kunt het **orderklantnr.** toewijzen, en **Factuurklantnr.** rechtstreeks op de pagina **Shopify-orders** door een klant te kiezen uit de lijst met bestaande klanten.
* U kunt een klantsjablooncode selecteren en vervolgens de klant maken en toewijzen via de actie **Nieuwe klant maken** op de pagina **Shopify-orders**. Merk op dat de Shopify-klant minimaal één adres moet hebben. Bij orders die zijn gemaakt via het verkoopkanaal Shopify POS ontbreken vaak adresgegevens.
* U kunt een bestaande klant toewijzen aan de gerelateerde **Shopify-klant** in het venster **Shopify-klanten** en vervolgens de actie **Toewijzing zoeken** kiezen op de pagina **Shopify-orders**.

### Hoe de connector kiest welke klant te gebruiken

De functie *Order importeren uit Shopify* probeert de klant in de volgende volgorde te selecteren:

1. Als het **Standaardklantnr.** veld is gedefinieerd in de **Shopify-klantsjabloon** voor de **Code van verzendland/regio**, dan het **Standaardklantnr.** wordt gebruikt, ongeacht de instellingen in de velden **Klant importeren uit Shopify** en **Type klanttoewijzing**. Meer informatie op [Klantensjabloon per land/regio](synchronize-customers.md#customer-template-per-countryregion).
2. Als **Klant importeren uit Shopify** is ingesteld op *Geen* en het **Standaardklantnr.** is gedefinieerd op de pagina **Shopify-winkelkaart**, wordt het **Standaardklantnr.** gebruikt.

De volgende stappen zijn afhankelijk van het **Type klanttoewijzing**.

* Als het **Altijd de standaardklant nemen** is, gebruikt de connector de klant die is gedefinieerd in het veld **Standaardklantnr.** op de pagina **Shopify-winkelkaart**.
* Als het **Op e-mail/telefoon** is, probeert de connector eerst de bestaande klant te vinden op id, vervolgens op e-mailadres en dan op telefoonnummer. Als de klant niet wordt gevonden, maakt de connector een nieuwe klant.
* Als het **Op factureringsadresinfo** is, probeert de connector eerst de bestaande klant te vinden op id en vervolgens op het factuuradres. Als de klant niet wordt gevonden, maakt de connector een nieuwe klant.

> [!NOTE]  
> De connector gebruikt informatie van het factuuradres en creëert de factuurklant [!INCLUDE[prod_short](../includes/prod_short.md)]. De orderklant is dezelfde als de factuurklant.

### Verschillende verwerkingsregels voor orders

Misschien wilt u orders anders verwerken op basis van een regel. Voor bestellingen van een specifiek verkoopkanaal, zoals POS, moet bijvoorbeeld de standaardklant worden gebruikt, maar u wilt dat uw online winkel echte informatie over de klant heeft.

Een manier om aan deze vereiste te voldoen, is door een extra Shopify-winkelkaart te maken en filters te gebruiken op de aanvraagpagina **Orders synchroniseren vanuit Shopify** .

Voorbeeld: u hebt een online winkel en een Shopify POS. Voor uw POS wilt u een vaste klant gebruiken, maar voor uw webwinkel wilt u klanten maken in [!INCLUDE[prod_short](../includes/prod_short.md)]. De volgende procedure somt de stappen op hoog niveau op. Ga voor meer informatie naar de bijbehorende Help-artikelen.

1. Maak een Shopify-winkel met de naam *STORE* en koppel deze aan uw Shopify-account.
2. Configureer artikel-/productsynchronisatie zodat deze winkel productinformatie beheert.
3. Geef op dat klanten met orders worden geïmporteerd. De connector moet klanten vinden door naar hun e-mailadres te zoeken. Als het geen adres vindt, gebruikt het de klantsjabloon om een nieuwe klant te maken.
4. Maak een Shopify-winkel met de naam *POS* en koppel deze aan uw Shopify-account.
6. Zorg ervoor dat synchronisatie van artikel/product is uitgeschakeld.
7. Selecteer de connector die de standaardklant gebruikt.
8. Maak een terugkerend taakwachtrij-item voor rapport 30104 **Orders synchroniseren vanuit Shopify**. Selecteer **STORE** in het veld **Shopify-winkelcode** en gebruik filters om alle orders te krijgen, behalve orders die het POS-verkoopkanaal maakt. Bijvoorbeeld **<>Point of Sale**
9. Maak een terugkerend taakwachtrij-item voor het rapport 30104 **Orders synchroniseren vanuit Shopify**. Selecteer **POS** in het veld **Shopify-winkelcode** en gebruik filters om orders te krijgen die zijn gegenereerd door het POS-verkoopkanaal. Bijvoorbeeld **<>Point of Sale**.

Elke taakwachtrij importeert en verwerkt orders binnen de gedefinieerde filters en gebruikt de regels van de bijbehorende Shopify-winkelkaart. Ze maken bijvoorbeeld verkooppuntorders voor de standaardklant.

>![Belangrijk] Om conflicten bij het verwerken van orders te voorkomen, moet u eraan denken dezelfde taakwachtrijcategorie te gebruiken voor beide taakwachtrij-items.

### Impact van bewerkingen van orders

In Shopify:

|Bewerken|Gevolgen voor reeds geïmporteerde order|Gevolgen voor order die voor het eerst wordt geïmporteerd|
|------|-----------|-----------|
|De afhandelingslocatie wijzigen | Oorspronkelijke vestiging is in regels | De afhandelingsvestiging is gesynchroniseerd met [!INCLUDE[prod_short](../includes/prod_short.md)].|
|Een order bewerken en de hoeveelheid verhogen| De orderkop en de aanvullende tabellen worden bijgewerkt in [!INCLUDE[prod_short](../includes/prod_short.md)], regels niet.| Geïmporteerde order gebruikt nieuwe hoeveelheid|
|Een order bewerken en de hoeveelheid verlagen| De orderkop en de aanvullende tabellen worden bijgewerkt in [!INCLUDE[prod_short](../includes/prod_short.md)], regels niet.| Geïmporteerde order gebruikt de oorspronkelijke hoeveelheid, het veld Afhandelbare hoeveelheid bevat een nieuwe waarde.|
|Een order bewerken en een bestaand artikel verwijderen | De orderkop en de aanvullende tabellen worden bijgewerkt in [!INCLUDE[prod_short](../includes/prod_short.md)], regels niet.| Verwijderde artikelen worden nog steeds geïmporteerd, het veld Afhandelbare hoeveelheid bevat nul. |
|Een order bewerken en een nieuw artikel toevoegen | De orderkop wordt bijgewerkt, de regels niet. | Originele en toegevoegde artikelen worden geïmporteerd. |
|Order verwerken: afhandelen, betalingsinformatie bijwerken | De orderkop wordt bijgewerkt, maar de regels niet. |De wijziging heeft geen invloed op hoe de order wordt geïmporteerd.|
|Order annuleren | De orderkop wordt bijgewerkt, maar de regels niet. |Geannuleerde order wordt niet geïmporteerd |

In [!INCLUDE[prod_short](../includes/prod_short.md)]:

|Bewerken|Impact|
|------|-----------|
|De vestiging wijzigen in een andere vestiging, toegewezen aan de Shopify-vestigingen. Verzending boeken | Order wordt gemarkeerd als afgehandeld. De oorspronkelijke vestiging wordt gebruikt. |
|De vestiging wijzigen in een andere vestiging, niet toegewezen aan de Shopify-vestigingen. Verzending boeken | De afhandeling wordt niet gesynchroniseerd met Shopify. |
|De hoeveelheid verlagen. Verzending boeken | De Shopify-order wordt gemarkeerd als gedeeltelijk vervuld. |
|De hoeveelheid verhogen. Verzending boeken | De afhandeling wordt niet gesynchroniseerd met Shopify. |
|Een nieuw artikel toevoegen. Verzending boeken | De Shopify-order wordt gemarkeerd als afgehandeld. Regels worden niet bijgewerkt. |

## Verzendingen synchroniseren met Shopify

Wanneer een verkooporder die is gemaakt op basis van een Shopify-order, wordt verzonden, kunt u de verzendingen synchroniseren met Shopify.

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verzendingen combineren met Shopify** in en kies vervolgens de gerelateerde koppeling.
2. Definieer indien nodig de filters op verzendingen. U kunt bijvoorbeeld een verzending bijwerken die op een specifieke datum is geboekt.
3. Kies de knop **Ok**.

De order binnen Shopify wordt gemarkeerd als vervuld. De klant ontvangt automatisch een verzendbericht per e-mail of sms. Als er een expediteur en een traceringscode op de verzending zijn vermeld, wordt de trackinginformatie in de e-mail opgenomen.

Gebruik als alternatief de actie **Verzendingen synchroniseren** op de pagina Shopify-verkooporders of Shopify-winkel.

U kunt de volgende taken plannen om geautomatiseerd te worden uitgevoerd. Zie voor meer informatie [Periodieke taken plannen](background.md#to-schedule-recurring-tasks).

>[!Important]
>De vestiging, inclusief blanco vestiging, gedefinieerd op de geboekte verzendingsregel, moet een overeenkomende record hebben op de Shopify-vestiging. Anders wordt deze regel niet teruggestuurd naar Shopify. Meer informatie op [Locatietoewijzing](synchronize-orders.md#location-mapping).

Vergeet niet **Orders synchroniseren vanuit Shopify** uit te voeren om de afhandelingsstatus van een order bij te werken in [!INCLUDE[prod_short](../includes/prod_short.md)]. De connectorfunctionaliteit archiveert ook volledig betaalde en afgehandelde orders in zowel Shopify als [!INCLUDE[prod_short](../includes/prod_short.md)], mits aan de voorwaarden is voldaan.

### Expediteurs en tracerings-URL

Als het document van de **geboekte verkoopverzending** de **Expediteurscode** en/of **Traceringsnummer (zending)** bevat, wordt deze informatie in de e-mail met de verzendbevestiging verzonden naar Shopify en naar de klant.

Het traceringsbedrijf wordt ingevuld in de volgende volgorde (van hoog naar laag) op basis van de expediteurrecord:

* **Shopify-traceringsbedrijf**
* **Naam**
* **Code**

Als het veld **Tracerings-URL van pakket** is ingevuld voor de expediteursrecord, bevat de verzendbevestiging ook een tracerings-URL.

## Retouren en terugbetalingen

Bij een integratie tussen Shopify en [!INCLUDE[prod_short](../includes/prod_short.md)] is het belangrijk om zoveel mogelijk bedrijfsgegevens te kunnen synchroniseren. Dat maakt het gemakkelijker om uw financiën en voorraadniveaus up-to-date te houden in [!INCLUDE[prod_short](../includes/prod_short.md)]. De gegevens die u kunt synchroniseren, omvatten retouren en terugbetalingen die zijn geregistreerd in Shopify-beheer of Shopify POS.

Retouren en terugbetalingen worden geïmporteerd met hun gerelateerde orders als u het verwerkingstype op de Shopify-winkelkaart hebt ingeschakeld.

Retouren worden alleen ter informatie geïmporteerd. Er is geen verwerkingslogica aan verbonden.

Financiële en indien nodig voorraadtransacties worden verwerkt via terugbetalingen. Terugbetalingen kunnen producten omvatten of alleen bedragen, bijvoorbeeld als een handelaar heeft besloten verzendkosten of een ander bedrag te compenseren.
U kunt verkoopcreditnota's voor terugbetalingen maken. De creditnota's kunnen de volgende typen regels hebben:

|Type|Nr.|Opmerking|
|-|-|-|
|Grootboekrekening|Rekening voor verkochte geschenkbonnen| Gebruik voor terugbetalingen met betrekking tot cadeaubonnen.|
|Grootboekrekening|Terugbetalingsrekening niet-herbevoorrading | Gebruik voor terugbetalingen met betrekking tot producten die niet zijn aangevuld. |
|Artikel |Artikelnr.| Gebruik voor terugbetalingen met betrekking tot producten die zijn aangevuld. Geldig voor directe terugbetalingen of terugbetalingen gekoppeld aan terugbetalingen. De vestigingscode op de kredietregel wordt ingesteld op basis van de geselecteerde waarde voor de retourvestiging.|
|Grootboekrekening| Terugbetalingsrekening | Gebruik voor andere terugbetaalde bedragen die niet gerelateerd zijn aan producten of cadeaubonnen. Bijvoorbeeld fooien of als u handmatig een terug te betalen bedrag hebt opgegeven in Shopify. |

>[!Note]
>De retourvestiging, inclusief lege vestigingen, gedefinieerd op de **Shopify-winkelkaart**, worden gebruikt op de gemaakte creditnota. Het systeem negeert de oorspronkelijke vestigingen van ordes of zendingen.

## Geschenkbonnen

In de Shopify-winkel kunt u cadeaubonnen verkopen, die kunnen worden gebruikt om voor echte producten te betalen.

Bij het omgaan met cadeaubonnen is het belangrijk om een waarde in te voeren in het veld **Rekening voor verkochte geschenkbonnen** in het venster **Shopify-winkelkaart**. De verkochte cadeaukaart wordt gesynchroniseerd samen met bestellingen op de regel. Een toegepaste cadeaubon wordt ook geïmporteerd met de bestelling, maar nu als transactie. Merk op dat de cadeaubon het te factureren bedrag niet verlaagt.

Om de uitgegeven en toegepaste cadeaubonnen te bekijken kiest u het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Geschenkbonnen** in en kiest u vervolgens de gerelateerde koppeling.

## Zie ook

[Aan de slag met de connector voor Shopify](get-started.md)  
