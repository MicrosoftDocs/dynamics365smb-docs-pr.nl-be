---
title: Datumbereiken instellen in Business Central | Microsoft Docs
description: Leren hoe u een rapport kunt verkrijgen om gegevens te tonen uit specifieke tijdperioden met behulp van datumbereiken in Business Central.
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 05/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 552578ce097f7f647ed0962fec0448059d3ca3b2
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="entering-date-ranges"></a><span data-ttu-id="eefb7-103">Datumbereiken invoeren</span><span class="sxs-lookup"><span data-stu-id="eefb7-103">Entering Date Ranges</span></span> 
<span data-ttu-id="eefb7-104">U kunt filters met een begin- en einddatum instellen om alleen de gegevens in dat datumbereik of tijdsinterval in te stellen.</span><span class="sxs-lookup"><span data-stu-id="eefb7-104">You can set filters containing a start date and an end date to display only the data contained in that date range or time interval.</span></span> <span data-ttu-id="eefb7-105">Voor het instellen van een datumbereik gelden speciale regels.</span><span class="sxs-lookup"><span data-stu-id="eefb7-105">Special rules apply to the way you set date ranges.</span></span> <span data-ttu-id="eefb7-106">Neem als voorbeeld de **Klanten top 10**:</span><span class="sxs-lookup"><span data-stu-id="eefb7-106">Let's take the **Customer Top 10** as an example:</span></span>

![Een datumbereik instellen op de aanvraagpagina voor de lijst Klanten top 10](./media/ui-enter-date-ranges/customer-top10-list.png)

<span data-ttu-id="eefb7-108">Hier kunt u de lijst tot een datumbereik beperken, zoals de afgelopen 2 weken of een totaal van 6 weken, of wat voor bereik u ook nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="eefb7-108">Here you can limit the report to a date range such as the past 2 weeks, or a total of 6 weeks, or whatever range you want.</span></span> <span data-ttu-id="eefb7-109">Als u datumbereiken wilt invoeren, voert u datums in en gebruikt u **..**</span><span class="sxs-lookup"><span data-stu-id="eefb7-109">To set date ranges, you enter dates and then use either **..**</span></span> <span data-ttu-id="eefb7-110">of **|** om het bereik in te stellen.</span><span class="sxs-lookup"><span data-stu-id="eefb7-110">or **|** to set the range.</span></span> <span data-ttu-id="eefb7-111">Als u in ons voorbeeld de top 10 klanten voor de eerste twee weken van mei wilt invoeren, stelt u het datumfilter in op *05 01 17..05 14 17*.</span><span class="sxs-lookup"><span data-stu-id="eefb7-111">In our example, to show the top 10 customers for the first two weeks of May, you would set the date filter to *05 01 17..05 14 17*.</span></span>
<span data-ttu-id="eefb7-112">Hier volgen enkele andere voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="eefb7-112">Here are a couple of other examples:</span></span>

| <span data-ttu-id="eefb7-113">Betekenis</span><span class="sxs-lookup"><span data-stu-id="eefb7-113">Meaning</span></span> | <span data-ttu-id="eefb7-114">Opmerking</span><span class="sxs-lookup"><span data-stu-id="eefb7-114">Example</span></span> | <span data-ttu-id="eefb7-115">Opgenomen posten</span><span class="sxs-lookup"><span data-stu-id="eefb7-115">Entries included</span></span> |
|---|---|---|
|<span data-ttu-id="eefb7-116">Gelijk aan</span><span class="sxs-lookup"><span data-stu-id="eefb7-116">Equal to</span></span>| <span data-ttu-id="eefb7-117">12 15 16</span><span class="sxs-lookup"><span data-stu-id="eefb7-117">12 15 16</span></span> |<span data-ttu-id="eefb7-118">Alleen posten die zijn geboekt op 15 december 2016.</span><span class="sxs-lookup"><span data-stu-id="eefb7-118">Only those posted on December 15 2016.</span></span>|
|<span data-ttu-id="eefb7-119">Interval</span><span class="sxs-lookup"><span data-stu-id="eefb7-119">Interval</span></span>| <span data-ttu-id="eefb7-120">12 15 16..01 15 17</span><span class="sxs-lookup"><span data-stu-id="eefb7-120">12 15 16..01 15 17</span></span><br /><br /><span data-ttu-id="eefb7-121">..12 15 16</span><span class="sxs-lookup"><span data-stu-id="eefb7-121">..12 15 16</span></span>|<span data-ttu-id="eefb7-122">Posten die zijn geboekt in de periode tussen en tot en met 15 december 2016 en 15 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="eefb7-122">Those posted on dates between and including December 15 2016 and January 15 2017.</span></span><br /><br /><span data-ttu-id="eefb7-123">Posten die zijn geboekt op 15 december 2016 of eerder.</span><span class="sxs-lookup"><span data-stu-id="eefb7-123">Those posted on December 15 2016 or earlier.</span></span>|
|<span data-ttu-id="eefb7-124">Of/of</span><span class="sxs-lookup"><span data-stu-id="eefb7-124">Either/or</span></span>|<span data-ttu-id="eefb7-125">12 15 16&#124;12 16 16</span><span class="sxs-lookup"><span data-stu-id="eefb7-125">12 15 16&#124;12 16 16</span></span>|<span data-ttu-id="eefb7-126">Posten die zijn geboekt op 15 december of 16 december 2016.</span><span class="sxs-lookup"><span data-stu-id="eefb7-126">Those posted on either December 15 or December 16 2016.</span></span> <span data-ttu-id="eefb7-127">Als deze posten zijn geboekt op beide dagen, worden ze allebei weergegeven.</span><span class="sxs-lookup"><span data-stu-id="eefb7-127">If there are entries posted on both days, they will all be displayed.</span></span>|

