---
title: Een sandboxomgeving maken
description: Maak een omgeving voor verkennen, leren, demonstreren, ontwikkelen en testen vanuit Business Central.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 06/08/2021
ms.author: solsen
ms.openlocfilehash: a76ae33815b8e9368f45b72fd8703bfc47cbd079
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215640"
---
# <a name="creating-a-sandbox-environment-in-prod_short"></a><span data-ttu-id="1d0fa-103">Een sandboxomgeving maken in [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="1d0fa-103">Creating a Sandbox Environment in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

<span data-ttu-id="1d0fa-104">Met [!INCLUDE[prod_short](includes/prod_short.md)] kunt u eenvoudig een veilige omgeving creëren waar u kunt testen, trainen of problemen oplossen zonder de werkprocessen of bedrijfsgegevens van uw bedrijf te verstoren.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-104">With [!INCLUDE[prod_short](includes/prod_short.md)], you can easily create a safe environment where you can test, train, or troubleshoot without disturbing your company's work processes or business data.</span></span> <span data-ttu-id="1d0fa-105">Een dergelijke niet-productieomgeving wordt een *sandbox* genoemd.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-105">Such a non-production environment is called a *sandbox*.</span></span> <span data-ttu-id="1d0fa-106">Geïsoleerd van de productieomgeving is een sandboxomgeving de plaats om de service te ontdekken, te leren kennen, te demonstreren, te ontwikkelen en te testen, zonder het risico te lopen dat de gegevens en instellingen van uw productieomgeving worden beïnvloed.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-106">Isolated from production, a sandbox environment is the place to safely explore, learn, demo, develop, and test the service without the risk of affecting the data and settings of your production environment.</span></span>  

