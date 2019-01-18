---
title: Instellingen voor serviceartikelen en serviceartikelonderdelen | Microsoft Docs
description: Leer wat u moet instellen voordat u serviceartikelen, inclusief standaardwaarden voor onder andere de responstijd, het contractkortingspercentage en de serviceprijsgroep, kunt gebruiken.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: e82aa86668da5999117eea636ee29d8fde2cc09e
ms.contentlocale: nl-be
ms.lasthandoff: 11/26/2018

---
# <a name="set-up-service-items-and-service-item-components"></a><span data-ttu-id="c976f-103">Serviceartikelen en serviceartikelonderdelen instellen</span><span class="sxs-lookup"><span data-stu-id="c976f-103">Set Up Service Items and Service Item Components</span></span>
<span data-ttu-id="c976f-104">Als u met serviceartikelen wilt werken, moet u het volgende instellen</span><span class="sxs-lookup"><span data-stu-id="c976f-104">To work with service items, you must set up the following</span></span>

* <span data-ttu-id="c976f-105">Serviceartikelgroepen.</span><span class="sxs-lookup"><span data-stu-id="c976f-105">Service item groups.</span></span>
* <span data-ttu-id="c976f-106">Optioneel</span><span class="sxs-lookup"><span data-stu-id="c976f-106">Optional</span></span>

## <a name="to-set-up-service-item-groups"></a><span data-ttu-id="c976f-107">Serviceartikelgroepen instellen</span><span class="sxs-lookup"><span data-stu-id="c976f-107">To set up service item groups</span></span>
<span data-ttu-id="c976f-108">U kunt groepen van artikelen instellen die aan elkaar gerelateerd zijn met betrekking tot herstel en onderhoud.</span><span class="sxs-lookup"><span data-stu-id="c976f-108">You can set up groups of items that are related in terms of repair and maintenance.</span></span> <span data-ttu-id="c976f-109">U kunt standaardwaarden voor serviceartikelen in een serviceartikelgroep opgeven, zoals responstijd, contractkortingspercentage en serviceprijsgroep.</span><span class="sxs-lookup"><span data-stu-id="c976f-109">You can define default values for service items in a service item group, such as response time, contract discount percent, and service price group.</span></span> <span data-ttu-id="c976f-110">Voor artikelen in een serviceartikelgroep kunt u aangeven of deze automatisch als serviceartikelen moeten worden geregistreerd wanneer ze worden verkocht.</span><span class="sxs-lookup"><span data-stu-id="c976f-110">For items in a service item group, you can select whether you want them to be automatically registered as service items when they are sold.</span></span>  

<span data-ttu-id="c976f-111">U wijst serviceartikelgroepen toe aan artikelen op de kaart **Artikel** en aan serviceartikelen op de kaart **Serviceartikel**.</span><span class="sxs-lookup"><span data-stu-id="c976f-111">You assign service item groups to items on the **Item** card, and to service items on the **Service Item** card.</span></span>  

1. <span data-ttu-id="c976f-112">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Serviceartikelgroepen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="c976f-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c976f-113">Maak een nieuwe serviceartikelgroep.</span><span class="sxs-lookup"><span data-stu-id="c976f-113">Create a new service item group.</span></span>  
3. <span data-ttu-id="c976f-114">Vul de velden **Code** en **Omschrijving** in.</span><span class="sxs-lookup"><span data-stu-id="c976f-114">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="c976f-115">Geef in het veld **Std. contractkorting %** het standaardpercentage voor de contractkorting op dat u wilt toewijzen aan de serviceartikelen in de groep.</span><span class="sxs-lookup"><span data-stu-id="c976f-115">In the **Default Contract Discount %** field, enter the default contract discount percentage that you want the service items in the group to have.</span></span>  
5. <span data-ttu-id="c976f-116">Geef in het veld **Std. serviceprijsgroepcode** de code voor de standaardserviceprijsgroep op die u wilt toewijzen aan de serviceartikelen in de groep.</span><span class="sxs-lookup"><span data-stu-id="c976f-116">In the **Default Serv. Price Group Code** field, enter the default service price group code that you want the service items in the group to have.</span></span>  
6. <span data-ttu-id="c976f-117">Voer in het veld **Std. responstijd (Uren)** de standaardresponstijd in uren in die u wilt toewijzen aan de serviceartikelen in de groep.</span><span class="sxs-lookup"><span data-stu-id="c976f-117">In the **Default Response Time (Hours)** field, enter the default response time in hours that you want the service items in the group to have.</span></span>  
7. <span data-ttu-id="c976f-118">Als u de artikelen in de groep bij verkoop als serviceartikelen wilt registreren, moet u het veld **Serviceartikel maken** selecteren.</span><span class="sxs-lookup"><span data-stu-id="c976f-118">If you want to register the items in the group as service items when they are sold, select the **Create Service Item** field.</span></span>  

