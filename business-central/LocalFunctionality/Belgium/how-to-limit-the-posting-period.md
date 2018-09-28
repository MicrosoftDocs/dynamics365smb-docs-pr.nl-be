---
title: De boekingsperiode beperken
description: 'U kunt de periode waarop boeking is toegestaan op drie verschillende niveaus beperken: **op bedrijf**, **op gebruiker** en **op sjabloon**.'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 08c14c51ff9e2cf61ea81ece9417bfe5c02bf3a2
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="limit-the-posting-period"></a>De boekingsperiode beperken
In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kunt u de periode waarop boeking is toegestaan op drie verschillende niveaus beperken: **op bedrijf**, **op gebruiker** en **op sjabloon**.  

Boekingsperioden beperken kan handig zijn als een bedrijf zijn verkoopdagboek aan het einde van elke maand sluit. Dit voorkomt dat verkopers verkoopdocumenten van de vorige maand registreren. Tegelijkertijd kan het inkoopdagboek open blijven om inkomende inkoopfacturen van de vorige maand te registreren.  

Wanneer u in het venster **Financieel-dagboeksjablonen** boekt, wordt de inhoud van het veld **Boeken toegest. vanaf** en het veld **Boeken toegest. tot** gecontroleerd op een datuminterval. Het datuminterval geeft aan wanneer u een dagboeksjabloon kunt boeken. Als het veld leeg is, wordt het venster **Gebruikersinstellingen** gecontroleerd op een datuminterval voor de huidige gebruiker. Als het venster **Gebruikersinstellingen** geen interval bevat, wordt het veld **Boeken toegest. vanaf** en het veld **Boeken toegest. tot** in het venster **Boekhoudinstellingen** gecontroleerd op een datuminterval op het bedrijfsniveau.  

## <a name="to-limit-the-posting-periods-by-company"></a>De boekingsperioden per bedrijf beperken  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Grootboekinstellingen** in en klik vervolgens op de gerelateerde koppeling.  
2.  Als u het begin van de periode wilt opgeven, kiest u het veld **Boeken toegest. vanaf** en voert u vervolgens de vroegste datum in waarop boeken naar het bedrijf is ingeschakeld.  
3.  Als u het einde van de periode wilt opgeven, kiest u het veld **Boeken toegest. tot** en voert u vervolgens de laatste datum in waarop boeken naar het bedrijf is ingeschakeld.  

## <a name="to-limit-the-posting-periods-by-user"></a>De boekingsperioden per gebruiker beperken  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Gebruikersinstellingen** in en klik vervolgens op de gerelateerde koppeling.  
2.  Als u het begin van de periode wilt opgeven, kiest u het veld **Boeken toegest. vanaf** en voert u vervolgens de vroegste datum in waarop de gebruiker naar het bedrijf kan boeken.  
3.  Als u het einde van de periode wilt opgeven, kiest u het veld **Boeken toegest. tot** en voert u vervolgens de laatste datum in waarop de gebruiker naar het bedrijf kan boeken.  

## <a name="to-limit-the-posting-periods-by-template"></a>De boekingsperioden per sjabloon beperken  

1.  Kies het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Financieel-dagboeksjablonen** in en klik vervolgens op de gerelateerde koppeling.  
2.  Als u het begin van de periode wilt opgeven, kiest u het veld **Boeken toegest. vanaf** en voert u vervolgens de vroegste datum in waarop de gebruiker naar het bedrijf kan boeken.  
3.  Als u het einde van de periode wilt opgeven, kiest u het veld **Boeken toegest. tot** en voert u vervolgens de laatste datum in waarop de gebruiker naar het bedrijf kan boeken.  

## <a name="see-also"></a>Zie ook  
 [Belgische lokale functionaliteit](belgium-local-functionality.md)   
 [Boekingsperioden opgeven](../../finance-how-specify-posting-periods.md)

