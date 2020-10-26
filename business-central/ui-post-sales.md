---
title: Verkoopdocumenten boeken | Microsoft Docs
description: Meer informatie over de verschillende boekingsfuncties om verkoopdocumenten te boeken en hoe u geboekte documenten kunt bijwerken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5ca69a35aac0ba61591dfdfd71d739726e2fb62f
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3910142"
---
# <a name="posting-sales"></a>Verkopen boeken

In het menu **Boeken** in een verkoopdocument kunt u kiezen uit de volgende boekingsfuncties:

* **Boeken**
* **Boeken en nieuw**
* **Boeken en verzenden**
* **Voorbeeld van boeking weergeven**
* **Conceptfactuur**
* **Pro-formafactuur**
* **Testrapport**

Wanneer u alle regels hebt ingevuld en alle informatie hebt ingevoerd op de verkooporder, kunt u de order boeken. Hiermee worden een verzending en een factuur gemaakt.

Wanneer een verkooporder wordt geboekt, worden de rekening van de klant, het grootboek en de artikelposten bijgewerkt.

Voor elke verkooporder wordt een verkooppost gemaakt in de tabel **Grootboekpost** . Ook wordt er een post in de klantrekening in de tabel **Klantpost** en een grootboekpost wordt in de desbetreffende rekening voor tegoeden gemaakt. Bovendien kan het boeken van de order resulteren in een btw-post en een grootboekpost voor de totale korting. Of er een post voor de korting wordt geboekt hangt af van de inhoud van het veld **Korting boeken** op de pagina **Verkoopinstellingen** .

Voor elke verkooporderregel wordt een artikelpost gemaakt in de tabel **Artikelpost** (als de verkoopregels artikelnummers bevatten) of wordt een grootboekpost gemaakt in de tabel **Grootboekpost** (als de verkoopregels een grootboekrekening bevatten). Daarnaast worden verkooporders altijd geregistreerd in de tabellen **Verkoopverzendkop** en **Verkoopfactuurkop** .

> [!IMPORTANT]  
> Wanneer u een order boekt, kunt u zowel een verzending als een factuur maken. Deze kunnen tegelijk of afzonderlijk worden uitgevoerd. U kunt ook een gedeeltelijke verzending en een gedeeltelijke factuur maken door de velden **Te verzenden aantal** en **Te factureren aantal** op de afzonderlijke verkooporderregels in te vullen voordat u de boeking uitvoert. U kunt geen factuur maken voor iets wat niet is verzonden. U kunt dus pas factureren nadat u een verzending hebt geregistreerd, of u moet ervoor kiezen om tegelijkertijd te verzenden en factureren.

U kunt boeken of boeken en verzenden. Als u ervoor kiest om te boeken en te verzenden, wordt er een pdf-bestand gegenereerd dat u vervolgens kunt verzenden. U kunt ook de functie **Batchboeken** kiezen, waarmee u verschillende orders tegelijkertijd kunt boeken. Zie voor meer informatie [Meerdere documenten tegelijkertijd boeken](ui-batch-posting.md).

## <a name="viewing-ledger-entries"></a>Posten bekijken

Na de boeking worden de geboekte verkoopregels verwijderd uit de order. Er verschijnt een bericht als de boeking is voltooid. Hierna kunt u de geboekte posten bekijken op de verschillende pagina's die geboekte posten bevatten, zoals de pagina's **Klantposten** , **Grootboekposten** , **Artikelposten** , **Geboekte verkoopverzendingen** en **Geboekte verkoopfacturen** .  

In de meeste gevallen kunt u posten openen vanaf de betrokken kaart of het betreffende document. Kies bijvoorbeeld op de pagina **Klantenkaart** de actie **Posten** .

## <a name="editing-ledger-entries"></a>Posten bewerken

U kunt bepaalde velden in geboekte inkoopdocumenten bewerken, zoals het **Traceringsnummer (zending)** . veld. Zie voor meer informatie [Geboekte documenten bewerken](across-edit-posted-document.md). Voor kritiekere velden die van invloed zijn op het controlespoor, moet u het boeken omkeren of ongedaan maken. Zie voor meer informatie [Journaalboekingen tegenboeken en ontvangsten/zendingen ongedaan maken](finance-how-reverse-journal-posting.md).

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/ship-invoice-items-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Verkoop](sales-manage-sales.md)  
[Meerdere documenten tegelijkertijd boeken](ui-batch-posting.md)  
[Geboekte documenten bewerken](across-edit-posted-document.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[Niet-betaalde verkoopfacturen corrigeren of annuleren](sales-how-correct-cancel-sales-invoice.md)  
[Pagina's en informatie zoeken met Vertel me](ui-search.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
