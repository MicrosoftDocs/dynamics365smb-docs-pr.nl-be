---
title: Opslaglocatieaanvulling berekenen | Microsoft Docs
description: Als de vestiging is ingesteld voor het gebruik van gestuurde opslag en pick, worden de prioriteiten van de opslagsjabloon voor de vestiging in aanmerking genomen wanneer de ontvangsten worden opgeslagen.
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
ms.openlocfilehash: e667ca56aa22fafc7fe6d0a4880c419a4272db26
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="calculate-bin-replenishment"></a><span data-ttu-id="34cbb-103">Opslaglocatieaanvulling berekenen</span><span class="sxs-lookup"><span data-stu-id="34cbb-103">Calculate Bin Replenishment</span></span>
<span data-ttu-id="34cbb-104">Als de vestiging is ingesteld voor het gebruik van gestuurde opslag en pick, worden de prioriteiten van de opslagsjabloon voor de vestiging in aanmerking genomen wanneer de ontvangsten worden opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="34cbb-104">When the location is set up to use directed put-away and pick, priorities of the put-away template for the location are taken into account when putting receipts away.</span></span> <span data-ttu-id="34cbb-105">Prioriteiten omvatten de minimale en maximale aantallen van de opslaglocatie-inhoud die zijn vastgesteld voor een bepaalde opslaglocatie en de zonevolgordes.</span><span class="sxs-lookup"><span data-stu-id="34cbb-105">Priorities include the minimum and maximum quantities of bin content that have been fixed for a particular bin, and the bin rankings.</span></span> <span data-ttu-id="34cbb-106">Dus als er in een rustig tempo artikelen worden afgeleverd, worden de meestgebruikte opslaglocaties gevuld met de artikelen.</span><span class="sxs-lookup"><span data-stu-id="34cbb-106">Therefore, if items are arriving at a steady pace, the most-used pick bins will be filled up as they are emptied.</span></span>  

<span data-ttu-id="34cbb-107">De nieuwe voorraad komt echter niet altijd gestaag binnen.</span><span class="sxs-lookup"><span data-stu-id="34cbb-107">But inventory does not always arrive in a steady trickle.</span></span> <span data-ttu-id="34cbb-108">Soms worden artikelen in grote aantallen aangekocht, zodat het bedrijf een korting kan bedingen en soms produceert de productieafdeling een groot aantal artikelen om een lage eenheidsprijs te bewerkstelligen.</span><span class="sxs-lookup"><span data-stu-id="34cbb-108">Sometimes, items are purchased in large quantities so that the company can obtain a rebate, or your production unit might produce a lot of one item to achieve a low unit cost.</span></span> <span data-ttu-id="34cbb-109">In dat geval zullen er lange tijd geen artikelen worden ontvangen in het magazijn en moeten de artikelen van tijd tot tijd worden verplaatst van bulkopslag naar pickopslaglocaties.</span><span class="sxs-lookup"><span data-stu-id="34cbb-109">Then items will not be received in the warehouse again for some time, and the warehouse needs to periodically move items to pick bins from bulk storage areas.</span></span>  

<span data-ttu-id="34cbb-110">Het kan ook voorkomen dat het magazijn op korte termijn een nieuwe voorraad verwacht en dat het bulkopslaggebied hiervoor moet worden leeggemaakt.</span><span class="sxs-lookup"><span data-stu-id="34cbb-110">It could also be that the warehouse is expecting new stock to arrive soon and wants to empty the bulk storage area of items before the new merchandise arrives.</span></span>  

<span data-ttu-id="34cbb-111">Als u aan de bulkopslaglocaties alleen de activiteit **Opslag** hebt toegewezen, waarbij de activiteit **Pick** is niet geselecteerd voor de opslaglocatiesoort, moet u er altijd zelf voor zorgen dat de pickopslaglocaties worden aangevuld. Er worden namelijk geen voorstellen gedaan voor pickactiviteiten uit opslaglocaties.</span><span class="sxs-lookup"><span data-stu-id="34cbb-111">Finally, if you have defined your bulk storage bins with a bin type action **Put Away** only, that is, the bin type does not have the **Pick** action selected, you must always keep your pick bins replenished, since Put Away-type bins are not suggested for a pick of inventory.</span></span>  

