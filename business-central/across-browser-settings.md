---
title: Uw browser instellen
description: Beschrijft hoe u browsers instelt om te werken met Business Central en producten die ermee integreren.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, web client, troubleshooting, errors
ms.date: 01/08/2021
ms.author: jswymer
ms.openlocfilehash: b5083735be31b635cb3fc3ce404e7f182d04640f
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384986"
---
# <a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a><span data-ttu-id="14f54-103">Uw browser instellen en er problemen mee oplossen om te werken met de Business Central-webclient</span><span class="sxs-lookup"><span data-stu-id="14f54-103">Setting Up and Troubleshooting Your Browser to Work With Business Central Web Client</span></span>

<span data-ttu-id="14f54-104">In dit artikel wordt uitgelegd hoe u uw browser zo instelt dat de [!INCLUDE[web_client](includes/web_client.md)] en al zijn functies werken naar behoren.</span><span class="sxs-lookup"><span data-stu-id="14f54-104">This article explains how to set up your browser so that the [!INCLUDE[web_client](includes/web_client.md)] and all its features work properly.</span></span> <span data-ttu-id="14f54-105">Lees dit artikel als u problemen ondervindt bij het openen van de [!INCLUDE[web_client](includes/web_client.md)], omdat sommige problemen kunnen worden veroorzaakt door de instellingen van uw browser.</span><span class="sxs-lookup"><span data-stu-id="14f54-105">Read this article if you're having problems opening the [!INCLUDE[web_client](includes/web_client.md)], because some problems may be caused by your browser's settings.</span></span>

<span data-ttu-id="14f54-106">Het artikel bevat details voor het instellen van Microsoft Edge, maar de vereisten voor JavaScript, cookies en pop-ups zijn hetzelfde voor alle ondersteunde browsers.</span><span class="sxs-lookup"><span data-stu-id="14f54-106">The article provides details for setting up Microsoft Edge, but the requirements for JavaScript, cookies, and pop-ups are the same for all supported browsers.</span></span> <span data-ttu-id="14f54-107">Raadpleeg voor andere browsers de instructies van de fabrikant.</span><span class="sxs-lookup"><span data-stu-id="14f54-107">For other browsers, refer to the instructions provided by the manufacturer.</span></span>  

## <a name="use-a-supported-browser"></a><span data-ttu-id="14f54-108">Een ondersteunde browser gebruiken</span><span class="sxs-lookup"><span data-stu-id="14f54-108">Use a supported browser</span></span>

