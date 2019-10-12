---
title: Gebruik uw gegevens om een app te maken| Microsoft Docs
description: U kunt uw Business Central-gegevens als gegevensbron beschikbaar maken en een OData-URL van uw webservices opgeven om een bedrijfsapp te maken met PowerApps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 4b8005154afb988cf25c6a04b7beeaafd199afca
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305047"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a><span data-ttu-id="9ad07-103">Verbinding met uw Business Central-gegevens maken om een bedrijfsapp te maken met PowerApps</span><span class="sxs-lookup"><span data-stu-id="9ad07-103">Connecting to Your Business Central Data to Build a Business App Using PowerApps</span></span>
<span data-ttu-id="9ad07-104">U kunt uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens als gegevensbron beschikbaar maken in PowerApps.</span><span class="sxs-lookup"><span data-stu-id="9ad07-104">You can make your [!INCLUDE[d365fin](includes/d365fin_md.md)] data available as a data source in PowerApps.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="9ad07-105">U moet een geldig account bij [!INCLUDE[d365fin](includes/d365fin_md.md)] en PowerApps hebben.</span><span class="sxs-lookup"><span data-stu-id="9ad07-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with PowerApps.</span></span>  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-powerapps"></a><span data-ttu-id="9ad07-106">[!INCLUDE[d365fin](includes/d365fin_md.md)] als gegevensbron toevoegen in PowerApps</span><span class="sxs-lookup"><span data-stu-id="9ad07-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in PowerApps</span></span>
1. <span data-ttu-id="9ad07-107">Navigeer in de browser naar [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) en meld u aan.</span><span class="sxs-lookup"><span data-stu-id="9ad07-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="9ad07-108">Kies op de startpagina **Apps**, **Een app maken** en **Canvas** om een nieuwe canvas-app te maken.</span><span class="sxs-lookup"><span data-stu-id="9ad07-108">On the Home page, choose the **Apps**, **Create an app** and **Canvas** to create a new canvas app.</span></span> <span data-ttu-id="9ad07-109">Deze app wordt ontworpen voor gebruik op een mobiel apparaat, maar u kunt ook een andere sjabloon gebruiken.</span><span class="sxs-lookup"><span data-stu-id="9ad07-109">This app will be designed for use on a mobile device, but you can also choose to use another template.</span></span>

    <span data-ttu-id="9ad07-110">De volgende stap om een PowerApp te maken bestaat eruit uw gegevens te selecteren.</span><span class="sxs-lookup"><span data-stu-id="9ad07-110">The next step to create a PowerApp is to select your data.</span></span> <span data-ttu-id="9ad07-111">Kies het pijlpictogram en kies vervolgens de optie **Nieuwe verbinding** linksboven in de pagina.</span><span class="sxs-lookup"><span data-stu-id="9ad07-111">Choose the Arrow icon then choose the **New connection** option in the upper left side of the page.</span></span>
