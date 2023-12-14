---
title: Goedkeuringswerkstromen exporteren en importeren
description: 'Als u werkstromen wilt overbrengen naar andere Business Central-databases, bijvoorbeeld om tijd te besparen wanneer u nieuwe werkstromen maakt, kunt u werkstromen exporteren en importeren.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: bholtorf
---
# <a name="export-and-import-approval-workflows"></a>Goedkeuringswerkstromen exporteren en importeren

Als u werkstromen wilt overbrengen naar andere [!INCLUDE[prod_short](includes/prod_short.md)]-databases, bijvoorbeeld om tijd te besparen wanneer u nieuwe werkstromen maakt, kunt u werkstromen exporteren en importeren.  

Een andere manier om werkstromen snel te maken is werkstroomsjablonen te gebruiken. Meer informatie op [Werkstromen maken van werkstroomsjablonen](across-how-to-create-workflows-from-workflow-templates.md)  

Op de pagina **Werkstroom** kunt u een werkstroom maken door de betrokken stappen te vermelden op de regels. Elke stap bestaat uit een werkstroomgebeurtenis, aangepast door gebeurtenistoestanden, en een werkstroomantwoord, aangepast door antwoordopties. U definieert werkstroomregels door velden op werkstroomregels te vullen met behulp van lijsten met vaste gebeurtenis- en reactiewaarden die scenario's vertegenwoordigen die worden ondersteund door de toepassingscode. Zie voor meer informatie [Werkstromen maken](across-how-to-create-workflows.md).  

## <a name="export-a-workflow"></a>Een werkstroom exporteren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Werkstromen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer een werkstroom en kies de actie **Exporteren naar bestand**.  

## <a name="import-a-workflow"></a>Een werkstroom importeren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Werkstromen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Importeren uit bestand**.  
3. Selecteer op de pagina **Importeren** **Kiezen**, kies het XML-bestand dat de werkstroom bevat, en klik vervolgens op **Openen**.  

> [!CAUTION]  
> Als de werkstroomcode al in de database bestaat, worden de werkstroomstappen overschreven door de stappen in de geïmporteerde werkstroom.  

## <a name="see-also"></a>Zie ook

[Goedkeuringswerkstromen maken](across-how-to-create-workflows.md)  
[Werkstromen maken van werkstroomsjablonen](across-how-to-create-workflows-from-workflow-templates.md)  
[Gearchiveerde instanties van werkstroomstappen bekijken](across-how-to-view-archived-workflow-step-instances.md)  
[Goedkeuringswerkstromen verwijderen](across-how-to-delete-workflows.md)  
[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Goedkeuringswerkstromen instellen](across-set-up-workflows.md)  
[Goedkeuringswerkstromen gebruiken](across-use-workflows.md)  
[Werkstroom](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
