---
title: Opgeslagen instellingen wijzigen en toepassen | Microsoft Docs
description: Beschrijft het gebruik van vooraf gedefinieerde opties en filters om een lijst aan te passen en de juiste gegevens te genereren.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 3e7b00d54a9c655a77b7b7f4854e59993866427e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251246"
---
# <a name="managing-saved-settings-on-reports"></a><span data-ttu-id="c5bc2-103">Opgeslagen instellingen in rapporten beheren</span><span class="sxs-lookup"><span data-stu-id="c5bc2-103">Managing Saved Settings on Reports</span></span>
<span data-ttu-id="c5bc2-104">Wanneer gebruikers rapporten uitvoeren, zien ze meestal een pagina waarmee ze bepaalde opties en filters kunnen instellen om de gegevens te wijzigen die in het gegenereerde rapport worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-104">When running a reports, users are typically presented with a page that lets them set certain options and filters for changing the data that is included in the generated report.</span></span> <span data-ttu-id="c5bc2-105">Deze pagina wordt de rapportaanvraagpagina genoemd.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-105">This page is called the report request page.</span></span> <span data-ttu-id="c5bc2-106">Een rapport kan een of meer *opgeslagen instellingen* bevatten die gebruikers op het rapport kunnen toepassen vanaf de aanvraagpagina.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-106">A report can include one or more *saved settings* that users can apply to the report from the request page.</span></span> <span data-ttu-id="c5bc2-107">*Opgeslagen instellingen* zijn in wezen vooraf gedefinieerde opties en filters.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="c5bc2-108">Met behulp van opgeslagen instellingen kunt u snel en betrouwbaar rapporten genereren die de juiste gegevens bevatten.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span> <span data-ttu-id="c5bc2-109">Voor meer informatie over hoe opgeslagen instellingen worden gebruikt, raadpleegt u [Opgeslagen instellingen gebruiken](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="c5bc2-109">For more information about how saved settings are used, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

<span data-ttu-id="c5bc2-110">Als u de juiste machtigingen hebt, kunt u de opgeslagen instellingen voor alle gebruikers in een bedrijf weergeven, maken en wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-110">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in company.</span></span> <span data-ttu-id="c5bc2-111">U kunt opgeslagen instellingen voor een rapport toewijzen aan afzonderlijke gebruikers of aan alle gebruikers in het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-111">You can assign saved settings for a report to individual users or all users in the company.</span></span>

<!--
## Apply saved settings to a report
1. Open the report.

   The report request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="create-and-modify-saved-settings-for-all-users"></a><span data-ttu-id="c5bc2-112">Opgeslagen instellingen maken en wijzigen voor alle gebruikers</span><span class="sxs-lookup"><span data-stu-id="c5bc2-112">Create and modify saved settings for all users</span></span>
<span data-ttu-id="c5bc2-113">U beheert opgeslagen instellingen vanaf pagina 1560 **Rapportinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-113">You manage saved settings from page **1560 Reports Settings**.</span></span> <span data-ttu-id="c5bc2-114">Er zijn twee manieren om deze pagina te openen:</span><span class="sxs-lookup"><span data-stu-id="c5bc2-114">There are two ways to open this page:</span></span>
-   <span data-ttu-id="c5bc2-115">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rapportinstellingen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Settings**, and then choose the related link.</span></span>
-   <span data-ttu-id="c5bc2-116">Open een rapport, kies de opzoekactie naast het vak **Standaardwaarden gebruiken uit**, kies **Selecteren vanuit volledige lijst**.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-116">Open a report, choose the lookup next to the **Used default values from:** box, choose **Select from full list**.</span></span>

