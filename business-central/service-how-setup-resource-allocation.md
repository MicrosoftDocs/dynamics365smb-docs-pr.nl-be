---
title: Resourcetoewijzing instellen | Microsoft Docs
description: Leer hoe u er met het systeem voor kunt zorgen dat u iemand toewijst die over de vereiste vaardigheden beschikt om een service te bieden.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resource, skill, service, zones
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 7b7a01bc61d55379cd12563d1f31f331c3b4fd74
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "932493"
---
# <a name="set-up-resource-allocation"></a><span data-ttu-id="bc8b6-103">Resourcetoewijzing instellen</span><span class="sxs-lookup"><span data-stu-id="bc8b6-103">Set Up Resource Allocation</span></span>
<span data-ttu-id="bc8b6-104">Om ervoor te zorgen dat een servicetaak goed wordt uitgevoerd, is het belangrijk een resource te vinden die gekwalificeerd is om het werk uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-104">To ensure that a service task is performed well, it's important to find a resource who is qualified to do the work.</span></span> <span data-ttu-id="bc8b6-105">U kunt [!INCLUDE[d365fin](includes/d365fin_md.md)] zo instellen dat het eenvoudig is om iemand toe te wijzen die over de juiste bekwaamheden voor het project beschikt.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-105">You can set up [!INCLUDE[d365fin](includes/d365fin_md.md)] so that it's easy to allocate someone who has the right skills for the job.</span></span> <span data-ttu-id="bc8b6-106">In [!INCLUDE[d365fin](includes/d365fin_md.md)] noemen we dit _resourcetoewijzing_.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-106">In [!INCLUDE[d365fin](includes/d365fin_md.md)], we call this _resource allocation_.</span></span> <span data-ttu-id="bc8b6-107">U kunt resources toewijzen op basis van hun vaardigheden, beschikbaarheid en locatie (of ze zich in dezelfde serviceregio als de klant bevinden).</span><span class="sxs-lookup"><span data-stu-id="bc8b6-107">You can allocate resources based on their skill, availability, or whether they are in the same service zone as the customer.</span></span> 

<span data-ttu-id="bc8b6-108">U moet het volgende instellen om resourcetoewijzing te gebruiken:</span><span class="sxs-lookup"><span data-stu-id="bc8b6-108">To use resource allocation, you must set up:</span></span>  
  
* <span data-ttu-id="bc8b6-109">De benodigde bekwaamheden om serviceartikelen te repareren en te onderhouden.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-109">The skills required to repair and maintain service items.</span></span> <span data-ttu-id="bc8b6-110">U wijst deze toe aan serviceartikelen en resources.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-110">You assign these to service items and resources.</span></span>  
* <span data-ttu-id="bc8b6-111">Geografische gebieden, regio's, die u voor de markt definieert.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-111">Geographic regions, called zones, that you define for your market.</span></span> <span data-ttu-id="bc8b6-112">Dit kunnen bijvoorbeeld Oost, West, Centraal, enzovoort zijn.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-112">For example, East, West, Central, and so on.</span></span> <span data-ttu-id="bc8b6-113">U wijst deze toe aan klanten en resources.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-113">You assign these to customers and resources.</span></span>  
* <span data-ttu-id="bc8b6-114">Of er resourcebekwaamheden en -regio's moeten worden weergegeven en of er een waarschuwing moet worden weergegeven als iemand een ongeschikte resource kiest of een resource die zich niet in de klantregio bevindt.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-114">Whether to display resource skills and zones, and whether to display a warning if someone chooses unqualified resource, or a resource that is not in the customer zone.</span></span>  

