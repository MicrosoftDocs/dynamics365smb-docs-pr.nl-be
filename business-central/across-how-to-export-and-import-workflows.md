---
title: Werkstromen exporteren en importeren | Microsoft Docs
description: Als u werkstromen wilt overbrengen naar andere Business Central-databases, bijvoorbeeld om tijd te besparen wanneer u nieuwe werkstromen maakt, kunt u werkstromen exporteren en importeren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 579a2ab10eefd5e706dfa5f686702ac780764578
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="export-and-import-workflows"></a><span data-ttu-id="50237-103">Werkstromen exporteren en importeren</span><span class="sxs-lookup"><span data-stu-id="50237-103">Export and Import Workflows</span></span>
<span data-ttu-id="50237-104">Als u werkstromen wilt overbrengen naar andere [!INCLUDE[d365fin](includes/d365fin_md.md)]-databases, bijvoorbeeld om tijd te besparen wanneer u nieuwe werkstromen maakt, kunt u werkstromen exporteren en importeren.</span><span class="sxs-lookup"><span data-stu-id="50237-104">To transfer workflows to other [!INCLUDE[d365fin](includes/d365fin_md.md)] databases, for example to save time when creating new workflows, you can export and import workflows.</span></span>  

 <span data-ttu-id="50237-105">Een andere manier om werkstromen snel te maken is werkstromen te maken van werkstroomsjablonen.</span><span class="sxs-lookup"><span data-stu-id="50237-105">Another way to quickly create workflows is to create workflows from workflow templates.</span></span> <span data-ttu-id="50237-106">Zie voor meer informatie [Werkstromen maken van werkstroomsjablonen](across-how-to-create-workflows-from-workflow-templates.md).</span><span class="sxs-lookup"><span data-stu-id="50237-106">For more information, see [Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md).</span></span>  

 <span data-ttu-id="50237-107">In het venster **Werkstroom** kunt u een werkstroom maken door de betrokken stappen te vermelden op de regels.</span><span class="sxs-lookup"><span data-stu-id="50237-107">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="50237-108">Elke stap bestaat uit een werkstroomgebeurtenis, aangepast door gebeurtenistoestanden, en een werkstroomantwoord, aangepast door antwoordopties.</span><span class="sxs-lookup"><span data-stu-id="50237-108">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="50237-109">U definieert werkstroomregels door velden op werkstroomregels te vullen vanuit lijsten met vaste gebeurtenis- en reactiewaarden die scenario's vertegenwoordigen die worden ondersteund door de toepassingscode.</span><span class="sxs-lookup"><span data-stu-id="50237-109">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="50237-110">Zie voor meer informatie [Werkstromen maken](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="50237-110">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-export-a-workflow"></a><span data-ttu-id="50237-111">Een werkstroom exporteren</span><span class="sxs-lookup"><span data-stu-id="50237-111">To export a workflow</span></span>  
1.  <span data-ttu-id="50237-112">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Werkstromen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="50237-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="50237-113">Selecteer een werkstroom en kies de actie **Exporteren naar bestand**.</span><span class="sxs-lookup"><span data-stu-id="50237-113">Select a workflow, and then choose the **Export to File** action.</span></span>  
3.  <span data-ttu-id="50237-114">Kies in het venster **Bestand exporteren** de knop **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="50237-114">In the **Export File** window, choose the **Save** button.</span></span>  
4.  <span data-ttu-id="50237-115">Selecteer in het venster **Exporteren** een bestandslocatie en kies vervolgens de knop **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="50237-115">In the **Export** window, select a file location, and then choose the **Save** button.</span></span>  

## <a name="to-import-a-workflow"></a><span data-ttu-id="50237-116">Een werkstroom importeren</span><span class="sxs-lookup"><span data-stu-id="50237-116">To import a workflow</span></span>  
1.  <span data-ttu-id="50237-117">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Werkstromen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="50237-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="50237-118">Kies de actie **Importeren uit bestand**.</span><span class="sxs-lookup"><span data-stu-id="50237-118">Choose the **Import from File** action.</span></span>  
3.  <span data-ttu-id="50237-119">Selecteer in het venster **Importeren** het XML-bestand dat de werkstroom bevat, en klik vervolgens op **Openen**.</span><span class="sxs-lookup"><span data-stu-id="50237-119">In the **Import** window, choose the XML file that contains the workflow, and then choose the **Open** button.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="50237-120">Als de werkstroomcode al in de database bestaat, worden de werkstroomstappen overschreven door de stappen in de geïmporteerde werkstroom.</span><span class="sxs-lookup"><span data-stu-id="50237-120">If the workflow code already exists in the database, the workflow steps will be overwritten with the steps in the imported workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="50237-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="50237-121">See Also</span></span>  
 <span data-ttu-id="50237-122">[Werkstromen maken](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="50237-122">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="50237-123">[Werkstromen maken van werkstroomsjablonen](across-how-to-create-workflows-from-workflow-templates.md) </span><span class="sxs-lookup"><span data-stu-id="50237-123">[Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md) </span></span>  
 <span data-ttu-id="50237-124">[Gearchiveerde instanties van werkstroomstappen bekijken](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="50237-124">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="50237-125">[Werkstromen verwijderen](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="50237-125">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="50237-126">[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="50237-126">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="50237-127">[Werkstromen instellen](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="50237-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="50237-128">[Werkstromen gebruiken](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="50237-128">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="50237-129">Werkstroom</span><span class="sxs-lookup"><span data-stu-id="50237-129">Workflow</span></span>](across-workflow.md)   

