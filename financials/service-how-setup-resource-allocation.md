---
title: Resourcetoewijzing instellen | Microsoft Docs
description: Leer hoe u er met het systeem voor kunt zorgen dat u iemand toewijst die over de vereiste vaardigheden beschikt om een service te bieden.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resource, skill, service, zones
ms.date: 08/22/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b16ba9366aefc108f39667678fe8ab70ce421b83
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---

# <a name="set-up-resource-allocation"></a><span data-ttu-id="0aab7-103">Resourcetoewijzing instellen</span><span class="sxs-lookup"><span data-stu-id="0aab7-103">Set Up Resource Allocation</span></span>
<span data-ttu-id="0aab7-104">Om ervoor te zorgen dat een servicetaak goed wordt uitgevoerd, is het belangrijk een resource te vinden die gekwalificeerd is om het werk uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="0aab7-104">To ensure that a service task is performed well, it's important to find a resource who is qualified to do the work.</span></span> <span data-ttu-id="0aab7-105">U kunt [!INCLUDE[d365fin](includes/d365fin_md.md)] zo instellen dat het eenvoudig is om iemand toe te wijzen die over de juiste bekwaamheden voor het project beschikt.</span><span class="sxs-lookup"><span data-stu-id="0aab7-105">You can set up [!INCLUDE[d365fin](includes/d365fin_md.md)] so that it's easy to allocate someone who has the right skills for the job.</span></span> <span data-ttu-id="0aab7-106">In [!INCLUDE[d365fin](includes/d365fin_md.md)] noemen we dit _resourcetoewijzing_.</span><span class="sxs-lookup"><span data-stu-id="0aab7-106">In [!INCLUDE[d365fin](includes/d365fin_md.md)], we call this _resource allocation_.</span></span> <span data-ttu-id="0aab7-107">U kunt resources toewijzen op basis van hun vaardigheden, beschikbaarheid en locatie (of ze zich in dezelfde serviceregio als de klant bevinden).</span><span class="sxs-lookup"><span data-stu-id="0aab7-107">You can allocate resources based on their skill, availability, or whether they are in the same service zone as the customer.</span></span> 

<span data-ttu-id="0aab7-108">U moet het volgende instellen om resourcetoewijzing te gebruiken:</span><span class="sxs-lookup"><span data-stu-id="0aab7-108">To use resource allocation, you must set up:</span></span>  
  
* <span data-ttu-id="0aab7-109">De benodigde bekwaamheden om serviceartikelen te repareren en te onderhouden.</span><span class="sxs-lookup"><span data-stu-id="0aab7-109">The skills required to repair and maintain service items.</span></span> <span data-ttu-id="0aab7-110">U wijst deze toe aan serviceartikelen en resources.</span><span class="sxs-lookup"><span data-stu-id="0aab7-110">You assign these to service items and resources.</span></span>  
* <span data-ttu-id="0aab7-111">Geografische gebieden, regio's, die u voor de markt definieert.</span><span class="sxs-lookup"><span data-stu-id="0aab7-111">Geographic regions, called zones, that you define for your market.</span></span> <span data-ttu-id="0aab7-112">Dit kunnen bijvoorbeeld Oost, West, Centraal, enzovoort zijn.</span><span class="sxs-lookup"><span data-stu-id="0aab7-112">For example, East, West, Central, and so on.</span></span> <span data-ttu-id="0aab7-113">U wijst deze toe aan klanten en resources.</span><span class="sxs-lookup"><span data-stu-id="0aab7-113">You assign these to customers and resources.</span></span>  
* <span data-ttu-id="0aab7-114">Of er resourcebekwaamheden en -regio's moeten worden weergegeven en of er een waarschuwing moet worden weergegeven als iemand een ongeschikte resource kiest of een resource die zich niet in de klantregio bevindt.</span><span class="sxs-lookup"><span data-stu-id="0aab7-114">Whether to display resource skills and zones, and whether to display a warning if someone chooses unqualified resource, or a resource that is not in the customer zone.</span></span>  

