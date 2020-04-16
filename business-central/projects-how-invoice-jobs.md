---
title: Een projectverkoopfactuur maken om een project te factureren| Microsoft Docs
description: Beschrijft hoe u klanten factureert voor projectkosten tijdens de voortgang van een project.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 277e5e6cb212202f930ed49012184aa67a23d03f
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191271"
---
# <a name="invoice-jobs"></a><span data-ttu-id="8eb06-103">Projecten factureren</span><span class="sxs-lookup"><span data-stu-id="8eb06-103">Invoice Jobs</span></span>
<span data-ttu-id="8eb06-104">Tijdens het project kunnen projectkosten van resourceverbruik, materialen en aan het project gerelateerde inkopen, zich ophopen.</span><span class="sxs-lookup"><span data-stu-id="8eb06-104">During the project, job costs from resource usage, materials, and job-related purchases can accumulate.</span></span> <span data-ttu-id="8eb06-105">Naarmate het project vordert, worden deze transacties geboekt in het projectdagboek.</span><span class="sxs-lookup"><span data-stu-id="8eb06-105">As the job progresses, these transactions get posted to the job journal.</span></span> <span data-ttu-id="8eb06-106">Het is van belang dat alle kosten worden vastgelegd in het projectdagboek voordat u het project aan de klant factureert.</span><span class="sxs-lookup"><span data-stu-id="8eb06-106">It is important that all costs get recorded in the job journal before you invoice the customer.</span></span>

> [!NOTE]
> <span data-ttu-id="8eb06-107">U kunt ook externe resources aanschaffen die niet aan een project gerelateerd zijn, bijvoorbeeld om een leverancier te factureren voor het geleverde werk.</span><span class="sxs-lookup"><span data-stu-id="8eb06-107">You can also purchase external resources unrelated to a job, for example, to invoice a vendor for work delivered.</span></span> <span data-ttu-id="8eb06-108">Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="8eb06-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

<span data-ttu-id="8eb06-109">U kunt het hele project factureren vanuit de pagina **Projecttaakregels** of alleen de geselecteerde factureerbare regels factureren vanuit de pagina **Planningsregels**.</span><span class="sxs-lookup"><span data-stu-id="8eb06-109">You can invoice the whole job from the **Job Task Lines** page or only invoice selected billable lines from the **Planning Lines** page.</span></span> <span data-ttu-id="8eb06-110">Facturering kan plaatsvinden nadat het project is voltooid of op bepaalde intervallen tijdens de voortgang van het project op basis van een factureringsschema.</span><span class="sxs-lookup"><span data-stu-id="8eb06-110">Invoicing can be done after the job is finished or at certain intervals during the job's progress based on an invoicing schedule.</span></span>

