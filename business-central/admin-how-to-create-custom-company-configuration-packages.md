---
title: Aangepaste configuratiepakketten voor bedrijven maken | Microsoft Docs
description: Naarmate uw bedrijf groeit, zult u waarschijnlijk gaan vertrouwen op een set bedrijfstypen die u met de meeste van uw klanten gebruikt. U kunt uw implementatieproces stroomlijnen door van deze typen configuratiepakketten voor bedrijven te maken die beschikbaar zijn voor hergebruik.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e26174fcf723e13ef5a9ed0b386006c0439e1c7a
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="71ef5-104">Aangepaste configuratiepakketten voor bedrijven maken</span><span class="sxs-lookup"><span data-stu-id="71ef5-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="71ef5-105">Naarmate uw bedrijf groeit, zult u waarschijnlijk gaan vertrouwen op een set bedrijfstypen die u met de meeste van uw klanten gebruikt.</span><span class="sxs-lookup"><span data-stu-id="71ef5-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="71ef5-106">U kunt uw implementatieproces stroomlijnen door van deze typen configuratiepakketten voor bedrijven te maken die beschikbaar zijn voor hergebruik.</span><span class="sxs-lookup"><span data-stu-id="71ef5-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="71ef5-107">In het algemeen maakt u een configuratiepakket per functiegebied. Zo kunt u bijvoorbeeld een pakket maken voor uw productiefunctionaliteit.</span><span class="sxs-lookup"><span data-stu-id="71ef5-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="71ef5-108">Dat kunt u vervolgens toepassen en nieuwe gebieden in een bedrijf instellen als u ze nodig hebt</span><span class="sxs-lookup"><span data-stu-id="71ef5-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="71ef5-109">Een andere benadering zou zijn om een pakket te maken dat de tabellen bevat waarin de instellingen worden gedefinieerd, zoals de volgende:</span><span class="sxs-lookup"><span data-stu-id="71ef5-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="71ef5-110">VA-instellingen</span><span class="sxs-lookup"><span data-stu-id="71ef5-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="71ef5-111">Grootboekinstellingen</span><span class="sxs-lookup"><span data-stu-id="71ef5-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="71ef5-112">Voorraadinstellingen</span><span class="sxs-lookup"><span data-stu-id="71ef5-112">Inventory Setup</span></span>  
-   <span data-ttu-id="71ef5-113">Productie-instellingen</span><span class="sxs-lookup"><span data-stu-id="71ef5-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="71ef5-114">Inkoopinstellingen</span><span class="sxs-lookup"><span data-stu-id="71ef5-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="71ef5-115">Marketinginstellingen</span><span class="sxs-lookup"><span data-stu-id="71ef5-115">Marketing Setup</span></span>  
-   <span data-ttu-id="71ef5-116">Service-instellingen</span><span class="sxs-lookup"><span data-stu-id="71ef5-116">Service Setup</span></span>  
-   <span data-ttu-id="71ef5-117">Verkoopinstellingen</span><span class="sxs-lookup"><span data-stu-id="71ef5-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="71ef5-118">Magazijninstellingen</span><span class="sxs-lookup"><span data-stu-id="71ef5-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="71ef5-119">Boekingsgroepinstellingen</span><span class="sxs-lookup"><span data-stu-id="71ef5-119">General Posting Setup</span></span>  
-   <span data-ttu-id="71ef5-120">Btw-boekingsgroepinstellingen</span><span class="sxs-lookup"><span data-stu-id="71ef5-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="71ef5-121">Voorraadboekingsinstellingen</span><span class="sxs-lookup"><span data-stu-id="71ef5-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="71ef5-122">Als u een complete lijst met instellingstabellen wilt zien, kiest u het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Instellingen** in en kiest u vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="71ef5-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="71ef5-123">Een aangepast configuratiepakket voor een bedrijf maken</span><span class="sxs-lookup"><span data-stu-id="71ef5-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="71ef5-124">Definieer een nieuwe [!INCLUDE[d365fin](includes/d365fin_md.md)],</span><span class="sxs-lookup"><span data-stu-id="71ef5-124">Create a new [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="71ef5-125">***NIET MOGELIJK Koppeling naar Help voor "Een nieuwe tenant maken"***.</span><span class="sxs-lookup"><span data-stu-id="71ef5-125">***NOT POSSIBLE Link to help for "Creating a New Tenant"***.</span></span>   
2.  <span data-ttu-id="71ef5-126">Maak een nieuw bedrijf voor de branche- of oplossingssjabloon.</span><span class="sxs-lookup"><span data-stu-id="71ef5-126">Create a new company for the industry or solution template.</span></span> <span data-ttu-id="71ef5-127">Zie [Een nieuw bedrijf maken](admin-how-to-create-a-new-company.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="71ef5-127">For more information, see [Create a New Company](admin-how-to-create-a-new-company.md).</span></span>  
3.  <span data-ttu-id="71ef5-128">Stel het nieuwe bedrijf in op de door u benodigde wijze.</span><span class="sxs-lookup"><span data-stu-id="71ef5-128">Setup the new company in the way you need.</span></span> <span data-ttu-id="71ef5-129">Vul alle vereiste instellingentabellen in.</span><span class="sxs-lookup"><span data-stu-id="71ef5-129">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="71ef5-130">Open het nieuw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="71ef5-130">Open the new company.</span></span>
5. <span data-ttu-id="71ef5-131">Open het venster **Configuratiewerkblad**.</span><span class="sxs-lookup"><span data-stu-id="71ef5-131">Open the **Configuration Worksheet** window.</span></span>  
6.  <span data-ttu-id="71ef5-132">Voeg de tabellen die u wilt overbrengen naar een ander bedrijf toe aan het werkblad.</span><span class="sxs-lookup"><span data-stu-id="71ef5-132">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="71ef5-133">Wijs de werkbladregels toe aan het pakket.</span><span class="sxs-lookup"><span data-stu-id="71ef5-133">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="71ef5-134">Maak een vragenlijst voor de meest gebruikte instellingentabel.</span><span class="sxs-lookup"><span data-stu-id="71ef5-134">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="71ef5-135">Stel configuratiesjablonen op om het gemakkelijker te maken om hoofdgegevens, zoals klanten of artikelen, te definiëren.</span><span class="sxs-lookup"><span data-stu-id="71ef5-135">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="71ef5-136">Exporteer uw pakket als een .rapidstart-bestand.</span><span class="sxs-lookup"><span data-stu-id="71ef5-136">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="71ef5-137">Zie ook</span><span class="sxs-lookup"><span data-stu-id="71ef5-137">See Also</span></span>  
[<span data-ttu-id="71ef5-138">Een bedrijf met RapidStart Services instellen</span><span class="sxs-lookup"><span data-stu-id="71ef5-138">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="71ef5-139">Beheer</span><span class="sxs-lookup"><span data-stu-id="71ef5-139">Administration</span></span>](admin-setup-and-administration.md)

