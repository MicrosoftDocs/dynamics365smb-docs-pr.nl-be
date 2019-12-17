---
title: Gebruik uw gegevens om een app te maken| Microsoft Docs
description: U kunt uw Business Central-gegevens als gegevensbron beschikbaar maken en een OData-URL van uw webservices opgeven om een bedrijfsapp te maken met Power Apps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 11/20/2019
ms.author: edupont
ms.openlocfilehash: 9cf587dca8224e742ecbde30bcabc35697bb6f2a
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881012"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a><span data-ttu-id="ba281-103">Verbinding met uw Business Central-gegevens maken om een bedrijfsapp te maken met Power Apps</span><span class="sxs-lookup"><span data-stu-id="ba281-103">Connecting to Your Business Central Data to Build a Business App Using Power Apps</span></span>

<span data-ttu-id="ba281-104">U kunt uw [!INCLUDE[prodshort](includes/prodshort.md)]-gegevens als gegevensbron beschikbaar maken in Power Apps.</span><span class="sxs-lookup"><span data-stu-id="ba281-104">You can make your [!INCLUDE[prodshort](includes/prodshort.md)] data available as a data source in Power Apps.</span></span>  

> [!NOTE]  
> <span data-ttu-id="ba281-105">U moet een geldig account bij [!INCLUDE[prodshort](includes/prodshort.md)] en Power Apps hebben.</span><span class="sxs-lookup"><span data-stu-id="ba281-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power Apps.</span></span>  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-apps"></a><span data-ttu-id="ba281-106">[!INCLUDE[prodshort](includes/prodshort.md)] als gegevensbron in Power Apps toevoegen</span><span class="sxs-lookup"><span data-stu-id="ba281-106">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power Apps</span></span>