<span data-ttu-id="1d0fa-107">Uw beheerder beheert sandboxomgevingen in het [beheercentrum](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), maar als u snel iets wilt testen, kunt u een sandboxomgeving maken vanuit [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="1d0fa-107">Your administrator manages sandbox environments in the [administration center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), but if you want to quickly test something, you can create a sandbox environment from inside [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="1d0fa-108">Als u klaar bent, kunt u de sandbox verwijderen met behulp van het beheercentrum.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-108">Once you're done, you can remove the sandbox, using the administration center.</span></span>  

> [!NOTE]
> <span data-ttu-id="1d0fa-109">Technisch gezien zijn sandbox-omgevingen heel anders dan productieomgevingen, zelfs als uw beheerder een sandbox maakt die productiegegevens bevat.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-109">Technically, sandbox environments are very different from production environments, even if your administrator creates a sandbox that includes production data.</span></span> <span data-ttu-id="1d0fa-110">U kunt geen sandbox gebruiken voor benchmarking en u kunt bijvoorbeeld geen database-export aanvragen.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-110">You cannot use a sandbox for benchmarking, and you cannot request a database export, for example.</span></span> <span data-ttu-id="1d0fa-111">Als uw beheerder een sandbox voor benchmarking wilt maken, kan hij of zij een speciale omgeving maken in het beheercentrum.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-111">If you want to create a sandbox for benchmarking, your administrator can create a dedicated environment in the administration center.</span></span> <span data-ttu-id="1d0fa-112">Zie voor meer informatie [Productie- en sandbox-omgevingen](/dynamics365/business-central/dev-itpro/administration/environment-types).</span><span class="sxs-lookup"><span data-stu-id="1d0fa-112">For more information, see [Production and Sandbox Environments](/dynamics365/business-central/dev-itpro/administration/environment-types).</span></span>

## <a name="to-create-a-sandbox-environment-in-your-prod_short"></a><span data-ttu-id="1d0fa-113">Een sandboxomgeving maken in uw [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="1d0fa-113">To create a sandbox environment in your [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

1. <span data-ttu-id="1d0fa-114">Meld u aan bij uw productie-exemplaar van [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="1d0fa-114">Sign in to your production instance of [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

2. <span data-ttu-id="1d0fa-115">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Sandboxomgeving** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sandbox Environment**, and then choose the related link.</span></span>
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. <span data-ttu-id="1d0fa-116">Kies de knop **Maken**.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-116">Choose the **Create** button.</span></span>  

    <span data-ttu-id="1d0fa-117">Er wordt een ander tabblad met [!INCLUDE[prod_short](includes/prod_short.md)] geopend, waar u de installatie van uw sandbox-omgeving kunt voltooien.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-117">Another tab with [!INCLUDE[prod_short](includes/prod_short.md)] opens where you can finish the setup of your sandbox environment.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="1d0fa-118">Als u pop-upblokkering hebt ingeschakeld in uw browser, wijzigt u deze om URL's van het adres \*.businesscentral.dynamics.com toe te staan.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-118">If you have pop-up blocker enabled in your browser, change it to allow URLs from the \*.businesscentral.dynamics.com address.</span></span>

<span data-ttu-id="1d0fa-119">Wanneer de sandboxomgeving gereed is, wordt u omgeleid naar de welkomstwizard van de sandboxomgeving.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-119">When the sandbox environment is ready, you will be redirected to sandbox environment's Welcome wizard.</span></span>
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

<span data-ttu-id="1d0fa-120">U kunt de knop **Meer informatie** kiezen om te lezen over ontwikkelaarsscenario's die u in een sandboxomgeving kunt proberen of kies de knop **Sluiten** om door te gaan naar het rolcentrum van uw [!INCLUDE[prod_short](includes/prod_short.md)]-sandboxexemplaar.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-120">You can choose the **Learn more** button to read about developer scenarios that you can try in a sandbox environment or choose the **Close** button to continue to the Role Center of your [!INCLUDE[prod_short](includes/prod_short.md)] sandbox instance.</span></span>

<span data-ttu-id="1d0fa-121">Boven in het rolcentrum verschijnt een bericht om u te laten weten dat dit een sandboxomgeving is.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-121">At the top of the Role Center, a notification appears to inform you that this is a sandbox environment.</span></span> <span data-ttu-id="1d0fa-122">Ook in de titelbalk van de client wordt de soort omgeving weergegeven.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-122">You can also see the type of the environment in the title bar of the client.</span></span>
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> <span data-ttu-id="1d0fa-123">Een sandbox-omgeving die op deze manier is gemaakt, bevat alleen de standaarddemonstratiegegevens voor het CRONUS-bedrijf.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-123">A sandbox environment created in this way only contains the default demonstration data for the CRONUS company.</span></span> <span data-ttu-id="1d0fa-124">Er worden geen gegevens gekopieerd of anderszins overgedragen vanuit de productieomgeving.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-124">No data is copied or otherwise transferred from the production environment.</span></span>
>
> <span data-ttu-id="1d0fa-125">U kunt ook een sandbox-omgeving maken op basis van productiegegevens.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-125">Alternatively, create a sandbox environment based on production data.</span></span> <span data-ttu-id="1d0fa-126">U moet dit doen via het beheercentrum.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-126">You must do this through the administration center.</span></span> <span data-ttu-id="1d0fa-127">Zie voor meer informatie [Omgevingen beheren](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) in de ontwikkelaar- en beheercontent.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-127">For more information, see [Managing Environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) in the developer and administration content.</span></span>  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

<span data-ttu-id="1d0fa-128">Een beheerder kan voor sommige gebruikers de toegang tot de sandboxomgeving beperken of zelfs blokkeren.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-128">An administrator can limit or even block access for some users to the sandbox environment.</span></span> <span data-ttu-id="1d0fa-129">Dit kunt u doen met de standaardbeveiligingsfuncties van het product, zoals de gebruikerskaart, gebruikersgroepen en machtigingensets.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-129">This can be done by using the standard security features of the product, such as the User card, user groups, and permission sets.</span></span> <span data-ttu-id="1d0fa-130">Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-130">For more information, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a><span data-ttu-id="1d0fa-131">Geavanceerde functionaliteit in de sandboxomgeving</span><span class="sxs-lookup"><span data-stu-id="1d0fa-131">Advanced Functionality in the Sandbox Environment</span></span>

<span data-ttu-id="1d0fa-132">De sandboxomgeving is onder andere nuttig omdat deze een aantal handige functies bevat:</span><span class="sxs-lookup"><span data-stu-id="1d0fa-132">The sandbox environment is not least useful because it includes a couple of handy features:</span></span>

* [<span data-ttu-id="1d0fa-133">Geavanceerde gebruikerservaring</span><span class="sxs-lookup"><span data-stu-id="1d0fa-133">Advanced user experience</span></span>](#advanced-user-experience)  
* [<span data-ttu-id="1d0fa-134">Volledige voorbeeldgegevens</span><span class="sxs-lookup"><span data-stu-id="1d0fa-134">Complete sample data</span></span>](#complete-sample-data)  
* [<span data-ttu-id="1d0fa-135">Ontwerper</span><span class="sxs-lookup"><span data-stu-id="1d0fa-135">Designer</span></span>](#designer)  

### <a name="advanced-user-experience"></a><span data-ttu-id="1d0fa-136">Geavanceerde gebruikerservaring</span><span class="sxs-lookup"><span data-stu-id="1d0fa-136">Advanced user experience</span></span>

<span data-ttu-id="1d0fa-137">Het is mogelijk de volledige functionaliteit van de standaardversie van [!INCLUDE[prod_short](includes/prod_short.md)] in een sandboxtenant in te schakelen en uit te proberen door het veld **Ervaring** op de pagina **Bedrijfsgegevens** in te stellen op *Premium*.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-137">It is possible to enable and try the full functionality of the standard version of [!INCLUDE[prod_short](includes/prod_short.md)] in a sandbox tenant by setting the **Experience** field on the **Company Information** page to *Premium*.</span></span> Zoek de pagina **Bedrijfsgegevens** in het menu van het :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="pictogram Instellingen":::.  

<span data-ttu-id="1d0fa-139">Nadat u de *Premium*-gebruikerservaring hebt ingeschakeld, krijgt u toegang tot alle standaardprofielen (rollen) en Rolcentra in de standaardversie.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-139">After you have enabled the *Premium* user experience, you get access to all the standard profiles (roles) and Role Centers in the standard version.</span></span> <span data-ttu-id="1d0fa-140">U kunt ook een evaluatiebedrijf maken dat volledig is ingesteld, inclusief demonstratiegegevens en toegang tot de geavanceerde gebieden van het product.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-140">You can also create an evaluation company that is fully set up, including demonstration data and access to the advanced areas of the product.</span></span> <span data-ttu-id="1d0fa-141">U kunt ook contact opnemen met een wederverkoper voor een demonstratie van de mogelijkheden.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-141">Alternatively, contact a reselling partner for a demonstration of the capabilities.</span></span> <span data-ttu-id="1d0fa-142">Zie [Hoe vind ik een partner-reseller?](/dynamics365/business-central/across-faq.yml#findpartner) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-142">For more information, see [How do I find a reselling partner?](/dynamics365/business-central/across-faq.yml#findpartner).</span></span>  

### <a name="complete-sample-data"></a><span data-ttu-id="1d0fa-143">Volledige voorbeeldgegevens</span><span class="sxs-lookup"><span data-stu-id="1d0fa-143">Complete sample data</span></span>

<span data-ttu-id="1d0fa-144">Neem voor situaties waarin u aanvullende voorbeeldgegevens nodig heeft, contact op met uw wederverkoper.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-144">For situations where you need additional sample data, please talk to your reselling partner.</span></span>
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

#### <a name="to-create-a-company-with-complete-sample-data-in-a-sandbox"></a><span data-ttu-id="1d0fa-145">Een bedrijf maken met volledige voorbeeldgegevens in een sandbox</span><span class="sxs-lookup"><span data-stu-id="1d0fa-145">To create a company with complete sample data in a sandbox</span></span>

1. <span data-ttu-id="1d0fa-146">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bedrijven** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-146">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1d0fa-147">Kies de actie **Nieuw** en kies vervolgens **Nieuw bedrijf maken**.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-147">Choose the **New** action, and then choose **Create New Company**.</span></span>  
3. <span data-ttu-id="1d0fa-148">Kies op de pagina **Begeleide instelling voor het maken van een bedrijf** **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-148">In the **Assisted Setup for Creating a Company** page, choose **Next**.</span></span>  
4. <span data-ttu-id="1d0fa-149">Geef een naam op voor het nieuwe bedrijf en kies vervolgens in het veld **Selecteer de gegevens en de instelling om aan de slag te gaan** **Geavanceerde evaluatie - volledige voorbeeldgegevens**.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-149">Specify a name for the new company, and then, in the **Select the data and setup to get started** field, choose **Advanced Evaluation - Complete Sample Data**.</span></span>  
5. <span data-ttu-id="1d0fa-150">Voer de rest van de begeleide instelling uit.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-150">Complete the rest of the assisted setup guide.</span></span>  

<span data-ttu-id="1d0fa-151">Wanneer de begeleide instelling is voltooid, kunt u beginnen met het verkennen van het nieuwe bedrijf met de volledige voorbeeldgegevens.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-151">When the assisted setup guide completes, you can start exploring the new company with the complete sample data.</span></span> <span data-ttu-id="1d0fa-152">Zie [Nieuwe bedrijven maken in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-152">For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).</span></span>  

### <a name="designer"></a><span data-ttu-id="1d0fa-153">Ontwerper</span><span class="sxs-lookup"><span data-stu-id="1d0fa-153">Designer</span></span>

<span data-ttu-id="1d0fa-154">In een sandboxomgeving is de **Ontwerper** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="1d0fa-154">In a sandbox environment, you will find the **Designer** enabled.</span></span> <span data-ttu-id="1d0fa-155">U kunt de Ontwerper activeren door het ontwerppictogram ![Ontwerper](./media/across-sandbox/sandbox-inclient-design-icon.png) te selecteren op een pagina of door de menuoptie **Ontwerp** te kiezen in het menu ![Instellingen](media/ui-experience/settings_icon_small.png).</span><span class="sxs-lookup"><span data-stu-id="1d0fa-155">You can activate Designer by selecting the design icon ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) on a page, or by choosing the **Design** menu item in the ![Settings](media/ui-experience/settings_icon_small.png) Settings menu.</span></span>  

<span data-ttu-id="1d0fa-156">Voor meer informatie zie [Designer gebruiken](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) in de inhoud voor ontwikkelaars en beheerders (alleen in het Engels).</span><span class="sxs-lookup"><span data-stu-id="1d0fa-156">For more information, see [Using Designer](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) in the developer and admin content (in English only).</span></span>  

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a><span data-ttu-id="1d0fa-157">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1d0fa-157">See Also</span></span>

<span data-ttu-id="1d0fa-158">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1d0fa-158">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="1d0fa-159">[[!INCLUDE[prod_long](includes/prod_long.md)]-proefversies en -abonnementen](across-preview.md)</span><span class="sxs-lookup"><span data-stu-id="1d0fa-159">[[!INCLUDE[prod_long](includes/prod_long.md)] Trials and Subscriptions](across-preview.md)</span></span>  
[<span data-ttu-id="1d0fa-160">Omgevingen beheren in het Business Central-beheercentrum</span><span class="sxs-lookup"><span data-stu-id="1d0fa-160">Managing Environments in the Business Central administration center</span></span>](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
