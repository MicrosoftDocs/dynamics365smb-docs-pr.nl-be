---
title: Begrijpen hoe u verkoopdocumenten boekt | Microsoft Docs
description: Leren over de verschillende boekingsfuncties om verkoopdocumenten te boeken.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: solsen
ms.openlocfilehash: 7ada688f7946d7f857dc6d4a6518b8bcb4e5c707
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816357"
---
# <a name="posting-sales"></a>Verkopen boeken
In de **Boekingsgroep** op een verkoopdocument kunt u kiezen uit de volgende boekingsfuncties:

* **Boeken**
* **Testrapport**
* **Boeken en verzenden**
* **Boeken en afdrukken**
* **Boeken en e-mailen**
* **Batchboeken**
* **Voorbeeld van boeking weergeven**

Wanneer u alle regels hebt ingevuld en alle informatie hebt ingevoerd op de verkooporder, kunt u de order boeken. Hiermee worden een verzending en een factuur gemaakt.

Wanneer een verkooporder wordt geboekt, worden de rekening van de klant, het grootboek en de artikelposten bijgewerkt.

Voor elke verkooporder wordt een verkooppost gemaakt in de tabel **Grootboekpost**. Ook wordt er een post in de klantrekening in de tabel **Klantpost** en een grootboekpost wordt in de desbetreffende rekening voor tegoeden gemaakt. Bovendien kan het boeken van de order resulteren in een btw-post en een grootboekpost voor de totale korting. Of er een post voor de korting wordt geboekt hangt af van de inhoud van het veld **Korting boeken** op de pagina **Verkoopinstellingen**.

Voor elke verkooporderregel wordt een artikelpost gemaakt in de tabel **Artikelpost** (als de verkoopregels artikelnummers bevatten) of wordt een grootboekpost gemaakt in de tabel **Grootboekpost** (als de verkoopregels een grootboekrekening bevatten). Daarnaast worden verkooporders altijd geregistreerd in de tabellen **Verkoopverzendkop** en **Verkoopfactuurkop**.

> [!IMPORTANT]  
>   Wanneer u een order boekt, kunt u zowel een verzending als een factuur maken. Deze kunnen tegelijk of afzonderlijk worden uitgevoerd. U kunt ook een gedeeltelijke verzending en een gedeeltelijke factuur maken door de velden **Te verzenden aantal** en **Te factureren aantal** op de afzonderlijke verkooporderregels in te vullen voordat u de boeking uitvoert. U kunt geen factuur maken voor iets wat niet is verzonden. U kunt dus pas factureren nadat u een verzending hebt geregistreerd, of u moet ervoor kiezen om tegelijkertijd te verzenden en factureren.

Na de boeking worden de geboekte verkoopregels verwijderd uit de order. Er verschijnt een bericht als de boeking is voltooid. Hierna kunt u de geboekte posten bekijken op de verschillende pagina's die geboekte posten bevatten, zoals de pagina's **Klantposten**, **Grootboekposten**, **Artikelposten**, **Geboekte verkoopverzendingen** en **Geboekte verkoopfacturen**.

## <a name="see-also"></a>Zie ook
[Verkoop](sales-manage-sales.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

