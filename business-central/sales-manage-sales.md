---
title: Overzicht van taken om verkoop te beheren
description: 'Lees alles over hoe u de services van Business Central kunt gebruiken voor het beheren van verkoopactiviteiten met uw klanten met verkoopfacturen, bestellingen, offertes en meer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.search.keywords: 'trade, sell'
ms.search.form: '253,'
ms.date: 01/25/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Verkopen

U maakt een verkoopfactuur of een verkooporder om uw overeenkomst met een klant vast te leggen om bepaalde producten tegen bepaalde leverings- en betalingsvoorwaarden te verkopen.

U moet verkooporders gebruiken als uw verkoopproces vereist dat u delen van een orderaantal kunt verzenden, bijvoorbeeld omdat de volledige hoeveelheid niet meteen beschikbaar is. Als u artikelen verkoopt door rechtstreeks van uw leverancier bij de klant te leveren, als een doorverzending, moet u ook verkooporders gebruiken. Wat betreft alle andere aspecten werken verkooporders op dezelfde manier als verkoopfacturen. Bij verkooporders kunt u door middel van de functionaliteit ordertoezegging ook vastgestelde leverdatums aan klanten mededelen.  

U kunt met de klant onderhandelen door eerst een verkoopofferte te maken, die u kunt omzetten in een verkoopfactuur of verkooporder wanneer er een overeenkomst is. Nadat de klant de overeenkomst heeft bevestigd, kunt u een orderbevestiging verzenden om uw verplichting vast te leggen dat de producten worden geleverd zoals is overeengekomen.

U kunt een geboekte verkoopfactuur gemakkelijk corrigeren of annuleren voordat e klant deze betaalt. Bijvoorbeeld als u een typefout wilt corrigeren of als de klant in het begin van het orderproces verzoekt om een wijziging. Als de geboekte verkoopfactuur is betaald, moet u een verkoopcreditnota of een verkoopretourorder maken om de verkoop tegen te boeken.

Goede verkoop- en marketingmethoden zijn gebaseerd op de juiste beslissingen op het juiste tijdstip. Marketingfunctionaliteit in [!INCLUDE[prod_short](includes/prod_short.md)] biedt een nauwkeurig en tijdig overzichten van uw contactgegevens, zodat u uw potentiële klanten efficiënter kunt bedienen en de klanttevredenheid kunt verhogen. Zie voor meer informatie [Relatiebeheer](marketing-relationship-management.md).

Als u Microsoft Dynamics 365 Sales gebruikt voor contacten met klanten, kunt u profiteren van naadloze integratie in het proces van potentiële klant naar inkomsten door [!INCLUDE [prod_short](includes/prod_short.md)] te gebruiken voor backendactiviteiten. Bijvoorbeeld om orders te verwerken, voorraad te beheren en uw financiën te regelen. Zie voor meer informatie [Microsoft Dynamics 365 Sales gebruiken vanuit Business Central](marketing-integrate-dynamicscrm.md)

In bedrijfsomgevingen waar de klant moet betalen voordat producten worden geleverd, zoals in de detailhandel, moet u wachten op de betalingsontvangst voordat u de producten levert. In de meeste gevallen verwerkt u inkomende betalingen enkele weken na levering door de betalingen te vereffenen met de gerelateerde geboekte, niet-betaalde verkoopfacturen. Zie voor meer informatie [Betalingen reconciliëren met automatische vereffening](receivables-how-reconcile-payments-auto-application.md).

Verkoopdocumenten kunnen worden verzonden als PDF-bestanden die aan e-mail zijn gekoppeld. De hoofdtekst van de e-mail bevat een uittreksel van het verkoopdocument, zoals producten, totaalbedrag en een koppeling naar de PayPal-site. Meer informatie op [Documenten per e-mail verzenden](ui-how-send-documents-email.md).

Voor alle verkoopprocessen kunt u een goedkeuringswerkstroom inbouwen. Een goedkeuringswerkstroom kan bijvoorbeeld vereisen dat een manager grote verkopen aan bepaalde klanten goedkeurt. Zie voor meer informatie [Werkstromen gebruiken](across-use-workflows.md).

De volgende secties beschrijven een reeks taken, met koppelingen naar de artikelen waarin deze worden behandeld.

## Aan de slag met verkoopmogelijkheden

Voordat u gaat verkopen, geeft u aan hoe u de verkoopprocessen van uw bedrijf wilt beheren.

|Actie| Zie |
|---|---|
| Maak een klantenkaart voor elke klant aan wie u verkoopt.|[Nieuwe klanten registreren](sales-how-register-new-customers.md) |
| Stel in hoe u verkoopt, zoals prijzen en kortingen, klantprijs- en kortingsgroepen, verkopers, verzendmethoden en agenten. | [Verkopen instellen](sales-setup-sales.md) |

## Verkoopanalyses

In dit gedeelte worden de analytische hulpmiddelen beschreven die u kunt gebruiken om inzicht te krijgen in uw verkoopgegevens.

| Actie | Zie |
| --- | --- |
| Leer meer over de mogelijkheden voor het analyseren van verkoopgegevens. | [Overzicht van verkoopanalyses](sales-analytics-overview.md) |
| Voer ad-hocanalyses uit van verkoopgegevens rechtstreeks op lijstpagina's en query's. | [Rapporten met verkoopanalyses maken](bi-how-create-analysis-views-reports.md) |
| Ingebouwde verkooprapporten verkennen | [Ingebouwde verkooprapporten](sales-reports.md) |

