---
title: Standaardregels instellen voor periodieke verkoop en inkopen | Microsoft Docs
description: U kunt verkoopregels en inkoopregels instellen die u vaak maakt en deze vervolgens invoeren op verkoop- en inkoopdocumenten om de regels snel te vullen met standaardgegevens.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: df4f093ded0a55d45c40be15c5888035d6e3b2df
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="create-recurring-sales-and-purchase-lines"></a><span data-ttu-id="f8356-103">Periodieke verkoop- en inkoopregels maken</span><span class="sxs-lookup"><span data-stu-id="f8356-103">Create Recurring Sales and Purchase Lines</span></span>
<span data-ttu-id="f8356-104">Als u vaak verkoop- en inkoopregels met dezelfde informatie moet maken, kunt u standaardregels instellen die u dan kunt invoegen op periodieke verkoop- en inkoopdocumenten, bijvoorbeeld voor periodieke aanvullingsorders.</span><span class="sxs-lookup"><span data-stu-id="f8356-104">If you often need to create sales and purchase lines with similar information, you can set up standard lines that you can then insert on recurring sales and purchase documents, for example, for recurring replenishment orders.</span></span>  

<span data-ttu-id="f8356-105">In de volgende procedure wordt beschreven hoe u werkt met standaardverkoopregels.</span><span class="sxs-lookup"><span data-stu-id="f8356-105">The following procedure shows how to work with standard sales lines.</span></span> <span data-ttu-id="f8356-106">Dit werkt op een soortgelijke manier voor standaardinkoopregels.</span><span class="sxs-lookup"><span data-stu-id="f8356-106">It works in a similar way for standard purchase lines.</span></span>  

## <a name="to-set-up-standard-sales-lines"></a><span data-ttu-id="f8356-107">Standaardverkoopregels instellen</span><span class="sxs-lookup"><span data-stu-id="f8356-107">To set up standard sales lines</span></span>  
1. <span data-ttu-id="f8356-108">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Standaardverkoopregels** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="f8356-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Sales Lines**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f8356-109">Kies in het venster **Standaardverkoopregels** de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="f8356-109">In the **Standard Sales Lines** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="f8356-110">Vul de benodigde velden in op het sneltabblad **Algemeen**.</span><span class="sxs-lookup"><span data-stu-id="f8356-110">On the **General** FastTab, fill the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="f8356-111">Voer op het sneltabblad **Regels** gegevens in de velden in om verkoopregels voor te bereiden die de standaardregels reflecteren die u verwacht te gebruiken als terugkerende regels in verkoopdocumenten.</span><span class="sxs-lookup"><span data-stu-id="f8356-111">On the **Lines** FastTab, enter information in the fields to prepare sales lines that reflect the standard lines that you expect to use as recurring lines on sales documents.</span></span>  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a><span data-ttu-id="f8356-112">Standaardverkoopregels invoegen op een verkoopfactuur</span><span class="sxs-lookup"><span data-stu-id="f8356-112">To insert standard sales lines on a sales invoice</span></span>
1. <span data-ttu-id="f8356-113">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Facturen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="f8356-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="f8356-114">Open de verkoopfactuur waarin u een of meer standaardverkoopregels wilt invoegen.</span><span class="sxs-lookup"><span data-stu-id="f8356-114">Open the sales invoice that you want to insert one or more standard sales lines on.</span></span>
3. <span data-ttu-id="f8356-115">Kies de actie **Periodieke verkoopregels ophalen**.</span><span class="sxs-lookup"><span data-stu-id="f8356-115">Choose the **Get Recurring Sales Lines** action.</span></span>
4. <span data-ttu-id="f8356-116">Kies in het venster **Periodieke verkoopregels** de opzoekknop in het veld **Code** en selecteer een set standaardverkoopregels.</span><span class="sxs-lookup"><span data-stu-id="f8356-116">In the **Recurring Sales Lines** window, choose the lookup button in the **Code** field, and then select a set of standard sales lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f8356-117">Als u de set doorlopende verkoopregels samen met de batchverwerking **Periodieke verkoopfacturen maken** wilt gebruiken, moet u ook de velden **Geldig vanaf datum** en **Geldig tot datum** in het venster **Periodieke verkoopregels** invullen.</span><span class="sxs-lookup"><span data-stu-id="f8356-117">To use the recurring sales lines set together with the **Create Recurring Sales Invoices** batch job, you must also fill in the **Valid From Date** and **Valid To Date** fields in the **Recurring Sales Lines** window.</span></span> <span data-ttu-id="f8356-118">Zie voor meer informatie het gedeelte "Meerdere verkoopfacturen maken op basis van standaardverkoopregels".</span><span class="sxs-lookup"><span data-stu-id="f8356-118">For more information, see the "To create multiple sales invoices based on standard sales lines" section.</span></span>

