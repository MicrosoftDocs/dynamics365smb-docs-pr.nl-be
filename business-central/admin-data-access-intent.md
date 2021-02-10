---
title: Databasetoegangsintentie beheren in Business Central | Microsoft Docs
description: Wijzig de databasetoegangsintentie voor rapporten, API-pagina's en query's.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6d79f5b2851df85ea9f19faeeb941eccfd1b397b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752837"
---
# <a name="managing-database-access-intent"></a><span data-ttu-id="e806c-103">Databasetoegangsintentie beheren</span><span class="sxs-lookup"><span data-stu-id="e806c-103">Managing Database Access Intent</span></span> 

<span data-ttu-id="e806c-104">Als supergebruiker of beheerder kunt u de databasetoegangsintentie voor rapporten, pagina's van het type API en query's wijzigen om de prestaties van de service te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="e806c-104">As a super user or administrator, you can change the database access intent on reports, pages of the type API, and queries to improve performance of the service.</span></span>

## <a name="overview"></a><span data-ttu-id="e806c-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="e806c-105">Overview</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="e806c-106">kan worden ingesteld om alleen-lezen replica's van de primaire (lezen-schrijven) database te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e806c-106">can be set up to use read-only replicas of the primary (read-write) database.</span></span> <span data-ttu-id="e806c-107">Het gebruik van de databasereplica vermindert de belasting van de primaire database.</span><span class="sxs-lookup"><span data-stu-id="e806c-107">Using the database replica reduces the load on the primary database.</span></span> <span data-ttu-id="e806c-108">In sommige gevallen verbetert het ook de prestaties bij het bekijken van gegevens in de client.</span><span class="sxs-lookup"><span data-stu-id="e806c-108">In some cases, it will also improve the performance when viewing data in the client.</span></span> <span data-ttu-id="e806c-109">Replica's zijn gunstig voor objecten, zoals rapporten, query's en API-pagina's, die alleen worden gebruikt voor het bekijken van gegevens en niet voor het wijzigen van gegevens.</span><span class="sxs-lookup"><span data-stu-id="e806c-109">Replicas are beneficial for objects, like reports, queries, and API pages, that are used for viewing data only, not modifying data.</span></span>

<span data-ttu-id="e806c-110">Wanneer objecten worden uitgevoerd, bepaalt de databasetoegangsintentie of een alleen-lezen replica, indien beschikbaar, of de primaire database moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e806c-110">When objects run, the database access intent determines whether to use a read-only replica, if one is available, or the primary database.</span></span> <span data-ttu-id="e806c-111">Rapporten, API-pagina's en query's worden ontwikkeld met een vooraf gedefinieerde databasetoegangsintentie (zie [eigenschap DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span><span class="sxs-lookup"><span data-stu-id="e806c-111">Reports, API pages, and queries are developed with a predefined database access intent (see [DatabaseAccessIntent property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span></span>

<span data-ttu-id="e806c-112">Met de pagina **Lijst met intenties voor databasetoegang** kunt u de vooraf gedefinieerde intentie voor databasetoegang voor objecten overschrijven wanneer ze worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="e806c-112">The **Database Access Intent List** page lets you override the predefined database access intent for objects when they're run.</span></span>

<span data-ttu-id="e806c-113">In databasetermen staat deze functie algemeen bekend als *read scale-out*. Voor meer informatie over read scale-out en datatoegangsintentie in [!INCLUDE[prod_short](includes/prod_short.md)] raadpleegt u [Read scale-out gebruiken voor betere prestaties](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) in de [!INCLUDE[prod_short](includes/prod_short.md)] Help voor ontwikkelaars en beheer.</span><span class="sxs-lookup"><span data-stu-id="e806c-113">In database terms, this feature is commonly known as *read scale-out*. For more information about read-scale out and data access intent in [!INCLUDE[prod_short](includes/prod_short.md)], see [Utilizing Read Scale-Out for Better Performance](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) in the [!INCLUDE[prod_short](includes/prod_short.md)] Developer and Administration help.</span></span>

