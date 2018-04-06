---
title: 'Ontwerpdetails: Integratie met voorraad | Microsoft Docs'
description: De module Magazijnbeheer en de module Voorraad kunnen met elkaar communiceren in inventarisatie en in voorraad- of magazijnherwaardering.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: df77e655c58b6eba6f431ef66be3152f56ac634f
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-integration-with-inventory"></a><span data-ttu-id="0f01d-103">Ontwerpdetails: Integratie met voorraad</span><span class="sxs-lookup"><span data-stu-id="0f01d-103">Design Details: Integration with Inventory</span></span>
<span data-ttu-id="0f01d-104">De module Magazijnbeheer en de module Voorraad kunnen met elkaar communiceren in inventarisatie en in voorraad- of magazijnherwaardering.</span><span class="sxs-lookup"><span data-stu-id="0f01d-104">The Warehouse Management application area and the Inventory application area interact with one another in physical inventory and in inventory or warehouse adjustment.</span></span>  
  
## <a name="physical-inventory"></a><span data-ttu-id="0f01d-105">Physical Inventory</span><span class="sxs-lookup"><span data-stu-id="0f01d-105">Physical Inventory</span></span>  
 <span data-ttu-id="0f01d-106">Het venster **Mag.-inventarisatiedagboek** wordt gebruikt met het venster **Inventarisatiedagboek** voor alle geavanceerd magazijnvestigingen.</span><span class="sxs-lookup"><span data-stu-id="0f01d-106">The **Whse. Phys. Inventory Journal** window is used with the **Phys. Inventory Journal** window for all advanced warehouse locations.</span></span> <span data-ttu-id="0f01d-107">De voorraad op het niveau van opslaglocaties wordt berekend en er wordt een afgedrukte lijst geleverd voor de magazijnmedewerker.</span><span class="sxs-lookup"><span data-stu-id="0f01d-107">The inventory on bin level is calculated, and a printed list is provided for the warehouse employee.</span></span> <span data-ttu-id="0f01d-108">Het overzicht toont welke artikelen in welke opslaglocaties moeten worden geteld.</span><span class="sxs-lookup"><span data-stu-id="0f01d-108">The list shows which items in which bins must be counted.</span></span>  
  
 <span data-ttu-id="0f01d-109">De magazijnmedewerker voert het getelde aantal in het venster **Mag.-inventarisatiedagboek** in en boekt vervolgens het dagboek.</span><span class="sxs-lookup"><span data-stu-id="0f01d-109">The warehouse employee enters the counted quantity in the **Whse. Phys. Inventory Journal** window and then posts the journal.</span></span>  
  
 <span data-ttu-id="0f01d-110">Als het getelde aantal groter is dan het aantal op de dagboekregel, wordt een verplaatsing voor dit verschil geboekt van de standaard herwaarderingsopslaglocatie naar de getelde opslaglocatie.</span><span class="sxs-lookup"><span data-stu-id="0f01d-110">If the counted quantity is greater than the quantity on the journal line, a movement is posted for this difference from the default adjustment bin to the counted bin.</span></span> <span data-ttu-id="0f01d-111">Hiermee wordt het aantal in de getelde opslaglocatie verhoogd en het aantal in de standaardherwaarderingsopslaglocatie verlaagd.</span><span class="sxs-lookup"><span data-stu-id="0f01d-111">This increases the quantity in the counted bin and decreases the quantity in the default adjustment bin.</span></span>  
  
 <span data-ttu-id="0f01d-112">Als het getelde aantal kleiner is dan het aantal op de dagboekregel, wordt een verplaatsing voor dit verschil geboekt van de getelde opslaglocatie naar de standaard herwaarderingsopslaglocatie.</span><span class="sxs-lookup"><span data-stu-id="0f01d-112">If the quantity counted is less than the quantity on the journal line, a movement for this difference is posted from the counted bin to the default adjustment bin.</span></span> <span data-ttu-id="0f01d-113">Hiermee wordt het aantal in de getelde opslaglocatie verlaagd en het aantal in de standaardherwaarderingsopslaglocatie verhoogd.</span><span class="sxs-lookup"><span data-stu-id="0f01d-113">This decreases the quantity in the counted bin and increases the quantity in the default adjustment bin.</span></span>  
  
 <span data-ttu-id="0f01d-114">In geavanceerde magazijnconfiguraties wordt de waarde in het veld **Aantal (berekend)** opgehaald uit artikelposten en wordt de waarde in het veld **Aantal (Inventarisatie)** opgehaald uit magazijnposten, met uitzondering van de inhoud van de herwaarderingsopslaglocatie.</span><span class="sxs-lookup"><span data-stu-id="0f01d-114">In advanced warehouse configurations, the value in the **Quantity (Calculated)** field is retrieved from item ledger entries and the value in the **Quantity (Phys. Inventory)** field is retrieved from warehouse entries, excluding the adjustment bin content.</span></span> <span data-ttu-id="0f01d-115">Het veld **Aantal** geeft het verschil aan tussen de eerste twee velden, en moet gelijk zijn aan de inhoud van de correctieopslaglocatie.</span><span class="sxs-lookup"><span data-stu-id="0f01d-115">The **Quantity** field specifies the difference between the first two fields, which should be equal to the contents of the adjustment bin.</span></span>  
  
 <span data-ttu-id="0f01d-116">Wanneer u het inventarisatiedagboek boekt, wordt de voorraad en de standaardherwaarderingsopslaglocatie bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="0f01d-116">When you post the physical inventory journal, the inventory and the default adjustment bin are updated.</span></span>  
  
