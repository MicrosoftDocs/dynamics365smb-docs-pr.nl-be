---
title: 'Procedure: Werkstromen maken van werkstroomsjablonen | Microsoft Docs'
description: Om tijd te besparen bij het maken van nieuwe werkstromen kunt u werkstromen maken van werkstroomsjablonen.
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: be25518b225b479d5db21b7014817743f28837bd
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="create-workflows-from-workflow-templates"></a><span data-ttu-id="c690d-103">Werkstromen maken van werkstroomsjablonen</span><span class="sxs-lookup"><span data-stu-id="c690d-103">Create Workflows from Workflow Templates</span></span>
<span data-ttu-id="c690d-104">Om tijd te besparen bij het maken van nieuwe werkstromen kunt u werkstromen maken van werkstroomsjablonen.</span><span class="sxs-lookup"><span data-stu-id="c690d-104">To save time when creating new workflows, you can create workflows from workflow templates.</span></span>  

 <span data-ttu-id="c690d-105">Werkstroomsjablonen zijn niet-bewerkbare werkstromen die in de algemene versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] bestaan.</span><span class="sxs-lookup"><span data-stu-id="c690d-105">Workflow templates are non-editable workflows that exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c690d-106">De codes voor werkstroomsjablonen die door Microsoft worden toegevoegd, hebben het voorvoegsel "MS-".</span><span class="sxs-lookup"><span data-stu-id="c690d-106">The codes for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span>  

 <span data-ttu-id="c690d-107">Een andere manier om snel een werkstroom te maken is een bestaande werkstroom te importeren die u in een bestand buiten [!INCLUDE[d365fin](includes/d365fin_md.md)] hebt.</span><span class="sxs-lookup"><span data-stu-id="c690d-107">Another way to quickly create a workflow is to import an existing workflow that you have on a file outside of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="c690d-108">Zie voor meer informatie [Werkstromen exporteren en importeren](across-how-to-export-and-import-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="c690d-108">For more information, see [Export and Import Workflows](across-how-to-export-and-import-workflows.md).</span></span>  

<span data-ttu-id="c690d-109">In het venster **Werkstroom** kunt u een werkstroom maken door de betrokken stappen te vermelden op de regels.</span><span class="sxs-lookup"><span data-stu-id="c690d-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="c690d-110">Elke stap bestaat uit een werkstroomgebeurtenis, aangepast door gebeurtenistoestanden, en een werkstroomantwoord, aangepast door antwoordopties.</span><span class="sxs-lookup"><span data-stu-id="c690d-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="c690d-111">U definieert werkstroomregels door velden op werkstroomregels te vullen vanuit lijsten met vaste gebeurtenis- en reactiewaarden die scenario's vertegenwoordigen die worden ondersteund door de toepassingscode.</span><span class="sxs-lookup"><span data-stu-id="c690d-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="c690d-112">Zie voor meer informatie [Werkstromen maken](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="c690d-112">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-create-a-workflow-from-workflow-template"></a><span data-ttu-id="c690d-113">Een werkstroom maken van een werkstroomsjabloon</span><span class="sxs-lookup"><span data-stu-id="c690d-113">To create a workflow from workflow template</span></span>  
1.  <span data-ttu-id="c690d-114">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Werkstromen** in en klik op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="c690d-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c690d-115">Kies de actie **Werkstroom maken van sjabloon**.</span><span class="sxs-lookup"><span data-stu-id="c690d-115">Choose the **Create Workflow from Template** action.</span></span> <span data-ttu-id="c690d-116">Het venster **Werkstroomsjablonen** verschijnt.</span><span class="sxs-lookup"><span data-stu-id="c690d-116">The **Workflow Templates** window opens.</span></span>  
3.  <span data-ttu-id="c690d-117">Selecteer een werkstroomsjabloon en kies vervolgens de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="c690d-117">Select a workflow template, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="c690d-118">Het venster **Werkstroom** wordt geopend voor een nieuwe werkstroom die alle gegevens van de geselecteerde sjabloon bevat.</span><span class="sxs-lookup"><span data-stu-id="c690d-118">The **Workflow** window opens for a new workflow containing all the information of the selected template.</span></span> <span data-ttu-id="c690d-119">De waarde in het veld **Code** wordt uitgebreid met bijvoorbeeld '- 01' om aan te geven dat dit de eerste werkstroom is die is gemaakt vanuit de werkstroomsjabloon.</span><span class="sxs-lookup"><span data-stu-id="c690d-119">The value in the **Code** field is extended with, for example, “-01” to indicate that this is the first workflow that is created from the workflow template.</span></span>  
4.  <span data-ttu-id="c690d-120">Ga verder met het maken van de werkstroom door de werkstroomstappen te bewerken of nieuwe stappen toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="c690d-120">Proceed to create the workflow by editing the workflow steps or add new steps.</span></span> <span data-ttu-id="c690d-121">Zie voor meer informatie [Werkstromen maken](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="c690d-121">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="c690d-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c690d-122">See Also</span></span>  
 <span data-ttu-id="c690d-123">[Werkstromen maken](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="c690d-123">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="c690d-124">[Werkstromen exporteren en importeren](across-how-to-export-and-import-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="c690d-124">[Export and Import Workflows](across-how-to-export-and-import-workflows.md) </span></span>  
 <span data-ttu-id="c690d-125">[Gearchiveerde instanties van werkstroomstappen bekijken](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="c690d-125">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="c690d-126">[Werkstromen verwijderen](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="c690d-126">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="c690d-127">[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="c690d-127">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="c690d-128">[Werkstromen instellen](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="c690d-128">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="c690d-129">[Werkstromen gebruiken](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="c690d-129">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="c690d-130">Werkstroom</span><span class="sxs-lookup"><span data-stu-id="c690d-130">Workflow</span></span>](across-workflow.md)   