<span data-ttu-id="eefb7-128">U kunt de verschillende notatiesoorten ook combineren.</span><span class="sxs-lookup"><span data-stu-id="eefb7-128">You can also combine the various format types.</span></span>

| <span data-ttu-id="eefb7-129">Opmerking</span><span class="sxs-lookup"><span data-stu-id="eefb7-129">Example</span></span> | <span data-ttu-id="eefb7-130">Opgenomen posten</span><span class="sxs-lookup"><span data-stu-id="eefb7-130">Entries included</span></span> |
|---|---|
|<span data-ttu-id="eefb7-131">12 15 16&#124;12 01 16..05 31 17</span><span class="sxs-lookup"><span data-stu-id="eefb7-131">12 15 16&#124;12 01 16..05 31 17</span></span> | <span data-ttu-id="eefb7-132">Posten die zijn geboekt op 15 december 2016 of op datums tussen en tot en met 1 december 2016 en 31 mei 2017.</span><span class="sxs-lookup"><span data-stu-id="eefb7-132">Entries posted either on December 15 2016 or on dates between and including December 01 2016 and May 31 2017.</span></span> |
|<span data-ttu-id="eefb7-133">..12 14 16&#124;12 30 16..</span><span class="sxs-lookup"><span data-stu-id="eefb7-133">..12 14 16&#124;12 30 16..</span></span> | <span data-ttu-id="eefb7-134">Posten die zijn geboekt op 14 december of eerder, of posten die zijn geboekt op 30 december of later. Dit wil zeggen, alle posten behalve die zijn geboekt tussen 15 december en 29 december tot en met.</span><span class="sxs-lookup"><span data-stu-id="eefb7-134">Entries posted on December 14 or earlier, or entries posted on December 30 or later - that is, all entries except those posted on dates between and including December 15 and 29.</span></span> |

<span data-ttu-id="eefb7-135">U ziet dat we hier de Amerikaanse datumnotatie MMDDYY hebben gebruikt.</span><span class="sxs-lookup"><span data-stu-id="eefb7-135">Note that we have used the US date format MMDDYY here.</span></span> <span data-ttu-id="eefb7-136">Zodra [!INCLUDE[d365fin](includes/d365fin_md.md)] beschikbaar wordt in andere markten, zult u de indelingen kunnen gebruiken die u gewend bent.</span><span class="sxs-lookup"><span data-stu-id="eefb7-136">As [!INCLUDE[d365fin](includes/d365fin_md.md)] becomes available in other markets, you'll be able to use the formats that you are used to.</span></span>

## <a name="see-also"></a><span data-ttu-id="eefb7-137">Zie ook</span><span class="sxs-lookup"><span data-stu-id="eefb7-137">See Also</span></span>
<span data-ttu-id="eefb7-138">[Werken met [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="eefb7-138">[Working with [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="eefb7-139">Criteria in filters invoeren</span><span class="sxs-lookup"><span data-stu-id="eefb7-139">Entering Criteria in Filters </span></span>](ui-enter-criteria-filters.md)  
[<span data-ttu-id="eefb7-140">Algemene bedrijfsfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="eefb7-140">General Business Functionality</span></span>](ui-across-business-areas.md)

