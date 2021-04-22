---
title: 'Ontwerpdetails: Magazijnoverzicht | Microsoft Docs'
description: Om de fysieke verwerking van artikelen op het niveau van zones en opslaglocaties te ondersteunen, moeten alle gegevens worden getraceerd van elke transactie of verplaatsing in het magazijn. Dit wordt beheerd in de tabel **Magazijnpost**. Elke transactie wordt opgeslagen in een magazijnjournaal.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 8a972cebc919e0e308f22b417a62f33cb8b06f62
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785147"
---
# <a name="design-details-warehouse-overview"></a><span data-ttu-id="ba230-105">Ontwerpdetails: Magazijnoverzicht</span><span class="sxs-lookup"><span data-stu-id="ba230-105">Design Details: Warehouse Overview</span></span>
<span data-ttu-id="ba230-106">Om de fysieke verwerking van artikelen op het niveau van zones en opslaglocaties te ondersteunen, moeten alle gegevens worden getraceerd van elke transactie of verplaatsing in het magazijn.</span><span class="sxs-lookup"><span data-stu-id="ba230-106">To support the physical handling of items on the zone and bin level, all information must be traced for each transaction or movement in the warehouse.</span></span> <span data-ttu-id="ba230-107">Dit wordt beheerd in de tabel **Magazijnpost**.</span><span class="sxs-lookup"><span data-stu-id="ba230-107">This is managed in the **Warehouse Entry** table.</span></span> <span data-ttu-id="ba230-108">Elke transactie wordt opgeslagen in een magazijnjournaal.</span><span class="sxs-lookup"><span data-stu-id="ba230-108">Each transaction is stored in a warehouse register.</span></span>  

<span data-ttu-id="ba230-109">Magazijndocumenten en een magazijndagboek worden gebruikt om artikelmutaties in het magazijn te registreren.</span><span class="sxs-lookup"><span data-stu-id="ba230-109">Warehouse documents and a warehouse journal are used to register item movements in the warehouse.</span></span> <span data-ttu-id="ba230-110">Telkens wanneer een artikel in het magazijn wordt verplaatst, ontvangen, opgeslagen, gepickt, verzonden of aangepast, worden magazijnposten vastgelegd om de fysieke informatie op te slaan over zone, opslaglocatie en aantal.</span><span class="sxs-lookup"><span data-stu-id="ba230-110">Every time that an item in the warehouse is moved, received, put away, picked, shipped, or adjusted, warehouse entries are registered to store the physical information about zone, bin, and quantity.</span></span>

