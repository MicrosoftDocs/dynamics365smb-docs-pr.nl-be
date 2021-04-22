---
title: 'Procedure: Werkstromen maken van werkstroomsjablonen | Microsoft Docs'
description: Om tijd te besparen bij het maken van nieuwe werkstromen kunt u werkstromen maken van werkstroomsjablonen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 2540632936a502cd1873c7db34733f5dd83db4b9
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775859"
---
# <a name="create-workflows-from-workflow-templates"></a><span data-ttu-id="d63a0-103">Werkstromen maken van werkstroomsjablonen</span><span class="sxs-lookup"><span data-stu-id="d63a0-103">Create Workflows from Workflow Templates</span></span>
<span data-ttu-id="d63a0-104">Om tijd te besparen bij het maken van nieuwe werkstromen kunt u werkstromen maken van werkstroomsjablonen.</span><span class="sxs-lookup"><span data-stu-id="d63a0-104">To save time when creating new workflows, you can create workflows from workflow templates.</span></span>  

 <span data-ttu-id="d63a0-105">Werkstroomsjablonen zijn niet-bewerkbare werkstromen die in de algemene versie van [!INCLUDE[prod_short](includes/prod_short.md)] bestaan.</span><span class="sxs-lookup"><span data-stu-id="d63a0-105">Workflow templates are non-editable workflows that exist in the generic version of [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="d63a0-106">De codes voor werkstroomsjablonen die door Microsoft worden toegevoegd, hebben het voorvoegsel "MS-".</span><span class="sxs-lookup"><span data-stu-id="d63a0-106">The codes for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span>  

 <span data-ttu-id="d63a0-107">Een andere manier om snel een werkstroom te maken is een bestaande werkstroom te importeren die u in een bestand buiten [!INCLUDE[prod_short](includes/prod_short.md)] hebt.</span><span class="sxs-lookup"><span data-stu-id="d63a0-107">Another way to quickly create a workflow is to import an existing workflow that you have on a file outside of [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="d63a0-108">Zie voor meer informatie [Werkstromen exporteren en importeren](across-how-to-export-and-import-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="d63a0-108">For more information, see [Export and Import Workflows](across-how-to-export-and-import-workflows.md).</span></span>  

<span data-ttu-id="d63a0-109">Op de pagina **Werkstroom** kunt u een werkstroom maken door de betrokken stappen te vermelden op de regels.</span><span class="sxs-lookup"><span data-stu-id="d63a0-109">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="d63a0-110">Elke stap bestaat uit een werkstroomgebeurtenis, aangepast door gebeurtenistoestanden, en een werkstroomantwoord, aangepast door antwoordopties.</span><span class="sxs-lookup"><span data-stu-id="d63a0-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="d63a0-111">U definieert werkstroomregels door velden op werkstroomregels te vullen vanuit lijsten met vaste gebeurtenis- en reactiewaarden die scenario's vertegenwoordigen die worden ondersteund door de toepassingscode.</span><span class="sxs-lookup"><span data-stu-id="d63a0-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="d63a0-112">Zie voor meer informatie [Werkstromen maken](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="d63a0-112">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-create-a-workflow-from-workflow-template"></a><span data-ttu-id="d63a0-113">Een werkstroom maken van een werkstroomsjabloon</span><span class="sxs-lookup"><span data-stu-id="d63a0-113">To create a workflow from workflow template</span></span>  
1.  <span data-ttu-id="d63a0-114">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Werkstromen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="d63a0-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="d63a0-115">Kies de actie **Werkstroom maken van sjabloon**.</span><span class="sxs-lookup"><span data-stu-id="d63a0-115">Choose the **Create Workflow from Template** action.</span></span> <span data-ttu-id="d63a0-116">De pagina **Werkstroomsjablonen** verschijnt.</span><span class="sxs-lookup"><span data-stu-id="d63a0-116">The **Workflow Templates** page opens.</span></span>  
3.  <span data-ttu-id="d63a0-117">Selecteer een werkstroomsjabloon en kies vervolgens de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="d63a0-117">Select a workflow template, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="d63a0-118">De pagina **Werkstroom** wordt geopend voor een nieuwe werkstroom die alle gegevens van de geselecteerde sjabloon bevat.</span><span class="sxs-lookup"><span data-stu-id="d63a0-118">The **Workflow** page opens for a new workflow containing all the information of the selected template.</span></span> <span data-ttu-id="d63a0-119">De waarde in het veld **Code** wordt uitgebreid met bijvoorbeeld '- 01' om aan te geven dat dit de eerste werkstroom is die is gemaakt vanuit de werkstroomsjabloon.</span><span class="sxs-lookup"><span data-stu-id="d63a0-119">The value in the **Code** field is extended with, for example, “-01” to indicate that this is the first workflow that is created from the workflow template.</span></span>  
4.  <span data-ttu-id="d63a0-120">Ga verder met het maken van de werkstroom door de werkstroomstappen te bewerken of nieuwe stappen toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="d63a0-120">Proceed to create the workflow by editing the workflow steps or add new steps.</span></span> <span data-ttu-id="d63a0-121">Zie voor meer informatie [Werkstromen maken](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="d63a0-121">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="d63a0-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d63a0-122">See Also</span></span>  
 <span data-ttu-id="d63a0-123">[Werkstromen maken](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d63a0-123">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="d63a0-124">[Werkstromen exporteren en importeren](across-how-to-export-and-import-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d63a0-124">[Export and Import Workflows](across-how-to-export-and-import-workflows.md) </span></span>  
 <span data-ttu-id="d63a0-125">[Gearchiveerde instanties van werkstroomstappen bekijken](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="d63a0-125">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="d63a0-126">[Werkstromen verwijderen](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d63a0-126">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="d63a0-127">[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="d63a0-127">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="d63a0-128">[Werkstromen instellen](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d63a0-128">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="d63a0-129">[Werkstromen gebruiken](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d63a0-129">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="d63a0-130">Werkstroom</span><span class="sxs-lookup"><span data-stu-id="d63a0-130">Workflow</span></span>](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]