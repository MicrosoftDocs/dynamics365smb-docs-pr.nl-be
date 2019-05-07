---
title: Kostenplaatsen en kostenobjecten voor rekeningschema's definiëren | Microsoft Docs
description: In het grootboek kunt u de inkomsten- en onkostenposten automatisch overbrengen naar de kostprijsboekhouding, hetzij voor elke grootboekboeking of met behulp van een batchtaak. Wanneer u de overdracht uitvoert, worden alleen de posten overgebracht die al zijn gekoppeld aan een kostenplaats of een kostenobject. Om tot een zinvolle overdracht te komen, moet u ervoor zorgen dat kostenplaatsen en de kostenobjecten juist zijn gedefinieerd.
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
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: 00c0ac4a37476c2ab21ddc850e80e7abeb5eda18
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "923334"
---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a>Kostenplaatsen en kostenobjecten voor rekeningschema's definiëren
In het grootboek kunt u de inkomsten- en onkostenposten automatisch overbrengen naar de kostprijsboekhouding, hetzij voor elke grootboekboeking of met behulp van een batchtaak. Wanneer u de overdracht uitvoert, worden door [!INCLUDE[d365fin](includes/d365fin_md.md)] alleen de posten overgebracht die al zijn gekoppeld aan een kostenplaats of een kostenobject. Om tot een zinvolle overdracht te komen, moet u ervoor zorgen dat kostenplaatsen en de kostenobjecten juist zijn gedefinieerd.  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a>Standaarddimensiewaarden definiëren voor grootboekrekeningen  
Voor elke grootboekrekening definieert u standaarddimensiewaarden in de tabel **Standaarddimensie**. In het volgende voorbeeld ziet u hoe u kunt definiëren dat er altijd een AFDELING als kostenplaats, maar nooit een PROJECT als kostenobject moet voorkomen bij het boeken naar een grootboekrekening.  

|**Dimensiecode**|**Waardeboeking**|  
|------------------------------------------|-----------------------------------------|  
|Kostenplaats|Verplicht|  
|Kostendrager|Geen|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a>Dimensiewaarden voor overheadkosten en directe kosten definiëren  
 Overheadkosten kunt u overbrengen naar een kostenplaats en directe kosten naar een kostenobject. In de volgende tabel ziet u de optimale combinatie van instelwaarden voor dimensies.  

|Overbrengen naar|Kostenplaatsboeking|Kostenobjectboeking|  
|-----------------|-------------------------|-------------------------|  
|Kostenplaats|Verplicht|Geen|  
|Kostenobject|Geen|Verplicht|  

> [!NOTE]  
>  Zorg ervoor dat de vooraf gedefinieerde kostenplaats en het vooraf gedefinieerde kostenobject die u in het grootboek hebt ingesteld, automatisch naar de kostprijsboekhouding worden overgedragen, door het selectievakje **GB-boekingen controleren** op de pagina Instelling kostprijsboekhouding te selecteren.  

## <a name="see-also"></a>Zie ook  
[Kosten verantwoorden](finance-manage-cost-accounting.md)  
[Kostenboekhouding instellen](finance-set-up-cost-accounting.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
