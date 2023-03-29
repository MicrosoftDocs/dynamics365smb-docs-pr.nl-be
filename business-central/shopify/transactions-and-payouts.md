---
title: Synchroniseren en transacties en uitbetalingen
description: Import van transacties en uitbetalingen vanuit Shopify instellen en uitvoeren.
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30124, 30125, 30130, 30131, 30132, 30133, 30134,'
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
---

# Transacties en uitbetalingen

Wanneer een klant het afrekenen in de online winkel voltooit, wordt de informatie over betalingen opgeslagen als een **Transactie**. Er kunnen meerdere transacties aan de bestelling zijn gekoppeld, bijvoorbeeld wanneer een klant een cadeaubon gebruikt om een deel van de kosten te betalen en vervolgens een creditcard of PayPal gebruikt voor het resterende bedrag.

Als u Shopify Payment als betalingsprovider gebruikt, kunt u naast informatie over geld dat door de betalingsprovider van de klant is ontvangen, ook uitbetalingen zien van Shopify naar uw bankrekening.

## Transacties

De betalingstransacties die plaatsvinden in Shopify, worden gesynchroniseerd met de orders en kunnen worden bekeken op de pagina **Shopify-orders**.

Als u alle transacties wilt bekijken, kiest u het ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Transacties** in en selecteert u vervolgens de gerelateerde koppeling.

