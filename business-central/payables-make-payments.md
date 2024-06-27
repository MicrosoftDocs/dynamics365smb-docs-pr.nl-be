---
title: Overzicht van taken om betalingen aan leveranciers te beheren
description: 'Schetst taken om betalingen aan leveranciers en schuldeisers te beheren, bijvoorbeeld het boeken van betalingsregels en het ophalen van een overzicht van het verschuldigde saldo.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.search.keywords: 'print check, vendor payment, creditor, debt, balance due, AP'
ms.search.form: '254, 256, 1190, 1191, 1227, 1228, 1229'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Betalingen uitvoeren

U betaalt leveranciers of klanten of betaalt vergoedingen aan uw werknemers door betalingsregels te boeken op de pagina **Betalingsdagboek**. Het betalingsjournaal is een algemeen journaal dat is geoptimaliseerd voor het uitvoeren van betalingen en biedt veel krachtige acties. Bijvoorbeeld de actie **Leveranciersbetalingen voorstellen** die de verschuldigde leveranciersbetalingen vindt, en het rapport **Leverancier - Open posten** met een overzicht van verschuldigde leveranciersbetalingen.  

U kunt het betalingsproces starten vanuit de lijsten, kaarten, en posten voor leveranciers, klanten en medewerkers. Elk van de pagina's heeft een knop die de betalingsstroom start en u helpt het betalingsdagboek in te vullen.  

Vanuit het betalingsdagboek kunt u automatische cheques afdrukken of vastleggen wanneer cheques worden uitgeschreven. Wanneer **Automatische cheque** is geselecteerd in het veld **Betalingssoort**, moet u regels afdrukken die cheques vertegenwoordigen, voordat u het betalingsdagboek kunt boeken.

Nadat u betalingen hebt geboekt, kunt u deze exporteren naar een bankbestand dat u kunt uploaden naar uw bank voor verwerking.

Nadat de betalingen in uw bank worden gemaakt, moet u deze met de relateerde openstaande leveranciers- of werknemersposten vereffenen. U kunt ze handmatig vereffenen of door een bankafschriftbestand te importeren en de betalingen automatisch vereffenen. Zie voor meer informatie [Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md).

De volgende tabel beschrijft een reeks taken, met koppelingen naar de artikelen waarin deze worden beschreven.

| Tot | Zie |
| --- | --- |
|Basisfuncties begrijpen van de pagina **Betalingsdagboek**, die is gebaseerd op het diversendagboek, om het boeken van betalingen naar leveranciers of werknemers voor te bereiden.|[Werken met diversendagboeken](ui-work-general-journals.md)|
|Boek betalingen aan leveranciers of werknemers en terugbetalingen aan klanten en vereffen de betalingen optioneel met de gerelateerde niet-betaalde facturen/creditnota's om deze als betaald te sluiten.|[Betalingen en terugbetalingen vastleggen](payables-how-post-payments-refunds.md)|
| Gebruik een functie op de pagina **Betalingsdagboek** om leveranciersbetalingen voor te stellen volgens geselecteerde criteria, zoals kortingsgeschiktheid, vervaldatum en uw liquiditeit. |[Leveranciersbetalingen voorstellen](payables-how-suggest-vendor-payments.md) |
| Geef cheques uit voor leveranciersbetalingen of terugbetalingen aan klanten, hetzij als afdrukken, hetzij als automatische cheques. Cheques nietig verklaren voor of na het boeken. |[Chequebetalingen doen](payables-how-work-checks.md) |
|Elektronische betalingen doen op basis van de EU-norm voor SEPA-krediettransfers.|[Betalingen doen met de extensie AMC Banking 365 Fundamentals of SEPA-kredietoverdracht](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|
| Een leverancier contant of per cheque betalen en de betaling boeken op het moment dat u de factuur boekt. |[Inkoopfacturen meteen vereffenen](finance-how-to-settle-purchase-invoices-promptly.md) |
| Om ervoor te zorgen dat uw bank alleen gevalideerde cheques en bedragen vrijgeeft, kunt u deze verzenden in een bestand dat gegevens over de leverancier, cheque en betaling bevat. |[Een Positive Pay-bestand exporteren](finance-how-positive-pay.md) |

## Zie ook

[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Tegoeden beheren](receivables-manage-receivables.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
