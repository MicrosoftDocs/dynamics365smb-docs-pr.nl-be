---
title: Een klantenkaart maken om nieuwe klanten te registreren | Microsoft Docs
description: Meer informatie over hoe u een leverancierskaart maakt om een nieuwe leverancier te registreren.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 78710d796ed73d7b4c2505f6cbb8c7d5f41d7320
ms.contentlocale: nl-be
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-register-new-vendors"></a><span data-ttu-id="578bf-103">Procedure: Nieuwe leveranciers registreren</span><span class="sxs-lookup"><span data-stu-id="578bf-103">How to: Register New Vendors</span></span>
<span data-ttu-id="578bf-104">Leveranciers leveren de producten die u verkoopt.</span><span class="sxs-lookup"><span data-stu-id="578bf-104">Vendors provide the products that you sell.</span></span> <span data-ttu-id="578bf-105">Elke leverancier van wie u inkoopt, moet als een leverancierkaart zijn geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="578bf-105">Each vendor that you purchase from must be registered as a vendor card.</span></span>

<span data-ttu-id="578bf-106">Voordat u nieuwe leveranciers kunt vastleggen, moet u verschillende inkoopcodes instellen waaruit u kunt selecteren wanneer u leverancierskaarten invult.</span><span class="sxs-lookup"><span data-stu-id="578bf-106">Before you can register new vendors, you must set up various purchase codes that you can select from when you fill vendor cards.</span></span> <span data-ttu-id="578bf-107">Wanneer alle vereiste stamgegevens zijn gemaakt, kunt u aanvullende gegevens voor de leverancier configureren, zoals het toekennen van een prioriteit aan de leverancier voor betalingsdoeleinden en u kunt artikelen vermelden die deze leverancier en andere leveranciers kunnen leveren.</span><span class="sxs-lookup"><span data-stu-id="578bf-107">When all of the required master data is created, you can perform additional configuration of the vendor, such as prioritize the vendor for payment purposes and list items that the vendor and other vendors can supply.</span></span> <span data-ttu-id="578bf-108">Een andere reeks instellingen die u kunt opgeven, zijn de overeenkomsten met betrekking tot kortingen, prijzen en betalingswijzen.</span><span class="sxs-lookup"><span data-stu-id="578bf-108">Another group of setup tasks for vendors is to record your agreements concerning discounts, prices, and payment methods.</span></span> <span data-ttu-id="578bf-109">Zie voor meer informatie [Inkoop instellen](purchasing-setup-purchasing.md).</span><span class="sxs-lookup"><span data-stu-id="578bf-109">For more information, see [Setting Up Purchasing](purchasing-setup-purchasing.md).</span></span>

