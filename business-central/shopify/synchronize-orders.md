---
title: Verkooporders synchroniseren en uitvoeren
description: Import en verwerking van verkooporders vanuit Shopify instellen en uitvoeren.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: ce11aa8766550e72cab2f811ef6602dba4271211
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9076317"
---
# <a name="synchronize-and-fulfill-sales-orders"></a>Verkooporders synchroniseren en uitvoeren

In dit artikel worden de benodigde instellingen en stappen beschreven die u moet uitvoeren om verkooporders te synchroniseren en af te handelen vanuit Shopify in [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="set-the-import-of-orders-on-the-shopify-shop-card"></a>De import van orders instellen op de Shopify-winkelkaart

Een reguliere Shopify-order kan extra bedragen hebben, zoals verzendkosten of, indien ingeschakeld, fooien. Deze bedragen worden direct op de grootboekrekeningen geboekt. Kies de grootboekrekening die voor specifieke transacties moet worden gebruikt:

- **Rekening voor verzendkosten**
- **Rekening voor verkochte geschenkbonnen**. Zie voor meer informatie [Geschenkbon](synchronize-orders.md#gift-cards).
- **Fooienrekening**  

Schakel **Automatisch orders maken** in om automatisch verkoopdocumenten te maken in [!INCLUDE[prod_short](../includes/prod_short.md)] zodra de Shopify-order is geïmporteerd.
Het verkoopdocument in [!INCLUDE[prod_short](../includes/prod_short.md)] bevat een koppeling naar de Shopify-order. Als u het veld **Shopify-order-nr. op documentregel** selecteert, wordt deze informatie herhaald op de verkoopregels van het type *Opmerking*.

In het veld **Bron van belastinggebied** kunt u prioriteit definiëren voor het selecteren van de btw-gebiedscode of de btw-bedrijfsboekingsgroep, op basis van adres. Deze stap is relevant voor landen/regio's met sales tax, maar kan worden gebruikt voor btw-landen/regio's. Zie [Opmerkingen over belasting](synchronize-orders.md#tax-remarks) voor meer informatie.

### <a name="shipment-method-mapping"></a>Toewijzing van verzendwijzen

De **Code van verzendwijze** voor verkoopdocumenten die worden geïmporteerd uit Shopify; kan automatisch worden ingevuld. U moet de **Toewijzing van verzendwijzen** configureren.

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u toewijzing wilt definiëren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Toewijzing van verzendwijzen**. De records voor verzendmethoden die zijn gedefinieerd in de [**Verzenden**](https://www.shopify.com/admin/settings/payments)-instellingen in uw **Shopify-beheer**, worden automatisch gemaakt.
4. In het veld **Naam** kunt u de naam van de verzendmethode zien vanuit Shopify.
5. Voer de **Code van verzendwijze** in met de bijbehorende verzendmethode in [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> Als er meerdere verzendkosten aan een verkooporder zijn gekoppeld, wordt er slechts één geselecteerd als de verzendmethode en toegewezen aan het verkoopdocument.

### <a name="payment-method-mapping"></a>Toewijzing van betalingsmethoden

Om de **Code van betalingsmethode** automatisch in te vullen voor verkoopdocumenten die worden geïmporteerd uit Shopify, moet u de **Toewijzing van betalingsmethoden** configureren.

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u toewijzing wilt definiëren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Toewijzing van betalingsmethoden**.
4. Voer in de velden **Gateway** en **Creditcardmaatschappij** de naam in van de betalingsmethode uit Shopify. De record wordt automatisch gemaakt wanneer u Shopify-orders importeert.
5. Voer de **Betalingswijze** in met de bijbehorende betalingsmethode in [!INCLUDE[prod_short](../includes/prod_short.md)].
6. Stel de **Prioriteit** in voor gevallen waarin de klant meerdere betalingsmethoden gebruikt. De betalingsmethode met de hoogste prioriteit wordt geselecteerd in het verkoopdocument. Als beide betalingsmethoden dezelfde prioriteit hebben, wordt de betalingsmethode met het hoogste bedrag gebruikt.

### <a name="location-mapping"></a>Locatietoewijzing

Om de **Vestiging** automatisch in te vullen voor verkoopdocumenten die worden geïmporteerd uit Shopify, moet u de **Shopify - Winkelvestigingen** configureren.

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u de toewijzing van locaties wilt configureren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Vestigingen** om de **Shopify-winkellocaties** te openen.
4. Kies de actie **Shopify-vestigingen ophalen** om alle locaties te importeren die zijn gedefinieerd in Shopify. U vindt ze in de [**Vestigingen**](https://www.shopify.com/admin/settings/locations)-instellingen in uw **Shopify beheer**-venster. Merk op dat de locatie gemarkeerd als *Standaard* wordt gebruikt bij het importeren van onvervulde Shopify-orders.
5. Voer de **Standaard vestiging** in met de bijbehorende locatie in [!INCLUDE[prod_short](../includes/prod_short.md)].

> [!NOTE]  
> U moet de vestigingstoewijzing configureren als de schakelaar **Vestiging verplicht** is ingeschakeld op de kaart **Voorraadinstellingen**, anders kunt u geen verkoopdocumenten maken.

## <a name="run-the-order-synchronization"></a>De ordersynchronisatie uitvoeren

In de volgende procedure wordt beschreven hoe u de verkooporders importeert en bijwerkt.

> [!NOTE]  
> Gearchiveerde orders in Shopify kunnen niet worden geïmporteerd. Deactiveer de optie **De order automatisch archiveren** in het gedeelte **Orderverwerking** van de **Afrekening**-instellingen in uw deelvenster **Shopify-beheer** om ervoor te zorgen dat alle orders worden geïmporteerd naar [!INCLUDE[prod_short](../includes/prod_short.md)]. Als u gearchiveerde orders moet importeren, gebruikt u de actie **Orders deactiveren** op de pagina [Orders](https://www.shopify.com/admin/orders) van het deelvenster Shopify-beheer.

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u orders wilt importeren, om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Orders**.
4. Kies de actie **Orders synchroniseren vanuit Shopify**.
5. Definieer indien nodig filters op orders. U kunt bijvoorbeeld volledig betaalde orders of orders met een laag risiconiveau importeren.
6. Kies de knop **Ok**.

U kunt ook zoeken naar de batchverwerking **Orders synchroniseren vanuit Shopify**.

U kunt de volgende taken plannen om geautomatiseerd te worden uitgevoerd. Zie voor meer informatie [Terugkerende taken plannen](background.md#to-schedule-recurring-tasks).

## <a name="review-imported-orders"></a>Geïmporteerde bestellingen bekijken

Zodra het importeren is voltooid, kunt u de Shopify-order verkennen en alle gerelateerde informatie vinden. Zoek bijvoorbeeld de betalingstransacties, verzendkosten, het risiconiveau of afhandelingen als de order al is uitgevoerd in Shopify. U kunt ook een orderbevestiging zien die naar de klant is verzonden door de actie **Shopify-statuspagina** te kiezen.

> [!NOTE]  
> U kunt rechtstreeks navigeren naar het venster **Shopify-orders** en u ziet dan orders met de status *Geopend* van alle winkels. Om voltooide orders te bekijken moet u de pagina **Shopify-orders** openen vanuit het specifieke **Shopify-winkelkaart** venster.

## <a name="create-sales-documents-in-business-central"></a>Verkoopdocument maken in Business Central

Als de schakelaar **Automatisch orders maken** is ingeschakeld op de **Shopify-winkelkaart**, probeert [!INCLUDE[prod_short](../includes/prod_short.md)] een verkoopdocument te maken zodra de order is geïmporteerd. Als het proces problemen oplevert, bijvoorbeeld als er een klant of product ontbreekt, moet u het probleem oplossen. Vervolgens kunt u proberen de verkooporder opnieuw te maken.

### <a name="to-create-sales-documents"></a>Verkoopdocumenten maken

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u orders wilt synchroniseren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Orders**.
4. Selecteer de order waarvoor u een verkoopdocument wilt maken en kies de actie **Verkoopdocumenten maken**.
5. Kies **Ja**.

Als de Shopify-order afhandeling vereist, wordt een **verkooporder** gemaakt. Voor volledig afgehandelde Shopify-orders, zoals bestellingen die alleen een cadeaubon bevatten of die al zijn afgehandeld in Shopify, wordt een **verkoopfactuur** gemaakt.

Er wordt nu een verkoopdocument gemaakt en het kan worden beheerd met behulp van de standaardfunctionaliteit van [!INCLUDE[prod_short](../includes/prod_short.md)].

### <a name="manage-missing-customers"></a>Ontbrekende klanten beheren

Als uw instellingen voorkomen dat automatisch een klant wordt gemaakt en geen juiste bestaande klant kan worden gevonden, wijst u handmatig een klant toe aan een Shopify-bestelling. Er zijn enkele opties:

- U kunt het **orderklantnr.** toewijzen, rechtstreeks in de **Shopify-order** door een klant te kiezen uit de lijst met bestaande klanten.
- U kunt een klantsjablooncode selecteren, de klant maken en toewijzen via de actie **Nieuwe klant maken** op de pagina **Shopify-orders**.
- U kunt een bestaande klant toewijzen aan de gerelateerde **Shopify-klant** in het venster **Shopify-klanten** en vervolgens de actie **Toewijzing zoeken** kiezen op de pagina **Shopify-orders**.

### <a name="tax-remarks"></a>Opmerkingen over belasting

Terwijl de geïmporteerde Shopify-order informatie over belastingen bevat, worden de belastingen opnieuw berekend wanneer u het verkoopdocument maakt. Vanwege de herberekening is het belangrijk dat de btw/belasting-instellingen correct zijn in [!INCLUDE[prod_short](../includes/prod_short.md)].

- Meerdere productbelasting/btw-tarieven. Sommige productcategorieën zijn bijvoorbeeld onderworpen aan verlaagde belastingtarieven. Die items moeten bestaan in [!INCLUDE[prod_short](../includes/prod_short.md)] en zijn toegewezen aan Shopify-producten. Anders wordt bij het automatisch maken van ontbrekende artikelen de btw-productboekingsgroep gebruikt.

- Adresafhankelijke belastingtarieven. Gebruik het veld **Prioriteit van belastinggebied** samen met de tabel **Klantensjablonen** om standaardlogica te overschrijven die de **Code van belastinggebied** invult in het verkoopdocument. Het veld **Prioriteit van belastinggebied** specificeert de prioriteit waar de functie de informatie over land/regio en staat/provincie vandaan moet halen. Dan wordt de bijbehorende record in de Shopify-klantsjablonen gevonden en worden **Code van belastinggebied**, **Belastingplichtig** en **Btw-bedrijfsboekingsgroep** gebruikt wanneer een verkoopdocument wordt gemaakt.

- Prijs inclusief btw. Het veld **Prijzen inclusief btw**/**Prijzen inclusief omzetbelasting** in het gemaakte verkoopdocument is niet afhankelijk van de klant, maar van de **Klantensjabloon** van de Shopify-winkelkaart of de klantensjabloon per land/regio.

### <a name="impact-of-edits-of-orders"></a>Impact van bewerkingen van orders

|Bewerken|Impact|
|------|-----------|
|Wijzig in Shopify de afhandelingslocatie | De oorspronkelijke locatie wordt gesynchroniseerd met [!INCLUDE[prod_short](../includes/prod_short.md)]. |
|Bewerk in Shopify een order en wijzig de hoeveelheid| De orderkop en de aanvullende tabellen worden bijgewerkt in [!INCLUDE[prod_short](../includes/prod_short.md)], regels niet. |
|Bewerk in Shopify een order en voeg een nieuw artikel toe | De orderkop wordt bijgewerkt, de regels niet. |
|Wijzig in [!INCLUDE[prod_short](../includes/prod_short.md)] de vestiging in een andere vestiging, toegewezen aan de Shopify-vestigingen. Verzending boeken | Na het synchroniseren van de afhandeling wordt de vestiging bijgewerkt in Shopify. |
|Wijzig in [!INCLUDE[prod_short](../includes/prod_short.md)] de vestiging in een andere vestiging, niet toegewezen aan de Shopify-vestigingen. Verzending boeken | De afhandeling wordt niet gesynchroniseerd met Shopify. |
|Verlaag in [!INCLUDE[prod_short](../includes/prod_short.md)] de hoeveelheid. Verzending boeken | De Shopify-order wordt gemarkeerd als gedeeltelijk vervuld. |
|Voeg in [!INCLUDE[prod_short](../includes/prod_short.md)] een nieuw artikel toe. Verzending boeken | De Shopify-order wordt gemarkeerd als afgehandeld. Regels worden niet bijgewerkt. |

## <a name="synchronize-shipments-to-shopify"></a>Verzendingen synchroniseren met Shopify

Wanneer een verkooporder die is gemaakt op basis van een Shopify-order, wordt verzonden, kunt u de verzendingen synchroniseren met Shopify.

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verzendingen combineren met Shopify** in en kies vervolgens de gerelateerde koppeling.
2. Definieer indien nodig de filters op verzendingen. U kunt bijvoorbeeld een verzending bijwerken die op een specifieke datum is geboekt.
3. Kies de knop **OK**.

De order binnen Shopify wordt gemarkeerd als vervuld. De klant ontvangt automatisch een verzendbericht per e-mail of sms. Als er een expediteur en een traceringscode op de verzending zijn vermeld, wordt de trackinginformatie in de e-mail opgenomen.

> [!NOTE]  
> Vergeet niet **Orders synchroniseren vanuit Shopify** uit te voeren om de afhandelingsstatus van de order bij te werken in [!INCLUDE[prod_short](../includes/prod_short.md)]. De connectorfunctionaliteit archiveert ook volledig betaalde en afgehandelde orders in zowel Shopify als [!INCLUDE[prod_short](../includes/prod_short.md)], mits aan de voorwaarden is voldaan.

### <a name="shipping-agents-and-tracking-url"></a>Expediteurs en tracerings-URL

Als het document van de **geboekte verkoopverzending** de **Expediteurscode** en/of **Traceringsnummer (zending)** bevat, wordt deze informatie in de e-mail met de verzendbevestiging verzonden naar Shopify en naar de eindklant.

Het traceringsbedrijf wordt ingevuld op basis van de expediteurrecord met de volgende prioriteiten (van hoog naar laag):

- **Shopify-traceringsbedrijf**
- **Naam**
- **Code**

Als het veld **Tracerings-URL van pakket** is ingevuld voor de expediteursrecord, bevat de verzendbevestiging ook een tracerings-URL.

## <a name="gift-cards"></a>Geschenkbonnen

In de Shopify-winkel kunt u cadeaubonnen verkopen, die later kunnen worden gebruikt om voor echte producten te betalen.

Bij het omgaan met cadeaubonnen is het belangrijk om een waarde in te voeren in het veld **Rekening voor verkochte geschenkbonnen** in het venster **Shopify-winkelkaart**. De verkochte cadeaukaart wordt gesynchroniseerd samen met bestellingen op de regel. Een toegepaste cadeaubon wordt ook geïmporteerd met de bestelling, maar nu als transactie. Merk op dat de cadeaubon het te factureren bedrag niet verlaagt.

Om de uitgegeven en toegepaste cadeaubonnen te bekijken kiest u het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Geschenkbonnen** in en kiest u vervolgens de gerelateerde koppeling.

## <a name="transactions"></a>Transacties

De betalingstransacties die plaatsvonden in Shopify, worden gesynchroniseerd met de bestellingen en kunnen worden bekeken vanuit de pagina *Shopify-orders*.

Als u alle transacties wilt bekijken, kiest u het ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Transacties** in en selecteert u vervolgens de gerelateerde koppeling.

## <a name="payouts"></a>Uitbetalingen

Als uw winkel Shopify Payments heeft ingeschakeld, ontvangt u betalingen via *Shopify-uitbetalingen* wanneer een klant betaalt met Shopify Payments en versneld afrekenen.

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u uitbetalingen wilt synchroniseren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Uitbetalingen synchroniseren**.

Als u alle uitbetalingen wilt bekijken, kiest u het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Uitbetalingen** in en selecteert u vervolgens de gerelateerde koppeling.

## <a name="see-also"></a>Zie ook

[Aan de slag met de connector voor Shopify](get-started.md)  
