---
title: "Kosten definiëren en toewijzen | Microsoft Docs"
description: "Tijdens kostenverdelingen worden kosten en opbrengsten verplaatst tussen kostensoorten , kostenplaatsen en kostenobjecten. U kunt zo veel verdelingen definiëren als u nodig hebt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7bdddcadf3fb7dceb762354e8fa527158782b676
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="defining-and-allocating-costs"></a>Kosten definiëren en toewijzen
Tijdens kostenverdelingen worden kosten en opbrengsten verplaatst tussen kostensoorten , kostenplaatsen en kostenobjecten. U kunt zo veel verdelingen definiëren als u nodig hebt. Elke verdeling bestaat uit:  

-   Een toewijzingsbron.  
-   Een of meer verdeeldoelen.  

De verdelingsbron bepaalt welke kosten moeten worden verdeeld en de verdeeldoelen bepalen waaraan de kosten moeten worden toegewezen. Een verdelingsbron kan bijvoorbeeld zijn de kosten voor de kostensoort elektriciteit en verwarming. U kunt alle verwarmings- en elektriciteitskosten aan drie kostenplaatsen toewijzen: Werkplaats, Productie en Verkoop. Deze kostenplaatsen zijn uw verdeeldoelen.  

Voor elke verdelingsbron definieert u een verdelingsniveau, een geldigheidsperiode en een variant als groeperings-id. U kunt met behulp van een batchtaak filters instellen om verdelingsdefinities te selecteren en vervolgens wordt de kostenverdeling automatisch uitgevoerd.  

Voor elk verdeeldoel moet u een verdelingbasis definiëren. De verdelingbasis kan statisch of dynamisch zijn.  

-   Statische toewijzingen zijn gebaseerd op een vaste waarde voor bijvoorbeeld oppervlak of een vastgestelde verdeelsleutel, zoals 5:2:4.  
-   Dynamische toewijzingen zijn afhankelijk van wijzigbare waarden, bijvoorbeeld het aantal werknemers in een kostenplaats of de omzet van een kostenobject gedurende een bepaalde periode.  

In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.

|Aan|Zie|  
|--------|---------|  
|Een verdelingsbron en de doelen ervoor instellen.|[Een verdelingsbron en de doelen ervoor instellen](finance-how-to-set-up-allocation-source-and-targets.md)|  
|Filters instellen voor dynamische toewijzingsgrondslagen.|[Filters instellen voor dynamische toewijzingsgrondslagen](finance-setting-filters-for-dynamic-allocation-bases.md)|  
|Zie een voorbeeld van hoe een statische toewijzing kan worden gedefinieerd.|[Voorbeeld scenario: statische toewijzingen op basis van de verdeelsleutel definiëren](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)|  
|Zie een voorbeeld van hoe een dynamische toewijzing kan worden gedefinieerd.|[Voorbeeld scenario: dynamische toewijzingen op basis van de verkochte artikelen definiëren](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)|  

## <a name="see-also"></a>Zie ook  
 [Kostenboekhouding instellen](finance-set-up-cost-accounting.md)   
 [Kostenposten overbrengen en boeken](finance-transfer-and-post-cost-entries.md)   
 [Kosten verantwoorden](finance-manage-cost-accounting.md)   
 [Terminologie in kostprijsboekhouding](finance-terminology-in-cost-accounting.md)   
 [Kostprijsboekhouding](finance-about-cost-accounting.md)

