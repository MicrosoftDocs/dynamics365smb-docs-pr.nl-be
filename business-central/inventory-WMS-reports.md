---
title: Voorraad- en magazijnrapporten en analyses
description: Bekijk welke voorraad- en magazijnrapporten en analyses beschikbaar zijn in de standaardversie van Business Central, zodat u uw bedrijf kunt volgen.
author: AndreiPanko
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 06/01/2021
ms.author: andreipa
ms.openlocfilehash: 8a4418699f28acd3ede80616ba69c56f50781e43
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216446"
---
# <a name="inventory-and-warehouse-reports-and-analytics-in-business-central"></a>Voorraad- en magazijnrapporten en analyses in Business Central

Voorraad- en magazijnrapportage in [!INCLUDE [prod_short](includes/prod_short.md)] stelt voorraad- en zakelijke professionals in staat om inzichten en statistieken te krijgen over huidige en vroegere voorraad- en magazijnactiviteiten.  

## <a name="reports"></a>Rapporten

De volgende tabel beschrijft enkele van de belangrijkste rapporten in voorraad- en magazijnrapportage.

|Rapport |Object-id|Omschrijving  |
|---------|---------|---------|
|**Voorraad - Beschikbaarheid per periode**|707|Als u een overzicht wilt hebben van specifieke artikelen/voorraadeenheden en hun beschikbaarheid. Dit rapport toont u gecumuleerde waarden zoals brutobehoeften, geplande en geplande ontvangsten, de voorraad, enzovoort. |
|**Voorraadwaardering**|1001|Toont voorraadwaardering van specifieke artikelen in uw voorraad. De lijst bevat tevens informatie over positieve en negatieve voorraadmutaties in de loop van de tijd.|
|**Verloopdatum artikel - Aantal**|5809|Toont een overzicht van de aantallen van geselecteerde artikelen waarvan de vervaldatum in een bepaalde periode valt. Het overzicht bevat het aantal eenheden van het geselecteerde artikel dat binnen een bepaalde tijdspanne vervalt. In het afgedrukte document ziet u van elk artikel dat u in de lijstinstellingen opgeeft het aantal eenheden dat binnen elk van drie perioden met gelijke lengte vervalt en het totale voorraadaantal.<br>U kunt opgeven wat in er in de lijst wordt opgenomen door filters in te stellen. Als u geen filters instelt, bevat de lijst alle records. De aantallen in de lijst hebben alleen betrekking op de artikelaantallen waarvoor vervaldatums zijn gedefinieerd.|
|**Artikelouderdomsanalyse - Aantal** of **Art.-ouderdomsanalyse - Waarde**|5807 of 5808|Toont een overzicht van de huidige ouderdomsanalyse van de geselecteerde artikelen in voorraad. De lijst toont hoeveel eenheden of waarde van het geselecteerde artikel aan de voorraad zijn toegevoegd of uit de voorraad verwijderd, en op welk tijdstip. Artikelen kunnen worden toegevoegd aan of verwijderd uit de voorraad als gevolg van inkopen, verkopen en positieve en negatieve correcties.|
|**Lijst van voorraadkosten en prijzen**|716|Geeft de volgende prijsgegevens voor de geselecteerde artikelen of SKU's weer: directe kostprijs, laatste directe kosten, eenheidsprijs, winstpercentage en winst. |
|**Mag.-opslaglocatieoverzicht**|7319|Toont een overzicht van magazijnopslaglocaties, hun instellingen en het aantal artikelen in de opslaglocaties. Dit rapport kan worden gebruikt voor alle locaties, die 'opslaglocatie' als verplicht veld hebben. |
|**Status van magazijnverzending**|7313|Toont een overzicht per vestiging van geopende brondocumenten met artikelen die zijn verzonden, of die nog moeten worden verzonden. Dit rapport kan gebruikt worden voor alle locaties waar **Verzending vereist** is geselecteerd. **Status van magazijnverzending** toont locaties, opslaglocatiecodes, documentstatus, hoeveelheden.|
|**Voorraad - Picklijst**|813|Geeft een lijst met verkooporders weer waarin een artikel is opgenomen. De volgende gegevens worden voor elk artikel weergegeven: verkooporderregel met naam van de klant, variantcode, vestiging, opslaglocatie, verzenddatum, te verzenden aantal en eenheid. Het te verzenden aantal wordt voor elk artikel opgeteld. U kunt de lijst gebruiken wanneer artikelen uit de voorraad worden verzameld.<br>Opmerking: dit rapport is niet beschikbaar voor geavanceerde magazijnfunctionaliteit.|
|**Mag.-herwaarderingsopslaglocatie**|7320|Dit speciale rapport is alleen bedoeld voor een geavanceerd magazijn en toont de resterende hoeveelheden die nog in de correctieopslaglocatie zelf zijn opgeslagen. Normaal gesproken zou deze specifieke opslaglocatie leeg moeten zijn. De enige reden waarom deze opslaglocatie wordt gevuld, is het resultaat van een fysiek telproces of als er hoeveelheden artikelen zijn verwijderd of toegevoegd aan het magazijn|


## <a name="tasks"></a>Taken

In de volgende artikelen worden enkele van de belangrijkste taken beschreven voor het analyseren van de toestand van uw bedrijf:

* [Analyselijsten maken](bi-how-create-analysis-views-reports.md)  
* [Beschikbaarheid van artikelen weergeven](inventory-how-availability-overview.md)


## <a name="see-also"></a>Zie ook

[Voorraad instellen](inventory-setup-inventory.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Magazijnbeheer](warehouse-manage-warehouse.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
