---
title: 'Procedure: een verdelingsbron en verdeeldoelen instellen | Microsoft Docs'
description: Elke toewijzing bestaat uit een verdelingsbron en een of meer verdeeldoelen. De verdelingsbron definieert welke kosten worden toegerekend. De verdeeldoelen bepalen waaraan de kosten worden toegerekend.
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
ms.openlocfilehash: d57669191209090f15a424537d98d106db681a38
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-allocation-source-and-targets"></a>Een verdelingsbron en de doelen ervoor instellen
Elke toewijzing bestaat uit een verdelingsbron en een of meer verdeeldoelen. De verdelingsbron definieert welke kosten worden toegerekend. De verdeeldoelen bepalen waaraan de kosten worden toegerekend.  

## <a name="to-set-up-cost-allocations"></a>Kostenverdeling instellen  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Kostenverdeling** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies in het venster **Kostenverdeling** de actie **Bewerken**.  
3.  Geef een id voor de verdelingsbron op in het veld **ID**.  
4.  Definieer een niveau als een getal tussen 1 en 99 in het veld **Niveau**. De verdelingsboeking volgt de volgorde van de niveaus.  
5.  Voer een kostensoort in om te bepalen welke typen kosten worden toegerekend in het veld **Kostensoortbereik**. Als alle kosten voor een kostensoort worden toegerekend, wordt geen bereik gedefinieerd.  
6.  Voer een kostenplaats met kosten in om toe te wijzen in het veld **Kostenplaatscode**.  
7.  Voer een kostenobject met kosten in om toe te wijzen in het veld **Kostenobjectcode**. In de meeste gevallen blijft dit veld leeg, omdat kostenobjecten zelden worden toegewezen aan andere kostenobjecten.  
8.  Voer een kostensoort in het veld **Credit naar kostensoort** in. De kosten die zijn toegewezen worden gecrediteerd aan de bronkostensoort. De creditboeking wordt geboekt naar de hier opgegeven kostensoort.  
9. Definieer de toewijzingsdoelen op het sneltabblad **Regels**. Voer op de eerste regel een kostensoort in het veld **Doelkostensoort** in. Hiermee wordt gedefinieerd van welke kostensoort de toerekening wordt gedebiteerd.  
10. Voer op de eerste regel het eerste toewijzingsdoel in het veld **Doelkostenplaats** **Doelkostenobject** in. Deze twee velden definiëren van welke kostenplaats of kostenobject de toewijzing wordt gedebiteerd. U kunt slechts een van deze velden invullen, maar niet beide.  
11. Herhaal de dezelfde stappen op de tweede regel om extra verdeeldoelen in te stellen.  
12. Nadat u het verdeeldoel en de verdelingsbronnen hebt ingesteld, kiest u de actie **Verdeelsleutel berekenen** om de totaalwaarden van de aandelen te berekenen.  

> [!NOTE]  
>  Selecteer het selectievakje **Geblokkeerd** om de toewijzingsinstelling te deactiveren.  

## <a name="see-also"></a>Zie ook  
[Kosten verantwoorden](finance-manage-cost-accounting.md)  
 [Filters instellen voor dynamische toewijzingsgrondslagen](finance-setting-filters-for-dynamic-allocation-bases.md)   
 [Voorbeeld scenario: statische toewijzingen op basis van de verdeelsleutel definiëren](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)   
 [Voorbeeld scenario: dynamische toewijzingen op basis van de verkochte artikelen definiëren](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
 [Kosten definiëren en toewijzen](finance-define-and-allocate-costs.md)   
 [Terminologie in kostprijsboekhouding](finance-terminology-in-cost-accounting.md)  
 [Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

