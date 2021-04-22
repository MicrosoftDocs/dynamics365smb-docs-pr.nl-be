---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7ead218d289668d893a659f730a4c64e31195f10
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788643"
---
<span data-ttu-id="623ec-101">Wanneer u een datumtijd invoert (een datum en een tijd gecombineerd tot één veld), moet u een spatie invoeren tussen de datum en de tijd.</span><span class="sxs-lookup"><span data-stu-id="623ec-101">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="623ec-102">Het datumdeel kan alleen spaties in de vorm van het officiële datumscheidingsteken van uw regio-instellingen bevatten.</span><span class="sxs-lookup"><span data-stu-id="623ec-102">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="623ec-103">De tijd kan spaties bevatten rond de AM/PM-indicator in relevante regionale instellingen.</span><span class="sxs-lookup"><span data-stu-id="623ec-103">The time can contain spaces around the AM/PM indicator in relevant regional settings.</span></span>

<!--It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.-->

<span data-ttu-id="623ec-104">In de volgende tabel wordt aangegeven op welke manier u de datum/tijd kunt invoeren en hoe de verschillende manieren worden geïnterpreteerd.</span><span class="sxs-lookup"><span data-stu-id="623ec-104">The following table lists the various ways in which you can enter datetimes and how they're interpreted.</span></span>  