## <a name="to-set-up-skills"></a><span data-ttu-id="0aab7-115">Bekwaamheden instellen</span><span class="sxs-lookup"><span data-stu-id="0aab7-115">To set up skills</span></span>
1. <span data-ttu-id="0aab7-116">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bekwaamheden** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="0aab7-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Skills**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0aab7-117">Vul de velden in.</span><span class="sxs-lookup"><span data-stu-id="0aab7-117">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a><span data-ttu-id="0aab7-118">Bekwaamheden toewijzen aan serviceartikelen en resources</span><span class="sxs-lookup"><span data-stu-id="0aab7-118">To assign skills to service items and resources</span></span>
1. <span data-ttu-id="0aab7-119">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Serviceartikelen** of **Resources** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="0aab7-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Items** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0aab7-120">Open de kaart voor het serviceartikel of de resource en kies een van de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="0aab7-120">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="0aab7-121">Voor serviceartikelen kiest u **Resourcebekwaamheden**.</span><span class="sxs-lookup"><span data-stu-id="0aab7-121">For service items, choose **Resource Skills**.</span></span>  
    * <span data-ttu-id="0aab7-122">Voor resources kiest u **Bekwaamheden**.</span><span class="sxs-lookup"><span data-stu-id="0aab7-122">For resources, choose **Skills**.</span></span>  

## <a name="to-set-up-zones"></a><span data-ttu-id="0aab7-123">Regio's instellen</span><span class="sxs-lookup"><span data-stu-id="0aab7-123">To set up zones</span></span>
1. <span data-ttu-id="0aab7-124">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Regio's** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="0aab7-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Zones**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0aab7-125">Vul de velden in.</span><span class="sxs-lookup"><span data-stu-id="0aab7-125">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a><span data-ttu-id="0aab7-126">Regio's toewijzen aan klanten en resources</span><span class="sxs-lookup"><span data-stu-id="0aab7-126">To assign zones to customers and resources</span></span> 
1. <span data-ttu-id="0aab7-127">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Klanten** of **Resources** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="0aab7-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers** or **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0aab7-128">Open de kaart voor het serviceartikel of de resource en kies een van de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="0aab7-128">Open the card for the service item or resource, and then choose one of the following:</span></span>  
  
    * <span data-ttu-id="0aab7-129">Voor klanten kiest u een regio in het veld **Serviceregiocode**.</span><span class="sxs-lookup"><span data-stu-id="0aab7-129">For customers, choose a zone in the **Service Zone Code** field.</span></span>  
    * <span data-ttu-id="0aab7-130">Voor resources kiest u de actie **Serviceregio's**.</span><span class="sxs-lookup"><span data-stu-id="0aab7-130">For resources, choose the **Service Zones** action.</span></span>  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a><span data-ttu-id="0aab7-131">Opgeven wat er moet worden weergegeven wanneer een resource is gekozen</span><span class="sxs-lookup"><span data-stu-id="0aab7-131">To specify what to show when a resource is chosen</span></span>
1. <span data-ttu-id="0aab7-132">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Service-instellingen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="0aab7-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Setup**, and then choose the related link.</span></span> 
2. <span data-ttu-id="0aab7-133">Kies in het veld **Optie resourcebekwaamheden** een van de opties die in de volgende tabel worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="0aab7-133">In the **Resource Skills Option** field, choose one of the options described in the following table.</span></span>  
  
    |<span data-ttu-id="0aab7-134">**Optie**</span><span class="sxs-lookup"><span data-stu-id="0aab7-134">**Option**</span></span>|<span data-ttu-id="0aab7-135">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="0aab7-135">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="0aab7-136">Code getoond</span><span class="sxs-lookup"><span data-stu-id="0aab7-136">Code Shown</span></span> | <span data-ttu-id="0aab7-137">Alleen de code wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0aab7-137">Displays the code only.</span></span>|  
    |<span data-ttu-id="0aab7-138">Waarschuwing getoond</span><span class="sxs-lookup"><span data-stu-id="0aab7-138">Warning Displayed</span></span> | <span data-ttu-id="0aab7-139">De informatie wordt weergegeven en er wordt een waarschuwing weergegeven als u een resource kiest die niet geschikt is.</span><span class="sxs-lookup"><span data-stu-id="0aab7-139">Shows the information and displays a warning if you choose a resource that is not qualified.</span></span>|  
    |<span data-ttu-id="0aab7-140">Niet gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0aab7-140">Not Used</span></span> | <span data-ttu-id="0aab7-141">Geef deze gegevens niet weer.</span><span class="sxs-lookup"><span data-stu-id="0aab7-141">Does not show this information.</span></span>|  

## <a name="to-update-resource-capacity"></a><span data-ttu-id="0aab7-142">Resourcecapaciteit bijwerken</span><span class="sxs-lookup"><span data-stu-id="0aab7-142">To update resource capacity</span></span>  
<span data-ttu-id="0aab7-143">U kunt de resourcecapaciteit desgewenst wijzigen.</span><span class="sxs-lookup"><span data-stu-id="0aab7-143">You may need to change the capacity of resources.</span></span>  
  
