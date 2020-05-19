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
ms.date: 04/27/2020
ms.author: sgroespe
ms.openlocfilehash: ce41715830545c89651bac7d117b6c356650b7c3
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324186"
---
# <a name="register-new-vendors"></a><span data-ttu-id="3c512-103">Nieuwe leveranciers registreren</span><span class="sxs-lookup"><span data-stu-id="3c512-103">Register New Vendors</span></span>
<span data-ttu-id="3c512-104">Leveranciers leveren de producten die u verkoopt.</span><span class="sxs-lookup"><span data-stu-id="3c512-104">Vendors provide the products that you sell.</span></span> <span data-ttu-id="3c512-105">Elke leverancier van wie u inkoopt, moet als een leverancierkaart zijn geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="3c512-105">Each vendor that you purchase from must be registered as a vendor card.</span></span>

<span data-ttu-id="3c512-106">Voordat u nieuwe leveranciers kunt vastleggen, moet u verschillende inkoopcodes instellen waaruit u kunt selecteren wanneer u leverancierskaarten invult.</span><span class="sxs-lookup"><span data-stu-id="3c512-106">Before you can register new vendors, you must set up various purchase codes that you can select from when you fill vendor cards.</span></span> <span data-ttu-id="3c512-107">Wanneer alle vereiste stamgegevens zijn gemaakt, kunt u aanvullende gegevens voor de leverancier configureren, zoals het toekennen van een prioriteit aan de leverancier voor betalingsdoeleinden en u kunt artikelen vermelden die deze leverancier en andere leveranciers kunnen leveren.</span><span class="sxs-lookup"><span data-stu-id="3c512-107">When all of the required master data is created, you can perform additional configuration of the vendor, such as prioritize the vendor for payment purposes and list items that the vendor and other vendors can supply.</span></span> <span data-ttu-id="3c512-108">Een andere reeks instellingen die u kunt opgeven, zijn de overeenkomsten met betrekking tot kortingen, prijzen en betalingswijzen.</span><span class="sxs-lookup"><span data-stu-id="3c512-108">Another group of setup tasks for vendors is to record your agreements concerning discounts, prices, and payment methods.</span></span> <span data-ttu-id="3c512-109">Zie voor meer informatie [Inkoop instellen](purchasing-setup-purchasing.md).</span><span class="sxs-lookup"><span data-stu-id="3c512-109">For more information, see [Setting Up Purchasing](purchasing-setup-purchasing.md).</span></span>

