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
ms.date: 07/16/2020
ms.author: edupont
ms.openlocfilehash: 092b76b7b25958b0df7155c335d7567c2b92fbf9
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783186"
---
# <a name="date-calculation-for-purchases"></a><span data-ttu-id="0545e-104">Datumberekening voor inkoop</span><span class="sxs-lookup"><span data-stu-id="0545e-104">Date Calculation for Purchases</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="0545e-105">berekent automatisch de datum waarop u een artikel moet bestellen om het op een bepaalde datum in voorraad te hebben.</span><span class="sxs-lookup"><span data-stu-id="0545e-105">automatically calculates the date on which you must order an item to have it in inventory on a certain date.</span></span> <span data-ttu-id="0545e-106">Dit is de datum waarop u kunt verwachten dat artikelen die op een bepaalde datum zijn besteld beschikbaar zijn om te worden gepickt.</span><span class="sxs-lookup"><span data-stu-id="0545e-106">This is the date on which you can expect items ordered on a particular date to be available for picking.</span></span>  

<span data-ttu-id="0545e-107">Als u een aangevraagde ontvangstdatum opgeeft op een inkooporder is de berekende besteldatum de datum waarop de order moet worden geplaatst om de artikelen te ontvangen op de datum die u hebt aangevraagd.</span><span class="sxs-lookup"><span data-stu-id="0545e-107">If you specify a requested receipt date on a purchase order header, then the calculated order date is the date on which the order must be placed to receive the items on the date that you requested.</span></span> <span data-ttu-id="0545e-108">Vervolgens wordt de datum waarop de artikelen beschikbaar zijn om te worden gepickt berekend en ingevoerd in het veld **Verwachte ontvangstdatum**.</span><span class="sxs-lookup"><span data-stu-id="0545e-108">Then, the date on which the items are available for picking is calculated and entered in the **Expected Receipt Date** field.</span></span>  

<span data-ttu-id="0545e-109">Als u geen aangevraagde ontvangstdatum opgeeft, wordt automatisch de orderdatum op de regel gebruikt voor de berekening van de datum waarop de artikelen naar verwachting worden ontvangen en de datum waarop de artikelen beschikbaar zijn voor picken.</span><span class="sxs-lookup"><span data-stu-id="0545e-109">If you do not specify a requested receipt date, then the order date on the line is used as the starting point for calculating the date on which you can expect to receive the items and the date on which the items are available for picking.</span></span>  

## <a name="calculating-with-a-requested-receipt-date"></a><span data-ttu-id="0545e-110">Berekenen met een aangevraagde ontvangstdatum</span><span class="sxs-lookup"><span data-stu-id="0545e-110">Calculating with a requested receipt date</span></span>

<span data-ttu-id="0545e-111">Als er een aangevraagde ontvangstdatum op de inkooporderregel staat, wordt automatisch deze datum gebruikt als uitgangspunt voor de volgende berekeningen.</span><span class="sxs-lookup"><span data-stu-id="0545e-111">If there is a requested receipt date on the purchase order line, then that date is used as the starting point for the following calculations.</span></span>  

- <span data-ttu-id="0545e-112">aangevraagde ontvangstdatum - levertermijn = orderdatum</span><span class="sxs-lookup"><span data-stu-id="0545e-112">requested receipt date - lead time calculation = order date</span></span>  
- <span data-ttu-id="0545e-113">aangevraagde ontvangstdatum + inslagtijd + veiligheidstijd = verwachte ontvangstdatum</span><span class="sxs-lookup"><span data-stu-id="0545e-113">requested receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="0545e-114">Als u een aangevraagde ontvangstdatum op de inkooporderkop hebt ingevoerd, wordt deze datum gekopieerd naar het bijbehorende veld op alle regels.</span><span class="sxs-lookup"><span data-stu-id="0545e-114">If you entered a requested receipt date on the purchase order header, then that date is copied to the corresponding field on all the lines.</span></span> <span data-ttu-id="0545e-115">U kunt deze datum op elke orderregel desgewenst wijzigen of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="0545e-115">You can change this date on any of the lines, or you can remove the date on the line.</span></span>  

