---
title: Datumberekening voor inkoop | Microsoft Docs
description: Het programma berekent automatisch de datum waarop u een artikel moet bestellen zodat u het op een bepaalde datum in voorraad hebt. Dit is de datum waarop u kunt verwachten dat artikelen die op een bepaalde datum zijn besteld beschikbaar zijn om te worden gepickt.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7a37b1ef9e4a73faf8d04398dbc4023eb04ab9f6
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="date-calculation-for-purchases"></a><span data-ttu-id="fd5a7-104">Datumberekening voor inkoop</span><span class="sxs-lookup"><span data-stu-id="fd5a7-104">Date Calculation for Purchases</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="fd5a7-105"> berekent automatisch de datum waarop u een artikel moet bestellen om het op een bepaalde datum in voorraad te hebben.</span><span class="sxs-lookup"><span data-stu-id="fd5a7-105"> automatically calculates the date on which you must order an item to have it in inventory on a certain date.</span></span> <span data-ttu-id="fd5a7-106">Dit is de datum waarop u kunt verwachten dat artikelen die op een bepaalde datum zijn besteld beschikbaar zijn om te worden gepickt.</span><span class="sxs-lookup"><span data-stu-id="fd5a7-106">This is the date on which you can expect items ordered on a particular date to be available for picking.</span></span>  

<span data-ttu-id="fd5a7-107">Als u een aangevraagde ontvangstdatum opgeeft op een inkooporder is de berekende besteldatum de datum waarop de order moet worden geplaatst om de artikelen te ontvangen op de datum die u hebt aangevraagd.</span><span class="sxs-lookup"><span data-stu-id="fd5a7-107">If you specify a requested receipt date on a purchase order header, then the calculated order date is the date on which the order must be placed to receive the items on the date that you requested.</span></span> <span data-ttu-id="fd5a7-108">Vervolgens wordt de datum waarop de artikelen beschikbaar zijn om te worden gepickt berekend en ingevoerd in het veld **Verwachte ontvangstdatum**.</span><span class="sxs-lookup"><span data-stu-id="fd5a7-108">Then, the date on which the items are available for picking is calculated and entered in the **Expected Receipt Date** field.</span></span>  

<span data-ttu-id="fd5a7-109">Als u geen aangevraagde ontvangstdatum opgeeft, wordt automatisch de orderdatum op de regel gebruikt voor de berekening van de datum waarop de artikelen naar verwachting worden ontvangen en de datum waarop de artikelen beschikbaar zijn voor picken.</span><span class="sxs-lookup"><span data-stu-id="fd5a7-109">If you do not specify a requested receipt date, then the order date on the line is used as the starting point for calculating the date on which you can expect to receive the items and the date on which the items are available for picking.</span></span>  

## <a name="calculating-with-a-requested-receipt-date"></a><span data-ttu-id="fd5a7-110">Datums berekenen met een verzochte ontvangstdatum</span><span class="sxs-lookup"><span data-stu-id="fd5a7-110">Calculating with a Requested Receipt Date</span></span>  
<span data-ttu-id="fd5a7-111">Als er een aangevraagde ontvangstdatum op de inkooporderregel staat, wordt automatisch deze datum gebruikt als uitgangspunt voor de volgende berekeningen.</span><span class="sxs-lookup"><span data-stu-id="fd5a7-111">If there is a requested receipt date on the purchase order line, then that date is used as the starting point for the following calculations.</span></span>  

- <span data-ttu-id="fd5a7-112">aangevraagde ontvangstdatum - levertermijn = orderdatum</span><span class="sxs-lookup"><span data-stu-id="fd5a7-112">requested receipt date - lead time calculation = order date</span></span>  
- <span data-ttu-id="fd5a7-113">aangevraagde ontvangstdatum + inslagtijd + veiligheidstijd = verwachte ontvangstdatum</span><span class="sxs-lookup"><span data-stu-id="fd5a7-113">requested receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="fd5a7-114">Als u een aangevraagde ontvangstdatum op de inkooporderkop hebt ingevoerd, wordt deze datum gekopieerd naar het bijbehorende veld op alle regels.</span><span class="sxs-lookup"><span data-stu-id="fd5a7-114">If you entered a requested receipt date on the purchase order header, then that date is copied to the corresponding field on all the lines.</span></span> <span data-ttu-id="fd5a7-115">U kunt deze datum op elke orderregel desgewenst wijzigen of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="fd5a7-115">You can change this date on any of the lines, or you can remove the date on the line.</span></span>  

## <a name="calculating-without-a-requested-delivery-date"></a><span data-ttu-id="fd5a7-116">Datums berekenen zonder verzochte leverdatum</span><span class="sxs-lookup"><span data-stu-id="fd5a7-116">Calculating without a Requested Delivery Date</span></span>  
<span data-ttu-id="fd5a7-117">Als u een inkooporderregel invoert zonder een verzochte leverdatum, wordt in het veld **Orderdatum** op de regel de datum ingevuld uit het veld **Orderdatum** op de inkooporderkop.</span><span class="sxs-lookup"><span data-stu-id="fd5a7-117">If you enter a purchase order line without a requested delivery date, then the **Order Date** field on the line is filled with the date in the **Order Date** field on the purchase order header.</span></span> <span data-ttu-id="fd5a7-118">Dit kan de datum zijn die u hebt ingevoerd of de werkdatum.</span><span class="sxs-lookup"><span data-stu-id="fd5a7-118">This is either the date that you entered or the work date.</span></span> <span data-ttu-id="fd5a7-119">Vervolgens worden automatisch de volgende datums voor de inkooporderregel berekend, met de orderdatum als uitgangspunt.</span><span class="sxs-lookup"><span data-stu-id="fd5a7-119">The following dates are then calculated for the purchase order line, with the order date as the starting point.</span></span>  

- <span data-ttu-id="fd5a7-120">orderdatum + levertermijn = geplande ontvangstdatum</span><span class="sxs-lookup"><span data-stu-id="fd5a7-120">order date + lead time calculation = planned receipt date</span></span>  
- <span data-ttu-id="fd5a7-121">geplande ontvangstdatum + inslagtijd + veiligheidstijd = verwachte ontvangstdatum</span><span class="sxs-lookup"><span data-stu-id="fd5a7-121">planned receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="fd5a7-122">Als u de orderdatum op de regel wijzigt, bijvoorbeeld omdat de artikelen pas later bij de leverancier beschikbaar zijn, worden de relevante datums op de regel automatisch opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="fd5a7-122">If you change the order date on the line, such as when items are not available at your vendor until a later date, then the relevant dates on the line are automatically recalculated.</span></span>  

<span data-ttu-id="fd5a7-123">Als u de orderdatum op de kop wijzigt, wordt deze datum automatisch gekopieerd naar het veld **Order Date** op alle regels en worden alle bijbehorende datumvelden vervolgens opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="fd5a7-123">If you change the order date on the header, then that date is copied to the **Order Date** field on all the lines, and all the related date fields are then recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fd5a7-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="fd5a7-124">See Also</span></span>  
 <span data-ttu-id="fd5a7-125">[Datumberekening voor verkoop](sales-date-calculation-for-sales.md) </span><span class="sxs-lookup"><span data-stu-id="fd5a7-125">[Date Calculation for Sales](sales-date-calculation-for-sales.md) </span></span>  
 [<span data-ttu-id="fd5a7-126">Ordertoezeggingsdatums berekenen</span><span class="sxs-lookup"><span data-stu-id="fd5a7-126">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="fd5a7-127">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fd5a7-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

