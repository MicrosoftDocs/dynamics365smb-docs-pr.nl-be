---
title: Een projectverkoopfactuur maken om een project te factureren| Microsoft Docs
description: Beschrijft hoe u klanten factureert voor projectkosten tijdens de voortgang van een project.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9367dc5875b687b95076efffb3b0df2019332651
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-invoice-jobs"></a><span data-ttu-id="d8150-103">Procedure: Projecten factureren</span><span class="sxs-lookup"><span data-stu-id="d8150-103">How to: Invoice Jobs</span></span>
<span data-ttu-id="d8150-104">Tijdens het project kunnen projectkosten van resourceverbruik, materialen en aan het project gerelateerde inkopen, zich ophopen.</span><span class="sxs-lookup"><span data-stu-id="d8150-104">During the project, job costs from resource usage, materials, and job-related purchases can accumulate.</span></span> <span data-ttu-id="d8150-105">Naarmate het project vordert, worden deze transacties geboekt in het projectdagboek.</span><span class="sxs-lookup"><span data-stu-id="d8150-105">As the job progresses, these transactions get posted to the job journal.</span></span> <span data-ttu-id="d8150-106">Het is van belang dat alle kosten worden vastgelegd in het projectdagboek voordat u het project aan de klant factureert.</span><span class="sxs-lookup"><span data-stu-id="d8150-106">It is important that all costs get recorded in the job journal before you invoice the customer.</span></span>

<span data-ttu-id="d8150-107">U kunt het hele project factureren vanuit het venster **Projecttaakregels** of alleen de geselecteerde factureerbare regels factureren vanuit het venster **Planningsregels**.</span><span class="sxs-lookup"><span data-stu-id="d8150-107">You can invoice the whole job from the **Job Task Lines** window or only invoice selected billable lines from the **Planning Lines** window.</span></span> <span data-ttu-id="d8150-108">Facturering kan plaatsvinden nadat het project is voltooid of op bepaalde intervallen tijdens de voortgang van het project op basis van een factureringsschema.</span><span class="sxs-lookup"><span data-stu-id="d8150-108">Invoicing can be done after the job is finished or at certain intervals during the job's progress based on an invoicing schedule.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d8150-109">Als u **Factureerbaar** selecteert in het veld **Regelsoort project** in de inkoopdocumenten voor aan het project gerelateerde inkopen, worden projectplanningsregels gemaakt die gereed zijn om te worden gefactureerd aan de klant.</span><span class="sxs-lookup"><span data-stu-id="d8150-109">If you select **Billable** in the **Job Line Type** field on the purchase documents for job-related purchases, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="d8150-110">Zie [Procedure: Projectvoorraden beheren](projects-how-manage-project-supplies.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d8150-110">For more information, see [How to: Manage Project Supplies](projects-how-manage-project-supplies.md).</span></span>

## <a name="to-create-and-post-a-job-sales-invoice"></a><span data-ttu-id="d8150-111">Een projectverkoopfactuur maken en boeken</span><span class="sxs-lookup"><span data-stu-id="d8150-111">To create and post a job sales invoice</span></span>
<span data-ttu-id="d8150-112">U kunt een factuur maken voor een project of voor één of meer projecttaken voor een klant, wanneer ofwel het werk dat moet worden gefactureerd voltooid is ofwel de datum voor facturering op basis van een factureringsschema is bereikt.</span><span class="sxs-lookup"><span data-stu-id="d8150-112">You can create an invoice for a job or for one or more job tasks for a customer when either the work to be invoiced is complete or the date for invoicing based on an invoicing schedule has been reached.</span></span>

<span data-ttu-id="d8150-113">Vanuit het venster **Projecten** kunt u een klant factureren door het project te selecteren en vervolgens de actie **Projectverkoopfactuur maken** te kiezen.</span><span class="sxs-lookup"><span data-stu-id="d8150-113">From the **Jobs** window, you can invoice a customer by selecting the job, and then choosing the **Create Job Sales Invoice** action.</span></span> <span data-ttu-id="d8150-114">In de volgende procedure wordt beschreven hoe u een batchverwerking gebruikt om meerdere projecten te factureren.</span><span class="sxs-lookup"><span data-stu-id="d8150-114">The following procedure shows how to use a batch job to invoice multiple jobs.</span></span>  

