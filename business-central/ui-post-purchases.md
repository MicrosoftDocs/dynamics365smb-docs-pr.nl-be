---
title: Begrijpen hoe u inkoopdocumenten boekt | Microsoft Docs
description: Leren over de verschillende boekingsfuncties om inkoopdocumenten te boeken.
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d4d1c86f88acfce861a3330ba5457ce3f80c264c
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="posting-purchases"></a>Inkopen boeken
In de **Boekingsgroep** op een inkoopdocument kunt u kiezen uit de volgende boekingsfuncties:

* **Boeken**
* **Voorbeeld van boeking weergeven**
* **Boeken en afdrukken**
* **Testrapport**
* **Batchboeken**

Wanneer u alle regels hebt ingevuld en alle informatie hebt ingevoerd op de inkooporder, kunt u de order boeken. Dit houdt in dat u een ontvangst en een factuur maakt.

Wanneer een inkooporder wordt geboekt, worden de rekening van de leverancier, het grootboek en de artikelposten bijgewerkt.

Voor elke inkooporder wordt een inkooppost gemaakt in de tabel **Grootboekpost**. Ook wordt een post in de leveranciersrekening in de tabel **Leverancierspost** gemaakt en wordt er een grootboekpost in de betreffende schuldenrekening gemaakt. Bovendien kan het boeken van de order resulteren in een btw-post en een grootboekpost voor de totale korting. Of er een post voor de korting wordt geboekt, wordt bepaald door de inhoud van het veld **Korting boeken** in het venster **Inkoopinstellingen**.

Voor elke inkooporderregel wordt een artikelpost gemaakt in de tabel **Artikelpost** (als op de inkoopregels artikelnummers staan) of een grootboekpost in de tabel **Grootboekpost** (als op de inkoopregels een grootboekrekening staat). Daarnaast worden inkooporders altijd vastgelegd in de tabellen **Inkoopontvangst** en **Inkoopfactuur**.

Voordat u gaat boeken, kunt u een controlelijst afdrukken met alle informatie uit de inkooporder en eventuele fouten die erin voorkomen. Kies **Boeken** en vervolgens **Testrapport** als u het rapport wilt afdrukken.

> [!IMPORTANT]  
>   Tijdens het boeken van een order kunt u zowel een ontvangst als een factuur maken. Deze kunt u tegelijkertijd, maar ook onafhankelijk van elkaar maken. U kunt ook een gedeeltelijke ontvangst en een gedeeltelijke factuur maken door de velden **Te ontvangen aantal** en **Te factureren aantal** op de afzonderlijke inkooporderregels in te vullen voordat u de boeking uitvoert. U kunt geen factuur maken voor iets dat niet is ontvangen. Dit betekent dat u pas kunt factureren als er een ontvangst is vastgelegd, of u moet tegelijkertijd ontvangen en factureren.

U kunt de optie Boeken of Boeken en afdrukken kiezen. Als u ervoor kiest om te boeken en af te drukken, wordt een lijst afgedrukt nadat de order is geboekt. U kunt ook de functie **Batchboeken** kiezen, waarmee u verschillende orders tegelijkertijd kunt boeken.

Na de boeking worden de geboekte inkoopregels verwijderd uit de order. Er verschijnt een bericht als de boeking is voltooid. Hierna kunt u de geboekte posten bekijken in de verschillende vensters die geboekte posten bevatten, zoals de vensters **Leveranciersposten**, **Grootboekposten**, **Artikelposten**, **Geboekte inkoopontvangsten** en **Geboekte inkoopfacturen**.

## <a name="see-also"></a>Zie ook
[Inkoop](purchasing-manage-purchasing.md)  
[Documenten en dagboeken boeken](ui-post-documents-journals.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


