---
title: "De relatie tussen kostensoorten en grootboekrekeningen definiëren | Microsoft Docs"
description: Leer hoe u de relatie tussen de kostensoort en de grootboekrekening definieert.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost types, general ledger
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0f2f30b8b56ae4afcff230a7934a6bcac4d205db
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts"></a><span data-ttu-id="78596-103">De relatie tussen de kostensoorten en grootboekrekeningen definiëren</span><span class="sxs-lookup"><span data-stu-id="78596-103">Defining the Relationship Between Cost Types and General Ledger Accounts</span></span>
<span data-ttu-id="78596-104">De relatie tussen het kostensoort en de grootboekrekening wordt gemaakt in het kostensoort en in de grootboekrekening.</span><span class="sxs-lookup"><span data-stu-id="78596-104">The relationship between the cost type and the general ledger account is created in the cost type and in the general ledger account.</span></span>  

* <span data-ttu-id="78596-105">Het veld **Grootboekrekeningbereik** in de tabel **Kostensoort** bepaalt welke grootboekrekeningen tot een kostensoort behoren.</span><span class="sxs-lookup"><span data-stu-id="78596-105">The **G/L Account Range** field in the **Cost Type** table establishes which general ledger accounts belong to a cost type.</span></span>  
* <span data-ttu-id="78596-106">Het veld **Nr. saldokostensoort**</span><span class="sxs-lookup"><span data-stu-id="78596-106">The **Cost Type No.**</span></span> <span data-ttu-id="78596-107">in het rekeningschema bepaalt tot welk kostensoort een grootboekrekening behoort.</span><span class="sxs-lookup"><span data-stu-id="78596-107">field in the chart of accounts establishes which cost type a general ledger account belongs to.</span></span>  

<span data-ttu-id="78596-108">Deze twee velden worden automatisch ingevuld wanneer u de functie **Kostensoorten ophalen uit rekeningschema** gebruikt.</span><span class="sxs-lookup"><span data-stu-id="78596-108">These two fields are filled automatically when you use the **Get Cost Types from Chart of Accounts** function.</span></span>  

## <a name="relationship-between-general-ledger-accounts-and-cost-types"></a><span data-ttu-id="78596-109">Relatie tussen de grootboekrekeningen en kostensoorten</span><span class="sxs-lookup"><span data-stu-id="78596-109">Relationship Between General Ledger Accounts and Cost Types</span></span>  
<span data-ttu-id="78596-110">Er bestaat een n:1-relatie tussen de grootboekrekeningen en kostensoorten</span><span class="sxs-lookup"><span data-stu-id="78596-110">There is an n:1 relationship between general ledger accounts and cost types.</span></span> <span data-ttu-id="78596-111">Verschillende grootboekrekeningen kunnen tot één kostensoort behoren, maar elke afzonderlijke grootboekrekening behoort maar tot één kostensoort.</span><span class="sxs-lookup"><span data-stu-id="78596-111">Several general ledger accounts can belong to one cost type, but each general ledger account belongs to only one cost type.</span></span> <span data-ttu-id="78596-112">De volgende tabel beschrijft de detail in de relatie.</span><span class="sxs-lookup"><span data-stu-id="78596-112">The following table describes the details in the relationship.</span></span>  

