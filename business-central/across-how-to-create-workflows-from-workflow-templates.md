---
title: Werkstromen maken van werkstroomsjablonen
description: Om tijd te besparen bij het maken van nieuwe goedkeuringswerkstromen kunt u werkstromen maken van werkstroomsjablonen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: dajoo
ms.topic: how-to
ms.search.keywords: null
ms.date: 03/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-workflows-from-workflow-templates"></a>Werkstromen maken van werkstroomsjablonen

Op de pagina **Werkstroom** kunt u een werkstroom maken door een reeks werkstroomstappen op de regels te maken. Elke stap bestaat uit een werkstroomgebeurtenis (Als gebeurtenis), aangepast door gebeurtenisvoorwaarden (Op voorwaarde), en een werkstroomreactie (Dan reactie), aangepast door responsopties. De velden op werkstroomregels bieden vaste lijsten van gebeurtenis- en reactiewaarden die de scenario's vertegenwoordigen die [!INCLUDE [prod_short](includes/prod_short.md)] ondersteunt. Zie voor meer informatie [Werkstromen maken](across-how-to-create-workflows.md).

Om u tijd te besparen bij het maken van goedkeuringswerkstromen, biedt [!INCLUDE [prod_short](includes/prod_short.md)] werkstroomsjablonen. De sjablonen zijn beschikbaar op de pagina **Werkstroomsjablonen**. U kunt de sjablonen gebruiken zoals ze zijn, of ze aanpassen aan uw behoeften. De codes voor de werkstroomsjablonen van Microsoft hebben het voorvoegsel **MS-**.

[!INCLUDE [workflow-next-step](includes/workflow-next-step.md)]

Als u een werkstroomsjabloon wijzigt, maar later spijt krijgt van de wijziging, gebruikt u de actie **Microsoft-sjablonen opnieuw instellen** om terug te keren naar de oorspronkelijke instelling voor de werkstroom.

> [!CAUTION]
> Met de actie **Microsoft-sjablonen opnieuw instellen** worden alle Microsoft-werkstroomsjablonen opnieuw ingesteld. U kunt geen enkele sjabloon opnieuw instellen.  

Een andere manier om snel een werkstroom te maken, is door deze te importeren, bijvoorbeeld als u deze vanuit een ander exemplaar van [!INCLUDE[prod_short](includes/prod_short.md)] hebt geëxporteerd. Meer informatie op [Werkstromen exporteren en importeren](across-how-to-export-and-import-workflows.md).  

## <a name="to-create-a-workflow-from-a-workflow-template"></a>Een werkstroom maken van een werkstroomsjabloon

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Werkstromen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuwe werkstroom uit sjabloon**. De pagina **Werkstroomsjablonen** verschijnt.  
3. Selecteer een werkstroomsjabloon en kies vervolgens **OK**.  

   De pagina **Werkstroom** wordt geopend voor een nieuwe werkstroom die alle gegevens van de geselecteerde sjabloon bevat. De waarde in het veld **Code** wordt uitgebreid met bijvoorbeeld '- 01' om aan te geven dat dit de eerste werkstroom is die is gemaakt vanuit de werkstroomsjabloon.  
4. Als u de werkstroom wilt aanpassen, bewerkt u de werkstroomstappen of voegt u nieuwe stappen toe. Zie voor meer informatie [Werkstromen maken](across-how-to-create-workflows.md).  

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
