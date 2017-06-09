---
title: 'Procedure: vaste activa verplaatsen, splitsen of combineren| Microsoft Docs'
description: Beschrijft hoe u een vast activum kunt herindelen om het te verplaatsen, te splitsen of te combineren met andere vaste activa.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 09/29/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 50e1a8d7012394b4b3f710991f7d45ae244656c9
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-transfer-split-or-combine-fixed-assets"></a>Procedure: Vaste activa verplaatsen, splitsen of combineren.
U gebruikt het herindelingsdagboek voor vaste activa voor het verplaatsen, combineren en splitsen van vaste activa. U bekijkt de resultaten van de herindeling van vaste activa of drukt deze af met het rapport **Vast activum - Boekwaarde 02**.

## <a name="to-transfer-a-fixed-asset-to-a-different-department"></a>Een vast activum naar een andere afdeling verplaatsen
Mogelijk moet u een vast activum verplaatsen naar een andere afdeling wanneer u bijvoorbeeld een activum in de productieafdeling plaatst zolang het niet af is en het vervolgens verplaatst naar de administratieafdeling wanneer het klaar is.  

1. Stel een nieuw vast activum in. Voer de nieuwe afdeling in het veld **Kostenplaats** in.
2. Wijs een afschrijvingsboek voor vaste activa aan het nieuwe vaste activum toe. Zie [Procedure: Vaste activa aanschaffen](fa-how-acquire.md) voor meer informatie.
3. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **VA-herindelingsdagboeken** in en kies vervolgens de gerelateerde koppeling.
4. Een herindelingsdagboek maken waarin het veld **VA-nr.** het oorspronkelijke vaste activum bevat en het veld **Nieuw VA-nr.** het nieuwe vaste activum bevat dat moet worden verplaatst.  
5. Kies de actie **Herindelen**.

    Er worden nu twee regels gemaakt in het financieel dagboek voor vaste activa met behulp van de sjabloon en batch die u hebt opgegeven in het venster **VA-dagboekinstellingen** voor het opgegeven afschrijvingsboek. Zie [Procedure: Afschrijving voor vaste activa instellen](fa-how-setup-depreciation.md) voor meer informatie.
6. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **VA-financiële dagboeken** in en kies vervolgens de gerelateerde koppeling.    
7. Kies in het venster **Financieel dagboek voor vaste activa** de actie **Boeken** om de herindeling te boeken die u in stap 4 en 5 hebt uitgevoerd.

Als u aanschafkosten voor één activum hebt geboekt, kunt u het herindelingsdagboek voor vaste activa gebruiken om de aanschafkosten over meerdere activa te verdelen.  

## <a name="to-split-a-fixed-asset-into-three-fixed-assets"></a>Een vast activum in drie vaste activa splitsen
U kunt één vast activum in meerdere vaste activa splitsen, bijvoorbeeld als u een vast activum moet verdelen in drie verschillende afdelingen. In dat geval kunt u bijvoorbeeld 25 procent van de aanschafkosten en afschrijving voor het oorspronkelijke vaste activum naar het tweede vaste activum verplaatsen, en 45 procent naar het derde activum. De resterende 30 procent blijft in het oorspronkelijke vaste activum.

1. Twee nieuwe vaste activa instellen Voer de nieuwe afdeling in het veld **Kostenplaats** in.
2. Wijs afschrijvingsboeken voor vaste activa aan de nieuwe vaste activa toe. Zie [Procedure: Vaste activa aanschaffen](fa-how-acquire.md) voor meer informatie.
3. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **VA-herindelingsdagboeken** in en kies vervolgens de gerelateerde koppeling.
4. Maak twee herindelingsdagboekregels, één voor elk nieuw vast activum.
5. Voer op de eerste regel het tweede vaste activum in het veld **Nieuw VA-nr.** in en 25 in het veld **Herindeling aanschafkosten-%**.
6. Voer op de tweede regel het derde vaste activum in het veld **Nieuw VA-nr.** in en 40 in het veld **Herindeling aanschafkosten-%**.
7. Schakel op beide regels de selectievakjes **Herindeling aanschafkosten** en **Herindeling afschrijving** in.   
8. Kies de actie **Herindelen**.

    Er worden nu twee regels gemaakt in het financieel dagboek voor vaste activa met behulp van de sjabloon en batch die u hebt opgegeven in het venster **VA-dagboekinstellingen** voor het opgegeven afschrijvingsboek. Zie [Procedure: Afschrijving voor vaste activa instellen](fa-how-setup-depreciation.md) voor meer informatie.    
9. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **VA-financiële dagboeken** in en kies vervolgens de gerelateerde koppeling.
10. Kies in het venster **Financieel dagboek voor vaste activa** de actie **Boeken** om de herindeling te boeken die u in stap 4 tot en met 8 hebt uitgevoerd.

## <a name="to-combine-two-fixed-assets-into-one"></a>Twee vaste activa combineren in één vast activum
U kunt meerdere vaste activa combineren in één vast activum, bijvoorbeeld als u gedistribueerde vaste activa in één afdeling verplaatst. Als u aanschafkosten en afschrijving hebt geboekt voor het vaste activum dat moet worden verplaatst, worden deze waarden gecombineerd in het ene vaste activum.

1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **VA-herindelingsdagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Een herindelingsdagboek maken waarin het veld **VA-nr.** het oorspronkelijke vaste activum bevat dat moet worden verplaatst/gecombineerd en het veld **Nieuw VA-nr.** het vaste activum bevat waarmee het wordt gecombineerd.
3. Laat het veld **Herindeling aanschafkosten-%** leeg om de gehele aanschafkosten te verplaatsen/combineren.    
4. Schakel de selectievakjes **Herindeling aanschafkosten** en **Herindeling afschrijving** in.
5. Kies op het tabblad **Acties** de optie **Herindelen**.

    Er worden nu twee regels gemaakt in het financieel dagboek voor vaste activa met behulp van de sjabloon en batch die u hebt opgegeven in het venster **VA-dagboekinstellingen** voor het opgegeven afschrijvingsboek. Zie [Procedure: Afschrijving voor vaste activa instellen](fa-how-setup-depreciation.md) voor meer informatie.   
6. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **VA-financiële dagboeken** in en kies vervolgens de gerelateerde koppeling.
7. Kies in het venster **Financieel dagboek voor vaste activa** de actie **Boeken** om de herindeling te boeken die u in stap 2 tot en met 5 hebt uitgevoerd.

## <a name="to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification"></a>Gewijzigde afschrijvingsboekwaarden wegens herindeling van vaste activa bekijken
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **VA-boekwaarde 02** in en kies vervolgens de gerelateerde koppeling.
2. Vul indien nodig de velden in.
3. Kies de knop **Afdrukken** of **Voorbeeld**.  

## <a name="see-also"></a>Zie ook
[Vaste activa](fa-manage.md)  
[Vaste activa instellen](fa-setup.md)  
[Financiën](finance.md)  
[Welkom bij [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)](index.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

