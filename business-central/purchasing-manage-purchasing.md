---
title: Overzicht van taken om inkoop te beheren
description: 'Schetst taken om uw inkoop- of verwervingsprocessen te beheren, onder andere hoe inkoopfacturen en inkooporders werken.'
author: brentholtorf
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'procurement, supply, vendor order'
ms.search.form: '460, 9307'
ms.date: 03/21/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Inkopen

U maakt een inkoopfactuur of inkooporder om de kosten van inkopen vast te leggen en leveranciers te volgen. Als u een voorraad moeten controleren, worden inkoopfacturen ook gebruikt om voorraadniveaus dynamisch aan te passen zodat u uw voorraadkosten kunt beperken en betere klantenservice kunt bieden. De inkoopkosten, inclusief servicekosten en voorraadwaarden die resulteren uit boekingsinkoopfacturen, dragen bij aan winstcijfers en andere financiële KPI's in het rolcentrum.

U moet inkooporders gebruiken als uw inkoopproces vereist dat u gedeeltelijke ontvangsten van een orderhoeveelheid registreert, bijvoorbeeld omdat de volledige hoeveelheid niet beschikbaar was bij de leverancier. Als u artikelen verkoopt door rechtstreeks van uw leverancier bij de klant te leveren, als een doorverzending, moet u ook inkooporders gebruiken. Zie [Doorverzendingen maken](sales-how-drop-shipment.md) voor meer informatie. Wat betreft alle andere aspecten werken inkooporders op dezelfde manier als inkoopfacturen.

U kunt inkoopfacturen automatisch laten maken met behulp van de OCR-service (Optical Character Recognition) om PDF-facturen van uw leveranciers te converteren naar elektronische documenten, die vervolgens door een werkstroom naar inkoopfacturen worden geconverteerd. Als u deze functionaliteit wilt gebruiken, moet u zich eerst aanmelden voor de OCR-service en dan verschillende instellingen uitvoeren. Zie [Inkomende documenten gebruiken](across-income-documents.md) voor meer informatie.

Producten kunnen zowel voorraadartikelen als services zijn. Zie voor meer informatie [Nieuwe artikelen registreren](inventory-how-register-new-items.md).

Voor alle inkoopprocessen kunt u een goedkeuringswerkstroom opnemen, bijvoorbeeld om te vereisen dat grote inkopen worden goedgekeurd door de administrateur. Zie voor meer informatie [Goedkeuringswerkstromen gebruiken](across-how-use-approval-workflows.md).

De volgende secties beschrijven een reeks taken, met koppelingen naar de artikelen waarin deze worden behandeld.

## Aan de slag met inkoopmogelijkheden

Voordat u goederen koopt, geeft u aan hoe u de inkoopprocessen van uw bedrijf wilt beheren.

|Actie| Zie |
|---|---|
| De regels en waarden configureren die het inkoopbeleid van uw bedrijf bepalen. | [Inkoop instellen](purchasing-setup-purchasing.md) |
| Elke leverancier van wie u inkoopt, registreren met een leverancierskaart. | [Nieuwe leveranciers registreren.](purchasing-how-register-new-vendors.md) |

## Inkoopanalyses

In dit gedeelte worden de analytische hulpmiddelen beschreven die u kunt gebruiken om inzicht te krijgen in uw inkoopprocessen.

| Actie | Zie |
| --- | --- |
| Leer meer over de mogelijkheden voor het analyseren van inkoopgegevens. | [Overzicht van inkoopanalyses](purchasing-analytics-overview.md) |
| Voer ad-hocanalyses uit van inkoopgegevens rechtstreeks op lijstpagina's en query's. | [Adhoc-analyse van inkoopgegevens](ad-hoc-analysis-purchasing.md) |
| Ingebouwde inkooprapporten verkennen | [Ingebouwde inkooprapporten](purchase-reports.md) |

## Van offerte naar order naar inkoopfactuur

In de volgende tabel wordt beschreven hoe u eenvoudige inkoopprocessen kunt gebruiken.

| Tot | Zie |
| --- | --- |
|Maak een inkoopofferte om een offerteaanvraag van uw leverancier weer te geven, die u later in een inkooporder kunt omzetten.|[Offertes aanvragen](purchasing-how-request-quotes.md)|
| Maak een inkoopfactuur voor alle of voor geselecteerde regels op een verkoopfactuur. |[Artikelen inkopen voor een verkoop](purchasing-how-purchase-products-sale.md) |
| Maak een inkoopfactuur om uw overeenstemming met een leverancier vast te leggen om producten tegen bepaalde leverings- en betalingscondities te kopen. |[Inkopen vastleggen](purchasing-how-record-purchases.md) |
| Leer hoe [!INCLUDE[prod_short](includes/prod_short.md)] berekent wanneer u een artikel moet bestellen, zodat u het op een bepaalde datum ontvangt.|[Datumberekening voor inkopen](purchasing-date-calculation-for-purchases.md)|
|Begrijpen wat er gebeurt wanneer u aankoopdocumenten boekt.|[Inkopen boeken](ui-post-purchases.md)|

Als u complexere inkoopprocessen nodig heeft, vindt u in de volgende tabel artikelen waarin wordt uitgelegd wat u kunt doen met [!INCLUDE[prod_short](includes/prod_short.md)].

| Tot | Zie |
| --- | --- |
| Voer een actie op een onbetaalde, geboekte inkoopfactuur uit om automatisch een creditmemo te maken en de inkoopfactuur te annuleren of opnieuw te maken zodat u correcties kunt aanbrengen. |[Niet-betaalde verkoopfacturen corrigeren of annuleren](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Maak een inkoopcreditnota om een bepaalde geboekte inkoopfactuur terug te boeken om te weerspiegelen welke producten u naar de leverancier terugstuurt en welk betalingsbedrag u zult innen. |[Inkoopretouren of annuleringen verwerken](purchasing-how-process-purchase-returns-cancellations.md) |
|Beheer uw toezegging aan een leverancier om grote hoeveelheden te kopen die in meerdere verzendingen worden geleverd.|[Werken met inkoopraamcontracten](sales-how-to-create-blanket-sales-orders.md)|


## Geannuleerde orders, terugbetalingen en retourzendingen

In de volgende tabel wordt beschreven hoe u omgaat met geannuleerde orders, terugbetalingen en retourzendingen van goederen die u inkoopt.

| Tot | Zie |
| --- | --- |
|Tref voorbereidingen om meerdere ontvangsten van dezelfde leverancier in één keer te factureren, door de ontvangsten in een factuur te combineren.|[Ontvangsten combineren op één factuur](purchasing-how-to-combine-receipts.md)|
|Converteer bijvoorbeeld elektronische facturen van uw leveranciers naar inkoopfacturen in Business Central.|[Elektronische documenten ontvangen en converteren](purchasing-how-to-receive-and-convert-electronic-documents.md)|


## Andere processen in verkoop

In de volgende tabel wordt beschreven hoe u met andere inkoopprocessen werkt.

| Tot | Zie |
| --- | --- |
|Los verwarring op wanneer twee of meer records bestaan voor dezelfde leverancier.|[Dubbele records samenvoegen](sales-how-merge-duplicate-records.md)|


## Externe documentnummers

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## Zie ook

[Inkoop instellen](purchasing-setup-purchasing.md)  
[Nieuwe leveranciers registreren.](purchasing-how-register-new-vendors.md)  
[Overzicht van inkoopanalyses](purchasing-analytics-overview.md)   
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
