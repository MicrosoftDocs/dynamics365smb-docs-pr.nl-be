---
title: Aangepaste configuratiepakketten voor bedrijven maken | Microsoft Docs
description: Naarmate uw bedrijf groeit, zult u waarschijnlijk gaan vertrouwen op een set bedrijfstypen die u met de meeste van uw klanten gebruikt. U kunt uw implementatieproces stroomlijnen door van deze typen configuratiepakketten voor bedrijven te maken die beschikbaar zijn voor hergebruik.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7feaa0e41cf5800ffd51d5807a90f6929492804e
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="create-custom-company-configuration-packages"></a>Aangepaste configuratiepakketten voor bedrijven maken
Naarmate uw bedrijf groeit, zult u waarschijnlijk gaan vertrouwen op een set bedrijfstypen die u met de meeste van uw klanten gebruikt. U kunt uw implementatieproces stroomlijnen door van deze typen configuratiepakketten voor bedrijven te maken die beschikbaar zijn voor hergebruik.  

In het algemeen maakt u een configuratiepakket per functiegebied. Zo kunt u bijvoorbeeld een pakket maken voor uw productiefunctionaliteit. Dat kunt u vervolgens toepassen en nieuwe gebieden in een bedrijf instellen als u ze nodig hebt  

Een andere benadering zou zijn om een pakket te maken dat de tabellen bevat waarin de instellingen worden gedefinieerd, zoals de volgende:  

-   VA-instellingen  
-   Grootboekinstellingen  
-   Voorraadinstellingen  
-   Productie-instellingen  
-   Inkoopinstellingen  
-   Marketinginstellingen  
-   Service-instellingen  
-   Verkoopinstellingen  
-   Magazijninstellingen  
-   Boekingsgroepinstellingen  
-   Btw-boekingsgroepinstellingen  
-   Voorraadboekingsgroepinstellingen  

Als u een volledige lijst met instellingstabellen wilt zien, kiest u het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voert u **Instellingen** in en kiest u de gerelateerde koppeling.  

## <a name="to-create-a-custom-company-configuration-package"></a>Een aangepast configuratiepakket voor een bedrijf maken  
1.  Definieer een nieuwe [!INCLUDE[d365fin](includes/d365fin_md.md)], ***NIET MOGELIJK Koppeling naar Help voor "Een nieuwe tenant maken"***.   
2.  Maak een nieuw bedrijf voor de branche- of oplossingssjabloon. Zie [Een nieuw bedrijf maken](admin-how-to-create-a-new-company.md) voor meer informatie.  
3.  Stel het nieuwe bedrijf in op de door u benodigde wijze. Vul alle vereiste instellingentabellen in.  
4.  Open het nieuw bedrijf.
5. Open het venster **Configuratiewerkblad**.  
6.  Voeg de tabellen die u wilt overbrengen naar een ander bedrijf toe aan het werkblad. Wijs de werkbladregels toe aan het pakket.  
7.  Maak een vragenlijst voor de meest gebruikte instellingentabel.  
8.  Stel configuratiesjablonen op om het gemakkelijker te maken om hoofdgegevens, zoals klanten of artikelen, te definiëren.  
9.  Exporteer uw pakket als een .rapidstart-bestand.  

## <a name="see-also"></a>Zie ook  
[Een bedrijf met RapidStart Services instellen](admin-set-up-a-company-with-rapidstart.md)  
[Beheer](admin-setup-and-administration.md)

