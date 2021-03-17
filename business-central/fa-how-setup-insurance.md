---
title: VA-verzekering instellen| Microsoft Docs
description: U stelt een verzekeringskaart en algemene verzekeringsbeleidsgegevens in om verzekeringsdekking voor vaste activa te beheren.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: policy, coverage
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 10527690d19d019f8a5d94d8c4817f6a3bcd8479
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5380189"
---
# <a name="set-up-fixed-asset-insurance"></a>Verzekering van vaste activa instellen
Om de verzekeringsdekking voor vaste activa te beheren, moet u eerst enkele algemene verzekeringsgegevens en een verzekeringskaart per polis instellen.

## <a name="to-set-up-general-insurance-information"></a>Algemene verzekeringsinformatie instellen
Als u de verzekeringsfuncties wilt gebruiken in [!INCLUDE[prod_short](includes/prod_short.md)], moet u algemene verzekeringsinformatie instellen.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **VA-instellingen** in en kies de gerelateerde koppeling.  
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-insurance-types"></a>Verzekeringssoorten instellen
U kunt uw verzekeringspolissen in categorieën indelen, bijvoorbeeld diefstalverzekering of brandverzekering. De verzekeringssoorten worden gebruikt op de verzekeringskaarten.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verzekeringssoorten** in en kies de gerelateerde koppeling.  
2. Vul indien nodig de velden in.

## <a name="to-set-up-insurance-cards"></a>Verzekeringskaarten instellen
Gegevens over verzekeringspolissen kunt u invoeren op de verzekeringskaart.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verzekering** in en kies de gerelateerde koppeling.  
2. Kies op de pagina **Verzekering** de actie **Nieuw** om een nieuwe verzekeringskaart te maken.  
3. Vul de benodigde velden in.

## <a name="to-set-up-insurance-journal-templates"></a>Verzekeringsdagboeksjablonen instellen
Er wordt in [!INCLUDE[prod_short](includes/prod_short.md)] automatisch een verzekeringsdagboeksjabloon gemaakt als u de pagina **Verzekeringsdagboek** voor het eerst opent, maar het is ook mogelijk om extra dagboeksjablonen in te stellen. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verzekeringsdagboeksjablonen** in en kies de desbetreffende koppeling.  
2. Vul indien nodig de velden in.

## <a name="to-set-up-insurance-journal-batches"></a>Verzekeringsdagboekbatches instellen
Het is mogelijk om batches in te stellen in een verzekeringsdagboeksjabloon. De waarden in de dagboekbatch worden als standaardwaarden gebruikt als de velden op de dagboekregels niet zijn ingevuld. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verzekeringsdagboeksjablonen** in en kies de desbetreffende koppeling.  
2. Selecteer een verzekeringsdagboeksjabloon en kies vervolgens de actie **Batches**.
3. Vul op de pagina **Verzekeringsdagboekbatches** indien nodig de velden in.

> [!NOTE]  
>   Nummers hebben een speciale functie in dagboeknamen. Als een dagboeksjabloon of dagboekbatch een nummer bevat, wordt dit nummer bij elke boeking van het dagboek automatisch verhoogd. Als HH1 bijvoorbeeld is opgegeven in het veld **Naam**, verandert de naam van het dagboek in HH2 als het dagboek met de naam HH1 is geboekt.

## <a name="see-also"></a>Zie ook
[Vaste activa instellen](fa-setup.md)  
[Vaste activa](fa-manage.md)  
[Financiën](finance.md)  
[Aan de slag](product-get-started.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]