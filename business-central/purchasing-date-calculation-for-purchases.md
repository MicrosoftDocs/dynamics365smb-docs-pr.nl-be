---
title: Datumberekening voor inkoop | Microsoft Docs
description: De toepassing berekent automatisch de datum waarop u een artikel moet bestellen zodat u het op een bepaalde datum in voorraad hebt. Dit is de datum waarop u kunt verwachten dat artikelen die op een bepaalde datum zijn besteld beschikbaar zijn om te worden gepickt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 7b39bcd593489e40d218cf29a3d288dd128cce04
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192783"
---
# <a name="date-calculation-for-purchases"></a><span data-ttu-id="d8b7c-104">Datumberekening voor inkoop</span><span class="sxs-lookup"><span data-stu-id="d8b7c-104">Date Calculation for Purchases</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="d8b7c-105">berekent automatisch de datum waarop u een artikel moet bestellen om het op een bepaalde datum in voorraad te hebben.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-105">automatically calculates the date on which you must order an item to have it in inventory on a certain date.</span></span> <span data-ttu-id="d8b7c-106">Dit is de datum waarop u kunt verwachten dat artikelen die op een bepaalde datum zijn besteld beschikbaar zijn om te worden gepickt.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-106">This is the date on which you can expect items ordered on a particular date to be available for picking.</span></span>  

<span data-ttu-id="d8b7c-107">Als u een aangevraagde ontvangstdatum opgeeft op een inkooporder is de berekende besteldatum de datum waarop de order moet worden geplaatst om de artikelen te ontvangen op de datum die u hebt aangevraagd.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-107">If you specify a requested receipt date on a purchase order header, then the calculated order date is the date on which the order must be placed to receive the items on the date that you requested.</span></span> <span data-ttu-id="d8b7c-108">Vervolgens wordt de datum waarop de artikelen beschikbaar zijn om te worden gepickt berekend en ingevoerd in het veld **Verwachte ontvangstdatum**.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-108">Then, the date on which the items are available for picking is calculated and entered in the **Expected Receipt Date** field.</span></span>  

<span data-ttu-id="d8b7c-109">Als u geen aangevraagde ontvangstdatum opgeeft, wordt automatisch de orderdatum op de regel gebruikt voor de berekening van de datum waarop de artikelen naar verwachting worden ontvangen en de datum waarop de artikelen beschikbaar zijn voor picken.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-109">If you do not specify a requested receipt date, then the order date on the line is used as the starting point for calculating the date on which you can expect to receive the items and the date on which the items are available for picking.</span></span>  

## <a name="calculating-with-a-requested-receipt-date"></a><span data-ttu-id="d8b7c-110">Datums berekenen met een verzochte ontvangstdatum</span><span class="sxs-lookup"><span data-stu-id="d8b7c-110">Calculating with a Requested Receipt Date</span></span>  
<span data-ttu-id="d8b7c-111">Als er een aangevraagde ontvangstdatum op de inkooporderregel staat, wordt automatisch deze datum gebruikt als uitgangspunt voor de volgende berekeningen.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-111">If there is a requested receipt date on the purchase order line, then that date is used as the starting point for the following calculations.</span></span>  

- <span data-ttu-id="d8b7c-112">aangevraagde ontvangstdatum - levertermijn = orderdatum</span><span class="sxs-lookup"><span data-stu-id="d8b7c-112">requested receipt date - lead time calculation = order date</span></span>  
- <span data-ttu-id="d8b7c-113">aangevraagde ontvangstdatum + inslagtijd + veiligheidstijd = verwachte ontvangstdatum</span><span class="sxs-lookup"><span data-stu-id="d8b7c-113">requested receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="d8b7c-114">Als u een aangevraagde ontvangstdatum op de inkooporderkop hebt ingevoerd, wordt deze datum gekopieerd naar het bijbehorende veld op alle regels.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-114">If you entered a requested receipt date on the purchase order header, then that date is copied to the corresponding field on all the lines.</span></span> <span data-ttu-id="d8b7c-115">U kunt deze datum op elke orderregel desgewenst wijzigen of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-115">You can change this date on any of the lines, or you can remove the date on the line.</span></span>  

