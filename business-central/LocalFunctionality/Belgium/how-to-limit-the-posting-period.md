---
title: 'De boekingsperiode beperken [BE]'
description: 'U kunt de periode waarop boeking is toegestaan op drie verschillende niveaus beperken: op bedrijf, op gebruiker en op sjabloon.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/17/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="limit-the-posting-period-in-the-belgian-version"></a>De boekingsperiode beperken in de Belgische versie
In [!INCLUDE[prod_short](../../includes/prod_short.md)] kunt u de periode waarop boeking is toegestaan op drie verschillende niveaus beperken: **op bedrijf**, **op gebruiker** en **op sjabloon**.  

Boekingsperioden beperken kan handig zijn als een bedrijf zijn verkoopdagboek aan het einde van elke maand sluit. Dit voorkomt dat verkopers verkoopdocumenten van de vorige maand registreren. Tegelijkertijd kan het inkoopdagboek open blijven om inkomende inkoopfacturen van de vorige maand te registreren.  

Wanneer u op de pagina **Financieel-dagboeksjablonen** boekt, wordt de inhoud van het veld **Boeken toegest. vanaf** en het veld **Boeken toegest. tot** gecontroleerd op een datuminterval. Het datuminterval geeft aan wanneer u een dagboeksjabloon kunt boeken. Als het veld leeg is, wordt de pagina **Gebruikersinstellingen** gecontroleerd op een datuminterval voor de huidige gebruiker. Als de pagina **Gebruikersinstellingen** geen interval bevat, wordt het veld **Boeken toegest. vanaf** en het veld **Boeken toegest. tot** op de pagina **Boekhoudinstellingen** gecontroleerd op een datuminterval op het bedrijfsniveau.  

## <a name="to-limit-the-posting-periods-by-company"></a>De boekingsperioden per bedrijf beperken

1.  Kies het pictogram ![lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Grootboekinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2.  Als u het begin van de periode wilt opgeven, kiest u het veld **Boeken toegest. vanaf** en voert u vervolgens de vroegste datum in waarop boeken naar het bedrijf is ingeschakeld.  
3.  Als u het einde van de periode wilt opgeven, kiest u het veld **Boeken toegest. tot** en voert u vervolgens de laatste datum in waarop boeken naar het bedrijf is ingeschakeld.  

## <a name="to-limit-the-posting-periods-by-user"></a>De boekingsperioden per gebruiker beperken

1.  Kies het pictogram ![lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Gebruikersinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2.  Als u het begin van de periode wilt opgeven, kiest u het veld **Boeken toegest. vanaf** en voert u vervolgens de vroegste datum in waarop de gebruiker naar het bedrijf kan boeken.  
3.  Als u het einde van de periode wilt opgeven, kiest u het veld **Boeken toegest. tot** en voert u vervolgens de laatste datum in waarop de gebruiker naar het bedrijf kan boeken.  

## <a name="to-limit-the-posting-periods-by-template"></a>De boekingsperioden per sjabloon beperken

1.  Kies het pictogram ![lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Dagboeksjablonen** in en kies vervolgens de gerelateerde koppeling.  
2.  Als u het begin van de periode wilt opgeven, kiest u het veld **Boeken toegest. vanaf** en voert u vervolgens de vroegste datum in waarop de gebruiker naar het bedrijf kan boeken.  
3.  Als u het einde van de periode wilt opgeven, kiest u het veld **Boeken toegest. tot** en voert u vervolgens de laatste datum in waarop de gebruiker naar het bedrijf kan boeken.  

## <a name="see-also"></a>Zie ook
 [Belgische lokale functionaliteit](belgium-local-functionality.md)   
 [Boekingsperioden opgeven](../../finance-how-specify-posting-periods.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
