---
title: Begrijpen hoe u inkoopdocumenten boekt | Microsoft Docs
description: Meer informatie over de verschillende boekingsfuncties om inkoopdocumenten te boeken en hoe u geboekte documenten kunt bijwerken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 78657265e45aa9eb01d56a65aab8366c24b3d39a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756754"
---
# <a name="posting-purchases"></a>Inkopen boeken
In een inkoopdocument kunt u kiezen uit de volgende boekingsacties:

* **Boeken**
* **Voorbeeld van boeking weergeven**
* **Boeken en afdrukken**
* **Testrapport**
* **Batchboeken**

Wanneer een inkoopdocument wordt geboekt, worden de rekening van de leverancier, het grootboek, de artikelposten en de resourceposten bijgewerkt.

Voor elk inkoopdocument wordt een inkooppost gemaakt in de tabel **Grootboekpost**. Ook wordt een post in de leveranciersrekening in de tabel **Leverancierspost** gemaakt en wordt er een grootboekpost in de betreffende schuldenrekening gemaakt. Bovendien kan het boeken van de inkoop resulteren in een btw-post en een grootboekpost voor de totale korting. Of er een post voor de korting wordt geboekt, wordt bepaald door de inhoud van het veld **Korting boeken** op de pagina **Inkoopinstellingen**.

Voor elke inkoopregel worden de volgende vermeldingen gemaakt:
- Een vermelding in de tabel **Artikelpost** als de inkoopregel van het type **Artikel** is.
- Een vermelding in de tabel **Grootboekpost** als de inkoopregel van het type **Grootboekrekening** is
- Een vermelding in de tabel **Resourcepost** als de inkoopregel van het type **Resource** is.

Daarnaast worden inkoopdocumenten altijd vastgelegd in de tabellen **Inkoopontvangst** en **Inkoopfactuur**.

Voordat u gaat boeken, kunt u een controlelijst afdrukken met alle informatie uit de inkooporder en eventuele fouten die erin voorkomen. Kies **Boeken** en vervolgens **Testrapport** als u het rapport wilt afdrukken.

> [!IMPORTANT]  
>   Tijdens het boeken van een inkooporder voor artikelen kunt u zowel een ontvangst als een factuur maken. Deze kunt u tegelijkertijd, maar ook onafhankelijk van elkaar maken. U kunt ook een gedeeltelijke ontvangst en een gedeeltelijke factuur maken door de velden **Te ontvangen aantal** en **Te factureren aantal** op de afzonderlijke inkooporderregels in te vullen voordat u de boeking uitvoert. U kunt geen factuur maken voor iets dat niet is ontvangen. Dit betekent dat u pas kunt factureren als er een ontvangst is vastgelegd, of u moet tegelijkertijd ontvangen en factureren.

U kunt boeken of boeken en afdrukken. Als u ervoor kiest om te boeken en af te drukken, wordt een lijst afgedrukt nadat de order is geboekt. U kunt ook de functie **Batchboeken** kiezen, waarmee u verschillende orders tegelijkertijd kunt boeken. Zie voor meer informatie [Meerdere documenten tegelijkertijd boeken](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Posten bekijken
Na de boeking worden de geboekte inkoopregels verwijderd uit de order. Er verschijnt een bericht als de boeking is voltooid. Hierna kunt u de geboekte posten bekijken op de verschillende pagina's die geboekte posten bevatten, zoals de pagina's **Leveranciersposten**, **Grootboekposten**, **Artikelposten**, **Resourceposten**, **Inkoopontvangsten** en **Geboekte inkoopfacturen**.

In de meeste gevallen kunt u posten openen vanaf de betrokken kaart of het betreffende document. Kies bijvoorbeeld op de pagina **Leverancierskaart** de actie **Posten**.

## <a name="editing-ledger-entries"></a>Posten bewerken
U kunt bepaalde velden in geboekte inkoopdocumenten bewerken, zoals het veld **Betalingsreferentie**. Zie voor meer informatie [Geboekte documenten bewerken](across-edit-posted-document.md). Voor kritiekere velden die van invloed zijn op het controlespoor, moet u het boeken omkeren of ongedaan maken. Zie voor meer informatie [Journaalboekingen tegenboeken en ontvangsten/zendingen ongedaan maken](finance-how-reverse-journal-posting.md).

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index)

## <a name="see-also"></a>Zie ook
[Geboekte documenten bewerken](across-edit-posted-document.md)  
[Meerdere documenten tegelijkertijd boeken](ui-batch-posting.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Documenten en dagboeken boeken](ui-post-documents-journals.md)  
[Niet-betaalde inkoopfacturen corrigeren of annuleren](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Pagina's en informatie zoeken met Vertel me](ui-search.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]