---
title: Standaardopslaglocaties aan artikelen toewijzen | Microsoft Docs
description: Indien u op een locatie met opslaglocaties werkt, kan het toewijzen van standaardopslaglocaties aan uw artikelen het verzenden, ontvangen en verplaatsen van artikelen veel eenvoudiger maken. Wanneer een standaard opslaglocatie is toegewezen aan een artikel, wordt elke keer dat u een transactie voor dit artikel opstart deze opslaglocatie voorgesteld.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2075010c892893d28c7ae3fe627709669bc80a38
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="assign-default-bins-to-items"></a><span data-ttu-id="f3f96-104">Standaardopslaglocaties aan artikelen toewijzen</span><span class="sxs-lookup"><span data-stu-id="f3f96-104">Assign Default Bins to Items</span></span>
<span data-ttu-id="f3f96-105">Indien u op een locatie met opslaglocaties werkt, kan het toewijzen van standaardopslaglocaties aan uw artikelen het verzenden, ontvangen en verplaatsen van artikelen veel eenvoudiger maken.</span><span class="sxs-lookup"><span data-stu-id="f3f96-105">If you are using bins at a location, assigning default bins to your items can make the process of shipping, receiving, and moving your items much easier.</span></span> <span data-ttu-id="f3f96-106">Wanneer een standaard opslaglocatie is toegewezen aan een artikel, wordt elke keer dat u een transactie voor dit artikel opstart deze opslaglocatie voorgesteld.</span><span class="sxs-lookup"><span data-stu-id="f3f96-106">When a default bin is assigned to an item, this bin is suggested every time you initiate a transaction for this item.</span></span> <span data-ttu-id="f3f96-107">Standaardopslaglocaties worden gedefinieerd in het venster **Opslaglocatie-inhoud**.</span><span class="sxs-lookup"><span data-stu-id="f3f96-107">Default bins are defined in the **Bin Content** window.</span></span>  

## <a name="to-assign-a-default-bin-to-an-item"></a><span data-ttu-id="f3f96-108">Een standaardopslaglocatie toewijzen aan een artikel</span><span class="sxs-lookup"><span data-stu-id="f3f96-108">To assign a default bin to an item</span></span>
1.  <span data-ttu-id="f3f96-109">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Voorstel opslaglocatie-inhoudaanmaak** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="f3f96-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bin Content Creation Worksheet**, and choose the related link.</span></span>  
2.  <span data-ttu-id="f3f96-110">Vul de opslaglocatiecode en het artikel in voor elke opslaglocatie die u wilt instellen als standaardwaarde voor een artikel.</span><span class="sxs-lookup"><span data-stu-id="f3f96-110">Fill in the bin code and item information for each bin that you would like to set up as a default for an item.</span></span> <span data-ttu-id="f3f96-111">Selecteer het veld **Standaard**.</span><span class="sxs-lookup"><span data-stu-id="f3f96-111">Make sure to select the **Default** field.</span></span>  
3.  <span data-ttu-id="f3f96-112">Kies de actie **Opslaglocatie-inhoud maken**.</span><span class="sxs-lookup"><span data-stu-id="f3f96-112">Choose the **Create Bin Content** action.</span></span> <span data-ttu-id="f3f96-113">Er worden nu standaardopslaglocaties voor uw artikel toegewezen.</span><span class="sxs-lookup"><span data-stu-id="f3f96-113">Default bins are now assigned for your item.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f3f96-114">Wanneer een artikel wordt opgeslagen terwijl er voor het artikel geen standaardopslaglocatie is toegewezen, wordt de locatie waar het artikel wordt opgeslagen toegewezen als de standaardopslaglocatie.</span><span class="sxs-lookup"><span data-stu-id="f3f96-114">When an item is put away, if the item does not have a default bin assigned, the bin where the item is put away is assigned as the default.</span></span>  

## <a name="to-change-the-default-bin-for-an-item"></a><span data-ttu-id="f3f96-115">De standaardopslaglocatie voor een artikel wijzigen</span><span class="sxs-lookup"><span data-stu-id="f3f96-115">To change the default bin for an item</span></span>  
<span data-ttu-id="f3f96-116">Soms moet u de standaardtoewijzing van de opslaglocatie voor een bepaald artikel wijzigen of een standaardopslaglocatie toewijzen aan een nieuw artikel.</span><span class="sxs-lookup"><span data-stu-id="f3f96-116">You may need to change the default bin assignment for an item or assign a default bin to a new item.</span></span>    
1.  <span data-ttu-id="f3f96-117">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Opslaglocatie-inhoud** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="f3f96-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bin Contents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f3f96-118">Selecteer de juiste vestiging in het veld **Vestigingsfilter**.</span><span class="sxs-lookup"><span data-stu-id="f3f96-118">In the **Location Filter** field, select the appropriate location code.</span></span>  
3.  <span data-ttu-id="f3f96-119">Zoek naar de huidige inhoudspost van de standaardopslaglocatie voor het artikel en schakel het selectievakje **Standaardopslaglocatie** uit.</span><span class="sxs-lookup"><span data-stu-id="f3f96-119">Find the current default bin content entry for the item and clear the **Default Bin** check box.</span></span>  
4.  <span data-ttu-id="f3f96-120">Zoek naar de regel Opslaglocatie-inhoud van de opslaglocatie die u wilt instellen als de nieuwe standaardopslaglocatie.</span><span class="sxs-lookup"><span data-stu-id="f3f96-120">Find the bin content line for the bin that you would like as the new default bin.</span></span> <span data-ttu-id="f3f96-121">Schakel het selectievakje **Standaardopslaglocatie** in.</span><span class="sxs-lookup"><span data-stu-id="f3f96-121">Select the **Default Bin** check box.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f3f96-122">Wanneer een artikel voor het eerst wordt opgeslagen terwijl er geen standaardopslaglocatie is toegewezen aan het artikel, wordt de locatie waar het artikel wordt opgeslagen ingesteld als de standaardopslaglocatie voor het artikel.</span><span class="sxs-lookup"><span data-stu-id="f3f96-122">When an item is put away for the first time, and the item does not have a default bin assigned, the system will assign the bin where the item is put away as the default bin for the item.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f3f96-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f3f96-123">See Also</span></span>  
[<span data-ttu-id="f3f96-124">Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="f3f96-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="f3f96-125">Voorraad</span><span class="sxs-lookup"><span data-stu-id="f3f96-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="f3f96-126">[Magazijnbeheer instellen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="f3f96-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="f3f96-127">[Assemblagebeheer](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="f3f96-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="f3f96-128">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="f3f96-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="f3f96-129">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f3f96-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

