---
title: Standaardregels instellen en gebruiken voor periodieke verkoop en inkopen| Microsoft Docs
description: U kunt verkoopregels en inkoopregels instellen die u vaak maakt en deze vervolgens invoeren op verkoop- en inkoopdocumenten om de regels snel te vullen met standaardgegevens.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 6f7202da4290ae3f6093baed4185649c30d6a199
ms.contentlocale: nl-be
ms.lasthandoff: 09/27/2017

---
# <a name="how-to-create-recurring-sales-and-purchase-lines"></a><span data-ttu-id="04785-103">Procedure: Periodieke verkoop- en inkoopregels maken</span><span class="sxs-lookup"><span data-stu-id="04785-103">How to: Create Recurring Sales and Purchase Lines</span></span>
<span data-ttu-id="04785-104">Als u vaak verkoop- en inkoopregels met dezelfde informatie moet maken, kunt u standaardregels instellen die u dan kunt invoegen op periodieke verkoop- en inkoopdocumenten, bijvoorbeeld voor periodieke aanvullingsorders.</span><span class="sxs-lookup"><span data-stu-id="04785-104">If you often need to create sales and purchase lines with similar information, you can set up standard lines that you can then insert on recurring sales and purchase documents, for example, for recurring replenishment orders.</span></span>  

<span data-ttu-id="04785-105">In de volgende procedure wordt beschreven hoe u werkt met standaardverkoopregels.</span><span class="sxs-lookup"><span data-stu-id="04785-105">The following procedure shows how to work with standard sales lines.</span></span> <span data-ttu-id="04785-106">Dit werkt op een soortgelijke manier voor standaardinkoopregels.</span><span class="sxs-lookup"><span data-stu-id="04785-106">It works in a similar way for standard purchase lines.</span></span>  

## <a name="to-set-up-standard-sales-lines"></a><span data-ttu-id="04785-107">Standaardverkoopregels instellen</span><span class="sxs-lookup"><span data-stu-id="04785-107">To set up standard sales lines</span></span>  
1. <span data-ttu-id="04785-108">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Standaardverkoopcodes** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="04785-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Standard Sales Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="04785-109">Kies in het venster **Standaardverkoopregels** de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="04785-109">In the **Standard Sales Lines** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="04785-110">Vul de benodigde velden in op het sneltabblad **Algemeen**.</span><span class="sxs-lookup"><span data-stu-id="04785-110">On the **General** FastTab, fill the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="04785-111">Voer op het sneltabblad **Regels** gegevens in de velden in om verkoopregels voor te bereiden die de standaardregels reflecteren die u verwacht te gebruiken als terugkerende regels in verkoopdocumenten.</span><span class="sxs-lookup"><span data-stu-id="04785-111">On the **Lines** FastTab, enter information in the fields to prepare sales lines that reflect the standard lines that you expect to use as recurring lines on sales documents.</span></span>  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a><span data-ttu-id="04785-112">Standaardverkoopregels invoegen op een verkoopfactuur</span><span class="sxs-lookup"><span data-stu-id="04785-112">To insert standard sales lines on a sales invoice</span></span>
1. <span data-ttu-id="04785-113">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Facturen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="04785-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="04785-114">Open de verkoopfactuur waarin u een of meer standaardverkoopregels wilt invoegen.</span><span class="sxs-lookup"><span data-stu-id="04785-114">Open the sales invoice that you want to insert one or more standard sales lines on.</span></span>
3. <span data-ttu-id="04785-115">Kies de actie **Periodieke verkoopregels ophalen**.</span><span class="sxs-lookup"><span data-stu-id="04785-115">Choose the **Get Recurring Sales Lines** action.</span></span>
4. <span data-ttu-id="04785-116">Kies in het venster **Periodieke verkoopregels** de opzoekknop in het veld **Code** en selecteer een set standaardverkoopregels.</span><span class="sxs-lookup"><span data-stu-id="04785-116">In the **Recurring Sales Lines** window, choose the lookup button in the **Code** field, and then select a set of standard sales lines.</span></span>
5. <span data-ttu-id="04785-117">Kies de knop **OK** om de standaardverkoopregels op de factuur in te voegen, waar u deze zo kunt gebruiken of de gegevens kunt bewerken.</span><span class="sxs-lookup"><span data-stu-id="04785-117">Choose the **OK** button to insert the standard sales lines on the invoice, where you can reuse as is or edit the information.</span></span>

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a><span data-ttu-id="04785-118">Meerdere verkoopfacturen maken op basis van standaardverkoopregels</span><span class="sxs-lookup"><span data-stu-id="04785-118">To create multiple sales invoices based on standard sales lines</span></span>
<span data-ttu-id="04785-119">U kunt de batchverwerking **Periodieke verkoopfacturen maken** gebruiken om verkoopfacturen te maken volgens de standaardverkoopregels die zijn toegewezen aan de klanten, en met boekingsdatums binnen de datums voor geldig vanaf en geldig tot die u in de standaardverkoopcode opgeeft.</span><span class="sxs-lookup"><span data-stu-id="04785-119">You can use the **Create Recurring Sales Inv.** batch job to create sales invoices according to standard sales lines that are assigned to the customers and with posting dates within the valid-from and valid-to dates that you specify on the standard sales code.</span></span>

