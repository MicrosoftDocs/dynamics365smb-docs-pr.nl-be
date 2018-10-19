---
title: Inzichten waarvoor een actie kan worden uitgevoerd weergeven in rolcentra | Microsoft Docs
description: "De extensie Essentiële zakelijke inzichten roteert een reeks zakelijke inzichten in rolcentra."
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: BI, add-in, insight, headline, data
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 0879d8ff0fbca3b18c36412e0a5fbe2f39372f2a
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---

# <a name="the-essential-business-insights-extension"></a><span data-ttu-id="65d25-103">De extensie Essentiële zakelijke inzichten</span><span class="sxs-lookup"><span data-stu-id="65d25-103">The Essential Business Insights Extension</span></span>
<span data-ttu-id="65d25-104">De extensie Essentiële zakelijke inzichten zoekt interessante bedrijfsfeiten in uw bedrijfsgegevens en geeft ze weer als krantenkoppen in rolcentra.</span><span class="sxs-lookup"><span data-stu-id="65d25-104">The Essential Business Insights extension finds interesting business facts in your company data and displays them as newspaper-like headlines in Role Centers.</span></span> <span data-ttu-id="65d25-105">Afhankelijk van wat de extensie in de gegevens vindt, worden de inzichten van de vorige week, maand, of drie maanden vanaf de huidige datum weergegeven.</span><span class="sxs-lookup"><span data-stu-id="65d25-105">Depending on what the extension finds in the data, the insights are from the last week, month, or three months from the current date.</span></span> <span data-ttu-id="65d25-106">De inzichten worden om de 10 minuten bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="65d25-106">The insights update every 10 minutes.</span></span>  

<span data-ttu-id="65d25-107">Als u beter naar een inzicht wilt kijken, kunt u naar de bron ervan gaan.</span><span class="sxs-lookup"><span data-stu-id="65d25-107">If you want to take a closer look at an insight, you can choose it to go to its source.</span></span> <span data-ttu-id="65d25-108">Als u bijvoorbeeld details wilt over de grootste verkoopfactuur die vorige week is geboekt, kunt u het inzicht kiezen om de factuur weer te geven.</span><span class="sxs-lookup"><span data-stu-id="65d25-108">For example, if you want details about the largest sales invoice that was posted last week, you can choose the insight to display the invoice.</span></span>

<span data-ttu-id="65d25-109">De volgende tabel beschrijft de inzichten die deze extensie biedt voor elk rolcentrum.</span><span class="sxs-lookup"><span data-stu-id="65d25-109">The following table describes the insights that this extension provides for each Role Center.</span></span>

