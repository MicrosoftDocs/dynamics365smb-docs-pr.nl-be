---
title: Werkstromen exporteren en importeren | Microsoft Docs
description: Als u werkstromen wilt overbrengen naar andere Business Central-databases, bijvoorbeeld om tijd te besparen wanneer u nieuwe werkstromen maakt, kunt u werkstromen exporteren en importeren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: a0a67c3b6a706820c8b5fb073c090a6586435ca7
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816965"
---
# <a name="export-and-import-workflows"></a>Werkstromen exporteren en importeren
Als u werkstromen wilt overbrengen naar andere [!INCLUDE[d365fin](includes/d365fin_md.md)]-databases, bijvoorbeeld om tijd te besparen wanneer u nieuwe werkstromen maakt, kunt u werkstromen exporteren en importeren.  

 Een andere manier om werkstromen snel te maken is werkstromen te maken van werkstroomsjablonen. Zie voor meer informatie [Werkstromen maken van werkstroomsjablonen](across-how-to-create-workflows-from-workflow-templates.md).  

 Op de pagina **Werkstroom** kunt u een werkstroom maken door de betrokken stappen te vermelden op de regels. Elke stap bestaat uit een werkstroomgebeurtenis, aangepast door gebeurtenistoestanden, en een werkstroomantwoord, aangepast door antwoordopties. U definieert werkstroomregels door velden op werkstroomregels te vullen vanuit lijsten met vaste gebeurtenis- en reactiewaarden die scenario's vertegenwoordigen die worden ondersteund door de toepassingscode. Zie voor meer informatie [Werkstromen maken](across-how-to-create-workflows.md).  

## <a name="to-export-a-workflow"></a>Een werkstroom exporteren  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Werkstromen** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer een werkstroom en kies de actie **Exporteren naar bestand**.  
3.  Kies op de pagina **Bestand exporteren** de knop **Opslaan**.  
4.  Selecteer op de pagina **Exporteren** een bestandslocatie en kies vervolgens de knop **Opslaan**.  

## <a name="to-import-a-workflow"></a>Een werkstroom importeren  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Werkstromen** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Importeren uit bestand**.  
3.  Selecteer op de pagina **Importeren** het XML-bestand dat de werkstroom bevat, en klik vervolgens op **Openen**.  

> [!CAUTION]  
>  Als de werkstroomcode al in de database bestaat, worden de werkstroomstappen overschreven door de stappen in de geïmporteerde werkstroom.  

## <a name="see-also"></a>Zie ook  
 [Werkstromen maken](across-how-to-create-workflows.md)   
 [Werkstromen maken van werkstroomsjablonen](across-how-to-create-workflows-from-workflow-templates.md)   
 [Gearchiveerde instanties van werkstroomstappen bekijken](across-how-to-view-archived-workflow-step-instances.md)   
 [Werkstromen verwijderen](across-how-to-delete-workflows.md)   
 [Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Werkstromen instellen](across-set-up-workflows.md)   
 [Werkstromen gebruiken](across-use-workflows.md)   
 [Werkstroom](across-workflow.md)   
