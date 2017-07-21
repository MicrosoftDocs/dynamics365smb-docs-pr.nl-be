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
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: d0b9020596484a8910db2f5720adfe159ad96fe7
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---
# <a name="make-payments"></a>Betalingen doen
Als u betalingen aan leveranciers betaalt, boekt u de relateerde betalingsregels in het venster **Betalingsdagboek**. U kunt de functie **Leveranciersbetalingen voorstellen** gebruiken om betalingen te vinden die moeten worden voldaan. U kunt ook het rapport **Leverancier - Open posten** gebruiken om een overzicht te krijgen van betalingen die moeten worden voldaan.

Vanuit het betalingsdagboek kunt u automatische cheques afdrukken of vastleggen wanneer cheques worden uitgeschreven. Wanneer **Automatische cheque** is geselecteerd in het veld **Betalingssoort**, moeten de cheques worden afgedrukt voordat de dagboekregels kunnen worden geboekt.

Wanneer de betalingen worden geboekt, kunt u deze exporteren naar een bankbestand om ze te uploaden naar uw bank voor verwerking.

Nadat de betalingen in uw bank worden gemaakt, moet u deze met de relateerde openstaande leveranciersposten vereffenen. U kunt dit handmatig doen of door een bankafschriftbestand te importeren en de betalingen automatisch te vereffenen. Zie voor meer informatie [Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md).

In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.

| Als u dit wilt doen | Zie |
| --- | --- |
| Gebruik een functie om leveranciersbetalingen voor te stellen volgens geselecteerde criteria, zoals kortingsgeschiktheid, vervaldatum en uw liquiditeit. |[Procedure: Leveranciersbetalingen voorstellen](payables-how-suggest-vendor-payments.md) |
| Cheques uitgeven voor betalingen, als afdrukken of computercheques. Cheques nietig verklaren voor of na het boeken. |[Procedure: Werken met cheques](payables-how-work-checks.md) |
| Om ervoor te zorgen dat uw bank alleen gevalideerde cheques en bedragen vrijgeeft, kunt u deze verzenden in een bestand dat gegevens over de leverancier, cheque en betaling bevat. |[Procedure: Een Positive Pay-bestand exporteren](finance-how-positive-pay.md) |
|Exporteer betalingen vanuit het venster **Betalingsdagboek** naar een bankbestand dat u uploadt naar uw bank voor verwerking, inclusief EFT (electronic funds transfer) in Noord-Amerika. |[Procedure: Betalingen naar een bankbestand exporteren](payables-how-export-payments-bank-file.md)|  

## <a name="see-also"></a>Zie ook
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Tegoeden beheren](receivables-manage-receivables.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

