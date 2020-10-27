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
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 718d4378a897b187ba3073449869184fef5cec98
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924840"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a><span data-ttu-id="70d52-103">Verbinding met uw Business Central-gegevens maken om een bedrijfsapp te maken met Power Apps</span><span class="sxs-lookup"><span data-stu-id="70d52-103">Connecting to Your Business Central Data to Build a Business App Using Power Apps</span></span>

<span data-ttu-id="70d52-104">U kunt uw [!INCLUDE[prodshort](includes/prodshort.md)]-gegevens als gegevensbron beschikbaar maken in Power Apps.</span><span class="sxs-lookup"><span data-stu-id="70d52-104">You can make your [!INCLUDE[prodshort](includes/prodshort.md)] data available as a data source in Power Apps.</span></span>  

> [!NOTE]  
> <span data-ttu-id="70d52-105">U moet een geldig account bij [!INCLUDE[prodshort](includes/prodshort.md)] en Power Apps hebben.</span><span class="sxs-lookup"><span data-stu-id="70d52-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power Apps.</span></span>  

## <a name="to-add-prodshort-as-a-data-source-in-power-apps"></a><span data-ttu-id="70d52-106">[!INCLUDE[prodshort](includes/prodshort.md)] als gegevensbron toevoegen in Power Apps</span><span class="sxs-lookup"><span data-stu-id="70d52-106">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power Apps</span></span>