> [!NOTE]  
>   <span data-ttu-id="8eb06-111">Als u **Factureerbaar** selecteert in het veld **Regelsoort project** in de inkoopdocumenten voor aan het project gerelateerde inkopen, worden projectplanningsregels gemaakt die gereed zijn om te worden gefactureerd aan de klant.</span><span class="sxs-lookup"><span data-stu-id="8eb06-111">If you select **Billable** in the **Job Line Type** field on the purchase documents for job-related purchases, then job planning lines that are ready to be invoiced to the customer are created.</span></span> <span data-ttu-id="8eb06-112">Zie [Projectvoorraden beheren](projects-how-manage-project-supplies.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8eb06-112">For more information, see [Manage Project Supplies](projects-how-manage-project-supplies.md).</span></span>

## <a name="to-create-and-post-a-job-sales-invoice"></a><span data-ttu-id="8eb06-113">Een projectverkoopfactuur maken en boeken</span><span class="sxs-lookup"><span data-stu-id="8eb06-113">To create and post a job sales invoice</span></span>
<span data-ttu-id="8eb06-114">U kunt een factuur maken voor een project of voor één of meer projecttaken voor een klant, wanneer ofwel het werk dat moet worden gefactureerd voltooid is ofwel de datum voor facturering op basis van een factureringsschema is bereikt.</span><span class="sxs-lookup"><span data-stu-id="8eb06-114">You can create an invoice for a job or for one or more job tasks for a customer when either the work to be invoiced is complete or the date for invoicing based on an invoicing schedule has been reached.</span></span>

<span data-ttu-id="8eb06-115">Vanuit de pagina **Projecten** kunt u een klant factureren door het project te selecteren en vervolgens de actie **Projectverkoopfactuur maken** te kiezen.</span><span class="sxs-lookup"><span data-stu-id="8eb06-115">From the **Jobs** page, you can invoice a customer by selecting the job, and then choosing the **Create Job Sales Invoice** action.</span></span> <span data-ttu-id="8eb06-116">In de volgende procedure wordt beschreven hoe u een batchverwerking gebruikt om meerdere projecten te factureren.</span><span class="sxs-lookup"><span data-stu-id="8eb06-116">The following procedure shows how to use a batch job to invoice multiple jobs.</span></span>  

1. <span data-ttu-id="8eb06-117">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopfactuur project maken** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="8eb06-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Job Create Sales Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8eb06-118">Vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="8eb06-118">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="8eb06-119">Stel filters in als u de projecten wilt beperken die door de batchverwerking worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="8eb06-119">Set filters if you want to limit the jobs that the batch job will process.</span></span>
4. <span data-ttu-id="8eb06-120">Kies de knop **OK** om de facturen te maken.</span><span class="sxs-lookup"><span data-stu-id="8eb06-120">Choose the **OK** button to create the invoices.</span></span>  

## <a name="to-create-multiple-job-sales-invoices-from-job-planning-lines"></a><span data-ttu-id="8eb06-121">Meerdere projectverkoopfacturen maken vanuit projectplanningsregels</span><span class="sxs-lookup"><span data-stu-id="8eb06-121">To create multiple job sales invoices from job planning lines</span></span>
<span data-ttu-id="8eb06-122">U kunt een factuur maken vanuit een projectplanningsregel en op dat moment de hoeveelheid van het artikel, resource of grootboekrekening die u wilt factureren, aangeven.</span><span class="sxs-lookup"><span data-stu-id="8eb06-122">You can create an invoice from a job planning lines, and indicate at that time the quantity of the item, resource, or general ledger account that you want to invoice.</span></span>

1. <span data-ttu-id="8eb06-123">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projecten** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="8eb06-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="8eb06-124">Open een relevant project.</span><span class="sxs-lookup"><span data-stu-id="8eb06-124">Open a relevant job.</span></span>
3. <span data-ttu-id="8eb06-125">Selecteer een projecttaak waarvoor **Boeking** de **projecttaaksoort** is, en kies vervolgens de actie **Projectplanningsregels**.</span><span class="sxs-lookup"><span data-stu-id="8eb06-125">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="8eb06-126">Voer op een projectplanningsregel in het veld **Aantal te verplaatsen naar factuur** de hoeveelheid van het artikel, de resource en het soort grootboekrekening dat u wilt factureren in.</span><span class="sxs-lookup"><span data-stu-id="8eb06-126">On a job planning line, in the **Qty. To Transfer to Invoice** field, enter the quantity of the item, resource, general ledger account type that you want to invoice.</span></span>  
5. <span data-ttu-id="8eb06-127">Kies de actie **Verkoopfactuur maken**.</span><span class="sxs-lookup"><span data-stu-id="8eb06-127">Choose the **Create Sales Invoice** action.</span></span>
6. <span data-ttu-id="8eb06-128">Voer op de pagina **Verkoopfactuur project maken** de boekingsdatum in en of u een nieuwe factuur wilt maken of toevoegen aan deze factuur of aan een bestaande factuur.</span><span class="sxs-lookup"><span data-stu-id="8eb06-128">On the **Job Create Sales Invoice** page, enter the posting date and whether you want to create a new invoice or append this invoice to an existing one.</span></span>
7. <span data-ttu-id="8eb06-129">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="8eb06-129">Choose the **OK** button.</span></span>  

    <span data-ttu-id="8eb06-130">Op de projectplanningsregel, in het veld **Aantal overgebracht naar factuur** ziet u de hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="8eb06-130">On the job planning line, in the **Qty. Transferred to Invoice** field, you can see the quantity.</span></span>
8. <span data-ttu-id="8eb06-131">Kies op de pagina **Projectplanningsregels** de actie **Verkoopfacturen/-creditnota's**.</span><span class="sxs-lookup"><span data-stu-id="8eb06-131">On the **Job Planning Lines** page, choose the **Sales Invoices/Credit Memos** action.</span></span>

    <span data-ttu-id="8eb06-132">De pagina **Verkoopfactuur** wordt geopend met het aantal dat u naar de factuur hebt verzonden.</span><span class="sxs-lookup"><span data-stu-id="8eb06-132">The **Sales Invoice** page opens, showing the quantity that you have transferred to the invoice.</span></span>  
9. <span data-ttu-id="8eb06-133">Breng eventuele aanvullende wijzigingen aan en kies vervolgens de actie **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="8eb06-133">Make any additional changes, and then choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="8eb06-134">De bovengenoemde procedure is soortgelijk voor het maken, controleren en boeken van een aan een project gerelateerde verkoopcreditnota.</span><span class="sxs-lookup"><span data-stu-id="8eb06-134">The above procedure is similar for creating, reviewing, and posting a job-related sales credit memo.</span></span>

## <a name="to-calculate-and-post-job-completion-entries"></a><span data-ttu-id="8eb06-135">Projectvoltooiingsposten berekenen en boeken</span><span class="sxs-lookup"><span data-stu-id="8eb06-135">To calculate and post job completion entries</span></span>
<span data-ttu-id="8eb06-136">Wanneer u alle activiteiten voor een project hebt uitgevoerd, waaronder gebruiksboekingen en -facturering, moet u het project bijwerken om de **Status** in te stellen op **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="8eb06-136">When you have completed all activities for a job, including usage posting and invoicing, you must update the job to have a **Status** of **Completed**.</span></span> <span data-ttu-id="8eb06-137">Vervolgens moet u eventueel OHW tegenboeken dat naar het grootboek is geboekt.</span><span class="sxs-lookup"><span data-stu-id="8eb06-137">Then, you must reverse any WIP that has been posted to the general ledger.</span></span>

1. <span data-ttu-id="8eb06-138">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projecten** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="8eb06-138">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8eb06-139">Selecteer een open project en kies vervolgens de actie **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="8eb06-139">Select an open job, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="8eb06-140">Selecteer in het veld **Status** de optie **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="8eb06-140">In the **Status** field, select **Completed**.</span></span>
4. <span data-ttu-id="8eb06-141">Volg de hulpstappen om OHW te berekenen en te boeken.</span><span class="sxs-lookup"><span data-stu-id="8eb06-141">Follow the assistance steps to calculate and post WIP.</span></span> <span data-ttu-id="8eb06-142">Of volg stap 5 en 6 om dit handmatig te doen.</span><span class="sxs-lookup"><span data-stu-id="8eb06-142">Alternatively, follows steps 5 and 6 to do so manually.</span></span>  
5. <span data-ttu-id="8eb06-143">Kies de actie **OHW berekenen**.</span><span class="sxs-lookup"><span data-stu-id="8eb06-143">Choose the **Calculate WIP** action.</span></span>
6. <span data-ttu-id="8eb06-144">Vul op de pagina **OHW voor project berekenen** indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="8eb06-144">On the **Job Calculate WIP** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="8eb06-145">De OHW-posten voor het project die worden gemaakt door het uitvoeren van de batchverwerking, hebben nu een vinkje in het selectievak **Project voltooid** om aan te geven dat het voltooiingsposten zijn.</span><span class="sxs-lookup"><span data-stu-id="8eb06-145">The job WIP entries created by running the batch job will have the **Job Complete** check box selected to show that they are completion entries.</span></span>  
7. <span data-ttu-id="8eb06-146">Kies de actie **Project-OHW naar GB boeken**.</span><span class="sxs-lookup"><span data-stu-id="8eb06-146">Choose the **Job Post WIP to G/L** action.</span></span>
8. <span data-ttu-id="8eb06-147">Vul op de pagina **Project-OHW naar GB boeken** indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="8eb06-147">On the **Job Post WIP to G/L** page, fill in the fields as necessary.</span></span>  

     <span data-ttu-id="8eb06-148">De OHW-grootboekposten voor het project die worden gemaakt door het uitvoeren van de batchverwerking hebben nu een vinkje in het selectievak **Project voltooid** om aan te geven dat het voltooide posten zijn.</span><span class="sxs-lookup"><span data-stu-id="8eb06-148">The job WIP general ledger entries created by running the batch job will have the **Job Complete** check box selected to show they are completion entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="8eb06-149">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8eb06-149">See Also</span></span>
[<span data-ttu-id="8eb06-150">Projecten beheren</span><span class="sxs-lookup"><span data-stu-id="8eb06-150">Managing Projects</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="8eb06-151">Financiën</span><span class="sxs-lookup"><span data-stu-id="8eb06-151">Finance</span></span>](finance.md)  
<span data-ttu-id="8eb06-152">[Inkoop](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="8eb06-152">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="8eb06-153">[Verkoop](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="8eb06-153">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="8eb06-154">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8eb06-154">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