<span data-ttu-id="3c512-110">Leverancierskaarten bevatten de informatie die is vereist om producten van de leverancier te kunnen kopen.</span><span class="sxs-lookup"><span data-stu-id="3c512-110">Vendor cards hold the information that is required to buy products from the vendor.</span></span> <span data-ttu-id="3c512-111">Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md) en [Nieuwe artikelen registreren](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="3c512-111">For more information, see [Record Purchases](purchasing-how-record-purchases.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="3c512-112">Als leveranciersjablonen voor verschillende leveranciersoorten bestaan, wordt een pagina automatisch weergegeven wanneer u een nieuwe leverancierskaart maakt, van waaruit u een geschikte leveranciersjabloon kunt selecteren.</span><span class="sxs-lookup"><span data-stu-id="3c512-112">If vendor templates exist for different vendor types, then a page appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="3c512-113">Als er slechts één leveranciersjabloon bestaat, gebruiken nieuwe leverancierkaarten altijd deze sjabloon.</span><span class="sxs-lookup"><span data-stu-id="3c512-113">If only one vendor template exists, then new vendor cards always use that template.</span></span>
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="to-create-a-new-vendor-card"></a><span data-ttu-id="3c512-114">Een nieuwe leverancierskaart maken</span><span class="sxs-lookup"><span data-stu-id="3c512-114">To create a new vendor card</span></span>
1. <span data-ttu-id="3c512-115">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Leveranciers** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="3c512-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="3c512-116">Kies op de pagina **Leveranciers** de optie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="3c512-116">On the **Vendors** page, Choose **New**.</span></span>

    <span data-ttu-id="3c512-117">Wanneer er meer dan één leveranciersjabloon bestaat, opent er een pagina waarin u een leveranciersjabloon kunt selecteren.</span><span class="sxs-lookup"><span data-stu-id="3c512-117">If more than one vendor template exists, then a page opens from which you can select a vendor template.</span></span> <span data-ttu-id="3c512-118">In dat geval volgt u de volgende twee stappen.</span><span class="sxs-lookup"><span data-stu-id="3c512-118">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="3c512-119">Kies op de pagina **Selecteer een sjabloon voor een nieuwe leverancier** de sjabloon die u wilt gebruiken voor de nieuwe leverancierskaart.</span><span class="sxs-lookup"><span data-stu-id="3c512-119">On the **Select a template for a new vendor** page, choose the template that you want to use for the new vendor card.</span></span>
4. <span data-ttu-id="3c512-120">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="3c512-120">Choose the **OK** button.</span></span> <span data-ttu-id="3c512-121">Een nieuwe leverancierskaart wordt geopend met enkele velden ingevuld met informatie uit de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="3c512-121">A new vendor card opens with some fields filled with information from the template.</span></span>
5. <span data-ttu-id="3c512-122">Ga door met velden op de leverancierskaart in te vullen of te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="3c512-122">Proceed to fill or change fields on the vendor card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="3c512-123">Als u het factuuradres dat voor elke factuur van een leverancier wordt gebruikt niet kent, vult u het veld **Betaaladres** niet in.</span><span class="sxs-lookup"><span data-stu-id="3c512-123">If you do not know the invoicing address that will be used for every invoice from a vendor, do not fill in the **Pay-to** field.</span></span> <span data-ttu-id="3c512-124">Kies in dat geval het nummer van de factuurleverancier nadat u een inkoopofferte, inkooporder of inkoopkop hebt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="3c512-124">Instead, choose the pay-to vendor number after you have set up a purchase quote, order, or invoice header.</span></span>

<span data-ttu-id="3c512-125">De leverancier is nu geregistreerd en de leverancierskaart is klaar om voor inkoopdocumenten te worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="3c512-125">The vendor is now registered, and the vendor card is ready to be used on purchase documents.</span></span>

<span data-ttu-id="3c512-126">Als u deze leverancierskaart als sjabloon wilt gebruiken wanneer u nieuwe leverancierskaarten maakt, kunt u deze opslaan als leveranciersjabloon.</span><span class="sxs-lookup"><span data-stu-id="3c512-126">If you want to use this vendor card as a template when you create new vendor cards, you can save it as a vendor template.</span></span> <span data-ttu-id="3c512-127">Zie de volgende onderwerpen voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="3c512-127">For more information, see the following section.</span></span>

### <a name="deleting-vendor-cards"></a><span data-ttu-id="3c512-128">Leverancierskaarten verwijderen</span><span class="sxs-lookup"><span data-stu-id="3c512-128">Deleting Vendor Cards</span></span>
<span data-ttu-id="3c512-129">Als u een transactie voor een leverancier hebt geboekt, kunt u de kaart niet verwijderen omdat de grootboekposten mogelijk nodig zijn voor controle.</span><span class="sxs-lookup"><span data-stu-id="3c512-129">If you have posted a transaction for a vendor, you cannot delete the card because the ledger entries may be needed for auditing.</span></span> <span data-ttu-id="3c512-130">Als u leverancierskaarten met grootboekposten wilt verwijderen, neemt u contact op met de Microsoft-partner om dat via code te doen.</span><span class="sxs-lookup"><span data-stu-id="3c512-130">To delete vendor cards with ledger entries, contact to Microsoft partner to do so through code.</span></span>

## <a name="to-save-the-vendor-card-as-a-template"></a><span data-ttu-id="3c512-131">De leverancierskaart als sjabloon opslaan</span><span class="sxs-lookup"><span data-stu-id="3c512-131">To save the vendor card as a template</span></span>
1. <span data-ttu-id="3c512-132">Kies op de pagina **Leverancierskaart** de actie **Opslaan als sjabloon**.</span><span class="sxs-lookup"><span data-stu-id="3c512-132">On the **Vendor Card** page, choose the **Save as Template** action.</span></span> <span data-ttu-id="3c512-133">De pagina **Leveranciersjabloon** opent de weergave van de leverancierkaart als sjabloon.</span><span class="sxs-lookup"><span data-stu-id="3c512-133">The **Vendor Template** page opens showing the vendor card as a template.</span></span>
2. <span data-ttu-id="3c512-134">Vul de benodigde velden in.</span><span class="sxs-lookup"><span data-stu-id="3c512-134">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="3c512-135">Als u sjablonen wilt hergebruiken, kiest u de actie **Dimensies**.</span><span class="sxs-lookup"><span data-stu-id="3c512-135">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="3c512-136">De pagina **Dimensiesjablonen** geeft alle dimensiecodes weer die voor de leverancier zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="3c512-136">The **Dimension Templates** page opens showing any dimension codes that are set up for the vendor.</span></span>
4. <span data-ttu-id="3c512-137">Bewerk of typ dimensiecodes die van toepassing zijn op nieuwe leverancierkaarten die worden gemaakt met de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="3c512-137">Edit or enter dimension codes that will apply to new vendor cards created by using the template.</span></span>
5. <span data-ttu-id="3c512-138">Wanneer u de nieuwe leveranciersjabloon hebt voltooid, kiest u de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c512-138">When you have completed the new vendor template, choose the **OK** button.</span></span>  
   <span data-ttu-id="3c512-139">De leveranciersjabloon wordt toegevoegd aan de lijst met leveranciersjablonen, zodat u deze kunt gebruiken om nieuwe leverancierskaarten te maken.</span><span class="sxs-lookup"><span data-stu-id="3c512-139">The vendor template is added to the list of vendor templates, so that you can use it to create new vendor cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="3c512-140">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3c512-140">See Also</span></span>
[<span data-ttu-id="3c512-141">Dubbele records samenvoegen</span><span class="sxs-lookup"><span data-stu-id="3c512-141">Merge Duplicate Records</span></span>](sales-how-merge-duplicate-records.md)  
[<span data-ttu-id="3c512-142">Nummerreeksen maken</span><span class="sxs-lookup"><span data-stu-id="3c512-142">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="3c512-143">Inkoop</span><span class="sxs-lookup"><span data-stu-id="3c512-143">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="3c512-144">[Inkopen vastleggen](purchasing-how-record-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="3c512-144">[Record Purchases](purchasing-how-record-purchases.md) </span></span>  
<span data-ttu-id="3c512-145">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3c512-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
