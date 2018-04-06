---
title: Overzicht van taken om betalingen aan leveranciers te beheren | Microsoft Docs
description: Schetst taken om betalingen aan leveranciers en schuldeisers te beheren, bijvoorbeeld het boeken van betalingsregels en het ophalen van een overzicht van het verschuldigde saldo.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, vendor payment, creditor, debt, balance due, AP
ms.date: 11/17/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6dfdfce56a06c779881eb0a0f9553d19b6abd1ef
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="making-payments"></a>Betalingen uitvoeren
Als u betalingen aan leveranciers of vergoedingen aan uw werknemers uitvoert, boekt u de relateerde betalingsregels in het venster **Betalingsdagboek**. U kunt de functie **Leveranciersbetalingen voorstellen** gebruiken om verschuldigde leveranciersbetalingen te vinden. U kunt ook het rapport **Leverancier - Open posten** gebruiken om een overzicht te krijgen van verschuldigde leveranciersbetalingen.

Vanuit het betalingsdagboek kunt u automatische cheques afdrukken of vastleggen wanneer cheques worden uitgeschreven. Wanneer **Automatische cheque** is geselecteerd in het veld **Betalingssoort**, moeten de cheques worden afgedrukt voordat de dagboekregels kunnen worden geboekt.

Wanneer de betalingen worden geboekt, kunt u deze exporteren naar een bankbestand om ze te uploaden naar uw bank voor verwerking.

Nadat de betalingen in uw bank worden gemaakt, moet u deze met de relateerde openstaande leveranciers- of werknemersposten vereffenen. U kunt dit handmatig doen of door een bankafschriftbestand te importeren en de betalingen automatisch te vereffenen. Zie voor meer informatie [Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md).

In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.

| Als u dit wilt doen | Zie |
| --- | --- |
|In het venster **Betalingsdagboek**, dat is gebaseerd op van het dagboek, kunt u betalingen aan leveranciers of werknemers boeken.|[Werken met diversendagboeken](ui-work-general-journals.md)|
| Gebruik een functie om leveranciersbetalingen voor te stellen volgens geselecteerde criteria, zoals kortingsgeschiktheid, vervaldatum en uw liquiditeit. |[Leveranciersbetalingen voorstellen](payables-how-suggest-vendor-payments.md) |
|Vergoed werknemers voor kosten die zij tijdens zakelijke bezigheden maken door de vergoeding over te maken naar hun bankrekening.|[Kosten van werknemers registreren en terugbetalen](finance-how-record-reimburse-employee-expenses.md)|
| Geef cheques uit voor leveranciersbetalingen, als afdrukken of computercheques. Cheques nietig verklaren voor of na het boeken. |[Werken met cheques](payables-how-work-checks.md) |
| De leverancier contant of per cheque betalen en de betaling boeken op het moment dat u de factuur boekt. |[Inkoopfacturen meteen vereffenen](finance-how-to-settle-purchase-invoices-promptly.md) |
| Om ervoor te zorgen dat uw bank alleen gevalideerde cheques en bedragen vrijgeeft, kunt u deze verzenden in een bestand dat gegevens over de leverancier, cheque en betaling bevat. |[Een Positive Pay-bestand exporteren](finance-how-positive-pay.md) |
|Exporteer betalingen vanuit het venster **Betalingsdagboek** naar een bankbestand dat u uploadt naar uw bank voor verwerking, inclusief EFT (electronic funds transfer) in Noord-Amerika. |[Betalingen naar een bankbestand exporteren](payables-how-export-payments-bank-file.md)|
|Doe elektronische betalingen op basis van de EU-norm voor SEPA-krediettransfers.|[Betalingen verrichten met de conversieservice van bankgegevens of SEPA-overmaking](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|    

## <a name="see-also"></a>Zie ook
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Tegoeden beheren](receivables-manage-receivables.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

