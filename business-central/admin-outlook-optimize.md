---
title: Outlook optimaliseren voor uw bedrijfsinbox
description: Meer informatie over wat u kunt doen om de ervaring met de bedrijfsinbox te verbeteren in Microsoft Outlook.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Outlook, Microsoft 365, inbox, business inbox, WebView2, Edge, addin, add-in
ms.date: 05/12/2021
ms.author: jswymer
ms.openlocfilehash: 2fee1782057d0f45319e4d12d715c2e1e0d3d4a6
ms.sourcegitcommit: 61e279b253370cdf87b7bc1ee0f927e4f0521344
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 05/19/2021
ms.locfileid: "6064868"
---
# <a name="optimizing-outlook-for-your-business-inbox"></a><span data-ttu-id="86c4f-103">Outlook optimaliseren voor uw bedrijfsinbox</span><span class="sxs-lookup"><span data-stu-id="86c4f-103">Optimizing Outlook for Your Business Inbox</span></span> 

<span data-ttu-id="86c4f-104">In dit artikel wordt besproken wat u kunt doen om de best mogelijke ervaring te krijgen met de bedrijfsinbox in Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="86c4f-104">This article discusses things you can do to get the best possible experience with the Business Inbox in Microsoft Outlook.</span></span> 

## <a name="update-outlook"></a><span data-ttu-id="86c4f-105">Outlook bijwerken</span><span class="sxs-lookup"><span data-stu-id="86c4f-105">Update Outlook</span></span>

<span data-ttu-id="86c4f-106">Update naar Outlook-versie 2012 of nieuwer.</span><span class="sxs-lookup"><span data-stu-id="86c4f-106">Update to Outlook version 2012 or newer.</span></span>

> [!NOTE]
> <span data-ttu-id="86c4f-107">Als u Outlook niet kunt bijwerken naar versie 2012 of hoger, zorg er dan voor dat u ten minste bijwerkt naar versie 1905.</span><span class="sxs-lookup"><span data-stu-id="86c4f-107">If you are unable to update Outlook to version 2012 or later, make sure that you at least update to version 1905.</span></span> <span data-ttu-id="86c4f-108">Dit voorkomt dat de Outlook-invoegtoepassing wordt uitgevoerd met legacy Internet Explorer-componenten</span><span class="sxs-lookup"><span data-stu-id="86c4f-108">This prevents the Outlook Add-in from running using legacy Internet Explorer components</span></span>

### <a name="how-to-check-your-version-of-outlook"></a><span data-ttu-id="86c4f-109">Hoe u uw versie van Outlook kunt controleren</span><span class="sxs-lookup"><span data-stu-id="86c4f-109">How to check your version of Outlook</span></span>

<span data-ttu-id="86c4f-110">Of u nu Office 2019 of Microsoft 365 gebruikt, volg deze Microsoft Support-gids om te controleren welke versie van Outlook u hebt:</span><span class="sxs-lookup"><span data-stu-id="86c4f-110">Whether you use Office 2019 or Microsoft 365, follow this Microsoft Support guide to check which version of Outlook you have:</span></span>  

