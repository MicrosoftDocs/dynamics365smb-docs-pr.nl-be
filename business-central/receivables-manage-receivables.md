---
title: Overzicht van taken om debiteuren te beheren
description: Dit artikel beschrijft taken om tegoeden te beheren en betalingen te vereffenen met klanten- of leveranciersposten.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'customer payment, debtor, balance due, AR'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# Tegoeden beheren

Een regelmatige stap in elk financieel ritme is het reconciliëren van bankrekeningen. Om verkoopfacturen en inkoopcreditnota's als betaald af te sluiten, vereffent u binnenkomende betalingen met klant- of leveranciersposten.

Terwijl de meeste klanten in B2B-omgevingen enige tijd na levering betalen, waarbij de geboekte verkoopfacturen open blijven zodat de afdeling Vorderingen deze kan sluiten (vereffenen) wanneer betaling wordt ontvangen, kunnen sommige verkoopfacturen direct worden betaald, bijvoorbeeld met PayPal. Dergelijke facturen worden direct als betaald vereffend wanneer deze worden geboekt en worden daarom niet weergegeven als betalingen die moeten worden verwerkt in Crediteuren. Zie voor meer informatie bijvoorbeeld [Verkopen factureren](sales-how-invoice-sales.md).  

Een van de snelste manieren om in [!INCLUDE[prod_short](includes/prod_short.md)] betalingen vast te leggen is met de pagina **Betalingsreconciliatiedagboek** is door een bankafschriftbestand of -feed te importeren. Betalingen worden vereffend met openstaande leveranciers- of klantenposten, op basis van overeenkomsten in de gegevens tussen de betalingtekst en de informatie in de posten. U kunt de resultaten controleren en wijzigen voordat u het dagboek boekt en bankrekeningposten voor posten sluiten wanneer u het dagboek boekt. De bankrekening wordt gereconcilieerd wanneer alle betalingen zijn vereffend.

Er zijn andere pagina's waarin u betalingen kunt vereffenen of bankrekeningen kunt reconciliëren:

* De pagina **Bankreconciliaties**, waarin u bankrekeningen reconcilieert door geïmporteerde regels van bankrekeningafschriften te koppelen aan uw bankrekeningposten. Hier kunt u ook chequebetalingen reconciliëren. Zie [Bankrekeningen reconciliëren](bank-how-reconcile-bank-accounts-separately.md) voor meer informatie. Hier kunt u geen betalingen vereffenen.
* De pagina **Betalingsregistratie**, waar u betalingen handmatig kunt vereffenen die zijn ontvangen als contant, cheque of banktransactie, aan de hand van een gegenereerde lijst met niet-betaalde verkoopdocumenten. Deze functionaliteit is alleen beschikbaar voor verkoopdocumenten. Hier kunt u geen uitgaande betalingen vereffenen en kunt u geen bankrekeningen reconciliëren.
* De pagina **Ontvangstendagboek**, waar u handmatig ontvangsten kunt boeken op de betreffende grootboek- of klantrekening of een andere rekening, door een betalingsregel in te voeren. U kunt de ontvangst of terugbetaling vereffenen met een of meer openstaande posten, voordat u het ontvangstendagboek boekt of via de klantposten. Hier kunt u geen bankrekeningen reconciliëren.

De pagina **Betalingsreconciliatiedagboek** gebruikt automatische overeenkomstlogica die u kunt instellen op de pagina **Regels betalingsvereffening**. Zie [Regels instellen voor automatische vereffening van betalingen](receivables-how-set-up-payment-application-rules.md) voor meer informatie.  

Andere aspecten van het beheer van tegoeden omvatten het innen van openstaande saldi, inclusief rentefacturen en aanmaningen en het instellen van bankrekeningen om toe te staan dat betalingen van klanten automatisch van hun rekening worden afgeschreven.

De volgende tabel beschrijft een reeks taken, met koppelingen naar de artikelen waarin deze worden beschreven.  

| Tot | Zie |
| --- | --- |
| Pas betalingen toe op geopende klant- of leveranciersposten op basis van een geïmporteerd bankafschriftbestand of feed. Reconcilieer de bankrekening nadat u alle betalingen heeft toegepast. |[Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Betalingen vereffenen met open klantenposten op basis van een lijst met onbetaalde verkoopdocumenten op de pagina **Betalingsregistratie**. |[Klantbetalingen uit een lijst met onbetaalde verkoopdocumenten reconciliëren](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Boek ontvangsten of terugbetalingen voor klanten in het ontvangstendagboek en vereffen deze met klantposten via het dagboek of via geboekte posten. |[Klantbetalingen reconciliëren met het ontvangstendagboek of vanuit klantenposten](receivables-how-apply-sales-transactions-manually.md) |
| Klanten te herinneren aan achterstallige bedragen, rente en rentefacturen te berekenen en rekeningen met vorderingen te beheren. |[Openstaande saldi innen](receivables-collect-outstanding-balances.md) |
|Met instemming van de klant, betalingen rechtstreeks vanaf de bankrekening van de klant innen, alleen in de Euro-valuta.|[Betalingen verzamelen via automatische incasso van SEPA](finance-collect-payments-with-sepa-direct-debit.md)|
|Blokkeer een klant van worden ingevoerd in documenten of van boeken, bijvoorbeeld vanwege insolventie.|[Klanten blokkeren](receivables-how-block-customers.md)|
|Stel een tolerantie in waarmee het systeem een factuur sluit hoewel de betaling, inclusief een eventuele korting, het bedrag op de factuur niet volledig dekt.|[Werken met betalingstoleranties en contantkortingstoleranties](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Voorspellen wanneer betalingen te laat worden gedaan voor verkoopdocumenten. | [De extensie Voorspelling van te late betaling](ui-extensions-late-payment-prediction.md) |

## Zie ook

[Verkoop](sales-manage-sales.md)  
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
