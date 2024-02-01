---
title: 'Niet-aftrekbare btw instellen [BE]'
description: U kunt de btw-bedragen voor bepaalde soorten onkosten berekenen die gedeeltelijk als btw kunnen worden aangegeven.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/17/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-non-deductible-vat-in-the-belgian-version"></a>Niet-aftrekbare btw instellen in de Belgische versie
U kunt btw-bedragen voor bepaalde soorten onkosten berekenen die gedeeltelijk als btw kunnen worden aangegeven. Wanneer u op de pagina **Grootboekrekening** 75 opgeeft in het veld **% niet-aftrekbare btw**, wordt 75 procent van het normale btw-bedrag beschouwd als bijkomende kosten en tijdens het boeken toegevoegd aan het nettobedrag. De resterende 25 procent wordt als normale btw geboekt.  

> [!NOTE]  
>  Als geen waarde wordt opgegeven in het veld **% niet-aftrekbare btw**, is het btw-bedrag 100 procent aftrekbaar.  

## <a name="to-set-up-the-non-deductible-vat-percentage"></a>Het niet-aftrekbare btw-percentage instellen

1.  Kies het pictogram ![lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Rekeningschema** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer een onkostengrootboekrekening waarvoor de gedeeltelijke aftrek nodig is en kies vervolgens de actie **Bewerken**.  
3.  Voer het bedrag in het veld **Niet-aftrekbare btw** in.  
4.  Kies de knop **Ok**.  

## <a name="see-also"></a>Zie ook
 [Belgische btw](belgian-vat.md)   
 [Periodieke btw-rapporten afdrukken](how-to-print-periodic-vat-reports.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
