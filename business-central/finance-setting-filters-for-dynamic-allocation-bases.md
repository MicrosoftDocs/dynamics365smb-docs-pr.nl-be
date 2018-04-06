---
title: Filters instellen voor dynamische toewijzingsgrondslagen | Microsoft Docs
description: De methode voor dynamische toewijzing is gebaseerd op wijzigbare waarden. Bijvoorbeeld het aantal werknemers in een kostenplaats, of de verkochte artikelen van een kostenobject in een bepaalde periode. Er zijn negen vooraf gedefinieerde toewijzingsgrondslagen en twaalf dynamische periodes. U stelt verschillende filters in op basis van de toewijzingsgrondslag.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5ca8e7008c2bfe4a9abeb9d9b7b467a38e2c1971
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="setting-filters-for-dynamic-allocation-bases"></a>Filters instellen voor dynamische toewijzingsgrondslagen
De methode voor dynamische toewijzing is gebaseerd op wijzigbare waarden. Bijvoorbeeld het aantal werknemers in een kostenplaats, of de verkochte artikelen van een kostenobject in een bepaalde periode. Er zijn negen vooraf gedefinieerde toewijzingsgrondslagen en twaalf dynamische periodes. U stelt verschillende filters in op basis van de toewijzingsgrondslag.  

## <a name="setting-filters-for-dynamic-allocation-bases"></a>Filters instellen voor dynamische toewijzingsgrondslagen  
 De volgende tabel laat zien welke filters mogelijk zijn voor de verschillende toewijzingsgrondslagen en welke waarden geldig zijn in de velden **Nr.-filter** en **Groepfilter**. Druk op F1 in het veld **Datumfiltercode** om gedetailleerde omschrijvingen te lezen.  

|**Basis**|**Nr.-filter**|**Datumfiltercode**|**Kostenplaatsfilter**|**Kostenobjectfilter**|**Groepfilter**|  
|--------------|----------------------------------------|----------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------|  
|Grootboekposten|Grootboekrekening|Ja|Ja|Ja|N.v.t.|  
|Grootboekbudgetposten|Grootboekrekening|Ja|Ja|Ja|Budgetnaam|  
|Kostensoortposten|Toeslagsoort|Ja|Ja|Ja|N.v.t.|  
|Kostenbegrotingsposten|Toeslagsoort|Ja|Ja|Ja|Budget|  
|Aantal werknemers|N.v.t.|Ja|Ja|Ja|N.v.t.|  
|Artikelen verkocht (aantal)|Artikelnr.|Ja|Ja|Ja|Voorraadboekingsgroep|  
|Artikelen ingekocht (aantal)|Artikelnr.|Ja|Ja|Ja|Voorraadboekingsgroep|  
|Artikelen verkocht (bedrag)|Artikelnr.|Ja|Ja|Ja|Voorraadboekingsgroep|  
|Artikelen ingekocht (bedrag)|Artikelnr.|Ja|Ja|Ja|Voorraadboekingsgroep|  

## <a name="see-also"></a>Zie ook  
 [Voorbeeldscenario: dynamische toewijzingen op basis van de verkochte artikelen definiëren](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
 [Een verdelingsbron en de doelen ervoor instellen](finance-how-to-set-up-allocation-source-and-targets.md)   
 [Kosten definiëren en toewijzen](finance-define-and-allocate-costs.md)

