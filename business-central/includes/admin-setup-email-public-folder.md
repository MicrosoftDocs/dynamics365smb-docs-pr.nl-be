---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 06/25/2020
ms.author: edupont
ms.openlocfilehash: 8c5f4205128d52ec88f432cea7ece98e0310546d
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528022"
---
<span data-ttu-id="eb9ed-101">Voordat u e-mailregistratie kunt instellen, moet u uw Exchange Online voorbereiden met [openbare mappen](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019).</span><span class="sxs-lookup"><span data-stu-id="eb9ed-101">Before you can set up email logging, you must prepare your Exchange Online with [public folders](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019).</span></span> <span data-ttu-id="eb9ed-102">U kunt dit doen in het [Exchange-beheercentrum](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019) of u kunt de [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps) gebruiken.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-102">You can do this in the [Exchange admin center](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019), or you can use the [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps).</span></span>  

> [!TIP]
> <span data-ttu-id="eb9ed-103">Als u de [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps) wilt gebruiken, vindt u inspiratie voor het opzetten van uw script in een voorbeeldscript dat we hebben gepubliceerd [de BCTech repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).</span><span class="sxs-lookup"><span data-stu-id="eb9ed-103">If you want to use the [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps), you can find inspiration for how to set up your script in a sample script that we published to [the BCTech repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).</span></span>

<span data-ttu-id="eb9ed-104">De volgende lijst beschrijft de belangrijkste stappen met koppelingen voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-104">The following list describes the main steps with links to learn more.</span></span>  

- <span data-ttu-id="eb9ed-105">Maak een beheerdersrol voor openbare mappen op basis van de informatie in de volgende tabel:</span><span class="sxs-lookup"><span data-stu-id="eb9ed-105">Create an admin role for public folders based on the information in the following table:</span></span>

  |<span data-ttu-id="eb9ed-106">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="eb9ed-106">Property</span></span>        |<span data-ttu-id="eb9ed-107">Waarde</span><span class="sxs-lookup"><span data-stu-id="eb9ed-107">Value</span></span>                     |
  |----------------|--------------------------|
  |<span data-ttu-id="eb9ed-108">Name</span><span class="sxs-lookup"><span data-stu-id="eb9ed-108">Name</span></span>            |<span data-ttu-id="eb9ed-109">Beheer van openbare mappen</span><span class="sxs-lookup"><span data-stu-id="eb9ed-109">Public Folders Management</span></span> |
  |<span data-ttu-id="eb9ed-110">Geselecteerde rollen</span><span class="sxs-lookup"><span data-stu-id="eb9ed-110">Selected roles</span></span>  |<span data-ttu-id="eb9ed-111">Openbare mappen</span><span class="sxs-lookup"><span data-stu-id="eb9ed-111">Public Folders</span></span>            |
  |<span data-ttu-id="eb9ed-112">Geselecteerde leden</span><span class="sxs-lookup"><span data-stu-id="eb9ed-112">Selected members</span></span>|<span data-ttu-id="eb9ed-113">Het e-mailadres van het gebruikersaccount dat Business Central zal gebruiken om de e-mailregistratietaak uit te voeren</span><span class="sxs-lookup"><span data-stu-id="eb9ed-113">The email of the user account that Business Central will use to run the email logging job</span></span>|

  <span data-ttu-id="eb9ed-114">Zie [Rolgroepen beheren](/exchange/permissions/role-groups?view=exchserver-2019) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-114">For more information, see [Manage role groups](/exchange/permissions/role-groups?view=exchserver-2019).</span></span>

- <span data-ttu-id="eb9ed-115">Maak een nieuwe openbare mappostbus op basis van de informatie in de volgende tabel:</span><span class="sxs-lookup"><span data-stu-id="eb9ed-115">Create a new public folder mailbox based on the information in the following table:</span></span>

  |<span data-ttu-id="eb9ed-116">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="eb9ed-116">Property</span></span>        |<span data-ttu-id="eb9ed-117">Waarde</span><span class="sxs-lookup"><span data-stu-id="eb9ed-117">Value</span></span>                     |
  |----------------|--------------------------|
  |<span data-ttu-id="eb9ed-118">Name</span><span class="sxs-lookup"><span data-stu-id="eb9ed-118">Name</span></span>            |<span data-ttu-id="eb9ed-119">Openbare postbus</span><span class="sxs-lookup"><span data-stu-id="eb9ed-119">Public MailBox</span></span>            |

  <span data-ttu-id="eb9ed-120">Zie voor meer informatie [Een openbare mappostbus maken in Exchange Server](/exchange/collaboration/public-folders/create-public-folder-mailboxes).</span><span class="sxs-lookup"><span data-stu-id="eb9ed-120">For more information, see [Create a public folder mailbox in Exchange Server](/exchange/collaboration/public-folders/create-public-folder-mailboxes).</span></span>  