<span data-ttu-id="c5bc2-117">De pagina bevat alle bestaande opgeslagen instellingsvermeldingen voor alle gebruikers.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-117">The page displays all the existing save settings entries for all users.</span></span> <span data-ttu-id="c5bc2-118">Als er een gebruikersnaam in de kolom **Toegewezen aan** staat, kan alleen deze gebruiker de opgeslagen instellingen voor het corresponderende rapport gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-118">If there is a user name in the **Assigned to** column, only that user can use the saved settings for the associated report.</span></span> <span data-ttu-id="c5bc2-119">Als er een selectievakje in de kolom **Gedeeld met alle gebruikers** staat, kunnen alle gebruikers de opgeslagen instellingen voor het rapport gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-119">If there is a check mark in the **Share with all users** column, all users can use the saved settings for the report.</span></span>

<span data-ttu-id="c5bc2-120">Vanaf de pagina **Rapportinstellingen** kunt u het volgende doen:</span><span class="sxs-lookup"><span data-stu-id="c5bc2-120">From the **Report Settings** page, you can:</span></span>
-   <span data-ttu-id="c5bc2-121">**Nieuw** kiezen om een geheel nieuwe vermelding met opgeslagen instellingen te maken.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-121">Choose **New** to create a new saved settings entry from scratch.</span></span>
-   <span data-ttu-id="c5bc2-122">Een vermelding met opgeslagen instellingen selecteren en **Kopiëren** kiezen om een kopie te maken.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-122">Select a saved settings entry from the list, and choose **Copy** to create a copy.</span></span>
-   <span data-ttu-id="c5bc2-123">Een vermelding met opgeslagen instellingen in de lijst selecteren en **Bewerken** kiezen om een vermelding met opgeslagen instellingen te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-123">Select a saved settings entry from the list, and choose **Edit** to modify a saved settings entry.</span></span>


> [!Important]
> <span data-ttu-id="c5bc2-124">Denk na over de naam die u een vermelding met opgeslagen instellingen geeft.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-124">Consider the name that you give a saved settings entry.</span></span> <span data-ttu-id="c5bc2-125">Als u een vermelding met opgeslagen instellingen voor alle gebruikers maakt en deze dezelfde naam geeft als een bestaande vermelding met opgeslagen instellingen die aan één specifieke gebruiker is toegewezen, kan die gebruiker de vermelding met opgeslagen instellingen die aan iedereen is toegewezen, niet gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-125">If you create a saved settings entry for all users, and you give it the same name as an existing saved settings entry that is assigned to a specific user only, then that user will not be able to use the saved settings entry that is assigned to everyone.</span></span>  <span data-ttu-id="c5bc2-126">Onder **Opgeslagen instellingen** op de rapportaanvraagpagina ziet de gebruiker twee vermeldingen met opgeslagen instellingen met dezelfde naam.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-126">Under **Saved Settings** on the report request page, the user will see two saved settings entries with the same name.</span></span> <span data-ttu-id="c5bc2-127">Ongeacht welke optie de gebruiker echter kiest, de gebruikersspecifieke vermelding met opgeslagen instellingen wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-127">However, no matter which option he chooses, the user-specific saved settings entry will be used.</span></span>

> [!NOTE]
> <span data-ttu-id="c5bc2-128">De functie voor opgeslagen instellingen is alleen beschikbaar voor rapporten waarvoor de [eigenschap SaveValues](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) van de rapportaanvraagpagina is ingesteld op `Yes`.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-128">The saved settings feature is available only on reports where the [SaveValues property](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) of the report's request page is set to `Yes`.</span></span> <span data-ttu-id="c5bc2-129">De eigenschap **SaveValues** wordt ingesteld in de ontwikkelomgeving.</span><span class="sxs-lookup"><span data-stu-id="c5bc2-129">The **SaveValues** property is set in the development environment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c5bc2-130">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c5bc2-130">See Also</span></span>
[<span data-ttu-id="c5bc2-131">Werken met rapporten en batchverwerkingen</span><span class="sxs-lookup"><span data-stu-id="c5bc2-131">Working with Reports and Batch Jobs</span></span>](ui-work-report.md)  