1. <span data-ttu-id="0aab7-144">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png ""pictogram Zoeken naar pagina of rapport"), voer **Resourcecapaciteit** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="0aab7-144">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Capacity**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0aab7-145">Kies de resource en kies vervolgens de actie **Capaciteit instellen**.</span><span class="sxs-lookup"><span data-stu-id="0aab7-145">Choose the resource, and then choose the **Set Capacity** action.</span></span>  
3. <span data-ttu-id="0aab7-146">Breng de wijzigingen aan en kies **Capaciteit bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="0aab7-146">Make the changes, and then choose **Update Capacity**.</span></span>  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a><span data-ttu-id="0aab7-147">Bekwaamheden voor artikelen, serviceartikelen of serviceartikelgroepen bijwerken</span><span class="sxs-lookup"><span data-stu-id="0aab7-147">To update skills for items, service items, or service item groups</span></span>
<span data-ttu-id="0aab7-148">Wilt u de bekwaamheidscodes wijzigen die aan artikelen zijn toegewezen, bijvoorbeeld van **PC** in **STUKS**, dan kunt u dit voor een artikel, serviceartikel of alle items in een serviceartikelgroep doen.</span><span class="sxs-lookup"><span data-stu-id="0aab7-148">If you want to change the skill codes assigned to items, for example from **PC** to **PCS**, you can do so either for an item, service item, or for all items in a service item group.</span></span>  
  
1. <span data-ttu-id="0aab7-149">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikelen** of **Serviceartikel**, of **Serviceartikelgroep** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="0aab7-149">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items** or **Service Item**, or **Service Item Group**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0aab7-150">Kies de entiteit die u wilt bijwerken en kies vervolgens de actie **Resourcebekwaamheden**.</span><span class="sxs-lookup"><span data-stu-id="0aab7-150">Choose the entity to update, and then choose the **Resource Skills** action.</span></span>  
3. <span data-ttu-id="0aab7-151">Op de regel met de code die u wilt wijzigen, selecteert u de betreffende bekwaamheidscode in het veld **Bekwaamheidscode**.</span><span class="sxs-lookup"><span data-stu-id="0aab7-151">On the line with the code to be changed, in the **Skill Code** field, choose the relevant skill code.</span></span>  
4.  <span data-ttu-id="0aab7-152">Als er serviceartikelen aan het artikel zijn gekoppeld, wordt er een dialoogvenster geopend met de volgende twee opties:</span><span class="sxs-lookup"><span data-stu-id="0aab7-152">If the item has associated service items, a dialog box opens with the following two options:</span></span>  
  
    * <span data-ttu-id="0aab7-153">De bekwaamheidscodes wijzigen in de geselecteerde waarde: selecteer deze optie als u de oude bekwaamheidscode voor alle gerelateerde serviceartikelen wilt vervangen door de nieuwe code.</span><span class="sxs-lookup"><span data-stu-id="0aab7-153">Change the skill codes to the selected value: Select this option if you want to replace the old skill code with the new one on all the related service items.</span></span>  
    * <span data-ttu-id="0aab7-154">De bekwaamheidscodes verwijderen of hun relatie bijwerken: selecteer deze optie als u alleen voor dit artikel de bekwaamheidscode wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="0aab7-154">Delete the skill codes or update their relation: Select this option if you want to change the skill code on this item only.</span></span> <span data-ttu-id="0aab7-155">De bekwaamheidscode voor de gerelateerde serviceartikelen wordt opnieuw toegewezen, dat wil zeggen dat het veld **Toegewezen vanuit** wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="0aab7-155">The skill code on the related service items will be reassigned, that is, the **Assigned From** field will be updated.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0aab7-156">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0aab7-156">See Also</span></span>
[<span data-ttu-id="0aab7-157">Resources toewijzen</span><span class="sxs-lookup"><span data-stu-id="0aab7-157">Allocate Resources</span></span>](service-how-to-allocate-resources.md)  
[<span data-ttu-id="0aab7-158">Service- en werkuren instellen</span><span class="sxs-lookup"><span data-stu-id="0aab7-158">Set Up Work Hours and Service Hours</span></span>](service-how-setup-work-service-hours.md)  
[<span data-ttu-id="0aab7-159">Foutrapportage instellen</span><span class="sxs-lookup"><span data-stu-id="0aab7-159">Set Up Fault Reporting</span></span>](service-how-setup-fault-reporting.md)  
[<span data-ttu-id="0aab7-160">Codes voor standaardservices instellen</span><span class="sxs-lookup"><span data-stu-id="0aab7-160">Set Up Codes for Standard Services</span></span>](service-how-setup-service-coding.md)  
 