<span data-ttu-id="578bf-110">Leverancierskaarten bevatten de informatie die is vereist om producten van de leverancier te kunnen kopen.</span><span class="sxs-lookup"><span data-stu-id="578bf-110">Vendor cards hold the information that is required to buy products from the vendor.</span></span> <span data-ttu-id="578bf-111">Zie voor meer informatie [Procedure: Inkopen vastleggen](purchasing-how-record-purchases.md) en [Procedure: Nieuwe artikelen registreren](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="578bf-111">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md) and [How to: Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="578bf-112">Als leveranciersjablonen voor verschillende leveranciersoorten bestaan, wordt een venster automatisch weergegeven wanneer u een nieuwe leverancierskaart maakt, van waaruit u een geschikte leveranciersjabloon kunt selecteren.</span><span class="sxs-lookup"><span data-stu-id="578bf-112">If vendor templates exist for different vendor types, then a window appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="578bf-113">Als er slechts één leveranciersjabloon bestaat, gebruiken nieuwe leverancierkaarten altijd deze sjabloon.</span><span class="sxs-lookup"><span data-stu-id="578bf-113">If only one vendor template exists, then new vendor cards always use that template.</span></span>

## <a name="to-create-a-new-vendor-card"></a><span data-ttu-id="578bf-114">Een nieuwe leverancierskaart maken</span><span class="sxs-lookup"><span data-stu-id="578bf-114">To create a new vendor card</span></span>
1. <span data-ttu-id="578bf-115">Kies op de startpagina **Leveranciers** om de lijst met bestaande leveranciers te openen.</span><span class="sxs-lookup"><span data-stu-id="578bf-115">On the Home page, choose **Vendors** to open the list of existing vendors.</span></span>  
2. <span data-ttu-id="578bf-116">Kies in het venster **Leveranciers** **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="578bf-116">In the **Vendors** window, Choose **New**.</span></span>

    <span data-ttu-id="578bf-117">Wanneer er meer dan één leveranciersjabloon bestaat, opent er een venster waarin u een leveranciersjabloon kunt selecteren.</span><span class="sxs-lookup"><span data-stu-id="578bf-117">If more than one vendor template exists, then a window opens from which you can select a vendor template.</span></span> <span data-ttu-id="578bf-118">In dat geval volgt u de volgende twee stappen.</span><span class="sxs-lookup"><span data-stu-id="578bf-118">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="578bf-119">Kies in het venster **Selecteer een sjabloon voor een nieuwe leverancier** de sjabloon die u wilt gebruiken voor de nieuwe leverancierskaart.</span><span class="sxs-lookup"><span data-stu-id="578bf-119">In the **Select a template for a new vendor** window, choose the template that you want to use for the new vendor card.</span></span>
4. <span data-ttu-id="578bf-120">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="578bf-120">Choose the **OK** button.</span></span> <span data-ttu-id="578bf-121">Een nieuwe leverancierskaart wordt geopend met enkele velden ingevuld met informatie uit de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="578bf-121">A new vendor card opens with some fields filled with information from the template.</span></span>
5. <span data-ttu-id="578bf-122">Ga door met velden op de leverancierskaart in te vullen of te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="578bf-122">Proceed to fill or change fields on the vendor card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="578bf-123">De leverancier is nu geregistreerd en de leverancierskaart is klaar om voor inkoopdocumenten te worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="578bf-123">The vendor is now registered, and the vendor card is ready to be used on purchase documents.</span></span>

<span data-ttu-id="578bf-124">Als u deze leverancierskaart als sjabloon wilt gebruiken wanneer u nieuwe leverancierskaarten maakt, kunt u deze opslaan als leveranciersjabloon.</span><span class="sxs-lookup"><span data-stu-id="578bf-124">If you want to use this vendor card as a template when you create new vendor cards, you can save it as a vendor template.</span></span> <span data-ttu-id="578bf-125">Zie de volgende onderwerpen voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="578bf-125">For more information, see the following section.</span></span>

## <a name="to-save-the-vendor-card-as-a-template"></a><span data-ttu-id="578bf-126">De leverancierskaart als sjabloon opslaan</span><span class="sxs-lookup"><span data-stu-id="578bf-126">To save the vendor card as a template</span></span>
1. <span data-ttu-id="578bf-127">Kies in het venster **Leverancierskaart** de actie **Opslaan als sjabloon**.</span><span class="sxs-lookup"><span data-stu-id="578bf-127">In the **Vendor Card** window, choose the **Save as Template** action.</span></span> <span data-ttu-id="578bf-128">Het venster **Leveranciersjabloon** opent de weergave van de leverancierkaart als sjabloon.</span><span class="sxs-lookup"><span data-stu-id="578bf-128">The **Vendor Template** window opens showing the vendor card as a template.</span></span>
2. <span data-ttu-id="578bf-129">Vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="578bf-129">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="578bf-130">Als u sjablonen wilt hergebruiken, kiest u de actie **Dimensies**.</span><span class="sxs-lookup"><span data-stu-id="578bf-130">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="578bf-131">Het venster **Dimensiesjablonen** geeft alle dimensiecodes weer die voor de leverancier zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="578bf-131">The **Dimension Templates** window opens showing any dimension codes that are set up for the vendor.</span></span>
4. <span data-ttu-id="578bf-132">Bewerk of typ dimensiecodes die van toepassing zijn op nieuwe leverancierkaarten die worden gemaakt met de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="578bf-132">Edit or enter dimension codes that will apply to new vendor cards created by using the template.</span></span>
5. <span data-ttu-id="578bf-133">Wanneer u de nieuwe leveranciersjabloon hebt voltooid, kiest u de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="578bf-133">When you have completed the new vendor template, choose the **OK** button.</span></span>  
   <span data-ttu-id="578bf-134">De leveranciersjabloon wordt toegevoegd aan de lijst met leveranciersjablonen, zodat u deze kunt gebruiken om nieuwe leverancierskaarten te maken.</span><span class="sxs-lookup"><span data-stu-id="578bf-134">The vendor template is added to the list of vendor templates, so that you can use it to create new vendor cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="578bf-135">Zie ook</span><span class="sxs-lookup"><span data-stu-id="578bf-135">See Also</span></span>
[<span data-ttu-id="578bf-136">Inkoop</span><span class="sxs-lookup"><span data-stu-id="578bf-136">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="578bf-137">[Procedure: Inkopen vastleggen](purchasing-how-record-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="578bf-137">[How to: Record Purchases](purchasing-how-record-purchases.md) </span></span>  
<span data-ttu-id="578bf-138">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="578bf-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

