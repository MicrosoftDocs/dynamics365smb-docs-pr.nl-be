---
title: Splitsen van bulkgoederen met gestuurde opslag en pick
description: 'Leer hoe u automatisch bulksplitsing met gerichte opslag en pick, evenals bulksplitsing in picks, opslag, verplaatsingen en meer kunt inschakelen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '5703, 7352'
ms.date: 11/04/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Automatisch splitsen van bulkgoederen met gestuurde opslag en pick inschakelen

Voor locaties die gebruikmaken van gestuurde opslag en pick, [!INCLUDE[prod_short](includes/prod_short.md)] kunt u eenheden opsplitsen in kleinere eenheden wanneer er magazijninstructies worden gemaakt voor brondocumenten, productieorders of interne picks en opslag. Bulksplitsing kan ook betekenen dat artikelen in kleinere eenheden worden verzameld om de hoeveelheid van een grotere maateenheid op een brondocument of productieorder te evenaren.

## Bulksplitsing in picks  

Als u artikelen wilt opslaan in een aantal verschillende eenheden in een locatie en deze automatisch wilt laten combineren tijdens het pickproces, schakelt u de wisselknop **Bulksplitsing toestaan** in op de pagina Vestigingskaart. Voor de uitvoering van een taak zoekt [!INCLUDE [prod_short](includes/prod_short.md)] daarna automatisch naar een artikel in dezelfde maateenheid. Is die er niet, dan zal [!INCLUDE [prod_short](includes/prod_short.md)] voorstellen dat u een grotere maateenheid opsplitst in de maateenheid die nodig is.  

Als er alleen kleinere eenheden beschikbaar zijn, zal [!INCLUDE [prod_short](includes/prod_short.md)] voorstellen dat u artikelen verzamelt om aan de hoeveelheid voor de verzending of productieorder te kunnen voldoen. In de praktijk wordt de grotere eenheid op het brondocument opgesplitst in kleinere pickeenheden.  

## Bulksplitsing in opslag  

Bij magazijnopslag stelt [!INCLUDE [prod_short](includes/prod_short.md)] Plaatsen-regels voor in de opslageenheid. Zo kunnen er bijvoorbeeld stuks worden voorgesteld, ook al komen de artikelen in een andere maateenheid aan.  

## Bulksplitsing in verplaatsingen  

[!INCLUDE [prod_short](includes/prod_short.md)] kan ook bulksplitsing uitvoeren in bevoorradingsverplaatsingen als de wisselknop **Bulksplitsing toestaan** op de pagina **Bakaanvulling berekenen** is ingeschakeld.  

U kunt de resultaten van de omzetting van de ene eenheid in de andere weergeven als tussenliggende bulksplitsingsregels in de opslag-, pick- of verplaatsingsinstructies.  

> [!NOTE]  
> Als u het veld **Breakbulkfilter plaatsen** in de kop van de magazijninstructie selecteert, worden de bulksplitsingsregels verborgen wanneer de grotere eenheid volledig wordt gebruikt. Bijvoorbeeld: als een pallet 12 stuks bevat en u alle 12 stuks gebruikt, wordt u gevraagd 1 pallet te nemen en 12 stuks te plaatsen. Als u echter slechts 9 stuks moet picken, worden de bulksplitsingsregels niet verborgen, zelfs niet als u het veld **Bulksplitsingsfilter** hebt geselecteerd. De regels worden niet verborgen omdat u de resterende drie stuks ergens in het magazijn moet opslaan.  

> [!NOTE]  
> Als u wilt dat uw maateenheden optimaal presteren in het magazijn, ook in verband met bulksplitsing, moet u proberen om:  
>
> - De basiseenheid voor een artikel in te stellen als de kleinste eenheid die u denkt nodig te hebben in de magazijnprocessen.  
> - Alternatieve eenheden voor het artikel instellen als veelvouden van de basiseenheid.  

## Zie ook  

[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md) 
[Assemblagebeheer](assembly-assemble-items.md)
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]