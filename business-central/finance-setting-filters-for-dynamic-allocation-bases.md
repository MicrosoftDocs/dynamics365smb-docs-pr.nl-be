---
title: Filters instellen voor dynamische toewijzingsgrondslagen | Microsoft Docs
description: De methode voor dynamische toewijzing is gebaseerd op wijzigbare waarden. Bijvoorbeeld het aantal werknemers in een kostenplaats, of de verkochte artikelen van een kostenobject in een bepaalde periode. Er zijn negen vooraf gedefinieerde toewijzingsgrondslagen en twaalf dynamische periodes. U stelt verschillende filters in op basis van de toewijzingsgrondslag.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: 35f9a542d57bfe27c9a9ee48f4a41af7071cdd47
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "935508"
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
[Kosten definiëren en toewijzen](finance-define-and-allocate-costs.md)
