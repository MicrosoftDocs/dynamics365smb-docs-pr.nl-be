---
title: Betalingsverplichtingen beheren | Microsoft Docs
description: Betalingsverplichtingen beheren
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 92b16c52589a07661d9ff080e9ef8a0f6be633f7
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="managing-payables"></a>Betalingsverplichtingen beheren
Een groot deel van het beheer van uw betalingsverplichtingen is het betalen van uw leveranciers. U kunt functies gebruiken om in het venster **Betalingsdagboek** automatisch betalingsregels toe te voegen voor inkoopfacturen die betaald moeten worden. Als u banktransacties naar uw bank wilt verzenden, kunt u meerdere betalingsdagboekregels naar een bestand exporteren, dat u vervolgens naar uw bank uploadt. U kunt ook betalingen per cheque doen, inclusief deze verzenden als elektronische betalingen.

Een andere veel voorkomende taak is uitgaande betalingen met de relateerde leveranciersposten te vereffenen om daarmee de gerelateerde inkoopfacturen of inkoopcreditnota's te sluiten als zijnde betaald. U kunt dit werk in het venster **Betalingsreconciliatiedagboek** doen door een bankafschriftbestand te importeren om de betalingen te registreren. De betalingen worden vereffend met openstaande leveranciers- of klantenposten, door de betalingtekst te vergelijken met de informatie in de posten. Er zijn verschillende manieren om de overeenkomsten te controleren en te wijzigen voordat u het dagboek boekt. U kunt ervoor kiezen om openstaande bankrekeningposten met betrekking tot de vereffende posten te sluiten wanneer u het dagboek boekt. De bankrekening wordt automatisch gereconcilieerd wanneer alle betalingen worden vereffend.

U kunt ook uitgaande betalingen handmatig vereffenen in het venster **Betalingsdagboek** of vanuit de gerelateerde leveranciersposten.

In de volgende tabel wordt een reeks taken beschreven binnen crediteuren, met koppelingen naar de beschrijvende onderwerpen.

| Als u dit wilt doen | Zie |
| --- | --- |
| Genereer vervallen leveranciersbetalingen in volgorde van prioriteit, volgens betalingskortingen en boetes voor te late betalingen. Exporteer de betalingen desgewenst naar een bankbestand wanneer u boekt. |[Betalingen doen](payables-make-payments.md) |
| Vereffen leveranciersbetalingen automatisch met niet-betaalde inkoopfacturen door een bankafschriftbestand te importeren. |[Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Vereffen leveranciersbetalingen handmatig met niet-betaalde inkoopfacturen. |[Procedure: Leveranciersbetalingen handmatig reconciliëren](payables-how-apply-purchase-transactions-manually.md) |

## <a name="see-also"></a>Zie ook
[Inkoop](purchasing-manage-purchasing.md)  
[Tegoeden beheren](receivables-manage-receivables.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