|<span data-ttu-id="623ec-105">Post</span><span class="sxs-lookup"><span data-stu-id="623ec-105">Entry</span></span>|<span data-ttu-id="623ec-106">Interpretatie</span><span class="sxs-lookup"><span data-stu-id="623ec-106">Interpretation</span></span>|
|---------------|------------------------|
|<span data-ttu-id="623ec-107">08-01-2022 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="623ec-107">08-01-2022 05:48:12 PM</span></span>|<span data-ttu-id="623ec-108">08\-01\-2022 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="623ec-108">08\-01\-2022 05:48:12 PM</span></span>|
|<span data-ttu-id="623ec-109">131222 132455</span><span class="sxs-lookup"><span data-stu-id="623ec-109">131222 132455</span></span>|<span data-ttu-id="623ec-110">13-12-22 13:24:55</span><span class="sxs-lookup"><span data-stu-id="623ec-110">13-12-22 13:24:55</span></span>|
|<span data-ttu-id="623ec-111">1-12-22 10</span><span class="sxs-lookup"><span data-stu-id="623ec-111">1-12-22 10</span></span>|<span data-ttu-id="623ec-112">01-12-22 10:00:00</span><span class="sxs-lookup"><span data-stu-id="623ec-112">01-12-22 10:00:00</span></span>|
|<span data-ttu-id="623ec-113">1.12.22 5</span><span class="sxs-lookup"><span data-stu-id="623ec-113">1.12.22 5</span></span>|<span data-ttu-id="623ec-114">01-12-22 05:00:00</span><span class="sxs-lookup"><span data-stu-id="623ec-114">01-12-22 05:00:00</span></span>|
|<span data-ttu-id="623ec-115">1.12.22</span><span class="sxs-lookup"><span data-stu-id="623ec-115">1.12.22</span></span>|<span data-ttu-id="623ec-116">01-12-22 00:00:00</span><span class="sxs-lookup"><span data-stu-id="623ec-116">01-12-22 00:00:00</span></span>|
|<span data-ttu-id="623ec-117">11 12</span><span class="sxs-lookup"><span data-stu-id="623ec-117">11 12</span></span>|<span data-ttu-id="623ec-118">11.huidige maand.huidig jaar 12:00:00</span><span class="sxs-lookup"><span data-stu-id="623ec-118">11-current month-current year 12:00:00</span></span>|
|<span data-ttu-id="623ec-119">1112 12</span><span class="sxs-lookup"><span data-stu-id="623ec-119">1112 12</span></span>|<span data-ttu-id="623ec-120">11.12.huidig jaar 12:00:00</span><span class="sxs-lookup"><span data-stu-id="623ec-120">11-12-current year 12:00:00</span></span>|
|<span data-ttu-id="623ec-121">h of huidige datum</span><span class="sxs-lookup"><span data-stu-id="623ec-121">t or today</span></span>|<span data-ttu-id="623ec-122">huidige datum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="623ec-122">today's date 00:00:00</span></span>|
|<span data-ttu-id="623ec-123">h tijd</span><span class="sxs-lookup"><span data-stu-id="623ec-123">t time</span></span>|<span data-ttu-id="623ec-124">huidige datum werkelijke tijd</span><span class="sxs-lookup"><span data-stu-id="623ec-124">today's date actual time</span></span>|
|<span data-ttu-id="623ec-125">h 10:30</span><span class="sxs-lookup"><span data-stu-id="623ec-125">t 10:30</span></span>|<span data-ttu-id="623ec-126">huidige datum 10:30:00</span><span class="sxs-lookup"><span data-stu-id="623ec-126">today's date 10:30:00</span></span>|
|<span data-ttu-id="623ec-127">h 3:3:3</span><span class="sxs-lookup"><span data-stu-id="623ec-127">t 3:3:3</span></span>|<span data-ttu-id="623ec-128">huidige datum 03:03:03</span><span class="sxs-lookup"><span data-stu-id="623ec-128">today's date 03:03:03</span></span>|
|<span data-ttu-id="623ec-129">w of werkdatum</span><span class="sxs-lookup"><span data-stu-id="623ec-129">w or workdate</span></span>|<span data-ttu-id="623ec-130">de werkdatum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="623ec-130">the working date 00:00:00</span></span>|
|<span data-ttu-id="623ec-131">ma of maandag</span><span class="sxs-lookup"><span data-stu-id="623ec-131">m or Monday</span></span>|<span data-ttu-id="623ec-132">Maandag van de huidige week 00:00:00</span><span class="sxs-lookup"><span data-stu-id="623ec-132">Monday of the current week 00:00:00</span></span>|
|<span data-ttu-id="623ec-133">di of dinsdag</span><span class="sxs-lookup"><span data-stu-id="623ec-133">tu or Tuesday</span></span>|<span data-ttu-id="623ec-134">Dinsdag van de huidige week 00:00:00</span><span class="sxs-lookup"><span data-stu-id="623ec-134">Tuesday of the current week 00:00:00</span></span>|
|<span data-ttu-id="623ec-135">wo of woensdag</span><span class="sxs-lookup"><span data-stu-id="623ec-135">we or Wednesday</span></span>|<span data-ttu-id="623ec-136">Woensdag van de huidige week 00:00:00</span><span class="sxs-lookup"><span data-stu-id="623ec-136">Wednesday of the current week 00:00:00</span></span>|
|<span data-ttu-id="623ec-137">do of donderdag</span><span class="sxs-lookup"><span data-stu-id="623ec-137">th or Thursday</span></span>|<span data-ttu-id="623ec-138">Donderdag van de huidige week 00:00:00</span><span class="sxs-lookup"><span data-stu-id="623ec-138">Thursday of the current week 00:00:00</span></span>|
|<span data-ttu-id="623ec-139">vr of vrijdag</span><span class="sxs-lookup"><span data-stu-id="623ec-139">f or Friday</span></span>|<span data-ttu-id="623ec-140">Vrijdag van de huidige week 00:00:00</span><span class="sxs-lookup"><span data-stu-id="623ec-140">Friday of the current week 00:00:00</span></span>|
|<span data-ttu-id="623ec-141">za of zaterdag</span><span class="sxs-lookup"><span data-stu-id="623ec-141">s or Saturday</span></span>|<span data-ttu-id="623ec-142">Zaterdag van de huidige week 00:00:00</span><span class="sxs-lookup"><span data-stu-id="623ec-142">Saturday of the current week 00:00:00</span></span>|
|<span data-ttu-id="623ec-143">zo of zondag</span><span class="sxs-lookup"><span data-stu-id="623ec-143">su or Sunday</span></span>|<span data-ttu-id="623ec-144">Zondag van de huidige week 00:00:00</span><span class="sxs-lookup"><span data-stu-id="623ec-144">Sunday of the current week 00:00:00</span></span>|
|<span data-ttu-id="623ec-145">di 10:30</span><span class="sxs-lookup"><span data-stu-id="623ec-145">tu 10:30</span></span>|<span data-ttu-id="623ec-146">Dinsdag van de huidige week 10:30:00</span><span class="sxs-lookup"><span data-stu-id="623ec-146">Tuesday of the current week 10:30:00</span></span>|
|<span data-ttu-id="623ec-147">di 3:3:3</span><span class="sxs-lookup"><span data-stu-id="623ec-147">tu 3:3:3</span></span>|<span data-ttu-id="623ec-148">Dinsdag van de huidige week 03:03:03</span><span class="sxs-lookup"><span data-stu-id="623ec-148">Tuesday of the current week 03:03:03</span></span>|
|<span data-ttu-id="623ec-149">d23 t</span><span class="sxs-lookup"><span data-stu-id="623ec-149">t23 t</span></span>|<span data-ttu-id="623ec-150">Dinsdag van week 23 van het werkdatumjaar huidige tijd van dag</span><span class="sxs-lookup"><span data-stu-id="623ec-150">Tuesday of week 23 of the work date year, current time of day</span></span>|
|<span data-ttu-id="623ec-151">d23</span><span class="sxs-lookup"><span data-stu-id="623ec-151">t23</span></span>|<span data-ttu-id="623ec-152">Dinsdag van week 23 van het werkdatumjaar</span><span class="sxs-lookup"><span data-stu-id="623ec-152">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="623ec-153">d 23</span><span class="sxs-lookup"><span data-stu-id="623ec-153">t 23</span></span>|<span data-ttu-id="623ec-154">Vandaag 23:00:00</span><span class="sxs-lookup"><span data-stu-id="623ec-154">Today 23:00:00</span></span>|
|<span data-ttu-id="623ec-155">d-1</span><span class="sxs-lookup"><span data-stu-id="623ec-155">t-1</span></span>|<span data-ttu-id="623ec-156">Dinsdag van week 1 van het werkdatumjaar</span><span class="sxs-lookup"><span data-stu-id="623ec-156">Tuesday of week 1 of the work date year</span></span>|


