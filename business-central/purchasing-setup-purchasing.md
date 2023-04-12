---
title: Overzicht van taken om inkoop in te stellen
description: Beschrijft de taken voor het definiëren van het inkoopbeleid van uw bedrijf en het instellen van uw inkoopprocessen.
author: SorenGP
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'procurement, supply, vendor order'
ms.search.form: '175, 176, 177, 178, 456, 460, 5727, 5729'
ms.date: 08/30/2022
ms.author: edupont
---
# Inkoop instellen

Voordat u inkoopprocessen kunt gaan beheren, moet u de regels en waarden uit het inkoopbeleid van het bedrijf configureren.

U moet de algemene instellingen definiëren op de pagina **Inkoopinstellingen**, wat meestal één keer wordt gedaan tijdens de eerste implementatie. Lees meer in de volgende sectie, [Inkoopinstellingen](#purchases-and-payables-setup).

Een aparte reeks van taken die verband houdt met het registreren van nieuwe leveranciers is het vastleggen van alle speciale prijzen of kortingsovereenkomsten die u met elke leverancier hebt afgesloten.

Inkoopinstellingen met betrekking tot financiën, zoals betalingswijzen en valuta's, worden behandeld in het gedeelte Instelling van financiën. Zie [Financiën instellen](finance-setup-finance.md) voor meer informatie. Op dezelfde manier zijn voorraadgerelateerde inkoopinstellingen, zoals maateenheden en artikeltraceringscodes, te vinden in de [sectie Voorraadinstelling](inventory-setup-inventory.md).

## Inkoopinstellingen

Voordat u met inkopen gaat werken, specificeert u op de pagina **Inkoopinstellingen** hoe inkoopwaarden worden geboekt en welke nummerreeksen worden gebruikt voor leveranciers en inkoopdocumenten.

### Algemene instellingen

Op het sneltabblad **Algemeen** geeft u aan hoe kortingen moeten worden berekend en geboekt en of factuurbedragen moeten worden afgerond. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

Sommige velden vereisen speciale aandacht, zoals het veld **Factuurk. per btw-ident. berek.**, waarin wordt aangegeven of de factuurkorting wordt berekend op basis van het btw-nummer of het factuurtotaal. Zie [Btw-boekingsgroepen in btw-boekingsinstellingen combineren](finance-setup-vat.md#combine-vat-posting-groups-in-vat-posting-setups) voor meer informatie.

Evenzo kan het veld **Valuta's vereffenen** resulteren in kleine afrondingsverschillen wanneer boekingen in verschillende valuta met elkaar worden vereffend. Zie [Vereffening van posten in verschillende valuta's inschakelen](finance-how-enable-application-ledger-entries-different-currencies.md) voor meer informatie.

Ook veranderen sommige velden hun gedrag of zijn afhankelijk van hoe andere velden zijn ingesteld. Zo wordt bijvoorbeeld de functie **Voortbet. cntr. bij boeken** beïnvloed door hoe het veld **Automatische update van vooruitbetaling** is ingesteld bij het controleren op openstaande vooruitbetalingen.

Lees hieronder details over de velden [**Extern documentnr. verplicht**](#external-document-number) en [**Precieze kostenvereff. verplicht**](#exact-cost-reversing).

### Instellingen voor nummerreeksen

Op het sneltabblad **Nummerreeksen** moet u unieke identificatiecodes opgeven die worden gebruikt voor leveranciers, facturen en andere inkoopdocumenten. Nummering is niet alleen belangrijk voor interne processen, maar moet mogelijk ook voldoen aan lokale regelgeving. Het is dus misschien de moeite waard om te overwegen om alle series vooraf in te stellen op de pagina **Nr.-reeks** in plaats van nieuwe te maken vanuit **Inkoopinstellingen**. Zie [Nummerreeksen maken](ui-create-number-series.md) voor meer informatie.

## Externe documentnummer

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## Precieze kostentegenboeking

De functie **Precieze kostenvereff. verplicht** helpt ervoor te zorgen dat geretourneerde goederen worden gewaardeerd tegen dezelfde kosten als toen ze oorspronkelijk uit de voorraad werden gehaald, met behulp van een vaste vereffening in plaats van een gemiddelde of FIFO-waarderingsmethode (first-in, first-out) te volgen. Lees meer in de sectie [Ontwerpdetails: vaste vereffening](design-details-item-application.md#fixed-application). Als er later aanvullende kosten worden toegevoegd aan de oorspronkelijke inkoop, wordt de waarde van de respectievelijke geretourneerde inkoop bijgewerkt.

Als deze functie is ingeschakeld, kan een retourtransactie alleen worden geboekt door het artikelpostnummer in te voeren in het veld **Vereffeningsnr. artikelpost** op de inkoopretourorderregel. Het veld wordt standaard niet weergegeven op het sneltabblad **Regels**. Leer hoe u velden kunt toevoegen aan pagina's in de sectie [Uw werkruimte personaliseren](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

[!INCLUDE[local-functionality](includes/local-functionality.md)]

## Meer inkoopconfiguraties

| Tot | Zie |
| --- | --- |
| Maak een leverancierskaart voor elke leverancier bij wie u inkoopt. |[Nieuwe leveranciers registreren](purchasing-how-register-new-vendors.md) |
| Bepaal de prioriteit van leveranciers. |[De prioriteit van leveranciers bepalen](purchasing-how-prioritize-vendors.md) |
| Voer bankrekeninggegevens, inclusief IBAN- en SWIFT-codes, in op de kaart van uw leverancier. | [Bankrekeningen van leverancier instellen](purchasing-how-set-up-vendors-bank-accounts.md) |
| Stel inkopers in, wijs leveranciers aan hen toe en codes om statistieken bij te houden. |[Inkopers instellen](purchasing-how-setup-purchasers.md) |
| Voer de verschillende kortingen en speciale prijzen in die leveranciers u verlenen, afhankelijk van artikel, hoeveelheden en/of datum. |[Procedure: afspraken over prijzen, kortingen en betalingen van inkopen vastleggen](purchasing-how-record-purchase-price-discount-payment-agreements.md) |
| Definieer wat u betaalt voor de artikelen en diensten die door uw bedrijf zijn gekocht.  | [Prijzen en kortingen instellen](across-prices-and-discounts.md) |
| Maak standaardregels die moeten worden ingevoegd op periodieke inkoopdocumenten. | [Periodieke inkoopregels instellen](purchasing-how-work-recurring-purchase-lines.md) |
| Maak reeksen van taken om processen die door verschillende gebruikers worden uitgevoerd, met elkaar te verbinden, zoals het aanvragen en goedkeuren van inkooporders. | [Inkoopgoedkeuringswerkstromen instellen](across-set-up-workflows.md) |
| Beheer zakelijke interacties met uw leveranciers, importeer ontvangen factuurdocumenten en registreer nieuwe leveranciers met behulp van de Outlook-e-mailclient. | [De Business Central-invoegtoepassing voor Outlook instellen](admin-outlook.md) |
| Bekijk onkostennota's, converteer papieren en elektronische documenten naar journaalregels en digitaliseer papieren facturen van leveranciers. | [Inkomende documenten instellen](across-how-setup-income-documents.md) |
| Geef standaardrapporten op die voor verschillende documenttypen moeten worden gebruikt. |[Rapportselectie in Business Central](across-report-selections.md)|
|Geef aan of gebruikers inkoopfacturen mogen boeken en of ze deze samen met een zending moeten boeken. |[Definieer een beleid voor het boeken van facturen voor gebruikers](admin-setup-invoice-posting-policy.md)|

## Zie gerelateerde training op [Microsoft Learn](/learn/paths/trade-get-started-dynamics-365-business-central/).

## Zie ook

[Inkoop](purchasing-manage-purchasing.md)  
[Overzicht instellen](setup.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
