---
title: Invoicing en Business Central gebruiken | Microsoft Docs
description: Oplossing om Microsoft Invoicing te kunnen openen wanneer u zich hebt aangemeld voor Dynamics 365 Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/22/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: ddd86615679e6231418b479a440b7555a3e1c50f
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a><span data-ttu-id="909ed-103">Dezelfde Office 365-account gebruiken in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] en Microsoft Invoicing</span><span class="sxs-lookup"><span data-stu-id="909ed-103">Using the same Office 365 Account in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] and Microsoft Invoicing</span></span>
<span data-ttu-id="909ed-104">Wanneer u zich aanmeldt voor de proefversie van [!INCLUDE[d365fin](includes/d365fin_md.md)], kunt u kiezen voor de evaluatiefase van 30 dagen, het abonnement laten ingaan of stoppen met het gebruiken van [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="909ed-104">When you sign up for a trial with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can move to a 30-day evaluation phase, you can start a subscription, or you can stop using [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="909ed-105">In alle gevallen kan er bij het aanmelden bij de Office-portal een tegel met de naam **Business center** worden weergegeven. Klik hierop.</span><span class="sxs-lookup"><span data-stu-id="909ed-105">In all cases, if you log into the Office Portal, you might see a tile called **Business center** and click it.</span></span> <span data-ttu-id="909ed-106">Deze tegel maakt deel uit van het Office 365 Business Premium-abonnement, dus niet iedereen krijgt deze tegel te zien in de Office-portal.</span><span class="sxs-lookup"><span data-stu-id="909ed-106">This is part of the Office 365 Business Premium subscription, so not everyone will see that tile in the Office Portal.</span></span>  

<span data-ttu-id="909ed-107">Als u het Business center opent, wordt er een gedeelte met de naam **Invoicing** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="909ed-107">If you do access the Business center, you will see a section called **Invoicing**.</span></span> <span data-ttu-id="909ed-108">Als u dat gedeelte opent, wordt het bericht weergegeven dat u geen toegang tot Microsoft Invoicing hebt omdat uw account wordt gebruikt in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="909ed-108">If you access that section, you will see a message that you cannot access Microsoft Invoicing because your account is used in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="909ed-109">Er wordt een vergelijkbaar bericht weergegeven als u de mobiele app voor Invoicing installeert.</span><span class="sxs-lookup"><span data-stu-id="909ed-109">You see a similar message if you install the mobile app for Invoicing.</span></span>  

## <a name="workaround"></a><span data-ttu-id="909ed-110">Oplossing</span><span class="sxs-lookup"><span data-stu-id="909ed-110">Workaround</span></span>
<span data-ttu-id="909ed-111">Invoicing en [!INCLUDE[d365fin](includes/d365fin_md.md)] delen een platform.</span><span class="sxs-lookup"><span data-stu-id="909ed-111">Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)] have a shared platform.</span></span> <span data-ttu-id="909ed-112">Dit betekent dat u als een bestaande gebruiker van [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt herkend wanneer u op Invoicing klikt in het Business center.</span><span class="sxs-lookup"><span data-stu-id="909ed-112">That means that you are recognized as an existing user of [!INCLUDE[d365fin](includes/d365fin_md.md)] when you click Invoicing in the Business center.</span></span> <span data-ttu-id="909ed-113">De reden hiervoor is dat Invoicing niet hetzelfde bedrijf kan gebruiken als [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="909ed-113">The reason is that Invoicing cannot use the same company as [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="909ed-114">U moet u daarom aanmelden bij [!INCLUDE[d365fin](includes/d365fin_md.md)], de naam van uw bestaande bedrijf wijzigen en vervolgens een nieuw bedrijf maken om in Invoicing te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="909ed-114">So you will have to log into [!INCLUDE[d365fin](includes/d365fin_md.md)] and rename your existing company, and then create a new company that you can then use in Invoicing.</span></span> <span data-ttu-id="909ed-115">Er worden geen gegevens verplaatst of overschreven tijdens deze oplossingsprocedure.</span><span class="sxs-lookup"><span data-stu-id="909ed-115">No data is moved or overwritten during this workaround.</span></span>

### <a name="to-rename-your-company"></a><span data-ttu-id="909ed-116">De naam van uw bedrijf wijzigen</span><span class="sxs-lookup"><span data-stu-id="909ed-116">To rename your company</span></span>
1.  <span data-ttu-id="909ed-117">Meld u aan bij uw [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="909ed-117">Sign in to your [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
2.  <span data-ttu-id="909ed-118">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bedrijven** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="909ed-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Companies**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="909ed-119">Kies in het venster **Bedrijven** de knop **Lijst bewerken**.</span><span class="sxs-lookup"><span data-stu-id="909ed-119">In the **Companies** window, choose the **Edit List** button.</span></span>  
4.  <span data-ttu-id="909ed-120">Wijzig de naam van het item *Mijn bedrijf*.</span><span class="sxs-lookup"><span data-stu-id="909ed-120">Change the name of the *My Company* entry to something else.</span></span>  

    <span data-ttu-id="909ed-121">Wacht een aantal minuten.</span><span class="sxs-lookup"><span data-stu-id="909ed-121">Wait a number of minutes.</span></span> <span data-ttu-id="909ed-122">Er wordt een aantal wijzigingen doorgevoerd in de onderliggende database, wat enige tijd kost.</span><span class="sxs-lookup"><span data-stu-id="909ed-122">We’ll be making a number of changes in the underlying database, and that takes a while.</span></span>
5.  <span data-ttu-id="909ed-123">Wanneer het systeem klaar is, kiest u de knop **Nieuw bedrijf maken**.</span><span class="sxs-lookup"><span data-stu-id="909ed-123">When the system is ready again, choose the **Create New Company** button.</span></span>  
6.  <span data-ttu-id="909ed-124">Geef in het dialoogvenster dat verschijnt de naam op als *Mijn bedrijf* en kies de optie **Productie - Alleen instellingsgegevens**.</span><span class="sxs-lookup"><span data-stu-id="909ed-124">In the dialog that appears, specify the name as *My Company*, and choose the **Production – Setup Data Only** option.</span></span>  

<span data-ttu-id="909ed-125">Dit kost opnieuw een aantal minuten.</span><span class="sxs-lookup"><span data-stu-id="909ed-125">This again takes a number of minutes.</span></span> <span data-ttu-id="909ed-126">Wanneer het proces is voltooid, kunt u Invoicing openen als onderdeel van uw Office 365 Business Premium-ervaring.</span><span class="sxs-lookup"><span data-stu-id="909ed-126">When the process completes, you will be able to access Invoicing as part of your Office 365 Business Premium experience.</span></span>  

### <a name="what-about-my-data"></a><span data-ttu-id="909ed-127">Hoe zit het met mijn gegevens?</span><span class="sxs-lookup"><span data-stu-id="909ed-127">What about my data?</span></span>
<span data-ttu-id="909ed-128">Wanneer u de naam van het oorspronkelijke Mijn bedrijf wijzigt, wordt de naam gewijzigd van de databasetabellen met de bestaande [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens, maar de gegevens zelf blijven ongewijzigd.</span><span class="sxs-lookup"><span data-stu-id="909ed-128">When you rename the original My Company, the database tables that store your existing [!INCLUDE[d365fin](includes/d365fin_md.md)] data are renamed, but the data itself is not touched.</span></span>  

<span data-ttu-id="909ed-129">Als u zowel Invoicing als [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruikt, worden de gegevens in twee verschillende containers (de twee bedrijven) opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="909ed-129">If you use both Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)], the data is stored in two different containers (the two companies).</span></span> <span data-ttu-id="909ed-130">Er wordt niets gedeeld, dus u moet de klanten en artikelen in beide bedrijven beheren.</span><span class="sxs-lookup"><span data-stu-id="909ed-130">Nothing is shared, so you'll have to manage customers and items in both companies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="909ed-131">Zie ook</span><span class="sxs-lookup"><span data-stu-id="909ed-131">See Also</span></span>
[<span data-ttu-id="909ed-132">Veelgestelde vragen</span><span class="sxs-lookup"><span data-stu-id="909ed-132">Frequently Asked Questions</span></span>](across-faq.md)  
[<span data-ttu-id="909ed-133">Beheer</span><span class="sxs-lookup"><span data-stu-id="909ed-133">Administration</span></span>](admin-setup-and-administration.md)  

