---
title: Power BI-integratieonderdeel en architectuuroverzicht voor Business Central | Microsoft Docs
description: U kunt eenvoudig inzichten verwerven, bedrijfsinformatie genereren en KPI's vaststellen op basis van uw Business Central-gegevens met de Business Central-apps voor Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: d6c01d95dfaebe6682c4c5e20bc85bdebb0c9b54
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377935"
---
# <a name="power-bi-integration-component-and-architecture-overview-for-prod_short"></a><span data-ttu-id="63b14-103">Power BI-integratieonderdeel en architectuuroverzicht voor [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="63b14-103">Power BI Integration Component and Architecture Overview for [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>

<span data-ttu-id="63b14-104">In dit artikel komt u meer te weten over de verschillende aspecten van de Power BI-integratie met [!INCLUDE[prod_short](includes/prod_short.md)], wat u kan helpen bij de implementatie en het gebruik ervan.</span><span class="sxs-lookup"><span data-stu-id="63b14-104">In this article, you'll learn about the different aspects of Power BI integration with [!INCLUDE[prod_short](includes/prod_short.md)] to help you understand its implementation and use.</span></span>

## <a name="components"></a><span data-ttu-id="63b14-105">Onderdelen</span><span class="sxs-lookup"><span data-stu-id="63b14-105">Components</span></span>

<span data-ttu-id="63b14-106">In de volgende tabel worden de belangrijkste onderdelen beschreven die betrokken zijn bij de Power BI-integratie.</span><span class="sxs-lookup"><span data-stu-id="63b14-106">The following table describes the major components involved with Power BI integration.</span></span>

|<span data-ttu-id="63b14-107">Onderdeel</span><span class="sxs-lookup"><span data-stu-id="63b14-107">Component</span></span>|<span data-ttu-id="63b14-108">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="63b14-108">Description</span></span>|
|---------|-----------|
|<span data-ttu-id="63b14-109">Power BI</span><span class="sxs-lookup"><span data-stu-id="63b14-109">Power BI</span></span>|<span data-ttu-id="63b14-110">Een cloudservice voor het hosten en beheren van rapporten.</span><span class="sxs-lookup"><span data-stu-id="63b14-110">A cloud-based report hosting and management service.</span></span>|
|<span data-ttu-id="63b14-111">Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="63b14-111">Power BI Desktop</span></span>|<span data-ttu-id="63b14-112">Een bewerkingsprogramma waarmee u rapporten en dashboards kunt maken en waarmee u ook rapporten kunt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="63b14-112">An authoring tool for building reports and dashboards, and allows you to run reports.</span></span> <span data-ttu-id="63b14-113">Het programma is beschikbaar als gratis download in de Microsoft Store en wordt lokaal geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="63b14-113">It's available as a free download on Microsoft Store and is installed locally.</span></span>|
|[!INCLUDE[prod_short](includes/prod_short.md)]|<span data-ttu-id="63b14-114">Online- of on-premises oplossing met connectors die beschikbaar zijn voor Power BI en de mogelijkheid om een Power BI-gedeelte in te sluiten.</span><span class="sxs-lookup"><span data-stu-id="63b14-114">Online or on-premises solution with connectors exposed to Power BI and the ability to embed a Power BI part.</span></span>|

## <a name="whats-available-from-the-start"></a><span data-ttu-id="63b14-115">Wat er vanaf het begin beschikbaar is</span><span class="sxs-lookup"><span data-stu-id="63b14-115">What's available from the start</span></span>

<span data-ttu-id="63b14-116">In de volgende tabel worden de beschikbare functies beschreven.</span><span class="sxs-lookup"><span data-stu-id="63b14-116">The following table describes available features.</span></span>

