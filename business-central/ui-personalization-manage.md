---
title: Personalisatie beheren als beheerder in Business Central | Microsoft Docs
description: Meer informatie over hoe u de gebruikersinterface kunt aanpassen aan uw manier van werken.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 08/16/2019
ms.author: jswymer
ms.openlocfilehash: 268d61e05f84643abe8eeeb283bd035e0247fe1c
ms.sourcegitcommit: 81b6062194bf04d8052a3cd394cc0b41e3f53e6d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 08/20/2019
ms.locfileid: "1887749"
---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="9e011-103">Personalisaties beheren als beheerder</span><span class="sxs-lookup"><span data-stu-id="9e011-103">Managing Personalization as an Administrator</span></span>

<span data-ttu-id="9e011-104"> Gebruikers kunnen hun werkruimte aan hun eigen voorkeuren aanpassen.</span><span class="sxs-lookup"><span data-stu-id="9e011-104">Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="9e011-105">Als beheerder bepaalt en beheert u personalisatie door:</span><span class="sxs-lookup"><span data-stu-id="9e011-105">As an administrator, you control and manage personalization by:</span></span>

-   <span data-ttu-id="9e011-106">De personalisatie in of uit te schakelen voor de hele toepassing (alleen on-premises installatie).</span><span class="sxs-lookup"><span data-stu-id="9e011-106">Enabling or disabling the personalization feature for the entire the application (on-premises installation only).</span></span>
-   <span data-ttu-id="9e011-107">De personalisatiefunctie in of uit te schakelen voor gebruikers van een specifiek profiel.</span><span class="sxs-lookup"><span data-stu-id="9e011-107">Enabling or disabling the personalization feature for users of a specific profile.</span></span>
-   <span data-ttu-id="9e011-108">Paginapersonalisaties te wissen die gebruikers hebben aangebracht.</span><span class="sxs-lookup"><span data-stu-id="9e011-108">Clearing any page personalizations that users have made.</span></span>

## <a name="EnablePersonalization"></a><span data-ttu-id="9e011-109">Personalisatie in- of uitschakelen (alleen on-premises)</span><span class="sxs-lookup"><span data-stu-id="9e011-109">To enable or disable personalization (On-Premises Only)</span></span>

<span data-ttu-id="9e011-110">Standaard is personalisatie niet ingeschakeld in de client.</span><span class="sxs-lookup"><span data-stu-id="9e011-110">By default, personalization is not enabled in the client.</span></span> <span data-ttu-id="9e011-111">U schakelt personalisatie in of uit door het configuratiebestand te wijzigen (navsettings.json) van het Business Central-webserverexemplaar dat de clients bedient.</span><span class="sxs-lookup"><span data-stu-id="9e011-111">You enable or disable personalization by modifying the configuration file (navsettings.json) of the Business Central Web Server instance that serves the clients.</span></span>

1. <span data-ttu-id="9e011-112">Als u personalisatie wilt inschakelen, voegt u de volgende regel toe aan het bestand navsettings.json:</span><span class="sxs-lookup"><span data-stu-id="9e011-112">To enable personalization, add the following line in the navsettings.json file:</span></span>

    ```
    "PersonalizationEnabled": "true"
    ```

    <span data-ttu-id="9e011-113">Als u personalisatie wilt uitschakelen, verwijdert u deze regel of wijzigt u deze in:</span><span class="sxs-lookup"><span data-stu-id="9e011-113">To disable personalization, remove this line or change it to:</span></span>

    ```
    "PersonalizationEnabled": "false"
    ```

    <span data-ttu-id="9e011-114">Voor meer informatie over hoe u het navsettings.json-bestand wijzigt raadpleegt u [Het bestand navsettings.json rechtstreeks wijzigen](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings)</span><span class="sxs-lookup"><span data-stu-id="9e011-114">For more information about how to modify the navsettings.json file, see [Modify the navsettings.json file directly](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).</span></span>