<span data-ttu-id="14f54-109">Zorg ervoor dat u een van de ondersteunde browsers gebruikt.</span><span class="sxs-lookup"><span data-stu-id="14f54-109">Make sure to use a one of the supported browsers.</span></span> <span data-ttu-id="14f54-110">Zie [Minimumvereisten om Business Central te gebruiken](product-requirements.md#recommended-browsers).</span><span class="sxs-lookup"><span data-stu-id="14f54-110">See [Minimum Requirements for Using Business Central](product-requirements.md#recommended-browsers).</span></span>  

## <a name="allow-javascript-from-business-central"></a><span data-ttu-id="14f54-111">JavaScript toestaan vanuit Business Central</span><span class="sxs-lookup"><span data-stu-id="14f54-111">Allow JavaScript from Business Central</span></span>

<span data-ttu-id="14f54-112">*Probleem:*</span><span class="sxs-lookup"><span data-stu-id="14f54-112">*Problem:*</span></span>

<span data-ttu-id="14f54-113">Als de browser JavaScript niet toestaat, ziet u **NietOndersteund/UitgeschakeldJavaScript** op de adresbalk en een **HTTP-fout 404.0 - niet gevonden** bericht wanneer u probeert [!INCLUDE[prod_short](includes/prod_short.md)] te openen.</span><span class="sxs-lookup"><span data-stu-id="14f54-113">If the browser doesn't allow JavaScript, you'll see **NotSupported/DisabledJavaScript** in the address bar and an **HTTP Error 404.0 - Not Found** message when you try to open [!INCLUDE[prod_short](includes/prod_short.md)], and the</span></span> 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

<span data-ttu-id="14f54-114">*Oplossing:*</span><span class="sxs-lookup"><span data-stu-id="14f54-114">*Fix:*</span></span>

1. <span data-ttu-id="14f54-115">Ga in Microsoft Edge naar **Instellingen** > **Cookies en sitetoestemmingen** > **JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="14f54-115">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **JavaScript**.</span></span>
2. <span data-ttu-id="14f54-116">Ga op een van de volgende manieren te werk:</span><span class="sxs-lookup"><span data-stu-id="14f54-116">Do one of the following steps.</span></span> <span data-ttu-id="14f54-117">Kies de stap die wordt aanbevolen door uw organisatie:</span><span class="sxs-lookup"><span data-stu-id="14f54-117">Choose the step that is recommended by your organization:</span></span>

    - <span data-ttu-id="14f54-118">Verplaats de schakelaar **Toegestaan** naar links (Uit).</span><span class="sxs-lookup"><span data-stu-id="14f54-118">Move the **Allowed** toggle to the left (Off).</span></span> <span data-ttu-id="14f54-119">Selecteer vervolgens **Toevoegen** en typ het adres (URL) voor [!INCLUDE[prod_short](includes/prod_short.md)] in het vak **Site**.</span><span class="sxs-lookup"><span data-stu-id="14f54-119">Then, select **Add** and type the address (URL) for [!INCLUDE[prod_short](includes/prod_short.md)] in the **Site** box.</span></span> <span data-ttu-id="14f54-120">Selecteer **Toevoegen** wanneer u klaar bent.</span><span class="sxs-lookup"><span data-stu-id="14f54-120">Select **Add** when done.</span></span>
    - <span data-ttu-id="14f54-121">Verplaats de schakelaar **Toegestaan** naar rechts (Aan).</span><span class="sxs-lookup"><span data-stu-id="14f54-121">Move the **Allowed** toggle to the right (On).</span></span>

## <a name="allow-cookies-from-business-central"></a><span data-ttu-id="14f54-122">Cookies toestaan vanuit Business Central</span><span class="sxs-lookup"><span data-stu-id="14f54-122">Allow cookies from Business Central</span></span>

<span data-ttu-id="14f54-123">*Probleem:*</span><span class="sxs-lookup"><span data-stu-id="14f54-123">*Problem:*</span></span>

<span data-ttu-id="14f54-124">Als de browser geen cookies toestaat, krijgt u de volgende foutmelding:</span><span class="sxs-lookup"><span data-stu-id="14f54-124">If the browser doesn't allow cookies, you'll get the following error:</span></span>

<span data-ttu-id="14f54-125">**De pagina kon niet worden gevonden. Controleer het adres en probeer het opnieuw.**</span><span class="sxs-lookup"><span data-stu-id="14f54-125">**Sorry, the page could not be found. Please check the address and try again.**</span></span> 

<span data-ttu-id="14f54-126">*Oplossing:*</span><span class="sxs-lookup"><span data-stu-id="14f54-126">*Fix:*</span></span>

1. <span data-ttu-id="14f54-127">Ga in Microsoft Edge naar **Instellingen** > **Cookies en sitetoestemmingen** > **Cookies en sitegegevens**.</span><span class="sxs-lookup"><span data-stu-id="14f54-127">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Cookies and site data**.</span></span>
2. <span data-ttu-id="14f54-128">Verplaats de schakelaar **Sites toestaan cookiegegevens op te slaan en te lezen** naar rechts (Aan).</span><span class="sxs-lookup"><span data-stu-id="14f54-128">Move the **Allow sites to save and read cookie data** toggle to the right (On).</span></span>  

## <a name="allow-pop-ups-from-business-central"></a><a name="popup"></a><span data-ttu-id="14f54-129">Pop-ups toestaan vanuit Business Central</span><span class="sxs-lookup"><span data-stu-id="14f54-129">Allow pop-ups from Business Central</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="14f54-130">integreert met verschillende producten.</span><span class="sxs-lookup"><span data-stu-id="14f54-130">integrates with several products.</span></span> <span data-ttu-id="14f54-131">In sommige gevallen, zoals bij Microsoft Teams, wordt [!INCLUDE[prod_short](includes/prod_short.md)] geopend in een venster binnen het product.</span><span class="sxs-lookup"><span data-stu-id="14f54-131">In some cases, like with Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] opens, or "pop-ups", within the product.</span></span> <span data-ttu-id="14f54-132">Deze mogelijkheid vereist dat uw browser pop-ups toestaat vanuit [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="14f54-132">This capability requires that your browser allows pop-ups from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

<span data-ttu-id="14f54-133">*Probleem:*</span><span class="sxs-lookup"><span data-stu-id="14f54-133">*Problem:*</span></span>

<span data-ttu-id="14f54-134">Als pop-ups voor [!INCLUDE[prod_short](includes/prod_short.md)] worden geblokkeerd, krijgt u een bericht dat lijkt op het volgende bericht:</span><span class="sxs-lookup"><span data-stu-id="14f54-134">If pop-ups for [!INCLUDE[prod_short](includes/prod_short.md)] are being blocked, you get a message similar to the following message:</span></span>

<span data-ttu-id="14f54-135">**Er is iets fout gegaan. Uw browser blokkeert mogelijk pop-ups die Business Central nodig heeft.**</span><span class="sxs-lookup"><span data-stu-id="14f54-135">**Something went wrong. Your browser may be blocking pop-ups needed by Business Central.**</span></span>

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
<span data-ttu-id="14f54-136">*Oplossing:*</span><span class="sxs-lookup"><span data-stu-id="14f54-136">*Fix:*</span></span>

1. <span data-ttu-id="14f54-137">Ga in Microsoft Edge naar **Instellingen** > **Cookies en sitetoestemmingen** > **Pop-ups en omleidingen**.</span><span class="sxs-lookup"><span data-stu-id="14f54-137">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Pop-ups and redirects**.</span></span>
2. <span data-ttu-id="14f54-138">Verplaats de schakelaar **Geblokkeerd** naar rechts (Aan).</span><span class="sxs-lookup"><span data-stu-id="14f54-138">Move the **Blocked** toggle to the right (On).</span></span>
3. <span data-ttu-id="14f54-139">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="14f54-139">Select **Add**.</span></span> <span data-ttu-id="14f54-140">Typ in het vak **Site** `https://businesscentral.dynamics.com` en selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="14f54-140">In the **Site** box, type `https://businesscentral.dynamics.com`, then select **Add**.</span></span>

## <a name="see-also"></a><span data-ttu-id="14f54-141">Zie ook</span><span class="sxs-lookup"><span data-stu-id="14f54-141">See Also</span></span>

[<span data-ttu-id="14f54-142">Problemen met Teams oplossen</span><span class="sxs-lookup"><span data-stu-id="14f54-142">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]