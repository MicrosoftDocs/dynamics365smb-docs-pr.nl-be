---
title: Werkstromen gebruiken | Microsoft Docs
description: U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd. Systeemtaken, zoals automatische boekingen, kunnen als stappen in werkstromen worden opgenomen, die worden voorafgegaan of gevolgd door gebruikerstaken. Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e5dee76fa49d66d72c7e20cb9ff5eead63cf37aa
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "928358"
---
# <a name="using-workflows"></a><span data-ttu-id="8aa45-105">Werkstromen gebruiken</span><span class="sxs-lookup"><span data-stu-id="8aa45-105">Using Workflows</span></span>
<span data-ttu-id="8aa45-106">U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="8aa45-106">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="8aa45-107">Systeemtaken, zoals automatische boekingen, kunnen als stappen in werkstromen worden opgenomen, die worden voorafgegaan of gevolgd door gebruikerstaken.</span><span class="sxs-lookup"><span data-stu-id="8aa45-107">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="8aa45-108">Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen.</span><span class="sxs-lookup"><span data-stu-id="8aa45-108">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="8aa45-109">Voordat u kunt beginnen met werkstromen gebruiken, moet u de werkstroomgebruikers instellen, werkstromen maken, mogelijk de code aanpassen en opgeven hoe gebruikers berichten ontvangen.</span><span class="sxs-lookup"><span data-stu-id="8aa45-109">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="8aa45-110">Zie voor meer informatie [Werkstromen instellen](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="8aa45-110">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="8aa45-111">Veelvoorkomende werkstroomstappen gaan over gebruikers die goedkeuring aanvragen voor taken, en fiatteurs die goedkeuringsaanvragen accepteren of afwijzen.</span><span class="sxs-lookup"><span data-stu-id="8aa45-111">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="8aa45-112">Daarom verwijzen veel onderwerpen over het gebruik van werkstromen naar goedkeuringen.</span><span class="sxs-lookup"><span data-stu-id="8aa45-112">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="8aa45-113">In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.</span><span class="sxs-lookup"><span data-stu-id="8aa45-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="8aa45-114">**Als u dit wilt doen**</span><span class="sxs-lookup"><span data-stu-id="8aa45-114">**To**</span></span>|<span data-ttu-id="8aa45-115">**Onderwerp**</span><span class="sxs-lookup"><span data-stu-id="8aa45-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="8aa45-116">Stel in dat een werkstroom start wanneer de eerste invoerpuntgebeurtenis plaatsvindt.</span><span class="sxs-lookup"><span data-stu-id="8aa45-116">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="8aa45-117">Werkstromen inschakelen</span><span class="sxs-lookup"><span data-stu-id="8aa45-117">Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="8aa45-118">Vraag goedkeuring van een taak aan, als fiatteur, accepteer, weiger of delegeer goedkeuringen en verzend of bekijk goedkeuringsberichten.</span><span class="sxs-lookup"><span data-stu-id="8aa45-118">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="8aa45-119">Goedkeuringswerkstromen gebruiken</span><span class="sxs-lookup"><span data-stu-id="8aa45-119">Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="8aa45-120">Maak werkstroomstappen die voorkomen dat een bepaald recordtype wordt gebruikt voordat een bepaalde gebeurtenis plaatsvindt, bijvoorbeeld de goedkeuring van de record.</span><span class="sxs-lookup"><span data-stu-id="8aa45-120">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="8aa45-121">Gebruik van een record beperken en toestaan</span><span class="sxs-lookup"><span data-stu-id="8aa45-121">Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="8aa45-122">Geef instanties van werkstroomstappen met de status Voltooid weer.</span><span class="sxs-lookup"><span data-stu-id="8aa45-122">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="8aa45-123">Gearchiveerde instanties van werkstroomstappen bekijken</span><span class="sxs-lookup"><span data-stu-id="8aa45-123">View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="8aa45-124">Verwijder een werkstroom als u zeker weet dat u die niet meer gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8aa45-124">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="8aa45-125">Werkstromen verwijderen</span><span class="sxs-lookup"><span data-stu-id="8aa45-125">Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="8aa45-126">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8aa45-126">See Also</span></span>  
<span data-ttu-id="8aa45-127">[Werkstromen instellen](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="8aa45-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="8aa45-128">[Werkstroom](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="8aa45-128">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="8aa45-129">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8aa45-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
