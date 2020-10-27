---
title: 'Procedure: een offerte maken voor een op-order-assembleren-verkoop | Microsoft Docs'
description: U kunt assemblagebeheer gebruiken om een assemblageartikel op verzoek van een klant aan te passen tijdens het verkoopproces.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3710cb0e9d3ca4c9fb699f535a6cb3b0be68cb78
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924490"
---
# <a name="quote-an-assemble-to-order-sale"></a><span data-ttu-id="d9635-103">Een offerte maken voor een assembleren voor order-verkoop</span><span class="sxs-lookup"><span data-stu-id="d9635-103">Quote an Assemble-to-Order Sale</span></span>
<span data-ttu-id="d9635-104">U kunt assemblagebeheer gebruiken om een assemblageartikel op verzoek van een klant aan te passen tijdens het verkoopproces.</span><span class="sxs-lookup"><span data-stu-id="d9635-104">You can use assembly management to customize an assembly item to a customer’s request during the sales process.</span></span> <span data-ttu-id="d9635-105">Zie voor meer informatie [Op order geassembleerde artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="d9635-105">For more information, see [Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>  

<span data-ttu-id="d9635-106">Als u een ander soort artikel verkoopt, kunt u ook een verkoopofferte maken voor een aangepast assemblageartikel voordat u deze omzet in een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="d9635-106">As when you sell any other type of item, you can also create a sales quote for a customized assembly item before converting it to a sales order.</span></span> <span data-ttu-id="d9635-107">Dit proces omvat verschillende extra stappen wanneer u het vergelijkt met het maken van een normale verkoopofferte, en gebruikt assemblageoffertes, een variatie van een gekoppelde assemblageorder.</span><span class="sxs-lookup"><span data-stu-id="d9635-107">This process involves several extra steps when you compare it to creating a regular sales quote, and it uses a variation of a linked assembly order, which is an assembly quote.</span></span>

> [!NOTE]  
>  <span data-ttu-id="d9635-108">Zoals alle soorten van offertes worden de aantallen op assemblageoffertes niet gebruikt in beschikbaarheid, plannen of reserveringen.</span><span class="sxs-lookup"><span data-stu-id="d9635-108">Like all types of quotes, the quantities on assembly quotes are not used in availability, planning, or reservations.</span></span>  

## <a name="to-create-a-sales-quote-for-an-assemble-to-order-item"></a><span data-ttu-id="d9635-109">Een verkoopofferte voor een op-order-assembleren-artikel maken</span><span class="sxs-lookup"><span data-stu-id="d9635-109">To create a sales quote for an assemble-to-order item</span></span>  
1.  <span data-ttu-id="d9635-110">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopofferte** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="d9635-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Quote** , and then choose the related link.</span></span>  
2.  <span data-ttu-id="d9635-111">Maak een nieuwe verkoopofferteregel met één regel voor een assemblageartikel.</span><span class="sxs-lookup"><span data-stu-id="d9635-111">Create a sales quote line with one line for an assembly item.</span></span> <span data-ttu-id="d9635-112">Zie voor meer informatie [Verkoopoffertes maken](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="d9635-112">For more information, see [Make Sales Quotes](sales-how-make-offers.md).</span></span>  
3.  <span data-ttu-id="d9635-113">Voer de volledige aantal het in veld **Aantal voor op order assembleren** in.</span><span class="sxs-lookup"><span data-stu-id="d9635-113">In the **Qty. to Assemble to Order** field, enter the full quantity.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="d9635-114">U moet geen offerte maken voor een gedeeltelijke hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="d9635-114">You should not quote a partial quantity.</span></span> <span data-ttu-id="d9635-115">Daarom moet u dezelfde hoeveelheid invoeren die u hebt ingevoerd in het veld **Hoeveelheid** op de verkoopofferteregel.</span><span class="sxs-lookup"><span data-stu-id="d9635-115">Therefore, you must enter the same quantity that you entered in the **Quantity** field on the sales quote line.</span></span>  

4.  <span data-ttu-id="d9635-116">Kies op het sneltabblad **Regels** de optie **Regel** en vervolgens **Op order assembleren** en **Op orderregels assembleren** .</span><span class="sxs-lookup"><span data-stu-id="d9635-116">On the **Lines** FastTab, choose **Line** , choose **Assemble to Order** , and then choose **Assemble-to-Order Lines** .</span></span> <span data-ttu-id="d9635-117">Of kies het veld **Aant. op order assembleren** op de regel.</span><span class="sxs-lookup"><span data-stu-id="d9635-117">Alternatively, choose the **Qty. to Assemble to Order** field on the line.</span></span>  
5.  <span data-ttu-id="d9635-118">Bekijk of wijzig de assemblageorderregels volgens de offerte die de klant heeft aangevraagd op de pagina **Op orderregels assembleren** .</span><span class="sxs-lookup"><span data-stu-id="d9635-118">On the **Assemble-to-Order Lines** page, review or modify the assembly order lines according to the quote that the customer is requesting.</span></span> <span data-ttu-id="d9635-119">Als u meer informatie wilt, kiest u de actie **Document weergeven** om het volledige offerteraamcontract te openen.</span><span class="sxs-lookup"><span data-stu-id="d9635-119">If you want to view more information, choose the **Show Document** action to open the complete blanket quote order.</span></span> <span data-ttu-id="d9635-120">U kunt de inhoud van de meeste velden niet wijzigen en u kunt niet boeken.</span><span class="sxs-lookup"><span data-stu-id="d9635-120">You cannot change the contents of most fields, and you cannot post.</span></span>  
6.  <span data-ttu-id="d9635-121">Wanneer u de assemblageorderregels hebt bijgewerkt volgens de offerte sluit u de pagina **Op orderregels assembleren** om terug te keren naar de pagina **Verkoopofferte** .</span><span class="sxs-lookup"><span data-stu-id="d9635-121">When you have adjusted the assembly order lines according to the quote, close the **Assemble-to-Order Lines** page to return to the **Sales Quote** page.</span></span>  
7.  <span data-ttu-id="d9635-122">Als de klant de offerte heeft geaccepteerd, maakt u een verkooporder voor het genoteerde assemblageartikel.</span><span class="sxs-lookup"><span data-stu-id="d9635-122">If the customer accepts the quote, then create a sales order for the quoted assembly item.</span></span> <span data-ttu-id="d9635-123">Zie voor meer informatie [Verkoopoffertes maken](sales-how-make-offers.md).</span><span class="sxs-lookup"><span data-stu-id="d9635-123">For more information, see [Make Sales Quotes](sales-how-make-offers.md).</span></span> <span data-ttu-id="d9635-124">De gekoppelde assemblageofferte en eventuele aanpassingen zijn gekoppeld aan die nieuwe verkooporder, als voorbereiding op de assemblage van het artikel of de artikelen die verkocht worden.</span><span class="sxs-lookup"><span data-stu-id="d9635-124">The linked assembly quote and any customizations are linked to that new sales order to prepare for assembly of the item or items to be sold.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d9635-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d9635-125">See Also</span></span>  
[<span data-ttu-id="d9635-126">Assemblagebeheer</span><span class="sxs-lookup"><span data-stu-id="d9635-126">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="d9635-127">Werken met stuklijsten</span><span class="sxs-lookup"><span data-stu-id="d9635-127">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="d9635-128">Voorraad</span><span class="sxs-lookup"><span data-stu-id="d9635-128">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="d9635-129">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="d9635-129">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="d9635-130">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d9635-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
