---
title: Een inkooporder maken om een aanbod op te vragen | Microsoft Docs
description: Beschrijft hoe u een verkoopaanbieding of een offerteaanvraagdocument maakt om uw aanbod aan een klant vast te leggen om producten onder bepaalde voorwaarden te verkopen.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: bc7bb92185d979871298a3312019e3116fecdab5
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3782938"
---
# <a name="request-quotes"></a>Offertes aanvragen
U kunt een inkoopofferte als conceptversie van de inkooporder gebruiken. De order kan vervolgens in een inkoopfactuur of een order worden omgezet.


## <a name="to-create-a-purchase-quote"></a>Een inkoopofferte maken
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopoffertes** in en kies de gerelateerde koppeling.
2. Maak een nieuw document op dezelfde manier als u een inkooporder maakt. Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a>Een inkoopofferte omzetten in een inkooporder
Wanneer u de leveranciersofferte hebt geaccepteerd, kunt u deze omzetten naar een inkoopfactuur of order om de inkoop te verwerken.

1. Open eeen inkoopofferte die klaar is om te worden geconverteerd en kies de actie **Order maken**.

De inkoopofferte wordt verwijderd uit de database. Een inkoopfactuur of -order wordt gemaakt op basis van de informatie in de inkoopofferte waarin u de inkoop kunt verwerken. Op de inkoopfactuur of inkooporder vermeldt het veld **Offertenr.** het nummer van de inkoopofferte van waaruit het is gemaakt.

## <a name="see-also"></a>Zie ook
[Inkoop](purchasing-manage-purchasing.md)  
[Inkoop instellen](purchasing-setup-purchasing.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
