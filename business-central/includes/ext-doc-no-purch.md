---
author: brentholtorf
ms.topic: include
ms.date: 03/20/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Op inkoopdocumenten en dagboeken kunt u een documentnummer opgeven dat verwijst naar het nummeringssysteem van de leverancier. Gebruik dit veld om het nummer vast te leggen dat de leverancier aan de order, factuur of creditnota heeft toegewezen. U kunt dit externe documentnummer later gebruiken als u om de een of andere reden de geboekte post moet zoeken met dit nummer.

Het veld **Extern documentnr. verplicht** op de pagina **Inkoopinstellingen** geeft aan of het verplicht is om een extern documentnummer in te voeren in de volgende situaties:

* In het veld **Leveranciersfactuurnr.**, het veld **Ordernr. leverancier** of het veld **Creditnotanr. leverancier** in een inkoopkop

* In het veld **Extern documentnr.** op een dagboekregel, waarbij *Factuur*, *Creditnota* of *Rentefactuur* in het veld **Documentsoort** staat en *Leverancier* in het veld **Rekeningsoort**.

Als u dit veld selecteert, is het niet mogelijk om een factuur, een creditnota of het bovengenoemde soort dagboekregel te boeken zonder een extern documentnummer.

Het externe documentnummer wordt opgenomen in geboekte documenten waar u kunt zoeken op het betreffende nummer. U kunt ook zoeken met behulp van het externe documentnummer wanneer u door leveranciersposten navigeert.

Een andere manier om met externe documentnummers om te gaan is het veld **Uw referentie** te gebruiken. Als u het veld **Uw referentie** gebruikt, wordt het nummer opgenomen in geboekte documenten en kunt u er op dezelfde manier op zoeken als naar waarden van **Extern documentnr.**-velden. Maar het veld is niet beschikbaar op journaalregels.