Als u de toewijzing van een betalingsmethode hebt geconfigureerd, wordt aan het gecreëerde verkoopdocument een betalingsmethodecode toegewezen. Zie voor meer informatie [Toewijzing van betalingsmethoden](#payment-method-mapping).

## Uitbetalingen

Als uw winkel Shopify Payment gebruikt, ontvangt u betalingen via **Shopify-uitbetalingen** wanneer een klant betaalt met Shopify Payments en versneld afrekenen.

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u uitbetalingen wilt synchroniseren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Uitbetalingen synchroniseren**.

Als u alle uitbetalingen wilt bekijken, kiest u het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Uitbetalingen** in en selecteert u vervolgens de gerelateerde koppeling.

**Uitbetalingen** zijn alleen voor informatieve doeleinden en hebben geen invloed op het grootboek, hoewel ze handig kunnen zijn bij het verwerken van uw bankrekeningafschrift.

## Toewijzing van betalingsmethoden

Om de **Code van betalingsmethode** automatisch in te vullen voor verkoopdocumenten die worden geïmporteerd uit Shopify, moet u **Toewijzing van betalingsmethoden** configureren.

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u een toewijzing wilt definiëren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Toewijzing van betalingsmethoden**.
4. Voer in de velden **Gateway** en **Creditcardmaatschappij** de naam in van de betalingsmethode uit Shopify. De record wordt automatisch gemaakt wanneer u Shopify-orders importeert.
5. Voer de **Betalingswijze** in met de bijbehorende betalingsmethode in [!INCLUDE[prod_short](../includes/prod_short.md)].
6. Stel de **Prioriteit** in voor gevallen waarin de klant meerdere betalingsmethoden gebruikt. De betalingsmethode met de hoogste prioriteit wordt geselecteerd in het verkoopdocument. Als beide betalingsmethoden dezelfde prioriteit hebben, wordt de betalingsmethode met het hoogste bedrag gebruikt.

> [!NOTE]  
> Als voor de bijbehorende betaalmethode in [!INCLUDE[prod_short](../includes/prod_short.md)] **Grootboekrekening** en **Tegenrekeningnr.** zijn ingevuld, maakt het factuursysteem tijdens het boeken een tegenboeking van het type *Betaling* en wordt deze vereffend met het *Factuur*-type in de klantenpost.

## Praktijkgevallen
  
Partijen:

* Koper - persoon die goederen koopt van online Shopify-winkel.
* Handelaar - uw bedrijf.
* Betalingsprovider - bedrijf dat de betalingsverwerking voor u faciliteert. Kan Shopify Payments of een derde partij zijn.

### Hoe geld stroomt

De koper koopt goederen in de online winkel. De laatste stap is het verwerken van de betaling.

>[!NOTE]
> Dit voorbeeld dekt geen gevallen waarin de betaling is voltooid buiten Shopify-afhandeling om, wat geldig is voor B2B-scenario's.
  
De koper betaalt met creditcard, PayPal of een lokale betaalmethode zoals MobilePay in Denemarken. De betalingsprovider neemt het volledige bedrag van de Koper in ontvangst. Op dit moment wordt het geld van de Koper overgemaakt naar de betalingsprovider.

Afhankelijk van de betalingsprovider kan de handelaar dit geld op zijn rekening bij de betalingsprovider zien - zowel ontvangen bedragen als ingehouden commissies. Betalingsaanbieders nemen vaak een commissie van elke transactie en in sommige gevallen kunnen ze ook een vast bedrag hebben.
  
Afhankelijk van de betalingsprovider activeert de handelaar een overboeking van het geld naar zijn bankrekening (uitbetaling) handmatig of gebeurt dit automatisch binnen een bepaalde periode - eenmaal per dag, eenmaal per maand, enzovoort.
  
Afhankelijk van de bank kan de Handelaar deze inkomende transactie op zijn bankrekening zien via internetbankieren of in het bankafschrift.

Er zijn verschillende opties voor het afhandelen van betalingstransacties in [!INCLUDE[prod_short](../includes/prod_short.md)]
  
### Optie 1: inkomende overschrijvingen op bankrekening afstemmen met originele facturen
  
Verkoper importeert verkooporder naar [!INCLUDE[prod_short](../includes/prod_short.md)] en boekt verzending en factuur.

Resultaat: systeem creëert een **klantenpost** van het type *Factuur* met het volledige bedrag. **Open** is ingesteld op Ja. Het **resterend bedrag** gelijk is aan het factuurbedrag.

Handelaar importeert bankafschrift met behulp van betalingsreconciliatiejournaal.

problemen:

1. Kan lastig zijn als er meerdere facturen (en creditnota's) zijn, maar één uitbetaling van de betalingsprovider met een forfaitair bedrag.
2. Bedrag komt meestal niet overeen vanwege commissie. U kunt betalingstolerantie en/of betalingskortingen gebruiken om vergoedingen af te handelen.

### Optie 2: reconcilieer inkomende overschrijvingen naar bankrekening met tussentijdse rekening die geld vertegenwoordigt bij de betalingsprovider
  
Verkoper importeert verkooporder naar [!INCLUDE[prod_short](../includes/prod_short.md)] en boekt verzending en factuur.
  
Resultaat: systeem creëert een klantenpost van het type **Factuur** met het volledige bedrag. **Open** is ingesteld op Ja. Het **resterend bedrag** gelijk is aan het factuurbedrag.

Omdat de verkooporder echter een betalingsmethodecode heeft waarbij de velden **Tegenrekeningsoort** en **Tegenrekeningnummer** zijn ingevuld, maakt het systeem automatisch een andere klantpost van het type **Betaling** en past deze toe op de eerder gemaakte klantenpost.

>[!NOTE]
> Het systeem vult het veld Betalingswijze in op basis van de toewijzing van betalingsmethoden. Zie voor meer informatie [Toewijzing van betalingsmethoden](#payment-method-mapping).
  
U kunt saldorekeningen voor betalingsmethoden op twee manieren definiëren:

* **Tegenrekeningsoort**, ingesteld als *Bank* en **Bankrekeningnr.**, vullen de speciale bankrekening in die uw rekening vertegenwoordigt bij de betalingsprovider.
* **Tegenrekeningsoort**, ingesteld als *Grootboekrekening** en **Bankrekeningnr.**, vullen de grootboekbankrekening in die uw rekening vertegenwoordigt bij de betalingsprovider.

Het is zinvol om een bankrekening te gebruiken als de betalingsprovider een soort rekeningafschrift exporteert, dat u kunt importeren in het betalingsreconciliatiejournaal.

De handelaar importeert het bankafschrift met behulp van betalingsreconciliatiejournaal. De inkomende uitbetaling kan worden verwerkt:

* als overschrijving van een andere bank. Als de overboeking een paar dagen duurt of een valutawisselkoers vereist, kunt u een tussentijdse grootboekrekening gebruiken.
* als verschil op de grootboekrekening die uw rekening vertegenwoordigt bij de betalingsprovider.
  
Het resterende saldo op de grootboek- of bankrekening die uw rekening bij de betalingsprovider vertegenwoordigt, kan worden afgeschreven als 'Kosten/commissies'

problemen:

1. U kunt meerdere grootboek- of bankrekeningen maken als u met meerdere betalingsproviders te maken hebt. Verkooporders in [!INCLUDE[prod_short](../includes/prod_short.md)] ondersteunen echter slechts één betalingsmethodecode, wat het moeilijk maakt om gevallen te behandelen waarin een koper meerdere betalingsmethoden gebruikt voor een order.

## Zie ook

[Aan de slag met de connector voor Shopify](get-started.md)  
