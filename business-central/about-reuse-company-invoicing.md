---
title: Invoicing en Business Central gebruiken | Microsoft Docs
description: Oplossing om Microsoft Invoicing te kunnen openen wanneer u zich hebt aangemeld voor Dynamics 365 Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Invoicing, Office 365
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 0173d64e140cfea91bf7f08d821c2d30cf0eb7b3
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241496"
---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a><span data-ttu-id="cf520-103">Dezelfde Office 365-account gebruiken in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] en Microsoft Invoicing</span><span class="sxs-lookup"><span data-stu-id="cf520-103">Using the same Office 365 Account in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] and Microsoft Invoicing</span></span>
<span data-ttu-id="cf520-104">Wanneer u zich aanmeldt voor de proefversie van [!INCLUDE[d365fin](includes/d365fin_md.md)], kunt u kiezen voor de evaluatiefase van 30 dagen, het abonnement laten ingaan of stoppen met het gebruiken van [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="cf520-104">When you sign up for a trial with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can move to a 30-day evaluation phase, you can start a subscription, or you can stop using [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="cf520-105">In alle gevallen kan er bij het aanmelden bij de Office-portal een tegel met de naam **Microsoft Invoicing** worden weergegeven. Klik hierop.</span><span class="sxs-lookup"><span data-stu-id="cf520-105">In all cases, if you sign in to the Office Portal, you might see a tile called **Microsoft Invoicing** and click it.</span></span> <span data-ttu-id="cf520-106">Deze tegel maakt deel uit van het Office 365 Business Premium-abonnement, dus niet iedereen krijgt deze tegel te zien in de Office-portal.</span><span class="sxs-lookup"><span data-stu-id="cf520-106">This is part of the Office 365 Business Premium subscription, so not everyone will see that tile in the Office Portal.</span></span>  

<span data-ttu-id="cf520-107">Als u Microsoft Invoicing opent, wordt het bericht weergegeven dat u geen toegang tot Microsoft Invoicing hebt omdat uw account wordt gebruikt in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="cf520-107">If you access Microsoft Invoicing, you will see a message that you cannot access Microsoft Invoicing because your account is used in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="cf520-108">Er wordt een vergelijkbaar bericht weergegeven als u de mobiele app voor Invoicing installeert.</span><span class="sxs-lookup"><span data-stu-id="cf520-108">You see a similar message if you install the mobile app for Invoicing.</span></span>  

## <a name="workaround"></a><span data-ttu-id="cf520-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="cf520-109">Workaround</span></span>
<span data-ttu-id="cf520-110">Invoicing en [!INCLUDE[d365fin](includes/d365fin_md.md)] delen een platform.</span><span class="sxs-lookup"><span data-stu-id="cf520-110">Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)] have a shared platform.</span></span> <span data-ttu-id="cf520-111">Dit betekent dat u als een bestaande gebruiker van [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt herkend wanneer u op Invoicing klikt in de Office-portal.</span><span class="sxs-lookup"><span data-stu-id="cf520-111">That means that you are recognized as an existing user of [!INCLUDE[d365fin](includes/d365fin_md.md)] when you click Invoicing in the Office Portal.</span></span> <span data-ttu-id="cf520-112">De reden hiervoor is dat Invoicing niet hetzelfde bedrijf kan gebruiken als [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="cf520-112">The reason is that Invoicing cannot use the same company as [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="cf520-113">U moet u daarom aanmelden bij [!INCLUDE[d365fin](includes/d365fin_md.md)], de naam van uw bestaande bedrijf wijzigen en vervolgens een nieuw bedrijf maken om in Invoicing te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="cf520-113">So you will have to sign in to [!INCLUDE[d365fin](includes/d365fin_md.md)] and rename your existing company, and then create a new company that you can then use in Invoicing.</span></span> <span data-ttu-id="cf520-114">Er worden geen gegevens verplaatst of overschreven tijdens deze oplossingsprocedure.</span><span class="sxs-lookup"><span data-stu-id="cf520-114">No data is moved or overwritten during this workaround.</span></span>

### <a name="to-rename-your-company"></a><span data-ttu-id="cf520-115">De naam van uw bedrijf wijzigen</span><span class="sxs-lookup"><span data-stu-id="cf520-115">To rename your company</span></span>
1. <span data-ttu-id="cf520-116">Meld u aan bij [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="cf520-116">Sign in to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
2. <span data-ttu-id="cf520-117">Kies in de rechterbovenhoek het pictogram **Instellingen** ![Instellingen](media/ui-experience/settings_icon_small.png "pictogram Instellingen voor rolcentrum") en kies vervolgens **Mijn instellingen**.</span><span class="sxs-lookup"><span data-stu-id="cf520-117">In the top right corner, choose the **Settings** icon ![Settings](media/ui-experience/settings_icon_small.png "Settings icon for role center"), and then choose **My Settings**.</span></span>
3. <span data-ttu-id="cf520-118">Kies in het veld **Bedrijf** een ander bedrijf.</span><span class="sxs-lookup"><span data-stu-id="cf520-118">In the **Company** field, choose a different company.</span></span>
4. <span data-ttu-id="cf520-119">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bedrijven** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="cf520-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.</span></span>  
5. <span data-ttu-id="cf520-120">Kies op de pagina **Bedrijven** **Lijst bewerken**.</span><span class="sxs-lookup"><span data-stu-id="cf520-120">On the **Companies** page, choose **Edit List**.</span></span>  
6. <span data-ttu-id="cf520-121">Wijzig de naam van het item *Mijn bedrijf*.</span><span class="sxs-lookup"><span data-stu-id="cf520-121">Change the name of the *My Company* entry to something else.</span></span>  

    <span data-ttu-id="cf520-122">Wacht een aantal minuten.</span><span class="sxs-lookup"><span data-stu-id="cf520-122">Wait a number of minutes.</span></span> <span data-ttu-id="cf520-123">Er wordt een aantal wijzigingen doorgevoerd in de onderliggende database, wat enige tijd kost.</span><span class="sxs-lookup"><span data-stu-id="cf520-123">We’ll be making a number of changes in the underlying database, and that takes a while.</span></span>
7.  <span data-ttu-id="cf520-124">Wanneer het systeem klaar is, kiest u de knop **Nieuw bedrijf maken**.</span><span class="sxs-lookup"><span data-stu-id="cf520-124">When the system is ready again, choose the **Create New Company** button.</span></span>  
8.  <span data-ttu-id="cf520-125">Geef in het dialoogvenster dat verschijnt de naam op als *Mijn bedrijf* en kies de optie **Productie - Alleen instellingsgegevens**.</span><span class="sxs-lookup"><span data-stu-id="cf520-125">In the dialog that appears, specify the name as *My Company*, and choose the **Production – Setup Data Only** option.</span></span>  

<span data-ttu-id="cf520-126">Dit kost opnieuw een aantal minuten.</span><span class="sxs-lookup"><span data-stu-id="cf520-126">This again takes a number of minutes.</span></span> <span data-ttu-id="cf520-127">Wanneer het proces is voltooid, kunt u Invoicing openen als onderdeel van uw Office 365 Business Premium-ervaring.</span><span class="sxs-lookup"><span data-stu-id="cf520-127">When the process completes, you will be able to access Invoicing as part of your Office 365 Business Premium experience.</span></span>  

### <a name="what-about-my-data"></a><span data-ttu-id="cf520-128">Hoe zit het met mijn gegevens?</span><span class="sxs-lookup"><span data-stu-id="cf520-128">What about my data?</span></span>
<span data-ttu-id="cf520-129">Wanneer u de naam van het oorspronkelijke Mijn bedrijf wijzigt, wordt de naam gewijzigd van de databasetabellen met de bestaande [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens, maar de gegevens zelf blijven ongewijzigd.</span><span class="sxs-lookup"><span data-stu-id="cf520-129">When you rename the original My Company, the database tables that store your existing [!INCLUDE[d365fin](includes/d365fin_md.md)] data are renamed, but the data itself is not touched.</span></span>  

<span data-ttu-id="cf520-130">Als u zowel Invoicing als [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruikt, worden de gegevens in twee verschillende containers (de twee bedrijven) opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="cf520-130">If you use both Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)], the data is stored in two different containers (the two companies).</span></span> <span data-ttu-id="cf520-131">Er wordt niets gedeeld, dus u moet de klanten en artikelen in beide bedrijven beheren.</span><span class="sxs-lookup"><span data-stu-id="cf520-131">Nothing is shared, so you'll have to manage customers and items in both companies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cf520-132">Zie ook</span><span class="sxs-lookup"><span data-stu-id="cf520-132">See Also</span></span>
[<span data-ttu-id="cf520-133">Veelgestelde vragen</span><span class="sxs-lookup"><span data-stu-id="cf520-133">Frequently Asked Questions</span></span>](across-faq.md)  
[<span data-ttu-id="cf520-134">Beheer</span><span class="sxs-lookup"><span data-stu-id="cf520-134">Administration</span></span>](admin-setup-and-administration.md)  
