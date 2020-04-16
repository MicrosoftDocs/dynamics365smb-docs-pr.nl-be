---
title: Waarom kan ik een pagina niet personaliseren | Microsoft Docs
description: Verklaart waarom u een pagina niet kunt personaliseren en wat u kunt doen om deze te ontgrendelen zodat u de pagina wel kunt personaliseren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 9774c3472a70967f6b0250e2f02e817f26e9b710
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195735"
---
# <a name="why-a-page-is-locked-from-personalization"></a><span data-ttu-id="b8b19-103">Waarom een pagina is vergrendeld voor personaliseren</span><span class="sxs-lookup"><span data-stu-id="b8b19-103">Why a Page is Locked from Personalization</span></span>

<span data-ttu-id="b8b19-104">Er zijn twee voorwaarden die voorkomen dat u een pagina personaliseert.</span><span class="sxs-lookup"><span data-stu-id="b8b19-104">There are two conditions that prevent you from personalizing a page.</span></span> <span data-ttu-id="b8b19-105">Of de pagina is vergrendeld (zoals aangegeven door het pictogram ![Personaliseringsvergrendeling](media/personalization-lock-icon.png "Personalisatievergrendeling")) of de pagina is geblokkeerd (zoals aangegeven door het pictogram ![Personalisatie geblokkeerd](media/personalization-blocked-icon.png "Personalisatie geblokkeerd")).</span><span class="sxs-lookup"><span data-stu-id="b8b19-105">Either the page is locked (as indicated by the ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock")) icon or it is blocked (as indicated by the ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon).</span></span>

## <a name="locked-from-personalizing"></a><span data-ttu-id="b8b19-106">Vergrendeld tegen personaliseren</span><span class="sxs-lookup"><span data-stu-id="b8b19-106">Locked from Personalizing</span></span>

<span data-ttu-id="b8b19-107">Als er een pictogram ![Personaliseringsvergrendeling](media/personalization-lock-icon.png "Personalisatievergrendeling") is te zien in de banner **Personaliseren** wanneer u een pagina opent, kunt u op dit moment geen persoonlijke instellingen meer wijzigen op de pagina.</span><span class="sxs-lookup"><span data-stu-id="b8b19-107">If there is a ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon in the **Personalizing** banner when you open a page, this means that you are currently prevented from making any more personalization changes to the page.</span></span>

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

<span data-ttu-id="b8b19-108">Hiervoor kunnen twee redenen bestaan:</span><span class="sxs-lookup"><span data-stu-id="b8b19-108">There can be two reasons for this:</span></span>

1. <span data-ttu-id="b8b19-109">U hebt de pagina eerder gepersonaliseerd, maar dit is met een eerdere versie van het product gebeurd.</span><span class="sxs-lookup"><span data-stu-id="b8b19-109">You have personalized the page before, but it was done using an earlier version of the product.</span></span> <span data-ttu-id="b8b19-110">We hebben de manier waarop personalisatie achter de schermen werkt, gewijzigd sinds u de pagina voor het laatst hebt gepersonaliseerd.</span><span class="sxs-lookup"><span data-stu-id="b8b19-110">We changed the way personalization works behind the scenes since the last time that you personalized the page.</span></span> <span data-ttu-id="b8b19-111">De oude en de nieuwe aanpak werken helaas niet goed samen.</span><span class="sxs-lookup"><span data-stu-id="b8b19-111">Unfortunately, the old way and new way of doing things do not work together.</span></span>

2. <span data-ttu-id="b8b19-112">Tot dusverre hebt u alleen [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] gebruikt om de pagina te personaliseren.</span><span class="sxs-lookup"><span data-stu-id="b8b19-112">Until now, you have only used the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] to personalize the page.</span></span>

### <a name="unlocking-the-page"></a><span data-ttu-id="b8b19-113">De pagina ontgrendelen</span><span class="sxs-lookup"><span data-stu-id="b8b19-113">Unlocking the Page</span></span>

<span data-ttu-id="b8b19-114">Als u een pagina wilt ontgrendelen en door wilt gaan met personaliseren, kiest u het pictogram ![Personaliseringsvergrendeling](media/personalization-lock-icon.png "Personalisatievergrendeling") en kiest u vervolgens de actie **Ontgrendelen**.</span><span class="sxs-lookup"><span data-stu-id="b8b19-114">If you want to unlock a page and continue personalizing it, choose the ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon, and then choose the **Unlock** action.</span></span>  

