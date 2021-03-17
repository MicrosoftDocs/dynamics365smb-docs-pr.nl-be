---
title: Artikelen of services inkopen voor een project en voorzieningen beheren| Microsoft Docs
description: Beschrijft hoe u de voorraad en aankoop van materiaal en services voor projecten beheert.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d6c9b1102ca54ed6445522bc2d36088d5934e1fe
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5376474"
---
# <a name="manage-job-supplies"></a><span data-ttu-id="dbf21-103">Projectvoorraden beheren</span><span class="sxs-lookup"><span data-stu-id="dbf21-103">Manage Job Supplies</span></span>
<span data-ttu-id="dbf21-104">Het beheren van projectgoederen van artikelen, services en onkosten is een integraal en zeer belangrijk aspect van de uitvoering van alle projecten.</span><span class="sxs-lookup"><span data-stu-id="dbf21-104">Managing project supplies of items, services, and expenses is an integral and critical aspect of the execution of all jobs.</span></span> <span data-ttu-id="dbf21-105">U kunt voorraadhoeveelheden gebruiken of projectspecifieke inkopen doen met behulp van inkooporders of inkoopfacturen.</span><span class="sxs-lookup"><span data-stu-id="dbf21-105">You can use inventory quantities or make job-specific purchases using purchase orders or purchase invoices.</span></span> <span data-ttu-id="dbf21-106">Stel bijvoorbeeld dat bij een serviceproject voor een computer een nieuwe schijf vereist is.</span><span class="sxs-lookup"><span data-stu-id="dbf21-106">For example, a service job on a computer requires a new disk.</span></span> <span data-ttu-id="dbf21-107">U maakt een inkoopfactuur om een nieuwe schijf te kopen en legt het project vast waarvoor deze wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="dbf21-107">You create a purchase invoice to buy a new disk and record the job that it will be used on.</span></span>