<span data-ttu-id="04785-120">In het venster **Periodieke verkoopregels** kunt u ook een betalingsmethode voor automatische incasso en machtiging voor automatische incasso opgeven.</span><span class="sxs-lookup"><span data-stu-id="04785-120">In the **Recurring Sales Lines** window, you can also specify a direct-debit payment method and a direct-debit mandate.</span></span> <span data-ttu-id="04785-121">De verkoopfacturen die zijn gemaakt met de batchverwerking **Periodieke verkoopfacturen maken** bevatten dan informatie die nodig is om de betaling voor de verkoopfacturen met automatische incasso van SEPA te innen.</span><span class="sxs-lookup"><span data-stu-id="04785-121">The sales invoices that are created with the **Create Recurring Sales Inv.** batch job will then include information required to collect payment for the sales invoices with SEPA direct debit.</span></span> <span data-ttu-id="04785-122">Zie voor meer informatie [Betalingen verzamelen via automatische incasso van SEPA](finance-collect-payments-with-sepa-direct-debit.md).</span><span class="sxs-lookup"><span data-stu-id="04785-122">For more information, see [Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).</span></span>

1. <span data-ttu-id="04785-123">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Periodieke verkoopfacturen aanmaken** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="04785-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Create Recurring Sales Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="04785-124">Vul de velden in het venster **Periodieke verkoopfacturen maken** in met de benodigde gegevens.</span><span class="sxs-lookup"><span data-stu-id="04785-124">In the **Create Recurring Sales Inv.** window, fill in the fields as necessary.</span></span>
3. <span data-ttu-id="04785-125">In het veld **Code** voert u de code in voor standaardverkoopregels die aan een klant worden toegewezen voor wie u verkoopfacturen wilt maken.</span><span class="sxs-lookup"><span data-stu-id="04785-125">In the **Code** field, enter the code for standard sales lines assigned to a customer that you want to create sales invoices for.</span></span>
4. <span data-ttu-id="04785-126">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="04785-126">Choose the **OK** button.</span></span>

<span data-ttu-id="04785-127">Verkoopfacturen worden gemaakt voor klanten met de opgegeven standaard klantverkoopcode en een waarde opgegeven voor automatische incasso-informatie voor het boeken op de opgegeven datum.</span><span class="sxs-lookup"><span data-stu-id="04785-127">Sales invoices are created for the customers with the specified standard customer sales code, and any specified direct-debit information, for posting on the specified date.</span></span>

## <a name="see-also"></a><span data-ttu-id="04785-128">Zie ook</span><span class="sxs-lookup"><span data-stu-id="04785-128">See Also</span></span>  
[<span data-ttu-id="04785-129">Verkoop</span><span class="sxs-lookup"><span data-stu-id="04785-129">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="04785-130">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="04785-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

