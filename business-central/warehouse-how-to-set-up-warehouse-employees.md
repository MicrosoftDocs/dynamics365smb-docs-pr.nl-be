---
title: Magazijnmedewerkers instellen | Microsoft Docs
description: Elke gebruiker die magazijnactiviteiten uitvoert, moet als magazijnmedewerker worden ingesteld op één standaardlocatie en eventueel meer niet-standaardlocaties.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4a2ebf2d28833b9cb79c5711fd0314134dfc0915
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784179"
---
# <a name="set-up-warehouse-employees"></a><span data-ttu-id="5e9a7-103">Magazijnmedewerkers instellen</span><span class="sxs-lookup"><span data-stu-id="5e9a7-103">Set Up Warehouse Employees</span></span>
<span data-ttu-id="5e9a7-104">Elke gebruiker die magazijnactiviteiten uitvoert, moet als magazijnmedewerker worden ingesteld op één standaardlocatie en eventueel meer niet-standaardlocaties.</span><span class="sxs-lookup"><span data-stu-id="5e9a7-104">Each user who performs warehouse activities must be set up as a warehouse employee assigned to one default location and potentially more non-default locations.</span></span> <span data-ttu-id="5e9a7-105">Met behulp van deze standaardinstellingen worden alle magazijnactiviteiten in de gehele database naar de locatie van de medewerker gefilterd, zodat de medewerker de magazijnactiviteiten alleen op de standaardlocatie kan uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="5e9a7-105">This user setup filters all warehouse activities across the database to the employee's location so that the employee can only perform the warehouse activities at the default location.</span></span> <span data-ttu-id="5e9a7-106">Een gebruiker kan aan extra, niet-standaardlocaties worden toegewezen, waarvoor de medewerker activiteitsregels kan weergeven, maar de activiteiten zelf niet kan uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="5e9a7-106">A user can be assigned to additional non-default locations for which the employee can view activity lines but not perform the activities.</span></span>

## <a name="to-set-up-warehouse-employees"></a><span data-ttu-id="5e9a7-107">Magazijnmedewerkers instellen</span><span class="sxs-lookup"><span data-stu-id="5e9a7-107">To set up warehouse employees</span></span>  
1.  <span data-ttu-id="5e9a7-108">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnmedewerkers** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="5e9a7-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
2. <span data-ttu-id="5e9a7-109">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="5e9a7-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="5e9a7-110">Selecteer het veld **Gebruikers-id** en selecteer vervolgens de gebruiker die als een magazijnwerknemer moet worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="5e9a7-110">Select the **User ID** field, and then select the user to be added as a warehouse employee.</span></span> <span data-ttu-id="5e9a7-111">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="5e9a7-111">Choose the **OK** button.</span></span>  
6.  <span data-ttu-id="5e9a7-112">Voer in het veld **Vestigingscode** de code in van de vestiging waar de gebruiker gaat werken.</span><span class="sxs-lookup"><span data-stu-id="5e9a7-112">In the **Location Code** field, enter the code of the location where the user will be working.</span></span>  
7.  <span data-ttu-id="5e9a7-113">Schakel het selectievakje **Standaard** om om de vestiging vast te leggen als enige vestiging waar de medewerker magazijnactiviteiten mag uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="5e9a7-113">Select the **Default** check box to define the location as the only location where the employee can perform warehouse activities.</span></span>  
8.  <span data-ttu-id="5e9a7-114">Herhaal deze stappen als u meer medewerkers aan vestigingen wilt toewijzen of als u niet-standaardvestigingen wilt toewijzen aan bestaande magazijnmedewerkers.</span><span class="sxs-lookup"><span data-stu-id="5e9a7-114">Repeat these steps to assign other employees to locations or assign non-default locations to existing warehouse employees.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5e9a7-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5e9a7-115">See Also</span></span>  
[<span data-ttu-id="5e9a7-116">Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="5e9a7-116">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="5e9a7-117">Voorraad</span><span class="sxs-lookup"><span data-stu-id="5e9a7-117">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="5e9a7-118">[Magazijnbeheer instellen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="5e9a7-118">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="5e9a7-119">[Assemblagebeheer](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="5e9a7-119">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="5e9a7-120">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="5e9a7-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="5e9a7-121">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5e9a7-121">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]