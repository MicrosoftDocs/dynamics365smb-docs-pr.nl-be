---
title: 'Procedure: Het gebruik van een record verhinderen en toestaan'
description: 'Als u wilt voorkomen dat een record wordt gebruikt, kunt u twee werkstroomreacties opnemen in een werkstroom die het gebruik van de record bepaalt.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: bholtorf
---
# Gebruik van een record beperken en toestaan

Als u wilt voorkomen dat een record wordt gebruikt bij bepaalde activiteiten, bijvoorbeeld totdat de record is goedgekeurd, kunt u twee werkstroomantwoorden opnemen in een werkstroom die het gebruik van de record bestuurt. Eén werkstroomreactie beperkt het gebruik van de record zoals gedefinieerd door de werkstroomgebeurtenis en -voorwaarden. De andere werkstroomreactie staat het gebruik van de record toe zoals gedefinieerd door de werkstroomgebeurtenis en -voorwaarden. Er zijn twee reacties in de standaardversie van [!INCLUDE[prod_short](includes/prod_short.md)] voor dit doel: **Recordbeperking toevoegen** en **Recordbeperking verwijderen**.

> [!NOTE]  
> De standaardversie van [!INCLUDE[prod_short](includes/prod_short.md)] helpt verhinderen dat een record wordt geboekt, als betaling wordt geëxporteerd en als cheque wordt afgedrukt. Als een Microsoft-partner andere beperkingen wil ondersteunen, moet deze de toepassingscode aanpassen.  

> [!NOTE]  
> De werkstroomfunctionaliteit om te verhinderen en toe te staan dat records worden gebruikt houdt geen verband met de functionaliteit om het boeken van artikel-, klant- en leveranciersrecords te blokkeren.

In de volgende procedure wordt beschreven hoe u het boeken van inkooporders kunt verhinderen totdat deze zijn goedgekeurd. De nieuwe werkstroom wordt gebaseerd op de bestaande sjabloon *Goedkeuringswerkstroom inkoopfactuur*.  

## Een werkstroomstap maken die voorkomt dat niet-goedgekeurde inkooporders worden geboekt

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Werkstromen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Werkstromen** de actie **Nieuwe werkstroom uit sjabloon**. Meer informatie op [Werkstromen maken van werkstroomsjablonen](across-how-to-create-workflows-from-workflow-templates.md)
3. Kies op de pagina **Werkstroomsjablonen** de sjabloon genaamd *Goedkeuringswerkstroom inkoopfactuur*.  

   Bij de eerste twee werkstroomstappen draait het om het verhinderen en vervolgens het toestaan van het gebruik van inkoopfacturen. Wijzig de gebeurtenisvoorwaarde in de eerste stap van de werkstroom om op te geven dat deze van toepassing is op inkooporders.  
4. Kies op het sneltabblad **Werkstroomstappen** het veld **Op voorwaarde** voor de eerste stap en selecteer vervolgens voor het filter **Documentsoort** de optie **Order**.  
5. Ga door om andere werkstroomstappen te bewerken, te verwijderen of toe te voegen om een bedrijfsproces te vertegenwoordigen dat begint door het boeken van niet-goedgekeurde inkooporders te verhinderen.  

## Zie ook

[Goedkeuringswerkstromen gebruiken](across-use-workflows.md)  
[Goedkeuringswerkstromen maken](across-how-to-create-workflows.md)  
[Werkstroom](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
