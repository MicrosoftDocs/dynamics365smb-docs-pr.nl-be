---
title: Werkstromen gebruiken
description: U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd. Lees meer over de verschillende stappen die u moet nemen om werkstromen te gaan gebruiken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fc2917a304a5a43228f9156dffd0a9a8011f9047
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378910"
---
# <a name="using-workflows"></a><span data-ttu-id="391b9-104">Werkstromen gebruiken</span><span class="sxs-lookup"><span data-stu-id="391b9-104">Using Workflows</span></span>
<span data-ttu-id="391b9-105">U kunt werkstromen instellen en gebruiken om bedrijfsprocestaken te verbinden die door verschillende gebruikers worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="391b9-105">You can set up and use workflows that connect business-process tasks performed by different users.</span></span> <span data-ttu-id="391b9-106">Systeemtaken, zoals automatische boekingen, kunnen als stappen in werkstromen worden opgenomen, die worden voorafgegaan of gevolgd door gebruikerstaken.</span><span class="sxs-lookup"><span data-stu-id="391b9-106">System tasks, such as automatic posting, can be included as steps in workflows, preceded or followed by user tasks.</span></span> <span data-ttu-id="391b9-107">Het aanvragen en verlenen van goedkeuringen om nieuwe records te maken, zijn voorbeelden van veelvoorkomende werkstroomstappen.</span><span class="sxs-lookup"><span data-stu-id="391b9-107">Requesting and granting approval to create new records are typical workflow steps.</span></span>  

 <span data-ttu-id="391b9-108">Voordat u kunt beginnen met werkstromen gebruiken, moet u de werkstroomgebruikers instellen, werkstromen maken, mogelijk de code aanpassen en opgeven hoe gebruikers berichten ontvangen.</span><span class="sxs-lookup"><span data-stu-id="391b9-108">Before you can begin to use workflows, you must set up workflow users, create the workflows, potentially preceded by code customization and specify how users receive notifications.</span></span> <span data-ttu-id="391b9-109">Zie voor meer informatie [Werkstromen instellen](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="391b9-109">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="391b9-110">Veelvoorkomende werkstroomstappen gaan over gebruikers die goedkeuring aanvragen voor taken, en fiatteurs die goedkeuringsaanvragen accepteren of afwijzen.</span><span class="sxs-lookup"><span data-stu-id="391b9-110">Typical workflow steps are about users who request approval of tasks and approvers accepting or rejecting approval requests.</span></span> <span data-ttu-id="391b9-111">Daarom verwijzen veel onderwerpen over het gebruik van werkstromen naar goedkeuringen.</span><span class="sxs-lookup"><span data-stu-id="391b9-111">Therefore, many topics about how to use workflows refer to approvals.</span></span>  

 <span data-ttu-id="391b9-112">In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.</span><span class="sxs-lookup"><span data-stu-id="391b9-112">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

|<span data-ttu-id="391b9-113">**Als u dit wilt doen**</span><span class="sxs-lookup"><span data-stu-id="391b9-113">**To**</span></span>|<span data-ttu-id="391b9-114">**Onderwerp**</span><span class="sxs-lookup"><span data-stu-id="391b9-114">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="391b9-115">Stel in dat een werkstroom start wanneer de eerste invoerpuntgebeurtenis plaatsvindt.</span><span class="sxs-lookup"><span data-stu-id="391b9-115">Set a workflow to start when the first entry-point event occurs.</span></span>|[<span data-ttu-id="391b9-116">Werkstromen inschakelen</span><span class="sxs-lookup"><span data-stu-id="391b9-116">Enable Workflows</span></span>](across-how-to-enable-workflows.md)|  
|<span data-ttu-id="391b9-117">Vraag goedkeuring van een taak aan, als fiatteur, accepteer, weiger of delegeer goedkeuringen en verzend of bekijk goedkeuringsberichten.</span><span class="sxs-lookup"><span data-stu-id="391b9-117">Request approval of a task, as an approver, accept, decline, or delegate approvals, and send or view approval notifications.</span></span>|[<span data-ttu-id="391b9-118">Goedkeuringswerkstromen gebruiken</span><span class="sxs-lookup"><span data-stu-id="391b9-118">Use Approval Workflows</span></span>](across-how-use-approval-workflows.md)|  
|<span data-ttu-id="391b9-119">Maak werkstroomstappen die voorkomen dat een bepaald recordtype wordt gebruikt voordat een bepaalde gebeurtenis plaatsvindt, bijvoorbeeld de goedkeuring van de record.</span><span class="sxs-lookup"><span data-stu-id="391b9-119">Create workflow steps that restrict a certain record type from being used before a certain event occurs, for example that the record is approved.</span></span>|[<span data-ttu-id="391b9-120">Gebruik van een record beperken en toestaan</span><span class="sxs-lookup"><span data-stu-id="391b9-120">Restrict and Allow Usage of a Record</span></span>](across-how-to-restrict-and-allow-usage-of-a-record.md)|  
|<span data-ttu-id="391b9-121">Geef instanties van werkstroomstappen met de status Voltooid weer.</span><span class="sxs-lookup"><span data-stu-id="391b9-121">View workflow step instances of status Completed.</span></span>|[<span data-ttu-id="391b9-122">Gearchiveerde instanties van werkstroomstappen bekijken</span><span class="sxs-lookup"><span data-stu-id="391b9-122">View Archived Workflow Step Instances</span></span>](across-how-to-view-archived-workflow-step-instances.md)|  
|<span data-ttu-id="391b9-123">Verwijder een werkstroom als u zeker weet dat u die niet meer gebruikt.</span><span class="sxs-lookup"><span data-stu-id="391b9-123">Delete a workflow that you are sure will no longer be used.</span></span>|[<span data-ttu-id="391b9-124">Werkstromen verwijderen</span><span class="sxs-lookup"><span data-stu-id="391b9-124">Delete Workflows</span></span>](across-how-to-delete-workflows.md)|  

## <a name="see-also"></a><span data-ttu-id="391b9-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="391b9-125">See Also</span></span>  
<span data-ttu-id="391b9-126">[Werkstromen instellen](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="391b9-126">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
<span data-ttu-id="391b9-127">[Werkstroom](across-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="391b9-127">[Workflow](across-workflow.md) </span></span>  
<span data-ttu-id="391b9-128">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="391b9-128">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]