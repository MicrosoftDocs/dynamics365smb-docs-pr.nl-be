---
title: Waarom kan ik een pagina niet personaliseren | Microsoft Docs
description: Verklaart waarom u een pagina niet kunt personaliseren en wat u kunt doen om deze te ontgrendelen zodat u de pagina wel kunt personaliseren.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 1a3edaca2e76388d82ea8991c3196410dd9c7288
ms.sourcegitcommit: a88d1e9c0ab647cb8d9d81d32c0bdc82843f4145
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/31/2019
ms.locfileid: "1796793"
---
# <a name="why-a-page-is-locked-from-personalization"></a><span data-ttu-id="1628b-103">Waarom een pagina is vergrendeld voor personaliseren</span><span class="sxs-lookup"><span data-stu-id="1628b-103">Why a Page is Locked from Personalization</span></span>

<span data-ttu-id="1628b-104">Er zijn twee voorwaarden die voorkomen dat u een pagina personaliseert.</span><span class="sxs-lookup"><span data-stu-id="1628b-104">There are two conditions that prevent you from personalizing a page.</span></span> <span data-ttu-id="1628b-105">Of de pagina is vergrendeld (zoals aangegeven door ![Personaliseringsvergrendeling](media/personalization-lock-icon.png "Personaliseringsvergrendeling")) of de pagina is geblokkeerd (zoals aangegeven door ![Personalisatie geblokkeerd](media/personalization-blocked-icon.png "Personalisatie geblokkeerd")).</span><span class="sxs-lookup"><span data-stu-id="1628b-105">Either the page is locked (as indicated by ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock")) or it is blocked (as indicated by ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked")).</span></span>

## <a name="locked-from-personalizing"></a><span data-ttu-id="1628b-106">Vergrendeld tegen personaliseren</span><span class="sxs-lookup"><span data-stu-id="1628b-106">Locked from Personalizing</span></span>

<span data-ttu-id="1628b-107">Als er een pictogram ![Personaliseringsvergrendeling](media/personalization-lock-icon.png "Personaliseringsvergrendeling") is te zien in de banner **Personaliseren** wanneer u een pagina opent (zoals weergegeven), kunt u op dit moment geen persoonlijke instellingen meer wijzigen op de pagina.</span><span class="sxs-lookup"><span data-stu-id="1628b-107">If there is a ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon in the **Personalizing** banner when you open a page (as shown), this means that you are currently prevented from making any more personalization changes to the page.</span></span>

<span data-ttu-id="1628b-108">![Personaliseringsvergrendeling](media/personalization-locked.png "Personaliseringsvergrendeling")</span><span class="sxs-lookup"><span data-stu-id="1628b-108">![Personalize Lock](media/personalization-locked.png "Personalize lock")</span></span>


<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

<span data-ttu-id="1628b-109">Hiervoor kunnen twee redenen bestaan:</span><span class="sxs-lookup"><span data-stu-id="1628b-109">There can be two reasons for this:</span></span>

1. <span data-ttu-id="1628b-110">U hebt de pagina eerder gepersonaliseerd, maar dit is met een eerdere versie van het product gebeurd.</span><span class="sxs-lookup"><span data-stu-id="1628b-110">You have personalized the page before, but it was done using an earlier version of the product.</span></span> <span data-ttu-id="1628b-111">We hebben de manier waarop personalisatie achter de schermen werkt, gewijzigd sinds u de pagina voor het laatst hebt gepersonaliseerd.</span><span class="sxs-lookup"><span data-stu-id="1628b-111">We changed the way personalization works behind the scenes since the last time that you personalized the page.</span></span> <span data-ttu-id="1628b-112">De oude en de nieuwe aanpak werken helaas niet goed samen.</span><span class="sxs-lookup"><span data-stu-id="1628b-112">Unfortunately, the old way and new way of doing things do not work together.</span></span>

2. <span data-ttu-id="1628b-113">Tot dusverre hebt u alleen [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] gebruikt om de pagina te personaliseren.</span><span class="sxs-lookup"><span data-stu-id="1628b-113">Until now, you have only used the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] to personalize the page.</span></span>

### <a name="unlocking-the-page"></a><span data-ttu-id="1628b-114">De pagina ontgrendelen</span><span class="sxs-lookup"><span data-stu-id="1628b-114">Unlocking the Page</span></span>

