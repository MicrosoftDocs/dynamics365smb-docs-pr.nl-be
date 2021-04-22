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
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0ebb62a4ef9ea84ec5bfddc099dfb6120a4e6405
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774053"
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
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]