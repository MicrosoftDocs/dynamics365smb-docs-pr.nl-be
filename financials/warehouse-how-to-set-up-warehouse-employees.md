---
title: Magazijnmedewerkers instellen | Microsoft Docs
description: "Elke gebruiker die magazijnactiviteiten uitvoert, moet als magazijnmedewerker worden ingesteld op één standaardlocatie en eventueel meer niet-standaardlocaties."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 45a5f7e2140bffd192ecb586e45cc44894752656
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-warehouse-employees"></a><span data-ttu-id="8f06d-103">Magazijnmedewerkers instellen</span><span class="sxs-lookup"><span data-stu-id="8f06d-103">Set Up Warehouse Employees</span></span>
<span data-ttu-id="8f06d-104">Elke gebruiker die magazijnactiviteiten uitvoert, moet als magazijnmedewerker worden ingesteld op één standaardlocatie en eventueel meer niet-standaardlocaties.</span><span class="sxs-lookup"><span data-stu-id="8f06d-104">Each user who performs warehouse activities must be set up as a warehouse employee assigned to one default location and potentially more non-default locations.</span></span> <span data-ttu-id="8f06d-105">Met behulp van deze standaardinstellingen worden alle magazijnactiviteiten in de gehele database naar de locatie van de medewerker gefilterd, zodat de medewerker de magazijnactiviteiten alleen op de standaardlocatie kan uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="8f06d-105">This user setup filters all warehouse activities across the database to the employee's location so that the employee can only perform the warehouse activities at the default location.</span></span> <span data-ttu-id="8f06d-106">Een gebruiker kan aan extra, niet-standaardlocaties worden toegewezen, waarvoor de medewerker activiteitsregels kan weergeven, maar de activiteiten zelf niet kan uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="8f06d-106">A user can be assigned to additional non-default locations for which the employee can view activity lines but not perform the activities.</span></span>

## <a name="to-set-up-warehouse-employees"></a><span data-ttu-id="8f06d-107">Magazijnmedewerkers instellen</span><span class="sxs-lookup"><span data-stu-id="8f06d-107">To set up warehouse employees</span></span>  
1.  <span data-ttu-id="8f06d-108">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Magazijnwerknemers** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="8f06d-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8f06d-109">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="8f06d-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="8f06d-110">Selecteer het veld **Gebruikers-id** en selecteer vervolgens de gebruiker die als een magazijnwerknemer moet worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="8f06d-110">Select the **User ID** field, and then select the user to be added as a warehouse employee.</span></span> <span data-ttu-id="8f06d-111">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="8f06d-111">Choose the **OK** button.</span></span>  
6.  <span data-ttu-id="8f06d-112">Voer in het veld **Vestigingscode** de code in van de vestiging waar de gebruiker gaat werken.</span><span class="sxs-lookup"><span data-stu-id="8f06d-112">In the **Location Code** field, enter the code of the location where the user will be working.</span></span>  
7.  <span data-ttu-id="8f06d-113">Schakel het selectievakje **Standaard** om om de vestiging vast te leggen als enige vestiging waar de medewerker magazijnactiviteiten mag uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="8f06d-113">Select the **Default** check box to define the location as the only location where the employee can perform warehouse activities.</span></span>  
8.  <span data-ttu-id="8f06d-114">Herhaal deze stappen als u meer medewerkers aan vestigingen wilt toewijzen of als u niet-standaardvestigingen wilt toewijzen aan bestaande magazijnmedewerkers.</span><span class="sxs-lookup"><span data-stu-id="8f06d-114">Repeat these steps to assign other employees to locations or assign non-default locations to existing warehouse employees.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8f06d-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8f06d-115">See Also</span></span>  
[<span data-ttu-id="8f06d-116">Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="8f06d-116">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="8f06d-117">Voorraad</span><span class="sxs-lookup"><span data-stu-id="8f06d-117">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="8f06d-118">[Magazijnbeheer instellen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="8f06d-118">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="8f06d-119">[Assemblagebeheer](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="8f06d-119">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="8f06d-120">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="8f06d-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="8f06d-121">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8f06d-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

