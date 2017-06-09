---
title: 'Procedure: Verzekering voor vaste activa instellen| Microsoft Docs'
description: Beschrijft hoe u het systeem instelt voor verzekering van vaste activa.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 03/23/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 6473b74823f787e6b1eac599bb95b6d100a02c1e
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-fixed-asset-insurance"></a>Procedure: Verzekering voor vaste activa instellen
Om de verzekeringsdekking voor vaste activa te beheren, moet u eerst enkele algemene verzekeringsgegevens en een verzekeringskaart per polis instellen.

## <a name="to-set-up-general-insurance-information"></a>Algemene verzekeringsinformatie instellen
Als u de verzekeringsfuncties wilt gebruiken in [!INCLUDE[d365fin](includes/d365fin_md.md)], moet u algemene verzekeringsinformatie instellen.  

1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **VA-instellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a>Verzekeringssoorten instellen
U kunt uw verzekeringspolissen in categorieën indelen, bijvoorbeeld diefstalverzekering of brandverzekering. De verzekeringssoorten worden gebruikt op de verzekeringskaarten.

1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Verzekeringssoorten** in en kies vervolgens de gerelateerde koppeling.  
2. Vul indien nodig de velden in.

## <a name="to-set-up-insurance-cards"></a>Verzekeringskaarten instellen
Gegevens over verzekeringspolissen kunt u invoeren op de verzekeringskaart.  

1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Verzekering** in en kies vervolgens de gerelateerde koppeling.  
2. Kies in het venster **Verzekering** de actie **Nieuw** om een nieuwe verzekeringskaart te maken.  
3. Vul indien nodig de velden in.

## <a name="to-set-up-insurance-journal-templates"></a>Verzekeringsdagboeksjablonen instellen
Er wordt in [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisch een verzekeringsdagboeksjabloon gemaakt als u **Verzekeringsdagboek** voor het eerst opent, maar het is ook mogelijk om extra dagboeksjablonen in te stellen. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.  

1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Verzekeringsdagboeksjablonen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul indien nodig de velden in.

## <a name="to-set-up-insurance-journal-batches"></a>Verzekeringsdagboekbatches instellen
Het is mogelijk om batches in te stellen in een verzekeringsdagboeksjabloon. De waarden in de dagboekbatch worden als standaardwaarden gebruikt als de velden op de dagboekregels niet zijn ingevuld. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.  

1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Verzekeringsdagboeksjablonen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer een verzekeringsdagboeksjabloon en kies vervolgens de actie **Batches**.
3. Vul in het venster **Verzekeringsdagboekbatches** indien nodig de velden in.

**Opmerking**: nummers hebben een speciale functie in dagboeknamen. Als een dagboeksjabloon of dagboekbatch een nummer bevat, wordt dit nummer bij elke boeking van het dagboek automatisch verhoogd. Als HH1 bijvoorbeeld is opgegeven in het veld **Naam**, verandert de naam van het dagboek in HH2 als het dagboek met de naam HH1 is geboekt.

## <a name="see-also"></a>Zie ook
[Vaste activa instellen](fa-setup.md)  
[Vaste activa](fa-manage.md)  
[Financiën](finance.md)  
[Welkom bij [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)](index.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

