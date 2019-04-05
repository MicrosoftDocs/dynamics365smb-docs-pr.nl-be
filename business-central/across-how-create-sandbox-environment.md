---
title: Een sandboxomgeving maken | Microsoft Docs
description: Maak een omgeving waarin u kunt ontdekken, leren, demonstreren, ontwikkelen en testen.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 02/15/2019
ms.author: solsen
ms.openlocfilehash: 91db02673c1e408927d9863af9ec6751bc33e480
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816592"
---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="creating-a-sandbox-environment"></a><span data-ttu-id="76058-103">Een sandboxomgeving maken</span><span class="sxs-lookup"><span data-stu-id="76058-103">Creating a Sandbox Environment</span></span>
<span data-ttu-id="76058-104">Een sandboxomgeving (voorbeeld) is een niet-productie-exemplaar van [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="76058-104">A sandbox environment (Preview) is a non-production instance of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="76058-105">Geïsoleerd van de productieomgeving is een sandboxomgeving de plaats om de service te ontdekken, te leren kennen, te demonstreren, te ontwikkelen en te testen, zonder het risico te lopen dat de gegevens en instellingen van uw productieomgeving worden beïnvloed.</span><span class="sxs-lookup"><span data-stu-id="76058-105">Isolated from production, a sandbox environment is the place to safely explore, learn, demo, develop, and test the service without the risk of affecting the data and settings of your production environment.</span></span>

## <a name="to-create-a-sandbox-environment"></a><span data-ttu-id="76058-106">Een sandboxomgeving maken</span><span class="sxs-lookup"><span data-stu-id="76058-106">To create a sandbox environment</span></span>
<span data-ttu-id="76058-107">U moet een abonnement op [!INCLUDE[d365fin](includes/d365fin_md.md)] hebben om een sandboxomgeving te maken.</span><span class="sxs-lookup"><span data-stu-id="76058-107">You must have a subscription to [!INCLUDE[d365fin](includes/d365fin_md.md)] to be able to create a sandbox environment.</span></span> <span data-ttu-id="76058-108">Per abonnement kan er slechts één sandboxomgeving bestaan.</span><span class="sxs-lookup"><span data-stu-id="76058-108">There can only be one sandbox environment per subscription.</span></span>

1. <span data-ttu-id="76058-109">Meld aan bij uw productie-exemplaar van de [!INCLUDE[d365fin](includes/d365fin_md.md)]-service.</span><span class="sxs-lookup"><span data-stu-id="76058-109">Sign in to your production instance of the [!INCLUDE[d365fin](includes/d365fin_md.md)] service.</span></span>
2. <span data-ttu-id="76058-110">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Sandboxomgeving** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="76058-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sandbox Environment**, and then choose the related link.</span></span>
<!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. <span data-ttu-id="76058-111">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="76058-111">Select **Create**.</span></span>  
  <span data-ttu-id="76058-112">Er wordt een ander tabblad in uw browser geopend waarin u de instelling van uw sandboxomgeving kunt voltooien.</span><span class="sxs-lookup"><span data-stu-id="76058-112">Another tab in your browser will open for finishing the setup of your sandbox environment.</span></span>
> [!NOTE]  
>  <span data-ttu-id="76058-113">Als u pop-upblokkering hebt ingeschakeld in uw browser, wijzigt u deze om URL's van het adres \*.businesscentral.dynamics.com toe te staan.</span><span class="sxs-lookup"><span data-stu-id="76058-113">If you have pop-up blocker enabled in your browser, change it to allow URLs from the \*.businesscentral.dynamics.com address.</span></span>   

4. <span data-ttu-id="76058-114">Wanneer de sandboxomgeving gereed is, wordt u omgeleid naar de welkomstwizard van de sandboxomgeving.</span><span class="sxs-lookup"><span data-stu-id="76058-114">When the sandbox environment is ready, you will be redirected to sandbox environment's Welcome wizard.</span></span>
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

5. <span data-ttu-id="76058-115">Kies **Meer informatie** voor scenario's die u in een sandboxomgeving kunt uitproberen.</span><span class="sxs-lookup"><span data-stu-id="76058-115">Choose **Learn more** to read about scenarios that you can try in a sandbox environment.</span></span> <span data-ttu-id="76058-116">U kunt ook **Sluiten** kiezen om door te gaan naar het rolcentrum van uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-sandboxexemplaar.</span><span class="sxs-lookup"><span data-stu-id="76058-116">Or, choose **Close** to continue to the Role Center of your [!INCLUDE[d365fin](includes/d365fin_md.md)] sandbox instance.</span></span>
6. <span data-ttu-id="76058-117">Boven in het rolcentrum verschijnt een bericht om u te laten weten dat dit een sandboxomgeving is.</span><span class="sxs-lookup"><span data-stu-id="76058-117">At the top of the Role Center, a notification appears to inform you that this is a sandbox environment.</span></span> <span data-ttu-id="76058-118">Ook in de titelbalk van de client wordt de soort omgeving weergegeven.</span><span class="sxs-lookup"><span data-stu-id="76058-118">You can also see the type of the environment in the title bar of the client.</span></span>
<!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) --> 
<span data-ttu-id="76058-119">In de sandboxomgeving wordt een nieuwe tenant gemaakt.</span><span class="sxs-lookup"><span data-stu-id="76058-119">In the sandbox environment, a new tenant has been created.</span></span> <span data-ttu-id="76058-120">Deze tenant wordt geladen met standaarddemonstratiegegevens voor het CRONUS-bedrijf.</span><span class="sxs-lookup"><span data-stu-id="76058-120">This tenant is loaded with default demonstration data for the CRONUS company.</span></span> <span data-ttu-id="76058-121">Tijdens het maken van de sandbox worden er geen gegevens gekopieerd of anderszins overgebracht vanuit de productieomgeving.</span><span class="sxs-lookup"><span data-stu-id="76058-121">No data is copied or otherwise transferred from the production environment during the sandbox creation.</span></span>