<span data-ttu-id="b8b19-115">Voordat u de pagina ontgrendelt, houdt u rekening met het volgende:</span><span class="sxs-lookup"><span data-stu-id="b8b19-115">Before you unlock the page, be aware of the following:</span></span>

- <span data-ttu-id="b8b19-116">De huidige personalisatie van de pagina wordt gewist.</span><span class="sxs-lookup"><span data-stu-id="b8b19-116">The current personalization of the page will be cleared.</span></span> <span data-ttu-id="b8b19-117">De pagina keert terug naar de oorspronkelijke indeling en u moet opnieuw beginnen.</span><span class="sxs-lookup"><span data-stu-id="b8b19-117">The page will go back to its original layout, and you will have to start from scratch.</span></span>

- <span data-ttu-id="b8b19-118">In de [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] blijft de pagina zoals deze is en hebben de nieuwe personalisatiewijzigingen die in de Business Central-client zijn aangebracht, geen invloed.</span><span class="sxs-lookup"><span data-stu-id="b8b19-118">In the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], the page will remain as-is and will not be affected by the new personalization changes made in the Business Central client.</span></span> <span data-ttu-id="b8b19-119">Vanaf nu zijn de personalisatie in de [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] en in Business Central volledig gescheiden van elkaar.</span><span class="sxs-lookup"><span data-stu-id="b8b19-119">Going forward, the personalization in the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] and Business Central client will be completely separate from each other.</span></span>

## <a name="blocked-from-personalizing"></a><span data-ttu-id="b8b19-120">Geblokkeerd tegen personaliseren</span><span class="sxs-lookup"><span data-stu-id="b8b19-120">Blocked from Personalizing</span></span>

<span data-ttu-id="b8b19-121">Als de banner **Personaliseren** het pictogram ![Personalisatie geblokkeerd](media/personalization-blocked-icon.png "Personalisatie geblokkeerd") bevat, betekent dit dat u geblokkeerd wordt om personalisatie op de pagina aan te brengen.</span><span class="sxs-lookup"><span data-stu-id="b8b19-121">If there is a ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon in the **Personalizing** banner, this means that you are blocked from doing any personalization to the page.</span></span>

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked](media/personalization-blocked.png "Personalize lock") -->

<span data-ttu-id="b8b19-122">De reden hiervoor is dat het rolcentrum of de rol die op dat moment aan uw gebruikersaccount is gekoppeld, deze pagina specifiek voor uw rol wijzigt.</span><span class="sxs-lookup"><span data-stu-id="b8b19-122">The reason for this is that the Role Center or role that is currently associated with your user account modifies this page specifically for your role.</span></span> <span data-ttu-id="b8b19-123">Neem contact op met uw beheerder voor hulp.</span><span class="sxs-lookup"><span data-stu-id="b8b19-123">Contact your administrator for assistance.</span></span> <span data-ttu-id="b8b19-124">U kunt ook overschakelen naar een rolcentrum met rolaanpassing voor deze pagina.</span><span class="sxs-lookup"><span data-stu-id="b8b19-124">Alternatively, try switching to a Role Center that does include role-tailoring for this page.</span></span> <span data-ttu-id="b8b19-125">Zie voor meer informatie [Basisinstellingen wijzigen](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="b8b19-125">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b8b19-126">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b8b19-126">See Also</span></span>
[<span data-ttu-id="b8b19-127">Uw werkruimte personaliseren</span><span class="sxs-lookup"><span data-stu-id="b8b19-127">Personalize Your Workspace</span></span>](ui-personalization-user.md)  
[<span data-ttu-id="b8b19-128">Pagina's aanpassen voor profielen</span><span class="sxs-lookup"><span data-stu-id="b8b19-128">Customize Pages for Profiles</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="b8b19-129">Basisinstellingen wijzigen</span><span class="sxs-lookup"><span data-stu-id="b8b19-129">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="b8b19-130">Wijzigen welke functies worden weergegeven</span><span class="sxs-lookup"><span data-stu-id="b8b19-130">Change Which Features are Displayed</span></span>](ui-experiences.md)  
