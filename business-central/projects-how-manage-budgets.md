---
title: Een budget instellen en beheren voor een project| Microsoft Docs
description: Beschrijft hoe u resources plant en de kosten van een project voorspelt en beheert door een budget voor elk project in te stellen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 995d181496dc1827f21c0b3edd9e52dd6c15c297
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="manage-job-budgets"></a><span data-ttu-id="88a36-103">Projectbudgetten maken</span><span class="sxs-lookup"><span data-stu-id="88a36-103">Manage Job Budgets</span></span>
<span data-ttu-id="88a36-104">Voor elk project kunt u een budget instellen.</span><span class="sxs-lookup"><span data-stu-id="88a36-104">You can set up a budget for each job.</span></span> <span data-ttu-id="88a36-105">Het budget wordt gebruikt om de resources te plannen die.u aan een project toewijst.</span><span class="sxs-lookup"><span data-stu-id="88a36-105">The budget is used to plan the resources that you allocate to a job.</span></span> <span data-ttu-id="88a36-106">Dit kan een algemeen budget zijn met weinig posten of een budget met veel posten die in activiteitsniveaus zijn onderverdeeld.</span><span class="sxs-lookup"><span data-stu-id="88a36-106">The budget can be either general with few entries or it can contain more entries that are divided into activity levels.</span></span> <span data-ttu-id="88a36-107">U kunt vervolgens de gebudgetteerde bedragen vergelijken met het werkelijke gebruik zoals vastgelegd in het projectdagboek.</span><span class="sxs-lookup"><span data-stu-id="88a36-107">You can then compare the budgeted amounts with the actual usage as recorded in the job journal.</span></span> <span data-ttu-id="88a36-108">Door verschillen tussen werkelijk en gebudgetteerd gebruik te controleren kunt u een lopend project controleren en de kwaliteit van toekomstige projecten verbeteren doordat kosten minder snel worden onderschat.</span><span class="sxs-lookup"><span data-stu-id="88a36-108">By monitoring differences between actual usage and budgeted usage, you can control an ongoing project and improve the quality of future jobs by reducing the risk of underestimating costs.</span></span>