> [!NOTE]
> <span data-ttu-id="0545e-116">Als uw proces is gebaseerd op achterwaartse berekening, bijvoorbeeld als u de gevraagde ontvangstdatum gebruikt om de besteldatum te verkrijgen, raden we u aan datumformules te gebruiken met vaste looptijden, zoals '5D' voor vijf dagen of '1W' voor een week.</span><span class="sxs-lookup"><span data-stu-id="0545e-116">If your process is based on backward calculation, for example, if you use the requested receipt date to get the order date, we recommend that you use date formulas that have fixed durations, such as "5D" for five days or "1W" for one week.</span></span> <span data-ttu-id="0545e-117">Datumformules zonder vaste duur, zoals 'CW' voor de huidige week of CM voor de huidige maand, kunnen leiden tot onjuiste datumberekeningen.</span><span class="sxs-lookup"><span data-stu-id="0545e-117">Date formulas without fixed durations, such as "CW" for current week or CM for current month, can result in incorrect date calculations.</span></span> <span data-ttu-id="0545e-118">Zie voor meer informatie over datumformules [Werken met kalenderdatums en -tijden](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="0545e-118">For more information about date formulas, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

## <a name="calculating-without-a-requested-delivery-date"></a><span data-ttu-id="0545e-119">Berekenen zonder aangevraagde leverdatum</span><span class="sxs-lookup"><span data-stu-id="0545e-119">Calculating without a requested delivery date</span></span>

<span data-ttu-id="0545e-120">Als u een inkooporderregel invoert zonder een verzochte leverdatum, wordt in het veld **Orderdatum** op de regel de datum ingevuld uit het veld **Orderdatum** op de inkooporderkop.</span><span class="sxs-lookup"><span data-stu-id="0545e-120">If you enter a purchase order line without a requested delivery date, then the **Order Date** field on the line is filled with the date in the **Order Date** field on the purchase order header.</span></span> <span data-ttu-id="0545e-121">Dit kan de datum zijn die u hebt ingevoerd of de werkdatum.</span><span class="sxs-lookup"><span data-stu-id="0545e-121">This is either the date that you entered or the work date.</span></span> <span data-ttu-id="0545e-122">Vervolgens worden automatisch de volgende datums voor de inkooporderregel berekend, met de orderdatum als uitgangspunt.</span><span class="sxs-lookup"><span data-stu-id="0545e-122">The following dates are then calculated for the purchase order line, with the order date as the starting point.</span></span>  

- <span data-ttu-id="0545e-123">orderdatum + levertermijn = geplande ontvangstdatum</span><span class="sxs-lookup"><span data-stu-id="0545e-123">order date + lead time calculation = planned receipt date</span></span>  
- <span data-ttu-id="0545e-124">geplande ontvangstdatum + inslagtijd + veiligheidstijd = verwachte ontvangstdatum</span><span class="sxs-lookup"><span data-stu-id="0545e-124">planned receipt date + inbound whse. handling time + safety lead time = expected receipt date</span></span>  

<span data-ttu-id="0545e-125">Als u de orderdatum op de regel wijzigt, bijvoorbeeld omdat de artikelen pas later bij de leverancier beschikbaar zijn, worden de relevante datums op de regel automatisch opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="0545e-125">If you change the order date on the line, such as when items are not available at your vendor until a later date, then the relevant dates on the line are automatically recalculated.</span></span>  

<span data-ttu-id="0545e-126">Als u de orderdatum op de kop wijzigt, wordt deze datum automatisch gekopieerd naar het veld **Order Date** op alle regels en worden alle bijbehorende datumvelden vervolgens opnieuw berekend.</span><span class="sxs-lookup"><span data-stu-id="0545e-126">If you change the order date on the header, then that date is copied to the **Order Date** field on all the lines, and all the related date fields are then recalculated.</span></span>  

## <a name="default-values-for-lead-time-calculation"></a><span data-ttu-id="0545e-127">Standaardwaarden voor levertijdtijdberekening</span><span class="sxs-lookup"><span data-stu-id="0545e-127">Default values for lead time calculation</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="0545e-128">gebruikt de waarde van het veld **Levertermijnberek.** op de inkooporderregel om de order en de verwachte ontvangstdatums te berekenen.</span><span class="sxs-lookup"><span data-stu-id="0545e-128">uses the value from the **Lead Time Calculation** field on the purchase order line to calculate the order and the expected receipt dates.</span></span>  

<span data-ttu-id="0545e-129">U kunt de waarde op de regel handmatig specificeren of het programma de waarden laten gebruiken die zijn gedefinieerd op de leverancierskaart, artikelkaart, SKU-kaart of de artikelleverancierscatalogus.</span><span class="sxs-lookup"><span data-stu-id="0545e-129">You can manually specify the value on the line or let the program use values that are defined on the vendor card, item card, stockkeeping unit card, or the item vendor catalog.</span></span>
<span data-ttu-id="0545e-130">De levertermijnwaarde op de leverancierskaart wordt echter alleen gebruikt als er geen doorlooptijd is opgegeven op de artikelkaart, de SKU-kaart of de artikelleverancierscatalogus voor het artikel.</span><span class="sxs-lookup"><span data-stu-id="0545e-130">However, the lead time value on the vendor card is used only if a lead time is not specified on the item card, stockkeeping unit card, or the item vendor catalog for the item.</span></span> <span data-ttu-id="0545e-131">Dit is ook de escalerende volgorde van prioriteit voor deze waarden.</span><span class="sxs-lookup"><span data-stu-id="0545e-131">This is also the escalating order of priority for these values.</span></span> <span data-ttu-id="0545e-132">Als ze allemaal worden verstrekt, heeft de levertermijn van de leverancierskaart de laagste prioriteit en heeft de levertermijn van de artikelleverancierscatalogus de hoogste prioriteit.</span><span class="sxs-lookup"><span data-stu-id="0545e-132">If they are all provided, the lead time from the vendor card has the lowest priority, and the lead time from the item vendor catalog has the highest priority.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0545e-133">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0545e-133">See Also</span></span>

<span data-ttu-id="0545e-134">[Datumberekening voor verkoop](sales-date-calculation-for-sales.md) </span><span class="sxs-lookup"><span data-stu-id="0545e-134">[Date Calculation for Sales](sales-date-calculation-for-sales.md) </span></span>  
[<span data-ttu-id="0545e-135">Ordertoezeggingsdatums berekenen</span><span class="sxs-lookup"><span data-stu-id="0545e-135">Calculate Order Promising Dates</span></span>](sales-how-to-calculate-order-promising-dates.md)  
<span data-ttu-id="0545e-136">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0545e-136">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
