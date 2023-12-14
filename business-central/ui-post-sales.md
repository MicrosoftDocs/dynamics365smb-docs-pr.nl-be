---
title: Verkoopdocumenten boeken
description: Meer informatie over de verschillende boekingsfuncties om verkoopdocumenten te boeken en hoe u geboekte documenten kunt bijwerken.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: bholtorf
ms.search.form: '130, 142, 1350'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Verkopen boeken

In het menu **Boeken** in een verkoopdocument kunt u kiezen uit de volgende boekingsfuncties:

* **Boeken**
* **Boeken en nieuw**
* **Boeken en verzenden**
* **Voorbeeld van boeking weergeven**
* **Batchboeken**
* **Testrapport**

> [!NOTE]
> Voor verkooporders kunt u ook opties zien met betrekking tot de vooruitbetalingsfunctionaliteit. Zie voor meer informatie [Vooruitbetalingen factureren](finance-invoice-prepayments.md).

Wanneer u alle regels hebt ingevuld en alle informatie hebt ingevoerd op de verkooporder, kunt u de order boeken. Hiermee worden een verzending en een factuur gemaakt.

Wanneer een verkooporder wordt geboekt, worden de rekening van de klant, het grootboek en de artikelposten bijgewerkt.

Voor elke verkooporder wordt een verkooppost gemaakt in de tabel **Grootboekpost**. Ook wordt er een post in de klantrekening in de tabel **Klantpost** en een grootboekpost wordt in de desbetreffende rekening voor tegoeden gemaakt. Bovendien kan het boeken van de order resulteren in een btw-post en een grootboekpost voor de totale korting. Of er een post voor de korting wordt geboekt hangt af van de inhoud van het veld **Korting boeken** op de pagina **Verkoopinstellingen**.

Voor elke verkooporderregel wordt een artikelpost gemaakt in de tabel **Artikelpost** (als de verkoopregels artikelnummers bevatten) of wordt een grootboekpost gemaakt in de tabel **Grootboekpost** (als de verkoopregels een grootboekrekening bevatten). Daarnaast worden verkooporders altijd geregistreerd in de tabellen **Verkoopverzendkop** en **Verkoopfactuurkop**.

[!INCLUDE [order-ship-invoice](includes/order-ship-invoice.md)]

U kunt boeken of boeken en verzenden. Als u ervoor kiest om te boeken en te verzenden, wordt er een pdf-bestand gegenereerd dat u vervolgens kunt verzenden. U kunt ook de functie **Batchboeken** kiezen, waarmee u verschillende orders tegelijkertijd kunt boeken. Zie voor meer informatie [Meerdere documenten tegelijkertijd boeken](ui-batch-posting.md).

## Posten bekijken

Na de boeking worden de geboekte verkoopregels verwijderd uit de order. Er verschijnt een bericht als de boeking is voltooid. Hierna kunt u de geboekte posten bekijken op de verschillende pagina's die geboekte posten bevatten, zoals de pagina's **Klantposten**, **Grootboekposten**, **Artikelposten**, **Geboekte verkoopverzendingen** en **Geboekte verkoopfacturen**.  

In de meeste gevallen kunt u posten openen vanaf de betrokken kaart of het betreffende document. Kies bijvoorbeeld op de pagina **Klantenkaart** de actie **Posten**.

## Posten bewerken

U kunt bepaalde velden in geboekte inkoopdocumenten bewerken, zoals het **Traceringsnummer (zending)**. veld. Zie voor meer informatie [Geboekte documenten bewerken](across-edit-posted-document.md). Voor kritiekere velden die van invloed zijn op het controlespoor, moet u het boeken omkeren of ongedaan maken. Zie voor meer informatie [Journaalboekingen tegenboeken en ontvangsten/zendingen ongedaan maken](finance-how-reverse-journal-posting.md).

## Zie ook

[Verkoop](sales-manage-sales.md)  
[Meerdere documenten tegelijkertijd boeken](ui-batch-posting.md)  
[Geboekte documenten bewerken](across-edit-posted-document.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[Niet-betaalde verkoopfacturen corrigeren of annuleren](sales-how-correct-cancel-sales-invoice.md)  
[Pagina's en informatie zoeken met Vertel me](ui-search.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]  
