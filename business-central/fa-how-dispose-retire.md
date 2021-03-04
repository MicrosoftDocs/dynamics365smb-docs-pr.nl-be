---
title: Activa afstoten of van de hand doen| Microsoft Docs
description: U moet een buitengebruikstellingwaarde boeken wanneer u een vast activum laat uitvallen, verkoopt of buiten gebruik stelt.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 16d052c67a2d9b5513e9dac901dfeddce0527512
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749430"
---
# <a name="dispose-of-or-retire-fixed-assets"></a>Vaste activa afstoten of van de hand doen

Als u een vast activum verkoopt of anderszins buiten gebruik stelt, moet u de buitengebruikstellingswaarde boeken om de winst of het verlies te berekenen en te registreren. Een buitengebruikstellingspost is de laatste post die voor een vast activum wordt geboekt. Voor vaste activa die gedeeltelijk buiten gebruik zijn gesteld, kunt u meerdere buitengebruikstellingsposten boeken. Het totaal van alle geboekte buitengebruikstellingsbedragen moet een creditbedrag zijn.  

> [!NOTE]  
> Als u een vast activum inruilt, moet u zowel de verkoop van het oude activum (buitengebruikstelling) als de aankoop van het nieuwe activum (aanschaf) registreren. Zie [Vaste activa aanschaffen](fa-how-acquire.md) voor meer informatie.  

Bij de volgende stappen wordt ervan uitgegaan dat u de relevante boekingsgroepen al hebt ingesteld op de pagina **FA-boekingsgroepen**. Zie [Boekingsgroepen voor vaste activa instellen](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups) voor meer informatie.  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a>Een buitengebruikstelling boeken vanuit het financieel dagboek voor vaste activa

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **VA fin. dagboeken** in en kies de gerelateerde koppeling.  
2. Maak een eerste dagboekregel en vul de velden indien nodig in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. In het veld **VA-boekingssoort** selecteert u **Buitengebruikstelling**.  
4. Kies de actie **VA-tegenrekening invoegen**. Er wordt een tweede dagboekregel gemaakt voor de tegenrekening die voor de boeking van de buitengebruikstelling is ingesteld.  

    > [!NOTE]  
    >  Stap 4 werkt alleen als u het volgende hebt ingesteld: op de pagina **VA-boekingsgroep** voor de boekingsgroep van het vaste activum bevat het veld **Buitengebruikstellingsrekening** de grootboekdebetrekening en het veld **Tegenrekening buitengebruikstelling** bevat de grootboekrekening waarnaar u tegenrekeningsposten voor buitengebruikstelling wilt boeken. Zie [Boekingsgroepen voor vaste activa instellen](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups) voor meer informatie.  
5. Kies de actie **Boeken**.  

Als u een gedeelte van een vast activum verkoopt of het niet langer meer gebruikt, moet u het activum opsplitsen voordat u de buitengebruikstellingstransactie kunt vastleggen. Zie [Vaste activa overbrengen, splitsen of combineren](fa-how-trans-split-combine.md) voor meer informatie.  

## <a name="to-view-disposal-ledger-entries"></a>Buitengebruikstellingsposten bekijken
Als u een vast activum verkoopt of buiten gebruik stelt, moet u de buitengebruikstellingswaarde boeken naar het grootboek waar u het resultaat kunt bekijken.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vaste activa** in en kies de gerelateerde koppeling.  
2. Selecteer het vaste activum waarvoor u posten wilt bekijken en kies vervolgens de actie **Afschrijvingsboeken**.  
3. Selecteer het afschrijvingsboek waarvoor u posten wilt bekijken en kies vervolgens de actie **Posten**.  
4. Selecteer een regel die de waarde **Buitengebruikstelling** in het veld **VA-boekingscategorie** bevat en kies vervolgens de actie **Posten zoeken**.  
5. Selecteer op de pagina **Posten zoeken** de regel van de grootboekpost en klik op de actie **Verwante posten weergeven**.  

De pagina **Grootboekposten** wordt geopend. Op deze pagina kunt u de posten zien waarin de boeking van de buitengebruikstelling is geresulteerd.  

## <a name="see-also"></a>Zie ook

[Vaste activa](fa-manage.md)  
[Vaste activa instellen](fa-setup.md)  
[Boekingsgroepen voor vaste activa instellen](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
[Financiën](finance.md)  
[Aan de slag](product-get-started.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Posten zoeken](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]