---
title: 'Procedure: Het gebruik van een record verhinderen en toestaan'
description: Als u wilt voorkomen dat een record wordt gebruikt, kunt u twee werkstroomreacties opnemen in een werkstroom die het gebruik van de record bepaalt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 7873091d64e55460986437cf255d98cd0d00b6d3
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130158"
---
# <a name="restrict-and-allow-usage-of-a-record"></a>Gebruik van een record beperken en toestaan

Als u wilt voorkomen dat een record wordt gebruikt bij bepaalde activiteiten, bijvoorbeeld totdat de record is goedgekeurd, kunt u twee werkstroomantwoorden opnemen in een werkstroom die het gebruik van de record bestuurt. Eén werkstroomantwoord beperkt het gebruik van de record zoals gedefinieerd door de werkstroomgebeurtenis en -voorwaarden. Een andere werkstroomantwoord staat het gebruik van de record toe zoals gedefinieerd door de werkstroomgebeurtenis en -voorwaarden. Er zijn twee reacties in de standaardversie van [!INCLUDE[prod_short](includes/prod_short.md)] voor dit doel: **Recordbeperking toevoegen** en **Recordbeperking verwijderen**.

> [!NOTE]  
> De standaardversie van [!INCLUDE[prod_short](includes/prod_short.md)] helpt verhinderen dat een record wordt geboekt, als betaling wordt geëxporteerd en als cheque wordt afgedrukt. Als een Microsoft-partner andere beperkingen wil ondersteunen, moet deze de toepassingscode aanpassen.  

> [!NOTE]  
> De werkstroomfunctionaliteit om te verhinderen en toe te staan dat records worden gebruikt houdt geen verband met de functionaliteit om het boeken van artikel-, klant- en leveranciersrecords te blokkeren.

In de volgende procedure wordt beschreven hoe u het boeken van inkooporders kunt verhinderen totdat deze zijn goedgekeurd. De nieuwe werkstroom wordt gebaseerd op de bestaande sjabloon Goedkeuringswerkstroom inkoopfactuur.  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Een werkstroomstap maken die voorkomt dat niet-goedgekeurde inkooporders worden geboekt

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Werkstromen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Werkstromen** de actie **Nieuwe werkstroom uit sjabloon**. Zie voor meer informatie [Werkstromen maken van werkstroomsjablonen](across-how-to-create-workflows-from-workflow-templates.md).
3. Kies op de pagina **Werkstroomsjablonen** de sjabloon genaamd *Goedkeuringswerkstroom inkoopfactuur*.  

   Zoals u ziet, draait het bij de eerste twee werkstroomstappen om het verhinderen en vervolgens het toestaan van het gebruik van inkoopfacturen. Ga door met het wijzigen van de gebeurtenisvoorwaarde in de eerste stap van de werkstroom om op te geven dat deze van toepassing is op inkooporders.  
4. Kies op het sneltabblad **Werkstroomstappen** het veld **Op voorwaarde** voor de eerste stap en selecteer vervolgens voor het filter **Documentsoort** de optie **Order**.  
5. Ga door om andere werkstroomstappen te bewerken, te verwijderen of toe te voegen in een bedrijfsproces dat begint door het boeken van niet-goedgekeurde inkooporders te verhinderen.  

## <a name="see-also"></a>Zie ook

[Werkstromen maken](across-how-to-create-workflows.md)  
[Werkstroom](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]