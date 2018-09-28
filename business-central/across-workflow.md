---
title: Werkstroom | Microsoft Docs
description: U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd. Systeemtaken, zoals automatische boekingen, kunnen als stappen in werkstromen worden opgenomen, die worden voorafgegaan of gevolgd door gebruikerstaken. Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen.
services: project-madeira
documentationcenter: 
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
ms.openlocfilehash: 7a7782fcb51eb9078cb62c4892814cd178518332
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="workflow"></a><span data-ttu-id="caefc-105">Werkstroom</span><span class="sxs-lookup"><span data-stu-id="caefc-105">Workflow</span></span>
<span data-ttu-id="caefc-106">U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="caefc-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="caefc-107">Systeemtaken, zoals automatische boekingen, kunnen als stappen in werkstromen worden opgenomen, die worden voorafgegaan of gevolgd door gebruikerstaken.</span><span class="sxs-lookup"><span data-stu-id="caefc-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="caefc-108">Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen.</span><span class="sxs-lookup"><span data-stu-id="caefc-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="caefc-109">In het venster **Werkstroom** kunt u een werkstroom maken door de betrokken stappen te vermelden op de regels.</span><span class="sxs-lookup"><span data-stu-id="caefc-109">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="caefc-110">Elke stap bestaat uit een werkstroomgebeurtenis, aangepast door gebeurtenistoestanden, en een werkstroomantwoord, aangepast door antwoordopties.</span><span class="sxs-lookup"><span data-stu-id="caefc-110">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="caefc-111">U definieert werkstroomregels door velden op werkstroomregels te vullen vanuit lijsten met vaste gebeurtenis- en reactiewaarden die scenario's vertegenwoordigen die worden ondersteund door de toepassingscode.</span><span class="sxs-lookup"><span data-stu-id="caefc-111">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span>  

 <span data-ttu-id="caefc-112">De algemene versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] bevat een aantal vooraf geconfigureerde werkstromen die worden vertegenwoordigd door werkstroomsjablonen die u kunt kopiëren om werkstromen te maken.</span><span class="sxs-lookup"><span data-stu-id="caefc-112">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] includes a number of preconfigured workflows represented by workflow templates that you can copy to create workflows.</span></span> <span data-ttu-id="caefc-113">De code voor werkstroomsjablonen die door Microsoft worden toegevoegd, heeft het voorvoegsel "MS-".</span><span class="sxs-lookup"><span data-stu-id="caefc-113">The code for workflow templates that are added by Microsoft are prefixed with “MS-“.</span></span> <span data-ttu-id="caefc-114">Zie voor meer informatie de lijst met werkstroomsjablonen in het venster Werkstroomsjablonen venster.</span><span class="sxs-lookup"><span data-stu-id="caefc-114">For more information, see the list of workflow templates in the Workflow Templates window.</span></span>  

 <span data-ttu-id="caefc-115">Als een bedrijfsscenario een werkstroomgebeurtenis of -reactie vereist die niet wordt ondersteund, moet een Microsoft-partner ze implementeren door de toepassingscode aan te passen.</span><span class="sxs-lookup"><span data-stu-id="caefc-115">If a business scenario requires a workflow event or response that is not supported, a Microsoft partner must implement them by customizing the application code.</span></span> <span data-ttu-id="caefc-116">Raadpleeg [Procedure: Nieuwe werkstroomgebeurtenissen en -reacties implementeren](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) in de Help voor ontwikkelaars en IT-professionals voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="caefc-116">For more information, see [Walkthrough: Implementing New Workflow Events and Responses](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) in the developer and IT-pro help.</span></span>

> [!NOTE]  
> <span data-ttu-id="caefc-117">Werkstromen kunnen ook worden gestart vanuit Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="caefc-117">Workflows can also be initiated from Microsoft Flow.</span></span> <span data-ttu-id="caefc-118">Zie voor meer informatie [Business Central gebruiken in een geautomatiseerde werkstroom](across-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="caefc-118">For more information, see [Using Business Central in an Automated Workflow](across-how-use-financials-data-source-flow.md).</span></span>  

 <span data-ttu-id="caefc-119">In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.</span><span class="sxs-lookup"><span data-stu-id="caefc-119">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="caefc-120">**Als u dit wilt doen**</span><span class="sxs-lookup"><span data-stu-id="caefc-120">**To**</span></span>|<span data-ttu-id="caefc-121">**Onderwerp**</span><span class="sxs-lookup"><span data-stu-id="caefc-121">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="caefc-122">Gebruikers van werkstromen instellen, opgeven hoe gebruikers berichten krijgen en nieuwe werkstromen maken.</span><span class="sxs-lookup"><span data-stu-id="caefc-122">Set up workflow users, specify how users get notified, and create new workflows.</span></span> <span data-ttu-id="caefc-123">Voor nieuwe werkstromen voor niet-ondersteunde scenario's implementeert u de vereiste workflowelementen door de toepassingcode aan te passen.</span><span class="sxs-lookup"><span data-stu-id="caefc-123">For new workflows for unsupported scenarios, implement the required workflow elements by customizing the application code.</span></span>|[<span data-ttu-id="caefc-124">Werkstromen instellen</span><span class="sxs-lookup"><span data-stu-id="caefc-124">Setting Up Workflows</span></span>](across-set-up-workflows.md)|  
|<span data-ttu-id="caefc-125">Werkstromen inschakelen, reageren op werkstroomberichten, inclusief goedkeuringen aanvragen en aanvragen goedkeuren om een werkstroomstap uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="caefc-125">Enable workflows, act on workflow notifications, including request approvals and approve requests to perform a workflow step.</span></span> <span data-ttu-id="caefc-126">Werkstromen archiveren en verwijderen.</span><span class="sxs-lookup"><span data-stu-id="caefc-126">Archive and delete workflows.</span></span>|[<span data-ttu-id="caefc-127">Werkstromen gebruiken</span><span class="sxs-lookup"><span data-stu-id="caefc-127">Using Workflows</span></span>](across-use-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="caefc-128">Zie ook</span><span class="sxs-lookup"><span data-stu-id="caefc-128">See Also</span></span>  
[<span data-ttu-id="caefc-129">Verkoop</span><span class="sxs-lookup"><span data-stu-id="caefc-129">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="caefc-130">Inkoop</span><span class="sxs-lookup"><span data-stu-id="caefc-130">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="caefc-131">Projecten beheren</span><span class="sxs-lookup"><span data-stu-id="caefc-131">Managing Projects</span></span>](projects-manage-projects.md)  
<span data-ttu-id="caefc-132">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="caefc-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

