---
title: Opslagsjablonen instellen | Microsoft Docs
description: Dankzij gestuurde opslag en pick kan op elk tijdstip de meest geschikte opslaglocatie worden gevonden. Dit gebeurt op basis van de opslagsjabloon dat u voor het magazijn hebt ingesteld, de opslaglocatievolgorde die u aan de verschillende opslaglocaties hebt toegewezen en de minimum- en maximumaantallen die u voor vaste opslaglocaties hebt ingesteld.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6b6064bbad133ca521e5cb44667b9ead1368c1e0
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382363"
---
# <a name="set-up-put-away-templates"></a><span data-ttu-id="436da-103">Opslagsjablonen instellen</span><span class="sxs-lookup"><span data-stu-id="436da-103">Set Up Put-away Templates</span></span>

<span data-ttu-id="436da-104">Dankzij gestuurde opslag en pick kan op elk tijdstip de meest geschikte opslaglocatie worden gevonden. Dit gebeurt op basis van de opslagsjabloon dat u voor het magazijn hebt ingesteld, de opslaglocatievolgorde die u aan de verschillende opslaglocaties hebt toegewezen en de minimum- en maximumaantallen die u voor vaste opslaglocaties hebt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="436da-104">With directed put-away and pick functionality, the most appropriate bin for your items at any given time is suggested, according to the put-away template that you have set up for the warehouse, the bin rankings you have given to the bins, and the minimum and maximum quantities that you have set up for fixed bins.</span></span>  

<span data-ttu-id="436da-105">U kunt een aantal opslagsjablonen instellen en er vervolgens een van selecteren als hoofdsjabloon voor opslagactiviteiten in uw magazijn.</span><span class="sxs-lookup"><span data-stu-id="436da-105">You can set up a number of put-away templates and select one of them to govern put-aways in general in your warehouse.</span></span> <span data-ttu-id="436da-106">U kunt ook een bepaalde opslagsjabloon koppelen aan een artikel of SKU waarvoor speciale opslagvereisten gelden.</span><span class="sxs-lookup"><span data-stu-id="436da-106">You can also select a put-away template for any item or stockkeeping unit that might have special put-away requirements.</span></span>  

## <a name="to-set-up-put-away-templates"></a><span data-ttu-id="436da-107">U kunt als volgt opslagsjablonen instellen</span><span class="sxs-lookup"><span data-stu-id="436da-107">To set up put-away templates</span></span>

1. <span data-ttu-id="436da-108">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Opslagsjablonen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="436da-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Put-away Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="436da-109">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="436da-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="436da-110">Voer een unieke id in voor de sjabloon die u wilt maken.</span><span class="sxs-lookup"><span data-stu-id="436da-110">Enter a code that is the unique identifier of the template you are about to create.</span></span>  
4. <span data-ttu-id="436da-111">Typ desgewenst een korte omschrijving.</span><span class="sxs-lookup"><span data-stu-id="436da-111">Enter a short description, if you wish.</span></span>  
5. <span data-ttu-id="436da-112">Voer op de eerste regel de opslaglocatievereisten in die u de hoogste prioriteit wilt geven bij opslagactiviteiten in het programma.</span><span class="sxs-lookup"><span data-stu-id="436da-112">Fill in the first line with the bin requirements that you want fulfilled first and foremost when suggesting a put-away.</span></span>

    <span data-ttu-id="436da-113">Als u bijvoorbeeld wilt dat de standaardopslagmethode gebaseerd is op vaste opslaglocaties, kiest u het veld **Vaste opslaglocatie zoeken**.</span><span class="sxs-lookup"><span data-stu-id="436da-113">For example, if want the default put-away method to be based on fixed bins, then choose the **Find Fixed Bin** field.</span></span> [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="436da-114">Op de tweede regel voert u de vereisten in die u van secundair belang acht bij het zoeken naar een opslaglocatie.</span><span class="sxs-lookup"><span data-stu-id="436da-114">Fill in the second line with the bin requirements that would be your second choice to fulfill in finding a bin for put-away.</span></span> <span data-ttu-id="436da-115">De tweede regel wordt alleen gebruikt indien een opslaglocatie die aan de voorwaarden van de eerste regel voldoet niet kan worden gevonden.</span><span class="sxs-lookup"><span data-stu-id="436da-115">The second line is used only if a bin that meets the requirements of the first line cannot be found.</span></span>  
7. <span data-ttu-id="436da-116">Vul de regels in totdat u alle acceptabele plaatsingsvereisten hebt ingevoerd waaraan moet worden voldaan bij de opslag van artikelen.</span><span class="sxs-lookup"><span data-stu-id="436da-116">Continue to fill in the lines until you have described all the acceptable bin placements that you want to use in the put-away process.</span></span>  
8. <span data-ttu-id="436da-117">Schakel het selectievakje **Vrije opslaglocatie zoeken** op de laatste regel van de opslagsjabloon in.</span><span class="sxs-lookup"><span data-stu-id="436da-117">On the last line in the put-away template, select the **Find Floating Bin** check box.</span></span>  

<span data-ttu-id="436da-118">U kunt verschillende opslagsjablonen maken en deze naar wens toepassen.</span><span class="sxs-lookup"><span data-stu-id="436da-118">You can create various put-away templates and then apply them as you see fit.</span></span> <span data-ttu-id="436da-119">Er wordt allereerst rekening gehouden met de opslagsjabloon die u hebt geselecteerd voor het artikel of de SKU.</span><span class="sxs-lookup"><span data-stu-id="436da-119">The put-away template that you selected for the item or stockkeeping unit, if any is used first.</span></span> <span data-ttu-id="436da-120">Als deze velden niet zijn ingevuld, wordt de opslagsjabloon gebruikt die u voor het magazijn hebt geselecteerd op het sneltabblad **Opslaglocatiebeleid** van de vestigingskaart.</span><span class="sxs-lookup"><span data-stu-id="436da-120">If these fields are not filled in, then the put-away template that you selected for the warehouse on the **Bin Policies** FastTab on the location card is used.</span></span>  

## <a name="see-also"></a><span data-ttu-id="436da-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="436da-121">See Also</span></span>

[<span data-ttu-id="436da-122">Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="436da-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="436da-123">Voorraad</span><span class="sxs-lookup"><span data-stu-id="436da-123">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="436da-124">Magazijnbeheer instellen</span><span class="sxs-lookup"><span data-stu-id="436da-124">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="436da-125">Assemblagebeheer</span><span class="sxs-lookup"><span data-stu-id="436da-125">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="436da-126">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="436da-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="436da-127">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="436da-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]