|<span data-ttu-id="78596-113">Relatie</span><span class="sxs-lookup"><span data-stu-id="78596-113">Relationship</span></span>|<span data-ttu-id="78596-114">**Grootboekrekeningbereik**</span><span class="sxs-lookup"><span data-stu-id="78596-114">**G/L Account Range**</span></span>|<span data-ttu-id="78596-115">**Nr. kostensoort**</span><span class="sxs-lookup"><span data-stu-id="78596-115">**Cost Type No.**</span></span>|  
|------------------|------------------------------------------------|-------------------------------------------|  
|<span data-ttu-id="78596-116">Één grootboekrekening voor elk kostensoort</span><span class="sxs-lookup"><span data-stu-id="78596-116">One general ledger account for each cost type</span></span>|<span data-ttu-id="78596-117">Eén grootboekrekening</span><span class="sxs-lookup"><span data-stu-id="78596-117">One general ledger account</span></span>|<span data-ttu-id="78596-118">Eén kostensoort</span><span class="sxs-lookup"><span data-stu-id="78596-118">One cost type</span></span>|  
|<span data-ttu-id="78596-119">Verschillende grootboekrekeningen voor één kostensoort</span><span class="sxs-lookup"><span data-stu-id="78596-119">Several general ledger accounts for one cost type</span></span>|<span data-ttu-id="78596-120">Bijvoorbeeld rekeningenbereik grootboek 7110..7193 voor elke grootboekrekening</span><span class="sxs-lookup"><span data-stu-id="78596-120">General ledger account range, for example, 7110..7193 for each general ledger account</span></span>|<span data-ttu-id="78596-121">Voor elke grootboekrekening in het bereik is slechts één kostensoort</span><span class="sxs-lookup"><span data-stu-id="78596-121">For each general ledger account in the range, there is only one cost type</span></span>|  
|<span data-ttu-id="78596-122">Kostensoorten zonder overeenkomende grootboekrekeningen</span><span class="sxs-lookup"><span data-stu-id="78596-122">Cost types without corresponding general ledger accounts</span></span>|<Empty>||  
|<span data-ttu-id="78596-123">Grootboekrekeningen waarvan de posten niet overgebracht worden</span><span class="sxs-lookup"><span data-stu-id="78596-123">General ledger accounts whose entries will not be transferred</span></span>||<Empty>|  

## <a name="cost-types-without-a-relationship-to-the-general-ledger"></a><span data-ttu-id="78596-124">Kostensoorten zonder relatie met het grootboek</span><span class="sxs-lookup"><span data-stu-id="78596-124">Cost Types Without a Relationship to the General Ledger</span></span>  
<span data-ttu-id="78596-125">Er bestaat mogelijk geen relatie tussen een kostensoort en grootboekrekeningen als aan een van de volgende voorwaarden wordt voldaan:</span><span class="sxs-lookup"><span data-stu-id="78596-125">A cost type may not have a relationship to general ledger accounts if one of the following conditions is true:</span></span>  

* <span data-ttu-id="78596-126">Rekeningen voor operationeel boekhouden zoals voor het de berekenen van rente en afschrijvingen, nemen alleen de kosten mee van de operationele boekhouding.</span><span class="sxs-lookup"><span data-stu-id="78596-126">Accounts for operational accounting, such as Calc. Interest and Depreciation, only take costs from the operational accounting.</span></span>  
* <span data-ttu-id="78596-127">Ondersteunende kostensoorten, zoals kostensoorten 9901, 9902 en 9903 in de [!INCLUDE[d365fin](includes/d365fin_md.md)]-database , worden gebruikt als credit- of debet-rekeningen voor toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="78596-127">Helping cost types, such as cost types 9901, 9902, and 9903 in the [!INCLUDE[d365fin](includes/d365fin_md.md)] database, are used as credit and debit accounts for allocations.</span></span>  
* <span data-ttu-id="78596-128">De ondersteunende rekening, 9920 in de [!INCLUDE[d365fin](includes/d365fin_md.md)]-database, bevat de werkelijke overlopende transitoria die het verschil laten zien tussen de kosten en de onkosten uit het grootboek.</span><span class="sxs-lookup"><span data-stu-id="78596-128">The helping account, 9920 in the [!INCLUDE[d365fin](includes/d365fin_md.md)] database, contains actual accruals that show the difference between costs and the expense from the general ledger.</span></span>  

## <a name="see-also"></a><span data-ttu-id="78596-129">Zie ook</span><span class="sxs-lookup"><span data-stu-id="78596-129">See Also</span></span>  
[<span data-ttu-id="78596-130">Kosten verantwoorden</span><span class="sxs-lookup"><span data-stu-id="78596-130">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="78596-131">[Kostenboekhouding instellen](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="78596-131">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
[<span data-ttu-id="78596-132">Kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="78596-132">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="78596-133">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="78596-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