1. <span data-ttu-id="d8150-115">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verkoopfactuur project maken** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="d8150-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Job Create Sales Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d8150-116">Vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="d8150-116">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="d8150-117">Stel filters in als u de projecten wilt beperken die door de batchverwerking worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="d8150-117">Set filters if you want to limit the jobs that the batch job will process.</span></span>
4. <span data-ttu-id="d8150-118">Kies de knop **OK** om de facturen te maken.</span><span class="sxs-lookup"><span data-stu-id="d8150-118">Choose the **OK** button to create the invoices.</span></span>  

## <a name="to-create-multiple-job-sales-invoices-from-job-planning-lines"></a><span data-ttu-id="d8150-119">Meerdere projectverkoopfacturen maken vanuit projectplanningsregels</span><span class="sxs-lookup"><span data-stu-id="d8150-119">To create multiple job sales invoices from job planning lines</span></span>
<span data-ttu-id="d8150-120">U kunt een factuur maken vanuit een projectplanningsregel en op dat moment de hoeveelheid van het artikel, resource of grootboekrekening die u wilt factureren, aangeven.</span><span class="sxs-lookup"><span data-stu-id="d8150-120">You can create an invoice from a job planning lines, and indicate at that time the quantity of the item, resource, or general ledger account that you want to invoice.</span></span>

1. <span data-ttu-id="d8150-121">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projecten** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="d8150-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="d8150-122">Open het betreffende project.</span><span class="sxs-lookup"><span data-stu-id="d8150-122">Open a relevant job.</span></span>
3. <span data-ttu-id="d8150-123">Selecteer een projecttaak waarvoor **Boeking** de **projecttaaksoort** is, en kies vervolgens de actie **Projectplanningsregels**.</span><span class="sxs-lookup"><span data-stu-id="d8150-123">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="d8150-124">Voer op een projectplanningsregel in het veld **Aantal te verplaatsen naar factuur** de hoeveelheid van het artikel, de resource en het soort grootboekrekening dat u wilt factureren in.</span><span class="sxs-lookup"><span data-stu-id="d8150-124">On a job planning line, in the **Qty. To Transfer to Invoice** field, enter the quantity of the item, resource, general ledger account type that you want to invoice.</span></span>  
5. <span data-ttu-id="d8150-125">Kies de actie **Verkoopfactuur maken**.</span><span class="sxs-lookup"><span data-stu-id="d8150-125">Choose the **Create Sales Invoice** action.</span></span>
6. <span data-ttu-id="d8150-126">Voer in het venster **Verkoopfactuur project maken** de boekingsdatum in en of u een nieuwe factuur wilt maken of toevoegen aan deze factuur of aan een bestaande factuur.</span><span class="sxs-lookup"><span data-stu-id="d8150-126">In the **Job Create Sales Invoice** window, enter the posting date and whether you want to create a new invoice or append this invoice to an existing one.</span></span>
7. <span data-ttu-id="d8150-127">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="d8150-127">Choose the **OK** button.</span></span>  

    <span data-ttu-id="d8150-128">Op de projectplanningsregel, in het veld **Aantal overgebracht naar factuur** ziet u de hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="d8150-128">On the job planning line, in the **Qty. Transferred to Invoice** field, you can see the quantity.</span></span>
8. <span data-ttu-id="d8150-129">Kies in het venster **Projectplanningsregels** de actie **Verkoopfacturen/-creditnota's**.</span><span class="sxs-lookup"><span data-stu-id="d8150-129">In the **Job Planning Lines** window, choose the **Sales Invoices/Credit Memos** action.</span></span>

    <span data-ttu-id="d8150-130">Het venster **Verkoopfactuur** wordt geopend met het aantal dat u naar de factuur hebt verzonden.</span><span class="sxs-lookup"><span data-stu-id="d8150-130">The **Sales Invoice** window opens, showing the quantity that you have transferred to the invoice.</span></span>  
