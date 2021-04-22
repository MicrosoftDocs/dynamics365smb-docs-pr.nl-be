---
title: Automatisch splitsen van bulkgoederen met gestuurde opslag en pick | Microsoft Docs
description: Voor locaties die gebruikmaken van gestuurde opslag en pick, kunt u eenheden opsplitsen in kleinere eenheden wanneer er magazijninstructies worden gemaakt die voldoen aan de eisen met betrekking tot brondocumenten, -productieorders of interne picks en opslag.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0b42d344753a0284d6f9cddc5d488f1e82ef3074
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5782796"
---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a><span data-ttu-id="233cc-103">Automatisch splitsen van bulkgoederen met gestuurde opslag en pick inschakelen</span><span class="sxs-lookup"><span data-stu-id="233cc-103">Enable Automatic Breaking Bulk with Directed Put-away and Pick</span></span>
<span data-ttu-id="233cc-104">Voor locaties die gebruikmaken van gestuurde opslag en pick, kan [!INCLUDE[prod_short](includes/prod_short.md)] in allerlei situaties, bulkgoederen automatisch splitsen (dit houdt in dat een bepaalde eenheid wordt opgesplitst in kleinere eenheden) wanneer er magazijninstructies worden gemaakt die voldoen aan de eisen met betrekking tot brondocumenten, -productieorders of interne picks en opslag.</span><span class="sxs-lookup"><span data-stu-id="233cc-104">For locations that use directed put-away and pick, [!INCLUDE[prod_short](includes/prod_short.md)] can, in various situations, automatically breakbulk, that is, break a larger unit of measure into smaller units of measure, when it creates warehouse instructions that fulfill the needs of source documents, production orders, or internal picks and put-aways.</span></span> <span data-ttu-id="233cc-105">Bulksplitsing betekent soms ook het verzamelen van kleinere eenheden, indien nodig, om te voldoen aan uitgaande verzoeken door de grotere eenheid op het brondocument of de productieorder te splitsen in kleinere eenheden die in het magazijn beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="233cc-105">To breakbulk sometimes also means gathering smaller units of measure, if necessary, to meet outbound requests by breaking the larger unit of measure on the source document or production order into the smaller units of measure that are available in the warehouse.</span></span>   

## <a name="breakbulking-in-picks"></a><span data-ttu-id="233cc-106">Bulksplitsing in picks</span><span class="sxs-lookup"><span data-stu-id="233cc-106">Breakbulking in Picks</span></span>  
<span data-ttu-id="233cc-107">Als u artikelen wilt opslaan in een aantal verschillende eenheden en deze, zo nodig automatisch wilt laten combineren tijdens het pickproces, selecteert u het veld **Breakbulk toestaan** op de vestigingskaart.</span><span class="sxs-lookup"><span data-stu-id="233cc-107">If you want to store items in several different units of measure and allow them to be automatically combined as needed in the picking process, select the **Allow Breakbulk** field on the location card.</span></span>  

<span data-ttu-id="233cc-108">Voor de uitvoering van een taak zoekt de toepassing automatisch naar een artikel in dezelfde maateenheid.</span><span class="sxs-lookup"><span data-stu-id="233cc-108">To fulfill a task, application automatically looks for an item in the same unit of measure.</span></span> <span data-ttu-id="233cc-109">Als deze vorm van het artikel echter niet wordt gevonden en dit veld is geselecteerd, wordt u gevraagd een bepaalde maateenheid op te splitsen in de vereiste maateenheid.</span><span class="sxs-lookup"><span data-stu-id="233cc-109">But if it cannot find this form of the item, and this field is selected, application will suggest that you break a larger unit of measure into the unit of measure that is needed.</span></span>  

<span data-ttu-id="233cc-110">Als het systeem alleen kleinere eenheden kan vinden, wordt u gevraagd artikelen te verzamelen om aan de hoeveelheid op de verzending of productieorder te kunnen voldoen.</span><span class="sxs-lookup"><span data-stu-id="233cc-110">If the system can only find smaller units of measure, it will suggest that you gather items to fulfill the quantity on the shipment or production order.</span></span> <span data-ttu-id="233cc-111">In de praktijk wordt de grotere eenheid op het brondocument opgesplitst in kleinere pickeenheden.</span><span class="sxs-lookup"><span data-stu-id="233cc-111">In effect, it breaks the larger unit of measure on the source document into smaller units for picking.</span></span>  