3. <span data-ttu-id="9ad07-112">Kies in de lijst met beschikbare verbindingen **Business Central** en kies de knop **Maken**.</span><span class="sxs-lookup"><span data-stu-id="9ad07-112">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="9ad07-113">PowerApps maakt verbinding met uw [!INCLUDE [prodshort](includes/prodshort.md)] met behulp van de aanmeldingsgegevens waarmee u bent aangemeld.</span><span class="sxs-lookup"><span data-stu-id="9ad07-113">PowerApps will connect to your [!INCLUDE [prodshort](includes/prodshort.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="9ad07-114">Als u geen beheerder hebt van uw [!INCLUDE [prodshort](includes/prodshort.md)], kunt u zich met een ander account aanmelden.</span><span class="sxs-lookup"><span data-stu-id="9ad07-114">If you are not an administrator of your [!INCLUDE [prodshort](includes/prodshort.md)], you may have to sign in with another account.</span></span>  

4.  <span data-ttu-id="9ad07-115">Met PowerApps wordt een lijst met *omgevingen en bedrijven* weergegeven die beschikbaar zijn in [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="9ad07-115">PowerApps will display a list of *Environments and companies* that are available from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="9ad07-116">Kies de omgeving en het bedrijf met de gegevens waarmee u verbinding wilt maken.</span><span class="sxs-lookup"><span data-stu-id="9ad07-116">Choose the environment and company that contains the data you want to connect to.</span></span> <span data-ttu-id="9ad07-117">Vervolgens krijgt u een lijst met API's te zien.</span><span class="sxs-lookup"><span data-stu-id="9ad07-117">Next, you will be presented with a list of APIs.</span></span> <span data-ttu-id="9ad07-118">Selecteer de **API** waarmee u verbinding wilt maken.</span><span class="sxs-lookup"><span data-stu-id="9ad07-118">Select the **API** you want to connect to.</span></span>

<span data-ttu-id="9ad07-119">Deze zogenaamde tabellen maken deel uit van de [!INCLUDE [prodshort](includes/prodshort.md)] API.</span><span class="sxs-lookup"><span data-stu-id="9ad07-119">These so-called tables are part of the [!INCLUDE [prodshort](includes/prodshort.md)] API.</span></span> <span data-ttu-id="9ad07-120">U hoeft de eindpunten niet zelf te configureren. De [!INCLUDE [prodshort](includes/prodshort.md)]-connector voor PowerApps doet dat voor u.</span><span class="sxs-lookup"><span data-stu-id="9ad07-120">You do not have to configure the end points yourself - the [!INCLUDE [prodshort](includes/prodshort.md)] connector for PowerApps does it for you.</span></span>  

    If you want to include data from other tables in [!INCLUDE [prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE [prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in PowerApps. For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).  

<span data-ttu-id="9ad07-121">Nu hebt u met succes een koppeling gemaakt naar uw [!INCLUDE [prodshort](includes/prodshort.md)]-gegevens en kunt u uw PowerApp gaan maken.</span><span class="sxs-lookup"><span data-stu-id="9ad07-121">At this point, you have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="9ad07-122">U kunt extra schermen toevoegen en verbinding met extra gegevens maken vanuit uw [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="9ad07-122">You can add additional screens and connect to additional data from your [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="9ad07-123">Zie voor meer informatie [Een canvasapp maken vanuit een sjabloon in PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).</span><span class="sxs-lookup"><span data-stu-id="9ad07-123">For more information, see [Create a canvas app from a template in PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).</span></span>  

<span data-ttu-id="9ad07-124">Wanneer u de app hebt ontworpen en gemaakt, u deze met uw collega's delen.</span><span class="sxs-lookup"><span data-stu-id="9ad07-124">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="9ad07-125">Zie voor meer informatie [Een canvasapp opslaan en publiceren in PowerApps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="9ad07-125">For more information, see [Save and publish a canvas app in PowerApps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="9ad07-126">Als u verbinding wilt maken met [!INCLUDE [prodshort](includes/prodshort.md)] on-premises, moet u de connector **Business Central (on-premises)** kiezen in stap 3.</span><span class="sxs-lookup"><span data-stu-id="9ad07-126">If you want to connect to [!INCLUDE [prodshort](includes/prodshort.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9ad07-127">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9ad07-127">See Also</span></span>

[<span data-ttu-id="9ad07-128">Een canvasapp maken vanuit een sjabloon in PowerApps</span><span class="sxs-lookup"><span data-stu-id="9ad07-128">Create a canvas app from a template in PowerApps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="9ad07-129">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="9ad07-129">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="9ad07-130">Bedrijfsgegevens importeren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="9ad07-130">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="9ad07-131">[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="9ad07-131">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="9ad07-132">Financiën</span><span class="sxs-lookup"><span data-stu-id="9ad07-132">Finance</span></span>](finance.md)  
[<span data-ttu-id="9ad07-133">Aan de slag met het ontwikkelen van verbindingsapps voor Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="9ad07-133">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