<span data-ttu-id="dbf21-108">Als voor het inkoopproces de fysieke transactie niet apart hoeft te worden vastgelegd, kan een aankoop worden verwerkt op de pagina **GB-dagboek project**.</span><span class="sxs-lookup"><span data-stu-id="dbf21-108">If the purchase process does not require that the physical transaction be recorded separately, then a purchase may be processed on the **Job G/L Journal** page.</span></span> <span data-ttu-id="dbf21-109">Zie voor meer informatie [Gebruik vastleggen voor projecten](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="dbf21-109">For more information, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="to-purchase-items-or-services-for-a-job"></a><span data-ttu-id="dbf21-110">Artikelen of services inkopen voor een project</span><span class="sxs-lookup"><span data-stu-id="dbf21-110">To purchase items or services for a job</span></span>
<span data-ttu-id="dbf21-111">In de volgende procedure wordt beschreven hoe u een inkoopfactuur gebruikt om producten voor een project te kopen.</span><span class="sxs-lookup"><span data-stu-id="dbf21-111">The following procedure shows how to use a purchase invoice to purchase products for a job.</span></span> <span data-ttu-id="dbf21-112">Dezelfde stappen gelden bij gebruik van een inkooporder.</span><span class="sxs-lookup"><span data-stu-id="dbf21-112">The same steps apply when using a purchase order.</span></span>  

1. <span data-ttu-id="dbf21-113">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopfacturen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="dbf21-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dbf21-114">Kies de actie **Nieuw** en vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="dbf21-114">Choose the **New** action and fill in the fields as necessary.</span></span> <span data-ttu-id="dbf21-115">Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="dbf21-115">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>
3. <span data-ttu-id="dbf21-116">Selecteer in de velden **Projectnr.** en **Projecttaaknr.** de gegevens van het project waarvoor u artikelen of services wilt inkopen.</span><span class="sxs-lookup"><span data-stu-id="dbf21-116">In the **Job No.** and **Job Task No.** fields, select the information of the job that you want to purchase items or services for.</span></span> <span data-ttu-id="dbf21-117">Gebruik de personalisatietools als een veld niet zichtbaar is.</span><span class="sxs-lookup"><span data-stu-id="dbf21-117">Use the personalization tools if a field is not visible.</span></span> <span data-ttu-id="dbf21-118">Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="dbf21-118">For more information, see [Personalize Your Workspace](ui-personalization-user.md).</span></span>

    <span data-ttu-id="dbf21-119">De waarde die u selecteert in het veld **Projectregelsoort** definieert of een planningsregel wordt gemaakt wanneer u het gebruik van het artikel boekt.</span><span class="sxs-lookup"><span data-stu-id="dbf21-119">The value that you select in the **Job Line Type** field defines whether a planning line is created when you post the usage of the item.</span></span> <span data-ttu-id="dbf21-120">Als het veld **Factureerbaar** bevat, worden projectplanningsregels gemaakt die gereed zijn om te worden gefactureerd aan de klant.</span><span class="sxs-lookup"><span data-stu-id="dbf21-120">If the field contains **Billable**, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="dbf21-121">Zie [Projecten factureren](projects-how-invoice-jobs.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="dbf21-121">For more information, see [Invoice Jobs](projects-how-invoice-jobs.md).</span></span>
4. <span data-ttu-id="dbf21-122">Kies de actie **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="dbf21-122">Choose the **Post** action.</span></span>

## <a name="to-view-the-value-of-purchases-for-a-job"></a><span data-ttu-id="dbf21-123">De waarde van aankopen voor een project weergeven</span><span class="sxs-lookup"><span data-stu-id="dbf21-123">To view the value of purchases for a job</span></span>
1. <span data-ttu-id="dbf21-124">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projecten** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="dbf21-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="dbf21-125">Open de betreffende projectkaart.</span><span class="sxs-lookup"><span data-stu-id="dbf21-125">Open a relevant job card.</span></span>

    <span data-ttu-id="dbf21-126">In het sneltabblad **Taken** bevat het veld **Openstaande orders** het totale uitstaande bedrag in de lokale valuta van voorraadartikelen en -services op inkoopdocumenten voor de projecttaakregel.</span><span class="sxs-lookup"><span data-stu-id="dbf21-126">On the **Tasks** FastTab, the **Outstanding Orders** field shows the total outstanding amount, in local currency, of inventory items and services on purchase documents for the job task line.</span></span>  

    <span data-ttu-id="dbf21-127">Het veld **Ontv./Niet gefact. bedrag** bevat de waarde van artikelen die worden geleverd op inkoopdocumenten, maar die nog niet zijn gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="dbf21-127">The **Amt. Rec. Not Invoiced** field shows the value of items delivered on purchase documents, but not yet invoiced.</span></span>  
3. <span data-ttu-id="dbf21-128">Kies een van de velden om de pagina **Inkoopregels** te openen. Op deze pagina kunt u informatie bekijken over de gerelateerde inkoopdocumentregels, inclusief welke artikelen of services zijn ontvangen.</span><span class="sxs-lookup"><span data-stu-id="dbf21-128">Choose either of the fields to open the **Purchase Lines** page where you can review information about the related purchase document lines, including which items or services have been received.</span></span>

## <a name="to-post-a-job-related-expense"></a><span data-ttu-id="dbf21-129">Projectkosten boeken</span><span class="sxs-lookup"><span data-stu-id="dbf21-129">To post a job-related expense</span></span>
<span data-ttu-id="dbf21-130">Als u buitengewone of eenmalige projectkosten maakt, kunt u de pagina **GB-dagboek project** gebruiken om ze direct te boeken naar de relevante projectrekening.</span><span class="sxs-lookup"><span data-stu-id="dbf21-130">If you incur extraordinary or one-time job expenses, you can use the **Job G/L Journal** page to post them directly to the relevant job account.</span></span>

1. <span data-ttu-id="dbf21-131">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **GB-dagboeken voor project** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="dbf21-131">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job G/L Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dbf21-132">Maak een nieuwe regel en voer gegevens voor de kosten in, zoals in de velden **Projectnr.** en **Projecttaaknr**.</span><span class="sxs-lookup"><span data-stu-id="dbf21-132">Create a new line and enter information about the expense, including information in the **Job No.** and **Job Task No** fields.</span></span>  
3. <span data-ttu-id="dbf21-133">Wanneer het dagboek compleet is, kiest u de actie **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="dbf21-133">When the journal is complete, choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="dbf21-134">Zie ook</span><span class="sxs-lookup"><span data-stu-id="dbf21-134">See Also</span></span>
[<span data-ttu-id="dbf21-135">Projectbeheer</span><span class="sxs-lookup"><span data-stu-id="dbf21-135">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="dbf21-136">Financiën</span><span class="sxs-lookup"><span data-stu-id="dbf21-136">Finance</span></span>](finance.md)  
<span data-ttu-id="dbf21-137">[Inkoop](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="dbf21-137">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="dbf21-138">[Verkoop](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="dbf21-138">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="dbf21-139">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dbf21-139">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]