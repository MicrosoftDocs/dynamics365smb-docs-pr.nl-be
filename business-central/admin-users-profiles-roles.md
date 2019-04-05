---
title: Gebruikers en rollen beheren | Microsoft Docs
description: Leren hoe u gebruikers en rolcentra beheert in Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 10/24/2018
ms.author: edupont
ms.openlocfilehash: 7ecd8a5ad2b321d4d1683047e70ede90c7ce229f
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816806"
---
# <a name="understanding-users-profiles-and-role-centers"></a><span data-ttu-id="2e86b-103">Gebruikers, profielen en rolcentra</span><span class="sxs-lookup"><span data-stu-id="2e86b-103">Understanding Users, Profiles, and Role Centers</span></span>

<span data-ttu-id="2e86b-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)] worden gebruikers toegevoegd door een beheerder die gebruikers tevens toegang geeft tot de gebieden van [!INCLUDE[d365fin](includes/d365fin_md.md)] die ze voor hun werk nodig hebben.</span><span class="sxs-lookup"><span data-stu-id="2e86b-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], users are added by an administrator who also gives users access to the areas of [!INCLUDE[d365fin](includes/d365fin_md.md)] that they need in their work.</span></span>  

<span data-ttu-id="2e86b-105">Toegang tot functionaliteit wordt beheerd door middel van *gebruikersgroepen* en *profielen*.</span><span class="sxs-lookup"><span data-stu-id="2e86b-105">Access to functionality is managed through *user groups* and *profiles*.</span></span> <span data-ttu-id="2e86b-106">Als beheerder kunt u profielen toevoegen en verwijderen als onderdeel van uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-abonnement en kunt u gebruikersmachtigingen toewijzen met behulp van gebruikersgroepen.</span><span class="sxs-lookup"><span data-stu-id="2e86b-106">As an administrator, you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription, and you can assign users permissions through user groups.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="2e86b-107">Gebruikers toevoegen</span><span class="sxs-lookup"><span data-stu-id="2e86b-107">Adding Users</span></span>

