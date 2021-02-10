---
title: Standaardopslaglocaties aan artikelen toewijzen | Microsoft Docs
description: Indien u op een locatie met opslaglocaties werkt, kan het toewijzen van standaardopslaglocaties aan uw artikelen het verzenden, ontvangen en verplaatsen van artikelen veel eenvoudiger maken. Wanneer een standaard opslaglocatie is toegewezen aan een artikel, wordt elke keer dat u een transactie voor dit artikel opstart deze opslaglocatie voorgesteld.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f3374929434876cee088f046efc6d5f950671cc8
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756329"
---
# <a name="assign-default-bins-to-items"></a><span data-ttu-id="0d433-104">Standaardopslaglocaties aan artikelen toewijzen</span><span class="sxs-lookup"><span data-stu-id="0d433-104">Assign Default Bins to Items</span></span>
<span data-ttu-id="0d433-105">Indien u op een locatie met opslaglocaties werkt, kan het toewijzen van standaardopslaglocaties aan uw artikelen het verzenden, ontvangen en verplaatsen van artikelen veel eenvoudiger maken.</span><span class="sxs-lookup"><span data-stu-id="0d433-105">If you are using bins at a location, assigning default bins to your items can make the process of shipping, receiving, and moving your items much easier.</span></span> <span data-ttu-id="0d433-106">Wanneer een standaard opslaglocatie is toegewezen aan een artikel, wordt elke keer dat u een transactie voor dit artikel opstart deze opslaglocatie voorgesteld.</span><span class="sxs-lookup"><span data-stu-id="0d433-106">When a default bin is assigned to an item, this bin is suggested every time you initiate a transaction for this item.</span></span> <span data-ttu-id="0d433-107">Standaardopslaglocaties worden gedefinieerd op de pagina **Opslaglocatie-inhoud**.</span><span class="sxs-lookup"><span data-stu-id="0d433-107">Default bins are defined on the **Bin Content** page.</span></span>  

## <a name="to-assign-a-default-bin-to-an-item"></a><span data-ttu-id="0d433-108">Een standaardopslaglocatie toewijzen aan een artikel</span><span class="sxs-lookup"><span data-stu-id="0d433-108">To assign a default bin to an item</span></span>
1.  <span data-ttu-id="0d433-109">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorstel opslaglocatie-inhoudaanmaak** in en kies vervolgens de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="0d433-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bin Content Creation Worksheet**, and choose the related link.</span></span>  
2.  <span data-ttu-id="0d433-110">Vul de opslaglocatiecode en het artikel in voor elke opslaglocatie die u wilt instellen als standaardwaarde voor een artikel.</span><span class="sxs-lookup"><span data-stu-id="0d433-110">Fill in the bin code and item information for each bin that you would like to set up as a default for an item.</span></span> <span data-ttu-id="0d433-111">Selecteer het veld **Standaard**.</span><span class="sxs-lookup"><span data-stu-id="0d433-111">Make sure to select the **Default** field.</span></span>  
3.  <span data-ttu-id="0d433-112">Kies de actie **Opslaglocatie-inhoud maken**.</span><span class="sxs-lookup"><span data-stu-id="0d433-112">Choose the **Create Bin Content** action.</span></span> <span data-ttu-id="0d433-113">Er worden nu standaardopslaglocaties voor uw artikel toegewezen.</span><span class="sxs-lookup"><span data-stu-id="0d433-113">Default bins are now assigned for your item.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0d433-114">Wanneer een artikel wordt opgeslagen terwijl er voor het artikel geen standaardopslaglocatie is toegewezen, wordt de locatie waar het artikel wordt opgeslagen toegewezen als de standaardopslaglocatie.</span><span class="sxs-lookup"><span data-stu-id="0d433-114">When an item is put away, if the item does not have a default bin assigned, the bin where the item is put away is assigned as the default.</span></span>  

## <a name="to-change-the-default-bin-for-an-item"></a><span data-ttu-id="0d433-115">De standaardopslaglocatie voor een artikel wijzigen</span><span class="sxs-lookup"><span data-stu-id="0d433-115">To change the default bin for an item</span></span>  
<span data-ttu-id="0d433-116">Soms moet u de standaardtoewijzing van de opslaglocatie voor een bepaald artikel wijzigen of een standaardopslaglocatie toewijzen aan een nieuw artikel.</span><span class="sxs-lookup"><span data-stu-id="0d433-116">You may need to change the default bin assignment for an item or assign a default bin to a new item.</span></span>    
1.  <span data-ttu-id="0d433-117">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Opslaglocatie-inhoud** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="0d433-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bin Contents**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="0d433-118">Selecteer de juiste vestiging in het veld **Vestigingsfilter**.</span><span class="sxs-lookup"><span data-stu-id="0d433-118">In the **Location Filter** field, select the appropriate location code.</span></span>  
3.  <span data-ttu-id="0d433-119">Zoek naar de huidige inhoudspost van de standaardopslaglocatie voor het artikel en schakel het selectievakje **Standaardopslaglocatie** uit.</span><span class="sxs-lookup"><span data-stu-id="0d433-119">Find the current default bin content entry for the item and clear the **Default Bin** check box.</span></span>  
4.  <span data-ttu-id="0d433-120">Zoek naar de regel Opslaglocatie-inhoud van de opslaglocatie die u wilt instellen als de nieuwe standaardopslaglocatie.</span><span class="sxs-lookup"><span data-stu-id="0d433-120">Find the bin content line for the bin that you would like as the new default bin.</span></span> <span data-ttu-id="0d433-121">Schakel het selectievakje **Standaardopslaglocatie** in.</span><span class="sxs-lookup"><span data-stu-id="0d433-121">Select the **Default Bin** check box.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0d433-122">Wanneer een artikel voor het eerst wordt opgeslagen terwijl er geen standaardopslaglocatie is toegewezen aan het artikel, wordt de locatie waar het artikel wordt opgeslagen ingesteld als de standaardopslaglocatie voor het artikel.</span><span class="sxs-lookup"><span data-stu-id="0d433-122">When an item is put away for the first time, and the item does not have a default bin assigned, the system will assign the bin where the item is put away as the default bin for the item.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0d433-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0d433-123">See Also</span></span>  
[<span data-ttu-id="0d433-124">Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="0d433-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="0d433-125">Voorraad</span><span class="sxs-lookup"><span data-stu-id="0d433-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="0d433-126">[Magazijnbeheer instellen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="0d433-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="0d433-127">[Assemblagebeheer](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="0d433-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="0d433-128">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="0d433-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="0d433-129">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0d433-129">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
