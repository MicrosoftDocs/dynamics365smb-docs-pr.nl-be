---
title: Gebruikers en rollen beheren | Microsoft Docs
description: Leren hoe u gebruikers en rolcentra beheert in Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: profiles, users
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1a94d023424c6eceb93af6e9ca89a90a3a94e996
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a><span data-ttu-id="11a15-103">Gebruikers, profielen en rolcentra</span><span class="sxs-lookup"><span data-stu-id="11a15-103">Understanding Users, Profiles, and Role Centers</span></span>

<span data-ttu-id="11a15-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)] worden gebruikers toegevoegd door een beheerder die gebruikers tevens toegang geeft tot de gebieden van [!INCLUDE[d365fin](includes/d365fin_md.md)] die ze voor hun werk nodig hebben.</span><span class="sxs-lookup"><span data-stu-id="11a15-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], users are added by an administrator who also gives users access to the areas of [!INCLUDE[d365fin](includes/d365fin_md.md)] that they need in their work.</span></span>  

<span data-ttu-id="11a15-105">Toegang tot functionaliteit wordt beheerd door middel van *gebruikersgroepen* en *profielen*.</span><span class="sxs-lookup"><span data-stu-id="11a15-105">Access to functionality is managed through *user groups* and *profiles*.</span></span> <span data-ttu-id="11a15-106">Als beheerder kunt u profielen toevoegen en verwijderen als onderdeel van uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-abonnement en kunt u gebruikersmachtigingen toewijzen met behulp van gebruikersgroepen.</span><span class="sxs-lookup"><span data-stu-id="11a15-106">As an administrator, you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription, and you can assign users permissions through user groups.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="11a15-107">Gebruikers toevoegen</span><span class="sxs-lookup"><span data-stu-id="11a15-107">Adding Users</span></span>

<span data-ttu-id="11a15-108">Als u gebruikers wilt toevoegen in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, moet de Office 365-beheerder van uw bedrijf eerst de gebruikers in het Office 365-beheercentrum maken.</span><span class="sxs-lookup"><span data-stu-id="11a15-108">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="11a15-109">Zie voor meer informatie [Gebruikers aan Office 365 toevoegen voor bedrijven](https://aka.ms/CreateOffice365Users).</span><span class="sxs-lookup"><span data-stu-id="11a15-109">For more information, see [Add Users to Office 365 for business](https://aka.ms/CreateOffice365Users).</span></span>

<span data-ttu-id="11a15-110">Vervolgens kan de beheerder machtigingen toewijzen aan elke gebruiker en groep gebruikers.</span><span class="sxs-lookup"><span data-stu-id="11a15-110">Then, the administrator can assign permissions to each user and groups of users.</span></span> <span data-ttu-id="11a15-111">Zie [Gebruikers en machtigingen beheren](ui-how-users-permissions.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="11a15-111">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

### <a name="users-of-on-premises-deployments"></a><span data-ttu-id="11a15-112">Gebruikers van on-premises implementaties</span><span class="sxs-lookup"><span data-stu-id="11a15-112">Users of on-premises deployments</span></span>

<span data-ttu-id="11a15-113">Voor on-premises implementaties van [!INCLUDE[d365fin](includes/d365fin_md.md)] kan de beheerder kiezen tussen verschillende autorisatiemechanismen voor referenties voor gebruikers.</span><span class="sxs-lookup"><span data-stu-id="11a15-113">For on-premises deployments of [!INCLUDE[d365fin](includes/d365fin_md.md)], the administrator can choose between different credential authorization mechanisms for users.</span></span> <span data-ttu-id="11a15-114">Wanneer u dan een gebruiker maakt, geeft u verschillende informatie op, afhankelijk van het referentietype dat u in de specifieke [!INCLUDE[server](includes/server.md)]-instantie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="11a15-114">Then, when you create a user, you provide different information depending on the credential type that you are using in the specific [!INCLUDE[server](includes/server.md)] instance.</span></span> <span data-ttu-id="11a15-115">Zie voor meer informatie [Verificatie en referentietypen](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in het gedeelte Beheer van de ontwikkelaars- en ITPro-inhoud voor [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="11a15-115">For more information, see the [Authentication and Credential Types](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in the Administration section of the developer and ITPro content for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="profiles"></a><span data-ttu-id="11a15-116">Profielen</span><span class="sxs-lookup"><span data-stu-id="11a15-116">Profiles</span></span>

<span data-ttu-id="11a15-117">Aan alle personen in het bedrijf die toegang tot [!INCLUDE[d365fin](includes/d365fin_md.md)] hebben, wordt een *profiel* toegewezen dat ze toegang biedt tot een *rolcentrum*.</span><span class="sxs-lookup"><span data-stu-id="11a15-117">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span>

<span data-ttu-id="11a15-118">Profielen zijn verzamelingen [!INCLUDE[d365fin](includes/d365fin_md.md)]-gebruikers die hetzelfde rolcentrum delen.</span><span class="sxs-lookup"><span data-stu-id="11a15-118">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="11a15-119">Een rolcentrum is het invoerpunt en de homepage voor [!INCLUDE[d365fin](includes/d365fin_md.md)], waarmee u snel toegang krijgt tot de belangrijkste taken en verschillende inzichten en KPI's over uw werk kunt weergeven.</span><span class="sxs-lookup"><span data-stu-id="11a15-119">A Role Center is the entry point and home page for [!INCLUDE[d365fin](includes/d365fin_md.md)] that gives you quick access to your most important tasks and displays various insights and key performance indicators (KPIs) about your work.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="11a15-120">In de huidige versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] online kunt u geen profielen toevoegen, bewerken of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="11a15-120">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] online, you cannot add, edit, or delete profiles.</span></span>  

## <a name="configuration-and-personalization"></a><span data-ttu-id="11a15-121">Configuratie en personalisatie</span><span class="sxs-lookup"><span data-stu-id="11a15-121">Configuration and Personalization</span></span>
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->
<span data-ttu-id="11a15-122">Gebruikers passen de gebruikersinterface van hun persoonlijke versie aan door de gebruikersinterface onder hun eigen gebruikersaanmelding te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="11a15-122">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="11a15-123">Deze personalisatie kan worden verwijderd door de beheerder.</span><span class="sxs-lookup"><span data-stu-id="11a15-123">This personalization can be deleted by the administrator.</span></span> <span data-ttu-id="11a15-124">Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="11a15-124">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="11a15-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="11a15-125">See Also</span></span>  
[<span data-ttu-id="11a15-126">Gebruikers en machtigingen beheren</span><span class="sxs-lookup"><span data-stu-id="11a15-126">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
[<span data-ttu-id="11a15-127">Personalisaties beheren als beheerder</span><span class="sxs-lookup"><span data-stu-id="11a15-127">Managing Personalization as an Administrator</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="11a15-128">Het personaliseren van uw werkruimte</span><span class="sxs-lookup"><span data-stu-id="11a15-128">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  