<span data-ttu-id="1628b-115">Als u een pagina wilt ontgrendelen en door wilt gaan met personaliseren, kiest u ![Personaliseringsvergrendeling](media/personalization-lock-icon.png "Personaliseringsvergrendeling") en vervolgens **Ontgrendelen**.</span><span class="sxs-lookup"><span data-stu-id="1628b-115">If you want to unlock a page and continue personalizing it, choose ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock"), and then **Unlock**.</span></span>  

<span data-ttu-id="1628b-116">Voordat u de pagina ontgrendelt, houdt u rekening met het volgende:</span><span class="sxs-lookup"><span data-stu-id="1628b-116">Before you unlock the page, be aware of the following:</span></span>

- <span data-ttu-id="1628b-117">De huidige personalisatie van de pagina wordt gewist.</span><span class="sxs-lookup"><span data-stu-id="1628b-117">The current personalization of the page will be cleared.</span></span> <span data-ttu-id="1628b-118">De pagina keert terug naar de oorspronkelijke indeling en u moet opnieuw beginnen.</span><span class="sxs-lookup"><span data-stu-id="1628b-118">The page will go back to its original layout, and you will have to start from scratch.</span></span>

- <span data-ttu-id="1628b-119">In de [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] blijft de pagina zoals deze is en hebben de nieuwe personalisatiewijzigingen die in de Business Central-client zijn aangebracht, geen invloed.</span><span class="sxs-lookup"><span data-stu-id="1628b-119">In the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], the page will remain as-is and will not be affected by the new personalization changes made in the Business Central client.</span></span> <span data-ttu-id="1628b-120">Vanaf nu zijn de personalisatie in de [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] en in Business Central volledig gescheiden van elkaar.</span><span class="sxs-lookup"><span data-stu-id="1628b-120">Going forward, the personalization in the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] and Business Central client will be completely separate from each other.</span></span>

## <a name="blocked-from-personalizing"></a><span data-ttu-id="1628b-121">Geblokkeerd tegen personaliseren</span><span class="sxs-lookup"><span data-stu-id="1628b-121">Blocked from Personalizing</span></span>

<span data-ttu-id="1628b-122">Als de banner Personaliseren het pictogram ![Personalisatie geblokkeerd](media/personalization-blocked-icon.png "Personalisatie geblokkeerd") bevat, betekent dit dat u geblokkeerd wordt om personalisatie op de pagina aan te brengen.</span><span class="sxs-lookup"><span data-stu-id="1628b-122">If there is a ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon in the Personalizing banner, this means that you are blocked from doing any personalization to the page.</span></span>

<span data-ttu-id="1628b-123">![Personalisatie geblokkeerd](media/personalization-blocked.png "Personalisatie geblokkeerd")</span><span class="sxs-lookup"><span data-stu-id="1628b-123">![Personalize blocked](media/personalization-blocked.png "Personalize lock")</span></span>

<span data-ttu-id="1628b-124">De reden hiervoor is dat het rolcentrum of de rol die op dat moment aan uw gebruikersaccount is gekoppeld, deze pagina specifiek voor uw rol wijzigt.</span><span class="sxs-lookup"><span data-stu-id="1628b-124">The reason for this is that the Role Center or role that is currently associated with your user account modifies this page specifically for your role.</span></span> <span data-ttu-id="1628b-125">Neem contact met uw beheerder op voor hulp of schakel indien van toepassing over op een rolcentrum (ga vanuit [**Mijn instellingen**](https://businesscentral.dynamics.com?page=9176 "rechtstreeks naar de pagina met uw gebruikersinstellingen in Business Central")) dat rolaanpassing voor deze pagina bevat.</span><span class="sxs-lookup"><span data-stu-id="1628b-125">Please contact your administrator for assistance or, if it makes sense, try switching to a Role Center (from  [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central")) that does include role-tailoring for this page.</span></span>

## <a name="see-also"></a><span data-ttu-id="1628b-126">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1628b-126">See Also</span></span>
[<span data-ttu-id="1628b-127">Het personaliseren van uw werkruimte</span><span class="sxs-lookup"><span data-stu-id="1628b-127">Personalizing Your Workspace</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="1628b-128">Personalisatie beheren</span><span class="sxs-lookup"><span data-stu-id="1628b-128">Managing Personalization</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="1628b-129">Basisinstellingen wijzigen</span><span class="sxs-lookup"><span data-stu-id="1628b-129">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="1628b-130">Wijzigen welke functies worden weergegeven</span><span class="sxs-lookup"><span data-stu-id="1628b-130">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
