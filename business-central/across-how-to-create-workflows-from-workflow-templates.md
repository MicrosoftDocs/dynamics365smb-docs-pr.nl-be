---
title: 'Procedure: Werkstromen maken van werkstroomsjablonen | Microsoft Docs'
description: Om tijd te besparen bij het maken van nieuwe werkstromen kunt u werkstromen maken van werkstroomsjablonen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 0ae5a7a308568dd8ede10c485564824685963bf4
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "817082"
---
# <a name="create-workflows-from-workflow-templates"></a><span data-ttu-id="ec731-103">Werkstromen maken van werkstroomsjablonen</span><span class="sxs-lookup"><span data-stu-id="ec731-103">Create Workflows from Workflow Templates</span></span>
<span data-ttu-id="ec731-104">Om tijd te besparen bij het maken van nieuwe werkstromen kunt u werkstromen maken van werkstroomsjablonen.</span><span class="sxs-lookup"><span data-stu-id="ec731-104">To save time when creating new workflows, you can create workflows from workflow templates.</span></span>  

 <span data-ttu-id="ec731-105">Werkstroomsjablonen zijn niet-bewerkbare werkstromen die in de algemene versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] bestaan.</span><span class="sxs-lookup"><span data-stu-id="ec731-105">Workflow templates are non-editable workflows that exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="ec731-106">De codes voor werkstroomsjablonen die door Microsoft worden toegevoegd, hebben het voorvoegsel "MS-".</span><span class="sxs-lookup"><span data-stu-id="ec731-106">The codes for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span>  

 <span data-ttu-id="ec731-107">Een andere manier om snel een werkstroom te maken is een bestaande werkstroom te importeren die u in een bestand buiten [!INCLUDE[d365fin](includes/d365fin_md.md)] hebt.</span><span class="sxs-lookup"><span data-stu-id="ec731-107">Another way to quickly create a workflow is to import an existing workflow that you have on a file outside of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="ec731-108">Zie voor meer informatie [Werkstromen exporteren en importeren](across-how-to-export-and-import-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="ec731-108">For more information, see [Export and Import Workflows](across-how-to-export-and-import-workflows.md).</span></span>  

<span data-ttu-id="ec731-109">Op de pagina **Werkstroom** kunt u een werkstroom maken door de betrokken stappen te vermelden op de regels.</span><span class="sxs-lookup"><span data-stu-id="ec731-109">On the **Workflow** page, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="ec731-110">Elke stap bestaat uit een werkstroomgebeurtenis, aangepast door gebeurtenistoestanden, en een werkstroomantwoord, aangepast door antwoordopties.</span><span class="sxs-lookup"><span data-stu-id="ec731-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="ec731-111">U definieert werkstroomregels door velden op werkstroomregels te vullen vanuit lijsten met vaste gebeurtenis- en reactiewaarden die scenario's vertegenwoordigen die worden ondersteund door de toepassingscode.</span><span class="sxs-lookup"><span data-stu-id="ec731-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="ec731-112">Zie voor meer informatie [Werkstromen maken](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="ec731-112">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-create-a-workflow-from-workflow-template"></a><span data-ttu-id="ec731-113">Een werkstroom maken van een werkstroomsjabloon</span><span class="sxs-lookup"><span data-stu-id="ec731-113">To create a workflow from workflow template</span></span>  
1.  <span data-ttu-id="ec731-114">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Werkstromen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="ec731-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ec731-115">Kies de actie **Werkstroom maken van sjabloon**.</span><span class="sxs-lookup"><span data-stu-id="ec731-115">Choose the **Create Workflow from Template** action.</span></span> <span data-ttu-id="ec731-116">De pagina **Werkstroomsjablonen** verschijnt.</span><span class="sxs-lookup"><span data-stu-id="ec731-116">The **Workflow Templates** page opens.</span></span>  
3.  <span data-ttu-id="ec731-117">Selecteer een werkstroomsjabloon en kies vervolgens de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec731-117">Select a workflow template, and then choose the **OK** button.</span></span>  

     <span data-ttu-id="ec731-118">De pagina **Werkstroom** wordt geopend voor een nieuwe werkstroom die alle gegevens van de geselecteerde sjabloon bevat.</span><span class="sxs-lookup"><span data-stu-id="ec731-118">The **Workflow** page opens for a new workflow containing all the information of the selected template.</span></span> <span data-ttu-id="ec731-119">De waarde in het veld **Code** wordt uitgebreid met bijvoorbeeld '- 01' om aan te geven dat dit de eerste werkstroom is die is gemaakt vanuit de werkstroomsjabloon.</span><span class="sxs-lookup"><span data-stu-id="ec731-119">The value in the **Code** field is extended with, for example, “-01” to indicate that this is the first workflow that is created from the workflow template.</span></span>  
4.  <span data-ttu-id="ec731-120">Ga verder met het maken van de werkstroom door de werkstroomstappen te bewerken of nieuwe stappen toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="ec731-120">Proceed to create the workflow by editing the workflow steps or add new steps.</span></span> <span data-ttu-id="ec731-121">Zie voor meer informatie [Werkstromen maken](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="ec731-121">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="ec731-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ec731-122">See Also</span></span>  
 <span data-ttu-id="ec731-123">[Werkstromen maken](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="ec731-123">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="ec731-124">[Werkstromen exporteren en importeren](across-how-to-export-and-import-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="ec731-124">[Export and Import Workflows](across-how-to-export-and-import-workflows.md) </span></span>  
 <span data-ttu-id="ec731-125">[Gearchiveerde instanties van werkstroomstappen bekijken](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="ec731-125">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="ec731-126">[Werkstromen verwijderen](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="ec731-126">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="ec731-127">[Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="ec731-127">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="ec731-128">[Werkstromen instellen](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="ec731-128">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="ec731-129">[Werkstromen gebruiken](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="ec731-129">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="ec731-130">Werkstroom</span><span class="sxs-lookup"><span data-stu-id="ec731-130">Workflow</span></span>](across-workflow.md)   
