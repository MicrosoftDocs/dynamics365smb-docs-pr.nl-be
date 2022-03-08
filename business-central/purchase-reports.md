---
title: Inkooprapporten en analyses
description: Bekijk welke inkooprapporten en analyses beschikbaar zijn in de standaardversie van Business Central, zodat u uw bedrijf kunt volgen.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 3f818e556b2ebe3f50189b0057f1302a5598d904
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543182"
---
# <a name="purchase-reports-and-analytics-in-business-central"></a>Inkooprapporten en analyses in Business Central

Inkooprapportage in [!INCLUDE [prod_short](includes/prod_short.md)] stelt aanschaf- en zakelijke professionals in staat om inzichten en statistieken te krijgen over huidige en vroegere inkoopactiviteiten.  

## <a name="reports"></a>Rapporten

De volgende tabel beschrijft enkele van de belangrijkste rapporten in inkooprapportage.

|Rapport |Object-id|Omschrijving  |
|---------|---------|---------|
|**Inkoopstatistiek**|312|[!INCLUDE [reports-purchase-statistics](includes/reports-purchase-statistics.md)]|
|**Leverancier - Top 10**|311|Hier wordt voor een geselecteerde periode informatie weergegeven over de inkoop bij leveranciers. U kunt het aantal leveranciers opgeven dat u wilt opnemen in de lijst.<br>De leveranciers worden op bedrag gesorteerd en u kunt aangeven of op inkoopbedrag of op saldo moet worden gesorteerd. De lijst biedt u een kort overzicht van de leveranciers waarbij u het meeste inkoopt of de grootste schulden hebt.|
|**Verkoperartikelcatalogus** of **Artikelleverancierscatalogus**|320 of 720|Toont een lijst met leveranciers voor de geselecteerde artikelen of artikelen voor geselecteerde leveranciers. Voor elke combinatie van artikel en leverancier worden de directe kostprijs, de berekening van de doorlooptijd en het artikelnummer van de leverancier weergegeven.<br>In de VS, Canada en Mexico is dit rapport niet beschikbaar. Gebruik in plaats daarvan het rapport **Artikel-/leverancierscatalogus** (10164).|
|**Leverancier-/artikelinkoop**|313|Bevat een overzicht van artikelposten per leverancier in een geselecteerde periode. De lijst bevat informatie over gefactureerde aantallen, bedragen en mogelijke kortingen. U kunt de lijst bijvoorbeeld gebruiken voor een analyse van de artikelen die door het bedrijf zijn ingekocht en om aan te tonen of er een relatie is tussen kortingen en ingekochte artikelen.|
|**Lijst van voorraadkosten en prijzen**|716|Geeft de volgende prijsgegevens voor de geselecteerde artikelen of SKU's weer: directe kostprijs, laatste directe kosten, eenheidsprijs, winstpercentage en winst.|
|**Voorraad - Beschikbaarheid per periode**|707|Als u een overzicht wilt hebben van specifieke artikelen/voorraadeenheden en hun beschikbaarheid. Dit rapport toont u gecumuleerde waarden zoals brutobehoeften, geplande en geplande ontvangsten, de voorraad, enzovoort. |
|**Voorraad - Leveranciersstatistiek**|714|Geeft een lijst met leveranciers weer waarbij uw bedrijf in een geselecteerde periode artikelen heeft ingekocht. De gefactureerde aantallen, bedragen en kortingen worden weergegeven. U kunt de lijst gebruiken voor een analyse van de artikelinkopen van het bedrijf.|
|**Voorraad - Inkooporders**|709|Geeft de lijst met artikelen weer die bij leveranciers zijn besteld. U vindt hier ook de verwachte ontvangstdatum en het aantal en bedrag in backorders. Met de lijst kunt u bijvoorbeeld vaststellen wanneer artikelen moeten worden ontvangen en of een herinnering van een backorder moet worden verzonden|
|**Beschikbaar voor ontvangst**|409|Hier wordt weergegeven welke artikelen op inkoopdocumenten, zoals retourorders voor verzending beschikbaar zijn. U bepaalt of in de lijst de status van een document of van een inkoopregel wordt weergegeven. <br>Wanneer u de lijst afdrukt, kunt u ook het aantal dat voor verzending beschikbaar is, bijwerken in het veld **Te ontvangen aantal** op de inkoopregels. Het veld **Te ontvangen aantal** in inkoopcreditnota's en negatieve inkooporderregels bevat het te verzenden aantal. Vervolgens kunt u de lijst gebruiken om te bepalen welke documenten moeten worden verzonden. **opmerking**: dit rapport is niet beschikbaar voor geavanceerde magazijnfunctionaliteit.|
<!--|**Vervallen posten leverancier**|11006| DACH-specifiek: een rapport dat zowel door de teamleider van uw ingekochte afdeling als de boekhouding kan worden gebruikt. Hier heeft u een overzicht van de onbetaalde leveranciersfacturen inclusief de vervaldata, valuta's en bedragen. Basis zijn de openstaande leveranciersposten.| -->




## <a name="tasks"></a>Taken

In de volgende artikelen worden enkele van de belangrijkste taken beschreven voor het analyseren van de toestand van uw bedrijf:

* [Analyselijsten maken](bi-how-create-analysis-views-reports.md)  
* [Beschikbaarheid van artikelen weergeven](inventory-how-availability-overview.md)  


## <a name="see-also"></a>Zie ook

[Inkopen instellen](purchasing-setup-purchasing.md)  
[Inkoop](purchasing-manage-purchasing.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
