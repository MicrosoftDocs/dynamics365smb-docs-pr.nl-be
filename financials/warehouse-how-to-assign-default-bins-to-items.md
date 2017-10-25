---
title: Standaardopslaglocaties aan artikelen toewijzen | Microsoft Docs
description: Indien u op een locatie met opslaglocaties werkt, kan het toewijzen van standaardopslaglocaties aan uw artikelen het verzenden, ontvangen en verplaatsen van artikelen veel eenvoudiger maken. Wanneer een standaard opslaglocatie is toegewezen aan een artikel, wordt elke keer dat u een transactie voor dit artikel opstart deze opslaglocatie voorgesteld.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: ae0d22fa5384edef167e5ba473977079c6473673
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-assign-default-bins-to-items"></a><span data-ttu-id="2efe0-104">Procedure: standaardopslaglocaties aan artikelen toewijzen</span><span class="sxs-lookup"><span data-stu-id="2efe0-104">How to: Assign Default Bins to Items</span></span>
<span data-ttu-id="2efe0-105">Indien u op een locatie met opslaglocaties werkt, kan het toewijzen van standaardopslaglocaties aan uw artikelen het verzenden, ontvangen en verplaatsen van artikelen veel eenvoudiger maken.</span><span class="sxs-lookup"><span data-stu-id="2efe0-105">If you are using bins at a location, assigning default bins to your items can make the process of shipping, receiving, and moving your items much easier.</span></span> <span data-ttu-id="2efe0-106">Wanneer een standaard opslaglocatie is toegewezen aan een artikel, wordt elke keer dat u een transactie voor dit artikel opstart deze opslaglocatie voorgesteld.</span><span class="sxs-lookup"><span data-stu-id="2efe0-106">When a default bin is assigned to an item, this bin is suggested every time you initiate a transaction for this item.</span></span> <span data-ttu-id="2efe0-107">Standaardopslaglocaties worden gedefinieerd in het venster **Opslaglocatie-inhoud**.</span><span class="sxs-lookup"><span data-stu-id="2efe0-107">Default bins are defined in the **Bin Content** window.</span></span>  

## <a name="to-assign-a-default-bin-to-an-item"></a><span data-ttu-id="2efe0-108">Een standaardopslaglocatie toewijzen aan een artikel</span><span class="sxs-lookup"><span data-stu-id="2efe0-108">To assign a default bin to an item</span></span>
1.  <span data-ttu-id="2efe0-109">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Voorstel opslaglocatie-inhoudaanmaak** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="2efe0-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bin Content Creation Worksheet**, and choose the related link.</span></span>  
2.  <span data-ttu-id="2efe0-110">Vul de opslaglocatiecode en het artikel in voor elke opslaglocatie die u wilt instellen als standaardwaarde voor een artikel.</span><span class="sxs-lookup"><span data-stu-id="2efe0-110">Fill in the bin code and item information for each bin that you would like to set up as a default for an item.</span></span> <span data-ttu-id="2efe0-111">Selecteer het veld **Standaard**.</span><span class="sxs-lookup"><span data-stu-id="2efe0-111">Make sure to select the **Default** field.</span></span>  
3.  <span data-ttu-id="2efe0-112">Kies de actie **Opslaglocatie-inhoud maken**.</span><span class="sxs-lookup"><span data-stu-id="2efe0-112">Choose the **Create Bin Content** action.</span></span> <span data-ttu-id="2efe0-113">Er worden nu standaardopslaglocaties voor uw artikel toegewezen.</span><span class="sxs-lookup"><span data-stu-id="2efe0-113">Default bins are now assigned for your item.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2efe0-114">Wanneer een artikel wordt opgeslagen terwijl er voor het artikel geen standaardopslaglocatie is toegewezen, wordt de locatie waar het artikel wordt opgeslagen toegewezen als de standaardopslaglocatie.</span><span class="sxs-lookup"><span data-stu-id="2efe0-114">When an item is put away, if the item does not have a default bin assigned, the bin where the item is put away is assigned as the default.</span></span>  

## <a name="to-change-the-default-bin-for-an-item"></a><span data-ttu-id="2efe0-115">De standaardopslaglocatie voor een artikel wijzigen</span><span class="sxs-lookup"><span data-stu-id="2efe0-115">To change the default bin for an item</span></span>  
<span data-ttu-id="2efe0-116">Soms moet u de standaardtoewijzing van de opslaglocatie voor een bepaald artikel wijzigen of een standaardopslaglocatie toewijzen aan een nieuw artikel.</span><span class="sxs-lookup"><span data-stu-id="2efe0-116">You may need to change the default bin assignment for an item or assign a default bin to a new item.</span></span>    
1.  <span data-ttu-id="2efe0-117">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Opslaglocatie-inhoud** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="2efe0-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bin Contents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2efe0-118">Selecteer de juiste vestiging in het veld **Vestigingsfilter**.</span><span class="sxs-lookup"><span data-stu-id="2efe0-118">In the **Location Filter** field, select the appropriate location code.</span></span>  
3.  <span data-ttu-id="2efe0-119">Zoek naar de huidige inhoudspost van de standaardopslaglocatie voor het artikel en schakel het selectievakje **Standaardopslaglocatie** uit.</span><span class="sxs-lookup"><span data-stu-id="2efe0-119">Find the current default bin content entry for the item and clear the **Default Bin** check box.</span></span>  
4.  <span data-ttu-id="2efe0-120">Zoek naar de regel Opslaglocatie-inhoud van de opslaglocatie die u wilt instellen als de nieuwe standaardopslaglocatie.</span><span class="sxs-lookup"><span data-stu-id="2efe0-120">Find the bin content line for the bin that you would like as the new default bin.</span></span> <span data-ttu-id="2efe0-121">Schakel het selectievakje **Standaardopslaglocatie** in.</span><span class="sxs-lookup"><span data-stu-id="2efe0-121">Select the **Default Bin** check box.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2efe0-122">Wanneer een artikel voor het eerst wordt opgeslagen terwijl er geen standaardopslaglocatie is toegewezen aan het artikel, wordt de locatie waar het artikel wordt opgeslagen ingesteld als de standaardopslaglocatie voor het artikel.</span><span class="sxs-lookup"><span data-stu-id="2efe0-122">When an item is put away for the first time, and the item does not have a default bin assigned, the system will assign the bin where the item is put away as the default bin for the item.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2efe0-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2efe0-123">See Also</span></span>  
[<span data-ttu-id="2efe0-124">Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="2efe0-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="2efe0-125">Voorraad</span><span class="sxs-lookup"><span data-stu-id="2efe0-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="2efe0-126">[Magazijnbeheer instellen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="2efe0-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="2efe0-127">[Assemblagebeheer](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="2efe0-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="2efe0-128">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="2efe0-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="2efe0-129">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2efe0-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