## <a name="to-change-the-database-access-intent"></a><span data-ttu-id="e806c-114">De intentie van de databasetoegang wijzigen</span><span class="sxs-lookup"><span data-stu-id="e806c-114">To change the database access intent</span></span>

1. <span data-ttu-id="e806c-115">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Lijst met intenties voor databasetoegang** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="e806c-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Database Access Intent List**, and then choose the related link.</span></span>

    <span data-ttu-id="e806c-116">De pagina bevat alle rapporten, pagina's en query's.</span><span class="sxs-lookup"><span data-stu-id="e806c-116">The page lists all reports, pages, and queries.</span></span> <span data-ttu-id="e806c-117">De kolom **Toegangsintentie** bevat een van de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="e806c-117">The **Access Intent** column includes one of the following values:</span></span>

    |<span data-ttu-id="e806c-118">**Instelling**</span><span class="sxs-lookup"><span data-stu-id="e806c-118">**Setting**</span></span>|<span data-ttu-id="e806c-119">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="e806c-119">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="e806c-120">**Standaard**</span><span class="sxs-lookup"><span data-stu-id="e806c-120">**Default**</span></span>|<span data-ttu-id="e806c-121">Geeft aan dat het object de vooraf gedefinieerde intentie voor databasetoegang gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e806c-121">Indicates that the object uses the predefined database access intent.</span></span>|
    |<span data-ttu-id="e806c-122">**Schrijven toestaan**</span><span class="sxs-lookup"><span data-stu-id="e806c-122">**Allow Write**</span></span>|<span data-ttu-id="e806c-123">Stelt het object in om de primaire database te gebruiken, zodat de gebruiker gegevens kan wijzigen.</span><span class="sxs-lookup"><span data-stu-id="e806c-123">Sets the object to use the primary database, allowing the user to modify data.</span></span>|
    |<span data-ttu-id="e806c-124">**Alleen-lezen**</span><span class="sxs-lookup"><span data-stu-id="e806c-124">**Read Only**</span></span>|<span data-ttu-id="e806c-125">Stelt het object in om de databasereplica te gebruiken, wat betekent dat de gebruiker alleen gegevens kan bekijken en geen gegevens kan wijzigen.</span><span class="sxs-lookup"><span data-stu-id="e806c-125">Sets the object to use the database replica, which means that the user can only view data, not change data.</span></span>|

2. <span data-ttu-id="e806c-126">Kies de actie **Lijst bewerken**.</span><span class="sxs-lookup"><span data-stu-id="e806c-126">Choose the **Edit List** action.</span></span>

3. <span data-ttu-id="e806c-127">Wijzig op de pagina **Bewerken - Lijst met intenties voor databasetoegang** het veld **Toegangsintentie** voor de objecten.</span><span class="sxs-lookup"><span data-stu-id="e806c-127">On the **Edit - Database Access Intent List** page, change the **Access Intent** field for the objects.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e806c-128">Als een object dat kan worden bewerkt, zoals de klantenkaart, is ingesteld op **Alleen-lezen**, zal de primaire database nog steeds worden gebruikt, ongeacht de toegangsintentie, zodat gebruikers normaal wijzigingen kunnen aanbrengen.</span><span class="sxs-lookup"><span data-stu-id="e806c-128">If an object that is editable, like the Customer Card, is set to **Read Only**, the primary database will still be used, regardless of the access intent, allowing users to make changes as normal.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="e806c-129">Zie Gerelateerde training op [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="e806c-129">See Related Training at [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="e806c-130">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e806c-130">See Also</span></span>
[<span data-ttu-id="e806c-131">Bedrijfsfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="e806c-131">Business Functionality</span></span>](across-business-functionality.md)  
[<span data-ttu-id="e806c-132">Algemene bedrijfsfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="e806c-132">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="e806c-133">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e806c-133">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="e806c-134">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="e806c-134">Getting Started</span></span>](product-get-started.md)    

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
