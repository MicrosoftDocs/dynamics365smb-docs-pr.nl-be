---
title: Opslagsjablonen instellen | Microsoft Docs
description: Dankzij gestuurde opslag en pick kan op elk tijdstip de meest geschikte opslaglocatie worden gevonden. Dit gebeurt op basis van de opslagsjabloon dat u voor het magazijn hebt ingesteld, de opslaglocatievolgorde die u aan de verschillende opslaglocaties hebt toegewezen en de minimum- en maximumaantallen die u voor vaste opslaglocaties hebt ingesteld.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2020
ms.author: edupont
ms.openlocfilehash: 8e6f248768f558f3bc5e12002234ffb56b006759
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3780022"
---
# <a name="set-up-put-away-templates"></a><span data-ttu-id="0ae6e-103">Opslagsjablonen instellen</span><span class="sxs-lookup"><span data-stu-id="0ae6e-103">Set Up Put-away Templates</span></span>

<span data-ttu-id="0ae6e-104">Dankzij gestuurde opslag en pick kan op elk tijdstip de meest geschikte opslaglocatie worden gevonden. Dit gebeurt op basis van de opslagsjabloon dat u voor het magazijn hebt ingesteld, de opslaglocatievolgorde die u aan de verschillende opslaglocaties hebt toegewezen en de minimum- en maximumaantallen die u voor vaste opslaglocaties hebt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="0ae6e-104">With directed put-away and pick functionality, the most appropriate bin for your items at any given time is suggested, according to the put-away template that you have set up for the warehouse, the bin rankings you have given to the bins, and the minimum and maximum quantities that you have set up for fixed bins.</span></span>  

<span data-ttu-id="0ae6e-105">U kunt een aantal opslagsjablonen instellen en er vervolgens een van selecteren als hoofdsjabloon voor opslagactiviteiten in uw magazijn.</span><span class="sxs-lookup"><span data-stu-id="0ae6e-105">You can set up a number of put-away templates and select one of them to govern put-aways in general in your warehouse.</span></span> <span data-ttu-id="0ae6e-106">U kunt ook een bepaalde opslagsjabloon koppelen aan een artikel of SKU waarvoor speciale opslagvereisten gelden.</span><span class="sxs-lookup"><span data-stu-id="0ae6e-106">You can also select a put-away template for any item or stockkeeping unit that might have special put-away requirements.</span></span>  

## <a name="to-set-up-put-away-templates"></a><span data-ttu-id="0ae6e-107">U kunt als volgt opslagsjablonen instellen</span><span class="sxs-lookup"><span data-stu-id="0ae6e-107">To set up put-away templates</span></span>

1. <span data-ttu-id="0ae6e-108">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Opslagsjablonen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="0ae6e-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Put-away Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0ae6e-109">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="0ae6e-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="0ae6e-110">Voer een unieke id in voor de sjabloon die u wilt maken.</span><span class="sxs-lookup"><span data-stu-id="0ae6e-110">Enter a code that is the unique identifier of the template you are about to create.</span></span>  
4. <span data-ttu-id="0ae6e-111">Typ desgewenst een korte omschrijving.</span><span class="sxs-lookup"><span data-stu-id="0ae6e-111">Enter a short description, if you wish.</span></span>  
5. <span data-ttu-id="0ae6e-112">Voer op de eerste regel de opslaglocatievereisten in die u de hoogste prioriteit wilt geven bij opslagactiviteiten in het programma.</span><span class="sxs-lookup"><span data-stu-id="0ae6e-112">Fill in the first line with the bin requirements that you want fulfilled first and foremost when suggesting a put-away.</span></span>

    <span data-ttu-id="0ae6e-113">Als u bijvoorbeeld wilt dat de standaardopslagmethode gebaseerd is op vaste opslaglocaties, kiest u het veld **Vaste opslaglocatie zoeken**.</span><span class="sxs-lookup"><span data-stu-id="0ae6e-113">For example, if want the default put-away method to be based on fixed bins, then choose the **Find Fixed Bin** field.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="0ae6e-114">Op de tweede regel voert u de vereisten in die u van secundair belang acht bij het zoeken naar een opslaglocatie.</span><span class="sxs-lookup"><span data-stu-id="0ae6e-114">Fill in the second line with the bin requirements that would be your second choice to fulfill in finding a bin for put-away.</span></span> <span data-ttu-id="0ae6e-115">De tweede regel wordt alleen gebruikt indien een opslaglocatie die aan de voorwaarden van de eerste regel voldoet niet kan worden gevonden.</span><span class="sxs-lookup"><span data-stu-id="0ae6e-115">The second line is used only if a bin that meets the requirements of the first line cannot be found.</span></span>  
7. <span data-ttu-id="0ae6e-116">Vul de regels in totdat u alle acceptabele plaatsingsvereisten hebt ingevoerd waaraan moet worden voldaan bij de opslag van artikelen.</span><span class="sxs-lookup"><span data-stu-id="0ae6e-116">Continue to fill in the lines until you have described all the acceptable bin placements that you want to use in the put-away process.</span></span>  
8. <span data-ttu-id="0ae6e-117">Schakel het selectievakje **Vrije opslaglocatie zoeken** op de laatste regel van de opslagsjabloon in.</span><span class="sxs-lookup"><span data-stu-id="0ae6e-117">On the last line in the put-away template, select the **Find Floating Bin** check box.</span></span>  

<span data-ttu-id="0ae6e-118">U kunt verschillende opslagsjablonen maken en deze naar wens toepassen.</span><span class="sxs-lookup"><span data-stu-id="0ae6e-118">You can create various put-away templates and then apply them as you see fit.</span></span> <span data-ttu-id="0ae6e-119">Er wordt allereerst rekening gehouden met de opslagsjabloon die u hebt geselecteerd voor het artikel of de SKU.</span><span class="sxs-lookup"><span data-stu-id="0ae6e-119">The put-away template that you selected for the item or stockkeeping unit, if any is used first.</span></span> <span data-ttu-id="0ae6e-120">Als deze velden niet zijn ingevuld, wordt de opslagsjabloon gebruikt die u voor het magazijn hebt geselecteerd op het sneltabblad **Opslaglocatiebeleid** van de vestigingskaart.</span><span class="sxs-lookup"><span data-stu-id="0ae6e-120">If these fields are not filled in, then the put-away template that you selected for the warehouse on the **Bin Policies** FastTab on the location card is used.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0ae6e-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0ae6e-121">See Also</span></span>

[<span data-ttu-id="0ae6e-122">Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="0ae6e-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="0ae6e-123">Voorraad</span><span class="sxs-lookup"><span data-stu-id="0ae6e-123">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="0ae6e-124">Magazijnbeheer instellen</span><span class="sxs-lookup"><span data-stu-id="0ae6e-124">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="0ae6e-125">Assemblagebeheer</span><span class="sxs-lookup"><span data-stu-id="0ae6e-125">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="0ae6e-126">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="0ae6e-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="0ae6e-127">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0ae6e-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