|<span data-ttu-id="65d25-110">Rolcentrum</span><span class="sxs-lookup"><span data-stu-id="65d25-110">Role Center</span></span>|<span data-ttu-id="65d25-111">Vragen waarop de inzichten antwoord geven</span><span class="sxs-lookup"><span data-stu-id="65d25-111">Questions the Insights Answer</span></span>|
|----|-----|
|<span data-ttu-id="65d25-112">Standaard</span><span class="sxs-lookup"><span data-stu-id="65d25-112">Default</span></span>|<span data-ttu-id="65d25-113">Geeft een begroeting weer en een koppeling met productinformatie.</span><span class="sxs-lookup"><span data-stu-id="65d25-113">Displays a greeting, and link to product information.</span></span>|
|<span data-ttu-id="65d25-114">Bedrijfsmanager</span><span class="sxs-lookup"><span data-stu-id="65d25-114">Business Manager</span></span>|<li> <span data-ttu-id="65d25-115">Wat was het populairste artikel vorige week, maand of afgelopen drie maanden en hoeveel zijn er verkocht?</span><span class="sxs-lookup"><span data-stu-id="65d25-115">What was the most popular item last week, month, or last three months, and how many did we sell?</span></span><br><li> <span data-ttu-id="65d25-116">Wat is de grootste verkooporder vorige week, maand of afgelopen drie maanden?</span><span class="sxs-lookup"><span data-stu-id="65d25-116">What was the largest sale order last week, month, or last three months?</span></span><br><li> <span data-ttu-id="65d25-117">Wie of wat was de drukste resource en wat waren de boekingen?</span><span class="sxs-lookup"><span data-stu-id="65d25-117">Who, or what, was the busiest resource, and what were the bookings?</span></span><br><li> <span data-ttu-id="65d25-118">Zijn de verkopen afgelopen week, maand of drie maanden toegenomen, vergeleken met dezelfde periode vorig jaar?</span><span class="sxs-lookup"><span data-stu-id="65d25-118">Have sales gone up in the last week, month, or three months, compared to the same period last year?</span></span><br><li> <span data-ttu-id="65d25-119">Wat was de grootste verkoopfactuur die we afgelopen week, maand of drie maanden hebben geboekt en naar welke klant hebben we de factuur gestuurd?</span><span class="sxs-lookup"><span data-stu-id="65d25-119">What was the biggest sales invoice we posted last week, month, or last three months, and to which customer did we send the bill?</span></span></li> |
|<span data-ttu-id="65d25-120">Accountant</span><span class="sxs-lookup"><span data-stu-id="65d25-120">Accountant</span></span>|<li> <span data-ttu-id="65d25-121">Wat is de grootste verkooporder en geboekte factuur vorige week, maand of afgelopen drie maanden?</span><span class="sxs-lookup"><span data-stu-id="65d25-121">What was the largest sales order and posted invoice last week, month, or last three months?</span></span><br><li> <span data-ttu-id="65d25-122">Zijn de verkopen afgelopen week, maand of drie maanden toegenomen, vergeleken met dezelfde periode vorig jaar?</span><span class="sxs-lookup"><span data-stu-id="65d25-122">Have sales gone up in the last week, month, or three months, compared to the same period last year?</span></span> |
|<span data-ttu-id="65d25-123">Orderverwerker</span><span class="sxs-lookup"><span data-stu-id="65d25-123">Order Processor</span></span>| <span data-ttu-id="65d25-124">Wat is de grootste verkooporder en geboekte factuur vorige week, maand of afgelopen drie maanden?</span><span class="sxs-lookup"><span data-stu-id="65d25-124">What was the largest sale order and posted invoice last week, month, or last three months?</span></span>|
|<span data-ttu-id="65d25-125">Relatiebeheer</span><span class="sxs-lookup"><span data-stu-id="65d25-125">Relationship Manager</span></span>| <span data-ttu-id="65d25-126">Wat was het grootste gefactureerde bedrag en naar welke klant hebben we de factuur gestuurd?</span><span class="sxs-lookup"><span data-stu-id="65d25-126">What was the largest invoiced amount, and to which customer did we send the bill?</span></span>|
|<span data-ttu-id="65d25-127">Teamlid</span><span class="sxs-lookup"><span data-stu-id="65d25-127">Team Member</span></span>| <span data-ttu-id="65d25-128">Geeft een begroeting weer en een koppeling met productinformatie.</span><span class="sxs-lookup"><span data-stu-id="65d25-128">Displays a greeting, and link to product information.</span></span>|
|<span data-ttu-id="65d25-129">Projectleider</span><span class="sxs-lookup"><span data-stu-id="65d25-129">Project Manager</span></span>| <span data-ttu-id="65d25-130">Geeft een begroeting weer en een koppeling met productinformatie.</span><span class="sxs-lookup"><span data-stu-id="65d25-130">Displays a greeting, and link to product information.</span></span>|
|<span data-ttu-id="65d25-131">Beheerder</span><span class="sxs-lookup"><span data-stu-id="65d25-131">Administrator</span></span>| <span data-ttu-id="65d25-132">Geeft een begroeting weer en een koppeling met productinformatie.</span><span class="sxs-lookup"><span data-stu-id="65d25-132">Displays a greeting, and link to product information.</span></span>|

## <a name="see-also"></a><span data-ttu-id="65d25-133">Zie ook</span><span class="sxs-lookup"><span data-stu-id="65d25-133">See Also</span></span>
<span data-ttu-id="65d25-134">[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="65d25-134">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>

