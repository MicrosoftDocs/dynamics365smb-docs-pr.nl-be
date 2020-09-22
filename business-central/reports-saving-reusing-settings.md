---
title: Opgeslagen instellingen wijzigen en toepassen | Microsoft Docs
description: Beschrijft het gebruik van vooraf gedefinieerde opties en filters om een lijst aan te passen en de juiste gegevens te genereren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: d61e599b9e86f28de6edcf4ccff5b245503880fe
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784621"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a><span data-ttu-id="8e283-103">Opgeslagen instellingen beheren voor rapporten en batchtaken</span><span class="sxs-lookup"><span data-stu-id="8e283-103">Manage Saved Settings for Reports and Batch jobs</span></span>
<span data-ttu-id="8e283-104">Wanneer gebruikers rapporten uitvoeren, zien ze meestal een pagina waarmee ze opties kunnen selecteren en filters kunnen instellen om de gegevens te wijzigen die in het gegenereerde rapport worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="8e283-104">When running reports, users are typically presented with a page that lets them select options and set filters to change the data that is included in the generated report.</span></span> <span data-ttu-id="8e283-105">Deze pagina wordt de aanvraagpagina genoemd.</span><span class="sxs-lookup"><span data-stu-id="8e283-105">This page is called the request page.</span></span> <span data-ttu-id="8e283-106">Een rapport kan een of meer *opgeslagen instellingen* bevatten die gebruikers op het rapport kunnen toepassen vanaf de aanvraagpagina.</span><span class="sxs-lookup"><span data-stu-id="8e283-106">A report can include one or more *saved settings* that users can apply to the report from the request page.</span></span> <span data-ttu-id="8e283-107">*Opgeslagen instellingen* zijn in wezen vooraf gedefinieerde opties en filters.</span><span class="sxs-lookup"><span data-stu-id="8e283-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="8e283-108">Met behulp van opgeslagen instellingen kunt u snel en betrouwbaar rapporten genereren die de juiste gegevens bevatten.</span><span class="sxs-lookup"><span data-stu-id="8e283-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span> <span data-ttu-id="8e283-109">Zie voor meer informatie [Opgeslagen instellingen gebruiken](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="8e283-109">For more information, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

> [!NOTE]
> <span data-ttu-id="8e283-110">Dit onderwerp verwijst hoofdzakelijk naar 'rapport', maar soortgelijke informatie geldt voor batchverwerkingen.</span><span class="sxs-lookup"><span data-stu-id="8e283-110">This topic refers mainly to "report", but similar information applies to batch jobs.</span></span>

<span data-ttu-id="8e283-111">Als u de juiste machtigingen hebt, kunt u de opgeslagen instellingen voor alle gebruikers in een bedrijf weergeven, maken en wijzigen.</span><span class="sxs-lookup"><span data-stu-id="8e283-111">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in a company.</span></span> <span data-ttu-id="8e283-112">U kunt opgeslagen instellingen voor een rapport toewijzen aan afzonderlijke gebruikers of aan alle gebruikers in het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="8e283-112">You can assign saved settings for a report to individual users or to all users in the company.</span></span>

<!--
## Apply saved settings to a report
1. Open the report.

   The request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="to-create-and-modify-saved-settings-for-all-users"></a><span data-ttu-id="8e283-113">Opgeslagen instellingen maken en wijzigen voor alle gebruikers</span><span class="sxs-lookup"><span data-stu-id="8e283-113">To create and modify saved settings for all users</span></span>
<span data-ttu-id="8e283-114">U beheert opgeslagen instellingen op de pagina **Rapportinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="8e283-114">You manage saved settings on the **Reports Settings** page.</span></span> <span data-ttu-id="8e283-115">Er zijn twee manieren om deze pagina te openen:</span><span class="sxs-lookup"><span data-stu-id="8e283-115">There are two ways to open this page:</span></span>
-   <span data-ttu-id="8e283-116">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rapportinstellingen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="8e283-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Settings**, and then choose the related link.</span></span>
-   <span data-ttu-id="8e283-117">Open een rapport, kies de opzoekactie in het veld **Standaardwaarden gebruiken uit** en kies vervolgens de actie **Selecteren vanuit volledige lijst**.</span><span class="sxs-lookup"><span data-stu-id="8e283-117">Open a report, choose the lookup in the **Use default values from** field, and then choose the **Select from full list** action.</span></span>

<span data-ttu-id="8e283-118">De pagina bevat alle bestaande opgeslagen instellingsvermeldingen voor alle gebruikers.</span><span class="sxs-lookup"><span data-stu-id="8e283-118">The page displays all the existing saved settings entries for all users.</span></span> <span data-ttu-id="8e283-119">Als er een gebruikersnaam in het veld **Toegewezen aan** staat, kan alleen deze gebruiker de opgeslagen instellingen voor het corresponderende rapport gebruiken.</span><span class="sxs-lookup"><span data-stu-id="8e283-119">If there is a user name in the **Assigned to** field, only that user can use the saved settings for the associated report.</span></span> <span data-ttu-id="8e283-120">Als er een vinkje in het veld **Gedeeld met alle gebruikers** staat, kunnen alle gebruikers de opgeslagen instellingen voor het rapport gebruiken.</span><span class="sxs-lookup"><span data-stu-id="8e283-120">If there is a check mark in the **Share with all users** field, all users can use the saved settings for the report.</span></span>

<span data-ttu-id="8e283-121">Vanaf de pagina **Rapportinstellingen** kunt u het volgende doen:</span><span class="sxs-lookup"><span data-stu-id="8e283-121">From the **Report Settings** page, you can:</span></span>
-   <span data-ttu-id="8e283-122">Kies de actie **Nieuw** om een nieuwe vermelding met opgeslagen instellingen te maken.</span><span class="sxs-lookup"><span data-stu-id="8e283-122">Choose the **New** action to create a new saved settings entry from scratch.</span></span>
-   <span data-ttu-id="8e283-123">Selecteer een vermelding met opgeslagen instellingen en kies de actie **Kopiëren** om een kopie te maken.</span><span class="sxs-lookup"><span data-stu-id="8e283-123">Select a saved settings entry from the list, and choose the **Copy** action to create a copy.</span></span>
-   <span data-ttu-id="8e283-124">Selecteer een vermelding met opgeslagen instellingen in de lijst en kies de actie **Bewerken** om een vermelding met opgeslagen instellingen te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="8e283-124">Select a saved settings entry from the list, and choose the **Edit** action to modify a saved settings entry.</span></span>

> [!Important]
> <span data-ttu-id="8e283-125">Denk na over de naam die u een vermelding met opgeslagen instellingen geeft.</span><span class="sxs-lookup"><span data-stu-id="8e283-125">Consider the name that you give a saved settings entry.</span></span> <span data-ttu-id="8e283-126">Als u een vermelding met opgeslagen instellingen voor alle gebruikers maakt en deze dezelfde naam geeft als een bestaande vermelding met opgeslagen instellingen die aan één specifieke gebruiker is toegewezen, kan die gebruiker de vermelding met opgeslagen instellingen die aan iedereen is toegewezen, niet gebruiken.</span><span class="sxs-lookup"><span data-stu-id="8e283-126">If you create a saved settings entry for all users, and you give it the same name as an existing saved settings entry that is assigned to a specific user only, then that user will not be able to use the saved settings entry that is assigned to everyone.</span></span>  <span data-ttu-id="8e283-127">In de sectie **Opgeslagen instellingen** op de aanvraagpagina ziet de gebruiker twee vermeldingen met opgeslagen instellingen met dezelfde naam.</span><span class="sxs-lookup"><span data-stu-id="8e283-127">In the **Saved Settings** section on the request page, the user will see two saved settings entries with the same name.</span></span> <span data-ttu-id="8e283-128">Ongeacht welke optie de gebruiker echter kiest, de gebruikersspecifieke vermelding met opgeslagen instellingen wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8e283-128">However, no matter which option they choose, the user-specific saved settings entry will be used.</span></span>

> [!NOTE]
> <span data-ttu-id="8e283-129">De functie voor opgeslagen instellingen is alleen beschikbaar voor rapporten waarvoor de [eigenschap SaveValues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) van de rapportaanvraagpagina is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8e283-129">The Saved Settings feature is available only on reports where the [SaveValues property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) of the report's request page is set to **Yes**.</span></span> <span data-ttu-id="8e283-130">De eigenschap **SaveValues** wordt ingesteld in de ontwikkelomgeving.</span><span class="sxs-lookup"><span data-stu-id="8e283-130">The **SaveValues** property is set in the development environment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8e283-131">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8e283-131">See Also</span></span>
[<span data-ttu-id="8e283-132">Werken met rapporten, batchverwerkingen en XMLports</span><span class="sxs-lookup"><span data-stu-id="8e283-132">Working with Reports, Batch Jobs, and XMLports</span></span>](ui-work-report.md)  
