---
title: 'Procedure: Vaste activa buiten gebruik stellen of afstoten| Microsoft Docs'
description: Beschrijft hoe u een vast activum kunt verkopen of afstoten.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 28e4a67ae3df82a2860ced1b971ee41975c8d578
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-dispose-of-or-retire-fixed-assets"></a>Procedure: Vaste activa buiten gebruik stellen of afstoten
Als u een vast activum verkoopt of anderszins buiten gebruik stelt, moet u de buitengebruikstellingswaarde boeken om de winst of het verlies te berekenen en te registreren. Een buitengebruikstellingspost is de laatste post die voor een vast activum wordt geboekt. Voor vaste activa die gedeeltelijk buiten gebruik zijn gesteld, kunt u meerdere buitengebruikstellingsposten boeken. Het totaal van alle geboekte buitengebruikstellingsbedragen moet een creditbedrag zijn.  

**Opmerking:** als u een vast activum inruilt, moet u zowel de verkoop van het oude activum (buitengebruikstelling) als de aankoop van het nieuwe activum (aanschaf) registreren. Zie [Procedure: Vaste activa aanschaffen](fa-how-acquire.md) voor meer informatie.  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a>Een buitengebruikstelling boeken vanuit het financieel dagboek voor vaste activa
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **VA-financiële dagboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een eerste dagboekregel en vul de velden indien nodig in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. In het veld **VA-boekingssoort** selecteert u **Buitengebruikstelling**.  
4. Kies de actie **VA-tegenrekening invoegen**. Er wordt een tweede dagboekregel gemaakt voor de tegenrekening die voor de boeking van de buitengebruikstelling is ingesteld.  

    **Opmerking:** stap 4 werkt alleen als u het volgende hebt ingesteld: in het venster **VA-boekingsgroep** voor de boekingsgroep van het vaste activum bevat het veld **Buitengebruikstellingsrekening** de grootboekdebetrekening en het veld **Tegenrekening buitengebruikstelling** bevat de grootboekrekening waarnaar u tegenrekeningsposten voor buitengebruikstelling wilt boeken. Zie het gedeelte "Boekingsgroepen voor vaste activa instellen" in de [Procedure: Algemene gegevens voor vaste activa instellen](fa-how-setup-general.md) voor meer informatie.  
5. Kies de actie **Boeken**.  

    Als u een gedeelte van een vast activum verkoopt of het niet langer meer gebruikt, moet u het activum opsplitsen voordat u de buitengebruikstellingstransactie kunt vastleggen. Zie [Procedure to: Vaste activa overbrengen, splitsen of combineren](fa-how-trans-split-combine.md) voor meer informatie.  

## <a name="to-view-disposal-ledger-entries"></a>Buitengebruikstellingsposten bekijken
Als u een vast activum verkoopt of buiten gebruik stelt, moet u de buitengebruikstellingswaarde boeken naar het grootboek waar u het resultaat kunt bekijken.  

1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Vaste activa** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer het vaste activum waarvoor u posten wilt bekijken en kies vervolgens de actie **Afschrijvingsboeken**.  
3. Selecteer het afschrijvingsboek waarvoor u posten wilt bekijken en kies vervolgens de actie **Posten**.  
4. Selecteer een regel die de waarde **Buitengebruikstelling** in het veld **VA-boekingscategorie** bevat en kies vervolgens de actie **Navigeren**.  
5. Selecteer in het venster **Navigeren** de regel van de grootboekpost en klik op de actie **Weergeven**.  

Het **Grootboekposten** wordt geopend. In dit venster kunt u de posten zien waarin de boeking van de buitengebruikstelling is geresulteerd.  

## <a name="see-also"></a>Zie ook
[Vaste activa](fa-manage.md)  
[Vaste activa instellen](fa-setup.md)  
[Financiën](finance.md)  
[Welkom bij [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)](index.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