### <a name="warehouse-adjustments-to-the-item-ledger"></a><span data-ttu-id="0f01d-117">Magazijncorrecties in de artikelpost</span><span class="sxs-lookup"><span data-stu-id="0f01d-117">Warehouse Adjustments to the Item Ledger</span></span>  
 <span data-ttu-id="0f01d-118">U gebruikt het venster **Artikeldagboek** en de functie **Magazijnherwaardering berekenen** om voorraad op de artikelpost aan te passen in overeenstemming met een aanpassing die is gemaakt in het artikelaantal in een magazijnopslaglocatie.</span><span class="sxs-lookup"><span data-stu-id="0f01d-118">You use the **Item Journal** window and the **Calculate Whse. Adjustment** function to adjust inventory on the item ledger in accordance with an adjustment that has been made to the item quantity in a warehouse bin.</span></span> <span data-ttu-id="0f01d-119">Als u een koppeling tussen de voorraad en het magazijn wilt maken, moet u een standaardherwaarderingsopslaglocatie per vestiging definiëren.</span><span class="sxs-lookup"><span data-stu-id="0f01d-119">To create a link between the inventory and the warehouse, you must define a default adjustment bin per location.</span></span>  
  
 <span data-ttu-id="0f01d-120">De standaardcorrectieopslaglocatie registreert artikelen in het magazijn wanneer u een toename voor de voorraad boekt.</span><span class="sxs-lookup"><span data-stu-id="0f01d-120">The default adjustment bin registers items in the warehouse when you post an increase for the inventory.</span></span> <span data-ttu-id="0f01d-121">Als u echter een afname boekt, wordt het aantal op de standaardopslaglocatie ook verlaagd.</span><span class="sxs-lookup"><span data-stu-id="0f01d-121">However, if you post a decrease, the quantity on the default bin is also decreased.</span></span> <span data-ttu-id="0f01d-122">In beide gevallen worden artikelposten en magazijnposten gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0f01d-122">In both cases, item ledger entries and warehouse entries are created.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="0f01d-123">De correctieopslaglocatie wordt niet weergegeven in de beschikbaarheidsberekening.</span><span class="sxs-lookup"><span data-stu-id="0f01d-123">The adjustment bin is not included in the availability calculation.</span></span>  
  
 <span data-ttu-id="0f01d-124">Wanneer u de opslaglocatie-inhoud wilt aanpassen, kunt u het magazijnartikeldagboek gebruiken, van waaruit u het artikelnummer, de zonecode, de opslaglocatiecode en het aantal kunt invoeren die u wilt aanpassen.</span><span class="sxs-lookup"><span data-stu-id="0f01d-124">If you want to adjust the bin content, you can use the warehouse item journal, from which you can enter the item number, zone code, bin code, and quantity that you want to adjust.</span></span>  
  
 <span data-ttu-id="0f01d-125">Als u een positief aantal invoert en de regel boekt, wordt de voorraad die in de opslaglocatie is opgeslagen vergroot en wordt het aantal dat in de standaardherwaarderingsopslaglocatie is opgeslagen, even veel verkleind.</span><span class="sxs-lookup"><span data-stu-id="0f01d-125">If you enter a positive quantity and post the line, then the inventory stored in the bin increases, and the quantity of the default adjustment bin decreases correspondingly.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0f01d-126">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0f01d-126">See Also</span></span>  
 <span data-ttu-id="0f01d-127">[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md) </span><span class="sxs-lookup"><span data-stu-id="0f01d-127">[Design Details: Warehouse Management](design-details-warehouse-management.md) </span></span>  
 [<span data-ttu-id="0f01d-128">Ontwerpdetails: Beschikbaarheid in het magazijn</span><span class="sxs-lookup"><span data-stu-id="0f01d-128">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)
