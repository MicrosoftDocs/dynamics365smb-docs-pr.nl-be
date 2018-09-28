---
title: Bankrekeningen beheren| Microsoft Docs
description: "U moet regelmatig bankposten reconciliëren met de gerelateerde banktransacties in uw bankrekeningen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: 319faa64adc93c9e54cf792325daeb6a5a8e0b80
ms.contentlocale: nl-be
ms.lasthandoff: 06/28/2018

---
# <a name="managing-bank-accounts"></a>Bankrekeningen beheren
U moet met vaste intervallen uw bankposten reconciliëren in [!INCLUDE[d365fin](includes/d365fin_md.md)] met de gerelateerde banktransacties in bankrekeningen bij uw bank, en vervolgens het saldo boeken naar uw bankrekening. U kunt deze taak uitvoeren als onderdeel van de verwerking van betalingen op een bankafschrift in het **Betalingsreconciliatiedagboek**. U kunt de taak ook apart van de betalingsverwerking uitvoeren in het venster **Bankreconciliatie**, waar u bankafschriftregels in het linkerdeelvenster reconcilieert met uw interne bankposten in het rechterdeelvenster. In beide vensters kunt u de bankafschriftinformatie invullen door een bestand of een feed te importeren en kunt u automatische afstemmingsvoorstellen gebruiken.

> [!NOTE]  
> In Noord-Amerikaanse versies kunt u bankreconciliatie ook uitvoeren in het venster **Werkblad bankreconciliatie**, dat geschikter is voor cheques en borgsommen, maar geen importeren van bankafschriftbestanden biedt. Als u dit venster wilt gebruiken in plaats van het venster **Bankreconciliatie**, schakelt u het veld **Bankreconciliatie met automatische afstemming** uit in het venster **Boekhoudinstellingen**. Zie voor meer informatie het gedeelte "Bankrekeningen reconciliëren" onder Lokale functionaliteit voor de Verenigde Staten.

Soms moet u bedragen overboeken tussen bankrekeningen in [!INCLUDE[d365fin](includes/d365fin_md.md)] om transfers bij uw bank weer te geven. U voert deze taak in het venster **Dagboek** op verschillende manieren uit, afhankelijk van de valuta van de gelden.

Voordat u bankrekeningen kunt beheren, moet u elke bankrekening als bankrekeningkaart instellen. Daarnaast moet u elektronische services instellen die u kunt gebruiken voor de import van bankafschriften en de export van het betalingsbestand. Zie voor meer informatie [Bankrekeningen instellen](bank-setup-banking.md).

In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.

| Als u dit wilt doen | Zie |
| --- | --- |
| Bankrekeningen reconciliëren met betrekking tot betalingsverwerking in het venster **Betalingsreconciliatiedagboek**. |[Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Bankrekeningen reconciliëren, inclusief chequeposten als afzonderlijke taak in het venster **Bankreconciliatie**. |[Bankrekeningen apart reconciliëren](bank-how-reconcile-bank-accounts-separately.md) |
| Transacties boeken tussen bankrekeningen in dezelfde valuta of in verschillende valuta's. |[Bankfondsen overboeken](bank-how-transfer-bank-funds.md) |

## <a name="see-also"></a>Zie ook
[Bankieren instellen](bank-setup-banking.md)  
[Tegoeden beheren](receivables-manage-receivables.md)  
[Betalingsverplichtingen beheren](payables-manage-payables.md)    
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

