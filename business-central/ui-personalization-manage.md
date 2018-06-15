---
title: Personalisatie beheren als beheerder in Financials | Microsoft Docs
description: Meer informatie over hoe u de gebruikersinterface kunt aanpassen aan uw manier van werken.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 07/26/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 7c346455a9e27d7274b116754f1d594484b95d67
ms.openlocfilehash: 2d9b45bf21d325e60beadedfc94827d7f3fda075
ms.contentlocale: nl-be
ms.lasthandoff: 04/18/2018

---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="59db1-103">Personalisaties beheren als beheerder</span><span class="sxs-lookup"><span data-stu-id="59db1-103">Managing Personalization as an Administrator</span></span>
<!--NAV in the Web client-->
<span data-ttu-id="59db1-104">Gebruikers kunnen hun werkruimte aan hun eigen voorkeuren aanpassen.</span><span class="sxs-lookup"><span data-stu-id="59db1-104">Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="59db1-105">Als beheerder kunt u personalisaties bewaken en beheren door voor gebruikers de mogelijkheid uit te schakelen om pagina´s te personaliseren, en door alle personalisaties die door gebruikers zijn gemaakt, te wissen.</span><span class="sxs-lookup"><span data-stu-id="59db1-105">As an administrator, you can control and manage personalization by disabling the ability for users to personalize pages and clearing any page personalizations that users have made.</span></span>

## <a name="disable-personalization-for-a-profile"></a><span data-ttu-id="59db1-106">Personalisatie uitschakelen voor een profiel</span><span class="sxs-lookup"><span data-stu-id="59db1-106">Disable personalization for a profile</span></span>
<span data-ttu-id="59db1-107">U kunt voorkomen dat alle gebruikers die tot een bepaald profiel behoren, in staat zijn hun pagina's te personaliseren.</span><span class="sxs-lookup"><span data-stu-id="59db1-107">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>
1.  <span data-ttu-id="59db1-108">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Profielen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="59db1-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Profiles**, and then choose the related link.</span></span>
2.  <span data-ttu-id="59db1-109">Selecteer in de lijst het profiel dat u wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="59db1-109">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="59db1-110">Selecteer het selectievakje **Personalisering deactiveren** en kies vervolgens de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="59db1-110">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

## <a name="clear-user-personalizations"></a><span data-ttu-id="59db1-111">Gebruikerspersonalisaties wissen</span><span class="sxs-lookup"><span data-stu-id="59db1-111">Clear user personalizations</span></span>

<span data-ttu-id="59db1-112">Door paginapersonalisaties te wissen wordt de pagina teruggezet naar de oorspronkelijke layout die deze had voordat de personalisatie werd doorgevoerd.</span><span class="sxs-lookup"><span data-stu-id="59db1-112">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="59db1-113">Er zijn twee manieren om de personalisaties te wissen die door gebruikers aan pagina's zijn aangebracht: met de pagina **Pers. gebruikersinstellingen verwijderen** en met de pagina **Gebruikerspersonalisatiekaart**.</span><span class="sxs-lookup"><span data-stu-id="59db1-113">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** page and using the **User Personalization Card** page.</span></span>

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="59db1-114">Personalisaties wissen met de pagina Pers. gebruikersinstellingen verwijderen.</span><span class="sxs-lookup"><span data-stu-id="59db1-114">Clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="59db1-115">Met de pagina **Pers. gebruikersinstellingen verwijderen** kunt u personalisaties voor elke gebruiker afzonderlijk per pagina wissen.</span><span class="sxs-lookup"><span data-stu-id="59db1-115">The **Delete User Personalization** page enables you to clear personalizations on a per-page basis for each user individually.</span></span>