## Van offerte naar order naar verkoopfactuur

In de volgende tabel wordt beschreven hoe u eenvoudige verkoopprocessen kunt gebruiken.

|Actie| Zie |
|---|---|
| Maak een verkoopofferte om producten aan te bieden tegen overeen te komen condities voordat de offerte wordt omgezet in een verkoopfactuur. |[Verkoopoffertes maken](sales-how-make-offers.md) |
| Een verkooporder verwerken (misschien met een gedeeltelijke verzending of met behulp van doorverzending). |[Producten verkopen](sales-how-sell-products.md) |
| Maak een verkoopfactuur om uw overeenstemming met een klant vast te leggen om bepaalde producten tegen bepaalde leverings- en betalingscondities aan hen te verkopen. |[Verkopen factureren](sales-how-invoice-sales.md) |
|Begrijpen wat er gebeurt wanneer u verkoopdocumenten boekt.|[Verkopen boeken](ui-post-sales.md)|

Als u complexere verkoopprocessen nodig heeft, vindt u in de volgende tabel artikelen waarin wordt uitgelegd wat u kunt doen met [!INCLUDE[prod_short](includes/prod_short.md)].

|Actie| Zie |
|---|---|
| Handel een verkooporder af met meerdere deelverzendingen. | [Gedeeltelijke verzendingen verwerken](sales-how-send-partial-shipments.md) |
| Stel standaardverkoop- of inkoopregels in die u snel kunt invoegen in documenten, bijvoorbeeld voor terugkerende aanvullingsorders.|[Periodieke verkoop- en inkoopregels maken](sales-how-work-standard-lines.md)|  
|Beheer de toezegging van de klant om grote aantallen in te kopen, die in de loop van de tijd in meerdere verzendingen worden geleverd.|[Werken met verkoopraamcontracten](sales-how-to-create-blanket-sales-orders.md)|
|Factureer een klant één keer voor meerdere zendingen, door de zendingen te combineren op een factuur.|[Verzendingen combineren op één factuur](sales-how-to-combine-shipments-on-a-single-invoice.md)|
|Verkoop assemblageartikelen die momenteel niet beschikbaar zijn door een gekoppelde assemblageorder te maken. De assemblageorder kan de volledige of gedeeltelijke hoeveelheid van de verkooporder leveren.|[Assembleren voor order-artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md)|

## Picken en verzenden

In de volgende tabel wordt beschreven hoe u artikelen voor een verkooporder pickt en naar de klant verzendt.

| Tot | Zie |
| --- | --- |
|Picken van artikelen voor verzending voorbereiden.|[De picklijst afdrukken](sales-how-print-picking-list.md)|
| Koppel een verkooporder aan een inkooporder om een doorverzendartikel te verkopen dat direct vanaf de leverancier bij de klant wordt geleverd. |[Doorverzendingen uitvoeren](sales-how-drop-shipment.md) |
|Laat een catalogusartikel verzenden van een leverancier naar uw magazijn, zodat u het artikel naar uw klant kunt verzenden.|[Speciale orders maken](sales-how-to-create-special-orders.md)|
|Informeer klanten over orderleverdatums door berekening van ofwel de datum waarop het artikel beschikbaar is voor toezegging (ATP) of de datum waarop het artikel kan worden toegezegd (CTP).|[Ordertoezeggingsdatums berekenen](sales-how-to-calculate-order-promising-dates.md)|
| Leer hoe u een pakket van een geboekte verkoopverzending kunt volgen. | [Pakketten traceren](sales-how-track-packages.md) |

## Geannuleerde orders, terugbetalingen en retourzendingen

In de volgende tabel wordt beschreven hoe u omgaat met geannuleerde orders, terugbetalingen en retourzendingen van goederen.

| Tot | Zie |
| --- | --- |
| Voer een actie op een onbetaalde geboekte verkoopfactuur uit om automatisch een creditnota te maken en de verkoopfactuur te annuleren of opnieuw te maken zodat u correcties kunt aanbrengen. |[Niet-betaalde verkoopfacturen corrigeren of annuleren](sales-how-correct-cancel-sales-invoice.md) |
| Maak een verkoopcreditnota om een bepaalde geboekte verkoopfactuur terug te boeken om de klantretouren en het terugbetalingsbedrag te weerspiegelen. |[Verkoopretouren of annuleringen verwerken](sales-how-process-sales-returns-cancellations.md) |

## Andere processen in verkoop

In de volgende tabel wordt beschreven hoe u met andere verkoopprocessen werkt.

| Tot | Zie |
| --- | --- |
|Los verwarring op wanneer twee of meer records bestaan voor dezelfde klant.|[Dubbele records samenvoegen](sales-how-merge-duplicate-records.md)|

## Zie ook

[Verkopen instellen](sales-setup-sales.md)  
[Nieuwe klanten registreren](sales-how-register-new-customers.md)  
[Overzicht van verkoopanalyses](sales-analytics-overview.md)   
[Tegoeden beheren](receivables-manage-receivables.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