1. <span data-ttu-id="70d52-107">Navigeer in de browser naar [powerapps.microsoft.com](https://powerapps.microsoft.com/) en meld u aan.</span><span class="sxs-lookup"><span data-stu-id="70d52-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/), and then sign in.</span></span>
2. <span data-ttu-id="70d52-108">Kies op de startpagina in de sectie **Start vanuit gegevens** de tegel **Andere gegevensbronnen** .</span><span class="sxs-lookup"><span data-stu-id="70d52-108">On the Home page, in the **Start from data** section, choose the **Other data sources** tile.</span></span>  

    <span data-ttu-id="70d52-109">Dit opent Power Apps Studio.</span><span class="sxs-lookup"><span data-stu-id="70d52-109">This opens Power Apps Studio.</span></span> <span data-ttu-id="70d52-110">Bij de eerste aanmelding moet u het land/regio specificeren.</span><span class="sxs-lookup"><span data-stu-id="70d52-110">On first login, you must specify the country/region.</span></span>  
3. <span data-ttu-id="70d52-111">Kies in de lijst met beschikbare verbindingen **Business Central** en kies de knop **Maken** .</span><span class="sxs-lookup"><span data-stu-id="70d52-111">In the list of available connections, choose **Business Central** , and then choose the **Create** button.</span></span>

    <span data-ttu-id="70d52-112">Power Apps maakt verbinding met uw [!INCLUDE[prodshort](includes/prodshort.md)] met behulp van de aanmeldingsgegevens waarmee u bent aangemeld.</span><span class="sxs-lookup"><span data-stu-id="70d52-112">Power Apps will connect to your [!INCLUDE[prodshort](includes/prodshort.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="70d52-113">Als u geen beheerder hebt van uw [!INCLUDE[prodshort](includes/prodshort.md)], kunt u zich met een ander account aanmelden.</span><span class="sxs-lookup"><span data-stu-id="70d52-113">If you are not an administrator of your [!INCLUDE[prodshort](includes/prodshort.md)], you may have to sign in with another account.</span></span>  

4. <span data-ttu-id="70d52-114">Met Power Apps wordt een lijst met *omgevingen en bedrijven* weergegeven die beschikbaar zijn in [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="70d52-114">Power Apps will display a list of *Environments and companies* that are available from [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="70d52-115">Kies de omgeving en het bedrijf met de gegevens waarmee u verbinding wilt maken, bijvoorbeeld *PRODUCTIE - Mijn bedrijf* .</span><span class="sxs-lookup"><span data-stu-id="70d52-115">Choose the environment and company that contains the data you want to connect to, such as *PRODUCTION - My Company* .</span></span>  

5. <span data-ttu-id="70d52-116">Vervolgens krijgt u een lijst met tabellen te zien die worden weergegeven als onderdeel van de API voor uw omgeving.</span><span class="sxs-lookup"><span data-stu-id="70d52-116">Next, you will be presented with a list of tables that are exposed as part of the API for your environment.</span></span> <span data-ttu-id="70d52-117">Selecteer de tabel waarmee u verbinding wilt maken en kies vervolgens **Verbinden** .</span><span class="sxs-lookup"><span data-stu-id="70d52-117">Select the table that you want to connect to, and then choose **Connect** .</span></span>

<span data-ttu-id="70d52-118">Deze zogenaamde tabellen worden door de [!INCLUDE[prodshort](includes/prodshort.md)]-connector voor Power Apps als eindpunten beschikbaar gemaakt.</span><span class="sxs-lookup"><span data-stu-id="70d52-118">These so-called tables are exposed as endpoints by the [!INCLUDE[prodshort](includes/prodshort.md)] connector for Power Apps.</span></span>  

> [!NOTE]
> <span data-ttu-id="70d52-119">Als u gegevens uit andere tabellen in [!INCLUDE[prodshort](includes/prodshort.md)] in uw app wilt opnemen, moet u met een ontwikkelaar werken om een aangepaste API te maken in [!INCLUDE[prodshort](includes/prodshort.md)] en vervolgens die aangepaste API gebruiken via een aangepaste connector in Power Apps.</span><span class="sxs-lookup"><span data-stu-id="70d52-119">If you want to include data from other tables in [!INCLUDE[prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE[prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in Power Apps.</span></span> <span data-ttu-id="70d52-120">Zie voor meer informatie [Een nieuwe aangepaste connector maken](/connectors/custom-connectors/define-blank).</span><span class="sxs-lookup"><span data-stu-id="70d52-120">For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).</span></span>  

<span data-ttu-id="70d52-121">Nu hebt u met succes een koppeling gemaakt naar uw [!INCLUDE[prodshort](includes/prodshort.md)]-gegevens en kunt u uw PowerApp gaan maken.</span><span class="sxs-lookup"><span data-stu-id="70d52-121">At this point, you have successfully connected to your [!INCLUDE[prodshort](includes/prodshort.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="70d52-122">U kunt extra schermen toevoegen en verbinding met extra gegevens maken vanuit uw [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="70d52-122">You can add additional screens and connect to additional data from your [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="70d52-123">Zie voor meer informatie [Een canvasapp maken vanuit een voorbeeld in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span><span class="sxs-lookup"><span data-stu-id="70d52-123">For more information, see [Create a canvas app from a sample in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span></span>  

<span data-ttu-id="70d52-124">Wanneer u de app hebt ontworpen en gemaakt, u deze met uw collega's delen.</span><span class="sxs-lookup"><span data-stu-id="70d52-124">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="70d52-125">Zie voor meer informatie [Een canvasapp opslaan en publiceren in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="70d52-125">For more information, see [Save and publish a canvas app in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="70d52-126">Als u verbinding wilt maken met [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, moet u de connector **Business Central (on-premises)** kiezen in stap 3.</span><span class="sxs-lookup"><span data-stu-id="70d52-126">If you want to connect to [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="70d52-127">Zie ook</span><span class="sxs-lookup"><span data-stu-id="70d52-127">See Also</span></span>

[<span data-ttu-id="70d52-128">Een canvasapp maken vanuit een sjabloon in Power Apps</span><span class="sxs-lookup"><span data-stu-id="70d52-128">Create a canvas app from a template in Power Apps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="70d52-129">Bedrijfsgegevens importeren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="70d52-129">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="70d52-130">[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="70d52-130">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="70d52-131">Aan de slag met het ontwikkelen van verbindingsapps voor Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="70d52-131">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