1. <span data-ttu-id="ba281-107">Navigeer in de browser naar [powerapps.microsoft.com](https://powerapps.microsoft.com/) en meld u aan.</span><span class="sxs-lookup"><span data-stu-id="ba281-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/), and then sign in.</span></span>
2. <span data-ttu-id="ba281-108">Kies op de startpagina **Apps**, **Een app maken** en **Canvas** om een nieuwe canvas-app te maken.</span><span class="sxs-lookup"><span data-stu-id="ba281-108">On the Home page, choose the **Apps**, **Create an app** and **Canvas** to create a new canvas app.</span></span> <span data-ttu-id="ba281-109">Deze app wordt ontworpen voor gebruik op een mobiel apparaat, maar u kunt ook een andere sjabloon gebruiken.</span><span class="sxs-lookup"><span data-stu-id="ba281-109">This app will be designed for use on a mobile device, but you can also choose to use another template.</span></span>

    <span data-ttu-id="ba281-110">De volgende stap om een Power App te maken bestaat eruit uw gegevens te selecteren.</span><span class="sxs-lookup"><span data-stu-id="ba281-110">The next step to create a Power App is to select your data.</span></span> <span data-ttu-id="ba281-111">Kies het pijlpictogram en kies vervolgens de optie **Nieuwe verbinding** linksboven in de pagina.</span><span class="sxs-lookup"><span data-stu-id="ba281-111">Choose the Arrow icon then choose the **New connection** option in the upper left side of the page.</span></span>
3. <span data-ttu-id="ba281-112">Kies in de lijst met beschikbare verbindingen **Business Central** en kies de knop **Maken**.</span><span class="sxs-lookup"><span data-stu-id="ba281-112">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="ba281-113">Power Apps maakt verbinding met uw [!INCLUDE [prodshort](includes/prodshort.md)] met behulp van de aanmeldingsgegevens waarmee u bent aangemeld.</span><span class="sxs-lookup"><span data-stu-id="ba281-113">Power Apps will connect to your [!INCLUDE [prodshort](includes/prodshort.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="ba281-114">Als u geen beheerder hebt van uw [!INCLUDE [prodshort](includes/prodshort.md)], kunt u zich met een ander account aanmelden.</span><span class="sxs-lookup"><span data-stu-id="ba281-114">If you are not an administrator of your [!INCLUDE [prodshort](includes/prodshort.md)], you may have to sign in with another account.</span></span>  

4. <span data-ttu-id="ba281-115">Met Power Apps wordt een lijst met *omgevingen en bedrijven* weergegeven die beschikbaar zijn in [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="ba281-115">Power Apps will display a list of *Environments and companies* that are available from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="ba281-116">Kies de omgeving en het bedrijf met de gegevens waarmee u verbinding wilt maken.</span><span class="sxs-lookup"><span data-stu-id="ba281-116">Choose the environment and company that contains the data you want to connect to.</span></span> <span data-ttu-id="ba281-117">Vervolgens krijgt u een lijst met API's te zien.</span><span class="sxs-lookup"><span data-stu-id="ba281-117">Next, you will be presented with a list of APIs.</span></span> <span data-ttu-id="ba281-118">Selecteer de **API** waarmee u verbinding wilt maken.</span><span class="sxs-lookup"><span data-stu-id="ba281-118">Select the **API** you want to connect to.</span></span>

<span data-ttu-id="ba281-119">Deze zogenaamde tabellen maken deel uit van de [!INCLUDE [prodshort](includes/prodshort.md)] API.</span><span class="sxs-lookup"><span data-stu-id="ba281-119">These so-called tables are part of the [!INCLUDE [prodshort](includes/prodshort.md)] API.</span></span> <span data-ttu-id="ba281-120">U hoeft de eindpunten niet zelf te configureren. De [!INCLUDE [prodshort](includes/prodshort.md)]-connector voor Power Apps doet dat voor u.</span><span class="sxs-lookup"><span data-stu-id="ba281-120">You do not have to configure the end points yourself - the [!INCLUDE [prodshort](includes/prodshort.md)] connector for Power Apps does it for you.</span></span>  

> [!NOTE]
> <span data-ttu-id="ba281-121">Als u gegevens uit andere tabellen in [!INCLUDE [prodshort](includes/prodshort.md)] in uw app wilt opnemen, moet u met een ontwikkelaar werken om een aangepaste API te maken in [!INCLUDE [prodshort](includes/prodshort.md)] en vervolgens die aangepaste API gebruiken via een aangepaste connector in Power Apps.</span><span class="sxs-lookup"><span data-stu-id="ba281-121">If you want to include data from other tables in [!INCLUDE [prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE [prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in Power Apps.</span></span> <span data-ttu-id="ba281-122">Zie voor meer informatie [Een nieuwe aangepaste connector maken](/connectors/custom-connectors/define-blank).</span><span class="sxs-lookup"><span data-stu-id="ba281-122">For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).</span></span>  

<span data-ttu-id="ba281-123">Nu hebt u met succes een koppeling gemaakt naar uw [!INCLUDE [prodshort](includes/prodshort.md)]-gegevens en kunt u uw PowerApp gaan maken.</span><span class="sxs-lookup"><span data-stu-id="ba281-123">At this point, you have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="ba281-124">U kunt extra schermen toevoegen en verbinding met extra gegevens maken vanuit uw [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="ba281-124">You can add additional screens and connect to additional data from your [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="ba281-125">Zie voor meer informatie [Een canvasapp maken vanuit een sjabloon in Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive).</span><span class="sxs-lookup"><span data-stu-id="ba281-125">For more information, see [Create a canvas app from a template in Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive).</span></span>  

<span data-ttu-id="ba281-126">Wanneer u de app hebt ontworpen en gemaakt, u deze met uw collega's delen.</span><span class="sxs-lookup"><span data-stu-id="ba281-126">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="ba281-127">Zie voor meer informatie [Een canvasapp opslaan en publiceren in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="ba281-127">For more information, see [Save and publish a canvas app in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="ba281-128">Als u verbinding wilt maken met [!INCLUDE [prodshort](includes/prodshort.md)] on-premises, moet u de connector **Business Central (on-premises)** kiezen in stap 3.</span><span class="sxs-lookup"><span data-stu-id="ba281-128">If you want to connect to [!INCLUDE [prodshort](includes/prodshort.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ba281-129">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ba281-129">See Also</span></span>

[<span data-ttu-id="ba281-130">Een canvasapp maken vanuit een sjabloon in Power Apps</span><span class="sxs-lookup"><span data-stu-id="ba281-130">Create a canvas app from a template in Power Apps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="ba281-131">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="ba281-131">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="ba281-132">Bedrijfsgegevens importeren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="ba281-132">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="ba281-133">[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="ba281-133">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="ba281-134">Financiën</span><span class="sxs-lookup"><span data-stu-id="ba281-134">Finance</span></span>](finance.md)  
[<span data-ttu-id="ba281-135">Aan de slag met het ontwikkelen van verbindingsapps voor Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="ba281-135">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