- <span data-ttu-id="eb9ed-121">Nieuwe openbare mappen maken</span><span class="sxs-lookup"><span data-stu-id="eb9ed-121">Create new public folders</span></span>

  - <span data-ttu-id="eb9ed-122">Maak een nieuwe openbare map met de naam *E-mailregistratie* in de root zodat het volledige pad naar de map ```\Email Logging\``` wordt</span><span class="sxs-lookup"><span data-stu-id="eb9ed-122">Create a new public folder with the name *Email Logging* in the root so that the full path to the folder becomes ```\Email Logging\```</span></span>
  - <span data-ttu-id="eb9ed-123">Maak twee submappen zodat het resultaat de volgende volledige paden naar de mappen is:</span><span class="sxs-lookup"><span data-stu-id="eb9ed-123">Create two subfolders so that the the result is the following full paths to the folders:</span></span>
    - ```\Email Logging\Queue\```
    - ```\Email Logging\Storage\```

  <span data-ttu-id="eb9ed-124">Raadpleeg [Een openbare map maken](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-124">For more information, see [Create a public folder](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019).</span></span>

- <span data-ttu-id="eb9ed-125">De openbare map *Wachtrij* inschakelen voor post</span><span class="sxs-lookup"><span data-stu-id="eb9ed-125">Mail-enable the *Queue* public folder</span></span>

  <span data-ttu-id="eb9ed-126">Zie voor meer informatie [Een openbare map in- of uitschakelen voor post](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019)</span><span class="sxs-lookup"><span data-stu-id="eb9ed-126">For more information, see [Mail-enable or mail-disable a public folder](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019)</span></span>

- <span data-ttu-id="eb9ed-127">Het verzenden van e-mails naar de openbare map *Wachtrij* inschakelen met behulp van Outlook of de Exchange Management Shell</span><span class="sxs-lookup"><span data-stu-id="eb9ed-127">Mail-enable sending emails to the *Queue* public folder using Outlook or the Exchange Management Shell</span></span>

  <span data-ttu-id="eb9ed-128">Zie voor meer informatie [Anonieme gebruikers toestaan om e-mail te verzenden naar een voor e-mail geschikte openbare map](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder)</span><span class="sxs-lookup"><span data-stu-id="eb9ed-128">For more information, see [Allow anonymous users to send email to a mail-enabled public folder](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder)</span></span>

- <span data-ttu-id="eb9ed-129">Stel de gebruiker van e-mailregistratie in als eigenaar van beide openbare mappen, *Wachtrij* en *Opslag*, die Outlook of de Exchange Management Shell gebruiken op basis van de informatie in de volgende tabel:</span><span class="sxs-lookup"><span data-stu-id="eb9ed-129">Set the email logging user as an owner of both public folders, *Queue* and *Storage* public folders  using Outlook or the Exchange Management Shell based on the information in the following table:</span></span>

  |<span data-ttu-id="eb9ed-130">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="eb9ed-130">Property</span></span>        |<span data-ttu-id="eb9ed-131">Waarde</span><span class="sxs-lookup"><span data-stu-id="eb9ed-131">Value</span></span>                     |
  |----------------|--------------------------|
  |<span data-ttu-id="eb9ed-132">Gebruiker</span><span class="sxs-lookup"><span data-stu-id="eb9ed-132">User</span></span>            |<span data-ttu-id="eb9ed-133">Het e-mailadres van het gebruikersaccount dat Business Central zal gebruiken om de e-mailregistratietaak uit te voeren</span><span class="sxs-lookup"><span data-stu-id="eb9ed-133">The email of the user account that Business Central will use to run the email logging job</span></span>|
  |<span data-ttu-id="eb9ed-134">Machtigingsniveau</span><span class="sxs-lookup"><span data-stu-id="eb9ed-134">Permission level</span></span>|<span data-ttu-id="eb9ed-135">Eigenaar</span><span class="sxs-lookup"><span data-stu-id="eb9ed-135">Owner</span></span>                     |

  <span data-ttu-id="eb9ed-136">Zie voor meer informatie [Machtigingen voor openbare mappen toewijzen](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).</span><span class="sxs-lookup"><span data-stu-id="eb9ed-136">For more information, see [Assign permissions to the public folder](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).</span></span>

- <span data-ttu-id="eb9ed-137">Maak twee mapstroomregels op basis van de informatie in de volgende tabel</span><span class="sxs-lookup"><span data-stu-id="eb9ed-137">Create two mail flow rules based on the information in the following table</span></span>

  |<span data-ttu-id="eb9ed-138">Doel</span><span class="sxs-lookup"><span data-stu-id="eb9ed-138">Purpose</span></span>  |<span data-ttu-id="eb9ed-139">Name</span><span class="sxs-lookup"><span data-stu-id="eb9ed-139">Name</span></span> |<span data-ttu-id="eb9ed-140">Voorwaarden</span><span class="sxs-lookup"><span data-stu-id="eb9ed-140">Conditions</span></span>                        |<span data-ttu-id="eb9ed-141">Actie</span><span class="sxs-lookup"><span data-stu-id="eb9ed-141">Action</span></span>                                       |
  |---------|-----|----------------------------------|---------------------------------------------|
  |<span data-ttu-id="eb9ed-142">Een regel voor inkomende e-mail</span><span class="sxs-lookup"><span data-stu-id="eb9ed-142">A rule for incoming email</span></span> |<span data-ttu-id="eb9ed-143">Naar deze organisatie verzonden e-mail registreren</span><span class="sxs-lookup"><span data-stu-id="eb9ed-143">Log Email Sent to This Organization</span></span>|<span data-ttu-id="eb9ed-144">*De afzender* bevindt zich *buiten de organisatie* en *de ontvanger* bevindt zich *binnen de organisatie*</span><span class="sxs-lookup"><span data-stu-id="eb9ed-144">*The sender* is located *Outside the organization*, and *the recipient* is located *Inside the organization*</span></span>|<span data-ttu-id="eb9ed-145">BCC het e-mailaccount dat is opgegeven voor de openbare map *Wachtrij*</span><span class="sxs-lookup"><span data-stu-id="eb9ed-145">BCC the email account that is specified for the *Queue* public folder</span></span>|
  |<span data-ttu-id="eb9ed-146">Een regel voor uitgaande e-mail</span><span class="sxs-lookup"><span data-stu-id="eb9ed-146">A rule for outgoing email</span></span> | <span data-ttu-id="eb9ed-147">Uit deze organisatie verzonden e-mail registreren</span><span class="sxs-lookup"><span data-stu-id="eb9ed-147">Log Email Sent from This Organization</span></span> |<span data-ttu-id="eb9ed-148">*De afzender* bevindt zich *binnen de organisatie* en *de ontvanger* bevindt zich *buiten de organisatie*</span><span class="sxs-lookup"><span data-stu-id="eb9ed-148">*The sender* is located *Inside the organization*, and *the recipient* is located *Outside the organization*</span></span>|<span data-ttu-id="eb9ed-149">BCC het e-mailaccount dat is opgegeven voor de openbare map *Wachtrij*</span><span class="sxs-lookup"><span data-stu-id="eb9ed-149">BCC the email account that is specified for the *Queue* public folder</span></span>|
  
  <span data-ttu-id="eb9ed-150">Zie voor meer informatie [Poststroomregels beheren in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) en [Poststroomregelacties in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-action).</span><span class="sxs-lookup"><span data-stu-id="eb9ed-150">For more information, see [Manage mail flow rules in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) and [Mail flow rule actions in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-action).</span></span>

> [!NOTE]
> <span data-ttu-id="eb9ed-151">Als u wijzigingen aanbrengt in de Exchange Management Shell, worden de wijzigingen met vertraging zichtbaar in het Exchange-beheercentrum.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-151">If you make changes in the Exchange Management Shell, the changes become visible in the Exchange admin center after a delay.</span></span> <span data-ttu-id="eb9ed-152">De wijzigingen die in Exchange zijn aangebracht, zijn ook beschikbaar in [!INCLUDE[prodshort](prodshort.md)] na een vertraging.</span><span class="sxs-lookup"><span data-stu-id="eb9ed-152">Also, the changes made in Exchange will be available in [!INCLUDE[prodshort](prodshort.md)] after a delay.</span></span>