> [!Note]
> <span data-ttu-id="d8b7c-116">Als uw proces is gebaseerd op achterwaartse berekening, bijvoorbeeld als u de gevraagde ontvangstdatum gebruikt om de besteldatum te verkrijgen, raden we u aan datumformules te gebruiken met vaste looptijden, zoals '5D' voor vijf dagen of '1W' voor een week.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-116">If your process is based on backward calculation, for example, if you use the requested receipt date to get the order date, we recommend that you use date formulas that have fixed durations, such as "5D" for five days or "1W" for one week.</span></span> <span data-ttu-id="d8b7c-117">Datumformules zonder vaste duur, zoals 'CW' voor de huidige week of CM voor de huidige maand, kunnen leiden tot onjuiste datumberekeningen.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-117">Date formulas without fixed durations, such as "CW" for current week or CM for current month, can result in incorrect date calculations.</span></span> <span data-ttu-id="d8b7c-118">Zie voor meer informatie over datumformules [Werken met kalenderdatums en -tijden](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="d8b7c-118">For more information about date formulas, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

## <a name="calculating-without-a-requested-delivery-date"></a><span data-ttu-id="d8b7c-119">Datums berekenen zonder verzochte leverdatum</span><span class="sxs-lookup"><span data-stu-id="d8b7c-119">Calculating without a Requested Delivery Date</span></span>  
<span data-ttu-id="d8b7c-120">Als u een inkooporderregel invoert zonder een verzochte leverdatum, wordt in het veld **Orderdatum** op de regel de datum ingevuld uit het veld **Orderdatum** op de inkooporderkop.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-120">If you enter a purchase order line without a requested delivery date, then the **Order Date** field on the line is filled with the date in the **Order Date** field on the purchase order header.</span></span> <span data-ttu-id="d8b7c-121">Dit kan de datum zijn die u hebt ingevoerd of de werkdatum.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-121">This is either the date that you entered or the work date.</span></span> <span data-ttu-id="d8b7c-122">Vervolgens worden automatisch de volgende datums voor de inkooporderregel berekend, met de orderdatum als uitgangspunt.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-122">The following dates are then calculated for the purchase order line, with the order date as the starting point.</span></span>  

- <span data-ttu-id="d8b7c-123">orderdatum + levertermijn = geplande ontvangstdatum</span><span class="sxs-lookup"><span data-stu-id="d8b7c-123">order date + lead time calculation = planned receipt date</span></span>  
- <span data-ttu-id="d8b7c-124">geplande ontvangstdatum + inslagtijd + veiligheidstijd = verwachte ontvangstdatum</span><span class="sxs-lookup"><span data-stu-id="d8b7c-124">planned receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="d8b7c-125">Als u de orderdatum op de regel wijzigt, bijvoorbeeld omdat de artikelen pas later bij de leverancier beschikbaar zijn, worden de relevante datums op de regel automatisch opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-125">If you change the order date on the line, such as when items are not available at your vendor until a later date, then the relevant dates on the line are automatically recalculated.</span></span>  

<span data-ttu-id="d8b7c-126">Als u de orderdatum op de kop wijzigt, wordt deze datum automatisch gekopieerd naar het veld **Order Date** op alle regels en worden alle bijbehorende datumvelden vervolgens opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="d8b7c-126">If you change the order date on the header, then that date is copied to the **Order Date** field on all the lines, and all the related date fields are then recalculated.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d8b7c-127">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d8b7c-127">See Also</span></span>  
 <span data-ttu-id="d8b7c-128">[Datumberekening voor verkoop](sales-date-calculation-for-sales.md) </span><span class="sxs-lookup"><span data-stu-id="d8b7c-128">[Date Calculation for Sales](sales-date-calculation-for-sales.md) </span></span>  
 [<span data-ttu-id="d8b7c-129">Ordertoezeggingsdatums berekenen</span><span class="sxs-lookup"><span data-stu-id="d8b7c-129">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
 <span data-ttu-id="d8b7c-130">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d8b7c-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