[<span data-ttu-id="86c4f-111">Over Office: welke versie van Office gebruik ik?</span><span class="sxs-lookup"><span data-stu-id="86c4f-111">About Office: What version of Office am I using?</span></span>](https://support.microsoft.com/office/about-office-what-version-of-office-am-i-using-932788b8-a3ce-44bf-bb09-e334518b8b19)

### <a name="how-to-update-outlook"></a><span data-ttu-id="86c4f-112">Outlook bijwerken</span><span class="sxs-lookup"><span data-stu-id="86c4f-112">How to update Outlook</span></span>

<span data-ttu-id="86c4f-113">Volg deze Microsoft Support-gids of neem contact op met uw beheerder om Outlook bij te werken naar de nieuwste versie:</span><span class="sxs-lookup"><span data-stu-id="86c4f-113">To update Outlook to the latest version, follow this Microsoft Support guide or contact your administrator:</span></span>

[<span data-ttu-id="86c4f-114">Office-updates installeren</span><span class="sxs-lookup"><span data-stu-id="86c4f-114">Install Office updates</span></span>](https://support.microsoft.com/office/install-office-updates-2ab296f3-7f03-43a2-8e50-46de917611c5)

## <a name="install-microsoft-edge-webview2"></a><span data-ttu-id="86c4f-115">Microsoft Edge WebView2 installeren</span><span class="sxs-lookup"><span data-stu-id="86c4f-115">Install Microsoft Edge WebView2</span></span>

<span data-ttu-id="86c4f-116">Verzekeren dat Microsoft Edge WebView2 is geïnstalleerd op uw apparaat.</span><span class="sxs-lookup"><span data-stu-id="86c4f-116">Ensure that Microsoft Edge WebView2 is installed on your device.</span></span>

### <a name="how-to-check-if-microsoft-edge-webview2-is-installed"></a><span data-ttu-id="86c4f-117">Hoe te controleren of Microsoft Edge WebView2 is geïnstalleerd</span><span class="sxs-lookup"><span data-stu-id="86c4f-117">How to check if Microsoft Edge WebView2 is installed</span></span> 

<span data-ttu-id="86c4f-118">Om te controleren of u Microsoft Edge WebView2 hebt geïnstalleerd op een computer, voert u de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="86c4f-118">To check if you have Microsoft Edge WebView2 installed on a computer, do the following steps:</span></span>

<span data-ttu-id="86c4f-119">Vanuit het startmenu:</span><span class="sxs-lookup"><span data-stu-id="86c4f-119">From Start menu:</span></span>

1. <span data-ttu-id="86c4f-120">Kies **Start** ![Windows Start](media/windows-start-icon.png "Pictogram Windows Start") > **Instellingen** ![Windows-instellingen](media/windows-settings-icon.png "Pictogram Windows-instellingen") > **Apps en functies**.</span><span class="sxs-lookup"><span data-stu-id="86c4f-120">Choose **Start** ![Windows Start](media/windows-start-icon.png "Windows Start icon") > **Settings** ![Windows Settings](media/windows-settings-icon.png "Windows Settings icon") > **Apps & Features**.</span></span>
2. <span data-ttu-id="86c4f-121">Typ **WebView2** in het zoekvak.</span><span class="sxs-lookup"><span data-stu-id="86c4f-121">In the search box, type **WebView2**.</span></span> <span data-ttu-id="86c4f-122">Als Microsoft Edge WebView2 is geïnstalleerd, ziet u een item met de naam **Microsoft Edge WebView2 Runtime**.</span><span class="sxs-lookup"><span data-stu-id="86c4f-122">If Microsoft Edge WebView2 is installed, you'll see an entry called **Microsoft Edge WebView2 Runtime**.</span></span>

<span data-ttu-id="86c4f-123">Vanuit het Configuratiescherm:</span><span class="sxs-lookup"><span data-stu-id="86c4f-123">From Control Panel:</span></span>

1. <span data-ttu-id="86c4f-124">Typ in het zoekvak naast **Start** ![Windows Start](media/windows-start-icon.png "Pictogram Windows Start") **Configuratiescherm** en selecteer het resultaat.</span><span class="sxs-lookup"><span data-stu-id="86c4f-124">In the search box next to **Start** ![Windows Start](media/windows-start-icon.png "Windows Start icon"), type **Control Panel**, and then select the result.</span></span>
2. <span data-ttu-id="86c4f-125">Kies **Programma's** > **Programma's en functies**.</span><span class="sxs-lookup"><span data-stu-id="86c4f-125">Choose **Programs** > **Programs and Features**.</span></span>
3. <span data-ttu-id="86c4f-126">Typ **WebView2** in het zoekvak.</span><span class="sxs-lookup"><span data-stu-id="86c4f-126">In the search box, type **WebView2**.</span></span> <span data-ttu-id="86c4f-127">Als Microsoft Edge WebView2 is geïnstalleerd, ziet u een item met de naam **Microsoft Edge WebView2 Runtime**.</span><span class="sxs-lookup"><span data-stu-id="86c4f-127">If Microsoft Edge WebView2 is installed, you'll see an entry called **Microsoft Edge WebView2 Runtime**.</span></span>

### <a name="how-to-install-microsoft-edge-webview2"></a><span data-ttu-id="86c4f-128">Microsoft Edge WebView2 installeren</span><span class="sxs-lookup"><span data-stu-id="86c4f-128">How to install Microsoft Edge WebView2</span></span> 

1. <span data-ttu-id="86c4f-129">Ga met uw browser naar [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/).</span><span class="sxs-lookup"><span data-stu-id="86c4f-129">Using your browser, go to [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/).</span></span>
2. <span data-ttu-id="86c4f-130">Kies **Downloaden**.</span><span class="sxs-lookup"><span data-stu-id="86c4f-130">Choose **Download**.</span></span>
3. <span data-ttu-id="86c4f-131">Stel **Architectuur selecteren** in op uw systeem.</span><span class="sxs-lookup"><span data-stu-id="86c4f-131">Set **Select Architecture** to match your system.</span></span>
4. <span data-ttu-id="86c4f-132">Kies **Downloaden**.</span><span class="sxs-lookup"><span data-stu-id="86c4f-132">Choose **Download**.</span></span>

> [!NOTE]
> <span data-ttu-id="86c4f-133">Uw organisatie heeft mogelijk beperkingen op welke componenten op uw apparaat kunnen worden geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="86c4f-133">Your organization may have restriction on which components can be installed on your device.</span></span> <span data-ttu-id="86c4f-134">Neem contact op met uw beheerder voor hulp.</span><span class="sxs-lookup"><span data-stu-id="86c4f-134">Contact your administrator for assistance.</span></span>

## <a name="use-a-supported-browser"></a><span data-ttu-id="86c4f-135">Een ondersteunde browser gebruiken</span><span class="sxs-lookup"><span data-stu-id="86c4f-135">Use a supported browser</span></span>

<span data-ttu-id="86c4f-136">Overweeg om Outlook voor het web te gebruiken in een van de browsers die door Business Central worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="86c4f-136">Consider using Outlook for the Web in one of the browsers supported by Business Central.</span></span> <span data-ttu-id="86c4f-137">Zie voor een lijst met ondersteunde browsers [Minimumvereisten voor het gebruik van Business Central](product-requirements.md#browsers).</span><span class="sxs-lookup"><span data-stu-id="86c4f-137">For a list of supported browsers, see [Minimum Requirements for Using Business Central](product-requirements.md#browsers).</span></span>

## <a name="see-also"></a><span data-ttu-id="86c4f-138">Zie ook</span><span class="sxs-lookup"><span data-stu-id="86c4f-138">See Also</span></span>

[<span data-ttu-id="86c4f-139">Voorbereid zijn om zaken te doen</span><span class="sxs-lookup"><span data-stu-id="86c4f-139">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
[<span data-ttu-id="86c4f-140">Business Central op mijn mobiele apparaat krijgen</span><span class="sxs-lookup"><span data-stu-id="86c4f-140">Getting Business Central on my Mobile Device</span></span>](install-mobile-app.md)  
[<span data-ttu-id="86c4f-141">Documenten per e-mail verzenden</span><span class="sxs-lookup"><span data-stu-id="86c4f-141">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
[<span data-ttu-id="86c4f-142">Financiën</span><span class="sxs-lookup"><span data-stu-id="86c4f-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="86c4f-143">Verkoop</span><span class="sxs-lookup"><span data-stu-id="86c4f-143">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="86c4f-144">Inkoop</span><span class="sxs-lookup"><span data-stu-id="86c4f-144">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="86c4f-145">Minimale vereisten voor Outlook</span><span class="sxs-lookup"><span data-stu-id="86c4f-145">Minimum Requirements for Outlook</span></span>](product-requirements.md#outlook)  
[<span data-ttu-id="86c4f-146">Invoegtoepassingen gebruiken in Outlook op het web</span><span class="sxs-lookup"><span data-stu-id="86c4f-146">Using add-ins in Outlook on the web</span></span>](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]