9. <span data-ttu-id="d8150-131">Breng eventuele aanvullende wijzigingen aan en kies vervolgens de actie **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="d8150-131">Make any additional changes, and then choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d8150-132">De bovengenoemde procedure is soortgelijk voor het maken, controleren en boeken van een aan een project gerelateerde verkoopcreditnota.</span><span class="sxs-lookup"><span data-stu-id="d8150-132">The above procedure is similar for creating, reviewing, and posting a job-related sales credit memo.</span></span>

## <a name="to-calculate-and-post-job-completion-entries"></a><span data-ttu-id="d8150-133">Projectvoltooiingsposten berekenen en boeken</span><span class="sxs-lookup"><span data-stu-id="d8150-133">To calculate and post job completion entries</span></span>
<span data-ttu-id="d8150-134">Wanneer u alle activiteiten voor een project hebt uitgevoerd, waaronder gebruiksboekingen en -facturering, moet u het project bijwerken om de **Status** in te stellen op **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="d8150-134">When you have completed all activities for a job, including usage posting and invoicing, you must update the job to have a **Status** of **Completed**.</span></span> <span data-ttu-id="d8150-135">Vervolgens moet u eventueel OHW tegenboeken dat naar het grootboek is geboekt.</span><span class="sxs-lookup"><span data-stu-id="d8150-135">Then, you must reverse any WIP that has been posted to the general ledger.</span></span>

1. <span data-ttu-id="d8150-136">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projecten** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="d8150-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d8150-137">Selecteer een open project en kies vervolgens de actie **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="d8150-137">Select an open job, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="d8150-138">Selecteer in het veld **Status** de optie **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="d8150-138">In the **Status** field, select **Completed**.</span></span>
4. <span data-ttu-id="d8150-139">Volg de hulpstappen om OHW te berekenen en te boeken.</span><span class="sxs-lookup"><span data-stu-id="d8150-139">Follow the assistance steps to calculate and post WIP.</span></span> <span data-ttu-id="d8150-140">Of volg stap 5 en 6 om dit handmatig te doen.</span><span class="sxs-lookup"><span data-stu-id="d8150-140">Alternatively, follows steps 5 and 6 to do so manually.</span></span>  
5. <span data-ttu-id="d8150-141">Kies de actie **OHW berekenen**.</span><span class="sxs-lookup"><span data-stu-id="d8150-141">Choose the **Calculate WIP** action.</span></span>
6. <span data-ttu-id="d8150-142">Vul in het venster **OHW voor project berekenen** indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="d8150-142">In the **Job Calculate WIP** window, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="d8150-143">De OHW-posten voor het project die worden gemaakt door het uitvoeren van de batchverwerking, hebben nu een vinkje in het selectievak **Project voltooid** om aan te geven dat het voltooiingsposten zijn.</span><span class="sxs-lookup"><span data-stu-id="d8150-143">The job WIP entries created by running the batch job will have the **Job Complete** check box selected to show that they are completion entries.</span></span>  
7. <span data-ttu-id="d8150-144">Kies de actie **Project-OHW naar GB boeken**.</span><span class="sxs-lookup"><span data-stu-id="d8150-144">Choose the **Job Post WIP to G/L** action.</span></span>
8. <span data-ttu-id="d8150-145">Vul in het venster **Project-OHW naar GB boeken** indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="d8150-145">In the **Job Post WIP to G/L** window, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="d8150-146">De OHW-grootboekposten voor het project die worden gemaakt door het uitvoeren van de batchverwerking hebben nu een vinkje in het selectievak **Project voltooid** om aan te geven dat het voltooide posten zijn.</span><span class="sxs-lookup"><span data-stu-id="d8150-146">The job WIP general ledger entries created by running the batch job will have the **Job Complete** check box selected to show they are completion entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8150-147">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d8150-147">See Also</span></span>
[<span data-ttu-id="d8150-148">Projecten beheren</span><span class="sxs-lookup"><span data-stu-id="d8150-148">Managing Projects</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="d8150-149">Financiën</span><span class="sxs-lookup"><span data-stu-id="d8150-149">Finance</span></span>](finance.md)  
<span data-ttu-id="d8150-150">[Inkoop](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="d8150-150">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="d8150-151">[Verkoop](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="d8150-151">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="d8150-152">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d8150-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

