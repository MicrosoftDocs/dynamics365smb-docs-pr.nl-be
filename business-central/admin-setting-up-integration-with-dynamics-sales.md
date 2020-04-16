---
title: Gebruikersaccounts instellen voor integratie met Common Data Service | Microsoft Docs
description: Leer hoe u gebruikersaccounts instelt die de apps gebruiken om gegevens uit te wisselen, en die personen gebruiken om toegang te krijgen tot gegevens in de apps en deze te synchroniseren.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: ad10aa53b4fe6a8b9b65ad798c206fa251e08a7a
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196507"
---
# <a name="setting-up-user-accounts-for-integrating-with-common-data-service"></a><span data-ttu-id="c6755-103">Gebruikersaccounts instellen voor integratie met Common Data Service</span><span class="sxs-lookup"><span data-stu-id="c6755-103">Setting Up User Accounts for Integrating with Common Data Service</span></span>
<span data-ttu-id="c6755-104">Dit artikel geeft een overzicht van hoe u de gebruikersaccounts instelt die vereist zijn om [!INCLUDE[d365fin](includes/cds_long_md.md)] te integreren met [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c6755-104">This article provides an overview of how to set up the user accounts that are required to integrate [!INCLUDE[d365fin](includes/cds_long_md.md)] with [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="setting-up-the-administrator-user-account"></a><span data-ttu-id="c6755-105">Het beheerdersaccount instellen in Sales</span><span class="sxs-lookup"><span data-stu-id="c6755-105">Setting Up the Administrator User Account</span></span>
<span data-ttu-id="c6755-106">U moet uw beheerdersaccount toevoegen voor [!INCLUDE[d365fin](includes/d365fin_md.md)] als gebruiker in [!INCLUDE[d365fin](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c6755-106">You must add your administrator user account for [!INCLUDE[d365fin](includes/d365fin_md.md)] as a user in [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> <span data-ttu-id="c6755-107">Bij het opzetten van de verbinding tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[d365fin](includes/cds_long_md.md)] wordt dit account één keer gebruikt om enkele vereiste componenten te installeren en configureren.</span><span class="sxs-lookup"><span data-stu-id="c6755-107">When you set up the connection between [!INCLUDE[d365fin](includes/d365fin_md.md)] and [!INCLUDE[d365fin](includes/cds_long_md.md)] we will use this account one time to install and configure some required components.</span></span> <!--Verify this-->

## <a name="setting-up-the-user-account-for-the-integration"></a><span data-ttu-id="c6755-108">Het gebruikersaccount instellen voor de integratie</span><span class="sxs-lookup"><span data-stu-id="c6755-108">Setting Up the User Account for the Integration</span></span>
<span data-ttu-id="c6755-109">U moet een speciaal gebruikersaccount in uw Office 365-abonnement maken dat zowel [!INCLUDE[d365fin](includes/d365fin_md.md)] als [!INCLUDE[d365fin](includes/cds_long_md.md)] kan gebruiken om gegevens te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="c6755-109">You must create a dedicated user account in your Office 365 subscription that both [!INCLUDE[d365fin](includes/d365fin_md.md)] and [!INCLUDE[d365fin](includes/cds_long_md.md)] can use to synchronize data.</span></span> <span data-ttu-id="c6755-110">Dit gebruikersaccount moet zich kunnen aanmelden bij [!INCLUDE[d365fin](includes/cds_long_md.md)], wat betekent dat deze gebruiker een licentie moet hebben voor [!INCLUDE[d365fin](includes/cds_long_md.md)] en dat ten minste één beveiligingsrol in [!INCLUDE[d365fin](includes/cds_long_md.md)] aan het account moet zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="c6755-110">This user account must be able to sign in to [!INCLUDE[d365fin](includes/cds_long_md.md)], which means this user must have a license for [!INCLUDE[d365fin](includes/cds_long_md.md)] and at least one security role assigned to it in [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> <!--not sure that this applies as described [here](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-user-account). For more information about how to create users in [!INCLUDE[d365fin](includes/cds_long_md.md)], see [Manage security, users, and teams](https://go.microsoft.com/fwlink/?LinkID=616518). --> <span data-ttu-id="c6755-111">Nadat de verbinding is ingesteld, wijst [!INCLUDE[d365fin](includes/d365fin_md.md)] aan het gebruikersaccount de beveiligingsrollen toe die het nodig heeft in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c6755-111">After the connection is set up, [!INCLUDE[d365fin](includes/d365fin_md.md)] will assign the user account the security roles that it needs in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

<!--![Assisted setup guide showing place to enter synchronization user credentials](media/sync-user-setup.png "Visualization assisted setup wizard page showing place to enter synchronization user credentials")-->

> [!IMPORTANT]  
> <span data-ttu-id="c6755-112">Gebruik het beheerdersaccount niet voor [!INCLUDE[d365fin](includes/cds_long_md.md)] voor synchronisatie.</span><span class="sxs-lookup"><span data-stu-id="c6755-112">Do not use the administrator account for [!INCLUDE[d365fin](includes/cds_long_md.md)] for synchronization.</span></span> <span data-ttu-id="c6755-113">Als u dat doet wordt de synchronisatie verstoord.</span><span class="sxs-lookup"><span data-stu-id="c6755-113">Doing so will break the synchronization.</span></span>

## <a name="permissions-and-security-roles-for-user-accounts-in-d365fin"></a><span data-ttu-id="c6755-114">Machtigingen en beveiligingsrollen voor gebruikersaccounts in [!INCLUDE[d365fin](includes/cds_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="c6755-114">Permissions and Security Roles for User Accounts in [!INCLUDE[d365fin](includes/cds_long_md.md)]</span></span>
<span data-ttu-id="c6755-115">Wanneer u de CDS-basisintegratieoplossing installeert, worden machtigingen voor het integratiegebruikersaccount geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="c6755-115">When you install the CDS Base Integration Solution, permissions for the integration user account are configured.</span></span> <span data-ttu-id="c6755-116">Als deze machtigingen zijn gewijzigd, moet u deze mogelijk opnieuw instellen.</span><span class="sxs-lookup"><span data-stu-id="c6755-116">If those permissions are changed you might need to reset them.</span></span> <span data-ttu-id="c6755-117">U kunt dat doen door de CDS-basisintegratieoplossing opnieuw te installeren door te kiezen voor **Integratieoplossing opnieuw implementeren** op de pagina **Common Data Service-verbinding instellen**.</span><span class="sxs-lookup"><span data-stu-id="c6755-117">You can do that by reinstalling the CDS Base Integration Solution by choosing **Redeploy Integration Solution** on the **Common Data Service Connection Setup** page.</span></span> <span data-ttu-id="c6755-118">De beveiligingsrol van Business Central CDS-integratie is geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="c6755-118">The Business Central CDS Integration security role is deployed.</span></span>


<!--
The following tables list the minimum permissions for the user accounts in [!INCLUDE[d365fin](includes/cds_long_md.md)].

### Minimum Permissions for the Administrator
The following table displays the minimum permissions on each tab for each security role that is required for the administrator user.

##### Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Model Driven App|Global|||Read|
|Plugin Assembly|Global|Read|Read|Read|
|Plugin Type|Global|Read|Read|Read|
|Relationship|Global|||Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Proessing Step|Global|Read|Read|Read|
|SDK Message Proessing Step Image|Global|Read|Read|Read|
|System From|Global|||Write|

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2020|
|----|----|-----|----|----|
|Business Central Account Statistics|Global|Read|Read|Read|
|Business Central Connection|Global|Create, Read, Write, Delete|Create, Read, Write, Delete|Create, Read, Write, Delete|
|Post Configuration|Global|||Write|

#### Integration User
The following table displays the minimum permissions on each tab for each security role that is required for the integration user.

##### Core Records
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Account|Global|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|Create, Read, Write, Append, Append To, Assign|
|Action Card|Global||Read|Read|
|Connection|Global|Read|Read|Read|
|Contact|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Note|Global|||Create, Read, Write, Delete Append, Assign|
|Opportunity|Global||Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Post|Global|||Create, Read, Append To|
|User Entity UI|User|Create, Read, Write|Create, Read, Write|Create, Read, Write|

##### Sales
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Invoice|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Order|Global|Read, Write, Append To|Read, Write, Append To|Read, Write, Append, Append To, Assign|
|Product|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|Property|Global|Read|Read|Read|
|Property Association|Global|Read|Read|Read|
|Property Option Set Item|Global|Read|Read|Read|
|Quote|Global|Read|Read|Read|

##### Service
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Case|Global|Read|Read|Read|

##### Business Management
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Currency|Global|Create, Read, Write|Create, Read, Write|Create, Read, Write|
|Organization|Global|Read, Write|Read, Write|Read, Write|
|Security Role|Global|||Read|
|User|Global|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|Create, Read, Write, Append, Append To|
|User Settings|Global|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|Create, Read, Write, Delete, Append To|
|Act on Behalf of Another User|Global|Yes|Yes|Yes|

##### Customization
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Field|Global||Read|Read|
|Plug-in Assembly|Global|Read|Read|Read|
|Plug-in Type|Global|Read|Read|Read|
|SDK Message|Global|Read|Read|Read|
|SDK Message Processing Step|Global|Read|Read|Read|
|Web Resource|Global|Read|Read|Read|

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

### Product Availability User
You can allow sales people to view inventory levels for the items they sell by granting them the permissions described in the following table.

##### Custom Entities
|Security Role|Access Level|Dynamics NAV 2018 and Earlier|Business Central <br> October 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central Account Statistics|Global|Create, Read, Write, Append To|Create, Read, Write, Append To|Create, Read, Write, Append To|
|Dynamics 365 Business Central Connection|Global|Read|Read|Read|

-->

## <a name="see-also"></a><span data-ttu-id="c6755-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c6755-119">See Also</span></span>  
[<span data-ttu-id="c6755-120">Integreren met Common Data Service</span><span class="sxs-lookup"><span data-stu-id="c6755-120">Integrating with Common Data Service</span></span>](admin-common-data-service.md)  
[<span data-ttu-id="c6755-121">Integreren met Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="c6755-121">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
