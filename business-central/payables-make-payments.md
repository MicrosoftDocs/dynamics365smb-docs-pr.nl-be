---
title: Overzicht van taken om betalingen aan leveranciers te beheren | Microsoft Docs
description: Schetst taken om betalingen aan leveranciers en schuldeisers te beheren, bijvoorbeeld het boeken van betalingsregels en het ophalen van een overzicht van het verschuldigde saldo.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 99da82d54a2e769c2ebbaf7d4c103791119517d9
ms.sourcegitcommit: d0dc5e5c46b932899e2a9c7183959d0ff37738d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076474"
---
# <a name="making-payments"></a>Betalingen uitvoeren

Als u betalingen aan leveranciers of klanten doet of vergoedingen aan uw werknemers uitvoert, boekt u de gerelateerde betalingsregels op de pagina **Betalingsdagboek**. Het betalingsdagboek is een diversendagboek dat is geoptimaliseerd voor het doen van betalingen en bevat een aantal krachtige functies zoals de functie **Leveranciersbetalingen voorstellen**, die verschuldigde betalingen zoekt, en het rapport **Leverancier - Open posten** dat een overzicht bevat van verschuldigde leveranciersbetalingen.  

U kunt het betalingsproces starten vanuit de lijsten, kaarten, en posten voor leveranciers, klanten en medewerkers. Elk van de pagina's heeft een knop die de betalingsstroom start en u helpt het betalingsdagboek in te vullen.  

Vanuit het betalingsdagboek kunt u automatische cheques afdrukken of vastleggen wanneer cheques worden uitgeschreven. Wanneer **Automatische cheque** is geselecteerd in het veld **Betalingssoort**, moeten de cheques worden afgedrukt voordat de dagboekregels kunnen worden geboekt.

Wanneer de betalingen worden geboekt, kunt u deze exporteren naar een bankbestand om ze te uploaden naar uw bank voor verwerking.

Nadat de betalingen in uw bank worden gemaakt, moet u deze met de relateerde openstaande leveranciers- of werknemersposten vereffenen. U kunt dit handmatig doen of door een bankafschriftbestand te importeren en de betalingen automatisch te vereffenen. Zie voor meer informatie [Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md).

In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.

| Aan | Zie |
| --- | --- |
|Basisfuncties begrijpen van de pagina **Betalingsdagboek**, die is gebaseerd op het diversendagboek, om het boeken van betalingen naar leveranciers of werknemers voor te bereiden.|[Werken met diversendagboeken](ui-work-general-journals.md)|
|Boek betalingen aan leveranciers of werknemers en terugbetalingen aan klanten en vereffen de betalingen optioneel met de gerelateerde niet-betaalde facturen/creditnota's om deze als betaald te sluiten.|[Betalingen en terugbetalingen vastleggen](payables-how-post-payments-refunds.md)|
| Gebruik een functie op de pagina **Betalingsdagboek** om leveranciersbetalingen voor te stellen volgens geselecteerde criteria, zoals kortingsgeschiktheid, vervaldatum en uw liquiditeit. |[Leveranciersbetalingen voorstellen](payables-how-suggest-vendor-payments.md) |
| Geef cheques uit voor leveranciersbetalingen of terugbetalingen aan klanten, hetzij als afdrukken, hetzij als automatische cheques. Cheques nietig verklaren voor of na het boeken. |[Chequebetalingen doen](payables-how-work-checks.md) |
|Doe elektronische betalingen op basis van de EU-norm voor SEPA-krediettransfers.|[Betalingen doen met de AMC Banking 365 Fundamentals-extensie of SEPA-kredietoverdracht](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|
| Een leverancier contant of per cheque betalen en de betaling boeken op het moment dat u de factuur boekt. |[Inkoopfacturen meteen vereffenen](finance-how-to-settle-purchase-invoices-promptly.md) |
| Om ervoor te zorgen dat uw bank alleen gevalideerde cheques en bedragen vrijgeeft, kunt u deze verzenden in een bestand dat gegevens over de leverancier, cheque en betaling bevat. |[Een Positive Pay-bestand exporteren](finance-how-positive-pay.md) |

## <a name="see-also"></a>Zie ook
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Tegoeden beheren](receivables-manage-receivables.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
