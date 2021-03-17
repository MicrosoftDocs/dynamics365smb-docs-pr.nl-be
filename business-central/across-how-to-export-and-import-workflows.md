---
title: Werkstromen exporteren en importeren | Microsoft Docs
description: Als u werkstromen wilt overbrengen naar andere Business Central-databases, bijvoorbeeld om tijd te besparen wanneer u nieuwe werkstromen maakt, kunt u werkstromen exporteren en importeren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6f47b137a2915f790b510c0fd66944a4fe7814ca
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384436"
---
# <a name="export-and-import-workflows"></a><span data-ttu-id="e52ae-103">Werkstromen exporteren en importeren</span><span class="sxs-lookup"><span data-stu-id="e52ae-103">Export and Import Workflows</span></span>
<span data-ttu-id="e52ae-104">Als u werkstromen wilt overbrengen naar andere [!INCLUDE[prod_short](includes/prod_short.md)]-databases, bijvoorbeeld om tijd te besparen wanneer u nieuwe werkstromen maakt, kunt u werkstromen exporteren en importeren.</span><span class="sxs-lookup"><span data-stu-id="e52ae-104">To transfer workflows to other [!INCLUDE[prod_short](includes/prod_short.md)] databases, for example to save time when creating new workflows, you can export and import workflows.</span></span>  

 <span data-ttu-id="e52ae-105">Een andere manier om werkstromen snel te maken is werkstromen te maken van werkstroomsjablonen.</span><span class="sxs-lookup"><span data-stu-id="e52ae-105">Another way to quickly create workflows is to create workflows from workflow templates.</span></span> <span data-ttu-id="e52ae-106">Zie voor meer informatie [Werkstromen maken van werkstroomsjablonen](across-how-to-create-workflows-from-workflow-templates.md).</span><span class="sxs-lookup"><span data-stu-id="e52ae-106">For more information, see [Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md).</span></span>  

 <span data-ttu-id="e52ae-107">Op de pagina **Werkstroom** kunt u een werkstroom maken door de betrokken stappen te vermelden op de regels.</span><span class="sxs-lookup"><span data-stu-id="e52ae-107">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="e52ae-108">Elke stap bestaat uit een werkstroomgebeurtenis, aangepast door gebeurtenistoestanden, en een werkstroomantwoord, aangepast door antwoordopties.</span><span class="sxs-lookup"><span data-stu-id="e52ae-108">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="e52ae-109">U definieert werkstroomregels door velden op werkstroomregels te vullen vanuit lijsten met vaste gebeurtenis- en reactiewaarden die scenario's vertegenwoordigen die worden ondersteund door de toepassingscode.</span><span class="sxs-lookup"><span data-stu-id="e52ae-109">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="e52ae-110">Zie voor meer informatie [Werkstromen maken](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="e52ae-110">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-export-a-workflow"></a><span data-ttu-id="e52ae-111">Een werkstroom exporteren</span><span class="sxs-lookup"><span data-stu-id="e52ae-111">To export a workflow</span></span>  
1.  <span data-ttu-id="e52ae-112">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Werkstromen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="e52ae-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e52ae-113">Selecteer een werkstroom en kies de actie **Exporteren naar bestand**.</span><span class="sxs-lookup"><span data-stu-id="e52ae-113">Select a workflow, and then choose the **Export to File** action.</span></span>  
3.  <span data-ttu-id="e52ae-114">Kies op de pagina **Bestand exporteren** de knop **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e52ae-114">On the **Export File** page, choose the **Save** button.</span></span>  
4.  <span data-ttu-id="e52ae-115">Selecteer op de pagina **Exporteren** een bestandslocatie en kies vervolgens de knop **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e52ae-115">On the **Export** page, select a file location, and then choose the **Save** button.</span></span>  

## <a name="to-import-a-workflow"></a><span data-ttu-id="e52ae-116">Een werkstroom importeren</span><span class="sxs-lookup"><span data-stu-id="e52ae-116">To import a workflow</span></span>  
1.  <span data-ttu-id="e52ae-117">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Werkstromen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="e52ae-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e52ae-118">Kies de actie **Importeren uit bestand**.</span><span class="sxs-lookup"><span data-stu-id="e52ae-118">Choose the **Import from File** action.</span></span>  
3.  <span data-ttu-id="e52ae-119">Selecteer op de pagina **Importeren** het XML-bestand dat de werkstroom bevat, en klik vervolgens op **Openen**.</span><span class="sxs-lookup"><span data-stu-id="e52ae-119">On the **Import** page, choose the XML file that contains the workflow, and then choose the **Open** button.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="e52ae-120">Als de werkstroomcode al in de database bestaat, worden de werkstroomstappen overschreven door de stappen in de geïmporteerde werkstroom.</span><span class="sxs-lookup"><span data-stu-id="e52ae-120">If the workflow code already exists in the database, the workflow steps will be overwritten with the steps in the imported workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e52ae-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e52ae-121">See Also</span></span>  
 <span data-ttu-id="e52ae-122">[Werkstromen maken](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="e52ae-122">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="e52ae-123">[Werkstromen maken van werkstroomsjablonen](across-how-to-create-workflows-from-workflow-templates.md) </span><span class="sxs-lookup"><span data-stu-id="e52ae-123">[Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md) </span></span>  
 <span data-ttu-id="e52ae-124">[Gearchiveerde instanties van werkstroomstappen bekijken](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="e52ae-124">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="e52ae-125">[Werkstromen verwijderen](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="e52ae-125">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="e52ae-126">[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="e52ae-126">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="e52ae-127">[Werkstromen instellen](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="e52ae-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="e52ae-128">[Werkstromen gebruiken](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="e52ae-128">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="e52ae-129">Werkstroom</span><span class="sxs-lookup"><span data-stu-id="e52ae-129">Workflow</span></span>](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]