---
title: Werkstromen maken van werkstroomsjablonen
description: Om tijd te besparen bij het maken van nieuwe goedkeuringswerkstromen kunt u niet-bewerkbare werkstromen maken van de werkstroomsjablonen met het voorvoegsel 'MS'.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="create-workflows-from-workflow-templates"></a>Werkstromen maken van werkstroomsjablonen

Om tijd te besparen bij het maken van nieuwe goedkeuringswerkstromen kunt u werkstroomsjablonen gebruiken.  

Werkstroomsjablonen zijn niet-bewerkbare werkstromen die in de standaardversie van [!INCLUDE[prod_short](includes/prod_short.md)] bestaan. De codes voor werkstroomsjablonen die door Microsoft zijn gemaakt, hebben het voorvoegsel 'MS-'.  

Een andere manier om snel een werkstroom te maken is een bestaande werkstroom te importeren die u in een bestand buiten [!INCLUDE[prod_short](includes/prod_short.md)] hebt. Meer informatie op [Werkstromen exporteren en importeren](across-how-to-export-and-import-workflows.md).  

Op de pagina **Werkstroom** kunt u een werkstroom maken door de betrokken stappen te vermelden op de regels. Elke stap bestaat uit een werkstroomgebeurtenis, aangepast door gebeurtenistoestanden, en een werkstroomantwoord, aangepast door antwoordopties. U definieert werkstroomregels door velden op werkstroomregels te vullen vanuit lijsten met vaste gebeurtenis- en reactiewaarden die scenario's vertegenwoordigen die worden ondersteund door de toepassingscode. Zie voor meer informatie [Werkstromen maken](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-a-workflow-template"></a>Een werkstroom maken van een werkstroomsjabloon

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Werkstromen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuwe werkstroom uit sjabloon**. De pagina **Werkstroomsjablonen** verschijnt.  
3. Selecteer een werkstroomsjabloon en kies vervolgens **OK**.  

   De pagina **Werkstroom** wordt geopend voor een nieuwe werkstroom die alle gegevens van de geselecteerde sjabloon bevat. De waarde in het veld **Code** wordt uitgebreid met bijvoorbeeld '- 01' om aan te geven dat dit de eerste werkstroom is die is gemaakt vanuit de werkstroomsjabloon.  
4. Ga verder met het maken van de werkstroom door de werkstroomstappen te bewerken of nieuwe stappen toe te voegen. Zie voor meer informatie [Werkstromen maken](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Zie ook

[Goedkeuringswerkstromen maken](across-how-to-create-workflows.md)  
[Goedkeuringswerkstromen exporteren en importeren](across-how-to-export-and-import-workflows.md)  
[Gearchiveerde instanties van werkstroomstappen bekijken](across-how-to-view-archived-workflow-step-instances.md)  
[Goedkeuringswerkstromen verwijderen](across-how-to-delete-workflows.md)  
[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Goedkeuringswerkstromen instellen](across-set-up-workflows.md)  
[Goedkeuringswerkstromen gebruiken](across-use-workflows.md)  
[Werkstroom](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
