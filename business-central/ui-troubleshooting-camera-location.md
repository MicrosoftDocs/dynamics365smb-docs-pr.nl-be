---
title: 'Problemen oplossen: toegang tot camera en locatie'
description: In dit artikel wordt beschreven hoe u problemen met de toegang tot camera- en locatiegegevens in Business Central oplost.
author: blrobl
ms.author: t-blrobl
ms.date: 04/22/2020
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: dynamics365-business-central
ms.openlocfilehash: befb7af01ba26512a4b62005e81b5a3ff351b02f
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324492"
---
# <a name="troubleshooting-accessing-camera-and-location"></a><span data-ttu-id="6524e-103">Problemen oplossen: toegang tot camera en locatie</span><span class="sxs-lookup"><span data-stu-id="6524e-103">Troubleshooting: Accessing Camera and Location</span></span>

<span data-ttu-id="6524e-104">U kunt enkele problemen tegenkomen wanneer u probeert toegang te krijgen tot de camera en de locatiegegevens van een apparaat [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="6524e-104">You might come across some issues when trying to access the camera and location information of a device from [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="6524e-105">Hieronder vindt u de mogelijke oorzaken van deze problemen en hoe u ze kunt omzeilen.</span><span class="sxs-lookup"><span data-stu-id="6524e-105">You can find the possible causes behind these problems and how to work around them listed below.</span></span>

## <a name="device-must-have-camera-and-location-capabilities"></a><span data-ttu-id="6524e-106">Het apparaat moet camera- en locatiemogelijkheden hebben</span><span class="sxs-lookup"><span data-stu-id="6524e-106">Device must have Camera and Location Capabilities</span></span>

<span data-ttu-id="6524e-107">Om toegang te krijgen tot de camera of de locatie van een gebruiker vanaf een apparaat, moet het apparaat respectievelijk een fysieke camera hebben of de mogelijkheid om locatiegegevens op te halen.</span><span class="sxs-lookup"><span data-stu-id="6524e-107">In order to access the camera or a user's location from a device, the device must have a physical camera or the capability to retrieve location information, respectively.</span></span>

<span data-ttu-id="6524e-108">Als uw apparaat camera- en locatiemogelijkheden heeft, maar u nog steeds problemen ondervindt, is het mogelijk dat sommige stuurprogramma's moeten worden bijgewerkt of opnieuw moeten worden geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="6524e-108">If your device has camera and location capabilities but you still encounter problems, it is possible that some drivers need updating or reinstalling.</span></span> <span data-ttu-id="6524e-109">Zelfs als u het niet zeker weet, raden we u altijd aan om het besturingssysteem, de stuurprogramma's en de browser van uw apparaat bij te werken naar de nieuwste versie voor de beste ervaring.</span><span class="sxs-lookup"><span data-stu-id="6524e-109">Even if you are unsure, we always recommend you update your device operating system, drivers, and browser to the latest version for the best experience.</span></span>

## <a name="access-permissions-not-enabled"></a><span data-ttu-id="6524e-110">Toegangsmachtigingen niet ingeschakeld</span><span class="sxs-lookup"><span data-stu-id="6524e-110">Access Permissions not Enabled</span></span>

<span data-ttu-id="6524e-111">U moet algemene toegang tot de camera en locatie inschakelen vanuit de privacyinstellingen van uw apparaat en u moet daar expliciet toestemming voor geven aan [!INCLUDE[prodshort](includes/prodshort.md)] om er toegang toe te krijgen.</span><span class="sxs-lookup"><span data-stu-id="6524e-111">You must enable general access to camera and location from your device's privacy settings and explicitly give permission to  [!INCLUDE[prodshort](includes/prodshort.md)] to access them.</span></span> <span data-ttu-id="6524e-112">Ga bijvoorbeeld om de machtigingen te zien of te wijzigen voor een apparaat dat op Windows draait naar **Instellingen**, kies **Privacy** en dan **App-machtigingen**.</span><span class="sxs-lookup"><span data-stu-id="6524e-112">For example, to see or change permissions for a device running on Windows, go to **Settings**, choose **Privacy**, and then **App permissions**.</span></span> 

<span data-ttu-id="6524e-113">Voor mobiele apparaten moet u toegangsmachtigingen voor camera en locatie verlenen aan de mobiele [!INCLUDE[prodshort](includes/prodshort.md)]-app.</span><span class="sxs-lookup"><span data-stu-id="6524e-113">For mobile devices, you must give camera and location access permissions to the [!INCLUDE[prodshort](includes/prodshort.md)] Mobile App.</span></span> <span data-ttu-id="6524e-114">Als u dit wilt doen voor een iOS-apparaat, gaat u naar **Instellingen**, kiest u **Privacy** en vervolgens **Camera** of **Locatie**.</span><span class="sxs-lookup"><span data-stu-id="6524e-114">To do so for an iOS device, go to **Settings**, choose **Privacy**, and then **Camera** or **Location**.</span></span> <span data-ttu-id="6524e-115">Ga voor Android-apparaten naar **Instellingen**, kies **Apps en meldingen**, **Geavanceerd**, **Machtigingenbeheer** en vervolgens **Camera** of **Locatie**.</span><span class="sxs-lookup"><span data-stu-id="6524e-115">For Android devices go to **Settings**, choose **Apps & Notifications**, **Advanced**, **Permission Manager**, and then **Camera** or **Location**.</span></span>

<span data-ttu-id="6524e-116">Bovendien, als u [!INCLUDE[prodshort](includes/prodshort.md)] gebruikt in een browser, moet u ook de [!INCLUDE[prodshort](includes/prodshort.md)]-sitemachtiging voor toegang tot de camera of locatiegegevens verlenen.</span><span class="sxs-lookup"><span data-stu-id="6524e-116">In addition, if you are using [!INCLUDE[prodshort](includes/prodshort.md)] in a browser, you must also grant the [!INCLUDE[prodshort](includes/prodshort.md)] site permission to access the camera or location information.</span></span> <span data-ttu-id="6524e-117">Als u de machtigingen van een site in de Microsoft Edge-browser wilt wijzigen, gaat u naar **Instellingen**, kiest u **Sitemachtigingen** en vervolgens **Camera** of **Locatie**.</span><span class="sxs-lookup"><span data-stu-id="6524e-117">To see or change a site's permissions in the Microsoft Edge browser, go to **Settings**, choose **Site Permissions**, and then **Camera** or **Location**.</span></span> <span data-ttu-id="6524e-118">Merk op dat dit voor andere browsers anders kan zijn.</span><span class="sxs-lookup"><span data-stu-id="6524e-118">Note that this might be different for other browsers.</span></span>

<span data-ttu-id="6524e-119">Standaard zal het apparaat of de browser een verzoek openen om toegang te krijgen tot deze mogelijkheden wanneer de gebruiker ze voor de eerste keer activeert.</span><span class="sxs-lookup"><span data-stu-id="6524e-119">By default, the device or browser will pop up a request to access these capabilities when the user activates them for the first time.</span></span>

> [!NOTE]  
> <span data-ttu-id="6524e-120">Sommige oude browsers geven geen toegang tot camera en locatie.</span><span class="sxs-lookup"><span data-stu-id="6524e-120">Some old browsers do not grant access to camera and location.</span></span> <span data-ttu-id="6524e-121">Camera is bijvoorbeeld niet beschikbaar in Internet Explorer of de oudere Edge-browser.</span><span class="sxs-lookup"><span data-stu-id="6524e-121">For example, camera is not available in Internet Explorer or the legacy Edge browser.</span></span>

## <a name="web-client-connection-not-secure"></a><span data-ttu-id="6524e-122">Webclient-verbinding niet veilig</span><span class="sxs-lookup"><span data-stu-id="6524e-122">Web Client Connection not Secure</span></span>

<span data-ttu-id="6524e-123">De camera- en locatiemogelijkheden zijn alleen beschikbaar bij toegang tot de webclient via SSL-beveiligde HTTP-verbindingen, met behulp van het `https://` URI-schema.</span><span class="sxs-lookup"><span data-stu-id="6524e-123">The camera and location capabilities are only available when accessing the Web Client through SSL secured HTTP connections, using the `https://` URI scheme.</span></span> 

<span data-ttu-id="6524e-124">De enige uitzondering is verbinding maken met `http://localhost`, gebruikt voor ontwikkelings- en testdoeleinden.</span><span class="sxs-lookup"><span data-stu-id="6524e-124">The only exception is connecting to `http://localhost`, used for development and test purposes.</span></span>


## <a name="working-with-virtualization-technologies"></a><span data-ttu-id="6524e-125">Werken met virtualisatietechnologieën</span><span class="sxs-lookup"><span data-stu-id="6524e-125">Working with Virtualization Technologies</span></span>

<span data-ttu-id="6524e-126">Bij het verbinden met [!INCLUDE[prodshort](includes/prodshort.md)] via Remote Desktop of andere virtualisatie is de toegang tot camera of locatie mogelijk niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="6524e-126">When connecting to [!INCLUDE[prodshort](includes/prodshort.md)] through Remote Desktop or another virtualization, the access to camera or location might not be available.</span></span> <span data-ttu-id="6524e-127">Als dit het geval is, gebruik dan het fysieke systeem.</span><span class="sxs-lookup"><span data-stu-id="6524e-127">If this is the case, use the physical system instead.</span></span>

## <a name="antivirus-software"></a><span data-ttu-id="6524e-128">Antivirussoftware</span><span class="sxs-lookup"><span data-stu-id="6524e-128">Antivirus Software</span></span>
<span data-ttu-id="6524e-129">Sommige antivirussoftware blokkeert standaard de toegang tot de camera en de locatie.</span><span class="sxs-lookup"><span data-stu-id="6524e-129">Some antivirus software block access to camera and location by default.</span></span> <span data-ttu-id="6524e-130">Vergeet niet om uw antivirussoftware-instellingen te controleren.</span><span class="sxs-lookup"><span data-stu-id="6524e-130">Remember to check your antivirus software settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="6524e-131">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6524e-131">See Also</span></span>
[<span data-ttu-id="6524e-132">De camera implementeren in AL</span><span class="sxs-lookup"><span data-stu-id="6524e-132">Implementing the Camera in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[<span data-ttu-id="6524e-133">De locatie implementeren in AL</span><span class="sxs-lookup"><span data-stu-id="6524e-133">Implementing the Location in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)
