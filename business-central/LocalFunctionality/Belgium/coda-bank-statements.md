---
title: CODA-bankafschriften
description: CODA (geCOdeerd DAgafschrift) is een nationale bankstandaard, ontworpen door de Belgische Vereniging van Banken, waarmee elektronische bankafschriften automatisch kunnen worden verwerkt.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ceff51934c1c3604328a139b8a4a4aefac6e91fd
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="coda-bank-statements"></a>CODA-bankafschriften
CODA (geCOdeerd DAgafschrift) is een nationale bankstandaard, ontworpen door de Belgische Vereniging van Banken, waarmee elektronische bankafschriften automatisch kunnen worden verwerkt.  

Aan elke soort transactie in een CODA-afschrift wordt een unieke code toegewezen. [!INCLUDE[d365fin](../../includes/d365fin_md.md)] gebruikt deze code om transacties te interpreteren en deze te vereffenen met de betreffende posten.  

## <a name="applying-statement-lines"></a>Afschriftregels vereffenen  
Wanneer u een CODA-afschrift hebt geïmporteerd, kunt u de afschriftregels vereffenen met bestaande posten, op basis van de gegevens in de tabel **Transactiecodering**.  

Als de transactiecodering van de afschriftregel niet wordt gevonden, stopt [!INCLUDE[d365fin](../../includes/d365fin_md.md)] met de verwerking en wordt doorgegaan naar de volgende afschriftregel. Als u het veld **Standaardboeking** selecteert, wordt de afschriftregel als standaardboeking gebruikt.  

Als de transactiecodering van de afschriftregel wordt gevonden, worden de afschriftregels vergeleken met de volgende rekeningsoorten en bijbehorende rekeningnummers:  

- Grootboek: als de rekeningsoort een grootboekrekening is, wordt de afschriftregel geboekt op de bijhorende grootboekrekening.  

- Klant of leverancier: als de rekeningsoort een klant- of leveranciersrekening is, wordt een overeenkomende klant- of leverancierspost gevonden op basis van de volgende criteria:  

    - Als een post met de standaardindeling wordt gevonden, wordt de post vergeleken met de afschriftregel en wordt de vereffeningsstatus ingesteld op **Vereffend**. Als de post niet de standaardindeling gebruikt, wordt het bankrekeningnummer van de klant of leverancier gebruikt om de klant of leverancier te vinden.  

    - Als er geen post met een corresponderend restbedrag wordt gevonden, wordt de klant- of leveranciersrekening gebruikt en wordt de vereffeningsstatus ingesteld op **Gedeeltelijk vereffend**.  

    - Als het bankrekeningnummer wordt gebruikt om de klant of leverancier te zoeken, wordt een bijbehorende post gevonden op basis van het bedrag van de afschriftregel. Als het bedrag wordt gevonden, wordt de afschriftregel vergeleken met de bijbehorende post en wordt de vereffeningsstatus ingesteld op **Vereffend**.  

    - Als het bankrekeningnummer niet kan worden gebruikt om de klant of leverancier te zoeken, wordt in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] gestopt met de verwerking of wordt de huidige regel als standaardboeking gebruikt, voordat wordt doorgegaan met de volgende afschriftregel.  

U kunt het proces zo vaak uitvoeren als u wilt. Alleen afschriftregels met een lege vereffeningsstatus worden vereffend.  

Wanneer u alle afschriftregels hebt vereffend met een grootboekrekening of een bijbehorende klanten- of leverancierspost, kunt u de CODA-afschriftregels boeken. Zie voor meer informatie [CODA-afschriften automatisch overbrengen en boeken](how-to-manually-transfer-and-post-coda-statements.md).  

## <a name="see-also"></a>Zie ook  
 [Elektronisch bankieren voor België](belgian-electronic-banking.md)   
 [Bankrekeningen instellen voor CODA](how-to-set-up-bank-accounts-for-coda.md)   
 [IBLC-BLWI-transactiecodes instellen](how-to-set-up-iblc-blwi-transaction-codes.md)   
 [CODA-afschriften importeren](how-to-import-coda-statements.md)   
 [CODA-afschriften vereffenen](how-to-apply-coda-statements.md)   
 [Financiële dagboeken maken](how-to-create-financial-journals.md)   
 [CODA-afschriften automatisch overbrengen en boeken](how-to-automatically-transfer-and-post-coda-statements.md)   
 [CODA-afschriften handmatig overbrengen en boeken](how-to-manually-transfer-and-post-coda-statements.md)

