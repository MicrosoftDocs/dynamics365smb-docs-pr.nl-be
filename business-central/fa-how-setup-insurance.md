---
title: VA-verzekering instellen| Microsoft Docs
description: U stelt een verzekeringskaart en algemene verzekeringsbeleidsgegevens in om verzekeringsdekking voor vaste activa te beheren.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 076fdb197a2fef45f67d4c2738eaac0503c91e51
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-fixed-asset-insurance"></a>Verzekering van vaste activa instellen
Om de verzekeringsdekking voor vaste activa te beheren, moet u eerst enkele algemene verzekeringsgegevens en een verzekeringskaart per polis instellen.

## <a name="to-set-up-general-insurance-information"></a>Algemene verzekeringsinformatie instellen
Als u de verzekeringsfuncties wilt gebruiken in [!INCLUDE[d365fin](includes/d365fin_md.md)], moet u algemene verzekeringsinformatie instellen.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **VA-instellingen** in en klik vervolgens op de gerelateerde koppeling.  
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a>Verzekeringssoorten instellen
U kunt uw verzekeringspolissen in categorieën indelen, bijvoorbeeld diefstalverzekering of brandverzekering. De verzekeringssoorten worden gebruikt op de verzekeringskaarten.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verzekeringssoorten** in en klik vervolgens op de gerelateerde koppeling.  
2. Vul indien nodig de velden in.

## <a name="to-set-up-insurance-cards"></a>Verzekeringskaarten instellen
Gegevens over verzekeringspolissen kunt u invoeren op de verzekeringskaart.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verzekering** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies in het venster **Verzekering** de actie **Nieuw** om een nieuwe verzekeringskaart te maken.  
3. Vul indien nodig de velden in.

## <a name="to-set-up-insurance-journal-templates"></a>Verzekeringsdagboeksjablonen instellen
Er wordt in [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisch een verzekeringsdagboeksjabloon gemaakt als u **Verzekeringsdagboek** voor het eerst opent, maar het is ook mogelijk om extra dagboeksjablonen in te stellen. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verzekeringsdagboeksjablonen** in en klik vervolgens op de gerelateerde koppeling.  
2. Vul indien nodig de velden in.

## <a name="to-set-up-insurance-journal-batches"></a>Verzekeringsdagboekbatches instellen
Het is mogelijk om batches in te stellen in een verzekeringsdagboeksjabloon. De waarden in de dagboekbatch worden als standaardwaarden gebruikt als de velden op de dagboekregels niet zijn ingevuld. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verzekeringsdagboeksjablonen** in en klik vervolgens op de gerelateerde koppeling.  
2. Selecteer een verzekeringsdagboeksjabloon en kies vervolgens de actie **Batches**.
3. Vul in het venster **Verzekeringsdagboekbatches** indien nodig de velden in.

> [!NOTE]  
>   Nummers hebben een speciale functie in dagboeknamen. Als een dagboeksjabloon of dagboekbatch een nummer bevat, wordt dit nummer bij elke boeking van het dagboek automatisch verhoogd. Als HH1 bijvoorbeeld is opgegeven in het veld **Naam**, verandert de naam van het dagboek in HH2 als het dagboek met de naam HH1 is geboekt.

## <a name="see-also"></a>Zie ook
[Vaste activa instellen](fa-setup.md)  
[Vaste activa](fa-manage.md)  
[Financiën](finance.md)  
[Welkom bij [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

