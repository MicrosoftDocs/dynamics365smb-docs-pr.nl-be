---
title: Werkstroomberichten
description: In veel werkstroomantwoorden wordt aan een gebruiker gemeld dat er een gebeurtenis is opgetreden waarop deze moet reageren. De gebeurtenis in een werkstroomstap kan bijvoorbeeld zijn dat Gebruiker 1 de goedkeuring van een nieuwe record aanvraagt, en het antwoord is dat er een bericht wordt verzonden naar Gebruiker 2, de fiatteur. In de volgende werkstroomstap kan de gebeurtenis zijn dat Gebruiker 2 de record goedkeurt, en het antwoord is dat er een bericht wordt verzonden naar Gebruiker 3, die een gerelateerde bewerking van de goedgekeurde record start. Voor werkstroomstappen die betrekking hebben op goedkeuring, is elk bericht gekoppeld aan een goedkeuringspost.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 10/14/2020
ms.author: edupont
ms.openlocfilehash: d11a391a7fd91f6a094dfae9f8908ba4314b357a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378960"
---
# <a name="workflow-notifications"></a><span data-ttu-id="dc237-106">Werkstroomberichten</span><span class="sxs-lookup"><span data-stu-id="dc237-106">Workflow Notifications</span></span>

<span data-ttu-id="dc237-107">Stel uw workflows zo in dat gebruikers automatisch op de hoogte worden gesteld wanneer hun aandacht vereist is voor een stap in die workflow.</span><span class="sxs-lookup"><span data-stu-id="dc237-107">Set up your workflows to automatically notify users when their attention is required for a step in that workflow.</span></span> <span data-ttu-id="dc237-108">In veel werkstroomreacties wordt aan een gebruiker gemeld dat er een gebeurtenis is opgetreden waarop deze moet reageren.</span><span class="sxs-lookup"><span data-stu-id="dc237-108">Many workflow responses are about notifying a user that an event has occurred that they must act on.</span></span> <span data-ttu-id="dc237-109">De gebeurtenis in een werkstroomstap kan bijvoorbeeld zijn dat Gebruiker 1 de goedkeuring van een nieuwe record aanvraagt, en het antwoord is dat er een bericht wordt verzonden naar Gebruiker 2, de fiatteur.</span><span class="sxs-lookup"><span data-stu-id="dc237-109">For example, on one workflow step, the event can be that User 1 requests approval of a new record, and the response is that a notification is sent to User 2, the approver.</span></span> <span data-ttu-id="dc237-110">In de volgende werkstroomstap kan de gebeurtenis zijn dat Gebruiker 2 de record goedkeurt, en het antwoord is dat er een bericht wordt verzonden naar Gebruiker 3, die een gerelateerde bewerking van de goedgekeurde record start.</span><span class="sxs-lookup"><span data-stu-id="dc237-110">On the next workflow step, the event can be that User 2 approves the record, and the response is that a notification is sent to User 3 to start a related processing of the approved record.</span></span> <span data-ttu-id="dc237-111">Voor werkstroomstappen die betrekking hebben op goedkeuring, is elk bericht gekoppeld aan een goedkeuringspost.</span><span class="sxs-lookup"><span data-stu-id="dc237-111">For workflow steps that are about approval, each notification is tied to an approval entry.</span></span> <span data-ttu-id="dc237-112">Zie [Werkstroom](across-workflow.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="dc237-112">For more information, see [Workflow](across-workflow.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="dc237-113">De algemene versie van [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt berichten als e-mail en als interne opmerking.</span><span class="sxs-lookup"><span data-stu-id="dc237-113">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] supports notifications as email and as internal notes.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="dc237-114">Alle werkstroomberichten worden verzonden via een taakwachtrij.</span><span class="sxs-lookup"><span data-stu-id="dc237-114">All workflow notifications are sent through a job queue.</span></span> <span data-ttu-id="dc237-115">Zorg dat de taakwachtrij in uw installatie is ingesteld om werkstroomberichten te verwerken en dat het selectievakje **Automatisch starten van server** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="dc237-115">Make sure that the job queue in your installation is set up to handle workflow notifications, and that the **Start Automatically From Server** check box is selected.</span></span> <span data-ttu-id="dc237-116">Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="dc237-116">For more information, see [Use Job Queues to Schedule Tasks](admin-job-queues-schedule-tasks.md).</span></span>

## <a name="set-up-notifications"></a><span data-ttu-id="dc237-117">Berichten instellen</span><span class="sxs-lookup"><span data-stu-id="dc237-117">Set up notifications</span></span>

<span data-ttu-id="dc237-118">U stelt verschillende aspecten van werkstroomberichten op de volgende plaatsen in:</span><span class="sxs-lookup"><span data-stu-id="dc237-118">You set up different aspects of workflow notifications in the following places:</span></span>  

* <span data-ttu-id="dc237-119">Bericht van fiatteur</span><span class="sxs-lookup"><span data-stu-id="dc237-119">Approver notification</span></span>

    <span data-ttu-id="dc237-120">Voor goedkeuringswerkstromen kunt u de ontvangers van werkstroomberichten instellen door op de pagina **Gebruikersinstellingen voor goedkeuring** een regel in te vullen voor elke gebruiker die deelneemt aan de werkstroom.</span><span class="sxs-lookup"><span data-stu-id="dc237-120">For approval workflows, you set up the recipients of workflow notifications by filling a line on the **Approval User Setup** page for each user that takes part in the workflow.</span></span>  

    <span data-ttu-id="dc237-121">Als bijvoorbeeld Gebruiker 2 wordt opgegeven in het veld **Fiatteur-id** op de regel voor Gebruiker 1, wordt het bericht over de goedkeuringsaanvraag verzonden naar Gebruiker 1.</span><span class="sxs-lookup"><span data-stu-id="dc237-121">For example, if User 2 is specified in the **Approver ID** field on the line for User 1, then the approval request notification is sent to User 1.</span></span> <span data-ttu-id="dc237-122">Zie voor meer informatie [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="dc237-122">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>  
* <span data-ttu-id="dc237-123">Berichtplanningen</span><span class="sxs-lookup"><span data-stu-id="dc237-123">Notification schedules</span></span>

    <span data-ttu-id="dc237-124">U stelt in wanneer en hoe gebruikers werkstroomberichten ontvangen door de pagina **Berichtplanning** in te vullen voor elke werkstroomgebruiker.</span><span class="sxs-lookup"><span data-stu-id="dc237-124">You set up when and how users receive workflow notifications by filling the **Notification Schedule** page for each workflow user.</span></span> <span data-ttu-id="dc237-125">Zie voor meer informatie [Vastleggen wanneer en hoe gebruikers berichten ontvangen](across-how-to-specify-when-and-how-to-receive-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="dc237-125">For more information, see [Specify When and How to Receive Notifications](across-how-to-specify-when-and-how-to-receive-notifications.md).</span></span>  
* <span data-ttu-id="dc237-126">De e-mailberichten aanpassen</span><span class="sxs-lookup"><span data-stu-id="dc237-126">Customize the email notifications</span></span>

    <span data-ttu-id="dc237-127">Als u wilt, kunt u de inhoud van het e-mailbericht wijzigen door rapport 1320, Berichte-mail te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="dc237-127">If you want, you can customize the content of the email notification by modifying report 1320, Notification Email.</span></span> <span data-ttu-id="dc237-128">Zie voor meer informatie [Aangepaste rapportlay-outs maken en wijzigen](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="dc237-128">For more information, see [Create and Modify Custom Report Layouts](ui-how-create-custom-report-layout.md).</span></span>  
* <span data-ttu-id="dc237-129">Reactieopties</span><span class="sxs-lookup"><span data-stu-id="dc237-129">Response options</span></span>

    <span data-ttu-id="dc237-130">U stelt specifieke inhoud en regels van een werkstroombericht in als u de betreffende werkstroom maakt.</span><span class="sxs-lookup"><span data-stu-id="dc237-130">You set up specific content and rules of a workflow notification when you create the workflow in question.</span></span> <span data-ttu-id="dc237-131">U doet dit door opties te selecteren op de pagina **Opties werkstroomreactie** voor het werkstroomantwoord dat het bericht representeert.</span><span class="sxs-lookup"><span data-stu-id="dc237-131">You do this by selecting options on the **Workflow Response Options** page for the workflow response that represents the notification.</span></span> <span data-ttu-id="dc237-132">Zie voor meer informatie stap 9 in [Werkstromen maken](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="dc237-132">For more information, see step 9 in [Create Workflows](across-how-to-create-workflows.md).</span></span>  

* <span data-ttu-id="dc237-133">Afzender informeren</span><span class="sxs-lookup"><span data-stu-id="dc237-133">Notify sender</span></span>

    <span data-ttu-id="dc237-134">Voeg voor goedkeuringswerkstromen een werkstroomreactiestap toe om de afzender te informeren wanneer het verzoek is goedgekeurd of afgewezen.</span><span class="sxs-lookup"><span data-stu-id="dc237-134">For approval workflows, add a workflow response step to notify the sender when the request has been approved or rejected.</span></span> <span data-ttu-id="dc237-135">Zie voor meer informatie stap 9 in [Werkstromen maken](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="dc237-135">For more information, see step 9 in [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="dc237-136">Zie ook</span><span class="sxs-lookup"><span data-stu-id="dc237-136">See Also</span></span>

[<span data-ttu-id="dc237-137">Goedkeuringsgebruikers instellen</span><span class="sxs-lookup"><span data-stu-id="dc237-137">Set Up Approval Users</span></span>](across-how-to-set-up-approval-users.md)  
[<span data-ttu-id="dc237-138">Werkstroomgebruikers instellen</span><span class="sxs-lookup"><span data-stu-id="dc237-138">Set Up Workflow Users</span></span>](across-how-to-set-up-workflow-users.md)  
[<span data-ttu-id="dc237-139">Opgeven wanneer en hoe gebruikers berichten ontvangen</span><span class="sxs-lookup"><span data-stu-id="dc237-139">Specify When and How to Receive Notifications</span></span>](across-how-to-specify-when-and-how-to-receive-notifications.md)  
[<span data-ttu-id="dc237-140">Werkstromen maken</span><span class="sxs-lookup"><span data-stu-id="dc237-140">Create Workflows</span></span>](across-how-to-create-workflows.md)  
[<span data-ttu-id="dc237-141">Aangepaste rapportlay-outs maken en wijzigen</span><span class="sxs-lookup"><span data-stu-id="dc237-141">Create and Modify Custom Report Layouts</span></span>](ui-how-create-custom-report-layout.md)  
[<span data-ttu-id="dc237-142">Taakwachtrijen gebruiken om taken te plannen</span><span class="sxs-lookup"><span data-stu-id="dc237-142">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)  
[<span data-ttu-id="dc237-143">E-mail instellen</span><span class="sxs-lookup"><span data-stu-id="dc237-143">Set up Email</span></span>](admin-how-setup-email.md)  
[<span data-ttu-id="dc237-144">Procedure: Een werkstroom voor inkoopgoedkeuring instellen en gebruiken</span><span class="sxs-lookup"><span data-stu-id="dc237-144">Walkthrough: Setting Up and Using a Purchase Approval Workflow</span></span>](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[<span data-ttu-id="dc237-145">Werkstroom</span><span class="sxs-lookup"><span data-stu-id="dc237-145">Workflow</span></span>](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]