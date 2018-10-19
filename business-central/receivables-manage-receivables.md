---
title: Overzicht van taken om tegoeden te beheren | Microsoft Docs
description: Beschrijft taken om tegoeden te beheren en betalingen te vereffenen met klanten- of leveranciersposten.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f153bd8ff54ed00604ad5ac894b9368575050505
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="managing-receivables"></a>Tegoeden beheren
Een veel voorkomende stap in het financiële ritme is het reconciliëren van bankrekeningen. Hierbij moet u inkomende betalingen vereffenen met klant- of leveranciersposten, om verkoopfacturen en inkoopcreditnota's te sluiten als betaald.

Terwijl de meeste klanten in B2B-omgevingen enige tijd na levering betalen, waarbij de geboekte verkoopfacturen open blijven zodat de afdeling Vorderingen deze kan sluiten (vereffenen) wanneer betaling wordt ontvangen, kunnen sommige verkoopfacturen direct worden betaald, bijvoorbeeld met PayPal. Dergelijke facturen worden direct als betaald vereffend wanneer deze worden geboekt en worden daarom niet weergegeven als betalingen die moeten worden verwerkt in Crediteuren. Zie voor meer informatie bijvoorbeeld [Verkopen factureren](sales-how-invoice-sales.md).  

Een van de snelste manieren om in [!INCLUDE[d365fin](includes/d365fin_md.md)] betalingen vast te leggen in het venster **Dagboek betalingsreconciliatie** is door een bankafschriftbestand of -feed te importeren. Betalingen worden vereffend met openstaande leveranciers- of klantenposten, op basis van overeenkomsten in de gegevens tussen de betalingtekst en de informatie in de posten. U kunt de resultaten controleren en wijzigen voordat u het dagboek boekt en bankrekeningposten voor posten sluiten wanneer u het dagboek boekt. De bankrekening wordt gereconcilieerd wanneer alle betalingen zijn vereffend.

Er zijn andere vensters waarin u betalingen kunt vereffenen of bankrekeningen kunt reconciliëren:

* Het venster **Bankreconciliaties**, waarin u bankrekeningen reconcilieert door geïmporteerde regels van bankrekeningafschriften te koppelen aan uw bankrekeningposten. Hier kunt u ook chequebetalingen reconciliëren. Zie [Bankrekeningen apart reconciliëren](bank-how-reconcile-bank-accounts-separately.md) voor meer informatie. Hier kunt u geen betalingen vereffenen.
* Het venster **Betalingsregistratie**, waar u betalingen handmatig kunt vereffenen die zijn ontvangen als contant, cheque of banktransactie, aan de hand van een gegenereerde lijst met niet-betaalde verkoopdocumenten. Deze functionaliteit is alleen beschikbaar voor verkoopdocumenten. Hier kunt u geen uitgaande betalingen vereffenen en kunt u geen bankrekeningen reconciliëren.
* Het venster **Ontvangstendagboek**, waar u handmatig ontvangsten kunt boeken op de betreffende grootboek- of klantrekening of een andere rekening, door een betalingsregel in te voeren. U kunt de ontvangst of terugbetaling vereffenen met een of meer openstaande posten, voordat u het ontvangstendagboek boekt of via de klantposten. Hier kunt u geen bankrekeningen reconciliëren.  

Een andere taak bij het beheer van tegoeden is het innen van openstaande saldi, inclusief rentefacturen, en het versturen van aanmaningen. [!INCLUDE[d365fin](includes/d365fin_md.md)] biedt ook manieren om deze taken uit te voeren. Zie voor meer informatie [Openstaande saldi innen](receivables-collect-outstanding-balances.md).  

In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.  

| Als u dit wilt doen | Zie |
| --- | --- |
| Vereffen betalingen om klant- of leveranciersposten te openen op basis van een geïmporteerd bankafschriftbestand of een bankfeed en de bankrekening te reconciliëren wanneer alle betalingen zijn vereffend. |[Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Vereffen betalingen met openstaande klantposten op basis van handmatige invoer in een lijst met onbetaalde verkoopdocumenten. |[Klantbetalingen van een lijst met onbetaalde verkoopdocumenten handmatig reconciliëren](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Boek ontvangsten of terugbetalingen voor klanten in het ontvangstendagboek en vereffen deze met klantposten via het dagboek of via geboekte posten. |[Klantbetalingen handmatig reconciliëren](receivables-how-apply-sales-transactions-manually.md) |
| Klanten te herinneren aan achterstallige bedragen, rente en rentefacturen te berekenen en rekeningen met vorderingen te beheren. |[Openstaande saldi innen](receivables-collect-outstanding-balances.md) |
| Voorspellen wanneer betalingen te laat worden gedaan voor verkoopdocumenten. | [De extensie Voorspelling van te late betaling](ui-extensions-late-payment-prediction.md) |
|Blokkeer een klant van worden ingevoerd in documenten of van boeken, bijvoorbeeld vanwege insolventie.|[Klanten blokkeren](receivables-how-block-customers.md)|
|Zorg dat u de kosten van verzonden artikelen kent door toegevoegde artikelkosten op te tellen, zoals vracht, fysieke verwerking, verzekering en transport, die u maakt nadat u hebt verkocht.|[Artikeltoeslagen gebruiken om extra handelskosten te verantwoorden](payables-how-assign-item-charges.md)|
|Stel een tolerantie in waarmee het systeem een factuur sluit hoewel de betaling, inclusief een eventuele korting, het bedrag op de factuur niet volledig dekt.|[Werken met betalingstolerantie en contantkortingstolerantie](finance-payment-tolerance-and-payment-discount-tolerance.md)|
## <a name="see-also"></a>Zie ook
[Verkoop](sales-manage-sales.md)  
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