|<span data-ttu-id="63b14-117">Functie</span><span class="sxs-lookup"><span data-stu-id="63b14-117">Feature</span></span>|<span data-ttu-id="63b14-118">Ondersteuning voor [!INCLUDE[prod_short](includes/prod_short.md)] online of on-premises</span><span class="sxs-lookup"><span data-stu-id="63b14-118">[!INCLUDE[prod_short](includes/prod_short.md)] online or on-premises support</span></span>|
|-------|---------------------|
|<span data-ttu-id="63b14-119">Power BI-connectors</span><span class="sxs-lookup"><span data-stu-id="63b14-119">Power BI connectors</span></span>|<span data-ttu-id="63b14-120">Beide.</span><span class="sxs-lookup"><span data-stu-id="63b14-120">Both.</span></span> <span data-ttu-id="63b14-121">Verschillende connectors voor online en on-premises.</span><span class="sxs-lookup"><span data-stu-id="63b14-121">Different connectors for online and on-premises.</span></span> <span data-ttu-id="63b14-122">Dezelfde connector wordt gebruikt voor Power BI Desktop en de Power BI-service</span><span class="sxs-lookup"><span data-stu-id="63b14-122">Same connector used for Power BI Desktop and Power BI Service</span></span> |
|<span data-ttu-id="63b14-123">Ingesloten gedeelte voor het weergeven van een bepaald rapport in een feitenblok in [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="63b14-123">Embedded experience for viewing a given report inside a FactBox in [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>|<span data-ttu-id="63b14-124">Beide.</span><span class="sxs-lookup"><span data-stu-id="63b14-124">Both.</span></span> <span data-ttu-id="63b14-125">Vereist configuratie om rapporten weer te geven voor on-premises.</span><span class="sxs-lookup"><span data-stu-id="63b14-125">Requires configuration to display reports for on-premises.</span></span>|
|<span data-ttu-id="63b14-126">Power BI-rapportbeheer vanuit [!INCLUDE[prod_short](includes/prod_short.md)]</span><span class="sxs-lookup"><span data-stu-id="63b14-126">Power BI report management from [!INCLUDE[prod_short](includes/prod_short.md)]</span></span>|<span data-ttu-id="63b14-127">Online</span><span class="sxs-lookup"><span data-stu-id="63b14-127">Online</span></span>|
|<span data-ttu-id="63b14-128">Standaard Power BI-rapporten in rolcentra die zijn geïmplementeerd in Power BI</span><span class="sxs-lookup"><span data-stu-id="63b14-128">Default Power BI reports on role centers deployed to Power BI</span></span>|<span data-ttu-id="63b14-129">Online</span><span class="sxs-lookup"><span data-stu-id="63b14-129">Online</span></span>|
|<span data-ttu-id="63b14-130">Power BI-apps in Microsoft AppSource</span><span class="sxs-lookup"><span data-stu-id="63b14-130">Power BI Apps on Microsoft AppSource</span></span>|<span data-ttu-id="63b14-131">Online.</span><span class="sxs-lookup"><span data-stu-id="63b14-131">Online.</span></span>|

## <a name="architecture"></a><span data-ttu-id="63b14-132">Architectuur</span><span class="sxs-lookup"><span data-stu-id="63b14-132">Architecture</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="63b14-133">kan worden geïntegreerd met Power BI via een connector die OData gebruikt.</span><span class="sxs-lookup"><span data-stu-id="63b14-133">integrates with Power BI through a connector using OData.</span></span> <span data-ttu-id="63b14-134">De gegevensbron voor Power BI-rapporten wordt beschikbaar gemaakt in de vorm van OData-webservices.</span><span class="sxs-lookup"><span data-stu-id="63b14-134">The data source for Power BI reports is exposed as OData web services.</span></span>

![Power BI-architectuur voor integratie met Business Central](./media/power-bi-architecture.png)

## <a name="general-flow"></a><span data-ttu-id="63b14-136">Algemene stroom</span><span class="sxs-lookup"><span data-stu-id="63b14-136">General Flow</span></span>

<span data-ttu-id="63b14-137">In het volgende diagram wordt de basiswerkstroom voor gebruikers getoond wanneer ze [!INCLUDE[prod_short](includes/prod_short.md)] verbinden met Power BI.</span><span class="sxs-lookup"><span data-stu-id="63b14-137">The following diagram illustrates the basic workflow for users when connecting [!INCLUDE[prod_short](includes/prod_short.md)] to Power BI.</span></span>

![Power BI-werkstroom voor integratie met Business Central](./media/power-bi-flow.png)

1. <span data-ttu-id="63b14-139">Gebruiker meldt zich aan voor een Power BI-account.</span><span class="sxs-lookup"><span data-stu-id="63b14-139">User signs up for a Power BI account.</span></span>
2. <span data-ttu-id="63b14-140">Gebruiker maakt verbinding met Power BI vanuit [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="63b14-140">User connects to Power BI from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>
3. [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="63b14-141">verifieert de licentie.</span><span class="sxs-lookup"><span data-stu-id="63b14-141">verifies the license.</span></span>
4. [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="63b14-142">implementeert standaardrapporten in de Power BI-service.</span><span class="sxs-lookup"><span data-stu-id="63b14-142">deploys default reports to the Power BI service.</span></span> <span data-ttu-id="63b14-143">Deze stap vindt alleen plaats voor [!INCLUDE[prod_short](includes/prod_short.md)] online.</span><span class="sxs-lookup"><span data-stu-id="63b14-143">This step only happens for [!INCLUDE[prod_short](includes/prod_short.md)] online.</span></span>
5. [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="63b14-144">maakt rapporten in Power BI beschikbaar voor selectie in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="63b14-144">makes reports in Power BI available for selection in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="63b14-145">Standaardrapporten worden automatisch weergegeven in Power BI-gedeeltes.</span><span class="sxs-lookup"><span data-stu-id="63b14-145">Default reports are automatically displayed in Power BI parts.</span></span>
6. <span data-ttu-id="63b14-146">Gebruiker maakt een rapport aan in Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="63b14-146">User creates a report in Power BI Desktop.</span></span>
7. <span data-ttu-id="63b14-147">Gebruiker publiceert het rapport naar de Power BI-service.</span><span class="sxs-lookup"><span data-stu-id="63b14-147">User publishes the report to the Power BI service.</span></span> <span data-ttu-id="63b14-148">De rapporten zijn vervolgens beschikbaar voor selectie in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="63b14-148">The reports are then available for selection in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="63b14-149">Zie Gerelateerde training op [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="63b14-149">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="63b14-150">Zie ook</span><span class="sxs-lookup"><span data-stu-id="63b14-150">See Also</span></span>

[<span data-ttu-id="63b14-151">Business Central en Power BI</span><span class="sxs-lookup"><span data-stu-id="63b14-151">Business Central and Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="63b14-152">Power BI voor consumenten</span><span class="sxs-lookup"><span data-stu-id="63b14-152">Power BI for consumers</span></span>](/power-bi/consumer/end-user-consumer)  
[<span data-ttu-id="63b14-153">De 'nieuwe look' van de Power BI-service</span><span class="sxs-lookup"><span data-stu-id="63b14-153">The 'new look' of the Power BI service</span></span>](/power-bi/service-new-look)  
[<span data-ttu-id="63b14-154">Snelle start: verbinding maken met uw gegevens in Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="63b14-154">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
[<span data-ttu-id="63b14-155">Power BI-documentatie</span><span class="sxs-lookup"><span data-stu-id="63b14-155">Power BI documentation</span></span>](/power-bi/)  
[<span data-ttu-id="63b14-156">Bedrijfsinformatie</span><span class="sxs-lookup"><span data-stu-id="63b14-156">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="63b14-157">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="63b14-157">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="63b14-158">Bedrijfsgegevens importeren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="63b14-158">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="63b14-159">[Instellen van [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="63b14-159">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
<span data-ttu-id="63b14-160">[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken als Power BI-gegevensbron](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="63b14-160">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md)</span></span>  
<span data-ttu-id="63b14-161">[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken als Power Apps-gegevensbron](across-how-use-financials-data-source-powerapps.md)</span><span class="sxs-lookup"><span data-stu-id="63b14-161">[Using [!INCLUDE[prod_short](includes/prod_short.md)] as a Power Apps Data Source](across-how-use-financials-data-source-powerapps.md)</span></span>  
<span data-ttu-id="63b14-162">[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken in Power Automate](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="63b14-162">[Using [!INCLUDE[prod_short](includes/prod_short.md)] in Power Automate](across-how-use-financials-data-source-flow.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]