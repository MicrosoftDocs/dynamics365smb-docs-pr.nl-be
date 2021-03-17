---
title: 'Ontwerpdetails: Voorraadwaardering | Microsoft Docs'
description: Voorraadwaardering is de bepaling van de kostprijs van een voorraadartikel.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 497c2fb891af31af20a6b7a150edd9a9907748e2
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389861"
---
# <a name="design-details-inventory-valuation"></a><span data-ttu-id="8df89-103">Ontwerpdetails: Voorraadwaardering</span><span class="sxs-lookup"><span data-stu-id="8df89-103">Design Details: Inventory Valuation</span></span>
<span data-ttu-id="8df89-104">Voorraadwaardering is de bepaling van de kosten die worden toegewezen aan een voorraadartikel, zoals uitgedrukt met de volgende vergelijking.</span><span class="sxs-lookup"><span data-stu-id="8df89-104">Inventory valuation is the determination of the cost that is assigned to an inventory item, as expressed by the following equation.</span></span>  

<span data-ttu-id="8df89-105">Eindvoorraad = beginvoorraad + netto inkopen - kosten van verkochte goederen</span><span class="sxs-lookup"><span data-stu-id="8df89-105">Ending inventory = beginning inventory + net purchases – cost of goods sold</span></span>  

<span data-ttu-id="8df89-106">De berekening van voorraadwaardering gebruikt het veld **Tot. werk. kosten** van de waardeposten voor het artikel.</span><span class="sxs-lookup"><span data-stu-id="8df89-106">The calculation of inventory valuation uses the **Cost Amount (Actual)** field of the value entries for the item.</span></span> <span data-ttu-id="8df89-107">De posten zijn ingedeeld volgens het boekingssoort dat overeenkomt met de kostenonderdelen, directe kosten, indirecte kosten, verschil, herwaardering en afronding.</span><span class="sxs-lookup"><span data-stu-id="8df89-107">The entries are classified according to the entry type that corresponds to the cost components, direct cost, indirect cost, variance, revaluation, and rounding.</span></span> <span data-ttu-id="8df89-108">Zie [Ontwerpdetails: kostenonderdelen](design-details-cost-components.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8df89-108">For more information, see [Design Details: Cost Components](design-details-cost-components.md).</span></span>  

<span data-ttu-id="8df89-109">Posten worden met elkaar vereffend door vaste vereffening of op basis van de aanname van de algemene kostenstroom die wordt gedefinieerd door de waarderingsmethode.</span><span class="sxs-lookup"><span data-stu-id="8df89-109">Entries are applied against each other, either by the fixed application or according to the general cost-flow assumption defined by the costing method.</span></span> <span data-ttu-id="8df89-110">Eén negatieve voorraadmutatiepost kan worden vereffend met meer dan één positieve post met verschillende boekingsdatums en mogelijk verschillende aanschafkosten.</span><span class="sxs-lookup"><span data-stu-id="8df89-110">One entry of inventory decrease can be applied to more than one increase entry with different posting dates and possibly different acquisition costs.</span></span> <span data-ttu-id="8df89-111">Zie [Ontwerpdetails: artikelvereffening](design-details-item-application.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8df89-111">For more information, see [Design Details: Item Application](design-details-item-application.md).</span></span> <span data-ttu-id="8df89-112">Berekening van de voorraadwaarde voor een bepaalde datum is daarom gebaseerd op het totaliseren van positieve en negatieve waardeposten.</span><span class="sxs-lookup"><span data-stu-id="8df89-112">Therefore, calculation of the inventory value for a given date is based on summing up positive and negative value entries.</span></span>  

## <a name="inventory-valuation-report"></a><span data-ttu-id="8df89-113">Rapport Voorraadwaardering</span><span class="sxs-lookup"><span data-stu-id="8df89-113">Inventory Valuation report</span></span>  
<span data-ttu-id="8df89-114">Voor het berekenen van de voorraadwaarde in de lijst **Voorraadwaardering** wordt eerst de waarde van de voorraad van het artikel berekend op een bepaalde begindatum.</span><span class="sxs-lookup"><span data-stu-id="8df89-114">To calculate the inventory value in the **Inventory Valuation** report, the report begins by calculating the value of the item’s inventory at a given starting date.</span></span> <span data-ttu-id="8df89-115">Vervolgens wordt de waarde van positieve voorraadmutaties opgeteld en wordt de waarde van negatieve voorraadmutaties afgetrokken tot een bepaalde einddatum.</span><span class="sxs-lookup"><span data-stu-id="8df89-115">It then adds the value of inventory increases and subtracts the value of inventory decreases up to a given ending date.</span></span> <span data-ttu-id="8df89-116">Het eindresultaat is de voorraadwaarde op de einddatum.</span><span class="sxs-lookup"><span data-stu-id="8df89-116">The end result is the inventory value on the ending date.</span></span> <span data-ttu-id="8df89-117">De lijst berekent deze waarden door de waarden in het veld **Tot. werk. kosten** in de waardeposten op te tellen, met de boekingsdatums als filters.</span><span class="sxs-lookup"><span data-stu-id="8df89-117">The report calculates these values by summing the values in the **Cost Amount (Actual)** field in the value entries, using the posting dates as filters.</span></span>  

<span data-ttu-id="8df89-118">De afgedrukte lijst geeft altijd de werkelijke bedragen weer, dat wil zeggen, de kosten van posten die als gefactureerd zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="8df89-118">The printed report always shows actual amounts, that is, the cost of entries that have been posted as invoiced.</span></span> <span data-ttu-id="8df89-119">De verwachte kosten van posten die als ontvangen of verzonden zijn geboekt, worden ook in de lijst afgedrukt als u het selectievakje Inclusief verwachte kosten op het sneltabblad Opties inschakelt.</span><span class="sxs-lookup"><span data-stu-id="8df89-119">The report will also print the expected cost of entries that have posted as received or shipped, if you select the Include Expected Cost field on the Options FastTab.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="8df89-120">Waarden in de lijst **Voorraadwaardering** worden gereconcilieerd met de voorraadrekening in het grootboek, wat betekent dat de waardeposten in kwestie naar het grootboek zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="8df89-120">Values in the **Inventory Valuation** report is reconciled with the Inventory account in the general ledger, meaning the value entries in question have been posted to the general ledger.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="8df89-121">Bedragen in de **Waarde**-kolommen van het rapport zijn gebaseerd op de boekingsdatum van transacties voor een artikel.</span><span class="sxs-lookup"><span data-stu-id="8df89-121">Amounts in the **Value** columns of the report are based on the posting date of transactions for an item.</span></span>  

## <a name="inventory-valuation---wip-report"></a><span data-ttu-id="8df89-122">Rapport Voorraadwaardering - OHW</span><span class="sxs-lookup"><span data-stu-id="8df89-122">Inventory Valuation - WIP report</span></span>  
<span data-ttu-id="8df89-123">Een productiebedrijf moet de waarde van drie soorten voorraad bepalen:</span><span class="sxs-lookup"><span data-stu-id="8df89-123">A manufacturing company needs to determine the value of three types of inventory:</span></span>  

* <span data-ttu-id="8df89-124">Voorraad grondstoffen</span><span class="sxs-lookup"><span data-stu-id="8df89-124">Raw Materials inventory</span></span>  
* <span data-ttu-id="8df89-125">OHW-voorraad</span><span class="sxs-lookup"><span data-stu-id="8df89-125">WIP inventory</span></span>  
* <span data-ttu-id="8df89-126">Voorraad eindproducten</span><span class="sxs-lookup"><span data-stu-id="8df89-126">Finished Goods inventory</span></span>  

<span data-ttu-id="8df89-127">De waarde van OHW-vooraad wordt bepaald door de volgende vergelijking:</span><span class="sxs-lookup"><span data-stu-id="8df89-127">The value of WIP inventory is determined by the following equation:</span></span>  

* <span data-ttu-id="8df89-128">Eind-OHW-voorraad = begin-OHW-voorraad + productiekosten - kosten van vervaardigde goederen</span><span class="sxs-lookup"><span data-stu-id="8df89-128">Ending WIP inventory = Beginning WIP inventory + manufacturing costs – cost of goods manufactured</span></span>  

<span data-ttu-id="8df89-129">Voor ingekochte voorraad vormen de waardeposten de basis van de voorraadwaardering.</span><span class="sxs-lookup"><span data-stu-id="8df89-129">As for purchased inventory, the value entries provide the basis of the inventory valuation.</span></span> <span data-ttu-id="8df89-130">De berekening wordt uitgevoerd met de waarden in het veld **Tot. werk. kosten** van het artikel en capaciteitswaardeposten die aan een productieorder zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="8df89-130">The calculation is made using the values in the **Cost Amount (Actual)** field of the item and capacity value entries associated with a production order.</span></span>  

<span data-ttu-id="8df89-131">Het doel van OHW-voorraadwaardering is de waarde te bepalen van de artikelen waarvoor productie nog niet is voltooid op een bepaalde datum.</span><span class="sxs-lookup"><span data-stu-id="8df89-131">The purpose of WIP inventory valuation is to determine the value of the items whose manufacturing has not yet been completed on a given date.</span></span> <span data-ttu-id="8df89-132">De OHW-voorraadwaarde wordt daarom gebaseerd op de waardeposten die gekoppeld zijn aan de verbruiks- en capaciteitsposten.</span><span class="sxs-lookup"><span data-stu-id="8df89-132">Therefore the WIP inventory value is based on the value entries related to the consumption and capacity ledger entries.</span></span> <span data-ttu-id="8df89-133">Verbruikposten moeten volledig worden gefactureerd op de datum van de waardering.</span><span class="sxs-lookup"><span data-stu-id="8df89-133">Consumption ledger entries must be completely invoiced at the date of the valuation.</span></span> <span data-ttu-id="8df89-134">De lijst **Voorraadwaardering - OHW** geeft daarom de kosten voor de OHW-voorraadwaarde in twee categorieën weer: verbruik en capaciteit.</span><span class="sxs-lookup"><span data-stu-id="8df89-134">Therefore, the **Inventory Valuation – WIP** report shows the costs representing the WIP inventory value in two categories: consumption and capacity.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8df89-135">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8df89-135">See Also</span></span>  
<span data-ttu-id="8df89-136">[Ontwerpdetails: Reconciliatie met het grootboek](design-details-reconciliation-with-the-general-ledger.md) </span><span class="sxs-lookup"><span data-stu-id="8df89-136">[Design Details: Reconciliation with the General Ledger](design-details-reconciliation-with-the-general-ledger.md) </span></span>  
<span data-ttu-id="8df89-137">[Ontwerpdetails: Herwaardering](design-details-revaluation.md) </span><span class="sxs-lookup"><span data-stu-id="8df89-137">[Design Details: Revaluation](design-details-revaluation.md) </span></span>  
<span data-ttu-id="8df89-138">[Ontwerpdetails: Productieorderboeking](design-details-production-order-posting.md)
[Voorraadkosten beheren](finance-manage-inventory-costs.md)</span><span class="sxs-lookup"><span data-stu-id="8df89-138">[Design Details: Production Order Posting](design-details-production-order-posting.md)
[Managing Inventory Costs](finance-manage-inventory-costs.md)</span></span>  
[<span data-ttu-id="8df89-139">Financiën</span><span class="sxs-lookup"><span data-stu-id="8df89-139">Finance</span></span>](finance.md)  
<span data-ttu-id="8df89-140">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8df89-140">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]