## <a name="to-set-up-service-item-components"></a><span data-ttu-id="c976f-119">Serviceartikelcomponenten instellen</span><span class="sxs-lookup"><span data-stu-id="c976f-119">To set up service item components</span></span>
<span data-ttu-id="c976f-120">Een serviceartikel kan bestaan uit meerdere onderdelen die u door reserveonderdelen kunt vervangen wanneer voor het artikel service wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c976f-120">A service item can consist of several components, which can be replaced with spare parts when the item is serviced.</span></span> <span data-ttu-id="c976f-121">Deze onderdelen zijn ingesteld op de pagina **Serviceartikelonderdeeloverzicht**.</span><span class="sxs-lookup"><span data-stu-id="c976f-121">These components are set up on the **Service Item Component List** page.</span></span> <span data-ttu-id="c976f-122">Als u onderdelen wilt instellen voor serviceartikelen die zijn ingesteld als stuklijst, kunt u de stuklijstartikelen kopiëren en instellen als serviceartikelcomponenten.</span><span class="sxs-lookup"><span data-stu-id="c976f-122">Additionally, if you want to set up components for service items that are BOMs, you can copy the BOM items and create them as service item components.</span></span>

1. <span data-ttu-id="c976f-123">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Serviceartikelen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="c976f-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="c976f-124">Open het serviceartikel waarvoor u componenten wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="c976f-124">Open the service item for which you want to set up components.</span></span>  
3. <span data-ttu-id="c976f-125">Kies de actie **Materialen**.</span><span class="sxs-lookup"><span data-stu-id="c976f-125">Choose the **Components** action.</span></span> <span data-ttu-id="c976f-126">De pagina **Serviceartikelonderdeeloverzicht** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="c976f-126">The **Service Item Component List** page opens.</span></span>  
4. <span data-ttu-id="c976f-127">Een nieuw component toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c976f-127">Add a new component.</span></span>  
5. <span data-ttu-id="c976f-128">Kies in het veld **Soort** de optie **Serviceartikel** als de component zelf een geregistreerd serviceartikel is.</span><span class="sxs-lookup"><span data-stu-id="c976f-128">In the **Type** field, choose **Service Item** if the component itself is a registered service item.</span></span> <span data-ttu-id="c976f-129">Selecteer anders **Artikel**.</span><span class="sxs-lookup"><span data-stu-id="c976f-129">Otherwise, select **Item**.</span></span>  
6. <span data-ttu-id="c976f-130">Selecteer in het veld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="c976f-130">In the **No.**</span></span> <span data-ttu-id="c976f-131">het artikel of serviceartikel dat een component is van het serviceartikel.</span><span class="sxs-lookup"><span data-stu-id="c976f-131">field, choose the item or service item that is a component of the service item.</span></span>  

## <a name="to-set-up-service-item-components-from-a-bom"></a><span data-ttu-id="c976f-132">Serviceartikelcomponenten instellen uit stuklijsten</span><span class="sxs-lookup"><span data-stu-id="c976f-132">To set up service item components from a BOM</span></span>
1.  <span data-ttu-id="c976f-133">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Serviceartikelen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="c976f-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Items**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c976f-134">Open het serviceartikel waarvoor u componenten wilt instellen vanuit een stuklijst.</span><span class="sxs-lookup"><span data-stu-id="c976f-134">Open the service item for which you want to set up components from a BOM.</span></span>  
3. <span data-ttu-id="c976f-135">Kies de actie **Materialen**.</span><span class="sxs-lookup"><span data-stu-id="c976f-135">Choose the **Components** action.</span></span> <span data-ttu-id="c976f-136">De pagina **Serviceartikelonderdeeloverzicht** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="c976f-136">The **Service Item Component List** page opens.</span></span>  
4. <span data-ttu-id="c976f-137">Kies de actie **Van stuklijst kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="c976f-137">Choose the **Copy from BOM** action.</span></span>  

    <span data-ttu-id="c976f-138">Wanneer het artikel waaraan het serviceartikel is gekoppeld, een stuklijst is, worden automatisch componenten gemaakt voor alle artikelen in de stuklijst.</span><span class="sxs-lookup"><span data-stu-id="c976f-138">If the item that the service item is linked to is a BOM, the components for all the items in the BOM are created automatically.</span></span>  

## <a name="to-set-up-a-service-shelf"></a><span data-ttu-id="c976f-139">Serviceschappen instellen</span><span class="sxs-lookup"><span data-stu-id="c976f-139">To set up a service shelf</span></span>
<span data-ttu-id="c976f-140">U kunt serviceschappen instellen om de opslaglocatie van uw serviceartikelen aan te duiden.</span><span class="sxs-lookup"><span data-stu-id="c976f-140">You can set up service shelves that identify where you store your service items.</span></span> <span data-ttu-id="c976f-141">U wijst serviceschappen toe aan serviceartikelen op de pagina's **Serviceorder** en **Serviceartikelwerkbon**.</span><span class="sxs-lookup"><span data-stu-id="c976f-141">You assign service shelves to service items on the **Service Order** and **Service Item Worksheet** pages.</span></span>  

1. <span data-ttu-id="c976f-142">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Serviceschappen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="c976f-142">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Shelves**, and then choose the related link.</span></span>
2. <span data-ttu-id="c976f-143">Vul de benodigde velden in.</span><span class="sxs-lookup"><span data-stu-id="c976f-143">Fill in the fields as necessary.</span></span>

## <a name="see-also"></a><span data-ttu-id="c976f-144">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c976f-144">See Also</span></span>
<span data-ttu-id="c976f-145">[Codes voor standaardservices instellen](service-how-setup-service-coding.md) </span><span class="sxs-lookup"><span data-stu-id="c976f-145">[Set Up Codes for Standard Services](service-how-setup-service-coding.md) </span></span>  
[<span data-ttu-id="c976f-146">Troubleshooting instellen</span><span class="sxs-lookup"><span data-stu-id="c976f-146">Set Up Troubleshooting</span></span>](service-how-setup-troubleshooting.md)