## <a name="breakbulking-in-put-aways"></a><span data-ttu-id="233cc-112">Bulksplitsing in opslag</span><span class="sxs-lookup"><span data-stu-id="233cc-112">Breakbulking in Put-aways</span></span>  
<span data-ttu-id="233cc-113">Bij de magazijnopslag stelt de toepassing automatisch Plaatsen-actieregels voor in de opslageenheid, bijvoorbeeld stuks, hoewel de artikelen in een andere eenheid arriveren.</span><span class="sxs-lookup"><span data-stu-id="233cc-113">In the warehouse put-away, application automatically suggests Place action lines in the put-away unit of measure, for example, pieces, even though the items arrive in a different unit of measure.</span></span>  

## <a name="breakbulking-in-movements"></a><span data-ttu-id="233cc-114">Bulksplitsing in verplaatsingen</span><span class="sxs-lookup"><span data-stu-id="233cc-114">Breakbulking in Movements</span></span>  
<span data-ttu-id="233cc-115">De toepassing past ook automatisch bulksplitsing toe op aanvullingsverplaatsingen, als u het veld **Breakbulk toestaan** op het sneltabblad **Optie** van de pagina **Opslagloc.-aanvulling** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="233cc-115">The application also breakbulks automatically in replenishment movements, if the **Allow Breakbulk** field is selected on the **Option** FastTab on the **Calculate Bin Replenishment** page.</span></span>  

<span data-ttu-id="233cc-116">U kunt de resultaten van de omzetting van de ene eenheid in de andere weergeven als tussenliggende bulksplitsingsregels in de opslag-, pick- of verplaatsingsinstructies.</span><span class="sxs-lookup"><span data-stu-id="233cc-116">You can view the results of the conversion process from one unit of measure to another as intermediate breakbulk lines in the put-away, pick, or movement instructions.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="233cc-117">Als u het veld **Breakbulkfilter plaatsen** in de kop van de magazijninstructie selecteert, worden de bulksplitsingsregels verborgen wanneer de grotere eenheid volledig wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="233cc-117">If you select the **Set Breakbulk Filter** field on the warehouse instruction header, application will hide the breakbulk lines whenever the larger unit of measure is going to be completely used.</span></span> <span data-ttu-id="233cc-118">Bijvoorbeeld: als een pallet 12 stuks bevat en u alle 12 stuks gaat gebruiken, wordt u gevraagd 1 pallet te nemen en 12 stuks te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="233cc-118">For example, if a pallet is 12 pieces and you are going to use all 12 pieces, the pick will then direct you to take 1 pallet and place 12 pieces.</span></span> <span data-ttu-id="233cc-119">Als u echter maar 9 stuks nodig hebt, worden de opsplitsingsregels niet verborgen, zelfs niet als u het veld **Breakbulkfilter** hebt geselecteerd omdat u de resterende drie stuks ergens in het magazijn moet plaatsen.</span><span class="sxs-lookup"><span data-stu-id="233cc-119">However, if you have to pick only 9 pieces, then the breakbulk lines will not be hidden, even if you have selected the **Breakbulk Filter** field, because you have to place the remaining three pieces somewhere in the warehouse.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="233cc-120">Als u wilt dat uw eenheden optimaal presteren in het magazijn, ook in verband met de bulksplitsingsfunctionaliteit, moet u waar mogelijk proberen om:</span><span class="sxs-lookup"><span data-stu-id="233cc-120">If you want your units of measure to perform optimally in the warehouse, also in connection with the breakbulk functionality, you should wherever possible try to:</span></span>  
>   
> - <span data-ttu-id="233cc-121">De basiseenheid voor een artikel in te stellen als de kleinste eenheid die u denkt nodig te hebben in de magazijnprocessen.</span><span class="sxs-lookup"><span data-stu-id="233cc-121">Set up the base unit of measure for an item as the smallest unit of measure that you expect to handle in your warehouse processes.</span></span>  
> - <span data-ttu-id="233cc-122">Alternatieve eenheden voor het artikel instellen als veelvouden van de basiseenheid.</span><span class="sxs-lookup"><span data-stu-id="233cc-122">Set up your alternative units of measure for the item as multiples of the base unit of measure.</span></span>  

## <a name="see-also"></a><span data-ttu-id="233cc-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="233cc-123">See Also</span></span>  
[<span data-ttu-id="233cc-124">Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="233cc-124">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="233cc-125">Voorraad</span><span class="sxs-lookup"><span data-stu-id="233cc-125">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="233cc-126">[Magazijnbeheer instellen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="233cc-126">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="233cc-127">[Assemblagebeheer](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="233cc-127">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="233cc-128">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="233cc-128">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="233cc-129">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="233cc-129">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]