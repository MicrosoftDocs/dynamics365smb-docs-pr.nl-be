---
title: Overzicht van taken om betalingen aan leveranciers te beheren | Microsoft Docs
description: Schetst taken om betalingen aan leveranciers en schuldeisers te beheren, bijvoorbeeld het boeken van betalingsregels en het ophalen van een overzicht van het verschuldigde saldo.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 04/26/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: db28ad9a4adb45514b1d1287d269d8daefe64865
ms.openlocfilehash: 6b912e8f54fd0e3fb4ac4a1eee3c376c209ffe65
ms.contentlocale: nl-be
ms.lasthandoff: 04/26/2018

---
# <a name="making-payments"></a>Betalingen uitvoeren
Als u betalingen aan leveranciers of vergoedingen aan uw werknemers uitvoert, boekt u de relateerde betalingsregels in het venster **Betalingsdagboek**. U kunt de functie **Leveranciersbetalingen voorstellen** gebruiken om verschuldigde leveranciersbetalingen te vinden. U kunt ook het rapport **Leverancier - Open posten** gebruiken om een overzicht te krijgen van verschuldigde leveranciersbetalingen.

Vanuit het betalingsdagboek kunt u automatische cheques afdrukken of vastleggen wanneer cheques worden uitgeschreven. Wanneer **Automatische cheque** is geselecteerd in het veld **Betalingssoort**, moeten de cheques worden afgedrukt voordat de dagboekregels kunnen worden geboekt.

Wanneer de betalingen worden geboekt, kunt u deze exporteren naar een bankbestand om ze te uploaden naar uw bank voor verwerking.

Nadat de betalingen in uw bank worden gemaakt, moet u deze met de relateerde openstaande leveranciers- of werknemersposten vereffenen. U kunt dit handmatig doen of door een bankafschriftbestand te importeren en de betalingen automatisch te vereffenen. Zie voor meer informatie [Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md).

In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.

| Aan | Zie |
| --- | --- |
|Basisfuncties begrijpen van het venster **Betalingsdagboek**, dat is gebaseerd op het diversendagboek, om het boeken van betalingen naar leveranciers of werknemers voor te bereiden.|[Werken met diversendagboeken](ui-work-general-journals.md)|
|Boek betalingen aan leveranciers en terugbetalingen aan klanten en vereffen de betalingen optioneel met de gerelateerde niet-betaalde facturen/creditnota's om deze als betaald te sluiten.|[Betalingen en terugbetalingen vastleggen](payables-how-post-payments-refunds.md)|
| Gebruik een functie in het venster **Betalingsdagboek** om leveranciersbetalingen voor te stellen volgens geselecteerde criteria, zoals kortingsgeschiktheid, vervaldatum en uw liquiditeit. |[Leveranciersbetalingen voorstellen](payables-how-suggest-vendor-payments.md) |
| Geef cheques uit voor leveranciersbetalingen of terugbetalingen aan klanten, hetzij als afdrukken, hetzij als automatische cheques. Cheques nietig verklaren voor of na het boeken. |[Chequebetalingen doen](payables-how-work-checks.md) |
|Doe elektronische betalingen door betalingen te exporteren naar een bankbestand dat u uploadt naar uw bank voor verwerking, inclusief EFT (Electronic Funds Transfer) in Noord-Amerika. |[Elektronische betalingen doen](payables-how-export-payments-bank-file.md)|
|Doe elektronische betalingen op basis van de EU-norm voor SEPA-krediettransfers.|[Betalingen verrichten met de conversieservice van bankgegevens of SEPA-overmaking](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|
| De leverancier contant of per cheque betalen en de betaling boeken op het moment dat u de factuur boekt. |[Inkoopfacturen meteen vereffenen](finance-how-to-settle-purchase-invoices-promptly.md) |
|Vergoed werknemers voor kosten die zij tijdens zakelijke bezigheden maken door de vergoeding over te maken naar hun bankrekening.|[Kosten van werknemers registreren en terugbetalen](finance-how-record-reimburse-employee-expenses.md)|
| Om ervoor te zorgen dat uw bank alleen gevalideerde cheques en bedragen vrijgeeft, kunt u deze verzenden in een bestand dat gegevens over de leverancier, cheque en betaling bevat. |[Een Positive Pay-bestand exporteren](finance-how-positive-pay.md) |

## <a name="see-also"></a>Zie ook
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Tegoeden beheren](receivables-manage-receivables.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