7. <span data-ttu-id="76058-122">U kunt op elk moment terugkeren naar de pagina **Sandboxomgeving** en de sandboxomgeving herstellen.</span><span class="sxs-lookup"><span data-stu-id="76058-122">At any time, you can return to the **Sandbox Environment** page, and reset the sandbox environment.</span></span>
> [!NOTE]  
>  <span data-ttu-id="76058-123">Wanneer u de sandboxomgeving herstelt, wordt deze volledig verwijderd en vervolgens opnieuw gemaakt met de standaarddemonstratiegegevens.</span><span class="sxs-lookup"><span data-stu-id="76058-123">Resetting the sandbox environment will remove it completely, and then create it again with the default demonstration data.</span></span>  

8. <span data-ttu-id="76058-124">Als u wilt schakelen tussen uw productie- en sandboxomgeving, kunt u het startprogramma voor apps van Business Central gebruiken.</span><span class="sxs-lookup"><span data-stu-id="76058-124">To switch between your production and sandbox environments, you can use the Business Central app launcher.</span></span>
<!-- ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

9. <span data-ttu-id="76058-125">Een beheerder of een andere gebruiker kan de toegang tot de sandboxomgeving voor sommige gebruikers beperken of zelfs blokkeren.</span><span class="sxs-lookup"><span data-stu-id="76058-125">It is possible for an administrator or another user to limit or even block access for some users to the sandbox environment.</span></span> <span data-ttu-id="76058-126">Dit kunt u doen met de standaardbeveiligingsfuncties van het product, zoals de kaart Gebruiker, gebruikersgroepen en machtigingensets.</span><span class="sxs-lookup"><span data-stu-id="76058-126">This can be done by using the standard security features of the product, such as the User card, User Groups, and Permission Sets.</span></span>

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a><span data-ttu-id="76058-127">Geavanceerde functionaliteit in de sandboxomgeving</span><span class="sxs-lookup"><span data-stu-id="76058-127">Advanced functionality in the sandbox environment</span></span>
### <a name="designer"></a><span data-ttu-id="76058-128">Ontwerper</span><span class="sxs-lookup"><span data-stu-id="76058-128">Designer</span></span>
<span data-ttu-id="76058-129">In een sandboxomgeving is de functie **Ontwerper** ingeschakeld. U kunt deze functie activeren door het pictogram ![Ontwerper](./media/across-sandbox/sandbox-inclient-design-icon.png) te selecteren op een pagina.</span><span class="sxs-lookup"><span data-stu-id="76058-129">In a sandbox environment, you will find the **Designer** enabled, which you can activate by selecting the design icon ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) on a page.</span></span>

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="enable-the-advanced-user-experience"></a><span data-ttu-id="76058-130">De geavanceerde gebruikerservaring inschakelen</span><span class="sxs-lookup"><span data-stu-id="76058-130">Enable the advanced user experience</span></span>
<span data-ttu-id="76058-131">Het is mogelijk om de geavanceerde (volledige) functionaliteit van [!INCLUDE[d365fin](includes/d365fin_md.md)] in een sandboxtenant in te schakelen door het veld **Ervaring** op de pagina **Bedrijfsgegevens** in te stellen.</span><span class="sxs-lookup"><span data-stu-id="76058-131">It is possible to enable and try the advanced (full) functionality of [!INCLUDE[d365fin](includes/d365fin_md.md)] in a sandbox tenant by setting the **Experience** field on the **Company Information** page.</span></span>

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

<span data-ttu-id="76058-132">Als u de geavanceerde functionaliteit in een sandboxtenant hebt ingeschakeld, krijgt u toegang tot alle standaardprofielen en rolcentra.</span><span class="sxs-lookup"><span data-stu-id="76058-132">After you’ve enabled the advanced functionality in a sandbox tenant, you get access to all the standard Profiles and Role Centers.</span></span> <span data-ttu-id="76058-133">U kunt ook een evaluatiebedrijf maken dat volledig is ingesteld, inclusief demonstratiegegevens en toegang tot de geavanceerde gebieden van het product.</span><span class="sxs-lookup"><span data-stu-id="76058-133">You can also create an evaluation company that is fully set up, including demonstration data and access to the advanced areas of the product.</span></span>

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->


## <a name="see-also"></a><span data-ttu-id="76058-134">Zie ook</span><span class="sxs-lookup"><span data-stu-id="76058-134">See Also</span></span>
<span data-ttu-id="76058-135">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="76058-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