<span data-ttu-id="88a36-109">In de volgende procedure wordt beschreven hoe u gebudgetteerde kosten inschat tijdens een planning.</span><span class="sxs-lookup"><span data-stu-id="88a36-109">The following procedure describes how to estimate budgeted costs during planning.</span></span> <span data-ttu-id="88a36-110">Voor informatie over het vastleggen van gebudgetteerde versus werkelijke projectprijzen en -kosten raadpleegt u [Gebruik voor projecten vastleggen](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="88a36-110">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>  

## <a name="JobBudgetCosts"></a> <span data-ttu-id="88a36-111">De gebudgetteerde kosten voor een project schatten</span><span class="sxs-lookup"><span data-stu-id="88a36-111">To estimate the budgeted costs for a job</span></span>
<span data-ttu-id="88a36-112">Wanneer een klant de prijs wil weten van een project dat op basis van gebruik wordt gefactureerd, moet u de gebudgetteerde kosten voor het project bepalen.</span><span class="sxs-lookup"><span data-stu-id="88a36-112">When a customer wants to know the price of a job that will be invoiced based on usage, you must have to determine the budgeted costs for the job.</span></span> <span data-ttu-id="88a36-113">U gebruikt hiervoor het venster **Projecttaakregels**.</span><span class="sxs-lookup"><span data-stu-id="88a36-113">You use the **Job Task Lines** window to do this.</span></span>

1. <span data-ttu-id="88a36-114">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projecten** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="88a36-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="88a36-115">Open een relevant project.</span><span class="sxs-lookup"><span data-stu-id="88a36-115">Open a relevant job.</span></span>
3. <span data-ttu-id="88a36-116">Selecteer een taakregel van het soort Boeking en kies vervolgens de actie **Projectplanningsregels**.</span><span class="sxs-lookup"><span data-stu-id="88a36-116">Select a task line of type Posting, and then choose the **Job Planning Lines** action.</span></span>
4. <span data-ttu-id="88a36-117">Vul op een nieuwe regel de velden indien nodig in.</span><span class="sxs-lookup"><span data-stu-id="88a36-117">On a new line, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

<span data-ttu-id="88a36-118">Raadpleeg voor het veld **Regelsoort** de volgende informatie.</span><span class="sxs-lookup"><span data-stu-id="88a36-118">For the **Line Type** field, refer to the following information.</span></span>  

| <span data-ttu-id="88a36-119">Regelsoort</span><span class="sxs-lookup"><span data-stu-id="88a36-119">Line Type</span></span> | <span data-ttu-id="88a36-120">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="88a36-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="88a36-121">**Budget en factureerbaar**</span><span class="sxs-lookup"><span data-stu-id="88a36-121">**Both Budget and Billable**</span></span> |<span data-ttu-id="88a36-122">De kosten en prijzen die zijn ingevoerd op de planningsregel, zijn de gebudgetteerde kosten voor de betreffende planningsregel.</span><span class="sxs-lookup"><span data-stu-id="88a36-122">The cost and price amounts entered on the planning line are the budgeted costs for the particular planning line.</span></span> <span data-ttu-id="88a36-123">Het prijsbedrag wordt gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="88a36-123">The price amount will be invoiced.</span></span> |
| <span data-ttu-id="88a36-124">**Budget**</span><span class="sxs-lookup"><span data-stu-id="88a36-124">**Budget**</span></span> |<span data-ttu-id="88a36-125">Er worden geen gebruikstoeslagen doorberekend aan de klant.</span><span class="sxs-lookup"><span data-stu-id="88a36-125">The customer is not charged for usage.</span></span> <span data-ttu-id="88a36-126">Gebruik kan nooit worden overgebracht naar een factuur, maar wordt wel nog gebruikt bij de OHW-berekening.</span><span class="sxs-lookup"><span data-stu-id="88a36-126">Usage is not transferred to an invoice, but will still be used in the calculation of WIP.</span></span> |
| <span data-ttu-id="88a36-127">**Factureerbaar**</span><span class="sxs-lookup"><span data-stu-id="88a36-127">**Billable**</span></span> |<span data-ttu-id="88a36-128">Er worden gebruikstoeslagen doorberekend aan de klant.</span><span class="sxs-lookup"><span data-stu-id="88a36-128">The customer is charged for usage.</span></span> <span data-ttu-id="88a36-129">Het gebruik wordt naar de factuur overgebracht en wordt gebaseerd op het aantal dat is opgegeven in het veld Te factureren aantal.</span><span class="sxs-lookup"><span data-stu-id="88a36-129">Usage is transferred to the invoice, based on the quantity specified in the Qty. to Transfer to Invoice field.</span></span> |

> [!NOTE]  
>   <span data-ttu-id="88a36-130">Het veld **Planningsdatum** voor de planningsregel bevat de datum waarop gebruik dat gerelateerd is aan de planningsregel, naar verwachting is voltooid.</span><span class="sxs-lookup"><span data-stu-id="88a36-130">The **Planning Date** field for the planning line contains the date when usage related to the planning line is expected to be completed.</span></span> <span data-ttu-id="88a36-131">Het is ook de datum waarop de planningsregel kan worden overgebracht naar een verkoopfactuur en geboekt.</span><span class="sxs-lookup"><span data-stu-id="88a36-131">It is also the date when the planning line may be transferred to a sales invoice and posted.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="88a36-132">Wanneer u het veld **Aantal** invult, wordt alle informatie over de totale verkoopprijs en de totale kostprijs berekend en ingevuld voor die planningsregel.</span><span class="sxs-lookup"><span data-stu-id="88a36-132">When you fill in the **Quantity** field, all total price and total cost information will be calculated and filled in for that planning line.</span></span> <span data-ttu-id="88a36-133">U kunt dit op elk gewenst moment wijzigen.</span><span class="sxs-lookup"><span data-stu-id="88a36-133">You can edit them at any time.</span></span>

<span data-ttu-id="88a36-134">In het veld **Projectkaart** kunt u nu een overzicht zien van de totale gebudgetteerde kosten, gebudgetteerde prijs, factureerbare kosten en factureerbare prijs voor elke taak.</span><span class="sxs-lookup"><span data-stu-id="88a36-134">In the **Job Card** window, you can now see a summary of the total budgeted costs, budgeted price, billable cost and billable price for each task.</span></span>

<span data-ttu-id="88a36-135">Voor informatie over het vastleggen van gebudgetteerde versus werkelijke projectprijzen en -kosten raadpleegt u [Gebruik voor projecten vastleggen](projects-how-record-job-usage.md).</span><span class="sxs-lookup"><span data-stu-id="88a36-135">For information about recording budgeted versus actual job prices and costs, see [Record Usage for Jobs](projects-how-record-job-usage.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="88a36-136">Zie ook</span><span class="sxs-lookup"><span data-stu-id="88a36-136">See Also</span></span>
[<span data-ttu-id="88a36-137">Projectbeheer</span><span class="sxs-lookup"><span data-stu-id="88a36-137">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="88a36-138">Financiën</span><span class="sxs-lookup"><span data-stu-id="88a36-138">Finance</span></span>](finance.md)  
<span data-ttu-id="88a36-139">[Inkoop](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="88a36-139">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="88a36-140">[Verkoop](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="88a36-140">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="88a36-141">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="88a36-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

