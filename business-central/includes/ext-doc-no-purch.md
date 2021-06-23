---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: 59376b96dcd6f755040b07784ceca53e157bcf14
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116054"
---
Op inkoopdocumenten en dagboeken kunt u een documentnummer opgeven dat verwijst naar het nummeringssysteem van de leverancier. Gebruik dit veld om het nummer vast te leggen dat de leverancier aan de order, factuur of creditnota heeft toegewezen. U kunt dit externe documentnummer later gebruiken als u om de een of andere reden de geboekte post moet zoeken met dit nummer.

Het veld **Extern documentnr. verplicht** op de pagina **Inkoopinstellingen** geeft aan of het verplicht is om een extern documentnummer in te voeren in de volgende situaties:

* In het veld **Leveranciersfactuurnr.**, het veld **Ordernr. leverancier** of het veld **Creditnotanr. leverancier** in een inkoopkop

* In het veld **Extern documentnr.** op een dagboekregel, waarbij *Factuur*, *Creditnota* of *Rentefactuur* in het veld **Documentsoort** staat en *Leverancier* in het veld **Rekeningsoort**.

Als u dit veld selecteert, is het niet mogelijk om een factuur, een creditnota of het bovengenoemde soort dagboekregel te boeken zonder een extern documentnummer.

Het externe documentnummer wordt opgenomen in geboekte documenten waar u kunt zoeken op het betreffende nummer. U kunt ook zoeken met behulp van het externe documentnummer wanneer u door leveranciersposten navigeert.

Een andere manier om met externe documentnummers om te gaan is het veld **Uw referentie** te gebruiken. Als u het veld **Uw referentie** gebruikt, wordt het nummer opgenomen in geboekte documenten en kunt u er op dezelfde manier op zoeken als naar waarden van **Extern documentnr.**-velden. Maar het veld is niet beschikbaar op journaalregels.