<span data-ttu-id="2e86b-108">Als u gebruikers wilt toevoegen in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, moet de Office 365-beheerder van uw bedrijf eerst de gebruikers in het Office 365-beheercentrum maken.</span><span class="sxs-lookup"><span data-stu-id="2e86b-108">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="2e86b-109">Zie voor meer informatie [Gebruikers aan Office 365 toevoegen voor bedrijven](https://aka.ms/CreateOffice365Users).</span><span class="sxs-lookup"><span data-stu-id="2e86b-109">For more information, see [Add Users to Office 365 for business](https://aka.ms/CreateOffice365Users).</span></span>

<span data-ttu-id="2e86b-110">Vervolgens kan de beheerder machtigingen toewijzen aan elke gebruiker en groep gebruikers.</span><span class="sxs-lookup"><span data-stu-id="2e86b-110">Then, the administrator can assign permissions to each user and groups of users.</span></span> <span data-ttu-id="2e86b-111">Zie [Gebruikers en machtigingen beheren](ui-how-users-permissions.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="2e86b-111">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

<span data-ttu-id="2e86b-112">De krachtigste machtigingen die een gebruiker kan hebben, is de machtigingenset SUPER.</span><span class="sxs-lookup"><span data-stu-id="2e86b-112">The most powerful permissions that a user can have is the SUPER permission set.</span></span> <span data-ttu-id="2e86b-113">Elk bedrijf moet minimaal één gebruiker met deze machtigingenset hebben, maar het is een best practice om elke gebruiker machtigingen te geven die overeenkomen met hun werkbehoeften in [!INCLUDE[prodshort](includes/prodshort.md)] en niet meer dan dat.</span><span class="sxs-lookup"><span data-stu-id="2e86b-113">Each company must have at least one user with this permission set, but it is a best practice to give each user permissions that match their work needs in [!INCLUDE[prodshort](includes/prodshort.md)] and not more than that.</span></span> <span data-ttu-id="2e86b-114">Dit helpt zorgen dat gebruikers bijvoorbeeld alleen toegang hebben tot gegevens die relevant zijn voor hun werk.</span><span class="sxs-lookup"><span data-stu-id="2e86b-114">This helps ensure that users only have access to data that is relevant to their work, for example.</span></span>  

> [!TIP]
> <span data-ttu-id="2e86b-115">Het is een best practice om ervoor te zorgen dat de Office 365-beheerder ook de machtigingenset SUPER heeft in [!INCLUDE[prodshort](includes/prodshort.md)] omdat dat veel beheertaken eenvoudiger maakt, inclusief het instellen van integratie met andere apps.</span><span class="sxs-lookup"><span data-stu-id="2e86b-115">It's a best practice to make sure that the Office 365 administrator also has the SUPER permission set in [!INCLUDE[prodshort](includes/prodshort.md)] because that makes many administrative tasks easier, including setting up integration with other apps.</span></span>

### <a name="users-of-on-premises-deployments"></a><span data-ttu-id="2e86b-116">Gebruikers van on-premises implementaties</span><span class="sxs-lookup"><span data-stu-id="2e86b-116">Users of on-premises deployments</span></span>

<span data-ttu-id="2e86b-117">Voor on-premises implementaties van [!INCLUDE[d365fin](includes/d365fin_md.md)] kan de beheerder kiezen tussen verschillende autorisatiemechanismen voor referenties voor gebruikers.</span><span class="sxs-lookup"><span data-stu-id="2e86b-117">For on-premises deployments of [!INCLUDE[d365fin](includes/d365fin_md.md)], the administrator can choose between different credential authorization mechanisms for users.</span></span> <span data-ttu-id="2e86b-118">Wanneer u dan een gebruiker maakt, geeft u verschillende informatie op, afhankelijk van het referentietype dat u in de specifieke [!INCLUDE[server](includes/server.md)]-instantie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="2e86b-118">Then, when you create a user, you provide different information depending on the credential type that you are using in the specific [!INCLUDE[server](includes/server.md)] instance.</span></span> <span data-ttu-id="2e86b-119">Zie voor meer informatie [Verificatie en referentietypen](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in het gedeelte Beheer van de ontwikkelaars- en ITPro-inhoud voor [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2e86b-119">For more information, see the [Authentication and Credential Types](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in the Administration section of the developer and ITPro content for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="profiles"></a><span data-ttu-id="2e86b-120">Profielen</span><span class="sxs-lookup"><span data-stu-id="2e86b-120">Profiles</span></span>

<span data-ttu-id="2e86b-121">Aan alle personen in het bedrijf die toegang tot [!INCLUDE[d365fin](includes/d365fin_md.md)] hebben, wordt een *profiel* toegewezen dat ze toegang biedt tot een *rolcentrum*.</span><span class="sxs-lookup"><span data-stu-id="2e86b-121">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span>

<span data-ttu-id="2e86b-122">Profielen zijn verzamelingen [!INCLUDE[d365fin](includes/d365fin_md.md)]-gebruikers die hetzelfde rolcentrum delen.</span><span class="sxs-lookup"><span data-stu-id="2e86b-122">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="2e86b-123">Een rolcentrum is het invoerpunt en de homepage voor [!INCLUDE[d365fin](includes/d365fin_md.md)], waarmee u snel toegang krijgt tot de belangrijkste taken en verschillende inzichten en KPI's over uw werk kunt weergeven.</span><span class="sxs-lookup"><span data-stu-id="2e86b-123">A Role Center is the entry point and home page for [!INCLUDE[d365fin](includes/d365fin_md.md)] that gives you quick access to your most important tasks and displays various insights and key performance indicators (KPIs) about your work.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2e86b-124">In de huidige versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] online kunt u geen profielen toevoegen, bewerken of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="2e86b-124">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] online, you cannot add, edit, or delete profiles.</span></span>  

### <a name="CreateProfile"></a><span data-ttu-id="2e86b-125">Een profiel maken</span><span class="sxs-lookup"><span data-stu-id="2e86b-125">Create a profile</span></span>

1.  <span data-ttu-id="2e86b-126">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Profieloverzicht** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="2e86b-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Profile List**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="2e86b-127">Kies op de pagina **Profieloverzicht** de actie **Nieuw** om de pagina **Nieuwe profielkaart** te openen.</span><span class="sxs-lookup"><span data-stu-id="2e86b-127">On the **Profile List** page, choose the **New** action to open the **New Profile Card** page.</span></span>  

3.  <span data-ttu-id="2e86b-128">Voer in het veld **Profiel-id** een naam in die de beoogde rol van de gebruikers beschrijft.</span><span class="sxs-lookup"><span data-stu-id="2e86b-128">In the **Profile ID** field, enter a name that describes the intended role of the users.</span></span>  

4.  <span data-ttu-id="2e86b-129">Voer in het veld **Beschrijving** een beschrijving in van de profiel-id in, bijvoorbeeld **Orderverwerker**.</span><span class="sxs-lookup"><span data-stu-id="2e86b-129">In the **Description** field, enter a description of the Profile ID, for example, **Order Processor**.</span></span>  

5.  <span data-ttu-id="2e86b-130">Stel het veld **Rolcentrum-id** in op het rolcentrum dat u aan het profiel wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="2e86b-130">Set the **Role Center ID** field to the Role Center that you want to assign to the profile.</span></span>  

<span data-ttu-id="2e86b-131">De procedure voor het wijzigen van een bestaand profiel is hetzelfde, behalve dat u een bestaand profiel selecteert op de pagina **Profieloverzicht** in plaats van de actie **Nieuw** te kiezen.</span><span class="sxs-lookup"><span data-stu-id="2e86b-131">The procedure for modifying an existing profile is the same, except you select an existing profile on the **Profile List** page instead of choosing the **New** action.</span></span>  


### <a name="copy-a-profile"></a><span data-ttu-id="2e86b-132">Een profiel kopiëren</span><span class="sxs-lookup"><span data-stu-id="2e86b-132">Copy a profile</span></span>
<span data-ttu-id="2e86b-133">Een profiel kopiëren kan u tijd besparen als u dezelfde instellingen voor een profiel wilt gebruiken en u slechts enkele instellingen wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="2e86b-133">Copying a profile can save you time if you want to use similar settings on a profile and you only want to change a few settings.</span></span>

1.  <span data-ttu-id="2e86b-134">Open het profiel dat u wilt kopiëren en kies vervolgens de actie **Profiel kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="2e86b-134">Open the profile that you want to copy, and then choose the **Copy Profile** action.</span></span>

2.  <span data-ttu-id="2e86b-135">Voer in het veld **Nieuwe profiel-id** een naam in voor het profiel dat u wilt kopiëren.</span><span class="sxs-lookup"><span data-stu-id="2e86b-135">In **New Profile ID** field, enter a name for the profile that you want to copy.</span></span>

3.  <span data-ttu-id="2e86b-136">Stel het veld **Nieuw profielbereik** op een van de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="2e86b-136">Set the **New Profile Scope** field to one of the following:</span></span>

    - <span data-ttu-id="2e86b-137">**Systeem** om het profiel voor de nieuwe tenantdatabases beschikbaar te maken die de toepassing gebruikt.</span><span class="sxs-lookup"><span data-stu-id="2e86b-137">**System** to make the new profile available to all tenant databases that use the application.</span></span>
    - <span data-ttu-id="2e86b-138">**Tenant** om het nieuwe profiel alleen voor de huidige tenantdatabase beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="2e86b-138">**Tenant** to make the new profile available to just the current tenant database.</span></span>
4. <span data-ttu-id="2e86b-139">Kies de knop **OK** als u gereed bent.</span><span class="sxs-lookup"><span data-stu-id="2e86b-139">Choose the **OK** button when done.</span></span>

### <a name="ExportImportProfile"></a><span data-ttu-id="2e86b-140">Profielen exporteren en importeren</span><span class="sxs-lookup"><span data-stu-id="2e86b-140">Export and import profiles</span></span>

<span data-ttu-id="2e86b-141">U kunt profielen als XML-bestanden van en naar een [!INCLUDE[d365fin](includes/d365fin_md.md)] database exporteren en importeren.</span><span class="sxs-lookup"><span data-stu-id="2e86b-141">You can export and import profiles as XML files to and from the a [!INCLUDE[d365fin](includes/d365fin_md.md)] database.</span></span> <span data-ttu-id="2e86b-142">Het exporteren en importeren van een profiel kan u tijd besparen als u de gebruikersinterface configureert, omdat u een bestaande profielconfiguratie opnieuw gebruikt in plaats van dat een profiel helemaal vanaf het begin moet worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="2e86b-142">Exporting and importing a profile can save you time when configuring the user interface because you reuse an existing profile configuration instead of having to configure a profile from scratch.</span></span> <span data-ttu-id="2e86b-143">Als u een profiel hebt dat in een [!INCLUDE[d365fin](includes/d365fin_md.md)] database is geconfigureerd en u alle of een aantal van dezelfde profielconfiguraties in een andere database opnieuw wilt gebruiken, kunt u het profiel naar een XML-bestand exporteren.</span><span class="sxs-lookup"><span data-stu-id="2e86b-143">If you have a profile that is configured in a [!INCLUDE[d365fin](includes/d365fin_md.md)] database and you would like to reuse all or some of the same profile configurations in another database, you can export the profile to an XML file.</span></span> <span data-ttu-id="2e86b-144">Vervolgens kunt u het XML-profielbestand in een andere database importeren.</span><span class="sxs-lookup"><span data-stu-id="2e86b-144">Then, you can import the profile XML file into the other database.</span></span>

-   <span data-ttu-id="2e86b-145">Als u een profiel wilt exporteren, kunt u de actie **Profielen exporteren** in het **Profieloverzicht** of de pagina **Profielkaart** kiezen of u kunt zoeken naar de pagina **Profielen exporteren** en deze openen.</span><span class="sxs-lookup"><span data-stu-id="2e86b-145">To export a profile, you can either choose the **Export Profiles** action from the **Profile List** or **Profile Card** page or you can search for and open the **Export Profiles** page.</span></span> <span data-ttu-id="2e86b-146">Sla het XML-bestand op op een locatie op uw computer of netwerk.</span><span class="sxs-lookup"><span data-stu-id="2e86b-146">Save the XML file to a location on your computer or network.</span></span>

-   <span data-ttu-id="2e86b-147">Als u een profiel wilt importeren, kunt u de actie **Profiel importeren** op de pagina **Profieloverzicht** kiezen of kunt u de pagina **Profielen importeren** kiezen.</span><span class="sxs-lookup"><span data-stu-id="2e86b-147">To import a profile, you can either choose the **Import Profile** action from the **Profile List** page, or you can search for and open the **Import Profiles** page.</span></span> 

    > [!NOTE]  
    >  <span data-ttu-id="2e86b-148">U kunt geen profiel importeren dat al bestaat in de database, zelfs als het XML-bestand anders is genoemd of andere inhoud heeft.</span><span class="sxs-lookup"><span data-stu-id="2e86b-148">You cannot import a profile that already exists in the database, even though the XML file is named differently or has different content.</span></span> <span data-ttu-id="2e86b-149">U moet het bestaande profiel verwijderen voordat u het nieuwe profiel kunt importeren.</span><span class="sxs-lookup"><span data-stu-id="2e86b-149">You must delete the existing profile before you can import the new profile.</span></span>


## <a name="configuration-and-personalization"></a><span data-ttu-id="2e86b-150">Configuratie en personalisatie</span><span class="sxs-lookup"><span data-stu-id="2e86b-150">Configuration and Personalization</span></span>
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->

<span data-ttu-id="2e86b-151">Gebruikers passen de gebruikersinterface van hun persoonlijke versie aan door de gebruikersinterface onder hun eigen gebruikersaanmelding te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="2e86b-151">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="2e86b-152">Deze personalisatie kan worden verwijderd door de beheerder.</span><span class="sxs-lookup"><span data-stu-id="2e86b-152">This personalization can be deleted by the administrator.</span></span> <span data-ttu-id="2e86b-153">Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="2e86b-153">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="2e86b-154">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2e86b-154">See Also</span></span>  
[<span data-ttu-id="2e86b-155">Gebruikers en machtigingen beheren</span><span class="sxs-lookup"><span data-stu-id="2e86b-155">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
[<span data-ttu-id="2e86b-156">Personalisaties beheren als beheerder</span><span class="sxs-lookup"><span data-stu-id="2e86b-156">Managing Personalization as an Administrator</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="2e86b-157">Het personaliseren van uw werkruimte</span><span class="sxs-lookup"><span data-stu-id="2e86b-157">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