1.  <span data-ttu-id="59db1-116">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Pers. gebruikersinstellingen verwijderen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="59db1-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="59db1-117">De pagina bevat alle pagina's die zijn gepersonaliseerd en gebruiker waartoe ze behoren.</span><span class="sxs-lookup"><span data-stu-id="59db1-117">The page lists all the pages that have been personalized and the user it belongs to.</span></span>

    >[!NOTE]
    > <span data-ttu-id="59db1-118">Een vinkje in de kolommen **Oude persoonlijke instellingen** geeft aan dat de personalisatie is uitgevoerd in een oudere versie van [!INCLUDE[d365fin](includes/d365fin_md.md)], die anders met personalisatie omging dan nu het geval is.</span><span class="sxs-lookup"><span data-stu-id="59db1-118">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="59db1-119">Gebruikers die proberen deze pagina's te personaliseren zijn hiertoe niet in staat, tenzij ze ervoor kiezen de pagina te ontgrendelen.</span><span class="sxs-lookup"><span data-stu-id="59db1-119">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="59db1-120">Zie voor meer informatie [Waarom is een pagina vergrendeld voor personaliseren?](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="59db1-120">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="59db1-121">Selecteer het gegeven dat u wilt verwijderen en kies de actie **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="59db1-121">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="59db1-122">De gebruiker ziet de wijzigingen de volgende keer dat hij of zij zich aanmeldt.</span><span class="sxs-lookup"><span data-stu-id="59db1-122">The user will see the changes the next time they sign-in.</span></span>

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="59db1-123">Personalisaties wissen met de pagina Gebruikerspersonalisatiekaart.</span><span class="sxs-lookup"><span data-stu-id="59db1-123">Clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="59db1-124">Met de pagina **Gebruikerspersonalisatiekaart** kunt u de personalisaties op alle pagina´s voor een bepaalde gebruiker wissen.</span><span class="sxs-lookup"><span data-stu-id="59db1-124">The **User Personalization Card** page enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="59db1-125">Hiervoor hebt u schrijfmachtiging nodig voor tabel 2000000072 **Profiel**.</span><span class="sxs-lookup"><span data-stu-id="59db1-125">This requires write permission to Table 2000000072 **Profile**.</span></span>

1.  <span data-ttu-id="59db1-126">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Gebruikerspersonalisatie** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="59db1-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="59db1-127">De pagina **Gebruikerspersonalisatie** bevat alle gebruikers waarvoor mogelijk gepersonaliseerde pagina's voorkomen.</span><span class="sxs-lookup"><span data-stu-id="59db1-127">The **User Personalization** page lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="59db1-128">Als u een gebruikers-ID niet kunt vinden in de lijst, bestaan er geen gepersonaliseerde pagina´s voor.</span><span class="sxs-lookup"><span data-stu-id="59db1-128">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span>

2. <span data-ttu-id="59db1-129">Selecteer de gebruiker in de lijst en kies vervolgens de actie **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="59db1-129">Select the user from the list, and then choose the **Edit** action.</span></span>

3.  <span data-ttu-id="59db1-130">Op het tabblad **Acties** kiest **Aangepaste pagina's wissen**.</span><span class="sxs-lookup"><span data-stu-id="59db1-130">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="59db1-131">De gebruiker ziet de wijzigingen de volgende keer dat hij of zij zich aanmeldt.</span><span class="sxs-lookup"><span data-stu-id="59db1-131">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="59db1-132">Zie ook</span><span class="sxs-lookup"><span data-stu-id="59db1-132">See Also</span></span>
[<span data-ttu-id="59db1-133">Het personaliseren van uw werkruimte</span><span class="sxs-lookup"><span data-stu-id="59db1-133">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="59db1-134">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="59db1-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="59db1-135">Basisinstellingen wijzigen</span><span class="sxs-lookup"><span data-stu-id="59db1-135">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="59db1-136">Wijzigen welke functies worden weergegeven</span><span class="sxs-lookup"><span data-stu-id="59db1-136">Changing Which Features are Displayed</span></span>](ui-experiences.md)  

