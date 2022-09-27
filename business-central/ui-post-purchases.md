---
title: Inkoopdocumenten boeken
description: Meer informatie over de verschillende manieren om inkoopdocumenten te boeken en hoe u geboekte documenten bijwerkt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.form: ''
ms.date: 08/08/2022
ms.author: edupont
ms.openlocfilehash: 1bae22c83f1e7138fbfe16bb39aea3ad9d65d788
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531012"
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

Voor elke inkoopregel worden, indien van toepassing, boekingen gemaakt in de:

* tabel **Artikelpost** als de inkoopregel van het type **Artikel** is.
* tabel **Grootboekpost** als de inkoopregel van het type **Grootboekrekening** is
* tabel **Resourcepost** als de inkoopregel van het type **Resource** is.

Daarnaast worden inkoopdocumenten altijd vastgelegd in de tabellen **Inkoopontvangst** en **Inkoopfactuur**.

Voordat u gaat boeken, kunt u een controlelijst afdrukken met alle informatie uit de inkooporder en eventuele fouten die erin voorkomen. Kies **Boeken** en vervolgens **Testrapport** als u het rapport wilt afdrukken.

> [!IMPORTANT]  
> Tijdens het boeken van een inkooporder voor artikelen kunt u zowel een ontvangst als een factuur maken. Deze kunt u tegelijkertijd, maar ook onafhankelijk van elkaar maken. U kunt ook een gedeeltelijke ontvangst en een gedeeltelijke factuur maken door de velden **Te ontvangen aantal** en **Te factureren aantal** op de afzonderlijke inkooporderregels in te vullen voordat u de boeking uitvoert. Houd er rekening mee dat u geen inkoopfactuur kunt maken van een inkooporder voor producten of diensten die niet zijn ontvangen. Dit betekent dat u pas kunt factureren als er een ontvangst is vastgelegd, of u moet tegelijkertijd ontvangen en factureren.
>
> Als u een inkoopfactuur wilt boeken zonder een inkoopontvangstbewijs vast te leggen in [!INCLUDE[prod_short](includes/prod_short.md)], maakt u het document op de pagina **Inkoopfacturen**. Zie voor meer informatie [Aankopen registreren met inkoopfacturen](purchasing-how-record-purchases.md).

U kunt boeken of boeken en afdrukken. Als u ervoor kiest om te boeken en af te drukken, wordt een lijst afgedrukt nadat de order is geboekt. U kunt ook de actie **Batchboeken** kiezen, waarmee u verschillende orders tegelijkertijd kunt boeken. Zie voor meer informatie [Meerdere documenten tegelijkertijd boeken](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Posten bekijken

Na de boeking worden de geboekte inkoopregels verwijderd uit de order. Er verschijnt een bericht als de boeking is voltooid. Hierna kunt u de geboekte posten bekijken op de verschillende pagina's inclusief de pagina's **Leveranciersposten**, **Grootboekposten**, **Artikelposten**, **Resourceposten**, **Inkoopontvangsten** en **Geboekte inkoopfacturen**.

In de meeste gevallen kunt u posten openen vanaf de betrokken kaart of het betreffende document. Kies bijvoorbeeld op de pagina **Leverancierskaart** de actie **Posten**.

## <a name="editing-ledger-entries"></a>Posten bewerken

U kunt bepaalde velden in geboekte inkoopdocumenten bewerken, zoals het veld **Betalingsreferentie**. Zie voor meer informatie [Geboekte documenten bewerken](across-edit-posted-document.md). Voor kritiekere velden die van invloed zijn op het controlespoor, moet u het boeken omkeren of ongedaan maken. Zie voor meer informatie [Journaalboekingen tegenboeken en ontvangsten/zendingen ongedaan maken](finance-how-reverse-journal-posting.md).

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/receive-invoice-dynamics-d365-business-central/index)

## <a name="see-also"></a>Zie ook

[Geboekte documenten bewerken](across-edit-posted-document.md)  
[Meerdere documenten tegelijkertijd boeken](ui-batch-posting.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Documenten en dagboeken boeken](ui-post-documents-journals.md)  
[Niet-betaalde inkoopfacturen corrigeren of annuleren](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Pagina's en informatie zoeken met Vertel me](ui-search.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
