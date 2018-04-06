---
title: De productiebatcheenheid gebruiken | Microsoft Docs
description: "Als een artikel in één eenheid in voorraad is, maar in een andere eenheid wordt geproduceerd, moet de productieorder gebruikmaken van een productiebatcheenheid voor het berekenen van het juiste aantal onderdelen. Een voorbeeld van een berekening van een productiebatcheenheid is wanneer een geproduceerd artikel als stukgoed in voorraad is maar in tonnen gewicht wordt geproduceerd."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c7c76ce91b58d6cdba09652c54696dc38a87f950
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-manufacturing-batch-units-of-measure"></a>Werken met productiebatcheenheden
Als een artikel in één eenheid in voorraad is, maar in een andere eenheid wordt geproduceerd, kan een productieorder worden gemaakt die gebruikmaakt van een productiebatcheenheid voor het berekenen van het juiste aantal onderdelen tijdens de batchverwerking **Productieorder vernieuwen**. Een voorbeeld van een berekening van een productiebatcheenheid is wanneer een geproduceerd artikel als stukgoed in voorraad is maar in tonnen gewicht wordt geproduceerd.  

## <a name="to-create-a-production-bom-using-a-batch-unit-of-measure"></a>Een productiestuklijst maken met behulp van een batcheenheid  
1.  De productiebatcheenheid wordt ingesteld als alternatieve eenheid in het venster **Artikeleenheden** bij het artikel dat moet worden geproduceerd. De batcheenheid komt niet in de plaats van de basiseenheid van het artikel.  
2.  Maak een productiestuklijst voor het artikel dat is ingesteld met de productiebatcheenheid. Zie voor meer informatie [Productiestuklijsten maken](production-how-to-create-production-boms.md).  
3.  Selecteer de eenheidscode voor de productiebatcheenheid in het veld **Eenheidscode**.  
4.  Voer voor elke productiestuklijstregel in het veld **Aantal per** het aantal van dit onderdeelartikel in dat nodig is om deze batcheenheid te maken.  
5.  Open **Artikel** voor het betreffende artikel.  

    Selecteer op het sneltabblad **Aanvulling** in de groep **Prod.-stuklijstnr.** de hierboven gemaakte productiestuklijst.  
6.  Maak een productieorderkop met het artikel dat is ingesteld met de productiebatcheenheid. Zie voor meer informatie [Productieorders maken](production-how-to-create-production-orders.md).  
7.  Kies de actie **Vernieuwen** en kies vervolgens de knop **OK**.  

Kies op het sneltabblad **Regels** de actie **Regel** en kies vervolgens de actie **Materialen** om het resultaat te bekijken. Het programma berekent het juiste aantal materialen dat nodig is om aan de productiestuklijst te voldoen op basis van de productiebatcheenheid.  

## <a name="to-calculate-a-manufacturing-batch-unit-of-measure-on-a-production-order"></a>Een productiebatcheenheid berekenen in een productieorder  
1.  Maak een productieorderkop met het artikel dat is ingesteld met de productiebatcheenheid.  
2.  Typ in het veld **Artikelnr.** in de productieorderregel hetzelfde artikelnummer dat wordt gebruikt in de kop.  
3.  Voer in het veld **Aantal** hetzelfde aantal in dat wordt gebruikt in de kop.  
4.  Selecteer de eenheidscode voor de productiebatcheenheid in het veld **Eenheidscode**.  
5.  Kies de actie **Vernieuwen**.
6.  Schakel op het sneltabblad **Berekenen** het selectievakje **Regels** uit.  
7.  Kies de knop **OK**.  
8.  Kies op het sneltabblad **Regels** de actie **Regel** en kies vervolgens de actie **Materialen** om het resultaat te bekijken. Het juiste aantal materialen dat nodig is om aan de productiestuklijst te voldoen wordt berekend op basis van de productiebatcheenheid.  

## <a name="see-also"></a>Zie ook  
[Bewerkingsplannen maken](production-how-to-create-routings.md)  
[Productiestuklijsten maken](production-how-to-create-production-boms.md)     
[Productie instellen](production-configure-production-processes.md)  
[Productie](production-manage-manufacturing.md)    
[Gepland](production-planning.md)   
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

