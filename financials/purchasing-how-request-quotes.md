---
title: Een inkooporder maken om een aanbod bij uw leverancier op te vragen | Microsoft Docs
description: Beschrijft hoe u een verkoopaanbieding of een offerteaanvraagdocument maakt om uw aanbod aan een klant vast te leggen om producten onder bepaalde voorwaarden te verkopen.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 08/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: fe51ade7a46ab7a8fdf77419a0098ac47fe2e5d1
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-request-quotes"></a>Procedure: Offertes aanvragen
U kunt een inkoopofferte als conceptversie van de inkooporder gebruiken. De order kan vervolgens in een inkoopfactuur of een order worden omgezet.


## <a name="to-create-a-purchase-quote"></a>Een inkoopofferte maken
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Inkoopoffertes** in en klik vervolgens op de gerelateerde koppeling.
2. Maak een nieuw document op dezelfde manier als u een inkooporder maakt. Zie voor meer informatie [Procedure: Inkopen vastleggen](purchasing-how-record-purchases.md).

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a>Een inkoopofferte omzetten in een inkooporder
Wanneer u de leveranciersofferte hebt geaccepteerd, kunt u deze omzetten naar een inkoopfactuur of order om de inkoop te verwerken.

1. Open eeen inkoopofferte die klaar is om te worden geconverteerd en kies de actie **Order maken**.

De inkoopofferte wordt verwijderd uit de database. Een inkoopfactuur of een verkooporder wordt gemaakt op basis van de informatie in de inkoopofferte waarin u de inkoop kunt verwerken. Op de inkoopfactuur of inkooporder vermeldt het veld **Offertenr.** het nummer van de inkoopofferte van waaruit het is gemaakt.

## <a name="see-also"></a>Zie ook
[Inkoop](purchasing-manage-purchasing.md)  
[Inkoop instellen](purchasing-setup-purchasing.md)  
[Procedure: Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