## <a name="to-set-up-skills"></a><span data-ttu-id="bc8b6-115">Bekwaamheden instellen</span><span class="sxs-lookup"><span data-stu-id="bc8b6-115">To set up skills</span></span>
1. <span data-ttu-id="bc8b6-116">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bekwaamheden** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Skills**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bc8b6-117">Vul de benodigde velden in.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a><span data-ttu-id="bc8b6-118">Bekwaamheden toewijzen aan serviceartikelen en resources</span><span class="sxs-lookup"><span data-stu-id="bc8b6-118">To assign skills to service items and resources</span></span>
1. <span data-ttu-id="bc8b6-119">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Serviceartikelen** of **Resources** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Items** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bc8b6-120">Open de kaart voor het serviceartikel of de resource en kies een van de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="bc8b6-120">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="bc8b6-121">Voor serviceartikelen kiest u **Resourcebekwaamheden**.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-121">For service items, choose **Resource Skills**.</span></span>  
    * <span data-ttu-id="bc8b6-122">Voor resources kiest u **Bekwaamheden**.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-122">For resources, choose **Skills**.</span></span>  

## <a name="to-set-up-zones"></a><span data-ttu-id="bc8b6-123">Regio's instellen</span><span class="sxs-lookup"><span data-stu-id="bc8b6-123">To set up zones</span></span>
1. <span data-ttu-id="bc8b6-124">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Zones** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Zones**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bc8b6-125">Vul de benodigde velden in.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a><span data-ttu-id="bc8b6-126">Regio's toewijzen aan klanten en resources</span><span class="sxs-lookup"><span data-stu-id="bc8b6-126">To assign zones to customers and resources</span></span> 
1. <span data-ttu-id="bc8b6-127">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** of **Resources** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bc8b6-128">Open de kaart voor het serviceartikel of de resource en kies een van de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="bc8b6-128">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="bc8b6-129">Voor klanten kiest u een regio in het veld **Serviceregiocode**.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-129">For customers, choose a zone in the **Service Zone Code** field.</span></span>  
    * <span data-ttu-id="bc8b6-130">Voor resources kiest u de actie **Serviceregio's**.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-130">For resources, choose the **Service Zones** action.</span></span>  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a><span data-ttu-id="bc8b6-131">Opgeven wat er moet worden weergegeven wanneer een resource is gekozen</span><span class="sxs-lookup"><span data-stu-id="bc8b6-131">To specify what to show when a resource is chosen</span></span>
1. <span data-ttu-id="bc8b6-132">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Service-instellingen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Setup**, and then choose the related link.</span></span> 
2. <span data-ttu-id="bc8b6-133">Kies in het veld **Optie resourcebekwaamheden** een van de opties die in de volgende tabel worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-133">In the **Resource Skills Option** field, choose one of the options described in the following table.</span></span>  
  
    |<span data-ttu-id="bc8b6-134">**Optie**</span><span class="sxs-lookup"><span data-stu-id="bc8b6-134">**Option**</span></span>|<span data-ttu-id="bc8b6-135">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="bc8b6-135">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="bc8b6-136">Code getoond</span><span class="sxs-lookup"><span data-stu-id="bc8b6-136">Code Shown</span></span> | <span data-ttu-id="bc8b6-137">Alleen de code wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-137">Displays the code only.</span></span>|  
    |<span data-ttu-id="bc8b6-138">Waarschuwing getoond</span><span class="sxs-lookup"><span data-stu-id="bc8b6-138">Warning Displayed</span></span> | <span data-ttu-id="bc8b6-139">De informatie wordt weergegeven en er wordt een waarschuwing weergegeven als u een resource kiest die niet geschikt is.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-139">Shows the information and displays a warning if you choose a resource that is not qualified.</span></span>|  
    |<span data-ttu-id="bc8b6-140">Niet gebruikt.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-140">Not Used</span></span> | <span data-ttu-id="bc8b6-141">Geef deze gegevens niet weer.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-141">Does not show this information.</span></span>|  

## <a name="to-update-resource-capacity"></a><span data-ttu-id="bc8b6-142">Resourcecapaciteit bijwerken</span><span class="sxs-lookup"><span data-stu-id="bc8b6-142">To update resource capacity</span></span>  
<span data-ttu-id="bc8b6-143">U kunt de resourcecapaciteit desgewenst wijzigen.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-143">You may need to change the capacity of resources.</span></span>  
  