5. <span data-ttu-id="f8356-119">Kies de knop **OK** om de standaardverkoopregels op de factuur in te voegen, waar u deze zo kunt gebruiken of de gegevens kunt bewerken.</span><span class="sxs-lookup"><span data-stu-id="f8356-119">Choose the **OK** button to insert the standard sales lines on the invoice where you can reuse them as is or edit the information.</span></span>

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a><span data-ttu-id="f8356-120">Meerdere verkoopfacturen maken op basis van standaardverkoopregels</span><span class="sxs-lookup"><span data-stu-id="f8356-120">To create multiple sales invoices based on standard sales lines</span></span>
<span data-ttu-id="f8356-121">U kunt de batchverwerking **Periodieke verkoopfacturen maken** gebruiken om verkoopfacturen te maken volgens de standaardverkoopregels die zijn toegewezen aan de klanten, en met boekingsdatums binnen de datums voor geldig vanaf en geldig tot die u op de standaardverkoopregels opgeeft.</span><span class="sxs-lookup"><span data-stu-id="f8356-121">You can use the **Create Recurring Sales Invoices** batch job to create sales invoices according to standard sales lines that are assigned to the customers and with posting dates within the valid-from and valid-to dates that you specify on the standard sales lines.</span></span>

> [!NOTE]
> <span data-ttu-id="f8356-122">In het venster **Periodieke verkoopregels** kunt u ook een betalingsmethode voor automatische incasso en machtiging voor automatische incasso opgeven.</span><span class="sxs-lookup"><span data-stu-id="f8356-122">In the **Recurring Sales Lines** window, you can also specify a direct-debit payment method and a direct-debit mandate.</span></span> <span data-ttu-id="f8356-123">De verkoopfacturen die zijn gemaakt met de batchverwerking **Periodieke verkoopfacturen maken** bevatten dan informatie die nodig is om de betaling voor de verkoopfacturen met automatische incasso van SEPA te innen.</span><span class="sxs-lookup"><span data-stu-id="f8356-123">The sales invoices that are created with the **Create Recurring Sales Inv.** batch job will then include information required to collect payment for the sales invoices with SEPA direct debit.</span></span> <span data-ttu-id="f8356-124">Zie voor meer informatie [Betalingen verzamelen via automatische incasso van SEPA](finance-collect-payments-with-sepa-direct-debit.md).</span><span class="sxs-lookup"><span data-stu-id="f8356-124">For more information, see [Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).</span></span>

1. <span data-ttu-id="f8356-125">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Periodieke verkoopfacturen maken** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="f8356-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Create Recurring Sales Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="f8356-126">Vul de velden in het venster **Periodieke verkoopfacturen maken** in met de benodigde gegevens.</span><span class="sxs-lookup"><span data-stu-id="f8356-126">In the **Create Recurring Sales Invoices** window, fill in the fields as necessary.</span></span>
3. <span data-ttu-id="f8356-127">In het filterveld **Code** voert u de code in voor standaardverkoopregels die aan een klant worden toegewezen voor wie u verkoopfacturen wilt maken.</span><span class="sxs-lookup"><span data-stu-id="f8356-127">In the **Code** filter field, enter the code for standard sales lines that are assigned to a customer that you want to create sales invoices for.</span></span>
4. <span data-ttu-id="f8356-128">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="f8356-128">Choose the **OK** button.</span></span>

<span data-ttu-id="f8356-129">Verkoopfacturen worden gemaakt voor klanten met de opgegeven standaard klantverkoopcode en een waarde opgegeven voor automatische incasso-informatie voor het boeken op de opgegeven datum.</span><span class="sxs-lookup"><span data-stu-id="f8356-129">Sales invoices are created for the customers with the specified standard customer sales code, and any specified direct-debit information, for posting on the specified date.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8356-130">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f8356-130">See Also</span></span>  
[<span data-ttu-id="f8356-131">Verkoop</span><span class="sxs-lookup"><span data-stu-id="f8356-131">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="f8356-132">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f8356-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

