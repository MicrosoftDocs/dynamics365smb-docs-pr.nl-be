---
title: Een leverancierskaart maken om nieuwe leveranciers te registreren | Microsoft Docs
description: Meer informatie over hoe u een leverancierskaart maakt om een nieuwe leverancier te registreren.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7e8306ad65b41784e853dfc46a41c2deee997180
ms.sourcegitcommit: ab4141739a53ec100d42773f0da863fbeefa384f
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/14/2019
ms.locfileid: "2577243"
---
# <a name="register-new-vendors"></a><span data-ttu-id="5fcd1-103">Nieuwe leveranciers registreren</span><span class="sxs-lookup"><span data-stu-id="5fcd1-103">Register New Vendors</span></span>
<span data-ttu-id="5fcd1-104">Leveranciers leveren de producten die u verkoopt.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-104">Vendors provide the products that you sell.</span></span> <span data-ttu-id="5fcd1-105">Elke leverancier van wie u inkoopt, moet als een leverancierkaart zijn geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-105">Each vendor that you purchase from must be registered as a vendor card.</span></span>

<span data-ttu-id="5fcd1-106">Voordat u nieuwe leveranciers kunt vastleggen, moet u verschillende inkoopcodes instellen waaruit u kunt selecteren wanneer u leverancierskaarten invult.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-106">Before you can register new vendors, you must set up various purchase codes that you can select from when you fill vendor cards.</span></span> <span data-ttu-id="5fcd1-107">Wanneer alle vereiste stamgegevens zijn gemaakt, kunt u aanvullende gegevens voor de leverancier configureren, zoals het toekennen van een prioriteit aan de leverancier voor betalingsdoeleinden en u kunt artikelen vermelden die deze leverancier en andere leveranciers kunnen leveren.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-107">When all of the required master data is created, you can perform additional configuration of the vendor, such as prioritize the vendor for payment purposes and list items that the vendor and other vendors can supply.</span></span> <span data-ttu-id="5fcd1-108">Een andere reeks instellingen die u kunt opgeven, zijn de overeenkomsten met betrekking tot kortingen, prijzen en betalingswijzen.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-108">Another group of setup tasks for vendors is to record your agreements concerning discounts, prices, and payment methods.</span></span> <span data-ttu-id="5fcd1-109">Zie voor meer informatie [Inkoop instellen](purchasing-setup-purchasing.md).</span><span class="sxs-lookup"><span data-stu-id="5fcd1-109">For more information, see [Setting Up Purchasing](purchasing-setup-purchasing.md).</span></span>

<span data-ttu-id="5fcd1-110">Leverancierskaarten bevatten de informatie die is vereist om producten van de leverancier te kunnen kopen.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-110">Vendor cards hold the information that is required to buy products from the vendor.</span></span> <span data-ttu-id="5fcd1-111">Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md) en [Nieuwe artikelen registreren](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="5fcd1-111">For more information, see [Record Purchases](purchasing-how-record-purchases.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="5fcd1-112">Als leveranciersjablonen voor verschillende leveranciersoorten bestaan, wordt een pagina automatisch weergegeven wanneer u een nieuwe leverancierskaart maakt, van waaruit u een geschikte leveranciersjabloon kunt selecteren.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-112">If vendor templates exist for different vendor types, then a page appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="5fcd1-113">Als er slechts één leveranciersjabloon bestaat, gebruiken nieuwe leverancierkaarten altijd deze sjabloon.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-113">If only one vendor template exists, then new vendor cards always use that template.</span></span>
<br><br>
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE3PZtd]

## <a name="to-create-a-new-vendor-card"></a><span data-ttu-id="5fcd1-114">Een nieuwe leverancierskaart maken</span><span class="sxs-lookup"><span data-stu-id="5fcd1-114">To create a new vendor card</span></span>
1. <span data-ttu-id="5fcd1-115">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Leveranciers** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="5fcd1-116">Kies op de pagina **Leveranciers** de optie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-116">On the **Vendors** page, Choose **New**.</span></span>

    <span data-ttu-id="5fcd1-117">Wanneer er meer dan één leveranciersjabloon bestaat, opent er een pagina waarin u een leveranciersjabloon kunt selecteren.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-117">If more than one vendor template exists, then a page opens from which you can select a vendor template.</span></span> <span data-ttu-id="5fcd1-118">In dat geval volgt u de volgende twee stappen.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-118">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="5fcd1-119">Kies op de pagina **Selecteer een sjabloon voor een nieuwe leverancier** de sjabloon die u wilt gebruiken voor de nieuwe leverancierskaart.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-119">On the **Select a template for a new vendor** page, choose the template that you want to use for the new vendor card.</span></span>