1. <span data-ttu-id="bc8b6-144">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Resourcecapaciteit** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-144">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Resource Capacity**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bc8b6-145">Kies de resource en kies vervolgens de actie **Capaciteit instellen**.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-145">Choose the resource, and then choose the **Set Capacity** action.</span></span>  
3. <span data-ttu-id="bc8b6-146">Breng de wijzigingen aan en kies **Capaciteit bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-146">Make the changes, and then choose **Update Capacity**.</span></span>  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a><span data-ttu-id="bc8b6-147">Bekwaamheden voor artikelen, serviceartikelen of serviceartikelgroepen bijwerken</span><span class="sxs-lookup"><span data-stu-id="bc8b6-147">To update skills for items, service items, or service item groups</span></span>
<span data-ttu-id="bc8b6-148">Wilt u de bekwaamheidscodes wijzigen die aan artikelen zijn toegewezen, bijvoorbeeld van **PC** in **STUKS**, dan kunt u dit voor een artikel, serviceartikel of alle items in een serviceartikelgroep doen.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-148">If you want to change the skill codes assigned to items, for example from **PC** to **PCS**, you can do so either for an item, service item, or for all items in a service item group.</span></span>  
  
1. <span data-ttu-id="bc8b6-149">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen**, **Serviceartikel** of **Serviceartikelgroep** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-149">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items** or **Service Item**, or **Service Item Group**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bc8b6-150">Kies de entiteit die u wilt bijwerken en kies vervolgens de actie **Resourcebekwaamheden**.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-150">Choose the entity to update, and then choose the **Resource Skills** action.</span></span>  
3. <span data-ttu-id="bc8b6-151">Op de regel met de code die u wilt wijzigen, selecteert u de betreffende bekwaamheidscode in het veld **Bekwaamheidscode**.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-151">On the line with the code to be changed, in the **Skill Code** field, choose the relevant skill code.</span></span>  
4.  <span data-ttu-id="bc8b6-152">Als er serviceartikelen aan het artikel zijn gekoppeld, wordt er een dialoogvenster geopend met de volgende twee opties:</span><span class="sxs-lookup"><span data-stu-id="bc8b6-152">If the item has associated service items, a dialog box opens with the following two options:</span></span>  
  
    * <span data-ttu-id="bc8b6-153">De bekwaamheidscodes wijzigen in de geselecteerde waarde: selecteer deze optie als u de oude bekwaamheidscode voor alle gerelateerde serviceartikelen wilt vervangen door de nieuwe code.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-153">Change the skill codes to the selected value: Select this option if you want to replace the old skill code with the new one on all the related service items.</span></span>  
    * <span data-ttu-id="bc8b6-154">De bekwaamheidscodes verwijderen of hun relatie bijwerken: selecteer deze optie als u alleen voor dit artikel de bekwaamheidscode wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-154">Delete the skill codes or update their relation: Select this option if you want to change the skill code on this item only.</span></span> <span data-ttu-id="bc8b6-155">De bekwaamheidscode voor de gerelateerde serviceartikelen wordt opnieuw toegewezen, dat wil zeggen dat het veld **Toegewezen vanuit** wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="bc8b6-155">The skill code on the related service items will be reassigned, that is, the **Assigned From** field will be updated.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bc8b6-156">Zie ook</span><span class="sxs-lookup"><span data-stu-id="bc8b6-156">See Also</span></span>
[<span data-ttu-id="bc8b6-157">Resources toewijzen</span><span class="sxs-lookup"><span data-stu-id="bc8b6-157">Allocate Resources</span></span>](service-how-to-allocate-resources.md)  
[<span data-ttu-id="bc8b6-158">Service- en werkuren instellen</span><span class="sxs-lookup"><span data-stu-id="bc8b6-158">Set Up Work Hours and Service Hours</span></span>](service-how-setup-work-service-hours.md)  
[<span data-ttu-id="bc8b6-159">Foutrapportage instellen</span><span class="sxs-lookup"><span data-stu-id="bc8b6-159">Set Up Fault Reporting</span></span>](service-how-setup-fault-reporting.md)  
[<span data-ttu-id="bc8b6-160">Codes voor standaardservices instellen</span><span class="sxs-lookup"><span data-stu-id="bc8b6-160">Set Up Codes for Standard Services</span></span>](service-how-setup-service-coding.md)  
 