<span data-ttu-id="ba230-111">De tabel **Opslaglocatie-inhoud** wordt gebruikt om alle verschillende dimensies van de inhoud van een opslaglocatie per artikel, zoals eenheid, en maximum- en minimumaantal te verwerken.</span><span class="sxs-lookup"><span data-stu-id="ba230-111">The **Bin Content** table is used to handle all the different dimensions of the contents of a bin per item, such as unit of measure, maximum quantity, and minimum quantity.</span></span> <span data-ttu-id="ba230-112">De tabel **Opslaglocatie-inhoud** bevat ook stroomvelden naar de magazijnposten, magazijninstructies en magazijndagboekregels, die ervoor zorgen dat de beschikbaarheid van een artikel per opslaglocatie en een opslaglocatie voor een artikel snel kunnen worden berekend.</span><span class="sxs-lookup"><span data-stu-id="ba230-112">The **Bin Content** table also contains flow fields to the warehouse entries, warehouse instructions, and warehouse journal lines, which ensures that the availability of an item per bin and a bin for an item can be calculated quickly.</span></span> <span data-ttu-id="ba230-113">Zie voor meer informatie [Ontwerpdetails: Beschikbaarheid in het magazijn](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="ba230-113">For more information, see [Design Details: Availability in the Warehouse](design-details-availability-in-the-warehouse.md).</span></span>  

<span data-ttu-id="ba230-114">Wanneer artikelboekingen buiten de magazijnmodule plaatsvinden, wordt een standaardherwaarderingsopslaglocatie per vestiging gebruikt om magazijnposten te synchroniseren met voorraadposten.</span><span class="sxs-lookup"><span data-stu-id="ba230-114">When item postings occur outside the warehouse module, a default adjustment bin per location is used to synchronize warehouse entries with inventory entries.</span></span> <span data-ttu-id="ba230-115">Tijdens fysieke inventarisatie van het magazijn worden eventuele verschillen tussen de berekende en getelde aantallen geregistreerd in de correctieopslaglocatie en vervolgens als corrigerende artikelposten geboekt.</span><span class="sxs-lookup"><span data-stu-id="ba230-115">During physical inventory of the warehouse, any differences between the calculated and counted quantities are recorded in the adjustment bin and then posted as correcting item ledger entries.</span></span> <span data-ttu-id="ba230-116">Zie [Ontwerpdetails: Integratie met voorraad](design-details-integration-with-inventory.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ba230-116">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="ba230-117">De volgende illustratie geeft gebruikelijke magazijnstromen aan.</span><span class="sxs-lookup"><span data-stu-id="ba230-117">The following illustration outlines typical warehouse flows.</span></span>  

<span data-ttu-id="ba230-118">![Overzicht van magazijnprocessen](media/design_details_warehouse_management_overview.png "Overzicht van magazijnprocessen")</span><span class="sxs-lookup"><span data-stu-id="ba230-118">![Overview of warehouse processes](media/design_details_warehouse_management_overview.png "Overview of warehouse processes")</span></span>  

## <a name="basic-or-advanced-warehousing"></a><span data-ttu-id="ba230-119">Elementaire of geavanceerde magazijnfuncties</span><span class="sxs-lookup"><span data-stu-id="ba230-119">Basic or Advanced Warehousing</span></span>  
<span data-ttu-id="ba230-120">De magazijnfunctionaliteit in [!INCLUDE[prod_short](includes/prod_short.md)] kan in verschillende complexiteitsniveaus worden geïmplementeerd, afhankelijk van de processen en het ordervolume van een bedrijf.</span><span class="sxs-lookup"><span data-stu-id="ba230-120">Warehouse functionality in [!INCLUDE[prod_short](includes/prod_short.md)] can be implemented in different complexity levels, depending on a company’s processes and order volume.</span></span> <span data-ttu-id="ba230-121">Het belangrijkste verschil is dat de activiteiten per order worden uitgevoerd bij standaardmagazijnbeheer, terwijl ze worden samengevoegd voor meerdere orders bij geavanceerd magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="ba230-121">The main difference is that activities are performed order-by-order in basic warehousing when they are consolidated for multiple orders in advanced warehousing.</span></span>  

 <span data-ttu-id="ba230-122">Om te onderscheiden tussen de verschillende complexiteitniveaus wordt in deze documentatie verwezen naar twee algemene denominaties, elementaire en geavanceerde magazijnfuncties.</span><span class="sxs-lookup"><span data-stu-id="ba230-122">To differentiate between the different complexity levels, this documentation refers to two general denominations, Basic and Advanced Warehousing.</span></span> <span data-ttu-id="ba230-123">Dit eenvoudig onderscheid omvat meerdere verschillende complexiteitniveaus zoals gedefinieerd door productgranules en vestigingsinstellingen, waarbij elk wordt ondersteund door verschillende UI-documenten.</span><span class="sxs-lookup"><span data-stu-id="ba230-123">This simple differentiation covers several different complexity levels as defined by product granules and location setup, each supported by different UI documents.</span></span> <span data-ttu-id="ba230-124">Zie voor meer informatie [Ontwerpdetails: Magazijninstelling](design-details-warehouse-setup.md).</span><span class="sxs-lookup"><span data-stu-id="ba230-124">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="ba230-125">Het meest geavanceerde niveau van magazijnbeheer wordt in deze documentatie "WMS-installaties" genoemd, aangezien voor dit niveau de meest geavanceerde granule is vereist: Warehouse Management System.</span><span class="sxs-lookup"><span data-stu-id="ba230-125">The most advanced level of warehousing is referred to as “WMS installations” in this documentation, since this level requires the most advanced granule, Warehouse Management Systems.</span></span>  

 <span data-ttu-id="ba230-126">De volgende verschillende UI-documenten worden gebruikt in standaard- en geavanceerde magazijnfuncties.</span><span class="sxs-lookup"><span data-stu-id="ba230-126">The following different UI documents are used in basic and advanced warehousing.</span></span>  

## <a name="basic-ui-documents"></a><span data-ttu-id="ba230-127">Elementaire UI-documenten</span><span class="sxs-lookup"><span data-stu-id="ba230-127">Basic UI Documents</span></span>  

-   <span data-ttu-id="ba230-128">**Voorraadopslag**</span><span class="sxs-lookup"><span data-stu-id="ba230-128">**Inventory Put-away**</span></span>  
-   <span data-ttu-id="ba230-129">**Voorraadpick**</span><span class="sxs-lookup"><span data-stu-id="ba230-129">**Inventory Pick**</span></span>  
-   <span data-ttu-id="ba230-130">**Voorraadverplaatsing**</span><span class="sxs-lookup"><span data-stu-id="ba230-130">**Inventory Movement**</span></span>  
-   <span data-ttu-id="ba230-131">**Artikeldagboek**</span><span class="sxs-lookup"><span data-stu-id="ba230-131">**Item Journal**</span></span>  
-   <span data-ttu-id="ba230-132">**Artikelherindelingsdagboek**</span><span class="sxs-lookup"><span data-stu-id="ba230-132">**Item Reclassification Journal**</span></span>  
-   <span data-ttu-id="ba230-133">(Diverse lijsten)</span><span class="sxs-lookup"><span data-stu-id="ba230-133">(Various reports)</span></span>  

## <a name="advanced-ui-documents"></a><span data-ttu-id="ba230-134">Geavanceerde UI-documenten</span><span class="sxs-lookup"><span data-stu-id="ba230-134">Advanced UI Documents</span></span>  

-   <span data-ttu-id="ba230-135">**Magazijnontvangst**</span><span class="sxs-lookup"><span data-stu-id="ba230-135">**Warehouse Receipt**</span></span>  
-   <span data-ttu-id="ba230-136">**Opslagvoorstel**</span><span class="sxs-lookup"><span data-stu-id="ba230-136">**Put-away Worksheet**</span></span>  
-   <span data-ttu-id="ba230-137">**Magazijnopslag**</span><span class="sxs-lookup"><span data-stu-id="ba230-137">**Warehouse Put-away**</span></span>  
-   <span data-ttu-id="ba230-138">**Pickvoorstel**</span><span class="sxs-lookup"><span data-stu-id="ba230-138">**Pick Worksheet**</span></span>  
-   <span data-ttu-id="ba230-139">**Magazijnpick**</span><span class="sxs-lookup"><span data-stu-id="ba230-139">**Warehouse Pick**</span></span>  
-   <span data-ttu-id="ba230-140">**Verplaatsingsvoorstel**</span><span class="sxs-lookup"><span data-stu-id="ba230-140">**Movement Worksheet**</span></span>  
-   <span data-ttu-id="ba230-141">**Magazijnverplaatsing**</span><span class="sxs-lookup"><span data-stu-id="ba230-141">**Warehouse Movement**</span></span>  
-   <span data-ttu-id="ba230-142">**Interne mag.-pick**</span><span class="sxs-lookup"><span data-stu-id="ba230-142">**Internal Whse. Pick**</span></span>  
-   <span data-ttu-id="ba230-143">**Interne mag.-opslag**</span><span class="sxs-lookup"><span data-stu-id="ba230-143">**Internal Whse. Put-away**</span></span>  
-   <span data-ttu-id="ba230-144">**Voorstel opslaglocatieaanmaak**</span><span class="sxs-lookup"><span data-stu-id="ba230-144">**Bin Creation Worksheet**</span></span>  
-   <span data-ttu-id="ba230-145">**Voorstel opslaglocatie-inhoudaanmaak**</span><span class="sxs-lookup"><span data-stu-id="ba230-145">**Bin Content Creation Worksheet**</span></span>  
-   <span data-ttu-id="ba230-146">**Mag.-artikeldagboek**</span><span class="sxs-lookup"><span data-stu-id="ba230-146">**Whse. Item Journal**</span></span>  
-   <span data-ttu-id="ba230-147">**Mag.-herindelingsdagboek**</span><span class="sxs-lookup"><span data-stu-id="ba230-147">**Whse. Item Reclass. Journal**</span></span>  
-   <span data-ttu-id="ba230-148">(Diverse lijsten)</span><span class="sxs-lookup"><span data-stu-id="ba230-148">(Various reports)</span></span>  

<span data-ttu-id="ba230-149">Voor meer informatie over elk document raadpleegt u de respectievelijke paginaonderwerpen.</span><span class="sxs-lookup"><span data-stu-id="ba230-149">For more information about each document, see the respective page topics.</span></span>  

### <a name="terminology"></a><span data-ttu-id="ba230-150">Terminologie</span><span class="sxs-lookup"><span data-stu-id="ba230-150">Terminology</span></span>  
<span data-ttu-id="ba230-151">Ter afstemming met de financiële begrippen van inkopen en verkopen verwijst de [!INCLUDE[prod_short](includes/prod_short.md)]-magazijndocumentatie naar de volgende termen voor artikelstromen in het magazijn.</span><span class="sxs-lookup"><span data-stu-id="ba230-151">To align with the financial concepts of purchases and sales, [!INCLUDE[prod_short](includes/prod_short.md)] warehouse documentation refers to the following terms for item flow in the warehouse.</span></span>  

|<span data-ttu-id="ba230-152">Term</span><span class="sxs-lookup"><span data-stu-id="ba230-152">Term</span></span>|<span data-ttu-id="ba230-153">Description</span><span class="sxs-lookup"><span data-stu-id="ba230-153">Description</span></span>|  
|----------|---------------------------------------|  
|<span data-ttu-id="ba230-154">Inkomende stroom</span><span class="sxs-lookup"><span data-stu-id="ba230-154">Inbound flow</span></span>|<span data-ttu-id="ba230-155">Artikelen die naar de magazijnvestiging worden verplaatst, zoals inkopen en inkomende transfers.</span><span class="sxs-lookup"><span data-stu-id="ba230-155">Items moving into the warehouse location, such as purchases and inbound transfers.</span></span>|  
|<span data-ttu-id="ba230-156">Interne stroom</span><span class="sxs-lookup"><span data-stu-id="ba230-156">Internal flow</span></span>|<span data-ttu-id="ba230-157">Artikelen die binnen de magazijnvestiging worden verplaatst, zoals productiecomponenten en output.</span><span class="sxs-lookup"><span data-stu-id="ba230-157">Items moving inside the warehouse location, such as production components and output.</span></span>|  
|<span data-ttu-id="ba230-158">Uitgaande stroom</span><span class="sxs-lookup"><span data-stu-id="ba230-158">Outbound flow</span></span>|<span data-ttu-id="ba230-159">Artikelen die uit de magazijnvestiging worden verplaatst, zoals verkopen en uitgaande transfers.</span><span class="sxs-lookup"><span data-stu-id="ba230-159">Items moving out of the warehouse location, such as sales and outbound transfers.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="ba230-160">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ba230-160">See Also</span></span>  
 [<span data-ttu-id="ba230-161">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="ba230-161">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]