4. <span data-ttu-id="5fcd1-120">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-120">Choose the **OK** button.</span></span> <span data-ttu-id="5fcd1-121">Een nieuwe leverancierskaart wordt geopend met enkele velden ingevuld met informatie uit de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-121">A new vendor card opens with some fields filled with information from the template.</span></span>
5. <span data-ttu-id="5fcd1-122">Ga door met velden op de leverancierskaart in te vullen of te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-122">Proceed to fill or change fields on the vendor card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="5fcd1-123">Als u het factuuradres dat voor elke factuur van een leverancier wordt gebruikt niet kent, vult u het veld **Betaaladres** niet in.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-123">If you do not know the invoicing address that will be used for every invoice from a vendor, do not fill in the **Pay-to** field.</span></span> <span data-ttu-id="5fcd1-124">Kies in dat geval het nummer van de factuurleverancier nadat u een inkoopofferte, inkooporder of inkoopkop hebt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-124">Instead, choose the pay-to vendor number after you have set up a purchase quote, order, or invoice header.</span></span>

<span data-ttu-id="5fcd1-125">De leverancier is nu geregistreerd en de leverancierskaart is klaar om voor inkoopdocumenten te worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-125">The vendor is now registered, and the vendor card is ready to be used on purchase documents.</span></span>

<span data-ttu-id="5fcd1-126">Als u deze leverancierskaart als sjabloon wilt gebruiken wanneer u nieuwe leverancierskaarten maakt, kunt u deze opslaan als leveranciersjabloon.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-126">If you want to use this vendor card as a template when you create new vendor cards, you can save it as a vendor template.</span></span> <span data-ttu-id="5fcd1-127">Zie de volgende onderwerpen voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-127">For more information, see the following section.</span></span>

## <a name="to-save-the-vendor-card-as-a-template"></a><span data-ttu-id="5fcd1-128">De leverancierskaart als sjabloon opslaan</span><span class="sxs-lookup"><span data-stu-id="5fcd1-128">To save the vendor card as a template</span></span>
1. <span data-ttu-id="5fcd1-129">Kies op de pagina **Leverancierskaart** de actie **Opslaan als sjabloon**.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-129">On the **Vendor Card** page, choose the **Save as Template** action.</span></span> <span data-ttu-id="5fcd1-130">De pagina **Leveranciersjabloon** opent de weergave van de leverancierkaart als sjabloon.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-130">The **Vendor Template** page opens showing the vendor card as a template.</span></span>
2. <span data-ttu-id="5fcd1-131">Vul de benodigde velden in.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-131">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="5fcd1-132">Als u sjablonen wilt hergebruiken, kiest u de actie **Dimensies**.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-132">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="5fcd1-133">De pagina **Dimensiesjablonen** geeft alle dimensiecodes weer die voor de leverancier zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-133">The **Dimension Templates** page opens showing any dimension codes that are set up for the vendor.</span></span>
4. <span data-ttu-id="5fcd1-134">Bewerk of typ dimensiecodes die van toepassing zijn op nieuwe leverancierkaarten die worden gemaakt met de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-134">Edit or enter dimension codes that will apply to new vendor cards created by using the template.</span></span>
5. <span data-ttu-id="5fcd1-135">Wanneer u de nieuwe leveranciersjabloon hebt voltooid, kiest u de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-135">When you have completed the new vendor template, choose the **OK** button.</span></span>  
   <span data-ttu-id="5fcd1-136">De leveranciersjabloon wordt toegevoegd aan de lijst met leveranciersjablonen, zodat u deze kunt gebruiken om nieuwe leverancierskaarten te maken.</span><span class="sxs-lookup"><span data-stu-id="5fcd1-136">The vendor template is added to the list of vendor templates, so that you can use it to create new vendor cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="5fcd1-137">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5fcd1-137">See Also</span></span>
[<span data-ttu-id="5fcd1-138">Dubbele records samenvoegen</span><span class="sxs-lookup"><span data-stu-id="5fcd1-138">Merge Duplicate Records</span></span>](sales-how-merge-duplicate-records.md)  
[<span data-ttu-id="5fcd1-139">Nummerreeksen maken</span><span class="sxs-lookup"><span data-stu-id="5fcd1-139">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="5fcd1-140">Inkoop</span><span class="sxs-lookup"><span data-stu-id="5fcd1-140">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="5fcd1-141">[Inkopen vastleggen](purchasing-how-record-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="5fcd1-141">[Record Purchases](purchasing-how-record-purchases.md) </span></span>  
<span data-ttu-id="5fcd1-142">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5fcd1-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