## <a name="to-replenish-pick-bins"></a><span data-ttu-id="34cbb-112">U kunt als volgt pickopslaglocaties aanvullen</span><span class="sxs-lookup"><span data-stu-id="34cbb-112">To replenish pick bins</span></span>  
1.  <span data-ttu-id="34cbb-113">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verplaatsingsvoorstel** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="34cbb-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Movement Worksheet**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="34cbb-114">Kies de actie **Opslaglocatieaanvulling berekenen** om de rapportaanvraagpagina te openen.</span><span class="sxs-lookup"><span data-stu-id="34cbb-114">Choose the **Calculate Bin Replenishment** action to open the report request page.</span></span>  
3.  <span data-ttu-id="34cbb-115">Geef in het opvraagvenster voor de batchverwerking criteria op om het aantal aanvullingsvoorstellen te beperken dat wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="34cbb-115">Fill in the batch job request window to limit the scope of the replenishment suggestions that will be calculated.</span></span> <span data-ttu-id="34cbb-116">Wellicht bent u alleen geïnteresseerd in bepaalde artikelen, zones of opslaglocaties.</span><span class="sxs-lookup"><span data-stu-id="34cbb-116">For example, you might be concerned with particular items, zones, or bins.</span></span>  
4.  <span data-ttu-id="34cbb-117">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="34cbb-117">Choose the **OK** button.</span></span> <span data-ttu-id="34cbb-118">Er worden regels gemaakt voor de aanvullingsverplaatsingen die moeten worden uitgevoerd. Dit gebeurt op basis van de voorschriften die zijn opgesteld voor de opslaglocaties en de bijhorende inhoud, zijnde artikelen in de opslaglocaties.</span><span class="sxs-lookup"><span data-stu-id="34cbb-118">Lines are created for the replenishment movements that need to be performed according to the rules that have been set up for the bins and bin contents, that is, items in bins.</span></span>  
5.  <span data-ttu-id="34cbb-119">Als u alle voorgestelde aanvullingen wilt uitvoeren, kiest u de actie **Verplaatsing maken**.</span><span class="sxs-lookup"><span data-stu-id="34cbb-119">If you want to perform all the suggested replenishments, choose the **Create Movement** action.</span></span> <span data-ttu-id="34cbb-120">De magazijnmedewerkers kunnen de instructies bekijken onder het menu-item **Verplaatsingen**, ze uitvoeren en vervolgens registreren.</span><span class="sxs-lookup"><span data-stu-id="34cbb-120">Employees can now find instructions in the **Movements** menu item, carry them out and register them.</span></span>  
6.  <span data-ttu-id="34cbb-121">Als u alleen wilt dat sommige voorstellen worden uitgevoerd, verwijdert u de minder belangrijke regels. Vervolgens maakt u een verplaatsingsinstructie.</span><span class="sxs-lookup"><span data-stu-id="34cbb-121">If you only want some of the suggestions to be performed, delete the lines that are less important and then create a movement.</span></span>  

<span data-ttu-id="34cbb-122">De volgende keer dat u de aanvulling van de opslaglocaties berekent, worden de verwijderde voorstellen automatisch opnieuw gemaakt,op voorwaarde dat deze voorstellen nog steeds geldig zijn.</span><span class="sxs-lookup"><span data-stu-id="34cbb-122">The next time you calculate bin replenishment, the suggestions that you have deleted will be recreated, if they are still valid at that time.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="34cbb-123">Als aan de volgende voorwaarden wordt voldaan voor een artikel:</span><span class="sxs-lookup"><span data-stu-id="34cbb-123">If the following conditions are met for an item:</span></span>  
>   
>  -   <span data-ttu-id="34cbb-124">het artikel heeft een vervaldatum en</span><span class="sxs-lookup"><span data-stu-id="34cbb-124">The item has an expiration date, and</span></span>  
> -   <span data-ttu-id="34cbb-125">Het veld **Picken volgens FEFO** op de vestigingskaart is geselecteerd, en</span><span class="sxs-lookup"><span data-stu-id="34cbb-125">The **Pick According to FEFO** field on the location card is selected, and</span></span>  
> -   <span data-ttu-id="34cbb-126">u gebruikt de functionaliteit **Opslaglocatieaanvulling berekenen**,</span><span class="sxs-lookup"><span data-stu-id="34cbb-126">You use the **Calculate Bin Replenishment** functionality</span></span>  
>   
>  <span data-ttu-id="34cbb-127">zijn de velden **Van zone** en **Van opslaglocatie** leeg, omdat het algoritme waarmee wordt berekend waar vandaan de artikelen worden verplaatst, alleen wordt geactiveerd als u de functie **Verplaatsing maken** activeert.</span><span class="sxs-lookup"><span data-stu-id="34cbb-127">then the **From Zone** and **From Bin** fields will be blank because the algorithm to calculate from where to move the items is triggered only when you activate the **Create Movement** function.</span></span>  

## <a name="see-also"></a><span data-ttu-id="34cbb-128">Zie ook</span><span class="sxs-lookup"><span data-stu-id="34cbb-128">See Also</span></span>  
[<span data-ttu-id="34cbb-129">Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="34cbb-129">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="34cbb-130">Picken op basis van FEFO</span><span class="sxs-lookup"><span data-stu-id="34cbb-130">Picking by FEFO</span></span>](warehouse-picking-by-fefo.md)  
[<span data-ttu-id="34cbb-131">Voorraad</span><span class="sxs-lookup"><span data-stu-id="34cbb-131">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="34cbb-132">[Magazijnbeheer instellen](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="34cbb-132">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="34cbb-133">[Assemblagebeheer](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="34cbb-133">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="34cbb-134">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="34cbb-134">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="34cbb-135">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="34cbb-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

