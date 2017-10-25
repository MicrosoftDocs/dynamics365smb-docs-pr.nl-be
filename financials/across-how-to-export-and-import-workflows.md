---
title: Werkstromen exporteren en importeren | Microsoft Docs
description: Als u werkstromen wilt overbrengen naar andere [!INCLUDE[d365fin](includes/d365fin_md.md)]-databases, bijvoorbeeld om tijd te besparen wanneer u nieuwe werkstromen maakt, kunt u werkstromen exporteren en importeren.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 8126d3850103819e885d9d131ca3074f1b7cfda1
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-export-and-import-workflows"></a>Procedure: Werkstromen exporteren en importeren
Als u werkstromen wilt overbrengen naar andere [!INCLUDE[d365fin](includes/d365fin_md.md)]-databases, bijvoorbeeld om tijd te besparen wanneer u nieuwe werkstromen maakt, kunt u werkstromen exporteren en importeren.  

 Een andere manier om werkstromen snel te maken is werkstromen te maken van werkstroomsjablonen. Zie voor meer informatie [Procedure: Werkstromen maken van werkstroomsjablonen](across-how-to-create-workflows-from-workflow-templates.md).  

 In het venster **Werkstroom** kunt u een werkstroom maken door de betrokken stappen te vermelden op de regels. Elke stap bestaat uit een werkstroomgebeurtenis, aangepast door gebeurtenistoestanden, en een werkstroomantwoord, aangepast door antwoordopties. U definieert werkstroomregels door velden op werkstroomregels te vullen vanuit lijsten met vaste gebeurtenis- en reactiewaarden die scenario's vertegenwoordigen die worden ondersteund door de toepassingscode. Zie voor meer informatie [Procedure: Werkstromen maken](across-how-to-create-workflows.md).  

## <a name="to-export-a-workflow"></a>Een werkstroom exporteren  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Werkstromen** in en klik op de gerelateerde koppeling.  
2.  Selecteer een werkstroom en kies de actie **Exporteren naar bestand**.  
3.  Kies in het venster **Bestand exporteren** de knop **Opslaan**.  
4.  Selecteer in het venster **Exporteren** een bestandslocatie en kies vervolgens de knop **Opslaan**.  

## <a name="to-import-a-workflow"></a>Een werkstroom importeren  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Werkstromen** in en klik op de gerelateerde koppeling.  
2.  Kies de actie **Importeren uit bestand**.  
3.  Selecteer in het venster **Importeren** het XML-bestand dat de werkstroom bevat, en klik vervolgens op **Openen**.  

> [!CAUTION]  
>  Als de werkstroomcode al in de database bestaat, worden de werkstroomstappen overschreven door de stappen in de geïmporteerde werkstroom.  

## <a name="see-also"></a>Zie ook  
 [Procedure: Werkstromen maken](across-how-to-create-workflows.md)   
 [Procedure: Werkstromen maken van werkstroomsjablonen](across-how-to-create-workflows-from-workflow-templates.md)   
 [Procedure: Gearchiveerde instanties van werkstroomstappen bekijken](across-how-to-view-archived-workflow-step-instances.md)   
 [Procedure: Werkstromen verwijderen](across-how-to-delete-workflows.md)   
 [Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Werkstromen instellen](across-set-up-workflows.md)   
 [Werkstromen gebruiken](across-use-workflows.md)   
 [Werkstroom](across-workflow.md)   