2. <span data-ttu-id="9e011-115">De toepassingssymbolen genereren en downloaden.</span><span class="sxs-lookup"><span data-stu-id="9e011-115">Generate and download the application symbols.</span></span>

    <span data-ttu-id="9e011-116">Deze stap is optioneel en is niet vereist om personalisatie in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="9e011-116">This step is optional, and not required to enable personalization.</span></span> <span data-ttu-id="9e011-117">Het zorgt echter dat nieuwe pagina's die worden gemaakt door ontwikkelaars, kunnen worden gepersonaliseerd.</span><span class="sxs-lookup"><span data-stu-id="9e011-117">However, it ensures that new pages that are created by developers can be personalized.</span></span>

    1. <span data-ttu-id="9e011-118">Eerst genereert u de symbolen door finsql.exe uit te voeren met de opdracht `generatesymbolreference`.</span><span class="sxs-lookup"><span data-stu-id="9e011-118">First, you generate the symbols by running finsql.exe with `generatesymbolreference` command.</span></span> <span data-ttu-id="9e011-119">Het finsql.exe-bestand bevindt zich in de installatiemap voor de [!INCLUDE[server](includes/server.md)] Dynamics NAV ontwikkelingsomgeving (CSIDE).</span><span class="sxs-lookup"><span data-stu-id="9e011-119">The finsql.exe file is located in the installation folder for the [!INCLUDE[server](includes/server.md)] and Dynamics NAV Development Environment (CSIDE).</span></span> <span data-ttu-id="9e011-120">Als u de symbolen wilt genereren, opent u een opdrachtprompt, wijzigt u de map waar het bestand is opgeslagen en voert u de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="9e011-120">To generate the symbols, open a command prompt, change to the directory where the file is store, and the run the following command:</span></span>

        ```
        finsql.exe Command=generatesymbolreference, Database="<Database Name>", ServerName=<SQL Server Name\<Server Instance>
        ```
    <span data-ttu-id="9e011-121">Voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="9e011-121">For example:</span></span>

        ```
        finsql.exe Command=generatesymbolreference, Database="Demo Database BC", ServerName=MySQLServer\BCDEMO
        ```

    <span data-ttu-id="9e011-122">Zie voor meer informatie [C/SIDE en AL naast elkaar uitvoeren](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).</span><span class="sxs-lookup"><span data-stu-id="9e011-122">For more information, see [Running C/SIDE and AL Side-by-Side](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).</span></span>

    2. <span data-ttu-id="9e011-123">Configureer het [!INCLUDE[nav_server_md](includes/nav_server_md.md)]-exemplaar zodat het **toepassingssymboolverwijzingen laadt bij opstarten van de server** (EnableSymbolLoadingAtServerStartup).</span><span class="sxs-lookup"><span data-stu-id="9e011-123">Configure [!INCLUDE[nav_server_md](includes/nav_server_md.md)] instance to **Enable loading application symbol references at server startup** (EnableSymbolLoadingAtServerStartup).</span></span> <span data-ttu-id="9e011-124">Zie [Business Central Server configureren](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="9e011-124">For more information, see [Configuring Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).</span></span>

## <a name="to-disable-personalization-for-a-profile"></a><span data-ttu-id="9e011-125">Personalisatie uitschakelen voor een profiel</span><span class="sxs-lookup"><span data-stu-id="9e011-125">To disable personalization for a profile</span></span>

<span data-ttu-id="9e011-126">U kunt voorkomen dat alle gebruikers die tot een bepaald profiel behoren, in staat zijn hun pagina's te personaliseren.</span><span class="sxs-lookup"><span data-stu-id="9e011-126">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>

1. <span data-ttu-id="9e011-127">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Profielen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="9e011-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="9e011-128">Selecteer in de lijst het profiel dat u wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="9e011-128">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="9e011-129">Selecteer het selectievakje **Personalisering deactiveren** en kies vervolgens de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e011-129">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

> [!NOTE]  
> <span data-ttu-id="9e011-130">In Business Central online kunt u personalisatie alleen uitschakelen voor een tenantprofiel, niet voor systeemprofielen.</span><span class="sxs-lookup"><span data-stu-id="9e011-130">In Business Central online, you can only disable personalization for a tenant profile, not for system profiles.</span></span> 

## <a name="to-clear-user-personalizations"></a><span data-ttu-id="9e011-131">Gebruikerspersonalisaties wissen</span><span class="sxs-lookup"><span data-stu-id="9e011-131">To clear user personalizations</span></span>

<span data-ttu-id="9e011-132">Door paginapersonalisaties te wissen wordt de pagina teruggezet naar de oorspronkelijke layout die deze had voordat de personalisatie werd doorgevoerd.</span><span class="sxs-lookup"><span data-stu-id="9e011-132">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="9e011-133">Er zijn twee manieren om de personalisaties te wissen die door gebruikers aan pagina's zijn aangebracht: met de pagina **Pers. gebruikersinstellingen verwijderen** en met de pagina **Gebruikerspersonalisatiekaart**.</span><span class="sxs-lookup"><span data-stu-id="9e011-133">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** page and using the **User Personalization Card** page.</span></span>

### <a name="to-clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="9e011-134">Gebruikerspersonalisaties wissen met de pagina Pers. gebruikersinstellingen verwijderen.</span><span class="sxs-lookup"><span data-stu-id="9e011-134">To clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="9e011-135">Met de pagina **Pers. gebruikersinstellingen verwijderen** kunt u personalisaties voor elke gebruiker afzonderlijk per pagina wissen.</span><span class="sxs-lookup"><span data-stu-id="9e011-135">The **Delete User Personalization** page enables you to clear personalizations on a per-page basis for each user individually.</span></span>

1. <span data-ttu-id="9e011-136">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Pers. gebruikersinstellingen verwijderen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="9e011-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="9e011-137">De pagina bevat alle pagina's die zijn gepersonaliseerd en gebruiker waartoe ze behoren.</span><span class="sxs-lookup"><span data-stu-id="9e011-137">The page lists all the pages that have been personalized and the user it belongs to.</span></span>

    >[!NOTE]
    > <span data-ttu-id="9e011-138">Een vinkje in de kolommen **Oude persoonlijke instellingen** geeft aan dat de personalisatie is uitgevoerd in een oudere versie van [!INCLUDE[d365fin](includes/d365fin_md.md)], die anders met personalisatie omging dan nu het geval is.</span><span class="sxs-lookup"><span data-stu-id="9e011-138">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="9e011-139">Gebruikers die proberen deze pagina's te personaliseren zijn hiertoe niet in staat, tenzij ze ervoor kiezen de pagina te ontgrendelen.</span><span class="sxs-lookup"><span data-stu-id="9e011-139">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="9e011-140">Zie voor meer informatie [Waarom is een pagina vergrendeld voor personaliseren?](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="9e011-140">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="9e011-141">Selecteer het gegeven dat u wilt verwijderen en kies de actie **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="9e011-141">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="9e011-142">De gebruiker ziet de wijzigingen de volgende keer dat hij of zij zich aanmeldt.</span><span class="sxs-lookup"><span data-stu-id="9e011-142">The user will see the changes the next time they sign-in.</span></span>

### <a name="to-clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="9e011-143">Gebruikerspersonalisaties wissen met de pagina Gebruikerspersonalisatiekaart.</span><span class="sxs-lookup"><span data-stu-id="9e011-143">To clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="9e011-144">Met de pagina **Gebruikerspersonalisatiekaart** kunt u de personalisaties op alle pagina´s voor een bepaalde gebruiker wissen.</span><span class="sxs-lookup"><span data-stu-id="9e011-144">The **User Personalization Card** page enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="9e011-145">Hiervoor hebt u schrijfmachtiging nodig voor tabel 2000000072 **Profiel**.</span><span class="sxs-lookup"><span data-stu-id="9e011-145">This requires write permission to Table 2000000072 **Profile**.</span></span>

1. <span data-ttu-id="9e011-146">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Pers. gebruikersinstellingen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="9e011-146">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="9e011-147">De pagina **Gebruikerspersonalisatie** bevat alle gebruikers waarvoor mogelijk gepersonaliseerde pagina's voorkomen.</span><span class="sxs-lookup"><span data-stu-id="9e011-147">The **User Personalization** page lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="9e011-148">Als u een gebruikers-ID niet kunt vinden in de lijst, bestaan er geen gepersonaliseerde pagina´s voor.</span><span class="sxs-lookup"><span data-stu-id="9e011-148">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span>

2. <span data-ttu-id="9e011-149">Selecteer de gebruiker in de lijst en kies vervolgens de actie **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="9e011-149">Select the user from the list, and then choose the **Edit** action.</span></span>

3. <span data-ttu-id="9e011-150">Op het tabblad **Acties** kiest **Aangepaste pagina's wissen**.</span><span class="sxs-lookup"><span data-stu-id="9e011-150">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="9e011-151">De gebruiker ziet de wijzigingen de volgende keer dat hij of zij zich aanmeldt.</span><span class="sxs-lookup"><span data-stu-id="9e011-151">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e011-152">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9e011-152">See Also</span></span>
[<span data-ttu-id="9e011-153">Het personaliseren van uw werkruimte</span><span class="sxs-lookup"><span data-stu-id="9e011-153">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="9e011-154">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9e011-154">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="9e011-155">Basisinstellingen wijzigen</span><span class="sxs-lookup"><span data-stu-id="9e011-155">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="9e011-156">Wijzigen welke functies worden weergegeven</span><span class="sxs-lookup"><span data-stu-id="9e011-156">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
