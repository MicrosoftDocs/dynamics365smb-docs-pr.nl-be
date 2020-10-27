---
title: Microsoft Teams-integratie met Business Central beheren | Microsoft Docs
description: Business Central-integratie met Microsoft Teams beheren.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: 3c04dfb2f77eba906b2567ca9438849e1cc20861
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989371"
---
# <a name="managing-microsoft-teams-integration-with-business-central"></a><span data-ttu-id="8744f-103">Microsoft Teams-integratie met Business Central beheren</span><span class="sxs-lookup"><span data-stu-id="8744f-103">Managing Microsoft Teams Integration with Business Central</span></span>

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

<span data-ttu-id="8744f-104">Dit artikel geeft een overzicht van wat u als beheerder kunt doen om Microsoft Teams-integratie met [!INCLUDE [prodshort](includes/prodshort.md)] te beheren.</span><span class="sxs-lookup"><span data-stu-id="8744f-104">This article provides an overview of what you can do as an administrator to control Microsoft Teams integration with [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>

## <a name="in-microsoft-teams"></a><span data-ttu-id="8744f-105">In Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8744f-105">In Microsoft Teams</span></span>

### <a name="minimum-requirements"></a><span data-ttu-id="8744f-106">Minimumvereisten</span><span class="sxs-lookup"><span data-stu-id="8744f-106">Minimum requirements</span></span>

<span data-ttu-id="8744f-107">In dit gedeelte worden de minimumvereisten voor de functies van de [!INCLUDE [prodshort](includes/prodshort.md)]-app beschreven om in Teams te werken.</span><span class="sxs-lookup"><span data-stu-id="8744f-107">This section describes the minimum requirements for the [!INCLUDE [prodshort](includes/prodshort.md)] app features to work in Teams.</span></span>

- <span data-ttu-id="8744f-108">Vereiste licenties</span><span class="sxs-lookup"><span data-stu-id="8744f-108">Required licenses</span></span>

    <span data-ttu-id="8744f-109">Deze tabel geeft u een overzicht van de licenties die nodig zijn voor de functies van de [!INCLUDE [prodshort](includes/prodshort.md)]-app om in Teams te werken.</span><span class="sxs-lookup"><span data-stu-id="8744f-109">This table gives you an overview of the licenses needed for the [!INCLUDE [prodshort](includes/prodshort.md)] app features to work in Teams.</span></span>

    |<span data-ttu-id="8744f-110">Wat</span><span class="sxs-lookup"><span data-stu-id="8744f-110">What</span></span>|<span data-ttu-id="8744f-111">Teams-licentie</span><span class="sxs-lookup"><span data-stu-id="8744f-111">Teams license</span></span>|<span data-ttu-id="8744f-112">Business Central-licentie</span><span class="sxs-lookup"><span data-stu-id="8744f-112">Business Central license</span></span>|
    |----|---|---|
    |<span data-ttu-id="8744f-113">Een link naar een [!INCLUDE [prodshort](includes/prodshort.md)]-record opnemen in een gesprek en het verzenden als een kaart.</span><span class="sxs-lookup"><span data-stu-id="8744f-113">Paste a link to a [!INCLUDE [prodshort](includes/prodshort.md)] record into a conversation, and send it as a card.</span></span>|<span data-ttu-id="8744f-114">![vinkje](media/check.png "vinkje")</span><span class="sxs-lookup"><span data-stu-id="8744f-114">![check mark](media/check.png "check")</span></span>|<span data-ttu-id="8744f-115">![vinkje](media/check.png "vinkje")</span><span class="sxs-lookup"><span data-stu-id="8744f-115">![check mark](media/check.png "check")</span></span>|
    |<span data-ttu-id="8744f-116">Een kaart van een [!INCLUDE [prodshort](includes/prodshort.md)]-record weergeven in een gesprek.</span><span class="sxs-lookup"><span data-stu-id="8744f-116">View a card of a [!INCLUDE [prodshort](includes/prodshort.md)] record in a conversation.</span></span>|<span data-ttu-id="8744f-117">![vinkje](media/check.png "vinkje")</span><span class="sxs-lookup"><span data-stu-id="8744f-117">![check mark](media/check.png "check")</span></span>||
    |<span data-ttu-id="8744f-118">Meer details van een kaart voor een [!INCLUDE [prodshort](includes/prodshort.md)]-record weergeven in een gesprek.</span><span class="sxs-lookup"><span data-stu-id="8744f-118">View more details of card for a [!INCLUDE [prodshort](includes/prodshort.md)] record in a conversation.</span></span>|<span data-ttu-id="8744f-119">![vinkje](media/check.png "vinkje")</span><span class="sxs-lookup"><span data-stu-id="8744f-119">![check mark](media/check.png "check")</span></span>|<span data-ttu-id="8744f-120">![vinkje](media/check.png "vinkje")</span><span class="sxs-lookup"><span data-stu-id="8744f-120">![check mark](media/check.png "check")</span></span>|

- <span data-ttu-id="8744f-121">URL-voorbeelden toestaan</span><span class="sxs-lookup"><span data-stu-id="8744f-121">Allow URL previews</span></span>

    <span data-ttu-id="8744f-122">Beleidsinstelling **URL-voorbeelden toestaan** moet zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="8744f-122">**Allow URL previews** policy setting must be turned on.</span></span> <span data-ttu-id="8744f-123">Anders kan er geen kaart worden gegenereerd voor Business Central-koppelingen die in een Teams-gesprek worden geplakt.</span><span class="sxs-lookup"><span data-stu-id="8744f-123">Otherwise, a card can't be generated for Business Central links pasted into a Teams conversation.</span></span> <span data-ttu-id="8744f-124">Zie voor meer informatie over deze instelling [Berichtenbeleid beheren in Teams](/microsoftteams/messaging-policies-in-teams).</span><span class="sxs-lookup"><span data-stu-id="8744f-124">For more information about this setting, see [Manage messaging policies in Teams](/microsoftteams/messaging-policies-in-teams).</span></span>

### <a name="managing-the-business-central-app-optional"></a><span data-ttu-id="8744f-125">De Business Central-app beheren (optioneel)</span><span class="sxs-lookup"><span data-stu-id="8744f-125">Managing the Business Central app (optional)</span></span>

<span data-ttu-id="8744f-126">Als Teams-beheerder kunt u alle apps voor uw organisatie beheren, inclusief de [!INCLUDE [prodshort](includes/prodshort.md)]-app.</span><span class="sxs-lookup"><span data-stu-id="8744f-126">As a Teams administrator, you can manage all apps for your organization, including the [!INCLUDE [prodshort](includes/prodshort.md)] app.</span></span> <span data-ttu-id="8744f-127">U kunt de [!INCLUDE [prodshort](includes/prodshort.md)]-app voor uw organisatie beheren, gebruikers blokkeren tegen het installeren van de app en meer.</span><span class="sxs-lookup"><span data-stu-id="8744f-127">You can approve or install the [!INCLUDE [prodshort](includes/prodshort.md)] app for your organization, block user's from installing the app, and more.</span></span>

<span data-ttu-id="8744f-128">Zie de volgende artikelen in de Microsoft Teams-documentatie voor meer informatie:</span><span class="sxs-lookup"><span data-stu-id="8744f-128">For more information, see the following articles in the Microsoft Teams documentation:</span></span>

- [<span data-ttu-id="8744f-129">Uw apps beheren in het Microsoft Teams-beheercentrum</span><span class="sxs-lookup"><span data-stu-id="8744f-129">Manage your apps in the Microsoft Teams admin center</span></span>](https://docs.microsoft.com/MicrosoftTeams/manage-apps)
- [<span data-ttu-id="8744f-130">Installatiebeleid voor apps beheren in Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8744f-130">Manage app setup policies in Microsoft Teams</span></span>](https://docs.microsoft.com/microsoftteams/teams-app-setup-policies)

## <a name="in-prodshort"></a><span data-ttu-id="8744f-131">In [!INCLUDE [prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="8744f-131">In [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

### <a name="minimum-requirements"></a><span data-ttu-id="8744f-132">Minimumvereisten</span><span class="sxs-lookup"><span data-stu-id="8744f-132">Minimum requirements</span></span>

- <span data-ttu-id="8744f-133">[!INCLUDE [prodshort](includes/prodshort.md)]-versie:</span><span class="sxs-lookup"><span data-stu-id="8744f-133">[!INCLUDE [prodshort](includes/prodshort.md)] version:</span></span>

    <span data-ttu-id="8744f-134">[!INCLUDE [prodshort](includes/prodshort.md)]-releasewave 2 van 2020 (versie 17) of hoger.</span><span class="sxs-lookup"><span data-stu-id="8744f-134">[!INCLUDE [prodshort](includes/prodshort.md)] 2020 release wave 2 (version 17) or later.</span></span> <span data-ttu-id="8744f-135">Teams-integratie wordt alleen ondersteund voor [!INCLUDE [prodshort](includes/prodshort.md)] online; niet on-premises.</span><span class="sxs-lookup"><span data-stu-id="8744f-135">Teams integration is only supported for [!INCLUDE [prodshort](includes/prodshort.md)] online; not on-premises.</span></span>

- <span data-ttu-id="8744f-136">Codeunit **2718 Page Summary Provider** wordt gepubliceerd als een webservice:</span><span class="sxs-lookup"><span data-stu-id="8744f-136">Codeunit **2718 Page Summary Provider** is published as a web service:</span></span>

    <span data-ttu-id="8744f-137">Deze codeunit wordt standaard als webservice gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="8744f-137">This codeunit is published as a web service by default.</span></span> <span data-ttu-id="8744f-138">De codeunit is onderdeel van de [!INCLUDE [prodshort](includes/prodshort.md)]-systeemtoepassing.</span><span class="sxs-lookup"><span data-stu-id="8744f-138">The codeunit is part of the [!INCLUDE [prodshort](includes/prodshort.md)] system application.</span></span> <span data-ttu-id="8744f-139">De codeunit wordt gebruikt om de veldgegevens op te halen voor een [!INCLUDE [prodshort](includes/prodshort.md)]-pagina die wordt toegevoegd aan een Teams-gesprek.</span><span class="sxs-lookup"><span data-stu-id="8744f-139">It's used to get the field data for a [!INCLUDE [prodshort](includes/prodshort.md)] page added to a Teams conversation.</span></span> 

- <span data-ttu-id="8744f-140">Gebruikersmachtigingen:</span><span class="sxs-lookup"><span data-stu-id="8744f-140">User permissions:</span></span>

    <span data-ttu-id="8744f-141">De pagina's en gegevens die gebruikers kunnen bekijken en bewerken in een Teams-gesprek worden voor het grootste deel bepaald door hun machtigingen in [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="8744f-141">For the most part, the pages and data that users can view and edit in a Teams conversation is controlled by their permissions in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>
    
    - <span data-ttu-id="8744f-142">Om een [!INCLUDE [prodshort](includes/prodshort.md)]-koppeling te plakken in een Teams-gesprek en deze te laten uitbreiden naar een kaart, moeten gebruikers ten minste leesrechten hebben voor de pagina en de gegevens ervan.</span><span class="sxs-lookup"><span data-stu-id="8744f-142">To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, users must have at least read permission on the page and its data.</span></span>
    - <span data-ttu-id="8744f-143">Zodra een kaart in een gesprek is ingediend, kan elke gebruiker in dat gesprek die kaart bekijken zonder toestemming voor Business Central.</span><span class="sxs-lookup"><span data-stu-id="8744f-143">Once a card is submitted into a conversation, any user in that conversation can view that card without permission to Business Central.</span></span>
    - <span data-ttu-id="8744f-144">Om meer details van een kaart te zien of de record te openen in [!INCLUDE [prodshort](includes/prodshort.md)] moeten gebruikers leesbevoegdheid hebben voor de pagina en de gegevens ervan.</span><span class="sxs-lookup"><span data-stu-id="8744f-144">To view more details for a card or open the record in [!INCLUDE [prodshort](includes/prodshort.md)], users must have read permission on the page and its data.</span></span>
    - <span data-ttu-id="8744f-145">Om gegevens te wijzigen hebben gebruikers wijzigingsmachtiging nodig.</span><span class="sxs-lookup"><span data-stu-id="8744f-145">To change data, user's need modify permissions.</span></span>
    
    <span data-ttu-id="8744f-146">Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie over machtigingen.</span><span class="sxs-lookup"><span data-stu-id="8744f-146">For information about permissions, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8744f-147">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8744f-147">See Also</span></span>
[<span data-ttu-id="8744f-148">Integratieoverzicht van Business Central en Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8744f-148">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="8744f-149">[De [!INCLUDE [prodshort](includes/prodshort.md)]-app installeren voor Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="8744f-149">[Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="8744f-150">Ontwikkeling voor Teams-integratie</span><span class="sxs-lookup"><span data-stu-id="8744f-150">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[<span data-ttu-id="8744f-151">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="8744f-151">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
