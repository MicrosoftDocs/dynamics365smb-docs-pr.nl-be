---
title: Servicecontracten opstellen | Microsoft Docs
description: Leer hoe u servicecontracten opstelt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 216bbd775c66fca619d792ff578d198405fc7612
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781543"
---
# <a name="set-up-service-contracts"></a><span data-ttu-id="91287-103">Servicecontracten instellen</span><span class="sxs-lookup"><span data-stu-id="91287-103">Set Up Service Contracts</span></span>
<span data-ttu-id="91287-104">Voordat u met contracten kunt werken, moet u het volgende instellen:</span><span class="sxs-lookup"><span data-stu-id="91287-104">Before you can work with contracts, you must set up the following:</span></span> 

* <span data-ttu-id="91287-105">**Servicecontractgroepen**, waarmee gerelateerde servicecontracten worden verzameld.</span><span class="sxs-lookup"><span data-stu-id="91287-105">**Service contract groups**, which gather service contracts that are related in some way.</span></span>
* <span data-ttu-id="91287-106">**Servicecontractboekingsgroepen**, die worden gebruikt om de servicecontractboekingen te groeperen voor servicefacturen die worden gemaakt voor servicecontracten.</span><span class="sxs-lookup"><span data-stu-id="91287-106">**Service contract account groups**, which are used to group the service contract accounts together for service invoices created for service contracts.</span></span> <span data-ttu-id="91287-107">U wijst deze groepen toe aan servicecontracten.</span><span class="sxs-lookup"><span data-stu-id="91287-107">You assign these groups to service contracts.</span></span>  
* <span data-ttu-id="91287-108">**Contractsjablonen** waarmee contractindelingen worden gedefinieerd van contracten waarin de meestvoorkomende servicecontractdetails zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="91287-108">**Contract templates** that define contract layouts of contracts that include the most commonly used service contract details.</span></span> <span data-ttu-id="91287-109">U kunt servicecontractoffertes maken met sjablonen.</span><span class="sxs-lookup"><span data-stu-id="91287-109">When you create service contract quotes, you can create them by using templates.</span></span> <span data-ttu-id="91287-110">Wanneer u een contractofferte maakt, bevatten de velden automatisch de inhoud van de sjabloonvelden.</span><span class="sxs-lookup"><span data-stu-id="91287-110">When you create a contract quote, the fields automatically contain the contents of the template fields.</span></span>
* <span data-ttu-id="91287-111">**Klantensjablonen** waarmee u offertes voor contacten of potentiële klanten kunt maken die niet als klant zijn geregistreerd in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="91287-111">**Customer templates** that let you create quotes for contacts or potential customers who are not registered as customers in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="to-set-up-a-service-contract-group"></a><span data-ttu-id="91287-112">Servicecontractgroepen instellen</span><span class="sxs-lookup"><span data-stu-id="91287-112">To set up a service contract group</span></span>  
1. <span data-ttu-id="91287-113">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Servicecontractgroepen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="91287-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Contract Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="91287-114">Vul de velden in.</span><span class="sxs-lookup"><span data-stu-id="91287-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="91287-115">Schakel het selectievakje **Alleen kort. op contr.-orders** in als u wilt dat contract- of servicekortingen alleen geldig zijn voor contractserviceorders, zoals onderhoud.</span><span class="sxs-lookup"><span data-stu-id="91287-115">Choose the **Disc. on Contr. Orders Only** check box if you want contract or service discounts to be valid only for contract service orders, such as maintenance.</span></span>  

## <a name="to-set-up-a-service-contract-account-group"></a><span data-ttu-id="91287-116">Servicecontractboekingsgroepen instellen</span><span class="sxs-lookup"><span data-stu-id="91287-116">To set up a service contract account group</span></span>  
1. <span data-ttu-id="91287-117">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Servicecontractboekingsgroepen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="91287-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Serv. Contract Account Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="91287-118">Maak een nieuwe servicecontractboekingsgroep.</span><span class="sxs-lookup"><span data-stu-id="91287-118">Create a new service contract account group.</span></span>   
3. <span data-ttu-id="91287-119">Vul de velden **Code** en **Omschrijving** in.</span><span class="sxs-lookup"><span data-stu-id="91287-119">Fill in the **Code** and **Description** fields.</span></span> <span data-ttu-id="91287-120">Met deze velden wordt de servicecontractboekingsgroep omschreven.</span><span class="sxs-lookup"><span data-stu-id="91287-120">These fields describe the service account group.</span></span>  
4. <span data-ttu-id="91287-121">Vul het veld **Niet-vooruitbetaalde contractenrekening** in. Kies het nummer van de niet-vooruitbetaalde grootboekrekening.</span><span class="sxs-lookup"><span data-stu-id="91287-121">Fill in the **Non-Prepaid Contract Acc.** field, choose general ledger account number for the non-prepaid account.</span></span>  
5. <span data-ttu-id="91287-122">Kies in het veld **Vooruitbetaalde contractenrekening** het nummer van de vooruitbetaalde grootboekrekening.</span><span class="sxs-lookup"><span data-stu-id="91287-122">In the **Prepaid Contract Acc.** field, choose the general ledger account number for the prepaid account.</span></span>  

