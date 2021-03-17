---
title: Productie-output en bewerkingstijd in batches boeken | Microsoft Docs
description: Het outputaantal geeft het gereedgemelde aantal van onderhanden werk aan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 83354217bac3b27457303083163cf5eae4494e79
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380468"
---
# <a name="batch-post-output-and-run-times"></a>Output en bewerkingstijden in batches boeken
Het outputaantal geeft het gereedgemelde aantal van onderhanden werk aan.  

> [!NOTE]
> Alleen wanneer u het outputaantal bij de laatste bewerking boekt, wordt de voorraad automatisch bijgewerkt.  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a>Outputaantallen voor een of meer productieorderregels boeken
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Outputdagboek** in en kies de desbetreffende koppeling.  
2. Voer in de velden informatie over de productieorder en output in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Als de bewerking is voltooid, selecteert u het veld **Voltooid**.  

    Als het magazijn waar de artikelen worden opgeslagen opslaglocaties gebruikt, maar geen pickverwerking vereist, kunt u  een opslaglocatie toewijzen aan de dagboekregel om aan te geven waar de artikelen in het magazijn moeten worden geplaatst. Zie [Productie- of assemblageoutput opslaan](warehouse-how-to-put-away-production-output.md) voor meer informatie.  

4. Kies de actie **Boeken** om de bewerkingen te boeken. Het outputaantal wordt geboekt. Het artikel is nu beschikbaar voor verzending.  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a>Bewerkingstijd boeken voor een of meerdere productieorderregels
De bewerkingstijd geeft de benodigde werktijd voor onderhanden werk aan.    

1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Outputdagboek** in en kies de desbetreffende koppeling.  
2. Voer in de velden informatie over de productieorder en output in.  
3.  Als de bewerking is voltooid, selecteert u het veld **Voltooid**.  
4. Kies de actie **Boeken** om de bestede tijd per bewerking te boeken. Capaciteitsposten worden bijgewerkt voor de gebruikte afdelingen of bewerkingsplaatsen.

## <a name="see-also"></a>Zie ook  
[Productie](production-manage-manufacturing.md)    
[Productie instellen](production-configure-production-processes.md)  
[Gepland](production-planning.md)      
[Voorraad](inventory-manage-inventory.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]