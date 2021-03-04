---
title: Bankrekeningen beheren| Microsoft Docs
description: U moet regelmatig bankposten reconciliëren met de gerelateerde banktransacties in uw bankrekeningen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reconcile
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7eb749c17ea9f17b3ef7c7c29c5dc9037fcbaf9c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752342"
---
# <a name="reconciling-bank-accounts"></a>Bankrekeningen reconciliëren

Voor al uw bankrekeningen moet op gezette tijden een bankafstemming worden uitgevoerd om ervoor te zorgen dat de kasgegevens van het bedrijf correct zijn. U doet dit door boekingen op uw interne bankrekeningen te vergelijken en af te stemmen met banktransacties bij uw bank en vervolgens de saldi op uw interne bankrekeningen te boeken om totalen beschikbaar te stellen voor financiële managers. Bankafstemming is ook een praktische manier om ontbrekende betalingen en boekhoudfouten te ontdekken en op te lossen.

U kunt de taak uitvoeren op de pagina **Bankreconciliatie**, waar u bankafschriftregels in het linkerdeelvenster afstemt met uw interne bankposten in het rechterdeelvenster. U kunt deze taak ook uitvoeren op de pagina **Betalingsreconciliatiedagboek** als onderdeel van de verwerking van betalingen op een bankafschrift. Op beide pagina's kunt u de bankafschriftinformatie invullen door een bestand of een feed te importeren en kunt u automatische afstemmingsvoorstellen gebruiken.

> [!NOTE]  
> In de Noord-Amerikaanse versies kunt u bankreconciliatie ook uitvoeren op de pagina **Werkblad bankreconciliatie**, dat geschikter is voor cheques en borgsommen, maar geen importeren van bankafschriftbestanden biedt. Als u deze pagina wilt gebruiken in plaats van de pagina **Bankreconciliatie**, schakelt u het veld **Bankreconciliatie met automatische afstemming** uit op de pagina **Boekhoudinstellingen**. Zie voor meer informatie [Bankrekeningen reconciliëren](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) onder Lokale functionaliteit voor de Verenigde Staten.

Voordat u uw bankrekeningen kunt beheren in [!INCLUDE[prod_short](includes/prod_short.md)], moet u elke bankrekening als bankrekeningkaart instellen. Daarnaast moet u elektronische services instellen die u kunt gebruiken voor de import van bankafschriften en de export van het betalingsbestand. Zie [Bankieren instellen](bank-setup-banking.md) voor meer informatie.

De volgende tabel beschrijft een reeks taken, met koppelingen naar de onderwerpen waarin deze worden beschreven.

| Als u dit wilt doen: | Zie |
| --- | --- |
| Bankrekeningen reconciliëren als afzonderlijke taak op de pagina **Bankreconciliatie**. |[Bankrekeningen afstemmen](bank-how-reconcile-bank-accounts-separately.md) |
| Bankrekeningen reconciliëren met betrekking tot betalingsverwerking op de pagina **Betalingsreconciliatiedagboek**. |[Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md) |

> [!TIP]
> Gebruik bankreconciliatie om te controleren of uw boeken up-to-date zijn en boek de reconciliatie pas als u er tevreden mee bent.

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/paths/reconcile-bank-accounts-dynamics-365-business-central/)

## <a name="see-also"></a>Zie ook

[Bankieren instellen](bank-setup-banking.md)  
[Bankrekeningen afstemmen](bank-how-reconcile-bank-accounts-separately.md)  
[Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Bankfondsen overboeken](bank-how-transfer-bank-funds.md)  
[Tegoeden beheren](receivables-manage-receivables.md)  
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]