## <a name="to-set-up-a-contract-template"></a><span data-ttu-id="91287-123">Contractsjablonen instellen</span><span class="sxs-lookup"><span data-stu-id="91287-123">To set up a contract template</span></span>  
1. <span data-ttu-id="91287-124">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Servicecontractsjablonen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="91287-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Contract Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="91287-125">Maak een nieuwe servicecontractsjabloon.</span><span class="sxs-lookup"><span data-stu-id="91287-125">Create a new service contract template.</span></span>  
3. <span data-ttu-id="91287-126">Selecteer in het veld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="91287-126">In the **No.**</span></span> <span data-ttu-id="91287-127">een nummer voor de contractsjabloon.</span><span class="sxs-lookup"><span data-stu-id="91287-127">field, enter a number for the contract template.</span></span>  
  
     <span data-ttu-id="91287-128">Als u op de pagina **Servicebeheerinstellingen** nummerreeksen voor contractsjablonen hebt ingesteld, kunt u ook op Enter drukken om het eerstvolgende beschikbare contractsjabloonnummer in te voeren.</span><span class="sxs-lookup"><span data-stu-id="91287-128">Alternatively, if you have set up number series for contract templates on the **Service Mgt. Setup** page, you can press the Enter key to enter the next available contract template number.</span></span> <span data-ttu-id="91287-129">Vul eventueel de andere velden in.</span><span class="sxs-lookup"><span data-stu-id="91287-129">Fill in the other fields if appropriate.</span></span>  
  
4. <span data-ttu-id="91287-130">Vul op het sneltabblad **Factuur** het veld **Serv.-contractboekingsgroep**, de **Factuurperiode**, enzovoort in.</span><span class="sxs-lookup"><span data-stu-id="91287-130">On the **Invoice** FastTab, fill in the **Serv. Contract Acc. Group Code** field, the **Invoice Period**, and so on.</span></span> <span data-ttu-id="91287-131">Vul eventueel de andere velden in.</span><span class="sxs-lookup"><span data-stu-id="91287-131">Fill in the other fields if appropriate.</span></span>  
5. <span data-ttu-id="91287-132">Kies de actie **Servicekortingen** om contractkortingen toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="91287-132">Choose the **Service Discounts** action to add contract discounts.</span></span>  

## <a name="to-set-up-a-customer-template"></a><span data-ttu-id="91287-133">Klantsjablonen instellen</span><span class="sxs-lookup"><span data-stu-id="91287-133">To set up a customer template</span></span>  
1. <span data-ttu-id="91287-134">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klantsjablonen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="91287-134">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="91287-135">Maak een nieuwe klantensjabloonkaart.</span><span class="sxs-lookup"><span data-stu-id="91287-135">Create a new customer template card.</span></span>  
3. <span data-ttu-id="91287-136">Typ op het sneltabblad **Algemeen** een code en omschrijving voor de klantensjabloonkaart in de velden **Code** en **Omschrijving**.</span><span class="sxs-lookup"><span data-stu-id="91287-136">On the **General** FastTab, enter a code and a description for the customer template in the **Code** and **Description** fields respectively.</span></span> 
4. <span data-ttu-id="91287-137">Als u zoekcriteria wilt opgeven, vult u de andere velden in, zoals **Land-/regiocode**, **Regio** en **Taal**.</span><span class="sxs-lookup"><span data-stu-id="91287-137">To define search criteria, fill in the other fields, such as **Country/Region Code**, **Territory Code**, and **Language Code**.</span></span>  
5. <span data-ttu-id="91287-138">Vul de velden **Bedrijfsboekingsgroep** en **Klantboekingsgroep** in.</span><span class="sxs-lookup"><span data-stu-id="91287-138">Fill in the **Gen. Bus. Posting Group** and **Customer Posting Group** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="91287-139">Zie ook</span><span class="sxs-lookup"><span data-stu-id="91287-139">See Also</span></span>
[<span data-ttu-id="91287-140">CRM - Service instellen</span><span class="sxs-lookup"><span data-stu-id="91287-140">Setting Up Service Management</span></span>](service-setup-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]